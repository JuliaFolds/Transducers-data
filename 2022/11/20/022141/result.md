# Benchmark result

* Pull request commit: [`adb836a62c98ac48449cec932a9878b6426c58fb`](https://github.com/JuliaFolds/Transducers.jl/commit/adb836a62c98ac48449cec932a9878b6426c58fb)
* Pull request: <https://github.com/JuliaFolds/Transducers.jl/pull/243> (Update */Manifest.toml)

# Judge result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmarks:
    - Target: 20 Nov 2022 - 02:14
    - Baseline: 20 Nov 2022 - 02:20
* Package commits:
    - Target: ce70d0
    - Baseline: 958213
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
| `["append!!", "eduction"]`                                     |                1.08 (5%) :x: |                   1.00 (1%)  |
| `["cartesian", "copyto!", "iter"]`                             |                1.11 (5%) :x: |                   1.00 (1%)  |
| `["cat", "xf"]`                                                |                1.07 (5%) :x: |                   1.00 (1%)  |
| `["dot", "blas"]`                                              |                1.07 (5%) :x: |                   1.00 (1%)  |
| `["dot", "man"]`                                               | 0.92 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["dot", "rf"]`                                                | 0.93 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["dot", "xf"]`                                                |                1.08 (5%) :x: |                   1.00 (1%)  |
| `["filter_sum", "1000", "RandomFloats", "noinit", "naive"]`    |                1.15 (5%) :x: |                   1.00 (1%)  |
| `["filter_sum", "1000", "RandomFloats", "withinit", "base"]`   |                1.07 (5%) :x: |                   1.00 (1%)  |
| `["filter_sum", "1000", "RandomFloats", "withinit", "naive"]`  | 0.86 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["filter_sum", "1000", "UnitRange", "noinit", "naive"]`       |                1.06 (5%) :x: |                   1.00 (1%)  |
| `["filter_sum", "1000", "UnitRange", "withinit", "base"]`      |                1.07 (5%) :x: |                   1.00 (1%)  |
| `["filter_sum", "1000", "UnitRange", "withinit", "naive"]`     | 0.93 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["filter_sum", "10000", "UnitRange", "noinit", "base"]`       | 0.94 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["gemm", "fusedmul", "xf", "2"]`                              | 0.95 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["gemm", "mul", "linalg", "256"]`                             | 0.94 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["gemm", "mul", "linalg", "32"]`                              | 0.93 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["gemm", "mul", "man", "ivdep", "32"]`                        |                1.11 (5%) :x: |                   1.00 (1%)  |
| `["gemm", "mul", "man", "ivdep", "8"]`                         | 0.77 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["gemm", "mul", "man", "true", "32"]`                         |                1.06 (5%) :x: |                   1.00 (1%)  |
| `["gemm", "mul", "man", "true", "8"]`                          | 0.91 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["gemm", "mul", "xf", "ivdep", "8"]`                          | 0.88 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["gemm", "mul", "xf", "true", "32"]`                          | 0.86 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["gemm", "mul", "xf", "true", "8"]`                           | 0.86 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["groupby", "sum", "sac"]`                                    | 0.01 (5%) :white_check_mark: | 0.12 (1%) :white_check_mark: |
| `["groupby", "sum", "xf-with-init"]`                           | 0.89 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["mapcat_eduction", "xf-eduction"]`                           |                1.13 (5%) :x: |                   1.00 (1%)  |
| `["missing_dot", "naive"]`                                     | 0.90 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["missing_dot", "rf_nota"]`                                   |                1.06 (5%) :x: |                   1.00 (1%)  |
| `["missing_dot", "xf_nota"]`                                   | 0.95 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["overhead", "reduce_basecase"]`                              |                1.07 (5%) :x: |                   1.00 (1%)  |
| `["sum_transpose", "30", "withinit", "iter"]`                  |                1.10 (5%) :x: |                   1.00 (1%)  |
| `["sum_transpose", "30", "withinit", "man"]`                   |                1.06 (5%) :x: |                   1.00 (1%)  |
| `["sum_transpose", "30", "withinit", "xf"]`                    |                1.10 (5%) :x: |                   1.00 (1%)  |

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
      Ubuntu 22.04.1 LTS
  uname: Linux 5.15.0-1022-azure #27-Ubuntu SMP Thu Oct 13 17:09:33 UTC 2022 x86_64 x86_64
  CPU: Intel(R) Xeon(R) CPU E5-2673 v4 @ 2.30GHz: 
              speed         user         nice          sys         idle          irq
       #1  2294 MHz       6654 s          0 s        172 s       2740 s          0 s
       #2  2294 MHz       1641 s          0 s        176 s       7726 s          0 s
       
  Memory: 6.781223297119141 GB (3698.85546875 MB free)
  Uptime: 962.89 sec
  Load Avg:  1.05  1.02  0.72
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-12.0.1 (ORCJIT, broadwell)
```

### Baseline
```
Julia Version 1.7.3
Commit 742b9abb4d (2022-05-06 12:58 UTC)
Platform Info:
  OS: Linux (x86_64-pc-linux-gnu)
      Ubuntu 22.04.1 LTS
  uname: Linux 5.15.0-1022-azure #27-Ubuntu SMP Thu Oct 13 17:09:33 UTC 2022 x86_64 x86_64
  CPU: Intel(R) Xeon(R) CPU E5-2673 v4 @ 2.30GHz: 
              speed         user         nice          sys         idle          irq
       #1  2294 MHz       9863 s          0 s        228 s       2842 s          0 s
       #2  2294 MHz       1830 s          0 s        206 s      10868 s          0 s
       
  Memory: 6.781223297119141 GB (3593.48828125 MB free)
  Uptime: 1300.16 sec
  Load Avg:  1.0  1.02  0.84
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-12.0.1 (ORCJIT, broadwell)
```

---
# Target result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmark: 20 Nov 2022 - 2:14
* Package commit: ce70d0
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
| `["append!!", "eduction"]`                                     |  19.600 μs (5%) |         |  53.98 KiB (1%) |           8 |
| `["append!!", "xf"]`                                           |  20.400 μs (5%) |         |  53.98 KiB (1%) |           8 |
| `["cartesian", "copyto!", "iter"]`                             |   2.222 μs (5%) |         |                 |             |
| `["cartesian", "copyto!", "man"]`                              |   2.000 μs (5%) |         |                 |             |
| `["cartesian", "copyto!", "xf"]`                               |   2.222 μs (5%) |         |                 |             |
| `["cat", "base"]`                                              |   1.650 μs (5%) |         |                 |             |
| `["cat", "xf"]`                                                |   1.630 μs (5%) |         |                 |             |
| `["collect", "filter-missing"]`                                |  51.001 μs (5%) |         |  41.33 KiB (1%) |          10 |
| `["collect", "identity-float"]`                                |  23.001 μs (5%) |         | 326.61 KiB (1%) |          10 |
| `["collect", "identity-union"]`                                | 146.002 μs (5%) |         | 679.41 KiB (1%) |       10010 |
| `["dict", "base"]`                                             |   4.432 ms (5%) |         |  92.45 KiB (1%) |          22 |
| `["dict", "xf"]`                                               |   4.244 ms (5%) |         |  91.95 KiB (1%) |          18 |
| `["dot", "blas"]`                                              |   2.444 μs (5%) |         |                 |             |
| `["dot", "man"]`                                               |   2.300 μs (5%) |         |                 |             |
| `["dot", "rf"]`                                                |   3.062 μs (5%) |         |                 |             |
| `["dot", "xf"]`                                                |   3.300 μs (5%) |         |                 |             |
| `["filter_map_map!", "man"]`                                   |  68.100 μs (5%) |         |                 |             |
| `["filter_map_map!", "xf"]`                                    |  74.401 μs (5%) |         |                 |             |
| `["filter_map_reduce", "man"]`                                 | 200.602 μs (5%) |         |                 |             |
| `["filter_map_reduce", "xf"]`                                  | 206.502 μs (5%) |         |                 |             |
| `["filter_sum", "1000", "RandomFloats", "noinit", "base"]`     |   1.890 μs (5%) |         |                 |             |
| `["filter_sum", "1000", "RandomFloats", "noinit", "naive"]`    |   1.290 μs (5%) |         |                 |             |
| `["filter_sum", "1000", "RandomFloats", "noinit", "xf"]`       |   1.550 μs (5%) |         |                 |             |
| `["filter_sum", "1000", "RandomFloats", "withinit", "base"]`   |   1.610 μs (5%) |         |                 |             |
| `["filter_sum", "1000", "RandomFloats", "withinit", "naive"]`  | 658.902 ns (5%) |         |                 |             |
| `["filter_sum", "1000", "RandomFloats", "withinit", "xf"]`     |   1.560 μs (5%) |         |                 |             |
| `["filter_sum", "1000", "UnitRange", "noinit", "base"]`        | 891.429 ns (5%) |         |                 |             |
| `["filter_sum", "1000", "UnitRange", "noinit", "naive"]`       | 980.000 ns (5%) |         |                 |             |
| `["filter_sum", "1000", "UnitRange", "noinit", "xf"]`          | 229.366 ns (5%) |         |                 |             |
| `["filter_sum", "1000", "UnitRange", "withinit", "base"]`      | 170.381 ns (5%) |         |                 |             |
| `["filter_sum", "1000", "UnitRange", "withinit", "naive"]`     | 591.234 ns (5%) |         |                 |             |
| `["filter_sum", "1000", "UnitRange", "withinit", "xf"]`        | 171.100 ns (5%) |         |                 |             |
| `["filter_sum", "10000", "RandomFloats", "noinit", "base"]`    |  18.400 μs (5%) |         |                 |             |
| `["filter_sum", "10000", "RandomFloats", "noinit", "naive"]`   |  42.100 μs (5%) |         |                 |             |
| `["filter_sum", "10000", "RandomFloats", "noinit", "xf"]`      |  15.200 μs (5%) |         |                 |             |
| `["filter_sum", "10000", "RandomFloats", "withinit", "base"]`  |  15.200 μs (5%) |         |                 |             |
| `["filter_sum", "10000", "RandomFloats", "withinit", "naive"]` |  35.900 μs (5%) |         |                 |             |
| `["filter_sum", "10000", "RandomFloats", "withinit", "xf"]`    |  15.600 μs (5%) |         |                 |             |
| `["filter_sum", "10000", "UnitRange", "noinit", "base"]`       |   9.100 μs (5%) |         |                 |             |
| `["filter_sum", "10000", "UnitRange", "noinit", "naive"]`      |   9.700 μs (5%) |         |                 |             |
| `["filter_sum", "10000", "UnitRange", "noinit", "xf"]`         |   2.233 μs (5%) |         |                 |             |
| `["filter_sum", "10000", "UnitRange", "withinit", "base"]`     |   1.640 μs (5%) |         |                 |             |
| `["filter_sum", "10000", "UnitRange", "withinit", "naive"]`    |   6.100 μs (5%) |         |                 |             |
| `["filter_sum", "10000", "UnitRange", "withinit", "xf"]`       |   1.540 μs (5%) |         |                 |             |
| `["findall", "base"]`                                          | 173.602 μs (5%) |         | 797.20 KiB (1%) |           8 |
| `["findall", "xf-array"]`                                      |   1.261 ms (5%) |         |   2.94 MiB (1%) |       96426 |
| `["findall", "xf-iter"]`                                       | 839.008 μs (5%) |         |   1.83 MiB (1%) |          14 |
| `["gemm", "fusedmul", "blas", "16"]`                           |   5.399 ms (5%) |         |                 |             |
| `["gemm", "fusedmul", "blas", "2"]`                            |   4.020 ms (5%) |         |                 |             |
| `["gemm", "fusedmul", "blas", "32"]`                           |   7.147 ms (5%) |         |                 |             |
| `["gemm", "fusedmul", "blas", "8"]`                            |   4.182 ms (5%) |         |                 |             |
| `["gemm", "fusedmul", "xf", "16"]`                             |   5.422 ms (5%) |         |  192 bytes (1%) |           4 |
| `["gemm", "fusedmul", "xf", "2"]`                              | 649.405 μs (5%) |         |  192 bytes (1%) |           4 |
| `["gemm", "fusedmul", "xf", "32"]`                             |  10.992 ms (5%) |         |  192 bytes (1%) |           4 |
| `["gemm", "fusedmul", "xf", "8"]`                              |   2.700 ms (5%) |         |  192 bytes (1%) |           4 |
| `["gemm", "mul", "linalg", "256"]`                             |   1.044 ms (5%) |         |                 |             |
| `["gemm", "mul", "linalg", "32"]`                              |   3.987 μs (5%) |         |                 |             |
| `["gemm", "mul", "linalg", "8"]`                               | 298.712 ns (5%) |         |                 |             |
| `["gemm", "mul", "man", "false", "256"]`                       |   4.830 ms (5%) |         |                 |             |
| `["gemm", "mul", "man", "false", "32"]`                        |   8.050 μs (5%) |         |                 |             |
| `["gemm", "mul", "man", "false", "8"]`                         | 389.604 ns (5%) |         |                 |             |
| `["gemm", "mul", "man", "ivdep", "256"]`                       |   4.789 ms (5%) |         |                 |             |
| `["gemm", "mul", "man", "ivdep", "32"]`                        |   6.660 μs (5%) |         |                 |             |
| `["gemm", "mul", "man", "ivdep", "8"]`                         | 386.572 ns (5%) |         |                 |             |
| `["gemm", "mul", "man", "true", "256"]`                        |   4.744 ms (5%) |         |                 |             |
| `["gemm", "mul", "man", "true", "32"]`                         |   7.025 μs (5%) |         |                 |             |
| `["gemm", "mul", "man", "true", "8"]`                          | 455.330 ns (5%) |         |                 |             |
| `["gemm", "mul", "xf", "false", "256"]`                        |   4.821 ms (5%) |         |   80 bytes (1%) |           3 |
| `["gemm", "mul", "xf", "false", "32"]`                         |   7.167 μs (5%) |         |   80 bytes (1%) |           3 |
| `["gemm", "mul", "xf", "false", "8"]`                          | 507.071 ns (5%) |         |   80 bytes (1%) |           3 |
| `["gemm", "mul", "xf", "ivdep", "256"]`                        |   4.774 ms (5%) |         |   80 bytes (1%) |           3 |
| `["gemm", "mul", "xf", "ivdep", "32"]`                         |   6.220 μs (5%) |         |   80 bytes (1%) |           3 |
| `["gemm", "mul", "xf", "ivdep", "8"]`                          | 441.842 ns (5%) |         |   80 bytes (1%) |           3 |
| `["gemm", "mul", "xf", "true", "256"]`                         |   4.804 ms (5%) |         |   80 bytes (1%) |           3 |
| `["gemm", "mul", "xf", "true", "32"]`                          |   6.650 μs (5%) |         |   80 bytes (1%) |           3 |
| `["gemm", "mul", "xf", "true", "8"]`                           | 518.285 ns (5%) |         |   80 bytes (1%) |           3 |
| `["groupby", "sum", "sac"]`                                    | 135.700 μs (5%) |         |   1.64 KiB (1%) |          11 |
| `["groupby", "sum", "xf-with-init"]`                           | 131.201 μs (5%) |         |   1.05 KiB (1%) |           9 |
| `["groupby", "sum", "xf-without-init"]`                        | 136.900 μs (5%) |         |   1.05 KiB (1%) |           9 |
| `["mapcat_eduction", "base"]`                                  |  52.800 μs (5%) |         |                 |             |
| `["mapcat_eduction", "xf-eduction"]`                           |   1.790 μs (5%) |         |                 |             |
| `["mapcat_eduction", "xf-xf"]`                                 |   1.790 μs (5%) |         |                 |             |
| `["missing_argmax", "man"]`                                    |   1.670 μs (5%) |         |                 |             |
| `["missing_argmax", "rf"]`                                     |   1.340 μs (5%) |         |                 |             |
| `["missing_argmax", "xf"]`                                     |   1.370 μs (5%) |         |   32 bytes (1%) |           1 |
| `["missing_dot", "equiv"]`                                     |   2.333 μs (5%) |         |   16 bytes (1%) |           1 |
| `["missing_dot", "man"]`                                       |   1.260 μs (5%) |         |   16 bytes (1%) |           1 |
| `["missing_dot", "naive"]`                                     |   2.120 μs (5%) |         |   16 bytes (1%) |           1 |
| `["missing_dot", "rf"]`                                        |   1.280 μs (5%) |         |   16 bytes (1%) |           1 |
| `["missing_dot", "rf_nota"]`                                   |   2.411 μs (5%) |         |   16 bytes (1%) |           1 |
| `["missing_dot", "xf"]`                                        | 101.401 μs (5%) |         |  72.05 KiB (1%) |        3736 |
| `["missing_dot", "xf_nota"]`                                   |  93.001 μs (5%) |         |  72.20 KiB (1%) |        3746 |
| `["overhead", "foldl"]`                                        |   3.500 ns (5%) |         |                 |             |
| `["overhead", "reduce_basecase"]`                              | 112.673 ns (5%) |         |   16 bytes (1%) |           1 |
| `["partition_by", "man"]`                                      |   2.353 ms (5%) |         |  480 bytes (1%) |           3 |
| `["partition_by", "xf"]`                                       |   2.476 ms (5%) |         |  592 bytes (1%) |           5 |
| `["set", "base"]`                                              |   4.541 ms (5%) |         |  49.14 KiB (1%) |          17 |
| `["set", "xf"]`                                                |   4.734 ms (5%) |         |  49.17 KiB (1%) |          19 |
| `["sum_transpose", "30", "noinit", "iter"]`                    |   1.720 μs (5%) |         |                 |             |
| `["sum_transpose", "30", "noinit", "man"]`                     |   1.510 μs (5%) |         |                 |             |
| `["sum_transpose", "30", "noinit", "xf"]`                      | 818.182 ns (5%) |         |   32 bytes (1%) |           2 |
| `["sum_transpose", "30", "withinit", "iter"]`                  |   1.400 μs (5%) |         |                 |             |
| `["sum_transpose", "30", "withinit", "man"]`                   | 820.290 ns (5%) |         |                 |             |
| `["sum_transpose", "30", "withinit", "xf"]`                    | 933.333 ns (5%) |         |   48 bytes (1%) |           3 |
| `["teerf_filter", "noinit"]`                                   | 386.935 ns (5%) |         |   80 bytes (1%) |           3 |
| `["teerf_filter", "withinit"]`                                 | 226.715 ns (5%) |         |                 |             |

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
      Ubuntu 22.04.1 LTS
  uname: Linux 5.15.0-1022-azure #27-Ubuntu SMP Thu Oct 13 17:09:33 UTC 2022 x86_64 x86_64
  CPU: Intel(R) Xeon(R) CPU E5-2673 v4 @ 2.30GHz: 
              speed         user         nice          sys         idle          irq
       #1  2294 MHz       6654 s          0 s        172 s       2740 s          0 s
       #2  2294 MHz       1641 s          0 s        176 s       7726 s          0 s
       
  Memory: 6.781223297119141 GB (3698.85546875 MB free)
  Uptime: 962.89 sec
  Load Avg:  1.05  1.02  0.72
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-12.0.1 (ORCJIT, broadwell)
```

---
# Baseline result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmark: 20 Nov 2022 - 2:20
* Package commit: 958213
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
| `["append!!", "eduction"]`                                     |  18.200 μs (5%) |         |  53.98 KiB (1%) |           8 |
| `["append!!", "xf"]`                                           |  20.100 μs (5%) |         |  53.98 KiB (1%) |           8 |
| `["cartesian", "copyto!", "iter"]`                             |   2.000 μs (5%) |         |                 |             |
| `["cartesian", "copyto!", "man"]`                              |   2.000 μs (5%) |         |                 |             |
| `["cartesian", "copyto!", "xf"]`                               |   2.133 μs (5%) |         |                 |             |
| `["cat", "base"]`                                              |   1.660 μs (5%) |         |                 |             |
| `["cat", "xf"]`                                                |   1.530 μs (5%) |         |                 |             |
| `["collect", "filter-missing"]`                                |  51.700 μs (5%) |         |  41.33 KiB (1%) |          10 |
| `["collect", "identity-float"]`                                |  23.501 μs (5%) |         | 326.61 KiB (1%) |          10 |
| `["collect", "identity-union"]`                                | 151.701 μs (5%) |         | 679.41 KiB (1%) |       10010 |
| `["dict", "base"]`                                             |   4.288 ms (5%) |         |  92.45 KiB (1%) |          22 |
| `["dict", "xf"]`                                               |   4.187 ms (5%) |         |  91.95 KiB (1%) |          18 |
| `["dot", "blas"]`                                              |   2.278 μs (5%) |         |                 |             |
| `["dot", "man"]`                                               |   2.489 μs (5%) |         |                 |             |
| `["dot", "rf"]`                                                |   3.300 μs (5%) |         |                 |             |
| `["dot", "xf"]`                                                |   3.062 μs (5%) |         |                 |             |
| `["filter_map_map!", "man"]`                                   |  68.001 μs (5%) |         |                 |             |
| `["filter_map_map!", "xf"]`                                    |  71.500 μs (5%) |         |                 |             |
| `["filter_map_reduce", "man"]`                                 | 206.401 μs (5%) |         |                 |             |
| `["filter_map_reduce", "xf"]`                                  | 206.501 μs (5%) |         |                 |             |
| `["filter_sum", "1000", "RandomFloats", "noinit", "base"]`     |   1.840 μs (5%) |         |                 |             |
| `["filter_sum", "1000", "RandomFloats", "noinit", "naive"]`    |   1.120 μs (5%) |         |                 |             |
| `["filter_sum", "1000", "RandomFloats", "noinit", "xf"]`       |   1.510 μs (5%) |         |                 |             |
| `["filter_sum", "1000", "RandomFloats", "withinit", "base"]`   |   1.510 μs (5%) |         |                 |             |
| `["filter_sum", "1000", "RandomFloats", "withinit", "naive"]`  | 763.810 ns (5%) |         |                 |             |
| `["filter_sum", "1000", "RandomFloats", "withinit", "xf"]`     |   1.610 μs (5%) |         |                 |             |
| `["filter_sum", "1000", "UnitRange", "noinit", "base"]`        | 920.000 ns (5%) |         |                 |             |
| `["filter_sum", "1000", "UnitRange", "noinit", "naive"]`       | 926.667 ns (5%) |         |                 |             |
| `["filter_sum", "1000", "UnitRange", "noinit", "xf"]`          | 221.971 ns (5%) |         |                 |             |
| `["filter_sum", "1000", "UnitRange", "withinit", "base"]`      | 158.848 ns (5%) |         |                 |             |
| `["filter_sum", "1000", "UnitRange", "withinit", "naive"]`     | 635.678 ns (5%) |         |                 |             |
| `["filter_sum", "1000", "UnitRange", "withinit", "xf"]`        | 170.692 ns (5%) |         |                 |             |
| `["filter_sum", "10000", "RandomFloats", "noinit", "base"]`    |  18.400 μs (5%) |         |                 |             |
| `["filter_sum", "10000", "RandomFloats", "noinit", "naive"]`   |  40.800 μs (5%) |         |                 |             |
| `["filter_sum", "10000", "RandomFloats", "noinit", "xf"]`      |  14.700 μs (5%) |         |                 |             |
| `["filter_sum", "10000", "RandomFloats", "withinit", "base"]`  |  14.800 μs (5%) |         |                 |             |
| `["filter_sum", "10000", "RandomFloats", "withinit", "naive"]` |  35.500 μs (5%) |         |                 |             |
| `["filter_sum", "10000", "RandomFloats", "withinit", "xf"]`    |  15.200 μs (5%) |         |                 |             |
| `["filter_sum", "10000", "UnitRange", "noinit", "base"]`       |   9.700 μs (5%) |         |                 |             |
| `["filter_sum", "10000", "UnitRange", "noinit", "naive"]`      |  10.000 μs (5%) |         |                 |             |
| `["filter_sum", "10000", "UnitRange", "noinit", "xf"]`         |   2.167 μs (5%) |         |                 |             |
| `["filter_sum", "10000", "UnitRange", "withinit", "base"]`     |   1.580 μs (5%) |         |                 |             |
| `["filter_sum", "10000", "UnitRange", "withinit", "naive"]`    |   6.080 μs (5%) |         |                 |             |
| `["filter_sum", "10000", "UnitRange", "withinit", "xf"]`       |   1.580 μs (5%) |         |                 |             |
| `["findall", "base"]`                                          | 168.401 μs (5%) |         | 797.20 KiB (1%) |           8 |
| `["findall", "xf-array"]`                                      |   1.282 ms (5%) |         |   2.94 MiB (1%) |       96426 |
| `["findall", "xf-iter"]`                                       | 858.304 μs (5%) |         |   1.83 MiB (1%) |          14 |
| `["gemm", "fusedmul", "blas", "16"]`                           |   5.402 ms (5%) |         |                 |             |
| `["gemm", "fusedmul", "blas", "2"]`                            |   3.957 ms (5%) |         |                 |             |
| `["gemm", "fusedmul", "blas", "32"]`                           |   7.055 ms (5%) |         |                 |             |
| `["gemm", "fusedmul", "blas", "8"]`                            |   4.164 ms (5%) |         |                 |             |
| `["gemm", "fusedmul", "xf", "16"]`                             |   5.462 ms (5%) |         |  192 bytes (1%) |           4 |
| `["gemm", "fusedmul", "xf", "2"]`                              | 686.303 μs (5%) |         |  192 bytes (1%) |           4 |
| `["gemm", "fusedmul", "xf", "32"]`                             |  11.103 ms (5%) |         |  192 bytes (1%) |           4 |
| `["gemm", "fusedmul", "xf", "8"]`                              |   2.679 ms (5%) |         |  192 bytes (1%) |           4 |
| `["gemm", "mul", "linalg", "256"]`                             |   1.112 ms (5%) |         |                 |             |
| `["gemm", "mul", "linalg", "32"]`                              |   4.300 μs (5%) |         |                 |             |
| `["gemm", "mul", "linalg", "8"]`                               | 300.000 ns (5%) |         |                 |             |
| `["gemm", "mul", "man", "false", "256"]`                       |   4.821 ms (5%) |         |                 |             |
| `["gemm", "mul", "man", "false", "32"]`                        |   7.900 μs (5%) |         |                 |             |
| `["gemm", "mul", "man", "false", "8"]`                         | 400.000 ns (5%) |         |                 |             |
| `["gemm", "mul", "man", "ivdep", "256"]`                       |   4.748 ms (5%) |         |                 |             |
| `["gemm", "mul", "man", "ivdep", "32"]`                        |   6.000 μs (5%) |         |                 |             |
| `["gemm", "mul", "man", "ivdep", "8"]`                         | 500.000 ns (5%) |         |                 |             |
| `["gemm", "mul", "man", "true", "256"]`                        |   4.801 ms (5%) |         |                 |             |
| `["gemm", "mul", "man", "true", "32"]`                         |   6.600 μs (5%) |         |                 |             |
| `["gemm", "mul", "man", "true", "8"]`                          | 500.000 ns (5%) |         |                 |             |
| `["gemm", "mul", "xf", "false", "256"]`                        |   4.796 ms (5%) |         |   80 bytes (1%) |           3 |
| `["gemm", "mul", "xf", "false", "32"]`                         |   7.200 μs (5%) |         |   80 bytes (1%) |           3 |
| `["gemm", "mul", "xf", "false", "8"]`                          | 500.000 ns (5%) |         |   80 bytes (1%) |           3 |
| `["gemm", "mul", "xf", "ivdep", "256"]`                        |   4.765 ms (5%) |         |   80 bytes (1%) |           3 |
| `["gemm", "mul", "xf", "ivdep", "32"]`                         |   6.500 μs (5%) |         |   80 bytes (1%) |           3 |
| `["gemm", "mul", "xf", "ivdep", "8"]`                          | 500.000 ns (5%) |         |   80 bytes (1%) |           3 |
| `["gemm", "mul", "xf", "true", "256"]`                         |   4.769 ms (5%) |         |   80 bytes (1%) |           3 |
| `["gemm", "mul", "xf", "true", "32"]`                          |   7.700 μs (5%) |         |   80 bytes (1%) |           3 |
| `["gemm", "mul", "xf", "true", "8"]`                           | 600.000 ns (5%) |         |   80 bytes (1%) |           3 |
| `["groupby", "sum", "sac"]`                                    |   9.201 ms (5%) |         |  13.14 KiB (1%) |         103 |
| `["groupby", "sum", "xf-with-init"]`                           | 147.500 μs (5%) |         |   1.05 KiB (1%) |           9 |
| `["groupby", "sum", "xf-without-init"]`                        | 139.601 μs (5%) |         |   1.05 KiB (1%) |           9 |
| `["mapcat_eduction", "base"]`                                  |  51.700 μs (5%) |         |                 |             |
| `["mapcat_eduction", "xf-eduction"]`                           |   1.590 μs (5%) |         |                 |             |
| `["mapcat_eduction", "xf-xf"]`                                 |   1.730 μs (5%) |         |                 |             |
| `["missing_argmax", "man"]`                                    |   1.650 μs (5%) |         |                 |             |
| `["missing_argmax", "rf"]`                                     |   1.320 μs (5%) |         |                 |             |
| `["missing_argmax", "xf"]`                                     |   1.310 μs (5%) |         |   32 bytes (1%) |           1 |
| `["missing_dot", "equiv"]`                                     |   2.267 μs (5%) |         |   16 bytes (1%) |           1 |
| `["missing_dot", "man"]`                                       |   1.220 μs (5%) |         |   16 bytes (1%) |           1 |
| `["missing_dot", "naive"]`                                     |   2.350 μs (5%) |         |   16 bytes (1%) |           1 |
| `["missing_dot", "rf"]`                                        |   1.300 μs (5%) |         |   16 bytes (1%) |           1 |
| `["missing_dot", "rf_nota"]`                                   |   2.267 μs (5%) |         |   16 bytes (1%) |           1 |
| `["missing_dot", "xf"]`                                        |  97.200 μs (5%) |         |  72.17 KiB (1%) |        3744 |
| `["missing_dot", "xf_nota"]`                                   |  98.001 μs (5%) |         |  71.92 KiB (1%) |        3733 |
| `["overhead", "foldl"]`                                        |   3.600 ns (5%) |         |                 |             |
| `["overhead", "reduce_basecase"]`                              | 105.539 ns (5%) |         |   16 bytes (1%) |           1 |
| `["partition_by", "man"]`                                      |   2.254 ms (5%) |         |  480 bytes (1%) |           3 |
| `["partition_by", "xf"]`                                       |   2.520 ms (5%) |         |  592 bytes (1%) |           5 |
| `["set", "base"]`                                              |   4.682 ms (5%) |         |  49.14 KiB (1%) |          17 |
| `["set", "xf"]`                                                |   4.664 ms (5%) |         |  49.17 KiB (1%) |          19 |
| `["sum_transpose", "30", "noinit", "iter"]`                    |   1.660 μs (5%) |         |                 |             |
| `["sum_transpose", "30", "noinit", "man"]`                     |   1.550 μs (5%) |         |                 |             |
| `["sum_transpose", "30", "noinit", "xf"]`                      | 818.182 ns (5%) |         |   32 bytes (1%) |           2 |
| `["sum_transpose", "30", "withinit", "iter"]`                  |   1.270 μs (5%) |         |                 |             |
| `["sum_transpose", "30", "withinit", "man"]`                   | 772.464 ns (5%) |         |                 |             |
| `["sum_transpose", "30", "withinit", "xf"]`                    | 848.718 ns (5%) |         |   48 bytes (1%) |           3 |
| `["teerf_filter", "noinit"]`                                   | 395.477 ns (5%) |         |   80 bytes (1%) |           3 |
| `["teerf_filter", "withinit"]`                                 | 227.397 ns (5%) |         |                 |             |

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
      Ubuntu 22.04.1 LTS
  uname: Linux 5.15.0-1022-azure #27-Ubuntu SMP Thu Oct 13 17:09:33 UTC 2022 x86_64 x86_64
  CPU: Intel(R) Xeon(R) CPU E5-2673 v4 @ 2.30GHz: 
              speed         user         nice          sys         idle          irq
       #1  2294 MHz       9863 s          0 s        228 s       2842 s          0 s
       #2  2294 MHz       1830 s          0 s        206 s      10868 s          0 s
       
  Memory: 6.781223297119141 GB (3593.48828125 MB free)
  Uptime: 1300.16 sec
  Load Avg:  1.0  1.02  0.84
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-12.0.1 (ORCJIT, broadwell)
```

---
# Runtime information
| Runtime Info | |
|:--|:--|
| BLAS #threads | 2 |
| `BLAS.vendor()` | `openblas64` |
| `Sys.CPU_THREADS` | 2 |

`lscpu` output:

    Architecture:                    x86_64
    CPU op-mode(s):                  32-bit, 64-bit
    Address sizes:                   46 bits physical, 48 bits virtual
    Byte Order:                      Little Endian
    CPU(s):                          2
    On-line CPU(s) list:             0,1
    Vendor ID:                       GenuineIntel
    Model name:                      Intel(R) Xeon(R) CPU E5-2673 v4 @ 2.30GHz
    CPU family:                      6
    Model:                           79
    Thread(s) per core:              1
    Core(s) per socket:              2
    Socket(s):                       1
    Stepping:                        1
    BogoMIPS:                        4589.36
    Flags:                           fpu vme de pse tsc msr pae mce cx8 apic sep mtrr pge mca cmov pat pse36 clflush mmx fxsr sse sse2 ss ht syscall nx pdpe1gb rdtscp lm constant_tsc rep_good nopl xtopology cpuid pni pclmulqdq ssse3 fma cx16 pcid sse4_1 sse4_2 movbe popcnt aes xsave avx f16c rdrand hypervisor lahf_lm abm 3dnowprefetch invpcid_single pti fsgsbase bmi1 hle avx2 smep bmi2 erms invpcid rtm rdseed adx smap xsaveopt md_clear
    Hypervisor vendor:               Microsoft
    Virtualization type:             full
    L1d cache:                       64 KiB (2 instances)
    L1i cache:                       64 KiB (2 instances)
    L2 cache:                        512 KiB (2 instances)
    L3 cache:                        50 MiB (1 instance)
    NUMA node(s):                    1
    NUMA node0 CPU(s):               0,1
    Vulnerability Itlb multihit:     KVM: Mitigation: VMX unsupported
    Vulnerability L1tf:              Mitigation; PTE Inversion
    Vulnerability Mds:               Mitigation; Clear CPU buffers; SMT Host state unknown
    Vulnerability Meltdown:          Mitigation; PTI
    Vulnerability Mmio stale data:   Vulnerable: Clear CPU buffers attempted, no microcode; SMT Host state unknown
    Vulnerability Retbleed:          Not affected
    Vulnerability Spec store bypass: Vulnerable
    Vulnerability Spectre v1:        Mitigation; usercopy/swapgs barriers and __user pointer sanitization
    Vulnerability Spectre v2:        Mitigation; Retpolines, STIBP disabled, RSB filling, PBRSB-eIBRS Not affected
    Vulnerability Srbds:             Not affected
    Vulnerability Tsx async abort:   Mitigation; Clear CPU buffers; SMT Host state unknown
    

| Cpu Property       | Value                                                   |
|:------------------ |:------------------------------------------------------- |
| Brand              | Intel(R) Xeon(R) CPU E5-2673 v4 @ 2.30GHz               |
| Vendor             | :Intel                                                  |
| Architecture       | :Broadwell                                              |
| Model              | Family: 0x06, Model: 0x4f, Stepping: 0x01, Type: 0x00   |
| Cores              | 2 physical cores, 2 logical cores (on executing CPU)    |
|                    | No Hyperthreading hardware capability detected          |
| Clock Frequencies  | Not supported by CPU                                    |
| Data Cache         | Level 1:3 : (32, 256, 51200) kbytes                     |
|                    | 64 byte cache line size                                 |
| Address Size       | 48 bits virtual, 46 bits physical                       |
| SIMD               | 256 bit = 32 byte max. SIMD vector size                 |
| Time Stamp Counter | TSC is accessible via `rdtsc`                           |
|                    | TSC increased at every clock cycle (non-invariant TSC)  |
| Perf. Monitoring   | Performance Monitoring Counters (PMC) are not supported |
| Hypervisor         | Yes, Microsoft                                          |

