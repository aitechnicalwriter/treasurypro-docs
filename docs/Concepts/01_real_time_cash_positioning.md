```markdown
# Real-Time Cash Positioning
## Understanding Real-Time Cash Positioning
The Real-Time Cash Positioning dashboard is a critical feature within your ERP software, giving you an immediate, accurate view of your company's available funds across all QBank accounts.
This feature is unique because it combines two different types of financial data, which is essential for making smart intraday decisions:

### 1. Instant Funds (Real-Time Data)
When you look at your Available Balance on the Cash Positioning dashboard, that number is fetched directly from QBank's core system the moment you refresh the page.
Endpoint Used: This relies on the QBank Connect /balances endpoint.
Best For: Making immediate decisions, such as confirming funds for a large wire transfer or ensuring a check won't cause an overdraft. This data is the most current and can be refreshed multiple times per hour.

### 2. Reconciliation and Auditing (Batch-Latent Data)
The detailed Transaction History visible below the balance is used for daily reconciliation, auditing, and reporting.
Endpoint Used: This relies on the QBank Connect /transactions endpoint.
Data Latency: Since transactional records (like checks cleared or ACH debits) are processed through the bank's end-of-day batch processing, the history you view is updated only once per day, typically after 1:00 am (the nightly cutoff).
Best For: Month-end closing, regulatory reporting, and confirming past activity.

## The Core Concept: Data Cutoff
The most important thing to remember is the daily data cutoff. Any transactions that occur today (for instance, an ACH payment initiated this morning) will not appear in your detailed Transaction History until tomorrow morning after the nightly data synchronization. The only way to see today's impact is through the Available Balance figure.

---

# alternative content

# 💰 Real-Time Cash Positioning: A Core TreasuryPro Concept

Real-Time Cash Positioning is the capability to view your company’s global cash balances and transactions as they occur, providing an immediate, accurate snapshot of liquidity. This is fundamental to **TreasuryPro's** value proposition, allowing treasury professionals to make informed decisions about funding and investment quickly.

---

## Why Real-Time Data Matters

Traditional cash positioning relies on end-of-day bank files, which creates a significant time delay (a cash blind spot). Real-Time Cash Positioning eliminates this lag by integrating directly with QBank and other financial institutions via the **QBank Connect API**.

| Old Method (End-of-Day) | TreasuryPro Real-Time Positioning |
| :--- | :--- |
| **Data Latency:** 12-24 hours | **Data Latency:** Seconds |
| **Decision Impact:** Reactive | **Decision Impact:** Proactive |
| **Risk:** Increased overdraft/idle cash risk | **Risk:** Optimized liquidity management |

## Key Components

The system relies on three core components working together:

1.  **QBank Connect:** Our primary API integration layer that ingests transaction feeds directly from QBank as they are processed.
2.  **Intraday Ledger:** A continuously updated ledger that aggregates and normalizes real-time data from all connected accounts.
3.  **Liquidity Forecast Engine:** Uses the real-time data to generate precise, hourly liquidity forecasts, allowing for immediate action.

By understanding the real-time cash position, users gain the ability to **maximize investment returns** and **minimize borrowing costs** with unparalleled speed.
```
