#  ServiceNow Overview

## Lecture Summary

This section introduces the foundational architecture of the ServiceNow platform, breaking down its delivery model as a Cloud-based Software-as-a-Service (SaaS). It explores how ServiceNow structured its data management through distinct cloud instances, how it manages platform versions named alphabetically after global cities, and provides a quick structural tour of the user interface.

---

## Key Points

* **SaaS Delivery:** ServiceNow is licensed on a subscription basis and runs entirely in the cloud, removing the need for local hardware installation.

* **Multi-Instance Architecture:** Every organization receives isolated database silos (instances), ensuring configuration and security changes do not leak into other companies' data.

* **Release Cadence:** Platform upgrades drop twice per year following an alphabetical naming system based on major global cities.

---

## Detailed Notes

### 1. What is ServiceNow?

ServiceNow is a cloud-based workflow automation platform used by organizations to manage IT services, employee requests, approvals, and business processes through a centralized system. It helps automate tasks, improve efficiency, and provide better service management.

# Real-Life Example

Think of ServiceNow as an online help desk and workflow management system.

For example:

1. An employee needs a new laptop.
2. They submit a request in ServiceNow.
3. The manager receives an approval request.
4. The IT team gets a task to prepare the laptop.
5. The employee can track the request status.
6. Once completed, the request is closed.

Everything happens automatically and is tracked in one system.

# Why Companies Use ServiceNow

✅ Automates repetitive work

✅ Tracks requests and incidents

✅ Improves productivity

✅ Reduces manual effort

✅ Provides reports and dashboards

✅ Centralizes all service requests

### 2. Multi-Instance vs. Multi-Tenant Architecture

Understanding how ServiceNow holds data is critical for system administrators:

* **Multi-Tenant (Standard Cloud):** Multiple companies share the exact same application and database hardware resources. (e.g., Salesforce).

* **Multi-Instance (ServiceNow Model):** Every client organization gets their own isolated, dedicated web application and database environment. 

  * *Benefit:* Upgrades, database tuning, and custom application scripts can be managed independently for each client without breaking things for others.

### 3. The Enterprise Environment Landscape

In a real enterprise deployment, you do not configure applications directly where regular employees work. ServiceNow infrastructure typically utilizes a three-tiered instance strategy:

1\. **Development (Dev):** Where administrators and developers build features and test configurations.

2\. **Test/QA:** Where configurations are moved to undergo strict quality assurance and user acceptance testing.

3\. **Production (Prod):** The live environment utilized by the end users to conduct day-to-day business operations.

---

Steps / Process: Navigating the Core UI Components
--------------------------------------------------

When logging into a newly provisioned instance, the interface breaks down into three key functional areas. Follow these simple paths to navigate them:

## 1\. Accessing Global Utilities via the Banner Frame

### What is the Banner Frame?

The Banner Frame is the top header bar in ServiceNow. It provides access to system-wide features such as Search, User Preferences, Notifications, and Settings.

### Navigation
1. Login to your ServiceNow instance.
2. Look at the top-right corner.
3. Click your Profile Icon.
4. Explore:
Preferences
Impersonate User
Logout

### Real-Time Example

Suppose a user reports that dates are displaying in the wrong time zone.

Solution:

Click Profile Icon
Open Preferences
Change Time Zone
Save
## 2\. Finding Modules via the Application Navigator

### What is Application Navigator?

The Application Navigator is the left-side menu panel used to access applications and modules.

1. Navigation
2. Locate Filter Navigator.
3. Type "Incident".
4. Expand Incident application.
5. Click:
Create New
Open
All

### Example:

Real-Time Example

A service desk agent needs to create a new incident.

### Navigation:

Application Navigator
→ Incident
→ Create New
## \3. Interacting with Data via Content Frame
### What is the Content Frame?

The Content Frame is the central workspace where lists and forms are displayed.

1. Navigation
Open:
Incident → All
Observe Incident List View.
Click any Incident Number.
Form View opens.

### Example:

Real-Time Example

A user reports a laptop issue.

Open Incident List.
Click existing incident.
Update:
State
Assignment Group
Work Notes
Save record.

* * * * *

Important Terms
---------------

| **Term** | **Meaning** |
| --- | --- |
| **SaaS** | **Software as a Service**; software distribution model where a third-party provider hosts applications over the internet. |
| **Instance** | An isolated, specific cloud URL sandbox or production environment dedicated to a single customer. |
| **Application Navigator** | The left-hand sidebar menu containing all modules and applications accessible to your user role. |
| **ITSM** | **IT Service Management**; the core ServiceNow suite used to design, deliver, and manage IT services (e.g., Incidents, Problems, Changes). |

* * * * *

Commands / Syntax / Configuration
---------------------------------

-   **The Navigator Filter Textbox:** Typing keywords into the top of the Application Navigator instantly filters out non-matching menu options.

-   **Configuration Shortcut (Bonus Pro-Tip):** Typing `<table_name>.list` (e.g., `incident.list`) into the navigator filter box and hitting Enter bypasses menus and opens that data table list view directly in the content frame.

* * * * *

Examples
--------

-   **Release Name Tracking:** * Older historical versions: *Kingston*, *London*, *Madrid*.

    -   Modern versions: *Utah*, *Washington DC*, *Xanadu*.

-   **URL Formatting:** A company named "Acme" will typically access their instances via unique subdomains like `acmedev.service-now.com`, `acmetest.service-now.com`, and `acme.service-now.com`.

* * * * *

Certification Focus
-------------------

-   **Remember for the Exam:** ServiceNow uses a **Multi-Instance** architecture, *not* multi-tenant. This is a favorite trick question on the CSA exam.

-   **Common Mistake:** Confusing the *Banner Frame* (global utilities) with the *Application Navigator* (menu structures). Memorize the exact terminology used for the user interface zones.

-   **Release sequence rule:** Platform updates occur **twice a year** and follow alphabetical city naming conventions.

* * * * *

### Real-Life Company Example

Suppose employees report:

"We need a new category called 'Laptop Upgrade' while creating IT requests."

## As a ServiceNow Administrator:

1. Create the category in Dev.
2. Test request creation.
3. Capture changes in an Update Set.
4. Move Update Set to Test.
5. QA team validates functionality.
6. Deploy to Production.
7. Employees can now select "Laptop
8. Upgrade" when submitting requests.
#### Interview Question

Why should we not make changes directly in Production?

Answer:

1. Can impact live users.
2. May cause system outages.
3. Difficult to test safely.
#### Following Dev → Test → Production ensures quality and stability.
Key Takeaway

A ServiceNow Administrator's daily workflow is:

Build → Test → Package → Validate → Deploy

using

Development → Update Set → Test → Production

to ensure changes are safe and reliable before reaching end users

* * * * *

Quick Revision (30 sec)
-----------------------

-   **ServiceNow is a SaaS platform** that runs entirely inside web browsers.

-   **It utilizes a Multi-Instance architecture** giving every client a dedicated database instance.

-   **Platform upgrades launch twice a year** following an alphabetical global city naming pattern.

-   **The UI contains three main frames:** The Banner Frame, Application Navigator, and Content Frame.

-   **The typical deployment lifecycle** runs from Development ➔ Test ➔ Production.