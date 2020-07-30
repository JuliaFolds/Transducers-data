# Benchmark result

* Pull request commit: [`246886f6307aebe4936e62119b5aa0e598de7428`](https://github.com/JuliaFolds/Transducers.jl/commit/246886f6307aebe4936e62119b5aa0e598de7428)
* Pull request: <https://github.com/JuliaFolds/Transducers.jl/pull/387> (Add KeepSomething; deprecate Keep)

# Judge result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmarks:
    - Target: 30 Jul 2020 - 17:59
    - Baseline: 30 Jul 2020 - 18:03
* Package commits:
    - Target: 4d0f46
    - Baseline: d1995c
* Julia commits:
    - Target: 44fa15
    - Baseline: 44fa15
* Julia command flags:
    - Target: None
    - Baseline: None
* Environment variables:
    - Target: `OMP_NUM_THREADS => 1` `JULIA_NUM_THREADS => 1`
    - Baseline: `OMP_NUM_THREADS => 1` `JULIA_NUM_THREADS => 1`

## Results
A ratio greater than `1.0` denotes a possible regression (marked with :x:), while a ratio less
than `1.0` denotes a possible improvement (marked with :white_check_mark:). Only significant results - results
that indicate possible regressions or improvements - are shown below (thus, an empty table means that all
benchmark results remained invariant between builds).

| ID                                       | time ratio                   | memory ratio                 |
|------------------------------------------|------------------------------|------------------------------|
| `["dot", "man"]`                         | 0.94 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["filter_map_map!", "man"]`             | 0.89 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["findall", "xf-array"]`                |                   1.01 (5%)  | 0.97 (1%) :white_check_mark: |
| `["findall", "xf-iter"]`                 |                1.08 (5%) :x: |                   1.00 (1%)  |
| `["gemm", "fusedmul", "xf", "16"]`       | 0.91 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["gemm", "fusedmul", "xf", "2"]`        | 0.86 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["gemm", "fusedmul", "xf", "32"]`       | 0.89 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["gemm", "mul", "linalg", "32"]`        | 0.87 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["gemm", "mul", "linalg", "8"]`         | 0.68 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["gemm", "mul", "man", "false", "32"]`  |                1.07 (5%) :x: |                   1.00 (1%)  |
| `["gemm", "mul", "man", "false", "8"]`   |                1.07 (5%) :x: |                   1.00 (1%)  |
| `["gemm", "mul", "man", "ivdep", "8"]`   | 0.80 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["gemm", "mul", "man", "true", "8"]`    |                1.21 (5%) :x: |                   1.00 (1%)  |
| `["gemm", "mul", "xf", "false", "256"]`  | 0.95 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["gemm", "mul", "xf", "false", "32"]`   |                1.07 (5%) :x: |                   1.00 (1%)  |
| `["gemm", "mul", "xf", "false", "8"]`    | 0.80 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["gemm", "mul", "xf", "ivdep", "8"]`    |                1.17 (5%) :x: |                   1.00 (1%)  |
| `["gemm", "mul", "xf", "true", "8"]`     |                1.07 (5%) :x: |                   1.00 (1%)  |
| `["groupby", "sum", "sac"]`              | 0.93 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["groupby", "sum", "xf-with-init"]`     | 0.94 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["groupby", "sum", "xf-without-init"]`  | 0.93 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["missing_dot", "xf_nota"]`             |                1.05 (5%) :x: |                   1.00 (1%)  |
| `["overhead", "foldl"]`                  |                1.17 (5%) :x: |                   1.00 (1%)  |

## Benchmark Group List
Here's a list of all the benchmark groups executed by this job:

- `["append!!"]`
- `["cat"]`
- `["collect"]`
- `["dict"]`
- `["dot"]`
- `["filter_map_map!"]`
- `["filter_map_reduce"]`
- `["findall"]`
- `["gemm", "fusedmul", "blas"]`
- `["gemm", "fusedmul", "xf"]`
- `["gemm", "mul", "linalg"]`
- `["gemm", "mul", "man", "false"]`
- `["gemm", "mul", "man", "ivdep"]`
- `["gemm", "mul", "man", "true"]`
- `["gemm", "mul", "xf", "false"]`
- `["gemm", "mul", "xf", "ivdep"]`
- `["gemm", "mul", "xf", "true"]`
- `["groupby", "sum"]`
- `["mapcat_eduction"]`
- `["missing_argmax"]`
- `["missing_dot"]`
- `["overhead"]`
- `["partition_by"]`
- `["set"]`

## Julia versioninfo

### Target
```
Julia Version 1.4.2
Commit 44fa15b150* (2020-05-23 18:35 UTC)
Platform Info:
  OS: Linux (x86_64-pc-linux-gnu)
      Ubuntu 18.04.4 LTS
  uname: Linux 5.3.0-1032-azure #33~18.04.1-Ubuntu SMP Fri Jun 26 15:01:15 UTC 2020 x86_64 x86_64
  CPU: Intel(R) Xeon(R) Platinum 8171M CPU @ 2.60GHz: 
              speed         user         nice          sys         idle          irq
       #1  2095 MHz      17971 s          0 s       1187 s      49986 s          0 s
       #2  2095 MHz      48626 s          0 s       2092 s      19395 s          0 s
       
  Memory: 6.764884948730469 GB (2882.41015625 MB free)
  Uptime: 715.0 sec
  Load Avg:  1.03564453125  0.98193359375  0.61962890625
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-8.0.1 (ORCJIT, skylake)
```

### Baseline
```
Julia Version 1.4.2
Commit 44fa15b150* (2020-05-23 18:35 UTC)
Platform Info:
  OS: Linux (x86_64-pc-linux-gnu)
      Ubuntu 18.04.4 LTS
  uname: Linux 5.3.0-1032-azure #33~18.04.1-Ubuntu SMP Fri Jun 26 15:01:15 UTC 2020 x86_64 x86_64
  CPU: Intel(R) Xeon(R) Platinum 8171M CPU @ 2.60GHz: 
              speed         user         nice          sys         idle          irq
       #1  2095 MHz      40057 s          0 s       1286 s      56177 s          0 s
       #2  2095 MHz      54885 s          0 s       2202 s      41361 s          0 s
       
  Memory: 6.764884948730469 GB (2765.34765625 MB free)
  Uptime: 1000.0 sec
  Load Avg:  1.0  1.0  0.73291015625
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-8.0.1 (ORCJIT, skylake)
```

---
# Target result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmark: 30 Jul 2020 - 17:59
* Package commit: 4d0f46
* Julia commit: 44fa15
* Julia command flags: None
* Environment variables: `OMP_NUM_THREADS => 1` `JULIA_NUM_THREADS => 1`

## Results
Below is a table of this job's results, obtained by running the benchmarks.
The values listed in the `ID` column have the structure `[parent_group, child_group, ..., key]`, and can be used to
index into the BaseBenchmarks suite to retrieve the corresponding benchmarks.
The percentages accompanying time and memory values in the below table are noise tolerances. The "true"
time/memory value for a given benchmark is expected to fall within this percentage of the reported value.
An empty cell means that the value was zero.

| ID                                       | time            | GC time | memory          | allocations |
|------------------------------------------|----------------:|--------:|----------------:|------------:|
| `["append!!", "eduction"]`               |  16.601 μs (5%) |         |  64.72 KiB (1%) |          18 |
| `["append!!", "xf"]`                     |  16.500 μs (5%) |         |  64.72 KiB (1%) |          18 |
| `["cat", "base"]`                        |   1.450 μs (5%) |         |                 |             |
| `["cat", "xf"]`                          |   1.650 μs (5%) |         |                 |             |
| `["collect", "filter-missing"]`          |  94.201 μs (5%) |         | 345.31 KiB (1%) |       10015 |
| `["collect", "identity-float"]`          |  72.101 μs (5%) |         | 569.16 KiB (1%) |       10015 |
| `["collect", "identity-union"]`          | 267.604 μs (5%) |         | 705.22 KiB (1%) |       16671 |
| `["dict", "base"]`                       |   3.882 ms (5%) |         |  92.91 KiB (1%) |          22 |
| `["dict", "xf"]`                         |   4.224 ms (5%) |         |  92.36 KiB (1%) |          21 |
| `["dot", "blas"]`                        |   1.030 μs (5%) |         |                 |             |
| `["dot", "man"]`                         |   1.000 μs (5%) |         |                 |             |
| `["dot", "rf"]`                          |   1.800 μs (5%) |         |                 |             |
| `["dot", "xf"]`                          |   1.856 μs (5%) |         |   64 bytes (1%) |           3 |
| `["filter_map_map!", "man"]`             |  56.900 μs (5%) |         |                 |             |
| `["filter_map_map!", "xf"]`              | 568.104 μs (5%) |         |  304 bytes (1%) |          17 |
| `["filter_map_reduce", "man"]`           | 192.202 μs (5%) |         |                 |             |
| `["filter_map_reduce", "xf"]`            | 191.902 μs (5%) |         |                 |             |
| `["findall", "base"]`                    | 732.310 μs (5%) |         |   2.00 MiB (1%) |          21 |
| `["findall", "xf-array"]`                | 700.109 μs (5%) |         |   2.95 MiB (1%) |       96625 |
| `["findall", "xf-iter"]`                 |   3.460 ms (5%) |         |   9.63 MiB (1%) |      299948 |
| `["gemm", "fusedmul", "blas", "16"]`     |   4.319 ms (5%) |         |                 |             |
| `["gemm", "fusedmul", "blas", "2"]`      |   3.315 ms (5%) |         |                 |             |
| `["gemm", "fusedmul", "blas", "32"]`     |   5.980 ms (5%) |         |                 |             |
| `["gemm", "fusedmul", "blas", "8"]`      |   3.448 ms (5%) |         |                 |             |
| `["gemm", "fusedmul", "xf", "16"]`       |   4.957 ms (5%) |         |  160 bytes (1%) |           6 |
| `["gemm", "fusedmul", "xf", "2"]`        | 577.105 μs (5%) |         |  160 bytes (1%) |           6 |
| `["gemm", "fusedmul", "xf", "32"]`       |   9.739 ms (5%) |         |  160 bytes (1%) |           6 |
| `["gemm", "fusedmul", "xf", "8"]`        |   2.554 ms (5%) |         |  160 bytes (1%) |           6 |
| `["gemm", "mul", "linalg", "256"]`       | 747.408 μs (5%) |         |                 |             |
| `["gemm", "mul", "linalg", "32"]`        |   2.511 μs (5%) |         |                 |             |
| `["gemm", "mul", "linalg", "8"]`         | 204.706 ns (5%) |         |                 |             |
| `["gemm", "mul", "man", "false", "256"]` |   1.398 ms (5%) |         |                 |             |
| `["gemm", "mul", "man", "false", "32"]`  |   3.950 μs (5%) |         |                 |             |
| `["gemm", "mul", "man", "false", "8"]`   | 320.851 ns (5%) |         |                 |             |
| `["gemm", "mul", "man", "ivdep", "256"]` |   1.455 ms (5%) |         |                 |             |
| `["gemm", "mul", "man", "ivdep", "32"]`  |   3.263 μs (5%) |         |                 |             |
| `["gemm", "mul", "man", "ivdep", "8"]`   | 319.574 ns (5%) |         |                 |             |
| `["gemm", "mul", "man", "true", "256"]`  |   1.402 ms (5%) |         |                 |             |
| `["gemm", "mul", "man", "true", "32"]`   |   3.943 μs (5%) |         |                 |             |
| `["gemm", "mul", "man", "true", "8"]`    | 363.158 ns (5%) |         |                 |             |
| `["gemm", "mul", "xf", "false", "256"]`  |   1.401 ms (5%) |         |   48 bytes (1%) |           2 |
| `["gemm", "mul", "xf", "false", "32"]`   |   3.957 μs (5%) |         |   48 bytes (1%) |           2 |
| `["gemm", "mul", "xf", "false", "8"]`    | 321.429 ns (5%) |         |   48 bytes (1%) |           2 |
| `["gemm", "mul", "xf", "ivdep", "256"]`  |   1.436 ms (5%) |         |   48 bytes (1%) |           2 |
| `["gemm", "mul", "xf", "ivdep", "32"]`   |   3.150 μs (5%) |         |   48 bytes (1%) |           2 |
| `["gemm", "mul", "xf", "ivdep", "8"]`    | 351.643 ns (5%) |         |   48 bytes (1%) |           2 |
| `["gemm", "mul", "xf", "true", "256"]`   |   1.405 ms (5%) |         |   48 bytes (1%) |           2 |
| `["gemm", "mul", "xf", "true", "32"]`    |   4.029 μs (5%) |         |   48 bytes (1%) |           2 |
| `["gemm", "mul", "xf", "true", "8"]`     | 319.716 ns (5%) |         |   48 bytes (1%) |           2 |
| `["groupby", "sum", "sac"]`              | 209.501 μs (5%) |         | 313.14 KiB (1%) |       10007 |
| `["groupby", "sum", "xf-with-init"]`     | 155.501 μs (5%) |         | 157.44 KiB (1%) |       10008 |
| `["groupby", "sum", "xf-without-init"]`  | 153.501 μs (5%) |         | 157.44 KiB (1%) |       10008 |
| `["mapcat_eduction", "base"]`            |   1.560 μs (5%) |         |                 |             |
| `["mapcat_eduction", "xf-eduction"]`     |   1.600 μs (5%) |         |                 |             |
| `["mapcat_eduction", "xf-xf"]`           |   1.600 μs (5%) |         |                 |             |
| `["missing_argmax", "man"]`              |   2.233 μs (5%) |         |   32 bytes (1%) |           1 |
| `["missing_argmax", "rf"]`               |   2.178 μs (5%) |         |   32 bytes (1%) |           1 |
| `["missing_argmax", "xf"]`               |   2.078 μs (5%) |         |   32 bytes (1%) |           1 |
| `["missing_dot", "equiv"]`               |   1.220 μs (5%) |         |   16 bytes (1%) |           1 |
| `["missing_dot", "man"]`                 |   1.130 μs (5%) |         |   16 bytes (1%) |           1 |
| `["missing_dot", "naive"]`               |   3.957 μs (5%) |         |   16 bytes (1%) |           1 |
| `["missing_dot", "rf"]`                  |   1.140 μs (5%) |         |   16 bytes (1%) |           1 |
| `["missing_dot", "rf_nota"]`             |   1.220 μs (5%) |         |   16 bytes (1%) |           1 |
| `["missing_dot", "xf"]`                  | 172.202 μs (5%) |         |  71.95 KiB (1%) |        3735 |
| `["missing_dot", "xf_nota"]`             | 175.602 μs (5%) |         |  71.91 KiB (1%) |        3732 |
| `["overhead", "foldl"]`                  |   4.200 ns (5%) |         |                 |             |
| `["overhead", "reduce_basecase"]`        | 152.228 ns (5%) |         |  416 bytes (1%) |           7 |
| `["partition_by", "man"]`                |   1.822 ms (5%) |         |  352 bytes (1%) |           4 |
| `["partition_by", "xf"]`                 |   2.995 ms (5%) |         |   6.10 MiB (1%) |      200007 |
| `["set", "base"]`                        |   4.760 ms (5%) |         |  49.58 KiB (1%) |          18 |
| `["set", "xf"]`                          |   4.367 ms (5%) |         |  49.63 KiB (1%) |          21 |

## Benchmark Group List
Here's a list of all the benchmark groups executed by this job:

- `["append!!"]`
- `["cat"]`
- `["collect"]`
- `["dict"]`
- `["dot"]`
- `["filter_map_map!"]`
- `["filter_map_reduce"]`
- `["findall"]`
- `["gemm", "fusedmul", "blas"]`
- `["gemm", "fusedmul", "xf"]`
- `["gemm", "mul", "linalg"]`
- `["gemm", "mul", "man", "false"]`
- `["gemm", "mul", "man", "ivdep"]`
- `["gemm", "mul", "man", "true"]`
- `["gemm", "mul", "xf", "false"]`
- `["gemm", "mul", "xf", "ivdep"]`
- `["gemm", "mul", "xf", "true"]`
- `["groupby", "sum"]`
- `["mapcat_eduction"]`
- `["missing_argmax"]`
- `["missing_dot"]`
- `["overhead"]`
- `["partition_by"]`
- `["set"]`

## Julia versioninfo
```
Julia Version 1.4.2
Commit 44fa15b150* (2020-05-23 18:35 UTC)
Platform Info:
  OS: Linux (x86_64-pc-linux-gnu)
      Ubuntu 18.04.4 LTS
  uname: Linux 5.3.0-1032-azure #33~18.04.1-Ubuntu SMP Fri Jun 26 15:01:15 UTC 2020 x86_64 x86_64
  CPU: Intel(R) Xeon(R) Platinum 8171M CPU @ 2.60GHz: 
              speed         user         nice          sys         idle          irq
       #1  2095 MHz      17971 s          0 s       1187 s      49986 s          0 s
       #2  2095 MHz      48626 s          0 s       2092 s      19395 s          0 s
       
  Memory: 6.764884948730469 GB (2882.41015625 MB free)
  Uptime: 715.0 sec
  Load Avg:  1.03564453125  0.98193359375  0.61962890625
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-8.0.1 (ORCJIT, skylake)
```

---
# Baseline result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmark: 30 Jul 2020 - 18:3
* Package commit: d1995c
* Julia commit: 44fa15
* Julia command flags: None
* Environment variables: `OMP_NUM_THREADS => 1` `JULIA_NUM_THREADS => 1`

## Results
Below is a table of this job's results, obtained by running the benchmarks.
The values listed in the `ID` column have the structure `[parent_group, child_group, ..., key]`, and can be used to
index into the BaseBenchmarks suite to retrieve the corresponding benchmarks.
The percentages accompanying time and memory values in the below table are noise tolerances. The "true"
time/memory value for a given benchmark is expected to fall within this percentage of the reported value.
An empty cell means that the value was zero.

| ID                                       | time            | GC time | memory          | allocations |
|------------------------------------------|----------------:|--------:|----------------:|------------:|
| `["append!!", "eduction"]`               |  16.000 μs (5%) |         |  64.72 KiB (1%) |          18 |
| `["append!!", "xf"]`                     |  16.201 μs (5%) |         |  64.72 KiB (1%) |          18 |
| `["cat", "base"]`                        |   1.450 μs (5%) |         |                 |             |
| `["cat", "xf"]`                          |   1.650 μs (5%) |         |                 |             |
| `["collect", "filter-missing"]`          |  92.801 μs (5%) |         | 345.31 KiB (1%) |       10015 |
| `["collect", "identity-float"]`          |  73.200 μs (5%) |         | 569.16 KiB (1%) |       10015 |
| `["collect", "identity-union"]`          | 266.502 μs (5%) |         | 705.56 KiB (1%) |       16693 |
| `["dict", "base"]`                       |   4.022 ms (5%) |         |  92.91 KiB (1%) |          22 |
| `["dict", "xf"]`                         |   4.050 ms (5%) |         |  92.36 KiB (1%) |          21 |
| `["dot", "blas"]`                        |   1.080 μs (5%) |         |                 |             |
| `["dot", "man"]`                         |   1.060 μs (5%) |         |                 |             |
| `["dot", "rf"]`                          |   1.811 μs (5%) |         |                 |             |
| `["dot", "xf"]`                          |   1.867 μs (5%) |         |   64 bytes (1%) |           3 |
| `["filter_map_map!", "man"]`             |  63.901 μs (5%) |         |                 |             |
| `["filter_map_map!", "xf"]`              | 567.004 μs (5%) |         |  304 bytes (1%) |          17 |
| `["filter_map_reduce", "man"]`           | 191.702 μs (5%) |         |                 |             |
| `["filter_map_reduce", "xf"]`            | 192.201 μs (5%) |         |                 |             |
| `["findall", "base"]`                    | 702.804 μs (5%) |         |   2.00 MiB (1%) |          21 |
| `["findall", "xf-array"]`                | 695.505 μs (5%) |         |   3.05 MiB (1%) |       99776 |
| `["findall", "xf-iter"]`                 |   3.198 ms (5%) |         |   9.63 MiB (1%) |      299915 |
| `["gemm", "fusedmul", "blas", "16"]`     |   4.381 ms (5%) |         |                 |             |
| `["gemm", "fusedmul", "blas", "2"]`      |   3.313 ms (5%) |         |                 |             |
| `["gemm", "fusedmul", "blas", "32"]`     |   6.045 ms (5%) |         |                 |             |
| `["gemm", "fusedmul", "blas", "8"]`      |   3.452 ms (5%) |         |                 |             |
| `["gemm", "fusedmul", "xf", "16"]`       |   5.450 ms (5%) |         |  160 bytes (1%) |           6 |
| `["gemm", "fusedmul", "xf", "2"]`        | 674.204 μs (5%) |         |  160 bytes (1%) |           6 |
| `["gemm", "fusedmul", "xf", "32"]`       |  10.948 ms (5%) |         |  160 bytes (1%) |           6 |
| `["gemm", "fusedmul", "xf", "8"]`        |   2.571 ms (5%) |         |  160 bytes (1%) |           6 |
| `["gemm", "mul", "linalg", "256"]`       | 748.204 μs (5%) |         |                 |             |
| `["gemm", "mul", "linalg", "32"]`        |   2.900 μs (5%) |         |                 |             |
| `["gemm", "mul", "linalg", "8"]`         | 300.000 ns (5%) |         |                 |             |
| `["gemm", "mul", "man", "false", "256"]` |   1.469 ms (5%) |         |                 |             |
| `["gemm", "mul", "man", "false", "32"]`  |   3.700 μs (5%) |         |                 |             |
| `["gemm", "mul", "man", "false", "8"]`   | 300.000 ns (5%) |         |                 |             |
| `["gemm", "mul", "man", "ivdep", "256"]` |   1.464 ms (5%) |         |                 |             |
| `["gemm", "mul", "man", "ivdep", "32"]`  |   3.300 μs (5%) |         |                 |             |
| `["gemm", "mul", "man", "ivdep", "8"]`   | 400.000 ns (5%) |         |                 |             |
| `["gemm", "mul", "man", "true", "256"]`  |   1.465 ms (5%) |         |                 |             |
| `["gemm", "mul", "man", "true", "32"]`   |   3.800 μs (5%) |         |                 |             |
| `["gemm", "mul", "man", "true", "8"]`    | 300.000 ns (5%) |         |                 |             |
| `["gemm", "mul", "xf", "false", "256"]`  |   1.478 ms (5%) |         |   48 bytes (1%) |           2 |
| `["gemm", "mul", "xf", "false", "32"]`   |   3.700 μs (5%) |         |   48 bytes (1%) |           2 |
| `["gemm", "mul", "xf", "false", "8"]`    | 400.000 ns (5%) |         |   48 bytes (1%) |           2 |
| `["gemm", "mul", "xf", "ivdep", "256"]`  |   1.468 ms (5%) |         |   48 bytes (1%) |           2 |
| `["gemm", "mul", "xf", "ivdep", "32"]`   |   3.200 μs (5%) |         |   48 bytes (1%) |           2 |
| `["gemm", "mul", "xf", "ivdep", "8"]`    | 300.000 ns (5%) |         |   48 bytes (1%) |           2 |
| `["gemm", "mul", "xf", "true", "256"]`   |   1.472 ms (5%) |         |   48 bytes (1%) |           2 |
| `["gemm", "mul", "xf", "true", "32"]`    |   3.900 μs (5%) |         |   48 bytes (1%) |           2 |
| `["gemm", "mul", "xf", "true", "8"]`     | 300.000 ns (5%) |         |   48 bytes (1%) |           2 |
| `["groupby", "sum", "sac"]`              | 225.504 μs (5%) |         | 313.14 KiB (1%) |       10007 |
| `["groupby", "sum", "xf-with-init"]`     | 165.102 μs (5%) |         | 157.44 KiB (1%) |       10008 |
| `["groupby", "sum", "xf-without-init"]`  | 165.702 μs (5%) |         | 157.44 KiB (1%) |       10008 |
| `["mapcat_eduction", "base"]`            |   1.550 μs (5%) |         |                 |             |
| `["mapcat_eduction", "xf-eduction"]`     |   1.600 μs (5%) |         |                 |             |
| `["mapcat_eduction", "xf-xf"]`           |   1.600 μs (5%) |         |                 |             |
| `["missing_argmax", "man"]`              |   2.233 μs (5%) |         |   32 bytes (1%) |           1 |
| `["missing_argmax", "rf"]`               |   2.100 μs (5%) |         |   32 bytes (1%) |           1 |
| `["missing_argmax", "xf"]`               |   2.111 μs (5%) |         |   32 bytes (1%) |           1 |
| `["missing_dot", "equiv"]`               |   1.200 μs (5%) |         |   16 bytes (1%) |           1 |
| `["missing_dot", "man"]`                 |   1.130 μs (5%) |         |   16 bytes (1%) |           1 |
| `["missing_dot", "naive"]`               |   3.943 μs (5%) |         |   16 bytes (1%) |           1 |
| `["missing_dot", "rf"]`                  |   1.140 μs (5%) |         |   16 bytes (1%) |           1 |
| `["missing_dot", "rf_nota"]`             |   1.240 μs (5%) |         |   16 bytes (1%) |           1 |
| `["missing_dot", "xf"]`                  | 167.401 μs (5%) |         |  72.11 KiB (1%) |        3742 |
| `["missing_dot", "xf_nota"]`             | 166.701 μs (5%) |         |  71.98 KiB (1%) |        3734 |
| `["overhead", "foldl"]`                  |   3.600 ns (5%) |         |                 |             |
| `["overhead", "reduce_basecase"]`        | 152.901 ns (5%) |         |  416 bytes (1%) |           7 |
| `["partition_by", "man"]`                |   1.844 ms (5%) |         |  352 bytes (1%) |           4 |
| `["partition_by", "xf"]`                 |   2.949 ms (5%) |         |   6.10 MiB (1%) |      200007 |
| `["set", "base"]`                        |   4.628 ms (5%) |         |  49.58 KiB (1%) |          18 |
| `["set", "xf"]`                          |   4.292 ms (5%) |         |  49.63 KiB (1%) |          21 |

## Benchmark Group List
Here's a list of all the benchmark groups executed by this job:

- `["append!!"]`
- `["cat"]`
- `["collect"]`
- `["dict"]`
- `["dot"]`
- `["filter_map_map!"]`
- `["filter_map_reduce"]`
- `["findall"]`
- `["gemm", "fusedmul", "blas"]`
- `["gemm", "fusedmul", "xf"]`
- `["gemm", "mul", "linalg"]`
- `["gemm", "mul", "man", "false"]`
- `["gemm", "mul", "man", "ivdep"]`
- `["gemm", "mul", "man", "true"]`
- `["gemm", "mul", "xf", "false"]`
- `["gemm", "mul", "xf", "ivdep"]`
- `["gemm", "mul", "xf", "true"]`
- `["groupby", "sum"]`
- `["mapcat_eduction"]`
- `["missing_argmax"]`
- `["missing_dot"]`
- `["overhead"]`
- `["partition_by"]`
- `["set"]`

## Julia versioninfo
```
Julia Version 1.4.2
Commit 44fa15b150* (2020-05-23 18:35 UTC)
Platform Info:
  OS: Linux (x86_64-pc-linux-gnu)
      Ubuntu 18.04.4 LTS
  uname: Linux 5.3.0-1032-azure #33~18.04.1-Ubuntu SMP Fri Jun 26 15:01:15 UTC 2020 x86_64 x86_64
  CPU: Intel(R) Xeon(R) Platinum 8171M CPU @ 2.60GHz: 
              speed         user         nice          sys         idle          irq
       #1  2095 MHz      40057 s          0 s       1286 s      56177 s          0 s
       #2  2095 MHz      54885 s          0 s       2202 s      41361 s          0 s
       
  Memory: 6.764884948730469 GB (2765.34765625 MB free)
  Uptime: 1000.0 sec
  Load Avg:  1.0  1.0  0.73291015625
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-8.0.1 (ORCJIT, skylake)
```

---
# Runtime information
| Runtime Info | |
|:--|:--|
| BLAS #threads | 2 |
| `BLAS.vendor()` | `openblas64` |
| `Sys.CPU_THREADS` | 2 |

`lscpu` output:

    Architecture:        x86_64
    CPU op-mode(s):      32-bit, 64-bit
    Byte Order:          Little Endian
    CPU(s):              2
    On-line CPU(s) list: 0,1
    Thread(s) per core:  1
    Core(s) per socket:  2
    Socket(s):           1
    NUMA node(s):        1
    Vendor ID:           GenuineIntel
    CPU family:          6
    Model:               85
    Model name:          Intel(R) Xeon(R) Platinum 8171M CPU @ 2.60GHz
    Stepping:            4
    CPU MHz:             2095.075
    BogoMIPS:            4190.15
    Hypervisor vendor:   Microsoft
    Virtualization type: full
    L1d cache:           32K
    L1i cache:           32K
    L2 cache:            1024K
    L3 cache:            36608K
    NUMA node0 CPU(s):   0,1
    Flags:               fpu vme de pse tsc msr pae mce cx8 apic sep mtrr pge mca cmov pat pse36 clflush mmx fxsr sse sse2 ss ht syscall nx pdpe1gb rdtscp lm constant_tsc rep_good nopl xtopology cpuid pni pclmulqdq ssse3 fma cx16 pcid sse4_1 sse4_2 movbe popcnt aes xsave avx f16c rdrand hypervisor lahf_lm abm 3dnowprefetch invpcid_single pti fsgsbase bmi1 hle avx2 smep bmi2 erms invpcid rtm mpx avx512f avx512dq rdseed adx smap clflushopt avx512cd avx512bw avx512vl xsaveopt xsavec xsaves
    

| Cpu Property       | Value                                                   |
|:------------------ |:------------------------------------------------------- |
| Brand              | Intel(R) Xeon(R) Platinum 8171M CPU @ 2.60GHz           |
| Vendor             | :Intel                                                  |
| Architecture       | :Skylake                                                |
| Model              | Family: 0x06, Model: 0x55, Stepping: 0x04, Type: 0x00   |
| Cores              | 2 physical cores, 2 logical cores (on executing CPU)    |
|                    | No Hyperthreading detected                              |
| Clock Frequencies  | Not supported by CPU                                    |
| Data Cache         | Level 1:3 : (32, 1024, 36608) kbytes                    |
|                    | 64 byte cache line size                                 |
| Address Size       | 48 bits virtual, 44 bits physical                       |
| SIMD               | 512 bit = 64 byte max. SIMD vector size                 |
| Time Stamp Counter | TSC is accessible via `rdtsc`                           |
|                    | TSC increased at every clock cycle (non-invariant TSC)  |
| Perf. Monitoring   | Performance Monitoring Counters (PMC) are not supported |
| Hypervisor         | Yes, Microsoft                                          |

