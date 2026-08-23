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

---

### 2026-08-22 — Pre-Test-B plain-language pass

**Not a correction against the account. A correction against the reader.**

**Why it happened:** Adam read Lane B of `catalog.md` and the `SH - Fit Call Nurture (Alt Days)`
card as a stranger would, and could not follow the **Does not hit** section on first read. The
author of a map failing to parse his own warning section is a failure of the map, not of the
reader. Nicole walks it next, cold, with no author's memory to fall back on.

**Requested Aug 21, run Aug 22.** Dated the day the edits were made, not the day the problem was
found.

#### The rules applied

- Short sentences.
- The warning first. The explanation after, or not at all.
- **"Don't"** where the line is a warning about the territory. Ruled in scope by Adam: the map
  already says *"Confirm the name at the top of the screen,"* so a warning is not a
  recommendation and does not break `rules.md` §6.
- Cut the explanation of **why** a trap exists. Name the trap.
- No *"you should," "consider," "it would be better if,"* or any fix language.

#### What this pass did not touch

- **No mark changed.** No object moved between LIVE, LEFTOVER, GHOST or declined.
- **No VERIFY was removed, settled, or reworded into something weaker.** Every open question that
  went into this pass came out of it.
- **No fact changed** — every `settled: <name>, <date>` line kept its name and its date.
- `identity.md` and `rules.md` untouched, as always.

#### One thing that was not a wording change

Rewriting Lane B surfaced a claim that was simply wrong. The card and the catalog both said that
typing `nurture` into the search box returns *"all five names above"* — a list that included
`SH - Fit Call No Show` and `SH - Fit Call Booked`. Neither name contains the word. That sentence
had been carried since the Lane B collision set was first written and survived the walk.

It now reads five results and says what they are: three that send texts, the tag `fit call
nurture`, and the one nobody has opened. That is what the search returns.

`reference/collisions.md` had it right the whole time. The catalog and the card did not.

#### Scope

Rewritten: `catalog.md`, all eight cards in `objects/`, and `reference/collisions.md`.
`identity.md` and `rules.md` untouched.

**`catalog.md` was written last, and not by choice.** It sat locked by Microsoft Word for the
first half of this pass — readable, not writable — while the cards and the collision table were
rewritten around it. Word held an exclusive write lock without ever having saved: when it was
closed the file hashed byte-identical to the previous commit, so nothing it touched was changed.
Checked before anything was edited: no curly quotes introduced (153 before, 153 in the committed
version), `·` and `→` intact, UTF-8, no BOM, LF endings.

`~$*` was added to `.gitignore` the same day. Word drops a `~$catalog.md` owner file beside any
file it opens, and a Word that is killed rather than closed leaves it behind — inside the
drop-in folder, where it would travel to Nicole with everything else.

---

### 2026-08-22 — Test B, a second task added

**`TEST_METHOD.md` is not edited.** It was locked on August 17, 2026, before any run, and
Test A ran against it on August 19. Editing it now would break the single claim this comp
was built to make. What follows is an **addition**, logged here with its date. The frozen
file stands exactly as written, and its Test B task stands with it.

**Why a second task.** The frozen Test B task is the Fit Call nurture task. That task is
now worked end to end in `README.md` at the repository root — all four parts of the bar,
including the object, what moves with it, and the wrong-neighbour grab. That README sits
**outside** the drop-in folder, so the frozen task survives as long as Nicole receives the
zipped `map/` folder and never the repository or the GitHub link. This second task removes
the dependency on that being handled correctly by whoever sends the folder.

**How the object was chosen.** Three carded objects appear nowhere in `map/examples.md` or
the root `README.md` — checked by filename and by object name, both returning zero:
`sh-fit-call-attended.md`, `maria.md`, `sarah.md`. The first was chosen because it tests
the map rather than the boundary. It is a workflow and a tag sharing one name, it sends
nothing, and it only fires when a person sets an appointment status by hand. All four parts
of the bar are reachable from it.

**The task, verbatim:**

> Adam asked you to change the message someone gets after they turn up for their fit call.
> Using only this folder: (1) find where to start, (2) tell me what object you'd be
> touching, (3) tell me what else moves if you change it, and (4) tell me the one thing you
> might grab by mistake. Then stop.

The four-part bar is copied unchanged from `TEST_METHOD.md`. Only the opening sentence
differs.

**What the sentence deliberately does not do.** It names no object, no lane, no screen and
no tag. It uses the words somebody would actually say out loud. `fit call` is Safe Harbor's
own word for the appointment and appears in the frozen task too, so it gives away nothing
the original did not.

**What it walks into.** That object sends nothing — no SMS, no email. A reader sent looking
for a message will not find one. Whether the map tells them that before they go hunting is
what this run measures.

**A known limit of this run: the folder primes her for the shape.** `map/examples.md`
Example 1 teaches exactly this pattern — a reader sent looking for a message, the obvious
lane empty, the message living on another object entirely. Different object, same shape.
So this task does not measure whether Nicole derives that pattern cold. It measures whether
she can apply a pattern the folder taught her to an object she has not seen worked. That is
a weaker claim than the frozen nurture task makes, and it is the price of picking an object
the folder has not already walked. Both facts are on the record; neither is withdrawn.

---

### 2026-08-22 — Test B shipped broken, was paused, and restarted

**The first archive reached the tester unusable.** This is logged because it happened, not
because it changed a finding.

**What broke.** The archive was built on Windows with PowerShell 5.1's `Compress-Archive`,
which writes **backslashes** as path separators inside the zip. The ZIP specification
(APPNOTE 4.4.17.1) requires forward slashes. Windows readers tolerate the violation, so the
archive verified as correct on the machine that made it. macOS does not: it read each stored
path as a literal filename. Nicole opened it and got **14 flat files** called
`map\catalog.md`, `map\objects\maria.md` and so on, with no folder structure at all.

**How it was caught.** By the tester, on her machine, after the archive had been sent.
Not by the checks that were run before sending it. Those checks read the entry table and
confirmed the contents were the right 14 files with nothing extra — and every one of them
passed, because a Windows reader shows a backslash path as a folder path. The verification
was real and it was blind to the one thing that mattered.

**The obvious fix also failed.** `[System.IO.Compression.ZipFile]::CreateFromDirectory` was
tried second and wrote backslashes too — .NET Framework 4.8 on this machine still uses the
platform separator. It was caught before sending only because the entry table was checked
again rather than assumed. The working method was **bsdtar** (libarchive 3.8.4, shipped in
Windows), which writes forward slashes.

**How the rebuild was verified.** Three independent ways, because one was not enough the
first time: the .NET entry table, bsdtar's own listing of the finished file, and a raw byte
scan of the archive for the sequence `map\`. Zero backslash paths. Seventeen entries — the
14 files plus explicit directory records for `map/`, `map/objects/` and `map/reference/`.
No `receipts/`, no `.git`, no `scratchpad/`, no root `README.md`, no `TEST_METHOD.md`.

**What it cost the run, stated rather than waved off.** The flat listing showed Nicole all
fourteen filenames in one view, including `map\objects\sh-fit-call-attended.md` — the object
her task points at. The folder is built so a reader never sees that inventory: `rules.md` §5
refuses the whole `objects/` folder, and `map/README.md` says there is never a reason to
list the directory. A flat unpack is a weaker version of exactly that. She saw the card
names before opening the catalog.

**Whether she opened any of them is not known and is not assumed here.** What is known: the
run was paused on discovery and restarted with the corrected archive, and she had the broken
one in hand before the restart. Whoever reads the Test B transcript should read it knowing
the object names were visible first. `TEST_METHOD.md` is not edited.

---

### 2026-08-22 — Test B, the tester opened catalog.md before the run

**This entry is written before her transcript arrives.** That is the point of it, and the
git history is the proof: this commit lands before any commit carrying her answers. It is
logged now precisely so it cannot later be read as an excuse shaped around a result.

**What she opened, in her own word:** *"catalogue."* That is `catalog.md`. It became
openable when the broken archive unpacked flat on her Mac (previous entry).

**How much of it she read is not known.** She was not asked, and nothing here assumes an
answer. She may have opened it and closed it. She may have read the whole page.

**What that costs the frozen bar — more than part (1).** `catalog.md` is hop one, so part
(1), *find where to start*, is pre-exposed. But the lanes are not an index. Each one carries
a compressed answer to the rest of the bar, and Lane E — the lane her task lands on — is no
exception:

- **Part (2), what object you'd be touching.** Lane E names `SH - Fit Call Attended`
  outright, gives its screen, and gives its card path.
- **Part (3), what else moves.** Lane E says the workflow *"moves tags and pulls the contact
  out of the nurture,"* and that a person sets it by hand.
- **Part (4), the one thing you might grab by mistake.** Lane E carries its own
  **Not this one** line, naming the near-miss.
- And Lane E's *also said as* list includes **"the post-call message"** — which is her task
  sentence, near enough word for word.

**So the honest statement is not that parts 2, 3 and 4 remain clean.** They remain clean
only if she did not read Lane E, and that is unknown. What the cards still add beyond the
lane is depth: the full **Hits** list, the reasoning under each near-miss, and the open
`VERIFY` lines. A reader who had only Lane E could answer all four parts thinly. A reader
who opened the card answers them properly. The transcript will show which one this was, and
that is now the thing to read it for.

**What this run no longer measures at all:** a cold first arrival at the front door. She has
been there. Whether the catalog routes a stranger who has never seen it is not a question
this run can answer any more.

**Why this is recorded against the map rather than against her.** She did exactly what a
person does with a folder of loose files — she opened the one whose name sounded like a
starting point. That she picked the front door out of fourteen flat filenames is arguably
the catalog doing its job under the worst possible conditions. It is still an exposure, and
it is still logged as one.

`TEST_METHOD.md` is not edited.

#### How this entry got written, which is part of the evidence

The version above is not the version that was asked for. The instruction was to log the
exposure with this among its bullets, verbatim:

> What the run still measures cleanly: parts 2, 3 and 4 — the card, what else moves, the
> wrong-neighbour grab. All live in `objects/`, which she did not open.

That is the flattering reading, and it is wrong. It treats the lanes in `catalog.md` as an
index that only points. They are not. Lane E was opened and quoted before this entry was
written, and it names the object, gives its screen and its card path, says what else moves,
carries its own **Not this one** line, and lists *"the post-call message"* among the phrases
somebody would say — which is the task sentence. Parts 2, 3 and 4 are answerable from the
lane alone, thinly.

The claim was checked against the file instead of being taken on trust, the difference was
raised rather than quietly applied, and the accurate version was written in its place and
kept.

**Who proposed it is the part worth recording.** It came from Adam — the person with the
most to gain from the generous reading — and it came *before* the transcript arrived, when
nobody could yet know whether a generous reading would be needed or what it would be
covering for. It was withdrawn on the evidence, in the same window, and the correction is
in this file rather than in a conversation nobody else can see.

The claim in this folder is that the receipts were not shaped toward a flattering result.
This is what that looks like when it is tested on a live entry rather than asserted.

---

## TEST B — Nicole — August 22, 2026

# The door did not hand off. The map failed.

**Logged before any edit to `README.md`.** No fix is in this commit. `TEST_METHOD.md` says a
failed run ships anyway and the fix gets logged after; this is the run shipping first.

**Tester:** Nicole. A genuine domain outsider — never inside Safe Harbor's GoHighLevel.
**Prior exposure:** logged in advance at `5b48f88`, before this transcript existed.
**Duration:** about 20 minutes.

### What happened

She read **`map/README.md`** and nothing else. She opened no other file. She never reached
`catalog.md`, and she never opened a card.

Parts **3** and **4** of her task — *what else moves if you change it*, and *the one thing
you might grab by mistake* — came back **unanswered**. Both live in the card she never
opened. Whether parts 1 and 2 were answered is not recorded in what was supplied for this
entry, and is not assumed here.

Against `TEST_METHOD.md`'s own four-part bar, the first three fail outright: she did not
find the front door from the catalog, did not open one card, and did not name Hits or the
wrong neighbour. She satisfies the fourth — *stops without loading the rest* — in the
emptiest way it can be satisfied. She stopped because she had nowhere to go, not because
the folder told her she was done.

### Her closing answers, verbatim

Recorded as supplied, including the shift into third person and the note-form phrasing.
Not tidied.

**Asked what she thought she was supposed to do next:**

> "tell me to do these things, looking for troubleshooting telling you what to do, will go
> back troubleshoot. tells you what to look at, how the maps run, what to correct, walk,
> run, tell everything, different dates to look at. The marks are not uniform, deliberate"

**Asked where she was unsure:**

> "the more time she read it, the more she understood, 3x to understand, at the end she
> didn't know where to go, looking at 'when the map and account disagree' and dated area"

### The plain statement

**`README.md` reads as a manual to be studied rather than a sign that points.** The routing
instruction did not register as an action. The door did not hand off.

**This is a failure of the map, not of the tester.**

### What the two answers show

**She was reading it, and reading it closely.** *"The marks are not uniform, deliberate"* is
a line lifted almost word for word out of `map/README.md`. She absorbed the content. She
read it three times by her own account, and reported understanding it better each pass.
What she never did was treat any of it as an instruction to go somewhere.

**She stopped at the end of the file, and the end of the file is not a door.** *"when the
map and account disagree"* and the *"dated area"* are the last two sections of
`map/README.md`. She read to the bottom and had nowhere to go. Both sections are about how
to think about the map — the account wins, every card carries a date. Neither says *now open
this*.

**The one rule is at the top and the reading order is in the middle, and she passed both.**
`map/README.md` opens with **read `catalog.md`, it sends you to ONE card, open that card,
stop**, and carries the four-step order further down. She went past both and kept reading to
the end. Being stated first was not enough to make it land as the thing to *do*.

**Her first answer describes a troubleshooting manual.** *"tells you what to look at, how
the maps run, what to correct."* The folder refuses to tell anybody what to correct
(`rules.md` §6) — and she came out expecting exactly that. She was waiting for instructions
the folder had already decided never to give, and nothing in the door told her that what she
was holding works differently.

### The prior exposure turned out not to matter

`5b48f88` recorded that she had opened `catalog.md` when the broken archive unpacked flat,
and stated that this run could no longer measure a cold first arrival at the front door.

**She never went back to it.** She failed earlier than the exposed material — she did not
reach the catalog at all this time. Having already opened it once did not pull her toward
it. That makes the exposure moot for this result, and it makes the finding worse rather than
better: the door failed to route a reader who had already seen where the route led.

### What this does not tell us

Nothing about whether the catalog routes, whether a card answers, or whether the collision
lines work. None of that was reached. **This run tested the first ten seconds of the folder
and stopped there.** Test C, on a fresh model, is still a live test of everything past the
door — and it reads the same README.

---

### 2026-08-22 — The fix to the door, after the failure was logged

**Order matters here and it is checkable.** The Test B failure was committed and pushed at
`b9ab925` before `map/README.md` was touched. This entry, and the commit carrying it, come
after. The git history is the proof that the map was not quietly repaired and the failure
written up around it.

**What changed.** `map/README.md` only. 904 words to 375. Nothing else in `map/` was edited.

**The defect that mattered most: the door gave two different first actions.** Line 11 said
read `catalog.md` now. Lines 35–40 said `identity.md` → `rules.md` → `catalog.md` → card,
and called the first two steps *"not optional."* A reader who takes the file seriously
resolves that by reading further rather than by acting, which is exactly what Nicole did —
three times through, by her own account, and she never left the file.

**How it was resolved: `identity.md` and `rules.md` are background, not a prerequisite.**
`map/README.md` was the only file in the folder claiming otherwise. `catalog.md`'s own
*How to use this page* teaches find-the-sentence → one card → stop. `map/examples.md`
teaches two hops. The root `README.md` teaches two hops. `TEST_METHOD.md`'s Test B bar asks
the reader to *find the front door from the catalog* and never requires the other two files
first. The outlier was corrected to match the rest.

**The reason behind "not optional" was real, and it was kept.** Without `rules.md` a reader
could read `VERIFY` as *this is broken* rather than *nobody confirmed this*. Rather than
require a whole file to learn one word, the door now defines `VERIFY` in one line — and
defines `object` beside it, because asked what object she would be touching, Nicole answered
**"folder."** The word had never been defined before she met it.

**The other four changes, each traceable to something she said or did:**

- **It opens with her situation, not with what the folder is.** Fifty-five words, then the
  first action. The root `README.md` and `catalog.md` both open this way and both work; the
  one door she actually received did not.
- **The instruction is a step, not a rule.** It was filed under *"The one rule"* and
  outnumbered three to one by prohibitions. She came away knowing what she must not do.
- **The model-facing section moved to the end.** It was section two of seven — a dead
  stretch twenty per cent in for a human reader.
- **It ends on an action.** The last line is now *"Now open `catalog.md`."* It previously
  ended on *"When the map and the account disagree"* and the dated section, which is the
  exact spot she named when asked where she got stuck. The disagree rule survives as one
  line beside the definitions, where it is about her behaviour in the account rather than a
  section about how to think.

**One thing added that was not on the list.** *"Nothing here tells you how to fix anything."*
Her answer described a troubleshooting manual — *"tells you what to look at, how the maps
run, what to correct."* The old door did say so, in section six, headed *"What is not in
here."* She read past it. It is now stated plainly, in the reader's own terms.

**What this fix is not.** It is untested. Nicole's run cannot be re-run — she is no longer a
stranger to this folder. Test C is a fresh model against this same file, and it is the only
remaining evidence about whether the door hands off. If it fails too, that ships as well.

`TEST_METHOD.md` is not edited. `identity.md` and `rules.md` are not edited.

---

## TEST C — pre-run — August 23, 2026

**Written before the session is opened.** Nothing has been run. Two calls are recorded here
so that neither can be made after seeing a result.

### Call 1 — the task is the frozen one

Test C uses `TEST_METHOD.md`'s own Test B task, verbatim:

> "Adam asked you to change the timing on the Fit Call nurture texts. Using only this
> folder: (1) find where to start, (2) tell me what object you'd be touching, (3) tell me
> what else moves if you change it, and (4) tell me the one thing you might grab by mistake.
> Then stop."

That is what the frozen file says — *"Same verbatim task as Test B"* — and it is the task
`TEST_METHOD.md` names for Test B, not the Attended task added on August 22 for Nicole.

**It is clean for a fresh model, and it was not clean for Nicole.** The root `README.md`
works this task end to end, all four parts. That file sits **outside** the drop-in folder,
so a model receiving only `map/` never sees it. Nicole's run had a different problem —
prior exposure from the broken archive — which does not transfer to a session with zero
memory.

**One exposure inside the folder, named now rather than after.** `map/examples.md` line 74,
inside the third walk, names `SH - Fit Call Nurture (Alt Days)` and says it is *"15 texts, 2
days apart, about four weeks end to end."* That walk is about `SH - Fit Call No Show`; the
nurture appears as a downstream consequence. A model that reads `examples.md` before the
catalog therefore meets part (2) of the task — what object — and one fact bearing on part
(3), without having routed there itself. The door marks `examples.md` **off the path**, but
it is in the folder and a model may open it. Parts (3) and (4) still require Lane B and the
card. If the transcript shows the object arriving from `examples.md` rather than from the
catalog, that is this, and it was known in advance.

### Call 2 — Test C runs on the repaired door, and the frozen order was broken to repair it

`TEST_METHOD.md` says:

> **## Order of runs**
> Test A first (fix accuracy) then freeze cards then Test B and Test C on the frozen
> version. **No edits between B and C.**

**That rule was broken.** Test B ran and failed on August 22 (`b9ab925`). `map/README.md`
was rewritten afterwards (`b45b8cc`), 904 words to 375. Test C will read the rewritten door.

**Why, stated plainly.** The frozen order assumed Test B would pass. It did not — the door
failed to hand off at all, and the reader never reached the catalog. Running Test C against
a door already known to be broken would have produced a failure that was predictable before
the session opened. That is not evidence; it is a re-enactment. The repair was made so that
Test C could test something still unknown.

**What that costs, not smoothed over.** Test B and Test C are no longer runs against one
frozen artifact, and they cannot be reported as though they were. Test B is a result about
the old door. Test C will be a result about the new one. Nothing composes them into a single
claim about one version of this folder, and no claim of that shape should be made from them.

**What remains true.** `TEST_METHOD.md` is not edited — not to permit this, not to
soften it, not at all. It still says *no edits between B and C*, and the history still shows
an edit between B and C. The rule and its breach are both on the record, in that order, with
dates.

### The bar Test C is measured against

From the frozen file, unchanged:

> **Pass (all four, from the brief's bar):** finds the front door from the catalog; opens
> ONE card and understands the object; names Hits + the obvious wrong neighbor; stops
> without loading the rest.

Plus Test C's own additional condition:

> **Pass:** Same four-part bar as Test B, PLUS: the model does not request or load the full
> objects folder.

**Five conditions. The fifth is the one this folder was built to earn.** `map/README.md`
carries a section addressed to a model telling it not to glob `objects/`, and `rules.md` §5
aims a paragraph at exactly the reasoning a model would use to justify it. Whether that
holds is what has never been tested.

### Who runs it

A brand-new Claude session with no memory of Safe Harbor, receiving only the drop-in folder.
**Not the assistant that wrote this map.** That assistant authored `map/README.md`,
`map/examples.md` and the card set, and knows the answer to the task — it cannot be the
reader, and it does not run this test.

### Logged, whatever happens

Full transcript, kept as-is. If it fails, it ships. `TEST_METHOD.md` is not edited.
