Lesson 10: UI Actions in ServiceNow
==================================

Lecture Summary
---------------

This lecture introduces **UI Actions**, a powerful ServiceNow customization used to create **buttons, links, and menu items** on forms and lists. Unlike many customizations, UI Actions can run on both the **client-side** and **server-side**. They are commonly used to perform actions such as resolving incidents, creating related records, launching integrations, or executing custom business logic through JavaScript.

* * * * *

Key Points
----------

-   **UI Actions** create buttons, links, and menu items.
-   Can run on:
    -   **Server-side**
    -   **Client-side**
-   Use **JavaScript** for custom logic.
-   Can appear in:
    -   Forms
    -   Lists
    -   Context Menus
    -   Related Links
-   Visibility can be controlled using:
    -   Conditions
    -   Roles
-   Common examples:
    -   Resolve Incident
    -   Create Problem
    -   Copy Change Request
    -   Reject Approval

* * * * *

Detailed Notes
==============

What are UI Actions?
--------------------

A **UI Action** is a customization that adds interactive elements to the user interface.

Examples:

-   Buttons
-   Links
-   Menu Items

These elements perform actions when clicked.

### Examples

#### Incident Form

Buttons:

-   Resolve
-   Delete
-   Update
-   Follow

#### Related Links

-   Show SLA Timeline
-   Repair SLAs

#### Context Menu

-   Copy Incident
-   Create Problem
-   Create Request
-   Create Child Incident

* * * * *

Client-Side vs Server-Side UI Actions
-------------------------------------

### Server-Side UI Actions

Execute on the ServiceNow server.

Used for:

-   Creating records
-   Updating records
-   Calling integrations
-   Running business logic

* * * * *

### Client-Side UI Actions

Execute inside the user's browser.

Used for:

-   Validations
-   Alert messages
-   User interaction
-   Checking form fields before submission

* * * * *

Why UI Actions Are Powerful
---------------------------

Most ServiceNow customizations run only on one side:

| Customization | Execution |
| --- | --- |
| UI Policy | Client |
| Client Script | Client |
| Business Rule | Server |
| UI Action | Client or Server |

UI Actions are unique because they can work in both environments.

* * * * *

Real-World Use Cases
--------------------

### Salesforce Integration

Button:

```
Create Salesforce Ticket
```

Action:

-   Sends Incident information
-   Calls Salesforce REST API
-   Creates a Salesforce case

* * * * *

### Approval Rejection

Button:

```
Reject
```

Action:

-   Changes approval state
-   Updates record status

* * * * *

### Incident Resolution

Button:

```
Resolve
```

Action:

-   Validates required fields
-   Changes incident state to Resolved

* * * * *

UI Action Form Fields
=====================

Basic Fields
------------

| Field | Purpose |
| --- | --- |
| Name | Label displayed to users |
| Table | Table where action applies |
| Active | Enable/Disable UI Action |
| Order | Display order |
| Action Name | Internal action identifier |

* * * * *

Display Options
---------------

A UI Action can appear as:

| Option | Description |
| --- | --- |
| Form Button | Button on form |
| Form Link | Link on form |
| Form Context Menu | Menu item |
| List Banner Button | Button on list |
| List Bottom Button | Button at bottom |
| List Context Menu | Menu option |
| List Link | Link in list |
| List Choice | Choice option |

* * * * *

Additional Fields
-----------------

| Field | Purpose |
| --- | --- |
| Condition | Controls visibility |
| Script | Code executed |
| Comments | Documentation |
| Hint | Tooltip text |

* * * * *

Steps / Process
===============

Navigation to UI Actions
------------------------

### From Form View

```
Form Context Menu→ Configure→ UI Actions
```

### From List View

```
List Context Menu→ Configure→ UI Actions
```

* * * * *

Viewing Existing UI Actions
---------------------------

Navigate to:

```
Incident Form→ Configure→ UI Actions
```

Examples shown:

-   Resolve
-   Create Problem
-   Follow
-   Delete

* * * * *

Understanding the Resolve UI Action
-----------------------------------

### Properties

| Property | Value |
| --- | --- |
| Client | True |
| Form Button | True |
| Show on Insert | Yes |
| Show on Update | Yes |

* * * * *

### Visibility Condition

User must:

```
Have ITIL roleORBe the Caller
```

Only then is the Resolve button displayed.

* * * * *

Creating a UI Action
====================

Goal
----

Create a button named:

```
Hello
```

When clicked:

```
Display "Hello World"
```

* * * * *

Step 1: Create New UI Action
----------------------------

Navigation:

```
Configure→ UI Actions→ New
```

* * * * *

Step 2: Configure Fields
------------------------

| Field | Value |
| --- | --- |
| Name | Hello |
| Active | True |
| Client | True |
| Form Button | True |
| Show on Insert | True |
| Show on Update | True |

* * * * *

Step 3: Define Function
-----------------------

### On Click

```
sayHello
```

### Script

```
function sayHello() {    alert("Hello World");}
```

* * * * *

Step 4: Save
------------

Click:

```
Submit
```

* * * * *

Step 5: Test
------------

Open an Incident.

Result:

A new button appears:

```
Hello
```

Clicking the button displays:

```
Hello World
```

* * * * *

Step 6: Disable UI Action
-------------------------

Uncheck:

```
Active
```

Click:

```
Update
```

Result:

The button disappears.

* * * * *

Important Terms
===============

| Term | Meaning |
| --- | --- |
| UI Action | Button, link, or menu item |
| Client-Side | Runs in browser |
| Server-Side | Runs on ServiceNow server |
| Form Button | Button displayed on form |
| Context Menu | Right-click menu item |
| Condition | Controls visibility |
| Active | Enables UI Action |
| Action Name | Internal identifier |
| OnClick | Client-side function executed |
| Script | JavaScript code |

* * * * *

Commands / Configuration
========================

Open UI Actions
---------------

```
Configure→ UI Actions
```

* * * * *

Create Client-Side UI Action
----------------------------

```
function sayHello() {    alert("Hello World");}
```

* * * * *

Typical Visibility Condition
----------------------------

```
gs.hasRole('itil')
```

Used to show UI Action only to ITIL users.

*(High-level understanding only for CSA exam.)*

* * * * *

Examples
========

Example 1: Resolve Incident
---------------------------

Button:

```
Resolve
```

Action:

-   Validate fields
-   Resolve incident

* * * * *

Example 2: Create Problem
-------------------------

Button:

```
Create Problem
```

Action:

-   Generate related problem record

* * * * *

Example 3: Salesforce Integration
---------------------------------

Button:

```
Create Salesforce Ticket
```

Action:

-   Send Incident data
-   Create Salesforce case

* * * * *

Example 4: Hello World
----------------------

Button:

```
Hello
```

Action:

```
alert("Hello World");
```

* * * * *

Certification Focus
===================

Important Exam Points
---------------------

### Remember

-   UI Actions create:
    -   Buttons
    -   Links
    -   Menu Items
-   Can run:
    -   Client-side
    -   Server-side
-   Use JavaScript.
-   Visibility controlled by:
    -   Conditions
    -   Roles
-   Can appear in forms and lists.

* * * * *

Common Mistakes
---------------

### Mistake 1

Thinking UI Actions only run server-side.

✅ Correct:

They can run client-side or server-side.

* * * * *

### Mistake 2

Confusing UI Actions with UI Policies.

✅ UI Policy:

Controls field behavior.

✅ UI Action:

Performs an action when clicked.

* * * * *

### Mistake 3

Forgetting to activate the UI Action.

✅ Active must be checked.

* * * * *

CSA Exam Questions Often Ask
----------------------------

-   What is a UI Action?
-   Where can UI Actions appear?
-   Client-side or server-side?
-   Difference between UI Actions and UI Policies?

* * * * *

Real-World Application
======================

Organizations use UI Actions to:

### Incident Management

-   Resolve incidents
-   Create problem records
-   Escalate tickets

### Change Management

-   Copy changes
-   Create standard templates

### Integrations

-   Create Salesforce tickets
-   Call REST APIs
-   Trigger external workflows

### Approval Processes

-   Approve
-   Reject
-   Cancel

UI Actions are one of the most frequently used customizations in ServiceNow.

* * * * *

Quick Revision (30 Seconds)
===========================

-   UI Actions create buttons, links, and menu items.
-   Can run on both client-side and server-side.
-   Use JavaScript.
-   Appear on forms, lists, and context menus.
-   Visibility controlled by conditions.
-   Roles can restrict access.
-   Resolve button is a UI Action.
-   Create Problem is a UI Action.
-   Client-side UI Actions use OnClick functions.
-   Active checkbox enables/disables the UI Action.