# character-fit

Fit **character** into a substrate, run one test, read one artifact.

No framework, no pipeline, no scale-management layer, no governance docs. Each
substrate is a single self-contained script — written from scratch — that
reduces the substrate to the smallest structure that could carry the character
signature and checks it against a sealed analytic answer. The skill lives in the
recipe and in whoever is running it, not in a reusable machine.

**The whole process is two cards: [`RECIPE.md`](RECIPE.md).** Read it; it is the
repo.

## What a substrate looks like here

One file. It builds the minimal model, seals the expected reading, runs the
reads, draws one picture, and prints `MATCH` / `MISS` / `KILL` against the seal.
When it's done it leaves one result file behind. Then the next substrate.

## Lineage

Successor to the frozen `mpa-conform`. Everything that elaborated on the process
— the bounding box, the block-in, the four-module SOP, the scale-management RFC
— stayed behind. Only the recipe came across.

## License

MIT.
