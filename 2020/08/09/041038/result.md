# Benchmark result (via Travis)


# Judge result
# Benchmark Report for */home/travis/build/JuliaFolds/Transducers.jl*

## Job Properties
* Time of benchmarks:
    - Target: 9 Aug 2020 - 04:05
    - Baseline: 9 Aug 2020 - 04:09
* Package commits:
    - Target: a8816d
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
| `["filter_map_map!", "xf"]`              | 0.94 (5%) :white_check_mark: |   1.00 (1%)  |
| `["gemm", "fusedmul", "xf", "16"]`       |                1.07 (5%) :x: |   1.00 (1%)  |
| `["gemm", "mul", "linalg", "8"]`         | 0.87 (5%) :white_check_mark: |   1.00 (1%)  |
| `["gemm", "mul", "man", "false", "256"]` |                1.06 (5%) :x: |   1.00 (1%)  |
| `["gemm", "mul", "man", "false", "32"]`  |                1.09 (5%) :x: |   1.00 (1%)  |
| `["gemm", "mul", "man", "false", "8"]`   |                1.18 (5%) :x: |   1.00 (1%)  |
| `["gemm", "mul", "man", "ivdep", "32"]`  |                1.09 (5%) :x: |   1.00 (1%)  |
| `["gemm", "mul", "man", "true", "256"]`  |                1.06 (5%) :x: |   1.00 (1%)  |
| `["gemm", "mul", "man", "true", "32"]`   |                1.08 (5%) :x: |   1.00 (1%)  |
| `["gemm", "mul", "man", "true", "8"]`    | 0.76 (5%) :white_check_mark: |   1.00 (1%)  |
| `["gemm", "mul", "xf", "false", "256"]`  |                1.06 (5%) :x: |   1.00 (1%)  |
| `["gemm", "mul", "xf", "false", "32"]`   | 0.88 (5%) :white_check_mark: |   1.00 (1%)  |
| `["gemm", "mul", "xf", "false", "8"]`    |                1.21 (5%) :x: |   1.00 (1%)  |
| `["gemm", "mul", "xf", "ivdep", "8"]`    | 0.93 (5%) :white_check_mark: |   1.00 (1%)  |
| `["gemm", "mul", "xf", "true", "32"]`    |                1.25 (5%) :x: |   1.00 (1%)  |
| `["gemm", "mul", "xf", "true", "8"]`     |                1.28 (5%) :x: |   1.00 (1%)  |
| `["groupby", "sum", "sac"]`              | 0.92 (5%) :white_check_mark: |   1.00 (1%)  |
| `["groupby", "sum", "xf-without-init"]`  | 0.91 (5%) :white_check_mark: |   1.00 (1%)  |
| `["mapcat_eduction", "base"]`            | 0.94 (5%) :white_check_mark: |   1.00 (1%)  |
| `["mapcat_eduction", "xf-eduction"]`     |                1.06 (5%) :x: |   1.00 (1%)  |
| `["missing_argmax", "rf"]`               |                1.24 (5%) :x: |   1.00 (1%)  |
| `["missing_argmax", "xf"]`               | 0.80 (5%) :white_check_mark: |   1.00 (1%)  |
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
       #1  2800 MHz      63352 s          0 s       1353 s       6741 s          0 s
       #2  2800 MHz       6337 s          0 s       1042 s      64100 s          0 s
       
  Memory: 7.790031433105469 GB (5632.640625 MB free)
  Uptime: 724.0 sec
  Load Avg:  1.00341796875  0.9697265625  0.61376953125
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
       #1  2800 MHz      68043 s          0 s       1446 s      29047 s          0 s
       #2  2800 MHz      28672 s          0 s       1202 s      68741 s          0 s
       
  Memory: 7.790031433105469 GB (5664.46484375 MB free)
  Uptime: 996.0 sec
  Load Avg:  1.0  0.9970703125  0.72607421875
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-8.0.1 (ORCJIT, skylake)
```

---
# Target result
# Benchmark Report for */home/travis/build/JuliaFolds/Transducers.jl*

## Job Properties
* Time of benchmark: 9 Aug 2020 - 4:5
* Package commit: a8816d
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
| `["append!!", "eduction"]`                                                  |  18.974 μs (5%) |         |  64.72 KiB (1%) |          18 |
| `["append!!", "xf"]`                                                        |  18.946 μs (5%) |         |  64.72 KiB (1%) |          18 |
| `["cat", "base"]`                                                           |   1.634 μs (5%) |         |                 |             |
| `["cat", "xf"]`                                                             |   2.074 μs (5%) |         |                 |             |
| `["collect", "filter-missing"]`                                             | 106.499 μs (5%) |         | 345.31 KiB (1%) |       10015 |
| `["collect", "identity-float"]`                                             |  94.402 μs (5%) |         | 569.16 KiB (1%) |       10015 |
| `["collect", "identity-union"]`                                             | 305.625 μs (5%) |         | 705.17 KiB (1%) |       16668 |
| `["dict", "base"]`                                                          |   3.601 ms (5%) |         |  92.91 KiB (1%) |          22 |
| `["dict", "xf"]`                                                            |   3.691 ms (5%) |         |  92.36 KiB (1%) |          21 |
| `["dot", "blas"]`                                                           |   1.228 μs (5%) |         |                 |             |
| `["dot", "man"]`                                                            |   1.197 μs (5%) |         |                 |             |
| `["dot", "rf"]`                                                             |   2.209 μs (5%) |         |                 |             |
| `["dot", "xf"]`                                                             |   2.270 μs (5%) |         |   64 bytes (1%) |           3 |
| `["filter_map_map!", "man"]`                                                |  77.693 μs (5%) |         |                 |             |
| `["filter_map_map!", "xf"]`                                                 | 627.488 μs (5%) |         |  304 bytes (1%) |          17 |
| `["filter_map_reduce", "man"]`                                              | 203.879 μs (5%) |         |                 |             |
| `["filter_map_reduce", "xf"]`                                               | 203.890 μs (5%) |         |                 |             |
| `["filter_sum", ":xs => :floats", ":withinit => false", ":impl => :base"]`  |   2.381 μs (5%) |         |                 |             |
| `["filter_sum", ":xs => :floats", ":withinit => false", ":impl => :naive"]` |   1.209 μs (5%) |         |                 |             |
| `["filter_sum", ":xs => :floats", ":withinit => false", ":impl => :xf"]`    |   1.152 μs (5%) |         |                 |             |
| `["filter_sum", ":xs => :floats", ":withinit => true", ":impl => :base"]`   |   1.148 μs (5%) |         |                 |             |
| `["filter_sum", ":xs => :floats", ":withinit => true", ":impl => :naive"]`  |   1.328 μs (5%) |         |                 |             |
| `["filter_sum", ":xs => :floats", ":withinit => true", ":impl => :xf"]`     |   1.148 μs (5%) |         |                 |             |
| `["filter_sum", ":xs => :ints", ":withinit => false", ":impl => :base"]`    |   1.638 μs (5%) |         |                 |             |
| `["filter_sum", ":xs => :ints", ":withinit => false", ":impl => :naive"]`   |   1.043 μs (5%) |         |                 |             |
| `["filter_sum", ":xs => :ints", ":withinit => false", ":impl => :xf"]`      |   1.478 μs (5%) |         |                 |             |
| `["filter_sum", ":xs => :ints", ":withinit => true", ":impl => :base"]`     | 108.254 ns (5%) |         |                 |             |
| `["filter_sum", ":xs => :ints", ":withinit => true", ":impl => :naive"]`    | 591.217 ns (5%) |         |                 |             |
| `["filter_sum", ":xs => :ints", ":withinit => true", ":impl => :xf"]`       | 115.648 ns (5%) |         |                 |             |
| `["findall", "base"]`                                                       | 872.112 μs (5%) |         |   2.00 MiB (1%) |          21 |
| `["findall", "xf-array"]`                                                   | 792.643 μs (5%) |         |   3.03 MiB (1%) |       99216 |
| `["findall", "xf-iter"]`                                                    | 980.061 μs (5%) |         |   5.05 MiB (1%) |       99942 |
| `["gemm", "fusedmul", "blas", "16"]`                                        |   6.484 ms (5%) |         |                 |             |
| `["gemm", "fusedmul", "blas", "2"]`                                         |   4.671 ms (5%) |         |                 |             |
| `["gemm", "fusedmul", "blas", "32"]`                                        |   8.764 ms (5%) |         |                 |             |
| `["gemm", "fusedmul", "blas", "8"]`                                         |   5.417 ms (5%) |         |                 |             |
| `["gemm", "fusedmul", "xf", "16"]`                                          |   5.151 ms (5%) |         |  160 bytes (1%) |           6 |
| `["gemm", "fusedmul", "xf", "2"]`                                           | 618.501 μs (5%) |         |  160 bytes (1%) |           6 |
| `["gemm", "fusedmul", "xf", "32"]`                                          |  10.453 ms (5%) |         |  160 bytes (1%) |           6 |
| `["gemm", "fusedmul", "xf", "8"]`                                           |   2.558 ms (5%) |         |  160 bytes (1%) |           6 |
| `["gemm", "mul", "linalg", "256"]`                                          | 969.830 μs (5%) |         |                 |             |
| `["gemm", "mul", "linalg", "32"]`                                           |   3.105 μs (5%) |         |                 |             |
| `["gemm", "mul", "linalg", "8"]`                                            | 262.901 ns (5%) |         |                 |             |
| `["gemm", "mul", "man", "false", "256"]`                                    |   2.075 ms (5%) |         |                 |             |
| `["gemm", "mul", "man", "false", "32"]`                                     |   5.550 μs (5%) |         |                 |             |
| `["gemm", "mul", "man", "false", "8"]`                                      | 512.380 ns (5%) |         |                 |             |
| `["gemm", "mul", "man", "ivdep", "256"]`                                    |   2.034 ms (5%) |         |                 |             |
| `["gemm", "mul", "man", "ivdep", "32"]`                                     |   4.749 μs (5%) |         |                 |             |
| `["gemm", "mul", "man", "ivdep", "8"]`                                      | 400.076 ns (5%) |         |                 |             |
| `["gemm", "mul", "man", "true", "256"]`                                     |   2.060 ms (5%) |         |                 |             |
| `["gemm", "mul", "man", "true", "32"]`                                      |   5.640 μs (5%) |         |                 |             |
| `["gemm", "mul", "man", "true", "8"]`                                       | 411.995 ns (5%) |         |                 |             |
| `["gemm", "mul", "xf", "false", "256"]`                                     |   2.080 ms (5%) |         |   48 bytes (1%) |           2 |
| `["gemm", "mul", "xf", "false", "32"]`                                      |   5.548 μs (5%) |         |   48 bytes (1%) |           2 |
| `["gemm", "mul", "xf", "false", "8"]`                                       | 471.133 ns (5%) |         |   48 bytes (1%) |           2 |
| `["gemm", "mul", "xf", "ivdep", "256"]`                                     |   2.024 ms (5%) |         |   48 bytes (1%) |           2 |
| `["gemm", "mul", "xf", "ivdep", "32"]`                                      |   4.587 μs (5%) |         |   48 bytes (1%) |           2 |
| `["gemm", "mul", "xf", "ivdep", "8"]`                                       | 457.492 ns (5%) |         |   48 bytes (1%) |           2 |
| `["gemm", "mul", "xf", "true", "256"]`                                      |   2.073 ms (5%) |         |   48 bytes (1%) |           2 |
| `["gemm", "mul", "xf", "true", "32"]`                                       |   6.395 μs (5%) |         |   48 bytes (1%) |           2 |
| `["gemm", "mul", "xf", "true", "8"]`                                        | 498.868 ns (5%) |         |   48 bytes (1%) |           2 |
| `["groupby", "sum", "sac"]`                                                 | 226.650 μs (5%) |         | 313.14 KiB (1%) |       10007 |
| `["groupby", "sum", "xf-with-init"]`                                        | 175.235 μs (5%) |         | 157.44 KiB (1%) |       10008 |
| `["groupby", "sum", "xf-without-init"]`                                     | 170.178 μs (5%) |         | 157.44 KiB (1%) |       10008 |
| `["mapcat_eduction", "base"]`                                               |   1.926 μs (5%) |         |                 |             |
| `["mapcat_eduction", "xf-eduction"]`                                        |   1.781 μs (5%) |         |                 |             |
| `["mapcat_eduction", "xf-xf"]`                                              |   1.688 μs (5%) |         |                 |             |
| `["missing_argmax", "man"]`                                                 |   2.366 μs (5%) |         |   32 bytes (1%) |           1 |
| `["missing_argmax", "rf"]`                                                  |   2.860 μs (5%) |         |   32 bytes (1%) |           1 |
| `["missing_argmax", "xf"]`                                                  |   2.284 μs (5%) |         |   32 bytes (1%) |           1 |
| `["missing_dot", "equiv"]`                                                  |   1.554 μs (5%) |         |   16 bytes (1%) |           1 |
| `["missing_dot", "man"]`                                                    |   1.378 μs (5%) |         |   16 bytes (1%) |           1 |
| `["missing_dot", "naive"]`                                                  |   4.309 μs (5%) |         |   16 bytes (1%) |           1 |
| `["missing_dot", "rf"]`                                                     |   1.293 μs (5%) |         |   16 bytes (1%) |           1 |
| `["missing_dot", "rf_nota"]`                                                |   1.547 μs (5%) |         |   16 bytes (1%) |           1 |
| `["missing_dot", "xf"]`                                                     | 187.863 μs (5%) |         |  71.92 KiB (1%) |        3732 |
| `["missing_dot", "xf_nota"]`                                                | 186.802 μs (5%) |         |  72.14 KiB (1%) |        3742 |
| `["overhead", "foldl"]`                                                     |   4.445 ns (5%) |         |                 |             |
| `["overhead", "reduce_basecase"]`                                           | 242.834 ns (5%) |         |  464 bytes (1%) |           9 |
| `["partition_by", "man"]`                                                   |   1.805 ms (5%) |         |  352 bytes (1%) |           4 |
| `["partition_by", "xf"]`                                                    |   2.844 ms (5%) |         |   6.10 MiB (1%) |      200007 |
| `["set", "base"]`                                                           |   4.273 ms (5%) |         |  49.58 KiB (1%) |          18 |
| `["set", "xf"]`                                                             |   3.970 ms (5%) |         |  49.63 KiB (1%) |          21 |

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
       #1  2800 MHz      63352 s          0 s       1353 s       6741 s          0 s
       #2  2800 MHz       6337 s          0 s       1042 s      64100 s          0 s
       
  Memory: 7.790031433105469 GB (5632.640625 MB free)
  Uptime: 724.0 sec
  Load Avg:  1.00341796875  0.9697265625  0.61376953125
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-8.0.1 (ORCJIT, skylake)
```

---
# Baseline result
# Benchmark Report for */home/travis/build/JuliaFolds/Transducers.jl*

## Job Properties
* Time of benchmark: 9 Aug 2020 - 4:9
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
| `["append!!", "eduction"]`               |  18.849 μs (5%) |         |  64.72 KiB (1%) |          18 |
| `["append!!", "xf"]`                     |  18.765 μs (5%) |         |  64.72 KiB (1%) |          18 |
| `["cat", "base"]`                        |   1.778 μs (5%) |         |                 |             |
| `["cat", "xf"]`                          |   1.773 μs (5%) |         |                 |             |
| `["collect", "filter-missing"]`          | 106.424 μs (5%) |         | 345.31 KiB (1%) |       10015 |
| `["collect", "identity-float"]`          |  92.652 μs (5%) |         | 569.16 KiB (1%) |       10015 |
| `["collect", "identity-union"]`          | 305.896 μs (5%) |         | 705.25 KiB (1%) |       16673 |
| `["dict", "base"]`                       |   3.605 ms (5%) |         |  92.91 KiB (1%) |          22 |
| `["dict", "xf"]`                         |   3.689 ms (5%) |         |  92.36 KiB (1%) |          21 |
| `["dot", "blas"]`                        |   1.220 μs (5%) |         |                 |             |
| `["dot", "man"]`                         |   1.183 μs (5%) |         |                 |             |
| `["dot", "rf"]`                          |   2.148 μs (5%) |         |                 |             |
| `["dot", "xf"]`                          |   2.274 μs (5%) |         |   64 bytes (1%) |           3 |
| `["filter_map_map!", "man"]`             |  77.821 μs (5%) |         |                 |             |
| `["filter_map_map!", "xf"]`              | 667.418 μs (5%) |         |  304 bytes (1%) |          17 |
| `["filter_map_reduce", "man"]`           | 202.887 μs (5%) |         |                 |             |
| `["filter_map_reduce", "xf"]`            | 203.920 μs (5%) |         |                 |             |
| `["findall", "base"]`                    | 838.281 μs (5%) |         |   2.00 MiB (1%) |          21 |
| `["findall", "xf-array"]`                | 786.946 μs (5%) |         |   3.05 MiB (1%) |       99769 |
| `["findall", "xf-iter"]`                 | 952.561 μs (5%) |         |   5.05 MiB (1%) |       99925 |
| `["gemm", "fusedmul", "blas", "16"]`     |   6.488 ms (5%) |         |                 |             |
| `["gemm", "fusedmul", "blas", "2"]`      |   4.705 ms (5%) |         |                 |             |
| `["gemm", "fusedmul", "blas", "32"]`     |   8.822 ms (5%) |         |                 |             |
| `["gemm", "fusedmul", "blas", "8"]`      |   5.220 ms (5%) |         |                 |             |
| `["gemm", "fusedmul", "xf", "16"]`       |   4.792 ms (5%) |         |  160 bytes (1%) |           6 |
| `["gemm", "fusedmul", "xf", "2"]`        | 602.953 μs (5%) |         |  160 bytes (1%) |           6 |
| `["gemm", "fusedmul", "xf", "32"]`       |  10.290 ms (5%) |         |  160 bytes (1%) |           6 |
| `["gemm", "fusedmul", "xf", "8"]`        |   2.545 ms (5%) |         |  160 bytes (1%) |           6 |
| `["gemm", "mul", "linalg", "256"]`       | 976.628 μs (5%) |         |                 |             |
| `["gemm", "mul", "linalg", "32"]`        |   3.212 μs (5%) |         |                 |             |
| `["gemm", "mul", "linalg", "8"]`         | 302.000 ns (5%) |         |                 |             |
| `["gemm", "mul", "man", "false", "256"]` |   1.962 ms (5%) |         |                 |             |
| `["gemm", "mul", "man", "false", "32"]`  |   5.103 μs (5%) |         |                 |             |
| `["gemm", "mul", "man", "false", "8"]`   | 435.000 ns (5%) |         |                 |             |
| `["gemm", "mul", "man", "ivdep", "256"]` |   1.943 ms (5%) |         |                 |             |
| `["gemm", "mul", "man", "ivdep", "32"]`  |   4.345 μs (5%) |         |                 |             |
| `["gemm", "mul", "man", "ivdep", "8"]`   | 407.000 ns (5%) |         |                 |             |
| `["gemm", "mul", "man", "true", "256"]`  |   1.948 ms (5%) |         |                 |             |
| `["gemm", "mul", "man", "true", "32"]`   |   5.214 μs (5%) |         |                 |             |
| `["gemm", "mul", "man", "true", "8"]`    | 540.000 ns (5%) |         |                 |             |
| `["gemm", "mul", "xf", "false", "256"]`  |   1.963 ms (5%) |         |   48 bytes (1%) |           2 |
| `["gemm", "mul", "xf", "false", "32"]`   |   6.269 μs (5%) |         |   48 bytes (1%) |           2 |
| `["gemm", "mul", "xf", "false", "8"]`    | 389.000 ns (5%) |         |   48 bytes (1%) |           2 |
| `["gemm", "mul", "xf", "ivdep", "256"]`  |   1.945 ms (5%) |         |   48 bytes (1%) |           2 |
| `["gemm", "mul", "xf", "ivdep", "32"]`   |   4.483 μs (5%) |         |   48 bytes (1%) |           2 |
| `["gemm", "mul", "xf", "ivdep", "8"]`    | 492.000 ns (5%) |         |   48 bytes (1%) |           2 |
| `["gemm", "mul", "xf", "true", "256"]`   |   1.984 ms (5%) |         |   48 bytes (1%) |           2 |
| `["gemm", "mul", "xf", "true", "32"]`    |   5.099 μs (5%) |         |   48 bytes (1%) |           2 |
| `["gemm", "mul", "xf", "true", "8"]`     | 390.000 ns (5%) |         |   48 bytes (1%) |           2 |
| `["groupby", "sum", "sac"]`              | 246.558 μs (5%) |         | 313.14 KiB (1%) |       10007 |
| `["groupby", "sum", "xf-with-init"]`     | 179.411 μs (5%) |         | 157.44 KiB (1%) |       10008 |
| `["groupby", "sum", "xf-without-init"]`  | 187.731 μs (5%) |         | 157.44 KiB (1%) |       10008 |
| `["mapcat_eduction", "base"]`            |   2.041 μs (5%) |         |                 |             |
| `["mapcat_eduction", "xf-eduction"]`     |   1.687 μs (5%) |         |                 |             |
| `["mapcat_eduction", "xf-xf"]`           |   1.687 μs (5%) |         |                 |             |
| `["missing_argmax", "man"]`              |   2.365 μs (5%) |         |   32 bytes (1%) |           1 |
| `["missing_argmax", "rf"]`               |   2.304 μs (5%) |         |   32 bytes (1%) |           1 |
| `["missing_argmax", "xf"]`               |   2.853 μs (5%) |         |   32 bytes (1%) |           1 |
| `["missing_dot", "equiv"]`               |   1.537 μs (5%) |         |   16 bytes (1%) |           1 |
| `["missing_dot", "man"]`                 |   1.326 μs (5%) |         |   16 bytes (1%) |           1 |
| `["missing_dot", "naive"]`               |   4.325 μs (5%) |         |   16 bytes (1%) |           1 |
| `["missing_dot", "rf"]`                  |   1.265 μs (5%) |         |   16 bytes (1%) |           1 |
| `["missing_dot", "rf_nota"]`             |   1.547 μs (5%) |         |   16 bytes (1%) |           1 |
| `["missing_dot", "xf"]`                  | 188.011 μs (5%) |         |  71.59 KiB (1%) |        3719 |
| `["missing_dot", "xf_nota"]`             | 182.510 μs (5%) |         |  72.22 KiB (1%) |        3746 |
| `["overhead", "foldl"]`                  |   4.150 ns (5%) |         |                 |             |
| `["overhead", "reduce_basecase"]`        | 238.885 ns (5%) |         |  464 bytes (1%) |           9 |
| `["partition_by", "man"]`                |   1.842 ms (5%) |         |  352 bytes (1%) |           4 |
| `["partition_by", "xf"]`                 |   2.843 ms (5%) |         |   6.10 MiB (1%) |      200007 |
| `["set", "base"]`                        |   4.170 ms (5%) |         |  49.58 KiB (1%) |          18 |
| `["set", "xf"]`                          |   3.969 ms (5%) |         |  49.63 KiB (1%) |          21 |

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
       #1  2800 MHz      68043 s          0 s       1446 s      29047 s          0 s
       #2  2800 MHz      28672 s          0 s       1202 s      68741 s          0 s
       
  Memory: 7.790031433105469 GB (5664.46484375 MB free)
  Uptime: 996.0 sec
  Load Avg:  1.0  0.9970703125  0.72607421875
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
    CPU MHz:               2800.200
    BogoMIPS:              5600.40
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

