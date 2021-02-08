# Benchmark result

* Pull request commit: [`6eca1938b953047dc614b3f0d1d4fcdfb0edbc04`](https://github.com/JuliaFolds/Transducers.jl/commit/6eca1938b953047dc614b3f0d1d4fcdfb0edbc04)
* Pull request: <https://github.com/JuliaFolds/Transducers.jl/pull/243> (Update */Manifest.toml)

# Judge result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmarks:
    - Target: 8 Feb 2021 - 01:02
    - Baseline: 8 Feb 2021 - 01:07
* Package commits:
    - Target: 99403d
    - Baseline: 6b0f22
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
| `["cartesian", "copyto!", "iter"]`                             |                1.31 (5%) :x: |    1.00 (1%)  |
| `["cartesian", "copyto!", "man"]`                              |                1.42 (5%) :x: |    1.00 (1%)  |
| `["cat", "base"]`                                              | 0.93 (5%) :white_check_mark: |    1.00 (1%)  |
| `["collect", "identity-float"]`                                |                1.14 (5%) :x: |    1.00 (1%)  |
| `["filter_map_reduce", "man"]`                                 | 0.89 (5%) :white_check_mark: |    1.00 (1%)  |
| `["filter_map_reduce", "xf"]`                                  |                1.21 (5%) :x: |    1.00 (1%)  |
| `["filter_sum", "1000", "RandomFloats", "noinit", "naive"]`    |                1.08 (5%) :x: |    1.00 (1%)  |
| `["filter_sum", "1000", "RandomFloats", "withinit", "naive"]`  |                1.12 (5%) :x: |    1.00 (1%)  |
| `["filter_sum", "1000", "UnitRange", "noinit", "naive"]`       | 0.87 (5%) :white_check_mark: |    1.00 (1%)  |
| `["filter_sum", "10000", "RandomFloats", "noinit", "base"]`    |                1.26 (5%) :x: |    1.00 (1%)  |
| `["filter_sum", "10000", "UnitRange", "noinit", "naive"]`      | 0.86 (5%) :white_check_mark: |    1.00 (1%)  |
| `["gemm", "fusedmul", "blas", "2"]`                            |                1.07 (5%) :x: |    1.00 (1%)  |
| `["gemm", "mul", "linalg", "8"]`                               |                1.15 (5%) :x: |    1.00 (1%)  |
| `["gemm", "mul", "man", "false", "8"]`                         |                1.09 (5%) :x: |    1.00 (1%)  |
| `["gemm", "mul", "man", "true", "256"]`                        | 0.93 (5%) :white_check_mark: |    1.00 (1%)  |
| `["gemm", "mul", "man", "true", "8"]`                          | 0.92 (5%) :white_check_mark: |    1.00 (1%)  |
| `["gemm", "mul", "xf", "ivdep", "8"]`                          |                1.14 (5%) :x: |    1.00 (1%)  |
| `["groupby", "sum", "sac"]`                                    | 0.92 (5%) :white_check_mark: | 2.10 (1%) :x: |
| `["groupby", "sum", "xf-with-init"]`                           |                1.34 (5%) :x: |    1.00 (1%)  |
| `["missing_dot", "equiv"]`                                     |                1.12 (5%) :x: |    1.00 (1%)  |
| `["missing_dot", "xf"]`                                        |                1.09 (5%) :x: |    1.00 (1%)  |
| `["missing_dot", "xf_nota"]`                                   |                1.15 (5%) :x: |    1.00 (1%)  |
| `["set", "xf"]`                                                | 0.93 (5%) :white_check_mark: |    1.00 (1%)  |
| `["sum_transpose", "30", "withinit", "iter"]`                  | 0.85 (5%) :white_check_mark: |    1.00 (1%)  |

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
  uname: Linux 5.4.0-1039-azure #41~18.04.1-Ubuntu SMP Mon Jan 18 14:00:01 UTC 2021 x86_64 x86_64
  CPU: Intel(R) Xeon(R) Platinum 8171M CPU @ 2.60GHz: 
              speed         user         nice          sys         idle          irq
       #1  2095 MHz      20670 s          0 s       1488 s      60152 s          0 s
       #2  2095 MHz      57636 s          0 s       1524 s      23213 s          0 s
       
  Memory: 6.791393280029297 GB (3697.453125 MB free)
  Uptime: 836.0 sec
  Load Avg:  1.0  0.9775390625  0.671875
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-9.0.1 (ORCJIT, skylake-avx512)
```

### Baseline
```
Julia Version 1.5.3
Commit 788b2c77c1 (2020-11-09 13:37 UTC)
Platform Info:
  OS: Linux (x86_64-pc-linux-gnu)
      Ubuntu 18.04.5 LTS
  uname: Linux 5.4.0-1039-azure #41~18.04.1-Ubuntu SMP Mon Jan 18 14:00:01 UTC 2021 x86_64 x86_64
  CPU: Intel(R) Xeon(R) Platinum 8171M CPU @ 2.60GHz: 
              speed         user         nice          sys         idle          irq
       #1  2095 MHz      41492 s          0 s       1678 s      70715 s          0 s
       #2  2095 MHz      68208 s          0 s       1724 s      43974 s          0 s
       
  Memory: 6.791393280029297 GB (3705.32421875 MB free)
  Uptime: 1152.0 sec
  Load Avg:  1.05078125  1.02001953125  0.79296875
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-9.0.1 (ORCJIT, skylake-avx512)
```

---
# Target result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmark: 8 Feb 2021 - 1:2
* Package commit: 99403d
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
| `["append!!", "eduction"]`                                     |  20.600 μs (5%) |         |  64.63 KiB (1%) |          13 |
| `["append!!", "xf"]`                                           |  21.400 μs (5%) |         |  64.63 KiB (1%) |          13 |
| `["cartesian", "copyto!", "iter"]`                             |   6.620 μs (5%) |         |                 |             |
| `["cartesian", "copyto!", "man"]`                              |   3.737 μs (5%) |         |                 |             |
| `["cartesian", "copyto!", "xf"]`                               |   3.775 μs (5%) |         |                 |             |
| `["cat", "base"]`                                              |   2.078 μs (5%) |         |                 |             |
| `["cat", "xf"]`                                                |   1.840 μs (5%) |         |                 |             |
| `["collect", "filter-missing"]`                                |  72.101 μs (5%) |         |  32.81 KiB (1%) |          14 |
| `["collect", "identity-float"]`                                |  30.200 μs (5%) |         | 256.66 KiB (1%) |          14 |
| `["collect", "identity-union"]`                                | 165.503 μs (5%) |         | 601.13 KiB (1%) |       10013 |
| `["dict", "base"]`                                             |   4.779 ms (5%) |         |  92.91 KiB (1%) |          22 |
| `["dict", "xf"]`                                               |   4.946 ms (5%) |         |  92.31 KiB (1%) |          18 |
| `["dot", "blas"]`                                              |   1.340 μs (5%) |         |                 |             |
| `["dot", "man"]`                                               |   1.380 μs (5%) |         |                 |             |
| `["dot", "rf"]`                                                |   2.378 μs (5%) |         |                 |             |
| `["dot", "xf"]`                                                |   2.489 μs (5%) |         |   64 bytes (1%) |           3 |
| `["filter_map_map!", "man"]`                                   |  57.801 μs (5%) |         |                 |             |
| `["filter_map_map!", "xf"]`                                    | 757.711 μs (5%) |         |   80 bytes (1%) |           3 |
| `["filter_map_reduce", "man"]`                                 | 226.503 μs (5%) |         |                 |             |
| `["filter_map_reduce", "xf"]`                                  | 255.704 μs (5%) |         |                 |             |
| `["filter_sum", "1000", "RandomFloats", "noinit", "base"]`     |   1.420 μs (5%) |         |                 |             |
| `["filter_sum", "1000", "RandomFloats", "noinit", "naive"]`    |   1.540 μs (5%) |         |                 |             |
| `["filter_sum", "1000", "RandomFloats", "noinit", "xf"]`       |   1.978 μs (5%) |         |                 |             |
| `["filter_sum", "1000", "RandomFloats", "withinit", "base"]`   |   1.978 μs (5%) |         |                 |             |
| `["filter_sum", "1000", "RandomFloats", "withinit", "naive"]`  |   1.020 μs (5%) |         |                 |             |
| `["filter_sum", "1000", "RandomFloats", "withinit", "xf"]`     |   1.980 μs (5%) |         |                 |             |
| `["filter_sum", "1000", "UnitRange", "noinit", "base"]`        |   2.011 μs (5%) |         |                 |             |
| `["filter_sum", "1000", "UnitRange", "noinit", "naive"]`       |   1.140 μs (5%) |         |                 |             |
| `["filter_sum", "1000", "UnitRange", "noinit", "xf"]`          | 135.394 ns (5%) |         |                 |             |
| `["filter_sum", "1000", "UnitRange", "withinit", "base"]`      | 117.263 ns (5%) |         |                 |             |
| `["filter_sum", "1000", "UnitRange", "withinit", "naive"]`     |   1.020 μs (5%) |         |                 |             |
| `["filter_sum", "1000", "UnitRange", "withinit", "xf"]`        | 140.852 ns (5%) |         |                 |             |
| `["filter_sum", "10000", "RandomFloats", "noinit", "base"]`    |  44.901 μs (5%) |         |                 |             |
| `["filter_sum", "10000", "RandomFloats", "noinit", "naive"]`   |  52.901 μs (5%) |         |                 |             |
| `["filter_sum", "10000", "RandomFloats", "noinit", "xf"]`      |  20.100 μs (5%) |         |                 |             |
| `["filter_sum", "10000", "RandomFloats", "withinit", "base"]`  |  20.100 μs (5%) |         |                 |             |
| `["filter_sum", "10000", "RandomFloats", "withinit", "naive"]` |  49.001 μs (5%) |         |                 |             |
| `["filter_sum", "10000", "RandomFloats", "withinit", "xf"]`    |  19.801 μs (5%) |         |                 |             |
| `["filter_sum", "10000", "UnitRange", "noinit", "base"]`       |  20.000 μs (5%) |         |                 |             |
| `["filter_sum", "10000", "UnitRange", "noinit", "naive"]`      |  11.200 μs (5%) |         |                 |             |
| `["filter_sum", "10000", "UnitRange", "noinit", "xf"]`         |   1.300 μs (5%) |         |                 |             |
| `["filter_sum", "10000", "UnitRange", "withinit", "base"]`     |   1.120 μs (5%) |         |                 |             |
| `["filter_sum", "10000", "UnitRange", "withinit", "naive"]`    |  10.100 μs (5%) |         |                 |             |
| `["filter_sum", "10000", "UnitRange", "withinit", "xf"]`       |   1.300 μs (5%) |         |                 |             |
| `["findall", "base"]`                                          | 930.917 μs (5%) |         |   2.00 MiB (1%) |          18 |
| `["findall", "xf-array"]`                                      | 833.915 μs (5%) |         |   3.02 MiB (1%) |       98829 |
| `["findall", "xf-iter"]`                                       | 374.807 μs (5%) |         |   2.00 MiB (1%) |          19 |
| `["gemm", "fusedmul", "blas", "16"]`                           |   3.572 ms (5%) |         |                 |             |
| `["gemm", "fusedmul", "blas", "2"]`                            |   2.945 ms (5%) |         |                 |             |
| `["gemm", "fusedmul", "blas", "32"]`                           |   4.559 ms (5%) |         |                 |             |
| `["gemm", "fusedmul", "blas", "8"]`                            |   3.142 ms (5%) |         |                 |             |
| `["gemm", "fusedmul", "xf", "16"]`                             |   5.822 ms (5%) |         |  192 bytes (1%) |           4 |
| `["gemm", "fusedmul", "xf", "2"]`                              | 718.411 μs (5%) |         |  192 bytes (1%) |           4 |
| `["gemm", "fusedmul", "xf", "32"]`                             |  11.739 ms (5%) |         |  192 bytes (1%) |           4 |
| `["gemm", "fusedmul", "xf", "8"]`                              |   2.898 ms (5%) |         |  192 bytes (1%) |           4 |
| `["gemm", "mul", "linalg", "256"]`                             | 521.308 μs (5%) |         |                 |             |
| `["gemm", "mul", "linalg", "32"]`                              |   2.044 μs (5%) |         |                 |             |
| `["gemm", "mul", "linalg", "8"]`                               | 229.299 ns (5%) |         |                 |             |
| `["gemm", "mul", "man", "false", "256"]`                       |   1.861 ms (5%) |         |                 |             |
| `["gemm", "mul", "man", "false", "32"]`                        |   5.633 μs (5%) |         |                 |             |
| `["gemm", "mul", "man", "false", "8"]`                         | 434.854 ns (5%) |         |                 |             |
| `["gemm", "mul", "man", "ivdep", "256"]`                       |   1.881 ms (5%) |         |                 |             |
| `["gemm", "mul", "man", "ivdep", "32"]`                        |   4.071 μs (5%) |         |                 |             |
| `["gemm", "mul", "man", "ivdep", "8"]`                         | 401.505 ns (5%) |         |                 |             |
| `["gemm", "mul", "man", "true", "256"]`                        |   1.762 ms (5%) |         |                 |             |
| `["gemm", "mul", "man", "true", "32"]`                         |   5.417 μs (5%) |         |                 |             |
| `["gemm", "mul", "man", "true", "8"]`                          | 369.854 ns (5%) |         |                 |             |
| `["gemm", "mul", "xf", "false", "256"]`                        |   1.861 ms (5%) |         |   80 bytes (1%) |           3 |
| `["gemm", "mul", "xf", "false", "32"]`                         |   5.500 μs (5%) |         |   80 bytes (1%) |           3 |
| `["gemm", "mul", "xf", "false", "8"]`                          | 486.093 ns (5%) |         |   80 bytes (1%) |           3 |
| `["gemm", "mul", "xf", "ivdep", "256"]`                        |   1.866 ms (5%) |         |   80 bytes (1%) |           3 |
| `["gemm", "mul", "xf", "ivdep", "32"]`                         |   4.114 μs (5%) |         |   80 bytes (1%) |           3 |
| `["gemm", "mul", "xf", "ivdep", "8"]`                          | 572.425 ns (5%) |         |   80 bytes (1%) |           3 |
| `["gemm", "mul", "xf", "true", "256"]`                         |   1.836 ms (5%) |         |   80 bytes (1%) |           3 |
| `["gemm", "mul", "xf", "true", "32"]`                          |   5.529 μs (5%) |         |   80 bytes (1%) |           3 |
| `["gemm", "mul", "xf", "true", "8"]`                           | 612.145 ns (5%) |         |   80 bytes (1%) |           3 |
| `["groupby", "sum", "sac"]`                                    | 207.303 μs (5%) |         |   1.28 KiB (1%) |          14 |
| `["groupby", "sum", "xf-with-init"]`                           | 189.103 μs (5%) |         |   1.20 KiB (1%) |           9 |
| `["groupby", "sum", "xf-without-init"]`                        | 188.002 μs (5%) |         |   1.20 KiB (1%) |           9 |
| `["mapcat_eduction", "base"]`                                  |   2.100 μs (5%) |         |                 |             |
| `["mapcat_eduction", "xf-eduction"]`                           |   1.878 μs (5%) |         |                 |             |
| `["mapcat_eduction", "xf-xf"]`                                 |   1.880 μs (5%) |         |                 |             |
| `["missing_argmax", "man"]`                                    |   2.978 μs (5%) |         |   32 bytes (1%) |           1 |
| `["missing_argmax", "rf"]`                                     |   2.020 μs (5%) |         |   32 bytes (1%) |           1 |
| `["missing_argmax", "xf"]`                                     |   2.090 μs (5%) |         |   32 bytes (1%) |           1 |
| `["missing_dot", "equiv"]`                                     |   2.110 μs (5%) |         |   16 bytes (1%) |           1 |
| `["missing_dot", "man"]`                                       |   1.600 μs (5%) |         |   16 bytes (1%) |           1 |
| `["missing_dot", "naive"]`                                     |   5.417 μs (5%) |         |   16 bytes (1%) |           1 |
| `["missing_dot", "rf"]`                                        |   1.570 μs (5%) |         |   16 bytes (1%) |           1 |
| `["missing_dot", "rf_nota"]`                                   |   1.540 μs (5%) |         |   16 bytes (1%) |           1 |
| `["missing_dot", "xf"]`                                        | 120.102 μs (5%) |         |  72.17 KiB (1%) |        3744 |
| `["missing_dot", "xf_nota"]`                                   | 111.202 μs (5%) |         |  72.14 KiB (1%) |        3742 |
| `["overhead", "foldl"]`                                        |   5.600 ns (5%) |         |                 |             |
| `["overhead", "reduce_basecase"]`                              | 160.111 ns (5%) |         |   48 bytes (1%) |           2 |
| `["partition_by", "man"]`                                      |   2.506 ms (5%) |         |  352 bytes (1%) |           4 |
| `["partition_by", "xf"]`                                       |   2.547 ms (5%) |         |  544 bytes (1%) |           6 |
| `["set", "base"]`                                              |   5.479 ms (5%) |         |  49.56 KiB (1%) |          17 |
| `["set", "xf"]`                                                |   5.398 ms (5%) |         |  49.59 KiB (1%) |          19 |
| `["sum_transpose", "30", "noinit", "iter"]`                    |   2.522 μs (5%) |         |                 |             |
| `["sum_transpose", "30", "noinit", "man"]`                     |   2.833 μs (5%) |         |                 |             |
| `["sum_transpose", "30", "noinit", "xf"]`                      |   1.410 μs (5%) |         |   32 bytes (1%) |           2 |
| `["sum_transpose", "30", "withinit", "iter"]`                  |   1.710 μs (5%) |         |                 |             |
| `["sum_transpose", "30", "withinit", "man"]`                   |   1.280 μs (5%) |         |                 |             |
| `["sum_transpose", "30", "withinit", "xf"]`                    |   1.360 μs (5%) |         |   48 bytes (1%) |           3 |
| `["teerf_filter", "noinit"]`                                   |   2.444 μs (5%) |         |  160 bytes (1%) |           7 |
| `["teerf_filter", "withinit"]`                                 | 218.779 ns (5%) |         |                 |             |

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
  uname: Linux 5.4.0-1039-azure #41~18.04.1-Ubuntu SMP Mon Jan 18 14:00:01 UTC 2021 x86_64 x86_64
  CPU: Intel(R) Xeon(R) Platinum 8171M CPU @ 2.60GHz: 
              speed         user         nice          sys         idle          irq
       #1  2095 MHz      20670 s          0 s       1488 s      60152 s          0 s
       #2  2095 MHz      57636 s          0 s       1524 s      23213 s          0 s
       
  Memory: 6.791393280029297 GB (3697.453125 MB free)
  Uptime: 836.0 sec
  Load Avg:  1.0  0.9775390625  0.671875
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-9.0.1 (ORCJIT, skylake-avx512)
```

---
# Baseline result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmark: 8 Feb 2021 - 1:7
* Package commit: 6b0f22
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
| `["append!!", "eduction"]`                                     |  20.500 μs (5%) |         |  64.63 KiB (1%) |          13 |
| `["append!!", "xf"]`                                           |  21.101 μs (5%) |         |  64.63 KiB (1%) |          13 |
| `["cartesian", "copyto!", "iter"]`                             |   5.040 μs (5%) |         |                 |             |
| `["cartesian", "copyto!", "man"]`                              |   2.625 μs (5%) |         |                 |             |
| `["cartesian", "copyto!", "xf"]`                               |   3.850 μs (5%) |         |                 |             |
| `["cat", "base"]`                                              |   2.244 μs (5%) |         |                 |             |
| `["cat", "xf"]`                                                |   1.850 μs (5%) |         |                 |             |
| `["collect", "filter-missing"]`                                |  69.701 μs (5%) |         |  32.81 KiB (1%) |          14 |
| `["collect", "identity-float"]`                                |  26.600 μs (5%) |         | 256.66 KiB (1%) |          14 |
| `["collect", "identity-union"]`                                | 163.702 μs (5%) |         | 601.13 KiB (1%) |       10013 |
| `["dict", "base"]`                                             |   4.685 ms (5%) |         |  92.91 KiB (1%) |          22 |
| `["dict", "xf"]`                                               |   4.894 ms (5%) |         |  92.31 KiB (1%) |          18 |
| `["dot", "blas"]`                                              |   1.300 μs (5%) |         |                 |             |
| `["dot", "man"]`                                               |   1.340 μs (5%) |         |                 |             |
| `["dot", "rf"]`                                                |   2.378 μs (5%) |         |                 |             |
| `["dot", "xf"]`                                                |   2.467 μs (5%) |         |   64 bytes (1%) |           3 |
| `["filter_map_map!", "man"]`                                   |  58.301 μs (5%) |         |                 |             |
| `["filter_map_map!", "xf"]`                                    | 775.519 μs (5%) |         |   80 bytes (1%) |           3 |
| `["filter_map_reduce", "man"]`                                 | 255.508 μs (5%) |         |                 |             |
| `["filter_map_reduce", "xf"]`                                  | 212.006 μs (5%) |         |                 |             |
| `["filter_sum", "1000", "RandomFloats", "noinit", "base"]`     |   1.420 μs (5%) |         |                 |             |
| `["filter_sum", "1000", "RandomFloats", "noinit", "naive"]`    |   1.430 μs (5%) |         |                 |             |
| `["filter_sum", "1000", "RandomFloats", "noinit", "xf"]`       |   1.978 μs (5%) |         |                 |             |
| `["filter_sum", "1000", "RandomFloats", "withinit", "base"]`   |   1.978 μs (5%) |         |                 |             |
| `["filter_sum", "1000", "RandomFloats", "withinit", "naive"]`  | 910.000 ns (5%) |         |                 |             |
| `["filter_sum", "1000", "RandomFloats", "withinit", "xf"]`     |   1.940 μs (5%) |         |                 |             |
| `["filter_sum", "1000", "UnitRange", "noinit", "base"]`        |   2.011 μs (5%) |         |                 |             |
| `["filter_sum", "1000", "UnitRange", "noinit", "naive"]`       |   1.310 μs (5%) |         |                 |             |
| `["filter_sum", "1000", "UnitRange", "noinit", "xf"]`          | 135.749 ns (5%) |         |                 |             |
| `["filter_sum", "1000", "UnitRange", "withinit", "base"]`      | 117.150 ns (5%) |         |                 |             |
| `["filter_sum", "1000", "UnitRange", "withinit", "naive"]`     |   1.030 μs (5%) |         |                 |             |
| `["filter_sum", "1000", "UnitRange", "withinit", "xf"]`        | 140.122 ns (5%) |         |                 |             |
| `["filter_sum", "10000", "RandomFloats", "noinit", "base"]`    |  35.701 μs (5%) |         |                 |             |
| `["filter_sum", "10000", "RandomFloats", "noinit", "naive"]`   |  51.100 μs (5%) |         |                 |             |
| `["filter_sum", "10000", "RandomFloats", "noinit", "xf"]`      |  20.101 μs (5%) |         |                 |             |
| `["filter_sum", "10000", "RandomFloats", "withinit", "base"]`  |  19.600 μs (5%) |         |                 |             |
| `["filter_sum", "10000", "RandomFloats", "withinit", "naive"]` |  49.201 μs (5%) |         |                 |             |
| `["filter_sum", "10000", "RandomFloats", "withinit", "xf"]`    |  20.100 μs (5%) |         |                 |             |
| `["filter_sum", "10000", "UnitRange", "noinit", "base"]`       |  20.000 μs (5%) |         |                 |             |
| `["filter_sum", "10000", "UnitRange", "noinit", "naive"]`      |  13.000 μs (5%) |         |                 |             |
| `["filter_sum", "10000", "UnitRange", "noinit", "xf"]`         |   1.300 μs (5%) |         |                 |             |
| `["filter_sum", "10000", "UnitRange", "withinit", "base"]`     |   1.110 μs (5%) |         |                 |             |
| `["filter_sum", "10000", "UnitRange", "withinit", "naive"]`    |  10.200 μs (5%) |         |                 |             |
| `["filter_sum", "10000", "UnitRange", "withinit", "xf"]`       |   1.300 μs (5%) |         |                 |             |
| `["findall", "base"]`                                          | 910.111 μs (5%) |         |   2.00 MiB (1%) |          18 |
| `["findall", "xf-array"]`                                      | 818.427 μs (5%) |         |   3.02 MiB (1%) |       98829 |
| `["findall", "xf-iter"]`                                       | 370.512 μs (5%) |         |   2.00 MiB (1%) |          19 |
| `["gemm", "fusedmul", "blas", "16"]`                           |   3.571 ms (5%) |         |                 |             |
| `["gemm", "fusedmul", "blas", "2"]`                            |   2.760 ms (5%) |         |                 |             |
| `["gemm", "fusedmul", "blas", "32"]`                           |   4.404 ms (5%) |         |                 |             |
| `["gemm", "fusedmul", "blas", "8"]`                            |   3.082 ms (5%) |         |                 |             |
| `["gemm", "fusedmul", "xf", "16"]`                             |   5.861 ms (5%) |         |  192 bytes (1%) |           4 |
| `["gemm", "fusedmul", "xf", "2"]`                              | 719.518 μs (5%) |         |  192 bytes (1%) |           4 |
| `["gemm", "fusedmul", "xf", "32"]`                             |  11.751 ms (5%) |         |  192 bytes (1%) |           4 |
| `["gemm", "fusedmul", "xf", "8"]`                              |   2.897 ms (5%) |         |  192 bytes (1%) |           4 |
| `["gemm", "mul", "linalg", "256"]`                             | 519.715 μs (5%) |         |                 |             |
| `["gemm", "mul", "linalg", "32"]`                              |   2.100 μs (5%) |         |                 |             |
| `["gemm", "mul", "linalg", "8"]`                               | 200.000 ns (5%) |         |                 |             |
| `["gemm", "mul", "man", "false", "256"]`                       |   1.929 ms (5%) |         |                 |             |
| `["gemm", "mul", "man", "false", "32"]`                        |   5.600 μs (5%) |         |                 |             |
| `["gemm", "mul", "man", "false", "8"]`                         | 400.000 ns (5%) |         |                 |             |
| `["gemm", "mul", "man", "ivdep", "256"]`                       |   1.881 ms (5%) |         |                 |             |
| `["gemm", "mul", "man", "ivdep", "32"]`                        |   4.100 μs (5%) |         |                 |             |
| `["gemm", "mul", "man", "ivdep", "8"]`                         | 400.000 ns (5%) |         |                 |             |
| `["gemm", "mul", "man", "true", "256"]`                        |   1.894 ms (5%) |         |                 |             |
| `["gemm", "mul", "man", "true", "32"]`                         |   5.400 μs (5%) |         |                 |             |
| `["gemm", "mul", "man", "true", "8"]`                          | 400.000 ns (5%) |         |                 |             |
| `["gemm", "mul", "xf", "false", "256"]`                        |   1.944 ms (5%) |         |   80 bytes (1%) |           3 |
| `["gemm", "mul", "xf", "false", "32"]`                         |   5.500 μs (5%) |         |   80 bytes (1%) |           3 |
| `["gemm", "mul", "xf", "false", "8"]`                          | 500.000 ns (5%) |         |   80 bytes (1%) |           3 |
| `["gemm", "mul", "xf", "ivdep", "256"]`                        |   1.843 ms (5%) |         |   80 bytes (1%) |           3 |
| `["gemm", "mul", "xf", "ivdep", "32"]`                         |   4.100 μs (5%) |         |   80 bytes (1%) |           3 |
| `["gemm", "mul", "xf", "ivdep", "8"]`                          | 500.000 ns (5%) |         |   80 bytes (1%) |           3 |
| `["gemm", "mul", "xf", "true", "256"]`                         |   1.881 ms (5%) |         |   80 bytes (1%) |           3 |
| `["gemm", "mul", "xf", "true", "32"]`                          |   5.500 μs (5%) |         |   80 bytes (1%) |           3 |
| `["gemm", "mul", "xf", "true", "8"]`                           | 600.000 ns (5%) |         |   80 bytes (1%) |           3 |
| `["groupby", "sum", "sac"]`                                    | 225.306 μs (5%) |         |  624 bytes (1%) |           5 |
| `["groupby", "sum", "xf-with-init"]`                           | 141.004 μs (5%) |         |   1.20 KiB (1%) |           9 |
| `["groupby", "sum", "xf-without-init"]`                        | 186.404 μs (5%) |         |   1.20 KiB (1%) |           9 |
| `["mapcat_eduction", "base"]`                                  |   2.089 μs (5%) |         |                 |             |
| `["mapcat_eduction", "xf-eduction"]`                           |   1.856 μs (5%) |         |                 |             |
| `["mapcat_eduction", "xf-xf"]`                                 |   1.870 μs (5%) |         |                 |             |
| `["missing_argmax", "man"]`                                    |   2.978 μs (5%) |         |   32 bytes (1%) |           1 |
| `["missing_argmax", "rf"]`                                     |   2.010 μs (5%) |         |   32 bytes (1%) |           1 |
| `["missing_argmax", "xf"]`                                     |   2.090 μs (5%) |         |   32 bytes (1%) |           1 |
| `["missing_dot", "equiv"]`                                     |   1.880 μs (5%) |         |   16 bytes (1%) |           1 |
| `["missing_dot", "man"]`                                       |   1.570 μs (5%) |         |   16 bytes (1%) |           1 |
| `["missing_dot", "naive"]`                                     |   5.400 μs (5%) |         |   16 bytes (1%) |           1 |
| `["missing_dot", "rf"]`                                        |   1.550 μs (5%) |         |   16 bytes (1%) |           1 |
| `["missing_dot", "rf_nota"]`                                   |   1.550 μs (5%) |         |   16 bytes (1%) |           1 |
| `["missing_dot", "xf"]`                                        | 110.604 μs (5%) |         |  72.06 KiB (1%) |        3738 |
| `["missing_dot", "xf_nota"]`                                   |  97.103 μs (5%) |         |  72.13 KiB (1%) |        3742 |
| `["overhead", "foldl"]`                                        |   5.600 ns (5%) |         |                 |             |
| `["overhead", "reduce_basecase"]`                              | 163.909 ns (5%) |         |   48 bytes (1%) |           2 |
| `["partition_by", "man"]`                                      |   2.497 ms (5%) |         |  352 bytes (1%) |           4 |
| `["partition_by", "xf"]`                                       |   2.536 ms (5%) |         |  544 bytes (1%) |           6 |
| `["set", "base"]`                                              |   5.564 ms (5%) |         |  49.56 KiB (1%) |          17 |
| `["set", "xf"]`                                                |   5.831 ms (5%) |         |  49.59 KiB (1%) |          19 |
| `["sum_transpose", "30", "noinit", "iter"]`                    |   2.511 μs (5%) |         |                 |             |
| `["sum_transpose", "30", "noinit", "man"]`                     |   2.822 μs (5%) |         |                 |             |
| `["sum_transpose", "30", "noinit", "xf"]`                      |   1.410 μs (5%) |         |   32 bytes (1%) |           2 |
| `["sum_transpose", "30", "withinit", "iter"]`                  |   2.020 μs (5%) |         |                 |             |
| `["sum_transpose", "30", "withinit", "man"]`                   |   1.280 μs (5%) |         |                 |             |
| `["sum_transpose", "30", "withinit", "xf"]`                    |   1.360 μs (5%) |         |   48 bytes (1%) |           3 |
| `["teerf_filter", "noinit"]`                                   |   2.422 μs (5%) |         |  160 bytes (1%) |           7 |
| `["teerf_filter", "withinit"]`                                 | 218.579 ns (5%) |         |                 |             |

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
  uname: Linux 5.4.0-1039-azure #41~18.04.1-Ubuntu SMP Mon Jan 18 14:00:01 UTC 2021 x86_64 x86_64
  CPU: Intel(R) Xeon(R) Platinum 8171M CPU @ 2.60GHz: 
              speed         user         nice          sys         idle          irq
       #1  2095 MHz      41492 s          0 s       1678 s      70715 s          0 s
       #2  2095 MHz      68208 s          0 s       1724 s      43974 s          0 s
       
  Memory: 6.791393280029297 GB (3705.32421875 MB free)
  Uptime: 1152.0 sec
  Load Avg:  1.05078125  1.02001953125  0.79296875
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
    CPU MHz:             2095.093
    BogoMIPS:            4190.18
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
| Address Size       | 48 bits virtual, 46 bits physical                       |
| SIMD               | 512 bit = 64 byte max. SIMD vector size                 |
| Time Stamp Counter | TSC is accessible via `rdtsc`                           |
|                    | TSC increased at every clock cycle (non-invariant TSC)  |
| Perf. Monitoring   | Performance Monitoring Counters (PMC) are not supported |
| Hypervisor         | Yes, Microsoft                                          |

