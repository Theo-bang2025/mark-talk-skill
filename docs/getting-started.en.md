# Getting started with Mark Talk

[中文](getting-started.md) · English · [Project home](../README.en.md)

Install the skill, then try a small communication problem. You do not need to build profiles first or upload an entire chat history. The conversations below are authored demonstrations, not recorded test results or promises about how a recipient will respond.

## Install and check

### Qianwen desktop work mode

A participant used desktop version `5.0.0.268`: enter work mode, paste the repository link, and ask Qianwen to install it. You can send:

```text
Please install the mark-talk/ skill directory from https://github.com/Theo-bang2025/mark-talk-skill, including references/relationship-card.md. Tell me the actual installation location, skill name, and version in SKILL.md when installation is complete.
```

Then check the following in your client:

1. Find `mark-talk` in the skill list and check that it is enabled. Complete any installation confirmation shown by the client.
2. Check that the installed folder contains `SKILL.md` and `references/relationship-card.md`. The repository's README and tests are not the skill instructions to load.
3. Start a new work-mode conversation. If the skill list has not refreshed, restart the client and try again.
4. Send an example below and look for a visible skill invocation marker. Two reply options alone do not prove that the skill loaded.

For manual installation, [download the repository ZIP](https://github.com/Theo-bang2025/mark-talk-skill/archive/refs/heads/main.zip), extract it, and find `mark-talk/`. If your client accepts local skills, import that entire folder with its reference file. The participant did not separately test this manual route.

The [official QwenWork guide](https://help.aliyun.com/zh/qwenwork/skills) documents GitHub installation and the local `~/.qwenworkcn/skills/` folder. QwenWork and Qianwen desktop work mode may expose different interfaces; follow the client you actually have.

### Codex

The [current official documentation](https://learn.chatgpt.com/docs/build-skills) lists `~/.agents/skills/` for user skills and `.agents/skills/` for repository skills. Place the complete folder there:

```text
~/.agents/skills/mark-talk/SKILL.md
~/.agents/skills/mark-talk/references/relationship-card.md
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

### Make a resource request concrete

> I'm leading an internal tool that should launch next month. There are only two of us, including a part-time colleague. I want one tester for two weeks.

A possible request is:

> I'd like to request one tester for two weeks to help validate the internal tool before launch. We're planning to launch next month, and the project currently has only me and a part-time colleague. Could we arrange that testing support?

You can ask the assistant for another approach that helps the manager make a decision. If you have not accepted a shorter assignment, part-time support, or a later launch, the assistant should not offer those concessions on your behalf. Real testing scope and workload estimates can strengthen the request when available.

### Make it sound like you

After choosing an option, say:

> Make this shorter and less like a formal status report. Keep the request for one person for two weeks and the launch next month.

For example:

> Could we borrow one tester for two weeks? The tool launches next month, and it's currently just me and a part-time colleague. I'd like to get the pre-launch testing covered.

A change in tone should preserve the facts. It should not add a claim that test cases are already prepared. You can also ask for one message, firmer wording, or analysis before drafting.

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

The assistant should stop using it in the current conversation without restating the fields. A future chat may still receive old information from you or the host. Managing a particular saved file or a host memory entry is a separate operation with its own actual tools and verifiable result.

## Troubleshooting

| What you see | What to check |
| --- | --- |
| No skill in the list | Installation support, folder nesting, and both required files. Do not assume an unsupported client can import it. |
| An ordinary chat response | Look for invocation evidence. For everyday use, name Mark Talk; evaluate automatic activation separately. |
| Incomplete card updates | Check that the reference file was imported, and supply the current full card. |
| A new chat lacks the old context | Provide your saved card again. This version has no separate database. |
| An invented deadline or work status | Do not send it. Identify the sentence and ask for a grounded rewrite; an anonymous report helps the project. |
| Garbled text | Check reading/encoding behavior. Model instructions are ASCII English; user documentation is UTF-8. A financial mistake alone does not establish an encoding cause. |

For a comparison, use the [evaluation guide](../tests/README.en.md) in separate conversations with fixed inputs. Ordinary use can remain interactive.
