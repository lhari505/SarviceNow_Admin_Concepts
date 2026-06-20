Lecture Summary

This lecture provides a foundational overview of ServiceNow, including its architecture, ecosystem, technology stack, release cycle, environments, and user interface. ServiceNow is a Software as a Service (SaaS) platform hosted in ServiceNow data centers and accessed through a web browser. The lecture also introduces major ServiceNow product areas, development lifecycle environments, and core UI components that users interact with daily.

Key Points
ServiceNow is a SaaS platform hosted by ServiceNow.
Originally focused on IT Service Management (ITSM).
Supports many business functions beyond ITSM.
Built on a Java-based technology stack.
Uses feature releases, patch releases, and hotfixes.
Organizations typically have Development, Test, and Production environments.
Frequent cloning keeps environments synchronized.
Main UI components are the Banner, Application Navigator, and Content Frame.
Users primarily work with List Views and Form Views.
Detailed Notes
1. What is ServiceNow?
Definition

ServiceNow is a Software as a Service (SaaS) platform licensed through a subscription model.

Similar SaaS products include:

Salesforce
Workday
Key Characteristics
No local installation required.
Hosted in ServiceNow Data Centers.
Accessed through any modern web browser.
Applications and data are stored in ServiceNow infrastructure.
Customers simply subscribe and access the platform online.
Important Concept

Unlike traditional software:

❌ No software installation on user computers.

❌ No hosting in customer data centers.

✅ Hosted entirely by ServiceNow.

2. ServiceNow Origins – IT Service Management (ITSM)
What is ITSM?

ITSM (IT Service Management) focuses on managing IT services and support processes.

Core ITSM Applications
Incident Management

Used to track and resolve service interruptions.

Example:

Internet outage
Email issue
Laptop problem
Software malfunction
Problem Management

Used to identify root causes of recurring incidents.

Change Management

Used to control changes made to IT systems.

Most Popular Application

Incident Management remains one of ServiceNow's most widely used applications.

Real-Life Example

When calling:

Internet provider
Mobile carrier
IT Help Desk

A support agent may create an Incident Ticket in ServiceNow behind the scenes.

3. Expansion of the ServiceNow Platform

ServiceNow has evolved far beyond ITSM.

Major Product Areas
IT Service Management (ITSM)

Core ticketing and service management.

IT Operations Management (ITOM)

Infrastructure monitoring and operations.

IT Business Management (ITBM)

Project and portfolio management.

IT Asset Management (ITAM)

Tracks organizational assets.

Examples:

Laptops
Servers
Software licenses
DevOps

Supports development and deployment processes.

Security Operations (SecOps)

Security incident and vulnerability management.

HR Service Delivery (HRSD)

Employee service and HR workflows.

Customer Service Management (CSM)

Customer support and service requests.

Governance, Risk & Compliance (GRC)

Risk management and regulatory compliance.

Key Takeaway

ServiceNow continuously expands its offerings with every release.

4. Custom Application Development

One of ServiceNow's strongest capabilities is building custom applications.

Benefits

Developers can leverage built-in platform features such as:

Business Rules
Workflows
Forms
Tables
Notifications
Approvals
Result

Organizations can rapidly develop business applications with minimal infrastructure concerns.

5. ServiceNow Technology Stack

Exam Note: Detailed stack knowledge is usually not heavily tested but is useful for understanding the platform.

Core Technologies
Component	Technology
Programming Platform	Java
Web Server	Apache Tomcat
Application Server	J2EE
Database	MySQL
JavaScript Engine	Mozilla Rhino
Mozilla Rhino

Mozilla Rhino is a JavaScript engine written in Java.

Purpose:

Executes JavaScript inside the Java environment.

Example:

When a developer writes:

Business Rules
Client Scripts
Script Includes

The JavaScript is processed using Rhino.

6. ServiceNow Release Cycle

ServiceNow delivers updates through:

Feature Releases

Contain:

New features
New applications
Platform enhancements

Feature releases are named after cities.

Recent Feature Releases
Year	Release
2022	San Diego
2022	Tokyo
2023	Utah
2023	Vancouver
2024	Washington DC
2024	Xanadu
2025	Yokohama
Release Frequency

Typically:

Every 6–8 months

Patch Releases

Contain:

Bug fixes
Stability improvements
Multiple hotfixes
Hotfixes

Contain:

Specific issue corrections
Emergency fixes
Important Note

Course concepts generally remain applicable across releases.

However:

UI may vary slightly.
Features may move locations.
New capabilities may be added.
7. ServiceNow Environments

A typical ServiceNow implementation includes three environments.

Development (DEV)

Purpose:

Build new features
Create applications
Perform configuration changes

Activities:

Development work
Customization
Initial testing
Test (TEST)

Purpose:

Validate changes
User Acceptance Testing (UAT)

Activities:

Functional testing
Bug verification
Regression testing
Production (PROD)

Purpose:

Live environment

Activities:

Used by end users
Runs business operations
8. Deployment Flow
Standard Process
Development
      ↓
     Test
      ↓
 Production
Workflow
Develop changes in DEV.
Move changes to TEST.
Perform validation and testing.
Fix defects if necessary.
Promote changes to PROD.
9. Cloning Best Practices
What is Cloning?

Copying one ServiceNow instance into another.

Example:

Production
   ↓
 Test
   ↓
 Development
Why Clone?

Keeps environments synchronized.

Benefits
Accurate testing
Consistent data
Reliable development
Fewer deployment surprises
Risks of Not Cloning

Over time:

DEV and TEST become outdated.
Data differs from Production.
Testing becomes unreliable.
Deployment risks increase.
Best Practice

Perform regular cloning from:

Production → Test → Development

10. ServiceNow User Interface (UI)

The UI contains three primary components.

1. Banner

Located at the top.

Purpose:

Navigation
User profile access
Global actions
2. Application Navigator

Located on the left side.

Purpose:

Search applications
Access modules
Navigate platform features
3. Main Content Frame

Located in the center/right area.

Purpose:

Displays forms
Displays lists
Displays records and applications
11. List View
Purpose

Displays multiple records at once.

Examples
Incident list
Change list
User list
Benefits
Search records
Filter records
Sort records
Bulk update records
12. Form View
Purpose

Displays a single record.

Examples

Viewing one:

Incident
User
Change Request
Benefits
Create records
Update records
Review details
13. UI Changes Across Releases

ServiceNow occasionally updates the UI.

Important Points
Core functionality remains similar.
Menu locations may change.
Appearance may differ slightly.
Concepts remain consistent.
Student Tip

If your instance looks different:

Do not panic.
Search for the same functionality.
The feature likely still exists.
Steps / Process
ServiceNow Development Lifecycle
Step 1

Develop changes in Development Environment.

Step 2

Move changes to Test Environment.

Step 3

Perform testing and validation.

Step 4

Fix identified defects.

Step 5

Promote changes to Production Environment.

Step 6

Perform regular cloning from Production.

Important Terms
Term	Meaning
ServiceNow	Cloud-based SaaS platform for digital workflows
SaaS	Software delivered through the internet via subscription
ITSM	IT Service Management
Incident	Record used to track service disruptions
Problem	Root cause analysis of recurring incidents
Change	Controlled modification to IT systems
Business Rule	Server-side automation logic
Feature Release	Major release containing new functionality
Patch Release	Collection of fixes and improvements
Hotfix	Immediate fix for specific issues
Clone	Copying one instance into another
DEV	Development Environment
TEST	Testing Environment
PROD	Production Environment
List View	Displays multiple records
Form View	Displays a single record
Commands / Syntax / Configuration
Environment Flow
DEV → TEST → PROD
Clone Flow
PROD → TEST
PROD → DEV
ServiceNow Stack
Java
   ↓
Apache Tomcat
   ↓
J2EE Application Server
   ↓
MySQL Database
   ↓
Mozilla Rhino (JavaScript Engine)
Examples
Example 1: Incident Management

Employee cannot access email.

Process:

Create Incident.
Assign technician.
Investigate issue.
Resolve incident.
Close ticket.
Example 2: Application Development

Business needs an Employee Asset Request application.

Developer uses:

Tables
Forms
Business Rules
Workflows

to quickly build the solution.

Example 3: Environment Promotion

Developer creates a feature in DEV.

After testing:

DEV → TEST → PROD

The feature becomes available to end users.

Certification Focus
Important Points for Exams
ServiceNow is a SaaS platform.
ServiceNow originated in ITSM.
Know Incident, Problem, and Change Management.
Understand DEV, TEST, and PROD environments.
Understand cloning purpose.
Know List View vs Form View.
Understand feature releases, patches, and hotfixes.
Feature releases are named after cities.
ServiceNow supports custom application development.
Common Mistakes

❌ Thinking ServiceNow is installed locally.

❌ Confusing TEST and PROD environments.

❌ Ignoring cloning best practices.

❌ Assuming UI differences mean functionality is removed.

❌ Deploying directly to Production without testing.

Things to Remember

✅ ServiceNow is cloud-hosted.

✅ Incident Management is ServiceNow's most recognized application.

✅ Custom applications are a major platform capability.

✅ Feature releases occur approximately every 6–8 months.

✅ Organizations typically use DEV, TEST, and PROD environments.

✅ Cloning keeps environments synchronized.

✅ Most user work occurs in List Views and Form Views.

Real-World Application

A large enterprise may use ServiceNow to:

Manage IT incidents.
Track hardware and software assets.
Automate HR onboarding.
Handle customer service requests.
Manage security incidents.
Track compliance requirements.

Developers build and test changes in DEV, validate them in TEST, and deploy them to PROD. Regular cloning ensures all environments stay aligned with the live system.