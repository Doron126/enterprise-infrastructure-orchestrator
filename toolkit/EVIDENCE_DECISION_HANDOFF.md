# Evidence & Decision Handoff

A03 · 1.0 · 10 September 2026

## Use this when

An engineer or receiving reviewer needs a small record after a pause, changed evidence or responsibility transfer. It is optional, even on long projects.

For a one-shot answer, or when the existing ticket/document already preserves sufficient context and authority, omit this asset and use native ChatGPT directly. This is not a project-management system, hidden memory or a required bundle.

## Inputs

- **Required:** project/customer/object scope; needed facts/decisions with source locators; owner-selected authoritative revision or unresolved authority; next question/action.
- **Useful if available:** prior handoff/parent, dated new evidence and decision dependencies. A first handoff has no parent; missing history stays missing.
- **Only if necessary:** other assets, full inventories or attachments. Do not include whole conversations/customer archives by default.

## Handoff to return

Keep one Markdown record. Plain bullets can replace the tables when shorter; no parallel JSON/CSV copy is required.

**Scope:** [customer/project/site and stable affected identities; state unknown identities explicitly].

**Authority:** [record revision; parent or first record; as-of date; who explicitly selected this revision, with statement/reference, or unresolved]. Record revision is distinct from this template's revision.

**Source boundary:** [supplied evidence / permitted research and transfer scope].

| Relevant fact or relationship | Evidence / date / scope and status | Decision consequence |
|---|---|---|
| [only what the next engineer needs] | [source/file/section locator; observed for its capture, owner-reported, inferred, conflicted or unknown; stale limits] | [affected decision; unchanged findings can say none] |

| Decision | Current status and basis | Open question / next action |
|---|---|---|
| [named decision; local ID only if useful] | [supported by which facts; current, on hold, superseded or disputed; not a new approval] | [smallest useful next step; owner if known] |

**Change since parent — optional:** [changed fact/source → directly affected findings and downstream decisions; what is preserved; unresolved competing revisions]. Omit for a first handoff with no known delta.

## Continuity boundaries

Only explicit owner selection establishes authority, not a later timestamp. Retain competing revisions and mark affected decisions disputed until reconciled. Only conclusions independent of that conflict can continue.

A changed fact selectively reopens dependent findings/decisions. Preserve unrelated findings, dated operational evidence and other blockers on an already-held decision. Same-name objects in other customers/projects stay separate. Local labels are not collected native identifiers.

Unavailable source content leaves a locator and an explicit limit, not freshly verified evidence. Unresolved identity, authority or dependency limits the affected continuation; no reconstructed history or blanket validation.

Store minimum sanitized context and no secrets. Restricted-environment evidence requires approved transfer before analysis elsewhere. Vendor snapshots retain original limits. Unspecified research permission means supplied evidence only. No automatic refresh, private-network access or offline ChatGPT inference is provided. Past approval does not authorize present execution.

## Compact synthetic example

Fictional project Larch, site East, gateway `gw-02` / object `larch-g2`. The service owner's supplied note explicitly selects record r2, parent r1, as of 9 September. Research/transfer boundary: supplied sanitized records only.

| Fact / source | Revision consequence |
|---|---|
| E1: 8 September export showed two active paths, A and B | Preserved as historical observation |
| E2: 9 September same-object export shows only path A active; B health unresolved | Reopens D1, the planned A restart: **HOLD**, because remaining service coverage is unproven |
| E1 also recorded configuration label `edge-east` | Preserved for that capture; E2 supplies no change to it and does not freshly verify it |

Next: obtain a current read-only B-path health record before reassessing D1. r2 does not approve a restart or silently delete r1. No full project bundle is needed.

## Maintenance and retirement

Maintainer: Doron Shamo. Role expectation: an engineer experienced in evidence handoffs/revisions. Archive if existing tickets/records suffice, it is not reused, or duplicate-state maintenance exceeds its handoff value.
