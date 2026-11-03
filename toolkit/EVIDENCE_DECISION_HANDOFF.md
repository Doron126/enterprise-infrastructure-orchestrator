# Evidence & Decision Handoff

A03 · 1.1 · 3 November 2026

## Use this when

An engineer or receiving reviewer needs a small record after a pause, changed evidence or responsibility transfer, including moving a project between ChatGPT conversations. It is optional, even on long projects. See the [conversation migration guide](../docs/CHATGPT_CONVERSATION_HANDOFF.md) for that use case.

For a one-shot answer, or when the existing ticket/document already preserves sufficient context and authority, omit this asset and use native ChatGPT directly. This is not a project-management system, hidden memory or a required bundle.

## Inputs

- **Required:** project/customer/object scope; needed facts/decisions with source locators; owner-selected authoritative revision or unresolved authority; next question/action if known, otherwise the state needed to identify it.
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

The following sections are optional; include them when relevant, including for conversation migration. Refer to the fact and decision records above rather than repeating them; use compact bullets for simple work.

**Established Instructions and Constraints:** [current user-established requirements needed to continue: architecture, platforms/versions, security and operational boundaries, accepted or prohibited approaches, validation criteria, names and environment limits; identify superseded instructions as such where needed]. Distinguish user instructions and approved approaches from assistant suggestions. Include only necessary sanitized information, never secrets.

**Completed Work and Acceptance Status:** [deliverables, changes and partial work; tests and observed results, failures and baseline defects; pending validation or acceptance; rejected approaches and reasons; artifact paths, versions, commit IDs and evidence locators where relevant]. Mark planned versus executed, executed versus verified, and verified versus accepted; identify acceptance authority and its basis if established. Recommendations are not acceptance. Historical acceptance does not authorize a new action.

**Continuation Point:** [latest known state and last meaningful completed action; active task, blockers and outstanding decisions; smallest useful next action, dependencies and required inputs; relevant files, commands, artifacts or references; permissions or operational approvals still required]. If the state or next action is unknown, say so and identify what is needed to establish it; do not invent one. Avoid repeating completed work unnecessarily, but do not promote an unverified report to a verified result.

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

## Revision note

1.1 adds optional instructions and constraints, completed work and acceptance, and continuation point sections, plus a conversation migration guide. Existing 1.0 handoffs remain usable; add the new sections only when relevant.

## Maintenance and retirement

Maintainer: Doron Shamo. Role expectation: an engineer experienced in evidence handoffs/revisions. Archive if existing tickets/records suffice, it is not reused, or duplicate-state maintenance exceeds its handoff value.
