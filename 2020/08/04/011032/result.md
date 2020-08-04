# Benchmark result (via Travis)


# Judge result
# Benchmark Report for */home/travis/build/JuliaFolds/Transducers.jl*

## Job Properties
* Time of benchmarks:
    - Target: 4 Aug 2020 - 01:04
    - Baseline: 4 Aug 2020 - 01:09
* Package commits:
    - Target: ec4a9a
    - Baseline: d6f0cd
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
| `["cat", "xf"]`                          |                1.19 (5%) :x: |                   1.00 (1%)  |
| `["filter_map_map!", "man"]`             |                1.15 (5%) :x: |                   1.00 (1%)  |
| `["findall", "xf-array"]`                |                   1.01 (5%)  | 0.99 (1%) :white_check_mark: |
| `["gemm", "fusedmul", "xf", "8"]`        |                1.06 (5%) :x: |                   1.00 (1%)  |
| `["gemm", "mul", "linalg", "8"]`         | 0.83 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["gemm", "mul", "man", "false", "256"]` |                1.07 (5%) :x: |                   1.00 (1%)  |
| `["gemm", "mul", "man", "false", "32"]`  |                1.07 (5%) :x: |                   1.00 (1%)  |
| `["gemm", "mul", "man", "false", "8"]`   |                1.23 (5%) :x: |                   1.00 (1%)  |
| `["gemm", "mul", "man", "ivdep", "32"]`  |                1.06 (5%) :x: |                   1.00 (1%)  |
| `["gemm", "mul", "man", "ivdep", "8"]`   | 0.93 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["gemm", "mul", "man", "true", "256"]`  |                1.06 (5%) :x: |                   1.00 (1%)  |
| `["gemm", "mul", "man", "true", "32"]`   |                1.09 (5%) :x: |                   1.00 (1%)  |
| `["gemm", "mul", "man", "true", "8"]`    | 0.92 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["gemm", "mul", "xf", "false", "256"]`  |                1.07 (5%) :x: |                   1.00 (1%)  |
| `["gemm", "mul", "xf", "ivdep", "8"]`    |                1.20 (5%) :x: |                   1.00 (1%)  |
| `["gemm", "mul", "xf", "true", "256"]`   |                1.08 (5%) :x: |                   1.00 (1%)  |
| `["gemm", "mul", "xf", "true", "32"]`    |                1.08 (5%) :x: |                   1.00 (1%)  |
| `["gemm", "mul", "xf", "true", "8"]`     |                1.23 (5%) :x: |                   1.00 (1%)  |
| `["groupby", "sum", "sac"]`              | 0.62 (5%) :white_check_mark: | 0.50 (1%) :white_check_mark: |
| `["groupby", "sum", "xf-without-init"]`  | 0.93 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["mapcat_eduction", "xf-eduction"]`     |                1.06 (5%) :x: |                   1.00 (1%)  |
| `["missing_argmax", "rf"]`               |                1.24 (5%) :x: |                   1.00 (1%)  |
| `["missing_argmax", "xf"]`               | 0.80 (5%) :white_check_mark: |                   1.00 (1%)  |

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
       #1  2800 MHz      11254 s          0 s       1108 s      53725 s          0 s
       #2  2800 MHz      52930 s          0 s       1211 s      12486 s          0 s
       
  Memory: 7.7900238037109375 GB (5705.3046875 MB free)
  Uptime: 671.0 sec
  Load Avg:  1.00146484375  0.9267578125  0.55078125
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
       #1  2800 MHz      20524 s          0 s       1327 s      74592 s          0 s
       #2  2800 MHz      73642 s          0 s       1514 s      21865 s          0 s
       
  Memory: 7.7900238037109375 GB (5655.08203125 MB free)
  Uptime: 975.0 sec
  Load Avg:  1.11669921875  1.05078125  0.72998046875
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-8.0.1 (ORCJIT, skylake)
```

---
# Target result
# Benchmark Report for */home/travis/build/JuliaFolds/Transducers.jl*

## Job Properties
* Time of benchmark: 4 Aug 2020 - 1:4
* Package commit: ec4a9a
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
| `["append!!", "eduction"]`               |  19.123 μs (5%) |         |  64.72 KiB (1%) |          18 |
| `["append!!", "xf"]`                     |  18.844 μs (5%) |         |  64.72 KiB (1%) |          18 |
| `["cat", "base"]`                        |   1.635 μs (5%) |         |                 |             |
| `["cat", "xf"]`                          |   2.075 μs (5%) |         |                 |             |
| `["collect", "filter-missing"]`          | 104.486 μs (5%) |         | 345.31 KiB (1%) |       10015 |
| `["collect", "identity-float"]`          |  87.369 μs (5%) |         | 569.16 KiB (1%) |       10015 |
| `["collect", "identity-union"]`          | 305.571 μs (5%) |         | 705.14 KiB (1%) |       16668 |
| `["dict", "base"]`                       |   3.613 ms (5%) |         |  92.91 KiB (1%) |          22 |
| `["dict", "xf"]`                         |   3.720 ms (5%) |         |  92.36 KiB (1%) |          21 |
| `["dot", "blas"]`                        |   1.219 μs (5%) |         |                 |             |
| `["dot", "man"]`                         |   1.206 μs (5%) |         |                 |             |
| `["dot", "rf"]`                          |   2.191 μs (5%) |         |                 |             |
| `["dot", "xf"]`                          |   2.274 μs (5%) |         |   64 bytes (1%) |           3 |
| `["filter_map_map!", "man"]`             |  75.825 μs (5%) |         |                 |             |
| `["filter_map_map!", "xf"]`              | 669.439 μs (5%) |         |  304 bytes (1%) |          17 |
| `["filter_map_reduce", "man"]`           | 202.886 μs (5%) |         |                 |             |
| `["filter_map_reduce", "xf"]`            | 202.708 μs (5%) |         |                 |             |
| `["findall", "base"]`                    | 827.415 μs (5%) |         |   2.00 MiB (1%) |          21 |
| `["findall", "xf-array"]`                | 777.974 μs (5%) |         |   3.01 MiB (1%) |       98565 |
| `["findall", "xf-iter"]`                 |   3.298 ms (5%) |         |   9.63 MiB (1%) |      299913 |
| `["gemm", "fusedmul", "blas", "16"]`     |   5.471 ms (5%) |         |                 |             |
| `["gemm", "fusedmul", "blas", "2"]`      |   3.954 ms (5%) |         |                 |             |
| `["gemm", "fusedmul", "blas", "32"]`     |   7.637 ms (5%) |         |                 |             |
| `["gemm", "fusedmul", "blas", "8"]`      |   4.293 ms (5%) |         |                 |             |
| `["gemm", "fusedmul", "xf", "16"]`       |   4.522 ms (5%) |         |  160 bytes (1%) |           6 |
| `["gemm", "fusedmul", "xf", "2"]`        | 567.261 μs (5%) |         |  160 bytes (1%) |           6 |
| `["gemm", "fusedmul", "xf", "32"]`       |   8.958 ms (5%) |         |  160 bytes (1%) |           6 |
| `["gemm", "fusedmul", "xf", "8"]`        |   2.455 ms (5%) |         |  160 bytes (1%) |           6 |
| `["gemm", "mul", "linalg", "256"]`       | 962.399 μs (5%) |         |                 |             |
| `["gemm", "mul", "linalg", "32"]`        |   3.378 μs (5%) |         |                 |             |
| `["gemm", "mul", "linalg", "8"]`         | 253.374 ns (5%) |         |                 |             |
| `["gemm", "mul", "man", "false", "256"]` |   2.046 ms (5%) |         |                 |             |
| `["gemm", "mul", "man", "false", "32"]`  |   5.557 μs (5%) |         |                 |             |
| `["gemm", "mul", "man", "false", "8"]`   | 512.266 ns (5%) |         |                 |             |
| `["gemm", "mul", "man", "ivdep", "256"]` |   2.014 ms (5%) |         |                 |             |
| `["gemm", "mul", "man", "ivdep", "32"]`  |   4.610 μs (5%) |         |                 |             |
| `["gemm", "mul", "man", "ivdep", "8"]`   | 398.320 ns (5%) |         |                 |             |
| `["gemm", "mul", "man", "true", "256"]`  |   2.032 ms (5%) |         |                 |             |
| `["gemm", "mul", "man", "true", "32"]`   |   5.648 μs (5%) |         |                 |             |
| `["gemm", "mul", "man", "true", "8"]`    | 411.850 ns (5%) |         |                 |             |
| `["gemm", "mul", "xf", "false", "256"]`  |   2.048 ms (5%) |         |   48 bytes (1%) |           2 |
| `["gemm", "mul", "xf", "false", "32"]`   |   6.203 μs (5%) |         |   48 bytes (1%) |           2 |
| `["gemm", "mul", "xf", "false", "8"]`    | 393.203 ns (5%) |         |   48 bytes (1%) |           2 |
| `["gemm", "mul", "xf", "ivdep", "256"]`  |   2.003 ms (5%) |         |   48 bytes (1%) |           2 |
| `["gemm", "mul", "xf", "ivdep", "32"]`   |   4.602 μs (5%) |         |   48 bytes (1%) |           2 |
| `["gemm", "mul", "xf", "ivdep", "8"]`    | 453.782 ns (5%) |         |   48 bytes (1%) |           2 |
| `["gemm", "mul", "xf", "true", "256"]`   |   2.065 ms (5%) |         |   48 bytes (1%) |           2 |
| `["gemm", "mul", "xf", "true", "32"]`    |   5.531 μs (5%) |         |   48 bytes (1%) |           2 |
| `["gemm", "mul", "xf", "true", "8"]`     | 498.980 ns (5%) |         |   48 bytes (1%) |           2 |
| `["groupby", "sum", "sac"]`              | 154.282 μs (5%) |         | 157.84 KiB (1%) |       10019 |
| `["groupby", "sum", "xf-with-init"]`     | 170.350 μs (5%) |         | 157.44 KiB (1%) |       10008 |
| `["groupby", "sum", "xf-without-init"]`  | 168.656 μs (5%) |         | 157.44 KiB (1%) |       10008 |
| `["mapcat_eduction", "base"]`            |   1.926 μs (5%) |         |                 |             |
| `["mapcat_eduction", "xf-eduction"]`     |   1.782 μs (5%) |         |                 |             |
| `["mapcat_eduction", "xf-xf"]`           |   1.689 μs (5%) |         |                 |             |
| `["missing_argmax", "man"]`              |   2.368 μs (5%) |         |   32 bytes (1%) |           1 |
| `["missing_argmax", "rf"]`               |   2.846 μs (5%) |         |   32 bytes (1%) |           1 |
| `["missing_argmax", "xf"]`               |   2.281 μs (5%) |         |   32 bytes (1%) |           1 |
| `["missing_dot", "equiv"]`               |   1.533 μs (5%) |         |   16 bytes (1%) |           1 |
| `["missing_dot", "man"]`                 |   1.371 μs (5%) |         |   16 bytes (1%) |           1 |
| `["missing_dot", "naive"]`               |   4.315 μs (5%) |         |   16 bytes (1%) |           1 |
| `["missing_dot", "rf"]`                  |   1.239 μs (5%) |         |   16 bytes (1%) |           1 |
| `["missing_dot", "rf_nota"]`             |   1.463 μs (5%) |         |   16 bytes (1%) |           1 |
| `["missing_dot", "xf"]`                  | 184.129 μs (5%) |         |  72.38 KiB (1%) |        3752 |
| `["missing_dot", "xf_nota"]`             | 185.517 μs (5%) |         |  72.16 KiB (1%) |        3744 |
| `["overhead", "foldl"]`                  |   4.150 ns (5%) |         |                 |             |
| `["overhead", "reduce_basecase"]`        | 237.931 ns (5%) |         |  464 bytes (1%) |           9 |
| `["partition_by", "man"]`                |   1.796 ms (5%) |         |  352 bytes (1%) |           4 |
| `["partition_by", "xf"]`                 |   2.841 ms (5%) |         |   6.10 MiB (1%) |      200007 |
| `["set", "base"]`                        |   4.370 ms (5%) |         |  49.58 KiB (1%) |          18 |
| `["set", "xf"]`                          |   3.956 ms (5%) |         |  49.63 KiB (1%) |          21 |

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
       #1  2800 MHz      11254 s          0 s       1108 s      53725 s          0 s
       #2  2800 MHz      52930 s          0 s       1211 s      12486 s          0 s
       
  Memory: 7.7900238037109375 GB (5705.3046875 MB free)
  Uptime: 671.0 sec
  Load Avg:  1.00146484375  0.9267578125  0.55078125
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-8.0.1 (ORCJIT, skylake)
```

---
# Baseline result
# Benchmark Report for */home/travis/build/JuliaFolds/Transducers.jl*

## Job Properties
* Time of benchmark: 4 Aug 2020 - 1:9
* Package commit: d6f0cd
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
| `["append!!", "eduction"]`               |  18.739 μs (5%) |         |  64.72 KiB (1%) |          18 |
| `["append!!", "xf"]`                     |  18.685 μs (5%) |         |  64.72 KiB (1%) |          18 |
| `["cat", "base"]`                        |   1.635 μs (5%) |         |                 |             |
| `["cat", "xf"]`                          |   1.746 μs (5%) |         |                 |             |
| `["collect", "filter-missing"]`          | 103.731 μs (5%) |         | 345.31 KiB (1%) |       10015 |
| `["collect", "identity-float"]`          |  90.129 μs (5%) |         | 569.16 KiB (1%) |       10015 |
| `["collect", "identity-union"]`          | 303.361 μs (5%) |         | 705.22 KiB (1%) |       16673 |
| `["dict", "base"]`                       |   3.578 ms (5%) |         |  92.91 KiB (1%) |          22 |
| `["dict", "xf"]`                         |   3.686 ms (5%) |         |  92.36 KiB (1%) |          21 |
| `["dot", "blas"]`                        |   1.230 μs (5%) |         |                 |             |
| `["dot", "man"]`                         |   1.206 μs (5%) |         |                 |             |
| `["dot", "rf"]`                          |   2.159 μs (5%) |         |                 |             |
| `["dot", "xf"]`                          |   2.266 μs (5%) |         |   64 bytes (1%) |           3 |
| `["filter_map_map!", "man"]`             |  66.053 μs (5%) |         |                 |             |
| `["filter_map_map!", "xf"]`              | 666.274 μs (5%) |         |  304 bytes (1%) |          17 |
| `["filter_map_reduce", "man"]`           | 202.760 μs (5%) |         |                 |             |
| `["filter_map_reduce", "xf"]`            | 203.937 μs (5%) |         |                 |             |
| `["findall", "base"]`                    | 839.163 μs (5%) |         |   2.00 MiB (1%) |          21 |
| `["findall", "xf-array"]`                | 768.723 μs (5%) |         |   3.04 MiB (1%) |       99661 |
| `["findall", "xf-iter"]`                 |   3.180 ms (5%) |         |   9.63 MiB (1%) |      299922 |
| `["gemm", "fusedmul", "blas", "16"]`     |   5.431 ms (5%) |         |                 |             |
| `["gemm", "fusedmul", "blas", "2"]`      |   3.935 ms (5%) |         |                 |             |
| `["gemm", "fusedmul", "blas", "32"]`     |   7.875 ms (5%) |         |                 |             |
| `["gemm", "fusedmul", "blas", "8"]`      |   4.362 ms (5%) |         |                 |             |
| `["gemm", "fusedmul", "xf", "16"]`       |   4.757 ms (5%) |         |  160 bytes (1%) |           6 |
| `["gemm", "fusedmul", "xf", "2"]`        | 547.669 μs (5%) |         |  160 bytes (1%) |           6 |
| `["gemm", "fusedmul", "xf", "32"]`       |   9.234 ms (5%) |         |  160 bytes (1%) |           6 |
| `["gemm", "fusedmul", "xf", "8"]`        |   2.321 ms (5%) |         |  160 bytes (1%) |           6 |
| `["gemm", "mul", "linalg", "256"]`       | 964.085 μs (5%) |         |                 |             |
| `["gemm", "mul", "linalg", "32"]`        |   3.452 μs (5%) |         |                 |             |
| `["gemm", "mul", "linalg", "8"]`         | 305.000 ns (5%) |         |                 |             |
| `["gemm", "mul", "man", "false", "256"]` |   1.916 ms (5%) |         |                 |             |
| `["gemm", "mul", "man", "false", "32"]`  |   5.178 μs (5%) |         |                 |             |
| `["gemm", "mul", "man", "false", "8"]`   | 415.000 ns (5%) |         |                 |             |
| `["gemm", "mul", "man", "ivdep", "256"]` |   1.945 ms (5%) |         |                 |             |
| `["gemm", "mul", "man", "ivdep", "32"]`  |   4.353 μs (5%) |         |                 |             |
| `["gemm", "mul", "man", "ivdep", "8"]`   | 429.000 ns (5%) |         |                 |             |
| `["gemm", "mul", "man", "true", "256"]`  |   1.923 ms (5%) |         |                 |             |
| `["gemm", "mul", "man", "true", "32"]`   |   5.187 μs (5%) |         |                 |             |
| `["gemm", "mul", "man", "true", "8"]`    | 448.000 ns (5%) |         |                 |             |
| `["gemm", "mul", "xf", "false", "256"]`  |   1.916 ms (5%) |         |   48 bytes (1%) |           2 |
| `["gemm", "mul", "xf", "false", "32"]`   |   6.277 μs (5%) |         |   48 bytes (1%) |           2 |
| `["gemm", "mul", "xf", "false", "8"]`    | 398.000 ns (5%) |         |   48 bytes (1%) |           2 |
| `["gemm", "mul", "xf", "ivdep", "256"]`  |   1.942 ms (5%) |         |   48 bytes (1%) |           2 |
| `["gemm", "mul", "xf", "ivdep", "32"]`   |   4.470 μs (5%) |         |   48 bytes (1%) |           2 |
| `["gemm", "mul", "xf", "ivdep", "8"]`    | 377.000 ns (5%) |         |   48 bytes (1%) |           2 |
| `["gemm", "mul", "xf", "true", "256"]`   |   1.909 ms (5%) |         |   48 bytes (1%) |           2 |
| `["gemm", "mul", "xf", "true", "32"]`    |   5.136 μs (5%) |         |   48 bytes (1%) |           2 |
| `["gemm", "mul", "xf", "true", "8"]`     | 407.000 ns (5%) |         |   48 bytes (1%) |           2 |
| `["groupby", "sum", "sac"]`              | 246.956 μs (5%) |         | 313.14 KiB (1%) |       10007 |
| `["groupby", "sum", "xf-with-init"]`     | 177.489 μs (5%) |         | 157.44 KiB (1%) |       10008 |
| `["groupby", "sum", "xf-without-init"]`  | 182.260 μs (5%) |         | 157.44 KiB (1%) |       10008 |
| `["mapcat_eduction", "base"]`            |   1.929 μs (5%) |         |                 |             |
| `["mapcat_eduction", "xf-eduction"]`     |   1.684 μs (5%) |         |                 |             |
| `["mapcat_eduction", "xf-xf"]`           |   1.682 μs (5%) |         |                 |             |
| `["missing_argmax", "man"]`              |   2.368 μs (5%) |         |   32 bytes (1%) |           1 |
| `["missing_argmax", "rf"]`               |   2.288 μs (5%) |         |   32 bytes (1%) |           1 |
| `["missing_argmax", "xf"]`               |   2.857 μs (5%) |         |   32 bytes (1%) |           1 |
| `["missing_dot", "equiv"]`               |   1.527 μs (5%) |         |   16 bytes (1%) |           1 |
| `["missing_dot", "man"]`                 |   1.306 μs (5%) |         |   16 bytes (1%) |           1 |
| `["missing_dot", "naive"]`               |   4.401 μs (5%) |         |   16 bytes (1%) |           1 |
| `["missing_dot", "rf"]`                  |   1.268 μs (5%) |         |   16 bytes (1%) |           1 |
| `["missing_dot", "rf_nota"]`             |   1.534 μs (5%) |         |   16 bytes (1%) |           1 |
| `["missing_dot", "xf"]`                  | 188.148 μs (5%) |         |  72.08 KiB (1%) |        3742 |
| `["missing_dot", "xf_nota"]`             | 189.175 μs (5%) |         |  72.36 KiB (1%) |        3752 |
| `["overhead", "foldl"]`                  |   4.153 ns (5%) |         |                 |             |
| `["overhead", "reduce_basecase"]`        | 241.588 ns (5%) |         |  464 bytes (1%) |           9 |
| `["partition_by", "man"]`                |   1.835 ms (5%) |         |  352 bytes (1%) |           4 |
| `["partition_by", "xf"]`                 |   2.831 ms (5%) |         |   6.10 MiB (1%) |      200007 |
| `["set", "base"]`                        |   4.314 ms (5%) |         |  49.58 KiB (1%) |          18 |
| `["set", "xf"]`                          |   4.028 ms (5%) |         |  49.63 KiB (1%) |          21 |

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
       #1  2800 MHz      20524 s          0 s       1327 s      74592 s          0 s
       #2  2800 MHz      73642 s          0 s       1514 s      21865 s          0 s
       
  Memory: 7.7900238037109375 GB (5655.08203125 MB free)
  Uptime: 975.0 sec
  Load Avg:  1.11669921875  1.05078125  0.72998046875
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

