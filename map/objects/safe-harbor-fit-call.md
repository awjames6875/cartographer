# Safe Harbor Fit Call

**Type:**   calendar / booking link · settled: Sadie, August 19, 2026
**Mark:**   LIVE · settled: Sadie, August 19, 2026    **Checked:** August 19, 2026
**Where:**  Calendars → "Safe Harbor Fit Call" · calendar ID `AuOmiT3Afi2aXSlH7JJQ`
**Source:** the calendar of that name, opened from the account. Cited, not copied — open the real thing and read it there (`rules.md` §4).

Came here from Lane G of `catalog.md`. Read this card, then open the account. Do not open a second card (`rules.md` §5).

---

**What earned the mark**

- **found in the account** — Calendars
- **enabled, with availability on it** — Monday to Friday, 8:00am to 5:00pm, auto-confirm on
- **a link to it in use** — the booking slug resolves live, and two walked workflows send it to contacts

All three settled: Sadie, August 19, 2026.

---

**VERIFY-1 — settled**

**`safe-harbor-fit-call` is the live slug.** `safeharbor-fit-call` returns a 404 · settled: Sadie, August 19, 2026 — she opened the calendar, read the link off it, and tested both spellings in a browser.

This was the highest-priority open line on the map, and the reason it mattered stands even now it is closed: Safe Harbor's own written documentation disagreed with itself, so **at least one document still in circulation carries the dead spelling**. A link copied out of a document rather than out of the account may still be the 404.

The two walked workflows that send the link — **Safe Harbor Consultation Lead Flow Vo2** and **SH - Fit Call No Show** — both carry the live spelling · settled: Sadie, August 19, 2026. Anywhere else it appears has not been checked: `VERIFY — which other objects, documents, or messages carry a booking link, and which spelling each uses · settles by: the account, and wherever Safe Harbor keeps its written documentation`

**A correction to this card's own reasoning.** It previously said a complete booking URL carries the sub-account's location ID, and redacted whole links for that reason. The live link is of the form `.../widget/bookings/<slug>` and carries no location ID · settled: Sadie, August 19, 2026. The slugs-only habit stays because the slug is the part that answers the question, but the reason written here was wrong and the account is what corrected it (`rules.md` §4).

---

**Hits**

- A booking on this calendar fires **SH - Fit Call Booked** · settled: Sadie, August 19, 2026
- Setting an appointment on it to status **showed** fires **SH - Fit Call Attended**; setting it to **No Show** fires **SH - Fit Call No Show** · settled: Sadie, August 19, 2026
- All three of those trigger on this calendar's ID specifically, not on any booking anywhere in the account · settled: Sadie, August 19, 2026
- Books 15-minute calls with **Apollo**, on Google Meet · settled: Sadie, August 19, 2026
- Accepts bookings from at least 4 hours ahead, up to 60 days out · settled: Sadie, August 19, 2026
- **Auto-confirms**, and sends its own confirmation message to the client from this screen · settled: Sadie, August 19, 2026

**The confirmation message lives here, not in a workflow** · settled: Sadie, August 19, 2026.

This is the correction that matters most for anybody routed to Lane C. `SH - Fit Call Booked` sends nothing at all — it only moves tags. Somebody told to "change the confirmation message" who opens that workflow will find no message in it. The wording is on this calendar's screen.

The confirmation message also tells the client a confirmation text follows. What sends that text is not on the walked map: `VERIFY — what sends the confirmation text the calendar's message promises · settles by: this calendar's notification settings, and the account`

`VERIFY — whether a reminder goes out before the call, and whether it comes from this calendar's notification settings or from somewhere else · settles by: this calendar's notification settings in the account`

**Two statuses on this calendar are set by a person, by hand** · settled: Sadie, August 19, 2026 (C-5). Nothing here flips an appointment to showed or No Show when the time passes. Both downstream workflows wait on somebody clicking.

`VERIFY — whose availability this calendar reads beyond Apollo, and who else it is assigned to · settles by: the calendar in the account`

---

**Does not hit**

- **Schedule an Appointment** — the other calendar, on the same screen. The words "the booking calendar" and "the appointment calendar" describe either one. It is reported as do-not-touch, and workflows are reported to filter around it, which puts its name *inside* workflow steps that have nothing else to do with it. That appearance is a filter excluding it, not a connection. Named in `catalog.md` under **Named, and nothing flowing through**.

- **The workflow carrying the text the link was in.** Still the near-miss for *"the link in the text goes to the wrong place"* — but the shape of it has changed now VERIFY-1 is settled. The link is correct in both walked workflows, so a wrong link found in a message did not come from either of them, and changing this calendar will not fix a stale link already typed somewhere else. Both spellings differ by one hyphen on screen.

- **Sarah, and any booking made from a call.** Sarah is configured in a different sub-account and does not create contacts in this one · settled: Sadie, August 19, 2026 (C-9). `VERIFY — whether Maria books onto this calendar, and whether a booking she makes is distinguishable from one a person made · settles by: the account`
