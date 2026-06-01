# Contributing — build the smallest version of it

OEP is a protocol, not a product, and a standard built by one person is just a project
with delusions. The most useful thing you can do here is **not** agree in a thread. It's
to build the smallest version of your agreement — or your disagreement — because a
working node is the only argument that counts, and every one that appears is verifiable
evidence the concern is shared. Solidarity you can `git clone`.

This is **disagree-by-doing**.

## Ways in, smallest first

- **10 min — become a candidate node.**
  Fork [`resume-agent-web`](https://github.com/yuens1002/resume-agent-web), point two
  env vars at any backend (even a stub `/info`), deploy. You now have a queryable node.
  Open an issue here with its URL — it joins the [evidence graph](./EVIDENCE-GRAPH.md).

- **An afternoon — build the other side.**
  Stand up a minimal employer `/role` endpoint returning *verified* claims (actual
  stack, team size, remote policy) instead of JD marketing copy. This is the missing
  half. If you do, **claim [`positions/employer.md`](./positions/employer.md)** — replace
  the steelman with your real argument.

- **A position — disagree at a specific node.**
  Open a PR against your own side's file (`positions/candidate.md` *or*
  `positions/employer.md`), or against [RECONCILIATION.md](./RECONCILIATION.md), and
  bring evidence. Rule: **you may revise only your own side's position.** Neither side
  edits the other's; OEP edits neither — it reconciles.

- **The trust plumbing.**
  Prototype the [TRUST.md](./TRUST.md) handshake — DNS-TXT domain verification, agent-card
  signing, a co-signature over a shared block. Reference implementations are the strongest
  contribution: they turn a proposed handshake point into a verified graph edge.

## What gets merged

A change lands when it carries a **falsifiable edge** — a reference implementation, a
passing test, a live endpoint, or a co-signed record — per the evidence-graph invariant.
Proposals without a verifiable edge stay open as proposals, not standard.

Conflicts aren't settled by who argues hardest or by any maintainer's decree. They're
settled by a working node that demonstrably serves the [mission](./MISSION.md) better,
and by preferring reversible handshakes. If nothing does, the honest outcome is **"left
open"** — recorded, not forced.

## Who we're looking for

Other candidates willing to be nodes. Employers willing to expose one honest endpoint.
Engineers who care about interop and verification. And people who understand governance,
the HR domain, and community stewardship better than the first author does — this needs
exactly the perspectives one person can't supply.

## Provenance norm

If AI helped you build your contribution, that's welcome and on-mission — it's value
transfer, not extraction. No need to name a tool; the work and its evidence speak.
