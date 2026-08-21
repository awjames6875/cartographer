# SH - Fit Call Booked

**Type:**   workflow · settled: Sadie, August 19, 2026
**Mark:**   VERIFY — not confirmed · settles by: the published state in the workflow list · **Checked:** August 19, 2026
**Where:**  Automation → Workflows → "SH - Fit Call Booked"
**Source:** the workflow of that name, opened from the account. Cited, not copied — open the real thing and read it there (`rules.md` §4).

Came here from Lane C of `catalog.md`. Read this card, then open the account. Do not open a second card (`rules.md` §5).

---

**The mark is one leg short**

`rules.md` §1 wants three things for LIVE. Sadie's walk gave two:

- **found in the account** — settled: Sadie, August 19, 2026
- **a way in that can fire** — settled: Sadie, August 19, 2026 (the calendar trigger below)
- **published** — *not confirmed.* She read the trigger and the steps, which a draft also shows. She was not asked the published state of this one.

---

**Hits**

- Fires when a contact books on the **Safe Harbor Fit Call** calendar — calendar ID `AuOmiT3Afi2aXSlH7JJQ`, contact mode only. It fires from the booking itself, not from a tag · settled: Sadie, August 19, 2026
- Removes the contact from **SH - Fit Call Nurture (Alt Days)** · settled: Sadie, August 19, 2026
- Removes the tag `fit call nurture` · settled: Sadie, August 19, 2026
- Removes the tag `fit call no show`, clearing any earlier no-show state · settled: Sadie, August 19, 2026
- Adds the tag `fit call booked` · settled: Sadie, August 19, 2026

**This workflow sends nothing.** It has no SMS step and no email step — every action it takes is a tag or a workflow removal · settled: Sadie, August 19, 2026.

That matters because of the sentence that sends people to Lane C. **"Change the confirmation message" does not land here.** The Fit Call calendar is set to auto-confirm and carries its own confirmation message to clients, so the text somebody receives on booking comes from the calendar's screen, not from this workflow · settled: Sadie, August 19, 2026. `objects/safe-harbor-fit-call.md` is that object. Anybody who opens this workflow looking for message wording will find tags and leave without finding it.

`VERIFY — whether any reminder before the call exists, and whether it comes from the calendar's notification settings or from a step somewhere else · settles by: the calendar's notification settings in the account`

**The tag it writes is not the tag Vo2 reads.** This workflow adds `fit call booked`. **Safe Harbor Consultation Lead Flow Vo2** reads `Appointment Booked` before deciding whether to send a booking reminder · settled: Sadie, August 19, 2026 (VERIFY-2). Both tags exist in the account. Nothing walked so far writes `Appointment Booked` — `VERIFY — what writes the tag Appointment Booked, if anything does · settles by: the account`.

That is a record of what each object reads and writes. It is not a finding about whether anything is wrong (`rules.md` §6), and the walk was not asked the question.

---

**Does not hit**

- **The tag named `fit call booked`.** Same words, different kind of object, different screen: this workflow lives under Automation → Workflows, the tag under Settings → Tags. Somebody saying "the fit call booked thing" could mean either one, and they are changed in two different places. This workflow is what writes that tag, which makes the pair easier to confuse rather than harder — `VERIFY — whether tag names in this account are case-sensitive · settles by: Settings → Tags`.

- **SH - Fit Call No Show** — shares the first 14 characters: `SH - Fit Call `. Both are named for something that happens after a booking exists, and the difference between them is whether the person turned up, which is a word that sits late in both names. They are also linked in fact: No Show removes the tag this workflow adds.

- **The Safe Harbor Fit Call calendar.** The near-miss for anybody sent here about message wording or booking times. This workflow reacts to a booking on that calendar; it does not own the calendar, its availability, its confirmation message, or its link.
