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

**This name belongs to two objects.** A published workflow, and a tag called `fit call attended` · settled: Sadie, August 19, 2026 (C-4).

It is **not** an appointment status. Those are system-defined — `confirmed`, `showed`, `no-show`, `cancelled` — and "Fit Call Attended" is not among them · settled: Sadie, August 19, 2026.

This is the third name on the map that belongs to two objects, after `SH - Fit Call Booked` / `fit call booked` and the pair in Lane F.

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

**Two objects carry this name.** The workflow is at Automation → Workflows. The tag `fit call attended` is at Settings → Tags. Check which one you have open before you change anything.

- **The tag `fit call attended`** — not this one. Same name, different screen. This workflow is what writes it. `VERIFY — whether tag names in this account are case-sensitive · settles by: Settings → Tags`
- **`SH - Fit Call No Show`** — not this one. Same first 14 characters: `SH - Fit Call `. Same appointment, same screen, same person — a different status. The word that separates the names sits at the end, which is the part read last.
- **`SH - Fit Call Booked`** — not this one. Same first 14. Booked fires when the appointment is made. This one fires when somebody records it was kept.

**"The fit call one" is at least three workflow names and four tags.** All of them describe something that happened around one call.
