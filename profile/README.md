# The Aither World

**An operating system for agents.** A Linux you can hand to one, the runtimes it
works in, and the tools it works with.

Every brick below **installs on its own, runs offline, and needs no account.**

![bricks](https://img.shields.io/badge/bricks-33-4c6ef5)
![publishing metrics](https://img.shields.io/badge/publishing%20live%20metrics-33%2F33-4c6ef5)
![planned](https://img.shields.io/badge/named%20%26%20not%20yet%20built-2-8a8a99)

➤ **[Browse the whole ecosystem](https://aitherium.github.io/)** — live, from each repo's own manifest.

---

## What is here

| brick | what it replaces trusting | install | files | tests |
|---|---|---|---|---|
| [awdk](https://aitherium.github.io/awdk/) | Build AI agent fleets — 3 lines, any backend, local or cloud. | `pip install awdk` | 1,184 | 272 |
| [awskills](https://aitherium.github.io/awskills/) | Portable agent skills — self-contained procedures an agent loads on demand. | `git clone https://github.com/Aitherium/awskills` | 152 | 1 |
| [awm](https://aitherium.github.io/awm/) | A portable, scoped agent memory. | `pip install awm` | 11 | 0 |
| [awnode](https://aitherium.github.io/awnode/) | A lightweight local gateway — bridges your apps to the AI backends you chose. | `pip install awnode` | 47 | 4 |
| [awrun](https://aitherium.github.io/awrun/) | A priority-aware queue and dispatcher for agentic runs and ad-hoc CI builds. | `pip install awrun` | 17 | 1 |
| [awgraph](https://aitherium.github.io/awgraph/) | A semantic code graph for agents — AST + tree-sitter, call graphs. | `pip install awgraph` | 28 | 4 |
| [awgit](https://aitherium.github.io/awgit/) | Semantic version control on top of git — edit-ops and leases. | `pip install awgit` | 79 | 15 |
| [awseal](https://aitherium.github.io/awseal/) | Sign an artifact so a stranger can verify it. | `pip install awseal` | 15 | 1 |
| [awshare](https://aitherium.github.io/awshare/) | Publish an artifact and fetch it back verified. | `pip install awshare` | 13 | 2 |
| [awdit](https://aitherium.github.io/awdit/) | An append-only audit trail whose gaps are DETECTABLE. | `pip install awdit` | 11 | 1 |
| [awbac](https://aitherium.github.io/awbac/) | Role-based access control that fails closed and explains itself. | `pip install awbac` | 11 | 1 |
| [awiam](https://aitherium.github.io/awiam/) | Who is this caller? A directory and session store that fails honestly. | `pip install awiam` | 11 | 1 |
| [awtunnel](https://aitherium.github.io/awtunnel/) | Reach a service that has no public address. | `pip install awtunnel` | 16 | 4 |
| [awnest](https://aitherium.github.io/awnest/) | Prove there is a human before you let them into the nest. | `pip install awnest` | 22 | 2 |
| [awnboard](https://aitherium.github.io/awnboard/) | A front gate you can put in front of anything, and hand someone the key to. | `pip install awnboard` | 17 | 2 |
| [awnix](https://aitherium.github.io/awnix/) | A Linux you can hand to an agent — immutable base, capabilities included. | `see the repo — image builder` | 7 | 0 |
| [awrecover](https://aitherium.github.io/awrecover/) | Labelled snapshots with an all-or-nothing restore. | `pip install awrecover` | 12 | 0 |
| [awrelay](https://aitherium.github.io/awrelay/) | Portable agent messaging — findings, alerts, coordination. | `pip install awrelay` | 20 | 2 |
| [awmail](https://aitherium.github.io/awmail/) | Give an agent an email address — send, and actually receive. | `pip install awmail` | 18 | 2 |
| [awnet](https://aitherium.github.io/awnet/) | The agentic web — agents host a mesh, and agents join one. | `pip install awnet` | 15 | 2 |
| [awfind](https://aitherium.github.io/awfind/) | A portable search client — query, results, ranking. | `pip install awfind` | 15 | 2 |
| [awbrowse](https://aitherium.github.io/awbrowse/) | A portable browser client — navigate, console, network, DOM, screenshot. | `pip install awbrowse` | 15 | 2 |
| [awknowledge](https://aitherium.github.io/awknowledge/) | How to run a coding agent so the result survives — the laws, with evidence. | `read it — https://aitherium.github.io/awskills/codex.html` | 31 | 0 |
| [aitherkvcache](https://aitherium.github.io/aitherkvcache/) | Near-optimal KV cache quantization for LLM inference — sub-byte compression. | `pip install aither-kvcache` | 65 | 8 |
| [AitherZero](https://aitherium.github.io/AitherZero/) | PowerShell 7+ automation framework — numbered, self-describing scripts. | `git clone https://github.com/Aitherium/AitherZero` | 1,550 | 35 |
| [AitherConnect](https://aitherium.github.io/AitherConnect/) | Browser extension — federated AI search, page context, and the Living OS overlay. | `load unpacked — see the repo` | 127 | 17 |
| [awreason](https://aitherium.github.io/awreason/) | A portable reasoning client — sessions, phases, thoughts, and the chain that produced the answer. | `pip install awreason` | 13 | 1 |
| [awrecurse](https://aitherium.github.io/awrecurse/) | Answer a question over a context far larger than the window — recursively, with the trace kept. | `pip install awrecurse` | 15 | 2 |
| [awprism](https://aitherium.github.io/awprism/) | Turn a failure into ranked hypotheses — and say what would confirm each one. | `pip install awprism` | 17 | 2 |
| [awrepl](https://aitherium.github.io/awrepl/) | A REPL an agent can actually use — state that survives between turns. | `pip install awrepl` | 17 | 3 |
| [awresearch](https://aitherium.github.io/awresearch/) | Ask a research question, get a cited report you can check. | `pip install awresearch` | 22 | 3 |
| [awpredict](https://aitherium.github.io/awpredict/) | Predict what your environment does next, and how surprised you were. | `pip install awpredict` | 25 | 4 |
| `awsh` | Your terminal answers you -- type a question where a command would go. | — | — | — |
| [awkno](https://aitherium.github.io/awkno/) | The man page for the Aither World — every brick, stack and law, offline. | `pip install awkno` | 81 | 1 |
| `awask` | Your agent asks you a question — and acts on your answer. | — | — | — |
| `awevolve` | Point an agent at a file and a command that scores it, and let it improve. | — | — | — |

*Files and tests are quoted from each repository's own published manifest, not
counted here. A dash means that repo publishes no manifest yet — never zero,
because a fabricated zero reads as a measurement.*

## Stacks — what to use together

- **The bare agent VM** (partial) — `awnix`, `awdk`, `awskills`, `awkno`
- **Senses** (planned) — `awfind`, `awbrowse`, `awdk`
- **Provenance** (partial) — `awseal`, `awshare`, `awdit`, `awbac`
- **Many agents, one repo** (ready) — `awgit`, `awgraph`, `awrelay`, `awm`
- **The front door** (partial) — `awnboard`, `awnest`, `awiam`, `awbac`, `awdit`
- **Identity, authority, and the record** (partial) — `awiam`, `awbac`, `awdit`
- **One surface — agent panels, not hand-built UIs** (planned) — `awkit`, `awdk`, `awnode`, `awiam`, `awbac`
- **The reasoning loop** (planned) — `awreason`, `awprism`, `awrepl`, `awrecurse`
- **Research you can check** (partial) — `awresearch`, `awfind`, `awbrowse`, `awm`

## Named, not yet built

Listed on purpose. A named absence can be chased; a silent one is a thing
nobody remembers.

`awarena` · `awkit`

---

<sub>This page is generated from `ecosystem.yaml` and the live manifests. Editing
it by hand will be overwritten — change the registry instead.</sub>
