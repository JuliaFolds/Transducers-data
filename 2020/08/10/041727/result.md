# Multi-thread benchmark result

* Pull request commit: [`29d65cb43cdc1297e624c1372bbe80373d93b483`](https://github.com/JuliaFolds/Transducers.jl/commit/29d65cb43cdc1297e624c1372bbe80373d93b483)
* Pull request: <https://github.com/JuliaFolds/Transducers.jl/pull/412> (Improve compilation latency for non-inferable case)

# Judge result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmarks:
    - Target: 10 Aug 2020 - 04:12
    - Baseline: 10 Aug 2020 - 04:17
* Package commits:
    - Target: 2f6462
    - Baseline: 1f6750
* Julia commits:
    - Target: 96786e
    - Baseline: 96786e
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

| ID                                                  | time ratio                   | memory ratio  |
|-----------------------------------------------------|------------------------------|---------------|
| `["collect", "seq"]`                                |                1.06 (5%) :x: |    1.00 (1%)  |
| `["collect", "unordered", "basesize=1"]`            |                1.08 (5%) :x: |    1.00 (1%)  |
| `["collect", "unordered", "basesize=1024"]`         |                1.16 (5%) :x: | 1.02 (1%) :x: |
| `["findfirst", "n=1000", "foldl"]`                  | 0.95 (5%) :white_check_mark: |    1.00 (1%)  |
| `["findfirst", "n=1000", "reduce", "basesize=128"]` |                1.07 (5%) :x: |    1.00 (1%)  |
| `["findfirst", "n=1000", "reduce", "basesize=256"]` |                1.16 (5%) :x: |    1.00 (1%)  |
| `["findfirst", "n=1000", "reduce", "basesize=512"]` |                1.17 (5%) :x: |    1.00 (1%)  |
| `["findfirst", "n=500", "reduce", "basesize=128"]`  | 0.89 (5%) :white_check_mark: |    1.00 (1%)  |
| `["findfirst", "n=500", "reduce", "basesize=256"]`  | 0.89 (5%) :white_check_mark: |    1.00 (1%)  |
| `["findfirst", "n=500", "reduce", "basesize=512"]`  | 0.89 (5%) :white_check_mark: |    1.00 (1%)  |
| `["parallel_histogram", "comm", "basesize=8192"]`   |                1.06 (5%) :x: |    1.00 (1%)  |
| `["sum", "random", "foldl"]`                        |                1.12 (5%) :x: |    1.00 (1%)  |
| `["sum", "valley", "foldl"]`                        |                1.09 (5%) :x: |    1.00 (1%)  |
| `["words", "nthreads=2"]`                           |                   1.04 (5%)  | 1.01 (1%) :x: |
| `["words", "nthreads=4"]`                           |                   1.05 (5%)  | 1.01 (1%) :x: |

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
Julia Version 1.5.0
Commit 96786e22cc (2020-08-01 23:44 UTC)
Platform Info:
  OS: Linux (x86_64-pc-linux-gnu)
      Ubuntu 18.04.4 LTS
  uname: Linux 5.3.0-1034-azure #35~18.04.1-Ubuntu SMP Mon Jul 13 12:54:45 UTC 2020 x86_64 x86_64
  CPU: Intel(R) Xeon(R) Platinum 8171M CPU @ 2.60GHz: 
              speed         user         nice          sys         idle          irq
       #1  2095 MHz      50121 s          0 s       2212 s      37007 s          0 s
       #2  2095 MHz      46368 s          0 s       2351 s      40708 s          0 s
       
  Memory: 6.764881134033203 GB (3025.5859375 MB free)
  Uptime: 916.0 sec
  Load Avg:  1.66943359375  1.4599609375  0.859375
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-9.0.1 (ORCJIT, skylake)
```

### Baseline
```
Julia Version 1.5.0
Commit 96786e22cc (2020-08-01 23:44 UTC)
Platform Info:
  OS: Linux (x86_64-pc-linux-gnu)
      Ubuntu 18.04.4 LTS
  uname: Linux 5.3.0-1034-azure #35~18.04.1-Ubuntu SMP Mon Jul 13 12:54:45 UTC 2020 x86_64 x86_64
  CPU: Intel(R) Xeon(R) Platinum 8171M CPU @ 2.60GHz: 
              speed         user         nice          sys         idle          irq
       #1  2095 MHz      75031 s          0 s       2677 s      39081 s          0 s
       #2  2095 MHz      64588 s          0 s       2824 s      49666 s          0 s
       
  Memory: 6.764881134033203 GB (3093.703125 MB free)
  Uptime: 1194.0 sec
  Load Avg:  1.7119140625  1.5654296875  1.06005859375
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-9.0.1 (ORCJIT, skylake)
```

---
# Target result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmark: 10 Aug 2020 - 4:12
* Package commit: 2f6462
* Julia commit: 96786e
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
| `["collect", "assoc", "basesize=1"]`                | 308.413 ms (5%) | 9.548 ms |   82.15 MiB (1%) |     1368048 |
| `["collect", "assoc", "basesize=1024"]`             | 202.681 ms (5%) |          |    1.83 MiB (1%) |        1597 |
| `["collect", "assoc", "basesize=32"]`               | 208.507 ms (5%) |          |    5.47 MiB (1%) |       47070 |
| `["collect", "seq"]`                                | 409.326 ms (5%) |          |  512.72 KiB (1%) |          15 |
| `["collect", "unordered", "basesize=1"]`            | 463.728 ms (5%) |          |   30.01 MiB (1%) |      360588 |
| `["collect", "unordered", "basesize=1024"]`         | 282.668 ms (5%) |          |  791.67 KiB (1%) |        2073 |
| `["collect", "unordered", "basesize=32"]`           | 229.231 ms (5%) |          |    1.46 MiB (1%) |       12192 |
| `["findfirst", "n=1000", "foldl"]`                  | 621.759 ms (5%) |          |                  |             |
| `["findfirst", "n=1000", "reduce", "basesize=128"]` | 348.981 ms (5%) |          |  546.33 KiB (1%) |        9561 |
| `["findfirst", "n=1000", "reduce", "basesize=256"]` | 376.869 ms (5%) |          |  278.25 KiB (1%) |        4888 |
| `["findfirst", "n=1000", "reduce", "basesize=512"]` | 384.458 ms (5%) |          |  144.61 KiB (1%) |        2548 |
| `["findfirst", "n=400", "foldl"]`                   | 451.340 ms (5%) |          |                  |             |
| `["findfirst", "n=400", "reduce", "basesize=128"]`  | 244.773 ms (5%) |          | 1012.89 KiB (1%) |       17726 |
| `["findfirst", "n=400", "reduce", "basesize=256"]`  | 245.655 ms (5%) |          |  509.63 KiB (1%) |        8952 |
| `["findfirst", "n=400", "reduce", "basesize=512"]`  | 245.303 ms (5%) |          |  258.83 KiB (1%) |        4563 |
| `["findfirst", "n=500", "foldl"]`                   |  81.658 ms (5%) |          |                  |             |
| `["findfirst", "n=500", "reduce", "basesize=128"]`  |  42.844 ms (5%) |          |  152.59 KiB (1%) |        2677 |
| `["findfirst", "n=500", "reduce", "basesize=256"]`  |  42.543 ms (5%) |          |   82.00 KiB (1%) |        1444 |
| `["findfirst", "n=500", "reduce", "basesize=512"]`  |  45.442 ms (5%) |          |   46.83 KiB (1%) |         827 |
| `["overhead", "default"]`                           | 142.605 μs (5%) |          |  140.72 KiB (1%) |        2464 |
| `["overhead", "stoppable=false"]`                   | 143.706 μs (5%) |          |  140.78 KiB (1%) |        2465 |
| `["overhead", "stoppable=true"]`                    | 260.711 μs (5%) |          |  140.78 KiB (1%) |        2465 |
| `["parallel_histogram", "assoc", "basesize=16384"]` |   4.310 ms (5%) |          |  731.81 KiB (1%) |          94 |
| `["parallel_histogram", "assoc", "basesize=4096"]`  |   4.889 ms (5%) |          |    1.80 MiB (1%) |         448 |
| `["parallel_histogram", "assoc", "basesize=8192"]`  |   4.623 ms (5%) |          |    1.43 MiB (1%) |         220 |
| `["parallel_histogram", "comm", "basesize=16384"]`  |  14.359 ms (5%) |          |    1.22 MiB (1%) |         160 |
| `["parallel_histogram", "comm", "basesize=4096"]`   |  23.945 ms (5%) |          |    1.04 MiB (1%) |        1342 |
| `["parallel_histogram", "comm", "basesize=8192"]`   |  19.595 ms (5%) |          |    1.25 MiB (1%) |         978 |
| `["parallel_histogram", "seq"]`                     |   7.190 ms (5%) |          |  364.61 KiB (1%) |          24 |
| `["sum", "random", "foldl"]`                        |  15.679 ms (5%) |          |    32 bytes (1%) |           2 |
| `["sum", "random", "reduce", "basesize=128"]`       |   8.018 ms (5%) |          |  292.02 KiB (1%) |        5213 |
| `["sum", "random", "reduce", "basesize=256"]`       |   7.922 ms (5%) |          |  144.53 KiB (1%) |        2589 |
| `["sum", "random", "reduce", "basesize=512"]`       |   7.819 ms (5%) |          |   71.11 KiB (1%) |        1279 |
| `["sum", "uniform", "foldl"]`                       |  13.507 ms (5%) |          |    32 bytes (1%) |           2 |
| `["sum", "uniform", "reduce", "basesize=128"]`      |   7.793 ms (5%) |          |  292.02 KiB (1%) |        5213 |
| `["sum", "uniform", "reduce", "basesize=256"]`      |   7.641 ms (5%) |          |  144.53 KiB (1%) |        2589 |
| `["sum", "uniform", "reduce", "basesize=512"]`      |   7.556 ms (5%) |          |   71.06 KiB (1%) |        1278 |
| `["sum", "valley", "foldl"]`                        |  15.858 ms (5%) |          |    32 bytes (1%) |           2 |
| `["sum", "valley", "reduce", "basesize=128"]`       |   8.199 ms (5%) |          |  292.02 KiB (1%) |        5213 |
| `["sum", "valley", "reduce", "basesize=256"]`       |   8.119 ms (5%) |          |  144.53 KiB (1%) |        2589 |
| `["sum", "valley", "reduce", "basesize=512"]`       |   7.891 ms (5%) |          |   71.09 KiB (1%) |        1279 |
| `["words", "nthreads=1"]`                           |  19.167 ms (5%) |          |   31.80 MiB (1%) |     1036451 |
| `["words", "nthreads=2"]`                           |  13.765 ms (5%) |          |   32.52 MiB (1%) |     1036594 |
| `["words", "nthreads=4"]`                           |  14.671 ms (5%) |          |   33.15 MiB (1%) |     1036885 |

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
Julia Version 1.5.0
Commit 96786e22cc (2020-08-01 23:44 UTC)
Platform Info:
  OS: Linux (x86_64-pc-linux-gnu)
      Ubuntu 18.04.4 LTS
  uname: Linux 5.3.0-1034-azure #35~18.04.1-Ubuntu SMP Mon Jul 13 12:54:45 UTC 2020 x86_64 x86_64
  CPU: Intel(R) Xeon(R) Platinum 8171M CPU @ 2.60GHz: 
              speed         user         nice          sys         idle          irq
       #1  2095 MHz      50121 s          0 s       2212 s      37007 s          0 s
       #2  2095 MHz      46368 s          0 s       2351 s      40708 s          0 s
       
  Memory: 6.764881134033203 GB (3025.5859375 MB free)
  Uptime: 916.0 sec
  Load Avg:  1.66943359375  1.4599609375  0.859375
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-9.0.1 (ORCJIT, skylake)
```

---
# Baseline result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmark: 10 Aug 2020 - 4:17
* Package commit: 1f6750
* Julia commit: 96786e
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
| `["collect", "assoc", "basesize=1"]`                | 307.088 ms (5%) | 10.845 ms |   82.16 MiB (1%) |     1368051 |
| `["collect", "assoc", "basesize=1024"]`             | 202.186 ms (5%) |           |    1.83 MiB (1%) |        1597 |
| `["collect", "assoc", "basesize=32"]`               | 205.899 ms (5%) |           |    5.47 MiB (1%) |       47069 |
| `["collect", "seq"]`                                | 387.197 ms (5%) |           |  512.72 KiB (1%) |          15 |
| `["collect", "unordered", "basesize=1"]`            | 429.429 ms (5%) |           |   30.01 MiB (1%) |      360748 |
| `["collect", "unordered", "basesize=1024"]`         | 244.047 ms (5%) |           |  778.83 KiB (1%) |        1662 |
| `["collect", "unordered", "basesize=32"]`           | 226.857 ms (5%) |           |    1.47 MiB (1%) |       12400 |
| `["findfirst", "n=1000", "foldl"]`                  | 655.507 ms (5%) |           |                  |             |
| `["findfirst", "n=1000", "reduce", "basesize=128"]` | 325.324 ms (5%) |           |  546.33 KiB (1%) |        9561 |
| `["findfirst", "n=1000", "reduce", "basesize=256"]` | 325.112 ms (5%) |           |  278.25 KiB (1%) |        4888 |
| `["findfirst", "n=1000", "reduce", "basesize=512"]` | 328.881 ms (5%) |           |  144.66 KiB (1%) |        2550 |
| `["findfirst", "n=400", "foldl"]`                   | 463.503 ms (5%) |           |                  |             |
| `["findfirst", "n=400", "reduce", "basesize=128"]`  | 244.678 ms (5%) |           | 1012.89 KiB (1%) |       17726 |
| `["findfirst", "n=400", "reduce", "basesize=256"]`  | 241.168 ms (5%) |           |  509.63 KiB (1%) |        8952 |
| `["findfirst", "n=400", "reduce", "basesize=512"]`  | 243.924 ms (5%) |           |  258.84 KiB (1%) |        4564 |
| `["findfirst", "n=500", "foldl"]`                   |  78.470 ms (5%) |           |                  |             |
| `["findfirst", "n=500", "reduce", "basesize=128"]`  |  48.109 ms (5%) |           |  152.59 KiB (1%) |        2677 |
| `["findfirst", "n=500", "reduce", "basesize=256"]`  |  47.966 ms (5%) |           |   82.00 KiB (1%) |        1444 |
| `["findfirst", "n=500", "reduce", "basesize=512"]`  |  51.297 ms (5%) |           |   46.84 KiB (1%) |         828 |
| `["overhead", "default"]`                           | 145.211 μs (5%) |           |  140.72 KiB (1%) |        2464 |
| `["overhead", "stoppable=false"]`                   | 143.310 μs (5%) |           |  140.78 KiB (1%) |        2465 |
| `["overhead", "stoppable=true"]`                    | 262.019 μs (5%) |           |  140.78 KiB (1%) |        2465 |
| `["parallel_histogram", "assoc", "basesize=16384"]` |   4.353 ms (5%) |           |  731.81 KiB (1%) |          94 |
| `["parallel_histogram", "assoc", "basesize=4096"]`  |   4.917 ms (5%) |           |    1.80 MiB (1%) |         448 |
| `["parallel_histogram", "assoc", "basesize=8192"]`  |   4.630 ms (5%) |           |    1.43 MiB (1%) |         220 |
| `["parallel_histogram", "comm", "basesize=16384"]`  |  13.948 ms (5%) |           |    1.22 MiB (1%) |         207 |
| `["parallel_histogram", "comm", "basesize=4096"]`   |  24.106 ms (5%) |           |    1.03 MiB (1%) |        1235 |
| `["parallel_histogram", "comm", "basesize=8192"]`   |  18.503 ms (5%) |           |    1.25 MiB (1%) |        1003 |
| `["parallel_histogram", "seq"]`                     |   6.873 ms (5%) |           |  364.61 KiB (1%) |          24 |
| `["sum", "random", "foldl"]`                        |  14.003 ms (5%) |           |    32 bytes (1%) |           2 |
| `["sum", "random", "reduce", "basesize=128"]`       |   8.101 ms (5%) |           |  292.02 KiB (1%) |        5213 |
| `["sum", "random", "reduce", "basesize=256"]`       |   7.884 ms (5%) |           |  144.53 KiB (1%) |        2589 |
| `["sum", "random", "reduce", "basesize=512"]`       |   7.778 ms (5%) |           |   71.11 KiB (1%) |        1279 |
| `["sum", "uniform", "foldl"]`                       |  13.902 ms (5%) |           |    32 bytes (1%) |           2 |
| `["sum", "uniform", "reduce", "basesize=128"]`      |   7.838 ms (5%) |           |  292.02 KiB (1%) |        5213 |
| `["sum", "uniform", "reduce", "basesize=256"]`      |   7.671 ms (5%) |           |  144.53 KiB (1%) |        2589 |
| `["sum", "uniform", "reduce", "basesize=512"]`      |   7.537 ms (5%) |           |   71.06 KiB (1%) |        1278 |
| `["sum", "valley", "foldl"]`                        |  14.506 ms (5%) |           |    32 bytes (1%) |           2 |
| `["sum", "valley", "reduce", "basesize=128"]`       |   8.087 ms (5%) |           |  292.02 KiB (1%) |        5213 |
| `["sum", "valley", "reduce", "basesize=256"]`       |   7.958 ms (5%) |           |  144.53 KiB (1%) |        2589 |
| `["sum", "valley", "reduce", "basesize=512"]`       |   7.829 ms (5%) |           |   71.06 KiB (1%) |        1278 |
| `["words", "nthreads=1"]`                           |  19.577 ms (5%) |           |   31.73 MiB (1%) |     1033786 |
| `["words", "nthreads=2"]`                           |  13.290 ms (5%) |           |   32.09 MiB (1%) |     1033859 |
| `["words", "nthreads=4"]`                           |  13.996 ms (5%) |           |   32.81 MiB (1%) |     1034004 |

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
Julia Version 1.5.0
Commit 96786e22cc (2020-08-01 23:44 UTC)
Platform Info:
  OS: Linux (x86_64-pc-linux-gnu)
      Ubuntu 18.04.4 LTS
  uname: Linux 5.3.0-1034-azure #35~18.04.1-Ubuntu SMP Mon Jul 13 12:54:45 UTC 2020 x86_64 x86_64
  CPU: Intel(R) Xeon(R) Platinum 8171M CPU @ 2.60GHz: 
              speed         user         nice          sys         idle          irq
       #1  2095 MHz      75031 s          0 s       2677 s      39081 s          0 s
       #2  2095 MHz      64588 s          0 s       2824 s      49666 s          0 s
       
  Memory: 6.764881134033203 GB (3093.703125 MB free)
  Uptime: 1194.0 sec
  Load Avg:  1.7119140625  1.5654296875  1.06005859375
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-9.0.1 (ORCJIT, skylake)
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

