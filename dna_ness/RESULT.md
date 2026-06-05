# dna_ness — RESULT

substrate: **Nicholas et al. fuel-driven DNA-NESS** (Angew. Chem. Int. Ed. 2025,
10.1002/anie.202512967; open PMC12535392) · kind: **real, measured** · verdict:
**MATCH** · view: `view.png` · scripts: `dna_ness.py` (the read) +
`dna_ness_crosscheck.py` (independent confirmation)

The first netted substrate, and character-fit's worked exemplar of a complete
traversal: a real driven chemical network reads as emergent identity — a protected
NESS circulation *minted* by the drive, not stored.

## Sealed (before the fit)

A detailed-balanced DNA-hybridization cycle (A=0 on its own) driven by RNase-H fuel
hydrolysis into a protected, sustained NESS circulation — minted ∧ protected ∧
sustained, on measured rates. Expected: MATCH.

## The read — `dna_ness.py` (N=3 reduction on measured rates)

- **Minted** ✓ — Module A alone (reversible hybridization triangle) A=0
  (Kolmogorov / detailed balance); Module B alone (enzyme drain) A=0; coupled
  A≈+14.5 with J≠0. The current is created by the coupling, absent in either part.
- **Protected** ✓ — sign(A) is drive-locked: 0/400 reciprocal deformations of the
  hybridization rates flip it. The enzyme is irreversible, so sign(A) can only be
  zeroed by removing the drive — never flipped (stronger than "rewire").
- **Sustained** ✓ — cut the drive (k_deg→0): J→~1e-15 (detailed balance restored,
  collapses); sever the Q↔OQ edge: J→~1e-16 (no cycle). Run-loop, nothing stored.

[F],[O] cancel around the cycle, so minting + protection rest on the measured
constants alone; the baths set only the current magnitude.

## The confirmation — `dna_ness_crosscheck.py` (full nonlinear network)

Built the full mass-action network (8 reactions, SI Sec. 3), integrated to NESS,
compared against the N=3 reduction:
- the full network circulates (minting holds in the full model);
- the N=3 reduction reproduces the per-quencher cycling rate to within ~15%, same
  sign — faithful, not a reduction artifact;
- fuel-cut run-loop: circulation collapses to <1% on a timescale consistent with
  the SI's experimental ~3-min recovery.

## Honest scope

- N=3 reduction of a ~10-species CRN: enzyme folded to a pseudo-first-order drain
  k_deg (QSS on FQE, [E] chemostatted); output O / fuel F are baths.
- [F],[O] set the current magnitude (representative NESS values); they cancel in
  the protected affinity.
- kFrebind_r taken from the SI's own detailed-balance constraint (matches the
  published 7.6e-9 to 2 sig figs).
- Slow side-processes (waste, enzyme deactivation — the SI's own "drift") omitted
  for a clean NESS.

## Why this is a real MATCH, not a tautology

The data path is independent: the rate constants are measured (SI), the
affinity/current are computed from them, and the full-network cross-check is an
independent forward model — not the reduction's own algebra. A KILL would have been
any of minted / protected / sustained failing on the measured rates, or the full
network failing to circulate. None did.
