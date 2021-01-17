# Multi-thread benchmark result

* Pull request commit: [`38ad3d6d2ee62aeda1754c8ce80f2a0bb2a73ab0`](https://github.com/JuliaFolds/Transducers.jl/commit/38ad3d6d2ee62aeda1754c8ce80f2a0bb2a73ab0)
* Pull request: <https://github.com/JuliaFolds/Transducers.jl/pull/444> (Add new transducer Consecutive(size, step))

# Judge result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmarks:
    - Target: 17 Jan 2021 - 00:37
    - Baseline: 17 Jan 2021 - 00:42
* Package commits:
    - Target: 310808
    - Baseline: dbdd4d
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

| ID                                                  | time ratio                   | memory ratio  |
|-----------------------------------------------------|------------------------------|---------------|
| `["collect", "assoc", "basesize=32"]`               | 0.95 (5%) :white_check_mark: |    1.00 (1%)  |
| `["collect", "unordered", "basesize=1"]`            |                1.06 (5%) :x: |    1.00 (1%)  |
| `["collect", "unordered", "basesize=1024"]`         |                   1.01 (5%)  | 1.04 (1%) :x: |
| `["collect", "unordered", "basesize=32"]`           | 0.94 (5%) :white_check_mark: |    1.00 (1%)  |
| `["findfirst", "n=1000", "foldl"]`                  | 0.88 (5%) :white_check_mark: |    1.00 (1%)  |
| `["findfirst", "n=1000", "reduce", "basesize=128"]` | 0.89 (5%) :white_check_mark: |    1.00 (1%)  |
| `["findfirst", "n=1000", "reduce", "basesize=256"]` | 0.83 (5%) :white_check_mark: |    1.00 (1%)  |
| `["findfirst", "n=1000", "reduce", "basesize=512"]` | 0.80 (5%) :white_check_mark: |    1.00 (1%)  |
| `["findfirst", "n=400", "foldl"]`                   | 0.80 (5%) :white_check_mark: |    1.00 (1%)  |
| `["findfirst", "n=400", "reduce", "basesize=128"]`  | 0.85 (5%) :white_check_mark: |    1.00 (1%)  |
| `["findfirst", "n=400", "reduce", "basesize=256"]`  | 0.85 (5%) :white_check_mark: |    1.00 (1%)  |
| `["findfirst", "n=400", "reduce", "basesize=512"]`  | 0.89 (5%) :white_check_mark: |    1.00 (1%)  |
| `["findfirst", "n=500", "foldl"]`                   | 0.85 (5%) :white_check_mark: |    1.00 (1%)  |
| `["findfirst", "n=500", "reduce", "basesize=128"]`  | 0.80 (5%) :white_check_mark: |    1.00 (1%)  |
| `["findfirst", "n=500", "reduce", "basesize=256"]`  | 0.88 (5%) :white_check_mark: |    1.00 (1%)  |
| `["findfirst", "n=500", "reduce", "basesize=512"]`  | 0.87 (5%) :white_check_mark: |    1.00 (1%)  |
| `["overhead", "default"]`                           | 0.88 (5%) :white_check_mark: |    1.00 (1%)  |
| `["overhead", "stoppable=false"]`                   | 0.90 (5%) :white_check_mark: |    1.00 (1%)  |
| `["overhead", "stoppable=true"]`                    |                1.07 (5%) :x: |    1.00 (1%)  |
| `["parallel_histogram", "comm", "basesize=4096"]`   | 0.95 (5%) :white_check_mark: |    0.99 (1%)  |
| `["parallel_histogram", "seq"]`                     |                1.16 (5%) :x: |    1.00 (1%)  |
| `["sum", "random", "foldl"]`                        | 0.85 (5%) :white_check_mark: |    1.00 (1%)  |
| `["sum", "random", "reduce", "basesize=128"]`       | 0.81 (5%) :white_check_mark: |    1.00 (1%)  |
| `["sum", "random", "reduce", "basesize=256"]`       | 0.86 (5%) :white_check_mark: |    1.00 (1%)  |
| `["sum", "random", "reduce", "basesize=512"]`       | 0.84 (5%) :white_check_mark: |    1.00 (1%)  |
| `["sum", "uniform", "foldl"]`                       | 0.84 (5%) :white_check_mark: |    1.00 (1%)  |
| `["sum", "uniform", "reduce", "basesize=128"]`      | 0.86 (5%) :white_check_mark: |    1.00 (1%)  |
| `["sum", "uniform", "reduce", "basesize=256"]`      | 0.85 (5%) :white_check_mark: |    1.00 (1%)  |
| `["sum", "uniform", "reduce", "basesize=512"]`      | 0.85 (5%) :white_check_mark: |    1.00 (1%)  |
| `["sum", "valley", "reduce", "basesize=128"]`       | 0.86 (5%) :white_check_mark: |    1.00 (1%)  |
| `["sum", "valley", "reduce", "basesize=256"]`       | 0.86 (5%) :white_check_mark: |    1.00 (1%)  |
| `["sum", "valley", "reduce", "basesize=512"]`       | 0.86 (5%) :white_check_mark: |    1.00 (1%)  |
| `["words", "nthreads=1"]`                           |                1.10 (5%) :x: |    1.00 (1%)  |
| `["words", "nthreads=2"]`                           |                1.06 (5%) :x: |    1.00 (1%)  |
| `["words", "nthreads=4"]`                           |                1.07 (5%) :x: |    1.00 (1%)  |

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
       #1  2095 MHz      49742 s          0 s       2414 s      15266 s          0 s
       #2  2095 MHz      47664 s          0 s       2418 s      17316 s          0 s
       
  Memory: 6.791393280029297 GB (3738.46484375 MB free)
  Uptime: 691.0 sec
  Load Avg:  1.65380859375  1.50927734375  0.91455078125
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
       #1  2095 MHz      72101 s          0 s       3002 s      20464 s          0 s
       #2  2095 MHz      69006 s          0 s       2961 s      23648 s          0 s
       
  Memory: 6.791393280029297 GB (3762.82421875 MB free)
  Uptime: 974.0 sec
  Load Avg:  1.6630859375  1.54443359375  1.08447265625
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-9.0.1 (ORCJIT, skylake-avx512)
```

---
# Target result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmark: 17 Jan 2021 - 0:37
* Package commit: 310808
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
| `["collect", "assoc", "basesize=1"]`                | 317.374 ms (5%) | 12.839 ms |   82.16 MiB (1%) |     1368057 |
| `["collect", "assoc", "basesize=1024"]`             | 202.028 ms (5%) |           |    1.83 MiB (1%) |        1596 |
| `["collect", "assoc", "basesize=32"]`               | 204.775 ms (5%) |           |    5.47 MiB (1%) |       47069 |
| `["collect", "seq"]`                                | 364.068 ms (5%) |           |  512.72 KiB (1%) |          15 |
| `["collect", "unordered", "basesize=1"]`            | 473.172 ms (5%) |           |   30.01 MiB (1%) |      360579 |
| `["collect", "unordered", "basesize=1024"]`         | 250.142 ms (5%) |           |  796.02 KiB (1%) |        2212 |
| `["collect", "unordered", "basesize=32"]`           | 226.575 ms (5%) |           |    1.47 MiB (1%) |       12374 |
| `["findfirst", "n=1000", "foldl"]`                  | 572.836 ms (5%) |           |                  |             |
| `["findfirst", "n=1000", "reduce", "basesize=128"]` | 314.435 ms (5%) |           |  546.33 KiB (1%) |        9561 |
| `["findfirst", "n=1000", "reduce", "basesize=256"]` | 292.555 ms (5%) |           |  278.25 KiB (1%) |        4888 |
| `["findfirst", "n=1000", "reduce", "basesize=512"]` | 293.212 ms (5%) |           |  144.66 KiB (1%) |        2550 |
| `["findfirst", "n=400", "foldl"]`                   | 436.042 ms (5%) |           |                  |             |
| `["findfirst", "n=400", "reduce", "basesize=128"]`  | 217.300 ms (5%) |           | 1012.91 KiB (1%) |       17727 |
| `["findfirst", "n=400", "reduce", "basesize=256"]`  | 220.570 ms (5%) |           |  509.66 KiB (1%) |        8953 |
| `["findfirst", "n=400", "reduce", "basesize=512"]`  | 241.827 ms (5%) |           |  258.84 KiB (1%) |        4564 |
| `["findfirst", "n=500", "foldl"]`                   |  73.874 ms (5%) |           |                  |             |
| `["findfirst", "n=500", "reduce", "basesize=128"]`  |  37.257 ms (5%) |           |  152.59 KiB (1%) |        2677 |
| `["findfirst", "n=500", "reduce", "basesize=256"]`  |  38.431 ms (5%) |           |   82.00 KiB (1%) |        1444 |
| `["findfirst", "n=500", "reduce", "basesize=512"]`  |  39.907 ms (5%) |           |   46.83 KiB (1%) |         827 |
| `["overhead", "default"]`                           | 131.301 μs (5%) |           |  140.75 KiB (1%) |        2465 |
| `["overhead", "stoppable=false"]`                   | 130.701 μs (5%) |           |  140.78 KiB (1%) |        2465 |
| `["overhead", "stoppable=true"]`                    | 324.502 μs (5%) |           |  140.78 KiB (1%) |        2465 |
| `["parallel_histogram", "assoc", "basesize=16384"]` |   4.366 ms (5%) |           |  731.81 KiB (1%) |          94 |
| `["parallel_histogram", "assoc", "basesize=4096"]`  |   4.954 ms (5%) |           |    1.80 MiB (1%) |         448 |
| `["parallel_histogram", "assoc", "basesize=8192"]`  |   4.665 ms (5%) |           |    1.43 MiB (1%) |         220 |
| `["parallel_histogram", "comm", "basesize=16384"]`  |  14.930 ms (5%) |           |    1.22 MiB (1%) |         211 |
| `["parallel_histogram", "comm", "basesize=4096"]`   |  23.688 ms (5%) |           |    1.05 MiB (1%) |        1682 |
| `["parallel_histogram", "comm", "basesize=8192"]`   |  19.978 ms (5%) |           |    1.26 MiB (1%) |        1441 |
| `["parallel_histogram", "seq"]`                     |   8.147 ms (5%) |           |  364.61 KiB (1%) |          24 |
| `["sum", "random", "foldl"]`                        |  14.133 ms (5%) |           |    32 bytes (1%) |           2 |
| `["sum", "random", "reduce", "basesize=128"]`       |   6.902 ms (5%) |           |  292.02 KiB (1%) |        5213 |
| `["sum", "random", "reduce", "basesize=256"]`       |   6.790 ms (5%) |           |  144.53 KiB (1%) |        2589 |
| `["sum", "random", "reduce", "basesize=512"]`       |   6.699 ms (5%) |           |   71.11 KiB (1%) |        1279 |
| `["sum", "uniform", "foldl"]`                       |  12.881 ms (5%) |           |    32 bytes (1%) |           2 |
| `["sum", "uniform", "reduce", "basesize=128"]`      |   6.733 ms (5%) |           |  292.02 KiB (1%) |        5213 |
| `["sum", "uniform", "reduce", "basesize=256"]`      |   6.606 ms (5%) |           |  144.53 KiB (1%) |        2589 |
| `["sum", "uniform", "reduce", "basesize=512"]`      |   6.505 ms (5%) |           |   71.06 KiB (1%) |        1278 |
| `["sum", "valley", "foldl"]`                        |  13.323 ms (5%) |           |    32 bytes (1%) |           2 |
| `["sum", "valley", "reduce", "basesize=128"]`       |   7.029 ms (5%) |           |  292.02 KiB (1%) |        5213 |
| `["sum", "valley", "reduce", "basesize=256"]`       |   6.890 ms (5%) |           |  144.53 KiB (1%) |        2589 |
| `["sum", "valley", "reduce", "basesize=512"]`       |   6.825 ms (5%) |           |   71.06 KiB (1%) |        1278 |
| `["words", "nthreads=1"]`                           |  22.960 ms (5%) |           |   31.75 MiB (1%) |     1034363 |
| `["words", "nthreads=2"]`                           |  15.032 ms (5%) |           |   32.47 MiB (1%) |     1034511 |
| `["words", "nthreads=4"]`                           |  16.142 ms (5%) |           |   32.92 MiB (1%) |     1034653 |

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
       #1  2095 MHz      49742 s          0 s       2414 s      15266 s          0 s
       #2  2095 MHz      47664 s          0 s       2418 s      17316 s          0 s
       
  Memory: 6.791393280029297 GB (3738.46484375 MB free)
  Uptime: 691.0 sec
  Load Avg:  1.65380859375  1.50927734375  0.91455078125
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-9.0.1 (ORCJIT, skylake-avx512)
```

---
# Baseline result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmark: 17 Jan 2021 - 0:42
* Package commit: dbdd4d
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
| `["collect", "assoc", "basesize=1"]`                | 320.665 ms (5%) | 10.078 ms |   82.16 MiB (1%) |     1368051 |
| `["collect", "assoc", "basesize=1024"]`             | 208.906 ms (5%) |           |    1.83 MiB (1%) |        1596 |
| `["collect", "assoc", "basesize=32"]`               | 216.521 ms (5%) |           |    5.47 MiB (1%) |       47069 |
| `["collect", "seq"]`                                | 374.771 ms (5%) |           |  512.72 KiB (1%) |          15 |
| `["collect", "unordered", "basesize=1"]`            | 447.593 ms (5%) |           |   30.01 MiB (1%) |      360566 |
| `["collect", "unordered", "basesize=1024"]`         | 247.478 ms (5%) |           |  766.73 KiB (1%) |        1257 |
| `["collect", "unordered", "basesize=32"]`           | 240.904 ms (5%) |           |    1.47 MiB (1%) |       12428 |
| `["findfirst", "n=1000", "foldl"]`                  | 654.622 ms (5%) |           |                  |             |
| `["findfirst", "n=1000", "reduce", "basesize=128"]` | 354.844 ms (5%) |           |  546.34 KiB (1%) |        9562 |
| `["findfirst", "n=1000", "reduce", "basesize=256"]` | 351.630 ms (5%) |           |  278.25 KiB (1%) |        4888 |
| `["findfirst", "n=1000", "reduce", "basesize=512"]` | 364.853 ms (5%) |           |  144.69 KiB (1%) |        2551 |
| `["findfirst", "n=400", "foldl"]`                   | 543.788 ms (5%) |           |                  |             |
| `["findfirst", "n=400", "reduce", "basesize=128"]`  | 256.285 ms (5%) |           | 1012.86 KiB (1%) |       17725 |
| `["findfirst", "n=400", "reduce", "basesize=256"]`  | 258.665 ms (5%) |           |  509.63 KiB (1%) |        8952 |
| `["findfirst", "n=400", "reduce", "basesize=512"]`  | 270.622 ms (5%) |           |  258.83 KiB (1%) |        4563 |
| `["findfirst", "n=500", "foldl"]`                   |  87.044 ms (5%) |           |                  |             |
| `["findfirst", "n=500", "reduce", "basesize=128"]`  |  46.803 ms (5%) |           |  152.59 KiB (1%) |        2677 |
| `["findfirst", "n=500", "reduce", "basesize=256"]`  |  43.890 ms (5%) |           |   82.00 KiB (1%) |        1444 |
| `["findfirst", "n=500", "reduce", "basesize=512"]`  |  45.931 ms (5%) |           |   46.84 KiB (1%) |         828 |
| `["overhead", "default"]`                           | 148.700 μs (5%) |           |  140.72 KiB (1%) |        2464 |
| `["overhead", "stoppable=false"]`                   | 144.801 μs (5%) |           |  140.75 KiB (1%) |        2464 |
| `["overhead", "stoppable=true"]`                    | 303.101 μs (5%) |           |  140.78 KiB (1%) |        2465 |
| `["parallel_histogram", "assoc", "basesize=16384"]` |   4.292 ms (5%) |           |  731.81 KiB (1%) |          94 |
| `["parallel_histogram", "assoc", "basesize=4096"]`  |   5.066 ms (5%) |           |    1.80 MiB (1%) |         448 |
| `["parallel_histogram", "assoc", "basesize=8192"]`  |   4.593 ms (5%) |           |    1.43 MiB (1%) |         220 |
| `["parallel_histogram", "comm", "basesize=16384"]`  |  14.578 ms (5%) |           |    1.22 MiB (1%) |         225 |
| `["parallel_histogram", "comm", "basesize=4096"]`   |  24.935 ms (5%) |           |    1.06 MiB (1%) |        1713 |
| `["parallel_histogram", "comm", "basesize=8192"]`   |  19.887 ms (5%) |           |    1.25 MiB (1%) |        1057 |
| `["parallel_histogram", "seq"]`                     |   7.003 ms (5%) |           |  364.61 KiB (1%) |          24 |
| `["sum", "random", "foldl"]`                        |  16.548 ms (5%) |           |    32 bytes (1%) |           2 |
| `["sum", "random", "reduce", "basesize=128"]`       |   8.482 ms (5%) |           |  292.02 KiB (1%) |        5213 |
| `["sum", "random", "reduce", "basesize=256"]`       |   7.907 ms (5%) |           |  144.53 KiB (1%) |        2589 |
| `["sum", "random", "reduce", "basesize=512"]`       |   8.019 ms (5%) |           |   71.14 KiB (1%) |        1280 |
| `["sum", "uniform", "foldl"]`                       |  15.306 ms (5%) |           |    32 bytes (1%) |           2 |
| `["sum", "uniform", "reduce", "basesize=128"]`      |   7.868 ms (5%) |           |  292.02 KiB (1%) |        5213 |
| `["sum", "uniform", "reduce", "basesize=256"]`      |   7.743 ms (5%) |           |  144.56 KiB (1%) |        2590 |
| `["sum", "uniform", "reduce", "basesize=512"]`      |   7.629 ms (5%) |           |   71.06 KiB (1%) |        1278 |
| `["sum", "valley", "foldl"]`                        |  13.790 ms (5%) |           |    32 bytes (1%) |           2 |
| `["sum", "valley", "reduce", "basesize=128"]`       |   8.160 ms (5%) |           |  292.02 KiB (1%) |        5213 |
| `["sum", "valley", "reduce", "basesize=256"]`       |   7.985 ms (5%) |           |  144.53 KiB (1%) |        2589 |
| `["sum", "valley", "reduce", "basesize=512"]`       |   7.947 ms (5%) |           |   71.06 KiB (1%) |        1278 |
| `["words", "nthreads=1"]`                           |  20.819 ms (5%) |           |   31.77 MiB (1%) |     1035071 |
| `["words", "nthreads=2"]`                           |  14.129 ms (5%) |           |   32.49 MiB (1%) |     1035215 |
| `["words", "nthreads=4"]`                           |  15.142 ms (5%) |           |   32.94 MiB (1%) |     1035347 |

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
       #1  2095 MHz      72101 s          0 s       3002 s      20464 s          0 s
       #2  2095 MHz      69006 s          0 s       2961 s      23648 s          0 s
       
  Memory: 6.791393280029297 GB (3762.82421875 MB free)
  Uptime: 974.0 sec
  Load Avg:  1.6630859375  1.54443359375  1.08447265625
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
    CPU MHz:             2095.076
    BogoMIPS:            4190.15
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

