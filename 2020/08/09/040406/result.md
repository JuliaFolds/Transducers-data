# Benchmark result

* Pull request commit: [`19b3fe35c3b8aa1d04d925723f99b076448f7d26`](https://github.com/JuliaFolds/Transducers.jl/commit/19b3fe35c3b8aa1d04d925723f99b076448f7d26)
* Pull request: <https://github.com/JuliaFolds/Transducers.jl/pull/404> (Add bench_filter_sum.jl)

# Judge result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmarks:
    - Target: 9 Aug 2020 - 03:59
    - Baseline: 9 Aug 2020 - 04:03
* Package commits:
    - Target: 1af824
    - Baseline: 061a65
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
| `["cat", "base"]`                        | 0.94 (5%) :white_check_mark: |   1.00 (1%)  |
| `["cat", "xf"]`                          | 0.87 (5%) :white_check_mark: |   1.00 (1%)  |
| `["dict", "xf"]`                         |                1.06 (5%) :x: |   1.00 (1%)  |
| `["dot", "rf"]`                          |                1.12 (5%) :x: |   1.00 (1%)  |
| `["filter_map_map!", "xf"]`              | 0.92 (5%) :white_check_mark: |   1.00 (1%)  |
| `["filter_map_reduce", "man"]`           | 0.88 (5%) :white_check_mark: |   1.00 (1%)  |
| `["findall", "xf-array"]`                | 0.89 (5%) :white_check_mark: |   1.00 (1%)  |
| `["findall", "xf-iter"]`                 | 0.93 (5%) :white_check_mark: |   1.00 (1%)  |
| `["gemm", "fusedmul", "blas", "32"]`     | 0.94 (5%) :white_check_mark: |   1.00 (1%)  |
| `["gemm", "fusedmul", "blas", "8"]`      | 0.93 (5%) :white_check_mark: |   1.00 (1%)  |
| `["gemm", "fusedmul", "xf", "16"]`       | 0.84 (5%) :white_check_mark: |   1.00 (1%)  |
| `["gemm", "fusedmul", "xf", "2"]`        | 0.90 (5%) :white_check_mark: |   1.00 (1%)  |
| `["gemm", "fusedmul", "xf", "32"]`       | 0.94 (5%) :white_check_mark: |   1.00 (1%)  |
| `["gemm", "fusedmul", "xf", "8"]`        | 0.94 (5%) :white_check_mark: |   1.00 (1%)  |
| `["gemm", "mul", "linalg", "32"]`        |                1.11 (5%) :x: |   1.00 (1%)  |
| `["gemm", "mul", "linalg", "8"]`         | 0.79 (5%) :white_check_mark: |   1.00 (1%)  |
| `["gemm", "mul", "man", "false", "256"]` | 0.91 (5%) :white_check_mark: |   1.00 (1%)  |
| `["gemm", "mul", "man", "false", "8"]`   |                1.16 (5%) :x: |   1.00 (1%)  |
| `["gemm", "mul", "man", "ivdep", "8"]`   | 0.92 (5%) :white_check_mark: |   1.00 (1%)  |
| `["gemm", "mul", "man", "true", "256"]`  | 0.83 (5%) :white_check_mark: |   1.00 (1%)  |
| `["gemm", "mul", "man", "true", "32"]`   | 0.87 (5%) :white_check_mark: |   1.00 (1%)  |
| `["gemm", "mul", "man", "true", "8"]`    | 0.88 (5%) :white_check_mark: |   1.00 (1%)  |
| `["gemm", "mul", "xf", "false", "256"]`  | 0.88 (5%) :white_check_mark: |   1.00 (1%)  |
| `["gemm", "mul", "xf", "false", "8"]`    |                1.05 (5%) :x: |   1.00 (1%)  |
| `["gemm", "mul", "xf", "ivdep", "256"]`  | 0.86 (5%) :white_check_mark: |   1.00 (1%)  |
| `["gemm", "mul", "xf", "ivdep", "8"]`    | 0.80 (5%) :white_check_mark: |   1.00 (1%)  |
| `["gemm", "mul", "xf", "true", "256"]`   | 0.93 (5%) :white_check_mark: |   1.00 (1%)  |
| `["gemm", "mul", "xf", "true", "8"]`     |                1.18 (5%) :x: |   1.00 (1%)  |
| `["groupby", "sum", "sac"]`              |                1.09 (5%) :x: |   1.00 (1%)  |
| `["missing_argmax", "rf"]`               |                1.09 (5%) :x: |   1.00 (1%)  |
| `["missing_dot", "man"]`                 | 0.89 (5%) :white_check_mark: |   1.00 (1%)  |
| `["missing_dot", "rf"]`                  | 0.91 (5%) :white_check_mark: |   1.00 (1%)  |
| `["missing_dot", "rf_nota"]`             | 0.92 (5%) :white_check_mark: |   1.00 (1%)  |
| `["missing_dot", "xf_nota"]`             | 0.93 (5%) :white_check_mark: |   1.00 (1%)  |
| `["set", "base"]`                        | 0.93 (5%) :white_check_mark: |   1.00 (1%)  |

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
       #1  2095 MHz      52240 s          0 s       1377 s      20007 s          0 s
       #2  2095 MHz      16947 s          0 s       1773 s      55305 s          0 s
       
  Memory: 6.764881134033203 GB (2954.17578125 MB free)
  Uptime: 757.0 sec
  Load Avg:  1.03369140625  1.0126953125  0.65283203125
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
       #1  2095 MHz      53494 s          0 s       1446 s      45903 s          0 s
       #2  2095 MHz      42804 s          0 s       1933 s      56490 s          0 s
       
  Memory: 6.764881134033203 GB (2836.12109375 MB free)
  Uptime: 1030.0 sec
  Load Avg:  1.03564453125  1.01220703125  0.75634765625
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-8.0.1 (ORCJIT, skylake)
```

---
# Target result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmark: 9 Aug 2020 - 3:59
* Package commit: 1af824
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

| ID                                                                          | time            | GC time | memory          | allocations |
|-----------------------------------------------------------------------------|----------------:|--------:|----------------:|------------:|
| `["append!!", "eduction"]`                                                  |  18.100 μs (5%) |         |  64.72 KiB (1%) |          18 |
| `["append!!", "xf"]`                                                        |  19.800 μs (5%) |         |  64.72 KiB (1%) |          18 |
| `["cat", "base"]`                                                           |   1.820 μs (5%) |         |                 |             |
| `["cat", "xf"]`                                                             |   1.922 μs (5%) |         |                 |             |
| `["collect", "filter-missing"]`                                             | 107.901 μs (5%) |         | 345.31 KiB (1%) |       10015 |
| `["collect", "identity-float"]`                                             |  74.100 μs (5%) |         | 569.16 KiB (1%) |       10015 |
| `["collect", "identity-union"]`                                             | 294.901 μs (5%) |         | 704.83 KiB (1%) |       16646 |
| `["dict", "base"]`                                                          |   4.168 ms (5%) |         |  92.91 KiB (1%) |          22 |
| `["dict", "xf"]`                                                            |   4.355 ms (5%) |         |  92.36 KiB (1%) |          21 |
| `["dot", "blas"]`                                                           |   1.330 μs (5%) |         |                 |             |
| `["dot", "man"]`                                                            |   1.300 μs (5%) |         |                 |             |
| `["dot", "rf"]`                                                             |   2.378 μs (5%) |         |                 |             |
| `["dot", "xf"]`                                                             |   2.200 μs (5%) |         |   64 bytes (1%) |           3 |
| `["filter_map_map!", "man"]`                                                |  68.401 μs (5%) |         |                 |             |
| `["filter_map_map!", "xf"]`                                                 | 687.303 μs (5%) |         |  304 bytes (1%) |          17 |
| `["filter_map_reduce", "man"]`                                              | 223.001 μs (5%) |         |                 |             |
| `["filter_map_reduce", "xf"]`                                               | 222.800 μs (5%) |         |                 |             |
| `["filter_sum", ":xs => :floats", ":withinit => false", ":impl => :base"]`  |   3.313 μs (5%) |         |                 |             |
| `["filter_sum", ":xs => :floats", ":withinit => false", ":impl => :naive"]` |   1.450 μs (5%) |         |                 |             |
| `["filter_sum", ":xs => :floats", ":withinit => false", ":impl => :xf"]`    |   1.490 μs (5%) |         |                 |             |
| `["filter_sum", ":xs => :floats", ":withinit => true", ":impl => :base"]`   |   1.410 μs (5%) |         |                 |             |
| `["filter_sum", ":xs => :floats", ":withinit => true", ":impl => :naive"]`  |   1.440 μs (5%) |         |                 |             |
| `["filter_sum", ":xs => :floats", ":withinit => true", ":impl => :xf"]`     |   1.410 μs (5%) |         |                 |             |
| `["filter_sum", ":xs => :ints", ":withinit => false", ":impl => :base"]`    |   1.760 μs (5%) |         |                 |             |
| `["filter_sum", ":xs => :ints", ":withinit => false", ":impl => :naive"]`   | 813.333 ns (5%) |         |                 |             |
| `["filter_sum", ":xs => :ints", ":withinit => false", ":impl => :xf"]`      |   1.560 μs (5%) |         |                 |             |
| `["filter_sum", ":xs => :ints", ":withinit => true", ":impl => :base"]`     | 114.815 ns (5%) |         |                 |             |
| `["filter_sum", ":xs => :ints", ":withinit => true", ":impl => :naive"]`    |   1.010 μs (5%) |         |                 |             |
| `["filter_sum", ":xs => :ints", ":withinit => true", ":impl => :xf"]`       | 122.481 ns (5%) |         |                 |             |
| `["findall", "base"]`                                                       | 810.003 μs (5%) |         |   2.00 MiB (1%) |          21 |
| `["findall", "xf-array"]`                                                   | 765.803 μs (5%) |         |   2.99 MiB (1%) |       97823 |
| `["findall", "xf-iter"]`                                                    | 842.403 μs (5%) |         |   5.05 MiB (1%) |       99931 |
| `["gemm", "fusedmul", "blas", "16"]`                                        |   4.394 ms (5%) |         |                 |             |
| `["gemm", "fusedmul", "blas", "2"]`                                         |   3.451 ms (5%) |         |                 |             |
| `["gemm", "fusedmul", "blas", "32"]`                                        |   5.914 ms (5%) |         |                 |             |
| `["gemm", "fusedmul", "blas", "8"]`                                         |   3.452 ms (5%) |         |                 |             |
| `["gemm", "fusedmul", "xf", "16"]`                                          |   4.407 ms (5%) |         |  160 bytes (1%) |           6 |
| `["gemm", "fusedmul", "xf", "2"]`                                           | 587.902 μs (5%) |         |  160 bytes (1%) |           6 |
| `["gemm", "fusedmul", "xf", "32"]`                                          |  10.048 ms (5%) |         |  160 bytes (1%) |           6 |
| `["gemm", "fusedmul", "xf", "8"]`                                           |   2.582 ms (5%) |         |  160 bytes (1%) |           6 |
| `["gemm", "mul", "linalg", "256"]`                                          | 875.603 μs (5%) |         |                 |             |
| `["gemm", "mul", "linalg", "32"]`                                           |   3.322 μs (5%) |         |                 |             |
| `["gemm", "mul", "linalg", "8"]`                                            | 235.535 ns (5%) |         |                 |             |
| `["gemm", "mul", "man", "false", "256"]`                                    |   1.580 ms (5%) |         |                 |             |
| `["gemm", "mul", "man", "false", "32"]`                                     |   4.729 μs (5%) |         |                 |             |
| `["gemm", "mul", "man", "false", "8"]`                                      | 462.944 ns (5%) |         |                 |             |
| `["gemm", "mul", "man", "ivdep", "256"]`                                    |   1.569 ms (5%) |         |                 |             |
| `["gemm", "mul", "man", "ivdep", "32"]`                                     |   4.200 μs (5%) |         |                 |             |
| `["gemm", "mul", "man", "ivdep", "8"]`                                      | 368.844 ns (5%) |         |                 |             |
| `["gemm", "mul", "man", "true", "256"]`                                     |   1.568 ms (5%) |         |                 |             |
| `["gemm", "mul", "man", "true", "32"]`                                      |   4.243 μs (5%) |         |                 |             |
| `["gemm", "mul", "man", "true", "8"]`                                       | 442.424 ns (5%) |         |                 |             |
| `["gemm", "mul", "xf", "false", "256"]`                                     |   1.581 ms (5%) |         |   48 bytes (1%) |           2 |
| `["gemm", "mul", "xf", "false", "32"]`                                      |   4.743 μs (5%) |         |   48 bytes (1%) |           2 |
| `["gemm", "mul", "xf", "false", "8"]`                                       | 421.106 ns (5%) |         |   48 bytes (1%) |           2 |
| `["gemm", "mul", "xf", "ivdep", "256"]`                                     |   1.556 ms (5%) |         |   48 bytes (1%) |           2 |
| `["gemm", "mul", "xf", "ivdep", "32"]`                                      |   4.063 μs (5%) |         |   48 bytes (1%) |           2 |
| `["gemm", "mul", "xf", "ivdep", "8"]`                                       | 402.000 ns (5%) |         |   48 bytes (1%) |           2 |
| `["gemm", "mul", "xf", "true", "256"]`                                      |   1.583 ms (5%) |         |   48 bytes (1%) |           2 |
| `["gemm", "mul", "xf", "true", "32"]`                                       |   4.986 μs (5%) |         |   48 bytes (1%) |           2 |
| `["gemm", "mul", "xf", "true", "8"]`                                        | 473.474 ns (5%) |         |   48 bytes (1%) |           2 |
| `["groupby", "sum", "sac"]`                                                 | 266.601 μs (5%) |         | 313.14 KiB (1%) |       10007 |
| `["groupby", "sum", "xf-with-init"]`                                        | 200.700 μs (5%) |         | 157.44 KiB (1%) |       10008 |
| `["groupby", "sum", "xf-without-init"]`                                     | 194.201 μs (5%) |         | 157.44 KiB (1%) |       10008 |
| `["mapcat_eduction", "base"]`                                               |   2.078 μs (5%) |         |                 |             |
| `["mapcat_eduction", "xf-eduction"]`                                        |   2.120 μs (5%) |         |                 |             |
| `["mapcat_eduction", "xf-xf"]`                                              |   2.130 μs (5%) |         |                 |             |
| `["missing_argmax", "man"]`                                                 |   2.978 μs (5%) |         |   32 bytes (1%) |           1 |
| `["missing_argmax", "rf"]`                                                  |   2.767 μs (5%) |         |   32 bytes (1%) |           1 |
| `["missing_argmax", "xf"]`                                                  |   2.489 μs (5%) |         |   32 bytes (1%) |           1 |
| `["missing_dot", "equiv"]`                                                  |   1.450 μs (5%) |         |   16 bytes (1%) |           1 |
| `["missing_dot", "man"]`                                                    |   1.330 μs (5%) |         |   16 bytes (1%) |           1 |
| `["missing_dot", "naive"]`                                                  |   4.600 μs (5%) |         |   16 bytes (1%) |           1 |
| `["missing_dot", "rf"]`                                                     |   1.370 μs (5%) |         |   16 bytes (1%) |           1 |
| `["missing_dot", "rf_nota"]`                                                |   1.480 μs (5%) |         |   16 bytes (1%) |           1 |
| `["missing_dot", "xf"]`                                                     | 204.601 μs (5%) |         |  72.33 KiB (1%) |        3750 |
| `["missing_dot", "xf_nota"]`                                                | 203.101 μs (5%) |         |  72.05 KiB (1%) |        3738 |
| `["overhead", "foldl"]`                                                     |   4.800 ns (5%) |         |                 |             |
| `["overhead", "reduce_basecase"]`                                           | 266.412 ns (5%) |         |  464 bytes (1%) |           9 |
| `["partition_by", "man"]`                                                   |   1.930 ms (5%) |         |  352 bytes (1%) |           4 |
| `["partition_by", "xf"]`                                                    |   3.304 ms (5%) |         |   6.10 MiB (1%) |      200007 |
| `["set", "base"]`                                                           |   4.670 ms (5%) |         |  49.58 KiB (1%) |          18 |
| `["set", "xf"]`                                                             |   4.586 ms (5%) |         |  49.63 KiB (1%) |          21 |

## Benchmark Group List
Here's a list of all the benchmark groups executed by this job:

- `["append!!"]`
- `["cat"]`
- `["collect"]`
- `["dict"]`
- `["dot"]`
- `["filter_map_map!"]`
- `["filter_map_reduce"]`
- `["filter_sum", ":xs => :floats", ":withinit => false"]`
- `["filter_sum", ":xs => :floats", ":withinit => true"]`
- `["filter_sum", ":xs => :ints", ":withinit => false"]`
- `["filter_sum", ":xs => :ints", ":withinit => true"]`
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
       #1  2095 MHz      52240 s          0 s       1377 s      20007 s          0 s
       #2  2095 MHz      16947 s          0 s       1773 s      55305 s          0 s
       
  Memory: 6.764881134033203 GB (2954.17578125 MB free)
  Uptime: 757.0 sec
  Load Avg:  1.03369140625  1.0126953125  0.65283203125
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-8.0.1 (ORCJIT, skylake)
```

---
# Baseline result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmark: 9 Aug 2020 - 4:3
* Package commit: 061a65
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
| `["append!!", "eduction"]`               |  17.800 μs (5%) |         |  64.72 KiB (1%) |          18 |
| `["append!!", "xf"]`                     |  19.800 μs (5%) |         |  64.72 KiB (1%) |          18 |
| `["cat", "base"]`                        |   1.930 μs (5%) |         |                 |             |
| `["cat", "xf"]`                          |   2.200 μs (5%) |         |                 |             |
| `["collect", "filter-missing"]`          | 105.901 μs (5%) |         | 345.31 KiB (1%) |       10015 |
| `["collect", "identity-float"]`          |  77.801 μs (5%) |         | 569.16 KiB (1%) |       10015 |
| `["collect", "identity-union"]`          | 299.601 μs (5%) |         | 704.95 KiB (1%) |       16656 |
| `["dict", "base"]`                       |   4.064 ms (5%) |         |  92.91 KiB (1%) |          22 |
| `["dict", "xf"]`                         |   4.118 ms (5%) |         |  92.36 KiB (1%) |          21 |
| `["dot", "blas"]`                        |   1.360 μs (5%) |         |                 |             |
| `["dot", "man"]`                         |   1.310 μs (5%) |         |                 |             |
| `["dot", "rf"]`                          |   2.122 μs (5%) |         |                 |             |
| `["dot", "xf"]`                          |   2.167 μs (5%) |         |   64 bytes (1%) |           3 |
| `["filter_map_map!", "man"]`             |  70.301 μs (5%) |         |                 |             |
| `["filter_map_map!", "xf"]`              | 744.404 μs (5%) |         |  304 bytes (1%) |          17 |
| `["filter_map_reduce", "man"]`           | 252.001 μs (5%) |         |                 |             |
| `["filter_map_reduce", "xf"]`            | 226.901 μs (5%) |         |                 |             |
| `["findall", "base"]`                    | 819.703 μs (5%) |         |   2.00 MiB (1%) |          21 |
| `["findall", "xf-array"]`                | 859.303 μs (5%) |         |   3.00 MiB (1%) |       98213 |
| `["findall", "xf-iter"]`                 | 906.204 μs (5%) |         |   5.05 MiB (1%) |       99938 |
| `["gemm", "fusedmul", "blas", "16"]`     |   4.567 ms (5%) |         |                 |             |
| `["gemm", "fusedmul", "blas", "2"]`      |   3.445 ms (5%) |         |                 |             |
| `["gemm", "fusedmul", "blas", "32"]`     |   6.311 ms (5%) |         |                 |             |
| `["gemm", "fusedmul", "blas", "8"]`      |   3.699 ms (5%) |         |                 |             |
| `["gemm", "fusedmul", "xf", "16"]`       |   5.268 ms (5%) |         |  160 bytes (1%) |           6 |
| `["gemm", "fusedmul", "xf", "2"]`        | 652.504 μs (5%) |         |  160 bytes (1%) |           6 |
| `["gemm", "fusedmul", "xf", "32"]`       |  10.660 ms (5%) |         |  160 bytes (1%) |           6 |
| `["gemm", "fusedmul", "xf", "8"]`        |   2.745 ms (5%) |         |  160 bytes (1%) |           6 |
| `["gemm", "mul", "linalg", "256"]`       | 886.703 μs (5%) |         |                 |             |
| `["gemm", "mul", "linalg", "32"]`        |   3.000 μs (5%) |         |                 |             |
| `["gemm", "mul", "linalg", "8"]`         | 300.000 ns (5%) |         |                 |             |
| `["gemm", "mul", "man", "false", "256"]` |   1.730 ms (5%) |         |                 |             |
| `["gemm", "mul", "man", "false", "32"]`  |   4.800 μs (5%) |         |                 |             |
| `["gemm", "mul", "man", "false", "8"]`   | 400.000 ns (5%) |         |                 |             |
| `["gemm", "mul", "man", "ivdep", "256"]` |   1.639 ms (5%) |         |                 |             |
| `["gemm", "mul", "man", "ivdep", "32"]`  |   4.300 μs (5%) |         |                 |             |
| `["gemm", "mul", "man", "ivdep", "8"]`   | 400.000 ns (5%) |         |                 |             |
| `["gemm", "mul", "man", "true", "256"]`  |   1.879 ms (5%) |         |                 |             |
| `["gemm", "mul", "man", "true", "32"]`   |   4.900 μs (5%) |         |                 |             |
| `["gemm", "mul", "man", "true", "8"]`    | 500.000 ns (5%) |         |                 |             |
| `["gemm", "mul", "xf", "false", "256"]`  |   1.794 ms (5%) |         |   48 bytes (1%) |           2 |
| `["gemm", "mul", "xf", "false", "32"]`   |   4.800 μs (5%) |         |   48 bytes (1%) |           2 |
| `["gemm", "mul", "xf", "false", "8"]`    | 400.000 ns (5%) |         |   48 bytes (1%) |           2 |
| `["gemm", "mul", "xf", "ivdep", "256"]`  |   1.807 ms (5%) |         |   48 bytes (1%) |           2 |
| `["gemm", "mul", "xf", "ivdep", "32"]`   |   4.100 μs (5%) |         |   48 bytes (1%) |           2 |
| `["gemm", "mul", "xf", "ivdep", "8"]`    | 500.000 ns (5%) |         |   48 bytes (1%) |           2 |
| `["gemm", "mul", "xf", "true", "256"]`   |   1.701 ms (5%) |         |   48 bytes (1%) |           2 |
| `["gemm", "mul", "xf", "true", "32"]`    |   5.100 μs (5%) |         |   48 bytes (1%) |           2 |
| `["gemm", "mul", "xf", "true", "8"]`     | 400.000 ns (5%) |         |   48 bytes (1%) |           2 |
| `["groupby", "sum", "sac"]`              | 245.301 μs (5%) |         | 313.14 KiB (1%) |       10007 |
| `["groupby", "sum", "xf-with-init"]`     | 199.701 μs (5%) |         | 157.44 KiB (1%) |       10008 |
| `["groupby", "sum", "xf-without-init"]`  | 200.101 μs (5%) |         | 157.44 KiB (1%) |       10008 |
| `["mapcat_eduction", "base"]`            |   2.078 μs (5%) |         |                 |             |
| `["mapcat_eduction", "xf-eduction"]`     |   2.130 μs (5%) |         |                 |             |
| `["mapcat_eduction", "xf-xf"]`           |   2.130 μs (5%) |         |                 |             |
| `["missing_argmax", "man"]`              |   2.978 μs (5%) |         |   32 bytes (1%) |           1 |
| `["missing_argmax", "rf"]`               |   2.533 μs (5%) |         |   32 bytes (1%) |           1 |
| `["missing_argmax", "xf"]`               |   2.433 μs (5%) |         |   32 bytes (1%) |           1 |
| `["missing_dot", "equiv"]`               |   1.460 μs (5%) |         |   16 bytes (1%) |           1 |
| `["missing_dot", "man"]`                 |   1.500 μs (5%) |         |   16 bytes (1%) |           1 |
| `["missing_dot", "naive"]`               |   4.614 μs (5%) |         |   16 bytes (1%) |           1 |
| `["missing_dot", "rf"]`                  |   1.500 μs (5%) |         |   16 bytes (1%) |           1 |
| `["missing_dot", "rf_nota"]`             |   1.610 μs (5%) |         |   16 bytes (1%) |           1 |
| `["missing_dot", "xf"]`                  | 205.500 μs (5%) |         |  72.16 KiB (1%) |        3742 |
| `["missing_dot", "xf_nota"]`             | 219.501 μs (5%) |         |  72.20 KiB (1%) |        3746 |
| `["overhead", "foldl"]`                  |   4.800 ns (5%) |         |                 |             |
| `["overhead", "reduce_basecase"]`        | 262.218 ns (5%) |         |  464 bytes (1%) |           9 |
| `["partition_by", "man"]`                |   1.960 ms (5%) |         |  352 bytes (1%) |           4 |
| `["partition_by", "xf"]`                 |   3.295 ms (5%) |         |   6.10 MiB (1%) |      200007 |
| `["set", "base"]`                        |   5.013 ms (5%) |         |  49.58 KiB (1%) |          18 |
| `["set", "xf"]`                          |   4.717 ms (5%) |         |  49.63 KiB (1%) |          21 |

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
       #1  2095 MHz      53494 s          0 s       1446 s      45903 s          0 s
       #2  2095 MHz      42804 s          0 s       1933 s      56490 s          0 s
       
  Memory: 6.764881134033203 GB (2836.12109375 MB free)
  Uptime: 1030.0 sec
  Load Avg:  1.03564453125  1.01220703125  0.75634765625
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
    CPU MHz:             2095.077
    BogoMIPS:            4190.15
    Hypervisor vendor:   Microsoft
    Virtualization type: full
    L1d cache:           32K
    L1i cache:           32K
    L2 cache:            1024K
    L3 cache:            36608K
    NUMA node0 CPU(s):   0,1
    Flags:               fpu vme de pse tsc msr pae mce cx8 apic sep mtrr pge mca cmov pat pse36 clflush mmx fxsr sse sse2 ss ht syscall nx pdpe1gb rdtscp lm constant_tsc rep_good nopl xtopology cpuid pni pclmulqdq ssse3 fma cx16 pcid sse4_1 sse4_2 movbe popcnt aes xsave avx f16c rdrand hypervisor lahf_lm abm 3dnowprefetch invpcid_single pti fsgsbase bmi1 hle avx2 smep bmi2 erms invpcid rtm mpx avx512f avx512dq rdseed adx smap clflushopt avx512cd avx512bw avx512vl xsaveopt xsavec xsaves
    

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

