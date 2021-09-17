# Benchmark result

* Pull request commit: [`64aef1fc0773e87da1ee03b52b3f39a8e64e83d1`](https://github.com/JuliaFolds/Transducers.jl/commit/64aef1fc0773e87da1ee03b52b3f39a8e64e83d1)
* Pull request: <https://github.com/JuliaFolds/Transducers.jl/pull/243> (Update */Manifest.toml)

# Judge result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmarks:
    - Target: 17 Sep 2021 - 01:25
    - Baseline: 17 Sep 2021 - 01:30
* Package commits:
    - Target: a6a467
    - Baseline: 9ac175
* Julia commits:
    - Target: 69fcb5
    - Baseline: 69fcb5
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
| `["append!!", "eduction"]`                                     |                1.12 (5%) :x: |    1.00 (1%)  |
| `["cartesian", "copyto!", "iter"]`                             | 0.86 (5%) :white_check_mark: |    1.00 (1%)  |
| `["cartesian", "copyto!", "man"]`                              | 0.78 (5%) :white_check_mark: |    1.00 (1%)  |
| `["cartesian", "copyto!", "xf"]`                               | 0.93 (5%) :white_check_mark: |    1.00 (1%)  |
| `["cat", "base"]`                                              |                1.16 (5%) :x: |    1.00 (1%)  |
| `["cat", "xf"]`                                                | 0.86 (5%) :white_check_mark: |    1.00 (1%)  |
| `["dict", "xf"]`                                               | 0.91 (5%) :white_check_mark: |    1.00 (1%)  |
| `["filter_sum", "1000", "RandomFloats", "noinit", "base"]`     | 0.87 (5%) :white_check_mark: |    1.00 (1%)  |
| `["filter_sum", "1000", "RandomFloats", "noinit", "naive"]`    | 0.86 (5%) :white_check_mark: |    1.00 (1%)  |
| `["filter_sum", "1000", "RandomFloats", "withinit", "base"]`   |                1.17 (5%) :x: |    1.00 (1%)  |
| `["filter_sum", "1000", "RandomFloats", "withinit", "naive"]`  |                1.30 (5%) :x: |    1.00 (1%)  |
| `["filter_sum", "1000", "RandomFloats", "withinit", "xf"]`     |                1.18 (5%) :x: |    1.00 (1%)  |
| `["filter_sum", "1000", "UnitRange", "noinit", "naive"]`       |                1.14 (5%) :x: |    1.00 (1%)  |
| `["filter_sum", "1000", "UnitRange", "noinit", "xf"]`          |                1.06 (5%) :x: |    1.00 (1%)  |
| `["filter_sum", "1000", "UnitRange", "withinit", "base"]`      |                1.14 (5%) :x: |    1.00 (1%)  |
| `["filter_sum", "1000", "UnitRange", "withinit", "naive"]`     | 0.78 (5%) :white_check_mark: |    1.00 (1%)  |
| `["filter_sum", "10000", "RandomFloats", "noinit", "naive"]`   | 0.86 (5%) :white_check_mark: |    1.00 (1%)  |
| `["filter_sum", "10000", "RandomFloats", "noinit", "xf"]`      |                1.16 (5%) :x: |    1.00 (1%)  |
| `["filter_sum", "10000", "RandomFloats", "withinit", "base"]`  |                1.14 (5%) :x: |    1.00 (1%)  |
| `["filter_sum", "10000", "RandomFloats", "withinit", "naive"]` | 0.87 (5%) :white_check_mark: |    1.00 (1%)  |
| `["filter_sum", "10000", "UnitRange", "noinit", "naive"]`      | 0.89 (5%) :white_check_mark: |    1.00 (1%)  |
| `["filter_sum", "10000", "UnitRange", "withinit", "base"]`     |                1.15 (5%) :x: |    1.00 (1%)  |
| `["filter_sum", "10000", "UnitRange", "withinit", "naive"]`    |                1.06 (5%) :x: |    1.00 (1%)  |
| `["filter_sum", "10000", "UnitRange", "withinit", "xf"]`       | 0.86 (5%) :white_check_mark: |    1.00 (1%)  |
| `["findall", "base"]`                                          | 0.92 (5%) :white_check_mark: |    1.00 (1%)  |
| `["findall", "xf-array"]`                                      | 0.81 (5%) :white_check_mark: |    1.00 (1%)  |
| `["findall", "xf-iter"]`                                       | 0.90 (5%) :white_check_mark: |    1.00 (1%)  |
| `["gemm", "fusedmul", "blas", "16"]`                           | 0.93 (5%) :white_check_mark: |    1.00 (1%)  |
| `["gemm", "fusedmul", "blas", "2"]`                            | 0.94 (5%) :white_check_mark: |    1.00 (1%)  |
| `["gemm", "fusedmul", "blas", "8"]`                            | 0.94 (5%) :white_check_mark: |    1.00 (1%)  |
| `["gemm", "mul", "linalg", "256"]`                             |                1.09 (5%) :x: |    1.00 (1%)  |
| `["gemm", "mul", "linalg", "32"]`                              | 0.89 (5%) :white_check_mark: |    1.00 (1%)  |
| `["gemm", "mul", "man", "false", "256"]`                       | 0.94 (5%) :white_check_mark: |    1.00 (1%)  |
| `["gemm", "mul", "man", "false", "32"]`                        | 0.84 (5%) :white_check_mark: |    1.00 (1%)  |
| `["gemm", "mul", "man", "ivdep", "32"]`                        | 0.77 (5%) :white_check_mark: |    1.00 (1%)  |
| `["gemm", "mul", "man", "true", "32"]`                         | 0.85 (5%) :white_check_mark: |    1.00 (1%)  |
| `["gemm", "mul", "man", "true", "8"]`                          | 0.80 (5%) :white_check_mark: |    1.00 (1%)  |
| `["gemm", "mul", "xf", "false", "256"]`                        |                1.10 (5%) :x: |    1.00 (1%)  |
| `["gemm", "mul", "xf", "false", "32"]`                         | 0.81 (5%) :white_check_mark: |    1.00 (1%)  |
| `["gemm", "mul", "xf", "false", "8"]`                          | 0.72 (5%) :white_check_mark: |    1.00 (1%)  |
| `["gemm", "mul", "xf", "ivdep", "256"]`                        |                1.06 (5%) :x: |    1.00 (1%)  |
| `["gemm", "mul", "xf", "ivdep", "8"]`                          | 0.88 (5%) :white_check_mark: |    1.00 (1%)  |
| `["gemm", "mul", "xf", "true", "32"]`                          | 0.75 (5%) :white_check_mark: |    1.00 (1%)  |
| `["gemm", "mul", "xf", "true", "8"]`                           | 0.90 (5%) :white_check_mark: |    1.00 (1%)  |
| `["groupby", "sum", "sac"]`                                    |                   0.95 (5%)  | 2.10 (1%) :x: |
| `["groupby", "sum", "xf-without-init"]`                        | 0.95 (5%) :white_check_mark: |    1.00 (1%)  |
| `["mapcat_eduction", "base"]`                                  |                1.15 (5%) :x: |    1.00 (1%)  |
| `["mapcat_eduction", "xf-eduction"]`                           | 0.94 (5%) :white_check_mark: |    1.00 (1%)  |
| `["missing_argmax", "rf"]`                                     |                1.13 (5%) :x: |    1.00 (1%)  |
| `["missing_dot", "equiv"]`                                     |                1.18 (5%) :x: |    1.00 (1%)  |
| `["missing_dot", "naive"]`                                     | 0.87 (5%) :white_check_mark: |    1.00 (1%)  |
| `["missing_dot", "rf"]`                                        |                1.18 (5%) :x: |    1.00 (1%)  |
| `["missing_dot", "rf_nota"]`                                   | 0.79 (5%) :white_check_mark: |    1.00 (1%)  |
| `["overhead", "foldl"]`                                        |                1.33 (5%) :x: |    1.00 (1%)  |
| `["partition_by", "xf"]`                                       | 0.79 (5%) :white_check_mark: |    1.00 (1%)  |
| `["set", "base"]`                                              |                1.06 (5%) :x: |    1.00 (1%)  |
| `["set", "xf"]`                                                |                1.09 (5%) :x: |    1.00 (1%)  |
| `["sum_transpose", "30", "noinit", "iter"]`                    | 0.86 (5%) :white_check_mark: |    1.00 (1%)  |
| `["sum_transpose", "30", "noinit", "xf"]`                      | 0.87 (5%) :white_check_mark: |    1.00 (1%)  |
| `["sum_transpose", "30", "withinit", "xf"]`                    | 0.86 (5%) :white_check_mark: |    1.00 (1%)  |
| `["teerf_filter", "noinit"]`                                   | 0.87 (5%) :white_check_mark: |    1.00 (1%)  |
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
Julia Version 1.5.4
Commit 69fcb5745b (2021-03-11 19:13 UTC)
Platform Info:
  OS: Linux (x86_64-pc-linux-gnu)
      Ubuntu 20.04.3 LTS
  uname: Linux 5.8.0-1041-azure #44~20.04.1-Ubuntu SMP Fri Aug 20 20:41:09 UTC 2021 x86_64 x86_64
  CPU: Intel(R) Xeon(R) Platinum 8171M CPU @ 2.60GHz: 
              speed         user         nice          sys         idle          irq
       #1  2095 MHz       6294 s         14 s       1400 s      99195 s          0 s
       #2  2095 MHz      74168 s          8 s       1669 s      31394 s          0 s
       
  Memory: 6.790924072265625 GB (3266.61328125 MB free)
  Uptime: 1077.0 sec
  Load Avg:  1.0  0.97314453125  0.669921875
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-9.0.1 (ORCJIT, skylake-avx512)
```

### Baseline
```
Julia Version 1.5.4
Commit 69fcb5745b (2021-03-11 19:13 UTC)
Platform Info:
  OS: Linux (x86_64-pc-linux-gnu)
      Ubuntu 20.04.3 LTS
  uname: Linux 5.8.0-1041-azure #44~20.04.1-Ubuntu SMP Fri Aug 20 20:41:09 UTC 2021 x86_64 x86_64
  CPU: Intel(R) Xeon(R) Platinum 8171M CPU @ 2.60GHz: 
              speed         user         nice          sys         idle          irq
       #1  2095 MHz      37048 s         14 s       1714 s     101712 s          0 s
       #2  2095 MHz      76567 s          8 s       1916 s      62196 s          0 s
       
  Memory: 6.790924072265625 GB (3203.55859375 MB free)
  Uptime: 1413.0 sec
  Load Avg:  1.02978515625  1.04443359375  0.81494140625
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-9.0.1 (ORCJIT, skylake-avx512)
```

---
# Target result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmark: 17 Sep 2021 - 1:25
* Package commit: a6a467
* Julia commit: 69fcb5
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
| `["append!!", "eduction"]`                                     |  19.901 μs (5%) |         |  64.63 KiB (1%) |          13 |
| `["append!!", "xf"]`                                           |  18.401 μs (5%) |         |  64.63 KiB (1%) |          13 |
| `["cartesian", "copyto!", "iter"]`                             |   5.034 μs (5%) |         |                 |             |
| `["cartesian", "copyto!", "man"]`                              |   1.778 μs (5%) |         |                 |             |
| `["cartesian", "copyto!", "xf"]`                               |   2.700 μs (5%) |         |                 |             |
| `["cat", "base"]`                                              |   2.600 μs (5%) |         |                 |             |
| `["cat", "xf"]`                                                |   1.380 μs (5%) |         |                 |             |
| `["collect", "filter-missing"]`                                |  56.404 μs (5%) |         |  32.81 KiB (1%) |          14 |
| `["collect", "identity-float"]`                                |  27.202 μs (5%) |         | 256.66 KiB (1%) |          14 |
| `["collect", "identity-union"]`                                | 136.308 μs (5%) |         | 601.07 KiB (1%) |       10014 |
| `["dict", "base"]`                                             |   4.093 ms (5%) |         |  92.91 KiB (1%) |          22 |
| `["dict", "xf"]`                                               |   3.684 ms (5%) |         |  92.31 KiB (1%) |          18 |
| `["dot", "blas"]`                                              |   1.160 μs (5%) |         |                 |             |
| `["dot", "man"]`                                               |   1.160 μs (5%) |         |                 |             |
| `["dot", "rf"]`                                                |   1.810 μs (5%) |         |                 |             |
| `["dot", "xf"]`                                                |   1.890 μs (5%) |         |   64 bytes (1%) |           3 |
| `["filter_map_map!", "man"]`                                   |  56.603 μs (5%) |         |                 |             |
| `["filter_map_map!", "xf"]`                                    | 591.138 μs (5%) |         |   80 bytes (1%) |           3 |
| `["filter_map_reduce", "man"]`                                 | 191.812 μs (5%) |         |                 |             |
| `["filter_map_reduce", "xf"]`                                  | 191.712 μs (5%) |         |                 |             |
| `["filter_sum", "1000", "RandomFloats", "noinit", "base"]`     |   1.240 μs (5%) |         |                 |             |
| `["filter_sum", "1000", "RandomFloats", "noinit", "naive"]`    |   1.070 μs (5%) |         |                 |             |
| `["filter_sum", "1000", "RandomFloats", "noinit", "xf"]`       |   1.730 μs (5%) |         |                 |             |
| `["filter_sum", "1000", "RandomFloats", "withinit", "base"]`   |   1.730 μs (5%) |         |                 |             |
| `["filter_sum", "1000", "RandomFloats", "withinit", "naive"]`  |   1.004 μs (5%) |         |                 |             |
| `["filter_sum", "1000", "RandomFloats", "withinit", "xf"]`     |   1.720 μs (5%) |         |                 |             |
| `["filter_sum", "1000", "UnitRange", "noinit", "base"]`        |   1.760 μs (5%) |         |                 |             |
| `["filter_sum", "1000", "UnitRange", "noinit", "naive"]`       |   1.300 μs (5%) |         |                 |             |
| `["filter_sum", "1000", "UnitRange", "noinit", "xf"]`          | 107.641 ns (5%) |         |                 |             |
| `["filter_sum", "1000", "UnitRange", "withinit", "base"]`      | 100.537 ns (5%) |         |                 |             |
| `["filter_sum", "1000", "UnitRange", "withinit", "naive"]`     | 705.676 ns (5%) |         |                 |             |
| `["filter_sum", "1000", "UnitRange", "withinit", "xf"]`        | 105.675 ns (5%) |         |                 |             |
| `["filter_sum", "10000", "RandomFloats", "noinit", "base"]`    |  35.702 μs (5%) |         |                 |             |
| `["filter_sum", "10000", "RandomFloats", "noinit", "naive"]`   |  39.003 μs (5%) |         |                 |             |
| `["filter_sum", "10000", "RandomFloats", "noinit", "xf"]`      |  17.501 μs (5%) |         |                 |             |
| `["filter_sum", "10000", "RandomFloats", "withinit", "base"]`  |  19.501 μs (5%) |         |                 |             |
| `["filter_sum", "10000", "RandomFloats", "withinit", "naive"]` |  37.003 μs (5%) |         |                 |             |
| `["filter_sum", "10000", "RandomFloats", "withinit", "xf"]`    |  15.101 μs (5%) |         |                 |             |
| `["filter_sum", "10000", "UnitRange", "noinit", "base"]`       |  15.001 μs (5%) |         |                 |             |
| `["filter_sum", "10000", "UnitRange", "noinit", "naive"]`      |  10.101 μs (5%) |         |                 |             |
| `["filter_sum", "10000", "UnitRange", "noinit", "xf"]`         | 970.000 ns (5%) |         |                 |             |
| `["filter_sum", "10000", "UnitRange", "withinit", "base"]`     | 963.068 ns (5%) |         |                 |             |
| `["filter_sum", "10000", "UnitRange", "withinit", "naive"]`    |   8.101 μs (5%) |         |                 |             |
| `["filter_sum", "10000", "UnitRange", "withinit", "xf"]`       | 970.000 ns (5%) |         |                 |             |
| `["findall", "base"]`                                          | 748.248 μs (5%) |         |   2.00 MiB (1%) |          18 |
| `["findall", "xf-array"]`                                      | 679.743 μs (5%) |         |   3.02 MiB (1%) |       98829 |
| `["findall", "xf-iter"]`                                       | 304.120 μs (5%) |         |   2.00 MiB (1%) |          19 |
| `["gemm", "fusedmul", "blas", "16"]`                           |   3.174 ms (5%) |         |                 |             |
| `["gemm", "fusedmul", "blas", "2"]`                            |   2.615 ms (5%) |         |                 |             |
| `["gemm", "fusedmul", "blas", "32"]`                           |   4.275 ms (5%) |         |                 |             |
| `["gemm", "fusedmul", "blas", "8"]`                            |   2.881 ms (5%) |         |                 |             |
| `["gemm", "fusedmul", "xf", "16"]`                             |   5.639 ms (5%) |         |  192 bytes (1%) |           4 |
| `["gemm", "fusedmul", "xf", "2"]`                              | 676.944 μs (5%) |         |  192 bytes (1%) |           4 |
| `["gemm", "fusedmul", "xf", "32"]`                             |  11.594 ms (5%) |         |  192 bytes (1%) |           4 |
| `["gemm", "fusedmul", "xf", "8"]`                              |   2.823 ms (5%) |         |  192 bytes (1%) |           4 |
| `["gemm", "mul", "linalg", "256"]`                             | 444.229 μs (5%) |         |                 |             |
| `["gemm", "mul", "linalg", "32"]`                              |   1.770 μs (5%) |         |                 |             |
| `["gemm", "mul", "linalg", "8"]`                               | 197.191 ns (5%) |         |                 |             |
| `["gemm", "mul", "man", "false", "256"]`                       |   1.422 ms (5%) |         |                 |             |
| `["gemm", "mul", "man", "false", "32"]`                        |   4.686 μs (5%) |         |                 |             |
| `["gemm", "mul", "man", "false", "8"]`                         | 390.477 ns (5%) |         |                 |             |
| `["gemm", "mul", "man", "ivdep", "256"]`                       |   1.450 ms (5%) |         |                 |             |
| `["gemm", "mul", "man", "ivdep", "32"]`                        |   3.150 μs (5%) |         |                 |             |
| `["gemm", "mul", "man", "ivdep", "8"]`                         | 394.552 ns (5%) |         |                 |             |
| `["gemm", "mul", "man", "true", "256"]`                        |   1.419 ms (5%) |         |                 |             |
| `["gemm", "mul", "man", "true", "32"]`                         |   4.000 μs (5%) |         |                 |             |
| `["gemm", "mul", "man", "true", "8"]`                          | 319.020 ns (5%) |         |                 |             |
| `["gemm", "mul", "xf", "false", "256"]`                        |   1.518 ms (5%) |         |   80 bytes (1%) |           3 |
| `["gemm", "mul", "xf", "false", "32"]`                         |   3.872 μs (5%) |         |   80 bytes (1%) |           3 |
| `["gemm", "mul", "xf", "false", "8"]`                          | 359.919 ns (5%) |         |   80 bytes (1%) |           3 |
| `["gemm", "mul", "xf", "ivdep", "256"]`                        |   1.498 ms (5%) |         |   80 bytes (1%) |           3 |
| `["gemm", "mul", "xf", "ivdep", "32"]`                         |   3.600 μs (5%) |         |   80 bytes (1%) |           3 |
| `["gemm", "mul", "xf", "ivdep", "8"]`                          | 352.525 ns (5%) |         |   80 bytes (1%) |           3 |
| `["gemm", "mul", "xf", "true", "256"]`                         |   1.423 ms (5%) |         |   80 bytes (1%) |           3 |
| `["gemm", "mul", "xf", "true", "32"]`                          |   4.114 μs (5%) |         |   80 bytes (1%) |           3 |
| `["gemm", "mul", "xf", "true", "8"]`                           | 358.814 ns (5%) |         |   80 bytes (1%) |           3 |
| `["groupby", "sum", "sac"]`                                    | 160.311 μs (5%) |         |   1.28 KiB (1%) |          14 |
| `["groupby", "sum", "xf-with-init"]`                           | 135.108 μs (5%) |         |   1.20 KiB (1%) |           9 |
| `["groupby", "sum", "xf-without-init"]`                        | 134.609 μs (5%) |         |   1.20 KiB (1%) |           9 |
| `["mapcat_eduction", "base"]`                                  |   1.830 μs (5%) |         |                 |             |
| `["mapcat_eduction", "xf-eduction"]`                           |   1.630 μs (5%) |         |                 |             |
| `["mapcat_eduction", "xf-xf"]`                                 |   1.400 μs (5%) |         |                 |             |
| `["missing_argmax", "man"]`                                    |   2.233 μs (5%) |         |   32 bytes (1%) |           1 |
| `["missing_argmax", "rf"]`                                     |   1.490 μs (5%) |         |   32 bytes (1%) |           1 |
| `["missing_argmax", "xf"]`                                     |   1.370 μs (5%) |         |   32 bytes (1%) |           1 |
| `["missing_dot", "equiv"]`                                     |   2.000 μs (5%) |         |   16 bytes (1%) |           1 |
| `["missing_dot", "man"]`                                       |   1.200 μs (5%) |         |   16 bytes (1%) |           1 |
| `["missing_dot", "naive"]`                                     |   4.129 μs (5%) |         |   16 bytes (1%) |           1 |
| `["missing_dot", "rf"]`                                        |   1.390 μs (5%) |         |   16 bytes (1%) |           1 |
| `["missing_dot", "rf_nota"]`                                   |   2.010 μs (5%) |         |   16 bytes (1%) |           1 |
| `["missing_dot", "xf"]`                                        |  85.306 μs (5%) |         |  72.02 KiB (1%) |        3738 |
| `["missing_dot", "xf_nota"]`                                   |  82.405 μs (5%) |         |  72.13 KiB (1%) |        3743 |
| `["overhead", "foldl"]`                                        |   5.200 ns (5%) |         |                 |             |
| `["overhead", "reduce_basecase"]`                              | 120.862 ns (5%) |         |   48 bytes (1%) |           2 |
| `["partition_by", "man"]`                                      |   2.027 ms (5%) |         |  352 bytes (1%) |           4 |
| `["partition_by", "xf"]`                                       |   1.833 ms (5%) |         |  544 bytes (1%) |           6 |
| `["set", "base"]`                                              |   4.916 ms (5%) |         |  49.56 KiB (1%) |          17 |
| `["set", "xf"]`                                                |   4.836 ms (5%) |         |  49.59 KiB (1%) |          19 |
| `["sum_transpose", "30", "noinit", "iter"]`                    |   1.880 μs (5%) |         |                 |             |
| `["sum_transpose", "30", "noinit", "man"]`                     |   2.122 μs (5%) |         |                 |             |
| `["sum_transpose", "30", "noinit", "xf"]`                      |   1.230 μs (5%) |         |   32 bytes (1%) |           2 |
| `["sum_transpose", "30", "withinit", "iter"]`                  |   1.490 μs (5%) |         |                 |             |
| `["sum_transpose", "30", "withinit", "man"]`                   | 956.565 ns (5%) |         |                 |             |
| `["sum_transpose", "30", "withinit", "xf"]`                    |   1.020 μs (5%) |         |   48 bytes (1%) |           3 |
| `["teerf_filter", "noinit"]`                                   |   1.856 μs (5%) |         |  176 bytes (1%) |           7 |
| `["teerf_filter", "withinit"]`                                 | 189.933 ns (5%) |         |                 |             |

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
Julia Version 1.5.4
Commit 69fcb5745b (2021-03-11 19:13 UTC)
Platform Info:
  OS: Linux (x86_64-pc-linux-gnu)
      Ubuntu 20.04.3 LTS
  uname: Linux 5.8.0-1041-azure #44~20.04.1-Ubuntu SMP Fri Aug 20 20:41:09 UTC 2021 x86_64 x86_64
  CPU: Intel(R) Xeon(R) Platinum 8171M CPU @ 2.60GHz: 
              speed         user         nice          sys         idle          irq
       #1  2095 MHz       6294 s         14 s       1400 s      99195 s          0 s
       #2  2095 MHz      74168 s          8 s       1669 s      31394 s          0 s
       
  Memory: 6.790924072265625 GB (3266.61328125 MB free)
  Uptime: 1077.0 sec
  Load Avg:  1.0  0.97314453125  0.669921875
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-9.0.1 (ORCJIT, skylake-avx512)
```

---
# Baseline result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmark: 17 Sep 2021 - 1:30
* Package commit: 9ac175
* Julia commit: 69fcb5
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
| `["append!!", "eduction"]`                                     |  17.801 μs (5%) |         |  64.63 KiB (1%) |          13 |
| `["append!!", "xf"]`                                           |  18.601 μs (5%) |         |  64.63 KiB (1%) |          13 |
| `["cartesian", "copyto!", "iter"]`                             |   5.850 μs (5%) |         |                 |             |
| `["cartesian", "copyto!", "man"]`                              |   2.289 μs (5%) |         |                 |             |
| `["cartesian", "copyto!", "xf"]`                               |   2.900 μs (5%) |         |                 |             |
| `["cat", "base"]`                                              |   2.233 μs (5%) |         |                 |             |
| `["cat", "xf"]`                                                |   1.610 μs (5%) |         |                 |             |
| `["collect", "filter-missing"]`                                |  57.804 μs (5%) |         |  32.81 KiB (1%) |          14 |
| `["collect", "identity-float"]`                                |  26.602 μs (5%) |         | 256.66 KiB (1%) |          14 |
| `["collect", "identity-union"]`                                | 130.809 μs (5%) |         | 601.07 KiB (1%) |       10014 |
| `["dict", "base"]`                                             |   4.009 ms (5%) |         |  92.91 KiB (1%) |          22 |
| `["dict", "xf"]`                                               |   4.060 ms (5%) |         |  92.31 KiB (1%) |          18 |
| `["dot", "blas"]`                                              |   1.190 μs (5%) |         |                 |             |
| `["dot", "man"]`                                               |   1.150 μs (5%) |         |                 |             |
| `["dot", "rf"]`                                                |   1.810 μs (5%) |         |                 |             |
| `["dot", "xf"]`                                                |   1.910 μs (5%) |         |   64 bytes (1%) |           3 |
| `["filter_map_map!", "man"]`                                   |  58.103 μs (5%) |         |                 |             |
| `["filter_map_map!", "xf"]`                                    | 596.639 μs (5%) |         |   80 bytes (1%) |           3 |
| `["filter_map_reduce", "man"]`                                 | 191.912 μs (5%) |         |                 |             |
| `["filter_map_reduce", "xf"]`                                  | 192.012 μs (5%) |         |                 |             |
| `["filter_sum", "1000", "RandomFloats", "noinit", "base"]`     |   1.420 μs (5%) |         |                 |             |
| `["filter_sum", "1000", "RandomFloats", "noinit", "naive"]`    |   1.240 μs (5%) |         |                 |             |
| `["filter_sum", "1000", "RandomFloats", "noinit", "xf"]`       |   1.720 μs (5%) |         |                 |             |
| `["filter_sum", "1000", "RandomFloats", "withinit", "base"]`   |   1.480 μs (5%) |         |                 |             |
| `["filter_sum", "1000", "RandomFloats", "withinit", "naive"]`  | 773.719 ns (5%) |         |                 |             |
| `["filter_sum", "1000", "RandomFloats", "withinit", "xf"]`     |   1.460 μs (5%) |         |                 |             |
| `["filter_sum", "1000", "UnitRange", "noinit", "base"]`        |   1.750 μs (5%) |         |                 |             |
| `["filter_sum", "1000", "UnitRange", "noinit", "naive"]`       |   1.140 μs (5%) |         |                 |             |
| `["filter_sum", "1000", "UnitRange", "noinit", "xf"]`          | 101.189 ns (5%) |         |                 |             |
| `["filter_sum", "1000", "UnitRange", "withinit", "base"]`      |  87.903 ns (5%) |         |                 |             |
| `["filter_sum", "1000", "UnitRange", "withinit", "naive"]`     | 900.056 ns (5%) |         |                 |             |
| `["filter_sum", "1000", "UnitRange", "withinit", "xf"]`        | 105.033 ns (5%) |         |                 |             |
| `["filter_sum", "10000", "RandomFloats", "noinit", "base"]`    |  34.602 μs (5%) |         |                 |             |
| `["filter_sum", "10000", "RandomFloats", "noinit", "naive"]`   |  45.203 μs (5%) |         |                 |             |
| `["filter_sum", "10000", "RandomFloats", "noinit", "xf"]`      |  15.101 μs (5%) |         |                 |             |
| `["filter_sum", "10000", "RandomFloats", "withinit", "base"]`  |  17.101 μs (5%) |         |                 |             |
| `["filter_sum", "10000", "RandomFloats", "withinit", "naive"]` |  42.403 μs (5%) |         |                 |             |
| `["filter_sum", "10000", "RandomFloats", "withinit", "xf"]`    |  15.001 μs (5%) |         |                 |             |
| `["filter_sum", "10000", "UnitRange", "noinit", "base"]`       |  15.001 μs (5%) |         |                 |             |
| `["filter_sum", "10000", "UnitRange", "noinit", "naive"]`      |  11.300 μs (5%) |         |                 |             |
| `["filter_sum", "10000", "UnitRange", "noinit", "xf"]`         | 970.100 ns (5%) |         |                 |             |
| `["filter_sum", "10000", "UnitRange", "withinit", "base"]`     | 838.411 ns (5%) |         |                 |             |
| `["filter_sum", "10000", "UnitRange", "withinit", "naive"]`    |   7.676 μs (5%) |         |                 |             |
| `["filter_sum", "10000", "UnitRange", "withinit", "xf"]`       |   1.130 μs (5%) |         |                 |             |
| `["findall", "base"]`                                          | 811.152 μs (5%) |         |   2.00 MiB (1%) |          18 |
| `["findall", "xf-array"]`                                      | 838.754 μs (5%) |         |   3.02 MiB (1%) |       98829 |
| `["findall", "xf-iter"]`                                       | 337.621 μs (5%) |         |   2.00 MiB (1%) |          19 |
| `["gemm", "fusedmul", "blas", "16"]`                           |   3.406 ms (5%) |         |                 |             |
| `["gemm", "fusedmul", "blas", "2"]`                            |   2.779 ms (5%) |         |                 |             |
| `["gemm", "fusedmul", "blas", "32"]`                           |   4.377 ms (5%) |         |                 |             |
| `["gemm", "fusedmul", "blas", "8"]`                            |   3.050 ms (5%) |         |                 |             |
| `["gemm", "fusedmul", "xf", "16"]`                             |   5.764 ms (5%) |         |  192 bytes (1%) |           4 |
| `["gemm", "fusedmul", "xf", "2"]`                              | 683.443 μs (5%) |         |  192 bytes (1%) |           4 |
| `["gemm", "fusedmul", "xf", "32"]`                             |  11.653 ms (5%) |         |  192 bytes (1%) |           4 |
| `["gemm", "fusedmul", "xf", "8"]`                              |   2.805 ms (5%) |         |  192 bytes (1%) |           4 |
| `["gemm", "mul", "linalg", "256"]`                             | 409.426 μs (5%) |         |                 |             |
| `["gemm", "mul", "linalg", "32"]`                              |   2.000 μs (5%) |         |                 |             |
| `["gemm", "mul", "linalg", "8"]`                               | 200.000 ns (5%) |         |                 |             |
| `["gemm", "mul", "man", "false", "256"]`                       |   1.514 ms (5%) |         |                 |             |
| `["gemm", "mul", "man", "false", "32"]`                        |   5.600 μs (5%) |         |                 |             |
| `["gemm", "mul", "man", "false", "8"]`                         | 400.000 ns (5%) |         |                 |             |
| `["gemm", "mul", "man", "ivdep", "256"]`                       |   1.433 ms (5%) |         |                 |             |
| `["gemm", "mul", "man", "ivdep", "32"]`                        |   4.100 μs (5%) |         |                 |             |
| `["gemm", "mul", "man", "ivdep", "8"]`                         | 400.000 ns (5%) |         |                 |             |
| `["gemm", "mul", "man", "true", "256"]`                        |   1.459 ms (5%) |         |                 |             |
| `["gemm", "mul", "man", "true", "32"]`                         |   4.700 μs (5%) |         |                 |             |
| `["gemm", "mul", "man", "true", "8"]`                          | 400.000 ns (5%) |         |                 |             |
| `["gemm", "mul", "xf", "false", "256"]`                        |   1.382 ms (5%) |         |   80 bytes (1%) |           3 |
| `["gemm", "mul", "xf", "false", "32"]`                         |   4.800 μs (5%) |         |   80 bytes (1%) |           3 |
| `["gemm", "mul", "xf", "false", "8"]`                          | 500.000 ns (5%) |         |   80 bytes (1%) |           3 |
| `["gemm", "mul", "xf", "ivdep", "256"]`                        |   1.408 ms (5%) |         |   80 bytes (1%) |           3 |
| `["gemm", "mul", "xf", "ivdep", "32"]`                         |   3.600 μs (5%) |         |   80 bytes (1%) |           3 |
| `["gemm", "mul", "xf", "ivdep", "8"]`                          | 400.000 ns (5%) |         |   80 bytes (1%) |           3 |
| `["gemm", "mul", "xf", "true", "256"]`                         |   1.382 ms (5%) |         |   80 bytes (1%) |           3 |
| `["gemm", "mul", "xf", "true", "32"]`                          |   5.500 μs (5%) |         |   80 bytes (1%) |           3 |
| `["gemm", "mul", "xf", "true", "8"]`                           | 400.000 ns (5%) |         |   80 bytes (1%) |           3 |
| `["groupby", "sum", "sac"]`                                    | 168.311 μs (5%) |         |  624 bytes (1%) |           5 |
| `["groupby", "sum", "xf-with-init"]`                           | 138.509 μs (5%) |         |   1.20 KiB (1%) |           9 |
| `["groupby", "sum", "xf-without-init"]`                        | 141.909 μs (5%) |         |   1.20 KiB (1%) |           9 |
| `["mapcat_eduction", "base"]`                                  |   1.590 μs (5%) |         |                 |             |
| `["mapcat_eduction", "xf-eduction"]`                           |   1.730 μs (5%) |         |                 |             |
| `["mapcat_eduction", "xf-xf"]`                                 |   1.390 μs (5%) |         |                 |             |
| `["missing_argmax", "man"]`                                    |   2.233 μs (5%) |         |   32 bytes (1%) |           1 |
| `["missing_argmax", "rf"]`                                     |   1.320 μs (5%) |         |   32 bytes (1%) |           1 |
| `["missing_argmax", "xf"]`                                     |   1.400 μs (5%) |         |   32 bytes (1%) |           1 |
| `["missing_dot", "equiv"]`                                     |   1.700 μs (5%) |         |   16 bytes (1%) |           1 |
| `["missing_dot", "man"]`                                       |   1.190 μs (5%) |         |   16 bytes (1%) |           1 |
| `["missing_dot", "naive"]`                                     |   4.758 μs (5%) |         |   16 bytes (1%) |           1 |
| `["missing_dot", "rf"]`                                        |   1.180 μs (5%) |         |   16 bytes (1%) |           1 |
| `["missing_dot", "rf_nota"]`                                   |   2.560 μs (5%) |         |   16 bytes (1%) |           1 |
| `["missing_dot", "xf"]`                                        |  89.406 μs (5%) |         |  72.22 KiB (1%) |        3746 |
| `["missing_dot", "xf_nota"]`                                   |  81.306 μs (5%) |         |  72.00 KiB (1%) |        3738 |
| `["overhead", "foldl"]`                                        |   3.900 ns (5%) |         |                 |             |
| `["overhead", "reduce_basecase"]`                              | 116.214 ns (5%) |         |   48 bytes (1%) |           2 |
| `["partition_by", "man"]`                                      |   1.936 ms (5%) |         |  352 bytes (1%) |           4 |
| `["partition_by", "xf"]`                                       |   2.333 ms (5%) |         |  544 bytes (1%) |           6 |
| `["set", "base"]`                                              |   4.636 ms (5%) |         |  49.56 KiB (1%) |          17 |
| `["set", "xf"]`                                                |   4.422 ms (5%) |         |  49.59 KiB (1%) |          19 |
| `["sum_transpose", "30", "noinit", "iter"]`                    |   2.190 μs (5%) |         |                 |             |
| `["sum_transpose", "30", "noinit", "man"]`                     |   2.122 μs (5%) |         |                 |             |
| `["sum_transpose", "30", "noinit", "xf"]`                      |   1.410 μs (5%) |         |   32 bytes (1%) |           2 |
| `["sum_transpose", "30", "withinit", "iter"]`                  |   1.480 μs (5%) |         |                 |             |
| `["sum_transpose", "30", "withinit", "man"]`                   | 956.565 ns (5%) |         |                 |             |
| `["sum_transpose", "30", "withinit", "xf"]`                    |   1.180 μs (5%) |         |   48 bytes (1%) |           3 |
| `["teerf_filter", "noinit"]`                                   |   2.145 μs (5%) |         |  176 bytes (1%) |           7 |
| `["teerf_filter", "withinit"]`                                 | 165.227 ns (5%) |         |                 |             |

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
Julia Version 1.5.4
Commit 69fcb5745b (2021-03-11 19:13 UTC)
Platform Info:
  OS: Linux (x86_64-pc-linux-gnu)
      Ubuntu 20.04.3 LTS
  uname: Linux 5.8.0-1041-azure #44~20.04.1-Ubuntu SMP Fri Aug 20 20:41:09 UTC 2021 x86_64 x86_64
  CPU: Intel(R) Xeon(R) Platinum 8171M CPU @ 2.60GHz: 
              speed         user         nice          sys         idle          irq
       #1  2095 MHz      37048 s         14 s       1714 s     101712 s          0 s
       #2  2095 MHz      76567 s          8 s       1916 s      62196 s          0 s
       
  Memory: 6.790924072265625 GB (3203.55859375 MB free)
  Uptime: 1413.0 sec
  Load Avg:  1.02978515625  1.04443359375  0.81494140625
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
    Model name:                      Intel(R) Xeon(R) Platinum 8171M CPU @ 2.60GHz
    Stepping:                        4
    CPU MHz:                         2095.193
    BogoMIPS:                        4190.38
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
| Brand              | Intel(R) Xeon(R) Platinum 8171M CPU @ 2.60GHz           |
| Vendor             | :Intel                                                  |
| Architecture       | :Skylake                                                |
| Model              | Family: 0x06, Model: 0x55, Stepping: 0x04, Type: 0x00   |
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

