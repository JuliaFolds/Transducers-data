# Benchmark result

* Pull request commit: [`21ff2fddaa5c7179590cbfa3280ceaa6f1e2f450`](https://github.com/JuliaFolds/Transducers.jl/commit/21ff2fddaa5c7179590cbfa3280ceaa6f1e2f450)
* Pull request: <https://github.com/JuliaFolds/Transducers.jl/pull/243> (Update */Manifest.toml)

# Judge result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmarks:
    - Target: 4 Nov 2023 - 01:25
    - Baseline: 4 Nov 2023 - 01:30
* Package commits:
    - Target: 189991
    - Baseline: 2a51f8
* Julia commits:
    - Target: 742b9a
    - Baseline: 742b9a
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
| `["cartesian", "copyto!", "iter"]`                             | 0.92 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["cat", "base"]`                                              | 0.93 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["cat", "xf"]`                                                | 0.93 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["collect", "filter-missing"]`                                |                1.28 (5%) :x: |                   1.00 (1%)  |
| `["filter_map_reduce", "man"]`                                 | 0.93 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["filter_map_reduce", "xf"]`                                  | 0.93 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["filter_sum", "1000", "RandomFloats", "noinit", "xf"]`       | 0.93 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["filter_sum", "1000", "RandomFloats", "withinit", "xf"]`     | 0.93 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["filter_sum", "1000", "UnitRange", "withinit", "naive"]`     | 0.93 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["filter_sum", "10000", "RandomFloats", "withinit", "naive"]` | 0.77 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["filter_sum", "10000", "UnitRange", "noinit", "base"]`       | 0.94 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["filter_sum", "10000", "UnitRange", "noinit", "naive"]`      | 0.94 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["filter_sum", "10000", "UnitRange", "withinit", "base"]`     | 0.93 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["gemm", "fusedmul", "blas", "16"]`                           | 0.94 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["gemm", "mul", "man", "false", "32"]`                        | 0.95 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["gemm", "mul", "man", "false", "8"]`                         | 0.91 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["gemm", "mul", "man", "ivdep", "8"]`                         |                1.17 (5%) :x: |                   1.00 (1%)  |
| `["gemm", "mul", "xf", "ivdep", "32"]`                         | 0.94 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["gemm", "mul", "xf", "ivdep", "8"]`                          | 0.93 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["gemm", "mul", "xf", "true", "8"]`                           |                1.15 (5%) :x: |                   1.00 (1%)  |
| `["groupby", "sum", "sac"]`                                    | 0.02 (5%) :white_check_mark: | 0.12 (1%) :white_check_mark: |
| `["groupby", "sum", "xf-without-init"]`                        |                1.07 (5%) :x: |                   1.00 (1%)  |
| `["mapcat_eduction", "base"]`                                  | 0.93 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["mapcat_eduction", "xf-eduction"]`                           | 0.93 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["mapcat_eduction", "xf-xf"]`                                 | 0.93 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["missing_dot", "equiv"]`                                     | 0.91 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["missing_dot", "naive"]`                                     | 0.95 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["missing_dot", "rf"]`                                        | 0.95 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["missing_dot", "rf_nota"]`                                   | 0.92 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["missing_dot", "xf"]`                                        | 0.94 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["missing_dot", "xf_nota"]`                                   | 0.93 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["overhead", "foldl"]`                                        | 0.93 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["overhead", "reduce_basecase"]`                              |                1.08 (5%) :x: |                   1.00 (1%)  |
| `["sum_transpose", "30", "noinit", "iter"]`                    |                1.06 (5%) :x: |                   1.00 (1%)  |

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
      Ubuntu 22.04.3 LTS
  uname: Linux 6.2.0-1015-azure #15~22.04.1-Ubuntu SMP Fri Oct  6 13:20:44 UTC 2023 x86_64 x86_64
  CPU: Intel(R) Xeon(R) CPU E5-2673 v3 @ 2.40GHz: 
              speed         user         nice          sys         idle          irq
       #1  2397 MHz       6747 s          0 s        192 s       2908 s          0 s
       #2  2397 MHz       1423 s          0 s        274 s       8113 s          0 s
       
  Memory: 6.7597503662109375 GB (3563.02734375 MB free)
  Uptime: 995.95 sec
  Load Avg:  1.24  1.09  0.71
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-12.0.1 (ORCJIT, haswell)
```

### Baseline
```
Julia Version 1.7.3
Commit 742b9abb4d (2022-05-06 12:58 UTC)
Platform Info:
  OS: Linux (x86_64-pc-linux-gnu)
      Ubuntu 22.04.3 LTS
  uname: Linux 6.2.0-1015-azure #15~22.04.1-Ubuntu SMP Fri Oct  6 13:20:44 UTC 2023 x86_64 x86_64
  CPU: Intel(R) Xeon(R) CPU E5-2673 v3 @ 2.40GHz: 
              speed         user         nice          sys         idle          irq
       #1  2397 MHz       8610 s          0 s        272 s       4218 s          0 s
       #2  2397 MHz       2843 s          0 s        322 s       9896 s          0 s
       
  Memory: 6.7597503662109375 GB (3485.97265625 MB free)
  Uptime: 1322.17 sec
  Load Avg:  1.0  1.06  0.84
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-12.0.1 (ORCJIT, haswell)
```

---
# Target result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmark: 4 Nov 2023 - 1:25
* Package commit: 189991
* Julia commit: 742b9a
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
| `["append!!", "eduction"]`                                     |  23.001 μs (5%) |         |  53.98 KiB (1%) |           8 |
| `["append!!", "xf"]`                                           |  22.701 μs (5%) |         |  53.98 KiB (1%) |           8 |
| `["cartesian", "copyto!", "iter"]`                             |   2.278 μs (5%) |         |                 |             |
| `["cartesian", "copyto!", "man"]`                              |   2.444 μs (5%) |         |                 |             |
| `["cartesian", "copyto!", "xf"]`                               |   2.456 μs (5%) |         |                 |             |
| `["cat", "base"]`                                              |   1.780 μs (5%) |         |                 |             |
| `["cat", "xf"]`                                                |   1.480 μs (5%) |         |                 |             |
| `["collect", "filter-missing"]`                                |   1.640 μs (5%) |         |   9.94 KiB (1%) |           1 |
| `["collect", "identity-float"]`                                |   9.400 μs (5%) |         |  78.17 KiB (1%) |           2 |
| `["collect", "identity-union"]`                                | 163.904 μs (5%) |         | 400.53 KiB (1%) |       10003 |
| `["dict", "base"]`                                             |   4.694 ms (5%) |         |  92.45 KiB (1%) |          22 |
| `["dict", "xf"]`                                               |   4.655 ms (5%) |         |  91.95 KiB (1%) |          18 |
| `["dot", "blas"]`                                              |   2.178 μs (5%) |         |                 |             |
| `["dot", "man"]`                                               |   2.211 μs (5%) |         |                 |             |
| `["dot", "rf"]`                                                |   2.733 μs (5%) |         |                 |             |
| `["dot", "xf"]`                                                |   2.733 μs (5%) |         |                 |             |
| `["filter_map_map!", "man"]`                                   |  65.302 μs (5%) |         |                 |             |
| `["filter_map_map!", "xf"]`                                    |  69.502 μs (5%) |         |                 |             |
| `["filter_map_reduce", "man"]`                                 | 241.807 μs (5%) |         |                 |             |
| `["filter_map_reduce", "xf"]`                                  | 241.707 μs (5%) |         |                 |             |
| `["filter_sum", "1000", "RandomFloats", "noinit", "base"]`     |   2.600 μs (5%) |         |                 |             |
| `["filter_sum", "1000", "RandomFloats", "noinit", "naive"]`    |   1.430 μs (5%) |         |                 |             |
| `["filter_sum", "1000", "RandomFloats", "noinit", "xf"]`       |   1.710 μs (5%) |         |                 |             |
| `["filter_sum", "1000", "RandomFloats", "withinit", "base"]`   |   1.770 μs (5%) |         |                 |             |
| `["filter_sum", "1000", "RandomFloats", "withinit", "naive"]`  | 885.953 ns (5%) |         |                 |             |
| `["filter_sum", "1000", "RandomFloats", "withinit", "xf"]`     |   1.710 μs (5%) |         |                 |             |
| `["filter_sum", "1000", "UnitRange", "noinit", "base"]`        |   1.090 μs (5%) |         |                 |             |
| `["filter_sum", "1000", "UnitRange", "noinit", "naive"]`       |   1.090 μs (5%) |         |                 |             |
| `["filter_sum", "1000", "UnitRange", "noinit", "xf"]`          | 258.098 ns (5%) |         |                 |             |
| `["filter_sum", "1000", "UnitRange", "withinit", "base"]`      | 192.609 ns (5%) |         |                 |             |
| `["filter_sum", "1000", "UnitRange", "withinit", "naive"]`     | 696.619 ns (5%) |         |                 |             |
| `["filter_sum", "1000", "UnitRange", "withinit", "xf"]`        | 194.407 ns (5%) |         |                 |             |
| `["filter_sum", "10000", "RandomFloats", "noinit", "base"]`    |  27.100 μs (5%) |         |                 |             |
| `["filter_sum", "10000", "RandomFloats", "noinit", "naive"]`   |  51.602 μs (5%) |         |                 |             |
| `["filter_sum", "10000", "RandomFloats", "noinit", "xf"]`      |  18.500 μs (5%) |         |                 |             |
| `["filter_sum", "10000", "RandomFloats", "withinit", "base"]`  |  18.500 μs (5%) |         |                 |             |
| `["filter_sum", "10000", "RandomFloats", "withinit", "naive"]` |  34.501 μs (5%) |         |                 |             |
| `["filter_sum", "10000", "RandomFloats", "withinit", "xf"]`    |  18.500 μs (5%) |         |                 |             |
| `["filter_sum", "10000", "UnitRange", "noinit", "base"]`       |  10.400 μs (5%) |         |                 |             |
| `["filter_sum", "10000", "UnitRange", "noinit", "naive"]`      |  10.400 μs (5%) |         |                 |             |
| `["filter_sum", "10000", "UnitRange", "noinit", "xf"]`         |   2.622 μs (5%) |         |                 |             |
| `["filter_sum", "10000", "UnitRange", "withinit", "base"]`     |   1.750 μs (5%) |         |                 |             |
| `["filter_sum", "10000", "UnitRange", "withinit", "naive"]`    |   6.900 μs (5%) |         |                 |             |
| `["filter_sum", "10000", "UnitRange", "withinit", "xf"]`       |   1.810 μs (5%) |         |                 |             |
| `["findall", "base"]`                                          | 184.706 μs (5%) |         | 797.20 KiB (1%) |           8 |
| `["findall", "xf-array"]`                                      |   1.517 ms (5%) |         |   2.94 MiB (1%) |       96426 |
| `["findall", "xf-iter"]`                                       | 938.828 μs (5%) |         |   1.83 MiB (1%) |          14 |
| `["gemm", "fusedmul", "blas", "16"]`                           |   4.837 ms (5%) |         |                 |             |
| `["gemm", "fusedmul", "blas", "2"]`                            |   3.835 ms (5%) |         |                 |             |
| `["gemm", "fusedmul", "blas", "32"]`                           |   6.456 ms (5%) |         |                 |             |
| `["gemm", "fusedmul", "blas", "8"]`                            |   3.751 ms (5%) |         |                 |             |
| `["gemm", "fusedmul", "xf", "16"]`                             |   5.323 ms (5%) |         |  192 bytes (1%) |           4 |
| `["gemm", "fusedmul", "xf", "2"]`                              | 677.220 μs (5%) |         |  192 bytes (1%) |           4 |
| `["gemm", "fusedmul", "xf", "32"]`                             |  10.709 ms (5%) |         |  192 bytes (1%) |           4 |
| `["gemm", "fusedmul", "xf", "8"]`                              |   2.655 ms (5%) |         |  192 bytes (1%) |           4 |
| `["gemm", "mul", "linalg", "256"]`                             | 990.329 μs (5%) |         |                 |             |
| `["gemm", "mul", "linalg", "32"]`                              |   3.700 μs (5%) |         |                 |             |
| `["gemm", "mul", "linalg", "8"]`                               | 296.954 ns (5%) |         |                 |             |
| `["gemm", "mul", "man", "false", "256"]`                       |   4.348 ms (5%) |         |                 |             |
| `["gemm", "mul", "man", "false", "32"]`                        |   7.375 μs (5%) |         |                 |             |
| `["gemm", "mul", "man", "false", "8"]`                         | 453.077 ns (5%) |         |                 |             |
| `["gemm", "mul", "man", "ivdep", "256"]`                       |   4.309 ms (5%) |         |                 |             |
| `["gemm", "mul", "man", "ivdep", "32"]`                        |   5.934 μs (5%) |         |                 |             |
| `["gemm", "mul", "man", "ivdep", "8"]`                         | 468.378 ns (5%) |         |                 |             |
| `["gemm", "mul", "man", "true", "256"]`                        |   4.331 ms (5%) |         |                 |             |
| `["gemm", "mul", "man", "true", "32"]`                         |   6.960 μs (5%) |         |                 |             |
| `["gemm", "mul", "man", "true", "8"]`                          | 519.371 ns (5%) |         |                 |             |
| `["gemm", "mul", "xf", "false", "256"]`                        |   4.351 ms (5%) |         |   80 bytes (1%) |           3 |
| `["gemm", "mul", "xf", "false", "32"]`                         |   7.700 μs (5%) |         |   80 bytes (1%) |           3 |
| `["gemm", "mul", "xf", "false", "8"]`                          | 573.760 ns (5%) |         |   80 bytes (1%) |           3 |
| `["gemm", "mul", "xf", "ivdep", "256"]`                        |   4.306 ms (5%) |         |   80 bytes (1%) |           3 |
| `["gemm", "mul", "xf", "ivdep", "32"]`                         |   5.833 μs (5%) |         |   80 bytes (1%) |           3 |
| `["gemm", "mul", "xf", "ivdep", "8"]`                          | 463.418 ns (5%) |         |   80 bytes (1%) |           3 |
| `["gemm", "mul", "xf", "true", "256"]`                         |   4.316 ms (5%) |         |   80 bytes (1%) |           3 |
| `["gemm", "mul", "xf", "true", "32"]`                          |   7.020 μs (5%) |         |   80 bytes (1%) |           3 |
| `["gemm", "mul", "xf", "true", "8"]`                           | 573.580 ns (5%) |         |   80 bytes (1%) |           3 |
| `["groupby", "sum", "sac"]`                                    | 164.105 μs (5%) |         |   1.64 KiB (1%) |          11 |
| `["groupby", "sum", "xf-with-init"]`                           | 153.504 μs (5%) |         |   1.05 KiB (1%) |           9 |
| `["groupby", "sum", "xf-without-init"]`                        | 163.805 μs (5%) |         |   1.05 KiB (1%) |           9 |
| `["mapcat_eduction", "base"]`                                  |  59.801 μs (5%) |         |                 |             |
| `["mapcat_eduction", "xf-eduction"]`                           |   1.570 μs (5%) |         |                 |             |
| `["mapcat_eduction", "xf-xf"]`                                 |   1.570 μs (5%) |         |                 |             |
| `["missing_argmax", "man"]`                                    |   1.900 μs (5%) |         |                 |             |
| `["missing_argmax", "rf"]`                                     |   1.640 μs (5%) |         |                 |             |
| `["missing_argmax", "xf"]`                                     |   1.680 μs (5%) |         |   32 bytes (1%) |           1 |
| `["missing_dot", "equiv"]`                                     |   2.589 μs (5%) |         |   16 bytes (1%) |           1 |
| `["missing_dot", "man"]`                                       |   1.410 μs (5%) |         |   16 bytes (1%) |           1 |
| `["missing_dot", "naive"]`                                     |   2.478 μs (5%) |         |   16 bytes (1%) |           1 |
| `["missing_dot", "rf"]`                                        |   1.390 μs (5%) |         |   16 bytes (1%) |           1 |
| `["missing_dot", "rf_nota"]`                                   |   2.622 μs (5%) |         |   16 bytes (1%) |           1 |
| `["missing_dot", "xf"]`                                        | 105.303 μs (5%) |         |  72.02 KiB (1%) |        3736 |
| `["missing_dot", "xf_nota"]`                                   | 105.603 μs (5%) |         |  72.33 KiB (1%) |        3750 |
| `["overhead", "foldl"]`                                        |   4.100 ns (5%) |         |                 |             |
| `["overhead", "reduce_basecase"]`                              | 127.481 ns (5%) |         |   16 bytes (1%) |           1 |
| `["partition_by", "man"]`                                      |   2.568 ms (5%) |         |  480 bytes (1%) |           3 |
| `["partition_by", "xf"]`                                       |   2.907 ms (5%) |         |  592 bytes (1%) |           5 |
| `["set", "base"]`                                              |   4.890 ms (5%) |         |  49.14 KiB (1%) |          17 |
| `["set", "xf"]`                                                |   4.866 ms (5%) |         |  49.17 KiB (1%) |          19 |
| `["sum_transpose", "30", "noinit", "iter"]`                    |   2.233 μs (5%) |         |                 |             |
| `["sum_transpose", "30", "noinit", "man"]`                     |   1.760 μs (5%) |         |                 |             |
| `["sum_transpose", "30", "noinit", "xf"]`                      | 937.500 ns (5%) |         |                 |             |
| `["sum_transpose", "30", "withinit", "iter"]`                  |   1.510 μs (5%) |         |                 |             |
| `["sum_transpose", "30", "withinit", "man"]`                   | 936.667 ns (5%) |         |                 |             |
| `["sum_transpose", "30", "withinit", "xf"]`                    | 969.565 ns (5%) |         |                 |             |
| `["teerf_filter", "noinit"]`                                   | 468.221 ns (5%) |         |   80 bytes (1%) |           3 |
| `["teerf_filter", "withinit"]`                                 | 266.570 ns (5%) |         |                 |             |

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
      Ubuntu 22.04.3 LTS
  uname: Linux 6.2.0-1015-azure #15~22.04.1-Ubuntu SMP Fri Oct  6 13:20:44 UTC 2023 x86_64 x86_64
  CPU: Intel(R) Xeon(R) CPU E5-2673 v3 @ 2.40GHz: 
              speed         user         nice          sys         idle          irq
       #1  2397 MHz       6747 s          0 s        192 s       2908 s          0 s
       #2  2397 MHz       1423 s          0 s        274 s       8113 s          0 s
       
  Memory: 6.7597503662109375 GB (3563.02734375 MB free)
  Uptime: 995.95 sec
  Load Avg:  1.24  1.09  0.71
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-12.0.1 (ORCJIT, haswell)
```

---
# Baseline result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmark: 4 Nov 2023 - 1:30
* Package commit: 2a51f8
* Julia commit: 742b9a
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
| `["append!!", "eduction"]`                                     |  22.700 μs (5%) |         |  53.98 KiB (1%) |           8 |
| `["append!!", "xf"]`                                           |  22.801 μs (5%) |         |  53.98 KiB (1%) |           8 |
| `["cartesian", "copyto!", "iter"]`                             |   2.478 μs (5%) |         |                 |             |
| `["cartesian", "copyto!", "man"]`                              |   2.500 μs (5%) |         |                 |             |
| `["cartesian", "copyto!", "xf"]`                               |   2.578 μs (5%) |         |                 |             |
| `["cat", "base"]`                                              |   1.920 μs (5%) |         |                 |             |
| `["cat", "xf"]`                                                |   1.590 μs (5%) |         |                 |             |
| `["collect", "filter-missing"]`                                |   1.280 μs (5%) |         |   9.94 KiB (1%) |           1 |
| `["collect", "identity-float"]`                                |   9.300 μs (5%) |         |  78.17 KiB (1%) |           2 |
| `["collect", "identity-union"]`                                | 162.007 μs (5%) |         | 400.53 KiB (1%) |       10003 |
| `["dict", "base"]`                                             |   4.786 ms (5%) |         |  92.45 KiB (1%) |          22 |
| `["dict", "xf"]`                                               |   4.769 ms (5%) |         |  91.95 KiB (1%) |          18 |
| `["dot", "blas"]`                                              |   2.156 μs (5%) |         |                 |             |
| `["dot", "man"]`                                               |   2.222 μs (5%) |         |                 |             |
| `["dot", "rf"]`                                                |   2.722 μs (5%) |         |                 |             |
| `["dot", "xf"]`                                                |   2.733 μs (5%) |         |                 |             |
| `["filter_map_map!", "man"]`                                   |  64.502 μs (5%) |         |                 |             |
| `["filter_map_map!", "xf"]`                                    |  68.902 μs (5%) |         |                 |             |
| `["filter_map_reduce", "man"]`                                 | 259.609 μs (5%) |         |                 |             |
| `["filter_map_reduce", "xf"]`                                  | 259.609 μs (5%) |         |                 |             |
| `["filter_sum", "1000", "RandomFloats", "noinit", "base"]`     |   2.622 μs (5%) |         |                 |             |
| `["filter_sum", "1000", "RandomFloats", "noinit", "naive"]`    |   1.430 μs (5%) |         |                 |             |
| `["filter_sum", "1000", "RandomFloats", "noinit", "xf"]`       |   1.840 μs (5%) |         |                 |             |
| `["filter_sum", "1000", "RandomFloats", "withinit", "base"]`   |   1.840 μs (5%) |         |                 |             |
| `["filter_sum", "1000", "RandomFloats", "withinit", "naive"]`  | 923.484 ns (5%) |         |                 |             |
| `["filter_sum", "1000", "RandomFloats", "withinit", "xf"]`     |   1.840 μs (5%) |         |                 |             |
| `["filter_sum", "1000", "UnitRange", "noinit", "base"]`        |   1.120 μs (5%) |         |                 |             |
| `["filter_sum", "1000", "UnitRange", "noinit", "naive"]`       |   1.130 μs (5%) |         |                 |             |
| `["filter_sum", "1000", "UnitRange", "noinit", "xf"]`          | 269.951 ns (5%) |         |                 |             |
| `["filter_sum", "1000", "UnitRange", "withinit", "base"]`      | 197.641 ns (5%) |         |                 |             |
| `["filter_sum", "1000", "UnitRange", "withinit", "naive"]`     | 748.327 ns (5%) |         |                 |             |
| `["filter_sum", "1000", "UnitRange", "withinit", "xf"]`        | 201.520 ns (5%) |         |                 |             |
| `["filter_sum", "10000", "RandomFloats", "noinit", "base"]`    |  26.100 μs (5%) |         |                 |             |
| `["filter_sum", "10000", "RandomFloats", "noinit", "naive"]`   |  52.001 μs (5%) |         |                 |             |
| `["filter_sum", "10000", "RandomFloats", "noinit", "xf"]`      |  18.500 μs (5%) |         |                 |             |
| `["filter_sum", "10000", "RandomFloats", "withinit", "base"]`  |  18.500 μs (5%) |         |                 |             |
| `["filter_sum", "10000", "RandomFloats", "withinit", "naive"]` |  44.602 μs (5%) |         |                 |             |
| `["filter_sum", "10000", "RandomFloats", "withinit", "xf"]`    |  18.500 μs (5%) |         |                 |             |
| `["filter_sum", "10000", "UnitRange", "noinit", "base"]`       |  11.100 μs (5%) |         |                 |             |
| `["filter_sum", "10000", "UnitRange", "noinit", "naive"]`      |  11.100 μs (5%) |         |                 |             |
| `["filter_sum", "10000", "UnitRange", "noinit", "xf"]`         |   2.633 μs (5%) |         |                 |             |
| `["filter_sum", "10000", "UnitRange", "withinit", "base"]`     |   1.880 μs (5%) |         |                 |             |
| `["filter_sum", "10000", "UnitRange", "withinit", "naive"]`    |   7.150 μs (5%) |         |                 |             |
| `["filter_sum", "10000", "UnitRange", "withinit", "xf"]`       |   1.880 μs (5%) |         |                 |             |
| `["findall", "base"]`                                          | 184.607 μs (5%) |         | 797.20 KiB (1%) |           8 |
| `["findall", "xf-array"]`                                      |   1.495 ms (5%) |         |   2.94 MiB (1%) |       96426 |
| `["findall", "xf-iter"]`                                       | 969.436 μs (5%) |         |   1.83 MiB (1%) |          14 |
| `["gemm", "fusedmul", "blas", "16"]`                           |   5.140 ms (5%) |         |                 |             |
| `["gemm", "fusedmul", "blas", "2"]`                            |   3.845 ms (5%) |         |                 |             |
| `["gemm", "fusedmul", "blas", "32"]`                           |   6.425 ms (5%) |         |                 |             |
| `["gemm", "fusedmul", "blas", "8"]`                            |   3.725 ms (5%) |         |                 |             |
| `["gemm", "fusedmul", "xf", "16"]`                             |   5.334 ms (5%) |         |  192 bytes (1%) |           4 |
| `["gemm", "fusedmul", "xf", "2"]`                              | 690.924 μs (5%) |         |  192 bytes (1%) |           4 |
| `["gemm", "fusedmul", "xf", "32"]`                             |  10.825 ms (5%) |         |  192 bytes (1%) |           4 |
| `["gemm", "fusedmul", "xf", "8"]`                              |   2.697 ms (5%) |         |  192 bytes (1%) |           4 |
| `["gemm", "mul", "linalg", "256"]`                             | 989.533 μs (5%) |         |                 |             |
| `["gemm", "mul", "linalg", "32"]`                              |   3.800 μs (5%) |         |                 |             |
| `["gemm", "mul", "linalg", "8"]`                               | 300.000 ns (5%) |         |                 |             |
| `["gemm", "mul", "man", "false", "256"]`                       |   4.323 ms (5%) |         |                 |             |
| `["gemm", "mul", "man", "false", "32"]`                        |   7.800 μs (5%) |         |                 |             |
| `["gemm", "mul", "man", "false", "8"]`                         | 500.000 ns (5%) |         |                 |             |
| `["gemm", "mul", "man", "ivdep", "256"]`                       |   4.276 ms (5%) |         |                 |             |
| `["gemm", "mul", "man", "ivdep", "32"]`                        |   6.200 μs (5%) |         |                 |             |
| `["gemm", "mul", "man", "ivdep", "8"]`                         | 400.000 ns (5%) |         |                 |             |
| `["gemm", "mul", "man", "true", "256"]`                        |   4.297 ms (5%) |         |                 |             |
| `["gemm", "mul", "man", "true", "32"]`                         |   7.200 μs (5%) |         |                 |             |
| `["gemm", "mul", "man", "true", "8"]`                          | 500.000 ns (5%) |         |                 |             |
| `["gemm", "mul", "xf", "false", "256"]`                        |   4.327 ms (5%) |         |   80 bytes (1%) |           3 |
| `["gemm", "mul", "xf", "false", "32"]`                         |   7.800 μs (5%) |         |   80 bytes (1%) |           3 |
| `["gemm", "mul", "xf", "false", "8"]`                          | 600.000 ns (5%) |         |   80 bytes (1%) |           3 |
| `["gemm", "mul", "xf", "ivdep", "256"]`                        |   4.281 ms (5%) |         |   80 bytes (1%) |           3 |
| `["gemm", "mul", "xf", "ivdep", "32"]`                         |   6.200 μs (5%) |         |   80 bytes (1%) |           3 |
| `["gemm", "mul", "xf", "ivdep", "8"]`                          | 500.000 ns (5%) |         |   80 bytes (1%) |           3 |
| `["gemm", "mul", "xf", "true", "256"]`                         |   4.295 ms (5%) |         |   80 bytes (1%) |           3 |
| `["gemm", "mul", "xf", "true", "32"]`                          |   7.100 μs (5%) |         |   80 bytes (1%) |           3 |
| `["gemm", "mul", "xf", "true", "8"]`                           | 500.000 ns (5%) |         |   80 bytes (1%) |           3 |
| `["groupby", "sum", "sac"]`                                    |   9.119 ms (5%) |         |  13.14 KiB (1%) |         103 |
| `["groupby", "sum", "xf-with-init"]`                           | 159.605 μs (5%) |         |   1.05 KiB (1%) |           9 |
| `["groupby", "sum", "xf-without-init"]`                        | 153.505 μs (5%) |         |   1.05 KiB (1%) |           9 |
| `["mapcat_eduction", "base"]`                                  |  64.102 μs (5%) |         |                 |             |
| `["mapcat_eduction", "xf-eduction"]`                           |   1.680 μs (5%) |         |                 |             |
| `["mapcat_eduction", "xf-xf"]`                                 |   1.680 μs (5%) |         |                 |             |
| `["missing_argmax", "man"]`                                    |   1.950 μs (5%) |         |                 |             |
| `["missing_argmax", "rf"]`                                     |   1.620 μs (5%) |         |                 |             |
| `["missing_argmax", "xf"]`                                     |   1.680 μs (5%) |         |   32 bytes (1%) |           1 |
| `["missing_dot", "equiv"]`                                     |   2.833 μs (5%) |         |   16 bytes (1%) |           1 |
| `["missing_dot", "man"]`                                       |   1.460 μs (5%) |         |   16 bytes (1%) |           1 |
| `["missing_dot", "naive"]`                                     |   2.611 μs (5%) |         |   16 bytes (1%) |           1 |
| `["missing_dot", "rf"]`                                        |   1.470 μs (5%) |         |   16 bytes (1%) |           1 |
| `["missing_dot", "rf_nota"]`                                   |   2.856 μs (5%) |         |   16 bytes (1%) |           1 |
| `["missing_dot", "xf"]`                                        | 112.304 μs (5%) |         |  72.11 KiB (1%) |        3741 |
| `["missing_dot", "xf_nota"]`                                   | 113.104 μs (5%) |         |  72.19 KiB (1%) |        3742 |
| `["overhead", "foldl"]`                                        |   4.400 ns (5%) |         |                 |             |
| `["overhead", "reduce_basecase"]`                              | 118.473 ns (5%) |         |   16 bytes (1%) |           1 |
| `["partition_by", "man"]`                                      |   2.644 ms (5%) |         |  480 bytes (1%) |           3 |
| `["partition_by", "xf"]`                                       |   2.894 ms (5%) |         |  592 bytes (1%) |           5 |
| `["set", "base"]`                                              |   4.921 ms (5%) |         |  49.14 KiB (1%) |          17 |
| `["set", "xf"]`                                                |   4.905 ms (5%) |         |  49.17 KiB (1%) |          19 |
| `["sum_transpose", "30", "noinit", "iter"]`                    |   2.111 μs (5%) |         |                 |             |
| `["sum_transpose", "30", "noinit", "man"]`                     |   1.840 μs (5%) |         |                 |             |
| `["sum_transpose", "30", "noinit", "xf"]`                      | 970.833 ns (5%) |         |                 |             |
| `["sum_transpose", "30", "withinit", "iter"]`                  |   1.510 μs (5%) |         |                 |             |
| `["sum_transpose", "30", "withinit", "man"]`                   | 970.033 ns (5%) |         |                 |             |
| `["sum_transpose", "30", "withinit", "xf"]`                    | 969.565 ns (5%) |         |                 |             |
| `["teerf_filter", "noinit"]`                                   | 479.508 ns (5%) |         |   80 bytes (1%) |           3 |
| `["teerf_filter", "withinit"]`                                 | 276.480 ns (5%) |         |                 |             |

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
      Ubuntu 22.04.3 LTS
  uname: Linux 6.2.0-1015-azure #15~22.04.1-Ubuntu SMP Fri Oct  6 13:20:44 UTC 2023 x86_64 x86_64
  CPU: Intel(R) Xeon(R) CPU E5-2673 v3 @ 2.40GHz: 
              speed         user         nice          sys         idle          irq
       #1  2397 MHz       8610 s          0 s        272 s       4218 s          0 s
       #2  2397 MHz       2843 s          0 s        322 s       9896 s          0 s
       
  Memory: 6.7597503662109375 GB (3485.97265625 MB free)
  Uptime: 1322.17 sec
  Load Avg:  1.0  1.06  0.84
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-12.0.1 (ORCJIT, haswell)
```

---
# Runtime information
| Runtime Info | |
|:--|:--|
| BLAS #threads | 2 |
| `BLAS.vendor()` | `openblas64` |
| `Sys.CPU_THREADS` | 2 |

`lscpu` output:

    Architecture:                       x86_64
    CPU op-mode(s):                     32-bit, 64-bit
    Address sizes:                      46 bits physical, 48 bits virtual
    Byte Order:                         Little Endian
    CPU(s):                             2
    On-line CPU(s) list:                0,1
    Vendor ID:                          GenuineIntel
    Model name:                         Intel(R) Xeon(R) CPU E5-2673 v3 @ 2.40GHz
    CPU family:                         6
    Model:                              63
    Thread(s) per core:                 1
    Core(s) per socket:                 2
    Socket(s):                          1
    Stepping:                           2
    BogoMIPS:                           4794.44
    Flags:                              fpu vme de pse tsc msr pae mce cx8 apic sep mtrr pge mca cmov pat pse36 clflush mmx fxsr sse sse2 ss ht syscall nx pdpe1gb rdtscp lm constant_tsc rep_good nopl xtopology cpuid pni pclmulqdq ssse3 fma cx16 pcid sse4_1 sse4_2 movbe popcnt aes xsave avx f16c rdrand hypervisor lahf_lm abm invpcid_single pti fsgsbase bmi1 avx2 smep bmi2 erms invpcid xsaveopt md_clear
    Hypervisor vendor:                  Microsoft
    Virtualization type:                full
    L1d cache:                          64 KiB (2 instances)
    L1i cache:                          64 KiB (2 instances)
    L2 cache:                           512 KiB (2 instances)
    L3 cache:                           30 MiB (1 instance)
    NUMA node(s):                       1
    NUMA node0 CPU(s):                  0,1
    Vulnerability Gather data sampling: Not affected
    Vulnerability Itlb multihit:        KVM: Mitigation: VMX unsupported
    Vulnerability L1tf:                 Mitigation; PTE Inversion
    Vulnerability Mds:                  Mitigation; Clear CPU buffers; SMT Host state unknown
    Vulnerability Meltdown:             Mitigation; PTI
    Vulnerability Mmio stale data:      Vulnerable: Clear CPU buffers attempted, no microcode; SMT Host state unknown
    Vulnerability Retbleed:             Not affected
    Vulnerability Spec rstack overflow: Not affected
    Vulnerability Spec store bypass:    Vulnerable
    Vulnerability Spectre v1:           Mitigation; usercopy/swapgs barriers and __user pointer sanitization
    Vulnerability Spectre v2:           Mitigation; Retpolines, STIBP disabled, RSB filling, PBRSB-eIBRS Not affected
    Vulnerability Srbds:                Not affected
    Vulnerability Tsx async abort:      Not affected
    

| Cpu Property       | Value                                                   |
|:------------------ |:------------------------------------------------------- |
| Brand              | Intel(R) Xeon(R) CPU E5-2673 v3 @ 2.40GHz               |
| Vendor             | :Intel                                                  |
| Architecture       | :Haswell                                                |
| Model              | Family: 0x06, Model: 0x3f, Stepping: 0x02, Type: 0x00   |
| Cores              | 2 physical cores, 2 logical cores (on executing CPU)    |
|                    | No Hyperthreading hardware capability detected          |
| Clock Frequencies  | Not supported by CPU                                    |
| Data Cache         | Level 1:3 : (32, 256, 30720) kbytes                     |
|                    | 64 byte cache line size                                 |
| Address Size       | 48 bits virtual, 46 bits physical                       |
| SIMD               | 256 bit = 32 byte max. SIMD vector size                 |
| Time Stamp Counter | TSC is accessible via `rdtsc`                           |
|                    | TSC increased at every clock cycle (non-invariant TSC)  |
| Perf. Monitoring   | Performance Monitoring Counters (PMC) are not supported |
| Hypervisor         | Yes, Microsoft                                          |

