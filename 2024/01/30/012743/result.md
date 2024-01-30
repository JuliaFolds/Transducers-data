# Benchmark result

* Pull request commit: [`c09b494f38101d275eb0f783411a12f337686c97`](https://github.com/JuliaFolds/Transducers.jl/commit/c09b494f38101d275eb0f783411a12f337686c97)
* Pull request: <https://github.com/JuliaFolds/Transducers.jl/pull/243> (Update */Manifest.toml)

# Judge result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmarks:
    - Target: 30 Jan 2024 - 01:21
    - Baseline: 30 Jan 2024 - 01:25
* Package commits:
    - Target: 47822a
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
| `["cartesian", "copyto!", "iter"]`                             | 0.72 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["collect", "filter-missing"]`                                |                1.53 (5%) :x: |                   1.00 (1%)  |
| `["collect", "identity-float"]`                                | 0.53 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["filter_sum", "1000", "RandomFloats", "withinit", "naive"]`  |                1.18 (5%) :x: |                   1.00 (1%)  |
| `["gemm", "fusedmul", "blas", "2"]`                            | 0.91 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["gemm", "fusedmul", "blas", "8"]`                            | 0.93 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["gemm", "fusedmul", "xf", "2"]`                              | 0.92 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["gemm", "mul", "linalg", "8"]`                               | 0.69 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["gemm", "mul", "man", "false", "256"]`                       |                1.07 (5%) :x: |                   1.00 (1%)  |
| `["gemm", "mul", "man", "false", "32"]`                        |                1.05 (5%) :x: |                   1.00 (1%)  |
| `["gemm", "mul", "man", "false", "8"]`                         | 0.90 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["gemm", "mul", "man", "ivdep", "256"]`                       |                1.08 (5%) :x: |                   1.00 (1%)  |
| `["gemm", "mul", "man", "ivdep", "8"]`                         | 0.90 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["gemm", "mul", "man", "true", "256"]`                        |                1.08 (5%) :x: |                   1.00 (1%)  |
| `["gemm", "mul", "man", "true", "8"]`                          |                1.19 (5%) :x: |                   1.00 (1%)  |
| `["gemm", "mul", "xf", "false", "256"]`                        |                1.08 (5%) :x: |                   1.00 (1%)  |
| `["gemm", "mul", "xf", "false", "8"]`                          | 0.91 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["gemm", "mul", "xf", "ivdep", "256"]`                        |                1.07 (5%) :x: |                   1.00 (1%)  |
| `["gemm", "mul", "xf", "ivdep", "8"]`                          | 0.93 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["gemm", "mul", "xf", "true", "256"]`                         |                1.09 (5%) :x: |                   1.00 (1%)  |
| `["gemm", "mul", "xf", "true", "8"]`                           | 0.89 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["groupby", "sum", "sac"]`                                    | 0.01 (5%) :white_check_mark: | 0.12 (1%) :white_check_mark: |
| `["groupby", "sum", "xf-without-init"]`                        |                1.06 (5%) :x: |                   1.00 (1%)  |
| `["missing_dot", "man"]`                                       |                1.21 (5%) :x: |                   1.00 (1%)  |
| `["missing_dot", "rf"]`                                        | 0.83 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["set", "base"]`                                              |                1.05 (5%) :x: |                   1.00 (1%)  |

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
  uname: Linux 6.2.0-1018-azure #18~22.04.1-Ubuntu SMP Tue Nov 21 19:25:02 UTC 2023 x86_64 x86_64
  CPU: AMD EPYC 7763 64-Core Processor: 
              speed         user         nice          sys         idle          irq
       #1  2445 MHz       1062 s          0 s        107 s       6744 s          0 s
       #2  3243 MHz       1638 s          0 s        113 s       6170 s          0 s
       #3  2606 MHz       2163 s          0 s        120 s       5631 s          0 s
       #4  3216 MHz       1645 s          0 s        112 s       6160 s          0 s
       
  Memory: 15.60690689086914 GB (12435.328125 MB free)
  Uptime: 795.42 sec
  Load Avg:  1.03  0.95  0.56
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-12.0.1 (ORCJIT, znver3)
```

### Baseline
```
Julia Version 1.7.3
Commit 742b9abb4d (2022-05-06 12:58 UTC)
Platform Info:
  OS: Linux (x86_64-pc-linux-gnu)
      Ubuntu 22.04.3 LTS
  uname: Linux 6.2.0-1018-azure #18~22.04.1-Ubuntu SMP Tue Nov 21 19:25:02 UTC 2023 x86_64 x86_64
  CPU: AMD EPYC 7763 64-Core Processor: 
              speed         user         nice          sys         idle          irq
       #1  3193 MHz       2043 s          0 s        124 s       8283 s          0 s
       #2  2565 MHz       2042 s          0 s        134 s       8282 s          0 s
       #3  2445 MHz       2523 s          0 s        146 s       7781 s          0 s
       #4  3243 MHz       2468 s          0 s        153 s       7833 s          0 s
       
  Memory: 15.60690689086914 GB (12382.2265625 MB free)
  Uptime: 1049.52 sec
  Load Avg:  1.01  1.03  0.7
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-12.0.1 (ORCJIT, znver3)
```

---
# Target result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmark: 30 Jan 2024 - 1:21
* Package commit: 47822a
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
| `["append!!", "eduction"]`                                     |  14.387 μs (5%) |         |  53.98 KiB (1%) |           8 |
| `["append!!", "xf"]`                                           |  14.417 μs (5%) |         |  53.98 KiB (1%) |           8 |
| `["cartesian", "copyto!", "iter"]`                             |   1.567 μs (5%) |         |                 |             |
| `["cartesian", "copyto!", "man"]`                              |   2.181 μs (5%) |         |                 |             |
| `["cartesian", "copyto!", "xf"]`                               |   1.568 μs (5%) |         |                 |             |
| `["cat", "base"]`                                              |   1.709 μs (5%) |         |                 |             |
| `["cat", "xf"]`                                                |   1.015 μs (5%) |         |                 |             |
| `["collect", "filter-missing"]`                                | 663.364 ns (5%) |         |   9.94 KiB (1%) |           1 |
| `["collect", "identity-float"]`                                |   2.220 μs (5%) |         |  78.17 KiB (1%) |           2 |
| `["collect", "identity-union"]`                                | 104.296 μs (5%) |         | 400.53 KiB (1%) |       10003 |
| `["dict", "base"]`                                             |   2.977 ms (5%) |         |  92.45 KiB (1%) |          22 |
| `["dict", "xf"]`                                               |   2.974 ms (5%) |         |  91.95 KiB (1%) |          18 |
| `["dot", "blas"]`                                              |   1.560 μs (5%) |         |                 |             |
| `["dot", "man"]`                                               |   1.553 μs (5%) |         |                 |             |
| `["dot", "rf"]`                                                |   1.572 μs (5%) |         |                 |             |
| `["dot", "xf"]`                                                |   1.574 μs (5%) |         |                 |             |
| `["filter_map_map!", "man"]`                                   |  47.048 μs (5%) |         |                 |             |
| `["filter_map_map!", "xf"]`                                    |  49.132 μs (5%) |         |                 |             |
| `["filter_map_reduce", "man"]`                                 | 154.319 μs (5%) |         |                 |             |
| `["filter_map_reduce", "xf"]`                                  | 154.309 μs (5%) |         |                 |             |
| `["filter_sum", "1000", "RandomFloats", "noinit", "base"]`     |   3.362 μs (5%) |         |                 |             |
| `["filter_sum", "1000", "RandomFloats", "noinit", "naive"]`    |   1.589 μs (5%) |         |                 |             |
| `["filter_sum", "1000", "RandomFloats", "noinit", "xf"]`       |   1.208 μs (5%) |         |                 |             |
| `["filter_sum", "1000", "RandomFloats", "withinit", "base"]`   |   1.214 μs (5%) |         |                 |             |
| `["filter_sum", "1000", "RandomFloats", "withinit", "naive"]`  | 780.962 ns (5%) |         |                 |             |
| `["filter_sum", "1000", "RandomFloats", "withinit", "xf"]`     |   1.210 μs (5%) |         |                 |             |
| `["filter_sum", "1000", "UnitRange", "noinit", "base"]`        | 626.491 ns (5%) |         |                 |             |
| `["filter_sum", "1000", "UnitRange", "noinit", "naive"]`       | 627.140 ns (5%) |         |                 |             |
| `["filter_sum", "1000", "UnitRange", "noinit", "xf"]`          | 165.607 ns (5%) |         |                 |             |
| `["filter_sum", "1000", "UnitRange", "withinit", "base"]`      | 114.775 ns (5%) |         |                 |             |
| `["filter_sum", "1000", "UnitRange", "withinit", "naive"]`     | 625.205 ns (5%) |         |                 |             |
| `["filter_sum", "1000", "UnitRange", "withinit", "xf"]`        | 113.684 ns (5%) |         |                 |             |
| `["filter_sum", "10000", "RandomFloats", "noinit", "base"]`    |  33.923 μs (5%) |         |                 |             |
| `["filter_sum", "10000", "RandomFloats", "noinit", "naive"]`   |  15.118 μs (5%) |         |                 |             |
| `["filter_sum", "10000", "RandomFloats", "noinit", "xf"]`      |  12.343 μs (5%) |         |                 |             |
| `["filter_sum", "10000", "RandomFloats", "withinit", "base"]`  |  12.343 μs (5%) |         |                 |             |
| `["filter_sum", "10000", "RandomFloats", "withinit", "naive"]` |   9.177 μs (5%) |         |                 |             |
| `["filter_sum", "10000", "RandomFloats", "withinit", "xf"]`    |  12.343 μs (5%) |         |                 |             |
| `["filter_sum", "10000", "UnitRange", "noinit", "base"]`       |   6.179 μs (5%) |         |                 |             |
| `["filter_sum", "10000", "UnitRange", "noinit", "naive"]`      |   6.181 μs (5%) |         |                 |             |
| `["filter_sum", "10000", "UnitRange", "noinit", "xf"]`         |   1.638 μs (5%) |         |                 |             |
| `["filter_sum", "10000", "UnitRange", "withinit", "base"]`     |   1.126 μs (5%) |         |                 |             |
| `["filter_sum", "10000", "UnitRange", "withinit", "naive"]`    |   6.177 μs (5%) |         |                 |             |
| `["filter_sum", "10000", "UnitRange", "withinit", "xf"]`       |   1.122 μs (5%) |         |                 |             |
| `["findall", "base"]`                                          | 108.643 μs (5%) |         | 797.20 KiB (1%) |           8 |
| `["findall", "xf-array"]`                                      | 992.903 μs (5%) |         |   2.94 MiB (1%) |       96426 |
| `["findall", "xf-iter"]`                                       | 674.606 μs (5%) |         |   1.83 MiB (1%) |          14 |
| `["gemm", "fusedmul", "blas", "16"]`                           |   2.501 ms (5%) |         |                 |             |
| `["gemm", "fusedmul", "blas", "2"]`                            |   1.661 ms (5%) |         |                 |             |
| `["gemm", "fusedmul", "blas", "32"]`                           |   3.958 ms (5%) |         |                 |             |
| `["gemm", "fusedmul", "blas", "8"]`                            |   1.730 ms (5%) |         |                 |             |
| `["gemm", "fusedmul", "xf", "16"]`                             |   2.374 ms (5%) |         |  192 bytes (1%) |           4 |
| `["gemm", "fusedmul", "xf", "2"]`                              | 298.109 μs (5%) |         |  192 bytes (1%) |           4 |
| `["gemm", "fusedmul", "xf", "32"]`                             |   4.890 ms (5%) |         |  192 bytes (1%) |           4 |
| `["gemm", "fusedmul", "xf", "8"]`                              |   1.194 ms (5%) |         |  192 bytes (1%) |           4 |
| `["gemm", "mul", "linalg", "256"]`                             | 769.595 μs (5%) |         |                 |             |
| `["gemm", "mul", "linalg", "32"]`                              |   2.831 μs (5%) |         |                 |             |
| `["gemm", "mul", "linalg", "8"]`                               | 166.215 ns (5%) |         |                 |             |
| `["gemm", "mul", "man", "false", "256"]`                       |   2.273 ms (5%) |         |                 |             |
| `["gemm", "mul", "man", "false", "32"]`                        |   5.392 μs (5%) |         |                 |             |
| `["gemm", "mul", "man", "false", "8"]`                         | 289.390 ns (5%) |         |                 |             |
| `["gemm", "mul", "man", "ivdep", "256"]`                       |   2.247 ms (5%) |         |                 |             |
| `["gemm", "mul", "man", "ivdep", "32"]`                        |   4.527 μs (5%) |         |                 |             |
| `["gemm", "mul", "man", "ivdep", "8"]`                         | 279.731 ns (5%) |         |                 |             |
| `["gemm", "mul", "man", "true", "256"]`                        |   2.271 ms (5%) |         |                 |             |
| `["gemm", "mul", "man", "true", "32"]`                         |   4.974 μs (5%) |         |                 |             |
| `["gemm", "mul", "man", "true", "8"]`                          | 393.030 ns (5%) |         |                 |             |
| `["gemm", "mul", "xf", "false", "256"]`                        |   2.245 ms (5%) |         |   80 bytes (1%) |           3 |
| `["gemm", "mul", "xf", "false", "32"]`                         |   5.721 μs (5%) |         |   80 bytes (1%) |           3 |
| `["gemm", "mul", "xf", "false", "8"]`                          | 346.744 ns (5%) |         |   80 bytes (1%) |           3 |
| `["gemm", "mul", "xf", "ivdep", "256"]`                        |   2.255 ms (5%) |         |   80 bytes (1%) |           3 |
| `["gemm", "mul", "xf", "ivdep", "32"]`                         |   4.543 μs (5%) |         |   80 bytes (1%) |           3 |
| `["gemm", "mul", "xf", "ivdep", "8"]`                          | 324.689 ns (5%) |         |   80 bytes (1%) |           3 |
| `["gemm", "mul", "xf", "true", "256"]`                         |   2.255 ms (5%) |         |   80 bytes (1%) |           3 |
| `["gemm", "mul", "xf", "true", "32"]`                          |   4.981 μs (5%) |         |   80 bytes (1%) |           3 |
| `["gemm", "mul", "xf", "true", "8"]`                           | 330.937 ns (5%) |         |   80 bytes (1%) |           3 |
| `["groupby", "sum", "sac"]`                                    |  94.748 μs (5%) |         |   1.64 KiB (1%) |          11 |
| `["groupby", "sum", "xf-with-init"]`                           |  97.292 μs (5%) |         |   1.05 KiB (1%) |           9 |
| `["groupby", "sum", "xf-without-init"]`                        | 100.569 μs (5%) |         |   1.05 KiB (1%) |           9 |
| `["mapcat_eduction", "base"]`                                  |  30.849 μs (5%) |         |                 |             |
| `["mapcat_eduction", "xf-eduction"]`                           |   1.016 μs (5%) |         |                 |             |
| `["mapcat_eduction", "xf-xf"]`                                 |   1.015 μs (5%) |         |                 |             |
| `["missing_argmax", "man"]`                                    |   1.096 μs (5%) |         |                 |             |
| `["missing_argmax", "rf"]`                                     | 752.991 ns (5%) |         |                 |             |
| `["missing_argmax", "xf"]`                                     | 781.022 ns (5%) |         |   32 bytes (1%) |           1 |
| `["missing_dot", "equiv"]`                                     |   1.804 μs (5%) |         |   16 bytes (1%) |           1 |
| `["missing_dot", "man"]`                                       |   1.111 μs (5%) |         |   16 bytes (1%) |           1 |
| `["missing_dot", "naive"]`                                     |   2.737 μs (5%) |         |   16 bytes (1%) |           1 |
| `["missing_dot", "rf"]`                                        | 838.974 ns (5%) |         |   16 bytes (1%) |           1 |
| `["missing_dot", "rf_nota"]`                                   |   1.877 μs (5%) |         |   16 bytes (1%) |           1 |
| `["missing_dot", "xf"]`                                        |  67.567 μs (5%) |         |  72.02 KiB (1%) |        3736 |
| `["missing_dot", "xf_nota"]`                                   |  67.988 μs (5%) |         |  72.03 KiB (1%) |        3738 |
| `["overhead", "foldl"]`                                        |   2.795 ns (5%) |         |                 |             |
| `["overhead", "reduce_basecase"]`                              |  77.739 ns (5%) |         |   16 bytes (1%) |           1 |
| `["partition_by", "man"]`                                      |   1.856 ms (5%) |         |  480 bytes (1%) |           3 |
| `["partition_by", "xf"]`                                       |   2.178 ms (5%) |         |  592 bytes (1%) |           5 |
| `["set", "base"]`                                              |   2.808 ms (5%) |         |  49.14 KiB (1%) |          17 |
| `["set", "xf"]`                                                |   2.692 ms (5%) |         |  49.17 KiB (1%) |          19 |
| `["sum_transpose", "30", "noinit", "iter"]`                    |   2.752 μs (5%) |         |                 |             |
| `["sum_transpose", "30", "noinit", "man"]`                     |   3.145 μs (5%) |         |                 |             |
| `["sum_transpose", "30", "noinit", "xf"]`                      | 805.901 ns (5%) |         |                 |             |
| `["sum_transpose", "30", "withinit", "iter"]`                  |   1.006 μs (5%) |         |                 |             |
| `["sum_transpose", "30", "withinit", "man"]`                   | 805.132 ns (5%) |         |                 |             |
| `["sum_transpose", "30", "withinit", "xf"]`                    | 805.791 ns (5%) |         |                 |             |
| `["teerf_filter", "noinit"]`                                   | 291.104 ns (5%) |         |   80 bytes (1%) |           3 |
| `["teerf_filter", "withinit"]`                                 | 174.641 ns (5%) |         |                 |             |

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
  uname: Linux 6.2.0-1018-azure #18~22.04.1-Ubuntu SMP Tue Nov 21 19:25:02 UTC 2023 x86_64 x86_64
  CPU: AMD EPYC 7763 64-Core Processor: 
              speed         user         nice          sys         idle          irq
       #1  2445 MHz       1062 s          0 s        107 s       6744 s          0 s
       #2  3243 MHz       1638 s          0 s        113 s       6170 s          0 s
       #3  2606 MHz       2163 s          0 s        120 s       5631 s          0 s
       #4  3216 MHz       1645 s          0 s        112 s       6160 s          0 s
       
  Memory: 15.60690689086914 GB (12435.328125 MB free)
  Uptime: 795.42 sec
  Load Avg:  1.03  0.95  0.56
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-12.0.1 (ORCJIT, znver3)
```

---
# Baseline result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmark: 30 Jan 2024 - 1:25
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
| `["append!!", "eduction"]`                                     |  14.056 μs (5%) |         |  53.98 KiB (1%) |           8 |
| `["append!!", "xf"]`                                           |  13.946 μs (5%) |         |  53.98 KiB (1%) |           8 |
| `["cartesian", "copyto!", "iter"]`                             |   2.179 μs (5%) |         |                 |             |
| `["cartesian", "copyto!", "man"]`                              |   2.180 μs (5%) |         |                 |             |
| `["cartesian", "copyto!", "xf"]`                               |   1.566 μs (5%) |         |                 |             |
| `["cat", "base"]`                                              |   1.656 μs (5%) |         |                 |             |
| `["cat", "xf"]`                                                |   1.015 μs (5%) |         |                 |             |
| `["collect", "filter-missing"]`                                | 434.391 ns (5%) |         |   9.94 KiB (1%) |           1 |
| `["collect", "identity-float"]`                                |   4.161 μs (5%) |         |  78.17 KiB (1%) |           2 |
| `["collect", "identity-union"]`                                | 105.699 μs (5%) |         | 400.53 KiB (1%) |       10003 |
| `["dict", "base"]`                                             |   2.973 ms (5%) |         |  92.45 KiB (1%) |          22 |
| `["dict", "xf"]`                                               |   2.974 ms (5%) |         |  91.95 KiB (1%) |          18 |
| `["dot", "blas"]`                                              |   1.560 μs (5%) |         |                 |             |
| `["dot", "man"]`                                               |   1.553 μs (5%) |         |                 |             |
| `["dot", "rf"]`                                                |   1.572 μs (5%) |         |                 |             |
| `["dot", "xf"]`                                                |   1.574 μs (5%) |         |                 |             |
| `["filter_map_map!", "man"]`                                   |  47.369 μs (5%) |         |                 |             |
| `["filter_map_map!", "xf"]`                                    |  49.102 μs (5%) |         |                 |             |
| `["filter_map_reduce", "man"]`                                 | 154.289 μs (5%) |         |                 |             |
| `["filter_map_reduce", "xf"]`                                  | 154.290 μs (5%) |         |                 |             |
| `["filter_sum", "1000", "RandomFloats", "noinit", "base"]`     |   3.362 μs (5%) |         |                 |             |
| `["filter_sum", "1000", "RandomFloats", "noinit", "naive"]`    |   1.589 μs (5%) |         |                 |             |
| `["filter_sum", "1000", "RandomFloats", "noinit", "xf"]`       |   1.208 μs (5%) |         |                 |             |
| `["filter_sum", "1000", "RandomFloats", "withinit", "base"]`   |   1.214 μs (5%) |         |                 |             |
| `["filter_sum", "1000", "RandomFloats", "withinit", "naive"]`  | 662.063 ns (5%) |         |                 |             |
| `["filter_sum", "1000", "RandomFloats", "withinit", "xf"]`     |   1.210 μs (5%) |         |                 |             |
| `["filter_sum", "1000", "UnitRange", "noinit", "base"]`        | 626.491 ns (5%) |         |                 |             |
| `["filter_sum", "1000", "UnitRange", "noinit", "naive"]`       | 626.842 ns (5%) |         |                 |             |
| `["filter_sum", "1000", "UnitRange", "noinit", "xf"]`          | 165.776 ns (5%) |         |                 |             |
| `["filter_sum", "1000", "UnitRange", "withinit", "base"]`      | 115.330 ns (5%) |         |                 |             |
| `["filter_sum", "1000", "UnitRange", "withinit", "naive"]`     | 625.263 ns (5%) |         |                 |             |
| `["filter_sum", "1000", "UnitRange", "withinit", "xf"]`        | 113.978 ns (5%) |         |                 |             |
| `["filter_sum", "10000", "RandomFloats", "noinit", "base"]`    |  33.933 μs (5%) |         |                 |             |
| `["filter_sum", "10000", "RandomFloats", "noinit", "naive"]`   |  15.128 μs (5%) |         |                 |             |
| `["filter_sum", "10000", "RandomFloats", "noinit", "xf"]`      |  12.343 μs (5%) |         |                 |             |
| `["filter_sum", "10000", "RandomFloats", "withinit", "base"]`  |  12.343 μs (5%) |         |                 |             |
| `["filter_sum", "10000", "RandomFloats", "withinit", "naive"]` |   9.571 μs (5%) |         |                 |             |
| `["filter_sum", "10000", "RandomFloats", "withinit", "xf"]`    |  12.343 μs (5%) |         |                 |             |
| `["filter_sum", "10000", "UnitRange", "noinit", "base"]`       |   6.179 μs (5%) |         |                 |             |
| `["filter_sum", "10000", "UnitRange", "noinit", "naive"]`      |   6.181 μs (5%) |         |                 |             |
| `["filter_sum", "10000", "UnitRange", "noinit", "xf"]`         |   1.637 μs (5%) |         |                 |             |
| `["filter_sum", "10000", "UnitRange", "withinit", "base"]`     |   1.125 μs (5%) |         |                 |             |
| `["filter_sum", "10000", "UnitRange", "withinit", "naive"]`    |   6.177 μs (5%) |         |                 |             |
| `["filter_sum", "10000", "UnitRange", "withinit", "xf"]`       |   1.121 μs (5%) |         |                 |             |
| `["findall", "base"]`                                          | 109.084 μs (5%) |         | 797.20 KiB (1%) |           8 |
| `["findall", "xf-array"]`                                      | 986.320 μs (5%) |         |   2.94 MiB (1%) |       96426 |
| `["findall", "xf-iter"]`                                       | 654.918 μs (5%) |         |   1.83 MiB (1%) |          14 |
| `["gemm", "fusedmul", "blas", "16"]`                           |   2.588 ms (5%) |         |                 |             |
| `["gemm", "fusedmul", "blas", "2"]`                            |   1.825 ms (5%) |         |                 |             |
| `["gemm", "fusedmul", "blas", "32"]`                           |   3.930 ms (5%) |         |                 |             |
| `["gemm", "fusedmul", "blas", "8"]`                            |   1.866 ms (5%) |         |                 |             |
| `["gemm", "fusedmul", "xf", "16"]`                             |   2.465 ms (5%) |         |  192 bytes (1%) |           4 |
| `["gemm", "fusedmul", "xf", "2"]`                              | 324.420 μs (5%) |         |  192 bytes (1%) |           4 |
| `["gemm", "fusedmul", "xf", "32"]`                             |   4.809 ms (5%) |         |  192 bytes (1%) |           4 |
| `["gemm", "fusedmul", "xf", "8"]`                              |   1.238 ms (5%) |         |  192 bytes (1%) |           4 |
| `["gemm", "mul", "linalg", "256"]`                             | 769.343 μs (5%) |         |                 |             |
| `["gemm", "mul", "linalg", "32"]`                              |   2.875 μs (5%) |         |                 |             |
| `["gemm", "mul", "linalg", "8"]`                               | 240.000 ns (5%) |         |                 |             |
| `["gemm", "mul", "man", "false", "256"]`                       |   2.130 ms (5%) |         |                 |             |
| `["gemm", "mul", "man", "false", "32"]`                        |   5.130 μs (5%) |         |                 |             |
| `["gemm", "mul", "man", "false", "8"]`                         | 320.000 ns (5%) |         |                 |             |
| `["gemm", "mul", "man", "ivdep", "256"]`                       |   2.078 ms (5%) |         |                 |             |
| `["gemm", "mul", "man", "ivdep", "32"]`                        |   4.548 μs (5%) |         |                 |             |
| `["gemm", "mul", "man", "ivdep", "8"]`                         | 310.000 ns (5%) |         |                 |             |
| `["gemm", "mul", "man", "true", "256"]`                        |   2.105 ms (5%) |         |                 |             |
| `["gemm", "mul", "man", "true", "32"]`                         |   4.959 μs (5%) |         |                 |             |
| `["gemm", "mul", "man", "true", "8"]`                          | 330.000 ns (5%) |         |                 |             |
| `["gemm", "mul", "xf", "false", "256"]`                        |   2.075 ms (5%) |         |   80 bytes (1%) |           3 |
| `["gemm", "mul", "xf", "false", "32"]`                         |   5.480 μs (5%) |         |   80 bytes (1%) |           3 |
| `["gemm", "mul", "xf", "false", "8"]`                          | 380.000 ns (5%) |         |   80 bytes (1%) |           3 |
| `["gemm", "mul", "xf", "ivdep", "256"]`                        |   2.101 ms (5%) |         |   80 bytes (1%) |           3 |
| `["gemm", "mul", "xf", "ivdep", "32"]`                         |   4.578 μs (5%) |         |   80 bytes (1%) |           3 |
| `["gemm", "mul", "xf", "ivdep", "8"]`                          | 350.000 ns (5%) |         |   80 bytes (1%) |           3 |
| `["gemm", "mul", "xf", "true", "256"]`                         |   2.071 ms (5%) |         |   80 bytes (1%) |           3 |
| `["gemm", "mul", "xf", "true", "32"]`                          |   4.799 μs (5%) |         |   80 bytes (1%) |           3 |
| `["gemm", "mul", "xf", "true", "8"]`                           | 370.000 ns (5%) |         |   80 bytes (1%) |           3 |
| `["groupby", "sum", "sac"]`                                    |   6.659 ms (5%) |         |  13.14 KiB (1%) |         103 |
| `["groupby", "sum", "xf-with-init"]`                           |  99.587 μs (5%) |         |   1.05 KiB (1%) |           9 |
| `["groupby", "sum", "xf-without-init"]`                        |  94.607 μs (5%) |         |   1.05 KiB (1%) |           9 |
| `["mapcat_eduction", "base"]`                                  |  31.670 μs (5%) |         |                 |             |
| `["mapcat_eduction", "xf-eduction"]`                           |   1.015 μs (5%) |         |                 |             |
| `["mapcat_eduction", "xf-xf"]`                                 |   1.016 μs (5%) |         |                 |             |
| `["missing_argmax", "man"]`                                    |   1.099 μs (5%) |         |                 |             |
| `["missing_argmax", "rf"]`                                     | 756.851 ns (5%) |         |                 |             |
| `["missing_argmax", "xf"]`                                     | 769.111 ns (5%) |         |   32 bytes (1%) |           1 |
| `["missing_dot", "equiv"]`                                     |   1.814 μs (5%) |         |   16 bytes (1%) |           1 |
| `["missing_dot", "man"]`                                       | 915.917 ns (5%) |         |   16 bytes (1%) |           1 |
| `["missing_dot", "naive"]`                                     |   2.759 μs (5%) |         |   16 bytes (1%) |           1 |
| `["missing_dot", "rf"]`                                        |   1.016 μs (5%) |         |   16 bytes (1%) |           1 |
| `["missing_dot", "rf_nota"]`                                   |   1.791 μs (5%) |         |   16 bytes (1%) |           1 |
| `["missing_dot", "xf"]`                                        |  67.386 μs (5%) |         |  71.91 KiB (1%) |        3730 |
| `["missing_dot", "xf_nota"]`                                   |  67.416 μs (5%) |         |  72.23 KiB (1%) |        3746 |
| `["overhead", "foldl"]`                                        |   2.795 ns (5%) |         |                 |             |
| `["overhead", "reduce_basecase"]`                              |  76.059 ns (5%) |         |   16 bytes (1%) |           1 |
| `["partition_by", "man"]`                                      |   1.865 ms (5%) |         |  480 bytes (1%) |           3 |
| `["partition_by", "xf"]`                                       |   2.184 ms (5%) |         |  592 bytes (1%) |           5 |
| `["set", "base"]`                                              |   2.671 ms (5%) |         |  49.14 KiB (1%) |          17 |
| `["set", "xf"]`                                                |   2.675 ms (5%) |         |  49.17 KiB (1%) |          19 |
| `["sum_transpose", "30", "noinit", "iter"]`                    |   2.751 μs (5%) |         |                 |             |
| `["sum_transpose", "30", "noinit", "man"]`                     |   3.145 μs (5%) |         |                 |             |
| `["sum_transpose", "30", "noinit", "xf"]`                      | 807.560 ns (5%) |         |                 |             |
| `["sum_transpose", "30", "withinit", "iter"]`                  | 992.800 ns (5%) |         |                 |             |
| `["sum_transpose", "30", "withinit", "man"]`                   | 804.692 ns (5%) |         |                 |             |
| `["sum_transpose", "30", "withinit", "xf"]`                    | 805.791 ns (5%) |         |                 |             |
| `["teerf_filter", "noinit"]`                                   | 294.193 ns (5%) |         |   80 bytes (1%) |           3 |
| `["teerf_filter", "withinit"]`                                 | 174.420 ns (5%) |         |                 |             |

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
  uname: Linux 6.2.0-1018-azure #18~22.04.1-Ubuntu SMP Tue Nov 21 19:25:02 UTC 2023 x86_64 x86_64
  CPU: AMD EPYC 7763 64-Core Processor: 
              speed         user         nice          sys         idle          irq
       #1  3193 MHz       2043 s          0 s        124 s       8283 s          0 s
       #2  2565 MHz       2042 s          0 s        134 s       8282 s          0 s
       #3  2445 MHz       2523 s          0 s        146 s       7781 s          0 s
       #4  3243 MHz       2468 s          0 s        153 s       7833 s          0 s
       
  Memory: 15.60690689086914 GB (12382.2265625 MB free)
  Uptime: 1049.52 sec
  Load Avg:  1.01  1.03  0.7
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-12.0.1 (ORCJIT, znver3)
```

---
# Runtime information
| Runtime Info | |
|:--|:--|
| BLAS #threads | 4 |
| `BLAS.vendor()` | `openblas64` |
| `Sys.CPU_THREADS` | 4 |

`lscpu` output:

    Architecture:                       x86_64
    CPU op-mode(s):                     32-bit, 64-bit
    Address sizes:                      48 bits physical, 48 bits virtual
    Byte Order:                         Little Endian
    CPU(s):                             4
    On-line CPU(s) list:                0-3
    Vendor ID:                          AuthenticAMD
    Model name:                         AMD EPYC 7763 64-Core Processor
    CPU family:                         25
    Model:                              1
    Thread(s) per core:                 2
    Core(s) per socket:                 2
    Socket(s):                          1
    Stepping:                           1
    BogoMIPS:                           4890.86
    Flags:                              fpu vme de pse tsc msr pae mce cx8 apic sep mtrr pge mca cmov pat pse36 clflush mmx fxsr sse sse2 ht syscall nx mmxext fxsr_opt pdpe1gb rdtscp lm constant_tsc rep_good nopl tsc_reliable nonstop_tsc cpuid extd_apicid aperfmperf pni pclmulqdq ssse3 fma cx16 pcid sse4_1 sse4_2 movbe popcnt aes xsave avx f16c rdrand hypervisor lahf_lm cmp_legacy svm cr8_legacy abm sse4a misalignsse 3dnowprefetch osvw topoext invpcid_single vmmcall fsgsbase bmi1 avx2 smep bmi2 erms invpcid rdseed adx smap clflushopt clwb sha_ni xsaveopt xsavec xgetbv1 xsaves clzero xsaveerptr rdpru arat npt nrip_save tsc_scale vmcb_clean flushbyasid decodeassists pausefilter pfthreshold v_vmsave_vmload umip vaes vpclmulqdq rdpid fsrm
    Virtualization:                     AMD-V
    Hypervisor vendor:                  Microsoft
    Virtualization type:                full
    L1d cache:                          64 KiB (2 instances)
    L1i cache:                          64 KiB (2 instances)
    L2 cache:                           1 MiB (2 instances)
    L3 cache:                           32 MiB (1 instance)
    NUMA node(s):                       1
    NUMA node0 CPU(s):                  0-3
    Vulnerability Gather data sampling: Not affected
    Vulnerability Itlb multihit:        Not affected
    Vulnerability L1tf:                 Not affected
    Vulnerability Mds:                  Not affected
    Vulnerability Meltdown:             Not affected
    Vulnerability Mmio stale data:      Not affected
    Vulnerability Retbleed:             Not affected
    Vulnerability Spec rstack overflow: Mitigation; safe RET, no microcode
    Vulnerability Spec store bypass:    Vulnerable
    Vulnerability Spectre v1:           Mitigation; usercopy/swapgs barriers and __user pointer sanitization
    Vulnerability Spectre v2:           Mitigation; Retpolines, STIBP disabled, RSB filling, PBRSB-eIBRS Not affected
    Vulnerability Srbds:                Not affected
    Vulnerability Tsx async abort:      Not affected
    

| Cpu Property       | Value                                                      |
|:------------------ |:---------------------------------------------------------- |
| Brand              | AMD EPYC 7763 64-Core Processor                            |
| Vendor             | :AMD                                                       |
| Architecture       | :Unknown                                                   |
| Model              | Family: 0xaf, Model: 0x01, Stepping: 0x01, Type: 0x00      |
| Cores              | 16 physical cores, 16 logical cores (on executing CPU)     |
|                    | No Hyperthreading hardware capability detected             |
| Clock Frequencies  | Not supported by CPU                                       |
| Data Cache         | Level 1:3 : (32, 512, 32768) kbytes                        |
|                    | 64 byte cache line size                                    |
| Address Size       | 48 bits virtual, 48 bits physical                          |
| SIMD               | 256 bit = 32 byte max. SIMD vector size                    |
| Time Stamp Counter | TSC is accessible via `rdtsc`                              |
|                    | TSC runs at constant rate (invariant from clock frequency) |
| Perf. Monitoring   | Performance Monitoring Counters (PMC) are not supported    |
| Hypervisor         | Yes, Microsoft                                             |

