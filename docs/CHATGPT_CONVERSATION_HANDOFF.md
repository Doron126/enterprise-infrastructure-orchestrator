# ChatGPT conversation handoff

Use [A03 — Evidence & Decision Handoff](../toolkit/EVIDENCE_DECISION_HANDOFF.md) when moving a project from one ChatGPT conversation to another would benefit from a compact, reviewable record. This is optional; a sufficient existing ticket or document may already provide the needed context.

1. In the old conversation, make A03 available by opening or attaching it, then run Prompt A. Review and sanitize the resulting handoff, and supply or correct any important missing information.
2. In the new conversation, paste the handoff or attach it as a Markdown file, provide any needed permitted evidence or artifacts, and run Prompt B. Review its understanding before relying on consequential conclusions or actions.

A handoff does **not** automatically transfer the entire original conversation, files not included or reattached, hidden model context, unavailable historical messages, credentials or authenticated sessions, execution permissions, or operational approvals. A03 provides neither persistent memory nor automatic synchronization between conversations. Transfer only necessary, permitted, sanitized material; do not include secrets.

## Prompt A — old conversation

```text
Prepare one self-contained Markdown handoff for a new ChatGPT conversation using A03 — Evidence & Decision Handoff. Read and apply the A03 asset supplied or attached with this request (or, if accessible, toolkit/EVIDENCE_DECISION_HANDOFF.md at https://github.com/Doron126/enterprise-infrastructure-orchestrator). If A03 is unavailable, say so and ask me to provide it; do not claim to have applied it.

Examine all relevant conversation context, files and evidence actually available to you. Extract the latest known project state, preserving the technical details, established user instructions and constraints, findings, decisions, blockers and evidence necessary for continuation. Preserve source locators, capture dates and scopes, and meaningful project, object, artifact, version and commit identities. Distinguish evidence verified for its capture and scope from reported facts, assumptions or inferences, conflicts and unknowns. Do not reconstruct inaccessible history or missing evidence as fact, claim access to the full conversation when it may be truncated or unavailable, or resurrect superseded conclusions. Explicitly identify unavailable conversation context, files and sources and their consequences for the handoff.

Include the A03 sections Established Instructions and Constraints, Completed Work and Acceptance Status, and Continuation Point; mark missing or inapplicable information explicitly. Separate current instructions from superseded ones and assistant suggestions from user-approved requirements. Separate planned from executed, executed from verified, verified from accepted, and accepted from merely recommended work. Identify acceptance authority and evidence where known; historical acceptance is not permission for a new action. Record tests, results, failures, partial work, rejected approaches, pending validation and acceptance where relevant. State where work stopped, the active task, blockers, outstanding decisions, dependencies, required inputs, permissions still needed and the smallest useful next action. If the state or next action is unknown, say so rather than inventing one.

Keep conflicting revisions visible until reconciled. Record explicit owner selection of authority or mark authority unresolved; a newer timestamp alone does not establish authority. Changed evidence reopens only dependent findings and decisions; preserve unaffected findings within their original evidence limits. Keep same-name objects in different customers or projects distinct. A handoff does not authorize infrastructure changes. Include only necessary, permitted, sanitized information and no secrets. Make the record compact for a simple project, and useful for basic orientation without access to this conversation.
```

## Prompt B — new conversation

```text
Read the provided A03 handoff in full. Treat it as transferred project context and evidence, not automatically verified live state. Understand its scope, established instructions and constraints, evidence dates and limitations, completed versus planned work, validation and acceptance status, documented decisions, authority, blockers and unresolved issues. Preserve conflicting revisions until reconciled; only explicit owner selection establishes authority, not a later timestamp. Reopen findings and decisions only where changed evidence affects them, preserving unaffected findings within their original limits. Keep same-name objects in different customers or projects distinct.

Do not treat an assistant suggestion as a user-approved requirement, an unverified statement as a verified result, or historical acceptance as permission for a new action. Avoid unnecessarily repeating completed work. Identify missing attachments, inaccessible sources or other evidence needed for continuation; do not invent missing history or claim access to the prior conversation, files or live systems. A handoff grants no infrastructure change authorization. Use only necessary, permitted, sanitized information and no secrets.

Briefly state your understanding of the current state, important constraints, outstanding blockers and relevant evidence limits. Then resume at the documented continuation point: take the smallest useful authorized action if the required information is available, or identify the specific missing input or approval needed. If the continuation point is unknown, say so and seek the minimum information needed to establish it.
```

## Fictional example

In an old conversation, the engineer and ChatGPT troubleshoot a fictional Cedar build service. The handoff records that the service owner accepted a read-only inventory report for worker `cedar-w1`, based on the supplied report `reports/inventory.md` captured 8 September. A proposal to restart the worker has not been executed or accepted. The established constraint is to keep the live build queue running; the active task is investigating intermittent build delays. The latest available queue log ends before the delays, so current queue evidence is a blocker. The continuation point is to request a sanitized queue log covering the delay window and inspect it read-only; the handoff grants no restart approval.

The engineer pastes that reviewed handoff into a new conversation with Prompt B. The new conversation can orient itself from the record and ask for the missing log without recreating the accepted inventory. It treats the report as historical evidence within its capture scope, not proof of the current worker state.
