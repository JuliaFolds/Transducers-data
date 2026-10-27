# Benchmark result

* Pull request commit: [`7c0ffadfc69ff5c00f84b10a2b36dc684f66da0a`](https://github.com/JuliaFolds/Transducers.jl/commit/7c0ffadfc69ff5c00f84b10a2b36dc684f66da0a)
* Pull request: <https://github.com/JuliaFolds/Transducers.jl/pull/243> (Update */Manifest.toml)

# Judge result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmarks:
    - Target: 27 Oct 2026 - 04:39
    - Baseline: 27 Oct 2026 - 04:43
* Package commits:
    - Target: a12285a
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
| `["append!!", "eduction"]`                                     |                1.07 (5%) :x: |                   1.00 (1%)  |
| `["append!!", "xf"]`                                           |                1.08 (5%) :x: |                   1.00 (1%)  |
| `["cartesian", "copyto!", "man"]`                              |                1.06 (5%) :x: |                   1.00 (1%)  |
| `["collect", "identity-union"]`                                |                1.07 (5%) :x: |                   1.00 (1%)  |
| `["filter_map_map!", "xf"]`                                    |                1.05 (5%) :x: |                   1.00 (1%)  |
| `["findall", "xf-array"]`                                      |                1.06 (5%) :x: |                   1.00 (1%)  |
| `["gemm", "fusedmul", "blas", "16"]`                           |                1.10 (5%) :x: |                   1.00 (1%)  |
| `["gemm", "fusedmul", "blas", "2"]`                            |                1.06 (5%) :x: |                   1.00 (1%)  |
| `["gemm", "fusedmul", "blas", "32"]`                           |                1.16 (5%) :x: |                   1.00 (1%)  |
| `["gemm", "fusedmul", "blas", "8"]`                            |                1.09 (5%) :x: |                   1.00 (1%)  |
| `["gemm", "mul", "linalg", "8"]`                               | 0.86 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["groupby", "sum", "sac"]`                                    | 0.01 (5%) :white_check_mark: | 0.12 (1%) :white_check_mark: |

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
      Ubuntu 24.04.5 LTS
  uname: Linux 6.17.0-1022-azure #22-Ubuntu SMP Mon Jul 27 17:24:03 UTC 2026 x86_64 x86_64
  CPU: AMD EPYC 9V45 96-Core Processor: 
              speed         user         nice          sys         idle          irq
       #1  4210 MHz        466 s          0 s         60 s       5715 s          0 s
       #2  4269 MHz        161 s          0 s         47 s       6040 s          0 s
       #3  4260 MHz       1599 s          0 s         59 s       4560 s          0 s
       #4  4266 MHz       3497 s          0 s        131 s       2608 s          0 s
       
  Memory: 15.614940643310547 GB (11339.80859375 MB free)
  Uptime: 631.27 sec
  Load Avg:  1.0  0.93  0.55
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-12.0.1 (ORCJIT, generic)
```

### Baseline
```
Julia Version 1.7.3
Commit 742b9abb4d (2022-05-06 12:58 UTC)
Platform Info:
  OS: Linux (x86_64-pc-linux-gnu)
      Ubuntu 24.04.5 LTS
  uname: Linux 6.17.0-1022-azure #22-Ubuntu SMP Mon Jul 27 17:24:03 UTC 2026 x86_64 x86_64
  CPU: AMD EPYC 9V45 96-Core Processor: 
              speed         user         nice          sys         idle          irq
       #1  4503 MHz        978 s          0 s         71 s       7495 s          0 s
       #2  4499 MHz        631 s          0 s         58 s       7862 s          0 s
       #3  4508 MHz       2688 s          0 s        106 s       5728 s          0 s
       #4  4785 MHz       3745 s          0 s        144 s       4651 s          0 s
       
  Memory: 15.614940643310547 GB (11162.68359375 MB free)
  Uptime: 861.82 sec
  Load Avg:  1.0  0.97  0.66
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-12.0.1 (ORCJIT, generic)
```

---
# Target result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmark: 27 Oct 2026 - 04:39
* Package commit: a12285a
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
| `["append!!", "eduction"]`                                     |   8.790 μs (5%) |         |  53.98 KiB (1%) |           8 |
| `["append!!", "xf"]`                                           |   8.713 μs (5%) |         |  53.98 KiB (1%) |           8 |
| `["cartesian", "copyto!", "iter"]`                             | 960.500 ns (5%) |         |                 |             |
| `["cartesian", "copyto!", "man"]`                              | 835.406 ns (5%) |         |                 |             |
| `["cartesian", "copyto!", "xf"]`                               | 838.150 ns (5%) |         |                 |             |
| `["cat", "base"]`                                              |   1.067 μs (5%) |         |                 |             |
| `["cat", "xf"]`                                                | 640.453 ns (5%) |         |                 |             |
| `["collect", "filter-missing"]`                                | 389.451 ns (5%) |         |   9.94 KiB (1%) |           1 |
| `["collect", "identity-float"]`                                |   2.458 μs (5%) |         |  78.17 KiB (1%) |           2 |
| `["collect", "identity-union"]`                                |  75.843 μs (5%) |         | 400.53 KiB (1%) |       10003 |
| `["dict", "base"]`                                             |   1.566 ms (5%) |         |  92.45 KiB (1%) |          22 |
| `["dict", "xf"]`                                               |   1.543 ms (5%) |         |  91.95 KiB (1%) |          18 |
| `["dot", "blas"]`                                              |   1.208 μs (5%) |         |                 |             |
| `["dot", "man"]`                                               | 703.474 ns (5%) |         |                 |             |
| `["dot", "rf"]`                                                | 663.161 ns (5%) |         |                 |             |
| `["dot", "xf"]`                                                | 665.300 ns (5%) |         |                 |             |
| `["filter_map_map!", "man"]`                                   |  12.108 μs (5%) |         |                 |             |
| `["filter_map_map!", "xf"]`                                    |  12.048 μs (5%) |         |                 |             |
| `["filter_map_reduce", "man"]`                                 | 161.550 μs (5%) |         |                 |             |
| `["filter_map_reduce", "xf"]`                                  | 160.869 μs (5%) |         |                 |             |
| `["filter_sum", "1000", "RandomFloats", "noinit", "base"]`     |   2.301 μs (5%) |         |                 |             |
| `["filter_sum", "1000", "RandomFloats", "noinit", "naive"]`    |   1.109 μs (5%) |         |                 |             |
| `["filter_sum", "1000", "RandomFloats", "noinit", "xf"]`       |   1.123 μs (5%) |         |                 |             |
| `["filter_sum", "1000", "RandomFloats", "withinit", "base"]`   |   1.137 μs (5%) |         |                 |             |
| `["filter_sum", "1000", "RandomFloats", "withinit", "naive"]`  | 278.500 ns (5%) |         |                 |             |
| `["filter_sum", "1000", "RandomFloats", "withinit", "xf"]`     |   1.131 μs (5%) |         |                 |             |
| `["filter_sum", "1000", "UnitRange", "noinit", "base"]`        | 535.772 ns (5%) |         |                 |             |
| `["filter_sum", "1000", "UnitRange", "noinit", "naive"]`       | 437.626 ns (5%) |         |                 |             |
| `["filter_sum", "1000", "UnitRange", "noinit", "xf"]`          |  52.982 ns (5%) |         |                 |             |
| `["filter_sum", "1000", "UnitRange", "withinit", "base"]`      |  40.090 ns (5%) |         |                 |             |
| `["filter_sum", "1000", "UnitRange", "withinit", "naive"]`     | 351.431 ns (5%) |         |                 |             |
| `["filter_sum", "1000", "UnitRange", "withinit", "xf"]`        |  40.798 ns (5%) |         |                 |             |
| `["filter_sum", "10000", "RandomFloats", "noinit", "base"]`    |  23.395 μs (5%) |         |                 |             |
| `["filter_sum", "10000", "RandomFloats", "noinit", "naive"]`   |  10.455 μs (5%) |         |                 |             |
| `["filter_sum", "10000", "RandomFloats", "noinit", "xf"]`      |  11.717 μs (5%) |         |                 |             |
| `["filter_sum", "10000", "RandomFloats", "withinit", "base"]`  |  11.547 μs (5%) |         |                 |             |
| `["filter_sum", "10000", "RandomFloats", "withinit", "naive"]` |   2.693 μs (5%) |         |                 |             |
| `["filter_sum", "10000", "RandomFloats", "withinit", "xf"]`    |  11.677 μs (5%) |         |                 |             |
| `["filter_sum", "10000", "UnitRange", "noinit", "base"]`       |   5.056 μs (5%) |         |                 |             |
| `["filter_sum", "10000", "UnitRange", "noinit", "naive"]`      |   4.246 μs (5%) |         |                 |             |
| `["filter_sum", "10000", "UnitRange", "noinit", "xf"]`         | 523.042 ns (5%) |         |                 |             |
| `["filter_sum", "10000", "UnitRange", "withinit", "base"]`     | 394.890 ns (5%) |         |                 |             |
| `["filter_sum", "10000", "UnitRange", "withinit", "naive"]`    |   3.470 μs (5%) |         |                 |             |
| `["filter_sum", "10000", "UnitRange", "withinit", "xf"]`       | 403.100 ns (5%) |         |                 |             |
| `["findall", "base"]`                                          |  62.523 μs (5%) |         | 797.20 KiB (1%) |           8 |
| `["findall", "xf-array"]`                                      | 612.971 μs (5%) |         |   2.94 MiB (1%) |       96426 |
| `["findall", "xf-iter"]`                                       | 312.525 μs (5%) |         |   1.83 MiB (1%) |          14 |
| `["gemm", "fusedmul", "blas", "16"]`                           |   2.933 ms (5%) |         |                 |             |
| `["gemm", "fusedmul", "blas", "2"]`                            | 840.643 μs (5%) |         |                 |             |
| `["gemm", "fusedmul", "blas", "32"]`                           |   5.773 ms (5%) |         |                 |             |
| `["gemm", "fusedmul", "blas", "8"]`                            |   1.728 ms (5%) |         |                 |             |
| `["gemm", "fusedmul", "xf", "16"]`                             |   1.106 ms (5%) |         |  192 bytes (1%) |           4 |
| `["gemm", "fusedmul", "xf", "2"]`                              | 135.311 μs (5%) |         |  192 bytes (1%) |           4 |
| `["gemm", "fusedmul", "xf", "32"]`                             |   2.211 ms (5%) |         |  192 bytes (1%) |           4 |
| `["gemm", "fusedmul", "xf", "8"]`                              | 547.946 μs (5%) |         |  192 bytes (1%) |           4 |
| `["gemm", "mul", "linalg", "256"]`                             |   1.178 ms (5%) |         |                 |             |
| `["gemm", "mul", "linalg", "32"]`                              |   2.890 μs (5%) |         |                 |             |
| `["gemm", "mul", "linalg", "8"]`                               | 128.778 ns (5%) |         |                 |             |
| `["gemm", "mul", "man", "false", "256"]`                       |   1.011 ms (5%) |         |                 |             |
| `["gemm", "mul", "man", "false", "32"]`                        |   3.220 μs (5%) |         |                 |             |
| `["gemm", "mul", "man", "false", "8"]`                         | 229.360 ns (5%) |         |                 |             |
| `["gemm", "mul", "man", "ivdep", "256"]`                       | 691.779 μs (5%) |         |                 |             |
| `["gemm", "mul", "man", "ivdep", "32"]`                        |   2.773 μs (5%) |         |                 |             |
| `["gemm", "mul", "man", "ivdep", "8"]`                         | 228.347 ns (5%) |         |                 |             |
| `["gemm", "mul", "man", "true", "256"]`                        | 963.625 μs (5%) |         |                 |             |
| `["gemm", "mul", "man", "true", "32"]`                         |   3.088 μs (5%) |         |                 |             |
| `["gemm", "mul", "man", "true", "8"]`                          | 230.249 ns (5%) |         |                 |             |
| `["gemm", "mul", "xf", "false", "256"]`                        |   1.019 ms (5%) |         |   80 bytes (1%) |           3 |
| `["gemm", "mul", "xf", "false", "32"]`                         |   3.304 μs (5%) |         |   80 bytes (1%) |           3 |
| `["gemm", "mul", "xf", "false", "8"]`                          | 260.419 ns (5%) |         |   80 bytes (1%) |           3 |
| `["gemm", "mul", "xf", "ivdep", "256"]`                        | 661.534 μs (5%) |         |   80 bytes (1%) |           3 |
| `["gemm", "mul", "xf", "ivdep", "32"]`                         |   2.752 μs (5%) |         |   80 bytes (1%) |           3 |
| `["gemm", "mul", "xf", "ivdep", "8"]`                          | 254.433 ns (5%) |         |   80 bytes (1%) |           3 |
| `["gemm", "mul", "xf", "true", "256"]`                         | 976.543 μs (5%) |         |   80 bytes (1%) |           3 |
| `["gemm", "mul", "xf", "true", "32"]`                          |   3.284 μs (5%) |         |   80 bytes (1%) |           3 |
| `["gemm", "mul", "xf", "true", "8"]`                           | 258.130 ns (5%) |         |   80 bytes (1%) |           3 |
| `["groupby", "sum", "sac"]`                                    |  53.019 μs (5%) |         |   1.64 KiB (1%) |          11 |
| `["groupby", "sum", "xf-with-init"]`                           |  58.818 μs (5%) |         |   1.05 KiB (1%) |           9 |
| `["groupby", "sum", "xf-without-init"]`                        |  57.286 μs (5%) |         |   1.05 KiB (1%) |           9 |
| `["mapcat_eduction", "base"]`                                  |  25.978 μs (5%) |         |                 |             |
| `["mapcat_eduction", "xf-eduction"]`                           | 644.577 ns (5%) |         |                 |             |
| `["mapcat_eduction", "xf-xf"]`                                 | 635.791 ns (5%) |         |                 |             |
| `["missing_argmax", "man"]`                                    |   3.246 μs (5%) |         |                 |             |
| `["missing_argmax", "rf"]`                                     | 633.373 ns (5%) |         |                 |             |
| `["missing_argmax", "xf"]`                                     | 647.174 ns (5%) |         |   32 bytes (1%) |           1 |
| `["missing_dot", "equiv"]`                                     | 926.800 ns (5%) |         |   48 bytes (1%) |           3 |
| `["missing_dot", "man"]`                                       | 453.185 ns (5%) |         |   48 bytes (1%) |           3 |
| `["missing_dot", "naive"]`                                     |   1.903 μs (5%) |         |   48 bytes (1%) |           3 |
| `["missing_dot", "rf"]`                                        | 457.158 ns (5%) |         |   48 bytes (1%) |           3 |
| `["missing_dot", "rf_nota"]`                                   | 923.317 ns (5%) |         |   48 bytes (1%) |           3 |
| `["missing_dot", "xf"]`                                        |  42.143 μs (5%) |         |  72.02 KiB (1%) |        3738 |
| `["missing_dot", "xf_nota"]`                                   |  42.173 μs (5%) |         |  72.12 KiB (1%) |        3740 |
| `["overhead", "foldl"]`                                        |   1.412 ns (5%) |         |                 |             |
| `["overhead", "reduce_basecase"]`                              |  43.095 ns (5%) |         |   16 bytes (1%) |           1 |
| `["partition_by", "man"]`                                      |   1.338 ms (5%) |         |  480 bytes (1%) |           3 |
| `["partition_by", "xf"]`                                       |   1.506 ms (5%) |         |  592 bytes (1%) |           5 |
| `["set", "base"]`                                              |   1.836 ms (5%) |         |  49.14 KiB (1%) |          17 |
| `["set", "xf"]`                                                |   1.802 ms (5%) |         |  49.17 KiB (1%) |          19 |
| `["sum_transpose", "30", "noinit", "iter"]`                    |   1.937 μs (5%) |         |                 |             |
| `["sum_transpose", "30", "noinit", "man"]`                     |   3.326 μs (5%) |         |                 |             |
| `["sum_transpose", "30", "noinit", "xf"]`                      | 391.421 ns (5%) |         |                 |             |
| `["sum_transpose", "30", "withinit", "iter"]`                  | 519.304 ns (5%) |         |                 |             |
| `["sum_transpose", "30", "withinit", "man"]`                   | 385.520 ns (5%) |         |                 |             |
| `["sum_transpose", "30", "withinit", "xf"]`                    | 383.644 ns (5%) |         |                 |             |
| `["teerf_filter", "noinit"]`                                   | 137.186 ns (5%) |         |   80 bytes (1%) |           3 |
| `["teerf_filter", "withinit"]`                                 |  71.195 ns (5%) |         |                 |             |

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
      Ubuntu 24.04.5 LTS
  uname: Linux 6.17.0-1022-azure #22-Ubuntu SMP Mon Jul 27 17:24:03 UTC 2026 x86_64 x86_64
  CPU: AMD EPYC 9V45 96-Core Processor: 
              speed         user         nice          sys         idle          irq
       #1  4210 MHz        466 s          0 s         60 s       5715 s          0 s
       #2  4269 MHz        161 s          0 s         47 s       6040 s          0 s
       #3  4260 MHz       1599 s          0 s         59 s       4560 s          0 s
       #4  4266 MHz       3497 s          0 s        131 s       2608 s          0 s
       
  Memory: 15.614940643310547 GB (11339.80859375 MB free)
  Uptime: 631.27 sec
  Load Avg:  1.0  0.93  0.55
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-12.0.1 (ORCJIT, generic)
```

---
# Baseline result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmark: 27 Oct 2026 - 04:43
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
| `["append!!", "eduction"]`                                     |   8.206 μs (5%) |         |  53.98 KiB (1%) |           8 |
| `["append!!", "xf"]`                                           |   8.062 μs (5%) |         |  53.98 KiB (1%) |           8 |
| `["cartesian", "copyto!", "iter"]`                             | 946.094 ns (5%) |         |                 |             |
| `["cartesian", "copyto!", "man"]`                              | 785.646 ns (5%) |         |                 |             |
| `["cartesian", "copyto!", "xf"]`                               | 803.761 ns (5%) |         |                 |             |
| `["cat", "base"]`                                              |   1.046 μs (5%) |         |                 |             |
| `["cat", "xf"]`                                                | 621.671 ns (5%) |         |                 |             |
| `["collect", "filter-missing"]`                                | 403.392 ns (5%) |         |   9.94 KiB (1%) |           1 |
| `["collect", "identity-float"]`                                |   2.417 μs (5%) |         |  78.17 KiB (1%) |           2 |
| `["collect", "identity-union"]`                                |  70.846 μs (5%) |         | 400.53 KiB (1%) |       10003 |
| `["dict", "base"]`                                             |   1.509 ms (5%) |         |  92.45 KiB (1%) |          22 |
| `["dict", "xf"]`                                               |   1.494 ms (5%) |         |  91.95 KiB (1%) |          18 |
| `["dot", "blas"]`                                              |   1.181 μs (5%) |         |                 |             |
| `["dot", "man"]`                                               | 731.728 ns (5%) |         |                 |             |
| `["dot", "rf"]`                                                | 653.522 ns (5%) |         |                 |             |
| `["dot", "xf"]`                                                | 666.181 ns (5%) |         |                 |             |
| `["filter_map_map!", "man"]`                                   |  11.567 μs (5%) |         |                 |             |
| `["filter_map_map!", "xf"]`                                    |  11.437 μs (5%) |         |                 |             |
| `["filter_map_reduce", "man"]`                                 | 157.023 μs (5%) |         |                 |             |
| `["filter_map_reduce", "xf"]`                                  | 155.852 μs (5%) |         |                 |             |
| `["filter_sum", "1000", "RandomFloats", "noinit", "base"]`     |   2.289 μs (5%) |         |                 |             |
| `["filter_sum", "1000", "RandomFloats", "noinit", "naive"]`    |   1.089 μs (5%) |         |                 |             |
| `["filter_sum", "1000", "RandomFloats", "noinit", "xf"]`       |   1.130 μs (5%) |         |                 |             |
| `["filter_sum", "1000", "RandomFloats", "withinit", "base"]`   |   1.119 μs (5%) |         |                 |             |
| `["filter_sum", "1000", "RandomFloats", "withinit", "naive"]`  | 276.233 ns (5%) |         |                 |             |
| `["filter_sum", "1000", "RandomFloats", "withinit", "xf"]`     |   1.112 μs (5%) |         |                 |             |
| `["filter_sum", "1000", "UnitRange", "noinit", "base"]`        | 526.021 ns (5%) |         |                 |             |
| `["filter_sum", "1000", "UnitRange", "noinit", "naive"]`       | 432.333 ns (5%) |         |                 |             |
| `["filter_sum", "1000", "UnitRange", "noinit", "xf"]`          |  52.392 ns (5%) |         |                 |             |
| `["filter_sum", "1000", "UnitRange", "withinit", "base"]`      |  39.433 ns (5%) |         |                 |             |
| `["filter_sum", "1000", "UnitRange", "withinit", "naive"]`     | 350.522 ns (5%) |         |                 |             |
| `["filter_sum", "1000", "UnitRange", "withinit", "xf"]`        |  41.254 ns (5%) |         |                 |             |
| `["filter_sum", "10000", "RandomFloats", "noinit", "base"]`    |  22.994 μs (5%) |         |                 |             |
| `["filter_sum", "10000", "RandomFloats", "noinit", "naive"]`   |  10.315 μs (5%) |         |                 |             |
| `["filter_sum", "10000", "RandomFloats", "noinit", "xf"]`      |  11.567 μs (5%) |         |                 |             |
| `["filter_sum", "10000", "RandomFloats", "withinit", "base"]`  |  11.767 μs (5%) |         |                 |             |
| `["filter_sum", "10000", "RandomFloats", "withinit", "naive"]` |   2.696 μs (5%) |         |                 |             |
| `["filter_sum", "10000", "RandomFloats", "withinit", "xf"]`    |  11.687 μs (5%) |         |                 |             |
| `["filter_sum", "10000", "UnitRange", "noinit", "base"]`       |   5.201 μs (5%) |         |                 |             |
| `["filter_sum", "10000", "UnitRange", "noinit", "naive"]`      |   4.243 μs (5%) |         |                 |             |
| `["filter_sum", "10000", "UnitRange", "noinit", "xf"]`         | 517.663 ns (5%) |         |                 |             |
| `["filter_sum", "10000", "UnitRange", "withinit", "base"]`     | 385.925 ns (5%) |         |                 |             |
| `["filter_sum", "10000", "UnitRange", "withinit", "naive"]`    |   3.414 μs (5%) |         |                 |             |
| `["filter_sum", "10000", "UnitRange", "withinit", "xf"]`       | 388.575 ns (5%) |         |                 |             |
| `["findall", "base"]`                                          |  59.599 μs (5%) |         | 797.20 KiB (1%) |           8 |
| `["findall", "xf-array"]`                                      | 580.674 μs (5%) |         |   2.94 MiB (1%) |       96426 |
| `["findall", "xf-iter"]`                                       | 304.112 μs (5%) |         |   1.83 MiB (1%) |          14 |
| `["gemm", "fusedmul", "blas", "16"]`                           |   2.661 ms (5%) |         |                 |             |
| `["gemm", "fusedmul", "blas", "2"]`                            | 794.131 μs (5%) |         |                 |             |
| `["gemm", "fusedmul", "blas", "32"]`                           |   4.982 ms (5%) |         |                 |             |
| `["gemm", "fusedmul", "blas", "8"]`                            |   1.588 ms (5%) |         |                 |             |
| `["gemm", "fusedmul", "xf", "16"]`                             |   1.141 ms (5%) |         |  192 bytes (1%) |           4 |
| `["gemm", "fusedmul", "xf", "2"]`                              | 136.503 μs (5%) |         |  192 bytes (1%) |           4 |
| `["gemm", "fusedmul", "xf", "32"]`                             |   2.265 ms (5%) |         |  192 bytes (1%) |           4 |
| `["gemm", "fusedmul", "xf", "8"]`                              | 534.095 μs (5%) |         |  192 bytes (1%) |           4 |
| `["gemm", "mul", "linalg", "256"]`                             |   1.149 ms (5%) |         |                 |             |
| `["gemm", "mul", "linalg", "32"]`                              |   2.884 μs (5%) |         |                 |             |
| `["gemm", "mul", "linalg", "8"]`                               | 150.000 ns (5%) |         |                 |             |
| `["gemm", "mul", "man", "false", "256"]`                       | 995.141 μs (5%) |         |                 |             |
| `["gemm", "mul", "man", "false", "32"]`                        |   3.284 μs (5%) |         |                 |             |
| `["gemm", "mul", "man", "false", "8"]`                         | 240.000 ns (5%) |         |                 |             |
| `["gemm", "mul", "man", "ivdep", "256"]`                       | 668.675 μs (5%) |         |                 |             |
| `["gemm", "mul", "man", "ivdep", "32"]`                        |   2.734 μs (5%) |         |                 |             |
| `["gemm", "mul", "man", "ivdep", "8"]`                         | 240.000 ns (5%) |         |                 |             |
| `["gemm", "mul", "man", "true", "256"]`                        | 920.960 μs (5%) |         |                 |             |
| `["gemm", "mul", "man", "true", "32"]`                         |   3.054 μs (5%) |         |                 |             |
| `["gemm", "mul", "man", "true", "8"]`                          | 240.000 ns (5%) |         |                 |             |
| `["gemm", "mul", "xf", "false", "256"]`                        | 977.465 μs (5%) |         |   80 bytes (1%) |           3 |
| `["gemm", "mul", "xf", "false", "32"]`                         |   3.245 μs (5%) |         |   80 bytes (1%) |           3 |
| `["gemm", "mul", "xf", "false", "8"]`                          | 260.000 ns (5%) |         |   80 bytes (1%) |           3 |
| `["gemm", "mul", "xf", "ivdep", "256"]`                        | 644.059 μs (5%) |         |   80 bytes (1%) |           3 |
| `["gemm", "mul", "xf", "ivdep", "32"]`                         |   2.784 μs (5%) |         |   80 bytes (1%) |           3 |
| `["gemm", "mul", "xf", "ivdep", "8"]`                          | 260.000 ns (5%) |         |   80 bytes (1%) |           3 |
| `["gemm", "mul", "xf", "true", "256"]`                         | 936.694 μs (5%) |         |   80 bytes (1%) |           3 |
| `["gemm", "mul", "xf", "true", "32"]`                          |   3.165 μs (5%) |         |   80 bytes (1%) |           3 |
| `["gemm", "mul", "xf", "true", "8"]`                           | 260.000 ns (5%) |         |   80 bytes (1%) |           3 |
| `["groupby", "sum", "sac"]`                                    |   3.689 ms (5%) |         |  13.19 KiB (1%) |         106 |
| `["groupby", "sum", "xf-with-init"]`                           |  57.966 μs (5%) |         |   1.05 KiB (1%) |           9 |
| `["groupby", "sum", "xf-without-init"]`                        |  57.525 μs (5%) |         |   1.05 KiB (1%) |           9 |
| `["mapcat_eduction", "base"]`                                  |  25.839 μs (5%) |         |                 |             |
| `["mapcat_eduction", "xf-eduction"]`                           | 615.945 ns (5%) |         |                 |             |
| `["mapcat_eduction", "xf-xf"]`                                 | 641.080 ns (5%) |         |                 |             |
| `["missing_argmax", "man"]`                                    |   3.101 μs (5%) |         |                 |             |
| `["missing_argmax", "rf"]`                                     | 631.000 ns (5%) |         |                 |             |
| `["missing_argmax", "xf"]`                                     | 632.745 ns (5%) |         |   32 bytes (1%) |           1 |
| `["missing_dot", "equiv"]`                                     | 890.771 ns (5%) |         |   48 bytes (1%) |           3 |
| `["missing_dot", "man"]`                                       | 454.621 ns (5%) |         |   48 bytes (1%) |           3 |
| `["missing_dot", "naive"]`                                     |   1.932 μs (5%) |         |   48 bytes (1%) |           3 |
| `["missing_dot", "rf"]`                                        | 465.541 ns (5%) |         |   48 bytes (1%) |           3 |
| `["missing_dot", "rf_nota"]`                                   | 910.878 ns (5%) |         |   48 bytes (1%) |           3 |
| `["missing_dot", "xf"]`                                        |  41.762 μs (5%) |         |  72.19 KiB (1%) |        3744 |
| `["missing_dot", "xf_nota"]`                                   |  40.180 μs (5%) |         |  72.28 KiB (1%) |        3748 |
| `["overhead", "foldl"]`                                        |   1.412 ns (5%) |         |                 |             |
| `["overhead", "reduce_basecase"]`                              |  42.680 ns (5%) |         |   16 bytes (1%) |           1 |
| `["partition_by", "man"]`                                      |   1.298 ms (5%) |         |  480 bytes (1%) |           3 |
| `["partition_by", "xf"]`                                       |   1.488 ms (5%) |         |  592 bytes (1%) |           5 |
| `["set", "base"]`                                              |   1.834 ms (5%) |         |  49.14 KiB (1%) |          17 |
| `["set", "xf"]`                                                |   1.857 ms (5%) |         |  49.17 KiB (1%) |          19 |
| `["sum_transpose", "30", "noinit", "iter"]`                    |   1.883 μs (5%) |         |                 |             |
| `["sum_transpose", "30", "noinit", "man"]`                     |   3.199 μs (5%) |         |                 |             |
| `["sum_transpose", "30", "noinit", "xf"]`                      | 381.257 ns (5%) |         |                 |             |
| `["sum_transpose", "30", "withinit", "iter"]`                  | 510.340 ns (5%) |         |                 |             |
| `["sum_transpose", "30", "withinit", "man"]`                   | 384.436 ns (5%) |         |                 |             |
| `["sum_transpose", "30", "withinit", "xf"]`                    | 380.911 ns (5%) |         |                 |             |
| `["teerf_filter", "noinit"]`                                   | 133.040 ns (5%) |         |   80 bytes (1%) |           3 |
| `["teerf_filter", "withinit"]`                                 |  69.878 ns (5%) |         |                 |             |

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
      Ubuntu 24.04.5 LTS
  uname: Linux 6.17.0-1022-azure #22-Ubuntu SMP Mon Jul 27 17:24:03 UTC 2026 x86_64 x86_64
  CPU: AMD EPYC 9V45 96-Core Processor: 
              speed         user         nice          sys         idle          irq
       #1  4503 MHz        978 s          0 s         71 s       7495 s          0 s
       #2  4499 MHz        631 s          0 s         58 s       7862 s          0 s
       #3  4508 MHz       2688 s          0 s        106 s       5728 s          0 s
       #4  4785 MHz       3745 s          0 s        144 s       4651 s          0 s
       
  Memory: 15.614940643310547 GB (11162.68359375 MB free)
  Uptime: 861.82 sec
  Load Avg:  1.0  0.97  0.66
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-12.0.1 (ORCJIT, generic)
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
    Model name:                              AMD EPYC 9V45 96-Core Processor
    CPU family:                              26
    Model:                                   2
    Thread(s) per core:                      2
    Core(s) per socket:                      2
    Socket(s):                               1
    Stepping:                                1
    BogoMIPS:                                5192.24
    Flags:                                   fpu vme de pse tsc msr pae mce cx8 apic sep mtrr pge mca cmov pat pse36 clflush mmx fxsr sse sse2 ht syscall nx mmxext fxsr_opt pdpe1gb rdtscp lm constant_tsc rep_good nopl xtopology tsc_reliable nonstop_tsc cpuid extd_apicid aperfmperf tsc_known_freq pni pclmulqdq ssse3 fma cx16 pcid sse4_1 sse4_2 x2apic movbe popcnt aes xsave avx f16c rdrand hypervisor lahf_lm cmp_legacy svm cr8_legacy abm sse4a misalignsse 3dnowprefetch osvw topoext vmmcall fsgsbase bmi1 avx2 smep bmi2 erms invpcid avx512f avx512dq rdseed adx smap avx512ifma clflushopt clwb avx512cd sha_ni avx512bw avx512vl xsaveopt xsavec xgetbv1 xsaves user_shstk avx_vnni avx512_bf16 clzero xsaveerptr rdpru arat npt nrip_save tsc_scale vmcb_clean flushbyasid decodeassists pausefilter pfthreshold v_vmsave_vmload avx512vbmi umip avx512_vbmi2 gfni vaes vpclmulqdq avx512_vnni avx512_bitalg avx512_vpopcntdq rdpid fsrm avx512_vp2intersect
    Virtualization:                          AMD-V
    Hypervisor vendor:                       Microsoft
    Virtualization type:                     full
    L1d cache:                               96 KiB (2 instances)
    L1i cache:                               64 KiB (2 instances)
    L2 cache:                                2 MiB (2 instances)
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
    Vulnerability Tsa:                       Not affected
    Vulnerability Tsx async abort:           Not affected
    Vulnerability Vmscape:                   Not affected
    

| Cpu Property       | Value                                                      |
|:------------------ |:---------------------------------------------------------- |
| Brand              | AMD EPYC 9V45 96-Core Processor                            |
| Vendor             | :AMD                                                       |
| Architecture       | :Unknown                                                   |
| Model              | Family: 0xbf, Model: 0x02, Stepping: 0x01, Type: 0x00      |
| Cores              | 8 physical cores, 16 logical cores (on executing CPU)      |
|                    | Hyperthreading hardware capability detected                |
| Clock Frequencies  | Not supported by CPU                                       |
| Data Cache         | Level 1:3 : (48, 1024, 32768) kbytes                       |
|                    | 64 byte cache line size                                    |
| Address Size       | 48 bits virtual, 48 bits physical                          |
| SIMD               | 512 bit = 64 byte max. SIMD vector size                    |
| Time Stamp Counter | TSC is accessible via `rdtsc`                              |
|                    | TSC runs at constant rate (invariant from clock frequency) |
| Perf. Monitoring   | Performance Monitoring Counters (PMC) are not supported    |
| Hypervisor         | Yes, Microsoft                                             |

