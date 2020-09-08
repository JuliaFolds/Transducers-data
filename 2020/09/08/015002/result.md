# Multi-thread benchmark result

* Pull request commit: [`97b8458b15e7c4218f5977930d86e5ebdb2ab129`](https://github.com/JuliaFolds/Transducers.jl/commit/97b8458b15e7c4218f5977930d86e5ebdb2ab129)
* Pull request: <https://github.com/JuliaFolds/Transducers.jl/pull/425> (Undo JULIA_PKG_SERVER hack)

# Judge result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmarks:
    - Target: 8 Sep 2020 - 01:44
    - Baseline: 8 Sep 2020 - 01:49
* Package commits:
    - Target: bf3984
    - Baseline: 7e0cc7
* Julia commits:
    - Target: 697e78
    - Baseline: 697e78
* Julia command flags:
    - Target: None
    - Baseline: None
* Environment variables:
    - Target: `JULIA_NUM_THREADS => 2`
    - Baseline: `JULIA_NUM_THREADS => 2`

## Results
A ratio greater than `1.0` denotes a possible regression (marked with :x:), while a ratio less
than `1.0` denotes a possible improvement (marked with :white_check_mark:). Only significant results - results
that indicate possible regressions or improvements - are shown below (thus, an empty table means that all
benchmark results remained invariant between builds).

| ID                                                  | time ratio                   | memory ratio                 |
|-----------------------------------------------------|------------------------------|------------------------------|
| `["collect", "unordered", "basesize=1"]`            | 0.84 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["collect", "unordered", "basesize=1024"]`         |                   0.97 (5%)  |                1.02 (1%) :x: |
| `["collect", "unordered", "basesize=32"]`           | 0.83 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["findfirst", "n=1000", "reduce", "basesize=256"]` | 0.91 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["findfirst", "n=400", "reduce", "basesize=256"]`  | 0.95 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["findfirst", "n=500", "reduce", "basesize=256"]`  |                1.06 (5%) :x: |                   1.00 (1%)  |
| `["overhead", "stoppable=true"]`                    |                1.09 (5%) :x: |                   1.00 (1%)  |
| `["parallel_histogram", "assoc", "basesize=4096"]`  |                   0.99 (5%)  | 0.87 (1%) :white_check_mark: |
| `["parallel_histogram", "comm", "basesize=16384"]`  |                1.12 (5%) :x: |                   1.00 (1%)  |
| `["parallel_histogram", "comm", "basesize=4096"]`   |                1.10 (5%) :x: |                   1.00 (1%)  |
| `["parallel_histogram", "comm", "basesize=8192"]`   |                1.13 (5%) :x: |                   1.00 (1%)  |
| `["sum", "random", "reduce", "basesize=512"]`       |                1.17 (5%) :x: |                   1.00 (1%)  |
| `["words", "nthreads=1"]`                           |                1.19 (5%) :x: |                   1.00 (1%)  |
| `["words", "nthreads=2"]`                           |                1.10 (5%) :x: |                   1.00 (1%)  |
| `["words", "nthreads=4"]`                           |                1.06 (5%) :x: |                   1.01 (1%)  |

## Benchmark Group List
Here's a list of all the benchmark groups executed by this job:

- `["collect", "assoc"]`
- `["collect"]`
- `["collect", "unordered"]`
- `["findfirst", "n=1000"]`
- `["findfirst", "n=1000", "reduce"]`
- `["findfirst", "n=400"]`
- `["findfirst", "n=400", "reduce"]`
- `["findfirst", "n=500"]`
- `["findfirst", "n=500", "reduce"]`
- `["overhead"]`
- `["parallel_histogram", "assoc"]`
- `["parallel_histogram", "comm"]`
- `["parallel_histogram"]`
- `["sum", "random"]`
- `["sum", "random", "reduce"]`
- `["sum", "uniform"]`
- `["sum", "uniform", "reduce"]`
- `["sum", "valley"]`
- `["sum", "valley", "reduce"]`
- `["words"]`

## Julia versioninfo

### Target
```
Julia Version 1.5.1
Commit 697e782ab8 (2020-08-25 20:08 UTC)
Platform Info:
  OS: Linux (x86_64-pc-linux-gnu)
      Ubuntu 18.04.5 LTS
  uname: Linux 5.4.0-1023-azure #23~18.04.1-Ubuntu SMP Thu Aug 20 14:46:48 UTC 2020 x86_64 x86_64
  CPU: Intel(R) Xeon(R) CPU E5-2673 v4 @ 2.30GHz: 
              speed         user         nice          sys         idle          irq
       #1  2294 MHz      53745 s          0 s       2560 s      15227 s          0 s
       #2  2294 MHz      43950 s          0 s       2611 s      25486 s          0 s
       
  Memory: 6.764892578125 GB (3070.93359375 MB free)
  Uptime: 738.0 sec
  Load Avg:  1.73486328125  1.521484375  0.90478515625
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-9.0.1 (ORCJIT, broadwell)
```

### Baseline
```
Julia Version 1.5.1
Commit 697e782ab8 (2020-08-25 20:08 UTC)
Platform Info:
  OS: Linux (x86_64-pc-linux-gnu)
      Ubuntu 18.04.5 LTS
  uname: Linux 5.4.0-1023-azure #23~18.04.1-Ubuntu SMP Thu Aug 20 14:46:48 UTC 2020 x86_64 x86_64
  CPU: Intel(R) Xeon(R) CPU E5-2673 v4 @ 2.30GHz: 
              speed         user         nice          sys         idle          irq
       #1  2294 MHz      74979 s          0 s       3195 s      21296 s          0 s
       #2  2294 MHz      66089 s          0 s       3240 s      30564 s          0 s
       
  Memory: 6.764892578125 GB (3058.61328125 MB free)
  Uptime: 1019.0 sec
  Load Avg:  1.6474609375  1.59814453125  1.1025390625
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-9.0.1 (ORCJIT, broadwell)
```

---
# Target result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmark: 8 Sep 2020 - 1:44
* Package commit: bf3984
* Julia commit: 697e78
* Julia command flags: None
* Environment variables: `JULIA_NUM_THREADS => 2`

## Results
Below is a table of this job's results, obtained by running the benchmarks.
The values listed in the `ID` column have the structure `[parent_group, child_group, ..., key]`, and can be used to
index into the BaseBenchmarks suite to retrieve the corresponding benchmarks.
The percentages accompanying time and memory values in the below table are noise tolerances. The "true"
time/memory value for a given benchmark is expected to fall within this percentage of the reported value.
An empty cell means that the value was zero.

| ID                                                  | time            | GC time   | memory           | allocations |
|-----------------------------------------------------|----------------:|----------:|-----------------:|------------:|
| `["collect", "assoc", "basesize=1"]`                | 272.959 ms (5%) | 11.152 ms |   82.16 MiB (1%) |     1368080 |
| `["collect", "assoc", "basesize=1024"]`             | 151.770 ms (5%) |           |    1.83 MiB (1%) |        1597 |
| `["collect", "assoc", "basesize=32"]`               | 156.167 ms (5%) |           |    5.47 MiB (1%) |       47070 |
| `["collect", "seq"]`                                | 305.160 ms (5%) |           |  512.72 KiB (1%) |          15 |
| `["collect", "unordered", "basesize=1"]`            | 380.643 ms (5%) |           |   30.01 MiB (1%) |      360594 |
| `["collect", "unordered", "basesize=1024"]`         | 233.488 ms (5%) |           |  865.14 KiB (1%) |        4424 |
| `["collect", "unordered", "basesize=32"]`           | 180.373 ms (5%) |           |    1.48 MiB (1%) |       12784 |
| `["findfirst", "n=1000", "foldl"]`                  | 485.601 ms (5%) |           |                  |             |
| `["findfirst", "n=1000", "reduce", "basesize=128"]` | 263.730 ms (5%) |           |  546.34 KiB (1%) |        9562 |
| `["findfirst", "n=1000", "reduce", "basesize=256"]` | 257.208 ms (5%) |           |  278.25 KiB (1%) |        4888 |
| `["findfirst", "n=1000", "reduce", "basesize=512"]` | 262.546 ms (5%) |           |  144.66 KiB (1%) |        2550 |
| `["findfirst", "n=400", "foldl"]`                   | 373.431 ms (5%) |           |                  |             |
| `["findfirst", "n=400", "reduce", "basesize=128"]`  | 189.120 ms (5%) |           | 1012.86 KiB (1%) |       17725 |
| `["findfirst", "n=400", "reduce", "basesize=256"]`  | 191.920 ms (5%) |           |  509.63 KiB (1%) |        8952 |
| `["findfirst", "n=400", "reduce", "basesize=512"]`  | 189.657 ms (5%) |           |  258.83 KiB (1%) |        4563 |
| `["findfirst", "n=500", "foldl"]`                   |  61.896 ms (5%) |           |                  |             |
| `["findfirst", "n=500", "reduce", "basesize=128"]`  |  32.956 ms (5%) |           |  152.59 KiB (1%) |        2677 |
| `["findfirst", "n=500", "reduce", "basesize=256"]`  |  33.368 ms (5%) |           |   82.00 KiB (1%) |        1444 |
| `["findfirst", "n=500", "reduce", "basesize=512"]`  |  33.872 ms (5%) |           |   46.83 KiB (1%) |         827 |
| `["overhead", "default"]`                           | 144.900 μs (5%) |           |  140.75 KiB (1%) |        2465 |
| `["overhead", "stoppable=false"]`                   | 139.900 μs (5%) |           |  140.78 KiB (1%) |        2465 |
| `["overhead", "stoppable=true"]`                    | 281.001 μs (5%) |           |  140.78 KiB (1%) |        2465 |
| `["parallel_histogram", "assoc", "basesize=16384"]` |   3.353 ms (5%) |           |  731.81 KiB (1%) |          94 |
| `["parallel_histogram", "assoc", "basesize=4096"]`  |   3.988 ms (5%) |           |    1.80 MiB (1%) |         448 |
| `["parallel_histogram", "assoc", "basesize=8192"]`  |   3.648 ms (5%) |           |    1.43 MiB (1%) |         220 |
| `["parallel_histogram", "comm", "basesize=16384"]`  |  12.046 ms (5%) |           | 1009.77 KiB (1%) |         172 |
| `["parallel_histogram", "comm", "basesize=4096"]`   |  17.678 ms (5%) |           |    1.03 MiB (1%) |        1437 |
| `["parallel_histogram", "comm", "basesize=8192"]`   |  16.468 ms (5%) |           |    1.24 MiB (1%) |         860 |
| `["parallel_histogram", "seq"]`                     |   6.169 ms (5%) |           |  364.61 KiB (1%) |          24 |
| `["sum", "random", "foldl"]`                        |  11.622 ms (5%) |           |    32 bytes (1%) |           2 |
| `["sum", "random", "reduce", "basesize=128"]`       |   6.059 ms (5%) |           |  292.02 KiB (1%) |        5213 |
| `["sum", "random", "reduce", "basesize=256"]`       |   5.968 ms (5%) |           |  144.53 KiB (1%) |        2589 |
| `["sum", "random", "reduce", "basesize=512"]`       |   6.866 ms (5%) |           |   71.11 KiB (1%) |        1279 |
| `["sum", "uniform", "foldl"]`                       |  10.988 ms (5%) |           |    32 bytes (1%) |           2 |
| `["sum", "uniform", "reduce", "basesize=128"]`      |   5.920 ms (5%) |           |  292.02 KiB (1%) |        5213 |
| `["sum", "uniform", "reduce", "basesize=256"]`      |   5.703 ms (5%) |           |  144.53 KiB (1%) |        2589 |
| `["sum", "uniform", "reduce", "basesize=512"]`      |   5.607 ms (5%) |           |   71.06 KiB (1%) |        1278 |
| `["sum", "valley", "foldl"]`                        |  11.332 ms (5%) |           |    32 bytes (1%) |           2 |
| `["sum", "valley", "reduce", "basesize=128"]`       |   6.145 ms (5%) |           |  292.02 KiB (1%) |        5213 |
| `["sum", "valley", "reduce", "basesize=256"]`       |   6.071 ms (5%) |           |  144.53 KiB (1%) |        2589 |
| `["sum", "valley", "reduce", "basesize=512"]`       |   5.875 ms (5%) |           |   71.06 KiB (1%) |        1278 |
| `["words", "nthreads=1"]`                           |  24.140 ms (5%) |           |   31.74 MiB (1%) |     1034097 |
| `["words", "nthreads=2"]`                           |  15.251 ms (5%) |           |   32.45 MiB (1%) |     1034239 |
| `["words", "nthreads=4"]`                           |  14.831 ms (5%) |           |   33.09 MiB (1%) |     1034559 |

## Benchmark Group List
Here's a list of all the benchmark groups executed by this job:

- `["collect", "assoc"]`
- `["collect"]`
- `["collect", "unordered"]`
- `["findfirst", "n=1000"]`
- `["findfirst", "n=1000", "reduce"]`
- `["findfirst", "n=400"]`
- `["findfirst", "n=400", "reduce"]`
- `["findfirst", "n=500"]`
- `["findfirst", "n=500", "reduce"]`
- `["overhead"]`
- `["parallel_histogram", "assoc"]`
- `["parallel_histogram", "comm"]`
- `["parallel_histogram"]`
- `["sum", "random"]`
- `["sum", "random", "reduce"]`
- `["sum", "uniform"]`
- `["sum", "uniform", "reduce"]`
- `["sum", "valley"]`
- `["sum", "valley", "reduce"]`
- `["words"]`

## Julia versioninfo
```
Julia Version 1.5.1
Commit 697e782ab8 (2020-08-25 20:08 UTC)
Platform Info:
  OS: Linux (x86_64-pc-linux-gnu)
      Ubuntu 18.04.5 LTS
  uname: Linux 5.4.0-1023-azure #23~18.04.1-Ubuntu SMP Thu Aug 20 14:46:48 UTC 2020 x86_64 x86_64
  CPU: Intel(R) Xeon(R) CPU E5-2673 v4 @ 2.30GHz: 
              speed         user         nice          sys         idle          irq
       #1  2294 MHz      53745 s          0 s       2560 s      15227 s          0 s
       #2  2294 MHz      43950 s          0 s       2611 s      25486 s          0 s
       
  Memory: 6.764892578125 GB (3070.93359375 MB free)
  Uptime: 738.0 sec
  Load Avg:  1.73486328125  1.521484375  0.90478515625
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-9.0.1 (ORCJIT, broadwell)
```

---
# Baseline result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmark: 8 Sep 2020 - 1:49
* Package commit: 7e0cc7
* Julia commit: 697e78
* Julia command flags: None
* Environment variables: `JULIA_NUM_THREADS => 2`

## Results
Below is a table of this job's results, obtained by running the benchmarks.
The values listed in the `ID` column have the structure `[parent_group, child_group, ..., key]`, and can be used to
index into the BaseBenchmarks suite to retrieve the corresponding benchmarks.
The percentages accompanying time and memory values in the below table are noise tolerances. The "true"
time/memory value for a given benchmark is expected to fall within this percentage of the reported value.
An empty cell means that the value was zero.

| ID                                                  | time            | GC time  | memory           | allocations |
|-----------------------------------------------------|----------------:|---------:|-----------------:|------------:|
| `["collect", "assoc", "basesize=1"]`                | 261.351 ms (5%) | 9.986 ms |   82.16 MiB (1%) |     1368070 |
| `["collect", "assoc", "basesize=1024"]`             | 154.228 ms (5%) |          |    1.83 MiB (1%) |        1596 |
| `["collect", "assoc", "basesize=32"]`               | 154.414 ms (5%) |          |    5.47 MiB (1%) |       47069 |
| `["collect", "seq"]`                                | 297.495 ms (5%) |          |  512.72 KiB (1%) |          15 |
| `["collect", "unordered", "basesize=1"]`            | 452.111 ms (5%) |          |   30.01 MiB (1%) |      360718 |
| `["collect", "unordered", "basesize=1024"]`         | 239.967 ms (5%) |          |  850.48 KiB (1%) |        3955 |
| `["collect", "unordered", "basesize=32"]`           | 216.628 ms (5%) |          |    1.48 MiB (1%) |       12736 |
| `["findfirst", "n=1000", "foldl"]`                  | 501.849 ms (5%) |          |                  |             |
| `["findfirst", "n=1000", "reduce", "basesize=128"]` | 257.128 ms (5%) |          |  546.33 KiB (1%) |        9561 |
| `["findfirst", "n=1000", "reduce", "basesize=256"]` | 282.756 ms (5%) |          |  278.25 KiB (1%) |        4888 |
| `["findfirst", "n=1000", "reduce", "basesize=512"]` | 274.878 ms (5%) |          |  144.66 KiB (1%) |        2550 |
| `["findfirst", "n=400", "foldl"]`                   | 359.864 ms (5%) |          |                  |             |
| `["findfirst", "n=400", "reduce", "basesize=128"]`  | 186.929 ms (5%) |          | 1012.86 KiB (1%) |       17725 |
| `["findfirst", "n=400", "reduce", "basesize=256"]`  | 202.454 ms (5%) |          |  509.63 KiB (1%) |        8952 |
| `["findfirst", "n=400", "reduce", "basesize=512"]`  | 191.084 ms (5%) |          |  258.84 KiB (1%) |        4564 |
| `["findfirst", "n=500", "foldl"]`                   |  60.376 ms (5%) |          |                  |             |
| `["findfirst", "n=500", "reduce", "basesize=128"]`  |  31.483 ms (5%) |          |  152.59 KiB (1%) |        2677 |
| `["findfirst", "n=500", "reduce", "basesize=256"]`  |  31.523 ms (5%) |          |   82.00 KiB (1%) |        1444 |
| `["findfirst", "n=500", "reduce", "basesize=512"]`  |  33.482 ms (5%) |          |   46.83 KiB (1%) |         827 |
| `["overhead", "default"]`                           | 140.401 μs (5%) |          |  140.75 KiB (1%) |        2465 |
| `["overhead", "stoppable=false"]`                   | 141.501 μs (5%) |          |  140.78 KiB (1%) |        2465 |
| `["overhead", "stoppable=true"]`                    | 258.203 μs (5%) |          |  140.78 KiB (1%) |        2465 |
| `["parallel_histogram", "assoc", "basesize=16384"]` |   3.354 ms (5%) |          |  731.81 KiB (1%) |          94 |
| `["parallel_histogram", "assoc", "basesize=4096"]`  |   4.046 ms (5%) |          |    2.07 MiB (1%) |         454 |
| `["parallel_histogram", "assoc", "basesize=8192"]`  |   3.704 ms (5%) |          |    1.43 MiB (1%) |         220 |
| `["parallel_histogram", "comm", "basesize=16384"]`  |  10.794 ms (5%) |          | 1010.70 KiB (1%) |         239 |
| `["parallel_histogram", "comm", "basesize=4096"]`   |  16.057 ms (5%) |          |    1.03 MiB (1%) |        1528 |
| `["parallel_histogram", "comm", "basesize=8192"]`   |  14.523 ms (5%) |          |    1.24 MiB (1%) |         663 |
| `["parallel_histogram", "seq"]`                     |   6.184 ms (5%) |          |  364.61 KiB (1%) |          24 |
| `["sum", "random", "foldl"]`                        |  11.725 ms (5%) |          |    32 bytes (1%) |           2 |
| `["sum", "random", "reduce", "basesize=128"]`       |   6.079 ms (5%) |          |  292.02 KiB (1%) |        5213 |
| `["sum", "random", "reduce", "basesize=256"]`       |   5.932 ms (5%) |          |  144.53 KiB (1%) |        2589 |
| `["sum", "random", "reduce", "basesize=512"]`       |   5.866 ms (5%) |          |   71.11 KiB (1%) |        1279 |
| `["sum", "uniform", "foldl"]`                       |  11.125 ms (5%) |          |    32 bytes (1%) |           2 |
| `["sum", "uniform", "reduce", "basesize=128"]`      |   6.162 ms (5%) |          |  292.02 KiB (1%) |        5213 |
| `["sum", "uniform", "reduce", "basesize=256"]`      |   5.809 ms (5%) |          |  144.53 KiB (1%) |        2589 |
| `["sum", "uniform", "reduce", "basesize=512"]`      |   5.732 ms (5%) |          |   71.06 KiB (1%) |        1278 |
| `["sum", "valley", "foldl"]`                        |  11.594 ms (5%) |          |    32 bytes (1%) |           2 |
| `["sum", "valley", "reduce", "basesize=128"]`       |   6.132 ms (5%) |          |  292.02 KiB (1%) |        5213 |
| `["sum", "valley", "reduce", "basesize=256"]`       |   6.019 ms (5%) |          |  144.53 KiB (1%) |        2589 |
| `["sum", "valley", "reduce", "basesize=512"]`       |   5.840 ms (5%) |          |   71.06 KiB (1%) |        1278 |
| `["words", "nthreads=1"]`                           |  20.268 ms (5%) |          |   31.74 MiB (1%) |     1034759 |
| `["words", "nthreads=2"]`                           |  13.875 ms (5%) |          |   32.46 MiB (1%) |     1034929 |
| `["words", "nthreads=4"]`                           |  13.999 ms (5%) |          |   32.91 MiB (1%) |     1035066 |

## Benchmark Group List
Here's a list of all the benchmark groups executed by this job:

- `["collect", "assoc"]`
- `["collect"]`
- `["collect", "unordered"]`
- `["findfirst", "n=1000"]`
- `["findfirst", "n=1000", "reduce"]`
- `["findfirst", "n=400"]`
- `["findfirst", "n=400", "reduce"]`
- `["findfirst", "n=500"]`
- `["findfirst", "n=500", "reduce"]`
- `["overhead"]`
- `["parallel_histogram", "assoc"]`
- `["parallel_histogram", "comm"]`
- `["parallel_histogram"]`
- `["sum", "random"]`
- `["sum", "random", "reduce"]`
- `["sum", "uniform"]`
- `["sum", "uniform", "reduce"]`
- `["sum", "valley"]`
- `["sum", "valley", "reduce"]`
- `["words"]`

## Julia versioninfo
```
Julia Version 1.5.1
Commit 697e782ab8 (2020-08-25 20:08 UTC)
Platform Info:
  OS: Linux (x86_64-pc-linux-gnu)
      Ubuntu 18.04.5 LTS
  uname: Linux 5.4.0-1023-azure #23~18.04.1-Ubuntu SMP Thu Aug 20 14:46:48 UTC 2020 x86_64 x86_64
  CPU: Intel(R) Xeon(R) CPU E5-2673 v4 @ 2.30GHz: 
              speed         user         nice          sys         idle          irq
       #1  2294 MHz      74979 s          0 s       3195 s      21296 s          0 s
       #2  2294 MHz      66089 s          0 s       3240 s      30564 s          0 s
       
  Memory: 6.764892578125 GB (3058.61328125 MB free)
  Uptime: 1019.0 sec
  Load Avg:  1.6474609375  1.59814453125  1.1025390625
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-9.0.1 (ORCJIT, broadwell)
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
    CPU MHz:             2294.684
    BogoMIPS:            4589.36
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

