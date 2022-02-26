# Benchmark result

* Pull request commit: [`209dea968667816dbeee15ce3477baae3d3c50e4`](https://github.com/JuliaFolds/Transducers.jl/commit/209dea968667816dbeee15ce3477baae3d3c50e4)
* Pull request: <https://github.com/JuliaFolds/Transducers.jl/pull/243> (Update */Manifest.toml)

# Judge result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmarks:
    - Target: 26 Feb 2022 - 01:22
    - Baseline: 26 Feb 2022 - 01:26
* Package commits:
    - Target: be0634
    - Baseline: 39038b
* Julia commits:
    - Target: bf5349
    - Baseline: bf5349
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
| `["cartesian", "copyto!", "iter"]`                             |                1.09 (5%) :x: |                   1.00 (1%)  |
| `["collect", "identity-float"]`                                |                1.08 (5%) :x: |                   1.00 (1%)  |
| `["findall", "xf-array"]`                                      |                1.10 (5%) :x: |                   1.00 (1%)  |
| `["gemm", "mul", "linalg", "256"]`                             |                1.08 (5%) :x: |                   1.00 (1%)  |
| `["gemm", "mul", "linalg", "32"]`                              | 0.91 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["gemm", "mul", "linalg", "8"]`                               |                1.06 (5%) :x: |                   1.00 (1%)  |
| `["gemm", "mul", "man", "false", "256"]`                       | 0.93 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["gemm", "mul", "man", "false", "32"]`                        | 0.85 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["gemm", "mul", "man", "false", "8"]`                         |                1.17 (5%) :x: |                   1.00 (1%)  |
| `["gemm", "mul", "man", "ivdep", "256"]`                       | 0.92 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["gemm", "mul", "man", "ivdep", "8"]`                         |                1.11 (5%) :x: |                   1.00 (1%)  |
| `["gemm", "mul", "man", "true", "256"]`                        | 0.92 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["gemm", "mul", "man", "true", "8"]`                          |                1.13 (5%) :x: |                   1.00 (1%)  |
| `["gemm", "mul", "xf", "false", "256"]`                        | 0.93 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["gemm", "mul", "xf", "false", "8"]`                          | 0.79 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["gemm", "mul", "xf", "ivdep", "256"]`                        | 0.92 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["gemm", "mul", "xf", "true", "256"]`                         | 0.93 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["gemm", "mul", "xf", "true", "32"]`                          | 0.94 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["gemm", "mul", "xf", "true", "8"]`                           | 0.79 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["groupby", "sum", "sac"]`                                    | 0.02 (5%) :white_check_mark: | 0.12 (1%) :white_check_mark: |
| `["groupby", "sum", "xf-with-init"]`                           | 0.95 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["missing_dot", "rf_nota"]`                                   | 0.75 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["sum_transpose", "30", "withinit", "iter"]`                  | 0.71 (5%) :white_check_mark: |                   1.00 (1%)  |

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
Julia Version 1.7.2
Commit bf53498635 (2022-02-06 15:21 UTC)
Platform Info:
  OS: Linux (x86_64-pc-linux-gnu)
      Ubuntu 20.04.3 LTS
  uname: Linux 5.11.0-1028-azure #31~20.04.2-Ubuntu SMP Tue Jan 18 08:46:15 UTC 2022 x86_64 x86_64
  CPU: Intel(R) Xeon(R) Platinum 8272CL CPU @ 2.60GHz: 
              speed         user         nice          sys         idle          irq
       #1  2593 MHz       6553 s          2 s        128 s        731 s          0 s
       #2  2593 MHz        605 s          0 s         98 s       6716 s          0 s
       
  Memory: 6.7845458984375 GB (3812.734375 MB free)
  Uptime: 746.63 sec
  Load Avg:  1.0  0.95  0.61
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-12.0.1 (ORCJIT, skylake-avx512)
```

### Baseline
```
Julia Version 1.7.2
Commit bf53498635 (2022-02-06 15:21 UTC)
Platform Info:
  OS: Linux (x86_64-pc-linux-gnu)
      Ubuntu 20.04.3 LTS
  uname: Linux 5.11.0-1028-azure #31~20.04.2-Ubuntu SMP Tue Jan 18 08:46:15 UTC 2022 x86_64 x86_64
  CPU: Intel(R) Xeon(R) Platinum 8272CL CPU @ 2.60GHz: 
              speed         user         nice          sys         idle          irq
       #1  2593 MHz       9240 s          2 s        168 s        804 s          0 s
       #2  2593 MHz        730 s          0 s        121 s       9358 s          0 s
       
  Memory: 6.7845458984375 GB (3723.83984375 MB free)
  Uptime: 1026.71 sec
  Load Avg:  1.21  1.1  0.77
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-12.0.1 (ORCJIT, skylake-avx512)
```

---
# Target result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmark: 26 Feb 2022 - 1:22
* Package commit: be0634
* Julia commit: bf5349
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
| `["append!!", "eduction"]`                                     |  16.500 μs (5%) |         |  53.98 KiB (1%) |           8 |
| `["append!!", "xf"]`                                           |  16.600 μs (5%) |         |  53.98 KiB (1%) |           8 |
| `["cartesian", "copyto!", "iter"]`                             |   3.550 μs (5%) |         |                 |             |
| `["cartesian", "copyto!", "man"]`                              |   3.562 μs (5%) |         |                 |             |
| `["cartesian", "copyto!", "xf"]`                               |   2.978 μs (5%) |         |                 |             |
| `["cat", "base"]`                                              |   1.780 μs (5%) |         |                 |             |
| `["cat", "xf"]`                                                |   1.470 μs (5%) |         |                 |             |
| `["collect", "filter-missing"]`                                |  61.100 μs (5%) |         |  41.33 KiB (1%) |          10 |
| `["collect", "identity-float"]`                                |  19.901 μs (5%) |         | 326.61 KiB (1%) |          10 |
| `["collect", "identity-union"]`                                | 149.002 μs (5%) |         | 679.41 KiB (1%) |       10010 |
| `["dict", "base"]`                                             |   3.323 ms (5%) |         |  92.45 KiB (1%) |          22 |
| `["dict", "xf"]`                                               |   3.415 ms (5%) |         |  91.95 KiB (1%) |          18 |
| `["dot", "blas"]`                                              |   1.090 μs (5%) |         |                 |             |
| `["dot", "man"]`                                               |   1.710 μs (5%) |         |                 |             |
| `["dot", "rf"]`                                                |   1.740 μs (5%) |         |                 |             |
| `["dot", "xf"]`                                                |   1.720 μs (5%) |         |                 |             |
| `["filter_map_map!", "man"]`                                   |  50.701 μs (5%) |         |                 |             |
| `["filter_map_map!", "xf"]`                                    |  54.300 μs (5%) |         |                 |             |
| `["filter_map_reduce", "man"]`                                 | 209.103 μs (5%) |         |                 |             |
| `["filter_map_reduce", "xf"]`                                  | 203.303 μs (5%) |         |                 |             |
| `["filter_sum", "1000", "RandomFloats", "noinit", "base"]`     |   2.644 μs (5%) |         |                 |             |
| `["filter_sum", "1000", "RandomFloats", "noinit", "naive"]`    |   1.220 μs (5%) |         |                 |             |
| `["filter_sum", "1000", "RandomFloats", "noinit", "xf"]`       |   1.570 μs (5%) |         |                 |             |
| `["filter_sum", "1000", "RandomFloats", "withinit", "base"]`   |   1.580 μs (5%) |         |                 |             |
| `["filter_sum", "1000", "RandomFloats", "withinit", "naive"]`  | 610.863 ns (5%) |         |                 |             |
| `["filter_sum", "1000", "RandomFloats", "withinit", "xf"]`     |   1.580 μs (5%) |         |                 |             |
| `["filter_sum", "1000", "UnitRange", "noinit", "base"]`        | 830.318 ns (5%) |         |                 |             |
| `["filter_sum", "1000", "UnitRange", "noinit", "naive"]`       | 895.652 ns (5%) |         |                 |             |
| `["filter_sum", "1000", "UnitRange", "noinit", "xf"]`          | 160.623 ns (5%) |         |                 |             |
| `["filter_sum", "1000", "UnitRange", "withinit", "base"]`      | 115.126 ns (5%) |         |                 |             |
| `["filter_sum", "1000", "UnitRange", "withinit", "naive"]`     | 806.394 ns (5%) |         |                 |             |
| `["filter_sum", "1000", "UnitRange", "withinit", "xf"]`        | 121.774 ns (5%) |         |                 |             |
| `["filter_sum", "10000", "RandomFloats", "noinit", "base"]`    |  26.600 μs (5%) |         |                 |             |
| `["filter_sum", "10000", "RandomFloats", "noinit", "naive"]`   |  34.500 μs (5%) |         |                 |             |
| `["filter_sum", "10000", "RandomFloats", "noinit", "xf"]`      |  16.000 μs (5%) |         |                 |             |
| `["filter_sum", "10000", "RandomFloats", "withinit", "base"]`  |  16.000 μs (5%) |         |                 |             |
| `["filter_sum", "10000", "RandomFloats", "withinit", "naive"]` |  23.800 μs (5%) |         |                 |             |
| `["filter_sum", "10000", "RandomFloats", "withinit", "xf"]`    |  15.900 μs (5%) |         |                 |             |
| `["filter_sum", "10000", "UnitRange", "noinit", "base"]`       |   8.500 μs (5%) |         |                 |             |
| `["filter_sum", "10000", "UnitRange", "noinit", "naive"]`      |   8.867 μs (5%) |         |                 |             |
| `["filter_sum", "10000", "UnitRange", "noinit", "xf"]`         |   1.600 μs (5%) |         |                 |             |
| `["filter_sum", "10000", "UnitRange", "withinit", "base"]`     |   1.080 μs (5%) |         |                 |             |
| `["filter_sum", "10000", "UnitRange", "withinit", "naive"]`    |   7.975 μs (5%) |         |                 |             |
| `["filter_sum", "10000", "UnitRange", "withinit", "xf"]`       |   1.080 μs (5%) |         |                 |             |
| `["findall", "base"]`                                          | 132.402 μs (5%) |         | 797.20 KiB (1%) |           8 |
| `["findall", "xf-array"]`                                      |   1.276 ms (5%) |         |   2.94 MiB (1%) |       96426 |
| `["findall", "xf-iter"]`                                       | 769.410 μs (5%) |         |   1.83 MiB (1%) |          14 |
| `["gemm", "fusedmul", "blas", "16"]`                           |   2.733 ms (5%) |         |                 |             |
| `["gemm", "fusedmul", "blas", "2"]`                            |   2.067 ms (5%) |         |                 |             |
| `["gemm", "fusedmul", "blas", "32"]`                           |   3.337 ms (5%) |         |                 |             |
| `["gemm", "fusedmul", "blas", "8"]`                            |   2.210 ms (5%) |         |                 |             |
| `["gemm", "fusedmul", "xf", "16"]`                             |   5.302 ms (5%) |         |  192 bytes (1%) |           4 |
| `["gemm", "fusedmul", "xf", "2"]`                              | 651.609 μs (5%) |         |  192 bytes (1%) |           4 |
| `["gemm", "fusedmul", "xf", "32"]`                             |  10.541 ms (5%) |         |  192 bytes (1%) |           4 |
| `["gemm", "fusedmul", "xf", "8"]`                              |   2.626 ms (5%) |         |  192 bytes (1%) |           4 |
| `["gemm", "mul", "linalg", "256"]`                             | 487.207 μs (5%) |         |                 |             |
| `["gemm", "mul", "linalg", "32"]`                              |   1.460 μs (5%) |         |                 |             |
| `["gemm", "mul", "linalg", "8"]`                               | 211.593 ns (5%) |         |                 |             |
| `["gemm", "mul", "man", "false", "256"]`                       |   2.661 ms (5%) |         |                 |             |
| `["gemm", "mul", "man", "false", "32"]`                        |   5.800 μs (5%) |         |                 |             |
| `["gemm", "mul", "man", "false", "8"]`                         | 350.467 ns (5%) |         |                 |             |
| `["gemm", "mul", "man", "ivdep", "256"]`                       |   2.614 ms (5%) |         |                 |             |
| `["gemm", "mul", "man", "ivdep", "32"]`                        |   4.814 μs (5%) |         |                 |             |
| `["gemm", "mul", "man", "ivdep", "8"]`                         | 332.432 ns (5%) |         |                 |             |
| `["gemm", "mul", "man", "true", "256"]`                        |   2.612 ms (5%) |         |                 |             |
| `["gemm", "mul", "man", "true", "32"]`                         |   5.517 μs (5%) |         |                 |             |
| `["gemm", "mul", "man", "true", "8"]`                          | 338.609 ns (5%) |         |                 |             |
| `["gemm", "mul", "xf", "false", "256"]`                        |   2.669 ms (5%) |         |   80 bytes (1%) |           3 |
| `["gemm", "mul", "xf", "false", "32"]`                         |   5.900 μs (5%) |         |   80 bytes (1%) |           3 |
| `["gemm", "mul", "xf", "false", "8"]`                          | 395.527 ns (5%) |         |   80 bytes (1%) |           3 |
| `["gemm", "mul", "xf", "ivdep", "256"]`                        |   2.605 ms (5%) |         |   80 bytes (1%) |           3 |
| `["gemm", "mul", "xf", "ivdep", "32"]`                         |   5.050 μs (5%) |         |   80 bytes (1%) |           3 |
| `["gemm", "mul", "xf", "ivdep", "8"]`                          | 380.397 ns (5%) |         |   80 bytes (1%) |           3 |
| `["gemm", "mul", "xf", "true", "256"]`                         |   2.640 ms (5%) |         |   80 bytes (1%) |           3 |
| `["gemm", "mul", "xf", "true", "32"]`                          |   5.367 μs (5%) |         |   80 bytes (1%) |           3 |
| `["gemm", "mul", "xf", "true", "8"]`                           | 394.035 ns (5%) |         |   80 bytes (1%) |           3 |
| `["groupby", "sum", "sac"]`                                    | 123.702 μs (5%) |         |   1.64 KiB (1%) |          11 |
| `["groupby", "sum", "xf-with-init"]`                           | 123.302 μs (5%) |         |   1.05 KiB (1%) |           9 |
| `["groupby", "sum", "xf-without-init"]`                        | 120.901 μs (5%) |         |   1.05 KiB (1%) |           9 |
| `["mapcat_eduction", "base"]`                                  |  42.400 μs (5%) |         |                 |             |
| `["mapcat_eduction", "xf-eduction"]`                           |   1.490 μs (5%) |         |                 |             |
| `["mapcat_eduction", "xf-xf"]`                                 |   1.490 μs (5%) |         |                 |             |
| `["missing_argmax", "man"]`                                    |   2.389 μs (5%) |         |                 |             |
| `["missing_argmax", "rf"]`                                     |   1.500 μs (5%) |         |                 |             |
| `["missing_argmax", "xf"]`                                     |   1.430 μs (5%) |         |   32 bytes (1%) |           1 |
| `["missing_dot", "equiv"]`                                     |   2.120 μs (5%) |         |   16 bytes (1%) |           1 |
| `["missing_dot", "man"]`                                       |   1.270 μs (5%) |         |   16 bytes (1%) |           1 |
| `["missing_dot", "naive"]`                                     |   2.611 μs (5%) |         |   16 bytes (1%) |           1 |
| `["missing_dot", "rf"]`                                        |   1.250 μs (5%) |         |   16 bytes (1%) |           1 |
| `["missing_dot", "rf_nota"]`                                   |   2.120 μs (5%) |         |   16 bytes (1%) |           1 |
| `["missing_dot", "xf"]`                                        |  90.501 μs (5%) |         |  72.19 KiB (1%) |        3744 |
| `["missing_dot", "xf_nota"]`                                   |  89.101 μs (5%) |         |  72.11 KiB (1%) |        3742 |
| `["overhead", "foldl"]`                                        |   3.000 ns (5%) |         |                 |             |
| `["overhead", "reduce_basecase"]`                              |  86.917 ns (5%) |         |   16 bytes (1%) |           1 |
| `["partition_by", "man"]`                                      |   2.217 ms (5%) |         |  480 bytes (1%) |           3 |
| `["partition_by", "xf"]`                                       |   2.367 ms (5%) |         |  592 bytes (1%) |           5 |
| `["set", "base"]`                                              |   3.901 ms (5%) |         |  49.14 KiB (1%) |          17 |
| `["set", "xf"]`                                                |   3.658 ms (5%) |         |  49.17 KiB (1%) |          19 |
| `["sum_transpose", "30", "noinit", "iter"]`                    |   2.111 μs (5%) |         |                 |             |
| `["sum_transpose", "30", "noinit", "man"]`                     |   2.500 μs (5%) |         |                 |             |
| `["sum_transpose", "30", "noinit", "xf"]`                      |   1.080 μs (5%) |         |   32 bytes (1%) |           2 |
| `["sum_transpose", "30", "withinit", "iter"]`                  |   1.120 μs (5%) |         |                 |             |
| `["sum_transpose", "30", "withinit", "man"]`                   |   1.010 μs (5%) |         |                 |             |
| `["sum_transpose", "30", "withinit", "xf"]`                    |   1.080 μs (5%) |         |   48 bytes (1%) |           3 |
| `["teerf_filter", "noinit"]`                                   | 341.096 ns (5%) |         |   80 bytes (1%) |           3 |
| `["teerf_filter", "withinit"]`                                 | 189.556 ns (5%) |         |                 |             |

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
Julia Version 1.7.2
Commit bf53498635 (2022-02-06 15:21 UTC)
Platform Info:
  OS: Linux (x86_64-pc-linux-gnu)
      Ubuntu 20.04.3 LTS
  uname: Linux 5.11.0-1028-azure #31~20.04.2-Ubuntu SMP Tue Jan 18 08:46:15 UTC 2022 x86_64 x86_64
  CPU: Intel(R) Xeon(R) Platinum 8272CL CPU @ 2.60GHz: 
              speed         user         nice          sys         idle          irq
       #1  2593 MHz       6553 s          2 s        128 s        731 s          0 s
       #2  2593 MHz        605 s          0 s         98 s       6716 s          0 s
       
  Memory: 6.7845458984375 GB (3812.734375 MB free)
  Uptime: 746.63 sec
  Load Avg:  1.0  0.95  0.61
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-12.0.1 (ORCJIT, skylake-avx512)
```

---
# Baseline result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmark: 26 Feb 2022 - 1:26
* Package commit: 39038b
* Julia commit: bf5349
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
| `["append!!", "eduction"]`                                     |  16.400 μs (5%) |         |  53.98 KiB (1%) |           8 |
| `["append!!", "xf"]`                                           |  16.300 μs (5%) |         |  53.98 KiB (1%) |           8 |
| `["cartesian", "copyto!", "iter"]`                             |   3.263 μs (5%) |         |                 |             |
| `["cartesian", "copyto!", "man"]`                              |   3.550 μs (5%) |         |                 |             |
| `["cartesian", "copyto!", "xf"]`                               |   2.967 μs (5%) |         |                 |             |
| `["cat", "base"]`                                              |   1.780 μs (5%) |         |                 |             |
| `["cat", "xf"]`                                                |   1.460 μs (5%) |         |                 |             |
| `["collect", "filter-missing"]`                                |  58.401 μs (5%) |         |  41.33 KiB (1%) |          10 |
| `["collect", "identity-float"]`                                |  18.500 μs (5%) |         | 326.61 KiB (1%) |          10 |
| `["collect", "identity-union"]`                                | 152.302 μs (5%) |         | 679.41 KiB (1%) |       10010 |
| `["dict", "base"]`                                             |   3.324 ms (5%) |         |  92.45 KiB (1%) |          22 |
| `["dict", "xf"]`                                               |   3.417 ms (5%) |         |  91.95 KiB (1%) |          18 |
| `["dot", "blas"]`                                              |   1.100 μs (5%) |         |                 |             |
| `["dot", "man"]`                                               |   1.710 μs (5%) |         |                 |             |
| `["dot", "rf"]`                                                |   1.740 μs (5%) |         |                 |             |
| `["dot", "xf"]`                                                |   1.740 μs (5%) |         |                 |             |
| `["filter_map_map!", "man"]`                                   |  50.201 μs (5%) |         |                 |             |
| `["filter_map_map!", "xf"]`                                    |  52.001 μs (5%) |         |                 |             |
| `["filter_map_reduce", "man"]`                                 | 203.303 μs (5%) |         |                 |             |
| `["filter_map_reduce", "xf"]`                                  | 209.102 μs (5%) |         |                 |             |
| `["filter_sum", "1000", "RandomFloats", "noinit", "base"]`     |   2.667 μs (5%) |         |                 |             |
| `["filter_sum", "1000", "RandomFloats", "noinit", "naive"]`    |   1.220 μs (5%) |         |                 |             |
| `["filter_sum", "1000", "RandomFloats", "noinit", "xf"]`       |   1.570 μs (5%) |         |                 |             |
| `["filter_sum", "1000", "RandomFloats", "withinit", "base"]`   |   1.530 μs (5%) |         |                 |             |
| `["filter_sum", "1000", "RandomFloats", "withinit", "naive"]`  | 610.291 ns (5%) |         |                 |             |
| `["filter_sum", "1000", "RandomFloats", "withinit", "xf"]`     |   1.570 μs (5%) |         |                 |             |
| `["filter_sum", "1000", "UnitRange", "noinit", "base"]`        | 856.061 ns (5%) |         |                 |             |
| `["filter_sum", "1000", "UnitRange", "noinit", "naive"]`       | 893.478 ns (5%) |         |                 |             |
| `["filter_sum", "1000", "UnitRange", "noinit", "xf"]`          | 165.804 ns (5%) |         |                 |             |
| `["filter_sum", "1000", "UnitRange", "withinit", "base"]`      | 116.541 ns (5%) |         |                 |             |
| `["filter_sum", "1000", "UnitRange", "withinit", "naive"]`     | 806.394 ns (5%) |         |                 |             |
| `["filter_sum", "1000", "UnitRange", "withinit", "xf"]`        | 122.211 ns (5%) |         |                 |             |
| `["filter_sum", "10000", "RandomFloats", "noinit", "base"]`    |  26.800 μs (5%) |         |                 |             |
| `["filter_sum", "10000", "RandomFloats", "noinit", "naive"]`   |  33.901 μs (5%) |         |                 |             |
| `["filter_sum", "10000", "RandomFloats", "noinit", "xf"]`      |  15.900 μs (5%) |         |                 |             |
| `["filter_sum", "10000", "RandomFloats", "withinit", "base"]`  |  15.900 μs (5%) |         |                 |             |
| `["filter_sum", "10000", "RandomFloats", "withinit", "naive"]` |  24.100 μs (5%) |         |                 |             |
| `["filter_sum", "10000", "RandomFloats", "withinit", "xf"]`    |  15.900 μs (5%) |         |                 |             |
| `["filter_sum", "10000", "UnitRange", "noinit", "base"]`       |   8.467 μs (5%) |         |                 |             |
| `["filter_sum", "10000", "UnitRange", "noinit", "naive"]`      |   8.600 μs (5%) |         |                 |             |
| `["filter_sum", "10000", "UnitRange", "noinit", "xf"]`         |   1.610 μs (5%) |         |                 |             |
| `["filter_sum", "10000", "UnitRange", "withinit", "base"]`     |   1.090 μs (5%) |         |                 |             |
| `["filter_sum", "10000", "UnitRange", "withinit", "naive"]`    |   7.975 μs (5%) |         |                 |             |
| `["filter_sum", "10000", "UnitRange", "withinit", "xf"]`       |   1.090 μs (5%) |         |                 |             |
| `["findall", "base"]`                                          | 132.202 μs (5%) |         | 797.20 KiB (1%) |           8 |
| `["findall", "xf-array"]`                                      |   1.156 ms (5%) |         |   2.94 MiB (1%) |       96426 |
| `["findall", "xf-iter"]`                                       | 771.210 μs (5%) |         |   1.83 MiB (1%) |          14 |
| `["gemm", "fusedmul", "blas", "16"]`                           |   2.740 ms (5%) |         |                 |             |
| `["gemm", "fusedmul", "blas", "2"]`                            |   2.070 ms (5%) |         |                 |             |
| `["gemm", "fusedmul", "blas", "32"]`                           |   3.319 ms (5%) |         |                 |             |
| `["gemm", "fusedmul", "blas", "8"]`                            |   2.197 ms (5%) |         |                 |             |
| `["gemm", "fusedmul", "xf", "16"]`                             |   5.287 ms (5%) |         |  192 bytes (1%) |           4 |
| `["gemm", "fusedmul", "xf", "2"]`                              | 661.609 μs (5%) |         |  192 bytes (1%) |           4 |
| `["gemm", "fusedmul", "xf", "32"]`                             |  10.625 ms (5%) |         |  192 bytes (1%) |           4 |
| `["gemm", "fusedmul", "xf", "8"]`                              |   2.649 ms (5%) |         |  192 bytes (1%) |           4 |
| `["gemm", "mul", "linalg", "256"]`                             | 452.506 μs (5%) |         |                 |             |
| `["gemm", "mul", "linalg", "32"]`                              |   1.600 μs (5%) |         |                 |             |
| `["gemm", "mul", "linalg", "8"]`                               | 200.000 ns (5%) |         |                 |             |
| `["gemm", "mul", "man", "false", "256"]`                       |   2.862 ms (5%) |         |                 |             |
| `["gemm", "mul", "man", "false", "32"]`                        |   6.800 μs (5%) |         |                 |             |
| `["gemm", "mul", "man", "false", "8"]`                         | 300.000 ns (5%) |         |                 |             |
| `["gemm", "mul", "man", "ivdep", "256"]`                       |   2.833 ms (5%) |         |                 |             |
| `["gemm", "mul", "man", "ivdep", "32"]`                        |   5.000 μs (5%) |         |                 |             |
| `["gemm", "mul", "man", "ivdep", "8"]`                         | 300.000 ns (5%) |         |                 |             |
| `["gemm", "mul", "man", "true", "256"]`                        |   2.852 ms (5%) |         |                 |             |
| `["gemm", "mul", "man", "true", "32"]`                         |   5.700 μs (5%) |         |                 |             |
| `["gemm", "mul", "man", "true", "8"]`                          | 300.000 ns (5%) |         |                 |             |
| `["gemm", "mul", "xf", "false", "256"]`                        |   2.877 ms (5%) |         |   80 bytes (1%) |           3 |
| `["gemm", "mul", "xf", "false", "32"]`                         |   6.000 μs (5%) |         |   80 bytes (1%) |           3 |
| `["gemm", "mul", "xf", "false", "8"]`                          | 500.000 ns (5%) |         |   80 bytes (1%) |           3 |
| `["gemm", "mul", "xf", "ivdep", "256"]`                        |   2.829 ms (5%) |         |   80 bytes (1%) |           3 |
| `["gemm", "mul", "xf", "ivdep", "32"]`                         |   5.100 μs (5%) |         |   80 bytes (1%) |           3 |
| `["gemm", "mul", "xf", "ivdep", "8"]`                          | 400.000 ns (5%) |         |   80 bytes (1%) |           3 |
| `["gemm", "mul", "xf", "true", "256"]`                         |   2.851 ms (5%) |         |   80 bytes (1%) |           3 |
| `["gemm", "mul", "xf", "true", "32"]`                          |   5.700 μs (5%) |         |   80 bytes (1%) |           3 |
| `["gemm", "mul", "xf", "true", "8"]`                           | 500.000 ns (5%) |         |   80 bytes (1%) |           3 |
| `["groupby", "sum", "sac"]`                                    |   7.229 ms (5%) |         |  13.12 KiB (1%) |         102 |
| `["groupby", "sum", "xf-with-init"]`                           | 129.901 μs (5%) |         |   1.05 KiB (1%) |           9 |
| `["groupby", "sum", "xf-without-init"]`                        | 125.301 μs (5%) |         |   1.05 KiB (1%) |           9 |
| `["mapcat_eduction", "base"]`                                  |  42.801 μs (5%) |         |                 |             |
| `["mapcat_eduction", "xf-eduction"]`                           |   1.490 μs (5%) |         |                 |             |
| `["mapcat_eduction", "xf-xf"]`                                 |   1.490 μs (5%) |         |                 |             |
| `["missing_argmax", "man"]`                                    |   2.378 μs (5%) |         |                 |             |
| `["missing_argmax", "rf"]`                                     |   1.480 μs (5%) |         |                 |             |
| `["missing_argmax", "xf"]`                                     |   1.430 μs (5%) |         |   32 bytes (1%) |           1 |
| `["missing_dot", "equiv"]`                                     |   2.120 μs (5%) |         |   16 bytes (1%) |           1 |
| `["missing_dot", "man"]`                                       |   1.260 μs (5%) |         |   16 bytes (1%) |           1 |
| `["missing_dot", "naive"]`                                     |   2.544 μs (5%) |         |   16 bytes (1%) |           1 |
| `["missing_dot", "rf"]`                                        |   1.290 μs (5%) |         |   16 bytes (1%) |           1 |
| `["missing_dot", "rf_nota"]`                                   |   2.820 μs (5%) |         |   16 bytes (1%) |           1 |
| `["missing_dot", "xf"]`                                        |  86.701 μs (5%) |         |  72.12 KiB (1%) |        3740 |
| `["missing_dot", "xf_nota"]`                                   |  87.001 μs (5%) |         |  72.05 KiB (1%) |        3739 |
| `["overhead", "foldl"]`                                        |   2.900 ns (5%) |         |                 |             |
| `["overhead", "reduce_basecase"]`                              |  84.425 ns (5%) |         |   16 bytes (1%) |           1 |
| `["partition_by", "man"]`                                      |   2.200 ms (5%) |         |  480 bytes (1%) |           3 |
| `["partition_by", "xf"]`                                       |   2.399 ms (5%) |         |  592 bytes (1%) |           5 |
| `["set", "base"]`                                              |   3.760 ms (5%) |         |  49.14 KiB (1%) |          17 |
| `["set", "xf"]`                                                |   3.719 ms (5%) |         |  49.17 KiB (1%) |          19 |
| `["sum_transpose", "30", "noinit", "iter"]`                    |   2.111 μs (5%) |         |                 |             |
| `["sum_transpose", "30", "noinit", "man"]`                     |   2.500 μs (5%) |         |                 |             |
| `["sum_transpose", "30", "noinit", "xf"]`                      |   1.080 μs (5%) |         |   32 bytes (1%) |           2 |
| `["sum_transpose", "30", "withinit", "iter"]`                  |   1.580 μs (5%) |         |                 |             |
| `["sum_transpose", "30", "withinit", "man"]`                   |   1.010 μs (5%) |         |                 |             |
| `["sum_transpose", "30", "withinit", "xf"]`                    |   1.080 μs (5%) |         |   48 bytes (1%) |           3 |
| `["teerf_filter", "noinit"]`                                   | 332.425 ns (5%) |         |   80 bytes (1%) |           3 |
| `["teerf_filter", "withinit"]`                                 | 183.567 ns (5%) |         |                 |             |

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
Julia Version 1.7.2
Commit bf53498635 (2022-02-06 15:21 UTC)
Platform Info:
  OS: Linux (x86_64-pc-linux-gnu)
      Ubuntu 20.04.3 LTS
  uname: Linux 5.11.0-1028-azure #31~20.04.2-Ubuntu SMP Tue Jan 18 08:46:15 UTC 2022 x86_64 x86_64
  CPU: Intel(R) Xeon(R) Platinum 8272CL CPU @ 2.60GHz: 
              speed         user         nice          sys         idle          irq
       #1  2593 MHz       9240 s          2 s        168 s        804 s          0 s
       #2  2593 MHz        730 s          0 s        121 s       9358 s          0 s
       
  Memory: 6.7845458984375 GB (3723.83984375 MB free)
  Uptime: 1026.71 sec
  Load Avg:  1.21  1.1  0.77
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
    Byte Order:                      Little Endian
    Address sizes:                   46 bits physical, 48 bits virtual
    CPU(s):                          2
    On-line CPU(s) list:             0,1
    Thread(s) per core:              1
    Core(s) per socket:              2
    Socket(s):                       1
    NUMA node(s):                    1
    Vendor ID:                       GenuineIntel
    CPU family:                      6
    Model:                           85
    Model name:                      Intel(R) Xeon(R) Platinum 8272CL CPU @ 2.60GHz
    Stepping:                        7
    CPU MHz:                         2593.905
    BogoMIPS:                        5187.81
    Hypervisor vendor:               Microsoft
    Virtualization type:             full
    L1d cache:                       64 KiB
    L1i cache:                       64 KiB
    L2 cache:                        2 MiB
    L3 cache:                        35.8 MiB
    NUMA node0 CPU(s):               0,1
    Vulnerability Itlb multihit:     KVM: Mitigation: VMX unsupported
    Vulnerability L1tf:              Mitigation; PTE Inversion
    Vulnerability Mds:               Mitigation; Clear CPU buffers; SMT Host state unknown
    Vulnerability Meltdown:          Mitigation; PTI
    Vulnerability Spec store bypass: Vulnerable
    Vulnerability Spectre v1:        Mitigation; usercopy/swapgs barriers and __user pointer sanitization
    Vulnerability Spectre v2:        Mitigation; Full generic retpoline, STIBP disabled, RSB filling
    Vulnerability Srbds:             Not affected
    Vulnerability Tsx async abort:   Mitigation; Clear CPU buffers; SMT Host state unknown
    Flags:                           fpu vme de pse tsc msr pae mce cx8 apic sep mtrr pge mca cmov pat pse36 clflush mmx fxsr sse sse2 ss ht syscall nx pdpe1gb rdtscp lm constant_tsc rep_good nopl xtopology cpuid pni pclmulqdq ssse3 fma cx16 pcid sse4_1 sse4_2 movbe popcnt aes xsave avx f16c rdrand hypervisor lahf_lm abm 3dnowprefetch invpcid_single pti fsgsbase bmi1 hle avx2 smep bmi2 erms invpcid rtm mpx avx512f avx512dq rdseed adx smap clflushopt avx512cd avx512bw avx512vl xsaveopt xsavec xsaves md_clear
    

| Cpu Property       | Value                                                   |
|:------------------ |:------------------------------------------------------- |
| Brand              | Intel(R) Xeon(R) Platinum 8272CL CPU @ 2.60GHz          |
| Vendor             | :Intel                                                  |
| Architecture       | :Skylake                                                |
| Model              | Family: 0x06, Model: 0x55, Stepping: 0x07, Type: 0x00   |
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

