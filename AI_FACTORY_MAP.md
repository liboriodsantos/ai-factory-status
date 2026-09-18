# AI Factory — personal roadmap (Daniel)

Updated: 2026-09-18 ~19:26 (America/Toronto)  
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
| Gate 09.2+ / ops / HOST_FILE | Define remaining Gate09 slices; MCP admission HOST_FILE still unprovisioned | **NEXT** |
| Gate 10 | Activation + first useful supervised self-build | **AHEAD** |
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
- Full Gate09 **not** claimed — next = define Gate09.2+ / ops hardening / MCP admission HOST_FILE key; Gate10 when Daniel directs

## Daniel direction (2026-09-18 ~19:24 EDT)
1. Finish current Factory track  
2. Update web map incl. self-build Factory roadmap  
3. Continue building the Factory — **not** client products yet  

## Parked (secondary)
- Ellisbrook / FB-00.2, control-room mocks, off-main Director branches, ChatGPT Library register alone
