# Benchmark result

* Pull request commit: [`bf87a8d734f7c25a7170b6bf18e14c9ddd07f3f9`](https://github.com/JuliaFolds/Transducers.jl/commit/bf87a8d734f7c25a7170b6bf18e14c9ddd07f3f9)
* Pull request: <https://github.com/JuliaFolds/Transducers.jl/pull/396> (Run Aqua.test_stale_deps(Transducers))

# Judge result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmarks:
    - Target: 4 Aug 2020 - 17:28
    - Baseline: 4 Aug 2020 - 17:33
* Package commits:
    - Target: 5e6ae2
    - Baseline: 5c0b7f
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
| `["append!!", "eduction"]`               |                1.10 (5%) :x: |    1.00 (1%)  |
| `["cat", "base"]`                        |                1.24 (5%) :x: |    1.00 (1%)  |
| `["cat", "xf"]`                          |                1.15 (5%) :x: |    1.00 (1%)  |
| `["dot", "blas"]`                        |                1.07 (5%) :x: |    1.00 (1%)  |
| `["dot", "man"]`                         |                1.08 (5%) :x: |    1.00 (1%)  |
| `["findall", "xf-array"]`                |                1.10 (5%) :x: | 1.08 (1%) :x: |
| `["gemm", "fusedmul", "xf", "16"]`       | 0.91 (5%) :white_check_mark: |    1.00 (1%)  |
| `["gemm", "fusedmul", "xf", "2"]`        | 0.92 (5%) :white_check_mark: |    1.00 (1%)  |
| `["gemm", "fusedmul", "xf", "32"]`       |                1.20 (5%) :x: |    1.00 (1%)  |
| `["gemm", "fusedmul", "xf", "8"]`        |                1.21 (5%) :x: |    1.00 (1%)  |
| `["gemm", "mul", "linalg", "256"]`       | 0.88 (5%) :white_check_mark: |    1.00 (1%)  |
| `["gemm", "mul", "linalg", "8"]`         |                1.05 (5%) :x: |    1.00 (1%)  |
| `["gemm", "mul", "man", "false", "256"]` |                1.12 (5%) :x: |    1.00 (1%)  |
| `["gemm", "mul", "man", "false", "32"]`  | 0.77 (5%) :white_check_mark: |    1.00 (1%)  |
| `["gemm", "mul", "man", "false", "8"]`   |                1.38 (5%) :x: |    1.00 (1%)  |
| `["gemm", "mul", "man", "ivdep", "256"]` |                1.09 (5%) :x: |    1.00 (1%)  |
| `["gemm", "mul", "man", "ivdep", "32"]`  | 0.89 (5%) :white_check_mark: |    1.00 (1%)  |
| `["gemm", "mul", "man", "ivdep", "8"]`   | 0.64 (5%) :white_check_mark: |    1.00 (1%)  |
| `["gemm", "mul", "man", "true", "256"]`  |                1.10 (5%) :x: |    1.00 (1%)  |
| `["gemm", "mul", "man", "true", "8"]`    |                1.11 (5%) :x: |    1.00 (1%)  |
| `["gemm", "mul", "xf", "false", "256"]`  |                1.11 (5%) :x: |    1.00 (1%)  |
| `["gemm", "mul", "xf", "false", "32"]`   | 0.86 (5%) :white_check_mark: |    1.00 (1%)  |
| `["gemm", "mul", "xf", "false", "8"]`    | 0.81 (5%) :white_check_mark: |    1.00 (1%)  |
| `["gemm", "mul", "xf", "ivdep", "256"]`  |                1.09 (5%) :x: |    1.00 (1%)  |
| `["gemm", "mul", "xf", "true", "256"]`   |                1.09 (5%) :x: |    1.00 (1%)  |
| `["gemm", "mul", "xf", "true", "32"]`    | 0.76 (5%) :white_check_mark: |    1.00 (1%)  |
| `["mapcat_eduction", "base"]`            |                1.15 (5%) :x: |    1.00 (1%)  |
| `["mapcat_eduction", "xf-eduction"]`     |                1.15 (5%) :x: |    1.00 (1%)  |
| `["missing_dot", "equiv"]`               |                1.53 (5%) :x: |    1.00 (1%)  |
| `["missing_dot", "man"]`                 |                1.14 (5%) :x: |    1.00 (1%)  |
| `["missing_dot", "rf"]`                  |                1.35 (5%) :x: |    1.00 (1%)  |

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
       #1  2095 MHz      46712 s          0 s       1475 s      26761 s          0 s
       #2  2095 MHz      19891 s          0 s       1556 s      53819 s          0 s
       
  Memory: 6.764881134033203 GB (2865.77734375 MB free)
  Uptime: 770.0 sec
  Load Avg:  1.0  0.94921875  0.60302734375
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
       #1  2095 MHz      51285 s          0 s       1550 s      49227 s          0 s
       #2  2095 MHz      42405 s          0 s       1669 s      58301 s          0 s
       
  Memory: 6.764881134033203 GB (2723.4140625 MB free)
  Uptime: 1042.0 sec
  Load Avg:  1.0205078125  1.0  0.72265625
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-8.0.1 (ORCJIT, skylake)
```

---
# Target result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmark: 4 Aug 2020 - 17:28
* Package commit: 5e6ae2
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
| `["append!!", "eduction"]`               |  18.501 μs (5%) |         |  64.72 KiB (1%) |          18 |
| `["append!!", "xf"]`                     |  16.701 μs (5%) |         |  64.72 KiB (1%) |          18 |
| `["cat", "base"]`                        |   2.080 μs (5%) |         |                 |             |
| `["cat", "xf"]`                          |   2.611 μs (5%) |         |                 |             |
| `["collect", "filter-missing"]`          |  94.606 μs (5%) |         | 345.31 KiB (1%) |       10015 |
| `["collect", "identity-float"]`          |  69.004 μs (5%) |         | 569.16 KiB (1%) |       10015 |
| `["collect", "identity-union"]`          | 271.517 μs (5%) |         | 704.59 KiB (1%) |       16631 |
| `["dict", "base"]`                       |   3.638 ms (5%) |         |  92.91 KiB (1%) |          22 |
| `["dict", "xf"]`                         |   3.637 ms (5%) |         |  92.36 KiB (1%) |          21 |
| `["dot", "blas"]`                        |   1.160 μs (5%) |         |                 |             |
| `["dot", "man"]`                         |   1.120 μs (5%) |         |                 |             |
| `["dot", "rf"]`                          |   1.800 μs (5%) |         |                 |             |
| `["dot", "xf"]`                          |   1.880 μs (5%) |         |   64 bytes (1%) |           3 |
| `["filter_map_map!", "man"]`             |  68.703 μs (5%) |         |                 |             |
| `["filter_map_map!", "xf"]`              | 631.524 μs (5%) |         |  304 bytes (1%) |          17 |
| `["filter_map_reduce", "man"]`           | 192.310 μs (5%) |         |                 |             |
| `["filter_map_reduce", "xf"]`            | 192.310 μs (5%) |         |                 |             |
| `["findall", "base"]`                    | 708.941 μs (5%) |         |   2.00 MiB (1%) |          21 |
| `["findall", "xf-array"]`                | 692.839 μs (5%) |         |   3.03 MiB (1%) |       99356 |
| `["findall", "xf-iter"]`                 |   3.012 ms (5%) |         |   9.63 MiB (1%) |      299916 |
| `["gemm", "fusedmul", "blas", "16"]`     |   3.946 ms (5%) |         |                 |             |
| `["gemm", "fusedmul", "blas", "2"]`      |   3.029 ms (5%) |         |                 |             |
| `["gemm", "fusedmul", "blas", "32"]`     |   5.462 ms (5%) |         |                 |             |
| `["gemm", "fusedmul", "blas", "8"]`      |   3.334 ms (5%) |         |                 |             |
| `["gemm", "fusedmul", "xf", "16"]`       |   4.066 ms (5%) |         |  160 bytes (1%) |           6 |
| `["gemm", "fusedmul", "xf", "2"]`        | 552.422 μs (5%) |         |  160 bytes (1%) |           6 |
| `["gemm", "fusedmul", "xf", "32"]`       |   9.268 ms (5%) |         |  160 bytes (1%) |           6 |
| `["gemm", "fusedmul", "xf", "8"]`        |   2.161 ms (5%) |         |  160 bytes (1%) |           6 |
| `["gemm", "mul", "linalg", "256"]`       | 748.337 μs (5%) |         |                 |             |
| `["gemm", "mul", "linalg", "32"]`        |   2.500 μs (5%) |         |                 |             |
| `["gemm", "mul", "linalg", "8"]`         | 210.630 ns (5%) |         |                 |             |
| `["gemm", "mul", "man", "false", "256"]` |   1.480 ms (5%) |         |                 |             |
| `["gemm", "mul", "man", "false", "32"]`  |   4.014 μs (5%) |         |                 |             |
| `["gemm", "mul", "man", "false", "8"]`   | 414.085 ns (5%) |         |                 |             |
| `["gemm", "mul", "man", "ivdep", "256"]` |   1.466 ms (5%) |         |                 |             |
| `["gemm", "mul", "man", "ivdep", "32"]`  |   3.275 μs (5%) |         |                 |             |
| `["gemm", "mul", "man", "ivdep", "8"]`   | 318.897 ns (5%) |         |                 |             |
| `["gemm", "mul", "man", "true", "256"]`  |   1.462 ms (5%) |         |                 |             |
| `["gemm", "mul", "man", "true", "32"]`   |   4.029 μs (5%) |         |                 |             |
| `["gemm", "mul", "man", "true", "8"]`    | 333.347 ns (5%) |         |                 |             |
| `["gemm", "mul", "xf", "false", "256"]`  |   1.477 ms (5%) |         |   48 bytes (1%) |           2 |
| `["gemm", "mul", "xf", "false", "32"]`   |   5.000 μs (5%) |         |   48 bytes (1%) |           2 |
| `["gemm", "mul", "xf", "false", "8"]`    | 323.228 ns (5%) |         |   48 bytes (1%) |           2 |
| `["gemm", "mul", "xf", "ivdep", "256"]`  |   1.481 ms (5%) |         |   48 bytes (1%) |           2 |
| `["gemm", "mul", "xf", "ivdep", "32"]`   |   3.150 μs (5%) |         |   48 bytes (1%) |           2 |
| `["gemm", "mul", "xf", "ivdep", "8"]`    | 300.481 ns (5%) |         |   48 bytes (1%) |           2 |
| `["gemm", "mul", "xf", "true", "256"]`   |   1.463 ms (5%) |         |   48 bytes (1%) |           2 |
| `["gemm", "mul", "xf", "true", "32"]`    |   4.567 μs (5%) |         |   48 bytes (1%) |           2 |
| `["gemm", "mul", "xf", "true", "8"]`     | 403.082 ns (5%) |         |   48 bytes (1%) |           2 |
| `["groupby", "sum", "sac"]`              | 209.108 μs (5%) |         | 313.14 KiB (1%) |       10007 |
| `["groupby", "sum", "xf-with-init"]`     | 168.006 μs (5%) |         | 157.44 KiB (1%) |       10008 |
| `["groupby", "sum", "xf-without-init"]`  | 159.906 μs (5%) |         | 157.44 KiB (1%) |       10008 |
| `["mapcat_eduction", "base"]`            |   2.070 μs (5%) |         |                 |             |
| `["mapcat_eduction", "xf-eduction"]`     |   2.240 μs (5%) |         |                 |             |
| `["mapcat_eduction", "xf-xf"]`           |   1.860 μs (5%) |         |                 |             |
| `["missing_argmax", "man"]`              |   2.233 μs (5%) |         |   32 bytes (1%) |           1 |
| `["missing_argmax", "rf"]`               |   2.145 μs (5%) |         |   32 bytes (1%) |           1 |
| `["missing_argmax", "xf"]`               |   2.711 μs (5%) |         |   32 bytes (1%) |           1 |
| `["missing_dot", "equiv"]`               |   1.850 μs (5%) |         |   16 bytes (1%) |           1 |
| `["missing_dot", "man"]`                 |   1.330 μs (5%) |         |   16 bytes (1%) |           1 |
| `["missing_dot", "naive"]`               |   4.086 μs (5%) |         |   16 bytes (1%) |           1 |
| `["missing_dot", "rf"]`                  |   1.550 μs (5%) |         |   16 bytes (1%) |           1 |
| `["missing_dot", "rf_nota"]`             |   1.430 μs (5%) |         |   16 bytes (1%) |           1 |
| `["missing_dot", "xf"]`                  | 177.009 μs (5%) |         |  72.11 KiB (1%) |        3742 |
| `["missing_dot", "xf_nota"]`             | 180.609 μs (5%) |         |  72.13 KiB (1%) |        3742 |
| `["overhead", "foldl"]`                  |   3.900 ns (5%) |         |                 |             |
| `["overhead", "reduce_basecase"]`        | 227.970 ns (5%) |         |  464 bytes (1%) |           9 |
| `["partition_by", "man"]`                |   1.736 ms (5%) |         |  352 bytes (1%) |           4 |
| `["partition_by", "xf"]`                 |   2.761 ms (5%) |         |   6.10 MiB (1%) |      200007 |
| `["set", "base"]`                        |   4.570 ms (5%) |         |  49.58 KiB (1%) |          18 |
| `["set", "xf"]`                          |   4.114 ms (5%) |         |  49.63 KiB (1%) |          21 |

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
       #1  2095 MHz      46712 s          0 s       1475 s      26761 s          0 s
       #2  2095 MHz      19891 s          0 s       1556 s      53819 s          0 s
       
  Memory: 6.764881134033203 GB (2865.77734375 MB free)
  Uptime: 770.0 sec
  Load Avg:  1.0  0.94921875  0.60302734375
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-8.0.1 (ORCJIT, skylake)
```

---
# Baseline result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmark: 4 Aug 2020 - 17:33
* Package commit: 5c0b7f
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
| `["append!!", "eduction"]`               |  16.800 μs (5%) |         |  64.72 KiB (1%) |          18 |
| `["append!!", "xf"]`                     |  16.801 μs (5%) |         |  64.72 KiB (1%) |          18 |
| `["cat", "base"]`                        |   1.680 μs (5%) |         |                 |             |
| `["cat", "xf"]`                          |   2.278 μs (5%) |         |                 |             |
| `["collect", "filter-missing"]`          |  94.203 μs (5%) |         | 345.31 KiB (1%) |       10015 |
| `["collect", "identity-float"]`          |  69.902 μs (5%) |         | 569.16 KiB (1%) |       10015 |
| `["collect", "identity-union"]`          | 266.209 μs (5%) |         | 705.28 KiB (1%) |       16677 |
| `["dict", "base"]`                       |   3.659 ms (5%) |         |  92.91 KiB (1%) |          22 |
| `["dict", "xf"]`                         |   3.762 ms (5%) |         |  92.36 KiB (1%) |          21 |
| `["dot", "blas"]`                        |   1.080 μs (5%) |         |                 |             |
| `["dot", "man"]`                         |   1.040 μs (5%) |         |                 |             |
| `["dot", "rf"]`                          |   1.830 μs (5%) |         |                 |             |
| `["dot", "xf"]`                          |   1.850 μs (5%) |         |   64 bytes (1%) |           3 |
| `["filter_map_map!", "man"]`             |  68.807 μs (5%) |         |                 |             |
| `["filter_map_map!", "xf"]`              | 633.259 μs (5%) |         |  304 bytes (1%) |          17 |
| `["filter_map_reduce", "man"]`           | 195.506 μs (5%) |         |                 |             |
| `["filter_map_reduce", "xf"]`            | 192.006 μs (5%) |         |                 |             |
| `["findall", "base"]`                    | 705.123 μs (5%) |         |   2.00 MiB (1%) |          21 |
| `["findall", "xf-array"]`                | 629.621 μs (5%) |         |   2.81 MiB (1%) |       91859 |
| `["findall", "xf-iter"]`                 |   3.025 ms (5%) |         |   9.63 MiB (1%) |      299913 |
| `["gemm", "fusedmul", "blas", "16"]`     |   4.049 ms (5%) |         |                 |             |
| `["gemm", "fusedmul", "blas", "2"]`      |   2.998 ms (5%) |         |                 |             |
| `["gemm", "fusedmul", "blas", "32"]`     |   5.734 ms (5%) |         |                 |             |
| `["gemm", "fusedmul", "blas", "8"]`      |   3.288 ms (5%) |         |                 |             |
| `["gemm", "fusedmul", "xf", "16"]`       |   4.456 ms (5%) |         |  160 bytes (1%) |           6 |
| `["gemm", "fusedmul", "xf", "2"]`        | 601.560 μs (5%) |         |  160 bytes (1%) |           6 |
| `["gemm", "fusedmul", "xf", "32"]`       |   7.750 ms (5%) |         |  160 bytes (1%) |           6 |
| `["gemm", "fusedmul", "xf", "8"]`        |   1.783 ms (5%) |         |  160 bytes (1%) |           6 |
| `["gemm", "mul", "linalg", "256"]`       | 850.928 μs (5%) |         |                 |             |
| `["gemm", "mul", "linalg", "32"]`        |   2.500 μs (5%) |         |                 |             |
| `["gemm", "mul", "linalg", "8"]`         | 200.000 ns (5%) |         |                 |             |
| `["gemm", "mul", "man", "false", "256"]` |   1.327 ms (5%) |         |                 |             |
| `["gemm", "mul", "man", "false", "32"]`  |   5.200 μs (5%) |         |                 |             |
| `["gemm", "mul", "man", "false", "8"]`   | 300.000 ns (5%) |         |                 |             |
| `["gemm", "mul", "man", "ivdep", "256"]` |   1.351 ms (5%) |         |                 |             |
| `["gemm", "mul", "man", "ivdep", "32"]`  |   3.700 μs (5%) |         |                 |             |
| `["gemm", "mul", "man", "ivdep", "8"]`   | 500.000 ns (5%) |         |                 |             |
| `["gemm", "mul", "man", "true", "256"]`  |   1.332 ms (5%) |         |                 |             |
| `["gemm", "mul", "man", "true", "32"]`   |   4.100 μs (5%) |         |                 |             |
| `["gemm", "mul", "man", "true", "8"]`    | 300.000 ns (5%) |         |                 |             |
| `["gemm", "mul", "xf", "false", "256"]`  |   1.329 ms (5%) |         |   48 bytes (1%) |           2 |
| `["gemm", "mul", "xf", "false", "32"]`   |   5.800 μs (5%) |         |   48 bytes (1%) |           2 |
| `["gemm", "mul", "xf", "false", "8"]`    | 400.000 ns (5%) |         |   48 bytes (1%) |           2 |
| `["gemm", "mul", "xf", "ivdep", "256"]`  |   1.362 ms (5%) |         |   48 bytes (1%) |           2 |
| `["gemm", "mul", "xf", "ivdep", "32"]`   |   3.200 μs (5%) |         |   48 bytes (1%) |           2 |
| `["gemm", "mul", "xf", "ivdep", "8"]`    | 300.000 ns (5%) |         |   48 bytes (1%) |           2 |
| `["gemm", "mul", "xf", "true", "256"]`   |   1.348 ms (5%) |         |   48 bytes (1%) |           2 |
| `["gemm", "mul", "xf", "true", "32"]`    |   6.000 μs (5%) |         |   48 bytes (1%) |           2 |
| `["gemm", "mul", "xf", "true", "8"]`     | 400.000 ns (5%) |         |   48 bytes (1%) |           2 |
| `["groupby", "sum", "sac"]`              | 207.419 μs (5%) |         | 313.14 KiB (1%) |       10007 |
| `["groupby", "sum", "xf-with-init"]`     | 162.714 μs (5%) |         | 157.44 KiB (1%) |       10008 |
| `["groupby", "sum", "xf-without-init"]`  | 164.515 μs (5%) |         | 157.44 KiB (1%) |       10008 |
| `["mapcat_eduction", "base"]`            |   1.800 μs (5%) |         |                 |             |
| `["mapcat_eduction", "xf-eduction"]`     |   1.950 μs (5%) |         |                 |             |
| `["mapcat_eduction", "xf-xf"]`           |   1.950 μs (5%) |         |                 |             |
| `["missing_argmax", "man"]`              |   2.233 μs (5%) |         |   32 bytes (1%) |           1 |
| `["missing_argmax", "rf"]`               |   2.145 μs (5%) |         |   32 bytes (1%) |           1 |
| `["missing_argmax", "xf"]`               |   2.700 μs (5%) |         |   32 bytes (1%) |           1 |
| `["missing_dot", "equiv"]`               |   1.210 μs (5%) |         |   16 bytes (1%) |           1 |
| `["missing_dot", "man"]`                 |   1.170 μs (5%) |         |   16 bytes (1%) |           1 |
| `["missing_dot", "naive"]`               |   4.086 μs (5%) |         |   16 bytes (1%) |           1 |
| `["missing_dot", "rf"]`                  |   1.150 μs (5%) |         |   16 bytes (1%) |           1 |
| `["missing_dot", "rf_nota"]`             |   1.430 μs (5%) |         |   16 bytes (1%) |           1 |
| `["missing_dot", "xf"]`                  | 179.606 μs (5%) |         |  71.94 KiB (1%) |        3732 |
| `["missing_dot", "xf_nota"]`             | 190.106 μs (5%) |         |  72.16 KiB (1%) |        3742 |
| `["overhead", "foldl"]`                  |   3.900 ns (5%) |         |                 |             |
| `["overhead", "reduce_basecase"]`        | 224.739 ns (5%) |         |  464 bytes (1%) |           9 |
| `["partition_by", "man"]`                |   1.736 ms (5%) |         |  352 bytes (1%) |           4 |
| `["partition_by", "xf"]`                 |   2.831 ms (5%) |         |   6.10 MiB (1%) |      200007 |
| `["set", "base"]`                        |   4.448 ms (5%) |         |  49.58 KiB (1%) |          18 |
| `["set", "xf"]`                          |   3.959 ms (5%) |         |  49.63 KiB (1%) |          21 |

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
       #1  2095 MHz      51285 s          0 s       1550 s      49227 s          0 s
       #2  2095 MHz      42405 s          0 s       1669 s      58301 s          0 s
       
  Memory: 6.764881134033203 GB (2723.4140625 MB free)
  Uptime: 1042.0 sec
  Load Avg:  1.0205078125  1.0  0.72265625
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
    CPU MHz:             2095.214
    BogoMIPS:            4190.42
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

