# laya-check

Benchmark charts for the Mongolian classifier in [laya-mn](https://github.com/e9tgldr/laya-mn).

| Image | What it shows |
|---|---|
| `laya_benchmark.png` | laya-mn vs the shipped multilingual baseline |
| `laya_benchmark_common.png` | Same, restricted to commonly-hit scenarios |
| `laya_vs_jev.png` | laya-mn vs JEV |
| `laya_vs_jev_full.png` | The full breakdown |

The headline: the shipped multilingual checkpoint scores **0.3035** on the Mongolian test split. The fine-tuned model scores **0.8984** — 2.96× better across 5,668 decisions.

The JEV comparison matters because JEV is the commercial product people in Mongolia are sold. What surprised me is not that my model wins, but that the baseline is not merely inaccurate — its calibration error is 0.4277, meaning it is *confidently* wrong. That is the more persuasive number.
