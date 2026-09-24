# Children and Staff — Step-by-step procedures

These procedures describe the Peekaboo nursery portal at **https://peek.peek-a-boo.app** as it
behaves for the version currently running for customers.

**How to read this document**

- Plain text = taken directly from the product. Field exists, the label reads exactly this, this
  option is in this dropdown, this entry is required.
- Lines marked `> **Not yet checked on a live system:**` are things this document could not confirm
  with certainty. They are usually about what the server does after you press Save. Treat them as
  "expected, but verify on your own site before training staff on it".

Every button, tab, column and field name printed in **bold** is the literal English text shown on
screen. If the portal is switched to Arabic the same controls appear in Arabic.

---

## Part 1 — Children

### How to open the Children list

**Who can do this:** Any user whose role includes the **Our Loved Ones** permission. Users with role
"Root"/ID 1 always have access regardless of permissions.
**Where:** Sidebar group **People** → **Children**. URL: `https://peek.peek-a-boo.app/app/children`
**Before you start:** You must be signed in.

**Steps:**

1. Sign in to the portal.
2. In the left sidebar, find the group headed **People**.
3. Click **Children**.

**Good to know:**

- If your role does not have the **Our Loved Ones** permission, **Children** does not appear in the
  sidebar at all. Opening the address directly shows an access-denied page instead of the list.
- The page heading is **Children**, with the small label **NOS** above it.

---

### How to read the Children list

**Who can do this:** Anyone who can open the page.
**Where:** **People** → **Children**
**Before you start:** Nothing.

The children are shown as **cards in a grid**, not as a table with columns. There is no table view on
this page and no column chooser. Each card shows, in this order:

| Part of the card | What it shows |
|---|---|
| Photo | The child's uploaded picture. If there is no picture, a coloured circle with the child's initials (up to two letters). The circle is blue for a child recorded as male and orange/red otherwise. |
| Name | The child's full name. |
| Status pill | **Active** (green) or **Inactive** (red). |
| Age | A calculated age, shown as e.g. `18 months` under two years, or `3y 4m` / `3 yrs` above two years. |
| Attendance pill | Only if an attendance record exists for that child: **Present**, **Absent**, **Late**, **Excused**, or **Not Marked**. |
| Gender | **Male** or **Female**. |
| Nationality | The country name. |
| Allergy count | Only if the child has allergy records. Shown in red with a warning triangle, e.g. `2 allergy`. |
| Parent line | The linked parent's name, then a dot, then the parent's first phone number. |

Above the grid, the page shows a count followed by the word **enrolled**.

Each card has two round buttons on its right edge:

- A pencil button — opens the child for editing.
- A red bin button — deletes the child.

Clicking anywhere on the card body also opens the child for editing.

**Good to know — an important trap:**

- **The age printed on the card is not calculated from today's date.** It is calculated against a
  fixed date built into the product (21 April 2026). This means the age shown on the card will
  drift and will not agree with the child's true age as time passes. The **All Age Groups** filter,
  by contrast, *does* use the real current date. So a child can be filtered into an age group that
  does not match the age printed on their own card. Do not rely on the card age for anything
  official; check the birth date on the child's record instead.
- The word **enrolled** counts every child returned for your nursery, including inactive ones. It is
  not a count of currently active children.
- The allergy count and the attendance pill only appear when that data exists; an empty space does
  not mean "no allergies recorded", it means nothing was returned for that card.

---

### How to search and filter the Children list

**Who can do this:** Anyone who can open the page.
**Where:** **People** → **Children**
**Before you start:** Nothing.

**Steps:**

1. To search, type into the box labelled **Search by name or ID…** at the top left. The list filters
   as you type. It matches against the child's **name** and their **Social Security** / ID value.
   Matching ignores capital letters.
2. To filter by status, use the first dropdown. Options: **All Status**, **Active**, **Inactive**.
3. To filter by class, use the second dropdown. Options: **All Classes**, then one entry for each
   class set up at your nursery.
4. To filter by age band, use the third dropdown. Options: **All Age Groups**, then one entry per age
   group, each shown as its code, a dash, then its description.
5. To reset, click **Clear**.

If nothing matches you see: **No children match the current filters.**

**Good to know:**

- The **Clear** button only appears once a search term, a class filter or an age-group filter is
  active. It does **not** appear if the only thing you changed was the status dropdown.
- **Clear** resets the search box, the class filter and the age-group filter. **It does not reset the
  status filter.** If you had set status to **Inactive**, it stays on **Inactive** after clicking
  **Clear**, which can look like the list is still broken. Set it back to **All Status** by hand.
- The class filter matches the class stored on the child record itself. A child whose class comes
  only from a registration entry may not behave as you expect here.
- The age filter only includes children who have a birth date recorded. A child with no birth date is
  excluded from every specific age group.

---

### How to add a child

**Who can do this:** Any user with the **Our Loved Ones** permission.
**Where:** **People** → **Children** → **Add Child**. URL: `https://peek.peek-a-boo.app/app/children`
**Before you start:**

- Ideally, create the parent first so you can link them. You can also create the parent from inside
  this form (see "How to add a parent" below).
- Have the child's birth date to hand. It is required.

**Steps:**

1. Open **People** → **Children**.
2. Click **Add Child** (top right).
3. The page heading changes to **Add Child** and four tabs appear: **Child Data**, **Health**,
   **Pickup**, **Registrations**. You start on **Child Data**.
4. Fill in the fields on **Child Data** (full list below). **Child Name** and **Birth Date** are the
   only two the portal insists on.
5. Optionally add a photo on the right-hand panel: click the dashed box marked
   **Drag & drop or click**, or click **Browse ...**, and pick an image file.
6. Click **Save Child**.

**The form in full — the Child Data tab**

| Field | Required? | What to enter | Options (for dropdowns) |
|---|---|---|---|
| **Child Name** | **Yes** | The child's full name. Placeholder text reads `Full name`. | — |
| **Birth Date** | **Yes** | The date of birth, chosen from a date picker. | — |
| **Gender** | No | Pick from the list. | **--Select--**, **Male**, **Female** |
| **Nationality** | No | Pick the country. | **--Select--**, then every country on the portal's country list |
| **First Language** | No | Pick the language. | **--Select--**, then every language on the portal's language list |
| **Social Security** | No | ID number. Placeholder reads `ID / Emirates ID`. | — |
| **Parent** | No | Pick the parent/guardian this child belongs to. A **+** button beside it opens **Add New Parent**. | **--Select--**, then every parent already on the system |
| **Status** | No | On/off switch, labelled **Not Active / Active**. Starts **on** (Active) for a new child. | — |
| **Take Pictures** | No | On/off switch, labelled **No / Yes**. Starts **on**. | — |
| **Pic Nursery** | No | On/off switch, labelled **No / Yes**. Starts **on**. | — |
| **Pic Media** | No | On/off switch, labelled **No / Yes**. Starts **off**. | — |
| **Pic Social** | No | On/off switch, labelled **No / Yes**. Starts **off**. | — |
| **Staff Child** | No | On/off switch, labelled **No / Yes**. Starts **off**. | — |
| **Child SEN** | No | On/off switch, labelled **No / Yes**. Starts **off**. | — |
| **Notes** | No | Free-text box, three lines tall. | — |
| **Medical Notes** | No | Free-text box, three lines tall. | — |
| **Child Picture** | Marked with a red asterisk, but **not actually enforced** — see below | An image file. Sub-text reads **Drag & drop or click**; buttons **Remove** and **Browse ...**; when empty the strip below reads **No file selected**. | — |

**Validation you will actually hit**

- Leave **Child Name** empty and press **Save Child**: `Child name is required.`
- Leave **Birth Date** empty and press **Save Child**: `Birth date is required.`

No other field is checked by the portal before saving.

**After you save**

- On success the portal shows **Saved successfully** and returns you to the Children list.
- If the server reports a problem, its own message is shown; if it sends none, you see
  **Failed to save**.
- If the request itself fails, you see **Failed to save — changes may not have persisted**.

> **Not yet checked on a live system:** whether the server applies its own extra validation (for
> example rejecting a duplicate ID or a missing photo) and what wording it uses. The messages above
> are the ones the portal itself produces; anything the server sends is shown as-is and cannot be
> listed here.

**Good to know:**

- **The photo is marked required with a red asterisk, but nothing stops you saving without one.**
  The asterisk is cosmetic. Children save fine with no picture and simply show initials on the card.
- **The photo panel is hidden on narrow screens.** It only appears on large displays. On a tablet or
  a small laptop window you will not see the upload box at all.
- **The four tabs are not equal.** **Child Data** works immediately. **Health**, **Pickup** and
  **Registrations** will let you click their **Add** buttons, but if the child has not been saved yet
  you get `Please save the child first.` and nothing is added. So: save the child first, then reopen
  it to use the other three tabs.
- There is a **Gmail** field stored behind the scenes but it is **not shown on the form** in this
  version. You cannot enter or edit it here.
- **Cancel** discards the form and returns to the list without warning you about unsaved typing.

---

### How to add a parent while adding a child

**Who can do this:** Any user with the **Our Loved Ones** permission.
**Where:** Inside the child form, on the **Child Data** tab, the **+** button beside **Parent**.
**Before you start:** Nothing.

**Steps:**

1. In the child form, click the **+** button next to the **Parent** dropdown.
2. A window titled **Add New Parent** opens.
3. Fill in the fields (below). **Parent Name** and **Email 1** are enforced.
4. Click **Save**.

**The form in full — Add New Parent**

Main block:

| Field | Required? | What to enter | Options |
|---|---|---|---|
| **Parent Name** | **Yes** | The parent's full name. | — |
| **Parent Status** | No | On/off switch labelled **Not Active / Active**. Starts **on**. | — |
| **Phone 1** | No | Primary phone. | — |
| **Email 1** | **Yes** | Primary email address. | — |
| **Parent Country** | No | Country. | **--Select--**, then the country list |
| **Address** | No | Street address. | — |
| **Phone 2** | No | Second phone. | — |
| **Email 2** | No | Second email. | — |
| **User Name** | **Yes** (shown with a red asterisk) | Login name for the parent. Pre-filled automatically as `P-` followed by seven digits. A refresh button beside it generates a new one. | — |
| **Password** | **Yes** (shown with a red asterisk) | Login password. **Pre-filled with `12345678`.** An eye button reveals or hides it. | — |
| **Social Security** | No | ID number. | — |
| **Use Apps** | No | On/off switch labelled **No / Yes**. Starts **on**. | — |
| **Use Mail** | No | On/off switch labelled **No / Yes**. Starts **on**. | — |

Section **Spouse Contact Details**:

| Field | Required? | What to enter |
|---|---|---|
| **Spouse Name** | No | Name. |
| **Spouse Phone** | No | Phone. |
| **Spouse Email** | No | Email. |

Section **Emergency Contact Details**:

| Field | Required? | What to enter |
|---|---|---|
| **Contact Name** | No | Name of the emergency contact. |
| **Phone 1** | No | First emergency number. |
| **Phone 2** | No | Second emergency number. |

Buttons at the bottom: **Close** and **Save** (**Saving...** while it works).

**Validation**

- Empty **Parent Name**: `Parent name is required.`
- Empty **Email 1**: `Email 1 is required.`

**After you save**

- The window closes and a message appears reading the parent's name, a dash, then
  **Parent added successfully.**
- The new parent is selected automatically in the child form's **Parent** dropdown.
- If it fails, the server's message is shown, or **Failed to save parent**.

**Good to know — real traps:**

- **The password is pre-filled with `12345678` and is a real, working password.** If you leave it,
  the parent's account is created with that password. Change it, or make sure your nursery has a
  process for the parent to reset it.
- **Three fields in this window are collected but never saved.** The window internally tracks a
  relationship, a language and a nationality for the parent, but **none of them are sent when you
  press Save**. Do not rely on this window to record a parent's relationship to the child. Nothing
  on screen tells you this.
- The **User Name** is generated randomly. Write it down, or retrieve it later from the parent
  record, because the parent needs it to sign in.
- This window creates a parent. It does **not** on its own link them to the child — the link happens
  because the new parent is auto-selected in the **Parent** dropdown, and only becomes permanent when
  you then save the child.

---

### How to edit a child

**Who can do this:** Any user with the **Our Loved Ones** permission.
**Where:** **People** → **Children**, then the pencil button on a card (or click the card).
**Before you start:** Nothing.

**Steps:**

1. Open **People** → **Children**.
2. Click the pencil button on the child's card, or click the card body.
3. The heading reads **Edit Child**. All four tabs are now usable.
4. Change what you need on **Child Data**.
5. Click **Update Child**.

**After you save:** the portal shows **Updated successfully** and returns to the list.

**Good to know:**

- The button on an existing child reads **Update Child**, not **Save Child**.
- Only the **Child Data** tab is saved by **Update Child**. Entries on **Health**, **Pickup** and
  **Registrations** are saved individually inside their own windows the moment you press **Save**
  there — they do not wait for **Update Child**, and pressing **Cancel** afterwards does not undo
  them.
- If you had uploaded a photo previously, it is shown in the panel. Pressing **Remove** or the small
  X clears it from the form.

---

### How to deactivate a child

**Who can do this:** Any user with the **Our Loved Ones** permission.
**Where:** Inside the child record, **Child Data** tab, the **Status** switch.
**Before you start:** Nothing.

**Steps:**

1. Open the child for editing.
2. On **Child Data**, find **Status** (switch labelled **Not Active / Active**).
3. Switch it off.
4. Click **Update Child**.

The child's card will then show the red **Inactive** pill, and they can be found using the
**Inactive** option in the status filter.

**Good to know:**

- There is **no** one-click activate/deactivate button on the child cards. Deactivating always means
  opening the record and saving it. (The Staff page does have such a button — children do not.)
- Deactivating is the safe alternative to deleting: it keeps the child and all their history.

---

### How to delete a child

**Who can do this:** Any user with the **Our Loved Ones** permission.
**Where:** **People** → **Children**, the red bin button on a card.
**Before you start:** Consider deactivating instead. Deletion is offered with no undo.

**Steps:**

1. Open **People** → **Children**.
2. Click the red bin button on the child's card.
3. A confirmation box appears. Its title reads **Delete Child** and its message reads
   **Are you sure you want to delete** followed by the child's name and a question mark.
4. Click **Yes** to proceed, or **Cancel** to stop.

**After you delete**

- On success: **Deleted successfully**, and the card disappears from the list.
- If the child has related records, deletion is refused with:
  **Cannot delete this child because related records exist.**

> **Not yet checked on a live system:** exactly which related records block a deletion (for example
> attendance, invoices, registrations, health entries). The portal only reports that related records
> exist; it does not say which. Test on a sample child before deleting real ones.

**Good to know:**

- The confirmation box gives no warning that deletion is permanent and offers no "deactivate
  instead" option. The **Yes** button is the destructive one.
- Clicking the dark background behind the confirmation box counts as **Cancel**.

---

### How to record a health or medical entry for a child

**Who can do this:** Any user with the **Our Loved Ones** permission.
**Where:** Inside a saved child record → tab **Health**.
**Before you start:** **The child must already be saved.** On a brand-new unsaved child you get
`Please save the child first.`

**Steps:**

1. Open the child for editing.
2. Click the **Health** tab.
3. Click **Add Health**.
4. A window titled **Add Health** opens.
5. Choose a **Health Description** from the dropdown.
6. Optionally type a **Comment**.
7. Click **Save**.

**The form in full — Add Health**

| Field | Required? | What to enter | Options |
|---|---|---|---|
| **Health Description** | **Yes** | The condition, picked from the nursery's list of health entries. | **--Select--**, then every health entry configured for your nursery |
| **Comment** | No | Free text. Placeholder reads `Enter comment`. | — |

There is also a button **Add New Health** inside this window for creating a condition that is not yet
on the list (see next procedure). Footer buttons: **Close** and **Save**.

**Validation:** with no condition chosen: `Please select a health description.`

**The Health tab table** has these columns: an actions column, **Health Description**,
**Health Type**, **Comment**. Below it a line reads **Showing** … **to** … **of** … **entries**.
When empty the table shows **No data available in table**.

**After you save**

- **Health added.** appears and the window closes. The table refreshes to include the new row.
- On failure, the server's message is shown, or **Failed to save health**.

**Good to know — real traps:**

- **There is no way to edit an existing health entry.** The rows only have a delete (bin) button. The
  edit button exists in the product but is switched off in this version. To correct a mistake you
  must delete the row and add it again.
- The **Medical Notes** box on the **Child Data** tab is a completely separate free-text field. It is
  not connected to this Health tab in any way. Recording an allergy here does not put anything in
  **Medical Notes**, and vice versa.
- The allergy warning shown on the Children list cards is driven by allergy data on the child record.
  > **Not yet checked on a live system:** whether adding an entry of type **Allergy** here is what
  > makes that red allergy count appear on the card.

---

### How to add a new health condition to the nursery's list

**Who can do this:** Any user with the **Our Loved Ones** permission.
**Where:** Inside the **Add Health** window → **Add New Health**.
**Before you start:** Nothing.

**Steps:**

1. Open a child → **Health** tab → **Add Health**.
2. Click **Add New Health**.
3. A second window titled **Add New Health** opens on top.
4. Enter a **Health Name**.
5. Choose a **Health Type**.
6. Click **Save**.

**The form in full — Add New Health**

| Field | Required? | What to enter | Options |
|---|---|---|---|
| **Health Name** | **Yes** | The name of the condition. Placeholder reads `e.g. Celiac Disease`. | — |
| **Health Type** | No — if left blank it is saved as **Other** | The category. | **--Select--**, **Allergy**, **Chronic**, **Skin**, **Neurological**, **Dietary**, **Respiratory**, **Other** |

**Validation:** empty name: `Health name is required.`

**After you save**

- **Health type added successfully** appears, the window closes, and the new condition is selected
  automatically in the **Health Description** dropdown behind it.
- On failure: **Failed to add health type**.

**Good to know:**

- This creates a condition in your nursery's shared list, available for every child. It is not
  specific to the child you happen to have open.
- Leaving **Health Type** as **--Select--** does not produce an error; the condition is filed under
  **Other**.
- Creating the condition does **not** attach it to the child. It only selects it in the dropdown. You
  still have to press **Save** in the **Add Health** window to attach it.

---

### How to delete a health entry

**Steps:**

1. Open the child → **Health** tab.
2. Click the red bin button on the row.
3. The confirmation box is titled **Delete Health Record** and reads **Are you sure?**
4. Click **Yes**.

**After you delete:** **Health deleted.** On failure, the server's message or
**Failed to delete health**.

**Good to know:** the confirmation does not name which entry you are deleting — it just asks
**Are you sure?**. Check you clicked the right row first.

---

### How to add an authorised pickup person

**Who can do this:** Any user with the **Our Loved Ones** permission.
**Where:** Inside a saved child record → tab **Pickup**.
**Before you start:** **The child must already be saved**, otherwise: `Please save the child first.`

**Steps:**

1. Open the child for editing.
2. Click the **Pickup** tab.
3. Click **Add Pickup**.
4. A window titled **Add Pickup** opens.
5. Complete the fields.
6. Click **Save**.

**The form in full — Add Pickup**

| Field | Required? | What to enter | Options |
|---|---|---|---|
| **Name** | **Yes** | The person's full name. Placeholder reads `Full name`. | — |
| **Relation** | No | Their relationship to the child. | **--Select--**, **Father**, **Mother**, **Grandfather**, **Grandmother**, **Uncle**, **Aunt**, **Sibling**, **Nanny**, **Other** |
| **Phone** | No | Contact number. Placeholder reads `+971 50 000 0000`. | — |
| **Email** | No | Email address. Placeholder reads `email@example.com`. | — |

**Validation:** empty name: `Name is required.`

**The Pickup tab table** has columns: an actions column, **Name**, **Relation**, **Phone**, **Email**.
Empty phone or email show as a dash. When there are no rows: **No data available in table**.

**After you save:** **Pickup added.** and the table refreshes. On failure, the server's message or
**Failed to save pickup**.

**Good to know:**

- Unlike Health, pickup people **can** be edited. Each row has both a pencil and a bin button. Editing
  opens a window titled **Edit Pickup** and the save button reads **Update**; success message is
  **Pickup updated.**
- Only **Name** is enforced. It is entirely possible to save a pickup person with no phone number and
  no relationship recorded, which is rarely what a nursery wants. Make completing **Phone** and
  **Relation** a local rule.
- There is no photo, no ID document and no password/collection-code field for pickup people in this
  version.
- Deleting asks **Are you sure?** under the title **Delete Pickup Person**; success message is
  **Pickup deleted.**

---

### How to register a child into a class

**Who can do this:** Any user with the **Our Loved Ones** permission.
**Where:** Inside a saved child record → tab **Registrations**.
**Before you start:**

- **The child must already be saved**, otherwise: `Please save the child first.`
- The class must exist and be active.
- The session/timing must exist and be active.

**Steps:**

1. Open the child for editing.
2. Click the **Registrations** tab.
3. Click **Add Registration**.
4. A window titled **Add Registration** opens.
5. Choose the **Class**.
6. Set the two dates under **From / To Date**.
7. Choose the **Days** by clicking each day button, or use **Select all**.
8. Choose the **Timing**.
9. Leave **Status** on, or switch it off.
10. Click **Save**.

**The form in full — Add Registration**

| Field | Required? | What to enter | Options |
|---|---|---|---|
| **Class** | **Yes** | The class to register into. | **--Select--**, then every **active** class. Classes marked inactive are not listed. |
| **From / To Date** | **Yes** (both dates) | Two date pickers side by side separated by a dash: the start date and the end date. | — |
| **Days** | **Yes** (at least one) | Click the day buttons to switch each day on or off. Selected days are highlighted. A link to the right reads **Select all**, changing to **Deselect all** once every day is chosen. | **Monday**, **Tuesday**, **Wednesday**, **Thursday**, **Friday**, **Saturday**, **Sunday** |
| **Timing** | **Yes** | The session. Each option shows the session name followed by its start and end times in brackets. | **--Select--**, then every **active** session. Inactive sessions are not listed. |
| **Status** | No | On/off switch labelled **Not Active / Active**. Starts **on**. | — |

**Validation, checked in this order:**

1. No class: `Please select a class.`
2. Missing either date: `Please select from and to dates.`
3. No timing: `Please select timing.`
4. No days: `Please select days.`

**The Registrations tab table** has columns: an actions column, **Class**, **From Date**, **To Date**,
**Days**, **Timing**, **Status**. Days appear abbreviated as **Mon**, **Tue**, **Wed**, **Thu**,
**Fri**, **Sat**, **Sun**, separated by commas; a registration with no days shows a dash. **Status**
shows a green **Active** or a grey **Inactive** pill.

**After you save:** **Registration added.** and the table refreshes. On failure, the server's message
or **Failed to save registration**.

**Good to know — real traps:**

- **The registration is saved against the parent currently selected on the Child Data tab.** If you
  have not chosen a **Parent**, the registration is still saved but with no parent attached. Set the
  parent before registering.
  > **Not yet checked on a live system:** whether a registration saved with no parent causes problems
  > later in billing or in the parent app.
- **Empty class and session lists usually mean "nothing active", not "nothing exists".** Only active
  classes and active sessions appear. If a class is missing from the dropdown, check whether it has
  been deactivated rather than assuming it was deleted.
- **Select all** is a toggle. If every day is already selected the link reads **Deselect all** and
  clicking it clears every day in one go.
- Registrations can be edited (pencil button, window titled **Edit Registration**, button reads
  **Update**, success **Registration updated.**) and deleted (bin button, confirmation titled
  **Delete Registration** asking **Are you sure?**, success **Registration deleted.**).
- A child can hold more than one registration. Nothing warns you about overlapping dates or a clash
  between two registrations.

---

### Where parent and guardian details are managed

Within the Children area you can do exactly two things with parents:

1. **Link a child to an existing parent** — the **Parent** dropdown on the **Child Data** tab.
2. **Create a brand-new parent** — the **+** button beside that dropdown, which opens
   **Add New Parent** (documented above).

**You cannot edit or delete an existing parent from the child form.** There is no edit button beside
the **Parent** dropdown, and opening a child does not show you the linked parent's phone, email or
emergency contacts. To change a parent's details after creation you must use whatever parent
management exists elsewhere in the portal — it is not part of the Children page.

The Children list card does display the linked parent's name and first phone number, read-only.

---

## Part 2 — Staff

### How to open the Staff list

**Who can do this:** Any user whose role includes the **Our Heroes** permission. Role "Root"/ID 1
always has access.
**Where:** Sidebar group **People** → **Staff**. URL: `https://peek.peek-a-boo.app/app/staff`
**Before you start:** You must be signed in.

**Steps:**

1. In the left sidebar, open the group headed **People**.
2. Click **Staff**.

The heading reads **Staff**, with a count below it followed by **staff members**.

**Good to know:** without the **Our Heroes** permission the link is hidden and the address shows an
access-denied page.

---

### How to read the Staff list

**Who can do this:** Anyone who can open the page.
**Where:** **People** → **Staff**

Staff can be shown two ways. Two small buttons at the top right switch between them: **Table view**
and **Card view**. **Card view is the one you see by default.**

**Card view** — each card shows:

| Part of the card | What it shows |
|---|---|
| Photo | The uploaded picture, or a blue square with the first letter of the name. |
| Name | Full name. |
| Status pill | **Active** (green) or **Inactive** (red). |
| Role | The role name. |
| Contact block | Email, then phone, then the login username. |

Each card has three round buttons down the right side: a pencil (edit), a red bin (delete), and a
thumbs-up. The thumbs-up is the activate/deactivate toggle; hovering it shows **Deactivate** when the
person is active and **Activate** when they are not.

**Table view** — columns are: an actions column, then **Employee Name**, **Picture**, **Role**,
**Username**, **Password**, **Email**, **Phone**. The **Employee Name** cell also carries the
**Active** / **Inactive** pill. When nothing matches: **No staff members found**. A line underneath
reads **Showing** 1 **to** … **of** … **entries**.

**Good to know — a genuine privacy trap:**

- **Table view has a Password column, and it displays the staff member's actual password in plain
  text** whenever the server sends it. It only falls back to dots when no password is returned. Do
  not open table view on a screen visible to parents, visitors or other staff, and be careful when
  sharing your screen or projecting.
- Narrow screens hide columns progressively: **Picture**, **Role** and **Phone** disappear first,
  then **Username**, **Password** and **Email**. On a phone you may see only the name.
- Table view's toolbar shows buttons **Copy**, **PDF**, **Print**, **CSV**, **Column visibility »**,
  a **Show** / **entries** count selector, and a **Search:** box.
  **The Copy, PDF, Print, CSV, Column visibility and Show-entries controls do nothing in this
  version.** They are visible but not wired up. Only the **Search:** box works. There is no working
  export on this page.

---

### How to search and filter the Staff list

**Who can do this:** Anyone who can open the page.
**Where:** **People** → **Staff**, table view.

**Steps:**

1. Switch to **Table view**.
2. Type into the **Search:** box. It matches the **employee name only** — not email, not username,
   not phone. Capital letters are ignored.
3. Use the first dropdown to filter by role: **All Roles**, then one entry per role.
4. Use the second dropdown to filter by status: **All**, **Active**, **Inactive**.

**Good to know — an important trap:**

- **The search box and both filter dropdowns only exist in table view.** In card view there is no
  search box and no filters at all. But the filters you set in table view stay applied when you
  switch back to card view. So staff can appear to be "missing" from the card grid with no visible
  control explaining why. If the card list looks wrong, switch to **Table view** and check the
  filters, or reload the page.
- There is no **Clear** button on this page. Reset each dropdown by hand.

---

### How to add a staff member (this creates their portal login)

**Who can do this:** Any user with the **Our Heroes** permission.
**Where:** **People** → **Staff** → **Add Staff**. URL: `https://peek.peek-a-boo.app/app/staff`
**Before you start:**

- Decide which **Role** the person gets. The role controls what they can see in the portal, and it is
  required.
- Have their date of birth, phone and email to hand — all three are required.

**This form creates the person's portal account.** The **User Name** and **Password** you set here
are the credentials they use to sign in.

**Steps:**

1. Open **People** → **Staff**.
2. Click **Add Staff**.
3. A form opens headed **New Employee**, with two tabs: **Details** and **More...**. You start on
   **Details**.
4. Complete the required fields on **Details**.
5. Choose the **Role**.
6. Optionally set a photo using the panel on the right (**Drag & drop files here ...** /
   **Browse ...**).
7. Optionally switch to **More...** and fill in the extra fields.
8. Click **Save**.

**The form in full — Details tab**

| Field | Required? | What to enter | Options |
|---|---|---|---|
| **Employee Name** | **Yes** | Full name. | — |
| **Gender** | No | Defaults to **Female**. | **Female**, **Male** — note there is no blank option |
| **Employee Status** | No | Defaults to **Active**. | **Active**, **Inactive** |
| **Employee Code** | No | Your internal staff code. | — |
| **Nationality** | **Yes** | The country. | **--Select--**, then the country list |
| **DOB** | **Yes** | Date of birth, from a date picker. | — |
| **Phone 1** | **Yes** | Primary phone. Placeholder reads `+971 50 000 0000`. | — |
| **Email 1** | **Yes** | Primary email. | — |
| **Phone 2** | No | Second phone. | — |
| **Email 2** | No | Second email. | — |
| **Address** | No | Street address. | — |
| **User Name** | **Yes** | The login name. Pre-filled automatically. A refresh button beside it generates a new one. | — |
| **Password** | **Yes** | The login password. **Pre-filled with `123456`.** An eye button reveals or hides it. | — |
| **Role** | **Yes** | The person's role, which governs their portal permissions. | **--Select--**, then every role set up on your system |
| **Employee Picture** | Marked with a red asterisk, but **not enforced** | An image file. | — |

**The form in full — More... tab**

| Field | Required? | What to enter |
|---|---|---|
| **Emergency Contact Name** | No | Name of their emergency contact. |
| **Emergency Contact Number** | No | That contact's number. |
| **Capabilities** | No | Free text. Placeholder reads `e.g. CACHE Level 3, EYFS`. |
| **Joining Date** | No | Date picker. |
| **Employee Last Day** | No | Date picker. |
| **Employee Note** | No | Free text, single line. |
| **Social Security** | No | ID number. |
| **Degree** | No | Free text. |
| **Diploma** | No | Free text. |

Both tabs carry the same **Save** and **Cancel** buttons at the bottom, and both save the whole
record — you do not need to return to **Details** to save what you typed on **More...**.

**Validation, checked in this order:**

1. `Employee name is required.`
2. `Nationality is required.`
3. `Date of birth is required.`
4. `Phone 1 is required.`
5. `Email 1 is required.`
6. `Username is required.`
7. `Role is required.`

They are reported one at a time, so you may have to press **Save** several times to discover
everything that is missing.

**After you save**

- The server's own message is shown if it sends one; otherwise **Added successfully**.
- The form closes and you return to the list, which refreshes to include the new person.

> **Not yet checked on a live system:** whether the server rejects a duplicate username or a duplicate
> email address, and what it says if it does. Also not verified: whether the new staff member receives
> any email telling them their login details. Nothing in the portal sends one, so assume you must
> pass the username and password on yourself.

**Good to know — real traps:**

- **The password is pre-filled with `123456`.** If you do not change it, that is genuinely the
  account's password. Change it, or have the person change it immediately.
- **The username is generated from the role, so generate it *after* choosing the role.** The refresh
  button builds a name from the first three letters of the currently-selected role, as in
  `E-TEA-123456`. The name pre-filled when the form first opens was generated before you picked
  anything and will usually carry a generic `EMP` code. Pick the **Role** first, then click the
  refresh button, then save.
- **Saving is not protected against a failed request.** If the save fails outright, the form may not
  show you a clear error. Confirm the person actually appears in the list afterwards.
- **The photo panel is hidden on narrow screens**, exactly as on the child form.
- The photo's red asterisk is cosmetic; staff save without a picture and show an initial instead.
- **Employee Status** here is a dropdown, unlike the child form's switch.

---

### How to edit a staff member

**Who can do this:** Any user with the **Our Heroes** permission.
**Where:** **People** → **Staff**, the pencil button on a card or a table row.

**Steps:**

1. Open **People** → **Staff**.
2. Click the pencil button beside the person.
3. The form opens with the person's name as the title, on the **Details** tab.
4. Make your changes across **Details** and **More...**.
5. Click **Update**.

**After you save:** the server's message, or **Updated successfully**. You return to the list.

**Good to know:**

- On an existing person the button reads **Update**, not **Save**.
- The same seven required-field checks apply as when adding. If an older record is missing, say, a
  date of birth, you will be forced to supply one before you can save any other change.
- Clicking the card body does **not** open a staff member for editing — you must use the pencil
  button. (This differs from the Children page, where clicking the card works.)

---

### How to activate or deactivate a staff member

**Who can do this:** Any user with the **Our Heroes** permission.
**Where:** **People** → **Staff**, the thumbs-up button on a card or table row.

There are two ways.

**The quick way (one click):**

1. Find the person in the list.
2. Click the thumbs-up button. Hovering shows **Deactivate** if they are currently active, or
   **Activate** if they are not.

**After you click:** the server's message, or **Status updated**. On failure, the server's message or
**Update failed**.

**The other way (through the form):**

1. Open the person with the pencil button.
2. On **Details**, set **Employee Status** to **Active** or **Inactive**.
3. Click **Update**.

**Good to know — a real trap:**

- **The thumbs-up button asks for no confirmation.** One click changes the person's status
  immediately. It sits directly below the red delete button on the cards, so click carefully.
- The thumbs-up icon looks identical whether the person is active or inactive; only its colour and
  its hover text change. Hover before clicking if you are unsure which way it will go.
  > **Not yet checked on a live system:** the thumbs-up sends the person's whole current record back
  > to the server for it to flip the status. Whether a deactivated staff member is immediately
  > blocked from signing in has not been verified — do not rely on this alone to cut off access for a
  > departing employee.

---

### How to delete a staff member

**Who can do this:** Any user with the **Our Heroes** permission.
**Where:** **People** → **Staff**, the red bin button on a card or table row.
**Before you start:** Consider deactivating instead.

**Steps:**

1. Click the red bin button beside the person.
2. A confirmation box titled **Delete Employee** asks **Are you sure?**
3. Click **Yes**, or **Cancel** to stop.

**After you delete**

- On success: the server's message, or **Deleted successfully**.
- If the server refuses: its message, or **Employee could not be deleted**.
- If the request fails: the server's message, or **Delete failed**.

**Good to know:**

- The confirmation **does not name the person** — it only says **Are you sure?**. There is no name in
  the message to double-check against, so verify the row before clicking.
- Deleting removes their portal login. Deactivating is the safer choice for someone who may return.

---

### Assigning staff to a class

**This cannot be done from the Staff page.** There is no class field, no classroom dropdown and no
class assignment tab anywhere in the staff form or the staff list. The **Details** tab covers personal
and login details; the **More...** tab covers emergency contact, capabilities, employment dates,
notes and qualifications. Neither mentions classes.

Class assignment, if your nursery uses it, is handled elsewhere in the portal — not here.

> **Not yet checked on a live system:** which page does own staff-to-class assignment in your
> installation.

---

## Quick reference — things that catch people out

| Area | The trap |
|---|---|
| Children list | The age on each card is calculated against a fixed built-in date, not today. It will not match the child's real age. The age *filter* does use today's date, so the two can disagree. |
| Children list | **Clear** resets search, class and age group — but **not** the status filter. |
| Child form | The photo shows a red asterisk but is not actually required. |
| Child form | **Health**, **Pickup** and **Registrations** do nothing until the child has been saved once. |
| Child form | Entries added on those three tabs save immediately. **Cancel** does not undo them. |
| Add New Parent | Password pre-filled with `12345678` — it is real. |
| Add New Parent | The relationship, language and nationality captured in this window are **never saved**. |
| Health tab | Existing entries cannot be edited, only deleted and re-added. |
| Registrations | Only **active** classes and **active** sessions appear in the dropdowns. |
| Registrations | The registration takes the parent from the Child Data tab. No parent selected means no parent attached. |
| Children | There is no quick activate/deactivate button — you must open and save the record. |
| Staff table view | The **Password** column shows real passwords in plain text. |
| Staff table view | **Copy**, **PDF**, **Print**, **CSV**, **Column visibility** and the entries selector are all inert. |
| Staff list | Search and filters exist only in table view, but still apply in card view. |
| Staff form | Password pre-filled with `123456` — it is real. |
| Staff form | Generate the username **after** choosing the role, or it carries a generic code. |
| Staff list | The thumbs-up status toggle acts instantly with no confirmation, right under the delete button. |
| Staff | Class assignment is not available on this page at all. |
