# Plooto (plooto)

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
