# Benchmark result

* Pull request commit: [`8bc8f8354b71b483cb6ea99320d98402148d7402`](https://github.com/JuliaFolds/Transducers.jl/commit/8bc8f8354b71b483cb6ea99320d98402148d7402)
* Pull request: <https://github.com/JuliaFolds/Transducers.jl/pull/385> (Add more specialization hints to the compiler)

# Judge result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmarks:
    - Target: 3 Aug 2020 - 23:34
    - Baseline: 3 Aug 2020 - 23:39
* Package commits:
    - Target: 1c116d
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

| ID                                       | time ratio                   | memory ratio  |
|------------------------------------------|------------------------------|---------------|
| `["dict", "base"]`                       | 0.94 (5%) :white_check_mark: |    1.00 (1%)  |
| `["dot", "blas"]`                        |                1.06 (5%) :x: |    1.00 (1%)  |
| `["dot", "xf"]`                          | 0.93 (5%) :white_check_mark: |    1.00 (1%)  |
| `["findall", "xf-array"]`                | 0.92 (5%) :white_check_mark: | 1.02 (1%) :x: |
| `["gemm", "mul", "man", "false", "8"]`   |                1.16 (5%) :x: |    1.00 (1%)  |
| `["gemm", "mul", "man", "ivdep", "32"]`  | 0.92 (5%) :white_check_mark: |    1.00 (1%)  |
| `["gemm", "mul", "man", "ivdep", "8"]`   |                1.16 (5%) :x: |    1.00 (1%)  |
| `["gemm", "mul", "xf", "ivdep", "8"]`    |                1.13 (5%) :x: |    1.00 (1%)  |
| `["gemm", "mul", "xf", "true", "8"]`     |                1.13 (5%) :x: |    1.00 (1%)  |
| `["groupby", "sum", "xf-with-init"]`     |                1.09 (5%) :x: |    1.00 (1%)  |
| `["missing_dot", "man"]`                 |                1.09 (5%) :x: |    1.00 (1%)  |
| `["missing_dot", "naive"]`               |                1.07 (5%) :x: |    1.00 (1%)  |
| `["missing_dot", "rf"]`                  |                1.08 (5%) :x: |    1.00 (1%)  |
| `["overhead", "foldl"]`                  |                1.06 (5%) :x: |    1.00 (1%)  |

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
  uname: Linux 5.3.0-1032-azure #33~18.04.1-Ubuntu SMP Fri Jun 26 15:01:15 UTC 2020 x86_64 x86_64
  CPU: Intel(R) Xeon(R) CPU E5-2673 v4 @ 2.30GHz: 
              speed         user         nice          sys         idle          irq
       #1  2294 MHz      14174 s          0 s       1548 s      63890 s          0 s
       #2  2294 MHz      59505 s          0 s       1828 s      18039 s          0 s
       
  Memory: 6.764884948730469 GB (2890.40625 MB free)
  Uptime: 814.0 sec
  Load Avg:  1.02197265625  1.0  0.67626953125
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
  uname: Linux 5.3.0-1032-azure #33~18.04.1-Ubuntu SMP Fri Jun 26 15:01:15 UTC 2020 x86_64 x86_64
  CPU: Intel(R) Xeon(R) CPU E5-2673 v4 @ 2.30GHz: 
              speed         user         nice          sys         idle          irq
       #1  2294 MHz      27129 s          0 s       1726 s      81204 s          0 s
       #2  2294 MHz      76894 s          0 s       1985 s      30923 s          0 s
       
  Memory: 6.764884948730469 GB (2691.30078125 MB free)
  Uptime: 1120.0 sec
  Load Avg:  1.0  1.0  0.77880859375
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-8.0.1 (ORCJIT, broadwell)
```

---
# Target result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmark: 3 Aug 2020 - 23:34
* Package commit: 1c116d
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
| `["append!!", "eduction"]`               |  22.301 μs (5%) |         |  64.72 KiB (1%) |          18 |
| `["append!!", "xf"]`                     |  22.600 μs (5%) |         |  64.72 KiB (1%) |          18 |
| `["cat", "base"]`                        |   1.750 μs (5%) |         |                 |             |
| `["cat", "xf"]`                          |   2.033 μs (5%) |         |                 |             |
| `["collect", "filter-missing"]`          | 114.600 μs (5%) |         | 345.31 KiB (1%) |       10015 |
| `["collect", "identity-float"]`          |  92.301 μs (5%) |         | 569.16 KiB (1%) |       10015 |
| `["collect", "identity-union"]`          | 354.302 μs (5%) |         | 705.53 KiB (1%) |       16689 |
| `["dict", "base"]`                       |   5.103 ms (5%) |         |  92.91 KiB (1%) |          22 |
| `["dict", "xf"]`                         |   5.054 ms (5%) |         |  92.36 KiB (1%) |          21 |
| `["dot", "blas"]`                        |   2.444 μs (5%) |         |                 |             |
| `["dot", "man"]`                         |   2.467 μs (5%) |         |                 |             |
| `["dot", "rf"]`                          |   3.325 μs (5%) |         |                 |             |
| `["dot", "xf"]`                          |   3.288 μs (5%) |         |   64 bytes (1%) |           3 |
| `["filter_map_map!", "man"]`             |  76.800 μs (5%) |         |                 |             |
| `["filter_map_map!", "xf"]`              | 680.902 μs (5%) |         |  304 bytes (1%) |          17 |
| `["filter_map_reduce", "man"]`           | 242.001 μs (5%) |         |                 |             |
| `["filter_map_reduce", "xf"]`            | 234.202 μs (5%) |         |                 |             |
| `["findall", "base"]`                    |   1.005 ms (5%) |         |   2.00 MiB (1%) |          21 |
| `["findall", "xf-array"]`                | 892.005 μs (5%) |         |   3.03 MiB (1%) |       99211 |
| `["findall", "xf-iter"]`                 |   4.281 ms (5%) |         |   9.63 MiB (1%) |      299927 |
| `["gemm", "fusedmul", "blas", "16"]`     |   5.819 ms (5%) |         |                 |             |
| `["gemm", "fusedmul", "blas", "2"]`      |   4.067 ms (5%) |         |                 |             |
| `["gemm", "fusedmul", "blas", "32"]`     |   8.346 ms (5%) |         |                 |             |
| `["gemm", "fusedmul", "blas", "8"]`      |   4.385 ms (5%) |         |                 |             |
| `["gemm", "fusedmul", "xf", "16"]`       |   5.448 ms (5%) |         |  160 bytes (1%) |           6 |
| `["gemm", "fusedmul", "xf", "2"]`        | 682.103 μs (5%) |         |  160 bytes (1%) |           6 |
| `["gemm", "fusedmul", "xf", "32"]`       |  11.361 ms (5%) |         |  160 bytes (1%) |           6 |
| `["gemm", "fusedmul", "xf", "8"]`        |   2.802 ms (5%) |         |  160 bytes (1%) |           6 |
| `["gemm", "mul", "linalg", "256"]`       |   1.411 ms (5%) |         |                 |             |
| `["gemm", "mul", "linalg", "32"]`        |   4.386 μs (5%) |         |                 |             |
| `["gemm", "mul", "linalg", "8"]`         | 396.487 ns (5%) |         |                 |             |
| `["gemm", "mul", "man", "false", "256"]` |   4.877 ms (5%) |         |                 |             |
| `["gemm", "mul", "man", "false", "32"]`  |   7.725 μs (5%) |         |                 |             |
| `["gemm", "mul", "man", "false", "8"]`   | 465.816 ns (5%) |         |                 |             |
| `["gemm", "mul", "man", "ivdep", "256"]` |   4.823 ms (5%) |         |                 |             |
| `["gemm", "mul", "man", "ivdep", "32"]`  |   6.540 μs (5%) |         |                 |             |
| `["gemm", "mul", "man", "ivdep", "8"]`   | 464.975 ns (5%) |         |                 |             |
| `["gemm", "mul", "man", "true", "256"]`  |   4.857 ms (5%) |         |                 |             |
| `["gemm", "mul", "man", "true", "32"]`   |   7.925 μs (5%) |         |                 |             |
| `["gemm", "mul", "man", "true", "8"]`    | 418.692 ns (5%) |         |                 |             |
| `["gemm", "mul", "xf", "false", "256"]`  |   4.872 ms (5%) |         |   48 bytes (1%) |           2 |
| `["gemm", "mul", "xf", "false", "32"]`   |   8.133 μs (5%) |         |   48 bytes (1%) |           2 |
| `["gemm", "mul", "xf", "false", "8"]`    | 497.396 ns (5%) |         |   48 bytes (1%) |           2 |
| `["gemm", "mul", "xf", "ivdep", "256"]`  |   4.811 ms (5%) |         |   48 bytes (1%) |           2 |
| `["gemm", "mul", "xf", "ivdep", "32"]`   |   6.540 μs (5%) |         |   48 bytes (1%) |           2 |
| `["gemm", "mul", "xf", "ivdep", "8"]`    | 453.571 ns (5%) |         |   48 bytes (1%) |           2 |
| `["gemm", "mul", "xf", "true", "256"]`   |   4.859 ms (5%) |         |   48 bytes (1%) |           2 |
| `["gemm", "mul", "xf", "true", "32"]`    |   7.800 μs (5%) |         |   48 bytes (1%) |           2 |
| `["gemm", "mul", "xf", "true", "8"]`     | 451.261 ns (5%) |         |   48 bytes (1%) |           2 |
| `["groupby", "sum", "sac"]`              | 264.601 μs (5%) |         | 313.14 KiB (1%) |       10007 |
| `["groupby", "sum", "xf-with-init"]`     | 199.100 μs (5%) |         | 157.44 KiB (1%) |       10008 |
| `["groupby", "sum", "xf-without-init"]`  | 190.001 μs (5%) |         | 157.44 KiB (1%) |       10008 |
| `["mapcat_eduction", "base"]`            |   1.910 μs (5%) |         |                 |             |
| `["mapcat_eduction", "xf-eduction"]`     |   2.011 μs (5%) |         |                 |             |
| `["mapcat_eduction", "xf-xf"]`           |   1.989 μs (5%) |         |                 |             |
| `["missing_argmax", "man"]`              |   1.170 μs (5%) |         |   32 bytes (1%) |           1 |
| `["missing_argmax", "rf"]`               |   2.522 μs (5%) |         |   32 bytes (1%) |           1 |
| `["missing_argmax", "xf"]`               |   2.700 μs (5%) |         |   32 bytes (1%) |           1 |
| `["missing_dot", "equiv"]`               |   1.450 μs (5%) |         |   16 bytes (1%) |           1 |
| `["missing_dot", "man"]`                 |   1.510 μs (5%) |         |   16 bytes (1%) |           1 |
| `["missing_dot", "naive"]`               |   5.050 μs (5%) |         |   16 bytes (1%) |           1 |
| `["missing_dot", "rf"]`                  |   1.380 μs (5%) |         |   16 bytes (1%) |           1 |
| `["missing_dot", "rf_nota"]`             |   1.440 μs (5%) |         |   16 bytes (1%) |           1 |
| `["missing_dot", "xf"]`                  | 240.601 μs (5%) |         |  72.13 KiB (1%) |        3742 |
| `["missing_dot", "xf_nota"]`             | 235.802 μs (5%) |         |  71.80 KiB (1%) |        3728 |
| `["overhead", "foldl"]`                  |   5.200 ns (5%) |         |                 |             |
| `["overhead", "reduce_basecase"]`        | 316.232 ns (5%) |         |  464 bytes (1%) |           9 |
| `["partition_by", "man"]`                |   2.100 ms (5%) |         |  352 bytes (1%) |           4 |
| `["partition_by", "xf"]`                 |   3.399 ms (5%) |         |   6.10 MiB (1%) |      200007 |
| `["set", "base"]`                        |   5.862 ms (5%) |         |  49.58 KiB (1%) |          18 |
| `["set", "xf"]`                          |   5.210 ms (5%) |         |  49.63 KiB (1%) |          21 |

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
  uname: Linux 5.3.0-1032-azure #33~18.04.1-Ubuntu SMP Fri Jun 26 15:01:15 UTC 2020 x86_64 x86_64
  CPU: Intel(R) Xeon(R) CPU E5-2673 v4 @ 2.30GHz: 
              speed         user         nice          sys         idle          irq
       #1  2294 MHz      14174 s          0 s       1548 s      63890 s          0 s
       #2  2294 MHz      59505 s          0 s       1828 s      18039 s          0 s
       
  Memory: 6.764884948730469 GB (2890.40625 MB free)
  Uptime: 814.0 sec
  Load Avg:  1.02197265625  1.0  0.67626953125
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-8.0.1 (ORCJIT, broadwell)
```

---
# Baseline result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmark: 3 Aug 2020 - 23:39
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
| `["append!!", "eduction"]`               |  22.501 μs (5%) |         |  64.72 KiB (1%) |          18 |
| `["append!!", "xf"]`                     |  21.900 μs (5%) |         |  64.72 KiB (1%) |          18 |
| `["cat", "base"]`                        |   1.690 μs (5%) |         |                 |             |
| `["cat", "xf"]`                          |   1.967 μs (5%) |         |                 |             |
| `["collect", "filter-missing"]`          | 119.501 μs (5%) |         | 345.31 KiB (1%) |       10015 |
| `["collect", "identity-float"]`          |  96.900 μs (5%) |         | 569.16 KiB (1%) |       10015 |
| `["collect", "identity-union"]`          | 348.801 μs (5%) |         | 705.28 KiB (1%) |       16677 |
| `["dict", "base"]`                       |   5.429 ms (5%) |         |  92.91 KiB (1%) |          22 |
| `["dict", "xf"]`                         |   5.130 ms (5%) |         |  92.36 KiB (1%) |          21 |
| `["dot", "blas"]`                        |   2.311 μs (5%) |         |                 |             |
| `["dot", "man"]`                         |   2.533 μs (5%) |         |                 |             |
| `["dot", "rf"]`                          |   3.300 μs (5%) |         |                 |             |
| `["dot", "xf"]`                          |   3.525 μs (5%) |         |   64 bytes (1%) |           3 |
| `["filter_map_map!", "man"]`             |  74.701 μs (5%) |         |                 |             |
| `["filter_map_map!", "xf"]`              | 678.605 μs (5%) |         |  304 bytes (1%) |          17 |
| `["filter_map_reduce", "man"]`           | 233.901 μs (5%) |         |                 |             |
| `["filter_map_reduce", "xf"]`            | 233.901 μs (5%) |         |                 |             |
| `["findall", "base"]`                    |   1.047 ms (5%) |         |   2.00 MiB (1%) |          21 |
| `["findall", "xf-array"]`                | 965.603 μs (5%) |         |   2.97 MiB (1%) |       97158 |
| `["findall", "xf-iter"]`                 |   4.242 ms (5%) |         |   9.63 MiB (1%) |      299923 |
| `["gemm", "fusedmul", "blas", "16"]`     |   5.812 ms (5%) |         |                 |             |
| `["gemm", "fusedmul", "blas", "2"]`      |   4.045 ms (5%) |         |                 |             |
| `["gemm", "fusedmul", "blas", "32"]`     |   8.410 ms (5%) |         |                 |             |
| `["gemm", "fusedmul", "blas", "8"]`      |   4.365 ms (5%) |         |                 |             |
| `["gemm", "fusedmul", "xf", "16"]`       |   5.623 ms (5%) |         |  160 bytes (1%) |           6 |
| `["gemm", "fusedmul", "xf", "2"]`        | 675.105 μs (5%) |         |  160 bytes (1%) |           6 |
| `["gemm", "fusedmul", "xf", "32"]`       |  11.248 ms (5%) |         |  160 bytes (1%) |           6 |
| `["gemm", "fusedmul", "xf", "8"]`        |   2.794 ms (5%) |         |  160 bytes (1%) |           6 |
| `["gemm", "mul", "linalg", "256"]`       |   1.403 ms (5%) |         |                 |             |
| `["gemm", "mul", "linalg", "32"]`        |   4.500 μs (5%) |         |                 |             |
| `["gemm", "mul", "linalg", "8"]`         | 400.000 ns (5%) |         |                 |             |
| `["gemm", "mul", "man", "false", "256"]` |   4.956 ms (5%) |         |                 |             |
| `["gemm", "mul", "man", "false", "32"]`  |   7.900 μs (5%) |         |                 |             |
| `["gemm", "mul", "man", "false", "8"]`   | 400.000 ns (5%) |         |                 |             |
| `["gemm", "mul", "man", "ivdep", "256"]` |   4.916 ms (5%) |         |                 |             |
| `["gemm", "mul", "man", "ivdep", "32"]`  |   7.100 μs (5%) |         |                 |             |
| `["gemm", "mul", "man", "ivdep", "8"]`   | 400.000 ns (5%) |         |                 |             |
| `["gemm", "mul", "man", "true", "256"]`  |   4.933 ms (5%) |         |                 |             |
| `["gemm", "mul", "man", "true", "32"]`   |   7.800 μs (5%) |         |                 |             |
| `["gemm", "mul", "man", "true", "8"]`    | 400.000 ns (5%) |         |                 |             |
| `["gemm", "mul", "xf", "false", "256"]`  |   4.959 ms (5%) |         |   48 bytes (1%) |           2 |
| `["gemm", "mul", "xf", "false", "32"]`   |   7.900 μs (5%) |         |   48 bytes (1%) |           2 |
| `["gemm", "mul", "xf", "false", "8"]`    | 500.000 ns (5%) |         |   48 bytes (1%) |           2 |
| `["gemm", "mul", "xf", "ivdep", "256"]`  |   4.905 ms (5%) |         |   48 bytes (1%) |           2 |
| `["gemm", "mul", "xf", "ivdep", "32"]`   |   6.600 μs (5%) |         |   48 bytes (1%) |           2 |
| `["gemm", "mul", "xf", "ivdep", "8"]`    | 400.000 ns (5%) |         |   48 bytes (1%) |           2 |
| `["gemm", "mul", "xf", "true", "256"]`   |   4.963 ms (5%) |         |   48 bytes (1%) |           2 |
| `["gemm", "mul", "xf", "true", "32"]`    |   8.100 μs (5%) |         |   48 bytes (1%) |           2 |
| `["gemm", "mul", "xf", "true", "8"]`     | 400.000 ns (5%) |         |   48 bytes (1%) |           2 |
| `["groupby", "sum", "sac"]`              | 267.302 μs (5%) |         | 313.14 KiB (1%) |       10007 |
| `["groupby", "sum", "xf-with-init"]`     | 182.601 μs (5%) |         | 157.44 KiB (1%) |       10008 |
| `["groupby", "sum", "xf-without-init"]`  | 185.001 μs (5%) |         | 157.44 KiB (1%) |       10008 |
| `["mapcat_eduction", "base"]`            |   1.910 μs (5%) |         |                 |             |
| `["mapcat_eduction", "xf-eduction"]`     |   2.067 μs (5%) |         |                 |             |
| `["mapcat_eduction", "xf-xf"]`           |   1.922 μs (5%) |         |                 |             |
| `["missing_argmax", "man"]`              |   1.180 μs (5%) |         |   32 bytes (1%) |           1 |
| `["missing_argmax", "rf"]`               |   2.611 μs (5%) |         |   32 bytes (1%) |           1 |
| `["missing_argmax", "xf"]`               |   2.700 μs (5%) |         |   32 bytes (1%) |           1 |
| `["missing_dot", "equiv"]`               |   1.520 μs (5%) |         |   16 bytes (1%) |           1 |
| `["missing_dot", "man"]`                 |   1.390 μs (5%) |         |   16 bytes (1%) |           1 |
| `["missing_dot", "naive"]`               |   4.733 μs (5%) |         |   16 bytes (1%) |           1 |
| `["missing_dot", "rf"]`                  |   1.280 μs (5%) |         |   16 bytes (1%) |           1 |
| `["missing_dot", "rf_nota"]`             |   1.430 μs (5%) |         |   16 bytes (1%) |           1 |
| `["missing_dot", "xf"]`                  | 240.301 μs (5%) |         |  71.84 KiB (1%) |        3729 |
| `["missing_dot", "xf_nota"]`             | 238.300 μs (5%) |         |  72.25 KiB (1%) |        3746 |
| `["overhead", "foldl"]`                  |   4.900 ns (5%) |         |                 |             |
| `["overhead", "reduce_basecase"]`        | 314.474 ns (5%) |         |  464 bytes (1%) |           9 |
| `["partition_by", "man"]`                |   2.139 ms (5%) |         |  352 bytes (1%) |           4 |
| `["partition_by", "xf"]`                 |   3.558 ms (5%) |         |   6.10 MiB (1%) |      200007 |
| `["set", "base"]`                        |   5.899 ms (5%) |         |  49.58 KiB (1%) |          18 |
| `["set", "xf"]`                          |   5.240 ms (5%) |         |  49.63 KiB (1%) |          21 |

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
  uname: Linux 5.3.0-1032-azure #33~18.04.1-Ubuntu SMP Fri Jun 26 15:01:15 UTC 2020 x86_64 x86_64
  CPU: Intel(R) Xeon(R) CPU E5-2673 v4 @ 2.30GHz: 
              speed         user         nice          sys         idle          irq
       #1  2294 MHz      27129 s          0 s       1726 s      81204 s          0 s
       #2  2294 MHz      76894 s          0 s       1985 s      30923 s          0 s
       
  Memory: 6.764884948730469 GB (2691.30078125 MB free)
  Uptime: 1120.0 sec
  Load Avg:  1.0  1.0  0.77880859375
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
    CPU MHz:             2294.686
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

