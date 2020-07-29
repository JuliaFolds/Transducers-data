# Benchmark result

* Pull request commit: [`4b07b8bc30c8dfe64ce71acb239af36cd11e2b75`](https://github.com/JuliaFolds/Transducers.jl/commit/4b07b8bc30c8dfe64ce71acb239af36cd11e2b75)
* Pull request: <https://github.com/JuliaFolds/Transducers.jl/pull/385> (Add more specialization hints to the compiler)

# Judge result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmarks:
    - Target: 29 Jul 2020 - 06:02
    - Baseline: 29 Jul 2020 - 06:07
* Package commits:
    - Target: ceb445
    - Baseline: f3056a
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
| `["append!!", "xf"]`                     |                1.06 (5%) :x: |   1.00 (1%)  |
| `["collect", "identity-float"]`          | 0.94 (5%) :white_check_mark: |   1.00 (1%)  |
| `["dict", "base"]`                       |                1.08 (5%) :x: |   1.00 (1%)  |
| `["findall", "base"]`                    |                1.08 (5%) :x: |   1.00 (1%)  |
| `["gemm", "fusedmul", "blas", "16"]`     |                1.06 (5%) :x: |   1.00 (1%)  |
| `["gemm", "fusedmul", "blas", "8"]`      |                1.08 (5%) :x: |   1.00 (1%)  |
| `["gemm", "fusedmul", "xf", "8"]`        |                1.06 (5%) :x: |   1.00 (1%)  |
| `["gemm", "mul", "linalg", "256"]`       |                1.10 (5%) :x: |   1.00 (1%)  |
| `["gemm", "mul", "linalg", "8"]`         |                1.21 (5%) :x: |   1.00 (1%)  |
| `["gemm", "mul", "man", "false", "256"]` |                1.10 (5%) :x: |   1.00 (1%)  |
| `["gemm", "mul", "xf", "false", "8"]`    |                1.37 (5%) :x: |   1.00 (1%)  |
| `["gemm", "mul", "xf", "true", "32"]`    | 0.92 (5%) :white_check_mark: |   1.00 (1%)  |
| `["missing_dot", "equiv"]`               |                1.06 (5%) :x: |   1.00 (1%)  |
| `["missing_dot", "man"]`                 | 0.86 (5%) :white_check_mark: |   1.00 (1%)  |
| `["set", "base"]`                        | 0.94 (5%) :white_check_mark: |   1.00 (1%)  |

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
       #1  2294 MHz      47111 s          0 s       1254 s      53910 s          0 s
       #2  2294 MHz      22256 s          0 s       1884 s      79149 s          0 s
       
  Memory: 6.7648773193359375 GB (2829.49609375 MB free)
  Uptime: 1044.0 sec
  Load Avg:  1.06298828125  0.9775390625  0.6220703125
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
       #1  2294 MHz      72985 s          0 s       1434 s      56859 s          0 s
       #2  2294 MHz      25254 s          0 s       1976 s     105077 s          0 s
       
  Memory: 6.7648773193359375 GB (2649.73828125 MB free)
  Uptime: 1335.0 sec
  Load Avg:  1.02197265625  1.033203125  0.75537109375
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-8.0.1 (ORCJIT, broadwell)
```

---
# Target result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmark: 29 Jul 2020 - 6:2
* Package commit: ceb445
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
| `["append!!", "eduction"]`               |  15.900 μs (5%) |         |  64.72 KiB (1%) |          18 |
| `["append!!", "xf"]`                     |  16.400 μs (5%) |         |  64.72 KiB (1%) |          18 |
| `["cat", "base"]`                        |   1.530 μs (5%) |         |                 |             |
| `["cat", "xf"]`                          |   1.670 μs (5%) |         |                 |             |
| `["collect", "filter-missing"]`          |  88.400 μs (5%) |         | 345.31 KiB (1%) |       10015 |
| `["collect", "identity-float"]`          |  69.901 μs (5%) |         | 569.16 KiB (1%) |       10015 |
| `["collect", "identity-union"]`          | 269.501 μs (5%) |         | 705.11 KiB (1%) |       16666 |
| `["dict", "base"]`                       |   4.569 ms (5%) |         |  92.91 KiB (1%) |          22 |
| `["dict", "xf"]`                         |   4.176 ms (5%) |         |  92.36 KiB (1%) |          21 |
| `["dot", "blas"]`                        |   2.267 μs (5%) |         |                 |             |
| `["dot", "man"]`                         |   2.256 μs (5%) |         |                 |             |
| `["dot", "rf"]`                          |   3.050 μs (5%) |         |                 |             |
| `["dot", "xf"]`                          |   3.138 μs (5%) |         |   64 bytes (1%) |           3 |
| `["filter_map_map!", "man"]`             |  67.301 μs (5%) |         |                 |             |
| `["filter_map_map!", "xf"]`              | 534.408 μs (5%) |         |  304 bytes (1%) |          17 |
| `["filter_map_reduce", "man"]`           | 194.900 μs (5%) |         |                 |             |
| `["filter_map_reduce", "xf"]`            | 194.900 μs (5%) |         |                 |             |
| `["findall", "base"]`                    | 856.004 μs (5%) |         |   2.00 MiB (1%) |          21 |
| `["findall", "xf-array"]`                | 788.304 μs (5%) |         |   3.04 MiB (1%) |       99430 |
| `["findall", "xf-iter"]`                 |   3.306 ms (5%) |         |   9.63 MiB (1%) |      299927 |
| `["gemm", "fusedmul", "blas", "16"]`     |   5.671 ms (5%) |         |                 |             |
| `["gemm", "fusedmul", "blas", "2"]`      |   3.998 ms (5%) |         |                 |             |
| `["gemm", "fusedmul", "blas", "32"]`     |   8.222 ms (5%) |         |                 |             |
| `["gemm", "fusedmul", "blas", "8"]`      |   4.276 ms (5%) |         |                 |             |
| `["gemm", "fusedmul", "xf", "16"]`       |   5.342 ms (5%) |         |  160 bytes (1%) |           6 |
| `["gemm", "fusedmul", "xf", "2"]`        | 627.411 μs (5%) |         |  160 bytes (1%) |           6 |
| `["gemm", "fusedmul", "xf", "32"]`       |  10.858 ms (5%) |         |  160 bytes (1%) |           6 |
| `["gemm", "fusedmul", "xf", "8"]`        |   2.643 ms (5%) |         |  160 bytes (1%) |           6 |
| `["gemm", "mul", "linalg", "256"]`       |   1.339 ms (5%) |         |                 |             |
| `["gemm", "mul", "linalg", "32"]`        |   3.771 μs (5%) |         |                 |             |
| `["gemm", "mul", "linalg", "8"]`         | 362.617 ns (5%) |         |                 |             |
| `["gemm", "mul", "man", "false", "256"]` |   4.781 ms (5%) |         |                 |             |
| `["gemm", "mul", "man", "false", "32"]`  |   7.075 μs (5%) |         |                 |             |
| `["gemm", "mul", "man", "false", "8"]`   | 390.104 ns (5%) |         |                 |             |
| `["gemm", "mul", "man", "ivdep", "256"]` |   4.713 ms (5%) |         |                 |             |
| `["gemm", "mul", "man", "ivdep", "32"]`  |   6.040 μs (5%) |         |                 |             |
| `["gemm", "mul", "man", "ivdep", "8"]`   | 385.577 ns (5%) |         |                 |             |
| `["gemm", "mul", "man", "true", "256"]`  |   4.723 ms (5%) |         |                 |             |
| `["gemm", "mul", "man", "true", "32"]`   |   7.075 μs (5%) |         |                 |             |
| `["gemm", "mul", "man", "true", "8"]`    | 406.005 ns (5%) |         |                 |             |
| `["gemm", "mul", "xf", "false", "256"]`  |   4.779 ms (5%) |         |   48 bytes (1%) |           2 |
| `["gemm", "mul", "xf", "false", "32"]`   |   6.940 μs (5%) |         |   48 bytes (1%) |           2 |
| `["gemm", "mul", "xf", "false", "8"]`    | 409.960 ns (5%) |         |   48 bytes (1%) |           2 |
| `["gemm", "mul", "xf", "ivdep", "256"]`  |   4.746 ms (5%) |         |   48 bytes (1%) |           2 |
| `["gemm", "mul", "xf", "ivdep", "32"]`   |   5.533 μs (5%) |         |   48 bytes (1%) |           2 |
| `["gemm", "mul", "xf", "ivdep", "8"]`    | 394.064 ns (5%) |         |   48 bytes (1%) |           2 |
| `["gemm", "mul", "xf", "true", "256"]`   |   4.781 ms (5%) |         |   48 bytes (1%) |           2 |
| `["gemm", "mul", "xf", "true", "32"]`    |   6.920 μs (5%) |         |   48 bytes (1%) |           2 |
| `["gemm", "mul", "xf", "true", "8"]`     | 399.010 ns (5%) |         |   48 bytes (1%) |           2 |
| `["groupby", "sum", "sac"]`              | 213.403 μs (5%) |         | 313.14 KiB (1%) |       10007 |
| `["groupby", "sum", "xf-with-init"]`     | 156.203 μs (5%) |         | 157.44 KiB (1%) |       10008 |
| `["groupby", "sum", "xf-without-init"]`  | 158.002 μs (5%) |         | 157.44 KiB (1%) |       10008 |
| `["mapcat_eduction", "base"]`            |   1.480 μs (5%) |         |                 |             |
| `["mapcat_eduction", "xf-eduction"]`     |   1.600 μs (5%) |         |                 |             |
| `["mapcat_eduction", "xf-xf"]`           |   1.600 μs (5%) |         |                 |             |
| `["missing_argmax", "man"]`              | 915.385 ns (5%) |         |   32 bytes (1%) |           1 |
| `["missing_argmax", "rf"]`               |   2.111 μs (5%) |         |   32 bytes (1%) |           1 |
| `["missing_argmax", "xf"]`               |   2.133 μs (5%) |         |   32 bytes (1%) |           1 |
| `["missing_dot", "equiv"]`               |   1.053 μs (5%) |         |   16 bytes (1%) |           1 |
| `["missing_dot", "man"]`                 | 928.125 ns (5%) |         |   16 bytes (1%) |           1 |
| `["missing_dot", "naive"]`               |   4.057 μs (5%) |         |   16 bytes (1%) |           1 |
| `["missing_dot", "rf"]`                  | 850.000 ns (5%) |         |   16 bytes (1%) |           1 |
| `["missing_dot", "rf_nota"]`             | 928.571 ns (5%) |         |   16 bytes (1%) |           1 |
| `["missing_dot", "xf"]`                  | 180.000 μs (5%) |         |  72.11 KiB (1%) |        3740 |
| `["missing_dot", "xf_nota"]`             | 180.601 μs (5%) |         |  72.09 KiB (1%) |        3740 |
| `["overhead", "foldl"]`                  |   3.900 ns (5%) |         |                 |             |
| `["overhead", "reduce_basecase"]`        | 161.168 ns (5%) |         |  416 bytes (1%) |           7 |
| `["partition_by", "man"]`                |   1.837 ms (5%) |         |  352 bytes (1%) |           4 |
| `["partition_by", "xf"]`                 |   2.869 ms (5%) |         |   6.10 MiB (1%) |      200007 |
| `["set", "base"]`                        |   4.812 ms (5%) |         |  49.58 KiB (1%) |          18 |
| `["set", "xf"]`                          |   4.529 ms (5%) |         |  49.63 KiB (1%) |          21 |

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
       #1  2294 MHz      47111 s          0 s       1254 s      53910 s          0 s
       #2  2294 MHz      22256 s          0 s       1884 s      79149 s          0 s
       
  Memory: 6.7648773193359375 GB (2829.49609375 MB free)
  Uptime: 1044.0 sec
  Load Avg:  1.06298828125  0.9775390625  0.6220703125
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-8.0.1 (ORCJIT, broadwell)
```

---
# Baseline result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmark: 29 Jul 2020 - 6:7
* Package commit: f3056a
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
| `["append!!", "eduction"]`               |  15.600 μs (5%) |         |  64.72 KiB (1%) |          18 |
| `["append!!", "xf"]`                     |  15.400 μs (5%) |         |  64.72 KiB (1%) |          18 |
| `["cat", "base"]`                        |   1.500 μs (5%) |         |                 |             |
| `["cat", "xf"]`                          |   1.660 μs (5%) |         |                 |             |
| `["collect", "filter-missing"]`          |  90.001 μs (5%) |         | 345.31 KiB (1%) |       10015 |
| `["collect", "identity-float"]`          |  74.001 μs (5%) |         | 569.16 KiB (1%) |       10015 |
| `["collect", "identity-union"]`          | 267.103 μs (5%) |         | 704.86 KiB (1%) |       16648 |
| `["dict", "base"]`                       |   4.215 ms (5%) |         |  92.91 KiB (1%) |          22 |
| `["dict", "xf"]`                         |   4.329 ms (5%) |         |  92.36 KiB (1%) |          21 |
| `["dot", "blas"]`                        |   2.244 μs (5%) |         |                 |             |
| `["dot", "man"]`                         |   2.244 μs (5%) |         |                 |             |
| `["dot", "rf"]`                          |   3.050 μs (5%) |         |                 |             |
| `["dot", "xf"]`                          |   3.138 μs (5%) |         |   64 bytes (1%) |           3 |
| `["filter_map_map!", "man"]`             |  67.900 μs (5%) |         |                 |             |
| `["filter_map_map!", "xf"]`              | 539.605 μs (5%) |         |  304 bytes (1%) |          17 |
| `["filter_map_reduce", "man"]`           | 194.902 μs (5%) |         |                 |             |
| `["filter_map_reduce", "xf"]`            | 194.902 μs (5%) |         |                 |             |
| `["findall", "base"]`                    | 789.109 μs (5%) |         |   2.00 MiB (1%) |          21 |
| `["findall", "xf-array"]`                | 778.109 μs (5%) |         |   3.05 MiB (1%) |       99779 |
| `["findall", "xf-iter"]`                 |   3.340 ms (5%) |         |   9.63 MiB (1%) |      299920 |
| `["gemm", "fusedmul", "blas", "16"]`     |   5.357 ms (5%) |         |                 |             |
| `["gemm", "fusedmul", "blas", "2"]`      |   3.855 ms (5%) |         |                 |             |
| `["gemm", "fusedmul", "blas", "32"]`     |   7.985 ms (5%) |         |                 |             |
| `["gemm", "fusedmul", "blas", "8"]`      |   3.974 ms (5%) |         |                 |             |
| `["gemm", "fusedmul", "xf", "16"]`       |   5.589 ms (5%) |         |  160 bytes (1%) |           6 |
| `["gemm", "fusedmul", "xf", "2"]`        | 605.606 μs (5%) |         |  160 bytes (1%) |           6 |
| `["gemm", "fusedmul", "xf", "32"]`       |  11.166 ms (5%) |         |  160 bytes (1%) |           6 |
| `["gemm", "fusedmul", "xf", "8"]`        |   2.505 ms (5%) |         |  160 bytes (1%) |           6 |
| `["gemm", "mul", "linalg", "256"]`       |   1.213 ms (5%) |         |                 |             |
| `["gemm", "mul", "linalg", "32"]`        |   3.800 μs (5%) |         |                 |             |
| `["gemm", "mul", "linalg", "8"]`         | 300.000 ns (5%) |         |                 |             |
| `["gemm", "mul", "man", "false", "256"]` |   4.365 ms (5%) |         |                 |             |
| `["gemm", "mul", "man", "false", "32"]`  |   6.800 μs (5%) |         |                 |             |
| `["gemm", "mul", "man", "false", "8"]`   | 400.000 ns (5%) |         |                 |             |
| `["gemm", "mul", "man", "ivdep", "256"]` |   4.732 ms (5%) |         |                 |             |
| `["gemm", "mul", "man", "ivdep", "32"]`  |   6.200 μs (5%) |         |                 |             |
| `["gemm", "mul", "man", "ivdep", "8"]`   | 400.000 ns (5%) |         |                 |             |
| `["gemm", "mul", "man", "true", "256"]`  |   4.709 ms (5%) |         |                 |             |
| `["gemm", "mul", "man", "true", "32"]`   |   6.900 μs (5%) |         |                 |             |
| `["gemm", "mul", "man", "true", "8"]`    | 400.000 ns (5%) |         |                 |             |
| `["gemm", "mul", "xf", "false", "256"]`  |   4.773 ms (5%) |         |   48 bytes (1%) |           2 |
| `["gemm", "mul", "xf", "false", "32"]`   |   7.200 μs (5%) |         |   48 bytes (1%) |           2 |
| `["gemm", "mul", "xf", "false", "8"]`    | 300.000 ns (5%) |         |   48 bytes (1%) |           2 |
| `["gemm", "mul", "xf", "ivdep", "256"]`  |   4.716 ms (5%) |         |   48 bytes (1%) |           2 |
| `["gemm", "mul", "xf", "ivdep", "32"]`   |   5.600 μs (5%) |         |   48 bytes (1%) |           2 |
| `["gemm", "mul", "xf", "ivdep", "8"]`    | 400.000 ns (5%) |         |   48 bytes (1%) |           2 |
| `["gemm", "mul", "xf", "true", "256"]`   |   4.778 ms (5%) |         |   48 bytes (1%) |           2 |
| `["gemm", "mul", "xf", "true", "32"]`    |   7.500 μs (5%) |         |   48 bytes (1%) |           2 |
| `["gemm", "mul", "xf", "true", "8"]`     | 400.000 ns (5%) |         |   48 bytes (1%) |           2 |
| `["groupby", "sum", "sac"]`              | 205.901 μs (5%) |         | 313.14 KiB (1%) |       10007 |
| `["groupby", "sum", "xf-with-init"]`     | 154.701 μs (5%) |         | 157.44 KiB (1%) |       10008 |
| `["groupby", "sum", "xf-without-init"]`  | 156.401 μs (5%) |         | 157.44 KiB (1%) |       10008 |
| `["mapcat_eduction", "base"]`            |   1.480 μs (5%) |         |                 |             |
| `["mapcat_eduction", "xf-eduction"]`     |   1.600 μs (5%) |         |                 |             |
| `["mapcat_eduction", "xf-xf"]`           |   1.600 μs (5%) |         |                 |             |
| `["missing_argmax", "man"]`              | 915.385 ns (5%) |         |   32 bytes (1%) |           1 |
| `["missing_argmax", "rf"]`               |   2.133 μs (5%) |         |   32 bytes (1%) |           1 |
| `["missing_argmax", "xf"]`               |   2.111 μs (5%) |         |   32 bytes (1%) |           1 |
| `["missing_dot", "equiv"]`               | 994.737 ns (5%) |         |   16 bytes (1%) |           1 |
| `["missing_dot", "man"]`                 |   1.084 μs (5%) |         |   16 bytes (1%) |           1 |
| `["missing_dot", "naive"]`               |   4.043 μs (5%) |         |   16 bytes (1%) |           1 |
| `["missing_dot", "rf"]`                  | 890.292 ns (5%) |         |   16 bytes (1%) |           1 |
| `["missing_dot", "rf_nota"]`             | 944.918 ns (5%) |         |   16 bytes (1%) |           1 |
| `["missing_dot", "xf"]`                  | 186.202 μs (5%) |         |  72.05 KiB (1%) |        3736 |
| `["missing_dot", "xf_nota"]`             | 183.803 μs (5%) |         |  72.09 KiB (1%) |        3740 |
| `["overhead", "foldl"]`                  |   3.900 ns (5%) |         |                 |             |
| `["overhead", "reduce_basecase"]`        | 166.373 ns (5%) |         |  416 bytes (1%) |           7 |
| `["partition_by", "man"]`                |   1.853 ms (5%) |         |  352 bytes (1%) |           4 |
| `["partition_by", "xf"]`                 |   2.846 ms (5%) |         |   6.10 MiB (1%) |      200007 |
| `["set", "base"]`                        |   5.103 ms (5%) |         |  49.58 KiB (1%) |          18 |
| `["set", "xf"]`                          |   4.558 ms (5%) |         |  49.63 KiB (1%) |          21 |

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
       #1  2294 MHz      72985 s          0 s       1434 s      56859 s          0 s
       #2  2294 MHz      25254 s          0 s       1976 s     105077 s          0 s
       
  Memory: 6.7648773193359375 GB (2649.73828125 MB free)
  Uptime: 1335.0 sec
  Load Avg:  1.02197265625  1.033203125  0.75537109375
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

