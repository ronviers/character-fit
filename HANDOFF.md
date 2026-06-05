# HANDOFF — net one new substrate per session

A worklist, not a method. The method is [`RECIPE.md`](RECIPE.md); don't restate it
here. Standing objective: **each session takes exactly one substrate through the
RECIPE and leaves a verdict behind.** Over time that grows the framework's
evidence base past its single confirmed real instance (DNA-NESS).

## What counts as netting a substrate

A traversal is netted when `<substrate>/` holds:
- `<substrate>.py` — one self-contained script (copy-and-adapt a generator from
  [`simulators/`](simulators/), or transcribe a real substrate's measured numbers
  in-file).
- the sealed expected reading, written *before* the fit, inside the script.
- `view.png` — one picture.
- `RESULT.md` — the verdict (MATCH / MISS / KILL) and an honest scope note.

A **KILL counts as a netted substrate** — a clean falsification is the most
valuable result, not a failure. And verify the substrate's *own* ground truth
before its verdict counts: an invalidator like `ou_equilibrium` must first be
confirmed to honor FDT (X=1) so that an aging read there is a real false positive,
not a bug in the run.

A **deep scar counts too.** A traversal that surfaces a genuine, generalizable
failure mode — a new line for THE TRAPS in the RECIPE — is a netted success even
without a clean MATCH / MISS / KILL: the apparatus got sharper, which is the point.
Record it in `RESULT.md` and propose the trap.

## How to pick the next one (tiered)

1. **A real measured substrate whose numbers are in hand** — the prize, the thing
   that actually grows the framework. Queue one only once its data is already in
   the script (external sources rot — the DNA-NESS SI returned 403).
2. **Else the next invalidator** — synthetic but high-value: each is a known-truth
   attack built to make the framework fail.
3. **Else the next honest simulator** — keeps cadence, widens the substrate basis.

## Queue

**Tier 1 — real (the prize):**
- **β-collapse on a real substrate** — the framework's central bet: one memory
  exponent β governing aging C(t), the waiting-time tail, and the memory-kernel
  shape *at once*. Live candidate: the gastropod shell data already in
  `character-framework/data/` (Collins 2021, Dryad p5hqbzknw). Per the framework
  README, β has never been put to a real substrate as a three-measurement
  collapse — this is the sharpest single thing that can break the reading.
- **Active-lattice minted current** — Veenstra/Bartolo (Zenodo) circulation data.
  Known-hard: no perturbation protocol + artifact-dominated Var(J). Queue only
  when a two-frame read becomes reachable.
- **A fresh lead** — source the next real substrate through the outbound research
  channel; queue it once its numbers are in hand.

**Tier 2 — larder (cadence + falsification):** the 5 invalidators
(`ou_equilibrium`, `ising_equilibrium`, `driven_ring`, `mm1_queue`,
`logistic_chaos`), then the other honest simulators (`voter sk abp fbm sir east
wright_fisher heston lotka_volterra levy_flight two_temp_ou kww_oracle` + the
`constant/sine/square/white_noise` controls).

## Ledger (landed)

| substrate | kind | verdict | where |
|---|---|---|---|
| DNA-NESS (Nicholas 2025) | real, measured | MATCH — minted + protected + sustained; nonlinear cross-check confirmed | [`dna_ness/`](dna_ness/) — the worked exemplar (read + cross-check + `view.png` + `RESULT.md`); also the framework's one confirmed real instance |

## NEXT

**`ou_equilibrium`** — the first traversal in this repo. Cheap, exact analytic
truth (`C = e^{-t/τ}`, X=1, no aging, no current), and an invalidator: a false
aging or X≠1 read is a real falsification. Copy `simulators/ou_equilibrium/`, seal
*"equilibrium — X=1, no aging, no current,"* run the reads, **sweep the camera
(τ_obs) first**, make the picture, write the verdict. This proves the RECIPE
end-to-end in character-fit for the first time, and exercises the new
identifiability trap (X must be read where the data constrains it).

## Keep this thin

After a traversal: append one ledger line, drop the substrate from the queue, set
NEXT to your pick. That is the whole maintenance. If this file starts explaining
*how* to run a traversal, that belongs in the RECIPE — delete the drift. A clean
real PASS worth citing gets promoted into `character-framework` (an `experiments/`
script + a `character_receipts.md` line), the way DNA-NESS is; synthetic and
invalidator traversals stay here as the falsification record.
