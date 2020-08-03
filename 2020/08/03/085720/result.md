# Benchmark result (via Travis)


# Judge result
# Benchmark Report for */home/travis/build/JuliaFolds/Transducers.jl*

## Job Properties
* Time of benchmarks:
    - Target: 3 Aug 2020 - 08:52
    - Baseline: 3 Aug 2020 - 08:56
* Package commits:
    - Target: 80799b
    - Baseline: 0a31f9
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
| `["cat", "base"]`                        |                1.07 (5%) :x: |    1.00 (1%)  |
| `["filter_map_map!", "man"]`             | 0.90 (5%) :white_check_mark: |    1.00 (1%)  |
| `["filter_map_map!", "xf"]`              | 0.94 (5%) :white_check_mark: |    1.00 (1%)  |
| `["findall", "xf-array"]`                |                   1.03 (5%)  | 1.03 (1%) :x: |
| `["gemm", "fusedmul", "blas", "16"]`     |                1.07 (5%) :x: |    1.00 (1%)  |
| `["gemm", "fusedmul", "blas", "32"]`     |                1.08 (5%) :x: |    1.00 (1%)  |
| `["gemm", "fusedmul", "xf", "2"]`        | 0.93 (5%) :white_check_mark: |    1.00 (1%)  |
| `["gemm", "fusedmul", "xf", "8"]`        | 0.89 (5%) :white_check_mark: |    1.00 (1%)  |
| `["gemm", "mul", "linalg", "32"]`        | 0.88 (5%) :white_check_mark: |    1.00 (1%)  |
| `["gemm", "mul", "linalg", "8"]`         | 0.76 (5%) :white_check_mark: |    1.00 (1%)  |
| `["gemm", "mul", "man", "false", "32"]`  |                1.12 (5%) :x: |    1.00 (1%)  |
| `["gemm", "mul", "man", "false", "8"]`   |                1.19 (5%) :x: |    1.00 (1%)  |
| `["gemm", "mul", "man", "ivdep", "8"]`   | 0.80 (5%) :white_check_mark: |    1.00 (1%)  |
| `["gemm", "mul", "man", "true", "32"]`   |                1.12 (5%) :x: |    1.00 (1%)  |
| `["gemm", "mul", "xf", "false", "32"]`   | 0.81 (5%) :white_check_mark: |    1.00 (1%)  |
| `["gemm", "mul", "xf", "false", "8"]`    |                1.22 (5%) :x: |    1.00 (1%)  |
| `["gemm", "mul", "xf", "ivdep", "8"]`    |                1.24 (5%) :x: |    1.00 (1%)  |
| `["gemm", "mul", "xf", "true", "8"]`     |                1.30 (5%) :x: |    1.00 (1%)  |
| `["groupby", "sum", "sac"]`              | 0.94 (5%) :white_check_mark: |    1.00 (1%)  |
| `["groupby", "sum", "xf-with-init"]`     | 0.91 (5%) :white_check_mark: |    1.00 (1%)  |
| `["groupby", "sum", "xf-without-init"]`  | 0.90 (5%) :white_check_mark: |    1.00 (1%)  |
| `["mapcat_eduction", "xf-xf"]`           | 0.95 (5%) :white_check_mark: |    1.00 (1%)  |
| `["missing_dot", "man"]`                 |                1.12 (5%) :x: |    1.00 (1%)  |
| `["missing_dot", "rf"]`                  | 0.95 (5%) :white_check_mark: |    1.00 (1%)  |
| `["set", "xf"]`                          | 0.95 (5%) :white_check_mark: |    1.00 (1%)  |

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
       #1  2800 MHz      20144 s          0 s       1100 s      47638 s          0 s
       #2  2800 MHz      45908 s          0 s       1281 s      22748 s          0 s
       
  Memory: 7.790031433105469 GB (5716.8046875 MB free)
  Uptime: 705.0 sec
  Load Avg:  1.0  0.9521484375  0.5859375
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
       #1  2800 MHz      26917 s          0 s       1202 s      67693 s          0 s
       #2  2800 MHz      66044 s          0 s       1390 s      29474 s          0 s
       
  Memory: 7.790031433105469 GB (5691.69140625 MB free)
  Uptime: 975.0 sec
  Load Avg:  1.01513671875  1.015625  0.71923828125
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-8.0.1 (ORCJIT, skylake)
```

---
# Target result
# Benchmark Report for */home/travis/build/JuliaFolds/Transducers.jl*

## Job Properties
* Time of benchmark: 3 Aug 2020 - 8:52
* Package commit: 80799b
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
| `["append!!", "eduction"]`               |  18.732 μs (5%) |         |  64.72 KiB (1%) |          18 |
| `["append!!", "xf"]`                     |  18.723 μs (5%) |         |  64.72 KiB (1%) |          18 |
| `["cat", "base"]`                        |   1.632 μs (5%) |         |                 |             |
| `["cat", "xf"]`                          |   2.074 μs (5%) |         |                 |             |
| `["collect", "filter-missing"]`          | 103.888 μs (5%) |         | 345.31 KiB (1%) |       10015 |
| `["collect", "identity-float"]`          |  91.806 μs (5%) |         | 569.16 KiB (1%) |       10015 |
| `["collect", "identity-union"]`          | 307.922 μs (5%) |         | 705.05 KiB (1%) |       16658 |
| `["dict", "base"]`                       |   3.577 ms (5%) |         |  92.91 KiB (1%) |          22 |
| `["dict", "xf"]`                         |   3.693 ms (5%) |         |  92.36 KiB (1%) |          21 |
| `["dot", "blas"]`                        |   1.238 μs (5%) |         |                 |             |
| `["dot", "man"]`                         |   1.203 μs (5%) |         |                 |             |
| `["dot", "rf"]`                          |   2.169 μs (5%) |         |                 |             |
| `["dot", "xf"]`                          |   2.279 μs (5%) |         |   64 bytes (1%) |           3 |
| `["filter_map_map!", "man"]`             |  71.306 μs (5%) |         |                 |             |
| `["filter_map_map!", "xf"]`              | 625.103 μs (5%) |         |  304 bytes (1%) |          17 |
| `["filter_map_reduce", "man"]`           | 202.727 μs (5%) |         |                 |             |
| `["filter_map_reduce", "xf"]`            | 202.722 μs (5%) |         |                 |             |
| `["findall", "base"]`                    | 831.051 μs (5%) |         |   2.00 MiB (1%) |          21 |
| `["findall", "xf-array"]`                | 787.388 μs (5%) |         |   3.03 MiB (1%) |       99366 |
| `["findall", "xf-iter"]`                 |   3.205 ms (5%) |         |   9.63 MiB (1%) |      299931 |
| `["gemm", "fusedmul", "blas", "16"]`     |   5.631 ms (5%) |         |                 |             |
| `["gemm", "fusedmul", "blas", "2"]`      |   4.016 ms (5%) |         |                 |             |
| `["gemm", "fusedmul", "blas", "32"]`     |   7.777 ms (5%) |         |                 |             |
| `["gemm", "fusedmul", "blas", "8"]`      |   4.550 ms (5%) |         |                 |             |
| `["gemm", "fusedmul", "xf", "16"]`       |   4.947 ms (5%) |         |  160 bytes (1%) |           6 |
| `["gemm", "fusedmul", "xf", "2"]`        | 576.514 μs (5%) |         |  160 bytes (1%) |           6 |
| `["gemm", "fusedmul", "xf", "32"]`       |   9.849 ms (5%) |         |  160 bytes (1%) |           6 |
| `["gemm", "fusedmul", "xf", "8"]`        |   2.151 ms (5%) |         |  160 bytes (1%) |           6 |
| `["gemm", "mul", "linalg", "256"]`       | 962.550 μs (5%) |         |                 |             |
| `["gemm", "mul", "linalg", "32"]`        |   3.098 μs (5%) |         |                 |             |
| `["gemm", "mul", "linalg", "8"]`         | 249.348 ns (5%) |         |                 |             |
| `["gemm", "mul", "man", "false", "256"]` |   2.031 ms (5%) |         |                 |             |
| `["gemm", "mul", "man", "false", "32"]`  |   5.544 μs (5%) |         |                 |             |
| `["gemm", "mul", "man", "false", "8"]`   | 512.078 ns (5%) |         |                 |             |
| `["gemm", "mul", "man", "ivdep", "256"]` |   2.033 ms (5%) |         |                 |             |
| `["gemm", "mul", "man", "ivdep", "32"]`  |   4.531 μs (5%) |         |                 |             |
| `["gemm", "mul", "man", "ivdep", "8"]`   | 398.797 ns (5%) |         |                 |             |
| `["gemm", "mul", "man", "true", "256"]`  |   2.025 ms (5%) |         |                 |             |
| `["gemm", "mul", "man", "true", "32"]`   |   5.630 μs (5%) |         |                 |             |
| `["gemm", "mul", "man", "true", "8"]`    | 413.145 ns (5%) |         |                 |             |
| `["gemm", "mul", "xf", "false", "256"]`  |   2.033 ms (5%) |         |   48 bytes (1%) |           2 |
| `["gemm", "mul", "xf", "false", "32"]`   |   5.079 μs (5%) |         |   48 bytes (1%) |           2 |
| `["gemm", "mul", "xf", "false", "8"]`    | 465.578 ns (5%) |         |   48 bytes (1%) |           2 |
| `["gemm", "mul", "xf", "ivdep", "256"]`  |   2.023 ms (5%) |         |   48 bytes (1%) |           2 |
| `["gemm", "mul", "xf", "ivdep", "32"]`   |   4.582 μs (5%) |         |   48 bytes (1%) |           2 |
| `["gemm", "mul", "xf", "ivdep", "8"]`    | 456.152 ns (5%) |         |   48 bytes (1%) |           2 |
| `["gemm", "mul", "xf", "true", "256"]`   |   2.017 ms (5%) |         |   48 bytes (1%) |           2 |
| `["gemm", "mul", "xf", "true", "32"]`    |   5.516 μs (5%) |         |   48 bytes (1%) |           2 |
| `["gemm", "mul", "xf", "true", "8"]`     | 498.949 ns (5%) |         |   48 bytes (1%) |           2 |
| `["groupby", "sum", "sac"]`              | 223.358 μs (5%) |         | 313.14 KiB (1%) |       10007 |
| `["groupby", "sum", "xf-with-init"]`     | 173.134 μs (5%) |         | 157.44 KiB (1%) |       10008 |
| `["groupby", "sum", "xf-without-init"]`  | 169.466 μs (5%) |         | 157.44 KiB (1%) |       10008 |
| `["mapcat_eduction", "base"]`            |   1.927 μs (5%) |         |                 |             |
| `["mapcat_eduction", "xf-eduction"]`     |   1.781 μs (5%) |         |                 |             |
| `["mapcat_eduction", "xf-xf"]`           |   1.687 μs (5%) |         |                 |             |
| `["missing_argmax", "man"]`              |   2.367 μs (5%) |         |   32 bytes (1%) |           1 |
| `["missing_argmax", "rf"]`               |   2.303 μs (5%) |         |   32 bytes (1%) |           1 |
| `["missing_argmax", "xf"]`               |   2.837 μs (5%) |         |   32 bytes (1%) |           1 |
| `["missing_dot", "equiv"]`               |   1.488 μs (5%) |         |   16 bytes (1%) |           1 |
| `["missing_dot", "man"]`                 |   1.369 μs (5%) |         |   16 bytes (1%) |           1 |
| `["missing_dot", "naive"]`               |   4.314 μs (5%) |         |   16 bytes (1%) |           1 |
| `["missing_dot", "rf"]`                  |   1.250 μs (5%) |         |   16 bytes (1%) |           1 |
| `["missing_dot", "rf_nota"]`             |   1.537 μs (5%) |         |   16 bytes (1%) |           1 |
| `["missing_dot", "xf"]`                  | 188.316 μs (5%) |         |  72.13 KiB (1%) |        3742 |
| `["missing_dot", "xf_nota"]`             | 182.694 μs (5%) |         |  71.88 KiB (1%) |        3732 |
| `["overhead", "foldl"]`                  |   4.150 ns (5%) |         |                 |             |
| `["overhead", "reduce_basecase"]`        | 244.349 ns (5%) |         |  464 bytes (1%) |           9 |
| `["partition_by", "man"]`                |   1.833 ms (5%) |         |  352 bytes (1%) |           4 |
| `["partition_by", "xf"]`                 |   2.861 ms (5%) |         |   6.10 MiB (1%) |      200007 |
| `["set", "base"]`                        |   4.293 ms (5%) |         |  49.58 KiB (1%) |          18 |
| `["set", "xf"]`                          |   3.978 ms (5%) |         |  49.63 KiB (1%) |          21 |

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
       #1  2800 MHz      20144 s          0 s       1100 s      47638 s          0 s
       #2  2800 MHz      45908 s          0 s       1281 s      22748 s          0 s
       
  Memory: 7.790031433105469 GB (5716.8046875 MB free)
  Uptime: 705.0 sec
  Load Avg:  1.0  0.9521484375  0.5859375
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-8.0.1 (ORCJIT, skylake)
```

---
# Baseline result
# Benchmark Report for */home/travis/build/JuliaFolds/Transducers.jl*

## Job Properties
* Time of benchmark: 3 Aug 2020 - 8:56
* Package commit: 0a31f9
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
| `["append!!", "eduction"]`               |  18.835 μs (5%) |         |  64.72 KiB (1%) |          18 |
| `["append!!", "xf"]`                     |  18.729 μs (5%) |         |  64.72 KiB (1%) |          18 |
| `["cat", "base"]`                        |   1.527 μs (5%) |         |                 |             |
| `["cat", "xf"]`                          |   2.074 μs (5%) |         |                 |             |
| `["collect", "filter-missing"]`          | 104.644 μs (5%) |         | 345.31 KiB (1%) |       10015 |
| `["collect", "identity-float"]`          |  91.510 μs (5%) |         | 569.16 KiB (1%) |       10015 |
| `["collect", "identity-union"]`          | 302.463 μs (5%) |         | 705.00 KiB (1%) |       16659 |
| `["dict", "base"]`                       |   3.580 ms (5%) |         |  92.91 KiB (1%) |          22 |
| `["dict", "xf"]`                         |   3.725 ms (5%) |         |  92.36 KiB (1%) |          21 |
| `["dot", "blas"]`                        |   1.207 μs (5%) |         |                 |             |
| `["dot", "man"]`                         |   1.189 μs (5%) |         |                 |             |
| `["dot", "rf"]`                          |   2.198 μs (5%) |         |                 |             |
| `["dot", "xf"]`                          |   2.268 μs (5%) |         |   64 bytes (1%) |           3 |
| `["filter_map_map!", "man"]`             |  78.964 μs (5%) |         |                 |             |
| `["filter_map_map!", "xf"]`              | 665.922 μs (5%) |         |  304 bytes (1%) |          17 |
| `["filter_map_reduce", "man"]`           | 203.123 μs (5%) |         |                 |             |
| `["filter_map_reduce", "xf"]`            | 204.046 μs (5%) |         |                 |             |
| `["findall", "base"]`                    | 823.666 μs (5%) |         |   2.00 MiB (1%) |          21 |
| `["findall", "xf-array"]`                | 762.177 μs (5%) |         |   2.94 MiB (1%) |       96405 |
| `["findall", "xf-iter"]`                 |   3.125 ms (5%) |         |   9.63 MiB (1%) |      299929 |
| `["gemm", "fusedmul", "blas", "16"]`     |   5.278 ms (5%) |         |                 |             |
| `["gemm", "fusedmul", "blas", "2"]`      |   4.095 ms (5%) |         |                 |             |
| `["gemm", "fusedmul", "blas", "32"]`     |   7.221 ms (5%) |         |                 |             |
| `["gemm", "fusedmul", "blas", "8"]`      |   4.546 ms (5%) |         |                 |             |
| `["gemm", "fusedmul", "xf", "16"]`       |   4.820 ms (5%) |         |  160 bytes (1%) |           6 |
| `["gemm", "fusedmul", "xf", "2"]`        | 620.243 μs (5%) |         |  160 bytes (1%) |           6 |
| `["gemm", "fusedmul", "xf", "32"]`       |   9.414 ms (5%) |         |  160 bytes (1%) |           6 |
| `["gemm", "fusedmul", "xf", "8"]`        |   2.416 ms (5%) |         |  160 bytes (1%) |           6 |
| `["gemm", "mul", "linalg", "256"]`       | 963.477 μs (5%) |         |                 |             |
| `["gemm", "mul", "linalg", "32"]`        |   3.513 μs (5%) |         |                 |             |
| `["gemm", "mul", "linalg", "8"]`         | 327.000 ns (5%) |         |                 |             |
| `["gemm", "mul", "man", "false", "256"]` |   2.075 ms (5%) |         |                 |             |
| `["gemm", "mul", "man", "false", "32"]`  |   4.937 μs (5%) |         |                 |             |
| `["gemm", "mul", "man", "false", "8"]`   | 430.000 ns (5%) |         |                 |             |
| `["gemm", "mul", "man", "ivdep", "256"]` |   2.026 ms (5%) |         |                 |             |
| `["gemm", "mul", "man", "ivdep", "32"]`  |   4.533 μs (5%) |         |                 |             |
| `["gemm", "mul", "man", "ivdep", "8"]`   | 499.000 ns (5%) |         |                 |             |
| `["gemm", "mul", "man", "true", "256"]`  |   2.054 ms (5%) |         |                 |             |
| `["gemm", "mul", "man", "true", "32"]`   |   5.012 μs (5%) |         |                 |             |
| `["gemm", "mul", "man", "true", "8"]`    | 424.000 ns (5%) |         |                 |             |
| `["gemm", "mul", "xf", "false", "256"]`  |   2.077 ms (5%) |         |   48 bytes (1%) |           2 |
| `["gemm", "mul", "xf", "false", "32"]`   |   6.268 μs (5%) |         |   48 bytes (1%) |           2 |
| `["gemm", "mul", "xf", "false", "8"]`    | 382.000 ns (5%) |         |   48 bytes (1%) |           2 |
| `["gemm", "mul", "xf", "ivdep", "256"]`  |   2.020 ms (5%) |         |   48 bytes (1%) |           2 |
| `["gemm", "mul", "xf", "ivdep", "32"]`   |   4.674 μs (5%) |         |   48 bytes (1%) |           2 |
| `["gemm", "mul", "xf", "ivdep", "8"]`    | 368.000 ns (5%) |         |   48 bytes (1%) |           2 |
| `["gemm", "mul", "xf", "true", "256"]`   |   2.066 ms (5%) |         |   48 bytes (1%) |           2 |
| `["gemm", "mul", "xf", "true", "32"]`    |   5.566 μs (5%) |         |   48 bytes (1%) |           2 |
| `["gemm", "mul", "xf", "true", "8"]`     | 385.000 ns (5%) |         |   48 bytes (1%) |           2 |
| `["groupby", "sum", "sac"]`              | 238.758 μs (5%) |         | 313.14 KiB (1%) |       10007 |
| `["groupby", "sum", "xf-with-init"]`     | 190.088 μs (5%) |         | 157.44 KiB (1%) |       10008 |
| `["groupby", "sum", "xf-without-init"]`  | 187.853 μs (5%) |         | 157.44 KiB (1%) |       10008 |
| `["mapcat_eduction", "base"]`            |   1.925 μs (5%) |         |                 |             |
| `["mapcat_eduction", "xf-eduction"]`     |   1.781 μs (5%) |         |                 |             |
| `["mapcat_eduction", "xf-xf"]`           |   1.781 μs (5%) |         |                 |             |
| `["missing_argmax", "man"]`              |   2.366 μs (5%) |         |   32 bytes (1%) |           1 |
| `["missing_argmax", "rf"]`               |   2.308 μs (5%) |         |   32 bytes (1%) |           1 |
| `["missing_argmax", "xf"]`               |   2.843 μs (5%) |         |   32 bytes (1%) |           1 |
| `["missing_dot", "equiv"]`               |   1.500 μs (5%) |         |   16 bytes (1%) |           1 |
| `["missing_dot", "man"]`                 |   1.223 μs (5%) |         |   16 bytes (1%) |           1 |
| `["missing_dot", "naive"]`               |   4.338 μs (5%) |         |   16 bytes (1%) |           1 |
| `["missing_dot", "rf"]`                  |   1.320 μs (5%) |         |   16 bytes (1%) |           1 |
| `["missing_dot", "rf_nota"]`             |   1.510 μs (5%) |         |   16 bytes (1%) |           1 |
| `["missing_dot", "xf"]`                  | 192.625 μs (5%) |         |  72.14 KiB (1%) |        3742 |
| `["missing_dot", "xf_nota"]`             | 190.922 μs (5%) |         |  71.97 KiB (1%) |        3734 |
| `["overhead", "foldl"]`                  |   4.150 ns (5%) |         |                 |             |
| `["overhead", "reduce_basecase"]`        | 238.516 ns (5%) |         |  464 bytes (1%) |           9 |
| `["partition_by", "man"]`                |   1.825 ms (5%) |         |  352 bytes (1%) |           4 |
| `["partition_by", "xf"]`                 |   2.847 ms (5%) |         |   6.10 MiB (1%) |      200007 |
| `["set", "base"]`                        |   4.327 ms (5%) |         |  49.58 KiB (1%) |          18 |
| `["set", "xf"]`                          |   4.189 ms (5%) |         |  49.63 KiB (1%) |          21 |

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
       #1  2800 MHz      26917 s          0 s       1202 s      67693 s          0 s
       #2  2800 MHz      66044 s          0 s       1390 s      29474 s          0 s
       
  Memory: 7.790031433105469 GB (5691.69140625 MB free)
  Uptime: 975.0 sec
  Load Avg:  1.01513671875  1.015625  0.71923828125
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
    CPU MHz:               2800.208
    BogoMIPS:              5600.41
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

