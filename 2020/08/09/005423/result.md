# Benchmark result

* Pull request commit: [`4d15a06c7487ae5a2c4612a9cf929666ec9ca823`](https://github.com/JuliaFolds/Transducers.jl/commit/4d15a06c7487ae5a2c4612a9cf929666ec9ca823)
* Pull request: <https://github.com/JuliaFolds/Transducers.jl/pull/401> ("Nested loops" for threaded fold; option to convert Cat to TCat)

# Judge result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmarks:
    - Target: 9 Aug 2020 - 00:49
    - Baseline: 9 Aug 2020 - 00:53
* Package commits:
    - Target: 9b0bf8
    - Baseline: f87cd6
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
| `["append!!", "eduction"]`               | 0.95 (5%) :white_check_mark: |   1.00 (1%)  |
| `["cat", "base"]`                        | 0.92 (5%) :white_check_mark: |   1.00 (1%)  |
| `["dict", "base"]`                       | 0.79 (5%) :white_check_mark: |   1.00 (1%)  |
| `["dict", "xf"]`                         | 0.88 (5%) :white_check_mark: |   1.00 (1%)  |
| `["filter_map_map!", "man"]`             | 0.86 (5%) :white_check_mark: |   1.00 (1%)  |
| `["findall", "xf-iter"]`                 |                1.05 (5%) :x: |   1.00 (1%)  |
| `["gemm", "fusedmul", "blas", "16"]`     |                1.05 (5%) :x: |   1.00 (1%)  |
| `["gemm", "fusedmul", "blas", "2"]`      |                1.06 (5%) :x: |   1.00 (1%)  |
| `["gemm", "fusedmul", "xf", "2"]`        | 0.79 (5%) :white_check_mark: |   1.00 (1%)  |
| `["gemm", "mul", "man", "false", "32"]`  | 0.92 (5%) :white_check_mark: |   1.00 (1%)  |
| `["gemm", "mul", "man", "false", "8"]`   |                1.07 (5%) :x: |   1.00 (1%)  |
| `["gemm", "mul", "man", "ivdep", "8"]`   |                1.07 (5%) :x: |   1.00 (1%)  |
| `["gemm", "mul", "man", "true", "8"]`    |                1.36 (5%) :x: |   1.00 (1%)  |
| `["gemm", "mul", "xf", "false", "32"]`   | 0.91 (5%) :white_check_mark: |   1.00 (1%)  |
| `["gemm", "mul", "xf", "false", "8"]`    |                1.05 (5%) :x: |   1.00 (1%)  |
| `["gemm", "mul", "xf", "ivdep", "32"]`   | 0.88 (5%) :white_check_mark: |   1.00 (1%)  |
| `["gemm", "mul", "xf", "ivdep", "8"]`    |                1.26 (5%) :x: |   1.00 (1%)  |
| `["gemm", "mul", "xf", "true", "32"]`    | 0.94 (5%) :white_check_mark: |   1.00 (1%)  |
| `["gemm", "mul", "xf", "true", "8"]`     |                1.06 (5%) :x: |   1.00 (1%)  |
| `["groupby", "sum", "sac"]`              |                1.08 (5%) :x: |   1.00 (1%)  |
| `["groupby", "sum", "xf-with-init"]`     |                1.09 (5%) :x: |   1.00 (1%)  |
| `["groupby", "sum", "xf-without-init"]`  |                1.10 (5%) :x: |   1.00 (1%)  |
| `["mapcat_eduction", "xf-xf"]`           |                1.08 (5%) :x: |   1.00 (1%)  |
| `["missing_dot", "equiv"]`               | 0.91 (5%) :white_check_mark: |   1.00 (1%)  |
| `["missing_dot", "rf_nota"]`             | 0.93 (5%) :white_check_mark: |   1.00 (1%)  |
| `["overhead", "foldl"]`                  |                1.13 (5%) :x: |   1.00 (1%)  |
| `["set", "base"]`                        |                1.06 (5%) :x: |   1.00 (1%)  |

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
       #1  2095 MHz      20370 s          0 s       1202 s      57070 s          0 s
       #2  2095 MHz      47581 s          0 s       1952 s      28894 s          0 s
       
  Memory: 6.764881134033203 GB (2943.54296875 MB free)
  Uptime: 802.0 sec
  Load Avg:  1.00048828125  0.9580078125  0.62158203125
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
       #1  2095 MHz      21901 s          0 s       1270 s      83742 s          0 s
       #2  2095 MHz      74216 s          0 s       2148 s      30352 s          0 s
       
  Memory: 6.764881134033203 GB (2830.26953125 MB free)
  Uptime: 1086.0 sec
  Load Avg:  1.01904296875  1.00830078125  0.74072265625
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-8.0.1 (ORCJIT, skylake)
```

---
# Target result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmark: 9 Aug 2020 - 0:49
* Package commit: 9b0bf8
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
| `["append!!", "eduction"]`               |  17.201 μs (5%) |         |  64.72 KiB (1%) |          18 |
| `["append!!", "xf"]`                     |  16.701 μs (5%) |         |  64.72 KiB (1%) |          18 |
| `["cat", "base"]`                        |   1.440 μs (5%) |         |                 |             |
| `["cat", "xf"]`                          |   1.660 μs (5%) |         |                 |             |
| `["collect", "filter-missing"]`          |  91.806 μs (5%) |         | 345.31 KiB (1%) |       10015 |
| `["collect", "identity-float"]`          |  65.704 μs (5%) |         | 569.16 KiB (1%) |       10015 |
| `["collect", "identity-union"]`          | 265.317 μs (5%) |         | 704.95 KiB (1%) |       16656 |
| `["dict", "base"]`                       |   3.555 ms (5%) |         |  92.91 KiB (1%) |          22 |
| `["dict", "xf"]`                         |   3.576 ms (5%) |         |  92.36 KiB (1%) |          21 |
| `["dot", "blas"]`                        |   1.030 μs (5%) |         |                 |             |
| `["dot", "man"]`                         |   1.040 μs (5%) |         |                 |             |
| `["dot", "rf"]`                          |   1.820 μs (5%) |         |                 |             |
| `["dot", "xf"]`                          |   1.880 μs (5%) |         |   64 bytes (1%) |           3 |
| `["filter_map_map!", "man"]`             |  57.102 μs (5%) |         |                 |             |
| `["filter_map_map!", "xf"]`              | 591.328 μs (5%) |         |  304 bytes (1%) |          17 |
| `["filter_map_reduce", "man"]`           | 191.911 μs (5%) |         |                 |             |
| `["filter_map_reduce", "xf"]`            | 191.911 μs (5%) |         |                 |             |
| `["findall", "base"]`                    | 710.345 μs (5%) |         |   2.00 MiB (1%) |          21 |
| `["findall", "xf-array"]`                | 665.441 μs (5%) |         |   3.06 MiB (1%) |      100064 |
| `["findall", "xf-iter"]`                 | 794.948 μs (5%) |         |   5.05 MiB (1%) |       99925 |
| `["gemm", "fusedmul", "blas", "16"]`     |   4.119 ms (5%) |         |                 |             |
| `["gemm", "fusedmul", "blas", "2"]`      |   3.200 ms (5%) |         |                 |             |
| `["gemm", "fusedmul", "blas", "32"]`     |   5.893 ms (5%) |         |                 |             |
| `["gemm", "fusedmul", "blas", "8"]`      |   3.108 ms (5%) |         |                 |             |
| `["gemm", "fusedmul", "xf", "16"]`       |   5.381 ms (5%) |         |  160 bytes (1%) |           6 |
| `["gemm", "fusedmul", "xf", "2"]`        | 490.224 μs (5%) |         |  160 bytes (1%) |           6 |
| `["gemm", "fusedmul", "xf", "32"]`       |  10.855 ms (5%) |         |  160 bytes (1%) |           6 |
| `["gemm", "fusedmul", "xf", "8"]`        |   2.520 ms (5%) |         |  160 bytes (1%) |           6 |
| `["gemm", "mul", "linalg", "256"]`       | 746.741 μs (5%) |         |                 |             |
| `["gemm", "mul", "linalg", "32"]`        |   2.511 μs (5%) |         |                 |             |
| `["gemm", "mul", "linalg", "8"]`         | 201.589 ns (5%) |         |                 |             |
| `["gemm", "mul", "man", "false", "256"]` |   1.332 ms (5%) |         |                 |             |
| `["gemm", "mul", "man", "false", "32"]`  |   3.763 μs (5%) |         |                 |             |
| `["gemm", "mul", "man", "false", "8"]`   | 319.755 ns (5%) |         |                 |             |
| `["gemm", "mul", "man", "ivdep", "256"]` |   1.356 ms (5%) |         |                 |             |
| `["gemm", "mul", "man", "ivdep", "32"]`  |   3.263 μs (5%) |         |                 |             |
| `["gemm", "mul", "man", "ivdep", "8"]`   | 319.760 ns (5%) |         |                 |             |
| `["gemm", "mul", "man", "true", "256"]`  |   1.338 ms (5%) |         |                 |             |
| `["gemm", "mul", "man", "true", "32"]`   |   4.172 μs (5%) |         |                 |             |
| `["gemm", "mul", "man", "true", "8"]`    | 409.020 ns (5%) |         |                 |             |
| `["gemm", "mul", "xf", "false", "256"]`  |   1.334 ms (5%) |         |   48 bytes (1%) |           2 |
| `["gemm", "mul", "xf", "false", "32"]`   |   3.650 μs (5%) |         |   48 bytes (1%) |           2 |
| `["gemm", "mul", "xf", "false", "8"]`    | 316.440 ns (5%) |         |   48 bytes (1%) |           2 |
| `["gemm", "mul", "xf", "ivdep", "256"]`  |   1.373 ms (5%) |         |   48 bytes (1%) |           2 |
| `["gemm", "mul", "xf", "ivdep", "32"]`   |   3.163 μs (5%) |         |   48 bytes (1%) |           2 |
| `["gemm", "mul", "xf", "ivdep", "8"]`    | 377.743 ns (5%) |         |   48 bytes (1%) |           2 |
| `["gemm", "mul", "xf", "true", "256"]`   |   1.324 ms (5%) |         |   48 bytes (1%) |           2 |
| `["gemm", "mul", "xf", "true", "32"]`    |   3.950 μs (5%) |         |   48 bytes (1%) |           2 |
| `["gemm", "mul", "xf", "true", "8"]`     | 317.614 ns (5%) |         |   48 bytes (1%) |           2 |
| `["groupby", "sum", "sac"]`              | 229.611 μs (5%) |         | 313.14 KiB (1%) |       10007 |
| `["groupby", "sum", "xf-with-init"]`     | 165.307 μs (5%) |         | 157.44 KiB (1%) |       10008 |
| `["groupby", "sum", "xf-without-init"]`  | 172.507 μs (5%) |         | 157.44 KiB (1%) |       10008 |
| `["mapcat_eduction", "base"]`            |   1.550 μs (5%) |         |                 |             |
| `["mapcat_eduction", "xf-eduction"]`     |   1.570 μs (5%) |         |                 |             |
| `["mapcat_eduction", "xf-xf"]`           |   1.680 μs (5%) |         |                 |             |
| `["missing_argmax", "man"]`              |   2.233 μs (5%) |         |   32 bytes (1%) |           1 |
| `["missing_argmax", "rf"]`               |   2.689 μs (5%) |         |   32 bytes (1%) |           1 |
| `["missing_argmax", "xf"]`               |   2.156 μs (5%) |         |   32 bytes (1%) |           1 |
| `["missing_dot", "equiv"]`               |   1.250 μs (5%) |         |   16 bytes (1%) |           1 |
| `["missing_dot", "man"]`                 |   1.160 μs (5%) |         |   16 bytes (1%) |           1 |
| `["missing_dot", "naive"]`               |   4.063 μs (5%) |         |   16 bytes (1%) |           1 |
| `["missing_dot", "rf"]`                  |   1.140 μs (5%) |         |   16 bytes (1%) |           1 |
| `["missing_dot", "rf_nota"]`             |   1.270 μs (5%) |         |   16 bytes (1%) |           1 |
| `["missing_dot", "xf"]`                  | 176.410 μs (5%) |         |  72.09 KiB (1%) |        3740 |
| `["missing_dot", "xf_nota"]`             | 176.010 μs (5%) |         |  72.20 KiB (1%) |        3746 |
| `["overhead", "foldl"]`                  |   4.400 ns (5%) |         |                 |             |
| `["overhead", "reduce_basecase"]`        | 222.188 ns (5%) |         |  464 bytes (1%) |           9 |
| `["partition_by", "man"]`                |   1.800 ms (5%) |         |  352 bytes (1%) |           4 |
| `["partition_by", "xf"]`                 |   2.960 ms (5%) |         |   6.10 MiB (1%) |      200007 |
| `["set", "base"]`                        |   4.535 ms (5%) |         |  49.58 KiB (1%) |          18 |
| `["set", "xf"]`                          |   4.019 ms (5%) |         |  49.63 KiB (1%) |          21 |

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
       #1  2095 MHz      20370 s          0 s       1202 s      57070 s          0 s
       #2  2095 MHz      47581 s          0 s       1952 s      28894 s          0 s
       
  Memory: 6.764881134033203 GB (2943.54296875 MB free)
  Uptime: 802.0 sec
  Load Avg:  1.00048828125  0.9580078125  0.62158203125
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-8.0.1 (ORCJIT, skylake)
```

---
# Baseline result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmark: 9 Aug 2020 - 0:53
* Package commit: f87cd6
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
| `["append!!", "eduction"]`               |  18.201 μs (5%) |         |  64.72 KiB (1%) |          18 |
| `["append!!", "xf"]`                     |  16.701 μs (5%) |         |  64.72 KiB (1%) |          18 |
| `["cat", "base"]`                        |   1.560 μs (5%) |         |                 |             |
| `["cat", "xf"]`                          |   1.650 μs (5%) |         |                 |             |
| `["collect", "filter-missing"]`          |  94.104 μs (5%) |         | 345.31 KiB (1%) |       10015 |
| `["collect", "identity-float"]`          |  68.203 μs (5%) |         | 569.16 KiB (1%) |       10015 |
| `["collect", "identity-union"]`          | 268.311 μs (5%) |         | 705.36 KiB (1%) |       16682 |
| `["dict", "base"]`                       |   4.475 ms (5%) |         |  92.91 KiB (1%) |          22 |
| `["dict", "xf"]`                         |   4.073 ms (5%) |         |  92.36 KiB (1%) |          21 |
| `["dot", "blas"]`                        |   1.020 μs (5%) |         |                 |             |
| `["dot", "man"]`                         |   1.070 μs (5%) |         |                 |             |
| `["dot", "rf"]`                          |   1.790 μs (5%) |         |                 |             |
| `["dot", "xf"]`                          |   1.860 μs (5%) |         |   64 bytes (1%) |           3 |
| `["filter_map_map!", "man"]`             |  66.106 μs (5%) |         |                 |             |
| `["filter_map_map!", "xf"]`              | 589.753 μs (5%) |         |  304 bytes (1%) |          17 |
| `["filter_map_reduce", "man"]`           | 191.908 μs (5%) |         |                 |             |
| `["filter_map_reduce", "xf"]`            | 191.808 μs (5%) |         |                 |             |
| `["findall", "base"]`                    | 731.631 μs (5%) |         |   2.00 MiB (1%) |          21 |
| `["findall", "xf-array"]`                | 660.828 μs (5%) |         |   3.05 MiB (1%) |       99774 |
| `["findall", "xf-iter"]`                 | 755.433 μs (5%) |         |   5.05 MiB (1%) |       99909 |
| `["gemm", "fusedmul", "blas", "16"]`     |   3.910 ms (5%) |         |                 |             |
| `["gemm", "fusedmul", "blas", "2"]`      |   3.011 ms (5%) |         |                 |             |
| `["gemm", "fusedmul", "blas", "32"]`     |   5.656 ms (5%) |         |                 |             |
| `["gemm", "fusedmul", "blas", "8"]`      |   3.139 ms (5%) |         |                 |             |
| `["gemm", "fusedmul", "xf", "16"]`       |   5.209 ms (5%) |         |  160 bytes (1%) |           6 |
| `["gemm", "fusedmul", "xf", "2"]`        | 622.859 μs (5%) |         |  160 bytes (1%) |           6 |
| `["gemm", "fusedmul", "xf", "32"]`       |  10.712 ms (5%) |         |  160 bytes (1%) |           6 |
| `["gemm", "fusedmul", "xf", "8"]`        |   2.619 ms (5%) |         |  160 bytes (1%) |           6 |
| `["gemm", "mul", "linalg", "256"]`       | 749.131 μs (5%) |         |                 |             |
| `["gemm", "mul", "linalg", "32"]`        |   2.500 μs (5%) |         |                 |             |
| `["gemm", "mul", "linalg", "8"]`         | 200.000 ns (5%) |         |                 |             |
| `["gemm", "mul", "man", "false", "256"]` |   1.367 ms (5%) |         |                 |             |
| `["gemm", "mul", "man", "false", "32"]`  |   4.100 μs (5%) |         |                 |             |
| `["gemm", "mul", "man", "false", "8"]`   | 300.000 ns (5%) |         |                 |             |
| `["gemm", "mul", "man", "ivdep", "256"]` |   1.389 ms (5%) |         |                 |             |
| `["gemm", "mul", "man", "ivdep", "32"]`  |   3.300 μs (5%) |         |                 |             |
| `["gemm", "mul", "man", "ivdep", "8"]`   | 300.000 ns (5%) |         |                 |             |
| `["gemm", "mul", "man", "true", "256"]`  |   1.373 ms (5%) |         |                 |             |
| `["gemm", "mul", "man", "true", "32"]`   |   4.201 μs (5%) |         |                 |             |
| `["gemm", "mul", "man", "true", "8"]`    | 300.000 ns (5%) |         |                 |             |
| `["gemm", "mul", "xf", "false", "256"]`  |   1.364 ms (5%) |         |   48 bytes (1%) |           2 |
| `["gemm", "mul", "xf", "false", "32"]`   |   4.000 μs (5%) |         |   48 bytes (1%) |           2 |
| `["gemm", "mul", "xf", "false", "8"]`    | 300.000 ns (5%) |         |   48 bytes (1%) |           2 |
| `["gemm", "mul", "xf", "ivdep", "256"]`  |   1.398 ms (5%) |         |   48 bytes (1%) |           2 |
| `["gemm", "mul", "xf", "ivdep", "32"]`   |   3.600 μs (5%) |         |   48 bytes (1%) |           2 |
| `["gemm", "mul", "xf", "ivdep", "8"]`    | 300.000 ns (5%) |         |   48 bytes (1%) |           2 |
| `["gemm", "mul", "xf", "true", "256"]`   |   1.373 ms (5%) |         |   48 bytes (1%) |           2 |
| `["gemm", "mul", "xf", "true", "32"]`    |   4.200 μs (5%) |         |   48 bytes (1%) |           2 |
| `["gemm", "mul", "xf", "true", "8"]`     | 300.000 ns (5%) |         |   48 bytes (1%) |           2 |
| `["groupby", "sum", "sac"]`              | 212.418 μs (5%) |         | 313.14 KiB (1%) |       10007 |
| `["groupby", "sum", "xf-with-init"]`     | 152.314 μs (5%) |         | 157.44 KiB (1%) |       10008 |
| `["groupby", "sum", "xf-without-init"]`  | 157.114 μs (5%) |         | 157.44 KiB (1%) |       10008 |
| `["mapcat_eduction", "base"]`            |   1.550 μs (5%) |         |                 |             |
| `["mapcat_eduction", "xf-eduction"]`     |   1.560 μs (5%) |         |                 |             |
| `["mapcat_eduction", "xf-xf"]`           |   1.560 μs (5%) |         |                 |             |
| `["missing_argmax", "man"]`              |   2.233 μs (5%) |         |   32 bytes (1%) |           1 |
| `["missing_argmax", "rf"]`               |   2.700 μs (5%) |         |   32 bytes (1%) |           1 |
| `["missing_argmax", "xf"]`               |   2.156 μs (5%) |         |   32 bytes (1%) |           1 |
| `["missing_dot", "equiv"]`               |   1.370 μs (5%) |         |   16 bytes (1%) |           1 |
| `["missing_dot", "man"]`                 |   1.130 μs (5%) |         |   16 bytes (1%) |           1 |
| `["missing_dot", "naive"]`               |   4.113 μs (5%) |         |   16 bytes (1%) |           1 |
| `["missing_dot", "rf"]`                  |   1.160 μs (5%) |         |   16 bytes (1%) |           1 |
| `["missing_dot", "rf_nota"]`             |   1.370 μs (5%) |         |   16 bytes (1%) |           1 |
| `["missing_dot", "xf"]`                  | 176.507 μs (5%) |         |  71.91 KiB (1%) |        3732 |
| `["missing_dot", "xf_nota"]`             | 176.407 μs (5%) |         |  71.98 KiB (1%) |        3736 |
| `["overhead", "foldl"]`                  |   3.900 ns (5%) |         |                 |             |
| `["overhead", "reduce_basecase"]`        | 225.743 ns (5%) |         |  464 bytes (1%) |           9 |
| `["partition_by", "man"]`                |   1.754 ms (5%) |         |  352 bytes (1%) |           4 |
| `["partition_by", "xf"]`                 |   2.952 ms (5%) |         |   6.10 MiB (1%) |      200007 |
| `["set", "base"]`                        |   4.283 ms (5%) |         |  49.58 KiB (1%) |          18 |
| `["set", "xf"]`                          |   3.949 ms (5%) |         |  49.63 KiB (1%) |          21 |

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
       #1  2095 MHz      21901 s          0 s       1270 s      83742 s          0 s
       #2  2095 MHz      74216 s          0 s       2148 s      30352 s          0 s
       
  Memory: 6.764881134033203 GB (2830.26953125 MB free)
  Uptime: 1086.0 sec
  Load Avg:  1.01904296875  1.00830078125  0.74072265625
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
    CPU MHz:             2095.195
    BogoMIPS:            4190.39
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

