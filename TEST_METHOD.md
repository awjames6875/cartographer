# TEST_METHOD.md — Written Before Any Run
**Comp #11 · The Cartographer · Safe Harbor GHL Map**
**Method locked:** August 17, 2026
**Rule:** This file does not change after the first run begins. Results get logged; the method stays frozen. Errors and stumbles stay in every transcript verbatim.

---

## Why this file exists
Comp #10 feedback, verbatim: "The three strongest claims — it refuses, it declines, it cannot prescribe — are designed, not shown." This comp, every claim gets tape. Method written first so the receipts cannot be shaped afterward (Comp #9 winning standard).

---

## TEST A — Sadie (insider accuracy check)
**Who:** Sadie, the VA currently inside the account. NOT a stranger test — an accuracy test.
**What she receives:** The full card set + catalog + collision table.
**Her job:**
1. Mark every card line TRUE / FALSE / OUTDATED against the live account
2. Resolve the three VERIFY items:
   - VERIFY-1: Booking slug - safe-harbor-fit-call vs safeharbor-fit-call (test both links live)
   - VERIFY-2: Which tag Vo2's If/Else actually checks - Fit Call Booked vs legacy Appointment Booked
   - VERIFY-3: Daycare Affiliation Tagging workflow - published state confirmed?
3. Name anything live in the account that the map missed
**Logged:** Every correction with date + what the map said + what reality says. Corrections log ships in the repo (outside the drop-in folder).
**Pass:** Map corrected to match reality. A wrong map corrected on tape is a receipt; a wrong map shipped is a failure.

## TEST B — Friend (true stranger, cold wander)
**Who:** Nicole Myrick, who has NEVER been inside Safe Harbor's GHL.
**What they receive:** ONLY the cartographer folder + this task, verbatim:
"Adam asked you to change the timing on the Fit Call nurture texts. Using only this folder: (1) find where to start, (2) tell me what object you'd be touching, (3) tell me what else moves if you change it, and (4) tell me the one thing you might grab by mistake. Then stop."
**Rules:** No help from Adam. No GHL login needed. Every question they ask out loud gets written down. Transcript verbatim, stumbles left in.
**Pass (all four, from the brief's bar):** finds the front door from the catalog; opens ONE card and understands the object; names Hits + the obvious wrong neighbor; stops without loading the rest.
**Fail is publishable:** If they get lost, the transcript ships anyway and the fix gets logged.

## TEST C — Fresh Claude session (model as reader)
**Who:** A brand-new Claude project/session with zero memory of Safe Harbor.
**What it receives:** The drop-in folder per the README's own instructions (catalog first, one card - if the README makes the model load everything, the README fails).
**Task:** Same verbatim task as Test B.
**Logged:** Full transcript, kept as-is.
**Pass:** Same four-part bar as Test B, PLUS: the model does not request or load the full objects folder.

---

## Order of runs
Test A first (fix accuracy) then freeze cards then Test B and Test C on the frozen version. No edits between B and C.

## What ships in the repo
- This file (proof the method predates the runs - commit it Day 1)
- /receipts/ folder OUTSIDE the drop-in: Sadie's dated corrections log, Test B transcript, Test C transcript
