# Domain examples

Read this file when the diagram needs realistic event-topic names, cache schemas, endpoint labels, or DLQ notes. The patterns are reusable across domains; the concrete values are drawn from real banking and commerce architectures and are illustrative, not mandatory.

## Event topic naming

`<system>.<domain>.<event>.<ENV>`

| Domain | Example |
| --- | --- |
| E-commerce and retail | `ecommerce.logistics.order.fulfilled.PROD` |
| Digital lending and fintech | `lending.origination.loan.disbursed.DEV` |
| Banking rails | `vb.int.notification.inbox.DEV`, `banking.transfer.completed.PROD` |
| Supply chain and IoT | `iot.telemetry.gateway.heartbeat.UAT` |

Kafka edge style:

```
edgeStyle=orthogonalEdgeStyle;dashed=1;flowAnimation=1;strokeColor=#FF6A00;strokeWidth=2;endArrow=classic;
```

DLQ callout note, amber (`fillColor=#fad7ac;strokeColor=#b46504`):

```
TBC: DLQ on event processing failure / retry policy
```

## Cache schema note

Architects annotate Redis key structure and scripts next to the Redis icon:

```text
KEY:     VB_INT_PARTNER::AUTH::{AUTH_CODE}
VALUE:   cifID, ccdID, accessibleData
EXPIRED: 15 min
```

```text
EVAL Lua script: reserve, accept, cancel, timeout_reservation
```

## Endpoint labels

Real diagrams mix step numbers, HTTP methods, paths, and change markers:

```text
1 - POST /v1/restriction/check (NEW)
2 - POST /v1/campaign/reserve
3.1(opt) - POST /v1/campaign/cancel
4 - POST /v1/campaign/accept
POST /vb/v1/bff-mobile-deposit-sof/v1/account/inquiry/summary (enhance)
POST /v1/deposit/account/inquiry
async event insert/update campaign_quota
fallback: redis data
```

The exact paths belong to the system being documented; keep the shape and replace the values.
