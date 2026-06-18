Lecture Summary
---------------

This lecture explains how **ServiceNow forms are designed from database tables**. The instructor demonstrates creating a new table (**Shipping Case**) and designing a form by adding different field types such as **Reference, String, Choice, Date/Time, Boolean, and List** fields. The lecture also covers **auto-number generation**, form layout design, and the relationship between **tables and forms** in ServiceNow.

* * * * *

Key Points
----------

-   Every ServiceNow form is based on a **database table**.
-   Creating a table automatically creates **6 system fields**.
-   Forms are designed by adding fields to the table.
-   Different field types serve different purposes:
    -   Reference
    -   String
    -   Choice
    -   Date/Time
    -   Boolean (True/False)
    -   List
-   Auto-numbering can generate unique record numbers automatically.
-   Form layouts can be organized into one-column or two-column views.
-   Data entered through forms is stored in the corresponding table.

* * * * *

Detailed Notes
==============

Understanding Form Design
-------------------------

### Core Principle

Before designing a form:

-   A **table must exist in the database**.
-   Forms are created based on tables.
-   Data entered in forms is stored in the corresponding table.

**Flow:**

```
Table Creation      ↓Field Creation      ↓Form Design      ↓Users Create Records      ↓Data Stored in Table
```

* * * * *

Automatic System Fields
-----------------------

Whenever a new table is created, ServiceNow automatically creates the following fields:

| System Field |
| --- |
| Created |
| Created By |
| Updated |
| Updated By |
| Updates |
| Sys ID |

These fields exist on the table automatically but may not appear on the form unless explicitly added.

* * * * *

Creating a New Table
--------------------

### Example

Table Label:

```
Shipping Case
```

When the label is entered:

-   Table name is automatically generated.
-   Custom tables start with:

```
u_
```

Example:

```
u_shipping_case
```

### Notes

-   Table label is usually provided by the client.
-   Developers generally do not decide table names independently.

* * * * *

Auto Number Field
-----------------

### Purpose

Generate unique record numbers automatically.

### Example

Incident records:

```
INC0010001
```

Shipping Case records:

```
SH0010001
```

### Configuration

Enable:

```
Auto Number Checkbox
```

Define:

-   Prefix → SH
-   Starting Number
-   Number Length

### Result

A **Number** field is created automatically.

* * * * *

Reference Fields
================

What is a Reference Field?
--------------------------

A reference field points to records in another table.

### Characteristics

-   Shows a **magnifying glass icon**.
-   Accepts only valid records from the referenced table.
-   Invalid values are rejected.

* * * * *

Example 1: Caller Field
-----------------------

Field:

```
Caller
```

Reference Table:

```
sys_user
```

Users can only select existing users.

* * * * *

Example 2: Configuration Item
-----------------------------

Field:

```
Configuration Item
```

Reference Table:

```
cmdb_ci
```

Used to select configuration items from CMDB.

* * * * *

Example 3: Assignment Group
---------------------------

Reference Table:

```
sys_user_group
```

* * * * *

Example 4: Assigned To
----------------------

Reference Table:

```
sys_user
```

* * * * *

String Fields
=============

What is a String Field?
-----------------------

A string field accepts:

-   Letters
-   Numbers
-   Special Characters

### Examples

### Short Description

```
Length: 500 characters
```

### Description

```
Length: 2000 characters
```

### Usage

Used for entering free-text information.

* * * * *

Choice Fields
=============

What is a Choice Field?
-----------------------

Provides a predefined dropdown list.

### Example: Category

Choices:

```
SoftwareHardwareNetworkDatabaseQuery
```

* * * * *

### Example: Contact Type

Choices:

```
EmailPhoneWalk-InVirtual AgentTransfer
```

* * * * *

### Example: State

Choices:

```
NewIn ProgressOn HoldResolvedClosedCancelled
```

* * * * *

Choice Label vs Choice Value
----------------------------

### Choice Label

Displayed to users.

Example:

```
CriticalHighMediumLow
```

### Choice Value

Stored in database.

Example:

```
1234
```

### Why Use Numeric Values?

Makes calculations and scripting easier.

Example:

```
Priority <= 2
```

is easier than:

```
Priority == Critical OR High
```

* * * * *

Date/Time Fields
================

Purpose
-------

Track important timestamps.

### Examples

-   Opened At
-   Resolved At
-   Closed At
-   Cancelled At

* * * * *

Date vs Date-Time
-----------------

### Date

```
YYYY-MM-DD
```

### Date-Time (Timestamp)

```
YYYY-MM-DD HH:MM:SS
```

Includes:

-   Date
-   Hours
-   Minutes
-   Seconds

* * * * *

True/False Fields
=================

Purpose
-------

Store Boolean values.

### Display

Shown as a checkbox.

### Values

```
TrueFalse
```

Examples:

-   Active
-   Knowledge

* * * * *

List Fields
===========

What is a List Field?
---------------------

A list field allows selecting **multiple records**.

### Reference Field

Can select only one record.

Example:

```
John Steel
```

* * * * *

### List Field

Can select multiple records.

Example:

```
John SteelAbraham Lincoln
```

* * * * *

Example
-------

Field:

```
Watch List
```

Reference Table:

```
sys_user
```

* * * * *

Form Layout Design
==================

Single Column Layout
--------------------

All fields appear vertically.

```
Field 1Field 2Field 3
```

* * * * *

Two Column Layout
-----------------

Fields appear side by side.

```
Field A      Field BField C      Field D
```

* * * * *

Creating Sections
-----------------

Use:

```
+
```

(Create New Section)

### Important

Remove the section name if unnecessary.

* * * * *

Example Layout
--------------

### Left Column

-   Number
-   Caller
-   Category
-   Subcategory
-   Configuration Item

### Right Column

-   Contact Type
-   State
-   Impact
-   Urgency
-   Assignment Group
-   Assigned To

### Separate Section

-   Short Description
-   Description

Displayed in full width (single column).

* * * * *

Label vs Name Concepts
======================

Table
-----

| Property | Purpose |
| --- | --- |
| Table Label | User-friendly |
| Table Name | Developer/Internal |

* * * * *

Fields
------

| Property | Purpose |
| --- | --- |
| Field Label | User-friendly |
| Field Name | Developer/Internal |

* * * * *

Choices
-------

| Property | Purpose |
| --- | --- |
| Choice Label | User-friendly |
| Choice Value | Stored value |

* * * * *

Important Rule
--------------

After a field is created:

✅ Label can be changed.

❌ Name cannot be changed.

To change a field name:

1.  Delete field
2.  Create field again

* * * * *

ServiceNow Architecture Explained
=================================

Example: Incident Management
----------------------------

### Step 1

ServiceNow creates:

```
Incident Table
```

* * * * *

### Step 2

Designs:

```
Incident Form
```

* * * * *

### Step 3

Employees use the form.

* * * * *

### Step 4

Incident record is created.

* * * * *

### Step 5

Record is stored in Incident Table.

* * * * *

### Step 6

Support team resolves the issue.

* * * * *

### Step 7

Incident remains stored permanently for future reference.

* * * * *

Steps / Process
===============

Create a New Form
-----------------

### Step 1

Navigate:

```
System Definition → Tables
```

### Step 2

Create a new table.

### Step 3

Enable Auto Number if required.

### Step 4

Create fields:

-   Reference
-   String
-   Choice
-   Date/Time
-   Boolean
-   List

### Step 5

Design form layout.

### Step 6

Create sections.

### Step 7

Save and refresh.

### Step 8

Test form functionality.

* * * * *

Important Terms
===============

| Term | Meaning |
| --- | --- |
| Table | Database structure storing records |
| Form | User interface for entering records |
| Reference Field | Points to another table |
| String Field | Free text field |
| Choice Field | Dropdown field |
| List Field | Multi-select reference field |
| Auto Number | Automatically generated record number |
| Configuration Item (CI) | Asset/component stored in CMDB |
| Section | Grouping of fields on a form |
| Timestamp | Date and time together |
| sys_user | User table |
| sys_user_group | Group table |
| cmdb_ci | Configuration Item table |

* * * * *

Commands / Syntax / Configuration
=================================

### Create Table

```
System Definition → Tables
```

### Auto Number Configuration

```
Auto Number = TruePrefix = SH
```

### Common Reference Tables

```
sys_usersys_user_groupcmdb_ci
```

* * * * *

Examples
========

Example 1
---------

Caller field referencing:

```
sys_user
```

Users can only select existing users.

* * * * *

Example 2
---------

Watch List:

```
John SteelAbraham Lincoln
```

Multiple users selected.

* * * * *

Example 3
---------

Category Dropdown:

```
SoftwareHardwareNetworkDatabase
```

* * * * *

Certification Focus
===================

Important Points for Exams
--------------------------

-   Every form is based on a table.
-   Custom tables start with **u_**.
-   Reference fields point to another table.
-   List fields allow multiple selections.
-   Choice fields contain labels and values.
-   Auto Number creates unique record IDs.
-   Form Designer can be used to create fields and layouts.

* * * * *

Common Mistakes
---------------

❌ Confusing Label and Name

❌ Assuming system fields automatically appear on forms

❌ Using Reference field when List field is required

❌ Forgetting reference table selection

❌ Thinking field names can be renamed later

* * * * *

Things to Remember
------------------

-   Labels can be modified.
-   Field names cannot be modified after creation.
-   Data always resides in tables.
-   Forms are only a user interface layer.
-   Choice values are often numeric for easier calculations.