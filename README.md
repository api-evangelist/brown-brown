# Brown & Brown

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

Brown & Brown, Inc. (NYSE: BRO) is a Daytona Beach, Florida headquartered insurance brokerage and risk-management intermediary founded in 1939, and one of the largest independent brokers in the United States. Following the 2025 acquisition of Accession Risk Management Group (Risk Strategies and One80 Intermediaries), it reports through two segments: Retail — property and casualty insurance, employee benefits, private client, captive solutions and financial/wealth services — and Specialty Distribution — programs, wholesale brokerage and MGA/binding-authority businesses including Arrowhead. As a distributor rather than a carrier, Brown & Brown places risk with insurers instead of underwriting it, and its US home market has no federal insurance regulator and no open-insurance mandate. Its API posture reflects that honestly: Brown & Brown publishes no public developer portal and no self-serve API. developer.bbrown.com, developers.bbrown.com, docs.bbrown.com and api.bbrown.com do not resolve, and every /developers, /api, /partners and /integrations path returns 404. Every discoverable application subdomain is a login wall — agent, client and vendor portals behind Microsoft Entra ID SSO or third-party sign-in. The only real programmatic surface is partner-gated: the Arrowhead Programs "Enterprise API" (EAPI), a quoting integration distributed through comparative raters and aggregators such as CoverHound, Tarmika, Semsee and DAIS, with no public documentation, base URL or specification. No ACORD, AL3, ACORD XML or NGDS reference is published on any Brown & Brown first-party property; carrier data exchange runs, as it does across US retail brokerage, through the agency management system layer — Brown & Brown is a publicly referenced Vertafore AMS360 agency — and IVANS agency download rather than through any API Brown & Brown itself exposes. In July 2026 the company announced an AI-first transformation with Anthropic, McKinsey and Accenture, deploying Claude across 23,000 teammates and Claude Code across its software engineering organization; that is internal adoption and has so far produced no external API, developer portal or agent-facing surface. The only machine-readable documents Brown & Brown publishes are two RSS feeds — the blog and investor news releases.

**Areas:** Insurance · United States · Brokerage · Property and Casualty · Employee Benefits · Wholesale Brokerage · Managing General Agent · Risk Management · Agency Management

## Brown & Brown on APIs.io

Everything profiled for Brown & Brown is published on APIs.io rather than in this repository. Start at the provider page — **[apis.io/providers/brown-brown/](https://apis.io/providers/brown-brown/)** — or go straight to one of the APIs or properties below.

### Published properties

Each property below is a page on APIs.io carrying the machine-readable artifact and what it says.

#### Security (1)

Authentication, trust centre, and vulnerability disclosure.

- [Brown Brown Domain Security](https://apis.io/security/brown-brown/brown-brown-domain-security/)

## Where to find this API

Links to the company's own pages. This repository publishes no copy of their specifications — the canonical document is theirs and lives at the URLs below.

- [Website](https://www.bbrown.com/)
- [Support](https://us.bbrown.com/contact-us)
- [Blog](https://us.bbrown.com/blog/)
- [Terms of service](https://us.bbrown.com/general-terms-of-business)
- [Privacy policy](https://us.bbrown.com/privacy-policy)

## API Evangelist rating

**Kin Score 11.2** — emerging · rubric 0.24.0 · scored 2026-10-17

| Facet | Score |
|---|---|
| Discoverability | 49.1 |
| Contract quality | 0.0 |
| Contract governance | 0.0 |
| Operational transparency | 0.0 |
| Developer ergonomics | 7.1 |
| Access clarity | 27.6 |

**Agent readiness 0.0** — human-only

| Agent-readiness dimension | Result |
|---|---|
| Spec Presence | — |
| Agentic Access | — |
| Reversibility Documented | — |
| MCP Server | — |
| Auth Clarity | — |
| Idempotency | — |
| Error Semantics | — |
| OpenAPI Examples | — |
| Rate Limit Signal | — |
| Event Surface Described | — |
| Agent Skills | — |
| Well Known Catalog | — |
| Consent Identity | — |
| Agent Card | — |
| Dry Run Mode | — |
| Delegated Identity | — |
| Protected Resource Metadata | — |
| Dynamic Client Registration | — |
| Agentic Commerce | — |

**Regulatory alignment 12.3** — Insurance

The rubric is published at [github.com/api-evangelist/kin-score](https://github.com/api-evangelist/kin-score). The per-check breakdown behind these numbers — which checks were earned, partial or missed — along with score history and how this provider compares to its peers, is available at [apis.io/providers/brown-brown/](https://apis.io/providers/brown-brown/).

## How this profile is made

API Evangelist profiles a company's public API surface the way a developer would find it: the website, developer portal and documentation, the specifications it publishes, its public repositories, and its pricing, status and changelog pages. From that it derives the properties above — contracts split per API, workflows, schemas, collections, governance rules, plans and rate limits — and scores them against the published [Kin Score rubric](https://github.com/api-evangelist/kin-score).

The artifacts are published on [APIs.io](https://apis.io), not in this repository. This repository is the public record for Brown & Brown: the place to say something is wrong, missing or out of date, and to ask for a re-score or a removal.

## Open an issue

- **Something about this listing** — a wrong description, a missing API, a stale artifact or a question about the rating: [open an issue on this repository](https://github.com/api-evangelist/brown-brown/issues/new).
- **A new API, or one that is not in the catalog yet** — [submit it on APIs.io](https://apis.io/add/).
- **Anything else** — [the APIs.io inbox](https://github.com/api-search/inbox/issues/new) or [info@apievangelist.com](mailto:info@apievangelist.com).
