# Benchmark result (via Travis)


# Judge result
# Benchmark Report for */home/travis/build/JuliaFolds/Transducers.jl*

## Job Properties
* Time of benchmarks:
    - Target: 9 Aug 2020 - 05:05
    - Baseline: 9 Aug 2020 - 05:10
* Package commits:
    - Target: 6f7905
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

| ID                                       | time ratio                   | memory ratio |
|------------------------------------------|------------------------------|--------------|
| `["cat", "base"]`                        | 0.92 (5%) :white_check_mark: |   1.00 (1%)  |
| `["cat", "xf"]`                          |                1.17 (5%) :x: |   1.00 (1%)  |
| `["filter_map_map!", "man"]`             |                1.07 (5%) :x: |   1.00 (1%)  |
| `["filter_map_map!", "xf"]`              | 0.94 (5%) :white_check_mark: |   1.00 (1%)  |
| `["gemm", "fusedmul", "blas", "2"]`      |                1.05 (5%) :x: |   1.00 (1%)  |
| `["gemm", "fusedmul", "xf", "16"]`       | 0.90 (5%) :white_check_mark: |   1.00 (1%)  |
| `["gemm", "mul", "linalg", "8"]`         | 0.82 (5%) :white_check_mark: |   1.00 (1%)  |
| `["gemm", "mul", "man", "false", "32"]`  |                1.08 (5%) :x: |   1.00 (1%)  |
| `["gemm", "mul", "man", "false", "8"]`   |                1.18 (5%) :x: |   1.00 (1%)  |
| `["gemm", "mul", "man", "ivdep", "32"]`  |                1.10 (5%) :x: |   1.00 (1%)  |
| `["gemm", "mul", "man", "ivdep", "8"]`   | 0.93 (5%) :white_check_mark: |   1.00 (1%)  |
| `["gemm", "mul", "man", "true", "32"]`   |                1.08 (5%) :x: |   1.00 (1%)  |
| `["gemm", "mul", "man", "true", "8"]`    | 0.83 (5%) :white_check_mark: |   1.00 (1%)  |
| `["gemm", "mul", "xf", "false", "32"]`   | 0.77 (5%) :white_check_mark: |   1.00 (1%)  |
| `["gemm", "mul", "xf", "false", "8"]`    |                1.05 (5%) :x: |   1.00 (1%)  |
| `["gemm", "mul", "xf", "ivdep", "8"]`    | 0.90 (5%) :white_check_mark: |   1.00 (1%)  |
| `["gemm", "mul", "xf", "true", "32"]`    |                1.08 (5%) :x: |   1.00 (1%)  |
| `["gemm", "mul", "xf", "true", "8"]`     |                1.31 (5%) :x: |   1.00 (1%)  |
| `["groupby", "sum", "xf-with-init"]`     |                1.08 (5%) :x: |   1.00 (1%)  |
| `["mapcat_eduction", "base"]`            |                1.05 (5%) :x: |   1.00 (1%)  |
| `["mapcat_eduction", "xf-eduction"]`     |                1.06 (5%) :x: |   1.00 (1%)  |
| `["missing_argmax", "rf"]`               |                1.23 (5%) :x: |   1.00 (1%)  |
| `["missing_argmax", "xf"]`               | 0.81 (5%) :white_check_mark: |   1.00 (1%)  |
| `["overhead", "foldl"]`                  |                1.07 (5%) :x: |   1.00 (1%)  |

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
       #1  2800 MHz      44124 s          0 s       1263 s      32841 s          0 s
       #2  2800 MHz      32973 s          0 s       1106 s      45039 s          0 s
       
  Memory: 7.790031433105469 GB (5652.58984375 MB free)
  Uptime: 796.0 sec
  Load Avg:  1.0087890625  1.0  0.64453125
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
       #1  2800 MHz      53238 s          0 s       1424 s      50597 s          0 s
       #2  2800 MHz      50809 s          0 s       1203 s      54164 s          0 s
       
  Memory: 7.790031433105469 GB (5603.421875 MB free)
  Uptime: 1067.0 sec
  Load Avg:  1.0  1.0  0.74462890625
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-8.0.1 (ORCJIT, skylake)
```

---
# Target result
# Benchmark Report for */home/travis/build/JuliaFolds/Transducers.jl*

## Job Properties
* Time of benchmark: 9 Aug 2020 - 5:5
* Package commit: 6f7905
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
| `["append!!", "eduction"]`                                                                       |  18.562 μs (5%) |         |  64.72 KiB (1%) |          18 |
| `["append!!", "xf"]`                                                                             |  18.570 μs (5%) |         |  64.72 KiB (1%) |          18 |
| `["cat", "base"]`                                                                                |   1.632 μs (5%) |         |                 |             |
| `["cat", "xf"]`                                                                                  |   2.073 μs (5%) |         |                 |             |
| `["collect", "filter-missing"]`                                                                  | 106.729 μs (5%) |         | 345.31 KiB (1%) |       10015 |
| `["collect", "identity-float"]`                                                                  |  93.289 μs (5%) |         | 569.16 KiB (1%) |       10015 |
| `["collect", "identity-union"]`                                                                  | 301.469 μs (5%) |         | 705.38 KiB (1%) |       16681 |
| `["dict", "base"]`                                                                               |   3.577 ms (5%) |         |  92.91 KiB (1%) |          22 |
| `["dict", "xf"]`                                                                                 |   3.694 ms (5%) |         |  92.36 KiB (1%) |          21 |
| `["dot", "blas"]`                                                                                |   1.224 μs (5%) |         |                 |             |
| `["dot", "man"]`                                                                                 |   1.208 μs (5%) |         |                 |             |
| `["dot", "rf"]`                                                                                  |   2.149 μs (5%) |         |                 |             |
| `["dot", "xf"]`                                                                                  |   2.278 μs (5%) |         |   64 bytes (1%) |           3 |
| `["filter_map_map!", "man"]`                                                                     |  78.640 μs (5%) |         |                 |             |
| `["filter_map_map!", "xf"]`                                                                      | 626.643 μs (5%) |         |  304 bytes (1%) |          17 |
| `["filter_map_reduce", "man"]`                                                                   | 203.751 μs (5%) |         |                 |             |
| `["filter_map_reduce", "xf"]`                                                                    | 203.971 μs (5%) |         |                 |             |
| `["filter_sum", ":n => 1000", ":xs => :RandomFloats", ":withinit => false", ":impl => :base"]`   |   2.464 μs (5%) |         |                 |             |
| `["filter_sum", ":n => 1000", ":xs => :RandomFloats", ":withinit => false", ":impl => :naive"]`  |   1.183 μs (5%) |         |                 |             |
| `["filter_sum", ":n => 1000", ":xs => :RandomFloats", ":withinit => false", ":impl => :xf"]`     |   1.249 μs (5%) |         |                 |             |
| `["filter_sum", ":n => 1000", ":xs => :RandomFloats", ":withinit => true", ":impl => :base"]`    |   1.562 μs (5%) |         |                 |             |
| `["filter_sum", ":n => 1000", ":xs => :RandomFloats", ":withinit => true", ":impl => :naive"]`   | 690.574 ns (5%) |         |                 |             |
| `["filter_sum", ":n => 1000", ":xs => :RandomFloats", ":withinit => true", ":impl => :xf"]`      |   1.560 μs (5%) |         |                 |             |
| `["filter_sum", ":n => 1000", ":xs => :UnitRange", ":withinit => false", ":impl => :base"]`      |   1.631 μs (5%) |         |                 |             |
| `["filter_sum", ":n => 1000", ":xs => :UnitRange", ":withinit => false", ":impl => :naive"]`     | 739.984 ns (5%) |         |                 |             |
| `["filter_sum", ":n => 1000", ":xs => :UnitRange", ":withinit => false", ":impl => :xf"]`        |   1.477 μs (5%) |         |                 |             |
| `["filter_sum", ":n => 1000", ":xs => :UnitRange", ":withinit => true", ":impl => :base"]`       | 107.521 ns (5%) |         |                 |             |
| `["filter_sum", ":n => 1000", ":xs => :UnitRange", ":withinit => true", ":impl => :naive"]`      | 589.850 ns (5%) |         |                 |             |
| `["filter_sum", ":n => 1000", ":xs => :UnitRange", ":withinit => true", ":impl => :xf"]`         | 114.428 ns (5%) |         |                 |             |
| `["filter_sum", ":n => 10000", ":xs => :RandomFloats", ":withinit => false", ":impl => :base"]`  |  44.084 μs (5%) |         |                 |             |
| `["filter_sum", ":n => 10000", ":xs => :RandomFloats", ":withinit => false", ":impl => :naive"]` |  46.780 μs (5%) |         |                 |             |
| `["filter_sum", ":n => 10000", ":xs => :RandomFloats", ":withinit => false", ":impl => :xf"]`    |  40.192 μs (5%) |         |                 |             |
| `["filter_sum", ":n => 10000", ":xs => :RandomFloats", ":withinit => true", ":impl => :base"]`   |  15.846 μs (5%) |         |                 |             |
| `["filter_sum", ":n => 10000", ":xs => :RandomFloats", ":withinit => true", ":impl => :naive"]`  |  38.993 μs (5%) |         |                 |             |
| `["filter_sum", ":n => 10000", ":xs => :RandomFloats", ":withinit => true", ":impl => :xf"]`     |  15.838 μs (5%) |         |                 |             |
| `["filter_sum", ":n => 10000", ":xs => :UnitRange", ":withinit => false", ":impl => :base"]`     |  16.228 μs (5%) |         |                 |             |
| `["filter_sum", ":n => 10000", ":xs => :UnitRange", ":withinit => false", ":impl => :naive"]`    |   7.362 μs (5%) |         |                 |             |
| `["filter_sum", ":n => 10000", ":xs => :UnitRange", ":withinit => false", ":impl => :xf"]`       |  14.732 μs (5%) |         |                 |             |
| `["filter_sum", ":n => 10000", ":xs => :UnitRange", ":withinit => true", ":impl => :base"]`      |   1.032 μs (5%) |         |                 |             |
| `["filter_sum", ":n => 10000", ":xs => :UnitRange", ":withinit => true", ":impl => :naive"]`     |   5.886 μs (5%) |         |                 |             |
| `["filter_sum", ":n => 10000", ":xs => :UnitRange", ":withinit => true", ":impl => :xf"]`        |   1.096 μs (5%) |         |                 |             |
| `["findall", "base"]`                                                                            | 843.328 μs (5%) |         |   2.00 MiB (1%) |          21 |
| `["findall", "xf-array"]`                                                                        | 788.287 μs (5%) |         |   3.02 MiB (1%) |       98970 |
| `["findall", "xf-iter"]`                                                                         | 959.732 μs (5%) |         |   5.05 MiB (1%) |       99913 |
| `["gemm", "fusedmul", "blas", "16"]`                                                             |   6.310 ms (5%) |         |                 |             |
| `["gemm", "fusedmul", "blas", "2"]`                                                              |   4.874 ms (5%) |         |                 |             |
| `["gemm", "fusedmul", "blas", "32"]`                                                             |   8.510 ms (5%) |         |                 |             |
| `["gemm", "fusedmul", "blas", "8"]`                                                              |   5.344 ms (5%) |         |                 |             |
| `["gemm", "fusedmul", "xf", "16"]`                                                               |   4.724 ms (5%) |         |  160 bytes (1%) |           6 |
| `["gemm", "fusedmul", "xf", "2"]`                                                                | 649.503 μs (5%) |         |  160 bytes (1%) |           6 |
| `["gemm", "fusedmul", "xf", "32"]`                                                               |  10.162 ms (5%) |         |  160 bytes (1%) |           6 |
| `["gemm", "fusedmul", "xf", "8"]`                                                                |   2.474 ms (5%) |         |  160 bytes (1%) |           6 |
| `["gemm", "mul", "linalg", "256"]`                                                               | 973.344 μs (5%) |         |                 |             |
| `["gemm", "mul", "linalg", "32"]`                                                                |   3.340 μs (5%) |         |                 |             |
| `["gemm", "mul", "linalg", "8"]`                                                                 | 247.963 ns (5%) |         |                 |             |
| `["gemm", "mul", "man", "false", "256"]`                                                         |   2.047 ms (5%) |         |                 |             |
| `["gemm", "mul", "man", "false", "32"]`                                                          |   5.536 μs (5%) |         |                 |             |
| `["gemm", "mul", "man", "false", "8"]`                                                           | 511.667 ns (5%) |         |                 |             |
| `["gemm", "mul", "man", "ivdep", "256"]`                                                         |   2.022 ms (5%) |         |                 |             |
| `["gemm", "mul", "man", "ivdep", "32"]`                                                          |   4.751 μs (5%) |         |                 |             |
| `["gemm", "mul", "man", "ivdep", "8"]`                                                           | 398.239 ns (5%) |         |                 |             |
| `["gemm", "mul", "man", "true", "256"]`                                                          |   2.034 ms (5%) |         |                 |             |
| `["gemm", "mul", "man", "true", "32"]`                                                           |   5.626 μs (5%) |         |                 |             |
| `["gemm", "mul", "man", "true", "8"]`                                                            | 411.865 ns (5%) |         |                 |             |
| `["gemm", "mul", "xf", "false", "256"]`                                                          |   2.051 ms (5%) |         |   48 bytes (1%) |           2 |
| `["gemm", "mul", "xf", "false", "32"]`                                                           |   4.843 μs (5%) |         |   48 bytes (1%) |           2 |
| `["gemm", "mul", "xf", "false", "8"]`                                                            | 402.209 ns (5%) |         |   48 bytes (1%) |           2 |
| `["gemm", "mul", "xf", "ivdep", "256"]`                                                          |   2.016 ms (5%) |         |   48 bytes (1%) |           2 |
| `["gemm", "mul", "xf", "ivdep", "32"]`                                                           |   4.581 μs (5%) |         |   48 bytes (1%) |           2 |
| `["gemm", "mul", "xf", "ivdep", "8"]`                                                            | 449.631 ns (5%) |         |   48 bytes (1%) |           2 |
| `["gemm", "mul", "xf", "true", "256"]`                                                           |   2.044 ms (5%) |         |   48 bytes (1%) |           2 |
| `["gemm", "mul", "xf", "true", "32"]`                                                            |   5.478 μs (5%) |         |   48 bytes (1%) |           2 |
| `["gemm", "mul", "xf", "true", "8"]`                                                             | 499.005 ns (5%) |         |   48 bytes (1%) |           2 |
| `["groupby", "sum", "sac"]`                                                                      | 226.758 μs (5%) |         | 313.14 KiB (1%) |       10007 |
| `["groupby", "sum", "xf-with-init"]`                                                             | 175.584 μs (5%) |         | 157.44 KiB (1%) |       10008 |
| `["groupby", "sum", "xf-without-init"]`                                                          | 172.784 μs (5%) |         | 157.44 KiB (1%) |       10008 |
| `["mapcat_eduction", "base"]`                                                                    |   2.026 μs (5%) |         |                 |             |
| `["mapcat_eduction", "xf-eduction"]`                                                             |   1.780 μs (5%) |         |                 |             |
| `["mapcat_eduction", "xf-xf"]`                                                                   |   1.685 μs (5%) |         |                 |             |
| `["missing_argmax", "man"]`                                                                      |   2.365 μs (5%) |         |   32 bytes (1%) |           1 |
| `["missing_argmax", "rf"]`                                                                       |   2.852 μs (5%) |         |   32 bytes (1%) |           1 |
| `["missing_argmax", "xf"]`                                                                       |   2.299 μs (5%) |         |   32 bytes (1%) |           1 |
| `["missing_dot", "equiv"]`                                                                       |   1.556 μs (5%) |         |   16 bytes (1%) |           1 |
| `["missing_dot", "man"]`                                                                         |   1.393 μs (5%) |         |   16 bytes (1%) |           1 |
| `["missing_dot", "naive"]`                                                                       |   4.352 μs (5%) |         |   16 bytes (1%) |           1 |
| `["missing_dot", "rf"]`                                                                          |   1.252 μs (5%) |         |   16 bytes (1%) |           1 |
| `["missing_dot", "rf_nota"]`                                                                     |   1.551 μs (5%) |         |   16 bytes (1%) |           1 |
| `["missing_dot", "xf"]`                                                                          | 188.379 μs (5%) |         |  72.19 KiB (1%) |        3744 |
| `["missing_dot", "xf_nota"]`                                                                     | 187.200 μs (5%) |         |  72.31 KiB (1%) |        3750 |
| `["overhead", "foldl"]`                                                                          |   4.447 ns (5%) |         |                 |             |
| `["overhead", "reduce_basecase"]`                                                                | 242.781 ns (5%) |         |  464 bytes (1%) |           9 |
| `["partition_by", "man"]`                                                                        |   1.846 ms (5%) |         |  352 bytes (1%) |           4 |
| `["partition_by", "xf"]`                                                                         |   2.893 ms (5%) |         |   6.10 MiB (1%) |      200007 |
| `["set", "base"]`                                                                                |   4.274 ms (5%) |         |  49.58 KiB (1%) |          18 |
| `["set", "xf"]`                                                                                  |   3.978 ms (5%) |         |  49.63 KiB (1%) |          21 |

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
       #1  2800 MHz      44124 s          0 s       1263 s      32841 s          0 s
       #2  2800 MHz      32973 s          0 s       1106 s      45039 s          0 s
       
  Memory: 7.790031433105469 GB (5652.58984375 MB free)
  Uptime: 796.0 sec
  Load Avg:  1.0087890625  1.0  0.64453125
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-8.0.1 (ORCJIT, skylake)
```

---
# Baseline result
# Benchmark Report for */home/travis/build/JuliaFolds/Transducers.jl*

## Job Properties
* Time of benchmark: 9 Aug 2020 - 5:10
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
| `["append!!", "eduction"]`               |  18.911 μs (5%) |         |  64.72 KiB (1%) |          18 |
| `["append!!", "xf"]`                     |  18.780 μs (5%) |         |  64.72 KiB (1%) |          18 |
| `["cat", "base"]`                        |   1.777 μs (5%) |         |                 |             |
| `["cat", "xf"]`                          |   1.773 μs (5%) |         |                 |             |
| `["collect", "filter-missing"]`          | 106.278 μs (5%) |         | 345.31 KiB (1%) |       10015 |
| `["collect", "identity-float"]`          |  91.855 μs (5%) |         | 569.16 KiB (1%) |       10015 |
| `["collect", "identity-union"]`          | 304.531 μs (5%) |         | 704.89 KiB (1%) |       16648 |
| `["dict", "base"]`                       |   3.603 ms (5%) |         |  92.91 KiB (1%) |          22 |
| `["dict", "xf"]`                         |   3.682 ms (5%) |         |  92.36 KiB (1%) |          21 |
| `["dot", "blas"]`                        |   1.217 μs (5%) |         |                 |             |
| `["dot", "man"]`                         |   1.199 μs (5%) |         |                 |             |
| `["dot", "rf"]`                          |   2.142 μs (5%) |         |                 |             |
| `["dot", "xf"]`                          |   2.272 μs (5%) |         |   64 bytes (1%) |           3 |
| `["filter_map_map!", "man"]`             |  73.593 μs (5%) |         |                 |             |
| `["filter_map_map!", "xf"]`              | 667.865 μs (5%) |         |  304 bytes (1%) |          17 |
| `["filter_map_reduce", "man"]`           | 202.843 μs (5%) |         |                 |             |
| `["filter_map_reduce", "xf"]`            | 203.785 μs (5%) |         |                 |             |
| `["findall", "base"]`                    | 836.216 μs (5%) |         |   2.00 MiB (1%) |          21 |
| `["findall", "xf-array"]`                | 793.004 μs (5%) |         |   3.05 MiB (1%) |       99770 |
| `["findall", "xf-iter"]`                 | 957.565 μs (5%) |         |   5.05 MiB (1%) |       99937 |
| `["gemm", "fusedmul", "blas", "16"]`     |   6.476 ms (5%) |         |                 |             |
| `["gemm", "fusedmul", "blas", "2"]`      |   4.626 ms (5%) |         |                 |             |
| `["gemm", "fusedmul", "blas", "32"]`     |   8.638 ms (5%) |         |                 |             |
| `["gemm", "fusedmul", "blas", "8"]`      |   5.175 ms (5%) |         |                 |             |
| `["gemm", "fusedmul", "xf", "16"]`       |   5.278 ms (5%) |         |  160 bytes (1%) |           6 |
| `["gemm", "fusedmul", "xf", "2"]`        | 659.051 μs (5%) |         |  160 bytes (1%) |           6 |
| `["gemm", "fusedmul", "xf", "32"]`       |  10.578 ms (5%) |         |  160 bytes (1%) |           6 |
| `["gemm", "fusedmul", "xf", "8"]`        |   2.437 ms (5%) |         |  160 bytes (1%) |           6 |
| `["gemm", "mul", "linalg", "256"]`       | 969.671 μs (5%) |         |                 |             |
| `["gemm", "mul", "linalg", "32"]`        |   3.206 μs (5%) |         |                 |             |
| `["gemm", "mul", "linalg", "8"]`         | 304.000 ns (5%) |         |                 |             |
| `["gemm", "mul", "man", "false", "256"]` |   1.986 ms (5%) |         |                 |             |
| `["gemm", "mul", "man", "false", "32"]`  |   5.117 μs (5%) |         |                 |             |
| `["gemm", "mul", "man", "false", "8"]`   | 434.000 ns (5%) |         |                 |             |
| `["gemm", "mul", "man", "ivdep", "256"]` |   1.946 ms (5%) |         |                 |             |
| `["gemm", "mul", "man", "ivdep", "32"]`  |   4.338 μs (5%) |         |                 |             |
| `["gemm", "mul", "man", "ivdep", "8"]`   | 428.000 ns (5%) |         |                 |             |
| `["gemm", "mul", "man", "true", "256"]`  |   1.969 ms (5%) |         |                 |             |
| `["gemm", "mul", "man", "true", "32"]`   |   5.223 μs (5%) |         |                 |             |
| `["gemm", "mul", "man", "true", "8"]`    | 498.000 ns (5%) |         |                 |             |
| `["gemm", "mul", "xf", "false", "256"]`  |   1.986 ms (5%) |         |   48 bytes (1%) |           2 |
| `["gemm", "mul", "xf", "false", "32"]`   |   6.273 μs (5%) |         |   48 bytes (1%) |           2 |
| `["gemm", "mul", "xf", "false", "8"]`    | 383.000 ns (5%) |         |   48 bytes (1%) |           2 |
| `["gemm", "mul", "xf", "ivdep", "256"]`  |   1.941 ms (5%) |         |   48 bytes (1%) |           2 |
| `["gemm", "mul", "xf", "ivdep", "32"]`   |   4.472 μs (5%) |         |   48 bytes (1%) |           2 |
| `["gemm", "mul", "xf", "ivdep", "8"]`    | 498.000 ns (5%) |         |   48 bytes (1%) |           2 |
| `["gemm", "mul", "xf", "true", "256"]`   |   2.020 ms (5%) |         |   48 bytes (1%) |           2 |
| `["gemm", "mul", "xf", "true", "32"]`    |   5.084 μs (5%) |         |   48 bytes (1%) |           2 |
| `["gemm", "mul", "xf", "true", "8"]`     | 381.000 ns (5%) |         |   48 bytes (1%) |           2 |
| `["groupby", "sum", "sac"]`              | 231.605 μs (5%) |         | 313.14 KiB (1%) |       10007 |
| `["groupby", "sum", "xf-with-init"]`     | 163.288 μs (5%) |         | 157.44 KiB (1%) |       10008 |
| `["groupby", "sum", "xf-without-init"]`  | 170.356 μs (5%) |         | 157.44 KiB (1%) |       10008 |
| `["mapcat_eduction", "base"]`            |   1.927 μs (5%) |         |                 |             |
| `["mapcat_eduction", "xf-eduction"]`     |   1.687 μs (5%) |         |                 |             |
| `["mapcat_eduction", "xf-xf"]`           |   1.686 μs (5%) |         |                 |             |
| `["missing_argmax", "man"]`              |   2.365 μs (5%) |         |   32 bytes (1%) |           1 |
| `["missing_argmax", "rf"]`               |   2.314 μs (5%) |         |   32 bytes (1%) |           1 |
| `["missing_argmax", "xf"]`               |   2.838 μs (5%) |         |   32 bytes (1%) |           1 |
| `["missing_dot", "equiv"]`               |   1.532 μs (5%) |         |   16 bytes (1%) |           1 |
| `["missing_dot", "man"]`                 |   1.384 μs (5%) |         |   16 bytes (1%) |           1 |
| `["missing_dot", "naive"]`               |   4.323 μs (5%) |         |   16 bytes (1%) |           1 |
| `["missing_dot", "rf"]`                  |   1.270 μs (5%) |         |   16 bytes (1%) |           1 |
| `["missing_dot", "rf_nota"]`             |   1.546 μs (5%) |         |   16 bytes (1%) |           1 |
| `["missing_dot", "xf"]`                  | 186.075 μs (5%) |         |  72.09 KiB (1%) |        3740 |
| `["missing_dot", "xf_nota"]`             | 181.574 μs (5%) |         |  72.02 KiB (1%) |        3738 |
| `["overhead", "foldl"]`                  |   4.147 ns (5%) |         |                 |             |
| `["overhead", "reduce_basecase"]`        | 239.854 ns (5%) |         |  464 bytes (1%) |           9 |
| `["partition_by", "man"]`                |   1.845 ms (5%) |         |  352 bytes (1%) |           4 |
| `["partition_by", "xf"]`                 |   2.844 ms (5%) |         |   6.10 MiB (1%) |      200007 |
| `["set", "base"]`                        |   4.237 ms (5%) |         |  49.58 KiB (1%) |          18 |
| `["set", "xf"]`                          |   3.995 ms (5%) |         |  49.63 KiB (1%) |          21 |

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
       #1  2800 MHz      53238 s          0 s       1424 s      50597 s          0 s
       #2  2800 MHz      50809 s          0 s       1203 s      54164 s          0 s
       
  Memory: 7.790031433105469 GB (5603.421875 MB free)
  Uptime: 1067.0 sec
  Load Avg:  1.0  1.0  0.74462890625
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

