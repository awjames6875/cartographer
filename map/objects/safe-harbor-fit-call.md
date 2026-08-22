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

**Don't copy a booking link out of a document.** Safe Harbor's written documentation disagreed with itself, so at least one document still in circulation carries the dead spelling. Read the link off the calendar.

Both walked workflows that send the link — **Safe Harbor Consultation Lead Flow Vo2** and **SH - Fit Call No Show** — carry the live spelling · settled: Sadie, August 19, 2026. Nowhere else has been checked.

`VERIFY — which other objects, documents, or messages carry a booking link, and which spelling each uses · settles by: the account, and wherever Safe Harbor keeps its written documentation`

**This card had its own reasoning corrected.** It said a booking URL carries the sub-account's location ID, and redacted whole links for that reason. It does not — the live link is `.../widget/bookings/<slug>` · settled: Sadie, August 19, 2026. Slugs only, because the slug is the part that answers the question (`rules.md` §4).

---

**Hits**

- A booking on this calendar fires **SH - Fit Call Booked** · settled: Sadie, August 19, 2026
- Setting an appointment on it to status **showed** fires **SH - Fit Call Attended**; setting it to **No Show** fires **SH - Fit Call No Show** · settled: Sadie, August 19, 2026
- All three of those trigger on this calendar's ID specifically, not on any booking anywhere in the account · settled: Sadie, August 19, 2026
- Books 15-minute calls with **Apollo**, on Google Meet · settled: Sadie, August 19, 2026
- Accepts bookings from at least 4 hours ahead, up to 60 days out · settled: Sadie, August 19, 2026
- **Auto-confirms**, and sends its own confirmation message to the client from this screen · settled: Sadie, August 19, 2026

**The confirmation message lives here, not in a workflow** · settled: Sadie, August 19, 2026.

Sent here to change the confirmation message? This is the right screen. `SH - Fit Call Booked` sends nothing at all — it only moves tags.

The message tells the client a confirmation text follows. What sends that text is not on the walked map. `VERIFY — what sends the confirmation text the calendar's message promises · settles by: this calendar's notification settings, and the account`

`VERIFY — whether a reminder goes out before the call, and whether it comes from this calendar's notification settings or from somewhere else · settles by: this calendar's notification settings in the account`

**Two statuses on this calendar are set by a person, by hand** · settled: Sadie, August 19, 2026 (C-5). Nothing here flips an appointment to showed or No Show when the time passes. Both downstream workflows wait on somebody clicking.

`VERIFY — whose availability this calendar reads beyond Apollo, and who else it is assigned to · settles by: the calendar in the account`

---

**Does not hit**

**The full name of this one is `Safe Harbor Fit Call`. There are two calendars on that screen.**

- **`Schedule an Appointment`** — not this one. The other calendar, same screen. "The booking calendar" and "the appointment calendar" both fit either. Reported do-not-touch. Workflows filter around it, so its name appears inside steps that have nothing else to do with it — that is a filter excluding it, not a connection.
- **The workflow the link was sent in** — not this one. Both walked workflows carry the live slug · settled: Sadie, August 19, 2026. A wrong link in a message did not come from either. Changing this calendar does not fix a link already typed somewhere else.
- **Sarah, and any booking made from a call** — not this one. She is in a different sub-account and does not create contacts here · settled: Sadie, August 19, 2026 (C-9). `VERIFY — whether Maria books onto this calendar, and whether a booking she makes is distinguishable from one a person made · settles by: the account`
