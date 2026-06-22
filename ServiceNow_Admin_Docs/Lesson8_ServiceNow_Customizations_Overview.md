Lesson 8: ServiceNow Customizations Overview (Client-Side vs Server-Side)
=========================================================================

Lecture Summary
---------------

This lecture introduces the concept of **ServiceNow Customizations** and explains the important distinction between **Client-Side** and **Server-Side** processing. It provides a high-level overview of the major customization components available in ServiceNow, including **Client Scripts, Business Rules, Script Includes, UI Policies, UI Actions, and Data Policies**. Understanding where code executes and how data flows between the browser and ServiceNow servers is essential for both administrators and developers.

* * * * *

Key Points
----------

-   ServiceNow is highly customizable.
-   Customizations can run on either the **Client Side** or **Server Side**.
-   Client Side refers to the user's browser.
-   Server Side refers to ServiceNow application and database servers.
-   Data travels between client and server through requests and responses.
-   Six major customization types:
    -   Client Scripts
    -   Business Rules
    -   Script Includes
    -   UI Policies
    -   UI Actions
    -   Data Policies
-   ServiceNow allows creation of custom applications, tables, and pages.
-   Understanding client vs server processing is fundamental for CSA and development.

* * * * *

Detailed Notes
--------------

1\. Introduction to ServiceNow Customizations
=============================================

One of ServiceNow's greatest strengths is its flexibility.

Organizations can:

-   Modify existing applications
-   Create custom applications
-   Create custom tables
-   Build custom pages
-   Automate business processes
-   Extend platform functionality

ServiceNow provides multiple customization tools to accomplish these tasks.

* * * * *

2\. Client-Side vs Server-Side
==============================

This is one of the most important concepts in ServiceNow.

What is Client-Side?
--------------------

The **Client Side** refers to:

-   Web Browser
-   Laptop
-   Desktop
-   Mobile Device
-   Tablet

Examples:

```
Google ChromeMicrosoft EdgeFirefoxSafari
```

The browser displays information and interacts with users.

### Client-Side Characteristics

-   Runs in the browser
-   Faster user interaction
-   Limited access to database data
-   No direct database access
-   Used for form behavior and validation

* * * * *

What is Server-Side?
--------------------

The **Server Side** refers to ServiceNow Data Centers.

Includes:

```
Application ServersDatabase Servers
```

The server:

-   Stores records
-   Processes requests
-   Executes business logic
-   Returns data to users

### Server-Side Characteristics

-   Has access to all instance data
-   Can query databases
-   Executes business logic
-   Requires network communication

* * * * *

3\. How Data Flows in ServiceNow
================================

Whenever a user accesses data:

### Step 1

User opens a ServiceNow page.

```
Browser Request
```

↓

### Step 2

Request travels across the internet.

↓

### Step 3

Application Server receives request.

↓

### Step 4

Application Server queries Database Server.

↓

### Step 5

Database returns requested data.

↓

### Step 6

Application Server packages response.

↓

### Step 7

Response sent back to browser.

↓

### Step 8

Browser renders information on screen.

* * * * *

4\. Example: Viewing an Incident
================================

Suppose a user opens:

```
INC0010001
```

### What Happens?

Browser requests incident data.

ServiceNow server retrieves:

```
NumberPriorityCategoryStateDescriptionCaller
```

Server sends this information back.

Browser displays incident form.

### Important

The browser only receives data related to that incident.

If another incident is required:

```
New Request→ Server Processing→ New Response
```

must occur.

* * * * *

5\. Round-Trip Time (RTT)
=========================

Round-Trip Time is the amount of time required for:

```
Client → Server → Client
```

communication.

### Example

1.  Browser sends request.
2.  Request reaches ServiceNow data center.
3.  Server processes request.
4.  Server sends response.
5.  Browser receives response.

This total duration is called:

**Round-Trip Time (RTT)**

### Exam Tip

Network delays can occur even with fast internet because communication always requires RTT.

* * * * *

6\. ServiceNow Customization Components
=======================================

This course focuses on six major customization components.

* * * * *

A. Client Scripts
-----------------

### Purpose

Execute JavaScript on the browser.

### Common Uses

-   Validate fields
-   Show messages
-   Hide fields
-   Make fields mandatory

### Runs On

```
Client Side
```

* * * * *

B. Business Rules
-----------------

### Purpose

Execute logic when records are inserted, updated, deleted, or queried.

### Common Uses

-   Auto-populate fields
-   Create related records
-   Execute automation

### Runs On

```
Server Side
```

* * * * *

C. Script Includes
------------------

### Purpose

Reusable JavaScript classes and functions.

### Common Uses

-   Shared logic
-   Utility functions
-   Complex business processing

### Runs On

```
Server Side
```

* * * * *

D. UI Policies
--------------

### Purpose

Control form behavior without scripting.

### Common Uses

-   Mandatory fields
-   Read-only fields
-   Hide fields

### Runs On

```
Client Side
```

* * * * *

E. UI Actions
-------------

### Purpose

Create buttons, links, and context menu actions.

### Examples

```
Resolve IncidentClose ProblemApprove Request
```

### Runs On

```
Client or Server
```

Depending on configuration.

* * * * *

F. Data Policies
----------------

### Purpose

Enforce data consistency.

### Common Uses

-   Mandatory fields
-   Data validation

### Runs On

```
Server Side
```

Can also affect client behavior.

* * * * *

7\. Why Customizations Matter
=============================

Organizations rarely use ServiceNow exactly as delivered.

Customizations help:

-   Automate business processes
-   Improve user experience
-   Reduce manual work
-   Enforce standards
-   Increase productivity

Examples:

```
Auto-assign incidentsAuto-close ticketsValidate user inputGenerate approvalsSend notifications
```

* * * * *

Steps / Process
---------------

### ServiceNow Request Processing Flow

```
1\. User opens ServiceNow page2\. Browser sends request3\. Request reaches ServiceNow server4\. Application server processes request5\. Database server retrieves data6\. Application server builds response7\. Response returns to browser8\. Browser displays information
```

* * * * *

Important Terms
---------------

| Term | Meaning |
| --- | --- |
| Client Side | User browser where UI is displayed |
| Server Side | ServiceNow application and database servers |
| Request | Browser asking server for data |
| Response | Server returning requested data |
| RTT | Round-Trip Time between client and server |
| Customization | Modifying platform behavior |
| Client Script | Browser-side JavaScript |
| Business Rule | Server-side automation |
| Script Include | Reusable server-side code |
| UI Policy | No-code field behavior control |
| UI Action | Button, link, or action |
| Data Policy | Data validation and enforcement |

* * * * *

Commands / Configuration
------------------------

### Common Customization Navigation

#### Client Scripts

```
System Definition→ Client Scripts
```

#### Business Rules

```
System Definition→ Business Rules
```

#### Script Includes

```
System Definition→ Script Includes
```

#### UI Policies

```
System UI→ UI Policies
```

#### UI Actions

```
System Definition→ UI Actions
```

#### Data Policies

```
System Policy→ Data Policies
```

* * * * *

Examples
--------

### Example 1: Client Script

When Category = Hardware

```
Show Assignment Group field
```

Runs immediately in browser.

* * * * *

### Example 2: Business Rule

When Incident is created

```
Automatically assign to Service Desk
```

Runs on server.

* * * * *

### Example 3: UI Policy

Priority = Critical

```
Make Impact Mandatory
```

No scripting required.

* * * * *

Certification Focus
-------------------

### Important for CSA Exam

✔ Understand Client Side vs Server Side

✔ Browser = Client Side

✔ ServiceNow Data Center = Server Side

✔ Business Rules run on Server

✔ Client Scripts run on Client

✔ UI Policies require no scripting

✔ RTT refers to network communication delay

✔ ServiceNow is highly customizable

### Common Mistakes

❌ Confusing Client Scripts with Business Rules

❌ Assuming browser has access to all database records

❌ Forgetting server-side processing requires network communication

❌ Thinking UI Policies require JavaScript

* * * * *

Real-World Application
----------------------

Organizations commonly use customizations to:

-   Auto-assign incidents
-   Validate forms
-   Create approval workflows
-   Hide unnecessary fields
-   Create custom applications
-   Integrate external systems
-   Enforce business rules

Example:

```
Employee submits laptop request↓Business Rule creates approval↓Manager approves↓Task assigned to IT Team↓Notification sent automatically
```

* * * * *

Quick Revision (30 Seconds)
---------------------------

-   Client Side = Browser
-   Server Side = ServiceNow Data Center
-   Data moves through Requests and Responses
-   RTT = Client → Server → Client time
-   Client Scripts run in browser
-   Business Rules run on server
-   Script Includes provide reusable code
-   UI Policies control forms without scripting
-   UI Actions create buttons and actions
-   Data Policies enforce data consistency