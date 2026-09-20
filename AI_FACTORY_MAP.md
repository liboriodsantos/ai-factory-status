# AI Factory — personal roadmap (Daniel)

Updated: 2026-09-19 ~20:30 (America/Toronto)
Live: https://liboriodsantos.github.io/ai-factory-status/ *(Pages sync may lag; local box is truth)*  
Source of truth: GitHub `factory-bridge` `main` (`apps/factory-os`); local box `/home/box/projects/bigfit/`  
Public pointer: [`BRIDGE_STATE.md`](BRIDGE_STATE.md)  
This is a **roadmap / thinking board**, not the Factory software.

## Founding principles
- **Conversation-first, action-capable interface** — every Factory product ships with a conversational AI front door that executes actions (reports, email, PDFs, workflows), with menus/tabs underneath. Same idea for the proactive support agent.
- **Support stack (decided)** — Freshdesk (helpdesk) + Better Stack (monitoring + status page) + custom proactive AI agent (LLM + Freshdesk API + Better Stack webhooks). Not Intercom Fin / Sierra / Decagon at this stage.

## One sentence
Gates 08–11 **CLOSED / PASS**. Gate08 remains **CLOSED**. Gate09 canary packet **`HARNESS_PASS_09.06_HOST_RECON_PASS`**. **Factory OS is on `factory-bridge` main** (Home live loopback, FLOW spine, durable Factory DB, Decision Inbox V2, Operate RO). Write class **`factory.self_build.supervised`** (named only; no expansion). productionWrites **false**. FACTORY_MODE **PAUSED**. No Director keys. Client products parked.

## Object model spine
Idea → Concept → Conception Project → Definition → Blueprint → Product → Project → Release

## Factory OS (on main)
- Home **live loopback**
- **FLOW spine**
- **Durable Factory DB**
- **Decision Inbox V2**
- **Operate RO** (read-only)
- Repo: `apps/factory-os` on `factory-bridge` `main`
- This Pages agent could not clone `factory-bridge` (404 / out of token scope). Software truth stays on that repo’s `main`.

## Self-build Factory roadmap (Stage 4–5 climb)

| Stage | What | Status |
| --- | --- | --- |
| Define the Factory | What it is, who decides, how work is allowed | **DONE** |
| Operating system | Roles, routing, queues, budgets, safe stop, QA | **DONE** |
| FR-01 | Persistent runtime proved E2E, then paused; writes OFF | **DONE** |
| Gate 08 | Publish/install V2 signing path (08.04–08.16) | **CLOSED / PASS** |
| Gate 09 canary-track | Control-receipt paused canary (09.01–09.03) | **CLOSED / PASS** (~19:26 EDT 18 Sep) |
| Gate 09 canary packet | `HARNESS_PASS_09.06_HOST_RECON_PASS` | **RECORDED** |
| Gate 09.2 / ops / HOST_FILE | HOST_FILE + MCP PAUSED on :3001 | **PASS** |
| Gate 10 | Bundle v1 + v1.1 + compose inert + cutover + reboot recovery + rollback | **CLOSED / PASS** (~00:49 EDT 19 Sep) |
| Gate 11 | Supervised dependability (repeat jobs; measure quality/cost/repair/recovery) | **CLOSED / PASS** (~01:03 EDT 19 Sep) |
| Gate 12 / Stage 6 | Factory OS Control Room on `main` | **ON MAIN** (named surfaces above) |
| Later gates | Multi-tenant → bounded autonomy | **AHEAD** |

**Hard rule:** productionWrites **OFF**; FACTORY_MODE **PAUSED** until Daniel directs otherwise. Write class `factory.self_build.supervised` is **named only** — no expansion. No Director keys on host.

## Gate08 — CLOSED / PASS
- 08.01–03 accepted offline
- **08.04–08.14 PASS**
- **08.15 PASS** — live Director approval ceremony
- **08.16 ACCEPT PASS** — challenge evidence archived
- **CLOSED** 2026-09-18 ~19:00 EDT — Daniel: "close Gate 08"
- Close pack: `evidence/08_GATE_CLOSED_20260918.md`

## Gate09 — canary packet recorded
- Control-receipt canary **PASS** 2026-09-18 ~19:19 EDT (`PAUSED_CANARY_COMPLETED`, QA PASS)
- Canary-track **CLOSED** 2026-09-18 ~19:26 EDT — close pack: `evidence/09_GATE_CLOSE_PACK.md`
- Latest canary packet: **`HARNESS_PASS_09.06_HOST_RECON_PASS`**
- Evidence: `evidence/09_CANARY_PASS_20260918.md` + close pack
- productionWrites **false**; FACTORY_MODE **PAUSED**; spend **$0**
- Full Gate09 beyond this packet is **not** claimed
- Director private key remains **EXTERNAL** — no Director keys on host / none in this repo

## Daniel direction (2026-09-18 ~19:24 EDT)
1. Finish current Factory track  
2. Update web map incl. self-build Factory roadmap  
3. Continue building the Factory — **not** client products yet  

## Parked (secondary)
- Ellisbrook / FB-00.2, control-room mocks, off-main Director branches, ChatGPT Library register alone
- Post-Gate11 optional: unused ceremony transport scopes

## Gate 09.2 MCP (2026-09-18 ~23:54 EDT)
- **PASS** — V2 Director MCP healthy on `127.0.0.1:3001` (compose retained-shadow)
- FACTORY_MODE=PAUSED; productionWrites=false
- HOST_FILE admission key live; DIRECTOR_APPROVAL private still EXTERNAL (no Director keys)

## Gate10 — CLOSED / PASS (2026-09-19 ~00:49 EDT)
- Daniel: "close gate 10 if its fully ready"
- Close pack: `evidence/10_GATE_CLOSED_20260919.md`
- Included: Bundle v1 + v1.1; durable MCP + tool-scope; compose inert + cutover + bounded rollback; reboot recovery PASS (MCP downtime 47.229 s)
- Live MCP: `gate10-mcp-director-gateway-shadow-1` on `127.0.0.1:3001`
- productionWrites **false** / FACTORY_MODE **PAUSED** throughout
- Gate08 CLOSED; Gate09 canary packet `HARNESS_PASS_09.06_HOST_RECON_PASS`

## Gate11 — CLOSED / PASS (2026-09-19 ~01:03 EDT)
- Daniel: "close Gate 11"
- Close pack: `evidence/11_GATE_CLOSED_20260919.md`
- Dependability Run #1 **PASS** N=3 Self-Build style (mean 1.124s; $0; repair 0)
- Dependability Run #2 **PASS** N=3 MCP-compose recovery (mean downtime 1.784s; $0; repair 0)
- Evidence: `11_DEPENDABILITY_RUN1_PASS.md` + `11_DEPENDABILITY_RUN2_PASS.md`
- Stay PAUSED / writes false until he says otherwise
- Client products stay parked
