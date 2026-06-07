# Lesson 1: ServiceNow Fundamentals

## Course Overview

ServiceNow Admin Learning Roadmap.

This lesson introduces the ServiceNow platform, its architecture, products, benefits, and real-world usage. By the end of this lesson, you will understand why organizations use ServiceNow and how it helps automate business processes.

---

# Learning Objectives

After completing this lesson, you will be able to:

* Understand ServiceNow fundamentals
* Explain ServiceNow architecture
* Identify major ServiceNow products
* Understand ITSM concepts
* Describe ServiceNow instances
* Navigate the ServiceNow platform
* Understand real-world business use cases

---

# 1. What is ServiceNow?

ServiceNow is a cloud-based enterprise platform that helps organizations automate workflows and business processes.

It is widely used for:

* IT Service Management (ITSM)
* IT Operations Management (ITOM)
* Customer Service Management (CSM)
* HR Service Delivery (HRSD)
* Security Operations (SecOps)

---

## Simple Definition

ServiceNow is a platform that helps organizations manage work through automated workflows.

---

# 2. Why Was ServiceNow Created?

Before ServiceNow, companies managed IT requests using:

* Emails
* Excel Sheets
* Phone Calls
* Manual Tracking

Problems:

* Lost requests
* Delayed responses
* No visibility
* No SLA tracking

ServiceNow solves these problems by centralizing work management.

---

# 3. Real World Example

Imagine an employee cannot connect to VPN.

Traditional Process:

Employee → Email IT Team → Wait for Response

Problems:

* No tracking
* Delayed resolution
* No ownership

ServiceNow Process:

Employee → Create Incident

↓

Service Desk

↓

Network Team

↓

Issue Resolved

↓

Ticket Closed

Benefits:

* Faster support
* Accountability
* SLA Monitoring
* Reporting

---

# 4. What is a Workflow?

A workflow is a sequence of tasks performed to complete a business process.

Example:

Laptop Request Workflow

Employee Request

↓

Manager Approval

↓

IT Approval

↓

Laptop Allocation

↓

Request Completion

---

# 5. What is ITSM?

ITSM stands for Information Technology Service Management.

ITSM ensures IT services are delivered efficiently.

Main Processes:

* Incident Management
* Problem Management
* Change Management
* Request Management
* Knowledge Management

---

# 6. ServiceNow Products

## ITSM

Used to manage IT services.

Examples:

* Incidents
* Requests
* Changes

---

## ITOM

Used to manage infrastructure.

Examples:

* Discovery
* Event Management
* CMDB

---

## HRSD

Used by HR teams.

Examples:

* Employee Onboarding
* Employee Cases

---

## CSM

Used for customer support.

Examples:

* Customer Complaints
* Customer Requests

---

## SecOps

Used by Security Teams.

Examples:

* Security Incidents
* Vulnerability Management

---

# 7. ServiceNow Architecture

ServiceNow follows a three-tier architecture.

## Tier 1 – Presentation Layer

User Interface

Examples:

* Forms
* Lists
* Dashboards

Users access ServiceNow through a web browser.

---

## Tier 2 – Application Layer

Contains business logic.

Examples:

* Business Rules
* Client Scripts
* Flow Designer
* UI Policies

---

## Tier 3 – Database Layer

Stores data.

Examples:

* Incidents
* Users
* Requests
* Changes

---

# Architecture Flow

User Browser

↓

Application Server

↓

Database

---

# 8. What is Cloud Computing?

Cloud Computing means accessing services over the internet instead of local servers.

ServiceNow is a cloud platform.

Benefits:

* No local installation
* Automatic updates
* High availability
* Scalability

---

# 9. Service Models

## SaaS

Software as a Service

Examples:

* ServiceNow
* Salesforce
* Microsoft 365

Users only consume the software.

---

## PaaS

Platform as a Service

Provides development platform.

Example:

ServiceNow Platform

Developers build applications.

---

## IaaS

Infrastructure as a Service

Provides servers and storage.

Examples:

* AWS EC2
* Azure Virtual Machines

---

# 10. What is an Instance?

An Instance is a dedicated ServiceNow environment.

Example:

https://dev12345.service-now.com

Every organization gets separate instances.

---

# Types of Instances

## Development Instance

Used for development.

Activities:

* Create Forms
* Create Business Rules
* Build Catalog Items

---

## Test Instance

Used for testing.

Activities:

* User Testing
* QA Testing

---

## Production Instance

Used by actual users.

Activities:

* Incident Creation
* Request Submission

---

# Promotion Path

Development

↓

Test

↓

Production

---

# 11. ServiceNow Releases

ServiceNow releases new versions regularly.

Examples:

* Tokyo
* Utah
* Vancouver
* Washington DC
* Xanadu
* Yokohama
* Zurich

Benefits:

* New Features
* Security Updates
* Performance Improvements

---

# 12. ServiceNow Interface Overview

Main Components:

## Banner Frame

Top section of application.

Contains:

* User Profile
* Search
* Notifications

---

## Application Navigator

Used to search modules.

Example:

Incident

Users

Reports

---

## Content Frame

Displays records and forms.

---

# 13. Lists and Forms

## List

Displays multiple records.

Example:

Incident List

| Number | Description  |
| ------ | ------------ |
| INC001 | VPN Issue    |
| INC002 | Laptop Issue |

---

## Form

Displays one record.

Example:

Incident Form

* Number
* Caller
* Description
* Priority
* State

---

# 14. ServiceNow Tables

Everything in ServiceNow is stored in tables.

Examples:

| Table Name     | Purpose          |
| -------------- | ---------------- |
| Incident       | Stores incidents |
| Problem        | Stores problems  |
| Change Request | Stores changes   |
| User           | Stores users     |

---

# 15. Understanding Records

A record is a row in a table.

Example:

Incident Table

| Number     | Description |
| ---------- | ----------- |
| INC0010001 | VPN Down    |

This row is called a record.

---

# 16. What is Automation?

Automation reduces manual effort.

Example:

When Incident Priority = High

Automatically:

* Assign Group
* Send Email
* Create Task

No manual action required.

---

# 17. Departments Using ServiceNow

IT Department

* Incident Management
* Change Management

HR Department

* Employee Onboarding

Finance Department

* Approval Requests

Facilities Department

* Asset Requests

Security Team

* Security Incidents

---

# 18. Benefits of ServiceNow

* Workflow Automation
* Centralized Platform
* Faster Resolution
* SLA Tracking
* Better Reporting
* Improved Productivity
* Audit Tracking

---

# 19. Hands-On Exercise

Exercise 1

Login to ServiceNow Developer Instance.

Steps:

1. Open Application Navigator
2. Search Incident
3. Click Create New
4. Enter:

Short Description:

Laptop Not Working

5. Click Submit

Observe:

* Incident Number
* State
* Assignment Group

---

# Exercise 2

Open:

System Diagnostics

Review:

* Instance Name
* Build Version
* Release Information

---

# 20. Business Scenario

Company: ABC Technologies

Employees: 5000

Challenges:

* VPN Issues
* Laptop Issues
* Software Requests

Solution:

Implemented ServiceNow ITSM.

Results:

* 50% Faster Resolution
* SLA Compliance
* Better Reporting
* Improved User Satisfaction

---

# Interview Questions

## Q1. What is ServiceNow?

Answer:

ServiceNow is a cloud-based platform used to automate enterprise workflows and IT services.

---

## Q2. What is ITSM?

Answer:

ITSM is Information Technology Service Management, used to manage and deliver IT services efficiently.

---

## Q3. What are the major ServiceNow products?

Answer:

* ITSM
* ITOM
* HRSD
* CSM
* SecOps

---

## Q4. What is an Instance?

Answer:

An instance is an individual ServiceNow environment used for development, testing, or production.

---

## Q5. Explain ServiceNow Architecture.

Answer:

ServiceNow follows a three-tier architecture:

1. Presentation Layer
2. Application Layer
3. Database Layer

---

## Q6. What is the difference between List and Form?

Answer:

List displays multiple records.

Form displays a single record.

---

# Lesson Summary

In this lesson, you learned:

* ServiceNow Fundamentals
* ITSM Concepts
* ServiceNow Products
* Architecture
* Instances
* Lists and Forms
* Tables and Records
* Automation Concepts
* Real-World Business Usage

Congratulations! You have completed Lesson 1 – ServiceNow Fundamentals.