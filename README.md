# Moneris (moneris)

Moneris (Moneris Solutions Corporation) is Canada's largest payment processor and merchant-acquiring company, founded in December 2000 as a joint venture equally owned by Royal Bank of Canada (RBC) and Bank of Montreal (BMO). It is a payment-technology company in the payments-infrastructure layer of Canadian financial services — not a deposit-taking Schedule I bank — serving roughly 325,000 points of commerce and processing close to five billion transactions a year. Moneris runs a public developer portal documenting the Moneris Unified API, a REST/OpenAPI 3.0.3 platform on `api.moneris.io` (production) and `api.sb.moneris.io` (sandbox), secured with OAuth 2.0 client credentials and API keys.

**APIs.json:** [https://raw.githubusercontent.com/api-evangelist/moneris/refs/heads/main/apis.yml](https://raw.githubusercontent.com/api-evangelist/moneris/refs/heads/main/apis.yml)

## Open-Finance Posture

Canada has no operational open-banking mandate; the federal Consumer-Driven Banking (CDB) framework legislated in Budget 2024 / Fall Economic Statement 2024 (overseen by the FCAC) is not yet live. As a payment processor rather than a chartered bank, Moneris is not itself a CDB reporting entity — that obligation falls on its bank owners RBC and BMO. Moneris's public API surface is therefore a commercial, self-serve merchant-payments program, not a consumer data-sharing / FDX interface. Access to production requires tying a Developer Portal account to a recognized Moneris merchant account.

## Tags

- Financial Services
- Payments
- Payment Processing
- Card Payments
- Merchant Services
- Acquiring
- Canada
- Fintech
- Infrastructure

## Timestamps

- **Created:** 2026-07-23
- **Modified:** 2026-07-23

## APIs

All API products below are resource groups of the single Moneris Unified API (OpenAPI 3.0.3, version 2.6.1). Base URL `https://api.moneris.io` (sandbox `https://api.sb.moneris.io`). Authentication is OAuth 2.0 client credentials (fine-grained scopes) or an `X-Api-Key` API key.

### Moneris Payments API

Create, retrieve, list, cancel, complete, and increment card payments — purchase, pre-authorization/completion, incremental authorization, and multiple completions.

- **Human URL:** [https://developer.moneris.com/moneris-api/docs/purchase](https://developer.moneris.com/moneris-api/docs/purchase)
- **Base URL:** `https://api.moneris.io`
- [OpenAPI](openapi/moneris-unified-api-openapi.json)
- [API Reference](https://developer.moneris.com/moneris-api/reference/getpayments)

### Moneris Payment Methods API

Tokenize and manage stored payment methods for purchase-with-token and card-on-file flows.

- **Human URL:** [https://developer.moneris.com/moneris-api/docs/purchase-with-payment-token](https://developer.moneris.com/moneris-api/docs/purchase-with-payment-token)
- **Base URL:** `https://api.moneris.io`
- [OpenAPI](openapi/moneris-unified-api-openapi.json)
- [API Reference](https://developer.moneris.com/moneris-api/reference/getpaymentmethods)

### Moneris Refunds API

Create, retrieve, and list payment refunds and independent refunds.

- **Human URL:** [https://developer.moneris.com/moneris-api/reference/getrefunds](https://developer.moneris.com/moneris-api/reference/getrefunds)
- **Base URL:** `https://api.moneris.io`
- [OpenAPI](openapi/moneris-unified-api-openapi.json)
- [API Reference](https://developer.moneris.com/moneris-api/reference/getrefunds)

### Moneris Subscriptions API

Recurring-billing subscriptions — create, update, pause, resume, extend, cancel — with recurring-payment webhook events.

- **Human URL:** [https://developer.moneris.com/moneris-api/docs/recurring-billing](https://developer.moneris.com/moneris-api/docs/recurring-billing)
- **Base URL:** `https://api.moneris.io`
- [OpenAPI](openapi/moneris-unified-api-openapi.json)
- [API Reference](https://developer.moneris.com/moneris-api/reference/getsubscriptions)

### Moneris Customers API

Create, retrieve, list, update, and delete customer records.

- **Human URL:** [https://developer.moneris.com/moneris-api/reference/getcustomers](https://developer.moneris.com/moneris-api/reference/getcustomers)
- **Base URL:** `https://api.moneris.io`
- [OpenAPI](openapi/moneris-unified-api-openapi.json)
- [API Reference](https://developer.moneris.com/moneris-api/reference/getcustomers)

### Moneris 3-D Secure Authentication API

3-D Secure cardholder authentication (browser and requestor-initiated channels), including authentication value lookup for the challenge flow.

- **Human URL:** [https://developer.moneris.com/moneris-api/docs/3ds-browser](https://developer.moneris.com/moneris-api/docs/3ds-browser)
- **Base URL:** `https://api.moneris.io`
- [OpenAPI](openapi/moneris-unified-api-openapi.json)
- [API Reference](https://developer.moneris.com/moneris-api/reference/createauthentication)

### Moneris Kount Risk Inquiry API

Fraud and risk scoring through Kount — create, list, retrieve, and assert Kount inquiries.

- **Human URL:** [https://developer.moneris.com/moneris-api/docs/risk-inquiry-kount](https://developer.moneris.com/moneris-api/docs/risk-inquiry-kount)
- **Base URL:** `https://api.moneris.io`
- [OpenAPI](openapi/moneris-unified-api-openapi.json)
- [API Reference](https://developer.moneris.com/moneris-api/reference/createkountinquiry)

### Moneris Merchant Onboarding API

Third-party merchant onboarding and updating, terminal & service ordering, order-status tracking, supplies, and product recommendations for partners and ISVs.

- **Human URL:** [https://developer.moneris.com/moneris-api/docs/onboarding-and-updating](https://developer.moneris.com/moneris-api/docs/onboarding-and-updating)
- **Base URL:** `https://api.moneris.io`
- [OpenAPI](openapi/moneris-unified-api-openapi.json)
- [API Reference](https://developer.moneris.com/moneris-api/reference/createmerchant)

### Moneris Multi-Currency Pricing API

Foreign-currency exchange-rate lookup and rate retrieval to lock a rate for a subsequent MCP transaction.

- **Human URL:** [https://developer.moneris.com/moneris-api/docs/multi-currency-pricing](https://developer.moneris.com/moneris-api/docs/multi-currency-pricing)
- **Base URL:** `https://api.moneris.io`
- [OpenAPI](openapi/moneris-unified-api-openapi.json)
- [API Reference](https://developer.moneris.com/moneris-api/reference/mcprate)

### Moneris Disputes API

Chargeback and dispute handling — accept a dispute, retrieve details, upload response documents, and check upload status.

- **Human URL:** [https://developer.moneris.com/moneris-api/reference/getdisputebycaseidandrecordnumber](https://developer.moneris.com/moneris-api/reference/getdisputebycaseidandrecordnumber)
- **Base URL:** `https://api.moneris.io`
- [OpenAPI](openapi/moneris-unified-api-openapi.json)
- [API Reference](https://developer.moneris.com/moneris-api/reference/getdisputebycaseidandrecordnumber)

## Common Properties

- [Website](https://www.moneris.com)
- [Developer Portal](https://developer.moneris.com)
- [Documentation](https://developer.moneris.com/moneris-api/docs/introduction)
- [Registration](https://developer.moneris.com/login)
- [Postman](https://www.postman.com/moneris)
- [GitHub Organization](https://github.com/moneris)
- [LinkedIn](https://www.linkedin.com/company/moneris)
- [Blog](https://www.moneris.com/en/blog)
- [Terms of Service](https://www.moneris.com/en/legal/terms-of-use)
- [Privacy Policy](https://www.moneris.com/en/legal/privacy-policy)
- [Support](https://www.moneris.com/en/support/contact)

## Maintainers

**FN:** Kin Lane
**Email:** kin@apievangelist.com
