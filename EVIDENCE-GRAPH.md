# The evidence graph

Witnessed truth as a data model. This is the backbone: it's how a reconciled point,
or any claim a candidate or employer makes, becomes something a stranger can verify
instead of something they have to trust.

> **TL;DR** — Truth you can verify, not trust. Claims are nodes; the proof is the
> *edge*. A claim with no falsifiable out-edge is just an assertion. The first populated
> instance is this project's own trail — a premise logged (and **dated**) *before* the
> implementation, then evidence that showed up *after* it shipped, all examinable live.
> Skim **[the reference trail](#the-reference-trail--examine-it-yourself)**, or just go
> to **[yuens.me](https://www.yuens.me)** and ask it *"what is OEP?"* and *"what evidence
> is there for the work?"* — the answers are grounded in the dated reasoning below.

## The one invariant

**Every edge is falsifiable.** You can traverse `claim → evidence → verification` and
get a hard yes/no. A node with no verifiable out-edge is just an assertion. A half-truth
is a node with no witness edge.

The graph's worth is **edge-density and edge-verifiability** — not how many claims it
holds, but how many of them you can check.

## Nodes

- **claim / reasoning** — e.g. *"test coverage went 50→80% at $project"*,
  *"AI-as-replacement is net-zero value"*, or a reconciled handshake point.
- **evidence** — a git SHA, a repo, a test result, a live URL, a signed agent-card, an
  OB1-style observation, an external query event.
- **witness** — who attests: self, an employer domain, an eval harness, a stranger's
  model.

## Edges (all falsifiable)

- `claim —is_evidenced_by→ evidence`
- `evidence —verified_by→ method` (with a checkable result)
- `claim —co_signed_by→ domain` (two witnesses on one block — see [TRUST.md](./TRUST.md))
- `reasoning —stands_on→ claim`
- `position —reconciled_into→ handshake_point` (the reconciliation's own trace)

## How it maps to what already exists

- **Reasoning/claim nodes** — the candidate's profile + observations (the inward mind).
- **Work-evidence nodes** — git history, deploys, test inventories.
- **Witness edges** — Ed25519 agent-card signing + domain co-signatures (cryptographic).
- **Edge resolver** — the planned `/verify` endpoint: return the SHA-linked evidence for
  a given claim. Traversal over HTTP.
- **Witness events** — real external queries against a live agent; an independent model's
  assessment. Proof the graph is exercised, not theoretical.

## The reference trail — examine it yourself

The first populated instance of this graph is this project's own history. I'm putting
it here as an open invitation: **examine my path.** Don't take the shape on faith —
traverse it. The premise was logged in a private reasoning brain (OB1) and *dated*; the
implementation shipped; and only *then* did the evidence arrive. Because the premise
predates the evidence, you can check that the trail wasn't reverse-engineered from the
result — the timestamps are the witness.

### Premise nodes — logged *before* the evidence existed

Dated reasoning, captured as it happened (queryable live; ask the agent and it answers
from these):

- **2026-03-28** — *premise:* hiring should be an open protocol — "the email equivalent
  for hiring; any server, any client." resume-agent named as the candidate-side
  reference, "the employer side is the missing half." (The trifecta, implicit on day one.)
- **2026-04-22** — *premise discovered in the code, not designed:* "the public MCP +
  agent-card is a generic **base layer**, not a vertical — resume-agent is the reference
  implementation, not the final form," and "self-sovereign identity solves AI
  hallucination — your agent is your truth." This is the moment "my résumé" became "a
  protocol."
- **2026-05-06 / 05-07** — *premise articulated:* the résumé is no longer the artifact,
  the agent is; you're a node, not a document; CA-style federated trust (domain
  verification, co-signatures, "stores nothing, signs the handshake").
- **2026-06-01** — *premise sharpened:* AI-as-black-box reproduces existing work for no
  *net new* value; open tools are the hidden dependency of every past automation wave;
  use AI for value **transfer**, not extraction.

### Implementation nodes — the work, checkable

- `resume-agent` (live backend), `resume-agent-web` (live, MIT, forkable),
  **[yuens.me](https://www.yuens.me)** (running reference instance).
- Public surfaces: `/info`, `/query`, `/match`, a public MCP `ask_candidate` tool, an
  A2A agent-card, Ed25519 domain verification, and a public eval harness ("Truth
  Contract") that fails on fabrication or dropped citations.

### Evidence nodes — what showed up *after* it shipped

The validation the premise did not assume, and could not manufacture:

- **66 real external queries over 62 days**, 18 distinct IPs, callers self-tagged
  **interviewer (11)**, **ATS-screening (7)**, **ai-agent (5)**, plus 20 via Claude-User.
  The market used the door before it was formalized.
- **An independent model's verdict.** A separate ChatGPT session, handed only the public
  profile, assessed the candidate as "unusually aligned with an open employment protocol
  effort" and surfaced the *same* hard problem reasoned to internally (governance/adoption,
  not capability). A convergent outside witness.
- **A live falsifiable answer.** A visitor asked *"what evidence is there for the work
  presented?"* and the agent answered with artifacts — per-repo commit counts, test
  inventories, live endpoints, domain verification — naming its own Truth Contract.

### Traverse it

| Surface | What to do | What you can check |
|---|---|---|
| **Human** | open [yuens.me](https://www.yuens.me), ask *"what is OEP?"*, *"what led to it?"*, *"what's the evidence for the work?"* | the answers trace back to the dated premises above |
| **Machine** | call the public MCP `ask_candidate` tool, or read the A2A agent-card | the same trail, agent-to-agent |
| **Code** | read the repos — commits, tests, deploys | the implementation nodes resolve to real artifacts |

## Surfacing OB1 observations — the truth layer, made examinable

The premises and lessons (the "why," not just the "what") live as **observations** in
OB1 — the inward reasoning brain. Public-eligible observations are *already* the source
the live agent answers `/query` and the public MCP from, so the reasoning trail is
examinable today by asking. That's the current "way to add an observation to the graph":
capture it (public-eligible), and it becomes a queryable premise node the agent will cite.

**The honest gap, and the build-invite.** Semantic query surfaces the reasoning but
doesn't give each observation a *stable, linkable* citation with its date and its
resolved evidence edges. The enhancement that closes it is a curated, read-only
**observations surface** on the candidate-side backend — the [edge-resolver](#how-it-maps-to-what-already-exists)
(a `/verify`-style endpoint) made browsable: one stable id per premise, its date, and the
artifacts it stands on. That's an open contribution on `resume-agent`; until it lands,
the curated trail above plus live queries are the examinable form. (This is the
context-poverty gap logged 2026-04-30 — surfaced here on purpose: the graph names its
own missing edge.)

## Why an open-ended problem needs this exact form

Publishing an evidence graph is not publishing an **answer** — it's publishing a
**traceable line of inquiry**. The graph doesn't require you to be right; it requires
your reasoning and its support to be *checkable*:

> problem (evidenced) → each reasoning step (evidenced) → the work (evidenced) →
> outside validation (evidenced)

That turns **"trust me"** into **"verify me — then build with me."** A community can't
join a finished solution; it *can* join a graph — fork a branch, extend it, or disagree
at a specific node and bring its own evidence. The honesty is the architecture, and the
architecture is what lets more than one person solve the problem.

## Build-as-evidence

When someone forks a candidate node or stands up an employer `/role` endpoint, that
working node is **itself a witness edge** — falsifiable proof the concern is shared and
the trajectory is real, not a solo pitch. The graph grows by people building, not by
people agreeing.
