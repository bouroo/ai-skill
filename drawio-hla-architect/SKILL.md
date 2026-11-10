---
name: drawio-hla-architect
description: Author and QA-audit enterprise High-Level Architecture (HLA) diagrams as draw.io files: seven isolated swimlanes (client, gateway, BFF, orchestration, core, adaptor, external), Kubernetes pod and technology icon styling, a lifecycle colour matrix, a mandatory standard-palette page, zero-orphan topologically anchored edges, sequence-labelled flows, and a bundled strict validator. Use when the user asks for an HLA, HLD, solution-architecture diagram, draw.io or .drawio file, swimlane architecture, integration or sequence flow, or wants an existing .drawio architecture reviewed, audited, or fixed, even if they do not name draw.io or HLA directly. Not for free-form whiteboard sketches, UML class diagrams, or image generation with no architecture content.
---

# Draw.io Enterprise HLA Architecture

Author and audit High-Level Architecture (HLA) diagrams in draw.io format: `<name>.drawio`, never `.drawio.xml` or `.xml`. The standard is domain-agnostic; the tiers, colours, and invariants apply to banking, fintech, retail, e-commerce, logistics, healthcare, telecom, or any multi-tier enterprise system.

## Workflow

- [ ] 1. Establish scope: systems, inbound rails, sync and async callbacks, lifecycle state per component (new, enhanced, existing, external).
- [ ] 2. Generate the two-page skeleton: `python3 scripts/generate_hla_template.py`. It resolves `resources/standard_icons_tab.xml` relatively and writes the `.drawio` file to the repository root, outside this skill directory.
- [ ] 3. Lay out seven dedicated swimlanes and place components, reading `references/geometry.md` first.
- [ ] 4. Connect every node with anchored, sequence-labelled edges.
- [ ] 5. Validate: `python3 scripts/qa_verify_hla.py <file>.drawio --strict`.
- [ ] 6. Fix every reported error, re-run, and proceed only on `STATUS: PASSED (0 errors)`.

## Two specialist agents

- `agents/hla_architect_agent.md` — read when drafting a full diagram from business requirements, user stories, or a PRD.
- `agents/hla_qa_reviewer_agent.md` — read when auditing an existing diagram against the invariants.

## Nine mandatory invariants

1. **Two pages minimum.** Page 1 is the `HLA Overview`; Page 2 is the `Standard Colors and Icons` palette tab, which carries the lifecycle matrix, connector samples, pod shapes, database cylinders, and technology icons. The generator embeds the official Page 2 XML.
2. **One dedicated swimlane per tier.** Never merge tiers into one column. The universal seven: Client & Inbound Rails, Gateway, Channel BFF (`bff-*`), Orchestration (`orch-*`), Domain Core (`core-*`), Adaptor (`adaptor-*`), Enterprise Platforms & External Rails. Lanes 3 to 6 may sit inside a named platform container, or the container may be omitted for multi-platform ecosystems.
3. **Zero orphans, strict anchoring.** Every component has inbound and outbound connectivity. Every `<mxCell edge="1">` declares `source="<id>"` and `target="<id>"`; no floating lines. Async callback receivers (`orch-*-callback`) take the external webhook through the top corridor into the inbound endpoint, route through the gateway, then call the core.
4. **Sequence-labelled edges.** Format `<step> - <HTTP_METHOD> <path> [(NEW|enhance|opt)]`, or an event description such as `async event insert/update <entity>`, or `fallback: <store>`. Empty connections are forbidden.
5. **Minimise crossings.** Keep related components on one horizontal Y band. Route long return and webhook flows through the top corridor (Y < 120) or bottom corridor (Y > 800) with explicit orthogonal waypoints; never cut diagonally across middle tiers. Every edge carries `jumpStyle=arc;jumpSize=6;`.
6. **Lifecycle colour matrix.** New `#03CCFF`, Enhanced `#92D14F`, Existing `#BFBFBF`, External `#EF7D30`, Kafka bus `#FF6A00` (dashed, animated). Apply the matching fill, stroke width, database, and edge colours.
7. **HTML and newline safety.** Every icon and cylinder style appends `html=1;whiteSpace=wrap;`. Without it draw.io renders `<br>` literally on the canvas.
8. **Kafka standards.** Topic names follow `<system>.<domain>.<event>.<ENV>`; edges are dashed and animated in `#FF6A00`; add an amber DLQ note when retry policy is undecided.
9. **Redis and cache documentation.** Record key structure, value fields, TTL, and any Lua scripts next to the Redis icon.

## Gotchas

- Sprite and image icons need `html=1;`, and the multiline label needs `whiteSpace=wrap;`; otherwise raw `<br>` tags appear in the diagram.
- A pod style without connection points cannot be anchored; use the full pod style from `references/style-strings.md` rather than a minimal shape.
- Omitting `source` and `target` still renders a line, so QA must catch it; the strict auditor does.
- The Page 2 tab ids in upstream files are project-specific; keep the embedded standard tab rather than inventing ids.
- A single component in a lane must be centred, not left-aligned; compute it instead of eyeballing it.
- Generated files belong at the repository root; do not write them inside the skill directory.

## Bundled references and tools

| Path | Load when |
| --- | --- |
| `references/geometry.md` | Placing nodes, sizing lanes, centring a single component, or routing bypass corridors |
| `references/style-strings.md` | Writing pod, cylinder, icon, or edge style attributes, including the embedded vector icons |
| `references/domain-examples.md` | Realistic topic names, Redis schemas, and endpoint label examples are needed |
| `resources/standard_icons_tab.xml` | The generator already embeds it; read only to inspect or repair the palette page |
| `scripts/generate_hla_template.py` | Creating the initial two-page `.drawio` skeleton |
| `scripts/qa_verify_hla.py` | Validating or strict-auditing a finished diagram |

## Pre-flight sign-off

- [ ] File is `<name>.drawio` with no `.xml` suffix.
- [ ] Root has two pages: the HLA overview and the standard palette tab.
- [ ] Each tier sits in its own swimlane; no tier columns merged.
- [ ] Geometry holds the clearance rules in `references/geometry.md`; nothing overlaps.
- [ ] Stroke colours match the lifecycle matrix, including edge colours.
- [ ] Every edge is anchored and sequence-labelled; no orphans.
- [ ] Callback path is complete: webhook, gateway, callback receiver, core.
- [ ] All multiline icons carry `html=1;whiteSpace=wrap;`; all edges carry arc jumps.
- [ ] Kafka topics follow the naming convention with animated dashed edges.
- [ ] `python3 scripts/qa_verify_hla.py <file>.drawio --strict` reports `STATUS: PASSED (0 errors)`.
