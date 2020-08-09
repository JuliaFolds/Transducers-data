# Benchmark result

* Pull request commit: [`ae820f34175bfeca418566d3fea42af65f689e69`](https://github.com/JuliaFolds/Transducers.jl/commit/ae820f34175bfeca418566d3fea42af65f689e69)
* Pull request: <https://github.com/JuliaFolds/Transducers.jl/pull/403> (Tail-call function-barrier for arrays)

# Judge result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmarks:
    - Target: 9 Aug 2020 - 05:27
    - Baseline: 9 Aug 2020 - 05:32
* Package commits:
    - Target: b65dd9
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
| `["cat", "base"]`                                                                                |                1.17 (5%) :x: |                   1.00 (1%)  |
| `["cat", "xf"]`                                                                                  | 0.86 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["collect", "identity-float"]`                                                                  |                1.18 (5%) :x: |                   1.00 (1%)  |
| `["collect", "identity-union"]`                                                                  | 0.50 (5%) :white_check_mark: | 0.85 (1%) :white_check_mark: |
| `["filter_map_map!", "man"]`                                                                     |                1.15 (5%) :x: |                   1.00 (1%)  |
| `["filter_sum", ":n => 1000", ":xs => :RandomFloats", ":withinit => false", ":impl => :xf"]`     |                1.26 (5%) :x: |                   1.00 (1%)  |
| `["filter_sum", ":n => 1000", ":xs => :RandomFloats", ":withinit => true", ":impl => :naive"]`   |                1.06 (5%) :x: |                   1.00 (1%)  |
| `["filter_sum", ":n => 1000", ":xs => :UnitRange", ":withinit => false", ":impl => :naive"]`     | 0.70 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["filter_sum", ":n => 1000", ":xs => :UnitRange", ":withinit => false", ":impl => :xf"]`        | 0.07 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["filter_sum", ":n => 1000", ":xs => :UnitRange", ":withinit => true", ":impl => :base"]`       |                1.10 (5%) :x: |                   1.00 (1%)  |
| `["filter_sum", ":n => 1000", ":xs => :UnitRange", ":withinit => true", ":impl => :xf"]`         |                1.18 (5%) :x: |                   1.00 (1%)  |
| `["filter_sum", ":n => 10000", ":xs => :RandomFloats", ":withinit => false", ":impl => :naive"]` |                1.21 (5%) :x: |                   1.00 (1%)  |
| `["filter_sum", ":n => 10000", ":xs => :RandomFloats", ":withinit => false", ":impl => :xf"]`    | 0.40 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["filter_sum", ":n => 10000", ":xs => :UnitRange", ":withinit => false", ":impl => :naive"]`    | 0.72 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["filter_sum", ":n => 10000", ":xs => :UnitRange", ":withinit => false", ":impl => :xf"]`       | 0.06 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["filter_sum", ":n => 10000", ":xs => :UnitRange", ":withinit => true", ":impl => :xf"]`        |                1.07 (5%) :x: |                   1.00 (1%)  |
| `["findall", "xf-array"]`                                                                        |                1.06 (5%) :x: |                   1.00 (1%)  |
| `["findall", "xf-iter"]`                                                                         |                1.05 (5%) :x: |                   1.00 (1%)  |
| `["gemm", "mul", "linalg", "8"]`                                                                 |                1.21 (5%) :x: |                   1.00 (1%)  |
| `["gemm", "mul", "man", "false", "256"]`                                                         |                1.06 (5%) :x: |                   1.00 (1%)  |
| `["gemm", "mul", "man", "false", "32"]`                                                          |                1.07 (5%) :x: |                   1.00 (1%)  |
| `["gemm", "mul", "man", "ivdep", "32"]`                                                          |                1.10 (5%) :x: |                   1.00 (1%)  |
| `["gemm", "mul", "man", "ivdep", "8"]`                                                           |                1.13 (5%) :x: |                   1.00 (1%)  |
| `["gemm", "mul", "man", "true", "256"]`                                                          |                1.05 (5%) :x: |                   1.00 (1%)  |
| `["gemm", "mul", "man", "true", "32"]`                                                           |                1.07 (5%) :x: |                   1.00 (1%)  |
| `["gemm", "mul", "xf", "false", "8"]`                                                            |                1.14 (5%) :x: |                   1.00 (1%)  |
| `["gemm", "mul", "xf", "ivdep", "8"]`                                                            |                1.10 (5%) :x: |                   1.00 (1%)  |
| `["mapcat_eduction", "xf-xf"]`                                                                   |                1.16 (5%) :x: |                   1.00 (1%)  |
| `["missing_argmax", "rf"]`                                                                       | 0.58 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["missing_argmax", "xf"]`                                                                       | 0.47 (5%) :white_check_mark: |                   1.00 (1%)  |

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
      Ubuntu 18.04.4 LTS
  uname: Linux 5.3.0-1034-azure #35~18.04.1-Ubuntu SMP Mon Jul 13 12:54:45 UTC 2020 x86_64 x86_64
  CPU: Intel(R) Xeon(R) Platinum 8272CL CPU @ 2.60GHz: 
              speed         user         nice          sys         idle          irq
       #1  2593 MHz       5425 s          0 s       1383 s      71310 s          0 s
       #2  2593 MHz      67302 s          0 s       1626 s      10396 s          0 s
       
  Memory: 6.7913818359375 GB (3095.0078125 MB free)
  Uptime: 805.0 sec
  Load Avg:  1.0  0.9814453125  0.66796875
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
      Ubuntu 18.04.4 LTS
  uname: Linux 5.3.0-1034-azure #35~18.04.1-Ubuntu SMP Mon Jul 13 12:54:45 UTC 2020 x86_64 x86_64
  CPU: Intel(R) Xeon(R) Platinum 8272CL CPU @ 2.60GHz: 
              speed         user         nice          sys         idle          irq
       #1  2593 MHz       6752 s          0 s       1444 s      98787 s          0 s
       #2  2593 MHz      94840 s          0 s       1766 s      11664 s          0 s
       
  Memory: 6.7913818359375 GB (2878.99609375 MB free)
  Uptime: 1094.0 sec
  Load Avg:  1.060546875  1.0146484375  0.77734375
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-8.0.1 (ORCJIT, skylake)
```

---
# Target result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmark: 9 Aug 2020 - 5:27
* Package commit: b65dd9
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
| `["append!!", "eduction"]`                                                                       |  18.400 μs (5%) |         |  64.72 KiB (1%) |          18 |
| `["append!!", "xf"]`                                                                             |  18.400 μs (5%) |         |  64.72 KiB (1%) |          18 |
| `["cat", "base"]`                                                                                |   2.020 μs (5%) |         |                 |             |
| `["cat", "xf"]`                                                                                  |   2.022 μs (5%) |         |                 |             |
| `["collect", "filter-missing"]`                                                                  | 109.101 μs (5%) |         | 345.31 KiB (1%) |       10015 |
| `["collect", "identity-float"]`                                                                  |  85.701 μs (5%) |         | 569.16 KiB (1%) |       10015 |
| `["collect", "identity-union"]`                                                                  | 154.201 μs (5%) |         | 601.16 KiB (1%) |       10015 |
| `["dict", "base"]`                                                                               |   4.050 ms (5%) |         |  92.91 KiB (1%) |          22 |
| `["dict", "xf"]`                                                                                 |   4.210 ms (5%) |         |  92.36 KiB (1%) |          21 |
| `["dot", "blas"]`                                                                                |   1.210 μs (5%) |         |                 |             |
| `["dot", "man"]`                                                                                 |   1.180 μs (5%) |         |                 |             |
| `["dot", "rf"]`                                                                                  |   2.133 μs (5%) |         |                 |             |
| `["dot", "xf"]`                                                                                  |   2.211 μs (5%) |         |   64 bytes (1%) |           3 |
| `["filter_map_map!", "man"]`                                                                     |  62.600 μs (5%) |         |                 |             |
| `["filter_map_map!", "xf"]`                                                                      | 700.003 μs (5%) |         |  304 bytes (1%) |          17 |
| `["filter_map_reduce", "man"]`                                                                   | 231.201 μs (5%) |         |                 |             |
| `["filter_map_reduce", "xf"]`                                                                    | 231.202 μs (5%) |         |                 |             |
| `["filter_sum", ":n => 1000", ":xs => :RandomFloats", ":withinit => false", ":impl => :base"]`   |   1.360 μs (5%) |         |                 |             |
| `["filter_sum", ":n => 1000", ":xs => :RandomFloats", ":withinit => false", ":impl => :naive"]`  |   1.320 μs (5%) |         |                 |             |
| `["filter_sum", ":n => 1000", ":xs => :RandomFloats", ":withinit => false", ":impl => :xf"]`     |   1.770 μs (5%) |         |                 |             |
| `["filter_sum", ":n => 1000", ":xs => :RandomFloats", ":withinit => true", ":impl => :base"]`    |   1.770 μs (5%) |         |                 |             |
| `["filter_sum", ":n => 1000", ":xs => :RandomFloats", ":withinit => true", ":impl => :naive"]`   | 848.529 ns (5%) |         |                 |             |
| `["filter_sum", ":n => 1000", ":xs => :RandomFloats", ":withinit => true", ":impl => :xf"]`      |   1.770 μs (5%) |         |                 |             |
| `["filter_sum", ":n => 1000", ":xs => :UnitRange", ":withinit => false", ":impl => :base"]`      |   1.860 μs (5%) |         |                 |             |
| `["filter_sum", ":n => 1000", ":xs => :UnitRange", ":withinit => false", ":impl => :naive"]`     | 840.541 ns (5%) |         |                 |             |
| `["filter_sum", ":n => 1000", ":xs => :UnitRange", ":withinit => false", ":impl => :xf"]`        | 112.188 ns (5%) |         |                 |             |
| `["filter_sum", ":n => 1000", ":xs => :UnitRange", ":withinit => true", ":impl => :base"]`       | 110.118 ns (5%) |         |                 |             |
| `["filter_sum", ":n => 1000", ":xs => :UnitRange", ":withinit => true", ":impl => :naive"]`      | 670.253 ns (5%) |         |                 |             |
| `["filter_sum", ":n => 1000", ":xs => :UnitRange", ":withinit => true", ":impl => :xf"]`         | 118.233 ns (5%) |         |                 |             |
| `["filter_sum", ":n => 10000", ":xs => :RandomFloats", ":withinit => false", ":impl => :base"]`  |  45.700 μs (5%) |         |                 |             |
| `["filter_sum", ":n => 10000", ":xs => :RandomFloats", ":withinit => false", ":impl => :naive"]` |  63.800 μs (5%) |         |                 |             |
| `["filter_sum", ":n => 10000", ":xs => :RandomFloats", ":withinit => false", ":impl => :xf"]`    |  18.000 μs (5%) |         |                 |             |
| `["filter_sum", ":n => 10000", ":xs => :RandomFloats", ":withinit => true", ":impl => :base"]`   |  18.000 μs (5%) |         |                 |             |
| `["filter_sum", ":n => 10000", ":xs => :RandomFloats", ":withinit => true", ":impl => :naive"]`  |  44.200 μs (5%) |         |                 |             |
| `["filter_sum", ":n => 10000", ":xs => :RandomFloats", ":withinit => true", ":impl => :xf"]`     |  18.100 μs (5%) |         |                 |             |
| `["filter_sum", ":n => 10000", ":xs => :UnitRange", ":withinit => false", ":impl => :base"]`     |  18.400 μs (5%) |         |                 |             |
| `["filter_sum", ":n => 10000", ":xs => :UnitRange", ":withinit => false", ":impl => :naive"]`    |   8.367 μs (5%) |         |                 |             |
| `["filter_sum", ":n => 10000", ":xs => :UnitRange", ":withinit => false", ":impl => :xf"]`       |   1.060 μs (5%) |         |                 |             |
| `["filter_sum", ":n => 10000", ":xs => :UnitRange", ":withinit => true", ":impl => :base"]`      |   1.000 μs (5%) |         |                 |             |
| `["filter_sum", ":n => 10000", ":xs => :UnitRange", ":withinit => true", ":impl => :naive"]`     |   6.680 μs (5%) |         |                 |             |
| `["filter_sum", ":n => 10000", ":xs => :UnitRange", ":withinit => true", ":impl => :xf"]`        |   1.070 μs (5%) |         |                 |             |
| `["findall", "base"]`                                                                            | 831.605 μs (5%) |         |   2.00 MiB (1%) |          21 |
| `["findall", "xf-array"]`                                                                        | 820.604 μs (5%) |         |   3.02 MiB (1%) |       98970 |
| `["findall", "xf-iter"]`                                                                         | 896.905 μs (5%) |         |   5.05 MiB (1%) |       99913 |
| `["gemm", "fusedmul", "blas", "16"]`                                                             |   4.223 ms (5%) |         |                 |             |
| `["gemm", "fusedmul", "blas", "2"]`                                                              |   3.164 ms (5%) |         |                 |             |
| `["gemm", "fusedmul", "blas", "32"]`                                                             |   5.790 ms (5%) |         |                 |             |
| `["gemm", "fusedmul", "blas", "8"]`                                                              |   3.343 ms (5%) |         |                 |             |
| `["gemm", "fusedmul", "xf", "16"]`                                                               |   5.169 ms (5%) |         |  160 bytes (1%) |           6 |
| `["gemm", "fusedmul", "xf", "2"]`                                                                | 642.403 μs (5%) |         |  160 bytes (1%) |           6 |
| `["gemm", "fusedmul", "xf", "32"]`                                                               |  10.392 ms (5%) |         |  160 bytes (1%) |           6 |
| `["gemm", "fusedmul", "xf", "8"]`                                                                |   2.595 ms (5%) |         |  160 bytes (1%) |           6 |
| `["gemm", "mul", "linalg", "256"]`                                                               | 894.104 μs (5%) |         |                 |             |
| `["gemm", "mul", "linalg", "32"]`                                                                |   2.989 μs (5%) |         |                 |             |
| `["gemm", "mul", "linalg", "8"]`                                                                 | 242.222 ns (5%) |         |                 |             |
| `["gemm", "mul", "man", "false", "256"]`                                                         |   1.714 ms (5%) |         |                 |             |
| `["gemm", "mul", "man", "false", "32"]`                                                          |   4.586 μs (5%) |         |                 |             |
| `["gemm", "mul", "man", "false", "8"]`                                                           | 382.848 ns (5%) |         |                 |             |
| `["gemm", "mul", "man", "ivdep", "256"]`                                                         |   1.680 ms (5%) |         |                 |             |
| `["gemm", "mul", "man", "ivdep", "32"]`                                                          |   4.171 μs (5%) |         |                 |             |
| `["gemm", "mul", "man", "ivdep", "8"]`                                                           | 451.010 ns (5%) |         |                 |             |
| `["gemm", "mul", "man", "true", "256"]`                                                          |   1.698 ms (5%) |         |                 |             |
| `["gemm", "mul", "man", "true", "32"]`                                                           |   4.829 μs (5%) |         |                 |             |
| `["gemm", "mul", "man", "true", "8"]`                                                            | 399.005 ns (5%) |         |                 |             |
| `["gemm", "mul", "xf", "false", "256"]`                                                          |   1.702 ms (5%) |         |   48 bytes (1%) |           2 |
| `["gemm", "mul", "xf", "false", "32"]`                                                           |   4.443 μs (5%) |         |   48 bytes (1%) |           2 |
| `["gemm", "mul", "xf", "false", "8"]`                                                            | 454.455 ns (5%) |         |   48 bytes (1%) |           2 |
| `["gemm", "mul", "xf", "ivdep", "256"]`                                                          |   1.671 ms (5%) |         |   48 bytes (1%) |           2 |
| `["gemm", "mul", "xf", "ivdep", "32"]`                                                           |   3.975 μs (5%) |         |   48 bytes (1%) |           2 |
| `["gemm", "mul", "xf", "ivdep", "8"]`                                                            | 440.909 ns (5%) |         |   48 bytes (1%) |           2 |
| `["gemm", "mul", "xf", "true", "256"]`                                                           |   1.697 ms (5%) |         |   48 bytes (1%) |           2 |
| `["gemm", "mul", "xf", "true", "32"]`                                                            |   5.150 μs (5%) |         |   48 bytes (1%) |           2 |
| `["gemm", "mul", "xf", "true", "8"]`                                                             | 380.392 ns (5%) |         |   48 bytes (1%) |           2 |
| `["groupby", "sum", "sac"]`                                                                      | 262.201 μs (5%) |         | 313.14 KiB (1%) |       10007 |
| `["groupby", "sum", "xf-with-init"]`                                                             | 189.600 μs (5%) |         | 157.44 KiB (1%) |       10008 |
| `["groupby", "sum", "xf-without-init"]`                                                          | 192.601 μs (5%) |         | 157.44 KiB (1%) |       10008 |
| `["mapcat_eduction", "base"]`                                                                    |   1.880 μs (5%) |         |                 |             |
| `["mapcat_eduction", "xf-eduction"]`                                                             |   2.022 μs (5%) |         |                 |             |
| `["mapcat_eduction", "xf-xf"]`                                                                   |   2.356 μs (5%) |         |                 |             |
| `["missing_argmax", "man"]`                                                                      |   2.678 μs (5%) |         |   32 bytes (1%) |           1 |
| `["missing_argmax", "rf"]`                                                                       |   1.490 μs (5%) |         |   32 bytes (1%) |           1 |
| `["missing_argmax", "xf"]`                                                                       |   1.480 μs (5%) |         |   32 bytes (1%) |           1 |
| `["missing_dot", "equiv"]`                                                                       |   1.650 μs (5%) |         |   16 bytes (1%) |           1 |
| `["missing_dot", "man"]`                                                                         |   1.430 μs (5%) |         |   16 bytes (1%) |           1 |
| `["missing_dot", "naive"]`                                                                       |   4.957 μs (5%) |         |   16 bytes (1%) |           1 |
| `["missing_dot", "rf"]`                                                                          |   1.390 μs (5%) |         |   16 bytes (1%) |           1 |
| `["missing_dot", "rf_nota"]`                                                                     |   1.670 μs (5%) |         |   16 bytes (1%) |           1 |
| `["missing_dot", "xf"]`                                                                          | 212.901 μs (5%) |         |  72.22 KiB (1%) |        3746 |
| `["missing_dot", "xf_nota"]`                                                                     | 211.501 μs (5%) |         |  72.02 KiB (1%) |        3734 |
| `["overhead", "foldl"]`                                                                          |   4.700 ns (5%) |         |                 |             |
| `["overhead", "reduce_basecase"]`                                                                | 267.988 ns (5%) |         |  464 bytes (1%) |           9 |
| `["partition_by", "man"]`                                                                        |   2.026 ms (5%) |         |  352 bytes (1%) |           4 |
| `["partition_by", "xf"]`                                                                         |   3.066 ms (5%) |         |   6.10 MiB (1%) |      200007 |
| `["set", "base"]`                                                                                |   4.845 ms (5%) |         |  49.58 KiB (1%) |          18 |
| `["set", "xf"]`                                                                                  |   4.527 ms (5%) |         |  49.63 KiB (1%) |          21 |

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
      Ubuntu 18.04.4 LTS
  uname: Linux 5.3.0-1034-azure #35~18.04.1-Ubuntu SMP Mon Jul 13 12:54:45 UTC 2020 x86_64 x86_64
  CPU: Intel(R) Xeon(R) Platinum 8272CL CPU @ 2.60GHz: 
              speed         user         nice          sys         idle          irq
       #1  2593 MHz       5425 s          0 s       1383 s      71310 s          0 s
       #2  2593 MHz      67302 s          0 s       1626 s      10396 s          0 s
       
  Memory: 6.7913818359375 GB (3095.0078125 MB free)
  Uptime: 805.0 sec
  Load Avg:  1.0  0.9814453125  0.66796875
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-8.0.1 (ORCJIT, skylake)
```

---
# Baseline result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmark: 9 Aug 2020 - 5:32
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
| `["append!!", "eduction"]`                                                                       |  18.401 μs (5%) |         |  64.72 KiB (1%) |          18 |
| `["append!!", "xf"]`                                                                             |  18.400 μs (5%) |         |  64.72 KiB (1%) |          18 |
| `["cat", "base"]`                                                                                |   1.730 μs (5%) |         |                 |             |
| `["cat", "xf"]`                                                                                  |   2.356 μs (5%) |         |                 |             |
| `["collect", "filter-missing"]`                                                                  | 107.901 μs (5%) |         | 345.31 KiB (1%) |       10015 |
| `["collect", "identity-float"]`                                                                  |  72.600 μs (5%) |         | 569.16 KiB (1%) |       10015 |
| `["collect", "identity-union"]`                                                                  | 308.501 μs (5%) |         | 705.34 KiB (1%) |       16681 |
| `["dict", "base"]`                                                                               |   4.047 ms (5%) |         |  92.91 KiB (1%) |          22 |
| `["dict", "xf"]`                                                                                 |   4.176 ms (5%) |         |  92.36 KiB (1%) |          21 |
| `["dot", "blas"]`                                                                                |   1.200 μs (5%) |         |                 |             |
| `["dot", "man"]`                                                                                 |   1.180 μs (5%) |         |                 |             |
| `["dot", "rf"]`                                                                                  |   2.144 μs (5%) |         |                 |             |
| `["dot", "xf"]`                                                                                  |   2.222 μs (5%) |         |   64 bytes (1%) |           3 |
| `["filter_map_map!", "man"]`                                                                     |  54.201 μs (5%) |         |                 |             |
| `["filter_map_map!", "xf"]`                                                                      | 701.406 μs (5%) |         |  304 bytes (1%) |          17 |
| `["filter_map_reduce", "man"]`                                                                   | 230.101 μs (5%) |         |                 |             |
| `["filter_map_reduce", "xf"]`                                                                    | 231.301 μs (5%) |         |                 |             |
| `["filter_sum", ":n => 1000", ":xs => :RandomFloats", ":withinit => false", ":impl => :base"]`   |   1.300 μs (5%) |         |                 |             |
| `["filter_sum", ":n => 1000", ":xs => :RandomFloats", ":withinit => false", ":impl => :naive"]`  |   1.300 μs (5%) |         |                 |             |
| `["filter_sum", ":n => 1000", ":xs => :RandomFloats", ":withinit => false", ":impl => :xf"]`     |   1.400 μs (5%) |         |                 |             |
| `["filter_sum", ":n => 1000", ":xs => :RandomFloats", ":withinit => true", ":impl => :base"]`    |   1.800 μs (5%) |         |                 |             |
| `["filter_sum", ":n => 1000", ":xs => :RandomFloats", ":withinit => true", ":impl => :naive"]`   | 800.000 ns (5%) |         |                 |             |
| `["filter_sum", ":n => 1000", ":xs => :RandomFloats", ":withinit => true", ":impl => :xf"]`      |   1.800 μs (5%) |         |                 |             |
| `["filter_sum", ":n => 1000", ":xs => :UnitRange", ":withinit => false", ":impl => :base"]`      |   1.800 μs (5%) |         |                 |             |
| `["filter_sum", ":n => 1000", ":xs => :UnitRange", ":withinit => false", ":impl => :naive"]`     |   1.200 μs (5%) |         |                 |             |
| `["filter_sum", ":n => 1000", ":xs => :UnitRange", ":withinit => false", ":impl => :xf"]`        |   1.700 μs (5%) |         |                 |             |
| `["filter_sum", ":n => 1000", ":xs => :UnitRange", ":withinit => true", ":impl => :base"]`       | 100.000 ns (5%) |         |                 |             |
| `["filter_sum", ":n => 1000", ":xs => :UnitRange", ":withinit => true", ":impl => :naive"]`      | 700.000 ns (5%) |         |                 |             |
| `["filter_sum", ":n => 1000", ":xs => :UnitRange", ":withinit => true", ":impl => :xf"]`         | 100.000 ns (5%) |         |                 |             |
| `["filter_sum", ":n => 10000", ":xs => :RandomFloats", ":withinit => false", ":impl => :base"]`  |  44.900 μs (5%) |         |                 |             |
| `["filter_sum", ":n => 10000", ":xs => :RandomFloats", ":withinit => false", ":impl => :naive"]` |  52.900 μs (5%) |         |                 |             |
| `["filter_sum", ":n => 10000", ":xs => :RandomFloats", ":withinit => false", ":impl => :xf"]`    |  44.700 μs (5%) |         |                 |             |
| `["filter_sum", ":n => 10000", ":xs => :RandomFloats", ":withinit => true", ":impl => :base"]`   |  18.000 μs (5%) |         |                 |             |
| `["filter_sum", ":n => 10000", ":xs => :RandomFloats", ":withinit => true", ":impl => :naive"]`  |  42.700 μs (5%) |         |                 |             |
| `["filter_sum", ":n => 10000", ":xs => :RandomFloats", ":withinit => true", ":impl => :xf"]`     |  18.000 μs (5%) |         |                 |             |
| `["filter_sum", ":n => 10000", ":xs => :UnitRange", ":withinit => false", ":impl => :base"]`     |  18.400 μs (5%) |         |                 |             |
| `["filter_sum", ":n => 10000", ":xs => :UnitRange", ":withinit => false", ":impl => :naive"]`    |  11.700 μs (5%) |         |                 |             |
| `["filter_sum", ":n => 10000", ":xs => :UnitRange", ":withinit => false", ":impl => :xf"]`       |  16.700 μs (5%) |         |                 |             |
| `["filter_sum", ":n => 10000", ":xs => :UnitRange", ":withinit => true", ":impl => :base"]`      |   1.000 μs (5%) |         |                 |             |
| `["filter_sum", ":n => 10000", ":xs => :UnitRange", ":withinit => true", ":impl => :naive"]`     |   6.700 μs (5%) |         |                 |             |
| `["filter_sum", ":n => 10000", ":xs => :UnitRange", ":withinit => true", ":impl => :xf"]`        |   1.000 μs (5%) |         |                 |             |
| `["findall", "base"]`                                                                            | 798.804 μs (5%) |         |   2.00 MiB (1%) |          21 |
| `["findall", "xf-array"]`                                                                        | 776.103 μs (5%) |         |   3.02 MiB (1%) |       98970 |
| `["findall", "xf-iter"]`                                                                         | 850.504 μs (5%) |         |   5.05 MiB (1%) |       99913 |
| `["gemm", "fusedmul", "blas", "16"]`                                                             |   4.223 ms (5%) |         |                 |             |
| `["gemm", "fusedmul", "blas", "2"]`                                                              |   3.150 ms (5%) |         |                 |             |
| `["gemm", "fusedmul", "blas", "32"]`                                                             |   5.934 ms (5%) |         |                 |             |
| `["gemm", "fusedmul", "blas", "8"]`                                                              |   3.333 ms (5%) |         |                 |             |
| `["gemm", "fusedmul", "xf", "16"]`                                                               |   5.186 ms (5%) |         |  160 bytes (1%) |           6 |
| `["gemm", "fusedmul", "xf", "2"]`                                                                | 645.005 μs (5%) |         |  160 bytes (1%) |           6 |
| `["gemm", "fusedmul", "xf", "32"]`                                                               |  10.348 ms (5%) |         |  160 bytes (1%) |           6 |
| `["gemm", "fusedmul", "xf", "8"]`                                                                |   2.589 ms (5%) |         |  160 bytes (1%) |           6 |
| `["gemm", "mul", "linalg", "256"]`                                                               | 892.803 μs (5%) |         |                 |             |
| `["gemm", "mul", "linalg", "32"]`                                                                |   3.000 μs (5%) |         |                 |             |
| `["gemm", "mul", "linalg", "8"]`                                                                 | 200.000 ns (5%) |         |                 |             |
| `["gemm", "mul", "man", "false", "256"]`                                                         |   1.621 ms (5%) |         |                 |             |
| `["gemm", "mul", "man", "false", "32"]`                                                          |   4.300 μs (5%) |         |                 |             |
| `["gemm", "mul", "man", "false", "8"]`                                                           | 400.000 ns (5%) |         |                 |             |
| `["gemm", "mul", "man", "ivdep", "256"]`                                                         |   1.606 ms (5%) |         |                 |             |
| `["gemm", "mul", "man", "ivdep", "32"]`                                                          |   3.800 μs (5%) |         |                 |             |
| `["gemm", "mul", "man", "ivdep", "8"]`                                                           | 400.000 ns (5%) |         |                 |             |
| `["gemm", "mul", "man", "true", "256"]`                                                          |   1.611 ms (5%) |         |                 |             |
| `["gemm", "mul", "man", "true", "32"]`                                                           |   4.500 μs (5%) |         |                 |             |
| `["gemm", "mul", "man", "true", "8"]`                                                            | 400.000 ns (5%) |         |                 |             |
| `["gemm", "mul", "xf", "false", "256"]`                                                          |   1.623 ms (5%) |         |   48 bytes (1%) |           2 |
| `["gemm", "mul", "xf", "false", "32"]`                                                           |   4.300 μs (5%) |         |   48 bytes (1%) |           2 |
| `["gemm", "mul", "xf", "false", "8"]`                                                            | 400.000 ns (5%) |         |   48 bytes (1%) |           2 |
| `["gemm", "mul", "xf", "ivdep", "256"]`                                                          |   1.605 ms (5%) |         |   48 bytes (1%) |           2 |
| `["gemm", "mul", "xf", "ivdep", "32"]`                                                           |   3.900 μs (5%) |         |   48 bytes (1%) |           2 |
| `["gemm", "mul", "xf", "ivdep", "8"]`                                                            | 400.000 ns (5%) |         |   48 bytes (1%) |           2 |
| `["gemm", "mul", "xf", "true", "256"]`                                                           |   1.640 ms (5%) |         |   48 bytes (1%) |           2 |
| `["gemm", "mul", "xf", "true", "32"]`                                                            |   5.000 μs (5%) |         |   48 bytes (1%) |           2 |
| `["gemm", "mul", "xf", "true", "8"]`                                                             | 400.000 ns (5%) |         |   48 bytes (1%) |           2 |
| `["groupby", "sum", "sac"]`                                                                      | 250.202 μs (5%) |         | 313.14 KiB (1%) |       10007 |
| `["groupby", "sum", "xf-with-init"]`                                                             | 196.202 μs (5%) |         | 157.44 KiB (1%) |       10008 |
| `["groupby", "sum", "xf-without-init"]`                                                          | 192.802 μs (5%) |         | 157.44 KiB (1%) |       10008 |
| `["mapcat_eduction", "base"]`                                                                    |   1.880 μs (5%) |         |                 |             |
| `["mapcat_eduction", "xf-eduction"]`                                                             |   2.022 μs (5%) |         |                 |             |
| `["mapcat_eduction", "xf-xf"]`                                                                   |   2.022 μs (5%) |         |                 |             |
| `["missing_argmax", "man"]`                                                                      |   2.678 μs (5%) |         |   32 bytes (1%) |           1 |
| `["missing_argmax", "rf"]`                                                                       |   2.560 μs (5%) |         |   32 bytes (1%) |           1 |
| `["missing_argmax", "xf"]`                                                                       |   3.180 μs (5%) |         |   32 bytes (1%) |           1 |
| `["missing_dot", "equiv"]`                                                                       |   1.640 μs (5%) |         |   16 bytes (1%) |           1 |
| `["missing_dot", "man"]`                                                                         |   1.390 μs (5%) |         |   16 bytes (1%) |           1 |
| `["missing_dot", "naive"]`                                                                       |   4.871 μs (5%) |         |   16 bytes (1%) |           1 |
| `["missing_dot", "rf"]`                                                                          |   1.450 μs (5%) |         |   16 bytes (1%) |           1 |
| `["missing_dot", "rf_nota"]`                                                                     |   1.700 μs (5%) |         |   16 bytes (1%) |           1 |
| `["missing_dot", "xf"]`                                                                          | 205.901 μs (5%) |         |  72.20 KiB (1%) |        3747 |
| `["missing_dot", "xf_nota"]`                                                                     | 209.201 μs (5%) |         |  72.25 KiB (1%) |        3748 |
| `["overhead", "foldl"]`                                                                          |   4.700 ns (5%) |         |                 |             |
| `["overhead", "reduce_basecase"]`                                                                | 265.552 ns (5%) |         |  464 bytes (1%) |           9 |
| `["partition_by", "man"]`                                                                        |   2.025 ms (5%) |         |  352 bytes (1%) |           4 |
| `["partition_by", "xf"]`                                                                         |   3.060 ms (5%) |         |   6.10 MiB (1%) |      200007 |
| `["set", "base"]`                                                                                |   4.980 ms (5%) |         |  49.58 KiB (1%) |          18 |
| `["set", "xf"]`                                                                                  |   4.506 ms (5%) |         |  49.63 KiB (1%) |          21 |

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
      Ubuntu 18.04.4 LTS
  uname: Linux 5.3.0-1034-azure #35~18.04.1-Ubuntu SMP Mon Jul 13 12:54:45 UTC 2020 x86_64 x86_64
  CPU: Intel(R) Xeon(R) Platinum 8272CL CPU @ 2.60GHz: 
              speed         user         nice          sys         idle          irq
       #1  2593 MHz       6752 s          0 s       1444 s      98787 s          0 s
       #2  2593 MHz      94840 s          0 s       1766 s      11664 s          0 s
       
  Memory: 6.7913818359375 GB (2878.99609375 MB free)
  Uptime: 1094.0 sec
  Load Avg:  1.060546875  1.0146484375  0.77734375
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
    Model:               85
    Model name:          Intel(R) Xeon(R) Platinum 8272CL CPU @ 2.60GHz
    Stepping:            7
    CPU MHz:             2593.909
    BogoMIPS:            5187.81
    Hypervisor vendor:   Microsoft
    Virtualization type: full
    L1d cache:           32K
    L1i cache:           32K
    L2 cache:            1024K
    L3 cache:            36608K
    NUMA node0 CPU(s):   0,1
    Flags:               fpu vme de pse tsc msr pae mce cx8 apic sep mtrr pge mca cmov pat pse36 clflush mmx fxsr sse sse2 ss ht syscall nx pdpe1gb rdtscp lm constant_tsc rep_good nopl xtopology cpuid pni pclmulqdq ssse3 fma cx16 pcid sse4_1 sse4_2 movbe popcnt aes xsave avx f16c rdrand hypervisor lahf_lm abm 3dnowprefetch invpcid_single pti fsgsbase bmi1 hle avx2 smep bmi2 erms invpcid rtm mpx avx512f avx512dq rdseed adx smap clflushopt avx512cd avx512bw avx512vl xsaveopt xsavec xsaves md_clear
    

| Cpu Property       | Value                                                   |
|:------------------ |:------------------------------------------------------- |
| Brand              | Intel(R) Xeon(R) Platinum 8272CL CPU @ 2.60GHz          |
| Vendor             | :Intel                                                  |
| Architecture       | :Skylake                                                |
| Model              | Family: 0x06, Model: 0x55, Stepping: 0x07, Type: 0x00   |
| Cores              | 2 physical cores, 2 logical cores (on executing CPU)    |
|                    | No Hyperthreading detected                              |
| Clock Frequencies  | Not supported by CPU                                    |
| Data Cache         | Level 1:3 : (32, 1024, 36608) kbytes                    |
|                    | 64 byte cache line size                                 |
| Address Size       | 48 bits virtual, 46 bits physical                       |
| SIMD               | 512 bit = 64 byte max. SIMD vector size                 |
| Time Stamp Counter | TSC is accessible via `rdtsc`                           |
|                    | TSC increased at every clock cycle (non-invariant TSC)  |
| Perf. Monitoring   | Performance Monitoring Counters (PMC) are not supported |
| Hypervisor         | Yes, Microsoft                                          |

