# Idempotent Payment Processing

TreasuryPro's payment system is **idempotent**, guaranteeing that a payment request, even if submitted multiple times, is only **executed once** by the bank.

When dealing with API calls over the internet, network connectivity issues can cause a system to resend a request. Without idempotency, a single payment instruction might accidentally result in a duplicate payment being sent.

Idempotency protects against accidental **double-posting** of funds, ensuring the integrity of your ledger and preventing costly manual reconciliations. You only need to check the final status code (e.g., `200 OK` for success) without worrying if a re-submitted request was processed twice.

## How it Works

TreasuryPro uses a unique **Transaction ID (UUID)** for every payment initiated. When the request reaches the bank via QBank Connect, this UUID is checked.
    * If the UUID already exists in the system, the duplicate request is **rejected** with a `409 Conflict` status.
    * If the UUID is new, the payment is **processed**.


