# TEST A — Corrections Log
**Comp #11 · The Cartographer · Safe Harbor GHL Map**
**Walked by:** Sadie, Safe Harbor's VA — the person currently inside this account
**Date of walk:** August 19, 2026
**How it ran:** Sadie walked the account alone, on screen recording, working from the
question file frozen in `TEST_METHOD.md` on Aug 17 — two days before this run. Adam was
not on the call. Her answers and the recording are hers, unedited.
**What this test is and is not:** Sadie is an insider. This is an accuracy check, not a
stranger test. Tests B and C are the stranger tests.
**Recording:** https://www.loom.com/share/ef01e85c27e1444aa384ddc9e2821551 — Loom, Aug 19, 2026

---

## What the map got wrong

Every line below: what the card claimed, what the account showed, and who settled it.
Nothing here was corrected quietly. The VERIFY shape was committed on Aug 18 (`b725dfe`,
`9678c67`) before this walk, so the git history shows these answers arrived after the
questions, not the other way around.

### C-1 · The booking slug — VERIFY-1 settled
- **Map said:** two spellings in circulation, canonical unknown, top-priority VERIFY
- **Account shows:** `safe-harbor-fit-call` is live. `safeharbor-fit-call` returns 404.
- **Settled by:** Sadie, Aug 19 2026 — opened the calendar, read the link, tested both
- **Where it lands:** `safe-harbor-fit-call.md`, `collisions.md` row 9

### C-2 · Vo2 checks a different tag than the Booked workflow writes — VERIFY-2 settled
- **Map said:** unknown which tag Vo2's If/Else checks
- **Account shows:** Vo2's If/Else checks the tag **`Appointment Booked`**.
  `SH - Fit Call Booked` adds the tag **`fit call booked`**. Both tags exist in the account.
- **Also on record:** asked whether anything still uses the older tag, the walk answered
  "NO" — while the same walk recorded Vo2 checking it. Both answers are kept. The map
  records what each object reads and writes; it does not resolve the contradiction.
- **Settled by:** Sadie, Aug 19 2026 — opened the workflow, read the If/Else step
- **Where it lands:** `safe-harbor-consultation-lead-flow-vo2.md`, `sh-fit-call-booked.md`,
  `collisions.md` row 4 (moves from unsettled to a live pair)

### C-3 · Daycare — still published, not off
- **Map said:** Adam believed the workflow was turned off
- **Account shows:** `Daycare Affiliation Tagging` was **published** at the time of the
  walk. The custom field "Are you from Innovators of the Future?" is gone. The tags
  `Daycare Referral` and `Daycare - Angelicas Connection` still exist. No other workflow
  in Parent Intake references them. Sadie turned the workflow off during the walk.
- **Settled by:** Sadie, Aug 19 2026
- **Where it lands:** new leftover line in `catalog.md`. The mark reflects the state at
  the time of the walk and says the state changed during it.

### C-4 · SH - Fit Call Attended is both a workflow and a tag
- **Map said:** type inferred as workflow from the `SH - ` naming pattern, flagged as an
  inference rather than a finding
- **Account shows:** a published workflow (v5, created Aug 12 2026) **and** a tag
  `fit call attended`. Not an appointment status — those are system-defined.
- **Settled by:** Sadie, Aug 19 2026
- **Where it lands:** `sh-fit-call-attended.md`. This is a third instance of the pattern
  already carried by `Fit Call Booked` — same words, two object types, two screens.

### C-5 · Attended and No Show are set by hand
- **Map said:** open question — calendar or a person
- **Account shows:** a person changes the appointment status by hand. The platform does
  not flip it automatically after the time passes. `SH - Fit Call Attended` fires on
  status "showed"; `SH - Fit Call No Show` fires on status "No Show".
- **Settled by:** Sadie, Aug 19 2026
- **Where it lands:** both cards, and the calendar card. This changes what "hits" means
  for these two objects — the trigger is a human action, not an elapsed time.

### C-6 · Intake Journey Stage is a leftover, not a ghost
- **Map said:** GHOST, with the fork clause — found in the account would make it LEFTOVER
- **Account shows:** the custom field is **found** in Settings → Custom Fields
- **Settled by:** Sadie, Aug 19 2026
- **Where it lands:** moves out of "Names that route nowhere" into the leftover section.
  The fork clause worked as written — the mark flipped on evidence, not on a rewrite.

### C-7 · The nurture campaign is two campaigns, both published
- **Map said:** one campaign, called "the forms-nurture campaign" (Adam's nickname),
  in build, not live — with a VERIFY asking for its real name
- **Account shows:** **two** published campaigns: `Paperwork Reminder Nurture` and
  `SH - Assessment Booking Nurture`
- **Settled by:** Sadie, Aug 19 2026
- **Where it lands:** they leave the ghost section entirely. Two live objects the map
  did not have. The VERIFY asking for the real name is what surfaced them — a nickname
  would never have been searchable.

### C-8 · Maria's GHL footprint located
- **Map said:** unknown which GHL object carries her; card declined to guess a screen
- **Account shows:** a VAPI "Create a Call" action inside a workflow (Vo2), reachable
  from Automation → Workflows → Add action, once VAPI is connected in
  Settings → Integrations
- **Settled by:** Sadie, Aug 19 2026
- **Where it lands:** `maria.md`. The boundary itself holds — what she says still lives
  in VAPI, outside this map.

### C-9 · Sarah is in a different sub-account
- **Map said:** GHL-native inbound voice AI, inside the boundary, screen unconfirmed
- **Account shows:** Sarah is configured under the **Safe Harbor Behavioral Health**
  sub-account, not Safe Harbor Parent Intake. Calls she answers are stored there. She
  does not create contacts in Parent Intake.
- **Settled by:** Sadie, Aug 19 2026
- **Where it lands:** `sarah.md` becomes a boundary card like Maria's. Collision #8 is
  no longer "which direction" — it is "which sub-account," which is collision #8 and
  the two-sub-account collision turning out to be the same trap.

---

## What the map got right
- `SH - Fit Call Booked` does remove the contact from `SH - Fit Call Nurture (Alt Days)`
  and does remove the `fit call nurture` tag. A booked contact does not keep receiving
  nurture texts. This was the question blocking Test B, and the answer is clean.
- The nurture sequence is SMS-only, every 2 days, and removes its own tag at the end.
- `SH - Fit Call No Show` re-adds the nurture tag on its NO branch after 2 days.

## Limits of this test
- Sadie is inside this account daily. She is not a stranger, and this run proves nothing
  about whether a stranger can walk the map. That is Test B and Test C.
- She ran it alone. Nobody pushed back in the moment on the one answer that contradicts
  itself (C-2). Both halves are kept on record rather than reconciled.
- One object was changed during the walk (C-3, the daycare workflow). The map records
  the state at the time of the walk and says so.

---

## Corrections Log

Corrections arriving after the Aug 19 walk. Same test, later evidence, logged on the date
it came in. The C-1 through C-9 entries above are the walk itself and stay as they were.

### 2026-08-21 — Test A, Sadie workflow-list captures

**The evidence:** `receipts/workflow-list-aug20-1.png` and `receipts/workflow-list-aug20-2.png`,
received August 21, 2026. *The filenames read `aug20` and are wrong — they were typed by hand
on arrival, not produced by the source.* The captures are from August 21. The files are not
being renamed after the fact; the names stand and the error is recorded here, because quietly
correcting a receipt is the thing this folder exists to not do.

This is the workflow list — the screen `rules.md` §2 already names as what settles a published
state.

#### What the captures settled

- **Four marks move to LIVE.** `Safe Harbor Consultation Lead Flow Vo2`,
  `SH - Fit Call Nurture (Alt Days)`, `SH - Fit Call Booked` and `SH - Fit Call No Show` all
  read **Published**. Each already carried two of the three legs `rules.md` §1 wants for LIVE,
  settled on the Aug 19 walk; this screen is the third. All four rows are legible in capture 1.
  Applied to the four cards and to `catalog.md`.
- **"Fit Call Nurture" is two workflows** — `SH - Fit Call Nurture Trigger (24hr Check)` and
  `SH - Fit Call Nurture (Alt Days)`, both reading Published. The Trigger has no card. Lane B's
  named trap is the word *nurture*, and this is one more object carrying it.
- **`VAPI Transcript to Apollo`** reads Published and is not in `catalog.md`. Status TBD.
- **`Needs review (1)`** tab carries one item, unidentified.
- **`Paperwork Reminder Nurture`** — already reclassified by C-7 (Aug 19). No action needed.
  Line originated from an older reading, kept for trail.

#### The count is withdrawn

An earlier reading of these captures put the live workflow count at **8**. That number is wrong
and the reasoning behind it was wrong. Both are struck rather than amended.

What stands: **the walked set is 8.** The account holds substantially more published workflows
than that. The exact number is **unsettled** — the captures cross sub-accounts, and no
single-account list has been read end to end.

`VERIFY — how many published workflows the Parent Intake sub-account holds · settles by: that
sub-account's workflow list alone, read end to end`

#### Daycare Affiliation Tagging — contradicted, not resolved

- **C-3 (Aug 19) says:** Sadie found the workflow published and **switched it off during the walk**.
- **The Aug 21 capture shows:** `Daycare Affiliation Tagging`, in the list, reading **Published**.

Both are on the record. This log does not resolve which is true and does not name a cause —
`rules.md` §6 bans the verdict. An earlier reading of these captures reported no daycare workflow
in the live list at all; that reading was wrong and is struck.

`VERIFY — whether Daycare Affiliation Tagging is published today, and what moved it between
Aug 19 and Aug 21 · settles by: the Parent Intake workflow list, plus the workflow's own history`

#### The captures cross sub-accounts — C-9 recurring

The panels are not all one account. Alongside the Parent Intake objects, the captures show
`Safe Harbor Client Welcome`, `Post Session Follow Up`, `Safe Harbor Session Reminders`,
`GG - Day Intake Nurture`, and a further set including `Student Check-in`, `QR Check-in` and
`Child Contacts`.

**Counting across these captures counts several accounts at once** — which is the most likely
source of the withdrawn 8.

This is **C-9 recurring**. The same trap that put Sarah in the wrong sub-account: right product,
familiar screens, different account, and nothing on the screen announcing which one is being
read. It fails quietly. It caught a reading of this map's own evidence two days after the map
first wrote the trap down.

#### Limits of this round

- **Two composites is all there is.** The gallery header reads **6 photos**; two composite
  captures were received. The other four have not been obtained.
- **These are photos of a phone gallery, not the screen itself.** Panels are stacked and
  scrolled, rows are cropped at the top and bottom of some panels, and the `Last updated` and
  `Created on` columns are not legible at this resolution. Nothing has been read from those
  columns.
- **No single-account list has been read end to end,** which is why the count above is left open
  rather than replaced with a better number.
