# Messages, Calendar and Live Dashboard

Procedures for nursery staff using the Peekaboo portal at https://peek.peek-a-boo.app.

Everything written in plain text below was read directly from the software. Anything that could not
be confirmed from the software is marked with a **Not yet checked on a live system** note.

---

## Part 1 — Messages

### What this feature actually is

Messages is a **publishing tool**. You write an item, choose which children it is for, and publish it
to those children's families. The portal keeps a searchable history of everything you have published.

It is important to understand the shape of this feature before you use it:

- It is **one-way**. You publish outward to families.
- There is **no inbox**. Nothing from a parent arrives here.
- There is **no reply**. Neither you nor a parent can respond to a published item inside this screen.
- There is **no read receipt**. The screen does not show whether a parent has opened or seen an item.
- The only status the screen tracks is **Published** or **Unpublished** — that is, whether *you* have
  released the item, not whether anyone has received it.

So treat Messages the way you would treat a noticeboard or a newsletter mailing: use it to put
information out, and use the phone, email or a face-to-face conversation when you need a reply.

The page heading is **Communication**, with the small label **NOS** above it. The sidebar entry that
takes you there is **Messages**.

Directly under the heading the page shows a running count in the form
`<number> items · <number> published on this page`.

### The six message types

Messages has six types. Each one is a button across the top of the page, and each one also appears as
an option in the history filter. The exact on-screen labels are:

| Type label | What it is used for in the software |
| --- | --- |
| **Announcement** | General notice. Simplest form — no dates. |
| **Notification** | Notice that can be pinned to the top. |
| **Event** | The only type with start/end date and time fields and a **Fees** box. |
| **Newsletter** | Notice built around an attached document. |
| **Media** | One or more JPG/PNG images. |
| **Video Media** | A single video file. |

Clicking any of these six buttons does **two** things at once, which surprises people the first time:

1. It opens the compose window for that type, and
2. It sets the history list below to filter on that same type.

Each button also carries a small number badge showing how many items of that type are in the history
list you are currently looking at.

---

### How to publish an Announcement, Notification, Newsletter, Media or Video Media item

**Who can do this:** Staff whose role grants the *Communication* or *Console* permission. Without it
the Messages page is not reachable.

**Where:** Sidebar group **Communication** → **Messages**. URL: `https://peek.peek-a-boo.app/app/messages`

**Before you start:**
- Know which children the item is for. You **must** select at least one child — the item cannot be
  saved otherwise.
- Have any image, document or video file ready and within the size limits listed further below.

**Steps:**

1. Open **Messages** from the sidebar.
2. Click the type you want along the top: **Announcement**, **Notification**, **Newsletter**,
   **Media** or **Video Media**. The compose window opens, headed **Create** followed by the type
   name.
3. Under **Select Classes**, click one or more class circles. This is a filter, not the recipient
   list — see "How recipients are chosen" below.
4. Under **Children**, tick each child the item is for. You can use **Select All** to tick every
   child currently listed, or **Unselect All** to clear them.
5. Fill in **Title**. This is required.
6. Fill in **Description** if you want a body. This is a rich text box.
7. Fill in **URL** if you want to include a link.
8. Attach files if the type supports them (see the attachment table below).
9. Leave **Publish later** switched **off** to publish straight away. Switch it **on** to save the
   item without publishing it.
10. For **Notification** only, switch **Pin to Top** on if you want the item pinned.
11. Click **Publish Now**.

**The form in full:**

| Field | Required? | What to enter | Options |
| --- | --- | --- | --- |
| **Select Classes** | No | Click class circles to narrow the children list below | Your nursery's classes |
| **Children** | **Yes — at least one** | Tick each child the item is for | **Select All** / **Unselect All** |
| **Icon** | No | A small image shown with the item | Announcement, Notification, Newsletter only |
| **Attachment** | No | A document or file to attach | Announcement, Notification, Newsletter only |
| **Title** | **Yes** | The headline. Placeholder reads `Enter title...` | Free text |
| **Description** | No | The body text | Rich text editor |
| **URL** | No | A web link. Placeholder reads `https://...` | Free text |
| **Media images** | No | JPG/PNG images | **Media** type only. Multiple allowed |
| **Video** | **Yes for Video Media** | One video file | **Video Media** type only |
| **Publish later** | No | Off = publish now. On = save unpublished | On/Off switch |
| **Pin to Top** | No | Pins the item | **Notification** type only |

**After you save:**

- On success a green confirmation appears reading **Created successfully**, and the compose window
  closes.
- If you left **Title** empty, the item is not saved and a message reads **Title is required.**
- If you ticked no children, the item is not saved and a message reads
  **Please select at least one child.**
- On a **Video Media** item with no video chosen, a message reads
  **Please select a video before submitting.**
- If the save fails for another reason, a message reads **Create failed** or **Failed**.

> **Not yet checked on a live system:** whether families actually receive the item, how it reaches
> them (in-app, email, push notification, or some combination), how quickly it arrives, and what it
> looks like at their end. The portal screen confirms only that the item was saved and marked
> published. It does not report delivery. Confirm with a test item to a single child of a colleague's
> family before relying on this for anything urgent.

**Good to know:**
- **Publish later** is a save-without-publishing switch. It is *not* a scheduler — the form has no
  "publish on this date" box for these five types. An item saved this way stays unpublished until you
  edit it and publish it.
- Unpublished items are hidden from the history list by default. Switch the **Unpublished** toggle on
  above the history list to see them.

---

### How to publish an Event message

**Who can do this:** Staff with the *Communication* or *Console* permission.

**Where:** Sidebar group **Communication** → **Messages**, then the **Event** button.
URL: `https://peek.peek-a-boo.app/app/messages`

**Before you start:** Have the event's start and end date and time to hand.

**Steps:**

1. Open **Messages** and click **Event**.
2. Choose classes under **Select Classes**, then tick children under **Children**.
3. Enter the **Title**. Required.
4. Enter the **URL** if there is a booking or information link.
5. Enter the **Description**.
6. Attach an **Icon** and an **Attachment** if you want them.
7. Enter a figure in **Fees** if the event has a cost.
8. Set **Start Date / Time** — a date box and a time box side by side.
9. Set **End Date / Time** — likewise.
10. Leave **Publish later** off to publish now.
11. Click **Publish Now**.

**The form in full:**

| Field | Required? | What to enter | Options |
| --- | --- | --- | --- |
| **Select Classes** | No | Narrows the children list | Your nursery's classes |
| **Children** | **Yes — at least one** | Tick each child | **Select All** / **Unselect All** |
| **Icon** | No | Small image for the item | Single file |
| **Attachment** | No | Document or file | Single file |
| **Title** | **Yes** | Event name | Free text |
| **URL** | No | Link. Placeholder `https://...` | Free text |
| **Description** | No | Event details | Rich text editor |
| **Fees** | No | A number. Placeholder reads `Enter fees...` | Numbers, zero or above |
| **Start Date / Time** | No | Date plus time | Date picker and time picker |
| **End Date / Time** | No | Date plus time | Date picker and time picker |
| **Publish later** | No | Off = publish now | On/Off switch |

**After you save:** the same confirmations as above — **Created successfully** on success,
**Title is required.** or **Please select at least one child.** if something is missing.

**Good to know:**
- An Event message and a Calendar event are **two separate things**. Creating an Event message here
  does not place anything on the Calendar screen, and creating a Calendar event does not appear here.
  If you need both, create both.
- If you leave the time boxes empty but set dates, the times are recorded as `00:00`.
- The **Fees** box accepts a figure, but be aware it behaves differently from the other fields on this
  form — treat it as informational and record the real charge through the Finance screens.

---

### How recipients are chosen

This is the part most worth reading carefully, because the two selectors do different jobs.

- **Select Classes** is a **filter**. Clicking classes narrows the **Children** list underneath to
  just the children in those classes. If you select no classes at all, the **Children** list shows
  every child.
- **Children** is the **actual recipient list**. Only the children you tick receive the item.

The consequences of this are worth spelling out:

- Selecting a class **does not** by itself send to that class. You must still tick the children.
- To send to a whole class: click the class, then click **Select All** to tick every child in it.
- To send to everyone: select **no** classes, then click **Select All**. Note this ticks every child
  shown in the list at that moment.
- To send to individual children: tick just those children. You can tick children across several
  classes by selecting those classes first.
- Changing your class selection **clears every child you had already ticked**. Choose your classes
  first, then tick children — not the other way round.
- If a class has no children, the list shows **No children available**.

---

### Attachments, images and video — exact limits

Different message types accept different files. These are the limits enforced by the portal:

| Type | Upload box | Accepted file types | Size limit | Number of files |
| --- | --- | --- | --- | --- |
| Announcement | **Icon** | Any file | No limit enforced | One |
| Announcement | **Attachment** | Any file | No limit enforced | One |
| Notification | **Icon**, **Attachment** | Any file | No limit enforced | One each |
| Event | **Icon**, **Attachment** | Any file | No limit enforced | One each |
| Newsletter | **Icon**, **Attachment** | Any file | No limit enforced | One each |
| Media | **Media images** | JPG and PNG only | **1 MB per image** | Several |
| Video Media | **Video** | MP4, WebM, OGG, MOV | **35 MB** | One only |

Helper text shown under the upload boxes:

- Media images: **Select one or more JPG/PNG images. You can add more after selecting.**
- Video: **Select one MP4, WebM, OGG, or MOV video (max 35 MB).**

Every upload box shows **Drag & drop files here...** until you choose something. Once files are
chosen, a multi-file box shows `<number> file(s) selected`.

**The exact upload error wording.** If a file is over the limit, the upload is rejected and a message
appears in this exact form — the file's own name, then a space, then the fixed phrase:

> `holiday-photo.jpg exceeds the size limit.`

The fixed part is always **exceeds the size limit.** The file is not attached and the box is cleared.
If you are attaching several images at once and any single one is too big, **none** of them are
attached — reduce or remove the oversized file and choose them again.

**Good to know:**
- The 1 MB limit on Media images is small for a modern phone photo. Expect to resize before
  uploading.
- To remove a file you have already chosen, click the small **×** in its corner. Its label is
  **Remove file**.

---

### How to find and search past messages

**Who can do this:** Staff with the *Communication* or *Console* permission.

**Where:** The lower half of the **Messages** page.
URL: `https://peek.peek-a-boo.app/app/messages`

**Steps:**

1. Scroll to the history section. Its heading reads either **All History** or the type name followed
   by **History**, with the total count in brackets.
2. Type a word into **Keyword**. The box shows **Enter keyword**.
3. Set **From** and **To** to limit the search to a date range, if you want.
4. Choose a type in **Types** — **All Types**, or one of the six type names.
5. Click the round blue search button to the right. Its label is **Search messages**. Pressing Enter
   in the **Keyword** box does the same thing.

**The search controls in full:**

| Field | Required? | What to enter | Options |
| --- | --- | --- | --- |
| **Keyword** | No | A word to search for | Free text |
| **From** | No | Earliest date | Date picker |
| **To** | No | Latest date | Date picker |
| **Types** | No | Restrict to one type | **All Types**, **Announcement**, **Notification**, **Event**, **Newsletter**, **Media**, **Video Media** |
| **Unpublished** | No | Show items you saved but did not publish | On/Off switch |

**Good to know:**
- **Keyword**, **From** and **To** only take effect when you click the search button. **Types** and
  **Unpublished** apply the moment you change them.
- Two display layouts are available: **Timeline View** (cards) and **List View** (a table).
- **List View** has these columns: **Type**, **Title**, **Pinned**, **Publish On**, **Published**,
  **Created On**, and an unlabelled column holding the edit and delete buttons.
- In both layouts, a **green** dot means **Published** and an **amber** dot means **Unpublished**.
- The history shows 10 items per page. Below it you will see
  `Showing 1–10 of <total>` and **Page 1 of <n>**, with **Previous page** and **Next page** buttons.
- When nothing matches you will see **No history items yet.** or **No items of this type yet.**
- The counter at the very top of the page reads `<n> published on this page` — that counts published
  items on the page you are looking at, not in the whole system.

---

### How to edit a message after publishing

**Who can do this:** Staff with the *Communication* or *Console* permission.

**Where:** The history list on the **Messages** page.

**Steps:**

1. Find the item in the history list.
2. Click the pencil button on it. Its label is **Edit**.
3. The compose window reopens, headed **Edit** followed by the type name, with the existing content
   loaded.
4. Change what you need.
5. Click **Update & Send**.

**After you save:** a confirmation reads **Updated successfully**. If it fails, the message reads
**Update failed**.

**Good to know:**
- Yes — published messages **can** be edited. The type cannot be changed; editing an item reopens it
  as its original type.
- You can remove an attached file during an edit by clicking its **×**. Removing it and saving
  detaches it from the item.

> **Not yet checked on a live system:** whether an edit reaches families who already received the
> original, whether they see the updated version or the version as first published, and whether an
> edit triggers a second notification. Assume an edit may not reach anyone who already has the
> original, and send a fresh message if a correction genuinely matters.

---

### How to delete a message

**Who can do this:** Staff with the *Communication* or *Console* permission.

**Where:** The history list on the **Messages** page.

**Steps:**

1. Find the item in the history list.
2. Click the bin button on it. Its label is **Delete**.
3. A confirmation box appears headed **Delete this message**. It reads
   **Are you sure you want to delete <title>?** — or **Are you sure?** if the item has no title.
4. Click **Yes** to confirm, or **Cancel** to back out.

**After you save:** a confirmation reads **Deleted successfully**. If it fails, the message reads
**Delete failed**.

**Good to know:**
- There is no undo and no archive. Deleting removes the item from the history list for good.

> **Not yet checked on a live system:** whether deleting an item also withdraws it from families who
> already received it, or whether it only removes it from your history. Do not rely on deletion to
> retract something sent in error — contact the families directly.

---

## Part 2 — Calendar

### What the Calendar shows

The Calendar is a nursery-wide diary of events: holidays, trips, performances, meetings and so on.
The page heading is **Calendar**, with **Operations** above it and the line
**Nursery-wide events, holidays, and key dates** underneath.

It is a separate list from the Event messages described in Part 1. The two do not feed each other.

### The eight event types and their colours

Every event has exactly one type. The type sets the colour the event is drawn in. A key to these
colours sits at the bottom of the page under the heading **Event types:**.

| Type label | Colour |
| --- | --- |
| **Holiday** | Red |
| **Trip** | Sky blue |
| **Performance** | Violet |
| **Meeting** | Amber |
| **Class** | Green |
| **Assessment** | Orange |
| **Reminder** | Pink |
| **Other** | Grey |

The default type on a new event is **Meeting**.

### The two views

There are exactly **two** views, switched with a pair of buttons on the toolbar:

- **Month** — a traditional month grid, weeks running **Mon** to **Sun**. Today's date is circled.
  Each day shows up to three events; beyond that a line reads `+<number> more`.
- **Agenda** — a chronological list of events, each with its date block, title, type badge, time,
  class and description.

There is no day view and no week view.

The toolbar also carries **Today**, plus **Previous month** and **Next month** arrows, and shows the
month and year you are looking at. Above that sits a row of filter buttons: **All Classes** followed
by one button per class.

On a narrow screen such as a phone, the page opens in **Agenda**; on a wider screen it opens in
**Month**.

---

### How to add a Calendar event

**Who can do this:** Staff whose role grants the *Communication* or *Console* permission.

**Where:** Sidebar group **Operations** → **Calendar**.
URL: `https://peek.peek-a-boo.app/app/calendar`

**Before you start:** Know the date. A title and a start date are both required.

**Steps:**

1. Open **Calendar** from the sidebar.
2. Click **Add Event** at the top right. Alternatively, in **Month** view, click any empty part of a
   day square — this opens the same window with that date already filled in.
3. The window opens headed **Add event**.
4. Enter the **Event title**. The box shows the example `e.g. Eid Holiday`.
5. Choose the **Event type** from the dropdown.
6. Set the **Start date**. Required.
7. Set the **End date**. For a single-day event, leave it the same as the start date.
8. Set the **Start time** and **End time** if the event is not all day.
9. Type any **Description**. The box shows `Optional notes or details...`.
10. Under **Branches**, click a class if the event is for one class only. Leave every one unselected
    for a nursery-wide event — the note underneath reads
    **Leave all unselected for nursery-wide**.
11. Click **Save event**, or **Cancel** to abandon it.

**The form in full:**

| Field | Required? | What to enter | Options |
| --- | --- | --- | --- |
| **Event title** | **Yes** | Name of the event | Free text |
| **Event type** | **Yes** (defaults to **Meeting**) | The category | **Holiday**, **Trip**, **Performance**, **Meeting**, **Class**, **Assessment**, **Reminder**, **Other** |
| **Start date** | **Yes** | First day | Date picker |
| **End date** | No | Last day | Date picker |
| **Start time** | No | Start time | Time picker |
| **End time** | No | End time | Time picker |
| **Description** | No | Notes or details | Free text, multi-line |
| **Branches** | No | Click **one** class, or leave all unselected for nursery-wide | Your nursery's classes |

**After you save:**

- On success a confirmation reads **Event created**.
- With no title, nothing is saved and a message reads **Title required**.
- With no start date, nothing is saved and a message reads **Start date required**.
- With an end date earlier than the start date, nothing is saved and a message reads
  **End date cannot be before start date**.
- If the save fails for another reason, a message reads **Something went wrong**.

**Good to know:**
- Despite the plural heading **Branches**, only **one** class can be selected. Clicking a second
  class replaces the first. Clicking the selected class again deselects it.
- If you leave the times empty, the event is recorded as running from `00:00` to `23:59` on the days
  you chose.
- The class filter buttons at the top of the page always show nursery-wide events — an event with no
  class is visible under every filter.

> **Not yet checked on a live system:** whether Calendar events reach parents at all. This screen
> creates and stores events and shows them to staff. Nothing in it indicates that parents are
> notified or that the event appears in a parent-facing app. If families need to know about an event,
> publish an **Event** message from the Messages page as well, and confirm with your provider whether
> the Calendar is visible to parents.

---

### How to edit a Calendar event

**Who can do this:** Staff with the *Communication* or *Console* permission.

**Where:** Sidebar group **Operations** → **Calendar**.
URL: `https://peek.peek-a-boo.app/app/calendar`

**Steps:**

1. Find the event.
2. From **Month** view, click the event to open its detail card, then click **Edit**.
   From **Agenda** view, click the pencil button on the event's row — its label is **Edit event**.
   (You can also click the event title in Agenda to open the detail card first.)
3. The window opens headed **Edit event** with the existing details loaded.
4. Change what you need.
5. Click **Save event**.

**After you save:** a confirmation reads **Event updated**. The same three validation messages apply
as when adding — **Title required**, **Start date required**, and
**End date cannot be before start date**.

**Good to know:**
- The detail card shows the type badge, the title, the date (with an arrow to the end date if the
  event spans more than one day), and the time. If the event has no times set, the card shows
  **Time not set**; an all-day event shows **All day**.

---

### How to delete a Calendar event

**Who can do this:** Staff with the *Communication* or *Console* permission.

**Where:** Sidebar group **Operations** → **Calendar**.

**Steps:**

1. Find the event.
2. From **Month** view, click the event to open its detail card, then click **Delete**.
   From **Agenda** view, click the bin button on the event's row — its label is **Delete event**.
3. The event is deleted.

**After you save:** a confirmation reads **Event deleted**. If it fails, the message reads
**Delete failed**.

**Good to know:**
- Deleting a Calendar event happens **immediately**. Unlike deleting a message, there is **no**
  "are you sure?" confirmation box on either the detail card or the Agenda row. Click carefully.

---

## Part 3 — Live Dashboard

### What the Live Dashboard shows

The page heading is **Live Dashboard**, with **Nursery Operating System** above it and today's date
underneath. A green **Live** badge with a pulsing dot sits at the top right.

**Does it refresh on its own?** Yes. Every figure on this page refreshes automatically **every 60
seconds**. It also refreshes whenever you click back into the browser tab, and whenever your internet
connection is restored. You do not need to reload the page.

### The three tabs

| Tab label |
| --- |
| **Main Dashboard** |
| **Finance** |
| **CRM** |

The page opens on **Main Dashboard**.

---

### Tab 1 — Main Dashboard

**Three figures across the top:**

| Card title | What it counts, in plain words |
| --- | --- |
| **Children Present** | Children marked present or late today, shown against the total number of children on file — for example `18 / 24`. Underneath, the same figure as a percentage followed by **attendance**. |
| **Absent Today** | Children marked absent today plus those marked excused, added together. Underneath, the split: `<n> absent · <n> excused`. |
| **Active Staff** | Staff members whose record is currently active. Underneath, the total number of staff on file followed by **total staff**. |

**Three panels below:**

| Panel title | What it shows |
| --- | --- |
| **Classroom Occupancy** | One row per class. Class name, then how many children are present today followed by **present**, a bar, and the enrolled number against the class capacity. When a class has more children enrolled than its capacity, the bar and figures turn red. Empty state: **No classrooms found**. |
| **Late Arrivals** | Every child marked late today, with the reason recorded against them and the time they came in. If no reason was entered, the line reads **No reason given**. When there are none, a green tick appears with **No late arrivals today**. |
| **Upcoming & Pinned** | Up to three pinned, published items from Messages — each tagged **Announcement** — followed by up to six Calendar events dated today or later, earliest first. Empty state: **No upcoming events or pinned announcements**. |

**Over-capacity banner.** If any class has more children enrolled than its capacity allows, a red
banner appears above everything else showing the class name and the figures, followed by the word
**children**.

---

### Tab 2 — Finance

This tab covers **one month at a time**. A row of month buttons runs across the top, covering last
month and the seven months after it. **Custom Date** with a month picker lets you choose any other
month. The tab opens on the current month.

| Card or panel title | What it shows, in plain words |
| --- | --- |
| *(top summary panel, no heading)* | The total invoiced in the chosen month, with the word **billed** after it. Above it: the number of invoices followed by **invoices**, and the number of distinct children followed by **children**. A green badge shows the percentage followed by **Collected**. |
| **Collected** | Within the summary panel — the money received in the chosen month. |
| **Late** | Within the summary panel — the chosen month's billed amount minus what has been collected. |
| **Across all months** | A line under the summary panel showing the total still unpaid across every month, ending with the words **still unpaid**. |
| **Bills vs Collected** | A bar chart comparing billed against collected for each class in the chosen month, up to eight classes, with a percentage above each pair. Shows **No data** when there is nothing to chart. |
| **Revenue by Age Group** | Money received in the chosen month, grouped by age group. The note underneath reads **Receipts grouped by each child's configured class age group.** Empty state: **No age groups configured**. |
| **Outstanding Balances** | The four families owing the most, across all time. Each row shows the family name, the child's name beneath it, the amount owed, and a count of **Days Late**. Empty state: **No outstanding balances**. |

**Good to know:**
- The figures here are a live summary. The Finance screens in the sidebar remain the authoritative
  place to look at and act on individual invoices and receipts.

---

### Tab 3 — CRM

This tab covers admissions enquiries. **Nine figures run across the top:**

| Card title | Sub-label beneath | What it counts |
| --- | --- | --- |
| **Total Leads** | All CRM leads | Every enquiry on file |
| **Last 7 Days** | Recently received | Enquiries received in the past seven days |
| **New Leads** | New enquiries | Enquiries at the new stage |
| **Tour Booked** | Upcoming tours | Enquiries with a tour booked |
| **Toured** | Tour completed | Enquiries where the tour has happened |
| **Waiting List** | Awaiting progress | Enquiries on the waiting list |
| **Approved** | Approved leads | Approved enquiries |
| **Lost** | Lost leads | Enquiries recorded as lost |
| **Rejected** | Rejected leads | Enquiries recorded as rejected |

> **Where these cards and the Leads page disagree, trust the Leads page.** The Leads screen is the
> place where enquiries are actually worked and recorded, and its wording and counts are the ones to
> rely on. Several of these dashboard cards group enquiry stages differently from the way the Leads
> page presents them, so a figure here will not always line up with what you see there. Use these
> cards for a rough sense of volume; use the Leads page for anything you are going to act on, report
> or quote to someone.

**Three views below the cards,** switched with buttons labelled **Calendar**, **Graphs** and
**Details**. The tab opens on **Calendar**. A toolbar with **Today**, **Previous month** and
**Next month** sits above them.

| View | What it shows |
| --- | --- |
| **Calendar** | A month grid headed **CRM Calendar**, weeks running **Mon** to **Sun**, showing admissions-related events only. Up to three per day, then `+<n> more`. |
| **Graphs** | Four charts: **Leads**, **Referrals Type**, **Source** and **Referrals**. The first two use the segments **Total Leads**, **Total Registered**, **Total Applicants** and **Total Lost**. Charts with nothing to show display **No data**. |
| **Details** | A table per centre, broken down by age band, with the columns **Age**, **New Leads**, **KYC**, **Tour Taken**, **Application**, **Evaluation**, **Approved**, **Registered** and **Total Lost**. Leads with no age recorded appear under **Unspecified**. Empty state: **No CRM details found**. |

**Exporting the Details table:** with **Details** selected, an **Export to Excel** button appears on
the toolbar. Clicking it downloads a spreadsheet file named `crm-details.csv`.

**Good to know:**
- The two round charts, **Leads** and **Referrals Type**, are drawn from the same set of figures, so
  they will look alike. Read the **Source** and **Referrals** bar charts for the breakdown by where
  enquiries came from.
- The **Details** table and the **Graphs** charts group enquiry stages in different ways. Where you
  need an exact number, take it from the Leads page.

---

## Quick reference

| I want to... | Where to go |
| --- | --- |
| Tell families about something | **Messages** → pick a type → tick children → **Publish Now** |
| Send photos to families | **Messages** → **Media** (JPG/PNG, 1 MB each) |
| Send a video to families | **Messages** → **Video Media** (MP4/WebM/OGG/MOV, 35 MB) |
| Find something I sent before | **Messages** → history section → **Keyword** → search button |
| See things I saved but never published | **Messages** → history → **Unpublished** toggle on |
| Record a nursery event for staff | **Calendar** → **Add Event** |
| Check today's attendance at a glance | **Live Dashboard** → **Main Dashboard** |
| Check this month's money | **Live Dashboard** → **Finance** |
| Check admissions enquiries | **Leads** page (the CRM dashboard tab is a summary only) |
| Reply to a parent | Not possible in the portal — use phone, email or in person |
