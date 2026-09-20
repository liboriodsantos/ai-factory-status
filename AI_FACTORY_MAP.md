# AI Factory — personal roadmap (Daniel)

Updated: 2026-09-20 ~00:00 (America/Toronto)
Live: https://liboriodsantos.github.io/ai-factory-status/ *(Pages sync may lag; local box is truth)*  
Source of truth: GitHub `factory-bridge` `main` (`apps/factory-os`); local box `/home/box/projects/bigfit/`  
Public pointer: [`BRIDGE_STATE.md`](BRIDGE_STATE.md)  
This is a **roadmap / thinking board**, not the Factory software.

## Founding principles
- **Conversation-first, action-capable interface** — every Factory product ships with a conversational AI front door that executes actions (reports, email, PDFs, workflows), with menus/tabs underneath. Same idea for the proactive support agent.
- **Support stack (decided)** — Freshdesk (helpdesk) + Better Stack (monitoring + status page) + custom proactive AI agent (LLM + Freshdesk API + Better Stack webhooks). Not Intercom Fin / Sierra / Decagon at this stage.

## One sentence
Gates 08–11 **CLOSED / PASS**. Gate08 remains **CLOSED**. Gate09 canary packet **`HARNESS_PASS_09.06_HOST_RECON_PASS`**. **Factory OS through items 31–36** on `factory-bridge` main and standing host `factory-runtime-01` (11–30 still earned; **26** and **28** corrected): auth stub (PR #57), Home cost **`UNAVAILABLE`** (PR #58), host deploy + supervised ceremony (15–16), Ellisbrook live attach **NO-GO** (17), smoke host **PASS** (18), host redeploy latest main (19), durable loopback **`HTTP_BRIDGE`** (20), FLOW-01/02 deepen (21–22), Decision auth-gated approve (23), conversation bar **RO** (24), write-class design doc **no flip** (25), FLOW-03 **DONE** (**26**, **#73**), FLOW-01 universal record **DONE** (**28**, **#76**), host redeploy latest main **DONE** (**31**, auth + `HTTP_BRIDGE`, **PAUSED**), Pages 21–30 already live (**32**), Portfolio+Work **in progress** (**33**, **PR #77**), Teams **DONE** (**34**, **#78**), FLOW-02 universal record **DONE** (**35**, **#79**), FLOW-04 thin RO **in progress** (**36**, **PR #80**). Write class **`factory.self_build.supervised`** (named only; no expansion / no flip). productionWrites **false**. FACTORY_MODE **PAUSED**. Director keys **off host**. Client products parked. Software PR open/merged state was **not verified** from this Pages token.

## Object model spine
Idea → Concept → Conception Project → Definition → Blueprint → Product → Project → Release

## Factory OS (on main + standing host)
- Home **live loopback** via durable **`HTTP_BRIDGE`** on `factory-runtime-01` (item 20) · latest-main redeploy again (**31**)
- Home cost strip **`UNAVAILABLE`** (PR #58) — do not treat stub `$0` as earned spend
- **Auth stub** on main + host (PR #57) — stub only, not full People & Access
- **FLOW-01 / FLOW-02 deepened** (21–22) — still not full journeys
- FLOW-01 **universal record** (**28**, **PR #76**) · FLOW-02 **universal record** (**35**, **PR #79**)
- FLOW-03 **DONE** (**26**, **PR #73**) — thin Operate & Improve, not a full production→improvement chain
- FLOW-04 **thin RO in progress** (**36**, **PR #80**)
- Portfolio + Work **in progress** (**33**, **PR #77**)
- Teams **DONE** (**34**, **PR #78**)
- **Durable Factory DB**
- **Decision Inbox V2** · auth-gated approve (23) — not a write-class flip
- **Operate RO** (read-only)
- Conversation bar **RO** (24)
- Write-class design doc (25) — `factory.self_build.supervised` named only; **no flip**
- Host: deploy + supervised ceremony (15–16) · smoke **PASS** (18) · latest-main redeploy (19) · latest-main redeploy again (31) · remaining host durability (27, 29–30) not re-specified this brief
- Ellisbrook: readiness docs recorded (17); live attach **NO-GO**
- Pages 21–30: already live (**32**, this repo PR #14)
- Repo: `apps/factory-os` on `factory-bridge` `main`
- This Pages agent could not clone `factory-bridge` (404 / out of token scope). Software truth stays on that repo’s `main`. Software PR numbers **#73–#80** are from Daniel’s item-38 brief.

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
| Gate 12 / Stage 6 | Factory OS Control Room on `main` + standing host | **ITEMS 31–36** (host redeploy · Pages 21–30 live · Portfolio/Work WIP · Teams DONE · FLOW-02/04 · 26/28 corrected) |
| Later gates | Multi-tenant → bounded autonomy | **AHEAD** |

**Hard rule:** productionWrites **OFF**; FACTORY_MODE **PAUSED** until Daniel directs otherwise. Write class `factory.self_build.supervised` is **named only** — no expansion / **no flip**. No Director keys on host.

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
- Ellisbrook / FB-00.2 — readiness docs recorded (item 17); **live attach NO-GO**
- Control-room mocks, off-main Director branches, ChatGPT Library register alone
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

## Factory OS items 11–20 (2026-09-19 ~21:15 EDT)
- **11–14 software:** auth stub on main + host (**PR #57**); Home cost strip **`UNAVAILABLE`** (**PR #58**)
- **15–16:** host deploy + supervised ceremony (writes stayed false)
- **17:** Ellisbrook readiness docs — live attach **NO-GO**
- **18:** smoke host **PASS**
- **19:** host redeploy latest `main`
- **20:** durable loopback Bridge **`HTTP_BRIDGE`** on standing host `factory-runtime-01`
- FACTORY_MODE **PAUSED** · productionWrites **false** · Director keys **off host**
- Write class `factory.self_build.supervised` named only — **no expansion**

## Factory OS items 21–30 (corrected 2026-09-20 ~00:00 EDT)
- **21–22:** FLOW-01 / FLOW-02 deepen — still not full 13-gate / watch-the-Factory journeys
- **23:** Decision auth-gated approve — not a write-class flip
- **24:** conversation bar **RO** — no mutating intents
- **25:** write-class design doc — `factory.self_build.supervised` named only; **no flip**
- **26:** FLOW-03 **DONE** — factory-bridge **PR #73** (thin; not a full Operate & Improve chain)
- **27, 29–30:** prior board recorded host durability; **this brief did not re-specify** — not invented
- **28:** FLOW-01 universal record **DONE** — factory-bridge **PR #76**
- FACTORY_MODE **PAUSED** · productionWrites **false** · Director keys **off host**
- Write class `factory.self_build.supervised` named only — **no expansion / no flip**
- Ellisbrook live attach remains **NO-GO**

## Factory OS items 31–36 (2026-09-20 ~00:00 EDT)
- **31:** host redeploy latest `main` **DONE** — auth + **`HTTP_BRIDGE`** remain · **PAUSED**
- **32:** Pages 21–30 **already live** — this repo **PR #14** (last confirmed Pages SHA `8468472`)
- **33:** Portfolio + Work — **in progress** · factory-bridge **PR #77** (open vs merged not verified from this Pages token)
- **34:** Teams **DONE** — factory-bridge **PR #78**
- **35:** FLOW-02 universal record **DONE** — factory-bridge **PR #79**
- **36:** FLOW-04 thin RO — **in progress** · factory-bridge **PR #80** (open vs merged not verified from this Pages token)
- Software PR numbers from Daniel’s item-38 brief; `factory-bridge` was **not reachable** here
- FACTORY_MODE **PAUSED** · productionWrites **false** · Director keys **off host**
- Write class `factory.self_build.supervised` named only — **no expansion / no flip**
- Ellisbrook live attach remains **NO-GO**
