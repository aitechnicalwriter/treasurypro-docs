# 🆘 Troubleshooting QBank Connect Errors

This guide helps you diagnose common API-related user errors, such as payment failures and data sync issues, without needing to contact support immediately.

## Step 1: Check System Status
1. Look at the **QBank Connect Status Indicator** in the footer of the TreasuryPro dashboard.
    * If the indicator is **Red**, there is an active service interruption; no action is needed until the system recovers.

## Step 2: Review the Error Log
1. If the status is Green but a payment failed, navigate to **Payments** > **Error Log**.
2. Locate the failed payment by Transaction ID.
3. Review the **Error Code**. Common user-resolvable codes are:
    * **400 (Bad Request):** Indicates an invalid data field (e.g., incorrect currency code or character limit exceeded).

## Step 3: Correct Data and Resubmit
1. If the error is **400**, click the **Edit Payload** button.
2. Correct the invalid field (e.g., change `USDollar` to the correct `USD` ISO code).
3. Click **Resubmit**. The corrected payload is sent back to QBank Connect for processing.