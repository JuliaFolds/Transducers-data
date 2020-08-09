# Benchmark result

* Pull request commit: [`6350f51789386780ff095ecf22f111d3b07d5bf0`](https://github.com/JuliaFolds/Transducers.jl/commit/6350f51789386780ff095ecf22f111d3b07d5bf0)
* Pull request: <https://github.com/JuliaFolds/Transducers.jl/pull/408> (Define is_prelude on Tuple and NamedTuple)

# Judge result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmarks:
    - Target: 9 Aug 2020 - 21:34
    - Baseline: 9 Aug 2020 - 21:39
* Package commits:
    - Target: 28b91b
    - Baseline: 6d7f6f
* Julia commits:
    - Target: 96786e
    - Baseline: 96786e
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
| `["cat", "base"]`                                              |                1.44 (5%) :x: |    1.00 (1%)  |
| `["collect", "identity-float"]`                                | 0.90 (5%) :white_check_mark: |    1.00 (1%)  |
| `["filter_map_map!", "man"]`                                   |                1.15 (5%) :x: |    1.00 (1%)  |
| `["filter_sum", "1000", "UnitRange", "noinit", "naive"]`       |                1.13 (5%) :x: |    1.00 (1%)  |
| `["filter_sum", "1000", "UnitRange", "withinit", "naive"]`     | 0.91 (5%) :white_check_mark: |    1.00 (1%)  |
| `["filter_sum", "10000", "RandomFloats", "noinit", "naive"]`   | 0.86 (5%) :white_check_mark: |    1.00 (1%)  |
| `["filter_sum", "10000", "UnitRange", "noinit", "naive"]`      |                1.14 (5%) :x: |    1.00 (1%)  |
| `["filter_sum", "10000", "UnitRange", "withinit", "naive"]`    | 0.91 (5%) :white_check_mark: |    1.00 (1%)  |
| `["gemm", "fusedmul", "blas", "32"]`                           |                1.06 (5%) :x: |    1.00 (1%)  |
| `["gemm", "fusedmul", "blas", "8"]`                            | 0.78 (5%) :white_check_mark: |    1.00 (1%)  |
| `["gemm", "fusedmul", "xf", "16"]`                             | 0.88 (5%) :white_check_mark: |    1.00 (1%)  |
| `["gemm", "fusedmul", "xf", "2"]`                              |                1.13 (5%) :x: |    1.00 (1%)  |
| `["gemm", "fusedmul", "xf", "32"]`                             | 0.92 (5%) :white_check_mark: |    1.00 (1%)  |
| `["gemm", "fusedmul", "xf", "8"]`                              | 0.91 (5%) :white_check_mark: |    1.00 (1%)  |
| `["gemm", "mul", "linalg", "8"]`                               |                1.21 (5%) :x: |    1.00 (1%)  |
| `["gemm", "mul", "man", "false", "256"]`                       | 0.94 (5%) :white_check_mark: |    1.00 (1%)  |
| `["gemm", "mul", "man", "false", "8"]`                         |                1.20 (5%) :x: |    1.00 (1%)  |
| `["gemm", "mul", "man", "ivdep", "8"]`                         |                1.08 (5%) :x: |    1.00 (1%)  |
| `["gemm", "mul", "man", "true", "256"]`                        | 0.95 (5%) :white_check_mark: |    1.00 (1%)  |
| `["gemm", "mul", "man", "true", "8"]`                          |                1.14 (5%) :x: |    1.00 (1%)  |
| `["gemm", "mul", "xf", "false", "256"]`                        | 0.94 (5%) :white_check_mark: |    1.00 (1%)  |
| `["gemm", "mul", "xf", "false", "32"]`                         | 0.93 (5%) :white_check_mark: |    1.00 (1%)  |
| `["gemm", "mul", "xf", "true", "256"]`                         | 0.95 (5%) :white_check_mark: |    1.00 (1%)  |
| `["gemm", "mul", "xf", "true", "8"]`                           | 0.86 (5%) :white_check_mark: |    1.00 (1%)  |
| `["missing_argmax", "rf"]`                                     | 0.93 (5%) :white_check_mark: |    1.00 (1%)  |
| `["missing_dot", "equiv"]`                                     |                1.15 (5%) :x: |    1.00 (1%)  |
| `["sum_transpose", "30", "withinit", "iter"]`                  | 0.84 (5%) :white_check_mark: |    1.00 (1%)  |
| `["sum_transpose", "30", "withinit", "xf"]`                    |                1.10 (5%) :x: |    1.00 (1%)  |
| `["teerf_filter", "noinit"]`                                   | 0.19 (5%) :white_check_mark: | 1.17 (1%) :x: |

## Benchmark Group List
Here's a list of all the benchmark groups executed by this job:

- `["append!!"]`
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
Julia Version 1.5.0
Commit 96786e22cc (2020-08-01 23:44 UTC)
Platform Info:
  OS: Linux (x86_64-pc-linux-gnu)
      Ubuntu 18.04.4 LTS
  uname: Linux 5.3.0-1034-azure #35~18.04.1-Ubuntu SMP Mon Jul 13 12:54:45 UTC 2020 x86_64 x86_64
  CPU: Intel(R) Xeon(R) Platinum 8171M CPU @ 2.60GHz: 
              speed         user         nice          sys         idle          irq
       #1  2095 MHz      71477 s          0 s       1471 s      12951 s          0 s
       #2  2095 MHz       5434 s          0 s       1578 s      79058 s          0 s
       
  Memory: 6.764881134033203 GB (2978.21484375 MB free)
  Uptime: 880.0 sec
  Load Avg:  1.052734375  1.04736328125  0.72900390625
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-9.0.1 (ORCJIT, skylake)
```

### Baseline
```
Julia Version 1.5.0
Commit 96786e22cc (2020-08-01 23:44 UTC)
Platform Info:
  OS: Linux (x86_64-pc-linux-gnu)
      Ubuntu 18.04.4 LTS
  uname: Linux 5.3.0-1034-azure #35~18.04.1-Ubuntu SMP Mon Jul 13 12:54:45 UTC 2020 x86_64 x86_64
  CPU: Intel(R) Xeon(R) Platinum 8171M CPU @ 2.60GHz: 
              speed         user         nice          sys         idle          irq
       #1  2095 MHz      76391 s          0 s       1636 s      37895 s          0 s
       #2  2095 MHz      30464 s          0 s       1757 s      83888 s          0 s
       
  Memory: 6.764881134033203 GB (2975.97265625 MB free)
  Uptime: 1182.0 sec
  Load Avg:  1.0810546875  1.04296875  0.8310546875
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-9.0.1 (ORCJIT, skylake)
```

---
# Target result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmark: 9 Aug 2020 - 21:34
* Package commit: 28b91b
* Julia commit: 96786e
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
| `["append!!", "eduction"]`                                     |  22.200 μs (5%) |         |  64.63 KiB (1%) |          13 |
| `["append!!", "xf"]`                                           |  21.700 μs (5%) |         |  64.63 KiB (1%) |          13 |
| `["cat", "base"]`                                              |   3.212 μs (5%) |         |                 |             |
| `["cat", "xf"]`                                                |   2.011 μs (5%) |         |                 |             |
| `["collect", "filter-missing"]`                                |  75.200 μs (5%) |         |  32.81 KiB (1%) |          14 |
| `["collect", "identity-float"]`                                |  28.600 μs (5%) |         | 256.66 KiB (1%) |          14 |
| `["collect", "identity-union"]`                                | 173.101 μs (5%) |         | 601.08 KiB (1%) |       10013 |
| `["dict", "base"]`                                             |   4.894 ms (5%) |         |  92.91 KiB (1%) |          22 |
| `["dict", "xf"]`                                               |   5.074 ms (5%) |         |  92.31 KiB (1%) |          18 |
| `["dot", "blas"]`                                              |   1.440 μs (5%) |         |                 |             |
| `["dot", "man"]`                                               |   1.420 μs (5%) |         |                 |             |
| `["dot", "rf"]`                                                |   2.556 μs (5%) |         |                 |             |
| `["dot", "xf"]`                                                |   2.644 μs (5%) |         |   64 bytes (1%) |           3 |
| `["filter_map_map!", "man"]`                                   |  66.400 μs (5%) |         |                 |             |
| `["filter_map_map!", "xf"]`                                    | 828.806 μs (5%) |         |   80 bytes (1%) |           3 |
| `["filter_map_reduce", "man"]`                                 | 275.902 μs (5%) |         |                 |             |
| `["filter_map_reduce", "xf"]`                                  | 276.002 μs (5%) |         |                 |             |
| `["filter_sum", "1000", "RandomFloats", "noinit", "base"]`     |   1.530 μs (5%) |         |                 |             |
| `["filter_sum", "1000", "RandomFloats", "noinit", "naive"]`    |   1.540 μs (5%) |         |                 |             |
| `["filter_sum", "1000", "RandomFloats", "noinit", "xf"]`       |   2.133 μs (5%) |         |                 |             |
| `["filter_sum", "1000", "RandomFloats", "withinit", "base"]`   |   2.133 μs (5%) |         |                 |             |
| `["filter_sum", "1000", "RandomFloats", "withinit", "naive"]`  |   1.200 μs (5%) |         |                 |             |
| `["filter_sum", "1000", "RandomFloats", "withinit", "xf"]`     |   2.133 μs (5%) |         |                 |             |
| `["filter_sum", "1000", "UnitRange", "noinit", "base"]`        |   2.178 μs (5%) |         |                 |             |
| `["filter_sum", "1000", "UnitRange", "noinit", "naive"]`       |   1.610 μs (5%) |         |                 |             |
| `["filter_sum", "1000", "UnitRange", "noinit", "xf"]`          | 145.532 ns (5%) |         |                 |             |
| `["filter_sum", "1000", "UnitRange", "withinit", "base"]`      | 124.557 ns (5%) |         |                 |             |
| `["filter_sum", "1000", "UnitRange", "withinit", "naive"]`     |   1.010 μs (5%) |         |                 |             |
| `["filter_sum", "1000", "UnitRange", "withinit", "xf"]`        | 144.971 ns (5%) |         |                 |             |
| `["filter_sum", "10000", "RandomFloats", "noinit", "base"]`    |  50.600 μs (5%) |         |                 |             |
| `["filter_sum", "10000", "RandomFloats", "noinit", "naive"]`   |  55.201 μs (5%) |         |                 |             |
| `["filter_sum", "10000", "RandomFloats", "noinit", "xf"]`      |  21.600 μs (5%) |         |                 |             |
| `["filter_sum", "10000", "RandomFloats", "withinit", "base"]`  |  21.000 μs (5%) |         |                 |             |
| `["filter_sum", "10000", "RandomFloats", "withinit", "naive"]` |  52.500 μs (5%) |         |                 |             |
| `["filter_sum", "10000", "RandomFloats", "withinit", "xf"]`    |  21.600 μs (5%) |         |                 |             |
| `["filter_sum", "10000", "UnitRange", "noinit", "base"]`       |  21.100 μs (5%) |         |                 |             |
| `["filter_sum", "10000", "UnitRange", "noinit", "naive"]`      |  16.001 μs (5%) |         |                 |             |
| `["filter_sum", "10000", "UnitRange", "noinit", "xf"]`         |   1.390 μs (5%) |         |                 |             |
| `["filter_sum", "10000", "UnitRange", "withinit", "base"]`     |   1.200 μs (5%) |         |                 |             |
| `["filter_sum", "10000", "UnitRange", "withinit", "naive"]`    |  10.000 μs (5%) |         |                 |             |
| `["filter_sum", "10000", "UnitRange", "withinit", "xf"]`       |   1.400 μs (5%) |         |                 |             |
| `["findall", "base"]`                                          | 986.409 μs (5%) |         |   2.00 MiB (1%) |          18 |
| `["findall", "xf-array"]`                                      | 894.607 μs (5%) |         |   3.02 MiB (1%) |       98829 |
| `["findall", "xf-iter"]`                                       | 409.503 μs (5%) |         |   2.00 MiB (1%) |          19 |
| `["gemm", "fusedmul", "blas", "16"]`                           |   4.039 ms (5%) |         |                 |             |
| `["gemm", "fusedmul", "blas", "2"]`                            |   3.359 ms (5%) |         |                 |             |
| `["gemm", "fusedmul", "blas", "32"]`                           |   6.003 ms (5%) |         |                 |             |
| `["gemm", "fusedmul", "blas", "8"]`                            |   3.232 ms (5%) |         |                 |             |
| `["gemm", "fusedmul", "xf", "16"]`                             |   4.242 ms (5%) |         |  192 bytes (1%) |           4 |
| `["gemm", "fusedmul", "xf", "2"]`                              | 632.304 μs (5%) |         |  192 bytes (1%) |           4 |
| `["gemm", "fusedmul", "xf", "32"]`                             |   9.298 ms (5%) |         |  192 bytes (1%) |           4 |
| `["gemm", "fusedmul", "xf", "8"]`                              |   2.096 ms (5%) |         |  192 bytes (1%) |           4 |
| `["gemm", "mul", "linalg", "256"]`                             | 547.605 μs (5%) |         |                 |             |
| `["gemm", "mul", "linalg", "32"]`                              |   2.211 μs (5%) |         |                 |             |
| `["gemm", "mul", "linalg", "8"]`                               | 241.778 ns (5%) |         |                 |             |
| `["gemm", "mul", "man", "false", "256"]`                       |   1.896 ms (5%) |         |                 |             |
| `["gemm", "mul", "man", "false", "32"]`                        |   6.240 μs (5%) |         |                 |             |
| `["gemm", "mul", "man", "false", "8"]`                         | 599.438 ns (5%) |         |                 |             |
| `["gemm", "mul", "man", "ivdep", "256"]`                       |   1.921 ms (5%) |         |                 |             |
| `["gemm", "mul", "man", "ivdep", "32"]`                        |   4.400 μs (5%) |         |                 |             |
| `["gemm", "mul", "man", "ivdep", "8"]`                         | 432.663 ns (5%) |         |                 |             |
| `["gemm", "mul", "man", "true", "256"]`                        |   1.918 ms (5%) |         |                 |             |
| `["gemm", "mul", "man", "true", "32"]`                         |   5.583 μs (5%) |         |                 |             |
| `["gemm", "mul", "man", "true", "8"]`                          | 456.345 ns (5%) |         |                 |             |
| `["gemm", "mul", "xf", "false", "256"]`                        |   1.896 ms (5%) |         |   80 bytes (1%) |           3 |
| `["gemm", "mul", "xf", "false", "32"]`                         |   5.567 μs (5%) |         |   80 bytes (1%) |           3 |
| `["gemm", "mul", "xf", "false", "8"]`                          | 519.377 ns (5%) |         |   80 bytes (1%) |           3 |
| `["gemm", "mul", "xf", "ivdep", "256"]`                        |   1.946 ms (5%) |         |   80 bytes (1%) |           3 |
| `["gemm", "mul", "xf", "ivdep", "32"]`                         |   4.443 μs (5%) |         |   80 bytes (1%) |           3 |
| `["gemm", "mul", "xf", "ivdep", "8"]`                          | 488.149 ns (5%) |         |   80 bytes (1%) |           3 |
| `["gemm", "mul", "xf", "true", "256"]`                         |   1.905 ms (5%) |         |   80 bytes (1%) |           3 |
| `["gemm", "mul", "xf", "true", "32"]`                          |   5.667 μs (5%) |         |   80 bytes (1%) |           3 |
| `["gemm", "mul", "xf", "true", "8"]`                           | 517.193 ns (5%) |         |   80 bytes (1%) |           3 |
| `["groupby", "sum", "sac"]`                                    | 249.602 μs (5%) |         |  624 bytes (1%) |           5 |
| `["groupby", "sum", "xf-with-init"]`                           | 202.602 μs (5%) |         |   1.20 KiB (1%) |           9 |
| `["groupby", "sum", "xf-without-init"]`                        | 201.302 μs (5%) |         |   1.20 KiB (1%) |           9 |
| `["mapcat_eduction", "base"]`                                  |   2.311 μs (5%) |         |                 |             |
| `["mapcat_eduction", "xf-eduction"]`                           |   2.056 μs (5%) |         |                 |             |
| `["mapcat_eduction", "xf-xf"]`                                 |   2.011 μs (5%) |         |                 |             |
| `["missing_argmax", "man"]`                                    |   3.225 μs (5%) |         |   32 bytes (1%) |           1 |
| `["missing_argmax", "rf"]`                                     |   2.089 μs (5%) |         |   32 bytes (1%) |           1 |
| `["missing_argmax", "xf"]`                                     |   2.140 μs (5%) |         |   32 bytes (1%) |           1 |
| `["missing_dot", "equiv"]`                                     |   2.256 μs (5%) |         |   16 bytes (1%) |           1 |
| `["missing_dot", "man"]`                                       |   1.660 μs (5%) |         |   16 bytes (1%) |           1 |
| `["missing_dot", "naive"]`                                     |   5.817 μs (5%) |         |   16 bytes (1%) |           1 |
| `["missing_dot", "rf"]`                                        |   1.660 μs (5%) |         |   16 bytes (1%) |           1 |
| `["missing_dot", "rf_nota"]`                                   |   1.650 μs (5%) |         |   16 bytes (1%) |           1 |
| `["missing_dot", "xf"]`                                        | 116.901 μs (5%) |         |  72.16 KiB (1%) |        3743 |
| `["missing_dot", "xf_nota"]`                                   | 117.701 μs (5%) |         |  72.20 KiB (1%) |        3744 |
| `["overhead", "foldl"]`                                        |   5.600 ns (5%) |         |                 |             |
| `["overhead", "reduce_basecase"]`                              | 300.004 ns (5%) |         |  368 bytes (1%) |           6 |
| `["partition_by", "man"]`                                      |   2.568 ms (5%) |         |  352 bytes (1%) |           4 |
| `["partition_by", "xf"]`                                       |   2.551 ms (5%) |         |  544 bytes (1%) |           6 |
| `["set", "base"]`                                              |   5.721 ms (5%) |         |  49.56 KiB (1%) |          17 |
| `["set", "xf"]`                                                |   5.550 ms (5%) |         |  49.59 KiB (1%) |          19 |
| `["sum_transpose", "30", "noinit", "iter"]`                    |   2.711 μs (5%) |         |                 |             |
| `["sum_transpose", "30", "noinit", "man"]`                     |   3.063 μs (5%) |         |                 |             |
| `["sum_transpose", "30", "noinit", "xf"]`                      |   3.625 μs (5%) |         |                 |             |
| `["sum_transpose", "30", "withinit", "iter"]`                  |   1.830 μs (5%) |         |                 |             |
| `["sum_transpose", "30", "withinit", "man"]`                   |   1.380 μs (5%) |         |                 |             |
| `["sum_transpose", "30", "withinit", "xf"]`                    |   3.975 μs (5%) |         |                 |             |
| `["teerf_filter", "noinit"]`                                   | 483.595 ns (5%) |         |  112 bytes (1%) |           4 |
| `["teerf_filter", "withinit"]`                                 | 243.088 ns (5%) |         |                 |             |

## Benchmark Group List
Here's a list of all the benchmark groups executed by this job:

- `["append!!"]`
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
Julia Version 1.5.0
Commit 96786e22cc (2020-08-01 23:44 UTC)
Platform Info:
  OS: Linux (x86_64-pc-linux-gnu)
      Ubuntu 18.04.4 LTS
  uname: Linux 5.3.0-1034-azure #35~18.04.1-Ubuntu SMP Mon Jul 13 12:54:45 UTC 2020 x86_64 x86_64
  CPU: Intel(R) Xeon(R) Platinum 8171M CPU @ 2.60GHz: 
              speed         user         nice          sys         idle          irq
       #1  2095 MHz      71477 s          0 s       1471 s      12951 s          0 s
       #2  2095 MHz       5434 s          0 s       1578 s      79058 s          0 s
       
  Memory: 6.764881134033203 GB (2978.21484375 MB free)
  Uptime: 880.0 sec
  Load Avg:  1.052734375  1.04736328125  0.72900390625
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-9.0.1 (ORCJIT, skylake)
```

---
# Baseline result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmark: 9 Aug 2020 - 21:39
* Package commit: 6d7f6f
* Julia commit: 96786e
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
| `["append!!", "eduction"]`                                     |  21.801 μs (5%) |         |  64.63 KiB (1%) |          13 |
| `["append!!", "xf"]`                                           |  21.501 μs (5%) |         |  64.63 KiB (1%) |          13 |
| `["cat", "base"]`                                              |   2.225 μs (5%) |         |                 |             |
| `["cat", "xf"]`                                                |   2.022 μs (5%) |         |                 |             |
| `["collect", "filter-missing"]`                                |  76.500 μs (5%) |         |  32.81 KiB (1%) |          14 |
| `["collect", "identity-float"]`                                |  31.901 μs (5%) |         | 256.66 KiB (1%) |          14 |
| `["collect", "identity-union"]`                                | 173.401 μs (5%) |         | 601.04 KiB (1%) |       10013 |
| `["dict", "base"]`                                             |   4.892 ms (5%) |         |  92.91 KiB (1%) |          22 |
| `["dict", "xf"]`                                               |   5.079 ms (5%) |         |  92.31 KiB (1%) |          18 |
| `["dot", "blas"]`                                              |   1.420 μs (5%) |         |                 |             |
| `["dot", "man"]`                                               |   1.430 μs (5%) |         |                 |             |
| `["dot", "rf"]`                                                |   2.567 μs (5%) |         |                 |             |
| `["dot", "xf"]`                                                |   2.656 μs (5%) |         |   64 bytes (1%) |           3 |
| `["filter_map_map!", "man"]`                                   |  57.500 μs (5%) |         |                 |             |
| `["filter_map_map!", "xf"]`                                    | 829.010 μs (5%) |         |   80 bytes (1%) |           3 |
| `["filter_map_reduce", "man"]`                                 | 275.904 μs (5%) |         |                 |             |
| `["filter_map_reduce", "xf"]`                                  | 275.903 μs (5%) |         |                 |             |
| `["filter_sum", "1000", "RandomFloats", "noinit", "base"]`     |   1.530 μs (5%) |         |                 |             |
| `["filter_sum", "1000", "RandomFloats", "noinit", "naive"]`    |   1.540 μs (5%) |         |                 |             |
| `["filter_sum", "1000", "RandomFloats", "noinit", "xf"]`       |   2.133 μs (5%) |         |                 |             |
| `["filter_sum", "1000", "RandomFloats", "withinit", "base"]`   |   2.133 μs (5%) |         |                 |             |
| `["filter_sum", "1000", "RandomFloats", "withinit", "naive"]`  |   1.240 μs (5%) |         |                 |             |
| `["filter_sum", "1000", "RandomFloats", "withinit", "xf"]`     |   2.133 μs (5%) |         |                 |             |
| `["filter_sum", "1000", "UnitRange", "noinit", "base"]`        |   2.167 μs (5%) |         |                 |             |
| `["filter_sum", "1000", "UnitRange", "noinit", "naive"]`       |   1.420 μs (5%) |         |                 |             |
| `["filter_sum", "1000", "UnitRange", "noinit", "xf"]`          | 145.651 ns (5%) |         |                 |             |
| `["filter_sum", "1000", "UnitRange", "withinit", "base"]`      | 126.223 ns (5%) |         |                 |             |
| `["filter_sum", "1000", "UnitRange", "withinit", "naive"]`     |   1.110 μs (5%) |         |                 |             |
| `["filter_sum", "1000", "UnitRange", "withinit", "xf"]`        | 152.242 ns (5%) |         |                 |             |
| `["filter_sum", "10000", "RandomFloats", "noinit", "base"]`    |  50.601 μs (5%) |         |                 |             |
| `["filter_sum", "10000", "RandomFloats", "noinit", "naive"]`   |  64.000 μs (5%) |         |                 |             |
| `["filter_sum", "10000", "RandomFloats", "noinit", "xf"]`      |  21.700 μs (5%) |         |                 |             |
| `["filter_sum", "10000", "RandomFloats", "withinit", "base"]`  |  21.700 μs (5%) |         |                 |             |
| `["filter_sum", "10000", "RandomFloats", "withinit", "naive"]` |  52.400 μs (5%) |         |                 |             |
| `["filter_sum", "10000", "RandomFloats", "withinit", "xf"]`    |  21.200 μs (5%) |         |                 |             |
| `["filter_sum", "10000", "UnitRange", "noinit", "base"]`       |  21.200 μs (5%) |         |                 |             |
| `["filter_sum", "10000", "UnitRange", "noinit", "naive"]`      |  14.000 μs (5%) |         |                 |             |
| `["filter_sum", "10000", "UnitRange", "noinit", "xf"]`         |   1.400 μs (5%) |         |                 |             |
| `["filter_sum", "10000", "UnitRange", "withinit", "base"]`     |   1.200 μs (5%) |         |                 |             |
| `["filter_sum", "10000", "UnitRange", "withinit", "naive"]`    |  11.000 μs (5%) |         |                 |             |
| `["filter_sum", "10000", "UnitRange", "withinit", "xf"]`       |   1.400 μs (5%) |         |                 |             |
| `["findall", "base"]`                                          | 975.107 μs (5%) |         |   2.00 MiB (1%) |          18 |
| `["findall", "xf-array"]`                                      | 896.213 μs (5%) |         |   3.02 MiB (1%) |       98829 |
| `["findall", "xf-iter"]`                                       | 403.006 μs (5%) |         |   2.00 MiB (1%) |          19 |
| `["gemm", "fusedmul", "blas", "16"]`                           |   4.057 ms (5%) |         |                 |             |
| `["gemm", "fusedmul", "blas", "2"]`                            |   3.418 ms (5%) |         |                 |             |
| `["gemm", "fusedmul", "blas", "32"]`                           |   5.676 ms (5%) |         |                 |             |
| `["gemm", "fusedmul", "blas", "8"]`                            |   4.166 ms (5%) |         |                 |             |
| `["gemm", "fusedmul", "xf", "16"]`                             |   4.799 ms (5%) |         |  192 bytes (1%) |           4 |
| `["gemm", "fusedmul", "xf", "2"]`                              | 560.107 μs (5%) |         |  192 bytes (1%) |           4 |
| `["gemm", "fusedmul", "xf", "32"]`                             |  10.118 ms (5%) |         |  192 bytes (1%) |           4 |
| `["gemm", "fusedmul", "xf", "8"]`                              |   2.294 ms (5%) |         |  192 bytes (1%) |           4 |
| `["gemm", "mul", "linalg", "256"]`                             | 551.707 μs (5%) |         |                 |             |
| `["gemm", "mul", "linalg", "32"]`                              |   2.200 μs (5%) |         |                 |             |
| `["gemm", "mul", "linalg", "8"]`                               | 200.000 ns (5%) |         |                 |             |
| `["gemm", "mul", "man", "false", "256"]`                       |   2.023 ms (5%) |         |                 |             |
| `["gemm", "mul", "man", "false", "32"]`                        |   6.100 μs (5%) |         |                 |             |
| `["gemm", "mul", "man", "false", "8"]`                         | 500.000 ns (5%) |         |                 |             |
| `["gemm", "mul", "man", "ivdep", "256"]`                       |   2.005 ms (5%) |         |                 |             |
| `["gemm", "mul", "man", "ivdep", "32"]`                        |   4.400 μs (5%) |         |                 |             |
| `["gemm", "mul", "man", "ivdep", "8"]`                         | 400.000 ns (5%) |         |                 |             |
| `["gemm", "mul", "man", "true", "256"]`                        |   2.020 ms (5%) |         |                 |             |
| `["gemm", "mul", "man", "true", "32"]`                         |   5.800 μs (5%) |         |                 |             |
| `["gemm", "mul", "man", "true", "8"]`                          | 400.000 ns (5%) |         |                 |             |
| `["gemm", "mul", "xf", "false", "256"]`                        |   2.017 ms (5%) |         |   80 bytes (1%) |           3 |
| `["gemm", "mul", "xf", "false", "32"]`                         |   6.000 μs (5%) |         |   80 bytes (1%) |           3 |
| `["gemm", "mul", "xf", "false", "8"]`                          | 500.000 ns (5%) |         |   80 bytes (1%) |           3 |
| `["gemm", "mul", "xf", "ivdep", "256"]`                        |   2.006 ms (5%) |         |   80 bytes (1%) |           3 |
| `["gemm", "mul", "xf", "ivdep", "32"]`                         |   4.400 μs (5%) |         |   80 bytes (1%) |           3 |
| `["gemm", "mul", "xf", "ivdep", "8"]`                          | 500.000 ns (5%) |         |   80 bytes (1%) |           3 |
| `["gemm", "mul", "xf", "true", "256"]`                         |   2.009 ms (5%) |         |   80 bytes (1%) |           3 |
| `["gemm", "mul", "xf", "true", "32"]`                          |   5.900 μs (5%) |         |   80 bytes (1%) |           3 |
| `["gemm", "mul", "xf", "true", "8"]`                           | 600.000 ns (5%) |         |   80 bytes (1%) |           3 |
| `["groupby", "sum", "sac"]`                                    | 245.103 μs (5%) |         |  624 bytes (1%) |           5 |
| `["groupby", "sum", "xf-with-init"]`                           | 207.302 μs (5%) |         |   1.20 KiB (1%) |           9 |
| `["groupby", "sum", "xf-without-init"]`                        | 200.802 μs (5%) |         |   1.20 KiB (1%) |           9 |
| `["mapcat_eduction", "base"]`                                  |   2.267 μs (5%) |         |                 |             |
| `["mapcat_eduction", "xf-eduction"]`                           |   2.011 μs (5%) |         |                 |             |
| `["mapcat_eduction", "xf-xf"]`                                 |   2.011 μs (5%) |         |                 |             |
| `["missing_argmax", "man"]`                                    |   3.225 μs (5%) |         |   32 bytes (1%) |           1 |
| `["missing_argmax", "rf"]`                                     |   2.256 μs (5%) |         |   32 bytes (1%) |           1 |
| `["missing_argmax", "xf"]`                                     |   2.230 μs (5%) |         |   32 bytes (1%) |           1 |
| `["missing_dot", "equiv"]`                                     |   1.956 μs (5%) |         |   16 bytes (1%) |           1 |
| `["missing_dot", "man"]`                                       |   1.640 μs (5%) |         |   16 bytes (1%) |           1 |
| `["missing_dot", "naive"]`                                     |   5.817 μs (5%) |         |   16 bytes (1%) |           1 |
| `["missing_dot", "rf"]`                                        |   1.660 μs (5%) |         |   16 bytes (1%) |           1 |
| `["missing_dot", "rf_nota"]`                                   |   1.650 μs (5%) |         |   16 bytes (1%) |           1 |
| `["missing_dot", "xf"]`                                        | 117.002 μs (5%) |         |  72.30 KiB (1%) |        3750 |
| `["missing_dot", "xf_nota"]`                                   | 118.001 μs (5%) |         |  71.80 KiB (1%) |        3728 |
| `["overhead", "foldl"]`                                        |   5.600 ns (5%) |         |                 |             |
| `["overhead", "reduce_basecase"]`                              | 300.398 ns (5%) |         |  368 bytes (1%) |           6 |
| `["partition_by", "man"]`                                      |   2.666 ms (5%) |         |  352 bytes (1%) |           4 |
| `["partition_by", "xf"]`                                       |   2.654 ms (5%) |         |  544 bytes (1%) |           6 |
| `["set", "base"]`                                              |   5.674 ms (5%) |         |  49.56 KiB (1%) |          17 |
| `["set", "xf"]`                                                |   5.579 ms (5%) |         |  49.59 KiB (1%) |          19 |
| `["sum_transpose", "30", "noinit", "iter"]`                    |   2.711 μs (5%) |         |                 |             |
| `["sum_transpose", "30", "noinit", "man"]`                     |   3.063 μs (5%) |         |                 |             |
| `["sum_transpose", "30", "noinit", "xf"]`                      |   3.625 μs (5%) |         |                 |             |
| `["sum_transpose", "30", "withinit", "iter"]`                  |   2.170 μs (5%) |         |                 |             |
| `["sum_transpose", "30", "withinit", "man"]`                   |   1.380 μs (5%) |         |                 |             |
| `["sum_transpose", "30", "withinit", "xf"]`                    |   3.625 μs (5%) |         |                 |             |
| `["teerf_filter", "noinit"]`                                   |   2.498 μs (5%) |         |   96 bytes (1%) |           5 |
| `["teerf_filter", "withinit"]`                                 | 233.643 ns (5%) |         |                 |             |

## Benchmark Group List
Here's a list of all the benchmark groups executed by this job:

- `["append!!"]`
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
Julia Version 1.5.0
Commit 96786e22cc (2020-08-01 23:44 UTC)
Platform Info:
  OS: Linux (x86_64-pc-linux-gnu)
      Ubuntu 18.04.4 LTS
  uname: Linux 5.3.0-1034-azure #35~18.04.1-Ubuntu SMP Mon Jul 13 12:54:45 UTC 2020 x86_64 x86_64
  CPU: Intel(R) Xeon(R) Platinum 8171M CPU @ 2.60GHz: 
              speed         user         nice          sys         idle          irq
       #1  2095 MHz      76391 s          0 s       1636 s      37895 s          0 s
       #2  2095 MHz      30464 s          0 s       1757 s      83888 s          0 s
       
  Memory: 6.764881134033203 GB (2975.97265625 MB free)
  Uptime: 1182.0 sec
  Load Avg:  1.0810546875  1.04296875  0.8310546875
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-9.0.1 (ORCJIT, skylake)
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
    Model:               85
    Model name:          Intel(R) Xeon(R) Platinum 8171M CPU @ 2.60GHz
    Stepping:            4
    CPU MHz:             2095.077
    BogoMIPS:            4190.15
    Hypervisor vendor:   Microsoft
    Virtualization type: full
    L1d cache:           32K
    L1i cache:           32K
    L2 cache:            1024K
    L3 cache:            36608K
    NUMA node0 CPU(s):   0,1
    Flags:               fpu vme de pse tsc msr pae mce cx8 apic sep mtrr pge mca cmov pat pse36 clflush mmx fxsr sse sse2 ss ht syscall nx pdpe1gb rdtscp lm constant_tsc rep_good nopl xtopology cpuid pni pclmulqdq ssse3 fma cx16 pcid sse4_1 sse4_2 movbe popcnt aes xsave avx f16c rdrand hypervisor lahf_lm abm 3dnowprefetch invpcid_single pti fsgsbase bmi1 hle avx2 smep bmi2 erms invpcid rtm mpx avx512f avx512dq rdseed adx smap clflushopt avx512cd avx512bw avx512vl xsaveopt xsavec xsaves md_clear
    

| Cpu Property       | Value                                                   |
|:------------------ |:------------------------------------------------------- |
| Brand              | Intel(R) Xeon(R) Platinum 8171M CPU @ 2.60GHz           |
| Vendor             | :Intel                                                  |
| Architecture       | :Skylake                                                |
| Model              | Family: 0x06, Model: 0x55, Stepping: 0x04, Type: 0x00   |
| Cores              | 2 physical cores, 2 logical cores (on executing CPU)    |
|                    | No Hyperthreading detected                              |
| Clock Frequencies  | Not supported by CPU                                    |
| Data Cache         | Level 1:3 : (32, 1024, 36608) kbytes                    |
|                    | 64 byte cache line size                                 |
| Address Size       | 48 bits virtual, 44 bits physical                       |
| SIMD               | 512 bit = 64 byte max. SIMD vector size                 |
| Time Stamp Counter | TSC is accessible via `rdtsc`                           |
|                    | TSC increased at every clock cycle (non-invariant TSC)  |
| Perf. Monitoring   | Performance Monitoring Counters (PMC) are not supported |
| Hypervisor         | Yes, Microsoft                                          |

