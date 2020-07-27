# Benchmark result

* Pull request commit: [`219f1c7fb03675e4176c45f2bd3d4a76669f74b4`](https://github.com/JuliaFolds/Transducers.jl/commit/219f1c7fb03675e4176c45f2bd3d4a76669f74b4)
* Pull request: <https://github.com/JuliaFolds/Transducers.jl/pull/378> (Use released version of BenchmarkCI)

# Judge result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmarks:
    - Target: 27 Jul 2020 - 07:12
    - Baseline: 27 Jul 2020 - 07:17
* Package commits:
    - Target: 0ace2f
    - Baseline: 0e35d7
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
| `["cat", "xf"]`                          | 0.86 (5%) :white_check_mark: |    1.00 (1%)  |
| `["collect", "identity-float"]`          | 0.94 (5%) :white_check_mark: |    1.00 (1%)  |
| `["filter_map_map!", "man"]`             | 0.80 (5%) :white_check_mark: |    1.00 (1%)  |
| `["filter_map_map!", "xf"]`              |                1.07 (5%) :x: |    1.00 (1%)  |
| `["findall", "xf-array"]`                |                   0.98 (5%)  | 1.03 (1%) :x: |
| `["gemm", "mul", "linalg", "8"]`         |                1.21 (5%) :x: |    1.00 (1%)  |
| `["gemm", "mul", "man", "false", "8"]`   |                1.15 (5%) :x: |    1.00 (1%)  |
| `["gemm", "mul", "man", "true", "8"]`    |                1.23 (5%) :x: |    1.00 (1%)  |
| `["gemm", "mul", "xf", "false", "32"]`   |                1.28 (5%) :x: |    1.00 (1%)  |
| `["gemm", "mul", "xf", "ivdep", "32"]`   | 0.94 (5%) :white_check_mark: |    1.00 (1%)  |
| `["gemm", "mul", "xf", "ivdep", "8"]`    |                1.51 (5%) :x: |    1.00 (1%)  |
| `["gemm", "mul", "xf", "true", "32"]`    | 0.89 (5%) :white_check_mark: |    1.00 (1%)  |
| `["groupby", "sum", "sac"]`              |                1.10 (5%) :x: |    1.00 (1%)  |
| `["groupby", "sum", "xf-without-init"]`  |                1.09 (5%) :x: |    1.00 (1%)  |
| `["missing_argmax", "rf"]`               |                1.25 (5%) :x: |    1.00 (1%)  |
| `["missing_argmax", "xf"]`               | 0.79 (5%) :white_check_mark: |    1.00 (1%)  |
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
  CPU: Intel(R) Xeon(R) Platinum 8272CL CPU @ 2.60GHz: 
              speed         user         nice          sys         idle          irq
       #1  2593 MHz      54583 s          0 s       1429 s      57202 s          0 s
       #2  2593 MHz      10030 s          0 s       1623 s      97863 s          0 s
       
  Memory: 6.791385650634766 GB (3050.72265625 MB free)
  Uptime: 1181.0 sec
  Load Avg:  1.03515625  0.9970703125  0.68408203125
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
  uname: Linux 5.3.0-1032-azure #33~18.04.1-Ubuntu SMP Fri Jun 26 15:01:15 UTC 2020 x86_64 x86_64
  CPU: Intel(R) Xeon(R) Platinum 8272CL CPU @ 2.60GHz: 
              speed         user         nice          sys         idle          irq
       #1  2593 MHz      56195 s          0 s       1500 s      83109 s          0 s
       #2  2593 MHz      36064 s          0 s       1732 s      99391 s          0 s
       
  Memory: 6.791385650634766 GB (2900.8828125 MB free)
  Uptime: 1458.0 sec
  Load Avg:  1.0  1.0  0.78125
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-8.0.1 (ORCJIT, skylake)
```

---
# Target result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmark: 27 Jul 2020 - 7:12
* Package commit: 0ace2f
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
| `["append!!", "eduction"]`               |  19.600 μs (5%) |         |  64.72 KiB (1%) |          18 |
| `["append!!", "xf"]`                     |  19.500 μs (5%) |         |  64.72 KiB (1%) |          18 |
| `["cat", "base"]`                        |   1.770 μs (5%) |         |                 |             |
| `["cat", "xf"]`                          |   2.010 μs (5%) |         |                 |             |
| `["collect", "filter-missing"]`          | 113.300 μs (5%) |         | 345.31 KiB (1%) |       10015 |
| `["collect", "identity-float"]`          |  80.700 μs (5%) |         | 569.16 KiB (1%) |       10015 |
| `["collect", "identity-union"]`          | 319.703 μs (5%) |         | 704.83 KiB (1%) |       16646 |
| `["dict", "base"]`                       |   4.079 ms (5%) |         |  92.91 KiB (1%) |          22 |
| `["dict", "xf"]`                         |   4.210 ms (5%) |         |  92.36 KiB (1%) |          21 |
| `["dot", "blas"]`                        |   1.210 μs (5%) |         |                 |             |
| `["dot", "man"]`                         |   1.190 μs (5%) |         |                 |             |
| `["dot", "rf"]`                          |   2.133 μs (5%) |         |                 |             |
| `["dot", "xf"]`                          |   2.211 μs (5%) |         |   64 bytes (1%) |           3 |
| `["filter_map_map!", "man"]`             |  63.401 μs (5%) |         |                 |             |
| `["filter_map_map!", "xf"]`              | 750.309 μs (5%) |         |  304 bytes (1%) |          17 |
| `["filter_map_reduce", "man"]`           | 230.003 μs (5%) |         |                 |             |
| `["filter_map_reduce", "xf"]`            | 230.003 μs (5%) |         |                 |             |
| `["findall", "base"]`                    | 833.406 μs (5%) |         |   2.00 MiB (1%) |          21 |
| `["findall", "xf-array"]`                | 812.313 μs (5%) |         |   3.06 MiB (1%) |      100099 |
| `["findall", "xf-iter"]`                 |   3.437 ms (5%) |         |   9.63 MiB (1%) |      299937 |
| `["gemm", "fusedmul", "blas", "16"]`     |   4.275 ms (5%) |         |                 |             |
| `["gemm", "fusedmul", "blas", "2"]`      |   3.226 ms (5%) |         |                 |             |
| `["gemm", "fusedmul", "blas", "32"]`     |   5.917 ms (5%) |         |                 |             |
| `["gemm", "fusedmul", "blas", "8"]`      |   3.369 ms (5%) |         |                 |             |
| `["gemm", "fusedmul", "xf", "16"]`       |   5.281 ms (5%) |         |  160 bytes (1%) |           6 |
| `["gemm", "fusedmul", "xf", "2"]`        | 653.209 μs (5%) |         |  160 bytes (1%) |           6 |
| `["gemm", "fusedmul", "xf", "32"]`       |  10.521 ms (5%) |         |  160 bytes (1%) |           6 |
| `["gemm", "fusedmul", "xf", "8"]`        |   2.644 ms (5%) |         |  160 bytes (1%) |           6 |
| `["gemm", "mul", "linalg", "256"]`       | 892.213 μs (5%) |         |                 |             |
| `["gemm", "mul", "linalg", "32"]`        |   3.000 μs (5%) |         |                 |             |
| `["gemm", "mul", "linalg", "8"]`         | 242.465 ns (5%) |         |                 |             |
| `["gemm", "mul", "man", "false", "256"]` |   1.539 ms (5%) |         |                 |             |
| `["gemm", "mul", "man", "false", "32"]`  |   4.800 μs (5%) |         |                 |             |
| `["gemm", "mul", "man", "false", "8"]`   | 459.904 ns (5%) |         |                 |             |
| `["gemm", "mul", "man", "ivdep", "256"]` |   1.578 ms (5%) |         |                 |             |
| `["gemm", "mul", "man", "ivdep", "32"]`  |   3.800 μs (5%) |         |                 |             |
| `["gemm", "mul", "man", "ivdep", "8"]`   | 382.848 ns (5%) |         |                 |             |
| `["gemm", "mul", "man", "true", "256"]`  |   1.552 ms (5%) |         |                 |             |
| `["gemm", "mul", "man", "true", "32"]`   |   4.929 μs (5%) |         |                 |             |
| `["gemm", "mul", "man", "true", "8"]`    | 490.727 ns (5%) |         |                 |             |
| `["gemm", "mul", "xf", "false", "256"]`  |   1.542 ms (5%) |         |   48 bytes (1%) |           2 |
| `["gemm", "mul", "xf", "false", "32"]`   |   6.000 μs (5%) |         |   48 bytes (1%) |           2 |
| `["gemm", "mul", "xf", "false", "8"]`    | 387.197 ns (5%) |         |   48 bytes (1%) |           2 |
| `["gemm", "mul", "xf", "ivdep", "256"]`  |   1.595 ms (5%) |         |   48 bytes (1%) |           2 |
| `["gemm", "mul", "xf", "ivdep", "32"]`   |   3.650 μs (5%) |         |   48 bytes (1%) |           2 |
| `["gemm", "mul", "xf", "ivdep", "8"]`    | 453.305 ns (5%) |         |   48 bytes (1%) |           2 |
| `["gemm", "mul", "xf", "true", "256"]`   |   1.535 ms (5%) |         |   48 bytes (1%) |           2 |
| `["gemm", "mul", "xf", "true", "32"]`    |   4.814 μs (5%) |         |   48 bytes (1%) |           2 |
| `["gemm", "mul", "xf", "true", "8"]`     | 380.887 ns (5%) |         |   48 bytes (1%) |           2 |
| `["groupby", "sum", "sac"]`              | 276.303 μs (5%) |         | 313.14 KiB (1%) |       10007 |
| `["groupby", "sum", "xf-with-init"]`     | 199.602 μs (5%) |         | 157.44 KiB (1%) |       10008 |
| `["groupby", "sum", "xf-without-init"]`  | 208.402 μs (5%) |         | 157.44 KiB (1%) |       10008 |
| `["mapcat_eduction", "base"]`            |   1.870 μs (5%) |         |                 |             |
| `["mapcat_eduction", "xf-eduction"]`     |   1.920 μs (5%) |         |                 |             |
| `["mapcat_eduction", "xf-xf"]`           |   2.022 μs (5%) |         |                 |             |
| `["missing_argmax", "man"]`              |   2.678 μs (5%) |         |   32 bytes (1%) |           1 |
| `["missing_argmax", "rf"]`               |   3.200 μs (5%) |         |   32 bytes (1%) |           1 |
| `["missing_argmax", "xf"]`               |   2.533 μs (5%) |         |   32 bytes (1%) |           1 |
| `["missing_dot", "equiv"]`               |   1.650 μs (5%) |         |   16 bytes (1%) |           1 |
| `["missing_dot", "man"]`                 |   1.370 μs (5%) |         |   16 bytes (1%) |           1 |
| `["missing_dot", "naive"]`               |   4.914 μs (5%) |         |   16 bytes (1%) |           1 |
| `["missing_dot", "rf"]`                  |   1.410 μs (5%) |         |   16 bytes (1%) |           1 |
| `["missing_dot", "rf_nota"]`             |   1.640 μs (5%) |         |   16 bytes (1%) |           1 |
| `["missing_dot", "xf"]`                  | 208.403 μs (5%) |         |  72.02 KiB (1%) |        3738 |
| `["missing_dot", "xf_nota"]`             | 207.303 μs (5%) |         |  72.06 KiB (1%) |        3740 |
| `["overhead", "foldl"]`                  |   5.000 ns (5%) |         |                 |             |
| `["overhead", "reduce_basecase"]`        | 183.640 ns (5%) |         |  416 bytes (1%) |           7 |
| `["partition_by", "man"]`                |   2.028 ms (5%) |         |  352 bytes (1%) |           4 |
| `["partition_by", "xf"]`                 |   3.151 ms (5%) |         |   6.10 MiB (1%) |      200007 |
| `["set", "base"]`                        |   4.928 ms (5%) |         |  49.58 KiB (1%) |          18 |
| `["set", "xf"]`                          |   4.482 ms (5%) |         |  49.63 KiB (1%) |          21 |

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
  CPU: Intel(R) Xeon(R) Platinum 8272CL CPU @ 2.60GHz: 
              speed         user         nice          sys         idle          irq
       #1  2593 MHz      54583 s          0 s       1429 s      57202 s          0 s
       #2  2593 MHz      10030 s          0 s       1623 s      97863 s          0 s
       
  Memory: 6.791385650634766 GB (3050.72265625 MB free)
  Uptime: 1181.0 sec
  Load Avg:  1.03515625  0.9970703125  0.68408203125
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-8.0.1 (ORCJIT, skylake)
```

---
# Baseline result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmark: 27 Jul 2020 - 7:17
* Package commit: 0e35d7
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
| `["append!!", "eduction"]`               |  19.600 μs (5%) |         |  64.72 KiB (1%) |          18 |
| `["append!!", "xf"]`                     |  19.801 μs (5%) |         |  64.72 KiB (1%) |          18 |
| `["cat", "base"]`                        |   1.730 μs (5%) |         |                 |             |
| `["cat", "xf"]`                          |   2.350 μs (5%) |         |                 |             |
| `["collect", "filter-missing"]`          | 117.601 μs (5%) |         | 345.31 KiB (1%) |       10015 |
| `["collect", "identity-float"]`          |  85.901 μs (5%) |         | 569.16 KiB (1%) |       10015 |
| `["collect", "identity-union"]`          | 325.004 μs (5%) |         | 705.17 KiB (1%) |       16668 |
| `["dict", "base"]`                       |   4.051 ms (5%) |         |  92.91 KiB (1%) |          22 |
| `["dict", "xf"]`                         |   4.211 ms (5%) |         |  92.36 KiB (1%) |          21 |
| `["dot", "blas"]`                        |   1.210 μs (5%) |         |                 |             |
| `["dot", "man"]`                         |   1.180 μs (5%) |         |                 |             |
| `["dot", "rf"]`                          |   2.144 μs (5%) |         |                 |             |
| `["dot", "xf"]`                          |   2.211 μs (5%) |         |   64 bytes (1%) |           3 |
| `["filter_map_map!", "man"]`             |  79.601 μs (5%) |         |                 |             |
| `["filter_map_map!", "xf"]`              | 702.007 μs (5%) |         |  304 bytes (1%) |          17 |
| `["filter_map_reduce", "man"]`           | 231.202 μs (5%) |         |                 |             |
| `["filter_map_reduce", "xf"]`            | 229.902 μs (5%) |         |                 |             |
| `["findall", "base"]`                    | 834.609 μs (5%) |         |   2.00 MiB (1%) |          21 |
| `["findall", "xf-array"]`                | 833.109 μs (5%) |         |   2.96 MiB (1%) |       96955 |
| `["findall", "xf-iter"]`                 |   3.346 ms (5%) |         |   9.63 MiB (1%) |      299940 |
| `["gemm", "fusedmul", "blas", "16"]`     |   4.317 ms (5%) |         |                 |             |
| `["gemm", "fusedmul", "blas", "2"]`      |   3.272 ms (5%) |         |                 |             |
| `["gemm", "fusedmul", "blas", "32"]`     |   5.982 ms (5%) |         |                 |             |
| `["gemm", "fusedmul", "blas", "8"]`      |   3.433 ms (5%) |         |                 |             |
| `["gemm", "fusedmul", "xf", "16"]`       |   5.278 ms (5%) |         |  160 bytes (1%) |           6 |
| `["gemm", "fusedmul", "xf", "2"]`        | 656.506 μs (5%) |         |  160 bytes (1%) |           6 |
| `["gemm", "fusedmul", "xf", "32"]`       |  10.523 ms (5%) |         |  160 bytes (1%) |           6 |
| `["gemm", "fusedmul", "xf", "8"]`        |   2.634 ms (5%) |         |  160 bytes (1%) |           6 |
| `["gemm", "mul", "linalg", "256"]`       | 902.509 μs (5%) |         |                 |             |
| `["gemm", "mul", "linalg", "32"]`        |   3.000 μs (5%) |         |                 |             |
| `["gemm", "mul", "linalg", "8"]`         | 200.000 ns (5%) |         |                 |             |
| `["gemm", "mul", "man", "false", "256"]` |   1.545 ms (5%) |         |                 |             |
| `["gemm", "mul", "man", "false", "32"]`  |   4.700 μs (5%) |         |                 |             |
| `["gemm", "mul", "man", "false", "8"]`   | 400.000 ns (5%) |         |                 |             |
| `["gemm", "mul", "man", "ivdep", "256"]` |   1.579 ms (5%) |         |                 |             |
| `["gemm", "mul", "man", "ivdep", "32"]`  |   3.800 μs (5%) |         |                 |             |
| `["gemm", "mul", "man", "ivdep", "8"]`   | 400.000 ns (5%) |         |                 |             |
| `["gemm", "mul", "man", "true", "256"]`  |   1.556 ms (5%) |         |                 |             |
| `["gemm", "mul", "man", "true", "32"]`   |   4.700 μs (5%) |         |                 |             |
| `["gemm", "mul", "man", "true", "8"]`    | 400.000 ns (5%) |         |                 |             |
| `["gemm", "mul", "xf", "false", "256"]`  |   1.547 ms (5%) |         |   48 bytes (1%) |           2 |
| `["gemm", "mul", "xf", "false", "32"]`   |   4.700 μs (5%) |         |   48 bytes (1%) |           2 |
| `["gemm", "mul", "xf", "false", "8"]`    | 400.000 ns (5%) |         |   48 bytes (1%) |           2 |
| `["gemm", "mul", "xf", "ivdep", "256"]`  |   1.596 ms (5%) |         |   48 bytes (1%) |           2 |
| `["gemm", "mul", "xf", "ivdep", "32"]`   |   3.900 μs (5%) |         |   48 bytes (1%) |           2 |
| `["gemm", "mul", "xf", "ivdep", "8"]`    | 300.000 ns (5%) |         |   48 bytes (1%) |           2 |
| `["gemm", "mul", "xf", "true", "256"]`   |   1.534 ms (5%) |         |   48 bytes (1%) |           2 |
| `["gemm", "mul", "xf", "true", "32"]`    |   5.400 μs (5%) |         |   48 bytes (1%) |           2 |
| `["gemm", "mul", "xf", "true", "8"]`     | 400.000 ns (5%) |         |   48 bytes (1%) |           2 |
| `["groupby", "sum", "sac"]`              | 250.102 μs (5%) |         | 313.14 KiB (1%) |       10007 |
| `["groupby", "sum", "xf-with-init"]`     | 195.401 μs (5%) |         | 157.44 KiB (1%) |       10008 |
| `["groupby", "sum", "xf-without-init"]`  | 190.401 μs (5%) |         | 157.44 KiB (1%) |       10008 |
| `["mapcat_eduction", "base"]`            |   1.880 μs (5%) |         |                 |             |
| `["mapcat_eduction", "xf-eduction"]`     |   2.020 μs (5%) |         |                 |             |
| `["mapcat_eduction", "xf-xf"]`           |   2.022 μs (5%) |         |                 |             |
| `["missing_argmax", "man"]`              |   2.678 μs (5%) |         |   32 bytes (1%) |           1 |
| `["missing_argmax", "rf"]`               |   2.563 μs (5%) |         |   32 bytes (1%) |           1 |
| `["missing_argmax", "xf"]`               |   3.189 μs (5%) |         |   32 bytes (1%) |           1 |
| `["missing_dot", "equiv"]`               |   1.640 μs (5%) |         |   16 bytes (1%) |           1 |
| `["missing_dot", "man"]`                 |   1.390 μs (5%) |         |   16 bytes (1%) |           1 |
| `["missing_dot", "naive"]`               |   4.871 μs (5%) |         |   16 bytes (1%) |           1 |
| `["missing_dot", "rf"]`                  |   1.420 μs (5%) |         |   16 bytes (1%) |           1 |
| `["missing_dot", "rf_nota"]`             |   1.670 μs (5%) |         |   16 bytes (1%) |           1 |
| `["missing_dot", "xf"]`                  | 208.302 μs (5%) |         |  71.98 KiB (1%) |        3736 |
| `["missing_dot", "xf_nota"]`             | 210.802 μs (5%) |         |  72.02 KiB (1%) |        3738 |
| `["overhead", "foldl"]`                  |   4.700 ns (5%) |         |                 |             |
| `["overhead", "reduce_basecase"]`        | 183.640 ns (5%) |         |  416 bytes (1%) |           7 |
| `["partition_by", "man"]`                |   2.075 ms (5%) |         |  352 bytes (1%) |           4 |
| `["partition_by", "xf"]`                 |   3.172 ms (5%) |         |   6.10 MiB (1%) |      200007 |
| `["set", "base"]`                        |   4.786 ms (5%) |         |  49.58 KiB (1%) |          18 |
| `["set", "xf"]`                          |   4.505 ms (5%) |         |  49.63 KiB (1%) |          21 |

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
  CPU: Intel(R) Xeon(R) Platinum 8272CL CPU @ 2.60GHz: 
              speed         user         nice          sys         idle          irq
       #1  2593 MHz      56195 s          0 s       1500 s      83109 s          0 s
       #2  2593 MHz      36064 s          0 s       1732 s      99391 s          0 s
       
  Memory: 6.791385650634766 GB (2900.8828125 MB free)
  Uptime: 1458.0 sec
  Load Avg:  1.0  1.0  0.78125
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
    Model name:          Intel(R) Xeon(R) Platinum 8272CL CPU @ 2.60GHz
    Stepping:            7
    CPU MHz:             2593.906
    BogoMIPS:            5187.81
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
| Brand              | Intel(R) Xeon(R) Platinum 8272CL CPU @ 2.60GHz          |
| Vendor             | :Intel                                                  |
| Architecture       | :Skylake                                                |
| Model              | Family: 0x06, Model: 0x55, Stepping: 0x07, Type: 0x00   |
| Cores              | 2 physical cores, 2 logical cores (on executing CPU)    |
|                    | No Hyperthreading detected                              |
| Clock Frequencies  | Not supported by CPU                                    |
| Data Cache         | Level 1:3 : (32, 1024, 36608) kbytes                    |
|                    | 64 byte cache line size                                 |
| Address Size       | 48 bits virtual, 46 bits physical                       |
| SIMD               | 512 bit = 64 byte max. SIMD vector size                 |
| Time Stamp Counter | TSC is accessible via `rdtsc`                           |
|                    | TSC increased at every clock cycle (non-invariant TSC)  |
| Perf. Monitoring   | Performance Monitoring Counters (PMC) are not supported |
| Hypervisor         | Yes, Microsoft                                          |

