# Open Employment Protocol (OEP)

> **This repo does not define the standard. It reconciles two that do.**

OEP is the neutral ground between two sides of hiring that don't naturally agree —
the **candidate** who wants to be seen fairly and stay sovereign, and the **employer**
who wants real signal instead of noise. Each side brings its own concerns and its own
spec. OEP doesn't hand down law from above. It **poses both arguments and settles the
net outcome toward the mission** — and records that reconciliation as evidence anyone
can verify.

No party writes the rules. The standard *is* the reconciliation.

---

## Why this exists

AI used as a black box to do existing work cheaper creates no *net new* value: same
output, fewer people paid, savings routed to whoever owns the model. Every prior
automation wave eventually created **more** work — but only because the tools were
**open** enough for displaced people to re-enter as creators. AI's means of
production (compute, data, models, distribution) are unusually **concentrated**, so
that escape hatch isn't guaranteed this time.

OEP bets on the other path: use AI for value **transfer** — compound knowledge into
innovation, keep individuals sovereign and queryable, and route the matching market
around any single captor so people re-enter as *builders*, not get filtered out by a
black box.

The mechanism that makes it true is openness itself: **a truth kept private is only
half a truth — it has no outside witness to validate it.** Publishing it, and letting
humans and machines query it, is what makes it true. Trust by action, in the open.

See **[MISSION.md](./MISSION.md)** for the full argument (stated so you can attack it).

---

## The trifecta — three independent repos, no single owner

By design, no one concern owns the protocol or profits from its friction:

| Repo | Role | Its concern | Status |
|---|---|---|---|
| **[`resume-agent`](https://github.com/yuens1002/resume-agent)** + **[`resume-agent-web`](https://github.com/yuens1002/resume-agent-web)** | Candidate side — a queryable, signed agent | be seen fairly · own your data · stay sovereign and queryable | **live, open-source, forkable** |
| **`oep-recruiter`** (role-agent) | Employer side — verified claims, not marketing copy | find real signal · verify claims · filter the noise | *the missing half — being opened up* |
| **`oep`** (this repo) | The **reconciler** | hold both arguments · settle the net outcome · keep it no one's to own | *being opened up* |

The candidate side already exists and runs. The employer side and this reconciler are
what we're **calling collaborators to build** — because a standard built by one person
is just a project with delusions, and you cannot reconcile two sides you are standing
on one side of.

---

## What "reconciler, not author" means in practice

OEP's job is four things, none of which is "decide the spec":

1. **Hold both positions.** `positions/candidate.md` and `positions/employer.md` state
   each side's argument in its own words. Either side can revise its own file; neither
   side edits the other's.
2. **Reconcile them into a net outcome.** [RECONCILIATION.md](./RECONCILIATION.md)
   defines the process: where the two positions meet, where they conflict, and the
   minimal interoperable handshake that serves the mission without either side winning
   by decree.
3. **Record the reconciliation as a verifiable evidence graph.**
   [EVIDENCE-GRAPH.md](./EVIDENCE-GRAPH.md) is the data model — claims/positions as
   nodes, git SHAs / tests / live endpoints / signed records as evidence, with one
   invariant: **every edge is falsifiable.**
4. **Enforce — not dictate — the agreed handshake.** [TRUST.md](./TRUST.md) is the
   CA-style mechanism (domain-verified co-signatures; stores nothing; signs the
   handshake). It's *how* a reconciled agreement is made tamper-evident, not *who*
   decides what's in it.

---

## How to join — build the smallest version of it

We're not asking you to agree in an issue thread. We're asking you to **build the
smallest version of your agreement or your disagreement** — because here a working
node is the only argument that counts, and every one that appears is verifiable
evidence the concern is shared. Solidarity you can `git clone`.

- **10 min** — fork [`resume-agent-web`](https://github.com/yuens1002/resume-agent-web),
  point two env vars at any backend, and you have a queryable candidate node.
- **An afternoon** — sketch the other side: a minimal employer `/role` endpoint that
  returns *verified* claims (actual stack, team size, remote policy) instead of JD copy.
- **A position** — disagree at a specific node: open a PR against
  `positions/candidate.md` or `positions/employer.md`, or against
  [RECONCILIATION.md](./RECONCILIATION.md), and bring your evidence.

If you build a node, tell us — it becomes part of the graph that proves this is a
trajectory many people share, not one person's pitch. See
**[CONTRIBUTING.md](./CONTRIBUTING.md)**.

---

## Status

Early and deliberately open-ended. The candidate side is real and running; this repo
and the employer side are being stood up *with* collaborators rather than handed down
finished. Nothing here is settled by fiat — it's settled by reconciliation, in the open.

## Provenance

Built with heavy AI assistance, deliberately unnamed — it wasn't one tool, it was the
compounded intelligence of many iterations before this one. That's the thesis enacted:
build on top of accumulated capability and pass it forward, rather than treat it as a
black box that returns a cheaper copy of the work.

## License

[MIT](./LICENSE) — take it, reconcile it, keep it no one's to own.
