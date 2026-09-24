# Admissions, Settings and Access

For nursery staff using the Peekaboo portal at **https://peek.peek-a-boo.app**.

Every button, field, tab and status named in **bold** in this document is the exact
English text the portal displays. If your portal is set to Arabic, the wording will be
translated but the position on screen is the same.

## How this document marks uncertainty

Plain text = confirmed from the portal itself.

Anything introduced by **Not yet checked on a live system** describes what happens after
you press a button — server-side results, whether an email truly arrives, what a deletion
removes elsewhere. Those parts have not been confirmed against a running nursery, so treat
them as "expected", not "guaranteed".

---

# Part 1 — Understanding access

Read this first. It explains why two colleagues can see different menus.

## The access model in plain words

Your account has one **role**. The role decides which pages you can open. There are three
layers, applied in this order.

**Layer 1 — The Principal sees everything.**
If your role is Principal, every page in the portal is open to you. No permission list is
consulted at all. Nothing an administrator ticks or unticks changes what a Principal can
reach.

**Layer 2 — Two pages are reserved for the Admin role.**
**Roles & Access** and **Referrals & Sources** can only be opened by the Admin role.
This is fixed. Ticking those modules for a Registrar, a Teacher or an Accountant does not
let them in. Only the Principal (by Layer 1) and the Admin can reach these two pages.

**Layer 3 — Everyone else gets what their role was granted.**
For all other pages, the portal checks the module list saved against your role on the
**Roles & Access** page. If the module covering that page is ticked, you get in.

## The Centers page is Principal-only

**Centers** sits outside the three layers. It is restricted to the Principal.

Granting the Centers permission to any other role has no effect — the person still cannot
open the page and the link still does not appear in their sidebar. If a non-Principal
colleague needs to change nursery details, point them at **My Center** instead, which is a
normal permission-controlled page.

## The menu only shows what you may open

The sidebar is filtered by exactly the same rules that guard the pages. A link you are not
allowed to open is not greyed out — it is simply absent. A whole group heading disappears
when none of its links are available to you.

So "I cannot find Referrals & Sources in my menu" and "I do not have the Admin role" are
usually the same fact. This also means you cannot audit someone's access by asking them to
read their menu aloud and compare it to yours.

## Quick reference — who can open what

| Page | Sidebar label | Group | URL | Who can open it |
|---|---|---|---|---|
| Leads | **CRM Leads** | **Admissions CRM** | /app/crm/leads | Principal, or any role granted the covering module |
| Referrals & Sources | **Referrals & Sources** | **Admissions CRM** | /app/crm/referrals-sources | Principal and Admin only |
| Roles & Access | **Roles & Access** | **Reports & Admin** | /app/roles | Principal and Admin only |
| My Center | **My Center** | **Center** | /app/my-center | Principal, or any role granted the covering module |
| Centers | **Centers** | **Center** | /app/centers | Principal only |
| Packages | **Packages** | **Center** | /app/packages | Principal, or any role granted the covering module |

---

# Part 2 — Admissions (Leads)

The Leads page is the enquiry pipeline. A lead is one enquiry about one child, from the
first phone call through to a decision.

## The lead stages

There are nine stages. Two things about them matter in daily use.

First, not every stage can be chosen from every screen. The stage menu on the Leads page
offers eight stages. The **Lead Status** dropdown inside the task window offers a
different set of nine. Between them they cover all nine stages, but neither list is
complete on its own.

Second, and more importantly: **the same stage is labelled differently depending on where
you are looking.** Two stages share this quirk. The table below shows both labels.

### Stage table — where to look

| Stage | Label on the **Leads** page stage menu | Label in the task window **Lead Status** list | Notes |
|---|---|---|---|
| 1 | **New Lead** | **New Lead** | Same on both. The starting stage. |
| 2 | **Tour Taken** | **KYC** | Different label per screen. Treat **Tour Taken** as authoritative. |
| 3 | **Book a Tour** | **Book a Tour** | Same on both. |
| 4 | **Admission** | **Admission** | Same on both. |
| 5 | **Accepted** | **Accepted** | Same on both. |
| 6 | **Offer Letter** | **Evaluation** | Different label per screen. Treat **Offer Letter** as authoritative. |
| 7 | *(not offered)* | **Registered** | Only reachable from the task window. |
| 8 | **Lost** | **Lost** | Same on both. |
| 9 | **Rejected** | **Rejected** | Same on both. |

**Treat the Leads page labels as authoritative.** That is the screen your team works from
every day, it is the screen the stage badge on each lead row uses, and it is the wording
to use when you talk to colleagues or write your own notes.

The practical consequence: if you set a lead to **Tour Taken** from the Leads page and then
open the task window, the dropdown will read **KYC**. Nothing has gone wrong and the lead
has not moved. It is the same stage under a second name. The same applies to **Offer
Letter**, which reads **Evaluation** in the task window.

When writing internal guidance for your own nursery, pick the Leads page label and use it
consistently. Mentioning the second label once, as this table does, prevents confusion
without spreading it.

### Colour of the stage badge

The badge next to each lead is colour-coded, which is a faster read than the text:

- **Lost** — red
- **Accepted**, **Registered**, **Approved** — green
- **Admission** — green
- **Book a Tour**, **Offer Letter** — amber
- **Tour Taken**, **Submitted** — dark/neutral
- **New Lead** and anything unrecognised — blue

---

## How to find a lead

**Who can do this:** Principal, or any role granted the Leads module.
**Where:** **CRM Leads**, in the **Admissions CRM** group — /app/crm/leads
**Before you start:** Nothing.

**Steps:**

1. Open **CRM Leads**.
2. Type into the search box, placeholder **Search by name or ID...**. It matches the child's
   name, the parent's name, the phone number, the email address, and the lead's ID number.
3. To narrow further, press **Filter** to open the filter panel.
4. Set any filters you want, then press **Apply Filter**.
5. Press **Sort** to flip the list between A–Z and Z–A by child name.
6. Press **Reset** to clear the search box and every filter at once.

**The filters in full:**

| Filter | What it does | Options |
|---|---|---|
| **Date Range** | Two date boxes, from and to. Limits by the date the lead was created. | Dates |
| **Approved Date Range** | Two date boxes, from and to. | Dates |
| **Age Upto** | Filters by age. | Built from the ages present in your own leads |
| **Nationality** | Filters by nationality. | Built from your own leads |
| **Source** | Filters by record source. | Your **Communication Sources** list |
| **Referral** | Filters by referral. | Your **Referrals** list |
| **Joining Date** | Single date. Matches that exact joining date. | A date |
| **Grade** | Filters by grade. | Built from your own leads |
| **Admission** | Filters by admission value. | Built from your own leads |
| **Flow** | Filters by flow value. | Built from your own leads |
| **Operator** | Filters by the staff member on the lead. | Built from your own leads |

**Good to know:**
The **Reset** button is greyed out until at least one filter or search term is active, so
it doubles as an indicator that a filter is hiding rows. If a colleague says a lead has
vanished, check whether **Reset** is available before anything else.

When nothing matches your filters the page reads **No leads match these filters.** When the
nursery has no leads at all it reads **No leads found.** — two different messages, worth
distinguishing.

---

## How to add a lead

**Who can do this:** Principal, or any role granted the Leads module.
**Where:** **CRM Leads**, in the **Admissions CRM** group — /app/crm/leads
**Before you start:** Your **Referrals** and **Communication Sources** lists must already
contain at least one entry each, because both are required on this form and both are
dropdowns. Only the Principal and the Admin can add to those lists. If the dropdowns are
empty, ask one of them first.

**Steps:**

1. Open **CRM Leads**.
2. Press **Add**. The heading reads **Add a New Lead**.
3. Work down the eight numbered sections and fill in the fields. Required fields are marked
   with a red asterisk.
4. Press **Save** in the bar fixed at the bottom of the screen.

**The form in full.** The form is divided into eight numbered sections.

### 1. Child Details

| Field | Required? | What to enter | Options |
|---|---|---|---|
| **Child Photo** | No | Click the panel to browse, or drag an image onto it | Image files only, under 5 MB |
| **Child Name** | Yes | The child's full name | Free text |
| **Date of Birth** | Yes | The child's date of birth | Date picker |
| **Gender** | Yes | Pick one | **Male**, **Female**. Starts on **Male** |
| **Age Group** | No | The age group the child would join | Your nursery's age groups |
| **Nationality/Country** | Yes | The child's nationality | Country list |
| **Child ID Number** | No | National ID or similar. Placeholder shows the Emirates ID shape | Free text |
| **Primary Language** | No | Main language spoken | **English**, **Arabic**, **Urdu**, **Hindi**, **French**, **Spanish** |
| **Second Language** | No | As above | Same six |
| **Third Language** | No | As above | Same six |
| **Previous Nursery** | No | Name of the previous nursery, if any | Free text |
| **Transport Type** | No | How the child would travel | **Parent Drop-off**, **School Bus**, **Walking** |
| **Staff Member's Child** | Marked required, but has a default | On/off switch, reads **Yes** or **No** | Starts on **No** |
| **General Notes** | No | Background or observations | Long text |

### 2. Primary Parent/Guardian

| Field | Required? | What to enter | Options |
|---|---|---|---|
| **Name** | Yes | Full name of the primary guardian | Free text |
| **Primary Phone** | Yes | Main contact number | Phone |
| **Secondary Phone** | No | Alternate number | Phone |
| **Primary Email** | Yes | Main email address | Email |
| **Secondary Email** | No | Alternate email | Email |
| **Residential Address** | No | Full home address | Long text |

### 3. Second Parent/Guardian

This section is collapsed until you press **Add Second Parent or Guardian**. Once open,
the button changes to **Remove Second Parent**.

| Field | Required? | What to enter | Options |
|---|---|---|---|
| **Name** | No | Full name of the second guardian | Free text |
| **Phone** | No | Their number | Phone |
| **Email** | No | Their email | Email |

If you fill these in and then press **Remove Second Parent** before saving, the three
values are not saved.

### 4. Emergency Contact

| Field | Required? | What to enter | Options |
|---|---|---|---|
| **Name** | No | Who to call in an emergency | Free text |
| **Primary Phone** | No | Their number | Phone |
| **Secondary Phone** | No | Alternate emergency number | Phone |

### 5. Photography Consent

| Field | Required? | What to enter | Options |
|---|---|---|---|
| **Allow photos? (Consent for capturing images)** | Yes | Pick one | **Yes**, **No**. Starts on **Yes** |
| **SPECIFIC USES APPROVED:** | No | Three independent tick boxes | See below |

The three tick boxes are:

- **Nursery Use (Portfolios, inside learning logs)** — ticked by default
- **Media Use (Marketing brochures, booklets)** — ticked by default
- **Social Media Use (Instagram, Facebook posts)** — not ticked by default

The three boxes stay on screen and stay tickable even when **Allow photos?** is set to
**No**, and their settings are saved either way. Because of that, set the tick boxes to
match the consent you actually hold rather than relying on the **No** answer to clear them.

### 6. Special Educational Needs

| Field | Required? | What to enter | Options |
|---|---|---|---|
| **Has SEN? (Special Educational Needs)** | Yes | On/off switch, reads **Yes** or **No** | **Starts on Yes** |
| **SEN Details** | No | Diagnoses, support required, learning plans | Long text, appears only while the switch is **Yes** |

Note the default: **Has SEN?** starts switched on for every new lead. If the child has no
special educational needs, switch it to **No** yourself. It will not do so on its own.

### 7. Enquiry Details

| Field | Required? | What to enter | Options |
|---|---|---|---|
| **Enquiry Date** | No | When the enquiry came in | Date picker |
| **Referral Source** | Yes | Which referral brought this family | Your **Referrals** list |
| **Record Source** | Yes | Which communication source | Your **Communication Sources** list |

### 8. Visit & Joining

| Field | Required? | What to enter | Options |
|---|---|---|---|
| **Joining Date** | No | Expected start date | Date picker |
| **Visit Notes** | No | Tour notes, parent feedback, impressions | Long text |
| **Joining Notes** | No | Expected schedule, transition adjustments | Long text |

**After you save:**
The button reads **Saving...** while it works. On success a green message appears reading
**New lead saved successfully.** and you are returned to the list.

If a required field is empty the form does not submit and an error message appears
instead. Because of how the messages are wired, the message for a missing child name, date
of birth, parent name, referral or record source may appear as a short code rather than a
sentence. Whatever the wording, the meaning is the same: something required is blank. Work
down the eight sections and look for the red asterisks.

If the save is rejected you will see **Unable to save lead. Please check the form and try
again.** or the shorter **Unable to save lead.**

**Good to know:**
Photos must be image files and under 5 MB. A wrong file type gives **Please select an image
file.** and an oversized one gives **Photo must be smaller than 5 MB.**

Both **Referral Source** and **Record Source** are required, so a lead cannot be saved
without them. Make sure those two lists are populated before your team starts taking
enquiries.

---

## How to edit a lead

**Who can do this:** Principal, or any role granted the Leads module.
**Where:** **CRM Leads** — /app/crm/leads
**Before you start:** Nothing.

**Steps:**

1. Find the lead in the list.
2. Press the amber pencil button on its row — its label is **Edit**. Alternatively open
   the lead and press the amber pencil near the top of the detail page.
3. The form opens with the heading **Edit Lead** and the child's name beneath it. Every
   field and every rule is identical to adding a lead.
4. Change what you need.
5. Press **Update** in the bottom bar.

**After you save:**
The button reads **Saving...**, then a green **Lead updated successfully.** appears and you
return to the list.

**Good to know:**
The **Second Parent/Guardian** section opens automatically when the lead already has any
second-guardian details saved.

Editing a lead does not change its stage. Stage changes are made from the stage badge, as
described next.

---

## How to change a lead's stage

**Who can do this:** Principal, or any role granted the Leads module.
**Where:** **CRM Leads** — /app/crm/leads
**Before you start:** Decide what reminder date you want, because the portal will not let
you finish without one.

**Steps:**

1. Find the lead in the list.
2. Press its stage badge, at the right-hand end of the row. A short menu opens.
3. Pick the new stage. The menu offers **New Lead**, **Book a Tour**, **Tour Taken**,
   **Offer Letter**, **Admission**, **Lost**, **Accepted** and **Rejected**.
4. A window headed **Move Lead** opens. It reads **Are you sure you want to change the
   status of the lead to** followed by the stage you picked, and shows the lead's
   **Student Name**, **Parent Name**, **Phone**, **Email** and **Grade** so you can confirm
   you have the right family.
5. Set **Set Reminder Date**. This is required — it pre-fills with today's date.
6. Optionally type into the **Admin Comment** box.
7. Optionally press **Advanced Options** to reveal **Parent Email Message**, a box with the
   placeholder **Message sent to the parent**.
8. Press **Confirm & add task**.

**The form in full:**

| Field | Required? | What to enter | Options |
|---|---|---|---|
| **Set Reminder Date** | Yes | When to be reminded about this lead | Date picker, pre-filled with today |
| **Admin Comment** | No | Internal note about the change | Long text |
| **Parent Email Message** | No | Message intended for the parent. Hidden behind **Advanced Options** | Long text |

**After you save:**
The **Confirm & add task** button is disabled until a reminder date is set, and reads
**Saving...** while it works.

Changing a stage also creates a task against the lead. That is why the button says
"& add task" and why a reminder date is compulsory. If you leave **Admin Comment** filled
but **Parent Email Message** empty, the comment text is used as the message.

On success you see **Lead moved and task added successfully.** If the stage change saved
but the parent email could not be sent, an amber warning appears instead of the green
message.

> **Not yet checked on a live system:** whether the parent actually receives an email when
> a stage changes, what that email contains, and which mailbox it comes from. The portal
> clearly distinguishes a successful send from a failed one, so email is intended here, but
> this has not been confirmed end to end. Until you have verified it with a test lead using
> your own address, do not rely on a stage change to inform a parent.

**Good to know:**
Remember that the stage you pick here is recorded under the Leads page name. Opening the
task afterwards may show **KYC** in place of **Tour Taken**, or **Evaluation** in place of
**Offer Letter**. See the stage table.

---

## How to open a lead and see its full record

**Who can do this:** Principal, or any role granted the Leads module.
**Where:** **CRM Leads** — /app/crm/leads
**Before you start:** Nothing.

**Steps:**

1. Click the child's name in the list. The detail page opens.
2. To go back, press the small **Back to leads** arrow above the child's name.

**What the detail page shows.** The left panel lists **Student Name**, **Parent Name**,
**Phone**, **Email** and **Grade**, and beneath them a boxed grid containing: **Term**,
**DOB**, **Age**, **Nationality**, **Operator**, **Expected Joining**, **Source**,
**Referral**, **Previous School**, **Inquiry Date**, **Data Verified By**, **Documents
Verified By**, **No Enroll Reason**, **Reason Explanation** and **Joining Notes**.

**Age** is calculated from the date of birth and shown as years and months, for example
"3Yr 4m". Dates are displayed day-month-year. Anything empty shows a dash.

The middle panel is **Tasks** and the right panel is **Notes**. Both are covered below.

The buttons across the top are **Send payment URL**, **Download**, **Approve**, and a red
**Delete**.

**Good to know:**
A lead with no child name recorded appears as **Unnamed lead** throughout.

The **Download** button is present on this page. Its behaviour has not been confirmed.

> **Not yet checked on a live system:** what **Download** produces — whether it is a PDF, a
> spreadsheet, or something else.

---

## How to record a tour

There is no separate "tour" screen. A tour is recorded through the stage and the notes.
The usual sequence is:

**Before the tour:**

1. Open **CRM Leads** and press the lead's stage badge.
2. Set the stage to **Book a Tour**.
3. In the **Move Lead** window set **Set Reminder Date** to the tour date, so the tour
   shows up as a reminder.
4. Put the appointment details in **Admin Comment**.
5. Press **Confirm & add task**.

**After the tour:**

1. Press the stage badge again and set the stage to **Tour Taken**.
2. Record what happened in **Admin Comment**.
3. Press **Confirm & add task**.
4. Open the lead and add a fuller write-up in the **Notes** panel, or press the amber
   **Edit** pencil and use the **Visit Notes** box in section 8, **Visit & Joining**, which
   exists for exactly this purpose.

**Good to know:**
**Visit Notes** lives on the lead itself, so it holds one account of the visit and is the
right place for the settled summary. The **Notes** panel keeps a running dated list, better
for follow-up conversations. Using both is reasonable: **Visit Notes** for the record,
**Notes** for the trail.

Remember the label difference — after you set **Tour Taken**, the task window will show
this stage as **KYC**.

---

## How to add a note to a lead

**Who can do this:** Principal, or any role granted the Leads module.
**Where:** **CRM Leads**, then open the lead — /app/crm/leads
**Before you start:** Nothing.

**Steps:**

1. Open the lead.
2. Find the **Notes** panel on the right.
3. Type into the box, placeholder **Add New Note**.
4. Press **Add Note**.

**After you save:**
The button reads **Saving...** while it works, then a green **Note added successfully.**
appears and the box clears. The note joins the dated list above with today's date.

If it fails you see **Note could not be saved.**

**To edit a note:** press the amber pencil on the note, labelled **Edit note**. The text
loads into the box, the button changes to **Update Note**, and a **Cancel** button appears.
Press **Update Note** to save — success shows **Note updated successfully.**

**To delete a note:** press the red bin on the note, labelled **Delete note**, and confirm.
Success shows **Note deleted successfully.** Failure shows **Note could not be deleted.**

**Good to know:**
**Add Note** stays disabled until you type something, so empty notes cannot be created.

Each note is stamped with the date you added it. There is no way to backdate one, so if you
are writing up a conversation from last week, say so in the text.

When there are no notes the panel reads **No notes added.**

---

## How to add a follow-up task

**Who can do this:** Principal, or any role granted the Leads module.
**Where:** **CRM Leads**, then open the lead — /app/crm/leads
**Before you start:** Nothing.

**Steps:**

1. Open the lead.
2. In the **Tasks** panel, press the round **+** button, labelled **Add Task**.
3. A window headed **Add Task** opens, with **Date** and **Set Reminder Date** already
   filled in with the current date and time.
4. Choose a **Lead Status**.
5. Adjust **Date** and **Set Reminder Date** if needed.
6. Optionally type an **Admin Comment**.
7. Optionally attach files.
8. Optionally compose a message in the formatted editor on the right.
9. Press **Add Task**.

**The form in full:**

| Field | Required? | What to enter | Options |
|---|---|---|---|
| **Lead Status** | Yes | The stage this task relates to | **New Lead**, **KYC**, **Book a Tour**, **Admission**, **Accepted**, **Evaluation**, **Registered**, **Lost**, **Rejected** |
| **Date** | Yes | Date and time of the task | Date-and-time picker, pre-filled with now |
| **Set Reminder Date** | Yes | When to be reminded | Date picker, pre-filled with today |
| **Admin Comment** | No | Internal note | Long text |
| **Attachment** | No | Click or drag files onto the panel marked **Drag & drop files here...** | Any file type, several at a time |
| *(message editor)* | No | A formatted message, on the right of the window | Rich text |

Remember that this **Lead Status** list uses the alternative labels: **KYC** here is the
same stage as **Tour Taken** on the Leads page, and **Evaluation** here is the same stage
as **Offer Letter**. **Registered** appears only in this list.

**After you save:**
If **Lead Status**, **Date** or **Set Reminder Date** is missing you get **Lead status,
date and reminder date are required.** and nothing is saved.

On success the window closes and a green **Task added successfully.** appears. If the task
saved but the parent email did not go out, you get an amber **Task saved, but the parent
email could not be sent.** instead.

If it fails outright: **Task could not be saved.**

**To edit a task:** press the blue pencil on the task, labelled **Edit task**. The window
opens headed **Edit Task** and the save button reads **Update Task**. Success shows **Task
updated successfully.** Attachments already on the task are not listed in the edit window;
any files you add are added on top.

**To delete a task:** press the bin, labelled **Delete task**, and confirm. Success shows
**Task deleted successfully.**

**Good to know:**
Attachments queue up as removable chips before you save, each with its own bin button, so
you can drop the wrong file without starting over.

When a lead has no tasks the panel reads **No tasks added.**

> **Not yet checked on a live system:** whether adding a task emails the parent. The
> portal distinguishes a successful send from a failure, so email is intended, but this has
> not been confirmed.

---

## The Tasks panel on the main Leads page

The right-hand side of the Leads list shows a **Tasks** panel headed **Today**, with
**Previous day** and **Next day** arrows either side.

It shows at most ten tasks. Each entry shows the stage badge, the lead's name, the admin
comment (or **Task added** if there is none), who it belongs to, and the date. When there
is nothing to show it reads **No tasks for today.**

Pressing the blue pencil on an entry jumps you to that lead's detail page and opens the
task for editing. If the lead cannot be found you get **CRM lead not found for this task.**

**Good to know:**
The panel is capped at ten entries, so on a busy day it is a sample rather than a complete
list. For the full picture open the lead itself.

> **Not yet checked on a live system:** whether the **Previous day** and **Next day**
> arrows change what the panel shows.

---

## How to send a templated email

There are two separate things here: editing the stored templates, and sending the
admission-form link to one parent.

### Editing the stored email templates

**Who can do this:** Principal, or any role granted the Leads module.
**Where:** **CRM Leads** — /app/crm/leads
**Before you start:** Nothing.

**Steps:**

1. Open **CRM Leads**.
2. Press **Email Templates** at the top right. The page is headed **Email Templates**, with
   the subtitle **Email templates for lead statuses**.
3. The left column is headed **Lead Status** and lists one template per stage. Click the
   stage whose template you want to change.
4. Edit the **Subject** box.
5. Edit the body in the formatted editor beneath it.
6. Press **Update**.
7. Press **Back to CRM leads** to return.

**The form in full:**

| Field | Required? | What to enter | Options |
|---|---|---|---|
| **Subject** | Yes | The email subject line | Free text |
| *(body editor)* | Yes | The message body | Rich text |

**After you save:**
The button reads **Updating...** while it works, then **Email template updated
successfully.**

An empty subject gives **Subject is required.** and an empty body gives **Template content
is required.** Failure gives **Template could not be updated.**

**Good to know:**
The stage names in the left column come from the portal's own template records, so the
wording there may differ again from both columns of the stage table above. Match them by
position and colour rather than by exact text.

Your nursery logo is shown beneath the editor as a preview of how it will appear.

If no templates are set up, the page reads **No email templates found.**

> **Not yet checked on a live system:** when these saved templates are actually used —
> whether they are sent automatically on a stage change, or only ever sent manually.

### Sending the admission form link to one parent

**Who can do this:** Principal, or any role granted the Leads module.
**Where:** **CRM Leads**, then open the lead — /app/crm/leads

**Steps:**

1. Open the lead.
2. Press **Send payment URL** at the top left of the detail page.
3. A window headed **Send Form URL to Parent** opens.
4. **Parent Email** is filled in from the lead and cannot be typed into. If the lead has no
   email, it shows the placeholder **Parent email not available**.
5. Check the **Subject**, which is pre-filled as **Admission Form**.
6. Review the pre-written message in the editor. It is addressed to the parent by name,
   mentions the child by name, includes a link to the admission form, and is signed off
   with the nursery logo.
7. Press **Send Email**.

**After you press Send Email — read this before using it:**

This button does not send anything. Whatever you type, pressing **Send Email** produces the
message **Payment URL email API is not available yet.** and the window stays open.

This is stated plainly in the portal itself, not inferred. Sending from this window is not
available in the version you are running.

To get the admission form to a parent today, copy the link out of the message body and send
it from your own email. The rest of the window is still useful as a template: open it,
copy the wording, paste it into your mail client.

Two checks happen before that message appears. With no parent email you get **A valid
parent email address is required.** With an empty subject or body you get **Subject and
message are required.**

---

## What happens at the end of the pipeline

Two actions sit at the end: **Approve**, and moving a lead to a final stage.

### Approving a lead

**Steps:**

1. Open the lead.
2. Press the green **Approve** button at the top right.

While it works the button reads **Approving...**. On success you see **Lead approved
successfully.** and the button changes to read **Approved** and becomes unavailable, since
the lead is already approved. On failure: **Lead could not be approved.**

Approving sets the lead to the **Accepted** stage.

### The point to plan for: no child record is created

Reaching the final stage of the admissions pipeline does not create a child record.
Approving a lead does not create one either.

A lead and a child are separate records. Approving marks the enquiry as successful; it
does not enrol anybody. **The child must be added separately** on the **Children** page
before you can mark attendance, assign a class, record observations or raise an invoice for
that family.

This is how the portal is built, not a step you have missed. Build it into your admissions
routine:

1. Approve the lead, or move it to **Accepted** / **Admission**.
2. Go to the **Children** page and add the child, re-entering the details from the lead.
3. Carry on with classes, attendance and billing from the child record.

Plan for the re-keying. Before you approve, open the lead's detail page and keep it open,
or note down the child's name, date of birth, nationality, guardian names, phone numbers,
email addresses, address and emergency contact. You will need all of it again.

> **Not yet checked on a live system:** whether any automatic transfer to a child record
> exists elsewhere in the portal. Nothing on the Leads page performs one, so treat manual
> re-entry as the process.

---

## How to delete a lead

**Who can do this:** Principal, or any role granted the Leads module.
**Where:** **CRM Leads** — /app/crm/leads
**Before you start:** Consider moving the lead to **Lost** or **Rejected** instead. Those
stages keep the history and keep the family in your reporting. Deleting removes the row.

**Steps:**

1. Find the lead in the list, or open it.
2. Press the red bin button, labelled **Delete**.
3. Confirm when asked. The confirmation names the child so you can check you have the right
   one.

**After you save:**
Success shows **Lead deleted successfully.** Failure shows **Unable to delete lead.**

> **Not yet checked on a live system:** whether deleting a lead also removes its notes,
> its tasks and its attachments. Assume it does and that the deletion cannot be undone.

---

# Part 3 — Referrals & Sources

## What these two lists are

This page maintains the two dropdowns that every lead must use.

**Referrals** answers "what brought this family to us" — a specific campaign, sign, event
or recommendation. Each referral also carries a **Type** that groups it.

**Communication Sources** answers "through which channel did the enquiry arrive". Each
source carries a **Type** too.

Both appear on the lead form as required fields: **Referral Source** and **Record Source**
in section 7, **Enquiry Details**. A lead cannot be saved without one of each. Populate
both lists before your team starts taking enquiries.

## Who can open this page

**Principal and Admin only.** This is fixed. Granting the permission to a Registrar or any
other role does not let them in, and the link does not appear in their sidebar.

Plan around it: if your front-desk team takes enquiries but cannot add referrals, agree a
routine where they ask a Principal or Admin to add new ones, rather than discovering the
gap mid-enquiry with a parent waiting.

## What the page shows

**Where:** **Referrals & Sources**, in the **Admissions CRM** group —
/app/crm/referrals-sources

The page is titled **Referrals & Communication Sources**, with a count beneath reading the
number of **referrals**.

Across the top is a row of five cards showing your five most-used referrals, ranked by how
many leads name each one, with the count on each card. This is a quick read on which
channels are working. Empty cards read **No referral**.

Below that are two side-by-side lists: **Referrals** on the left and **Communication
Sources** on the right. Each has its own search box and its own round **+** button. Each
row is numbered and carries an amber **Edit** pencil and a red **Delete** bin. Referral
rows also show their **Type** as an amber tag.

---

## How to add a referral

**Who can do this:** Principal and Admin only.
**Where:** **Referrals & Sources** — /app/crm/referrals-sources
**Before you start:** Nothing.

**Steps:**

1. Open **Referrals & Sources**.
2. Press the round **+** button on the **Referrals** list, labelled **Add referral**.
3. A window headed **Add Referral** opens.
4. Type a **Name**.
5. Choose a **Type**.
6. Press **Add**.

**The form in full:**

| Field | Required? | What to enter | Options |
|---|---|---|---|
| **Name** | Yes | What staff will see in the lead form dropdown | Free text |
| **Type** | Yes | The category | **Digital**, **Printed**, **Signs**, **Recommendation**, **Event**, **Others**. Starts on **Digital** |

**After you save:**
Success shows **Added successfully.** and the window closes. An empty name gives **Referral
name is required.** and nothing is saved. A rejected save gives **Could not save the
record.**

**Good to know:**
The **Name** is what your team picks from the lead form, so write it the way they will
recognise it. "Instagram campaign March" beats "IG-03".

---

## How to add a communication source

**Who can do this:** Principal and Admin only.
**Where:** **Referrals & Sources** — /app/crm/referrals-sources

**Steps:**

1. Press the round **+** button on the **Communication Sources** list, labelled **Add
   communication source**.
2. A window headed **Add Communication Source** opens.
3. Type a **Name**.
4. Choose a **Type**.
5. Press **Add**.

**The form in full:**

| Field | Required? | What to enter | Options |
|---|---|---|---|
| **Name** | Yes | What staff will see in the dropdown | Free text |
| **Type** | Yes | The category | **General**, **Admission**, **Communication**. Starts on **General** |

**After you save:**
Success shows **Added successfully.** An empty name gives **Communication source name is
required.**

---

## How to edit a referral or a source

**Who can do this:** Principal and Admin only.
**Where:** **Referrals & Sources** — /app/crm/referrals-sources

**Steps:**

1. Find the entry. Each list has its own search box, placeholder **Search...**
2. Press the amber pencil on its row.
3. The window opens headed **Edit Referral** or **Edit Communication Source**, pre-filled.
4. Change the **Name**, the **Type**, or both.
5. Press **Save Changes**.

**After you save:**
Success shows **Updated successfully.** Failure shows **Could not save the record.**

**Good to know:**
Renaming an entry changes the label everywhere it is used, including on leads already
recorded against it. That is usually what you want — it keeps history consistent — but it
does mean a rename is not a way to separate old leads from new ones. To do that, add a new
entry and leave the old one alone.

---

## How to delete a referral or a source

**Who can do this:** Principal and Admin only.
**Where:** **Referrals & Sources** — /app/crm/referrals-sources
**Before you start:** Check the ranking cards at the top of the page. If the entry appears
there with a count, leads are using it.

**Steps:**

1. Find the entry.
2. Press the red bin on its row.
3. Confirm when asked. The confirmation names the entry.

**After you save:**
Success shows **Deleted successfully.** Failure shows **Could not delete the record.**

> **Not yet checked on a live system:** what happens to leads already recorded against a
> deleted referral or source — whether they keep the old name, show a blank, or block
> editing until a new value is chosen. Because both fields are required on the lead form,
> deleting an entry that is in use may make those leads awkward to edit later.

Given that, prefer to leave unused entries in place unless the list has become genuinely
unwieldy. If you must delete, check the ranking cards first and search the Leads page using
the **Referral** or **Source** filter to see what is attached.

**Good to know:**
When a list is empty it reads **No referrals found** or **No communication sources found**.
While loading it reads **Loading...**

---

# Part 4 — Roles & Access

## Who can open this page

**Principal and Admin only.** Fixed, and not affected by any permission setting.

**Where:** **Roles & Access**, in the **Reports & Admin** group — /app/roles

The page is titled **Roles & permissions**, with the subtitle **Manage roles and
active-center module access.** and a **Total roles** count.

---

## How to create a role

**Who can do this:** Principal and Admin only.
**Where:** **Roles & Access** — /app/roles
**Before you start:** Decide what the role should be able to open. You grant that in a
second step, after the role exists.

**Steps:**

1. Open **Roles & Access**.
2. Press **Add role**. A window opens headed **New role** with the title **Create a role**.
3. Type a **Role name**.
4. Leave **Status** as **Active**, or set it to **Inactive**.
5. Press **Create role**.

**The form in full:**

| Field | Required? | What to enter | Options |
|---|---|---|---|
| **Role name** | Yes | What the role is called | Free text |
| **Status** | No | Whether the role is in use | **Active**, **Inactive**. Starts on **Active** |

**After you save:**
The button shows a spinner while it works. On success the window closes and a green
confirmation appears. An empty name gives **Role name is required.** A rejected save gives
**Unable to save role.** or **Request failed.**

**Good to know:**
A new role starts with no modules granted, so it can open almost nothing until you complete
the next procedure.

---

## How to grant a role access to modules

**Who can do this:** Principal and Admin only.
**Where:** **Roles & Access** — /app/roles
**Before you start:** The role must already exist.

**Steps:**

1. Open **Roles & Access**.
2. Find the role. There is a search box with the placeholder **Search roles…**
3. Press **Manage access** on the role, or click the role's name. A panel opens on the
   right headed **Access assignment** with the role's name beneath it.
4. The panel lists every module your nursery has, arranged in groups. Beneath the role name
   a counter reads how many of the total are selected.
5. Click a module to tick it. Click again to untick. A ticked module is highlighted and
   carries a check mark.
6. Use **Select all** to tick everything, or **Clear all** to tick nothing.
7. Press **Save access**.
8. Press **Close** to shut the panel.

**After you save:**
The button shows a spinner while it works, then a green confirmation appears and the ticks
refresh to match what was stored. Failure gives **Unable to save role access.** or
**Request failed.**

If the panel shows **No enabled modules found for the active center.** there is nothing to
grant, which usually points to the nursery's subscription rather than to the role.

**Good to know — three things that will otherwise surprise you:**

**Granting the Centers module has no effect.** **Centers** is Principal-only. The tick will
save, and it will still not let the person in. Do not use it to give a deputy access to
nursery records — grant **My Center** instead.

**Granting Roles & Access or Referrals & Sources has no effect either**, for the same
reason. Those two are Admin-only. If someone needs them, they need the Admin role.

**The change takes effect on what the person can open, and on what they can see in the
menu.** Menu links appear and disappear with the permission. Ask the person to sign out and
back in before concluding that a change did not work.

**Good to know — planning:**
Grant the minimum that lets someone do their job, then add more when they ask. That is
easier to reason about than starting with **Select all** and removing things, and it avoids
briefly exposing records that a role should never have seen.

---

## How to rename a role or change its status

**Who can do this:** Principal and Admin only.
**Where:** **Roles & Access** — /app/roles

**Steps:**

1. Find the role.
2. Press the pencil button on its row, labelled **Edit**. The window opens headed **Edit
   role** with the current name as its title.
3. Change the **Role name**, the **Status**, or both.
4. Press **Update role**.

There is also a quicker route for status alone: press the small coloured dot button on the
role's row, labelled **Toggle status**. It flips **Active** to **Inactive** and back
without opening the window. The dot is green when the role is **Active** and grey when it
is **Inactive**.

**After you save:**
Success shows a green confirmation. Failure gives **Unable to save role.** for the window,
or **Unable to update status.** for the dot.

**Good to know:**
Each role's row shows its status and its ID number, in the form **Active · ID 4**. Quote
that ID when raising a support query — it is unambiguous in a way that a name is not.

> **Not yet checked on a live system:** what setting a role to **Inactive** does to people
> already assigned to it — whether they are locked out immediately, at next sign-in, or not
> at all. Until that is confirmed, do not rely on **Inactive** as a way to suspend
> somebody's access.

---

## How to delete a role

**Who can do this:** Principal and Admin only.
**Where:** **Roles & Access** — /app/roles
**Before you start:** Make sure nobody is using the role. Consider setting it to
**Inactive** first and waiting, rather than deleting outright.

**Steps:**

1. Find the role.
2. Press the red bin button on its row, labelled **Delete**.
3. Confirm when asked. The confirmation names the role.

**After you save:**
Success shows a green confirmation. If the access panel was open for that role, it closes.
Failure gives **Unable to delete role.**

> **Not yet checked on a live system:** what happens to staff accounts assigned to a
> deleted role — whether they lose all access, keep what they had, or block sign-in. Treat
> deleting a role in use as risky and check who holds it first.

---

# Part 5 — My Center

This is where a nursery changes its own details. It has two tabs: **Center Details** and
**Sessions**.

**Who can do this:** Principal, or any role granted the My Center module.
**Where:** **My Center**, in the **Center** group — /app/my-center

---

## How to update your nursery's details

**Where:** **My Center**, the **Center Details** tab
**Before you start:** Have your logo file ready if you are changing it.

**Steps:**

1. Open **My Center**.
2. Make sure the **Center Details** tab is selected. It is the one shown first.
3. Work down the sections and change what you need.
4. Press **Update** at the bottom.

**The form in full.** The tab is arranged in seven blocks.

### Basic information (no heading)

| Field | Required? | What to enter | Options |
|---|---|---|---|
| **Center Name** | Yes | The nursery's name | Free text |
| **Contact Title** | Yes | Job title of the main contact | Free text |
| **Contact Name** | Yes | Name of the main contact | Free text |
| **Capacity** | No | How many children the nursery can take | Free text |
| **Center Description** | Yes | A description of the nursery | Long text |

### Contacts

| Field | Required? | What to enter | Options |
|---|---|---|---|
| **Phone 1** | Yes | Main phone number | Free text |
| **Phone 2** | No | Second number | Free text |
| **Phone 3** | No | Third number | Free text |
| **Fax 1** | No | Fax number | Free text |
| **Fax 2** | No | Second fax | Free text |
| **Fax 3** | No | Third fax | Free text |
| **Email 1** | Yes | Main email address | Free text |
| **Email 2** | No | Second email | Free text |
| **Email 3** | No | Third email | Free text |

### Social Media

All six are optional free text.

| Field | Required? | What to enter |
|---|---|---|
| **Website** | No | Your website address |
| **Facebook** | No | Facebook page address |
| **Twitter** | No | Twitter address |
| **Instagram** | No | Instagram address |
| **YouTube** | No | YouTube channel address |
| **Cloud Folder** | No | A shared cloud folder address |

### Address

| Field | Required? | What to enter | Options |
|---|---|---|---|
| **Country** | Yes | The country | Dropdown. Empty option reads **--Select--** |
| **Currency Code** | No | Currency for invoices and fees | Dropdown. Empty option reads **--Select--** |
| **GMT Timezone** | Yes | Your offset from GMT | Free text |
| **Address** | Yes | The nursery's address | Free text |

While the lists load, the dropdowns read **Loading countries...** and **Loading
currencies...**

### Center Logo

Marked required with a red asterisk.

Drag an image onto the dashed panel, which reads **Drag & drop logo here ...**, or click it
to browse. There is also a **Browse ...** button beside a read-only box showing the chosen
file name, placeholder **Select file ...**

Once a logo is loaded, a small magnifier button enlarges it, and an **×** in the corner
removes it.

### Financial

| Field | Required? | What to enter | Options |
|---|---|---|---|
| **VAT TRN Number** | No | Your VAT registration number | Free text |
| **Payment Details** | No | Bank details shown to parents | Long text |

### Map

| Field | Required? | What to enter | Options |
|---|---|---|---|
| **Latitude** | No | Latitude of the nursery | Free text |
| **Longitude** | No | Longitude of the nursery | Free text |

**After you save:**
The button reads **Saving...** while it works, then **Center updated successfully**.

If a required field is empty, nothing saves and a message names the first one, in the form
"Center Name is required." — the field is also outlined in red. Nine fields are required:
**Center Name**, **Contact Title**, **Contact Name**, **Center Description**, **Phone 1**,
**Email 1**, **Country**, **GMT Timezone** and **Address**.

If the nursery record cannot be identified you get **Center id not found. Please refresh
and try again.** A rejected save gives **Failed to update center**.

**Good to know:**
**Update** saves the whole tab at once, not one section at a time. Work through everything
you want to change, then press it once.

The words **Update Center** appear in blue above the first block. That is a heading, not a
button — the button that saves is **Update** at the bottom.

---

## How to add a session

Sessions are the named parts of your nursery day — a morning session, an afternoon session,
a full day — each with a start and end time.

**Where:** **My Center**, the **Sessions** tab

**Steps:**

1. Open **My Center**.
2. Press the **Sessions** tab.
3. The right-hand panel is headed **Add Session**.
4. Type a **Session Name**.
5. Set **From Time**.
6. Set **To Time**.
7. Leave **Status** switched on for **Active**, or switch it off for **Not Active**.
8. Press **Save**.

**The form in full:**

| Field | Required? | What to enter | Options |
|---|---|---|---|
| **Session Name** | Yes | What the session is called | Free text |
| **From Time** | Yes | Start time | Time picker |
| **To Time** | Yes | End time. Must be later than **From Time** | Time picker |
| **Status** | No | Whether the session is in use | On/off switch, reads **Active** or **Not Active**. Starts **Active** |

**After you save:**
The button reads **Saving...** while it works, then **Session saved successfully.**

A missing field gives a message naming the first one, such as "Session name is required."
If **To Time** is not later than **From Time** you get **To time must be after from time.**
and nothing saves. A rejected save gives **Session could not be saved.** or **Failed to
save session.**

**Good to know:**
The list on the left shows **Session Name**, **From Time**, **To Time** and **Status**, ten
rows at a time, with page arrows beneath when there are more. When there are none it reads
**No sessions yet**.

---

## How to edit or delete a session

**Where:** **My Center**, the **Sessions** tab

**To edit:**

1. Press the pencil button on the session's row in the left-hand list.
2. The right-hand panel changes its heading to **Edit Session** and fills with that
   session's values.
3. Change what you need.
4. Press **Update**.
5. To abandon the edit, press **Cancel**, which appears next to **Update** while editing.

Success shows **Session updated successfully.**

**To delete:**

1. Press the red bin button on the session's row.
2. Confirm when asked.

Success shows **Session deleted successfully.** Failure gives **Session could not be
deleted.** or **Failed to delete session.** If you were editing that session at the time,
the form clears.

**Good to know:**
Both buttons are disabled while a save or delete is in progress, so double-clicking cannot
run the action twice.

> **Not yet checked on a live system:** what happens to attendance already recorded against
> a deleted session. Setting a session to **Not Active** is the more cautious way to retire
> one.

---

# Part 6 — Centers

## What it is and who can open it

**Centers** is the multi-nursery administration page. It lists every nursery in the
organisation and lets an administrator create new ones, edit them, and delete them. It also
covers each nursery's licence dates and administrator account.

**Who can do this:** Principal only.
**Where:** **Centers**, in the **Center** group — /app/centers

The page is titled **Centers**, with the eyebrow **Root administration** and the subtitle
**Manage every center and its administrator account.**

This is a stricter restriction than the others in this document. **Centers** is
Principal-only, and granting its permission to another role has no effect — the person
still cannot open it and the link still does not appear in their sidebar.

If you are not a Principal you will not see **Centers** in your menu, and that is expected.
The page you want is **My Center**, which lets a nursery manage its own details.

## What it contains, in outline

Because access is restricted to the Principal, this section is an outline rather than a
procedure.

The main screen is a searchable, paged table with the columns **Actions**, **Center**,
**Contact**, **Currency**, **Capacity**, **Phone** and **Admin**, a **Total centers** count,
and a **New center** button. When empty it reads **No centers found.**

Creating or editing a nursery opens a form in seven sections: **Center details**,
**Contacts**, **Social media**, **Address & regional settings**, **Center logo**,
**Financial**, and **License & center administrator**.

Two things appear here that **My Center** does not offer: a **Zone** field in the address
section, and the whole **License & center administrator** section, which holds **License
Start Date**, **License Expiry Date**, **Admin Username** and **Admin Password**. The
financial section also adds **Establishment # for WPS** and **Bank Code for WPS** alongside
the **VAT TRN Number** and **Payment Details** that My Center has.

Logos here must be JPG or PNG and no larger than 2 MB — the page states **JPG or PNG,
maximum 2 MB**, and rejects others with **Logo must be a JPG or PNG image.** or **Logo must
not exceed 2 MB.**

**Good to know:**
Day-to-day nursery settings belong in **My Center**. Use **Centers** only for organisation
-level work: opening a new nursery, renewing a licence, or changing a nursery's
administrator account.

---

# Part 7 — Packages

## What this is in business terms

**Packages** is your nursery's subscription to the portal itself. It is not about fees you
charge parents — those live in the finance pages.

A package sets how many children your portal can hold and which modules are switched on.
You buy in units: each package unit covers a fixed number of children, and buying several
units multiplies that capacity. You also choose how many months to subscribe for. The price
shown is per package unit per month, and the total is that price multiplied by the number of
units and the number of months.

**Who can do this:** Principal, or any role granted the Packages module.
**Where:** **Packages**, in the **Center** group — /app/packages

---

## What you can do here

**Steps to view your current subscription:**

1. Open **Packages**.
2. A badge at the top right shows your subscription state, or **No subscription** if you
   have none.
3. If you have a subscription, three cards appear showing **Valid until**, **Children
   limit**, and **Package units**.

**Steps to compare packages:**

1. Scroll to the cards below. Each shows the package name, how many **children per package
   unit** it covers, the price with **/ package / month** beside it, a description, and a
   ticked list of the modules it includes.
2. One card may carry a **Popular** badge.

**Steps to buy a package:**

1. Press **Select package** on the one you want.
2. The purchase screen opens, headed **Purchase** followed by the package name, with the
   subtitle **Choose capacity and subscription period, then complete secure payment.**
3. Set **Start date**, **Number of months** and **Package units**.
4. Fill in the card details.
5. Check the **Order summary** panel on the right, then press the **Pay** button, which
   shows the total.
6. To go back without buying, press **Back to packages**.

**The form in full:**

| Field | Required? | What to enter | Options |
|---|---|---|---|
| **Start date** | Yes | When the subscription should begin | Date picker, starts at today |
| **Number of months** | Yes | How long to subscribe for | A number from 1 to 60. Starts at 12 |
| **Package units** | Yes | How many units to buy | A number from 1 to 100. Starts at 1 |
| **Name on card** | Yes | Name as printed on the card | Free text |
| **Card number** | Yes | The long card number | Free text |
| **Expiry month** | Yes | Two digits | Placeholder **MM** |
| **Expiry year** | Yes | Four digits | Placeholder **YYYY** |
| **Security code** | Yes | The code on the card | Placeholder **CVC** |

The **Order summary** panel updates as you type and shows **Children capacity**,
**Subscription period**, **End date** and **Total**.

**After you save:**
The button reads **Processing...** while it works, then **Package purchased successfully.**
and you return to the package list.

Missing card details give **Please complete all card details.** A declined or failed
purchase gives **Package purchase failed.** If the payment service cannot be reached you
get **Could not load the secure payment service.**, and if it is not configured, **Stripe
publishable key is not configured.**

**Good to know:**
If you already have a valid or pending subscription, the **Select package** buttons and the
**Pay** button are disabled, and a note reads **Your center already has a valid or pending
subscription.** You cannot accidentally buy twice.

Card details go directly to the payment provider for tokenisation — the page states **Card
details are sent directly to Stripe for tokenization.** The portal does not store the card
number.

**Children capacity** is units multiplied by the children each unit covers. If your package
covers 15 children per unit and you buy 3 units, that is 45 children. Check this against
your actual roll before buying, and leave headroom for the year ahead.

> **Not yet checked on a live system:** what happens when a subscription expires — whether
> the portal locks, becomes read-only, or keeps working with a warning. Renew before the
> **Valid until** date rather than finding out.

---

# Appendix — Messages you may see

Grouped by where they appear. All are the portal's exact English wording.

## Leads

| Message | What it means |
|---|---|
| **New lead saved successfully.** | The lead was created. |
| **Lead updated successfully.** | Your edits were saved. |
| **Unable to save lead.** | The save was rejected. Check the form. |
| **Lead deleted successfully.** | The lead is gone. |
| **Unable to delete lead.** | The deletion did not happen. |
| **Lead moved and task added successfully.** | The stage changed and a task was created. |
| **Lead status could not be changed.** | The stage change did not save. |
| **Reminder date is required.** | Set **Set Reminder Date** before confirming. |
| **Lead approved successfully.** | The lead is now **Accepted**. |
| **Lead could not be approved.** | The approval did not save. |
| **No leads match these filters.** | A filter is hiding rows. Press **Reset**. |
| **No leads found.** | There are no leads at all. |
| **Unnamed lead** | The lead has no child name recorded. |

## Tasks and notes

| Message | What it means |
|---|---|
| **Task added successfully.** | The task was created. |
| **Task updated successfully.** | Your edits were saved. |
| **Task deleted successfully.** | The task is gone. |
| **Task saved, but the parent email could not be sent.** | The task saved; the email did not go out. |
| **Lead status, date and reminder date are required.** | Fill all three before saving. |
| **Note added successfully.** | The note was created. |
| **Note updated successfully.** | Your edits were saved. |
| **Note deleted successfully.** | The note is gone. |
| **No tasks added.** / **No notes added.** | This lead has none yet. |
| **No tasks for today.** | Nothing in the daily task panel. |
| **CRM lead not found for this task.** | The task's lead could not be located. |

## Email

| Message | What it means |
|---|---|
| **Payment URL email API is not available yet.** | **Send Email** does not send. Copy the link and send it yourself. |
| **A valid parent email address is required.** | The lead has no email address. |
| **Subject and message are required.** | Fill both before sending. |
| **Email template updated successfully.** | The template was saved. |
| **Template could not be updated.** | The template did not save. |
| **No email templates found.** | No templates are set up. |

## Referrals and sources

| Message | What it means |
|---|---|
| **Added successfully.** / **Updated successfully.** / **Deleted successfully.** | The action worked. |
| **Referral name is required.** | Type a name. |
| **Communication source name is required.** | Type a name. |
| **Could not save the record.** / **Could not delete the record.** | The action was rejected. |
| **No referrals found** / **No communication sources found** | The list is empty. |

## Roles

| Message | What it means |
|---|---|
| **Role name is required.** | Type a name. |
| **Unable to save role.** | The role did not save. |
| **Unable to save role access.** | The module ticks did not save. |
| **Unable to update status.** | The **Active**/**Inactive** flip did not save. |
| **Unable to delete role.** | The role was not deleted. |
| **No roles found.** | No roles match your search. |
| **No enabled modules found for the active center.** | Nothing to grant. Check the subscription. |

## My Center

| Message | What it means |
|---|---|
| **Center updated successfully** | The details tab saved. |
| **Failed to update center** | The save was rejected. |
| **Center id not found. Please refresh and try again.** | Reload the page and retry. |
| **Session saved successfully.** / **Session updated successfully.** / **Session deleted successfully.** | The action worked. |
| **To time must be after from time.** | Fix the times. |
| **No sessions yet** | No sessions are set up. |

## Packages

| Message | What it means |
|---|---|
| **Package purchased successfully.** | The purchase went through. |
| **Package purchase failed.** | The purchase did not complete. |
| **Please complete all card details.** | A card field is blank. |
| **Could not load the secure payment service.** | The payment provider could not be reached. |
| **Your center already has a valid or pending subscription.** | You cannot buy again yet. |
| **No subscription** | No active subscription. |
