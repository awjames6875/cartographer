# SH - Fit Call No Show

**Type:**   workflow · settled: Sadie, August 19, 2026
**Mark:**   LIVE · settled by workflow list captures, Sadie, Aug 21 2026, `receipts/workflow-list-aug20-1.png` + `receipts/workflow-list-aug20-2.png` · **Checked:** August 21, 2026
**Where:**  Automation → Workflows → "SH - Fit Call No Show"
**Source:** the workflow of that name, opened from the account. Cited, not copied — open the real thing and read it there (`rules.md` §4).

Came here from Lane D of `catalog.md`. Read this card, then open the account. Do not open a second card (`rules.md` §5).

---

**The mark stands on three legs**

`rules.md` §1 wants three things for LIVE. Sadie's walk gave two; the workflow list gave the third:

- **found in the account** — settled: Sadie, August 19, 2026
- **a way in that can fire** — settled: Sadie, August 19, 2026 (the status trigger below)
- **published** — settled by workflow list captures, Sadie, Aug 21 2026, `receipts/workflow-list-aug20-1.png` + `receipts/workflow-list-aug20-2.png`

The third leg stayed open for two days because reading a workflow's steps is not the same as finding it switched on. The workflow list is the screen that shows the switch, and on August 21 it read **Published**.

---

**Hits**

- Fires when an appointment on the **Safe Harbor Fit Call** calendar is set to status **No Show** — calendar ID `AuOmiT3Afi2aXSlH7JJQ`, standard events and contacts only · settled: Sadie, August 19, 2026
- Removes the tag `fit call booked` · settled: Sadie, August 19, 2026
- Adds the tag `fit call no show` · settled: Sadie, August 19, 2026
- Sends the contact one rebooking SMS, from the contact owner, carrying the booking link — slug `safe-harbor-fit-call` · settled: Sadie, August 19, 2026 (VERIFY-1, settled)
- Waits 2 days, then checks whether the contact now carries `fit call booked` · settled: Sadie, August 19, 2026
- **On the branch where they have not re-booked, adds the tag `fit call nurture`** — which starts **SH - Fit Call Nurture (Alt Days)** from its first message · settled: Sadie, August 19, 2026. On the branch where they have re-booked, nothing further runs.

**A person sets the no-show, not the calendar** · settled: Sadie, August 19, 2026 (C-5).

The platform does not flip the status when the time passes. Somebody opens the appointment and changes it by hand. That click is the only thing that reaches this workflow. Neither consequence below is visible from inside it:

- If nobody updates statuses, this workflow never fires. No rebooking SMS goes out.
- Changing anything in here changes what happens when somebody clicks — not what happens when a call is missed.

**This is the object that puts contacts back into the nurture.** The sequence has two doors: the tag this workflow adds after 2 days, and whatever else adds `fit call nurture`. Lane B is the sequence itself.

---

**Does not hit**

**The full name of this one is `SH - Fit Call No Show`. Read it to the end.**

- **`SH - Fit Call Nurture (Alt Days)`** — not this one. Same first 15 characters: `SH - Fit Call N`. A search typed that far returns both. This workflow re-adds the tag that starts it. Lane B is the nurture itself.
- **`SH - Fit Call Attended`** — not this one. Same first 14. Same appointment, same screen, same person — a different status. A contact's path is identical until somebody clicks.
- **`SH - Fit Call Booked`** — not this one. Same first 14. It removes the tag this workflow adds; this workflow removes the tag it adds. Reading either one alone shows half of that.
