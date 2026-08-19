# SH - Fit Call Attended

**Type:**   workflow
**Mark:**   VERIFY — not confirmed · settles by: the workflow list in the account · **Checked:** not yet (drawn August 18, 2026)
**Where:**  Automation → Workflows → "SH - Fit Call Attended"
**Source:** the workflow of that name, opened from the account. Cited, not copied — open the real thing and read it there (`rules.md` §4).

Came here from Lane E of `catalog.md`. Read this card, then open the account. Do not open a second card (`rules.md` §5).

---

**The type on this card is an inference, not a finding**

`SH - ` is the prefix carried by the three workflows walked so far, and by neither tag walked so far — `Fit Call Booked` and `Appointment Booked` carry no prefix. That pattern is where **workflow** on the line above came from.

A pattern across three names is not a finding about a fourth. If this name turns out to sit on a tag, an appointment status, or something else, the type line is what was wrong, and it gets corrected against the account (`rules.md` §4).

`VERIFY — that this name sits on a workflow rather than a tag or an appointment status · settles by: the workflow list in the account`

---

**The mark is not yet earned**

- **LIVE** would need: found in the workflow list · showing as published · at least one way in that can still fire.
- **LEFTOVER** would need: found in the list, and no way in survives.

Nobody has opened the list. Until somebody does, this card makes no claim either way.

---

**Hits**

Nothing below is a claim about what moves. Each line is the question that has to be answered, standing where its answer will go.

- `VERIFY — what fires this workflow, and what marks a contact as attended in the first place · settles by: the trigger step at the top of the workflow`
- `VERIFY — whether attended is set by the calendar's appointment status or by a person changing it by hand · settles by: the trigger step in the account`
- `VERIFY — which tag it applies, and which it removes · settles by: the workflow in the account`
- `VERIFY — whether it stops SH - Fit Call Nurture (Alt Days) for that contact · settles by: both workflows in the account`
- `VERIFY — whether it moves the contact into a pipeline stage, and which one · settles by: the steps in the workflow`
- `VERIFY — what it sends after the call, and how long after · settles by: the steps in the workflow`

A Hits line names a consequence the reader can go and look at (`rules.md` §3). None can be named from what has been seen, so each carries a VERIFY rather than a guess.

**The second line is the one that decides who can reach this workflow.** An attended state set by the calendar and an attended state set by a person are two different doors, opened by different people doing different things, and only one of them is described inside this workflow.

**The fourth line is the same question the SH - Fit Call Booked card asks about itself.** If both stop the nurture, both touch the same contact, and per `rules.md` §3 that belongs in **Hits** on both cards rather than in either card's **Does not hit**. Which of them actually does it — or whether both do — is open.

---

**Does not hit**

- **SH - Fit Call No Show** — shares the first 14 characters with this one: `SH - Fit Call `. The character count is the weaker half of the resemblance. The sharper half is that these two are the two outcomes of the same appointment. A contact's path is identical right up until the appointment time passes, and then it is one of these or the other. The word that separates them sits at the end of both names, which is the part of a name a reader confirms last.

- **SH - Fit Call Booked** — shares the first 14: `SH - Fit Call `. Named for the same appointment at the other end of it — Booked is reached when the appointment is made, this one when it is kept. Anybody handed the words "the fit call one" has at least three names to choose between, and all three are true descriptions of something that happened around one call.
