# Benchmark result

* Pull request commit: [`c7060ec6c36737281a2a7ab80955ac3155996c27`](https://github.com/JuliaFolds/Transducers.jl/commit/c7060ec6c36737281a2a7ab80955ac3155996c27)
* Pull request: <https://github.com/JuliaFolds/Transducers.jl/pull/243> (Update */Manifest.toml)

# Judge result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmarks:
    - Target: 27 Oct 2020 - 01:17
    - Baseline: 27 Oct 2020 - 01:23
* Package commits:
    - Target: 134d70
    - Baseline: da98f2
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
| `["append!!", "eduction"]`                                     |                1.05 (5%) :x: |    1.00 (1%)  |
| `["append!!", "xf"]`                                           |                1.12 (5%) :x: |    1.00 (1%)  |
| `["cartesian", "copyto!", "man"]`                              |                1.42 (5%) :x: |    1.00 (1%)  |
| `["cartesian", "copyto!", "xf"]`                               |                1.12 (5%) :x: |    1.00 (1%)  |
| `["cat", "base"]`                                              |                1.08 (5%) :x: |    1.00 (1%)  |
| `["cat", "xf"]`                                                |                1.33 (5%) :x: |    1.00 (1%)  |
| `["collect", "filter-missing"]`                                |                1.13 (5%) :x: |    1.00 (1%)  |
| `["collect", "identity-union"]`                                |                1.15 (5%) :x: |    1.00 (1%)  |
| `["dict", "base"]`                                             |                1.09 (5%) :x: |    1.00 (1%)  |
| `["dict", "xf"]`                                               |                1.10 (5%) :x: |    1.00 (1%)  |
| `["dot", "blas"]`                                              |                1.18 (5%) :x: |    1.00 (1%)  |
| `["dot", "man"]`                                               |                1.13 (5%) :x: |    1.00 (1%)  |
| `["filter_map_map!", "xf"]`                                    |                1.18 (5%) :x: |    1.00 (1%)  |
| `["filter_map_reduce", "man"]`                                 |                1.33 (5%) :x: |    1.00 (1%)  |
| `["filter_map_reduce", "xf"]`                                  |                1.18 (5%) :x: |    1.00 (1%)  |
| `["filter_sum", "1000", "RandomFloats", "noinit", "base"]`     | 0.85 (5%) :white_check_mark: |    1.00 (1%)  |
| `["filter_sum", "1000", "RandomFloats", "noinit", "naive"]`    |                1.16 (5%) :x: |    1.00 (1%)  |
| `["filter_sum", "1000", "RandomFloats", "withinit", "naive"]`  | 0.82 (5%) :white_check_mark: |    1.00 (1%)  |
| `["filter_sum", "1000", "RandomFloats", "withinit", "xf"]`     |                1.25 (5%) :x: |    1.00 (1%)  |
| `["filter_sum", "1000", "UnitRange", "noinit", "naive"]`       |                1.14 (5%) :x: |    1.00 (1%)  |
| `["filter_sum", "1000", "UnitRange", "noinit", "xf"]`          |                1.16 (5%) :x: |    1.00 (1%)  |
| `["filter_sum", "1000", "UnitRange", "withinit", "base"]`      |                1.16 (5%) :x: |    1.00 (1%)  |
| `["filter_sum", "1000", "UnitRange", "withinit", "naive"]`     |                1.16 (5%) :x: |    1.00 (1%)  |
| `["filter_sum", "10000", "RandomFloats", "noinit", "xf"]`      |                1.14 (5%) :x: |    1.00 (1%)  |
| `["filter_sum", "10000", "RandomFloats", "withinit", "base"]`  |                1.17 (5%) :x: |    1.00 (1%)  |
| `["filter_sum", "10000", "RandomFloats", "withinit", "naive"]` | 0.89 (5%) :white_check_mark: |    1.00 (1%)  |
| `["filter_sum", "10000", "UnitRange", "noinit", "base"]`       | 0.94 (5%) :white_check_mark: |    1.00 (1%)  |
| `["filter_sum", "10000", "UnitRange", "noinit", "naive"]`      |                1.25 (5%) :x: |    1.00 (1%)  |
| `["filter_sum", "10000", "UnitRange", "noinit", "xf"]`         | 0.93 (5%) :white_check_mark: |    1.00 (1%)  |
| `["filter_sum", "10000", "UnitRange", "withinit", "xf"]`       |                1.14 (5%) :x: |    1.00 (1%)  |
| `["findall", "base"]`                                          |                1.38 (5%) :x: |    1.00 (1%)  |
| `["findall", "xf-array"]`                                      |                1.08 (5%) :x: |    1.00 (1%)  |
| `["findall", "xf-iter"]`                                       |                1.26 (5%) :x: |    1.00 (1%)  |
| `["gemm", "fusedmul", "blas", "2"]`                            |                1.05 (5%) :x: |    1.00 (1%)  |
| `["gemm", "fusedmul", "blas", "32"]`                           |                1.09 (5%) :x: |    1.00 (1%)  |
| `["gemm", "fusedmul", "blas", "8"]`                            |                1.08 (5%) :x: |    1.00 (1%)  |
| `["gemm", "mul", "linalg", "256"]`                             |                1.12 (5%) :x: |    1.00 (1%)  |
| `["gemm", "mul", "linalg", "32"]`                              |                1.26 (5%) :x: |    1.00 (1%)  |
| `["gemm", "mul", "linalg", "8"]`                               |                1.15 (5%) :x: |    1.00 (1%)  |
| `["gemm", "mul", "man", "false", "256"]`                       |                1.22 (5%) :x: |    1.00 (1%)  |
| `["gemm", "mul", "man", "false", "8"]`                         |                1.12 (5%) :x: |    1.00 (1%)  |
| `["gemm", "mul", "man", "ivdep", "256"]`                       |                1.18 (5%) :x: |    1.00 (1%)  |
| `["gemm", "mul", "man", "ivdep", "32"]`                        | 0.85 (5%) :white_check_mark: |    1.00 (1%)  |
| `["gemm", "mul", "man", "true", "256"]`                        |                1.23 (5%) :x: |    1.00 (1%)  |
| `["gemm", "mul", "man", "true", "32"]`                         |                1.09 (5%) :x: |    1.00 (1%)  |
| `["gemm", "mul", "man", "true", "8"]`                          |                1.15 (5%) :x: |    1.00 (1%)  |
| `["gemm", "mul", "xf", "false", "256"]`                        |                1.17 (5%) :x: |    1.00 (1%)  |
| `["gemm", "mul", "xf", "false", "32"]`                         | 0.87 (5%) :white_check_mark: |    1.00 (1%)  |
| `["gemm", "mul", "xf", "false", "8"]`                          |                1.42 (5%) :x: |    1.00 (1%)  |
| `["gemm", "mul", "xf", "ivdep", "256"]`                        |                1.19 (5%) :x: |    1.00 (1%)  |
| `["gemm", "mul", "xf", "ivdep", "32"]`                         |                1.09 (5%) :x: |    1.00 (1%)  |
| `["gemm", "mul", "xf", "ivdep", "8"]`                          |                1.53 (5%) :x: |    1.00 (1%)  |
| `["gemm", "mul", "xf", "true", "256"]`                         |                1.25 (5%) :x: |    1.00 (1%)  |
| `["gemm", "mul", "xf", "true", "32"]`                          | 0.89 (5%) :white_check_mark: |    1.00 (1%)  |
| `["gemm", "mul", "xf", "true", "8"]`                           |                1.20 (5%) :x: |    1.00 (1%)  |
| `["groupby", "sum", "sac"]`                                    | 0.74 (5%) :white_check_mark: | 2.51 (1%) :x: |
| `["groupby", "sum", "xf-with-init"]`                           | 0.94 (5%) :white_check_mark: |    1.00 (1%)  |
| `["groupby", "sum", "xf-without-init"]`                        | 0.93 (5%) :white_check_mark: |    1.00 (1%)  |
| `["mapcat_eduction", "base"]`                                  |                1.34 (5%) :x: |    1.00 (1%)  |
| `["mapcat_eduction", "xf-eduction"]`                           |                1.38 (5%) :x: |    1.00 (1%)  |
| `["mapcat_eduction", "xf-xf"]`                                 |                1.34 (5%) :x: |    1.00 (1%)  |
| `["missing_argmax", "man"]`                                    | 0.87 (5%) :white_check_mark: |    1.00 (1%)  |
| `["missing_argmax", "xf"]`                                     |                1.08 (5%) :x: |    1.00 (1%)  |
| `["missing_dot", "equiv"]`                                     |                1.12 (5%) :x: |    1.00 (1%)  |
| `["missing_dot", "man"]`                                       |                1.35 (5%) :x: |    1.00 (1%)  |
| `["missing_dot", "naive"]`                                     |                1.18 (5%) :x: |    1.00 (1%)  |
| `["missing_dot", "rf"]`                                        |                1.35 (5%) :x: |    1.00 (1%)  |
| `["missing_dot", "rf_nota"]`                                   |                1.18 (5%) :x: |    1.00 (1%)  |
| `["missing_dot", "xf"]`                                        |                1.27 (5%) :x: |    1.00 (1%)  |
| `["missing_dot", "xf_nota"]`                                   |                1.20 (5%) :x: |    1.00 (1%)  |
| `["overhead", "foldl"]`                                        |                1.15 (5%) :x: |    1.00 (1%)  |
| `["partition_by", "xf"]`                                       |                1.14 (5%) :x: |    1.00 (1%)  |
| `["set", "base"]`                                              |                1.09 (5%) :x: |    1.00 (1%)  |
| `["set", "xf"]`                                                |                1.16 (5%) :x: |    1.00 (1%)  |
| `["sum_transpose", "30", "noinit", "iter"]`                    |                1.15 (5%) :x: |    1.00 (1%)  |
| `["sum_transpose", "30", "noinit", "xf"]`                      |                1.15 (5%) :x: |    1.00 (1%)  |
| `["sum_transpose", "30", "withinit", "iter"]`                  |                1.15 (5%) :x: |    1.00 (1%)  |
| `["sum_transpose", "30", "withinit", "xf"]`                    |                1.15 (5%) :x: |    1.00 (1%)  |
| `["teerf_filter", "noinit"]`                                   |                1.15 (5%) :x: |    1.00 (1%)  |
| `["teerf_filter", "withinit"]`                                 |                1.15 (5%) :x: |    1.00 (1%)  |

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
  uname: Linux 5.4.0-1031-azure #32~18.04.1-Ubuntu SMP Tue Oct 6 10:03:22 UTC 2020 x86_64 x86_64
  CPU: Intel(R) Xeon(R) Platinum 8171M CPU @ 2.60GHz: 
              speed         user         nice          sys         idle          irq
       #1  2095 MHz      23342 s          0 s       1666 s      55726 s          0 s
       #2  2095 MHz      53978 s          0 s       1472 s      25775 s          0 s
       
  Memory: 6.764892578125 GB (3275.98046875 MB free)
  Uptime: 829.0 sec
  Load Avg:  1.0029296875  0.98291015625  0.6640625
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-9.0.1 (ORCJIT, skylake-avx512)
```

### Baseline
```
Julia Version 1.5.2
Commit 539f3ce943 (2020-09-23 23:17 UTC)
Platform Info:
  OS: Linux (x86_64-pc-linux-gnu)
      Ubuntu 18.04.5 LTS
  uname: Linux 5.4.0-1031-azure #32~18.04.1-Ubuntu SMP Tue Oct 6 10:03:22 UTC 2020 x86_64 x86_64
  CPU: Intel(R) Xeon(R) Platinum 8171M CPU @ 2.60GHz: 
              speed         user         nice          sys         idle          irq
       #1  2095 MHz      28598 s          0 s       1962 s      83119 s          0 s
       #2  2095 MHz      81272 s          0 s       1723 s      31177 s          0 s
       
  Memory: 6.764892578125 GB (3103.1796875 MB free)
  Uptime: 1161.0 sec
  Load Avg:  1.0  1.0  0.77685546875
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-9.0.1 (ORCJIT, skylake-avx512)
```

---
# Target result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmark: 27 Oct 2020 - 1:17
* Package commit: 134d70
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
| `["append!!", "eduction"]`                                     |  18.902 μs (5%) |         |  64.63 KiB (1%) |          13 |
| `["append!!", "xf"]`                                           |  20.101 μs (5%) |         |  64.63 KiB (1%) |          13 |
| `["cartesian", "copyto!", "iter"]`                             |   5.800 μs (5%) |         |                 |             |
| `["cartesian", "copyto!", "man"]`                              |   3.250 μs (5%) |         |                 |             |
| `["cartesian", "copyto!", "xf"]`                               |   3.800 μs (5%) |         |                 |             |
| `["cat", "base"]`                                              |   2.422 μs (5%) |         |                 |             |
| `["cat", "xf"]`                                                |   1.840 μs (5%) |         |                 |             |
| `["collect", "filter-missing"]`                                |  71.103 μs (5%) |         |  32.81 KiB (1%) |          14 |
| `["collect", "identity-float"]`                                |  29.801 μs (5%) |         | 256.66 KiB (1%) |          14 |
| `["collect", "identity-union"]`                                | 170.609 μs (5%) |         | 601.04 KiB (1%) |       10013 |
| `["dict", "base"]`                                             |   4.414 ms (5%) |         |  92.91 KiB (1%) |          22 |
| `["dict", "xf"]`                                               |   4.552 ms (5%) |         |  92.31 KiB (1%) |          18 |
| `["dot", "blas"]`                                              |   1.360 μs (5%) |         |                 |             |
| `["dot", "man"]`                                               |   1.280 μs (5%) |         |                 |             |
| `["dot", "rf"]`                                                |   2.111 μs (5%) |         |                 |             |
| `["dot", "xf"]`                                                |   2.200 μs (5%) |         |   64 bytes (1%) |           3 |
| `["filter_map_map!", "man"]`                                   |  53.702 μs (5%) |         |                 |             |
| `["filter_map_map!", "xf"]`                                    | 690.727 μs (5%) |         |   80 bytes (1%) |           3 |
| `["filter_map_reduce", "man"]`                                 | 255.513 μs (5%) |         |                 |             |
| `["filter_map_reduce", "xf"]`                                  | 226.111 μs (5%) |         |                 |             |
| `["filter_sum", "1000", "RandomFloats", "noinit", "base"]`     |   1.060 μs (5%) |         |                 |             |
| `["filter_sum", "1000", "RandomFloats", "noinit", "naive"]`    |   1.240 μs (5%) |         |                 |             |
| `["filter_sum", "1000", "RandomFloats", "noinit", "xf"]`       |   1.720 μs (5%) |         |                 |             |
| `["filter_sum", "1000", "RandomFloats", "withinit", "base"]`   |   1.710 μs (5%) |         |                 |             |
| `["filter_sum", "1000", "RandomFloats", "withinit", "naive"]`  | 727.303 ns (5%) |         |                 |             |
| `["filter_sum", "1000", "RandomFloats", "withinit", "xf"]`     |   2.130 μs (5%) |         |                 |             |
| `["filter_sum", "1000", "UnitRange", "noinit", "base"]`        |   1.756 μs (5%) |         |                 |             |
| `["filter_sum", "1000", "UnitRange", "noinit", "naive"]`       |   1.310 μs (5%) |         |                 |             |
| `["filter_sum", "1000", "UnitRange", "noinit", "xf"]`          | 117.417 ns (5%) |         |                 |             |
| `["filter_sum", "1000", "UnitRange", "withinit", "base"]`      | 100.748 ns (5%) |         |                 |             |
| `["filter_sum", "1000", "UnitRange", "withinit", "naive"]`     | 900.048 ns (5%) |         |                 |             |
| `["filter_sum", "1000", "UnitRange", "withinit", "xf"]`        | 100.708 ns (5%) |         |                 |             |
| `["filter_sum", "10000", "RandomFloats", "noinit", "base"]`    |  41.002 μs (5%) |         |                 |             |
| `["filter_sum", "10000", "RandomFloats", "noinit", "naive"]`   |  51.203 μs (5%) |         |                 |             |
| `["filter_sum", "10000", "RandomFloats", "noinit", "xf"]`      |  20.001 μs (5%) |         |                 |             |
| `["filter_sum", "10000", "RandomFloats", "withinit", "base"]`  |  20.101 μs (5%) |         |                 |             |
| `["filter_sum", "10000", "RandomFloats", "withinit", "naive"]` |  43.902 μs (5%) |         |                 |             |
| `["filter_sum", "10000", "RandomFloats", "withinit", "xf"]`    |  17.501 μs (5%) |         |                 |             |
| `["filter_sum", "10000", "UnitRange", "noinit", "base"]`       |  20.001 μs (5%) |         |                 |             |
| `["filter_sum", "10000", "UnitRange", "noinit", "naive"]`      |  14.100 μs (5%) |         |                 |             |
| `["filter_sum", "10000", "UnitRange", "noinit", "xf"]`         |   1.300 μs (5%) |         |                 |             |
| `["filter_sum", "10000", "UnitRange", "withinit", "base"]`     | 963.211 ns (5%) |         |                 |             |
| `["filter_sum", "10000", "UnitRange", "withinit", "naive"]`    |   8.900 μs (5%) |         |                 |             |
| `["filter_sum", "10000", "UnitRange", "withinit", "xf"]`       |   1.290 μs (5%) |         |                 |             |
| `["findall", "base"]`                                          |   1.113 ms (5%) |         |   2.00 MiB (1%) |          18 |
| `["findall", "xf-array"]`                                      | 900.844 μs (5%) |         |   3.02 MiB (1%) |       98829 |
| `["findall", "xf-iter"]`                                       | 406.320 μs (5%) |         |   2.00 MiB (1%) |          19 |
| `["gemm", "fusedmul", "blas", "16"]`                           |   3.032 ms (5%) |         |                 |             |
| `["gemm", "fusedmul", "blas", "2"]`                            |   2.486 ms (5%) |         |                 |             |
| `["gemm", "fusedmul", "blas", "32"]`                           |   4.067 ms (5%) |         |                 |             |
| `["gemm", "fusedmul", "blas", "8"]`                            |   2.833 ms (5%) |         |                 |             |
| `["gemm", "fusedmul", "xf", "16"]`                             |   3.785 ms (5%) |         |  192 bytes (1%) |           4 |
| `["gemm", "fusedmul", "xf", "2"]`                              | 461.018 μs (5%) |         |  192 bytes (1%) |           4 |
| `["gemm", "fusedmul", "xf", "32"]`                             |   8.327 ms (5%) |         |  192 bytes (1%) |           4 |
| `["gemm", "fusedmul", "xf", "8"]`                              |   2.111 ms (5%) |         |  192 bytes (1%) |           4 |
| `["gemm", "mul", "linalg", "256"]`                             | 446.920 μs (5%) |         |                 |             |
| `["gemm", "mul", "linalg", "32"]`                              |   2.020 μs (5%) |         |                 |             |
| `["gemm", "mul", "linalg", "8"]`                               | 229.963 ns (5%) |         |                 |             |
| `["gemm", "mul", "man", "false", "256"]`                       |   1.634 ms (5%) |         |                 |             |
| `["gemm", "mul", "man", "false", "32"]`                        |   4.686 μs (5%) |         |                 |             |
| `["gemm", "mul", "man", "false", "8"]`                         | 335.163 ns (5%) |         |                 |             |
| `["gemm", "mul", "man", "ivdep", "256"]`                       |   1.611 ms (5%) |         |                 |             |
| `["gemm", "mul", "man", "ivdep", "32"]`                        |   3.550 μs (5%) |         |                 |             |
| `["gemm", "mul", "man", "ivdep", "8"]`                         | 302.867 ns (5%) |         |                 |             |
| `["gemm", "mul", "man", "true", "256"]`                        |   1.642 ms (5%) |         |                 |             |
| `["gemm", "mul", "man", "true", "32"]`                         |   4.472 μs (5%) |         |                 |             |
| `["gemm", "mul", "man", "true", "8"]`                          | 460.929 ns (5%) |         |                 |             |
| `["gemm", "mul", "xf", "false", "256"]`                        |   1.579 ms (5%) |         |   80 bytes (1%) |           3 |
| `["gemm", "mul", "xf", "false", "32"]`                         |   4.767 μs (5%) |         |   80 bytes (1%) |           3 |
| `["gemm", "mul", "xf", "false", "8"]`                          | 425.144 ns (5%) |         |   80 bytes (1%) |           3 |
| `["gemm", "mul", "xf", "ivdep", "256"]`                        |   1.619 ms (5%) |         |   80 bytes (1%) |           3 |
| `["gemm", "mul", "xf", "ivdep", "32"]`                         |   3.600 μs (5%) |         |   80 bytes (1%) |           3 |
| `["gemm", "mul", "xf", "ivdep", "8"]`                          | 460.426 ns (5%) |         |   80 bytes (1%) |           3 |
| `["gemm", "mul", "xf", "true", "256"]`                         |   1.684 ms (5%) |         |   80 bytes (1%) |           3 |
| `["gemm", "mul", "xf", "true", "32"]`                          |   5.343 μs (5%) |         |   80 bytes (1%) |           3 |
| `["gemm", "mul", "xf", "true", "8"]`                           | 481.930 ns (5%) |         |   80 bytes (1%) |           3 |
| `["groupby", "sum", "sac"]`                                    | 140.605 μs (5%) |         |   1.53 KiB (1%) |          16 |
| `["groupby", "sum", "xf-with-init"]`                           | 152.206 μs (5%) |         |   1.20 KiB (1%) |           9 |
| `["groupby", "sum", "xf-without-init"]`                        | 131.705 μs (5%) |         |   1.20 KiB (1%) |           9 |
| `["mapcat_eduction", "base"]`                                  |   2.100 μs (5%) |         |                 |             |
| `["mapcat_eduction", "xf-eduction"]`                           |   1.920 μs (5%) |         |                 |             |
| `["mapcat_eduction", "xf-xf"]`                                 |   1.860 μs (5%) |         |                 |             |
| `["missing_argmax", "man"]`                                    |   2.600 μs (5%) |         |   32 bytes (1%) |           1 |
| `["missing_argmax", "rf"]`                                     |   2.080 μs (5%) |         |   32 bytes (1%) |           1 |
| `["missing_argmax", "xf"]`                                     |   2.010 μs (5%) |         |   32 bytes (1%) |           1 |
| `["missing_dot", "equiv"]`                                     |   1.540 μs (5%) |         |   16 bytes (1%) |           1 |
| `["missing_dot", "man"]`                                       |   1.580 μs (5%) |         |   16 bytes (1%) |           1 |
| `["missing_dot", "naive"]`                                     |   4.784 μs (5%) |         |   16 bytes (1%) |           1 |
| `["missing_dot", "rf"]`                                        |   1.580 μs (5%) |         |   16 bytes (1%) |           1 |
| `["missing_dot", "rf_nota"]`                                   |   1.360 μs (5%) |         |   16 bytes (1%) |           1 |
| `["missing_dot", "xf"]`                                        | 103.305 μs (5%) |         |  72.14 KiB (1%) |        3742 |
| `["missing_dot", "xf_nota"]`                                   |  99.005 μs (5%) |         |  72.23 KiB (1%) |        3746 |
| `["overhead", "foldl"]`                                        |   6.000 ns (5%) |         |                 |             |
| `["overhead", "reduce_basecase"]`                              | 291.055 ns (5%) |         |  368 bytes (1%) |           6 |
| `["partition_by", "man"]`                                      |   2.253 ms (5%) |         |  352 bytes (1%) |           4 |
| `["partition_by", "xf"]`                                       |   2.460 ms (5%) |         |  544 bytes (1%) |           6 |
| `["set", "base"]`                                              |   4.727 ms (5%) |         |  49.56 KiB (1%) |          17 |
| `["set", "xf"]`                                                |   4.953 ms (5%) |         |  49.59 KiB (1%) |          19 |
| `["sum_transpose", "30", "noinit", "iter"]`                    |   2.511 μs (5%) |         |                 |             |
| `["sum_transpose", "30", "noinit", "man"]`                     |   2.833 μs (5%) |         |                 |             |
| `["sum_transpose", "30", "noinit", "xf"]`                      |   1.410 μs (5%) |         |   32 bytes (1%) |           2 |
| `["sum_transpose", "30", "withinit", "iter"]`                  |   2.010 μs (5%) |         |                 |             |
| `["sum_transpose", "30", "withinit", "man"]`                   |   1.280 μs (5%) |         |                 |             |
| `["sum_transpose", "30", "withinit", "xf"]`                    |   1.360 μs (5%) |         |   48 bytes (1%) |           3 |
| `["teerf_filter", "noinit"]`                                   | 446.485 ns (5%) |         |  112 bytes (1%) |           4 |
| `["teerf_filter", "withinit"]`                                 | 215.820 ns (5%) |         |                 |             |

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
  uname: Linux 5.4.0-1031-azure #32~18.04.1-Ubuntu SMP Tue Oct 6 10:03:22 UTC 2020 x86_64 x86_64
  CPU: Intel(R) Xeon(R) Platinum 8171M CPU @ 2.60GHz: 
              speed         user         nice          sys         idle          irq
       #1  2095 MHz      23342 s          0 s       1666 s      55726 s          0 s
       #2  2095 MHz      53978 s          0 s       1472 s      25775 s          0 s
       
  Memory: 6.764892578125 GB (3275.98046875 MB free)
  Uptime: 829.0 sec
  Load Avg:  1.0029296875  0.98291015625  0.6640625
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-9.0.1 (ORCJIT, skylake-avx512)
```

---
# Baseline result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmark: 27 Oct 2020 - 1:23
* Package commit: da98f2
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
| `["append!!", "eduction"]`                                     |  18.001 μs (5%) |         |  64.63 KiB (1%) |          13 |
| `["append!!", "xf"]`                                           |  18.000 μs (5%) |         |  64.63 KiB (1%) |          13 |
| `["cartesian", "copyto!", "iter"]`                             |   5.840 μs (5%) |         |                 |             |
| `["cartesian", "copyto!", "man"]`                              |   2.288 μs (5%) |         |                 |             |
| `["cartesian", "copyto!", "xf"]`                               |   3.388 μs (5%) |         |                 |             |
| `["cat", "base"]`                                              |   2.233 μs (5%) |         |                 |             |
| `["cat", "xf"]`                                                |   1.380 μs (5%) |         |                 |             |
| `["collect", "filter-missing"]`                                |  63.106 μs (5%) |         |  32.81 KiB (1%) |          14 |
| `["collect", "identity-float"]`                                |  28.601 μs (5%) |         | 256.66 KiB (1%) |          14 |
| `["collect", "identity-union"]`                                | 148.705 μs (5%) |         | 601.13 KiB (1%) |       10013 |
| `["dict", "base"]`                                             |   4.035 ms (5%) |         |  92.91 KiB (1%) |          22 |
| `["dict", "xf"]`                                               |   4.137 ms (5%) |         |  92.31 KiB (1%) |          18 |
| `["dot", "blas"]`                                              |   1.150 μs (5%) |         |                 |             |
| `["dot", "man"]`                                               |   1.130 μs (5%) |         |                 |             |
| `["dot", "rf"]`                                                |   2.067 μs (5%) |         |                 |             |
| `["dot", "xf"]`                                                |   2.133 μs (5%) |         |   64 bytes (1%) |           3 |
| `["filter_map_map!", "man"]`                                   |  51.903 μs (5%) |         |                 |             |
| `["filter_map_map!", "xf"]`                                    | 584.938 μs (5%) |         |   80 bytes (1%) |           3 |
| `["filter_map_reduce", "man"]`                                 | 191.816 μs (5%) |         |                 |             |
| `["filter_map_reduce", "xf"]`                                  | 191.716 μs (5%) |         |                 |             |
| `["filter_sum", "1000", "RandomFloats", "noinit", "base"]`     |   1.240 μs (5%) |         |                 |             |
| `["filter_sum", "1000", "RandomFloats", "noinit", "naive"]`    |   1.070 μs (5%) |         |                 |             |
| `["filter_sum", "1000", "RandomFloats", "noinit", "xf"]`       |   1.720 μs (5%) |         |                 |             |
| `["filter_sum", "1000", "RandomFloats", "withinit", "base"]`   |   1.720 μs (5%) |         |                 |             |
| `["filter_sum", "1000", "RandomFloats", "withinit", "naive"]`  | 887.909 ns (5%) |         |                 |             |
| `["filter_sum", "1000", "RandomFloats", "withinit", "xf"]`     |   1.700 μs (5%) |         |                 |             |
| `["filter_sum", "1000", "UnitRange", "noinit", "base"]`        |   1.756 μs (5%) |         |                 |             |
| `["filter_sum", "1000", "UnitRange", "noinit", "naive"]`       |   1.150 μs (5%) |         |                 |             |
| `["filter_sum", "1000", "UnitRange", "noinit", "xf"]`          | 101.149 ns (5%) |         |                 |             |
| `["filter_sum", "1000", "UnitRange", "withinit", "base"]`      |  86.853 ns (5%) |         |                 |             |
| `["filter_sum", "1000", "UnitRange", "withinit", "naive"]`     | 773.833 ns (5%) |         |                 |             |
| `["filter_sum", "1000", "UnitRange", "withinit", "xf"]`        | 100.822 ns (5%) |         |                 |             |
| `["filter_sum", "10000", "RandomFloats", "noinit", "base"]`    |  41.002 μs (5%) |         |                 |             |
| `["filter_sum", "10000", "RandomFloats", "noinit", "naive"]`   |  51.001 μs (5%) |         |                 |             |
| `["filter_sum", "10000", "RandomFloats", "noinit", "xf"]`      |  17.500 μs (5%) |         |                 |             |
| `["filter_sum", "10000", "RandomFloats", "withinit", "base"]`  |  17.200 μs (5%) |         |                 |             |
| `["filter_sum", "10000", "RandomFloats", "withinit", "naive"]` |  49.102 μs (5%) |         |                 |             |
| `["filter_sum", "10000", "RandomFloats", "withinit", "xf"]`    |  17.500 μs (5%) |         |                 |             |
| `["filter_sum", "10000", "UnitRange", "noinit", "base"]`       |  21.300 μs (5%) |         |                 |             |
| `["filter_sum", "10000", "UnitRange", "noinit", "naive"]`      |  11.300 μs (5%) |         |                 |             |
| `["filter_sum", "10000", "UnitRange", "noinit", "xf"]`         |   1.400 μs (5%) |         |                 |             |
| `["filter_sum", "10000", "UnitRange", "withinit", "base"]`     | 963.158 ns (5%) |         |                 |             |
| `["filter_sum", "10000", "UnitRange", "withinit", "naive"]`    |   8.900 μs (5%) |         |                 |             |
| `["filter_sum", "10000", "UnitRange", "withinit", "xf"]`       |   1.130 μs (5%) |         |                 |             |
| `["findall", "base"]`                                          | 804.671 μs (5%) |         |   2.00 MiB (1%) |          18 |
| `["findall", "xf-array"]`                                      | 833.773 μs (5%) |         |   3.02 MiB (1%) |       98829 |
| `["findall", "xf-iter"]`                                       | 322.827 μs (5%) |         |   2.00 MiB (1%) |          19 |
| `["gemm", "fusedmul", "blas", "16"]`                           |   2.908 ms (5%) |         |                 |             |
| `["gemm", "fusedmul", "blas", "2"]`                            |   2.362 ms (5%) |         |                 |             |
| `["gemm", "fusedmul", "blas", "32"]`                           |   3.727 ms (5%) |         |                 |             |
| `["gemm", "fusedmul", "blas", "8"]`                            |   2.617 ms (5%) |         |                 |             |
| `["gemm", "fusedmul", "xf", "16"]`                             |   3.970 ms (5%) |         |  192 bytes (1%) |           4 |
| `["gemm", "fusedmul", "xf", "2"]`                              | 468.432 μs (5%) |         |  192 bytes (1%) |           4 |
| `["gemm", "fusedmul", "xf", "32"]`                             |   8.420 ms (5%) |         |  192 bytes (1%) |           4 |
| `["gemm", "fusedmul", "xf", "8"]`                              |   2.180 ms (5%) |         |  192 bytes (1%) |           4 |
| `["gemm", "mul", "linalg", "256"]`                             | 399.932 μs (5%) |         |                 |             |
| `["gemm", "mul", "linalg", "32"]`                              |   1.600 μs (5%) |         |                 |             |
| `["gemm", "mul", "linalg", "8"]`                               | 200.000 ns (5%) |         |                 |             |
| `["gemm", "mul", "man", "false", "256"]`                       |   1.342 ms (5%) |         |                 |             |
| `["gemm", "mul", "man", "false", "32"]`                        |   4.500 μs (5%) |         |                 |             |
| `["gemm", "mul", "man", "false", "8"]`                         | 300.000 ns (5%) |         |                 |             |
| `["gemm", "mul", "man", "ivdep", "256"]`                       |   1.363 ms (5%) |         |                 |             |
| `["gemm", "mul", "man", "ivdep", "32"]`                        |   4.200 μs (5%) |         |                 |             |
| `["gemm", "mul", "man", "ivdep", "8"]`                         | 300.000 ns (5%) |         |                 |             |
| `["gemm", "mul", "man", "true", "256"]`                        |   1.339 ms (5%) |         |                 |             |
| `["gemm", "mul", "man", "true", "32"]`                         |   4.100 μs (5%) |         |                 |             |
| `["gemm", "mul", "man", "true", "8"]`                          | 400.000 ns (5%) |         |                 |             |
| `["gemm", "mul", "xf", "false", "256"]`                        |   1.346 ms (5%) |         |   80 bytes (1%) |           3 |
| `["gemm", "mul", "xf", "false", "32"]`                         |   5.500 μs (5%) |         |   80 bytes (1%) |           3 |
| `["gemm", "mul", "xf", "false", "8"]`                          | 300.000 ns (5%) |         |   80 bytes (1%) |           3 |
| `["gemm", "mul", "xf", "ivdep", "256"]`                        |   1.365 ms (5%) |         |   80 bytes (1%) |           3 |
| `["gemm", "mul", "xf", "ivdep", "32"]`                         |   3.300 μs (5%) |         |   80 bytes (1%) |           3 |
| `["gemm", "mul", "xf", "ivdep", "8"]`                          | 300.000 ns (5%) |         |   80 bytes (1%) |           3 |
| `["gemm", "mul", "xf", "true", "256"]`                         |   1.345 ms (5%) |         |   80 bytes (1%) |           3 |
| `["gemm", "mul", "xf", "true", "32"]`                          |   6.000 μs (5%) |         |   80 bytes (1%) |           3 |
| `["gemm", "mul", "xf", "true", "8"]`                           | 400.000 ns (5%) |         |   80 bytes (1%) |           3 |
| `["groupby", "sum", "sac"]`                                    | 190.513 μs (5%) |         |  624 bytes (1%) |           5 |
| `["groupby", "sum", "xf-with-init"]`                           | 161.310 μs (5%) |         |   1.20 KiB (1%) |           9 |
| `["groupby", "sum", "xf-without-init"]`                        | 141.410 μs (5%) |         |   1.20 KiB (1%) |           9 |
| `["mapcat_eduction", "base"]`                                  |   1.570 μs (5%) |         |                 |             |
| `["mapcat_eduction", "xf-eduction"]`                           |   1.390 μs (5%) |         |                 |             |
| `["mapcat_eduction", "xf-xf"]`                                 |   1.390 μs (5%) |         |                 |             |
| `["missing_argmax", "man"]`                                    |   2.978 μs (5%) |         |   32 bytes (1%) |           1 |
| `["missing_argmax", "rf"]`                                     |   1.990 μs (5%) |         |   32 bytes (1%) |           1 |
| `["missing_argmax", "xf"]`                                     |   1.860 μs (5%) |         |   32 bytes (1%) |           1 |
| `["missing_dot", "equiv"]`                                     |   1.380 μs (5%) |         |   16 bytes (1%) |           1 |
| `["missing_dot", "man"]`                                       |   1.170 μs (5%) |         |   16 bytes (1%) |           1 |
| `["missing_dot", "naive"]`                                     |   4.067 μs (5%) |         |   16 bytes (1%) |           1 |
| `["missing_dot", "rf"]`                                        |   1.170 μs (5%) |         |   16 bytes (1%) |           1 |
| `["missing_dot", "rf_nota"]`                                   |   1.150 μs (5%) |         |   16 bytes (1%) |           1 |
| `["missing_dot", "xf"]`                                        |  81.607 μs (5%) |         |  72.16 KiB (1%) |        3744 |
| `["missing_dot", "xf_nota"]`                                   |  82.407 μs (5%) |         |  72.11 KiB (1%) |        3740 |
| `["overhead", "foldl"]`                                        |   5.200 ns (5%) |         |                 |             |
| `["overhead", "reduce_basecase"]`                              | 287.309 ns (5%) |         |  368 bytes (1%) |           6 |
| `["partition_by", "man"]`                                      |   2.193 ms (5%) |         |  352 bytes (1%) |           4 |
| `["partition_by", "xf"]`                                       |   2.167 ms (5%) |         |  544 bytes (1%) |           6 |
| `["set", "base"]`                                              |   4.337 ms (5%) |         |  49.56 KiB (1%) |          17 |
| `["set", "xf"]`                                                |   4.264 ms (5%) |         |  49.59 KiB (1%) |          19 |
| `["sum_transpose", "30", "noinit", "iter"]`                    |   2.189 μs (5%) |         |                 |             |
| `["sum_transpose", "30", "noinit", "man"]`                     |   2.833 μs (5%) |         |                 |             |
| `["sum_transpose", "30", "noinit", "xf"]`                      |   1.230 μs (5%) |         |   32 bytes (1%) |           2 |
| `["sum_transpose", "30", "withinit", "iter"]`                  |   1.750 μs (5%) |         |                 |             |
| `["sum_transpose", "30", "withinit", "man"]`                   |   1.280 μs (5%) |         |                 |             |
| `["sum_transpose", "30", "withinit", "xf"]`                    |   1.180 μs (5%) |         |   48 bytes (1%) |           3 |
| `["teerf_filter", "noinit"]`                                   | 388.399 ns (5%) |         |  112 bytes (1%) |           4 |
| `["teerf_filter", "withinit"]`                                 | 187.953 ns (5%) |         |                 |             |

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
  uname: Linux 5.4.0-1031-azure #32~18.04.1-Ubuntu SMP Tue Oct 6 10:03:22 UTC 2020 x86_64 x86_64
  CPU: Intel(R) Xeon(R) Platinum 8171M CPU @ 2.60GHz: 
              speed         user         nice          sys         idle          irq
       #1  2095 MHz      28598 s          0 s       1962 s      83119 s          0 s
       #2  2095 MHz      81272 s          0 s       1723 s      31177 s          0 s
       
  Memory: 6.764892578125 GB (3103.1796875 MB free)
  Uptime: 1161.0 sec
  Load Avg:  1.0  1.0  0.77685546875
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-9.0.1 (ORCJIT, skylake-avx512)
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

