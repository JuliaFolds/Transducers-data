# Benchmark result

* Pull request commit: [`c704e2d45ba3ee4e3ead60fc11c5da147d7cb75e`](https://github.com/JuliaFolds/Transducers.jl/commit/c704e2d45ba3ee4e3ead60fc11c5da147d7cb75e)
* Pull request: <https://github.com/JuliaFolds/Transducers.jl/pull/397> (Define collect(::Foldable) rather than collect(::Eduction))

# Judge result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmarks:
    - Target: 6 Aug 2020 - 15:29
    - Baseline: 6 Aug 2020 - 15:34
* Package commits:
    - Target: 9b885b
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

| ID                                       | time ratio                   | memory ratio |
|------------------------------------------|------------------------------|--------------|
| `["cat", "base"]`                        | 0.92 (5%) :white_check_mark: |   1.00 (1%)  |
| `["collect", "filter-missing"]`          |                1.11 (5%) :x: |   1.00 (1%)  |
| `["collect", "identity-float"]`          |                1.06 (5%) :x: |   1.00 (1%)  |
| `["dot", "rf"]`                          | 0.88 (5%) :white_check_mark: |   1.00 (1%)  |
| `["dot", "xf"]`                          |                1.14 (5%) :x: |   1.00 (1%)  |
| `["gemm", "fusedmul", "blas", "8"]`      |                1.08 (5%) :x: |   1.00 (1%)  |
| `["gemm", "fusedmul", "xf", "16"]`       | 0.89 (5%) :white_check_mark: |   1.00 (1%)  |
| `["gemm", "fusedmul", "xf", "2"]`        | 0.84 (5%) :white_check_mark: |   1.00 (1%)  |
| `["gemm", "fusedmul", "xf", "32"]`       |                1.12 (5%) :x: |   1.00 (1%)  |
| `["gemm", "mul", "linalg", "32"]`        | 0.86 (5%) :white_check_mark: |   1.00 (1%)  |
| `["gemm", "mul", "linalg", "8"]`         | 0.92 (5%) :white_check_mark: |   1.00 (1%)  |
| `["gemm", "mul", "man", "false", "32"]`  |                1.05 (5%) :x: |   1.00 (1%)  |
| `["gemm", "mul", "man", "false", "8"]`   |                1.06 (5%) :x: |   1.00 (1%)  |
| `["gemm", "mul", "man", "ivdep", "8"]`   |                1.07 (5%) :x: |   1.00 (1%)  |
| `["gemm", "mul", "man", "true", "32"]`   | 0.87 (5%) :white_check_mark: |   1.00 (1%)  |
| `["gemm", "mul", "man", "true", "8"]`    |                1.21 (5%) :x: |   1.00 (1%)  |
| `["gemm", "mul", "xf", "false", "32"]`   | 0.91 (5%) :white_check_mark: |   1.00 (1%)  |
| `["gemm", "mul", "xf", "false", "8"]`    |                1.05 (5%) :x: |   1.00 (1%)  |
| `["gemm", "mul", "xf", "ivdep", "8"]`    |                1.17 (5%) :x: |   1.00 (1%)  |
| `["gemm", "mul", "xf", "true", "256"]`   |                1.06 (5%) :x: |   1.00 (1%)  |
| `["gemm", "mul", "xf", "true", "32"]`    | 0.94 (5%) :white_check_mark: |   1.00 (1%)  |
| `["gemm", "mul", "xf", "true", "8"]`     |                1.05 (5%) :x: |   1.00 (1%)  |
| `["groupby", "sum", "sac"]`              |                1.10 (5%) :x: |   1.00 (1%)  |
| `["groupby", "sum", "xf-with-init"]`     | 0.89 (5%) :white_check_mark: |   1.00 (1%)  |
| `["groupby", "sum", "xf-without-init"]`  | 0.90 (5%) :white_check_mark: |   1.00 (1%)  |
| `["mapcat_eduction", "xf-eduction"]`     |                1.15 (5%) :x: |   1.00 (1%)  |
| `["mapcat_eduction", "xf-xf"]`           | 0.93 (5%) :white_check_mark: |   1.00 (1%)  |
| `["missing_argmax", "rf"]`               | 0.89 (5%) :white_check_mark: |   1.00 (1%)  |
| `["missing_dot", "rf_nota"]`             |                1.30 (5%) :x: |   1.00 (1%)  |
| `["missing_dot", "xf"]`                  |                1.18 (5%) :x: |   1.00 (1%)  |
| `["missing_dot", "xf_nota"]`             | 0.91 (5%) :white_check_mark: |   1.00 (1%)  |
| `["overhead", "foldl"]`                  | 0.92 (5%) :white_check_mark: |   1.00 (1%)  |
| `["overhead", "reduce_basecase"]`        |                1.07 (5%) :x: |   1.00 (1%)  |

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
       #1  2095 MHz       7154 s          0 s       1291 s      63006 s          0 s
       #2  2095 MHz      61830 s          0 s       2056 s       8640 s          0 s
       
  Memory: 6.764873504638672 GB (2795.0703125 MB free)
  Uptime: 741.0 sec
  Load Avg:  1.11962890625  1.05517578125  0.71923828125
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
       #1  2095 MHz       9740 s          0 s       1387 s      89105 s          0 s
       #2  2095 MHz      87938 s          0 s       2177 s      11163 s          0 s
       
  Memory: 6.764873504638672 GB (2692.39453125 MB free)
  Uptime: 1030.0 sec
  Load Avg:  1.0  1.013671875  0.806640625
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-8.0.1 (ORCJIT, skylake)
```

---
# Target result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmark: 6 Aug 2020 - 15:29
* Package commit: 9b885b
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
| `["append!!", "eduction"]`               |  21.302 μs (5%) |         |  64.72 KiB (1%) |          18 |
| `["append!!", "xf"]`                     |  20.702 μs (5%) |         |  64.72 KiB (1%) |          18 |
| `["cat", "base"]`                        |   1.920 μs (5%) |         |                 |             |
| `["cat", "xf"]`                          |   2.200 μs (5%) |         |                 |             |
| `["collect", "filter-missing"]`          | 121.208 μs (5%) |         | 345.31 KiB (1%) |       10015 |
| `["collect", "identity-float"]`          |  90.207 μs (5%) |         | 569.16 KiB (1%) |       10015 |
| `["collect", "identity-union"]`          | 338.825 μs (5%) |         | 705.23 KiB (1%) |       16674 |
| `["dict", "base"]`                       |   4.523 ms (5%) |         |  92.91 KiB (1%) |          22 |
| `["dict", "xf"]`                         |   4.826 ms (5%) |         |  92.36 KiB (1%) |          21 |
| `["dot", "blas"]`                        |   1.350 μs (5%) |         |                 |             |
| `["dot", "man"]`                         |   1.300 μs (5%) |         |                 |             |
| `["dot", "rf"]`                          |   2.134 μs (5%) |         |                 |             |
| `["dot", "xf"]`                          |   2.500 μs (5%) |         |   64 bytes (1%) |           3 |
| `["filter_map_map!", "man"]`             |  60.502 μs (5%) |         |                 |             |
| `["filter_map_map!", "xf"]`              | 756.934 μs (5%) |         |  304 bytes (1%) |          17 |
| `["filter_map_reduce", "man"]`           | 255.816 μs (5%) |         |                 |             |
| `["filter_map_reduce", "xf"]`            | 255.917 μs (5%) |         |                 |             |
| `["findall", "base"]`                    | 920.164 μs (5%) |         |   2.00 MiB (1%) |          21 |
| `["findall", "xf-array"]`                | 903.161 μs (5%) |         |   3.04 MiB (1%) |       99401 |
| `["findall", "xf-iter"]`                 | 973.764 μs (5%) |         |   5.05 MiB (1%) |       99921 |
| `["gemm", "fusedmul", "blas", "16"]`     |   5.206 ms (5%) |         |                 |             |
| `["gemm", "fusedmul", "blas", "2"]`      |   3.798 ms (5%) |         |                 |             |
| `["gemm", "fusedmul", "blas", "32"]`     |   7.210 ms (5%) |         |                 |             |
| `["gemm", "fusedmul", "blas", "8"]`      |   4.160 ms (5%) |         |                 |             |
| `["gemm", "fusedmul", "xf", "16"]`       |   4.479 ms (5%) |         |  160 bytes (1%) |           6 |
| `["gemm", "fusedmul", "xf", "2"]`        | 521.024 μs (5%) |         |  160 bytes (1%) |           6 |
| `["gemm", "fusedmul", "xf", "32"]`       |   9.258 ms (5%) |         |  160 bytes (1%) |           6 |
| `["gemm", "fusedmul", "xf", "8"]`        |   2.193 ms (5%) |         |  160 bytes (1%) |           6 |
| `["gemm", "mul", "linalg", "256"]`       | 969.757 μs (5%) |         |                 |             |
| `["gemm", "mul", "linalg", "32"]`        |   2.925 μs (5%) |         |                 |             |
| `["gemm", "mul", "linalg", "8"]`         | 275.429 ns (5%) |         |                 |             |
| `["gemm", "mul", "man", "false", "256"]` |   1.800 ms (5%) |         |                 |             |
| `["gemm", "mul", "man", "false", "32"]`  |   4.743 μs (5%) |         |                 |             |
| `["gemm", "mul", "man", "false", "8"]`   | 424.643 ns (5%) |         |                 |             |
| `["gemm", "mul", "man", "ivdep", "256"]` |   1.780 ms (5%) |         |                 |             |
| `["gemm", "mul", "man", "ivdep", "32"]`  |   4.215 μs (5%) |         |                 |             |
| `["gemm", "mul", "man", "ivdep", "8"]`   | 426.111 ns (5%) |         |                 |             |
| `["gemm", "mul", "man", "true", "256"]`  |   1.788 ms (5%) |         |                 |             |
| `["gemm", "mul", "man", "true", "32"]`   |   4.886 μs (5%) |         |                 |             |
| `["gemm", "mul", "man", "true", "8"]`    | 485.154 ns (5%) |         |                 |             |
| `["gemm", "mul", "xf", "false", "256"]`  |   1.809 ms (5%) |         |   48 bytes (1%) |           2 |
| `["gemm", "mul", "xf", "false", "32"]`   |   4.757 μs (5%) |         |   48 bytes (1%) |           2 |
| `["gemm", "mul", "xf", "false", "8"]`    | 420.126 ns (5%) |         |   48 bytes (1%) |           2 |
| `["gemm", "mul", "xf", "ivdep", "256"]`  |   1.789 ms (5%) |         |   48 bytes (1%) |           2 |
| `["gemm", "mul", "xf", "ivdep", "32"]`   |   4.072 μs (5%) |         |   48 bytes (1%) |           2 |
| `["gemm", "mul", "xf", "ivdep", "8"]`    | 469.413 ns (5%) |         |   48 bytes (1%) |           2 |
| `["gemm", "mul", "xf", "true", "256"]`   |   1.866 ms (5%) |         |   48 bytes (1%) |           2 |
| `["gemm", "mul", "xf", "true", "32"]`    |   5.000 μs (5%) |         |   48 bytes (1%) |           2 |
| `["gemm", "mul", "xf", "true", "8"]`     | 420.628 ns (5%) |         |   48 bytes (1%) |           2 |
| `["groupby", "sum", "sac"]`              | 282.913 μs (5%) |         | 313.14 KiB (1%) |       10007 |
| `["groupby", "sum", "xf-with-init"]`     | 179.807 μs (5%) |         | 157.44 KiB (1%) |       10008 |
| `["groupby", "sum", "xf-without-init"]`  | 182.608 μs (5%) |         | 157.44 KiB (1%) |       10008 |
| `["mapcat_eduction", "base"]`            |   2.100 μs (5%) |         |                 |             |
| `["mapcat_eduction", "xf-eduction"]`     |   2.133 μs (5%) |         |                 |             |
| `["mapcat_eduction", "xf-xf"]`           |   2.133 μs (5%) |         |                 |             |
| `["missing_argmax", "man"]`              |   2.978 μs (5%) |         |   32 bytes (1%) |           1 |
| `["missing_argmax", "rf"]`               |   2.500 μs (5%) |         |   32 bytes (1%) |           1 |
| `["missing_argmax", "xf"]`               |   2.889 μs (5%) |         |   32 bytes (1%) |           1 |
| `["missing_dot", "equiv"]`               |   1.630 μs (5%) |         |   16 bytes (1%) |           1 |
| `["missing_dot", "man"]`                 |   1.520 μs (5%) |         |   16 bytes (1%) |           1 |
| `["missing_dot", "naive"]`               |   5.284 μs (5%) |         |   16 bytes (1%) |           1 |
| `["missing_dot", "rf"]`                  |   1.530 μs (5%) |         |   16 bytes (1%) |           1 |
| `["missing_dot", "rf_nota"]`             |   1.680 μs (5%) |         |   16 bytes (1%) |           1 |
| `["missing_dot", "xf"]`                  | 206.613 μs (5%) |         |  72.31 KiB (1%) |        3750 |
| `["missing_dot", "xf_nota"]`             | 207.513 μs (5%) |         |  72.13 KiB (1%) |        3741 |
| `["overhead", "foldl"]`                  |   4.800 ns (5%) |         |                 |             |
| `["overhead", "reduce_basecase"]`        | 300.798 ns (5%) |         |  464 bytes (1%) |           9 |
| `["partition_by", "man"]`                |   2.315 ms (5%) |         |  352 bytes (1%) |           4 |
| `["partition_by", "xf"]`                 |   3.428 ms (5%) |         |   6.10 MiB (1%) |      200007 |
| `["set", "base"]`                        |   5.408 ms (5%) |         |  49.58 KiB (1%) |          18 |
| `["set", "xf"]`                          |   5.241 ms (5%) |         |  49.63 KiB (1%) |          21 |

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
       #1  2095 MHz       7154 s          0 s       1291 s      63006 s          0 s
       #2  2095 MHz      61830 s          0 s       2056 s       8640 s          0 s
       
  Memory: 6.764873504638672 GB (2795.0703125 MB free)
  Uptime: 741.0 sec
  Load Avg:  1.11962890625  1.05517578125  0.71923828125
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-8.0.1 (ORCJIT, skylake)
```

---
# Baseline result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmark: 6 Aug 2020 - 15:34
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
| `["append!!", "eduction"]`               |  20.701 μs (5%) |         |  64.72 KiB (1%) |          18 |
| `["append!!", "xf"]`                     |  20.900 μs (5%) |         |  64.72 KiB (1%) |          18 |
| `["cat", "base"]`                        |   2.090 μs (5%) |         |                 |             |
| `["cat", "xf"]`                          |   2.200 μs (5%) |         |                 |             |
| `["collect", "filter-missing"]`          | 108.804 μs (5%) |         | 345.31 KiB (1%) |       10015 |
| `["collect", "identity-float"]`          |  85.504 μs (5%) |         | 569.16 KiB (1%) |       10015 |
| `["collect", "identity-union"]`          | 348.413 μs (5%) |         | 705.30 KiB (1%) |       16674 |
| `["dict", "base"]`                       |   4.681 ms (5%) |         |  92.91 KiB (1%) |          22 |
| `["dict", "xf"]`                         |   4.739 ms (5%) |         |  92.36 KiB (1%) |          21 |
| `["dot", "blas"]`                        |   1.370 μs (5%) |         |                 |             |
| `["dot", "man"]`                         |   1.350 μs (5%) |         |                 |             |
| `["dot", "rf"]`                          |   2.411 μs (5%) |         |                 |             |
| `["dot", "xf"]`                          |   2.200 μs (5%) |         |   64 bytes (1%) |           3 |
| `["filter_map_map!", "man"]`             |  61.006 μs (5%) |         |                 |             |
| `["filter_map_map!", "xf"]`              | 756.781 μs (5%) |         |  304 bytes (1%) |          17 |
| `["filter_map_reduce", "man"]`           | 254.610 μs (5%) |         |                 |             |
| `["filter_map_reduce", "xf"]`            | 256.209 μs (5%) |         |                 |             |
| `["findall", "base"]`                    | 915.934 μs (5%) |         |   2.00 MiB (1%) |          21 |
| `["findall", "xf-array"]`                | 889.033 μs (5%) |         |   3.03 MiB (1%) |       99052 |
| `["findall", "xf-iter"]`                 | 965.036 μs (5%) |         |   5.05 MiB (1%) |       99906 |
| `["gemm", "fusedmul", "blas", "16"]`     |   5.023 ms (5%) |         |                 |             |
| `["gemm", "fusedmul", "blas", "2"]`      |   3.667 ms (5%) |         |                 |             |
| `["gemm", "fusedmul", "blas", "32"]`     |   6.984 ms (5%) |         |                 |             |
| `["gemm", "fusedmul", "blas", "8"]`      |   3.853 ms (5%) |         |                 |             |
| `["gemm", "fusedmul", "xf", "16"]`       |   5.049 ms (5%) |         |  160 bytes (1%) |           6 |
| `["gemm", "fusedmul", "xf", "2"]`        | 619.271 μs (5%) |         |  160 bytes (1%) |           6 |
| `["gemm", "fusedmul", "xf", "32"]`       |   8.231 ms (5%) |         |  160 bytes (1%) |           6 |
| `["gemm", "fusedmul", "xf", "8"]`        |   2.264 ms (5%) |         |  160 bytes (1%) |           6 |
| `["gemm", "mul", "linalg", "256"]`       | 978.335 μs (5%) |         |                 |             |
| `["gemm", "mul", "linalg", "32"]`        |   3.400 μs (5%) |         |                 |             |
| `["gemm", "mul", "linalg", "8"]`         | 300.000 ns (5%) |         |                 |             |
| `["gemm", "mul", "man", "false", "256"]` |   1.892 ms (5%) |         |                 |             |
| `["gemm", "mul", "man", "false", "32"]`  |   4.500 μs (5%) |         |                 |             |
| `["gemm", "mul", "man", "false", "8"]`   | 400.000 ns (5%) |         |                 |             |
| `["gemm", "mul", "man", "ivdep", "256"]` |   1.836 ms (5%) |         |                 |             |
| `["gemm", "mul", "man", "ivdep", "32"]`  |   4.300 μs (5%) |         |                 |             |
| `["gemm", "mul", "man", "ivdep", "8"]`   | 400.000 ns (5%) |         |                 |             |
| `["gemm", "mul", "man", "true", "256"]`  |   1.847 ms (5%) |         |                 |             |
| `["gemm", "mul", "man", "true", "32"]`   |   5.600 μs (5%) |         |                 |             |
| `["gemm", "mul", "man", "true", "8"]`    | 400.000 ns (5%) |         |                 |             |
| `["gemm", "mul", "xf", "false", "256"]`  |   1.884 ms (5%) |         |   48 bytes (1%) |           2 |
| `["gemm", "mul", "xf", "false", "32"]`   |   5.200 μs (5%) |         |   48 bytes (1%) |           2 |
| `["gemm", "mul", "xf", "false", "8"]`    | 400.000 ns (5%) |         |   48 bytes (1%) |           2 |
| `["gemm", "mul", "xf", "ivdep", "256"]`  |   1.760 ms (5%) |         |   48 bytes (1%) |           2 |
| `["gemm", "mul", "xf", "ivdep", "32"]`   |   4.100 μs (5%) |         |   48 bytes (1%) |           2 |
| `["gemm", "mul", "xf", "ivdep", "8"]`    | 400.000 ns (5%) |         |   48 bytes (1%) |           2 |
| `["gemm", "mul", "xf", "true", "256"]`   |   1.757 ms (5%) |         |   48 bytes (1%) |           2 |
| `["gemm", "mul", "xf", "true", "32"]`    |   5.300 μs (5%) |         |   48 bytes (1%) |           2 |
| `["gemm", "mul", "xf", "true", "8"]`     | 400.000 ns (5%) |         |   48 bytes (1%) |           2 |
| `["groupby", "sum", "sac"]`              | 257.127 μs (5%) |         | 313.14 KiB (1%) |       10007 |
| `["groupby", "sum", "xf-with-init"]`     | 203.021 μs (5%) |         | 157.44 KiB (1%) |       10008 |
| `["groupby", "sum", "xf-without-init"]`  | 202.621 μs (5%) |         | 157.44 KiB (1%) |       10008 |
| `["mapcat_eduction", "base"]`            |   2.089 μs (5%) |         |                 |             |
| `["mapcat_eduction", "xf-eduction"]`     |   1.856 μs (5%) |         |                 |             |
| `["mapcat_eduction", "xf-xf"]`           |   2.300 μs (5%) |         |                 |             |
| `["missing_argmax", "man"]`              |   2.978 μs (5%) |         |   32 bytes (1%) |           1 |
| `["missing_argmax", "rf"]`               |   2.800 μs (5%) |         |   32 bytes (1%) |           1 |
| `["missing_argmax", "xf"]`               |   2.811 μs (5%) |         |   32 bytes (1%) |           1 |
| `["missing_dot", "equiv"]`               |   1.600 μs (5%) |         |   16 bytes (1%) |           1 |
| `["missing_dot", "man"]`                 |   1.510 μs (5%) |         |   16 bytes (1%) |           1 |
| `["missing_dot", "naive"]`               |   5.267 μs (5%) |         |   16 bytes (1%) |           1 |
| `["missing_dot", "rf"]`                  |   1.490 μs (5%) |         |   16 bytes (1%) |           1 |
| `["missing_dot", "rf_nota"]`             |   1.290 μs (5%) |         |   16 bytes (1%) |           1 |
| `["missing_dot", "xf"]`                  | 174.806 μs (5%) |         |  72.28 KiB (1%) |        3748 |
| `["missing_dot", "xf_nota"]`             | 226.809 μs (5%) |         |  72.20 KiB (1%) |        3746 |
| `["overhead", "foldl"]`                  |   5.200 ns (5%) |         |                 |             |
| `["overhead", "reduce_basecase"]`        | 279.857 ns (5%) |         |  464 bytes (1%) |           9 |
| `["partition_by", "man"]`                |   2.259 ms (5%) |         |  352 bytes (1%) |           4 |
| `["partition_by", "xf"]`                 |   3.448 ms (5%) |         |   6.10 MiB (1%) |      200007 |
| `["set", "base"]`                        |   5.581 ms (5%) |         |  49.58 KiB (1%) |          18 |
| `["set", "xf"]`                          |   5.206 ms (5%) |         |  49.63 KiB (1%) |          21 |

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
       #1  2095 MHz       9740 s          0 s       1387 s      89105 s          0 s
       #2  2095 MHz      87938 s          0 s       2177 s      11163 s          0 s
       
  Memory: 6.764873504638672 GB (2692.39453125 MB free)
  Uptime: 1030.0 sec
  Load Avg:  1.0  1.013671875  0.806640625
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
    CPU MHz:             2095.227
    BogoMIPS:            4190.45
    Hypervisor vendor:   Microsoft
    Virtualization type: full
    L1d cache:           32K
    L1i cache:           32K
    L2 cache:            1024K
    L3 cache:            36608K
    NUMA node0 CPU(s):   0,1
    Flags:               fpu vme de pse tsc msr pae mce cx8 apic sep mtrr pge mca cmov pat pse36 clflush mmx fxsr sse sse2 ss ht syscall nx pdpe1gb rdtscp lm constant_tsc rep_good nopl xtopology cpuid pni pclmulqdq ssse3 fma cx16 pcid sse4_1 sse4_2 movbe popcnt aes xsave avx f16c rdrand hypervisor lahf_lm abm 3dnowprefetch invpcid_single pti fsgsbase bmi1 hle avx2 smep bmi2 erms invpcid rtm mpx avx512f avx512dq rdseed adx smap clflushopt avx512cd avx512bw avx512vl xsaveopt xsavec xsaves
    

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

