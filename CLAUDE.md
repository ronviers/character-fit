# character-fit — session discipline

Read [`RECIPE.md`](RECIPE.md) first. It is the entire process. This file is the
only standing instruction beyond it.

- **Reinvent from scratch.** No shared framework, no imported pipeline, no
  abstraction built up front. One bespoke script per substrate. If two scripts
  end up sharing math, copy it — don't build a library to hold it until the
  shape has earned itself across many substrates. *It was never brittle if it
  never broke.*
- **The substrate is never touched.** You fit the analytic reference *to* the
  substrate's pristine data; you never bend the data onto a template. Whenever
  the thing you're scaling or clamping seems to be the substrate, stop — it's the
  reference.
- **Two habits are non-negotiable** (THE TRAPS in `RECIPE.md`): seal the expected
  answer before you fit, and treat a KILL as a real falsifier. Losing either
  hollows every verdict. For a structurally-blind read, hand a fresh subagent
  only the sealed-off data + the question, never the seal.
- **Don't rebuild the meta.** The bounding box, the block-in, the four-module
  SOP, the scale-management RFC — all frozen in `mpa-conform` on purpose. If you
  feel the urge to write a document that describes the process, write a substrate
  script instead.
- **No declared virtues in copy.** Show the behavior; don't announce it.

Everything 'mpa' is frozen. This repo does not read from or write to it.
