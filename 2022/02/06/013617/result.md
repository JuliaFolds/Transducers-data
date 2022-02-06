# Benchmark result

* Pull request commit: [`ce2a412a772d574eb1583abaf6be0498214b85e2`](https://github.com/JuliaFolds/Transducers.jl/commit/ce2a412a772d574eb1583abaf6be0498214b85e2)
* Pull request: <https://github.com/JuliaFolds/Transducers.jl/pull/243> (Update */Manifest.toml)

# Judge result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmarks:
    - Target: 6 Feb 2022 - 01:29
    - Baseline: 6 Feb 2022 - 01:35
* Package commits:
    - Target: 4cf859
    - Baseline: 39038b
* Julia commits:
    - Target: ac5cc9
    - Baseline: ac5cc9
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

| ID                                                             | time ratio                   | memory ratio                 |
|----------------------------------------------------------------|------------------------------|------------------------------|
| `["append!!", "eduction"]`                                     |                1.07 (5%) :x: |                   1.00 (1%)  |
| `["append!!", "xf"]`                                           |                1.09 (5%) :x: |                   1.00 (1%)  |
| `["cartesian", "copyto!", "iter"]`                             |                1.26 (5%) :x: |                   1.00 (1%)  |
| `["cartesian", "copyto!", "xf"]`                               |                1.26 (5%) :x: |                   1.00 (1%)  |
| `["cat", "base"]`                                              |                1.07 (5%) :x: |                   1.00 (1%)  |
| `["cat", "xf"]`                                                |                1.09 (5%) :x: |                   1.00 (1%)  |
| `["collect", "filter-missing"]`                                |                1.11 (5%) :x: |                   1.00 (1%)  |
| `["collect", "identity-float"]`                                |                1.13 (5%) :x: |                   1.00 (1%)  |
| `["collect", "identity-union"]`                                |                1.13 (5%) :x: |                   1.00 (1%)  |
| `["dot", "man"]`                                               |                1.08 (5%) :x: |                   1.00 (1%)  |
| `["dot", "rf"]`                                                |                1.07 (5%) :x: |                   1.00 (1%)  |
| `["dot", "xf"]`                                                |                1.07 (5%) :x: |                   1.00 (1%)  |
| `["filter_map_reduce", "man"]`                                 |                1.09 (5%) :x: |                   1.00 (1%)  |
| `["filter_map_reduce", "xf"]`                                  |                1.06 (5%) :x: |                   1.00 (1%)  |
| `["filter_sum", "1000", "RandomFloats", "noinit", "naive"]`    |                1.07 (5%) :x: |                   1.00 (1%)  |
| `["filter_sum", "1000", "RandomFloats", "noinit", "xf"]`       |                1.07 (5%) :x: |                   1.00 (1%)  |
| `["filter_sum", "1000", "RandomFloats", "withinit", "naive"]`  |                1.10 (5%) :x: |                   1.00 (1%)  |
| `["filter_sum", "1000", "UnitRange", "noinit", "base"]`        |                1.10 (5%) :x: |                   1.00 (1%)  |
| `["filter_sum", "1000", "UnitRange", "noinit", "naive"]`       |                1.13 (5%) :x: |                   1.00 (1%)  |
| `["filter_sum", "1000", "UnitRange", "withinit", "naive"]`     |                1.06 (5%) :x: |                   1.00 (1%)  |
| `["filter_sum", "10000", "RandomFloats", "noinit", "base"]`    |                1.10 (5%) :x: |                   1.00 (1%)  |
| `["filter_sum", "10000", "RandomFloats", "noinit", "naive"]`   |                1.17 (5%) :x: |                   1.00 (1%)  |
| `["filter_sum", "10000", "RandomFloats", "noinit", "xf"]`      |                1.09 (5%) :x: |                   1.00 (1%)  |
| `["filter_sum", "10000", "RandomFloats", "withinit", "base"]`  |                1.06 (5%) :x: |                   1.00 (1%)  |
| `["filter_sum", "10000", "RandomFloats", "withinit", "naive"]` |                1.23 (5%) :x: |                   1.00 (1%)  |
| `["filter_sum", "10000", "RandomFloats", "withinit", "xf"]`    |                1.10 (5%) :x: |                   1.00 (1%)  |
| `["filter_sum", "10000", "UnitRange", "noinit", "base"]`       |                1.10 (5%) :x: |                   1.00 (1%)  |
| `["filter_sum", "10000", "UnitRange", "noinit", "naive"]`      |                1.10 (5%) :x: |                   1.00 (1%)  |
| `["filter_sum", "10000", "UnitRange", "noinit", "xf"]`         |                1.09 (5%) :x: |                   1.00 (1%)  |
| `["filter_sum", "10000", "UnitRange", "withinit", "base"]`     |                1.10 (5%) :x: |                   1.00 (1%)  |
| `["filter_sum", "10000", "UnitRange", "withinit", "naive"]`    |                1.13 (5%) :x: |                   1.00 (1%)  |
| `["filter_sum", "10000", "UnitRange", "withinit", "xf"]`       |                1.09 (5%) :x: |                   1.00 (1%)  |
| `["findall", "base"]`                                          |                1.08 (5%) :x: |                   1.00 (1%)  |
| `["findall", "xf-array"]`                                      |                1.12 (5%) :x: |                   1.00 (1%)  |
| `["findall", "xf-iter"]`                                       |                1.08 (5%) :x: |                   1.00 (1%)  |
| `["gemm", "mul", "linalg", "256"]`                             |                1.07 (5%) :x: |                   1.00 (1%)  |
| `["gemm", "mul", "linalg", "32"]`                              | 0.92 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["gemm", "mul", "linalg", "8"]`                               |                1.08 (5%) :x: |                   1.00 (1%)  |
| `["gemm", "mul", "man", "false", "32"]`                        | 0.94 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["gemm", "mul", "man", "false", "8"]`                         |                1.13 (5%) :x: |                   1.00 (1%)  |
| `["gemm", "mul", "man", "ivdep", "32"]`                        |                1.08 (5%) :x: |                   1.00 (1%)  |
| `["gemm", "mul", "man", "ivdep", "8"]`                         |                1.38 (5%) :x: |                   1.00 (1%)  |
| `["gemm", "mul", "man", "true", "8"]`                          | 0.91 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["gemm", "mul", "xf", "false", "32"]`                         | 0.86 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["gemm", "mul", "xf", "ivdep", "32"]`                         | 0.87 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["gemm", "mul", "xf", "true", "32"]`                          |                1.10 (5%) :x: |                   1.00 (1%)  |
| `["gemm", "mul", "xf", "true", "8"]`                           |                1.13 (5%) :x: |                   1.00 (1%)  |
| `["groupby", "sum", "sac"]`                                    | 0.02 (5%) :white_check_mark: | 0.12 (1%) :white_check_mark: |
| `["mapcat_eduction", "base"]`                                  |                1.09 (5%) :x: |                   1.00 (1%)  |
| `["mapcat_eduction", "xf-xf"]`                                 |                1.07 (5%) :x: |                   1.00 (1%)  |
| `["missing_argmax", "man"]`                                    |                1.10 (5%) :x: |                   1.00 (1%)  |
| `["missing_argmax", "rf"]`                                     |                1.11 (5%) :x: |                   1.00 (1%)  |
| `["missing_argmax", "xf"]`                                     |                1.13 (5%) :x: |                   1.00 (1%)  |
| `["missing_dot", "man"]`                                       |                1.07 (5%) :x: |                   1.00 (1%)  |
| `["missing_dot", "naive"]`                                     |                1.10 (5%) :x: |                   1.00 (1%)  |
| `["missing_dot", "rf"]`                                        |                1.06 (5%) :x: |                   1.00 (1%)  |
| `["missing_dot", "xf_nota"]`                                   |                1.15 (5%) :x: |                   1.00 (1%)  |
| `["overhead", "foldl"]`                                        |                1.12 (5%) :x: |                   1.00 (1%)  |
| `["overhead", "reduce_basecase"]`                              |                1.06 (5%) :x: |                   1.00 (1%)  |
| `["set", "xf"]`                                                |                1.06 (5%) :x: |                   1.00 (1%)  |
| `["sum_transpose", "30", "noinit", "man"]`                     |                1.08 (5%) :x: |                   1.00 (1%)  |
| `["sum_transpose", "30", "noinit", "xf"]`                      |                1.06 (5%) :x: |                   1.00 (1%)  |
| `["sum_transpose", "30", "withinit", "iter"]`                  |                1.07 (5%) :x: |                   1.00 (1%)  |
| `["sum_transpose", "30", "withinit", "xf"]`                    |                1.06 (5%) :x: |                   1.00 (1%)  |
| `["teerf_filter", "noinit"]`                                   |                1.06 (5%) :x: |                   1.00 (1%)  |
| `["teerf_filter", "withinit"]`                                 |                1.09 (5%) :x: |                   1.00 (1%)  |

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
Julia Version 1.7.1
Commit ac5cc99908 (2021-12-22 19:35 UTC)
Platform Info:
  OS: Linux (x86_64-pc-linux-gnu)
      Ubuntu 20.04.3 LTS
  uname: Linux 5.11.0-1028-azure #31~20.04.2-Ubuntu SMP Tue Jan 18 08:46:15 UTC 2022 x86_64 x86_64
  CPU: Intel(R) Xeon(R) CPU E5-2673 v4 @ 2.30GHz: 
              speed         user         nice          sys         idle          irq
       #1  2294 MHz       7285 s          2 s        154 s        518 s          0 s
       #2  2294 MHz        604 s          1 s        157 s       7200 s          0 s
       
  Memory: 6.7845458984375 GB (3439.15234375 MB free)
  Uptime: 803.78 sec
  Load Avg:  1.04  1.01  0.67
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-12.0.1 (ORCJIT, broadwell)
```

### Baseline
```
Julia Version 1.7.1
Commit ac5cc99908 (2021-12-22 19:35 UTC)
Platform Info:
  OS: Linux (x86_64-pc-linux-gnu)
      Ubuntu 20.04.3 LTS
  uname: Linux 5.11.0-1028-azure #31~20.04.2-Ubuntu SMP Tue Jan 18 08:46:15 UTC 2022 x86_64 x86_64
  CPU: Intel(R) Xeon(R) CPU E5-2673 v4 @ 2.30GHz: 
              speed         user         nice          sys         idle          irq
       #1  2294 MHz      10437 s          2 s        198 s        615 s          0 s
       #2  2294 MHz        782 s          1 s        181 s      10280 s          0 s
       
  Memory: 6.7845458984375 GB (3411.71484375 MB free)
  Uptime: 1133.3 sec
  Load Avg:  1.0  1.01  0.79
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-12.0.1 (ORCJIT, broadwell)
```

---
# Target result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmark: 6 Feb 2022 - 1:29
* Package commit: 4cf859
* Julia commit: ac5cc9
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
| `["append!!", "eduction"]`                                     |  19.600 μs (5%) |         |  53.98 KiB (1%) |           8 |
| `["append!!", "xf"]`                                           |  20.800 μs (5%) |         |  53.98 KiB (1%) |           8 |
| `["cartesian", "copyto!", "iter"]`                             |   2.456 μs (5%) |         |                 |             |
| `["cartesian", "copyto!", "man"]`                              |   2.200 μs (5%) |         |                 |             |
| `["cartesian", "copyto!", "xf"]`                               |   2.456 μs (5%) |         |                 |             |
| `["cat", "base"]`                                              |   1.570 μs (5%) |         |                 |             |
| `["cat", "xf"]`                                                |   1.580 μs (5%) |         |                 |             |
| `["collect", "filter-missing"]`                                |  52.000 μs (5%) |         |  41.33 KiB (1%) |          10 |
| `["collect", "identity-float"]`                                |  20.600 μs (5%) |         | 326.61 KiB (1%) |          10 |
| `["collect", "identity-union"]`                                | 150.401 μs (5%) |         | 679.41 KiB (1%) |       10010 |
| `["dict", "base"]`                                             |   4.249 ms (5%) |         |  92.45 KiB (1%) |          22 |
| `["dict", "xf"]`                                               |   4.257 ms (5%) |         |  91.95 KiB (1%) |          18 |
| `["dot", "blas"]`                                              |   2.444 μs (5%) |         |                 |             |
| `["dot", "man"]`                                               |   2.411 μs (5%) |         |                 |             |
| `["dot", "rf"]`                                                |   3.300 μs (5%) |         |                 |             |
| `["dot", "xf"]`                                                |   3.300 μs (5%) |         |                 |             |
| `["filter_map_map!", "man"]`                                   |  67.501 μs (5%) |         |                 |             |
| `["filter_map_map!", "xf"]`                                    |  72.400 μs (5%) |         |                 |             |
| `["filter_map_reduce", "man"]`                                 | 212.801 μs (5%) |         |                 |             |
| `["filter_map_reduce", "xf"]`                                  | 206.601 μs (5%) |         |                 |             |
| `["filter_sum", "1000", "RandomFloats", "noinit", "base"]`     |   1.840 μs (5%) |         |                 |             |
| `["filter_sum", "1000", "RandomFloats", "noinit", "naive"]`    |   1.260 μs (5%) |         |                 |             |
| `["filter_sum", "1000", "RandomFloats", "noinit", "xf"]`       |   1.560 μs (5%) |         |                 |             |
| `["filter_sum", "1000", "RandomFloats", "withinit", "base"]`   |   1.510 μs (5%) |         |                 |             |
| `["filter_sum", "1000", "RandomFloats", "withinit", "naive"]`  | 639.535 ns (5%) |         |                 |             |
| `["filter_sum", "1000", "RandomFloats", "withinit", "xf"]`     |   1.510 μs (5%) |         |                 |             |
| `["filter_sum", "1000", "UnitRange", "noinit", "base"]`        | 976.596 ns (5%) |         |                 |             |
| `["filter_sum", "1000", "UnitRange", "noinit", "naive"]`       |   1.015 μs (5%) |         |                 |             |
| `["filter_sum", "1000", "UnitRange", "noinit", "xf"]`          | 229.158 ns (5%) |         |                 |             |
| `["filter_sum", "1000", "UnitRange", "withinit", "base"]`      | 165.266 ns (5%) |         |                 |             |
| `["filter_sum", "1000", "UnitRange", "withinit", "naive"]`     | 610.233 ns (5%) |         |                 |             |
| `["filter_sum", "1000", "UnitRange", "withinit", "xf"]`        | 165.899 ns (5%) |         |                 |             |
| `["filter_sum", "10000", "RandomFloats", "noinit", "base"]`    |  18.400 μs (5%) |         |                 |             |
| `["filter_sum", "10000", "RandomFloats", "noinit", "naive"]`   |  42.801 μs (5%) |         |                 |             |
| `["filter_sum", "10000", "RandomFloats", "noinit", "xf"]`      |  15.200 μs (5%) |         |                 |             |
| `["filter_sum", "10000", "RandomFloats", "withinit", "base"]`  |  15.600 μs (5%) |         |                 |             |
| `["filter_sum", "10000", "RandomFloats", "withinit", "naive"]` |  37.200 μs (5%) |         |                 |             |
| `["filter_sum", "10000", "RandomFloats", "withinit", "xf"]`    |  16.700 μs (5%) |         |                 |             |
| `["filter_sum", "10000", "UnitRange", "noinit", "base"]`       |   9.700 μs (5%) |         |                 |             |
| `["filter_sum", "10000", "UnitRange", "noinit", "naive"]`      |   9.800 μs (5%) |         |                 |             |
| `["filter_sum", "10000", "UnitRange", "noinit", "xf"]`         |   2.167 μs (5%) |         |                 |             |
| `["filter_sum", "10000", "UnitRange", "withinit", "base"]`     |   1.590 μs (5%) |         |                 |             |
| `["filter_sum", "10000", "UnitRange", "withinit", "naive"]`    |   6.260 μs (5%) |         |                 |             |
| `["filter_sum", "10000", "UnitRange", "withinit", "xf"]`       |   1.540 μs (5%) |         |                 |             |
| `["findall", "base"]`                                          | 169.001 μs (5%) |         | 797.20 KiB (1%) |           8 |
| `["findall", "xf-array"]`                                      |   1.300 ms (5%) |         |   2.94 MiB (1%) |       96426 |
| `["findall", "xf-iter"]`                                       | 835.197 μs (5%) |         |   1.83 MiB (1%) |          14 |
| `["gemm", "fusedmul", "blas", "16"]`                           |   5.380 ms (5%) |         |                 |             |
| `["gemm", "fusedmul", "blas", "2"]`                            |   3.995 ms (5%) |         |                 |             |
| `["gemm", "fusedmul", "blas", "32"]`                           |   7.160 ms (5%) |         |                 |             |
| `["gemm", "fusedmul", "blas", "8"]`                            |   4.167 ms (5%) |         |                 |             |
| `["gemm", "fusedmul", "xf", "16"]`                             |   5.435 ms (5%) |         |  192 bytes (1%) |           4 |
| `["gemm", "fusedmul", "xf", "2"]`                              | 653.604 μs (5%) |         |  192 bytes (1%) |           4 |
| `["gemm", "fusedmul", "xf", "32"]`                             |  10.940 ms (5%) |         |  192 bytes (1%) |           4 |
| `["gemm", "fusedmul", "xf", "8"]`                              |   2.722 ms (5%) |         |  192 bytes (1%) |           4 |
| `["gemm", "mul", "linalg", "256"]`                             |   1.110 ms (5%) |         |                 |             |
| `["gemm", "mul", "linalg", "32"]`                              |   3.586 μs (5%) |         |                 |             |
| `["gemm", "mul", "linalg", "8"]`                               | 324.787 ns (5%) |         |                 |             |
| `["gemm", "mul", "man", "false", "256"]`                       |   4.823 ms (5%) |         |                 |             |
| `["gemm", "mul", "man", "false", "32"]`                        |   7.450 μs (5%) |         |                 |             |
| `["gemm", "mul", "man", "false", "8"]`                         | 452.551 ns (5%) |         |                 |             |
| `["gemm", "mul", "man", "ivdep", "256"]`                       |   4.789 ms (5%) |         |                 |             |
| `["gemm", "mul", "man", "ivdep", "32"]`                        |   6.380 μs (5%) |         |                 |             |
| `["gemm", "mul", "man", "ivdep", "8"]`                         | 415.080 ns (5%) |         |                 |             |
| `["gemm", "mul", "man", "true", "256"]`                        |   4.812 ms (5%) |         |                 |             |
| `["gemm", "mul", "man", "true", "32"]`                         |   7.025 μs (5%) |         |                 |             |
| `["gemm", "mul", "man", "true", "8"]`                          | 363.366 ns (5%) |         |                 |             |
| `["gemm", "mul", "xf", "false", "256"]`                        |   4.839 ms (5%) |         |   80 bytes (1%) |           3 |
| `["gemm", "mul", "xf", "false", "32"]`                         |   7.150 μs (5%) |         |   80 bytes (1%) |           3 |
| `["gemm", "mul", "xf", "false", "8"]`                          | 485.279 ns (5%) |         |   80 bytes (1%) |           3 |
| `["gemm", "mul", "xf", "ivdep", "256"]`                        |   4.783 ms (5%) |         |   80 bytes (1%) |           3 |
| `["gemm", "mul", "xf", "ivdep", "32"]`                         |   6.000 μs (5%) |         |   80 bytes (1%) |           3 |
| `["gemm", "mul", "xf", "ivdep", "8"]`                          | 484.216 ns (5%) |         |   80 bytes (1%) |           3 |
| `["gemm", "mul", "xf", "true", "256"]`                         |   4.809 ms (5%) |         |   80 bytes (1%) |           3 |
| `["gemm", "mul", "xf", "true", "32"]`                          |   7.700 μs (5%) |         |   80 bytes (1%) |           3 |
| `["gemm", "mul", "xf", "true", "8"]`                           | 453.066 ns (5%) |         |   80 bytes (1%) |           3 |
| `["groupby", "sum", "sac"]`                                    | 130.701 μs (5%) |         |   1.64 KiB (1%) |          11 |
| `["groupby", "sum", "xf-with-init"]`                           | 128.300 μs (5%) |         |   1.05 KiB (1%) |           9 |
| `["groupby", "sum", "xf-without-init"]`                        | 123.600 μs (5%) |         |   1.05 KiB (1%) |           9 |
| `["mapcat_eduction", "base"]`                                  |  52.600 μs (5%) |         |                 |             |
| `["mapcat_eduction", "xf-eduction"]`                           |   1.730 μs (5%) |         |                 |             |
| `["mapcat_eduction", "xf-xf"]`                                 |   1.790 μs (5%) |         |                 |             |
| `["missing_argmax", "man"]`                                    |   1.610 μs (5%) |         |                 |             |
| `["missing_argmax", "rf"]`                                     |   1.280 μs (5%) |         |                 |             |
| `["missing_argmax", "xf"]`                                     |   1.420 μs (5%) |         |   32 bytes (1%) |           1 |
| `["missing_dot", "equiv"]`                                     |   2.333 μs (5%) |         |   16 bytes (1%) |           1 |
| `["missing_dot", "man"]`                                       |   1.230 μs (5%) |         |   16 bytes (1%) |           1 |
| `["missing_dot", "naive"]`                                     |   2.244 μs (5%) |         |   16 bytes (1%) |           1 |
| `["missing_dot", "rf"]`                                        |   1.220 μs (5%) |         |   16 bytes (1%) |           1 |
| `["missing_dot", "rf_nota"]`                                   |   2.400 μs (5%) |         |   16 bytes (1%) |           1 |
| `["missing_dot", "xf"]`                                        |  93.301 μs (5%) |         |  72.23 KiB (1%) |        3747 |
| `["missing_dot", "xf_nota"]`                                   |  98.001 μs (5%) |         |  72.00 KiB (1%) |        3736 |
| `["overhead", "foldl"]`                                        |   3.600 ns (5%) |         |                 |             |
| `["overhead", "reduce_basecase"]`                              | 102.872 ns (5%) |         |   16 bytes (1%) |           1 |
| `["partition_by", "man"]`                                      |   2.329 ms (5%) |         |  480 bytes (1%) |           3 |
| `["partition_by", "xf"]`                                       |   2.471 ms (5%) |         |  592 bytes (1%) |           5 |
| `["set", "base"]`                                              |   4.409 ms (5%) |         |  49.14 KiB (1%) |          17 |
| `["set", "xf"]`                                                |   4.416 ms (5%) |         |  49.17 KiB (1%) |          19 |
| `["sum_transpose", "30", "noinit", "iter"]`                    |   1.780 μs (5%) |         |                 |             |
| `["sum_transpose", "30", "noinit", "man"]`                     |   1.560 μs (5%) |         |                 |             |
| `["sum_transpose", "30", "noinit", "xf"]`                      | 869.028 ns (5%) |         |   32 bytes (1%) |           2 |
| `["sum_transpose", "30", "withinit", "iter"]`                  |   1.270 μs (5%) |         |                 |             |
| `["sum_transpose", "30", "withinit", "man"]`                   | 795.652 ns (5%) |         |                 |             |
| `["sum_transpose", "30", "withinit", "xf"]`                    | 825.000 ns (5%) |         |   48 bytes (1%) |           3 |
| `["teerf_filter", "noinit"]`                                   | 385.172 ns (5%) |         |   80 bytes (1%) |           3 |
| `["teerf_filter", "withinit"]`                                 | 227.220 ns (5%) |         |                 |             |

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
Julia Version 1.7.1
Commit ac5cc99908 (2021-12-22 19:35 UTC)
Platform Info:
  OS: Linux (x86_64-pc-linux-gnu)
      Ubuntu 20.04.3 LTS
  uname: Linux 5.11.0-1028-azure #31~20.04.2-Ubuntu SMP Tue Jan 18 08:46:15 UTC 2022 x86_64 x86_64
  CPU: Intel(R) Xeon(R) CPU E5-2673 v4 @ 2.30GHz: 
              speed         user         nice          sys         idle          irq
       #1  2294 MHz       7285 s          2 s        154 s        518 s          0 s
       #2  2294 MHz        604 s          1 s        157 s       7200 s          0 s
       
  Memory: 6.7845458984375 GB (3439.15234375 MB free)
  Uptime: 803.78 sec
  Load Avg:  1.04  1.01  0.67
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-12.0.1 (ORCJIT, broadwell)
```

---
# Baseline result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmark: 6 Feb 2022 - 1:35
* Package commit: 39038b
* Julia commit: ac5cc9
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
| `["append!!", "eduction"]`                                     |  18.300 μs (5%) |         |  53.98 KiB (1%) |           8 |
| `["append!!", "xf"]`                                           |  19.100 μs (5%) |         |  53.98 KiB (1%) |           8 |
| `["cartesian", "copyto!", "iter"]`                             |   1.944 μs (5%) |         |                 |             |
| `["cartesian", "copyto!", "man"]`                              |   2.110 μs (5%) |         |                 |             |
| `["cartesian", "copyto!", "xf"]`                               |   1.956 μs (5%) |         |                 |             |
| `["cat", "base"]`                                              |   1.470 μs (5%) |         |                 |             |
| `["cat", "xf"]`                                                |   1.450 μs (5%) |         |                 |             |
| `["collect", "filter-missing"]`                                |  46.700 μs (5%) |         |  41.33 KiB (1%) |          10 |
| `["collect", "identity-float"]`                                |  18.300 μs (5%) |         | 326.61 KiB (1%) |          10 |
| `["collect", "identity-union"]`                                | 133.601 μs (5%) |         | 679.41 KiB (1%) |       10010 |
| `["dict", "base"]`                                             |   4.152 ms (5%) |         |  92.45 KiB (1%) |          22 |
| `["dict", "xf"]`                                               |   4.185 ms (5%) |         |  91.95 KiB (1%) |          18 |
| `["dot", "blas"]`                                              |   2.433 μs (5%) |         |                 |             |
| `["dot", "man"]`                                               |   2.233 μs (5%) |         |                 |             |
| `["dot", "rf"]`                                                |   3.075 μs (5%) |         |                 |             |
| `["dot", "xf"]`                                                |   3.075 μs (5%) |         |                 |             |
| `["filter_map_map!", "man"]`                                   |  70.500 μs (5%) |         |                 |             |
| `["filter_map_map!", "xf"]`                                    |  73.500 μs (5%) |         |                 |             |
| `["filter_map_reduce", "man"]`                                 | 195.001 μs (5%) |         |                 |             |
| `["filter_map_reduce", "xf"]`                                  | 195.001 μs (5%) |         |                 |             |
| `["filter_sum", "1000", "RandomFloats", "noinit", "base"]`     |   1.780 μs (5%) |         |                 |             |
| `["filter_sum", "1000", "RandomFloats", "noinit", "naive"]`    |   1.180 μs (5%) |         |                 |             |
| `["filter_sum", "1000", "RandomFloats", "noinit", "xf"]`       |   1.460 μs (5%) |         |                 |             |
| `["filter_sum", "1000", "RandomFloats", "withinit", "base"]`   |   1.560 μs (5%) |         |                 |             |
| `["filter_sum", "1000", "RandomFloats", "withinit", "naive"]`  | 582.564 ns (5%) |         |                 |             |
| `["filter_sum", "1000", "RandomFloats", "withinit", "xf"]`     |   1.460 μs (5%) |         |                 |             |
| `["filter_sum", "1000", "UnitRange", "noinit", "base"]`        | 891.489 ns (5%) |         |                 |             |
| `["filter_sum", "1000", "UnitRange", "noinit", "naive"]`       | 900.000 ns (5%) |         |                 |             |
| `["filter_sum", "1000", "UnitRange", "noinit", "xf"]`          | 222.384 ns (5%) |         |                 |             |
| `["filter_sum", "1000", "UnitRange", "withinit", "base"]`      | 160.516 ns (5%) |         |                 |             |
| `["filter_sum", "1000", "UnitRange", "withinit", "naive"]`     | 574.432 ns (5%) |         |                 |             |
| `["filter_sum", "1000", "UnitRange", "withinit", "xf"]`        | 161.027 ns (5%) |         |                 |             |
| `["filter_sum", "10000", "RandomFloats", "noinit", "base"]`    |  16.800 μs (5%) |         |                 |             |
| `["filter_sum", "10000", "RandomFloats", "noinit", "naive"]`   |  36.700 μs (5%) |         |                 |             |
| `["filter_sum", "10000", "RandomFloats", "noinit", "xf"]`      |  13.900 μs (5%) |         |                 |             |
| `["filter_sum", "10000", "RandomFloats", "withinit", "base"]`  |  14.700 μs (5%) |         |                 |             |
| `["filter_sum", "10000", "RandomFloats", "withinit", "naive"]` |  30.300 μs (5%) |         |                 |             |
| `["filter_sum", "10000", "RandomFloats", "withinit", "xf"]`    |  15.200 μs (5%) |         |                 |             |
| `["filter_sum", "10000", "UnitRange", "noinit", "base"]`       |   8.800 μs (5%) |         |                 |             |
| `["filter_sum", "10000", "UnitRange", "noinit", "naive"]`      |   8.900 μs (5%) |         |                 |             |
| `["filter_sum", "10000", "UnitRange", "noinit", "xf"]`         |   1.989 μs (5%) |         |                 |             |
| `["filter_sum", "10000", "UnitRange", "withinit", "base"]`     |   1.450 μs (5%) |         |                 |             |
| `["filter_sum", "10000", "UnitRange", "withinit", "naive"]`    |   5.560 μs (5%) |         |                 |             |
| `["filter_sum", "10000", "UnitRange", "withinit", "xf"]`       |   1.410 μs (5%) |         |                 |             |
| `["findall", "base"]`                                          | 156.601 μs (5%) |         | 797.20 KiB (1%) |           8 |
| `["findall", "xf-array"]`                                      |   1.163 ms (5%) |         |   2.94 MiB (1%) |       96426 |
| `["findall", "xf-iter"]`                                       | 773.005 μs (5%) |         |   1.83 MiB (1%) |          14 |
| `["gemm", "fusedmul", "blas", "16"]`                           |   5.381 ms (5%) |         |                 |             |
| `["gemm", "fusedmul", "blas", "2"]`                            |   3.995 ms (5%) |         |                 |             |
| `["gemm", "fusedmul", "blas", "32"]`                           |   7.151 ms (5%) |         |                 |             |
| `["gemm", "fusedmul", "blas", "8"]`                            |   4.086 ms (5%) |         |                 |             |
| `["gemm", "fusedmul", "xf", "16"]`                             |   5.365 ms (5%) |         |  192 bytes (1%) |           4 |
| `["gemm", "fusedmul", "xf", "2"]`                              | 687.804 μs (5%) |         |  192 bytes (1%) |           4 |
| `["gemm", "fusedmul", "xf", "32"]`                             |  10.949 ms (5%) |         |  192 bytes (1%) |           4 |
| `["gemm", "fusedmul", "xf", "8"]`                              |   2.642 ms (5%) |         |  192 bytes (1%) |           4 |
| `["gemm", "mul", "linalg", "256"]`                             |   1.033 ms (5%) |         |                 |             |
| `["gemm", "mul", "linalg", "32"]`                              |   3.900 μs (5%) |         |                 |             |
| `["gemm", "mul", "linalg", "8"]`                               | 300.000 ns (5%) |         |                 |             |
| `["gemm", "mul", "man", "false", "256"]`                       |   4.877 ms (5%) |         |                 |             |
| `["gemm", "mul", "man", "false", "32"]`                        |   7.900 μs (5%) |         |                 |             |
| `["gemm", "mul", "man", "false", "8"]`                         | 400.000 ns (5%) |         |                 |             |
| `["gemm", "mul", "man", "ivdep", "256"]`                       |   4.654 ms (5%) |         |                 |             |
| `["gemm", "mul", "man", "ivdep", "32"]`                        |   5.900 μs (5%) |         |                 |             |
| `["gemm", "mul", "man", "ivdep", "8"]`                         | 300.000 ns (5%) |         |                 |             |
| `["gemm", "mul", "man", "true", "256"]`                        |   4.687 ms (5%) |         |                 |             |
| `["gemm", "mul", "man", "true", "32"]`                         |   7.000 μs (5%) |         |                 |             |
| `["gemm", "mul", "man", "true", "8"]`                          | 400.000 ns (5%) |         |                 |             |
| `["gemm", "mul", "xf", "false", "256"]`                        |   4.765 ms (5%) |         |   80 bytes (1%) |           3 |
| `["gemm", "mul", "xf", "false", "32"]`                         |   8.300 μs (5%) |         |   80 bytes (1%) |           3 |
| `["gemm", "mul", "xf", "false", "8"]`                          | 500.000 ns (5%) |         |   80 bytes (1%) |           3 |
| `["gemm", "mul", "xf", "ivdep", "256"]`                        |   4.729 ms (5%) |         |   80 bytes (1%) |           3 |
| `["gemm", "mul", "xf", "ivdep", "32"]`                         |   6.900 μs (5%) |         |   80 bytes (1%) |           3 |
| `["gemm", "mul", "xf", "ivdep", "8"]`                          | 500.000 ns (5%) |         |   80 bytes (1%) |           3 |
| `["gemm", "mul", "xf", "true", "256"]`                         |   4.625 ms (5%) |         |   80 bytes (1%) |           3 |
| `["gemm", "mul", "xf", "true", "32"]`                          |   7.000 μs (5%) |         |   80 bytes (1%) |           3 |
| `["gemm", "mul", "xf", "true", "8"]`                           | 400.000 ns (5%) |         |   80 bytes (1%) |           3 |
| `["groupby", "sum", "sac"]`                                    |   8.609 ms (5%) |         |  13.16 KiB (1%) |         103 |
| `["groupby", "sum", "xf-with-init"]`                           | 128.501 μs (5%) |         |   1.05 KiB (1%) |           9 |
| `["groupby", "sum", "xf-without-init"]`                        | 127.101 μs (5%) |         |   1.05 KiB (1%) |           9 |
| `["mapcat_eduction", "base"]`                                  |  48.400 μs (5%) |         |                 |             |
| `["mapcat_eduction", "xf-eduction"]`                           |   1.680 μs (5%) |         |                 |             |
| `["mapcat_eduction", "xf-xf"]`                                 |   1.680 μs (5%) |         |                 |             |
| `["missing_argmax", "man"]`                                    |   1.470 μs (5%) |         |                 |             |
| `["missing_argmax", "rf"]`                                     |   1.150 μs (5%) |         |                 |             |
| `["missing_argmax", "xf"]`                                     |   1.260 μs (5%) |         |   32 bytes (1%) |           1 |
| `["missing_dot", "equiv"]`                                     |   2.311 μs (5%) |         |   16 bytes (1%) |           1 |
| `["missing_dot", "man"]`                                       |   1.150 μs (5%) |         |   16 bytes (1%) |           1 |
| `["missing_dot", "naive"]`                                     |   2.044 μs (5%) |         |   16 bytes (1%) |           1 |
| `["missing_dot", "rf"]`                                        |   1.150 μs (5%) |         |   16 bytes (1%) |           1 |
| `["missing_dot", "rf_nota"]`                                   |   2.378 μs (5%) |         |   16 bytes (1%) |           1 |
| `["missing_dot", "xf"]`                                        |  95.400 μs (5%) |         |  72.17 KiB (1%) |        3744 |
| `["missing_dot", "xf_nota"]`                                   |  85.401 μs (5%) |         |  72.11 KiB (1%) |        3741 |
| `["overhead", "foldl"]`                                        |   3.200 ns (5%) |         |                 |             |
| `["overhead", "reduce_basecase"]`                              |  97.340 ns (5%) |         |   16 bytes (1%) |           1 |
| `["partition_by", "man"]`                                      |   2.247 ms (5%) |         |  480 bytes (1%) |           3 |
| `["partition_by", "xf"]`                                       |   2.406 ms (5%) |         |  592 bytes (1%) |           5 |
| `["set", "base"]`                                              |   4.296 ms (5%) |         |  49.14 KiB (1%) |          17 |
| `["set", "xf"]`                                                |   4.156 ms (5%) |         |  49.17 KiB (1%) |          19 |
| `["sum_transpose", "30", "noinit", "iter"]`                    |   1.850 μs (5%) |         |                 |             |
| `["sum_transpose", "30", "noinit", "man"]`                     |   1.450 μs (5%) |         |                 |             |
| `["sum_transpose", "30", "noinit", "xf"]`                      | 816.901 ns (5%) |         |   32 bytes (1%) |           2 |
| `["sum_transpose", "30", "withinit", "iter"]`                  |   1.190 μs (5%) |         |                 |             |
| `["sum_transpose", "30", "withinit", "man"]`                   | 771.014 ns (5%) |         |                 |             |
| `["sum_transpose", "30", "withinit", "xf"]`                    | 776.485 ns (5%) |         |   48 bytes (1%) |           3 |
| `["teerf_filter", "noinit"]`                                   | 362.201 ns (5%) |         |   80 bytes (1%) |           3 |
| `["teerf_filter", "withinit"]`                                 | 208.065 ns (5%) |         |                 |             |

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
Julia Version 1.7.1
Commit ac5cc99908 (2021-12-22 19:35 UTC)
Platform Info:
  OS: Linux (x86_64-pc-linux-gnu)
      Ubuntu 20.04.3 LTS
  uname: Linux 5.11.0-1028-azure #31~20.04.2-Ubuntu SMP Tue Jan 18 08:46:15 UTC 2022 x86_64 x86_64
  CPU: Intel(R) Xeon(R) CPU E5-2673 v4 @ 2.30GHz: 
              speed         user         nice          sys         idle          irq
       #1  2294 MHz      10437 s          2 s        198 s        615 s          0 s
       #2  2294 MHz        782 s          1 s        181 s      10280 s          0 s
       
  Memory: 6.7845458984375 GB (3411.71484375 MB free)
  Uptime: 1133.3 sec
  Load Avg:  1.0  1.01  0.79
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-12.0.1 (ORCJIT, broadwell)
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
    Model:                           79
    Model name:                      Intel(R) Xeon(R) CPU E5-2673 v4 @ 2.30GHz
    Stepping:                        1
    CPU MHz:                         2294.685
    BogoMIPS:                        4589.37
    Hypervisor vendor:               Microsoft
    Virtualization type:             full
    L1d cache:                       64 KiB
    L1i cache:                       64 KiB
    L2 cache:                        512 KiB
    L3 cache:                        50 MiB
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
    Flags:                           fpu vme de pse tsc msr pae mce cx8 apic sep mtrr pge mca cmov pat pse36 clflush mmx fxsr sse sse2 ss ht syscall nx pdpe1gb rdtscp lm constant_tsc rep_good nopl xtopology cpuid pni pclmulqdq ssse3 fma cx16 pcid sse4_1 sse4_2 movbe popcnt aes xsave avx f16c rdrand hypervisor lahf_lm abm 3dnowprefetch invpcid_single pti fsgsbase bmi1 hle avx2 smep bmi2 erms invpcid rtm rdseed adx smap xsaveopt md_clear
    

| Cpu Property       | Value                                                   |
|:------------------ |:------------------------------------------------------- |
| Brand              | Intel(R) Xeon(R) CPU E5-2673 v4 @ 2.30GHz               |
| Vendor             | :Intel                                                  |
| Architecture       | :Broadwell                                              |
| Model              | Family: 0x06, Model: 0x4f, Stepping: 0x01, Type: 0x00   |
| Cores              | 2 physical cores, 2 logical cores (on executing CPU)    |
|                    | No Hyperthreading hardware capability detected          |
| Clock Frequencies  | Not supported by CPU                                    |
| Data Cache         | Level 1:3 : (32, 256, 51200) kbytes                     |
|                    | 64 byte cache line size                                 |
| Address Size       | 48 bits virtual, 46 bits physical                       |
| SIMD               | 256 bit = 32 byte max. SIMD vector size                 |
| Time Stamp Counter | TSC is accessible via `rdtsc`                           |
|                    | TSC increased at every clock cycle (non-invariant TSC)  |
| Perf. Monitoring   | Performance Monitoring Counters (PMC) are not supported |
| Hypervisor         | Yes, Microsoft                                          |

