# simulators — frozen honest-simulator larder

Twenty-one data-path-independent simulators carried from the frozen
`mpa-central/library/primitives/`. Each is a thin honest reproduction of a named
substrate that generates its own data (or runs a small in-process simulation) —
no external dataset required at run time. The prior-art attribution lives in each
module header (e.g. `voter` → Mobilia 2023, Leeds 1080, CC-BY-4.0).

**This is a larder, not a library.** Reference material to *copy and adapt*, not a
package to import wholesale. When you do a substrate from scratch (per
[`../RECIPE.md`](../RECIPE.md)), lift its simulator, inline the bits of `_shared/`
it actually uses, and drop the rest — the new substrate script must stand alone.
`_shared/protocol.py` + `runtime.py` are here only so an old simulator still runs
as a reference; they are not the going-forward contract.

**Why these survived the migration:** they are the honest *generators* — the
thing that produces a substrate's data independently of the code that fits it
(THE TRAPS: *ground truth is independent*). What did **not** come across: the
138 MB of cached cells they produced (regenerable, carrying an overdue refresh
debt — frozen in `mpa-central/library/data/`), and the grinder that orchestrated
them (`grind_library.py`, `MANIFEST.json` — the reusable-machine apparatus the
pivot sheds). Ignore the old per-primitive `grind.py` entry points and the
streaming-event protocol they emit; in a from-scratch script you drive the
simulator however the RECIPE wants and read `(C, χ)` straight off it.

## The simulators

| Name | Domain | OP axis | Reference dataset |
|---|---|---|---|
| `voter` | Network dynamics / opinion | switching rate ν | Leeds 1080 (CC-BY 4.0) |
| `sk` | Mean-field spin glass | T | Zenodo 4318983 (CC-BY 4.0) |
| `abp` | Active matter / colloids | Péclet Pe | amep (BSD-3) |
| `fbm` | Anomalous diffusion | Hurst H | AnDi (CC-BY) |
| `sir` | Epidemic dynamics | R₀ | CDC `cfa-gam-rt` (public domain) |
| `east` | Kinetically constrained model | T | KCM literature |
| `wright_fisher` | Population genetics | selection s | Dryad wdbrv162z (CC0) |
| `heston` | Financial / regime-switching | regime pack | Kaggle fsynth (MIT) |
| `lotka_volterra` | Predator-prey ecology | prey α | SLV literature |
| `levy_flight` | Lévy CTRW / heavy tails | tail α | AnDi (CC-BY) |

### Invalidator battery — built to make the framework fail

Five substrates with a known ground truth and a stated falsifier; the point is the
*read*, not coverage. Verify the substrate's own ground truth before its verdict
counts (e.g. `ou_equilibrium` is confirmed to honor FDT, X≈1, so any aging read
there is a real false positive — *not* a discovery).

| Name | Attack | Falsifier |
|---|---|---|
| `ou_equilibrium` | analytic FDT null (exact `C=e^{-t/τ}`, X=1) | reports X≠1 or aging |
| `ising_equilibrium` | critical-slowing ≠ aging (2D Ising at Tc) | persistent X<1 in equilibrium |
| `driven_ring` | sustained NESS current — attacks "everything → r" | r forced on a perpetual current |
| `mm1_queue` | common-exponent triality (a named corpus falsifier) | α_s ≠ heavy-traffic exponent ½ |
| `logistic_chaos` | attacks the stochasticity premise (deterministic, no bath) | a finite FDT-respecting regime on a Lyapunov-divergent system |

The remaining directories (`constant`, `sine_wave`, `square_wave`, `white_noise`,
`kww_oracle`, `two_temp_ou`) are controls, oracles, and known-truth cases — for
sanity-checking a read before you trust it on a real substrate.
