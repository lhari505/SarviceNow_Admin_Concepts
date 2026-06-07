# Lesson 1: ServiceNow Fundamentals

---

# Page 1: Course Overview

## Welcome to ServiceNow Admin Learning Roadmap

This document is the foundation of your ServiceNow Admin learning journey.

ServiceNow is widely used in enterprise IT environments to automate workflows, manage incidents, and improve service delivery.

This lesson introduces:

* ServiceNow basics
* Architecture
* ITSM overview
* Instance types
* Real-world usage

---

# Page 2: Learning Objectives

After completing this lesson, you will understand:

* What ServiceNow is and why it is used
* Core ITSM concepts
* ServiceNow architecture layers
* SaaS vs PaaS model
* Instance environments (Dev/Test/Prod)
* ServiceNow UI basics
* Real-world business usage

---

# Page 3: What is ServiceNow?

ServiceNow is a **cloud-based enterprise workflow platform** used to automate business and IT processes.

It helps organizations manage:

* IT services
* Employee requests
* Customer support
* Security incidents
* HR processes

---

## Simple Definition

ServiceNow is a platform that helps organizations manage and automate work through digital workflows.

---

## Real Use Case

When an employee has a VPN issue:

Instead of emails and manual tracking:

ServiceNow provides structured ticketing:

* Incident creation
* Assignment
* Resolution tracking
* Closure with audit history

---

# Page 4: Why ServiceNow is Needed?

### Before ServiceNow

Organizations used:

* Emails
* Excel sheets
* Phone calls
* Manual follow-ups

### Problems

* No tracking system
* Missed requests
* No accountability
* SLA violations

---

### After ServiceNow

Everything is centralized:

* Automated ticket creation
* Workflow assignment
* SLA tracking
* Reporting dashboards

---

# Page 5: ITSM Overview

ITSM = IT Service Management

It defines how IT services are delivered and managed.

## Core ITSM Modules

| Module               | Purpose                 |
| -------------------- | ----------------------- |
| Incident Management  | Restore service quickly |
| Problem Management   | Find root cause         |
| Change Management    | Manage system changes   |
| Request Management   | Handle service requests |
| Knowledge Management | Share solutions         |

---

## Example

Laptop not working → Incident created → Assigned → Resolved → Closed

---

# Page 6: ServiceNow Architecture

ServiceNow follows a **3-layer architecture**

---

## 1. Presentation Layer

User interface layer.

Includes:

* Forms
* Lists
* Dashboards

Users interact using browsers like Chrome or Edge.

---

## 2. Application Layer

Contains business logic:

* Business Rules
* Client Scripts
* Flow Designer
* UI Policies

Example:

If Priority = High → Auto assign to Network Team

---

## 3. Database Layer

Stores all data in tables:

* Incident
* Problem
* Change
* User

---

## Architecture Flow

User → Application Server → Database

---

# Page 7: Cloud & Service Models

## What is Cloud Computing?

Cloud computing means accessing services over the internet without installing software locally.

ServiceNow is a **SaaS platform**.

---

## Service Models

### SaaS (Software as a Service)

* ServiceNow
* Salesforce
* Microsoft 365

Users simply use the application.

---

### PaaS (Platform as a Service)

ServiceNow also acts as a platform where developers build applications.

---

### IaaS (Infrastructure as a Service)

Examples:

* AWS EC2
* Azure Virtual Machines

Provides servers and infrastructure.

---

# Page 8: What is an Instance?

An instance is a **separate ServiceNow environment**.

Example URL:

https://dev12345.service-now.com

---

## Types of Instances

### Development Instance

Used for:

* Configuration
* Development
* Testing new features

---

### Test Instance

Used for:

* QA testing
* User acceptance testing

---

### Production Instance

Used by real users:

* Incident creation
* Request handling

---

## Instance Flow

Development → Testing → Production

---

# Page 9: ServiceNow Interface

## Main UI Components

### 1. Banner Frame

Top section:

* User profile
* Search
* Notifications

---

### 2. Application Navigator

Used to search modules:

* Incident
* Users
* Reports

---

### 3. Content Area

Displays:

* Forms
* Lists
* Records

---

## Lists vs Forms

### List View

Shows multiple records

Example:

INC001 → VPN Issue
INC002 → Laptop Issue

---

### Form View

Shows single record details:

* Number
* Caller
* Priority
* State

---

# Page 10: Real-World Example & Summary

## Business Scenario

Company: ABC Technologies

Challenges:

* VPN issues
* Laptop failures
* Software requests

---

## Solution

Implemented ServiceNow ITSM:

* Incident Management
* Automated assignment
* SLA tracking
* Dashboards

---

## Results

* Faster resolution time (50% improvement)
* Better reporting
* Reduced manual effort
* Improved user satisfaction

---

# Interview Questions

## Q1. What is ServiceNow?

A cloud-based platform used to automate IT and business workflows.

---

## Q2. What is ITSM?

ITSM is the process of managing IT services efficiently.

---

## Q3. What is an Instance?

A separate ServiceNow environment used for development, testing, or production.

---

## Q4. What is ServiceNow architecture?

Three layers:

* Presentation
* Application
* Database

---

## Q5. Difference between List and Form?

* List → Multiple records
* Form → Single record

---

# Lesson Summary

In this lesson, you learned:

* ServiceNow fundamentals
* ITSM basics
* Architecture
* Cloud model
* Instances
* UI navigation
* Real-world usage

---

## Next Lesson Preview

Lesson 2 will cover:

* Users
* Groups
* Roles
* Access control
* Admin setup
