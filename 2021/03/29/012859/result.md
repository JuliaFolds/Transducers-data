# Benchmark result

* Pull request commit: [`5d31eca53bb480de3fda2736c1379db7048f29ef`](https://github.com/JuliaFolds/Transducers.jl/commit/5d31eca53bb480de3fda2736c1379db7048f29ef)
* Pull request: <https://github.com/JuliaFolds/Transducers.jl/pull/243> (Update */Manifest.toml)

# Judge result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmarks:
    - Target: 29 Mar 2021 - 01:22
    - Baseline: 29 Mar 2021 - 01:28
* Package commits:
    - Target: acd58d
    - Baseline: 0e46ec
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
| `["cat", "xf"]`                                                | 0.66 (5%) :white_check_mark: |    1.00 (1%)  |
| `["collect", "identity-float"]`                                | 0.89 (5%) :white_check_mark: |    1.00 (1%)  |
| `["filter_sum", "1000", "RandomFloats", "noinit", "base"]`     | 0.29 (5%) :white_check_mark: |    1.00 (1%)  |
| `["filter_sum", "1000", "UnitRange", "noinit", "xf"]`          | 0.94 (5%) :white_check_mark: |    1.00 (1%)  |
| `["filter_sum", "10000", "RandomFloats", "noinit", "base"]`    | 0.83 (5%) :white_check_mark: |    1.00 (1%)  |
| `["findall", "xf-iter"]`                                       |                1.10 (5%) :x: |    1.00 (1%)  |
| `["gemm", "mul", "man", "false", "8"]`                         |                1.11 (5%) :x: |    1.00 (1%)  |
| `["gemm", "mul", "man", "ivdep", "8"]`                         |                1.30 (5%) :x: |    1.00 (1%)  |
| `["gemm", "mul", "man", "true", "8"]`                          |                1.13 (5%) :x: |    1.00 (1%)  |
| `["gemm", "mul", "xf", "false", "8"]`                          |                1.10 (5%) :x: |    1.00 (1%)  |
| `["gemm", "mul", "xf", "true", "8"]`                           | 0.89 (5%) :white_check_mark: |    1.00 (1%)  |
| `["groupby", "sum", "sac"]`                                    |                   0.98 (5%)  | 2.10 (1%) :x: |
| `["mapcat_eduction", "xf-eduction"]`                           | 0.53 (5%) :white_check_mark: |    1.00 (1%)  |
| `["mapcat_eduction", "xf-xf"]`                                 | 0.53 (5%) :white_check_mark: |    1.00 (1%)  |
| `["missing_dot", "equiv"]`                                     |                1.07 (5%) :x: |    1.00 (1%)  |
| `["overhead", "foldl"]`                                        |                1.06 (5%) :x: |    1.00 (1%)  |
| `["overhead", "reduce_basecase"]`                              | 0.95 (5%) :white_check_mark: |    1.00 (1%)  |

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
  uname: Linux 5.4.0-1041-azure #43-Ubuntu SMP Fri Feb 26 10:21:20 UTC 2021 x86_64 x86_64
  CPU: Intel(R) Xeon(R) CPU E5-2673 v3 @ 2.40GHz: 
              speed         user         nice          sys         idle          irq
       #1  2397 MHz      73264 s         18 s       1446 s      11392 s          0 s
       #2  2397 MHz       8287 s          6 s       1413 s      76364 s          0 s
       
  Memory: 6.791343688964844 GB (3702.07421875 MB free)
  Uptime: 874.0 sec
  Load Avg:  1.00537109375  0.9814453125  0.66357421875
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-9.0.1 (ORCJIT, haswell)
```

### Baseline
```
Julia Version 1.5.4
Commit 69fcb5745b (2021-03-11 19:13 UTC)
Platform Info:
  OS: Linux (x86_64-pc-linux-gnu)
      Ubuntu 20.04.2 LTS
  uname: Linux 5.4.0-1041-azure #43-Ubuntu SMP Fri Feb 26 10:21:20 UTC 2021 x86_64 x86_64
  CPU: Intel(R) Xeon(R) CPU E5-2673 v3 @ 2.40GHz: 
              speed         user         nice          sys         idle          irq
       #1  2397 MHz      93360 s         18 s       1722 s      24447 s          0 s
       #2  2397 MHz      21381 s          6 s       1586 s      96515 s          0 s
       
  Memory: 6.791343688964844 GB (3528.28515625 MB free)
  Uptime: 1208.0 sec
  Load Avg:  1.0  1.0  0.77783203125
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-9.0.1 (ORCJIT, haswell)
```

---
# Target result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmark: 29 Mar 2021 - 1:22
* Package commit: acd58d
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
| `["append!!", "eduction"]`                                     |  21.601 μs (5%) |         |  64.63 KiB (1%) |          13 |
| `["append!!", "xf"]`                                           |  21.401 μs (5%) |         |  64.63 KiB (1%) |          13 |
| `["cartesian", "copyto!", "iter"]`                             |   7.050 μs (5%) |         |                 |             |
| `["cartesian", "copyto!", "man"]`                              |   4.100 μs (5%) |         |                 |             |
| `["cartesian", "copyto!", "xf"]`                               |   3.100 μs (5%) |         |                 |             |
| `["cat", "base"]`                                              |   2.122 μs (5%) |         |                 |             |
| `["cat", "xf"]`                                                |   2.611 μs (5%) |         |                 |             |
| `["collect", "filter-missing"]`                                |  65.003 μs (5%) |         |  32.81 KiB (1%) |          14 |
| `["collect", "identity-float"]`                                |  29.601 μs (5%) |         | 256.66 KiB (1%) |          14 |
| `["collect", "identity-union"]`                                | 173.509 μs (5%) |         | 601.08 KiB (1%) |       10014 |
| `["dict", "base"]`                                             |   5.294 ms (5%) |         |  92.91 KiB (1%) |          22 |
| `["dict", "xf"]`                                               |   5.206 ms (5%) |         |  92.31 KiB (1%) |          18 |
| `["dot", "blas"]`                                              |   2.311 μs (5%) |         |                 |             |
| `["dot", "man"]`                                               |   2.289 μs (5%) |         |                 |             |
| `["dot", "rf"]`                                                |   2.722 μs (5%) |         |                 |             |
| `["dot", "xf"]`                                                |   2.800 μs (5%) |         |   64 bytes (1%) |           3 |
| `["filter_map_map!", "man"]`                                   |  66.803 μs (5%) |         |                 |             |
| `["filter_map_map!", "xf"]`                                    | 690.335 μs (5%) |         |   80 bytes (1%) |           3 |
| `["filter_map_reduce", "man"]`                                 | 259.613 μs (5%) |         |                 |             |
| `["filter_map_reduce", "xf"]`                                  | 259.613 μs (5%) |         |                 |             |
| `["filter_sum", "1000", "RandomFloats", "noinit", "base"]`     | 965.261 ns (5%) |         |                 |             |
| `["filter_sum", "1000", "RandomFloats", "noinit", "naive"]`    |   1.340 μs (5%) |         |                 |             |
| `["filter_sum", "1000", "RandomFloats", "noinit", "xf"]`       |   1.840 μs (5%) |         |                 |             |
| `["filter_sum", "1000", "RandomFloats", "withinit", "base"]`   |   1.840 μs (5%) |         |                 |             |
| `["filter_sum", "1000", "RandomFloats", "withinit", "naive"]`  |   1.110 μs (5%) |         |                 |             |
| `["filter_sum", "1000", "RandomFloats", "withinit", "xf"]`     |   1.840 μs (5%) |         |                 |             |
| `["filter_sum", "1000", "UnitRange", "noinit", "base"]`        |   2.278 μs (5%) |         |                 |             |
| `["filter_sum", "1000", "UnitRange", "noinit", "naive"]`       | 934.517 ns (5%) |         |                 |             |
| `["filter_sum", "1000", "UnitRange", "noinit", "xf"]`          | 210.284 ns (5%) |         |                 |             |
| `["filter_sum", "1000", "UnitRange", "withinit", "base"]`      | 206.843 ns (5%) |         |                 |             |
| `["filter_sum", "1000", "UnitRange", "withinit", "naive"]`     | 644.474 ns (5%) |         |                 |             |
| `["filter_sum", "1000", "UnitRange", "withinit", "xf"]`        | 210.286 ns (5%) |         |                 |             |
| `["filter_sum", "10000", "RandomFloats", "noinit", "base"]`    |  44.503 μs (5%) |         |                 |             |
| `["filter_sum", "10000", "RandomFloats", "noinit", "naive"]`   |  51.703 μs (5%) |         |                 |             |
| `["filter_sum", "10000", "RandomFloats", "noinit", "xf"]`      |  18.500 μs (5%) |         |                 |             |
| `["filter_sum", "10000", "RandomFloats", "withinit", "base"]`  |  18.500 μs (5%) |         |                 |             |
| `["filter_sum", "10000", "RandomFloats", "withinit", "naive"]` |  47.803 μs (5%) |         |                 |             |
| `["filter_sum", "10000", "RandomFloats", "withinit", "xf"]`    |  18.500 μs (5%) |         |                 |             |
| `["filter_sum", "10000", "UnitRange", "noinit", "base"]`       |  22.301 μs (5%) |         |                 |             |
| `["filter_sum", "10000", "UnitRange", "noinit", "naive"]`      |   9.300 μs (5%) |         |                 |             |
| `["filter_sum", "10000", "UnitRange", "noinit", "xf"]`         |   1.940 μs (5%) |         |                 |             |
| `["filter_sum", "10000", "UnitRange", "withinit", "base"]`     |   1.870 μs (5%) |         |                 |             |
| `["filter_sum", "10000", "UnitRange", "withinit", "naive"]`    |   6.080 μs (5%) |         |                 |             |
| `["filter_sum", "10000", "UnitRange", "withinit", "xf"]`       |   1.930 μs (5%) |         |                 |             |
| `["findall", "base"]`                                          | 981.451 μs (5%) |         |   2.00 MiB (1%) |          18 |
| `["findall", "xf-array"]`                                      | 897.646 μs (5%) |         |   3.02 MiB (1%) |       98829 |
| `["findall", "xf-iter"]`                                       | 381.220 μs (5%) |         |   2.00 MiB (1%) |          19 |
| `["gemm", "fusedmul", "blas", "16"]`                           |   4.764 ms (5%) |         |                 |             |
| `["gemm", "fusedmul", "blas", "2"]`                            |   3.539 ms (5%) |         |                 |             |
| `["gemm", "fusedmul", "blas", "32"]`                           |   6.340 ms (5%) |         |                 |             |
| `["gemm", "fusedmul", "blas", "8"]`                            |   3.685 ms (5%) |         |                 |             |
| `["gemm", "fusedmul", "xf", "16"]`                             |   5.282 ms (5%) |         |  192 bytes (1%) |           4 |
| `["gemm", "fusedmul", "xf", "2"]`                              | 674.834 μs (5%) |         |  192 bytes (1%) |           4 |
| `["gemm", "fusedmul", "xf", "32"]`                             |  10.889 ms (5%) |         |  192 bytes (1%) |           4 |
| `["gemm", "fusedmul", "xf", "8"]`                              |   2.632 ms (5%) |         |  192 bytes (1%) |           4 |
| `["gemm", "mul", "linalg", "256"]`                             | 990.451 μs (5%) |         |                 |             |
| `["gemm", "mul", "linalg", "32"]`                              |   3.700 μs (5%) |         |                 |             |
| `["gemm", "mul", "linalg", "8"]`                               | 286.705 ns (5%) |         |                 |             |
| `["gemm", "mul", "man", "false", "256"]`                       |   4.303 ms (5%) |         |                 |             |
| `["gemm", "mul", "man", "false", "32"]`                        |   7.800 μs (5%) |         |                 |             |
| `["gemm", "mul", "man", "false", "8"]`                         | 554.572 ns (5%) |         |                 |             |
| `["gemm", "mul", "man", "ivdep", "256"]`                       |   4.263 ms (5%) |         |                 |             |
| `["gemm", "mul", "man", "ivdep", "32"]`                        |   5.750 μs (5%) |         |                 |             |
| `["gemm", "mul", "man", "ivdep", "8"]`                         | 519.398 ns (5%) |         |                 |             |
| `["gemm", "mul", "man", "true", "256"]`                        |   4.298 ms (5%) |         |                 |             |
| `["gemm", "mul", "man", "true", "32"]`                         |   7.175 μs (5%) |         |                 |             |
| `["gemm", "mul", "man", "true", "8"]`                          | 450.020 ns (5%) |         |                 |             |
| `["gemm", "mul", "xf", "false", "256"]`                        |   4.310 ms (5%) |         |   80 bytes (1%) |           3 |
| `["gemm", "mul", "xf", "false", "32"]`                         |   7.850 μs (5%) |         |   80 bytes (1%) |           3 |
| `["gemm", "mul", "xf", "false", "8"]`                          | 549.233 ns (5%) |         |   80 bytes (1%) |           3 |
| `["gemm", "mul", "xf", "ivdep", "256"]`                        |   4.369 ms (5%) |         |   80 bytes (1%) |           3 |
| `["gemm", "mul", "xf", "ivdep", "32"]`                         |   5.867 μs (5%) |         |   80 bytes (1%) |           3 |
| `["gemm", "mul", "xf", "ivdep", "8"]`                          | 585.110 ns (5%) |         |   80 bytes (1%) |           3 |
| `["gemm", "mul", "xf", "true", "256"]`                         |   4.301 ms (5%) |         |   80 bytes (1%) |           3 |
| `["gemm", "mul", "xf", "true", "32"]`                          |   7.375 μs (5%) |         |   80 bytes (1%) |           3 |
| `["gemm", "mul", "xf", "true", "8"]`                           | 531.963 ns (5%) |         |   80 bytes (1%) |           3 |
| `["groupby", "sum", "sac"]`                                    | 211.111 μs (5%) |         |   1.28 KiB (1%) |          14 |
| `["groupby", "sum", "xf-with-init"]`                           | 173.808 μs (5%) |         |   1.20 KiB (1%) |           9 |
| `["groupby", "sum", "xf-without-init"]`                        | 175.109 μs (5%) |         |   1.20 KiB (1%) |           9 |
| `["mapcat_eduction", "base"]`                                  |   1.940 μs (5%) |         |                 |             |
| `["mapcat_eduction", "xf-eduction"]`                           |   2.111 μs (5%) |         |                 |             |
| `["mapcat_eduction", "xf-xf"]`                                 |   2.111 μs (5%) |         |                 |             |
| `["missing_argmax", "man"]`                                    |   1.430 μs (5%) |         |   32 bytes (1%) |           1 |
| `["missing_argmax", "rf"]`                                     |   1.680 μs (5%) |         |   32 bytes (1%) |           1 |
| `["missing_argmax", "xf"]`                                     |   1.670 μs (5%) |         |   32 bytes (1%) |           1 |
| `["missing_dot", "equiv"]`                                     |   2.433 μs (5%) |         |   16 bytes (1%) |           1 |
| `["missing_dot", "man"]`                                       |   1.490 μs (5%) |         |   16 bytes (1%) |           1 |
| `["missing_dot", "naive"]`                                     |   5.500 μs (5%) |         |   16 bytes (1%) |           1 |
| `["missing_dot", "rf"]`                                        |   1.490 μs (5%) |         |   16 bytes (1%) |           1 |
| `["missing_dot", "rf_nota"]`                                   |   2.422 μs (5%) |         |   16 bytes (1%) |           1 |
| `["missing_dot", "xf"]`                                        | 116.706 μs (5%) |         |  72.20 KiB (1%) |        3744 |
| `["missing_dot", "xf_nota"]`                                   | 118.306 μs (5%) |         |  71.95 KiB (1%) |        3734 |
| `["overhead", "foldl"]`                                        |   5.500 ns (5%) |         |                 |             |
| `["overhead", "reduce_basecase"]`                              | 168.978 ns (5%) |         |   48 bytes (1%) |           2 |
| `["partition_by", "man"]`                                      |   2.360 ms (5%) |         |  352 bytes (1%) |           4 |
| `["partition_by", "xf"]`                                       |   2.326 ms (5%) |         |  544 bytes (1%) |           6 |
| `["set", "base"]`                                              |   6.049 ms (5%) |         |  49.56 KiB (1%) |          17 |
| `["set", "xf"]`                                                |   5.894 ms (5%) |         |  49.59 KiB (1%) |          19 |
| `["sum_transpose", "30", "noinit", "iter"]`                    |   2.600 μs (5%) |         |                 |             |
| `["sum_transpose", "30", "noinit", "man"]`                     |   1.780 μs (5%) |         |                 |             |
| `["sum_transpose", "30", "noinit", "xf"]`                      |   1.090 μs (5%) |         |   32 bytes (1%) |           2 |
| `["sum_transpose", "30", "withinit", "iter"]`                  |   1.910 μs (5%) |         |                 |             |
| `["sum_transpose", "30", "withinit", "man"]`                   | 966.667 ns (5%) |         |                 |             |
| `["sum_transpose", "30", "withinit", "xf"]`                    |   1.030 μs (5%) |         |   48 bytes (1%) |           3 |
| `["teerf_filter", "noinit"]`                                   |   3.088 μs (5%) |         |  192 bytes (1%) |           8 |
| `["teerf_filter", "withinit"]`                                 | 304.685 ns (5%) |         |                 |             |

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
  uname: Linux 5.4.0-1041-azure #43-Ubuntu SMP Fri Feb 26 10:21:20 UTC 2021 x86_64 x86_64
  CPU: Intel(R) Xeon(R) CPU E5-2673 v3 @ 2.40GHz: 
              speed         user         nice          sys         idle          irq
       #1  2397 MHz      73264 s         18 s       1446 s      11392 s          0 s
       #2  2397 MHz       8287 s          6 s       1413 s      76364 s          0 s
       
  Memory: 6.791343688964844 GB (3702.07421875 MB free)
  Uptime: 874.0 sec
  Load Avg:  1.00537109375  0.9814453125  0.66357421875
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-9.0.1 (ORCJIT, haswell)
```

---
# Baseline result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmark: 29 Mar 2021 - 1:28
* Package commit: 0e46ec
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
| `["append!!", "eduction"]`                                     |  21.101 μs (5%) |         |  64.63 KiB (1%) |          13 |
| `["append!!", "xf"]`                                           |  21.201 μs (5%) |         |  64.63 KiB (1%) |          13 |
| `["cartesian", "copyto!", "iter"]`                             |   7.050 μs (5%) |         |                 |             |
| `["cartesian", "copyto!", "man"]`                              |   4.100 μs (5%) |         |                 |             |
| `["cartesian", "copyto!", "xf"]`                               |   3.100 μs (5%) |         |                 |             |
| `["cat", "base"]`                                              |   2.122 μs (5%) |         |                 |             |
| `["cat", "xf"]`                                                |   3.978 μs (5%) |         |                 |             |
| `["collect", "filter-missing"]`                                |  65.103 μs (5%) |         |  32.81 KiB (1%) |          14 |
| `["collect", "identity-float"]`                                |  33.302 μs (5%) |         | 256.66 KiB (1%) |          14 |
| `["collect", "identity-union"]`                                | 169.709 μs (5%) |         | 601.16 KiB (1%) |       10014 |
| `["dict", "base"]`                                             |   5.293 ms (5%) |         |  92.91 KiB (1%) |          22 |
| `["dict", "xf"]`                                               |   5.332 ms (5%) |         |  92.31 KiB (1%) |          18 |
| `["dot", "blas"]`                                              |   2.300 μs (5%) |         |                 |             |
| `["dot", "man"]`                                               |   2.289 μs (5%) |         |                 |             |
| `["dot", "rf"]`                                                |   2.722 μs (5%) |         |                 |             |
| `["dot", "xf"]`                                                |   2.800 μs (5%) |         |   64 bytes (1%) |           3 |
| `["filter_map_map!", "man"]`                                   |  66.404 μs (5%) |         |                 |             |
| `["filter_map_map!", "xf"]`                                    | 688.035 μs (5%) |         |   80 bytes (1%) |           3 |
| `["filter_map_reduce", "man"]`                                 | 259.613 μs (5%) |         |                 |             |
| `["filter_map_reduce", "xf"]`                                  | 259.613 μs (5%) |         |                 |             |
| `["filter_sum", "1000", "RandomFloats", "noinit", "base"]`     |   3.361 μs (5%) |         |                 |             |
| `["filter_sum", "1000", "RandomFloats", "noinit", "naive"]`    |   1.330 μs (5%) |         |                 |             |
| `["filter_sum", "1000", "RandomFloats", "noinit", "xf"]`       |   1.840 μs (5%) |         |                 |             |
| `["filter_sum", "1000", "RandomFloats", "withinit", "base"]`   |   1.840 μs (5%) |         |                 |             |
| `["filter_sum", "1000", "RandomFloats", "withinit", "naive"]`  |   1.160 μs (5%) |         |                 |             |
| `["filter_sum", "1000", "RandomFloats", "withinit", "xf"]`     |   1.840 μs (5%) |         |                 |             |
| `["filter_sum", "1000", "UnitRange", "noinit", "base"]`        |   2.278 μs (5%) |         |                 |             |
| `["filter_sum", "1000", "UnitRange", "noinit", "naive"]`       | 944.862 ns (5%) |         |                 |             |
| `["filter_sum", "1000", "UnitRange", "noinit", "xf"]`          | 223.864 ns (5%) |         |                 |             |
| `["filter_sum", "1000", "UnitRange", "withinit", "base"]`      | 207.010 ns (5%) |         |                 |             |
| `["filter_sum", "1000", "UnitRange", "withinit", "naive"]`     | 638.626 ns (5%) |         |                 |             |
| `["filter_sum", "1000", "UnitRange", "withinit", "xf"]`        | 210.286 ns (5%) |         |                 |             |
| `["filter_sum", "10000", "RandomFloats", "noinit", "base"]`    |  53.803 μs (5%) |         |                 |             |
| `["filter_sum", "10000", "RandomFloats", "noinit", "naive"]`   |  51.403 μs (5%) |         |                 |             |
| `["filter_sum", "10000", "RandomFloats", "noinit", "xf"]`      |  18.500 μs (5%) |         |                 |             |
| `["filter_sum", "10000", "RandomFloats", "withinit", "base"]`  |  18.500 μs (5%) |         |                 |             |
| `["filter_sum", "10000", "RandomFloats", "withinit", "naive"]` |  49.202 μs (5%) |         |                 |             |
| `["filter_sum", "10000", "RandomFloats", "withinit", "xf"]`    |  18.500 μs (5%) |         |                 |             |
| `["filter_sum", "10000", "UnitRange", "noinit", "base"]`       |  22.301 μs (5%) |         |                 |             |
| `["filter_sum", "10000", "UnitRange", "noinit", "naive"]`      |   9.300 μs (5%) |         |                 |             |
| `["filter_sum", "10000", "UnitRange", "noinit", "xf"]`         |   1.940 μs (5%) |         |                 |             |
| `["filter_sum", "10000", "UnitRange", "withinit", "base"]`     |   1.870 μs (5%) |         |                 |             |
| `["filter_sum", "10000", "UnitRange", "withinit", "naive"]`    |   6.060 μs (5%) |         |                 |             |
| `["filter_sum", "10000", "UnitRange", "withinit", "xf"]`       |   1.940 μs (5%) |         |                 |             |
| `["findall", "base"]`                                          | 993.251 μs (5%) |         |   2.00 MiB (1%) |          18 |
| `["findall", "xf-array"]`                                      | 898.346 μs (5%) |         |   3.02 MiB (1%) |       98829 |
| `["findall", "xf-iter"]`                                       | 347.718 μs (5%) |         |   2.00 MiB (1%) |          19 |
| `["gemm", "fusedmul", "blas", "16"]`                           |   4.792 ms (5%) |         |                 |             |
| `["gemm", "fusedmul", "blas", "2"]`                            |   3.552 ms (5%) |         |                 |             |
| `["gemm", "fusedmul", "blas", "32"]`                           |   6.329 ms (5%) |         |                 |             |
| `["gemm", "fusedmul", "blas", "8"]`                            |   3.693 ms (5%) |         |                 |             |
| `["gemm", "fusedmul", "xf", "16"]`                             |   5.296 ms (5%) |         |  192 bytes (1%) |           4 |
| `["gemm", "fusedmul", "xf", "2"]`                              | 657.333 μs (5%) |         |  192 bytes (1%) |           4 |
| `["gemm", "fusedmul", "xf", "32"]`                             |  10.573 ms (5%) |         |  192 bytes (1%) |           4 |
| `["gemm", "fusedmul", "xf", "8"]`                              |   2.634 ms (5%) |         |  192 bytes (1%) |           4 |
| `["gemm", "mul", "linalg", "256"]`                             | 996.851 μs (5%) |         |                 |             |
| `["gemm", "mul", "linalg", "32"]`                              |   3.700 μs (5%) |         |                 |             |
| `["gemm", "mul", "linalg", "8"]`                               | 300.000 ns (5%) |         |                 |             |
| `["gemm", "mul", "man", "false", "256"]`                       |   4.297 ms (5%) |         |                 |             |
| `["gemm", "mul", "man", "false", "32"]`                        |   7.700 μs (5%) |         |                 |             |
| `["gemm", "mul", "man", "false", "8"]`                         | 500.000 ns (5%) |         |                 |             |
| `["gemm", "mul", "man", "ivdep", "256"]`                       |   4.254 ms (5%) |         |                 |             |
| `["gemm", "mul", "man", "ivdep", "32"]`                        |   5.700 μs (5%) |         |                 |             |
| `["gemm", "mul", "man", "ivdep", "8"]`                         | 400.000 ns (5%) |         |                 |             |
| `["gemm", "mul", "man", "true", "256"]`                        |   4.284 ms (5%) |         |                 |             |
| `["gemm", "mul", "man", "true", "32"]`                         |   7.100 μs (5%) |         |                 |             |
| `["gemm", "mul", "man", "true", "8"]`                          | 400.000 ns (5%) |         |                 |             |
| `["gemm", "mul", "xf", "false", "256"]`                        |   4.302 ms (5%) |         |   80 bytes (1%) |           3 |
| `["gemm", "mul", "xf", "false", "32"]`                         |   7.800 μs (5%) |         |   80 bytes (1%) |           3 |
| `["gemm", "mul", "xf", "false", "8"]`                          | 500.000 ns (5%) |         |   80 bytes (1%) |           3 |
| `["gemm", "mul", "xf", "ivdep", "256"]`                        |   4.254 ms (5%) |         |   80 bytes (1%) |           3 |
| `["gemm", "mul", "xf", "ivdep", "32"]`                         |   5.900 μs (5%) |         |   80 bytes (1%) |           3 |
| `["gemm", "mul", "xf", "ivdep", "8"]`                          | 600.000 ns (5%) |         |   80 bytes (1%) |           3 |
| `["gemm", "mul", "xf", "true", "256"]`                         |   4.382 ms (5%) |         |   80 bytes (1%) |           3 |
| `["gemm", "mul", "xf", "true", "32"]`                          |   7.300 μs (5%) |         |   80 bytes (1%) |           3 |
| `["gemm", "mul", "xf", "true", "8"]`                           | 600.000 ns (5%) |         |   80 bytes (1%) |           3 |
| `["groupby", "sum", "sac"]`                                    | 215.411 μs (5%) |         |  624 bytes (1%) |           5 |
| `["groupby", "sum", "xf-with-init"]`                           | 176.209 μs (5%) |         |   1.20 KiB (1%) |           9 |
| `["groupby", "sum", "xf-without-init"]`                        | 176.209 μs (5%) |         |   1.20 KiB (1%) |           9 |
| `["mapcat_eduction", "base"]`                                  |   1.940 μs (5%) |         |                 |             |
| `["mapcat_eduction", "xf-eduction"]`                           |   3.989 μs (5%) |         |                 |             |
| `["mapcat_eduction", "xf-xf"]`                                 |   3.989 μs (5%) |         |                 |             |
| `["missing_argmax", "man"]`                                    |   1.430 μs (5%) |         |   32 bytes (1%) |           1 |
| `["missing_argmax", "rf"]`                                     |   1.660 μs (5%) |         |   32 bytes (1%) |           1 |
| `["missing_argmax", "xf"]`                                     |   1.660 μs (5%) |         |   32 bytes (1%) |           1 |
| `["missing_dot", "equiv"]`                                     |   2.267 μs (5%) |         |   16 bytes (1%) |           1 |
| `["missing_dot", "man"]`                                       |   1.470 μs (5%) |         |   16 bytes (1%) |           1 |
| `["missing_dot", "naive"]`                                     |   5.517 μs (5%) |         |   16 bytes (1%) |           1 |
| `["missing_dot", "rf"]`                                        |   1.470 μs (5%) |         |   16 bytes (1%) |           1 |
| `["missing_dot", "rf_nota"]`                                   |   2.433 μs (5%) |         |   16 bytes (1%) |           1 |
| `["missing_dot", "xf"]`                                        | 118.906 μs (5%) |         |  72.25 KiB (1%) |        3746 |
| `["missing_dot", "xf_nota"]`                                   | 116.406 μs (5%) |         |  72.05 KiB (1%) |        3738 |
| `["overhead", "foldl"]`                                        |   5.200 ns (5%) |         |                 |             |
| `["overhead", "reduce_basecase"]`                              | 178.236 ns (5%) |         |   48 bytes (1%) |           2 |
| `["partition_by", "man"]`                                      |   2.351 ms (5%) |         |  352 bytes (1%) |           4 |
| `["partition_by", "xf"]`                                       |   2.356 ms (5%) |         |  544 bytes (1%) |           6 |
| `["set", "base"]`                                              |   5.919 ms (5%) |         |  49.56 KiB (1%) |          17 |
| `["set", "xf"]`                                                |   5.790 ms (5%) |         |  49.59 KiB (1%) |          19 |
| `["sum_transpose", "30", "noinit", "iter"]`                    |   2.611 μs (5%) |         |                 |             |
| `["sum_transpose", "30", "noinit", "man"]`                     |   1.770 μs (5%) |         |                 |             |
| `["sum_transpose", "30", "noinit", "xf"]`                      |   1.090 μs (5%) |         |   32 bytes (1%) |           2 |
| `["sum_transpose", "30", "withinit", "iter"]`                  |   1.910 μs (5%) |         |                 |             |
| `["sum_transpose", "30", "withinit", "man"]`                   | 966.722 ns (5%) |         |                 |             |
| `["sum_transpose", "30", "withinit", "xf"]`                    |   1.030 μs (5%) |         |   48 bytes (1%) |           3 |
| `["teerf_filter", "noinit"]`                                   |   3.075 μs (5%) |         |  192 bytes (1%) |           8 |
| `["teerf_filter", "withinit"]`                                 | 302.739 ns (5%) |         |                 |             |

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
  uname: Linux 5.4.0-1041-azure #43-Ubuntu SMP Fri Feb 26 10:21:20 UTC 2021 x86_64 x86_64
  CPU: Intel(R) Xeon(R) CPU E5-2673 v3 @ 2.40GHz: 
              speed         user         nice          sys         idle          irq
       #1  2397 MHz      93360 s         18 s       1722 s      24447 s          0 s
       #2  2397 MHz      21381 s          6 s       1586 s      96515 s          0 s
       
  Memory: 6.791343688964844 GB (3528.28515625 MB free)
  Uptime: 1208.0 sec
  Load Avg:  1.0  1.0  0.77783203125
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-9.0.1 (ORCJIT, haswell)
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
    Model:                           63
    Model name:                      Intel(R) Xeon(R) CPU E5-2673 v3 @ 2.40GHz
    Stepping:                        2
    CPU MHz:                         2397.219
    BogoMIPS:                        4794.43
    Hypervisor vendor:               Microsoft
    Virtualization type:             full
    L1d cache:                       64 KiB
    L1i cache:                       64 KiB
    L2 cache:                        512 KiB
    L3 cache:                        30 MiB
    NUMA node0 CPU(s):               0,1
    Vulnerability Itlb multihit:     KVM: Vulnerable
    Vulnerability L1tf:              Mitigation; PTE Inversion
    Vulnerability Mds:               Mitigation; Clear CPU buffers; SMT Host state unknown
    Vulnerability Meltdown:          Mitigation; PTI
    Vulnerability Spec store bypass: Vulnerable
    Vulnerability Spectre v1:        Mitigation; usercopy/swapgs barriers and __user pointer sanitization
    Vulnerability Spectre v2:        Mitigation; Full generic retpoline, STIBP disabled, RSB filling
    Vulnerability Srbds:             Not affected
    Vulnerability Tsx async abort:   Not affected
    Flags:                           fpu vme de pse tsc msr pae mce cx8 apic sep mtrr pge mca cmov pat pse36 clflush mmx fxsr sse sse2 ss ht syscall nx pdpe1gb rdtscp lm constant_tsc rep_good nopl xtopology cpuid pni pclmulqdq ssse3 fma cx16 pcid sse4_1 sse4_2 movbe popcnt aes xsave avx f16c rdrand hypervisor lahf_lm abm invpcid_single pti fsgsbase bmi1 avx2 smep bmi2 erms invpcid xsaveopt md_clear
    

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

