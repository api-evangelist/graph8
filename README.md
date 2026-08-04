# graph8

Autonomous revenue system — an AI-native B2B sales platform that finds buyers, launches
campaigns, runs conversations and builds pipeline against one buyer graph.

- **Platform:** https://graph8.com
- **Developer platform:** https://graph8.com/build/
- **Documentation:** https://docs.graph8.com
- **Pricing:** https://graph8.com/pricing
- **llms.txt:** https://graph8.com/llms.txt · https://docs.graph8.com/llms.txt

One company, four brands: **graph8** (platform), **graph8 build** (developers), **CIENCE**
(SDR/GTM services), **Tenbound** (research magazine and community).

Part of the [API Evangelist](https://apievangelist.com) network. Profiled 2026-08-03; every
surface was fetched first — see `X-Discovery` in `apis.yml`.

## What is published

| | |
| --- | --- |
| `graph8.com/llms.txt` | **200** — 3.4KB |
| `docs.graph8.com/llms.txt` | **200** — 46KB, 278 links, 15 developer pages |
| `/build/` — API, SDKs, CLI, MCP, components, infrastructure | **200** — six documented surfaces |
| Pricing, status, changelog | **200** |

## What is not — the honest gaps

**No OpenAPI is publicly fetchable.** 404 at `/openapi.json`, `docs.graph8.com/openapi.json` and
`/api-reference/openapi.json`; `api.graph8.com` does not resolve. The `/build/status` page
nonetheless advertises **"REST + OpenAPI — Operational"**.

**`graph8.com/api/openapi.json` looks like a spec and is not one.** It returns 200 with 958,565
bytes that are **byte-identical** to a control request for `/api/zzz-control-nonsense` — the whole
`/api/*` tree is a single-page-app catch-all. Any probe under it reports a false success. The apex
control `/zzz-control-nonsense` correctly 404s, so this is scoped to `/api/*`.

**No reachable MCP endpoint.** `/mcp` 404s, though MCP is marketed with named tools
(`search_contacts`, `enrich_company`, `read_signals`).

**No spec was modelled on their behalf.** The developer platform is explicitly in preview and a
workspace endpoint is issued on request, so these are gaps to close rather than defects to paper
over.
