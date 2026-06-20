**Working with Lists and Forms in ServiceNow**
==============================================

Lecture Summary
---------------

This lecture explains the two most commonly used interfaces in ServiceNow: **List Views** and **Form Views**. Lists are used to display and manage multiple records simultaneously, while forms are designed for viewing and editing a single record. The lecture demonstrates navigation between lists and forms, mass updates, inline editing, record actions, UI Actions, related lists, and read-only fields.

* * * * *

Key Points
==========

-   **List View** displays multiple records at once.
-   **Form View** displays a single record.
-   Lists support filtering, sorting, searching, and bulk updates.
-   Forms provide a detailed view of a record and expose additional functionality.
-   Users can edit fields directly from a list using **inline editing**.
-   Checkboxes in lists enable **mass updates** and bulk actions.
-   Forms contain **tabs**, **related lists**, **attachments**, and **UI Actions**.
-   Some fields can be configured as **read-only**.
-   Administrators control form behavior and field accessibility.

* * * * *

Detailed Notes
==============

1\. Introduction to Lists and Forms
-----------------------------------

As a ServiceNow Administrator or Developer, most daily activities occur within:

1.  **List Views**
2.  **Form Views**

These are simply two different ways of viewing records stored in ServiceNow tables.

### Relationship

`Table\
  ↓\
Records\
  ↓\
List View (Multiple Records)\
Form View (Single Record)`

* * * * *

2\. Understanding List View
===========================

What is a List View?
--------------------

A **List View** displays multiple records from a table.

Example:

`Open Incidents\
--------------------------------------------------\
INC0010001\
INC0010002\
INC0010003\
INC0010004`

Each row represents a separate record.

### Characteristics

-   Shows multiple records simultaneously.
-   Displays selected fields as columns.
-   Supports sorting and filtering.
-   Allows mass updates.
-   Supports inline editing.

* * * * *

Components of a List View
-------------------------

### Breadcrumb Filter

Located at the top of the list.

Example:

```
Active = True
```

This indicates the current filter being applied.

### Columns

Examples:

-   Number
-   Opened
-   Short Description
-   Caller
-   Category
-   State

Each column represents a field from the underlying table.

* * * * *

Column Context Menu
-------------------

Each column contains a hamburger menu.

Used for:

-   Sorting
-   Filtering
-   Configuring columns
-   Additional actions

* * * * *

Main List Menu
--------------

Located in the upper-left corner of the list.

Provides options such as:

-   Exporting records
-   Configuring list layout
-   Selecting row count
-   Additional list operations

* * * * *

3\. Number of Records per Page
==============================

ServiceNow allows administrators and users to define how many records appear per page.

Examples:

`10 Records\
20 Records\
50 Records\
100 Records`

### Recommended Setting

The instructor recommends:

```
50 Records Per Page
```

### Why Not Always Use 100?

Displaying more records requires:

-   More database queries
-   More processing
-   Longer load times

### Performance Impact

| Rows | Performance |
| --- | --- |
| 10 | Fast |
| 50 | Balanced |
| 100 | Slower |

* * * * *

4\. Inline Editing in List Views
================================

What is Inline Editing?
-----------------------

Users can modify field values directly from the list without opening the record.

### Example

Double-click a field:

```
Opened DateCategorySubcategory
```

Modify the value immediately.

### Benefits

-   Faster updates
-   Reduced navigation
-   Increased productivity

### Requirement

Users must have appropriate permissions or roles.

* * * * *

5\. Mass Updates Using Checkboxes
=================================

Each row contains a checkbox.

### Purpose

Select multiple records simultaneously.

### Example

```
☑ Incident 59☑ Incident 60
```

### Available Actions

-   Archive
-   Delete
-   Update
-   Other bulk operations

### Benefits

Useful when working with many records.

* * * * *

6\. Record Preview (Information Icon)
=====================================

Before opening a record fully, users can click the **Information Icon**.

### Purpose

Quickly view:

-   Additional fields
-   Record details
-   Key information

### Benefit

Allows quick inspection without leaving the list.

* * * * *

7\. Understanding Form View
===========================

What is a Form View?
--------------------

A **Form View** displays one record at a time.

Example:

```
Incident: INC0000059
```

### Purpose

Used for:

-   Creating records
-   Editing records
-   Viewing detailed information

* * * * *

8\. Advantages of Form View
===========================

Since only one record is displayed:

-   More screen space is available.
-   More fields can be shown.
-   Advanced functionality becomes available.

### Example

Incident Form:

`Number\
Caller\
Assignment Group\
Category\
Impact\
Urgency\
Priority`

* * * * *

9\. Form Sections and Tabs
==========================

Large forms are divided into sections.

### Example Tabs

#### Notes

Stores work notes and comments.

#### Related Records

Displays linked records.

#### Resolution Information

Contains closure details.

### Benefits

-   Better organization
-   Easier navigation
-   Cleaner user experience

* * * * *

10\. Related Lists
==================

Related Lists appear at the bottom of a form.

### Purpose

Display records related to the current record.

Examples:

-   Incident Tasks
-   Attachments
-   Approvals
-   Child Records

### Benefit

Provides a complete picture of the record relationship.

* * * * *

11\. Form Actions and Features
==============================

Forms provide several capabilities unavailable in lists.

* * * * *

Attachments
-----------

Users can attach files directly to a record.

Examples:

-   Screenshots
-   PDFs
-   Logs
-   Documents

* * * * *

Email Functionality
-------------------

Users can send emails directly from the form.

### Use Cases

-   Notify stakeholders
-   Send updates
-   Request information

* * * * *

Follow Record
-------------

Users can follow a record and receive updates.

* * * * *

Record Updates
--------------

Administrators and authorized users can update field values directly.

* * * * *

12\. UI Actions
===============

What are UI Actions?
--------------------

UI Actions are buttons displayed on forms.

Examples:

`Save\
Update\
Resolve\
Close`

### Purpose

Execute specific actions.

### Example

Incident State = New

Button Available:

```
Resolve
```

Clicking Resolve executes incident resolution logic.

* * * * *

13\. Record Navigation Arrows
=============================

When opening a form from a list:

Users see navigation arrows.

### Functions

```
↑ Previous Record↓ Next Record
```

### Benefit

Navigate records without returning to the list.

* * * * *

14\. Editable vs Read-Only Fields
=================================

Some fields are editable.

Examples:

-   Assignment Group
-   Category
-   Configuration Item

Some fields are read-only.

### Example

Priority

In the demonstration:

```
Priority = Read Only
```

### Why?

Priority is calculated automatically from:

```
Impact + Urgency
```

Therefore users cannot manually modify it.

* * * * *

15\. Administrator Control
==========================

Administrators can control:

### Form Behavior

-   Visible fields
-   Hidden fields
-   Field order

### Field Security

-   Read-only fields
-   Mandatory fields
-   Editable fields

### User Experience

-   Form layouts
-   UI Actions
-   Related Lists

* * * * *

Steps / Process
===============

Opening a Record from a List
----------------------------

### Step 1

Navigate to a list.

Example:

```
Open Incidents
```

### Step 2

Locate the desired record.

### Step 3

Click the Information Icon (optional).

### Step 4

Select:

```
Open Record
```

### Step 5

The Form View opens.

* * * * *

Performing a Mass Update
------------------------

### Step 1

Open a list.

### Step 2

Select multiple checkboxes.

### Step 3

Choose a bulk action.

Example:

```
DeleteArchiveUpdate
```

### Step 4

Execute the action.

* * * * *

Editing a Record from List View
-------------------------------

### Step 1

Locate the record.

### Step 2

Double-click a field.

### Step 3

Modify the value.

### Step 4

Save changes.

* * * * *

Important Terms
===============

| Term | Meaning |
| --- | --- |
| **List View** | Displays multiple records simultaneously |
| **Form View** | Displays a single record |
| **Inline Editing** | Editing fields directly within a list |
| **Breadcrumb** | Filter condition displayed above a list |
| **Related List** | Records associated with the current record |
| **UI Action** | Button performing a predefined action |
| **Read-Only Field** | Field that users cannot edit |
| **Mass Update** | Updating multiple records simultaneously |
| **Record Preview** | Quick view of record information |
| **Attachment** | File associated with a record |

* * * * *

Commands / Syntax / Configuration
=================================

List vs Form
------------

`List View\
   ↓\
Multiple Records

Form View\
   ↓\
Single Record`

* * * * *

Incident Navigation
-------------------

`List\
 ↓\
Open Record\
 ↓\
Form`

* * * * *

Priority Calculation
--------------------

```
Impact + Urgency        ↓     Priority
```

* * * * *

Examples
========

Example 1: Mass Update
----------------------

Select:

```
☑ INC0000059☑ INC0000060
```

Action:

```
Archive
```

Both records are updated simultaneously.

* * * * *

Example 2: Inline Editing
-------------------------

Double-click:

```
Category
```

Change value:

```
Network → Hardware
```

No need to open the form.

* * * * *

Example 3: Form View
--------------------

Incident:

```
INC0000059
```

Contains:

-   Caller
-   Category
-   Impact
-   Assignment Group
-   Resolution Information

All accessible from a single form.

* * * * *

Certification Focus
===================

Important Points for Exams
--------------------------

-   Lists display **multiple records**.
-   Forms display **one record**.
-   Lists support filtering and sorting.
-   Lists allow **inline editing**.
-   Checkboxes enable **mass updates**.
-   Forms provide access to **UI Actions**.
-   Forms contain **related lists**.
-   Fields can be configured as **read-only**.
-   Priority is often calculated from **Impact** and **Urgency**.

* * * * *

Common Mistakes
---------------

❌ Confusing List View with Form View.

❌ Opening records unnecessarily when inline editing is available.

❌ Assuming all fields are editable.

❌ Forgetting that UI Actions are typically form-specific.

❌ Displaying excessive rows and impacting performance.

* * * * *

Things to Remember
------------------

✅ Lists = Multiple records.

✅ Forms = Single record.

✅ Double-click enables inline editing.

✅ Checkboxes support bulk operations.

✅ UI Actions perform record-specific functions.

✅ Related Lists display connected records.

✅ Priority may be automatically calculated.

✅ Administrators control form behavior.

* * * * *

Real-World Application
======================

In a Service Desk environment:

### List View

Used to:

-   Monitor open incidents
-   Filter high-priority tickets
-   Assign incidents in bulk
-   Update multiple records

### Form View

Used to:

-   Investigate incidents
-   Add work notes
-   Attach screenshots
-   Resolve tickets
-   Send notifications

Administrators frequently customize forms and lists to improve efficiency and user experience.

* * * * *

Quick Revision (30 sec)
=======================

-   **List View** = Multiple records.
-   **Form View** = Single record.
-   Lists support sorting and filtering.
-   Double-click fields for inline editing.
-   Checkboxes enable mass updates.
-   Information Icon previews records.
-   Forms display additional fields and tabs.
-   Related Lists show connected records.
-   UI Actions are form buttons like Resolve.
-   Read-only fields cannot be edited directly.