Lesson 9: Client Scripts in ServiceNow
======================================

Overview
--------

Client Scripts are client-side JavaScript customizations in ServiceNow. They execute in the user's browser and are used to control form behavior, validate user input, display messages, and dynamically modify fields without requiring a server call.

Unlike Business Rules, which run on the server, Client Scripts execute directly in the browser, providing a faster and more interactive user experience.

* * * * *

Learning Objectives
-------------------

By the end of this lesson, you will be able to:

-   Understand what Client Scripts are.
-   Differentiate between Client Scripts and Business Rules.
-   Identify the four Client Script types.
-   Configure and create Client Scripts.
-   Use Client Scripts to control form behavior.
-   Understand the g_form API.
-   Create and test a simple Client Script.

* * * * *

What are Client Scripts?
========================

Client Scripts are JavaScript programs that run on the client-side (browser).

They execute when users interact with forms or list records and are commonly used to:

-   Validate form data
-   Display messages
-   Show or hide fields
-   Set field values
-   Make fields mandatory
-   Improve user experience

### Examples

-   Display a warning message when Priority is set to High.
-   Highlight VIP callers.
-   Automatically populate field values.
-   Validate data before saving.

* * * * *

Client-Side vs Server-Side
==========================

| Client Scripts | Business Rules |
| Run in Browser | Run on Server |
| Faster Execution | Requires Server Processing |
| Form Interaction | Database Operations |
| Uses g_form API | Uses GlideRecord API |
| No Direct Database Access | Full Database Access |

### Simple Explanation

Client Script = Controls the Form

Business Rule = Controls the Database

* * * * *

Client Script Types
===================

ServiceNow provides four Client Script types.

1\. OnLoad
----------

Runs when a form loads.

### Trigger

```
User Opens Record
↓
Form Loads
↓
OnLoad Script Executes
```

### Example

Highlight VIP callers when the form opens.

* * * * *

2\. OnChange
------------

Runs whenever a field value changes.

### Trigger

```
User Changes Field
↓
OnChange Script Executes
```

### Example

Display a message when State changes.

* * * * *

3\. OnSubmit
------------

Runs when the user saves or submits the form.

### Trigger

```
User Clicks Save
↓
OnSubmit Executes
↓
Form Saves
```

### Example

Prevent save if mandatory information is missing.

* * * * *

4\. OnCellEdit
--------------

Runs when a field is edited directly from a list view.

### Trigger

```
List View
↓
User Edits Cell
↓
OnCellEdit Executes
```

### Example

Validate Priority changes in a list.

* * * * *

Understanding g_form
====================

ServiceNow provides the g_form API for Client Scripts.

The g_form object allows scripts to interact with fields on a form.

### Common Methods

#### Get Field Value

```
var state = g_form.getValue('state');
```

#### Set Field Value

```
g_form.setValue('priority', '1');
```

#### Show Message

```
g_form.addInfoMessage('Record Updated');
```

#### Make Field Mandatory

```
g_form.setMandatory('short_description', true);
```

#### Hide Field

```
g_form.setVisible('subcategory', false);
```

#### Make Field Read-Only

```
g_form.setReadOnly('priority', true);
```

* * * * *

Client Script Form Fields
=========================

Name
----

Name of the Client Script.

Example:

```
Notify Conflict
```

* * * * *

Table
-----

Table where the Client Script runs.

Example:

```
Change Request
```

* * * * *

UI Type
-------

Determines where the script runs.

### Desktop

Runs in browser interface only.

### Mobile / Service Portal

Runs in Service Portal and Mobile.

### All

Runs everywhere.

Recommended option:

```
All
```

* * * * *

Type
----

Specifies the trigger.

Options:

-   OnLoad
-   OnChange
-   OnSubmit
-   OnCellEdit

* * * * *

Field Name
----------

Only visible for OnChange scripts.

Specifies which field triggers the script.

Example:

```
State
```

* * * * *

Active
------

Determines whether the script is enabled.

```
True = Enabled
False = Disabled
```

* * * * *

Real-Time Examples
==================

Example 1: VIP Caller Highlight
-------------------------------

Requirement:

When form loads and Caller is VIP:

```
Highlight Caller Field
```

Type:

```
OnLoad
```

* * * * *

Example 2: State Change Message
-------------------------------

Requirement:

When State changes from New to Authorize:

```
Display Message
```

Type:

```
OnChange
```

* * * * *

Example 3: Save Validation
--------------------------

Requirement:

Prevent save if Description is empty.

Type:

```
OnSubmit
```

* * * * *

GlideAjax and Client Scripts
============================

Client Scripts cannot directly access database data.

To retrieve server-side information, they can call:

```
GlideAjax
```

GlideAjax allows Client Scripts to communicate with Script Includes on the server.

Flow:

```
Client Script
↓
GlideAjax
↓
Script Include
↓
Server Response
↓
Browser
```

* * * * *

Creating a Client Script
========================

Requirement
-----------

When State changes to "Authorize", display:

```
Hello World
```

* * * * *

Step 1
------

Navigate to:

```
Change → All
```

Open any Change Request.

* * * * *

Step 2
------

Navigate to:

```
Form Context Menu
→ Configure
→ Client Scripts
```

* * * * *

Step 3
------

Click New

* * * * *

Step 4
------

Configure

```
Name: Say Hello

Table: Change Request

UI Type: All

Type: OnChange

Field Name: State
```

* * * * *

Step 5
------

Script

```
function onChange(control, oldValue, newValue, isLoading) {

    if (isLoading) {
        return;
    }

    alert("Hello World");

}
```

* * * * *

Step 6
------

Submit

* * * * *

Testing the Client Script
=========================

### Current State

```
New
```

### Change To

```
Authorize
```

### Result

```
Hello World
```

Popup appears immediately.

* * * * *

Deactivating a Client Script
============================

Navigation:

```
System Definition
→ Client Scripts
```

Steps:

1.  Open Client Script
2.  Uncheck Active
3.  Click Update

Result:

```
Client Script Disabled
```

* * * * *

Business Rules vs Client Scripts
================================

| Feature | Business Rule | Client Script |
| Runs On | Server | Browser |
| Language | JavaScript | JavaScript |
| Database Access | Yes | No |
| Form Control | Limited | Excellent |
| Performance | Slower | Faster |
| User Interaction | No | Yes |

* * * * *

Key Exam Points
===============

✅ Client Scripts run on the Client Side

✅ Written using JavaScript

✅ Used primarily for Form Behavior

✅ Four Types:

-   OnLoad
-   OnChange
-   OnSubmit
-   OnCellEdit

✅ Use g_form API

✅ Can call Script Includes using GlideAjax

✅ Do not directly access the database

✅ Improve User Experience

* * * * *

Simple Definition
-----------------

**Client Scripts are client-side JavaScript programs that execute in the user's browser to control form behavior, validate input, and improve user interaction within ServiceNow.**