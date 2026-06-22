Lesson 7: UI Policies in ServiceNow
===================================

Lecture Summary
---------------

This lecture introduces **UI Policies**, one of the most common form customizations in ServiceNow. UI Policies allow administrators to dynamically control form behavior without writing code. They can make fields **mandatory**, **read-only**, or **hidden** based on conditions. UI Policies run on the **client-side** and help enforce business requirements while improving the user experience.

* * * * *

Key Points
----------

-   **UI Policies** control form behavior dynamically.
-   Run on the **client-side (browser)**.
-   Used to make fields:
    -   Mandatory
    -   Read-Only
    -   Hidden/Visible
-   Usually require **no scripting**.
-   Consist of:
    -   UI Policy
    -   UI Policy Actions
-   Can be enabled or disabled using the **Active** checkbox.
-   Conditions determine when the policy executes.

* * * * *

Detailed Notes
==============

What is a UI Policy?
--------------------

A **UI Policy** is a ServiceNow customization used to control how fields behave on a form.

Common uses:

-   Make a field required.
-   Make a field read-only.
-   Hide or show fields.
-   Change form behavior based on user input.

### Example

Requirement:

> If Incident State = Resolved, then Close Code must be mandatory.

Result:

-   User cannot save the record without selecting a Close Code.
-   ServiceNow displays an error message until the field is completed.

* * * * *

UI Policies Run on the Client-Side
----------------------------------

UI Policies execute in the user's browser.

### Flow

1.  User opens a form.
2.  ServiceNow sends UI Policy definitions to the browser.
3.  User changes a field value.
4.  UI Policy condition is evaluated.
5.  Actions are applied instantly.

### Benefits

-   Faster response.
-   No server call required.
-   Better user experience.

* * * * *

Common UI Policy Use Cases
--------------------------

### 1\. Make Field Mandatory

**Condition**

State = Resolved

**Action**

Close Code = Mandatory

* * * * *

### 2\. Make Field Read-Only

**Condition**

State = Closed

**Action**

Short Description = Read-Only

* * * * *

### 3\. Hide a Field

**Condition**

State = Open

**Action**

Resolution Notes = Hidden

* * * * *

UI Policy Components
--------------------

### UI Policy Record

Contains:

| Field | Purpose |
| --- | --- |
| Table | Table where policy applies |
| Active | Enables/Disables policy |
| Short Description | Description of policy |
| Conditions | Determines when policy runs |
| Order | Execution order |

* * * * *

### UI Policy Actions

UI Policy Actions define what happens to a field.

Available actions:

| Property | Purpose |
| --- | --- |
| Mandatory | Make field required |
| Visible | Show/Hide field |
| Read-only | Lock field editing |

Options:

-   Leave Alone
-   True
-   False

* * * * *

Example: Mandatory Fields for All Incidents
-------------------------------------------

Out-of-box UI Policy:

### Condition

No condition specified.

Meaning:

-   Always runs.

### Actions

| Field | Mandatory |
| --- | --- |
| Caller ID | True |
| Short Description | True |

Result:

These fields are always required.

* * * * *

Example: Read-Only on Closed Incidents
--------------------------------------

### Condition

State = Closed

OR

State = Canceled

### Actions

Multiple incident fields are set to:

**Read-Only = True**

Result:

Users cannot modify the incident after closure.

* * * * *

Steps / Process
===============

Navigation to View UI Policies
------------------------------

```
Incident Form→ Form Context Menu→ Configure→ UI Policies
```

* * * * *

Create a New UI Policy
----------------------

### Requirement

When Category = Database:

-   Hide Subcategory
-   Require Business Service

### Step 1: Open UI Policies

```
Incident Form→ Configure→ UI Policies→ New
```

* * * * *

### Step 2: Create Policy

Fill:

| Field | Value |
| --- | --- |
| Table | Incident |
| Short Description | Hide Subcategory, Require Business Service |
| Active | True |
| Order | 100 |
| Condition | Category = Database |

Save the record.

* * * * *

### Step 3: Create UI Policy Action #1

| Field | Value |
| --- | --- |
| Field Name | Subcategory |
| Visible | False |

Result:

Subcategory field disappears.

* * * * *

### Step 4: Create UI Policy Action #2

| Field | Value |
| --- | --- |
| Field Name | Business Service |
| Mandatory | True |

Result:

Business Service becomes required.

* * * * *

### Step 5: Test

Select:

```
Category = Database
```

Expected Result:

-   Subcategory hidden
-   Business Service required

Change Category:

```
Category = Network
```

Expected Result:

-   Subcategory visible again
-   Business Service no longer required

* * * * *

Important Terms
===============

| Term | Meaning |
| --- | --- |
| UI Policy | Controls form behavior without scripting |
| UI Policy Action | Defines field actions |
| Client-Side | Executes in browser |
| Mandatory | Field must contain a value |
| Read-Only | User cannot edit field |
| Visible | Controls field visibility |
| Condition | Determines when policy runs |
| Active | Enables/disables policy |
| Order | Determines execution sequence |

* * * * *

Commands / Configuration
========================

Access UI Policies
------------------

```
Form Context Menu→ Configure→ UI Policies
```

### Create UI Policy

```
New→ Select Table→ Define Condition→ Save→ Add UI Policy Actions
```

* * * * *

Advanced View
-------------

A UI Policy can be switched to **Advanced View**.

Additional feature:

-   Script section

Used for:

-   Complex logic
-   Advanced customization

**Exam Tip:** UI Policies generally do not require scripting.

* * * * *

Examples
========

Example 1
---------

### Condition

```
State = Closed
```

### Action

```
Short Description → Read Only
```

* * * * *

Example 2
---------

### Condition

```
Category = Database
```

### Actions

```
Subcategory → HiddenBusiness Service → Mandatory
```

* * * * *

Example 3
---------

### Condition

```
State = Resolved
```

### Action

```
Close Code → Mandatory
```

* * * * *

Certification Focus
===================

Important Exam Points
---------------------

### Remember

-   UI Policies run on the **Client-Side**.
-   Used for:
    -   Mandatory fields
    -   Read-only fields
    -   Hidden fields
-   Usually require **no scripting**.
-   Consist of:
    -   UI Policy
    -   UI Policy Actions

* * * * *

Common Mistakes
---------------

### Mistake 1

Thinking UI Policies run on the server.

✅ Correct:

UI Policies run in the browser.

* * * * *

### Mistake 2

Using Client Scripts when a UI Policy can solve the requirement.

✅ Prefer UI Policies first.

* * * * *

### Mistake 3

Creating a UI Policy but forgetting UI Policy Actions.

✅ Actions are required to affect fields.

* * * * *

CSA Exam Questions Often Ask
----------------------------

-   What is a UI Policy?
-   Client-side or server-side?
-   Difference between UI Policy and UI Policy Action.
-   When should UI Policies be used?

* * * * *

Real-World Application
======================

Organizations commonly use UI Policies for:

### Incident Management

-   Require Resolution Code when closing incidents.
-   Lock fields after closure.

### Change Management

-   Make Risk mandatory for high-risk changes.

### HR Applications

-   Show employee fields only for employee requests.

### Customer Service

-   Display additional fields depending on case type.

UI Policies help enforce business rules without writing code.

* * * * *

Quick Revision (30 Seconds)
===========================

-   UI Policies control form behavior.
-   Run on the **client-side**.
-   Used to make fields:
    -   Mandatory
    -   Read-only
    -   Hidden
-   UI Policies use conditions.
-   UI Policy Actions define field behavior.
-   No scripting required in most cases.
-   Active checkbox enables/disables policy.
-   Order controls execution sequence.
-   Common use case: require fields during record closure.
-   Preferred over scripting when possible.