# Benchmark result

* Pull request commit: [`d8d240018f170046a9e768cbd3209a15b3ecdee0`](https://github.com/JuliaFolds/Transducers.jl/commit/d8d240018f170046a9e768cbd3209a15b3ecdee0)
* Pull request: <https://github.com/JuliaFolds/Transducers.jl/pull/409> (Switch to Julia 1.5 as the main version in CIs)

# Judge result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmarks:
    - Target: 9 Aug 2020 - 20:43
    - Baseline: 9 Aug 2020 - 20:47
* Package commits:
    - Target: 34d0fb
    - Baseline: b8efee
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

| ID                                                             | time ratio                   | memory ratio |
|----------------------------------------------------------------|------------------------------|--------------|
| `["append!!", "xf"]`                                           |                1.06 (5%) :x: |   1.00 (1%)  |
| `["collect", "filter-missing"]`                                |                1.05 (5%) :x: |   1.00 (1%)  |
| `["collect", "identity-float"]`                                |                1.17 (5%) :x: |   1.00 (1%)  |
| `["filter_map_map!", "man"]`                                   |                1.16 (5%) :x: |   1.00 (1%)  |
| `["filter_sum", "1000", "RandomFloats", "withinit", "naive"]`  |                1.19 (5%) :x: |   1.00 (1%)  |
| `["filter_sum", "10000", "RandomFloats", "noinit", "base"]`    |                1.06 (5%) :x: |   1.00 (1%)  |
| `["gemm", "fusedmul", "xf", "32"]`                             |                1.07 (5%) :x: |   1.00 (1%)  |
| `["gemm", "fusedmul", "xf", "8"]`                              | 0.93 (5%) :white_check_mark: |   1.00 (1%)  |
| `["gemm", "mul", "linalg", "32"]`                              | 0.86 (5%) :white_check_mark: |   1.00 (1%)  |
| `["gemm", "mul", "linalg", "8"]`                               |                1.80 (5%) :x: |   1.00 (1%)  |
| `["gemm", "mul", "man", "false", "8"]`                         |                1.09 (5%) :x: |   1.00 (1%)  |
| `["gemm", "mul", "xf", "false", "8"]`                          |                1.19 (5%) :x: |   1.00 (1%)  |
| `["gemm", "mul", "xf", "ivdep", "8"]`                          |                1.12 (5%) :x: |   1.00 (1%)  |
| `["gemm", "mul", "xf", "true", "8"]`                           |                1.18 (5%) :x: |   1.00 (1%)  |
| `["missing_argmax", "xf"]`                                     |                1.11 (5%) :x: |   1.00 (1%)  |
| `["sum_transpose", "30", "withinit", "xf"]`                    |                1.10 (5%) :x: |   1.00 (1%)  |

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
       #1  2095 MHz       6866 s          0 s       1222 s      86545 s          0 s
       #2  2095 MHz      61492 s          0 s       1569 s      31374 s          0 s
       
  Memory: 6.764881134033203 GB (2887.59375 MB free)
  Uptime: 964.0 sec
  Load Avg:  1.04248046875  0.9853515625  0.62109375
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
       #1  2095 MHz       6981 s          0 s       1279 s     112231 s          0 s
       #2  2095 MHz      87090 s          0 s       1806 s      31409 s          0 s
       
  Memory: 6.764881134033203 GB (2988.125 MB free)
  Uptime: 1224.0 sec
  Load Avg:  1.09326171875  1.03759765625  0.744140625
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-9.0.1 (ORCJIT, skylake)
```

---
# Target result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmark: 9 Aug 2020 - 20:43
* Package commit: 34d0fb
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
| `["append!!", "eduction"]`                                     |  15.200 μs (5%) |         |  64.63 KiB (1%) |          13 |
| `["append!!", "xf"]`                                           |  15.400 μs (5%) |         |  64.63 KiB (1%) |          13 |
| `["cat", "base"]`                                              |   1.550 μs (5%) |         |                 |             |
| `["cat", "xf"]`                                                |   1.400 μs (5%) |         |                 |             |
| `["collect", "filter-missing"]`                                |  50.202 μs (5%) |         |  32.81 KiB (1%) |          14 |
| `["collect", "identity-float"]`                                |  21.500 μs (5%) |         | 256.66 KiB (1%) |          14 |
| `["collect", "identity-union"]`                                | 122.605 μs (5%) |         | 601.04 KiB (1%) |       10013 |
| `["dict", "base"]`                                             |   3.391 ms (5%) |         |  92.91 KiB (1%) |          22 |
| `["dict", "xf"]`                                               |   3.514 ms (5%) |         |  92.31 KiB (1%) |          18 |
| `["dot", "blas"]`                                              |   1.000 μs (5%) |         |                 |             |
| `["dot", "man"]`                                               | 958.417 ns (5%) |         |                 |             |
| `["dot", "rf"]`                                                |   1.770 μs (5%) |         |                 |             |
| `["dot", "xf"]`                                                |   1.840 μs (5%) |         |   64 bytes (1%) |           3 |
| `["filter_map_map!", "man"]`                                   |  62.202 μs (5%) |         |                 |             |
| `["filter_map_map!", "xf"]`                                    | 580.521 μs (5%) |         |   80 bytes (1%) |           3 |
| `["filter_map_reduce", "man"]`                                 | 191.507 μs (5%) |         |                 |             |
| `["filter_map_reduce", "xf"]`                                  | 191.607 μs (5%) |         |                 |             |
| `["filter_sum", "1000", "RandomFloats", "noinit", "base"]`     |   1.060 μs (5%) |         |                 |             |
| `["filter_sum", "1000", "RandomFloats", "noinit", "naive"]`    |   1.070 μs (5%) |         |                 |             |
| `["filter_sum", "1000", "RandomFloats", "noinit", "xf"]`       |   1.480 μs (5%) |         |                 |             |
| `["filter_sum", "1000", "RandomFloats", "withinit", "base"]`   |   1.480 μs (5%) |         |                 |             |
| `["filter_sum", "1000", "RandomFloats", "withinit", "naive"]`  | 826.500 ns (5%) |         |                 |             |
| `["filter_sum", "1000", "RandomFloats", "withinit", "xf"]`     |   1.480 μs (5%) |         |                 |             |
| `["filter_sum", "1000", "UnitRange", "noinit", "base"]`        |   1.510 μs (5%) |         |                 |             |
| `["filter_sum", "1000", "UnitRange", "noinit", "naive"]`       | 706.234 ns (5%) |         |                 |             |
| `["filter_sum", "1000", "UnitRange", "noinit", "xf"]`          | 100.957 ns (5%) |         |                 |             |
| `["filter_sum", "1000", "UnitRange", "withinit", "base"]`      |  87.816 ns (5%) |         |                 |             |
| `["filter_sum", "1000", "UnitRange", "withinit", "naive"]`     | 669.452 ns (5%) |         |                 |             |
| `["filter_sum", "1000", "UnitRange", "withinit", "xf"]`        | 100.003 ns (5%) |         |                 |             |
| `["filter_sum", "10000", "RandomFloats", "noinit", "base"]`    |  35.201 μs (5%) |         |                 |             |
| `["filter_sum", "10000", "RandomFloats", "noinit", "naive"]`   |  38.302 μs (5%) |         |                 |             |
| `["filter_sum", "10000", "RandomFloats", "noinit", "xf"]`      |  15.000 μs (5%) |         |                 |             |
| `["filter_sum", "10000", "RandomFloats", "withinit", "base"]`  |  14.700 μs (5%) |         |                 |             |
| `["filter_sum", "10000", "RandomFloats", "withinit", "naive"]` |  36.502 μs (5%) |         |                 |             |
| `["filter_sum", "10000", "RandomFloats", "withinit", "xf"]`    |  15.000 μs (5%) |         |                 |             |
| `["filter_sum", "10000", "UnitRange", "noinit", "base"]`       |  14.701 μs (5%) |         |                 |             |
| `["filter_sum", "10000", "UnitRange", "noinit", "naive"]`      |   6.980 μs (5%) |         |                 |             |
| `["filter_sum", "10000", "UnitRange", "noinit", "xf"]`         | 966.667 ns (5%) |         |                 |             |
| `["filter_sum", "10000", "UnitRange", "withinit", "base"]`     | 829.513 ns (5%) |         |                 |             |
| `["filter_sum", "10000", "UnitRange", "withinit", "naive"]`    |   6.620 μs (5%) |         |                 |             |
| `["filter_sum", "10000", "UnitRange", "withinit", "xf"]`       | 966.667 ns (5%) |         |                 |             |
| `["findall", "base"]`                                          | 685.226 μs (5%) |         |   2.00 MiB (1%) |          18 |
| `["findall", "xf-array"]`                                      | 594.123 μs (5%) |         |   3.02 MiB (1%) |       98829 |
| `["findall", "xf-iter"]`                                       | 253.610 μs (5%) |         |   2.00 MiB (1%) |          19 |
| `["gemm", "fusedmul", "blas", "16"]`                           |   2.879 ms (5%) |         |                 |             |
| `["gemm", "fusedmul", "blas", "2"]`                            |   2.400 ms (5%) |         |                 |             |
| `["gemm", "fusedmul", "blas", "32"]`                           |   3.523 ms (5%) |         |                 |             |
| `["gemm", "fusedmul", "blas", "8"]`                            |   2.563 ms (5%) |         |                 |             |
| `["gemm", "fusedmul", "xf", "16"]`                             |   5.027 ms (5%) |         |  192 bytes (1%) |           4 |
| `["gemm", "fusedmul", "xf", "2"]`                              | 577.520 μs (5%) |         |  192 bytes (1%) |           4 |
| `["gemm", "fusedmul", "xf", "32"]`                             |   9.411 ms (5%) |         |  192 bytes (1%) |           4 |
| `["gemm", "fusedmul", "xf", "8"]`                              |   2.088 ms (5%) |         |  192 bytes (1%) |           4 |
| `["gemm", "mul", "linalg", "256"]`                             | 396.015 μs (5%) |         |                 |             |
| `["gemm", "mul", "linalg", "32"]`                              |   1.540 μs (5%) |         |                 |             |
| `["gemm", "mul", "linalg", "8"]`                               | 180.197 ns (5%) |         |                 |             |
| `["gemm", "mul", "man", "false", "256"]`                       |   1.448 ms (5%) |         |                 |             |
| `["gemm", "mul", "man", "false", "32"]`                        |   4.043 μs (5%) |         |                 |             |
| `["gemm", "mul", "man", "false", "8"]`                         | 325.791 ns (5%) |         |                 |             |
| `["gemm", "mul", "man", "ivdep", "256"]`                       |   1.404 ms (5%) |         |                 |             |
| `["gemm", "mul", "man", "ivdep", "32"]`                        |   3.138 μs (5%) |         |                 |             |
| `["gemm", "mul", "man", "ivdep", "8"]`                         | 298.845 ns (5%) |         |                 |             |
| `["gemm", "mul", "man", "true", "256"]`                        |   1.437 ms (5%) |         |                 |             |
| `["gemm", "mul", "man", "true", "32"]`                         |   3.938 μs (5%) |         |                 |             |
| `["gemm", "mul", "man", "true", "8"]`                          | 392.089 ns (5%) |         |                 |             |
| `["gemm", "mul", "xf", "false", "256"]`                        |   1.454 ms (5%) |         |   80 bytes (1%) |           3 |
| `["gemm", "mul", "xf", "false", "32"]`                         |   3.850 μs (5%) |         |   80 bytes (1%) |           3 |
| `["gemm", "mul", "xf", "false", "8"]`                          | 357.014 ns (5%) |         |   80 bytes (1%) |           3 |
| `["gemm", "mul", "xf", "ivdep", "256"]`                        |   1.403 ms (5%) |         |   80 bytes (1%) |           3 |
| `["gemm", "mul", "xf", "ivdep", "32"]`                         |   3.288 μs (5%) |         |   80 bytes (1%) |           3 |
| `["gemm", "mul", "xf", "ivdep", "8"]`                          | 335.918 ns (5%) |         |   80 bytes (1%) |           3 |
| `["gemm", "mul", "xf", "true", "256"]`                         |   1.440 ms (5%) |         |   80 bytes (1%) |           3 |
| `["gemm", "mul", "xf", "true", "32"]`                          |   4.000 μs (5%) |         |   80 bytes (1%) |           3 |
| `["gemm", "mul", "xf", "true", "8"]`                           | 354.512 ns (5%) |         |   80 bytes (1%) |           3 |
| `["groupby", "sum", "sac"]`                                    | 159.605 μs (5%) |         |  624 bytes (1%) |           5 |
| `["groupby", "sum", "xf-with-init"]`                           | 132.805 μs (5%) |         |   1.20 KiB (1%) |           9 |
| `["groupby", "sum", "xf-without-init"]`                        | 131.404 μs (5%) |         |   1.20 KiB (1%) |           9 |
| `["mapcat_eduction", "base"]`                                  |   1.560 μs (5%) |         |                 |             |
| `["mapcat_eduction", "xf-eduction"]`                           |   1.400 μs (5%) |         |                 |             |
| `["mapcat_eduction", "xf-xf"]`                                 |   1.400 μs (5%) |         |                 |             |
| `["missing_argmax", "man"]`                                    |   2.233 μs (5%) |         |   32 bytes (1%) |           1 |
| `["missing_argmax", "rf"]`                                     |   1.290 μs (5%) |         |   32 bytes (1%) |           1 |
| `["missing_argmax", "xf"]`                                     |   1.430 μs (5%) |         |   32 bytes (1%) |           1 |
| `["missing_dot", "equiv"]`                                     |   1.130 μs (5%) |         |   16 bytes (1%) |           1 |
| `["missing_dot", "man"]`                                       |   1.160 μs (5%) |         |   16 bytes (1%) |           1 |
| `["missing_dot", "naive"]`                                     |   3.963 μs (5%) |         |   16 bytes (1%) |           1 |
| `["missing_dot", "rf"]`                                        |   1.170 μs (5%) |         |   16 bytes (1%) |           1 |
| `["missing_dot", "rf_nota"]`                                   |   1.160 μs (5%) |         |   16 bytes (1%) |           1 |
| `["missing_dot", "xf"]`                                        |  81.103 μs (5%) |         |  72.16 KiB (1%) |        3742 |
| `["missing_dot", "xf_nota"]`                                   |  82.103 μs (5%) |         |  72.13 KiB (1%) |        3742 |
| `["overhead", "foldl"]`                                        |   3.600 ns (5%) |         |                 |             |
| `["overhead", "reduce_basecase"]`                              | 210.087 ns (5%) |         |  368 bytes (1%) |           6 |
| `["partition_by", "man"]`                                      |   1.742 ms (5%) |         |  352 bytes (1%) |           4 |
| `["partition_by", "xf"]`                                       |   1.740 ms (5%) |         |  544 bytes (1%) |           6 |
| `["set", "base"]`                                              |   3.957 ms (5%) |         |  49.56 KiB (1%) |          17 |
| `["set", "xf"]`                                                |   3.826 ms (5%) |         |  49.59 KiB (1%) |          19 |
| `["sum_transpose", "30", "noinit", "iter"]`                    |   1.880 μs (5%) |         |                 |             |
| `["sum_transpose", "30", "noinit", "man"]`                     |   2.122 μs (5%) |         |                 |             |
| `["sum_transpose", "30", "noinit", "xf"]`                      |   2.511 μs (5%) |         |                 |             |
| `["sum_transpose", "30", "withinit", "iter"]`                  |   1.270 μs (5%) |         |                 |             |
| `["sum_transpose", "30", "withinit", "man"]`                   | 956.522 ns (5%) |         |                 |             |
| `["sum_transpose", "30", "withinit", "xf"]`                    |   2.756 μs (5%) |         |                 |             |

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
       #1  2095 MHz       6866 s          0 s       1222 s      86545 s          0 s
       #2  2095 MHz      61492 s          0 s       1569 s      31374 s          0 s
       
  Memory: 6.764881134033203 GB (2887.59375 MB free)
  Uptime: 964.0 sec
  Load Avg:  1.04248046875  0.9853515625  0.62109375
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-9.0.1 (ORCJIT, skylake)
```

---
# Baseline result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmark: 9 Aug 2020 - 20:47
* Package commit: b8efee
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
| `["append!!", "eduction"]`                                     |  15.100 μs (5%) |         |  64.63 KiB (1%) |          13 |
| `["append!!", "xf"]`                                           |  14.500 μs (5%) |         |  64.63 KiB (1%) |          13 |
| `["cat", "base"]`                                              |   1.530 μs (5%) |         |                 |             |
| `["cat", "xf"]`                                                |   1.400 μs (5%) |         |                 |             |
| `["collect", "filter-missing"]`                                |  47.704 μs (5%) |         |  32.81 KiB (1%) |          14 |
| `["collect", "identity-float"]`                                |  18.402 μs (5%) |         | 256.66 KiB (1%) |          14 |
| `["collect", "identity-union"]`                                | 117.310 μs (5%) |         | 601.13 KiB (1%) |       10013 |
| `["dict", "base"]`                                             |   3.386 ms (5%) |         |  92.91 KiB (1%) |          22 |
| `["dict", "xf"]`                                               |   3.515 ms (5%) |         |  92.31 KiB (1%) |          18 |
| `["dot", "blas"]`                                              | 980.100 ns (5%) |         |                 |             |
| `["dot", "man"]`                                               |   1.008 μs (5%) |         |                 |             |
| `["dot", "rf"]`                                                |   1.770 μs (5%) |         |                 |             |
| `["dot", "xf"]`                                                |   1.830 μs (5%) |         |   64 bytes (1%) |           3 |
| `["filter_map_map!", "man"]`                                   |  53.704 μs (5%) |         |                 |             |
| `["filter_map_map!", "xf"]`                                    | 580.138 μs (5%) |         |   80 bytes (1%) |           3 |
| `["filter_map_reduce", "man"]`                                 | 191.615 μs (5%) |         |                 |             |
| `["filter_map_reduce", "xf"]`                                  | 191.515 μs (5%) |         |                 |             |
| `["filter_sum", "1000", "RandomFloats", "noinit", "base"]`     |   1.060 μs (5%) |         |                 |             |
| `["filter_sum", "1000", "RandomFloats", "noinit", "naive"]`    |   1.070 μs (5%) |         |                 |             |
| `["filter_sum", "1000", "RandomFloats", "noinit", "xf"]`       |   1.480 μs (5%) |         |                 |             |
| `["filter_sum", "1000", "RandomFloats", "withinit", "base"]`   |   1.480 μs (5%) |         |                 |             |
| `["filter_sum", "1000", "RandomFloats", "withinit", "naive"]`  | 695.647 ns (5%) |         |                 |             |
| `["filter_sum", "1000", "RandomFloats", "withinit", "xf"]`     |   1.460 μs (5%) |         |                 |             |
| `["filter_sum", "1000", "UnitRange", "noinit", "base"]`        |   1.510 μs (5%) |         |                 |             |
| `["filter_sum", "1000", "UnitRange", "noinit", "naive"]`       | 706.269 ns (5%) |         |                 |             |
| `["filter_sum", "1000", "UnitRange", "noinit", "xf"]`          | 100.962 ns (5%) |         |                 |             |
| `["filter_sum", "1000", "UnitRange", "withinit", "base"]`      |  87.716 ns (5%) |         |                 |             |
| `["filter_sum", "1000", "UnitRange", "withinit", "naive"]`     | 669.484 ns (5%) |         |                 |             |
| `["filter_sum", "1000", "UnitRange", "withinit", "xf"]`        | 100.009 ns (5%) |         |                 |             |
| `["filter_sum", "10000", "RandomFloats", "noinit", "base"]`    |  33.203 μs (5%) |         |                 |             |
| `["filter_sum", "10000", "RandomFloats", "noinit", "naive"]`   |  38.204 μs (5%) |         |                 |             |
| `["filter_sum", "10000", "RandomFloats", "noinit", "xf"]`      |  15.001 μs (5%) |         |                 |             |
| `["filter_sum", "10000", "RandomFloats", "withinit", "base"]`  |  14.701 μs (5%) |         |                 |             |
| `["filter_sum", "10000", "RandomFloats", "withinit", "naive"]` |  37.703 μs (5%) |         |                 |             |
| `["filter_sum", "10000", "RandomFloats", "withinit", "xf"]`    |  15.001 μs (5%) |         |                 |             |
| `["filter_sum", "10000", "UnitRange", "noinit", "base"]`       |  14.701 μs (5%) |         |                 |             |
| `["filter_sum", "10000", "UnitRange", "noinit", "naive"]`      |   6.981 μs (5%) |         |                 |             |
| `["filter_sum", "10000", "UnitRange", "noinit", "xf"]`         | 966.722 ns (5%) |         |                 |             |
| `["filter_sum", "10000", "UnitRange", "withinit", "base"]`     | 829.551 ns (5%) |         |                 |             |
| `["filter_sum", "10000", "UnitRange", "withinit", "naive"]`    |   6.620 μs (5%) |         |                 |             |
| `["filter_sum", "10000", "UnitRange", "withinit", "xf"]`       | 966.722 ns (5%) |         |                 |             |
| `["findall", "base"]`                                          | 675.757 μs (5%) |         |   2.00 MiB (1%) |          18 |
| `["findall", "xf-array"]`                                      | 593.150 μs (5%) |         |   3.02 MiB (1%) |       98829 |
| `["findall", "xf-iter"]`                                       | 249.720 μs (5%) |         |   2.00 MiB (1%) |          19 |
| `["gemm", "fusedmul", "blas", "16"]`                           |   2.912 ms (5%) |         |                 |             |
| `["gemm", "fusedmul", "blas", "2"]`                            |   2.402 ms (5%) |         |                 |             |
| `["gemm", "fusedmul", "blas", "32"]`                           |   3.537 ms (5%) |         |                 |             |
| `["gemm", "fusedmul", "blas", "8"]`                            |   2.574 ms (5%) |         |                 |             |
| `["gemm", "fusedmul", "xf", "16"]`                             |   5.171 ms (5%) |         |  192 bytes (1%) |           4 |
| `["gemm", "fusedmul", "xf", "2"]`                              | 579.940 μs (5%) |         |  192 bytes (1%) |           4 |
| `["gemm", "fusedmul", "xf", "32"]`                             |   8.794 ms (5%) |         |  192 bytes (1%) |           4 |
| `["gemm", "fusedmul", "xf", "8"]`                              |   2.250 ms (5%) |         |  192 bytes (1%) |           4 |
| `["gemm", "mul", "linalg", "256"]`                             | 399.631 μs (5%) |         |                 |             |
| `["gemm", "mul", "linalg", "32"]`                              |   1.800 μs (5%) |         |                 |             |
| `["gemm", "mul", "linalg", "8"]`                               | 100.000 ns (5%) |         |                 |             |
| `["gemm", "mul", "man", "false", "256"]`                       |   1.488 ms (5%) |         |                 |             |
| `["gemm", "mul", "man", "false", "32"]`                        |   4.100 μs (5%) |         |                 |             |
| `["gemm", "mul", "man", "false", "8"]`                         | 300.000 ns (5%) |         |                 |             |
| `["gemm", "mul", "man", "ivdep", "256"]`                       |   1.418 ms (5%) |         |                 |             |
| `["gemm", "mul", "man", "ivdep", "32"]`                        |   3.100 μs (5%) |         |                 |             |
| `["gemm", "mul", "man", "ivdep", "8"]`                         | 300.000 ns (5%) |         |                 |             |
| `["gemm", "mul", "man", "true", "256"]`                        |   1.447 ms (5%) |         |                 |             |
| `["gemm", "mul", "man", "true", "32"]`                         |   3.800 μs (5%) |         |                 |             |
| `["gemm", "mul", "man", "true", "8"]`                          | 400.000 ns (5%) |         |                 |             |
| `["gemm", "mul", "xf", "false", "256"]`                        |   1.493 ms (5%) |         |   80 bytes (1%) |           3 |
| `["gemm", "mul", "xf", "false", "32"]`                         |   3.801 μs (5%) |         |   80 bytes (1%) |           3 |
| `["gemm", "mul", "xf", "false", "8"]`                          | 300.000 ns (5%) |         |   80 bytes (1%) |           3 |
| `["gemm", "mul", "xf", "ivdep", "256"]`                        |   1.419 ms (5%) |         |   80 bytes (1%) |           3 |
| `["gemm", "mul", "xf", "ivdep", "32"]`                         |   3.200 μs (5%) |         |   80 bytes (1%) |           3 |
| `["gemm", "mul", "xf", "ivdep", "8"]`                          | 300.000 ns (5%) |         |   80 bytes (1%) |           3 |
| `["gemm", "mul", "xf", "true", "256"]`                         |   1.487 ms (5%) |         |   80 bytes (1%) |           3 |
| `["gemm", "mul", "xf", "true", "32"]`                          |   4.000 μs (5%) |         |   80 bytes (1%) |           3 |
| `["gemm", "mul", "xf", "true", "8"]`                           | 300.000 ns (5%) |         |   80 bytes (1%) |           3 |
| `["groupby", "sum", "sac"]`                                    | 160.710 μs (5%) |         |  624 bytes (1%) |           5 |
| `["groupby", "sum", "xf-with-init"]`                           | 129.708 μs (5%) |         |   1.20 KiB (1%) |           9 |
| `["groupby", "sum", "xf-without-init"]`                        | 133.209 μs (5%) |         |   1.20 KiB (1%) |           9 |
| `["mapcat_eduction", "base"]`                                  |   1.560 μs (5%) |         |                 |             |
| `["mapcat_eduction", "xf-eduction"]`                           |   1.430 μs (5%) |         |                 |             |
| `["mapcat_eduction", "xf-xf"]`                                 |   1.400 μs (5%) |         |                 |             |
| `["missing_argmax", "man"]`                                    |   2.233 μs (5%) |         |   32 bytes (1%) |           1 |
| `["missing_argmax", "rf"]`                                     |   1.230 μs (5%) |         |   32 bytes (1%) |           1 |
| `["missing_argmax", "xf"]`                                     |   1.290 μs (5%) |         |   32 bytes (1%) |           1 |
| `["missing_dot", "equiv"]`                                     |   1.150 μs (5%) |         |   16 bytes (1%) |           1 |
| `["missing_dot", "man"]`                                       |   1.150 μs (5%) |         |   16 bytes (1%) |           1 |
| `["missing_dot", "naive"]`                                     |   3.975 μs (5%) |         |   16 bytes (1%) |           1 |
| `["missing_dot", "rf"]`                                        |   1.160 μs (5%) |         |   16 bytes (1%) |           1 |
| `["missing_dot", "rf_nota"]`                                   |   1.160 μs (5%) |         |   16 bytes (1%) |           1 |
| `["missing_dot", "xf"]`                                        |  81.707 μs (5%) |         |  72.13 KiB (1%) |        3742 |
| `["missing_dot", "xf_nota"]`                                   |  85.307 μs (5%) |         |  72.19 KiB (1%) |        3744 |
| `["overhead", "foldl"]`                                        |   3.600 ns (5%) |         |                 |             |
| `["overhead", "reduce_basecase"]`                              | 213.063 ns (5%) |         |  368 bytes (1%) |           6 |
| `["partition_by", "man"]`                                      |   1.750 ms (5%) |         |  352 bytes (1%) |           4 |
| `["partition_by", "xf"]`                                       |   1.741 ms (5%) |         |  544 bytes (1%) |           6 |
| `["set", "base"]`                                              |   3.920 ms (5%) |         |  49.56 KiB (1%) |          17 |
| `["set", "xf"]`                                                |   3.867 ms (5%) |         |  49.59 KiB (1%) |          19 |
| `["sum_transpose", "30", "noinit", "iter"]`                    |   1.880 μs (5%) |         |                 |             |
| `["sum_transpose", "30", "noinit", "man"]`                     |   2.122 μs (5%) |         |                 |             |
| `["sum_transpose", "30", "noinit", "xf"]`                      |   2.511 μs (5%) |         |                 |             |
| `["sum_transpose", "30", "withinit", "iter"]`                  |   1.270 μs (5%) |         |                 |             |
| `["sum_transpose", "30", "withinit", "man"]`                   | 956.565 ns (5%) |         |                 |             |
| `["sum_transpose", "30", "withinit", "xf"]`                    |   2.511 μs (5%) |         |                 |             |

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
       #1  2095 MHz       6981 s          0 s       1279 s     112231 s          0 s
       #2  2095 MHz      87090 s          0 s       1806 s      31409 s          0 s
       
  Memory: 6.764881134033203 GB (2988.125 MB free)
  Uptime: 1224.0 sec
  Load Avg:  1.09326171875  1.03759765625  0.744140625
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
    CPU MHz:             2095.196
    BogoMIPS:            4190.39
    Hypervisor vendor:   Microsoft
    Virtualization type: full
    L1d cache:           32K
    L1i cache:           32K
    L2 cache:            1024K
    L3 cache:            36608K
    NUMA node0 CPU(s):   0,1
    Flags:               fpu vme de pse tsc msr pae mce cx8 apic sep mtrr pge mca cmov pat pse36 clflush mmx fxsr sse sse2 ss ht syscall nx pdpe1gb rdtscp lm constant_tsc rep_good nopl xtopology cpuid pni pclmulqdq ssse3 fma cx16 pcid sse4_1 sse4_2 movbe popcnt aes xsave avx f16c rdrand hypervisor lahf_lm abm 3dnowprefetch invpcid_single pti fsgsbase bmi1 hle avx2 smep bmi2 erms invpcid rtm mpx avx512f avx512dq rdseed adx smap clflushopt avx512cd avx512bw avx512vl xsaveopt xsavec xsaves
    

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

