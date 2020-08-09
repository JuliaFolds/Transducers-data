# Benchmark result

* Pull request commit: [`82444ea9b6aa6e87f66da77ed9d727975cda705b`](https://github.com/JuliaFolds/Transducers.jl/commit/82444ea9b6aa6e87f66da77ed9d727975cda705b)
* Pull request: <https://github.com/JuliaFolds/Transducers.jl/pull/404> (Add bench_filter_sum.jl)

# Judge result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmarks:
    - Target: 9 Aug 2020 - 04:31
    - Baseline: 9 Aug 2020 - 04:36
* Package commits:
    - Target: 396ae9
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
| `["cat", "base"]`                        | 0.93 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["cat", "xf"]`                          |                1.19 (5%) :x: |                   1.00 (1%)  |
| `["dot", "man"]`                         | 0.93 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["filter_map_map!", "man"]`             |                1.18 (5%) :x: |                   1.00 (1%)  |
| `["filter_map_map!", "xf"]`              | 0.94 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["findall", "xf-array"]`                |                   0.98 (5%)  | 0.98 (1%) :white_check_mark: |
| `["gemm", "fusedmul", "blas", "8"]`      | 0.93 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["gemm", "fusedmul", "xf", "16"]`       |                1.22 (5%) :x: |                   1.00 (1%)  |
| `["gemm", "fusedmul", "xf", "2"]`        |                1.11 (5%) :x: |                   1.00 (1%)  |
| `["gemm", "fusedmul", "xf", "8"]`        | 0.75 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["gemm", "mul", "man", "false", "32"]`  |                1.09 (5%) :x: |                   1.00 (1%)  |
| `["gemm", "mul", "man", "false", "8"]`   |                1.38 (5%) :x: |                   1.00 (1%)  |
| `["gemm", "mul", "man", "ivdep", "8"]`   |                1.06 (5%) :x: |                   1.00 (1%)  |
| `["gemm", "mul", "man", "true", "8"]`    | 0.83 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["gemm", "mul", "xf", "false", "32"]`   |                1.35 (5%) :x: |                   1.00 (1%)  |
| `["gemm", "mul", "xf", "false", "8"]`    |                1.07 (5%) :x: |                   1.00 (1%)  |
| `["gemm", "mul", "xf", "ivdep", "32"]`   |                1.05 (5%) :x: |                   1.00 (1%)  |
| `["gemm", "mul", "xf", "ivdep", "8"]`    | 0.76 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["gemm", "mul", "xf", "true", "32"]`    |                1.14 (5%) :x: |                   1.00 (1%)  |
| `["gemm", "mul", "xf", "true", "8"]`     |                1.35 (5%) :x: |                   1.00 (1%)  |
| `["groupby", "sum", "xf-with-init"]`     |                1.07 (5%) :x: |                   1.00 (1%)  |
| `["missing_dot", "rf_nota"]`             | 0.90 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["missing_dot", "xf_nota"]`             |                1.06 (5%) :x: |                   1.00 (1%)  |

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
  CPU: Intel(R) Xeon(R) Platinum 8171M CPU @ 2.60GHz: 
              speed         user         nice          sys         idle          irq
       #1  2095 MHz      37782 s          0 s       1246 s      31539 s          0 s
       #2  2095 MHz      29750 s          0 s       1779 s      39622 s          0 s
       
  Memory: 6.764881134033203 GB (2814.1015625 MB free)
  Uptime: 728.0 sec
  Load Avg:  1.0  0.99462890625  0.671875
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
  CPU: Intel(R) Xeon(R) Platinum 8171M CPU @ 2.60GHz: 
              speed         user         nice          sys         idle          irq
       #1  2095 MHz      52600 s          0 s       1337 s      42901 s          0 s
       #2  2095 MHz      41101 s          0 s       1908 s      54439 s          0 s
       
  Memory: 6.764881134033203 GB (2770.8359375 MB free)
  Uptime: 992.0 sec
  Load Avg:  1.01611328125  1.0185546875  0.77294921875
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-8.0.1 (ORCJIT, skylake)
```

---
# Target result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmark: 9 Aug 2020 - 4:31
* Package commit: 396ae9
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

| ID                                                                                | time            | GC time | memory          | allocations |
|-----------------------------------------------------------------------------------|----------------:|--------:|----------------:|------------:|
| `["append!!", "eduction"]`                                                        |  15.602 μs (5%) |         |  64.72 KiB (1%) |          18 |
| `["append!!", "xf"]`                                                              |  15.601 μs (5%) |         |  64.72 KiB (1%) |          18 |
| `["cat", "base"]`                                                                 |   1.560 μs (5%) |         |                 |             |
| `["cat", "xf"]`                                                                   |   1.960 μs (5%) |         |                 |             |
| `["collect", "filter-missing"]`                                                   |  90.706 μs (5%) |         | 345.31 KiB (1%) |       10015 |
| `["collect", "identity-float"]`                                                   |  64.105 μs (5%) |         | 569.16 KiB (1%) |       10015 |
| `["collect", "identity-union"]`                                                   | 264.618 μs (5%) |         | 705.13 KiB (1%) |       16667 |
| `["dict", "base"]`                                                                |   3.375 ms (5%) |         |  92.91 KiB (1%) |          22 |
| `["dict", "xf"]`                                                                  |   3.489 ms (5%) |         |  92.36 KiB (1%) |          21 |
| `["dot", "blas"]`                                                                 | 990.100 ns (5%) |         |                 |             |
| `["dot", "man"]`                                                                  | 950.100 ns (5%) |         |                 |             |
| `["dot", "rf"]`                                                                   |   1.780 μs (5%) |         |                 |             |
| `["dot", "xf"]`                                                                   |   1.850 μs (5%) |         |   64 bytes (1%) |           3 |
| `["filter_map_map!", "man"]`                                                      |  62.703 μs (5%) |         |                 |             |
| `["filter_map_map!", "xf"]`                                                       | 589.624 μs (5%) |         |  304 bytes (1%) |          17 |
| `["filter_map_reduce", "man"]`                                                    | 191.611 μs (5%) |         |                 |             |
| `["filter_map_reduce", "xf"]`                                                     | 191.712 μs (5%) |         |                 |             |
| `["filter_sum", ":xs => :RandomFloats", ":withinit => false", ":impl => :base"]`  |   1.160 μs (5%) |         |                 |             |
| `["filter_sum", ":xs => :RandomFloats", ":withinit => false", ":impl => :naive"]` |   1.100 μs (5%) |         |                 |             |
| `["filter_sum", ":xs => :RandomFloats", ":withinit => false", ":impl => :xf"]`    |   1.340 μs (5%) |         |                 |             |
| `["filter_sum", ":xs => :RandomFloats", ":withinit => true", ":impl => :base"]`   |   1.480 μs (5%) |         |                 |             |
| `["filter_sum", ":xs => :RandomFloats", ":withinit => true", ":impl => :naive"]`  | 690.651 ns (5%) |         |                 |             |
| `["filter_sum", ":xs => :RandomFloats", ":withinit => true", ":impl => :xf"]`     |   1.480 μs (5%) |         |                 |             |
| `["filter_sum", ":xs => :UnitRange", ":withinit => false", ":impl => :base"]`     |   1.500 μs (5%) |         |                 |             |
| `["filter_sum", ":xs => :UnitRange", ":withinit => false", ":impl => :naive"]`    | 705.643 ns (5%) |         |                 |             |
| `["filter_sum", ":xs => :UnitRange", ":withinit => false", ":impl => :xf"]`       |   1.340 μs (5%) |         |                 |             |
| `["filter_sum", ":xs => :UnitRange", ":withinit => true", ":impl => :base"]`      |  87.377 ns (5%) |         |                 |             |
| `["filter_sum", ":xs => :UnitRange", ":withinit => true", ":impl => :naive"]`     | 565.984 ns (5%) |         |                 |             |
| `["filter_sum", ":xs => :UnitRange", ":withinit => true", ":impl => :xf"]`        |  91.734 ns (5%) |         |                 |             |
| `["findall", "base"]`                                                             | 689.844 μs (5%) |         |   2.00 MiB (1%) |          21 |
| `["findall", "xf-array"]`                                                         | 644.740 μs (5%) |         |   2.98 MiB (1%) |       97538 |
| `["findall", "xf-iter"]`                                                          | 726.344 μs (5%) |         |   5.05 MiB (1%) |       99917 |
| `["gemm", "fusedmul", "blas", "16"]`                                              |   3.837 ms (5%) |         |                 |             |
| `["gemm", "fusedmul", "blas", "2"]`                                               |   2.968 ms (5%) |         |                 |             |
| `["gemm", "fusedmul", "blas", "32"]`                                              |   4.961 ms (5%) |         |                 |             |
| `["gemm", "fusedmul", "blas", "8"]`                                               |   2.841 ms (5%) |         |                 |             |
| `["gemm", "fusedmul", "xf", "16"]`                                                |   5.313 ms (5%) |         |  160 bytes (1%) |           6 |
| `["gemm", "fusedmul", "xf", "2"]`                                                 | 550.123 μs (5%) |         |  160 bytes (1%) |           6 |
| `["gemm", "fusedmul", "xf", "32"]`                                                |   7.268 ms (5%) |         |  160 bytes (1%) |           6 |
| `["gemm", "fusedmul", "xf", "8"]`                                                 |   1.803 ms (5%) |         |  160 bytes (1%) |           6 |
| `["gemm", "mul", "linalg", "256"]`                                                | 744.441 μs (5%) |         |                 |             |
| `["gemm", "mul", "linalg", "32"]`                                                 |   2.500 μs (5%) |         |                 |             |
| `["gemm", "mul", "linalg", "8"]`                                                  | 201.705 ns (5%) |         |                 |             |
| `["gemm", "mul", "man", "false", "256"]`                                          |   1.389 ms (5%) |         |                 |             |
| `["gemm", "mul", "man", "false", "32"]`                                           |   4.029 μs (5%) |         |                 |             |
| `["gemm", "mul", "man", "false", "8"]`                                            | 413.080 ns (5%) |         |                 |             |
| `["gemm", "mul", "man", "ivdep", "256"]`                                          |   1.375 ms (5%) |         |                 |             |
| `["gemm", "mul", "man", "ivdep", "32"]`                                           |   3.413 μs (5%) |         |                 |             |
| `["gemm", "mul", "man", "ivdep", "8"]`                                            | 318.389 ns (5%) |         |                 |             |
| `["gemm", "mul", "man", "true", "256"]`                                           |   1.383 ms (5%) |         |                 |             |
| `["gemm", "mul", "man", "true", "32"]`                                            |   4.029 μs (5%) |         |                 |             |
| `["gemm", "mul", "man", "true", "8"]`                                             | 333.197 ns (5%) |         |                 |             |
| `["gemm", "mul", "xf", "false", "256"]`                                           |   1.393 ms (5%) |         |   48 bytes (1%) |           2 |
| `["gemm", "mul", "xf", "false", "32"]`                                            |   5.000 μs (5%) |         |   48 bytes (1%) |           2 |
| `["gemm", "mul", "xf", "false", "8"]`                                             | 322.051 ns (5%) |         |   48 bytes (1%) |           2 |
| `["gemm", "mul", "xf", "ivdep", "256"]`                                           |   1.379 ms (5%) |         |   48 bytes (1%) |           2 |
| `["gemm", "mul", "xf", "ivdep", "32"]`                                            |   3.363 μs (5%) |         |   48 bytes (1%) |           2 |
| `["gemm", "mul", "xf", "ivdep", "8"]`                                             | 303.514 ns (5%) |         |   48 bytes (1%) |           2 |
| `["gemm", "mul", "xf", "true", "256"]`                                            |   1.410 ms (5%) |         |   48 bytes (1%) |           2 |
| `["gemm", "mul", "xf", "true", "32"]`                                             |   4.543 μs (5%) |         |   48 bytes (1%) |           2 |
| `["gemm", "mul", "xf", "true", "8"]`                                              | 404.520 ns (5%) |         |   48 bytes (1%) |           2 |
| `["groupby", "sum", "sac"]`                                                       | 207.108 μs (5%) |         | 313.14 KiB (1%) |       10007 |
| `["groupby", "sum", "xf-with-init"]`                                              | 163.106 μs (5%) |         | 157.44 KiB (1%) |       10008 |
| `["groupby", "sum", "xf-without-init"]`                                           | 159.006 μs (5%) |         | 157.44 KiB (1%) |       10008 |
| `["mapcat_eduction", "base"]`                                                     |   1.550 μs (5%) |         |                 |             |
| `["mapcat_eduction", "xf-eduction"]`                                              |   1.680 μs (5%) |         |                 |             |
| `["mapcat_eduction", "xf-xf"]`                                                    |   1.600 μs (5%) |         |                 |             |
| `["missing_argmax", "man"]`                                                       |   2.233 μs (5%) |         |   32 bytes (1%) |           1 |
| `["missing_argmax", "rf"]`                                                        |   2.089 μs (5%) |         |   32 bytes (1%) |           1 |
| `["missing_argmax", "xf"]`                                                        |   2.678 μs (5%) |         |   32 bytes (1%) |           1 |
| `["missing_dot", "equiv"]`                                                        |   1.430 μs (5%) |         |   16 bytes (1%) |           1 |
| `["missing_dot", "man"]`                                                          |   1.130 μs (5%) |         |   16 bytes (1%) |           1 |
| `["missing_dot", "naive"]`                                                        |   4.000 μs (5%) |         |   16 bytes (1%) |           1 |
| `["missing_dot", "rf"]`                                                           |   1.160 μs (5%) |         |   16 bytes (1%) |           1 |
| `["missing_dot", "rf_nota"]`                                                      |   1.220 μs (5%) |         |   16 bytes (1%) |           1 |
| `["missing_dot", "xf"]`                                                           | 179.410 μs (5%) |         |  72.19 KiB (1%) |        3744 |
| `["missing_dot", "xf_nota"]`                                                      | 175.410 μs (5%) |         |  71.98 KiB (1%) |        3736 |
| `["overhead", "foldl"]`                                                           |   3.900 ns (5%) |         |                 |             |
| `["overhead", "reduce_basecase"]`                                                 | 221.762 ns (5%) |         |  464 bytes (1%) |           9 |
| `["partition_by", "man"]`                                                         |   1.727 ms (5%) |         |  352 bytes (1%) |           4 |
| `["partition_by", "xf"]`                                                          |   2.553 ms (5%) |         |   6.10 MiB (1%) |      200007 |
| `["set", "base"]`                                                                 |   4.104 ms (5%) |         |  49.58 KiB (1%) |          18 |
| `["set", "xf"]`                                                                   |   3.746 ms (5%) |         |  49.63 KiB (1%) |          21 |

## Benchmark Group List
Here's a list of all the benchmark groups executed by this job:

- `["append!!"]`
- `["cat"]`
- `["collect"]`
- `["dict"]`
- `["dot"]`
- `["filter_map_map!"]`
- `["filter_map_reduce"]`
- `["filter_sum", ":xs => :RandomFloats", ":withinit => false"]`
- `["filter_sum", ":xs => :RandomFloats", ":withinit => true"]`
- `["filter_sum", ":xs => :UnitRange", ":withinit => false"]`
- `["filter_sum", ":xs => :UnitRange", ":withinit => true"]`
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
  CPU: Intel(R) Xeon(R) Platinum 8171M CPU @ 2.60GHz: 
              speed         user         nice          sys         idle          irq
       #1  2095 MHz      37782 s          0 s       1246 s      31539 s          0 s
       #2  2095 MHz      29750 s          0 s       1779 s      39622 s          0 s
       
  Memory: 6.764881134033203 GB (2814.1015625 MB free)
  Uptime: 728.0 sec
  Load Avg:  1.0  0.99462890625  0.671875
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-8.0.1 (ORCJIT, skylake)
```

---
# Baseline result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmark: 9 Aug 2020 - 4:36
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
| `["append!!", "eduction"]`               |  15.401 μs (5%) |         |  64.72 KiB (1%) |          18 |
| `["append!!", "xf"]`                     |  15.301 μs (5%) |         |  64.72 KiB (1%) |          18 |
| `["cat", "base"]`                        |   1.680 μs (5%) |         |                 |             |
| `["cat", "xf"]`                          |   1.650 μs (5%) |         |                 |             |
| `["collect", "filter-missing"]`          |  91.403 μs (5%) |         | 345.31 KiB (1%) |       10015 |
| `["collect", "identity-float"]`          |  61.602 μs (5%) |         | 569.16 KiB (1%) |       10015 |
| `["collect", "identity-union"]`          | 267.510 μs (5%) |         | 705.41 KiB (1%) |       16683 |
| `["dict", "base"]`                       |   3.411 ms (5%) |         |  92.91 KiB (1%) |          22 |
| `["dict", "xf"]`                         |   3.485 ms (5%) |         |  92.36 KiB (1%) |          21 |
| `["dot", "blas"]`                        |   1.010 μs (5%) |         |                 |             |
| `["dot", "man"]`                         |   1.020 μs (5%) |         |                 |             |
| `["dot", "rf"]`                          |   1.790 μs (5%) |         |                 |             |
| `["dot", "xf"]`                          |   1.830 μs (5%) |         |   64 bytes (1%) |           3 |
| `["filter_map_map!", "man"]`             |  53.006 μs (5%) |         |                 |             |
| `["filter_map_map!", "xf"]`              | 626.964 μs (5%) |         |  304 bytes (1%) |          17 |
| `["filter_map_reduce", "man"]`           | 191.806 μs (5%) |         |                 |             |
| `["filter_map_reduce", "xf"]`            | 191.806 μs (5%) |         |                 |             |
| `["findall", "base"]`                    | 668.222 μs (5%) |         |   2.00 MiB (1%) |          21 |
| `["findall", "xf-array"]`                | 656.623 μs (5%) |         |   3.05 MiB (1%) |       99977 |
| `["findall", "xf-iter"]`                 | 705.724 μs (5%) |         |   5.05 MiB (1%) |       99929 |
| `["gemm", "fusedmul", "blas", "16"]`     |   3.786 ms (5%) |         |                 |             |
| `["gemm", "fusedmul", "blas", "2"]`      |   2.933 ms (5%) |         |                 |             |
| `["gemm", "fusedmul", "blas", "32"]`     |   5.113 ms (5%) |         |                 |             |
| `["gemm", "fusedmul", "blas", "8"]`      |   3.052 ms (5%) |         |                 |             |
| `["gemm", "fusedmul", "xf", "16"]`       |   4.353 ms (5%) |         |  160 bytes (1%) |           6 |
| `["gemm", "fusedmul", "xf", "2"]`        | 493.854 μs (5%) |         |  160 bytes (1%) |           6 |
| `["gemm", "fusedmul", "xf", "32"]`       |   7.352 ms (5%) |         |  160 bytes (1%) |           6 |
| `["gemm", "fusedmul", "xf", "8"]`        |   2.393 ms (5%) |         |  160 bytes (1%) |           6 |
| `["gemm", "mul", "linalg", "256"]`       | 748.225 μs (5%) |         |                 |             |
| `["gemm", "mul", "linalg", "32"]`        |   2.600 μs (5%) |         |                 |             |
| `["gemm", "mul", "linalg", "8"]`         | 200.000 ns (5%) |         |                 |             |
| `["gemm", "mul", "man", "false", "256"]` |   1.457 ms (5%) |         |                 |             |
| `["gemm", "mul", "man", "false", "32"]`  |   3.700 μs (5%) |         |                 |             |
| `["gemm", "mul", "man", "false", "8"]`   | 300.000 ns (5%) |         |                 |             |
| `["gemm", "mul", "man", "ivdep", "256"]` |   1.426 ms (5%) |         |                 |             |
| `["gemm", "mul", "man", "ivdep", "32"]`  |   3.300 μs (5%) |         |                 |             |
| `["gemm", "mul", "man", "ivdep", "8"]`   | 300.000 ns (5%) |         |                 |             |
| `["gemm", "mul", "man", "true", "256"]`  |   1.442 ms (5%) |         |                 |             |
| `["gemm", "mul", "man", "true", "32"]`   |   4.100 μs (5%) |         |                 |             |
| `["gemm", "mul", "man", "true", "8"]`    | 400.000 ns (5%) |         |                 |             |
| `["gemm", "mul", "xf", "false", "256"]`  |   1.459 ms (5%) |         |   48 bytes (1%) |           2 |
| `["gemm", "mul", "xf", "false", "32"]`   |   3.700 μs (5%) |         |   48 bytes (1%) |           2 |
| `["gemm", "mul", "xf", "false", "8"]`    | 300.000 ns (5%) |         |   48 bytes (1%) |           2 |
| `["gemm", "mul", "xf", "ivdep", "256"]`  |   1.420 ms (5%) |         |   48 bytes (1%) |           2 |
| `["gemm", "mul", "xf", "ivdep", "32"]`   |   3.200 μs (5%) |         |   48 bytes (1%) |           2 |
| `["gemm", "mul", "xf", "ivdep", "8"]`    | 400.000 ns (5%) |         |   48 bytes (1%) |           2 |
| `["gemm", "mul", "xf", "true", "256"]`   |   1.448 ms (5%) |         |   48 bytes (1%) |           2 |
| `["gemm", "mul", "xf", "true", "32"]`    |   4.000 μs (5%) |         |   48 bytes (1%) |           2 |
| `["gemm", "mul", "xf", "true", "8"]`     | 300.000 ns (5%) |         |   48 bytes (1%) |           2 |
| `["groupby", "sum", "sac"]`              | 212.421 μs (5%) |         | 313.14 KiB (1%) |       10007 |
| `["groupby", "sum", "xf-with-init"]`     | 152.315 μs (5%) |         | 157.44 KiB (1%) |       10008 |
| `["groupby", "sum", "xf-without-init"]`  | 167.017 μs (5%) |         | 157.44 KiB (1%) |       10008 |
| `["mapcat_eduction", "base"]`            |   1.550 μs (5%) |         |                 |             |
| `["mapcat_eduction", "xf-eduction"]`     |   1.600 μs (5%) |         |                 |             |
| `["mapcat_eduction", "xf-xf"]`           |   1.590 μs (5%) |         |                 |             |
| `["missing_argmax", "man"]`              |   2.233 μs (5%) |         |   32 bytes (1%) |           1 |
| `["missing_argmax", "rf"]`               |   2.156 μs (5%) |         |   32 bytes (1%) |           1 |
| `["missing_argmax", "xf"]`               |   2.645 μs (5%) |         |   32 bytes (1%) |           1 |
| `["missing_dot", "equiv"]`               |   1.420 μs (5%) |         |   16 bytes (1%) |           1 |
| `["missing_dot", "man"]`                 |   1.120 μs (5%) |         |   16 bytes (1%) |           1 |
| `["missing_dot", "naive"]`               |   4.038 μs (5%) |         |   16 bytes (1%) |           1 |
| `["missing_dot", "rf"]`                  |   1.160 μs (5%) |         |   16 bytes (1%) |           1 |
| `["missing_dot", "rf_nota"]`             |   1.360 μs (5%) |         |   16 bytes (1%) |           1 |
| `["missing_dot", "xf"]`                  | 171.906 μs (5%) |         |  72.05 KiB (1%) |        3737 |
| `["missing_dot", "xf_nota"]`             | 166.106 μs (5%) |         |  72.19 KiB (1%) |        3746 |
| `["overhead", "foldl"]`                  |   3.900 ns (5%) |         |                 |             |
| `["overhead", "reduce_basecase"]`        | 221.754 ns (5%) |         |  464 bytes (1%) |           9 |
| `["partition_by", "man"]`                |   1.733 ms (5%) |         |  352 bytes (1%) |           4 |
| `["partition_by", "xf"]`                 |   2.557 ms (5%) |         |   6.10 MiB (1%) |      200007 |
| `["set", "base"]`                        |   3.984 ms (5%) |         |  49.58 KiB (1%) |          18 |
| `["set", "xf"]`                          |   3.760 ms (5%) |         |  49.63 KiB (1%) |          21 |

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
  CPU: Intel(R) Xeon(R) Platinum 8171M CPU @ 2.60GHz: 
              speed         user         nice          sys         idle          irq
       #1  2095 MHz      52600 s          0 s       1337 s      42901 s          0 s
       #2  2095 MHz      41101 s          0 s       1908 s      54439 s          0 s
       
  Memory: 6.764881134033203 GB (2770.8359375 MB free)
  Uptime: 992.0 sec
  Load Avg:  1.01611328125  1.0185546875  0.77294921875
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
    Model name:          Intel(R) Xeon(R) Platinum 8171M CPU @ 2.60GHz
    Stepping:            4
    CPU MHz:             2095.195
    BogoMIPS:            4190.39
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
| Brand              | Intel(R) Xeon(R) Platinum 8171M CPU @ 2.60GHz           |
| Vendor             | :Intel                                                  |
| Architecture       | :Skylake                                                |
| Model              | Family: 0x06, Model: 0x55, Stepping: 0x04, Type: 0x00   |
| Cores              | 2 physical cores, 2 logical cores (on executing CPU)    |
|                    | No Hyperthreading detected                              |
| Clock Frequencies  | Not supported by CPU                                    |
| Data Cache         | Level 1:3 : (32, 1024, 36608) kbytes                    |
|                    | 64 byte cache line size                                 |
| Address Size       | 48 bits virtual, 44 bits physical                       |
| SIMD               | 512 bit = 64 byte max. SIMD vector size                 |
| Time Stamp Counter | TSC is accessible via `rdtsc`                           |
|                    | TSC increased at every clock cycle (non-invariant TSC)  |
| Perf. Monitoring   | Performance Monitoring Counters (PMC) are not supported |
| Hypervisor         | Yes, Microsoft                                          |

