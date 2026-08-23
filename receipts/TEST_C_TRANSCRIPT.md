# TEST C — Transcript
**Comp #11 · The Cartographer · Safe Harbor GHL Map**

**Date of run:** August 23, 2026
**Reader:** A fresh Claude session opened in an Incognito window. No memory of Safe Harbor,
no prior context on this account, this map, or this competition. Not the assistant that
wrote the folder.
**What it received:** `cartographer-map-for-nicole.zip` — 37,190 bytes, uploaded whole.
Fourteen files under a single `map/` folder. No `receipts/`, no `TEST_METHOD.md`, no root
`README.md`, nothing from outside the drop-in folder.
**Rules of the run:** No help, no hints, no corrections, no follow-up prompts. Any question
the model asked was left unanswered and stays in the transcript.

---

## The task, given verbatim and nothing else

> Adam asked you to change the timing on the Fit Call nurture texts. Using only this folder:
> (1) find where to start, (2) tell me what object you'd be touching, (3) tell me what else
> moves if you change it, and (4) tell me the one thing you might grab by mistake. Then stop.

This is the task frozen in `TEST_METHOD.md` on August 17, 2026, before any run.

---

## What this run is measured against

Five conditions — the four-part bar Test C inherits from Test B, plus its own fifth:

1. Finds the front door from the catalog
2. Opens ONE card and understands the object
3. Names Hits + the obvious wrong neighbour
4. Stops without loading the rest
5. **Does not request or load the full `objects/` folder**

---

## Two things recorded before this run, not after

Both are logged in full at `314788b` in `TEST_A_CORRECTIONS.md`, committed before this
session was opened.

**This run reads a repaired door.** `TEST_METHOD.md` says *no edits between B and C*. That
rule was broken: Test B failed on August 22 (`b9ab925`) and `map/README.md` was rewritten
afterwards (`b45b8cc`). Test B is a result about the old door; this is a result about the
new one. They do not compose into a single claim about one version of this folder.

**One exposure was known in advance.** `map/examples.md` line 74 names
`SH - Fit Call Nurture (Alt Days)` and gives its length, inside a walk about a different
object. If the object name appears in this transcript before `catalog.md` is opened, that
is where it came from.

---

## Transcript

*Verbatim, unedited, stumbles left in. Nothing removed.*

<!-- PASTE THE RAW TRANSCRIPT BELOW THIS LINE -->


## Answer first

**Start:** `catalog.md` → Lane B → `objects/sh-fit-call-nurture-alt-days.md` → stop.

**Object you'd touch:** the workflow `SH - Fit Call Nurture (Alt Days)` at Automation → Workflows. Mark: LIVE (checked Aug 21, 2026).

One honesty note: `catalog.md` was in the upload list but its contents didn't render for me. The card itself says "Came here from Lane B of `catalog.md`," so I'm trusting that line for hop one. You may want to confirm the lane yourself.

---

## 1. Where to start

1. Open `catalog.md`, find Lane B ("the nurture texts").
2. Open the one card it names: `objects/sh-fit-call-nurture-alt-days.md`.
3. Stop reading the folder. Open the workflow in the account.

---

## 2. What you'd be touching

`SH - Fit Call Nurture (Alt Days)` — a workflow that fires on the tag `fit call nurture` and sends 15 SMS, 2 days apart, each carrying the `safe-harbor-fit-call` booking link. Timing = the wait steps inside it.

---

## 3. What else moves if you change the timing

| Moves | Why |
|---|---|
| **The name goes stale** | "Alt Days" describes 2-day spacing. The name doesn't update itself. |
| **Total length stretches** | 15 messages. Wider gaps push it past ~4 weeks; the last message is written as a last message and lands wherever the math puts it. |
| **The stop doesn't move** | `SH - Fit Call Booked` and `SH - Fit Call Attended` are what pull a contact out. They're not on screen and editing the nurture doesn't change them. |
| **Re-entry doesn't move** | `SH - Fit Call No Show` re-adds the tag after 2 days if nobody re-booked, restarting this sequence from message one. |

**Still unconfirmed (VERIFY):** `SH - Fit Call Nurture Trigger (24hr Check)` is published, nobody has opened it, and whether it touches this sequence settles only by opening it in the account.

---

## 4. The one thing you might grab by mistake

**`SH - Fit Call Nurture Trigger (24hr Check)`** — identical to the right name for 22 characters. Searching `SH - Fit Call Nurture` returns both. The only difference is what's inside the bracket at the end. Read the name to the end before you edit.

(Don't search just `nurture` either — five things come back.)

**Stop. Go open `Automation → Workflows → "SH - Fit Call Nurture (Alt Days)"` and read the wait steps there.** If the account disagrees with any of the above, the account is right.
