# Attendance and Daily Reports

Procedures for nursery staff using the Peekaboo portal at https://peek.peek-a-boo.app

**How to read this guide.** Plain text describes what the screen contains and what each control does, taken directly from the live version of the portal. Anything written under a line beginning **Not yet checked on a live system** describes what is expected to happen after you press a button, and has not been confirmed by watching a real nursery account. Treat those notes as "probably, but confirm the first time you do it".

---

## Read this first: recording illness, injury or a temperature

The daily report form shows a **Health Status** card and a **Temperature** card. You can select **Healthy**, **Mild Concern** or **Sent Home**, and you can type a temperature in degrees Celsius. These two cards are helpful while you are filling the form in and they will show a **Elevated** flag at 38 degrees or above, but the values in those two cards are not part of what gets sent when you press **Save Draft** or **Publish**. They will not appear on the saved report and they will not reach the parent.

So whenever there is anything at all about illness, injury, a temperature reading or a child being sent home:

1. Write it in full in the **Note to parents** box, and if it affected the child's day, also in **Activities & behaviour**. Both of these boxes are saved with the report and both reach the parent.
2. Include the actual numbers and times in that text, for example "Temperature 38.4C taken at 13:20, parent called at 13:30."
3. Tell your room lead in person as well. Do not rely on the report alone to raise a concern.
4. If medicine was given, also fill the **Medicine** box in the **Daily Care** card. That one is saved.

Filling in **Health Status** and **Temperature** does no harm. Just never let them be the only place the information exists.

---

# Children's attendance

### How to mark a child present, late, absent or excused

**Who can do this:** Any staff member whose portal login can open the Operations group in the sidebar.

**Where:** Sidebar group **Operations**, item **Children Attendance**, at `/app/attendance`.

**Before you start:** This screen always works on today's date, and only today. The date is shown at the top of the page next to the word **NOS** and is taken from the device you are using. There is no date picker on this screen, so you cannot use it to go back and fill in a previous day. For any other date, use **Attendance Reports** to look at what was recorded, and see the note at the end of this section.

**Steps:**

1. Open **Children Attendance** from the **Operations** group in the sidebar.
2. Wait for the list to fill in. While it loads, the table shows **Loading attendance...**. If no children come back at all it shows **No children found**.
3. Optionally narrow the list to one room using the round filter buttons above the table. The first is **All** and the rest are your classroom names.
4. Find the child's row. The **Child** column shows their name and, if they have allergies recorded, the word **Allergy** in red underneath.
5. In the **Update Status** column, press one of the four buttons: **Present**, **Late**, **Absent** or **Excused**.

The currently applied status is the button drawn with a ring around it, and it is also shown as a coloured pill in the **Status** column.

**What the four buttons do to the times:**

- **Present** and **Late** set a check-in time. If the child already had a check-in time it is kept as it was; if not, the current clock time is filled in for you.
- **Absent** and **Excused** clear both the check-in and check-out times.

**The options in full:**

| Button you press | Shown in the Status column as | Meaning in use |
| --- | --- | --- |
| **Present** | **Present** | Child is in and attending normally |
| **Late** | **Late** | Child is in, arrived after the expected time |
| **Absent** | **Absent** | Child is not in |
| **Excused** | **Excused** | Child is not in, and the absence is authorised |
| (nothing pressed yet) | **Not Marked** | No attendance decision has been recorded today |

**Not Marked** is not a button you can press. It is what the **Status** column shows for any child nobody has marked yet today. It cannot be set deliberately and cannot be undone once you have marked a child; the nearest equivalent is to set the correct status instead.

**After you save:**

> **Not yet checked on a live system:** pressing a status button sends the change immediately, with no extra confirmation step. A green message reading **Attendance updated** is expected on success. If it does not go through, the message is either the reason sent back by the system or the fallback **Failed to update attendance**. The four status buttons and the **Checkout** button are all disabled while a save is in progress.

**Good to know:**

- The four counters across the top of the page, each labelled **Present**, **Absent**, **Late** and **Excused** with **of {n} total** beneath, count only children who have an attendance record today.
- The check-in and check-out times appear under the status pill, prefixed **In** and **Out**.

---

### How to check a child out at the end of the day

**Who can do this:** Any staff member who can open **Children Attendance**.

**Where:** Sidebar group **Operations**, item **Children Attendance**, at `/app/attendance`.

**Before you start:** The **Checkout** button only appears on a row once all of the following are true: the child's status is **Present** or **Late**, they have a check-in time, they do not already have a check-out time, and their attendance has already been saved once today. If you cannot see the button, the usual reason is that the child has not been marked in yet, or has already been checked out.

**Steps:**

1. Open **Children Attendance**.
2. Find the child's row.
3. Press **Checkout** in the **Actions** column.

The current clock time is used as the check-out time. You are not asked to confirm or to type a time.

**After you save:**

> **Not yet checked on a live system:** a green message reading **Checkout time marked** is expected on success, and the **Out** time should then appear under the child's status. On failure the message is the reason sent back by the system, or the fallback **Failed to mark checkout**.

**Good to know:** To record a check-out at a time other than right now, use **Edit** on the row instead and type the time by hand.

---

### How to correct a child's attendance record, or add a note

**Who can do this:** Any staff member who can open **Children Attendance**.

**Where:** Sidebar group **Operations**, item **Children Attendance**, at `/app/attendance`.

**Before you start:** This panel edits today's record for that child. It is the only place on this screen where you can type an exact time or leave a note.

**Steps:**

1. Open **Children Attendance** and find the child's row.
2. Press **Edit** in the **Actions** column. A panel slides in from the side headed **Edit Child Attendance**, with the line **Update the attendance details for this record.** beneath it.
3. Change **Status** using the dropdown if needed.
4. Type a **Check-In** time and a **Check-Out** time if needed. Both are 24-hour time fields.
5. Type anything the family or the next shift needs to know in **Notes**. The box suggests **Add any handover details, absence reason, or pickup notes.**
6. Press **Save Changes**. To abandon the edit instead, press **Cancel**.

**The options in full — the Status dropdown in the edit panel:**

| Option | Value it records |
| --- | --- |
| **Present** | Present |
| **Absent** | Absent |
| **Late** | Late |
| **Excused** | Excused |

These are the same four statuses as the quick buttons. **Not Marked** is not offered here.

**Good to know:**

- If you set **Status** to **Absent** or **Excused**, the **Check-In** and **Check-Out** boxes empty themselves and grey out, because an absent child has no times. Choose **Present** or **Late** first if you need to enter times.
- If you set **Status** to **Present** or **Late** and there is no check-in time yet, the current clock time is filled in for you. You can type over it.
- The panel's **Classroom** picker and the search box only appear when recording a brand new entry, not when editing an existing row, so when you press **Edit** you will see the status, times and notes only.

**After you save:**

> **Not yet checked on a live system:** a green message reading **Attendance saved** is expected, and the panel should close on its own. On failure the message is the reason sent back by the system, or the fallback **Failed to save attendance**, and the panel stays open so your typing is not lost.

---

### What is not possible on the children's attendance screen

- **You cannot pick a date.** The screen is fixed to today. There is no way to back-fill yesterday or any earlier day from here.
- **There is no bulk "mark everyone present" button.** Each child is marked with their own button press.
- **You cannot delete an attendance record**, only change it to a different status.
- **The picked-up-by name is not something you can type here.** If you need to record who collected a child, put it in the **Notes** box on the **Edit** panel.

---

# Staff attendance

Staff attendance is a separate screen from children's attendance, and **the status options are deliberately different**. Children can be marked **Excused**; staff cannot. Staff can be marked **On Leave**; children cannot. Do not assume the two screens behave alike.

### How to mark a staff member in, absent or on leave

**Who can do this:** Any staff member whose login can open **Staff Attendance**. In practice this is a management or administration task.

**Where:** Sidebar group **Operations**, item **Staff Attendance**, at `/app/staff-attendance`.

**Before you start:** Like the children's screen, this works on today only and has no date picker.

**Steps:**

1. Open **Staff Attendance** from the **Operations** group.
2. Wait for the list. While loading it shows **Loading staff attendance...**; if nothing comes back it shows **No staff found.**
3. Optionally filter by job role using the round buttons along the top. The first is **All** and the rest are your role names.
4. Find the employee's row in the **Employee** column.
5. Press the button you need in the **Actions** column:
   - **Check in** records them as present. This button only appears while the employee has no check-in time yet.
   - **Absent** records them as absent.
   - **Leave** records them as on leave.

**The options in full:**

| Button | Status shown on the row | Appears when |
| --- | --- | --- |
| **Check in** | **Present** | Only while the employee has no check-in time recorded today |
| **Absent** | **Absent** | Always |
| **Leave** | **On Leave** | Always |
| **Checkout** | (status is unchanged) | Only once there is a check-in time and no check-out time |
| (nothing pressed yet) | **Not Marked** | No decision recorded today |

Note the wording difference: the button is labelled **Leave** but the resulting status on the row and in the summary card reads **On Leave**.

A fifth status, **Late**, exists for staff and is shown on the row if it is already set, but there is no quick button for it. To set **Late** you must use **Edit**, described next.

**How the times behave:** **Check in** sets the current clock time as check-in, unless a check-in time already exists, in which case it is kept. **Absent** and **Leave** clear both times.

**After you save:**

> **Not yet checked on a live system:** the change is sent immediately. A green message is expected, either wording sent back by the system or the fallback **Staff attendance saved.** On failure the expected message is the system's reason or the fallback **Attendance could not be saved.** All the buttons on the screen are disabled while a save is running.

**Good to know:** The **Check / Checkout** column shows the two times as pills. A time that has not been recorded shows as `--:--`.

---

### How to check a staff member out

**Steps:**

1. Open **Staff Attendance** and find the employee's row.
2. Press **Checkout** in the **Actions** column.

The current clock time is recorded as the check-out time and the employee's existing status is left unchanged. The button only shows once there is a check-in time and no check-out time yet.

---

### How to correct a staff attendance record, or add a note

**Where:** Sidebar group **Operations**, item **Staff Attendance**, at `/app/staff-attendance`.

**Steps:**

1. Find the employee's row and press **Edit** in the **Actions** column. A dialog opens headed **Edit Staff Attendance**.
2. Choose the **Status** from the dropdown.
3. Type a **Check-In** time and a **Check-Out** time as needed.
4. Add anything relevant in **Notes**.
5. Press **Save Changes**, or **Cancel** to abandon.

**The options in full — the Status dropdown for staff:**

| Option | Notes |
| --- | --- |
| **Present** | |
| **Late** | Only settable here, not from the row buttons |
| **Absent** | |
| **On Leave** | The row buttons call this **Leave** |

There is no **Excused** option for staff. That status exists only for children.

**Good to know:**

- If the employee was **Not Marked**, the dialog opens with **Present** already selected, so check it before saving.
- Unlike the children's edit panel, the staff time boxes are never greyed out, so it is possible to leave times against an **Absent** or **On Leave** record. Clear both boxes yourself if that is not what you mean.
- While saving, the save button reads **Saving...**

**After you save:**

> **Not yet checked on a live system:** the dialog is expected to close by itself on success, with a green confirmation message. On failure the dialog stays open and an error message appears.

---

# Attendance reports

### How to look up attendance history for a date range

**Who can do this:** Any staff member whose login shows the **Reports & Admin** group.

**Where:** Sidebar group **Reports & Admin**, item **Attendance Reports**, at `/app/attendance-reports`.

**Before you start:** This screen is read-only. You cannot mark or change attendance here. It covers both children and staff, one at a time. When you open it, the range is already set from the first day of the current month to today.

**Steps:**

1. Open **Attendance Reports** from the **Reports & Admin** group.
2. Choose who the report is about using the pair of buttons at top left: **Children** or **Staff**.
3. Set the **From** date.
4. Set the **To** date. This field will not accept a date earlier than **From**.
5. Narrow the report using the dropdown to the right. For children it is labelled **Classroom** and lists your classrooms; for staff it is labelled **Role** and lists your job roles. Either way the first option is **All**.
6. Read the grid. Each person is a row, each date in the range is a column.

While the data is arriving the grid shows **Loading attendance report...**. If nobody matches, it shows **No students or staff found for this period.** Switching between **Children** and **Staff** resets the classroom or role dropdown back to **All**.

**The options in full — the marker letters in the grid:**

| Marker | Meaning | Shown on hover as |
| --- | --- | --- |
| **P** | Present, filled green circle | **Present** |
| **A** | Absent, red outline | **Absent** |
| **L** | Late, amber outline | **Late** |
| **V** | On leave, blue outline. Used for staff | **Leave** |
| **E** | Excused, blue outline. Used for children | **Excused** |
| **-** | Nothing was recorded for that person on that day | **Not marked** |

The same key is printed along the bottom of the grid, showing **Present**, **Absent**, **Late**, **Leave** and **Not marked**.

**The summary row across the top of the grid:**

| Column | What it counts |
| --- | --- |
| **Total Working Days** | Number of people multiplied by the number of non-weekend days in the range |
| **Total Present Days** | Days marked present |
| **Total Late Days** | Days marked late |
| **Total Absent Days** | Days marked absent, on leave or excused, added together |
| **Total Not Marked Days** | Working days with nothing recorded |
| **Present %** | Present days as a percentage of total working days |
| **Absent %** | Absent days as a percentage of total working days |
| **Not Marked %** | Not-marked days as a percentage of total working days |

Two things to keep in mind when quoting these figures. Saturdays and Sundays are excluded from the totals and are shaded pink in the grid, regardless of whether your nursery actually opens then. And **Total Absent Days** rolls absence, leave and excused absence into one number, so it is not a count of unauthorised absence on its own.

**How to export or print:**

- Press **CSV** to download a spreadsheet file. It is named after the type and the date range, for example `children-attendance-2026-09-01-2026-09-24.csv`.
- Press **Print / PDF** to open a printable table, headed **Children Attendance Report** or **Staff Attendance Report** to match what you are viewing.

Both buttons are greyed out until there is at least one person in the results. The exported and printed versions use the full words **Present**, **Absent**, **Late**, **Leave**, **Excused** and **Not marked** rather than the single-letter markers.

**Good to know:** The report will not display more than 370 days at once, so keep ranges to under a year.

---

# Daily reports

The daily report is the record that goes to the family. It is filled in one child at a time.

### How to create a daily report for a child

**Who can do this:** Any staff member whose login can open **Daily Reports**, normally the room staff.

**Where:** Sidebar group **Operations**, item **Daily Reports**, at `/app/daily-reports`, then the **New Report** button.

**Before you start:** A new report is always dated today. There is no way to choose a different date when creating one. Only children whose registration is active in the chosen class appear in the list.

Which cards you see depends on the settings for that class, so not every room will show every card described below. A card is hidden only when someone has explicitly switched it off in the class settings.

**Steps:**

1. Open **Daily Reports** from the **Operations** group.
2. Press **New Report** at the top right.
3. Under **Select Class**, press the class you are writing reports for. The child list on the left reloads.
4. Pick the child from the list on the left. Each name shows their initials, and the word **Allergy** in red if allergies are recorded. While the list loads you will see **Loading children...**, and if the class is empty, **No children in this class.**
5. Fill in the cards on the right, described in full below. Until you pick a child, that side reads **Select a child to fill in their report**.
6. Save the report using one of the three buttons at the bottom, described in the next procedure.
7. Pick the next child from the left-hand list and repeat. A green tick appears beside every child you have already saved today, and your typing for each child is kept while you move between them.

**The options in full — every card on the form, in the order it appears:**

**1. Today I Was** — the child's mood. Pick one of five.

| Option |
| --- |
| **Great** |
| **Good** |
| **Okay** |
| **Unsettled** |
| **Upset** |

Note that **Okay** and **Good** are stored as the same value, so a report saved as **Okay** may read back as **Good** when you view it later. If the distinction matters, say so in **Note to parents**.

**2. Meals & Drinks** — up to five meals, each with the same set of choices.

| Meal | Extra boxes on that meal |
| --- | --- |
| **Breakfast** | a time, and a free-text box prompting **Add a comment…** |
| **Snack AM** | a time, and a comment box |
| **Lunch** | a time, and a comment box |
| **Snack PM** | a time, and a comment box |
| **Milk** | a time, and a box labelled **ML amount** instead of a comment |

For each meal, choose how much was eaten:

| Option | Meaning |
| --- | --- |
| **All** | Ate everything |
| **Most** | Ate most of it |
| **Some** | Ate a little |
| **None** | Ate nothing |

For **Snack PM**, be aware that the amount you choose is not currently carried through to the saved report, and the **Milk** amount is only kept if you also fill in the **ML amount** box or the milk time. So for those two, put anything important in the comment box or in **Note to parents** rather than relying on the amount buttons alone.

**3. Nap Time** — pick one of four.

| Option | Effect |
| --- | --- |
| **Slept Well** | Reveals **From** and **To** time boxes |
| **Brief Nap** | Reveals **From** and **To** time boxes |
| **No Nap** | No time boxes |
| **N/A** | No time boxes |

The nap times are what get saved. If you choose **Slept Well** or **Brief Nap** but leave **From** and **To** empty, the nap will not appear on the saved report, so always fill in the two times.

**4. Daily Care** — four free-text boxes.

| Box | Suggested content shown in the box |
| --- | --- |
| **Water** | **e.g. 200 ml** |
| **Juice** | **Amount** |
| **Medicine** | **Details** |
| **Hygiene** | **Notes** |

**Water**, **Juice** and **Medicine** are saved with the report. Anything typed in **Hygiene** is not carried through when the report is saved, so if a nappy change, toileting accident or similar needs to reach the family, write it in **Note to parents** as well.

**5. Items Needed** — four supplies the family may need to send in. Each one is a pair of buttons, **Yes** and **No**.

| Item |
| --- |
| **Diapers** |
| **Clothes** |
| **Wipes** |
| **Cream** |

Anything you leave untouched is saved as not needed, so you only need to press **Yes** on the ones that apply.

**6. Health Status** — three choices: **Healthy**, **Mild Concern**, **Sent Home**. See the safety section at the top of this guide: these selections are not saved with the report. Put the detail in **Note to parents** and tell your room lead.

**7. Temperature** — a number in degrees Celsius, with **36.6** shown as an example. Readings of 38.0 and above are flagged **Elevated**, anything lower **Normal**, and the card reminds you **Leave blank if not taken. Flagged automatically at 38°C+.** As above, this reading is not saved with the report, so write the number into **Note to parents** too.

**8. Teacher Note** — two free-text boxes, and the most important part of the form because both are saved and both reach the family.

| Box | Suggested content shown in the box |
| --- | --- |
| **Note to parents** | **Write a message for the family…** |
| **Activities & behaviour** | **What did the child do today? How did they behave?** |

---

### How to save, publish, or publish and email a daily report

**Where:** The row of buttons at the bottom of the report form.

**Steps:** Press one of the three buttons.

**The options in full:**

| Button | What it does |
| --- | --- |
| **Save Draft** | Stores the report without marking it as sent. It appears in the list with a **Draft** badge. Use this when the day is not finished. |
| **Publish** | Stores the report and stamps it as sent, so it shows a **Published** badge. This is the normal end-of-day action. |
| **Publish & Email** | Publishes the report and then emails it to the family in one step. |

**Publish & Email** does both things in sequence, so you do not need to press **Publish** first.

**After you save:**

> **Not yet checked on a live system:** a green message reading **Daily report published** or **Daily report saved** is expected. If it fails, the expected message is the reason sent back by the system or the fallback **Unable to save daily report**.

> **Not yet checked on a live system:** after **Publish & Email** succeeds, the expected message names how many people it reached, in the form **Report published and emailed to** followed by a number and **recipient(s)**. If the email part fails the expected message is **Unable to publish and email report**, or **Email failed**. Because the publish happens before the email, a failed email does not necessarily mean the report was not saved. Check the list for the **Published** badge before trying again.

**Good to know:**

- Pressing **Save Draft** and then **Publish** for the same child updates the one report rather than creating a second one.
- A line reading **Report saved for** followed by the child's name appears under the buttons once you have saved that child at least once in this sitting.
- The buttons are disabled while a save is running.

---

### How to find and read a report from an earlier day

**Where:** Sidebar group **Operations**, item **Daily Reports**, at `/app/daily-reports`.

**Steps:**

1. Open **Daily Reports**. It opens on today's date.
2. Change the date box at the top left to the day you want. Unlike the attendance screens, this one does let you choose any date.
3. Optionally narrow by room with the dropdown beside it. The first option is **All Classrooms**.
4. Press a child in the left-hand list to open their report on the right.

The heading line counts how many reports match, as a number followed by **published** and a number followed by **drafts**.

**What the left-hand list tells you:**

| What you see on the row | Meaning |
| --- | --- |
| A mood face and **Published** in green | A report exists and has been sent |
| A mood face and **Draft** in amber | A report exists but has not been sent |
| **Report not created** in red | No report was written for that child on that date |
| An envelope button | Emails that report to the family. Greyed out when no report exists |

If nobody matches the date and room you chose, the list reads **No reports for this date.** If you open a child with no report, the right-hand side reads **No report available** with the explanation **This child does not have a daily report for this date.** and a **Create Report** button. Note that **Create Report** starts a report dated today, not for the date you were looking at.

**What the opened report shows:** the child's name, the date and the room, then the mood, the health status badge, **Meals**, **Daily Care**, **Items Needed**, **Nap**, **Comment**, **Teacher Note**, and at the bottom either **Parent viewed** or **Parent has not viewed yet**.

**Good to know:** Because health status is not stored with the report, every saved report displays **Healthy** on this screen. It reflects the stored blank value, not an assessment anyone made of the child. This is another reason to put anything health-related into the note text.

---

### How to correct a report after it has been saved

**Where:** Sidebar group **Operations**, item **Daily Reports**, with a report open on the right.

**Before you start:** Only the **Teacher Note** can be edited once a report has been saved. Moods, meals, nap, care and items needed cannot be changed from this screen.

**Steps:**

1. Open the report as described above.
2. Find the **Teacher Note** section and press the small pencil button beside the heading.
3. Edit the text in the box.
4. Press **Save**, or **Cancel** to abandon the change.

**After you save:**

> **Not yet checked on a live system:** a green message reading **Report updated** is expected, and the box should close back to plain text. On failure the expected message is the reason sent back by the system or the fallback **Update failed**.

**Good to know:**

- If a report has been edited, a line reading **Edited {n} times** appears under the note, with the number in place of `{n}`.
- If something other than the note is wrong, the practical fix is to explain the correction in the **Teacher Note** and tell the family directly. There is no way to rewrite the meals or nap on a saved report from this screen.

---

### How to email a saved report to a family

**Steps:**

1. Open **Daily Reports** and set the date and room so the child appears in the list.
2. Press the envelope button on the right of that child's row. It shows a spinner while it sends.

The envelope is greyed out for any child whose row reads **Report not created**; hovering it explains **Report not created yet**. On a row that does have a report, hovering shows **Email parent**.

**After you save:**

> **Not yet checked on a live system:** a green message naming the number of recipients is expected, in the form **Report emailed to** followed by a number and **recipient(s)**, or **Report sent successfully** when no count comes back. On failure the expected message is the system's reason or the fallback **Send failed**.

**Good to know:** You can email a report that is still a **Draft**. The badge and the email are independent, so check the badge before sending if you meant to publish it first.

---

## Quick reference: every attendance status

| Status label | Children's attendance | Staff attendance | Marker in reports |
| --- | --- | --- | --- |
| **Present** | Yes, quick button and dropdown | Yes, via **Check in** and dropdown | **P** |
| **Late** | Yes, quick button and dropdown | Dropdown only, no quick button | **L** |
| **Absent** | Yes, quick button and dropdown | Yes, quick button and dropdown | **A** |
| **Excused** | Yes, quick button and dropdown | Not available | **E** |
| **On Leave** | Not available | Yes, quick button labelled **Leave** | **V** |
| **Not Marked** | Display only, cannot be set | Display only, cannot be set | **-** |
