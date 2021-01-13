# Benchmark result

* Pull request commit: [`0ca69729195d5290df07f2c3cb7128b6a06fdb65`](https://github.com/JuliaFolds/Transducers.jl/commit/0ca69729195d5290df07f2c3cb7128b6a06fdb65)
* Pull request: <https://github.com/JuliaFolds/Transducers.jl/pull/243> (Update */Manifest.toml)

# Judge result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmarks:
    - Target: 13 Jan 2021 - 01:41
    - Baseline: 13 Jan 2021 - 01:46
* Package commits:
    - Target: 1ff6f1
    - Baseline: dbdd4d
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
| `["append!!", "eduction"]`                                     |                1.08 (5%) :x: |    1.00 (1%)  |
| `["append!!", "xf"]`                                           |                1.10 (5%) :x: |    1.00 (1%)  |
| `["cartesian", "copyto!", "man"]`                              |                1.10 (5%) :x: |    1.00 (1%)  |
| `["cat", "base"]`                                              | 0.94 (5%) :white_check_mark: |    1.00 (1%)  |
| `["cat", "xf"]`                                                | 0.94 (5%) :white_check_mark: |    1.00 (1%)  |
| `["dict", "base"]`                                             |                1.06 (5%) :x: |    1.00 (1%)  |
| `["dot", "blas"]`                                              | 0.89 (5%) :white_check_mark: |    1.00 (1%)  |
| `["dot", "man"]`                                               | 0.93 (5%) :white_check_mark: |    1.00 (1%)  |
| `["filter_sum", "1000", "RandomFloats", "noinit", "base"]`     |                3.05 (5%) :x: |    1.00 (1%)  |
| `["filter_sum", "1000", "RandomFloats", "noinit", "naive"]`    | 0.72 (5%) :white_check_mark: |    1.00 (1%)  |
| `["filter_sum", "1000", "RandomFloats", "withinit", "base"]`   | 0.95 (5%) :white_check_mark: |    1.00 (1%)  |
| `["filter_sum", "1000", "RandomFloats", "withinit", "xf"]`     | 0.95 (5%) :white_check_mark: |    1.00 (1%)  |
| `["filter_sum", "1000", "UnitRange", "noinit", "base"]`        | 0.95 (5%) :white_check_mark: |    1.00 (1%)  |
| `["filter_sum", "1000", "UnitRange", "withinit", "naive"]`     | 0.88 (5%) :white_check_mark: |    1.00 (1%)  |
| `["filter_sum", "10000", "RandomFloats", "noinit", "base"]`    |                1.37 (5%) :x: |    1.00 (1%)  |
| `["filter_sum", "10000", "RandomFloats", "withinit", "base"]`  | 0.95 (5%) :white_check_mark: |    1.00 (1%)  |
| `["filter_sum", "10000", "UnitRange", "noinit", "base"]`       | 0.94 (5%) :white_check_mark: |    1.00 (1%)  |
| `["filter_sum", "10000", "UnitRange", "noinit", "xf"]`         | 0.94 (5%) :white_check_mark: |    1.00 (1%)  |
| `["filter_sum", "10000", "UnitRange", "withinit", "naive"]`    | 0.81 (5%) :white_check_mark: |    1.00 (1%)  |
| `["findall", "xf-iter"]`                                       | 0.91 (5%) :white_check_mark: |    1.00 (1%)  |
| `["gemm", "fusedmul", "blas", "2"]`                            | 0.95 (5%) :white_check_mark: |    1.00 (1%)  |
| `["gemm", "mul", "linalg", "32"]`                              | 0.88 (5%) :white_check_mark: |    1.00 (1%)  |
| `["gemm", "mul", "linalg", "8"]`                               | 0.93 (5%) :white_check_mark: |    1.00 (1%)  |
| `["gemm", "mul", "man", "false", "8"]`                         | 0.94 (5%) :white_check_mark: |    1.00 (1%)  |
| `["gemm", "mul", "man", "ivdep", "32"]`                        | 0.86 (5%) :white_check_mark: |    1.00 (1%)  |
| `["gemm", "mul", "man", "ivdep", "8"]`                         | 0.89 (5%) :white_check_mark: |    1.00 (1%)  |
| `["gemm", "mul", "man", "true", "8"]`                          |                1.38 (5%) :x: |    1.00 (1%)  |
| `["gemm", "mul", "xf", "false", "8"]`                          |                1.14 (5%) :x: |    1.00 (1%)  |
| `["gemm", "mul", "xf", "true", "8"]`                           |                1.42 (5%) :x: |    1.00 (1%)  |
| `["groupby", "sum", "sac"]`                                    |                   1.04 (5%)  | 2.10 (1%) :x: |
| `["groupby", "sum", "xf-without-init"]`                        |                1.06 (5%) :x: |    1.00 (1%)  |
| `["missing_argmax", "rf"]`                                     | 0.93 (5%) :white_check_mark: |    1.00 (1%)  |
| `["missing_dot", "equiv"]`                                     | 0.94 (5%) :white_check_mark: |    1.00 (1%)  |
| `["missing_dot", "rf_nota"]`                                   | 0.91 (5%) :white_check_mark: |    1.00 (1%)  |
| `["missing_dot", "xf"]`                                        | 0.92 (5%) :white_check_mark: |    1.00 (1%)  |
| `["overhead", "reduce_basecase"]`                              | 0.95 (5%) :white_check_mark: |    1.00 (1%)  |
| `["sum_transpose", "30", "noinit", "man"]`                     | 0.94 (5%) :white_check_mark: |    1.00 (1%)  |
| `["sum_transpose", "30", "withinit", "iter"]`                  |                1.06 (5%) :x: |    1.00 (1%)  |
| `["teerf_filter", "noinit"]`                                   | 0.92 (5%) :white_check_mark: |    1.00 (1%)  |
| `["teerf_filter", "withinit"]`                                 | 0.93 (5%) :white_check_mark: |    1.00 (1%)  |

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
      Ubuntu 18.04.5 LTS
  uname: Linux 5.4.0-1032-azure #33~18.04.1-Ubuntu SMP Tue Nov 17 11:40:52 UTC 2020 x86_64 x86_64
  CPU: Intel(R) Xeon(R) CPU E5-2673 v4 @ 2.30GHz: 
              speed         user         nice          sys         idle          irq
       #1  2294 MHz      58029 s          0 s       1384 s      21164 s          0 s
       #2  2294 MHz      19634 s          0 s       1640 s      59323 s          0 s
       
  Memory: 6.7913970947265625 GB (3653.140625 MB free)
  Uptime: 820.0 sec
  Load Avg:  1.0576171875  1.00146484375  0.6572265625
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
      Ubuntu 18.04.5 LTS
  uname: Linux 5.4.0-1032-azure #33~18.04.1-Ubuntu SMP Tue Nov 17 11:40:52 UTC 2020 x86_64 x86_64
  CPU: Intel(R) Xeon(R) CPU E5-2673 v4 @ 2.30GHz: 
              speed         user         nice          sys         idle          irq
       #1  2294 MHz      87975 s          0 s       1668 s      24063 s          0 s
       #2  2294 MHz      22536 s          0 s       1803 s      89303 s          0 s
       
  Memory: 6.7913970947265625 GB (3634.08984375 MB free)
  Uptime: 1152.0 sec
  Load Avg:  1.1162109375  1.0322265625  0.7880859375
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-9.0.1 (ORCJIT, broadwell)
```

---
# Target result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmark: 13 Jan 2021 - 1:41
* Package commit: 1ff6f1
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
| `["append!!", "eduction"]`                                     |  16.700 μs (5%) |         |  64.63 KiB (1%) |          13 |
| `["append!!", "xf"]`                                           |  16.700 μs (5%) |         |  64.63 KiB (1%) |          13 |
| `["cartesian", "copyto!", "iter"]`                             |   4.943 μs (5%) |         |                 |             |
| `["cartesian", "copyto!", "man"]`                              |   2.040 μs (5%) |         |                 |             |
| `["cartesian", "copyto!", "xf"]`                               |   2.344 μs (5%) |         |                 |             |
| `["cat", "base"]`                                              |   1.570 μs (5%) |         |                 |             |
| `["cat", "xf"]`                                                |   2.033 μs (5%) |         |                 |             |
| `["collect", "filter-missing"]`                                |  47.500 μs (5%) |         |  32.81 KiB (1%) |          14 |
| `["collect", "identity-float"]`                                |  24.500 μs (5%) |         | 256.66 KiB (1%) |          14 |
| `["collect", "identity-union"]`                                | 129.300 μs (5%) |         | 601.05 KiB (1%) |       10013 |
| `["dict", "base"]`                                             |   4.182 ms (5%) |         |  92.91 KiB (1%) |          22 |
| `["dict", "xf"]`                                               |   4.070 ms (5%) |         |  92.31 KiB (1%) |          18 |
| `["dot", "blas"]`                                              |   2.222 μs (5%) |         |                 |             |
| `["dot", "man"]`                                               |   2.078 μs (5%) |         |                 |             |
| `["dot", "rf"]`                                                |   3.050 μs (5%) |         |                 |             |
| `["dot", "xf"]`                                                |   3.150 μs (5%) |         |   64 bytes (1%) |           3 |
| `["filter_map_map!", "man"]`                                   |  68.500 μs (5%) |         |                 |             |
| `["filter_map_map!", "xf"]`                                    | 522.302 μs (5%) |         |   80 bytes (1%) |           3 |
| `["filter_map_reduce", "man"]`                                 | 194.900 μs (5%) |         |                 |             |
| `["filter_map_reduce", "xf"]`                                  | 194.900 μs (5%) |         |                 |             |
| `["filter_sum", "1000", "RandomFloats", "noinit", "base"]`     |   2.744 μs (5%) |         |                 |             |
| `["filter_sum", "1000", "RandomFloats", "noinit", "naive"]`    | 716.031 ns (5%) |         |                 |             |
| `["filter_sum", "1000", "RandomFloats", "noinit", "xf"]`       |   1.380 μs (5%) |         |                 |             |
| `["filter_sum", "1000", "RandomFloats", "withinit", "base"]`   |   1.380 μs (5%) |         |                 |             |
| `["filter_sum", "1000", "RandomFloats", "withinit", "naive"]`  | 852.055 ns (5%) |         |                 |             |
| `["filter_sum", "1000", "RandomFloats", "withinit", "xf"]`     |   1.380 μs (5%) |         |                 |             |
| `["filter_sum", "1000", "UnitRange", "noinit", "base"]`        |   1.550 μs (5%) |         |                 |             |
| `["filter_sum", "1000", "UnitRange", "noinit", "naive"]`       | 702.778 ns (5%) |         |                 |             |
| `["filter_sum", "1000", "UnitRange", "noinit", "xf"]`          | 159.356 ns (5%) |         |                 |             |
| `["filter_sum", "1000", "UnitRange", "withinit", "base"]`      | 163.241 ns (5%) |         |                 |             |
| `["filter_sum", "1000", "UnitRange", "withinit", "naive"]`     | 455.838 ns (5%) |         |                 |             |
| `["filter_sum", "1000", "UnitRange", "withinit", "xf"]`        | 158.586 ns (5%) |         |                 |             |
| `["filter_sum", "10000", "RandomFloats", "noinit", "base"]`    |  40.101 μs (5%) |         |                 |             |
| `["filter_sum", "10000", "RandomFloats", "noinit", "naive"]`   |  37.900 μs (5%) |         |                 |             |
| `["filter_sum", "10000", "RandomFloats", "noinit", "xf"]`      |  13.900 μs (5%) |         |                 |             |
| `["filter_sum", "10000", "RandomFloats", "withinit", "base"]`  |  13.900 μs (5%) |         |                 |             |
| `["filter_sum", "10000", "RandomFloats", "withinit", "naive"]` |  36.500 μs (5%) |         |                 |             |
| `["filter_sum", "10000", "RandomFloats", "withinit", "xf"]`    |  13.900 μs (5%) |         |                 |             |
| `["filter_sum", "10000", "UnitRange", "noinit", "base"]`       |  15.400 μs (5%) |         |                 |             |
| `["filter_sum", "10000", "UnitRange", "noinit", "naive"]`      |   6.960 μs (5%) |         |                 |             |
| `["filter_sum", "10000", "UnitRange", "noinit", "xf"]`         |   1.460 μs (5%) |         |                 |             |
| `["filter_sum", "10000", "UnitRange", "withinit", "base"]`     |   1.410 μs (5%) |         |                 |             |
| `["filter_sum", "10000", "UnitRange", "withinit", "naive"]`    |   4.414 μs (5%) |         |                 |             |
| `["filter_sum", "10000", "UnitRange", "withinit", "xf"]`       |   1.460 μs (5%) |         |                 |             |
| `["findall", "base"]`                                          | 733.903 μs (5%) |         |   2.00 MiB (1%) |          18 |
| `["findall", "xf-array"]`                                      | 650.003 μs (5%) |         |   3.02 MiB (1%) |       98829 |
| `["findall", "xf-iter"]`                                       | 269.401 μs (5%) |         |   2.00 MiB (1%) |          19 |
| `["gemm", "fusedmul", "blas", "16"]`                           |   4.688 ms (5%) |         |                 |             |
| `["gemm", "fusedmul", "blas", "2"]`                            |   3.495 ms (5%) |         |                 |             |
| `["gemm", "fusedmul", "blas", "32"]`                           |   6.434 ms (5%) |         |                 |             |
| `["gemm", "fusedmul", "blas", "8"]`                            |   3.781 ms (5%) |         |                 |             |
| `["gemm", "fusedmul", "xf", "16"]`                             |   4.842 ms (5%) |         |  192 bytes (1%) |           4 |
| `["gemm", "fusedmul", "xf", "2"]`                              | 619.102 μs (5%) |         |  192 bytes (1%) |           4 |
| `["gemm", "fusedmul", "xf", "32"]`                             |  10.207 ms (5%) |         |  192 bytes (1%) |           4 |
| `["gemm", "fusedmul", "xf", "8"]`                              |   2.491 ms (5%) |         |  192 bytes (1%) |           4 |
| `["gemm", "mul", "linalg", "256"]`                             | 967.003 μs (5%) |         |                 |             |
| `["gemm", "mul", "linalg", "32"]`                              |   3.538 μs (5%) |         |                 |             |
| `["gemm", "mul", "linalg", "8"]`                               | 278.767 ns (5%) |         |                 |             |
| `["gemm", "mul", "man", "false", "256"]`                       |   4.287 ms (5%) |         |                 |             |
| `["gemm", "mul", "man", "false", "32"]`                        |   7.200 μs (5%) |         |                 |             |
| `["gemm", "mul", "man", "false", "8"]`                         | 376.617 ns (5%) |         |                 |             |
| `["gemm", "mul", "man", "ivdep", "256"]`                       |   4.243 ms (5%) |         |                 |             |
| `["gemm", "mul", "man", "ivdep", "32"]`                        |   5.517 μs (5%) |         |                 |             |
| `["gemm", "mul", "man", "ivdep", "8"]`                         | 355.560 ns (5%) |         |                 |             |
| `["gemm", "mul", "man", "true", "256"]`                        |   4.293 ms (5%) |         |                 |             |
| `["gemm", "mul", "man", "true", "32"]`                         |   6.760 μs (5%) |         |                 |             |
| `["gemm", "mul", "man", "true", "8"]`                          | 415.152 ns (5%) |         |                 |             |
| `["gemm", "mul", "xf", "false", "256"]`                        |   4.320 ms (5%) |         |   80 bytes (1%) |           3 |
| `["gemm", "mul", "xf", "false", "32"]`                         |   7.250 μs (5%) |         |   80 bytes (1%) |           3 |
| `["gemm", "mul", "xf", "false", "8"]`                          | 455.897 ns (5%) |         |   80 bytes (1%) |           3 |
| `["gemm", "mul", "xf", "ivdep", "256"]`                        |   4.244 ms (5%) |         |   80 bytes (1%) |           3 |
| `["gemm", "mul", "xf", "ivdep", "32"]`                         |   5.617 μs (5%) |         |   80 bytes (1%) |           3 |
| `["gemm", "mul", "xf", "ivdep", "8"]`                          | 394.527 ns (5%) |         |   80 bytes (1%) |           3 |
| `["gemm", "mul", "xf", "true", "256"]`                         |   4.314 ms (5%) |         |   80 bytes (1%) |           3 |
| `["gemm", "mul", "xf", "true", "32"]`                          |   6.780 μs (5%) |         |   80 bytes (1%) |           3 |
| `["gemm", "mul", "xf", "true", "8"]`                           | 426.638 ns (5%) |         |   80 bytes (1%) |           3 |
| `["groupby", "sum", "sac"]`                                    | 165.400 μs (5%) |         |   1.28 KiB (1%) |          14 |
| `["groupby", "sum", "xf-with-init"]`                           | 130.800 μs (5%) |         |   1.20 KiB (1%) |           9 |
| `["groupby", "sum", "xf-without-init"]`                        | 139.600 μs (5%) |         |   1.20 KiB (1%) |           9 |
| `["mapcat_eduction", "base"]`                                  |   1.470 μs (5%) |         |                 |             |
| `["mapcat_eduction", "xf-eduction"]`                           |   1.770 μs (5%) |         |                 |             |
| `["mapcat_eduction", "xf-xf"]`                                 |   1.770 μs (5%) |         |                 |             |
| `["missing_argmax", "man"]`                                    | 963.158 ns (5%) |         |   32 bytes (1%) |           1 |
| `["missing_argmax", "rf"]`                                     |   1.270 μs (5%) |         |   32 bytes (1%) |           1 |
| `["missing_argmax", "xf"]`                                     |   1.310 μs (5%) |         |   32 bytes (1%) |           1 |
| `["missing_dot", "equiv"]`                                     | 924.020 ns (5%) |         |   16 bytes (1%) |           1 |
| `["missing_dot", "man"]`                                       |   1.000 μs (5%) |         |   16 bytes (1%) |           1 |
| `["missing_dot", "naive"]`                                     |   4.043 μs (5%) |         |   16 bytes (1%) |           1 |
| `["missing_dot", "rf"]`                                        |   1.008 μs (5%) |         |   16 bytes (1%) |           1 |
| `["missing_dot", "rf_nota"]`                                   | 921.277 ns (5%) |         |   16 bytes (1%) |           1 |
| `["missing_dot", "xf"]`                                        |  87.700 μs (5%) |         |  71.98 KiB (1%) |        3734 |
| `["missing_dot", "xf_nota"]`                                   |  91.000 μs (5%) |         |  72.11 KiB (1%) |        3740 |
| `["overhead", "foldl"]`                                        |   4.200 ns (5%) |         |                 |             |
| `["overhead", "reduce_basecase"]`                              | 227.494 ns (5%) |         |  368 bytes (1%) |           6 |
| `["partition_by", "man"]`                                      |   1.767 ms (5%) |         |  352 bytes (1%) |           4 |
| `["partition_by", "xf"]`                                       |   1.774 ms (5%) |         |  544 bytes (1%) |           6 |
| `["set", "base"]`                                              |   4.475 ms (5%) |         |  49.56 KiB (1%) |          17 |
| `["set", "xf"]`                                                |   4.418 ms (5%) |         |  49.59 KiB (1%) |          19 |
| `["sum_transpose", "30", "noinit", "iter"]`                    |   1.860 μs (5%) |         |                 |             |
| `["sum_transpose", "30", "noinit", "man"]`                     |   1.340 μs (5%) |         |                 |             |
| `["sum_transpose", "30", "noinit", "xf"]`                      | 820.238 ns (5%) |         |   32 bytes (1%) |           2 |
| `["sum_transpose", "30", "withinit", "iter"]`                  |   1.340 μs (5%) |         |                 |             |
| `["sum_transpose", "30", "withinit", "man"]`                   | 728.244 ns (5%) |         |                 |             |
| `["sum_transpose", "30", "withinit", "xf"]`                    | 777.570 ns (5%) |         |   48 bytes (1%) |           3 |
| `["teerf_filter", "noinit"]`                                   |   1.830 μs (5%) |         |  160 bytes (1%) |           7 |
| `["teerf_filter", "withinit"]`                                 | 228.243 ns (5%) |         |                 |             |

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
      Ubuntu 18.04.5 LTS
  uname: Linux 5.4.0-1032-azure #33~18.04.1-Ubuntu SMP Tue Nov 17 11:40:52 UTC 2020 x86_64 x86_64
  CPU: Intel(R) Xeon(R) CPU E5-2673 v4 @ 2.30GHz: 
              speed         user         nice          sys         idle          irq
       #1  2294 MHz      58029 s          0 s       1384 s      21164 s          0 s
       #2  2294 MHz      19634 s          0 s       1640 s      59323 s          0 s
       
  Memory: 6.7913970947265625 GB (3653.140625 MB free)
  Uptime: 820.0 sec
  Load Avg:  1.0576171875  1.00146484375  0.6572265625
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-9.0.1 (ORCJIT, broadwell)
```

---
# Baseline result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmark: 13 Jan 2021 - 1:46
* Package commit: dbdd4d
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
| `["append!!", "eduction"]`                                     |  15.500 μs (5%) |         |  64.63 KiB (1%) |          13 |
| `["append!!", "xf"]`                                           |  15.200 μs (5%) |         |  64.63 KiB (1%) |          13 |
| `["cartesian", "copyto!", "iter"]`                             |   4.943 μs (5%) |         |                 |             |
| `["cartesian", "copyto!", "man"]`                              |   1.850 μs (5%) |         |                 |             |
| `["cartesian", "copyto!", "xf"]`                               |   2.344 μs (5%) |         |                 |             |
| `["cat", "base"]`                                              |   1.670 μs (5%) |         |                 |             |
| `["cat", "xf"]`                                                |   2.156 μs (5%) |         |                 |             |
| `["collect", "filter-missing"]`                                |  47.900 μs (5%) |         |  32.81 KiB (1%) |          14 |
| `["collect", "identity-float"]`                                |  24.300 μs (5%) |         | 256.66 KiB (1%) |          14 |
| `["collect", "identity-union"]`                                | 132.001 μs (5%) |         | 601.04 KiB (1%) |       10013 |
| `["dict", "base"]`                                             |   3.928 ms (5%) |         |  92.91 KiB (1%) |          22 |
| `["dict", "xf"]`                                               |   4.089 ms (5%) |         |  92.31 KiB (1%) |          18 |
| `["dot", "blas"]`                                              |   2.489 μs (5%) |         |                 |             |
| `["dot", "man"]`                                               |   2.233 μs (5%) |         |                 |             |
| `["dot", "rf"]`                                                |   3.063 μs (5%) |         |                 |             |
| `["dot", "xf"]`                                                |   3.150 μs (5%) |         |   64 bytes (1%) |           3 |
| `["filter_map_map!", "man"]`                                   |  66.000 μs (5%) |         |                 |             |
| `["filter_map_map!", "xf"]`                                    | 526.103 μs (5%) |         |   80 bytes (1%) |           3 |
| `["filter_map_reduce", "man"]`                                 | 194.901 μs (5%) |         |                 |             |
| `["filter_map_reduce", "xf"]`                                  | 194.901 μs (5%) |         |                 |             |
| `["filter_sum", "1000", "RandomFloats", "noinit", "base"]`     | 900.000 ns (5%) |         |                 |             |
| `["filter_sum", "1000", "RandomFloats", "noinit", "naive"]`    | 993.130 ns (5%) |         |                 |             |
| `["filter_sum", "1000", "RandomFloats", "noinit", "xf"]`       |   1.380 μs (5%) |         |                 |             |
| `["filter_sum", "1000", "RandomFloats", "withinit", "base"]`   |   1.460 μs (5%) |         |                 |             |
| `["filter_sum", "1000", "RandomFloats", "withinit", "naive"]`  | 857.534 ns (5%) |         |                 |             |
| `["filter_sum", "1000", "RandomFloats", "withinit", "xf"]`     |   1.460 μs (5%) |         |                 |             |
| `["filter_sum", "1000", "UnitRange", "noinit", "base"]`        |   1.640 μs (5%) |         |                 |             |
| `["filter_sum", "1000", "UnitRange", "noinit", "naive"]`       | 709.028 ns (5%) |         |                 |             |
| `["filter_sum", "1000", "UnitRange", "noinit", "xf"]`          | 159.603 ns (5%) |         |                 |             |
| `["filter_sum", "1000", "UnitRange", "withinit", "base"]`      | 156.787 ns (5%) |         |                 |             |
| `["filter_sum", "1000", "UnitRange", "withinit", "naive"]`     | 519.289 ns (5%) |         |                 |             |
| `["filter_sum", "1000", "UnitRange", "withinit", "xf"]`        | 159.091 ns (5%) |         |                 |             |
| `["filter_sum", "10000", "RandomFloats", "noinit", "base"]`    |  29.300 μs (5%) |         |                 |             |
| `["filter_sum", "10000", "RandomFloats", "noinit", "naive"]`   |  38.800 μs (5%) |         |                 |             |
| `["filter_sum", "10000", "RandomFloats", "noinit", "xf"]`      |  13.900 μs (5%) |         |                 |             |
| `["filter_sum", "10000", "RandomFloats", "withinit", "base"]`  |  14.700 μs (5%) |         |                 |             |
| `["filter_sum", "10000", "RandomFloats", "withinit", "naive"]` |  36.800 μs (5%) |         |                 |             |
| `["filter_sum", "10000", "RandomFloats", "withinit", "xf"]`    |  13.900 μs (5%) |         |                 |             |
| `["filter_sum", "10000", "UnitRange", "noinit", "base"]`       |  16.300 μs (5%) |         |                 |             |
| `["filter_sum", "10000", "UnitRange", "noinit", "naive"]`      |   6.980 μs (5%) |         |                 |             |
| `["filter_sum", "10000", "UnitRange", "noinit", "xf"]`         |   1.550 μs (5%) |         |                 |             |
| `["filter_sum", "10000", "UnitRange", "withinit", "base"]`     |   1.410 μs (5%) |         |                 |             |
| `["filter_sum", "10000", "UnitRange", "withinit", "naive"]`    |   5.457 μs (5%) |         |                 |             |
| `["filter_sum", "10000", "UnitRange", "withinit", "xf"]`       |   1.460 μs (5%) |         |                 |             |
| `["findall", "base"]`                                          | 757.706 μs (5%) |         |   2.00 MiB (1%) |          18 |
| `["findall", "xf-array"]`                                      | 678.506 μs (5%) |         |   3.02 MiB (1%) |       98829 |
| `["findall", "xf-iter"]`                                       | 295.302 μs (5%) |         |   2.00 MiB (1%) |          19 |
| `["gemm", "fusedmul", "blas", "16"]`                           |   4.709 ms (5%) |         |                 |             |
| `["gemm", "fusedmul", "blas", "2"]`                            |   3.696 ms (5%) |         |                 |             |
| `["gemm", "fusedmul", "blas", "32"]`                           |   6.719 ms (5%) |         |                 |             |
| `["gemm", "fusedmul", "blas", "8"]`                            |   3.803 ms (5%) |         |                 |             |
| `["gemm", "fusedmul", "xf", "16"]`                             |   4.904 ms (5%) |         |  192 bytes (1%) |           4 |
| `["gemm", "fusedmul", "xf", "2"]`                              | 604.003 μs (5%) |         |  192 bytes (1%) |           4 |
| `["gemm", "fusedmul", "xf", "32"]`                             |   9.961 ms (5%) |         |  192 bytes (1%) |           4 |
| `["gemm", "fusedmul", "xf", "8"]`                              |   2.420 ms (5%) |         |  192 bytes (1%) |           4 |
| `["gemm", "mul", "linalg", "256"]`                             | 964.706 μs (5%) |         |                 |             |
| `["gemm", "mul", "linalg", "32"]`                              |   4.000 μs (5%) |         |                 |             |
| `["gemm", "mul", "linalg", "8"]`                               | 300.000 ns (5%) |         |                 |             |
| `["gemm", "mul", "man", "false", "256"]`                       |   4.291 ms (5%) |         |                 |             |
| `["gemm", "mul", "man", "false", "32"]`                        |   7.200 μs (5%) |         |                 |             |
| `["gemm", "mul", "man", "false", "8"]`                         | 400.000 ns (5%) |         |                 |             |
| `["gemm", "mul", "man", "ivdep", "256"]`                       |   4.434 ms (5%) |         |                 |             |
| `["gemm", "mul", "man", "ivdep", "32"]`                        |   6.400 μs (5%) |         |                 |             |
| `["gemm", "mul", "man", "ivdep", "8"]`                         | 400.000 ns (5%) |         |                 |             |
| `["gemm", "mul", "man", "true", "256"]`                        |   4.205 ms (5%) |         |                 |             |
| `["gemm", "mul", "man", "true", "32"]`                         |   6.700 μs (5%) |         |                 |             |
| `["gemm", "mul", "man", "true", "8"]`                          | 300.000 ns (5%) |         |                 |             |
| `["gemm", "mul", "xf", "false", "256"]`                        |   4.237 ms (5%) |         |   80 bytes (1%) |           3 |
| `["gemm", "mul", "xf", "false", "32"]`                         |   7.200 μs (5%) |         |   80 bytes (1%) |           3 |
| `["gemm", "mul", "xf", "false", "8"]`                          | 400.000 ns (5%) |         |   80 bytes (1%) |           3 |
| `["gemm", "mul", "xf", "ivdep", "256"]`                        |   4.222 ms (5%) |         |   80 bytes (1%) |           3 |
| `["gemm", "mul", "xf", "ivdep", "32"]`                         |   5.600 μs (5%) |         |   80 bytes (1%) |           3 |
| `["gemm", "mul", "xf", "ivdep", "8"]`                          | 400.000 ns (5%) |         |   80 bytes (1%) |           3 |
| `["gemm", "mul", "xf", "true", "256"]`                         |   4.240 ms (5%) |         |   80 bytes (1%) |           3 |
| `["gemm", "mul", "xf", "true", "32"]`                          |   6.900 μs (5%) |         |   80 bytes (1%) |           3 |
| `["gemm", "mul", "xf", "true", "8"]`                           | 300.000 ns (5%) |         |   80 bytes (1%) |           3 |
| `["groupby", "sum", "sac"]`                                    | 159.200 μs (5%) |         |  624 bytes (1%) |           5 |
| `["groupby", "sum", "xf-with-init"]`                           | 129.901 μs (5%) |         |   1.20 KiB (1%) |           9 |
| `["groupby", "sum", "xf-without-init"]`                        | 131.800 μs (5%) |         |   1.20 KiB (1%) |           9 |
| `["mapcat_eduction", "base"]`                                  |   1.520 μs (5%) |         |                 |             |
| `["mapcat_eduction", "xf-eduction"]`                           |   1.770 μs (5%) |         |                 |             |
| `["mapcat_eduction", "xf-xf"]`                                 |   1.770 μs (5%) |         |                 |             |
| `["missing_argmax", "man"]`                                    | 968.421 ns (5%) |         |   32 bytes (1%) |           1 |
| `["missing_argmax", "rf"]`                                     |   1.360 μs (5%) |         |   32 bytes (1%) |           1 |
| `["missing_argmax", "xf"]`                                     |   1.290 μs (5%) |         |   32 bytes (1%) |           1 |
| `["missing_dot", "equiv"]`                                     | 984.000 ns (5%) |         |   16 bytes (1%) |           1 |
| `["missing_dot", "man"]`                                       |   1.021 μs (5%) |         |   16 bytes (1%) |           1 |
| `["missing_dot", "naive"]`                                     |   4.043 μs (5%) |         |   16 bytes (1%) |           1 |
| `["missing_dot", "rf"]`                                        |   1.015 μs (5%) |         |   16 bytes (1%) |           1 |
| `["missing_dot", "rf_nota"]`                                   |   1.011 μs (5%) |         |   16 bytes (1%) |           1 |
| `["missing_dot", "xf"]`                                        |  94.900 μs (5%) |         |  72.22 KiB (1%) |        3746 |
| `["missing_dot", "xf_nota"]`                                   |  90.400 μs (5%) |         |  72.13 KiB (1%) |        3742 |
| `["overhead", "foldl"]`                                        |   4.100 ns (5%) |         |                 |             |
| `["overhead", "reduce_basecase"]`                              | 239.470 ns (5%) |         |  368 bytes (1%) |           6 |
| `["partition_by", "man"]`                                      |   1.761 ms (5%) |         |  352 bytes (1%) |           4 |
| `["partition_by", "xf"]`                                       |   1.766 ms (5%) |         |  544 bytes (1%) |           6 |
| `["set", "base"]`                                              |   4.622 ms (5%) |         |  49.56 KiB (1%) |          17 |
| `["set", "xf"]`                                                |   4.330 ms (5%) |         |  49.59 KiB (1%) |          19 |
| `["sum_transpose", "30", "noinit", "iter"]`                    |   1.870 μs (5%) |         |                 |             |
| `["sum_transpose", "30", "noinit", "man"]`                     |   1.420 μs (5%) |         |                 |             |
| `["sum_transpose", "30", "noinit", "xf"]`                      | 820.250 ns (5%) |         |   32 bytes (1%) |           2 |
| `["sum_transpose", "30", "withinit", "iter"]`                  |   1.270 μs (5%) |         |                 |             |
| `["sum_transpose", "30", "withinit", "man"]`                   | 748.855 ns (5%) |         |                 |             |
| `["sum_transpose", "30", "withinit", "xf"]`                    | 778.505 ns (5%) |         |   48 bytes (1%) |           3 |
| `["teerf_filter", "noinit"]`                                   |   1.990 μs (5%) |         |  160 bytes (1%) |           7 |
| `["teerf_filter", "withinit"]`                                 | 244.354 ns (5%) |         |                 |             |

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
      Ubuntu 18.04.5 LTS
  uname: Linux 5.4.0-1032-azure #33~18.04.1-Ubuntu SMP Tue Nov 17 11:40:52 UTC 2020 x86_64 x86_64
  CPU: Intel(R) Xeon(R) CPU E5-2673 v4 @ 2.30GHz: 
              speed         user         nice          sys         idle          irq
       #1  2294 MHz      87975 s          0 s       1668 s      24063 s          0 s
       #2  2294 MHz      22536 s          0 s       1803 s      89303 s          0 s
       
  Memory: 6.7913970947265625 GB (3634.08984375 MB free)
  Uptime: 1152.0 sec
  Load Avg:  1.1162109375  1.0322265625  0.7880859375
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
    Model:               79
    Model name:          Intel(R) Xeon(R) CPU E5-2673 v4 @ 2.30GHz
    Stepping:            1
    CPU MHz:             2294.683
    BogoMIPS:            4589.36
    Hypervisor vendor:   Microsoft
    Virtualization type: full
    L1d cache:           32K
    L1i cache:           32K
    L2 cache:            256K
    L3 cache:            51200K
    NUMA node0 CPU(s):   0,1
    Flags:               fpu vme de pse tsc msr pae mce cx8 apic sep mtrr pge mca cmov pat pse36 clflush mmx fxsr sse sse2 ss ht syscall nx pdpe1gb rdtscp lm constant_tsc rep_good nopl xtopology cpuid pni pclmulqdq ssse3 fma cx16 pcid sse4_1 sse4_2 movbe popcnt aes xsave avx f16c rdrand hypervisor lahf_lm abm 3dnowprefetch invpcid_single pti fsgsbase bmi1 hle avx2 smep bmi2 erms invpcid rtm rdseed adx smap xsaveopt md_clear
    

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

