Lecture Summary
---------------

This lecture explains **Dictionary Properties** in ServiceNow. The instructor demonstrates how to configure field-level properties such as **Mandatory**, **Read Only**, **Display**, **Default Values**, and **Dependent Values**. The lecture also introduces the **Current Object**, **Calculated Fields**, **Display Values**, and how auto-generated numbers work through **Number Maintenance**.

* * * * *

Key Points
----------

-   **Dictionary = Field = Column** (all mean the same thing).
-   Field settings are called **Dictionary Properties**.
-   Important dictionary properties:
    -   Mandatory
    -   Read Only
    -   Display
    -   Default Value
    -   Dependent Value
    -   Calculated Value
-   Default values populate only on **new records**.
-   Only **one field** should be marked as Display.
-   **Current Object** stores all field values of a record.
-   Dependent choice lists filter values based on another field.
-   Number generation is controlled through **Number Maintenance**.

* * * * *

Detailed Notes
==============

Understanding Dictionary
========================

What is a Dictionary?
---------------------

In ServiceNow:

| Term | Meaning |
| --- | --- |
| Dictionary | Field |
| Field | Column |
| Column | Database Field |

All three terms represent the same thing.

Example:

```
Shipping Case Table   ↓Fields/Dictionaries   ↓ColorPriorityShort DescriptionCategorySubcategory
```

* * * * *

Dictionary Properties
=====================

Dictionary properties control the behavior of fields.

Common dictionary properties:

-   Mandatory
-   Read Only
-   Display
-   Default Value
-   Dependent Value
-   Calculated Value

* * * * *

Mandatory Fields
================

Purpose
-------

Mandatory fields must be filled before submitting a record.

### Example

Fields made mandatory:

```
ColorShort Description
```

### Configuration

1.  Open the field from the table.
2.  Check:

```
Mandatory = True
```

1.  Save.

### Result

Users cannot submit the form without entering values.

* * * * *

Real-Life Example
-----------------

Bank Account Opening Form

Mandatory details:

-   First Name
-   Last Name
-   Aadhaar Number
-   PAN Number
-   Date of Birth

Without mandatory details, the account cannot be created.

Similarly, ServiceNow requires mandatory fields before creating records.

* * * * *

Read Only Fields
================

Purpose
-------

Prevent users from modifying a field.

### Example

Fields configured as Read Only:

```
NumberPriority
```

### Configuration

1.  Open field dictionary.
2.  Check:

```
Read Only = True
```

1.  Save.

### Result

Users can view the value but cannot edit it.

* * * * *

New Record vs Existing Record
=============================

New Record
----------

Characteristics:

```
System ID = -1Label = New Record
```

Indicates the record has not been saved yet.

* * * * *

Existing Record
---------------

Characteristics:

```
System ID generatedRecord Number generated
```

After saving:

```
SH001014
```

The record becomes an existing record.

* * * * *

Display Field
=============

What is a Display Field?
------------------------

Display field represents the record when referenced elsewhere.

* * * * *

Default Behavior
----------------

Initially:

```
Number
```

acts as the display value.

Example:

```
SH001014
```

* * * * *

Changing Display Field
----------------------

Instead of Number:

```
Short Description
```

can become the display field.

### Configuration

1.  Open field dictionary.
2.  Check:

```
Display = True
```

1.  Save.

* * * * *

Important Rule
--------------

Only **one field** should be marked as Display.

### Incorrect

```
Short Description = DisplayDescription = Display
```

### Problem

System becomes confused about which field to display.

* * * * *

Default Values
==============

Purpose
-------

Automatically populate values when opening a new record.

### Important

Default values only populate on:

```
New Records
```

They do not overwrite existing records.

* * * * *

Examples
--------

### Caller

Populate logged-in user automatically.

Configuration:

```
Use Dynamic Default = Me
```

* * * * *

### Contact Type

Default:

```
Walk-In
```

* * * * *

### State

Default:

```
New
```

* * * * *

### Impact

Default:

```
Low
```

* * * * *

### Urgency

Default:

```
Low
```

* * * * *

### Priority

Default:

```
Very Low
```

* * * * *

### Active

Default:

```
True
```

* * * * *

How to Configure
----------------

1.  Open field dictionary.
2.  Scroll to:

```
Default Value
```

1.  Enter the desired value.
2.  Save.

* * * * *

Choice Labels vs Choice Values
==============================

Important Concept
-----------------

Choices contain:

### Choice Label

Visible to users.

Example:

```
Low
```

### Choice Value

Stored in database.

Example:

```
low
```

* * * * *

Configuration Rule
------------------

Use:

```
Choice Value
```

inside Default Value field.

Not the Label.

* * * * *

Dependent Values
================

Purpose
-------

Filter choices based on another field's selection.

* * * * *

Example
-------

### Category

```
SoftwareHardwareDatabaseNetworkInquiry
```

* * * * *

### Subcategory

Depends on Category.

* * * * *

### Software

Subcategories:

```
LinuxWindowsUnix
```

* * * * *

### Hardware

Subcategories:

```
LaptopDesktopKeyboard
```

* * * * *

### Database

Subcategories:

```
OracleMySQLSybase
```

* * * * *

Configuration
-------------

### Step 1

Open:

```
Subcategory Field
```

### Step 2

Advanced View

### Step 3

Set:

```
Dependent Field = Category
```

### Step 4

Map dependent values for each choice.

* * * * *

Result
------

Selecting:

```
Category = Software
```

Shows:

```
LinuxWindowsUnix
```

Only.

* * * * *

Current Object
==============

Very Important Concept
----------------------

The instructor emphasized this as a critical ServiceNow concept.

* * * * *

Purpose
-------

Current Object stores all field values of the current record.

Example record values:

```
NumberCallerCategorySubcategoryPriorityDescription
```

All are available in:

```
current
```

* * * * *

Accessing Values
----------------

### Method 1

```
current.u_number
```

Returns:

```
Number field value
```

* * * * *

### Method 2

```
current.u_category
```

Returns:

```
Category value
```

* * * * *

### Method 3

```
current.u_subcategory
```

Returns:

```
Subcategory value
```

* * * * *

Alternative Method
------------------

Using getValue()

```
current.getValue('u_number')
```

```
current.getValue('u_category')
```

```
current.getValue('u_subcategory')
```

Both methods retrieve field values.

* * * * *

Calculated Fields
=================

Purpose
-------

Generate values dynamically based on other fields.

* * * * *

Example Requirement
-------------------

Display:

```
Number + Short Description
```

Example:

```
SH001014 Order Not Received
```

* * * * *

Steps
-----

### Step 1

Create new String field:

```
Display Name
```

* * * * *

### Step 2

Open Advanced View.

* * * * *

### Step 3

Check:

```
Calculated = True
```

* * * * *

### Step 4

Use script.

Example logic:

```
current.getValue('u_number') +current.getValue('u_short_description')
```

* * * * *

### Step 5

Save.

* * * * *

### Step 6

Mark this new field as:

```
Display = True
```

* * * * *

Result
------

Record display value becomes:

```
Number + Short Description
```

* * * * *

Number Field Behavior
=====================

Observation
-----------

When opening a new form:

```
SH001005
```

Refresh:

```
SH001006
```

Refresh:

```
SH001007
```

Even without saving.

* * * * *

Important Note
--------------

Number sequence continues increasing regardless of save.

Unused numbers are skipped.

This is expected ServiceNow behavior.

* * * * *

Number Maintenance
==================

Purpose
-------

Manage auto-generated numbers.

* * * * *

Navigation
----------

```
Number Maintenance
```

* * * * *

Features
--------

### Reset Counter

Restart numbering sequence.

* * * * *

### Change Starting Point

Example:

```
1000
```

to

```
2000
```

New records begin from:

```
SH002000
```

* * * * *

Preview Icon
============

Purpose
-------

View referenced record details quickly.

### Example

Caller Field

```
John Steele
```

Preview icon displays:

-   User ID
-   First Name
-   Last Name
-   User Information

Without opening the full record.

* * * * *

Form as a Data Source
=====================

Important Concept
-----------------

Forms are only one method of inserting data.

Other data sources:

-   Forms
-   Email
-   Excel Import
-   Record Producers
-   Scripts
-   Virtual Agents

All eventually store data in ServiceNow tables.

* * * * *

Steps / Process
===============

Make Field Mandatory
--------------------

1.  Open field dictionary.
2.  Check Mandatory.
3.  Save.

* * * * *

Make Field Read Only
--------------------

1.  Open field dictionary.
2.  Check Read Only.
3.  Save.

* * * * *

Set Display Field
-----------------

1.  Open field.
2.  Check Display.
3.  Save.

* * * * *

Configure Default Value
-----------------------

1.  Open field.
2.  Enter Default Value.
3.  Save.

* * * * *

Configure Dependent Choices
---------------------------

1.  Open dependent field.
2.  Select parent field.
3.  Map dependent values.
4.  Save.

* * * * *

Create Calculated Field
-----------------------

1.  Create String field.
2.  Enable Calculated.
3.  Write calculation logic.
4.  Save.
5.  Mark field as Display if required.

* * * * *

Important Terms
===============

| Term | Meaning |
| --- | --- |
| Dictionary | Field definition |
| Mandatory | Must be filled |
| Read Only | Cannot be edited |
| Display Field | Record identifier shown to users |
| Default Value | Automatically populated value |
| Dependent Value | Choice depends on another field |
| Current Object | Holds current record values |
| Calculated Field | Value generated dynamically |
| Choice Label | Visible text |
| Choice Value | Stored database value |
| Number Maintenance | Controls auto-numbering |

* * * * *

Commands / Syntax / Configuration
=================================

### Access Field Value

```
current.u_number
```

```
current.u_category
```

* * * * *

### Using getValue()

```
current.getValue('u_number')
```

```
current.getValue('u_category')
```

* * * * *

### Dynamic Default User

```
Use Dynamic Default = Me
```

* * * * *

### Calculated Field

```
current.getValue('u_number') +current.getValue('u_short_description')
```

* * * * *

Examples
========

Example 1: Mandatory Field
--------------------------

```
ColorShort Description
```

Must be filled before submission.

* * * * *

Example 2: Default Values
-------------------------

```
Caller = Logged-In UserState = NewPriority = Very Low
```

* * * * *

Example 3: Dependent Choices
----------------------------

```
Category = Software
```

Subcategories:

```
LinuxWindowsUnix
```

* * * * *

Example 4: Calculated Display Value
-----------------------------------

```
SH001014 Order Not Received
```

Generated using:

```
Number + Short Description
```

* * * * *

Certification Focus
===================

Important Points for Exams
--------------------------

-   Dictionary = Field = Column.
-   Mandatory, Read Only, Display, Default Value are dictionary properties.
-   Only one field should be marked as Display.
-   Default values apply only to new records.
-   Current Object stores record field values.
-   Dependent values require a parent-child relationship.
-   Choice Value is used internally, not Choice Label.
-   Number Maintenance controls auto-number generation.

* * * * *

Common Mistakes
---------------

❌ Using Choice Label instead of Choice Value.

❌ Marking multiple fields as Display.

❌ Expecting Default Values to update existing records.

❌ Forgetting to set the parent field when configuring dependent choices.

❌ Assuming forms are the only source of data entry.

* * * * *

Things to Remember
------------------

-   System ID = -1 means New Record.
-   Default values populate only on new forms.
-   Read Only fields cannot be edited.
-   Display field identifies records.
-   Current Object is heavily used in scripting.
-   Calculated fields derive values dynamically.
-   Number generation continues even if records are not saved.

* * * * *

Real-World Application
======================

### Incident Management

-   Category → Subcategory dependency.
-   Auto-generated incident numbers.
-   Default priorities and states.

### Customer Service

-   Shipping case numbers generated automatically.
-   Mandatory customer details.
-   Read-only tracking numbers.

### Employee Self-Service

-   Logged-in user automatically populated.
-   Default values reduce manual entry.

### Enterprise Applications

-   Calculated display names improve readability.
-   Dependent fields improve user experience and data quality