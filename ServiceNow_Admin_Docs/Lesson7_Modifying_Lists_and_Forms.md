Modifying Lists and Forms in ServiceNow
=======================================

Lecture Summary
---------------

This lecture explains how to **personalize** and **configure** Lists and Forms in ServiceNow. Personalization affects only the logged-in user, while configuration affects all users across the system. The session also covers **List Layout**, **Form Layout**, **Form Design**, **Related Lists**, **List Calculations**, and **List Control** options available to administrators.

* * * * *

Key Points
----------

-   **Personalization** is user-specific.
-   **Configuration** is system-wide and requires admin privileges.
-   Lists can be customized by adding, removing, or reordering columns.
-   Forms can be customized by adding, removing, or rearranging fields.
-   Administrators can configure layouts for all users.
-   Related Lists can be added or removed from forms.
-   List Calculations provide averages, totals, minimums, and maximums.
-   List Controls allow administrators to restrict list functionality.

* * * * *

Detailed Notes
--------------

1\. Personalizing vs Configuring
================================

There are two ways to modify Lists and Forms in ServiceNow:

| Type | Scope | Permission Required |
| --- | --- | --- |
| Personalize | Current User Only | Any User |
| Configure | Entire System | Administrator |

### Personalization

Changes affect only the currently logged-in user.

Example:

-   Businessman Bob customizes the Incident List.
-   Admin Adam customizes the same list differently.

Each user sees their own customized version.

### Configuration

Changes affect all users in the system.

Only administrators can perform configurations.

* * * * *

2\. Personalizing Lists
=======================

Purpose
-------

Allows users to customize their own list view.

### Features

-   Add columns
-   Remove columns
-   Reorder columns

### Navigation

```
List View→ List Context Menu (Hamburger Menu)→ Personalize List Columns
```

### Example

Selected Fields:

```
NumberCreatedShort DescriptionCategoryOpened By
```

Users can:

-   Add new fields
-   Remove unwanted fields
-   Rearrange column order

These changes are stored in user preferences.

* * * * *

3\. Configuring Lists
=====================

Purpose
-------

Configure the default list layout for all users.

### Navigation

```
List Context Menu→ List Layout
```

### Features

-   Add fields
-   Remove fields
-   Reorder fields
-   Set default list structure

### Important

Only users with admin privileges can configure lists.

Configured layouts become the default view for all users.

* * * * *

4\. Personalizing Forms
=======================

Purpose
-------

Customize a form for a specific user.

### Features

-   Add fields
-   Remove fields
-   Rearrange fields

### Navigation

```
Form View→ Personalize Form
```

### Important

Changes apply only to the logged-in user.

* * * * *

5\. Configuring Forms
=====================

Purpose
-------

Modify the default form layout for all users.

### Navigation

```
Form Context Menu→ Configure→ Form Layout
```

### Features

-   Add fields
-   Remove fields
-   Reorder fields
-   Configure sections

### Example

Incident Form:

```
CallerCategoryAssignment GroupAssigned ToPriorityState
```

Administrators can rearrange these fields for everyone.

* * * * *

6\. Form Sections
=================

Forms may contain multiple sections.

Example:

```
Resolution InformationNotesRelated Records
```

### Navigation

```
Form Context Menu→ Configure→ Form Layout→ Section
```

### Capabilities

-   Add fields to sections
-   Remove fields from sections
-   Reorder fields within sections

* * * * *

7\. Form Design
===============

A visual drag-and-drop interface for form customization.

### Navigation

```
Form Context Menu→ Configure→ Form Design
```

### Features

-   Drag and drop fields
-   Change field properties
-   Modify views
-   Visual layout management

* * * * *

8\. Related Lists
=================

Related Lists display records associated with the current record.

### Example

Incident Record:

```
Task SLAsAffected CIsChange Requests
```

### Navigation

```
Form Context Menu→ Configure→ Related Lists
```

### Capabilities

-   Add Related Lists
-   Remove Related Lists
-   Select View

* * * * *

9\. List Calculations
=====================

ServiceNow can calculate values directly from list columns.

### Navigation

```
List Context Menu→ List Calculations
```

### Supported Calculations

| Calculation | Description |
| --- | --- |
| Average | Mean value |
| Sum | Total value |
| Minimum | Smallest value |
| Maximum | Largest value |

### Example

Priority Column:

```
Average Priority = 2.57
```

Displayed at the bottom of the list.

* * * * *

10\. List Control
=================

Provides advanced control over list behavior.

### Navigation

```
List Context Menu→ List Control
```

### Options

-   Hide New Button
-   Hide Edit Button
-   Disable Filters
-   Restrict Access
-   Configure List-Level Controls

* * * * *

Steps / Process
---------------

### Personalize List

```
1\. Open List View2\. Click List Context Menu3\. Select Personalize List Columns4\. Add/Remove Columns5\. Save
```

* * * * *

### Configure List

```
1\. Open List View2\. Click List Context Menu3\. Select List Layout4\. Modify Fields5\. Save
```

* * * * *

### Personalize Form

```
1\. Open Form2\. Click Personalize Form3\. Add/Remove Fields4\. Save
```

* * * * *

### Configure Form

```
1\. Open Form2\. Form Context Menu3\. Configure4\. Form Layout5\. Modify Fields6\. Save
```

* * * * *

### Configure Related Lists

```
1\. Open Form2\. Form Context Menu3\. Configure4\. Related Lists5\. Add/Remove Lists6\. Save
```

* * * * *

Important Terms
---------------

| Term | Meaning |
| --- | --- |
| Personalize List | User-specific list customization |
| Configure List | System-wide list customization |
| Personalize Form | User-specific form customization |
| Configure Form | System-wide form customization |
| List Layout | Controls columns shown in a list |
| Form Layout | Controls fields shown on a form |
| Form Design | Drag-and-drop form editor |
| Related List | Displays related records |
| List Calculations | Aggregate functions on list data |
| List Control | Advanced controls for list behavior |

* * * * *

Commands / Configuration
------------------------

### Personalize List

```
List Context Menu→ Personalize List Columns
```

### Configure List

```
List Context Menu→ List Layout
```

### Personalize Form

```
Personalize Form
```

### Configure Form

```
Form Context Menu→ Configure→ Form Layout
```

### Form Design

```
Form Context Menu→ Configure→ Form Design
```

### Related Lists

```
Form Context Menu→ Configure→ Related Lists
```

* * * * *

Examples
--------

### Example 1

Personalized Incident List

User A:

```
NumberPriorityAssigned To
```

User B:

```
NumberCategoryCallerState
```

Both users see different layouts.

* * * * *

### Example 2

Configured Incident Form

Administrator adds:

```
Business ServiceConfiguration ItemAssignment Group
```

All users now see these fields.

* * * * *

### Example 3

Related List

Added:

```
Affected CIs
```

Users can view affected Configuration Items directly from the Incident form.

* * * * *

Certification Focus
-------------------

### Important for CSA Exam

✔ Difference between Personalization and Configuration

✔ Personalize affects only current user

✔ Configure affects all users

✔ List Layout vs Form Layout

✔ Related Lists purpose

✔ Form Design functionality

✔ List Calculations usage

✔ List Control capabilities

### Common Mistakes

❌ Assuming personalization affects all users

❌ Confusing Form Layout with Form Design

❌ Forgetting admin permissions are required for configuration

* * * * *

Real-World Application
----------------------

Administrators commonly:

-   Configure Incident forms
-   Configure Change forms
-   Add business-required fields
-   Create department-specific views
-   Configure Related Lists
-   Customize Service Desk user experience
-   Use List Calculations for reporting analysis

* * * * *

Quick Revision (30 Seconds)
---------------------------

-   Personalization = User-specific
-   Configuration = System-wide
-   List Layout configures list columns
-   Form Layout configures form fields
-   Form Design provides drag-and-drop customization
-   Related Lists display associated records
-   List Calculations show averages, totals, min, max
-   List Control manages list permissions and behavior
-   Admin role required for configuration
-   Personalized views override configured defaults