# SH - Fit Call Attended

**Type:**   workflow **and** tag — two objects, one name · settled: Sadie, August 19, 2026
**Mark:**   LIVE · settled: Sadie, August 19, 2026    **Checked:** August 19, 2026
**Where:**  Automation → Workflows → "SH - Fit Call Attended" · the tag: Settings → Tags → `fit call attended`
**Source:** the workflow of that name, opened from the account. Cited, not copied — open the real thing and read it there (`rules.md` §4).

Came here from Lane E of `catalog.md`. Read this card, then open the account. Do not open a second card (`rules.md` §5).

---

**What earned the mark**

This is the one object on the walked map where all three of `rules.md` §1's conditions came back answered:

- **found in the account** — Automation → Workflows
- **published** — status Published, version 5, created and last updated August 12, 2026
- **a way in that can fire** — an appointment on the Safe Harbor Fit Call calendar set to status "showed"

All three settled: Sadie, August 19, 2026.

---

**The type was an inference. It was half right, and the half it missed is the interesting half.**

This card previously guessed **workflow** from the `SH - ` prefix, and flagged the guess. Sadie found **both** a published workflow and a tag named `fit call attended` (C-4).

It is **not** an appointment status. Those are system-defined — `confirmed`, `showed`, `no-show`, `cancelled` — and "Fit Call Attended" is not among them · settled: Sadie, August 19, 2026.

So the prefix pattern found a real workflow and hid a real tag standing beside it. This is the **third** instance of the same shape on this map, after `SH - Fit Call Booked` / `fit call booked` and the pair in Lane F. A name on this map does not reliably belong to one object.

---

**Hits**

- Fires when an appointment on the **Safe Harbor Fit Call** calendar is set to status **showed** — calendar ID `AuOmiT3Afi2aXSlH7JJQ`, standard events and contacts only · settled: Sadie, August 19, 2026
- Removes the tags `fit call nurture`, `fit call no show`, and `fit call booked` · settled: Sadie, August 19, 2026
- Adds the tag `fit call attended` · settled: Sadie, August 19, 2026
- Removes the contact from **SH - Fit Call Nurture (Alt Days)** · settled: Sadie, August 19, 2026

**A person sets attended, not the calendar** · settled: Sadie, August 19, 2026 (C-5). The platform does not flip an appointment to "showed" when the time passes. Somebody opens the appointment and changes the status by hand. If nobody does, this workflow never fires and a contact who genuinely attended keeps their `fit call booked` tag and stays in the nurture.

**This workflow sends nothing** — no SMS, no email. Every action is a tag or a workflow removal · settled: Sadie, August 19, 2026. Anybody sent here to change "the follow-up after the call" will not find a message in it.

`VERIFY — whether anything sends a post-call message, and where it lives · settles by: the account`
`VERIFY — whether this workflow moves the contact into a pipeline stage · settles by: the steps in the workflow`

**It is the second object that stops the nurture.** `SH - Fit Call Booked` does the same. Per `rules.md` §3 that belongs in **Hits** on all three cards rather than in anybody's **Does not hit**.

---

**Does not hit**

- **The tag `fit call attended`.** Same name, different object, different screen. This workflow is what writes that tag. `VERIFY — whether tag names in this account are case-sensitive · settles by: Settings → Tags`

- **SH - Fit Call No Show** — shares the first 14 characters: `SH - Fit Call `. The character count is the weaker half of the resemblance. The sharper half is that these two are the two outcomes of one appointment, reached from **the same screen by the same person choosing a different status**. A contact's path is identical right up until somebody clicks, and the word that separates the two names sits at the end of both, which is the part a reader confirms last.

- **SH - Fit Call Booked** — shares the first 14: `SH - Fit Call `. Named for the same appointment at the other end of it — Booked fires when the appointment is made, this one when somebody records that it was kept. Anybody handed "the fit call one" has at least three workflow names and four tags to choose between, and all of them are true descriptions of something that happened around one call.
