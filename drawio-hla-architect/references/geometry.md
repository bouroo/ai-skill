# Geometry and clearance rules

Read this file before placing nodes, sizing lanes, centring a lone component, or routing a bypass corridor.

## Clearance

- Outer system container at `y = 25`, child swimlanes at `y = 80`: 55px of vertical clearance so the container title is never covered.
- Swimlane headers occupy `y = 80` to `115`. Every microservice, pod, and database icon starts at `y >= 120`.
- An outer container's right edge (`x + width`) ends at least 20 to 25px before an adjacent independent lane. A container ending at `x = 1790` means the next lane starts at `x = 1820`.
- Component-to-component spacing is at least 40px horizontally and 50px vertically. Pods, cylinders, and note callouts never overlap.
- Edge labels offset by `dy = -12` or `dy = 12` and never collide with pod borders or cylinders.

## Default seven-lane widths

`client=240, gateway=180, bff=220, orch=260, core=485, adaptor=260, external=520`.

## Centring a single component

A lane holding one component on a track centres it:

```
center_x = lane_x + (lane_width - component_width) / 2
```

Worked positions for a 44px component:

| Lane | `lane_x` | width | `center_x` |
| --- | --- | --- | --- |
| Client | 40 | 240 | 138 |
| Gateway | 295 | 180 | 363 |
| Channel BFF | 505 | 220 | 593 |
| Orchestration | 740 | 260 | 848 |
| Domain Core | 1015 | 485 | 1236 |
| Adaptor | 1515 | 260 | 1623 |
| External | 1820 | 520 | 2058 |

For a 160px component in the external lane, `center_x = 2000`.

`HLADiagramBuilder` computes this: pass `lane="lane_id"` to `add_pod`, or call `get_lane_center_x(lane_id, width)` and `get_lane_col_x(lane_id, col, total_cols, width)` for multi-column tracks.

## Bypass corridors

Long return flows (external async webhooks returning from the rightmost lane to the leftmost, token handoffs to web views) route through the top corridor (`Y < 120`) or the bottom corridor (`Y > 800`) using explicit orthogonal waypoints:

```xml
<Array as="points"><mxPoint x="..." y="..."/></Array>
```

Never route them diagonally across middle tiers, and keep `jumpStyle=arc;jumpSize=6;` on every edge so crossings render as arc bridges.
