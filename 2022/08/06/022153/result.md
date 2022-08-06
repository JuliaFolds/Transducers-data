# Multi-thread benchmark result

* Pull request commit: [`ac17a66928ed2fa15ae35d47d34db6c384bd8a87`](https://github.com/JuliaFolds/Transducers.jl/commit/ac17a66928ed2fa15ae35d47d34db6c384bd8a87)
* Pull request: <https://github.com/JuliaFolds/Transducers.jl/pull/243> (Update */Manifest.toml)

# Judge result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmarks:
    - Target: 6 Aug 2022 - 02:15
    - Baseline: 6 Aug 2022 - 02:21
* Package commits:
    - Target: 3ee3bb
    - Baseline: 6125fe
* Julia commits:
    - Target: 742b9a
    - Baseline: 742b9a
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
| `["collect", "unordered", "basesize=1"]`            |                   0.99 (5%)  |                1.02 (1%) :x: |
| `["findfirst", "n=1000", "reduce", "basesize=128"]` | 0.78 (5%) :white_check_mark: | 0.79 (1%) :white_check_mark: |
| `["findfirst", "n=1000", "reduce", "basesize=256"]` | 0.92 (5%) :white_check_mark: | 0.93 (1%) :white_check_mark: |
| `["findfirst", "n=1000", "reduce", "basesize=512"]` | 0.79 (5%) :white_check_mark: | 0.88 (1%) :white_check_mark: |
| `["findfirst", "n=400", "foldl"]`                   |                1.06 (5%) :x: |                   1.00 (1%)  |
| `["findfirst", "n=400", "reduce", "basesize=128"]`  |                1.08 (5%) :x: |                1.01 (1%) :x: |
| `["findfirst", "n=400", "reduce", "basesize=256"]`  |                1.15 (5%) :x: |                1.08 (1%) :x: |
| `["findfirst", "n=400", "reduce", "basesize=512"]`  |                   1.04 (5%)  | 0.95 (1%) :white_check_mark: |
| `["findfirst", "n=500", "reduce", "basesize=128"]`  | 0.80 (5%) :white_check_mark: | 0.84 (1%) :white_check_mark: |
| `["findfirst", "n=500", "reduce", "basesize=256"]`  |                1.40 (5%) :x: |                1.28 (1%) :x: |
| `["findfirst", "n=500", "reduce", "basesize=512"]`  |                1.21 (5%) :x: | 0.93 (1%) :white_check_mark: |
| `["overhead", "stoppable=true"]`                    | 0.94 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["parallel_histogram", "comm", "basesize=16384"]`  |                   1.01 (5%)  | 0.98 (1%) :white_check_mark: |
| `["parallel_histogram", "comm", "basesize=4096"]`   |                1.12 (5%) :x: |                1.09 (1%) :x: |
| `["parallel_histogram", "comm", "basesize=8192"]`   |                   1.04 (5%)  |                1.03 (1%) :x: |
| `["partition_length_maximum", "rand", "reduce"]`    |                1.06 (5%) :x: | 0.96 (1%) :white_check_mark: |
| `["words", "nthreads=4"]`                           | 0.94 (5%) :white_check_mark: |                   1.00 (1%)  |

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
- `["partition_length_maximum", "rand"]`
- `["splitby", "count"]`
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
Julia Version 1.7.3
Commit 742b9abb4d (2022-05-06 12:58 UTC)
Platform Info:
  OS: Linux (x86_64-pc-linux-gnu)
      Ubuntu 20.04.4 LTS
  uname: Linux 5.15.0-1014-azure #17~20.04.1-Ubuntu SMP Thu Jun 23 20:01:51 UTC 2022 x86_64 x86_64
  CPU: Intel(R) Xeon(R) CPU E5-2673 v4 @ 2.30GHz: 
              speed         user         nice          sys         idle          irq
       #1  2294 MHz       4437 s          2 s        232 s       4601 s          0 s
       #2  2294 MHz       6191 s          2 s        264 s       2831 s          0 s
       
  Memory: 6.780967712402344 GB (3712.453125 MB free)
  Uptime: 934.13 sec
  Load Avg:  1.64  1.47  0.88
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-12.0.1 (ORCJIT, broadwell)
```

### Baseline
```
Julia Version 1.7.3
Commit 742b9abb4d (2022-05-06 12:58 UTC)
Platform Info:
  OS: Linux (x86_64-pc-linux-gnu)
      Ubuntu 20.04.4 LTS
  uname: Linux 5.15.0-1014-azure #17~20.04.1-Ubuntu SMP Thu Jun 23 20:01:51 UTC 2022 x86_64 x86_64
  CPU: Intel(R) Xeon(R) CPU E5-2673 v4 @ 2.30GHz: 
              speed         user         nice          sys         idle          irq
       #1  2294 MHz       7030 s          2 s        323 s       5198 s          0 s
       #2  2294 MHz       8464 s          2 s        376 s       3724 s          0 s
       
  Memory: 6.780967712402344 GB (3641.8046875 MB free)
  Uptime: 1262.94 sec
  Load Avg:  2.12  1.84  1.22
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-12.0.1 (ORCJIT, broadwell)
```

---
# Target result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmark: 6 Aug 2022 - 2:15
* Package commit: 3ee3bb
* Julia commit: 742b9a
* Julia command flags: None
* Environment variables: `JULIA_NUM_THREADS => 2`

## Results
Below is a table of this job's results, obtained by running the benchmarks.
The values listed in the `ID` column have the structure `[parent_group, child_group, ..., key]`, and can be used to
index into the BaseBenchmarks suite to retrieve the corresponding benchmarks.
The percentages accompanying time and memory values in the below table are noise tolerances. The "true"
time/memory value for a given benchmark is expected to fall within this percentage of the reported value.
An empty cell means that the value was zero.

| ID                                                  | time            | GC time | memory          | allocations |
|-----------------------------------------------------|----------------:|--------:|----------------:|------------:|
| `["collect", "assoc", "basesize=1"]`                | 226.728 ms (5%) |         |  25.97 MiB (1%) |      306811 |
| `["collect", "assoc", "basesize=1024"]`             | 168.243 ms (5%) |         |   2.61 MiB (1%) |         455 |
| `["collect", "assoc", "basesize=32"]`               | 172.924 ms (5%) |         |   4.82 MiB (1%) |       11714 |
| `["collect", "seq"]`                                | 337.308 ms (5%) |         | 812.73 KiB (1%) |          11 |
| `["collect", "unordered", "basesize=1"]`            | 358.487 ms (5%) |         |  23.93 MiB (1%) |      413926 |
| `["collect", "unordered", "basesize=1024"]`         | 188.354 ms (5%) |         |   1.03 MiB (1%) |        1617 |
| `["collect", "unordered", "basesize=32"]`           | 201.343 ms (5%) |         |   1.59 MiB (1%) |       15011 |
| `["findfirst", "n=1000", "foldl"]`                  | 554.419 ms (5%) |         |                 |             |
| `["findfirst", "n=1000", "reduce", "basesize=128"]` | 437.285 ms (5%) |         | 305.59 KiB (1%) |        4295 |
| `["findfirst", "n=1000", "reduce", "basesize=256"]` | 397.428 ms (5%) |         | 157.20 KiB (1%) |        2193 |
| `["findfirst", "n=1000", "reduce", "basesize=512"]` | 519.400 ms (5%) |         | 107.98 KiB (1%) |        1507 |
| `["findfirst", "n=400", "foldl"]`                   | 420.882 ms (5%) |         |                 |             |
| `["findfirst", "n=400", "reduce", "basesize=128"]`  | 223.033 ms (5%) |         | 378.30 KiB (1%) |        5394 |
| `["findfirst", "n=400", "reduce", "basesize=256"]`  | 247.011 ms (5%) |         | 214.41 KiB (1%) |        3057 |
| `["findfirst", "n=400", "reduce", "basesize=512"]`  | 315.411 ms (5%) |         | 138.05 KiB (1%) |        1987 |
| `["findfirst", "n=500", "foldl"]`                   |  68.781 ms (5%) |         |                 |             |
| `["findfirst", "n=500", "reduce", "basesize=128"]`  | 142.702 ms (5%) |         | 226.88 KiB (1%) |        3174 |
| `["findfirst", "n=500", "reduce", "basesize=256"]`  | 114.597 ms (5%) |         | 106.47 KiB (1%) |        1451 |
| `["findfirst", "n=500", "reduce", "basesize=512"]`  | 115.875 ms (5%) |         |  55.95 KiB (1%) |         765 |
| `["overhead", "default"]`                           |  74.701 μs (5%) |         |  32.77 KiB (1%) |         419 |
| `["overhead", "stoppable=false"]`                   |  74.300 μs (5%) |         |  32.78 KiB (1%) |         419 |
| `["overhead", "stoppable=true"]`                    |  87.100 μs (5%) |         |  44.25 KiB (1%) |         610 |
| `["parallel_histogram", "assoc", "basesize=16384"]` |   2.725 ms (5%) |         | 728.91 KiB (1%) |          57 |
| `["parallel_histogram", "assoc", "basesize=4096"]`  |   3.400 ms (5%) |         |   1.79 MiB (1%) |         215 |
| `["parallel_histogram", "assoc", "basesize=8192"]`  |   2.994 ms (5%) |         |   1.42 MiB (1%) |         117 |
| `["parallel_histogram", "comm", "basesize=16384"]`  |  19.756 ms (5%) |         |   1.61 MiB (1%) |        3567 |
| `["parallel_histogram", "comm", "basesize=4096"]`   |  25.193 ms (5%) |         |   1.29 MiB (1%) |        8314 |
| `["parallel_histogram", "comm", "basesize=8192"]`   |  22.519 ms (5%) |         |   1.26 MiB (1%) |        5587 |
| `["parallel_histogram", "seq"]`                     |   4.523 ms (5%) |         | 364.16 KiB (1%) |          24 |
| `["partition_length_maximum", "rand", "foldl"]`     |  36.093 ms (5%) |         |                 |             |
| `["partition_length_maximum", "rand", "reduce"]`    |  18.341 ms (5%) |         |  704 bytes (1%) |          10 |
| `["splitby", "count", "foldl"]`                     |   1.694 ms (5%) |         |                 |             |
| `["splitby", "count", "man"]`                       |   1.295 ms (5%) |         |                 |             |
| `["splitby", "count", "reduce"]`                    | 838.803 μs (5%) |         |   1.06 KiB (1%) |          19 |
| `["sum", "random", "foldl"]`                        |  12.914 ms (5%) |         |                 |             |
| `["sum", "random", "reduce", "basesize=128"]`       |   6.632 ms (5%) |         |  74.20 KiB (1%) |        1105 |
| `["sum", "random", "reduce", "basesize=256"]`       |   6.500 ms (5%) |         |  36.70 KiB (1%) |         545 |
| `["sum", "random", "reduce", "basesize=512"]`       |   6.433 ms (5%) |         |  18.11 KiB (1%) |         270 |
| `["sum", "uniform", "foldl"]`                       |  12.355 ms (5%) |         |                 |             |
| `["sum", "uniform", "reduce", "basesize=128"]`      |   6.451 ms (5%) |         |  74.17 KiB (1%) |        1104 |
| `["sum", "uniform", "reduce", "basesize=256"]`      |   6.385 ms (5%) |         |  36.67 KiB (1%) |         544 |
| `["sum", "uniform", "reduce", "basesize=512"]`      |   6.230 ms (5%) |         |  18.03 KiB (1%) |         268 |
| `["sum", "valley", "foldl"]`                        |  12.760 ms (5%) |         |                 |             |
| `["sum", "valley", "reduce", "basesize=128"]`       |   6.755 ms (5%) |         |  74.08 KiB (1%) |        1101 |
| `["sum", "valley", "reduce", "basesize=256"]`       |   6.553 ms (5%) |         |  36.67 KiB (1%) |         544 |
| `["sum", "valley", "reduce", "basesize=512"]`       |   6.416 ms (5%) |         |  17.97 KiB (1%) |         266 |
| `["words", "nthreads=1"]`                           |  26.306 ms (5%) |         |  31.53 MiB (1%) |     1026790 |
| `["words", "nthreads=2"]`                           |  16.383 ms (5%) |         |  31.89 MiB (1%) |     1026826 |
| `["words", "nthreads=4"]`                           |  15.740 ms (5%) |         |  32.78 MiB (1%) |     1026986 |

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
- `["partition_length_maximum", "rand"]`
- `["splitby", "count"]`
- `["sum", "random"]`
- `["sum", "random", "reduce"]`
- `["sum", "uniform"]`
- `["sum", "uniform", "reduce"]`
- `["sum", "valley"]`
- `["sum", "valley", "reduce"]`
- `["words"]`

## Julia versioninfo
```
Julia Version 1.7.3
Commit 742b9abb4d (2022-05-06 12:58 UTC)
Platform Info:
  OS: Linux (x86_64-pc-linux-gnu)
      Ubuntu 20.04.4 LTS
  uname: Linux 5.15.0-1014-azure #17~20.04.1-Ubuntu SMP Thu Jun 23 20:01:51 UTC 2022 x86_64 x86_64
  CPU: Intel(R) Xeon(R) CPU E5-2673 v4 @ 2.30GHz: 
              speed         user         nice          sys         idle          irq
       #1  2294 MHz       4437 s          2 s        232 s       4601 s          0 s
       #2  2294 MHz       6191 s          2 s        264 s       2831 s          0 s
       
  Memory: 6.780967712402344 GB (3712.453125 MB free)
  Uptime: 934.13 sec
  Load Avg:  1.64  1.47  0.88
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-12.0.1 (ORCJIT, broadwell)
```

---
# Baseline result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmark: 6 Aug 2022 - 2:21
* Package commit: 6125fe
* Julia commit: 742b9a
* Julia command flags: None
* Environment variables: `JULIA_NUM_THREADS => 2`

## Results
Below is a table of this job's results, obtained by running the benchmarks.
The values listed in the `ID` column have the structure `[parent_group, child_group, ..., key]`, and can be used to
index into the BaseBenchmarks suite to retrieve the corresponding benchmarks.
The percentages accompanying time and memory values in the below table are noise tolerances. The "true"
time/memory value for a given benchmark is expected to fall within this percentage of the reported value.
An empty cell means that the value was zero.

| ID                                                  | time            | GC time | memory          | allocations |
|-----------------------------------------------------|----------------:|--------:|----------------:|------------:|
| `["collect", "assoc", "basesize=1"]`                | 233.993 ms (5%) |         |  25.97 MiB (1%) |      306746 |
| `["collect", "assoc", "basesize=1024"]`             | 169.920 ms (5%) |         |   2.61 MiB (1%) |         456 |
| `["collect", "assoc", "basesize=32"]`               | 173.889 ms (5%) |         |   4.82 MiB (1%) |       11703 |
| `["collect", "seq"]`                                | 326.290 ms (5%) |         | 812.73 KiB (1%) |          11 |
| `["collect", "unordered", "basesize=1"]`            | 361.163 ms (5%) |         |  23.53 MiB (1%) |      400784 |
| `["collect", "unordered", "basesize=1024"]`         | 193.153 ms (5%) |         |   1.02 MiB (1%) |        1378 |
| `["collect", "unordered", "basesize=32"]`           | 198.259 ms (5%) |         |   1.60 MiB (1%) |       15170 |
| `["findfirst", "n=1000", "foldl"]`                  | 537.556 ms (5%) |         |                 |             |
| `["findfirst", "n=1000", "reduce", "basesize=128"]` | 563.414 ms (5%) |         | 389.19 KiB (1%) |        5475 |
| `["findfirst", "n=1000", "reduce", "basesize=256"]` | 433.985 ms (5%) |         | 168.84 KiB (1%) |        2360 |
| `["findfirst", "n=1000", "reduce", "basesize=512"]` | 655.859 ms (5%) |         | 122.91 KiB (1%) |        1737 |
| `["findfirst", "n=400", "foldl"]`                   | 398.527 ms (5%) |         |                 |             |
| `["findfirst", "n=400", "reduce", "basesize=128"]`  | 206.096 ms (5%) |         | 373.97 KiB (1%) |        5343 |
| `["findfirst", "n=400", "reduce", "basesize=256"]`  | 215.141 ms (5%) |         | 198.75 KiB (1%) |        2854 |
| `["findfirst", "n=400", "reduce", "basesize=512"]`  | 302.868 ms (5%) |         | 144.70 KiB (1%) |        2057 |
| `["findfirst", "n=500", "foldl"]`                   |  67.664 ms (5%) |         |                 |             |
| `["findfirst", "n=500", "reduce", "basesize=128"]`  | 178.643 ms (5%) |         | 268.77 KiB (1%) |        3737 |
| `["findfirst", "n=500", "reduce", "basesize=256"]`  |  81.941 ms (5%) |         |  83.50 KiB (1%) |        1137 |
| `["findfirst", "n=500", "reduce", "basesize=512"]`  |  95.886 ms (5%) |         |  60.39 KiB (1%) |         820 |
| `["overhead", "default"]`                           |  76.300 μs (5%) |         |  32.73 KiB (1%) |         418 |
| `["overhead", "stoppable=false"]`                   |  75.900 μs (5%) |         |  32.75 KiB (1%) |         418 |
| `["overhead", "stoppable=true"]`                    |  92.301 μs (5%) |         |  44.25 KiB (1%) |         610 |
| `["parallel_histogram", "assoc", "basesize=16384"]` |   2.617 ms (5%) |         | 728.91 KiB (1%) |          57 |
| `["parallel_histogram", "assoc", "basesize=4096"]`  |   3.311 ms (5%) |         |   1.79 MiB (1%) |         215 |
| `["parallel_histogram", "assoc", "basesize=8192"]`  |   2.998 ms (5%) |         |   1.42 MiB (1%) |         117 |
| `["parallel_histogram", "comm", "basesize=16384"]`  |  19.567 ms (5%) |         |   1.64 MiB (1%) |        4444 |
| `["parallel_histogram", "comm", "basesize=4096"]`   |  22.425 ms (5%) |         |   1.18 MiB (1%) |        4668 |
| `["parallel_histogram", "comm", "basesize=8192"]`   |  21.725 ms (5%) |         |   1.22 MiB (1%) |        6268 |
| `["parallel_histogram", "seq"]`                     |   4.506 ms (5%) |         | 364.16 KiB (1%) |          24 |
| `["partition_length_maximum", "rand", "foldl"]`     |  34.531 ms (5%) |         |                 |             |
| `["partition_length_maximum", "rand", "reduce"]`    |  17.382 ms (5%) |         |  736 bytes (1%) |          11 |
| `["splitby", "count", "foldl"]`                     |   1.759 ms (5%) |         |                 |             |
| `["splitby", "count", "man"]`                       |   1.295 ms (5%) |         |                 |             |
| `["splitby", "count", "reduce"]`                    | 820.404 μs (5%) |         |   1.06 KiB (1%) |          18 |
| `["sum", "random", "foldl"]`                        |  12.801 ms (5%) |         |                 |             |
| `["sum", "random", "reduce", "basesize=128"]`       |   6.610 ms (5%) |         |  74.23 KiB (1%) |        1106 |
| `["sum", "random", "reduce", "basesize=256"]`       |   6.628 ms (5%) |         |  36.77 KiB (1%) |         547 |
| `["sum", "random", "reduce", "basesize=512"]`       |   6.451 ms (5%) |         |  18.05 KiB (1%) |         268 |
| `["sum", "uniform", "foldl"]`                       |  12.389 ms (5%) |         |                 |             |
| `["sum", "uniform", "reduce", "basesize=128"]`      |   6.558 ms (5%) |         |  74.14 KiB (1%) |        1103 |
| `["sum", "uniform", "reduce", "basesize=256"]`      |   6.232 ms (5%) |         |  36.70 KiB (1%) |         545 |
| `["sum", "uniform", "reduce", "basesize=512"]`      |   6.102 ms (5%) |         |  18.00 KiB (1%) |         267 |
| `["sum", "valley", "foldl"]`                        |  12.923 ms (5%) |         |                 |             |
| `["sum", "valley", "reduce", "basesize=128"]`       |   6.795 ms (5%) |         |  74.11 KiB (1%) |        1102 |
| `["sum", "valley", "reduce", "basesize=256"]`       |   6.616 ms (5%) |         |  36.70 KiB (1%) |         545 |
| `["sum", "valley", "reduce", "basesize=512"]`       |   6.532 ms (5%) |         |  18.00 KiB (1%) |         267 |
| `["words", "nthreads=1"]`                           |  26.779 ms (5%) |         |  31.60 MiB (1%) |     1029328 |
| `["words", "nthreads=2"]`                           |  16.760 ms (5%) |         |  31.95 MiB (1%) |     1029376 |
| `["words", "nthreads=4"]`                           |  16.709 ms (5%) |         |  32.85 MiB (1%) |     1029554 |

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
- `["partition_length_maximum", "rand"]`
- `["splitby", "count"]`
- `["sum", "random"]`
- `["sum", "random", "reduce"]`
- `["sum", "uniform"]`
- `["sum", "uniform", "reduce"]`
- `["sum", "valley"]`
- `["sum", "valley", "reduce"]`
- `["words"]`

## Julia versioninfo
```
Julia Version 1.7.3
Commit 742b9abb4d (2022-05-06 12:58 UTC)
Platform Info:
  OS: Linux (x86_64-pc-linux-gnu)
      Ubuntu 20.04.4 LTS
  uname: Linux 5.15.0-1014-azure #17~20.04.1-Ubuntu SMP Thu Jun 23 20:01:51 UTC 2022 x86_64 x86_64
  CPU: Intel(R) Xeon(R) CPU E5-2673 v4 @ 2.30GHz: 
              speed         user         nice          sys         idle          irq
       #1  2294 MHz       7030 s          2 s        323 s       5198 s          0 s
       #2  2294 MHz       8464 s          2 s        376 s       3724 s          0 s
       
  Memory: 6.780967712402344 GB (3641.8046875 MB free)
  Uptime: 1262.94 sec
  Load Avg:  2.12  1.84  1.22
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-12.0.1 (ORCJIT, broadwell)
```

---
# Runtime information
| Runtime Info | |
|:--|:--|
| BLAS #threads | 2 |
| `BLAS.vendor()` | `openblas64` |
| `Sys.CPU_THREADS` | 2 |

`lscpu` output:

    Architecture:                    x86_64
    CPU op-mode(s):                  32-bit, 64-bit
    Byte Order:                      Little Endian
    Address sizes:                   46 bits physical, 48 bits virtual
    CPU(s):                          2
    On-line CPU(s) list:             0,1
    Thread(s) per core:              1
    Core(s) per socket:              2
    Socket(s):                       1
    NUMA node(s):                    1
    Vendor ID:                       GenuineIntel
    CPU family:                      6
    Model:                           79
    Model name:                      Intel(R) Xeon(R) CPU E5-2673 v4 @ 2.30GHz
    Stepping:                        1
    CPU MHz:                         2294.685
    BogoMIPS:                        4589.37
    Hypervisor vendor:               Microsoft
    Virtualization type:             full
    L1d cache:                       64 KiB
    L1i cache:                       64 KiB
    L2 cache:                        512 KiB
    L3 cache:                        50 MiB
    NUMA node0 CPU(s):               0,1
    Vulnerability Itlb multihit:     KVM: Mitigation: VMX unsupported
    Vulnerability L1tf:              Mitigation; PTE Inversion
    Vulnerability Mds:               Mitigation; Clear CPU buffers; SMT Host state unknown
    Vulnerability Meltdown:          Mitigation; PTI
    Vulnerability Mmio stale data:   Vulnerable: Clear CPU buffers attempted, no microcode; SMT Host state unknown
    Vulnerability Spec store bypass: Vulnerable
    Vulnerability Spectre v1:        Mitigation; usercopy/swapgs barriers and __user pointer sanitization
    Vulnerability Spectre v2:        Mitigation; Retpolines, STIBP disabled, RSB filling
    Vulnerability Srbds:             Not affected
    Vulnerability Tsx async abort:   Mitigation; Clear CPU buffers; SMT Host state unknown
    Flags:                           fpu vme de pse tsc msr pae mce cx8 apic sep mtrr pge mca cmov pat pse36 clflush mmx fxsr sse sse2 ss ht syscall nx pdpe1gb rdtscp lm constant_tsc rep_good nopl xtopology cpuid pni pclmulqdq ssse3 fma cx16 pcid sse4_1 sse4_2 movbe popcnt aes xsave avx f16c rdrand hypervisor lahf_lm abm 3dnowprefetch invpcid_single pti fsgsbase bmi1 hle avx2 smep bmi2 erms invpcid rtm rdseed adx smap xsaveopt md_clear
    

| Cpu Property       | Value                                                   |
|:------------------ |:------------------------------------------------------- |
| Brand              | Intel(R) Xeon(R) CPU E5-2673 v4 @ 2.30GHz               |
| Vendor             | :Intel                                                  |
| Architecture       | :Broadwell                                              |
| Model              | Family: 0x06, Model: 0x4f, Stepping: 0x01, Type: 0x00   |
| Cores              | 2 physical cores, 2 logical cores (on executing CPU)    |
|                    | No Hyperthreading hardware capability detected          |
| Clock Frequencies  | Not supported by CPU                                    |
| Data Cache         | Level 1:3 : (32, 256, 51200) kbytes                     |
|                    | 64 byte cache line size                                 |
| Address Size       | 48 bits virtual, 46 bits physical                       |
| SIMD               | 256 bit = 32 byte max. SIMD vector size                 |
| Time Stamp Counter | TSC is accessible via `rdtsc`                           |
|                    | TSC increased at every clock cycle (non-invariant TSC)  |
| Perf. Monitoring   | Performance Monitoring Counters (PMC) are not supported |
| Hypervisor         | Yes, Microsoft                                          |

