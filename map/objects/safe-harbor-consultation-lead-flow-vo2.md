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
- **Starts Maria.** On the branch where the contact has a phone number, a VAPI "Create a Call" action places the outbound call · settled: Sadie, August 19, 2026. This is the object that starts her — see `objects/maria.md`, which maps her footprint and stops at the VAPI line.
- Writes Maria's call summary and transcript into an internal email, as merge fields · settled: Sadie, August 19, 2026
- Sends the contact the Fit Call booking link, slug `safe-harbor-fit-call` · settled: Sadie, August 19, 2026 (VERIFY-1, settled — see `objects/safe-harbor-fit-call.md`)
- **Reads the tag `Appointment Booked`** to decide whether to send a booking reminder · settled: Sadie, August 19, 2026 (VERIFY-2, settled)
- Adds the tag `Missing Phone Number` on the branch where no phone number is present, and emails named users · settled: Sadie, August 19, 2026

**VERIFY-2 settled, and it opened a longer question.** This workflow *reads* `Appointment Booked`. Every tag-writing object walked on this map writes a different one — `fit call booked`, `fit call nurture`, `fit call no show`, `fit call attended`. Nothing walked so far writes `Appointment Booked`.

`VERIFY — what writes the tag Appointment Booked, if anything does · settles by: the account`

That line is an observation about the walked set, not a verdict about this workflow. Six objects have been read; the account holds more. The map records what each object reads and writes and stops there (`rules.md` §6).

Asked separately whether anything still used the older tag, the walk answered **"NO"** — while the same walk recorded this workflow reading it. Both answers are on the record in `/receipts/`. The map does not reconcile them.

**Tag capitalisation is not settled.** `Appointment Booked` was reported with capitals; the tags the other workflows write were reported in lower case. Whether the account treats those as one tag or two is not something this walk answers. `VERIFY — whether tag names here are case-sensitive · settles by: Settings → Tags`

---

**Does not hit**

- **SH - Fit Call Nurture (Alt Days) — settled, and the answer is no.** This card previously asked whether the nurture sat downstream of this workflow. It does not. The nurture starts when the tag `fit call nurture` is added to a contact, and this workflow never adds that tag · settled: Sadie, August 19, 2026. Somebody sent here to change "the first messages a new lead gets" is in the right place; somebody sent here to change the nurture texts is not, and Lane B is where they belong.

- **An earlier version of this same flow, if one is still in the list.** Still open. The name ends in **Vo2**, which implies something came before it, and Sadie was not asked whether a predecessor survives. `VERIFY — is there an earlier Safe Harbor Consultation Lead Flow in the list · settles by: the workflow list in the account`. If it is there, both answer to the same words in a search box, and an older copy looks exactly as correct as a current one at a glance.

- **GOLDEN COPY - Lead Flow Vo2** — shares `Lead Flow Vo2` with this name, reported a backup draft that was never published. It sorts under G rather than S, so a search box returns both and a scroll down the list does not. Named in `catalog.md` under **Named, and nothing flowing through**.
