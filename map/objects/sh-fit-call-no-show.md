# SH - Fit Call No Show

**Type:**   workflow · settled: Sadie, August 19, 2026
**Mark:**   VERIFY — not confirmed · settles by: the published state in the workflow list · **Checked:** August 19, 2026
**Where:**  Automation → Workflows → "SH - Fit Call No Show"
**Source:** the workflow of that name, opened from the account. Cited, not copied — open the real thing and read it there (`rules.md` §4).

Came here from Lane D of `catalog.md`. Read this card, then open the account. Do not open a second card (`rules.md` §5).

---

**The mark is one leg short**

`rules.md` §1 wants three things for LIVE. Sadie's walk gave two:

- **found in the account** — settled: Sadie, August 19, 2026
- **a way in that can fire** — settled: Sadie, August 19, 2026 (the status trigger below)
- **published** — *not confirmed.* She read the trigger and the steps, which a draft also shows. She was not asked the published state of this one.

---

**Hits**

- Fires when an appointment on the **Safe Harbor Fit Call** calendar is set to status **No Show** — calendar ID `AuOmiT3Afi2aXSlH7JJQ`, standard events and contacts only · settled: Sadie, August 19, 2026
- Removes the tag `fit call booked` · settled: Sadie, August 19, 2026
- Adds the tag `fit call no show` · settled: Sadie, August 19, 2026
- Sends the contact one rebooking SMS, from the contact owner, carrying the booking link — slug `safe-harbor-fit-call` · settled: Sadie, August 19, 2026 (VERIFY-1, settled)
- Waits 2 days, then checks whether the contact now carries `fit call booked` · settled: Sadie, August 19, 2026
- **On the branch where they have not re-booked, adds the tag `fit call nurture`** — which starts **SH - Fit Call Nurture (Alt Days)** from its first message · settled: Sadie, August 19, 2026. On the branch where they have re-booked, nothing further runs.

**A person sets the no-show, not the calendar** · settled: Sadie, August 19, 2026 (C-5).

The platform does not flip an appointment to No Show when the time passes. Somebody opens the appointment and changes the status by hand, and that hand movement is the only thing that reaches this workflow. Two consequences follow, and neither is visible from inside the workflow:

- If nobody updates statuses, this workflow never fires. The contact keeps whatever tags they had and no rebooking SMS goes out.
- Whoever does update statuses is the trigger. Changing anything in here changes what happens when *they* click, not what happens when a call is missed.

**This is the object that puts contacts back into the nurture.** Anybody changing nurture timing should know the sequence has two doors: the tag applied here after 2 days, and whatever else adds `fit call nurture`. Lane B is the sequence itself.

---

**Does not hit**

- **SH - Fit Call Nurture (Alt Days)** — shares the first 15 characters: `SH - Fit Call N`. A search box typed that far returns both, and these two are the closest pair on the walked map by name. They are also genuinely connected — this workflow re-adds the tag that starts that one — so the resemblance in the names is not the only reason a reader ends up holding the wrong one. Lane B carries the collision from the other side, and now names two further nurture campaigns Sadie found.

- **SH - Fit Call Attended** — shares the first 14: `SH - Fit Call `, and the two are the two outcomes of the same appointment, set by the same person on the same screen by choosing a different status. A contact's path is identical until somebody clicks.

- **SH - Fit Call Booked** — shares the first 14: `SH - Fit Call `. It removes the tag this workflow adds, and this workflow removes the tag it adds. Reading either one alone shows half of that.
