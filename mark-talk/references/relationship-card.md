# Relationship cards: user-controlled context

A relationship card is plain text saved and supplied by the user. It keeps objectives and known context for different people separate. The skill can use only a card supplied in the current conversation. It has no independent permission to read, write, or erase memory across conversations. Render the card in the user's language; use natural Chinese field labels for Chinese users.

## Complete card schema

Keep these eight fields, in this order, when creating or fully returning a card:

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

For a Chinese user, translate the labels naturally. For an unknown value write the equivalent of "not provided"; for an empty facts or interpretations field write the equivalent of "none". Do not fill a field by inferring a personality, preference, or role from a short message. A user-confirmed fact is something the user explicitly reports or confirms, not something independently verified by the skill. Keep each interpretation tied to a specific reported interaction. Do not retain irrelevant sensitive details.

## Create and view

When asked to create a card, use the facts already supplied. Ask at most one question if its answer is essential for future use; otherwise leave unknown fields unfilled. When asked to create or view, show the complete card. Do not add reply options unless the user also asks for a message to send. Do not turn every ordinary conversation into an automatic card update.

## Correct, update, or remove a card entry

1. Identify the exact old field and content, the user's requested change, and the user-provided evidence. An explicit correction from the user takes priority over an old card or model inference.
2. Show a short change summary: old content -> proposed replacement or removal. Cite the user's new statement as the reason. If new evidence only invalidates a guess, do not infer the opposite personality trait or feeling.
3. Return the **complete updated card**, preserving every field and every item the user did not ask to change. If the last tentative interpretation is removed, keep that field and mark it "none" instead of silently omitting it.
4. Say the new card is for the user to review and save. Only replacing the user's saved copy makes it available for a future conversation. If the user says "show me first," mark it as a proposal awaiting their confirmation. If the user has already asked to delete a particular entry, present the updated card without another approval step.
5. For a deletion, say "This updated card omits the entry" rather than "I deleted it" as if stored data was erased. End the response with an explicit sentence in the user's language: the new card does not erase old host conversations, host memory, attachments, or separately saved copies. The deletion response is incomplete without this sentence.

If a new statement conflicts with an old user-confirmed fact, show the conflict and ask which statement to retain. Do not silently overwrite it. Use a date explicitly available from the host for "last updated"; if none is available, write the equivalent of "not recorded".

## Delete the whole card

When the user asks to discard a whole card, stop relying on it in the current conversation and do not repeat its contents. Explain that the skill has no independent card storage and cannot delete a copy saved by the user or the host product's old messages and memory. The user must remove those from their respective locations. Future conversations may still receive old information from the user or host settings; do not promise to remember this deletion across sessions. Ordinary communication help remains available without a card.
