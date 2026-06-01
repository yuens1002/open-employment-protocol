# The evidence graph

Witnessed truth as a data model. This is the backbone: it's how a reconciled point,
or any claim a candidate or employer makes, becomes something a stranger can verify
instead of something they have to trust.

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
