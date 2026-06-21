**Lecture Notes: ServiceNow Overview, Architecture, Environments, Release Cycle & User Interface**
==================================================================================================

Lecture Summary
---------------

This lecture provides a foundational overview of **ServiceNow**, including its SaaS architecture, history, ecosystem, technology stack, release cycle, environments, and user interface. ServiceNow began as an **IT Service Management (ITSM)** platform but has evolved into a comprehensive enterprise workflow platform supporting multiple business functions. Understanding these core concepts is essential for both ServiceNow Administrators and Developers.

* * * * *

Key Points
==========

-   **ServiceNow** is a **Software as a Service (SaaS)** platform.
-   Customers access ServiceNow through a web browser.
-   ServiceNow is hosted in ServiceNow-managed data centers.
-   Originally focused on **ITSM (IT Service Management)**.
-   Supports many business functions beyond ITSM.
-   Built using Java technologies and a MySQL database.
-   New releases occur approximately every **6--8 months**.
-   Organizations typically have **Development**, **Test**, and **Production** environments.
-   Regular cloning keeps environments synchronized.
-   The UI consists of the **Banner**, **Application Navigator**, and **Main Content Frame**.

* * * * *

Detailed Notes
==============

1\. What is ServiceNow?
=======================

Definition
----------

**ServiceNow** is a cloud-based Software as a Service (SaaS) platform that organizations use to automate business processes and workflows.

### SaaS Model

Unlike traditional software:

❌ No local installation

❌ No server maintenance

❌ No infrastructure management

✅ Access through a browser

✅ Subscription-based licensing

✅ Hosted by ServiceNow

* * * * *

How ServiceNow Works
--------------------

```
Organization
      ↓
Subscription License
      ↓
ServiceNow Platform
      ↓
Access via Browser
      ↓
ServiceNow Data Centers
```

All applications, databases, and configurations are hosted in ServiceNow-managed data centers.

* * * * *

2\. History of ServiceNow
=========================

ServiceNow Origins
------------------

ServiceNow initially focused on:

### IT Service Management (ITSM)

ITSM applications include:

-   Incident Management
-   Problem Management
-   Change Management

* * * * *

Most Popular Application
------------------------

### Incident Management

An incident represents a disruption or issue affecting a service.

### Real-World Examples

-   Internet service outage
-   Email access issue
-   VPN connection problem
-   Mobile service interruption

When users report these issues, support teams often create an incident record in ServiceNow.

* * * * *

Growth Beyond ITSM
------------------

ServiceNow has expanded significantly beyond traditional IT operations.

Today, ServiceNow supports many business functions across organizations.

* * * * *

3\. ServiceNow Ecosystem
========================

ServiceNow provides solutions across multiple business areas.

* * * * *

IT Service Management (ITSM)
----------------------------

Core applications:

-   Incident
-   Problem
-   Change
-   Request Management

* * * * *

IT Operations Management (ITOM)
-------------------------------

Focuses on:

-   Infrastructure monitoring
-   Discovery
-   Event Management

* * * * *

IT Business Management (ITBM)
-----------------------------

Supports:

-   Project Management
-   Portfolio Management
-   Resource Planning

* * * * *

IT Asset Management (ITAM)
--------------------------

Tracks organizational assets.

Examples:

### Hardware Assets

-   Laptops
-   Servers
-   Mobile Devices

### Software Assets

-   Microsoft Office
-   Adobe Licenses
-   Operating Systems

* * * * *

DevOps
------

Supports:

-   CI/CD integration
-   Agile development
-   Deployment automation

* * * * *

Security Operations
-------------------

Provides:

-   Security incident management
-   Vulnerability response

* * * * *

HR Service Delivery
-------------------

Supports:

-   Employee onboarding
-   HR requests
-   Employee case management

* * * * *

Customer Service Management (CSM)
---------------------------------

Supports customer-facing service operations.

* * * * *

Governance, Risk & Compliance (GRC)
-----------------------------------

Helps organizations:

-   Manage risk
-   Ensure compliance
-   Track audits

* * * * *

4\. Custom Application Development
==================================

One of ServiceNow's most powerful capabilities is:

Application Development on the Now Platform
-------------------------------------------

Organizations can build custom applications without creating everything from scratch.

* * * * *

### Available Components

#### Business Rules

Automate backend processing.

#### Workflows

Automate approval processes and business logic.

#### Forms

Capture user input.

#### Tables

Store business data.

* * * * *

### Example

A company could create:

```
Employee Travel Request Application
```

using:

-   Forms
-   Workflows
-   Business Rules
-   Notifications

without building an entirely new platform.

* * * * *

5\. ServiceNow Technology Stack
===============================

Purpose
-------

Understanding the stack helps developers understand how ServiceNow works behind the scenes.

* * * * *

Java-Based Platform
-------------------

ServiceNow is primarily built using Java technologies.

* * * * *

Apache Tomcat
-------------

### Role

Web Server

Handles:

-   User requests
-   Application hosting

* * * * *

J2EE Application Server
-----------------------

### Role

Executes business logic and platform services.

* * * * *

MySQL Database
--------------

### Role

Stores:

-   Records
-   Tables
-   Configurations
-   User data

* * * * *

Mozilla Rhino
-------------

### Definition

A JavaScript engine written in Java.

### Purpose

Allows JavaScript execution within the Java environment.

* * * * *

### Example

A Business Rule written in JavaScript:

```
current.priority = 1;
```

is executed through Mozilla Rhino.

* * * * *

ServiceNow Stack Diagram
========================

```
Browser
   ↓
Apache Tomcat
   ↓
J2EE Application Server
   ↓
Mozilla Rhino
   ↓
MySQL Database
```

* * * * *

6\. ServiceNow Release Cycle
============================

ServiceNow continuously introduces updates.

* * * * *

Feature Releases
----------------

### Purpose

Deliver:

-   New features
-   New applications
-   Platform enhancements

* * * * *

### Naming Convention

Feature releases are named after cities.

* * * * *

Recent Releases
---------------

| Release | Year |
| --- | --- |
| San Diego | 2022 |
| Tokyo | 2022 |
| Utah | 2023 |
| Vancouver | 2023 |
| Washington DC | 2024 |
| Xanadu | 2024 |
| Yokohama | 2025 |

* * * * *

Release Frequency
-----------------

Typically:

```
Every 6--8 Months
```

* * * * *

Patch Releases
==============

### Purpose

Fix:

-   Bugs
-   Defects
-   Stability issues

* * * * *

Hotfixes
========

### Purpose

Resolve urgent issues quickly.

### Characteristics

-   Released as needed
-   Smaller than patch releases

* * * * *

Relationship
------------

```
Feature Release      ↓Patch Release      ↓Hotfixes
```

A patch release may contain multiple hotfixes.

* * * * *

7\. ServiceNow Environments
===========================

Organizations typically receive three environments.

* * * * *

Development Environment (DEV)
-----------------------------

### Purpose

Used by developers and administrators.

Activities:

-   Build applications
-   Create workflows
-   Configure features

* * * * *

Test Environment (TEST)
-----------------------

### Purpose

Validate changes before production.

Activities:

-   User Acceptance Testing (UAT)
-   Functional Testing
-   Bug Verification

* * * * *

Production Environment (PROD)
-----------------------------

### Purpose

Live environment used by actual users.

Contains:

-   Real business data
-   Active users
-   Production services

* * * * *

Environment Flow
================

```
Development      ↓Testing      ↓Production
```

* * * * *

8\. Deployment Process
======================

Step 1
------

Develop feature in DEV.

* * * * *

Step 2
------

Move changes to TEST.

* * * * *

Step 3
------

Perform testing.

* * * * *

Step 4
------

Move approved changes to PROD.

* * * * *

Step 5
------

Users begin using the feature.

* * * * *

9\. Cloning Best Practice
=========================

What is Cloning?
----------------

Copying one environment into another.

* * * * *

Common Practice
---------------

Clone:

```
Development
      ↓
Testing
      ↓
Production
```

* * * * *

Why Clone?
----------

Keeps environments synchronized.

Benefits:

-   Consistent testing
-   Accurate development
-   Reduced deployment risk

* * * * *

Risk of Not Cloning
-------------------

Over time:

```
Development ≠ Test ≠ Production
```

This can create:

-   Testing failures
-   Deployment conflicts
-   Unexpected bugs

* * * * *

10\. ServiceNow User Interface (UI)
===================================

The ServiceNow interface has three major components.

* * * * *

Banner
------

Located at the top.

Contains:

-   Search
-   User Profile
-   Notifications

* * * * *

Application Navigator
---------------------

Located on the left side.

Used to:

-   Search applications
-   Open modules
-   Navigate the platform

* * * * *

Main Content Frame
------------------

Located in the center.

Displays:

-   Lists
-   Forms
-   Dashboards
-   Reports

* * * * *

UI Layout
=========

```
+----------------------+
| Banner               |
+----------------------+

| Navigator | Content |
|            | Frame  |
|            |        |

* * * * *

11\. Lists and Forms
====================

Most daily work occurs in:

List View
---------

Displays:

```
Multiple Records
```

Example:

```
Incident List
```

* * * * *

Form View
---------

Displays:

```
Single Record
```

Example:

```
Incident INC0010001
```

* * * * *

12\. UI Changes Across Releases
===============================

ServiceNow occasionally updates the interface.

### Important Point

The appearance may change, but:

✅ Core functionality remains similar.

✅ Features may move locations.

✅ Navigation may slightly differ.

* * * * *

Example
-------

A button visible in one release may:

-   Move to another menu
-   Have a different icon
-   Appear in a different position

* * * * *

Steps / Process
===============

ServiceNow Change Deployment Process
------------------------------------

### Step 1

Develop feature in DEV.

### Step 2

Move changes to TEST.

### Step 3

Perform testing.

### Step 4

Resolve defects.

### Step 5

Deploy to PROD.

### Step 6

Users access the new functionality.

* * * * *

Environment Synchronization Process
-----------------------------------

### Step 1

Clone Production.

### Step 2

Overwrite Test Environment.

### Step 3

Clone Production.

### Step 4

Overwrite Development Environment.

### Step 5

Continue development with updated data.

* * * * *

Important Terms
===============
| Term                | Meaning                                         |
| ------------------- | ----------------------------------------------- |
| **ServiceNow**      | Cloud-based workflow automation platform        |
| **SaaS**            | Software delivered through a subscription model |
| **ITSM**            | IT Service Management                           |
| **Incident**        | Unplanned interruption to a service             |
| **Business Rule**   | Server-side automation logic                    |
| **Workflow**        | Automated business process                      |
| **Feature Release** | Major platform release containing new features  |
| **Patch Release**   | Bug-fix release                                 |
| **Hotfix**          | Emergency fix for specific issues               |
| **Clone**           | Copy one environment to another                 |
| **DEV**             | Development Environment                         |
| **TEST**            | Testing Environment                             |
| **PROD**            | Production Environment                          |


* * * * *

Commands / Syntax / Configuration
=================================

Environment Flow
----------------

```
DEV
 ↓
TEST
 ↓
PROD
```

* * * * *

Clone Strategy
--------------

```
PROD
 ↓
TEST

PROD
 ↓
DEV
```

* * * * *

ServiceNow Architecture
-----------------------

```
Browser
 ↓
Tomcat
 ↓
J2EE
 ↓
Rhino
 ↓
MySQL
```

* * * * *

Examples
========

Example 1: Incident Management
------------------------------

User reports:

```
Unable to Access Email
```

Support creates:

```
Incident Record
```

inside ServiceNow.

* * * * *

Example 2: Custom Application
-----------------------------

HR creates:

```
Employee Onboarding Application
```

using:

-   Forms
-   Workflows
-   Business Rules

* * * * *

Example 3: Environment Deployment
---------------------------------

Developer creates:

```
New Approval Workflow
```

Flow:

```
DEV → TEST → PROD
```

* * * * *

Certification Focus
===================

Important Points for Exams
--------------------------

-   ServiceNow is a **SaaS platform**.
-   ServiceNow is hosted in ServiceNow data centers.
-   ServiceNow originated as an **ITSM platform**.
-   Incident Management is the most widely used application.
-   ServiceNow supports many business areas beyond ITSM.
-   ServiceNow uses Java technologies and MySQL.
-   Feature releases occur approximately every **6--8 months**.
-   Organizations typically use **DEV, TEST, PROD** environments.
-   Production should be cloned regularly to lower environments.
-   UI contains Banner, Navigator, and Content Frame.

* * * * *

Common Mistakes
---------------

❌ Thinking ServiceNow must be installed locally.

❌ Confusing Patch Releases with Feature Releases.

❌ Making changes directly in Production.

❌ Forgetting to clone environments regularly.

❌ Assuming UI changes affect core functionality.

* * * * *

Things to Remember
------------------

✅ ServiceNow = SaaS.

✅ Hosted by ServiceNow.

✅ Started with ITSM.

✅ Incident Management is the flagship application.

✅ Supports HR, Security, DevOps, Asset Management, and more.

✅ Java + MySQL architecture.

✅ Releases every 6--8 months.

✅ Use DEV → TEST → PROD deployment process.

✅ Clone Production regularly.

* * * * *

Real-World Application
======================

Organizations use ServiceNow to:

-   Manage IT incidents
-   Automate employee onboarding
-   Track company assets
-   Handle security incidents
-   Manage customer requests
-   Perform compliance audits

A large enterprise may have:

```
50,000+ UsersThousands of Daily TicketsMultiple Custom Applications
```

all running on a single ServiceNow platform.

* * * * *

Quick Revision (30 sec)
=======================

-   ServiceNow is a **SaaS platform**.
-   Hosted in ServiceNow data centers.
-   Started with **ITSM**.
-   Most popular application = **Incident Management**.
-   Supports HR, Security, DevOps, ITAM, CSM, and GRC.
-   Built on Java, Tomcat, Rhino, and MySQL.
-   Releases occur every **6--8 months**.
-   Environments: **DEV → TEST → PROD**.
-   Clone Production regularly.
-   UI consists of Banner, Navigator, and Main Content Frame.