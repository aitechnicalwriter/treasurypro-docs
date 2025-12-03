# QBank Connect Status Codes (Troubleshooting)

When payments fail or data syncs are interrupted, TreasuryPro displays a status code originating from the QBank Connect API. Use this table to understand the issue and identify the next step.

| Code | Plain Language Meaning | Resolution/Next Step |
| :--- | :--- | :--- |
| **200 OK** | Success. The request was accepted and processed. | No action required. |
| **400 Bad Request** | **User Input Error.** A required field was incorrect (e.g., wrong currency code, invalid account number format). | Review the payment details in the **Error Log** and correct the field. |
| **401 Unauthorized** | **Access Denied.** Your user token has expired, or you lack the correct **Role-Based Access Control (RBAC)** permissions. | Log out and log back in, or contact your Administrator to verify permissions. |
| **409 Conflict** | **Duplicate Payment.** The payment system detected this transaction ID has already been successfully processed. | Review the transaction status to confirm the original payment went through. Do not resubmit. |
| **500 Internal Error** | **Service Interruption.** An unexpected error occurred on the QBank Connect server. | Wait 5-10 minutes and check the **System Status** dashboard. If persistent, contact support. |