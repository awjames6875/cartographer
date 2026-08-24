# TEST A — Account Walk with Sadie

Comp \#11 · The Cartographer · Safe Harbor GHL Map  
Method: frozen in TEST\_METHOD.md, committed Aug 17, 2026 — before this run  
Date of walk: \_\_\_19 August 2026\_\_\_\_\_\_\_\_\_  
Present: Adam James, Sadie  
Recorded: yes / no (consent given: yes / no)

**Redaction, Aug 21 2026:** three phone numbers replaced with `[phone redacted]` — the
same rule the cards follow. Nothing else was touched. Every answer, every calendar and
form ID, and the recording link are intact, so anything stated here is still checkable
against the account.

\---

## HOW THIS WORKS — read aloud before starting

Sadie's job is to LOOK and REPORT. Not to fix, change, publish, delete, or clean up  
anything. If something is wrong, that is a finding, not a task.

Every answer gets written in this file as she says it. Wrong answers stay in. If the  
map is wrong, the correction is the receipt — it is worth more than a map that  
happened to be right.

Write the date next to each answer.

\---

## PRIORITY 1 — The three contradictions

*My own documents disagree with each other on these. Highest value questions in the file.*

### VERIFY-1 — The booking slug

Open Calendars → "Safe Harbor Fit Call" → read the actual booking link.

Which spelling is real? safe-harbor-fit-call OR safeharbor-fit-call  
**Answer: [https://api.leadconnectorhq.com/widget/bookings/safe-harbor-fit-call](https://api.leadconnectorhq.com/widget/bookings/safe-harbor-fit-call)**  
Date: 08-19-2026

Open BOTH links in a browser. What happens to each?  
**Answer:** safe-harbor-fit-call \- opens the correct webpage. Safeharbor-fit-call goes to 404 error.  
Date: 08-19-2026

### VERIFY-2 — Which tag does Vo2 check?

Open Automation → Workflows → "Safe Harbor Consultation Lead Flow Vo2" → find the If/Else step near the end.  
find the If/Else step near the end.  
Exact tag name the If/Else is checking:  
**Answer:** Appointment booked. Date: 08-19-2026

Does a tag named Fit Call Booked exist?  
**Answer:** yes

Does a tag named Appointment Booked exist?  
**Answer:** yes

If both exist, is anything still using the older one?  
**Answer:** NO

	

### VERIFY-3 — Daycare (program discontinued)

*Safe Harbor no longer works with daycares. Adam believes the workflow is off — We turned them off today.*  
Workflow "Daycare Affiliation Tagging" — exists? · published or draft?  
**Answer:** yes · Published

Custom field "Are you from Innovators of the Future?" — still there?  
**Answer:** No

Tags Daycare Referral and Daycare \- Angelicas Connection — still there?  
**Answer:** Yes, still there

Do any OTHER workflows still reference these tags or that field?  
**Answer:** None in sub account safe harbor parents intake

  *(most important line in this section — a dead program's tags can still be wired to something live)*  
	  
\---

## PRIORITY 2 — The question that blocks Tiffany's test

### Does booking stop the nurture texts?

Open "SH \- Fit Call Booked" and read its steps  
**Here’s what your current workflow “SH \- Fit Call Booked” does:**  
**Triggers:**

* **Customer Books Safe Harbor Fit Call Appointment: Fires when a customer books an appointment on the specific calendar with ID AuOmiT3Afi2aXSlH7JJQ, and the booking is in “contact” mode.**

**Actions:**

* **Remove from SH \- Fit Call Nurture (Alt Days) Workflow: Immediately unenrolls the contact from the other workflow named “SH \- Fit Call Nurture (Alt Days)”.**  
* **Remove Tag: fit call nurture: Removes the contact tag fit call nurture from the contact.**  
* **Remove Tag: fit call no show: Removes the contact tag fit call no show from the contact.**  
* **Add Tag: fit call booked: Adds the tag fit call booked to the contact, marking them as having a booked fit call.**

**Overall, this workflow cleans up any previous nurture/no-show status and clearly marks the contact as “fit call booked” as soon as they schedule that appointment.**  
.  
Does it remove the contact from "SH \- Fit Call Nurture (Alt Days)"?  
**Answer:** yes

Does it remove the tag Fit Call Nurture?  
**Answer:** yes

If a contact books, can they still receive nurture texts telling them to book?  
**Answer:** NO. Date: 08-19-2026

\---

## PRIORITY 3 — The eight walked objects

*Same three questions each. Write what the screen says, not what it should say.*

| \# | Object | Published or draft? | What turns it on (trigger)? | Tags added / removed |  
|---|--------|--------------------|-----------------------------|----------------------|  
| 1 | Safe Harbor Consultation Lead Flow Vo2 | | | |  
**Overall purpose:**  
**Handle new Safe Harbor consultation leads from the website, notify your team, trigger a Voice AI intake call, and drive the lead to book a “Fit Call” with Apollo, with follow‑ups if they don’t book.**  
---

**Trigger:**

* **Lead Form Submission (Safe Harbor):**  
  * **Fires when a contact submits one of two specific website forms (IDs tP6U9TbhZI7RcUEAeDm1 or QiHZ9AqGPrLJR596VHON).**

---

**Actions (in order):**

* **Add Website Lead and 60-Day Funnel Tags:**  
  * **Tags the contact with “Website Lead” and “60-Day Funnel”.**  
* **Internal Notification (SMS) – notify Apollo on text for new lead:**  
  * **Sends an internal SMS to all users:**  
    * **“New Safe Harbor lead: \[name\] — \[phone\]. Maria is calling them now. Details in the platform.”**  
* **Internal Notification (Email) – notify Apollo on email for new lead:**  
  * **Sends an internal email to your team (userType: all) with full form details:**  
    * **Name, phone, email**  
    * **Who Needs Support**  
    * **Insurance Type**  
    * **TCPA Consent**  
    * **Date Submitted**  
  * **From: “Safe Harbor Behavioral Health” support@safeharborbehavioralhealth.com**  
  * **Subject: “A new lead just submitted the website form”**  
* **Send Confirmation SMS to Contact:**  
  * **To the lead:**  
    * **Thanks them for the inquiry and says you’ll be contacting them shortly.**  
    * **Signed with the user’s first name.**  
* **Send Confirmation Email to Contact:**  
  * **To the lead, from business email:**  
    * **Confirms you received their consultation request.**  
    * **Tells them Maria will call soon from [phone redacted] to ask a few questions.**  
    * **Explains that after Maria’s call, they’ll get a text to book a free 15‑minute Fit Call with Apollo.**  
    * **Provides a fallback if they miss the call (reply to email or text [phone redacted]).**  
* **Wait 90 Seconds:**  
  * **Short delay before tagging and branching.**  
* **Add Voice AI Called Tag:**  
  * **Adds the tag “Voice AI Called” to the contact.**  
* **If/Else – Check if Contact Phone Number is present:**  
  * **Condition: does the contact have a phone number?**

---

### **YES branch (phone number present)**

* **\#6 VAPI Outbound Call (Custom Webhook):**  
  * **Calls the VAPI API (https://api.vapi.ai/call/phone) to trigger an outbound Voice AI call.**  
  * **Sends:**  
    * **Assistant ID and phoneNumberId**  
    * **Customer number: \+1{{contact.phone}}**  
    * **Customer name: {{contact.name}}**  
    * **Assistant variables: contact first name, insurance type, who needs support, and child’s first name.**  
* **Wait 15 Minutes:**  
  * **Gives time for the Voice AI call to complete and data to be available.**  
* **Send Call Summary and Transcript to Apollo (Email):**  
  * **Sends an email (to be configured with recipients) containing:**  
    * **{{voice\_ai.summary}}**  
    * **{{voice\_ai.transcript}}**  
  * **Subject: “Call Summary and Transcript”.**  
* **Send Fit Call Booking SMS to Contact:**  
  * **To the lead:**  
    * **Thanks them for chatting with Maria.**  
    * **Sends booking link for the free Fit Call with Apollo:**  
      * **https://api.leadconnectorhq.com/widget/bookings/safe-harbor-fit-call**  
* **Wait 24 Hours:**  
  * **Waits one day to see if they book.**  
* **If/Else – Check if Appointment Booked Tag Exists:**  
  * **Checks if the contact has the tag “Appointment Booked”.**  
* **YES sub-branch – Appointment Booked Tag Present:**  
  * **No further actions; the flow ends for booked contacts.**  
* **NO sub-branch – None:**  
* **SMS – Reminder to Book Fit Call:**  
  * **To the lead:**  
    * **Gentle reminder to book their free Fit Call.**  
    * **Re-sends the same booking link.**

---

### **NO branch (no phone number present)**

* **Add 'Missing Phone Number' Tag:**  
  * **Tags the contact with “Missing Phone Number”.**  
* **Internal Notification for Missing Phone (Email):**  
  * **Sends an internal email to specific users (three selected users) saying:**  
    * **A new lead submitted the form without a phone number.**  
    * **Maria could not call them.**  
    * **Includes lead name, email, source, and (blank) phone.**  
  * **Subject: “Lead Missing Phone Number \- Action Required”.**

---

**Net effect:**

* **Every form lead is tagged and acknowledged by SMS and email.**  
* **If a phone number exists:**  
  * **Voice AI (VAPI) calls the lead, then Apollo receives a summary and transcript.**  
  * **The lead gets a booking link for a Fit Call and a reminder if they don’t book within 24 hours.**  
* **If no phone number:**  
  * **The lead is tagged as missing phone, and your team is alerted to follow up manually.**

| 2 | SH \- Fit Call Nurture (Alt Days) | | | |  
**Purpose:**  
**A long-term SMS nurture sequence for contacts who get the “fit call nurture” tag, encouraging them to book a free 15‑minute Fit Call with Safe Harbor, while staying gentle and low-pressure.**  
**How it starts (Trigger):**

**Triggers:**

* **Contact Tag: Fires when the tag "fit call nurture" is added to a contact.**

**Once that tag is added, the contact enters this workflow.**

**What happens next (Actions in order):**

**Actions:**

* **SMS: Immediate intro text from Safe Harbor holding their spot and linking to the Fit Call booking page.**  
* **Wait: Wait 2 days.**  
* **Send SMS: Taking the first step: Normalizes that reaching out is hard and invites them again to book.**  
* **Wait: Wait 2 days.**  
* **Send SMS: SoonerCare/Medicaid info: Reassures them that sessions are typically covered if they have SoonerCare/Medicaid, with booking link.**  
* **Wait: Wait 2 days.**  
* **Send SMS: Apollo introduction: Personal intro from Apollo, the person they’d speak with on the Fit Call.**  
* **Wait: Wait 2 days.**  
* **Send SMS: Not alone message: Emotional reassurance that they don’t have to figure things out alone, with booking link.**  
* **Wait: Wait 2 days.**  
* **Send SMS: Fit Call availability: Clarifies Fit Call hours (Mon–Fri, 8am–5pm) and flexibility.**  
* **Wait: Wait 2 days.**  
* **Send SMS: We help Tulsa families: Social proof that you help Tulsa families every week, with booking link.**  
* **Wait: Wait 2 days.**  
* **Send SMS: Still thinking it over?: Normalizes hesitation and keeps the door open.**  
* **Wait: Wait 2 days.**  
* **Send SMS: Have a question?: Invites them to reply with questions; emphasizes a real person reads the texts.**  
* **Wait: Wait 2 days.**  
* **Send SMS: 15-Minute Call Answers Everything: Clarifies what the call covers (insurance, scheduling, what sessions look like).**  
* **Wait: Wait 2 days.**  
* **Send SMS: Safe Harbor checking in: Gentle check-in, reiterating no pressure and open door.**  
* **Wait: Wait 2 days.**  
* **Send SMS: No instruction manuals: Empathy message about parenting being hard, with booking link.**  
* **Wait: Wait 2 days.**  
* **Send SMS: We're Not Going Anywhere: Reassures them you’ll be here whenever timing is right.**  
* **Wait: Wait 2 days.**  
* **Send SMS: We'll stop texting soon: Signals the sequence is wrapping up and keeps the door open.**  
* **Wait: Wait 2 days.**  
* **Send SMS: Last text: Final message with phone number and booking link, personalized with first name.**  
* **Remove 'fit call nurture' Tag: Removes the "fit call nurture" tag from the contact, effectively marking them as completed for this nurture.**

**Overall behavior:**

* **Entire sequence is SMS-only, spaced every 2 days.**  
* **Tone is supportive, low-pressure, and focused on reassurance, logistics (time/coverage), and keeping the door open.**  
* **At the end, the tag is removed so they don’t keep re-entering this same nurture based on that tag.**

| 3 | SH \- Fit Call Booked | | | |  
**Here’s what your current workflow "SH \- Fit Call Booked" does:**  
**Trigger:**

* **Customer Books Safe Harbor Fit Call Appointment:**  
  * **Fires when a customer books an appointment on the specific calendar with ID AuOmiT3Afi2aXSlH7JJQ.**  
  * **Only runs when the booking is made in contact mode (i.e., for a contact, not some other entity).**

**Actions (in order):**

* **Remove from SH \- Fit Call Nurture (Alt Days) Workflow:**  
  * **Immediately removes the contact from the other workflow named "SH \- Fit Call Nurture (Alt Days)" so they don’t keep receiving nurture messages after they’ve booked.**  
* **Remove Tag: fit call nurture:**  
  * **Removes the "fit call nurture" tag from the contact, indicating they are no longer just being nurtured toward booking.**  
* **Remove Tag: fit call no show:**  
  * **Removes the "fit call no show" tag from the contact, clearing any previous no‑show status they might have had.**  
* **Add Tag: fit call booked:**  
  * **Adds the "fit call booked" tag to the contact, marking them as having an upcoming fit call booked.**

**In plain terms: when someone books a Safe Harbor Fit Call on that calendar, this workflow cleans up their old nurture/no‑show status and tags them as booked, while also pulling them out of the nurture workflow so they don’t get conflicting messages.**  
**purpose of this workflow?**  
**The purpose of this workflow is to update a contact’s status when they successfully book a Safe Harbor Fit Call so that all your systems and messaging stay consistent.**

**More specifically, it:**

* **Stops nurture messaging by removing them from the “SH \- Fit Call Nurture (Alt Days)” workflow.**  
* **Cleans up old tags (removes “fit call nurture” and “fit call no show”) so they’re not treated as still nurturing or as a no‑show.**  
* **Marks them as booked by adding the “fit call booked” tag, which you can use for follow-up workflows, reporting, and segmentation.**

**In short: it converts someone from a “lead being nurtured / possible no‑show” into a clearly tagged “fit call booked” contact and prevents conflicting automations from running on them**

| 4 | SH \- Fit Call No Show | | | |  
**Here’s what your current workflow “SH \- Fit Call No Show” does:**  
**Trigger:**

* **Appointment Status Change: No Show, Safe Harbor Fit Call:**  
  * **Fires when an appointment on the Safe Harbor Fit Call calendar (ID: AuOmiT3Afi2aXSlH7JJQ) is marked as No Show.**  
  * **Only runs for standard events (eventType \= normal) and for contacts (not other modes).**

**Actions (in order):**

* **Remove Tag: fit call booked:**  
  * **Immediately removes the "fit call booked" tag from the contact.**  
* **Add Tag: fit call no show:**  
  * **Adds the "fit call no show" tag to the contact so you can track no-shows.**  
* **Send Fit Call No Show SMS:**  
  * **Sends this SMS to the contact, from the contact owner:**  
    ***Hi {{contact.first\_name}}, we missed you today — totally fine, life gets busy. One thing though: the sooner you rebook, the sooner your family gets support. Takes 15 seconds: [https://api.leadconnectorhq.com/widget/bookings/safe-harbor-fit-call](https://api.leadconnectorhq.com/widget/bookings/safe-harbor-fit-call)***  
* **Wait 2 Days:**  
  * **Pauses the workflow for 2 days after the SMS is sent.**  
* **Check if Tag 'fit call booked' Present (If/Else condition):**  
  * **After 2 days, checks whether the contact now has the "fit call booked" tag.**  
  * **This splits into two branches:**  
    * **Tag Present – YES Branch:**  
      * **If the contact does have the "fit call booked" tag, they follow this branch.**  
      * **Currently, there are no further actions configured on this YES branch (it effectively ends here).**  
    * **None (NO Branch):**  
      * **If the contact does not have the "fit call booked" tag, they follow this branch.**  
* **Add Tag (on NO Branch):**  
  * **On the NO branch only (no rebooking after 2 days), the workflow adds the "fit call nurture" tag to the contact.**  
  * **This likely moves them into a separate nurture sequence or segment for ongoing follow-up.**

**In plain language:**  
**When someone no-shows their Safe Harbor Fit Call, you remove their “booked” tag, mark them as a no-show, send a rebooking SMS, wait 2 days, then check if they rebooked. If they did, the workflow stops. If they didn’t, you tag them for a nurture sequence.**

| 5 | SH \- Fit Call Attended | | | |  
**Here’s what your current workflow “SH \- Fit Call Attended” does:**  
**Trigger:**

* **Appointment Status Showed on Safe Harbor Fit Call:**  
  * **Fires when an appointment:**  
    * **Is a normal event type**  
    * **Is booked on the “Safe Harbor Fit Call” calendar (ID: AuOmiT3Afi2aXSlH7JJQ)**  
    * **Has an appointment status of “showed”**  
    * **Is associated with a contact (not, for example, just a lead without a contact record)**

**Actions (in order):**

* **Remove Tag: fit call nurture:**  
  * **Removes the contact tag “fit call nurture” from the contact, if present.**  
* **Remove Tag: fit call no show:**  
  * **Removes the contact tag “fit call no show” from the contact, if present.**  
* **Remove Tag: fit call booked:**  
  * **Removes the contact tag “fit call booked” from the contact, if present.**  
* **Add Contact Tag: fit call attended:**  
  * **Adds the tag “fit call attended” to the contact to mark that they actually attended their fit call.**  
* **Remove Contact From Workflow: SH \- Fit Call Nurture (Alt Days):**  
  * **Removes the contact from the other workflow named “SH \- Fit Call Nurture (Alt Days)” so they stop receiving that nurture sequence once they’ve attended.**

**In plain terms: when someone shows up to their Safe Harbor Fit Call, this workflow cleans up any pre-call or no-show tags, marks them as having attended, and pulls them out of the pre-call nurture workflow.**

| 6 | Safe Harbor Fit Call (calendar) | | | |  
**It's a quick 15-minute introductory call with your intake team designed to:**

* **✅ Confirm you're a good fit for services**  
* **✅ Verify insurance coverage**  
* **✅ Answer questions before a client's first session**

---

### **⚙️ Key Settings**

| Detail | Value |
| :---- | :---- |
| **Duration** | **15 minutes** |
| **Meeting Format** | **Google Meet ("Join Your Fit Call")** |
| **Availability** | **Monday–Friday, 8:00 AM – 5:00 PM** |
| **Advance Booking** | **At least 4 hours ahead** |
| **Booking Window** | **Up to 60 days out** |
| **Auto-Confirm** | **Yes** |
| **Team Member** | **Apollo (Safe Harbor)** |

---

### **💬 Confirmation Message to Clients**

***"Your fit call with Apollo at Safe Harbor is confirmed\! You'll receive a confirmation text shortly. Questions? Call us at [phone redacted]."***

**In short, this calendar is your first touchpoint in the client intake process — a low-pressure screening call to make sure potential clients are matched with the right services before booking a full session.**

| 7 | Maria (outbound voice AI) | | | |  
**Outbound bot used for basic customer interaction in the beginning to help assure the clients of immediate assistance and timely call backs along with assisting them to book a free call with our therapists**  
**It triggers for VAPI and is set under the name MARIA.**

| 8 | Sarah (inbound voice AI) | | | |  
**Sarah is set for the other subaccount safe harbor behavioral health. It ddoes answer the calls the come in but store them under a different sub account**

Extra for \#5: is "SH \- Fit Call Attended" actually a workflow — or is it a tag or an  
appointment status? (The map guessed workflow from the naming pattern.)  
\*\*Answer:\*\* \_  
**It's actually both — a workflow and a tag. Here's what I found:**  
---

### **✅ Workflow: "SH \- Fit Call Attended"**

* **Status: Published**  
* **Version: 5**  
* **Created: August 12, 2026**  
* **Last Updated: August 12, 2026**

**This is an active, published automation that fires when a fit call is attended.**

---

### **🏷️ Tag: "fit call attended"**

**There's also a matching tag (lowercase: *fit call attended*) in your location — likely applied by the workflow when it runs, to mark the contact's status.**

---

### **❌ Appointment Status?**

**No — it's not a native appointment status. Appointment statuses in the platform are system-defined (e.g., *confirmed*, *showed*, *no-show*, *cancelled*). "Fit Call Attended" is tracked via the tag instead.**

---

**In short: The workflow "SH \- Fit Call Attended" triggers when a fit call appointment is attended, and it likely applies the "fit call attended" tag to the contact as part of its automation.**

Extra for \#6: is the "attended / no-show" state set by the calendar automatically, or  
by a person changing it by hand?  
**\*\*Answer:\*\* By a person, manually — the platform does not automatically flip an appointment to "showed" or "no-show" after the scheduled time passes.**  
**Here's how it typically works:**

---

### **🔄 The Manual Process**

1. **A team member opens the appointment in the calendar (or from the contact record)**  
2. **They manually change the appointment status to "Showed" or "No-Show"**  
3. **That status change triggers the corresponding workflow**

---

### **🔗 How Your Workflows Connect**

| Manual Status Change | Triggers Workflow |
| :---- | :---- |
| **Appointment → Showed** | **SH \- Fit Call Attended** |
| **Appointment → No-Show** | **SH \- Fit Call No Show** |

---

### **⚠️ Key Implication**

**If your team doesn't update appointment statuses in the calendar, those workflows will never fire — contacts won't get tagged, moved through the pipeline, or receive follow-up automations.**

\---

## \#\# PRIORITY 4 — Ghosts: found or empty?

*Rule: found in the account \= LEFTOVER. Search comes back empty \= GHOST.*

Search Custom Fields for "Intake Journey Stage" — found or empty?  
**Answer:** Found  
What is the nurture campaign you're building actually NAMED in GHL?  
  not a searchable name.)  
**Answer:** Paperwork Reminder Nurture and SH \- Assessment Booking Nurture. Date: 08-19-2026  
 \*\*Date:\*\* 08-19-2026  
Is that campaign published or still draft?  
**Answer:** Published  
\---

## \#\# PRIORITY 5 — Two open questions

Where does Maria live inside GHL? A webhook step inside a workflow? An inbound webhook trigger? Somewhere else? What exact screen?  
  webhook trigger? Somewhere else? What exact screen?  
**Answer:** the outbound bot is configured as a VAPI “Create a Call” action inside a workflow, found in the Add action panel in Automation → Workflows, after you’ve connected VAPI in Settings → Integrations.  
Does Sarah create contacts when she answers a call?  
**Answer:** no

\---

## \#\# PRIORITY 6 — The catch-all

Is there anything LIVE in this account that is not on this list? (Workflows, calendars, forms, tags, custom fields, voice agents — anything.)  
(Workflows, calendars, forms, tags, custom fields, voice agents — anything.)

**Answer:** everything so far built by sadie has been covered above and answered. Date: 08-19-2026  
**\*\*Date:\*\* 08-19-2026**

\---

## \#\# AFTER THE WALK — for Adam

\- \[ \] Every answer above dated  
\- \[ \] Corrections applied to the cards, each one dated in /receipts/  
\- \[ \] Anything Sadie named that the map missed → new catalog line  
\- \[ \] This completed file saved to /receipts/ OUTSIDE the map/ drop-in folder (M10)  
\- \[ \] Recording (if any) saved and linked in /receipts/  
