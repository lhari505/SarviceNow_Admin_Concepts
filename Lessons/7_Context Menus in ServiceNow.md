**Context Menus in ServiceNow**
===============================

Lecture Summary
---------------

This lecture introduces **Context Menus** in ServiceNow, which provide quick access to actions and configurations based on where the user is working. Context menus are available in both **List Views** and **Form Views** and can be accessed through the **hamburger menu icon** or by right-clicking on records, columns, and fields. The lecture covers List Context Menus, Column Context Menus, Cell Context Menus, Form Context Menus, and Field Context Menus, along with their practical uses.

* * * * *

Key Points
==========

-   **Context Menus** provide quick access to actions and configurations.
-   Available in both **List Views** and **Form Views**.
-   Accessed through the **hamburger menu icon** or right-click actions.
-   Administrators can customize menu items.
-   Different context menus serve different purposes.
-   List Context Menus manage list-level operations.
-   Column Context Menus manage column-specific operations.
-   Cell Context Menus manage record-specific actions.
-   Form Context Menus manage record and form actions.
-   Field Context Menus provide field-level configuration options.

* * * * *

Detailed Notes
==============

1\. What are Context Menus?
===========================

Definition
----------

A **Context Menu** is a menu containing actions relevant to the current object, record, field, or list being viewed.

### Purpose

Context menus help users:

-   Access actions quickly
-   Configure records
-   Manage lists
-   Customize forms
-   Perform administrative tasks

* * * * *

Accessing Context Menus
-----------------------

Context menus are typically accessed using:

```
☰ Hamburger Menu
```

or

```
Right Click
```

on a field, record, or cell.

* * * * *

2\. Types of Context Menus in ServiceNow
========================================

ServiceNow provides several types of context menus:

### List View Context Menus

-   Main List Context Menu
-   Column Context Menu
-   Cell Context Menu

### Form View Context Menus

-   Main Form Context Menu
-   Field Context Menu
-   Related List Context Menu

* * * * *

3\. Main List Context Menu
==========================

Location
--------

Located in the:

```
Top Left of Main Content Frame
```

within a list view.

* * * * *

Purpose
-------

Provides actions related to the entire list.

* * * * *

Key Options
-----------

### Personalize List Columns

Allows users to:

-   Add columns
-   Remove columns
-   Customize visible fields

* * * * *

### Change View

Switch between different predefined views.

Example:

```
Default ViewMobile ViewPortal View
```

* * * * *

### Mobile View Example

Default View:

```
Many Columns Displayed
```

Mobile View:

```
NumberStateShort DescriptionEscalation
```

Only essential columns are displayed.

* * * * *

### List Layout

Controls:

-   Column order
-   Visible columns
-   List structure

* * * * *

### List Calculations

Used for:

-   Summaries
-   Totals
-   Aggregations

* * * * *

### List Control

Used to configure list behavior.

* * * * *

### Configure Menu

Provides access to table configuration options.

Example:

```
Configure TableConfigure FormsConfigure Lists
```

* * * * *

### Import / Export

Allows importing and exporting records.

Supported formats may include:

-   CSV
-   Excel
-   XML

* * * * *

### Favorites

Save frequently used lists.

* * * * *

### Update Selected

Perform updates on selected records.

* * * * *

### Create Application Files

Used during application development.

* * * * *

### Import XML

Import records through XML files.

* * * * *

4\. Column Context Menu
=======================

Location
--------

Found beside each column header.

Example:

```
NumberPriorityStateCategory
```

* * * * *

Purpose
-------

Provides actions specific to a column.

* * * * *

Available Actions
-----------------

### Sort Ascending

```
A → Z
```

* * * * *

### Sort Descending

```
Z → A
```

* * * * *

### Group By

Groups records based on field values.

Example:

```
Group By State
```

Results:

```
NewIn ProgressResolvedClosed
```

* * * * *

### Charts

Generate visual reports.

Examples:

-   Bar Chart
-   Pie Chart

* * * * *

### Visual Task Board

Displays records in a board format.

Similar to:

```
Kanban Board
```

* * * * *

5\. Cell Context Menu
=====================

Location
--------

Appears when right-clicking a cell in a list.

* * * * *

Purpose
-------

Provides actions related to a specific record.

* * * * *

Common Options
--------------

### Show Matching

Creates a filter using the selected value.

Example:

```
Caller = Abel Tuter
```

Returns all records with that caller.

* * * * *

### Filter Out

Excludes matching records.

Example:

```
Priority = High
```

Removes High Priority records from results.

* * * * *

### Copy URL

Copies the record URL.

* * * * *

### Copy sys_id

Copies the unique record identifier.

* * * * *

### Edit Tags

Manage record tags.

* * * * *

### Assign To Me

Assigns the task to the current user.

Available on Task-based records.

* * * * *

### Live Feed Options

-   Follow on Live Feed
-   Show Live Feed

* * * * *

### Add to Visual Task Board

Adds the record to a Visual Task Board.

* * * * *

6\. Main Form Context Menu
==========================

Location
--------

Top-left corner of the form view.

Same location as the List Context Menu.

* * * * *

Purpose
-------

Provides actions for the currently opened record.

* * * * *

Record-Specific Actions
-----------------------

Examples:

### Save

```
Save Record
```

* * * * *

### Close

```
Close Problem
```

* * * * *

### Resolve Incidents

Resolve incidents related to the problem.

* * * * *

### Create Normal Change

Create a change request associated with the problem.

* * * * *

Form Configuration Actions
==========================

These are similar to list configuration options.

Examples:

-   Configure Table
-   Configure Form
-   Configure Lists

* * * * *

Export Options
==============

Export the current record.

* * * * *

Change View
===========

Switch between form views.

* * * * *

Favorites
=========

Add form to favorites.

* * * * *

Copy URL
========

Copy record URL.

* * * * *

Copy sys_id
===========

Copy record unique identifier.

* * * * *

XML View
========

Display the record in XML format.

Useful for:

-   Troubleshooting
-   Integrations
-   Development

* * * * *

History
=======

View record history.

* * * * *

Reload Form
===========

Refresh the form.

* * * * *

7\. Field Context Menu
======================

Location
--------

Right-click on almost any field within a form.

* * * * *

Purpose
-------

Provides field-specific administrative actions.

* * * * *

Available Options
-----------------

### Configure Label

Modify field label.

Example:

```
Caller↓Requested By
```

* * * * *

### Configure Dictionary

Open dictionary entry for the field.

Allows configuration of:

-   Data Type
-   Length
-   Attributes
-   Default Values

* * * * *

### Configure Styles

Customize field appearance.

* * * * *

### Show Field

Displays technical information about the field.

Example Information:

| Property | Value |
| --- | --- |
| Table | Task |
| Field Name | cmdb_ci |
| Type | Reference |

* * * * *

Why Show Field is Useful
------------------------

Many times:

```
Field Label ≠ Field Name
```

Example:

```
Label = Configuration ItemField Name = cmdb_ci
```

Developers often need the actual field name.

* * * * *

### Watch Field

Used for debugging field behavior.

Useful when troubleshooting:

-   Client Scripts
-   UI Policies
-   Form Logic

* * * * *

8\. Related List Context Menus
==============================

Location
--------

Within Related Lists at the bottom of forms.

* * * * *

Available Actions
-----------------

### Change Filter

Modify records displayed.

* * * * *

### Refresh List

Reload related records.

* * * * *

### Column Context Menus

Available within related lists.

* * * * *

### Cell Context Menus

Available within related records.

* * * * *

9\. Administrator Customization
===============================

Administrators can:

### Add Menu Items

Create custom context menu options.

* * * * *

### Remove Menu Items

Hide unnecessary actions.

* * * * *

### Customize User Experience

Tailor menus to organizational needs.

* * * * *

Steps / Process
===============

Accessing the Main List Context Menu
------------------------------------

### Step 1

Open a List View.

### Step 2

Click:

```
☰
```

### Step 3

Select desired action.

Example:

```
Change ViewExportConfigure
```

* * * * *

Accessing a Column Context Menu
-------------------------------

### Step 1

Locate a column header.

### Step 2

Click column menu icon.

### Step 3

Choose action.

Example:

```
SortGroup ByPie Chart
```

* * * * *

Accessing a Field Context Menu
------------------------------

### Step 1

Open a Form.

### Step 2

Right-click a field.

### Step 3

Select:

```
Show FieldConfigure DictionaryConfigure Label
```

* * * * *

Important Terms
===============

| Term | Meaning |
| --- | --- |
| **Context Menu** | Menu containing actions related to the current object |
| **List Context Menu** | Menu for list-level operations |
| **Column Context Menu** | Menu for column-specific actions |
| **Cell Context Menu** | Menu for record-specific actions |
| **Form Context Menu** | Menu for form and record actions |
| **Field Context Menu** | Menu for field configuration |
| **Show Matching** | Filters records with matching values |
| **Filter Out** | Removes matching records |
| **Dictionary** | Defines field properties and behavior |
| **sys_id** | Unique identifier for a record |

* * * * *

Commands / Syntax / Configuration
=================================

Show Matching
-------------

```
Right Click Cell→ Show Matching
```

* * * * *

Filter Out
----------

```
Right Click Cell→ Filter Out
```

* * * * *

Show Field Information
----------------------

```
Right Click Field→ Show Field
```

* * * * *

Configure Dictionary
--------------------

```
Right Click Field→ Configure Dictionary
```

* * * * *

Change View
-----------

```
List Context Menu→ Change View
```

* * * * *

Examples
========

Example 1: Change List View
---------------------------

Current View:

```
Default View
```

Switch To:

```
Mobile View
```

Result:

Only essential columns are displayed.

* * * * *

Example 2: Group Records
------------------------

Column:

```
State
```

Action:

```
Group By State
```

Result:

Records grouped by status.

* * * * *

Example 3: Show Field Information
---------------------------------

Field:

```
Configuration Item
```

Show Field returns:

```
Field Name = cmdb_ciType = ReferenceTable = Task
```

* * * * *

Example 4: Filter Out
---------------------

Right-click:

```
Priority = High
```

Select:

```
Filter Out
```

Result:

High Priority records disappear from the list.

* * * * *

Certification Focus
===================

Important Points for Exams
--------------------------

-   Context menus exist in both Lists and Forms.
-   Administrators can customize context menus.
-   List Context Menu manages list-level actions.
-   Column Context Menu provides sorting and grouping.
-   Cell Context Menu provides filtering actions.
-   Form Context Menu contains record-specific actions.
-   Field Context Menu provides dictionary and field configuration options.
-   **Show Field** reveals technical field details.
-   **sys_id** can be copied from context menus.

* * * * *

Common Mistakes
---------------

❌ Confusing Field Context Menu with Form Context Menu.

❌ Assuming all context menus contain the same options.

❌ Forgetting that administrators can customize menus.

❌ Using labels instead of field names during development.

❌ Ignoring Show Field when troubleshooting.

* * * * *

Things to Remember
------------------

✅ Context menus are accessed via hamburger menus or right-clicks.

✅ Different contexts display different menu options.

✅ Show Field reveals field metadata.

✅ Configure Dictionary opens field configuration.

✅ Show Matching creates filters quickly.

✅ Filter Out excludes unwanted records.

✅ sys_id can be copied directly from context menus.

* * * * *

Real-World Application
======================

Administrators use Context Menus daily for:

-   Customizing forms
-   Modifying lists
-   Configuring fields
-   Exporting records
-   Debugging issues

Developers frequently use:

```
Show FieldConfigure DictionaryCopy sys_id
```

Support teams commonly use:

```
Show MatchingFilter OutAssign To Me
```

These shortcuts greatly improve productivity and reduce navigation time.

* * * * *

Quick Revision (30 sec)
=======================

-   Context Menus provide quick access to actions.
-   Available in both Lists and Forms.
-   Main List Menu controls list-level operations.
-   Column Menu supports sorting and grouping.
-   Cell Menu supports Show Matching and Filter Out.
-   Form Menu contains record actions.
-   Field Menu allows Configure Dictionary and Show Field.
-   Show Field displays field metadata.
-   sys_id can be copied from context menus.
-   Administrators can customize menu items.