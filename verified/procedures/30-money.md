# Money in Peekaboo — verified procedures for nursery staff

Every button, field, column and message named in **bold** in this document is a literal
piece of text taken from the version of Peekaboo customers are running. Where a statement
describes what happens *after* you press Save (server messages, numbering, refreshes), it
is marked with a "Not yet checked on a live system" note.

All screens live under `https://peek.peek-a-boo.app`.

---

## How money flows through Peekaboo

Peekaboo keeps two separate sides of the books, and they do **not** talk to each other.

**Money coming in (sidebar group: Account)**

- **Services** is the catalogue. Each service carries a fee, a cost, a VAT percentage and
  a tax-exempt flag.
- **Invoices** bill a child. An invoice picks a child, an invoice type and one or more
  service lines. Each line's fee and VAT percentage are pulled from the Services
  catalogue when you choose the service.
- **Receipts** record money received. A receipt is recorded **against a child**, with one
  or more payment lines. Each payment line names a **Mode of Payment**.
- **Payment Modes** is the list that feeds the **Mode of Payment** dropdown on receipts
  and on payment vouchers.
- **Balance by Class** adds up invoices and receipts per child and shows the difference.

What is genuinely connected: an invoice line points at a service; a receipt payment line
points at a payment mode; Balance by Class reads invoices and receipts.

What is **not** connected — state this plainly to staff, because it drives the whole
reconciliation routine:

- An invoice has **no paid/unpaid status**. There is no status column, no status badge and
  no field anywhere on the invoice screen that marks it as settled.
- A receipt is **not linked to a specific invoice**. You choose a child, and optionally a
  single entry from the **Services** dropdown, but never an invoice number.
- Because of the two points above, you work out who owes what by **comparing totals on
  Balance by Class**, not by looking at an invoice.

**Money going out (sidebar group: Finance)**

- **Suppliers** is the list of people you buy from.
- **Purchases** record what you bought: a supplier, a type, and service lines with
  quantity, fee and VAT.
- **Expenses** record a single spend: a supply category, a type, a supplier, one amount,
  one VAT amount, and a mandatory file attachment.
- **Expense Types** feeds the **Expense Supply** dropdown on the Expenses form.
- **Payment Vouchers** record money paid out to a supplier, as payment lines.

On the money-going-out side, only two links exist: every one of Purchases, Expenses and
Payment Vouchers chooses a **Supplier**, and Expenses chooses an **Expense Supply** from
Expense Types. Beyond that they are **independent records**. Recording a purchase does not
create an expense. Paying a supplier with a payment voucher does not mark any purchase or
expense as paid, and none of these three screens has a paid/unpaid status either.

**Currency.** Amounts on invoice, receipt, purchase, expense and voucher screens are shown
as plain numbers to two decimal places, with no currency symbol. Balance by Class is the
one screen that prints a currency code, and it always prints **AED**, fixed in the
software. The invoice and receipt printouts carry a fixed letterhead reading
**Peekaboo Nursery**, phone **+971 4 123 4567**, email **info@peekaboo.ae**, website
**www.peekabooedu.com** and **VAT TRN: TRN 10000254587895**.

**Who can do this (applies to every procedure below).** Access is per-screen, granted by
your role under **Roles & Access**. The permission names are **Services**, **Invoices**,
**Receipts**, **Payment Modes**, **Balance by Class**, **Suppliers**, **Purchases**,
**Expenses**, **Expense Types** and **Payment Voucher**. A user whose role holds the
permission sees the sidebar entry and can open the screen; one who does not, cannot.
Balance by Class opens for anyone holding **Balance by Class**, **Invoices** or
**Receipts**. The top-level administrator role bypasses these checks and sees everything.
Within a screen there is no finer control: anyone who can open a screen can add, edit and
delete on it.

**Deleting anything.** Every delete on every screen below opens the same confirmation box,
titled **Delete** followed by the record type (for example **Delete Invoice**), asking
**Are you sure?**, with **Cancel** and **Yes**. Nothing is deleted until you press **Yes**.

---

# MONEY COMING IN

## How to view and search the Services catalogue

**Who can do this:** roles holding the **Services** permission.
**Where:** sidebar **Services**, in the **Account** group · `/app/services`
**Before you start:** nothing.

**Steps:**

1. Open **Services** from the sidebar.
2. Read the count under the heading, shown as a number followed by **services configured**.
3. Type into the **Search services...** box to filter. The search looks at the service name
   and the service type only — it does not search the description.
4. Click a column heading to sort by it. **Service Name**, **Service Fee**,
   **Service Type**, **Service VAT** and **Service Cost** are all sortable.
5. Use the page controls beneath the table to move through the list. The table shows 10
   rows per page until you change it.

**What the screen shows:** one row per service with columns **Service Name**,
**Service Fee**, **Service Type**, **Service VAT**, **Service Cost** and **Tax Exempt**.
Fee, VAT and Cost are shown to two decimal places. **Tax Exempt** shows **Yes** or **No**
as a coloured pill. If nothing matches you see **No services found**.

---

## How to create a service

**Who can do this:** roles holding the **Services** permission.
**Where:** sidebar **Services**, **Account** group · `/app/services`
**Before you start:** know the fee you charge, the cost to you, and the VAT percentage.

**Steps:**

1. Open **Services**.
2. Press **Add Service** at the top right. A panel headed **Service** opens.
3. Fill in the form (below).
4. Press **Save**.

**The form in full:**

| Field | Required? | What to enter | Options |
| --- | --- | --- | --- |
| **Services Name** | Yes | The name staff will pick from dropdowns | Free text, at most 255 characters |
| **Services Fee** | Yes | What you charge | Number, zero or more, two decimals |
| **Services Cost** | Yes | What it costs you | Number, zero or more, two decimals |
| **Services Description** | Yes | A short description | Free text, at most 255 characters |
| **Services Type** | Yes | Which kind of item this is | **Services**, **Inventory**, **Resources**, **Expense**. Opens on **Services** |
| **Services MOQ** | No | Minimum order quantity | Number, zero or more. Opens at 0 |
| **Tax Exempt** | No | Whether VAT applies | On/off switch reading **Yes** or **No**. Opens on **No** |
| **Services VAT** | Yes | VAT percentage for this service | Number between 0 and 100 |

Although **Services MOQ** carries no asterisk, leaving it empty blocks the save with
**MOQ must be a non-negative number.** Leave the 0 in place unless you mean to change it.

**How the totals work:** none. This screen stores figures; it calculates nothing. The fee
and VAT you enter here become the starting values for invoice and purchase lines.

**After you save:** if anything is missing you get **Please complete the required fields.**
and the offending boxes turn red with a message underneath — for example
**Service name required**, **Valid service fee is required**, **Valid service cost is
required**, **Service description is required**, **Service name cannot exceed 255
characters.** or **VAT must be between 0 and 100**.

> **Not yet checked on a live system:** on success the screen shows a message sent back by
> the server rather than fixed wording, so the exact text is unconfirmed. The form then
> closes and empties.

**Good to know:**

- The four **Services Type** options are fixed and cannot be added to from this screen.
- **Tax Exempt** here is a property of the catalogue item. It is a separate setting from
  the **Tax Exempt** switch on the invoice, which overrides VAT for the whole invoice.

---

## How to edit or delete a service

**Who can do this:** roles holding the **Services** permission.
**Where:** sidebar **Services**, **Account** group · `/app/services`

**Steps to edit:**

1. Find the service in the table.
2. Press the edit control on its row. The page scrolls up to a panel headed
   **Edit Service**, pre-filled.
3. Change what you need. The fields and rules are exactly as in the create form above.
4. Press **Update**, or **Cancel** to abandon the change.

**Steps to delete:**

1. Press the delete control on the row.
2. The box **Delete Service** asks **Are you sure?**. Press **Yes**.

**Good to know:** editing a service changes the catalogue from that point on. Invoices and
purchases already saved keep the fee and VAT that were copied onto their lines at the time.

---

## How to view, search and print an invoice

**Who can do this:** roles holding the **Invoices** permission.
**Where:** sidebar **Invoices**, **Account** group · `/app/invoices`

**What the screen shows:** the page splits in two. On the left is a scrolling list of
invoices; on the right, the selected invoice laid out as a printable document. Until you
pick one, the right side reads **Select an invoice to view details.**

Each entry in the left list shows the date, the child's name, a blue **INV** badge and the
invoice amount to two decimal places. There is no paid or unpaid marker — Peekaboo does not
record one.

**Steps:**

1. Open **Invoices**. The count under the title reads as a number followed by **invoices**.
2. Type in the **Search invoices...** box to filter. It matches the invoice number, the
   date, the amount and the child's name.
3. Press **Sort** to flip between newest-first and oldest-first by date. Newest first is
   the starting order.
4. Click an entry. The right-hand pane fills with the invoice.
5. Press **Print** to send it to your printer, or **Email** to send it to the parent.

**What the printed invoice contains:** the Peekaboo letterhead; the invoice type as a
heading; **To** with the parent name and child name, plus the parent's phone and email;
**Date**; and **INV#** showing the invoice number padded to eight digits. Then a table with
columns **Service**, **QTY**, **Fee**, **Disc%**, **Disc Amnt**, **VAT%**, **VAT Amnt** and
**Total**, followed by a **Total VAT** row and a **TOTAL** row.

**Good to know:**

- If the child has no parent email on file, **Email** stops and tells you
  **No parent email found for this child.**
- The list shows every invoice; there is no date-range filter and no per-child filter on
  this screen. To see one child's position, use **Balance by Class**.

> **Not yet checked on a live system:** after a successful send the screen shows
> **Invoice emailed to** followed by the address; a failure shows **Failed to send email.
> Please try again.** Whether the parent receives it depends on mail delivery, which is
> outside the screen.

---

## How to create an invoice

**Who can do this:** roles holding the **Invoices** permission.
**Where:** sidebar **Invoices**, **Account** group · `/app/invoices`
**Before you start:** the services you are billing must already exist in **Services**.

**Steps:**

1. Open **Invoices**.
2. Press **Add Invoice**. A panel headed **Add New Invoice** opens with one blank service
   line ready.
3. Set **Date**, **Type** and **Child**.
4. Decide **Tax Exempt** before you enter lines.
5. On the first service row, choose the **Service**. The **Fee** and **VAT (%)** fill in
   automatically from the catalogue.
6. Set **QTY**, and **Fee** and **DISC (%)** if they differ from the defaults.
7. Press **Add Service** to add another row, and repeat. Press the small cross at the end
   of a row to remove it.
8. Check the **Total VAT** and **TOTAL** boxes at the foot of the table.
9. Press **Save**.

**The form in full — invoice header:**

| Field | Required? | What to enter | Options |
| --- | --- | --- | --- |
| **Date** | Yes | The invoice date | Date picker. Opens on today |
| **Type** | Yes | The invoice type | Dropdown of types configured for your nursery; opens on **--Select--** |
| **Child** | Yes | Who is being billed | Dropdown of children; opens on **--Select--** |
| **Tax Exempt** | No | Removes VAT from every line | On/off switch reading **Yes** or **No**. Opens on **No** |

**The form in full — each service line:**

| Column | Required? | What to enter | Options |
| --- | --- | --- | --- |
| **Service** | Yes | The item being billed | Dropdown from the Services catalogue |
| **QTY** | Yes | How many | Whole number, at least 1. Opens at 1 |
| **Fee** | Yes | Price for one | Number, zero or more. Fills from the service, and you may overwrite it |
| **DISC (%)** | No | Discount percentage | Number from 0 to 100. Opens at 0 |
| **DISC Amnt** | — | Calculated | Read-only |
| **VAT (%)** | — | Filled from the service | Read-only, greyed out |
| **VAT Amnt** | — | Calculated | Read-only |
| **Total** | — | Calculated | Read-only |

**How the totals work,** in order, for each line:

1. The discount amount is the fee times the quantity, times the discount percentage
   divided by 100, rounded to two decimals.
2. The line's taxable base is the fee times the quantity, minus that discount amount.
3. The VAT percentage is the one carried by the chosen service — **unless Tax Exempt is
   Yes on the invoice, in which case it is forced to 0 for every line.**
4. The VAT amount is the base times the VAT percentage divided by 100, rounded to two
   decimals.
5. The line **Total** is the base plus the VAT amount.

**Total VAT** is the sum of the VAT amounts of the lines that have a service chosen.
**TOTAL** is the sum of their line totals. Both are read-only: you can change a total only
by changing quantity, fee or discount. **You can override the Fee on any line**, but not
the VAT percentage, the discount amount, the VAT amount or either grand total.

**After you save:** a missing or invalid entry gives **Please complete the required
fields.** with red text at the offending spot — **Date is required.**, **Invoice type is
required.**, **Child is required.**, **Service is required.**, **Quantity must be greater
than zero.**, **Enter a valid fee.** or **Discount must be between 0 and 100.** On success
you see **Invoice added** and the form closes and empties.

**Good to know:**

- Turning **Tax Exempt** on or off re-prices every line instantly and keeps what you have
  typed. It does not clear your lines.
- Lines with no service chosen are ignored when the invoice is saved and are left out of
  the totals, so an empty spare row does no harm.
- You can delete every row, leaving none. Saving then stops with **At least one service is
  required.**
- **VAT (%)** cannot be typed into. To bill a different VAT rate, change it on the service
  in the catalogue first.

> **Not yet checked on a live system:** the invoice number is produced after saving, and
> the numbering scheme has not been confirmed.

---

## How to edit or delete an invoice

**Who can do this:** roles holding the **Invoices** permission.
**Where:** sidebar **Invoices**, **Account** group · `/app/invoices`

**Steps to edit:**

1. Find the invoice in the left list.
2. Press the pencil control on the entry. The service lines are fetched and the panel
   opens headed **Edit Invoice**, pre-filled.
3. Change the header fields or the lines exactly as when creating.
4. Press **Update**.

**Steps to delete:**

1. Press the bin control on the entry.
2. **Delete Invoice** asks **Are you sure?**. Press **Yes**.

**After you save:** **Invoice updated** on a successful edit, **Invoice deleted** after a
delete. If the lines cannot be fetched when you press edit, you see **Invoice details
failed to load** and the form opens without them — do not save in that state, as you would
overwrite the invoice with empty lines.

**Good to know:** deleting an invoice removes it from the **Billed** column on Balance by
Class, which changes that child's balance. Receipts already recorded are untouched, because
they were never attached to the invoice.

---

## How to view, search and print a receipt

**Who can do this:** roles holding the **Receipts** permission.
**Where:** sidebar **Receipts**, **Account** group · `/app/receipts`

**What the screen shows:** the same split layout as Invoices — a list on the left, the
selected receipt as a printable document on the right. Each entry shows the date, the
child's name, an amber badge carrying the receipt type, and the amount. When the screen
opens it loads the first receipt in the list on its own.

**Steps:**

1. Open **Receipts**. The count reads as a number followed by **receipts**.
2. Type in **Search receipts...** to filter. It matches the child's name, the receipt
   number and the receipt type.
3. Press **Sort** to flip the date order. Newest first is the starting order.
4. Click an entry to open it on the right.
5. Press **Print**, or **Email** to send it to the parent. While sending, the button reads
   **Sending...**

**What the printed receipt contains:** the Peekaboo letterhead and logo; the receipt type
as a heading; **To** with the parent and child names and the parent's email; the receipt
description and any chosen service beneath it; **Date**; and **INV#** padded to eight
digits. Then a table with columns **Value Date**, **Mode of Payment**, **Payment Detail**
and **Amount / Cheque**, and a **Total** line prefixed **AED**. If the receipt has no
payment lines the table reads **No payment lines**.

> **Not yet checked on a live system:** the success and failure text after **Email** comes
> back from the server; where it does not, the screen falls back to **Receipt emailed
> successfully.** or **Failed to send email. Please try again.**

---

## How to record a receipt

**Who can do this:** roles holding the **Receipts** permission.
**Where:** sidebar **Receipts**, **Account** group · `/app/receipts`
**Before you start:** the payment modes you need must exist in **Payment Modes**.

**Steps:**

1. Open **Receipts**.
2. Press **Add Receipt**. The panel opens headed **Add Receipt**.
3. Fill in **Transaction Date**, **Child**, **Type** and **Description**.
4. Press **Add Line** under **Payment Lines** to create the first payment row. **The form
   opens with no payment rows at all, so you must do this at least once.**
5. On the row, set **Value Date**, **Mode of Payment**, **Payment Detail** and
   **Amount / Cheque**.
6. Repeat step 4 for each further payment.
7. Press **Save**.

**The form in full — receipt header:**

| Field | Required? | What to enter | Options |
| --- | --- | --- | --- |
| **Transaction Date** | Yes | The date of the receipt | Date picker. Opens on today |
| **Child** | Yes | Who the money came for | Dropdown of children; opens on **--Select--**, or **Loading children...** while it loads |
| **Type** | Yes | The receipt type | Dropdown; opens on **--Select--**, or **Loading types...** |
| **Reference** | No | Your own reference | Free text, at most 11 characters |
| **Services** | No | One service this receipt relates to | Dropdown; opens on **--Select--**. Only one may be chosen |
| **Description** | Yes | What the payment is for | Multi-line text |

**The form in full — each payment line:**

| Column | Required? | What to enter | Options |
| --- | --- | --- | --- |
| **Value Date** | Yes | When the money is good | Date picker; a new row opens on the receipt's date |
| **Mode of Payment** | Yes | How it was paid | Dropdown from **Payment Modes**; **Loading modes...** while it loads |
| **Payment Detail** | Yes | Cheque number, reference, note | Free text |
| **Amount / Cheque** | Yes | The amount | Number greater than zero |

**How the totals work:** the receipt total is simply the sum of the amounts on the payment
lines, to two decimal places. There is no VAT and no discount on a receipt. No total is
shown on the form while you type — the figure appears on the printed receipt as **Total**.
You cannot type the total yourself.

**After you save:** anything missing gives **Please complete the required fields.** with
red text where it is needed — **Transaction date is required.**, **Child is required.**,
**Receipt type is required.**, **Description is required.**, **Reference cannot exceed 11
characters.**, **At least one payment line is required.**, **Value date is required.**,
**Payment mode is required.**, **Payment detail is required.** or **Enter an amount greater
than zero.**

> **Not yet checked on a live system:** on success the screen shows a message from the
> server, falling back to **Receipt saved** where none is sent. The form then closes and
> empties.

**Good to know:**

- **The payment lines table starts completely empty.** Nothing is shown under
  **Payment Lines** until you press **Add Line**, and saving without one is refused.
- Payment lines with an amount of zero or blank are dropped when the receipt is saved, even
  though the form rejects them first — so a stray zero row does not reach the record.
- The **Services** dropdown records one service for reference only. It does not price the
  receipt and does not tie the receipt to an invoice.
- **There is nowhere to enter an invoice number.** A receipt attaches to a child, never to
  a bill.

---

## How to edit or delete a receipt

**Who can do this:** roles holding the **Receipts** permission.
**Where:** sidebar **Receipts**, **Account** group · `/app/receipts`

**Steps to edit:**

1. Press the pencil control on the entry in the left list.
2. The panel opens headed **Edit Receipt** and the payment lines load — a grey placeholder
   shows while they arrive.
3. Change what you need, then press **Update**.

**Steps to delete:**

1. Press the bin control on the entry.
2. **Delete Receipt** asks **Are you sure?**. Press **Yes**.

**Good to know:** if the payment lines cannot be fetched you see **Receipt details failed
to load** and the form gives you one blank row instead of the real lines. Cancel rather
than save, or you will replace the recorded payments with the single row on screen. If the
linked service cannot be fetched you see **Associated service failed to load**; the payment
lines are still fine.

> **Not yet checked on a live system:** the message after a successful update or delete is
> sent by the server; where none is sent the screen shows **Receipt deleted** after a
> delete.

---

## How to manage Payment Modes

**Who can do this:** roles holding the **Payment Modes** permission.
**Where:** sidebar **Payment Modes**, **Account** group · `/app/payment-modes`
**Before you start:** these are accounting codes. Get the chart and chapter numbers from
whoever keeps your books before inventing them.

**What the screen shows:** two panels side by side. On the left, the list of modes with
columns **Acc#**, **Desc** and **Chart ID**; empty, it reads **No payment modes**. On the
right, the form, headed **Add Payment Mode** or **Edit Payment Mode**. There is no search
box and no paging on this screen — every mode is listed at once. The count under the title
reads as a number followed by **payment modes configured**.

**Steps to create:**

1. Open **Payment Modes**.
2. Fill in the form on the right.
3. Press **Save**.

**Steps to edit:** press the edit control on a row; the form on the right fills in and its
heading changes to **Edit Payment Mode**. Change what you need and press **Update**, or
**Cancel** to drop the change. **Cancel** appears only while editing.

**Steps to delete:** press the delete control on the row, then **Yes** in
**Delete Payment Mode**.

**The form in full:**

| Field | Required? | What to enter | Options |
| --- | --- | --- | --- |
| **Account Number** | Yes | The account number for this mode | Free text |
| **Description** | Yes | The name staff will see in dropdowns | Free text |
| **Chapt ID** | Yes | Chapter number | Whole number, no decimals |
| **QB Account** | No | Matching external accounting account | Free text |
| **Chart ID** | Yes | Chart of accounts number | Whole number, no decimals |
| **Charges ID** | No | Charges account number | Whole number if given; recorded as 0 when left empty |
| **Trace Checks** | No | Whether cheques are traced | On/off switch reading **Yes** or **No**. Opens on **No** |

**How the totals work:** none. This screen holds no amounts.

**After you save:** errors give **Please complete the required fields.** with
**Account number is required.**, **Description is required.**, **Chapt ID must be an
integer.**, **Chart ID must be an integer.** or **Charges ID must be an integer.** On
success you see **Payment mode added** or **Payment mode updated**, and the list refreshes.
A refusal from the server shows its own message, or **Payment mode could not be added.** /
**Payment mode could not be updated.**

**Good to know:**

- What you type in **Description** is exactly what appears in the **Mode of Payment**
  dropdown on receipts and payment vouchers, so keep it plain: Cash, Bank Transfer, Cheque.
- Deleting a mode that older receipts used may leave those receipts showing a dash instead
  of a mode name on the printed copy.

---

## How to read Balance by Class

**Who can do this:** roles holding **Balance by Class**, **Invoices** or **Receipts**.
**Where:** sidebar **Balance by Class**, **Account** group · `/app/balance-by-class`
**Before you start:** nothing. This screen only reads; you cannot change anything on it.

**What the screen shows:** the heading **Balance By Class** with the note **Balance per
class**, then one row per child with columns **Student**, **Billed**, **Received** and
**Balance**. The **Student** column carries the student code, the class name, the child's
name and the parent's name — or **No parent assigned** where there is none, and
**Unassigned** where the child has no class. Empty, it reads **No student balances found
for this class.**

**Steps:**

1. Open **Balance by Class**.
2. Press a class chip along the top to narrow to one class. **All Classes** is selected
   when the screen opens. Only active classes appear as chips.
3. Type in **Search student...** to filter. It matches the child's name, the parent's name,
   the student code and the class name.
4. Set **As of** to a date to include only invoices and receipts dated on or before that
   day. Left empty, everything is included.

**How the totals work,** for each child:

1. **Billed** is the sum of the amounts of all that child's invoices.
2. **Received** is the sum of the amounts of all that child's receipts.
3. **Balance** is **Billed minus Received**.

When **As of** holds a date, an invoice or receipt counts only if its own date falls on or
before it. Each figure is a straight total of whole documents; nothing is apportioned.

**How to read the colours and the signs — read this carefully, it is easy to misread:**

- Every figure is printed as **AED** followed by its **absolute value**. Minus signs are
  never printed. A balance of minus 500 appears as **= AED 500**, exactly like a balance of
  plus 500.
- The prefixes are fixed labels, not arithmetic. **Billed** always carries **+**,
  **Received** always carries **-**, and **Balance** always carries **=**, whatever the
  numbers are.
- **Billed** is always green. **Received** is always red. Neither colour means anything is
  wrong; they mark the direction of the column, not the health of the account.
- **Balance** is the only colour that carries information, and it works the opposite way
  round from what most people expect: the balance is shown **red only when it is below
  zero**, and grey when it is zero or above. A child who owes you money (billed more than
  received) shows a **grey** balance. A child who has **overpaid** shows a **red** one.

So: to find debtors, read the **Balance** figures rather than hunting for red, and treat a
red balance as a credit sitting on the account.

**Practical reconciliation.** Because invoices carry no paid/unpaid status and receipts are
not attached to invoices, this screen is where you find out where a family stands. Filter to
a class, set **As of** to the end of the period, and compare **Billed** against
**Received** child by child. A non-zero **Balance** is the amount outstanding — or, where
it shows red, the amount held in credit.

**Good to know:**

- The class chips list active classes only, so a child in a closed class can be reached
  through **All Classes** and the search box, but not through a chip.
- There is no export button on this screen.
- Where a child has no student code recorded, the screen makes one up for display from the
  child's record. It is a display convenience, not an official reference.

---

# MONEY GOING OUT

## How to manage Suppliers

**Who can do this:** roles holding the **Suppliers** permission.
**Where:** sidebar **Suppliers**, **Finance** group · `/app/suppliers`

**What the screen shows:** two panels. On the left, the supplier list with columns
**Supplier Name**, **Phone**, **Email** and **VAT**, a **Search suppliers...** box, and
**Supplier Name** sortable. Empty, it reads **No suppliers**. On the right, the form headed
**Add Supplier** or **Edit Supplier**. Every supplier is listed at once; there is no paging.
The count reads as a number followed by **suppliers configured**.

**Steps to create:**

1. Open **Suppliers**.
2. Complete the form on the right.
3. Press **Save**.

**Steps to edit:** press the edit control on a row, change the fields, press **Update**.
**Cancel** appears only while editing.

**Steps to delete:** press the delete control, then **Yes** in **Delete Supplier**.

**The form in full:**

| Field | Required? | What to enter | Options |
| --- | --- | --- | --- |
| **Supplier Name** | Yes | The supplier's name | Free text |
| **Supplier Phone** | No | Contact number | Telephone box |
| **Supplier Email** | No | Contact email | Must be a valid address if filled |
| **Supplier Address** | No | Postal address | Free text |
| **Supplier Terms** | No | Payment terms, e.g. 30 days | Free text |
| **Supplier VAT** | Yes | VAT percentage | Number from 0 to 100. Opens at 0.00 |
| **Supplier Description** | No | Any notes | Multi-line text |

Although **Supplier VAT** carries no asterisk, clearing it blocks the save with **Supplier
VAT must be between 0 and 100.** Leave the 0.00 if VAT does not apply.

**How the totals work:** none. **Supplier VAT** is stored against the supplier for
reference; purchase lines take their VAT from the **Services** catalogue, not from here.

**After you save:** errors give **Please complete the required fields.** with **Supplier
name is required.**, **Enter a valid email address.** or **Supplier VAT must be between 0
and 100.**

> **Not yet checked on a live system:** the message after a successful save or delete comes
> from the server, so its exact wording is unconfirmed. A failure to delete shows **Failed
> to delete supplier**.

**Good to know:** suppliers feed the **Supplier** dropdown on **Purchases**, **Expenses**
and **Payment Voucher**. Create the supplier before trying to record any of those.

---

## How to manage Expense Types

**Who can do this:** roles holding the **Expense Types** permission.
**Where:** sidebar **Expense Types**, **Finance** group · `/app/expense-types`

**What the screen shows:** a list on the left with columns **Type Name** and
**Description**, both sortable, with a **Search expense types...** box; empty it reads
**No expense types**. The form sits on the right, headed **Add Expense Type** or
**Edit Expense Type**. Everything is listed at once. The count reads as a number followed
by **expense types configured**.

**Steps to create:**

1. Open **Expense Types**.
2. Enter **Type Name**, and **Description** if you want one.
3. Press **Save**.

**Steps to edit:** press the edit control on a row, change the fields, press **Update**.
**Cancel** shows only while editing.

**Steps to delete:** press the delete control, then **Yes** in **Delete Expense Type**.

**The form in full:**

| Field | Required? | What to enter | Options |
| --- | --- | --- | --- |
| **Type Name** | Yes | The category name, e.g. Cleaning | Free text |
| **Description** | No | A note about what belongs here | Free text |

**How the totals work:** none.

**After you save:** a missing name gives **Please complete the required fields.** with
**Expense type name is required.** under the box. A failed delete shows **Failed to delete
expense type**.

**Good to know:** these entries fill the **Expense Supply** dropdown on the Expenses form —
not the **Type** dropdown, which comes from a separate list of journal types. Set your
categories up here before recording expenses.

---

## How to view and search Expenses

**Who can do this:** roles holding the **Expenses** permission.
**Where:** sidebar **Expenses**, **Finance** group · `/app/expenses`

**What the screen shows:** one table with columns **Date**, **Supply**, **Supplier**,
**Amount** and **Attachment**. **Date**, **Supply**, **Supplier** and **Amount** are
sortable. The **Attachment** column shows a coloured type badge — **Image**, **PDF**,
**Document**, **Sheet**, **Presentation**, **Archive** or **File** — with **View** and
**Download** buttons, or the words **No file**. Empty, it reads **No expenses found**. The
table shows 10 rows a page. The count reads as a number followed by **expenses**.

**Steps:**

1. Open **Expenses**.
2. Use the search box to filter. It matches the supplier name, the expense supply category
   and the description.
3. Press a column heading to sort.
4. Press **View** to open an attachment in a new tab, or **Download** to save it.

**Exporting:** four buttons sit above the table — **Copy**, **PDF**, **Print** and **CSV**.
**Copy** puts the table on your clipboard and reports **Expenses copied**; **CSV**
downloads a file; **PDF** and **Print** both open your browser's print dialogue. A failure
shows **Unable to export expenses**.

**Good to know — the export ignores your search and your page.** All four buttons export
**every expense record**, not the rows you have filtered to and not just the page you are
looking at. The exported columns are **Date**, **Supply**, **Supplier**, **Amount**, **VAT**
and **Description** — note that **VAT** and **Description** appear in the export but not on
screen. Check the row count after exporting if you expected a filtered extract.

---

## How to record an expense

**Who can do this:** roles holding the **Expenses** permission.
**Where:** sidebar **Expenses**, **Finance** group · `/app/expenses`
**Before you start:** have the receipt or invoice file to hand — **an attachment is
compulsory on a new expense** — and make sure the supplier and the expense type exist.

**Steps:**

1. Open **Expenses**.
2. Press **Add Expense**. The panel opens headed **Add Expense**.
3. Complete the fields.
4. Attach the document: drag it onto the dashed area, or click the area, or press
   **Browse ...**.
5. Press **Save**.

**The form in full:**

| Field | Required? | What to enter | Options |
| --- | --- | --- | --- |
| **Expense Supply** | Yes | The spend category | Dropdown from **Expense Types**; opens on **--Select--** |
| **Type** | Yes | The journal type | Dropdown of types configured for your nursery; opens on **--Select--** |
| **Date** | Yes | The date of the spend | Date picker. Opens on today |
| **Supplier** | Yes | Who was paid | Dropdown from **Suppliers**; opens on **--Select--** |
| **Amount** | Yes | The amount, excluding VAT as you record it | Number greater than zero. Opens at 0.00 |
| **VAT** | No | The VAT amount **in money, not a percentage** | Number, zero or more. Opens at 0.00 |
| **Description** | No | What it was for | Free text |
| **Attachment** | Yes when creating | The receipt or invoice | One file, 2 MB maximum. Images, PDF, Word, Excel, CSV, text, PowerPoint, ZIP and RAR |

**How the totals work:** there is no arithmetic on this screen. **Amount** and **VAT** are
both typed in and stored exactly as you enter them. Peekaboo does **not** calculate VAT from
a percentage here, does not add the two together, and shows no combined total. The
**Amount** column in the list is the **Amount** figure alone; the VAT sits in its own field
and appears only in the export.

**After you save:** errors give **Please complete the required fields.** with **Expense
supply is required.**, **Expense type is required.**, **Supplier is required.**, **Expense
date is required.**, **Amount must be greater than zero.**, **VAT cannot be negative.** or
**Attachment is required**. A file over the limit is refused at once with **Attachment must
not exceed 2 MB.**

> **Not yet checked on a live system:** the confirmation after a successful save is sent by
> the server, so its wording is unconfirmed. The form then closes and empties.

**Good to know:**

- **Attachment** is compulsory when creating but not when editing, so an expense saved
  earlier can be updated without re-attaching its file.
- Only one file fits. Attaching a second replaces the first.
- **VAT** is a money amount. Typing 5 here records five in currency, not five per cent.
- The dashed drop area previews images and PDFs directly; other file types show a badge and
  the file name.

---

## How to edit or delete an expense

**Who can do this:** roles holding the **Expenses** permission.
**Where:** sidebar **Expenses**, **Finance** group · `/app/expenses`

**Steps to edit:**

1. Press the edit control on the row. The page scrolls up and the panel opens headed
   **Edit Expense**, pre-filled, with the existing attachment shown.
2. Change what you need. To swap the file, remove the current one with the small cross and
   attach another; to keep it, leave it alone.
3. Press **Update**.

**Steps to delete:** press the delete control, then **Yes** in **Delete Expense**.

> **Not yet checked on a live system:** the messages after a successful update or delete
> come from the server. Where the server reports a problem on delete, the screen falls back
> to **Delete failed**.

---

## How to view and search Purchases

**Who can do this:** roles holding the **Purchases** permission.
**Where:** sidebar **Purchases**, **Finance** group · `/app/purchases`

**What the screen shows:** a table with columns **Date**, **Type**, **Purchase#**,
**Supplier** and **Amount**, all sortable, with **Actions** at the end. Empty, it reads
**No purchases found**. Ten rows a page. The count reads as a number followed by
**purchases recorded**.

**Steps:**

1. Open **Purchases**.
2. Use **Search purchases...** to filter. It matches the purchase type, the supplier name
   and the purchase number.
3. Press a column heading to sort, and the controls beneath to change page.

**Exporting:** the same four buttons, **Copy**, **PDF**, **Print** and **CSV**, sit above
the table. **Copy** reports **Purchases copied**; a failure shows **Unable to export
purchases**. The exported columns are **Date**, **Type**, **Purchase #**, **Supplier** and
**Amount**.

**Good to know — the export ignores your search and your page here too.** All four buttons
export **every purchase record**, regardless of what you have filtered to or which page is
on screen.

---

## How to record a purchase

**Who can do this:** roles holding the **Purchases** permission.
**Where:** sidebar **Purchases**, **Finance** group · `/app/purchases`
**Before you start:** the supplier must exist in **Suppliers**, and the items must exist in
**Services**.

**Steps:**

1. Open **Purchases**.
2. Press **+ Add Purchase**. The panel opens headed **Add New Purchase** with one blank
   line ready under the sub-heading **Purchases**.
3. **Set Tax Exempt first, before you enter any lines** — see the warning below.
4. Set **Date**, **Type** and **Supplier**.
5. On the line, choose the **Service**. **Fee** and **VAT (%)** fill in automatically.
6. Set **QTY**, and adjust **Fee** if it differs.
7. Press **Add Purchase** beside the table to add another line; press the bin at the start
   of a line to remove it.
8. Check **Total VAT** and **Total** at the foot.
9. Press **Save**.

**The form in full — purchase header:**

| Field | Required? | What to enter | Options |
| --- | --- | --- | --- |
| **Date** | Yes | The purchase date | Date picker. Opens on today |
| **Type** | Yes | The purchase type | Dropdown; opens on **--Select--** |
| **Supplier** | Yes | Who you bought from | Dropdown from **Suppliers**; opens on **--Select--** |
| **Tax Exempt** | No | Removes VAT from every line | On/off switch reading **Yes** or **No**. Opens on **No** |

**The form in full — each purchase line:**

| Column | Required? | What to enter | Options |
| --- | --- | --- | --- |
| **Service** | Yes | The item bought | Dropdown from the Services catalogue |
| **QTY** | Yes | How many | Whole number, at least 1. Opens at 1 |
| **Fee** | Yes | Price for one | Number greater than zero. Fills from the service, and you may overwrite it |
| **VAT (%)** | — | Filled from the service | Read-only, greyed out |
| **VAT Amount** | — | Calculated | Read-only |
| **Total** | — | Calculated | Read-only |

**How the totals work,** for each line:

1. The base is the fee times the quantity. **There is no discount on a purchase line** —
   unlike an invoice, no discount column exists.
2. The VAT percentage is the one carried by the chosen service, or 0 for every line when
   **Tax Exempt** is **Yes**.
3. The VAT amount is the base times the VAT percentage divided by 100, to two decimals.
4. The line **Total** is the base plus the VAT amount.

**Total VAT** is the sum of the line VAT amounts and **Total** the sum of the line totals.
Both are read-only. A new line opens with a VAT percentage of 5 before you pick a service;
choosing a service replaces it with that service's rate.

**After you save:** errors give **Please complete the required fields.** with **Date is
required.**, **Type is required.**, **Supplier is required.**, **Service is required.**,
**Quantity must be greater than zero.** or **Fee must be greater than zero.**

> **Not yet checked on a live system:** the confirmation on success and the purchase
> numbering are produced by the server and are unconfirmed.

**Good to know — the most important trap on this screen:**

- **Switching Tax Exempt wipes every line you have entered.** Unlike the invoice screen,
  which simply re-prices, the purchase screen blanks all lines back to empty when the
  switch is touched — the services, quantities and fees you typed are lost. Always set
  **Tax Exempt** before entering lines. If you realise mid-entry that it is wrong, expect
  to retype the lines.
- Turning **Tax Exempt** on also changes which services the **Service** dropdown offers:
  the list is drawn from a different set of catalogue entries while the switch is on.
- Unlike the invoice form, a line with no service chosen is **not** skipped: it is refused
  with **Service is required.** Remove spare rows before saving.

---

## How to edit or delete a purchase

**Who can do this:** roles holding the **Purchases** permission.
**Where:** sidebar **Purchases**, **Finance** group · `/app/purchases`

**Steps to edit:**

1. Press the edit control in the **Actions** column. The panel opens headed **Edit
   Purchase** and the lines load — a grey placeholder shows in the table meanwhile.
2. Change what you need, then press **Update**.

**Steps to delete:** press the delete control, then **Yes** in **Delete Purchase**.

**Good to know:** while editing, touching **Tax Exempt** clears the loaded lines in exactly
the same way as when creating. If the lines cannot be fetched you see **Purchase details
failed to load** and the form is left holding a single blank row — cancel rather than save.

---

## How to view and search Payment Vouchers

**Who can do this:** roles holding the **Payment Voucher** permission.
**Where:** sidebar **Payment Voucher**, **Finance** group · `/app/payment-voucher`

**What the screen shows:** a table with columns **Date**, **Type**, **Number**,
**Supplier** and **Amount**, all sortable. Empty, it reads **No vouchers found**. Ten rows
a page. The count reads as a number followed by **vouchers recorded**.

**Steps:**

1. Open **Payment Voucher**.
2. Use **Search vouchers...** to filter. It matches the voucher number, the voucher type,
   the supplier name and the voucher reference.
3. Press the view control on a row to open **Payment Voucher Details** over the page. It
   shows **Date**, **Number**, **Supplier** and **Amount**, then the payment lines under
   **Value Date**, **Mode**, **Detail** and **Amount**. Press **Close** to return.

**Exporting:** **Copy**, **PDF**, **Print** and **CSV** as on the other Finance screens.
**Copy** reports **Payment vouchers copied**; a failure shows **Unable to export payment
vouchers**. The same caution applies — **the export covers every voucher, not your filtered
view**.

> **Not yet checked on a live system:** if the lines cannot be fetched the screen shows
> **Payment voucher details failed to load**.

---

## How to record a payment voucher

**Who can do this:** roles holding the **Payment Voucher** permission.
**Where:** sidebar **Payment Voucher**, **Finance** group · `/app/payment-voucher`
**Before you start:** the supplier must exist in **Suppliers**, and the payment modes in
**Payment Modes**.

**Steps:**

1. Open **Payment Voucher**.
2. Press **+ Add Payment Voucher**. The panel opens headed **Add Payment Voucher** with one
   blank payment line ready.
3. Set **Date**, **Supplier** and **Type**, and fill **Reference** and **Description** if
   you use them.
4. On the payment line, set **Value Date**, **Mode of Payment**, **Payment Detail** and the
   amount.
5. Add further lines as needed, and remove any you do not want.
6. Press **Save**.

**The form in full — voucher header:**

| Field | Required? | What to enter | Options |
| --- | --- | --- | --- |
| **Date** | Yes | The voucher date | Date picker. Opens on today |
| **Supplier** | Yes | Who is being paid | Dropdown from **Suppliers**; opens on **--Select--** |
| **Type** | Yes | The voucher type | Dropdown; opens on **--Select--** |
| **Reference** | No | Your own reference | Free text |
| **Description** | No | What the payment covers | Free text |

**The form in full — each payment line:**

| Column | Required? | What to enter | Options |
| --- | --- | --- | --- |
| **Value Date** | Yes | When the money leaves | Date picker; a new line opens on today |
| **Mode of Payment** | Yes | How it was paid | Dropdown from **Payment Modes** |
| **Payment Detail** | Yes | Cheque number, reference, note | Free text |
| **Amount** | Yes | The amount | Number greater than zero |

**How the totals work:** the voucher total is the sum of the amounts on the payment lines,
to two decimal places. There is no VAT and no discount on a voucher. You cannot type the
total; it is recorded from the lines and shown as **Amount** in the list and in
**Payment Voucher Details**.

**After you save:** errors give **Please complete the required fields.** with **Transaction
date is required**, **Supplier is required**, **Voucher type is required**, **At least one
payment line is required.**, **Value date is required.**, **Payment mode is required.**,
**Payment detail is required.** or **Amount must be greater than zero.**

> **Not yet checked on a live system:** the confirmation on success and the voucher
> numbering come from the server and are unconfirmed.

**Good to know:**

- Unlike the receipt form, this one opens with a payment line already in place, so you can
  type straight into it.
- A payment voucher is a record of money paid to a supplier. **It does not settle a
  purchase or an expense**, and no screen marks either as paid. If you need the link, note
  the purchase or invoice number in **Reference** or **Description** by hand.

---

## How to edit or delete a payment voucher

**Who can do this:** roles holding the **Payment Voucher** permission.
**Where:** sidebar **Payment Voucher**, **Finance** group · `/app/payment-voucher`

**Steps to edit:**

1. Press the edit control on the row. The panel opens headed **Edit Payment Voucher** and
   the payment lines load.
2. Change what you need, then press **Update**.

**Steps to delete:** press the delete control, then **Yes** in the confirmation box.

**Good to know:** while the lines are loading the payment table is briefly empty. Wait for
the rows to appear before editing, so you do not save a voucher with its lines missing.
