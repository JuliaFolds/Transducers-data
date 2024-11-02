# Benchmark result

* Pull request commit: [`dd5d98a0befa1399bcfc1aa114a483ded2fe8a70`](https://github.com/JuliaFolds/Transducers.jl/commit/dd5d98a0befa1399bcfc1aa114a483ded2fe8a70)
* Pull request: <https://github.com/JuliaFolds/Transducers.jl/pull/243> (Update */Manifest.toml)

# Judge result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmarks:
    - Target: 2 Nov 2024 - 01:50
    - Baseline: 2 Nov 2024 - 01:54
* Package commits:
    - Target: b74cbf
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
| `["collect", "identity-float"]`                                |                1.06 (5%) :x: |                   1.00 (1%)  |
| `["filter_sum", "1000", "RandomFloats", "withinit", "naive"]`  | 0.95 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["filter_sum", "10000", "RandomFloats", "withinit", "naive"]` | 0.95 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["gemm", "mul", "linalg", "8"]`                               | 0.72 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["gemm", "mul", "man", "false", "256"]`                       |                1.06 (5%) :x: |                   1.00 (1%)  |
| `["gemm", "mul", "man", "false", "32"]`                        | 0.95 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["gemm", "mul", "man", "false", "8"]`                         | 0.88 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["gemm", "mul", "man", "ivdep", "256"]`                       |                1.07 (5%) :x: |                   1.00 (1%)  |
| `["gemm", "mul", "man", "ivdep", "8"]`                         | 0.87 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["gemm", "mul", "man", "true", "8"]`                          | 0.68 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["gemm", "mul", "xf", "false", "8"]`                          | 0.88 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["gemm", "mul", "xf", "ivdep", "256"]`                        |                1.05 (5%) :x: |                   1.00 (1%)  |
| `["gemm", "mul", "xf", "ivdep", "8"]`                          | 0.72 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["gemm", "mul", "xf", "true", "8"]`                           | 0.87 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["groupby", "sum", "sac"]`                                    | 0.01 (5%) :white_check_mark: | 0.12 (1%) :white_check_mark: |
| `["groupby", "sum", "xf-without-init"]`                        | 0.93 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["missing_argmax", "rf"]`                                     | 0.91 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["missing_dot", "equiv"]`                                     | 0.95 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["missing_dot", "rf"]`                                        |                1.21 (5%) :x: |                   1.00 (1%)  |
| `["overhead", "foldl"]`                                        | 0.90 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["set", "base"]`                                              | 0.95 (5%) :white_check_mark: |                   1.00 (1%)  |

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
      Ubuntu 22.04.5 LTS
  uname: Linux 6.5.0-1025-azure #26~22.04.1-Ubuntu SMP Thu Jul 11 22:33:04 UTC 2024 x86_64 x86_64
  CPU: AMD EPYC 7763 64-Core Processor: 
              speed         user         nice          sys         idle          irq
       #1  2445 MHz       1776 s          0 s        111 s       5588 s          0 s
       #2  2445 MHz       1782 s          0 s         99 s       5590 s          0 s
       #3  3267 MHz       1236 s          0 s        119 s       6119 s          0 s
       #4  3244 MHz       1675 s          0 s        113 s       5691 s          0 s
       
  Memory: 15.606491088867188 GB (12468.84375 MB free)
  Uptime: 750.47 sec
  Load Avg:  1.02  0.93  0.55
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
      Ubuntu 22.04.5 LTS
  uname: Linux 6.5.0-1025-azure #26~22.04.1-Ubuntu SMP Thu Jul 11 22:33:04 UTC 2024 x86_64 x86_64
  CPU: AMD EPYC 7763 64-Core Processor: 
              speed         user         nice          sys         idle          irq
       #1  3256 MHz       2191 s          0 s        132 s       7685 s          0 s
       #2  3243 MHz       2492 s          0 s        119 s       7395 s          0 s
       #3  3246 MHz       1858 s          0 s        145 s       8007 s          0 s
       #4  3163 MHz       2509 s          0 s        150 s       7356 s          0 s
       
  Memory: 15.606491088867188 GB (12385.22265625 MB free)
  Uptime: 1004.38 sec
  Load Avg:  1.03  1.01  0.69
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-12.0.1 (ORCJIT, znver3)
```

---
# Target result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmark: 2 Nov 2024 - 1:50
* Package commit: b74cbf
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
| `["append!!", "eduction"]`                                     |  14.327 μs (5%) |         |  53.98 KiB (1%) |           8 |
| `["append!!", "xf"]`                                           |  14.035 μs (5%) |         |  53.98 KiB (1%) |           8 |
| `["cartesian", "copyto!", "iter"]`                             |   1.567 μs (5%) |         |                 |             |
| `["cartesian", "copyto!", "man"]`                              |   1.566 μs (5%) |         |                 |             |
| `["cartesian", "copyto!", "xf"]`                               |   1.567 μs (5%) |         |                 |             |
| `["cat", "base"]`                                              |   1.737 μs (5%) |         |                 |             |
| `["cat", "xf"]`                                                |   1.016 μs (5%) |         |                 |             |
| `["collect", "filter-missing"]`                                | 449.267 ns (5%) |         |   9.94 KiB (1%) |           1 |
| `["collect", "identity-float"]`                                |   2.853 μs (5%) |         |  78.17 KiB (1%) |           2 |
| `["collect", "identity-union"]`                                | 104.914 μs (5%) |         | 400.53 KiB (1%) |       10003 |
| `["dict", "base"]`                                             |   2.973 ms (5%) |         |  92.45 KiB (1%) |          22 |
| `["dict", "xf"]`                                               |   2.974 ms (5%) |         |  91.95 KiB (1%) |          18 |
| `["dot", "blas"]`                                              |   1.560 μs (5%) |         |                 |             |
| `["dot", "man"]`                                               |   1.554 μs (5%) |         |                 |             |
| `["dot", "rf"]`                                                |   1.575 μs (5%) |         |                 |             |
| `["dot", "xf"]`                                                |   1.572 μs (5%) |         |                 |             |
| `["filter_map_map!", "man"]`                                   |  47.709 μs (5%) |         |                 |             |
| `["filter_map_map!", "xf"]`                                    |  47.879 μs (5%) |         |                 |             |
| `["filter_map_reduce", "man"]`                                 | 154.306 μs (5%) |         |                 |             |
| `["filter_map_reduce", "xf"]`                                  | 154.306 μs (5%) |         |                 |             |
| `["filter_sum", "1000", "RandomFloats", "noinit", "base"]`     |   3.361 μs (5%) |         |                 |             |
| `["filter_sum", "1000", "RandomFloats", "noinit", "naive"]`    |   1.590 μs (5%) |         |                 |             |
| `["filter_sum", "1000", "RandomFloats", "noinit", "xf"]`       |   1.208 μs (5%) |         |                 |             |
| `["filter_sum", "1000", "RandomFloats", "withinit", "base"]`   |   1.210 μs (5%) |         |                 |             |
| `["filter_sum", "1000", "RandomFloats", "withinit", "naive"]`  | 574.262 ns (5%) |         |                 |             |
| `["filter_sum", "1000", "RandomFloats", "withinit", "xf"]`     |   1.214 μs (5%) |         |                 |             |
| `["filter_sum", "1000", "UnitRange", "noinit", "base"]`        | 626.187 ns (5%) |         |                 |             |
| `["filter_sum", "1000", "UnitRange", "noinit", "naive"]`       | 626.830 ns (5%) |         |                 |             |
| `["filter_sum", "1000", "UnitRange", "noinit", "xf"]`          | 163.889 ns (5%) |         |                 |             |
| `["filter_sum", "1000", "UnitRange", "withinit", "base"]`      | 113.794 ns (5%) |         |                 |             |
| `["filter_sum", "1000", "UnitRange", "withinit", "naive"]`     | 625.246 ns (5%) |         |                 |             |
| `["filter_sum", "1000", "UnitRange", "withinit", "xf"]`        | 113.662 ns (5%) |         |                 |             |
| `["filter_sum", "10000", "RandomFloats", "noinit", "base"]`    |  33.923 μs (5%) |         |                 |             |
| `["filter_sum", "10000", "RandomFloats", "noinit", "naive"]`   |  15.098 μs (5%) |         |                 |             |
| `["filter_sum", "10000", "RandomFloats", "noinit", "xf"]`      |  12.342 μs (5%) |         |                 |             |
| `["filter_sum", "10000", "RandomFloats", "withinit", "base"]`  |  12.343 μs (5%) |         |                 |             |
| `["filter_sum", "10000", "RandomFloats", "withinit", "naive"]` |   8.439 μs (5%) |         |                 |             |
| `["filter_sum", "10000", "RandomFloats", "withinit", "xf"]`    |  12.342 μs (5%) |         |                 |             |
| `["filter_sum", "10000", "UnitRange", "noinit", "base"]`       |   6.181 μs (5%) |         |                 |             |
| `["filter_sum", "10000", "UnitRange", "noinit", "naive"]`      |   6.181 μs (5%) |         |                 |             |
| `["filter_sum", "10000", "UnitRange", "noinit", "xf"]`         |   1.630 μs (5%) |         |                 |             |
| `["filter_sum", "10000", "UnitRange", "withinit", "base"]`     |   1.124 μs (5%) |         |                 |             |
| `["filter_sum", "10000", "UnitRange", "withinit", "naive"]`    |   6.177 μs (5%) |         |                 |             |
| `["filter_sum", "10000", "UnitRange", "withinit", "xf"]`       |   1.123 μs (5%) |         |                 |             |
| `["findall", "base"]`                                          | 109.242 μs (5%) |         | 797.20 KiB (1%) |           8 |
| `["findall", "xf-array"]`                                      | 985.987 μs (5%) |         |   2.94 MiB (1%) |       96426 |
| `["findall", "xf-iter"]`                                       | 689.938 μs (5%) |         |   1.83 MiB (1%) |          14 |
| `["gemm", "fusedmul", "blas", "16"]`                           |   2.454 ms (5%) |         |                 |             |
| `["gemm", "fusedmul", "blas", "2"]`                            |   1.631 ms (5%) |         |                 |             |
| `["gemm", "fusedmul", "blas", "32"]`                           |   3.996 ms (5%) |         |                 |             |
| `["gemm", "fusedmul", "blas", "8"]`                            |   1.714 ms (5%) |         |                 |             |
| `["gemm", "fusedmul", "xf", "16"]`                             |   2.579 ms (5%) |         |  192 bytes (1%) |           4 |
| `["gemm", "fusedmul", "xf", "2"]`                              | 321.176 μs (5%) |         |  192 bytes (1%) |           4 |
| `["gemm", "fusedmul", "xf", "32"]`                             |   5.177 ms (5%) |         |  192 bytes (1%) |           4 |
| `["gemm", "fusedmul", "xf", "8"]`                              |   1.297 ms (5%) |         |  192 bytes (1%) |           4 |
| `["gemm", "mul", "linalg", "256"]`                             | 769.377 μs (5%) |         |                 |             |
| `["gemm", "mul", "linalg", "32"]`                              |   2.829 μs (5%) |         |                 |             |
| `["gemm", "mul", "linalg", "8"]`                               | 171.888 ns (5%) |         |                 |             |
| `["gemm", "mul", "man", "false", "256"]`                       |   2.217 ms (5%) |         |                 |             |
| `["gemm", "mul", "man", "false", "32"]`                        |   5.258 μs (5%) |         |                 |             |
| `["gemm", "mul", "man", "false", "8"]`                         | 289.786 ns (5%) |         |                 |             |
| `["gemm", "mul", "man", "ivdep", "256"]`                       |   2.226 ms (5%) |         |                 |             |
| `["gemm", "mul", "man", "ivdep", "32"]`                        |   4.538 μs (5%) |         |                 |             |
| `["gemm", "mul", "man", "ivdep", "8"]`                         | 277.066 ns (5%) |         |                 |             |
| `["gemm", "mul", "man", "true", "256"]`                        |   2.219 ms (5%) |         |                 |             |
| `["gemm", "mul", "man", "true", "32"]`                         |   4.966 μs (5%) |         |                 |             |
| `["gemm", "mul", "man", "true", "8"]`                          | 291.295 ns (5%) |         |                 |             |
| `["gemm", "mul", "xf", "false", "256"]`                        |   2.214 ms (5%) |         |   80 bytes (1%) |           3 |
| `["gemm", "mul", "xf", "false", "32"]`                         |   5.585 μs (5%) |         |   80 bytes (1%) |           3 |
| `["gemm", "mul", "xf", "false", "8"]`                          | 350.038 ns (5%) |         |   80 bytes (1%) |           3 |
| `["gemm", "mul", "xf", "ivdep", "256"]`                        |   2.223 ms (5%) |         |   80 bytes (1%) |           3 |
| `["gemm", "mul", "xf", "ivdep", "32"]`                         |   4.551 μs (5%) |         |   80 bytes (1%) |           3 |
| `["gemm", "mul", "xf", "ivdep", "8"]`                          | 326.175 ns (5%) |         |   80 bytes (1%) |           3 |
| `["gemm", "mul", "xf", "true", "256"]`                         |   2.213 ms (5%) |         |   80 bytes (1%) |           3 |
| `["gemm", "mul", "xf", "true", "32"]`                          |   4.981 μs (5%) |         |   80 bytes (1%) |           3 |
| `["gemm", "mul", "xf", "true", "8"]`                           | 331.196 ns (5%) |         |   80 bytes (1%) |           3 |
| `["groupby", "sum", "sac"]`                                    |  94.164 μs (5%) |         |   1.64 KiB (1%) |          11 |
| `["groupby", "sum", "xf-with-init"]`                           |  95.788 μs (5%) |         |   1.05 KiB (1%) |           9 |
| `["groupby", "sum", "xf-without-init"]`                        |  93.273 μs (5%) |         |   1.05 KiB (1%) |           9 |
| `["mapcat_eduction", "base"]`                                  |  31.789 μs (5%) |         |                 |             |
| `["mapcat_eduction", "xf-eduction"]`                           |   1.016 μs (5%) |         |                 |             |
| `["mapcat_eduction", "xf-xf"]`                                 |   1.016 μs (5%) |         |                 |             |
| `["missing_argmax", "man"]`                                    |   1.095 μs (5%) |         |                 |             |
| `["missing_argmax", "rf"]`                                     | 705.798 ns (5%) |         |                 |             |
| `["missing_argmax", "xf"]`                                     | 781.252 ns (5%) |         |   32 bytes (1%) |           1 |
| `["missing_dot", "equiv"]`                                     |   1.816 μs (5%) |         |   16 bytes (1%) |           1 |
| `["missing_dot", "man"]`                                       | 833.364 ns (5%) |         |   16 bytes (1%) |           1 |
| `["missing_dot", "naive"]`                                     |   2.753 μs (5%) |         |   16 bytes (1%) |           1 |
| `["missing_dot", "rf"]`                                        |   1.133 μs (5%) |         |   16 bytes (1%) |           1 |
| `["missing_dot", "rf_nota"]`                                   |   1.790 μs (5%) |         |   16 bytes (1%) |           1 |
| `["missing_dot", "xf"]`                                        |  68.046 μs (5%) |         |  72.30 KiB (1%) |        3748 |
| `["missing_dot", "xf_nota"]`                                   |  68.588 μs (5%) |         |  72.12 KiB (1%) |        3738 |
| `["overhead", "foldl"]`                                        |   2.794 ns (5%) |         |                 |             |
| `["overhead", "reduce_basecase"]`                              |  76.861 ns (5%) |         |   16 bytes (1%) |           1 |
| `["partition_by", "man"]`                                      |   1.859 ms (5%) |         |  480 bytes (1%) |           3 |
| `["partition_by", "xf"]`                                       |   2.185 ms (5%) |         |  592 bytes (1%) |           5 |
| `["set", "base"]`                                              |   2.672 ms (5%) |         |  49.14 KiB (1%) |          17 |
| `["set", "xf"]`                                                |   2.677 ms (5%) |         |  49.17 KiB (1%) |          19 |
| `["sum_transpose", "30", "noinit", "iter"]`                    |   2.751 μs (5%) |         |                 |             |
| `["sum_transpose", "30", "noinit", "man"]`                     |   3.144 μs (5%) |         |                 |             |
| `["sum_transpose", "30", "noinit", "xf"]`                      | 805.879 ns (5%) |         |                 |             |
| `["sum_transpose", "30", "withinit", "iter"]`                  | 866.466 ns (5%) |         |                 |             |
| `["sum_transpose", "30", "withinit", "man"]`                   | 805.110 ns (5%) |         |                 |             |
| `["sum_transpose", "30", "withinit", "xf"]`                    | 805.659 ns (5%) |         |                 |             |
| `["teerf_filter", "noinit"]`                                   | 293.665 ns (5%) |         |   80 bytes (1%) |           3 |
| `["teerf_filter", "withinit"]`                                 | 172.286 ns (5%) |         |                 |             |

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
      Ubuntu 22.04.5 LTS
  uname: Linux 6.5.0-1025-azure #26~22.04.1-Ubuntu SMP Thu Jul 11 22:33:04 UTC 2024 x86_64 x86_64
  CPU: AMD EPYC 7763 64-Core Processor: 
              speed         user         nice          sys         idle          irq
       #1  2445 MHz       1776 s          0 s        111 s       5588 s          0 s
       #2  2445 MHz       1782 s          0 s         99 s       5590 s          0 s
       #3  3267 MHz       1236 s          0 s        119 s       6119 s          0 s
       #4  3244 MHz       1675 s          0 s        113 s       5691 s          0 s
       
  Memory: 15.606491088867188 GB (12468.84375 MB free)
  Uptime: 750.47 sec
  Load Avg:  1.02  0.93  0.55
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-12.0.1 (ORCJIT, znver3)
```

---
# Baseline result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmark: 2 Nov 2024 - 1:54
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
| `["append!!", "eduction"]`                                     |  13.805 μs (5%) |         |  53.98 KiB (1%) |           8 |
| `["append!!", "xf"]`                                           |  13.725 μs (5%) |         |  53.98 KiB (1%) |           8 |
| `["cartesian", "copyto!", "iter"]`                             |   1.566 μs (5%) |         |                 |             |
| `["cartesian", "copyto!", "man"]`                              |   1.568 μs (5%) |         |                 |             |
| `["cartesian", "copyto!", "xf"]`                               |   1.635 μs (5%) |         |                 |             |
| `["cat", "base"]`                                              |   1.762 μs (5%) |         |                 |             |
| `["cat", "xf"]`                                                |   1.016 μs (5%) |         |                 |             |
| `["collect", "filter-missing"]`                                | 464.215 ns (5%) |         |   9.94 KiB (1%) |           1 |
| `["collect", "identity-float"]`                                |   2.691 μs (5%) |         |  78.17 KiB (1%) |           2 |
| `["collect", "identity-union"]`                                | 104.254 μs (5%) |         | 400.53 KiB (1%) |       10003 |
| `["dict", "base"]`                                             |   2.974 ms (5%) |         |  92.45 KiB (1%) |          22 |
| `["dict", "xf"]`                                               |   2.975 ms (5%) |         |  91.95 KiB (1%) |          18 |
| `["dot", "blas"]`                                              |   1.560 μs (5%) |         |                 |             |
| `["dot", "man"]`                                               |   1.554 μs (5%) |         |                 |             |
| `["dot", "rf"]`                                                |   1.575 μs (5%) |         |                 |             |
| `["dot", "xf"]`                                                |   1.572 μs (5%) |         |                 |             |
| `["filter_map_map!", "man"]`                                   |  47.448 μs (5%) |         |                 |             |
| `["filter_map_map!", "xf"]`                                    |  49.963 μs (5%) |         |                 |             |
| `["filter_map_reduce", "man"]`                                 | 154.307 μs (5%) |         |                 |             |
| `["filter_map_reduce", "xf"]`                                  | 154.306 μs (5%) |         |                 |             |
| `["filter_sum", "1000", "RandomFloats", "noinit", "base"]`     |   3.361 μs (5%) |         |                 |             |
| `["filter_sum", "1000", "RandomFloats", "noinit", "naive"]`    |   1.590 μs (5%) |         |                 |             |
| `["filter_sum", "1000", "RandomFloats", "noinit", "xf"]`       |   1.208 μs (5%) |         |                 |             |
| `["filter_sum", "1000", "RandomFloats", "withinit", "base"]`   |   1.210 μs (5%) |         |                 |             |
| `["filter_sum", "1000", "RandomFloats", "withinit", "naive"]`  | 604.674 ns (5%) |         |                 |             |
| `["filter_sum", "1000", "RandomFloats", "withinit", "xf"]`     |   1.214 μs (5%) |         |                 |             |
| `["filter_sum", "1000", "UnitRange", "noinit", "base"]`        | 626.193 ns (5%) |         |                 |             |
| `["filter_sum", "1000", "UnitRange", "noinit", "naive"]`       | 626.836 ns (5%) |         |                 |             |
| `["filter_sum", "1000", "UnitRange", "noinit", "xf"]`          | 164.086 ns (5%) |         |                 |             |
| `["filter_sum", "1000", "UnitRange", "withinit", "base"]`      | 114.111 ns (5%) |         |                 |             |
| `["filter_sum", "1000", "UnitRange", "withinit", "naive"]`     | 625.251 ns (5%) |         |                 |             |
| `["filter_sum", "1000", "UnitRange", "withinit", "xf"]`        | 113.718 ns (5%) |         |                 |             |
| `["filter_sum", "10000", "RandomFloats", "noinit", "base"]`    |  33.932 μs (5%) |         |                 |             |
| `["filter_sum", "10000", "RandomFloats", "noinit", "naive"]`   |  15.108 μs (5%) |         |                 |             |
| `["filter_sum", "10000", "RandomFloats", "noinit", "xf"]`      |  12.342 μs (5%) |         |                 |             |
| `["filter_sum", "10000", "RandomFloats", "withinit", "base"]`  |  12.343 μs (5%) |         |                 |             |
| `["filter_sum", "10000", "RandomFloats", "withinit", "naive"]` |   8.883 μs (5%) |         |                 |             |
| `["filter_sum", "10000", "RandomFloats", "withinit", "xf"]`    |  12.342 μs (5%) |         |                 |             |
| `["filter_sum", "10000", "UnitRange", "noinit", "base"]`       |   6.179 μs (5%) |         |                 |             |
| `["filter_sum", "10000", "UnitRange", "noinit", "naive"]`      |   6.183 μs (5%) |         |                 |             |
| `["filter_sum", "10000", "UnitRange", "noinit", "xf"]`         |   1.630 μs (5%) |         |                 |             |
| `["filter_sum", "10000", "UnitRange", "withinit", "base"]`     |   1.125 μs (5%) |         |                 |             |
| `["filter_sum", "10000", "UnitRange", "withinit", "naive"]`    |   6.179 μs (5%) |         |                 |             |
| `["filter_sum", "10000", "UnitRange", "withinit", "xf"]`       |   1.123 μs (5%) |         |                 |             |
| `["findall", "base"]`                                          | 108.742 μs (5%) |         | 797.20 KiB (1%) |           8 |
| `["findall", "xf-array"]`                                      | 981.817 μs (5%) |         |   2.94 MiB (1%) |       96426 |
| `["findall", "xf-iter"]`                                       | 688.651 μs (5%) |         |   1.83 MiB (1%) |          14 |
| `["gemm", "fusedmul", "blas", "16"]`                           |   2.467 ms (5%) |         |                 |             |
| `["gemm", "fusedmul", "blas", "2"]`                            |   1.632 ms (5%) |         |                 |             |
| `["gemm", "fusedmul", "blas", "32"]`                           |   3.978 ms (5%) |         |                 |             |
| `["gemm", "fusedmul", "blas", "8"]`                            |   1.711 ms (5%) |         |                 |             |
| `["gemm", "fusedmul", "xf", "16"]`                             |   2.568 ms (5%) |         |  192 bytes (1%) |           4 |
| `["gemm", "fusedmul", "xf", "2"]`                              | 326.738 μs (5%) |         |  192 bytes (1%) |           4 |
| `["gemm", "fusedmul", "xf", "32"]`                             |   5.174 ms (5%) |         |  192 bytes (1%) |           4 |
| `["gemm", "fusedmul", "xf", "8"]`                              |   1.291 ms (5%) |         |  192 bytes (1%) |           4 |
| `["gemm", "mul", "linalg", "256"]`                             | 776.625 μs (5%) |         |                 |             |
| `["gemm", "mul", "linalg", "32"]`                              |   2.885 μs (5%) |         |                 |             |
| `["gemm", "mul", "linalg", "8"]`                               | 240.000 ns (5%) |         |                 |             |
| `["gemm", "mul", "man", "false", "256"]`                       |   2.086 ms (5%) |         |                 |             |
| `["gemm", "mul", "man", "false", "32"]`                        |   5.540 μs (5%) |         |                 |             |
| `["gemm", "mul", "man", "false", "8"]`                         | 331.000 ns (5%) |         |                 |             |
| `["gemm", "mul", "man", "ivdep", "256"]`                       |   2.085 ms (5%) |         |                 |             |
| `["gemm", "mul", "man", "ivdep", "32"]`                        |   4.568 μs (5%) |         |                 |             |
| `["gemm", "mul", "man", "ivdep", "8"]`                         | 320.000 ns (5%) |         |                 |             |
| `["gemm", "mul", "man", "true", "256"]`                        |   2.127 ms (5%) |         |                 |             |
| `["gemm", "mul", "man", "true", "32"]`                         |   5.099 μs (5%) |         |                 |             |
| `["gemm", "mul", "man", "true", "8"]`                          | 430.000 ns (5%) |         |                 |             |
| `["gemm", "mul", "xf", "false", "256"]`                        |   2.113 ms (5%) |         |   80 bytes (1%) |           3 |
| `["gemm", "mul", "xf", "false", "32"]`                         |   5.811 μs (5%) |         |   80 bytes (1%) |           3 |
| `["gemm", "mul", "xf", "false", "8"]`                          | 400.000 ns (5%) |         |   80 bytes (1%) |           3 |
| `["gemm", "mul", "xf", "ivdep", "256"]`                        |   2.113 ms (5%) |         |   80 bytes (1%) |           3 |
| `["gemm", "mul", "xf", "ivdep", "32"]`                         |   4.588 μs (5%) |         |   80 bytes (1%) |           3 |
| `["gemm", "mul", "xf", "ivdep", "8"]`                          | 450.000 ns (5%) |         |   80 bytes (1%) |           3 |
| `["gemm", "mul", "xf", "true", "256"]`                         |   2.131 ms (5%) |         |   80 bytes (1%) |           3 |
| `["gemm", "mul", "xf", "true", "32"]`                          |   5.079 μs (5%) |         |   80 bytes (1%) |           3 |
| `["gemm", "mul", "xf", "true", "8"]`                           | 380.000 ns (5%) |         |   80 bytes (1%) |           3 |
| `["groupby", "sum", "sac"]`                                    |   6.768 ms (5%) |         |  13.14 KiB (1%) |         103 |
| `["groupby", "sum", "xf-with-init"]`                           |  97.281 μs (5%) |         |   1.05 KiB (1%) |           9 |
| `["groupby", "sum", "xf-without-init"]`                        | 100.607 μs (5%) |         |   1.05 KiB (1%) |           9 |
| `["mapcat_eduction", "base"]`                                  |  31.458 μs (5%) |         |                 |             |
| `["mapcat_eduction", "xf-eduction"]`                           |   1.016 μs (5%) |         |                 |             |
| `["mapcat_eduction", "xf-xf"]`                                 |   1.016 μs (5%) |         |                 |             |
| `["missing_argmax", "man"]`                                    |   1.098 μs (5%) |         |                 |             |
| `["missing_argmax", "rf"]`                                     | 772.817 ns (5%) |         |                 |             |
| `["missing_argmax", "xf"]`                                     | 767.835 ns (5%) |         |   32 bytes (1%) |           1 |
| `["missing_dot", "equiv"]`                                     |   1.920 μs (5%) |         |   16 bytes (1%) |           1 |
| `["missing_dot", "man"]`                                       | 835.455 ns (5%) |         |   16 bytes (1%) |           1 |
| `["missing_dot", "naive"]`                                     |   2.751 μs (5%) |         |   16 bytes (1%) |           1 |
| `["missing_dot", "rf"]`                                        | 933.800 ns (5%) |         |   16 bytes (1%) |           1 |
| `["missing_dot", "rf_nota"]`                                   |   1.766 μs (5%) |         |   16 bytes (1%) |           1 |
| `["missing_dot", "xf"]`                                        |  67.606 μs (5%) |         |  72.20 KiB (1%) |        3744 |
| `["missing_dot", "xf_nota"]`                                   |  67.395 μs (5%) |         |  72.11 KiB (1%) |        3742 |
| `["overhead", "foldl"]`                                        |   3.105 ns (5%) |         |                 |             |
| `["overhead", "reduce_basecase"]`                              |  75.249 ns (5%) |         |   16 bytes (1%) |           1 |
| `["partition_by", "man"]`                                      |   1.879 ms (5%) |         |  480 bytes (1%) |           3 |
| `["partition_by", "xf"]`                                       |   2.193 ms (5%) |         |  592 bytes (1%) |           5 |
| `["set", "base"]`                                              |   2.826 ms (5%) |         |  49.14 KiB (1%) |          17 |
| `["set", "xf"]`                                                |   2.684 ms (5%) |         |  49.17 KiB (1%) |          19 |
| `["sum_transpose", "30", "noinit", "iter"]`                    |   2.751 μs (5%) |         |                 |             |
| `["sum_transpose", "30", "noinit", "man"]`                     |   3.118 μs (5%) |         |                 |             |
| `["sum_transpose", "30", "noinit", "xf"]`                      | 805.780 ns (5%) |         |                 |             |
| `["sum_transpose", "30", "withinit", "iter"]`                  | 866.431 ns (5%) |         |                 |             |
| `["sum_transpose", "30", "withinit", "man"]`                   | 805.121 ns (5%) |         |                 |             |
| `["sum_transpose", "30", "withinit", "xf"]`                    | 805.670 ns (5%) |         |                 |             |
| `["teerf_filter", "noinit"]`                                   | 292.500 ns (5%) |         |   80 bytes (1%) |           3 |
| `["teerf_filter", "withinit"]`                                 | 173.862 ns (5%) |         |                 |             |

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
      Ubuntu 22.04.5 LTS
  uname: Linux 6.5.0-1025-azure #26~22.04.1-Ubuntu SMP Thu Jul 11 22:33:04 UTC 2024 x86_64 x86_64
  CPU: AMD EPYC 7763 64-Core Processor: 
              speed         user         nice          sys         idle          irq
       #1  3256 MHz       2191 s          0 s        132 s       7685 s          0 s
       #2  3243 MHz       2492 s          0 s        119 s       7395 s          0 s
       #3  3246 MHz       1858 s          0 s        145 s       8007 s          0 s
       #4  3163 MHz       2509 s          0 s        150 s       7356 s          0 s
       
  Memory: 15.606491088867188 GB (12385.22265625 MB free)
  Uptime: 1004.38 sec
  Load Avg:  1.03  1.01  0.69
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
    BogoMIPS:                           4890.85
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
    Vulnerability Spec rstack overflow: Vulnerable: Safe RET, no microcode
    Vulnerability Spec store bypass:    Vulnerable
    Vulnerability Spectre v1:           Mitigation; usercopy/swapgs barriers and __user pointer sanitization
    Vulnerability Spectre v2:           Mitigation; Retpolines; STIBP disabled; RSB filling; PBRSB-eIBRS Not affected; BHI Not affected
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

