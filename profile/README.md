# The Aither World

**An operating system for agents** — a Linux you can hand to one, the runtimes it
works in, and the tools it works with.

`aw` is **Aither World**. Every name reads as a phrase: `awknowledge` is *Aither
World Knowledge*, `awnix` is *Aither World Nix*, `awnet` is *Aither World Net*.

Every brick **installs on its own, runs offline, and needs no account.** That is the
whole rule: if a brick's one-line pitch cannot be written without naming a sibling,
it is not a brick — it is a subsystem of something else, and shipping it separately
would teach you to adopt a dependency you never wanted.

![bricks](https://img.shields.io/badge/bricks-46-4c6ef5)
![publishing metrics](https://img.shields.io/badge/publishing%20live%20metrics-43%2F46-4c6ef5)
![planned](https://img.shields.io/badge/named%20%26%20not%20yet%20built-8-8a8a99)

➤ **[Browse the whole ecosystem](https://aitherium.github.io/)** — live, from each repo's own manifest.

---

## Start here

Four bricks carry the story. Take one; the rest still work without it.

| brick | what it is | install | one line |
|---|---|---|---|
| [awnix](https://aitherium.github.io/awnix/) | **the machine** — immutable base | `see the repo — image builder` | A Linux you can hand to an agent — immutable base, capabilities included. |
| [awdk](https://aitherium.github.io/awdk/) | **the runtime** — agent fleets | `pip install awdk` | Build AI agent fleets — 3 lines, any backend, local or cloud. |
| [awknowledge](https://aitherium.github.io/awknowledge/) | **the doctrine** — how to run one | `read it — https://aitherium.github.io/awknowledge/` | How to run a coding agent so the result survives — the laws, with evidence. |
| [awsh](https://aitherium.github.io/awsh/) | **the cockpit** — your terminal | `npm i -g @aitherium/awsh` | Your terminal answers you -- type a question where a command would go. |

The layering is deliberate, and it is the one design decision worth reading twice:

```
  awnix      immutable OS + the aw* capabilities     <- guarantees live HERE
    + awdk   three lines in a Dockerfile             <- the bare agent VM
      + you  skills, packs, credentials
```

Capabilities go in the **base**, not the agent — leases, call graph, messaging,
scoped memory, snapshots, verified artifacts. Put them in the agent instead and
every guarantee walks out the door with it when you swap the agent.

---

## Where this came from

**AitherOS** is the platform these were cut out of: a live agentic fleet — services,
agents, a memory graph, an inference plane — run in production every day. It is not
a demo, and it is not what you install. The bricks are: each one is the piece that
survived being made standalone, published under its own licence, with its own tests.

A brick is not shipped when it builds. It is shipped when a stranger can adopt it
alone, offline, and check what it claims.

---

## Every brick

| brick | what it does | install | files | tests |
|---|---|---|---|---|
| [awdk](https://aitherium.github.io/awdk/) | Build AI agent fleets — 3 lines, any backend, local or cloud. | `pip install awdk` | 1,269 | 290 |
| [awskills](https://aitherium.github.io/awskills/) | Portable agent skills — self-contained procedures an agent loads on demand. | `git clone https://github.com/Aitherium/awskills` | 155 | 1 |
| [awpack](https://aitherium.github.io/awpack/) | First-party agent packs — the ones we build, versioned and installable on their own. | `git clone https://github.com/Aitherium/awpack` | 15 | 0 |
| [awm](https://aitherium.github.io/awm/) | A portable, scoped agent memory. | `pip install awm` | 17 | 0 |
| [awnode](https://aitherium.github.io/awnode/) | A lightweight local gateway — bridges your apps to the AI backends you chose. | `pip install awnode` | 50 | 4 |
| [awrun](https://aitherium.github.io/awrun/) | A priority-aware queue and dispatcher for agentic runs and ad-hoc CI builds. It also judges whether the runner pool is big enough for the queue it is draining, and can ask a host to grow it -- reserving capacity is zero-sum, so a saturated pool needs more of it, not a different share of it. | `pip install awrun` | 22 | 1 |
| [awgraph](https://aitherium.github.io/awgraph/) | A semantic code graph for agents — AST + tree-sitter, call graphs. | `pip install awgraph` | 32 | 6 |
| [awgit](https://aitherium.github.io/awgit/) | Semantic version control on top of git — edit-ops and leases. | `pip install awgit` | 82 | 16 |
| [awdelphi](https://aitherium.github.io/awdelphi/) | Anonymous multi-round expert panels — a converged answer with a trace. | `pip install git+https://github.com/Aitherium/awdelphi.git` | 24 | 6 |
| [awtoll](https://aitherium.github.io/awtoll/) | What every tool call costs you in context, measured from your own transcripts. | `pip install git+https://github.com/Aitherium/awtoll.git` | 21 | 1 |
| [awseal](https://aitherium.github.io/awseal/) | Sign an artifact so a stranger can verify it. | `pip install awseal` | 18 | 1 |
| [awshare](https://aitherium.github.io/awshare/) | Publish an artifact and fetch it back verified. | `pip install awshare` | 19 | 2 |
| [awdit](https://aitherium.github.io/awdit/) | An append-only audit trail whose gaps are DETECTABLE. | `pip install git+https://github.com/Aitherium/awdit.git` | 17 | 1 |
| [awbac](https://aitherium.github.io/awbac/) | Role-based access control that fails closed and explains itself. | `pip install git+https://github.com/Aitherium/awbac.git` | 17 | 1 |
| [awiam](https://aitherium.github.io/awiam/) | Who is this caller? A directory and session store that fails honestly. | `pip install git+https://github.com/Aitherium/awiam.git` | 17 | 1 |
| [awtunnel](https://aitherium.github.io/awtunnel/) | Reach a service that has no public address. | `pip install git+https://github.com/Aitherium/awtunnel.git` | 19 | 4 |
| [awnest](https://aitherium.github.io/awnest/) | Prove there is a human before you let them into the nest. | `pip install awnest` | 24 | 2 |
| [awrena](https://aitherium.github.io/awrena/) | Put two agents head to head and get a verdict you can check. | `pip install awrena` | — | — |
| [awnboard](https://aitherium.github.io/awnboard/) | A front gate you can put in front of anything, and hand someone the key to. | `pip install awnboard` | 19 | 2 |
| [awnix](https://aitherium.github.io/awnix/) | A Linux you can hand to an agent — immutable base, capabilities included. | `see the repo — image builder` | 10 | 0 |
| [awrecover](https://aitherium.github.io/awrecover/) | Labelled snapshots with an all-or-nothing restore. | `pip install git+https://github.com/Aitherium/awrecover.git` | 19 | 3 |
| `awstorage` | Every drive on every node, indexed, classified and diffed -- so you can see what you own before you delete it. | — | — | — |
| [awrelay](https://aitherium.github.io/awrelay/) | Portable agent messaging — findings, alerts, coordination. | `pip install awrelay` | 25 | 3 |
| [awask](https://aitherium.github.io/awask/) | Your agent asks you a question — and acts on your answer. | `pip install awask` | — | — |
| [awmail](https://aitherium.github.io/awmail/) | Give an agent an email address — send, and actually receive. | `pip install awmail` | 20 | 2 |
| [awnet](https://aitherium.github.io/awnet/) | The agentic web — agents host a mesh, and agents join one. | `pip install git+https://github.com/Aitherium/awnet.git` | 18 | 2 |
| `awswarm` | Run one model too big for any single GPU across a pool of small ones. | — | — | — |
| [awfind](https://aitherium.github.io/awfind/) | A portable search client — query, results, ranking. | `pip install awfind` | 17 | 2 |
| [awbrowse](https://aitherium.github.io/awbrowse/) | A portable browser client — navigate, console, network, DOM, screenshot. | `pip install awbrowse` | 17 | 2 |
| `awvoice` | Hear and speak — transcribe audio, synthesize a voice. | — | — | — |
| `awvision` | See an image — describe it, ask it a question, compare two. | — | — | — |
| `awscreen` | See this machine — what is on screen, and where to click it. | — | — | — |
| `awkit` | Render an agent panel from a tool result — one component, any React app. | — | — | — |
| `awbeads` | A spatial canvas for a page — arrange things, connect them, and keep the arrangement. | — | — | — |
| `awclassify` | Classify any document -- what it is, who may read it, who it is for, what it is about. | — | — | — |
| [awknowledge](https://aitherium.github.io/awknowledge/) | How to run a coding agent so the result survives — the laws, with evidence. | `read it — https://aitherium.github.io/awknowledge/` | 85 | 0 |
| `awbrain` | Your history as a wiki of linked markdown — claims pinned to the evidence. | — | — | — |
| `gobbonet-agentic` | GobboNet campaigns with a real agent brain — scoped memory, graph recall. | — | — | — |
| [aitherkvcache](https://aitherium.github.io/aitherkvcache/) | Near-optimal KV cache quantization for LLM inference — sub-byte compression. | `pip install aither-kvcache` | 66 | 8 |
| [awrtifact](https://aitherium.github.io/awrtifact/) | Deliberately chunk artifacts into GitHub release assets — the productized aitherkvcache mirror lane. | `pip install awrtifact` | 31 | 6 |
| [AitherZero](https://aitherium.github.io/AitherZero/) | PowerShell 7+ automation framework — numbered, self-describing scripts. | `git clone https://github.com/Aitherium/AitherZero` | 1,569 | 35 |
| [AitherConnect](https://aitherium.github.io/AitherConnect/) | Browser extension — federated AI search, page context, and the Living OS overlay. | `load unpacked — see the repo` | 129 | 17 |
| [awreason](https://aitherium.github.io/awreason/) | A portable reasoning client — sessions, phases, thoughts, and the chain that produced the answer. | `pip install awreason` | 16 | 1 |
| [awrecurse](https://aitherium.github.io/awrecurse/) | Answer a question over a context far larger than the window — recursively, with the trace kept. | `pip install awrecurse` | 18 | 2 |
| [awprism](https://aitherium.github.io/awprism/) | Turn a failure into ranked hypotheses — and say what would confirm each one. | `pip install awprism` | 20 | 2 |
| [awrepl](https://aitherium.github.io/awrepl/) | A REPL an agent can actually use — state that survives between turns. | `pip install awrepl` | 20 | 3 |
| [awresearch](https://aitherium.github.io/awresearch/) | Ask a research question, get a cited report you can check. | `pip install git+https://github.com/Aitherium/awresearch.git` | 25 | 3 |
| [awfocus](https://aitherium.github.io/awfocus/) | See, search and steer every Claude session from one command. | `pip install awfocus` | 21 | 1 |
| [awgym](https://aitherium.github.io/awgym/) | An ARC training gym — a game a world model can watch, and six roles that play through it. | `pip install awgym` | 46 | 4 |
| [awpredict](https://aitherium.github.io/awpredict/) | Predict what your environment does next, and how surprised you were. | `pip install git+https://github.com/Aitherium/awpredict.git` | 38 | 8 |
| `awevolve` | Point an agent at a file and a command that scores it, and let it improve. | — | — | — |
| [awsh](https://aitherium.github.io/awsh/) | Your terminal answers you -- type a question where a command would go. | `npm i -g @aitherium/awsh` | 1,144 | 47 |
| [awrise](https://aitherium.github.io/awrise/) | Wake an agent on a schedule, let it do one thing, and put it back to sleep. | `pip install awrise` | — | — |
| [awkno](https://aitherium.github.io/awkno/) | The man page for the Aither World — every brick, stack and law, offline. | `pip install awkno` | 130 | 1 |
| [awwall](https://aitherium.github.io/awwall/) | Say what a workload may reach, and watch everything else fail closed. | `pip install awwall` | — | — |
| `awrouter` | OpenRouter for your own fleet: pick a model backend by cost/latency/ capability, fail over, fit the context window, stream. Standalone, OpenAI-compatible, no Aither-specifics required to be valuable. | — | — | — |
| [awembed](https://aitherium.github.io/awembed/) | Train an embedding model that knows your corpus, and prove it beats the big one. | `pip install awembed` | — | — |
| [awtax](https://aitherium.github.io/awtax/) | Turn any tax PDF -- returns, W-2, 1099, statements, even scans -- into structured data you can check. | `git clone https://github.com/Aitherium/awtax` | — | — |
| `awprove` | Drive a page as the real user, check what actually rendered, and get a test that goes red if it ever stops being true. | — | — | — |

*Files and tests are quoted from each repository's own published manifest, not
counted here. A dash means that repo publishes no manifest yet — never zero,
because a fabricated zero reads as a measurement.*

## Stacks — what to use together

A stack is an assembly, not a bundle. `ready` means the pieces exist **and** the
assembly is documented; `partial` means the pieces ship and wiring them is still
yours to do. Saying which is which is the point — a stack that ships every part
and no story is how a working thing reaches nobody.

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
- **The inference commons -- pool compute, storage and caches across strangers' nodes** (partial) — `awnix`, `awnode`, `awnet`, `awcache`, `awswarm`, `awpool`, `aitherkvcache`, `awrtifact`, `awtunnel`, `awwall`
- **Retrieval you trained yourself** (partial) — `awembed`, `awdata`, `awgraph`, `awfind`, `awm`, `awdk`

## Named, not yet built

Listed on purpose. A named absence can be chased; a silent one is a thing
nobody remembers.

`awpool` · `awspaces` · `awcache` · `awsprite` · `awbonsai` · `awmod` · `awlog` · `awdata`

---

## Two houses

| | |
|---|---|
| **[aitherium.com](https://aitherium.com)** | The platform. AitherOS, the Living Desktop, the hosted planes. |
| **[aitherium.org](https://aitherium.org)** | The Aitherium Foundation. Mission, programs, transparency, how to get involved. |
| **[aitherium.github.io](https://aitherium.github.io/)** | The ecosystem hub — every brick, live from its own manifest. |

---

<sub>This page is generated from `ecosystem.yaml` and the live manifests, and is
published to BOTH the public and the member-only org profile. Editing either by
hand will be overwritten — change the registry instead.</sub>
