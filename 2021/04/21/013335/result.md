# Benchmark result

* Pull request commit: [`e2f63c04a26913dee5eb3d8defd415aad2f38387`](https://github.com/JuliaFolds/Transducers.jl/commit/e2f63c04a26913dee5eb3d8defd415aad2f38387)
* Pull request: <https://github.com/JuliaFolds/Transducers.jl/pull/243> (Update */Manifest.toml)

# Judge result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmarks:
    - Target: 21 Apr 2021 - 01:26
    - Baseline: 21 Apr 2021 - 01:32
* Package commits:
    - Target: 420a7d
    - Baseline: 2cc4af
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
| `["append!!", "eduction"]`                                     |                1.09 (5%) :x: |    1.00 (1%)  |
| `["cat", "xf"]`                                                |                1.08 (5%) :x: |    1.00 (1%)  |
| `["dot", "man"]`                                               |                1.06 (5%) :x: |    1.00 (1%)  |
| `["filter_map_map!", "xf"]`                                    | 0.94 (5%) :white_check_mark: |    1.00 (1%)  |
| `["filter_sum", "1000", "RandomFloats", "noinit", "base"]`     | 0.85 (5%) :white_check_mark: |    1.00 (1%)  |
| `["filter_sum", "1000", "RandomFloats", "noinit", "naive"]`    | 0.93 (5%) :white_check_mark: |    1.00 (1%)  |
| `["filter_sum", "1000", "RandomFloats", "withinit", "naive"]`  | 0.87 (5%) :white_check_mark: |    1.00 (1%)  |
| `["filter_sum", "1000", "UnitRange", "noinit", "base"]`        |                1.07 (5%) :x: |    1.00 (1%)  |
| `["filter_sum", "1000", "UnitRange", "noinit", "xf"]`          |                1.07 (5%) :x: |    1.00 (1%)  |
| `["filter_sum", "10000", "UnitRange", "withinit", "naive"]`    | 0.95 (5%) :white_check_mark: |    1.00 (1%)  |
| `["findall", "base"]`                                          |                1.09 (5%) :x: |    1.00 (1%)  |
| `["gemm", "mul", "linalg", "8"]`                               |                1.08 (5%) :x: |    1.00 (1%)  |
| `["gemm", "mul", "man", "ivdep", "8"]`                         | 0.91 (5%) :white_check_mark: |    1.00 (1%)  |
| `["gemm", "mul", "man", "true", "8"]`                          | 0.94 (5%) :white_check_mark: |    1.00 (1%)  |
| `["gemm", "mul", "xf", "false", "8"]`                          | 0.74 (5%) :white_check_mark: |    1.00 (1%)  |
| `["groupby", "sum", "sac"]`                                    |                   0.98 (5%)  | 2.10 (1%) :x: |
| `["mapcat_eduction", "base"]`                                  | 0.93 (5%) :white_check_mark: |    1.00 (1%)  |
| `["missing_argmax", "xf"]`                                     |                1.06 (5%) :x: |    1.00 (1%)  |
| `["missing_dot", "equiv"]`                                     | 0.90 (5%) :white_check_mark: |    1.00 (1%)  |
| `["missing_dot", "man"]`                                       | 0.94 (5%) :white_check_mark: |    1.00 (1%)  |
| `["set", "base"]`                                              |                1.06 (5%) :x: |    1.00 (1%)  |
| `["set", "xf"]`                                                |                1.06 (5%) :x: |    1.00 (1%)  |

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
      Ubuntu 20.04.2 LTS
  uname: Linux 5.4.0-1043-azure #45-Ubuntu SMP Fri Mar 19 17:33:38 UTC 2021 x86_64 x86_64
  CPU: Intel(R) Xeon(R) CPU E5-2673 v4 @ 2.30GHz: 
              speed         user         nice          sys         idle          irq
       #1  2294 MHz       8953 s         17 s       1302 s     101121 s          0 s
       #2  2294 MHz      75647 s          8 s       1841 s      34106 s          0 s
       
  Memory: 6.791343688964844 GB (3541.890625 MB free)
  Uptime: 1121.0 sec
  Load Avg:  1.1171875  1.01611328125  0.68798828125
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-9.0.1 (ORCJIT, broadwell)
```

### Baseline
```
Julia Version 1.5.4
Commit 69fcb5745b (2021-03-11 19:13 UTC)
Platform Info:
  OS: Linux (x86_64-pc-linux-gnu)
      Ubuntu 20.04.2 LTS
  uname: Linux 5.4.0-1043-azure #45-Ubuntu SMP Fri Mar 19 17:33:38 UTC 2021 x86_64 x86_64
  CPU: Intel(R) Xeon(R) CPU E5-2673 v4 @ 2.30GHz: 
              speed         user         nice          sys         idle          irq
       #1  2294 MHz      11666 s         17 s       1485 s     132977 s          0 s
       #2  2294 MHz     107485 s          8 s       2086 s      36856 s          0 s
       
  Memory: 6.791343688964844 GB (3462.7265625 MB free)
  Uptime: 1470.0 sec
  Load Avg:  1.0  1.005859375  0.80712890625
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-9.0.1 (ORCJIT, broadwell)
```

---
# Target result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmark: 21 Apr 2021 - 1:26
* Package commit: 420a7d
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
| `["append!!", "eduction"]`                                     |  19.801 μs (5%) |         |  64.63 KiB (1%) |          13 |
| `["append!!", "xf"]`                                           |  19.300 μs (5%) |         |  64.63 KiB (1%) |          13 |
| `["cartesian", "copyto!", "iter"]`                             |   5.767 μs (5%) |         |                 |             |
| `["cartesian", "copyto!", "man"]`                              |   2.211 μs (5%) |         |                 |             |
| `["cartesian", "copyto!", "xf"]`                               |   2.633 μs (5%) |         |                 |             |
| `["cat", "base"]`                                              |   1.830 μs (5%) |         |                 |             |
| `["cat", "xf"]`                                                |   2.533 μs (5%) |         |                 |             |
| `["collect", "filter-missing"]`                                |  57.801 μs (5%) |         |  32.81 KiB (1%) |          14 |
| `["collect", "identity-float"]`                                |  27.200 μs (5%) |         | 256.66 KiB (1%) |          14 |
| `["collect", "identity-union"]`                                | 158.102 μs (5%) |         | 601.16 KiB (1%) |       10014 |
| `["dict", "base"]`                                             |   4.948 ms (5%) |         |  92.91 KiB (1%) |          22 |
| `["dict", "xf"]`                                               |   4.821 ms (5%) |         |  92.31 KiB (1%) |          18 |
| `["dot", "blas"]`                                              |   2.467 μs (5%) |         |                 |             |
| `["dot", "man"]`                                               |   2.578 μs (5%) |         |                 |             |
| `["dot", "rf"]`                                                |   3.563 μs (5%) |         |                 |             |
| `["dot", "xf"]`                                                |   3.663 μs (5%) |         |   64 bytes (1%) |           3 |
| `["filter_map_map!", "man"]`                                   |  73.701 μs (5%) |         |                 |             |
| `["filter_map_map!", "xf"]`                                    | 650.308 μs (5%) |         |   80 bytes (1%) |           3 |
| `["filter_map_reduce", "man"]`                                 | 226.503 μs (5%) |         |                 |             |
| `["filter_map_reduce", "xf"]`                                  | 233.902 μs (5%) |         |                 |             |
| `["filter_sum", "1000", "RandomFloats", "noinit", "base"]`     | 876.316 ns (5%) |         |                 |             |
| `["filter_sum", "1000", "RandomFloats", "noinit", "naive"]`    |   1.200 μs (5%) |         |                 |             |
| `["filter_sum", "1000", "RandomFloats", "noinit", "xf"]`       |   1.670 μs (5%) |         |                 |             |
| `["filter_sum", "1000", "RandomFloats", "withinit", "base"]`   |   1.660 μs (5%) |         |                 |             |
| `["filter_sum", "1000", "RandomFloats", "withinit", "naive"]`  | 909.121 ns (5%) |         |                 |             |
| `["filter_sum", "1000", "RandomFloats", "withinit", "xf"]`     |   1.720 μs (5%) |         |                 |             |
| `["filter_sum", "1000", "UnitRange", "noinit", "base"]`        |   1.930 μs (5%) |         |                 |             |
| `["filter_sum", "1000", "UnitRange", "noinit", "naive"]`       | 843.655 ns (5%) |         |                 |             |
| `["filter_sum", "1000", "UnitRange", "noinit", "xf"]`          | 198.774 ns (5%) |         |                 |             |
| `["filter_sum", "1000", "UnitRange", "withinit", "base"]`      | 186.840 ns (5%) |         |                 |             |
| `["filter_sum", "1000", "UnitRange", "withinit", "naive"]`     | 623.127 ns (5%) |         |                 |             |
| `["filter_sum", "1000", "UnitRange", "withinit", "xf"]`        | 190.830 ns (5%) |         |                 |             |
| `["filter_sum", "10000", "RandomFloats", "noinit", "base"]`    |  39.401 μs (5%) |         |                 |             |
| `["filter_sum", "10000", "RandomFloats", "noinit", "naive"]`   |  45.200 μs (5%) |         |                 |             |
| `["filter_sum", "10000", "RandomFloats", "noinit", "xf"]`      |  16.200 μs (5%) |         |                 |             |
| `["filter_sum", "10000", "RandomFloats", "withinit", "base"]`  |  16.700 μs (5%) |         |                 |             |
| `["filter_sum", "10000", "RandomFloats", "withinit", "naive"]` |  44.100 μs (5%) |         |                 |             |
| `["filter_sum", "10000", "RandomFloats", "withinit", "xf"]`    |  16.200 μs (5%) |         |                 |             |
| `["filter_sum", "10000", "UnitRange", "noinit", "base"]`       |  18.500 μs (5%) |         |                 |             |
| `["filter_sum", "10000", "UnitRange", "noinit", "naive"]`      |   8.367 μs (5%) |         |                 |             |
| `["filter_sum", "10000", "UnitRange", "noinit", "xf"]`         |   1.810 μs (5%) |         |                 |             |
| `["filter_sum", "10000", "UnitRange", "withinit", "base"]`     |   1.750 μs (5%) |         |                 |             |
| `["filter_sum", "10000", "UnitRange", "withinit", "naive"]`    |   5.640 μs (5%) |         |                 |             |
| `["filter_sum", "10000", "UnitRange", "withinit", "xf"]`       |   1.720 μs (5%) |         |                 |             |
| `["findall", "base"]`                                          | 940.911 μs (5%) |         |   2.00 MiB (1%) |          18 |
| `["findall", "xf-array"]`                                      | 868.710 μs (5%) |         |   3.02 MiB (1%) |       98829 |
| `["findall", "xf-iter"]`                                       | 326.504 μs (5%) |         |   2.00 MiB (1%) |          19 |
| `["gemm", "fusedmul", "blas", "16"]`                           |   5.418 ms (5%) |         |                 |             |
| `["gemm", "fusedmul", "blas", "2"]`                            |   4.000 ms (5%) |         |                 |             |
| `["gemm", "fusedmul", "blas", "32"]`                           |   7.155 ms (5%) |         |                 |             |
| `["gemm", "fusedmul", "blas", "8"]`                            |   4.144 ms (5%) |         |                 |             |
| `["gemm", "fusedmul", "xf", "16"]`                             |   5.362 ms (5%) |         |  192 bytes (1%) |           4 |
| `["gemm", "fusedmul", "xf", "2"]`                              | 669.808 μs (5%) |         |  192 bytes (1%) |           4 |
| `["gemm", "fusedmul", "xf", "32"]`                             |  10.786 ms (5%) |         |  192 bytes (1%) |           4 |
| `["gemm", "fusedmul", "xf", "8"]`                              |   2.674 ms (5%) |         |  192 bytes (1%) |           4 |
| `["gemm", "mul", "linalg", "256"]`                             |   1.118 ms (5%) |         |                 |             |
| `["gemm", "mul", "linalg", "32"]`                              |   4.129 μs (5%) |         |                 |             |
| `["gemm", "mul", "linalg", "8"]`                               | 324.153 ns (5%) |         |                 |             |
| `["gemm", "mul", "man", "false", "256"]`                       |   4.735 ms (5%) |         |                 |             |
| `["gemm", "mul", "man", "false", "32"]`                        |   8.633 μs (5%) |         |                 |             |
| `["gemm", "mul", "man", "false", "8"]`                         | 489.068 ns (5%) |         |                 |             |
| `["gemm", "mul", "man", "ivdep", "256"]`                       |   4.669 ms (5%) |         |                 |             |
| `["gemm", "mul", "man", "ivdep", "32"]`                        |   6.400 μs (5%) |         |                 |             |
| `["gemm", "mul", "man", "ivdep", "8"]`                         | 454.592 ns (5%) |         |                 |             |
| `["gemm", "mul", "man", "true", "256"]`                        |   4.704 ms (5%) |         |                 |             |
| `["gemm", "mul", "man", "true", "32"]`                         |   7.950 μs (5%) |         |                 |             |
| `["gemm", "mul", "man", "true", "8"]`                          | 376.005 ns (5%) |         |                 |             |
| `["gemm", "mul", "xf", "false", "256"]`                        |   4.753 ms (5%) |         |   80 bytes (1%) |           3 |
| `["gemm", "mul", "xf", "false", "32"]`                         |   8.667 μs (5%) |         |   80 bytes (1%) |           3 |
| `["gemm", "mul", "xf", "false", "8"]`                          | 444.335 ns (5%) |         |   80 bytes (1%) |           3 |
| `["gemm", "mul", "xf", "ivdep", "256"]`                        |   4.752 ms (5%) |         |   80 bytes (1%) |           3 |
| `["gemm", "mul", "xf", "ivdep", "32"]`                         |   6.500 μs (5%) |         |   80 bytes (1%) |           3 |
| `["gemm", "mul", "xf", "ivdep", "8"]`                          | 522.518 ns (5%) |         |   80 bytes (1%) |           3 |
| `["gemm", "mul", "xf", "true", "256"]`                         |   4.733 ms (5%) |         |   80 bytes (1%) |           3 |
| `["gemm", "mul", "xf", "true", "32"]`                          |   8.167 μs (5%) |         |   80 bytes (1%) |           3 |
| `["gemm", "mul", "xf", "true", "8"]`                           | 493.163 ns (5%) |         |   80 bytes (1%) |           3 |
| `["groupby", "sum", "sac"]`                                    | 187.002 μs (5%) |         |   1.28 KiB (1%) |          14 |
| `["groupby", "sum", "xf-with-init"]`                           | 151.201 μs (5%) |         |   1.20 KiB (1%) |           9 |
| `["groupby", "sum", "xf-without-init"]`                        | 152.202 μs (5%) |         |   1.20 KiB (1%) |           9 |
| `["mapcat_eduction", "base"]`                                  |   1.710 μs (5%) |         |                 |             |
| `["mapcat_eduction", "xf-eduction"]`                           |   2.122 μs (5%) |         |                 |             |
| `["mapcat_eduction", "xf-xf"]`                                 |   2.122 μs (5%) |         |                 |             |
| `["missing_argmax", "man"]`                                    |   1.170 μs (5%) |         |   32 bytes (1%) |           1 |
| `["missing_argmax", "rf"]`                                     |   1.440 μs (5%) |         |   32 bytes (1%) |           1 |
| `["missing_argmax", "xf"]`                                     |   1.530 μs (5%) |         |   32 bytes (1%) |           1 |
| `["missing_dot", "equiv"]`                                     |   1.980 μs (5%) |         |   16 bytes (1%) |           1 |
| `["missing_dot", "man"]`                                       |   1.330 μs (5%) |         |   16 bytes (1%) |           1 |
| `["missing_dot", "naive"]`                                     |   4.772 μs (5%) |         |   16 bytes (1%) |           1 |
| `["missing_dot", "rf"]`                                        |   1.350 μs (5%) |         |   16 bytes (1%) |           1 |
| `["missing_dot", "rf_nota"]`                                   |   2.156 μs (5%) |         |   16 bytes (1%) |           1 |
| `["missing_dot", "xf"]`                                        | 102.201 μs (5%) |         |  72.25 KiB (1%) |        3746 |
| `["missing_dot", "xf_nota"]`                                   | 102.901 μs (5%) |         |  72.06 KiB (1%) |        3738 |
| `["overhead", "foldl"]`                                        |   4.700 ns (5%) |         |                 |             |
| `["overhead", "reduce_basecase"]`                              | 155.917 ns (5%) |         |   48 bytes (1%) |           2 |
| `["partition_by", "man"]`                                      |   2.164 ms (5%) |         |  352 bytes (1%) |           4 |
| `["partition_by", "xf"]`                                       |   2.210 ms (5%) |         |  544 bytes (1%) |           6 |
| `["set", "base"]`                                              |   6.158 ms (5%) |         |  49.56 KiB (1%) |          17 |
| `["set", "xf"]`                                                |   6.071 ms (5%) |         |  49.59 KiB (1%) |          19 |
| `["sum_transpose", "30", "noinit", "iter"]`                    |   2.244 μs (5%) |         |                 |             |
| `["sum_transpose", "30", "noinit", "man"]`                     |   1.610 μs (5%) |         |                 |             |
| `["sum_transpose", "30", "noinit", "xf"]`                      |   1.021 μs (5%) |         |   32 bytes (1%) |           2 |
| `["sum_transpose", "30", "withinit", "iter"]`                  |   1.570 μs (5%) |         |                 |             |
| `["sum_transpose", "30", "withinit", "man"]`                   | 875.634 ns (5%) |         |                 |             |
| `["sum_transpose", "30", "withinit", "xf"]`                    | 933.333 ns (5%) |         |   48 bytes (1%) |           3 |
| `["teerf_filter", "noinit"]`                                   |   2.278 μs (5%) |         |  192 bytes (1%) |           8 |
| `["teerf_filter", "withinit"]`                                 | 274.921 ns (5%) |         |                 |             |

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
      Ubuntu 20.04.2 LTS
  uname: Linux 5.4.0-1043-azure #45-Ubuntu SMP Fri Mar 19 17:33:38 UTC 2021 x86_64 x86_64
  CPU: Intel(R) Xeon(R) CPU E5-2673 v4 @ 2.30GHz: 
              speed         user         nice          sys         idle          irq
       #1  2294 MHz       8953 s         17 s       1302 s     101121 s          0 s
       #2  2294 MHz      75647 s          8 s       1841 s      34106 s          0 s
       
  Memory: 6.791343688964844 GB (3541.890625 MB free)
  Uptime: 1121.0 sec
  Load Avg:  1.1171875  1.01611328125  0.68798828125
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-9.0.1 (ORCJIT, broadwell)
```

---
# Baseline result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmark: 21 Apr 2021 - 1:32
* Package commit: 2cc4af
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
| `["append!!", "eduction"]`                                     |  18.200 μs (5%) |         |  64.63 KiB (1%) |          13 |
| `["append!!", "xf"]`                                           |  18.600 μs (5%) |         |  64.63 KiB (1%) |          13 |
| `["cartesian", "copyto!", "iter"]`                             |   5.950 μs (5%) |         |                 |             |
| `["cartesian", "copyto!", "man"]`                              |   2.144 μs (5%) |         |                 |             |
| `["cartesian", "copyto!", "xf"]`                               |   2.700 μs (5%) |         |                 |             |
| `["cat", "base"]`                                              |   1.830 μs (5%) |         |                 |             |
| `["cat", "xf"]`                                                |   2.356 μs (5%) |         |                 |             |
| `["collect", "filter-missing"]`                                |  56.701 μs (5%) |         |  32.81 KiB (1%) |          14 |
| `["collect", "identity-float"]`                                |  27.800 μs (5%) |         | 256.66 KiB (1%) |          14 |
| `["collect", "identity-union"]`                                | 156.802 μs (5%) |         | 601.07 KiB (1%) |       10014 |
| `["dict", "base"]`                                             |   5.044 ms (5%) |         |  92.91 KiB (1%) |          22 |
| `["dict", "xf"]`                                               |   4.957 ms (5%) |         |  92.31 KiB (1%) |          18 |
| `["dot", "blas"]`                                              |   2.478 μs (5%) |         |                 |             |
| `["dot", "man"]`                                               |   2.422 μs (5%) |         |                 |             |
| `["dot", "rf"]`                                                |   3.550 μs (5%) |         |                 |             |
| `["dot", "xf"]`                                                |   3.663 μs (5%) |         |   64 bytes (1%) |           3 |
| `["filter_map_map!", "man"]`                                   |  75.301 μs (5%) |         |                 |             |
| `["filter_map_map!", "xf"]`                                    | 689.809 μs (5%) |         |   80 bytes (1%) |           3 |
| `["filter_map_reduce", "man"]`                                 | 233.902 μs (5%) |         |                 |             |
| `["filter_map_reduce", "xf"]`                                  | 233.902 μs (5%) |         |                 |             |
| `["filter_sum", "1000", "RandomFloats", "noinit", "base"]`     |   1.029 μs (5%) |         |                 |             |
| `["filter_sum", "1000", "RandomFloats", "noinit", "naive"]`    |   1.290 μs (5%) |         |                 |             |
| `["filter_sum", "1000", "RandomFloats", "noinit", "xf"]`       |   1.610 μs (5%) |         |                 |             |
| `["filter_sum", "1000", "RandomFloats", "withinit", "base"]`   |   1.720 μs (5%) |         |                 |             |
| `["filter_sum", "1000", "RandomFloats", "withinit", "naive"]`  |   1.048 μs (5%) |         |                 |             |
| `["filter_sum", "1000", "RandomFloats", "withinit", "xf"]`     |   1.720 μs (5%) |         |                 |             |
| `["filter_sum", "1000", "UnitRange", "noinit", "base"]`        |   1.800 μs (5%) |         |                 |             |
| `["filter_sum", "1000", "UnitRange", "noinit", "naive"]`       | 823.636 ns (5%) |         |                 |             |
| `["filter_sum", "1000", "UnitRange", "noinit", "xf"]`          | 185.440 ns (5%) |         |                 |             |
| `["filter_sum", "1000", "UnitRange", "withinit", "base"]`      | 186.688 ns (5%) |         |                 |             |
| `["filter_sum", "1000", "UnitRange", "withinit", "naive"]`     | 623.127 ns (5%) |         |                 |             |
| `["filter_sum", "1000", "UnitRange", "withinit", "xf"]`        | 190.830 ns (5%) |         |                 |             |
| `["filter_sum", "10000", "RandomFloats", "noinit", "base"]`    |  39.001 μs (5%) |         |                 |             |
| `["filter_sum", "10000", "RandomFloats", "noinit", "naive"]`   |  43.201 μs (5%) |         |                 |             |
| `["filter_sum", "10000", "RandomFloats", "noinit", "xf"]`      |  16.700 μs (5%) |         |                 |             |
| `["filter_sum", "10000", "RandomFloats", "withinit", "base"]`  |  16.200 μs (5%) |         |                 |             |
| `["filter_sum", "10000", "RandomFloats", "withinit", "naive"]` |  43.401 μs (5%) |         |                 |             |
| `["filter_sum", "10000", "RandomFloats", "withinit", "xf"]`    |  16.700 μs (5%) |         |                 |             |
| `["filter_sum", "10000", "UnitRange", "noinit", "base"]`       |  19.100 μs (5%) |         |                 |             |
| `["filter_sum", "10000", "UnitRange", "noinit", "naive"]`      |   8.367 μs (5%) |         |                 |             |
| `["filter_sum", "10000", "UnitRange", "noinit", "xf"]`         |   1.820 μs (5%) |         |                 |             |
| `["filter_sum", "10000", "UnitRange", "withinit", "base"]`     |   1.690 μs (5%) |         |                 |             |
| `["filter_sum", "10000", "UnitRange", "withinit", "naive"]`    |   5.960 μs (5%) |         |                 |             |
| `["filter_sum", "10000", "UnitRange", "withinit", "xf"]`       |   1.810 μs (5%) |         |                 |             |
| `["findall", "base"]`                                          | 862.610 μs (5%) |         |   2.00 MiB (1%) |          18 |
| `["findall", "xf-array"]`                                      | 843.510 μs (5%) |         |   3.02 MiB (1%) |       98829 |
| `["findall", "xf-iter"]`                                       | 333.304 μs (5%) |         |   2.00 MiB (1%) |          19 |
| `["gemm", "fusedmul", "blas", "16"]`                           |   5.405 ms (5%) |         |                 |             |
| `["gemm", "fusedmul", "blas", "2"]`                            |   4.011 ms (5%) |         |                 |             |
| `["gemm", "fusedmul", "blas", "32"]`                           |   7.181 ms (5%) |         |                 |             |
| `["gemm", "fusedmul", "blas", "8"]`                            |   4.149 ms (5%) |         |                 |             |
| `["gemm", "fusedmul", "xf", "16"]`                             |   5.376 ms (5%) |         |  192 bytes (1%) |           4 |
| `["gemm", "fusedmul", "xf", "2"]`                              | 695.608 μs (5%) |         |  192 bytes (1%) |           4 |
| `["gemm", "fusedmul", "xf", "32"]`                             |  10.838 ms (5%) |         |  192 bytes (1%) |           4 |
| `["gemm", "fusedmul", "xf", "8"]`                              |   2.679 ms (5%) |         |  192 bytes (1%) |           4 |
| `["gemm", "mul", "linalg", "256"]`                             |   1.123 ms (5%) |         |                 |             |
| `["gemm", "mul", "linalg", "32"]`                              |   4.100 μs (5%) |         |                 |             |
| `["gemm", "mul", "linalg", "8"]`                               | 300.000 ns (5%) |         |                 |             |
| `["gemm", "mul", "man", "false", "256"]`                       |   4.793 ms (5%) |         |                 |             |
| `["gemm", "mul", "man", "false", "32"]`                        |   8.400 μs (5%) |         |                 |             |
| `["gemm", "mul", "man", "false", "8"]`                         | 500.000 ns (5%) |         |                 |             |
| `["gemm", "mul", "man", "ivdep", "256"]`                       |   4.748 ms (5%) |         |                 |             |
| `["gemm", "mul", "man", "ivdep", "32"]`                        |   6.400 μs (5%) |         |                 |             |
| `["gemm", "mul", "man", "ivdep", "8"]`                         | 500.000 ns (5%) |         |                 |             |
| `["gemm", "mul", "man", "true", "256"]`                        |   4.775 ms (5%) |         |                 |             |
| `["gemm", "mul", "man", "true", "32"]`                         |   7.800 μs (5%) |         |                 |             |
| `["gemm", "mul", "man", "true", "8"]`                          | 400.000 ns (5%) |         |                 |             |
| `["gemm", "mul", "xf", "false", "256"]`                        |   4.794 ms (5%) |         |   80 bytes (1%) |           3 |
| `["gemm", "mul", "xf", "false", "32"]`                         |   8.400 μs (5%) |         |   80 bytes (1%) |           3 |
| `["gemm", "mul", "xf", "false", "8"]`                          | 600.000 ns (5%) |         |   80 bytes (1%) |           3 |
| `["gemm", "mul", "xf", "ivdep", "256"]`                        |   4.768 ms (5%) |         |   80 bytes (1%) |           3 |
| `["gemm", "mul", "xf", "ivdep", "32"]`                         |   6.500 μs (5%) |         |   80 bytes (1%) |           3 |
| `["gemm", "mul", "xf", "ivdep", "8"]`                          | 500.000 ns (5%) |         |   80 bytes (1%) |           3 |
| `["gemm", "mul", "xf", "true", "256"]`                         |   4.845 ms (5%) |         |   80 bytes (1%) |           3 |
| `["gemm", "mul", "xf", "true", "32"]`                          |   7.900 μs (5%) |         |   80 bytes (1%) |           3 |
| `["gemm", "mul", "xf", "true", "8"]`                           | 500.000 ns (5%) |         |   80 bytes (1%) |           3 |
| `["groupby", "sum", "sac"]`                                    | 190.702 μs (5%) |         |  624 bytes (1%) |           5 |
| `["groupby", "sum", "xf-with-init"]`                           | 152.102 μs (5%) |         |   1.20 KiB (1%) |           9 |
| `["groupby", "sum", "xf-without-init"]`                        | 153.102 μs (5%) |         |   1.20 KiB (1%) |           9 |
| `["mapcat_eduction", "base"]`                                  |   1.830 μs (5%) |         |                 |             |
| `["mapcat_eduction", "xf-eduction"]`                           |   2.067 μs (5%) |         |                 |             |
| `["mapcat_eduction", "xf-xf"]`                                 |   2.133 μs (5%) |         |                 |             |
| `["missing_argmax", "man"]`                                    |   1.170 μs (5%) |         |   32 bytes (1%) |           1 |
| `["missing_argmax", "rf"]`                                     |   1.430 μs (5%) |         |   32 bytes (1%) |           1 |
| `["missing_argmax", "xf"]`                                     |   1.440 μs (5%) |         |   32 bytes (1%) |           1 |
| `["missing_dot", "equiv"]`                                     |   2.210 μs (5%) |         |   16 bytes (1%) |           1 |
| `["missing_dot", "man"]`                                       |   1.410 μs (5%) |         |   16 bytes (1%) |           1 |
| `["missing_dot", "naive"]`                                     |   4.914 μs (5%) |         |   16 bytes (1%) |           1 |
| `["missing_dot", "rf"]`                                        |   1.340 μs (5%) |         |   16 bytes (1%) |           1 |
| `["missing_dot", "rf_nota"]`                                   |   2.222 μs (5%) |         |   16 bytes (1%) |           1 |
| `["missing_dot", "xf"]`                                        | 105.702 μs (5%) |         |  72.31 KiB (1%) |        3750 |
| `["missing_dot", "xf_nota"]`                                   | 107.502 μs (5%) |         |  72.23 KiB (1%) |        3746 |
| `["overhead", "foldl"]`                                        |   4.500 ns (5%) |         |                 |             |
| `["overhead", "reduce_basecase"]`                              | 155.046 ns (5%) |         |   48 bytes (1%) |           2 |
| `["partition_by", "man"]`                                      |   2.178 ms (5%) |         |  352 bytes (1%) |           4 |
| `["partition_by", "xf"]`                                       |   2.160 ms (5%) |         |  544 bytes (1%) |           6 |
| `["set", "base"]`                                              |   5.810 ms (5%) |         |  49.56 KiB (1%) |          17 |
| `["set", "xf"]`                                                |   5.744 ms (5%) |         |  49.59 KiB (1%) |          19 |
| `["sum_transpose", "30", "noinit", "iter"]`                    |   2.322 μs (5%) |         |                 |             |
| `["sum_transpose", "30", "noinit", "man"]`                     |   1.610 μs (5%) |         |                 |             |
| `["sum_transpose", "30", "noinit", "xf"]`                      |   1.021 μs (5%) |         |   32 bytes (1%) |           2 |
| `["sum_transpose", "30", "withinit", "iter"]`                  |   1.540 μs (5%) |         |                 |             |
| `["sum_transpose", "30", "withinit", "man"]`                   | 904.878 ns (5%) |         |                 |             |
| `["sum_transpose", "30", "withinit", "xf"]`                    | 933.333 ns (5%) |         |   48 bytes (1%) |           3 |
| `["teerf_filter", "noinit"]`                                   |   2.356 μs (5%) |         |  192 bytes (1%) |           8 |
| `["teerf_filter", "withinit"]`                                 | 276.901 ns (5%) |         |                 |             |

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
      Ubuntu 20.04.2 LTS
  uname: Linux 5.4.0-1043-azure #45-Ubuntu SMP Fri Mar 19 17:33:38 UTC 2021 x86_64 x86_64
  CPU: Intel(R) Xeon(R) CPU E5-2673 v4 @ 2.30GHz: 
              speed         user         nice          sys         idle          irq
       #1  2294 MHz      11666 s         17 s       1485 s     132977 s          0 s
       #2  2294 MHz     107485 s          8 s       2086 s      36856 s          0 s
       
  Memory: 6.791343688964844 GB (3462.7265625 MB free)
  Uptime: 1470.0 sec
  Load Avg:  1.0  1.005859375  0.80712890625
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
    CPU MHz:                         2294.686
    BogoMIPS:                        4589.37
    Hypervisor vendor:               Microsoft
    Virtualization type:             full
    L1d cache:                       64 KiB
    L1i cache:                       64 KiB
    L2 cache:                        512 KiB
    L3 cache:                        50 MiB
    NUMA node0 CPU(s):               0,1
    Vulnerability Itlb multihit:     KVM: Vulnerable
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

