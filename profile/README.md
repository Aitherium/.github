# The Aither World

**An operating system for agents.** A Linux you can hand to one, the runtimes it
works in, and the tools it works with.

Every brick below **installs on its own, runs offline, and needs no account.**

![bricks](https://img.shields.io/badge/bricks-72-4c6ef5)
![publishing metrics](https://img.shields.io/badge/publishing%20live%20metrics-69%2F72-4c6ef5)
![planned](https://img.shields.io/badge/named%20%26%20not%20yet%20built-19-8a8a99)

➤ **[Browse the whole ecosystem](https://aitherium.github.io/)** — live, from each repo's own manifest.

---

## The bricks, in layers

**`awharness`** — the super agent harness. One name for the kit, the shell and the bricks an agent works with, taken together. It is a harness that sits above other harnesses: the shell drives Claude Code, Codex and the rest as real products, and the bricks give every one of them the same memory, jobs, leases, permits and tools.

- **Today:** There is no single install. `pip install awdk` and `npm i -g @aitherium/awsh` are two commands, and each other brick installs on its own line. `adk harness parts` reads this list and reports which parts this machine has, at what version, and the install line for each one it lacks.
- **Planned, not built:** One install command that brings the composed bricks up together, and one process that starts them. Neither exists; nothing by this name is published.
- **Composed (11, bold below):** `awdk` `awsh` `awskills` `awm` `awgraph` `awrun` `awrise` `awgit` `awpermit` `awrelay` `awnode`

It is one of a family:

| name | reads as | what it does | bricks it composes | members that are not bricks |
|---|---|---|---|---|
| **`awharness`** | Aither World Harness | The super agent harness | `awdk` `awsh` `awskills` `awm` `awgraph` `awrun` `awrise` `awgit` `awpermit` `awrelay` `awnode` | — |
| **`awmodel`** | Aither World Model | Predict what the world does next | `awpredict` `awgym` `awm` | `WorldModel` (service) · `system-world-model` (library) · `LatentPredictor` (library) · `LearnedWorldModel` (library) · `gym-world-model-tools` (tools) |
| **`awengine`** | Aither World Engine | Run worlds, and imagine what comes next in them | `awsaga` | `AitherSaga` (service) · `Prometheus` (service) · `AitherCNS` (service) · `Prospector` (module) |

**`awmodel`** — The pieces that predict what an environment does next and score how wrong the prediction was. An agent run by the harness asks it before acting; a world run by the engine is one of the things it is asked about.

- **Today:** One installable brick sits at the centre: `awpredict` (a JEPA-style latent predictor and a lighter transition model, with a lookup table to beat). `awgym` is a game it can watch, and `awm` predicts an action's outcome from remembered state. The other parts are code inside the platform, not packages: a belief graph over fleet events, a model of the platform's own services, and two learned predictors used by the planner. They are separate models; nothing joins them into one.
- **Planned, not built:** One model the parts share, and one command that asks it. Neither exists; nothing by this name is published.
- **Start here:** `awpredict engines`
- **`awm` is also composed by another sibling, on purpose:** Memory is composed by the harness, and its `awm_world_state` and `awm_predict` tools encode remembered state and predict an action's outcome from it, which is this grouping's job too.
- `WorldModel` (service, not a brick): One belief graph over fleet events — entities, relations and what is expected next.
- `system-world-model` (library, not a brick): A model of the platform itself — which services are about to fail, and what happens if one does.
- `LatentPredictor` (library, not a brick): A JEPA-style latent predictor that records the transitions that surprised it.
- `LearnedWorldModel` (library, not a brick): A small neural transition predictor for the planner, with a lookup table until it has seen enough.
- `gym-world-model-tools` (tools, not a brick): The gym's model as tools — encode a grid, predict the next one, score the surprise, train.

**`awengine`** — The pieces that run a world: a story takes a turn a checker can refuse, a simulation advances by a tick, and the platform's own senses are rolled forward as a dream. The harness runs the agents that live in these worlds; the model is what predicts them.

- **Today:** One brick, `awsaga`, is registered and not yet installable. The rest are fleet services, not packages: AitherSaga keeps story projects and turns, Prometheus is the tick-based world simulation (not the metrics product, which is a different service), AitherCNS fuses the platform's senses into one state and rolls it forward, and Prospector is a failure-forecast head inside AitherCNS. AitherCNS and Prospector are off unless switched on. Each runs on its own; there is no single engine process, and `saga_continuity_check` is a gateway tool, not a command a stranger can install.
- **Planned, not built:** One engine a world pack starts, with the simulation and the imagination behind one door. Neither exists; nothing by this name is published.
- **Start here:** `saga_continuity_check`
- `AitherSaga` (service, not a brick): Story projects, characters, places and turns, with a continuity check.
- `Prometheus` (service, not a brick): The world simulation — lives, factions, economy and weather, advanced tick by tick.
- `AitherCNS` (service, not a brick): Fuses the platform's senses into one state and rolls it forward — digest, imagine, dream.
- `Prospector` (module, not a brick): A failure-forecast head inside AitherCNS — what the fleet's telemetry is imagined to do next.

Products built from these bricks:

| product | reads as | what it is | try it | page |
|---|---|---|---|---|
| **`awtab`** | Aither World Tab | A whole agent in one browser tab | [aitherium.com/gobbonet/chat.html](https://aitherium.com/gobbonet/chat.html) | [https://aitherium.com/awtab](https://aitherium.com/awtab) |

**`awtab`** — One browser tab runs a 1-bit language model on the visitor's GPU through WebGPU, a tool-calling agent loop and an on-device embedder. There is no inference server: the model, the tools and the search all run inside the tab.

- **Today:** Live in a WebGPU browser at aitherium.com/gobbonet/chat.html. Two model sizes from PrismML's Bonsai family (1.7B and 4B) download once and the browser caches them; the tools run in a worker inside the tab. It has been measured on one GPU class only.
- **Planned, not built:** Reloading with no network, the smaller 384-d embedder in the tab, and measurements on more than one class of GPU. None of these is done yet. awtab is a page, not a package: nothing by this name is on npm or PyPI.
- **Claim, checked 2026-11-13:** As of 13 November 2026 we found no other browser stack that runs a 1-bit model, a tool-calling agent loop and an on-device embedder together in one tab, with no inference server.
- **Limit:** It needs a browser with WebGPU and a GPU it can use.
- **Limit:** The first load downloads 248 MB (1.7B) to 572 MB (4B) before the first answer; after that the browser cache serves it.
- **Limit:** Search downloads its embedder (the 1024-d one) the first time it is used.
- **Limit:** Measured on one GPU class only, and reloading with no network has not been tested.
- **Built from:** `awkit`; not bricks: `webml-runtime` (library) · `tab-tool-loop` (library) · `tab-embedder` (module) · `gobbonet-chat` (module)
- `webml-runtime` (library, not a brick): Runs the 1-bit model on the visitor's GPU through WebGPU. Proprietary, and withheld from the public awkit package.
- `tab-tool-loop` (library, not a brick): The agent loop in the tab — the model asks for a tool, a worker runs it, the answer goes back to the model.
- `tab-embedder` (module, not a brick): Turns text into vectors on the visitor's GPU, inside the tab, so search needs no embedding server.
- `gobbonet-chat` (module, not a brick): The chat page people open, wired to the model, the tools and the embedder in the tab.

<picture>
  <source media="(prefers-color-scheme: dark)" srcset="https://aitherium.github.io/brick-map-dark.svg">
  <img alt="awharness: 98 bricks in 8 layers — Harness, Memory and knowledge, Reasoning and learning, Work, Trust, Reach, Senses and media, Substrate" src="https://aitherium.github.io/brick-map-light.svg">
</picture>

| layer | what it is for | bricks |
|---|---|---|
| **Harness** | Build an agent, run it, and drive other agent harnesses. | [**awsh**](https://github.com/Aitherium/awsh) · [**awdk**](https://github.com/Aitherium/awdk) · [**awskills**](https://github.com/Aitherium/awskills) · [awpack](https://github.com/Aitherium/awpack) · [awflow](https://github.com/Aitherium/awflow) · [awrepl](https://github.com/Aitherium/awrepl) · [awsettings](https://github.com/Aitherium/awsettings) · [awfocus](https://github.com/Aitherium/awfocus) · awresume *(planned)* · awmod *(planned)* · awcap *(planned)* |
| **Memory and knowledge** | What an agent remembers, and what it can look up. | [**awm**](https://github.com/Aitherium/awm) · [**awgraph**](https://github.com/Aitherium/awgraph) · [awbrain](https://github.com/Aitherium/awbrain) · [awknowledge](https://github.com/Aitherium/awknowledge) · [awkno](https://github.com/Aitherium/awkno) · [awembed](https://github.com/Aitherium/awembed) · awdata *(planned)* · [awmine](https://github.com/Aitherium/awmine) · awindex *(not published)* · [awfind](https://github.com/Aitherium/awfind) · [awresearch](https://github.com/Aitherium/awresearch) |
| **Reasoning and learning** | Think a hard question through, decide, and improve from the result. | [**awpredict**](https://github.com/Aitherium/awpredict) · [**awgym**](https://github.com/Aitherium/awgym) · [awreason](https://github.com/Aitherium/awreason) · [awrecurse](https://github.com/Aitherium/awrecurse) · [awprism](https://github.com/Aitherium/awprism) · [awdecide](https://github.com/Aitherium/awdecide) · [awdelphi](https://github.com/Aitherium/awdelphi) · [awevolve](https://github.com/Aitherium/awevolve) · awlab *(planned)* · [awrena](https://github.com/Aitherium/awrena) · [awclassify](https://github.com/Aitherium/awclassify) · [awtoll](https://github.com/Aitherium/awtoll) |
| **Work** | Jobs, schedules, version control and the files work leaves behind. | [**awrun**](https://github.com/Aitherium/awrun) · [**awrise**](https://github.com/Aitherium/awrise) · [**awgit**](https://github.com/Aitherium/awgit) · [awpool](https://github.com/Aitherium/awpool) · [awedgerunner](https://github.com/Aitherium/awedgerunner) · [awrecover](https://github.com/Aitherium/awrecover) · [awstorage](https://github.com/Aitherium/awstorage) · [awrtifact](https://github.com/Aitherium/awrtifact) · [awshare](https://github.com/Aitherium/awshare) · awsync *(merged)* · [awreport](https://github.com/Aitherium/awreport) · awlog *(planned)* · [awtax](https://github.com/Aitherium/awtax) · [awsuite](https://github.com/Aitherium/awsuite) |
| **Trust** | Who is calling, what they may do, and the record of what they did. | [**awpermit**](https://github.com/Aitherium/awpermit) · [awnest](https://github.com/Aitherium/awnest) · awprove *(not published)* · [awseal](https://github.com/Aitherium/awseal) · [awdit](https://github.com/Aitherium/awdit) · [awbac](https://github.com/Aitherium/awbac) · [awiam](https://github.com/Aitherium/awiam) · [awwall](https://github.com/Aitherium/awwall) · [awnboard](https://github.com/Aitherium/awnboard) · awscope *(planned)* · awgov *(planned)* |
| **Reach** | Messages, people, devices and the network between them. | [**awrelay**](https://github.com/Aitherium/awrelay) · [awask](https://github.com/Aitherium/awask) · [awmail](https://github.com/Aitherium/awmail) · [awdiscord](https://github.com/Aitherium/awdiscord) · [awdesk](https://github.com/Aitherium/awdesk) · [AitherConnect](https://github.com/Aitherium/AitherConnect) · [awtunnel](https://github.com/Aitherium/awtunnel) · [awnet](https://github.com/Aitherium/awnet) · awspaces *(planned)* · awplay *(planned)* · awcrowd *(planned)* · awgather *(planned)* |
| **Senses and media** | See, hear, browse, render and show. | **awsaga** *(planned)* · [awbrowse](https://github.com/Aitherium/awbrowse) · [awvoice](https://github.com/Aitherium/awvoice) · [awvision](https://github.com/Aitherium/awvision) · [awscreen](https://github.com/Aitherium/awscreen) · awcams *(not published)* · [awkit](https://github.com/Aitherium/awkit) · [awbeads](https://github.com/Aitherium/awbeads) · [awsprite](https://github.com/Aitherium/awsprite) · [awavatar](https://github.com/Aitherium/awavatar) · awdeck *(planned)* · awforge *(planned)* · mediaforge *(not published)* · awiris *(planned)* · [gawbbonet](https://github.com/Aitherium/gawbbonet) · awexpress *(planned)* |
| **Substrate** | The OS, the gateway and the model serving everything above runs on. | [**awnode**](https://github.com/Aitherium/awnode) · [awnix](https://github.com/Aitherium/awnix) · aitheros *(not published)* · awdaemons *(not published)* · [awrouter](https://github.com/Aitherium/awrouter) · [awswarm](https://github.com/Aitherium/awswarm) · awcache *(planned)* · [awbonsai](https://github.com/Aitherium/awbonsai) · awasp *(planned)* · [aitherkvcache](https://github.com/Aitherium/aitherkvcache) · [AitherZero](https://github.com/Aitherium/AitherZero) |

Every brick with its one-line purpose and status, and a Mermaid version of the map: [brick-map.md](https://github.com/Aitherium/Aitherium.github.io/blob/main/brick-map.md).

## What is here

| brick | what it replaces trusting | install | files | tests |
|---|---|---|---|---|
| [awdk](https://aitherium.github.io/awdk/) | Build AI agent fleets — 3 lines, any backend, local or cloud. | `pip install awdk` | 2,826 | 845 |
| [awskills](https://aitherium.github.io/awskills/) | Portable agent skills — self-contained procedures an agent loads on demand. | `git clone https://github.com/Aitherium/awskills` | 214 | 1 |
| [awpack](https://aitherium.github.io/awpack/) | First-party agent packs — the ones we build, versioned and installable on their own. | `git clone https://github.com/Aitherium/awpack` | 51 | 1 |
| [awm](https://aitherium.github.io/awm/) | A portable, scoped agent memory. | `pip install awm` | 63 | 23 |
| `aitheros` | One file you run, and the machine has a local AI stack. | — | — | — |
| `awdaemons` | The AitherOS daemons as one file — no Python, no signing, no install. | — | — | — |
| [awdesk](https://aitherium.github.io/awdesk/) | Aither World Desk -- the desktop body of AitherOS Online: tray, avatars, decision cards, the Living Desktop as an overlay. | `see the repo -- Electron app (npm install && npx electron .)` | 1,251 | 1 |
| [awnode](https://aitherium.github.io/awnode/) | A lightweight local gateway — bridges your apps to the AI backends you chose. | `pip install awnode` | 93 | 25 |
| [awrun](https://aitherium.github.io/awrun/) | A priority-aware queue and dispatcher for agentic runs and ad-hoc CI builds. It also judges whether the runner pool is big enough for the queue it is draining, and can ask a host to grow it -- reserving capacity is zero-sum, so a saturated pool needs more of it, not a different share of it. | `pip install awrun` | 59 | 17 |
| [awpool](https://aitherium.github.io/awpool/) | The free half of the elastic work pool: dispatches public-safe work onto the free GitHub-hosted runners of the public aw* mirrors, so their idle CI minutes become compute. awrun remains the paid/self-hosted lane; this is its free twin. | `pip install awpool` | 26 | 4 |
| [awedgerunner](https://aitherium.github.io/awedgerunner/) | Run agent and CI work on edge runners nobody has to rack -- a volunteer's idle GPU, a phone on your own mesh, an edge worker, a free or spot CI runner -- under a lease with a hard budget cap, a named payer and an expiry. | `pip install awedgerunner` | 23 | 3 |
| [awgraph](https://aitherium.github.io/awgraph/) | A semantic code graph for agents — AST + tree-sitter, call graphs. | `pip install awgraph` | 68 | 26 |
| [awgit](https://aitherium.github.io/awgit/) | Semantic version control on top of git — edit-ops and leases. | `pip install awgit` | 122 | 35 |
| [awdelphi](https://aitherium.github.io/awdelphi/) | Anonymous multi-round expert panels — a converged answer with a trace. | `pip install awdelphi` | 37 | 7 |
| [awclassify](https://aitherium.github.io/awclassify/) | Classify any document -- what it is, who may read it, who it is for, what it is about. | `pip install awclassify` | 29 | 2 |
| [awdecide](https://aitherium.github.io/awdecide/) | One typed-decision contract -- choice / score / bool with a probability -- over a ladder of backends you already run (rules, tiny local models, an LLM's logprobs), fail-closed, with a Brier ledger that resolves every decision against its outcome. | `pip install awdecide` | 92 | 11 |
| [awtoll](https://aitherium.github.io/awtoll/) | What every tool call costs you in context, measured from your own transcripts. | `pip install awtoll` | 31 | 1 |
| [awseal](https://aitherium.github.io/awseal/) | Sign an artifact so a stranger can verify it. | `pip install awseal` | 29 | 2 |
| [awshare](https://aitherium.github.io/awshare/) | Publish an artifact and fetch it back verified. | `pip install awshare` | 32 | 4 |
| [awsuite](https://aitherium.github.io/awsuite/) | Your Google Workspace as agent tools, and no write happens without a yes. | `pip install awsuite` | 49 | 8 |
| [awdit](https://aitherium.github.io/awdit/) | An append-only audit trail whose gaps are DETECTABLE. | `pip install awdit` | 26 | 1 |
| [awbac](https://aitherium.github.io/awbac/) | Role-based access control that fails closed and explains itself. | `pip install awbac` | 25 | 1 |
| [awiam](https://aitherium.github.io/awiam/) | Who is this caller? A directory and session store that fails honestly. | `pip install awiam` | 26 | 1 |
| [awtunnel](https://aitherium.github.io/awtunnel/) | Reach a service that has no public address. | `pip install awtunnel` | 34 | 7 |
| [awpermit](https://aitherium.github.io/awpermit/) | Let an agent through your door with a scope, a spend cap, and someone accountable. | `pip install git+https://github.com/Aitherium/awpermit` | 26 | 2 |
| [awnest](https://aitherium.github.io/awnest/) | Prove there is a human before you let them into the nest. | `pip install awnest` | 35 | 4 |
| [awrena](https://aitherium.github.io/awrena/) | Put two agents head to head and get a verdict you can check. | `pip install awrena` | 21 | 1 |
| [awnboard](https://aitherium.github.io/awnboard/) | A front gate you can put in front of anything, and hand someone the key to. | `pip install awnboard` | 27 | 2 |
| [awnix](https://aitherium.github.io/awnix/) | A Linux you can hand to an agent — immutable base, capabilities included. | `podman build -t awnix:latest -f Containerfile .` | 25 | 0 |
| [awrecover](https://aitherium.github.io/awrecover/) | Labelled snapshots with an all-or-nothing restore. | `pip install awrecover` | 30 | 6 |
| [awstorage](https://aitherium.github.io/awstorage/) | Every drive on every node, indexed, classified and diffed -- so you can see what you own before you delete it. | `pip install awstorage` | 82 | 28 |
| [awrelay](https://aitherium.github.io/awrelay/) | Portable agent messaging — findings, alerts, coordination. | `pip install awrelay` | 51 | 15 |
| [awask](https://aitherium.github.io/awask/) | Your agent asks you a question — and acts on your answer. | `pip install awask` | 76 | 17 |
| [awmail](https://aitherium.github.io/awmail/) | Give an agent an email address — send, and actually receive. | `pip install awmail` | 28 | 2 |
| [awdiscord](https://aitherium.github.io/awdiscord/) | Put any agent on Discord as a real bot, with an operator in the loop. | `pip install git+https://github.com/Aitherium/awdiscord.git` | 218 | 116 |
| `mediaforge` | The creative studio — search the boards, render scenes, keep the character. | — | — | — |
| [awnet](https://aitherium.github.io/awnet/) | The agentic web — agents host a mesh, and agents join one. | `pip install awnet` | 26 | 2 |
| [awswarm](https://aitherium.github.io/awswarm/) | Run one model too big for any single GPU across a pool of small ones. | `pip install awswarm` | 38 | 10 |
| [awfind](https://aitherium.github.io/awfind/) | A portable search client — query, results, ranking. | `pip install awfind` | 37 | 7 |
| `awindex` | A curated, git-backed map of the internet — .aither keywords and trust you can check. | — | — | — |
| [awbrowse](https://aitherium.github.io/awbrowse/) | A portable browser client — navigate, console, network, DOM, screenshot. | `pip install awbrowse` | 30 | 4 |
| `awprove` | Drive a page as the real user, check what rendered, and get a test that goes red if it stops being true. | — | — | — |
| [awvoice](https://aitherium.github.io/awvoice/) | Hear and speak — transcribe audio, synthesize a voice. | `pip install awvoice` | 42 | 10 |
| [awvision](https://aitherium.github.io/awvision/) | See an image — describe it, ask it a question, compare two. | `pip install awvision` | 29 | 4 |
| `awcams` | Private camera recording and one-line event summaries, on storage you own. | — | — | — |
| [awscreen](https://aitherium.github.io/awscreen/) | See this machine — what is on screen, and where to click it. | `pip install awscreen` | 66 | 22 |
| [awkit](https://aitherium.github.io/awkit/) | Render an agent panel from a tool result — one component, any React app. | `git clone https://github.com/Aitherium/awkit` | — | — |
| [awbeads](https://aitherium.github.io/awbeads/) | A spatial canvas for a page — arrange things, connect them, and keep the arrangement. | `git clone https://github.com/Aitherium/awbeads` | — | — |
| [awsprite](https://aitherium.github.io/awsprite/) | Hatch a companion that grows only from what you teach it, then take it home. | `pip install awsprite` | 34 | 8 |
| [awbonsai](https://aitherium.github.io/awbonsai/) | Run a real model in the visitor's own browser — no server round trip, no upload. | `git clone https://github.com/Aitherium/awbonsai` | — | — |
| [awknowledge](https://aitherium.github.io/awknowledge/) | How to run a coding agent so the result survives — the laws, with evidence. | `read it — https://aitherium.github.io/awknowledge/` | 146 | 0 |
| [awbrain](https://aitherium.github.io/awbrain/) | Your history as a wiki of linked markdown — claims pinned to the evidence. | `pip install awbrain` | 28 | 1 |
| [gawbbonet](https://aitherium.github.io/gawbbonet/) | GobboNet campaigns with a real agent brain — scoped memory, graph recall. | `pip install gawbbonet` | 19 | 1 |
| [aitherkvcache](https://aitherium.github.io/aitherkvcache/) | Near-optimal KV cache quantization for LLM inference — sub-byte compression. | `pip install aither-kvcache` | 73 | 8 |
| [awrtifact](https://aitherium.github.io/awrtifact/) | Deliberately chunk artifacts into GitHub release assets — the productized aitherkvcache mirror lane. | `pip install awrtifact` | 77 | 24 |
| [AitherZero](https://aitherium.github.io/AitherZero/) | PowerShell 7+ automation framework — numbered, self-describing scripts. | `git clone https://github.com/Aitherium/AitherZero` | 1,685 | 51 |
| [AitherConnect](https://aitherium.github.io/AitherConnect/) | Browser extension — federated AI search, page context, and the Living OS overlay. | `https://chromewebstore.google.com/detail/awconnect/peeojgjhjficedkncdejbfnacooodbak` | 11 | 0 |
| [awreason](https://aitherium.github.io/awreason/) | A portable reasoning client — sessions, phases, thoughts, and the chain that produced the answer. | `pip install awreason` | 24 | 1 |
| [awrecurse](https://aitherium.github.io/awrecurse/) | Answer a question over a context far larger than the window — recursively, with the trace kept. | `pip install awrecurse` | 29 | 4 |
| [awprism](https://aitherium.github.io/awprism/) | Turn a failure into ranked hypotheses — and say what would confirm each one. | `pip install awprism` | 34 | 5 |
| [awrepl](https://aitherium.github.io/awrepl/) | A REPL an agent can actually use — state that survives between turns. | `pip install awrepl` | 32 | 5 |
| [awreport](https://aitherium.github.io/awreport/) | File a bug report that has already scrubbed your secrets and collapsed the duplicate. | `pip install awreport` | 33 | 7 |
| [awresearch](https://aitherium.github.io/awresearch/) | Ask a research question, get a cited report you can check. | `pip install awresearch` | 34 | 4 |
| [awfocus](https://aitherium.github.io/awfocus/) | See, search and steer every Claude session from one command. | `pip install awfocus` | 33 | 2 |
| [awgym](https://aitherium.github.io/awgym/) | An ARC training gym — a game a world model can watch, and six roles that play through it. | `pip install awgym` | 71 | 13 |
| [awpredict](https://aitherium.github.io/awpredict/) | Predict what your environment does next, and how surprised you were. | `pip install git+https://github.com/Aitherium/awpredict.git` | 56 | 13 |
| [awevolve](https://aitherium.github.io/awevolve/) | Point an agent at a file and a command that scores it, and let it improve. | `pip install awevolve` | 28 | 1 |
| [awsh](https://aitherium.github.io/awsh/) | Your terminal answers you -- type a question where a command would go. | `npm i -g @aitherium/awsh` | 1,255 | 106 |
| [awmine](https://aitherium.github.io/awmine/) | Mine what your agents did -- outcomes, lessons and procedures out of the transcripts they left behind. | `pip install git+https://github.com/Aitherium/awmine.git` | 53 | 21 |
| [awrise](https://aitherium.github.io/awrise/) | Wake an agent on a schedule, let it do one thing, and put it back to sleep. | `pip install awrise` | 70 | 34 |
| [awkno](https://aitherium.github.io/awkno/) | The man page for the Aither World — every brick, stack and law, offline. | `pip install awkno` | 214 | 3 |
| [awwall](https://aitherium.github.io/awwall/) | Say what a workload may reach, and watch everything else fail closed. | `pip install awwall` | 21 | 2 |
| [awrouter](https://aitherium.github.io/awrouter/) | OpenRouter for your own fleet: pick a model backend by cost/latency/ capability, fail over, fit the context window, stream. Standalone, OpenAI-compatible, no Aither-specifics required to be valuable. | `pip install awrouter` | 34 | 6 |
| [awembed](https://aitherium.github.io/awembed/) | Train an embedding model that knows your corpus, and prove it beats the big one. | `pip install awembed` | 34 | 3 |
| [awtax](https://aitherium.github.io/awtax/) | Turn any tax PDF -- returns, W-2, 1099, statements, even scans -- into structured data you can check. | `pip install awtax` | 26 | 1 |
| [awflow](https://aitherium.github.io/awflow/) | A deterministic workflow runtime — chain agent calls with journal replay and budget control. | `pip install aitherium-awflow` | 31 | 5 |
| [awsettings](https://aitherium.github.io/awsettings/) | Your agent's permissions and config, following you to the next machine. | `pip install awsettings` | 59 | 21 |
| [awavatar](https://aitherium.github.io/awavatar/) | One character spec in, a rigged, animated, multi-style avatar pack out. | `pip install awavatar` | 28 | 3 |

*Files and tests are quoted from each repository's own published manifest, not
counted here. A dash means that repo publishes no manifest yet — never zero,
because a fabricated zero reads as a measurement.*

## Stacks — what to use together

- **The studio** (partial) — `awforge`, `awfind`, `awbrowse`, `awresearch`, `awm`
- **The bare agent VM** (partial) — `awnix`, `awdk`, `awskills`, `awkno`, `awsettings`
- **Senses** (ready) — `awfind`, `awbrowse`, `awvoice`, `awvision`, `awscreen`, `awdk`
- **Avatar ensemble** (partial) — `awdk`, `awsh`, `awvoice`, `awvision`, `awsprite`, `awdesk`
- **Provenance** (partial) — `awseal`, `awshare`, `awdit`, `awbac`
- **Many agents, one repo** (ready) — `awgit`, `awgraph`, `awrelay`, `awm`
- **The front door** (partial) — `awnboard`, `awnest`, `awiam`, `awbac`, `awdit`
- **Aither World Services** (partial) — `awnix`, `awdaemons`, `awrun`, `awiam`, `awbac`, `awdit`, `awseal`, `awrelay`, `awtunnel`, `awpack`
- **Identity, authority, and the record** (partial) — `awiam`, `awbac`, `awdit`
- **One surface — agent panels, not hand-built UIs** (partial) — `awkit`, `awdk`, `awnode`, `awiam`, `awbac`
- **The reasoning loop** (partial) — `awreason`, `awprism`, `awrepl`, `awrecurse`
- **Research you can check** (partial) — `awresearch`, `awfind`, `awbrowse`, `awm`
- **A pool across your own devices** (partial) — `awnet`, `awnode`, `awdk`
- **A personal agent that lives with you -- desk, browser, site, devices, tunnels** (partial) — `awdesk`, `AitherConnect`, `awsprite`, `awdk`, `awm`, `awkno`, `awknowledge`, `awnboard`, `awiam`, `awtunnel`, `awnet`, `awnode`, `awnix`, `awsh`
- **Grow a companion in the browser, then take it home** (partial) — `awsprite`, `awbonsai`, `awdk`, `awsh`, `awnode`
- **The inference commons -- pool compute, storage and caches across strangers' nodes** (partial) — `awnix`, `awnode`, `awnet`, `awcache`, `awswarm`, `awpool`, `aitherkvcache`, `awrtifact`, `awtunnel`, `awwall`, `awedgerunner`
- **Retrieval you trained yourself** (partial) — `awembed`, `awdata`, `awgraph`, `awfind`, `awm`, `awdk`
- **Dark Matters Living World** (partial) — `awavatar`, `awdk`, `awdecide`, `awsprite`, `awrtifact`, `awrun`
- **The Creator Stack — Saga + Media Forge + Iris on your own machine** (partial) — `awsaga`, `mediaforge`, `awiris`, `awsprite`, `awdesk`, `awbonsai`, `awdk`, `awnode`, `AitherConnect`, `awrtifact`
- **Set and forget -- the clock, the queue, and the record** (partial) — `awrise`, `awrun`, `awrelay`, `awask`, `awdk`
- **The scheduler, open -- route, queue, clock** (partial) — `awrouter`, `awrun`, `awrise`, `awnode`, `awdk`
- **An orchestrator for agent workloads -- stateful, governed, no cluster** (partial) — `awrun`, `awflow`, `awrise`, `awrouter`, `awnode`, `awdk`, `awrepl`, `awnix`, `awiam`, `awbac`, `awdit`, `awseal`, `awshare`
- **A scheduler that learns -- pillars 2, 3 and 6 for wakes** (partial) — `awrise`, `awm`, `awpredict`, `awdecide`, `awembed`, `awevolve`, `awdk`
- **Train what you run -- harvest, train, score, keep-or-revert, on a wake** (partial) — `awrise`, `awdata`, `awlab`, `awevolve`, `awdecide`, `awdk`
- **Mine what you ran -- transcripts in, packs and outcomes out** (partial) — `awmine`, `awtoll`, `awm`, `awdata`, `awdecide`, `awskills`, `awdk`, `awrise`
- **The daily driver** (partial) — `awsh`, `awdk`, `awnode`, `awdesk`, `awskills`
- **The Aither way to run Claude Code** (partial) — `awdk`, `awsh`, `awsettings`, `awskills`, `awknowledge`, `awkno`, `awgit`, `awrelay`, `awm`, `awgraph`, `awfind`, `awfocus`, `awprism`, `awdecide`, `awvoice`
- **The workspace bridge** (partial) — `awsuite`, `awdk`, `awsh`, `awskills`, `awpack`
- **Trust, with the proof** (partial) — `awiam`, `awpermit`, `awtunnel`

## Named, not yet built

Listed on purpose. A named absence can be chased; a silent one is a thing
nobody remembers.

`awcap` · `awexpress` · `awscope` · `awgather` · `awplay` · `awcrowd` · `awspaces` · `awcache` · `awdeck` · `awforge` · `awasp` · `awlab` · `awdata` · `awmod` · `awlog` · `awresume` · `awsaga` · `awiris` · `awgov`

## Built on

The open-source projects under the bricks. Each one is something we actually
run: the registry has to name a file in our repo that proves it before it is
listed here.

[![Blender + Rigify](https://img.shields.io/badge/built%20on-Blender%20%2B%20Rigify-5EC9CC)](https://www.blender.org/) [![CentOS Stream](https://img.shields.io/badge/built%20on-CentOS%20Stream-5EC9CC)](https://www.centos.org/centos-stream/) [![Chromium](https://img.shields.io/badge/built%20on-Chromium-5EC9CC)](https://www.chromium.org/) [![ComfyUI](https://img.shields.io/badge/built%20on-ComfyUI-5EC9CC)](https://github.com/comfyanonymous/ComfyUI) [![Docker](https://img.shields.io/badge/built%20on-Docker-5EC9CC)](https://github.com/moby/moby) [![FFmpeg](https://img.shields.io/badge/built%20on-FFmpeg-5EC9CC)](https://ffmpeg.org/) [![headroom](https://img.shields.io/badge/built%20on-headroom-5EC9CC)](https://github.com/headroomlabs-ai/headroom) [![Hunyuan3D](https://img.shields.io/badge/built%20on-Hunyuan3D-5EC9CC)](https://github.com/Tencent-Hunyuan/Hunyuan3D-2.1) [![LanceDB](https://img.shields.io/badge/built%20on-LanceDB-5EC9CC)](https://github.com/lancedb/lancedb) [![llama.cpp](https://img.shields.io/badge/built%20on-llama.cpp-5EC9CC)](https://github.com/ggml-org/llama.cpp) [![Next.js](https://img.shields.io/badge/built%20on-Next.js-5EC9CC)](https://github.com/vercel/next.js) [![PhotoCraft](https://img.shields.io/badge/built%20on-PhotoCraft-5EC9CC)](https://github.com/storytold/photocraft) [![Playwright](https://img.shields.io/badge/built%20on-Playwright-5EC9CC)](https://github.com/microsoft/playwright) [![Podman](https://img.shields.io/badge/built%20on-Podman-5EC9CC)](https://github.com/containers/podman) [![REA (Reverse Engineer Anything)](https://img.shields.io/badge/built%20on-REA%20%28Reverse%20Engineer%20Anything%29-5EC9CC)](https://github.com/morluto/rea) [![React](https://img.shields.io/badge/built%20on-React-5EC9CC)](https://github.com/facebook/react) [![repowise](https://img.shields.io/badge/built%20on-repowise-5EC9CC)](https://github.com/repowise-dev/repowise) [![SANA](https://img.shields.io/badge/built%20on-SANA-5EC9CC)](https://github.com/NVlabs/Sana) [![vLLM](https://img.shields.io/badge/built%20on-vLLM-5EC9CC)](https://github.com/vllm-project/vllm) [![WireGuard](https://img.shields.io/badge/built%20on-WireGuard-5EC9CC)](https://www.wireguard.com/)

| project | what we run it for | license |
|---|---|---|
| [Blender + Rigify](https://www.blender.org/) | Headless auto-rigging service for generated characters. | `GPL-2.0-or-later` |
| [CentOS Stream](https://www.centos.org/centos-stream/) | Base image of awnix — bootable, immutable, built with bootc. | `Compilation GPL-2.0; each package under its own license; bootc MIT OR Apache-2.0` |
| [Chromium](https://www.chromium.org/) | Headless browser engine for AitherBrowser sessions and smoke tests. | `BSD-3-Clause (plus bundled third-party licenses)` |
| [ComfyUI](https://github.com/comfyanonymous/ComfyUI) | Visual generation engine behind media-forge — images, video, and the 3D stack (Hunyuan3D). | `GPL-3.0` |
| [Docker](https://github.com/moby/moby) | Compose stacks and image builds for the fleet. | `Apache-2.0` |
| [FFmpeg](https://ffmpeg.org/) | Every media transform — frames, mux, HLS transcode. | `LGPL-2.1+ (GPL in some builds)` |
| [headroom](https://github.com/headroomlabs-ai/headroom) | Reversible context compression — a sidecar plus agent-callable tools. | `Apache-2.0` |
| [Hunyuan3D](https://github.com/Tencent-Hunyuan/Hunyuan3D-2.1) | Image-to-3D mesh generation behind AitherMeshGen (standalone API and ComfyUI nodes). Not affiliated with or endorsed by Tencent. | `Tencent Hunyuan 3D 2.1 Community License (territory excludes the EU, UK and South Korea)` |
| [LanceDB](https://github.com/lancedb/lancedb) | Vector store behind AitherNexus. | `Apache-2.0` |
| [llama.cpp](https://github.com/ggml-org/llama.cpp) | Local inference engine — llama-server lanes and the Bonsai models (our PrismML fork). | `MIT` |
| [Next.js](https://github.com/vercel/next.js) | The framework AitherVeil — the portal and Living OS desktop — is built with. | `MIT` |
| [PhotoCraft](https://github.com/storytold/photocraft) | Raster engine behind Media Forge's photo ops (psd_render, psd_layers, photo_adjust, photo_filter, photo_actions, photo_export) -- pinned photocraft-cli 0.3.0 subprocess, sha-checked, never vendored. | `MIT OR Apache-2.0` |
| [Playwright](https://github.com/microsoft/playwright) | Browser automation under AitherBrowser and the AitherVeil e2e suite. | `Apache-2.0` |
| [Podman](https://github.com/containers/podman) | Rootless container runtime; systemd quadlet units for the desktop and appliances. | `Apache-2.0` |
| [REA (Reverse Engineer Anything)](https://github.com/morluto/rea) | Reverse-engineering engine behind the rea toolpack — pinned rea CLI as a sidecar (never vendored), wrapped with our fail-closed obligation ledger and target-auth policy. | `MIT` |
| [React](https://github.com/facebook/react) | UI library for AitherVeil and its desktop apps. | `MIT` |
| [repowise](https://github.com/repowise-dev/repowise) | Codebase-intelligence service (pinned 0.31.0) — wiki, risk and symbol lookup exposed to agents over MCP. | `AGPL-3.0-or-later` |
| [SANA](https://github.com/NVlabs/Sana) | Fast image-generation backend, profile-gated. | `Apache-2.0 (code and the Efficient-Large-Model checkpoints); Gemma terms for its text encoder` |
| [vLLM](https://github.com/vllm-project/vllm) | GPU inference lanes, extended by our vLLM mesh plugin. | `Apache-2.0` |
| [WireGuard](https://www.wireguard.com/) | The private overlay network under AitherNet / AitherMesh. | `GPL-2.0` |

---

<sub>This page is generated from `ecosystem.yaml` and the live manifests. Editing
it by hand will be overwritten — change the registry instead.</sub>
