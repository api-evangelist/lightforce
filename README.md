# Lightforce

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
