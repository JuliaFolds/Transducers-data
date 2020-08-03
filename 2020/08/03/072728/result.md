# Benchmark result

* Pull request commit: [`3310cf42fca7d1ecdc930b2eec1e878d12dc300d`](https://github.com/JuliaFolds/Transducers.jl/commit/3310cf42fca7d1ecdc930b2eec1e878d12dc300d)
* Pull request: <https://github.com/JuliaFolds/Transducers.jl/pull/391> (TEST Tweak test/environments/main/Project.toml)

# Judge result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmarks:
    - Target: 3 Aug 2020 - 07:22
    - Baseline: 3 Aug 2020 - 07:26
* Package commits:
    - Target: 69f95a
    - Baseline: 64beaa
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
| `["append!!", "eduction"]`               |                1.07 (5%) :x: |   1.00 (1%)  |
| `["append!!", "xf"]`                     |                1.08 (5%) :x: |   1.00 (1%)  |
| `["cat", "base"]`                        |                1.08 (5%) :x: |   1.00 (1%)  |
| `["collect", "identity-float"]`          | 0.73 (5%) :white_check_mark: |   1.00 (1%)  |
| `["dot", "man"]`                         | 0.86 (5%) :white_check_mark: |   1.00 (1%)  |
| `["filter_map_map!", "man"]`             |                1.13 (5%) :x: |   1.00 (1%)  |
| `["filter_map_map!", "xf"]`              | 0.88 (5%) :white_check_mark: |   1.00 (1%)  |
| `["gemm", "fusedmul", "blas", "16"]`     | 0.85 (5%) :white_check_mark: |   1.00 (1%)  |
| `["gemm", "fusedmul", "blas", "2"]`      | 0.83 (5%) :white_check_mark: |   1.00 (1%)  |
| `["gemm", "fusedmul", "blas", "8"]`      | 0.82 (5%) :white_check_mark: |   1.00 (1%)  |
| `["gemm", "fusedmul", "xf", "16"]`       | 0.92 (5%) :white_check_mark: |   1.00 (1%)  |
| `["gemm", "fusedmul", "xf", "2"]`        |                1.09 (5%) :x: |   1.00 (1%)  |
| `["gemm", "fusedmul", "xf", "32"]`       |                1.08 (5%) :x: |   1.00 (1%)  |
| `["gemm", "fusedmul", "xf", "8"]`        | 0.90 (5%) :white_check_mark: |   1.00 (1%)  |
| `["gemm", "mul", "linalg", "32"]`        |                1.16 (5%) :x: |   1.00 (1%)  |
| `["gemm", "mul", "linalg", "8"]`         | 0.68 (5%) :white_check_mark: |   1.00 (1%)  |
| `["gemm", "mul", "man", "false", "256"]` | 0.93 (5%) :white_check_mark: |   1.00 (1%)  |
| `["gemm", "mul", "man", "false", "32"]`  |                1.07 (5%) :x: |   1.00 (1%)  |
| `["gemm", "mul", "man", "ivdep", "256"]` | 0.95 (5%) :white_check_mark: |   1.00 (1%)  |
| `["gemm", "mul", "man", "ivdep", "32"]`  | 0.88 (5%) :white_check_mark: |   1.00 (1%)  |
| `["gemm", "mul", "man", "ivdep", "8"]`   |                1.06 (5%) :x: |   1.00 (1%)  |
| `["gemm", "mul", "man", "true", "256"]`  | 0.92 (5%) :white_check_mark: |   1.00 (1%)  |
| `["gemm", "mul", "man", "true", "32"]`   | 0.80 (5%) :white_check_mark: |   1.00 (1%)  |
| `["gemm", "mul", "man", "true", "8"]`    | 0.66 (5%) :white_check_mark: |   1.00 (1%)  |
| `["gemm", "mul", "xf", "false", "256"]`  | 0.93 (5%) :white_check_mark: |   1.00 (1%)  |
| `["gemm", "mul", "xf", "false", "32"]`   |                1.10 (5%) :x: |   1.00 (1%)  |
| `["gemm", "mul", "xf", "false", "8"]`    | 0.93 (5%) :white_check_mark: |   1.00 (1%)  |
| `["gemm", "mul", "xf", "true", "256"]`   | 0.93 (5%) :white_check_mark: |   1.00 (1%)  |
| `["gemm", "mul", "xf", "true", "32"]`    | 0.92 (5%) :white_check_mark: |   1.00 (1%)  |
| `["gemm", "mul", "xf", "true", "8"]`     |                1.18 (5%) :x: |   1.00 (1%)  |
| `["groupby", "sum", "xf-with-init"]`     | 0.82 (5%) :white_check_mark: |   1.00 (1%)  |
| `["missing_argmax", "rf"]`               | 0.86 (5%) :white_check_mark: |   1.00 (1%)  |
| `["missing_argmax", "xf"]`               | 0.82 (5%) :white_check_mark: |   1.00 (1%)  |
| `["missing_dot", "xf"]`                  |                1.07 (5%) :x: |   1.00 (1%)  |
| `["set", "base"]`                        | 0.85 (5%) :white_check_mark: |   1.00 (1%)  |
| `["set", "xf"]`                          | 0.79 (5%) :white_check_mark: |   1.00 (1%)  |

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
  CPU: Intel(R) Xeon(R) Platinum 8171M CPU @ 2.60GHz: 
              speed         user         nice          sys         idle          irq
       #1  2095 MHz      15414 s          0 s       1111 s      51421 s          0 s
       #2  2095 MHz      48816 s          0 s       1904 s      17254 s          0 s
       
  Memory: 6.7648773193359375 GB (2733.9375 MB free)
  Uptime: 698.0 sec
  Load Avg:  1.0595703125  1.0  0.630859375
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
  CPU: Intel(R) Xeon(R) Platinum 8171M CPU @ 2.60GHz: 
              speed         user         nice          sys         idle          irq
       #1  2095 MHz      26231 s          0 s       1201 s      66959 s          0 s
       #2  2095 MHz      64287 s          0 s       2039 s      28042 s          0 s
       
  Memory: 6.7648773193359375 GB (2724.19140625 MB free)
  Uptime: 964.0 sec
  Load Avg:  1.13037109375  1.03125  0.74853515625
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-8.0.1 (ORCJIT, skylake)
```

---
# Target result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmark: 3 Aug 2020 - 7:22
* Package commit: 69f95a
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
| `["append!!", "xf"]`                     |  16.100 μs (5%) |         |  64.72 KiB (1%) |          18 |
| `["cat", "base"]`                        |   1.560 μs (5%) |         |                 |             |
| `["cat", "xf"]`                          |   1.650 μs (5%) |         |                 |             |
| `["collect", "filter-missing"]`          |  89.801 μs (5%) |         | 345.31 KiB (1%) |       10015 |
| `["collect", "identity-float"]`          |  63.800 μs (5%) |         | 569.16 KiB (1%) |       10015 |
| `["collect", "identity-union"]`          | 258.203 μs (5%) |         | 705.03 KiB (1%) |       16659 |
| `["dict", "base"]`                       |   3.411 ms (5%) |         |  92.91 KiB (1%) |          22 |
| `["dict", "xf"]`                         |   3.527 ms (5%) |         |  92.36 KiB (1%) |          21 |
| `["dot", "blas"]`                        |   1.000 μs (5%) |         |                 |             |
| `["dot", "man"]`                         |   1.010 μs (5%) |         |                 |             |
| `["dot", "rf"]`                          |   1.790 μs (5%) |         |                 |             |
| `["dot", "xf"]`                          |   1.860 μs (5%) |         |   64 bytes (1%) |           3 |
| `["filter_map_map!", "man"]`             |  73.301 μs (5%) |         |                 |             |
| `["filter_map_map!", "xf"]`              | 588.804 μs (5%) |         |  304 bytes (1%) |          17 |
| `["filter_map_reduce", "man"]`           | 191.801 μs (5%) |         |                 |             |
| `["filter_map_reduce", "xf"]`            | 191.801 μs (5%) |         |                 |             |
| `["findall", "base"]`                    | 692.207 μs (5%) |         |   2.00 MiB (1%) |          21 |
| `["findall", "xf-array"]`                | 650.707 μs (5%) |         |   3.05 MiB (1%) |      100012 |
| `["findall", "xf-iter"]`                 |   2.674 ms (5%) |         |   9.63 MiB (1%) |      299922 |
| `["gemm", "fusedmul", "blas", "16"]`     |   3.786 ms (5%) |         |                 |             |
| `["gemm", "fusedmul", "blas", "2"]`      |   2.924 ms (5%) |         |                 |             |
| `["gemm", "fusedmul", "blas", "32"]`     |   5.226 ms (5%) |         |                 |             |
| `["gemm", "fusedmul", "blas", "8"]`      |   2.795 ms (5%) |         |                 |             |
| `["gemm", "fusedmul", "xf", "16"]`       |   4.146 ms (5%) |         |  160 bytes (1%) |           6 |
| `["gemm", "fusedmul", "xf", "2"]`        | 521.103 μs (5%) |         |  160 bytes (1%) |           6 |
| `["gemm", "fusedmul", "xf", "32"]`       |   8.189 ms (5%) |         |  160 bytes (1%) |           6 |
| `["gemm", "fusedmul", "xf", "8"]`        |   1.800 ms (5%) |         |  160 bytes (1%) |           6 |
| `["gemm", "mul", "linalg", "256"]`       | 749.206 μs (5%) |         |                 |             |
| `["gemm", "mul", "linalg", "32"]`        |   2.911 μs (5%) |         |                 |             |
| `["gemm", "mul", "linalg", "8"]`         | 204.037 ns (5%) |         |                 |             |
| `["gemm", "mul", "man", "false", "256"]` |   1.323 ms (5%) |         |                 |             |
| `["gemm", "mul", "man", "false", "32"]`  |   3.962 μs (5%) |         |                 |             |
| `["gemm", "mul", "man", "false", "8"]`   | 403.241 ns (5%) |         |                 |             |
| `["gemm", "mul", "man", "ivdep", "256"]` |   1.347 ms (5%) |         |                 |             |
| `["gemm", "mul", "man", "ivdep", "32"]`  |   3.250 μs (5%) |         |                 |             |
| `["gemm", "mul", "man", "ivdep", "8"]`   | 316.949 ns (5%) |         |                 |             |
| `["gemm", "mul", "man", "true", "256"]`  |   1.331 ms (5%) |         |                 |             |
| `["gemm", "mul", "man", "true", "32"]`   |   3.938 μs (5%) |         |                 |             |
| `["gemm", "mul", "man", "true", "8"]`    | 332.020 ns (5%) |         |                 |             |
| `["gemm", "mul", "xf", "false", "256"]`  |   1.324 ms (5%) |         |   48 bytes (1%) |           2 |
| `["gemm", "mul", "xf", "false", "32"]`   |   4.057 μs (5%) |         |   48 bytes (1%) |           2 |
| `["gemm", "mul", "xf", "false", "8"]`    | 372.816 ns (5%) |         |   48 bytes (1%) |           2 |
| `["gemm", "mul", "xf", "ivdep", "256"]`  |   1.363 ms (5%) |         |   48 bytes (1%) |           2 |
| `["gemm", "mul", "xf", "ivdep", "32"]`   |   3.138 μs (5%) |         |   48 bytes (1%) |           2 |
| `["gemm", "mul", "xf", "ivdep", "8"]`    | 299.611 ns (5%) |         |   48 bytes (1%) |           2 |
| `["gemm", "mul", "xf", "true", "256"]`   |   1.319 ms (5%) |         |   48 bytes (1%) |           2 |
| `["gemm", "mul", "xf", "true", "32"]`    |   4.029 μs (5%) |         |   48 bytes (1%) |           2 |
| `["gemm", "mul", "xf", "true", "8"]`     | 354.976 ns (5%) |         |   48 bytes (1%) |           2 |
| `["groupby", "sum", "sac"]`              | 205.401 μs (5%) |         | 313.14 KiB (1%) |       10007 |
| `["groupby", "sum", "xf-with-init"]`     | 150.000 μs (5%) |         | 157.44 KiB (1%) |       10008 |
| `["groupby", "sum", "xf-without-init"]`  | 149.000 μs (5%) |         | 157.44 KiB (1%) |       10008 |
| `["mapcat_eduction", "base"]`            |   1.550 μs (5%) |         |                 |             |
| `["mapcat_eduction", "xf-eduction"]`     |   1.590 μs (5%) |         |                 |             |
| `["mapcat_eduction", "xf-xf"]`           |   1.590 μs (5%) |         |                 |             |
| `["missing_argmax", "man"]`              |   2.233 μs (5%) |         |   32 bytes (1%) |           1 |
| `["missing_argmax", "rf"]`               |   2.111 μs (5%) |         |   32 bytes (1%) |           1 |
| `["missing_argmax", "xf"]`               |   2.078 μs (5%) |         |   32 bytes (1%) |           1 |
| `["missing_dot", "equiv"]`               |   1.200 μs (5%) |         |   16 bytes (1%) |           1 |
| `["missing_dot", "man"]`                 |   1.130 μs (5%) |         |   16 bytes (1%) |           1 |
| `["missing_dot", "naive"]`               |   3.938 μs (5%) |         |   16 bytes (1%) |           1 |
| `["missing_dot", "rf"]`                  |   1.130 μs (5%) |         |   16 bytes (1%) |           1 |
| `["missing_dot", "rf_nota"]`             |   1.210 μs (5%) |         |   16 bytes (1%) |           1 |
| `["missing_dot", "xf"]`                  | 175.801 μs (5%) |         |  72.00 KiB (1%) |        3738 |
| `["missing_dot", "xf_nota"]`             | 172.202 μs (5%) |         |  72.13 KiB (1%) |        3742 |
| `["overhead", "foldl"]`                  |   4.400 ns (5%) |         |                 |             |
| `["overhead", "reduce_basecase"]`        | 218.907 ns (5%) |         |  464 bytes (1%) |           9 |
| `["partition_by", "man"]`                |   1.655 ms (5%) |         |  352 bytes (1%) |           4 |
| `["partition_by", "xf"]`                 |   2.492 ms (5%) |         |   6.10 MiB (1%) |      200007 |
| `["set", "base"]`                        |   3.993 ms (5%) |         |  49.58 KiB (1%) |          18 |
| `["set", "xf"]`                          |   3.743 ms (5%) |         |  49.63 KiB (1%) |          21 |

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
  CPU: Intel(R) Xeon(R) Platinum 8171M CPU @ 2.60GHz: 
              speed         user         nice          sys         idle          irq
       #1  2095 MHz      15414 s          0 s       1111 s      51421 s          0 s
       #2  2095 MHz      48816 s          0 s       1904 s      17254 s          0 s
       
  Memory: 6.7648773193359375 GB (2733.9375 MB free)
  Uptime: 698.0 sec
  Load Avg:  1.0595703125  1.0  0.630859375
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-8.0.1 (ORCJIT, skylake)
```

---
# Baseline result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmark: 3 Aug 2020 - 7:26
* Package commit: 64beaa
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
| `["append!!", "eduction"]`               |  14.900 μs (5%) |         |  64.72 KiB (1%) |          18 |
| `["append!!", "xf"]`                     |  14.900 μs (5%) |         |  64.72 KiB (1%) |          18 |
| `["cat", "base"]`                        |   1.440 μs (5%) |         |                 |             |
| `["cat", "xf"]`                          |   1.650 μs (5%) |         |                 |             |
| `["collect", "filter-missing"]`          |  88.300 μs (5%) |         | 345.31 KiB (1%) |       10015 |
| `["collect", "identity-float"]`          |  87.001 μs (5%) |         | 569.16 KiB (1%) |       10015 |
| `["collect", "identity-union"]`          | 252.401 μs (5%) |         | 705.38 KiB (1%) |       16679 |
| `["dict", "base"]`                       |   3.386 ms (5%) |         |  92.91 KiB (1%) |          22 |
| `["dict", "xf"]`                         |   3.481 ms (5%) |         |  92.36 KiB (1%) |          21 |
| `["dot", "blas"]`                        |   1.030 μs (5%) |         |                 |             |
| `["dot", "man"]`                         |   1.170 μs (5%) |         |                 |             |
| `["dot", "rf"]`                          |   1.790 μs (5%) |         |                 |             |
| `["dot", "xf"]`                          |   1.840 μs (5%) |         |   64 bytes (1%) |           3 |
| `["filter_map_map!", "man"]`             |  64.601 μs (5%) |         |                 |             |
| `["filter_map_map!", "xf"]`              | 670.702 μs (5%) |         |  304 bytes (1%) |          17 |
| `["filter_map_reduce", "man"]`           | 191.801 μs (5%) |         |                 |             |
| `["filter_map_reduce", "xf"]`            | 191.800 μs (5%) |         |                 |             |
| `["findall", "base"]`                    | 677.103 μs (5%) |         |   2.00 MiB (1%) |          21 |
| `["findall", "xf-array"]`                | 651.303 μs (5%) |         |   3.06 MiB (1%) |      100082 |
| `["findall", "xf-iter"]`                 |   2.722 ms (5%) |         |   9.63 MiB (1%) |      299928 |
| `["gemm", "fusedmul", "blas", "16"]`     |   4.461 ms (5%) |         |                 |             |
| `["gemm", "fusedmul", "blas", "2"]`      |   3.523 ms (5%) |         |                 |             |
| `["gemm", "fusedmul", "blas", "32"]`     |   5.307 ms (5%) |         |                 |             |
| `["gemm", "fusedmul", "blas", "8"]`      |   3.427 ms (5%) |         |                 |             |
| `["gemm", "fusedmul", "xf", "16"]`       |   4.489 ms (5%) |         |  160 bytes (1%) |           6 |
| `["gemm", "fusedmul", "xf", "2"]`        | 477.902 μs (5%) |         |  160 bytes (1%) |           6 |
| `["gemm", "fusedmul", "xf", "32"]`       |   7.589 ms (5%) |         |  160 bytes (1%) |           6 |
| `["gemm", "fusedmul", "xf", "8"]`        |   1.995 ms (5%) |         |  160 bytes (1%) |           6 |
| `["gemm", "mul", "linalg", "256"]`       | 757.404 μs (5%) |         |                 |             |
| `["gemm", "mul", "linalg", "32"]`        |   2.500 μs (5%) |         |                 |             |
| `["gemm", "mul", "linalg", "8"]`         | 300.000 ns (5%) |         |                 |             |
| `["gemm", "mul", "man", "false", "256"]` |   1.427 ms (5%) |         |                 |             |
| `["gemm", "mul", "man", "false", "32"]`  |   3.700 μs (5%) |         |                 |             |
| `["gemm", "mul", "man", "false", "8"]`   | 400.000 ns (5%) |         |                 |             |
| `["gemm", "mul", "man", "ivdep", "256"]` |   1.423 ms (5%) |         |                 |             |
| `["gemm", "mul", "man", "ivdep", "32"]`  |   3.700 μs (5%) |         |                 |             |
| `["gemm", "mul", "man", "ivdep", "8"]`   | 300.000 ns (5%) |         |                 |             |
| `["gemm", "mul", "man", "true", "256"]`  |   1.443 ms (5%) |         |                 |             |
| `["gemm", "mul", "man", "true", "32"]`   |   4.900 μs (5%) |         |                 |             |
| `["gemm", "mul", "man", "true", "8"]`    | 500.000 ns (5%) |         |                 |             |
| `["gemm", "mul", "xf", "false", "256"]`  |   1.430 ms (5%) |         |   48 bytes (1%) |           2 |
| `["gemm", "mul", "xf", "false", "32"]`   |   3.700 μs (5%) |         |   48 bytes (1%) |           2 |
| `["gemm", "mul", "xf", "false", "8"]`    | 400.000 ns (5%) |         |   48 bytes (1%) |           2 |
| `["gemm", "mul", "xf", "ivdep", "256"]`  |   1.417 ms (5%) |         |   48 bytes (1%) |           2 |
| `["gemm", "mul", "xf", "ivdep", "32"]`   |   3.100 μs (5%) |         |   48 bytes (1%) |           2 |
| `["gemm", "mul", "xf", "ivdep", "8"]`    | 300.000 ns (5%) |         |   48 bytes (1%) |           2 |
| `["gemm", "mul", "xf", "true", "256"]`   |   1.426 ms (5%) |         |   48 bytes (1%) |           2 |
| `["gemm", "mul", "xf", "true", "32"]`    |   4.400 μs (5%) |         |   48 bytes (1%) |           2 |
| `["gemm", "mul", "xf", "true", "8"]`     | 300.000 ns (5%) |         |   48 bytes (1%) |           2 |
| `["groupby", "sum", "sac"]`              | 214.101 μs (5%) |         | 313.14 KiB (1%) |       10007 |
| `["groupby", "sum", "xf-with-init"]`     | 182.101 μs (5%) |         | 157.44 KiB (1%) |       10008 |
| `["groupby", "sum", "xf-without-init"]`  | 156.600 μs (5%) |         | 157.44 KiB (1%) |       10008 |
| `["mapcat_eduction", "base"]`            |   1.550 μs (5%) |         |                 |             |
| `["mapcat_eduction", "xf-eduction"]`     |   1.600 μs (5%) |         |                 |             |
| `["mapcat_eduction", "xf-xf"]`           |   1.600 μs (5%) |         |                 |             |
| `["missing_argmax", "man"]`              |   2.233 μs (5%) |         |   32 bytes (1%) |           1 |
| `["missing_argmax", "rf"]`               |   2.445 μs (5%) |         |   32 bytes (1%) |           1 |
| `["missing_argmax", "xf"]`               |   2.544 μs (5%) |         |   32 bytes (1%) |           1 |
| `["missing_dot", "equiv"]`               |   1.200 μs (5%) |         |   16 bytes (1%) |           1 |
| `["missing_dot", "man"]`                 |   1.120 μs (5%) |         |   16 bytes (1%) |           1 |
| `["missing_dot", "naive"]`               |   3.925 μs (5%) |         |   16 bytes (1%) |           1 |
| `["missing_dot", "rf"]`                  |   1.130 μs (5%) |         |   16 bytes (1%) |           1 |
| `["missing_dot", "rf_nota"]`             |   1.210 μs (5%) |         |   16 bytes (1%) |           1 |
| `["missing_dot", "xf"]`                  | 163.901 μs (5%) |         |  72.23 KiB (1%) |        3748 |
| `["missing_dot", "xf_nota"]`             | 165.501 μs (5%) |         |  72.08 KiB (1%) |        3738 |
| `["overhead", "foldl"]`                  |   4.200 ns (5%) |         |                 |             |
| `["overhead", "reduce_basecase"]`        | 218.091 ns (5%) |         |  464 bytes (1%) |           9 |
| `["partition_by", "man"]`                |   1.645 ms (5%) |         |  352 bytes (1%) |           4 |
| `["partition_by", "xf"]`                 |   2.483 ms (5%) |         |   6.10 MiB (1%) |      200007 |
| `["set", "base"]`                        |   4.693 ms (5%) |         |  49.58 KiB (1%) |          18 |
| `["set", "xf"]`                          |   4.708 ms (5%) |         |  49.63 KiB (1%) |          21 |

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
  CPU: Intel(R) Xeon(R) Platinum 8171M CPU @ 2.60GHz: 
              speed         user         nice          sys         idle          irq
       #1  2095 MHz      26231 s          0 s       1201 s      66959 s          0 s
       #2  2095 MHz      64287 s          0 s       2039 s      28042 s          0 s
       
  Memory: 6.7648773193359375 GB (2724.19140625 MB free)
  Uptime: 964.0 sec
  Load Avg:  1.13037109375  1.03125  0.74853515625
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
    CPU MHz:             2095.082
    BogoMIPS:            4190.16
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

