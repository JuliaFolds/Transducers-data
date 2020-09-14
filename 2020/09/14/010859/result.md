# Benchmark result

* Pull request commit: [`b653da99ec655a4801b8dba5f43eaee937d17525`](https://github.com/JuliaFolds/Transducers.jl/commit/b653da99ec655a4801b8dba5f43eaee937d17525)
* Pull request: <https://github.com/JuliaFolds/Transducers.jl/pull/243> (Update */Manifest.toml)

# Judge result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmarks:
    - Target: 14 Sep 2020 - 01:02
    - Baseline: 14 Sep 2020 - 01:08
* Package commits:
    - Target: 533c41
    - Baseline: b2fa04
* Julia commits:
    - Target: 697e78
    - Baseline: 697e78
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
| `["append!!", "eduction"]`                                     | 0.84 (5%) :white_check_mark: |    1.00 (1%)  |
| `["append!!", "xf"]`                                           | 0.74 (5%) :white_check_mark: |    1.00 (1%)  |
| `["cartesian", "copyto!", "iter"]`                             | 0.86 (5%) :white_check_mark: |    1.00 (1%)  |
| `["cat", "base"]`                                              | 0.93 (5%) :white_check_mark: |    1.00 (1%)  |
| `["cat", "xf"]`                                                | 0.86 (5%) :white_check_mark: |    1.00 (1%)  |
| `["collect", "filter-missing"]`                                |                1.06 (5%) :x: |    1.00 (1%)  |
| `["collect", "identity-float"]`                                |                1.13 (5%) :x: |    1.00 (1%)  |
| `["dict", "base"]`                                             | 0.89 (5%) :white_check_mark: |    1.00 (1%)  |
| `["dict", "xf"]`                                               | 0.88 (5%) :white_check_mark: |    1.00 (1%)  |
| `["dot", "blas"]`                                              | 0.89 (5%) :white_check_mark: |    1.00 (1%)  |
| `["dot", "man"]`                                               | 0.81 (5%) :white_check_mark: |    1.00 (1%)  |
| `["dot", "rf"]`                                                | 0.85 (5%) :white_check_mark: |    1.00 (1%)  |
| `["dot", "xf"]`                                                | 0.76 (5%) :white_check_mark: |    1.00 (1%)  |
| `["filter_map_map!", "xf"]`                                    | 0.91 (5%) :white_check_mark: |    1.00 (1%)  |
| `["filter_map_reduce", "xf"]`                                  |                1.16 (5%) :x: |    1.00 (1%)  |
| `["filter_sum", "1000", "RandomFloats", "noinit", "base"]`     | 0.86 (5%) :white_check_mark: |    1.00 (1%)  |
| `["filter_sum", "1000", "RandomFloats", "noinit", "xf"]`       | 0.87 (5%) :white_check_mark: |    1.00 (1%)  |
| `["filter_sum", "1000", "RandomFloats", "withinit", "base"]`   | 0.85 (5%) :white_check_mark: |    1.00 (1%)  |
| `["filter_sum", "1000", "RandomFloats", "withinit", "naive"]`  | 0.77 (5%) :white_check_mark: |    1.00 (1%)  |
| `["filter_sum", "1000", "RandomFloats", "withinit", "xf"]`     | 0.75 (5%) :white_check_mark: |    1.00 (1%)  |
| `["filter_sum", "1000", "UnitRange", "noinit", "base"]`        | 0.75 (5%) :white_check_mark: |    1.00 (1%)  |
| `["filter_sum", "1000", "UnitRange", "noinit", "naive"]`       | 0.88 (5%) :white_check_mark: |    1.00 (1%)  |
| `["filter_sum", "1000", "UnitRange", "withinit", "naive"]`     |                1.25 (5%) :x: |    1.00 (1%)  |
| `["filter_sum", "10000", "RandomFloats", "noinit", "base"]`    | 0.75 (5%) :white_check_mark: |    1.00 (1%)  |
| `["filter_sum", "10000", "RandomFloats", "noinit", "naive"]`   | 0.76 (5%) :white_check_mark: |    1.00 (1%)  |
| `["filter_sum", "10000", "RandomFloats", "noinit", "xf"]`      | 0.86 (5%) :white_check_mark: |    1.00 (1%)  |
| `["filter_sum", "10000", "RandomFloats", "withinit", "naive"]` | 0.87 (5%) :white_check_mark: |    1.00 (1%)  |
| `["filter_sum", "10000", "UnitRange", "noinit", "base"]`       | 0.86 (5%) :white_check_mark: |    1.00 (1%)  |
| `["filter_sum", "10000", "UnitRange", "noinit", "naive"]`      | 0.87 (5%) :white_check_mark: |    1.00 (1%)  |
| `["filter_sum", "10000", "UnitRange", "noinit", "xf"]`         | 0.85 (5%) :white_check_mark: |    1.00 (1%)  |
| `["filter_sum", "10000", "UnitRange", "withinit", "base"]`     | 0.87 (5%) :white_check_mark: |    1.00 (1%)  |
| `["filter_sum", "10000", "UnitRange", "withinit", "naive"]`    |                1.10 (5%) :x: |    1.00 (1%)  |
| `["filter_sum", "10000", "UnitRange", "withinit", "xf"]`       | 0.75 (5%) :white_check_mark: |    1.00 (1%)  |
| `["findall", "base"]`                                          | 0.90 (5%) :white_check_mark: |    1.00 (1%)  |
| `["findall", "xf-array"]`                                      |                1.14 (5%) :x: |    1.00 (1%)  |
| `["findall", "xf-iter"]`                                       | 0.87 (5%) :white_check_mark: |    1.00 (1%)  |
| `["gemm", "fusedmul", "blas", "2"]`                            |                1.06 (5%) :x: |    1.00 (1%)  |
| `["gemm", "mul", "linalg", "32"]`                              | 0.85 (5%) :white_check_mark: |    1.00 (1%)  |
| `["gemm", "mul", "linalg", "8"]`                               | 0.89 (5%) :white_check_mark: |    1.00 (1%)  |
| `["gemm", "mul", "man", "false", "256"]`                       | 0.95 (5%) :white_check_mark: |    1.00 (1%)  |
| `["gemm", "mul", "man", "false", "32"]`                        | 0.88 (5%) :white_check_mark: |    1.00 (1%)  |
| `["gemm", "mul", "man", "false", "8"]`                         | 0.81 (5%) :white_check_mark: |    1.00 (1%)  |
| `["gemm", "mul", "man", "ivdep", "256"]`                       | 0.93 (5%) :white_check_mark: |    1.00 (1%)  |
| `["gemm", "mul", "man", "ivdep", "32"]`                        | 0.78 (5%) :white_check_mark: |    1.00 (1%)  |
| `["gemm", "mul", "man", "ivdep", "8"]`                         | 0.87 (5%) :white_check_mark: |    1.00 (1%)  |
| `["gemm", "mul", "man", "true", "32"]`                         |                1.31 (5%) :x: |    1.00 (1%)  |
| `["gemm", "mul", "man", "true", "8"]`                          | 0.92 (5%) :white_check_mark: |    1.00 (1%)  |
| `["gemm", "mul", "xf", "false", "8"]`                          | 0.53 (5%) :white_check_mark: |    1.00 (1%)  |
| `["gemm", "mul", "xf", "ivdep", "256"]`                        |                1.15 (5%) :x: |    1.00 (1%)  |
| `["gemm", "mul", "xf", "ivdep", "8"]`                          |                1.25 (5%) :x: |    1.00 (1%)  |
| `["gemm", "mul", "xf", "true", "32"]`                          | 0.87 (5%) :white_check_mark: |    1.00 (1%)  |
| `["gemm", "mul", "xf", "true", "8"]`                           | 0.89 (5%) :white_check_mark: |    1.00 (1%)  |
| `["groupby", "sum", "sac"]`                                    | 0.71 (5%) :white_check_mark: | 2.51 (1%) :x: |
| `["mapcat_eduction", "base"]`                                  | 0.74 (5%) :white_check_mark: |    1.00 (1%)  |
| `["mapcat_eduction", "xf-eduction"]`                           |                1.19 (5%) :x: |    1.00 (1%)  |
| `["missing_argmax", "rf"]`                                     | 0.88 (5%) :white_check_mark: |    1.00 (1%)  |
| `["missing_argmax", "xf"]`                                     | 0.85 (5%) :white_check_mark: |    1.00 (1%)  |
| `["missing_dot", "man"]`                                       |                1.14 (5%) :x: |    1.00 (1%)  |
| `["missing_dot", "naive"]`                                     | 0.75 (5%) :white_check_mark: |    1.00 (1%)  |
| `["missing_dot", "rf"]`                                        | 0.76 (5%) :white_check_mark: |    1.00 (1%)  |
| `["missing_dot", "rf_nota"]`                                   | 0.84 (5%) :white_check_mark: |    1.00 (1%)  |
| `["missing_dot", "xf"]`                                        | 0.90 (5%) :white_check_mark: |    1.00 (1%)  |
| `["missing_dot", "xf_nota"]`                                   | 0.86 (5%) :white_check_mark: |    1.00 (1%)  |
| `["overhead", "foldl"]`                                        | 0.94 (5%) :white_check_mark: |    1.00 (1%)  |
| `["partition_by", "man"]`                                      | 0.77 (5%) :white_check_mark: |    1.00 (1%)  |
| `["partition_by", "xf"]`                                       | 0.89 (5%) :white_check_mark: |    1.00 (1%)  |
| `["set", "base"]`                                              | 0.92 (5%) :white_check_mark: |    1.00 (1%)  |
| `["sum_transpose", "30", "noinit", "iter"]`                    |                1.15 (5%) :x: |    1.00 (1%)  |
| `["sum_transpose", "30", "noinit", "xf"]`                      | 0.87 (5%) :white_check_mark: |    1.00 (1%)  |
| `["sum_transpose", "30", "withinit", "xf"]`                    | 0.88 (5%) :white_check_mark: |    1.00 (1%)  |
| `["teerf_filter", "noinit"]`                                   | 0.80 (5%) :white_check_mark: |    1.00 (1%)  |
| `["teerf_filter", "withinit"]`                                 | 0.86 (5%) :white_check_mark: |    1.00 (1%)  |

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
Julia Version 1.5.1
Commit 697e782ab8 (2020-08-25 20:08 UTC)
Platform Info:
  OS: Linux (x86_64-pc-linux-gnu)
      Ubuntu 18.04.5 LTS
  uname: Linux 5.4.0-1023-azure #23~18.04.1-Ubuntu SMP Thu Aug 20 14:46:48 UTC 2020 x86_64 x86_64
  CPU: Intel(R) Xeon(R) Platinum 8171M CPU @ 2.60GHz: 
              speed         user         nice          sys         idle          irq
       #1  2095 MHz      50128 s          0 s       1482 s      30168 s          0 s
       #2  2095 MHz      25232 s          0 s       1657 s      54960 s          0 s
       
  Memory: 6.791393280029297 GB (3011.56640625 MB free)
  Uptime: 836.0 sec
  Load Avg:  1.013671875  1.0  0.6650390625
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-9.0.1 (ORCJIT, skylake-avx512)
```

### Baseline
```
Julia Version 1.5.1
Commit 697e782ab8 (2020-08-25 20:08 UTC)
Platform Info:
  OS: Linux (x86_64-pc-linux-gnu)
      Ubuntu 18.04.5 LTS
  uname: Linux 5.4.0-1023-azure #23~18.04.1-Ubuntu SMP Thu Aug 20 14:46:48 UTC 2020 x86_64 x86_64
  CPU: Intel(R) Xeon(R) Platinum 8171M CPU @ 2.60GHz: 
              speed         user         nice          sys         idle          irq
       #1  2095 MHz      55353 s          0 s       1685 s      57660 s          0 s
       #2  2095 MHz      52834 s          0 s       1840 s      60172 s          0 s
       
  Memory: 6.791393280029297 GB (3038.2421875 MB free)
  Uptime: 1166.0 sec
  Load Avg:  1.00146484375  1.0146484375  0.791015625
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-9.0.1 (ORCJIT, skylake-avx512)
```

---
# Target result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmark: 14 Sep 2020 - 1:2
* Package commit: 533c41
* Julia commit: 697e78
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
| `["append!!", "eduction"]`                                     |  18.500 μs (5%) |         |  64.63 KiB (1%) |          13 |
| `["append!!", "xf"]`                                           |  16.100 μs (5%) |         |  64.63 KiB (1%) |          13 |
| `["cartesian", "copyto!", "iter"]`                             |   4.983 μs (5%) |         |                 |             |
| `["cartesian", "copyto!", "man"]`                              |   2.800 μs (5%) |         |                 |             |
| `["cartesian", "copyto!", "xf"]`                               |   2.833 μs (5%) |         |                 |             |
| `["cat", "base"]`                                              |   1.560 μs (5%) |         |                 |             |
| `["cat", "xf"]`                                                |   1.380 μs (5%) |         |                 |             |
| `["collect", "filter-missing"]`                                |  56.800 μs (5%) |         |  32.81 KiB (1%) |          14 |
| `["collect", "identity-float"]`                                |  26.800 μs (5%) |         | 256.66 KiB (1%) |          14 |
| `["collect", "identity-union"]`                                | 138.401 μs (5%) |         | 601.04 KiB (1%) |       10013 |
| `["dict", "base"]`                                             |   4.108 ms (5%) |         |  92.91 KiB (1%) |          22 |
| `["dict", "xf"]`                                               |   4.118 ms (5%) |         |  92.31 KiB (1%) |          18 |
| `["dot", "blas"]`                                              |   1.180 μs (5%) |         |                 |             |
| `["dot", "man"]`                                               |   1.080 μs (5%) |         |                 |             |
| `["dot", "rf"]`                                                |   1.800 μs (5%) |         |                 |             |
| `["dot", "xf"]`                                                |   1.856 μs (5%) |         |   64 bytes (1%) |           3 |
| `["filter_map_map!", "man"]`                                   |  58.600 μs (5%) |         |                 |             |
| `["filter_map_map!", "xf"]`                                    | 587.404 μs (5%) |         |   80 bytes (1%) |           3 |
| `["filter_map_reduce", "man"]`                                 | 191.901 μs (5%) |         |                 |             |
| `["filter_map_reduce", "xf"]`                                  | 223.002 μs (5%) |         |                 |             |
| `["filter_sum", "1000", "RandomFloats", "noinit", "base"]`     |   1.070 μs (5%) |         |                 |             |
| `["filter_sum", "1000", "RandomFloats", "noinit", "naive"]`    |   1.240 μs (5%) |         |                 |             |
| `["filter_sum", "1000", "RandomFloats", "noinit", "xf"]`       |   1.730 μs (5%) |         |                 |             |
| `["filter_sum", "1000", "RandomFloats", "withinit", "base"]`   |   1.470 μs (5%) |         |                 |             |
| `["filter_sum", "1000", "RandomFloats", "withinit", "naive"]`  | 691.556 ns (5%) |         |                 |             |
| `["filter_sum", "1000", "RandomFloats", "withinit", "xf"]`     |   1.480 μs (5%) |         |                 |             |
| `["filter_sum", "1000", "UnitRange", "noinit", "base"]`        |   1.510 μs (5%) |         |                 |             |
| `["filter_sum", "1000", "UnitRange", "noinit", "naive"]`       | 990.000 ns (5%) |         |                 |             |
| `["filter_sum", "1000", "UnitRange", "noinit", "xf"]`          | 101.970 ns (5%) |         |                 |             |
| `["filter_sum", "1000", "UnitRange", "withinit", "base"]`      |  87.911 ns (5%) |         |                 |             |
| `["filter_sum", "1000", "UnitRange", "withinit", "naive"]`     | 774.713 ns (5%) |         |                 |             |
| `["filter_sum", "1000", "UnitRange", "withinit", "xf"]`        | 105.379 ns (5%) |         |                 |             |
| `["filter_sum", "10000", "RandomFloats", "noinit", "base"]`    |  35.200 μs (5%) |         |                 |             |
| `["filter_sum", "10000", "RandomFloats", "noinit", "naive"]`   |  45.100 μs (5%) |         |                 |             |
| `["filter_sum", "10000", "RandomFloats", "noinit", "xf"]`      |  15.001 μs (5%) |         |                 |             |
| `["filter_sum", "10000", "RandomFloats", "withinit", "base"]`  |  17.500 μs (5%) |         |                 |             |
| `["filter_sum", "10000", "RandomFloats", "withinit", "naive"]` |  37.500 μs (5%) |         |                 |             |
| `["filter_sum", "10000", "RandomFloats", "withinit", "xf"]`    |  15.100 μs (5%) |         |                 |             |
| `["filter_sum", "10000", "UnitRange", "noinit", "base"]`       |  15.000 μs (5%) |         |                 |             |
| `["filter_sum", "10000", "UnitRange", "noinit", "naive"]`      |   9.700 μs (5%) |         |                 |             |
| `["filter_sum", "10000", "UnitRange", "noinit", "xf"]`         | 964.706 ns (5%) |         |                 |             |
| `["filter_sum", "10000", "UnitRange", "withinit", "base"]`     | 970.000 ns (5%) |         |                 |             |
| `["filter_sum", "10000", "UnitRange", "withinit", "naive"]`    |   8.900 μs (5%) |         |                 |             |
| `["filter_sum", "10000", "UnitRange", "withinit", "xf"]`       | 970.000 ns (5%) |         |                 |             |
| `["findall", "base"]`                                          | 862.205 μs (5%) |         |   2.00 MiB (1%) |          18 |
| `["findall", "xf-array"]`                                      | 771.505 μs (5%) |         |   3.02 MiB (1%) |       98829 |
| `["findall", "xf-iter"]`                                       | 334.202 μs (5%) |         |   2.00 MiB (1%) |          19 |
| `["gemm", "fusedmul", "blas", "16"]`                           |   3.547 ms (5%) |         |                 |             |
| `["gemm", "fusedmul", "blas", "2"]`                            |   2.947 ms (5%) |         |                 |             |
| `["gemm", "fusedmul", "blas", "32"]`                           |   4.295 ms (5%) |         |                 |             |
| `["gemm", "fusedmul", "blas", "8"]`                            |   3.071 ms (5%) |         |                 |             |
| `["gemm", "fusedmul", "xf", "16"]`                             |   5.830 ms (5%) |         |  192 bytes (1%) |           4 |
| `["gemm", "fusedmul", "xf", "2"]`                              | 682.604 μs (5%) |         |  192 bytes (1%) |           4 |
| `["gemm", "fusedmul", "xf", "32"]`                             |  11.751 ms (5%) |         |  192 bytes (1%) |           4 |
| `["gemm", "fusedmul", "xf", "8"]`                              |   2.887 ms (5%) |         |  192 bytes (1%) |           4 |
| `["gemm", "mul", "linalg", "256"]`                             | 407.002 μs (5%) |         |                 |             |
| `["gemm", "mul", "linalg", "32"]`                              |   1.790 μs (5%) |         |                 |             |
| `["gemm", "mul", "linalg", "8"]`                               | 177.391 ns (5%) |         |                 |             |
| `["gemm", "mul", "man", "false", "256"]`                       |   1.644 ms (5%) |         |                 |             |
| `["gemm", "mul", "man", "false", "32"]`                        |   4.157 μs (5%) |         |                 |             |
| `["gemm", "mul", "man", "false", "8"]`                         | 325.897 ns (5%) |         |                 |             |
| `["gemm", "mul", "man", "ivdep", "256"]`                       |   1.561 ms (5%) |         |                 |             |
| `["gemm", "mul", "man", "ivdep", "32"]`                        |   3.138 μs (5%) |         |                 |             |
| `["gemm", "mul", "man", "ivdep", "8"]`                         | 348.505 ns (5%) |         |                 |             |
| `["gemm", "mul", "man", "true", "256"]`                        |   1.639 ms (5%) |         |                 |             |
| `["gemm", "mul", "man", "true", "32"]`                         |   5.243 μs (5%) |         |                 |             |
| `["gemm", "mul", "man", "true", "8"]`                          | 369.048 ns (5%) |         |                 |             |
| `["gemm", "mul", "xf", "false", "256"]`                        |   1.672 ms (5%) |         |   80 bytes (1%) |           3 |
| `["gemm", "mul", "xf", "false", "32"]`                         |   4.500 μs (5%) |         |   80 bytes (1%) |           3 |
| `["gemm", "mul", "xf", "false", "8"]`                          | 368.293 ns (5%) |         |   80 bytes (1%) |           3 |
| `["gemm", "mul", "xf", "ivdep", "256"]`                        |   1.858 ms (5%) |         |   80 bytes (1%) |           3 |
| `["gemm", "mul", "xf", "ivdep", "32"]`                         |   4.112 μs (5%) |         |   80 bytes (1%) |           3 |
| `["gemm", "mul", "xf", "ivdep", "8"]`                          | 501.041 ns (5%) |         |   80 bytes (1%) |           3 |
| `["gemm", "mul", "xf", "true", "256"]`                         |   1.623 ms (5%) |         |   80 bytes (1%) |           3 |
| `["gemm", "mul", "xf", "true", "32"]`                          |   4.614 μs (5%) |         |   80 bytes (1%) |           3 |
| `["gemm", "mul", "xf", "true", "8"]`                           | 531.915 ns (5%) |         |   80 bytes (1%) |           3 |
| `["groupby", "sum", "sac"]`                                    | 119.600 μs (5%) |         |   1.53 KiB (1%) |          16 |
| `["groupby", "sum", "xf-with-init"]`                           | 142.201 μs (5%) |         |   1.20 KiB (1%) |           9 |
| `["groupby", "sum", "xf-without-init"]`                        | 140.601 μs (5%) |         |   1.20 KiB (1%) |           9 |
| `["mapcat_eduction", "base"]`                                  |   1.560 μs (5%) |         |                 |             |
| `["mapcat_eduction", "xf-eduction"]`                           |   1.660 μs (5%) |         |                 |             |
| `["mapcat_eduction", "xf-xf"]`                                 |   1.390 μs (5%) |         |                 |             |
| `["missing_argmax", "man"]`                                    |   2.233 μs (5%) |         |   32 bytes (1%) |           1 |
| `["missing_argmax", "rf"]`                                     |   1.840 μs (5%) |         |   32 bytes (1%) |           1 |
| `["missing_argmax", "xf"]`                                     |   1.530 μs (5%) |         |   32 bytes (1%) |           1 |
| `["missing_dot", "equiv"]`                                     |   1.740 μs (5%) |         |   16 bytes (1%) |           1 |
| `["missing_dot", "man"]`                                       |   1.350 μs (5%) |         |   16 bytes (1%) |           1 |
| `["missing_dot", "naive"]`                                     |   4.100 μs (5%) |         |   16 bytes (1%) |           1 |
| `["missing_dot", "rf"]`                                        |   1.180 μs (5%) |         |   16 bytes (1%) |           1 |
| `["missing_dot", "rf_nota"]`                                   |   1.720 μs (5%) |         |   16 bytes (1%) |           1 |
| `["missing_dot", "xf"]`                                        |  82.901 μs (5%) |         |  72.03 KiB (1%) |        3736 |
| `["missing_dot", "xf_nota"]`                                   |  82.200 μs (5%) |         |  72.08 KiB (1%) |        3738 |
| `["overhead", "foldl"]`                                        |   4.900 ns (5%) |         |                 |             |
| `["overhead", "reduce_basecase"]`                              | 213.241 ns (5%) |         |  368 bytes (1%) |           6 |
| `["partition_by", "man"]`                                      |   1.906 ms (5%) |         |  352 bytes (1%) |           4 |
| `["partition_by", "xf"]`                                       |   2.150 ms (5%) |         |  544 bytes (1%) |           6 |
| `["set", "base"]`                                              |   4.736 ms (5%) |         |  49.56 KiB (1%) |          17 |
| `["set", "xf"]`                                                |   4.918 ms (5%) |         |  49.59 KiB (1%) |          19 |
| `["sum_transpose", "30", "noinit", "iter"]`                    |   2.511 μs (5%) |         |                 |             |
| `["sum_transpose", "30", "noinit", "man"]`                     |   2.467 μs (5%) |         |                 |             |
| `["sum_transpose", "30", "noinit", "xf"]`                      |   1.230 μs (5%) |         |   32 bytes (1%) |           2 |
| `["sum_transpose", "30", "withinit", "iter"]`                  |   1.510 μs (5%) |         |                 |             |
| `["sum_transpose", "30", "withinit", "man"]`                   |   1.114 μs (5%) |         |                 |             |
| `["sum_transpose", "30", "withinit", "xf"]`                    |   1.190 μs (5%) |         |   48 bytes (1%) |           3 |
| `["teerf_filter", "noinit"]`                                   | 328.365 ns (5%) |         |  112 bytes (1%) |           4 |
| `["teerf_filter", "withinit"]`                                 | 164.896 ns (5%) |         |                 |             |

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
Julia Version 1.5.1
Commit 697e782ab8 (2020-08-25 20:08 UTC)
Platform Info:
  OS: Linux (x86_64-pc-linux-gnu)
      Ubuntu 18.04.5 LTS
  uname: Linux 5.4.0-1023-azure #23~18.04.1-Ubuntu SMP Thu Aug 20 14:46:48 UTC 2020 x86_64 x86_64
  CPU: Intel(R) Xeon(R) Platinum 8171M CPU @ 2.60GHz: 
              speed         user         nice          sys         idle          irq
       #1  2095 MHz      50128 s          0 s       1482 s      30168 s          0 s
       #2  2095 MHz      25232 s          0 s       1657 s      54960 s          0 s
       
  Memory: 6.791393280029297 GB (3011.56640625 MB free)
  Uptime: 836.0 sec
  Load Avg:  1.013671875  1.0  0.6650390625
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-9.0.1 (ORCJIT, skylake-avx512)
```

---
# Baseline result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmark: 14 Sep 2020 - 1:8
* Package commit: b2fa04
* Julia commit: 697e78
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
| `["append!!", "eduction"]`                                     |  22.001 μs (5%) |         |  64.63 KiB (1%) |          13 |
| `["append!!", "xf"]`                                           |  21.700 μs (5%) |         |  64.63 KiB (1%) |          13 |
| `["cartesian", "copyto!", "iter"]`                             |   5.767 μs (5%) |         |                 |             |
| `["cartesian", "copyto!", "man"]`                              |   2.800 μs (5%) |         |                 |             |
| `["cartesian", "copyto!", "xf"]`                               |   2.700 μs (5%) |         |                 |             |
| `["cat", "base"]`                                              |   1.680 μs (5%) |         |                 |             |
| `["cat", "xf"]`                                                |   1.600 μs (5%) |         |                 |             |
| `["collect", "filter-missing"]`                                |  53.701 μs (5%) |         |  32.81 KiB (1%) |          14 |
| `["collect", "identity-float"]`                                |  23.701 μs (5%) |         | 256.66 KiB (1%) |          14 |
| `["collect", "identity-union"]`                                | 134.500 μs (5%) |         | 601.04 KiB (1%) |       10013 |
| `["dict", "base"]`                                             |   4.611 ms (5%) |         |  92.91 KiB (1%) |          22 |
| `["dict", "xf"]`                                               |   4.694 ms (5%) |         |  92.31 KiB (1%) |          18 |
| `["dot", "blas"]`                                              |   1.330 μs (5%) |         |                 |             |
| `["dot", "man"]`                                               |   1.330 μs (5%) |         |                 |             |
| `["dot", "rf"]`                                                |   2.130 μs (5%) |         |                 |             |
| `["dot", "xf"]`                                                |   2.456 μs (5%) |         |   64 bytes (1%) |           3 |
| `["filter_map_map!", "man"]`                                   |  57.901 μs (5%) |         |                 |             |
| `["filter_map_map!", "xf"]`                                    | 646.413 μs (5%) |         |   80 bytes (1%) |           3 |
| `["filter_map_reduce", "man"]`                                 | 191.905 μs (5%) |         |                 |             |
| `["filter_map_reduce", "xf"]`                                  | 191.905 μs (5%) |         |                 |             |
| `["filter_sum", "1000", "RandomFloats", "noinit", "base"]`     |   1.240 μs (5%) |         |                 |             |
| `["filter_sum", "1000", "RandomFloats", "noinit", "naive"]`    |   1.240 μs (5%) |         |                 |             |
| `["filter_sum", "1000", "RandomFloats", "noinit", "xf"]`       |   1.980 μs (5%) |         |                 |             |
| `["filter_sum", "1000", "RandomFloats", "withinit", "base"]`   |   1.720 μs (5%) |         |                 |             |
| `["filter_sum", "1000", "RandomFloats", "withinit", "naive"]`  | 900.000 ns (5%) |         |                 |             |
| `["filter_sum", "1000", "RandomFloats", "withinit", "xf"]`     |   1.980 μs (5%) |         |                 |             |
| `["filter_sum", "1000", "UnitRange", "noinit", "base"]`        |   2.010 μs (5%) |         |                 |             |
| `["filter_sum", "1000", "UnitRange", "noinit", "naive"]`       |   1.130 μs (5%) |         |                 |             |
| `["filter_sum", "1000", "UnitRange", "noinit", "xf"]`          | 102.079 ns (5%) |         |                 |             |
| `["filter_sum", "1000", "UnitRange", "withinit", "base"]`      |  88.336 ns (5%) |         |                 |             |
| `["filter_sum", "1000", "UnitRange", "withinit", "naive"]`     | 619.540 ns (5%) |         |                 |             |
| `["filter_sum", "1000", "UnitRange", "withinit", "xf"]`        | 105.708 ns (5%) |         |                 |             |
| `["filter_sum", "10000", "RandomFloats", "noinit", "base"]`    |  46.700 μs (5%) |         |                 |             |
| `["filter_sum", "10000", "RandomFloats", "noinit", "naive"]`   |  59.601 μs (5%) |         |                 |             |
| `["filter_sum", "10000", "RandomFloats", "noinit", "xf"]`      |  17.500 μs (5%) |         |                 |             |
| `["filter_sum", "10000", "RandomFloats", "withinit", "base"]`  |  17.500 μs (5%) |         |                 |             |
| `["filter_sum", "10000", "RandomFloats", "withinit", "naive"]` |  43.100 μs (5%) |         |                 |             |
| `["filter_sum", "10000", "RandomFloats", "withinit", "xf"]`    |  14.700 μs (5%) |         |                 |             |
| `["filter_sum", "10000", "UnitRange", "noinit", "base"]`       |  17.400 μs (5%) |         |                 |             |
| `["filter_sum", "10000", "UnitRange", "noinit", "naive"]`      |  11.100 μs (5%) |         |                 |             |
| `["filter_sum", "10000", "UnitRange", "noinit", "xf"]`         |   1.129 μs (5%) |         |                 |             |
| `["filter_sum", "10000", "UnitRange", "withinit", "base"]`     |   1.110 μs (5%) |         |                 |             |
| `["filter_sum", "10000", "UnitRange", "withinit", "naive"]`    |   8.067 μs (5%) |         |                 |             |
| `["filter_sum", "10000", "UnitRange", "withinit", "xf"]`       |   1.290 μs (5%) |         |                 |             |
| `["findall", "base"]`                                          | 953.926 μs (5%) |         |   2.00 MiB (1%) |          18 |
| `["findall", "xf-array"]`                                      | 676.519 μs (5%) |         |   3.02 MiB (1%) |       98829 |
| `["findall", "xf-iter"]`                                       | 384.711 μs (5%) |         |   2.00 MiB (1%) |          19 |
| `["gemm", "fusedmul", "blas", "16"]`                           |   3.496 ms (5%) |         |                 |             |
| `["gemm", "fusedmul", "blas", "2"]`                            |   2.781 ms (5%) |         |                 |             |
| `["gemm", "fusedmul", "blas", "32"]`                           |   4.233 ms (5%) |         |                 |             |
| `["gemm", "fusedmul", "blas", "8"]`                            |   2.983 ms (5%) |         |                 |             |
| `["gemm", "fusedmul", "xf", "16"]`                             |   5.822 ms (5%) |         |  192 bytes (1%) |           4 |
| `["gemm", "fusedmul", "xf", "2"]`                              | 706.015 μs (5%) |         |  192 bytes (1%) |           4 |
| `["gemm", "fusedmul", "xf", "32"]`                             |  11.726 ms (5%) |         |  192 bytes (1%) |           4 |
| `["gemm", "fusedmul", "xf", "8"]`                              |   2.800 ms (5%) |         |  192 bytes (1%) |           4 |
| `["gemm", "mul", "linalg", "256"]`                             | 418.610 μs (5%) |         |                 |             |
| `["gemm", "mul", "linalg", "32"]`                              |   2.100 μs (5%) |         |                 |             |
| `["gemm", "mul", "linalg", "8"]`                               | 200.000 ns (5%) |         |                 |             |
| `["gemm", "mul", "man", "false", "256"]`                       |   1.737 ms (5%) |         |                 |             |
| `["gemm", "mul", "man", "false", "32"]`                        |   4.700 μs (5%) |         |                 |             |
| `["gemm", "mul", "man", "false", "8"]`                         | 400.000 ns (5%) |         |                 |             |
| `["gemm", "mul", "man", "ivdep", "256"]`                       |   1.670 ms (5%) |         |                 |             |
| `["gemm", "mul", "man", "ivdep", "32"]`                        |   4.000 μs (5%) |         |                 |             |
| `["gemm", "mul", "man", "ivdep", "8"]`                         | 400.000 ns (5%) |         |                 |             |
| `["gemm", "mul", "man", "true", "256"]`                        |   1.573 ms (5%) |         |                 |             |
| `["gemm", "mul", "man", "true", "32"]`                         |   4.000 μs (5%) |         |                 |             |
| `["gemm", "mul", "man", "true", "8"]`                          | 400.000 ns (5%) |         |                 |             |
| `["gemm", "mul", "xf", "false", "256"]`                        |   1.673 ms (5%) |         |   80 bytes (1%) |           3 |
| `["gemm", "mul", "xf", "false", "32"]`                         |   4.500 μs (5%) |         |   80 bytes (1%) |           3 |
| `["gemm", "mul", "xf", "false", "8"]`                          | 700.000 ns (5%) |         |   80 bytes (1%) |           3 |
| `["gemm", "mul", "xf", "ivdep", "256"]`                        |   1.611 ms (5%) |         |   80 bytes (1%) |           3 |
| `["gemm", "mul", "xf", "ivdep", "32"]`                         |   4.100 μs (5%) |         |   80 bytes (1%) |           3 |
| `["gemm", "mul", "xf", "ivdep", "8"]`                          | 400.000 ns (5%) |         |   80 bytes (1%) |           3 |
| `["gemm", "mul", "xf", "true", "256"]`                         |   1.600 ms (5%) |         |   80 bytes (1%) |           3 |
| `["gemm", "mul", "xf", "true", "32"]`                          |   5.300 μs (5%) |         |   80 bytes (1%) |           3 |
| `["gemm", "mul", "xf", "true", "8"]`                           | 600.000 ns (5%) |         |   80 bytes (1%) |           3 |
| `["groupby", "sum", "sac"]`                                    | 169.503 μs (5%) |         |  624 bytes (1%) |           5 |
| `["groupby", "sum", "xf-with-init"]`                           | 141.002 μs (5%) |         |   1.20 KiB (1%) |           9 |
| `["groupby", "sum", "xf-without-init"]`                        | 141.102 μs (5%) |         |   1.20 KiB (1%) |           9 |
| `["mapcat_eduction", "base"]`                                  |   2.100 μs (5%) |         |                 |             |
| `["mapcat_eduction", "xf-eduction"]`                           |   1.390 μs (5%) |         |                 |             |
| `["mapcat_eduction", "xf-xf"]`                                 |   1.390 μs (5%) |         |                 |             |
| `["missing_argmax", "man"]`                                    |   2.233 μs (5%) |         |   32 bytes (1%) |           1 |
| `["missing_argmax", "rf"]`                                     |   2.080 μs (5%) |         |   32 bytes (1%) |           1 |
| `["missing_argmax", "xf"]`                                     |   1.800 μs (5%) |         |   32 bytes (1%) |           1 |
| `["missing_dot", "equiv"]`                                     |   1.770 μs (5%) |         |   16 bytes (1%) |           1 |
| `["missing_dot", "man"]`                                       |   1.180 μs (5%) |         |   16 bytes (1%) |           1 |
| `["missing_dot", "naive"]`                                     |   5.457 μs (5%) |         |   16 bytes (1%) |           1 |
| `["missing_dot", "rf"]`                                        |   1.550 μs (5%) |         |   16 bytes (1%) |           1 |
| `["missing_dot", "rf_nota"]`                                   |   2.040 μs (5%) |         |   16 bytes (1%) |           1 |
| `["missing_dot", "xf"]`                                        |  91.902 μs (5%) |         |  72.02 KiB (1%) |        3738 |
| `["missing_dot", "xf_nota"]`                                   |  95.903 μs (5%) |         |  72.20 KiB (1%) |        3746 |
| `["overhead", "foldl"]`                                        |   5.200 ns (5%) |         |                 |             |
| `["overhead", "reduce_basecase"]`                              | 221.547 ns (5%) |         |  368 bytes (1%) |           6 |
| `["partition_by", "man"]`                                      |   2.470 ms (5%) |         |  352 bytes (1%) |           4 |
| `["partition_by", "xf"]`                                       |   2.426 ms (5%) |         |  544 bytes (1%) |           6 |
| `["set", "base"]`                                              |   5.123 ms (5%) |         |  49.56 KiB (1%) |          17 |
| `["set", "xf"]`                                                |   4.915 ms (5%) |         |  49.59 KiB (1%) |          19 |
| `["sum_transpose", "30", "noinit", "iter"]`                    |   2.189 μs (5%) |         |                 |             |
| `["sum_transpose", "30", "noinit", "man"]`                     |   2.467 μs (5%) |         |                 |             |
| `["sum_transpose", "30", "noinit", "xf"]`                      |   1.410 μs (5%) |         |   32 bytes (1%) |           2 |
| `["sum_transpose", "30", "withinit", "iter"]`                  |   1.490 μs (5%) |         |                 |             |
| `["sum_transpose", "30", "withinit", "man"]`                   |   1.114 μs (5%) |         |                 |             |
| `["sum_transpose", "30", "withinit", "xf"]`                    |   1.360 μs (5%) |         |   48 bytes (1%) |           3 |
| `["teerf_filter", "noinit"]`                                   | 409.135 ns (5%) |         |  112 bytes (1%) |           4 |
| `["teerf_filter", "withinit"]`                                 | 191.582 ns (5%) |         |                 |             |

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
Julia Version 1.5.1
Commit 697e782ab8 (2020-08-25 20:08 UTC)
Platform Info:
  OS: Linux (x86_64-pc-linux-gnu)
      Ubuntu 18.04.5 LTS
  uname: Linux 5.4.0-1023-azure #23~18.04.1-Ubuntu SMP Thu Aug 20 14:46:48 UTC 2020 x86_64 x86_64
  CPU: Intel(R) Xeon(R) Platinum 8171M CPU @ 2.60GHz: 
              speed         user         nice          sys         idle          irq
       #1  2095 MHz      55353 s          0 s       1685 s      57660 s          0 s
       #2  2095 MHz      52834 s          0 s       1840 s      60172 s          0 s
       
  Memory: 6.791393280029297 GB (3038.2421875 MB free)
  Uptime: 1166.0 sec
  Load Avg:  1.00146484375  1.0146484375  0.791015625
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
    CPU MHz:             2095.081
    BogoMIPS:            4190.16
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

