# Brown & Brown (brown-brown)

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
