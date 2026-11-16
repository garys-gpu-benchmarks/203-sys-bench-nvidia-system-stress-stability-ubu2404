# Results: 203 CPU + System Stress (Baseline Health)

**Main goal:** Analyze GPU thermal and power behavior under combined CPU and GPU load  
**Tools:** Run stress-ng --cpu --cpu-load, bin/gpu_stress (cuBLAS GEMM), and nvidia-smi --query-gpu

Reference results measured by the maintainer on the system shown in each section (generator TEMPLATE_00_143 · recorded 2026-11-16). Your own runs write `results/RESULTS_ACTUAL.md` in the same format.

> Smoke runs use deliberately small sizes. They check that the workload installs and runs end to end; their numbers are not performance results. Baseline and extended are.

<!-- profile:smoke -->
## smoke

- **System:** 1× NVIDIA H100 NVL (95830 MiB) · Intel(R) Xeon(R) Platinum 8452Y · Ubuntu 24.04.5 LTS · kernel 6.8.0-138-generic · driver 595.91.07
- **Run:** 2026-11-16T18:59:40Z · status **PASS** (exit 0)
- **Time (mm:ss):** setup 01:10 · benchmark 00:11 · whole run 01:26
- **Source:** run 203_20261116_185940
- **Command:** `bash run_benchmark.sh --smoke --num-threads 16 --cpu-load-percent 50 --gpu-load-percent 50 --temp-threshold 85 --power-threshold 700 --duration 5 --poll-interval 1`

| # | Metric | Result |
|---|---|---|
| 1 | Peak GPU temperature (peak_gpu_temperature_c) | 39.0 |
| 2 | Sustained GPU power (sustained_gpu_power_w) | 232.642 |
| 3 | GPU ECC error count (gpu_system_ecc_error_count) | 0.0 |
| 4 | Thermal throttle events (thermal_throttle_event_count) | 0.0 |
<!-- /profile:smoke -->
