# Evaluate Mark Talk

[中文](README.md) · English

The default campaign compares **0.2.0 with the 0.3.0 candidate** for task usefulness, selective clarification, iteration and natural wording, alongside facts and user control. This is a plan, not a passed result. Controlled inputs are Chinese; translations create a different test and do not establish English performance.

See the [2026-10-26 final summary](reports/2026-10-26-0.3.0-evaluation-summary.md): 40 valid Codex responses, 36 Qianwen main-track responses and six separately reported Qianwen pilot responses. The user closed the two quota-interrupted Qianwen comparisons for this round. The frozen plan below remains unchanged; closure does not mean acceptance.

One participant has completed all ten pairs. See the [feedback and refinement report](reports/2026-10-29-0.3.0-human-feedback-and-refinement.md) and the separate [targeted replay inputs](refinement-scenarios.md). Development wording tests do not count toward the original host campaign or replace human and Qianwen acceptance.

## Ask an AI coach

Use a separate coaching conversation:

```text
Read this project's tests/ai-guide.md, tests/README.en.md, tests/dialogue-scenarios.md, tests/inputs.md and tests/record-template.md. Confirm full files and actual old/candidate package identities. Guide me in English one step at a time. Targets use separate contexts and see only the current user input, never fact tables, scoring or historical reports. Do not invent settings, tool actions, measurements or human preferences. Report partial completion honestly.
```

For a local candidate, provide its actual documents/package; do not assume GitHub main includes it.

## Fix packages, environment and context

Pin old to `82dd114484f0a92068c6096c4843a68202083807` (`v0.2.0`), candidate to a source commit and all three SHA-256 hashes. A version string alone does not identify an iteration. Install only the corresponding version, refresh/reopen and verify actual files. Candidate adds `references/upward-methods.md`; old has two files.

Record product/version/mode, visible model and backend uncertainty, OS, sampling, tools, permissions, other skills, memory/history and actual isolation scope in the [template](record-template.md). Unknown stays unknown. Keep settings equal. Do not simulate a switch with an instruction to ignore rules. Freeze files during a run; revisions get new IDs while failures remain.

Keep coaching, scoring, all tests/fact tables and prior answers outside target access. A new chat can inherit memory or files. Use verifiably independent scopes per case/condition; S8/S9-b and each three-turn task share only their own context. Disable memory non-destructively where supported; never delete personal data. If isolation is unverifiable, report an ecological trial. Balanced order cannot erase persistent state.

Record automatic injection separately from active retrieval or unknown. Preserve unexpected details as suspected contamination until evidence establishes a source; a diagnostic rerun cannot replace the original.

## Run 29 conversations / 40 responses

Use [dialogue-v1](dialogue-scenarios.md) and unchanged [upward-v1.1](inputs.md):

1. Candidate regression: S1–S7, S8 then same-context S9-b, independent S9-a: **9 / 10**.
2. Candidate risk repeats: S1, S5, S6 and S8 → S9-b twice more each in fresh contexts: **8 / 10**. Each trajectory totals three runs.
3. Transfer: T1–T4 single-turn, T5–T6 three-turn, each version: **12 / 20** combined. Old first for T1/T3/T5, candidate first for T2/T4/T6.

Send only the current payload without labels or explicit skill invocation for automatic activation. Preserve first questions without answering in regression, except always append S9-b after S8 without answering unscripted questions. Follow-ups are not new contexts or independent activation opportunities.

T5 reveals only fact-table rows corresponding to actual questions; no question means the fixed second-turn prompt. Both versions have equal opportunities, not guaranteed equal information. T6 has a fixed correction. Both have fixed third-turn convergence prompts. Never send evaluator tables to targets.

Save actual input, complete first output, context/workspace alias, timestamps, tool/activation evidence and deviations. Core and reference loading are separate visible loaded / not loaded / unknown observations; asking the model afterward proves neither. Do not redraw or select the best output. Optional A1/A2, C1–C3, N1/N2 diagnostics are outside 29/40; storage fixtures use fictional temporary data only. Explicit-load developer replay is separate from target-host acceptance.

## Score and obtain human feedback

Use [rubric v2.1](rubric.md) and [case notes](scenarios.md) in another context. Six dimensions remain facts/commitments, interaction efficiency, usability, strategy, expression/relationship and information/capability boundaries. Cite actual inputs and output. First/final turns are separate; high averages do not offset H1–H4. U1 unsupported action claims do not pass. File names, timestamps or a verification summary alone do not establish active tools.

Separate quality, format conventions and human preferences. Check question value, uptake of revealed facts/corrections, repeated questions and convergence. Naturalness depends on medium, relationship and user's habits, not synonym counts or a four-part script. Relevant questions can advance the same task.

For concealed scoring, a separate organizer removes labels, assigns random IDs and withholds the mapping. Record developer involvement and prior exposure. Reading old outputs first is not blind; style may still reveal conditions.

Invite five volunteers for two fictional/anonymized tasks each: ten evaluations. Humans alone record initial preference, ties/neither, edits, voice, question usefulness and willingness to send after checking facts. Record actual length, elapsed time and time to find the draft; unmeasured stays unrecorded. Gates: at least 8/10 willing to use candidate with no/minor edits after checking, 7/10 finding it more useful than old; ties/neither remain in the denominator. All transfer tasks must work with no confirmed serious errors; three runs per risk trajectory must show no confirmed H1/H4. These are product decisions, not population estimates.

## Report limits and retain failures

Report actual contexts/responses, pairs, serious errors, U1, contamination, missing data and unknown loading. Keep regression, repeats and transfer separate, communication and cards separate. Do not pool unmatched turns or different models/rubrics. Public development tasks are not unseen holdouts. Developer replay, real-host automatic activation and human acceptance are distinct; pending gates remain pending.

Raw materials are private by default. Remove personal/environment traces before voluntary sharing and record publication permission. Real chats may use anonymous summaries; receiving files does not authorize publication.

## Optional historical off/on protocol

For calibration only, upward-v1.1 off/on uses **9 contexts / 10 responses per condition, 18 / 20 total**, including S8 → S9-b in both. It is separate from old/candidate acceptance and not pooled with 29/40. The same isolation, evidence and retention rules apply.
