# Brown & Brown (brown-brown)

Brown & Brown, Inc. (NYSE: BRO) is a Daytona Beach, Florida headquartered insurance brokerage and risk-management intermediary founded in 1939, and one of the largest independent brokers in the United States. Following the 2025 acquisition of Accession Risk Management Group (Risk Strategies and One80 Intermediaries), it reports through two segments: Retail — property and casualty insurance, employee benefits, private client, captive solutions and financial/wealth services — and Specialty Distribution — programs, wholesale brokerage and MGA/binding-authority businesses including Arrowhead. As a distributor rather than a carrier, Brown & Brown places risk with insurers instead of underwriting it.

**APIs.json:** [https://raw.githubusercontent.com/api-evangelist/brown-brown/refs/heads/main/apis.yml](https://raw.githubusercontent.com/api-evangelist/brown-brown/refs/heads/main/apis.yml)

## Tags

- Insurance
- United States
- Broker
- Property and Casualty
- Employee Benefits
- Wholesale Brokerage
- Managing General Agent
- Risk Management
- Agency Management
- Partner Gated

## Timestamps

- **Created:** 2026-07-25
- **Modified:** 2026-07-25

## APIs

**None.** Brown & Brown publishes no public, self-serve API and no developer portal.

This is not an omission in the profile — it is the finding. The United States has no federal insurance regulator and no open-insurance mandate, so nothing compels a broker or carrier to publish an interface. Brown & Brown is a clean confirmation of what that produces: the fifth-largest US independent brokerage, $1.9 billion in Q1 2026 revenue, and zero public API surface.

### What was probed

- `developer.bbrown.com`, `developers.bbrown.com`, `docs.bbrown.com`, `api.bbrown.com`, `apis.bbrown.com`, `portal.bbrown.com` — **none resolve in DNS**.
- `/developers`, `/developer`, `/api`, `/partners`, `/integrations` on both `bbrown.com` and `us.bbrown.com` — **all 404**.
- `/.well-known/security.txt`, `/.well-known/openid-configuration`, `/.well-known/oauth-authorization-server` — **all 404**.
- Roughly 35 `bbrown.com` subdomains enumerated. Every application host is a login wall: `ratings.bbrown.com` redirects to Microsoft Entra ID, `accidentclaims.bbrown.com` is a third-party (ABL Group) claimant login, `cyberapp.bbrown.com` is a Centraleyes GRC tenant, `bbwrite.bbrown.com` and `legalentity.bbrown.com` are Cloudflare-challenged. None carries reference documentation.

### The one real programmatic surface — partner-gated

Arrowhead Programs, part of Brown & Brown's Specialty Distribution segment (now branded within Arrowhead Intermediaries alongside Bridge Specialty Group and One80 Intermediaries), operates an **Enterprise API (EAPI)** layered over the Arrowhead Exchange agent platform. It is a **quote** integration, delivered by commercial agreement to comparative raters and aggregators — CoverHound, Tarmika, Semsee, DAIS. It is not consumer-facing, not self-serve, and has no public documentation, base URL or specification.

`api.arrowheadexchange.com` resolves behind Cloudflare but returns **404 for the root and for every probed spec path** (`/openapi.json`, `/openapi.yaml`, `/swagger.json`, `/swagger/v1/swagger.json`, `/v1/openapi.json`, `/api-docs`, `/docs`, `/spec`, `/redoc`, `/swagger`, `/.well-known/openid-configuration`). A gateway exists; nothing public is served from it.

### ACORD posture

**No ACORD reference published; exchange runs via Vertafore AMS360 / IVANS agency download.**

No mention of ACORD, AL3, ACORD XML, ACORD certification or NGDS appears on any Brown & Brown first-party property, or in the Arrowhead API material. The company's actual carrier data exchange runs where it runs for essentially all US retail brokerage — through the agency management system layer. Brown & Brown is a publicly referenced Vertafore AMS360 agency (Vertafore, May 2025), and AMS360-class systems carry carrier policy download over IVANS in ACORD AL3 / ACORD XML. That plumbing belongs to the AMS vendor and the carriers, not to an interface Brown & Brown publishes.

### Quote / bind / issue / FNOL

| Verb | Exposed | Audience |
| --- | --- | --- |
| Quote | Yes | Partner-only (Arrowhead EAPI via aggregators) |
| Bind | No | — |
| Issue | No | — |
| FNOL | No | Gated portals and the carriers on whose paper the risk sits |

### Auth, webhooks, SDKs

No public API means no published authentication scheme. Observed portal auth is OIDC/SAML federation to Microsoft Entra ID plus separate third-party vendor logins. No webhook catalog, no AsyncAPI, no GraphQL endpoint, no published `.proto`, no public Postman workspace, no first-party SDKs.

### Technology signal

On **July 23, 2026** Brown & Brown announced an AI-first transformation with **Anthropic, McKinsey & Company and Accenture** — deploying Claude across 23,000 teammates and Claude Code across the entire software engineering organization, with a value management office for governance and ROI. This is internal adoption. As of this record it has produced no external API, developer portal or agent-facing surface, which makes Brown & Brown a company worth re-probing.

## Artifacts

Everything spec-dependent is absent because there is no spec. What is here is probe evidence:

- [`well-known/brown-brown-well-known.yml`](well-known/brown-brown-well-known.yml) — discovery-surface record. No `/.well-known/` document of any kind, no `llms.txt` (the `/llms.txt` 200 is a HubSpot 301 to the homepage), plus the full re-run of contract discovery against `api.arrowheadexchange.com`.
- [`security/brown-brown-domain-security.yml`](security/brown-brown-domain-security.yml) — TLS 1.3 and HSTS on both web hosts, SPF and DMARC at `p=reject`, no DNSSEC and no CAA.
- [`llms/brown-brown-llms.txt`](llms/brown-brown-llms.txt) — generated by API Evangelist (not published by Brown & Brown) so an agent reading this repo gets the honest posture rather than guessing.

No packages, CLI, components, sandbox, changelog, status page, trust center, security.txt or vulnerability-disclosure program was found. `github.com/brown-and-brown` is **disproved**, not merely unverified — its three repos are an unrelated educational site and two personal developer homepages.

## Links

- [Website](https://www.bbrown.com/)
- [US Website](https://us.bbrown.com/)
- [Blog](https://us.bbrown.com/blog/) · [Blog RSS](https://us.bbrown.com/blog/rss.xml)
- [Investor Relations](https://investor.bbrown.com/) · [News Release RSS](https://investor.bbrown.com/rss/news-releases.xml)
- [About](https://us.bbrown.com/about/)
- [Contact](https://us.bbrown.com/contact-us)
- [Customer Logins](https://us.bbrown.com/customer-logins)
- [Careers](https://us.bbrown.com/careers/)
- [General Terms of Business](https://us.bbrown.com/general-terms-of-business) · [Privacy Policy](https://us.bbrown.com/privacy-policy)
- [LinkedIn](https://www.linkedin.com/company/brown-brown-insurance)

## Review

See [review.yml](review.yml) for the full reviewer finding, every probed URL with its HTTP status, the ACORD posture record, and the dated `enrichment:` rounds.
