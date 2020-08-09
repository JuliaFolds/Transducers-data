# Benchmark result (via Travis)


# Judge result
# Benchmark Report for */home/travis/build/JuliaFolds/Transducers.jl*

## Job Properties
* Time of benchmarks:
    - Target: 9 Aug 2020 - 04:24
    - Baseline: 9 Aug 2020 - 04:28
* Package commits:
    - Target: 6166ff
    - Baseline: 061a65
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

| ID                                       | time ratio                   | memory ratio                 |
|------------------------------------------|------------------------------|------------------------------|
| `["cat", "base"]`                        | 0.92 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["cat", "xf"]`                          |                1.17 (5%) :x: |                   1.00 (1%)  |
| `["filter_map_map!", "xf"]`              | 0.94 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["findall", "xf-array"]`                |                   0.99 (5%)  | 0.98 (1%) :white_check_mark: |
| `["gemm", "fusedmul", "blas", "32"]`     | 0.94 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["gemm", "fusedmul", "xf", "16"]`       |                1.11 (5%) :x: |                   1.00 (1%)  |
| `["gemm", "fusedmul", "xf", "8"]`        |                1.06 (5%) :x: |                   1.00 (1%)  |
| `["gemm", "mul", "linalg", "8"]`         | 0.86 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["gemm", "mul", "man", "false", "256"]` |                1.05 (5%) :x: |                   1.00 (1%)  |
| `["gemm", "mul", "man", "false", "8"]`   |                1.19 (5%) :x: |                   1.00 (1%)  |
| `["gemm", "mul", "man", "ivdep", "256"]` |                1.06 (5%) :x: |                   1.00 (1%)  |
| `["gemm", "mul", "man", "ivdep", "32"]`  |                1.11 (5%) :x: |                   1.00 (1%)  |
| `["gemm", "mul", "man", "ivdep", "8"]`   | 0.94 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["gemm", "mul", "man", "true", "256"]`  |                1.06 (5%) :x: |                   1.00 (1%)  |
| `["gemm", "mul", "man", "true", "8"]`    | 0.84 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["gemm", "mul", "xf", "false", "32"]`   | 0.77 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["gemm", "mul", "xf", "ivdep", "256"]`  |                1.06 (5%) :x: |                   1.00 (1%)  |
| `["gemm", "mul", "xf", "true", "8"]`     |                1.29 (5%) :x: |                   1.00 (1%)  |
| `["groupby", "sum", "xf-with-init"]`     |                1.05 (5%) :x: |                   1.00 (1%)  |
| `["mapcat_eduction", "base"]`            |                1.06 (5%) :x: |                   1.00 (1%)  |
| `["mapcat_eduction", "xf-eduction"]`     |                1.05 (5%) :x: |                   1.00 (1%)  |
| `["missing_argmax", "xf"]`               |                1.25 (5%) :x: |                   1.00 (1%)  |
| `["missing_dot", "equiv"]`               |                1.05 (5%) :x: |                   1.00 (1%)  |

## Benchmark Group List
Here's a list of all the benchmark groups executed by this job:

- `["append!!"]`
- `["cat"]`
- `["collect"]`
- `["dict"]`
- `["dot"]`
- `["filter_map_map!"]`
- `["filter_map_reduce"]`
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
       #1  2800 MHz       9096 s          0 s       1126 s      61521 s          0 s
       #2  2800 MHz      61184 s          0 s       1285 s       9610 s          0 s
       
  Memory: 7.790031433105469 GB (5646.65234375 MB free)
  Uptime: 730.0 sec
  Load Avg:  1.00390625  0.97802734375  0.623046875
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
       #1  2800 MHz      20182 s          0 s       1291 s      77543 s          0 s
       #2  2800 MHz      77326 s          0 s       1348 s      20703 s          0 s
       
  Memory: 7.790031433105469 GB (5582.6640625 MB free)
  Uptime: 1003.0 sec
  Load Avg:  1.11572265625  1.056640625  0.75341796875
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-8.0.1 (ORCJIT, skylake)
```

---
# Target result
# Benchmark Report for */home/travis/build/JuliaFolds/Transducers.jl*

## Job Properties
* Time of benchmark: 9 Aug 2020 - 4:24
* Package commit: 6166ff
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

| ID                                                                          | time            | GC time | memory          | allocations |
|-----------------------------------------------------------------------------|----------------:|--------:|----------------:|------------:|
| `["append!!", "eduction"]`                                                  |  18.660 μs (5%) |         |  64.72 KiB (1%) |          18 |
| `["append!!", "xf"]`                                                        |  18.579 μs (5%) |         |  64.72 KiB (1%) |          18 |
| `["cat", "base"]`                                                           |   1.634 μs (5%) |         |                 |             |
| `["cat", "xf"]`                                                             |   2.075 μs (5%) |         |                 |             |
| `["collect", "filter-missing"]`                                             | 106.885 μs (5%) |         | 345.31 KiB (1%) |       10015 |
| `["collect", "identity-float"]`                                             |  91.570 μs (5%) |         | 569.16 KiB (1%) |       10015 |
| `["collect", "identity-union"]`                                             | 306.979 μs (5%) |         | 704.78 KiB (1%) |       16643 |
| `["dict", "base"]`                                                          |   3.578 ms (5%) |         |  92.91 KiB (1%) |          22 |
| `["dict", "xf"]`                                                            |   3.696 ms (5%) |         |  92.36 KiB (1%) |          21 |
| `["dot", "blas"]`                                                           |   1.231 μs (5%) |         |                 |             |
| `["dot", "man"]`                                                            |   1.162 μs (5%) |         |                 |             |
| `["dot", "rf"]`                                                             |   2.166 μs (5%) |         |                 |             |
| `["dot", "xf"]`                                                             |   2.269 μs (5%) |         |   64 bytes (1%) |           3 |
| `["filter_map_map!", "man"]`                                                |  79.001 μs (5%) |         |                 |             |
| `["filter_map_map!", "xf"]`                                                 | 628.443 μs (5%) |         |  304 bytes (1%) |          17 |
| `["filter_map_reduce", "man"]`                                              | 202.829 μs (5%) |         |                 |             |
| `["filter_map_reduce", "xf"]`                                               | 203.154 μs (5%) |         |                 |             |
| `["filter_sum", ":xs => :floats", ":withinit => false", ":impl => :base"]`  |   1.193 μs (5%) |         |                 |             |
| `["filter_sum", ":xs => :floats", ":withinit => false", ":impl => :naive"]` |   1.254 μs (5%) |         |                 |             |
| `["filter_sum", ":xs => :floats", ":withinit => false", ":impl => :xf"]`    |   1.490 μs (5%) |         |                 |             |
| `["filter_sum", ":xs => :floats", ":withinit => true", ":impl => :base"]`   |   1.161 μs (5%) |         |                 |             |
| `["filter_sum", ":xs => :floats", ":withinit => true", ":impl => :naive"]`  |   1.357 μs (5%) |         |                 |             |
| `["filter_sum", ":xs => :floats", ":withinit => true", ":impl => :xf"]`     |   1.225 μs (5%) |         |                 |             |
| `["filter_sum", ":xs => :ints", ":withinit => false", ":impl => :base"]`    |   1.638 μs (5%) |         |                 |             |
| `["filter_sum", ":xs => :ints", ":withinit => false", ":impl => :naive"]`   | 741.664 ns (5%) |         |                 |             |
| `["filter_sum", ":xs => :ints", ":withinit => false", ":impl => :xf"]`      |   1.485 μs (5%) |         |                 |             |
| `["filter_sum", ":xs => :ints", ":withinit => true", ":impl => :base"]`     | 108.223 ns (5%) |         |                 |             |
| `["filter_sum", ":xs => :ints", ":withinit => true", ":impl => :naive"]`    | 590.433 ns (5%) |         |                 |             |
| `["filter_sum", ":xs => :ints", ":withinit => true", ":impl => :xf"]`       | 111.802 ns (5%) |         |                 |             |
| `["findall", "base"]`                                                       | 837.596 μs (5%) |         |   2.00 MiB (1%) |          21 |
| `["findall", "xf-array"]`                                                   | 781.601 μs (5%) |         |   2.98 MiB (1%) |       97538 |
| `["findall", "xf-iter"]`                                                    | 966.501 μs (5%) |         |   5.05 MiB (1%) |       99917 |
| `["gemm", "fusedmul", "blas", "16"]`                                        |   6.891 ms (5%) |         |                 |             |
| `["gemm", "fusedmul", "blas", "2"]`                                         |   4.802 ms (5%) |         |                 |             |
| `["gemm", "fusedmul", "blas", "32"]`                                        |   8.231 ms (5%) |         |                 |             |
| `["gemm", "fusedmul", "blas", "8"]`                                         |   5.520 ms (5%) |         |                 |             |
| `["gemm", "fusedmul", "xf", "16"]`                                          |   5.143 ms (5%) |         |  160 bytes (1%) |           6 |
| `["gemm", "fusedmul", "xf", "2"]`                                           | 593.491 μs (5%) |         |  160 bytes (1%) |           6 |
| `["gemm", "fusedmul", "xf", "32"]`                                          |  10.526 ms (5%) |         |  160 bytes (1%) |           6 |
| `["gemm", "fusedmul", "xf", "8"]`                                           |   2.719 ms (5%) |         |  160 bytes (1%) |           6 |
| `["gemm", "mul", "linalg", "256"]`                                          | 968.668 μs (5%) |         |                 |             |
| `["gemm", "mul", "linalg", "32"]`                                           |   3.364 μs (5%) |         |                 |             |
| `["gemm", "mul", "linalg", "8"]`                                            | 253.664 ns (5%) |         |                 |             |
| `["gemm", "mul", "man", "false", "256"]`                                    |   2.122 ms (5%) |         |                 |             |
| `["gemm", "mul", "man", "false", "32"]`                                     |   5.132 μs (5%) |         |                 |             |
| `["gemm", "mul", "man", "false", "8"]`                                      | 515.469 ns (5%) |         |                 |             |
| `["gemm", "mul", "man", "ivdep", "256"]`                                    |   2.107 ms (5%) |         |                 |             |
| `["gemm", "mul", "man", "ivdep", "32"]`                                     |   4.818 μs (5%) |         |                 |             |
| `["gemm", "mul", "man", "ivdep", "8"]`                                      | 405.239 ns (5%) |         |                 |             |
| `["gemm", "mul", "man", "true", "256"]`                                     |   2.118 ms (5%) |         |                 |             |
| `["gemm", "mul", "man", "true", "32"]`                                      |   5.396 μs (5%) |         |                 |             |
| `["gemm", "mul", "man", "true", "8"]`                                       | 420.352 ns (5%) |         |                 |             |
| `["gemm", "mul", "xf", "false", "256"]`                                     |   2.131 ms (5%) |         |   48 bytes (1%) |           2 |
| `["gemm", "mul", "xf", "false", "32"]`                                      |   4.806 μs (5%) |         |   48 bytes (1%) |           2 |
| `["gemm", "mul", "xf", "false", "8"]`                                       | 399.635 ns (5%) |         |   48 bytes (1%) |           2 |
| `["gemm", "mul", "xf", "ivdep", "256"]`                                     |   2.108 ms (5%) |         |   48 bytes (1%) |           2 |
| `["gemm", "mul", "xf", "ivdep", "32"]`                                      |   4.615 μs (5%) |         |   48 bytes (1%) |           2 |
| `["gemm", "mul", "xf", "ivdep", "8"]`                                       | 458.045 ns (5%) |         |   48 bytes (1%) |           2 |
| `["gemm", "mul", "xf", "true", "256"]`                                      |   2.117 ms (5%) |         |   48 bytes (1%) |           2 |
| `["gemm", "mul", "xf", "true", "32"]`                                       |   5.223 μs (5%) |         |   48 bytes (1%) |           2 |
| `["gemm", "mul", "xf", "true", "8"]`                                        | 502.401 ns (5%) |         |   48 bytes (1%) |           2 |
| `["groupby", "sum", "sac"]`                                                 | 223.549 μs (5%) |         | 313.14 KiB (1%) |       10007 |
| `["groupby", "sum", "xf-with-init"]`                                        | 173.991 μs (5%) |         | 157.44 KiB (1%) |       10008 |
| `["groupby", "sum", "xf-without-init"]`                                     | 172.902 μs (5%) |         | 157.44 KiB (1%) |       10008 |
| `["mapcat_eduction", "base"]`                                               |   2.044 μs (5%) |         |                 |             |
| `["mapcat_eduction", "xf-eduction"]`                                        |   1.781 μs (5%) |         |                 |             |
| `["mapcat_eduction", "xf-xf"]`                                              |   1.688 μs (5%) |         |                 |             |
| `["missing_argmax", "man"]`                                                 |   2.367 μs (5%) |         |   32 bytes (1%) |           1 |
| `["missing_argmax", "rf"]`                                                  |   2.288 μs (5%) |         |   32 bytes (1%) |           1 |
| `["missing_argmax", "xf"]`                                                  |   2.889 μs (5%) |         |   32 bytes (1%) |           1 |
| `["missing_dot", "equiv"]`                                                  |   1.555 μs (5%) |         |   16 bytes (1%) |           1 |
| `["missing_dot", "man"]`                                                    |   1.367 μs (5%) |         |   16 bytes (1%) |           1 |
| `["missing_dot", "naive"]`                                                  |   4.269 μs (5%) |         |   16 bytes (1%) |           1 |
| `["missing_dot", "rf"]`                                                     |   1.256 μs (5%) |         |   16 bytes (1%) |           1 |
| `["missing_dot", "rf_nota"]`                                                |   1.524 μs (5%) |         |   16 bytes (1%) |           1 |
| `["missing_dot", "xf"]`                                                     | 187.794 μs (5%) |         |  71.84 KiB (1%) |        3728 |
| `["missing_dot", "xf_nota"]`                                                | 183.797 μs (5%) |         |  72.19 KiB (1%) |        3744 |
| `["overhead", "foldl"]`                                                     |   4.155 ns (5%) |         |                 |             |
| `["overhead", "reduce_basecase"]`                                           | 235.760 ns (5%) |         |  464 bytes (1%) |           9 |
| `["partition_by", "man"]`                                                   |   1.831 ms (5%) |         |  352 bytes (1%) |           4 |
| `["partition_by", "xf"]`                                                    |   2.889 ms (5%) |         |   6.10 MiB (1%) |      200007 |
| `["set", "base"]`                                                           |   4.391 ms (5%) |         |  49.58 KiB (1%) |          18 |
| `["set", "xf"]`                                                             |   3.984 ms (5%) |         |  49.63 KiB (1%) |          21 |

## Benchmark Group List
Here's a list of all the benchmark groups executed by this job:

- `["append!!"]`
- `["cat"]`
- `["collect"]`
- `["dict"]`
- `["dot"]`
- `["filter_map_map!"]`
- `["filter_map_reduce"]`
- `["filter_sum", ":xs => :floats", ":withinit => false"]`
- `["filter_sum", ":xs => :floats", ":withinit => true"]`
- `["filter_sum", ":xs => :ints", ":withinit => false"]`
- `["filter_sum", ":xs => :ints", ":withinit => true"]`
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
       #1  2800 MHz       9096 s          0 s       1126 s      61521 s          0 s
       #2  2800 MHz      61184 s          0 s       1285 s       9610 s          0 s
       
  Memory: 7.790031433105469 GB (5646.65234375 MB free)
  Uptime: 730.0 sec
  Load Avg:  1.00390625  0.97802734375  0.623046875
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-8.0.1 (ORCJIT, skylake)
```

---
# Baseline result
# Benchmark Report for */home/travis/build/JuliaFolds/Transducers.jl*

## Job Properties
* Time of benchmark: 9 Aug 2020 - 4:28
* Package commit: 061a65
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

| ID                                       | time            | GC time | memory          | allocations |
|------------------------------------------|----------------:|--------:|----------------:|------------:|
| `["append!!", "eduction"]`               |  18.723 μs (5%) |         |  64.72 KiB (1%) |          18 |
| `["append!!", "xf"]`                     |  18.420 μs (5%) |         |  64.72 KiB (1%) |          18 |
| `["cat", "base"]`                        |   1.778 μs (5%) |         |                 |             |
| `["cat", "xf"]`                          |   1.773 μs (5%) |         |                 |             |
| `["collect", "filter-missing"]`          | 107.229 μs (5%) |         | 345.31 KiB (1%) |       10015 |
| `["collect", "identity-float"]`          |  91.017 μs (5%) |         | 569.16 KiB (1%) |       10015 |
| `["collect", "identity-union"]`          | 307.514 μs (5%) |         | 705.20 KiB (1%) |       16670 |
| `["dict", "base"]`                       |   3.578 ms (5%) |         |  92.91 KiB (1%) |          22 |
| `["dict", "xf"]`                         |   3.691 ms (5%) |         |  92.36 KiB (1%) |          21 |
| `["dot", "blas"]`                        |   1.212 μs (5%) |         |                 |             |
| `["dot", "man"]`                         |   1.199 μs (5%) |         |                 |             |
| `["dot", "rf"]`                          |   2.182 μs (5%) |         |                 |             |
| `["dot", "xf"]`                          |   2.273 μs (5%) |         |   64 bytes (1%) |           3 |
| `["filter_map_map!", "man"]`             |  78.123 μs (5%) |         |                 |             |
| `["filter_map_map!", "xf"]`              | 665.580 μs (5%) |         |  304 bytes (1%) |          17 |
| `["filter_map_reduce", "man"]`           | 203.120 μs (5%) |         |                 |             |
| `["filter_map_reduce", "xf"]`            | 203.846 μs (5%) |         |                 |             |
| `["findall", "base"]`                    | 841.838 μs (5%) |         |   2.00 MiB (1%) |          21 |
| `["findall", "xf-array"]`                | 791.777 μs (5%) |         |   3.05 MiB (1%) |       99805 |
| `["findall", "xf-iter"]`                 | 979.517 μs (5%) |         |   5.05 MiB (1%) |       99928 |
| `["gemm", "fusedmul", "blas", "16"]`     |   6.613 ms (5%) |         |                 |             |
| `["gemm", "fusedmul", "blas", "2"]`      |   4.871 ms (5%) |         |                 |             |
| `["gemm", "fusedmul", "blas", "32"]`     |   8.731 ms (5%) |         |                 |             |
| `["gemm", "fusedmul", "blas", "8"]`      |   5.375 ms (5%) |         |                 |             |
| `["gemm", "fusedmul", "xf", "16"]`       |   4.630 ms (5%) |         |  160 bytes (1%) |           6 |
| `["gemm", "fusedmul", "xf", "2"]`        | 576.049 μs (5%) |         |  160 bytes (1%) |           6 |
| `["gemm", "fusedmul", "xf", "32"]`       |  10.544 ms (5%) |         |  160 bytes (1%) |           6 |
| `["gemm", "fusedmul", "xf", "8"]`        |   2.577 ms (5%) |         |  160 bytes (1%) |           6 |
| `["gemm", "mul", "linalg", "256"]`       | 974.324 μs (5%) |         |                 |             |
| `["gemm", "mul", "linalg", "32"]`        |   3.436 μs (5%) |         |                 |             |
| `["gemm", "mul", "linalg", "8"]`         | 295.000 ns (5%) |         |                 |             |
| `["gemm", "mul", "man", "false", "256"]` |   2.014 ms (5%) |         |                 |             |
| `["gemm", "mul", "man", "false", "32"]`  |   5.085 μs (5%) |         |                 |             |
| `["gemm", "mul", "man", "false", "8"]`   | 432.000 ns (5%) |         |                 |             |
| `["gemm", "mul", "man", "ivdep", "256"]` |   1.989 ms (5%) |         |                 |             |
| `["gemm", "mul", "man", "ivdep", "32"]`  |   4.352 μs (5%) |         |                 |             |
| `["gemm", "mul", "man", "ivdep", "8"]`   | 432.000 ns (5%) |         |                 |             |
| `["gemm", "mul", "man", "true", "256"]`  |   2.002 ms (5%) |         |                 |             |
| `["gemm", "mul", "man", "true", "32"]`   |   5.216 μs (5%) |         |                 |             |
| `["gemm", "mul", "man", "true", "8"]`    | 501.000 ns (5%) |         |                 |             |
| `["gemm", "mul", "xf", "false", "256"]`  |   2.048 ms (5%) |         |   48 bytes (1%) |           2 |
| `["gemm", "mul", "xf", "false", "32"]`   |   6.264 μs (5%) |         |   48 bytes (1%) |           2 |
| `["gemm", "mul", "xf", "false", "8"]`    | 382.000 ns (5%) |         |   48 bytes (1%) |           2 |
| `["gemm", "mul", "xf", "ivdep", "256"]`  |   1.990 ms (5%) |         |   48 bytes (1%) |           2 |
| `["gemm", "mul", "xf", "ivdep", "32"]`   |   4.487 μs (5%) |         |   48 bytes (1%) |           2 |
| `["gemm", "mul", "xf", "ivdep", "8"]`    | 445.000 ns (5%) |         |   48 bytes (1%) |           2 |
| `["gemm", "mul", "xf", "true", "256"]`   |   2.069 ms (5%) |         |   48 bytes (1%) |           2 |
| `["gemm", "mul", "xf", "true", "32"]`    |   5.168 μs (5%) |         |   48 bytes (1%) |           2 |
| `["gemm", "mul", "xf", "true", "8"]`     | 388.000 ns (5%) |         |   48 bytes (1%) |           2 |
| `["groupby", "sum", "sac"]`              | 232.419 μs (5%) |         | 313.14 KiB (1%) |       10007 |
| `["groupby", "sum", "xf-with-init"]`     | 165.673 μs (5%) |         | 157.44 KiB (1%) |       10008 |
| `["groupby", "sum", "xf-without-init"]`  | 173.828 μs (5%) |         | 157.44 KiB (1%) |       10008 |
| `["mapcat_eduction", "base"]`            |   1.925 μs (5%) |         |                 |             |
| `["mapcat_eduction", "xf-eduction"]`     |   1.688 μs (5%) |         |                 |             |
| `["mapcat_eduction", "xf-xf"]`           |   1.690 μs (5%) |         |                 |             |
| `["missing_argmax", "man"]`              |   2.365 μs (5%) |         |   32 bytes (1%) |           1 |
| `["missing_argmax", "rf"]`               |   2.308 μs (5%) |         |   32 bytes (1%) |           1 |
| `["missing_argmax", "xf"]`               |   2.319 μs (5%) |         |   32 bytes (1%) |           1 |
| `["missing_dot", "equiv"]`               |   1.475 μs (5%) |         |   16 bytes (1%) |           1 |
| `["missing_dot", "man"]`                 |   1.419 μs (5%) |         |   16 bytes (1%) |           1 |
| `["missing_dot", "naive"]`               |   4.308 μs (5%) |         |   16 bytes (1%) |           1 |
| `["missing_dot", "rf"]`                  |   1.256 μs (5%) |         |   16 bytes (1%) |           1 |
| `["missing_dot", "rf_nota"]`             |   1.565 μs (5%) |         |   16 bytes (1%) |           1 |
| `["missing_dot", "xf"]`                  | 190.548 μs (5%) |         |  72.00 KiB (1%) |        3734 |
| `["missing_dot", "xf_nota"]`             | 178.663 μs (5%) |         |  71.89 KiB (1%) |        3732 |
| `["overhead", "foldl"]`                  |   4.150 ns (5%) |         |                 |             |
| `["overhead", "reduce_basecase"]`        | 239.998 ns (5%) |         |  464 bytes (1%) |           9 |
| `["partition_by", "man"]`                |   1.807 ms (5%) |         |  352 bytes (1%) |           4 |
| `["partition_by", "xf"]`                 |   2.891 ms (5%) |         |   6.10 MiB (1%) |      200007 |
| `["set", "base"]`                        |   4.211 ms (5%) |         |  49.58 KiB (1%) |          18 |
| `["set", "xf"]`                          |   3.963 ms (5%) |         |  49.63 KiB (1%) |          21 |

## Benchmark Group List
Here's a list of all the benchmark groups executed by this job:

- `["append!!"]`
- `["cat"]`
- `["collect"]`
- `["dict"]`
- `["dot"]`
- `["filter_map_map!"]`
- `["filter_map_reduce"]`
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
       #1  2800 MHz      20182 s          0 s       1291 s      77543 s          0 s
       #2  2800 MHz      77326 s          0 s       1348 s      20703 s          0 s
       
  Memory: 7.790031433105469 GB (5582.6640625 MB free)
  Uptime: 1003.0 sec
  Load Avg:  1.11572265625  1.056640625  0.75341796875
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
    CPU MHz:               2800.184
    BogoMIPS:              5600.36
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

