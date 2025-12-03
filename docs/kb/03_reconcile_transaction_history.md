How to Reconcile Transaction History (Batch-Latent Data)
This guide explains how to use the detailed transaction history for daily auditing and reconciliation. Remember that this data is Batch-Latent, meaning it updates once per day.
Step 1: Access the Transaction History Report
From the Real-Time Cash Positioning dashboard:
Select the Account: Click on the account you wish to reconcile.
View History: Navigate to the "Detailed Transaction History" tab, which displays transactions dating back to the start of the previous business day.
Step 2: Use the Posting Date Filter
For accurate, auditable daily reconciliation, it is critical to filter the report using the Posting Date field, not the transaction date.
Locate Filters: Find the date range or filtering options above the transaction list.
Apply Posting Date: Set the filter to search by Posting Date and select the previous business day's date.
Reason: The Posting Date reflects the date the transaction record was synchronized by the QBank Connect mETL engine (after 1:00 am). By filtering on yesterday's Posting Date, you ensure you are viewing only fully reconciled and final records.
Run Report: Click "Apply" or "Run Report" to refresh the list with synchronized data.
Step 3: Compare Balances and History
The goal of reconciliation is to match the transaction history received via the API to your internal ERP records and verify the figures against the bank's final Ledger Balance.
Verify Opening Balance: Ensure the Ledger Balance from the prior day matches your ERP's closing cash position for that date.
Match Transactions: Cross-reference the individual transaction entries from the QBank Connect report with the transactions logged in your ERP system.
Use Date Fields: If there are discrepancies, use the three date fields provided by QBank Connect (transaction_date, value_date, and posting_date) to clarify timing, as explained in the Architecture Overview. The posting_date is the final authority for synchronized records.
Confirm Closure: Once all entries for the previous day are matched, your daily cash position is considered fully reconciled and ready for internal accounting closure.

---

# Alternative Content

# 🔄 How to Reconcile Transaction History (Batch-Latent Data)

While TreasuryPro provides real-time cash positioning, regulatory compliance and auditing require reconciliation against final, batch-processed bank statements (End-of-Day or EOD data). This guide shows you how to use batch-latent data for reconciliation.

## Understanding Batch-Latent Data

Batch-latent data refers to transaction records received in large, scheduled data dumps (e.g., MT940 files). This data is typically considered the *official* record for accounting purposes.

---

## Step 1: Generate the Reconciliation Report

1.  Navigate to the **Reports** module in the main TreasuryPro navigation.
2.  Select **GL Reconciliation** from the report category menu.
3.  Set the following parameters:
    * **Date Range:** Select the month or quarter you wish to reconcile.
    * **Data Source:** Select **EOD Statement Data** (ensuring you are not using the Intraday Feed).
4.  Click **Generate Report**.

## Step 2: Compare and Flag Discrepancies

1.  The report will display two main columns: **Booked Balance** (from EOD files) and **Intraday Final Balance** (from the QBank Connect feed).
2.  Any row where the balances differ by more than \$0.01 is automatically flagged in red.
3.  Click the **Flag as Discrepancy** button next to the row to open a ticket in your internal tracking system for further investigation by the operations team.

> **Note:** The majority of discrepancies are caused by transactions that were initiated intraday but settled on the following business day.