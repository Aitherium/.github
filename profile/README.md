# The Aither World

**An operating system for agents.** A Linux you can hand to one, the runtimes it
works in, and the tools it works with.

Every brick below **installs on its own, runs offline, and needs no account.**

![bricks](https://img.shields.io/badge/bricks-55-4c6ef5)
![publishing metrics](https://img.shields.io/badge/publishing%20live%20metrics-55%2F55-4c6ef5)
![planned](https://img.shields.io/badge/named%20%26%20not%20yet%20built-15-8a8a99)

➤ **[Browse the whole ecosystem](https://aitherium.github.io/)** — live, from each repo's own manifest.

---

## What is here

| brick | what it replaces trusting | install | files | tests |
|---|---|---|---|---|
| [awdk](https://aitherium.github.io/awdk/) | Build AI agent fleets — 3 lines, any backend, local or cloud. | `pip install awdk` | 1,422 | 351 |
| [awskills](https://aitherium.github.io/awskills/) | Portable agent skills — self-contained procedures an agent loads on demand. | `git clone https://github.com/Aitherium/awskills` | 170 | 1 |
| [awpack](https://aitherium.github.io/awpack/) | First-party agent packs — the ones we build, versioned and installable on their own. | `git clone https://github.com/Aitherium/awpack` | 24 | 0 |
| [awm](https://aitherium.github.io/awm/) | A portable, scoped agent memory. | `pip install awm` | 21 | 0 |
| `aitheros` | One file you run, and the machine has a local AI stack. | — | — | — |
| `awdaemons` | The AitherOS daemons as one file — no Python, no signing, no install. | — | — | — |
| [awdesk](https://aitherium.github.io/awdesk/) | Aither World Desk -- the desktop body of AitherOS Online: tray, avatars, decision cards, the Living Desktop as an overlay. | `see the repo -- Electron app (npm install && npx electron .)` | 258 | 0 |
| [awnode](https://aitherium.github.io/awnode/) | A lightweight local gateway — bridges your apps to the AI backends you chose. | `pip install awnode` | 62 | 5 |
| [awrun](https://aitherium.github.io/awrun/) | A priority-aware queue and dispatcher for agentic runs and ad-hoc CI builds. It also judges whether the runner pool is big enough for the queue it is draining, and can ask a host to grow it -- reserving capacity is zero-sum, so a saturated pool needs more of it, not a different share of it. | `pip install awrun` | 36 | 6 |
| [awgraph](https://aitherium.github.io/awgraph/) | A semantic code graph for agents — AST + tree-sitter, call graphs. | `pip install awgraph` | 46 | 15 |
| [awgit](https://aitherium.github.io/awgit/) | Semantic version control on top of git — edit-ops and leases. | `pip install awgit` | 87 | 16 |
| [awdelphi](https://aitherium.github.io/awdelphi/) | Anonymous multi-round expert panels — a converged answer with a trace. | `pip install awdelphi` | 31 | 7 |
| `awclassify` | Classify any document -- what it is, who may read it, who it is for, what it is about. | — | — | — |
| [awtoll](https://aitherium.github.io/awtoll/) | What every tool call costs you in context, measured from your own transcripts. | `pip install awtoll` | 25 | 1 |
| [awseal](https://aitherium.github.io/awseal/) | Sign an artifact so a stranger can verify it. | `pip install awseal` | 21 | 1 |
| [awshare](https://aitherium.github.io/awshare/) | Publish an artifact and fetch it back verified. | `pip install awshare` | 22 | 2 |
| [awdit](https://aitherium.github.io/awdit/) | An append-only audit trail whose gaps are DETECTABLE. | `pip install awdit` | 20 | 1 |
| [awbac](https://aitherium.github.io/awbac/) | Role-based access control that fails closed and explains itself. | `pip install awbac` | 20 | 1 |
| [awiam](https://aitherium.github.io/awiam/) | Who is this caller? A directory and session store that fails honestly. | `pip install awiam` | 20 | 1 |
| [awtunnel](https://aitherium.github.io/awtunnel/) | Reach a service that has no public address. | `pip install awtunnel` | 28 | 7 |
| [awnest](https://aitherium.github.io/awnest/) | Prove there is a human before you let them into the nest. | `pip install awnest` | 30 | 4 |
| [awrena](https://aitherium.github.io/awrena/) | Put two agents head to head and get a verdict you can check. | `pip install awrena` | 16 | 1 |
| [awnboard](https://aitherium.github.io/awnboard/) | A front gate you can put in front of anything, and hand someone the key to. | `pip install awnboard` | 22 | 2 |
| [awnix](https://aitherium.github.io/awnix/) | A Linux you can hand to an agent — immutable base, capabilities included. | `podman build -t awnix:latest -f Containerfile .` | 14 | 0 |
| [awrecover](https://aitherium.github.io/awrecover/) | Labelled snapshots with an all-or-nothing restore. | `pip install awrecover` | 22 | 3 |
| [awstorage](https://aitherium.github.io/awstorage/) | Every drive on every node, indexed, classified and diffed -- so you can see what you own before you delete it. | `pip install awstorage` | 30 | 4 |
| [awrelay](https://aitherium.github.io/awrelay/) | Portable agent messaging — findings, alerts, coordination. | `pip install awrelay` | 37 | 9 |
| [awask](https://aitherium.github.io/awask/) | Your agent asks you a question — and acts on your answer. | `pip install awask` | 44 | 7 |
| [awmail](https://aitherium.github.io/awmail/) | Give an agent an email address — send, and actually receive. | `pip install awmail` | 23 | 2 |
| `mediaforge` | The creative studio — search the boards, render scenes, keep the character. | — | — | — |
| [awnet](https://aitherium.github.io/awnet/) | The agentic web — agents host a mesh, and agents join one. | `pip install awnet` | 21 | 2 |
| `awswarm` | Run one model too big for any single GPU across a pool of small ones. | — | — | — |
| [awfind](https://aitherium.github.io/awfind/) | A portable search client — query, results, ranking. | `pip install awfind` | 24 | 4 |
| [awbrowse](https://aitherium.github.io/awbrowse/) | A portable browser client — navigate, console, network, DOM, screenshot. | `pip install awbrowse` | 23 | 4 |
| `awprove` | Drive a page as the real user, check what rendered, and get a test that goes red if it stops being true. | — | — | — |
| [awvoice](https://aitherium.github.io/awvoice/) | Hear and speak — transcribe audio, synthesize a voice. | `pip install awvoice` | 21 | 2 |
| [awvision](https://aitherium.github.io/awvision/) | See an image — describe it, ask it a question, compare two. | `pip install awvision` | 20 | 2 |
| [awscreen](https://aitherium.github.io/awscreen/) | See this machine — what is on screen, and where to click it. | `pip install awscreen` | 23 | 4 |
| `awkit` | Render an agent panel from a tool result — one component, any React app. | — | — | — |
| `awbeads` | A spatial canvas for a page — arrange things, connect them, and keep the arrangement. | — | — | — |
| `awbonsai` | Run a real model in the visitor's own browser — no server round trip, no upload. | — | — | — |
| [awknowledge](https://aitherium.github.io/awknowledge/) | How to run a coding agent so the result survives — the laws, with evidence. | `read it — https://aitherium.github.io/awknowledge/` | 113 | 0 |
| `awbrain` | Your history as a wiki of linked markdown — claims pinned to the evidence. | — | — | — |
| [gawbbonet](https://aitherium.github.io/gawbbonet/) | GobboNet campaigns with a real agent brain — scoped memory, graph recall. | `pip install gawbbonet` | 14 | 1 |
| [aitherkvcache](https://aitherium.github.io/aitherkvcache/) | Near-optimal KV cache quantization for LLM inference — sub-byte compression. | `pip install aither-kvcache` | 67 | 8 |
| [awrtifact](https://aitherium.github.io/awrtifact/) | Deliberately chunk artifacts into GitHub release assets — the productized aitherkvcache mirror lane. | `pip install awrtifact` | 54 | 13 |
| [AitherZero](https://aitherium.github.io/AitherZero/) | PowerShell 7+ automation framework — numbered, self-describing scripts. | `git clone https://github.com/Aitherium/AitherZero` | 1,622 | 35 |
| [AitherConnect](https://aitherium.github.io/AitherConnect/) | Browser extension — federated AI search, page context, and the Living OS overlay. | `load unpacked — see the repo` | 5 | 0 |
| [awreason](https://aitherium.github.io/awreason/) | A portable reasoning client — sessions, phases, thoughts, and the chain that produced the answer. | `pip install awreason` | 19 | 1 |
| [awrecurse](https://aitherium.github.io/awrecurse/) | Answer a question over a context far larger than the window — recursively, with the trace kept. | `pip install awrecurse` | 22 | 3 |
| [awprism](https://aitherium.github.io/awprism/) | Turn a failure into ranked hypotheses — and say what would confirm each one. | `pip install awprism` | 23 | 2 |
| [awrepl](https://aitherium.github.io/awrepl/) | A REPL an agent can actually use — state that survives between turns. | `pip install awrepl` | 23 | 3 |
| `awreport` | File a bug report that has already scrubbed your secrets and collapsed the duplicate. | — | — | — |
| [awresearch](https://aitherium.github.io/awresearch/) | Ask a research question, get a cited report you can check. | `pip install awresearch` | 28 | 3 |
| [awfocus](https://aitherium.github.io/awfocus/) | See, search and steer every Claude session from one command. | `pip install awfocus` | 26 | 1 |
| [awgym](https://aitherium.github.io/awgym/) | An ARC training gym — a game a world model can watch, and six roles that play through it. | `pip install awgym` | 65 | 12 |
| [awpredict](https://aitherium.github.io/awpredict/) | Predict what your environment does next, and how surprised you were. | `pip install git+https://github.com/Aitherium/awpredict.git` | 44 | 10 |
| `awevolve` | Point an agent at a file and a command that scores it, and let it improve. | — | — | — |
| [awsh](https://aitherium.github.io/awsh/) | Your terminal answers you -- type a question where a command would go. | `npm i -g @aitherium/awsh` | 1,168 | 58 |
| `awmine` | Mine what your agents did -- outcomes, lessons and procedures out of the transcripts they left behind. | — | — | — |
| [awrise](https://aitherium.github.io/awrise/) | Wake an agent on a schedule, let it do one thing, and put it back to sleep. | `pip install awrise` | 58 | 31 |
| [awkno](https://aitherium.github.io/awkno/) | The man page for the Aither World — every brick, stack and law, offline. | `pip install awkno` | 169 | 1 |
| [awwall](https://aitherium.github.io/awwall/) | Say what a workload may reach, and watch everything else fail closed. | `pip install awwall` | 15 | 2 |
| `awrouter` | OpenRouter for your own fleet: pick a model backend by cost/latency/ capability, fail over, fit the context window, stream. Standalone, OpenAI-compatible, no Aither-specifics required to be valuable. | — | — | — |
| [awembed](https://aitherium.github.io/awembed/) | Train an embedding model that knows your corpus, and prove it beats the big one. | `pip install awembed` | 27 | 2 |
| [awtax](https://aitherium.github.io/awtax/) | Turn any tax PDF -- returns, W-2, 1099, statements, even scans -- into structured data you can check. | `pip install awtax` | 21 | 1 |
| [awflow](https://aitherium.github.io/awflow/) | A deterministic workflow runtime — chain agent calls with journal replay and budget control. | `pip install aitherium-awflow` | 24 | 3 |
| [awsettings](https://aitherium.github.io/awsettings/) | Your agent's permissions and config, following you to the next machine. | `pip install awsettings` | 29 | 5 |
| [awavatar](https://aitherium.github.io/awavatar/) | One character spec in, a rigged, animated, multi-style avatar pack out. | `pip install git+https://github.com/Aitherium/awavatar` | 19 | 1 |

*Files and tests are quoted from each repository's own published manifest, not
counted here. A dash means that repo publishes no manifest yet — never zero,
because a fabricated zero reads as a measurement.*

## Stacks — what to use together

- **The studio** (partial) — `awforge`, `awfind`, `awbrowse`, `awresearch`, `awm`
- **The bare agent VM** (partial) — `awnix`, `awdk`, `awskills`, `awkno`, `awsettings`
- **Senses** (ready) — `awfind`, `awbrowse`, `awvoice`, `awvision`, `awscreen`, `awdk`
- **Avatar ensemble** (planned) — `awdk`, `awsh`, `awvoice`, `awvision`, `awsprite`, `awdesk`
- **Provenance** (partial) — `awseal`, `awshare`, `awdit`, `awbac`
- **Many agents, one repo** (ready) — `awgit`, `awgraph`, `awrelay`, `awm`
- **The front door** (partial) — `awnboard`, `awnest`, `awiam`, `awbac`, `awdit`
- **Identity, authority, and the record** (partial) — `awiam`, `awbac`, `awdit`
- **One surface — agent panels, not hand-built UIs** (partial) — `awkit`, `awdk`, `awnode`, `awiam`, `awbac`
- **The reasoning loop** (partial) — `awreason`, `awprism`, `awrepl`, `awrecurse`
- **Research you can check** (partial) — `awresearch`, `awfind`, `awbrowse`, `awm`
- **A pool across your own devices** (partial) — `awnet`, `awnode`, `awdk`
- **A personal agent that lives with you -- desk, browser, site, devices, tunnels** (partial) — `awdesk`, `AitherConnect`, `awsprite`, `awdk`, `awm`, `awkno`, `awknowledge`, `awnboard`, `awiam`, `awtunnel`, `awnet`, `awnode`, `awnix`, `awsh`
- **Grow a companion in the browser, then take it home** (planned) — `awsprite`, `awbonsai`, `awdk`, `awsh`, `awnode`
- **The inference commons -- pool compute, storage and caches across strangers' nodes** (partial) — `awnix`, `awnode`, `awnet`, `awcache`, `awswarm`, `awpool`, `aitherkvcache`, `awrtifact`, `awtunnel`, `awwall`
- **Retrieval you trained yourself** (partial) — `awembed`, `awdata`, `awgraph`, `awfind`, `awm`, `awdk`
- **Dark Matters Living World** (planned) — `awavatar`, `awdk`, `awsprite`, `awrtifact`, `awrun`
- **The Creator Stack — Saga + Media Forge + Iris on your own machine** (partial) — `awsaga`, `mediaforge`, `awiris`, `awsprite`, `awdesk`, `awbonsai`, `awdk`, `awnode`, `AitherConnect`, `awrtifact`
- **Set and forget -- the clock, the queue, and the record** (partial) — `awrise`, `awrun`, `awrelay`, `awask`, `awdk`
- **The scheduler, open -- route, queue, clock** (partial) — `awrouter`, `awrun`, `awrise`, `awnode`, `awdk`
- **An orchestrator for agent workloads -- stateful, governed, no cluster** (partial) — `awrun`, `awflow`, `awrise`, `awrouter`, `awnode`, `awdk`, `awrepl`, `awnix`, `awiam`, `awbac`, `awdit`, `awseal`, `awshare`
- **A scheduler that learns -- pillars 2, 3 and 6 for wakes** (partial) — `awrise`, `awm`, `awpredict`, `awdecide`, `awembed`, `awevolve`, `awdk`
- **Train what you run -- harvest, train, score, keep-or-revert, on a wake** (partial) — `awrise`, `awdata`, `awlab`, `awevolve`, `awdecide`, `awdk`
- **Mine what you ran -- transcripts in, packs and outcomes out** (partial) — `awmine`, `awtoll`, `awm`, `awdata`, `awdecide`, `awskills`, `awdk`, `awrise`
- **The daily driver** (partial) — `awsh`, `awdk`, `awnode`, `awdesk`, `awskills`

## Named, not yet built

Listed on purpose. A named absence can be chased; a silent one is a thing
nobody remembers.

`awpool` · `awdecide` · `awspaces` · `awcache` · `awdeck` · `awforge` · `awsprite` · `awasp` · `awlab` · `awdata` · `awmod` · `awlog` · `awresume` · `awsaga` · `awiris`

---

<sub>This page is generated from `ecosystem.yaml` and the live manifests. Editing
it by hand will be overwritten — change the registry instead.</sub>
