# Moneris

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
> **Not from the company, and here with a question?** You are welcome here — we would rather be the
> front line and point you the right way than have a good report go nowhere. What this repository
> can answer is narrow, though, so it is worth knowing who you are actually looking for:
>
> - **A question about how the API works, an account, billing, or a bug in the service** — that is
>   the company's own support, not us. We profile this API; we do not operate it and cannot see
>   your account.
> - **A bug in an open-source project we only catalog** — file it on that project's own repository.
>   This has happened with a real and correct bug report that reached us instead of the people who
>   could fix it, which helped nobody.
> - **Anything about this listing itself** — the description, the tags, the rating, a missing or
>   wrong artifact — is ours. Open an issue here.
> - **Not sure, or something general about API Evangelist or APIs.io** — open an issue on the
>   [APIs.io Inbox](https://github.com/api-search/inbox) and we will route it.
>
> **This repository contains no software, and we will never ask you to download anything.** There is
> no build, release, installer, or binary here — only text and machine-readable API descriptions, so
> there is nothing here that can be "corrupt" or need "repairing". Any issue, comment, or email
> claiming otherwise and offering a download link is not from us and is hostile. Do not follow the
> link; it is a lure. Report it to GitHub and, if you like, tell us at
> [info@apievangelist.com](mailto:info@apievangelist.com) so we can take it down.
>
> **On a security or compliance team?** Email
> [info@apievangelist.com](mailto:info@apievangelist.com) with *security* in the subject line and
> you will get a person, not a form. We will tell you exactly which public URLs this profile was
> built from so your team can see the same surface we did, and we will take the listing down on
> request while you work through it.
>
> Full detail: **[Where this data comes from](https://apievangelist.com/about/where-our-data-comes-from)**
<!-- API-EVANGELIST-PROVENANCE:END -->

Moneris (Moneris Solutions Corporation) is Canada's largest payment processor and merchant-acquiring company, founded in December 2000 as a joint venture equally owned by Royal Bank of Canada (RBC) and Bank of Montreal (BMO). It is a payment-technology and card-acquiring company rather than a deposit-taking Schedule I bank, sitting in the payments-infrastructure layer of Canadian financial services: it serves roughly 325,000 points of commerce, processes close to five billion transactions a year, and handles on the order of one in three Canadian card transactions. In 2025-2026 RBC and BMO explored a sale of the venture, with Francisco Partners (owner of Verifone) reported as the lead buyer. Unlike its bank owners, Moneris is not subject to Canada's coming Consumer-Driven Banking framework; its "open" surface is a commercial, self-serve first-party developer program. Moneris runs a real, public developer portal at developer.moneris.com documenting the Moneris Unified API (REST, OpenAPI 3.0.3, hosts api.moneris.io production / api.sb.moneris.io sandbox) covering payments, tokenized payment methods, refunds, recurring billing/subscriptions, 3-D Secure, Kount fraud/risk, disputes, multi-currency pricing, and third-party merchant onboarding, secured with OAuth 2.0 client credentials and API keys, with a published Postman workspace.

**Areas:** Financial Services · Payments · Payment Processing · Card Payments · Merchant Services · Acquiring · Canada · Fintech · Infrastructure

## Moneris on APIs.io

Everything profiled for Moneris is published on APIs.io rather than in this repository. Start at the provider page — **[apis.io/providers/moneris/](https://apis.io/providers/moneris/)** — or go straight to one of the APIs or properties below.

### APIs (15)

- [Moneris 3D Secure API](https://apis.io/apis/moneris/moneris-3d-secure-api/) — Perform 3D Secure authentications against payment methods
- [Moneris Customers API](https://apis.io/apis/moneris/moneris-customers-api/) — Perform and Manage customers
- [Moneris Disputes API](https://apis.io/apis/moneris/moneris-disputes-api/) — Perform and Manage Disputes
- [Moneris Installments API](https://apis.io/apis/moneris/moneris-installments-api/) — Perform and Manage Installments
- [Moneris Kount API](https://apis.io/apis/moneris/moneris-kount-api/) — Perform and Manage Kount risk assessment inquiries
- [Moneris Merchant Onboarding API](https://apis.io/apis/moneris/moneris-merchant-onboarding-api/) — Manage Merchants onboarding
- [Moneris Multi-Currency Pricing Rate Lookup API](https://apis.io/apis/moneris/moneris-multi-currency-pricing-rate-lookup-api/) — Retrieve Multi-Currency Pricing Rate Lookups
- [Moneris Payment Methods API](https://apis.io/apis/moneris/moneris-payment-methods-api/) — Create and Manage payment methods
- [Moneris Payments API](https://apis.io/apis/moneris/moneris-payments-api/) — Perform and Manage payments
- [Moneris Products API](https://apis.io/apis/moneris/moneris-products-api/) — Product recommendations
- [Moneris Refunds API](https://apis.io/apis/moneris/moneris-refunds-api/) — Perform and Manage payment refunds
- [Moneris Subscriptions API](https://apis.io/apis/moneris/moneris-subscriptions-api/) — Perform and Manage Subscriptions
- [Moneris Surcharge Lookup API](https://apis.io/apis/moneris/moneris-surcharge-lookup-api/) — The Surcharge Lookup API from Moneris — 1 operation(s) for surcharge lookup.
- [Moneris Terminal & Service Orders API](https://apis.io/apis/moneris/moneris-terminal-service-orders-api/) — Manage Moneris Terminal & Service Orders
- [Moneris Validations API](https://apis.io/apis/moneris/moneris-validations-api/) — Perform and Manage card validations

### Published properties

Each property below is a page on APIs.io carrying the machine-readable artifact and what it says.

#### AsyncAPI (1)

Event-driven and webhook contracts.

- [Moneris Subscriptions Webhooks](https://apis.io/asyncapis/moneris/moneris-subscriptions-webhooks/)

#### MCP servers (1)

Model Context Protocol servers that expose the API to agents.

- [moneris](https://apis.io/servers/moneris/moneris/)

#### Agentic access (1)

Which operations an agent can call, which act, and which need a human in the loop.

- [Moneris Agentic Access](https://apis.io/agentic-access/moneris/moneris-agentic-access/)

#### Collections (1)

Postman and Open Collection request collections.

- [Moneris API](https://apis.io/collections/moneris/open-moneris-unified-api/)

#### Overlays (1)

OpenAPI overlays, including conversational phrasing for each operation.

- [Moneris Unified Api Overlay](https://apis.io/overlays/moneris/moneris-unified-api-overlay/)

#### Security (2)

Authentication, trust centre, and vulnerability disclosure.

- [Moneris Authentication](https://apis.io/security/moneris/moneris-authentication/)
- [Moneris Domain Security](https://apis.io/security/moneris/moneris-domain-security/)

#### OAuth scopes (1)

The permissions the API asks for.

- [Moneris Scopes](https://apis.io/scopes/moneris/moneris-scopes/)

## Where to find this API

Links to the company's own pages. This repository publishes no copy of their specifications — the canonical document is theirs and lives at the URLs below.

- [Website](https://www.moneris.com)
- [Documentation](https://developer.moneris.com/moneris-api/docs/introduction)
- [Getting started](https://developer.moneris.com/moneris-api/docs/getting-started-guide)
- [Sign up](https://developer.moneris.com/login)
- [Support](https://www.moneris.com/en/support/contact)
- [Changelog](https://developer.moneris.com/changelog)
- [Blog](https://www.moneris.com/en/blog)
- [Compliance](https://www.moneris.com/en/support/compliance-and-security/pci-data-security)
- [Terms of service](https://www.moneris.com/en/legal/terms-of-use)
- [Privacy policy](https://www.moneris.com/en/legal/privacy-policy)
- [GitHub](https://github.com/moneris)
- [Status](https://status.moneris.com)

## API Evangelist rating

**Kin Score 41.7** — developing · rubric 0.25.0 · scored 2026-10-23

| Facet | Score |
|---|---|
| Discoverability | 75.0 |
| Contract quality | 61.0 |
| Contract governance | 18.2 |
| Operational transparency | 34.2 |
| Developer ergonomics | 45.8 |
| Access clarity | 6.6 |

**Agent readiness 55.2** — agent-native

| Agent-readiness dimension | Result |
|---|---|
| Spec Presence | yes |
| Agentic Access | derived (partial credit) |
| Reversibility Documented | documented (partial credit) |
| MCP Server | verified |
| Auth Clarity | bearer (partial credit) |
| Idempotency | verified |
| Error Semantics | verified |
| OpenAPI Examples | partial |
| Rate Limit Signal | verified |
| Event Surface Described | yes |
| Agent Skills | derived (partial credit) |
| Well Known Catalog | — |
| Consent Identity | — |
| Agent Card | — |
| Dry Run Mode | — |
| Delegated Identity | — |
| Protected Resource Metadata | — |
| Dynamic Client Registration | — |
| Agentic Commerce | — |
| Pagination Ratio | paginated |
| Operation Distinctiveness | distinct |

**Regulatory alignment 36.6** — Payments

The rubric is published at [github.com/api-evangelist/kin-score](https://github.com/api-evangelist/kin-score). The per-check breakdown behind these numbers — which checks were earned, partial or missed — along with score history and how this provider compares to its peers, is available at [apis.io/providers/moneris/](https://apis.io/providers/moneris/).

## How this profile is made

API Evangelist profiles a company's public API surface the way a developer would find it: the website, developer portal and documentation, the specifications it publishes, its public repositories, and its pricing, status and changelog pages. From that it derives the properties above — contracts split per API, workflows, schemas, collections, governance rules, plans and rate limits — and scores them against the published [Kin Score rubric](https://github.com/api-evangelist/kin-score).

The artifacts are published on [APIs.io](https://apis.io), not in this repository. This repository is the public record for Moneris: the place to say something is wrong, missing or out of date, and to ask for a re-score or a removal.

## Open an issue

- **Something about this listing** — a wrong description, a missing API, a stale artifact or a question about the rating: [open an issue on this repository](https://github.com/api-evangelist/moneris/issues/new).
- **A new API, or one that is not in the catalog yet** — [submit it on APIs.io](https://apis.io/add/).
- **Anything else** — [the APIs.io inbox](https://github.com/api-search/inbox/issues/new) or [info@apievangelist.com](mailto:info@apievangelist.com).
