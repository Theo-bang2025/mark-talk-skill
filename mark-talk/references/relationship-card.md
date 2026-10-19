# Relationship cards: text the user controls

A card is a compact piece of context the user can inspect, edit, save, and supply in another conversation. Creating card text does not create a host memory entry. Saving a copy alone does not make it available in a future chat: the user must provide it there. Use the user's language for the card and explanations.

## The complete card

Return these eight fields when creating, viewing, or revising a card:

```text
Target alias and role:
My role:
Long-term objective:
Preferred communication style:
User-confirmed interaction facts:
Tentative interpretations, each with its evidence:
Current open matter:
Last updated:
```

Translate the labels naturally. Write "not provided" for unknown information and "none" for an empty facts or interpretations field. Keep the field when its last entry is removed. Use an explicitly available host date for the update; otherwise write "not recorded". User-confirmed means reported or confirmed by the user, not independently verified.

Do not infer a personality, preference, or feeling from one short message. Keep each tentative interpretation tied to the reported interaction that supports it. A new fact invalidating a guess does not establish the opposite guess.

## Create, view, or revise

For creation, use what is supplied and leave gaps visible. Ask at most one essential question. Return a card, not several competing cards or reply options, unless the user asks for both tasks.

For revision, show a short summary of the old entry, replacement or removal, and the user's basis for it. Return the complete new card, preserving unrelated content. If the user says "show me first," mark the result as a proposal; do not describe it as adopted or stored. If they already requested a specific removal, provide the revised text directly.

An explicit correction takes priority over an old model inference. If two user-confirmed facts genuinely conflict, identify the conflict and ask which to retain. Do not remove a separate fact, such as weekly discussion, merely because a new fact specifies when progress should be sent.

Say the card is ready for the user to review, save, and provide next time. Do not write host memory frontmatter, indexes, or a persistence plan during a text-card request.

## Remove an entry

Return the complete card with that entry omitted. State that the revised text omits it, rather than implying stored data was erased. Include a short, explicit sentence that this revision does not erase host history, host memory, attachments, or separately saved copies.

## Discard the whole card

Stop using it in the current conversation and do not repeat its contents. If it is not in the supplied context, acknowledge the request without reconstructing it or searching for it. Explain the scope once: this text operation does not delete stored files or host history and cannot ensure what information a future chat receives.

Do not search files, claim a memory-store inspection, or infer the absence of other copies. The user may separately ask to manage a particular saved copy through available host tools; follow that distinct request and report only verified results. Ordinary communication help can continue using the facts the user supplies now.
