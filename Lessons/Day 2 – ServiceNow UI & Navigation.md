# Day 2 – ServiceNow UI & Navigation

## Learning Objectives

By the end of this lesson, you will be able to:

* Navigate the ServiceNow platform confidently
* Understand the Application Navigator
* Work with Lists and Forms
* Use Filters effectively
* Customize your workspace
* Create Favorites and Bookmarks
* Understand modules and applications
* Perform common administrative navigation tasks
* Complete a real-world hands-on exercise

---

# Table of Contents

1. Introduction
2. ServiceNow User Interface Overview
3. Banner Frame
4. Application Navigator
5. Applications and Modules
6. Lists
7. Forms
8. Filters
9. Favorites
10. History
11. User Menu
12. Settings and Preferences
13. Search Functionality
14. Real-Time Scenario
15. Hands-On Lab
16. Mini Project
17. Interview Questions
18. Key Takeaways

---

# 1. Introduction

The ServiceNow User Interface (UI) is the primary way users interact with the platform.

Whether you are an Administrator, Developer, ITIL User, or End User, understanding navigation is the first step toward mastering ServiceNow.

A well-understood UI helps you:

* Work faster
* Find records quickly
* Create reports
* Configure applications
* Troubleshoot issues

---

# 2. ServiceNow User Interface Overview

The ServiceNow UI consists of several major components:

```text
+--------------------------------------+
| Header / Banner                      |
+--------------------------------------+
| Application Navigator                |
|                                      |
| Applications                         |
| Modules                              |
|                                      |
+------------------+-------------------+
|                  |                   |
|                  |                   |
|                  | Main Content Area |
|                  |                   |
|                  |                   |
+------------------+-------------------+
```

Major Sections:

1. Banner/Header
2. Application Navigator
3. Main Content Area
4. User Menu
5. Search

---

# 3. Banner Frame

The Banner is located at the top of the screen.

It contains:

* ServiceNow Logo
* Search
* Notifications
* Settings
* User Profile

## Example

```text
----------------------------------------------------
| ServiceNow | Search | Notifications | User Menu |
----------------------------------------------------
```

### Why It Matters

The banner provides quick access to platform-wide features.

---

# 4. Application Navigator

The Application Navigator is located on the left side.

It is used to access applications and modules.

## Examples of Applications

* Incident
* Change
* Problem
* Asset
* CMDB
* Service Catalog

## Example

```text
Application Navigator

Incident
   -> Create New
   -> Open
   -> Assigned To Me

Change
   -> Create New
   -> Open
```

### Search in Navigator

You can type:

```text
incident
```

to quickly find Incident-related modules.

---

# 5. Applications and Modules

## What is an Application?

An Application is a collection of related modules.

Example:

```text
Incident Application
```

contains:

* Create New
* Open
* Assigned to Me
* Closed

---

## What is a Module?

A Module is a menu item that opens:

* Lists
* Forms
* Reports
* Dashboards

Example:

```text
Incident > Open
```

This module opens a list of incidents.

---

# 6. Lists

A List displays multiple records.

Example:

```text
Incident List
```

| Number | Short Description | State       |
| ------ | ----------------- | ----------- |
| INC001 | Email Issue       | Open        |
| INC002 | VPN Issue         | In Progress |

---

## Common List Features

### Sort

Click column header.

Example:

```text
Sort by Created Date
```

---

### Filter

Filter records quickly.

Example:

```text
State = Open
```

---

### Group

Group records by:

* Assignment Group
* Priority
* State

---

### Export

Available export formats:

* Excel
* CSV
* XML
* PDF

---

# 7. Forms

A Form displays a single record.

Example:

```text
Incident Record
```

Fields:

* Number
* Caller
* Category
* Priority
* State

---

## Form Components

### Fields

Example:

```text
Short Description
```

### Sections

Example:

```text
Details
Resolution
Notes
```

### Related Lists

Example:

```text
Tasks
Approvals
Attachments
```

---

# 8. Filters

Filters help locate records quickly.

## Example

Find all active incidents.

Condition:

```text
Active = True
```

---

## Multiple Conditions

```text
Priority = 1
AND
State = Open
```

---

## Filter Operators

| Operator     | Example                |
| ------------ | ---------------------- |
| is           | State is Open          |
| contains     | Name contains John     |
| starts with  | Number starts with INC |
| greater than | Priority > 2           |

---

# 9. Favorites

Favorites allow quick access to frequently used modules.

## Add Favorite

1. Open module
2. Click Star Icon
3. Save

Example:

```text
Incident > Open
```

Now available under Favorites.

---

## Benefits

* Faster navigation
* Personalized workspace
* Increased productivity

---

# 10. History

History tracks recently visited records and modules.

Example:

```text
Recently Viewed

Incident Open
Change Open
CMDB
```

---

## Why Use History?

Quickly return to previously visited pages.

---

# 11. User Menu

Located at the top-right corner.

Contains:

* Profile
* Preferences
* Logout

---

## Profile

View:

* Name
* Email
* Roles

---

## Logout

Always logout after practice sessions.

---

# 12. Settings and Preferences

Users can personalize the platform.

## Examples

### Theme

* Dark Theme
* Light Theme

### Time Format

```text
12-hour
24-hour
```

### Language

Choose preferred language.

---

# 13. Global Search

Global Search searches across the platform.

Example:

```text
INC0010050
```

Search Results:

* Incident
* Change
* Knowledge Articles

---

## Benefits

Find information quickly.

---

# 14. Real-Time Scenario

## Scenario

You are a ServiceNow Administrator.

A user reports:

```text
I cannot access my email.
```

Steps:

1. Open Application Navigator
2. Navigate to Incident
3. Open Existing Incidents
4. Search User
5. Review Existing Tickets
6. Create New Incident

This is a common real-world activity.

---

# 15. Hands-On Lab

## Task 1

Explore:

```text
Incident
Change
Problem
Knowledge
```

---

## Task 2

Create Favorites

Add:

```text
Incident Open
Change Open
```

---

## Task 3

Apply Filters

Find:

```text
All Active Incidents
```

---

## Task 4

Sort Incident List

Sort by:

```text
Created Date
```

---

## Task 5

Open and Review Forms

Open:

```text
Incident Form
```

Identify:

* Fields
* Sections
* Related Lists

---

# 16. Mini Project

## Help Desk Navigation Exercise

Objective:

Become comfortable navigating ServiceNow.

### Steps

1. Open Incident Application
2. Create Test Incident
3. Save Record
4. Search Record
5. Add Module to Favorites
6. View History
7. Update Incident
8. Close Incident

---

## Expected Outcome

Understand:

* Navigation
* Lists
* Forms
* Filters
* Favorites

---

# 17. Interview Questions

### Q1. What is Application Navigator?

A menu used to access applications and modules.

---

### Q2. Difference between Application and Module?

Application:
A collection of related functionality.

Module:
A menu item within an application.

---

### Q3. What is a List?

Displays multiple records.

---

### Q4. What is a Form?

Displays a single record.

---

### Q5. What is Global Search?

A platform-wide search mechanism.

---

### Q6. What are Favorites?

Quick-access shortcuts to frequently used modules.

---

### Q7. What is History?

A record of recently visited pages.

---

### Q8. Why are Filters important?

They help locate records efficiently.

---

# 18. Key Takeaways

* ServiceNow navigation is the foundation of platform usage.
* Applications contain modules.
* Lists display multiple records.
* Forms display single records.
* Filters improve search efficiency.
* Favorites increase productivity.
* History helps revisit recent work.
* Understanding navigation is essential for Administrators and Developers.
