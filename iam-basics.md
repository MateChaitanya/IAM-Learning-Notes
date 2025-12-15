# IAM – Identity and Access Management

IAM stands for **Identity and Access Management**.

IAM is a framework that ensures:
- The **right user**
- Gets the **right access**
- To the **right system**
- At the **right time**
- For the **right reason**

IAM is a core part of **cybersecurity**.

---

## Why IAM is Needed

In organizations:
- Thousands of users exist
- Many applications are used
- Manual access management is risky

Problems without IAM:
- Unauthorized access
- Data leakage
- Delayed access removal
- Compliance issues

IAM solves these problems.

---

## What is Identity?

An **Identity** represents a user in the organization.

Examples:
- Employee
- Intern
- Contractor
- Vendor
- Customer

Identity contains user information such as:
<pre>
- Name
- Employee ID
- Email
- Department
- Role
- Manager
</pre>


Identity answers:
> **Who is the user?**

---

## What is an Account?

An **Account** is a technical representation of identity in a system.

Example:
- **Identity**: Chaitanya Mate
- **Account**: chaitanya.mate@company.com


One identity can have **multiple accounts**:
- Email account
- VPN account
- Application account

---

## Identity vs Account

| Identity | Account |
|---------|--------|
| Business concept | Technical concept |
| Represents a person | Represents system access |
| Created in IAM | Created in applications |

---

## Authentication

Authentication means:
> **Verifying who the user is**

Examples:
- Username & password
- OTP
- Biometric
- MFA

If authentication fails → access denied.

---

## Authorization

Authorization means:
> **Verifying what the user can access**

Examples:
- Read-only access
- Admin access
- Application-specific access

Authorization happens **after authentication**.

---

## Authentication vs Authorization
- **Login** → Authentication
- **Access Level** → Authorization


---

## Provisioning

Provisioning means:
> **Creating user access automatically**

<pre>
HR adds employee
↓
IAM creates accounts
↓
Access granted
</pre>


---

## Deprovisioning

Deprovisioning means:
> **Removing access when user leaves**

<pre>
Employee exits
↓
IAM disables accounts
↓
Access removed everywhere
</pre>


---

## Joiner – Mover – Leaver (JML)

### Joiner
- New employee joins
- Accounts are created
- Access is assigned

### Mover
- Role or department changes
- Old access removed
- New access granted

### Leaver
- Employee leaves
- All access revoked

---

## IAM Lifecycle Flow

<pre>
HR System
↓
IAM System
↓
Directory (LDAP / AD)
↓
Applications
</pre>


---

## Source of Truth (SoT)

Source of Truth is the system where **user data originates**.

Common SoT systems:
- HRMS (Workday, BambooHR)

IAM relies on SoT for:
- Joiner events
- Mover events
- Leaver events

---

## IAM Components

Core IAM components:
- Identity Management
- Access Management
- Authentication
- Authorization
- Provisioning
- Deprovisioning
- Governance
- Auditing

---

## IAM Tools

Examples of IAM-related tools:
- **Okta** – SSO, MFA, lifecycle management
- **Saviynt** – Identity governance
- **Active Directory** – Directory service
- **LDAP** – Directory protocol

---

## IAM Real-World Example

<pre>
Employee joins company
↓
HR updates employee record
↓
IAM detects the change
↓
User created in AD
↓
Access provided to applications
</pre>


---

## Benefits of IAM

- Improved security
- Reduced manual effort
- Faster onboarding
- Easy access removal
- Compliance readiness

---

## IAM and Compliance

IAM helps organizations:
- Enforce least privilege
- Perform access reviews
- Pass security audits

Managers can verify:
- Who has access
- Why access is provided

---

## One-Line Definition (Interview)

**IAM is used to manage digital identities and control access to systems securely.**

---

## Final Note

IAM is the foundation for:
- Okta
- Saviynt
- LDAP
- Active Directory
- Enterprise security systems

Strong IAM fundamentals are essential for IAM roles and interviews.
