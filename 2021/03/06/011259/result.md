# Benchmark result

* Pull request commit: [`4e8d029b7d3013747ea27e1fb2bf1cdcab449d26`](https://github.com/JuliaFolds/Transducers.jl/commit/4e8d029b7d3013747ea27e1fb2bf1cdcab449d26)
* Pull request: <https://github.com/JuliaFolds/Transducers.jl/pull/243> (Update */Manifest.toml)

# Judge result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmarks:
    - Target: 6 Mar 2021 - 01:06
    - Baseline: 6 Mar 2021 - 01:12
* Package commits:
    - Target: 44319b
    - Baseline: 2e58c7
* Julia commits:
    - Target: 788b2c
    - Baseline: 788b2c
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

| ID                                                             | time ratio                   | memory ratio  |
|----------------------------------------------------------------|------------------------------|---------------|
| `["append!!", "eduction"]`                                     |                1.07 (5%) :x: |    1.00 (1%)  |
| `["append!!", "xf"]`                                           |                1.18 (5%) :x: |    1.00 (1%)  |
| `["cartesian", "copyto!", "man"]`                              |                1.05 (5%) :x: |    1.00 (1%)  |
| `["cartesian", "copyto!", "xf"]`                               | 0.91 (5%) :white_check_mark: |    1.00 (1%)  |
| `["cat", "xf"]`                                                |                1.10 (5%) :x: |    1.00 (1%)  |
| `["collect", "identity-float"]`                                |                1.08 (5%) :x: |    1.00 (1%)  |
| `["filter_sum", "1000", "RandomFloats", "noinit", "base"]`     | 0.92 (5%) :white_check_mark: |    1.00 (1%)  |
| `["filter_sum", "1000", "RandomFloats", "noinit", "xf"]`       |                1.09 (5%) :x: |    1.00 (1%)  |
| `["filter_sum", "1000", "RandomFloats", "withinit", "base"]`   | 0.94 (5%) :white_check_mark: |    1.00 (1%)  |
| `["filter_sum", "1000", "RandomFloats", "withinit", "naive"]`  | 0.92 (5%) :white_check_mark: |    1.00 (1%)  |
| `["filter_sum", "1000", "UnitRange", "noinit", "base"]`        |                1.25 (5%) :x: |    1.00 (1%)  |
| `["filter_sum", "1000", "UnitRange", "withinit", "naive"]`     |                1.06 (5%) :x: |    1.00 (1%)  |
| `["filter_sum", "10000", "RandomFloats", "noinit", "base"]`    |                1.06 (5%) :x: |    1.00 (1%)  |
| `["filter_sum", "10000", "RandomFloats", "noinit", "naive"]`   |                1.10 (5%) :x: |    1.00 (1%)  |
| `["filter_sum", "10000", "RandomFloats", "withinit", "base"]`  |                1.06 (5%) :x: |    1.00 (1%)  |
| `["filter_sum", "10000", "UnitRange", "noinit", "naive"]`      |                1.06 (5%) :x: |    1.00 (1%)  |
| `["filter_sum", "10000", "UnitRange", "noinit", "xf"]`         |                1.06 (5%) :x: |    1.00 (1%)  |
| `["findall", "base"]`                                          |                1.10 (5%) :x: |    1.00 (1%)  |
| `["findall", "xf-array"]`                                      |                1.09 (5%) :x: |    1.00 (1%)  |
| `["gemm", "fusedmul", "blas", "32"]`                           |                1.06 (5%) :x: |    1.00 (1%)  |
| `["gemm", "fusedmul", "xf", "8"]`                              |                1.07 (5%) :x: |    1.00 (1%)  |
| `["gemm", "mul", "linalg", "256"]`                             |                1.05 (5%) :x: |    1.00 (1%)  |
| `["gemm", "mul", "linalg", "32"]`                              | 0.94 (5%) :white_check_mark: |    1.00 (1%)  |
| `["gemm", "mul", "man", "false", "8"]`                         | 0.83 (5%) :white_check_mark: |    1.00 (1%)  |
| `["gemm", "mul", "man", "ivdep", "32"]`                        | 0.93 (5%) :white_check_mark: |    1.00 (1%)  |
| `["gemm", "mul", "man", "ivdep", "8"]`                         |                1.30 (5%) :x: |    1.00 (1%)  |
| `["gemm", "mul", "man", "true", "32"]`                         | 0.93 (5%) :white_check_mark: |    1.00 (1%)  |
| `["gemm", "mul", "man", "true", "8"]`                          | 0.82 (5%) :white_check_mark: |    1.00 (1%)  |
| `["gemm", "mul", "xf", "false", "32"]`                         | 0.92 (5%) :white_check_mark: |    1.00 (1%)  |
| `["gemm", "mul", "xf", "false", "8"]`                          |                1.15 (5%) :x: |    1.00 (1%)  |
| `["gemm", "mul", "xf", "ivdep", "256"]`                        |                1.05 (5%) :x: |    1.00 (1%)  |
| `["gemm", "mul", "xf", "ivdep", "32"]`                         | 0.86 (5%) :white_check_mark: |    1.00 (1%)  |
| `["gemm", "mul", "xf", "ivdep", "8"]`                          |                1.15 (5%) :x: |    1.00 (1%)  |
| `["gemm", "mul", "xf", "true", "8"]`                           |                1.21 (5%) :x: |    1.00 (1%)  |
| `["groupby", "sum", "sac"]`                                    |                   0.98 (5%)  | 2.10 (1%) :x: |
| `["mapcat_eduction", "base"]`                                  |                1.17 (5%) :x: |    1.00 (1%)  |
| `["mapcat_eduction", "xf-eduction"]`                           |                1.07 (5%) :x: |    1.00 (1%)  |
| `["mapcat_eduction", "xf-xf"]`                                 |                1.10 (5%) :x: |    1.00 (1%)  |
| `["missing_argmax", "xf"]`                                     |                1.14 (5%) :x: |    1.00 (1%)  |
| `["missing_dot", "equiv"]`                                     |                1.19 (5%) :x: |    1.00 (1%)  |
| `["missing_dot", "man"]`                                       |                1.10 (5%) :x: |    1.00 (1%)  |
| `["missing_dot", "rf"]`                                        |                1.14 (5%) :x: |    1.00 (1%)  |
| `["missing_dot", "rf_nota"]`                                   |                1.11 (5%) :x: |    1.00 (1%)  |
| `["missing_dot", "xf"]`                                        |                1.16 (5%) :x: |    1.00 (1%)  |
| `["overhead", "foldl"]`                                        |                1.13 (5%) :x: |    1.00 (1%)  |
| `["sum_transpose", "30", "noinit", "xf"]`                      |                1.12 (5%) :x: |    1.00 (1%)  |

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
Julia Version 1.5.3
Commit 788b2c77c1 (2020-11-09 13:37 UTC)
Platform Info:
  OS: Linux (x86_64-pc-linux-gnu)
      Ubuntu 20.04.2 LTS
  uname: Linux 5.4.0-1040-azure #42-Ubuntu SMP Fri Feb 5 15:39:06 UTC 2021 x86_64 x86_64
  CPU: Intel(R) Xeon(R) CPU E5-2673 v4 @ 2.30GHz: 
              speed         user         nice          sys         idle          irq
       #1  2294 MHz      17728 s         15 s       1456 s      67047 s          0 s
       #2  2294 MHz      65932 s          9 s       1549 s      19174 s          0 s
       
  Memory: 6.7913818359375 GB (3681.14453125 MB free)
  Uptime: 877.0 sec
  Load Avg:  1.0  1.0  0.69970703125
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-9.0.1 (ORCJIT, broadwell)
```

### Baseline
```
Julia Version 1.5.3
Commit 788b2c77c1 (2020-11-09 13:37 UTC)
Platform Info:
  OS: Linux (x86_64-pc-linux-gnu)
      Ubuntu 20.04.2 LTS
  uname: Linux 5.4.0-1040-azure #42-Ubuntu SMP Fri Feb 5 15:39:06 UTC 2021 x86_64 x86_64
  CPU: Intel(R) Xeon(R) CPU E5-2673 v4 @ 2.30GHz: 
              speed         user         nice          sys         idle          irq
       #1  2294 MHz      49366 s         15 s       1641 s      69990 s          0 s
       #2  2294 MHz      68770 s          9 s       1830 s      50736 s          0 s
       
  Memory: 6.7913818359375 GB (3628.8046875 MB free)
  Uptime: 1225.0 sec
  Load Avg:  1.02197265625  1.0263671875  0.826171875
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-9.0.1 (ORCJIT, broadwell)
```

---
# Target result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmark: 6 Mar 2021 - 1:6
* Package commit: 44319b
* Julia commit: 788b2c
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
| `["append!!", "eduction"]`                                     |  18.100 μs (5%) |         |  64.63 KiB (1%) |          13 |
| `["append!!", "xf"]`                                           |  19.200 μs (5%) |         |  64.63 KiB (1%) |          13 |
| `["cartesian", "copyto!", "iter"]`                             |   4.983 μs (5%) |         |                 |             |
| `["cartesian", "copyto!", "man"]`                              |   2.033 μs (5%) |         |                 |             |
| `["cartesian", "copyto!", "xf"]`                               |   2.333 μs (5%) |         |                 |             |
| `["cat", "base"]`                                              |   1.830 μs (5%) |         |                 |             |
| `["cat", "xf"]`                                                |   2.367 μs (5%) |         |                 |             |
| `["collect", "filter-missing"]`                                |  48.700 μs (5%) |         |  32.81 KiB (1%) |          14 |
| `["collect", "identity-float"]`                                |  29.897 μs (5%) |         | 256.66 KiB (1%) |          14 |
| `["collect", "identity-union"]`                                | 137.200 μs (5%) |         | 601.08 KiB (1%) |       10014 |
| `["dict", "base"]`                                             |   4.815 ms (5%) |         |  92.91 KiB (1%) |          22 |
| `["dict", "xf"]`                                               |   4.424 ms (5%) |         |  92.31 KiB (1%) |          18 |
| `["dot", "blas"]`                                              |   2.244 μs (5%) |         |                 |             |
| `["dot", "man"]`                                               |   2.233 μs (5%) |         |                 |             |
| `["dot", "rf"]`                                                |   3.063 μs (5%) |         |                 |             |
| `["dot", "xf"]`                                                |   3.150 μs (5%) |         |   64 bytes (1%) |           3 |
| `["filter_map_map!", "man"]`                                   |  69.100 μs (5%) |         |                 |             |
| `["filter_map_map!", "xf"]`                                    | 542.700 μs (5%) |         |   80 bytes (1%) |           3 |
| `["filter_map_reduce", "man"]`                                 | 195.000 μs (5%) |         |                 |             |
| `["filter_map_reduce", "xf"]`                                  | 200.500 μs (5%) |         |                 |             |
| `["filter_sum", "1000", "RandomFloats", "noinit", "base"]`     | 772.881 ns (5%) |         |                 |             |
| `["filter_sum", "1000", "RandomFloats", "noinit", "naive"]`    |   1.080 μs (5%) |         |                 |             |
| `["filter_sum", "1000", "RandomFloats", "noinit", "xf"]`       |   1.510 μs (5%) |         |                 |             |
| `["filter_sum", "1000", "RandomFloats", "withinit", "base"]`   |   1.510 μs (5%) |         |                 |             |
| `["filter_sum", "1000", "RandomFloats", "withinit", "naive"]`  | 815.116 ns (5%) |         |                 |             |
| `["filter_sum", "1000", "RandomFloats", "withinit", "xf"]`     |   1.460 μs (5%) |         |                 |             |
| `["filter_sum", "1000", "UnitRange", "noinit", "base"]`        |   1.930 μs (5%) |         |                 |             |
| `["filter_sum", "1000", "UnitRange", "noinit", "naive"]`       | 703.546 ns (5%) |         |                 |             |
| `["filter_sum", "1000", "UnitRange", "noinit", "xf"]`          | 160.188 ns (5%) |         |                 |             |
| `["filter_sum", "1000", "UnitRange", "withinit", "base"]`      | 156.852 ns (5%) |         |                 |             |
| `["filter_sum", "1000", "UnitRange", "withinit", "naive"]`     | 549.738 ns (5%) |         |                 |             |
| `["filter_sum", "1000", "UnitRange", "withinit", "xf"]`        | 159.007 ns (5%) |         |                 |             |
| `["filter_sum", "10000", "RandomFloats", "noinit", "base"]`    |  34.400 μs (5%) |         |                 |             |
| `["filter_sum", "10000", "RandomFloats", "noinit", "naive"]`   |  41.000 μs (5%) |         |                 |             |
| `["filter_sum", "10000", "RandomFloats", "noinit", "xf"]`      |  13.900 μs (5%) |         |                 |             |
| `["filter_sum", "10000", "RandomFloats", "withinit", "base"]`  |  14.700 μs (5%) |         |                 |             |
| `["filter_sum", "10000", "RandomFloats", "withinit", "naive"]` |  36.800 μs (5%) |         |                 |             |
| `["filter_sum", "10000", "RandomFloats", "withinit", "xf"]`    |  13.900 μs (5%) |         |                 |             |
| `["filter_sum", "10000", "UnitRange", "noinit", "base"]`       |  15.400 μs (5%) |         |                 |             |
| `["filter_sum", "10000", "UnitRange", "noinit", "naive"]`      |   7.825 μs (5%) |         |                 |             |
| `["filter_sum", "10000", "UnitRange", "noinit", "xf"]`         |   1.700 μs (5%) |         |                 |             |
| `["filter_sum", "10000", "UnitRange", "withinit", "base"]`     |   1.530 μs (5%) |         |                 |             |
| `["filter_sum", "10000", "UnitRange", "withinit", "naive"]`    |   4.767 μs (5%) |         |                 |             |
| `["filter_sum", "10000", "UnitRange", "withinit", "xf"]`       |   1.600 μs (5%) |         |                 |             |
| `["findall", "base"]`                                          | 839.394 μs (5%) |         |   2.00 MiB (1%) |          18 |
| `["findall", "xf-array"]`                                      | 769.398 μs (5%) |         |   3.02 MiB (1%) |       98829 |
| `["findall", "xf-iter"]`                                       | 305.800 μs (5%) |         |   2.00 MiB (1%) |          19 |
| `["gemm", "fusedmul", "blas", "16"]`                           |   5.060 ms (5%) |         |                 |             |
| `["gemm", "fusedmul", "blas", "2"]`                            |   3.699 ms (5%) |         |                 |             |
| `["gemm", "fusedmul", "blas", "32"]`                           |   7.069 ms (5%) |         |                 |             |
| `["gemm", "fusedmul", "blas", "8"]`                            |   3.854 ms (5%) |         |                 |             |
| `["gemm", "fusedmul", "xf", "16"]`                             |   5.245 ms (5%) |         |  192 bytes (1%) |           4 |
| `["gemm", "fusedmul", "xf", "2"]`                              | 603.800 μs (5%) |         |  192 bytes (1%) |           4 |
| `["gemm", "fusedmul", "xf", "32"]`                             |  10.404 ms (5%) |         |  192 bytes (1%) |           4 |
| `["gemm", "fusedmul", "xf", "8"]`                              |   2.645 ms (5%) |         |  192 bytes (1%) |           4 |
| `["gemm", "mul", "linalg", "256"]`                             |   1.016 ms (5%) |         |                 |             |
| `["gemm", "mul", "linalg", "32"]`                              |   3.575 μs (5%) |         |                 |             |
| `["gemm", "mul", "linalg", "8"]`                               | 285.714 ns (5%) |         |                 |             |
| `["gemm", "mul", "man", "false", "256"]`                       |   4.632 ms (5%) |         |                 |             |
| `["gemm", "mul", "man", "false", "32"]`                        |   7.400 μs (5%) |         |                 |             |
| `["gemm", "mul", "man", "false", "8"]`                         | 416.751 ns (5%) |         |                 |             |
| `["gemm", "mul", "man", "ivdep", "256"]`                       |   4.422 ms (5%) |         |                 |             |
| `["gemm", "mul", "man", "ivdep", "32"]`                        |   5.500 μs (5%) |         |                 |             |
| `["gemm", "mul", "man", "ivdep", "8"]`                         | 390.452 ns (5%) |         |                 |             |
| `["gemm", "mul", "man", "true", "256"]`                        |   4.373 ms (5%) |         |                 |             |
| `["gemm", "mul", "man", "true", "32"]`                         |   6.850 μs (5%) |         |                 |             |
| `["gemm", "mul", "man", "true", "8"]`                          | 326.339 ns (5%) |         |                 |             |
| `["gemm", "mul", "xf", "false", "256"]`                        |   4.700 ms (5%) |         |   80 bytes (1%) |           3 |
| `["gemm", "mul", "xf", "false", "32"]`                         |   7.475 μs (5%) |         |   80 bytes (1%) |           3 |
| `["gemm", "mul", "xf", "false", "8"]`                          | 459.278 ns (5%) |         |   80 bytes (1%) |           3 |
| `["gemm", "mul", "xf", "ivdep", "256"]`                        |   4.711 ms (5%) |         |   80 bytes (1%) |           3 |
| `["gemm", "mul", "xf", "ivdep", "32"]`                         |   5.620 μs (5%) |         |   80 bytes (1%) |           3 |
| `["gemm", "mul", "xf", "ivdep", "8"]`                          | 461.026 ns (5%) |         |   80 bytes (1%) |           3 |
| `["gemm", "mul", "xf", "true", "256"]`                         |   4.633 ms (5%) |         |   80 bytes (1%) |           3 |
| `["gemm", "mul", "xf", "true", "32"]`                          |   8.175 μs (5%) |         |   80 bytes (1%) |           3 |
| `["gemm", "mul", "xf", "true", "8"]`                           | 484.896 ns (5%) |         |   80 bytes (1%) |           3 |
| `["groupby", "sum", "sac"]`                                    | 155.800 μs (5%) |         |   1.28 KiB (1%) |          14 |
| `["groupby", "sum", "xf-with-init"]`                           | 131.400 μs (5%) |         |   1.20 KiB (1%) |           9 |
| `["groupby", "sum", "xf-without-init"]`                        | 132.300 μs (5%) |         |   1.20 KiB (1%) |           9 |
| `["mapcat_eduction", "base"]`                                  |   1.720 μs (5%) |         |                 |             |
| `["mapcat_eduction", "xf-eduction"]`                           |   2.060 μs (5%) |         |                 |             |
| `["mapcat_eduction", "xf-xf"]`                                 |   2.000 μs (5%) |         |                 |             |
| `["missing_argmax", "man"]`                                    | 980.000 ns (5%) |         |   32 bytes (1%) |           1 |
| `["missing_argmax", "rf"]`                                     |   1.270 μs (5%) |         |   32 bytes (1%) |           1 |
| `["missing_argmax", "xf"]`                                     |   1.350 μs (5%) |         |   32 bytes (1%) |           1 |
| `["missing_dot", "equiv"]`                                     |   1.270 μs (5%) |         |   16 bytes (1%) |           1 |
| `["missing_dot", "man"]`                                       |   1.152 μs (5%) |         |   16 bytes (1%) |           1 |
| `["missing_dot", "naive"]`                                     |   4.200 μs (5%) |         |   16 bytes (1%) |           1 |
| `["missing_dot", "rf"]`                                        |   1.300 μs (5%) |         |   16 bytes (1%) |           1 |
| `["missing_dot", "rf_nota"]`                                   |   1.076 μs (5%) |         |   16 bytes (1%) |           1 |
| `["missing_dot", "xf"]`                                        | 107.301 μs (5%) |         |  72.22 KiB (1%) |        3744 |
| `["missing_dot", "xf_nota"]`                                   |  98.300 μs (5%) |         |  72.23 KiB (1%) |        3746 |
| `["overhead", "foldl"]`                                        |   4.400 ns (5%) |         |                 |             |
| `["overhead", "reduce_basecase"]`                              | 133.218 ns (5%) |         |   48 bytes (1%) |           2 |
| `["partition_by", "man"]`                                      |   1.762 ms (5%) |         |  352 bytes (1%) |           4 |
| `["partition_by", "xf"]`                                       |   1.770 ms (5%) |         |  544 bytes (1%) |           6 |
| `["set", "base"]`                                              |   4.982 ms (5%) |         |  49.56 KiB (1%) |          17 |
| `["set", "xf"]`                                                |   4.860 ms (5%) |         |  49.59 KiB (1%) |          19 |
| `["sum_transpose", "30", "noinit", "iter"]`                    |   1.870 μs (5%) |         |                 |             |
| `["sum_transpose", "30", "noinit", "man"]`                     |   1.340 μs (5%) |         |                 |             |
| `["sum_transpose", "30", "noinit", "xf"]`                      | 922.490 ns (5%) |         |   32 bytes (1%) |           2 |
| `["sum_transpose", "30", "withinit", "iter"]`                  |   1.270 μs (5%) |         |                 |             |
| `["sum_transpose", "30", "withinit", "man"]`                   | 727.835 ns (5%) |         |                 |             |
| `["sum_transpose", "30", "withinit", "xf"]`                    | 779.526 ns (5%) |         |   48 bytes (1%) |           3 |
| `["teerf_filter", "noinit"]`                                   |   2.020 μs (5%) |         |  192 bytes (1%) |           8 |
| `["teerf_filter", "withinit"]`                                 | 229.148 ns (5%) |         |                 |             |

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
Julia Version 1.5.3
Commit 788b2c77c1 (2020-11-09 13:37 UTC)
Platform Info:
  OS: Linux (x86_64-pc-linux-gnu)
      Ubuntu 20.04.2 LTS
  uname: Linux 5.4.0-1040-azure #42-Ubuntu SMP Fri Feb 5 15:39:06 UTC 2021 x86_64 x86_64
  CPU: Intel(R) Xeon(R) CPU E5-2673 v4 @ 2.30GHz: 
              speed         user         nice          sys         idle          irq
       #1  2294 MHz      17728 s         15 s       1456 s      67047 s          0 s
       #2  2294 MHz      65932 s          9 s       1549 s      19174 s          0 s
       
  Memory: 6.7913818359375 GB (3681.14453125 MB free)
  Uptime: 877.0 sec
  Load Avg:  1.0  1.0  0.69970703125
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-9.0.1 (ORCJIT, broadwell)
```

---
# Baseline result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmark: 6 Mar 2021 - 1:12
* Package commit: 2e58c7
* Julia commit: 788b2c
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
| `["append!!", "eduction"]`                                     |  16.900 μs (5%) |         |  64.63 KiB (1%) |          13 |
| `["append!!", "xf"]`                                           |  16.300 μs (5%) |         |  64.63 KiB (1%) |          13 |
| `["cartesian", "copyto!", "iter"]`                             |   4.966 μs (5%) |         |                 |             |
| `["cartesian", "copyto!", "man"]`                              |   1.933 μs (5%) |         |                 |             |
| `["cartesian", "copyto!", "xf"]`                               |   2.567 μs (5%) |         |                 |             |
| `["cat", "base"]`                                              |   1.780 μs (5%) |         |                 |             |
| `["cat", "xf"]`                                                |   2.156 μs (5%) |         |                 |             |
| `["collect", "filter-missing"]`                                |  48.800 μs (5%) |         |  32.81 KiB (1%) |          14 |
| `["collect", "identity-float"]`                                |  27.700 μs (5%) |         | 256.66 KiB (1%) |          14 |
| `["collect", "identity-union"]`                                | 134.100 μs (5%) |         | 601.07 KiB (1%) |       10014 |
| `["dict", "base"]`                                             |   4.685 ms (5%) |         |  92.91 KiB (1%) |          22 |
| `["dict", "xf"]`                                               |   4.548 ms (5%) |         |  92.31 KiB (1%) |          18 |
| `["dot", "blas"]`                                              |   2.244 μs (5%) |         |                 |             |
| `["dot", "man"]`                                               |   2.233 μs (5%) |         |                 |             |
| `["dot", "rf"]`                                                |   3.050 μs (5%) |         |                 |             |
| `["dot", "xf"]`                                                |   3.150 μs (5%) |         |   64 bytes (1%) |           3 |
| `["filter_map_map!", "man"]`                                   |  67.800 μs (5%) |         |                 |             |
| `["filter_map_map!", "xf"]`                                    | 538.501 μs (5%) |         |   80 bytes (1%) |           3 |
| `["filter_map_reduce", "man"]`                                 | 194.900 μs (5%) |         |                 |             |
| `["filter_map_reduce", "xf"]`                                  | 195.000 μs (5%) |         |                 |             |
| `["filter_sum", "1000", "RandomFloats", "noinit", "base"]`     | 839.831 ns (5%) |         |                 |             |
| `["filter_sum", "1000", "RandomFloats", "noinit", "naive"]`    |   1.110 μs (5%) |         |                 |             |
| `["filter_sum", "1000", "RandomFloats", "noinit", "xf"]`       |   1.380 μs (5%) |         |                 |             |
| `["filter_sum", "1000", "RandomFloats", "withinit", "base"]`   |   1.610 μs (5%) |         |                 |             |
| `["filter_sum", "1000", "RandomFloats", "withinit", "naive"]`  | 887.209 ns (5%) |         |                 |             |
| `["filter_sum", "1000", "RandomFloats", "withinit", "xf"]`     |   1.460 μs (5%) |         |                 |             |
| `["filter_sum", "1000", "UnitRange", "noinit", "base"]`        |   1.550 μs (5%) |         |                 |             |
| `["filter_sum", "1000", "UnitRange", "noinit", "naive"]`       | 709.220 ns (5%) |         |                 |             |
| `["filter_sum", "1000", "UnitRange", "noinit", "xf"]`          | 163.941 ns (5%) |         |                 |             |
| `["filter_sum", "1000", "UnitRange", "withinit", "base"]`      | 160.923 ns (5%) |         |                 |             |
| `["filter_sum", "1000", "UnitRange", "withinit", "naive"]`     | 519.372 ns (5%) |         |                 |             |
| `["filter_sum", "1000", "UnitRange", "withinit", "xf"]`        | 159.007 ns (5%) |         |                 |             |
| `["filter_sum", "10000", "RandomFloats", "noinit", "base"]`    |  32.600 μs (5%) |         |                 |             |
| `["filter_sum", "10000", "RandomFloats", "noinit", "naive"]`   |  37.200 μs (5%) |         |                 |             |
| `["filter_sum", "10000", "RandomFloats", "noinit", "xf"]`      |  13.900 μs (5%) |         |                 |             |
| `["filter_sum", "10000", "RandomFloats", "withinit", "base"]`  |  13.900 μs (5%) |         |                 |             |
| `["filter_sum", "10000", "RandomFloats", "withinit", "naive"]` |  36.600 μs (5%) |         |                 |             |
| `["filter_sum", "10000", "RandomFloats", "withinit", "xf"]`    |  13.900 μs (5%) |         |                 |             |
| `["filter_sum", "10000", "UnitRange", "noinit", "base"]`       |  15.400 μs (5%) |         |                 |             |
| `["filter_sum", "10000", "UnitRange", "noinit", "naive"]`      |   7.375 μs (5%) |         |                 |             |
| `["filter_sum", "10000", "UnitRange", "noinit", "xf"]`         |   1.600 μs (5%) |         |                 |             |
| `["filter_sum", "10000", "UnitRange", "withinit", "base"]`     |   1.530 μs (5%) |         |                 |             |
| `["filter_sum", "10000", "UnitRange", "withinit", "naive"]`    |   4.883 μs (5%) |         |                 |             |
| `["filter_sum", "10000", "UnitRange", "withinit", "xf"]`       |   1.600 μs (5%) |         |                 |             |
| `["findall", "base"]`                                          | 762.700 μs (5%) |         |   2.00 MiB (1%) |          18 |
| `["findall", "xf-array"]`                                      | 706.501 μs (5%) |         |   3.02 MiB (1%) |       98829 |
| `["findall", "xf-iter"]`                                       | 299.700 μs (5%) |         |   2.00 MiB (1%) |          19 |
| `["gemm", "fusedmul", "blas", "16"]`                           |   4.985 ms (5%) |         |                 |             |
| `["gemm", "fusedmul", "blas", "2"]`                            |   3.791 ms (5%) |         |                 |             |
| `["gemm", "fusedmul", "blas", "32"]`                           |   6.662 ms (5%) |         |                 |             |
| `["gemm", "fusedmul", "blas", "8"]`                            |   3.756 ms (5%) |         |                 |             |
| `["gemm", "fusedmul", "xf", "16"]`                             |   5.106 ms (5%) |         |  192 bytes (1%) |           4 |
| `["gemm", "fusedmul", "xf", "2"]`                              | 598.401 μs (5%) |         |  192 bytes (1%) |           4 |
| `["gemm", "fusedmul", "xf", "32"]`                             |  10.447 ms (5%) |         |  192 bytes (1%) |           4 |
| `["gemm", "fusedmul", "xf", "8"]`                              |   2.472 ms (5%) |         |  192 bytes (1%) |           4 |
| `["gemm", "mul", "linalg", "256"]`                             | 963.400 μs (5%) |         |                 |             |
| `["gemm", "mul", "linalg", "32"]`                              |   3.800 μs (5%) |         |                 |             |
| `["gemm", "mul", "linalg", "8"]`                               | 300.000 ns (5%) |         |                 |             |
| `["gemm", "mul", "man", "false", "256"]`                       |   4.453 ms (5%) |         |                 |             |
| `["gemm", "mul", "man", "false", "32"]`                        |   7.400 μs (5%) |         |                 |             |
| `["gemm", "mul", "man", "false", "8"]`                         | 500.000 ns (5%) |         |                 |             |
| `["gemm", "mul", "man", "ivdep", "256"]`                       |   4.479 ms (5%) |         |                 |             |
| `["gemm", "mul", "man", "ivdep", "32"]`                        |   5.900 μs (5%) |         |                 |             |
| `["gemm", "mul", "man", "ivdep", "8"]`                         | 300.000 ns (5%) |         |                 |             |
| `["gemm", "mul", "man", "true", "256"]`                        |   4.399 ms (5%) |         |                 |             |
| `["gemm", "mul", "man", "true", "32"]`                         |   7.400 μs (5%) |         |                 |             |
| `["gemm", "mul", "man", "true", "8"]`                          | 400.000 ns (5%) |         |                 |             |
| `["gemm", "mul", "xf", "false", "256"]`                        |   4.713 ms (5%) |         |   80 bytes (1%) |           3 |
| `["gemm", "mul", "xf", "false", "32"]`                         |   8.100 μs (5%) |         |   80 bytes (1%) |           3 |
| `["gemm", "mul", "xf", "false", "8"]`                          | 400.000 ns (5%) |         |   80 bytes (1%) |           3 |
| `["gemm", "mul", "xf", "ivdep", "256"]`                        |   4.478 ms (5%) |         |   80 bytes (1%) |           3 |
| `["gemm", "mul", "xf", "ivdep", "32"]`                         |   6.500 μs (5%) |         |   80 bytes (1%) |           3 |
| `["gemm", "mul", "xf", "ivdep", "8"]`                          | 400.000 ns (5%) |         |   80 bytes (1%) |           3 |
| `["gemm", "mul", "xf", "true", "256"]`                         |   4.492 ms (5%) |         |   80 bytes (1%) |           3 |
| `["gemm", "mul", "xf", "true", "32"]`                          |   8.200 μs (5%) |         |   80 bytes (1%) |           3 |
| `["gemm", "mul", "xf", "true", "8"]`                           | 400.000 ns (5%) |         |   80 bytes (1%) |           3 |
| `["groupby", "sum", "sac"]`                                    | 159.600 μs (5%) |         |  624 bytes (1%) |           5 |
| `["groupby", "sum", "xf-with-init"]`                           | 130.300 μs (5%) |         |   1.20 KiB (1%) |           9 |
| `["groupby", "sum", "xf-without-init"]`                        | 131.900 μs (5%) |         |   1.20 KiB (1%) |           9 |
| `["mapcat_eduction", "base"]`                                  |   1.470 μs (5%) |         |                 |             |
| `["mapcat_eduction", "xf-eduction"]`                           |   1.930 μs (5%) |         |                 |             |
| `["mapcat_eduction", "xf-xf"]`                                 |   1.822 μs (5%) |         |                 |             |
| `["missing_argmax", "man"]`                                    | 980.000 ns (5%) |         |   32 bytes (1%) |           1 |
| `["missing_argmax", "rf"]`                                     |   1.250 μs (5%) |         |   32 bytes (1%) |           1 |
| `["missing_argmax", "xf"]`                                     |   1.180 μs (5%) |         |   32 bytes (1%) |           1 |
| `["missing_dot", "equiv"]`                                     |   1.070 μs (5%) |         |   16 bytes (1%) |           1 |
| `["missing_dot", "man"]`                                       |   1.048 μs (5%) |         |   16 bytes (1%) |           1 |
| `["missing_dot", "naive"]`                                     |   4.071 μs (5%) |         |   16 bytes (1%) |           1 |
| `["missing_dot", "rf"]`                                        |   1.140 μs (5%) |         |   16 bytes (1%) |           1 |
| `["missing_dot", "rf_nota"]`                                   | 968.966 ns (5%) |         |   16 bytes (1%) |           1 |
| `["missing_dot", "xf"]`                                        |  92.600 μs (5%) |         |  72.06 KiB (1%) |        3738 |
| `["missing_dot", "xf_nota"]`                                   |  95.000 μs (5%) |         |  72.03 KiB (1%) |        3738 |
| `["overhead", "foldl"]`                                        |   3.900 ns (5%) |         |                 |             |
| `["overhead", "reduce_basecase"]`                              | 127.894 ns (5%) |         |   48 bytes (1%) |           2 |
| `["partition_by", "man"]`                                      |   1.821 ms (5%) |         |  352 bytes (1%) |           4 |
| `["partition_by", "xf"]`                                       |   1.855 ms (5%) |         |  544 bytes (1%) |           6 |
| `["set", "base"]`                                              |   5.055 ms (5%) |         |  49.56 KiB (1%) |          17 |
| `["set", "xf"]`                                                |   4.885 ms (5%) |         |  49.59 KiB (1%) |          19 |
| `["sum_transpose", "30", "noinit", "iter"]`                    |   1.870 μs (5%) |         |                 |             |
| `["sum_transpose", "30", "noinit", "man"]`                     |   1.340 μs (5%) |         |                 |             |
| `["sum_transpose", "30", "noinit", "xf"]`                      | 820.408 ns (5%) |         |   32 bytes (1%) |           2 |
| `["sum_transpose", "30", "withinit", "iter"]`                  |   1.280 μs (5%) |         |                 |             |
| `["sum_transpose", "30", "withinit", "man"]`                   | 727.835 ns (5%) |         |                 |             |
| `["sum_transpose", "30", "withinit", "xf"]`                    | 778.205 ns (5%) |         |   48 bytes (1%) |           3 |
| `["teerf_filter", "noinit"]`                                   |   1.930 μs (5%) |         |  192 bytes (1%) |           8 |
| `["teerf_filter", "withinit"]`                                 | 230.867 ns (5%) |         |                 |             |

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
Julia Version 1.5.3
Commit 788b2c77c1 (2020-11-09 13:37 UTC)
Platform Info:
  OS: Linux (x86_64-pc-linux-gnu)
      Ubuntu 20.04.2 LTS
  uname: Linux 5.4.0-1040-azure #42-Ubuntu SMP Fri Feb 5 15:39:06 UTC 2021 x86_64 x86_64
  CPU: Intel(R) Xeon(R) CPU E5-2673 v4 @ 2.30GHz: 
              speed         user         nice          sys         idle          irq
       #1  2294 MHz      49366 s         15 s       1641 s      69990 s          0 s
       #2  2294 MHz      68770 s          9 s       1830 s      50736 s          0 s
       
  Memory: 6.7913818359375 GB (3628.8046875 MB free)
  Uptime: 1225.0 sec
  Load Avg:  1.02197265625  1.0263671875  0.826171875
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-9.0.1 (ORCJIT, broadwell)
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
    Model:                           79
    Model name:                      Intel(R) Xeon(R) CPU E5-2673 v4 @ 2.30GHz
    Stepping:                        1
    CPU MHz:                         2294.685
    BogoMIPS:                        4589.37
    Hypervisor vendor:               Microsoft
    Virtualization type:             full
    L1d cache:                       64 KiB
    L1i cache:                       64 KiB
    L2 cache:                        512 KiB
    L3 cache:                        50 MiB
    NUMA node0 CPU(s):               0,1
    Vulnerability Itlb multihit:     KVM: Vulnerable
    Vulnerability L1tf:              Mitigation; PTE Inversion
    Vulnerability Mds:               Mitigation; Clear CPU buffers; SMT Host state unknown
    Vulnerability Meltdown:          Mitigation; PTI
    Vulnerability Spec store bypass: Vulnerable
    Vulnerability Spectre v1:        Mitigation; usercopy/swapgs barriers and __user pointer sanitization
    Vulnerability Spectre v2:        Mitigation; Full generic retpoline, STIBP disabled, RSB filling
    Vulnerability Srbds:             Not affected
    Vulnerability Tsx async abort:   Mitigation; Clear CPU buffers; SMT Host state unknown
    Flags:                           fpu vme de pse tsc msr pae mce cx8 apic sep mtrr pge mca cmov pat pse36 clflush mmx fxsr sse sse2 ss ht syscall nx pdpe1gb rdtscp lm constant_tsc rep_good nopl xtopology cpuid pni pclmulqdq ssse3 fma cx16 pcid sse4_1 sse4_2 movbe popcnt aes xsave avx f16c rdrand hypervisor lahf_lm abm 3dnowprefetch invpcid_single pti fsgsbase bmi1 hle avx2 smep bmi2 erms invpcid rtm rdseed adx smap xsaveopt md_clear
    

| Cpu Property       | Value                                                   |
|:------------------ |:------------------------------------------------------- |
| Brand              | Intel(R) Xeon(R) CPU E5-2673 v4 @ 2.30GHz               |
| Vendor             | :Intel                                                  |
| Architecture       | :Broadwell                                              |
| Model              | Family: 0x06, Model: 0x4f, Stepping: 0x01, Type: 0x00   |
| Cores              | 2 physical cores, 2 logical cores (on executing CPU)    |
|                    | No Hyperthreading detected                              |
| Clock Frequencies  | Not supported by CPU                                    |
| Data Cache         | Level 1:3 : (32, 256, 51200) kbytes                     |
|                    | 64 byte cache line size                                 |
| Address Size       | 48 bits virtual, 46 bits physical                       |
| SIMD               | 256 bit = 32 byte max. SIMD vector size                 |
| Time Stamp Counter | TSC is accessible via `rdtsc`                           |
|                    | TSC increased at every clock cycle (non-invariant TSC)  |
| Perf. Monitoring   | Performance Monitoring Counters (PMC) are not supported |
| Hypervisor         | Yes, Microsoft                                          |

