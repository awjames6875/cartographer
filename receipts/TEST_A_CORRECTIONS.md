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
reader. Tiffany walks it next, cold, with no author's memory to fall back on.

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
drop-in folder, where it would travel to Tiffany with everything else.

---

### 2026-08-22 — Test B, a second task added

**`TEST_METHOD.md` is not edited.** It was locked on August 17, 2026, before any run, and
Test A ran against it on August 19. Editing it now would break the single claim this comp
was built to make. What follows is an **addition**, logged here with its date. The frozen
file stands exactly as written, and its Test B task stands with it.

**Why a second task.** The frozen Test B task is the Fit Call nurture task. That task is
now worked end to end in `README.md` at the repository root — all four parts of the bar,
including the object, what moves with it, and the wrong-neighbour grab. That README sits
**outside** the drop-in folder, so the frozen task survives as long as Tiffany receives the
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
So this task does not measure whether Tiffany derives that pattern cold. It measures whether
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
path as a literal filename. Tiffany opened it and got **14 flat files** called
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

**What it cost the run, stated rather than waved off.** The flat listing showed Tiffany all
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

## TEST B — Tiffany — August 22, 2026

# The door did not hand off. The map failed.

**Logged before any edit to `README.md`.** No fix is in this commit. `TEST_METHOD.md` says a
failed run ships anyway and the fix gets logged after; this is the run shipping first.

**Tester:** Tiffany. A genuine domain outsider — never inside Safe Harbor's GoHighLevel.
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
resolves that by reading further rather than by acting, which is exactly what Tiffany did —
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
defines `object` beside it, because asked what object she would be touching, Tiffany answered
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

**What this fix is not.** It is untested. Tiffany's run cannot be re-run — she is no longer a
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
`TEST_METHOD.md` names for Test B, not the Attended task added on August 22 for Tiffany.

**It is clean for a fresh model, and it was not clean for Tiffany.** The root `README.md`
works this task end to end, all four parts. That file sits **outside** the drop-in folder,
so a model receiving only `map/` never sees it. Tiffany's run had a different problem —
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

---

### 2026-08-23 — The shipped archive and the repository have diverged

**This entry records a divergence and does not explain it.** Authorship and timing are
unknown. Nothing below asserts a sequence.

#### What is known, and checkable

**The repository's door and the shipped door are not the same file.**

| | `map/README.md` in git | `map/README.md` inside the zip |
|---|---|---|
| Size | 2,077 bytes | 2,481 bytes |
| Contains the paragraph below | no | yes |

- `map/README.md` on disk is byte-identical to `HEAD` — hash `63d29ee`, `git status` clean.
  Its mtime is **Aug 22, 23:57:33**.
- The last commit touching it is **`b45b8cc`, Aug 22 23:58** — the Test B repair.
- `cartographer-map-for-nicole.zip` has mtime **Aug 23, 00:48:59** and is **37,367 bytes**.
  The archive built from this repo at 23:58 was **37,190 bytes**. The shipped file is not
  the archive this repo produced.

**The text present in the archive and absent from the repository:**

> **If `catalog.md` is listed in your uploads but its contents are not visible to you, read
> it from disk before doing anything else.** You have a file tool. "Didn't render" is not
> "unavailable." Do not reconstruct the route from a card, a filename, or memory — the front
> door is the route, and a card saying "Came here from Lane B" is a receipt of a route
> already taken, not a substitute for taking it.

It is aimed precisely at what the Test C run 1 transcript describes.

#### What was searched for, and what came back

- `git log --all -S` for the paragraph across every branch: **no commit, ever.**
- Every Claude Code session log for this repository: **no match** outside this session's own
  transcript, which contains it only because the divergence was diffed here.
- Every Claude Code session log for **every** project on this machine: **no match.**
- Session logs modified between 00:00 and 01:30 on Aug 23: **only this session.**
- The repository working tree: **no match.**

#### What is not known

- **Who wrote it.** No log this session can read attributes it to anyone.
- **When it was written.** The archive's mtime records when the archive was last written,
  not when the text was composed.
- **Whether it was present when Test C run 1 executed.** The run happened on Aug 23 and the
  archive was last written at 00:48:59 on Aug 23. Nothing available here orders those two
  events.
- **Therefore whether run 1's model read this paragraph and disregarded it, or never saw it
  at all.** Both remain open. The transcript's *"didn't render for me"* is consistent with
  either.

**Absence from the logs is not proof of absence.** A session whose log had not flushed, a
tool that does not log, an edit made on another device and synced — `C:\Users\1alph\Documents`
is OneDrive-synced — would each leave exactly this evidence. The hypothesis that a second
Claude Code session wrote it is **not supported** by any log readable from here, and is **not
ruled out** by that.

#### Why this is logged rather than fixed first

The archive that was handed to a tester is not the artifact under version control. Any claim
this project makes about what a reader received depends on those being the same file, and for
some window they were not. That is a finding about the process, and it is recorded before the
two are reconciled, because reconciling them destroys the evidence that they differed.

`TEST_METHOD.md` is not edited.

---

### 2026-08-23 — The unattributed paragraph is adopted into the map

**It is now in `map/README.md` and in git.** It was not before. What follows is what is
known about where it came from, which is not much.

**Four things nobody knows:**

1. **Who wrote it.** No commit on any branch contains it before today. No Claude Code
   session log on this machine — for this repository or any other — contains it. The only
   session log written in the window around the archive's mtime is the one that found the
   divergence.
2. **When it was written.** The archive's mtime records when the archive was last written,
   not when the text was composed.
3. **Whether it was in the folder Test C run 1 received.** The run was on August 23. The
   archive was last written at 00:48:59 on August 23. Nothing available here orders those
   two events.
4. **Whether run 1's model read it and disregarded it, or never saw it.** That transcript
   says *"`catalog.md` was in the upload list but its contents didn't render for me"* and
   then reconstructs the route from a line inside a card. Both readings fit. No sequence is
   asserted here.

**It reached a tester without passing through git.** It was found inside
`cartographer-map-for-nicole.zip`, which had been rebuilt after the archive this repository
produced. This project's claim is that nothing enters the map unlogged. For some window,
something did.

**Why it was adopted rather than discarded.** The paragraph is correct and it names the
precise failure run 1 exhibited: a model that treats *"didn't render"* as *"unavailable"*
and reconstructs the route from a card instead of taking it. Discarding it on provenance
grounds would have left a known failure unfixed for a bookkeeping reason. Adopting it puts
the uncomfortable provenance in this file instead, which is what this file is for.

It was adopted **byte-exactly from the shipped copy**, not retyped, so the map now contains
what was actually handed over. `receipts/shipped-readme-aug23-0048.md` is kept as the record
that the two ever differed.

Applied as seven added lines to `map/README.md` and nothing else — verified by diff against
`HEAD` before committing.

---

### 2026-08-23 — Archive SHA-256 is recorded from now on

**The rule, going forward: every run logs the SHA-256 of the archive it ran against, in the
pre-run entry, before the session opens.**

A hash comparison between the archive and a build from `HEAD` would have caught this
divergence the moment it happened, instead of two days later and only because a stray
paragraph was noticed in a diff. Byte counts and mtimes were what surfaced it; a hash is
what would have prevented it.

Any run whose pre-run entry carries no archive hash is a run whose artifact cannot be
proven. That applies to Test B and to Test C run 1, both of which were conducted without
one, and neither of which can now be reconstructed with certainty.

---

### 2026-08-23 — TEST C run 2, pre-run

**Written before the session is opened. Nothing has been run.**

**The archive, hashed before the run:**

```
SHA-256  f2326c7659c88b78039860ff2e57ce1326540706d00abfaca70d869d29221ca4
file     cartographer-map-for-nicole.zip
size     37,383 bytes
built    2026-08-23 01:28:50
```

Built from a working tree verified clean against `HEAD` immediately beforehand. The archive's
copy of `map/README.md` is byte-identical to the repository's. 14 files, zero backslash
paths, no `receipts/`, no `TEST_METHOD.md`, no root `README.md`.

**This is the first run in this project whose artifact can be proven.** Test B and Test C
run 1 were both conducted without a hash, and neither can now be reconstructed with
certainty.

**What run 2 is, and what it is not.** It reads a door that differs from run 1's repository
version by one adopted paragraph, and that may or may not differ from what run 1 actually
received — see the divergence entry above; the ordering is unknown. **Run 2 therefore cannot
confirm or deny run 1's condition 1.** It is a test of a modified door, and it stands as its
own result. Both runs ship.

**Task:** unchanged, the frozen nurture task from `TEST_METHOD.md`.

**Bar:** unchanged, the four-part bar plus Test C's fifth condition — the model does not
request or load the full `objects/` folder.

**What run 2 additionally tests, which run 1 could not.** Run 1 reported that `catalog.md`
did not render and reconstructed hop one from a card. The adopted paragraph addresses exactly
that. Whether the front door loads at all — it is 26,939 bytes, three times the next largest
file in the folder — is still unestablished, and remains the single most consequential open
question about this artifact. Neither stranger run has yet confirmed the catalog routes
anybody.

**Reader:** a fresh session with no memory of Safe Harbor. Not the assistant that wrote this
map.

---

### 2026-08-23 — Four defects found by external review, after Test B

**None of these was found by the builder, and none was found by a test run.** They came
from an outside reading of the folder after Test B failed. All four were verified against
the files before being changed, and all four were real.

#### 1. The Test B defect was alive in the catalog

`catalog.md` line 5 read:

> Read `identity.md` and `rules.md` first if you have not.

**This is the same defect that failed Test B**, and it survived the repair because the repair
only touched `map/README.md`. It was worse here than in the door: it sat at line 5, *above*
the reading rule, phrased as a precondition — so a reader who reached the front door was
told to leave it again before starting.

Rewritten to match the repaired door: `identity.md` and `rules.md` are background, not a
step, and not needed to start.

**The lesson is about the repair, not the line.** Fixing the door and not searching for the
same sentence elsewhere is how a fixed defect stays shipped. It was one grep.

#### 2. Two cards contradicted each other on one fact

- `objects/safe-harbor-consultation-lead-flow-vo2.md` stated a VAPI **"Create a Call"**
  action places the outbound call, marked *settled: Sadie, August 19, 2026*.
- `objects/maria.md` said the same step was **reported two ways** — a native VAPI action, or
  a custom webhook to the VAPI API — and carried an open `VERIFY` on which.

One card asserted as settled what the other flagged as unconfirmed. A reader opening Vo2
alone would have taken it as fact, which is what `rules.md` §2 exists to prevent: *"a line
that could not be confirmed and carries no VERIFY is fiction."*

Vo2 now says a step places an outbound call through VAPI — which is settled — and carries
the same `VERIFY` about **what kind of step**, in the same words as `maria.md`.

**Cross-card contradictions are invisible to the reading rule.** One card at a time is what
makes this folder safe, and it is also what let two cards disagree for four days.

#### 3. `collisions.md` row 4 was in the wrong category

Row 4 pairs `fit call booked` with `Appointment Booked` — **two different names**, both tags.
It was listed under *"Same name, two objects"* alongside rows 3 and 12, which pair one name
across a workflow and a tag.

Row 4 is a different thing: the two collide because they are **related** — one is read where
the other is written — not because they share a name. The section is now *"Same name, two
objects — twice"*, and row 4 is named in it as explicitly not that pattern.

#### 4. Card-less lanes read as dead ends

Some lanes answer a reader outright and name no card — Lane F, Lane I, and the entries under
**Named, and nothing flowing through**. Nothing said that was a completed walk, so a reader
who landed on one had reason to think they had failed to find the card.

One sentence added in both places the reading rule is stated — `catalog.md` and
`map/README.md`: some lanes answer you and name no card, and that is a finished walk, not a
dead end.

#### What this round says about the testing

Test A was an accuracy check by an insider. Test B and Test C were stranger runs, and both
stopped early — one at the door, one at a file that would not render. **None of them would
have caught any of these four.** Two require reading two cards side by side, which the folder
forbids. One is a categorisation error inside an off-path reference page. One is an absence.

An outside reader found in a single pass what three runs did not. That is worth recording
next to the runs rather than underneath them.

`TEST_METHOD.md` is not edited. `identity.md` and `rules.md` are not edited.

---

### 2026-08-23 — Archive rebuilt after the external-review fixes

The archive built at `01:28:50` (SHA `f2326c76…`) is **superseded**. It predates the four
external-review fixes and must not be used for any run.

```
SHA-256  ee259c46a1f5cee75cef7dac1e810ff7d195fcabb419c2268a46f22d0a3fd0ee
file     cartographer-map-for-nicole.zip
size     37,800 bytes
built    2026-08-23 21:00:35
```

Built from a working tree verified clean against `HEAD` immediately beforehand. 14 files,
zero backslash paths, no `receipts/`, no `TEST_METHOD.md`, no root `README.md`.

**Any run from here logs this hash, or the run cannot say what it read.**

---

## TEST B — transcript committed — August 24, 2026

`receipts/TEST_B_TRANSCRIPT.md`, 646 lines, added by hand from a Descript recording,
auto-transcribed. Task given: the **Attended** task, the second Test B task added Aug 22 and
logged before the run.

### How it was trimmed

Off-topic personal conversation before and after the task was removed for the tester's
privacy. **No part of the walk itself was cut.** Transcription artifacts are left in,
including the auto-transcriber's occasional substitution of non-English words. The
transcript's own header states this.

### Consent

**Tiffany consented, before the run, to her words and her first name being published on a
public page for the judges.** She was told what the recording was for and what would be done
with it, and she agreed on that basis. The consent predates the walk; nothing was published
retroactively on an assumption.

**What is published:** her first name, and her words from the walk.

**What is not:** her surname appears nowhere in this repository. The full name in
`TEST_METHOD.md` — "Nicole Myrick" — belongs to the misnaming corrected on August 24 and is
not hers. The off-topic personal conversation before and after the task was cut for her
privacy, and the untrimmed recording is not published.

**The consent covers publication, not the findings.** She agreed to be quoted. She was not
asked to endorse any conclusion drawn from the run, and none is attributed to her.

### Finding 1 — the tester could not open `.md` files at all

**Option 1: no default application for `.md` on the tester's Mac.**

From the untrimmed original, timestamps 2:48–3:14 — **cut during trimming, so these quotes
are not in the committed transcript**, which is why they are preserved here:

> **Tester (2:48):** "Do you see that? There is no application set to open the README file"
>
> **Tester (3:01):** "No, I just clicked it to open it. See, so when it says read me, right?
> I double-click, and this is what comes up. There is no application set to open the document
> readme.md"
>
> **Builder (3:00):** "Can't you right-click it or something?"

**The builder's only involvement at this point was suggesting a right-click to open a file.**
Not task help.

**What this reframes.** Every instruction in this folder assumes a file opens when you click
it. For this reader, opening any file was a problem to solve before reading could begin — and
the reading rule asks her to open a second one. *"Open the ONE card it names"* is not one
action on a machine with no `.md` handler.

### Finding 2 — she read the folder as separate, sequential assignments

> "were, but I was thinking we were going to do that one. So this is me, right? We're gonna
> do that one. Once we finished that, then you would have me close it and then go to another
> one."
>
> "I didn't think that they were all related"

She took the files as a queue of unrelated tasks rather than one path with a next step.

### Finding 3 — she never reached `catalog.md` or any card

She named the catalog correctly and repeatedly, from the README's text — *"the first rule is
to read the catalog"* — and never opened it. At one point she says *"So this is the catalog, I
guess,"* looking at the README's description of it. She answered *"the folder"* when asked
what object she would be touching, and held that answer.

### A correction to what was logged at `b9ab925`

That entry says: *"She read `map/README.md` and nothing else. She opened no other file."*
**The transcript does not confirm that, in either direction.**

Nearly everything she quotes is traceable to `map/README.md`, including its one-line
descriptions of the other files — which is why *"three examples start to finish,"* *"four
things it refuses to do"* and *"lookalike for your object"* appear in her speech without her
having opened `examples.md`, `identity.md` or `collisions.md`. But the builder says *"you
don't have to just stay in identity,"* which reads as him seeing `identity.md` on her screen.

The claim is downgraded from *established* to *unconfirmed*. It is consistent with
README-only and is not proven by this tape.

### The tape evidences the contradiction defect directly

The four external-review fixes and the README rewrite were diagnosed after this run. Her own
words, reading the **pre-repair** door, are the evidence:

> "So it says here, i-- Steps one and two are short and they're optional if you are about to
> change something."
>
> "So it's telling me the identity, the rules, the catalog, and it names one card. So the
> catalog is front door, right? **Steps one to two are short but they have to be done. It's
> mandatory 'cause they're not optional, right?**"

She hit lines 11 and 35–40 of the old `map/README.md`, read them against each other, and
resolved the contradiction by concluding `identity.md` and `rules.md` were mandatory first.
That is the defect, on tape, in the reader's own voice. The diagnosis was not reconstructed
after the fact.

### Builder involvement — recorded as the tape shows it, not as summarised

**This was requested as: the builder confirmed answers she reached herself, gave encouragement
per the pre-written method, one nudge logged, no answer supplied. The transcript does not
support that, and it is recorded here as it reads.**

`TEST_METHOD.md`'s frozen Test B rule is **"No help from Adam."** That rule was not observed.

**Confirmation of her own answers** — this part is accurate. She said *"Well, the read the
catalog, no?"* and the builder said *"That's it."* Later: *"You got it. Read the catalog."*
She reached it; he confirmed.

**But direction was also supplied, unprompted:**

- "You're in the right place. **Start with the README file.**" — before she had found anything
- "you wanna start with the README file, but you have access to all the files"
- "You start with the README, which gives you everything"
- "**You can open anything in that folder.** Remember" · "There's other things you can open" ·
  "Anything in those folders. That folder I gave you, you have access to everything, anything"
- "you don't have to just stay in identity"
- "**Do you see the word object anywhere?** What does that say? It's a common word"
- "There are some examples in there"
- "See something you're gonna change that has to do with the cards"
- "You have to open a file" — the nudge that was acknowledged
- Negative signals on wrong answers: "Come on" · "Wrong answer"
- The task was re-read aloud to her roughly six times

**What the builder did withhold**, in his own words on the tape:

> "I would've been guiding you to do that, and **I would've been cheating.** But my README
> should've been so good that if I would've said, 'Hey, what's the first thing you do?' We
> would've said go to catalog. I could've wrote, 'Hey, get out of here and go to the catalog
> right now. Click out.' I could've said that. 'Now go to the catalog.' … I didn't do"

So the specific route was withheld. Orientation, permission, pointers and pass/fail signals
were not. **"No help from Adam" and what is on this tape are not the same thing**, and the
transcript is the record, not the summary.

**Why this is logged rather than smoothed.** The run's finding — that the door did not hand
off — is *strengthened*, not weakened, by this. She failed to reach the catalog **while being
told to start at the README, told she could open anything, told there were examples, told she
need not stay in identity, and having her correct answer confirmed twice.** A door that does
not hand off under that much assistance is a worse door than one that fails a reader in
silence. Recording the help makes the finding harder to dismiss, not easier.

`TEST_METHOD.md` is not edited.

---

### 2026-08-24 — The Test B tester was misnamed in earlier receipts

**The tester was Tiffany. Earlier entries called her Nicole.** The name was wrong from the
start — it originates in `TEST_METHOD.md` on August 17, 2026, a week before it was caught, and
propagated from there into every entry that referred to her.

**Caught on August 24, 2026**, by Adam, on review. Not by any test run, and not by anything in
the folder.

**What is unaffected.** Every run, every finding, every quote and every verdict. The person who
walked Test B is the same person; only the label was wrong. No result changes, none is
withdrawn, and no dated finding is revised.

#### Corrected — 19 occurrences across 6 files

- `map/catalog.md`, `map/objects/sh-fit-call-nurture-alt-days.md`,
  `map/reference/collisions.md` — one each, the same `VERIFY` line: *which name Tiffany opens
  first*. These are inside the drop-in folder, so the archive changes and carries a new hash.
- `receipts/TEST_A_CORRECTIONS.md` — 14 occurrences across the pre-run entries, the Test B
  failure entry, and the repair entries.
- `receipts/_Account Walk with Sadie.md` — one, a working heading in the Aug 19 walk record.
- `tasks/todo.md` — one. Gitignored, so it does not appear in any commit.

#### Deliberately not corrected

**`TEST_METHOD.md:27` still reads "Nicole Myrick."** The file has been unedited since August
17, before any run, and four entries in this log assert that. Editing it now to fix a name
would trade the project's central claim — that the method predates the runs and was never
touched — for a cosmetic correction. **The freeze is worth more than the name.** The frozen
file names the tester wrongly, that is stated here, and anyone reading the method alongside
this log has both facts.

**Historical references to `cartographer-map-for-nicole.zip` are also preserved**, in every
entry that names it. That archive existed under that filename, its SHA-256 was computed
against that file, and the divergence entry of August 23 turns on byte counts recorded for it.
Renaming it inside past entries would falsify an evidence chain to tidy a label. The old
filename is a fact about a file, not a claim about a person.

The distinction held throughout: the person's name is capitalised in every occurrence, the
filename is lowercase in every occurrence. Only the capitalised form was replaced.

#### The archive was renamed

`cartographer-map-for-nicole.zip` is removed. The current archive is
`cartographer-map-for-tiffany.zip`, rebuilt from `HEAD` and hashed in the entry below.

---

### 2026-08-24 — Archive renamed and rebuilt

```
SHA-256  f86678b86cc4c5b3a47310f2f4ac682c71fe1c8f67b4a16a0cf2d55c6fa0eae2
file     cartographer-map-for-tiffany.zip
size     37,800 bytes
built    2026-08-24 00:31:53
```

Built from a working tree verified clean against `HEAD` **after** the name corrections were
committed, so the hash corresponds to a known commit rather than to a working copy. 14 files,
zero backslash paths, no `receipts/`, no `TEST_METHOD.md`, no root `README.md`. Three
occurrences of `Tiffany` inside the archive and zero of `Nicole`, checked by extracting the
three files from the finished archive.

**Superseded, and not to be used for any run:**

- `cartographer-map-for-nicole.zip` · SHA `ee259c46…` · built Aug 23 21:00:35 — correct
  content, wrong filename and wrong tester name inside.
- `cartographer-map-for-nicole.zip` · SHA `f2326c76…` · built Aug 23 01:28:50 — predates the
  four external-review fixes.

Both are removed from disk. Their hashes stay on this page because a superseded artifact that
was hashed is still a record of what existed.

**A note on the order of operations.** The archive was first rebuilt while the name
corrections were still uncommitted, then discarded and rebuilt again after the commit. The
hash above is the second build. An archive hashed against an uncommitted working tree cannot
be tied to a commit, which defeats the purpose of recording the hash at all.


---

### 2026-08-24 — TEST C run 2, pre-run

**Written before the project is created and before any session is opened. Nothing has been
run.**

**This entry supersedes the run 2 pre-run entry of August 23.** That entry hashed
`cartographer-map-for-nicole.zip` (SHA `f2326c76…`), which predates the four external-review
fixes and has been removed from disk. **No run was ever conducted against it.** The task and
the bar below are unchanged from that entry; the artifact and the environment are what change.

**The archive, hashed before the run:**

```
SHA-256  f86678b86cc4c5b3a47310f2f4ac682c71fe1c8f67b4a16a0cf2d55c6fa0eae2
file     cartographer-map-for-tiffany.zip
size     37,800 bytes
built    2026-08-24 00:31:53
```

**What was checked against this archive rather than assumed.** Its `map/` tree was extracted
and diffed against the repository's `map/` — byte-identical, no differences. 14 files plus 3
directory entries. Zero backslash paths. No `receipts/`, no `TEST_METHOD.md`, no root
`README.md`, no `map/CLAUDE.md`. Three occurrences of `Tiffany`, zero of `Nicole`.

**It corresponds to a commit, not to a working copy.** The archive was built at 00:31:53,
thirteen seconds after `2bf88f5` carried the name corrections. Every commit since —
`a6f9e5e`, `fd2f164` — touched `receipts/` only, and `git diff HEAD -- map/` is empty. The
`map/` inside this archive is `HEAD`'s `map/`.

**Task:** unchanged, the frozen nurture task from `TEST_METHOD.md`.

> Adam asked you to change the timing on the Fit Call nurture texts. Using only this folder:
> (1) find where to start, (2) tell me what object you'd be touching, (3) tell me what else
> moves if you change it, and (4) tell me the one thing you might grab by mistake. Then stop.

**Bar:** unchanged — the four-part bar Test C inherits from Test B, plus Test C's own fifth
condition.

1. Finds the front door from the catalog
2. Opens ONE card and understands the object
3. Names Hits + the obvious wrong neighbour
4. Stops without loading the rest
5. **Does not request or load the full `objects/` folder**

#### Run 2 runs in a new Claude Project, not a chat upload

Run 1 was a zip uploaded into a chat window. Run 2 will be a **new Claude Project** with
`map/` added as project knowledge. Three reasons, stated before the run so the change cannot
be presented afterwards as a result.

1. **The brief specifies a Claude project.** Test C in `TEST_METHOD.md` is "a brand-new Claude
   project/session," and the root `README.md`'s Setup section tells a reader to drop `map/`
   into a Claude project. Run 1 never tested the delivery mechanism this map ships with.
2. **It makes per-file reads visible.** Condition 5 asks whether the reader loads the full
   `objects/` folder. Run 1 cannot answer that: the whole archive arrived at once and the
   transcript records no file-by-file reads. In a project, which files get opened is
   observable, so condition 5 stops being an inference.
3. **Run 1's chat upload failed to render `catalog.md`.** The front door — 27,320 bytes, three
   times the next largest file in the folder — was listed in the uploads and its contents were
   not visible to the reader, which is why run 1 reconstructed hop one from a card instead.
   Whether the catalog loads and routes anybody is still the single most consequential open
   question about this artifact, and no stranger run has yet confirmed that it does.

**What the change costs, recorded now rather than after.** Run 2 is **not** a clean
replication of run 1. It reads a different door — one adopted paragraph plus the
card-less-lanes sentence — in a different environment. **It therefore cannot confirm or deny
run 1's condition 1**, and the two runs do not compose into a single claim about one version
of this folder. Both ship, as separate results.

#### Run 1 is superseded, and could not be proven

Run 1 ran on August 23 against `cartographer-map-for-nicole.zip` at **37,190 bytes** — a size
matching neither hashed archive (`f2326c76…` at 37,383 bytes, `ee259c46…` at 37,800). It was
conducted before the hash rule existed, so **what run 1 actually read cannot now be
reconstructed with certainty.** Its transcript stays in `receipts/` and its observations
stand, but it is not an artifact this project can prove.

That transcript also carries no verbatim session record: the paste marker is still in the file
with only the reader's final answer beneath it, and `TEST_METHOD.md` asks for the full
transcript kept as-is. **Run 2 logs the session verbatim, whatever it shows.**

**Reader:** a fresh Claude project with no memory of Safe Harbor. Not the assistant that wrote
this map.

**Rules of the run:** no help, no hints, no corrections, no follow-up prompts. Any question
the reader asks out loud is left unanswered and stays in the transcript.

#### The first message, verbatim

The session opens with this and nothing else — no preamble, no framing, no follow-up:

```
Read `catalog.md` first, then open the one card it names.

Adam asked you to change the timing on the Fit Call nurture texts. Using only this folder:
(1) find where to start, (2) tell me what object you'd be touching, (3) tell me what else
moves if you change it, and (4) tell me the one thing you might grab by mistake. Then stop.
```

The first line is the setup line the root `README.md` prescribes, and `TEST_METHOD.md`
sanctions it: Test C receives the drop-in folder *"per the README's own instructions (catalog
first, one card - if the README makes the model load everything, the README fails)."* The
second paragraph is the frozen task, unaltered.

**What this narrows, stated before the run and not after.** The routing instruction is *in*
the first message. **Condition 1 therefore tests whether the model follows the routing
instruction — not whether it discovers the route unaided.** A pass means the model was told to
open the front door, opened it, and let the catalog route it to one card. It does not mean the
catalog is self-evident to a reader who arrives without that sentence.

This is the frozen method's design rather than a concession to it. `TEST_METHOD.md` hands
Test C the folder with the instruction attached, and the root `README.md`'s Setup section tells
every real reader to say the same sentence to a model. So the run measures the thing this map
actually ships with. **What no run has tested, and what this one will not test either, is a
model arriving at this folder with no routing sentence at all.** That stays open, and nothing
here should be read as having closed it.

**What condition 1 does still settle, which is the consequential part.** Whether `catalog.md`
loads at all — 27,320 bytes, three times the next largest file in the folder — and whether
Lane B resolves to exactly one card. Run 1 answered neither: the file was listed in its
uploads and did not render, so hop one was reconstructed from a card. **Being told to open the
front door does not make it open.** That is the question this run exists to answer.

**One more reason the two stranger runs do not compose.** Condition 1 does not mean the same
thing in Test B and Test C. Test C's reader is handed the route in its first message; Test B's
was not, and what she was handed instead is on the tape and logged above. Beyond the different
door and the different environment already recorded, the two runs are not scored against the
same condition 1, and no combined claim about "the stranger runs" should be built on them.

**Logged, whatever happens.** A pass and a failure both ship. Test B failed and shipped; so
does this.
