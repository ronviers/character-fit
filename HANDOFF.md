# HANDOFF — fit character to one substrate

Each session: take **one** substrate through [`RECIPE.md`](RECIPE.md) and leave a
verdict — a folder `<substrate>/` with the script (sealed answer inside),
`view.png`, and `RESULT.md`. That's the whole job. Worked example:
[`dna_ness/`](dna_ness/) (real, measured → MATCH).

## NEXT — `two_temp_ou`

Two coupled Ornstein–Uhlenbeck variables held at different temperatures: a real
NESS with a sustained heat current and a genuine FDT violation (X<1) — the first
substrate here with **actual character**, not a null, and with an **exact analytic
answer** (it's linear, so the stationary covariance and the response are closed
form; the simulator's operating points are even labelled by their true X). It also
walks straight into the identifiability trap — a naive 1-parameter fit can't
recover X; read X off the **raw FDR slope**.

It's already in [`simulators/two_temp_ou/`](simulators/two_temp_ou/). Copy it, seal
the expected reading (heat current present; X<1 set by the temperature gap; the
exact stationary covariance), **sweep the camera (τ_obs) first**, one picture,
verdict.

*(This is the pickup from frozen `mpa-conform`: its block-in named a reciprocal
coupled pair as the natural next, with two_temp_ou the substrate in hand. We take
it the lean way — one self-contained script, no oracle build, no blind pass, no
category taxonomy.)*

---

A **KILL** counts as a win (a clean falsification), and so does a **deep scar** (a
new line for THE TRAPS). Verify the substrate's own ground truth before its verdict
counts. After a traversal: add one line to Done, set the next NEXT, keep this file
thin — if it starts describing *how* to run a traversal, that's the RECIPE; delete
the drift.

## Done

- **DNA-NESS** (real, measured) → MATCH — minted + protected + sustained.
  [`dna_ness/`](dna_ness/).

A real measured substrate outranks any synthetic one — it's what grows the
framework; source one via [`SOURCING.md`](SOURCING.md) and queue it once its numbers
are in the script.
