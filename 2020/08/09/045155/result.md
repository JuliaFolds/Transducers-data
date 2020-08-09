# Benchmark result (via Travis)


# Judge result
# Benchmark Report for */home/travis/build/JuliaFolds/Transducers.jl*

## Job Properties
* Time of benchmarks:
    - Target: 9 Aug 2020 - 04:46
    - Baseline: 9 Aug 2020 - 04:51
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

| ID                                       | time ratio                   | memory ratio                 |
|------------------------------------------|------------------------------|------------------------------|
| `["append!!", "xf"]`                     |                1.06 (5%) :x: |                   1.00 (1%)  |
| `["cat", "base"]`                        | 0.92 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["cat", "xf"]`                          |                1.17 (5%) :x: |                   1.00 (1%)  |
| `["filter_map_map!", "man"]`             | 0.87 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["filter_map_map!", "xf"]`              | 0.93 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["findall", "xf-array"]`                |                   0.98 (5%)  | 0.99 (1%) :white_check_mark: |
| `["gemm", "fusedmul", "xf", "2"]`        |                1.23 (5%) :x: |                   1.00 (1%)  |
| `["gemm", "fusedmul", "xf", "32"]`       | 0.90 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["gemm", "mul", "linalg", "8"]`         | 0.79 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["gemm", "mul", "man", "false", "32"]`  |                1.08 (5%) :x: |                   1.00 (1%)  |
| `["gemm", "mul", "man", "false", "8"]`   |                1.18 (5%) :x: |                   1.00 (1%)  |
| `["gemm", "mul", "man", "ivdep", "32"]`  |                1.08 (5%) :x: |                   1.00 (1%)  |
| `["gemm", "mul", "man", "ivdep", "8"]`   | 0.93 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["gemm", "mul", "man", "true", "32"]`   |                1.08 (5%) :x: |                   1.00 (1%)  |
| `["gemm", "mul", "man", "true", "8"]`    | 0.80 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["gemm", "mul", "xf", "false", "32"]`   | 0.77 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["gemm", "mul", "xf", "false", "8"]`    |                1.24 (5%) :x: |                   1.00 (1%)  |
| `["gemm", "mul", "xf", "ivdep", "8"]`    | 0.90 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["gemm", "mul", "xf", "true", "32"]`    |                1.08 (5%) :x: |                   1.00 (1%)  |
| `["gemm", "mul", "xf", "true", "8"]`     |                1.24 (5%) :x: |                   1.00 (1%)  |
| `["groupby", "sum", "sac"]`              | 0.94 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["groupby", "sum", "xf-with-init"]`     |                1.10 (5%) :x: |                   1.00 (1%)  |
| `["mapcat_eduction", "xf-eduction"]`     |                1.05 (5%) :x: |                   1.00 (1%)  |
| `["missing_argmax", "rf"]`               |                1.24 (5%) :x: |                   1.00 (1%)  |
| `["missing_dot", "rf_nota"]`             | 0.94 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["overhead", "foldl"]`                  |                1.07 (5%) :x: |                   1.00 (1%)  |

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
       #1  2800 MHz      24788 s          0 s       1117 s      49643 s          0 s
       #2  2800 MHz      49680 s          0 s       1256 s      25831 s          0 s
       
  Memory: 7.7900238037109375 GB (5668.38671875 MB free)
  Uptime: 773.0 sec
  Load Avg:  1.02978515625  1.0  0.64013671875
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
       #1  2800 MHz      49225 s          0 s       1238 s      51312 s          0 s
       #2  2800 MHz      51396 s          0 s       1334 s      50212 s          0 s
       
  Memory: 7.7900238037109375 GB (5685.078125 MB free)
  Uptime: 1035.0 sec
  Load Avg:  1.0  1.0  0.73828125
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-8.0.1 (ORCJIT, skylake)
```

---
# Target result
# Benchmark Report for */home/travis/build/JuliaFolds/Transducers.jl*

## Job Properties
* Time of benchmark: 9 Aug 2020 - 4:46
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
| `["append!!", "eduction"]`                                                                       |  18.297 μs (5%) |         |  64.72 KiB (1%) |          18 |
| `["append!!", "xf"]`                                                                             |  18.152 μs (5%) |         |  64.72 KiB (1%) |          18 |
| `["cat", "base"]`                                                                                |   1.632 μs (5%) |         |                 |             |
| `["cat", "xf"]`                                                                                  |   2.074 μs (5%) |         |                 |             |
| `["collect", "filter-missing"]`                                                                  | 101.779 μs (5%) |         | 345.31 KiB (1%) |       10015 |
| `["collect", "identity-float"]`                                                                  |  84.292 μs (5%) |         | 569.16 KiB (1%) |       10015 |
| `["collect", "identity-union"]`                                                                  | 290.212 μs (5%) |         | 705.09 KiB (1%) |       16663 |
| `["dict", "base"]`                                                                               |   3.576 ms (5%) |         |  92.91 KiB (1%) |          22 |
| `["dict", "xf"]`                                                                                 |   3.691 ms (5%) |         |  92.36 KiB (1%) |          21 |
| `["dot", "blas"]`                                                                                |   1.208 μs (5%) |         |                 |             |
| `["dot", "man"]`                                                                                 |   1.214 μs (5%) |         |                 |             |
| `["dot", "rf"]`                                                                                  |   2.206 μs (5%) |         |                 |             |
| `["dot", "xf"]`                                                                                  |   2.262 μs (5%) |         |   64 bytes (1%) |           3 |
| `["filter_map_map!", "man"]`                                                                     |  63.675 μs (5%) |         |                 |             |
| `["filter_map_map!", "xf"]`                                                                      | 623.321 μs (5%) |         |  304 bytes (1%) |          17 |
| `["filter_map_reduce", "man"]`                                                                   | 203.507 μs (5%) |         |                 |             |
| `["filter_map_reduce", "xf"]`                                                                    | 203.802 μs (5%) |         |                 |             |
| `["filter_sum", ":n => 1000", ":xs => :RandomFloats", ":withinit => false", ":impl => :base"]`   |   2.436 μs (5%) |         |                 |             |
| `["filter_sum", ":n => 1000", ":xs => :RandomFloats", ":withinit => false", ":impl => :naive"]`  |   1.181 μs (5%) |         |                 |             |
| `["filter_sum", ":n => 1000", ":xs => :RandomFloats", ":withinit => false", ":impl => :xf"]`     |   1.247 μs (5%) |         |                 |             |
| `["filter_sum", ":n => 1000", ":xs => :RandomFloats", ":withinit => true", ":impl => :base"]`    |   1.561 μs (5%) |         |                 |             |
| `["filter_sum", ":n => 1000", ":xs => :RandomFloats", ":withinit => true", ":impl => :naive"]`   | 690.919 ns (5%) |         |                 |             |
| `["filter_sum", ":n => 1000", ":xs => :RandomFloats", ":withinit => true", ":impl => :xf"]`      |   1.561 μs (5%) |         |                 |             |
| `["filter_sum", ":n => 1000", ":xs => :UnitRange", ":withinit => false", ":impl => :base"]`      |   1.637 μs (5%) |         |                 |             |
| `["filter_sum", ":n => 1000", ":xs => :UnitRange", ":withinit => false", ":impl => :naive"]`     | 740.429 ns (5%) |         |                 |             |
| `["filter_sum", ":n => 1000", ":xs => :UnitRange", ":withinit => false", ":impl => :xf"]`        |   1.490 μs (5%) |         |                 |             |
| `["filter_sum", ":n => 1000", ":xs => :UnitRange", ":withinit => true", ":impl => :base"]`       | 106.990 ns (5%) |         |                 |             |
| `["filter_sum", ":n => 1000", ":xs => :UnitRange", ":withinit => true", ":impl => :naive"]`      | 590.150 ns (5%) |         |                 |             |
| `["filter_sum", ":n => 1000", ":xs => :UnitRange", ":withinit => true", ":impl => :xf"]`         | 115.387 ns (5%) |         |                 |             |
| `["filter_sum", ":n => 10000", ":xs => :RandomFloats", ":withinit => false", ":impl => :base"]`  |  44.117 μs (5%) |         |                 |             |
| `["filter_sum", ":n => 10000", ":xs => :RandomFloats", ":withinit => false", ":impl => :naive"]` |  46.665 μs (5%) |         |                 |             |
| `["filter_sum", ":n => 10000", ":xs => :RandomFloats", ":withinit => false", ":impl => :xf"]`    |  40.247 μs (5%) |         |                 |             |
| `["filter_sum", ":n => 10000", ":xs => :RandomFloats", ":withinit => true", ":impl => :base"]`   |  15.852 μs (5%) |         |                 |             |
| `["filter_sum", ":n => 10000", ":xs => :RandomFloats", ":withinit => true", ":impl => :naive"]`  |  38.767 μs (5%) |         |                 |             |
| `["filter_sum", ":n => 10000", ":xs => :RandomFloats", ":withinit => true", ":impl => :xf"]`     |  15.860 μs (5%) |         |                 |             |
| `["filter_sum", ":n => 10000", ":xs => :UnitRange", ":withinit => false", ":impl => :base"]`     |  16.227 μs (5%) |         |                 |             |
| `["filter_sum", ":n => 10000", ":xs => :UnitRange", ":withinit => false", ":impl => :naive"]`    |   7.365 μs (5%) |         |                 |             |
| `["filter_sum", ":n => 10000", ":xs => :UnitRange", ":withinit => false", ":impl => :xf"]`       |  14.766 μs (5%) |         |                 |             |
| `["filter_sum", ":n => 10000", ":xs => :UnitRange", ":withinit => true", ":impl => :base"]`      |   1.032 μs (5%) |         |                 |             |
| `["filter_sum", ":n => 10000", ":xs => :UnitRange", ":withinit => true", ":impl => :naive"]`     |   5.889 μs (5%) |         |                 |             |
| `["filter_sum", ":n => 10000", ":xs => :UnitRange", ":withinit => true", ":impl => :xf"]`        |   1.097 μs (5%) |         |                 |             |
| `["findall", "base"]`                                                                            | 802.847 μs (5%) |         |   2.00 MiB (1%) |          21 |
| `["findall", "xf-array"]`                                                                        | 737.959 μs (5%) |         |   3.02 MiB (1%) |       98970 |
| `["findall", "xf-iter"]`                                                                         | 878.791 μs (5%) |         |   5.05 MiB (1%) |       99913 |
| `["gemm", "fusedmul", "blas", "16"]`                                                             |   4.997 ms (5%) |         |                 |             |
| `["gemm", "fusedmul", "blas", "2"]`                                                              |   3.423 ms (5%) |         |                 |             |
| `["gemm", "fusedmul", "blas", "32"]`                                                             |   6.772 ms (5%) |         |                 |             |
| `["gemm", "fusedmul", "blas", "8"]`                                                              |   3.971 ms (5%) |         |                 |             |
| `["gemm", "fusedmul", "xf", "16"]`                                                               |   4.768 ms (5%) |         |  160 bytes (1%) |           6 |
| `["gemm", "fusedmul", "xf", "2"]`                                                                | 625.779 μs (5%) |         |  160 bytes (1%) |           6 |
| `["gemm", "fusedmul", "xf", "32"]`                                                               |   9.163 ms (5%) |         |  160 bytes (1%) |           6 |
| `["gemm", "fusedmul", "xf", "8"]`                                                                |   2.341 ms (5%) |         |  160 bytes (1%) |           6 |
| `["gemm", "mul", "linalg", "256"]`                                                               | 959.391 μs (5%) |         |                 |             |
| `["gemm", "mul", "linalg", "32"]`                                                                |   3.399 μs (5%) |         |                 |             |
| `["gemm", "mul", "linalg", "8"]`                                                                 | 254.110 ns (5%) |         |                 |             |
| `["gemm", "mul", "man", "false", "256"]`                                                         |   1.966 ms (5%) |         |                 |             |
| `["gemm", "mul", "man", "false", "32"]`                                                          |   5.528 μs (5%) |         |                 |             |
| `["gemm", "mul", "man", "false", "8"]`                                                           | 511.958 ns (5%) |         |                 |             |
| `["gemm", "mul", "man", "ivdep", "256"]`                                                         |   1.936 ms (5%) |         |                 |             |
| `["gemm", "mul", "man", "ivdep", "32"]`                                                          |   4.717 μs (5%) |         |                 |             |
| `["gemm", "mul", "man", "ivdep", "8"]`                                                           | 399.518 ns (5%) |         |                 |             |
| `["gemm", "mul", "man", "true", "256"]`                                                          |   1.950 ms (5%) |         |                 |             |
| `["gemm", "mul", "man", "true", "32"]`                                                           |   5.649 μs (5%) |         |                 |             |
| `["gemm", "mul", "man", "true", "8"]`                                                            | 412.115 ns (5%) |         |                 |             |
| `["gemm", "mul", "xf", "false", "256"]`                                                          |   1.969 ms (5%) |         |   48 bytes (1%) |           2 |
| `["gemm", "mul", "xf", "false", "32"]`                                                           |   4.818 μs (5%) |         |   48 bytes (1%) |           2 |
| `["gemm", "mul", "xf", "false", "8"]`                                                            | 471.816 ns (5%) |         |   48 bytes (1%) |           2 |
| `["gemm", "mul", "xf", "ivdep", "256"]`                                                          |   1.932 ms (5%) |         |   48 bytes (1%) |           2 |
| `["gemm", "mul", "xf", "ivdep", "32"]`                                                           |   4.591 μs (5%) |         |   48 bytes (1%) |           2 |
| `["gemm", "mul", "xf", "ivdep", "8"]`                                                            | 448.995 ns (5%) |         |   48 bytes (1%) |           2 |
| `["gemm", "mul", "xf", "true", "256"]`                                                           |   1.995 ms (5%) |         |   48 bytes (1%) |           2 |
| `["gemm", "mul", "xf", "true", "32"]`                                                            |   5.519 μs (5%) |         |   48 bytes (1%) |           2 |
| `["gemm", "mul", "xf", "true", "8"]`                                                             | 499.426 ns (5%) |         |   48 bytes (1%) |           2 |
| `["groupby", "sum", "sac"]`                                                                      | 223.498 μs (5%) |         | 313.14 KiB (1%) |       10007 |
| `["groupby", "sum", "xf-with-init"]`                                                             | 176.315 μs (5%) |         | 157.44 KiB (1%) |       10008 |
| `["groupby", "sum", "xf-without-init"]`                                                          | 171.331 μs (5%) |         | 157.44 KiB (1%) |       10008 |
| `["mapcat_eduction", "base"]`                                                                    |   1.926 μs (5%) |         |                 |             |
| `["mapcat_eduction", "xf-eduction"]`                                                             |   1.781 μs (5%) |         |                 |             |
| `["mapcat_eduction", "xf-xf"]`                                                                   |   1.688 μs (5%) |         |                 |             |
| `["missing_argmax", "man"]`                                                                      |   2.366 μs (5%) |         |   32 bytes (1%) |           1 |
| `["missing_argmax", "rf"]`                                                                       |   2.845 μs (5%) |         |   32 bytes (1%) |           1 |
| `["missing_argmax", "xf"]`                                                                       |   2.296 μs (5%) |         |   32 bytes (1%) |           1 |
| `["missing_dot", "equiv"]`                                                                       |   1.586 μs (5%) |         |   16 bytes (1%) |           1 |
| `["missing_dot", "man"]`                                                                         |   1.416 μs (5%) |         |   16 bytes (1%) |           1 |
| `["missing_dot", "naive"]`                                                                       |   4.351 μs (5%) |         |   16 bytes (1%) |           1 |
| `["missing_dot", "rf"]`                                                                          |   1.231 μs (5%) |         |   16 bytes (1%) |           1 |
| `["missing_dot", "rf_nota"]`                                                                     |   1.473 μs (5%) |         |   16 bytes (1%) |           1 |
| `["missing_dot", "xf"]`                                                                          | 184.709 μs (5%) |         |  72.06 KiB (1%) |        3740 |
| `["missing_dot", "xf_nota"]`                                                                     | 185.680 μs (5%) |         |  71.97 KiB (1%) |        3736 |
| `["overhead", "foldl"]`                                                                          |   4.447 ns (5%) |         |                 |             |
| `["overhead", "reduce_basecase"]`                                                                | 235.620 ns (5%) |         |  464 bytes (1%) |           9 |
| `["partition_by", "man"]`                                                                        |   1.848 ms (5%) |         |  352 bytes (1%) |           4 |
| `["partition_by", "xf"]`                                                                         |   2.821 ms (5%) |         |   6.10 MiB (1%) |      200007 |
| `["set", "base"]`                                                                                |   4.242 ms (5%) |         |  49.58 KiB (1%) |          18 |
| `["set", "xf"]`                                                                                  |   3.964 ms (5%) |         |  49.63 KiB (1%) |          21 |

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
       #1  2800 MHz      24788 s          0 s       1117 s      49643 s          0 s
       #2  2800 MHz      49680 s          0 s       1256 s      25831 s          0 s
       
  Memory: 7.7900238037109375 GB (5668.38671875 MB free)
  Uptime: 773.0 sec
  Load Avg:  1.02978515625  1.0  0.64013671875
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-8.0.1 (ORCJIT, skylake)
```

---
# Baseline result
# Benchmark Report for */home/travis/build/JuliaFolds/Transducers.jl*

## Job Properties
* Time of benchmark: 9 Aug 2020 - 4:51
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
| `["append!!", "eduction"]`               |  18.056 μs (5%) |         |  64.72 KiB (1%) |          18 |
| `["append!!", "xf"]`                     |  17.046 μs (5%) |         |  64.72 KiB (1%) |          18 |
| `["cat", "base"]`                        |   1.778 μs (5%) |         |                 |             |
| `["cat", "xf"]`                          |   1.774 μs (5%) |         |                 |             |
| `["collect", "filter-missing"]`          | 102.594 μs (5%) |         | 345.31 KiB (1%) |       10015 |
| `["collect", "identity-float"]`          |  82.928 μs (5%) |         | 569.16 KiB (1%) |       10015 |
| `["collect", "identity-union"]`          | 289.354 μs (5%) |         | 705.28 KiB (1%) |       16675 |
| `["dict", "base"]`                       |   3.605 ms (5%) |         |  92.91 KiB (1%) |          22 |
| `["dict", "xf"]`                         |   3.725 ms (5%) |         |  92.36 KiB (1%) |          21 |
| `["dot", "blas"]`                        |   1.225 μs (5%) |         |                 |             |
| `["dot", "man"]`                         |   1.189 μs (5%) |         |                 |             |
| `["dot", "rf"]`                          |   2.206 μs (5%) |         |                 |             |
| `["dot", "xf"]`                          |   2.271 μs (5%) |         |   64 bytes (1%) |           3 |
| `["filter_map_map!", "man"]`             |  73.124 μs (5%) |         |                 |             |
| `["filter_map_map!", "xf"]`              | 666.876 μs (5%) |         |  304 bytes (1%) |          17 |
| `["filter_map_reduce", "man"]`           | 202.613 μs (5%) |         |                 |             |
| `["filter_map_reduce", "xf"]`            | 203.671 μs (5%) |         |                 |             |
| `["findall", "base"]`                    | 787.241 μs (5%) |         |   2.00 MiB (1%) |          21 |
| `["findall", "xf-array"]`                | 756.178 μs (5%) |         |   3.06 MiB (1%) |      100109 |
| `["findall", "xf-iter"]`                 | 853.881 μs (5%) |         |   5.05 MiB (1%) |       99919 |
| `["gemm", "fusedmul", "blas", "16"]`     |   4.933 ms (5%) |         |                 |             |
| `["gemm", "fusedmul", "blas", "2"]`      |   3.454 ms (5%) |         |                 |             |
| `["gemm", "fusedmul", "blas", "32"]`     |   6.898 ms (5%) |         |                 |             |
| `["gemm", "fusedmul", "blas", "8"]`      |   3.794 ms (5%) |         |                 |             |
| `["gemm", "fusedmul", "xf", "16"]`       |   4.573 ms (5%) |         |  160 bytes (1%) |           6 |
| `["gemm", "fusedmul", "xf", "2"]`        | 508.149 μs (5%) |         |  160 bytes (1%) |           6 |
| `["gemm", "fusedmul", "xf", "32"]`       |  10.199 ms (5%) |         |  160 bytes (1%) |           6 |
| `["gemm", "fusedmul", "xf", "8"]`        |   2.355 ms (5%) |         |  160 bytes (1%) |           6 |
| `["gemm", "mul", "linalg", "256"]`       | 961.806 μs (5%) |         |                 |             |
| `["gemm", "mul", "linalg", "32"]`        |   3.458 μs (5%) |         |                 |             |
| `["gemm", "mul", "linalg", "8"]`         | 320.000 ns (5%) |         |                 |             |
| `["gemm", "mul", "man", "false", "256"]` |   1.958 ms (5%) |         |                 |             |
| `["gemm", "mul", "man", "false", "32"]`  |   5.111 μs (5%) |         |                 |             |
| `["gemm", "mul", "man", "false", "8"]`   | 433.000 ns (5%) |         |                 |             |
| `["gemm", "mul", "man", "ivdep", "256"]` |   1.931 ms (5%) |         |                 |             |
| `["gemm", "mul", "man", "ivdep", "32"]`  |   4.382 μs (5%) |         |                 |             |
| `["gemm", "mul", "man", "ivdep", "8"]`   | 430.000 ns (5%) |         |                 |             |
| `["gemm", "mul", "man", "true", "256"]`  |   1.939 ms (5%) |         |                 |             |
| `["gemm", "mul", "man", "true", "32"]`   |   5.231 μs (5%) |         |                 |             |
| `["gemm", "mul", "man", "true", "8"]`    | 515.000 ns (5%) |         |                 |             |
| `["gemm", "mul", "xf", "false", "256"]`  |   1.960 ms (5%) |         |   48 bytes (1%) |           2 |
| `["gemm", "mul", "xf", "false", "32"]`   |   6.281 μs (5%) |         |   48 bytes (1%) |           2 |
| `["gemm", "mul", "xf", "false", "8"]`    | 382.000 ns (5%) |         |   48 bytes (1%) |           2 |
| `["gemm", "mul", "xf", "ivdep", "256"]`  |   1.931 ms (5%) |         |   48 bytes (1%) |           2 |
| `["gemm", "mul", "xf", "ivdep", "32"]`   |   4.469 μs (5%) |         |   48 bytes (1%) |           2 |
| `["gemm", "mul", "xf", "ivdep", "8"]`    | 501.000 ns (5%) |         |   48 bytes (1%) |           2 |
| `["gemm", "mul", "xf", "true", "256"]`   |   2.045 ms (5%) |         |   48 bytes (1%) |           2 |
| `["gemm", "mul", "xf", "true", "32"]`    |   5.099 μs (5%) |         |   48 bytes (1%) |           2 |
| `["gemm", "mul", "xf", "true", "8"]`     | 403.000 ns (5%) |         |   48 bytes (1%) |           2 |
| `["groupby", "sum", "sac"]`              | 238.777 μs (5%) |         | 313.14 KiB (1%) |       10007 |
| `["groupby", "sum", "xf-with-init"]`     | 160.292 μs (5%) |         | 157.44 KiB (1%) |       10008 |
| `["groupby", "sum", "xf-without-init"]`  | 169.643 μs (5%) |         | 157.44 KiB (1%) |       10008 |
| `["mapcat_eduction", "base"]`            |   1.926 μs (5%) |         |                 |             |
| `["mapcat_eduction", "xf-eduction"]`     |   1.688 μs (5%) |         |                 |             |
| `["mapcat_eduction", "xf-xf"]`           |   1.687 μs (5%) |         |                 |             |
| `["missing_argmax", "man"]`              |   2.366 μs (5%) |         |   32 bytes (1%) |           1 |
| `["missing_argmax", "rf"]`               |   2.302 μs (5%) |         |   32 bytes (1%) |           1 |
| `["missing_argmax", "xf"]`               |   2.289 μs (5%) |         |   32 bytes (1%) |           1 |
| `["missing_dot", "equiv"]`               |   1.533 μs (5%) |         |   16 bytes (1%) |           1 |
| `["missing_dot", "man"]`                 |   1.360 μs (5%) |         |   16 bytes (1%) |           1 |
| `["missing_dot", "naive"]`               |   4.342 μs (5%) |         |   16 bytes (1%) |           1 |
| `["missing_dot", "rf"]`                  |   1.265 μs (5%) |         |   16 bytes (1%) |           1 |
| `["missing_dot", "rf_nota"]`             |   1.562 μs (5%) |         |   16 bytes (1%) |           1 |
| `["missing_dot", "xf"]`                  | 190.612 μs (5%) |         |  72.16 KiB (1%) |        3744 |
| `["missing_dot", "xf_nota"]`             | 191.881 μs (5%) |         |  71.50 KiB (1%) |        3714 |
| `["overhead", "foldl"]`                  |   4.158 ns (5%) |         |                 |             |
| `["overhead", "reduce_basecase"]`        | 240.026 ns (5%) |         |  464 bytes (1%) |           9 |
| `["partition_by", "man"]`                |   1.795 ms (5%) |         |  352 bytes (1%) |           4 |
| `["partition_by", "xf"]`                 |   2.799 ms (5%) |         |   6.10 MiB (1%) |      200007 |
| `["set", "base"]`                        |   4.182 ms (5%) |         |  49.58 KiB (1%) |          18 |
| `["set", "xf"]`                          |   3.986 ms (5%) |         |  49.63 KiB (1%) |          21 |

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
       #1  2800 MHz      49225 s          0 s       1238 s      51312 s          0 s
       #2  2800 MHz      51396 s          0 s       1334 s      50212 s          0 s
       
  Memory: 7.7900238037109375 GB (5685.078125 MB free)
  Uptime: 1035.0 sec
  Load Avg:  1.0  1.0  0.73828125
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
    CPU MHz:               2800.158
    BogoMIPS:              5600.31
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

