# Safe Harbor Consultation Lead Flow Vo2

**Type:**   workflow · settled: Sadie, August 19, 2026
**Mark:**   LIVE · settled by workflow list captures, Sadie, Aug 21 2026, `receipts/workflow-list-aug20-1.png` + `receipts/workflow-list-aug20-2.png` · **Checked:** August 21, 2026
**Where:**  Automation → Workflows → "Safe Harbor Consultation Lead Flow Vo2"
**Source:** the workflow of that name, opened from the account. Cited, not copied — open the real thing and read it there (`rules.md` §4).

Came here from Lane A of `catalog.md`. Read this card, then open the account. Do not open a second card (`rules.md` §5).

---

**The mark stands on three legs**

`rules.md` §1 wants three things for LIVE. Sadie's walk gave two; the workflow list gave the third:

- **found in the account** — settled: Sadie, August 19, 2026
- **a way in that can fire** — settled: Sadie, August 19, 2026 (the form trigger below)
- **published** — settled by workflow list captures, Sadie, Aug 21 2026, `receipts/workflow-list-aug20-1.png` + `receipts/workflow-list-aug20-2.png`

The third leg stayed open for two days because reading a workflow's steps is not the same as finding it switched on. The workflow list is the screen that shows the switch, and on August 21 it read **Published**.

---

**Hits**

- Fires on a submission of either of the two Safe Harbor website lead forms — form IDs `tP6U9TbhZI7RcUEAeDm1` and `QiHZ9AqGPrLJR596VHON` · settled: Sadie, August 19, 2026
- Adds the tags `Website Lead` and `60-Day Funnel` to the contact on entry · settled: Sadie, August 19, 2026
- Notifies the team twice about the new lead — once by SMS, once by email · settled: Sadie, August 19, 2026
- Adds the tag `Voice AI Called` · settled: Sadie, August 19, 2026
- **Starts Maria.** On the branch where the contact has a phone number, a step in this workflow places an outbound call through VAPI · settled: Sadie, August 19, 2026. **What kind of step is not settled.** It was described two ways in the same walk — a native VAPI "Create a Call" action, and a custom webhook to the VAPI API. One is a form field, the other a request body. `VERIFY — whether the step in this workflow is a native VAPI action or a custom webhook · settles by: opening the step in the account`. This is the object that starts her — see `objects/maria.md`, which maps her footprint and stops at the VAPI line.
- Writes Maria's call summary and transcript into an internal email, as merge fields · settled: Sadie, August 19, 2026
- Sends the contact the Fit Call booking link, slug `safe-harbor-fit-call` · settled: Sadie, August 19, 2026 (VERIFY-1, settled — see `objects/safe-harbor-fit-call.md`)
- **Reads the tag `Appointment Booked`** to decide whether to send a booking reminder · settled: Sadie, August 19, 2026 (VERIFY-2, settled)
- Adds the tag `Missing Phone Number` on the branch where no phone number is present, and emails named users · settled: Sadie, August 19, 2026

**This workflow reads the tag `Appointment Booked`. Nothing walked on this map writes that tag.** The other objects write `fit call booked`, `fit call nurture`, `fit call no show` and `fit call attended` · settled: Sadie, August 19, 2026.

`VERIFY — what writes the tag Appointment Booked, if anything does · settles by: the account`

Six objects have been read. The account holds more. This is a record of what was read, not a finding (`rules.md` §6).

The walk was also asked whether anything still uses the older tag and answered **"NO"** — in the same walk that recorded this workflow reading it. Both answers are in `/receipts/`. The map does not pick between them.

`Appointment Booked` was reported with capitals. The other tags were reported in lower case. `VERIFY — whether tag names here are case-sensitive · settles by: Settings → Tags`

---

**Does not hit**

**The full name of this one is `Safe Harbor Consultation Lead Flow Vo2`. Read it to the end.**

- **`SH - Fit Call Nurture (Alt Days)`** — not this one. This workflow never adds the tag `fit call nurture`, and that tag is the only thing that starts the nurture · settled: Sadie, August 19, 2026. Sent here to change the nurture texts? That is Lane B.
- **`GOLDEN COPY - Lead Flow Vo2`** — not this one. Shares `Lead Flow Vo2`. Reported a backup draft, never published. It sorts under G, not S — a search returns both, scrolling the list does not.
- **An earlier version of this flow, if one is still in the list.** The name ends in `Vo2`. Nobody was asked whether something came before it. An older copy looks exactly like a current one. `VERIFY — is there an earlier Safe Harbor Consultation Lead Flow in the list · settles by: the workflow list in the account`
