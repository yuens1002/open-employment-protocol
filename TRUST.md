# Trust — enforcement, not authority

This is the mechanism that makes a reconciled handshake **tamper-evident**. It is
deliberately *not* where anything is decided. Trust here answers "can this claim be
verified and was it agreed by the parties named?" — never "what should the standard be?"

Decisions happen in [RECONCILIATION.md](./RECONCILIATION.md). This page is only the
cryptographic plumbing that makes those decisions checkable.

## The model: a certificate authority that stores nothing

Analogy: SSL/TLS. Domain ownership is the root of trust. The familiar shape, applied to
employment:

- **Domain verification.** A party proves it controls a domain via a DNS TXT record —
  the same move as Let's Encrypt / ACME. That domain becomes its identity.
- **Signed agent-cards.** A party signs its `/.well-known/agent-card.json` (Ed25519).
  A verifier can confirm the card belongs to the claimed domain.
- **Co-signatures.** A shared data block — say, an employment record, or a reconciled
  handshake point — is signed by *two* verified domains. Two witnesses on one claim is
  what makes it credible. (This is the `claim —co_signed_by→ domain` edge in the
  [evidence graph](./EVIDENCE-GRAPH.md).)
- **OEP stores nothing.** It is not a database of people or employment history. It
  defines the signing/verification handshake; the data lives with the parties. Federated
  trust, no centralized store, nothing to capture or sell.

## Why not OIDC / OAuth as-is

Standard OIDC expects a human-in-the-loop browser redirect. Agents are ephemeral and
need multi-hop delegation. OIDC-A (OIDC for Agents) is emerging but unsettled. The
domain-verified co-signature model above solves the peer-to-peer trust gap directly,
without inheriting redirect-flow assumptions — while staying compatible with adopting
OIDC-A later if reconciliation lands there.

## Why a walled garden won't build this

Decentralizing identity verification removes the gatekeeper's revenue. A platform whose
business is owning both sides of the conversation has no incentive to let the two sides
verify each other directly. That's precisely the gap an open protocol fills.

## Scope discipline

If you find yourself writing a *rule about what the standard requires* in this file, it
belongs in [RECONCILIATION.md](./RECONCILIATION.md) instead. Keep this file to: how to
prove a domain, how to sign a card, how to co-sign a block, how to verify each. Plumbing
only.
