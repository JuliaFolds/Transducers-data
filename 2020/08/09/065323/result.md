# Benchmark result

* Pull request commit: [`34001b3d0471e7eea4b630ca3e2034ac751431e7`](https://github.com/JuliaFolds/Transducers.jl/commit/34001b3d0471e7eea4b630ca3e2034ac751431e7)
* Pull request: <https://github.com/JuliaFolds/Transducers.jl/pull/405> (Add bench_sum_transpose.jl)

# Judge result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmarks:
    - Target: 9 Aug 2020 - 06:47
    - Baseline: 9 Aug 2020 - 06:52
* Package commits:
    - Target: 3b595e
    - Baseline: 65db24
* Julia commits:
    - Target: 44fa15
    - Baseline: 44fa15
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
| `["append!!", "eduction"]`                                     |                1.05 (5%) :x: |   1.00 (1%)  |
| `["cat", "xf"]`                                                | 0.84 (5%) :white_check_mark: |   1.00 (1%)  |
| `["filter_map_map!", "man"]`                                   |                1.07 (5%) :x: |   1.00 (1%)  |
| `["filter_map_map!", "xf"]`                                    | 0.93 (5%) :white_check_mark: |   1.00 (1%)  |
| `["filter_sum", "1000", "RandomFloats", "noinit", "base"]`     |                2.09 (5%) :x: |   1.00 (1%)  |
| `["filter_sum", "1000", "RandomFloats", "noinit", "naive"]`    |                1.05 (5%) :x: |   1.00 (1%)  |
| `["filter_sum", "1000", "RandomFloats", "withinit", "naive"]`  |                1.32 (5%) :x: |   1.00 (1%)  |
| `["filter_sum", "1000", "UnitRange", "noinit", "base"]`        | 0.93 (5%) :white_check_mark: |   1.00 (1%)  |
| `["filter_sum", "1000", "UnitRange", "noinit", "naive"]`       |                1.39 (5%) :x: |   1.00 (1%)  |
| `["filter_sum", "1000", "UnitRange", "withinit", "naive"]`     | 0.75 (5%) :white_check_mark: |   1.00 (1%)  |
| `["filter_sum", "10000", "RandomFloats", "noinit", "base"]`    |                1.12 (5%) :x: |   1.00 (1%)  |
| `["filter_sum", "10000", "RandomFloats", "noinit", "naive"]`   |                1.22 (5%) :x: |   1.00 (1%)  |
| `["filter_sum", "10000", "RandomFloats", "withinit", "naive"]` |                1.08 (5%) :x: |   1.00 (1%)  |
| `["filter_sum", "10000", "RandomFloats", "withinit", "xf"]`    | 0.93 (5%) :white_check_mark: |   1.00 (1%)  |
| `["filter_sum", "10000", "UnitRange", "noinit", "naive"]`      |                1.40 (5%) :x: |   1.00 (1%)  |
| `["filter_sum", "10000", "UnitRange", "withinit", "naive"]`    | 0.74 (5%) :white_check_mark: |   1.00 (1%)  |
| `["gemm", "fusedmul", "xf", "16"]`                             |                1.13 (5%) :x: |   1.00 (1%)  |
| `["gemm", "fusedmul", "xf", "2"]`                              |                1.09 (5%) :x: |   1.00 (1%)  |
| `["gemm", "fusedmul", "xf", "8"]`                              | 0.93 (5%) :white_check_mark: |   1.00 (1%)  |
| `["gemm", "mul", "linalg", "8"]`                               | 0.90 (5%) :white_check_mark: |   1.00 (1%)  |
| `["gemm", "mul", "man", "false", "256"]`                       | 0.95 (5%) :white_check_mark: |   1.00 (1%)  |
| `["gemm", "mul", "man", "false", "32"]`                        |                1.11 (5%) :x: |   1.00 (1%)  |
| `["gemm", "mul", "man", "false", "8"]`                         | 0.72 (5%) :white_check_mark: |   1.00 (1%)  |
| `["gemm", "mul", "man", "ivdep", "8"]`                         |                1.08 (5%) :x: |   1.00 (1%)  |
| `["gemm", "mul", "man", "true", "256"]`                        | 0.95 (5%) :white_check_mark: |   1.00 (1%)  |
| `["gemm", "mul", "man", "true", "32"]`                         |                1.08 (5%) :x: |   1.00 (1%)  |
| `["gemm", "mul", "man", "true", "8"]`                          |                1.36 (5%) :x: |   1.00 (1%)  |
| `["gemm", "mul", "xf", "false", "32"]`                         |                1.28 (5%) :x: |   1.00 (1%)  |
| `["gemm", "mul", "xf", "false", "8"]`                          |                1.09 (5%) :x: |   1.00 (1%)  |
| `["gemm", "mul", "xf", "ivdep", "8"]`                          |                1.27 (5%) :x: |   1.00 (1%)  |
| `["gemm", "mul", "xf", "true", "32"]`                          | 0.89 (5%) :white_check_mark: |   1.00 (1%)  |
| `["gemm", "mul", "xf", "true", "8"]`                           | 0.73 (5%) :white_check_mark: |   1.00 (1%)  |
| `["groupby", "sum", "xf-with-init"]`                           | 0.92 (5%) :white_check_mark: |   1.00 (1%)  |
| `["mapcat_eduction", "xf-eduction"]`                           | 0.90 (5%) :white_check_mark: |   1.00 (1%)  |
| `["missing_dot", "man"]`                                       | 0.95 (5%) :white_check_mark: |   1.00 (1%)  |
| `["missing_dot", "rf_nota"]`                                   | 0.93 (5%) :white_check_mark: |   1.00 (1%)  |
| `["missing_dot", "xf_nota"]`                                   | 0.93 (5%) :white_check_mark: |   1.00 (1%)  |
| `["overhead", "foldl"]`                                        |                1.08 (5%) :x: |   1.00 (1%)  |
| `["partition_by", "man"]`                                      |                1.06 (5%) :x: |   1.00 (1%)  |
| `["set", "base"]`                                              |                1.13 (5%) :x: |   1.00 (1%)  |

## Benchmark Group List
Here's a list of all the benchmark groups executed by this job:

- `["append!!"]`
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

## Julia versioninfo

### Target
```
Julia Version 1.4.2
Commit 44fa15b150* (2020-05-23 18:35 UTC)
Platform Info:
  OS: Linux (x86_64-pc-linux-gnu)
      Ubuntu 18.04.4 LTS
  uname: Linux 5.3.0-1034-azure #35~18.04.1-Ubuntu SMP Mon Jul 13 12:54:45 UTC 2020 x86_64 x86_64
  CPU: Intel(R) Xeon(R) Platinum 8171M CPU @ 2.60GHz: 
              speed         user         nice          sys         idle          irq
       #1  2095 MHz      11238 s          0 s       1483 s      75010 s          0 s
       #2  2095 MHz      71208 s          0 s       1760 s      14814 s          0 s
       
  Memory: 6.764873504638672 GB (2461.12890625 MB free)
  Uptime: 896.0 sec
  Load Avg:  1.05126953125  1.01416015625  0.72119140625
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-8.0.1 (ORCJIT, skylake)
```

### Baseline
```
Julia Version 1.4.2
Commit 44fa15b150* (2020-05-23 18:35 UTC)
Platform Info:
  OS: Linux (x86_64-pc-linux-gnu)
      Ubuntu 18.04.4 LTS
  uname: Linux 5.3.0-1034-azure #35~18.04.1-Ubuntu SMP Mon Jul 13 12:54:45 UTC 2020 x86_64 x86_64
  CPU: Intel(R) Xeon(R) Platinum 8171M CPU @ 2.60GHz: 
              speed         user         nice          sys         idle          irq
       #1  2095 MHz      15742 s          0 s       1536 s     101490 s          0 s
       #2  2095 MHz      97673 s          0 s       1938 s      19199 s          0 s
       
  Memory: 6.764873504638672 GB (2602.08203125 MB free)
  Uptime: 1208.0 sec
  Load Avg:  1.0078125  1.0048828125  0.8193359375
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-8.0.1 (ORCJIT, skylake)
```

---
# Target result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmark: 9 Aug 2020 - 6:47
* Package commit: 3b595e
* Julia commit: 44fa15
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
| `["append!!", "eduction"]`                                     |  21.900 μs (5%) |         |  64.72 KiB (1%) |          18 |
| `["append!!", "xf"]`                                           |  21.900 μs (5%) |         |  64.72 KiB (1%) |          18 |
| `["cat", "base"]`                                              |   1.920 μs (5%) |         |                 |             |
| `["cat", "xf"]`                                                |   2.200 μs (5%) |         |                 |             |
| `["collect", "filter-missing"]`                                | 119.600 μs (5%) |         | 345.31 KiB (1%) |       10015 |
| `["collect", "identity-float"]`                                |  85.700 μs (5%) |         | 569.16 KiB (1%) |       10015 |
| `["collect", "identity-union"]`                                | 348.899 μs (5%) |         | 705.23 KiB (1%) |       16667 |
| `["dict", "base"]`                                             |   4.696 ms (5%) |         |  92.91 KiB (1%) |          22 |
| `["dict", "xf"]`                                               |   4.689 ms (5%) |         |  92.36 KiB (1%) |          21 |
| `["dot", "blas"]`                                              |   1.430 μs (5%) |         |                 |             |
| `["dot", "man"]`                                               |   1.350 μs (5%) |         |                 |             |
| `["dot", "rf"]`                                                |   2.400 μs (5%) |         |                 |             |
| `["dot", "xf"]`                                                |   2.467 μs (5%) |         |   64 bytes (1%) |           3 |
| `["filter_map_map!", "man"]`                                   |  65.700 μs (5%) |         |                 |             |
| `["filter_map_map!", "xf"]`                                    | 784.099 μs (5%) |         |  304 bytes (1%) |          17 |
| `["filter_map_reduce", "man"]`                                 | 255.799 μs (5%) |         |                 |             |
| `["filter_map_reduce", "xf"]`                                  | 255.799 μs (5%) |         |                 |             |
| `["filter_sum", "1000", "RandomFloats", "noinit", "base"]`     |   3.112 μs (5%) |         |                 |             |
| `["filter_sum", "1000", "RandomFloats", "noinit", "naive"]`    |   1.590 μs (5%) |         |                 |             |
| `["filter_sum", "1000", "RandomFloats", "noinit", "xf"]`       |   1.540 μs (5%) |         |                 |             |
| `["filter_sum", "1000", "RandomFloats", "withinit", "base"]`   |   1.980 μs (5%) |         |                 |             |
| `["filter_sum", "1000", "RandomFloats", "withinit", "naive"]`  | 970.370 ns (5%) |         |                 |             |
| `["filter_sum", "1000", "RandomFloats", "withinit", "xf"]`     |   1.980 μs (5%) |         |                 |             |
| `["filter_sum", "1000", "UnitRange", "noinit", "base"]`        |   2.022 μs (5%) |         |                 |             |
| `["filter_sum", "1000", "UnitRange", "noinit", "naive"]`       |   1.310 μs (5%) |         |                 |             |
| `["filter_sum", "1000", "UnitRange", "noinit", "xf"]`          |   1.790 μs (5%) |         |                 |             |
| `["filter_sum", "1000", "UnitRange", "withinit", "base"]`      | 117.000 ns (5%) |         |                 |             |
| `["filter_sum", "1000", "UnitRange", "withinit", "naive"]`     | 756.888 ns (5%) |         |                 |             |
| `["filter_sum", "1000", "UnitRange", "withinit", "xf"]`        | 123.314 ns (5%) |         |                 |             |
| `["filter_sum", "10000", "RandomFloats", "noinit", "base"]`    |  56.100 μs (5%) |         |                 |             |
| `["filter_sum", "10000", "RandomFloats", "noinit", "naive"]`   |  71.600 μs (5%) |         |                 |             |
| `["filter_sum", "10000", "RandomFloats", "noinit", "xf"]`      |  51.699 μs (5%) |         |                 |             |
| `["filter_sum", "10000", "RandomFloats", "withinit", "base"]`  |  20.100 μs (5%) |         |                 |             |
| `["filter_sum", "10000", "RandomFloats", "withinit", "naive"]` |  52.100 μs (5%) |         |                 |             |
| `["filter_sum", "10000", "RandomFloats", "withinit", "xf"]`    |  20.100 μs (5%) |         |                 |             |
| `["filter_sum", "10000", "UnitRange", "noinit", "base"]`       |  20.000 μs (5%) |         |                 |             |
| `["filter_sum", "10000", "UnitRange", "noinit", "naive"]`      |  12.999 μs (5%) |         |                 |             |
| `["filter_sum", "10000", "UnitRange", "noinit", "xf"]`         |  17.799 μs (5%) |         |                 |             |
| `["filter_sum", "10000", "UnitRange", "withinit", "base"]`     |   1.120 μs (5%) |         |                 |             |
| `["filter_sum", "10000", "UnitRange", "withinit", "naive"]`    |   7.450 μs (5%) |         |                 |             |
| `["filter_sum", "10000", "UnitRange", "withinit", "xf"]`       |   1.190 μs (5%) |         |                 |             |
| `["findall", "base"]`                                          | 905.798 μs (5%) |         |   2.00 MiB (1%) |          21 |
| `["findall", "xf-array"]`                                      | 886.898 μs (5%) |         |   3.02 MiB (1%) |       98970 |
| `["findall", "xf-iter"]`                                       | 959.198 μs (5%) |         |   5.05 MiB (1%) |       99913 |
| `["gemm", "fusedmul", "blas", "16"]`                           |   4.887 ms (5%) |         |                 |             |
| `["gemm", "fusedmul", "blas", "2"]`                            |   3.585 ms (5%) |         |                 |             |
| `["gemm", "fusedmul", "blas", "32"]`                           |   6.646 ms (5%) |         |                 |             |
| `["gemm", "fusedmul", "blas", "8"]`                            |   3.909 ms (5%) |         |                 |             |
| `["gemm", "fusedmul", "xf", "16"]`                             |   5.265 ms (5%) |         |  160 bytes (1%) |           6 |
| `["gemm", "fusedmul", "xf", "2"]`                              | 597.699 μs (5%) |         |  160 bytes (1%) |           6 |
| `["gemm", "fusedmul", "xf", "32"]`                             |   8.815 ms (5%) |         |  160 bytes (1%) |           6 |
| `["gemm", "fusedmul", "xf", "8"]`                              |   2.045 ms (5%) |         |  160 bytes (1%) |           6 |
| `["gemm", "mul", "linalg", "256"]`                             | 994.098 μs (5%) |         |                 |             |
| `["gemm", "mul", "linalg", "32"]`                              |   3.350 μs (5%) |         |                 |             |
| `["gemm", "mul", "linalg", "8"]`                               | 270.624 ns (5%) |         |                 |             |
| `["gemm", "mul", "man", "false", "256"]`                       |   1.809 ms (5%) |         |                 |             |
| `["gemm", "mul", "man", "false", "32"]`                        |   5.317 μs (5%) |         |                 |             |
| `["gemm", "mul", "man", "false", "8"]`                         | 433.163 ns (5%) |         |                 |             |
| `["gemm", "mul", "man", "ivdep", "256"]`                       |   1.796 ms (5%) |         |                 |             |
| `["gemm", "mul", "man", "ivdep", "32"]`                        |   4.228 μs (5%) |         |                 |             |
| `["gemm", "mul", "man", "ivdep", "8"]`                         | 431.156 ns (5%) |         |                 |             |
| `["gemm", "mul", "man", "true", "256"]`                        |   1.800 ms (5%) |         |                 |             |
| `["gemm", "mul", "man", "true", "32"]`                         |   5.483 μs (5%) |         |                 |             |
| `["gemm", "mul", "man", "true", "8"]`                          | 545.902 ns (5%) |         |                 |             |
| `["gemm", "mul", "xf", "false", "256"]`                        |   1.819 ms (5%) |         |   48 bytes (1%) |           2 |
| `["gemm", "mul", "xf", "false", "32"]`                         |   6.680 μs (5%) |         |   48 bytes (1%) |           2 |
| `["gemm", "mul", "xf", "false", "8"]`                          | 436.181 ns (5%) |         |   48 bytes (1%) |           2 |
| `["gemm", "mul", "xf", "ivdep", "256"]`                        |   1.855 ms (5%) |         |   48 bytes (1%) |           2 |
| `["gemm", "mul", "xf", "ivdep", "32"]`                         |   4.114 μs (5%) |         |   48 bytes (1%) |           2 |
| `["gemm", "mul", "xf", "ivdep", "8"]`                          | 507.767 ns (5%) |         |   48 bytes (1%) |           2 |
| `["gemm", "mul", "xf", "true", "256"]`                         |   1.878 ms (5%) |         |   48 bytes (1%) |           2 |
| `["gemm", "mul", "xf", "true", "32"]`                          |   5.333 μs (5%) |         |   48 bytes (1%) |           2 |
| `["gemm", "mul", "xf", "true", "8"]`                           | 435.171 ns (5%) |         |   48 bytes (1%) |           2 |
| `["groupby", "sum", "sac"]`                                    | 287.599 μs (5%) |         | 313.14 KiB (1%) |       10007 |
| `["groupby", "sum", "xf-with-init"]`                           | 204.599 μs (5%) |         | 157.44 KiB (1%) |       10008 |
| `["groupby", "sum", "xf-without-init"]`                        | 211.400 μs (5%) |         | 157.44 KiB (1%) |       10008 |
| `["mapcat_eduction", "base"]`                                  |   2.089 μs (5%) |         |                 |             |
| `["mapcat_eduction", "xf-eduction"]`                           |   2.133 μs (5%) |         |                 |             |
| `["mapcat_eduction", "xf-xf"]`                                 |   2.255 μs (5%) |         |                 |             |
| `["missing_argmax", "man"]`                                    |   2.989 μs (5%) |         |   32 bytes (1%) |           1 |
| `["missing_argmax", "rf"]`                                     |   2.875 μs (5%) |         |   32 bytes (1%) |           1 |
| `["missing_argmax", "xf"]`                                     |   3.612 μs (5%) |         |   32 bytes (1%) |           1 |
| `["missing_dot", "equiv"]`                                     |   1.650 μs (5%) |         |   16 bytes (1%) |           1 |
| `["missing_dot", "man"]`                                       |   1.560 μs (5%) |         |   16 bytes (1%) |           1 |
| `["missing_dot", "naive"]`                                     |   5.450 μs (5%) |         |   16 bytes (1%) |           1 |
| `["missing_dot", "rf"]`                                        |   1.540 μs (5%) |         |   16 bytes (1%) |           1 |
| `["missing_dot", "rf_nota"]`                                   |   1.630 μs (5%) |         |   16 bytes (1%) |           1 |
| `["missing_dot", "xf"]`                                        | 229.999 μs (5%) |         |  71.97 KiB (1%) |        3734 |
| `["missing_dot", "xf_nota"]`                                   | 233.199 μs (5%) |         |  72.16 KiB (1%) |        3744 |
| `["overhead", "foldl"]`                                        |   5.599 ns (5%) |         |                 |             |
| `["overhead", "reduce_basecase"]`                              | 295.219 ns (5%) |         |  464 bytes (1%) |           9 |
| `["partition_by", "man"]`                                      |   2.412 ms (5%) |         |  352 bytes (1%) |           4 |
| `["partition_by", "xf"]`                                       |   3.534 ms (5%) |         |   6.10 MiB (1%) |      200007 |
| `["set", "base"]`                                              |   6.024 ms (5%) |         |  49.58 KiB (1%) |          18 |
| `["set", "xf"]`                                                |   5.411 ms (5%) |         |  49.63 KiB (1%) |          21 |
| `["sum_transpose", "30", "noinit", "iter"]`                    |   2.522 μs (5%) |         |                 |             |
| `["sum_transpose", "30", "noinit", "man"]`                     |   2.822 μs (5%) |         |                 |             |
| `["sum_transpose", "30", "noinit", "xf"]`                      |   3.350 μs (5%) |         |                 |             |
| `["sum_transpose", "30", "withinit", "iter"]`                  |   1.660 μs (5%) |         |                 |             |
| `["sum_transpose", "30", "withinit", "man"]`                   |   1.380 μs (5%) |         |                 |             |
| `["sum_transpose", "30", "withinit", "xf"]`                    |   3.287 μs (5%) |         |                 |             |

## Benchmark Group List
Here's a list of all the benchmark groups executed by this job:

- `["append!!"]`
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

## Julia versioninfo
```
Julia Version 1.4.2
Commit 44fa15b150* (2020-05-23 18:35 UTC)
Platform Info:
  OS: Linux (x86_64-pc-linux-gnu)
      Ubuntu 18.04.4 LTS
  uname: Linux 5.3.0-1034-azure #35~18.04.1-Ubuntu SMP Mon Jul 13 12:54:45 UTC 2020 x86_64 x86_64
  CPU: Intel(R) Xeon(R) Platinum 8171M CPU @ 2.60GHz: 
              speed         user         nice          sys         idle          irq
       #1  2095 MHz      11238 s          0 s       1483 s      75010 s          0 s
       #2  2095 MHz      71208 s          0 s       1760 s      14814 s          0 s
       
  Memory: 6.764873504638672 GB (2461.12890625 MB free)
  Uptime: 896.0 sec
  Load Avg:  1.05126953125  1.01416015625  0.72119140625
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-8.0.1 (ORCJIT, skylake)
```

---
# Baseline result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmark: 9 Aug 2020 - 6:52
* Package commit: 65db24
* Julia commit: 44fa15
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
| `["append!!", "eduction"]`                                     |  20.800 μs (5%) |         |  64.72 KiB (1%) |          18 |
| `["append!!", "xf"]`                                           |  21.600 μs (5%) |         |  64.72 KiB (1%) |          18 |
| `["cat", "base"]`                                              |   1.930 μs (5%) |         |                 |             |
| `["cat", "xf"]`                                                |   2.611 μs (5%) |         |                 |             |
| `["collect", "filter-missing"]`                                | 120.706 μs (5%) |         | 345.31 KiB (1%) |       10015 |
| `["collect", "identity-float"]`                                |  83.105 μs (5%) |         | 569.16 KiB (1%) |       10015 |
| `["collect", "identity-union"]`                                | 348.318 μs (5%) |         | 705.34 KiB (1%) |       16681 |
| `["dict", "base"]`                                             |   4.594 ms (5%) |         |  92.91 KiB (1%) |          22 |
| `["dict", "xf"]`                                               |   4.782 ms (5%) |         |  92.36 KiB (1%) |          21 |
| `["dot", "blas"]`                                              |   1.420 μs (5%) |         |                 |             |
| `["dot", "man"]`                                               |   1.410 μs (5%) |         |                 |             |
| `["dot", "rf"]`                                                |   2.400 μs (5%) |         |                 |             |
| `["dot", "xf"]`                                                |   2.456 μs (5%) |         |   64 bytes (1%) |           3 |
| `["filter_map_map!", "man"]`                                   |  61.402 μs (5%) |         |                 |             |
| `["filter_map_map!", "xf"]`                                    | 839.724 μs (5%) |         |  304 bytes (1%) |          17 |
| `["filter_map_reduce", "man"]`                                 | 256.011 μs (5%) |         |                 |             |
| `["filter_map_reduce", "xf"]`                                  | 255.812 μs (5%) |         |                 |             |
| `["filter_sum", "1000", "RandomFloats", "noinit", "base"]`     |   1.488 μs (5%) |         |                 |             |
| `["filter_sum", "1000", "RandomFloats", "noinit", "naive"]`    |   1.510 μs (5%) |         |                 |             |
| `["filter_sum", "1000", "RandomFloats", "noinit", "xf"]`       |   1.490 μs (5%) |         |                 |             |
| `["filter_sum", "1000", "RandomFloats", "withinit", "base"]`   |   1.980 μs (5%) |         |                 |             |
| `["filter_sum", "1000", "RandomFloats", "withinit", "naive"]`  | 733.370 ns (5%) |         |                 |             |
| `["filter_sum", "1000", "RandomFloats", "withinit", "xf"]`     |   1.980 μs (5%) |         |                 |             |
| `["filter_sum", "1000", "UnitRange", "noinit", "base"]`        |   2.178 μs (5%) |         |                 |             |
| `["filter_sum", "1000", "UnitRange", "noinit", "naive"]`       | 940.000 ns (5%) |         |                 |             |
| `["filter_sum", "1000", "UnitRange", "noinit", "xf"]`          |   1.800 μs (5%) |         |                 |             |
| `["filter_sum", "1000", "UnitRange", "withinit", "base"]`      | 115.117 ns (5%) |         |                 |             |
| `["filter_sum", "1000", "UnitRange", "withinit", "naive"]`     |   1.015 μs (5%) |         |                 |             |
| `["filter_sum", "1000", "UnitRange", "withinit", "xf"]`        | 123.435 ns (5%) |         |                 |             |
| `["filter_sum", "10000", "RandomFloats", "noinit", "base"]`    |  50.003 μs (5%) |         |                 |             |
| `["filter_sum", "10000", "RandomFloats", "noinit", "naive"]`   |  58.603 μs (5%) |         |                 |             |
| `["filter_sum", "10000", "RandomFloats", "noinit", "xf"]`      |  50.002 μs (5%) |         |                 |             |
| `["filter_sum", "10000", "RandomFloats", "withinit", "base"]`  |  20.101 μs (5%) |         |                 |             |
| `["filter_sum", "10000", "RandomFloats", "withinit", "naive"]` |  48.302 μs (5%) |         |                 |             |
| `["filter_sum", "10000", "RandomFloats", "withinit", "xf"]`    |  21.701 μs (5%) |         |                 |             |
| `["filter_sum", "10000", "UnitRange", "noinit", "base"]`       |  20.001 μs (5%) |         |                 |             |
| `["filter_sum", "10000", "UnitRange", "noinit", "naive"]`      |   9.300 μs (5%) |         |                 |             |
| `["filter_sum", "10000", "UnitRange", "noinit", "xf"]`         |  17.800 μs (5%) |         |                 |             |
| `["filter_sum", "10000", "UnitRange", "withinit", "base"]`     |   1.120 μs (5%) |         |                 |             |
| `["filter_sum", "10000", "UnitRange", "withinit", "naive"]`    |  10.050 μs (5%) |         |                 |             |
| `["filter_sum", "10000", "UnitRange", "withinit", "xf"]`       |   1.190 μs (5%) |         |                 |             |
| `["findall", "base"]`                                          | 923.745 μs (5%) |         |   2.00 MiB (1%) |          21 |
| `["findall", "xf-array"]`                                      | 903.943 μs (5%) |         |   3.02 MiB (1%) |       98970 |
| `["findall", "xf-iter"]`                                       | 950.044 μs (5%) |         |   5.05 MiB (1%) |       99913 |
| `["gemm", "fusedmul", "blas", "16"]`                           |   4.739 ms (5%) |         |                 |             |
| `["gemm", "fusedmul", "blas", "2"]`                            |   3.520 ms (5%) |         |                 |             |
| `["gemm", "fusedmul", "blas", "32"]`                           |   6.838 ms (5%) |         |                 |             |
| `["gemm", "fusedmul", "blas", "8"]`                            |   3.754 ms (5%) |         |                 |             |
| `["gemm", "fusedmul", "xf", "16"]`                             |   4.641 ms (5%) |         |  160 bytes (1%) |           6 |
| `["gemm", "fusedmul", "xf", "2"]`                              | 550.317 μs (5%) |         |  160 bytes (1%) |           6 |
| `["gemm", "fusedmul", "xf", "32"]`                             |   9.144 ms (5%) |         |  160 bytes (1%) |           6 |
| `["gemm", "fusedmul", "xf", "8"]`                              |   2.209 ms (5%) |         |  160 bytes (1%) |           6 |
| `["gemm", "mul", "linalg", "256"]`                             | 995.541 μs (5%) |         |                 |             |
| `["gemm", "mul", "linalg", "32"]`                              |   3.400 μs (5%) |         |                 |             |
| `["gemm", "mul", "linalg", "8"]`                               | 300.000 ns (5%) |         |                 |             |
| `["gemm", "mul", "man", "false", "256"]`                       |   1.906 ms (5%) |         |                 |             |
| `["gemm", "mul", "man", "false", "32"]`                        |   4.800 μs (5%) |         |                 |             |
| `["gemm", "mul", "man", "false", "8"]`                         | 600.000 ns (5%) |         |                 |             |
| `["gemm", "mul", "man", "ivdep", "256"]`                       |   1.880 ms (5%) |         |                 |             |
| `["gemm", "mul", "man", "ivdep", "32"]`                        |   4.300 μs (5%) |         |                 |             |
| `["gemm", "mul", "man", "ivdep", "8"]`                         | 400.000 ns (5%) |         |                 |             |
| `["gemm", "mul", "man", "true", "256"]`                        |   1.895 ms (5%) |         |                 |             |
| `["gemm", "mul", "man", "true", "32"]`                         |   5.100 μs (5%) |         |                 |             |
| `["gemm", "mul", "man", "true", "8"]`                          | 400.000 ns (5%) |         |                 |             |
| `["gemm", "mul", "xf", "false", "256"]`                        |   1.913 ms (5%) |         |   48 bytes (1%) |           2 |
| `["gemm", "mul", "xf", "false", "32"]`                         |   5.200 μs (5%) |         |   48 bytes (1%) |           2 |
| `["gemm", "mul", "xf", "false", "8"]`                          | 400.000 ns (5%) |         |   48 bytes (1%) |           2 |
| `["gemm", "mul", "xf", "ivdep", "256"]`                        |   1.873 ms (5%) |         |   48 bytes (1%) |           2 |
| `["gemm", "mul", "xf", "ivdep", "32"]`                         |   4.100 μs (5%) |         |   48 bytes (1%) |           2 |
| `["gemm", "mul", "xf", "ivdep", "8"]`                          | 400.000 ns (5%) |         |   48 bytes (1%) |           2 |
| `["gemm", "mul", "xf", "true", "256"]`                         |   1.889 ms (5%) |         |   48 bytes (1%) |           2 |
| `["gemm", "mul", "xf", "true", "32"]`                          |   6.000 μs (5%) |         |   48 bytes (1%) |           2 |
| `["gemm", "mul", "xf", "true", "8"]`                           | 600.000 ns (5%) |         |   48 bytes (1%) |           2 |
| `["groupby", "sum", "sac"]`                                    | 277.208 μs (5%) |         | 313.14 KiB (1%) |       10007 |
| `["groupby", "sum", "xf-with-init"]`                           | 222.106 μs (5%) |         | 157.44 KiB (1%) |       10008 |
| `["groupby", "sum", "xf-without-init"]`                        | 213.806 μs (5%) |         | 157.44 KiB (1%) |       10008 |
| `["mapcat_eduction", "base"]`                                  |   2.067 μs (5%) |         |                 |             |
| `["mapcat_eduction", "xf-eduction"]`                           |   2.367 μs (5%) |         |                 |             |
| `["mapcat_eduction", "xf-xf"]`                                 |   2.367 μs (5%) |         |                 |             |
| `["missing_argmax", "man"]`                                    |   2.978 μs (5%) |         |   32 bytes (1%) |           1 |
| `["missing_argmax", "rf"]`                                     |   2.813 μs (5%) |         |   32 bytes (1%) |           1 |
| `["missing_argmax", "xf"]`                                     |   3.625 μs (5%) |         |   32 bytes (1%) |           1 |
| `["missing_dot", "equiv"]`                                     |   1.630 μs (5%) |         |   16 bytes (1%) |           1 |
| `["missing_dot", "man"]`                                       |   1.650 μs (5%) |         |   16 bytes (1%) |           1 |
| `["missing_dot", "naive"]`                                     |   5.434 μs (5%) |         |   16 bytes (1%) |           1 |
| `["missing_dot", "rf"]`                                        |   1.530 μs (5%) |         |   16 bytes (1%) |           1 |
| `["missing_dot", "rf_nota"]`                                   |   1.760 μs (5%) |         |   16 bytes (1%) |           1 |
| `["missing_dot", "xf"]`                                        | 239.911 μs (5%) |         |  71.92 KiB (1%) |        3733 |
| `["missing_dot", "xf_nota"]`                                   | 250.110 μs (5%) |         |  72.16 KiB (1%) |        3744 |
| `["overhead", "foldl"]`                                        |   5.200 ns (5%) |         |                 |             |
| `["overhead", "reduce_basecase"]`                              | 301.211 ns (5%) |         |  464 bytes (1%) |           9 |
| `["partition_by", "man"]`                                      |   2.266 ms (5%) |         |  352 bytes (1%) |           4 |
| `["partition_by", "xf"]`                                       |   3.589 ms (5%) |         |   6.10 MiB (1%) |      200007 |
| `["set", "base"]`                                              |   5.325 ms (5%) |         |  49.58 KiB (1%) |          18 |
| `["set", "xf"]`                                                |   5.173 ms (5%) |         |  49.63 KiB (1%) |          21 |

## Benchmark Group List
Here's a list of all the benchmark groups executed by this job:

- `["append!!"]`
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

## Julia versioninfo
```
Julia Version 1.4.2
Commit 44fa15b150* (2020-05-23 18:35 UTC)
Platform Info:
  OS: Linux (x86_64-pc-linux-gnu)
      Ubuntu 18.04.4 LTS
  uname: Linux 5.3.0-1034-azure #35~18.04.1-Ubuntu SMP Mon Jul 13 12:54:45 UTC 2020 x86_64 x86_64
  CPU: Intel(R) Xeon(R) Platinum 8171M CPU @ 2.60GHz: 
              speed         user         nice          sys         idle          irq
       #1  2095 MHz      15742 s          0 s       1536 s     101490 s          0 s
       #2  2095 MHz      97673 s          0 s       1938 s      19199 s          0 s
       
  Memory: 6.764873504638672 GB (2602.08203125 MB free)
  Uptime: 1208.0 sec
  Load Avg:  1.0078125  1.0048828125  0.8193359375
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-8.0.1 (ORCJIT, skylake)
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
    CPU MHz:             2095.076
    BogoMIPS:            4190.15
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

