# Plooto (plooto)

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

Plooto is a Toronto-based payments automation company (founded 2015 by Hamed Abbasi and Serguei Kloubkov) that helps small and medium businesses and accounting firms automate domestic and international accounts payable and accounts receivable. Its cloud platform unifies bill pay, approval workflows, supplier and customer payments, reconciliation, and reporting across Canadian EFT, US ACH, credit card, and cross-border rails, syncing two-way with QuickBooks Online, Xero, and NetSuite. Plooto is a licensed money services business in its home market of Canada, working with Tier 1 banks and processing partners.

**APIs.json:** [https://raw.githubusercontent.com/api-evangelist/plooto/refs/heads/main/apis.yml](https://raw.githubusercontent.com/api-evangelist/plooto/refs/heads/main/apis.yml)

## API Posture (honest)

Plooto is **integration-led, not API-platform-led**. A real first-party backend gateway exists at `https://api.plooto.com` (its root returns HTTP 204 and unknown paths return structured JSON errors) that powers the Plooto app and its accounting connectors — but Plooto does **not** publish a public, self-serve developer portal, downloadable OpenAPI/Swagger specification, or public API reference.

- No live developer portal — `developer.plooto.com` / `docs.plooto.com` do not resolve; `www.plooto.com` developer paths sit behind a Cloudflare bot wall (403); the gateway's own referenced docs host `support.plooto.co/docs` returns 530 (dead).
- No downloadable OpenAPI/Swagger — every spec probe against the gateway returned 404. Zero specs harvested.
- No public auth discovery — `/.well-known/openid-configuration` and `/.well-known/oauth-authorization-server` return 404.
- No first-party public Postman collection, GraphQL, gRPC, or AsyncAPI was found.

Plooto's verifiable integration surface for outside builders is its pre-built two-way accounting connectors (QuickBooks Online, Xero, NetSuite) plus a **gated partner onboarding** process. Third-party aggregators (Apideck / API Tracker) advertise "OpenAPI/webhooks/sandbox" for Plooto, but no first-party specification substantiates them, so they are not trusted here.

See [`review.yml`](review.yml) for the full reviewer findings and probe log.

## Tags

- Payments
- Canada
- Accounts Payable
- Accounts Receivable
- AP Automation
- AR Automation
- Bill Pay
- Money Transfer
- EFT
- ACH
- Cross-Border
- SMB

## Timestamps

- **Created:** 2026-07-24
- **Modified:** 2026-07-24

## APIs

No public, self-serve, documented API is available. See the API Posture section above.

## Common Properties

- [Website](https://www.plooto.com/)
- [Blog](https://www.plooto.com/blog)
- [Help Center](https://plooto.my.site.com/support/)
- [Pricing](https://www.plooto.com/pricing)
- [Security](https://www.plooto.com/plooto-security)
- [Terms of Service](https://www.plooto.com/terms-and-conditions)
- [Privacy Policy](https://www.plooto.com/privacy-policy)
- [LinkedIn](https://ca.linkedin.com/company/plooto)

## Maintainers

**FN:** Kin Lane
**Email:** kin@apievangelist.com
