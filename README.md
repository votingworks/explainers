# VxSuite Explainers

Interactive, self-contained HTML explainers for
[VxSuite](https://github.com/votingworks/vxsuite) engineering changes, hosted
via GitHub Pages at https://votingworks.github.io/explainers/.

Each explainer is a single HTML file with no external dependencies — all
styles, scripts, and graphics are inline, so the pages work offline and will
render identically for as long as the links live.

## Explainers

| Page | Subject |
| ---- | ------- |
| [streak-detection.html](https://votingworks.github.io/explainers/streak-detection.html) | How reordering pixel reads to match memory layout made ballot streak detection 5× faster (`vxsuite` ballot-interpreter) |
| [otsu-sharding.html](https://votingworks.github.io/explainers/otsu-sharding.html) | How sharding the Otsu histogram into eight interleaved copies halved page preparation — out-of-order execution, not SIMD (`vxsuite` ballot-interpreter) |
| [bubble-popcount.html](https://votingworks.github.io/explainers/bubble-popcount.html) | How bit-packing bubble-template rows into `u64`s made bubble scoring 6× faster — shift, OR, mask, popcount (`vxsuite` ballot-interpreter) |
| [qr-half-density.html](https://votingworks.github.io/explainers/qr-half-density.html) | How QR codes are found with 1-D scan lines and the 1:1:3:1:1 finder signature, and why half the lines are enough (`vxsuite` ballot-interpreter) |

## Adding an explainer

1. Add a self-contained `*.html` file at the repo root (no CDN scripts, fonts,
   or other external requests).
2. Add it to the list in `index.html` and the table above.
3. Push to `main` — the Deploy Pages workflow publishes automatically.
