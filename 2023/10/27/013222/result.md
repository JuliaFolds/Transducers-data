# Benchmark result

* Pull request commit: [`4e208f210b62655cb86682aed35a32315839d88a`](https://github.com/JuliaFolds/Transducers.jl/commit/4e208f210b62655cb86682aed35a32315839d88a)
* Pull request: <https://github.com/JuliaFolds/Transducers.jl/pull/243> (Update */Manifest.toml)

# Judge result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmarks:
    - Target: 27 Oct 2023 - 01:22
    - Baseline: 27 Oct 2023 - 01:27
* Package commits:
    - Target: b2f747
    - Baseline: 2a51f8
* Julia commits:
    - Target: 742b9a
    - Baseline: 742b9a
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

| ID                                                             | time ratio                   | memory ratio                 |
|----------------------------------------------------------------|------------------------------|------------------------------|
| `["cartesian", "copyto!", "iter"]`                             |                1.28 (5%) :x: |                   1.00 (1%)  |
| `["cartesian", "copyto!", "man"]`                              |                1.28 (5%) :x: |                   1.00 (1%)  |
| `["cartesian", "copyto!", "xf"]`                               |                1.31 (5%) :x: |                   1.00 (1%)  |
| `["collect", "filter-missing"]`                                |                1.19 (5%) :x: |                   1.00 (1%)  |
| `["collect", "identity-float"]`                                |                1.07 (5%) :x: |                   1.00 (1%)  |
| `["filter_sum", "1000", "RandomFloats", "withinit", "naive"]`  | 0.84 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["filter_sum", "10000", "RandomFloats", "withinit", "naive"]` | 0.75 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["gemm", "mul", "linalg", "32"]`                              | 0.92 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["gemm", "mul", "linalg", "8"]`                               | 0.74 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["gemm", "mul", "man", "false", "256"]`                       |                1.19 (5%) :x: |                   1.00 (1%)  |
| `["gemm", "mul", "man", "false", "32"]`                        |                1.06 (5%) :x: |                   1.00 (1%)  |
| `["gemm", "mul", "man", "false", "8"]`                         |                1.24 (5%) :x: |                   1.00 (1%)  |
| `["gemm", "mul", "man", "ivdep", "256"]`                       |                1.21 (5%) :x: |                   1.00 (1%)  |
| `["gemm", "mul", "man", "ivdep", "32"]`                        |                1.10 (5%) :x: |                   1.00 (1%)  |
| `["gemm", "mul", "man", "ivdep", "8"]`                         |                1.07 (5%) :x: |                   1.00 (1%)  |
| `["gemm", "mul", "man", "true", "256"]`                        |                1.20 (5%) :x: |                   1.00 (1%)  |
| `["gemm", "mul", "man", "true", "32"]`                         |                1.11 (5%) :x: |                   1.00 (1%)  |
| `["gemm", "mul", "man", "true", "8"]`                          |                1.12 (5%) :x: |                   1.00 (1%)  |
| `["gemm", "mul", "xf", "false", "256"]`                        |                1.19 (5%) :x: |                   1.00 (1%)  |
| `["gemm", "mul", "xf", "false", "32"]`                         |                1.07 (5%) :x: |                   1.00 (1%)  |
| `["gemm", "mul", "xf", "ivdep", "256"]`                        |                1.21 (5%) :x: |                   1.00 (1%)  |
| `["gemm", "mul", "xf", "ivdep", "32"]`                         |                1.05 (5%) :x: |                   1.00 (1%)  |
| `["gemm", "mul", "xf", "true", "256"]`                         |                1.20 (5%) :x: |                   1.00 (1%)  |
| `["gemm", "mul", "xf", "true", "8"]`                           |                1.16 (5%) :x: |                   1.00 (1%)  |
| `["groupby", "sum", "sac"]`                                    | 0.02 (5%) :white_check_mark: | 0.12 (1%) :white_check_mark: |
| `["groupby", "sum", "xf-without-init"]`                        |                1.05 (5%) :x: |                   1.00 (1%)  |

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
      Ubuntu 22.04.3 LTS
  uname: Linux 6.2.0-1015-azure #15~22.04.1-Ubuntu SMP Fri Oct  6 13:20:44 UTC 2023 x86_64 x86_64
  CPU: Intel(R) Xeon(R) Platinum 8370C CPU @ 2.80GHz: 
              speed         user         nice          sys         idle          irq
       #1  2793 MHz       4917 s          0 s        149 s       2373 s          0 s
       #2  2793 MHz       2394 s          0 s        174 s       4859 s          0 s
       
  Memory: 6.759746551513672 GB (3410.5234375 MB free)
  Uptime: 749.85 sec
  Load Avg:  1.07  0.98  0.61
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-12.0.1 (ORCJIT, icelake-server)
```

### Baseline
```
Julia Version 1.7.3
Commit 742b9abb4d (2022-05-06 12:58 UTC)
Platform Info:
  OS: Linux (x86_64-pc-linux-gnu)
      Ubuntu 22.04.3 LTS
  uname: Linux 6.2.0-1015-azure #15~22.04.1-Ubuntu SMP Fri Oct  6 13:20:44 UTC 2023 x86_64 x86_64
  CPU: Intel(R) Xeon(R) Platinum 8370C CPU @ 2.80GHz: 
              speed         user         nice          sys         idle          irq
       #1  2793 MHz       7605 s          0 s        192 s       2456 s          0 s
       #2  2793 MHz       2539 s          0 s        213 s       7479 s          0 s
       
  Memory: 6.759746551513672 GB (3376.22265625 MB free)
  Uptime: 1031.35 sec
  Load Avg:  1.0  1.0  0.74
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-12.0.1 (ORCJIT, icelake-server)
```

---
# Target result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmark: 27 Oct 2023 - 1:22
* Package commit: b2f747
* Julia commit: 742b9a
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
| `["append!!", "eduction"]`                                     |  18.900 μs (5%) |         |  53.98 KiB (1%) |           8 |
| `["append!!", "xf"]`                                           |  18.900 μs (5%) |         |  53.98 KiB (1%) |           8 |
| `["cartesian", "copyto!", "iter"]`                             |   3.625 μs (5%) |         |                 |             |
| `["cartesian", "copyto!", "man"]`                              |   3.625 μs (5%) |         |                 |             |
| `["cartesian", "copyto!", "xf"]`                               |   2.844 μs (5%) |         |                 |             |
| `["cat", "base"]`                                              |   1.930 μs (5%) |         |                 |             |
| `["cat", "xf"]`                                                |   1.550 μs (5%) |         |                 |             |
| `["collect", "filter-missing"]`                                |   1.140 μs (5%) |         |   9.94 KiB (1%) |           1 |
| `["collect", "identity-float"]`                                |   7.425 μs (5%) |         |  78.17 KiB (1%) |           2 |
| `["collect", "identity-union"]`                                | 149.898 μs (5%) |         | 400.53 KiB (1%) |       10003 |
| `["dict", "base"]`                                             |   3.622 ms (5%) |         |  92.45 KiB (1%) |          22 |
| `["dict", "xf"]`                                               |   3.818 ms (5%) |         |  91.95 KiB (1%) |          18 |
| `["dot", "blas"]`                                              |   3.425 μs (5%) |         |                 |             |
| `["dot", "man"]`                                               |   2.055 μs (5%) |         |                 |             |
| `["dot", "rf"]`                                                |   2.222 μs (5%) |         |                 |             |
| `["dot", "xf"]`                                                |   2.222 μs (5%) |         |                 |             |
| `["filter_map_map!", "man"]`                                   |  45.299 μs (5%) |         |                 |             |
| `["filter_map_map!", "xf"]`                                    |  49.100 μs (5%) |         |                 |             |
| `["filter_map_reduce", "man"]`                                 | 314.498 μs (5%) |         |                 |             |
| `["filter_map_reduce", "xf"]`                                  | 315.197 μs (5%) |         |                 |             |
| `["filter_sum", "1000", "RandomFloats", "noinit", "base"]`     |   3.650 μs (5%) |         |                 |             |
| `["filter_sum", "1000", "RandomFloats", "noinit", "naive"]`    |   1.850 μs (5%) |         |                 |             |
| `["filter_sum", "1000", "RandomFloats", "noinit", "xf"]`       |   2.489 μs (5%) |         |                 |             |
| `["filter_sum", "1000", "RandomFloats", "withinit", "base"]`   |   2.500 μs (5%) |         |                 |             |
| `["filter_sum", "1000", "RandomFloats", "withinit", "naive"]`  | 820.226 ns (5%) |         |                 |             |
| `["filter_sum", "1000", "RandomFloats", "withinit", "xf"]`     |   2.500 μs (5%) |         |                 |             |
| `["filter_sum", "1000", "UnitRange", "noinit", "base"]`        |   1.240 μs (5%) |         |                 |             |
| `["filter_sum", "1000", "UnitRange", "noinit", "naive"]`       |   1.070 μs (5%) |         |                 |             |
| `["filter_sum", "1000", "UnitRange", "noinit", "xf"]`          | 226.567 ns (5%) |         |                 |             |
| `["filter_sum", "1000", "UnitRange", "withinit", "base"]`      | 166.928 ns (5%) |         |                 |             |
| `["filter_sum", "1000", "UnitRange", "withinit", "naive"]`     | 813.782 ns (5%) |         |                 |             |
| `["filter_sum", "1000", "UnitRange", "withinit", "xf"]`        | 166.970 ns (5%) |         |                 |             |
| `["filter_sum", "10000", "RandomFloats", "noinit", "base"]`    |  36.799 μs (5%) |         |                 |             |
| `["filter_sum", "10000", "RandomFloats", "noinit", "naive"]`   |  17.699 μs (5%) |         |                 |             |
| `["filter_sum", "10000", "RandomFloats", "noinit", "xf"]`      |  25.499 μs (5%) |         |                 |             |
| `["filter_sum", "10000", "RandomFloats", "withinit", "base"]`  |  25.499 μs (5%) |         |                 |             |
| `["filter_sum", "10000", "RandomFloats", "withinit", "naive"]` |   7.900 μs (5%) |         |                 |             |
| `["filter_sum", "10000", "RandomFloats", "withinit", "xf"]`    |  25.499 μs (5%) |         |                 |             |
| `["filter_sum", "10000", "UnitRange", "noinit", "base"]`       |  12.299 μs (5%) |         |                 |             |
| `["filter_sum", "10000", "UnitRange", "noinit", "naive"]`      |   9.999 μs (5%) |         |                 |             |
| `["filter_sum", "10000", "UnitRange", "noinit", "xf"]`         |   2.211 μs (5%) |         |                 |             |
| `["filter_sum", "10000", "UnitRange", "withinit", "base"]`     |   1.600 μs (5%) |         |                 |             |
| `["filter_sum", "10000", "UnitRange", "withinit", "naive"]`    |   8.033 μs (5%) |         |                 |             |
| `["filter_sum", "10000", "UnitRange", "withinit", "xf"]`       |   1.600 μs (5%) |         |                 |             |
| `["findall", "base"]`                                          | 136.099 μs (5%) |         | 797.20 KiB (1%) |           8 |
| `["findall", "xf-array"]`                                      |   1.262 ms (5%) |         |   2.94 MiB (1%) |       96426 |
| `["findall", "xf-iter"]`                                       | 750.394 μs (5%) |         |   1.83 MiB (1%) |          14 |
| `["gemm", "fusedmul", "blas", "16"]`                           |   9.415 ms (5%) |         |                 |             |
| `["gemm", "fusedmul", "blas", "2"]`                            |   2.461 ms (5%) |         |                 |             |
| `["gemm", "fusedmul", "blas", "32"]`                           |  17.333 ms (5%) |         |                 |             |
| `["gemm", "fusedmul", "blas", "8"]`                            |   5.530 ms (5%) |         |                 |             |
| `["gemm", "fusedmul", "xf", "16"]`                             |   4.653 ms (5%) |         |  192 bytes (1%) |           4 |
| `["gemm", "fusedmul", "xf", "2"]`                              | 572.496 μs (5%) |         |  192 bytes (1%) |           4 |
| `["gemm", "fusedmul", "xf", "32"]`                             |   9.302 ms (5%) |         |  192 bytes (1%) |           4 |
| `["gemm", "fusedmul", "xf", "8"]`                              |   2.316 ms (5%) |         |  192 bytes (1%) |           4 |
| `["gemm", "mul", "linalg", "256"]`                             |   3.938 ms (5%) |         |                 |             |
| `["gemm", "mul", "linalg", "32"]`                              |   7.950 μs (5%) |         |                 |             |
| `["gemm", "mul", "linalg", "8"]`                               | 296.105 ns (5%) |         |                 |             |
| `["gemm", "mul", "man", "false", "256"]`                       |   3.266 ms (5%) |         |                 |             |
| `["gemm", "mul", "man", "false", "32"]`                        |   7.325 μs (5%) |         |                 |             |
| `["gemm", "mul", "man", "false", "8"]`                         | 497.404 ns (5%) |         |                 |             |
| `["gemm", "mul", "man", "ivdep", "256"]`                       |   3.185 ms (5%) |         |                 |             |
| `["gemm", "mul", "man", "ivdep", "32"]`                        |   6.180 μs (5%) |         |                 |             |
| `["gemm", "mul", "man", "ivdep", "8"]`                         | 427.036 ns (5%) |         |                 |             |
| `["gemm", "mul", "man", "true", "256"]`                        |   3.226 ms (5%) |         |                 |             |
| `["gemm", "mul", "man", "true", "32"]`                         |   6.900 μs (5%) |         |                 |             |
| `["gemm", "mul", "man", "true", "8"]`                          | 447.208 ns (5%) |         |                 |             |
| `["gemm", "mul", "xf", "false", "256"]`                        |   3.278 ms (5%) |         |   80 bytes (1%) |           3 |
| `["gemm", "mul", "xf", "false", "32"]`                         |   7.300 μs (5%) |         |   80 bytes (1%) |           3 |
| `["gemm", "mul", "xf", "false", "8"]`                          | 480.407 ns (5%) |         |   80 bytes (1%) |           3 |
| `["gemm", "mul", "xf", "ivdep", "256"]`                        |   3.170 ms (5%) |         |   80 bytes (1%) |           3 |
| `["gemm", "mul", "xf", "ivdep", "32"]`                         |   5.900 μs (5%) |         |   80 bytes (1%) |           3 |
| `["gemm", "mul", "xf", "ivdep", "8"]`                          | 483.072 ns (5%) |         |   80 bytes (1%) |           3 |
| `["gemm", "mul", "xf", "true", "256"]`                         |   3.215 ms (5%) |         |   80 bytes (1%) |           3 |
| `["gemm", "mul", "xf", "true", "32"]`                          |   6.680 μs (5%) |         |   80 bytes (1%) |           3 |
| `["gemm", "mul", "xf", "true", "8"]`                           | 462.431 ns (5%) |         |   80 bytes (1%) |           3 |
| `["groupby", "sum", "sac"]`                                    | 139.899 μs (5%) |         |   1.64 KiB (1%) |          11 |
| `["groupby", "sum", "xf-with-init"]`                           | 135.999 μs (5%) |         |   1.05 KiB (1%) |           9 |
| `["groupby", "sum", "xf-without-init"]`                        | 141.399 μs (5%) |         |   1.05 KiB (1%) |           9 |
| `["mapcat_eduction", "base"]`                                  |  51.099 μs (5%) |         |                 |             |
| `["mapcat_eduction", "xf-eduction"]`                           |   1.520 μs (5%) |         |                 |             |
| `["mapcat_eduction", "xf-xf"]`                                 |   1.520 μs (5%) |         |                 |             |
| `["missing_argmax", "man"]`                                    |   3.162 μs (5%) |         |                 |             |
| `["missing_argmax", "rf"]`                                     |   1.670 μs (5%) |         |                 |             |
| `["missing_argmax", "xf"]`                                     |   1.690 μs (5%) |         |   32 bytes (1%) |           1 |
| `["missing_dot", "equiv"]`                                     |   2.255 μs (5%) |         |   16 bytes (1%) |           1 |
| `["missing_dot", "man"]`                                       |   1.590 μs (5%) |         |   16 bytes (1%) |           1 |
| `["missing_dot", "naive"]`                                     |   3.350 μs (5%) |         |   16 bytes (1%) |           1 |
| `["missing_dot", "rf"]`                                        |   1.600 μs (5%) |         |   16 bytes (1%) |           1 |
| `["missing_dot", "rf_nota"]`                                   |   2.267 μs (5%) |         |   16 bytes (1%) |           1 |
| `["missing_dot", "xf"]`                                        |  90.799 μs (5%) |         |  72.02 KiB (1%) |        3736 |
| `["missing_dot", "xf_nota"]`                                   |  91.499 μs (5%) |         |  72.33 KiB (1%) |        3750 |
| `["overhead", "foldl"]`                                        |   3.599 ns (5%) |         |                 |             |
| `["overhead", "reduce_basecase"]`                              |  92.856 ns (5%) |         |   16 bytes (1%) |           1 |
| `["partition_by", "man"]`                                      |   2.601 ms (5%) |         |  480 bytes (1%) |           3 |
| `["partition_by", "xf"]`                                       |   2.838 ms (5%) |         |  592 bytes (1%) |           5 |
| `["set", "base"]`                                              |   3.843 ms (5%) |         |  49.14 KiB (1%) |          17 |
| `["set", "xf"]`                                                |   3.633 ms (5%) |         |  49.17 KiB (1%) |          19 |
| `["sum_transpose", "30", "noinit", "iter"]`                    |   3.225 μs (5%) |         |                 |             |
| `["sum_transpose", "30", "noinit", "man"]`                     |   4.328 μs (5%) |         |                 |             |
| `["sum_transpose", "30", "noinit", "xf"]`                      |   1.350 μs (5%) |         |                 |             |
| `["sum_transpose", "30", "withinit", "iter"]`                  |   1.440 μs (5%) |         |                 |             |
| `["sum_transpose", "30", "withinit", "man"]`                   |   1.350 μs (5%) |         |                 |             |
| `["sum_transpose", "30", "withinit", "xf"]`                    |   1.350 μs (5%) |         |                 |             |
| `["teerf_filter", "noinit"]`                                   | 400.497 ns (5%) |         |   80 bytes (1%) |           3 |
| `["teerf_filter", "withinit"]`                                 | 248.282 ns (5%) |         |                 |             |

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
      Ubuntu 22.04.3 LTS
  uname: Linux 6.2.0-1015-azure #15~22.04.1-Ubuntu SMP Fri Oct  6 13:20:44 UTC 2023 x86_64 x86_64
  CPU: Intel(R) Xeon(R) Platinum 8370C CPU @ 2.80GHz: 
              speed         user         nice          sys         idle          irq
       #1  2793 MHz       4917 s          0 s        149 s       2373 s          0 s
       #2  2793 MHz       2394 s          0 s        174 s       4859 s          0 s
       
  Memory: 6.759746551513672 GB (3410.5234375 MB free)
  Uptime: 749.85 sec
  Load Avg:  1.07  0.98  0.61
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-12.0.1 (ORCJIT, icelake-server)
```

---
# Baseline result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmark: 27 Oct 2023 - 1:27
* Package commit: 2a51f8
* Julia commit: 742b9a
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
| `["append!!", "eduction"]`                                     |  19.300 μs (5%) |         |  53.98 KiB (1%) |           8 |
| `["append!!", "xf"]`                                           |  19.300 μs (5%) |         |  53.98 KiB (1%) |           8 |
| `["cartesian", "copyto!", "iter"]`                             |   2.825 μs (5%) |         |                 |             |
| `["cartesian", "copyto!", "man"]`                              |   2.825 μs (5%) |         |                 |             |
| `["cartesian", "copyto!", "xf"]`                               |   2.178 μs (5%) |         |                 |             |
| `["cat", "base"]`                                              |   1.930 μs (5%) |         |                 |             |
| `["cat", "xf"]`                                                |   1.560 μs (5%) |         |                 |             |
| `["collect", "filter-missing"]`                                | 960.000 ns (5%) |         |   9.94 KiB (1%) |           1 |
| `["collect", "identity-float"]`                                |   6.950 μs (5%) |         |  78.17 KiB (1%) |           2 |
| `["collect", "identity-union"]`                                | 148.399 μs (5%) |         | 400.53 KiB (1%) |       10003 |
| `["dict", "base"]`                                             |   3.622 ms (5%) |         |  92.45 KiB (1%) |          22 |
| `["dict", "xf"]`                                               |   3.816 ms (5%) |         |  91.95 KiB (1%) |          18 |
| `["dot", "blas"]`                                              |   3.425 μs (5%) |         |                 |             |
| `["dot", "man"]`                                               |   2.055 μs (5%) |         |                 |             |
| `["dot", "rf"]`                                                |   2.244 μs (5%) |         |                 |             |
| `["dot", "xf"]`                                                |   2.255 μs (5%) |         |                 |             |
| `["filter_map_map!", "man"]`                                   |  44.700 μs (5%) |         |                 |             |
| `["filter_map_map!", "xf"]`                                    |  47.200 μs (5%) |         |                 |             |
| `["filter_map_reduce", "man"]`                                 | 315.498 μs (5%) |         |                 |             |
| `["filter_map_reduce", "xf"]`                                  | 315.099 μs (5%) |         |                 |             |
| `["filter_sum", "1000", "RandomFloats", "noinit", "base"]`     |   3.650 μs (5%) |         |                 |             |
| `["filter_sum", "1000", "RandomFloats", "noinit", "naive"]`    |   1.850 μs (5%) |         |                 |             |
| `["filter_sum", "1000", "RandomFloats", "noinit", "xf"]`       |   2.489 μs (5%) |         |                 |             |
| `["filter_sum", "1000", "RandomFloats", "withinit", "base"]`   |   2.500 μs (5%) |         |                 |             |
| `["filter_sum", "1000", "RandomFloats", "withinit", "naive"]`  | 974.988 ns (5%) |         |                 |             |
| `["filter_sum", "1000", "RandomFloats", "withinit", "xf"]`     |   2.500 μs (5%) |         |                 |             |
| `["filter_sum", "1000", "UnitRange", "noinit", "base"]`        |   1.230 μs (5%) |         |                 |             |
| `["filter_sum", "1000", "UnitRange", "noinit", "naive"]`       |   1.080 μs (5%) |         |                 |             |
| `["filter_sum", "1000", "UnitRange", "noinit", "xf"]`          | 225.730 ns (5%) |         |                 |             |
| `["filter_sum", "1000", "UnitRange", "withinit", "base"]`      | 167.062 ns (5%) |         |                 |             |
| `["filter_sum", "1000", "UnitRange", "withinit", "naive"]`     | 817.230 ns (5%) |         |                 |             |
| `["filter_sum", "1000", "UnitRange", "withinit", "xf"]`        | 166.971 ns (5%) |         |                 |             |
| `["filter_sum", "10000", "RandomFloats", "noinit", "base"]`    |  36.799 μs (5%) |         |                 |             |
| `["filter_sum", "10000", "RandomFloats", "noinit", "naive"]`   |  17.699 μs (5%) |         |                 |             |
| `["filter_sum", "10000", "RandomFloats", "noinit", "xf"]`      |  25.499 μs (5%) |         |                 |             |
| `["filter_sum", "10000", "RandomFloats", "withinit", "base"]`  |  25.399 μs (5%) |         |                 |             |
| `["filter_sum", "10000", "RandomFloats", "withinit", "naive"]` |  10.525 μs (5%) |         |                 |             |
| `["filter_sum", "10000", "RandomFloats", "withinit", "xf"]`    |  25.499 μs (5%) |         |                 |             |
| `["filter_sum", "10000", "UnitRange", "noinit", "base"]`       |  12.199 μs (5%) |         |                 |             |
| `["filter_sum", "10000", "UnitRange", "noinit", "naive"]`      |  10.000 μs (5%) |         |                 |             |
| `["filter_sum", "10000", "UnitRange", "noinit", "xf"]`         |   2.200 μs (5%) |         |                 |             |
| `["filter_sum", "10000", "UnitRange", "withinit", "base"]`     |   1.600 μs (5%) |         |                 |             |
| `["filter_sum", "10000", "UnitRange", "withinit", "naive"]`    |   8.033 μs (5%) |         |                 |             |
| `["filter_sum", "10000", "UnitRange", "withinit", "xf"]`       |   1.600 μs (5%) |         |                 |             |
| `["findall", "base"]`                                          | 135.699 μs (5%) |         | 797.20 KiB (1%) |           8 |
| `["findall", "xf-array"]`                                      |   1.254 ms (5%) |         |   2.94 MiB (1%) |       96426 |
| `["findall", "xf-iter"]`                                       | 726.996 μs (5%) |         |   1.83 MiB (1%) |          14 |
| `["gemm", "fusedmul", "blas", "16"]`                           |   9.445 ms (5%) |         |                 |             |
| `["gemm", "fusedmul", "blas", "2"]`                            |   2.458 ms (5%) |         |                 |             |
| `["gemm", "fusedmul", "blas", "32"]`                           |  17.297 ms (5%) |         |                 |             |
| `["gemm", "fusedmul", "blas", "8"]`                            |   5.522 ms (5%) |         |                 |             |
| `["gemm", "fusedmul", "xf", "16"]`                             |   4.708 ms (5%) |         |  192 bytes (1%) |           4 |
| `["gemm", "fusedmul", "xf", "2"]`                              | 575.297 μs (5%) |         |  192 bytes (1%) |           4 |
| `["gemm", "fusedmul", "xf", "32"]`                             |   9.382 ms (5%) |         |  192 bytes (1%) |           4 |
| `["gemm", "fusedmul", "xf", "8"]`                              |   2.307 ms (5%) |         |  192 bytes (1%) |           4 |
| `["gemm", "mul", "linalg", "256"]`                             |   3.934 ms (5%) |         |                 |             |
| `["gemm", "mul", "linalg", "32"]`                              |   8.599 μs (5%) |         |                 |             |
| `["gemm", "mul", "linalg", "8"]`                               | 399.000 ns (5%) |         |                 |             |
| `["gemm", "mul", "man", "false", "256"]`                       |   2.747 ms (5%) |         |                 |             |
| `["gemm", "mul", "man", "false", "32"]`                        |   6.899 μs (5%) |         |                 |             |
| `["gemm", "mul", "man", "false", "8"]`                         | 400.000 ns (5%) |         |                 |             |
| `["gemm", "mul", "man", "ivdep", "256"]`                       |   2.632 ms (5%) |         |                 |             |
| `["gemm", "mul", "man", "ivdep", "32"]`                        |   5.600 μs (5%) |         |                 |             |
| `["gemm", "mul", "man", "ivdep", "8"]`                         | 399.000 ns (5%) |         |                 |             |
| `["gemm", "mul", "man", "true", "256"]`                        |   2.685 ms (5%) |         |                 |             |
| `["gemm", "mul", "man", "true", "32"]`                         |   6.199 μs (5%) |         |                 |             |
| `["gemm", "mul", "man", "true", "8"]`                          | 399.000 ns (5%) |         |                 |             |
| `["gemm", "mul", "xf", "false", "256"]`                        |   2.748 ms (5%) |         |   80 bytes (1%) |           3 |
| `["gemm", "mul", "xf", "false", "32"]`                         |   6.799 μs (5%) |         |   80 bytes (1%) |           3 |
| `["gemm", "mul", "xf", "false", "8"]`                          | 499.000 ns (5%) |         |   80 bytes (1%) |           3 |
| `["gemm", "mul", "xf", "ivdep", "256"]`                        |   2.625 ms (5%) |         |   80 bytes (1%) |           3 |
| `["gemm", "mul", "xf", "ivdep", "32"]`                         |   5.599 μs (5%) |         |   80 bytes (1%) |           3 |
| `["gemm", "mul", "xf", "ivdep", "8"]`                          | 499.000 ns (5%) |         |   80 bytes (1%) |           3 |
| `["gemm", "mul", "xf", "true", "256"]`                         |   2.678 ms (5%) |         |   80 bytes (1%) |           3 |
| `["gemm", "mul", "xf", "true", "32"]`                          |   6.499 μs (5%) |         |   80 bytes (1%) |           3 |
| `["gemm", "mul", "xf", "true", "8"]`                           | 399.000 ns (5%) |         |   80 bytes (1%) |           3 |
| `["groupby", "sum", "sac"]`                                    |   7.286 ms (5%) |         |  13.14 KiB (1%) |         103 |
| `["groupby", "sum", "xf-with-init"]`                           | 135.699 μs (5%) |         |   1.05 KiB (1%) |           9 |
| `["groupby", "sum", "xf-without-init"]`                        | 134.399 μs (5%) |         |   1.05 KiB (1%) |           9 |
| `["mapcat_eduction", "base"]`                                  |  51.699 μs (5%) |         |                 |             |
| `["mapcat_eduction", "xf-eduction"]`                           |   1.520 μs (5%) |         |                 |             |
| `["mapcat_eduction", "xf-xf"]`                                 |   1.520 μs (5%) |         |                 |             |
| `["missing_argmax", "man"]`                                    |   3.175 μs (5%) |         |                 |             |
| `["missing_argmax", "rf"]`                                     |   1.670 μs (5%) |         |                 |             |
| `["missing_argmax", "xf"]`                                     |   1.690 μs (5%) |         |   32 bytes (1%) |           1 |
| `["missing_dot", "equiv"]`                                     |   2.255 μs (5%) |         |   16 bytes (1%) |           1 |
| `["missing_dot", "man"]`                                       |   1.600 μs (5%) |         |   16 bytes (1%) |           1 |
| `["missing_dot", "naive"]`                                     |   3.350 μs (5%) |         |   16 bytes (1%) |           1 |
| `["missing_dot", "rf"]`                                        |   1.600 μs (5%) |         |   16 bytes (1%) |           1 |
| `["missing_dot", "rf_nota"]`                                   |   2.278 μs (5%) |         |   16 bytes (1%) |           1 |
| `["missing_dot", "xf"]`                                        |  92.799 μs (5%) |         |  72.31 KiB (1%) |        3750 |
| `["missing_dot", "xf_nota"]`                                   |  91.899 μs (5%) |         |  72.17 KiB (1%) |        3744 |
| `["overhead", "foldl"]`                                        |   3.599 ns (5%) |         |                 |             |
| `["overhead", "reduce_basecase"]`                              |  93.486 ns (5%) |         |   16 bytes (1%) |           1 |
| `["partition_by", "man"]`                                      |   2.604 ms (5%) |         |  480 bytes (1%) |           3 |
| `["partition_by", "xf"]`                                       |   2.800 ms (5%) |         |  592 bytes (1%) |           5 |
| `["set", "base"]`                                              |   3.852 ms (5%) |         |  49.14 KiB (1%) |          17 |
| `["set", "xf"]`                                                |   3.677 ms (5%) |         |  49.17 KiB (1%) |          19 |
| `["sum_transpose", "30", "noinit", "iter"]`                    |   3.225 μs (5%) |         |                 |             |
| `["sum_transpose", "30", "noinit", "man"]`                     |   4.328 μs (5%) |         |                 |             |
| `["sum_transpose", "30", "noinit", "xf"]`                      |   1.350 μs (5%) |         |                 |             |
| `["sum_transpose", "30", "withinit", "iter"]`                  |   1.440 μs (5%) |         |                 |             |
| `["sum_transpose", "30", "withinit", "man"]`                   |   1.350 μs (5%) |         |                 |             |
| `["sum_transpose", "30", "withinit", "xf"]`                    |   1.350 μs (5%) |         |                 |             |
| `["teerf_filter", "noinit"]`                                   | 404.015 ns (5%) |         |   80 bytes (1%) |           3 |
| `["teerf_filter", "withinit"]`                                 | 248.018 ns (5%) |         |                 |             |

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
      Ubuntu 22.04.3 LTS
  uname: Linux 6.2.0-1015-azure #15~22.04.1-Ubuntu SMP Fri Oct  6 13:20:44 UTC 2023 x86_64 x86_64
  CPU: Intel(R) Xeon(R) Platinum 8370C CPU @ 2.80GHz: 
              speed         user         nice          sys         idle          irq
       #1  2793 MHz       7605 s          0 s        192 s       2456 s          0 s
       #2  2793 MHz       2539 s          0 s        213 s       7479 s          0 s
       
  Memory: 6.759746551513672 GB (3376.22265625 MB free)
  Uptime: 1031.35 sec
  Load Avg:  1.0  1.0  0.74
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-12.0.1 (ORCJIT, icelake-server)
```

---
# Runtime information
| Runtime Info | |
|:--|:--|
| BLAS #threads | 2 |
| `BLAS.vendor()` | `openblas64` |
| `Sys.CPU_THREADS` | 2 |

`lscpu` output:

    Architecture:                       x86_64
    CPU op-mode(s):                     32-bit, 64-bit
    Address sizes:                      46 bits physical, 48 bits virtual
    Byte Order:                         Little Endian
    CPU(s):                             2
    On-line CPU(s) list:                0,1
    Vendor ID:                          GenuineIntel
    Model name:                         Intel(R) Xeon(R) Platinum 8370C CPU @ 2.80GHz
    CPU family:                         6
    Model:                              106
    Thread(s) per core:                 1
    Core(s) per socket:                 2
    Socket(s):                          1
    Stepping:                           6
    BogoMIPS:                           5586.87
    Flags:                              fpu vme de pse tsc msr pae mce cx8 apic sep mtrr pge mca cmov pat pse36 clflush mmx fxsr sse sse2 ss ht syscall nx pdpe1gb rdtscp lm constant_tsc rep_good nopl xtopology cpuid pni pclmulqdq ssse3 fma cx16 pcid sse4_1 sse4_2 movbe popcnt aes xsave avx f16c rdrand hypervisor lahf_lm abm 3dnowprefetch invpcid_single pti fsgsbase bmi1 hle avx2 smep bmi2 erms invpcid rtm avx512f avx512dq rdseed adx smap clflushopt avx512cd avx512bw avx512vl xsaveopt xsavec xsaves md_clear
    Hypervisor vendor:                  Microsoft
    Virtualization type:                full
    L1d cache:                          96 KiB (2 instances)
    L1i cache:                          64 KiB (2 instances)
    L2 cache:                           2.5 MiB (2 instances)
    L3 cache:                           48 MiB (1 instance)
    NUMA node(s):                       1
    NUMA node0 CPU(s):                  0,1
    Vulnerability Gather data sampling: Unknown: Dependent on hypervisor status
    Vulnerability Itlb multihit:        KVM: Mitigation: VMX unsupported
    Vulnerability L1tf:                 Mitigation; PTE Inversion
    Vulnerability Mds:                  Mitigation; Clear CPU buffers; SMT Host state unknown
    Vulnerability Meltdown:             Mitigation; PTI
    Vulnerability Mmio stale data:      Vulnerable: Clear CPU buffers attempted, no microcode; SMT Host state unknown
    Vulnerability Retbleed:             Not affected
    Vulnerability Spec rstack overflow: Not affected
    Vulnerability Spec store bypass:    Vulnerable
    Vulnerability Spectre v1:           Mitigation; usercopy/swapgs barriers and __user pointer sanitization
    Vulnerability Spectre v2:           Mitigation; Retpolines, STIBP disabled, RSB filling, PBRSB-eIBRS Not affected
    Vulnerability Srbds:                Not affected
    Vulnerability Tsx async abort:      Mitigation; Clear CPU buffers; SMT Host state unknown
    

| Cpu Property       | Value                                                   |
|:------------------ |:------------------------------------------------------- |
| Brand              | Intel(R) Xeon(R) Platinum 8370C CPU @ 2.80GHz           |
| Vendor             | :Intel                                                  |
| Architecture       | :UnknownIntel                                           |
| Model              | Family: 0x06, Model: 0x6a, Stepping: 0x06, Type: 0x00   |
| Cores              | 2 physical cores, 2 logical cores (on executing CPU)    |
|                    | No Hyperthreading hardware capability detected          |
| Clock Frequencies  | Not supported by CPU                                    |
| Data Cache         | Level 1:3 : (48, 1280, 49152) kbytes                    |
|                    | 64 byte cache line size                                 |
| Address Size       | 48 bits virtual, 46 bits physical                       |
| SIMD               | 512 bit = 64 byte max. SIMD vector size                 |
| Time Stamp Counter | TSC is accessible via `rdtsc`                           |
|                    | TSC increased at every clock cycle (non-invariant TSC)  |
| Perf. Monitoring   | Performance Monitoring Counters (PMC) are not supported |
| Hypervisor         | Yes, Microsoft                                          |

