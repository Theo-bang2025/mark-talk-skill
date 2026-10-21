# Getting started with Mark Talk

[中文](getting-started.md) · English · [Project home](../README.en.md)

Install the skill, then try a small communication problem. You do not need to build profiles first or upload an entire chat history. The conversations below are authored demonstrations, not recorded test results or promises about how a recipient will respond.

## Install and check

### Qianwen desktop work mode

This tree is the 0.3.0 candidate. Candidate installation has not been accepted in Qianwen. Participants reported old GitHub installation and 0.2.0 local import on 5.0.0.268; those records do not verify this candidate.

For candidate use, take the complete `mark-talk/` from the actual source or local candidate ZIP. In a client supporting local import, ask:

```text
Install the local mark-talk/ folder I provide, keeping references/upward-methods.md and references/relationship-card.md. Verify SKILL.md says 0.3.0, and report the actual location and all three SHA-256 hashes. State anything you cannot observe.
```

Do not substitute GitHub main for a candidate that has not been synchronized. For public 0.2.0 use the [fixed commit folder](https://github.com/Theo-bang2025/mark-talk-skill/tree/82dd114484f0a92068c6096c4843a68202083807/mark-talk); it has no bundled methods file.

1. Import through your client's actual local-skill interface; enable only the intended Mark Talk version.
2. Check folder nesting and all three files. Root README/tests are not skill instructions. Hashes identify an iteration more precisely than the version string.
3. Refresh/reopen and inspect the skill list, then open a new work-mode conversation.
4. Look for visible core/reference invocation evidence. Two replies do not prove loading. Naming Mark Talk is useful in everyday use; automatic-activation evaluation uses unchanged inputs.

The [official QwenWork guide](https://help.aliyun.com/zh/qwenwork/skills), checked on 2026-10-21, describes GitHub/local installation and `~/.qwenworkcn/skills/`. Interfaces differ across products. If the actual client cannot import, record the limitation rather than claim success.

### Codex

The [current official documentation](https://learn.chatgpt.com/docs/build-skills) lists `~/.agents/skills/` for user skills and `.agents/skills/` for repository skills. Place the complete folder there:

```text
~/.agents/skills/mark-talk/SKILL.md
~/.agents/skills/mark-talk/references/relationship-card.md
~/.agents/skills/mark-talk/references/upward-methods.md
```

Open a new conversation and ask to use `$mark-talk`. Earlier project trials used a `.codex/skills` directory; that is a historical setup, not a recommendation to use the old path in every client.

## Work through a reply

### Start with incomplete context

You can begin with:

> I need to tell my supervisor I'm behind on the draft. How do I say it?

The assistant may ask:

> When did your supervisor ask for it, and what is holding it up? Those details determine whether to explain the current position or discuss a different arrangement.

You add:

> The draft is due tomorrow, but the experimental data is incomplete. I don't know when it will be ready.

A possible reply is:

> The draft is still missing some experimental data, so I can't yet confirm that a complete version will be ready tomorrow. Would you prefer an update on the current work tomorrow, or to review the complete draft once the data is available?

This asks what the supervisor needs to see. It does not promise that an unfinished partial draft can be delivered tomorrow. Add a delivery commitment only after you have confirmed what you can provide.

### Ask for something you can send now

> My manager wants the entire report redone tonight. I'm away without my computer. Give me two replies I can send now, without a long round of questions.

**Explain the constraint and ask about the need:**

> I'm away without my computer, so I can't redo the whole report tonight. When will this version be used, and which parts most need changing?

**State the boundary and clarify the next decision:**

> I need to be clear that I can't redo the whole report tonight without my computer. Would it help to clarify the changes needed first, or should we discuss the delivery arrangement for the complete version?

The first asks about the underlying deadline. The second makes the boundary more explicit. Neither assumes you can start tomorrow, take a call now, or deliver on Monday.

### Add facts, choose, then refine

> **You:** I'm leading an internal tool planned for next month. It's just me and a part-time colleague. I'd like one tester for two weeks; help me explain the need.
>
> **Assistant:** What have you already checked, and what should the tester cover? Those facts make your preparation and the gap concrete.
>
> **You:** We've tested the core flow ourselves. Cross-department permissions are untested, and neither of us has capacity for permissions and regression testing.
>
> **One approach:** I'd like one tester for two weeks for cross-department permissions and regression testing. We've tested the core flow, but my part-time colleague and I cannot cover this part. With launch planned next month, could you help arrange the support?
>
> **You:** Use that version. Shorter, like a chat. Don't give me two more options.
>
> **Assistant:** Could we get one tester for two weeks for permissions and regression testing? We've tested the core flow, but my part-time colleague and I can't cover this part. Could you help arrange someone?

The added basis comes from your actual work and gap, not invented test counts, positive feedback, risk probabilities, start dates or concessions. After selection the assistant revises one draft. You may also ask for a short initial request without following this exact question sequence.

### Change the voice while keeping the position

> Make it firmer. Keep one tester for two weeks. Don't offer part-time support or choose a start date for me.

For example:

> I need to request one tester for two weeks for permissions and regression testing. We've tested the core flow, but neither of us has capacity to cover this part. Could you arrange the support?

Firmer wording does not mean refusing the whole assignment; softer wording does not authorize a concession. Methods guide internal thinking rather than impose four sections or a repeated opening. Email, familiar chat and your own wording can be organized differently. Random synonym swaps do not make a message natural, and polishing must preserve facts, constraints, position and commitments.

## Use a relationship card

### Create it

> Make a card for Dr Zhou, my academic supervisor. I'm a graduate student, I want to keep the thesis moving, and I prefer concise messages. We discuss the thesis weekly; my current task is revising the first draft. Leave anything else unknown.

```text
Target alias and role: Dr Zhou, academic supervisor
My role: graduate student
Long-term objective: keep the thesis moving
Preferred communication style: concise
User-confirmed interaction facts: weekly thesis discussion
Tentative interpretations, each with its evidence: none
Current open matter: first-draft revision
Last updated: not recorded
```

The example supplies no date. An actual host date can be used when available. Your preferred style is not proof of the supervisor's preference.

### Save and reuse it

Copy the card into your own notes. In a new conversation, paste or upload it and add the current message:

> Here's the card I saved. Today my supervisor said, "Clarify the research question first." Help me ask what to tackle next.

Saving a file on your computer does not make every AI conversation read it automatically.

### Correct it before saving

> My supervisor said today that a progress update each Friday is enough. Add that fact, but show me the proposed change first.

The assistant should show the change, its basis, and a complete proposed card. Review it before replacing your notes. A weekly discussion and a Friday update may be separate arrangements, so one should not silently replace the other.

### Remove a guess or withdraw the whole card

If a different full card you provide contains the evening-update guess, you can request:

> Remove the guess that my supervisor likes evening updates. Keep the other entries and give me the complete revised card.

The revised card should retain the other fields and mark an empty interpretations field as `none`. Revising that text does not erase host history or other copies.

To withdraw an entire card, say:

> Stop using this entire card in this conversation, and don't repeat its contents.

The assistant should stop using it in the current conversation without restating the fields or offering a new task based on an old open matter. Facts you supply anew can be used without restoring the old card. A future chat may still receive old information from you or the host. Managing a particular saved file or a host memory entry is a separate operation with its own actual tools and verifiable result.

## Troubleshooting

| What you see | What to check |
| --- | --- |
| No skill in the list | Installation support, folder nesting, and all three candidate files. Do not assume an unsupported client can import it. |
| An ordinary chat response | Look for invocation evidence. For everyday use, name Mark Talk; evaluate automatic activation separately. |
| Generic requests or updates | Check that the methods file was imported/read; supply actual work or the concrete gap. No full book is needed. |
| Incomplete card updates | Check that the reference file was imported, and supply the current full card. |
| A new chat lacks the old context | Provide your saved card again. This version has no separate database. |
| An invented deadline or work status | Do not send it. Identify the sentence and ask for a grounded rewrite; an anonymous report helps the project. |
| Garbled text | Check reading/encoding behavior. Model instructions are ASCII English; user documentation is UTF-8. A financial mistake alone does not establish an encoding cause. |

For a comparison, use the [evaluation guide](../tests/README.en.md) in separate conversations with fixed inputs. Ordinary use can remain interactive.
