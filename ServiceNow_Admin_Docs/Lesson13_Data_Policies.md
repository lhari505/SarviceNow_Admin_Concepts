### Simple Explanation: Data Policies

**What is a Data Policy?**

A Data Policy is a rule that validates data on the **server-side**.

Think of it as:

> **UI Policy = Front Door Security**
>
> **Data Policy = Back Door Security**

Even if data comes from:

-   Forms
-   Import Sets
-   REST APIs
-   SOAP Web Services

the Data Policy still checks whether the data follows the rules.

* * * * *

### Why Do We Need Data Policies?

Suppose you have a rule:

> "Close Notes must be filled before an Incident is Closed."

A user using the ServiceNow form cannot bypass this.

But what if data comes from:

-   Excel Import
-   REST API
-   Integration Tool

Without a Data Policy, those systems could bypass the rule.

Data Policies prevent this.

* * * * *

### Real-Time Example

#### Requirement

When an Incident State is:

```
ResolvedORClosed
```

Then:

```
Close Code = MandatoryClose Notes = Mandatory
```

If these fields are empty:

```
Update Fails
```

* * * * *

### Data Policy Components

#### 1\. Table

The table where the policy runs.

Example:

```
Incident [incident]
```

* * * * *

#### 2\. Conditions

When should the policy run?

Example:

```
State is ResolvedORState is Closed
```

* * * * *

#### 3\. Data Policy Rules

What fields should be validated?

Example:

| Field | Mandatory |
| --- | --- |
| Close Code | True |
| Close Notes | True |

* * * * *

### Navigation

```
System Policy   → Data Policies
```

To create a new Data Policy:

```
System Policy   → Data Policies   → New
```

* * * * *

### Difference Between UI Policy and Data Policy

| UI Policy | Data Policy |
| --- | --- |
| Client-side | Server-side |
| Works on forms | Works on forms, imports, APIs |
| Controls UI behavior | Controls data validation |
| Can hide fields | Cannot hide fields |
| Can make fields mandatory | Can make fields mandatory |
| Can make fields read-only | Can enforce data rules |

* * * * *

### Real-Time Admin Use Cases

#### Incident Management

Require:

-   Close Code
-   Close Notes

before closing an Incident.

* * * * *

#### Change Management

Require:

```
Change TypeRiskAssignment Group
```

before a Change Request can be submitted.

* * * * *

#### Integrations

When data comes from:

-   REST API
-   SOAP API
-   Import Set

ensure required fields are populated.

* * * * *

### CSA Exam Points

Remember:

✅ Data Policies run on the **Server-side**

✅ Similar to UI Policies

✅ Used for **Imports and Integrations**

✅ Can make fields **Mandatory**

✅ Helps maintain **Data Integrity**

❌ Cannot hide fields

❌ Cannot show fields

❌ Cannot change form layout

### One-Line Interview Answer

> "A Data Policy is a server-side validation mechanism used to enforce data integrity across forms, imports, and integrations by making fields mandatory or validating data before it is saved."