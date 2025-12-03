```markdown
# How to Check Your Intraday Available Balance
This guide shows you how to get the most accurate, real-time snapshot of the funds available for use today.

## Step 1: Navigate to the Cash Positioning Dashboard
From your main ERP menu, locate and click the "Treasury" or "Cash Management" tab, and then select "Real-Time Cash Positioning."

## Step 2: Select the Target Account
In the Cash Positioning dashboard, you will see a list of all bank accounts linked to your ERP system through QBank Connect.
1. Locate Account: Use the search bar or filters (e.g., by Account Name or Account Number) to find the specific account you wish to review.
2. View Balance Panel: Click on the account name. A dedicated panel will load, displaying the following figures:
    - Available Balance: This is the real-time amount you have available to spend today. This figure reflects all pending debits and credits that have cleared, as well as any holds.
    - Ledger Balance: This is the technical balance that reflects transactions as of the last nightly cutoff (e.g., yesterday's closing balance).

## Step 3: Refresh the Data
To ensure the Available Balance is the most current number, you must manually trigger a fetch request from the bank.
1. Locate Refresh Button: Find the Refresh button (often represented by a circular arrow icon ) located near the Available Balance figure.
2. Click Refresh: Click the button. The system will send an immediate call to the QBank Connect /balances endpoint.
3. Confirm Timestamp: Once the data is updated, a timestamp will confirm the last successful data retrieval (e.g., "Last Updated: Today at 1:25 PM").

---

# Alternative Content

# 🔍 How to Check Your Intraday Available Balance

This guide explains how to view your real-time available cash balance across all integrated bank accounts using the TreasuryPro dashboard.

## Prerequisites

* You must have **Viewer** or **Controller** permissions for the Cash Management module.
* Your accounts must be connected to **QBank Connect** for real-time feed updates.

---

## Step 1: Access the Dashboard

1.  Log into your TreasuryPro application.
2.  From the primary navigation menu on the left, select the **Cash Management** icon (often represented by a piggy bank or money icon).
3.  The **Cash Overview Dashboard** will load, displaying summary widgets for all accounts.

## Step 2: Locate the Available Balance Widget

1.  Scroll down to the section labeled **Intraday Liquidity Position**.
2.  The top metric in this section is **Total Available Balance**. This figure is updated every 60 seconds based on the latest transactions received via QBank Connect.

## Step 3: View Account-Specific Details

1.  To drill down into a specific account, click the **View Details** button located in the bottom-right corner of the **Intraday Liquidity Position** widget.
2.  A table will expand, showing line-by-line data for each bank account. The most important columns are:
    * **Booked Balance:** The balance as of the last End-of-Day report.
    * **Pending Adjustments:** Total value of transactions confirmed but not yet settled.
    * **Intraday Available Balance:** (Booked Balance + Pending Adjustments). This is your true real-time usable cash.

## Troubleshooting

If the **Intraday Available Balance** is not updating, please verify your **QBank Connect** status under the System Settings menu.
```
