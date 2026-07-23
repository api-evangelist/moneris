---
name: Pre-authorize, complete, and refund a payment
description: Place a temporary hold with a pre-authorization, capture it with a completion, and issue a refund on the Moneris Unified API.
api: openapi/moneris-unified-api-openapi.json
operations: [createPayments, incrementPayment, completePayment, createRefund, getPayment]
---

# Pre-authorize, complete, and refund (Moneris Unified API)

Use this two-step flow when the final amount is not known at authorization time
(hospitality, rentals, deposits).

## Auth & required headers
- OAuth token with `scope=payment.write refund.write`; send
  `Authorization: Bearer <token>` plus `Api-Version`, `X-Merchant-Id`,
  `Accept-Language`.

## Steps
1. **Pre-authorize** — `createPayments` (`POST /payments`) with
   `automaticCapture: false` to place a temporary hold (valid 7-31 days). Keep
   the payment `id`. Include an `idempotencyKey`.
2. **(Optional) Increase the hold** — `incrementPayment`
   (`POST /payments/{payment-id}/increment`) to raise the held amount on an
   estimated authorization.
3. **Capture** — `completePayment` (`POST /payments/{payment-id}/complete`) with
   the final amount (may be less than the hold, within card-brand variance).
4. **Refund** — `createRefund` (`POST /refunds`) referencing the `paymentId` for
   a payment refund (no payment method needed).
5. **Confirm** — `getPayment` (`GET /payments/{payment-id}`).

## Rules
- Until captured, a pre-authorization stays eligible for `cancelPayment`.
- Set a unique `idempotencyKey` on every write (409 on replay).
- Sandbox: use the Penny Value Simulator to force declines
  (see sandbox/moneris-sandbox.yml); errors are RFC 7807 Problem JSON.
