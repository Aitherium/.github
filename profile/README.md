# The Aither World

**An operating system for agents.** A Linux you can hand to one, the runtimes it
works in, and the tools it works with.

Every brick below **installs on its own, runs offline, and needs no account.**

![bricks](https://img.shields.io/badge/bricks-55-4c6ef5)
![publishing metrics](https://img.shields.io/badge/publishing%20live%20metrics-55%2F55-4c6ef5)
![planned](https://img.shields.io/badge/named%20%26%20not%20yet%20built-13-8a8a99)

➤ **[Browse the whole ecosystem](https://aitherium.github.io/)** — live, from each repo's own manifest.

---

## What is here

| brick | what it replaces trusting | install | files | tests |
|---|---|---|---|---|
| [awdk](https://aitherium.github.io/awdk/) | Build AI agent fleets — 3 lines, any backend, local or cloud. | `pip install awdk` | 2,122 | 592 |
| [awskills](https://aitherium.github.io/awskills/) | Portable agent skills — self-contained procedures an agent loads on demand. | `git clone https://github.com/Aitherium/awskills` | 188 | 1 |
| [awpack](https://aitherium.github.io/awpack/) | First-party agent packs — the ones we build, versioned and installable on their own. | `git clone https://github.com/Aitherium/awpack` | 28 | 0 |
| [awm](https://aitherium.github.io/awm/) | A portable, scoped agent memory. | `pip install awm` | 61 | 23 |
| `aitheros` | One file you run, and the machine has a local AI stack. | — | — | — |
| `awdaemons` | The AitherOS daemons as one file — no Python, no signing, no install. | — | — | — |
| [awdesk](https://aitherium.github.io/awdesk/) | Aither World Desk -- the desktop body of AitherOS Online: tray, avatars, decision cards, the Living Desktop as an overlay. | `see the repo -- Electron app (npm install && npx electron .)` | 506 | 1 |
| [awnode](https://aitherium.github.io/awnode/) | A lightweight local gateway — bridges your apps to the AI backends you chose. | `pip install awnode` | 72 | 10 |
| [awrun](https://aitherium.github.io/awrun/) | A priority-aware queue and dispatcher for agentic runs and ad-hoc CI builds. It also judges whether the runner pool is big enough for the queue it is draining, and can ask a host to grow it -- reserving capacity is zero-sum, so a saturated pool needs more of it, not a different share of it. | `pip install awrun` | 43 | 9 |
| `awpool` | The free half of the elastic work pool: dispatches public-safe work onto the free GitHub-hosted runners of the public aw* mirrors, so their idle CI minutes become compute. awrun remains the paid/self-hosted lane; this is its free twin. | — | — | — |
| [awgraph](https://aitherium.github.io/awgraph/) | A semantic code graph for agents — AST + tree-sitter, call graphs. | `pip install awgraph` | 55 | 20 |
| [awgit](https://aitherium.github.io/awgit/) | Semantic version control on top of git — edit-ops and leases. | `pip install awgit` | 95 | 19 |
| [awdelphi](https://aitherium.github.io/awdelphi/) | Anonymous multi-round expert panels — a converged answer with a trace. | `pip install awdelphi` | 35 | 7 |
| `awclassify` | Classify any document -- what it is, who may read it, who it is for, what it is about. | — | — | — |
| `awdecide` | One typed-decision contract -- choice / score / bool with a probability -- over a ladder of backends you already run (rules, tiny local models, an LLM's logprobs), fail-closed, with a Brier ledger that resolves every decision against its outcome. | — | — | — |
| [awtoll](https://aitherium.github.io/awtoll/) | What every tool call costs you in context, measured from your own transcripts. | `pip install awtoll` | 29 | 1 |
| [awseal](https://aitherium.github.io/awseal/) | Sign an artifact so a stranger can verify it. | `pip install awseal` | 26 | 1 |
| [awshare](https://aitherium.github.io/awshare/) | Publish an artifact and fetch it back verified. | `pip install awshare` | 28 | 3 |
| [awdit](https://aitherium.github.io/awdit/) | An append-only audit trail whose gaps are DETECTABLE. | `pip install awdit` | 24 | 1 |
| [awbac](https://aitherium.github.io/awbac/) | Role-based access control that fails closed and explains itself. | `pip install awbac` | 23 | 1 |
| [awiam](https://aitherium.github.io/awiam/) | Who is this caller? A directory and session store that fails honestly. | `pip install awiam` | 24 | 1 |
| [awtunnel](https://aitherium.github.io/awtunnel/) | Reach a service that has no public address. | `pip install awtunnel` | 32 | 7 |
| [awnest](https://aitherium.github.io/awnest/) | Prove there is a human before you let them into the nest. | `pip install awnest` | 33 | 4 |
| [awrena](https://aitherium.github.io/awrena/) | Put two agents head to head and get a verdict you can check. | `pip install awrena` | 19 | 1 |
| [awnboard](https://aitherium.github.io/awnboard/) | A front gate you can put in front of anything, and hand someone the key to. | `pip install awnboard` | 25 | 2 |
| [awnix](https://aitherium.github.io/awnix/) | A Linux you can hand to an agent — immutable base, capabilities included. | `podman build -t awnix:latest -f Containerfile .` | 19 | 0 |
| [awrecover](https://aitherium.github.io/awrecover/) | Labelled snapshots with an all-or-nothing restore. | `pip install awrecover` | 26 | 4 |
| [awstorage](https://aitherium.github.io/awstorage/) | Every drive on every node, indexed, classified and diffed -- so you can see what you own before you delete it. | `pip install awstorage` | 66 | 20 |
| [awrelay](https://aitherium.github.io/awrelay/) | Portable agent messaging — findings, alerts, coordination. | `pip install awrelay` | 45 | 12 |
| [awask](https://aitherium.github.io/awask/) | Your agent asks you a question — and acts on your answer. | `pip install awask` | 55 | 8 |
| [awmail](https://aitherium.github.io/awmail/) | Give an agent an email address — send, and actually receive. | `pip install awmail` | 26 | 2 |
| `mediaforge` | The creative studio — search the boards, render scenes, keep the character. | — | — | — |
| [awnet](https://aitherium.github.io/awnet/) | The agentic web — agents host a mesh, and agents join one. | `pip install awnet` | 24 | 2 |
| `awswarm` | Run one model too big for any single GPU across a pool of small ones. | — | — | — |
| [awfind](https://aitherium.github.io/awfind/) | A portable search client — query, results, ranking. | `pip install awfind` | 33 | 6 |
| [awbrowse](https://aitherium.github.io/awbrowse/) | A portable browser client — navigate, console, network, DOM, screenshot. | `pip install awbrowse` | 28 | 4 |
| `awprove` | Drive a page as the real user, check what rendered, and get a test that goes red if it stops being true. | — | — | — |
| [awvoice](https://aitherium.github.io/awvoice/) | Hear and speak — transcribe audio, synthesize a voice. | `pip install awvoice` | 34 | 6 |
| [awvision](https://aitherium.github.io/awvision/) | See an image — describe it, ask it a question, compare two. | `pip install awvision` | 25 | 3 |
| [awscreen](https://aitherium.github.io/awscreen/) | See this machine — what is on screen, and where to click it. | `pip install awscreen` | 27 | 4 |
| `awkit` | Render an agent panel from a tool result — one component, any React app. | — | — | — |
| `awbeads` | A spatial canvas for a page — arrange things, connect them, and keep the arrangement. | — | — | — |
| `awsprite` | Hatch a companion that grows only from what you teach it, then take it home. | — | — | — |
| `awbonsai` | Run a real model in the visitor's own browser — no server round trip, no upload. | — | — | — |
| [awknowledge](https://aitherium.github.io/awknowledge/) | How to run a coding agent so the result survives — the laws, with evidence. | `read it — https://aitherium.github.io/awknowledge/` | 134 | 0 |
| `awbrain` | Your history as a wiki of linked markdown — claims pinned to the evidence. | — | — | — |
| [gawbbonet](https://aitherium.github.io/gawbbonet/) | GobboNet campaigns with a real agent brain — scoped memory, graph recall. | `pip install gawbbonet` | 17 | 1 |
| [aitherkvcache](https://aitherium.github.io/aitherkvcache/) | Near-optimal KV cache quantization for LLM inference — sub-byte compression. | `pip install aither-kvcache` | 70 | 8 |
| [awrtifact](https://aitherium.github.io/awrtifact/) | Deliberately chunk artifacts into GitHub release assets — the productized aitherkvcache mirror lane. | `pip install awrtifact` | 62 | 17 |
| [AitherZero](https://aitherium.github.io/AitherZero/) | PowerShell 7+ automation framework — numbered, self-describing scripts. | `git clone https://github.com/Aitherium/AitherZero` | 1,681 | 44 |
| [AitherConnect](https://aitherium.github.io/AitherConnect/) | Browser extension — federated AI search, page context, and the Living OS overlay. | `load unpacked — see the repo` | 167 | 33 |
| [awreason](https://aitherium.github.io/awreason/) | A portable reasoning client — sessions, phases, thoughts, and the chain that produced the answer. | `pip install awreason` | 22 | 1 |
| [awrecurse](https://aitherium.github.io/awrecurse/) | Answer a question over a context far larger than the window — recursively, with the trace kept. | `pip install awrecurse` | 27 | 4 |
| [awprism](https://aitherium.github.io/awprism/) | Turn a failure into ranked hypotheses — and say what would confirm each one. | `pip install awprism` | 32 | 5 |
| [awrepl](https://aitherium.github.io/awrepl/) | A REPL an agent can actually use — state that survives between turns. | `pip install awrepl` | 28 | 4 |
| `awreport` | File a bug report that has already scrubbed your secrets and collapsed the duplicate. | — | — | — |
| [awresearch](https://aitherium.github.io/awresearch/) | Ask a research question, get a cited report you can check. | `pip install awresearch` | 32 | 4 |
| [awfocus](https://aitherium.github.io/awfocus/) | See, search and steer every Claude session from one command. | `pip install awfocus` | 31 | 2 |
| [awgym](https://aitherium.github.io/awgym/) | An ARC training gym — a game a world model can watch, and six roles that play through it. | `pip install awgym` | 69 | 13 |
| [awpredict](https://aitherium.github.io/awpredict/) | Predict what your environment does next, and how surprised you were. | `pip install git+https://github.com/Aitherium/awpredict.git` | 46 | 10 |
| `awevolve` | Point an agent at a file and a command that scores it, and let it improve. | — | — | — |
| [awsh](https://aitherium.github.io/awsh/) | Your terminal answers you -- type a question where a command would go. | `npm i -g @aitherium/awsh` | 1,220 | 87 |
| `awmine` | Mine what your agents did -- outcomes, lessons and procedures out of the transcripts they left behind. | — | — | — |
| [awrise](https://aitherium.github.io/awrise/) | Wake an agent on a schedule, let it do one thing, and put it back to sleep. | `pip install awrise` | 63 | 32 |
| [awkno](https://aitherium.github.io/awkno/) | The man page for the Aither World — every brick, stack and law, offline. | `pip install awkno` | 182 | 1 |
| [awwall](https://aitherium.github.io/awwall/) | Say what a workload may reach, and watch everything else fail closed. | `pip install awwall` | 19 | 2 |
| `awrouter` | OpenRouter for your own fleet: pick a model backend by cost/latency/ capability, fail over, fit the context window, stream. Standalone, OpenAI-compatible, no Aither-specifics required to be valuable. | — | — | — |
| [awembed](https://aitherium.github.io/awembed/) | Train an embedding model that knows your corpus, and prove it beats the big one. | `pip install awembed` | 30 | 2 |
| [awtax](https://aitherium.github.io/awtax/) | Turn any tax PDF -- returns, W-2, 1099, statements, even scans -- into structured data you can check. | `pip install awtax` | 24 | 1 |
| [awflow](https://aitherium.github.io/awflow/) | A deterministic workflow runtime — chain agent calls with journal replay and budget control. | `pip install aitherium-awflow` | 29 | 5 |
| [awsettings](https://aitherium.github.io/awsettings/) | Your agent's permissions and config, following you to the next machine. | `pip install awsettings` | 44 | 12 |
| [awavatar](https://aitherium.github.io/awavatar/) | One character spec in, a rigged, animated, multi-style avatar pack out. | `pip install awavatar` | 24 | 2 |

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

## Named, not yet built

Listed on purpose. A named absence can be chased; a silent one is a thing
nobody remembers.

`awscope` · `awspaces` · `awcache` · `awdeck` · `awforge` · `awasp` · `awlab` · `awdata` · `awmod` · `awlog` · `awresume` · `awsaga` · `awiris`

## Built on

The open-source projects under the bricks. Each one is something we actually
run: the registry has to name a file in our repo that proves it before it is
listed here.

[![Blender + Rigify](https://img.shields.io/badge/built%20on-Blender%20%2B%20Rigify-5EC9CC)](https://www.blender.org/) [![CentOS Stream](https://img.shields.io/badge/built%20on-CentOS%20Stream-5EC9CC)](https://www.centos.org/centos-stream/) [![ComfyUI](https://img.shields.io/badge/built%20on-ComfyUI-5EC9CC)](https://github.com/comfyanonymous/ComfyUI) [![Docker](https://img.shields.io/badge/built%20on-Docker-5EC9CC)](https://github.com/moby/moby) [![FFmpeg](https://img.shields.io/badge/built%20on-FFmpeg-5EC9CC)](https://ffmpeg.org/) [![headroom](https://img.shields.io/badge/built%20on-headroom-5EC9CC)](https://github.com/headroomlabs-ai/headroom) [![LanceDB](https://img.shields.io/badge/built%20on-LanceDB-5EC9CC)](https://github.com/lancedb/lancedb) [![llama.cpp](https://img.shields.io/badge/built%20on-llama.cpp-5EC9CC)](https://github.com/ggml-org/llama.cpp) [![Podman](https://img.shields.io/badge/built%20on-Podman-5EC9CC)](https://github.com/containers/podman) [![SANA](https://img.shields.io/badge/built%20on-SANA-5EC9CC)](https://github.com/NVlabs/Sana) [![vLLM](https://img.shields.io/badge/built%20on-vLLM-5EC9CC)](https://github.com/vllm-project/vllm) [![WireGuard](https://img.shields.io/badge/built%20on-WireGuard-5EC9CC)](https://www.wireguard.com/)

| project | what we run it for | license |
|---|---|---|
| [Blender + Rigify](https://www.blender.org/) | Headless auto-rigging service for generated characters. | `GPL-2.0-or-later` |
| [CentOS Stream](https://www.centos.org/centos-stream/) | Base image of awnix — bootable, immutable, built with bootc. | see upstream |
| [ComfyUI](https://github.com/comfyanonymous/ComfyUI) | Visual generation engine behind media-forge — images, video, and the 3D stack (Hunyuan3D). | `GPL-3.0` |
| [Docker](https://github.com/moby/moby) | Compose stacks and image builds for the fleet. | `Apache-2.0` |
| [FFmpeg](https://ffmpeg.org/) | Every media transform — frames, mux, HLS transcode. | `LGPL-2.1+ (GPL in some builds)` |
| [headroom](https://github.com/headroomlabs-ai/headroom) | Reversible context compression — a sidecar plus agent-callable tools. | `Apache-2.0` |
| [LanceDB](https://github.com/lancedb/lancedb) | Vector store behind AitherNexus. | `Apache-2.0` |
| [llama.cpp](https://github.com/ggml-org/llama.cpp) | Local inference engine — llama-server lanes and the Bonsai models (our PrismML fork). | `MIT` |
| [Podman](https://github.com/containers/podman) | Rootless container runtime; systemd quadlet units for the desktop and appliances. | `Apache-2.0` |
| [SANA](https://github.com/NVlabs/Sana) | Fast image-generation backend, profile-gated. | see upstream |
| [vLLM](https://github.com/vllm-project/vllm) | GPU inference lanes, extended by our vLLM mesh plugin. | `Apache-2.0` |
| [WireGuard](https://www.wireguard.com/) | The private overlay network under AitherNet / AitherMesh. | `GPL-2.0` |

---

<sub>This page is generated from `ecosystem.yaml` and the live manifests. Editing
it by hand will be overwritten — change the registry instead.</sub>
