# Multi-thread benchmark result

* Pull request commit: [`fbbc9c3eb413404cb4dbad72ab53b38cb70c58e5`](https://github.com/JuliaFolds/Transducers.jl/commit/fbbc9c3eb413404cb4dbad72ab53b38cb70c58e5)
* Pull request: <https://github.com/JuliaFolds/Transducers.jl/pull/451> (Warn that Consecutive and Reduced are incompatible in parallel folds)

# Judge result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmarks:
    - Target: 18 Jan 2021 - 04:40
    - Baseline: 18 Jan 2021 - 04:45
* Package commits:
    - Target: eb54f3
    - Baseline: 8e896a
* Julia commits:
    - Target: 788b2c
    - Baseline: 788b2c
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
| `["collect", "assoc", "basesize=1"]`                | 0.93 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["collect", "unordered", "basesize=1024"]`         |                   1.03 (5%)  |                1.02 (1%) :x: |
| `["findfirst", "n=500", "reduce", "basesize=512"]`  | 0.94 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["overhead", "default"]`                           | 0.94 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["parallel_histogram", "assoc", "basesize=4096"]`  | 0.90 (5%) :white_check_mark: | 0.87 (1%) :white_check_mark: |
| `["parallel_histogram", "comm", "basesize=8192"]`   | 0.94 (5%) :white_check_mark: |                   0.99 (1%)  |
| `["sum", "random", "reduce", "basesize=128"]`       | 0.91 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["sum", "random", "reduce", "basesize=256"]`       | 0.89 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["sum", "uniform", "foldl"]`                       | 0.94 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["sum", "uniform", "reduce", "basesize=128"]`      | 0.92 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["sum", "uniform", "reduce", "basesize=256"]`      | 0.90 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["sum", "uniform", "reduce", "basesize=512"]`      | 0.87 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["sum", "valley", "reduce", "basesize=256"]`       | 0.95 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["sum", "valley", "reduce", "basesize=512"]`       | 0.90 (5%) :white_check_mark: |                   1.00 (1%)  |

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
Julia Version 1.5.3
Commit 788b2c77c1 (2020-11-09 13:37 UTC)
Platform Info:
  OS: Linux (x86_64-pc-linux-gnu)
      Ubuntu 18.04.5 LTS
  uname: Linux 5.4.0-1036-azure #38~18.04.1-Ubuntu SMP Wed Jan 6 18:26:30 UTC 2021 x86_64 x86_64
  CPU: Intel(R) Xeon(R) Platinum 8171M CPU @ 2.60GHz: 
              speed         user         nice          sys         idle          irq
       #1  2095 MHz      48764 s          0 s       2250 s      19181 s          0 s
       #2  2095 MHz      51747 s          0 s       2453 s      16139 s          0 s
       
  Memory: 6.791393280029297 GB (3655.63671875 MB free)
  Uptime: 720.0 sec
  Load Avg:  1.72119140625  1.4873046875  0.88427734375
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-9.0.1 (ORCJIT, skylake-avx512)
```

### Baseline
```
Julia Version 1.5.3
Commit 788b2c77c1 (2020-11-09 13:37 UTC)
Platform Info:
  OS: Linux (x86_64-pc-linux-gnu)
      Ubuntu 18.04.5 LTS
  uname: Linux 5.4.0-1036-azure #38~18.04.1-Ubuntu SMP Wed Jan 6 18:26:30 UTC 2021 x86_64 x86_64
  CPU: Intel(R) Xeon(R) Platinum 8171M CPU @ 2.60GHz: 
              speed         user         nice          sys         idle          irq
       #1  2095 MHz      71387 s          0 s       2800 s      24909 s          0 s
       #2  2095 MHz      73592 s          0 s       3072 s      22559 s          0 s
       
  Memory: 6.791393280029297 GB (3676.5 MB free)
  Uptime: 1010.0 sec
  Load Avg:  1.65576171875  1.587890625  1.09521484375
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-9.0.1 (ORCJIT, skylake-avx512)
```

---
# Target result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmark: 18 Jan 2021 - 4:40
* Package commit: eb54f3
* Julia commit: 788b2c
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
| `["collect", "assoc", "basesize=1"]`                | 359.810 ms (5%) | 10.836 ms |   82.15 MiB (1%) |     1368047 |
| `["collect", "assoc", "basesize=1024"]`             | 236.044 ms (5%) |           |    1.83 MiB (1%) |        1597 |
| `["collect", "assoc", "basesize=32"]`               | 244.001 ms (5%) |           |    5.47 MiB (1%) |       47070 |
| `["collect", "seq"]`                                | 449.982 ms (5%) |           |  512.72 KiB (1%) |          15 |
| `["collect", "unordered", "basesize=1"]`            | 480.434 ms (5%) |           |   30.01 MiB (1%) |      360587 |
| `["collect", "unordered", "basesize=1024"]`         | 293.608 ms (5%) |           |  799.58 KiB (1%) |        2326 |
| `["collect", "unordered", "basesize=32"]`           | 256.313 ms (5%) |           |    1.47 MiB (1%) |       12343 |
| `["findfirst", "n=1000", "foldl"]`                  | 742.366 ms (5%) |           |                  |             |
| `["findfirst", "n=1000", "reduce", "basesize=128"]` | 372.627 ms (5%) |           |  546.33 KiB (1%) |        9561 |
| `["findfirst", "n=1000", "reduce", "basesize=256"]` | 376.139 ms (5%) |           |  278.25 KiB (1%) |        4888 |
| `["findfirst", "n=1000", "reduce", "basesize=512"]` | 375.830 ms (5%) |           |  144.64 KiB (1%) |        2549 |
| `["findfirst", "n=400", "foldl"]`                   | 561.622 ms (5%) |           |                  |             |
| `["findfirst", "n=400", "reduce", "basesize=128"]`  | 287.340 ms (5%) |           | 1012.86 KiB (1%) |       17725 |
| `["findfirst", "n=400", "reduce", "basesize=256"]`  | 286.008 ms (5%) |           |  509.63 KiB (1%) |        8952 |
| `["findfirst", "n=400", "reduce", "basesize=512"]`  | 285.124 ms (5%) |           |  258.83 KiB (1%) |        4563 |
| `["findfirst", "n=500", "foldl"]`                   |  92.203 ms (5%) |           |                  |             |
| `["findfirst", "n=500", "reduce", "basesize=128"]`  |  48.425 ms (5%) |           |  152.59 KiB (1%) |        2677 |
| `["findfirst", "n=500", "reduce", "basesize=256"]`  |  48.159 ms (5%) |           |   82.00 KiB (1%) |        1444 |
| `["findfirst", "n=500", "reduce", "basesize=512"]`  |  49.660 ms (5%) |           |   46.83 KiB (1%) |         827 |
| `["overhead", "default"]`                           | 155.509 μs (5%) |           |  140.72 KiB (1%) |        2464 |
| `["overhead", "stoppable=false"]`                   | 158.209 μs (5%) |           |  140.75 KiB (1%) |        2464 |
| `["overhead", "stoppable=true"]`                    | 306.417 μs (5%) |           |  140.78 KiB (1%) |        2465 |
| `["parallel_histogram", "assoc", "basesize=16384"]` |   5.088 ms (5%) |           |  731.81 KiB (1%) |          94 |
| `["parallel_histogram", "assoc", "basesize=4096"]`  |   5.540 ms (5%) |           |    1.80 MiB (1%) |         448 |
| `["parallel_histogram", "assoc", "basesize=8192"]`  |   5.477 ms (5%) |           |    1.43 MiB (1%) |         220 |
| `["parallel_histogram", "comm", "basesize=16384"]`  |  15.656 ms (5%) |           |    1.22 MiB (1%) |         160 |
| `["parallel_histogram", "comm", "basesize=4096"]`   |  23.116 ms (5%) |           |    1.04 MiB (1%) |        1647 |
| `["parallel_histogram", "comm", "basesize=8192"]`   |  18.790 ms (5%) |           |    1.24 MiB (1%) |         877 |
| `["parallel_histogram", "seq"]`                     |   8.706 ms (5%) |           |  364.61 KiB (1%) |          24 |
| `["sum", "random", "foldl"]`                        |  18.548 ms (5%) |           |    32 bytes (1%) |           2 |
| `["sum", "random", "reduce", "basesize=128"]`       |   8.946 ms (5%) |           |  292.02 KiB (1%) |        5213 |
| `["sum", "random", "reduce", "basesize=256"]`       |   8.693 ms (5%) |           |  144.53 KiB (1%) |        2589 |
| `["sum", "random", "reduce", "basesize=512"]`       |   9.728 ms (5%) |           |   71.11 KiB (1%) |        1279 |
| `["sum", "uniform", "foldl"]`                       |  16.709 ms (5%) |           |    32 bytes (1%) |           2 |
| `["sum", "uniform", "reduce", "basesize=128"]`      |   8.952 ms (5%) |           |  292.02 KiB (1%) |        5213 |
| `["sum", "uniform", "reduce", "basesize=256"]`      |   8.409 ms (5%) |           |  144.53 KiB (1%) |        2589 |
| `["sum", "uniform", "reduce", "basesize=512"]`      |   8.011 ms (5%) |           |   71.06 KiB (1%) |        1278 |
| `["sum", "valley", "foldl"]`                        |  17.368 ms (5%) |           |    32 bytes (1%) |           2 |
| `["sum", "valley", "reduce", "basesize=128"]`       |   9.299 ms (5%) |           |  292.02 KiB (1%) |        5213 |
| `["sum", "valley", "reduce", "basesize=256"]`       |   9.213 ms (5%) |           |  144.53 KiB (1%) |        2589 |
| `["sum", "valley", "reduce", "basesize=512"]`       |   8.689 ms (5%) |           |   71.09 KiB (1%) |        1279 |
| `["words", "nthreads=1"]`                           |  24.573 ms (5%) |           |   31.90 MiB (1%) |     1038898 |
| `["words", "nthreads=2"]`                           |  16.460 ms (5%) |           |   32.25 MiB (1%) |     1038967 |
| `["words", "nthreads=4"]`                           |  16.703 ms (5%) |           |   32.97 MiB (1%) |     1039110 |

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
Julia Version 1.5.3
Commit 788b2c77c1 (2020-11-09 13:37 UTC)
Platform Info:
  OS: Linux (x86_64-pc-linux-gnu)
      Ubuntu 18.04.5 LTS
  uname: Linux 5.4.0-1036-azure #38~18.04.1-Ubuntu SMP Wed Jan 6 18:26:30 UTC 2021 x86_64 x86_64
  CPU: Intel(R) Xeon(R) Platinum 8171M CPU @ 2.60GHz: 
              speed         user         nice          sys         idle          irq
       #1  2095 MHz      48764 s          0 s       2250 s      19181 s          0 s
       #2  2095 MHz      51747 s          0 s       2453 s      16139 s          0 s
       
  Memory: 6.791393280029297 GB (3655.63671875 MB free)
  Uptime: 720.0 sec
  Load Avg:  1.72119140625  1.4873046875  0.88427734375
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-9.0.1 (ORCJIT, skylake-avx512)
```

---
# Baseline result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmark: 18 Jan 2021 - 4:45
* Package commit: 8e896a
* Julia commit: 788b2c
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
| `["collect", "assoc", "basesize=1"]`                | 386.852 ms (5%) | 12.022 ms |   82.16 MiB (1%) |     1368059 |
| `["collect", "assoc", "basesize=1024"]`             | 241.688 ms (5%) |           |    1.83 MiB (1%) |        1597 |
| `["collect", "assoc", "basesize=32"]`               | 245.117 ms (5%) |           |    5.47 MiB (1%) |       47070 |
| `["collect", "seq"]`                                | 468.462 ms (5%) |           |  512.72 KiB (1%) |          15 |
| `["collect", "unordered", "basesize=1"]`            | 495.960 ms (5%) |           |   30.01 MiB (1%) |      360654 |
| `["collect", "unordered", "basesize=1024"]`         | 284.735 ms (5%) |           |  782.83 KiB (1%) |        1790 |
| `["collect", "unordered", "basesize=32"]`           | 266.192 ms (5%) |           |    1.46 MiB (1%) |       12188 |
| `["findfirst", "n=1000", "foldl"]`                  | 742.107 ms (5%) |           |                  |             |
| `["findfirst", "n=1000", "reduce", "basesize=128"]` | 378.574 ms (5%) |           |  546.33 KiB (1%) |        9561 |
| `["findfirst", "n=1000", "reduce", "basesize=256"]` | 384.407 ms (5%) |           |  278.28 KiB (1%) |        4889 |
| `["findfirst", "n=1000", "reduce", "basesize=512"]` | 381.744 ms (5%) |           |  144.64 KiB (1%) |        2549 |
| `["findfirst", "n=400", "foldl"]`                   | 558.842 ms (5%) |           |                  |             |
| `["findfirst", "n=400", "reduce", "basesize=128"]`  | 289.207 ms (5%) |           | 1012.86 KiB (1%) |       17725 |
| `["findfirst", "n=400", "reduce", "basesize=256"]`  | 288.475 ms (5%) |           |  509.63 KiB (1%) |        8952 |
| `["findfirst", "n=400", "reduce", "basesize=512"]`  | 285.046 ms (5%) |           |  258.83 KiB (1%) |        4563 |
| `["findfirst", "n=500", "foldl"]`                   |  97.021 ms (5%) |           |                  |             |
| `["findfirst", "n=500", "reduce", "basesize=128"]`  |  50.396 ms (5%) |           |  152.59 KiB (1%) |        2677 |
| `["findfirst", "n=500", "reduce", "basesize=256"]`  |  50.378 ms (5%) |           |   82.00 KiB (1%) |        1444 |
| `["findfirst", "n=500", "reduce", "basesize=512"]`  |  52.627 ms (5%) |           |   46.80 KiB (1%) |         826 |
| `["overhead", "default"]`                           | 166.307 μs (5%) |           |  140.72 KiB (1%) |        2464 |
| `["overhead", "stoppable=false"]`                   | 152.606 μs (5%) |           |  140.75 KiB (1%) |        2464 |
| `["overhead", "stoppable=true"]`                    | 317.313 μs (5%) |           |  140.78 KiB (1%) |        2465 |
| `["parallel_histogram", "assoc", "basesize=16384"]` |   5.150 ms (5%) |           |  731.81 KiB (1%) |          94 |
| `["parallel_histogram", "assoc", "basesize=4096"]`  |   6.166 ms (5%) |           |    2.07 MiB (1%) |         454 |
| `["parallel_histogram", "assoc", "basesize=8192"]`  |   5.675 ms (5%) |           |    1.43 MiB (1%) |         220 |
| `["parallel_histogram", "comm", "basesize=16384"]`  |  16.089 ms (5%) |           |    1.22 MiB (1%) |         160 |
| `["parallel_histogram", "comm", "basesize=4096"]`   |  23.416 ms (5%) |           |    1.03 MiB (1%) |        1920 |
| `["parallel_histogram", "comm", "basesize=8192"]`   |  20.005 ms (5%) |           |    1.25 MiB (1%) |        1100 |
| `["parallel_histogram", "seq"]`                     |   9.006 ms (5%) |           |  364.61 KiB (1%) |          24 |
| `["sum", "random", "foldl"]`                        |  19.073 ms (5%) |           |    32 bytes (1%) |           2 |
| `["sum", "random", "reduce", "basesize=128"]`       |   9.783 ms (5%) |           |  292.02 KiB (1%) |        5213 |
| `["sum", "random", "reduce", "basesize=256"]`       |   9.764 ms (5%) |           |  144.53 KiB (1%) |        2589 |
| `["sum", "random", "reduce", "basesize=512"]`       |   9.634 ms (5%) |           |   71.11 KiB (1%) |        1279 |
| `["sum", "uniform", "foldl"]`                       |  17.809 ms (5%) |           |    32 bytes (1%) |           2 |
| `["sum", "uniform", "reduce", "basesize=128"]`      |   9.751 ms (5%) |           |  292.02 KiB (1%) |        5213 |
| `["sum", "uniform", "reduce", "basesize=256"]`      |   9.385 ms (5%) |           |  144.53 KiB (1%) |        2589 |
| `["sum", "uniform", "reduce", "basesize=512"]`      |   9.203 ms (5%) |           |   71.06 KiB (1%) |        1278 |
| `["sum", "valley", "foldl"]`                        |  18.055 ms (5%) |           |    32 bytes (1%) |           2 |
| `["sum", "valley", "reduce", "basesize=128"]`       |   9.746 ms (5%) |           |  292.02 KiB (1%) |        5213 |
| `["sum", "valley", "reduce", "basesize=256"]`       |   9.742 ms (5%) |           |  144.53 KiB (1%) |        2589 |
| `["sum", "valley", "reduce", "basesize=512"]`       |   9.707 ms (5%) |           |   71.06 KiB (1%) |        1278 |
| `["words", "nthreads=1"]`                           |  25.388 ms (5%) |           |   31.63 MiB (1%) |     1030575 |
| `["words", "nthreads=2"]`                           |  16.414 ms (5%) |           |   32.34 MiB (1%) |     1030716 |
| `["words", "nthreads=4"]`                           |  16.506 ms (5%) |           |   32.80 MiB (1%) |     1030881 |

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
Julia Version 1.5.3
Commit 788b2c77c1 (2020-11-09 13:37 UTC)
Platform Info:
  OS: Linux (x86_64-pc-linux-gnu)
      Ubuntu 18.04.5 LTS
  uname: Linux 5.4.0-1036-azure #38~18.04.1-Ubuntu SMP Wed Jan 6 18:26:30 UTC 2021 x86_64 x86_64
  CPU: Intel(R) Xeon(R) Platinum 8171M CPU @ 2.60GHz: 
              speed         user         nice          sys         idle          irq
       #1  2095 MHz      71387 s          0 s       2800 s      24909 s          0 s
       #2  2095 MHz      73592 s          0 s       3072 s      22559 s          0 s
       
  Memory: 6.791393280029297 GB (3676.5 MB free)
  Uptime: 1010.0 sec
  Load Avg:  1.65576171875  1.587890625  1.09521484375
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-9.0.1 (ORCJIT, skylake-avx512)
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
    CPU MHz:             2095.193
    BogoMIPS:            4190.38
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
| Address Size       | 48 bits virtual, 46 bits physical                       |
| SIMD               | 512 bit = 64 byte max. SIMD vector size                 |
| Time Stamp Counter | TSC is accessible via `rdtsc`                           |
|                    | TSC increased at every clock cycle (non-invariant TSC)  |
| Perf. Monitoring   | Performance Monitoring Counters (PMC) are not supported |
| Hypervisor         | Yes, Microsoft                                          |

