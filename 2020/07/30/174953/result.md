# Benchmark result (via Travis)


# Judge result
# Benchmark Report for */home/travis/build/JuliaFolds/Transducers.jl*

## Job Properties
* Time of benchmarks:
    - Target: 30 Jul 2020 - 17:44
    - Baseline: 30 Jul 2020 - 17:49
* Package commits:
    - Target: 4d0f46
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

| ID                                       | time ratio                   | memory ratio |
|------------------------------------------|------------------------------|--------------|
| `["append!!", "eduction"]`               |                1.08 (5%) :x: |   1.00 (1%)  |
| `["append!!", "xf"]`                     |                1.07 (5%) :x: |   1.00 (1%)  |
| `["collect", "identity-float"]`          |                1.06 (5%) :x: |   1.00 (1%)  |
| `["filter_map_map!", "man"]`             |                1.14 (5%) :x: |   1.00 (1%)  |
| `["findall", "xf-iter"]`                 |                1.06 (5%) :x: |   1.00 (1%)  |
| `["gemm", "fusedmul", "blas", "2"]`      |                1.05 (5%) :x: |   1.00 (1%)  |
| `["gemm", "fusedmul", "xf", "16"]`       |                1.06 (5%) :x: |   1.00 (1%)  |
| `["gemm", "fusedmul", "xf", "32"]`       | 0.93 (5%) :white_check_mark: |   1.00 (1%)  |
| `["gemm", "mul", "linalg", "8"]`         | 0.82 (5%) :white_check_mark: |   1.00 (1%)  |
| `["gemm", "mul", "man", "false", "256"]` |                1.10 (5%) :x: |   1.00 (1%)  |
| `["gemm", "mul", "man", "false", "32"]`  |                1.13 (5%) :x: |   1.00 (1%)  |
| `["gemm", "mul", "man", "false", "8"]`   | 0.92 (5%) :white_check_mark: |   1.00 (1%)  |
| `["gemm", "mul", "man", "ivdep", "256"]` |                1.06 (5%) :x: |   1.00 (1%)  |
| `["gemm", "mul", "man", "true", "256"]`  |                1.08 (5%) :x: |   1.00 (1%)  |
| `["gemm", "mul", "man", "true", "32"]`   |                1.13 (5%) :x: |   1.00 (1%)  |
| `["gemm", "mul", "man", "true", "8"]`    |                1.19 (5%) :x: |   1.00 (1%)  |
| `["gemm", "mul", "xf", "false", "256"]`  |                1.09 (5%) :x: |   1.00 (1%)  |
| `["gemm", "mul", "xf", "false", "32"]`   |                1.12 (5%) :x: |   1.00 (1%)  |
| `["gemm", "mul", "xf", "false", "8"]`    |                1.05 (5%) :x: |   1.00 (1%)  |
| `["gemm", "mul", "xf", "ivdep", "256"]`  |                1.05 (5%) :x: |   1.00 (1%)  |
| `["gemm", "mul", "xf", "ivdep", "8"]`    |                1.27 (5%) :x: |   1.00 (1%)  |
| `["gemm", "mul", "xf", "true", "256"]`   |                1.09 (5%) :x: |   1.00 (1%)  |
| `["gemm", "mul", "xf", "true", "32"]`    |                1.13 (5%) :x: |   1.00 (1%)  |
| `["mapcat_eduction", "base"]`            |                1.06 (5%) :x: |   1.00 (1%)  |
| `["mapcat_eduction", "xf-xf"]`           |                1.06 (5%) :x: |   1.00 (1%)  |
| `["missing_argmax", "rf"]`               | 0.81 (5%) :white_check_mark: |   1.00 (1%)  |
| `["missing_argmax", "xf"]`               |                1.24 (5%) :x: |   1.00 (1%)  |
| `["missing_dot", "man"]`                 | 0.95 (5%) :white_check_mark: |   1.00 (1%)  |
| `["missing_dot", "rf"]`                  |                1.08 (5%) :x: |   1.00 (1%)  |
| `["overhead", "foldl"]`                  | 0.88 (5%) :white_check_mark: |   1.00 (1%)  |

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
       #1  2800 MHz       9550 s          0 s       1049 s      53159 s          0 s
       #2  2800 MHz      52367 s          0 s       1136 s      10393 s          0 s
       
  Memory: 7.790031433105469 GB (5804.40625 MB free)
  Uptime: 649.0 sec
  Load Avg:  1.0  0.92138671875  0.5498046875
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
       #1  2800 MHz      34636 s          0 s       1163 s      54363 s          0 s
       #2  2800 MHz      53626 s          0 s       1198 s      35430 s          0 s
       
  Memory: 7.790031433105469 GB (5647.77734375 MB free)
  Uptime: 913.0 sec
  Load Avg:  1.0  0.9755859375  0.6708984375
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-8.0.1 (ORCJIT, skylake)
```

---
# Target result
# Benchmark Report for */home/travis/build/JuliaFolds/Transducers.jl*

## Job Properties
* Time of benchmark: 30 Jul 2020 - 17:44
* Package commit: 4d0f46
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
| `["append!!", "eduction"]`               |  17.039 μs (5%) |         |  64.72 KiB (1%) |          18 |
| `["append!!", "xf"]`                     |  16.897 μs (5%) |         |  64.72 KiB (1%) |          18 |
| `["cat", "base"]`                        |   1.554 μs (5%) |         |                 |             |
| `["cat", "xf"]`                          |   1.772 μs (5%) |         |                 |             |
| `["collect", "filter-missing"]`          |  95.087 μs (5%) |         | 345.31 KiB (1%) |       10015 |
| `["collect", "identity-float"]`          |  74.764 μs (5%) |         | 569.16 KiB (1%) |       10015 |
| `["collect", "identity-union"]`          | 279.816 μs (5%) |         | 705.03 KiB (1%) |       16661 |
| `["dict", "base"]`                       |   3.574 ms (5%) |         |  92.91 KiB (1%) |          22 |
| `["dict", "xf"]`                         |   3.687 ms (5%) |         |  92.36 KiB (1%) |          21 |
| `["dot", "blas"]`                        |   1.211 μs (5%) |         |                 |             |
| `["dot", "man"]`                         |   1.156 μs (5%) |         |                 |             |
| `["dot", "rf"]`                          |   2.203 μs (5%) |         |                 |             |
| `["dot", "xf"]`                          |   2.270 μs (5%) |         |   64 bytes (1%) |           3 |
| `["filter_map_map!", "man"]`             |  75.032 μs (5%) |         |                 |             |
| `["filter_map_map!", "xf"]`              | 669.787 μs (5%) |         |  304 bytes (1%) |          17 |
| `["filter_map_reduce", "man"]`           | 202.973 μs (5%) |         |                 |             |
| `["filter_map_reduce", "xf"]`            | 202.586 μs (5%) |         |                 |             |
| `["findall", "base"]`                    | 737.208 μs (5%) |         |   2.00 MiB (1%) |          21 |
| `["findall", "xf-array"]`                | 695.986 μs (5%) |         |   3.00 MiB (1%) |       98160 |
| `["findall", "xf-iter"]`                 |   3.068 ms (5%) |         |   9.63 MiB (1%) |      299936 |
| `["gemm", "fusedmul", "blas", "16"]`     |   4.704 ms (5%) |         |                 |             |
| `["gemm", "fusedmul", "blas", "2"]`      |   3.404 ms (5%) |         |                 |             |
| `["gemm", "fusedmul", "blas", "32"]`     |   6.540 ms (5%) |         |                 |             |
| `["gemm", "fusedmul", "blas", "8"]`      |   3.750 ms (5%) |         |                 |             |
| `["gemm", "fusedmul", "xf", "16"]`       |   5.311 ms (5%) |         |  160 bytes (1%) |           6 |
| `["gemm", "fusedmul", "xf", "2"]`        | 595.963 μs (5%) |         |  160 bytes (1%) |           6 |
| `["gemm", "fusedmul", "xf", "32"]`       |   9.627 ms (5%) |         |  160 bytes (1%) |           6 |
| `["gemm", "fusedmul", "xf", "8"]`        |   2.399 ms (5%) |         |  160 bytes (1%) |           6 |
| `["gemm", "mul", "linalg", "256"]`       | 956.407 μs (5%) |         |                 |             |
| `["gemm", "mul", "linalg", "32"]`        |   3.334 μs (5%) |         |                 |             |
| `["gemm", "mul", "linalg", "8"]`         | 247.935 ns (5%) |         |                 |             |
| `["gemm", "mul", "man", "false", "256"]` |   2.112 ms (5%) |         |                 |             |
| `["gemm", "mul", "man", "false", "32"]`  |   5.615 μs (5%) |         |                 |             |
| `["gemm", "mul", "man", "false", "8"]`   | 395.633 ns (5%) |         |                 |             |
| `["gemm", "mul", "man", "ivdep", "256"]` |   2.071 ms (5%) |         |                 |             |
| `["gemm", "mul", "man", "ivdep", "32"]`  |   4.544 μs (5%) |         |                 |             |
| `["gemm", "mul", "man", "ivdep", "8"]`   | 394.697 ns (5%) |         |                 |             |
| `["gemm", "mul", "man", "true", "256"]`  |   2.090 ms (5%) |         |                 |             |
| `["gemm", "mul", "man", "true", "32"]`   |   5.825 μs (5%) |         |                 |             |
| `["gemm", "mul", "man", "true", "8"]`    | 506.477 ns (5%) |         |                 |             |
| `["gemm", "mul", "xf", "false", "256"]`  |   2.099 ms (5%) |         |   48 bytes (1%) |           2 |
| `["gemm", "mul", "xf", "false", "32"]`   |   5.121 μs (5%) |         |   48 bytes (1%) |           2 |
| `["gemm", "mul", "xf", "false", "8"]`    | 402.556 ns (5%) |         |   48 bytes (1%) |           2 |
| `["gemm", "mul", "xf", "ivdep", "256"]`  |   2.058 ms (5%) |         |   48 bytes (1%) |           2 |
| `["gemm", "mul", "xf", "ivdep", "32"]`   |   4.399 μs (5%) |         |   48 bytes (1%) |           2 |
| `["gemm", "mul", "xf", "ivdep", "8"]`    | 467.000 ns (5%) |         |   48 bytes (1%) |           2 |
| `["gemm", "mul", "xf", "true", "256"]`   |   2.098 ms (5%) |         |   48 bytes (1%) |           2 |
| `["gemm", "mul", "xf", "true", "32"]`    |   5.532 μs (5%) |         |   48 bytes (1%) |           2 |
| `["gemm", "mul", "xf", "true", "8"]`     | 394.806 ns (5%) |         |   48 bytes (1%) |           2 |
| `["groupby", "sum", "sac"]`              | 243.153 μs (5%) |         | 313.14 KiB (1%) |       10007 |
| `["groupby", "sum", "xf-with-init"]`     | 174.386 μs (5%) |         | 157.44 KiB (1%) |       10008 |
| `["groupby", "sum", "xf-without-init"]`  | 182.802 μs (5%) |         | 157.44 KiB (1%) |       10008 |
| `["mapcat_eduction", "base"]`            |   2.054 μs (5%) |         |                 |             |
| `["mapcat_eduction", "xf-eduction"]`     |   1.682 μs (5%) |         |                 |             |
| `["mapcat_eduction", "xf-xf"]`           |   1.780 μs (5%) |         |                 |             |
| `["missing_argmax", "man"]`              |   2.364 μs (5%) |         |   32 bytes (1%) |           1 |
| `["missing_argmax", "rf"]`               |   2.308 μs (5%) |         |   32 bytes (1%) |           1 |
| `["missing_argmax", "xf"]`               |   2.844 μs (5%) |         |   32 bytes (1%) |           1 |
| `["missing_dot", "equiv"]`               |   1.545 μs (5%) |         |   16 bytes (1%) |           1 |
| `["missing_dot", "man"]`                 |   1.245 μs (5%) |         |   16 bytes (1%) |           1 |
| `["missing_dot", "naive"]`               |   4.363 μs (5%) |         |   16 bytes (1%) |           1 |
| `["missing_dot", "rf"]`                  |   1.325 μs (5%) |         |   16 bytes (1%) |           1 |
| `["missing_dot", "rf_nota"]`             |   1.610 μs (5%) |         |   16 bytes (1%) |           1 |
| `["missing_dot", "xf"]`                  | 184.059 μs (5%) |         |  72.30 KiB (1%) |        3748 |
| `["missing_dot", "xf_nota"]`             | 181.875 μs (5%) |         |  71.75 KiB (1%) |        3724 |
| `["overhead", "foldl"]`                  |   4.148 ns (5%) |         |                 |             |
| `["overhead", "reduce_basecase"]`        | 158.857 ns (5%) |         |  416 bytes (1%) |           7 |
| `["partition_by", "man"]`                |   1.832 ms (5%) |         |  352 bytes (1%) |           4 |
| `["partition_by", "xf"]`                 |   2.684 ms (5%) |         |   6.10 MiB (1%) |      200007 |
| `["set", "base"]`                        |   4.434 ms (5%) |         |  49.58 KiB (1%) |          18 |
| `["set", "xf"]`                          |   3.965 ms (5%) |         |  49.63 KiB (1%) |          21 |

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
       #1  2800 MHz       9550 s          0 s       1049 s      53159 s          0 s
       #2  2800 MHz      52367 s          0 s       1136 s      10393 s          0 s
       
  Memory: 7.790031433105469 GB (5804.40625 MB free)
  Uptime: 649.0 sec
  Load Avg:  1.0  0.92138671875  0.5498046875
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-8.0.1 (ORCJIT, skylake)
```

---
# Baseline result
# Benchmark Report for */home/travis/build/JuliaFolds/Transducers.jl*

## Job Properties
* Time of benchmark: 30 Jul 2020 - 17:49
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
| `["append!!", "eduction"]`               |  15.754 μs (5%) |         |  64.72 KiB (1%) |          18 |
| `["append!!", "xf"]`                     |  15.791 μs (5%) |         |  64.72 KiB (1%) |          18 |
| `["cat", "base"]`                        |   1.632 μs (5%) |         |                 |             |
| `["cat", "xf"]`                          |   1.743 μs (5%) |         |                 |             |
| `["collect", "filter-missing"]`          |  94.013 μs (5%) |         | 345.31 KiB (1%) |       10015 |
| `["collect", "identity-float"]`          |  70.202 μs (5%) |         | 569.16 KiB (1%) |       10015 |
| `["collect", "identity-union"]`          | 293.085 μs (5%) |         | 705.22 KiB (1%) |       16669 |
| `["dict", "base"]`                       |   3.572 ms (5%) |         |  92.91 KiB (1%) |          22 |
| `["dict", "xf"]`                         |   3.685 ms (5%) |         |  92.36 KiB (1%) |          21 |
| `["dot", "blas"]`                        |   1.225 μs (5%) |         |                 |             |
| `["dot", "man"]`                         |   1.196 μs (5%) |         |                 |             |
| `["dot", "rf"]`                          |   2.156 μs (5%) |         |                 |             |
| `["dot", "xf"]`                          |   2.271 μs (5%) |         |   64 bytes (1%) |           3 |
| `["filter_map_map!", "man"]`             |  65.612 μs (5%) |         |                 |             |
| `["filter_map_map!", "xf"]`              | 666.395 μs (5%) |         |  304 bytes (1%) |          17 |
| `["filter_map_reduce", "man"]`           | 202.354 μs (5%) |         |                 |             |
| `["filter_map_reduce", "xf"]`            | 203.376 μs (5%) |         |                 |             |
| `["findall", "base"]`                    | 735.132 μs (5%) |         |   2.00 MiB (1%) |          21 |
| `["findall", "xf-array"]`                | 697.178 μs (5%) |         |   2.98 MiB (1%) |       97695 |
| `["findall", "xf-iter"]`                 |   2.900 ms (5%) |         |   9.63 MiB (1%) |      299923 |
| `["gemm", "fusedmul", "blas", "16"]`     |   4.624 ms (5%) |         |                 |             |
| `["gemm", "fusedmul", "blas", "2"]`      |   3.230 ms (5%) |         |                 |             |
| `["gemm", "fusedmul", "blas", "32"]`     |   6.533 ms (5%) |         |                 |             |
| `["gemm", "fusedmul", "blas", "8"]`      |   3.647 ms (5%) |         |                 |             |
| `["gemm", "fusedmul", "xf", "16"]`       |   5.014 ms (5%) |         |  160 bytes (1%) |           6 |
| `["gemm", "fusedmul", "xf", "2"]`        | 604.401 μs (5%) |         |  160 bytes (1%) |           6 |
| `["gemm", "fusedmul", "xf", "32"]`       |  10.352 ms (5%) |         |  160 bytes (1%) |           6 |
| `["gemm", "fusedmul", "xf", "8"]`        |   2.425 ms (5%) |         |  160 bytes (1%) |           6 |
| `["gemm", "mul", "linalg", "256"]`       | 962.520 μs (5%) |         |                 |             |
| `["gemm", "mul", "linalg", "32"]`        |   3.200 μs (5%) |         |                 |             |
| `["gemm", "mul", "linalg", "8"]`         | 302.000 ns (5%) |         |                 |             |
| `["gemm", "mul", "man", "false", "256"]` |   1.928 ms (5%) |         |                 |             |
| `["gemm", "mul", "man", "false", "32"]`  |   4.960 μs (5%) |         |                 |             |
| `["gemm", "mul", "man", "false", "8"]`   | 431.000 ns (5%) |         |                 |             |
| `["gemm", "mul", "man", "ivdep", "256"]` |   1.948 ms (5%) |         |                 |             |
| `["gemm", "mul", "man", "ivdep", "32"]`  |   4.369 μs (5%) |         |                 |             |
| `["gemm", "mul", "man", "ivdep", "8"]`   | 400.000 ns (5%) |         |                 |             |
| `["gemm", "mul", "man", "true", "256"]`  |   1.939 ms (5%) |         |                 |             |
| `["gemm", "mul", "man", "true", "32"]`   |   5.132 μs (5%) |         |                 |             |
| `["gemm", "mul", "man", "true", "8"]`    | 427.000 ns (5%) |         |                 |             |
| `["gemm", "mul", "xf", "false", "256"]`  |   1.933 ms (5%) |         |   48 bytes (1%) |           2 |
| `["gemm", "mul", "xf", "false", "32"]`   |   4.565 μs (5%) |         |   48 bytes (1%) |           2 |
| `["gemm", "mul", "xf", "false", "8"]`    | 383.000 ns (5%) |         |   48 bytes (1%) |           2 |
| `["gemm", "mul", "xf", "ivdep", "256"]`  |   1.953 ms (5%) |         |   48 bytes (1%) |           2 |
| `["gemm", "mul", "xf", "ivdep", "32"]`   |   4.473 μs (5%) |         |   48 bytes (1%) |           2 |
| `["gemm", "mul", "xf", "ivdep", "8"]`    | 369.000 ns (5%) |         |   48 bytes (1%) |           2 |
| `["gemm", "mul", "xf", "true", "256"]`   |   1.921 ms (5%) |         |   48 bytes (1%) |           2 |
| `["gemm", "mul", "xf", "true", "32"]`    |   4.887 μs (5%) |         |   48 bytes (1%) |           2 |
| `["gemm", "mul", "xf", "true", "8"]`     | 388.000 ns (5%) |         |   48 bytes (1%) |           2 |
| `["groupby", "sum", "sac"]`              | 243.409 μs (5%) |         | 313.14 KiB (1%) |       10007 |
| `["groupby", "sum", "xf-with-init"]`     | 175.165 μs (5%) |         | 157.44 KiB (1%) |       10008 |
| `["groupby", "sum", "xf-without-init"]`  | 183.774 μs (5%) |         | 157.44 KiB (1%) |       10008 |
| `["mapcat_eduction", "base"]`            |   1.940 μs (5%) |         |                 |             |
| `["mapcat_eduction", "xf-eduction"]`     |   1.677 μs (5%) |         |                 |             |
| `["mapcat_eduction", "xf-xf"]`           |   1.677 μs (5%) |         |                 |             |
| `["missing_argmax", "man"]`              |   2.366 μs (5%) |         |   32 bytes (1%) |           1 |
| `["missing_argmax", "rf"]`               |   2.851 μs (5%) |         |   32 bytes (1%) |           1 |
| `["missing_argmax", "xf"]`               |   2.291 μs (5%) |         |   32 bytes (1%) |           1 |
| `["missing_dot", "equiv"]`               |   1.536 μs (5%) |         |   16 bytes (1%) |           1 |
| `["missing_dot", "man"]`                 |   1.314 μs (5%) |         |   16 bytes (1%) |           1 |
| `["missing_dot", "naive"]`               |   4.422 μs (5%) |         |   16 bytes (1%) |           1 |
| `["missing_dot", "rf"]`                  |   1.228 μs (5%) |         |   16 bytes (1%) |           1 |
| `["missing_dot", "rf_nota"]`             |   1.540 μs (5%) |         |   16 bytes (1%) |           1 |
| `["missing_dot", "xf"]`                  | 190.515 μs (5%) |         |  72.13 KiB (1%) |        3741 |
| `["missing_dot", "xf_nota"]`             | 182.626 μs (5%) |         |  72.34 KiB (1%) |        3750 |
| `["overhead", "foldl"]`                  |   4.735 ns (5%) |         |                 |             |
| `["overhead", "reduce_basecase"]`        | 160.917 ns (5%) |         |  416 bytes (1%) |           7 |
| `["partition_by", "man"]`                |   1.789 ms (5%) |         |  352 bytes (1%) |           4 |
| `["partition_by", "xf"]`                 |   2.693 ms (5%) |         |   6.10 MiB (1%) |      200007 |
| `["set", "base"]`                        |   4.330 ms (5%) |         |  49.58 KiB (1%) |          18 |
| `["set", "xf"]`                          |   3.967 ms (5%) |         |  49.63 KiB (1%) |          21 |

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
       #1  2800 MHz      34636 s          0 s       1163 s      54363 s          0 s
       #2  2800 MHz      53626 s          0 s       1198 s      35430 s          0 s
       
  Memory: 7.790031433105469 GB (5647.77734375 MB free)
  Uptime: 913.0 sec
  Load Avg:  1.0  0.9755859375  0.6708984375
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
    CPU MHz:               2800.176
    BogoMIPS:              5600.35
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

