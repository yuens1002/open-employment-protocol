# Governance — how a reconciled position becomes a living standard

> **This is the biggest open problem in this repo, and it is unsolved. On purpose, it is
> stated here rather than hidden.**

[RECONCILIATION.md](./RECONCILIATION.md) describes how the candidate side's spec and the
employer side's spec get posed against each other and netted into an outcome. But a
settlement on paper is not a standard. A standard is a settlement that is **published,
versioned, stewarded, and adopted** — and kept *no one's to own* while still being
operable. That layer — turning a reconciled position into a living thing implementers can
build against — is the **manifestation gap**, and it is not solved here yet.

## The honest statement of the gap

I have the protocol idea, and a running, open candidate-side reference implementation
([resume-agent](https://github.com/yuens1002/resume-agent) +
[resume-agent-web](https://github.com/yuens1002/resume-agent-web)). I do **not** have the
experience to stand up the foundation-grade governance an open standard needs — the
"IETF / W3C / Linux Foundation"-shaped layer: a neutral home, a change process, a way to
ratify a reconciliation, versioning, a publication format implementers can target, and an
IPR/licensing policy that keeps the spec un-ownable.

**This is an experience gap, not an idea gap.** Pretending otherwise would betray the whole
thesis — a protocol that hid its governance gap behind confident prose would be exactly the
black-box dishonesty OEP exists to refuse. The [evidence-graph](./EVIDENCE-GRAPH.md) method
says: name your missing edge. This is the largest one.

## So naming it *is* the work right now

This repo is therefore, today, a **staging ground — not a foundation.** It holds the
positions, the reconciliation process, and the evidence-graph method. The governance layer
is explicitly *to-be-reconciled-by-the-we*, and recording that here is what keeps the gap
witnessed instead of papered over.

## The call — the highest-leverage contribution to OEP

Above code, the contribution OEP most needs is **standards-governance experience.** If you
have worked on any of these, you are exactly who this is for:

- open-standards process and stewardship (IETF rough-consensus, W3C, OASIS, ECMA);
- neutral-home / foundation operations (Linux Foundation, OpenJS, Apache, CNCF);
- IPR / licensing policy for specifications that must stay un-ownable;
- spec publication, versioning, and conformance/reference-implementation discipline.

You do not need to agree with the thesis to help. Disagreeing with *how it should be
governed*, with evidence from a model that works, is the most valuable thing you can bring.

## Open questions — answerable in a PR or issue

These are concrete enough to engage directly. An answer with precedent and tradeoffs is a
real contribution:

1. **Where should a reconciled outcome live** so no single party owns it — a neutral
   foundation, a chartered repo, a registry? What's the lightest structure that is still
   credibly neutral?
2. **How is a reconciliation ratified** — what's the change process from "proposed handshake
   point" to "ratified standard"? Rough consensus + running code (IETF)? A two-independent-
   implementations rule (W3C)? Something smaller?
3. **How is it versioned and published** so implementers build against something stable
   rather than a moving README?
4. **What licensing / IPR policy** keeps the spec un-ownable while permitting reference
   implementations? (This repo is MIT today — is that right for a *spec*, or does it need a
   W3C-style patent/IPR grant?)
5. **What is the minimum honest governance** — enough to ratify and publish, without
   prematurely erecting a bureaucracy the protocol hasn't earned yet?

## Interim stance (until the above is reconciled)

- Changes still land by the [evidence-graph](./EVIDENCE-GRAPH.md) rule: a proposal becomes
  standard only when it carries a falsifiable edge (a reference implementation, a passing
  test, a live endpoint, a co-signed record).
- The [trust mechanism](./TRUST.md) provides *enforcement* (tamper-evidence) but is **not**
  governance — it cannot decide what the standard is, only verify what two parties agreed.
- Nothing in this repo is ratified yet. It is a proposal staged in the open, waiting for the
  people who can build the part its author honestly cannot.
