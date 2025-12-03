# Batch Processing and Cutoff Times

While TreasuryPro provides real-time data, many traditional payments (like ACH transfers) are handled by banks in scheduled Batches. 

## Batch Processing

TreasuryPro collects payments throughout the day and then groups into large files called batches. These batches are sent to the payment network at specific, fixed times during the day.

## Payment Cutoff Time

The Cutoff Time is the deadline by which a payment must be submitted and approved within TreasuryPro for it to be included in the bank's final daily batch.

* **Example:** If the ACH cutoff time is 3:00 PM EST, a payment approved at 3:01 PM EST will be held and included in the following day's batch.

The Cutoff Time is displayed in the **Payment Submission** module. 

> **Note:** ACH payments are always processed in batches, while Wire transfers typically have later or rolling cutoff times due to their immediate nature.