# Enterprise Infra Orchestrator — Infrastructure Engineering Toolkit

A small set of reusable Markdown engineering assets for reviewable infrastructure assessments, changes and handoffs. Each is optional and independently usable. No installation or build is needed.

**Published 10 September 2026.** A01, A02 and A03 each have independent revision 1.0. Accountable maintainer: Doron Shamo.

## Choose what you need

| Need | Use |
|---|---|
| A simple question, definition or explanation | Native ChatGPT; no asset |
| A scoped supportability or compatibility decision | [A01 — Supportability Assessment](toolkit/SUPPORTABILITY_ASSESSMENT.md) |
| Consequential change or acceptance planning | [A02 — Change & Acceptance Worksheet](toolkit/CHANGE_ACCEPTANCE_WORKSHEET.md) |
| Continue work across time, people or changed evidence | [A03 — Evidence & Decision Handoff](toolkit/EVIDENCE_DECISION_HANDOFF.md); optional |

If an existing ticket or document already preserves sufficient context, omit A03. You never need to use all three assets.

## How to use

1. Open or attach the relevant asset.
2. Provide the task and permitted, sanitized evidence.
3. Ask ChatGPT to produce the requested engineering artifact using it.
4. Review the output before operational use.

## Important boundaries

These assets are advisory. They execute no infrastructure changes, provide no automatic compatibility certification and manage no persistent project state. A procedure or planned acceptance criterion is not execution authority or an observed result. Missing evidence may remain unknown; review consequential assumptions and recovery dependencies.

Use only permitted, sanitized evidence. Restricted-network snapshots retain their capture date and scope limitations and require approved transfer for connected analysis. The toolkit provides no offline ChatGPT inference.

## Legacy Plugin

The published v1.3.4 Plugin remains separate under limited maintenance, with no current forced retirement date. Toolkit use requires no Plugin installation and causes no automatic migration. See the [legacy coexistence note](docs/LEGACY_PLUGIN_AND_TOOLKIT.md).

## Maintenance and revisions

Assets evolve independently. Maintenance covers revision/index accuracy, broken links, consequential clarity or safety defects and material contract changes. Changed fields, semantics or evidence requirements need a concise migration note. Assets may be archived or deprecated when no longer useful or responsibly maintainable.

Vendor/version facts belong in task evidence. Maintenance promises no live compatibility catalog, automatic verification or synchronization, monitoring, response SLA, perpetual support or compatibility with every future model.
