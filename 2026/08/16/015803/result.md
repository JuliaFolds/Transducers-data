# Benchmark result

* Pull request commit: [`3c81789a70d0ac5f830efb1485ffb6a9b73e0ffb`](https://github.com/JuliaFolds/Transducers.jl/commit/3c81789a70d0ac5f830efb1485ffb6a9b73e0ffb)
* Pull request: <https://github.com/JuliaFolds/Transducers.jl/pull/243> (Update */Manifest.toml)

# Judge result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmarks:
    - Target: 16 Aug 2026 - 01:51
    - Baseline: 16 Aug 2026 - 01:55
* Package commits:
    - Target: d24eb09
    - Baseline: 2a51f8d
* Julia commits:
    - Target: 742b9ab
    - Baseline: 742b9ab
* Julia command flags:
    - Target: None
    - Baseline: None
* Environment variables:
    - Target: `OMP_NUM_THREADS => 1` `JULIA_NUM_THREADS => 1`
    - Baseline: `OMP_NUM_THREADS => 1` `JULIA_NUM_THREADS => 1`

## Results
A ratio greater than `1.0` denotes a possible regression (marked with :x:), while a ratio less
than `1.0` denotes a possible improvement (marked with :white_check_mark:). Brackets display [tolerances](https://juliaci.github.io/BenchmarkTools.jl/stable/manual/#Benchmark-Parameters) for the benchmark estimates. Only significant results - results
that indicate possible regressions or improvements - are shown below (thus, an empty table means that all
benchmark results remained invariant between builds).

| ID                                                             | time ratio                   | memory ratio                 |
|----------------------------------------------------------------|------------------------------|------------------------------|
| `["cartesian", "copyto!", "iter"]`                             |                1.38 (5%) :x: |                   1.00 (1%)  |
| `["cartesian", "copyto!", "xf"]`                               |                1.55 (5%) :x: |                   1.00 (1%)  |
| `["collect", "filter-missing"]`                                | 0.92 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["collect", "identity-float"]`                                | 0.50 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["filter_map_map!", "man"]`                                   | 0.94 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["filter_sum", "1000", "RandomFloats", "withinit", "naive"]`  |                1.28 (5%) :x: |                   1.00 (1%)  |
| `["filter_sum", "1000", "UnitRange", "noinit", "base"]`        |                1.49 (5%) :x: |                   1.00 (1%)  |
| `["filter_sum", "10000", "UnitRange", "noinit", "base"]`       |                1.50 (5%) :x: |                   1.00 (1%)  |
| `["gemm", "fusedmul", "blas", "16"]`                           | 0.92 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["gemm", "fusedmul", "blas", "2"]`                            | 0.90 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["gemm", "fusedmul", "blas", "32"]`                           | 0.93 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["gemm", "fusedmul", "blas", "8"]`                            | 0.88 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["gemm", "fusedmul", "xf", "2"]`                              | 0.95 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["gemm", "fusedmul", "xf", "32"]`                             | 0.92 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["gemm", "mul", "linalg", "8"]`                               | 0.88 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["gemm", "mul", "man", "false", "8"]`                         | 0.93 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["gemm", "mul", "man", "ivdep", "8"]`                         | 0.90 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["gemm", "mul", "man", "true", "8"]`                          | 0.92 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["gemm", "mul", "xf", "false", "8"]`                          | 0.94 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["gemm", "mul", "xf", "ivdep", "8"]`                          |                1.18 (5%) :x: |                   1.00 (1%)  |
| `["groupby", "sum", "sac"]`                                    | 0.01 (5%) :white_check_mark: | 0.12 (1%) :white_check_mark: |
| `["groupby", "sum", "xf-with-init"]`                           | 0.95 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["missing_argmax", "xf"]`                                     |                1.07 (5%) :x: |                   1.00 (1%)  |
| `["missing_dot", "man"]`                                       | 0.83 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["missing_dot", "rf"]`                                        |                1.22 (5%) :x: |                   1.00 (1%)  |

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
Julia Version 1.7.3
Commit 742b9abb4d (2022-05-06 12:58 UTC)
Platform Info:
  OS: Linux (x86_64-pc-linux-gnu)
      Ubuntu 24.04.4 LTS
  uname: Linux 6.17.0-1022-azure #22-Ubuntu SMP Mon Jul 27 17:24:03 UTC 2026 x86_64 x86_64
  CPU: AMD EPYC 7763 64-Core Processor: 
              speed         user         nice          sys         idle          irq
       #1  3265 MHz        596 s          0 s         71 s       5739 s          0 s
       #2  3243 MHz        582 s          0 s        106 s       5670 s          0 s
       #3  3226 MHz       1494 s          0 s        106 s       4838 s          0 s
       #4  3240 MHz       3472 s          0 s        103 s       2854 s          0 s
       
  Memory: 15.614940643310547 GB (11373.328125 MB free)
  Uptime: 652.5 sec
  Load Avg:  1.0  0.94  0.58
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-12.0.1 (ORCJIT, znver3)
```

### Baseline
```
Julia Version 1.7.3
Commit 742b9abb4d (2022-05-06 12:58 UTC)
Platform Info:
  OS: Linux (x86_64-pc-linux-gnu)
      Ubuntu 24.04.4 LTS
  uname: Linux 6.17.0-1022-azure #22-Ubuntu SMP Mon Jul 27 17:24:03 UTC 2026 x86_64 x86_64
  CPU: AMD EPYC 7763 64-Core Processor: 
              speed         user         nice          sys         idle          irq
       #1  3240 MHz       1032 s          0 s         89 s       7708 s          0 s
       #2  3239 MHz        829 s          0 s        127 s       7825 s          0 s
       #3  3244 MHz       1920 s          0 s        148 s       6793 s          0 s
       #4  3240 MHz       4820 s          0 s        117 s       3918 s          0 s
       
  Memory: 15.614940643310547 GB (11253.41015625 MB free)
  Uptime: 895.34 sec
  Load Avg:  1.01  1.02  0.71
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-12.0.1 (ORCJIT, znver3)
```

---
# Target result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmark: 16 Aug 2026 - 01:51
* Package commit: d24eb09
* Julia commit: 742b9ab
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
| `["append!!", "eduction"]`                                     |  14.457 μs (5%) |         |  53.98 KiB (1%) |           8 |
| `["append!!", "xf"]`                                           |  14.468 μs (5%) |         |  53.98 KiB (1%) |           8 |
| `["cartesian", "copyto!", "iter"]`                             |   2.177 μs (5%) |         |                 |             |
| `["cartesian", "copyto!", "man"]`                              |   1.575 μs (5%) |         |                 |             |
| `["cartesian", "copyto!", "xf"]`                               |   2.487 μs (5%) |         |                 |             |
| `["cat", "base"]`                                              |   1.674 μs (5%) |         |                 |             |
| `["cat", "xf"]`                                                |   1.014 μs (5%) |         |                 |             |
| `["collect", "filter-missing"]`                                | 562.183 ns (5%) |         |   9.94 KiB (1%) |           1 |
| `["collect", "identity-float"]`                                |   2.217 μs (5%) |         |  78.17 KiB (1%) |           2 |
| `["collect", "identity-union"]`                                | 103.825 μs (5%) |         | 400.53 KiB (1%) |       10003 |
| `["dict", "base"]`                                             |   2.997 ms (5%) |         |  92.45 KiB (1%) |          22 |
| `["dict", "xf"]`                                               |   2.997 ms (5%) |         |  91.95 KiB (1%) |          18 |
| `["dot", "blas"]`                                              |   1.559 μs (5%) |         |                 |             |
| `["dot", "man"]`                                               |   1.553 μs (5%) |         |                 |             |
| `["dot", "rf"]`                                                |   1.572 μs (5%) |         |                 |             |
| `["dot", "xf"]`                                                |   1.573 μs (5%) |         |                 |             |
| `["filter_map_map!", "man"]`                                   |  46.537 μs (5%) |         |                 |             |
| `["filter_map_map!", "xf"]`                                    |  46.878 μs (5%) |         |                 |             |
| `["filter_map_reduce", "man"]`                                 | 154.299 μs (5%) |         |                 |             |
| `["filter_map_reduce", "xf"]`                                  | 154.309 μs (5%) |         |                 |             |
| `["filter_sum", "1000", "RandomFloats", "noinit", "base"]`     |   3.362 μs (5%) |         |                 |             |
| `["filter_sum", "1000", "RandomFloats", "noinit", "naive"]`    |   1.589 μs (5%) |         |                 |             |
| `["filter_sum", "1000", "RandomFloats", "noinit", "xf"]`       |   1.207 μs (5%) |         |                 |             |
| `["filter_sum", "1000", "RandomFloats", "withinit", "base"]`   |   1.213 μs (5%) |         |                 |             |
| `["filter_sum", "1000", "RandomFloats", "withinit", "naive"]`  | 790.963 ns (5%) |         |                 |             |
| `["filter_sum", "1000", "RandomFloats", "withinit", "xf"]`     |   1.209 μs (5%) |         |                 |             |
| `["filter_sum", "1000", "UnitRange", "noinit", "base"]`        | 934.483 ns (5%) |         |                 |             |
| `["filter_sum", "1000", "UnitRange", "noinit", "naive"]`       | 626.789 ns (5%) |         |                 |             |
| `["filter_sum", "1000", "UnitRange", "noinit", "xf"]`          | 166.042 ns (5%) |         |                 |             |
| `["filter_sum", "1000", "UnitRange", "withinit", "base"]`      | 114.774 ns (5%) |         |                 |             |
| `["filter_sum", "1000", "UnitRange", "withinit", "naive"]`     | 625.205 ns (5%) |         |                 |             |
| `["filter_sum", "1000", "UnitRange", "withinit", "xf"]`        | 113.949 ns (5%) |         |                 |             |
| `["filter_sum", "10000", "RandomFloats", "noinit", "base"]`    |  33.923 μs (5%) |         |                 |             |
| `["filter_sum", "10000", "RandomFloats", "noinit", "naive"]`   |  15.098 μs (5%) |         |                 |             |
| `["filter_sum", "10000", "RandomFloats", "noinit", "xf"]`      |  12.334 μs (5%) |         |                 |             |
| `["filter_sum", "10000", "RandomFloats", "withinit", "base"]`  |  12.333 μs (5%) |         |                 |             |
| `["filter_sum", "10000", "RandomFloats", "withinit", "naive"]` |   9.127 μs (5%) |         |                 |             |
| `["filter_sum", "10000", "RandomFloats", "withinit", "xf"]`    |  12.333 μs (5%) |         |                 |             |
| `["filter_sum", "10000", "UnitRange", "noinit", "base"]`       |   9.267 μs (5%) |         |                 |             |
| `["filter_sum", "10000", "UnitRange", "noinit", "naive"]`      |   6.179 μs (5%) |         |                 |             |
| `["filter_sum", "10000", "UnitRange", "noinit", "xf"]`         |   1.628 μs (5%) |         |                 |             |
| `["filter_sum", "10000", "UnitRange", "withinit", "base"]`     |   1.123 μs (5%) |         |                 |             |
| `["filter_sum", "10000", "UnitRange", "withinit", "naive"]`    |   6.177 μs (5%) |         |                 |             |
| `["filter_sum", "10000", "UnitRange", "withinit", "xf"]`       |   1.119 μs (5%) |         |                 |             |
| `["findall", "base"]`                                          | 108.915 μs (5%) |         | 797.20 KiB (1%) |           8 |
| `["findall", "xf-array"]`                                      |   1.002 ms (5%) |         |   2.94 MiB (1%) |       96426 |
| `["findall", "xf-iter"]`                                       | 692.098 μs (5%) |         |   1.83 MiB (1%) |          14 |
| `["gemm", "fusedmul", "blas", "16"]`                           |   2.459 ms (5%) |         |                 |             |
| `["gemm", "fusedmul", "blas", "2"]`                            |   1.671 ms (5%) |         |                 |             |
| `["gemm", "fusedmul", "blas", "32"]`                           |   3.987 ms (5%) |         |                 |             |
| `["gemm", "fusedmul", "blas", "8"]`                            |   1.746 ms (5%) |         |                 |             |
| `["gemm", "fusedmul", "xf", "16"]`                             |   2.422 ms (5%) |         |  192 bytes (1%) |           4 |
| `["gemm", "fusedmul", "xf", "2"]`                              | 294.522 μs (5%) |         |  192 bytes (1%) |           4 |
| `["gemm", "fusedmul", "xf", "32"]`                             |   4.862 ms (5%) |         |  192 bytes (1%) |           4 |
| `["gemm", "fusedmul", "xf", "8"]`                              |   1.203 ms (5%) |         |  192 bytes (1%) |           4 |
| `["gemm", "mul", "linalg", "256"]`                             | 775.815 μs (5%) |         |                 |             |
| `["gemm", "mul", "linalg", "32"]`                              |   2.820 μs (5%) |         |                 |             |
| `["gemm", "mul", "linalg", "8"]`                               | 167.042 ns (5%) |         |                 |             |
| `["gemm", "mul", "man", "false", "256"]`                       |   2.176 ms (5%) |         |                 |             |
| `["gemm", "mul", "man", "false", "32"]`                        |   5.153 μs (5%) |         |                 |             |
| `["gemm", "mul", "man", "false", "8"]`                         | 392.179 ns (5%) |         |                 |             |
| `["gemm", "mul", "man", "ivdep", "256"]`                       |   2.180 ms (5%) |         |                 |             |
| `["gemm", "mul", "man", "ivdep", "32"]`                        |   4.514 μs (5%) |         |                 |             |
| `["gemm", "mul", "man", "ivdep", "8"]`                         | 280.386 ns (5%) |         |                 |             |
| `["gemm", "mul", "man", "true", "256"]`                        |   2.176 ms (5%) |         |                 |             |
| `["gemm", "mul", "man", "true", "32"]`                         |   4.936 μs (5%) |         |                 |             |
| `["gemm", "mul", "man", "true", "8"]`                          | 293.921 ns (5%) |         |                 |             |
| `["gemm", "mul", "xf", "false", "256"]`                        |   2.179 ms (5%) |         |   80 bytes (1%) |           3 |
| `["gemm", "mul", "xf", "false", "32"]`                         |   5.545 μs (5%) |         |   80 bytes (1%) |           3 |
| `["gemm", "mul", "xf", "false", "8"]`                          | 350.280 ns (5%) |         |   80 bytes (1%) |           3 |
| `["gemm", "mul", "xf", "ivdep", "256"]`                        |   2.175 ms (5%) |         |   80 bytes (1%) |           3 |
| `["gemm", "mul", "xf", "ivdep", "32"]`                         |   4.539 μs (5%) |         |   80 bytes (1%) |           3 |
| `["gemm", "mul", "xf", "ivdep", "8"]`                          | 411.720 ns (5%) |         |   80 bytes (1%) |           3 |
| `["gemm", "mul", "xf", "true", "256"]`                         |   2.175 ms (5%) |         |   80 bytes (1%) |           3 |
| `["gemm", "mul", "xf", "true", "32"]`                          |   4.810 μs (5%) |         |   80 bytes (1%) |           3 |
| `["gemm", "mul", "xf", "true", "8"]`                           | 435.111 ns (5%) |         |   80 bytes (1%) |           3 |
| `["groupby", "sum", "sac"]`                                    |  94.317 μs (5%) |         |   1.64 KiB (1%) |          11 |
| `["groupby", "sum", "xf-with-init"]`                           |  97.142 μs (5%) |         |   1.05 KiB (1%) |           9 |
| `["groupby", "sum", "xf-without-init"]`                        |  99.667 μs (5%) |         |   1.05 KiB (1%) |           9 |
| `["mapcat_eduction", "base"]`                                  |  31.209 μs (5%) |         |                 |             |
| `["mapcat_eduction", "xf-eduction"]`                           |   1.015 μs (5%) |         |                 |             |
| `["mapcat_eduction", "xf-xf"]`                                 |   1.015 μs (5%) |         |                 |             |
| `["missing_argmax", "man"]`                                    |   1.098 μs (5%) |         |                 |             |
| `["missing_argmax", "rf"]`                                     | 769.465 ns (5%) |         |                 |             |
| `["missing_argmax", "xf"]`                                     | 799.417 ns (5%) |         |   32 bytes (1%) |           1 |
| `["missing_dot", "equiv"]`                                     |   1.812 μs (5%) |         |   48 bytes (1%) |           3 |
| `["missing_dot", "man"]`                                       | 850.426 ns (5%) |         |   48 bytes (1%) |           3 |
| `["missing_dot", "naive"]`                                     |   2.772 μs (5%) |         |   48 bytes (1%) |           3 |
| `["missing_dot", "rf"]`                                        |   1.159 μs (5%) |         |   48 bytes (1%) |           3 |
| `["missing_dot", "rf_nota"]`                                   |   1.899 μs (5%) |         |   48 bytes (1%) |           3 |
| `["missing_dot", "xf"]`                                        |  67.967 μs (5%) |         |  72.33 KiB (1%) |        3750 |
| `["missing_dot", "xf_nota"]`                                   |  67.677 μs (5%) |         |  72.16 KiB (1%) |        3740 |
| `["overhead", "foldl"]`                                        |   2.785 ns (5%) |         |                 |             |
| `["overhead", "reduce_basecase"]`                              |  75.842 ns (5%) |         |   16 bytes (1%) |           1 |
| `["partition_by", "man"]`                                      |   1.891 ms (5%) |         |  480 bytes (1%) |           3 |
| `["partition_by", "xf"]`                                       |   2.258 ms (5%) |         |  592 bytes (1%) |           5 |
| `["set", "base"]`                                              |   2.687 ms (5%) |         |  49.14 KiB (1%) |          17 |
| `["set", "xf"]`                                                |   2.683 ms (5%) |         |  49.17 KiB (1%) |          19 |
| `["sum_transpose", "30", "noinit", "iter"]`                    |   2.748 μs (5%) |         |                 |             |
| `["sum_transpose", "30", "noinit", "man"]`                     |   3.145 μs (5%) |         |                 |             |
| `["sum_transpose", "30", "noinit", "xf"]`                      | 806.622 ns (5%) |         |                 |             |
| `["sum_transpose", "30", "withinit", "iter"]`                  |   1.018 μs (5%) |         |                 |             |
| `["sum_transpose", "30", "withinit", "man"]`                   | 805.132 ns (5%) |         |                 |             |
| `["sum_transpose", "30", "withinit", "xf"]`                    | 805.681 ns (5%) |         |                 |             |
| `["teerf_filter", "noinit"]`                                   | 289.841 ns (5%) |         |   80 bytes (1%) |           3 |
| `["teerf_filter", "withinit"]`                                 | 173.924 ns (5%) |         |                 |             |

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
Julia Version 1.7.3
Commit 742b9abb4d (2022-05-06 12:58 UTC)
Platform Info:
  OS: Linux (x86_64-pc-linux-gnu)
      Ubuntu 24.04.4 LTS
  uname: Linux 6.17.0-1022-azure #22-Ubuntu SMP Mon Jul 27 17:24:03 UTC 2026 x86_64 x86_64
  CPU: AMD EPYC 7763 64-Core Processor: 
              speed         user         nice          sys         idle          irq
       #1  3265 MHz        596 s          0 s         71 s       5739 s          0 s
       #2  3243 MHz        582 s          0 s        106 s       5670 s          0 s
       #3  3226 MHz       1494 s          0 s        106 s       4838 s          0 s
       #4  3240 MHz       3472 s          0 s        103 s       2854 s          0 s
       
  Memory: 15.614940643310547 GB (11373.328125 MB free)
  Uptime: 652.5 sec
  Load Avg:  1.0  0.94  0.58
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-12.0.1 (ORCJIT, znver3)
```

---
# Baseline result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmark: 16 Aug 2026 - 01:55
* Package commit: 2a51f8d
* Julia commit: 742b9ab
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
| `["append!!", "eduction"]`                                     |  14.337 μs (5%) |         |  53.98 KiB (1%) |           8 |
| `["append!!", "xf"]`                                           |  14.347 μs (5%) |         |  53.98 KiB (1%) |           8 |
| `["cartesian", "copyto!", "iter"]`                             |   1.577 μs (5%) |         |                 |             |
| `["cartesian", "copyto!", "man"]`                              |   1.573 μs (5%) |         |                 |             |
| `["cartesian", "copyto!", "xf"]`                               |   1.602 μs (5%) |         |                 |             |
| `["cat", "base"]`                                              |   1.655 μs (5%) |         |                 |             |
| `["cat", "xf"]`                                                |   1.014 μs (5%) |         |                 |             |
| `["collect", "filter-missing"]`                                | 612.556 ns (5%) |         |   9.94 KiB (1%) |           1 |
| `["collect", "identity-float"]`                                |   4.447 μs (5%) |         |  78.17 KiB (1%) |           2 |
| `["collect", "identity-union"]`                                | 107.733 μs (5%) |         | 400.53 KiB (1%) |       10003 |
| `["dict", "base"]`                                             |   2.997 ms (5%) |         |  92.45 KiB (1%) |          22 |
| `["dict", "xf"]`                                               |   2.997 ms (5%) |         |  91.95 KiB (1%) |          18 |
| `["dot", "blas"]`                                              |   1.559 μs (5%) |         |                 |             |
| `["dot", "man"]`                                               |   1.553 μs (5%) |         |                 |             |
| `["dot", "rf"]`                                                |   1.572 μs (5%) |         |                 |             |
| `["dot", "xf"]`                                                |   1.577 μs (5%) |         |                 |             |
| `["filter_map_map!", "man"]`                                   |  49.523 μs (5%) |         |                 |             |
| `["filter_map_map!", "xf"]`                                    |  48.421 μs (5%) |         |                 |             |
| `["filter_map_reduce", "man"]`                                 | 154.309 μs (5%) |         |                 |             |
| `["filter_map_reduce", "xf"]`                                  | 154.299 μs (5%) |         |                 |             |
| `["filter_sum", "1000", "RandomFloats", "noinit", "base"]`     |   3.360 μs (5%) |         |                 |             |
| `["filter_sum", "1000", "RandomFloats", "noinit", "naive"]`    |   1.587 μs (5%) |         |                 |             |
| `["filter_sum", "1000", "RandomFloats", "noinit", "xf"]`       |   1.207 μs (5%) |         |                 |             |
| `["filter_sum", "1000", "RandomFloats", "withinit", "base"]`   |   1.209 μs (5%) |         |                 |             |
| `["filter_sum", "1000", "RandomFloats", "withinit", "naive"]`  | 617.873 ns (5%) |         |                 |             |
| `["filter_sum", "1000", "RandomFloats", "withinit", "xf"]`     |   1.213 μs (5%) |         |                 |             |
| `["filter_sum", "1000", "UnitRange", "noinit", "base"]`        | 626.345 ns (5%) |         |                 |             |
| `["filter_sum", "1000", "UnitRange", "noinit", "naive"]`       | 626.485 ns (5%) |         |                 |             |
| `["filter_sum", "1000", "UnitRange", "noinit", "xf"]`          | 165.686 ns (5%) |         |                 |             |
| `["filter_sum", "1000", "UnitRange", "withinit", "base"]`      | 113.781 ns (5%) |         |                 |             |
| `["filter_sum", "1000", "UnitRange", "withinit", "naive"]`     | 625.205 ns (5%) |         |                 |             |
| `["filter_sum", "1000", "UnitRange", "withinit", "xf"]`        | 114.307 ns (5%) |         |                 |             |
| `["filter_sum", "10000", "RandomFloats", "noinit", "base"]`    |  33.923 μs (5%) |         |                 |             |
| `["filter_sum", "10000", "RandomFloats", "noinit", "naive"]`   |  15.098 μs (5%) |         |                 |             |
| `["filter_sum", "10000", "RandomFloats", "noinit", "xf"]`      |  12.333 μs (5%) |         |                 |             |
| `["filter_sum", "10000", "RandomFloats", "withinit", "base"]`  |  12.333 μs (5%) |         |                 |             |
| `["filter_sum", "10000", "RandomFloats", "withinit", "naive"]` |   8.827 μs (5%) |         |                 |             |
| `["filter_sum", "10000", "RandomFloats", "withinit", "xf"]`    |  12.333 μs (5%) |         |                 |             |
| `["filter_sum", "10000", "UnitRange", "noinit", "base"]`       |   6.191 μs (5%) |         |                 |             |
| `["filter_sum", "10000", "UnitRange", "noinit", "naive"]`      |   6.179 μs (5%) |         |                 |             |
| `["filter_sum", "10000", "UnitRange", "noinit", "xf"]`         |   1.638 μs (5%) |         |                 |             |
| `["filter_sum", "10000", "UnitRange", "withinit", "base"]`     |   1.122 μs (5%) |         |                 |             |
| `["filter_sum", "10000", "UnitRange", "withinit", "naive"]`    |   6.177 μs (5%) |         |                 |             |
| `["filter_sum", "10000", "UnitRange", "withinit", "xf"]`       |   1.123 μs (5%) |         |                 |             |
| `["findall", "base"]`                                          | 110.046 μs (5%) |         | 797.20 KiB (1%) |           8 |
| `["findall", "xf-array"]`                                      |   1.002 ms (5%) |         |   2.94 MiB (1%) |       96426 |
| `["findall", "xf-iter"]`                                       | 698.990 μs (5%) |         |   1.83 MiB (1%) |          14 |
| `["gemm", "fusedmul", "blas", "16"]`                           |   2.679 ms (5%) |         |                 |             |
| `["gemm", "fusedmul", "blas", "2"]`                            |   1.852 ms (5%) |         |                 |             |
| `["gemm", "fusedmul", "blas", "32"]`                           |   4.266 ms (5%) |         |                 |             |
| `["gemm", "fusedmul", "blas", "8"]`                            |   1.975 ms (5%) |         |                 |             |
| `["gemm", "fusedmul", "xf", "16"]`                             |   2.501 ms (5%) |         |  192 bytes (1%) |           4 |
| `["gemm", "fusedmul", "xf", "2"]`                              | 310.302 μs (5%) |         |  192 bytes (1%) |           4 |
| `["gemm", "fusedmul", "xf", "32"]`                             |   5.275 ms (5%) |         |  192 bytes (1%) |           4 |
| `["gemm", "fusedmul", "xf", "8"]`                              |   1.250 ms (5%) |         |  192 bytes (1%) |           4 |
| `["gemm", "mul", "linalg", "256"]`                             | 778.149 μs (5%) |         |                 |             |
| `["gemm", "mul", "linalg", "32"]`                              |   2.835 μs (5%) |         |                 |             |
| `["gemm", "mul", "linalg", "8"]`                               | 190.000 ns (5%) |         |                 |             |
| `["gemm", "mul", "man", "false", "256"]`                       |   2.273 ms (5%) |         |                 |             |
| `["gemm", "mul", "man", "false", "32"]`                        |   5.410 μs (5%) |         |                 |             |
| `["gemm", "mul", "man", "false", "8"]`                         | 420.000 ns (5%) |         |                 |             |
| `["gemm", "mul", "man", "ivdep", "256"]`                       |   2.231 ms (5%) |         |                 |             |
| `["gemm", "mul", "man", "ivdep", "32"]`                        |   4.558 μs (5%) |         |                 |             |
| `["gemm", "mul", "man", "ivdep", "8"]`                         | 310.000 ns (5%) |         |                 |             |
| `["gemm", "mul", "man", "true", "256"]`                        |   2.231 ms (5%) |         |                 |             |
| `["gemm", "mul", "man", "true", "32"]`                         |   5.009 μs (5%) |         |                 |             |
| `["gemm", "mul", "man", "true", "8"]`                          | 320.000 ns (5%) |         |                 |             |
| `["gemm", "mul", "xf", "false", "256"]`                        |   2.231 ms (5%) |         |   80 bytes (1%) |           3 |
| `["gemm", "mul", "xf", "false", "32"]`                         |   5.601 μs (5%) |         |   80 bytes (1%) |           3 |
| `["gemm", "mul", "xf", "false", "8"]`                          | 371.000 ns (5%) |         |   80 bytes (1%) |           3 |
| `["gemm", "mul", "xf", "ivdep", "256"]`                        |   2.233 ms (5%) |         |   80 bytes (1%) |           3 |
| `["gemm", "mul", "xf", "ivdep", "32"]`                         |   4.558 μs (5%) |         |   80 bytes (1%) |           3 |
| `["gemm", "mul", "xf", "ivdep", "8"]`                          | 350.000 ns (5%) |         |   80 bytes (1%) |           3 |
| `["gemm", "mul", "xf", "true", "256"]`                         |   2.234 ms (5%) |         |   80 bytes (1%) |           3 |
| `["gemm", "mul", "xf", "true", "32"]`                          |   4.999 μs (5%) |         |   80 bytes (1%) |           3 |
| `["gemm", "mul", "xf", "true", "8"]`                           | 451.000 ns (5%) |         |   80 bytes (1%) |           3 |
| `["groupby", "sum", "sac"]`                                    |   6.727 ms (5%) |         |  13.19 KiB (1%) |         106 |
| `["groupby", "sum", "xf-with-init"]`                           | 102.512 μs (5%) |         |   1.05 KiB (1%) |           9 |
| `["groupby", "sum", "xf-without-init"]`                        |  96.922 μs (5%) |         |   1.05 KiB (1%) |           9 |
| `["mapcat_eduction", "base"]`                                  |  31.719 μs (5%) |         |                 |             |
| `["mapcat_eduction", "xf-eduction"]`                           |   1.015 μs (5%) |         |                 |             |
| `["mapcat_eduction", "xf-xf"]`                                 |   1.016 μs (5%) |         |                 |             |
| `["missing_argmax", "man"]`                                    |   1.097 μs (5%) |         |                 |             |
| `["missing_argmax", "rf"]`                                     | 741.891 ns (5%) |         |                 |             |
| `["missing_argmax", "xf"]`                                     | 750.573 ns (5%) |         |   32 bytes (1%) |           1 |
| `["missing_dot", "equiv"]`                                     |   1.865 μs (5%) |         |   48 bytes (1%) |           3 |
| `["missing_dot", "man"]`                                       |   1.030 μs (5%) |         |   48 bytes (1%) |           3 |
| `["missing_dot", "naive"]`                                     |   2.771 μs (5%) |         |   48 bytes (1%) |           3 |
| `["missing_dot", "rf"]`                                        | 950.800 ns (5%) |         |   48 bytes (1%) |           3 |
| `["missing_dot", "rf_nota"]`                                   |   1.808 μs (5%) |         |   48 bytes (1%) |           3 |
| `["missing_dot", "xf"]`                                        |  68.809 μs (5%) |         |  72.23 KiB (1%) |        3746 |
| `["missing_dot", "xf_nota"]`                                   |  68.038 μs (5%) |         |  72.14 KiB (1%) |        3744 |
| `["overhead", "foldl"]`                                        |   2.785 ns (5%) |         |                 |             |
| `["overhead", "reduce_basecase"]`                              |  77.450 ns (5%) |         |   16 bytes (1%) |           1 |
| `["partition_by", "man"]`                                      |   1.886 ms (5%) |         |  480 bytes (1%) |           3 |
| `["partition_by", "xf"]`                                       |   2.208 ms (5%) |         |  592 bytes (1%) |           5 |
| `["set", "base"]`                                              |   2.818 ms (5%) |         |  49.14 KiB (1%) |          17 |
| `["set", "xf"]`                                                |   2.704 ms (5%) |         |  49.17 KiB (1%) |          19 |
| `["sum_transpose", "30", "noinit", "iter"]`                    |   2.750 μs (5%) |         |                 |             |
| `["sum_transpose", "30", "noinit", "man"]`                     |   3.118 μs (5%) |         |                 |             |
| `["sum_transpose", "30", "noinit", "xf"]`                      | 805.722 ns (5%) |         |                 |             |
| `["sum_transpose", "30", "withinit", "iter"]`                  | 991.800 ns (5%) |         |                 |             |
| `["sum_transpose", "30", "withinit", "man"]`                   | 805.132 ns (5%) |         |                 |             |
| `["sum_transpose", "30", "withinit", "xf"]`                    | 805.681 ns (5%) |         |                 |             |
| `["teerf_filter", "noinit"]`                                   | 290.731 ns (5%) |         |   80 bytes (1%) |           3 |
| `["teerf_filter", "withinit"]`                                 | 172.302 ns (5%) |         |                 |             |

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
Julia Version 1.7.3
Commit 742b9abb4d (2022-05-06 12:58 UTC)
Platform Info:
  OS: Linux (x86_64-pc-linux-gnu)
      Ubuntu 24.04.4 LTS
  uname: Linux 6.17.0-1022-azure #22-Ubuntu SMP Mon Jul 27 17:24:03 UTC 2026 x86_64 x86_64
  CPU: AMD EPYC 7763 64-Core Processor: 
              speed         user         nice          sys         idle          irq
       #1  3240 MHz       1032 s          0 s         89 s       7708 s          0 s
       #2  3239 MHz        829 s          0 s        127 s       7825 s          0 s
       #3  3244 MHz       1920 s          0 s        148 s       6793 s          0 s
       #4  3240 MHz       4820 s          0 s        117 s       3918 s          0 s
       
  Memory: 15.614940643310547 GB (11253.41015625 MB free)
  Uptime: 895.34 sec
  Load Avg:  1.01  1.02  0.71
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-12.0.1 (ORCJIT, znver3)
```

---
# Runtime information
| Runtime Info | |
|:--|:--|
| BLAS #threads | 4 |
| `BLAS.vendor()` | `openblas64` |
| `Sys.CPU_THREADS` | 4 |

`lscpu` output:

    Architecture:                            x86_64
    CPU op-mode(s):                          32-bit, 64-bit
    Address sizes:                           48 bits physical, 48 bits virtual
    Byte Order:                              Little Endian
    CPU(s):                                  4
    On-line CPU(s) list:                     0-3
    Vendor ID:                               AuthenticAMD
    Model name:                              AMD EPYC 7763 64-Core Processor
    CPU family:                              25
    Model:                                   1
    Thread(s) per core:                      2
    Core(s) per socket:                      2
    Socket(s):                               1
    Stepping:                                1
    BogoMIPS:                                4890.86
    Flags:                                   fpu vme de pse tsc msr pae mce cx8 apic sep mtrr pge mca cmov pat pse36 clflush mmx fxsr sse sse2 ht syscall nx mmxext fxsr_opt pdpe1gb rdtscp lm constant_tsc rep_good nopl tsc_reliable nonstop_tsc cpuid extd_apicid aperfmperf tsc_known_freq pni pclmulqdq ssse3 fma cx16 pcid sse4_1 sse4_2 movbe popcnt aes xsave avx f16c rdrand hypervisor lahf_lm cmp_legacy svm cr8_legacy abm sse4a misalignsse 3dnowprefetch osvw topoext vmmcall fsgsbase bmi1 avx2 smep bmi2 erms invpcid rdseed adx smap clflushopt clwb sha_ni xsaveopt xsavec xgetbv1 xsaves user_shstk clzero xsaveerptr rdpru arat npt nrip_save tsc_scale vmcb_clean flushbyasid decodeassists pausefilter pfthreshold v_vmsave_vmload umip vaes vpclmulqdq rdpid fsrm
    Virtualization:                          AMD-V
    Hypervisor vendor:                       Microsoft
    Virtualization type:                     full
    L1d cache:                               64 KiB (2 instances)
    L1i cache:                               64 KiB (2 instances)
    L2 cache:                                1 MiB (2 instances)
    L3 cache:                                32 MiB (1 instance)
    NUMA node(s):                            1
    NUMA node0 CPU(s):                       0-3
    Vulnerability Gather data sampling:      Not affected
    Vulnerability Ghostwrite:                Not affected
    Vulnerability Indirect target selection: Not affected
    Vulnerability Itlb multihit:             Not affected
    Vulnerability L1tf:                      Not affected
    Vulnerability Mds:                       Not affected
    Vulnerability Meltdown:                  Not affected
    Vulnerability Mmio stale data:           Not affected
    Vulnerability Old microcode:             Not affected
    Vulnerability Reg file data sampling:    Not affected
    Vulnerability Retbleed:                  Not affected
    Vulnerability Spec rstack overflow:      Vulnerable: Safe RET, no microcode
    Vulnerability Spec store bypass:         Vulnerable
    Vulnerability Spectre v1:                Mitigation; usercopy/swapgs barriers and __user pointer sanitization
    Vulnerability Spectre v2:                Mitigation; Retpolines; STIBP disabled; RSB filling; PBRSB-eIBRS Not affected; BHI Not affected
    Vulnerability Srbds:                     Not affected
    Vulnerability Tsa:                       Vulnerable: No microcode
    Vulnerability Tsx async abort:           Not affected
    Vulnerability Vmscape:                   Not affected
    

| Cpu Property       | Value                                                      |
|:------------------ |:---------------------------------------------------------- |
| Brand              | AMD EPYC 7763 64-Core Processor                            |
| Vendor             | :AMD                                                       |
| Architecture       | :Unknown                                                   |
| Model              | Family: 0xaf, Model: 0x01, Stepping: 0x01, Type: 0x00      |
| Cores              | 16 physical cores, 16 logical cores (on executing CPU)     |
|                    | No Hyperthreading hardware capability detected             |
| Clock Frequencies  | Not supported by CPU                                       |
| Data Cache         | Level 1:3 : (32, 512, 32768) kbytes                        |
|                    | 64 byte cache line size                                    |
| Address Size       | 48 bits virtual, 48 bits physical                          |
| SIMD               | 256 bit = 32 byte max. SIMD vector size                    |
| Time Stamp Counter | TSC is accessible via `rdtsc`                              |
|                    | TSC runs at constant rate (invariant from clock frequency) |
| Perf. Monitoring   | Performance Monitoring Counters (PMC) are not supported    |
| Hypervisor         | Yes, Microsoft                                             |

