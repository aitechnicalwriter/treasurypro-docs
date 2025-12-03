# TreasuryPro Release Notes

## November 20, 2025: Version 2.2.0

This update introduces major enhancements to the Cash Management module, improving efficiency and data accuracy.

---

## What's New

### **Real-Time Status Indicators**
We have added a new status indicator to the **Payment Submission** screen. This provides immediate feedback on whether your submitted payment batch has been accepted by QBank Connect and is now processing, eliminating the need to check status logs manually.

* **Location:** Payment Submission Screen, under the Batch ID column.
* **Benefit:** Saves time and provides confidence in payment initiation.

### **Simplified Account Linking**
The process for linking new bank accounts via QBank Connect has been simplified to a three-step wizard, reducing the average setup time by 40%.

* **Location:** System Settings > Bank Account Configuration.
* **Benefit:** Faster onboarding of new banking partners and subsidiaries.

---

## Fixes and Improvements

| Issue Area | Description |
| :--- | :--- |
| **Reporting** | Fixed an issue where the Quarterly Liquidity Report sometimes failed to include accounts with zero activity. |
| **Dashboard** | Resolved a bug causing the **Intraday Available Balance** widget to temporarily show stale data if the network connection was briefly interrupted. Data now recovers instantly upon reconnection. |
| **API** | Improved error messaging for failed payment submissions due to invalid character limits in beneficiary fields. |


## November 6, 2025: Version 2.1.3

We upgraded your cash management features, powered by our partner, QBank Connect. These updates provide faster fund access and simpler auditing.

### 1. ⚡ New Payment Speed: Instant Transfers (Real-Time Payments)
You now have access to Real-Time Payments (RTP), a new payment option for urgent and high-value transfers.

#### What’s New for You?
- **Instant Confirmation**: When you submit a payment using the new Instant Transfer option, you receive immediate, guaranteed confirmation within seconds. This removes any uncertainty about whether the funds were successfully sent.
- **24/7/365 Availability**: Instant Transfers can be initiated and settled at any time, including nights, weekends, and holidays.
- **Irreversible Guarantee**: Once you receive the "Posted Success" status in your ERP, the payment is guaranteed to be settled in the recipient's account.

#### Where to Find It?
Look for the new "Instant Transfer (RTP)" option in the payment method dropdown when initiating a high-priority transfer or wire payment.
    Tip: Use Instant Transfer when you need to confirm a large payment has landed immediately, such as closing a last-minute deal or covering an urgent liability.

### 2. Automated Statement Image Retrieval
You no longer need to manually log into a separate QBank portal to download and file your monthly bank statements. TreasuryPro can now retrieve official statement PDFs automatically.

#### What’s New for You?
- **One-Click Auditing**: The new Statement Archive feature in your ERP provides a direct link to the official, monthly PDF statement image from QBank.
- **Simpler Reconciliation**: Easily access historical statements for audit trails without leaving your ERP environment.
- **Faster Access**: Statements are available immediately after the bank finalizes the month-end process.

#### Where to Find It?
Navigate to the Reporting or Document Archive module. You will find a new section titled "Bank Statement Images" where you can select the month and account to retrieve the PDF.

