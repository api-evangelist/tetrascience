# TetraScience

> Profile of [TetraScience](https://www.tetrascience.com/) for the [API Evangelist](https://apievangelist.com) network. TetraScience is the scientific data and AI platform company behind the **Tetra Scientific Data and AI Cloud** — purpose-built infrastructure that liberates, replatforms, and engineers raw lab data into FAIR, AI-native Tetra Data for pharma, biotech, CROs, and CDMOs.

This repo captures the TetraScience platform surface as a set of machine-readable artifacts conforming to the API Evangelist / API Commons specifications.

## Provider Snapshot

- **Website**: <https://www.tetrascience.com/>
- **Developers**: <https://developers.tetrascience.com/>
- **API Reference**: <https://developers.tetrascience.com/reference>
- **LLMs index**: <https://developers.tetrascience.com/llms.txt>
- **GitHub org**: <https://github.com/tetrascience>

### Production servers

- `https://api.tetrascience.com` — Production
- `https://api.tetrascience-uat.com` — UAT
- `https://api.tetrascience-dev.com` — Development

### Authentication

The Tetra Data Platform API uses two API-key headers on every authenticated request:

| Header          | Purpose                                            |
| --------------- | -------------------------------------------------- |
| `ts-auth-token` | API token issued from the TDP admin console        |
| `x-org-slug`    | Organization slug, for multi-tenant request routing |

SAML 2.0 / OIDC SSO is also supported for human users.

## Artifacts

| Type | File |
|------|------|
| [apis.yml](apis.yml) | API Evangelist provider index — full feature, use case, integration, and industry inventory |
| [openapi/tetrascience-openapi.yml](openapi/tetrascience-openapi.yml) · [.json](openapi/tetrascience-openapi.json) | Merged OpenAPI 3.1 spec for the Tetra Data and AI Cloud API |
| [rules/tetrascience-rules.yml](rules/tetrascience-rules.yml) | Spectral ruleset enforcing TetraScience's API conventions |
| [capabilities/](capabilities/) | Naftiko capability bundles for Agents, Pipelines, Files & Search, and Administration |
| [json-ld/tetrascience-context.jsonld](json-ld/tetrascience-context.jsonld) | JSON-LD context for Tetra Data, agents, pipelines, IDS, and AI layer |
| [vocabulary/tetrascience-vocabulary.yml](vocabulary/tetrascience-vocabulary.yml) | Domain vocabulary — platform, data lifecycle, ingestion, AI, compliance, scientific domains |
| [plans/tetrascience-plans-pricing.yml](plans/tetrascience-plans-pricing.yml) | API Commons Plans 0.1 — enterprise subscription, add-on modules, services |
| [rate-limits/tetrascience-rate-limits.yml](rate-limits/tetrascience-rate-limits.yml) | API Commons Rate Limits 0.1 — gateway, pipeline concurrency, search, ingest |
| [finops/tetrascience-finops.yml](finops/tetrascience-finops.yml) | FOCUS 1.3 cost mapping across subscription, agents, pipelines, storage, AI layer |

## API Surface

The merged OpenAPI spec covers **182 paths / 212 operations** across the following tag groups:

- **Identity & Access**: Tenants, Organizations, Users, Roles, Access Groups, Login
- **Lab Data Ingestion**: Agents, Connectors, Commands, Data Acquisition
- **Data Engineering**: Pipelines, Protocols, Task Scripts, IDS, ai-workflows, tetraflows
- **Data Lake & Search**: files, schemas, lakehouse, databricks, clusters
- **Apps & Subscriptions**: Data Apps, Data App Providers, Embedded / Linked Data Apps, Edit / View Subscriptions, Hubs, tetraspheres
- **Audit Trail**: Tenant-level audit log

> The merge ingests one OpenAPI fragment per published reference page. ~32 data-lake / file / workflow endpoints were rate-limited by Cloudflare at scrape time and may be backfilled in a subsequent refresh.

## Platform Pillars

- **Tetra Agents & Integrations** — Liberation layer for instrument and informatics data
- **Tetra Data Pipelines** — Serverless data engineering with replays and observability
- **Intermediate Data Schema (IDS)** — Vendor-neutral JSON schemas for scientific data
- **Tetra Data Lake** — Cloud object storage with attributes, tags, labels, audit
- **Tetra AI Layer / Sciborgs** — Scientific AI agents grounded in engineered Tetra Data
- **GxP Compliance Module** — 21 CFR Part 11 / EU Annex 11 alignment
- **Chromatography Insights App** — Cross-vendor CDS analytics

## Use Cases

Lab Data Automation · Scientific Data Engineering · GenAI / RAG for Lab Data · Chromatography Productivity · Discovery Acceleration · CMC & Bioprocessing · Manufacturing & QC · CRO / CDMO Data Exchange · GxP Regulated Workflows · Scientific Data Migration

## Industries

Pharmaceutical · Biotechnology · CRO · CDMO · Diagnostics · Cell & Gene Therapy · Analytical Chemistry

## License

The artifacts in this repository are published under the [API Evangelist](https://apievangelist.com) license. TetraScience product trademarks, documentation, and APIs remain the property of TetraScience PBC.
