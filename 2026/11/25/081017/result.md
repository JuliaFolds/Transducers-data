# Benchmark result

* Pull request commit: [`9148e2b519636e9d6491eaaa55338e9de9938b8c`](https://github.com/JuliaFolds/Transducers.jl/commit/9148e2b519636e9d6491eaaa55338e9de9938b8c)
* Pull request: <https://github.com/JuliaFolds/Transducers.jl/pull/243> (Update */Manifest.toml)

# Judge result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmarks:
    - Target: 25 Nov 2026 - 08:03
    - Baseline: 25 Nov 2026 - 08:07
* Package commits:
    - Target: e85187c
    - Baseline: 2a51f8d
* Julia commits:
    - Target: 742b9ab
    - Baseline: 742b9ab
* Julia command flags:
    - Target: None
    - Baseline: None
* Environment variables:
    - Target: `OMP_NUM_THREADS => 1` `JULIA_NUM_THREADS => 1`
    - Baseline: `OMP_NUM_THREADS => 1` `JULIA_NUM_THREADS => 1`

## Results
A ratio greater than `1.0` denotes a possible regression (marked with :x:), while a ratio less
than `1.0` denotes a possible improvement (marked with :white_check_mark:). Brackets display [tolerances](https://juliaci.github.io/BenchmarkTools.jl/stable/manual/#Benchmark-Parameters) for the benchmark estimates. Only significant results - results
that indicate possible regressions or improvements - are shown below (thus, an empty table means that all
benchmark results remained invariant between builds).

| ID                                                             | time ratio                   | memory ratio                 |
|----------------------------------------------------------------|------------------------------|------------------------------|
| `["cartesian", "copyto!", "man"]`                              | 0.88 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["cartesian", "copyto!", "xf"]`                               |                1.15 (5%) :x: |                   1.00 (1%)  |
| `["collect", "identity-union"]`                                |                1.05 (5%) :x: |                   1.00 (1%)  |
| `["filter_sum", "1000", "RandomFloats", "withinit", "naive"]`  | 0.76 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["filter_sum", "10000", "RandomFloats", "noinit", "naive"]`   |                1.11 (5%) :x: |                   1.00 (1%)  |
| `["filter_sum", "10000", "RandomFloats", "withinit", "naive"]` | 0.73 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["findall", "xf-array"]`                                      |                1.05 (5%) :x: |                   1.00 (1%)  |
| `["findall", "xf-iter"]`                                       | 0.92 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["gemm", "fusedmul", "xf", "32"]`                             | 0.94 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["gemm", "fusedmul", "xf", "8"]`                              | 0.88 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["gemm", "mul", "linalg", "8"]`                               | 0.87 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["gemm", "mul", "man", "ivdep", "8"]`                         | 0.93 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["gemm", "mul", "man", "true", "8"]`                          |                1.08 (5%) :x: |                   1.00 (1%)  |
| `["gemm", "mul", "xf", "false", "32"]`                         |                1.06 (5%) :x: |                   1.00 (1%)  |
| `["gemm", "mul", "xf", "false", "8"]`                          | 0.95 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["gemm", "mul", "xf", "ivdep", "8"]`                          | 0.94 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["groupby", "sum", "sac"]`                                    | 0.02 (5%) :white_check_mark: | 0.12 (1%) :white_check_mark: |
| `["teerf_filter", "noinit"]`                                   | 0.93 (5%) :white_check_mark: |                   1.00 (1%)  |

## Benchmark Group List
Here's a list of all the benchmark groups executed by this job:

- `["append!!"]`
- `["cartesian", "copyto!"]`
- `["cat"]`
- `["collect"]`
- `["dict"]`
- `["dot"]`
- `["filter_map_map!"]`
- `["filter_map_reduce"]`
- `["filter_sum", "1000", "RandomFloats", "noinit"]`
- `["filter_sum", "1000", "RandomFloats", "withinit"]`
- `["filter_sum", "1000", "UnitRange", "noinit"]`
- `["filter_sum", "1000", "UnitRange", "withinit"]`
- `["filter_sum", "10000", "RandomFloats", "noinit"]`
- `["filter_sum", "10000", "RandomFloats", "withinit"]`
- `["filter_sum", "10000", "UnitRange", "noinit"]`
- `["filter_sum", "10000", "UnitRange", "withinit"]`
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
- `["sum_transpose", "30", "noinit"]`
- `["sum_transpose", "30", "withinit"]`
- `["teerf_filter"]`

## Julia versioninfo

### Target
```
Julia Version 1.7.3
Commit 742b9abb4d (2022-05-06 12:58 UTC)
Platform Info:
  OS: Linux (x86_64-pc-linux-gnu)
      Ubuntu 26.04.1 LTS
  uname: Linux 7.0.0-1016-aws #17-Ubuntu SMP PREEMPT Mon Oct 19 17:36:33 UTC 2026 x86_64 unknown
  CPU: Intel(R) Xeon(R) 6975P-C: 
              speed         user         nice          sys         idle          irq
       #1  3900 MHz        827 s          0 s         48 s       5507 s          0 s
       #2  2918 MHz       1825 s          0 s         82 s       4496 s          0 s
       #3  3998 MHz       1071 s          0 s         75 s       5189 s          0 s
       #4  3026 MHz       1913 s          0 s         61 s       4400 s          0 s
       
  Memory: 15.332740783691406 GB (12855.19921875 MB free)
  Uptime: 652.99 sec
  Load Avg:  1.0  0.92  0.55
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-12.0.1 (ORCJIT, icelake-client)
```

### Baseline
```
Julia Version 1.7.3
Commit 742b9abb4d (2022-05-06 12:58 UTC)
Platform Info:
  OS: Linux (x86_64-pc-linux-gnu)
      Ubuntu 26.04.1 LTS
  uname: Linux 7.0.0-1016-aws #17-Ubuntu SMP PREEMPT Mon Oct 19 17:36:33 UTC 2026 x86_64 unknown
  CPU: Intel(R) Xeon(R) 6975P-C: 
              speed         user         nice          sys         idle          irq
       #1  3837 MHz       1061 s          0 s         66 s       7519 s          0 s
       #2  3240 MHz       2153 s          0 s         96 s       6419 s          0 s
       #3  3899 MHz       2383 s          0 s        106 s       6113 s          0 s
       #4  3921 MHz       2326 s          0 s         76 s       6236 s          0 s
       
  Memory: 15.332740783691406 GB (12765.7265625 MB free)
  Uptime: 879.75 sec
  Load Avg:  1.0  0.98  0.66
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-12.0.1 (ORCJIT, icelake-client)
```

---
# Target result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmark: 25 Nov 2026 - 08:03
* Package commit: e85187c
* Julia commit: 742b9ab
* Julia command flags: None
* Environment variables: `OMP_NUM_THREADS => 1` `JULIA_NUM_THREADS => 1`

## Results
Below is a table of this job's results, obtained by running the benchmarks.
The values listed in the `ID` column have the structure `[parent_group, child_group, ..., key]`, and can be used to
index into the BaseBenchmarks suite to retrieve the corresponding benchmarks.
The percentages accompanying time and memory values in the below table are noise tolerances. The "true"
time/memory value for a given benchmark is expected to fall within this percentage of the reported value.
An empty cell means that the value was zero.

| ID                                                             | time            | GC time | memory          | allocations |
|----------------------------------------------------------------|----------------:|--------:|----------------:|------------:|
| `["append!!", "eduction"]`                                     |   8.879 μs (5%) |         |  53.98 KiB (1%) |           8 |
| `["append!!", "xf"]`                                           |   8.726 μs (5%) |         |  53.98 KiB (1%) |           8 |
| `["cartesian", "copyto!", "iter"]`                             |   1.129 μs (5%) |         |                 |             |
| `["cartesian", "copyto!", "man"]`                              |   1.129 μs (5%) |         |                 |             |
| `["cartesian", "copyto!", "xf"]`                               |   1.299 μs (5%) |         |                 |             |
| `["cat", "base"]`                                              | 958.810 ns (5%) |         |                 |             |
| `["cat", "xf"]`                                                | 965.895 ns (5%) |         |                 |             |
| `["collect", "filter-missing"]`                                | 406.015 ns (5%) |         |   9.94 KiB (1%) |           1 |
| `["collect", "identity-float"]`                                |   2.818 μs (5%) |         |  78.17 KiB (1%) |           2 |
| `["collect", "identity-union"]`                                |  84.660 μs (5%) |         | 400.53 KiB (1%) |       10003 |
| `["dict", "base"]`                                             |   1.834 ms (5%) |         |  92.45 KiB (1%) |          22 |
| `["dict", "xf"]`                                               |   1.917 ms (5%) |         |  91.95 KiB (1%) |          18 |
| `["dot", "blas"]`                                              |   1.524 μs (5%) |         |                 |             |
| `["dot", "man"]`                                               |   1.016 μs (5%) |         |                 |             |
| `["dot", "rf"]`                                                |   1.764 μs (5%) |         |                 |             |
| `["dot", "xf"]`                                                |   1.763 μs (5%) |         |                 |             |
| `["filter_map_map!", "man"]`                                   |  15.866 μs (5%) |         |                 |             |
| `["filter_map_map!", "xf"]`                                    |  18.207 μs (5%) |         |                 |             |
| `["filter_map_reduce", "man"]`                                 | 141.494 μs (5%) |         |                 |             |
| `["filter_map_reduce", "xf"]`                                  | 141.497 μs (5%) |         |                 |             |
| `["filter_sum", "1000", "RandomFloats", "noinit", "base"]`     |   2.073 μs (5%) |         |                 |             |
| `["filter_sum", "1000", "RandomFloats", "noinit", "naive"]`    | 957.200 ns (5%) |         |                 |             |
| `["filter_sum", "1000", "RandomFloats", "noinit", "xf"]`       |   1.019 μs (5%) |         |                 |             |
| `["filter_sum", "1000", "RandomFloats", "withinit", "base"]`   |   1.026 μs (5%) |         |                 |             |
| `["filter_sum", "1000", "RandomFloats", "withinit", "naive"]`  | 390.871 ns (5%) |         |                 |             |
| `["filter_sum", "1000", "RandomFloats", "withinit", "xf"]`     |   1.026 μs (5%) |         |                 |             |
| `["filter_sum", "1000", "UnitRange", "noinit", "base"]`        | 472.546 ns (5%) |         |                 |             |
| `["filter_sum", "1000", "UnitRange", "noinit", "naive"]`       | 459.883 ns (5%) |         |                 |             |
| `["filter_sum", "1000", "UnitRange", "noinit", "xf"]`          | 138.027 ns (5%) |         |                 |             |
| `["filter_sum", "1000", "UnitRange", "withinit", "base"]`      | 104.362 ns (5%) |         |                 |             |
| `["filter_sum", "1000", "UnitRange", "withinit", "naive"]`     | 270.016 ns (5%) |         |                 |             |
| `["filter_sum", "1000", "UnitRange", "withinit", "xf"]`        | 103.667 ns (5%) |         |                 |             |
| `["filter_sum", "10000", "RandomFloats", "noinit", "base"]`    |  20.730 μs (5%) |         |                 |             |
| `["filter_sum", "10000", "RandomFloats", "noinit", "naive"]`   |   9.780 μs (5%) |         |                 |             |
| `["filter_sum", "10000", "RandomFloats", "noinit", "xf"]`      |  10.603 μs (5%) |         |                 |             |
| `["filter_sum", "10000", "RandomFloats", "withinit", "base"]`  |  10.589 μs (5%) |         |                 |             |
| `["filter_sum", "10000", "RandomFloats", "withinit", "naive"]` |   4.516 μs (5%) |         |                 |             |
| `["filter_sum", "10000", "RandomFloats", "withinit", "xf"]`    |  10.606 μs (5%) |         |                 |             |
| `["filter_sum", "10000", "UnitRange", "noinit", "base"]`       |   4.628 μs (5%) |         |                 |             |
| `["filter_sum", "10000", "UnitRange", "noinit", "naive"]`      |   4.499 μs (5%) |         |                 |             |
| `["filter_sum", "10000", "UnitRange", "noinit", "xf"]`         |   1.365 μs (5%) |         |                 |             |
| `["filter_sum", "10000", "UnitRange", "withinit", "base"]`     | 989.667 ns (5%) |         |                 |             |
| `["filter_sum", "10000", "UnitRange", "withinit", "naive"]`    |   2.582 μs (5%) |         |                 |             |
| `["filter_sum", "10000", "UnitRange", "withinit", "xf"]`       | 988.917 ns (5%) |         |                 |             |
| `["findall", "base"]`                                          |  75.307 μs (5%) |         | 797.20 KiB (1%) |           8 |
| `["findall", "xf-array"]`                                      | 673.031 μs (5%) |         |   2.94 MiB (1%) |       96426 |
| `["findall", "xf-iter"]`                                       | 375.682 μs (5%) |         |   1.83 MiB (1%) |          14 |
| `["gemm", "fusedmul", "blas", "16"]`                           |   4.394 ms (5%) |         |                 |             |
| `["gemm", "fusedmul", "blas", "2"]`                            |   1.705 ms (5%) |         |                 |             |
| `["gemm", "fusedmul", "blas", "32"]`                           |   7.438 ms (5%) |         |                 |             |
| `["gemm", "fusedmul", "blas", "8"]`                            |   2.858 ms (5%) |         |                 |             |
| `["gemm", "fusedmul", "xf", "16"]`                             |   4.532 ms (5%) |         |  192 bytes (1%) |           4 |
| `["gemm", "fusedmul", "xf", "2"]`                              | 552.317 μs (5%) |         |  192 bytes (1%) |           4 |
| `["gemm", "fusedmul", "xf", "32"]`                             |   8.545 ms (5%) |         |  192 bytes (1%) |           4 |
| `["gemm", "fusedmul", "xf", "8"]`                              |   1.991 ms (5%) |         |  192 bytes (1%) |           4 |
| `["gemm", "mul", "linalg", "256"]`                             |   1.537 ms (5%) |         |                 |             |
| `["gemm", "mul", "linalg", "32"]`                              |   3.435 μs (5%) |         |                 |             |
| `["gemm", "mul", "linalg", "8"]`                               | 141.238 ns (5%) |         |                 |             |
| `["gemm", "mul", "man", "false", "256"]`                       |   1.440 ms (5%) |         |                 |             |
| `["gemm", "mul", "man", "false", "32"]`                        |   3.820 μs (5%) |         |                 |             |
| `["gemm", "mul", "man", "false", "8"]`                         | 262.858 ns (5%) |         |                 |             |
| `["gemm", "mul", "man", "ivdep", "256"]`                       |   1.374 ms (5%) |         |                 |             |
| `["gemm", "mul", "man", "ivdep", "32"]`                        |   3.305 μs (5%) |         |                 |             |
| `["gemm", "mul", "man", "ivdep", "8"]`                         | 233.599 ns (5%) |         |                 |             |
| `["gemm", "mul", "man", "true", "256"]`                        |   1.406 ms (5%) |         |                 |             |
| `["gemm", "mul", "man", "true", "32"]`                         |   3.559 μs (5%) |         |                 |             |
| `["gemm", "mul", "man", "true", "8"]`                          | 281.948 ns (5%) |         |                 |             |
| `["gemm", "mul", "xf", "false", "256"]`                        |   1.424 ms (5%) |         |   80 bytes (1%) |           3 |
| `["gemm", "mul", "xf", "false", "32"]`                         |   3.884 μs (5%) |         |   80 bytes (1%) |           3 |
| `["gemm", "mul", "xf", "false", "8"]`                          | 297.791 ns (5%) |         |   80 bytes (1%) |           3 |
| `["gemm", "mul", "xf", "ivdep", "256"]`                        |   1.368 ms (5%) |         |   80 bytes (1%) |           3 |
| `["gemm", "mul", "xf", "ivdep", "32"]`                         |   3.251 μs (5%) |         |   80 bytes (1%) |           3 |
| `["gemm", "mul", "xf", "ivdep", "8"]`                          | 270.500 ns (5%) |         |   80 bytes (1%) |           3 |
| `["gemm", "mul", "xf", "true", "256"]`                         |   1.395 ms (5%) |         |   80 bytes (1%) |           3 |
| `["gemm", "mul", "xf", "true", "32"]`                          |   3.684 μs (5%) |         |   80 bytes (1%) |           3 |
| `["gemm", "mul", "xf", "true", "8"]`                           | 284.309 ns (5%) |         |   80 bytes (1%) |           3 |
| `["groupby", "sum", "sac"]`                                    |  72.030 μs (5%) |         |   1.64 KiB (1%) |          11 |
| `["groupby", "sum", "xf-with-init"]`                           |  71.620 μs (5%) |         |   1.05 KiB (1%) |           9 |
| `["groupby", "sum", "xf-without-init"]`                        |  70.477 μs (5%) |         |   1.05 KiB (1%) |           9 |
| `["mapcat_eduction", "base"]`                                  |  30.207 μs (5%) |         |                 |             |
| `["mapcat_eduction", "xf-eduction"]`                           | 963.800 ns (5%) |         |                 |             |
| `["mapcat_eduction", "xf-xf"]`                                 | 963.650 ns (5%) |         |                 |             |
| `["missing_argmax", "man"]`                                    |   2.221 μs (5%) |         |                 |             |
| `["missing_argmax", "rf"]`                                     |   1.070 μs (5%) |         |                 |             |
| `["missing_argmax", "xf"]`                                     |   1.092 μs (5%) |         |   32 bytes (1%) |           1 |
| `["missing_dot", "equiv"]`                                     |   1.310 μs (5%) |         |   48 bytes (1%) |           3 |
| `["missing_dot", "man"]`                                       | 644.912 ns (5%) |         |   48 bytes (1%) |           3 |
| `["missing_dot", "naive"]`                                     |   1.758 μs (5%) |         |   48 bytes (1%) |           3 |
| `["missing_dot", "rf"]`                                        | 623.272 ns (5%) |         |   48 bytes (1%) |           3 |
| `["missing_dot", "rf_nota"]`                                   |   1.300 μs (5%) |         |   48 bytes (1%) |           3 |
| `["missing_dot", "xf"]`                                        |  45.365 μs (5%) |         |  72.23 KiB (1%) |        3746 |
| `["missing_dot", "xf_nota"]`                                   |  45.534 μs (5%) |         |  71.94 KiB (1%) |        3736 |
| `["overhead", "foldl"]`                                        |   2.068 ns (5%) |         |                 |             |
| `["overhead", "reduce_basecase"]`                              |  52.645 ns (5%) |         |   16 bytes (1%) |           1 |
| `["partition_by", "man"]`                                      |   1.540 ms (5%) |         |  480 bytes (1%) |           3 |
| `["partition_by", "xf"]`                                       |   1.578 ms (5%) |         |  592 bytes (1%) |           5 |
| `["set", "base"]`                                              |   1.852 ms (5%) |         |  49.14 KiB (1%) |          17 |
| `["set", "xf"]`                                                |   1.817 ms (5%) |         |  49.17 KiB (1%) |          19 |
| `["sum_transpose", "30", "noinit", "iter"]`                    |   1.601 μs (5%) |         |                 |             |
| `["sum_transpose", "30", "noinit", "man"]`                     |   2.401 μs (5%) |         |                 |             |
| `["sum_transpose", "30", "noinit", "xf"]`                      | 432.833 ns (5%) |         |                 |             |
| `["sum_transpose", "30", "withinit", "iter"]`                  | 852.569 ns (5%) |         |                 |             |
| `["sum_transpose", "30", "withinit", "man"]`                   | 437.061 ns (5%) |         |                 |             |
| `["sum_transpose", "30", "withinit", "xf"]`                    | 437.419 ns (5%) |         |                 |             |
| `["teerf_filter", "noinit"]`                                   | 228.176 ns (5%) |         |   80 bytes (1%) |           3 |
| `["teerf_filter", "withinit"]`                                 | 154.182 ns (5%) |         |                 |             |

## Benchmark Group List
Here's a list of all the benchmark groups executed by this job:

- `["append!!"]`
- `["cartesian", "copyto!"]`
- `["cat"]`
- `["collect"]`
- `["dict"]`
- `["dot"]`
- `["filter_map_map!"]`
- `["filter_map_reduce"]`
- `["filter_sum", "1000", "RandomFloats", "noinit"]`
- `["filter_sum", "1000", "RandomFloats", "withinit"]`
- `["filter_sum", "1000", "UnitRange", "noinit"]`
- `["filter_sum", "1000", "UnitRange", "withinit"]`
- `["filter_sum", "10000", "RandomFloats", "noinit"]`
- `["filter_sum", "10000", "RandomFloats", "withinit"]`
- `["filter_sum", "10000", "UnitRange", "noinit"]`
- `["filter_sum", "10000", "UnitRange", "withinit"]`
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
- `["sum_transpose", "30", "noinit"]`
- `["sum_transpose", "30", "withinit"]`
- `["teerf_filter"]`

## Julia versioninfo
```
Julia Version 1.7.3
Commit 742b9abb4d (2022-05-06 12:58 UTC)
Platform Info:
  OS: Linux (x86_64-pc-linux-gnu)
      Ubuntu 26.04.1 LTS
  uname: Linux 7.0.0-1016-aws #17-Ubuntu SMP PREEMPT Mon Oct 19 17:36:33 UTC 2026 x86_64 unknown
  CPU: Intel(R) Xeon(R) 6975P-C: 
              speed         user         nice          sys         idle          irq
       #1  3900 MHz        827 s          0 s         48 s       5507 s          0 s
       #2  2918 MHz       1825 s          0 s         82 s       4496 s          0 s
       #3  3998 MHz       1071 s          0 s         75 s       5189 s          0 s
       #4  3026 MHz       1913 s          0 s         61 s       4400 s          0 s
       
  Memory: 15.332740783691406 GB (12855.19921875 MB free)
  Uptime: 652.99 sec
  Load Avg:  1.0  0.92  0.55
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-12.0.1 (ORCJIT, icelake-client)
```

---
# Baseline result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmark: 25 Nov 2026 - 08:07
* Package commit: 2a51f8d
* Julia commit: 742b9ab
* Julia command flags: None
* Environment variables: `OMP_NUM_THREADS => 1` `JULIA_NUM_THREADS => 1`

## Results
Below is a table of this job's results, obtained by running the benchmarks.
The values listed in the `ID` column have the structure `[parent_group, child_group, ..., key]`, and can be used to
index into the BaseBenchmarks suite to retrieve the corresponding benchmarks.
The percentages accompanying time and memory values in the below table are noise tolerances. The "true"
time/memory value for a given benchmark is expected to fall within this percentage of the reported value.
An empty cell means that the value was zero.

| ID                                                             | time            | GC time | memory          | allocations |
|----------------------------------------------------------------|----------------:|--------:|----------------:|------------:|
| `["append!!", "eduction"]`                                     |   8.534 μs (5%) |         |  53.98 KiB (1%) |           8 |
| `["append!!", "xf"]`                                           |   8.527 μs (5%) |         |  53.98 KiB (1%) |           8 |
| `["cartesian", "copyto!", "iter"]`                             |   1.129 μs (5%) |         |                 |             |
| `["cartesian", "copyto!", "man"]`                              |   1.285 μs (5%) |         |                 |             |
| `["cartesian", "copyto!", "xf"]`                               |   1.129 μs (5%) |         |                 |             |
| `["cat", "base"]`                                              | 959.190 ns (5%) |         |                 |             |
| `["cat", "xf"]`                                                | 965.737 ns (5%) |         |                 |             |
| `["collect", "filter-missing"]`                                | 400.690 ns (5%) |         |   9.94 KiB (1%) |           1 |
| `["collect", "identity-float"]`                                |   2.780 μs (5%) |         |  78.17 KiB (1%) |           2 |
| `["collect", "identity-union"]`                                |  80.313 μs (5%) |         | 400.53 KiB (1%) |       10003 |
| `["dict", "base"]`                                             |   1.900 ms (5%) |         |  92.45 KiB (1%) |          22 |
| `["dict", "xf"]`                                               |   1.884 ms (5%) |         |  91.95 KiB (1%) |          18 |
| `["dot", "blas"]`                                              |   1.523 μs (5%) |         |                 |             |
| `["dot", "man"]`                                               |   1.017 μs (5%) |         |                 |             |
| `["dot", "rf"]`                                                |   1.762 μs (5%) |         |                 |             |
| `["dot", "xf"]`                                                |   1.753 μs (5%) |         |                 |             |
| `["filter_map_map!", "man"]`                                   |  15.873 μs (5%) |         |                 |             |
| `["filter_map_map!", "xf"]`                                    |  18.095 μs (5%) |         |                 |             |
| `["filter_map_reduce", "man"]`                                 | 141.509 μs (5%) |         |                 |             |
| `["filter_map_reduce", "xf"]`                                  | 141.148 μs (5%) |         |                 |             |
| `["filter_sum", "1000", "RandomFloats", "noinit", "base"]`     |   2.072 μs (5%) |         |                 |             |
| `["filter_sum", "1000", "RandomFloats", "noinit", "naive"]`    | 914.600 ns (5%) |         |                 |             |
| `["filter_sum", "1000", "RandomFloats", "noinit", "xf"]`       |   1.023 μs (5%) |         |                 |             |
| `["filter_sum", "1000", "RandomFloats", "withinit", "base"]`   |   1.025 μs (5%) |         |                 |             |
| `["filter_sum", "1000", "RandomFloats", "withinit", "naive"]`  | 513.356 ns (5%) |         |                 |             |
| `["filter_sum", "1000", "RandomFloats", "withinit", "xf"]`     |   1.026 μs (5%) |         |                 |             |
| `["filter_sum", "1000", "UnitRange", "noinit", "base"]`        | 472.872 ns (5%) |         |                 |             |
| `["filter_sum", "1000", "UnitRange", "noinit", "naive"]`       | 459.944 ns (5%) |         |                 |             |
| `["filter_sum", "1000", "UnitRange", "noinit", "xf"]`          | 138.611 ns (5%) |         |                 |             |
| `["filter_sum", "1000", "UnitRange", "withinit", "base"]`      | 100.860 ns (5%) |         |                 |             |
| `["filter_sum", "1000", "UnitRange", "withinit", "naive"]`     | 270.636 ns (5%) |         |                 |             |
| `["filter_sum", "1000", "UnitRange", "withinit", "xf"]`        | 104.064 ns (5%) |         |                 |             |
| `["filter_sum", "10000", "RandomFloats", "noinit", "base"]`    |  20.817 μs (5%) |         |                 |             |
| `["filter_sum", "10000", "RandomFloats", "noinit", "naive"]`   |   8.811 μs (5%) |         |                 |             |
| `["filter_sum", "10000", "RandomFloats", "noinit", "xf"]`      |  10.578 μs (5%) |         |                 |             |
| `["filter_sum", "10000", "RandomFloats", "withinit", "base"]`  |  10.605 μs (5%) |         |                 |             |
| `["filter_sum", "10000", "RandomFloats", "withinit", "naive"]` |   6.181 μs (5%) |         |                 |             |
| `["filter_sum", "10000", "RandomFloats", "withinit", "xf"]`    |  10.603 μs (5%) |         |                 |             |
| `["filter_sum", "10000", "UnitRange", "noinit", "base"]`       |   4.629 μs (5%) |         |                 |             |
| `["filter_sum", "10000", "UnitRange", "noinit", "naive"]`      |   4.500 μs (5%) |         |                 |             |
| `["filter_sum", "10000", "UnitRange", "noinit", "xf"]`         |   1.369 μs (5%) |         |                 |             |
| `["filter_sum", "10000", "UnitRange", "withinit", "base"]`     | 968.417 ns (5%) |         |                 |             |
| `["filter_sum", "10000", "UnitRange", "withinit", "naive"]`    |   2.580 μs (5%) |         |                 |             |
| `["filter_sum", "10000", "UnitRange", "withinit", "xf"]`       | 990.917 ns (5%) |         |                 |             |
| `["findall", "base"]`                                          |  75.068 μs (5%) |         | 797.20 KiB (1%) |           8 |
| `["findall", "xf-array"]`                                      | 640.877 μs (5%) |         |   2.94 MiB (1%) |       96426 |
| `["findall", "xf-iter"]`                                       | 409.409 μs (5%) |         |   1.83 MiB (1%) |          14 |
| `["gemm", "fusedmul", "blas", "16"]`                           |   4.399 ms (5%) |         |                 |             |
| `["gemm", "fusedmul", "blas", "2"]`                            |   1.719 ms (5%) |         |                 |             |
| `["gemm", "fusedmul", "blas", "32"]`                           |   7.436 ms (5%) |         |                 |             |
| `["gemm", "fusedmul", "blas", "8"]`                            |   2.854 ms (5%) |         |                 |             |
| `["gemm", "fusedmul", "xf", "16"]`                             |   4.526 ms (5%) |         |  192 bytes (1%) |           4 |
| `["gemm", "fusedmul", "xf", "2"]`                              | 551.273 μs (5%) |         |  192 bytes (1%) |           4 |
| `["gemm", "fusedmul", "xf", "32"]`                             |   9.080 ms (5%) |         |  192 bytes (1%) |           4 |
| `["gemm", "fusedmul", "xf", "8"]`                              |   2.260 ms (5%) |         |  192 bytes (1%) |           4 |
| `["gemm", "mul", "linalg", "256"]`                             |   1.541 ms (5%) |         |                 |             |
| `["gemm", "mul", "linalg", "32"]`                              |   3.459 μs (5%) |         |                 |             |
| `["gemm", "mul", "linalg", "8"]`                               | 162.000 ns (5%) |         |                 |             |
| `["gemm", "mul", "man", "false", "256"]`                       |   1.476 ms (5%) |         |                 |             |
| `["gemm", "mul", "man", "false", "32"]`                        |   3.705 μs (5%) |         |                 |             |
| `["gemm", "mul", "man", "false", "8"]`                         | 260.000 ns (5%) |         |                 |             |
| `["gemm", "mul", "man", "ivdep", "256"]`                       |   1.365 ms (5%) |         |                 |             |
| `["gemm", "mul", "man", "ivdep", "32"]`                        |   3.280 μs (5%) |         |                 |             |
| `["gemm", "mul", "man", "ivdep", "8"]`                         | 251.000 ns (5%) |         |                 |             |
| `["gemm", "mul", "man", "true", "256"]`                        |   1.397 ms (5%) |         |                 |             |
| `["gemm", "mul", "man", "true", "32"]`                         |   3.416 μs (5%) |         |                 |             |
| `["gemm", "mul", "man", "true", "8"]`                          | 260.000 ns (5%) |         |                 |             |
| `["gemm", "mul", "xf", "false", "256"]`                        |   1.422 ms (5%) |         |   80 bytes (1%) |           3 |
| `["gemm", "mul", "xf", "false", "32"]`                         |   3.665 μs (5%) |         |   80 bytes (1%) |           3 |
| `["gemm", "mul", "xf", "false", "8"]`                          | 314.000 ns (5%) |         |   80 bytes (1%) |           3 |
| `["gemm", "mul", "xf", "ivdep", "256"]`                        |   1.364 ms (5%) |         |   80 bytes (1%) |           3 |
| `["gemm", "mul", "xf", "ivdep", "32"]`                         |   3.295 μs (5%) |         |   80 bytes (1%) |           3 |
| `["gemm", "mul", "xf", "ivdep", "8"]`                          | 288.000 ns (5%) |         |   80 bytes (1%) |           3 |
| `["gemm", "mul", "xf", "true", "256"]`                         |   1.402 ms (5%) |         |   80 bytes (1%) |           3 |
| `["gemm", "mul", "xf", "true", "32"]`                          |   3.544 μs (5%) |         |   80 bytes (1%) |           3 |
| `["gemm", "mul", "xf", "true", "8"]`                           | 294.000 ns (5%) |         |   80 bytes (1%) |           3 |
| `["groupby", "sum", "sac"]`                                    |   4.383 ms (5%) |         |  13.22 KiB (1%) |         107 |
| `["groupby", "sum", "xf-with-init"]`                           |  72.500 μs (5%) |         |   1.05 KiB (1%) |           9 |
| `["groupby", "sum", "xf-without-init"]`                        |  71.004 μs (5%) |         |   1.05 KiB (1%) |           9 |
| `["mapcat_eduction", "base"]`                                  |  30.406 μs (5%) |         |                 |             |
| `["mapcat_eduction", "xf-eduction"]`                           | 963.150 ns (5%) |         |                 |             |
| `["mapcat_eduction", "xf-xf"]`                                 | 963.000 ns (5%) |         |                 |             |
| `["missing_argmax", "man"]`                                    |   2.220 μs (5%) |         |                 |             |
| `["missing_argmax", "rf"]`                                     |   1.084 μs (5%) |         |                 |             |
| `["missing_argmax", "xf"]`                                     |   1.093 μs (5%) |         |   32 bytes (1%) |           1 |
| `["missing_dot", "equiv"]`                                     |   1.300 μs (5%) |         |   48 bytes (1%) |           3 |
| `["missing_dot", "man"]`                                       | 627.610 ns (5%) |         |   48 bytes (1%) |           3 |
| `["missing_dot", "naive"]`                                     |   1.712 μs (5%) |         |   48 bytes (1%) |           3 |
| `["missing_dot", "rf"]`                                        | 645.249 ns (5%) |         |   48 bytes (1%) |           3 |
| `["missing_dot", "rf_nota"]`                                   |   1.310 μs (5%) |         |   48 bytes (1%) |           3 |
| `["missing_dot", "xf"]`                                        |  45.489 μs (5%) |         |  72.14 KiB (1%) |        3744 |
| `["missing_dot", "xf_nota"]`                                   |  45.521 μs (5%) |         |  71.94 KiB (1%) |        3732 |
| `["overhead", "foldl"]`                                        |   2.069 ns (5%) |         |                 |             |
| `["overhead", "reduce_basecase"]`                              |  53.085 ns (5%) |         |   16 bytes (1%) |           1 |
| `["partition_by", "man"]`                                      |   1.558 ms (5%) |         |  480 bytes (1%) |           3 |
| `["partition_by", "xf"]`                                       |   1.616 ms (5%) |         |  592 bytes (1%) |           5 |
| `["set", "base"]`                                              |   1.846 ms (5%) |         |  49.14 KiB (1%) |          17 |
| `["set", "xf"]`                                                |   1.837 ms (5%) |         |  49.17 KiB (1%) |          19 |
| `["sum_transpose", "30", "noinit", "iter"]`                    |   1.604 μs (5%) |         |                 |             |
| `["sum_transpose", "30", "noinit", "man"]`                     |   2.401 μs (5%) |         |                 |             |
| `["sum_transpose", "30", "noinit", "xf"]`                      | 433.015 ns (5%) |         |                 |             |
| `["sum_transpose", "30", "withinit", "iter"]`                  | 854.862 ns (5%) |         |                 |             |
| `["sum_transpose", "30", "withinit", "man"]`                   | 436.020 ns (5%) |         |                 |             |
| `["sum_transpose", "30", "withinit", "xf"]`                    | 435.833 ns (5%) |         |                 |             |
| `["teerf_filter", "noinit"]`                                   | 245.352 ns (5%) |         |   80 bytes (1%) |           3 |
| `["teerf_filter", "withinit"]`                                 | 154.162 ns (5%) |         |                 |             |

## Benchmark Group List
Here's a list of all the benchmark groups executed by this job:

- `["append!!"]`
- `["cartesian", "copyto!"]`
- `["cat"]`
- `["collect"]`
- `["dict"]`
- `["dot"]`
- `["filter_map_map!"]`
- `["filter_map_reduce"]`
- `["filter_sum", "1000", "RandomFloats", "noinit"]`
- `["filter_sum", "1000", "RandomFloats", "withinit"]`
- `["filter_sum", "1000", "UnitRange", "noinit"]`
- `["filter_sum", "1000", "UnitRange", "withinit"]`
- `["filter_sum", "10000", "RandomFloats", "noinit"]`
- `["filter_sum", "10000", "RandomFloats", "withinit"]`
- `["filter_sum", "10000", "UnitRange", "noinit"]`
- `["filter_sum", "10000", "UnitRange", "withinit"]`
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
- `["sum_transpose", "30", "noinit"]`
- `["sum_transpose", "30", "withinit"]`
- `["teerf_filter"]`

## Julia versioninfo
```
Julia Version 1.7.3
Commit 742b9abb4d (2022-05-06 12:58 UTC)
Platform Info:
  OS: Linux (x86_64-pc-linux-gnu)
      Ubuntu 26.04.1 LTS
  uname: Linux 7.0.0-1016-aws #17-Ubuntu SMP PREEMPT Mon Oct 19 17:36:33 UTC 2026 x86_64 unknown
  CPU: Intel(R) Xeon(R) 6975P-C: 
              speed         user         nice          sys         idle          irq
       #1  3837 MHz       1061 s          0 s         66 s       7519 s          0 s
       #2  3240 MHz       2153 s          0 s         96 s       6419 s          0 s
       #3  3899 MHz       2383 s          0 s        106 s       6113 s          0 s
       #4  3921 MHz       2326 s          0 s         76 s       6236 s          0 s
       
  Memory: 15.332740783691406 GB (12765.7265625 MB free)
  Uptime: 879.75 sec
  Load Avg:  1.0  0.98  0.66
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-12.0.1 (ORCJIT, icelake-client)
```

---
# Runtime information
| Runtime Info | |
|:--|:--|
| BLAS #threads | 4 |
| `BLAS.vendor()` | `openblas64` |
| `Sys.CPU_THREADS` | 4 |

`lscpu` output:

    Architecture:                            x86_64
    CPU op-mode(s):                          32-bit, 64-bit
    Address sizes:                           48 bits physical, 48 bits virtual
    Byte Order:                              Little Endian
    CPU(s):                                  4
    On-line CPU(s) list:                     0-3
    Vendor ID:                               GenuineIntel
    Model name:                              Intel(R) Xeon(R) 6975P-C
    CPU family:                              6
    Model:                                   173
    Thread(s) per core:                      2
    Core(s) per socket:                      2
    Socket(s):                               1
    Stepping:                                1
    BogoMIPS:                                5400.00
    Flags:                                   fpu vme de pse tsc msr pae mce cx8 apic sep mtrr pge mca cmov pat pse36 clflush mmx fxsr sse sse2 ss ht syscall nx pdpe1gb rdtscp lm constant_tsc arch_perfmon rep_good nopl xtopology nonstop_tsc cpuid aperfmperf tsc_known_freq pni pclmulqdq monitor vmx ssse3 fma cx16 pdcm pcid sse4_1 sse4_2 x2apic movbe popcnt tsc_deadline_timer aes xsave avx f16c rdrand hypervisor lahf_lm abm 3dnowprefetch cpuid_fault ssbd ibrs ibpb stibp ibrs_enhanced tpr_shadow flexpriority ept vpid ept_ad fsgsbase tsc_adjust bmi1 avx2 smep bmi2 erms invpcid avx512f avx512dq rdseed adx smap avx512ifma clflushopt clwb avx512cd sha_ni avx512bw avx512vl xsaveopt xsavec xgetbv1 xsaves avx_vnni avx512_bf16 wbnoinvd ida arat vnmi avx512vbmi umip pku ospke waitpkg avx512_vbmi2 gfni vaes vpclmulqdq avx512_vnni avx512_bitalg tme avx512_vpopcntdq rdpid bus_lock_detect cldemote movdiri movdir64b md_clear serialize amx_bf16 avx512_fp16 amx_tile amx_int8 flush_l1d arch_capabilities
    Virtualization:                          VT-x
    Hypervisor vendor:                       KVM
    Virtualization type:                     full
    L1d cache:                               96 KiB (2 instances)
    L1i cache:                               128 KiB (2 instances)
    L2 cache:                                4 MiB (2 instances)
    L3 cache:                                480 MiB (1 instance)
    NUMA node(s):                            1
    NUMA node0 CPU(s):                       0-3
    Vulnerability Gather data sampling:      Not affected
    Vulnerability Ghostwrite:                Not affected
    Vulnerability Indirect target selection: Not affected
    Vulnerability Itlb multihit:             Not affected
    Vulnerability L1tf:                      Not affected
    Vulnerability Mds:                       Not affected
    Vulnerability Meltdown:                  Not affected
    Vulnerability Mmio stale data:           Not affected
    Vulnerability Old microcode:             Not affected
    Vulnerability Reg file data sampling:    Not affected
    Vulnerability Retbleed:                  Not affected
    Vulnerability Spec rstack overflow:      Not affected
    Vulnerability Spec store bypass:         Mitigation; Speculative Store Bypass disabled via prctl
    Vulnerability Spectre v1:                Mitigation; usercopy/swapgs barriers and __user pointer sanitization
    Vulnerability Spectre v2:                Mitigation; Enhanced / Automatic IBRS; IBPB conditional; PBRSB-eIBRS Not affected; BHI BHI_DIS_S
    Vulnerability Srbds:                     Not affected
    Vulnerability Tsa:                       Not affected
    Vulnerability Tsx async abort:           Not affected
    Vulnerability Vmscape:                   Not affected
    

| Cpu Property       | Value                                                      |
|:------------------ |:---------------------------------------------------------- |
| Brand              | Intel(R) Xeon(R) 6975P-C                                   |
| Vendor             | :Intel                                                     |
| Architecture       | :UnknownIntel                                              |
| Model              | Family: 0x06, Model: 0xad, Stepping: 0x01, Type: 0x00      |
| Cores              | 2 physical cores, 4 logical cores (on executing CPU)       |
|                    | Hyperthreading hardware capability detected                |
| Clock Frequencies  | Not supported by CPU                                       |
| Data Cache         | Level 1:3 : (48, 2048, 491520) kbytes                      |
|                    | 64 byte cache line size                                    |
| Address Size       | 48 bits virtual, 48 bits physical                          |
| SIMD               | 512 bit = 64 byte max. SIMD vector size                    |
| Time Stamp Counter | TSC is accessible via `rdtsc`                              |
|                    | TSC runs at constant rate (invariant from clock frequency) |
| Perf. Monitoring   | Performance Monitoring Counters (PMC) revision 5           |
|                    | Available hardware counters per logical core:              |
|                    | 1 fixed-function counters of 48 bit width                  |
|                    | 8 general-purpose counters of 48 bit width                 |
| Hypervisor         | Yes, KVM                                                   |

