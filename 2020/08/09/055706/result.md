# Benchmark result (via Travis)


# Judge result
# Benchmark Report for */home/travis/build/JuliaFolds/Transducers.jl*

## Job Properties
* Time of benchmarks:
    - Target: 9 Aug 2020 - 05:51
    - Baseline: 9 Aug 2020 - 05:56
* Package commits:
    - Target: 3a4a36
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

| ID                                                                                               | time ratio                   | memory ratio                 |
|--------------------------------------------------------------------------------------------------|------------------------------|------------------------------|
| `["cat", "base"]`                                                                                |                1.16 (5%) :x: |                   1.00 (1%)  |
| `["cat", "xf"]`                                                                                  | 0.86 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["collect", "identity-union"]`                                                                  | 0.52 (5%) :white_check_mark: | 0.85 (1%) :white_check_mark: |
| `["filter_sum", ":n => 1000", ":xs => :RandomFloats", ":withinit => false", ":impl => :naive"]`  | 0.95 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["filter_sum", ":n => 1000", ":xs => :RandomFloats", ":withinit => false", ":impl => :xf"]`     |                1.29 (5%) :x: |                   1.00 (1%)  |
| `["filter_sum", ":n => 1000", ":xs => :RandomFloats", ":withinit => true", ":impl => :naive"]`   | 0.92 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["filter_sum", ":n => 1000", ":xs => :UnitRange", ":withinit => false", ":impl => :naive"]`     | 0.70 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["filter_sum", ":n => 1000", ":xs => :UnitRange", ":withinit => false", ":impl => :xf"]`        | 0.08 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["filter_sum", ":n => 1000", ":xs => :UnitRange", ":withinit => true", ":impl => :base"]`       | 0.83 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["filter_sum", ":n => 1000", ":xs => :UnitRange", ":withinit => true", ":impl => :xf"]`         | 0.83 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["filter_sum", ":n => 10000", ":xs => :RandomFloats", ":withinit => false", ":impl => :naive"]` |                1.21 (5%) :x: |                   1.00 (1%)  |
| `["filter_sum", ":n => 10000", ":xs => :RandomFloats", ":withinit => false", ":impl => :xf"]`    | 0.40 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["filter_sum", ":n => 10000", ":xs => :UnitRange", ":withinit => false", ":impl => :naive"]`    | 0.71 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["filter_sum", ":n => 10000", ":xs => :UnitRange", ":withinit => false", ":impl => :xf"]`       | 0.07 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["gemm", "fusedmul", "blas", "16"]`                                                             | 0.75 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["gemm", "fusedmul", "blas", "2"]`                                                              | 0.67 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["gemm", "fusedmul", "blas", "32"]`                                                             | 0.84 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["gemm", "fusedmul", "blas", "8"]`                                                              | 0.73 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["gemm", "fusedmul", "xf", "16"]`                                                               | 0.93 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["gemm", "fusedmul", "xf", "32"]`                                                               | 0.95 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["gemm", "fusedmul", "xf", "8"]`                                                                | 0.95 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["gemm", "mul", "linalg", "8"]`                                                                 | 0.85 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["gemm", "mul", "man", "false", "256"]`                                                         |                1.08 (5%) :x: |                   1.00 (1%)  |
| `["gemm", "mul", "man", "false", "32"]`                                                          |                1.21 (5%) :x: |                   1.00 (1%)  |
| `["gemm", "mul", "man", "false", "8"]`                                                           | 0.93 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["gemm", "mul", "man", "ivdep", "256"]`                                                         |                1.06 (5%) :x: |                   1.00 (1%)  |
| `["gemm", "mul", "man", "ivdep", "32"]`                                                          |                1.11 (5%) :x: |                   1.00 (1%)  |
| `["gemm", "mul", "man", "true", "256"]`                                                          |                1.08 (5%) :x: |                   1.00 (1%)  |
| `["gemm", "mul", "man", "true", "32"]`                                                           |                1.18 (5%) :x: |                   1.00 (1%)  |
| `["gemm", "mul", "xf", "false", "256"]`                                                          |                1.08 (5%) :x: |                   1.00 (1%)  |
| `["gemm", "mul", "xf", "false", "32"]`                                                           |                1.20 (5%) :x: |                   1.00 (1%)  |
| `["gemm", "mul", "xf", "false", "8"]`                                                            |                1.14 (5%) :x: |                   1.00 (1%)  |
| `["gemm", "mul", "xf", "ivdep", "8"]`                                                            |                1.23 (5%) :x: |                   1.00 (1%)  |
| `["gemm", "mul", "xf", "true", "256"]`                                                           |                1.08 (5%) :x: |                   1.00 (1%)  |
| `["mapcat_eduction", "xf-xf"]`                                                                   |                1.16 (5%) :x: |                   1.00 (1%)  |
| `["missing_argmax", "rf"]`                                                                       | 0.58 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["missing_argmax", "xf"]`                                                                       | 0.48 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["missing_dot", "equiv"]`                                                                       | 0.94 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["missing_dot", "rf_nota"]`                                                                     | 0.93 (5%) :white_check_mark: |                   1.00 (1%)  |

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
       #1  2800 MHz      34722 s          0 s       1164 s      39786 s          0 s
       #2  2800 MHz      39394 s          0 s       1320 s      35479 s          0 s
       
  Memory: 7.790031433105469 GB (5791.41015625 MB free)
  Uptime: 768.0 sec
  Load Avg:  1.107421875  0.98876953125  0.62744140625
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
       #1  2800 MHz      49042 s          0 s       1277 s      54597 s          0 s
       #2  2800 MHz      54272 s          0 s       1440 s      49725 s          0 s
       
  Memory: 7.790031433105469 GB (5662.71484375 MB free)
  Uptime: 1061.0 sec
  Load Avg:  1.0  1.0  0.74072265625
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-8.0.1 (ORCJIT, skylake)
```

---
# Target result
# Benchmark Report for */home/travis/build/JuliaFolds/Transducers.jl*

## Job Properties
* Time of benchmark: 9 Aug 2020 - 5:51
* Package commit: 3a4a36
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
| `["append!!", "eduction"]`                                                                       |  18.140 μs (5%) |         |  64.72 KiB (1%) |          18 |
| `["append!!", "xf"]`                                                                             |  17.967 μs (5%) |         |  64.72 KiB (1%) |          18 |
| `["cat", "base"]`                                                                                |   1.778 μs (5%) |         |                 |             |
| `["cat", "xf"]`                                                                                  |   1.783 μs (5%) |         |                 |             |
| `["collect", "filter-missing"]`                                                                  | 102.357 μs (5%) |         | 345.31 KiB (1%) |       10015 |
| `["collect", "identity-float"]`                                                                  |  86.021 μs (5%) |         | 569.16 KiB (1%) |       10015 |
| `["collect", "identity-union"]`                                                                  | 150.604 μs (5%) |         | 601.16 KiB (1%) |       10015 |
| `["dict", "base"]`                                                                               |   3.609 ms (5%) |         |  92.91 KiB (1%) |          22 |
| `["dict", "xf"]`                                                                                 |   3.752 ms (5%) |         |  92.36 KiB (1%) |          21 |
| `["dot", "blas"]`                                                                                |   1.229 μs (5%) |         |                 |             |
| `["dot", "man"]`                                                                                 |   1.188 μs (5%) |         |                 |             |
| `["dot", "rf"]`                                                                                  |   2.140 μs (5%) |         |                 |             |
| `["dot", "xf"]`                                                                                  |   2.276 μs (5%) |         |   64 bytes (1%) |           3 |
| `["filter_map_map!", "man"]`                                                                     |  72.493 μs (5%) |         |                 |             |
| `["filter_map_map!", "xf"]`                                                                      | 623.447 μs (5%) |         |  304 bytes (1%) |          17 |
| `["filter_map_reduce", "man"]`                                                                   | 203.903 μs (5%) |         |                 |             |
| `["filter_map_reduce", "xf"]`                                                                    | 203.756 μs (5%) |         |                 |             |
| `["filter_sum", ":n => 1000", ":xs => :RandomFloats", ":withinit => false", ":impl => :base"]`   |   1.240 μs (5%) |         |                 |             |
| `["filter_sum", ":n => 1000", ":xs => :RandomFloats", ":withinit => false", ":impl => :naive"]`  |   1.175 μs (5%) |         |                 |             |
| `["filter_sum", ":n => 1000", ":xs => :RandomFloats", ":withinit => false", ":impl => :xf"]`     |   1.562 μs (5%) |         |                 |             |
| `["filter_sum", ":n => 1000", ":xs => :RandomFloats", ":withinit => true", ":impl => :base"]`    |   1.562 μs (5%) |         |                 |             |
| `["filter_sum", ":n => 1000", ":xs => :RandomFloats", ":withinit => true", ":impl => :naive"]`   | 692.649 ns (5%) |         |                 |             |
| `["filter_sum", ":n => 1000", ":xs => :RandomFloats", ":withinit => true", ":impl => :xf"]`      |   1.562 μs (5%) |         |                 |             |
| `["filter_sum", ":n => 1000", ":xs => :UnitRange", ":withinit => false", ":impl => :base"]`      |   1.633 μs (5%) |         |                 |             |
| `["filter_sum", ":n => 1000", ":xs => :UnitRange", ":withinit => false", ":impl => :naive"]`     | 741.024 ns (5%) |         |                 |             |
| `["filter_sum", ":n => 1000", ":xs => :UnitRange", ":withinit => false", ":impl => :xf"]`        | 118.348 ns (5%) |         |                 |             |
| `["filter_sum", ":n => 1000", ":xs => :UnitRange", ":withinit => true", ":impl => :base"]`       | 119.261 ns (5%) |         |                 |             |
| `["filter_sum", ":n => 1000", ":xs => :UnitRange", ":withinit => true", ":impl => :naive"]`      | 590.439 ns (5%) |         |                 |             |
| `["filter_sum", ":n => 1000", ":xs => :UnitRange", ":withinit => true", ":impl => :xf"]`         | 122.298 ns (5%) |         |                 |             |
| `["filter_sum", ":n => 10000", ":xs => :RandomFloats", ":withinit => false", ":impl => :base"]`  |  40.241 μs (5%) |         |                 |             |
| `["filter_sum", ":n => 10000", ":xs => :RandomFloats", ":withinit => false", ":impl => :naive"]` |  56.078 μs (5%) |         |                 |             |
| `["filter_sum", ":n => 10000", ":xs => :RandomFloats", ":withinit => false", ":impl => :xf"]`    |  15.865 μs (5%) |         |                 |             |
| `["filter_sum", ":n => 10000", ":xs => :RandomFloats", ":withinit => true", ":impl => :base"]`   |  15.789 μs (5%) |         |                 |             |
| `["filter_sum", ":n => 10000", ":xs => :RandomFloats", ":withinit => true", ":impl => :naive"]`  |  38.881 μs (5%) |         |                 |             |
| `["filter_sum", ":n => 10000", ":xs => :RandomFloats", ":withinit => true", ":impl => :xf"]`     |  15.832 μs (5%) |         |                 |             |
| `["filter_sum", ":n => 10000", ":xs => :UnitRange", ":withinit => false", ":impl => :base"]`     |  16.229 μs (5%) |         |                 |             |
| `["filter_sum", ":n => 10000", ":xs => :UnitRange", ":withinit => false", ":impl => :naive"]`    |   7.369 μs (5%) |         |                 |             |
| `["filter_sum", ":n => 10000", ":xs => :UnitRange", ":withinit => false", ":impl => :xf"]`       |   1.099 μs (5%) |         |                 |             |
| `["filter_sum", ":n => 10000", ":xs => :UnitRange", ":withinit => true", ":impl => :base"]`      |   1.038 μs (5%) |         |                 |             |
| `["filter_sum", ":n => 10000", ":xs => :UnitRange", ":withinit => true", ":impl => :naive"]`     |   5.892 μs (5%) |         |                 |             |
| `["filter_sum", ":n => 10000", ":xs => :UnitRange", ":withinit => true", ":impl => :xf"]`        |   1.109 μs (5%) |         |                 |             |
| `["findall", "base"]`                                                                            | 812.310 μs (5%) |         |   2.00 MiB (1%) |          21 |
| `["findall", "xf-array"]`                                                                        | 759.806 μs (5%) |         |   3.02 MiB (1%) |       98970 |
| `["findall", "xf-iter"]`                                                                         | 887.779 μs (5%) |         |   5.05 MiB (1%) |       99913 |
| `["gemm", "fusedmul", "blas", "16"]`                                                             |   5.063 ms (5%) |         |                 |             |
| `["gemm", "fusedmul", "blas", "2"]`                                                              |   3.540 ms (5%) |         |                 |             |
| `["gemm", "fusedmul", "blas", "32"]`                                                             |   7.305 ms (5%) |         |                 |             |
| `["gemm", "fusedmul", "blas", "8"]`                                                              |   4.080 ms (5%) |         |                 |             |
| `["gemm", "fusedmul", "xf", "16"]`                                                               |   4.352 ms (5%) |         |  160 bytes (1%) |           6 |
| `["gemm", "fusedmul", "xf", "2"]`                                                                | 539.044 μs (5%) |         |  160 bytes (1%) |           6 |
| `["gemm", "fusedmul", "xf", "32"]`                                                               |   8.705 ms (5%) |         |  160 bytes (1%) |           6 |
| `["gemm", "fusedmul", "xf", "8"]`                                                                |   2.288 ms (5%) |         |  160 bytes (1%) |           6 |
| `["gemm", "mul", "linalg", "256"]`                                                               | 946.137 μs (5%) |         |                 |             |
| `["gemm", "mul", "linalg", "32"]`                                                                |   3.107 μs (5%) |         |                 |             |
| `["gemm", "mul", "linalg", "8"]`                                                                 | 248.862 ns (5%) |         |                 |             |
| `["gemm", "mul", "man", "false", "256"]`                                                         |   2.052 ms (5%) |         |                 |             |
| `["gemm", "mul", "man", "false", "32"]`                                                          |   5.535 μs (5%) |         |                 |             |
| `["gemm", "mul", "man", "false", "8"]`                                                           | 395.930 ns (5%) |         |                 |             |
| `["gemm", "mul", "man", "ivdep", "256"]`                                                         |   2.020 ms (5%) |         |                 |             |
| `["gemm", "mul", "man", "ivdep", "32"]`                                                          |   4.801 μs (5%) |         |                 |             |
| `["gemm", "mul", "man", "ivdep", "8"]`                                                           | 465.837 ns (5%) |         |                 |             |
| `["gemm", "mul", "man", "true", "256"]`                                                          |   2.045 ms (5%) |         |                 |             |
| `["gemm", "mul", "man", "true", "32"]`                                                           |   5.599 μs (5%) |         |                 |             |
| `["gemm", "mul", "man", "true", "8"]`                                                            | 412.195 ns (5%) |         |                 |             |
| `["gemm", "mul", "xf", "false", "256"]`                                                          |   2.059 ms (5%) |         |   48 bytes (1%) |           2 |
| `["gemm", "mul", "xf", "false", "32"]`                                                           |   5.557 μs (5%) |         |   48 bytes (1%) |           2 |
| `["gemm", "mul", "xf", "false", "8"]`                                                            | 438.244 ns (5%) |         |   48 bytes (1%) |           2 |
| `["gemm", "mul", "xf", "ivdep", "256"]`                                                          |   2.010 ms (5%) |         |   48 bytes (1%) |           2 |
| `["gemm", "mul", "xf", "ivdep", "32"]`                                                           |   4.744 μs (5%) |         |   48 bytes (1%) |           2 |
| `["gemm", "mul", "xf", "ivdep", "8"]`                                                            | 454.426 ns (5%) |         |   48 bytes (1%) |           2 |
| `["gemm", "mul", "xf", "true", "256"]`                                                           |   2.069 ms (5%) |         |   48 bytes (1%) |           2 |
| `["gemm", "mul", "xf", "true", "32"]`                                                            |   5.481 μs (5%) |         |   48 bytes (1%) |           2 |
| `["gemm", "mul", "xf", "true", "8"]`                                                             | 391.308 ns (5%) |         |   48 bytes (1%) |           2 |
| `["groupby", "sum", "sac"]`                                                                      | 230.649 μs (5%) |         | 313.14 KiB (1%) |       10007 |
| `["groupby", "sum", "xf-with-init"]`                                                             | 168.819 μs (5%) |         | 157.44 KiB (1%) |       10008 |
| `["groupby", "sum", "xf-without-init"]`                                                          | 170.631 μs (5%) |         | 157.44 KiB (1%) |       10008 |
| `["mapcat_eduction", "base"]`                                                                    |   1.928 μs (5%) |         |                 |             |
| `["mapcat_eduction", "xf-eduction"]`                                                             |   1.782 μs (5%) |         |                 |             |
| `["mapcat_eduction", "xf-xf"]`                                                                   |   2.074 μs (5%) |         |                 |             |
| `["missing_argmax", "man"]`                                                                      |   2.369 μs (5%) |         |   32 bytes (1%) |           1 |
| `["missing_argmax", "rf"]`                                                                       |   1.340 μs (5%) |         |   32 bytes (1%) |           1 |
| `["missing_argmax", "xf"]`                                                                       |   1.358 μs (5%) |         |   32 bytes (1%) |           1 |
| `["missing_dot", "equiv"]`                                                                       |   1.465 μs (5%) |         |   16 bytes (1%) |           1 |
| `["missing_dot", "man"]`                                                                         |   1.302 μs (5%) |         |   16 bytes (1%) |           1 |
| `["missing_dot", "naive"]`                                                                       |   4.392 μs (5%) |         |   16 bytes (1%) |           1 |
| `["missing_dot", "rf"]`                                                                          |   1.257 μs (5%) |         |   16 bytes (1%) |           1 |
| `["missing_dot", "rf_nota"]`                                                                     |   1.504 μs (5%) |         |   16 bytes (1%) |           1 |
| `["missing_dot", "xf"]`                                                                          | 190.065 μs (5%) |         |  72.06 KiB (1%) |        3740 |
| `["missing_dot", "xf_nota"]`                                                                     | 188.340 μs (5%) |         |  71.75 KiB (1%) |        3724 |
| `["overhead", "foldl"]`                                                                          |   4.146 ns (5%) |         |                 |             |
| `["overhead", "reduce_basecase"]`                                                                | 237.657 ns (5%) |         |  464 bytes (1%) |           9 |
| `["partition_by", "man"]`                                                                        |   1.789 ms (5%) |         |  352 bytes (1%) |           4 |
| `["partition_by", "xf"]`                                                                         |   2.824 ms (5%) |         |   6.10 MiB (1%) |      200007 |
| `["set", "base"]`                                                                                |   4.205 ms (5%) |         |  49.58 KiB (1%) |          18 |
| `["set", "xf"]`                                                                                  |   4.005 ms (5%) |         |  49.63 KiB (1%) |          21 |

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
       #1  2800 MHz      34722 s          0 s       1164 s      39786 s          0 s
       #2  2800 MHz      39394 s          0 s       1320 s      35479 s          0 s
       
  Memory: 7.790031433105469 GB (5791.41015625 MB free)
  Uptime: 768.0 sec
  Load Avg:  1.107421875  0.98876953125  0.62744140625
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-8.0.1 (ORCJIT, skylake)
```

---
# Baseline result
# Benchmark Report for */home/travis/build/JuliaFolds/Transducers.jl*

## Job Properties
* Time of benchmark: 9 Aug 2020 - 5:56
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
| `["append!!", "eduction"]`                                                                       |  18.304 μs (5%) |         |  64.72 KiB (1%) |          18 |
| `["append!!", "xf"]`                                                                             |  18.249 μs (5%) |         |  64.72 KiB (1%) |          18 |
| `["cat", "base"]`                                                                                |   1.528 μs (5%) |         |                 |             |
| `["cat", "xf"]`                                                                                  |   2.073 μs (5%) |         |                 |             |
| `["collect", "filter-missing"]`                                                                  | 102.970 μs (5%) |         | 345.31 KiB (1%) |       10015 |
| `["collect", "identity-float"]`                                                                  |  87.737 μs (5%) |         | 569.16 KiB (1%) |       10015 |
| `["collect", "identity-union"]`                                                                  | 291.094 μs (5%) |         | 704.95 KiB (1%) |       16654 |
| `["dict", "base"]`                                                                               |   3.610 ms (5%) |         |  92.91 KiB (1%) |          22 |
| `["dict", "xf"]`                                                                                 |   3.724 ms (5%) |         |  92.36 KiB (1%) |          21 |
| `["dot", "blas"]`                                                                                |   1.219 μs (5%) |         |                 |             |
| `["dot", "man"]`                                                                                 |   1.206 μs (5%) |         |                 |             |
| `["dot", "rf"]`                                                                                  |   2.183 μs (5%) |         |                 |             |
| `["dot", "xf"]`                                                                                  |   2.268 μs (5%) |         |   64 bytes (1%) |           3 |
| `["filter_map_map!", "man"]`                                                                     |  73.112 μs (5%) |         |                 |             |
| `["filter_map_map!", "xf"]`                                                                      | 629.220 μs (5%) |         |  304 bytes (1%) |          17 |
| `["filter_map_reduce", "man"]`                                                                   | 202.676 μs (5%) |         |                 |             |
| `["filter_map_reduce", "xf"]`                                                                    | 203.734 μs (5%) |         |                 |             |
| `["filter_sum", ":n => 1000", ":xs => :RandomFloats", ":withinit => false", ":impl => :base"]`   |   1.219 μs (5%) |         |                 |             |
| `["filter_sum", ":n => 1000", ":xs => :RandomFloats", ":withinit => false", ":impl => :naive"]`  |   1.237 μs (5%) |         |                 |             |
| `["filter_sum", ":n => 1000", ":xs => :RandomFloats", ":withinit => false", ":impl => :xf"]`     |   1.214 μs (5%) |         |                 |             |
| `["filter_sum", ":n => 1000", ":xs => :RandomFloats", ":withinit => true", ":impl => :base"]`    |   1.592 μs (5%) |         |                 |             |
| `["filter_sum", ":n => 1000", ":xs => :RandomFloats", ":withinit => true", ":impl => :naive"]`   | 749.000 ns (5%) |         |                 |             |
| `["filter_sum", ":n => 1000", ":xs => :RandomFloats", ":withinit => true", ":impl => :xf"]`      |   1.602 μs (5%) |         |                 |             |
| `["filter_sum", ":n => 1000", ":xs => :UnitRange", ":withinit => false", ":impl => :base"]`      |   1.657 μs (5%) |         |                 |             |
| `["filter_sum", ":n => 1000", ":xs => :UnitRange", ":withinit => false", ":impl => :naive"]`     |   1.065 μs (5%) |         |                 |             |
| `["filter_sum", ":n => 1000", ":xs => :UnitRange", ":withinit => false", ":impl => :xf"]`        |   1.508 μs (5%) |         |                 |             |
| `["filter_sum", ":n => 1000", ":xs => :UnitRange", ":withinit => true", ":impl => :base"]`       | 143.000 ns (5%) |         |                 |             |
| `["filter_sum", ":n => 1000", ":xs => :UnitRange", ":withinit => true", ":impl => :naive"]`      | 618.000 ns (5%) |         |                 |             |
| `["filter_sum", ":n => 1000", ":xs => :UnitRange", ":withinit => true", ":impl => :xf"]`         | 148.000 ns (5%) |         |                 |             |
| `["filter_sum", ":n => 10000", ":xs => :RandomFloats", ":withinit => false", ":impl => :base"]`  |  39.426 μs (5%) |         |                 |             |
| `["filter_sum", ":n => 10000", ":xs => :RandomFloats", ":withinit => false", ":impl => :naive"]` |  46.296 μs (5%) |         |                 |             |
| `["filter_sum", ":n => 10000", ":xs => :RandomFloats", ":withinit => false", ":impl => :xf"]`    |  39.511 μs (5%) |         |                 |             |
| `["filter_sum", ":n => 10000", ":xs => :RandomFloats", ":withinit => true", ":impl => :base"]`   |  15.848 μs (5%) |         |                 |             |
| `["filter_sum", ":n => 10000", ":xs => :RandomFloats", ":withinit => true", ":impl => :naive"]`  |  37.343 μs (5%) |         |                 |             |
| `["filter_sum", ":n => 10000", ":xs => :RandomFloats", ":withinit => true", ":impl => :xf"]`     |  15.771 μs (5%) |         |                 |             |
| `["filter_sum", ":n => 10000", ":xs => :UnitRange", ":withinit => false", ":impl => :base"]`     |  16.228 μs (5%) |         |                 |             |
| `["filter_sum", ":n => 10000", ":xs => :UnitRange", ":withinit => false", ":impl => :naive"]`    |  10.336 μs (5%) |         |                 |             |
| `["filter_sum", ":n => 10000", ":xs => :UnitRange", ":withinit => false", ":impl => :xf"]`       |  14.742 μs (5%) |         |                 |             |
| `["filter_sum", ":n => 10000", ":xs => :UnitRange", ":withinit => true", ":impl => :base"]`      |   1.054 μs (5%) |         |                 |             |
| `["filter_sum", ":n => 10000", ":xs => :UnitRange", ":withinit => true", ":impl => :naive"]`     |   5.912 μs (5%) |         |                 |             |
| `["filter_sum", ":n => 10000", ":xs => :UnitRange", ":withinit => true", ":impl => :xf"]`        |   1.123 μs (5%) |         |                 |             |
| `["findall", "base"]`                                                                            | 805.627 μs (5%) |         |   2.00 MiB (1%) |          21 |
| `["findall", "xf-array"]`                                                                        | 745.574 μs (5%) |         |   3.02 MiB (1%) |       98970 |
| `["findall", "xf-iter"]`                                                                         | 902.498 μs (5%) |         |   5.05 MiB (1%) |       99913 |
| `["gemm", "fusedmul", "blas", "16"]`                                                             |   6.775 ms (5%) |         |                 |             |
| `["gemm", "fusedmul", "blas", "2"]`                                                              |   5.262 ms (5%) |         |                 |             |
| `["gemm", "fusedmul", "blas", "32"]`                                                             |   8.747 ms (5%) |         |                 |             |
| `["gemm", "fusedmul", "blas", "8"]`                                                              |   5.569 ms (5%) |         |                 |             |
| `["gemm", "fusedmul", "xf", "16"]`                                                               |   4.697 ms (5%) |         |  160 bytes (1%) |           6 |
| `["gemm", "fusedmul", "xf", "2"]`                                                                | 566.903 μs (5%) |         |  160 bytes (1%) |           6 |
| `["gemm", "fusedmul", "xf", "32"]`                                                               |   9.203 ms (5%) |         |  160 bytes (1%) |           6 |
| `["gemm", "fusedmul", "xf", "8"]`                                                                |   2.418 ms (5%) |         |  160 bytes (1%) |           6 |
| `["gemm", "mul", "linalg", "256"]`                                                               | 953.784 μs (5%) |         |                 |             |
| `["gemm", "mul", "linalg", "32"]`                                                                |   3.198 μs (5%) |         |                 |             |
| `["gemm", "mul", "linalg", "8"]`                                                                 | 292.000 ns (5%) |         |                 |             |
| `["gemm", "mul", "man", "false", "256"]`                                                         |   1.907 ms (5%) |         |                 |             |
| `["gemm", "mul", "man", "false", "32"]`                                                          |   4.567 μs (5%) |         |                 |             |
| `["gemm", "mul", "man", "false", "8"]`                                                           | 426.000 ns (5%) |         |                 |             |
| `["gemm", "mul", "man", "ivdep", "256"]`                                                         |   1.898 ms (5%) |         |                 |             |
| `["gemm", "mul", "man", "ivdep", "32"]`                                                          |   4.311 μs (5%) |         |                 |             |
| `["gemm", "mul", "man", "ivdep", "8"]`                                                           | 463.000 ns (5%) |         |                 |             |
| `["gemm", "mul", "man", "true", "256"]`                                                          |   1.891 ms (5%) |         |                 |             |
| `["gemm", "mul", "man", "true", "32"]`                                                           |   4.755 μs (5%) |         |                 |             |
| `["gemm", "mul", "man", "true", "8"]`                                                            | 427.000 ns (5%) |         |                 |             |
| `["gemm", "mul", "xf", "false", "256"]`                                                          |   1.898 ms (5%) |         |   48 bytes (1%) |           2 |
| `["gemm", "mul", "xf", "false", "32"]`                                                           |   4.642 μs (5%) |         |   48 bytes (1%) |           2 |
| `["gemm", "mul", "xf", "false", "8"]`                                                            | 384.000 ns (5%) |         |   48 bytes (1%) |           2 |
| `["gemm", "mul", "xf", "ivdep", "256"]`                                                          |   1.916 ms (5%) |         |   48 bytes (1%) |           2 |
| `["gemm", "mul", "xf", "ivdep", "32"]`                                                           |   4.689 μs (5%) |         |   48 bytes (1%) |           2 |
| `["gemm", "mul", "xf", "ivdep", "8"]`                                                            | 368.000 ns (5%) |         |   48 bytes (1%) |           2 |
| `["gemm", "mul", "xf", "true", "256"]`                                                           |   1.916 ms (5%) |         |   48 bytes (1%) |           2 |
| `["gemm", "mul", "xf", "true", "32"]`                                                            |   5.258 μs (5%) |         |   48 bytes (1%) |           2 |
| `["gemm", "mul", "xf", "true", "8"]`                                                             | 400.000 ns (5%) |         |   48 bytes (1%) |           2 |
| `["groupby", "sum", "sac"]`                                                                      | 231.403 μs (5%) |         | 313.14 KiB (1%) |       10007 |
| `["groupby", "sum", "xf-with-init"]`                                                             | 173.974 μs (5%) |         | 157.44 KiB (1%) |       10008 |
| `["groupby", "sum", "xf-without-init"]`                                                          | 170.430 μs (5%) |         | 157.44 KiB (1%) |       10008 |
| `["mapcat_eduction", "base"]`                                                                    |   1.925 μs (5%) |         |                 |             |
| `["mapcat_eduction", "xf-eduction"]`                                                             |   1.781 μs (5%) |         |                 |             |
| `["mapcat_eduction", "xf-xf"]`                                                                   |   1.782 μs (5%) |         |                 |             |
| `["missing_argmax", "man"]`                                                                      |   2.367 μs (5%) |         |   32 bytes (1%) |           1 |
| `["missing_argmax", "rf"]`                                                                       |   2.321 μs (5%) |         |   32 bytes (1%) |           1 |
| `["missing_argmax", "xf"]`                                                                       |   2.833 μs (5%) |         |   32 bytes (1%) |           1 |
| `["missing_dot", "equiv"]`                                                                       |   1.556 μs (5%) |         |   16 bytes (1%) |           1 |
| `["missing_dot", "man"]`                                                                         |   1.244 μs (5%) |         |   16 bytes (1%) |           1 |
| `["missing_dot", "naive"]`                                                                       |   4.316 μs (5%) |         |   16 bytes (1%) |           1 |
| `["missing_dot", "rf"]`                                                                          |   1.308 μs (5%) |         |   16 bytes (1%) |           1 |
| `["missing_dot", "rf_nota"]`                                                                     |   1.615 μs (5%) |         |   16 bytes (1%) |           1 |
| `["missing_dot", "xf"]`                                                                          | 183.142 μs (5%) |         |  72.03 KiB (1%) |        3740 |
| `["missing_dot", "xf_nota"]`                                                                     | 187.829 μs (5%) |         |  72.17 KiB (1%) |        3742 |
| `["overhead", "foldl"]`                                                                          |   4.153 ns (5%) |         |                 |             |
| `["overhead", "reduce_basecase"]`                                                                | 249.247 ns (5%) |         |  464 bytes (1%) |           9 |
| `["partition_by", "man"]`                                                                        |   1.798 ms (5%) |         |  352 bytes (1%) |           4 |
| `["partition_by", "xf"]`                                                                         |   2.762 ms (5%) |         |   6.10 MiB (1%) |      200007 |
| `["set", "base"]`                                                                                |   4.235 ms (5%) |         |  49.58 KiB (1%) |          18 |
| `["set", "xf"]`                                                                                  |   4.009 ms (5%) |         |  49.63 KiB (1%) |          21 |

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
       #1  2800 MHz      49042 s          0 s       1277 s      54597 s          0 s
       #2  2800 MHz      54272 s          0 s       1440 s      49725 s          0 s
       
  Memory: 7.790031433105469 GB (5662.71484375 MB free)
  Uptime: 1061.0 sec
  Load Avg:  1.0  1.0  0.74072265625
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
    CPU MHz:               2800.150
    BogoMIPS:              5600.30
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

