
---

## Steps / Process: Obtaining a Personal Developer Instance (PDI)

Follow these exact steps to set up your isolated practice environment:

1. **Navigate to the Site:** Go to the official [ServiceNow Developer Site](https://developer.servicenow.com).
2. **Register an Account:** Sign up for a free developer account using your email address.
3. **Request an Instance:** Once authenticated, locate your developer dashboard and click the **Request an Instance** button.
4. **Choose Your Release:** Select the latest stable version available to match the course ecosystem.
5. **Secure Your Credentials:** Save the generated instance URL, administrative username (`admin`), and temporary password immediately.

---

## Important Terms

| Term | Meaning |
| :--- | :--- |
| **PDI** | **Personal Developer Instance**; a free, isolated cloud sandbox provided by ServiceNow for learning, testing, and building applications. |
| **Instance** | A standalone cloud-based environment containing your specific ServiceNow platform database and applications. |
| **Out-of-the-Box (OOTB)** | The default features, configurations, and settings built into the ServiceNow platform before any custom changes are made. |

---

## Commands / Syntax / Configuration
* **System Maintenance Configuration:** There are no code commands for Section 1, but you must configure your habit to log into your PDI regularly. 
* **Inactivity Rule:** If your PDI detects **10 consecutive days of inactivity**, ServiceNow will reclaim (wipe and delete) your instance. Log in at least once a week to prevent losing your progress.

---

## Certification Focus
* **Remember for the Exam:** The standard user interface basics, navigation elements, and system definitions don't radically change between releases. Focus heavily on core administration principles.
* **Common Mistake:** Forgetting to log into the PDI during long breaks. If your instance is reclaimed due to inactivity, you will have to request a new one and re-do your custom configurations from scratch.

---

## Real-World Application
In enterprise environments, production data is highly sensitive. Companies use a multi-instance landscape (typically **Development ➔ Test ➔ Production**). As an administrator, you will use your developer-level skills to safely build and configure features in a non-production environment first, mimicking the workflow you practice on your PDI before moving anything into real-world corporate systems.

---

## Quick Revision (30 sec)
* **PDI stands for** Personal Developer Instance—your free personal cloud sandbox.
* **Register at** `developer.servicenow.com` to request your instance.
* **Avoid deletion** by logging into your PDI at least once every 10 days to keep it active.
* **Use `docs.servicenow.com`** as your primary reference manual for platform rules.
* **The CSA exam** tests foundational platform mechanics which remain stable across release versions.