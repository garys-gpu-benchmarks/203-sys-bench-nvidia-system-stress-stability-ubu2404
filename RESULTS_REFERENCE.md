# Results: 203 CPU + System Stress (Baseline Health)

**Main goal:** Analyze GPU thermal and power behavior under combined CPU and GPU load  
**Tools:** Run stress-ng --cpu --cpu-load, bin/gpu_stress (cuBLAS GEMM), and nvidia-smi --query-gpu

Reference results measured by the maintainer on the system shown in each section (generator TEMPLATE_00_138 · recorded 2026-11-12). Your own runs write `results/RESULTS_ACTUAL.md` in the same format.

> Smoke runs use deliberately small sizes. They check that the workload installs and runs end to end; their numbers are not performance results. Baseline and extended are.

<!-- profile:smoke -->
## smoke

- **System:** 1× NVIDIA H100 NVL (95830 MiB) · AMD EPYC 9374F 32-Core Processor · Ubuntu 24.04.5 LTS · kernel 6.8.0-138-generic · driver 595.91.07
- **Run:** 2026-11-12T22:37:38Z · status **PASS** (exit 0)
- **Time (mm:ss):** setup 00:34 · benchmark 00:09 · whole run 00:49
- **Source:** run 203_20261112_223738
- **Command:** `bash run_benchmark.sh --smoke --num-threads 16 --cpu-load-percent 50 --gpu-load-percent 50 --temp-threshold 75 --power-threshold 700 --duration 5 --poll-interval 1`

| # | Metric | Result |
|---|---|---|
| 1 | Peak GPU temperature (peak_gpu_temperature_c) | 52.0 |
| 2 | Sustained GPU power (sustained_gpu_power_w) | 225.06199999999998 |
| 3 | GPU ECC error count (gpu_system_ecc_error_count) | 0.0 |
| 4 | Thermal throttle events (thermal_throttle_event_count) | 0.0 |
<!-- /profile:smoke -->
