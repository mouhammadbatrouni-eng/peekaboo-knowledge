# Curriculum and Assessment

Procedures for nursery staff using the Peekaboo portal at <https://peek.peek-a-boo.app>.

Everything written in plain text below was read directly from the software your nursery is
running. Anything that depends on what the server sends back after you press a button is
marked with a **Not yet checked on a live system** note, because that cannot be confirmed
from the software alone.

---

## How the curriculum fits together

The whole of Early Childhood hangs off one record: the **Curriculum**. Nothing else in this
section can be created until at least one curriculum exists.

A curriculum is a container, not a scale or a syllabus. Three different kinds of record hang
directly off it, and each one is created on its own screen:

```
Curriculum
├── Learn Area ──── Aspect          (what is being learned)
├── Age Group                       (which band of months)
└── Attainment                      (how well it was done)
```

- **Curriculum** is the top level. It has a name, a description, a picture and an on/off
  switch. Most nurseries will have one.
- **Learn Area** is a broad strand of learning, and it belongs to exactly one curriculum.
  You pick the curriculum when you create the learn area.
- **Aspect** sits *inside* a learn area. Aspects are not created on a screen of their own,
  and they do not appear in the sidebar. You reach them by opening an existing learn area
  for editing: the aspect list appears in the edit form and is hidden when you are creating
  a new learn area. An aspect belongs to one learn area and carries no curriculum of its own.
- **Age Group** is a band of months (for example 24 to 36). It belongs to one curriculum and
  is picked from a list when you create it. Age groups are independent of learn areas.
- **Attainment** is a level of achievement. It also belongs to one curriculum. Attainment
  levels are *not* a fixed built-in scale. Each nursery types in its own level names and
  gives each one a number and a colour. If you want three levels, you create three records;
  if you want six, you create six.
- **Objectives** are the individual "can do" statements. They sit underneath an *aspect* and
  an *age group* together, not under a learn area directly. There is no Objectives screen in
  your menu, so objectives are not something you create or edit in the portal. You only ever
  meet them while writing an observation, where you tick the ones a child has shown.

**Classes sit outside this tree.** A class is a real room of children. It links to the
curriculum tree at exactly one point: you choose an **Age Group** when you set up the class.
A class has no direct link to a curriculum, a learn area or an attainment level.

Two things follow from this, and they matter when you plan your setup order:

1. You must create the **Curriculum** first, then **Age Groups**, before you can create a
   **Class**, because the class form requires an age group and the age group form requires a
   curriculum.
2. When you write an **Observation** you choose the curriculum, learn area, aspect and age
   group yourself on the observation screen. The observation does **not** inherit the
   curriculum from the child's class. The age group you pick on the observation screen is
   the one used to look up objectives, regardless of which age group the child's class is
   set to.

**The order to build things in:**

```
1. Curriculum
2. Learn Area  ──► then open it again to add Aspects
3. Age Groups
4. Attainment levels
5. Classes                     (needs an Age Group)
6. Children registered into a class   (done on the child's record, not here)
7. Observations                (needs all of the above)
8. Assessment Reports          (needs a class and a date range)
```

**Where children come from.** You cannot add a child to a class from any screen in this
section. Children are put into classes from the child's own record, by adding a
**Registration** that names a **Class** and a **From / To Date**. The Classes screen only
sets how many children the room is *for*; it does not hold the list of who they are.

---

## Classes

### How to view the list of classes

**Who can do this:** Staff whose role includes the Classes permission. Accounts with the top
administrator role can always reach it.

**Where:** Sidebar group **Early Childhood**, item **Classes**.
`https://peek.peek-a-boo.app/app/early-childhood/classes`

**Before you start:** Nothing.

**Steps:**

1. Open **Classes** from the sidebar.
2. The page opens in card view. Each card shows the class name, an **Active** or **Inactive**
   badge, the centre name and the age group code.
3. To switch to the detailed table, click the table icon in the top right of the page header.
   To switch back, click the grid icon beside it.

**Good to know:**

- The table view has extra columns the cards do not: **Status**, **Class Name**, **Center**,
  **Class Logo**, **Age Group**, **Class Description**, **No. of Children**,
  **Teacher Ratio**, **Teachers** and **Actions**.
- The filter dropdown (**All** / **Active** / **Inactive**) and the **Search classes** box
  only exist in table view. If you want to search or filter, switch to the table first.
- When there are no classes to show, the table reads **No classes found.**

### How to create a class

**Who can do this:** Staff whose role includes the Classes permission.

**Where:** Sidebar group **Early Childhood**, item **Classes**.
`https://peek.peek-a-boo.app/app/early-childhood/classes`

**Before you start:** At least one **Age Group** must already exist, which means a
**Curriculum** must exist too. If none does, the age group dropdown will read
**No age groups found** and you will not be able to save.

**Steps:**

1. Open **Classes** from the sidebar.
2. Click **Add Class** in the top right.
3. The form opens on the **Class Details** tab.
4. Type the **Class Name**. This is required.
5. Fill in the remaining details listed in the table below.
6. Choose an **Age Group** from the dropdown. This is required.
7. Enter **No. of Children** and **Teacher Ratio**. Both are required.
8. In the **Teachers assigned to this class** box, click a teacher's name to assign them.
   Click the name again to remove them. The counter beside the heading updates as you go.
9. To add a picture, click **Browse** in the **Class Logo** box and pick an image file. The
   picture appears in the box straight away.
10. If you want to change what families see in the daily report, click the **Class Settings**
    tab and use the switches. Each switch is labelled **No / Yes**.
11. Click **Save Class**.

**The form in full — Class Details tab:**

| Field | Required? | What to enter | Options |
| --- | --- | --- | --- |
| **Class Name** | Yes | The room's name as staff and families will see it | Free text |
| **Class Description** | No | A short note about the room | Free text |
| **Age Group** | Yes | The age band this room follows | A list of your age groups. Note the dropdown shows each age group's *description*, not its code |
| **No. of Children** | Yes | A whole number, 0 or more | Number |
| **Teacher Ratio** | Yes | A whole number, 1 or more | Number |
| **Status** | No | Whether the class is in use | **Active** or **Inactive**. Starts on **Active** |
| **Class Online URL** | No | A web address for an online session | Free text |
| **Teachers assigned to this class** | No | Click names to select | Your staff list. Click to add, click again to remove |
| **Class Logo** | No | A picture for the class | Any image file, chosen with **Browse** |

**The form in full — Class Settings tab:**

Every item here is an on/off switch controlling whether families see that item in this
class's daily report. The switches are grouped under these headings:

| Heading | Switches |
| --- | --- |
| **Daily Care** | **Mood Visible**, **Comment Visible**, **Water Visible**, **Juice Visible**, **Medicine Visible**, **Nap Visible**, **Hygiene Visible** |
| **Breakfast** | **Breakfast Visible**, **Breakfast Time Visible**, **Breakfast Comment Visible** |
| **Snack 1** | **Snack 1 Visible**, **Snack 1 Time Visible**, **Snack 1 Comment Visible** |
| **Lunch** | **Lunch Visible**, **Lunch Time Visible**, **Lunch Comment Visible** |
| **Snack 2** | **Snack 2 Visible**, **Snack 2 Time Visible**, **Snack 2 Comment Visible** |
| **Milk** | **Milk Visible**, **Milk Time Visible**, **Milk ML Visible** |
| **Health Tracking** | **Temperature in Daily Report** |

**After you save:**

- If a required field is empty you are stopped before anything is sent, and a red message
  appears: **Class name is required.**, **Age group is required.**,
  **No. of children is required.** or **Teacher ratio is required.**
- The button reads **Saving...** while the save is in progress.
- On success the message is **Class saved successfully.** and the form clears itself.
- If the save is refused the message is **Class could not be saved.** or
  **Failed to save class.**

> **Not yet checked on a live system:** whether the new class appears in the list without a
> page refresh, and whether the server sends back its own wording in place of the messages
> above. The portal will show the server's wording when it supplies any.

**Good to know:**

- The **Temperature in Daily Report** switch is shown on the Class Settings tab but it is
  not among the settings sent when you save. If your nursery needs a record of whether
  temperature is shown to families, keep that note outside the portal rather than relying on
  this switch to hold it.
- **No. of Children** is the room's number. It is the same number that later shows in the
  **No. of Children** column. It does not count who is actually registered.
- Choosing an age group does not ask you for a curriculum. The class takes the curriculum
  the age group already belongs to.

### How to edit a class

**Who can do this:** Staff whose role includes the Classes permission.

**Where:** Sidebar group **Early Childhood**, item **Classes**.
`https://peek.peek-a-boo.app/app/early-childhood/classes`

**Before you start:** The class must already exist.

**Steps:**

1. Open **Classes** from the sidebar.
2. Find the class. In card view click the pencil icon on the card; in table view click the
   pencil icon in the **Actions** column.
3. The form opens with the heading **Edit Class** and the page scrolls to the top.
4. Change whatever you need on the **Class Details** and **Class Settings** tabs. All the
   fields behave exactly as they do when creating a class.
5. Click **Save Changes**.

To abandon your changes, click **Cancel** instead. This returns you to the list.

**After you save:**

- The button reads **Saving...** while the save is in progress.
- On success the message is **Class updated successfully.**
- If the save is refused: **Class could not be saved.** or **Failed to save class.**

> **Not yet checked on a live system:** whether the teachers already assigned to the class
> are shown as selected when the form first opens. The form asks the server for the current
> assignments as it opens, so give it a moment before you start clicking teacher names, and
> check the count beside **Teachers assigned to this class** reflects reality before saving.

### How to delete a class

**Who can do this:** Staff whose role includes the Classes permission.

**Where:** Sidebar group **Early Childhood**, item **Classes**.
`https://peek.peek-a-boo.app/app/early-childhood/classes`

**Before you start:** Be aware that children are registered against classes on their own
records.

**Steps:**

1. Open **Classes** from the sidebar.
2. Click the bin icon on the card, or in the **Actions** column of the table.
3. A box appears headed **Delete Class** asking **Are you sure?**
4. Click **Yes** to delete, or **Cancel** to stop.

**After you delete:**

- On success the message is **Class deleted successfully.**
- If the deletion is refused: **Class could not be deleted.** or **Failed to delete class.**

> **Not yet checked on a live system:** what happens to children currently registered to the
> class, and to observations already recorded against it. The portal asks the server to
> delete and shows whatever the server replies. Before deleting a class that has been in use,
> check with whoever administers your system.

---

## Curriculum

### How to view, create and edit a curriculum

**Who can do this:** Staff whose role includes the Curriculum permission.

**Where:** Sidebar group **Early Childhood**, item **Curriculum**.
`https://peek.peek-a-boo.app/app/early-childhood/curriculum`

**Before you start:** Nothing. This is the first record to create.

**Steps to create:**

1. Open **Curriculum** from the sidebar. The list is on the left, the form on the right under
   the heading **Add Curriculum**.
2. Type the **Curriculum Name**. You cannot save without it.
3. Type a **Description** if you want one.
4. To add a picture, click **Browse** in the **Image** box and choose a file. It appears in
   the preview area, which otherwise reads **Drag or browse an image preview**.
5. The **Enabled** tickbox is ticked by default. Untick it to mark the curriculum inactive.
6. Click **Save Curriculum**.

**Steps to edit:**

1. Click the curriculum's name in the list, or the pencil icon in the **Actions** column.
2. The form heading changes to **Edit Curriculum** and fills with the existing details.
3. Change what you need and click **Save Curriculum**.

To empty the form and start again, click **Clear**.

**The form in full:**

| Field | Required? | What to enter | Options |
| --- | --- | --- | --- |
| **Curriculum Name** | Yes | The name of the curriculum | Free text |
| **Description** | No | A longer note. Shown under the name in the list | Free text, multiple lines |
| **Image** | No | A picture for the curriculum | Any image file, chosen with **Browse** |
| **Enabled** | No | Whether the curriculum is active | Tickbox. Ticked by default |

**The list columns:** **Curriculum**, **Image**, **Status**, **Actions**. The status shows
**Active** or **Inactive**. Where no picture has been added the image cell reads **No image**.
An empty list reads **No curriculum records found.**

**After you save:**

- The button reads **Saving...** when creating and **Updating...** when editing.
- On success the message is **Curriculum saved successfully.** and the form clears.
- If it fails: **An error occurred while saving the curriculum.**

> **Not yet checked on a live system:** whether the list refreshes on its own after a save,
> and whether the server replaces the wording above with its own.

**Good to know:** There is no tickbox or field for the curriculum's status in the list view
other than the badge. The badge is styled the same way whether the curriculum is active or
inactive, so read the word itself rather than the colour.

### How to delete a curriculum

**Steps:**

1. Open **Curriculum** from the sidebar.
2. Click the bin icon in the **Actions** column.
3. A box appears headed **Delete Curriculum** asking **Are you sure?**
4. Click **Yes**, or **Cancel** to stop.

**After you delete:**

- On success: **Curriculum deleted successfully.**
- If refused: **Curriculum could not be deleted.** or **Failed to delete curriculum.**

> **Not yet checked on a live system:** what happens to the learn areas, age groups and
> attainment levels that belong to the curriculum. Since everything in Early Childhood hangs
> off the curriculum, treat deleting one as a significant action and check with whoever
> administers your system first.

---

## Learn Area

### How to view, create and edit a learn area

**Who can do this:** Staff whose role includes the Learn Area permission.

**Where:** Sidebar group **Early Childhood**, item **Learn Area**.
`https://peek.peek-a-boo.app/app/early-childhood/learning-area`

**Before you start:** At least one **Curriculum** must exist. The curriculum dropdown is
required and you cannot save without choosing one.

**Steps to create:**

1. Open **Learn Area** from the sidebar. The list is on the left under the heading
   **Learn Area**, the form on the right under **Add Learn Area**.
2. Type the name in the **Learn Area** box. You cannot save without it.
3. Choose a **Curriculum** from the dropdown. It starts on **Select Curriculum** and is
   marked with a red asterisk.
4. Fill in **Area Curriculum**, **Description** and **Color** as needed.
5. The **Enabled** tickbox is ticked by default.
6. Click **Save Learn Area**.

**Steps to edit:**

1. Click the pencil icon in the **Actions** column of the list.
2. The form heading changes to **Edit Learn Area**. The **Learning Aspects** panel now
   appears at the bottom of the form.
3. Change what you need and click **Update Learn Area**.

To empty the form, click **Clear**. Note that clearing also closes the aspects panel, because
that panel only shows while you have a learn area open for editing.

**The form in full:**

| Field | Required? | What to enter | Options |
| --- | --- | --- | --- |
| **Learn Area** | Yes | The name of the learning strand | Free text |
| **Curriculum** | Yes | Which curriculum this strand belongs to | A list of your curricula. Starts on **Select Curriculum** |
| **Area Curriculum** | No | A short label. This is what appears on the coloured buttons when writing an observation | Free text |
| **Description** | No | A longer note. Shown under the name in the list | Free text |
| **Color** | No | The colour used for this area's button when writing an observation | Colour picker. Starts on a light blue |
| **Enabled** | No | Whether the area is active | Tickbox. Ticked by default |

**The list columns:** **Learn Area**, **Curriculum**, **Color**, **Status**, **Actions**.

**After you save:**

- If you have not chosen a curriculum you are stopped with **Curriculum is required.**, shown
  both as a message and in red beneath the dropdown.
- The button reads **Saving...** while saving.
- On success: **Learn area saved successfully.** and the form clears.
- If it fails: **Failed to save learn area.**

> **Not yet checked on a live system:** whether the list refreshes on its own, and whether the
> server supplies its own wording.

**Good to know:** **Area Curriculum** is a confusing name for what it does. It is not a second
curriculum link. It is the short label shown on the coloured **Learn Areas** buttons on the
observation screen. If you leave it empty, the observation screen falls back to showing the
full **Learn Area** name on the button instead.

### How to add or edit an aspect

Aspects sit inside a learn area. There is no Aspects screen and no sidebar entry for them.

**Who can do this:** Staff whose role includes the Learn Area permission.

**Where:** Sidebar group **Early Childhood**, item **Learn Area**, then open a learn area for
editing. `https://peek.peek-a-boo.app/app/early-childhood/learning-area`

**Before you start:** The learn area must already exist and be saved. You cannot add aspects
while creating a new learn area, only while editing a saved one.

**Steps:**

1. Open **Learn Area** from the sidebar.
2. Click the pencil icon beside the learn area you want.
3. Scroll down in the form to the panel headed **Learning Aspects**, with the note
   **Manage aspects for this learning area.**
4. Click **Add Aspect**. A box opens headed **Add Aspect**.
5. Type the name in the **Aspect** box.
6. Type a **Description** if you want one.
7. The **Enabled** tickbox is ticked by default.
8. Click **Save Aspect**, or **Cancel** to abandon.

To change an existing aspect, click the pencil icon beside it in the **Learning Aspects**
table. The box opens headed **Edit Aspect** and the button reads **Update Aspect**.

**The form in full:**

| Field | Required? | What to enter | Options |
| --- | --- | --- | --- |
| **Aspect** | Not enforced | The name of the aspect | Free text |
| **Description** | No | A longer note | Free text |
| **Enabled** | No | Whether the aspect is active | Tickbox. Ticked by default |

**The aspects table columns:** **Aspect**, **Description**, **Actions**. When a learn area has
no aspects the panel reads **No aspects added yet.**

**After you save:**

- On success: **Aspect saved successfully.** and the box closes.
- If it fails: **Failed to save aspect.**

> **Not yet checked on a live system:** whether the aspect list refreshes without reopening the
> learn area. The **Aspect** name is not checked before saving, so an aspect with a blank name
> may be accepted. Type a name before saving.

**To delete an aspect:** click the bin icon beside it. A box appears headed **Delete Aspect**
asking **Are you sure?** Click **Yes** or **Cancel**. If the deletion fails the message is
**Failed to delete aspect.**

> **Not yet checked on a live system:** what happens to objectives that sit under a deleted
> aspect, and to observations that already reference them.

### How to delete a learn area

**Steps:**

1. Open **Learn Area** from the sidebar.
2. Click the bin icon in the **Actions** column.
3. A box appears headed **Delete Learning Area** asking **Are you sure?**
4. Click **Yes**, or **Cancel** to stop.

**After you delete:**

- On success: **Learn area deleted successfully.**
- If refused: **Learn area could not be deleted.** or **Failed to delete learn area.**

> **Not yet checked on a live system:** whether the aspects inside the learn area are removed
> with it.

---

## Age Groups

### How to view, create and edit an age group

**Who can do this:** Staff whose role includes the Age Groups permission.

**Where:** Sidebar group **Early Childhood**, item **Age Groups**.
`https://peek.peek-a-boo.app/app/early-childhood/age-groups`

**Before you start:** At least one **Curriculum** must exist.

**Steps to create:**

1. Open **Age Groups** from the sidebar. The list is on the left, the form on the right under
   the heading **Add Age Group**.
2. Type the **Code**. You cannot save without it.
3. Choose a **Curriculum** from the dropdown. It starts on **Select Curriculum** and is marked
   with a red asterisk.
4. Enter **From Month** and **To Month** as numbers of months.
5. Choose a **Color** and type a **Description** if you want them.
6. Click **Save Age Group**.

**Steps to edit:**

1. Click the pencil icon in the **Actions** column.
2. The form heading changes to **Edit Age Group**.
3. Change what you need and click **Update Age Group**.

To empty the form, click **Clear**.

**The form in full:**

| Field | Required? | What to enter | Options |
| --- | --- | --- | --- |
| **Code** | Yes | A short label for the band, for example `24-36m` | Free text |
| **Curriculum** | Yes | Which curriculum this band belongs to | A list of your curricula. Starts on **Select Curriculum** |
| **From Month** | No | The youngest age in months | Number. Starts at 0 |
| **To Month** | No | The oldest age in months | Number. Starts at 0 |
| **Color** | No | The colour used for this band's button when writing an observation | Colour picker. Starts on a light blue |
| **Description** | No | A longer note | Free text |

**The list columns:** **Code**, **Curriculum**, **From Month**, **To Month**, **Color**,
**Actions**. The list is sorted by **From Month**, youngest first. An empty list reads
**No age groups found.**

**After you save:**

- If you have not chosen a curriculum you are stopped with **Curriculum is required.**
- The button reads **Saving...** while saving.
- On success: **Age group saved successfully.** and the form clears.
- If it fails: **An error occurred while saving the age group.**

**Good to know:**

- **From Month** and **To Month** are in months, not years. A two-to-three-year-old band is
  24 to 36.
- The **Description** is not shown in the list, but it *is* what the **Age Group** dropdown
  displays when you set up a class. If you leave the description blank, that dropdown will
  look empty on the Classes screen even though the age group exists. Fill in the description
  with something recognisable.
- Nothing stops you entering a **To Month** lower than the **From Month**, or creating two
  bands that overlap. Check your numbers yourself.

### How to delete an age group

**Steps:**

1. Open **Age Groups** from the sidebar.
2. Click the bin icon in the **Actions** column.
3. A box appears headed **Delete Age Group** asking **Are you sure?**
4. Click **Yes**, or **Cancel** to stop.

**After you delete:**

- On success: **Age group deleted successfully.**
- If refused: **Age group could not be deleted.** or **Failed to delete age group.**

> **Not yet checked on a live system:** what happens to classes that use the age group, and to
> objectives filed under it. An age group is the only link between a class and the curriculum
> tree, so check before deleting one that is in use.

---

## Attainment levels

Attainment levels are how your nursery describes *how well* a child has shown an objective.
They are **not** a fixed built-in scale. There is no default set. Every level your staff will
see when writing an observation is one that somebody at your nursery typed in on this screen,
and each one belongs to a particular curriculum.

Decide your wording as a team before you start, because these names appear beside every
objective on every observation.

### How to view, create and edit an attainment level

**Who can do this:** Staff whose role includes the Attainment permission.

**Where:** Sidebar group **Early Childhood**, item **Attainment**.
`https://peek.peek-a-boo.app/app/early-childhood/attainment`

**Before you start:** At least one **Curriculum** must exist.

**Steps to create:**

1. Open **Attainment** from the sidebar. The list is on the left under the heading
   **Attainment Levels**, the form on the right under **Add Attainment**.
2. Type the level's name in the **Attainment** box. You cannot save without it.
3. Choose a **Curriculum** from the dropdown. It starts on **Select Curriculum** and is marked
   with a red asterisk.
4. Enter a **Mark**. This is the number used to order the levels.
5. Type a **Description**.
6. Choose a **Color**.
7. Click **Save Attainment**.
8. Repeat for each level your nursery uses.

**Steps to edit:**

1. Click the pencil icon in the **Actions** column.
2. The form heading changes to **Edit Attainment**.
3. Change what you need and click **Update Attainment**.

To empty the form, click **Clear**.

**The form in full:**

| Field | Required? | What to enter | Options |
| --- | --- | --- | --- |
| **Attainment** | Yes | The level's name, for example `Emerging` | Free text |
| **Curriculum** | Yes | Which curriculum this level belongs to | A list of your curricula. Starts on **Select Curriculum** |
| **Mark** | No | A number used to sort the levels, lowest first | Number. Starts at 1 |
| **Description** | No | A longer note explaining what the level means | Free text |
| **Color** | No | The colour the level is shown in on the observation screen | Colour picker. Starts on a dark blue |

**The list columns:** **Attainment**, **Curriculum**, **Color**, **Mark**, **Actions**. The
list is sorted by **Mark**, lowest first. An empty list reads
**No attainment levels found.**

**After you save:**

- If you have not chosen a curriculum you are stopped with **Curriculum is required.**
- The button reads **Saving...** while saving.
- On success: **Attainment saved successfully.** and the form clears.
- If it fails: **Attainment could not be saved.** or **Failed to save attainment.**

**Good to know, and this one matters:**

- On this screen the list and the form both show the **Attainment** name. But on the
  observation screen, the attainment dropdowns show the **Description**, not the name. If you
  leave the description blank, those dropdowns will appear to have blank options when your
  staff are writing observations.

  **Put the wording you want staff to see in the Description field as well as the name.** The
  simplest approach is to enter the same words in both boxes.
- The **Mark** only controls the order the levels appear in on this list. It is not a score.
- Attainment levels are per curriculum. If you have more than one curriculum you will need to
  create a set of levels for each.

### How to delete an attainment level

**Steps:**

1. Open **Attainment** from the sidebar.
2. Click the bin icon in the **Actions** column.
3. A box appears headed **Delete Attainment Level** asking **Are you sure?**
4. Click **Yes**, or **Cancel** to stop.

**After you delete:**

- On success: **Attainment level deleted successfully.**
- If refused: **Attainment could not be deleted.** or **Failed to delete attainment.**

> **Not yet checked on a live system:** what happens to observations that already record that
> level against a child's objective.

---

## Observations

This is the screen teachers use day to day. An observation records what one child did, on one
date, and which objectives that showed, with an attainment level for each objective.

One observation covers **one child**. To record the same activity for three children, you
write three observations.

### How to record an observation

**Who can do this:** Staff whose role includes the Observations permission.

**Where:** Sidebar group **Early Childhood**, item **Observations**.
`https://peek.peek-a-boo.app/app/early-childhood/observation`

**Before you start:** All of the following must already exist, or you will not be able to
finish: a **Curriculum**, a **Learn Area** with at least one **Aspect**, an **Age Group**,
at least one **Attainment** level, a **Class**, and the child must be registered to that
class on their own record. Objectives must already exist under the aspect and age group you
intend to use; you cannot create objectives here.

**Steps:**

1. Open **Observations** from the sidebar.
2. In the top form, choose the **Class** from the dropdown. It starts on **Select Class**.
3. Choose the **Teacher** from the dropdown. It starts on **Select Teacher**.
4. Choose the child from the **Children** dropdown. It starts on **Select Child** and lists
   only children registered to the class you picked in step 2. While it is fetching it shows
   **Loading...**
5. Set the **Date**. It starts on today's date.
6. Type an **Observation Title**.
7. Write what you saw in the **Observation** box.
8. Write what you plan to do next in the **Next Step** box.
9. Move down to the panel headed **Add Objectives** and pick your way down the coloured
   buttons in order, because each one filters the next:
   - **Programs** — click the curriculum. This must be done first; the rows beneath stay empty
     until it is chosen.
   - **Learn Areas** — click a learn area. Click it again to deselect.
   - **Learn Aspects** — click an aspect. This row only appears once the chosen learn area has
     aspects.
   - **Age Groups** — click an age group. Click it again to deselect.
10. The objectives table fills in once you have chosen **both** an aspect and an age group.
    Until then it reads **No data available in table**.
11. Optionally set the **Age Group Attainment** dropdown. This sets the level that gets applied
    by default to each objective you tick from now on. It starts on **-- Select --**.
12. For each objective you want to record, click the objective's wording in the right-hand
    column of the table. A tick appears beside it and it is added to the panel on the right.
13. Set the attainment for each objective using the dropdown in the left-hand column
    (**Attainments**) of the same row. Every objective you select must have an attainment set
    or the save will be refused.
14. Check the panel on the right, headed **View Selected Objectives for** followed by the
    child's name. It groups your choices and shows the attainment beside each one. To take one
    off the list, click the bin icon beside it.
15. Click **Save Observation**.

To empty the whole form and start again, click **Clear**.

**The form in full — the top section:**

| Field | Required? | What to enter | Options |
| --- | --- | --- | --- |
| **Class** | Yes | The room the child is in | Your classes. Starts on **Select Class** |
| **Teacher** | Yes | Who made the observation | Your teaching staff. Starts on **Select Teacher** |
| **Children** | Yes | The child being observed | Children registered to the chosen class. Starts on **Select Child** |
| **Date** | No | The date of the observation | Date picker. Starts on today |
| **Observation Title** | Not enforced | A short heading | Free text |
| **Notes** | Not enforced | See the note below before using this | Free text |
| **Observation** | Not enforced | What you saw | Free text, multiple lines |
| **Next Step** | Not enforced | What you plan to do next | Free text, multiple lines |

**The objective picker in full:**

| Control | Required? | What it does | Options |
| --- | --- | --- | --- |
| **Programs** | Yes | Chooses the curriculum. Everything below depends on it | Coloured buttons, one per curriculum |
| **Learn Areas** | Yes | Narrows to one learning strand | Coloured buttons. Shows the **Area Curriculum** short label, or the full name if that is blank |
| **Learn Aspects** | Yes | Narrows to one aspect within the area | Coloured buttons. Only appears if the chosen area has aspects |
| **Age Groups** | Yes | Chooses which age band's objectives to list | Coloured buttons, one per age group in the curriculum |
| **Age Group Attainment** | No | Sets the default level applied to objectives you tick from here on | Your attainment levels. Starts on **-- Select --** |
| Objectives table, **Attainments** column | Yes, for each chosen objective | Sets the level for that one objective | Your attainment levels. Starts on **-- Select --** |
| Objectives table, right-hand column | Yes, at least one | Click the wording to select or deselect | Your objectives, ten to a page |

**After you save:**

- If something required is missing you are stopped before anything is sent and a red message
  appears. The possible messages are: **Class is required**, **Teacher is required**,
  **Child is required**, **Curriculum is required**, **Learning Area is required**,
  **Learning Aspect is required**, **Age Group is required**,
  **Please select at least one objective**, and
  **Please select attainment for all objectives**.
- On success the message is **Saved successfully** and the whole form clears.
- If it fails: **Failed to save**.

> **Not yet checked on a live system:** whether the new observation appears in the
> **Saved Observations** table without refreshing the page.

**Good to know:**

- **The Notes box is not saved.** There is a **Notes** field on the form and you can type in
  it, but its contents are not included when the observation is sent. Put anything you need
  to keep in the **Observation** box or the **Next Step** box instead. The detail window
  described below has a **Comments** heading that reads from this same unsaved field, so it
  will show **No comments saved.** for every observation. If you need comments attached to a
  child's record, use the comment boxes on the **Assessment Report** screen, which do save.
- **There is nothing to attach.** The observation form has no photo, file or video upload.
  The only picture in Early Childhood is the class logo and the curriculum image. If you need
  to keep a photograph with an observation, store it wherever your nursery normally keeps
  photographs and describe it in the **Observation** text.
- Changing the **Class** empties the **Children** dropdown and clears your chosen objectives,
  so pick the class before anything else.
- Changing the **Programs** button clears the learn area, aspect, age group and every
  objective you had chosen. Pick the curriculum before you start ticking.
- If more than ten objectives match your filters, use the numbered page buttons under the
  table. Objectives you have already ticked stay ticked when you change page.
- The right-hand panel has a heading **Saved Summary For This Child** for a child's previously
  saved objectives. In this version that summary is always empty, so the panel shows only what
  you have selected in this sitting. To see a child's earlier observations, use the
  **Saved Observations** table at the bottom of the page.

> **Not yet checked on a live system:** whether the **Children** dropdown fills in reliably
> after you choose a class. If it stays empty, first confirm the child has a current
> **Registration** to that class on their own record; if it is still empty, report it to
> whoever administers your system.

### How to view a saved observation

**Steps:**

1. Open **Observations** from the sidebar and scroll to the table headed
   **Saved Observations**. Underneath it a count reads either
   **1 saved observation** or, for example, **7 saved observations**.
2. Find the row you want. The columns are **Observation**, **Child**, **Class**, **Date**,
   **Objectives** and **Actions**. The **Objectives** column shows how many objectives were
   recorded.
3. Click the eye icon in the **Actions** column.
4. A window opens headed **Observation Details** showing the title, then four sections:
   **Observation**, **Comments**, **Next Step** and **Objectives**.
5. Click **Close** to shut the window.

**Good to know:** the **Comments** section reads from the unsaved **Notes** field, so it will
show **No comments saved.** for every observation. The **Objectives** section shows a count
followed by **objective(s)**, not the objectives themselves. To see the actual objectives,
open the observation for editing.

When there are no observations the table reads **No observations have been saved yet.**

### How to edit an observation

**Steps:**

1. Open **Observations** from the sidebar and find the row in **Saved Observations**.
2. Click the pencil icon in the **Actions** column.
3. The form at the top fills with the saved details and the objective picker reopens on the
   learn area, aspect and age group that were used.
4. Change the **Date**, **Observation Title**, **Observation** and **Next Step** as needed, and
   add or remove objectives and change their attainment levels exactly as when creating.
5. Click **Save Observation**.

**The three things you cannot change:** **Class**, **Teacher** and **Children** are all locked
when editing. Each is greyed out and its label carries the note **(Cannot be changed)**. If you
recorded an observation against the wrong child, delete it and write a new one.

**After you save:**

- On success: **Saved successfully** and the form clears.
- If it fails: **Failed to save**.

> **Not yet checked on a live system:** if an observation was saved with objectives drawn from
> more than one learn area or aspect, the picker reopens showing only the first one. The
> objectives from the other groupings are still listed in the right-hand panel and are still
> saved. Check the right-hand panel before saving so you can see everything that will be kept.

### How to delete an observation

**Steps:**

1. Open **Observations** from the sidebar and find the row in **Saved Observations**.
2. Click the bin icon in the **Actions** column.
3. A box appears headed **Delete Observation** asking **Are you sure?**
4. Click **Yes**, or **Cancel** to stop.

**After you delete:** on success the message is **Deleted successfully**.

> **Not yet checked on a live system:** whether the row disappears from the table without a
> refresh, and what is shown if the server refuses. A failed deletion may not display a
> message, so if the row is still there after you refresh, assume it was not deleted.

---

## Assessments

### How to use the Assessments screen

**Who can do this:** Staff whose role includes the Assessments permission.

**Where:** Sidebar group **Early Childhood**, item **Assessments**.
`https://peek.peek-a-boo.app/app/early-childhood/assessment`

**Before you start:** Nothing, though the counts will read zero until observations and reports
exist.

**What this screen does:** It is a summary and a signpost. You cannot create, edit or delete
anything here. It shows three counts and two links.

**Steps:**

1. Open **Assessments** from the sidebar.
2. Read the three counts across the top:
   - **Total Assessments** — how many assessment report records exist.
   - **Children Assessed** — how many different children those records cover.
   - **Total Comments** — how many comments have been written on them.
3. To go and write observations, click **Open Observations** in the panel headed
   **Observation Workflow**.
4. To go and work with reports, click **Open Assessment Report** in the panel headed
   **Assessment Reporting**.

**How it relates to observations:** despite the name, the counts on this page do **not** count
observations. They count the records created on the **Assessment Report** screen. A nursery
with many observations but no generated reports will see zeroes here. Use the
**Saved Observations** table on the Observations screen to see how many observations exist.

---

## Assessment Report

This screen does two separate jobs on one page, and it helps to keep them apart:

1. **Generating** brings up a list of children in a class over a date range, so you can file a
   report with comments for each one. This is a creation step.
2. **The report table** below lists reports already filed, and lets you read them, edit their
   comments, and get the data out.

### How to generate reports for a class

**Who can do this:** Staff whose role includes the Assessment Report permission.

**Where:** Sidebar group **Early Childhood**, item **Assessment Report**.
`https://peek.peek-a-boo.app/app/early-childhood/assessment-report`

**Before you start:** The class must exist and have children registered to it. At least one
**Learn Area** must exist, because each report row requires an **Area**.

**Steps:**

1. Open **Assessment Report** from the sidebar.
2. Set the **From Date**.
3. Set the **To Date**.
4. Choose the **Class**. The dropdown starts on **All classes**, but you must pick a specific
   class; leaving it on **All classes** is treated as not choosing one.
5. Click **Generate Report**. The button reads **Generating...** while it works.
6. A table appears headed **Generated Reports** with one row per child. Its columns are
   **Child Name**, **Area**, **Comments** and **Actions**.
7. For each child, choose an **Area** from the dropdown in that row. It starts on
   **Select Area**.
8. Type a comment in the box in the **Comments** column. Its placeholder reads
   **Comment 1**.
9. To add more comments for the same child, click **+ Add Comment**. Another box appears,
   with the placeholder **Comment 2**, and so on.
10. Click **Save Comments** in that child's **Actions** column. Each child is saved separately.
11. Repeat steps 7 to 10 for each child you want to file a report for.

**The filters in full:**

| Field | Required? | What to enter | Options |
| --- | --- | --- | --- |
| **From Date** | Yes | Start of the period | Date picker |
| **To Date** | Yes | End of the period. Must not be earlier than **From Date** | Date picker |
| **Class** | Yes | The class to report on | Your classes. Starts on **All classes**, which is not accepted |

**Each generated row in full:**

| Field | Required? | What to enter | Options |
| --- | --- | --- | --- |
| **Area** | Yes | The learn area this report covers | Your learn areas. Starts on **Select Area**. Shows each area's *description* |
| **Comments** | Yes, at least one | What you want to record about the child | Free text. Add more boxes with **+ Add Comment** |

**After you generate:**

- If a date or the class is missing: **Please select a date range and a class.**
- If the dates are the wrong way round: **The from date cannot be after the to date.**
- On success: **Report generated successfully**
- If it fails: **Failed to generate report**
- If no children match, no **Generated Reports** table appears at all.

**After you save a row:**

- If you have not chosen an area: **Please select an area**
- If every comment box is empty: **Please add at least one comment**. Blank boxes are ignored,
  so you can leave spare ones empty.
- On success: **Assessment saved** and that child's row disappears from **Generated Reports**,
  which is how you tell which children you have already done.
- If it fails: **Failed to save assessment**

> **Not yet checked on a live system:** whether the newly saved report appears in the lower
> table without refreshing the page, and what happens if you generate the same class and date
> range twice.

### How to read and update saved reports

**Where:** the lower table on the same page, headed with the export buttons and a
**Search** box.

**The columns:** **Children**, **Class Name**, **Assessment Reports**, **Observation**,
**Area**, **From/To**, **Comments**.

**Steps:**

1. To narrow the list, type into the **Search** box at the top right. It matches against the
   child's name, the class name, the area and the comment text. Note this box filters the
   saved report table only; it has no effect on generating.
2. To read a report's comments, click **Show Comment** in the **Comments** column. The row
   expands underneath. Click **Show Comment** again to collapse it. If there are none it reads
   **No comments yet for this observation.**
3. To change the comments, click **Update** in the same column. The row expands and shows a
   box labelled **Comment Editor**.
4. Edit the text and click **Save Comment**.

**After you save a comment:**

- On success: **Comment saved successfully**
- If it fails: **Failed to save comment**

While the table is loading it reads **Loading assessment reports...** If the search matches
nothing it reads **No report rows match the current filters.**

> **Not yet checked on a live system:** if a report has several comments, the table joins them
> into one line separated by commas, and the **Comment Editor** opens with that joined line.
> Saving from the editor may replace the several comments with the single edited line. If you
> need to change one comment out of several, check the result carefully afterwards.

### What you actually get out: the four export buttons

This is the part most often misunderstood, so here is exactly what each button produces. The
four buttons sit above the saved report table: **Copy**, **PDF**, **Print** and **CSV**. All
four are greyed out while the table is loading or empty.

| Button | What it actually does | Is it a file? |
| --- | --- | --- |
| **Copy** | Puts the whole visible table on your clipboard as text, ready to paste into a spreadsheet or an email | No file. Paste it somewhere |
| **CSV** | Downloads a spreadsheet file named `assessment-reports.csv` to your computer | **Yes, a real file** |
| **Print** | Opens a new browser window containing the table and immediately brings up your browser's print dialog | No file, unless you choose "Save as PDF" in the print dialog |
| **PDF** | Despite the name, this behaves like **Print**. It opens a new browser window and brings up the print dialog | No file, unless you choose "Save as PDF" in the print dialog |

**So: only CSV gives you a file directly.** To get a PDF, use **PDF** or **Print** and then
choose "Save as PDF" as the destination in your browser's print dialog.

Both **Print** and **PDF** need your browser to allow pop-up windows for this site. If pop-ups
are blocked, nothing will appear.

**Copy**, **CSV** and **Print** all produce the same seven columns: **Child**, **Class**,
**Report**, **Area**, **From**, **To**, **Comments**. The printed page is titled
**Assessment Reports**.

**After you export:**

- **Copy** on success: **Report rows copied**
- If any export fails, the message names the action and then reads
  **The action could not be completed**, for example **CSV: The action could not be completed**

### The per-child report buttons

Inside the table, the **Assessment Reports** column has a button on each row labelled
**Assessment Report**. This is different from the four export buttons above: it produces a
formatted one-child page rather than the whole table.

**Steps:**

1. Find the child's row in the saved report table.
2. Click the **Assessment Report** button in the **Assessment Reports** column.
3. A new browser window opens with a formatted page for that child and your browser's print
   dialog appears.
4. Either print it, or choose "Save as PDF" as the destination to get a file.

If the window cannot open, the message is **Could not open the PDF report window.** This
almost always means pop-ups are blocked for this site.

**The page is laid out with:** a heading, then boxes for **Child**, **Class**,
**Date Range**, **Age Group**, **Main Domain** and **Sub Domain**, then sections headed
**Observation**, **Objectives**, **Comments** and **Next Step**.

> **Not yet checked on a live system:** several of those boxes and sections are filled from
> details that the saved report table does not carry, so **Age Group**, **Sub Domain**, the
> **Observation** text, the **Objectives** list and the **Next Step** may come out blank or
> show placeholder wording such as **No comments yet for this observation.** The **Child**,
> **Class**, **Area** and date details are the parts filled from the row you clicked. Before
> sending one of these to a family, open it and read it through. If you need the observation
> text and objectives in a document for a family, the reliable source is the observation
> itself on the Observations screen.

---

## Quick reference: where each thing lives

| I want to... | Go to | Sidebar group |
| --- | --- | --- |
| Set up the top-level programme | **Curriculum** | Early Childhood |
| Set up learning strands | **Learn Area** | Early Childhood |
| Set up aspects | **Learn Area**, then edit an existing area | Early Childhood |
| Set up age bands | **Age Groups** | Early Childhood |
| Define our own achievement levels | **Attainment** | Early Childhood |
| Set up a room | **Classes** | Early Childhood |
| Put a child in a room | The child's own record, **Add Registration** | People → Children |
| Record what a child did | **Observations** | Early Childhood |
| See overall counts | **Assessments** | Early Childhood |
| File and export reports | **Assessment Report** | Early Childhood |
