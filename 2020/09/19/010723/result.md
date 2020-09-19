# Multi-thread benchmark result

* Pull request commit: [`71116043cd3c31418c719ef04539762f3b4a0b3e`](https://github.com/JuliaFolds/Transducers.jl/commit/71116043cd3c31418c719ef04539762f3b4a0b3e)
* Pull request: <https://github.com/JuliaFolds/Transducers.jl/pull/243> (Update */Manifest.toml)

# Judge result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmarks:
    - Target: 19 Sep 2020 - 01:01
    - Baseline: 19 Sep 2020 - 01:06
* Package commits:
    - Target: bc04fd
    - Baseline: b2fa04
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

| ID                                                  | time ratio    | memory ratio  |
|-----------------------------------------------------|---------------|---------------|
| `["collect", "assoc", "basesize=1"]`                | 1.05 (5%) :x: |    1.00 (1%)  |
| `["collect", "unordered", "basesize=1024"]`         | 1.41 (5%) :x: | 1.12 (1%) :x: |
| `["overhead", "default"]`                           | 1.11 (5%) :x: |    1.00 (1%)  |
| `["overhead", "stoppable=false"]`                   | 1.07 (5%) :x: |    1.00 (1%)  |
| `["parallel_histogram", "assoc", "basesize=16384"]` | 1.06 (5%) :x: |    1.00 (1%)  |
| `["parallel_histogram", "assoc", "basesize=4096"]`  | 1.07 (5%) :x: |    1.00 (1%)  |
| `["parallel_histogram", "assoc", "basesize=8192"]`  | 1.07 (5%) :x: |    1.00 (1%)  |
| `["parallel_histogram", "comm", "basesize=16384"]`  | 1.06 (5%) :x: | 1.20 (1%) :x: |
| `["parallel_histogram", "comm", "basesize=8192"]`   | 1.14 (5%) :x: |    0.99 (1%)  |
| `["parallel_histogram", "seq"]`                     | 1.08 (5%) :x: |    1.00 (1%)  |
| `["sum", "uniform", "reduce", "basesize=256"]`      | 1.09 (5%) :x: |    1.00 (1%)  |
| `["sum", "valley", "foldl"]`                        | 1.09 (5%) :x: |    1.00 (1%)  |
| `["sum", "valley", "reduce", "basesize=128"]`       | 1.06 (5%) :x: |    1.00 (1%)  |
| `["sum", "valley", "reduce", "basesize=256"]`       | 1.07 (5%) :x: |    1.00 (1%)  |
| `["sum", "valley", "reduce", "basesize=512"]`       | 1.08 (5%) :x: |    1.00 (1%)  |
| `["words", "nthreads=2"]`                           | 1.08 (5%) :x: | 1.01 (1%) :x: |
| `["words", "nthreads=4"]`                           | 1.08 (5%) :x: |    1.01 (1%)  |

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
  uname: Linux 5.4.0-1025-azure #25~18.04.1-Ubuntu SMP Sat Sep 5 15:28:57 UTC 2020 x86_64 x86_64
  CPU: Intel(R) Xeon(R) CPU E5-2673 v4 @ 2.30GHz: 
              speed         user         nice          sys         idle          irq
       #1  2294 MHz      51072 s          0 s       2580 s      18101 s          0 s
       #2  2294 MHz      47184 s          0 s       2634 s      22402 s          0 s
       
  Memory: 6.764892578125 GB (3019.3984375 MB free)
  Uptime: 743.0 sec
  Load Avg:  1.62109375  1.51806640625  0.93212890625
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
  uname: Linux 5.4.0-1025-azure #25~18.04.1-Ubuntu SMP Sat Sep 5 15:28:57 UTC 2020 x86_64 x86_64
  CPU: Intel(R) Xeon(R) CPU E5-2673 v4 @ 2.30GHz: 
              speed         user         nice          sys         idle          irq
       #1  2294 MHz      73103 s          0 s       3289 s      27422 s          0 s
       #2  2294 MHz      72695 s          0 s       3349 s      28304 s          0 s
       
  Memory: 6.764892578125 GB (3011.53515625 MB free)
  Uptime: 1067.0 sec
  Load Avg:  1.59326171875  1.57421875  1.13232421875
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-9.0.1 (ORCJIT, broadwell)
```

---
# Target result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmark: 19 Sep 2020 - 1:1
* Package commit: bc04fd
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
| `["collect", "assoc", "basesize=1"]`                | 322.314 ms (5%) | 13.715 ms |   82.16 MiB (1%) |     1368065 |
| `["collect", "assoc", "basesize=1024"]`             | 181.700 ms (5%) |           |    1.83 MiB (1%) |        1597 |
| `["collect", "assoc", "basesize=32"]`               | 187.086 ms (5%) |           |    5.47 MiB (1%) |       47069 |
| `["collect", "seq"]`                                | 347.819 ms (5%) |           |  512.72 KiB (1%) |          15 |
| `["collect", "unordered", "basesize=1"]`            | 463.029 ms (5%) |           |   30.01 MiB (1%) |      360665 |
| `["collect", "unordered", "basesize=1024"]`         | 283.448 ms (5%) |           |  876.08 KiB (1%) |        4774 |
| `["collect", "unordered", "basesize=32"]`           | 214.745 ms (5%) |           |    1.48 MiB (1%) |       12855 |
| `["findfirst", "n=1000", "foldl"]`                  | 584.231 ms (5%) |           |                  |             |
| `["findfirst", "n=1000", "reduce", "basesize=128"]` | 308.287 ms (5%) |           |  546.34 KiB (1%) |        9562 |
| `["findfirst", "n=1000", "reduce", "basesize=256"]` | 303.701 ms (5%) |           |  278.25 KiB (1%) |        4888 |
| `["findfirst", "n=1000", "reduce", "basesize=512"]` | 303.923 ms (5%) |           |  144.64 KiB (1%) |        2549 |
| `["findfirst", "n=400", "foldl"]`                   | 432.937 ms (5%) |           |                  |             |
| `["findfirst", "n=400", "reduce", "basesize=128"]`  | 224.929 ms (5%) |           | 1012.86 KiB (1%) |       17725 |
| `["findfirst", "n=400", "reduce", "basesize=256"]`  | 224.536 ms (5%) |           |  509.63 KiB (1%) |        8952 |
| `["findfirst", "n=400", "reduce", "basesize=512"]`  | 225.510 ms (5%) |           |  258.83 KiB (1%) |        4563 |
| `["findfirst", "n=500", "foldl"]`                   |  74.669 ms (5%) |           |                  |             |
| `["findfirst", "n=500", "reduce", "basesize=128"]`  |  38.514 ms (5%) |           |  152.59 KiB (1%) |        2677 |
| `["findfirst", "n=500", "reduce", "basesize=256"]`  |  38.015 ms (5%) |           |   82.00 KiB (1%) |        1444 |
| `["findfirst", "n=500", "reduce", "basesize=512"]`  |  41.647 ms (5%) |           |   46.83 KiB (1%) |         827 |
| `["overhead", "default"]`                           | 160.600 μs (5%) |           |  140.75 KiB (1%) |        2465 |
| `["overhead", "stoppable=false"]`                   | 157.300 μs (5%) |           |  140.78 KiB (1%) |        2465 |
| `["overhead", "stoppable=true"]`                    | 292.500 μs (5%) |           |  140.78 KiB (1%) |        2465 |
| `["parallel_histogram", "assoc", "basesize=16384"]` |   4.210 ms (5%) |           |  731.81 KiB (1%) |          94 |
| `["parallel_histogram", "assoc", "basesize=4096"]`  |   5.034 ms (5%) |           |    1.80 MiB (1%) |         448 |
| `["parallel_histogram", "assoc", "basesize=8192"]`  |   4.525 ms (5%) |           |    1.43 MiB (1%) |         220 |
| `["parallel_histogram", "comm", "basesize=16384"]`  |  12.831 ms (5%) |           |    1.22 MiB (1%) |         208 |
| `["parallel_histogram", "comm", "basesize=4096"]`   |  17.681 ms (5%) |           |    1.01 MiB (1%) |        1161 |
| `["parallel_histogram", "comm", "basesize=8192"]`   |  16.105 ms (5%) |           |    1.22 MiB (1%) |         279 |
| `["parallel_histogram", "seq"]`                     |   7.319 ms (5%) |           |  364.61 KiB (1%) |          24 |
| `["sum", "random", "foldl"]`                        |  13.900 ms (5%) |           |    32 bytes (1%) |           2 |
| `["sum", "random", "reduce", "basesize=128"]`       |   7.490 ms (5%) |           |  292.02 KiB (1%) |        5213 |
| `["sum", "random", "reduce", "basesize=256"]`       |   7.282 ms (5%) |           |  144.53 KiB (1%) |        2589 |
| `["sum", "random", "reduce", "basesize=512"]`       |   7.110 ms (5%) |           |   71.11 KiB (1%) |        1279 |
| `["sum", "uniform", "foldl"]`                       |  13.484 ms (5%) |           |    32 bytes (1%) |           2 |
| `["sum", "uniform", "reduce", "basesize=128"]`      |   7.149 ms (5%) |           |  292.02 KiB (1%) |        5213 |
| `["sum", "uniform", "reduce", "basesize=256"]`      |   7.047 ms (5%) |           |  144.53 KiB (1%) |        2589 |
| `["sum", "uniform", "reduce", "basesize=512"]`      |   6.974 ms (5%) |           |   71.06 KiB (1%) |        1278 |
| `["sum", "valley", "foldl"]`                        |  14.023 ms (5%) |           |    32 bytes (1%) |           2 |
| `["sum", "valley", "reduce", "basesize=128"]`       |   7.449 ms (5%) |           |  292.02 KiB (1%) |        5213 |
| `["sum", "valley", "reduce", "basesize=256"]`       |   7.280 ms (5%) |           |  144.53 KiB (1%) |        2589 |
| `["sum", "valley", "reduce", "basesize=512"]`       |   7.100 ms (5%) |           |   71.06 KiB (1%) |        1278 |
| `["words", "nthreads=1"]`                           |  24.467 ms (5%) |           |   31.72 MiB (1%) |     1033303 |
| `["words", "nthreads=2"]`                           |  15.618 ms (5%) |           |   32.43 MiB (1%) |     1033451 |
| `["words", "nthreads=4"]`                           |  16.434 ms (5%) |           |   33.07 MiB (1%) |     1033766 |

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
  uname: Linux 5.4.0-1025-azure #25~18.04.1-Ubuntu SMP Sat Sep 5 15:28:57 UTC 2020 x86_64 x86_64
  CPU: Intel(R) Xeon(R) CPU E5-2673 v4 @ 2.30GHz: 
              speed         user         nice          sys         idle          irq
       #1  2294 MHz      51072 s          0 s       2580 s      18101 s          0 s
       #2  2294 MHz      47184 s          0 s       2634 s      22402 s          0 s
       
  Memory: 6.764892578125 GB (3019.3984375 MB free)
  Uptime: 743.0 sec
  Load Avg:  1.62109375  1.51806640625  0.93212890625
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-9.0.1 (ORCJIT, broadwell)
```

---
# Baseline result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmark: 19 Sep 2020 - 1:6
* Package commit: b2fa04
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
| `["collect", "assoc", "basesize=1"]`                | 305.886 ms (5%) | 12.344 ms |   82.16 MiB (1%) |     1368075 |
| `["collect", "assoc", "basesize=1024"]`             | 176.684 ms (5%) |           |    1.83 MiB (1%) |        1597 |
| `["collect", "assoc", "basesize=32"]`               | 181.347 ms (5%) |           |    5.47 MiB (1%) |       47069 |
| `["collect", "seq"]`                                | 344.393 ms (5%) |           |  512.72 KiB (1%) |          15 |
| `["collect", "unordered", "basesize=1"]`            | 441.033 ms (5%) |           |   30.01 MiB (1%) |      360643 |
| `["collect", "unordered", "basesize=1024"]`         | 200.984 ms (5%) |           |  782.45 KiB (1%) |        1760 |
| `["collect", "unordered", "basesize=32"]`           | 207.809 ms (5%) |           |    1.47 MiB (1%) |       12620 |
| `["findfirst", "n=1000", "foldl"]`                  | 597.767 ms (5%) |           |                  |             |
| `["findfirst", "n=1000", "reduce", "basesize=128"]` | 306.223 ms (5%) |           |  546.33 KiB (1%) |        9561 |
| `["findfirst", "n=1000", "reduce", "basesize=256"]` | 301.390 ms (5%) |           |  278.25 KiB (1%) |        4888 |
| `["findfirst", "n=1000", "reduce", "basesize=512"]` | 307.439 ms (5%) |           |  144.66 KiB (1%) |        2550 |
| `["findfirst", "n=400", "foldl"]`                   | 431.678 ms (5%) |           |                  |             |
| `["findfirst", "n=400", "reduce", "basesize=128"]`  | 231.256 ms (5%) |           | 1012.88 KiB (1%) |       17726 |
| `["findfirst", "n=400", "reduce", "basesize=256"]`  | 224.146 ms (5%) |           |  509.63 KiB (1%) |        8952 |
| `["findfirst", "n=400", "reduce", "basesize=512"]`  | 224.782 ms (5%) |           |  258.83 KiB (1%) |        4563 |
| `["findfirst", "n=500", "foldl"]`                   |  74.280 ms (5%) |           |                  |             |
| `["findfirst", "n=500", "reduce", "basesize=128"]`  |  37.508 ms (5%) |           |  152.59 KiB (1%) |        2677 |
| `["findfirst", "n=500", "reduce", "basesize=256"]`  |  37.159 ms (5%) |           |   82.00 KiB (1%) |        1444 |
| `["findfirst", "n=500", "reduce", "basesize=512"]`  |  40.364 ms (5%) |           |   46.80 KiB (1%) |         826 |
| `["overhead", "default"]`                           | 144.800 μs (5%) |           |  140.75 KiB (1%) |        2465 |
| `["overhead", "stoppable=false"]`                   | 147.400 μs (5%) |           |  140.78 KiB (1%) |        2465 |
| `["overhead", "stoppable=true"]`                    | 282.700 μs (5%) |           |  140.78 KiB (1%) |        2465 |
| `["parallel_histogram", "assoc", "basesize=16384"]` |   3.985 ms (5%) |           |  731.81 KiB (1%) |          94 |
| `["parallel_histogram", "assoc", "basesize=4096"]`  |   4.725 ms (5%) |           |    1.80 MiB (1%) |         448 |
| `["parallel_histogram", "assoc", "basesize=8192"]`  |   4.235 ms (5%) |           |    1.43 MiB (1%) |         220 |
| `["parallel_histogram", "comm", "basesize=16384"]`  |  12.055 ms (5%) |           |    1.02 MiB (1%) |         295 |
| `["parallel_histogram", "comm", "basesize=4096"]`   |  17.335 ms (5%) |           |    1.00 MiB (1%) |        1138 |
| `["parallel_histogram", "comm", "basesize=8192"]`   |  14.175 ms (5%) |           |    1.23 MiB (1%) |         545 |
| `["parallel_histogram", "seq"]`                     |   6.797 ms (5%) |           |  364.61 KiB (1%) |          24 |
| `["sum", "random", "foldl"]`                        |  13.765 ms (5%) |           |    32 bytes (1%) |           2 |
| `["sum", "random", "reduce", "basesize=128"]`       |   7.400 ms (5%) |           |  292.02 KiB (1%) |        5213 |
| `["sum", "random", "reduce", "basesize=256"]`       |   7.302 ms (5%) |           |  144.53 KiB (1%) |        2589 |
| `["sum", "random", "reduce", "basesize=512"]`       |   7.125 ms (5%) |           |   71.11 KiB (1%) |        1279 |
| `["sum", "uniform", "foldl"]`                       |  13.322 ms (5%) |           |    32 bytes (1%) |           2 |
| `["sum", "uniform", "reduce", "basesize=128"]`      |   6.937 ms (5%) |           |  292.02 KiB (1%) |        5213 |
| `["sum", "uniform", "reduce", "basesize=256"]`      |   6.458 ms (5%) |           |  144.53 KiB (1%) |        2589 |
| `["sum", "uniform", "reduce", "basesize=512"]`      |   6.817 ms (5%) |           |   71.06 KiB (1%) |        1278 |
| `["sum", "valley", "foldl"]`                        |  12.915 ms (5%) |           |    32 bytes (1%) |           2 |
| `["sum", "valley", "reduce", "basesize=128"]`       |   7.050 ms (5%) |           |  292.02 KiB (1%) |        5213 |
| `["sum", "valley", "reduce", "basesize=256"]`       |   6.784 ms (5%) |           |  144.53 KiB (1%) |        2589 |
| `["sum", "valley", "reduce", "basesize=512"]`       |   6.565 ms (5%) |           |   71.09 KiB (1%) |        1279 |
| `["words", "nthreads=1"]`                           |  24.097 ms (5%) |           |   31.64 MiB (1%) |     1030902 |
| `["words", "nthreads=2"]`                           |  14.403 ms (5%) |           |   31.99 MiB (1%) |     1030971 |
| `["words", "nthreads=4"]`                           |  15.207 ms (5%) |           |   32.90 MiB (1%) |     1031265 |

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
  uname: Linux 5.4.0-1025-azure #25~18.04.1-Ubuntu SMP Sat Sep 5 15:28:57 UTC 2020 x86_64 x86_64
  CPU: Intel(R) Xeon(R) CPU E5-2673 v4 @ 2.30GHz: 
              speed         user         nice          sys         idle          irq
       #1  2294 MHz      73103 s          0 s       3289 s      27422 s          0 s
       #2  2294 MHz      72695 s          0 s       3349 s      28304 s          0 s
       
  Memory: 6.764892578125 GB (3011.53515625 MB free)
  Uptime: 1067.0 sec
  Load Avg:  1.59326171875  1.57421875  1.13232421875
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
    CPU MHz:             2294.683
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

