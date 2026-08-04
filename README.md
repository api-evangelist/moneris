# Moneris (moneris)

<!-- API-EVANGELIST-PROVENANCE:BEGIN -->
> ### About this repository
>
> **This is not our API.** This repository is an independent, third-party profile of a company's
> **publicly available** API surface, maintained by [API Evangelist](https://apievangelist.com).
> API Evangelist does not operate, host, resell, or support this company's APIs, and is not
> affiliated with or endorsed by the company unless stated on the profile.
>
> **Where the information came from.** Everything here is assembled from material a member of the
> public can reach with a browser and no credentials — the company's own website, developer portal
> and documentation, the specifications it publishes for public use (OpenAPI, AsyncAPI, JSON Schema,
> `apis.json`, `llms.txt` and similar), its public repositories, and its public status, pricing and
> changelog pages. **Nothing here is obtained by breaching a system, defeating an access control, or
> using credentials of any kind.**
>
> **The rating is an independent assessment.** The Kin Score and Agent Readiness rating are
> independently calculated scores of a company's *public* API artifacts, produced by API Evangelist
> against a published rubric. They are not certifications, endorsements, security assessments, or
> audits, and they score published artifacts — not the quality, safety, or security of the software.
>
> **Corrections, re-scores, and removal are free.** No partnership, contract, or purchase is
> required, and you do not need to justify the request.
>
> - **Something wrong?** Open an issue on this repository, or email
>   [info@apievangelist.com](mailto:info@apievangelist.com).
> - **Published something new?** Ask for a re-score and we will re-run the rating.
> - **Want the listing taken down?** Say so and we will honor it. The profile is reduced to your
>   company name, a factual description, and a link to your own site, and the company is recorded as
>   **unrated** — never scored zero for having asked.
>
> **Response times.** Acknowledgement within **one business day**; removal or restriction within
> **two business days**; corrections and re-scores within **five business days**.
>
> **On a security or compliance team?** Email
> [info@apievangelist.com](mailto:info@apievangelist.com) with *security* in the subject line and
> you will get a person, not a form. We will tell you exactly which public URLs this profile was
> built from so your team can see the same surface we did, and we will take the listing down on
> request while you work through it.
>
> Full detail: **[Where this data comes from](https://apievangelist.com/about/where-our-data-comes-from)**
<!-- API-EVANGELIST-PROVENANCE:END -->

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
