---
name: Create and manage a recurring subscription
description: Create a Moneris recurring-billing subscription with a webhook callback, then pause, resume, extend, or cancel it.
api: openapi/moneris-unified-api-openapi.json
operations: [createSubscriptions, getSubscription, updateSubscription, pauseSubscription, resumeSubscription, extendSubscription, cancelSubscription]
---

# Create and manage a recurring subscription (Moneris Unified API)

Use this flow for fixed-schedule recurring billing against a stored payment
method.

## Auth & required headers
- OAuth token with `scope=payment.write customer.write`; send
  `Authorization: Bearer <token>` plus `Api-Version`, `X-Merchant-Id`,
  `Accept-Language`.

## Steps
1. **Create the subscription** — `createSubscriptions` (`POST /subscriptions`)
   with the `paymentMethodId`, amount, interval/frequency, number of recurs, and
   a `callbackUrl` to receive webhook events. Include an `idempotencyKey`.
2. **Receive webhooks** — Moneris POSTs a `RECURRING_PAYMENT_CONFIRMED` event to
   your `callbackUrl` on each successful billing (envelope in
   asyncapi/moneris-subscriptions-webhooks.yml). Use `eventId` for
   dedupe/idempotency; return `200 OK`.
3. **Manage the series**:
   - Pause: `pauseSubscription` (`POST /subscriptions/{subscription-id}/pause`).
   - Resume: `resumeSubscription` (`POST /subscriptions/{subscription-id}/resume`).
   - Extend: `extendSubscription` (`POST /subscriptions/{subscription-id}/extend`)
     to add more recurs (positive only).
   - Update amount/details: `updateSubscription`
     (`PATCH /subscriptions/{subscription-id}`).
   - Cancel: `cancelSubscription` (`POST /subscriptions/{subscription-id}/cancel`).
4. **Inspect** — `getSubscription` (`GET /subscriptions/{subscription-id}`).

## Rules
- The schedule interval/frequency cannot be changed after creation; extend or
  pause instead. For irregular intervals use the Payment endpoint per charge.
- While paused, remaining recurs still decrement over time.
- Set a unique `idempotencyKey` on writes (409 on replay); errors are RFC 7807.
