# AI Factory — personal roadmap (Daniel)

Updated: 2026-09-20 ~05:15 (America/Toronto)
Live: https://liboriodsantos.github.io/ai-factory-status/ *(Pages sync may lag; local box is truth)*  
Source of truth: GitHub `factory-bridge` `main` (`apps/factory-os`); local box `/home/box/projects/bigfit/`  
Public pointer: [`BRIDGE_STATE.md`](BRIDGE_STATE.md)  
This is a **roadmap / thinking board**, not the Factory software.

## Founding principles
- **Conversation-first, action-capable interface** — every Factory product ships with a conversational AI front door that executes actions (reports, email, PDFs, workflows), with menus/tabs underneath. Same idea for the proactive support agent.
- **Support stack (decided)** — Freshdesk (helpdesk) + Better Stack (monitoring + status page) + custom proactive AI agent (LLM + Freshdesk API + Better Stack webhooks). Not Intercom Fin / Sierra / Decagon at this stage.

## One sentence
Gates 08–11 **CLOSED / PASS**. Gate08 remains **CLOSED**. Gate09 canary packet **`HARNESS_PASS_09.06_HOST_RECON_PASS`**. **Factory OS through items 45–65** on `factory-bridge` main and standing host `factory-runtime-01` (11–43 still earned; **33** and **36** closed via later **54** / **59**): Pages 37–43 already live (**45**, this repo **#17** @ `fb84e26`), Discover deepen (**46–48**, **#87**), Evidence deepen (**49–50**, **#86**), Integrations deepen (**51–52**, **#88**), Home next-best-action (**53**, **#85**), Portfolio+Work **DONE** (**54**, **#89**), Teams (**55**, **#90**), FLOW-01..04 (**56–59**, **#91–#94**), Discover universal record (**60**, **#95**), Evidence universal record (**61**, **#97**), Decision Inbox (**62**, **#98**), conversation bar (**63**, **#96**), Home strip (**64**, **#99** · cost stays **`UNAVAILABLE`**), Work→receipt (**65**, **#100**), operator host redeploy (**69**, `01f880b` · ANON HTTP **307** · **`HTTP_BRIDGE`** · **PAUSED**), docs **#101**, write-class design note (**71**, `24dca85` · docs only · **no flip**). Prior 37–43 stay earned (host 37 · Pages 31–36 · Discover shells · Evidence ledger · Integrations shell · Home NBA · host 43 @ `ca5fbb0` · probe ANON HTTP **307** · Bridge health **200** · evidenceClass **`HTTP_BRIDGE`**). Write class **`factory.self_build.supervised`** (named only; no expansion / no flip). productionWrites **false**. FACTORY_MODE **PAUSED**. Director keys **off host**. Client products parked. Buffer **75–86** DONE (Products **86** **#116** @ `b06390b`). Item **74** **DONE** — standing host tip synced to factory-bridge main `b06390b1552d10fce00d93be8734dc00d37bca7b` (includes Products #116). Item **70** **DONE** — same tip SHA; host is current with main through Products #116. Teams **#117**, Integrations **#118**, Actor **#119**, FLOW-03 **#120** (may still be open), Contract **#121**, and conversation-bar **#122** are **open, not merged** (GitHub Actions spending-limit — **not DONE**). Buffer **87–94** not merged. Item **8** still deferred (needs Daniel secret). Overnight software PR numbers **#85–#101** are from Daniel’s item-67 brief; this Pages token could not read `factory-bridge`. Merge SHAs for those PRs were **not** in the brief — not invented.

## Object model spine
Idea → Concept → Conception Project → Definition → Blueprint → Product → Project → Release

## Factory OS (on main + standing host)
- Home **live loopback** via durable **`HTTP_BRIDGE`** on `factory-runtime-01` (item 20) · latest-main redeploys (**31**, **37**, **43**) · operator host redeploys (**66**, **69**)
- Home **next-best-action** (**42**, **#84** · **53**, **#85**) — thin NBA; cost strip stays **`UNAVAILABLE`**
- Home strip (**64**, **#99**) · Home cost strip **`UNAVAILABLE`** (PR #58) — do not treat stub `$0` as earned spend
- **Auth stub** on main + host (PR #57) — stub only, not full People & Access
- Discover family **shells** (**39**, **#81**) · **deepen** (**46–48**, **#87**) · universal record (**60**, **#95**) — still not full Idea/Conception/Blueprint journeys
- Evidence & Receipts **ledger** (**40**, **#82**) · **deepen** (**49–50**, **#86**) · universal record (**61**, **#97**) — still not full challenge-id bind
- Integrations **shell** (**41**, **#83**) · **deepen** (**51–52**, **#88**) — still thin; adapter freeze still open · follow-up **#118** open, not merged (Actions spending-limit — not DONE)
- **FLOW-01 / FLOW-02 deepened** (21–22 · **56–57**, **#91–#92**) — still not full journeys
- FLOW-01 **universal record** (**28**, **#76**) · FLOW-02 **universal record** (**35**, **#79**)
- FLOW-03 **DONE** (**26**, **#73** · **58**, **#93**) — thin Operate & Improve, not a full production→improvement chain
- FLOW-04 **thin RO DONE** (**36** closed via **59**, **#94**) — still not a full Sell & Manage journey
- Portfolio + Work **DONE** (**33** closed via **54**, **#89**) · Work→receipt (**65**, **#100**)
- Teams **DONE** (**34**, **#78** · **55**, **#90**) — thin roster, not full People & Access · follow-up **#117** open, not merged (Actions spending-limit — not DONE)
- **Durable Factory DB**
- **Decision Inbox V2** · auth-gated approve (23) · deepen (**62**, **#98**) — not a write-class flip
- **Operate RO** (read-only)
- Conversation bar **RO** (24 · **63**, **#96**)
- Write-class design doc (25) — `factory.self_build.supervised` named only; **no flip**
- Write-class design note (**71**, `24dca85`) — docs only; **no flip**
- Host: deploy + supervised ceremony (15–16) · smoke **PASS** (18) · latest-main redeploy (19) · latest-main redeploy again (31) · standing host redeploy again (**37**, earlier ~`53512c5`) · standing host Factory OS redeploy (**43**, origin/main `ca5fbb0bf5e8bad66daec9be0861bfab8f371efc` includes **#81–#84** · probe ANON HTTP **307** · Bridge health **200** · evidenceClass **`HTTP_BRIDGE`**) · operator host redeploy (**69**, factory-bridge main `01f880b` · ANON HTTP **307** · **`HTTP_BRIDGE`** · **PAUSED**) · remaining host durability (27, 29–30) not re-specified this brief
- Ellisbrook: readiness docs recorded (17); live attach **NO-GO**
- Pages 21–30: already live (**32**, this repo PR #14)
- Pages 31–36: already live (**38**, this repo PR #15 @ `9d91184`)
- Pages 37–43: already live (**45**, this repo PR #17 @ `fb84e26`)
- Docs: factory-bridge **PR #101**
- Repo: `apps/factory-os` on `factory-bridge` `main`
- This Pages agent could not clone `factory-bridge` (404 / out of token scope). Software truth stays on that repo’s `main`. Overnight software PR numbers **#85–#101** are from Daniel’s item-67 brief. Merge SHAs for those PRs were **not** in the brief — not invented.

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
| Gate 12 / Stage 6 | Factory OS Control Room on `main` + standing host | **ITEMS 45–86** (buffer 75–86 DONE · Products 86 #116 @ `b06390b` · **74 tip sync DONE** @ `b06390b1552d10fce00d93be8734dc00d37bca7b` · **70 DONE** · host current with main through Products #116 · Teams **#117** / Integrations **#118** / Actor **#119** / FLOW-03 **#120** / Contract **#121** / conversation-bar **#122** open, not merged — Actions spending-limit, not DONE · buffer **87–94** not merged · item **8** deferred) |
| Later gates | Multi-tenant → bounded autonomy | **AHEAD** |

**Hard rule:** productionWrites **OFF**; FACTORY_MODE **PAUSED** until Daniel directs otherwise. Write class `factory.self_build.supervised` is **named only** — no expansion / **no flip**. No Director keys on host. Client products stay **parked**.

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
- **33:** Portfolio + Work — **closed via later 54** · factory-bridge **PR #89** (was #77 in progress)
- **34:** Teams **DONE** — factory-bridge **PR #78**
- **35:** FLOW-02 universal record **DONE** — factory-bridge **PR #79**
- **36:** FLOW-04 thin RO — **closed via later 59** · factory-bridge **PR #94** (was #80 in progress)
- Software PR numbers from Daniel’s item-38 brief; `factory-bridge` was **not reachable** here
- FACTORY_MODE **PAUSED** · productionWrites **false** · Director keys **off host**
- Write class `factory.self_build.supervised` named only — **no expansion / no flip**
- Ellisbrook live attach remains **NO-GO**

## Factory OS items 37–43 (2026-09-20 ~00:50 EDT)
- **37:** standing host redeploy **DONE** — earlier ~`53512c5` · auth + **`HTTP_BRIDGE`** remain · **PAUSED** · later redeploy is item **43**
- **38:** Pages 31–36 **already live** — this repo **PR #15** @ `9d91184`
- **39:** Discover family shells **DONE** — factory-bridge **PR #81** merged (thin shells; not full Discover journeys)
- **40:** Evidence & Receipts ledger **DONE** — factory-bridge **PR #82** merged @ `ca5fbb0bf5e8bad66daec9be0861bfab8f371efc` (thin ledger)
- **41:** Integrations shell **DONE** — factory-bridge **PR #83** merged @ `0d7c7ca3b7585043ad6cd6c1d785402af5f41c96` (thin shell)
- **42:** Home next-best-action **DONE** — factory-bridge **PR #84** merged @ `eb6fe902f1aa7d0a227e315443c075c55f6cd6f1` (thin NBA; cost stays **`UNAVAILABLE`**)
- **43:** standing host Factory OS redeploy **DONE** — factory-bridge origin/main `ca5fbb0bf5e8bad66daec9be0861bfab8f371efc` (includes **#81–#84**) · probe ANON HTTP **307** · Bridge health **200** · evidenceClass **`HTTP_BRIDGE`** · **PAUSED**
- Software PR numbers **#81–#84** and merge SHAs from Daniel’s item-44 brief; `factory-bridge` was **not reachable** here. Item **43** host SHA + probe facts are from Daniel’s item-43 brief.
- FACTORY_MODE **PAUSED** · productionWrites **false** · Director keys **off host**
- Write class `factory.self_build.supervised` named only — **no expansion / no flip**
- Ellisbrook live attach remains **NO-GO**

## Factory OS items 45–65 (2026-09-20 ~03:15 EDT)
- **45:** Pages 37–43 **already live** — this repo **PR #17** @ `fb84e26`
- **46–48:** Discover family deepen **DONE** — factory-bridge **PR #87** (thin deepen; not full Discover journeys)
- **49–50:** Evidence & Receipts deepen **DONE** — factory-bridge **PR #86** (thin deepen; not full challenge-id bind)
- **51–52:** Integrations deepen **DONE** — factory-bridge **PR #88** (thin deepen; adapter freeze still open)
- **53:** Home next-best-action **DONE** — factory-bridge **PR #85** (thin NBA; cost stays **`UNAVAILABLE`**)
- **54:** Portfolio + Work **DONE** — factory-bridge **PR #89** (closes 33; thin, not full LIVE FACTORY)
- **55:** Teams **DONE** — factory-bridge **PR #90** (thin roster; not full People & Access)
- **56–59:** FLOW-01..04 **DONE** — factory-bridge **PR #91–#94** (56 #91 · 57 #92 · 58 #93 · 59 #94 closes 36; still not full journeys)
- **60:** Discover universal record **DONE** — factory-bridge **PR #95**
- **61:** Evidence universal record **DONE** — factory-bridge **PR #97**
- **62:** Decision Inbox **DONE** — factory-bridge **PR #98** (deepen; not a write-class flip)
- **63:** conversation bar **DONE** — factory-bridge **PR #96** (still **RO**; no mutating intents)
- **64:** Home strip **DONE** — factory-bridge **PR #99** (cost stays **`UNAVAILABLE`**)
- **65:** Work→receipt **DONE** — factory-bridge **PR #100** (thin bind; not full LIVE FACTORY ledger)
- **66:** standing host redeploy **DONE** — operator · auth + **`HTTP_BRIDGE`** remain · **PAUSED**
- **67:** this Pages refresh — `ai-factory-status` board only (PR #18 / #19 follow-ups)
- **68:** host smoke **PASS** — operator · **PAUSED** / writes false
- **69:** standing host redeploy **DONE** — factory-bridge main `01f880b` · probe ANON HTTP **307** · evidenceClass **`HTTP_BRIDGE`** · **PAUSED** / writes false
- **70:** Pages final host-tip sync **DONE** — same tip SHA `b06390b1552d10fce00d93be8734dc00d37bca7b` · host is current with main through Products #116
- **71:** write-class design note **DONE** — factory-bridge `24dca85` · docs only · `factory.self_build.supervised` named · **no flip**
- **72:** nav sync **DONE** — factory-bridge main `6f66f6f`
- **73:** host ceremony **PASS** — operator · supervised · writes stayed false · **PAUSED**
- **74:** final host tip sync **DONE** — standing host tip synced to factory-bridge main `b06390b1552d10fce00d93be8734dc00d37bca7b` (includes Products #116) · evidence `74b_HOST_TIP_SYNC_20260920T091034Z.md` · anon GET / → 307 /login · `/api/status` → 401 `LOCAL_AUTH_REQUIRED` · factoryMode **PAUSED** · productionWrites **false** · authed evidenceClass **`HTTP_BRIDGE`** · bind `127.0.0.1:3210` only
- **open:** Teams **#117** · Integrations **#118** · Actor **#119** · FLOW-03 **#120** (may still be open) · Contract **#121** · conversation-bar **#122** — open, not merged · blocked on GitHub Actions spending-limit · buffer **87–94** not merged · **not DONE**
- **8:** still **deferred** (needs Daniel secret) · not claimed
- **75:** Environments **DONE** — factory-bridge **PR #105** @ `80b1cfb` (thin; not full env records)
- **76:** Monitoring **DONE** — factory-bridge **PR #106** @ `15eb0af` (after FLOW03-EV-MONITORING dedupe; thin)
- **77:** Incidents **DONE** — factory-bridge **PR #104** @ `91c091a` (thin; not full incident/postmortem)
- **78:** Improvement **DONE** — factory-bridge **PR #107** @ `1c46ca5` (thin; not full FIX/IMPROVE chain)
- **79:** Sales **DONE** — factory-bridge **PR #108** @ `9285da8` (thin; not full pipeline/proposal journey)
- **80:** Quotes **DONE** — factory-bridge **PR #109** @ `6033a2b` (thin; not full quote/proposal journey)
- **81:** Customers **DONE** — factory-bridge **PR #111** @ `eca85b3` (thin; not full Customer 360)
- **82:** Margin **DONE** — factory-bridge **PR #112** @ `9c66122` (thin; not full Lead→Margin / 18-gate)
- **83:** Delivery **DONE** — factory-bridge **PR #113** @ `c0fe95a` (thin; not full gate chain)
- **84:** Releases **DONE** — factory-bridge **PR #114** @ `0ec4c3d` (thin; not full candidate/calendar/promote)
- **85:** Roadmaps **DONE** — factory-bridge **PR #115** @ `9659603` (thin; not full timeline/critical-path)
- **86:** Products **DONE** — factory-bridge **PR #116** @ `b06390b` (thin; not full Product vs Project / health)
- **docs:** factory-bridge **PR #101** · **#110** on main (briefed; subject/SHA not in this brief — not invented)
- Overnight software PR numbers **#85–#101** from Daniel’s item-67 brief; `factory-bridge` was **not reachable** here. Merge SHAs for those PRs were **not** in the brief — not invented.
- FACTORY_MODE **PAUSED** · productionWrites **false** · Director keys **off host**
- Write class `factory.self_build.supervised` named only — **no expansion / no flip**
- Ellisbrook live attach remains **NO-GO**
