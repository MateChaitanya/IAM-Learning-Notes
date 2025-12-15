# LDAP (Lightweight Directory Access Protocol)

LDAP is one of the most important concepts in IAM.
Almost every IAM tool (Okta, Saviynt, SailPoint) works with LDAP or Active Directory.

This document explains LDAP in simple words with real examples.

---

## What is LDAP?

LDAP stands for **Lightweight Directory Access Protocol**.

LDAP is a **protocol** used to:
- Store user information
- Search user details
- Authenticate users
- Manage directory data

LDAP works like a **phone directory** for users in an organization.

---

## Why LDAP is Needed?

In large organizations:
- Thousands of employees exist
- Many applications need user details
- Authentication must be centralized

LDAP provides:
- Central user store
- Faster authentication
- Consistent user data

---

## What Information is Stored in LDAP?

LDAP stores user attributes such as:
- Username
- Email
- Employee ID
- Department
- Role
- Password (encrypted)
- Group membership


Example:
- **Name**: Chaitanya Mate
- **Username**: chaitanya.mate
- **Email**: chaitanya.mate@company.com
- **Department**: IT


---

## LDAP Directory Structure (Very Important)

LDAP uses a **tree structure** called **DIT (Directory Information Tree)**.

Example:
<pre>
dc=company,dc=com
├── ou=Employees
│   ├── uid=chaitanya.mate
│   ├── uid=rahul.sir
│
├── ou=Groups
│   ├── cn=Admins
│   ├── cn=Developers
</pre>


Explanation:
- `dc` → Domain Component
- `ou` → Organizational Unit
- `uid` → User ID
- `cn` → Common Name

---

## LDAP vs Database

| LDAP | Database |
|-----|---------|
| Optimized for read | Optimized for transactions |
| Tree structure | Table structure |
| Used for authentication | Used for business data |
| Fast lookup | Slower for identity search |

LDAP is **not used like MySQL**.

---

## LDAP Authentication Flow

1. User enters username & password
2. Application sends request to LDAP
3. LDAP verifies credentials
4. LDAP returns success or failure
5. Application grants or denies access

Simple flow:
User → Application → LDAP → Application


---

## LDAP Bind Operation

**Bind** means login/authentication to LDAP.

Types of Bind:
- Simple Bind (username + password)
- Anonymous Bind (no credentials)
- SASL Bind (secure authentication)

Most IAM tools use **secure bind**.

---

## LDAP Operations (CRUD)

LDAP supports basic operations:

- **Add** → Create user
- **Search** → Find user
- **Modify** → Update user attributes
- **Delete** → Remove user

IAM tools use these operations for provisioning.

---

## LDAP and Groups

LDAP groups are used for:
- Role assignment
- Access control

Example:
- **Developers Group** → Git access
- **HR Group** → Payroll access


Users get access through **group membership**.

---

## LDAP in IAM (Real Example)

### Joiner Process:
1. HR adds employee
2. IAM creates user in LDAP
3. Groups assigned automatically
4. Access granted

### Leaver Process:
1. HR marks employee inactive
2. IAM disables LDAP account
3. Access removed everywhere

---

## LDAP vs Active Directory (AD)

| LDAP | Active Directory |
|----|----------------|
| Protocol | Directory Service |
| Platform independent | Microsoft based |
| Used by many tools | Used mainly in Windows |
| Can exist without AD | AD uses LDAP |

👉 **Active Directory uses LDAP internally**

---

## LDAP and Okta

- Okta integrates with LDAP/AD
- Okta syncs users from LDAP
- LDAP can be source of truth
- Authentication can be delegated to LDAP

Flow:
User → Okta → LDAP → Okta → App


---

## LDAP and Saviynt

- Saviynt governs LDAP access
- Performs access reviews
- Certifies group memberships
- Ensures compliance

---

## LDAP Security

LDAP security includes:
- SSL/TLS encryption
- Secure Bind
- Access control rules

Secure LDAP uses:
-**LDAPS (Port 636)**


---

## LDAP Ports

| Port | Purpose |
|----|-------|
| 389 | LDAP (non-secure) |
| 636 | LDAPS (secure) |

---

## LDAP in Interviews (Important Points)

- LDAP is a protocol
- Used for centralized authentication
- Stores user identity data
- Works with IAM tools
- Uses tree structure (DIT)

---

## One-Line Definition (For Interview)

**LDAP is a directory protocol used to store, search, and authenticate user identities in a centralized manner.**

---

## Final Note

Understanding LDAP is mandatory for:
- IAM roles
- Okta
- Saviynt
- Identity Governance

This knowledge directly applies in real projects and interviews.

