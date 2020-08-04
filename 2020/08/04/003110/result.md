# Benchmark result (via Travis)


# Judge result
# Benchmark Report for */home/travis/build/JuliaFolds/Transducers.jl*

## Job Properties
* Time of benchmarks:
    - Target: 4 Aug 2020 - 00:25
    - Baseline: 4 Aug 2020 - 00:30
* Package commits:
    - Target: 21d6eb
    - Baseline: 84af4e
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
| `["append!!", "xf"]`                     |                1.10 (5%) :x: |                   1.00 (1%)  |
| `["cat", "xf"]`                          | 0.86 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["collect", "identity-float"]`          |                1.10 (5%) :x: |                   1.00 (1%)  |
| `["filter_map_map!", "xf"]`              |                1.07 (5%) :x: |                   1.00 (1%)  |
| `["findall", "base"]`                    |                1.07 (5%) :x: |                   1.00 (1%)  |
| `["findall", "xf-array"]`                |                   0.97 (5%)  | 0.96 (1%) :white_check_mark: |
| `["findall", "xf-iter"]`                 | 0.30 (5%) :white_check_mark: | 0.52 (1%) :white_check_mark: |
| `["gemm", "fusedmul", "blas", "16"]`     |                1.07 (5%) :x: |                   1.00 (1%)  |
| `["gemm", "fusedmul", "blas", "2"]`      |                1.05 (5%) :x: |                   1.00 (1%)  |
| `["gemm", "fusedmul", "xf", "32"]`       |                1.21 (5%) :x: |                   1.00 (1%)  |
| `["gemm", "mul", "linalg", "8"]`         | 0.82 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["gemm", "mul", "man", "false", "256"]` |                1.12 (5%) :x: |                   1.00 (1%)  |
| `["gemm", "mul", "man", "false", "32"]`  |                1.18 (5%) :x: |                   1.00 (1%)  |
| `["gemm", "mul", "man", "false", "8"]`   |                1.12 (5%) :x: |                   1.00 (1%)  |
| `["gemm", "mul", "man", "ivdep", "256"]` |                1.08 (5%) :x: |                   1.00 (1%)  |
| `["gemm", "mul", "man", "ivdep", "8"]`   | 0.82 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["gemm", "mul", "man", "true", "256"]`  |                1.10 (5%) :x: |                   1.00 (1%)  |
| `["gemm", "mul", "man", "true", "8"]`    |                1.18 (5%) :x: |                   1.00 (1%)  |
| `["gemm", "mul", "xf", "false", "256"]`  |                1.11 (5%) :x: |                   1.00 (1%)  |
| `["gemm", "mul", "xf", "false", "32"]`   |                1.27 (5%) :x: |                   1.00 (1%)  |
| `["gemm", "mul", "xf", "false", "8"]`    | 0.78 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["gemm", "mul", "xf", "ivdep", "256"]`  |                1.06 (5%) :x: |                   1.00 (1%)  |
| `["gemm", "mul", "xf", "ivdep", "32"]`   | 0.94 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["gemm", "mul", "xf", "ivdep", "8"]`    |                1.15 (5%) :x: |                   1.00 (1%)  |
| `["gemm", "mul", "xf", "true", "256"]`   |                1.10 (5%) :x: |                   1.00 (1%)  |
| `["gemm", "mul", "xf", "true", "8"]`     | 0.92 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["groupby", "sum", "xf-with-init"]`     | 0.93 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["mapcat_eduction", "base"]`            |                1.07 (5%) :x: |                   1.00 (1%)  |
| `["mapcat_eduction", "xf-eduction"]`     | 0.94 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["missing_argmax", "rf"]`               |                1.24 (5%) :x: |                   1.00 (1%)  |
| `["overhead", "foldl"]`                  |                1.07 (5%) :x: |                   1.00 (1%)  |

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
       #1  2800 MHz       7623 s          0 s       1121 s      58119 s          0 s
       #2  2800 MHz      57258 s          0 s       1213 s       8644 s          0 s
       
  Memory: 7.790031433105469 GB (5676.98046875 MB free)
  Uptime: 679.0 sec
  Load Avg:  1.0  0.931640625  0.5712890625
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
       #1  2800 MHz      14268 s          0 s       1244 s      78158 s          0 s
       #2  2800 MHz      77380 s          0 s       1314 s      15262 s          0 s
       
  Memory: 7.790031433105469 GB (5748.35546875 MB free)
  Uptime: 948.0 sec
  Load Avg:  1.0107421875  1.0009765625  0.70849609375
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-8.0.1 (ORCJIT, skylake)
```

---
# Target result
# Benchmark Report for */home/travis/build/JuliaFolds/Transducers.jl*

## Job Properties
* Time of benchmark: 4 Aug 2020 - 0:25
* Package commit: 21d6eb
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
| `["append!!", "eduction"]`               |  18.827 μs (5%) |         |  64.72 KiB (1%) |          18 |
| `["append!!", "xf"]`                     |  18.987 μs (5%) |         |  64.72 KiB (1%) |          18 |
| `["cat", "base"]`                        |   1.554 μs (5%) |         |                 |             |
| `["cat", "xf"]`                          |   1.774 μs (5%) |         |                 |             |
| `["collect", "filter-missing"]`          | 102.511 μs (5%) |         | 345.31 KiB (1%) |       10015 |
| `["collect", "identity-float"]`          |  89.817 μs (5%) |         | 569.16 KiB (1%) |       10015 |
| `["collect", "identity-union"]`          | 301.393 μs (5%) |         | 704.78 KiB (1%) |       16643 |
| `["dict", "base"]`                       |   3.607 ms (5%) |         |  92.91 KiB (1%) |          22 |
| `["dict", "xf"]`                         |   3.688 ms (5%) |         |  92.36 KiB (1%) |          21 |
| `["dot", "blas"]`                        |   1.214 μs (5%) |         |                 |             |
| `["dot", "man"]`                         |   1.206 μs (5%) |         |                 |             |
| `["dot", "rf"]`                          |   2.146 μs (5%) |         |                 |             |
| `["dot", "xf"]`                          |   2.277 μs (5%) |         |   64 bytes (1%) |           3 |
| `["filter_map_map!", "man"]`             |  75.575 μs (5%) |         |                 |             |
| `["filter_map_map!", "xf"]`              | 668.538 μs (5%) |         |  304 bytes (1%) |          17 |
| `["filter_map_reduce", "man"]`           | 203.685 μs (5%) |         |                 |             |
| `["filter_map_reduce", "xf"]`            | 203.801 μs (5%) |         |                 |             |
| `["findall", "base"]`                    | 832.784 μs (5%) |         |   2.00 MiB (1%) |          21 |
| `["findall", "xf-array"]`                | 740.664 μs (5%) |         |   2.92 MiB (1%) |       95685 |
| `["findall", "xf-iter"]`                 | 906.851 μs (5%) |         |   5.05 MiB (1%) |       99929 |
| `["gemm", "fusedmul", "blas", "16"]`     |   5.306 ms (5%) |         |                 |             |
| `["gemm", "fusedmul", "blas", "2"]`      |   3.883 ms (5%) |         |                 |             |
| `["gemm", "fusedmul", "blas", "32"]`     |   7.444 ms (5%) |         |                 |             |
| `["gemm", "fusedmul", "blas", "8"]`      |   4.271 ms (5%) |         |                 |             |
| `["gemm", "fusedmul", "xf", "16"]`       |   4.694 ms (5%) |         |  160 bytes (1%) |           6 |
| `["gemm", "fusedmul", "xf", "2"]`        | 601.170 μs (5%) |         |  160 bytes (1%) |           6 |
| `["gemm", "fusedmul", "xf", "32"]`       |  10.028 ms (5%) |         |  160 bytes (1%) |           6 |
| `["gemm", "fusedmul", "xf", "8"]`        |   2.371 ms (5%) |         |  160 bytes (1%) |           6 |
| `["gemm", "mul", "linalg", "256"]`       | 956.748 μs (5%) |         |                 |             |
| `["gemm", "mul", "linalg", "32"]`        |   3.331 μs (5%) |         |                 |             |
| `["gemm", "mul", "linalg", "8"]`         | 248.115 ns (5%) |         |                 |             |
| `["gemm", "mul", "man", "false", "256"]` |   2.075 ms (5%) |         |                 |             |
| `["gemm", "mul", "man", "false", "32"]`  |   5.750 μs (5%) |         |                 |             |
| `["gemm", "mul", "man", "false", "8"]`   | 449.540 ns (5%) |         |                 |             |
| `["gemm", "mul", "man", "ivdep", "256"]` |   2.043 ms (5%) |         |                 |             |
| `["gemm", "mul", "man", "ivdep", "32"]`  |   4.534 μs (5%) |         |                 |             |
| `["gemm", "mul", "man", "ivdep", "8"]`   | 394.567 ns (5%) |         |                 |             |
| `["gemm", "mul", "man", "true", "256"]`  |   2.060 ms (5%) |         |                 |             |
| `["gemm", "mul", "man", "true", "32"]`   |   5.110 μs (5%) |         |                 |             |
| `["gemm", "mul", "man", "true", "8"]`    | 506.492 ns (5%) |         |                 |             |
| `["gemm", "mul", "xf", "false", "256"]`  |   2.066 ms (5%) |         |   48 bytes (1%) |           2 |
| `["gemm", "mul", "xf", "false", "32"]`   |   6.195 μs (5%) |         |   48 bytes (1%) |           2 |
| `["gemm", "mul", "xf", "false", "8"]`    | 391.425 ns (5%) |         |   48 bytes (1%) |           2 |
| `["gemm", "mul", "xf", "ivdep", "256"]`  |   2.029 ms (5%) |         |   48 bytes (1%) |           2 |
| `["gemm", "mul", "xf", "ivdep", "32"]`   |   4.380 μs (5%) |         |   48 bytes (1%) |           2 |
| `["gemm", "mul", "xf", "ivdep", "8"]`    | 467.472 ns (5%) |         |   48 bytes (1%) |           2 |
| `["gemm", "mul", "xf", "true", "256"]`   |   2.046 ms (5%) |         |   48 bytes (1%) |           2 |
| `["gemm", "mul", "xf", "true", "32"]`    |   5.789 μs (5%) |         |   48 bytes (1%) |           2 |
| `["gemm", "mul", "xf", "true", "8"]`     | 393.280 ns (5%) |         |   48 bytes (1%) |           2 |
| `["groupby", "sum", "sac"]`              | 229.048 μs (5%) |         | 313.14 KiB (1%) |       10007 |
| `["groupby", "sum", "xf-with-init"]`     | 161.531 μs (5%) |         | 157.44 KiB (1%) |       10008 |
| `["groupby", "sum", "xf-without-init"]`  | 166.441 μs (5%) |         | 157.44 KiB (1%) |       10008 |
| `["mapcat_eduction", "base"]`            |   2.050 μs (5%) |         |                 |             |
| `["mapcat_eduction", "xf-eduction"]`     |   1.678 μs (5%) |         |                 |             |
| `["mapcat_eduction", "xf-xf"]`           |   1.781 μs (5%) |         |                 |             |
| `["missing_argmax", "man"]`              |   2.367 μs (5%) |         |   32 bytes (1%) |           1 |
| `["missing_argmax", "rf"]`               |   2.868 μs (5%) |         |   32 bytes (1%) |           1 |
| `["missing_argmax", "xf"]`               |   2.319 μs (5%) |         |   32 bytes (1%) |           1 |
| `["missing_dot", "equiv"]`               |   1.553 μs (5%) |         |   16 bytes (1%) |           1 |
| `["missing_dot", "man"]`                 |   1.247 μs (5%) |         |   16 bytes (1%) |           1 |
| `["missing_dot", "naive"]`               |   4.328 μs (5%) |         |   16 bytes (1%) |           1 |
| `["missing_dot", "rf"]`                  |   1.325 μs (5%) |         |   16 bytes (1%) |           1 |
| `["missing_dot", "rf_nota"]`             |   1.580 μs (5%) |         |   16 bytes (1%) |           1 |
| `["missing_dot", "xf"]`                  | 189.051 μs (5%) |         |  72.09 KiB (1%) |        3742 |
| `["missing_dot", "xf_nota"]`             | 190.176 μs (5%) |         |  72.05 KiB (1%) |        3740 |
| `["overhead", "foldl"]`                  |   4.737 ns (5%) |         |                 |             |
| `["overhead", "reduce_basecase"]`        | 240.022 ns (5%) |         |  464 bytes (1%) |           9 |
| `["partition_by", "man"]`                |   1.788 ms (5%) |         |  352 bytes (1%) |           4 |
| `["partition_by", "xf"]`                 |   2.774 ms (5%) |         |   6.10 MiB (1%) |      200007 |
| `["set", "base"]`                        |   4.230 ms (5%) |         |  49.58 KiB (1%) |          18 |
| `["set", "xf"]`                          |   3.997 ms (5%) |         |  49.63 KiB (1%) |          21 |

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
       #1  2800 MHz       7623 s          0 s       1121 s      58119 s          0 s
       #2  2800 MHz      57258 s          0 s       1213 s       8644 s          0 s
       
  Memory: 7.790031433105469 GB (5676.98046875 MB free)
  Uptime: 679.0 sec
  Load Avg:  1.0  0.931640625  0.5712890625
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-8.0.1 (ORCJIT, skylake)
```

---
# Baseline result
# Benchmark Report for */home/travis/build/JuliaFolds/Transducers.jl*

## Job Properties
* Time of benchmark: 4 Aug 2020 - 0:30
* Package commit: 84af4e
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
| `["append!!", "eduction"]`               |  17.946 μs (5%) |         |  64.72 KiB (1%) |          18 |
| `["append!!", "xf"]`                     |  17.252 μs (5%) |         |  64.72 KiB (1%) |          18 |
| `["cat", "base"]`                        |   1.527 μs (5%) |         |                 |             |
| `["cat", "xf"]`                          |   2.073 μs (5%) |         |                 |             |
| `["collect", "filter-missing"]`          | 100.360 μs (5%) |         | 345.31 KiB (1%) |       10015 |
| `["collect", "identity-float"]`          |  81.745 μs (5%) |         | 569.16 KiB (1%) |       10015 |
| `["collect", "identity-union"]`          | 289.380 μs (5%) |         | 704.56 KiB (1%) |       16631 |
| `["dict", "base"]`                       |   3.576 ms (5%) |         |  92.91 KiB (1%) |          22 |
| `["dict", "xf"]`                         |   3.691 ms (5%) |         |  92.36 KiB (1%) |          21 |
| `["dot", "blas"]`                        |   1.218 μs (5%) |         |                 |             |
| `["dot", "man"]`                         |   1.197 μs (5%) |         |                 |             |
| `["dot", "rf"]`                          |   2.203 μs (5%) |         |                 |             |
| `["dot", "xf"]`                          |   2.270 μs (5%) |         |   64 bytes (1%) |           3 |
| `["filter_map_map!", "man"]`             |  74.700 μs (5%) |         |                 |             |
| `["filter_map_map!", "xf"]`              | 622.981 μs (5%) |         |  304 bytes (1%) |          17 |
| `["filter_map_reduce", "man"]`           | 203.763 μs (5%) |         |                 |             |
| `["filter_map_reduce", "xf"]`            | 202.777 μs (5%) |         |                 |             |
| `["findall", "base"]`                    | 777.636 μs (5%) |         |   2.00 MiB (1%) |          21 |
| `["findall", "xf-array"]`                | 763.644 μs (5%) |         |   3.05 MiB (1%) |      100004 |
| `["findall", "xf-iter"]`                 |   2.998 ms (5%) |         |   9.63 MiB (1%) |      299909 |
| `["gemm", "fusedmul", "blas", "16"]`     |   4.957 ms (5%) |         |                 |             |
| `["gemm", "fusedmul", "blas", "2"]`      |   3.697 ms (5%) |         |                 |             |
| `["gemm", "fusedmul", "blas", "32"]`     |   7.429 ms (5%) |         |                 |             |
| `["gemm", "fusedmul", "blas", "8"]`      |   4.127 ms (5%) |         |                 |             |
| `["gemm", "fusedmul", "xf", "16"]`       |   4.814 ms (5%) |         |  160 bytes (1%) |           6 |
| `["gemm", "fusedmul", "xf", "2"]`        | 584.501 μs (5%) |         |  160 bytes (1%) |           6 |
| `["gemm", "fusedmul", "xf", "32"]`       |   8.294 ms (5%) |         |  160 bytes (1%) |           6 |
| `["gemm", "fusedmul", "xf", "8"]`        |   2.333 ms (5%) |         |  160 bytes (1%) |           6 |
| `["gemm", "mul", "linalg", "256"]`       | 963.663 μs (5%) |         |                 |             |
| `["gemm", "mul", "linalg", "32"]`        |   3.196 μs (5%) |         |                 |             |
| `["gemm", "mul", "linalg", "8"]`         | 302.000 ns (5%) |         |                 |             |
| `["gemm", "mul", "man", "false", "256"]` |   1.853 ms (5%) |         |                 |             |
| `["gemm", "mul", "man", "false", "32"]`  |   4.891 μs (5%) |         |                 |             |
| `["gemm", "mul", "man", "false", "8"]`   | 400.000 ns (5%) |         |                 |             |
| `["gemm", "mul", "man", "ivdep", "256"]` |   1.886 ms (5%) |         |                 |             |
| `["gemm", "mul", "man", "ivdep", "32"]`  |   4.465 μs (5%) |         |                 |             |
| `["gemm", "mul", "man", "ivdep", "8"]`   | 480.000 ns (5%) |         |                 |             |
| `["gemm", "mul", "man", "true", "256"]`  |   1.865 ms (5%) |         |                 |             |
| `["gemm", "mul", "man", "true", "32"]`   |   5.001 μs (5%) |         |                 |             |
| `["gemm", "mul", "man", "true", "8"]`    | 430.000 ns (5%) |         |                 |             |
| `["gemm", "mul", "xf", "false", "256"]`  |   1.855 ms (5%) |         |   48 bytes (1%) |           2 |
| `["gemm", "mul", "xf", "false", "32"]`   |   4.891 μs (5%) |         |   48 bytes (1%) |           2 |
| `["gemm", "mul", "xf", "false", "8"]`    | 499.000 ns (5%) |         |   48 bytes (1%) |           2 |
| `["gemm", "mul", "xf", "ivdep", "256"]`  |   1.917 ms (5%) |         |   48 bytes (1%) |           2 |
| `["gemm", "mul", "xf", "ivdep", "32"]`   |   4.665 μs (5%) |         |   48 bytes (1%) |           2 |
| `["gemm", "mul", "xf", "ivdep", "8"]`    | 408.000 ns (5%) |         |   48 bytes (1%) |           2 |
| `["gemm", "mul", "xf", "true", "256"]`   |   1.859 ms (5%) |         |   48 bytes (1%) |           2 |
| `["gemm", "mul", "xf", "true", "32"]`    |   5.625 μs (5%) |         |   48 bytes (1%) |           2 |
| `["gemm", "mul", "xf", "true", "8"]`     | 427.000 ns (5%) |         |   48 bytes (1%) |           2 |
| `["groupby", "sum", "sac"]`              | 222.337 μs (5%) |         | 313.14 KiB (1%) |       10007 |
| `["groupby", "sum", "xf-with-init"]`     | 174.508 μs (5%) |         | 157.44 KiB (1%) |       10008 |
| `["groupby", "sum", "xf-without-init"]`  | 168.954 μs (5%) |         | 157.44 KiB (1%) |       10008 |
| `["mapcat_eduction", "base"]`            |   1.925 μs (5%) |         |                 |             |
| `["mapcat_eduction", "xf-eduction"]`     |   1.781 μs (5%) |         |                 |             |
| `["mapcat_eduction", "xf-xf"]`           |   1.780 μs (5%) |         |                 |             |
| `["missing_argmax", "man"]`              |   2.367 μs (5%) |         |   32 bytes (1%) |           1 |
| `["missing_argmax", "rf"]`               |   2.318 μs (5%) |         |   32 bytes (1%) |           1 |
| `["missing_argmax", "xf"]`               |   2.293 μs (5%) |         |   32 bytes (1%) |           1 |
| `["missing_dot", "equiv"]`               |   1.488 μs (5%) |         |   16 bytes (1%) |           1 |
| `["missing_dot", "man"]`                 |   1.244 μs (5%) |         |   16 bytes (1%) |           1 |
| `["missing_dot", "naive"]`               |   4.337 μs (5%) |         |   16 bytes (1%) |           1 |
| `["missing_dot", "rf"]`                  |   1.279 μs (5%) |         |   16 bytes (1%) |           1 |
| `["missing_dot", "rf_nota"]`             |   1.578 μs (5%) |         |   16 bytes (1%) |           1 |
| `["missing_dot", "xf"]`                  | 188.114 μs (5%) |         |  72.30 KiB (1%) |        3748 |
| `["missing_dot", "xf_nota"]`             | 188.461 μs (5%) |         |  72.08 KiB (1%) |        3740 |
| `["overhead", "foldl"]`                  |   4.445 ns (5%) |         |                 |             |
| `["overhead", "reduce_basecase"]`        | 233.682 ns (5%) |         |  464 bytes (1%) |           9 |
| `["partition_by", "man"]`                |   1.790 ms (5%) |         |  352 bytes (1%) |           4 |
| `["partition_by", "xf"]`                 |   2.820 ms (5%) |         |   6.10 MiB (1%) |      200007 |
| `["set", "base"]`                        |   4.271 ms (5%) |         |  49.58 KiB (1%) |          18 |
| `["set", "xf"]`                          |   3.994 ms (5%) |         |  49.63 KiB (1%) |          21 |

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
       #1  2800 MHz      14268 s          0 s       1244 s      78158 s          0 s
       #2  2800 MHz      77380 s          0 s       1314 s      15262 s          0 s
       
  Memory: 7.790031433105469 GB (5748.35546875 MB free)
  Uptime: 948.0 sec
  Load Avg:  1.0107421875  1.0009765625  0.70849609375
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
    CPU MHz:               2800.174
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

