**Filters & Search in ServiceNow**
==================================

Lecture Summary
---------------

This lecture introduces **Filters and Search functionality** in ServiceNow. It explains the various search locations available throughout the platform, including Global Search and List Search. The lecture focuses on **search wildcards**, which allow users to perform powerful searches such as contains, does not contain, equals, starts with, and ends with. Understanding these search techniques is essential for efficiently locating records within ServiceNow.

* * * * *

Key Points
==========

-   ServiceNow provides multiple search options throughout the platform.
-   Common search locations include **Global Search** and **List Search**.
-   Search wildcards enhance search capabilities.
-   Different wildcards perform different matching operations.
-   Global Search performs searches across multiple tables.
-   List Search allows searching within a specific table.
-   Exact match and partial match searches behave differently.
-   Understanding search syntax improves productivity and troubleshooting.

* * * * *

Detailed Notes
==============

1\. Introduction to Search in ServiceNow
----------------------------------------

Searching is one of the most frequently used functions in ServiceNow.

Users often need to find:

-   Incidents
-   Problems
-   Change Requests
-   Users
-   Configuration Items
-   Knowledge Articles

ServiceNow provides multiple search mechanisms to locate records quickly.

* * * * *

2\. Search Locations in ServiceNow
==================================

There are several search bars throughout the platform.

Although they look different, they generally perform similar functions.

### Common Search Areas

#### Global Search

Located in the platform banner.

Purpose:

-   Searches across multiple tables simultaneously.

* * * * *

#### List Search

Located at the top of a list view.

Purpose:

-   Searches records within a specific table.

Example:

```
Incident List
```

Searches only incident records.

* * * * *

#### Column Search

Located directly beneath list columns.

Purpose:

-   Searches a specific field/column.

Example:

```
Short Description
```

Only searches the Short Description field.

* * * * *

#### Condition Builder

Another search method available within lists.

Used for:

-   Advanced filtering
-   Multiple conditions
-   Complex searches

(Discussed in a later lecture.)

* * * * *

3\. Searching for Specific Records
==================================

Suppose you know an incident number.

Example:

```
INC0010001
```

You can search using:

### Option 1

Global Search

### Option 2

List Search

### Option 3

Condition Builder

### Option 4

Column Search (if Number field is displayed)

* * * * *

4\. Search Wildcards
====================

What are Search Wildcards?
--------------------------

Wildcards are special characters that modify how searches behave.

They allow:

-   Partial matches
-   Pattern matching
-   Exclusions
-   Flexible searching

Wildcards make searches significantly more powerful.

* * * * *

5\. Contains Wildcard (*)
=========================

### Syntax

```
*searchterm
```

### Meaning

Returns records where the value contains the search term anywhere in the field.

### Example

```
*Mark
```

Matches:

`Mark\
Trademark\
Marketing\
John Mark Smith`

### Why?

Because "Mark" appears somewhere within the text.

* * * * *

Contains Example
----------------

Search:

```
*sap
```

Results:

```
SAP Server FailureIssue with SAP LoginRestart SAP Service
```

The term can appear anywhere.

* * * * *

6\. Does Not Contain Wildcard (!*)
==================================

### Syntax

```
!*searchterm
```

### Meaning

Returns records where the value does NOT contain the search term.

### Example

```
!*Mark
```

Returns:

```
John DoeMichael SmithJane Miller
```

Excludes:

```
MarkTrademarkMark Johnson
```

* * * * *

Demo Example
------------

Before search:

```
Incident 44 contains SAP
```

Search:

```
!*sap
```

Result:

```
Incident 44 disappears
```

Because SAP exists within that record.

* * * * *

7\. Equals Wildcard (=)
=======================

### Syntax

```
=searchterm
```

### Meaning

Performs an exact match.

The field value must match exactly.

* * * * *

### Example

Search:

```
=Miller
```

Matches:

```
Miller
```

Does NOT Match:

```
John MillerMiller123
```

* * * * *

Demo Example
------------

Search:

```
=sap
```

Result:

```
No records found
```

Reason:

No short description equals exactly "sap".

* * * * *

### Actual Match Example

Search:

```
=can'treademail
```

Result:

```
Single matching incident
```

Because the value matched exactly.

* * * * *

8\. Does Not Equal Wildcard (!=)
================================

### Syntax

```
!=searchterm
```

### Meaning

Returns all records except exact matches.

### Example

Search:

```
!=Miller
```

Returns:

```
JohnSmithBrown
```

Excludes:

```
Miller
```

* * * * *

9\. Starts With Wildcard (%)
============================

### Syntax

```
searchterm%
```

### Meaning

Find records beginning with the specified value.

### Example

Search:

```
Hello%
```

Matches:

```
Hello WorldHello UserHello123
```

Does NOT Match:

```
Say HelloWorld Hello
```

* * * * *

Demo Example
------------

Search:

```
sap%
```

Results:

```
SAP Login IssueSAP Upgrade FailureSAP Connection Error
```

All begin with SAP.

* * * * *

10\. Ends With Wildcard (%)
===========================

### Syntax

```
%searchterm
```

### Meaning

Find records ending with the specified value.

### Example

Search:

```
%password
```

Matches:

```
Reset passwordForgot passwordChange password
```

Does NOT Match:

```
Password reset requiredPassword issue
```

* * * * *

Demo Example
------------

Search:

```
%password
```

Result:

Three incidents ending with "password".

* * * * *

11\. Global Search Demonstration
================================

### Search Term

```
sap
```

### What Happens?

ServiceNow searches multiple tables.

Examples:

-   Incidents
-   Problems
-   Change Requests

* * * * *

### Results Page Displays

| Table | Matches |
| --- | --- |
| Incidents | 6 |
| Change Requests | 7 |
| Problems | 1 |

* * * * *

### Observation

The term SAP was found in fields such as:

-   Configuration Item
-   Implementation Plan
-   Short Description

This confirms Global Search behaves similarly to a **Contains Search**.

* * * * *

12\. List Search Demonstration
==============================

### Navigate To

```
Incident → All
```

### Search Using Number Field

Search:

```
INC0010001
```

### Result

Returns one matching incident.

### Important Observation

Number searches use:

```
Exact Match
```

Not Contains.

* * * * *

Search Wildcard Reference Table
===============================

| Wildcard | Meaning | Example |
| --- | --- | --- |
| *term | Contains | *sap |
| !*term | Does Not Contain | !*sap |
| =term | Equals | =Miller |
| !=term | Does Not Equal | !=Miller |
| term% | Starts With | sap% |
| %term | Ends With | %password |

* * * * *

Steps / Process
===============

Finding an Incident Using List Search
-------------------------------------

### Step 1

Open:

```
Incident → All
```

### Step 2

Select Number field.

### Step 3

Enter incident number.

Example:

```
INC0010001
```

### Step 4

Press Enter.

### Step 5

View matching record.

* * * * *

Using Wildcards
---------------

### Step 1

Locate a searchable column.

Example:

```
Short Description
```

### Step 2

Enter wildcard syntax.

Examples:

`*sap\
!*sap\
=sap\
sap%\
%password`

### Step 3

Press Enter.

### Step 4

Review matching records.

* * * * *

Important Terms
===============

| Term | Meaning |
| --- | --- |
| **Global Search** | Searches multiple tables simultaneously |
| **List Search** | Searches records within a specific table |
| **Column Search** | Searches a specific field in a list |
| **Condition Builder** | Advanced filtering tool |
| **Wildcard** | Special search character used for pattern matching |
| **Contains** | Finds values containing text anywhere |
| **Equals** | Exact value matching |
| **Starts With** | Finds values beginning with text |
| **Ends With** | Finds values ending with text |

* * * * *

Commands / Syntax / Configuration
=================================

Contains
--------

```
*sap
```

* * * * *

Does Not Contain
----------------

```
!*sap
```

* * * * *

Equals
------

```
=sap
```

* * * * *

Does Not Equal
--------------

```
!=sap
```

* * * * *

Starts With
-----------

```
sap%
```

* * * * *

Ends With
---------

```
%password
```

* * * * *

Examples
========

Example 1: Contains Search
--------------------------

Search:

```
*sap
```

Results:

```
SAP Login IssueUnable to Access SAPRestart SAP Service
```

* * * * *

Example 2: Exact Match
----------------------

Search:

```
=can'treademail
```

Result:

```
Single matching incident
```

* * * * *

Example 3: Starts With
----------------------

Search:

```
sap%
```

Results:

```
SAP UpgradeSAP Login FailureSAP Configuration Error
```

* * * * *

Example 4: Ends With
--------------------

Search:

```
%password
```

Results:

```
Reset passwordForgot passwordChange password
```

* * * * *

Certification Focus
===================

Important Points for Exams
--------------------------

-   Know the difference between **Global Search** and **List Search**.
-   Understand wildcard syntax.
-   Global Search searches multiple tables.
-   List Search searches a specific table.
-   `*` means Contains.
-   `!*` means Does Not Contain.
-   `=` means Exact Match.
-   `!=` means Does Not Equal.
-   `%` placement determines Starts With or Ends With.

* * * * *

Common Mistakes
---------------

❌ Assuming Global Search only searches one table.

❌ Using `=` when a partial match is needed.

❌ Confusing Starts With and Ends With syntax.

❌ Forgetting that Number field searches are exact matches.

❌ Using incorrect wildcard placement.

* * * * *

Things to Remember
------------------

✅ Global Search searches across tables.

✅ List Search searches within one table.

✅ `*term` = Contains.

✅ `!*term` = Does Not Contain.

✅ `=term` = Exact Match.

✅ `!=term` = Not Equal.

✅ `term%` = Starts With.

✅ `%term` = Ends With.

* * * * *

Real-World Application
======================

Service Desk analysts use search functionality constantly.

Examples:

### Incident Investigation

Search:

```
*sap
```

Finds all SAP-related incidents.

* * * * *

### Password Issues

Search:

```
%password
```

Finds incidents ending with password-related descriptions.

* * * * *

### Exact Ticket Lookup

Search:

```
INC0012456
```

Returns a specific incident immediately.

Efficient searching helps administrators, developers, and support teams quickly locate records and troubleshoot issues.

* * * * *

Quick Revision (30 sec)
=======================

-   ServiceNow has **Global Search** and **List Search**.
-   Global Search searches multiple tables.
-   List Search searches a single table.
-   `*term` = Contains.
-   `!*term` = Does Not Contain.
-   `=term` = Exact Match.
-   `!=term` = Not Equal.
-   `term%` = Starts With.
-   `%term` = Ends With.
-   Wildcards make searching faster and more powerful.