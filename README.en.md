# Mark Talk

[中文](README.md) · English

Messages to a manager, mentor or academic supervisor often need more than politeness: they need a clear account of your work, judgment and request. Mark Talk helps identify the current task, ask a few useful questions when necessary and draft a small number of distinct approaches. Add context, choose one and refine it into something you would say. You check and send the message.

The scope is upward workplace and academic communication: progress, help, resources, standards, constraints, criticism and confirmation. Start with one sentence; a relationship profile or full chat history is optional.

**This tree contains the `0.3.0` candidate, revised 2026-10-30, without a formal release.** The closed campaign retains 40 valid Codex responses and 42 deduplicated Qianwen responses. One participant completed ten paired evaluations: candidate preferred in three, old in five, with two ties. See the [human feedback and refinement report](tests/reports/2026-10-29-0.3.0-human-feedback-and-refinement.md). Repairs target visible responsibility, natural constraints, final-message convergence and persistence authorization. Historical failures and limitations remain in the [campaign summary](tests/reports/2026-10-26-0.3.0-evaluation-summary.md); formal acceptance is incomplete. The stable version remains available at the [fixed 0.2.0 commit](https://github.com/Theo-bang2025/mark-talk-skill/tree/82dd114484f0a92068c6096c4843a68202083807/mark-talk).

## Add facts, choose, then refine

This is a hand-written illustration, not a measured model output.

> **You:** I'd like one tester for two weeks, but I'm worried the department head will think I haven't planned properly.
>
> **Assistant:** What checks have you already completed, and what testing needs those two weeks? Those details make the basis and purpose concrete.
>
> **You:** We tested the core flow ourselves, but not cross-department account permissions. Launch is planned next month. My part-time colleague and I have no capacity for permissions and regression testing.
>
> **One of the assistant's approaches:** I'd like to request one tester for two weeks for cross-department permissions and regression testing. We've tested the core flow, but my part-time colleague and I have no capacity for this part. With launch planned next month, could you help arrange that support?
>
> **You:** Use this one. Shorter, like a chat message.
>
> **Assistant:** Could we get one tester for two weeks for permissions and regression testing? We've tested the core flow, but my part-time colleague and I can't cover this part. Could you help arrange someone?

Methods guide the thinking. Messages follow the relationship, medium and your habits, with elements omitted, combined or reordered as needed. There is no required four-part script or repeated opening, and no random synonym swapping to simulate naturalness. Revisions preserve facts, constraints, position and commitments.

## Install and try it

For the candidate, import the complete `mark-talk/` from this source tree or the local candidate ZIP into a client that supports local skills:

```text
mark-talk/
  SKILL.md
  references/upward-methods.md
  references/relationship-card.md
```

You can ask an installation assistant:

```text
Install the local mark-talk/ folder I provide, keeping both reference files. Check that SKILL.md says version 0.3.0 and revision 2026-10-30, and report the actual installation location and SHA-256 of all three files. State anything you cannot verify.
```

Check the revision date and hashes even when two packages both say 0.3.0. The old campaign froze source d4b5032; it is distinct from this revision. For GitHub installation, verify the actual branch and commit contain the intended revision. For 0.2.0 use the fixed commit above; it has no methods file. See the [getting-started guide](docs/getting-started.en.md) for paths and troubleshooting. The [official QwenWork guide](https://help.aliyun.com/zh/qwenwork/skills) describes GitHub and local installation; actual client interfaces and support need separate verification.

Enable it, open a new conversation and describe your task. If necessary in everyday use, name Mark Talk explicitly; automatic-activation tests retain the original input. You can say “give me one message now” or “use option two, firmer, without promising delivery tomorrow.” The [worked tutorial](docs/getting-started.en.md#work-through-a-reply) shows the complete interaction.

## Optional cards you control

A text card contains roles, goals, reported facts, tentative interpretations with evidence and the open matter. Preview, correct, remove an entry or withdraw the whole card. Save it yourself and provide it again in another conversation.

Withdrawal excludes old fields and matters from subsequent advice; facts you supply anew can be used. Editing card text does not erase host history, memory, attachments or other copies. Managing a specific stored copy is a separate task using actual host capabilities. See the [card examples](docs/getting-started.en.md#use-a-relationship-card).

## Evidence and limits

| Environment | What the evidence supports |
| --- | --- |
| Qianwen desktop work mode | Cross-build ecological trial on 5.0.5/5.0.7: 36 valid main-track responses, four complete version pairs, plus six separate pilot responses. Candidate T1 had no visible skill call; unsupported facts/commitments and unrequested writes remain |
| Codex | CLI 0.163.0-alpha.11 completed 29 contexts/40 responses and six version pairs with raw rule-loading evidence, under read-only permissions. Candidate T4 still added an unaccepted work commitment; a three-call overlap is disclosed |
| QwenWork | Official installation instructions exist; these do not establish identical interfaces or candidate loading in every Qianwen product |
| Doubao, Yuanbao, mobile | Direct import and use remain unverified |

Results depend on the host/model. The skill drafts messages, not predictions of approval or promotion. Share relevant excerpts without unnecessary sensitive details. The [methods and source limitations](mark-talk/references/upward-methods.md) are bundled; runtime use needs no network, key or database.

The [evaluation guide](tests/README.en.md) specifies old/candidate comparison: 29 conversations, 40 responses, distributable across runs, plus ten human task evaluations from five volunteers. Coaches and targets are separate. Developer behavior, host loading and human preference remain distinct evidence. Anonymous failures, rewrites and reproducible platform notes are welcome; raw personal chats need not be uploaded and received raw files are not automatically published.

See [round-two review](tests/reports/2026-10-21-qwen-round2-review.md), [roadmap](ROADMAP.md), [changelog](CHANGELOG.md) and [version recovery notes](docs/version-history.md). The scope remains upward communication; controlled records come later when observed usage warrants them.

[MIT](LICENSE) · [Skill](mark-talk/SKILL.md) · [Agent Skills specification](https://agentskills.io/specification). Model instructions are ASCII English; responses follow the user's language.
