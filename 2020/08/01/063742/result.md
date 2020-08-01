# Benchmark result (via Travis)


# Judge result
# Benchmark Report for */home/travis/build/JuliaFolds/Transducers.jl*

## Job Properties
* Time of benchmarks:
    - Target: 1 Aug 2020 - 06:32
    - Baseline: 1 Aug 2020 - 06:36
* Package commits:
    - Target: f03c59
    - Baseline: d1995c
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
| `["append!!", "eduction"]`               |                1.08 (5%) :x: |    1.00 (1%)  |
| `["append!!", "xf"]`                     |                1.07 (5%) :x: |    1.00 (1%)  |
| `["cat", "xf"]`                          |                1.19 (5%) :x: |    1.00 (1%)  |
| `["collect", "identity-float"]`          |                1.18 (5%) :x: |    1.00 (1%)  |
| `["collect", "identity-union"]`          |                1.06 (5%) :x: |    1.00 (1%)  |
| `["dot", "man"]`                         | 0.95 (5%) :white_check_mark: |    1.00 (1%)  |
| `["filter_map_map!", "xf"]`              | 0.94 (5%) :white_check_mark: |    1.00 (1%)  |
| `["findall", "xf-iter"]`                 |                1.06 (5%) :x: |    1.00 (1%)  |
| `["gemm", "fusedmul", "blas", "8"]`      |                1.05 (5%) :x: |    1.00 (1%)  |
| `["gemm", "fusedmul", "xf", "16"]`       | 0.91 (5%) :white_check_mark: |    1.00 (1%)  |
| `["gemm", "fusedmul", "xf", "2"]`        |                1.11 (5%) :x: |    1.00 (1%)  |
| `["gemm", "fusedmul", "xf", "32"]`       |                1.06 (5%) :x: |    1.00 (1%)  |
| `["gemm", "mul", "linalg", "8"]`         | 0.86 (5%) :white_check_mark: |    1.00 (1%)  |
| `["gemm", "mul", "man", "false", "32"]`  |                1.06 (5%) :x: |    1.00 (1%)  |
| `["gemm", "mul", "man", "false", "8"]`   |                1.24 (5%) :x: |    1.00 (1%)  |
| `["gemm", "mul", "man", "ivdep", "32"]`  |                1.10 (5%) :x: |    1.00 (1%)  |
| `["gemm", "mul", "man", "ivdep", "8"]`   | 0.93 (5%) :white_check_mark: |    1.00 (1%)  |
| `["gemm", "mul", "man", "true", "32"]`   |                1.06 (5%) :x: |    1.00 (1%)  |
| `["gemm", "mul", "man", "true", "8"]`    | 0.94 (5%) :white_check_mark: |    1.00 (1%)  |
| `["gemm", "mul", "xf", "false", "8"]`    |                1.20 (5%) :x: |    1.00 (1%)  |
| `["gemm", "mul", "xf", "ivdep", "8"]`    |                1.22 (5%) :x: |    1.00 (1%)  |
| `["gemm", "mul", "xf", "true", "32"]`    |                1.23 (5%) :x: |    1.00 (1%)  |
| `["gemm", "mul", "xf", "true", "8"]`     |                1.28 (5%) :x: |    1.00 (1%)  |
| `["groupby", "sum", "xf-with-init"]`     |                1.07 (5%) :x: |    1.00 (1%)  |
| `["mapcat_eduction", "xf-eduction"]`     |                1.06 (5%) :x: |    1.00 (1%)  |
| `["missing_argmax", "rf"]`               | 0.82 (5%) :white_check_mark: |    1.00 (1%)  |
| `["missing_argmax", "xf"]`               |                1.24 (5%) :x: |    1.00 (1%)  |
| `["overhead", "foldl"]`                  | 0.88 (5%) :white_check_mark: |    1.00 (1%)  |
| `["overhead", "reduce_basecase"]`        |                1.49 (5%) :x: | 1.12 (1%) :x: |

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
       #1  2800 MHz       9314 s          0 s       1229 s      52605 s          0 s
       #2  2800 MHz      54106 s          0 s       1232 s      10481 s          0 s
       
  Memory: 7.790031433105469 GB (5502.90234375 MB free)
  Uptime: 662.0 sec
  Load Avg:  1.0  0.9453125  0.5673828125
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
       #1  2800 MHz      17853 s          0 s       1316 s      69986 s          0 s
       #2  2800 MHz      71471 s          0 s       1412 s      18953 s          0 s
       
  Memory: 7.790031433105469 GB (5458.16796875 MB free)
  Uptime: 922.0 sec
  Load Avg:  1.42138671875  1.103515625  0.72607421875
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-8.0.1 (ORCJIT, skylake)
```

---
# Target result
# Benchmark Report for */home/travis/build/JuliaFolds/Transducers.jl*

## Job Properties
* Time of benchmark: 1 Aug 2020 - 6:32
* Package commit: f03c59
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
| `["append!!", "eduction"]`               |  18.402 μs (5%) |         |  64.72 KiB (1%) |          18 |
| `["append!!", "xf"]`                     |  18.105 μs (5%) |         |  64.72 KiB (1%) |          18 |
| `["cat", "base"]`                        |   1.634 μs (5%) |         |                 |             |
| `["cat", "xf"]`                          |   2.075 μs (5%) |         |                 |             |
| `["collect", "filter-missing"]`          |  98.382 μs (5%) |         | 345.31 KiB (1%) |       10015 |
| `["collect", "identity-float"]`          |  82.627 μs (5%) |         | 569.16 KiB (1%) |       10015 |
| `["collect", "identity-union"]`          | 297.566 μs (5%) |         | 705.14 KiB (1%) |       16666 |
| `["dict", "base"]`                       |   3.612 ms (5%) |         |  92.91 KiB (1%) |          22 |
| `["dict", "xf"]`                         |   3.708 ms (5%) |         |  92.36 KiB (1%) |          21 |
| `["dot", "blas"]`                        |   1.221 μs (5%) |         |                 |             |
| `["dot", "man"]`                         |   1.146 μs (5%) |         |                 |             |
| `["dot", "rf"]`                          |   2.166 μs (5%) |         |                 |             |
| `["dot", "xf"]`                          |   2.275 μs (5%) |         |   64 bytes (1%) |           3 |
| `["filter_map_map!", "man"]`             |  73.414 μs (5%) |         |                 |             |
| `["filter_map_map!", "xf"]`              | 625.540 μs (5%) |         |  304 bytes (1%) |          17 |
| `["filter_map_reduce", "man"]`           | 202.590 μs (5%) |         |                 |             |
| `["filter_map_reduce", "xf"]`            | 202.604 μs (5%) |         |                 |             |
| `["findall", "base"]`                    | 767.300 μs (5%) |         |   2.00 MiB (1%) |          21 |
| `["findall", "xf-array"]`                | 724.029 μs (5%) |         |   3.03 MiB (1%) |       99140 |
| `["findall", "xf-iter"]`                 |   3.147 ms (5%) |         |   9.63 MiB (1%) |      299924 |
| `["gemm", "fusedmul", "blas", "16"]`     |   4.683 ms (5%) |         |                 |             |
| `["gemm", "fusedmul", "blas", "2"]`      |   3.403 ms (5%) |         |                 |             |
| `["gemm", "fusedmul", "blas", "32"]`     |   6.747 ms (5%) |         |                 |             |
| `["gemm", "fusedmul", "blas", "8"]`      |   3.808 ms (5%) |         |                 |             |
| `["gemm", "fusedmul", "xf", "16"]`       |   4.382 ms (5%) |         |  160 bytes (1%) |           6 |
| `["gemm", "fusedmul", "xf", "2"]`        | 627.865 μs (5%) |         |  160 bytes (1%) |           6 |
| `["gemm", "fusedmul", "xf", "32"]`       |   8.710 ms (5%) |         |  160 bytes (1%) |           6 |
| `["gemm", "fusedmul", "xf", "8"]`        |   2.378 ms (5%) |         |  160 bytes (1%) |           6 |
| `["gemm", "mul", "linalg", "256"]`       | 951.263 μs (5%) |         |                 |             |
| `["gemm", "mul", "linalg", "32"]`        |   3.332 μs (5%) |         |                 |             |
| `["gemm", "mul", "linalg", "8"]`         | 250.290 ns (5%) |         |                 |             |
| `["gemm", "mul", "man", "false", "256"]` |   2.051 ms (5%) |         |                 |             |
| `["gemm", "mul", "man", "false", "32"]`  |   5.287 μs (5%) |         |                 |             |
| `["gemm", "mul", "man", "false", "8"]`   | 512.406 ns (5%) |         |                 |             |
| `["gemm", "mul", "man", "ivdep", "256"]` |   2.034 ms (5%) |         |                 |             |
| `["gemm", "mul", "man", "ivdep", "32"]`  |   4.759 μs (5%) |         |                 |             |
| `["gemm", "mul", "man", "ivdep", "8"]`   | 399.342 ns (5%) |         |                 |             |
| `["gemm", "mul", "man", "true", "256"]`  |   2.041 ms (5%) |         |                 |             |
| `["gemm", "mul", "man", "true", "32"]`   |   5.453 μs (5%) |         |                 |             |
| `["gemm", "mul", "man", "true", "8"]`    | 412.830 ns (5%) |         |                 |             |
| `["gemm", "mul", "xf", "false", "256"]`  |   2.057 ms (5%) |         |   48 bytes (1%) |           2 |
| `["gemm", "mul", "xf", "false", "32"]`   |   4.613 μs (5%) |         |   48 bytes (1%) |           2 |
| `["gemm", "mul", "xf", "false", "8"]`    | 464.744 ns (5%) |         |   48 bytes (1%) |           2 |
| `["gemm", "mul", "xf", "ivdep", "256"]`  |   2.030 ms (5%) |         |   48 bytes (1%) |           2 |
| `["gemm", "mul", "xf", "ivdep", "32"]`   |   4.670 μs (5%) |         |   48 bytes (1%) |           2 |
| `["gemm", "mul", "xf", "ivdep", "8"]`    | 458.751 ns (5%) |         |   48 bytes (1%) |           2 |
| `["gemm", "mul", "xf", "true", "256"]`   |   2.042 ms (5%) |         |   48 bytes (1%) |           2 |
| `["gemm", "mul", "xf", "true", "32"]`    |   6.010 μs (5%) |         |   48 bytes (1%) |           2 |
| `["gemm", "mul", "xf", "true", "8"]`     | 499.396 ns (5%) |         |   48 bytes (1%) |           2 |
| `["groupby", "sum", "sac"]`              | 225.309 μs (5%) |         | 313.14 KiB (1%) |       10007 |
| `["groupby", "sum", "xf-with-init"]`     | 173.567 μs (5%) |         | 157.44 KiB (1%) |       10008 |
| `["groupby", "sum", "xf-without-init"]`  | 168.779 μs (5%) |         | 157.44 KiB (1%) |       10008 |
| `["mapcat_eduction", "base"]`            |   1.927 μs (5%) |         |                 |             |
| `["mapcat_eduction", "xf-eduction"]`     |   1.782 μs (5%) |         |                 |             |
| `["mapcat_eduction", "xf-xf"]`           |   1.689 μs (5%) |         |                 |             |
| `["missing_argmax", "man"]`              |   2.368 μs (5%) |         |   32 bytes (1%) |           1 |
| `["missing_argmax", "rf"]`               |   2.319 μs (5%) |         |   32 bytes (1%) |           1 |
| `["missing_argmax", "xf"]`               |   2.835 μs (5%) |         |   32 bytes (1%) |           1 |
| `["missing_dot", "equiv"]`               |   1.537 μs (5%) |         |   16 bytes (1%) |           1 |
| `["missing_dot", "man"]`                 |   1.361 μs (5%) |         |   16 bytes (1%) |           1 |
| `["missing_dot", "naive"]`               |   4.322 μs (5%) |         |   16 bytes (1%) |           1 |
| `["missing_dot", "rf"]`                  |   1.249 μs (5%) |         |   16 bytes (1%) |           1 |
| `["missing_dot", "rf_nota"]`             |   1.554 μs (5%) |         |   16 bytes (1%) |           1 |
| `["missing_dot", "xf"]`                  | 187.545 μs (5%) |         |  71.83 KiB (1%) |        3730 |
| `["missing_dot", "xf_nota"]`             | 187.605 μs (5%) |         |  72.14 KiB (1%) |        3742 |
| `["overhead", "foldl"]`                  |   4.151 ns (5%) |         |                 |             |
| `["overhead", "reduce_basecase"]`        | 239.867 ns (5%) |         |  464 bytes (1%) |           9 |
| `["partition_by", "man"]`                |   1.831 ms (5%) |         |  352 bytes (1%) |           4 |
| `["partition_by", "xf"]`                 |   2.767 ms (5%) |         |   6.10 MiB (1%) |      200007 |
| `["set", "base"]`                        |   4.330 ms (5%) |         |  49.58 KiB (1%) |          18 |
| `["set", "xf"]`                          |   3.992 ms (5%) |         |  49.63 KiB (1%) |          21 |

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
       #1  2800 MHz       9314 s          0 s       1229 s      52605 s          0 s
       #2  2800 MHz      54106 s          0 s       1232 s      10481 s          0 s
       
  Memory: 7.790031433105469 GB (5502.90234375 MB free)
  Uptime: 662.0 sec
  Load Avg:  1.0  0.9453125  0.5673828125
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-8.0.1 (ORCJIT, skylake)
```

---
# Baseline result
# Benchmark Report for */home/travis/build/JuliaFolds/Transducers.jl*

## Job Properties
* Time of benchmark: 1 Aug 2020 - 6:36
* Package commit: d1995c
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
| `["append!!", "eduction"]`               |  16.969 μs (5%) |         |  64.72 KiB (1%) |          18 |
| `["append!!", "xf"]`                     |  16.856 μs (5%) |         |  64.72 KiB (1%) |          18 |
| `["cat", "base"]`                        |   1.634 μs (5%) |         |                 |             |
| `["cat", "xf"]`                          |   1.748 μs (5%) |         |                 |             |
| `["collect", "filter-missing"]`          |  93.855 μs (5%) |         | 345.31 KiB (1%) |       10015 |
| `["collect", "identity-float"]`          |  69.793 μs (5%) |         | 569.16 KiB (1%) |       10015 |
| `["collect", "identity-union"]`          | 280.206 μs (5%) |         | 704.94 KiB (1%) |       16655 |
| `["dict", "base"]`                       |   3.613 ms (5%) |         |  92.91 KiB (1%) |          22 |
| `["dict", "xf"]`                         |   3.720 ms (5%) |         |  92.36 KiB (1%) |          21 |
| `["dot", "blas"]`                        |   1.212 μs (5%) |         |                 |             |
| `["dot", "man"]`                         |   1.209 μs (5%) |         |                 |             |
| `["dot", "rf"]`                          |   2.194 μs (5%) |         |                 |             |
| `["dot", "xf"]`                          |   2.272 μs (5%) |         |   64 bytes (1%) |           3 |
| `["filter_map_map!", "man"]`             |  76.186 μs (5%) |         |                 |             |
| `["filter_map_map!", "xf"]`              | 667.318 μs (5%) |         |  304 bytes (1%) |          17 |
| `["filter_map_reduce", "man"]`           | 202.713 μs (5%) |         |                 |             |
| `["filter_map_reduce", "xf"]`            | 203.813 μs (5%) |         |                 |             |
| `["findall", "base"]`                    | 759.262 μs (5%) |         |   2.00 MiB (1%) |          21 |
| `["findall", "xf-array"]`                | 712.128 μs (5%) |         |   3.02 MiB (1%) |       98826 |
| `["findall", "xf-iter"]`                 |   2.973 ms (5%) |         |   9.63 MiB (1%) |      299939 |
| `["gemm", "fusedmul", "blas", "16"]`     |   4.782 ms (5%) |         |                 |             |
| `["gemm", "fusedmul", "blas", "2"]`      |   3.314 ms (5%) |         |                 |             |
| `["gemm", "fusedmul", "blas", "32"]`     |   6.688 ms (5%) |         |                 |             |
| `["gemm", "fusedmul", "blas", "8"]`      |   3.623 ms (5%) |         |                 |             |
| `["gemm", "fusedmul", "xf", "16"]`       |   4.798 ms (5%) |         |  160 bytes (1%) |           6 |
| `["gemm", "fusedmul", "xf", "2"]`        | 565.560 μs (5%) |         |  160 bytes (1%) |           6 |
| `["gemm", "fusedmul", "xf", "32"]`       |   8.202 ms (5%) |         |  160 bytes (1%) |           6 |
| `["gemm", "fusedmul", "xf", "8"]`        |   2.309 ms (5%) |         |  160 bytes (1%) |           6 |
| `["gemm", "mul", "linalg", "256"]`       | 952.131 μs (5%) |         |                 |             |
| `["gemm", "mul", "linalg", "32"]`        |   3.206 μs (5%) |         |                 |             |
| `["gemm", "mul", "linalg", "8"]`         | 290.000 ns (5%) |         |                 |             |
| `["gemm", "mul", "man", "false", "256"]` |   2.049 ms (5%) |         |                 |             |
| `["gemm", "mul", "man", "false", "32"]`  |   4.974 μs (5%) |         |                 |             |
| `["gemm", "mul", "man", "false", "8"]`   | 412.000 ns (5%) |         |                 |             |
| `["gemm", "mul", "man", "ivdep", "256"]` |   2.015 ms (5%) |         |                 |             |
| `["gemm", "mul", "man", "ivdep", "32"]`  |   4.315 μs (5%) |         |                 |             |
| `["gemm", "mul", "man", "ivdep", "8"]`   | 429.000 ns (5%) |         |                 |             |
| `["gemm", "mul", "man", "true", "256"]`  |   2.033 ms (5%) |         |                 |             |
| `["gemm", "mul", "man", "true", "32"]`   |   5.139 μs (5%) |         |                 |             |
| `["gemm", "mul", "man", "true", "8"]`    | 440.000 ns (5%) |         |                 |             |
| `["gemm", "mul", "xf", "false", "256"]`  |   2.052 ms (5%) |         |   48 bytes (1%) |           2 |
| `["gemm", "mul", "xf", "false", "32"]`   |   4.583 μs (5%) |         |   48 bytes (1%) |           2 |
| `["gemm", "mul", "xf", "false", "8"]`    | 386.000 ns (5%) |         |   48 bytes (1%) |           2 |
| `["gemm", "mul", "xf", "ivdep", "256"]`  |   2.011 ms (5%) |         |   48 bytes (1%) |           2 |
| `["gemm", "mul", "xf", "ivdep", "32"]`   |   4.465 μs (5%) |         |   48 bytes (1%) |           2 |
| `["gemm", "mul", "xf", "ivdep", "8"]`    | 375.000 ns (5%) |         |   48 bytes (1%) |           2 |
| `["gemm", "mul", "xf", "true", "256"]`   |   2.046 ms (5%) |         |   48 bytes (1%) |           2 |
| `["gemm", "mul", "xf", "true", "32"]`    |   4.900 μs (5%) |         |   48 bytes (1%) |           2 |
| `["gemm", "mul", "xf", "true", "8"]`     | 389.000 ns (5%) |         |   48 bytes (1%) |           2 |
| `["groupby", "sum", "sac"]`              | 228.681 μs (5%) |         | 313.14 KiB (1%) |       10007 |
| `["groupby", "sum", "xf-with-init"]`     | 162.630 μs (5%) |         | 157.44 KiB (1%) |       10008 |
| `["groupby", "sum", "xf-without-init"]`  | 167.798 μs (5%) |         | 157.44 KiB (1%) |       10008 |
| `["mapcat_eduction", "base"]`            |   1.937 μs (5%) |         |                 |             |
| `["mapcat_eduction", "xf-eduction"]`     |   1.678 μs (5%) |         |                 |             |
| `["mapcat_eduction", "xf-xf"]`           |   1.677 μs (5%) |         |                 |             |
| `["missing_argmax", "man"]`              |   2.369 μs (5%) |         |   32 bytes (1%) |           1 |
| `["missing_argmax", "rf"]`               |   2.814 μs (5%) |         |   32 bytes (1%) |           1 |
| `["missing_argmax", "xf"]`               |   2.284 μs (5%) |         |   32 bytes (1%) |           1 |
| `["missing_dot", "equiv"]`               |   1.564 μs (5%) |         |   16 bytes (1%) |           1 |
| `["missing_dot", "man"]`                 |   1.299 μs (5%) |         |   16 bytes (1%) |           1 |
| `["missing_dot", "naive"]`               |   4.398 μs (5%) |         |   16 bytes (1%) |           1 |
| `["missing_dot", "rf"]`                  |   1.255 μs (5%) |         |   16 bytes (1%) |           1 |
| `["missing_dot", "rf_nota"]`             |   1.533 μs (5%) |         |   16 bytes (1%) |           1 |
| `["missing_dot", "xf"]`                  | 192.189 μs (5%) |         |  72.02 KiB (1%) |        3738 |
| `["missing_dot", "xf_nota"]`             | 187.064 μs (5%) |         |  72.09 KiB (1%) |        3740 |
| `["overhead", "foldl"]`                  |   4.739 ns (5%) |         |                 |             |
| `["overhead", "reduce_basecase"]`        | 161.051 ns (5%) |         |  416 bytes (1%) |           7 |
| `["partition_by", "man"]`                |   1.792 ms (5%) |         |  352 bytes (1%) |           4 |
| `["partition_by", "xf"]`                 |   2.723 ms (5%) |         |   6.10 MiB (1%) |      200007 |
| `["set", "base"]`                        |   4.280 ms (5%) |         |  49.58 KiB (1%) |          18 |
| `["set", "xf"]`                          |   3.980 ms (5%) |         |  49.63 KiB (1%) |          21 |

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
       #1  2800 MHz      17853 s          0 s       1316 s      69986 s          0 s
       #2  2800 MHz      71471 s          0 s       1412 s      18953 s          0 s
       
  Memory: 7.790031433105469 GB (5458.16796875 MB free)
  Uptime: 922.0 sec
  Load Avg:  1.42138671875  1.103515625  0.72607421875
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
    CPU MHz:               2800.170
    BogoMIPS:              5600.34
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

