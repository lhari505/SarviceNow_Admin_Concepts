Business Rules in ServiceNow
============================

Overview
--------

Business Rules are one of the most commonly used customizations in ServiceNow.

They execute server-side JavaScript whenever specific database operations occur on a table.

Business Rules help automate tasks, enforce business logic, maintain data consistency, and perform actions automatically when records are created, updated, deleted, or queried.

* * * * *

What are Business Rules?
------------------------

A Business Rule is a server-side script that runs when a record is:

-   Inserted (Created)
-   Updated (Modified)
-   Deleted
-   Queried

Business Rules are attached to specific tables.

### Example

Incident Table → Business Rule

When an incident is updated:

-   Change state automatically
-   Increment counters
-   Clear fields
-   Create related records

* * * * *

Why Use Business Rules?
-----------------------

Business Rules help:

-   Automate repetitive tasks
-   Enforce business logic
-   Maintain data integrity
-   Update related records
-   Prevent invalid data

### Real-Time Example

When an Incident is reopened:

-   Clear Resolution Code
-   Clear Resolution Notes
-   Increment Reopen Count

This can be done automatically using a Business Rule.

* * * * *

Client-Side vs Server-Side
==========================

Client-Side
-----------

Runs in the user's browser.

Examples:

-   UI Policies
-   Client Scripts

### Characteristics

-   Fast execution
-   No database access
-   Used for form behavior

* * * * *

Server-Side
-----------

Runs on ServiceNow servers.

Examples:

-   Business Rules
-   Script Includes
-   Scheduled Jobs

### Characteristics

-   Has database access
-   Can modify records
-   Executes business logic

* * * * *

Business Rule Execution Timing
------------------------------

Business Rules can execute at different stages.

### Before

Runs before data is saved.

Used for:

-   Validation
-   Modifying values

Example:

```
State = NewBefore save → Change State to In Progress
```

* * * * *

### After

Runs after data is saved.

Used for:

-   Notifications
-   Creating related records

Example:

```
Create a task after an incident is created
```

* * * * *

### Async (Asynchronous)

Runs in the background after the record is saved.

Used for:

-   Integrations
-   Heavy processing

Example:

```
Send data to Salesforce
```

* * * * *

### Display

Runs before the form is displayed to the user.

Used for:

-   Preparing form data
-   Sending values to Client Scripts

* * * * *

Database Operations
===================

Business Rules can run on:

Insert
------

Runs when a new record is created.

Example:

```
Create a CI record when a new asset is created.
```

* * * * *

Update
------

Runs when an existing record changes.

Example:

```
Increment Reopen Count when incident is reopened.
```

* * * * *

Delete
------

Runs when a record is deleted.

Example:

```
Log deletion information.
```

* * * * *

Query
-----

Runs whenever records are queried.

Example:

```
Restrict records returned to users.
```

* * * * *

Business Rule Processing Flow
=============================

Viewing a Record
----------------

```
User Opens Incident        ↓Application Server        ↓Database Query        ↓Display Business Rule Executes        ↓Data Sent to Browser
```

* * * * *

Updating a Record
-----------------

```
User Updates Incident        ↓Before Business Rule Executes        ↓Database Update        ↓After Business Rule Executes        ↓Response Sent to Browser
```

* * * * *

Business Rule Form Fields
=========================

Name
----

Unique name of the Business Rule.

Example:

```
Set State To In Progress
```

* * * * *

Table
-----

Specifies the table where the Business Rule executes.

Example:

```
Incident
```

* * * * *

Active
------

Determines whether the Business Rule is active.

```
True = EnabledFalse = Disabled
```

* * * * *

Advanced
--------

Enables scripting and advanced configuration.

When checked:

-   Script field appears
-   Before/After options appear
-   Query/Delete options appear

* * * * *

When to Run Section
===================

### Insert

Execute when records are created.

### Update

Execute when records are modified.

### Delete

Execute when records are removed.

### Query

Execute during database queries.

### Condition

Determines when the rule should execute.

Example:

```
State is New
```

* * * * *

Business Rule Actions
=====================

Without scripting, Business Rules can simply set field values.

Example:

```
State = ClosedPriority = High
```

This method is simple but limited.

* * * * *

Real-Time Examples
==================

Example 1: Reopen Count
-----------------------

Requirement:

Whenever an incident is reopened:

```
Reopen Count = Reopen Count + 1
```

Business Rule:

```
Table: IncidentWhen: Before UpdateCondition: Incident ReopenedAction: Increment Reopen Count
```

* * * * *

Example 2: Clear Resolution Fields
----------------------------------

Requirement:

When incident is reopened:

```
Clear Resolution CodeClear Resolution NotesClear Resolved By
```

Business Rule automatically resets these fields.

* * * * *

Creating a Custom Business Rule
===============================

Requirement
-----------

When an Incident State is "New" and the record is updated:

Automatically change State to "In Progress".

* * * * *

Steps
-----

### Step 1

Open Incident Form

```
Incident → Open Record
```

### Step 2

Open Business Rules

```
Form Context Menu→ Configure→ Business Rules
```

### Step 3

Click New

### Step 4

Configure

```
Name: Set State To In ProgressTable: IncidentUpdate: CheckedCondition:State is New
```

### Step 5

Action

```
Set State = In Progress
```

### Step 6

Submit

* * * * *

Testing the Business Rule
=========================

### Scenario 1

Record State = New

Modify any field

Click Save

Result:

```
State changes to In Progress
```

* * * * *

### Scenario 2

Create a brand new Incident

Result:

```
Business Rule does NOT run
```

Reason:

```
Rule is configured for UpdateNot Insert
```

* * * * *

Deactivating a Business Rule
============================

Navigation:

```
System Definition→ Business Rules
```

Steps:

1.  Open Business Rule
2.  Uncheck Active
3.  Click Update

Result:

```
Business Rule becomes inactive.
```

* * * * *

Key Exam Points
===============

✅ Business Rules run on the Server Side

✅ Business Rules use JavaScript

✅ Business Rules execute on specific tables

✅ Can run Before, After, Async, or Display

✅ Can run on Insert, Update, Delete, or Query

✅ Used to automate database operations

✅ Advanced Business Rules support scripting

✅ One of the most important ServiceNow customizations for CSA and Administrator roles

### Simple Definition

> **Business Rules are server-side automation scripts that execute during database operations to enforce business logic and automate record processing in ServiceNow.**