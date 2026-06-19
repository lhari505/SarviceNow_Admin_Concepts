Lecture Summary
---------------

This lecture focuses on **Form Sections** and **Views** in ServiceNow. The instructor demonstrates how to organize forms using sections to improve usability and how a single form can be displayed in multiple views for different user groups. The session also explains the relationship between **Sections, Views, View Rules**, and introduces the difference between **Number** and **Sys ID**.

* * * * *

Key Points
----------

-   Sections make forms organized and user-friendly.
-   A form can contain multiple sections (tabs).
-   One form can have multiple views.
-   Different users can see the same form differently using views.
-   Number and Sys ID serve different purposes.
-   Form Design and Form Layout can both be used to customize forms.
-   View Rules automatically determine which view a user sees.

* * * * *

Detailed Notes
==============

Form Sections
=============

Why Create Sections?
--------------------

When a form contains many fields:

-   Users get confused.
-   The form becomes difficult to navigate.
-   Important information becomes harder to find.

### Benefits of Sections

-   Better organization
-   Easier navigation
-   Improved user experience
-   Logical grouping of information

* * * * *

What is a Section?
------------------

A **Section** is a separate area/tab on a form used to group related fields.

### Example

```
NotesRelated RecordsResolution InformationSystem Information
```

Each section contains fields related to that topic.

* * * * *

Creating Sections
-----------------

### Navigation

```
Form Design → Click (+) icon
```

### Steps

1.  Open Form Design.
2.  Click the **+ (New Section)** icon.
3.  Provide a section name.
4.  Select:
    -   One Column
    -   Two Columns
5.  Add required fields.
6.  Save the form.

* * * * *

Notes Section
=============

### Purpose

Store communication and activity-related information.

### Fields Added

-   Watch List
-   Work Notes
-   Activity Filter

### Important

**Activity Filter** is not a normal field.

It tracks:

-   Updates
-   Changes
-   Activities performed on the record

* * * * *

Resolution Information Section
==============================

### Purpose

Store closure-related information.

### Fields Added

-   Opened At
-   Resolved At
-   Closed At
-   Cancelled At

Additional fields:

-   Resolution Code (Choice Field)
-   Resolution Notes (String Field)

* * * * *

System Information Section
==========================

### Purpose

Store system-generated audit information.

### Fields Added

-   Created
-   Created By
-   Updated
-   Updated By
-   Updates

* * * * *

Sys ID vs Number
================

Sys ID
------

### Characteristics

-   Generated automatically.
-   Unique identifier for developers.
-   Exists behind the scenes.
-   Not shown on forms.

### Why Not Show Sys ID?

Employees:

-   Do not understand Sys ID.
-   Do not need Sys ID.

Therefore:

```
Sys ID is hidden from users.
```

* * * * *

Number Field
------------

### Characteristics

-   Visible to users.
-   Automatically generated.
-   Unique for every record.

Example:

```
SH001014SH001015SH001016
```

### Important

Once generated:

```
Number never changes.
```

* * * * *

Exam Tip
--------

| User Type | Unique Identifier |
| --- | --- |
| Employee | Number |
| Developer | Sys ID |

* * * * *

Related Records Section
=======================

Purpose
-------

Store relationships with other records.

### Example Fields

### Incident

Reference Table:

```
Incident Table
```

### Problem

Reference Table:

```
Problem Table
```

* * * * *

Understanding Views
===================

What is a View?
---------------

A **View** is a different layout of the same form.

The underlying table remains the same.

Only the appearance changes.

* * * * *

Why Use Views?
--------------

Different users may require different information.

Examples:

-   America Team
-   Germany Team
-   Australia Team
-   Korea Team
-   Paris Team

Each group can see a customized version of the same form.

* * * * *

Creating Views
==============

### Navigation

```
Form Design → View Dropdown
```

### Create New View

Example:

```
American ViewGermany ViewParis ViewAustralia ViewKorea View
```

* * * * *

Example Views
=============

Default View
------------

Original form layout.

-   Two columns
-   All sections visible

* * * * *

American View
-------------

-   Single-column layout
-   All sections visible

* * * * *

Germany View
------------

Only selected fields shown.

Example:

```
UrgencyImpactPriorityAssignment GroupAssigned To
```

* * * * *

Australia View
--------------

Minimal fields displayed.

Example:

```
CallerAssigned ToConfiguration Item
```

* * * * *

Korea View
----------

-   No sections
-   Simple form layout

* * * * *

Paris View
----------

Custom field arrangement.

* * * * *

Switching Views
===============

### Navigation

```
Hamburger Menu → View
```

Available Views:

```
DefaultAmericanAustraliaGermanyKoreaParis
```

* * * * *

View Rules
==========

Purpose
-------

Automatically display the correct view.

### Example

If user location is:

```
America
```

Display:

```
American View
```

* * * * *

If user location is:

```
Korea
```

Display:

```
Korea View
```

* * * * *

How Does ServiceNow Know?
-------------------------

Uses the **Location** field in the User record.

### Example

User Record

```
John SteelLocation: Dallas
```

Based on location:

-   America View
-   Australia View
-   Germany View
-   Korea View

can be assigned automatically.

* * * * *

Important Note
--------------

View Rules require:

```
Scripting
```

This topic will be covered later.

* * * * *

Form Design vs Form Layout
==========================

Form Design
-----------

Allows:

-   Create fields
-   Create sections
-   Create views
-   Arrange fields visually

### Limitation

Field names may need manual adjustment.

* * * * *

Form Layout
-----------

Allows:

-   Create fields
-   Create views
-   Create sections
-   Rearrange fields

### Advantage

Simpler field creation process.

* * * * *

Instructor Recommendation
-------------------------

Preferred:

```
Form Layout
```

Reason:

-   Faster
-   Easier
-   Less manual work

* * * * *

Ways to Create Fields
=====================

Method 1
--------

From Table

```
System Definition → Tables
```

* * * * *

Method 2
--------

From Form Design

* * * * *

Method 3
--------

From Form Layout

### Recommended Method

```
Form Layout
```

* * * * *

Form Sections Table
===================

Navigation
----------

```
Application Navigator → Form Sections
```

This stores all sections created for forms.

* * * * *

### Example

Shipping Case Table

Views:

```
Default ViewAmerican ViewAustralia ViewGermany ViewParis View
```

Each view contains its own section definitions.

* * * * *

Deleting Views
==============

Navigation
----------

```
System UI → Views
```

### Steps

1.  Open Views module.
2.  Search for view name.
3.  Open view record.
4.  Delete it.

### Example

Delete:

```
Korea View
```

* * * * *

Real ServiceNow Examples
========================

Incident Table
--------------

ServiceNow creates:

```
Incident Table
```

Then creates:

```
Incident Form
```

Then creates:

```
Multiple Views
```

* * * * *

Problem Table
-------------

```
Problem Table     ↓Problem Form     ↓Multiple Views
```

* * * * *

User Table
----------

```
sys_user
```

Example Views:

-   Default View
-   Self-Service View

When users click their profile:

```
Self-Service View
```

is displayed automatically.

* * * * *

Steps / Process
===============

Create Form Sections
--------------------

1.  Open Form Design.
2.  Click (+).
3.  Enter section name.
4.  Choose layout.
5.  Add fields.
6.  Save.
7.  Refresh form.

* * * * *

Create Views
------------

1.  Open Form Design.
2.  Select View Dropdown.
3.  Click New View.
4.  Enter view name.
5.  Customize layout.
6.  Save.

* * * * *

Delete Views
------------

1.  Navigate to:

```
System UI → Views
```

1.  Search for view.
2.  Open record.
3.  Delete.

* * * * *

Important Terms
===============

| Term | Meaning |
| --- | --- |
| Section | Group of related fields shown as a tab |
| View | Different layout of the same form |
| View Rule | Logic that automatically selects a view |
| Number | User-visible unique record identifier |
| Sys ID | Developer-visible unique record identifier |
| Activity Filter | Tracks record activities |
| Form Design | Visual tool for designing forms |
| Form Layout | Alternative tool for arranging forms |
| Self-Service View | Simplified user-facing view |

* * * * *

Commands / Configuration / Navigation
=====================================

### Form Design

```
Form Design
```

### Form Layout

```
Form Layout
```

### Form Sections

```
Application Navigator → Form Sections
```

### Views

```
System UI → Views
```

### Switch View

```
Hamburger Menu → View
```

* * * * *

Examples
========

Example 1: Notes Section
------------------------

Contains:

```
Watch ListWork NotesActivity Filter
```

* * * * *

Example 2: Resolution Information
---------------------------------

Contains:

```
Opened AtResolved AtClosed AtCancelled At
```

* * * * *

Example 3: Automatic View Selection
-----------------------------------

```
User Location = America
```

Result:

```
American View
```

* * * * *

Certification Focus
===================

Important Points for Exams
--------------------------

-   Sections organize forms into tabs.
-   One form can have multiple views.
-   Views only change appearance, not data.
-   Sys ID is hidden from end users.
-   Number is visible to users.
-   View Rules determine which view is displayed.
-   User location can be used in View Rules.
-   Form Design and Form Layout provide similar functionality.

* * * * *

Common Mistakes
---------------

❌ Confusing Sections with Views

❌ Thinking Views create separate tables

❌ Assuming Sys ID is visible on forms

❌ Believing Number and Sys ID are the same

❌ Forgetting that every view maintains its own section configuration

* * * * *

Things to Remember
------------------

-   Sections = Tabs
-   Views = Different layouts of same form
-   Number = Employee identifier
-   Sys ID = Developer identifier
-   View Rules require scripting
-   Form Layout is often easier than Form Design

* * * * *

Real-World Application
======================

### Global Organizations

Different countries may need different form layouts.

Examples:

-   US Support Team
-   Germany Support Team
-   Australia Support Team

All use the same table but see different views.

* * * * *

### ITSM Applications

Incident, Problem, Change, User, and Group forms all use:

-   Sections
-   Views
-   View Rules

to improve usability