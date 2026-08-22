# SH - Fit Call Booked

**Type:**   workflow · settled: Sadie, August 19, 2026
**Mark:**   LIVE · settled by workflow list captures, Sadie, Aug 21 2026, `receipts/workflow-list-aug20-1.png` + `receipts/workflow-list-aug20-2.png` · **Checked:** August 21, 2026
**Where:**  Automation → Workflows → "SH - Fit Call Booked"
**Source:** the workflow of that name, opened from the account. Cited, not copied — open the real thing and read it there (`rules.md` §4).

Came here from Lane C of `catalog.md`. Read this card, then open the account. Do not open a second card (`rules.md` §5).

---

**The mark stands on three legs**

`rules.md` §1 wants three things for LIVE. Sadie's walk gave two; the workflow list gave the third:

- **found in the account** — settled: Sadie, August 19, 2026
- **a way in that can fire** — settled: Sadie, August 19, 2026 (the calendar trigger below)
- **published** — settled by workflow list captures, Sadie, Aug 21 2026, `receipts/workflow-list-aug20-1.png` + `receipts/workflow-list-aug20-2.png`

The third leg stayed open for two days because reading a workflow's steps is not the same as finding it switched on. The workflow list is the screen that shows the switch, and on August 21 it read **Published**.

---

**Hits**

- Fires when a contact books on the **Safe Harbor Fit Call** calendar — calendar ID `AuOmiT3Afi2aXSlH7JJQ`, contact mode only. It fires from the booking itself, not from a tag · settled: Sadie, August 19, 2026
- Removes the contact from **SH - Fit Call Nurture (Alt Days)** · settled: Sadie, August 19, 2026
- Removes the tag `fit call nurture` · settled: Sadie, August 19, 2026
- Removes the tag `fit call no show`, clearing any earlier no-show state · settled: Sadie, August 19, 2026
- Adds the tag `fit call booked` · settled: Sadie, August 19, 2026

**This workflow sends nothing.** It has no SMS step and no email step — every action it takes is a tag or a workflow removal · settled: Sadie, August 19, 2026.

**Sent here to change the confirmation message? It is not in this workflow.** The Fit Call calendar auto-confirms and sends its own confirmation from its own screen · settled: Sadie, August 19, 2026. That object is `objects/safe-harbor-fit-call.md`.

`VERIFY — whether any reminder before the call exists, and whether it comes from the calendar's notification settings or from a step somewhere else · settles by: the calendar's notification settings in the account`

**This workflow writes `fit call booked`. Vo2 reads `Appointment Booked`.** Two different tags. Both exist in the account · settled: Sadie, August 19, 2026 (VERIFY-2). Nothing walked writes `Appointment Booked`.

`VERIFY — what writes the tag Appointment Booked, if anything does · settles by: the account`

A record of what each object reads and writes. Not a finding (`rules.md` §6), and the walk was not asked the question.

---

**Does not hit**

**Two objects carry this name.** The workflow is at Automation → Workflows. The tag `fit call booked` is at Settings → Tags. Check which one you have open before you change anything.

- **The tag `fit call booked`** — not this one. Same words, different screen. This workflow is what writes it. `VERIFY — whether tag names in this account are case-sensitive · settles by: Settings → Tags`
- **`SH - Fit Call No Show`** — not this one. Same first 14 characters: `SH - Fit Call `. The word that separates them sits at the end. It removes the tag this workflow adds.
- **The `Safe Harbor Fit Call` calendar** — not this one. Sent here about message wording or booking times? The calendar owns those. This workflow only reacts to a booking on it.
