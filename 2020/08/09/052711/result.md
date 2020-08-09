# Benchmark result (via Travis)


# Judge result
# Benchmark Report for */home/travis/build/JuliaFolds/Transducers.jl*

## Job Properties
* Time of benchmarks:
    - Target: 9 Aug 2020 - 05:21
    - Baseline: 9 Aug 2020 - 05:26
* Package commits:
    - Target: 527c53
    - Baseline: 747697
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

| ID                                       | time ratio                   | memory ratio  |
|------------------------------------------|------------------------------|---------------|
| `["cat", "base"]`                        | 0.86 (5%) :white_check_mark: |    1.00 (1%)  |
| `["collect", "identity-union"]`          |                1.06 (5%) :x: |    1.00 (1%)  |
| `["filter_map_map!", "man"]`             |                1.09 (5%) :x: |    1.00 (1%)  |
| `["filter_map_map!", "xf"]`              | 0.94 (5%) :white_check_mark: |    1.00 (1%)  |
| `["findall", "xf-array"]`                |                   1.04 (5%)  | 1.01 (1%) :x: |
| `["findall", "xf-iter"]`                 |                1.08 (5%) :x: |    1.00 (1%)  |
| `["gemm", "fusedmul", "xf", "2"]`        | 0.92 (5%) :white_check_mark: |    1.00 (1%)  |
| `["gemm", "fusedmul", "xf", "32"]`       |                1.08 (5%) :x: |    1.00 (1%)  |
| `["gemm", "mul", "linalg", "32"]`        | 0.90 (5%) :white_check_mark: |    1.00 (1%)  |
| `["gemm", "mul", "linalg", "8"]`         | 0.83 (5%) :white_check_mark: |    1.00 (1%)  |
| `["gemm", "mul", "man", "false", "256"]` | 0.93 (5%) :white_check_mark: |    1.00 (1%)  |
| `["gemm", "mul", "man", "false", "32"]`  |                1.10 (5%) :x: |    1.00 (1%)  |
| `["gemm", "mul", "man", "ivdep", "8"]`   | 0.94 (5%) :white_check_mark: |    1.00 (1%)  |
| `["gemm", "mul", "man", "true", "256"]`  | 0.94 (5%) :white_check_mark: |    1.00 (1%)  |
| `["gemm", "mul", "man", "true", "32"]`   |                1.13 (5%) :x: |    1.00 (1%)  |
| `["gemm", "mul", "man", "true", "8"]`    | 0.81 (5%) :white_check_mark: |    1.00 (1%)  |
| `["gemm", "mul", "xf", "false", "256"]`  | 0.93 (5%) :white_check_mark: |    1.00 (1%)  |
| `["gemm", "mul", "xf", "false", "8"]`    |                1.22 (5%) :x: |    1.00 (1%)  |
| `["gemm", "mul", "xf", "ivdep", "8"]`    | 0.84 (5%) :white_check_mark: |    1.00 (1%)  |
| `["gemm", "mul", "xf", "true", "256"]`   | 0.93 (5%) :white_check_mark: |    1.00 (1%)  |
| `["mapcat_eduction", "xf-xf"]`           |                1.11 (5%) :x: |    1.00 (1%)  |
| `["missing_dot", "equiv"]`               | 0.95 (5%) :white_check_mark: |    1.00 (1%)  |
| `["missing_dot", "man"]`                 | 0.90 (5%) :white_check_mark: |    1.00 (1%)  |
| `["missing_dot", "rf"]`                  |                1.09 (5%) :x: |    1.00 (1%)  |
| `["overhead", "foldl"]`                  | 0.91 (5%) :white_check_mark: |    1.00 (1%)  |

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
       #1  2800 MHz      51539 s          0 s       1336 s      14948 s          0 s
       #2  2800 MHz      14548 s          0 s        985 s      52381 s          0 s
       
  Memory: 7.790031433105469 GB (5679.29296875 MB free)
  Uptime: 689.0 sec
  Load Avg:  1.140625  0.99853515625  0.60400390625
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
       #1  2800 MHz      51903 s          0 s       1402 s      42855 s          0 s
       #2  2800 MHz      42512 s          0 s       1110 s      52693 s          0 s
       
  Memory: 7.790031433105469 GB (5702.41796875 MB free)
  Uptime: 973.0 sec
  Load Avg:  1.0  1.0  0.72216796875
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-8.0.1 (ORCJIT, skylake)
```

---
# Target result
# Benchmark Report for */home/travis/build/JuliaFolds/Transducers.jl*

## Job Properties
* Time of benchmark: 9 Aug 2020 - 5:21
* Package commit: 527c53
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

| ID                                                                      | time            | GC time | memory          | allocations |
|-------------------------------------------------------------------------|----------------:|--------:|----------------:|------------:|
| `["append!!", "eduction"]`                                              |  18.751 μs (5%) |         |  64.72 KiB (1%) |          18 |
| `["append!!", "xf"]`                                                    |  18.487 μs (5%) |         |  64.72 KiB (1%) |          18 |
| `["cat", "base"]`                                                       |   1.526 μs (5%) |         |                 |             |
| `["cat", "xf"]`                                                         |   1.745 μs (5%) |         |                 |             |
| `["collect", "filter-missing"]`                                         | 101.944 μs (5%) |         | 345.31 KiB (1%) |       10015 |
| `["collect", "identity-float"]`                                         |  81.269 μs (5%) |         | 569.16 KiB (1%) |       10015 |
| `["collect", "identity-union"]`                                         | 299.473 μs (5%) |         | 704.67 KiB (1%) |       16638 |
| `["dict", "base"]`                                                      |   3.612 ms (5%) |         |  92.91 KiB (1%) |          22 |
| `["dict", "xf"]`                                                        |   3.690 ms (5%) |         |  92.36 KiB (1%) |          21 |
| `["dot", "blas"]`                                                       |   1.211 μs (5%) |         |                 |             |
| `["dot", "man"]`                                                        |   1.160 μs (5%) |         |                 |             |
| `["dot", "rf"]`                                                         |   2.165 μs (5%) |         |                 |             |
| `["dot", "xf"]`                                                         |   2.268 μs (5%) |         |   64 bytes (1%) |           3 |
| `["filter_map_map!", "man"]`                                            |  75.270 μs (5%) |         |                 |             |
| `["filter_map_map!", "xf"]`                                             | 623.960 μs (5%) |         |  304 bytes (1%) |          17 |
| `["filter_map_reduce", "man"]`                                          | 202.719 μs (5%) |         |                 |             |
| `["filter_map_reduce", "xf"]`                                           | 202.504 μs (5%) |         |                 |             |
| `["findall", "base"]`                                                   | 792.061 μs (5%) |         |   2.00 MiB (1%) |          21 |
| `["findall", "xf-array"]`                                               | 757.946 μs (5%) |         |   3.06 MiB (1%) |      100063 |
| `["findall", "xf-iter"]`                                                | 901.124 μs (5%) |         |   5.05 MiB (1%) |       99908 |
| `["gemm", "fusedmul", "blas", "16"]`                                    |   4.833 ms (5%) |         |                 |             |
| `["gemm", "fusedmul", "blas", "2"]`                                     |   3.426 ms (5%) |         |                 |             |
| `["gemm", "fusedmul", "blas", "32"]`                                    |   6.915 ms (5%) |         |                 |             |
| `["gemm", "fusedmul", "blas", "8"]`                                     |   3.815 ms (5%) |         |                 |             |
| `["gemm", "fusedmul", "xf", "16"]`                                      |   4.575 ms (5%) |         |  160 bytes (1%) |           6 |
| `["gemm", "fusedmul", "xf", "2"]`                                       | 572.832 μs (5%) |         |  160 bytes (1%) |           6 |
| `["gemm", "fusedmul", "xf", "32"]`                                      |   9.301 ms (5%) |         |  160 bytes (1%) |           6 |
| `["gemm", "fusedmul", "xf", "8"]`                                       |   2.375 ms (5%) |         |  160 bytes (1%) |           6 |
| `["gemm", "mul", "linalg", "256"]`                                      | 953.607 μs (5%) |         |                 |             |
| `["gemm", "mul", "linalg", "32"]`                                       |   3.107 μs (5%) |         |                 |             |
| `["gemm", "mul", "linalg", "8"]`                                        | 250.013 ns (5%) |         |                 |             |
| `["gemm", "mul", "man", "false", "256"]`                                |   1.925 ms (5%) |         |                 |             |
| `["gemm", "mul", "man", "false", "32"]`                                 |   5.490 μs (5%) |         |                 |             |
| `["gemm", "mul", "man", "false", "8"]`                                  | 396.508 ns (5%) |         |                 |             |
| `["gemm", "mul", "man", "ivdep", "256"]`                                |   1.959 ms (5%) |         |                 |             |
| `["gemm", "mul", "man", "ivdep", "32"]`                                 |   4.550 μs (5%) |         |                 |             |
| `["gemm", "mul", "man", "ivdep", "8"]`                                  | 394.657 ns (5%) |         |                 |             |
| `["gemm", "mul", "man", "true", "256"]`                                 |   1.933 ms (5%) |         |                 |             |
| `["gemm", "mul", "man", "true", "32"]`                                  |   5.804 μs (5%) |         |                 |             |
| `["gemm", "mul", "man", "true", "8"]`                                   | 412.720 ns (5%) |         |                 |             |
| `["gemm", "mul", "xf", "false", "256"]`                                 |   1.934 ms (5%) |         |   48 bytes (1%) |           2 |
| `["gemm", "mul", "xf", "false", "32"]`                                  |   4.822 μs (5%) |         |   48 bytes (1%) |           2 |
| `["gemm", "mul", "xf", "false", "8"]`                                   | 470.712 ns (5%) |         |   48 bytes (1%) |           2 |
| `["gemm", "mul", "xf", "ivdep", "256"]`                                 |   1.956 ms (5%) |         |   48 bytes (1%) |           2 |
| `["gemm", "mul", "xf", "ivdep", "32"]`                                  |   4.399 μs (5%) |         |   48 bytes (1%) |           2 |
| `["gemm", "mul", "xf", "ivdep", "8"]`                                   | 376.261 ns (5%) |         |   48 bytes (1%) |           2 |
| `["gemm", "mul", "xf", "true", "256"]`                                  |   1.918 ms (5%) |         |   48 bytes (1%) |           2 |
| `["gemm", "mul", "xf", "true", "32"]`                                   |   4.873 μs (5%) |         |   48 bytes (1%) |           2 |
| `["gemm", "mul", "xf", "true", "8"]`                                    | 393.461 ns (5%) |         |   48 bytes (1%) |           2 |
| `["groupby", "sum", "sac"]`                                             | 226.360 μs (5%) |         | 313.14 KiB (1%) |       10007 |
| `["groupby", "sum", "xf-with-init"]`                                    | 160.754 μs (5%) |         | 157.44 KiB (1%) |       10008 |
| `["groupby", "sum", "xf-without-init"]`                                 | 168.140 μs (5%) |         | 157.44 KiB (1%) |       10008 |
| `["mapcat_eduction", "base"]`                                           |   1.956 μs (5%) |         |                 |             |
| `["mapcat_eduction", "xf-eduction"]`                                    |   1.687 μs (5%) |         |                 |             |
| `["mapcat_eduction", "xf-xf"]`                                          |   1.878 μs (5%) |         |                 |             |
| `["missing_argmax", "man"]`                                             |   2.366 μs (5%) |         |   32 bytes (1%) |           1 |
| `["missing_argmax", "rf"]`                                              |   2.850 μs (5%) |         |   32 bytes (1%) |           1 |
| `["missing_argmax", "xf"]`                                              |   2.299 μs (5%) |         |   32 bytes (1%) |           1 |
| `["missing_dot", "equiv"]`                                              |   1.497 μs (5%) |         |   16 bytes (1%) |           1 |
| `["missing_dot", "man"]`                                                |   1.236 μs (5%) |         |   16 bytes (1%) |           1 |
| `["missing_dot", "naive"]`                                              |   4.277 μs (5%) |         |   16 bytes (1%) |           1 |
| `["missing_dot", "rf"]`                                                 |   1.383 μs (5%) |         |   16 bytes (1%) |           1 |
| `["missing_dot", "rf_nota"]`                                            |   1.504 μs (5%) |         |   16 bytes (1%) |           1 |
| `["missing_dot", "xf"]`                                                 | 191.293 μs (5%) |         |  72.14 KiB (1%) |        3742 |
| `["missing_dot", "xf_nota"]`                                            | 192.518 μs (5%) |         |  71.50 KiB (1%) |        3714 |
| `["overhead", "foldl"]`                                                 |   4.144 ns (5%) |         |                 |             |
| `["overhead", "reduce_basecase"]`                                       | 243.313 ns (5%) |         |  464 bytes (1%) |           9 |
| `["partition_by", "man"]`                                               |   1.793 ms (5%) |         |  352 bytes (1%) |           4 |
| `["partition_by", "xf"]`                                                |   2.792 ms (5%) |         |   6.10 MiB (1%) |      200007 |
| `["set", "base"]`                                                       |   4.237 ms (5%) |         |  49.58 KiB (1%) |          18 |
| `["set", "xf"]`                                                         |   3.987 ms (5%) |         |  49.63 KiB (1%) |          21 |
| `["sum_transpose", ":n => 30", ":withinit => false", ":impl => :iter"]` |   2.008 μs (5%) |         |                 |             |
| `["sum_transpose", ":n => 30", ":withinit => false", ":impl => :man"]`  |   2.240 μs (5%) |         |                 |             |
| `["sum_transpose", ":n => 30", ":withinit => false", ":impl => :xf"]`   |   2.659 μs (5%) |         |                 |             |
| `["sum_transpose", ":n => 30", ":withinit => true", ":impl => :iter"]`  |   1.489 μs (5%) |         |                 |             |
| `["sum_transpose", ":n => 30", ":withinit => true", ":impl => :man"]`   |   1.018 μs (5%) |         |                 |             |
| `["sum_transpose", ":n => 30", ":withinit => true", ":impl => :xf"]`    |   2.393 μs (5%) |         |                 |             |

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
- `["sum_transpose", ":n => 30", ":withinit => false"]`
- `["sum_transpose", ":n => 30", ":withinit => true"]`

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
       #1  2800 MHz      51539 s          0 s       1336 s      14948 s          0 s
       #2  2800 MHz      14548 s          0 s        985 s      52381 s          0 s
       
  Memory: 7.790031433105469 GB (5679.29296875 MB free)
  Uptime: 689.0 sec
  Load Avg:  1.140625  0.99853515625  0.60400390625
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-8.0.1 (ORCJIT, skylake)
```

---
# Baseline result
# Benchmark Report for */home/travis/build/JuliaFolds/Transducers.jl*

## Job Properties
* Time of benchmark: 9 Aug 2020 - 5:26
* Package commit: 747697
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

| ID                                                                                               | time            | GC time | memory          | allocations |
|--------------------------------------------------------------------------------------------------|----------------:|--------:|----------------:|------------:|
| `["append!!", "eduction"]`                                                                       |  18.366 μs (5%) |         |  64.72 KiB (1%) |          18 |
| `["append!!", "xf"]`                                                                             |  18.294 μs (5%) |         |  64.72 KiB (1%) |          18 |
| `["cat", "base"]`                                                                                |   1.778 μs (5%) |         |                 |             |
| `["cat", "xf"]`                                                                                  |   1.773 μs (5%) |         |                 |             |
| `["collect", "filter-missing"]`                                                                  |  98.989 μs (5%) |         | 345.31 KiB (1%) |       10015 |
| `["collect", "identity-float"]`                                                                  |  80.500 μs (5%) |         | 569.16 KiB (1%) |       10015 |
| `["collect", "identity-union"]`                                                                  | 283.454 μs (5%) |         | 704.95 KiB (1%) |       16654 |
| `["dict", "base"]`                                                                               |   3.612 ms (5%) |         |  92.91 KiB (1%) |          22 |
| `["dict", "xf"]`                                                                                 |   3.718 ms (5%) |         |  92.36 KiB (1%) |          21 |
| `["dot", "blas"]`                                                                                |   1.231 μs (5%) |         |                 |             |
| `["dot", "man"]`                                                                                 |   1.201 μs (5%) |         |                 |             |
| `["dot", "rf"]`                                                                                  |   2.173 μs (5%) |         |                 |             |
| `["dot", "xf"]`                                                                                  |   2.282 μs (5%) |         |   64 bytes (1%) |           3 |
| `["filter_map_map!", "man"]`                                                                     |  69.147 μs (5%) |         |                 |             |
| `["filter_map_map!", "xf"]`                                                                      | 662.958 μs (5%) |         |  304 bytes (1%) |          17 |
| `["filter_map_reduce", "man"]`                                                                   | 203.751 μs (5%) |         |                 |             |
| `["filter_map_reduce", "xf"]`                                                                    | 202.588 μs (5%) |         |                 |             |
| `["filter_sum", ":n => 1000", ":xs => :RandomFloats", ":withinit => false", ":impl => :base"]`   |   2.495 μs (5%) |         |                 |             |
| `["filter_sum", ":n => 1000", ":xs => :RandomFloats", ":withinit => false", ":impl => :naive"]`  |   1.199 μs (5%) |         |                 |             |
| `["filter_sum", ":n => 1000", ":xs => :RandomFloats", ":withinit => false", ":impl => :xf"]`     |   2.514 μs (5%) |         |                 |             |
| `["filter_sum", ":n => 1000", ":xs => :RandomFloats", ":withinit => true", ":impl => :base"]`    |   1.603 μs (5%) |         |                 |             |
| `["filter_sum", ":n => 1000", ":xs => :RandomFloats", ":withinit => true", ":impl => :naive"]`   | 796.000 ns (5%) |         |                 |             |
| `["filter_sum", ":n => 1000", ":xs => :RandomFloats", ":withinit => true", ":impl => :xf"]`      |   1.591 μs (5%) |         |                 |             |
| `["filter_sum", ":n => 1000", ":xs => :UnitRange", ":withinit => false", ":impl => :base"]`      |   1.657 μs (5%) |         |                 |             |
| `["filter_sum", ":n => 1000", ":xs => :UnitRange", ":withinit => false", ":impl => :naive"]`     | 770.000 ns (5%) |         |                 |             |
| `["filter_sum", ":n => 1000", ":xs => :UnitRange", ":withinit => false", ":impl => :xf"]`        |   1.506 μs (5%) |         |                 |             |
| `["filter_sum", ":n => 1000", ":xs => :UnitRange", ":withinit => true", ":impl => :base"]`       | 140.000 ns (5%) |         |                 |             |
| `["filter_sum", ":n => 1000", ":xs => :UnitRange", ":withinit => true", ":impl => :naive"]`      | 618.000 ns (5%) |         |                 |             |
| `["filter_sum", ":n => 1000", ":xs => :UnitRange", ":withinit => true", ":impl => :xf"]`         | 146.000 ns (5%) |         |                 |             |
| `["filter_sum", ":n => 10000", ":xs => :RandomFloats", ":withinit => false", ":impl => :base"]`  |  43.752 μs (5%) |         |                 |             |
| `["filter_sum", ":n => 10000", ":xs => :RandomFloats", ":withinit => false", ":impl => :naive"]` |  56.295 μs (5%) |         |                 |             |
| `["filter_sum", ":n => 10000", ":xs => :RandomFloats", ":withinit => false", ":impl => :xf"]`    |  43.907 μs (5%) |         |                 |             |
| `["filter_sum", ":n => 10000", ":xs => :RandomFloats", ":withinit => true", ":impl => :base"]`   |  15.786 μs (5%) |         |                 |             |
| `["filter_sum", ":n => 10000", ":xs => :RandomFloats", ":withinit => true", ":impl => :naive"]`  |  37.515 μs (5%) |         |                 |             |
| `["filter_sum", ":n => 10000", ":xs => :RandomFloats", ":withinit => true", ":impl => :xf"]`     |  15.852 μs (5%) |         |                 |             |
| `["filter_sum", ":n => 10000", ":xs => :UnitRange", ":withinit => false", ":impl => :base"]`     |  16.225 μs (5%) |         |                 |             |
| `["filter_sum", ":n => 10000", ":xs => :UnitRange", ":withinit => false", ":impl => :naive"]`    |   7.388 μs (5%) |         |                 |             |
| `["filter_sum", ":n => 10000", ":xs => :UnitRange", ":withinit => false", ":impl => :xf"]`       |  14.740 μs (5%) |         |                 |             |
| `["filter_sum", ":n => 10000", ":xs => :UnitRange", ":withinit => true", ":impl => :base"]`      |   1.051 μs (5%) |         |                 |             |
| `["filter_sum", ":n => 10000", ":xs => :UnitRange", ":withinit => true", ":impl => :naive"]`     |   5.912 μs (5%) |         |                 |             |
| `["filter_sum", ":n => 10000", ":xs => :UnitRange", ":withinit => true", ":impl => :xf"]`        |   1.116 μs (5%) |         |                 |             |
| `["findall", "base"]`                                                                            | 775.402 μs (5%) |         |   2.00 MiB (1%) |          21 |
| `["findall", "xf-array"]`                                                                        | 730.762 μs (5%) |         |   3.02 MiB (1%) |       98970 |
| `["findall", "xf-iter"]`                                                                         | 831.362 μs (5%) |         |   5.05 MiB (1%) |       99913 |
| `["gemm", "fusedmul", "blas", "16"]`                                                             |   4.697 ms (5%) |         |                 |             |
| `["gemm", "fusedmul", "blas", "2"]`                                                              |   3.436 ms (5%) |         |                 |             |
| `["gemm", "fusedmul", "blas", "32"]`                                                             |   6.652 ms (5%) |         |                 |             |
| `["gemm", "fusedmul", "blas", "8"]`                                                              |   3.873 ms (5%) |         |                 |             |
| `["gemm", "fusedmul", "xf", "16"]`                                                               |   4.704 ms (5%) |         |  160 bytes (1%) |           6 |
| `["gemm", "fusedmul", "xf", "2"]`                                                                | 620.780 μs (5%) |         |  160 bytes (1%) |           6 |
| `["gemm", "fusedmul", "xf", "32"]`                                                               |   8.603 ms (5%) |         |  160 bytes (1%) |           6 |
| `["gemm", "fusedmul", "xf", "8"]`                                                                |   2.303 ms (5%) |         |  160 bytes (1%) |           6 |
| `["gemm", "mul", "linalg", "256"]`                                                               | 951.099 μs (5%) |         |                 |             |
| `["gemm", "mul", "linalg", "32"]`                                                                |   3.445 μs (5%) |         |                 |             |
| `["gemm", "mul", "linalg", "8"]`                                                                 | 302.000 ns (5%) |         |                 |             |
| `["gemm", "mul", "man", "false", "256"]`                                                         |   2.080 ms (5%) |         |                 |             |
| `["gemm", "mul", "man", "false", "32"]`                                                          |   5.009 μs (5%) |         |                 |             |
| `["gemm", "mul", "man", "false", "8"]`                                                           | 413.000 ns (5%) |         |                 |             |
| `["gemm", "mul", "man", "ivdep", "256"]`                                                         |   2.033 ms (5%) |         |                 |             |
| `["gemm", "mul", "man", "ivdep", "32"]`                                                          |   4.386 μs (5%) |         |                 |             |
| `["gemm", "mul", "man", "ivdep", "8"]`                                                           | 419.000 ns (5%) |         |                 |             |
| `["gemm", "mul", "man", "true", "256"]`                                                          |   2.062 ms (5%) |         |                 |             |
| `["gemm", "mul", "man", "true", "32"]`                                                           |   5.148 μs (5%) |         |                 |             |
| `["gemm", "mul", "man", "true", "8"]`                                                            | 510.000 ns (5%) |         |                 |             |
| `["gemm", "mul", "xf", "false", "256"]`                                                          |   2.081 ms (5%) |         |   48 bytes (1%) |           2 |
| `["gemm", "mul", "xf", "false", "32"]`                                                           |   4.610 μs (5%) |         |   48 bytes (1%) |           2 |
| `["gemm", "mul", "xf", "false", "8"]`                                                            | 387.000 ns (5%) |         |   48 bytes (1%) |           2 |
| `["gemm", "mul", "xf", "ivdep", "256"]`                                                          |   2.028 ms (5%) |         |   48 bytes (1%) |           2 |
| `["gemm", "mul", "xf", "ivdep", "32"]`                                                           |   4.568 μs (5%) |         |   48 bytes (1%) |           2 |
| `["gemm", "mul", "xf", "ivdep", "8"]`                                                            | 447.000 ns (5%) |         |   48 bytes (1%) |           2 |
| `["gemm", "mul", "xf", "true", "256"]`                                                           |   2.058 ms (5%) |         |   48 bytes (1%) |           2 |
| `["gemm", "mul", "xf", "true", "32"]`                                                            |   4.917 μs (5%) |         |   48 bytes (1%) |           2 |
| `["gemm", "mul", "xf", "true", "8"]`                                                             | 413.000 ns (5%) |         |   48 bytes (1%) |           2 |
| `["groupby", "sum", "sac"]`                                                                      | 229.378 μs (5%) |         | 313.14 KiB (1%) |       10007 |
| `["groupby", "sum", "xf-with-init"]`                                                             | 163.219 μs (5%) |         | 157.44 KiB (1%) |       10008 |
| `["groupby", "sum", "xf-without-init"]`                                                          | 171.285 μs (5%) |         | 157.44 KiB (1%) |       10008 |
| `["mapcat_eduction", "base"]`                                                                    |   1.924 μs (5%) |         |                 |             |
| `["mapcat_eduction", "xf-eduction"]`                                                             |   1.688 μs (5%) |         |                 |             |
| `["mapcat_eduction", "xf-xf"]`                                                                   |   1.688 μs (5%) |         |                 |             |
| `["missing_argmax", "man"]`                                                                      |   2.365 μs (5%) |         |   32 bytes (1%) |           1 |
| `["missing_argmax", "rf"]`                                                                       |   2.858 μs (5%) |         |   32 bytes (1%) |           1 |
| `["missing_argmax", "xf"]`                                                                       |   2.317 μs (5%) |         |   32 bytes (1%) |           1 |
| `["missing_dot", "equiv"]`                                                                       |   1.578 μs (5%) |         |   16 bytes (1%) |           1 |
| `["missing_dot", "man"]`                                                                         |   1.373 μs (5%) |         |   16 bytes (1%) |           1 |
| `["missing_dot", "naive"]`                                                                       |   4.339 μs (5%) |         |   16 bytes (1%) |           1 |
| `["missing_dot", "rf"]`                                                                          |   1.266 μs (5%) |         |   16 bytes (1%) |           1 |
| `["missing_dot", "rf_nota"]`                                                                     |   1.464 μs (5%) |         |   16 bytes (1%) |           1 |
| `["missing_dot", "xf"]`                                                                          | 190.546 μs (5%) |         |  72.03 KiB (1%) |        3740 |
| `["missing_dot", "xf_nota"]`                                                                     | 186.197 μs (5%) |         |  72.17 KiB (1%) |        3742 |
| `["overhead", "foldl"]`                                                                          |   4.531 ns (5%) |         |                 |             |
| `["overhead", "reduce_basecase"]`                                                                | 236.161 ns (5%) |         |  464 bytes (1%) |           9 |
| `["partition_by", "man"]`                                                                        |   1.844 ms (5%) |         |  352 bytes (1%) |           4 |
| `["partition_by", "xf"]`                                                                         |   2.767 ms (5%) |         |   6.10 MiB (1%) |      200007 |
| `["set", "base"]`                                                                                |   4.362 ms (5%) |         |  49.58 KiB (1%) |          18 |
| `["set", "xf"]`                                                                                  |   3.979 ms (5%) |         |  49.63 KiB (1%) |          21 |

## Benchmark Group List
Here's a list of all the benchmark groups executed by this job:

- `["append!!"]`
- `["cat"]`
- `["collect"]`
- `["dict"]`
- `["dot"]`
- `["filter_map_map!"]`
- `["filter_map_reduce"]`
- `["filter_sum", ":n => 1000", ":xs => :RandomFloats", ":withinit => false"]`
- `["filter_sum", ":n => 1000", ":xs => :RandomFloats", ":withinit => true"]`
- `["filter_sum", ":n => 1000", ":xs => :UnitRange", ":withinit => false"]`
- `["filter_sum", ":n => 1000", ":xs => :UnitRange", ":withinit => true"]`
- `["filter_sum", ":n => 10000", ":xs => :RandomFloats", ":withinit => false"]`
- `["filter_sum", ":n => 10000", ":xs => :RandomFloats", ":withinit => true"]`
- `["filter_sum", ":n => 10000", ":xs => :UnitRange", ":withinit => false"]`
- `["filter_sum", ":n => 10000", ":xs => :UnitRange", ":withinit => true"]`
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
       #1  2800 MHz      51903 s          0 s       1402 s      42855 s          0 s
       #2  2800 MHz      42512 s          0 s       1110 s      52693 s          0 s
       
  Memory: 7.790031433105469 GB (5702.41796875 MB free)
  Uptime: 973.0 sec
  Load Avg:  1.0  1.0  0.72216796875
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
    CPU MHz:               2800.188
    BogoMIPS:              5600.37
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

