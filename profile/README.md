# The Aither World

**An operating system for agents.** A Linux you can hand to one, the runtimes it
works in, and the tools it works with.

Every brick below **installs on its own, runs offline, and needs no account.**

![bricks](https://img.shields.io/badge/bricks-37-4c6ef5)
![publishing metrics](https://img.shields.io/badge/publishing%20live%20metrics-34%2F37-4c6ef5)
![planned](https://img.shields.io/badge/named%20%26%20not%20yet%20built-4-8a8a99)

➤ **[Browse the whole ecosystem](https://aitherium.github.io/)** — live, from each repo's own manifest.

---

## What is here

| brick | what it replaces trusting | install | files | tests |
|---|---|---|---|---|
| [awdk](https://aitherium.github.io/awdk/) | Build AI agent fleets — 3 lines, any backend, local or cloud. | `pip install awdk` | 1,215 | 284 |
| [awskills](https://aitherium.github.io/awskills/) | Portable agent skills — self-contained procedures an agent loads on demand. | `git clone https://github.com/Aitherium/awskills` | 154 | 1 |
| [awpack](https://aitherium.github.io/awpack/) | First-party agent packs — the ones we build, versioned and installable on their own. | `git clone https://github.com/Aitherium/awpack` | — | — |
| [awm](https://aitherium.github.io/awm/) | A portable, scoped agent memory. | `pip install awm` | 17 | 0 |
| [awnode](https://aitherium.github.io/awnode/) | A lightweight local gateway — bridges your apps to the AI backends you chose. | `pip install awnode` | 50 | 4 |
| [awrun](https://aitherium.github.io/awrun/) | A priority-aware queue and dispatcher for agentic runs and ad-hoc CI builds. It also judges whether the runner pool is big enough for the queue it is draining, and can ask a host to grow it -- reserving capacity is zero-sum, so a saturated pool needs more of it, not a different share of it. | `pip install awrun` | 21 | 1 |
| [awgraph](https://aitherium.github.io/awgraph/) | A semantic code graph for agents — AST + tree-sitter, call graphs. | `pip install awgraph` | 30 | 4 |
| [awgit](https://aitherium.github.io/awgit/) | Semantic version control on top of git — edit-ops and leases. | `pip install awgit` | 82 | 16 |
| [awtoll](https://aitherium.github.io/awtoll/) | What every tool call costs you in context, measured from your own transcripts. | `pip install git+https://github.com/Aitherium/awtoll.git` | 20 | 1 |
| [awseal](https://aitherium.github.io/awseal/) | Sign an artifact so a stranger can verify it. | `pip install awseal` | 18 | 1 |
| [awshare](https://aitherium.github.io/awshare/) | Publish an artifact and fetch it back verified. | `pip install awshare` | 19 | 2 |
| [awdit](https://aitherium.github.io/awdit/) | An append-only audit trail whose gaps are DETECTABLE. | `pip install git+https://github.com/Aitherium/awdit.git` | 17 | 1 |
| [awbac](https://aitherium.github.io/awbac/) | Role-based access control that fails closed and explains itself. | `pip install git+https://github.com/Aitherium/awbac.git` | 17 | 1 |
| [awiam](https://aitherium.github.io/awiam/) | Who is this caller? A directory and session store that fails honestly. | `pip install git+https://github.com/Aitherium/awiam.git` | 17 | 1 |
| [awtunnel](https://aitherium.github.io/awtunnel/) | Reach a service that has no public address. | `pip install git+https://github.com/Aitherium/awtunnel.git` | 19 | 4 |
| [awnest](https://aitherium.github.io/awnest/) | Prove there is a human before you let them into the nest. | `pip install awnest` | 24 | 2 |
| `awrena` | Put two agents head to head and get a verdict you can check. | — | — | — |
| [awnboard](https://aitherium.github.io/awnboard/) | A front gate you can put in front of anything, and hand someone the key to. | `pip install awnboard` | 19 | 2 |
| [awnix](https://aitherium.github.io/awnix/) | A Linux you can hand to an agent — immutable base, capabilities included. | `see the repo — image builder` | 10 | 0 |
| [awrecover](https://aitherium.github.io/awrecover/) | Labelled snapshots with an all-or-nothing restore. | `pip install git+https://github.com/Aitherium/awrecover.git` | 19 | 3 |
| [awrelay](https://aitherium.github.io/awrelay/) | Portable agent messaging — findings, alerts, coordination. | `pip install awrelay` | 23 | 2 |
| `awask` | Your agent asks you a question — and acts on your answer. | — | — | — |
| [awmail](https://aitherium.github.io/awmail/) | Give an agent an email address — send, and actually receive. | `pip install awmail` | 20 | 2 |
| [awnet](https://aitherium.github.io/awnet/) | The agentic web — agents host a mesh, and agents join one. | `pip install git+https://github.com/Aitherium/awnet.git` | 18 | 2 |
| [awfind](https://aitherium.github.io/awfind/) | A portable search client — query, results, ranking. | `pip install awfind` | 17 | 2 |
| [awbrowse](https://aitherium.github.io/awbrowse/) | A portable browser client — navigate, console, network, DOM, screenshot. | `pip install awbrowse` | 17 | 2 |
| `awvoice` | Hear and speak — transcribe audio, synthesize a voice. | — | — | — |
| `awvision` | See an image — describe it, ask it a question, compare two. | — | — | — |
| `awscreen` | See this machine — what is on screen, and where to click it. | — | — | — |
| `awkit` | Render an agent panel from a tool result — one component, any React app. | — | — | — |
| `awbeads` | A spatial canvas for a page — arrange things, connect them, and keep the arrangement. | — | — | — |
| [awknowledge](https://aitherium.github.io/awknowledge/) | How to run a coding agent so the result survives — the laws, with evidence. | `read it — https://aitherium.github.io/awknowledge/` | 84 | 0 |
| [gobbonet-agentic](https://aitherium.github.io/gobbonet-agentic/) | GobboNet campaigns with a real agent brain — scoped memory, graph recall. | `pip install awdk` | — | — |
| [aitherkvcache](https://aitherium.github.io/aitherkvcache/) | Near-optimal KV cache quantization for LLM inference — sub-byte compression. | `pip install aither-kvcache` | 65 | 8 |
| [AitherZero](https://aitherium.github.io/AitherZero/) | PowerShell 7+ automation framework — numbered, self-describing scripts. | `git clone https://github.com/Aitherium/AitherZero` | 1,552 | 35 |
| [AitherConnect](https://aitherium.github.io/AitherConnect/) | Browser extension — federated AI search, page context, and the Living OS overlay. | `load unpacked — see the repo` | 129 | 17 |
| [awreason](https://aitherium.github.io/awreason/) | A portable reasoning client — sessions, phases, thoughts, and the chain that produced the answer. | `pip install awreason` | 16 | 1 |
| [awrecurse](https://aitherium.github.io/awrecurse/) | Answer a question over a context far larger than the window — recursively, with the trace kept. | `pip install awrecurse` | 18 | 2 |
| [awprism](https://aitherium.github.io/awprism/) | Turn a failure into ranked hypotheses — and say what would confirm each one. | `pip install awprism` | 20 | 2 |
| [awrepl](https://aitherium.github.io/awrepl/) | A REPL an agent can actually use — state that survives between turns. | `pip install awrepl` | 20 | 3 |
| [awresearch](https://aitherium.github.io/awresearch/) | Ask a research question, get a cited report you can check. | `pip install git+https://github.com/Aitherium/awresearch.git` | 25 | 3 |
| [awpredict](https://aitherium.github.io/awpredict/) | Predict what your environment does next, and how surprised you were. | `pip install git+https://github.com/Aitherium/awpredict.git` | 28 | 4 |
| `awevolve` | Point an agent at a file and a command that scores it, and let it improve. | — | — | — |
| [awsh](https://aitherium.github.io/awsh/) | Your terminal answers you -- type a question where a command would go. | `npm i -g @aitherium/awsh` | — | — |
| `awrise` | Wake an agent on a schedule, let it do one thing, and put it back to sleep. | — | — | — |
| [awkno](https://aitherium.github.io/awkno/) | The man page for the Aither World — every brick, stack and law, offline. | `pip install awkno` | 115 | 1 |
| `awwall` | Say what a workload may reach, and watch everything else fail closed. | — | — | — |

*Files and tests are quoted from each repository's own published manifest, not
counted here. A dash means that repo publishes no manifest yet — never zero,
because a fabricated zero reads as a measurement.*

## Stacks — what to use together

- **The bare agent VM** (partial) — `awnix`, `awdk`, `awskills`, `awkno`
- **Senses** (ready) — `awfind`, `awbrowse`, `awvoice`, `awvision`, `awscreen`, `awdk`
- **Avatar ensemble** (planned) — `awdk`, `awsh`, `awvoice`, `awvision`, `awsprite`
- **Provenance** (partial) — `awseal`, `awshare`, `awdit`, `awbac`
- **Many agents, one repo** (ready) — `awgit`, `awgraph`, `awrelay`, `awm`
- **The front door** (partial) — `awnboard`, `awnest`, `awiam`, `awbac`, `awdit`
- **Identity, authority, and the record** (partial) — `awiam`, `awbac`, `awdit`
- **One surface — agent panels, not hand-built UIs** (planned) — `awkit`, `awdk`, `awnode`, `awiam`, `awbac`
- **The reasoning loop** (partial) — `awreason`, `awprism`, `awrepl`, `awrecurse`
- **Research you can check** (partial) — `awresearch`, `awfind`, `awbrowse`, `awm`
- **A pool across your own devices** (partial) — `awnet`, `awnode`, `awdk`
- **Grow a companion in the browser, then take it home** (planned) — `awsprite`, `awbonsai`, `awdk`, `awsh`, `awnode`

## Named, not yet built

Listed on purpose. A named absence can be chased; a silent one is a thing
nobody remembers.

`awpool` · `awswarm` · `awsprite` · `awbonsai`

---

<sub>This page is generated from `ecosystem.yaml` and the live manifests. Editing
it by hand will be overwritten — change the registry instead.</sub>
