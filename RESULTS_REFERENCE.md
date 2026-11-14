# Results: 123 BERT Inference Sweep

**Main goal:** Measure PyTorch BERT inference performance  
**Tools:** Run inline transformers.BertModel.from_pretrained on synthetic token batches

Reference results measured by the maintainer on the system shown in each section (generator TEMPLATE_00_141 · recorded 2026-11-14). Your own runs write `results/RESULTS_ACTUAL.md` in the same format.

> Smoke runs use deliberately small sizes. They check that the workload installs and runs end to end; their numbers are not performance results. Baseline and extended are.

<!-- profile:smoke -->
## smoke

- **System:** 1× AMD Instinct MI300X VF (196288 MB) · INTEL(R) XEON(R) PLATINUM 8568Y+ · Ubuntu 24.04.5 LTS · kernel 6.8.0-147-generic · driver 7.1.9.31600000
- **Run:** 2026-11-14T11:23:23Z · status **PASS** (exit 0)
- **Time (mm:ss):** setup 01:22 · benchmark 00:01 · whole run 01:36
- **Source:** run 123_20261114_112323
- **Command:** `bash run_benchmark.sh --smoke --model-name bert-base-uncased --dtype f16_r --sequence-len 32 --batch-size 1 --warmup-iters 2 --num-iterations 5`

| # | Metric | Result |
|---|---|---|
| 1 | Inference throughput (sequences_per_sec) | 269.76155829833164 |
| 2 | Inference latency, mean step time, ms (mean_latency_ms) | 3.706977399997413 |
| 3 | Token throughput (tokens_per_sec) | 8632.369865546612 |
| 4 | Peak GPU memory (peak_gpu_memory_gb) | 0.32100608 |
<!-- /profile:smoke -->
