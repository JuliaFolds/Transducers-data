# Benchmark result

* Pull request commit: [`52317636c7c735d8c98f9b2c987e34e5a16dbcb9`](https://github.com/JuliaFolds/Transducers.jl/commit/52317636c7c735d8c98f9b2c987e34e5a16dbcb9)
* Pull request: <https://github.com/JuliaFolds/Transducers.jl/pull/243> (Update */Manifest.toml)

# Judge result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmarks:
    - Target: 15 Aug 2020 - 00:54
    - Baseline: 15 Aug 2020 - 01:00
* Package commits:
    - Target: e4e9ba
    - Baseline: 3a5745
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
| `["cartesian", "copyto!", "man"]`                              | 0.90 (5%) :white_check_mark: |    1.00 (1%)  |
| `["cartesian", "copyto!", "xf"]`                               | 0.79 (5%) :white_check_mark: |    1.00 (1%)  |
| `["cat", "base"]`                                              |                1.15 (5%) :x: |    1.00 (1%)  |
| `["cat", "xf"]`                                                |                1.17 (5%) :x: |    1.00 (1%)  |
| `["collect", "filter-missing"]`                                |                1.28 (5%) :x: |    1.00 (1%)  |
| `["collect", "identity-float"]`                                |                1.17 (5%) :x: |    1.00 (1%)  |
| `["collect", "identity-union"]`                                |                1.25 (5%) :x: |    1.00 (1%)  |
| `["dot", "xf"]`                                                |                1.11 (5%) :x: |    1.00 (1%)  |
| `["filter_map_map!", "man"]`                                   |                1.29 (5%) :x: |    1.00 (1%)  |
| `["filter_map_map!", "xf"]`                                    |                1.32 (5%) :x: |    1.00 (1%)  |
| `["filter_map_reduce", "man"]`                                 |                1.33 (5%) :x: |    1.00 (1%)  |
| `["filter_map_reduce", "xf"]`                                  |                1.33 (5%) :x: |    1.00 (1%)  |
| `["filter_sum", "1000", "RandomFloats", "noinit", "naive"]`    |                1.15 (5%) :x: |    1.00 (1%)  |
| `["filter_sum", "1000", "RandomFloats", "noinit", "xf"]`       |                1.15 (5%) :x: |    1.00 (1%)  |
| `["filter_sum", "1000", "RandomFloats", "withinit", "naive"]`  |                1.05 (5%) :x: |    1.00 (1%)  |
| `["filter_sum", "1000", "RandomFloats", "withinit", "xf"]`     |                1.16 (5%) :x: |    1.00 (1%)  |
| `["filter_sum", "1000", "UnitRange", "noinit", "base"]`        |                1.15 (5%) :x: |    1.00 (1%)  |
| `["filter_sum", "1000", "UnitRange", "noinit", "naive"]`       | 0.86 (5%) :white_check_mark: |    1.00 (1%)  |
| `["filter_sum", "1000", "UnitRange", "noinit", "xf"]`          |                1.14 (5%) :x: |    1.00 (1%)  |
| `["filter_sum", "1000", "UnitRange", "withinit", "base"]`      |                1.15 (5%) :x: |    1.00 (1%)  |
| `["filter_sum", "1000", "UnitRange", "withinit", "naive"]`     | 0.91 (5%) :white_check_mark: |    1.00 (1%)  |
| `["filter_sum", "10000", "RandomFloats", "noinit", "naive"]`   |                1.33 (5%) :x: |    1.00 (1%)  |
| `["filter_sum", "10000", "RandomFloats", "noinit", "xf"]`      |                1.14 (5%) :x: |    1.00 (1%)  |
| `["filter_sum", "10000", "RandomFloats", "withinit", "base"]`  |                1.17 (5%) :x: |    1.00 (1%)  |
| `["filter_sum", "10000", "RandomFloats", "withinit", "xf"]`    |                1.33 (5%) :x: |    1.00 (1%)  |
| `["filter_sum", "10000", "UnitRange", "withinit", "naive"]`    | 0.79 (5%) :white_check_mark: |    1.00 (1%)  |
| `["findall", "base"]`                                          |                1.46 (5%) :x: |    1.00 (1%)  |
| `["findall", "xf-array"]`                                      |                1.23 (5%) :x: |    1.00 (1%)  |
| `["findall", "xf-iter"]`                                       |                1.34 (5%) :x: |    1.00 (1%)  |
| `["gemm", "fusedmul", "blas", "16"]`                           |                1.16 (5%) :x: |    1.00 (1%)  |
| `["gemm", "fusedmul", "blas", "2"]`                            |                1.16 (5%) :x: |    1.00 (1%)  |
| `["gemm", "fusedmul", "blas", "32"]`                           |                1.20 (5%) :x: |    1.00 (1%)  |
| `["gemm", "fusedmul", "blas", "8"]`                            |                1.15 (5%) :x: |    1.00 (1%)  |
| `["gemm", "fusedmul", "xf", "8"]`                              | 0.83 (5%) :white_check_mark: |    1.00 (1%)  |
| `["gemm", "mul", "linalg", "256"]`                             |                1.28 (5%) :x: |    1.00 (1%)  |
| `["gemm", "mul", "linalg", "8"]`                               |                1.14 (5%) :x: |    1.00 (1%)  |
| `["gemm", "mul", "man", "false", "256"]`                       |                1.25 (5%) :x: |    1.00 (1%)  |
| `["gemm", "mul", "man", "false", "8"]`                         |                1.13 (5%) :x: |    1.00 (1%)  |
| `["gemm", "mul", "man", "ivdep", "256"]`                       |                1.28 (5%) :x: |    1.00 (1%)  |
| `["gemm", "mul", "man", "ivdep", "32"]`                        |                1.27 (5%) :x: |    1.00 (1%)  |
| `["gemm", "mul", "man", "ivdep", "8"]`                         |                1.75 (5%) :x: |    1.00 (1%)  |
| `["gemm", "mul", "man", "true", "256"]`                        |                1.26 (5%) :x: |    1.00 (1%)  |
| `["gemm", "mul", "man", "true", "32"]`                         |                1.30 (5%) :x: |    1.00 (1%)  |
| `["gemm", "mul", "man", "true", "8"]`                          |                1.43 (5%) :x: |    1.00 (1%)  |
| `["gemm", "mul", "xf", "false", "256"]`                        |                1.25 (5%) :x: |    1.00 (1%)  |
| `["gemm", "mul", "xf", "false", "32"]`                         |                1.40 (5%) :x: |    1.00 (1%)  |
| `["gemm", "mul", "xf", "false", "8"]`                          |                1.61 (5%) :x: |    1.00 (1%)  |
| `["gemm", "mul", "xf", "ivdep", "256"]`                        |                1.28 (5%) :x: |    1.00 (1%)  |
| `["gemm", "mul", "xf", "ivdep", "32"]`                         |                1.11 (5%) :x: |    1.00 (1%)  |
| `["gemm", "mul", "xf", "ivdep", "8"]`                          |                1.55 (5%) :x: |    1.00 (1%)  |
| `["gemm", "mul", "xf", "true", "256"]`                         |                1.25 (5%) :x: |    1.00 (1%)  |
| `["gemm", "mul", "xf", "true", "32"]`                          |                1.29 (5%) :x: |    1.00 (1%)  |
| `["gemm", "mul", "xf", "true", "8"]`                           |                1.19 (5%) :x: |    1.00 (1%)  |
| `["groupby", "sum", "sac"]`                                    | 0.94 (5%) :white_check_mark: | 2.51 (1%) :x: |
| `["groupby", "sum", "xf-with-init"]`                           |                1.24 (5%) :x: |    1.00 (1%)  |
| `["groupby", "sum", "xf-without-init"]`                        |                1.24 (5%) :x: |    1.00 (1%)  |
| `["mapcat_eduction", "base"]`                                  |                1.33 (5%) :x: |    1.00 (1%)  |
| `["mapcat_eduction", "xf-eduction"]`                           |                1.16 (5%) :x: |    1.00 (1%)  |
| `["mapcat_eduction", "xf-xf"]`                                 |                1.42 (5%) :x: |    1.00 (1%)  |
| `["missing_argmax", "man"]`                                    |                1.33 (5%) :x: |    1.00 (1%)  |
| `["missing_argmax", "rf"]`                                     |                1.18 (5%) :x: |    1.00 (1%)  |
| `["missing_argmax", "xf"]`                                     |                1.17 (5%) :x: |    1.00 (1%)  |
| `["missing_dot", "equiv"]`                                     | 0.89 (5%) :white_check_mark: |    1.00 (1%)  |
| `["missing_dot", "man"]`                                       |                1.31 (5%) :x: |    1.00 (1%)  |
| `["missing_dot", "naive"]`                                     |                1.34 (5%) :x: |    1.00 (1%)  |
| `["missing_dot", "rf"]`                                        |                1.16 (5%) :x: |    1.00 (1%)  |
| `["missing_dot", "rf_nota"]`                                   |                1.32 (5%) :x: |    1.00 (1%)  |
| `["missing_dot", "xf"]`                                        |                1.34 (5%) :x: |    1.00 (1%)  |
| `["missing_dot", "xf_nota"]`                                   |                1.29 (5%) :x: |    1.00 (1%)  |
| `["overhead", "foldl"]`                                        |                1.24 (5%) :x: |    1.00 (1%)  |
| `["overhead", "reduce_basecase"]`                              |                1.33 (5%) :x: |    1.00 (1%)  |
| `["partition_by", "man"]`                                      | 0.94 (5%) :white_check_mark: |    1.00 (1%)  |
| `["partition_by", "xf"]`                                       |                1.05 (5%) :x: |    1.00 (1%)  |
| `["set", "base"]`                                              |                1.21 (5%) :x: |    1.00 (1%)  |
| `["set", "xf"]`                                                |                1.27 (5%) :x: |    1.00 (1%)  |
| `["sum_transpose", "30", "noinit", "iter"]`                    |                1.15 (5%) :x: |    1.00 (1%)  |
| `["sum_transpose", "30", "noinit", "man"]`                     |                1.34 (5%) :x: |    1.00 (1%)  |
| `["sum_transpose", "30", "noinit", "xf"]`                      |                1.15 (5%) :x: |    1.00 (1%)  |
| `["sum_transpose", "30", "withinit", "iter"]`                  |                1.33 (5%) :x: |    1.00 (1%)  |
| `["sum_transpose", "30", "withinit", "man"]`                   |                1.14 (5%) :x: |    1.00 (1%)  |
| `["sum_transpose", "30", "withinit", "xf"]`                    |                1.14 (5%) :x: |    1.00 (1%)  |
| `["teerf_filter", "noinit"]`                                   |                1.13 (5%) :x: |    1.00 (1%)  |
| `["teerf_filter", "withinit"]`                                 |                1.32 (5%) :x: |    1.00 (1%)  |

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
Julia Version 1.5.0
Commit 96786e22cc (2020-08-01 23:44 UTC)
Platform Info:
  OS: Linux (x86_64-pc-linux-gnu)
      Ubuntu 18.04.4 LTS
  uname: Linux 5.3.0-1034-azure #35~18.04.1-Ubuntu SMP Mon Jul 13 12:54:45 UTC 2020 x86_64 x86_64
  CPU: Intel(R) Xeon(R) Platinum 8171M CPU @ 2.60GHz: 
              speed         user         nice          sys         idle          irq
       #1  2095 MHz      66389 s          0 s       1492 s      11455 s          0 s
       #2  2095 MHz      10016 s          0 s       1605 s      68306 s          0 s
       
  Memory: 6.764881134033203 GB (2628.37890625 MB free)
  Uptime: 819.0 sec
  Load Avg:  1.0  0.99072265625  0.6953125
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
       #1  2095 MHz      93488 s          0 s       1772 s      17352 s          0 s
       #2  2095 MHz      15924 s          0 s       1794 s      95496 s          0 s
       
  Memory: 6.764881134033203 GB (2515.1328125 MB free)
  Uptime: 1153.0 sec
  Load Avg:  1.0107421875  1.00634765625  0.80712890625
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-9.0.1 (ORCJIT, skylake)
```

---
# Target result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmark: 15 Aug 2020 - 0:54
* Package commit: e4e9ba
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
| `["append!!", "eduction"]`                                     |  20.502 μs (5%) |         |  64.63 KiB (1%) |          13 |
| `["append!!", "xf"]`                                           |  20.902 μs (5%) |         |  64.63 KiB (1%) |          13 |
| `["cartesian", "copyto!", "iter"]`                             |   6.601 μs (5%) |         |                 |             |
| `["cartesian", "copyto!", "man"]`                              |   2.360 μs (5%) |         |                 |             |
| `["cartesian", "copyto!", "xf"]`                               |   3.034 μs (5%) |         |                 |             |
| `["cat", "base"]`                                              |   2.078 μs (5%) |         |                 |             |
| `["cat", "xf"]`                                                |   1.900 μs (5%) |         |                 |             |
| `["collect", "filter-missing"]`                                |  70.906 μs (5%) |         |  32.81 KiB (1%) |          14 |
| `["collect", "identity-float"]`                                |  29.603 μs (5%) |         | 256.66 KiB (1%) |          14 |
| `["collect", "identity-union"]`                                | 164.115 μs (5%) |         | 601.05 KiB (1%) |       10013 |
| `["dict", "base"]`                                             |   4.530 ms (5%) |         |  92.91 KiB (1%) |          22 |
| `["dict", "xf"]`                                               |   4.695 ms (5%) |         |  92.31 KiB (1%) |          18 |
| `["dot", "blas"]`                                              |   1.330 μs (5%) |         |                 |             |
| `["dot", "man"]`                                               |   1.250 μs (5%) |         |                 |             |
| `["dot", "rf"]`                                                |   2.360 μs (5%) |         |                 |             |
| `["dot", "xf"]`                                                |   2.440 μs (5%) |         |   64 bytes (1%) |           3 |
| `["filter_map_map!", "man"]`                                   |  68.705 μs (5%) |         |                 |             |
| `["filter_map_map!", "xf"]`                                    | 772.853 μs (5%) |         |   80 bytes (1%) |           3 |
| `["filter_map_reduce", "man"]`                                 | 255.621 μs (5%) |         |                 |             |
| `["filter_map_reduce", "xf"]`                                  | 255.422 μs (5%) |         |                 |             |
| `["filter_sum", "1000", "RandomFloats", "noinit", "base"]`     |   1.420 μs (5%) |         |                 |             |
| `["filter_sum", "1000", "RandomFloats", "noinit", "naive"]`    |   1.430 μs (5%) |         |                 |             |
| `["filter_sum", "1000", "RandomFloats", "noinit", "xf"]`       |   1.980 μs (5%) |         |                 |             |
| `["filter_sum", "1000", "RandomFloats", "withinit", "base"]`   |   1.960 μs (5%) |         |                 |             |
| `["filter_sum", "1000", "RandomFloats", "withinit", "naive"]`  | 919.007 ns (5%) |         |                 |             |
| `["filter_sum", "1000", "RandomFloats", "withinit", "xf"]`     |   1.980 μs (5%) |         |                 |             |
| `["filter_sum", "1000", "UnitRange", "noinit", "base"]`        |   2.010 μs (5%) |         |                 |             |
| `["filter_sum", "1000", "UnitRange", "noinit", "naive"]`       |   1.126 μs (5%) |         |                 |             |
| `["filter_sum", "1000", "UnitRange", "noinit", "xf"]`          | 135.046 ns (5%) |         |                 |             |
| `["filter_sum", "1000", "UnitRange", "withinit", "base"]`      | 116.261 ns (5%) |         |                 |             |
| `["filter_sum", "1000", "UnitRange", "withinit", "naive"]`     | 820.312 ns (5%) |         |                 |             |
| `["filter_sum", "1000", "UnitRange", "withinit", "xf"]`        | 135.667 ns (5%) |         |                 |             |
| `["filter_sum", "10000", "RandomFloats", "noinit", "base"]`    |  46.604 μs (5%) |         |                 |             |
| `["filter_sum", "10000", "RandomFloats", "noinit", "naive"]`   |  59.405 μs (5%) |         |                 |             |
| `["filter_sum", "10000", "RandomFloats", "noinit", "xf"]`      |  20.002 μs (5%) |         |                 |             |
| `["filter_sum", "10000", "RandomFloats", "withinit", "base"]`  |  20.002 μs (5%) |         |                 |             |
| `["filter_sum", "10000", "RandomFloats", "withinit", "naive"]` |  49.805 μs (5%) |         |                 |             |
| `["filter_sum", "10000", "RandomFloats", "withinit", "xf"]`    |  20.101 μs (5%) |         |                 |             |
| `["filter_sum", "10000", "UnitRange", "noinit", "base"]`       |  19.502 μs (5%) |         |                 |             |
| `["filter_sum", "10000", "UnitRange", "noinit", "naive"]`      |  11.168 μs (5%) |         |                 |             |
| `["filter_sum", "10000", "UnitRange", "noinit", "xf"]`         |   1.300 μs (5%) |         |                 |             |
| `["filter_sum", "10000", "UnitRange", "withinit", "base"]`     |   1.107 μs (5%) |         |                 |             |
| `["filter_sum", "10000", "UnitRange", "withinit", "naive"]`    |   8.061 μs (5%) |         |                 |             |
| `["filter_sum", "10000", "UnitRange", "withinit", "xf"]`       |   1.294 μs (5%) |         |                 |             |
| `["findall", "base"]`                                          |   1.039 ms (5%) |         |   2.00 MiB (1%) |          18 |
| `["findall", "xf-array"]`                                      | 814.471 μs (5%) |         |   3.02 MiB (1%) |       98829 |
| `["findall", "xf-iter"]`                                       | 406.835 μs (5%) |         |   2.00 MiB (1%) |          19 |
| `["gemm", "fusedmul", "blas", "16"]`                           |   3.500 ms (5%) |         |                 |             |
| `["gemm", "fusedmul", "blas", "2"]`                            |   2.836 ms (5%) |         |                 |             |
| `["gemm", "fusedmul", "blas", "32"]`                           |   4.393 ms (5%) |         |                 |             |
| `["gemm", "fusedmul", "blas", "8"]`                            |   3.061 ms (5%) |         |                 |             |
| `["gemm", "fusedmul", "xf", "16"]`                             |   4.517 ms (5%) |         |  192 bytes (1%) |           4 |
| `["gemm", "fusedmul", "xf", "2"]`                              | 588.541 μs (5%) |         |  192 bytes (1%) |           4 |
| `["gemm", "fusedmul", "xf", "32"]`                             |  10.267 ms (5%) |         |  192 bytes (1%) |           4 |
| `["gemm", "fusedmul", "xf", "8"]`                              |   2.047 ms (5%) |         |  192 bytes (1%) |           4 |
| `["gemm", "mul", "linalg", "256"]`                             | 515.741 μs (5%) |         |                 |             |
| `["gemm", "mul", "linalg", "32"]`                              |   2.034 μs (5%) |         |                 |             |
| `["gemm", "mul", "linalg", "8"]`                               | 227.207 ns (5%) |         |                 |             |
| `["gemm", "mul", "man", "false", "256"]`                       |   1.814 ms (5%) |         |                 |             |
| `["gemm", "mul", "man", "false", "32"]`                        |   5.400 μs (5%) |         |                 |             |
| `["gemm", "mul", "man", "false", "8"]`                         | 452.556 ns (5%) |         |                 |             |
| `["gemm", "mul", "man", "ivdep", "256"]`                       |   1.828 ms (5%) |         |                 |             |
| `["gemm", "mul", "man", "ivdep", "32"]`                        |   4.072 μs (5%) |         |                 |             |
| `["gemm", "mul", "man", "ivdep", "8"]`                         | 526.215 ns (5%) |         |                 |             |
| `["gemm", "mul", "man", "true", "256"]`                        |   1.813 ms (5%) |         |                 |             |
| `["gemm", "mul", "man", "true", "32"]`                         |   5.200 μs (5%) |         |                 |             |
| `["gemm", "mul", "man", "true", "8"]`                          | 428.673 ns (5%) |         |                 |             |
| `["gemm", "mul", "xf", "false", "256"]`                        |   1.814 ms (5%) |         |   80 bytes (1%) |           3 |
| `["gemm", "mul", "xf", "false", "32"]`                         |   5.450 μs (5%) |         |   80 bytes (1%) |           3 |
| `["gemm", "mul", "xf", "false", "8"]`                          | 483.204 ns (5%) |         |   80 bytes (1%) |           3 |
| `["gemm", "mul", "xf", "ivdep", "256"]`                        |   1.827 ms (5%) |         |   80 bytes (1%) |           3 |
| `["gemm", "mul", "xf", "ivdep", "32"]`                         |   4.115 μs (5%) |         |   80 bytes (1%) |           3 |
| `["gemm", "mul", "xf", "ivdep", "8"]`                          | 463.995 ns (5%) |         |   80 bytes (1%) |           3 |
| `["gemm", "mul", "xf", "true", "256"]`                         |   1.813 ms (5%) |         |   80 bytes (1%) |           3 |
| `["gemm", "mul", "xf", "true", "32"]`                          |   5.300 μs (5%) |         |   80 bytes (1%) |           3 |
| `["gemm", "mul", "xf", "true", "8"]`                           | 475.551 ns (5%) |         |   80 bytes (1%) |           3 |
| `["groupby", "sum", "sac"]`                                    | 159.211 μs (5%) |         |   1.53 KiB (1%) |          16 |
| `["groupby", "sum", "xf-with-init"]`                           | 174.112 μs (5%) |         |   1.20 KiB (1%) |           9 |
| `["groupby", "sum", "xf-without-init"]`                        | 174.812 μs (5%) |         |   1.20 KiB (1%) |           9 |
| `["mapcat_eduction", "base"]`                                  |   2.078 μs (5%) |         |                 |             |
| `["mapcat_eduction", "xf-eduction"]`                           |   1.890 μs (5%) |         |                 |             |
| `["mapcat_eduction", "xf-xf"]`                                 |   1.990 μs (5%) |         |                 |             |
| `["missing_argmax", "man"]`                                    |   2.978 μs (5%) |         |   32 bytes (1%) |           1 |
| `["missing_argmax", "rf"]`                                     |   2.070 μs (5%) |         |   32 bytes (1%) |           1 |
| `["missing_argmax", "xf"]`                                     |   2.110 μs (5%) |         |   32 bytes (1%) |           1 |
| `["missing_dot", "equiv"]`                                     |   1.360 μs (5%) |         |   16 bytes (1%) |           1 |
| `["missing_dot", "man"]`                                       |   1.560 μs (5%) |         |   16 bytes (1%) |           1 |
| `["missing_dot", "naive"]`                                     |   5.434 μs (5%) |         |   16 bytes (1%) |           1 |
| `["missing_dot", "rf"]`                                        |   1.560 μs (5%) |         |   16 bytes (1%) |           1 |
| `["missing_dot", "rf_nota"]`                                   |   1.530 μs (5%) |         |   16 bytes (1%) |           1 |
| `["missing_dot", "xf"]`                                        | 113.509 μs (5%) |         |  72.30 KiB (1%) |        3748 |
| `["missing_dot", "xf_nota"]`                                   | 109.809 μs (5%) |         |  72.11 KiB (1%) |        3742 |
| `["overhead", "foldl"]`                                        |   5.600 ns (5%) |         |                 |             |
| `["overhead", "reduce_basecase"]`                              | 286.087 ns (5%) |         |  368 bytes (1%) |           6 |
| `["partition_by", "man"]`                                      |   2.247 ms (5%) |         |  352 bytes (1%) |           4 |
| `["partition_by", "xf"]`                                       |   2.470 ms (5%) |         |  544 bytes (1%) |           6 |
| `["set", "base"]`                                              |   5.312 ms (5%) |         |  49.56 KiB (1%) |          17 |
| `["set", "xf"]`                                                |   5.217 ms (5%) |         |  49.59 KiB (1%) |          19 |
| `["sum_transpose", "30", "noinit", "iter"]`                    |   2.510 μs (5%) |         |                 |             |
| `["sum_transpose", "30", "noinit", "man"]`                     |   2.834 μs (5%) |         |                 |             |
| `["sum_transpose", "30", "noinit", "xf"]`                      |   1.410 μs (5%) |         |   32 bytes (1%) |           2 |
| `["sum_transpose", "30", "withinit", "iter"]`                  |   2.010 μs (5%) |         |                 |             |
| `["sum_transpose", "30", "withinit", "man"]`                   |   1.270 μs (5%) |         |                 |             |
| `["sum_transpose", "30", "withinit", "xf"]`                    |   1.360 μs (5%) |         |   48 bytes (1%) |           3 |
| `["teerf_filter", "noinit"]`                                   | 438.961 ns (5%) |         |  112 bytes (1%) |           4 |
| `["teerf_filter", "withinit"]`                                 | 215.873 ns (5%) |         |                 |             |

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
Julia Version 1.5.0
Commit 96786e22cc (2020-08-01 23:44 UTC)
Platform Info:
  OS: Linux (x86_64-pc-linux-gnu)
      Ubuntu 18.04.4 LTS
  uname: Linux 5.3.0-1034-azure #35~18.04.1-Ubuntu SMP Mon Jul 13 12:54:45 UTC 2020 x86_64 x86_64
  CPU: Intel(R) Xeon(R) Platinum 8171M CPU @ 2.60GHz: 
              speed         user         nice          sys         idle          irq
       #1  2095 MHz      66389 s          0 s       1492 s      11455 s          0 s
       #2  2095 MHz      10016 s          0 s       1605 s      68306 s          0 s
       
  Memory: 6.764881134033203 GB (2628.37890625 MB free)
  Uptime: 819.0 sec
  Load Avg:  1.0  0.99072265625  0.6953125
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-9.0.1 (ORCJIT, skylake)
```

---
# Baseline result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmark: 15 Aug 2020 - 1:0
* Package commit: 3a5745
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
| `["append!!", "eduction"]`                                     |  20.601 μs (5%) |         |  64.63 KiB (1%) |          13 |
| `["append!!", "xf"]`                                           |  20.501 μs (5%) |         |  64.63 KiB (1%) |          13 |
| `["cartesian", "copyto!", "iter"]`                             |   6.586 μs (5%) |         |                 |             |
| `["cartesian", "copyto!", "man"]`                              |   2.630 μs (5%) |         |                 |             |
| `["cartesian", "copyto!", "xf"]`                               |   3.845 μs (5%) |         |                 |             |
| `["cat", "base"]`                                              |   1.811 μs (5%) |         |                 |             |
| `["cat", "xf"]`                                                |   1.620 μs (5%) |         |                 |             |
| `["collect", "filter-missing"]`                                |  55.503 μs (5%) |         |  32.81 KiB (1%) |          14 |
| `["collect", "identity-float"]`                                |  25.202 μs (5%) |         | 256.66 KiB (1%) |          14 |
| `["collect", "identity-union"]`                                | 131.008 μs (5%) |         | 601.04 KiB (1%) |       10013 |
| `["dict", "base"]`                                             |   4.526 ms (5%) |         |  92.91 KiB (1%) |          22 |
| `["dict", "xf"]`                                               |   4.694 ms (5%) |         |  92.31 KiB (1%) |          18 |
| `["dot", "blas"]`                                              |   1.320 μs (5%) |         |                 |             |
| `["dot", "man"]`                                               |   1.300 μs (5%) |         |                 |             |
| `["dot", "rf"]`                                                |   2.360 μs (5%) |         |                 |             |
| `["dot", "xf"]`                                                |   2.190 μs (5%) |         |   64 bytes (1%) |           3 |
| `["filter_map_map!", "man"]`                                   |  53.106 μs (5%) |         |                 |             |
| `["filter_map_map!", "xf"]`                                    | 586.064 μs (5%) |         |   80 bytes (1%) |           3 |
| `["filter_map_reduce", "man"]`                                 | 191.712 μs (5%) |         |                 |             |
| `["filter_map_reduce", "xf"]`                                  | 191.811 μs (5%) |         |                 |             |
| `["filter_sum", "1000", "RandomFloats", "noinit", "base"]`     |   1.420 μs (5%) |         |                 |             |
| `["filter_sum", "1000", "RandomFloats", "noinit", "naive"]`    |   1.240 μs (5%) |         |                 |             |
| `["filter_sum", "1000", "RandomFloats", "noinit", "xf"]`       |   1.720 μs (5%) |         |                 |             |
| `["filter_sum", "1000", "RandomFloats", "withinit", "base"]`   |   1.980 μs (5%) |         |                 |             |
| `["filter_sum", "1000", "RandomFloats", "withinit", "naive"]`  | 871.676 ns (5%) |         |                 |             |
| `["filter_sum", "1000", "RandomFloats", "withinit", "xf"]`     |   1.700 μs (5%) |         |                 |             |
| `["filter_sum", "1000", "UnitRange", "noinit", "base"]`        |   1.750 μs (5%) |         |                 |             |
| `["filter_sum", "1000", "UnitRange", "noinit", "naive"]`       |   1.315 μs (5%) |         |                 |             |
| `["filter_sum", "1000", "UnitRange", "noinit", "xf"]`          | 118.160 ns (5%) |         |                 |             |
| `["filter_sum", "1000", "UnitRange", "withinit", "base"]`      | 100.735 ns (5%) |         |                 |             |
| `["filter_sum", "1000", "UnitRange", "withinit", "naive"]`     | 900.052 ns (5%) |         |                 |             |
| `["filter_sum", "1000", "UnitRange", "withinit", "xf"]`        | 134.056 ns (5%) |         |                 |             |
| `["filter_sum", "10000", "RandomFloats", "noinit", "base"]`    |  45.303 μs (5%) |         |                 |             |
| `["filter_sum", "10000", "RandomFloats", "noinit", "naive"]`   |  44.802 μs (5%) |         |                 |             |
| `["filter_sum", "10000", "RandomFloats", "noinit", "xf"]`      |  17.501 μs (5%) |         |                 |             |
| `["filter_sum", "10000", "RandomFloats", "withinit", "base"]`  |  17.101 μs (5%) |         |                 |             |
| `["filter_sum", "10000", "RandomFloats", "withinit", "naive"]` |  49.103 μs (5%) |         |                 |             |
| `["filter_sum", "10000", "RandomFloats", "withinit", "xf"]`    |  15.100 μs (5%) |         |                 |             |
| `["filter_sum", "10000", "UnitRange", "noinit", "base"]`       |  20.001 μs (5%) |         |                 |             |
| `["filter_sum", "10000", "UnitRange", "noinit", "naive"]`      |  11.334 μs (5%) |         |                 |             |
| `["filter_sum", "10000", "UnitRange", "noinit", "xf"]`         |   1.294 μs (5%) |         |                 |             |
| `["filter_sum", "10000", "UnitRange", "withinit", "base"]`     |   1.108 μs (5%) |         |                 |             |
| `["filter_sum", "10000", "UnitRange", "withinit", "naive"]`    |  10.221 μs (5%) |         |                 |             |
| `["filter_sum", "10000", "UnitRange", "withinit", "xf"]`       |   1.294 μs (5%) |         |                 |             |
| `["findall", "base"]`                                          | 711.644 μs (5%) |         |   2.00 MiB (1%) |          18 |
| `["findall", "xf-array"]`                                      | 664.240 μs (5%) |         |   3.02 MiB (1%) |       98829 |
| `["findall", "xf-iter"]`                                       | 303.119 μs (5%) |         |   2.00 MiB (1%) |          19 |
| `["gemm", "fusedmul", "blas", "16"]`                           |   3.010 ms (5%) |         |                 |             |
| `["gemm", "fusedmul", "blas", "2"]`                            |   2.446 ms (5%) |         |                 |             |
| `["gemm", "fusedmul", "blas", "32"]`                           |   3.668 ms (5%) |         |                 |             |
| `["gemm", "fusedmul", "blas", "8"]`                            |   2.666 ms (5%) |         |                 |             |
| `["gemm", "fusedmul", "xf", "16"]`                             |   4.640 ms (5%) |         |  192 bytes (1%) |           4 |
| `["gemm", "fusedmul", "xf", "2"]`                              | 573.964 μs (5%) |         |  192 bytes (1%) |           4 |
| `["gemm", "fusedmul", "xf", "32"]`                             |   9.950 ms (5%) |         |  192 bytes (1%) |           4 |
| `["gemm", "fusedmul", "xf", "8"]`                              |   2.470 ms (5%) |         |  192 bytes (1%) |           4 |
| `["gemm", "mul", "linalg", "256"]`                             | 401.752 μs (5%) |         |                 |             |
| `["gemm", "mul", "linalg", "32"]`                              |   2.000 μs (5%) |         |                 |             |
| `["gemm", "mul", "linalg", "8"]`                               | 200.000 ns (5%) |         |                 |             |
| `["gemm", "mul", "man", "false", "256"]`                       |   1.454 ms (5%) |         |                 |             |
| `["gemm", "mul", "man", "false", "32"]`                        |   5.400 μs (5%) |         |                 |             |
| `["gemm", "mul", "man", "false", "8"]`                         | 400.000 ns (5%) |         |                 |             |
| `["gemm", "mul", "man", "ivdep", "256"]`                       |   1.427 ms (5%) |         |                 |             |
| `["gemm", "mul", "man", "ivdep", "32"]`                        |   3.200 μs (5%) |         |                 |             |
| `["gemm", "mul", "man", "ivdep", "8"]`                         | 300.000 ns (5%) |         |                 |             |
| `["gemm", "mul", "man", "true", "256"]`                        |   1.441 ms (5%) |         |                 |             |
| `["gemm", "mul", "man", "true", "32"]`                         |   4.000 μs (5%) |         |                 |             |
| `["gemm", "mul", "man", "true", "8"]`                          | 300.000 ns (5%) |         |                 |             |
| `["gemm", "mul", "xf", "false", "256"]`                        |   1.451 ms (5%) |         |   80 bytes (1%) |           3 |
| `["gemm", "mul", "xf", "false", "32"]`                         |   3.900 μs (5%) |         |   80 bytes (1%) |           3 |
| `["gemm", "mul", "xf", "false", "8"]`                          | 300.000 ns (5%) |         |   80 bytes (1%) |           3 |
| `["gemm", "mul", "xf", "ivdep", "256"]`                        |   1.427 ms (5%) |         |   80 bytes (1%) |           3 |
| `["gemm", "mul", "xf", "ivdep", "32"]`                         |   3.700 μs (5%) |         |   80 bytes (1%) |           3 |
| `["gemm", "mul", "xf", "ivdep", "8"]`                          | 300.000 ns (5%) |         |   80 bytes (1%) |           3 |
| `["gemm", "mul", "xf", "true", "256"]`                         |   1.449 ms (5%) |         |   80 bytes (1%) |           3 |
| `["gemm", "mul", "xf", "true", "32"]`                          |   4.100 μs (5%) |         |   80 bytes (1%) |           3 |
| `["gemm", "mul", "xf", "true", "8"]`                           | 400.000 ns (5%) |         |   80 bytes (1%) |           3 |
| `["groupby", "sum", "sac"]`                                    | 169.218 μs (5%) |         |  624 bytes (1%) |           5 |
| `["groupby", "sum", "xf-with-init"]`                           | 140.015 μs (5%) |         |   1.20 KiB (1%) |           9 |
| `["groupby", "sum", "xf-without-init"]`                        | 140.515 μs (5%) |         |   1.20 KiB (1%) |           9 |
| `["mapcat_eduction", "base"]`                                  |   1.567 μs (5%) |         |                 |             |
| `["mapcat_eduction", "xf-eduction"]`                           |   1.630 μs (5%) |         |                 |             |
| `["mapcat_eduction", "xf-xf"]`                                 |   1.400 μs (5%) |         |                 |             |
| `["missing_argmax", "man"]`                                    |   2.233 μs (5%) |         |   32 bytes (1%) |           1 |
| `["missing_argmax", "rf"]`                                     |   1.750 μs (5%) |         |   32 bytes (1%) |           1 |
| `["missing_argmax", "xf"]`                                     |   1.810 μs (5%) |         |   32 bytes (1%) |           1 |
| `["missing_dot", "equiv"]`                                     |   1.530 μs (5%) |         |   16 bytes (1%) |           1 |
| `["missing_dot", "man"]`                                       |   1.190 μs (5%) |         |   16 bytes (1%) |           1 |
| `["missing_dot", "naive"]`                                     |   4.067 μs (5%) |         |   16 bytes (1%) |           1 |
| `["missing_dot", "rf"]`                                        |   1.350 μs (5%) |         |   16 bytes (1%) |           1 |
| `["missing_dot", "rf_nota"]`                                   |   1.160 μs (5%) |         |   16 bytes (1%) |           1 |
| `["missing_dot", "xf"]`                                        |  84.612 μs (5%) |         |  72.08 KiB (1%) |        3740 |
| `["missing_dot", "xf_nota"]`                                   |  85.305 μs (5%) |         |  72.31 KiB (1%) |        3750 |
| `["overhead", "foldl"]`                                        |   4.500 ns (5%) |         |                 |             |
| `["overhead", "reduce_basecase"]`                              | 214.648 ns (5%) |         |  368 bytes (1%) |           6 |
| `["partition_by", "man"]`                                      |   2.389 ms (5%) |         |  352 bytes (1%) |           4 |
| `["partition_by", "xf"]`                                       |   2.351 ms (5%) |         |  544 bytes (1%) |           6 |
| `["set", "base"]`                                              |   4.376 ms (5%) |         |  49.56 KiB (1%) |          17 |
| `["set", "xf"]`                                                |   4.109 ms (5%) |         |  49.59 KiB (1%) |          19 |
| `["sum_transpose", "30", "noinit", "iter"]`                    |   2.180 μs (5%) |         |                 |             |
| `["sum_transpose", "30", "noinit", "man"]`                     |   2.122 μs (5%) |         |                 |             |
| `["sum_transpose", "30", "noinit", "xf"]`                      |   1.230 μs (5%) |         |   32 bytes (1%) |           2 |
| `["sum_transpose", "30", "withinit", "iter"]`                  |   1.510 μs (5%) |         |                 |             |
| `["sum_transpose", "30", "withinit", "man"]`                   |   1.110 μs (5%) |         |                 |             |
| `["sum_transpose", "30", "withinit", "xf"]`                    |   1.190 μs (5%) |         |   48 bytes (1%) |           3 |
| `["teerf_filter", "noinit"]`                                   | 389.187 ns (5%) |         |  112 bytes (1%) |           4 |
| `["teerf_filter", "withinit"]`                                 | 163.424 ns (5%) |         |                 |             |

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
Julia Version 1.5.0
Commit 96786e22cc (2020-08-01 23:44 UTC)
Platform Info:
  OS: Linux (x86_64-pc-linux-gnu)
      Ubuntu 18.04.4 LTS
  uname: Linux 5.3.0-1034-azure #35~18.04.1-Ubuntu SMP Mon Jul 13 12:54:45 UTC 2020 x86_64 x86_64
  CPU: Intel(R) Xeon(R) Platinum 8171M CPU @ 2.60GHz: 
              speed         user         nice          sys         idle          irq
       #1  2095 MHz      93488 s          0 s       1772 s      17352 s          0 s
       #2  2095 MHz      15924 s          0 s       1794 s      95496 s          0 s
       
  Memory: 6.764881134033203 GB (2515.1328125 MB free)
  Uptime: 1153.0 sec
  Load Avg:  1.0107421875  1.00634765625  0.80712890625
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
    CPU MHz:             2095.242
    BogoMIPS:            4190.48
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

