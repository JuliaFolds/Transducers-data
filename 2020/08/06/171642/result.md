# Benchmark result

* Pull request commit: [`c06a9795c8360cb8029805fc1835a9370677b4aa`](https://github.com/JuliaFolds/Transducers.jl/commit/c06a9795c8360cb8029805fc1835a9370677b4aa)
* Pull request: <https://github.com/JuliaFolds/Transducers.jl/pull/397> (Define collect(::Foldable) rather than collect(::Eduction))

# Judge result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmarks:
    - Target: 6 Aug 2020 - 17:11
    - Baseline: 6 Aug 2020 - 17:16
* Package commits:
    - Target: f855af
    - Baseline: 76f082
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
| `["cat", "base"]`                        | 0.92 (5%) :white_check_mark: |    1.00 (1%)  |
| `["dict", "base"]`                       | 0.95 (5%) :white_check_mark: |    1.00 (1%)  |
| `["dict", "xf"]`                         | 0.94 (5%) :white_check_mark: |    1.00 (1%)  |
| `["dot", "blas"]`                        | 0.95 (5%) :white_check_mark: |    1.00 (1%)  |
| `["filter_map_map!", "man"]`             |                1.14 (5%) :x: |    1.00 (1%)  |
| `["findall", "xf-array"]`                |                   0.98 (5%)  | 1.02 (1%) :x: |
| `["gemm", "fusedmul", "blas", "2"]`      |                1.06 (5%) :x: |    1.00 (1%)  |
| `["gemm", "fusedmul", "xf", "16"]`       |                1.08 (5%) :x: |    1.00 (1%)  |
| `["gemm", "fusedmul", "xf", "8"]`        | 0.85 (5%) :white_check_mark: |    1.00 (1%)  |
| `["gemm", "mul", "linalg", "32"]`        | 0.84 (5%) :white_check_mark: |    1.00 (1%)  |
| `["gemm", "mul", "man", "false", "8"]`   | 0.80 (5%) :white_check_mark: |    1.00 (1%)  |
| `["gemm", "mul", "man", "ivdep", "256"]` | 0.95 (5%) :white_check_mark: |    1.00 (1%)  |
| `["gemm", "mul", "man", "ivdep", "32"]`  | 0.89 (5%) :white_check_mark: |    1.00 (1%)  |
| `["gemm", "mul", "man", "ivdep", "8"]`   |                1.07 (5%) :x: |    1.00 (1%)  |
| `["gemm", "mul", "man", "true", "8"]`    |                1.37 (5%) :x: |    1.00 (1%)  |
| `["gemm", "mul", "xf", "false", "8"]`    | 0.79 (5%) :white_check_mark: |    1.00 (1%)  |
| `["gemm", "mul", "xf", "ivdep", "8"]`    |                1.26 (5%) :x: |    1.00 (1%)  |
| `["gemm", "mul", "xf", "true", "256"]`   | 0.94 (5%) :white_check_mark: |    1.00 (1%)  |
| `["gemm", "mul", "xf", "true", "8"]`     |                1.23 (5%) :x: |    1.00 (1%)  |
| `["mapcat_eduction", "base"]`            | 0.94 (5%) :white_check_mark: |    1.00 (1%)  |
| `["mapcat_eduction", "xf-xf"]`           |                1.07 (5%) :x: |    1.00 (1%)  |
| `["missing_argmax", "rf"]`               |                1.29 (5%) :x: |    1.00 (1%)  |
| `["missing_argmax", "xf"]`               | 0.80 (5%) :white_check_mark: |    1.00 (1%)  |
| `["missing_dot", "equiv"]`               | 0.91 (5%) :white_check_mark: |    1.00 (1%)  |
| `["missing_dot", "rf_nota"]`             | 0.89 (5%) :white_check_mark: |    1.00 (1%)  |
| `["missing_dot", "xf_nota"]`             |                1.14 (5%) :x: |    1.00 (1%)  |
| `["overhead", "foldl"]`                  |                1.15 (5%) :x: |    1.00 (1%)  |
| `["set", "xf"]`                          |                1.10 (5%) :x: |    1.00 (1%)  |

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
       #1  2095 MHz       6279 s          0 s       1459 s      63780 s          0 s
       #2  2095 MHz      61530 s          0 s       1822 s       9153 s          0 s
       
  Memory: 6.764881134033203 GB (2875.67578125 MB free)
  Uptime: 740.0 sec
  Load Avg:  1.0  0.9501953125  0.60302734375
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
       #1  2095 MHz      11782 s          0 s       1557 s      86689 s          0 s
       #2  2095 MHz      84546 s          0 s       1908 s      14581 s          0 s
       
  Memory: 6.764881134033203 GB (2837.55859375 MB free)
  Uptime: 1027.0 sec
  Load Avg:  1.0029296875  1.0  0.732421875
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-8.0.1 (ORCJIT, skylake)
```

---
# Target result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmark: 6 Aug 2020 - 17:11
* Package commit: f855af
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
| `["append!!", "eduction"]`               |  17.902 μs (5%) |         |  64.72 KiB (1%) |          18 |
| `["append!!", "xf"]`                     |  17.402 μs (5%) |         |  64.72 KiB (1%) |          18 |
| `["cat", "base"]`                        |   1.440 μs (5%) |         |                 |             |
| `["cat", "xf"]`                          |   1.650 μs (5%) |         |                 |             |
| `["collect", "filter-missing"]`          |  94.011 μs (5%) |         | 345.31 KiB (1%) |       10015 |
| `["collect", "identity-float"]`          |  73.808 μs (5%) |         | 569.16 KiB (1%) |       10015 |
| `["collect", "identity-union"]`          | 282.334 μs (5%) |         | 705.17 KiB (1%) |       16669 |
| `["dict", "base"]`                       |   3.636 ms (5%) |         |  92.91 KiB (1%) |          22 |
| `["dict", "xf"]`                         |   3.683 ms (5%) |         |  92.36 KiB (1%) |          21 |
| `["dot", "blas"]`                        |   1.120 μs (5%) |         |                 |             |
| `["dot", "man"]`                         |   1.010 μs (5%) |         |                 |             |
| `["dot", "rf"]`                          |   1.790 μs (5%) |         |                 |             |
| `["dot", "xf"]`                          |   1.870 μs (5%) |         |   64 bytes (1%) |           3 |
| `["filter_map_map!", "man"]`             |  72.405 μs (5%) |         |                 |             |
| `["filter_map_map!", "xf"]`              | 631.443 μs (5%) |         |  304 bytes (1%) |          17 |
| `["filter_map_reduce", "man"]`           | 192.119 μs (5%) |         |                 |             |
| `["filter_map_reduce", "xf"]`            | 191.920 μs (5%) |         |                 |             |
| `["findall", "base"]`                    | 739.781 μs (5%) |         |   2.00 MiB (1%) |          21 |
| `["findall", "xf-array"]`                | 687.074 μs (5%) |         |   3.05 MiB (1%) |      100010 |
| `["findall", "xf-iter"]`                 | 797.985 μs (5%) |         |   5.05 MiB (1%) |       99919 |
| `["gemm", "fusedmul", "blas", "16"]`     |   4.206 ms (5%) |         |                 |             |
| `["gemm", "fusedmul", "blas", "2"]`      |   3.097 ms (5%) |         |                 |             |
| `["gemm", "fusedmul", "blas", "32"]`     |   5.763 ms (5%) |         |                 |             |
| `["gemm", "fusedmul", "blas", "8"]`      |   3.309 ms (5%) |         |                 |             |
| `["gemm", "fusedmul", "xf", "16"]`       |   5.157 ms (5%) |         |  160 bytes (1%) |           6 |
| `["gemm", "fusedmul", "xf", "2"]`        | 481.834 μs (5%) |         |  160 bytes (1%) |           6 |
| `["gemm", "fusedmul", "xf", "32"]`       |   8.955 ms (5%) |         |  160 bytes (1%) |           6 |
| `["gemm", "fusedmul", "xf", "8"]`        |   2.141 ms (5%) |         |  160 bytes (1%) |           6 |
| `["gemm", "mul", "linalg", "256"]`       | 743.768 μs (5%) |         |                 |             |
| `["gemm", "mul", "linalg", "32"]`        |   2.511 μs (5%) |         |                 |             |
| `["gemm", "mul", "linalg", "8"]`         | 201.714 ns (5%) |         |                 |             |
| `["gemm", "mul", "man", "false", "256"]` |   1.328 ms (5%) |         |                 |             |
| `["gemm", "mul", "man", "false", "32"]`  |   4.115 μs (5%) |         |                 |             |
| `["gemm", "mul", "man", "false", "8"]`   | 318.825 ns (5%) |         |                 |             |
| `["gemm", "mul", "man", "ivdep", "256"]` |   1.357 ms (5%) |         |                 |             |
| `["gemm", "mul", "man", "ivdep", "32"]`  |   3.275 μs (5%) |         |                 |             |
| `["gemm", "mul", "man", "ivdep", "8"]`   | 319.684 ns (5%) |         |                 |             |
| `["gemm", "mul", "man", "true", "256"]`  |   1.338 ms (5%) |         |                 |             |
| `["gemm", "mul", "man", "true", "32"]`   |   4.215 μs (5%) |         |                 |             |
| `["gemm", "mul", "man", "true", "8"]`    | 409.535 ns (5%) |         |                 |             |
| `["gemm", "mul", "xf", "false", "256"]`  |   1.331 ms (5%) |         |   48 bytes (1%) |           2 |
| `["gemm", "mul", "xf", "false", "32"]`   |   4.986 μs (5%) |         |   48 bytes (1%) |           2 |
| `["gemm", "mul", "xf", "false", "8"]`    | 316.127 ns (5%) |         |   48 bytes (1%) |           2 |
| `["gemm", "mul", "xf", "ivdep", "256"]`  |   1.372 ms (5%) |         |   48 bytes (1%) |           2 |
| `["gemm", "mul", "xf", "ivdep", "32"]`   |   3.150 μs (5%) |         |   48 bytes (1%) |           2 |
| `["gemm", "mul", "xf", "ivdep", "8"]`    | 377.480 ns (5%) |         |   48 bytes (1%) |           2 |
| `["gemm", "mul", "xf", "true", "256"]`   |   1.362 ms (5%) |         |   48 bytes (1%) |           2 |
| `["gemm", "mul", "xf", "true", "32"]`    |   4.129 μs (5%) |         |   48 bytes (1%) |           2 |
| `["gemm", "mul", "xf", "true", "8"]`     | 368.410 ns (5%) |         |   48 bytes (1%) |           2 |
| `["groupby", "sum", "sac"]`              | 214.415 μs (5%) |         | 313.14 KiB (1%) |       10007 |
| `["groupby", "sum", "xf-with-init"]`     | 150.610 μs (5%) |         | 157.44 KiB (1%) |       10008 |
| `["groupby", "sum", "xf-without-init"]`  | 156.510 μs (5%) |         | 157.44 KiB (1%) |       10008 |
| `["mapcat_eduction", "base"]`            |   1.550 μs (5%) |         |                 |             |
| `["mapcat_eduction", "xf-eduction"]`     |   1.570 μs (5%) |         |                 |             |
| `["mapcat_eduction", "xf-xf"]`           |   1.680 μs (5%) |         |                 |             |
| `["missing_argmax", "man"]`              |   2.234 μs (5%) |         |   32 bytes (1%) |           1 |
| `["missing_argmax", "rf"]`               |   2.700 μs (5%) |         |   32 bytes (1%) |           1 |
| `["missing_argmax", "xf"]`               |   2.156 μs (5%) |         |   32 bytes (1%) |           1 |
| `["missing_dot", "equiv"]`               |   1.270 μs (5%) |         |   16 bytes (1%) |           1 |
| `["missing_dot", "man"]`                 |   1.170 μs (5%) |         |   16 bytes (1%) |           1 |
| `["missing_dot", "naive"]`               |   4.100 μs (5%) |         |   16 bytes (1%) |           1 |
| `["missing_dot", "rf"]`                  |   1.130 μs (5%) |         |   16 bytes (1%) |           1 |
| `["missing_dot", "rf_nota"]`             |   1.260 μs (5%) |         |   16 bytes (1%) |           1 |
| `["missing_dot", "xf"]`                  | 177.517 μs (5%) |         |  72.02 KiB (1%) |        3736 |
| `["missing_dot", "xf_nota"]`             | 205.820 μs (5%) |         |  72.38 KiB (1%) |        3752 |
| `["overhead", "foldl"]`                  |   4.500 ns (5%) |         |                 |             |
| `["overhead", "reduce_basecase"]`        | 225.678 ns (5%) |         |  464 bytes (1%) |           9 |
| `["partition_by", "man"]`                |   1.744 ms (5%) |         |  352 bytes (1%) |           4 |
| `["partition_by", "xf"]`                 |   2.700 ms (5%) |         |   6.10 MiB (1%) |      200007 |
| `["set", "base"]`                        |   4.696 ms (5%) |         |  49.58 KiB (1%) |          18 |
| `["set", "xf"]`                          |   4.335 ms (5%) |         |  49.63 KiB (1%) |          21 |

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
       #1  2095 MHz       6279 s          0 s       1459 s      63780 s          0 s
       #2  2095 MHz      61530 s          0 s       1822 s       9153 s          0 s
       
  Memory: 6.764881134033203 GB (2875.67578125 MB free)
  Uptime: 740.0 sec
  Load Avg:  1.0  0.9501953125  0.60302734375
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-8.0.1 (ORCJIT, skylake)
```

---
# Baseline result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmark: 6 Aug 2020 - 17:16
* Package commit: 76f082
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
| `["append!!", "eduction"]`               |  17.301 μs (5%) |         |  64.72 KiB (1%) |          18 |
| `["append!!", "xf"]`                     |  16.901 μs (5%) |         |  64.72 KiB (1%) |          18 |
| `["cat", "base"]`                        |   1.560 μs (5%) |         |                 |             |
| `["cat", "xf"]`                          |   1.650 μs (5%) |         |                 |             |
| `["collect", "filter-missing"]`          |  95.006 μs (5%) |         | 345.31 KiB (1%) |       10015 |
| `["collect", "identity-float"]`          |  71.004 μs (5%) |         | 569.16 KiB (1%) |       10015 |
| `["collect", "identity-union"]`          | 280.017 μs (5%) |         | 705.28 KiB (1%) |       16677 |
| `["dict", "base"]`                       |   3.830 ms (5%) |         |  92.91 KiB (1%) |          22 |
| `["dict", "xf"]`                         |   3.922 ms (5%) |         |  92.36 KiB (1%) |          21 |
| `["dot", "blas"]`                        |   1.180 μs (5%) |         |                 |             |
| `["dot", "man"]`                         |   1.040 μs (5%) |         |                 |             |
| `["dot", "rf"]`                          |   1.830 μs (5%) |         |                 |             |
| `["dot", "xf"]`                          |   1.860 μs (5%) |         |   64 bytes (1%) |           3 |
| `["filter_map_map!", "man"]`             |  63.408 μs (5%) |         |                 |             |
| `["filter_map_map!", "xf"]`              | 635.486 μs (5%) |         |  304 bytes (1%) |          17 |
| `["filter_map_reduce", "man"]`           | 191.910 μs (5%) |         |                 |             |
| `["filter_map_reduce", "xf"]`            | 192.211 μs (5%) |         |                 |             |
| `["findall", "base"]`                    | 718.742 μs (5%) |         |   2.00 MiB (1%) |          21 |
| `["findall", "xf-array"]`                | 700.340 μs (5%) |         |   3.01 MiB (1%) |       98445 |
| `["findall", "xf-iter"]`                 | 792.246 μs (5%) |         |   5.05 MiB (1%) |       99914 |
| `["gemm", "fusedmul", "blas", "16"]`     |   4.377 ms (5%) |         |                 |             |
| `["gemm", "fusedmul", "blas", "2"]`      |   2.924 ms (5%) |         |                 |             |
| `["gemm", "fusedmul", "blas", "32"]`     |   5.931 ms (5%) |         |                 |             |
| `["gemm", "fusedmul", "blas", "8"]`      |   3.241 ms (5%) |         |                 |             |
| `["gemm", "fusedmul", "xf", "16"]`       |   4.759 ms (5%) |         |  160 bytes (1%) |           6 |
| `["gemm", "fusedmul", "xf", "2"]`        | 483.127 μs (5%) |         |  160 bytes (1%) |           6 |
| `["gemm", "fusedmul", "xf", "32"]`       |   9.339 ms (5%) |         |  160 bytes (1%) |           6 |
| `["gemm", "fusedmul", "xf", "8"]`        |   2.519 ms (5%) |         |  160 bytes (1%) |           6 |
| `["gemm", "mul", "linalg", "256"]`       | 746.342 μs (5%) |         |                 |             |
| `["gemm", "mul", "linalg", "32"]`        |   3.000 μs (5%) |         |                 |             |
| `["gemm", "mul", "linalg", "8"]`         | 200.000 ns (5%) |         |                 |             |
| `["gemm", "mul", "man", "false", "256"]` |   1.391 ms (5%) |         |                 |             |
| `["gemm", "mul", "man", "false", "32"]`  |   4.200 μs (5%) |         |                 |             |
| `["gemm", "mul", "man", "false", "8"]`   | 400.000 ns (5%) |         |                 |             |
| `["gemm", "mul", "man", "ivdep", "256"]` |   1.433 ms (5%) |         |                 |             |
| `["gemm", "mul", "man", "ivdep", "32"]`  |   3.700 μs (5%) |         |                 |             |
| `["gemm", "mul", "man", "ivdep", "8"]`   | 300.000 ns (5%) |         |                 |             |
| `["gemm", "mul", "man", "true", "256"]`  |   1.383 ms (5%) |         |                 |             |
| `["gemm", "mul", "man", "true", "32"]`   |   4.200 μs (5%) |         |                 |             |
| `["gemm", "mul", "man", "true", "8"]`    | 300.000 ns (5%) |         |                 |             |
| `["gemm", "mul", "xf", "false", "256"]`  |   1.398 ms (5%) |         |   48 bytes (1%) |           2 |
| `["gemm", "mul", "xf", "false", "32"]`   |   5.000 μs (5%) |         |   48 bytes (1%) |           2 |
| `["gemm", "mul", "xf", "false", "8"]`    | 400.000 ns (5%) |         |   48 bytes (1%) |           2 |
| `["gemm", "mul", "xf", "ivdep", "256"]`  |   1.378 ms (5%) |         |   48 bytes (1%) |           2 |
| `["gemm", "mul", "xf", "ivdep", "32"]`   |   3.200 μs (5%) |         |   48 bytes (1%) |           2 |
| `["gemm", "mul", "xf", "ivdep", "8"]`    | 300.000 ns (5%) |         |   48 bytes (1%) |           2 |
| `["gemm", "mul", "xf", "true", "256"]`   |   1.445 ms (5%) |         |   48 bytes (1%) |           2 |
| `["gemm", "mul", "xf", "true", "32"]`    |   4.200 μs (5%) |         |   48 bytes (1%) |           2 |
| `["gemm", "mul", "xf", "true", "8"]`     | 300.000 ns (5%) |         |   48 bytes (1%) |           2 |
| `["groupby", "sum", "sac"]`              | 220.528 μs (5%) |         | 313.14 KiB (1%) |       10007 |
| `["groupby", "sum", "xf-with-init"]`     | 153.720 μs (5%) |         | 157.44 KiB (1%) |       10008 |
| `["groupby", "sum", "xf-without-init"]`  | 162.422 μs (5%) |         | 157.44 KiB (1%) |       10008 |
| `["mapcat_eduction", "base"]`            |   1.650 μs (5%) |         |                 |             |
| `["mapcat_eduction", "xf-eduction"]`     |   1.570 μs (5%) |         |                 |             |
| `["mapcat_eduction", "xf-xf"]`           |   1.570 μs (5%) |         |                 |             |
| `["missing_argmax", "man"]`              |   2.233 μs (5%) |         |   32 bytes (1%) |           1 |
| `["missing_argmax", "rf"]`               |   2.100 μs (5%) |         |   32 bytes (1%) |           1 |
| `["missing_argmax", "xf"]`               |   2.689 μs (5%) |         |   32 bytes (1%) |           1 |
| `["missing_dot", "equiv"]`               |   1.400 μs (5%) |         |   16 bytes (1%) |           1 |
| `["missing_dot", "man"]`                 |   1.140 μs (5%) |         |   16 bytes (1%) |           1 |
| `["missing_dot", "naive"]`               |   4.157 μs (5%) |         |   16 bytes (1%) |           1 |
| `["missing_dot", "rf"]`                  |   1.170 μs (5%) |         |   16 bytes (1%) |           1 |
| `["missing_dot", "rf_nota"]`             |   1.410 μs (5%) |         |   16 bytes (1%) |           1 |
| `["missing_dot", "xf"]`                  | 178.810 μs (5%) |         |  72.25 KiB (1%) |        3748 |
| `["missing_dot", "xf_nota"]`             | 180.310 μs (5%) |         |  72.33 KiB (1%) |        3750 |
| `["overhead", "foldl"]`                  |   3.900 ns (5%) |         |                 |             |
| `["overhead", "reduce_basecase"]`        | 229.361 ns (5%) |         |  464 bytes (1%) |           9 |
| `["partition_by", "man"]`                |   1.734 ms (5%) |         |  352 bytes (1%) |           4 |
| `["partition_by", "xf"]`                 |   2.791 ms (5%) |         |   6.10 MiB (1%) |      200007 |
| `["set", "base"]`                        |   4.506 ms (5%) |         |  49.58 KiB (1%) |          18 |
| `["set", "xf"]`                          |   3.938 ms (5%) |         |  49.63 KiB (1%) |          21 |

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
       #1  2095 MHz      11782 s          0 s       1557 s      86689 s          0 s
       #2  2095 MHz      84546 s          0 s       1908 s      14581 s          0 s
       
  Memory: 6.764881134033203 GB (2837.55859375 MB free)
  Uptime: 1027.0 sec
  Load Avg:  1.0029296875  1.0  0.732421875
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
    CPU MHz:             2095.250
    BogoMIPS:            4190.50
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

