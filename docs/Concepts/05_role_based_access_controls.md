# Role-Based Access Controls

TreasuryPro uses **Role-Based Access Control (RBAC)** to manage user permissions. Instead of assigning permissions individually, permissions are grouped into **Roles**, which are then assigned to users.

## How Roles are Defined

| Role | Permissions Included | Key Task |
| :--- | :--- | :--- |
| **Viewer** | View all balances, run all reports. | Monitoring cash position. |
| **Creator** | View balances, create payment templates, initiate payments. | Preparing payment batches. |
| **Approver** | View all, approve any payment initiated by a Creator. | Releasing final payment to bank. |
| **Administrator** | All permissions, including user and system settings. | Managing user accounts and bank connections. |

## Separation of Duties

RBAC enforces **Separation of Duties (SoD)**. For example, the same user cannot be assigned both the **Creator** role and the **Approver** role for the same account, preventing a single person from initiating and finalizing a payment alone.