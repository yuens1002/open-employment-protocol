# Reconciliation — the process

OEP does not author a standard. It reconciles two. This document is the **process** by
which the candidate side's spec and the employer side's spec are posed against each
other and netted into the minimal interoperable handshake that serves the
[mission](./MISSION.md).

The governing body is the process, not a person.

## Inputs

Two positions, each owned by its own side, each living in its own file:

- **[`positions/candidate.md`](./positions/candidate.md)** — owned by the candidate side.
- **[`positions/employer.md`](./positions/employer.md)** — owned by the employer side.

Rule: **a side may revise only its own position.** Neither side edits the other's.
OEP edits neither — it reconciles them.

## The four moves

For any point of contact between the two positions, reconciliation runs four moves:

1. **Pose both arguments.** State what each side wants and *why*, in its own words.
   No paraphrase that flattens one side into the other's frame.
2. **Locate the seam.** Mark each point as one of:
   - **aligned** — both sides already want the same thing;
   - **tradeable** — the sides want different things, but a mutually cheaper exchange
     exists (e.g. candidate reveals more once the employer's `/role` claims are
     verified);
   - **conflict** — the sides want incompatible things; neither may win by decree.
3. **Net the outcome.** Produce the *minimal* interoperable behavior that serves the
   mission. Minimal is load-bearing: the standard is the smallest handshake both sides
   can implement, not the union of everyone's wish list.
4. **Witness it.** Every reconciled point becomes a claim node in the
   [evidence graph](./EVIDENCE-GRAPH.md) with a falsifiable edge — a reference
   implementation, a passing test, a live endpoint, or a co-signed record. A reconciled
   point with no verifiable edge is a proposal, not a standard.

## How a conflict is settled (without an authority)

Conflicts are not resolved by vote of who shows up loudest, and not by OEP picking a
winner. They are settled by **evidence and reversibility**:

- The burden is on the proposal to show a *working node* that demonstrates the behavior
  serving the mission better than the status quo. Build beats assert.
- A settlement that can't be reversed if it proves harmful is rejected in favor of one
  that can. Prefer reversible handshakes.
- If no net outcome serves the mission, the honest result is **"left open"** —
  recorded as an open seam, not forced. An open-ended problem stays open until a
  verifiable resolution exists.

## Output

The reconciled handshake — the actual interoperable contract — is the net of all
**aligned** and **tradeable** points that carry a verified edge. It is intentionally
small, and it grows only by reconciliation, never by either side's decree.

## Why it needs more than one person

You cannot reconcile two sides you are standing on one side of. This process is only
honest with real candidates and real employers maintaining their own positions. That's
not a nicety — it's the load-bearing reason OEP is a *we*. See
[CONTRIBUTING.md](./CONTRIBUTING.md).
