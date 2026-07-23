---
name: Create a customer and charge them
description: Create a Moneris customer, store a payment method, and process a purchase that authorizes and captures funds in one step.
api: openapi/moneris-unified-api-openapi.json
operations: [createCustomers, createPaymentMethod, createPayments, getPayment]
---

# Create a customer and charge them (Moneris Unified API)

Use this flow to onboard a customer, attach a stored payment method, and take a
purchase payment.

## Auth & required headers
- Get an OAuth 2.0 access token: `POST /oauth2/token` with
  `grant_type=client_credentials`, `client_id`, `client_secret`, and
  `scope=customer.write payment.write`. Send it as `Authorization: Bearer <token>`.
- Every call also requires `Api-Version` (date, e.g. `2024-09-17`),
  `X-Merchant-Id`, and `Accept-Language`.

## Steps
1. **Create the customer** — `createCustomers` (`POST /customers`). Supply name,
   email, and contact details. Keep the returned customer `id`.
2. **Store a payment method** — `createPaymentMethod`
   (`POST /payment-methods`). Prefer a Hosted-Tokenization temporary token or a
   Vault permanent token over raw PAN so you stay out of PCI scope. Keep the
   returned payment method `id`.
3. **Process the purchase** — `createPayments` (`POST /payments`) with the
   `paymentMethodId`, `amount`, `currencyCode` (e.g. `CAD`), and
   `automaticCapture: true` to authorize and capture in one call. Include an
   `idempotencyKey` so a retried request cannot double-charge.
4. **Confirm** — read `getPayment` (`GET /payments/{payment-id}`) and check the
   status plus the ISO response code.

## Rules
- **Idempotency**: set a unique `idempotencyKey` on `createPayments`; a replay
  with the same key returns HTTP 409 instead of a second charge
  (see conventions/moneris-conventions.yml).
- **Errors**: 4xx/5xx bodies are RFC 7807 Problem JSON
  (see errors/moneris-problem-types.yml); transaction declines carry ISO codes
  (see errors/moneris-decline-codes.yml).
- **Sandbox**: use `https://api.sb.moneris.io`; the cent value of `amount` picks
  the response code via the Penny Value Simulator
  (see sandbox/moneris-sandbox.yml).
