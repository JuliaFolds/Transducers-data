# Benchmark result (via Travis)


# Judge result
# Benchmark Report for */home/travis/build/JuliaFolds/Transducers.jl*

## Job Properties
* Time of benchmarks:
    - Target: 9 Aug 2020 - 07:20
    - Baseline: 9 Aug 2020 - 07:25
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
| `["append!!", "xf"]`                                           |                1.06 (5%) :x: |   1.00 (1%)  |
| `["cat", "xf"]`                                                | 0.86 (5%) :white_check_mark: |   1.00 (1%)  |
| `["filter_map_map!", "man"]`                                   |                1.12 (5%) :x: |   1.00 (1%)  |
| `["filter_map_map!", "xf"]`                                    | 0.94 (5%) :white_check_mark: |   1.00 (1%)  |
| `["filter_sum", "1000", "RandomFloats", "noinit", "base"]`     |                2.05 (5%) :x: |   1.00 (1%)  |
| `["filter_sum", "1000", "RandomFloats", "noinit", "xf"]`       |                1.06 (5%) :x: |   1.00 (1%)  |
| `["filter_sum", "1000", "RandomFloats", "withinit", "naive"]`  |                1.28 (5%) :x: |   1.00 (1%)  |
| `["filter_sum", "1000", "UnitRange", "noinit", "naive"]`       |                1.40 (5%) :x: |   1.00 (1%)  |
| `["filter_sum", "10000", "RandomFloats", "noinit", "base"]`    |                1.11 (5%) :x: |   1.00 (1%)  |
| `["filter_sum", "10000", "RandomFloats", "noinit", "naive"]`   |                1.22 (5%) :x: |   1.00 (1%)  |
| `["filter_sum", "10000", "RandomFloats", "withinit", "naive"]` |                1.07 (5%) :x: |   1.00 (1%)  |
| `["filter_sum", "10000", "UnitRange", "noinit", "naive"]`      |                1.40 (5%) :x: |   1.00 (1%)  |
| `["gemm", "fusedmul", "blas", "2"]`                            |                1.05 (5%) :x: |   1.00 (1%)  |
| `["gemm", "fusedmul", "xf", "32"]`                             |                1.13 (5%) :x: |   1.00 (1%)  |
| `["gemm", "fusedmul", "xf", "8"]`                              |                1.10 (5%) :x: |   1.00 (1%)  |
| `["gemm", "mul", "linalg", "8"]`                               | 0.91 (5%) :white_check_mark: |   1.00 (1%)  |
| `["gemm", "mul", "man", "false", "256"]`                       | 0.94 (5%) :white_check_mark: |   1.00 (1%)  |
| `["gemm", "mul", "man", "false", "32"]`                        |                1.18 (5%) :x: |   1.00 (1%)  |
| `["gemm", "mul", "man", "false", "8"]`                         | 0.73 (5%) :white_check_mark: |   1.00 (1%)  |
| `["gemm", "mul", "man", "ivdep", "8"]`                         | 0.91 (5%) :white_check_mark: |   1.00 (1%)  |
| `["gemm", "mul", "man", "true", "8"]`                          |                1.18 (5%) :x: |   1.00 (1%)  |
| `["gemm", "mul", "xf", "false", "256"]`                        | 0.94 (5%) :white_check_mark: |   1.00 (1%)  |
| `["gemm", "mul", "xf", "false", "32"]`                         |                1.26 (5%) :x: |   1.00 (1%)  |
| `["gemm", "mul", "xf", "false", "8"]`                          | 0.94 (5%) :white_check_mark: |   1.00 (1%)  |
| `["gemm", "mul", "xf", "ivdep", "32"]`                         | 0.94 (5%) :white_check_mark: |   1.00 (1%)  |
| `["gemm", "mul", "xf", "ivdep", "8"]`                          |                1.23 (5%) :x: |   1.00 (1%)  |
| `["gemm", "mul", "xf", "true", "256"]`                         | 0.91 (5%) :white_check_mark: |   1.00 (1%)  |
| `["gemm", "mul", "xf", "true", "8"]`                           | 0.80 (5%) :white_check_mark: |   1.00 (1%)  |
| `["groupby", "sum", "xf-with-init"]`                           | 0.94 (5%) :white_check_mark: |   1.00 (1%)  |
| `["mapcat_eduction", "xf-eduction"]`                           | 0.89 (5%) :white_check_mark: |   1.00 (1%)  |
| `["mapcat_eduction", "xf-xf"]`                                 | 0.95 (5%) :white_check_mark: |   1.00 (1%)  |
| `["missing_dot", "equiv"]`                                     | 0.88 (5%) :white_check_mark: |   1.00 (1%)  |
| `["set", "base"]`                                              | 0.92 (5%) :white_check_mark: |   1.00 (1%)  |

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
      Ubuntu 16.04.6 LTS
  uname: Linux 4.15.0-1028-gcp #29~16.04.1-Ubuntu SMP Tue Feb 12 16:31:10 UTC 2019 x86_64 x86_64
  CPU: Intel(R) Xeon(R) CPU: 
              speed         user         nice          sys         idle          irq
       #1  2800 MHz      15212 s          0 s       1093 s      62024 s          0 s
       #2  2800 MHz      61821 s          0 s       1306 s      16410 s          0 s
       
  Memory: 7.790031433105469 GB (5674.2578125 MB free)
  Uptime: 801.0 sec
  Load Avg:  1.0  0.98388671875  0.654296875
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
      Ubuntu 16.04.6 LTS
  uname: Linux 4.15.0-1028-gcp #29~16.04.1-Ubuntu SMP Tue Feb 12 16:31:10 UTC 2019 x86_64 x86_64
  CPU: Intel(R) Xeon(R) CPU: 
              speed         user         nice          sys         idle          irq
       #1  2800 MHz      24897 s          0 s       1155 s      81410 s          0 s
       #2  2800 MHz      81262 s          0 s       1458 s      25970 s          0 s
       
  Memory: 7.790031433105469 GB (5627.9296875 MB free)
  Uptime: 1092.0 sec
  Load Avg:  1.0087890625  1.0283203125  0.77783203125
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-8.0.1 (ORCJIT, skylake)
```

---
# Target result
# Benchmark Report for */home/travis/build/JuliaFolds/Transducers.jl*

## Job Properties
* Time of benchmark: 9 Aug 2020 - 7:20
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
| `["append!!", "eduction"]`                                     |  19.006 μs (5%) |         |  64.72 KiB (1%) |          18 |
| `["append!!", "xf"]`                                           |  18.936 μs (5%) |         |  64.72 KiB (1%) |          18 |
| `["cat", "base"]`                                              |   1.559 μs (5%) |         |                 |             |
| `["cat", "xf"]`                                                |   1.775 μs (5%) |         |                 |             |
| `["collect", "filter-missing"]`                                | 103.664 μs (5%) |         | 345.31 KiB (1%) |       10015 |
| `["collect", "identity-float"]`                                |  85.755 μs (5%) |         | 569.16 KiB (1%) |       10015 |
| `["collect", "identity-union"]`                                | 295.615 μs (5%) |         | 705.00 KiB (1%) |       16659 |
| `["dict", "base"]`                                             |   3.616 ms (5%) |         |  92.91 KiB (1%) |          22 |
| `["dict", "xf"]`                                               |   3.723 ms (5%) |         |  92.36 KiB (1%) |          21 |
| `["dot", "blas"]`                                              |   1.221 μs (5%) |         |                 |             |
| `["dot", "man"]`                                               |   1.197 μs (5%) |         |                 |             |
| `["dot", "rf"]`                                                |   2.166 μs (5%) |         |                 |             |
| `["dot", "xf"]`                                                |   2.271 μs (5%) |         |   64 bytes (1%) |           3 |
| `["filter_map_map!", "man"]`                                   |  71.868 μs (5%) |         |                 |             |
| `["filter_map_map!", "xf"]`                                    | 624.399 μs (5%) |         |  304 bytes (1%) |          17 |
| `["filter_map_reduce", "man"]`                                 | 202.891 μs (5%) |         |                 |             |
| `["filter_map_reduce", "xf"]`                                  | 202.783 μs (5%) |         |                 |             |
| `["filter_sum", "1000", "RandomFloats", "noinit", "base"]`     |   2.399 μs (5%) |         |                 |             |
| `["filter_sum", "1000", "RandomFloats", "noinit", "naive"]`    |   1.165 μs (5%) |         |                 |             |
| `["filter_sum", "1000", "RandomFloats", "noinit", "xf"]`       |   1.239 μs (5%) |         |                 |             |
| `["filter_sum", "1000", "RandomFloats", "withinit", "base"]`   |   1.570 μs (5%) |         |                 |             |
| `["filter_sum", "1000", "RandomFloats", "withinit", "naive"]`  | 743.793 ns (5%) |         |                 |             |
| `["filter_sum", "1000", "RandomFloats", "withinit", "xf"]`     |   1.560 μs (5%) |         |                 |             |
| `["filter_sum", "1000", "UnitRange", "noinit", "base"]`        |   1.635 μs (5%) |         |                 |             |
| `["filter_sum", "1000", "UnitRange", "noinit", "naive"]`       |   1.043 μs (5%) |         |                 |             |
| `["filter_sum", "1000", "UnitRange", "noinit", "xf"]`          |   1.479 μs (5%) |         |                 |             |
| `["filter_sum", "1000", "UnitRange", "withinit", "base"]`      | 108.294 ns (5%) |         |                 |             |
| `["filter_sum", "1000", "UnitRange", "withinit", "naive"]`     | 590.422 ns (5%) |         |                 |             |
| `["filter_sum", "1000", "UnitRange", "withinit", "xf"]`        | 114.586 ns (5%) |         |                 |             |
| `["filter_sum", "10000", "RandomFloats", "noinit", "base"]`    |  43.909 μs (5%) |         |                 |             |
| `["filter_sum", "10000", "RandomFloats", "noinit", "naive"]`   |  56.308 μs (5%) |         |                 |             |
| `["filter_sum", "10000", "RandomFloats", "noinit", "xf"]`      |  40.272 μs (5%) |         |                 |             |
| `["filter_sum", "10000", "RandomFloats", "withinit", "base"]`  |  15.853 μs (5%) |         |                 |             |
| `["filter_sum", "10000", "RandomFloats", "withinit", "naive"]` |  40.621 μs (5%) |         |                 |             |
| `["filter_sum", "10000", "RandomFloats", "withinit", "xf"]`    |  15.861 μs (5%) |         |                 |             |
| `["filter_sum", "10000", "UnitRange", "noinit", "base"]`       |  16.239 μs (5%) |         |                 |             |
| `["filter_sum", "10000", "UnitRange", "noinit", "naive"]`      |  10.341 μs (5%) |         |                 |             |
| `["filter_sum", "10000", "UnitRange", "noinit", "xf"]`         |  14.748 μs (5%) |         |                 |             |
| `["filter_sum", "10000", "UnitRange", "withinit", "base"]`     |   1.034 μs (5%) |         |                 |             |
| `["filter_sum", "10000", "UnitRange", "withinit", "naive"]`    |   5.892 μs (5%) |         |                 |             |
| `["filter_sum", "10000", "UnitRange", "withinit", "xf"]`       |   1.096 μs (5%) |         |                 |             |
| `["findall", "base"]`                                          | 817.727 μs (5%) |         |   2.00 MiB (1%) |          21 |
| `["findall", "xf-array"]`                                      | 743.329 μs (5%) |         |   3.02 MiB (1%) |       98970 |
| `["findall", "xf-iter"]`                                       | 840.175 μs (5%) |         |   5.05 MiB (1%) |       99913 |
| `["gemm", "fusedmul", "blas", "16"]`                           |   5.010 ms (5%) |         |                 |             |
| `["gemm", "fusedmul", "blas", "2"]`                            |   3.571 ms (5%) |         |                 |             |
| `["gemm", "fusedmul", "blas", "32"]`                           |   7.162 ms (5%) |         |                 |             |
| `["gemm", "fusedmul", "blas", "8"]`                            |   4.035 ms (5%) |         |                 |             |
| `["gemm", "fusedmul", "xf", "16"]`                             |   5.248 ms (5%) |         |  160 bytes (1%) |           6 |
| `["gemm", "fusedmul", "xf", "2"]`                              | 603.128 μs (5%) |         |  160 bytes (1%) |           6 |
| `["gemm", "fusedmul", "xf", "32"]`                             |  10.258 ms (5%) |         |  160 bytes (1%) |           6 |
| `["gemm", "fusedmul", "xf", "8"]`                              |   2.661 ms (5%) |         |  160 bytes (1%) |           6 |
| `["gemm", "mul", "linalg", "256"]`                             | 970.268 μs (5%) |         |                 |             |
| `["gemm", "mul", "linalg", "32"]`                              |   3.117 μs (5%) |         |                 |             |
| `["gemm", "mul", "linalg", "8"]`                               | 265.514 ns (5%) |         |                 |             |
| `["gemm", "mul", "man", "false", "256"]`                       |   1.850 ms (5%) |         |                 |             |
| `["gemm", "mul", "man", "false", "32"]`                        |   5.745 μs (5%) |         |                 |             |
| `["gemm", "mul", "man", "false", "8"]`                         | 396.687 ns (5%) |         |                 |             |
| `["gemm", "mul", "man", "ivdep", "256"]`                       |   1.894 ms (5%) |         |                 |             |
| `["gemm", "mul", "man", "ivdep", "32"]`                        |   4.564 μs (5%) |         |                 |             |
| `["gemm", "mul", "man", "ivdep", "8"]`                         | 394.642 ns (5%) |         |                 |             |
| `["gemm", "mul", "man", "true", "256"]`                        |   1.866 ms (5%) |         |                 |             |
| `["gemm", "mul", "man", "true", "32"]`                         |   5.113 μs (5%) |         |                 |             |
| `["gemm", "mul", "man", "true", "8"]`                          | 506.995 ns (5%) |         |                 |             |
| `["gemm", "mul", "xf", "false", "256"]`                        |   1.852 ms (5%) |         |   48 bytes (1%) |           2 |
| `["gemm", "mul", "xf", "false", "32"]`                         |   6.213 μs (5%) |         |   48 bytes (1%) |           2 |
| `["gemm", "mul", "xf", "false", "8"]`                          | 391.845 ns (5%) |         |   48 bytes (1%) |           2 |
| `["gemm", "mul", "xf", "ivdep", "256"]`                        |   1.920 ms (5%) |         |   48 bytes (1%) |           2 |
| `["gemm", "mul", "xf", "ivdep", "32"]`                         |   4.418 μs (5%) |         |   48 bytes (1%) |           2 |
| `["gemm", "mul", "xf", "ivdep", "8"]`                          | 467.417 ns (5%) |         |   48 bytes (1%) |           2 |
| `["gemm", "mul", "xf", "true", "256"]`                         |   1.843 ms (5%) |         |   48 bytes (1%) |           2 |
| `["gemm", "mul", "xf", "true", "32"]`                          |   5.763 μs (5%) |         |   48 bytes (1%) |           2 |
| `["gemm", "mul", "xf", "true", "8"]`                           | 393.638 ns (5%) |         |   48 bytes (1%) |           2 |
| `["groupby", "sum", "sac"]`                                    | 231.229 μs (5%) |         | 313.14 KiB (1%) |       10007 |
| `["groupby", "sum", "xf-with-init"]`                           | 163.756 μs (5%) |         | 157.44 KiB (1%) |       10008 |
| `["groupby", "sum", "xf-without-init"]`                        | 168.806 μs (5%) |         | 157.44 KiB (1%) |       10008 |
| `["mapcat_eduction", "base"]`                                  |   1.927 μs (5%) |         |                 |             |
| `["mapcat_eduction", "xf-eduction"]`                           |   1.678 μs (5%) |         |                 |             |
| `["mapcat_eduction", "xf-xf"]`                                 |   1.782 μs (5%) |         |                 |             |
| `["missing_argmax", "man"]`                                    |   2.367 μs (5%) |         |   32 bytes (1%) |           1 |
| `["missing_argmax", "rf"]`                                     |   2.302 μs (5%) |         |   32 bytes (1%) |           1 |
| `["missing_argmax", "xf"]`                                     |   2.848 μs (5%) |         |   32 bytes (1%) |           1 |
| `["missing_dot", "equiv"]`                                     |   1.413 μs (5%) |         |   16 bytes (1%) |           1 |
| `["missing_dot", "man"]`                                       |   1.255 μs (5%) |         |   16 bytes (1%) |           1 |
| `["missing_dot", "naive"]`                                     |   4.306 μs (5%) |         |   16 bytes (1%) |           1 |
| `["missing_dot", "rf"]`                                        |   1.313 μs (5%) |         |   16 bytes (1%) |           1 |
| `["missing_dot", "rf_nota"]`                                   |   1.569 μs (5%) |         |   16 bytes (1%) |           1 |
| `["missing_dot", "xf"]`                                        | 188.622 μs (5%) |         |  72.28 KiB (1%) |        3750 |
| `["missing_dot", "xf_nota"]`                                   | 186.595 μs (5%) |         |  72.19 KiB (1%) |        3744 |
| `["overhead", "foldl"]`                                        |   4.152 ns (5%) |         |                 |             |
| `["overhead", "reduce_basecase"]`                              | 237.335 ns (5%) |         |  464 bytes (1%) |           9 |
| `["partition_by", "man"]`                                      |   1.847 ms (5%) |         |  352 bytes (1%) |           4 |
| `["partition_by", "xf"]`                                       |   2.767 ms (5%) |         |   6.10 MiB (1%) |      200007 |
| `["set", "base"]`                                              |   4.188 ms (5%) |         |  49.58 KiB (1%) |          18 |
| `["set", "xf"]`                                                |   3.987 ms (5%) |         |  49.63 KiB (1%) |          21 |
| `["sum_transpose", "30", "noinit", "iter"]`                    |   2.012 μs (5%) |         |                 |             |
| `["sum_transpose", "30", "noinit", "man"]`                     |   2.228 μs (5%) |         |                 |             |
| `["sum_transpose", "30", "noinit", "xf"]`                      |   2.660 μs (5%) |         |                 |             |
| `["sum_transpose", "30", "withinit", "iter"]`                  |   1.441 μs (5%) |         |                 |             |
| `["sum_transpose", "30", "withinit", "man"]`                   |   1.016 μs (5%) |         |                 |             |
| `["sum_transpose", "30", "withinit", "xf"]`                    |   2.611 μs (5%) |         |                 |             |

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
      Ubuntu 16.04.6 LTS
  uname: Linux 4.15.0-1028-gcp #29~16.04.1-Ubuntu SMP Tue Feb 12 16:31:10 UTC 2019 x86_64 x86_64
  CPU: Intel(R) Xeon(R) CPU: 
              speed         user         nice          sys         idle          irq
       #1  2800 MHz      15212 s          0 s       1093 s      62024 s          0 s
       #2  2800 MHz      61821 s          0 s       1306 s      16410 s          0 s
       
  Memory: 7.790031433105469 GB (5674.2578125 MB free)
  Uptime: 801.0 sec
  Load Avg:  1.0  0.98388671875  0.654296875
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-8.0.1 (ORCJIT, skylake)
```

---
# Baseline result
# Benchmark Report for */home/travis/build/JuliaFolds/Transducers.jl*

## Job Properties
* Time of benchmark: 9 Aug 2020 - 7:25
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
| `["append!!", "eduction"]`                                     |  18.283 μs (5%) |         |  64.72 KiB (1%) |          18 |
| `["append!!", "xf"]`                                           |  17.793 μs (5%) |         |  64.72 KiB (1%) |          18 |
| `["cat", "base"]`                                              |   1.563 μs (5%) |         |                 |             |
| `["cat", "xf"]`                                                |   2.074 μs (5%) |         |                 |             |
| `["collect", "filter-missing"]`                                | 103.585 μs (5%) |         | 345.31 KiB (1%) |       10015 |
| `["collect", "identity-float"]`                                |  86.178 μs (5%) |         | 569.16 KiB (1%) |       10015 |
| `["collect", "identity-union"]`                                | 290.288 μs (5%) |         | 704.95 KiB (1%) |       16654 |
| `["dict", "base"]`                                             |   3.575 ms (5%) |         |  92.91 KiB (1%) |          22 |
| `["dict", "xf"]`                                               |   3.694 ms (5%) |         |  92.36 KiB (1%) |          21 |
| `["dot", "blas"]`                                              |   1.226 μs (5%) |         |                 |             |
| `["dot", "man"]`                                               |   1.204 μs (5%) |         |                 |             |
| `["dot", "rf"]`                                                |   2.203 μs (5%) |         |                 |             |
| `["dot", "xf"]`                                                |   2.270 μs (5%) |         |   64 bytes (1%) |           3 |
| `["filter_map_map!", "man"]`                                   |  64.285 μs (5%) |         |                 |             |
| `["filter_map_map!", "xf"]`                                    | 664.407 μs (5%) |         |  304 bytes (1%) |          17 |
| `["filter_map_reduce", "man"]`                                 | 202.871 μs (5%) |         |                 |             |
| `["filter_map_reduce", "xf"]`                                  | 203.807 μs (5%) |         |                 |             |
| `["filter_sum", "1000", "RandomFloats", "noinit", "base"]`     |   1.173 μs (5%) |         |                 |             |
| `["filter_sum", "1000", "RandomFloats", "noinit", "naive"]`    |   1.211 μs (5%) |         |                 |             |
| `["filter_sum", "1000", "RandomFloats", "noinit", "xf"]`       |   1.170 μs (5%) |         |                 |             |
| `["filter_sum", "1000", "RandomFloats", "withinit", "base"]`   |   1.569 μs (5%) |         |                 |             |
| `["filter_sum", "1000", "RandomFloats", "withinit", "naive"]`  | 579.444 ns (5%) |         |                 |             |
| `["filter_sum", "1000", "RandomFloats", "withinit", "xf"]`     |   1.568 μs (5%) |         |                 |             |
| `["filter_sum", "1000", "UnitRange", "noinit", "base"]`        |   1.639 μs (5%) |         |                 |             |
| `["filter_sum", "1000", "UnitRange", "noinit", "naive"]`       | 743.500 ns (5%) |         |                 |             |
| `["filter_sum", "1000", "UnitRange", "noinit", "xf"]`          |   1.482 μs (5%) |         |                 |             |
| `["filter_sum", "1000", "UnitRange", "withinit", "base"]`      | 107.232 ns (5%) |         |                 |             |
| `["filter_sum", "1000", "UnitRange", "withinit", "naive"]`     | 591.861 ns (5%) |         |                 |             |
| `["filter_sum", "1000", "UnitRange", "withinit", "xf"]`        | 115.422 ns (5%) |         |                 |             |
| `["filter_sum", "10000", "RandomFloats", "noinit", "base"]`    |  39.423 μs (5%) |         |                 |             |
| `["filter_sum", "10000", "RandomFloats", "noinit", "naive"]`   |  45.994 μs (5%) |         |                 |             |
| `["filter_sum", "10000", "RandomFloats", "noinit", "xf"]`      |  39.036 μs (5%) |         |                 |             |
| `["filter_sum", "10000", "RandomFloats", "withinit", "base"]`  |  15.845 μs (5%) |         |                 |             |
| `["filter_sum", "10000", "RandomFloats", "withinit", "naive"]` |  37.956 μs (5%) |         |                 |             |
| `["filter_sum", "10000", "RandomFloats", "withinit", "xf"]`    |  15.853 μs (5%) |         |                 |             |
| `["filter_sum", "10000", "UnitRange", "noinit", "base"]`       |  16.234 μs (5%) |         |                 |             |
| `["filter_sum", "10000", "UnitRange", "noinit", "naive"]`      |   7.388 μs (5%) |         |                 |             |
| `["filter_sum", "10000", "UnitRange", "noinit", "xf"]`         |  14.740 μs (5%) |         |                 |             |
| `["filter_sum", "10000", "UnitRange", "withinit", "base"]`     |   1.030 μs (5%) |         |                 |             |
| `["filter_sum", "10000", "UnitRange", "withinit", "naive"]`    |   5.890 μs (5%) |         |                 |             |
| `["filter_sum", "10000", "UnitRange", "withinit", "xf"]`       |   1.095 μs (5%) |         |                 |             |
| `["findall", "base"]`                                          | 807.737 μs (5%) |         |   2.00 MiB (1%) |          21 |
| `["findall", "xf-array"]`                                      | 725.743 μs (5%) |         |   3.02 MiB (1%) |       98970 |
| `["findall", "xf-iter"]`                                       | 842.710 μs (5%) |         |   5.05 MiB (1%) |       99913 |
| `["gemm", "fusedmul", "blas", "16"]`                           |   5.028 ms (5%) |         |                 |             |
| `["gemm", "fusedmul", "blas", "2"]`                            |   3.393 ms (5%) |         |                 |             |
| `["gemm", "fusedmul", "blas", "32"]`                           |   7.119 ms (5%) |         |                 |             |
| `["gemm", "fusedmul", "blas", "8"]`                            |   3.939 ms (5%) |         |                 |             |
| `["gemm", "fusedmul", "xf", "16"]`                             |   5.314 ms (5%) |         |  160 bytes (1%) |           6 |
| `["gemm", "fusedmul", "xf", "2"]`                              | 615.972 μs (5%) |         |  160 bytes (1%) |           6 |
| `["gemm", "fusedmul", "xf", "32"]`                             |   9.111 ms (5%) |         |  160 bytes (1%) |           6 |
| `["gemm", "fusedmul", "xf", "8"]`                              |   2.424 ms (5%) |         |  160 bytes (1%) |           6 |
| `["gemm", "mul", "linalg", "256"]`                             | 969.484 μs (5%) |         |                 |             |
| `["gemm", "mul", "linalg", "32"]`                              |   3.191 μs (5%) |         |                 |             |
| `["gemm", "mul", "linalg", "8"]`                               | 291.000 ns (5%) |         |                 |             |
| `["gemm", "mul", "man", "false", "256"]`                       |   1.959 ms (5%) |         |                 |             |
| `["gemm", "mul", "man", "false", "32"]`                        |   4.884 μs (5%) |         |                 |             |
| `["gemm", "mul", "man", "false", "8"]`                         | 542.000 ns (5%) |         |                 |             |
| `["gemm", "mul", "man", "ivdep", "256"]`                       |   1.931 ms (5%) |         |                 |             |
| `["gemm", "mul", "man", "ivdep", "32"]`                        |   4.529 μs (5%) |         |                 |             |
| `["gemm", "mul", "man", "ivdep", "8"]`                         | 435.000 ns (5%) |         |                 |             |
| `["gemm", "mul", "man", "true", "256"]`                        |   1.943 ms (5%) |         |                 |             |
| `["gemm", "mul", "man", "true", "32"]`                         |   5.041 μs (5%) |         |                 |             |
| `["gemm", "mul", "man", "true", "8"]`                          | 430.000 ns (5%) |         |                 |             |
| `["gemm", "mul", "xf", "false", "256"]`                        |   1.963 ms (5%) |         |   48 bytes (1%) |           2 |
| `["gemm", "mul", "xf", "false", "32"]`                         |   4.922 μs (5%) |         |   48 bytes (1%) |           2 |
| `["gemm", "mul", "xf", "false", "8"]`                          | 418.000 ns (5%) |         |   48 bytes (1%) |           2 |
| `["gemm", "mul", "xf", "ivdep", "256"]`                        |   1.932 ms (5%) |         |   48 bytes (1%) |           2 |
| `["gemm", "mul", "xf", "ivdep", "32"]`                         |   4.686 μs (5%) |         |   48 bytes (1%) |           2 |
| `["gemm", "mul", "xf", "ivdep", "8"]`                          | 381.000 ns (5%) |         |   48 bytes (1%) |           2 |
| `["gemm", "mul", "xf", "true", "256"]`                         |   2.020 ms (5%) |         |   48 bytes (1%) |           2 |
| `["gemm", "mul", "xf", "true", "32"]`                          |   5.594 μs (5%) |         |   48 bytes (1%) |           2 |
| `["gemm", "mul", "xf", "true", "8"]`                           | 495.000 ns (5%) |         |   48 bytes (1%) |           2 |
| `["groupby", "sum", "sac"]`                                    | 223.920 μs (5%) |         | 313.14 KiB (1%) |       10007 |
| `["groupby", "sum", "xf-with-init"]`                           | 175.067 μs (5%) |         | 157.44 KiB (1%) |       10008 |
| `["groupby", "sum", "xf-without-init"]`                        | 170.014 μs (5%) |         | 157.44 KiB (1%) |       10008 |
| `["mapcat_eduction", "base"]`                                  |   1.927 μs (5%) |         |                 |             |
| `["mapcat_eduction", "xf-eduction"]`                           |   1.877 μs (5%) |         |                 |             |
| `["mapcat_eduction", "xf-xf"]`                                 |   1.878 μs (5%) |         |                 |             |
| `["missing_argmax", "man"]`                                    |   2.366 μs (5%) |         |   32 bytes (1%) |           1 |
| `["missing_argmax", "rf"]`                                     |   2.260 μs (5%) |         |   32 bytes (1%) |           1 |
| `["missing_argmax", "xf"]`                                     |   2.842 μs (5%) |         |   32 bytes (1%) |           1 |
| `["missing_dot", "equiv"]`                                     |   1.599 μs (5%) |         |   16 bytes (1%) |           1 |
| `["missing_dot", "man"]`                                       |   1.254 μs (5%) |         |   16 bytes (1%) |           1 |
| `["missing_dot", "naive"]`                                     |   4.275 μs (5%) |         |   16 bytes (1%) |           1 |
| `["missing_dot", "rf"]`                                        |   1.375 μs (5%) |         |   16 bytes (1%) |           1 |
| `["missing_dot", "rf_nota"]`                                   |   1.631 μs (5%) |         |   16 bytes (1%) |           1 |
| `["missing_dot", "xf"]`                                        | 186.896 μs (5%) |         |  72.03 KiB (1%) |        3740 |
| `["missing_dot", "xf_nota"]`                                   | 192.110 μs (5%) |         |  72.17 KiB (1%) |        3742 |
| `["overhead", "foldl"]`                                        |   4.143 ns (5%) |         |                 |             |
| `["overhead", "reduce_basecase"]`                              | 243.857 ns (5%) |         |  464 bytes (1%) |           9 |
| `["partition_by", "man"]`                                      |   1.796 ms (5%) |         |  352 bytes (1%) |           4 |
| `["partition_by", "xf"]`                                       |   2.737 ms (5%) |         |   6.10 MiB (1%) |      200007 |
| `["set", "base"]`                                              |   4.545 ms (5%) |         |  49.58 KiB (1%) |          18 |
| `["set", "xf"]`                                                |   3.993 ms (5%) |         |  49.63 KiB (1%) |          21 |

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
      Ubuntu 16.04.6 LTS
  uname: Linux 4.15.0-1028-gcp #29~16.04.1-Ubuntu SMP Tue Feb 12 16:31:10 UTC 2019 x86_64 x86_64
  CPU: Intel(R) Xeon(R) CPU: 
              speed         user         nice          sys         idle          irq
       #1  2800 MHz      24897 s          0 s       1155 s      81410 s          0 s
       #2  2800 MHz      81262 s          0 s       1458 s      25970 s          0 s
       
  Memory: 7.790031433105469 GB (5627.9296875 MB free)
  Uptime: 1092.0 sec
  Load Avg:  1.0087890625  1.0283203125  0.77783203125
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

    Architecture:          x86_64
    CPU op-mode(s):        32-bit, 64-bit
    Byte Order:            Little Endian
    CPU(s):                2
    On-line CPU(s) list:   0,1
    Thread(s) per core:    2
    Core(s) per socket:    1
    Socket(s):             1
    NUMA node(s):          1
    Vendor ID:             GenuineIntel
    CPU family:            6
    Model:                 85
    Model name:            Intel(R) Xeon(R) CPU
    Stepping:              7
    CPU MHz:               2800.260
    BogoMIPS:              5600.52
    Hypervisor vendor:     KVM
    Virtualization type:   full
    L1d cache:             32K
    L1i cache:             32K
    L2 cache:              1024K
    L3 cache:              33792K
    NUMA node0 CPU(s):     0,1
    Flags:                 fpu vme de pse tsc msr pae mce cx8 apic sep mtrr pge mca cmov pat pse36 clflush mmx fxsr sse sse2 ss ht syscall nx pdpe1gb rdtscp lm constant_tsc rep_good nopl xtopology nonstop_tsc cpuid pni pclmulqdq ssse3 fma cx16 pcid sse4_1 sse4_2 x2apic movbe popcnt aes xsave avx f16c rdrand hypervisor lahf_lm abm 3dnowprefetch invpcid_single ssbd ibrs ibpb stibp ibrs_enhanced fsgsbase tsc_adjust bmi1 hle avx2 smep bmi2 erms invpcid rtm mpx avx512f avx512dq rdseed adx smap clflushopt clwb avx512cd avx512bw avx512vl xsaveopt xsavec xgetbv1 xsaves arat avx512_vnni arch_capabilities
    

| Cpu Property       | Value                                                      |
|:------------------ |:---------------------------------------------------------- |
| Brand              | Intel(R) Xeon(R) CPU                                       |
| Vendor             | :Intel                                                     |
| Architecture       | :Skylake                                                   |
| Model              | Family: 0x06, Model: 0x55, Stepping: 0x07, Type: 0x00      |
| Cores              | 1 physical cores, 2 logical cores (on executing CPU)       |
|                    | Hyperthreading detected                                    |
| Clock Frequencies  | Not supported by CPU                                       |
| Data Cache         | Level 1:3 : (32, 1024, 33792) kbytes                       |
|                    | 64 byte cache line size                                    |
| Address Size       | 48 bits virtual, 46 bits physical                          |
| SIMD               | 512 bit = 64 byte max. SIMD vector size                    |
| Time Stamp Counter | TSC is accessible via `rdtsc`                              |
|                    | TSC runs at constant rate (invariant from clock frequency) |
| Perf. Monitoring   | Performance Monitoring Counters (PMC) are not supported    |
| Hypervisor         | Yes, KVM                                                   |

