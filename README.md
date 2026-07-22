> **DEPRECATED — superseded by [static-ncino](https://github.com/kody-w/static-ncino) + [static-plaid](https://github.com/kody-w/static-plaid)** (real-product compatibility shapes). Endpoints stay live for old links; no updates.

# static-loan-origination

Deterministic, zero-dependency **loan origination & credit decisioning** simulator for the
fictional Bluegrass Credit Union, served as static JSON on GitHub Pages.

It models the **human-in-the-loop layer** of an agentic loan flow: applications referred to
underwriters, each carrying a full synthetic AI assessment (scorecard, bureau score, fraud
risk score, Open Banking affordability, recommendation, rationale), plus historical
underwriter decisions with `agreed_with_ai` model-feedback signals.

## Endpoints

| Collection | URL |
|---|---|
| Index | https://kody-w.github.io/static-loan-origination/api/v1/index.json |
| Referred applications | https://kody-w.github.io/static-loan-origination/api/v1/referred_applications.json |
| Underwriter decisions | https://kody-w.github.io/static-loan-origination/api/v1/decisions.json |
| MCP manifest | https://kody-w.github.io/static-loan-origination/mcp/manifest.json |

All collections use the `{count, value}` REST shape. CORS is open (GitHub Pages), so browser
apps can fetch these directly.

## Joins

`application_number` / `member_number` join
[static-core-banking](https://github.com/kody-w/static-core-banking) — the referred queue here
enriches that org's undecided applications (LA-3002, LA-3003, LA-3006, LA-3007).

## Disclaimer

Independently authored simulator serving generic loan-origination REST shapes; all members,
applications, and AI assessments synthetic; not affiliated with any financial institution or
vendor; simulation only — never use for real financial activity.
