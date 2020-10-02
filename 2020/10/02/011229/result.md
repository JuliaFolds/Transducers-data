# Benchmark result

* Pull request commit: [`9a58185290c456d4ef4d416c32d2948ebdf9fe8a`](https://github.com/JuliaFolds/Transducers.jl/commit/9a58185290c456d4ef4d416c32d2948ebdf9fe8a)
* Pull request: <https://github.com/JuliaFolds/Transducers.jl/pull/243> (Update */Manifest.toml)

# Judge result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmarks:
    - Target: 2 Oct 2020 - 01:06
    - Baseline: 2 Oct 2020 - 01:11
* Package commits:
    - Target: bf5738
    - Baseline: 8831b8
* Julia commits:
    - Target: 539f3c
    - Baseline: 539f3c
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
| `["append!!", "xf"]`                                           |                1.06 (5%) :x: |    1.00 (1%)  |
| `["collect", "identity-float"]`                                |                1.18 (5%) :x: |    1.00 (1%)  |
| `["dict", "base"]`                                             | 0.94 (5%) :white_check_mark: |    1.00 (1%)  |
| `["dict", "xf"]`                                               | 0.95 (5%) :white_check_mark: |    1.00 (1%)  |
| `["filter_sum", "1000", "RandomFloats", "noinit", "base"]`     |                3.85 (5%) :x: |    1.00 (1%)  |
| `["filter_sum", "1000", "RandomFloats", "noinit", "naive"]`    | 0.95 (5%) :white_check_mark: |    1.00 (1%)  |
| `["filter_sum", "1000", "RandomFloats", "withinit", "naive"]`  |                1.16 (5%) :x: |    1.00 (1%)  |
| `["filter_sum", "1000", "UnitRange", "withinit", "naive"]`     |                1.14 (5%) :x: |    1.00 (1%)  |
| `["filter_sum", "10000", "RandomFloats", "noinit", "base"]`    |                1.20 (5%) :x: |    1.00 (1%)  |
| `["filter_sum", "10000", "UnitRange", "withinit", "naive"]`    |                1.12 (5%) :x: |    1.00 (1%)  |
| `["gemm", "mul", "linalg", "8"]`                               | 0.93 (5%) :white_check_mark: |    1.00 (1%)  |
| `["gemm", "mul", "man", "false", "8"]`                         |                1.26 (5%) :x: |    1.00 (1%)  |
| `["gemm", "mul", "man", "ivdep", "8"]`                         | 0.91 (5%) :white_check_mark: |    1.00 (1%)  |
| `["gemm", "mul", "xf", "false", "8"]`                          |                1.13 (5%) :x: |    1.00 (1%)  |
| `["gemm", "mul", "xf", "ivdep", "8"]`                          |                1.29 (5%) :x: |    1.00 (1%)  |
| `["gemm", "mul", "xf", "true", "8"]`                           |                1.06 (5%) :x: |    1.00 (1%)  |
| `["groupby", "sum", "sac"]`                                    | 0.77 (5%) :white_check_mark: | 2.51 (1%) :x: |

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
Julia Version 1.5.2
Commit 539f3ce943 (2020-09-23 23:17 UTC)
Platform Info:
  OS: Linux (x86_64-pc-linux-gnu)
      Ubuntu 18.04.5 LTS
  uname: Linux 5.4.0-1025-azure #25~18.04.1-Ubuntu SMP Sat Sep 5 15:28:57 UTC 2020 x86_64 x86_64
  CPU: Intel(R) Xeon(R) CPU E5-2673 v4 @ 2.30GHz: 
              speed         user         nice          sys         idle          irq
       #1  2294 MHz      66486 s          0 s       1250 s      17518 s          0 s
       #2  2294 MHz       9462 s          0 s       1486 s      74752 s          0 s
       
  Memory: 6.764892578125 GB (3297.078125 MB free)
  Uptime: 875.0 sec
  Load Avg:  1.0  0.9912109375  0.693359375
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-9.0.1 (ORCJIT, broadwell)
```

### Baseline
```
Julia Version 1.5.2
Commit 539f3ce943 (2020-09-23 23:17 UTC)
Platform Info:
  OS: Linux (x86_64-pc-linux-gnu)
      Ubuntu 18.04.5 LTS
  uname: Linux 5.4.0-1025-azure #25~18.04.1-Ubuntu SMP Sat Sep 5 15:28:57 UTC 2020 x86_64 x86_64
  CPU: Intel(R) Xeon(R) CPU E5-2673 v4 @ 2.30GHz: 
              speed         user         nice          sys         idle          irq
       #1  2294 MHz      94256 s          0 s       1523 s      22055 s          0 s
       #2  2294 MHz      13983 s          0 s       1666 s     102674 s          0 s
       
  Memory: 6.764892578125 GB (3198.671875 MB free)
  Uptime: 1203.0 sec
  Load Avg:  1.0  1.0  0.806640625
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-9.0.1 (ORCJIT, broadwell)
```

---
# Target result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmark: 2 Oct 2020 - 1:6
* Package commit: bf5738
* Julia commit: 539f3c
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
| `["append!!", "eduction"]`                                     |  15.800 μs (5%) |         |  64.63 KiB (1%) |          13 |
| `["append!!", "xf"]`                                           |  16.000 μs (5%) |         |  64.63 KiB (1%) |          13 |
| `["cartesian", "copyto!", "iter"]`                             |   4.957 μs (5%) |         |                 |             |
| `["cartesian", "copyto!", "man"]`                              |   1.980 μs (5%) |         |                 |             |
| `["cartesian", "copyto!", "xf"]`                               |   2.333 μs (5%) |         |                 |             |
| `["cat", "base"]`                                              |   1.570 μs (5%) |         |                 |             |
| `["cat", "xf"]`                                                |   2.022 μs (5%) |         |                 |             |
| `["collect", "filter-missing"]`                                |  46.900 μs (5%) |         |  32.81 KiB (1%) |          14 |
| `["collect", "identity-float"]`                                |  26.900 μs (5%) |         | 256.66 KiB (1%) |          14 |
| `["collect", "identity-union"]`                                | 131.400 μs (5%) |         | 601.04 KiB (1%) |       10013 |
| `["dict", "base"]`                                             |   3.811 ms (5%) |         |  92.91 KiB (1%) |          22 |
| `["dict", "xf"]`                                               |   3.836 ms (5%) |         |  92.31 KiB (1%) |          18 |
| `["dot", "blas"]`                                              |   2.222 μs (5%) |         |                 |             |
| `["dot", "man"]`                                               |   2.222 μs (5%) |         |                 |             |
| `["dot", "rf"]`                                                |   3.050 μs (5%) |         |                 |             |
| `["dot", "xf"]`                                                |   3.150 μs (5%) |         |   64 bytes (1%) |           3 |
| `["filter_map_map!", "man"]`                                   |  70.100 μs (5%) |         |                 |             |
| `["filter_map_map!", "xf"]`                                    | 524.301 μs (5%) |         |   80 bytes (1%) |           3 |
| `["filter_map_reduce", "man"]`                                 | 194.900 μs (5%) |         |                 |             |
| `["filter_map_reduce", "xf"]`                                  | 194.900 μs (5%) |         |                 |             |
| `["filter_sum", "1000", "RandomFloats", "noinit", "base"]`     |   2.778 μs (5%) |         |                 |             |
| `["filter_sum", "1000", "RandomFloats", "noinit", "naive"]`    | 701.538 ns (5%) |         |                 |             |
| `["filter_sum", "1000", "RandomFloats", "noinit", "xf"]`       |   1.380 μs (5%) |         |                 |             |
| `["filter_sum", "1000", "RandomFloats", "withinit", "base"]`   |   1.380 μs (5%) |         |                 |             |
| `["filter_sum", "1000", "RandomFloats", "withinit", "naive"]`  | 845.455 ns (5%) |         |                 |             |
| `["filter_sum", "1000", "RandomFloats", "withinit", "xf"]`     |   1.380 μs (5%) |         |                 |             |
| `["filter_sum", "1000", "UnitRange", "noinit", "base"]`        |   1.550 μs (5%) |         |                 |             |
| `["filter_sum", "1000", "UnitRange", "noinit", "naive"]`       | 703.497 ns (5%) |         |                 |             |
| `["filter_sum", "1000", "UnitRange", "noinit", "xf"]`          | 160.025 ns (5%) |         |                 |             |
| `["filter_sum", "1000", "UnitRange", "withinit", "base"]`      | 156.750 ns (5%) |         |                 |             |
| `["filter_sum", "1000", "UnitRange", "withinit", "naive"]`     | 518.848 ns (5%) |         |                 |             |
| `["filter_sum", "1000", "UnitRange", "withinit", "xf"]`        | 159.091 ns (5%) |         |                 |             |
| `["filter_sum", "10000", "RandomFloats", "noinit", "base"]`    |  40.300 μs (5%) |         |                 |             |
| `["filter_sum", "10000", "RandomFloats", "noinit", "naive"]`   |  38.100 μs (5%) |         |                 |             |
| `["filter_sum", "10000", "RandomFloats", "noinit", "xf"]`      |  13.900 μs (5%) |         |                 |             |
| `["filter_sum", "10000", "RandomFloats", "withinit", "base"]`  |  13.900 μs (5%) |         |                 |             |
| `["filter_sum", "10000", "RandomFloats", "withinit", "naive"]` |  36.501 μs (5%) |         |                 |             |
| `["filter_sum", "10000", "RandomFloats", "withinit", "xf"]`    |  13.900 μs (5%) |         |                 |             |
| `["filter_sum", "10000", "UnitRange", "noinit", "base"]`       |  15.400 μs (5%) |         |                 |             |
| `["filter_sum", "10000", "UnitRange", "noinit", "naive"]`      |   6.980 μs (5%) |         |                 |             |
| `["filter_sum", "10000", "UnitRange", "noinit", "xf"]`         |   1.460 μs (5%) |         |                 |             |
| `["filter_sum", "10000", "UnitRange", "withinit", "base"]`     |   1.410 μs (5%) |         |                 |             |
| `["filter_sum", "10000", "UnitRange", "withinit", "naive"]`    |   4.967 μs (5%) |         |                 |             |
| `["filter_sum", "10000", "UnitRange", "withinit", "xf"]`       |   1.460 μs (5%) |         |                 |             |
| `["findall", "base"]`                                          | 728.602 μs (5%) |         |   2.00 MiB (1%) |          18 |
| `["findall", "xf-array"]`                                      | 675.102 μs (5%) |         |   3.02 MiB (1%) |       98829 |
| `["findall", "xf-iter"]`                                       | 270.301 μs (5%) |         |   2.00 MiB (1%) |          19 |
| `["gemm", "fusedmul", "blas", "16"]`                           |   4.738 ms (5%) |         |                 |             |
| `["gemm", "fusedmul", "blas", "2"]`                            |   3.545 ms (5%) |         |                 |             |
| `["gemm", "fusedmul", "blas", "32"]`                           |   6.253 ms (5%) |         |                 |             |
| `["gemm", "fusedmul", "blas", "8"]`                            |   3.663 ms (5%) |         |                 |             |
| `["gemm", "fusedmul", "xf", "16"]`                             |   5.045 ms (5%) |         |  192 bytes (1%) |           4 |
| `["gemm", "fusedmul", "xf", "2"]`                              | 628.301 μs (5%) |         |  192 bytes (1%) |           4 |
| `["gemm", "fusedmul", "xf", "32"]`                             |  10.076 ms (5%) |         |  192 bytes (1%) |           4 |
| `["gemm", "fusedmul", "xf", "8"]`                              |   2.516 ms (5%) |         |  192 bytes (1%) |           4 |
| `["gemm", "mul", "linalg", "256"]`                             | 970.402 μs (5%) |         |                 |             |
| `["gemm", "mul", "linalg", "32"]`                              |   3.513 μs (5%) |         |                 |             |
| `["gemm", "mul", "linalg", "8"]`                               | 277.551 ns (5%) |         |                 |             |
| `["gemm", "mul", "man", "false", "256"]`                       |   4.361 ms (5%) |         |                 |             |
| `["gemm", "mul", "man", "false", "32"]`                        |   7.425 μs (5%) |         |                 |             |
| `["gemm", "mul", "man", "false", "8"]`                         | 376.585 ns (5%) |         |                 |             |
| `["gemm", "mul", "man", "ivdep", "256"]`                       |   4.320 ms (5%) |         |                 |             |
| `["gemm", "mul", "man", "ivdep", "32"]`                        |   5.500 μs (5%) |         |                 |             |
| `["gemm", "mul", "man", "ivdep", "8"]`                         | 363.942 ns (5%) |         |                 |             |
| `["gemm", "mul", "man", "true", "256"]`                        |   4.354 ms (5%) |         |                 |             |
| `["gemm", "mul", "man", "true", "32"]`                         |   6.880 μs (5%) |         |                 |             |
| `["gemm", "mul", "man", "true", "8"]`                          | 415.578 ns (5%) |         |                 |             |
| `["gemm", "mul", "xf", "false", "256"]`                        |   4.360 ms (5%) |         |   80 bytes (1%) |           3 |
| `["gemm", "mul", "xf", "false", "32"]`                         |   7.450 μs (5%) |         |   80 bytes (1%) |           3 |
| `["gemm", "mul", "xf", "false", "8"]`                          | 452.551 ns (5%) |         |   80 bytes (1%) |           3 |
| `["gemm", "mul", "xf", "ivdep", "256"]`                        |   4.319 ms (5%) |         |   80 bytes (1%) |           3 |
| `["gemm", "mul", "xf", "ivdep", "32"]`                         |   5.600 μs (5%) |         |   80 bytes (1%) |           3 |
| `["gemm", "mul", "xf", "ivdep", "8"]`                          | 388.177 ns (5%) |         |   80 bytes (1%) |           3 |
| `["gemm", "mul", "xf", "true", "256"]`                         |   4.344 ms (5%) |         |   80 bytes (1%) |           3 |
| `["gemm", "mul", "xf", "true", "32"]`                          |   7.000 μs (5%) |         |   80 bytes (1%) |           3 |
| `["gemm", "mul", "xf", "true", "8"]`                           | 422.222 ns (5%) |         |   80 bytes (1%) |           3 |
| `["groupby", "sum", "sac"]`                                    | 124.200 μs (5%) |         |   1.53 KiB (1%) |          16 |
| `["groupby", "sum", "xf-with-init"]`                           | 130.500 μs (5%) |         |   1.20 KiB (1%) |           9 |
| `["groupby", "sum", "xf-without-init"]`                        | 131.500 μs (5%) |         |   1.20 KiB (1%) |           9 |
| `["mapcat_eduction", "base"]`                                  |   1.510 μs (5%) |         |                 |             |
| `["mapcat_eduction", "xf-eduction"]`                           |   1.780 μs (5%) |         |                 |             |
| `["mapcat_eduction", "xf-xf"]`                                 |   1.780 μs (5%) |         |                 |             |
| `["missing_argmax", "man"]`                                    | 970.000 ns (5%) |         |   32 bytes (1%) |           1 |
| `["missing_argmax", "rf"]`                                     |   1.270 μs (5%) |         |   32 bytes (1%) |           1 |
| `["missing_argmax", "xf"]`                                     |   1.280 μs (5%) |         |   32 bytes (1%) |           1 |
| `["missing_dot", "equiv"]`                                     | 916.327 ns (5%) |         |   16 bytes (1%) |           1 |
| `["missing_dot", "man"]`                                       |   1.004 μs (5%) |         |   16 bytes (1%) |           1 |
| `["missing_dot", "naive"]`                                     |   4.043 μs (5%) |         |   16 bytes (1%) |           1 |
| `["missing_dot", "rf"]`                                        |   1.012 μs (5%) |         |   16 bytes (1%) |           1 |
| `["missing_dot", "rf_nota"]`                                   | 925.000 ns (5%) |         |   16 bytes (1%) |           1 |
| `["missing_dot", "xf"]`                                        |  91.400 μs (5%) |         |  72.14 KiB (1%) |        3742 |
| `["missing_dot", "xf_nota"]`                                   |  90.600 μs (5%) |         |  72.17 KiB (1%) |        3744 |
| `["overhead", "foldl"]`                                        |   3.900 ns (5%) |         |                 |             |
| `["overhead", "reduce_basecase"]`                              | 231.381 ns (5%) |         |  368 bytes (1%) |           6 |
| `["partition_by", "man"]`                                      |   1.821 ms (5%) |         |  352 bytes (1%) |           4 |
| `["partition_by", "xf"]`                                       |   1.765 ms (5%) |         |  544 bytes (1%) |           6 |
| `["set", "base"]`                                              |   4.549 ms (5%) |         |  49.56 KiB (1%) |          17 |
| `["set", "xf"]`                                                |   4.302 ms (5%) |         |  49.59 KiB (1%) |          19 |
| `["sum_transpose", "30", "noinit", "iter"]`                    |   1.870 μs (5%) |         |                 |             |
| `["sum_transpose", "30", "noinit", "man"]`                     |   1.340 μs (5%) |         |                 |             |
| `["sum_transpose", "30", "noinit", "xf"]`                      | 820.482 ns (5%) |         |   32 bytes (1%) |           2 |
| `["sum_transpose", "30", "withinit", "iter"]`                  |   1.260 μs (5%) |         |                 |             |
| `["sum_transpose", "30", "withinit", "man"]`                   | 728.244 ns (5%) |         |                 |             |
| `["sum_transpose", "30", "withinit", "xf"]`                    | 777.500 ns (5%) |         |   48 bytes (1%) |           3 |
| `["teerf_filter", "noinit"]`                                   | 418.095 ns (5%) |         |  112 bytes (1%) |           4 |
| `["teerf_filter", "withinit"]`                                 | 228.642 ns (5%) |         |                 |             |

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
Julia Version 1.5.2
Commit 539f3ce943 (2020-09-23 23:17 UTC)
Platform Info:
  OS: Linux (x86_64-pc-linux-gnu)
      Ubuntu 18.04.5 LTS
  uname: Linux 5.4.0-1025-azure #25~18.04.1-Ubuntu SMP Sat Sep 5 15:28:57 UTC 2020 x86_64 x86_64
  CPU: Intel(R) Xeon(R) CPU E5-2673 v4 @ 2.30GHz: 
              speed         user         nice          sys         idle          irq
       #1  2294 MHz      66486 s          0 s       1250 s      17518 s          0 s
       #2  2294 MHz       9462 s          0 s       1486 s      74752 s          0 s
       
  Memory: 6.764892578125 GB (3297.078125 MB free)
  Uptime: 875.0 sec
  Load Avg:  1.0  0.9912109375  0.693359375
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-9.0.1 (ORCJIT, broadwell)
```

---
# Baseline result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmark: 2 Oct 2020 - 1:11
* Package commit: 8831b8
* Julia commit: 539f3c
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
| `["append!!", "eduction"]`                                     |  15.600 μs (5%) |         |  64.63 KiB (1%) |          13 |
| `["append!!", "xf"]`                                           |  15.100 μs (5%) |         |  64.63 KiB (1%) |          13 |
| `["cartesian", "copyto!", "iter"]`                             |   4.943 μs (5%) |         |                 |             |
| `["cartesian", "copyto!", "man"]`                              |   1.920 μs (5%) |         |                 |             |
| `["cartesian", "copyto!", "xf"]`                               |   2.344 μs (5%) |         |                 |             |
| `["cat", "base"]`                                              |   1.570 μs (5%) |         |                 |             |
| `["cat", "xf"]`                                                |   2.033 μs (5%) |         |                 |             |
| `["collect", "filter-missing"]`                                |  46.500 μs (5%) |         |  32.81 KiB (1%) |          14 |
| `["collect", "identity-float"]`                                |  22.800 μs (5%) |         | 256.66 KiB (1%) |          14 |
| `["collect", "identity-union"]`                                | 130.401 μs (5%) |         | 601.04 KiB (1%) |       10013 |
| `["dict", "base"]`                                             |   4.068 ms (5%) |         |  92.91 KiB (1%) |          22 |
| `["dict", "xf"]`                                               |   4.054 ms (5%) |         |  92.31 KiB (1%) |          18 |
| `["dot", "blas"]`                                              |   2.233 μs (5%) |         |                 |             |
| `["dot", "man"]`                                               |   2.222 μs (5%) |         |                 |             |
| `["dot", "rf"]`                                                |   3.063 μs (5%) |         |                 |             |
| `["dot", "xf"]`                                                |   3.150 μs (5%) |         |   64 bytes (1%) |           3 |
| `["filter_map_map!", "man"]`                                   |  68.201 μs (5%) |         |                 |             |
| `["filter_map_map!", "xf"]`                                    | 528.202 μs (5%) |         |   80 bytes (1%) |           3 |
| `["filter_map_reduce", "man"]`                                 | 194.900 μs (5%) |         |                 |             |
| `["filter_map_reduce", "xf"]`                                  | 194.900 μs (5%) |         |                 |             |
| `["filter_sum", "1000", "RandomFloats", "noinit", "base"]`     | 722.222 ns (5%) |         |                 |             |
| `["filter_sum", "1000", "RandomFloats", "noinit", "naive"]`    | 742.308 ns (5%) |         |                 |             |
| `["filter_sum", "1000", "RandomFloats", "noinit", "xf"]`       |   1.380 μs (5%) |         |                 |             |
| `["filter_sum", "1000", "RandomFloats", "withinit", "base"]`   |   1.380 μs (5%) |         |                 |             |
| `["filter_sum", "1000", "RandomFloats", "withinit", "naive"]`  | 729.883 ns (5%) |         |                 |             |
| `["filter_sum", "1000", "RandomFloats", "withinit", "xf"]`     |   1.380 μs (5%) |         |                 |             |
| `["filter_sum", "1000", "UnitRange", "noinit", "base"]`        |   1.550 μs (5%) |         |                 |             |
| `["filter_sum", "1000", "UnitRange", "noinit", "naive"]`       | 702.797 ns (5%) |         |                 |             |
| `["filter_sum", "1000", "UnitRange", "noinit", "xf"]`          | 159.402 ns (5%) |         |                 |             |
| `["filter_sum", "1000", "UnitRange", "withinit", "base"]`      | 155.751 ns (5%) |         |                 |             |
| `["filter_sum", "1000", "UnitRange", "withinit", "naive"]`     | 456.021 ns (5%) |         |                 |             |
| `["filter_sum", "1000", "UnitRange", "withinit", "xf"]`        | 158.587 ns (5%) |         |                 |             |
| `["filter_sum", "10000", "RandomFloats", "noinit", "base"]`    |  33.600 μs (5%) |         |                 |             |
| `["filter_sum", "10000", "RandomFloats", "noinit", "naive"]`   |  38.400 μs (5%) |         |                 |             |
| `["filter_sum", "10000", "RandomFloats", "noinit", "xf"]`      |  13.900 μs (5%) |         |                 |             |
| `["filter_sum", "10000", "RandomFloats", "withinit", "base"]`  |  13.900 μs (5%) |         |                 |             |
| `["filter_sum", "10000", "RandomFloats", "withinit", "naive"]` |  36.500 μs (5%) |         |                 |             |
| `["filter_sum", "10000", "RandomFloats", "withinit", "xf"]`    |  13.900 μs (5%) |         |                 |             |
| `["filter_sum", "10000", "UnitRange", "noinit", "base"]`       |  15.400 μs (5%) |         |                 |             |
| `["filter_sum", "10000", "UnitRange", "noinit", "naive"]`      |   6.960 μs (5%) |         |                 |             |
| `["filter_sum", "10000", "UnitRange", "noinit", "xf"]`         |   1.460 μs (5%) |         |                 |             |
| `["filter_sum", "10000", "UnitRange", "withinit", "base"]`     |   1.410 μs (5%) |         |                 |             |
| `["filter_sum", "10000", "UnitRange", "withinit", "naive"]`    |   4.417 μs (5%) |         |                 |             |
| `["filter_sum", "10000", "UnitRange", "withinit", "xf"]`       |   1.460 μs (5%) |         |                 |             |
| `["findall", "base"]`                                          | 751.904 μs (5%) |         |   2.00 MiB (1%) |          18 |
| `["findall", "xf-array"]`                                      | 674.703 μs (5%) |         |   3.02 MiB (1%) |       98829 |
| `["findall", "xf-iter"]`                                       | 277.001 μs (5%) |         |   2.00 MiB (1%) |          19 |
| `["gemm", "fusedmul", "blas", "16"]`                           |   4.738 ms (5%) |         |                 |             |
| `["gemm", "fusedmul", "blas", "2"]`                            |   3.551 ms (5%) |         |                 |             |
| `["gemm", "fusedmul", "blas", "32"]`                           |   6.257 ms (5%) |         |                 |             |
| `["gemm", "fusedmul", "blas", "8"]`                            |   3.674 ms (5%) |         |                 |             |
| `["gemm", "fusedmul", "xf", "16"]`                             |   5.048 ms (5%) |         |  192 bytes (1%) |           4 |
| `["gemm", "fusedmul", "xf", "2"]`                              | 628.902 μs (5%) |         |  192 bytes (1%) |           4 |
| `["gemm", "fusedmul", "xf", "32"]`                             |  10.218 ms (5%) |         |  192 bytes (1%) |           4 |
| `["gemm", "fusedmul", "xf", "8"]`                              |   2.518 ms (5%) |         |  192 bytes (1%) |           4 |
| `["gemm", "mul", "linalg", "256"]`                             | 970.004 μs (5%) |         |                 |             |
| `["gemm", "mul", "linalg", "32"]`                              |   3.500 μs (5%) |         |                 |             |
| `["gemm", "mul", "linalg", "8"]`                               | 300.000 ns (5%) |         |                 |             |
| `["gemm", "mul", "man", "false", "256"]`                       |   4.355 ms (5%) |         |                 |             |
| `["gemm", "mul", "man", "false", "32"]`                        |   7.400 μs (5%) |         |                 |             |
| `["gemm", "mul", "man", "false", "8"]`                         | 300.000 ns (5%) |         |                 |             |
| `["gemm", "mul", "man", "ivdep", "256"]`                       |   4.331 ms (5%) |         |                 |             |
| `["gemm", "mul", "man", "ivdep", "32"]`                        |   5.500 μs (5%) |         |                 |             |
| `["gemm", "mul", "man", "ivdep", "8"]`                         | 400.000 ns (5%) |         |                 |             |
| `["gemm", "mul", "man", "true", "256"]`                        |   4.341 ms (5%) |         |                 |             |
| `["gemm", "mul", "man", "true", "32"]`                         |   6.900 μs (5%) |         |                 |             |
| `["gemm", "mul", "man", "true", "8"]`                          | 400.000 ns (5%) |         |                 |             |
| `["gemm", "mul", "xf", "false", "256"]`                        |   4.353 ms (5%) |         |   80 bytes (1%) |           3 |
| `["gemm", "mul", "xf", "false", "32"]`                         |   7.500 μs (5%) |         |   80 bytes (1%) |           3 |
| `["gemm", "mul", "xf", "false", "8"]`                          | 400.000 ns (5%) |         |   80 bytes (1%) |           3 |
| `["gemm", "mul", "xf", "ivdep", "256"]`                        |   4.332 ms (5%) |         |   80 bytes (1%) |           3 |
| `["gemm", "mul", "xf", "ivdep", "32"]`                         |   5.600 μs (5%) |         |   80 bytes (1%) |           3 |
| `["gemm", "mul", "xf", "ivdep", "8"]`                          | 300.000 ns (5%) |         |   80 bytes (1%) |           3 |
| `["gemm", "mul", "xf", "true", "256"]`                         |   4.355 ms (5%) |         |   80 bytes (1%) |           3 |
| `["gemm", "mul", "xf", "true", "32"]`                          |   7.000 μs (5%) |         |   80 bytes (1%) |           3 |
| `["gemm", "mul", "xf", "true", "8"]`                           | 400.000 ns (5%) |         |   80 bytes (1%) |           3 |
| `["groupby", "sum", "sac"]`                                    | 160.900 μs (5%) |         |  624 bytes (1%) |           5 |
| `["groupby", "sum", "xf-with-init"]`                           | 129.400 μs (5%) |         |   1.20 KiB (1%) |           9 |
| `["groupby", "sum", "xf-without-init"]`                        | 130.200 μs (5%) |         |   1.20 KiB (1%) |           9 |
| `["mapcat_eduction", "base"]`                                  |   1.470 μs (5%) |         |                 |             |
| `["mapcat_eduction", "xf-eduction"]`                           |   1.770 μs (5%) |         |                 |             |
| `["mapcat_eduction", "xf-xf"]`                                 |   1.770 μs (5%) |         |                 |             |
| `["missing_argmax", "man"]`                                    | 970.000 ns (5%) |         |   32 bytes (1%) |           1 |
| `["missing_argmax", "rf"]`                                     |   1.250 μs (5%) |         |   32 bytes (1%) |           1 |
| `["missing_argmax", "xf"]`                                     |   1.250 μs (5%) |         |   32 bytes (1%) |           1 |
| `["missing_dot", "equiv"]`                                     | 908.163 ns (5%) |         |   16 bytes (1%) |           1 |
| `["missing_dot", "man"]`                                       |   1.007 μs (5%) |         |   16 bytes (1%) |           1 |
| `["missing_dot", "naive"]`                                     |   4.043 μs (5%) |         |   16 bytes (1%) |           1 |
| `["missing_dot", "rf"]`                                        |   1.025 μs (5%) |         |   16 bytes (1%) |           1 |
| `["missing_dot", "rf_nota"]`                                   | 932.692 ns (5%) |         |   16 bytes (1%) |           1 |
| `["missing_dot", "xf"]`                                        |  90.800 μs (5%) |         |  72.17 KiB (1%) |        3744 |
| `["missing_dot", "xf_nota"]`                                   |  91.300 μs (5%) |         |  72.22 KiB (1%) |        3746 |
| `["overhead", "foldl"]`                                        |   3.900 ns (5%) |         |                 |             |
| `["overhead", "reduce_basecase"]`                              | 225.941 ns (5%) |         |  368 bytes (1%) |           6 |
| `["partition_by", "man"]`                                      |   1.764 ms (5%) |         |  352 bytes (1%) |           4 |
| `["partition_by", "xf"]`                                       |   1.793 ms (5%) |         |  544 bytes (1%) |           6 |
| `["set", "base"]`                                              |   4.505 ms (5%) |         |  49.56 KiB (1%) |          17 |
| `["set", "xf"]`                                                |   4.337 ms (5%) |         |  49.59 KiB (1%) |          19 |
| `["sum_transpose", "30", "noinit", "iter"]`                    |   1.870 μs (5%) |         |                 |             |
| `["sum_transpose", "30", "noinit", "man"]`                     |   1.330 μs (5%) |         |                 |             |
| `["sum_transpose", "30", "noinit", "xf"]`                      | 820.482 ns (5%) |         |   32 bytes (1%) |           2 |
| `["sum_transpose", "30", "withinit", "iter"]`                  |   1.260 μs (5%) |         |                 |             |
| `["sum_transpose", "30", "withinit", "man"]`                   | 728.244 ns (5%) |         |                 |             |
| `["sum_transpose", "30", "withinit", "xf"]`                    | 777.500 ns (5%) |         |   48 bytes (1%) |           3 |
| `["teerf_filter", "noinit"]`                                   | 416.583 ns (5%) |         |  112 bytes (1%) |           4 |
| `["teerf_filter", "withinit"]`                                 | 229.136 ns (5%) |         |                 |             |

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
Julia Version 1.5.2
Commit 539f3ce943 (2020-09-23 23:17 UTC)
Platform Info:
  OS: Linux (x86_64-pc-linux-gnu)
      Ubuntu 18.04.5 LTS
  uname: Linux 5.4.0-1025-azure #25~18.04.1-Ubuntu SMP Sat Sep 5 15:28:57 UTC 2020 x86_64 x86_64
  CPU: Intel(R) Xeon(R) CPU E5-2673 v4 @ 2.30GHz: 
              speed         user         nice          sys         idle          irq
       #1  2294 MHz      94256 s          0 s       1523 s      22055 s          0 s
       #2  2294 MHz      13983 s          0 s       1666 s     102674 s          0 s
       
  Memory: 6.764892578125 GB (3198.671875 MB free)
  Uptime: 1203.0 sec
  Load Avg:  1.0  1.0  0.806640625
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
    CPU MHz:             2294.687
    BogoMIPS:            4589.37
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
| Address Size       | 48 bits virtual, 44 bits physical                       |
| SIMD               | 256 bit = 32 byte max. SIMD vector size                 |
| Time Stamp Counter | TSC is accessible via `rdtsc`                           |
|                    | TSC increased at every clock cycle (non-invariant TSC)  |
| Perf. Monitoring   | Performance Monitoring Counters (PMC) are not supported |
| Hypervisor         | Yes, Microsoft                                          |

