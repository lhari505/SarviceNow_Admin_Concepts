**Condition Builder and Breadcrumbs in ServiceNow**
===================================================

Lecture Summary
---------------

This lecture explains two important ServiceNow list filtering features: the **Condition Builder** and **Breadcrumbs**. The Condition Builder enables users to create complex queries without writing SQL, while Breadcrumbs provide a visual representation of active filters and allow quick modifications. The lecture also covers reference fields, saving filters, loading filters, sorting, and using quick filtering options such as **Show Matching** and **Filter Out**.

* * * * *

Key Points
==========

-   **Condition Builder** is used to create advanced queries without SQL.
-   Queries are built using **Field → Operator → Value**.
-   Supports filtering on **reference fields** and related records.
-   Filters can be **saved**, **loaded**, and **shared**.
-   **Breadcrumbs** display active filter conditions.
-   Breadcrumbs can be used to remove conditions quickly.
-   Right-click actions provide shortcuts such as **Show Matching** and **Filter Out**.
-   Conditions can be combined using **AND** and **OR** logic.
-   Filters can include sorting conditions.
-   Reference fields allow filtering based on related table data.

* * * * *

Detailed Notes
==============

1\. What is the Condition Builder?
----------------------------------

### Definition

The **Condition Builder** is a graphical query-building tool in ServiceNow that allows users to filter records without writing SQL statements.

### Purpose

It helps users:

-   Search records
-   Filter large datasets
-   Create complex queries
-   Save reusable filters
-   Access related record information

### Key Benefit

Users can create advanced database queries through a user-friendly interface.

* * * * *

2\. Structure of a Condition
============================

Every condition follows the same format:

```
Field → Operator → Value
```

### Example

```
Active → is → True
```

This returns all active records.

* * * * *

### Another Example

```
State → is one of → On Hold, Resolved
```

This returns records whose state is either:

-   On Hold
-   Resolved

* * * * *

3\. Opening the Condition Builder
=================================

### Steps

1.  Navigate to a List View.
2.  Click the **Filter Icon** (top-left).
3.  The Condition Builder panel opens.
4.  Build conditions using fields, operators, and values.

* * * * *

4\. Components of the Condition Builder
=======================================

Load Filter
-----------

Used to load previously saved filters.

* * * * *

Save Filter
-----------

Used to save frequently used filters.

Benefits:

-   Reusability
-   Consistency
-   Faster searching

* * * * *

Add Sort
--------

Allows sorting query results.

Example:

```
Category → Ascending
```

* * * * *

Condition Area
--------------

The main area where conditions are created.

Structure:

```
Field + Operator + Value
```

* * * * *

5\. Understanding Field Types
=============================

Different field types provide different operators.

* * * * *

Boolean Fields
--------------

Example:

```
Active
```

Possible values:

```
TrueFalse
```

Available operators:

-   is
-   is not
-   is empty

### Example

```
Active is True
```

* * * * *

Choice Fields
-------------

Example:

```
State
```

Available operators:

-   is
-   is not
-   is one of
-   is not one of

### Example

```
State is one ofOn Hold, Resolved
```

* * * * *

Reference Fields
----------------

Reference fields point to another table.

Example:

```
Assigned ToCallerOpened By
```

Reference fields are indicated by an arrow icon.

* * * * *

6\. Working with Reference Fields
=================================

### What Are Reference Fields?

A reference field stores a link to another record.

Example:

`Incident\
   ↓\
Caller\
   ↓\
User Record`

This allows access to user-related data.

* * * * *

### Example Query

Filter incidents where:

```
Caller → Location → San Francisco
```

This query searches the User table through the Caller field.

* * * * *

### Another Example

```
Assigned To → Location → San Diego
```

Returns incidents assigned to users located in San Diego.

* * * * *

7\. Creating an AND Condition
=============================

### Example Query

Condition 1:

```
Active is True
```

AND

Condition 2:

```
State is one ofOn Hold, Resolved
```

AND

Condition 3:

```
Impact is not one ofMedium, Low
```

* * * * *

### Meaning

Return incidents that:

-   Are Active
-   Are On Hold OR Resolved
-   Have High Impact

* * * * *

### Result

The demo returned:

```
4 Matching Records
```

* * * * *

8\. Understanding OR Conditions
===============================

Multiple condition groups can be combined.

### Example

Group 1

```
Active = TrueState = On Hold or ResolvedImpact ≠ Medium or Low
```

OR

Group 2

```
Active = FalseImpact = Low
```

* * * * *

### Logic

```
(Group 1)OR(Group 2)
```

Records matching either group will appear.

* * * * *

9\. Saving Filters
==================

### Steps

1.  Create conditions.
2.  Click **Save Filter**.
3.  Enter filter name.
4.  Choose visibility.

Example:

```
Only Me
```

1.  Save.

* * * * *

### Benefits

-   Reuse complex queries
-   Reduce repetitive work
-   Maintain consistency

* * * * *

10\. Loading Filters
====================

### Steps

1.  Open Condition Builder.
2.  Click **Load Filter**.
3.  Select saved filter.
4.  Query reloads automatically.

* * * * *

### Example

Saved filter returned:

```
13 Records
```

when reloaded.

* * * * *

11\. What are Breadcrumbs?
==========================

### Definition

Breadcrumbs display active query conditions at the top of list views.

Example:

```
Active = True >State = On Hold, Resolved >Impact ≠ Medium, Low
```

* * * * *

### Purpose

Provide a quick visual representation of active filters.

* * * * *

12\. Breadcrumb Structure
=========================

Example:

`Active = True\
>\
State = Resolved\
>\
Impact = High`

The greater-than sign represents:

```
AND
```

between conditions.

* * * * *

13\. Removing Conditions Using Breadcrumbs
==========================================

Instead of reopening the Condition Builder:

### Steps

1.  Locate breadcrumb condition.
2.  Click the **greater-than ( > )** symbol.

### Result

The selected condition is removed immediately.

* * * * *

### Benefit

Faster filter management.

* * * * *

14\. Breadcrumb Right-Click Options
===================================

Right-clicking a breadcrumb provides additional actions.

### Available Options

-   Copy URL
-   Copy Query

### Uses

-   Documentation
-   Sharing filters
-   Troubleshooting

* * * * *

15\. Quick Filtering with Show Matching
=======================================

### What is Show Matching?

Quickly creates a filter based on a field value.

### Example

Right-click:

```
Caller = Abel Tuter
```

Select:

```
Show Matching
```

Result:

Displays all incidents where:

```
Caller = Abel Tuter
```

* * * * *

16\. Quick Filtering with Filter Out
====================================

### What is Filter Out?

Excludes records matching a specific value.

### Example

Right-click:

```
Priority = Planning
```

Choose:

```
Filter Out
```

Result:

Removes all Planning priority records.

* * * * *

17\. Sorting Records
====================

Condition Builder also supports sorting.

### Example

Sort by:

```
Category
```

### Result

Records appear alphabetically.

* * * * *

Steps / Process
===============

Creating a Query
----------------

### Step 1

Open Incident List.

### Step 2

Click Filter Icon.

### Step 3

Select Field.

Example:

```
Active
```

### Step 4

Choose Operator.

Example:

```
is
```

### Step 5

Provide Value.

Example:

```
True
```

### Step 6

Add additional conditions if needed.

### Step 7

Run the query.

* * * * *

Saving a Filter
---------------

### Step 1

Create query.

### Step 2

Click Save Filter.

### Step 3

Enter name.

### Step 4

Choose visibility.

### Step 5

Save.

* * * * *

Using Show Matching
-------------------

### Step 1

Right-click field value.

### Step 2

Select:

```
Show Matching
```

### Step 3

ServiceNow automatically builds the filter.

* * * * *

Important Terms
===============

| Term | Meaning |
| --- | --- |
| **Condition Builder** | Tool used to create queries without SQL |
| **Breadcrumbs** | Visual representation of active filters |
| **Reference Field** | Field that points to a record in another table |
| **Boolean Field** | Field containing True/False values |
| **Choice Field** | Field containing predefined options |
| **Show Matching** | Filters records with the same field value |
| **Filter Out** | Excludes records with the selected value |
| **Load Filter** | Loads a saved query |
| **Save Filter** | Stores a query for future use |
| **Sort** | Orders records based on field values |

* * * * *

Commands / Syntax / Configuration
=================================

Basic Condition Format
----------------------

```
Field → Operator → Value
```

* * * * *

Example Query
-------------

`Active = True\
AND\
State IN (On Hold, Resolved)\
AND\
Impact NOT IN (Medium, Low)`

* * * * *

Reference Field Query
---------------------

```
Assigned To.Location = San Diego
```

* * * * *

OR Logic
--------

```
Group 1ORGroup 2
```

* * * * *

Breadcrumb Example
------------------

```
Active = True >State = Resolved >Impact = High
```

* * * * *

Examples
========

Example 1: Active High-Impact Incidents
---------------------------------------

Conditions:

```
Active = TrueState IN (On Hold, Resolved)Impact NOT IN (Medium, Low)
```

Result:

```
4 Records
```

* * * * *

Example 2: Assigned User Location
---------------------------------

Condition:

```
Assigned To → Location → San Diego
```

Result:

Only incidents assigned to users in San Diego.

* * * * *

Example 3: Show Matching
------------------------

Right-click:

```
Caller = Abel Tuter
```

Select:

```
Show Matching
```

Result:

Displays all incidents for that caller.

* * * * *

Example 4: Filter Out
---------------------

Right-click:

```
Priority = Planning
```

Select:

```
Filter Out
```

Result:

Removes Planning incidents from results.

* * * * *

Certification Focus
===================

Important Points for Exams
--------------------------

-   Condition Builder eliminates the need for SQL.
-   Query structure is **Field → Operator → Value**.
-   Breadcrumbs display active filters.
-   Reference fields can access related table data.
-   Filters can be saved and loaded.
-   AND and OR conditions are supported.
-   Show Matching creates quick filters.
-   Filter Out excludes matching records.
-   Breadcrumbs can remove conditions quickly.

* * * * *

Common Mistakes
---------------

❌ Confusing AND conditions with OR conditions.

❌ Forgetting that reference fields point to another table.

❌ Rebuilding filters instead of saving them.

❌ Opening Condition Builder when breadcrumbs can remove filters faster.

❌ Ignoring right-click shortcuts.

* * * * *

Things to Remember
------------------

✅ Condition Builder is one of the most powerful ServiceNow filtering tools.

✅ Reference fields allow filtering across tables.

✅ Breadcrumbs mirror active conditions.

✅ Saved filters save time.

✅ Show Matching creates filters quickly.

✅ Filter Out excludes unwanted records.

✅ Greater-than signs in breadcrumbs represent AND logic.

* * * * *

Real-World Application
======================

Service Desk teams frequently use Condition Builder to locate:

-   High-priority incidents
-   Unassigned tickets
-   Specific callers
-   Open changes
-   Active problems

Administrators use saved filters for:

-   Daily monitoring
-   Compliance reporting
-   Incident management dashboards

Developers and support teams use **reference field filtering** to find records based on related user, group, or configuration item information without writing database queries.

* * * * *

Quick Revision (30 sec)
=======================

-   **Condition Builder** creates queries without SQL.
-   Query format = **Field → Operator → Value**.
-   Supports **AND** and **OR** logic.
-   Reference fields access related tables.
-   **Breadcrumbs** show active filters.
-   Click breadcrumbs to remove conditions.
-   Right-click breadcrumbs to copy URL or query.
-   **Show Matching** finds similar records.
-   **Filter Out** excludes records.
-   Save filters for reuse