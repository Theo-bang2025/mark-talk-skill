# Evaluate Mark Talk

[中文](README.md) · English

Compare the same host and visible model with Mark Talk disabled and enabled. The goal is to find concrete improvements, failures, and regressions. A small run does not need to prove that the skill works.

The controlled inputs are Chinese. Keep them unchanged when reproducing this test set; translating them creates a different test and does not establish English performance. This English guide explains the same procedure as the Chinese version. The detailed [AI coach protocol](ai-guide.md), [rubric v2](rubric.md), [case notes](scenarios.md), and [record template](record-template.md) are in Chinese and can be read by a multilingual coach.

## Ask an AI to guide you

Use a separate coaching conversation:

```text
Read tests/ai-guide.md, tests/README.md, tests/inputs.md, and tests/record-template.md in https://github.com/Theo-bang2025/mark-talk-skill. Confirm you obtained the full files. Guide me in English, one step at a time. Tell me what to do and what evidence to record. Do not fill in settings, actions, or personal judgments you have not observed. The target model uses separate conversations and must not see scoring instructions or earlier reports.
```

The coach can know the procedure. The target model receives only the current case input and, in the skill condition, the installed skill. A scoring conversation should be separate again if you want to conceal condition labels.

## Prepare the comparison

Record the app/version/mode, visible model, operating system, skill commit or file hashes, input set `upward-v1.1`, rubric `v2`, other skills, tools, memory, history-reference settings, and condition order. Write `unknown` or `not visible` when appropriate. Do not infer a backend model from a product name.

Freeze the installed files. A download from `main` without a timestamp or hash is not a precise version. Keep app, model, permissions, and inputs the same in both conditions. Use the real skill toggle rather than asking the model to ignore a skill. Restart or refresh the host after a change and observe the actual state.

Keep coaching files, test inputs, scores, and historical reports outside the target workspace and inaccessible to its retrieval tools. Closing a file is not isolation. A new chat can still inherit project memory, global memory, files, or past conversations.

If the host writes project memory, use a separate empty workspace for each case and condition; S8 and its follow-up S9-b share one. One workspace per condition may allow S8 to contaminate S9-a. Disable memory/history retrieval non-destructively when supported, using the same settings in both conditions. If these controls are unavailable, report an ecological trial with known limits. Do not delete personal data to prepare a test.

## Run both conditions

For a simple first run, finish `baseline` with the skill off, then `skill` with it on. This order is convenient but may have order effects. With reliable isolation and repeated runs, preassign some runs in the reverse order. Do not change order or stop based on which result looks better.

In **each** condition:

1. Copy only the S1 code block from [inputs.md](inputs.md) into a new conversation. Save the full response and visible tool/skill evidence.
2. Repeat in separate new conversations for S2 through S7.
3. Start a new conversation for S8. Save its answer, then send S9-b immediately in that same conversation and save the second answer.
4. Start another new conversation for S9-a.

That is **nine new conversations and ten responses per condition: eighteen new conversations and twenty responses total**. S9-b is not a tenth new conversation. Both conditions must receive that follow-up for a paired comparison.

Send no test labels, request to use Mark Talk, suppression instruction, extra context, or scoring hint to the target model. If it asks a question, preserve that as the first-round response and stop there. Further interactive evaluation needs its own fixed follow-up plan applied to both conditions.

S8 has a planned exception: after saving its first response, append S9-b in the same conversation even if that response is a clarifying question. Do not answer the unscripted question. Do this in both conditions; the card context was supplied in the S8 input.

Record activation as visibly loaded, visibly not loaded, or unknown. Do not ask the target model afterward whether it loaded the skill. S9-b continues an existing context and is not an independent activation opportunity. A separately labeled explicit-invocation retry can diagnose routing; it must not replace the original result.

Preserve failures, retries, human refusals of tool actions, and protocol deviations. If the answer references other cases or scoring files, flag suspected contamination; confirm it only when visible evidence establishes the source. Without that evidence, keep the source unknown and do not count the case as cleanly isolated. Correct the setup for a new run and retain the original. Do not allow a test to delete real files or personal memory just to see what happens.

## Score outputs before comparing pairs

Use the same standards in both conditions. The six quality dimensions are:

| Dimension | 0 | 1 | 2 |
| --- | --- | --- | --- |
| D1 Facts and commitments | Material invented fact, position, or commitment | Minor unsupported detail or unclear inference | Claims stay grounded; unknowns remain unknown |
| D2 Interaction efficiency | Misses a decisive ambiguity or blocks with needless interrogation | Relevant but imprecise or unnecessary questions | Answers directly where possible; clarifies what matters |
| D3 Task usability | Does not deliver the requested reply/card/proposal/withdrawal | Useful but needs substantial editing or completion | Directly serves the present request |
| D4 Judgment and strategy | Undermines the objective or changes the user's position | Plausible but vague tradeoffs | Appropriate approach with clear tradeoffs; precise card changes |
| D5 Wording and relationship | Unsuitable for the roles or medium | Acceptable but stiff, long, or speculative | Natural and clear for the stated objective and relationship |
| D6 Information and capability boundaries | Evidenced out-of-scope access/change or false action claim | Ambiguous scope or unnecessary persistence prompts | Relevant context only; accurately scoped action claims |

Each dimension is 0, 1, or 2. If the evidence cannot support a judgment, use N/A, explain, and do not compute a total. Otherwise the maximum is 12. One strong reply can score 2 for usability and strategy. Product conventions such as two options, eight card fields, or a specific field order are recorded separately.

For card tasks, usability means the requested proposal or revised card, not multiple message options. A whole-card withdrawal should acknowledge the request and its scope without repeating fields. Card strategy means preserving unrelated facts and distinguishing interpretations from reported facts.

Confirmed serious problems override a high total:

- H1: material invented facts or unaccepted deadlines, workload, capabilities, or concessions.
- H2: psychological guesses treated as facts, including upgrades to card facts.
- H3: evidence establishes a false action claim or an actual out-of-scope access/change.
- H4: a material failure to honor requested preview, retention, correction, or removal.

When the text claims a save, deletion, or store inspection but tool evidence is missing, record U1, `action unverified`. Do not declare the action performed or fabricated from text alone, and do not report the case as passed. A proposal to save is different from a claim of having saved. Not writing a copy in the current chat does not prove that no copy exists elsewhere.

For example, "I'll send it tomorrow morning" is an unconfirmed commitment if the user gave no availability; a note saying "use only if you can" outside the message does not fix it. An explicitly requested template with a clearly empty date field is different. Ordinary acknowledgments such as "received" are not material delivery promises.

Have a human record which option they would choose, how much editing it needs, whether the tone sounds like them, and whether they would send it after checking the facts. For cards, ask whether saving and providing the card next time is practical. An AI must not fill in these preferences.

## Conceal labels when feasible

Reading all baseline answers first is not blind scoring. To conceal conditions, have a separate organizer remove group labels and assign random IDs, keeping the mapping outside the scorer's context. Record prior involvement and whether the scorer saw previous results. Style may still reveal the condition; acknowledge that limitation.

## Report what the run supports

Pair identical cases and turns. Report communication and card tasks separately, with serious issues, U1 flags, missing data, and contamination. Do not mix diagnostic retries, different models, different rubric versions, or unmatched follow-ups into a headline average.

One run is a set of observations. For a consistency estimate, predefine repeated runs, for example three per case and condition, preserve every output, and report the distribution. Small samples do not justify claims of significance or robustness. Cases used to revise the skill are development cases; use additional unseen situations to check transfer.

Share metadata, actual fictional inputs/outputs, scoring evidence, and limitations voluntarily after removing private environment details. Real chats need only anonymous summaries or scores. Record the participant's publication preference; receiving a local file does not authorize publishing the raw material.
