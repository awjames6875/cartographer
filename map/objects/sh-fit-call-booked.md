# SH - Fit Call Booked

**Type:**   workflow
**Mark:**   VERIFY — not confirmed · settles by: the workflow list in the account · **Checked:** not yet (drawn August 18, 2026)
**Where:**  Automation → Workflows → "SH - Fit Call Booked"
**Source:** the workflow of that name, opened from the account. Cited, not copied — open the real thing and read it there (`rules.md` §4).

Came here from Lane C of `catalog.md`. Read this card, then open the account. Do not open a second card (`rules.md` §5).

---

**The mark is not yet earned**

- **LIVE** would need: found in the workflow list · showing as published · at least one way in that can still fire.
- **LEFTOVER** would need: found in the list, and no way in survives.

Nobody has opened the list. Until somebody does, this card makes no claim either way.

---

**Hits**

Nothing below is a claim about what moves. Each line is the question that has to be answered, standing where its answer will go.

- `VERIFY — what fires this workflow · settles by: the trigger step at the top of the workflow`
- `VERIFY — whether it fires from the booking itself or from a tag being applied · settles by: the trigger step in the account`
- `VERIFY — which tag it applies, and whether that tag is the one named Fit Call Booked · settles by: the workflow in the account`
- `VERIFY — whether it stops SH - Fit Call Nurture (Alt Days) for that contact · settles by: both workflows in the account`
- `VERIFY — what it sends, and how far ahead of the call · settles by: the steps in the workflow`

The fourth line is the one that connects this card to Lane B. If this workflow is what stops the nurture, then it and the nurture both touch the same contact, and per `rules.md` §3 that belongs in **Hits** on both cards rather than in either card's **Does not hit**.

---

**Does not hit**

- **The tag named `Fit Call Booked`.** Same words, different kind of object, different screen: this workflow lives under Automation → Workflows, that tag under Settings → Tags. Somebody saying "the Fit Call Booked thing" could mean either one, and they are changed in two different places. A workflow and a tag can carry identical names without either one being a copy of the other.

- **SH - Fit Call No Show** — shares the first 14 characters with this one: `SH - Fit Call `. Both are named for something that happens after a booking exists, which is the resemblance that matters: the difference between them is whether the person turned up, and that word sits late in both names.
