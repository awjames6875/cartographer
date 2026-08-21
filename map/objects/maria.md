# Maria

**Type:**   not a GoHighLevel object · her footprint inside the sub-account is one workflow step, located below
**Mark:**   declined — see below · **Checked:** August 19, 2026
**Where:**  the step that starts her: Automation → Workflows → "Safe Harbor Consultation Lead Flow Vo2", on the branch where the contact has a phone number · settled: Sadie, August 19, 2026
**Source:** reported by Safe Harbor as an outbound voice AI running on VAPI. Nothing on this card is copied from VAPI, and this map does not open VAPI (`identity.md`, the territory).

Came here from Lane H of `catalog.md`. Read this card, then open the account. Do not open a second card (`rules.md` §5).

---

**Maria is outside the boundary. Her footprint is not.**

`identity.md` draws the territory as Safe Harbor's GoHighLevel sub-account and puts the phone system, and anything else that is not GoHighLevel, outside it. Maria runs on VAPI. VAPI is not GoHighLevel. She is outside.

What this card maps is the part of her that is inside — the objects in this sub-account that start her and receive from her. Those are GoHighLevel objects, they sit in the territory, and the ordinary rules apply.

What this card does not map, and what does not get added later: what she says on a call, how she is configured, what her script is, or anything else on the VAPI side. That somewhere is not in this folder and not in this account, and the map stops at the line rather than reaching across it.

---

**The mark is declined, not deferred**

Sadie's walk did not change this, and no walk can. **LIVE** requires that the object was found *in the account* (`rules.md` §1). Maria is not in the territory, so a mark she cannot earn is not a mark that is pending — it is one this map has no standing to give.

**Her footprint can be marked, and the object carrying it now has a name.** It is a step inside **Safe Harbor Consultation Lead Flow Vo2**, and that workflow has its own card and its own open mark.

---

**Hits**

Every line here is about a consequence **inside the sub-account**. What Maria does on the phone is a consequence too, and it is not this map's to record — a reader of this folder cannot go and look at it (`rules.md` §3).

- **What starts her — settled.** A step on the YES branch of **Safe Harbor Consultation Lead Flow Vo2**, on the branch where the contact has a phone number, places the outbound call · settled: Sadie, August 19, 2026
- **What comes back — settled.** Her call summary and transcript return into that same workflow as merge fields and go out in an internal email to the team · settled: Sadie, August 19, 2026
- The workflow adds the tag `Voice AI Called` before the call is placed. **That tag is written by the workflow, not by Maria** · settled: Sadie, August 19, 2026
- The workflow sends her the contact's first name, insurance type, who needs support, and the child's first name · settled: Sadie, August 19, 2026
- The number she dials out from is named in that workflow's confirmation email to the contact · settled: Sadie, August 19, 2026 · [phone redacted] — read it off the step, or from `/receipts/`
- **The name `Maria` does appear inside this sub-account** — in message copy inside that workflow, which tells the team and the contact that she is calling · settled: Sadie, August 19, 2026

**The two lines that were the whole card are now answered.** What starts her, and what comes back. Both live in one workflow, which means everything a person can change about Maria from inside GoHighLevel is on one screen.

**One thing about that step is reported two ways, and the map does not pick.** Sadie described the mechanism generally as a VAPI "Create a Call" action, available from the Add action panel once VAPI is connected in Settings → Integrations. Her walk-through of the workflow itself described the step as a VAPI outbound call implemented as a custom webhook to the VAPI API. Those are not the same mechanism, and which one is in this workflow decides whether changing it is a form field or a request body.

`VERIFY — whether the step in Vo2 is a native VAPI action or a custom webhook · settles by: opening the step in the account`

Still open:

- `VERIFY — whether she books onto Safe Harbor Fit Call, and whether a booking she makes is distinguishable from one a person made · settles by: the calendar in the account`
- `VERIFY — whether she writes anything to the contact record itself — a note, a custom field, a pipeline stage — as opposed to into an email · settles by: a contact record in the account`
- `VERIFY — what happens when she hands a live caller to a person, and who that person is · settles by: the account`

---

**Does not hit**

- **Sarah** — the other voice AI. **Both are now outside this map's boundary, and they are outside it in two different ways** · settled: Sadie, August 19, 2026 (C-9). Maria runs on VAPI — a different product entirely. Sarah runs on GoHighLevel, in the **Safe Harbor Behavioral Health** sub-account — the right product, the wrong territory. The old way of telling them apart was direction, outbound against inbound, and that still holds. It is no longer the difference that costs the most. Somebody who reaches for the wrong one is not opening the wrong screen; they are opening the wrong system, and now there are two wrong systems to land in.

- **The workflow step that starts her.** This is the near-miss for *"Maria said the wrong thing."* Two different things are wrong-able and they live in two places. Who she calls, when, and on what condition is set in the Vo2 step, in this sub-account. What she says once the call connects is set on the VAPI side, outside this map. Changing the step changes the first and leaves the second running exactly as it was. **The step now has an address, which makes this near-miss easier to reach — and no less wrong.**
