# Mark Talk

[中文](README.md) · English

Replying to a manager or an academic supervisor can be difficult when you need to explain a constraint, ask for support, or clarify a vague request. Mark Talk helps you identify what matters and draft a few replies with different tradeoffs. You review the wording and decide what to send.

The current scope is communication with people who guide, evaluate, or make decisions about your work. You can start with a sentence about the situation. A relationship profile or a full chat export is optional.

## A small example

Your manager wants the final project review by five, but a set of financial data is still missing. You ask how to reply.

One approach is to clarify the priority:

> A set of financial data is still missing, and I can't yet confirm that it will arrive by five. Would you prefer a progress update by then, or to review the final document once the data is complete?

Another asks for help coordinating the data:

> The financial data needed for the final review hasn't arrived, which may affect the five o'clock deadline. Could you help coordinate it? I'd also like to confirm what you need to see while the data is outstanding.

These are authored examples, not recorded model outputs. They show how a reply can make a clear request without promising an unconfirmed delivery time. Actual responses vary by model and context.

## Install it and describe the situation

In Qianwen desktop work mode, you can send:

```text
Please install the mark-talk/ skill folder from https://github.com/Theo-bang2025/mark-talk-skill, including its references/ directory. When done, tell me the actual installation location and skill version.
```

A participant installed the earlier version by pasting the GitHub link into Qianwen desktop `5.0.0.268` work mode and letting the app download it. The participant then ran the supplied scenarios. This is evidence for that specific setup; the `0.2.0` revision still needs a repeat test in that client.

Enable the skill, open a new chat, and describe your task:

```text
My supervisor wrote only "the argument needs more support" on my draft. Help me ask which part I should revise first. Give me two short messages.
```

For everyday use, you can name Mark Talk if it does not activate automatically. For an automatic-activation test, keep the test input unchanged. See the [getting started guide](docs/getting-started.en.md) for installation, examples, and troubleshooting. The [official QwenWork documentation](https://help.aliyun.com/zh/qwenwork/skills) also describes GitHub and local-file installation; client interfaces can differ.

## Give it the details that affect the reply

Describe what the other person said, what you want to achieve, and what you can actually do. Missing information need not become a long questionnaire. The skill should ask only when the answer changes the wording or a commitment.

| Need | Example request |
| --- | --- |
| A quick response | "I'm in a hurry. Give me two messages I can send now, without committing to a delivery time." |
| Support | "I want one tester for two weeks. Help me make a clear request." |
| Your own voice | "Shorten the second option. Keep the boundary that I can't deliver tonight." |
| Analysis first | "Help me clarify my objective and the choices I have before drafting." |
| Context for a particular person | "Use the relationship card below, and point out anything uncertain." |

The [worked examples](docs/getting-started.en.md) cover an incomplete request, a quick reply, a change in tone, and a card from creation through withdrawal.

## Keep control of relationship cards

A card is readable text containing roles, objectives, known interactions, and tentative interpretations. You can create one, preview a correction, remove a guess, or stop using it.

This version produces and revises text. To reuse a card, save it yourself and provide it in the next conversation. A revised card does not erase old host conversations, host memory, or other copies. The skill cannot control the host's automatic retention. See the [examples](docs/getting-started.en.md) and [card rules](mark-talk/references/relationship-card.md).

## What has been checked

| Environment | Evidence and limits |
| --- | --- |
| Qianwen desktop work mode | Participant-reported installation and activation on 5.0.0.268 with the earlier skill. Raw answers were reviewed; this is not a client test of 0.2.0. |
| Codex CLI | The first version had explicit-load and project-installation trials. Use the current [official skill documentation](https://learn.chatgpt.com/docs/build-skills) and [installation guide](docs/getting-started.en.md) for local placement. |
| QwenWork | Official documentation supports GitHub and local skill installation. Its interface should not be assumed identical to Qianwen desktop work mode. |
| Doubao, Yuanbao, and mobile clients | Direct installation and use have not been verified for this project. |

A skill guides the host model; it does not make every reply correct. Check the facts before sending, particularly deadlines, work already done, and concessions you have not accepted. Provide relevant excerpts and remove unrelated personal or confidential information.

## Help evaluate it

The [evaluation guide](tests/README.en.md) gives the procedure and a prompt for an AI coach. Both conditions receive the same input in separate conversations. Coaching instructions, scoring criteria, and earlier results stay outside the target model's context.

We retain the [historical trials](tests/evaluation.md) and a [review of the first Qianwen run](tests/reports/2026-10-19-qwen-review.md), both in Chinese. That review found unconfirmed commitments missed by the original high scores, so those scores are not presented as general evidence of effectiveness. Reports of failures, no benefit, and regressions are useful. Private conversations need only be summarized anonymously; outputs from the fictional cases may be shared voluntarily.

We will use further feedback to decide how local cards should be stored, edited, and exported before adding platform adapters or persistent memory. The [design](docs/superpowers/specs/2026-10-05-mark-talk-skill-design.md) and [changelog](CHANGELOG.md) document that path.

Released under the [MIT license](LICENSE). The installable folder is [mark-talk/](mark-talk/SKILL.md), following the [Agent Skills specification](https://agentskills.io/specification). Model instructions are in English to avoid an encoding problem observed in an earlier terminal setup; replies follow the user's language. The controlled scenario set is in Chinese and does not establish performance in English.
