# Benchmark result

* Pull request commit: [`90eab4af42961d69501db9e52bb67f5f19f66ec7`](https://github.com/JuliaFolds/Transducers.jl/commit/90eab4af42961d69501db9e52bb67f5f19f66ec7)
* Pull request: <https://github.com/JuliaFolds/Transducers.jl/pull/243> (Update */Manifest.toml)

# Judge result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmarks:
    - Target: 5 Aug 2020 - 00:52
    - Baseline: 5 Aug 2020 - 00:57
* Package commits:
    - Target: 63bfc8
    - Baseline: 0e1a4a
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
| `["append!!", "eduction"]`               |                1.23 (5%) :x: |                   1.00 (1%)  |
| `["append!!", "xf"]`                     |                1.34 (5%) :x: |                   1.00 (1%)  |
| `["collect", "filter-missing"]`          |                1.08 (5%) :x: |                   1.00 (1%)  |
| `["collect", "identity-float"]`          |                1.12 (5%) :x: |                   1.00 (1%)  |
| `["collect", "identity-union"]`          |                1.10 (5%) :x: |                   1.00 (1%)  |
| `["dict", "xf"]`                         |                1.08 (5%) :x: |                   1.00 (1%)  |
| `["findall", "xf-array"]`                |                1.06 (5%) :x: |                1.04 (1%) :x: |
| `["gemm", "fusedmul", "xf", "16"]`       | 0.90 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["gemm", "mul", "linalg", "32"]`        | 0.91 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["gemm", "mul", "man", "false", "8"]`   | 0.94 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["gemm", "mul", "man", "ivdep", "8"]`   |                1.24 (5%) :x: |                   1.00 (1%)  |
| `["gemm", "mul", "man", "true", "32"]`   | 0.88 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["gemm", "mul", "man", "true", "8"]`    | 0.85 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["gemm", "mul", "xf", "ivdep", "32"]`   | 0.91 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["gemm", "mul", "xf", "ivdep", "8"]`    | 0.91 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["gemm", "mul", "xf", "true", "8"]`     | 0.94 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["groupby", "sum", "sac"]`              | 0.75 (5%) :white_check_mark: | 0.50 (1%) :white_check_mark: |
| `["groupby", "sum", "xf-without-init"]`  | 0.94 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["mapcat_eduction", "base"]`            | 0.94 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["mapcat_eduction", "xf-xf"]`           | 0.94 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["missing_argmax", "man"]`              |                1.10 (5%) :x: |                   1.00 (1%)  |
| `["missing_argmax", "rf"]`               |                1.07 (5%) :x: |                   1.00 (1%)  |
| `["missing_argmax", "xf"]`               |                1.05 (5%) :x: |                   1.00 (1%)  |
| `["missing_dot", "equiv"]`               | 0.94 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["missing_dot", "man"]`                 |                1.21 (5%) :x: |                   1.00 (1%)  |
| `["overhead", "foldl"]`                  |                1.07 (5%) :x: |                   1.00 (1%)  |
| `["overhead", "reduce_basecase"]`        |                1.09 (5%) :x: |                   1.00 (1%)  |

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
       #1  2294 MHz       8292 s          0 s       1269 s      65808 s          0 s
       #2  2294 MHz      62090 s          0 s       1746 s      11642 s          0 s
       
  Memory: 6.764881134033203 GB (2591.80859375 MB free)
  Uptime: 776.0 sec
  Load Avg:  1.0  0.98974609375  0.671875
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
       #1  2294 MHz      31965 s          0 s       1608 s      74391 s          0 s
       #2  2294 MHz      70408 s          0 s       2058 s      35604 s          0 s
       
  Memory: 6.764881134033203 GB (2677.5546875 MB free)
  Uptime: 1103.0 sec
  Load Avg:  1.0  1.0  0.78125
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-8.0.1 (ORCJIT, broadwell)
```

---
# Target result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmark: 5 Aug 2020 - 0:52
* Package commit: 63bfc8
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
| `["append!!", "eduction"]`               |  19.500 μs (5%) |         |  64.72 KiB (1%) |          18 |
| `["append!!", "xf"]`                     |  20.699 μs (5%) |         |  64.72 KiB (1%) |          18 |
| `["cat", "base"]`                        |   1.510 μs (5%) |         |                 |             |
| `["cat", "xf"]`                          |   1.690 μs (5%) |         |                 |             |
| `["collect", "filter-missing"]`          |  96.699 μs (5%) |         | 345.31 KiB (1%) |       10015 |
| `["collect", "identity-float"]`          |  80.499 μs (5%) |         | 569.16 KiB (1%) |       10015 |
| `["collect", "identity-union"]`          | 299.397 μs (5%) |         | 705.58 KiB (1%) |       16694 |
| `["dict", "base"]`                       |   3.938 ms (5%) |         |  92.91 KiB (1%) |          22 |
| `["dict", "xf"]`                         |   4.014 ms (5%) |         |  92.36 KiB (1%) |          21 |
| `["dot", "blas"]`                        |   2.278 μs (5%) |         |                 |             |
| `["dot", "man"]`                         |   2.278 μs (5%) |         |                 |             |
| `["dot", "rf"]`                          |   3.062 μs (5%) |         |                 |             |
| `["dot", "xf"]`                          |   3.138 μs (5%) |         |   64 bytes (1%) |           3 |
| `["filter_map_map!", "man"]`             |  66.900 μs (5%) |         |                 |             |
| `["filter_map_map!", "xf"]`              | 538.006 μs (5%) |         |  304 bytes (1%) |          17 |
| `["filter_map_reduce", "man"]`           | 194.899 μs (5%) |         |                 |             |
| `["filter_map_reduce", "xf"]`            | 194.899 μs (5%) |         |                 |             |
| `["findall", "base"]`                    | 807.595 μs (5%) |         |   2.00 MiB (1%) |          21 |
| `["findall", "xf-array"]`                | 746.696 μs (5%) |         |   3.04 MiB (1%) |       99475 |
| `["findall", "xf-iter"]`                 |   3.003 ms (5%) |         |   9.63 MiB (1%) |      299949 |
| `["gemm", "fusedmul", "blas", "16"]`     |   4.990 ms (5%) |         |                 |             |
| `["gemm", "fusedmul", "blas", "2"]`      |   3.494 ms (5%) |         |                 |             |
| `["gemm", "fusedmul", "blas", "32"]`     |   7.131 ms (5%) |         |                 |             |
| `["gemm", "fusedmul", "blas", "8"]`      |   3.761 ms (5%) |         |                 |             |
| `["gemm", "fusedmul", "xf", "16"]`       |   5.036 ms (5%) |         |  160 bytes (1%) |           6 |
| `["gemm", "fusedmul", "xf", "2"]`        | 605.806 μs (5%) |         |  160 bytes (1%) |           6 |
| `["gemm", "fusedmul", "xf", "32"]`       |  10.272 ms (5%) |         |  160 bytes (1%) |           6 |
| `["gemm", "fusedmul", "xf", "8"]`        |   2.404 ms (5%) |         |  160 bytes (1%) |           6 |
| `["gemm", "mul", "linalg", "256"]`       |   1.210 ms (5%) |         |                 |             |
| `["gemm", "mul", "linalg", "32"]`        |   3.712 μs (5%) |         |                 |             |
| `["gemm", "mul", "linalg", "8"]`         | 290.406 ns (5%) |         |                 |             |
| `["gemm", "mul", "man", "false", "256"]` |   4.261 ms (5%) |         |                 |             |
| `["gemm", "mul", "man", "false", "32"]`  |   6.860 μs (5%) |         |                 |             |
| `["gemm", "mul", "man", "false", "8"]`   | 373.082 ns (5%) |         |                 |             |
| `["gemm", "mul", "man", "ivdep", "256"]` |   4.339 ms (5%) |         |                 |             |
| `["gemm", "mul", "man", "ivdep", "32"]`  |   6.020 μs (5%) |         |                 |             |
| `["gemm", "mul", "man", "ivdep", "8"]`   | 371.850 ns (5%) |         |                 |             |
| `["gemm", "mul", "man", "true", "256"]`  |   4.270 ms (5%) |         |                 |             |
| `["gemm", "mul", "man", "true", "32"]`   |   6.780 μs (5%) |         |                 |             |
| `["gemm", "mul", "man", "true", "8"]`    | 338.914 ns (5%) |         |                 |             |
| `["gemm", "mul", "xf", "false", "256"]`  |   4.255 ms (5%) |         |   48 bytes (1%) |           2 |
| `["gemm", "mul", "xf", "false", "32"]`   |   6.980 μs (5%) |         |   48 bytes (1%) |           2 |
| `["gemm", "mul", "xf", "false", "8"]`    | 388.945 ns (5%) |         |   48 bytes (1%) |           2 |
| `["gemm", "mul", "xf", "ivdep", "256"]`  |   4.221 ms (5%) |         |   48 bytes (1%) |           2 |
| `["gemm", "mul", "xf", "ivdep", "32"]`   |   5.533 μs (5%) |         |   48 bytes (1%) |           2 |
| `["gemm", "mul", "xf", "ivdep", "8"]`    | 362.255 ns (5%) |         |   48 bytes (1%) |           2 |
| `["gemm", "mul", "xf", "true", "256"]`   |   4.311 ms (5%) |         |   48 bytes (1%) |           2 |
| `["gemm", "mul", "xf", "true", "32"]`    |   6.900 μs (5%) |         |   48 bytes (1%) |           2 |
| `["gemm", "mul", "xf", "true", "8"]`     | 374.020 ns (5%) |         |   48 bytes (1%) |           2 |
| `["groupby", "sum", "sac"]`              | 155.302 μs (5%) |         | 157.84 KiB (1%) |       10019 |
| `["groupby", "sum", "xf-with-init"]`     | 155.602 μs (5%) |         | 157.44 KiB (1%) |       10008 |
| `["groupby", "sum", "xf-without-init"]`  | 154.402 μs (5%) |         | 157.44 KiB (1%) |       10008 |
| `["mapcat_eduction", "base"]`            |   1.500 μs (5%) |         |                 |             |
| `["mapcat_eduction", "xf-eduction"]`     |   1.600 μs (5%) |         |                 |             |
| `["mapcat_eduction", "xf-xf"]`           |   1.650 μs (5%) |         |                 |             |
| `["missing_argmax", "man"]`              |   1.010 μs (5%) |         |   32 bytes (1%) |           1 |
| `["missing_argmax", "rf"]`               |   2.278 μs (5%) |         |   32 bytes (1%) |           1 |
| `["missing_argmax", "xf"]`               |   2.278 μs (5%) |         |   32 bytes (1%) |           1 |
| `["missing_dot", "equiv"]`               | 943.590 ns (5%) |         |   16 bytes (1%) |           1 |
| `["missing_dot", "man"]`                 |   1.210 μs (5%) |         |   16 bytes (1%) |           1 |
| `["missing_dot", "naive"]`               |   4.086 μs (5%) |         |   16 bytes (1%) |           1 |
| `["missing_dot", "rf"]`                  | 934.211 ns (5%) |         |   16 bytes (1%) |           1 |
| `["missing_dot", "rf_nota"]`             | 928.261 ns (5%) |         |   16 bytes (1%) |           1 |
| `["missing_dot", "xf"]`                  | 182.000 μs (5%) |         |  72.14 KiB (1%) |        3742 |
| `["missing_dot", "xf_nota"]`             | 187.999 μs (5%) |         |  72.33 KiB (1%) |        3750 |
| `["overhead", "foldl"]`                  |   4.399 ns (5%) |         |                 |             |
| `["overhead", "reduce_basecase"]`        | 264.100 ns (5%) |         |  464 bytes (1%) |           9 |
| `["partition_by", "man"]`                |   1.644 ms (5%) |         |  352 bytes (1%) |           4 |
| `["partition_by", "xf"]`                 |   2.573 ms (5%) |         |   6.10 MiB (1%) |      200007 |
| `["set", "base"]`                        |   4.514 ms (5%) |         |  49.58 KiB (1%) |          18 |
| `["set", "xf"]`                          |   3.934 ms (5%) |         |  49.63 KiB (1%) |          21 |

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
       #1  2294 MHz       8292 s          0 s       1269 s      65808 s          0 s
       #2  2294 MHz      62090 s          0 s       1746 s      11642 s          0 s
       
  Memory: 6.764881134033203 GB (2591.80859375 MB free)
  Uptime: 776.0 sec
  Load Avg:  1.0  0.98974609375  0.671875
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-8.0.1 (ORCJIT, broadwell)
```

---
# Baseline result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmark: 5 Aug 2020 - 0:57
* Package commit: 0e1a4a
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
| `["append!!", "eduction"]`               |  15.800 μs (5%) |         |  64.72 KiB (1%) |          18 |
| `["append!!", "xf"]`                     |  15.400 μs (5%) |         |  64.72 KiB (1%) |          18 |
| `["cat", "base"]`                        |   1.480 μs (5%) |         |                 |             |
| `["cat", "xf"]`                          |   1.690 μs (5%) |         |                 |             |
| `["collect", "filter-missing"]`          |  89.702 μs (5%) |         | 345.31 KiB (1%) |       10015 |
| `["collect", "identity-float"]`          |  71.601 μs (5%) |         | 569.16 KiB (1%) |       10015 |
| `["collect", "identity-union"]`          | 273.104 μs (5%) |         | 704.81 KiB (1%) |       16645 |
| `["dict", "base"]`                       |   3.797 ms (5%) |         |  92.91 KiB (1%) |          22 |
| `["dict", "xf"]`                         |   3.700 ms (5%) |         |  92.36 KiB (1%) |          21 |
| `["dot", "blas"]`                        |   2.256 μs (5%) |         |                 |             |
| `["dot", "man"]`                         |   2.244 μs (5%) |         |                 |             |
| `["dot", "rf"]`                          |   3.063 μs (5%) |         |                 |             |
| `["dot", "xf"]`                          |   3.125 μs (5%) |         |   64 bytes (1%) |           3 |
| `["filter_map_map!", "man"]`             |  67.599 μs (5%) |         |                 |             |
| `["filter_map_map!", "xf"]`              | 539.590 μs (5%) |         |  304 bytes (1%) |          17 |
| `["filter_map_reduce", "man"]`           | 194.903 μs (5%) |         |                 |             |
| `["filter_map_reduce", "xf"]`            | 194.903 μs (5%) |         |                 |             |
| `["findall", "base"]`                    | 778.413 μs (5%) |         |   2.00 MiB (1%) |          21 |
| `["findall", "xf-array"]`                | 705.511 μs (5%) |         |   2.93 MiB (1%) |       95999 |
| `["findall", "xf-iter"]`                 |   2.984 ms (5%) |         |   9.63 MiB (1%) |      299947 |
| `["gemm", "fusedmul", "blas", "16"]`     |   5.041 ms (5%) |         |                 |             |
| `["gemm", "fusedmul", "blas", "2"]`      |   3.495 ms (5%) |         |                 |             |
| `["gemm", "fusedmul", "blas", "32"]`     |   7.306 ms (5%) |         |                 |             |
| `["gemm", "fusedmul", "blas", "8"]`      |   3.813 ms (5%) |         |                 |             |
| `["gemm", "fusedmul", "xf", "16"]`       |   5.592 ms (5%) |         |  160 bytes (1%) |           6 |
| `["gemm", "fusedmul", "xf", "2"]`        | 603.388 μs (5%) |         |  160 bytes (1%) |           6 |
| `["gemm", "fusedmul", "xf", "32"]`       |  10.040 ms (5%) |         |  160 bytes (1%) |           6 |
| `["gemm", "fusedmul", "xf", "8"]`        |   2.480 ms (5%) |         |  160 bytes (1%) |           6 |
| `["gemm", "mul", "linalg", "256"]`       |   1.212 ms (5%) |         |                 |             |
| `["gemm", "mul", "linalg", "32"]`        |   4.100 μs (5%) |         |                 |             |
| `["gemm", "mul", "linalg", "8"]`         | 300.000 ns (5%) |         |                 |             |
| `["gemm", "mul", "man", "false", "256"]` |   4.420 ms (5%) |         |                 |             |
| `["gemm", "mul", "man", "false", "32"]`  |   6.899 μs (5%) |         |                 |             |
| `["gemm", "mul", "man", "false", "8"]`   | 399.000 ns (5%) |         |                 |             |
| `["gemm", "mul", "man", "ivdep", "256"]` |   4.422 ms (5%) |         |                 |             |
| `["gemm", "mul", "man", "ivdep", "32"]`  |   6.099 μs (5%) |         |                 |             |
| `["gemm", "mul", "man", "ivdep", "8"]`   | 300.000 ns (5%) |         |                 |             |
| `["gemm", "mul", "man", "true", "256"]`  |   4.332 ms (5%) |         |                 |             |
| `["gemm", "mul", "man", "true", "32"]`   |   7.699 μs (5%) |         |                 |             |
| `["gemm", "mul", "man", "true", "8"]`    | 399.000 ns (5%) |         |                 |             |
| `["gemm", "mul", "xf", "false", "256"]`  |   4.296 ms (5%) |         |   48 bytes (1%) |           2 |
| `["gemm", "mul", "xf", "false", "32"]`   |   6.999 μs (5%) |         |   48 bytes (1%) |           2 |
| `["gemm", "mul", "xf", "false", "8"]`    | 399.000 ns (5%) |         |   48 bytes (1%) |           2 |
| `["gemm", "mul", "xf", "ivdep", "256"]`  |   4.337 ms (5%) |         |   48 bytes (1%) |           2 |
| `["gemm", "mul", "xf", "ivdep", "32"]`   |   6.099 μs (5%) |         |   48 bytes (1%) |           2 |
| `["gemm", "mul", "xf", "ivdep", "8"]`    | 399.000 ns (5%) |         |   48 bytes (1%) |           2 |
| `["gemm", "mul", "xf", "true", "256"]`   |   4.261 ms (5%) |         |   48 bytes (1%) |           2 |
| `["gemm", "mul", "xf", "true", "32"]`    |   7.000 μs (5%) |         |   48 bytes (1%) |           2 |
| `["gemm", "mul", "xf", "true", "8"]`     | 400.000 ns (5%) |         |   48 bytes (1%) |           2 |
| `["groupby", "sum", "sac"]`              | 207.397 μs (5%) |         | 313.14 KiB (1%) |       10007 |
| `["groupby", "sum", "xf-with-init"]`     | 155.597 μs (5%) |         | 157.44 KiB (1%) |       10008 |
| `["groupby", "sum", "xf-without-init"]`  | 164.297 μs (5%) |         | 157.44 KiB (1%) |       10008 |
| `["mapcat_eduction", "base"]`            |   1.590 μs (5%) |         |                 |             |
| `["mapcat_eduction", "xf-eduction"]`     |   1.610 μs (5%) |         |                 |             |
| `["mapcat_eduction", "xf-xf"]`           |   1.750 μs (5%) |         |                 |             |
| `["missing_argmax", "man"]`              | 915.050 ns (5%) |         |   32 bytes (1%) |           1 |
| `["missing_argmax", "rf"]`               |   2.133 μs (5%) |         |   32 bytes (1%) |           1 |
| `["missing_argmax", "xf"]`               |   2.167 μs (5%) |         |   32 bytes (1%) |           1 |
| `["missing_dot", "equiv"]`               |   1.005 μs (5%) |         |   16 bytes (1%) |           1 |
| `["missing_dot", "man"]`                 |   1.000 μs (5%) |         |   16 bytes (1%) |           1 |
| `["missing_dot", "naive"]`               |   4.071 μs (5%) |         |   16 bytes (1%) |           1 |
| `["missing_dot", "rf"]`                  | 902.658 ns (5%) |         |   16 bytes (1%) |           1 |
| `["missing_dot", "rf_nota"]`             | 943.500 ns (5%) |         |   16 bytes (1%) |           1 |
| `["missing_dot", "xf"]`                  | 188.203 μs (5%) |         |  72.02 KiB (1%) |        3736 |
| `["missing_dot", "xf_nota"]`             | 188.303 μs (5%) |         |  72.02 KiB (1%) |        3736 |
| `["overhead", "foldl"]`                  |   4.100 ns (5%) |         |                 |             |
| `["overhead", "reduce_basecase"]`        | 242.826 ns (5%) |         |  464 bytes (1%) |           9 |
| `["partition_by", "man"]`                |   1.641 ms (5%) |         |  352 bytes (1%) |           4 |
| `["partition_by", "xf"]`                 |   2.543 ms (5%) |         |   6.10 MiB (1%) |      200007 |
| `["set", "base"]`                        |   4.644 ms (5%) |         |  49.58 KiB (1%) |          18 |
| `["set", "xf"]`                          |   4.011 ms (5%) |         |  49.63 KiB (1%) |          21 |

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
       #1  2294 MHz      31965 s          0 s       1608 s      74391 s          0 s
       #2  2294 MHz      70408 s          0 s       2058 s      35604 s          0 s
       
  Memory: 6.764881134033203 GB (2677.5546875 MB free)
  Uptime: 1103.0 sec
  Load Avg:  1.0  1.0  0.78125
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
    CPU MHz:             2294.685
    BogoMIPS:            4589.37
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

