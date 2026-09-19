# AI Factory — personal roadmap (Daniel)

Updated: 2026-09-19 ~00:50 (America/Toronto)  
Live: https://liboriodsantos.github.io/ai-factory-status/ *(Pages sync may lag; local box is truth)*  
Source of truth: `/home/box/projects/bigfit/` on Bot computer  
This is a **roadmap / thinking board**, not the Factory software.

## Founding principles
- **Conversation-first, action-capable interface** — every Factory product ships with a conversational AI front door that executes actions (reports, email, PDFs, workflows), with menus/tabs underneath. Same idea for the proactive support agent.
- **Support stack (decided)** — Freshdesk (helpdesk) + Better Stack (monitoring + status page) + custom proactive AI agent (LLM + Freshdesk API + Better Stack webhooks). Not Intercom Fin / Sierra / Decagon at this stage.

## One sentence
Foundation (FR-01) is proven and paused. **Gate 08 is CLOSED / PASS**. **Gate 09 canary-track is CLOSED / PASS**. **Gate 10 is CLOSED / PASS** (~00:49 EDT). productionWrites remain **false**. Next = Gate 11 (supervised dependability) when Daniel directs; client products stay parked.

## Self-build Factory roadmap (Stage 4 climb)

| Stage | What | Status |
| --- | --- | --- |
| Define the Factory | What it is, who decides, how work is allowed | **DONE** |
| Operating system | Roles, routing, queues, budgets, safe stop, QA | **DONE** |
| FR-01 | Persistent runtime proved E2E, then paused; writes OFF | **DONE** |
| Gate 08 | Publish/install V2 signing path (08.04–08.16) | **CLOSED / PASS** |
| Gate 09 canary-track | Control-receipt paused canary (09.01–09.03) | **CLOSED / PASS** (~19:26 EDT) |
| Gate 09.2 / ops / HOST_FILE | HOST_FILE + MCP PAUSED on :3001 | **PASS** |
| Gate 10 | Bundle v1 + v1.1 + compose inert + cutover + reboot recovery + rollback | **CLOSED / PASS** (~00:49 EDT) |
| Gate 11 | Supervised dependability (repeat jobs; measure quality/cost/repair/recovery) | **NEXT when Daniel directs** |
| Later gates | Products → multi-tenant → bounded autonomy | **AHEAD** |

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
- Full Gate09 **not** claimed — Gate09.2 PASS separately

## Daniel direction (2026-09-18 ~19:24 EDT)
1. Finish current Factory track  
2. Update web map incl. self-build Factory roadmap  
3. Continue building the Factory — **not** client products yet  

## Parked (secondary)
- Ellisbrook / FB-00.2, control-room mocks, off-main Director branches, ChatGPT Library register alone
- Post-Gate10 optional: unused ceremony transport scopes; Pages refresh lag

## Gate 09.2 MCP (2026-09-18 ~23:54 EDT)
- **PASS** — V2 Director MCP healthy on `127.0.0.1:3001` (now compose retained-shadow)
- FACTORY_MODE=PAUSED; productionWrites=false
- HOST_FILE admission key live; DIRECTOR_APPROVAL private still EXTERNAL

## Gate10 — CLOSED / PASS (2026-09-19 ~00:49 EDT)
- Daniel: "close gate 10 if its fully ready"
- Close pack: `evidence/10_GATE_CLOSED_20260919.md`
- Included: Bundle v1 + v1.1; durable MCP + tool-scope; compose inert + cutover + bounded rollback; reboot recovery PASS (MCP downtime 47.229 s)
- Live MCP: `gate10-mcp-director-gateway-shadow-1` on `127.0.0.1:3001`
- productionWrites **false** / FACTORY_MODE **PAUSED** throughout
- Gate08 + Gate09 canary-track remain CLOSED
- Optional parked: ceremony transport scopes; Pages sync

## Gate11 (next)
- Roadmap Stage 5 / supervised dependability
- Repeat useful internal jobs; measure quality, duration, cost, repair, pause and recovery
- Starts only when Daniel directs; stay PAUSED / writes false until he says otherwise
