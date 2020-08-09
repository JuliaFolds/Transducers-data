# Benchmark result

* Pull request commit: [`d1a13bdda9c995b333fcd2bcb8c04a95269b9e18`](https://github.com/JuliaFolds/Transducers.jl/commit/d1a13bdda9c995b333fcd2bcb8c04a95269b9e18)
* Pull request: <https://github.com/JuliaFolds/Transducers.jl/pull/405> (Add bench_sum_transpose.jl)

# Judge result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmarks:
    - Target: 9 Aug 2020 - 05:05
    - Baseline: 9 Aug 2020 - 05:09
* Package commits:
    - Target: e376b2
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
| `["append!!", "eduction"]`               |                1.14 (5%) :x: |   1.00 (1%)  |
| `["collect", "identity-float"]`          |                1.07 (5%) :x: |   1.00 (1%)  |
| `["findall", "xf-iter"]`                 |                1.05 (5%) :x: |   1.00 (1%)  |
| `["gemm", "mul", "man", "false", "8"]`   | 0.84 (5%) :white_check_mark: |   1.00 (1%)  |
| `["gemm", "mul", "man", "ivdep", "8"]`   | 0.87 (5%) :white_check_mark: |   1.00 (1%)  |
| `["gemm", "mul", "man", "true", "8"]`    | 0.85 (5%) :white_check_mark: |   1.00 (1%)  |
| `["gemm", "mul", "xf", "false", "8"]`    |                1.27 (5%) :x: |   1.00 (1%)  |
| `["gemm", "mul", "xf", "ivdep", "8"]`    | 0.85 (5%) :white_check_mark: |   1.00 (1%)  |
| `["gemm", "mul", "xf", "true", "8"]`     | 0.88 (5%) :white_check_mark: |   1.00 (1%)  |
| `["missing_dot", "man"]`                 |                1.20 (5%) :x: |   1.00 (1%)  |
| `["missing_dot", "xf_nota"]`             |                1.06 (5%) :x: |   1.00 (1%)  |

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
      Ubuntu 18.04.4 LTS
  uname: Linux 5.3.0-1034-azure #35~18.04.1-Ubuntu SMP Mon Jul 13 12:54:45 UTC 2020 x86_64 x86_64
  CPU: Intel(R) Xeon(R) CPU E5-2673 v4 @ 2.30GHz: 
              speed         user         nice          sys         idle          irq
       #1  2294 MHz      54131 s          0 s       1250 s      16360 s          0 s
       #2  2294 MHz      12064 s          0 s       1396 s      58911 s          0 s
       
  Memory: 6.764881134033203 GB (2807.00390625 MB free)
  Uptime: 738.0 sec
  Load Avg:  1.0  0.955078125  0.60791015625
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-8.0.1 (ORCJIT, broadwell)
```

### Baseline
```
Julia Version 1.4.2
Commit 44fa15b150* (2020-05-23 18:35 UTC)
Platform Info:
  OS: Linux (x86_64-pc-linux-gnu)
      Ubuntu 18.04.4 LTS
  uname: Linux 5.3.0-1034-azure #35~18.04.1-Ubuntu SMP Mon Jul 13 12:54:45 UTC 2020 x86_64 x86_64
  CPU: Intel(R) Xeon(R) CPU E5-2673 v4 @ 2.30GHz: 
              speed         user         nice          sys         idle          irq
       #1  2294 MHz      74183 s          0 s       1396 s      21889 s          0 s
       #2  2294 MHz      17649 s          0 s       1490 s      78994 s          0 s
       
  Memory: 6.764881134033203 GB (2716.8125 MB free)
  Uptime: 996.0 sec
  Load Avg:  1.08349609375  1.0166015625  0.73046875
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-8.0.1 (ORCJIT, broadwell)
```

---
# Target result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmark: 9 Aug 2020 - 5:5
* Package commit: e376b2
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
| `["append!!", "eduction"]`                                              |  16.700 μs (5%) |         |  64.72 KiB (1%) |          18 |
| `["append!!", "xf"]`                                                    |  15.400 μs (5%) |         |  64.72 KiB (1%) |          18 |
| `["cat", "base"]`                                                       |   1.480 μs (5%) |         |                 |             |
| `["cat", "xf"]`                                                         |   1.690 μs (5%) |         |                 |             |
| `["collect", "filter-missing"]`                                         |  88.200 μs (5%) |         | 345.31 KiB (1%) |       10015 |
| `["collect", "identity-float"]`                                         |  71.301 μs (5%) |         | 569.16 KiB (1%) |       10015 |
| `["collect", "identity-union"]`                                         | 266.102 μs (5%) |         | 704.84 KiB (1%) |       16651 |
| `["dict", "base"]`                                                      |   3.777 ms (5%) |         |  92.91 KiB (1%) |          22 |
| `["dict", "xf"]`                                                        |   3.783 ms (5%) |         |  92.36 KiB (1%) |          21 |
| `["dot", "blas"]`                                                       |   2.267 μs (5%) |         |                 |             |
| `["dot", "man"]`                                                        |   2.256 μs (5%) |         |                 |             |
| `["dot", "rf"]`                                                         |   3.050 μs (5%) |         |                 |             |
| `["dot", "xf"]`                                                         |   3.125 μs (5%) |         |   64 bytes (1%) |           3 |
| `["filter_map_map!", "man"]`                                            |  68.601 μs (5%) |         |                 |             |
| `["filter_map_map!", "xf"]`                                             | 537.403 μs (5%) |         |  304 bytes (1%) |          17 |
| `["filter_map_reduce", "man"]`                                          | 194.901 μs (5%) |         |                 |             |
| `["filter_map_reduce", "xf"]`                                           | 194.901 μs (5%) |         |                 |             |
| `["findall", "base"]`                                                   | 749.006 μs (5%) |         |   2.00 MiB (1%) |          21 |
| `["findall", "xf-array"]`                                               | 733.606 μs (5%) |         |   3.05 MiB (1%) |      100004 |
| `["findall", "xf-iter"]`                                                | 761.906 μs (5%) |         |   5.05 MiB (1%) |       99924 |
| `["gemm", "fusedmul", "blas", "16"]`                                    |   4.966 ms (5%) |         |                 |             |
| `["gemm", "fusedmul", "blas", "2"]`                                     |   3.529 ms (5%) |         |                 |             |
| `["gemm", "fusedmul", "blas", "32"]`                                    |   7.148 ms (5%) |         |                 |             |
| `["gemm", "fusedmul", "blas", "8"]`                                     |   3.793 ms (5%) |         |                 |             |
| `["gemm", "fusedmul", "xf", "16"]`                                      |   4.957 ms (5%) |         |  160 bytes (1%) |           6 |
| `["gemm", "fusedmul", "xf", "2"]`                                       | 617.103 μs (5%) |         |  160 bytes (1%) |           6 |
| `["gemm", "fusedmul", "xf", "32"]`                                      |   9.990 ms (5%) |         |  160 bytes (1%) |           6 |
| `["gemm", "fusedmul", "xf", "8"]`                                       |   2.579 ms (5%) |         |  160 bytes (1%) |           6 |
| `["gemm", "mul", "linalg", "256"]`                                      |   1.208 ms (5%) |         |                 |             |
| `["gemm", "mul", "linalg", "32"]`                                       |   3.737 μs (5%) |         |                 |             |
| `["gemm", "mul", "linalg", "8"]`                                        | 288.571 ns (5%) |         |                 |             |
| `["gemm", "mul", "man", "false", "256"]`                                |   4.312 ms (5%) |         |                 |             |
| `["gemm", "mul", "man", "false", "32"]`                                 |   6.700 μs (5%) |         |                 |             |
| `["gemm", "mul", "man", "false", "8"]`                                  | 337.681 ns (5%) |         |                 |             |
| `["gemm", "mul", "man", "ivdep", "256"]`                                |   4.290 ms (5%) |         |                 |             |
| `["gemm", "mul", "man", "ivdep", "32"]`                                 |   6.017 μs (5%) |         |                 |             |
| `["gemm", "mul", "man", "ivdep", "8"]`                                  | 348.058 ns (5%) |         |                 |             |
| `["gemm", "mul", "man", "true", "256"]`                                 |   4.301 ms (5%) |         |                 |             |
| `["gemm", "mul", "man", "true", "32"]`                                  |   6.500 μs (5%) |         |                 |             |
| `["gemm", "mul", "man", "true", "8"]`                                   | 338.813 ns (5%) |         |                 |             |
| `["gemm", "mul", "xf", "false", "256"]`                                 |   4.312 ms (5%) |         |   48 bytes (1%) |           2 |
| `["gemm", "mul", "xf", "false", "32"]`                                  |   6.840 μs (5%) |         |   48 bytes (1%) |           2 |
| `["gemm", "mul", "xf", "false", "8"]`                                   | 380.597 ns (5%) |         |   48 bytes (1%) |           2 |
| `["gemm", "mul", "xf", "ivdep", "256"]`                                 |   4.159 ms (5%) |         |   48 bytes (1%) |           2 |
| `["gemm", "mul", "xf", "ivdep", "32"]`                                  |   5.567 μs (5%) |         |   48 bytes (1%) |           2 |
| `["gemm", "mul", "xf", "ivdep", "8"]`                                   | 339.913 ns (5%) |         |   48 bytes (1%) |           2 |
| `["gemm", "mul", "xf", "true", "256"]`                                  |   4.310 ms (5%) |         |   48 bytes (1%) |           2 |
| `["gemm", "mul", "xf", "true", "32"]`                                   |   6.680 μs (5%) |         |   48 bytes (1%) |           2 |
| `["gemm", "mul", "xf", "true", "8"]`                                    | 351.942 ns (5%) |         |   48 bytes (1%) |           2 |
| `["groupby", "sum", "sac"]`                                             | 206.001 μs (5%) |         | 313.14 KiB (1%) |       10007 |
| `["groupby", "sum", "xf-with-init"]`                                    | 154.701 μs (5%) |         | 157.44 KiB (1%) |       10008 |
| `["groupby", "sum", "xf-without-init"]`                                 | 152.201 μs (5%) |         | 157.44 KiB (1%) |       10008 |
| `["mapcat_eduction", "base"]`                                           |   1.490 μs (5%) |         |                 |             |
| `["mapcat_eduction", "xf-eduction"]`                                    |   1.600 μs (5%) |         |                 |             |
| `["mapcat_eduction", "xf-xf"]`                                          |   1.600 μs (5%) |         |                 |             |
| `["missing_argmax", "man"]`                                             | 896.552 ns (5%) |         |   32 bytes (1%) |           1 |
| `["missing_argmax", "rf"]`                                              |   2.100 μs (5%) |         |   32 bytes (1%) |           1 |
| `["missing_argmax", "xf"]`                                              |   2.089 μs (5%) |         |   32 bytes (1%) |           1 |
| `["missing_dot", "equiv"]`                                              | 917.308 ns (5%) |         |   16 bytes (1%) |           1 |
| `["missing_dot", "man"]`                                                |   1.105 μs (5%) |         |   16 bytes (1%) |           1 |
| `["missing_dot", "naive"]`                                              |   4.043 μs (5%) |         |   16 bytes (1%) |           1 |
| `["missing_dot", "rf"]`                                                 | 891.683 ns (5%) |         |   16 bytes (1%) |           1 |
| `["missing_dot", "rf_nota"]`                                            | 917.327 ns (5%) |         |   16 bytes (1%) |           1 |
| `["missing_dot", "xf"]`                                                 | 181.601 μs (5%) |         |  72.28 KiB (1%) |        3750 |
| `["missing_dot", "xf_nota"]`                                            | 184.902 μs (5%) |         |  72.33 KiB (1%) |        3750 |
| `["overhead", "foldl"]`                                                 |   3.900 ns (5%) |         |                 |             |
| `["overhead", "reduce_basecase"]`                                       | 246.578 ns (5%) |         |  464 bytes (1%) |           9 |
| `["partition_by", "man"]`                                               |   1.641 ms (5%) |         |  352 bytes (1%) |           4 |
| `["partition_by", "xf"]`                                                |   2.472 ms (5%) |         |   6.10 MiB (1%) |      200007 |
| `["set", "base"]`                                                       |   4.510 ms (5%) |         |  49.58 KiB (1%) |          18 |
| `["set", "xf"]`                                                         |   3.894 ms (5%) |         |  49.63 KiB (1%) |          21 |
| `["sum_transpose", ":n => 30", ":withinit => false", ":impl => :iter"]` |   1.860 μs (5%) |         |                 |             |
| `["sum_transpose", ":n => 30", ":withinit => false", ":impl => :man"]`  |   1.340 μs (5%) |         |                 |             |
| `["sum_transpose", ":n => 30", ":withinit => false", ":impl => :xf"]`   |   3.011 μs (5%) |         |                 |             |
| `["sum_transpose", ":n => 30", ":withinit => true", ":impl => :iter"]`  |   1.270 μs (5%) |         |                 |             |
| `["sum_transpose", ":n => 30", ":withinit => true", ":impl => :man"]`   | 729.323 ns (5%) |         |                 |             |
| `["sum_transpose", ":n => 30", ":withinit => true", ":impl => :xf"]`    |   3.011 μs (5%) |         |                 |             |

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
      Ubuntu 18.04.4 LTS
  uname: Linux 5.3.0-1034-azure #35~18.04.1-Ubuntu SMP Mon Jul 13 12:54:45 UTC 2020 x86_64 x86_64
  CPU: Intel(R) Xeon(R) CPU E5-2673 v4 @ 2.30GHz: 
              speed         user         nice          sys         idle          irq
       #1  2294 MHz      54131 s          0 s       1250 s      16360 s          0 s
       #2  2294 MHz      12064 s          0 s       1396 s      58911 s          0 s
       
  Memory: 6.764881134033203 GB (2807.00390625 MB free)
  Uptime: 738.0 sec
  Load Avg:  1.0  0.955078125  0.60791015625
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-8.0.1 (ORCJIT, broadwell)
```

---
# Baseline result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmark: 9 Aug 2020 - 5:9
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
| `["append!!", "eduction"]`               |  14.700 μs (5%) |         |  64.72 KiB (1%) |          18 |
| `["append!!", "xf"]`                     |  14.800 μs (5%) |         |  64.72 KiB (1%) |          18 |
| `["cat", "base"]`                        |   1.500 μs (5%) |         |                 |             |
| `["cat", "xf"]`                          |   1.660 μs (5%) |         |                 |             |
| `["collect", "filter-missing"]`          |  86.300 μs (5%) |         | 345.31 KiB (1%) |       10015 |
| `["collect", "identity-float"]`          |  66.900 μs (5%) |         | 569.16 KiB (1%) |       10015 |
| `["collect", "identity-union"]`          | 261.401 μs (5%) |         | 705.13 KiB (1%) |       16660 |
| `["dict", "base"]`                       |   3.936 ms (5%) |         |  92.91 KiB (1%) |          22 |
| `["dict", "xf"]`                         |   3.780 ms (5%) |         |  92.36 KiB (1%) |          21 |
| `["dot", "blas"]`                        |   2.278 μs (5%) |         |                 |             |
| `["dot", "man"]`                         |   2.267 μs (5%) |         |                 |             |
| `["dot", "rf"]`                          |   3.050 μs (5%) |         |                 |             |
| `["dot", "xf"]`                          |   3.125 μs (5%) |         |   64 bytes (1%) |           3 |
| `["filter_map_map!", "man"]`             |  67.301 μs (5%) |         |                 |             |
| `["filter_map_map!", "xf"]`              | 532.807 μs (5%) |         |  304 bytes (1%) |          17 |
| `["filter_map_reduce", "man"]`           | 194.900 μs (5%) |         |                 |             |
| `["filter_map_reduce", "xf"]`            | 194.900 μs (5%) |         |                 |             |
| `["findall", "base"]`                    | 734.303 μs (5%) |         |   2.00 MiB (1%) |          21 |
| `["findall", "xf-array"]`                | 701.803 μs (5%) |         |   3.03 MiB (1%) |       99199 |
| `["findall", "xf-iter"]`                 | 722.903 μs (5%) |         |   5.05 MiB (1%) |       99928 |
| `["gemm", "fusedmul", "blas", "16"]`     |   5.004 ms (5%) |         |                 |             |
| `["gemm", "fusedmul", "blas", "2"]`      |   3.528 ms (5%) |         |                 |             |
| `["gemm", "fusedmul", "blas", "32"]`     |   7.184 ms (5%) |         |                 |             |
| `["gemm", "fusedmul", "blas", "8"]`      |   3.791 ms (5%) |         |                 |             |
| `["gemm", "fusedmul", "xf", "16"]`       |   5.020 ms (5%) |         |  160 bytes (1%) |           6 |
| `["gemm", "fusedmul", "xf", "2"]`        | 619.508 μs (5%) |         |  160 bytes (1%) |           6 |
| `["gemm", "fusedmul", "xf", "32"]`       |   9.954 ms (5%) |         |  160 bytes (1%) |           6 |
| `["gemm", "fusedmul", "xf", "8"]`        |   2.479 ms (5%) |         |  160 bytes (1%) |           6 |
| `["gemm", "mul", "linalg", "256"]`       |   1.207 ms (5%) |         |                 |             |
| `["gemm", "mul", "linalg", "32"]`        |   3.800 μs (5%) |         |                 |             |
| `["gemm", "mul", "linalg", "8"]`         | 300.000 ns (5%) |         |                 |             |
| `["gemm", "mul", "man", "false", "256"]` |   4.294 ms (5%) |         |                 |             |
| `["gemm", "mul", "man", "false", "32"]`  |   6.900 μs (5%) |         |                 |             |
| `["gemm", "mul", "man", "false", "8"]`   | 400.000 ns (5%) |         |                 |             |
| `["gemm", "mul", "man", "ivdep", "256"]` |   4.266 ms (5%) |         |                 |             |
| `["gemm", "mul", "man", "ivdep", "32"]`  |   6.100 μs (5%) |         |                 |             |
| `["gemm", "mul", "man", "ivdep", "8"]`   | 400.000 ns (5%) |         |                 |             |
| `["gemm", "mul", "man", "true", "256"]`  |   4.273 ms (5%) |         |                 |             |
| `["gemm", "mul", "man", "true", "32"]`   |   6.800 μs (5%) |         |                 |             |
| `["gemm", "mul", "man", "true", "8"]`    | 400.000 ns (5%) |         |                 |             |
| `["gemm", "mul", "xf", "false", "256"]`  |   4.169 ms (5%) |         |   48 bytes (1%) |           2 |
| `["gemm", "mul", "xf", "false", "32"]`   |   6.900 μs (5%) |         |   48 bytes (1%) |           2 |
| `["gemm", "mul", "xf", "false", "8"]`    | 300.000 ns (5%) |         |   48 bytes (1%) |           2 |
| `["gemm", "mul", "xf", "ivdep", "256"]`  |   4.267 ms (5%) |         |   48 bytes (1%) |           2 |
| `["gemm", "mul", "xf", "ivdep", "32"]`   |   5.700 μs (5%) |         |   48 bytes (1%) |           2 |
| `["gemm", "mul", "xf", "ivdep", "8"]`    | 400.000 ns (5%) |         |   48 bytes (1%) |           2 |
| `["gemm", "mul", "xf", "true", "256"]`   |   4.171 ms (5%) |         |   48 bytes (1%) |           2 |
| `["gemm", "mul", "xf", "true", "32"]`    |   6.700 μs (5%) |         |   48 bytes (1%) |           2 |
| `["gemm", "mul", "xf", "true", "8"]`     | 400.000 ns (5%) |         |   48 bytes (1%) |           2 |
| `["groupby", "sum", "sac"]`              | 205.603 μs (5%) |         | 313.14 KiB (1%) |       10007 |
| `["groupby", "sum", "xf-with-init"]`     | 155.202 μs (5%) |         | 157.44 KiB (1%) |       10008 |
| `["groupby", "sum", "xf-without-init"]`  | 157.402 μs (5%) |         | 157.44 KiB (1%) |       10008 |
| `["mapcat_eduction", "base"]`            |   1.480 μs (5%) |         |                 |             |
| `["mapcat_eduction", "xf-eduction"]`     |   1.600 μs (5%) |         |                 |             |
| `["mapcat_eduction", "xf-xf"]`           |   1.600 μs (5%) |         |                 |             |
| `["missing_argmax", "man"]`              | 900.000 ns (5%) |         |   32 bytes (1%) |           1 |
| `["missing_argmax", "rf"]`               |   2.111 μs (5%) |         |   32 bytes (1%) |           1 |
| `["missing_argmax", "xf"]`               |   2.100 μs (5%) |         |   32 bytes (1%) |           1 |
| `["missing_dot", "equiv"]`               | 917.308 ns (5%) |         |   16 bytes (1%) |           1 |
| `["missing_dot", "man"]`                 | 918.182 ns (5%) |         |   16 bytes (1%) |           1 |
| `["missing_dot", "naive"]`               |   4.029 μs (5%) |         |   16 bytes (1%) |           1 |
| `["missing_dot", "rf"]`                  | 896.667 ns (5%) |         |   16 bytes (1%) |           1 |
| `["missing_dot", "rf_nota"]`             | 923.077 ns (5%) |         |   16 bytes (1%) |           1 |
| `["missing_dot", "xf"]`                  | 187.201 μs (5%) |         |  72.11 KiB (1%) |        3740 |
| `["missing_dot", "xf_nota"]`             | 175.101 μs (5%) |         |  72.30 KiB (1%) |        3748 |
| `["overhead", "foldl"]`                  |   3.900 ns (5%) |         |                 |             |
| `["overhead", "reduce_basecase"]`        | 236.758 ns (5%) |         |  464 bytes (1%) |           9 |
| `["partition_by", "man"]`                |   1.642 ms (5%) |         |  352 bytes (1%) |           4 |
| `["partition_by", "xf"]`                 |   2.471 ms (5%) |         |   6.10 MiB (1%) |      200007 |
| `["set", "base"]`                        |   4.393 ms (5%) |         |  49.58 KiB (1%) |          18 |
| `["set", "xf"]`                          |   3.920 ms (5%) |         |  49.63 KiB (1%) |          21 |

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
      Ubuntu 18.04.4 LTS
  uname: Linux 5.3.0-1034-azure #35~18.04.1-Ubuntu SMP Mon Jul 13 12:54:45 UTC 2020 x86_64 x86_64
  CPU: Intel(R) Xeon(R) CPU E5-2673 v4 @ 2.30GHz: 
              speed         user         nice          sys         idle          irq
       #1  2294 MHz      74183 s          0 s       1396 s      21889 s          0 s
       #2  2294 MHz      17649 s          0 s       1490 s      78994 s          0 s
       
  Memory: 6.764881134033203 GB (2716.8125 MB free)
  Uptime: 996.0 sec
  Load Avg:  1.08349609375  1.0166015625  0.73046875
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-8.0.1 (ORCJIT, broadwell)
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
    Model:               79
    Model name:          Intel(R) Xeon(R) CPU E5-2673 v4 @ 2.30GHz
    Stepping:            1
    CPU MHz:             2294.684
    BogoMIPS:            4589.36
    Hypervisor vendor:   Microsoft
    Virtualization type: full
    L1d cache:           32K
    L1i cache:           32K
    L2 cache:            256K
    L3 cache:            51200K
    NUMA node0 CPU(s):   0,1
    Flags:               fpu vme de pse tsc msr pae mce cx8 apic sep mtrr pge mca cmov pat pse36 clflush mmx fxsr sse sse2 ss ht syscall nx pdpe1gb rdtscp lm constant_tsc rep_good nopl xtopology cpuid pni pclmulqdq ssse3 fma cx16 pcid sse4_1 sse4_2 movbe popcnt aes xsave avx f16c rdrand hypervisor lahf_lm abm 3dnowprefetch invpcid_single pti fsgsbase bmi1 hle avx2 smep bmi2 erms invpcid rtm rdseed adx smap xsaveopt md_clear
    

| Cpu Property       | Value                                                   |
|:------------------ |:------------------------------------------------------- |
| Brand              | Intel(R) Xeon(R) CPU E5-2673 v4 @ 2.30GHz               |
| Vendor             | :Intel                                                  |
| Architecture       | :Broadwell                                              |
| Model              | Family: 0x06, Model: 0x4f, Stepping: 0x01, Type: 0x00   |
| Cores              | 2 physical cores, 2 logical cores (on executing CPU)    |
|                    | No Hyperthreading detected                              |
| Clock Frequencies  | Not supported by CPU                                    |
| Data Cache         | Level 1:3 : (32, 256, 51200) kbytes                     |
|                    | 64 byte cache line size                                 |
| Address Size       | 48 bits virtual, 44 bits physical                       |
| SIMD               | 256 bit = 32 byte max. SIMD vector size                 |
| Time Stamp Counter | TSC is accessible via `rdtsc`                           |
|                    | TSC increased at every clock cycle (non-invariant TSC)  |
| Perf. Monitoring   | Performance Monitoring Counters (PMC) are not supported |
| Hypervisor         | Yes, Microsoft                                          |

