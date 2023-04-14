# Benchmark result

* Pull request commit: [`3a961313d78243c5d674205c2f6d2868805ef7f9`](https://github.com/JuliaFolds/Transducers.jl/commit/3a961313d78243c5d674205c2f6d2868805ef7f9)
* Pull request: <https://github.com/JuliaFolds/Transducers.jl/pull/243> (Update */Manifest.toml)

# Judge result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmarks:
    - Target: 14 Apr 2023 - 01:35
    - Baseline: 14 Apr 2023 - 01:40
* Package commits:
    - Target: 257197
    - Baseline: f8d0df
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
| `["append!!", "eduction"]`                                     |                1.23 (5%) :x: |                   1.00 (1%)  |
| `["append!!", "xf"]`                                           |                1.21 (5%) :x: |                   1.00 (1%)  |
| `["cartesian", "copyto!", "iter"]`                             |                1.09 (5%) :x: |                   1.00 (1%)  |
| `["cartesian", "copyto!", "man"]`                              |                1.16 (5%) :x: |                   1.00 (1%)  |
| `["collect", "identity-union"]`                                | 0.94 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["dot", "blas"]`                                              |                1.26 (5%) :x: |                   1.00 (1%)  |
| `["dot", "man"]`                                               |                1.16 (5%) :x: |                   1.00 (1%)  |
| `["filter_sum", "1000", "RandomFloats", "noinit", "xf"]`       | 0.87 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["filter_sum", "1000", "RandomFloats", "withinit", "base"]`   | 0.87 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["filter_sum", "1000", "UnitRange", "noinit", "naive"]`       |                1.15 (5%) :x: |                   1.00 (1%)  |
| `["filter_sum", "1000", "UnitRange", "noinit", "xf"]`          |                1.16 (5%) :x: |                   1.00 (1%)  |
| `["filter_sum", "1000", "UnitRange", "withinit", "xf"]`        |                1.13 (5%) :x: |                   1.00 (1%)  |
| `["filter_sum", "10000", "RandomFloats", "noinit", "base"]`    | 0.86 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["filter_sum", "10000", "RandomFloats", "withinit", "xf"]`    |                1.16 (5%) :x: |                   1.00 (1%)  |
| `["filter_sum", "10000", "UnitRange", "noinit", "naive"]`      | 0.87 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["filter_sum", "10000", "UnitRange", "withinit", "base"]`     | 0.86 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["filter_sum", "10000", "UnitRange", "withinit", "naive"]`    | 0.86 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["filter_sum", "10000", "UnitRange", "withinit", "xf"]`       | 0.87 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["gemm", "mul", "linalg", "256"]`                             | 0.90 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["gemm", "mul", "linalg", "32"]`                              | 0.89 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["gemm", "mul", "man", "false", "32"]`                        | 0.84 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["gemm", "mul", "man", "false", "8"]`                         | 0.83 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["gemm", "mul", "man", "true", "32"]`                         | 0.82 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["gemm", "mul", "xf", "false", "32"]`                         | 0.84 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["gemm", "mul", "xf", "false", "8"]`                          | 0.75 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["gemm", "mul", "xf", "true", "8"]`                           |                1.17 (5%) :x: |                   1.00 (1%)  |
| `["groupby", "sum", "sac"]`                                    | 0.02 (5%) :white_check_mark: | 0.12 (1%) :white_check_mark: |
| `["groupby", "sum", "xf-without-init"]`                        |                1.19 (5%) :x: |                   1.00 (1%)  |
| `["mapcat_eduction", "base"]`                                  | 0.85 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["mapcat_eduction", "xf-xf"]`                                 |                1.16 (5%) :x: |                   1.00 (1%)  |
| `["missing_argmax", "man"]`                                    | 0.86 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["missing_argmax", "rf"]`                                     | 0.91 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["missing_argmax", "xf"]`                                     | 0.87 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["missing_dot", "equiv"]`                                     |                1.23 (5%) :x: |                   1.00 (1%)  |
| `["missing_dot", "naive"]`                                     | 0.95 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["missing_dot", "rf_nota"]`                                   |                1.21 (5%) :x: |                   1.00 (1%)  |
| `["missing_dot", "xf"]`                                        | 0.92 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["overhead", "foldl"]`                                        |                1.12 (5%) :x: |                   1.00 (1%)  |
| `["overhead", "reduce_basecase"]`                              | 0.94 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["sum_transpose", "30", "withinit", "iter"]`                  | 0.79 (5%) :white_check_mark: |                   1.00 (1%)  |

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
      Ubuntu 22.04.2 LTS
  uname: Linux 5.15.0-1035-azure #42-Ubuntu SMP Tue Feb 28 19:41:23 UTC 2023 x86_64 x86_64
  CPU: Intel(R) Xeon(R) Platinum 8171M CPU @ 2.60GHz: 
              speed         user         nice          sys         idle          irq
       #1  2095 MHz        519 s          0 s        181 s       8728 s          0 s
       #2  2095 MHz       7225 s          0 s        188 s       2025 s          0 s
       
  Memory: 6.781208038330078 GB (3701.3203125 MB free)
  Uptime: 952.69 sec
  Load Avg:  1.0  0.98  0.68
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-12.0.1 (ORCJIT, skylake-avx512)
```

### Baseline
```
Julia Version 1.7.3
Commit 742b9abb4d (2022-05-06 12:58 UTC)
Platform Info:
  OS: Linux (x86_64-pc-linux-gnu)
      Ubuntu 22.04.2 LTS
  uname: Linux 5.15.0-1035-azure #42-Ubuntu SMP Tue Feb 28 19:41:23 UTC 2023 x86_64 x86_64
  CPU: Intel(R) Xeon(R) Platinum 8171M CPU @ 2.60GHz: 
              speed         user         nice          sys         idle          irq
       #1  2095 MHz       1189 s          0 s        211 s      11089 s          0 s
       #2  2095 MHz       9652 s          0 s        234 s       2621 s          0 s
       
  Memory: 6.781208038330078 GB (3557.52734375 MB free)
  Uptime: 1260.01 sec
  Load Avg:  1.03  1.05  0.82
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-12.0.1 (ORCJIT, skylake-avx512)
```

---
# Target result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmark: 14 Apr 2023 - 1:35
* Package commit: 257197
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
| `["append!!", "eduction"]`                                     |  22.001 μs (5%) |         |  53.98 KiB (1%) |           8 |
| `["append!!", "xf"]`                                           |  19.501 μs (5%) |         |  53.98 KiB (1%) |           8 |
| `["cartesian", "copyto!", "iter"]`                             |   3.350 μs (5%) |         |                 |             |
| `["cartesian", "copyto!", "man"]`                              |   3.900 μs (5%) |         |                 |             |
| `["cartesian", "copyto!", "xf"]`                               |   2.800 μs (5%) |         |                 |             |
| `["cat", "base"]`                                              |   1.950 μs (5%) |         |                 |             |
| `["cat", "xf"]`                                                |   1.590 μs (5%) |         |                 |             |
| `["collect", "filter-missing"]`                                |  58.403 μs (5%) |         |  41.33 KiB (1%) |          10 |
| `["collect", "identity-float"]`                                |  20.501 μs (5%) |         | 326.61 KiB (1%) |          10 |
| `["collect", "identity-union"]`                                | 135.607 μs (5%) |         | 679.41 KiB (1%) |       10010 |
| `["dict", "base"]`                                             |   3.658 ms (5%) |         |  92.45 KiB (1%) |          22 |
| `["dict", "xf"]`                                               |   3.753 ms (5%) |         |  91.95 KiB (1%) |          18 |
| `["dot", "blas"]`                                              |   1.290 μs (5%) |         |                 |             |
| `["dot", "man"]`                                               |   1.840 μs (5%) |         |                 |             |
| `["dot", "rf"]`                                                |   1.860 μs (5%) |         |                 |             |
| `["dot", "xf"]`                                                |   1.860 μs (5%) |         |                 |             |
| `["filter_map_map!", "man"]`                                   |  57.902 μs (5%) |         |                 |             |
| `["filter_map_map!", "xf"]`                                    |  64.102 μs (5%) |         |                 |             |
| `["filter_map_reduce", "man"]`                                 | 191.708 μs (5%) |         |                 |             |
| `["filter_map_reduce", "xf"]`                                  | 192.808 μs (5%) |         |                 |             |
| `["filter_sum", "1000", "RandomFloats", "noinit", "base"]`     |   2.922 μs (5%) |         |                 |             |
| `["filter_sum", "1000", "RandomFloats", "noinit", "naive"]`    |   1.330 μs (5%) |         |                 |             |
| `["filter_sum", "1000", "RandomFloats", "noinit", "xf"]`       |   1.720 μs (5%) |         |                 |             |
| `["filter_sum", "1000", "RandomFloats", "withinit", "base"]`   |   1.720 μs (5%) |         |                 |             |
| `["filter_sum", "1000", "RandomFloats", "withinit", "naive"]`  | 669.435 ns (5%) |         |                 |             |
| `["filter_sum", "1000", "RandomFloats", "withinit", "xf"]`     |   1.720 μs (5%) |         |                 |             |
| `["filter_sum", "1000", "UnitRange", "noinit", "base"]`        | 943.792 ns (5%) |         |                 |             |
| `["filter_sum", "1000", "UnitRange", "noinit", "naive"]`       |   1.127 μs (5%) |         |                 |             |
| `["filter_sum", "1000", "UnitRange", "noinit", "xf"]`          | 181.134 ns (5%) |         |                 |             |
| `["filter_sum", "1000", "UnitRange", "withinit", "base"]`      | 126.346 ns (5%) |         |                 |             |
| `["filter_sum", "1000", "UnitRange", "withinit", "naive"]`     | 885.755 ns (5%) |         |                 |             |
| `["filter_sum", "1000", "UnitRange", "withinit", "xf"]`        | 133.686 ns (5%) |         |                 |             |
| `["filter_sum", "10000", "RandomFloats", "noinit", "base"]`    |  25.301 μs (5%) |         |                 |             |
| `["filter_sum", "10000", "RandomFloats", "noinit", "naive"]`   |  37.902 μs (5%) |         |                 |             |
| `["filter_sum", "10000", "RandomFloats", "noinit", "xf"]`      |  17.500 μs (5%) |         |                 |             |
| `["filter_sum", "10000", "RandomFloats", "withinit", "base"]`  |  17.500 μs (5%) |         |                 |             |
| `["filter_sum", "10000", "RandomFloats", "withinit", "naive"]` |  26.101 μs (5%) |         |                 |             |
| `["filter_sum", "10000", "RandomFloats", "withinit", "xf"]`    |  17.500 μs (5%) |         |                 |             |
| `["filter_sum", "10000", "UnitRange", "noinit", "base"]`       |   9.300 μs (5%) |         |                 |             |
| `["filter_sum", "10000", "UnitRange", "noinit", "naive"]`      |   8.400 μs (5%) |         |                 |             |
| `["filter_sum", "10000", "UnitRange", "noinit", "xf"]`         |   1.760 μs (5%) |         |                 |             |
| `["filter_sum", "10000", "UnitRange", "withinit", "base"]`     |   1.180 μs (5%) |         |                 |             |
| `["filter_sum", "10000", "UnitRange", "withinit", "naive"]`    |   7.534 μs (5%) |         |                 |             |
| `["filter_sum", "10000", "UnitRange", "withinit", "xf"]`       |   1.180 μs (5%) |         |                 |             |
| `["findall", "base"]`                                          | 127.006 μs (5%) |         | 797.20 KiB (1%) |           8 |
| `["findall", "xf-array"]`                                      |   1.279 ms (5%) |         |   2.94 MiB (1%) |       96426 |
| `["findall", "xf-iter"]`                                       | 760.336 μs (5%) |         |   1.83 MiB (1%) |          14 |
| `["gemm", "fusedmul", "blas", "16"]`                           |   2.786 ms (5%) |         |                 |             |
| `["gemm", "fusedmul", "blas", "2"]`                            |   2.133 ms (5%) |         |                 |             |
| `["gemm", "fusedmul", "blas", "32"]`                           |   3.489 ms (5%) |         |                 |             |
| `["gemm", "fusedmul", "blas", "8"]`                            |   2.258 ms (5%) |         |                 |             |
| `["gemm", "fusedmul", "xf", "16"]`                             |   5.627 ms (5%) |         |  192 bytes (1%) |           4 |
| `["gemm", "fusedmul", "xf", "2"]`                              | 701.326 μs (5%) |         |  192 bytes (1%) |           4 |
| `["gemm", "fusedmul", "xf", "32"]`                             |  11.593 ms (5%) |         |  192 bytes (1%) |           4 |
| `["gemm", "fusedmul", "xf", "8"]`                              |   2.763 ms (5%) |         |  192 bytes (1%) |           4 |
| `["gemm", "mul", "linalg", "256"]`                             | 452.614 μs (5%) |         |                 |             |
| `["gemm", "mul", "linalg", "32"]`                              |   1.510 μs (5%) |         |                 |             |
| `["gemm", "mul", "linalg", "8"]`                               | 209.613 ns (5%) |         |                 |             |
| `["gemm", "mul", "man", "false", "256"]`                       |   3.046 ms (5%) |         |                 |             |
| `["gemm", "mul", "man", "false", "32"]`                        |   5.400 μs (5%) |         |                 |             |
| `["gemm", "mul", "man", "false", "8"]`                         | 331.328 ns (5%) |         |                 |             |
| `["gemm", "mul", "man", "ivdep", "256"]`                       |   3.012 ms (5%) |         |                 |             |
| `["gemm", "mul", "man", "ivdep", "32"]`                        |   4.450 μs (5%) |         |                 |             |
| `["gemm", "mul", "man", "ivdep", "8"]`                         | 313.952 ns (5%) |         |                 |             |
| `["gemm", "mul", "man", "true", "256"]`                        |   2.980 ms (5%) |         |                 |             |
| `["gemm", "mul", "man", "true", "32"]`                         |   4.984 μs (5%) |         |                 |             |
| `["gemm", "mul", "man", "true", "8"]`                          | 393.050 ns (5%) |         |                 |             |
| `["gemm", "mul", "xf", "false", "256"]`                        |   3.060 ms (5%) |         |   80 bytes (1%) |           3 |
| `["gemm", "mul", "xf", "false", "32"]`                         |   5.480 μs (5%) |         |   80 bytes (1%) |           3 |
| `["gemm", "mul", "xf", "false", "8"]`                          | 373.753 ns (5%) |         |   80 bytes (1%) |           3 |
| `["gemm", "mul", "xf", "ivdep", "256"]`                        |   3.011 ms (5%) |         |   80 bytes (1%) |           3 |
| `["gemm", "mul", "xf", "ivdep", "32"]`                         |   5.350 μs (5%) |         |   80 bytes (1%) |           3 |
| `["gemm", "mul", "xf", "ivdep", "8"]`                          | 394.020 ns (5%) |         |   80 bytes (1%) |           3 |
| `["gemm", "mul", "xf", "true", "256"]`                         |   3.028 ms (5%) |         |   80 bytes (1%) |           3 |
| `["gemm", "mul", "xf", "true", "32"]`                          |   5.900 μs (5%) |         |   80 bytes (1%) |           3 |
| `["gemm", "mul", "xf", "true", "8"]`                           | 466.688 ns (5%) |         |   80 bytes (1%) |           3 |
| `["groupby", "sum", "sac"]`                                    | 127.204 μs (5%) |         |   1.64 KiB (1%) |          11 |
| `["groupby", "sum", "xf-with-init"]`                           | 121.303 μs (5%) |         |   1.05 KiB (1%) |           9 |
| `["groupby", "sum", "xf-without-init"]`                        | 137.005 μs (5%) |         |   1.05 KiB (1%) |           9 |
| `["mapcat_eduction", "base"]`                                  |  39.902 μs (5%) |         |                 |             |
| `["mapcat_eduction", "xf-eduction"]`                           |   1.630 μs (5%) |         |                 |             |
| `["mapcat_eduction", "xf-xf"]`                                 |   1.630 μs (5%) |         |                 |             |
| `["missing_argmax", "man"]`                                    |   2.222 μs (5%) |         |                 |             |
| `["missing_argmax", "rf"]`                                     |   1.450 μs (5%) |         |                 |             |
| `["missing_argmax", "xf"]`                                     |   1.340 μs (5%) |         |   32 bytes (1%) |           1 |
| `["missing_dot", "equiv"]`                                     |   2.800 μs (5%) |         |   16 bytes (1%) |           1 |
| `["missing_dot", "man"]`                                       |   1.350 μs (5%) |         |   16 bytes (1%) |           1 |
| `["missing_dot", "naive"]`                                     |   2.678 μs (5%) |         |   16 bytes (1%) |           1 |
| `["missing_dot", "rf"]`                                        |   1.190 μs (5%) |         |   16 bytes (1%) |           1 |
| `["missing_dot", "rf_nota"]`                                   |   2.767 μs (5%) |         |   16 bytes (1%) |           1 |
| `["missing_dot", "xf"]`                                        |  86.802 μs (5%) |         |  72.19 KiB (1%) |        3744 |
| `["missing_dot", "xf_nota"]`                                   |  84.203 μs (5%) |         |  72.31 KiB (1%) |        3750 |
| `["overhead", "foldl"]`                                        |   3.600 ns (5%) |         |                 |             |
| `["overhead", "reduce_basecase"]`                              |  85.357 ns (5%) |         |   16 bytes (1%) |           1 |
| `["partition_by", "man"]`                                      |   2.315 ms (5%) |         |  480 bytes (1%) |           3 |
| `["partition_by", "xf"]`                                       |   2.596 ms (5%) |         |  592 bytes (1%) |           5 |
| `["set", "base"]`                                              |   4.088 ms (5%) |         |  49.14 KiB (1%) |          17 |
| `["set", "xf"]`                                                |   3.946 ms (5%) |         |  49.17 KiB (1%) |          19 |
| `["sum_transpose", "30", "noinit", "iter"]`                    |   2.000 μs (5%) |         |                 |             |
| `["sum_transpose", "30", "noinit", "man"]`                     |   2.744 μs (5%) |         |                 |             |
| `["sum_transpose", "30", "noinit", "xf"]`                      |   1.110 μs (5%) |         |                 |             |
| `["sum_transpose", "30", "withinit", "iter"]`                  |   1.170 μs (5%) |         |                 |             |
| `["sum_transpose", "30", "withinit", "man"]`                   |   1.110 μs (5%) |         |                 |             |
| `["sum_transpose", "30", "withinit", "xf"]`                    |   1.109 μs (5%) |         |                 |             |
| `["teerf_filter", "noinit"]`                                   | 365.896 ns (5%) |         |   80 bytes (1%) |           3 |
| `["teerf_filter", "withinit"]`                                 | 178.402 ns (5%) |         |                 |             |

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
      Ubuntu 22.04.2 LTS
  uname: Linux 5.15.0-1035-azure #42-Ubuntu SMP Tue Feb 28 19:41:23 UTC 2023 x86_64 x86_64
  CPU: Intel(R) Xeon(R) Platinum 8171M CPU @ 2.60GHz: 
              speed         user         nice          sys         idle          irq
       #1  2095 MHz        519 s          0 s        181 s       8728 s          0 s
       #2  2095 MHz       7225 s          0 s        188 s       2025 s          0 s
       
  Memory: 6.781208038330078 GB (3701.3203125 MB free)
  Uptime: 952.69 sec
  Load Avg:  1.0  0.98  0.68
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-12.0.1 (ORCJIT, skylake-avx512)
```

---
# Baseline result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmark: 14 Apr 2023 - 1:40
* Package commit: f8d0df
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
| `["append!!", "eduction"]`                                     |  17.901 μs (5%) |         |  53.98 KiB (1%) |           8 |
| `["append!!", "xf"]`                                           |  16.100 μs (5%) |         |  53.98 KiB (1%) |           8 |
| `["cartesian", "copyto!", "iter"]`                             |   3.075 μs (5%) |         |                 |             |
| `["cartesian", "copyto!", "man"]`                              |   3.350 μs (5%) |         |                 |             |
| `["cartesian", "copyto!", "xf"]`                               |   2.800 μs (5%) |         |                 |             |
| `["cat", "base"]`                                              |   1.950 μs (5%) |         |                 |             |
| `["cat", "xf"]`                                                |   1.590 μs (5%) |         |                 |             |
| `["collect", "filter-missing"]`                                |  58.302 μs (5%) |         |  41.33 KiB (1%) |          10 |
| `["collect", "identity-float"]`                                |  19.601 μs (5%) |         | 326.61 KiB (1%) |          10 |
| `["collect", "identity-union"]`                                | 144.105 μs (5%) |         | 679.41 KiB (1%) |       10010 |
| `["dict", "base"]`                                             |   3.713 ms (5%) |         |  92.45 KiB (1%) |          22 |
| `["dict", "xf"]`                                               |   3.811 ms (5%) |         |  91.95 KiB (1%) |          18 |
| `["dot", "blas"]`                                              |   1.020 μs (5%) |         |                 |             |
| `["dot", "man"]`                                               |   1.580 μs (5%) |         |                 |             |
| `["dot", "rf"]`                                                |   1.850 μs (5%) |         |                 |             |
| `["dot", "xf"]`                                                |   1.850 μs (5%) |         |                 |             |
| `["filter_map_map!", "man"]`                                   |  60.402 μs (5%) |         |                 |             |
| `["filter_map_map!", "xf"]`                                    |  61.401 μs (5%) |         |                 |             |
| `["filter_map_reduce", "man"]`                                 | 191.802 μs (5%) |         |                 |             |
| `["filter_map_reduce", "xf"]`                                  | 192.005 μs (5%) |         |                 |             |
| `["filter_sum", "1000", "RandomFloats", "noinit", "base"]`     |   2.922 μs (5%) |         |                 |             |
| `["filter_sum", "1000", "RandomFloats", "noinit", "naive"]`    |   1.330 μs (5%) |         |                 |             |
| `["filter_sum", "1000", "RandomFloats", "noinit", "xf"]`       |   1.970 μs (5%) |         |                 |             |
| `["filter_sum", "1000", "RandomFloats", "withinit", "base"]`   |   1.980 μs (5%) |         |                 |             |
| `["filter_sum", "1000", "RandomFloats", "withinit", "naive"]`  | 670.018 ns (5%) |         |                 |             |
| `["filter_sum", "1000", "RandomFloats", "withinit", "xf"]`     |   1.720 μs (5%) |         |                 |             |
| `["filter_sum", "1000", "UnitRange", "noinit", "base"]`        | 937.521 ns (5%) |         |                 |             |
| `["filter_sum", "1000", "UnitRange", "noinit", "naive"]`       | 980.000 ns (5%) |         |                 |             |
| `["filter_sum", "1000", "UnitRange", "noinit", "xf"]`          | 156.755 ns (5%) |         |                 |             |
| `["filter_sum", "1000", "UnitRange", "withinit", "base"]`      | 125.227 ns (5%) |         |                 |             |
| `["filter_sum", "1000", "UnitRange", "withinit", "naive"]`     | 883.694 ns (5%) |         |                 |             |
| `["filter_sum", "1000", "UnitRange", "withinit", "xf"]`        | 117.881 ns (5%) |         |                 |             |
| `["filter_sum", "10000", "RandomFloats", "noinit", "base"]`    |  29.400 μs (5%) |         |                 |             |
| `["filter_sum", "10000", "RandomFloats", "noinit", "naive"]`   |  38.001 μs (5%) |         |                 |             |
| `["filter_sum", "10000", "RandomFloats", "noinit", "xf"]`      |  17.500 μs (5%) |         |                 |             |
| `["filter_sum", "10000", "RandomFloats", "withinit", "base"]`  |  17.500 μs (5%) |         |                 |             |
| `["filter_sum", "10000", "RandomFloats", "withinit", "naive"]` |  26.400 μs (5%) |         |                 |             |
| `["filter_sum", "10000", "RandomFloats", "withinit", "xf"]`    |  15.100 μs (5%) |         |                 |             |
| `["filter_sum", "10000", "UnitRange", "noinit", "base"]`       |   9.400 μs (5%) |         |                 |             |
| `["filter_sum", "10000", "UnitRange", "noinit", "naive"]`      |   9.700 μs (5%) |         |                 |             |
| `["filter_sum", "10000", "UnitRange", "noinit", "xf"]`         |   1.770 μs (5%) |         |                 |             |
| `["filter_sum", "10000", "UnitRange", "withinit", "base"]`     |   1.370 μs (5%) |         |                 |             |
| `["filter_sum", "10000", "UnitRange", "withinit", "naive"]`    |   8.733 μs (5%) |         |                 |             |
| `["filter_sum", "10000", "UnitRange", "withinit", "xf"]`       |   1.360 μs (5%) |         |                 |             |
| `["findall", "base"]`                                          | 124.505 μs (5%) |         | 797.20 KiB (1%) |           8 |
| `["findall", "xf-array"]`                                      |   1.251 ms (5%) |         |   2.94 MiB (1%) |       96426 |
| `["findall", "xf-iter"]`                                       | 736.623 μs (5%) |         |   1.83 MiB (1%) |          14 |
| `["gemm", "fusedmul", "blas", "16"]`                           |   2.815 ms (5%) |         |                 |             |
| `["gemm", "fusedmul", "blas", "2"]`                            |   2.153 ms (5%) |         |                 |             |
| `["gemm", "fusedmul", "blas", "32"]`                           |   3.435 ms (5%) |         |                 |             |
| `["gemm", "fusedmul", "blas", "8"]`                            |   2.259 ms (5%) |         |                 |             |
| `["gemm", "fusedmul", "xf", "16"]`                             |   5.643 ms (5%) |         |  192 bytes (1%) |           4 |
| `["gemm", "fusedmul", "xf", "2"]`                              | 714.020 μs (5%) |         |  192 bytes (1%) |           4 |
| `["gemm", "fusedmul", "xf", "32"]`                             |  11.493 ms (5%) |         |  192 bytes (1%) |           4 |
| `["gemm", "fusedmul", "xf", "8"]`                              |   2.766 ms (5%) |         |  192 bytes (1%) |           4 |
| `["gemm", "mul", "linalg", "256"]`                             | 500.316 μs (5%) |         |                 |             |
| `["gemm", "mul", "linalg", "32"]`                              |   1.700 μs (5%) |         |                 |             |
| `["gemm", "mul", "linalg", "8"]`                               | 200.000 ns (5%) |         |                 |             |
| `["gemm", "mul", "man", "false", "256"]`                       |   3.020 ms (5%) |         |                 |             |
| `["gemm", "mul", "man", "false", "32"]`                        |   6.400 μs (5%) |         |                 |             |
| `["gemm", "mul", "man", "false", "8"]`                         | 400.000 ns (5%) |         |                 |             |
| `["gemm", "mul", "man", "ivdep", "256"]`                       |   3.003 ms (5%) |         |                 |             |
| `["gemm", "mul", "man", "ivdep", "32"]`                        |   4.600 μs (5%) |         |                 |             |
| `["gemm", "mul", "man", "ivdep", "8"]`                         | 300.000 ns (5%) |         |                 |             |
| `["gemm", "mul", "man", "true", "256"]`                        |   3.028 ms (5%) |         |                 |             |
| `["gemm", "mul", "man", "true", "32"]`                         |   6.100 μs (5%) |         |                 |             |
| `["gemm", "mul", "man", "true", "8"]`                          | 400.000 ns (5%) |         |                 |             |
| `["gemm", "mul", "xf", "false", "256"]`                        |   3.049 ms (5%) |         |   80 bytes (1%) |           3 |
| `["gemm", "mul", "xf", "false", "32"]`                         |   6.500 μs (5%) |         |   80 bytes (1%) |           3 |
| `["gemm", "mul", "xf", "false", "8"]`                          | 500.000 ns (5%) |         |   80 bytes (1%) |           3 |
| `["gemm", "mul", "xf", "ivdep", "256"]`                        |   3.002 ms (5%) |         |   80 bytes (1%) |           3 |
| `["gemm", "mul", "xf", "ivdep", "32"]`                         |   5.400 μs (5%) |         |   80 bytes (1%) |           3 |
| `["gemm", "mul", "xf", "ivdep", "8"]`                          | 400.000 ns (5%) |         |   80 bytes (1%) |           3 |
| `["gemm", "mul", "xf", "true", "256"]`                         |   3.034 ms (5%) |         |   80 bytes (1%) |           3 |
| `["gemm", "mul", "xf", "true", "32"]`                          |   6.200 μs (5%) |         |   80 bytes (1%) |           3 |
| `["gemm", "mul", "xf", "true", "8"]`                           | 400.000 ns (5%) |         |   80 bytes (1%) |           3 |
| `["groupby", "sum", "sac"]`                                    |   8.463 ms (5%) |         |  13.14 KiB (1%) |         103 |
| `["groupby", "sum", "xf-with-init"]`                           | 118.103 μs (5%) |         |   1.05 KiB (1%) |           9 |
| `["groupby", "sum", "xf-without-init"]`                        | 115.203 μs (5%) |         |   1.05 KiB (1%) |           9 |
| `["mapcat_eduction", "base"]`                                  |  47.001 μs (5%) |         |                 |             |
| `["mapcat_eduction", "xf-eduction"]`                           |   1.640 μs (5%) |         |                 |             |
| `["mapcat_eduction", "xf-xf"]`                                 |   1.410 μs (5%) |         |                 |             |
| `["missing_argmax", "man"]`                                    |   2.589 μs (5%) |         |                 |             |
| `["missing_argmax", "rf"]`                                     |   1.600 μs (5%) |         |                 |             |
| `["missing_argmax", "xf"]`                                     |   1.540 μs (5%) |         |   32 bytes (1%) |           1 |
| `["missing_dot", "equiv"]`                                     |   2.278 μs (5%) |         |   16 bytes (1%) |           1 |
| `["missing_dot", "man"]`                                       |   1.380 μs (5%) |         |   16 bytes (1%) |           1 |
| `["missing_dot", "naive"]`                                     |   2.833 μs (5%) |         |   16 bytes (1%) |           1 |
| `["missing_dot", "rf"]`                                        |   1.180 μs (5%) |         |   16 bytes (1%) |           1 |
| `["missing_dot", "rf_nota"]`                                   |   2.289 μs (5%) |         |   16 bytes (1%) |           1 |
| `["missing_dot", "xf"]`                                        |  94.803 μs (5%) |         |  72.17 KiB (1%) |        3744 |
| `["missing_dot", "xf_nota"]`                                   |  80.203 μs (5%) |         |  71.92 KiB (1%) |        3733 |
| `["overhead", "foldl"]`                                        |   3.200 ns (5%) |         |                 |             |
| `["overhead", "reduce_basecase"]`                              |  90.625 ns (5%) |         |   16 bytes (1%) |           1 |
| `["partition_by", "man"]`                                      |   2.381 ms (5%) |         |  480 bytes (1%) |           3 |
| `["partition_by", "xf"]`                                       |   2.687 ms (5%) |         |  592 bytes (1%) |           5 |
| `["set", "base"]`                                              |   4.199 ms (5%) |         |  49.14 KiB (1%) |          17 |
| `["set", "xf"]`                                                |   3.958 ms (5%) |         |  49.17 KiB (1%) |          19 |
| `["sum_transpose", "30", "noinit", "iter"]`                    |   2.000 μs (5%) |         |                 |             |
| `["sum_transpose", "30", "noinit", "man"]`                     |   2.744 μs (5%) |         |                 |             |
| `["sum_transpose", "30", "noinit", "xf"]`                      |   1.110 μs (5%) |         |                 |             |
| `["sum_transpose", "30", "withinit", "iter"]`                  |   1.490 μs (5%) |         |                 |             |
| `["sum_transpose", "30", "withinit", "man"]`                   |   1.110 μs (5%) |         |                 |             |
| `["sum_transpose", "30", "withinit", "xf"]`                    |   1.114 μs (5%) |         |                 |             |
| `["teerf_filter", "noinit"]`                                   | 360.673 ns (5%) |         |   80 bytes (1%) |           3 |
| `["teerf_filter", "withinit"]`                                 | 179.113 ns (5%) |         |                 |             |

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
      Ubuntu 22.04.2 LTS
  uname: Linux 5.15.0-1035-azure #42-Ubuntu SMP Tue Feb 28 19:41:23 UTC 2023 x86_64 x86_64
  CPU: Intel(R) Xeon(R) Platinum 8171M CPU @ 2.60GHz: 
              speed         user         nice          sys         idle          irq
       #1  2095 MHz       1189 s          0 s        211 s      11089 s          0 s
       #2  2095 MHz       9652 s          0 s        234 s       2621 s          0 s
       
  Memory: 6.781208038330078 GB (3557.52734375 MB free)
  Uptime: 1260.01 sec
  Load Avg:  1.03  1.05  0.82
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-12.0.1 (ORCJIT, skylake-avx512)
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
    Model name:                      Intel(R) Xeon(R) Platinum 8171M CPU @ 2.60GHz
    CPU family:                      6
    Model:                           85
    Thread(s) per core:              1
    Core(s) per socket:              2
    Socket(s):                       1
    Stepping:                        4
    BogoMIPS:                        4190.37
    Flags:                           fpu vme de pse tsc msr pae mce cx8 apic sep mtrr pge mca cmov pat pse36 clflush mmx fxsr sse sse2 ss ht syscall nx pdpe1gb rdtscp lm constant_tsc rep_good nopl xtopology cpuid pni pclmulqdq ssse3 fma cx16 pcid sse4_1 sse4_2 movbe popcnt aes xsave avx f16c rdrand hypervisor lahf_lm abm 3dnowprefetch invpcid_single pti fsgsbase bmi1 hle avx2 smep bmi2 erms invpcid rtm avx512f avx512dq rdseed adx smap clflushopt avx512cd avx512bw avx512vl xsaveopt xsavec xsaves md_clear
    Hypervisor vendor:               Microsoft
    Virtualization type:             full
    L1d cache:                       64 KiB (2 instances)
    L1i cache:                       64 KiB (2 instances)
    L2 cache:                        2 MiB (2 instances)
    L3 cache:                        35.8 MiB (1 instance)
    NUMA node(s):                    1
    NUMA node0 CPU(s):               0,1
    Vulnerability Itlb multihit:     KVM: Mitigation: VMX unsupported
    Vulnerability L1tf:              Mitigation; PTE Inversion
    Vulnerability Mds:               Mitigation; Clear CPU buffers; SMT Host state unknown
    Vulnerability Meltdown:          Mitigation; PTI
    Vulnerability Mmio stale data:   Vulnerable: Clear CPU buffers attempted, no microcode; SMT Host state unknown
    Vulnerability Retbleed:          Vulnerable
    Vulnerability Spec store bypass: Vulnerable
    Vulnerability Spectre v1:        Mitigation; usercopy/swapgs barriers and __user pointer sanitization
    Vulnerability Spectre v2:        Mitigation; Retpolines, STIBP disabled, RSB filling, PBRSB-eIBRS Not affected
    Vulnerability Srbds:             Not affected
    Vulnerability Tsx async abort:   Mitigation; Clear CPU buffers; SMT Host state unknown
    

| Cpu Property       | Value                                                   |
|:------------------ |:------------------------------------------------------- |
| Brand              | Intel(R) Xeon(R) Platinum 8171M CPU @ 2.60GHz           |
| Vendor             | :Intel                                                  |
| Architecture       | :Skylake                                                |
| Model              | Family: 0x06, Model: 0x55, Stepping: 0x04, Type: 0x00   |
| Cores              | 2 physical cores, 2 logical cores (on executing CPU)    |
|                    | No Hyperthreading hardware capability detected          |
| Clock Frequencies  | Not supported by CPU                                    |
| Data Cache         | Level 1:3 : (32, 1024, 36608) kbytes                    |
|                    | 64 byte cache line size                                 |
| Address Size       | 48 bits virtual, 46 bits physical                       |
| SIMD               | 512 bit = 64 byte max. SIMD vector size                 |
| Time Stamp Counter | TSC is accessible via `rdtsc`                           |
|                    | TSC increased at every clock cycle (non-invariant TSC)  |
| Perf. Monitoring   | Performance Monitoring Counters (PMC) are not supported |
| Hypervisor         | Yes, Microsoft                                          |

