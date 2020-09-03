# Benchmark result

* Pull request commit: [`8824363395609874ce4e9a388bbddbf7ba1de044`](https://github.com/JuliaFolds/Transducers.jl/commit/8824363395609874ce4e9a388bbddbf7ba1de044)
* Pull request: <https://github.com/JuliaFolds/Transducers.jl/pull/243> (Update */Manifest.toml)

# Judge result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmarks:
    - Target: 3 Sep 2020 - 01:01
    - Baseline: 3 Sep 2020 - 01:07
* Package commits:
    - Target: c8f1ff
    - Baseline: c8dada
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
| `["cartesian", "copyto!", "man"]`                              |                1.06 (5%) :x: |    1.00 (1%)  |
| `["collect", "filter-missing"]`                                | 0.94 (5%) :white_check_mark: |    1.00 (1%)  |
| `["dict", "base"]`                                             | 0.94 (5%) :white_check_mark: |    1.00 (1%)  |
| `["filter_map_map!", "xf"]`                                    | 0.95 (5%) :white_check_mark: |    1.00 (1%)  |
| `["filter_sum", "1000", "RandomFloats", "noinit", "base"]`     |                3.91 (5%) :x: |    1.00 (1%)  |
| `["filter_sum", "1000", "RandomFloats", "withinit", "base"]`   | 0.93 (5%) :white_check_mark: |    1.00 (1%)  |
| `["filter_sum", "1000", "RandomFloats", "withinit", "naive"]`  |                1.11 (5%) :x: |    1.00 (1%)  |
| `["filter_sum", "1000", "UnitRange", "noinit", "xf"]`          |                1.06 (5%) :x: |    1.00 (1%)  |
| `["filter_sum", "1000", "UnitRange", "withinit", "naive"]`     |                1.06 (5%) :x: |    1.00 (1%)  |
| `["filter_sum", "10000", "RandomFloats", "noinit", "base"]`    |                1.13 (5%) :x: |    1.00 (1%)  |
| `["filter_sum", "10000", "RandomFloats", "noinit", "naive"]`   | 0.93 (5%) :white_check_mark: |    1.00 (1%)  |
| `["filter_sum", "10000", "RandomFloats", "withinit", "base"]`  | 0.84 (5%) :white_check_mark: |    1.00 (1%)  |
| `["filter_sum", "10000", "RandomFloats", "withinit", "naive"]` | 0.92 (5%) :white_check_mark: |    1.00 (1%)  |
| `["filter_sum", "10000", "RandomFloats", "withinit", "xf"]`    | 0.93 (5%) :white_check_mark: |    1.00 (1%)  |
| `["filter_sum", "10000", "UnitRange", "noinit", "base"]`       | 0.90 (5%) :white_check_mark: |    1.00 (1%)  |
| `["filter_sum", "10000", "UnitRange", "noinit", "xf"]`         | 0.94 (5%) :white_check_mark: |    1.00 (1%)  |
| `["filter_sum", "10000", "UnitRange", "withinit", "base"]`     | 0.87 (5%) :white_check_mark: |    1.00 (1%)  |
| `["filter_sum", "10000", "UnitRange", "withinit", "xf"]`       | 0.90 (5%) :white_check_mark: |    1.00 (1%)  |
| `["gemm", "fusedmul", "blas", "32"]`                           | 0.89 (5%) :white_check_mark: |    1.00 (1%)  |
| `["gemm", "mul", "linalg", "8"]`                               |                1.08 (5%) :x: |    1.00 (1%)  |
| `["gemm", "mul", "man", "false", "8"]`                         | 0.90 (5%) :white_check_mark: |    1.00 (1%)  |
| `["gemm", "mul", "man", "ivdep", "8"]`                         | 0.84 (5%) :white_check_mark: |    1.00 (1%)  |
| `["gemm", "mul", "xf", "false", "8"]`                          | 0.91 (5%) :white_check_mark: |    1.00 (1%)  |
| `["gemm", "mul", "xf", "true", "8"]`                           | 0.84 (5%) :white_check_mark: |    1.00 (1%)  |
| `["groupby", "sum", "sac"]`                                    | 0.76 (5%) :white_check_mark: | 2.51 (1%) :x: |
| `["groupby", "sum", "xf-with-init"]`                           | 0.95 (5%) :white_check_mark: |    1.00 (1%)  |
| `["missing_dot", "rf_nota"]`                                   | 0.88 (5%) :white_check_mark: |    1.00 (1%)  |
| `["missing_dot", "xf_nota"]`                                   | 0.91 (5%) :white_check_mark: |    1.00 (1%)  |
| `["set", "xf"]`                                                | 0.94 (5%) :white_check_mark: |    1.00 (1%)  |
| `["sum_transpose", "30", "withinit", "iter"]`                  | 0.93 (5%) :white_check_mark: |    1.00 (1%)  |
| `["sum_transpose", "30", "withinit", "man"]`                   | 0.90 (5%) :white_check_mark: |    1.00 (1%)  |
| `["teerf_filter", "noinit"]`                                   | 0.93 (5%) :white_check_mark: |    1.00 (1%)  |
| `["teerf_filter", "withinit"]`                                 | 0.94 (5%) :white_check_mark: |    1.00 (1%)  |

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
  uname: Linux 5.3.0-1035-azure #36-Ubuntu SMP Thu Aug 6 09:21:33 UTC 2020 x86_64 x86_64
  CPU: Intel(R) Xeon(R) CPU E5-2673 v4 @ 2.30GHz: 
              speed         user         nice          sys         idle          irq
       #1  2294 MHz       7689 s          0 s       1222 s      81426 s          0 s
       #2  2294 MHz      73450 s          0 s       1845 s      15360 s          0 s
       
  Memory: 6.764873504638672 GB (2900.2734375 MB free)
  Uptime: 925.0 sec
  Load Avg:  1.0068359375  1.0  0.7119140625
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-9.0.1 (ORCJIT, broadwell)
```

### Baseline
```
Julia Version 1.5.1
Commit 697e782ab8 (2020-08-25 20:08 UTC)
Platform Info:
  OS: Linux (x86_64-pc-linux-gnu)
      Ubuntu 18.04.5 LTS
  uname: Linux 5.3.0-1035-azure #36-Ubuntu SMP Thu Aug 6 09:21:33 UTC 2020 x86_64 x86_64
  CPU: Intel(R) Xeon(R) CPU E5-2673 v4 @ 2.30GHz: 
              speed         user         nice          sys         idle          irq
       #1  2294 MHz      11265 s          0 s       1397 s     113018 s          0 s
       #2  2294 MHz     104873 s          0 s       2107 s      18991 s          0 s
       
  Memory: 6.764873504638672 GB (2866.52734375 MB free)
  Uptime: 1280.0 sec
  Load Avg:  1.0009765625  1.009765625  0.82666015625
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-9.0.1 (ORCJIT, broadwell)
```

---
# Target result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmark: 3 Sep 2020 - 1:1
* Package commit: c8f1ff
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
| `["append!!", "eduction"]`                                     |  21.700 μs (5%) |         |  64.63 KiB (1%) |          13 |
| `["append!!", "xf"]`                                           |  20.200 μs (5%) |         |  64.63 KiB (1%) |          13 |
| `["cartesian", "copyto!", "iter"]`                             |   5.960 μs (5%) |         |                 |             |
| `["cartesian", "copyto!", "man"]`                              |   2.367 μs (5%) |         |                 |             |
| `["cartesian", "copyto!", "xf"]`                               |   2.800 μs (5%) |         |                 |             |
| `["cat", "base"]`                                              |   1.950 μs (5%) |         |                 |             |
| `["cat", "xf"]`                                                |   2.522 μs (5%) |         |                 |             |
| `["collect", "filter-missing"]`                                |  57.800 μs (5%) |         |  32.81 KiB (1%) |          14 |
| `["collect", "identity-float"]`                                |  33.400 μs (5%) |         | 256.66 KiB (1%) |          14 |
| `["collect", "identity-union"]`                                | 172.500 μs (5%) |         | 601.04 KiB (1%) |       10013 |
| `["dict", "base"]`                                             |   4.757 ms (5%) |         |  92.91 KiB (1%) |          22 |
| `["dict", "xf"]`                                               |   4.862 ms (5%) |         |  92.31 KiB (1%) |          18 |
| `["dot", "blas"]`                                              |   2.600 μs (5%) |         |                 |             |
| `["dot", "man"]`                                               |   2.578 μs (5%) |         |                 |             |
| `["dot", "rf"]`                                                |   3.563 μs (5%) |         |                 |             |
| `["dot", "xf"]`                                                |   3.663 μs (5%) |         |   64 bytes (1%) |           3 |
| `["filter_map_map!", "man"]`                                   |  75.300 μs (5%) |         |                 |             |
| `["filter_map_map!", "xf"]`                                    | 664.701 μs (5%) |         |   80 bytes (1%) |           3 |
| `["filter_map_reduce", "man"]`                                 | 233.900 μs (5%) |         |                 |             |
| `["filter_map_reduce", "xf"]`                                  | 233.900 μs (5%) |         |                 |             |
| `["filter_sum", "1000", "RandomFloats", "noinit", "base"]`     |   3.612 μs (5%) |         |                 |             |
| `["filter_sum", "1000", "RandomFloats", "noinit", "naive"]`    | 929.630 ns (5%) |         |                 |             |
| `["filter_sum", "1000", "RandomFloats", "noinit", "xf"]`       |   1.720 μs (5%) |         |                 |             |
| `["filter_sum", "1000", "RandomFloats", "withinit", "base"]`   |   1.720 μs (5%) |         |                 |             |
| `["filter_sum", "1000", "RandomFloats", "withinit", "naive"]`  |   1.070 μs (5%) |         |                 |             |
| `["filter_sum", "1000", "RandomFloats", "withinit", "xf"]`     |   1.910 μs (5%) |         |                 |             |
| `["filter_sum", "1000", "UnitRange", "noinit", "base"]`        |   2.000 μs (5%) |         |                 |             |
| `["filter_sum", "1000", "UnitRange", "noinit", "naive"]`       | 873.171 ns (5%) |         |                 |             |
| `["filter_sum", "1000", "UnitRange", "noinit", "xf"]`          | 218.152 ns (5%) |         |                 |             |
| `["filter_sum", "1000", "UnitRange", "withinit", "base"]`      | 188.376 ns (5%) |         |                 |             |
| `["filter_sum", "1000", "UnitRange", "withinit", "naive"]`     | 623.567 ns (5%) |         |                 |             |
| `["filter_sum", "1000", "UnitRange", "withinit", "xf"]`        | 197.545 ns (5%) |         |                 |             |
| `["filter_sum", "10000", "RandomFloats", "noinit", "base"]`    |  48.701 μs (5%) |         |                 |             |
| `["filter_sum", "10000", "RandomFloats", "noinit", "naive"]`   |  46.200 μs (5%) |         |                 |             |
| `["filter_sum", "10000", "RandomFloats", "noinit", "xf"]`      |  17.300 μs (5%) |         |                 |             |
| `["filter_sum", "10000", "RandomFloats", "withinit", "base"]`  |  16.200 μs (5%) |         |                 |             |
| `["filter_sum", "10000", "RandomFloats", "withinit", "naive"]` |  42.700 μs (5%) |         |                 |             |
| `["filter_sum", "10000", "RandomFloats", "withinit", "xf"]`    |  16.700 μs (5%) |         |                 |             |
| `["filter_sum", "10000", "UnitRange", "noinit", "base"]`       |  18.500 μs (5%) |         |                 |             |
| `["filter_sum", "10000", "UnitRange", "noinit", "naive"]`      |   8.967 μs (5%) |         |                 |             |
| `["filter_sum", "10000", "UnitRange", "noinit", "xf"]`         |   1.890 μs (5%) |         |                 |             |
| `["filter_sum", "10000", "UnitRange", "withinit", "base"]`     |   1.630 μs (5%) |         |                 |             |
| `["filter_sum", "10000", "UnitRange", "withinit", "naive"]`    |   5.760 μs (5%) |         |                 |             |
| `["filter_sum", "10000", "UnitRange", "withinit", "xf"]`       |   1.700 μs (5%) |         |                 |             |
| `["findall", "base"]`                                          | 924.302 μs (5%) |         |   2.00 MiB (1%) |          18 |
| `["findall", "xf-array"]`                                      | 901.102 μs (5%) |         |   3.02 MiB (1%) |       98829 |
| `["findall", "xf-iter"]`                                       | 373.301 μs (5%) |         |   2.00 MiB (1%) |          19 |
| `["gemm", "fusedmul", "blas", "16"]`                           |   5.720 ms (5%) |         |                 |             |
| `["gemm", "fusedmul", "blas", "2"]`                            |   4.063 ms (5%) |         |                 |             |
| `["gemm", "fusedmul", "blas", "32"]`                           |   7.528 ms (5%) |         |                 |             |
| `["gemm", "fusedmul", "blas", "8"]`                            |   4.230 ms (5%) |         |                 |             |
| `["gemm", "fusedmul", "xf", "16"]`                             |   5.415 ms (5%) |         |  192 bytes (1%) |           4 |
| `["gemm", "fusedmul", "xf", "2"]`                              | 672.301 μs (5%) |         |  192 bytes (1%) |           4 |
| `["gemm", "fusedmul", "xf", "32"]`                             |  10.891 ms (5%) |         |  192 bytes (1%) |           4 |
| `["gemm", "fusedmul", "xf", "8"]`                              |   2.688 ms (5%) |         |  192 bytes (1%) |           4 |
| `["gemm", "mul", "linalg", "256"]`                             |   1.121 ms (5%) |         |                 |             |
| `["gemm", "mul", "linalg", "32"]`                              |   4.143 μs (5%) |         |                 |             |
| `["gemm", "mul", "linalg", "8"]`                               | 323.556 ns (5%) |         |                 |             |
| `["gemm", "mul", "man", "false", "256"]`                       |   4.731 ms (5%) |         |                 |             |
| `["gemm", "mul", "man", "false", "32"]`                        |   8.433 μs (5%) |         |                 |             |
| `["gemm", "mul", "man", "false", "8"]`                         | 451.531 ns (5%) |         |                 |             |
| `["gemm", "mul", "man", "ivdep", "256"]`                       |   4.682 ms (5%) |         |                 |             |
| `["gemm", "mul", "man", "ivdep", "32"]`                        |   6.420 μs (5%) |         |                 |             |
| `["gemm", "mul", "man", "ivdep", "8"]`                         | 420.707 ns (5%) |         |                 |             |
| `["gemm", "mul", "man", "true", "256"]`                        |   4.727 ms (5%) |         |                 |             |
| `["gemm", "mul", "man", "true", "32"]`                         |   7.850 μs (5%) |         |                 |             |
| `["gemm", "mul", "man", "true", "8"]`                          | 501.563 ns (5%) |         |                 |             |
| `["gemm", "mul", "xf", "false", "256"]`                        |   4.734 ms (5%) |         |   80 bytes (1%) |           3 |
| `["gemm", "mul", "xf", "false", "32"]`                         |   8.433 μs (5%) |         |   80 bytes (1%) |           3 |
| `["gemm", "mul", "xf", "false", "8"]`                          | 545.789 ns (5%) |         |   80 bytes (1%) |           3 |
| `["gemm", "mul", "xf", "ivdep", "256"]`                        |   4.766 ms (5%) |         |   80 bytes (1%) |           3 |
| `["gemm", "mul", "xf", "ivdep", "32"]`                         |   6.580 μs (5%) |         |   80 bytes (1%) |           3 |
| `["gemm", "mul", "xf", "ivdep", "8"]`                          | 476.020 ns (5%) |         |   80 bytes (1%) |           3 |
| `["gemm", "mul", "xf", "true", "256"]`                         |   4.730 ms (5%) |         |   80 bytes (1%) |           3 |
| `["gemm", "mul", "xf", "true", "32"]`                          |   7.925 μs (5%) |         |   80 bytes (1%) |           3 |
| `["gemm", "mul", "xf", "true", "8"]`                           | 504.188 ns (5%) |         |   80 bytes (1%) |           3 |
| `["groupby", "sum", "sac"]`                                    | 153.600 μs (5%) |         |   1.53 KiB (1%) |          16 |
| `["groupby", "sum", "xf-with-init"]`                           | 158.200 μs (5%) |         |   1.20 KiB (1%) |           9 |
| `["groupby", "sum", "xf-without-init"]`                        | 162.101 μs (5%) |         |   1.20 KiB (1%) |           9 |
| `["mapcat_eduction", "base"]`                                  |   1.770 μs (5%) |         |                 |             |
| `["mapcat_eduction", "xf-eduction"]`                           |   2.289 μs (5%) |         |                 |             |
| `["mapcat_eduction", "xf-xf"]`                                 |   2.211 μs (5%) |         |                 |             |
| `["missing_argmax", "man"]`                                    |   1.210 μs (5%) |         |   32 bytes (1%) |           1 |
| `["missing_argmax", "rf"]`                                     |   1.580 μs (5%) |         |   32 bytes (1%) |           1 |
| `["missing_argmax", "xf"]`                                     |   1.640 μs (5%) |         |   32 bytes (1%) |           1 |
| `["missing_dot", "equiv"]`                                     |   2.278 μs (5%) |         |   16 bytes (1%) |           1 |
| `["missing_dot", "man"]`                                       |   1.440 μs (5%) |         |   16 bytes (1%) |           1 |
| `["missing_dot", "naive"]`                                     |   4.929 μs (5%) |         |   16 bytes (1%) |           1 |
| `["missing_dot", "rf"]`                                        |   1.380 μs (5%) |         |   16 bytes (1%) |           1 |
| `["missing_dot", "rf_nota"]`                                   |   2.030 μs (5%) |         |   16 bytes (1%) |           1 |
| `["missing_dot", "xf"]`                                        | 110.401 μs (5%) |         |  72.05 KiB (1%) |        3738 |
| `["missing_dot", "xf_nota"]`                                   | 108.100 μs (5%) |         |  72.16 KiB (1%) |        3742 |
| `["overhead", "foldl"]`                                        |   5.000 ns (5%) |         |                 |             |
| `["overhead", "reduce_basecase"]`                              | 278.571 ns (5%) |         |  368 bytes (1%) |           6 |
| `["partition_by", "man"]`                                      |   2.214 ms (5%) |         |  352 bytes (1%) |           4 |
| `["partition_by", "xf"]`                                       |   2.131 ms (5%) |         |  544 bytes (1%) |           6 |
| `["set", "base"]`                                              |   5.349 ms (5%) |         |  49.56 KiB (1%) |          17 |
| `["set", "xf"]`                                                |   5.020 ms (5%) |         |  49.59 KiB (1%) |          19 |
| `["sum_transpose", "30", "noinit", "iter"]`                    |   2.333 μs (5%) |         |                 |             |
| `["sum_transpose", "30", "noinit", "man"]`                     |   1.720 μs (5%) |         |                 |             |
| `["sum_transpose", "30", "noinit", "xf"]`                      |   1.050 μs (5%) |         |   32 bytes (1%) |           2 |
| `["sum_transpose", "30", "withinit", "iter"]`                  |   1.530 μs (5%) |         |                 |             |
| `["sum_transpose", "30", "withinit", "man"]`                   | 844.828 ns (5%) |         |                 |             |
| `["sum_transpose", "30", "withinit", "xf"]`                    | 960.000 ns (5%) |         |   48 bytes (1%) |           3 |
| `["teerf_filter", "noinit"]`                                   | 510.701 ns (5%) |         |  112 bytes (1%) |           4 |
| `["teerf_filter", "withinit"]`                                 | 276.978 ns (5%) |         |                 |             |

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
  uname: Linux 5.3.0-1035-azure #36-Ubuntu SMP Thu Aug 6 09:21:33 UTC 2020 x86_64 x86_64
  CPU: Intel(R) Xeon(R) CPU E5-2673 v4 @ 2.30GHz: 
              speed         user         nice          sys         idle          irq
       #1  2294 MHz       7689 s          0 s       1222 s      81426 s          0 s
       #2  2294 MHz      73450 s          0 s       1845 s      15360 s          0 s
       
  Memory: 6.764873504638672 GB (2900.2734375 MB free)
  Uptime: 925.0 sec
  Load Avg:  1.0068359375  1.0  0.7119140625
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-9.0.1 (ORCJIT, broadwell)
```

---
# Baseline result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmark: 3 Sep 2020 - 1:7
* Package commit: c8dada
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
| `["append!!", "eduction"]`                                     |  21.400 μs (5%) |         |  64.63 KiB (1%) |          13 |
| `["append!!", "xf"]`                                           |  21.000 μs (5%) |         |  64.63 KiB (1%) |          13 |
| `["cartesian", "copyto!", "iter"]`                             |   5.960 μs (5%) |         |                 |             |
| `["cartesian", "copyto!", "man"]`                              |   2.233 μs (5%) |         |                 |             |
| `["cartesian", "copyto!", "xf"]`                               |   2.778 μs (5%) |         |                 |             |
| `["cat", "base"]`                                              |   1.950 μs (5%) |         |                 |             |
| `["cat", "xf"]`                                                |   2.522 μs (5%) |         |                 |             |
| `["collect", "filter-missing"]`                                |  61.700 μs (5%) |         |  32.81 KiB (1%) |          14 |
| `["collect", "identity-float"]`                                |  33.400 μs (5%) |         | 256.66 KiB (1%) |          14 |
| `["collect", "identity-union"]`                                | 176.500 μs (5%) |         | 601.13 KiB (1%) |       10013 |
| `["dict", "base"]`                                             |   5.037 ms (5%) |         |  92.91 KiB (1%) |          22 |
| `["dict", "xf"]`                                               |   4.896 ms (5%) |         |  92.31 KiB (1%) |          18 |
| `["dot", "blas"]`                                              |   2.600 μs (5%) |         |                 |             |
| `["dot", "man"]`                                               |   2.567 μs (5%) |         |                 |             |
| `["dot", "rf"]`                                                |   3.563 μs (5%) |         |                 |             |
| `["dot", "xf"]`                                                |   3.663 μs (5%) |         |   64 bytes (1%) |           3 |
| `["filter_map_map!", "man"]`                                   |  74.501 μs (5%) |         |                 |             |
| `["filter_map_map!", "xf"]`                                    | 699.902 μs (5%) |         |   80 bytes (1%) |           3 |
| `["filter_map_reduce", "man"]`                                 | 233.900 μs (5%) |         |                 |             |
| `["filter_map_reduce", "xf"]`                                  | 242.000 μs (5%) |         |                 |             |
| `["filter_sum", "1000", "RandomFloats", "noinit", "base"]`     | 925.000 ns (5%) |         |                 |             |
| `["filter_sum", "1000", "RandomFloats", "noinit", "naive"]`    | 951.852 ns (5%) |         |                 |             |
| `["filter_sum", "1000", "RandomFloats", "noinit", "xf"]`       |   1.780 μs (5%) |         |                 |             |
| `["filter_sum", "1000", "RandomFloats", "withinit", "base"]`   |   1.840 μs (5%) |         |                 |             |
| `["filter_sum", "1000", "RandomFloats", "withinit", "naive"]`  | 960.000 ns (5%) |         |                 |             |
| `["filter_sum", "1000", "RandomFloats", "withinit", "xf"]`     |   1.840 μs (5%) |         |                 |             |
| `["filter_sum", "1000", "UnitRange", "noinit", "base"]`        |   2.000 μs (5%) |         |                 |             |
| `["filter_sum", "1000", "UnitRange", "noinit", "naive"]`       | 873.171 ns (5%) |         |                 |             |
| `["filter_sum", "1000", "UnitRange", "noinit", "xf"]`          | 204.952 ns (5%) |         |                 |             |
| `["filter_sum", "1000", "UnitRange", "withinit", "base"]`      | 195.726 ns (5%) |         |                 |             |
| `["filter_sum", "1000", "UnitRange", "withinit", "naive"]`     | 589.809 ns (5%) |         |                 |             |
| `["filter_sum", "1000", "UnitRange", "withinit", "xf"]`        | 204.419 ns (5%) |         |                 |             |
| `["filter_sum", "10000", "RandomFloats", "noinit", "base"]`    |  43.100 μs (5%) |         |                 |             |
| `["filter_sum", "10000", "RandomFloats", "noinit", "naive"]`   |  49.600 μs (5%) |         |                 |             |
| `["filter_sum", "10000", "RandomFloats", "noinit", "xf"]`      |  17.900 μs (5%) |         |                 |             |
| `["filter_sum", "10000", "RandomFloats", "withinit", "base"]`  |  19.300 μs (5%) |         |                 |             |
| `["filter_sum", "10000", "RandomFloats", "withinit", "naive"]` |  46.200 μs (5%) |         |                 |             |
| `["filter_sum", "10000", "RandomFloats", "withinit", "xf"]`    |  17.900 μs (5%) |         |                 |             |
| `["filter_sum", "10000", "UnitRange", "noinit", "base"]`       |  20.600 μs (5%) |         |                 |             |
| `["filter_sum", "10000", "UnitRange", "noinit", "naive"]`      |   9.300 μs (5%) |         |                 |             |
| `["filter_sum", "10000", "UnitRange", "noinit", "xf"]`         |   2.020 μs (5%) |         |                 |             |
| `["filter_sum", "10000", "UnitRange", "withinit", "base"]`     |   1.880 μs (5%) |         |                 |             |
| `["filter_sum", "10000", "UnitRange", "withinit", "naive"]`    |   5.700 μs (5%) |         |                 |             |
| `["filter_sum", "10000", "UnitRange", "withinit", "xf"]`       |   1.880 μs (5%) |         |                 |             |
| `["findall", "base"]`                                          | 957.202 μs (5%) |         |   2.00 MiB (1%) |          18 |
| `["findall", "xf-array"]`                                      | 882.902 μs (5%) |         |   3.02 MiB (1%) |       98829 |
| `["findall", "xf-iter"]`                                       | 359.301 μs (5%) |         |   2.00 MiB (1%) |          19 |
| `["gemm", "fusedmul", "blas", "16"]`                           |   5.854 ms (5%) |         |                 |             |
| `["gemm", "fusedmul", "blas", "2"]`                            |   4.112 ms (5%) |         |                 |             |
| `["gemm", "fusedmul", "blas", "32"]`                           |   8.498 ms (5%) |         |                 |             |
| `["gemm", "fusedmul", "blas", "8"]`                            |   4.350 ms (5%) |         |                 |             |
| `["gemm", "fusedmul", "xf", "16"]`                             |   5.602 ms (5%) |         |  192 bytes (1%) |           4 |
| `["gemm", "fusedmul", "xf", "2"]`                              | 669.902 μs (5%) |         |  192 bytes (1%) |           4 |
| `["gemm", "fusedmul", "xf", "32"]`                             |  11.371 ms (5%) |         |  192 bytes (1%) |           4 |
| `["gemm", "fusedmul", "xf", "8"]`                              |   2.685 ms (5%) |         |  192 bytes (1%) |           4 |
| `["gemm", "mul", "linalg", "256"]`                             |   1.119 ms (5%) |         |                 |             |
| `["gemm", "mul", "linalg", "32"]`                              |   4.100 μs (5%) |         |                 |             |
| `["gemm", "mul", "linalg", "8"]`                               | 300.000 ns (5%) |         |                 |             |
| `["gemm", "mul", "man", "false", "256"]`                       |   4.794 ms (5%) |         |                 |             |
| `["gemm", "mul", "man", "false", "32"]`                        |   8.400 μs (5%) |         |                 |             |
| `["gemm", "mul", "man", "false", "8"]`                         | 500.000 ns (5%) |         |                 |             |
| `["gemm", "mul", "man", "ivdep", "256"]`                       |   4.773 ms (5%) |         |                 |             |
| `["gemm", "mul", "man", "ivdep", "32"]`                        |   6.400 μs (5%) |         |                 |             |
| `["gemm", "mul", "man", "ivdep", "8"]`                         | 500.000 ns (5%) |         |                 |             |
| `["gemm", "mul", "man", "true", "256"]`                        |   4.806 ms (5%) |         |                 |             |
| `["gemm", "mul", "man", "true", "32"]`                         |   7.800 μs (5%) |         |                 |             |
| `["gemm", "mul", "man", "true", "8"]`                          | 500.000 ns (5%) |         |                 |             |
| `["gemm", "mul", "xf", "false", "256"]`                        |   4.804 ms (5%) |         |   80 bytes (1%) |           3 |
| `["gemm", "mul", "xf", "false", "32"]`                         |   8.400 μs (5%) |         |   80 bytes (1%) |           3 |
| `["gemm", "mul", "xf", "false", "8"]`                          | 600.000 ns (5%) |         |   80 bytes (1%) |           3 |
| `["gemm", "mul", "xf", "ivdep", "256"]`                        |   4.786 ms (5%) |         |   80 bytes (1%) |           3 |
| `["gemm", "mul", "xf", "ivdep", "32"]`                         |   6.600 μs (5%) |         |   80 bytes (1%) |           3 |
| `["gemm", "mul", "xf", "ivdep", "8"]`                          | 500.000 ns (5%) |         |   80 bytes (1%) |           3 |
| `["gemm", "mul", "xf", "true", "256"]`                         |   4.806 ms (5%) |         |   80 bytes (1%) |           3 |
| `["gemm", "mul", "xf", "true", "32"]`                          |   7.900 μs (5%) |         |   80 bytes (1%) |           3 |
| `["gemm", "mul", "xf", "true", "8"]`                           | 600.000 ns (5%) |         |   80 bytes (1%) |           3 |
| `["groupby", "sum", "sac"]`                                    | 200.901 μs (5%) |         |  624 bytes (1%) |           5 |
| `["groupby", "sum", "xf-with-init"]`                           | 166.901 μs (5%) |         |   1.20 KiB (1%) |           9 |
| `["groupby", "sum", "xf-without-init"]`                        | 163.800 μs (5%) |         |   1.20 KiB (1%) |           9 |
| `["mapcat_eduction", "base"]`                                  |   1.830 μs (5%) |         |                 |             |
| `["mapcat_eduction", "xf-eduction"]`                           |   2.289 μs (5%) |         |                 |             |
| `["mapcat_eduction", "xf-xf"]`                                 |   2.211 μs (5%) |         |                 |             |
| `["missing_argmax", "man"]`                                    |   1.240 μs (5%) |         |   32 bytes (1%) |           1 |
| `["missing_argmax", "rf"]`                                     |   1.620 μs (5%) |         |   32 bytes (1%) |           1 |
| `["missing_argmax", "xf"]`                                     |   1.640 μs (5%) |         |   32 bytes (1%) |           1 |
| `["missing_dot", "equiv"]`                                     |   2.200 μs (5%) |         |   16 bytes (1%) |           1 |
| `["missing_dot", "man"]`                                       |   1.450 μs (5%) |         |   16 bytes (1%) |           1 |
| `["missing_dot", "naive"]`                                     |   5.129 μs (5%) |         |   16 bytes (1%) |           1 |
| `["missing_dot", "rf"]`                                        |   1.430 μs (5%) |         |   16 bytes (1%) |           1 |
| `["missing_dot", "rf_nota"]`                                   |   2.320 μs (5%) |         |   16 bytes (1%) |           1 |
| `["missing_dot", "xf"]`                                        | 112.600 μs (5%) |         |  71.86 KiB (1%) |        3730 |
| `["missing_dot", "xf_nota"]`                                   | 118.300 μs (5%) |         |  72.16 KiB (1%) |        3742 |
| `["overhead", "foldl"]`                                        |   5.000 ns (5%) |         |                 |             |
| `["overhead", "reduce_basecase"]`                              | 292.857 ns (5%) |         |  368 bytes (1%) |           6 |
| `["partition_by", "man"]`                                      |   2.227 ms (5%) |         |  352 bytes (1%) |           4 |
| `["partition_by", "xf"]`                                       |   2.191 ms (5%) |         |  544 bytes (1%) |           6 |
| `["set", "base"]`                                              |   5.507 ms (5%) |         |  49.56 KiB (1%) |          17 |
| `["set", "xf"]`                                                |   5.328 ms (5%) |         |  49.59 KiB (1%) |          19 |
| `["sum_transpose", "30", "noinit", "iter"]`                    |   2.400 μs (5%) |         |                 |             |
| `["sum_transpose", "30", "noinit", "man"]`                     |   1.710 μs (5%) |         |                 |             |
| `["sum_transpose", "30", "noinit", "xf"]`                      |   1.060 μs (5%) |         |   32 bytes (1%) |           2 |
| `["sum_transpose", "30", "withinit", "iter"]`                  |   1.640 μs (5%) |         |                 |             |
| `["sum_transpose", "30", "withinit", "man"]`                   | 937.931 ns (5%) |         |                 |             |
| `["sum_transpose", "30", "withinit", "xf"]`                    |   1.000 μs (5%) |         |   48 bytes (1%) |           3 |
| `["teerf_filter", "noinit"]`                                   | 550.802 ns (5%) |         |  112 bytes (1%) |           4 |
| `["teerf_filter", "withinit"]`                                 | 294.604 ns (5%) |         |                 |             |

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
  uname: Linux 5.3.0-1035-azure #36-Ubuntu SMP Thu Aug 6 09:21:33 UTC 2020 x86_64 x86_64
  CPU: Intel(R) Xeon(R) CPU E5-2673 v4 @ 2.30GHz: 
              speed         user         nice          sys         idle          irq
       #1  2294 MHz      11265 s          0 s       1397 s     113018 s          0 s
       #2  2294 MHz     104873 s          0 s       2107 s      18991 s          0 s
       
  Memory: 6.764873504638672 GB (2866.52734375 MB free)
  Uptime: 1280.0 sec
  Load Avg:  1.0009765625  1.009765625  0.82666015625
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-9.0.1 (ORCJIT, broadwell)
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
    Model:               79
    Model name:          Intel(R) Xeon(R) CPU E5-2673 v4 @ 2.30GHz
    Stepping:            1
    CPU MHz:             2294.684
    BogoMIPS:            4589.36
    Hypervisor vendor:   Microsoft
    Virtualization type: full
    L1d cache:           32K
    L1i cache:           32K
    L2 cache:            256K
    L3 cache:            51200K
    NUMA node0 CPU(s):   0,1
    Flags:               fpu vme de pse tsc msr pae mce cx8 apic sep mtrr pge mca cmov pat pse36 clflush mmx fxsr sse sse2 ss ht syscall nx pdpe1gb rdtscp lm constant_tsc rep_good nopl xtopology cpuid pni pclmulqdq ssse3 fma cx16 pcid sse4_1 sse4_2 movbe popcnt aes xsave avx f16c rdrand hypervisor lahf_lm abm 3dnowprefetch invpcid_single pti fsgsbase bmi1 hle avx2 smep bmi2 erms invpcid rtm rdseed adx smap xsaveopt md_clear
    

| Cpu Property       | Value                                                   |
|:------------------ |:------------------------------------------------------- |
| Brand              | Intel(R) Xeon(R) CPU E5-2673 v4 @ 2.30GHz               |
| Vendor             | :Intel                                                  |
| Architecture       | :Broadwell                                              |
| Model              | Family: 0x06, Model: 0x4f, Stepping: 0x01, Type: 0x00   |
| Cores              | 2 physical cores, 2 logical cores (on executing CPU)    |
|                    | No Hyperthreading detected                              |
| Clock Frequencies  | Not supported by CPU                                    |
| Data Cache         | Level 1:3 : (32, 256, 51200) kbytes                     |
|                    | 64 byte cache line size                                 |
| Address Size       | 48 bits virtual, 44 bits physical                       |
| SIMD               | 256 bit = 32 byte max. SIMD vector size                 |
| Time Stamp Counter | TSC is accessible via `rdtsc`                           |
|                    | TSC increased at every clock cycle (non-invariant TSC)  |
| Perf. Monitoring   | Performance Monitoring Counters (PMC) are not supported |
| Hypervisor         | Yes, Microsoft                                          |

