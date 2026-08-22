# SH - Fit Call Nurture (Alt Days)

**Type:**   workflow · settled: Sadie, August 19, 2026
**Mark:**   LIVE · settled by workflow list captures, Sadie, Aug 21 2026, `receipts/workflow-list-aug20-1.png` + `receipts/workflow-list-aug20-2.png` · **Checked:** August 21, 2026
**Where:**  Automation → Workflows → "SH - Fit Call Nurture (Alt Days)"
**Source:** the workflow of that name, opened from the account. Cited, not copied — open the real thing and read it there (`rules.md` §4).

Came here from Lane B of `catalog.md`. Read this card, then open the account. Do not open a second card (`rules.md` §5).

---

**The mark stands on three legs**

`rules.md` §1 wants three things for LIVE. Sadie's walk gave two; the workflow list gave the third:

- **found in the account** — settled: Sadie, August 19, 2026
- **a way in that can fire** — settled: Sadie, August 19, 2026 (the tag trigger below)
- **published** — settled by workflow list captures, Sadie, Aug 21 2026, `receipts/workflow-list-aug20-1.png` + `receipts/workflow-list-aug20-2.png`

The third leg stayed open for two days because reading a workflow's steps is not the same as finding it switched on. The workflow list is the screen that shows the switch, and on August 21 it read **Published**.

---

**Hits**

- Fires when the tag `fit call nurture` is added to a contact. That tag is the only way in · settled: Sadie, August 19, 2026
- Sends **15 SMS, spaced 2 days apart** — about four weeks end to end. SMS only; no email anywhere in it · settled: Sadie, August 19, 2026
- Every message carries the Fit Call booking link, slug `safe-harbor-fit-call` · settled: Sadie, August 19, 2026
- Removes the tag `fit call nurture` from the contact after the last message, so a contact who finishes does not re-enter on that tag · settled: Sadie, August 19, 2026

**If you were sent here to change timing, three things decide what else moves.**

**One — the name is currently true, and it will not stay true by itself.** The wait steps are 2 days apart, which is what `Alt Days` claims · settled: Sadie, August 19, 2026. Change the spacing and the name starts describing something the workflow no longer does. The name will not update itself.

**Two — the length is 15 messages, not the spacing alone.** Widening the gaps stretches the whole sequence past four weeks. The last message is written as a last message, and it arrives whenever the maths puts it.

**Three — this sequence stops when a contact books, and that stop lives in other workflows, not in this one.** Two objects reach in and pull contacts out:

- **SH - Fit Call Booked** removes the contact from this workflow and removes the `fit call nurture` tag · settled: Sadie, August 19, 2026
- **SH - Fit Call Attended** does the same · settled: Sadie, August 19, 2026

Per `rules.md` §3 both belong in **Hits** here as well as on their own cards, because all three touch the same contact. Editing this workflow does not change either of them, and neither of them appears when you have this one open on screen.

**A contact can come back into this sequence after missing a call.** `SH - Fit Call No Show` waits 2 days, checks whether the contact has re-booked, and on the branch where they have not, adds `fit call nurture` again — which starts this workflow over from message one · settled: Sadie, August 19, 2026.

---

**Does not hit**

**Four of them now, not two.** Sadie's walk found two published nurture campaigns the map did not have (`/receipts/`, C-7):

- **SH - Fit Call No Show** — shares the first 15 characters: `SH - Fit Call N`. A search box typed that far returns both.
- **SH - Fit Call Booked** — shares the first 14: `SH - Fit Call `.
- **SH - Assessment Booking Nurture** — shares the first 5, `SH - `, and the word **Nurture**. Found and published · settled: Sadie, August 19, 2026. No card yet.
- **Paperwork Reminder Nurture** — shares no prefix at all, and the word **Nurture**. Found and published · settled: Sadie, August 19, 2026. No card yet.

**The word `nurture` is the trap, not the prefix.** Somebody handed *"change the nurture texts"* types `nurture` into the search box, and that returns all four names above plus the tag `fit call nurture` — five results, three of them workflows that send messages. Typing `SH - Fit Call N` returns two. The shorter, more natural search is the one that returns the bigger pile.

`VERIFY — which of these gets grabbed in place of this workflow · settles by: Test B — the run itself, and which name Nicole opens first`

Until then all four are live risks. Confirm the name at the top of the screen before touching anything.
