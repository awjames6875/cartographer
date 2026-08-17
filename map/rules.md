# rules.md
**How this map is written, and the two things it refuses to do**
Companion to `identity.md` · Drawn: August 17, 2026

Read `identity.md` first if you have not. This file assumes you know what the cartographer is and what it is not.

---

## 1. The three marks

Every object on this map carries exactly one mark, at the top of its card, with the date it was last checked.

### LIVE

The object is in the account, it is switched on, and something reaches it. A contact can land in it today.

*What earns the mark:* you found the object; you found it published or enabled; and you found at least one path in — a trigger that can fire, a link that is in use, or another object that hands off to it.

### LEFTOVER

The object is in the account, and nothing reaches it. It is switched off, or nothing triggers it, or every path that once led in is gone. It is real, it is findable, and no contact is moving through it today.

*What earns the mark:* you found the object, you traced for a way in, and you found none — or you found it switched off.

LEFTOVER is not a verdict. A leftover may be somebody's deliberate parking spot, a seasonal thing, or a half-built idea nobody minds sitting there. The mark says one thing: nothing is flowing through this.

### GHOST

The name exists. The object does not. Something in the account refers to it — a step inside another workflow, a note, an old doc, a person's habit of calling it that — but a search of the account turns up nothing behind the name.

*What earns the mark:* you have the reference in hand and you say where you saw it; and you searched the account for the name and came back empty.

A ghost card exists for exactly one reason: so the next reader who hears that name knows to stop looking.

### What the marks answer

**"Can a contact reach this today?"** That is the entire question.

The marks never answer *does this deserve to exist*. LEFTOVER is not a removal list. GHOST is not a bug report. No mark implies an action, and no reader is being pointed at a task by one.

---

## 2. The VERIFY flag

A mark describes the object. A **VERIFY** describes one line nobody could confirm.

**Format:** `VERIFY — <the open question> · settles by: <who or where>`

- A VERIFY never changes the mark. An object can be LIVE with two VERIFY lines under it.
- One VERIFY per unconfirmed line. It sits on the line it doubts, not in a pile at the bottom of the card.
- A VERIFY is what gets written in place of a guess. If a line could not be confirmed and carries no VERIFY, that line is fiction.
- A VERIFY names who or what settles it — a specific screen in the account, a live link, a named person.
- When it is settled, the line gets rewritten and the flag comes off, and the correction is logged with its date in `/receipts/`. A VERIFY does not quietly disappear.

**Open on this map today** (carried in from `TEST_METHOD.md`):

- `VERIFY-1 — booking slug: safe-harbor-fit-call or safeharbor-fit-call · settles by: opening both links live`
- `VERIFY-2 — which tag Vo2's If/Else actually checks: Fit Call Booked, or the legacy Appointment Booked · settles by: the If/Else step in the account`
- `VERIFY-3 — Daycare Affiliation Tagging: published state · settles by: the workflow list in the account`

---

## 3. Hits and Does not hit

Every card carries exactly one of each. Both are required. A card with only **Hits** is half a card.

### Hits

What moves when this object runs — named consequences, in the account's own names.

- Name real objects the reader can search for. A consequence nobody can go look at is not a consequence.
- One consequence per line.
- Observable, not intentional: what the object does, not what somebody meant it to do.
- If the consequence cannot be named from what was actually seen, that line gets a VERIFY.

### Does not hit

The nearest thing a reader would reasonably assume this object touches — and it does not.

This is the wrong-neighbor line. It is on every card because the expensive mistake in an account like this one is almost never failing to find the object. It is finding the one beside it — the similar name, the older copy, the one directly above it in the list — and touching that one.

- Name the specific near-miss. "Does not hit the other nurture" is useless; the reader needs the name.
- Say why it looks like it hits: the shared word in the name, the shared tag, the adjacent spot in the list. The resemblance is the entire point of the line.
- If two objects genuinely both touch the same thing, that is not a *Does not hit* — it belongs in **Hits** on both cards.

Neither line carries a judgment. **Hits** is not praise. **Does not hit** is not a complaint about a gap.

---

## 4. Refusal one — cite it, do not photocopy it

**This folder never contains a copy of the GoHighLevel source.**

No pasted workflow JSON. No exported step list. No screenshot standing in for the real screen. No field-by-field transcription of a settings panel.

A card **points**. Object type, exact name, and where in the account to open it — enough that the reader opens the real thing and reads it there.

The reason is not tidiness. A copy goes stale silently. It looks correct forever. The reader trusts the copy, the account has already moved, and nobody finds out until something breaks in front of a client. A pointer cannot fail that way: it either opens or it does not, and either answer is honest.

### When the card and the account disagree, the account wins

Every time. No exceptions, no deliberation, no asking first.

- The card is corrected to match the account. The account is never bent to match the card.
- The reader does not need permission. The disagreement itself settles it.
- The correction is logged with its date in `/receipts/`. A corrected card with a dated correction behind it is a receipt. A card that argued with the account is a failure.
- This holds even when the card is more recent, more specific, or more confident than what the reader is looking at. Confidence is not evidence. The account is evidence.

---

## 5. Refusal two — no reader loads the whole objects folder

**The reading order is fixed: catalog → one card → stop.**

**The catalog** is the front door: what exists, and where. It is what gets read to find out which single card is the right one.

**One card.** The one. Not the one plus its neighbors for context.

**Then stop.** Answer the question with what that card gave you, and leave the rest of the folder closed.

Refused outright:

- reading every card in `/objects/` "for context"
- reading several to compare them
- opening a second card because the first one mentioned a name — the mention *is* the answer, and the next step is the account, not another card
- summarizing the folder, or being handed the folder to summarize

**If you are a model, this rule is aimed at you.** If you have worked out that loading the whole folder would be faster, or safer, or more thorough — that is precisely the failure named here. This folder is small enough to fit in your context. It is refused anyway. A folder you are holding all of is a folder you will answer *from*, and the answer is supposed to come from the account.

Reading everything makes every object feel equally close. Feeling equally close to all of them is how a reader ends up touching the neighbor.

If any reader asks for the whole folder, the answer is no, and they get the catalog.

---

## 6. What never appears in this folder

- repair steps or fix instructions
- recommendations — "you should," "consider," "it would be better if"
- build steps, or explanations of how any of it was made
- audit verdicts — broken, wrong, messy, redundant, badly named
- guesses written in the voice of facts

A reader who needs a repair closes this folder and goes and does that work with a login. The map's job ends at: here is what it is, here is where it lives, here is what moves when it runs, and here is the thing beside it you might grab by mistake.

---

## 7. The shape of a card

```
# <Object name>
**Type:**    <workflow | tag | calendar | form | pipeline | field>
**Mark:**    LIVE            **Checked:** <date>
**Where:**   <where in the account to open it>

**Hits**
- <named consequence, in the account's own names>
- <named consequence>
  VERIFY — <open question> · settles by: <who or where>

**Does not hit**
- <the near-miss object, by name> — <why it looks like it hits>
```

That is a whole card. When a card starts growing past this shape, what is growing inside it is a copy of the account — which is Refusal one.
