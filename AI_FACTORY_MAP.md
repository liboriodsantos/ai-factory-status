# AI Factory — personal roadmap (Daniel)

Updated: 2026-09-19 ~00:11 (America/Toronto)  
Live: https://liboriodsantos.github.io/ai-factory-status/ *(Pages sync may lag; local box is truth)*  
Source of truth: `/home/box/projects/bigfit/` on Bot computer  
This is a **roadmap / thinking board**, not the Factory software.

## Founding principles
- **Conversation-first, action-capable interface** — every Factory product ships with a conversational AI front door that executes actions (reports, email, PDFs, workflows), with menus/tabs underneath. Same idea for the proactive support agent.
- **Support stack (decided)** — Freshdesk (helpdesk) + Better Stack (monitoring + status page) + custom proactive AI agent (LLM + Freshdesk API + Better Stack webhooks). Not Intercom Fin / Sierra / Decagon at this stage.

## One sentence
Foundation (FR-01) is proven and paused. **Gate 08 is CLOSED / PASS**. **Gate 09 canary-track is CLOSED / PASS** (~19:26 EDT). productionWrites remain **false**. Continue Factory self-build; client products stay parked.

## Self-build Factory roadmap (Stage 4 climb)

| Stage | What | Status |
| --- | --- | --- |
| Define the Factory | What it is, who decides, how work is allowed | **DONE** |
| Operating system | Roles, routing, queues, budgets, safe stop, QA | **DONE** |
| FR-01 | Persistent runtime proved E2E, then paused; writes OFF | **DONE** |
| Gate 08 | Publish/install V2 signing path (08.04–08.16) | **CLOSED / PASS** |
| Gate 09 canary-track | Control-receipt paused canary (09.01–09.03) | **CLOSED / PASS** (~19:26 EDT) |
| Gate 09.2 / ops / HOST_FILE | HOST_FILE + MCP PAUSED on :3001 | **PASS** |
| Gate 10 | Bundle v1 + v1.1 PASS; compose inert PASS; cutover/reboot/rollback remain | **IN PROGRESS** |
| Later gates | Dependability → products → multi-tenant → bounded autonomy | **AHEAD** |

**Hard rule:** productionWrites **OFF**; FACTORY_MODE **PAUSED** until Daniel directs otherwise.

## Gate08 — CLOSED / PASS
- 08.01–03 accepted offline
- **08.04–08.14 PASS**
- **08.15 PASS** — live Director approval ceremony
- **08.16 ACCEPT PASS** — challenge evidence archived
- **CLOSED** 2026-09-18 ~19:00 EDT — Daniel: "close Gate 08"
- Close pack: `evidence/08_GATE_CLOSED_20260918.md`

## Gate09 — canary-track CLOSED / PASS
- Control-receipt canary **PASS** 2026-09-18 ~19:19 EDT (`PAUSED_CANARY_COMPLETED`, QA PASS)
- Canary-track **CLOSED** 2026-09-18 ~19:26 EDT — close pack: `evidence/09_GATE_CLOSE_PACK.md`
- Evidence: `evidence/09_CANARY_PASS_20260918.md` + close pack
- productionWrites **false**; FACTORY_MODE **PAUSED**; spend **$0**
- Full Gate09 **not** claimed — Gate09.2 scope defined + host `keys/` + install scripts staged; **BLOCKED** on Daniel ADMISSION HOST_FILE install; Gate10 when Daniel directs

## Daniel direction (2026-09-18 ~19:24 EDT)
1. Finish current Factory track  
2. Update web map incl. self-build Factory roadmap  
3. Continue building the Factory — **not** client products yet  

## Parked (secondary)
- Ellisbrook / FB-00.2, control-room mocks, off-main Director branches, ChatGPT Library register alone


## Gate 09.2 MCP (2026-09-18 ~23:54 EDT)
- **PASS** — V2 Director MCP `gate092-director-mcp-paused` healthy on `127.0.0.1:3001`
- FACTORY_MODE=PAUSED; productionWrites=false
- HOST_FILE admission key live; DIRECTOR_APPROVAL private still EXTERNAL
- Next: Gate10 when Daniel directs

## Gate10 update (2026-09-19 00:05 EDT)
- **Self-Build Bundle v1: PASS** — Factory-supervised PAUSED package
- Durable V2 transport credentials issued (tool-scope); MCP `recover_factory_state` proved (403 without / 200 with)
- productionWrites **false** / FACTORY_MODE **PAUSED** re-proved
- Evidence: `evidence/10_SELF_BUILD_BUNDLE_v1/` + host `/var/lib/factory-self-build/bundles/SELF_BUILD_BUNDLE_v1_20260919T040443Z`
- Bundle webmap: `webmap/self-build-bundle-v1.html`
- Gate08 + Gate09 canary-track remain CLOSED
- Full Gate10 activation engineering: **IN PROGRESS** (first product done; residuals below)


## Gate10 update (2026-09-19 00:11 EDT)
- **Compose inert retained-shadow / candidate placeholders: PASS** — config prove; no compose up; live MCP preserved
- **Self-Build Bundle v1.1: PASS** — activation report + capability inventory via MCP tool-scope (`recover_factory_state` HTTP 200)
- Host: `/var/lib/factory-self-build/bundles/SELF_BUILD_BUNDLE_v1.1_20260919T041112Z` + `ACTIVATION_COMPOSE_INERT_20260919T041108Z`
- Local: `evidence/10_SELF_BUILD_BUNDLE_v1.1/` · `evidence/10_ACTIVATION_COMPOSE_INERT/`
- Webmap: `self-build-bundle-v1.1.html`
- **Gate10 NOT closed** — remaining: compose cutover of live MCP, reboot recovery, bounded rollback, ceremony scopes
- productionWrites **false** / PAUSED; Pages sync left to parent (`gh` unauthenticated)
