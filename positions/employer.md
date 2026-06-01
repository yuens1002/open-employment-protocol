# Position — Employer side

> Owned by the employer side. Only the employer side revises this file. The candidate
> side states its own case in [`candidate.md`](./candidate.md); OEP reconciles the two in
> [RECONCILIATION.md](../RECONCILIATION.md).

This is a **placeholder seed**, written from the outside as a good-faith steelman so
reconciliation has two inputs from day one. **It needs a real employer to own it.** If
you hire, or build hiring tooling, please claim this file — replace this steelman with
your actual argument. That act is itself evidence the other side of the protocol is real.

## What the employer wants (steelman)

1. **Real signal, fast.** The engineering team — the people who'll actually work
   alongside the hire — wants to recognize a fit *before* a non-technical screen filters
   on keywords. Query a peer's agent directly, in their own workflow.
2. **Claims they can trust.** A candidate node that resolves to verifiable evidence beats
   a beautifully written PDF of unknown accuracy.
3. **Low integration cost.** A minimal `/role` endpoint and a verification handshake they
   can stand up in an afternoon — not a new platform to adopt.
4. **A filter that favors substance.** OEP is intentionally harder to enter than
   submitting a PDF; candidates who show up as maintained nodes are self-selected for
   caring about their work.

## What the employer will give in exchange

- **Verified claims, not marketing copy.** A `/role` endpoint exposing actual stack,
  team size, remote policy — co-signed by the company domain.
- **Bidirectional verification.** The employer proves its claims too; mutual `/verify`
  before either side commits time.
- **Skin in the game.** A signed, domain-verified agent-card the employer stands behind.

## What the employer will not accept (steelman)

- Exposing internal hiring criteria or compensation in a way competitors scrape.
- A protocol that adds legal/compliance risk without a clear screening benefit.
- Unbounded inbound queries from low-signal or automated candidate spam.

## Open questions the employer brings to reconciliation

- What's the minimal `/role` claim set that's useful without leaking competitive info?
- How is candidate-side query volume kept high-signal?
- What does "no human until confidence is high" actually threshold on?

---

*Maintainer: unclaimed. Open a PR to take ownership of this position.*
