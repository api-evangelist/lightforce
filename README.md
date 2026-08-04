# Lightforce

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

LightForce Orthodontics, Inc. (https://lf.co) is a medical device and digital manufacturing company producing "generative braces" — fully customized, 3D-printed orthodontic brackets (LightBracket ceramic and metal) and indirect bonding trays, generated from each patient's own tooth anatomy and the treating orthodontist's digital treatment plan. Doctors submit intraoral scans and treatment plans through the LightForce Doctor Portal; LightForce designs, prints, and ships patient-specific appliances back to the practice.

Backed by: matrix-partners — https://lf.co

## API surface

LightForce publishes **no public developer API, developer portal, SDK, or API specification**. The only publicly machine-discoverable API surface is the OpenID Connect identity tenant that fronts the Doctor Portal:

- OIDC discovery: https://id.lightforceortho.com/.well-known/openid-configuration

## Artifacts

| Dir | Artifact | Method |
|---|---|---|
| `well-known/` | OIDC discovery, RFC 8414 metadata, JWKS (saved verbatim) + probe index | searched |
| `authentication/` | Full auth profile: endpoints, grants, token auth methods, DPoP, MFA | searched |
| `scopes/` | 14 identity scopes from `scopes_supported` | searched |
| `conformance/` | Standards asserted with evidence (OIDC, OAuth 2.0, PKCE, device grant, token exchange, DPoP, CIBA, HIPAA) | searched |
| `conventions/` | Cross-cutting semantics; most unknown — no public API documented | searched |
| `security/` | TLS/HSTS/DNS posture probed live | probed |
| `packages/` | Verified empty — no first-party client library on any registry | searched |
| `llms/` | Generated llms.txt (no provider-published one exists) | generated |
