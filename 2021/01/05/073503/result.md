# Benchmark result

* Pull request commit: [`2b5bae82abc8490b6a7133a3db394966c395db5e`](https://github.com/JuliaFolds/Transducers.jl/commit/2b5bae82abc8490b6a7133a3db394966c395db5e)
* Pull request: <https://github.com/JuliaFolds/Transducers.jl/pull/439> (Move executors from FLoops to Transducers)

# Judge result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmarks:
    - Target: 5 Jan 2021 - 07:29
    - Baseline: 5 Jan 2021 - 07:34
* Package commits:
    - Target: 1f9347
    - Baseline: ff76d1
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

| ID                                                             | time ratio                   | memory ratio |
|----------------------------------------------------------------|------------------------------|--------------|
| `["append!!", "eduction"]`                                     | 0.92 (5%) :white_check_mark: |   1.00 (1%)  |
| `["append!!", "xf"]`                                           | 0.89 (5%) :white_check_mark: |   1.00 (1%)  |
| `["cartesian", "copyto!", "iter"]`                             | 0.76 (5%) :white_check_mark: |   1.00 (1%)  |
| `["cartesian", "copyto!", "man"]`                              | 0.48 (5%) :white_check_mark: |   1.00 (1%)  |
| `["cartesian", "copyto!", "xf"]`                               | 0.70 (5%) :white_check_mark: |   1.00 (1%)  |
| `["collect", "filter-missing"]`                                | 0.89 (5%) :white_check_mark: |   1.00 (1%)  |
| `["collect", "identity-float"]`                                | 0.93 (5%) :white_check_mark: |   1.00 (1%)  |
| `["collect", "identity-union"]`                                | 0.86 (5%) :white_check_mark: |   1.00 (1%)  |
| `["dict", "base"]`                                             | 0.81 (5%) :white_check_mark: |   1.00 (1%)  |
| `["dict", "xf"]`                                               | 0.84 (5%) :white_check_mark: |   1.00 (1%)  |
| `["dot", "blas"]`                                              | 0.89 (5%) :white_check_mark: |   1.00 (1%)  |
| `["dot", "man"]`                                               | 0.76 (5%) :white_check_mark: |   1.00 (1%)  |
| `["dot", "xf"]`                                                | 0.76 (5%) :white_check_mark: |   1.00 (1%)  |
| `["filter_map_map!", "xf"]`                                    | 0.88 (5%) :white_check_mark: |   1.00 (1%)  |
| `["filter_map_reduce", "man"]`                                 | 0.86 (5%) :white_check_mark: |   1.00 (1%)  |
| `["filter_map_reduce", "xf"]`                                  | 0.86 (5%) :white_check_mark: |   1.00 (1%)  |
| `["filter_sum", "1000", "RandomFloats", "noinit", "naive"]`    | 0.88 (5%) :white_check_mark: |   1.00 (1%)  |
| `["filter_sum", "1000", "RandomFloats", "noinit", "xf"]`       | 0.86 (5%) :white_check_mark: |   1.00 (1%)  |
| `["filter_sum", "1000", "RandomFloats", "withinit", "base"]`   | 0.87 (5%) :white_check_mark: |   1.00 (1%)  |
| `["filter_sum", "1000", "RandomFloats", "withinit", "naive"]`  | 0.94 (5%) :white_check_mark: |   1.00 (1%)  |
| `["filter_sum", "1000", "RandomFloats", "withinit", "xf"]`     | 0.86 (5%) :white_check_mark: |   1.00 (1%)  |
| `["filter_sum", "1000", "UnitRange", "noinit", "base"]`        | 0.86 (5%) :white_check_mark: |   1.00 (1%)  |
| `["filter_sum", "1000", "UnitRange", "noinit", "naive"]`       | 0.86 (5%) :white_check_mark: |   1.00 (1%)  |
| `["filter_sum", "1000", "UnitRange", "withinit", "base"]`      | 0.86 (5%) :white_check_mark: |   1.00 (1%)  |
| `["filter_sum", "1000", "UnitRange", "withinit", "naive"]`     | 0.70 (5%) :white_check_mark: |   1.00 (1%)  |
| `["filter_sum", "1000", "UnitRange", "withinit", "xf"]`        | 0.87 (5%) :white_check_mark: |   1.00 (1%)  |
| `["filter_sum", "10000", "RandomFloats", "noinit", "base"]`    | 0.85 (5%) :white_check_mark: |   1.00 (1%)  |
| `["filter_sum", "10000", "RandomFloats", "noinit", "naive"]`   | 0.78 (5%) :white_check_mark: |   1.00 (1%)  |
| `["filter_sum", "10000", "RandomFloats", "withinit", "base"]`  | 0.86 (5%) :white_check_mark: |   1.00 (1%)  |
| `["filter_sum", "10000", "RandomFloats", "withinit", "xf"]`    | 0.86 (5%) :white_check_mark: |   1.00 (1%)  |
| `["filter_sum", "10000", "UnitRange", "noinit", "naive"]`      | 0.87 (5%) :white_check_mark: |   1.00 (1%)  |
| `["filter_sum", "10000", "UnitRange", "noinit", "xf"]`         | 0.87 (5%) :white_check_mark: |   1.00 (1%)  |
| `["filter_sum", "10000", "UnitRange", "withinit", "naive"]`    | 0.80 (5%) :white_check_mark: |   1.00 (1%)  |
| `["filter_sum", "10000", "UnitRange", "withinit", "xf"]`       | 0.86 (5%) :white_check_mark: |   1.00 (1%)  |
| `["findall", "xf-array"]`                                      | 0.86 (5%) :white_check_mark: |   1.00 (1%)  |
| `["gemm", "fusedmul", "blas", "2"]`                            | 0.88 (5%) :white_check_mark: |   1.00 (1%)  |
| `["gemm", "fusedmul", "blas", "32"]`                           | 0.88 (5%) :white_check_mark: |   1.00 (1%)  |
| `["gemm", "fusedmul", "blas", "8"]`                            | 0.89 (5%) :white_check_mark: |   1.00 (1%)  |
| `["gemm", "mul", "linalg", "32"]`                              | 0.89 (5%) :white_check_mark: |   1.00 (1%)  |
| `["gemm", "mul", "linalg", "8"]`                               | 0.88 (5%) :white_check_mark: |   1.00 (1%)  |
| `["gemm", "mul", "man", "ivdep", "32"]`                        | 0.89 (5%) :white_check_mark: |   1.00 (1%)  |
| `["gemm", "mul", "man", "ivdep", "8"]`                         |                1.15 (5%) :x: |   1.00 (1%)  |
| `["gemm", "mul", "man", "true", "32"]`                         | 0.92 (5%) :white_check_mark: |   1.00 (1%)  |
| `["gemm", "mul", "man", "true", "8"]`                          | 0.74 (5%) :white_check_mark: |   1.00 (1%)  |
| `["gemm", "mul", "xf", "false", "32"]`                         |                1.07 (5%) :x: |   1.00 (1%)  |
| `["gemm", "mul", "xf", "false", "8"]`                          | 0.85 (5%) :white_check_mark: |   1.00 (1%)  |
| `["gemm", "mul", "xf", "ivdep", "256"]`                        | 0.88 (5%) :white_check_mark: |   1.00 (1%)  |
| `["gemm", "mul", "xf", "true", "256"]`                         | 0.91 (5%) :white_check_mark: |   1.00 (1%)  |
| `["gemm", "mul", "xf", "true", "8"]`                           | 0.73 (5%) :white_check_mark: |   1.00 (1%)  |
| `["groupby", "sum", "sac"]`                                    | 0.86 (5%) :white_check_mark: |   1.00 (1%)  |
| `["groupby", "sum", "xf-without-init"]`                        | 0.94 (5%) :white_check_mark: |   1.00 (1%)  |
| `["mapcat_eduction", "xf-eduction"]`                           |                1.20 (5%) :x: |   1.00 (1%)  |
| `["mapcat_eduction", "xf-xf"]`                                 |                1.16 (5%) :x: |   1.00 (1%)  |
| `["missing_argmax", "man"]`                                    | 0.86 (5%) :white_check_mark: |   1.00 (1%)  |
| `["missing_argmax", "rf"]`                                     | 0.83 (5%) :white_check_mark: |   1.00 (1%)  |
| `["missing_dot", "naive"]`                                     | 0.87 (5%) :white_check_mark: |   1.00 (1%)  |
| `["missing_dot", "rf"]`                                        | 0.93 (5%) :white_check_mark: |   1.00 (1%)  |
| `["missing_dot", "rf_nota"]`                                   | 0.84 (5%) :white_check_mark: |   1.00 (1%)  |
| `["missing_dot", "xf"]`                                        | 0.88 (5%) :white_check_mark: |   1.00 (1%)  |
| `["missing_dot", "xf_nota"]`                                   | 0.85 (5%) :white_check_mark: |   1.00 (1%)  |
| `["overhead", "foldl"]`                                        | 0.93 (5%) :white_check_mark: |   1.00 (1%)  |
| `["overhead", "reduce_basecase"]`                              | 0.84 (5%) :white_check_mark: |   1.00 (1%)  |
| `["partition_by", "man"]`                                      | 0.81 (5%) :white_check_mark: |   1.00 (1%)  |
| `["partition_by", "xf"]`                                       | 0.85 (5%) :white_check_mark: |   1.00 (1%)  |
| `["set", "xf"]`                                                |                1.07 (5%) :x: |   1.00 (1%)  |
| `["sum_transpose", "30", "noinit", "iter"]`                    | 0.86 (5%) :white_check_mark: |   1.00 (1%)  |
| `["sum_transpose", "30", "noinit", "man"]`                     | 0.86 (5%) :white_check_mark: |   1.00 (1%)  |
| `["sum_transpose", "30", "noinit", "xf"]`                      | 0.75 (5%) :white_check_mark: |   1.00 (1%)  |
| `["sum_transpose", "30", "withinit", "iter"]`                  | 0.87 (5%) :white_check_mark: |   1.00 (1%)  |
| `["sum_transpose", "30", "withinit", "man"]`                   | 0.75 (5%) :white_check_mark: |   1.00 (1%)  |
| `["sum_transpose", "30", "withinit", "xf"]`                    | 0.86 (5%) :white_check_mark: |   1.00 (1%)  |
| `["teerf_filter", "withinit"]`                                 | 0.86 (5%) :white_check_mark: |   1.00 (1%)  |

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
  uname: Linux 5.4.0-1032-azure #33~18.04.1-Ubuntu SMP Tue Nov 17 11:40:52 UTC 2020 x86_64 x86_64
  CPU: Intel(R) Xeon(R) Platinum 8171M CPU @ 2.60GHz: 
              speed         user         nice          sys         idle          irq
       #1  2095 MHz      14944 s          0 s       1450 s      64486 s          0 s
       #2  2095 MHz      61979 s          0 s       1508 s      17426 s          0 s
       
  Memory: 6.7913970947265625 GB (3557.2890625 MB free)
  Uptime: 822.0 sec
  Load Avg:  1.1064453125  1.03857421875  0.6767578125
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
  uname: Linux 5.4.0-1032-azure #33~18.04.1-Ubuntu SMP Tue Nov 17 11:40:52 UTC 2020 x86_64 x86_64
  CPU: Intel(R) Xeon(R) Platinum 8171M CPU @ 2.60GHz: 
              speed         user         nice          sys         idle          irq
       #1  2095 MHz      29634 s          0 s       1604 s      79454 s          0 s
       #2  2095 MHz      77052 s          0 s       1647 s      32013 s          0 s
       
  Memory: 6.7913970947265625 GB (3555.40625 MB free)
  Uptime: 1121.0 sec
  Load Avg:  1.0  1.00439453125  0.77734375
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-9.0.1 (ORCJIT, skylake-avx512)
```

---
# Target result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmark: 5 Jan 2021 - 7:29
* Package commit: 1f9347
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
| `["append!!", "eduction"]`                                     |  18.302 μs (5%) |         |  64.63 KiB (1%) |          13 |
| `["append!!", "xf"]`                                           |  18.701 μs (5%) |         |  64.63 KiB (1%) |          13 |
| `["cartesian", "copyto!", "iter"]`                             |   5.034 μs (5%) |         |                 |             |
| `["cartesian", "copyto!", "man"]`                              |   1.780 μs (5%) |         |                 |             |
| `["cartesian", "copyto!", "xf"]`                               |   2.334 μs (5%) |         |                 |             |
| `["cat", "base"]`                                              |   2.600 μs (5%) |         |                 |             |
| `["cat", "xf"]`                                                |   1.610 μs (5%) |         |                 |             |
| `["collect", "filter-missing"]`                                |  55.704 μs (5%) |         |  32.81 KiB (1%) |          14 |
| `["collect", "identity-float"]`                                |  26.302 μs (5%) |         | 256.66 KiB (1%) |          14 |
| `["collect", "identity-union"]`                                | 127.409 μs (5%) |         | 601.04 KiB (1%) |       10013 |
| `["dict", "base"]`                                             |   3.561 ms (5%) |         |  92.91 KiB (1%) |          22 |
| `["dict", "xf"]`                                               |   3.554 ms (5%) |         |  92.31 KiB (1%) |          18 |
| `["dot", "blas"]`                                              |   1.030 μs (5%) |         |                 |             |
| `["dot", "man"]`                                               | 990.100 ns (5%) |         |                 |             |
| `["dot", "rf"]`                                                |   1.810 μs (5%) |         |                 |             |
| `["dot", "xf"]`                                                |   1.870 μs (5%) |         |   64 bytes (1%) |           3 |
| `["filter_map_map!", "man"]`                                   |  59.703 μs (5%) |         |                 |             |
| `["filter_map_map!", "xf"]`                                    | 603.233 μs (5%) |         |   80 bytes (1%) |           3 |
| `["filter_map_reduce", "man"]`                                 | 191.713 μs (5%) |         |                 |             |
| `["filter_map_reduce", "xf"]`                                  | 191.714 μs (5%) |         |                 |             |
| `["filter_sum", "1000", "RandomFloats", "noinit", "base"]`     |   1.240 μs (5%) |         |                 |             |
| `["filter_sum", "1000", "RandomFloats", "noinit", "naive"]`    |   1.250 μs (5%) |         |                 |             |
| `["filter_sum", "1000", "RandomFloats", "noinit", "xf"]`       |   1.490 μs (5%) |         |                 |             |
| `["filter_sum", "1000", "RandomFloats", "withinit", "base"]`   |   1.480 μs (5%) |         |                 |             |
| `["filter_sum", "1000", "RandomFloats", "withinit", "naive"]`  | 758.622 ns (5%) |         |                 |             |
| `["filter_sum", "1000", "RandomFloats", "withinit", "xf"]`     |   1.700 μs (5%) |         |                 |             |
| `["filter_sum", "1000", "UnitRange", "noinit", "base"]`        |   1.510 μs (5%) |         |                 |             |
| `["filter_sum", "1000", "UnitRange", "noinit", "naive"]`       | 846.415 ns (5%) |         |                 |             |
| `["filter_sum", "1000", "UnitRange", "noinit", "xf"]`          | 117.573 ns (5%) |         |                 |             |
| `["filter_sum", "1000", "UnitRange", "withinit", "base"]`      |  87.862 ns (5%) |         |                 |             |
| `["filter_sum", "1000", "UnitRange", "withinit", "naive"]`     | 619.387 ns (5%) |         |                 |             |
| `["filter_sum", "1000", "UnitRange", "withinit", "xf"]`        | 106.342 ns (5%) |         |                 |             |
| `["filter_sum", "10000", "RandomFloats", "noinit", "base"]`    |  35.203 μs (5%) |         |                 |             |
| `["filter_sum", "10000", "RandomFloats", "noinit", "naive"]`   |  45.904 μs (5%) |         |                 |             |
| `["filter_sum", "10000", "RandomFloats", "noinit", "xf"]`      |  17.501 μs (5%) |         |                 |             |
| `["filter_sum", "10000", "RandomFloats", "withinit", "base"]`  |  15.001 μs (5%) |         |                 |             |
| `["filter_sum", "10000", "RandomFloats", "withinit", "naive"]` |  42.203 μs (5%) |         |                 |             |
| `["filter_sum", "10000", "RandomFloats", "withinit", "xf"]`    |  15.101 μs (5%) |         |                 |             |
| `["filter_sum", "10000", "UnitRange", "noinit", "base"]`       |  17.501 μs (5%) |         |                 |             |
| `["filter_sum", "10000", "UnitRange", "noinit", "naive"]`      |   9.700 μs (5%) |         |                 |             |
| `["filter_sum", "10000", "UnitRange", "noinit", "xf"]`         |   1.127 μs (5%) |         |                 |             |
| `["filter_sum", "10000", "UnitRange", "withinit", "base"]`     | 964.932 ns (5%) |         |                 |             |
| `["filter_sum", "10000", "UnitRange", "withinit", "naive"]`    |   7.020 μs (5%) |         |                 |             |
| `["filter_sum", "10000", "UnitRange", "withinit", "xf"]`       | 975.063 ns (5%) |         |                 |             |
| `["findall", "base"]`                                          | 802.458 μs (5%) |         |   2.00 MiB (1%) |          18 |
| `["findall", "xf-array"]`                                      | 622.645 μs (5%) |         |   3.02 MiB (1%) |       98829 |
| `["findall", "xf-iter"]`                                       | 325.323 μs (5%) |         |   2.00 MiB (1%) |          19 |
| `["gemm", "fusedmul", "blas", "16"]`                           |   3.163 ms (5%) |         |                 |             |
| `["gemm", "fusedmul", "blas", "2"]`                            |   2.441 ms (5%) |         |                 |             |
| `["gemm", "fusedmul", "blas", "32"]`                           |   3.720 ms (5%) |         |                 |             |
| `["gemm", "fusedmul", "blas", "8"]`                            |   2.776 ms (5%) |         |                 |             |
| `["gemm", "fusedmul", "xf", "16"]`                             |   5.775 ms (5%) |         |  192 bytes (1%) |           4 |
| `["gemm", "fusedmul", "xf", "2"]`                              | 689.939 μs (5%) |         |  192 bytes (1%) |           4 |
| `["gemm", "fusedmul", "xf", "32"]`                             |  11.497 ms (5%) |         |  192 bytes (1%) |           4 |
| `["gemm", "fusedmul", "xf", "8"]`                              |   2.770 ms (5%) |         |  192 bytes (1%) |           4 |
| `["gemm", "mul", "linalg", "256"]`                             | 435.229 μs (5%) |         |                 |             |
| `["gemm", "mul", "linalg", "32"]`                              |   1.780 μs (5%) |         |                 |             |
| `["gemm", "mul", "linalg", "8"]`                               | 176.846 ns (5%) |         |                 |             |
| `["gemm", "mul", "man", "false", "256"]`                       |   1.579 ms (5%) |         |                 |             |
| `["gemm", "mul", "man", "false", "32"]`                        |   4.900 μs (5%) |         |                 |             |
| `["gemm", "mul", "man", "false", "8"]`                         | 390.068 ns (5%) |         |                 |             |
| `["gemm", "mul", "man", "ivdep", "256"]`                       |   1.583 ms (5%) |         |                 |             |
| `["gemm", "mul", "man", "ivdep", "32"]`                        |   3.550 μs (5%) |         |                 |             |
| `["gemm", "mul", "man", "ivdep", "8"]`                         | 458.736 ns (5%) |         |                 |             |
| `["gemm", "mul", "man", "true", "256"]`                        |   1.545 ms (5%) |         |                 |             |
| `["gemm", "mul", "man", "true", "32"]`                         |   4.700 μs (5%) |         |                 |             |
| `["gemm", "mul", "man", "true", "8"]`                          | 369.252 ns (5%) |         |                 |             |
| `["gemm", "mul", "xf", "false", "256"]`                        |   1.603 ms (5%) |         |   80 bytes (1%) |           3 |
| `["gemm", "mul", "xf", "false", "32"]`                         |   4.815 μs (5%) |         |   80 bytes (1%) |           3 |
| `["gemm", "mul", "xf", "false", "8"]`                          | 424.063 ns (5%) |         |   80 bytes (1%) |           3 |
| `["gemm", "mul", "xf", "ivdep", "256"]`                        |   1.378 ms (5%) |         |   80 bytes (1%) |           3 |
| `["gemm", "mul", "xf", "ivdep", "32"]`                         |   3.600 μs (5%) |         |   80 bytes (1%) |           3 |
| `["gemm", "mul", "xf", "ivdep", "8"]`                          | 406.429 ns (5%) |         |   80 bytes (1%) |           3 |
| `["gemm", "mul", "xf", "true", "256"]`                         |   1.399 ms (5%) |         |   80 bytes (1%) |           3 |
| `["gemm", "mul", "xf", "true", "32"]`                          |   4.986 μs (5%) |         |   80 bytes (1%) |           3 |
| `["gemm", "mul", "xf", "true", "8"]`                           | 366.526 ns (5%) |         |   80 bytes (1%) |           3 |
| `["groupby", "sum", "sac"]`                                    | 169.909 μs (5%) |         |  624 bytes (1%) |           5 |
| `["groupby", "sum", "xf-with-init"]`                           | 157.109 μs (5%) |         |   1.20 KiB (1%) |           9 |
| `["groupby", "sum", "xf-without-init"]`                        | 153.608 μs (5%) |         |   1.20 KiB (1%) |           9 |
| `["mapcat_eduction", "base"]`                                  |   1.830 μs (5%) |         |                 |             |
| `["mapcat_eduction", "xf-eduction"]`                           |   1.930 μs (5%) |         |                 |             |
| `["mapcat_eduction", "xf-xf"]`                                 |   1.870 μs (5%) |         |                 |             |
| `["missing_argmax", "man"]`                                    |   2.233 μs (5%) |         |   32 bytes (1%) |           1 |
| `["missing_argmax", "rf"]`                                     |   1.520 μs (5%) |         |   32 bytes (1%) |           1 |
| `["missing_argmax", "xf"]`                                     |   1.680 μs (5%) |         |   32 bytes (1%) |           1 |
| `["missing_dot", "equiv"]`                                     |   1.530 μs (5%) |         |   16 bytes (1%) |           1 |
| `["missing_dot", "man"]`                                       |   1.370 μs (5%) |         |   16 bytes (1%) |           1 |
| `["missing_dot", "naive"]`                                     |   4.143 μs (5%) |         |   16 bytes (1%) |           1 |
| `["missing_dot", "rf"]`                                        |   1.260 μs (5%) |         |   16 bytes (1%) |           1 |
| `["missing_dot", "rf_nota"]`                                   |   1.170 μs (5%) |         |   16 bytes (1%) |           1 |
| `["missing_dot", "xf"]`                                        |  84.906 μs (5%) |         |  72.19 KiB (1%) |        3746 |
| `["missing_dot", "xf_nota"]`                                   |  82.205 μs (5%) |         |  72.03 KiB (1%) |        3736 |
| `["overhead", "foldl"]`                                        |   4.200 ns (5%) |         |                 |             |
| `["overhead", "reduce_basecase"]`                              | 209.770 ns (5%) |         |  368 bytes (1%) |           6 |
| `["partition_by", "man"]`                                      |   1.861 ms (5%) |         |  352 bytes (1%) |           4 |
| `["partition_by", "xf"]`                                       |   1.849 ms (5%) |         |  544 bytes (1%) |           6 |
| `["set", "base"]`                                              |   4.708 ms (5%) |         |  49.56 KiB (1%) |          17 |
| `["set", "xf"]`                                                |   5.034 ms (5%) |         |  49.59 KiB (1%) |          19 |
| `["sum_transpose", "30", "noinit", "iter"]`                    |   1.880 μs (5%) |         |                 |             |
| `["sum_transpose", "30", "noinit", "man"]`                     |   2.122 μs (5%) |         |                 |             |
| `["sum_transpose", "30", "noinit", "xf"]`                      |   1.060 μs (5%) |         |   32 bytes (1%) |           2 |
| `["sum_transpose", "30", "withinit", "iter"]`                  |   1.480 μs (5%) |         |                 |             |
| `["sum_transpose", "30", "withinit", "man"]`                   | 959.136 ns (5%) |         |                 |             |
| `["sum_transpose", "30", "withinit", "xf"]`                    |   1.020 μs (5%) |         |   48 bytes (1%) |           3 |
| `["teerf_filter", "noinit"]`                                   |   2.110 μs (5%) |         |  160 bytes (1%) |           7 |
| `["teerf_filter", "withinit"]`                                 | 163.897 ns (5%) |         |                 |             |

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
  uname: Linux 5.4.0-1032-azure #33~18.04.1-Ubuntu SMP Tue Nov 17 11:40:52 UTC 2020 x86_64 x86_64
  CPU: Intel(R) Xeon(R) Platinum 8171M CPU @ 2.60GHz: 
              speed         user         nice          sys         idle          irq
       #1  2095 MHz      14944 s          0 s       1450 s      64486 s          0 s
       #2  2095 MHz      61979 s          0 s       1508 s      17426 s          0 s
       
  Memory: 6.7913970947265625 GB (3557.2890625 MB free)
  Uptime: 822.0 sec
  Load Avg:  1.1064453125  1.03857421875  0.6767578125
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-9.0.1 (ORCJIT, skylake-avx512)
```

---
# Baseline result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmark: 5 Jan 2021 - 7:34
* Package commit: ff76d1
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
| `["append!!", "eduction"]`                                     |  19.902 μs (5%) |         |  64.63 KiB (1%) |          13 |
| `["append!!", "xf"]`                                           |  20.902 μs (5%) |         |  64.63 KiB (1%) |          13 |
| `["cartesian", "copyto!", "iter"]`                             |   6.584 μs (5%) |         |                 |             |
| `["cartesian", "copyto!", "man"]`                              |   3.740 μs (5%) |         |                 |             |
| `["cartesian", "copyto!", "xf"]`                               |   3.356 μs (5%) |         |                 |             |
| `["cat", "base"]`                                              |   2.589 μs (5%) |         |                 |             |
| `["cat", "xf"]`                                                |   1.610 μs (5%) |         |                 |             |
| `["collect", "filter-missing"]`                                |  62.603 μs (5%) |         |  32.81 KiB (1%) |          14 |
| `["collect", "identity-float"]`                                |  28.202 μs (5%) |         | 256.66 KiB (1%) |          14 |
| `["collect", "identity-union"]`                                | 148.808 μs (5%) |         | 601.13 KiB (1%) |       10013 |
| `["dict", "base"]`                                             |   4.372 ms (5%) |         |  92.91 KiB (1%) |          22 |
| `["dict", "xf"]`                                               |   4.231 ms (5%) |         |  92.31 KiB (1%) |          18 |
| `["dot", "blas"]`                                              |   1.160 μs (5%) |         |                 |             |
| `["dot", "man"]`                                               |   1.310 μs (5%) |         |                 |             |
| `["dot", "rf"]`                                                |   1.830 μs (5%) |         |                 |             |
| `["dot", "xf"]`                                                |   2.460 μs (5%) |         |   64 bytes (1%) |           3 |
| `["filter_map_map!", "man"]`                                   |  57.606 μs (5%) |         |                 |             |
| `["filter_map_map!", "xf"]`                                    | 688.970 μs (5%) |         |   80 bytes (1%) |           3 |
| `["filter_map_reduce", "man"]`                                 | 222.511 μs (5%) |         |                 |             |
| `["filter_map_reduce", "xf"]`                                  | 222.611 μs (5%) |         |                 |             |
| `["filter_sum", "1000", "RandomFloats", "noinit", "base"]`     |   1.240 μs (5%) |         |                 |             |
| `["filter_sum", "1000", "RandomFloats", "noinit", "naive"]`    |   1.420 μs (5%) |         |                 |             |
| `["filter_sum", "1000", "RandomFloats", "noinit", "xf"]`       |   1.730 μs (5%) |         |                 |             |
| `["filter_sum", "1000", "RandomFloats", "withinit", "base"]`   |   1.710 μs (5%) |         |                 |             |
| `["filter_sum", "1000", "RandomFloats", "withinit", "naive"]`  | 809.045 ns (5%) |         |                 |             |
| `["filter_sum", "1000", "RandomFloats", "withinit", "xf"]`     |   1.980 μs (5%) |         |                 |             |
| `["filter_sum", "1000", "UnitRange", "noinit", "base"]`        |   1.750 μs (5%) |         |                 |             |
| `["filter_sum", "1000", "UnitRange", "noinit", "naive"]`       | 987.854 ns (5%) |         |                 |             |
| `["filter_sum", "1000", "UnitRange", "noinit", "xf"]`          | 117.898 ns (5%) |         |                 |             |
| `["filter_sum", "1000", "UnitRange", "withinit", "base"]`      | 102.741 ns (5%) |         |                 |             |
| `["filter_sum", "1000", "UnitRange", "withinit", "naive"]`     | 884.047 ns (5%) |         |                 |             |
| `["filter_sum", "1000", "UnitRange", "withinit", "xf"]`        | 122.672 ns (5%) |         |                 |             |
| `["filter_sum", "10000", "RandomFloats", "noinit", "base"]`    |  41.502 μs (5%) |         |                 |             |
| `["filter_sum", "10000", "RandomFloats", "noinit", "naive"]`   |  58.903 μs (5%) |         |                 |             |
| `["filter_sum", "10000", "RandomFloats", "noinit", "xf"]`      |  17.500 μs (5%) |         |                 |             |
| `["filter_sum", "10000", "RandomFloats", "withinit", "base"]`  |  17.500 μs (5%) |         |                 |             |
| `["filter_sum", "10000", "RandomFloats", "withinit", "naive"]` |  43.302 μs (5%) |         |                 |             |
| `["filter_sum", "10000", "RandomFloats", "withinit", "xf"]`    |  17.500 μs (5%) |         |                 |             |
| `["filter_sum", "10000", "UnitRange", "noinit", "base"]`       |  17.601 μs (5%) |         |                 |             |
| `["filter_sum", "10000", "UnitRange", "noinit", "naive"]`      |  11.100 μs (5%) |         |                 |             |
| `["filter_sum", "10000", "UnitRange", "noinit", "xf"]`         |   1.300 μs (5%) |         |                 |             |
| `["filter_sum", "10000", "UnitRange", "withinit", "base"]`     | 973.027 ns (5%) |         |                 |             |
| `["filter_sum", "10000", "UnitRange", "withinit", "naive"]`    |   8.760 μs (5%) |         |                 |             |
| `["filter_sum", "10000", "UnitRange", "withinit", "xf"]`       |   1.137 μs (5%) |         |                 |             |
| `["findall", "base"]`                                          | 815.042 μs (5%) |         |   2.00 MiB (1%) |          18 |
| `["findall", "xf-array"]`                                      | 720.537 μs (5%) |         |   3.02 MiB (1%) |       98829 |
| `["findall", "xf-iter"]`                                       | 339.717 μs (5%) |         |   2.00 MiB (1%) |          19 |
| `["gemm", "fusedmul", "blas", "16"]`                           |   3.326 ms (5%) |         |                 |             |
| `["gemm", "fusedmul", "blas", "2"]`                            |   2.782 ms (5%) |         |                 |             |
| `["gemm", "fusedmul", "blas", "32"]`                           |   4.209 ms (5%) |         |                 |             |
| `["gemm", "fusedmul", "blas", "8"]`                            |   3.118 ms (5%) |         |                 |             |
| `["gemm", "fusedmul", "xf", "16"]`                             |   5.656 ms (5%) |         |  192 bytes (1%) |           4 |
| `["gemm", "fusedmul", "xf", "2"]`                              | 691.773 μs (5%) |         |  192 bytes (1%) |           4 |
| `["gemm", "fusedmul", "xf", "32"]`                             |  11.300 ms (5%) |         |  192 bytes (1%) |           4 |
| `["gemm", "fusedmul", "xf", "8"]`                              |   2.831 ms (5%) |         |  192 bytes (1%) |           4 |
| `["gemm", "mul", "linalg", "256"]`                             | 454.657 μs (5%) |         |                 |             |
| `["gemm", "mul", "linalg", "32"]`                              |   2.000 μs (5%) |         |                 |             |
| `["gemm", "mul", "linalg", "8"]`                               | 200.000 ns (5%) |         |                 |             |
| `["gemm", "mul", "man", "false", "256"]`                       |   1.545 ms (5%) |         |                 |             |
| `["gemm", "mul", "man", "false", "32"]`                        |   4.700 μs (5%) |         |                 |             |
| `["gemm", "mul", "man", "false", "8"]`                         | 400.000 ns (5%) |         |                 |             |
| `["gemm", "mul", "man", "ivdep", "256"]`                       |   1.574 ms (5%) |         |                 |             |
| `["gemm", "mul", "man", "ivdep", "32"]`                        |   4.000 μs (5%) |         |                 |             |
| `["gemm", "mul", "man", "ivdep", "8"]`                         | 400.000 ns (5%) |         |                 |             |
| `["gemm", "mul", "man", "true", "256"]`                        |   1.554 ms (5%) |         |                 |             |
| `["gemm", "mul", "man", "true", "32"]`                         |   5.100 μs (5%) |         |                 |             |
| `["gemm", "mul", "man", "true", "8"]`                          | 500.000 ns (5%) |         |                 |             |
| `["gemm", "mul", "xf", "false", "256"]`                        |   1.541 ms (5%) |         |   80 bytes (1%) |           3 |
| `["gemm", "mul", "xf", "false", "32"]`                         |   4.500 μs (5%) |         |   80 bytes (1%) |           3 |
| `["gemm", "mul", "xf", "false", "8"]`                          | 500.000 ns (5%) |         |   80 bytes (1%) |           3 |
| `["gemm", "mul", "xf", "ivdep", "256"]`                        |   1.575 ms (5%) |         |   80 bytes (1%) |           3 |
| `["gemm", "mul", "xf", "ivdep", "32"]`                         |   3.600 μs (5%) |         |   80 bytes (1%) |           3 |
| `["gemm", "mul", "xf", "ivdep", "8"]`                          | 400.000 ns (5%) |         |   80 bytes (1%) |           3 |
| `["gemm", "mul", "xf", "true", "256"]`                         |   1.544 ms (5%) |         |   80 bytes (1%) |           3 |
| `["gemm", "mul", "xf", "true", "32"]`                          |   5.200 μs (5%) |         |   80 bytes (1%) |           3 |
| `["gemm", "mul", "xf", "true", "8"]`                           | 500.000 ns (5%) |         |   80 bytes (1%) |           3 |
| `["groupby", "sum", "sac"]`                                    | 196.820 μs (5%) |         |  624 bytes (1%) |           5 |
| `["groupby", "sum", "xf-with-init"]`                           | 161.416 μs (5%) |         |   1.20 KiB (1%) |           9 |
| `["groupby", "sum", "xf-without-init"]`                        | 163.016 μs (5%) |         |   1.20 KiB (1%) |           9 |
| `["mapcat_eduction", "base"]`                                  |   1.820 μs (5%) |         |                 |             |
| `["mapcat_eduction", "xf-eduction"]`                           |   1.610 μs (5%) |         |                 |             |
| `["mapcat_eduction", "xf-xf"]`                                 |   1.610 μs (5%) |         |                 |             |
| `["missing_argmax", "man"]`                                    |   2.600 μs (5%) |         |   32 bytes (1%) |           1 |
| `["missing_argmax", "rf"]`                                     |   1.830 μs (5%) |         |   32 bytes (1%) |           1 |
| `["missing_argmax", "xf"]`                                     |   1.750 μs (5%) |         |   32 bytes (1%) |           1 |
| `["missing_dot", "equiv"]`                                     |   1.530 μs (5%) |         |   16 bytes (1%) |           1 |
| `["missing_dot", "man"]`                                       |   1.350 μs (5%) |         |   16 bytes (1%) |           1 |
| `["missing_dot", "naive"]`                                     |   4.743 μs (5%) |         |   16 bytes (1%) |           1 |
| `["missing_dot", "rf"]`                                        |   1.350 μs (5%) |         |   16 bytes (1%) |           1 |
| `["missing_dot", "rf_nota"]`                                   |   1.390 μs (5%) |         |   16 bytes (1%) |           1 |
| `["missing_dot", "xf"]`                                        |  96.012 μs (5%) |         |  72.14 KiB (1%) |        3742 |
| `["missing_dot", "xf_nota"]`                                   |  96.605 μs (5%) |         |  71.86 KiB (1%) |        3730 |
| `["overhead", "foldl"]`                                        |   4.500 ns (5%) |         |                 |             |
| `["overhead", "reduce_basecase"]`                              | 249.607 ns (5%) |         |  368 bytes (1%) |           6 |
| `["partition_by", "man"]`                                      |   2.305 ms (5%) |         |  352 bytes (1%) |           4 |
| `["partition_by", "xf"]`                                       |   2.182 ms (5%) |         |  544 bytes (1%) |           6 |
| `["set", "base"]`                                              |   4.741 ms (5%) |         |  49.56 KiB (1%) |          17 |
| `["set", "xf"]`                                                |   4.689 ms (5%) |         |  49.59 KiB (1%) |          19 |
| `["sum_transpose", "30", "noinit", "iter"]`                    |   2.190 μs (5%) |         |                 |             |
| `["sum_transpose", "30", "noinit", "man"]`                     |   2.456 μs (5%) |         |                 |             |
| `["sum_transpose", "30", "noinit", "xf"]`                      |   1.410 μs (5%) |         |   32 bytes (1%) |           2 |
| `["sum_transpose", "30", "withinit", "iter"]`                  |   1.700 μs (5%) |         |                 |             |
| `["sum_transpose", "30", "withinit", "man"]`                   |   1.273 μs (5%) |         |                 |             |
| `["sum_transpose", "30", "withinit", "xf"]`                    |   1.190 μs (5%) |         |   48 bytes (1%) |           3 |
| `["teerf_filter", "noinit"]`                                   |   2.110 μs (5%) |         |  160 bytes (1%) |           7 |
| `["teerf_filter", "withinit"]`                                 | 190.752 ns (5%) |         |                 |             |

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
  uname: Linux 5.4.0-1032-azure #33~18.04.1-Ubuntu SMP Tue Nov 17 11:40:52 UTC 2020 x86_64 x86_64
  CPU: Intel(R) Xeon(R) Platinum 8171M CPU @ 2.60GHz: 
              speed         user         nice          sys         idle          irq
       #1  2095 MHz      29634 s          0 s       1604 s      79454 s          0 s
       #2  2095 MHz      77052 s          0 s       1647 s      32013 s          0 s
       
  Memory: 6.7913970947265625 GB (3555.40625 MB free)
  Uptime: 1121.0 sec
  Load Avg:  1.0  1.00439453125  0.77734375
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
    CPU MHz:             2095.244
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
| Address Size       | 48 bits virtual, 46 bits physical                       |
| SIMD               | 512 bit = 64 byte max. SIMD vector size                 |
| Time Stamp Counter | TSC is accessible via `rdtsc`                           |
|                    | TSC increased at every clock cycle (non-invariant TSC)  |
| Perf. Monitoring   | Performance Monitoring Counters (PMC) are not supported |
| Hypervisor         | Yes, Microsoft                                          |

