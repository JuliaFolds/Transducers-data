# Multi-thread benchmark result

* Pull request commit: [`9b98edf7653602a54c1c8f5c2b648b1bb77acedb`](https://github.com/JuliaFolds/Transducers.jl/commit/9b98edf7653602a54c1c8f5c2b648b1bb77acedb)
* Pull request: <https://github.com/JuliaFolds/Transducers.jl/pull/553> (Add fast pathway for `copy`, `collect`, `tcollect`, and `tcopy` for size-stable operations)

# Judge result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmarks:
    - Target: 4 May 2023 - 23:34
    - Baseline: 4 May 2023 - 23:39
* Package commits:
    - Target: 91881e
    - Baseline: f8d0df
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
| `["collect", "assoc", "basesize=1"]`                | 0.83 (5%) :white_check_mark: | 0.17 (1%) :white_check_mark: |
| `["collect", "assoc", "basesize=1024"]`             |                   1.00 (5%)  | 0.42 (1%) :white_check_mark: |
| `["collect", "assoc", "basesize=32"]`               |                   0.99 (5%)  | 0.31 (1%) :white_check_mark: |
| `["collect", "seq"]`                                |                   1.00 (5%)  | 0.32 (1%) :white_check_mark: |
| `["findfirst", "n=1000", "reduce", "basesize=128"]` |                1.73 (5%) :x: |                1.68 (1%) :x: |
| `["findfirst", "n=1000", "reduce", "basesize=256"]` |                1.13 (5%) :x: |                1.08 (1%) :x: |
| `["findfirst", "n=1000", "reduce", "basesize=512"]` |                1.30 (5%) :x: |                1.33 (1%) :x: |
| `["findfirst", "n=400", "reduce", "basesize=128"]`  |                   1.05 (5%)  |                1.04 (1%) :x: |
| `["findfirst", "n=400", "reduce", "basesize=256"]`  | 0.93 (5%) :white_check_mark: | 0.92 (1%) :white_check_mark: |
| `["findfirst", "n=400", "reduce", "basesize=512"]`  | 0.77 (5%) :white_check_mark: | 0.73 (1%) :white_check_mark: |
| `["findfirst", "n=500", "reduce", "basesize=128"]`  | 0.68 (5%) :white_check_mark: | 0.75 (1%) :white_check_mark: |
| `["findfirst", "n=500", "reduce", "basesize=256"]`  | 0.92 (5%) :white_check_mark: | 0.84 (1%) :white_check_mark: |
| `["findfirst", "n=500", "reduce", "basesize=512"]`  |                2.29 (5%) :x: |                1.74 (1%) :x: |
| `["parallel_histogram", "assoc", "basesize=16384"]` |                1.05 (5%) :x: |                   1.00 (1%)  |
| `["parallel_histogram", "assoc", "basesize=4096"]`  |                   1.01 (5%)  |                1.15 (1%) :x: |
| `["parallel_histogram", "comm", "basesize=16384"]`  |                   0.98 (5%)  | 0.99 (1%) :white_check_mark: |
| `["parallel_histogram", "comm", "basesize=4096"]`   | 0.89 (5%) :white_check_mark: | 0.95 (1%) :white_check_mark: |
| `["parallel_histogram", "comm", "basesize=8192"]`   |                   1.03 (5%)  |                1.37 (1%) :x: |
| `["splitby", "count", "foldl"]`                     | 0.87 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["splitby", "count", "man"]`                       |                1.17 (5%) :x: |                   1.00 (1%)  |
| `["splitby", "count", "reduce"]`                    | 0.90 (5%) :white_check_mark: |                1.03 (1%) :x: |
| `["sum", "random", "reduce", "basesize=128"]`       |                1.05 (5%) :x: |                   1.00 (1%)  |
| `["sum", "random", "reduce", "basesize=512"]`       |                1.05 (5%) :x: |                   1.00 (1%)  |
| `["sum", "valley", "reduce", "basesize=128"]`       | 0.92 (5%) :white_check_mark: |                   1.00 (1%)  |

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
      Ubuntu 22.04.2 LTS
  uname: Linux 5.15.0-1036-azure #43-Ubuntu SMP Wed Mar 29 16:11:05 UTC 2023 x86_64 x86_64
  CPU: Intel(R) Xeon(R) Platinum 8171M CPU @ 2.60GHz: 
              speed         user         nice          sys         idle          irq
       #1  2095 MHz       4758 s          0 s        286 s       4138 s          0 s
       #2  2095 MHz       6141 s          0 s        294 s       2726 s          0 s
       
  Memory: 6.781208038330078 GB (3633.3046875 MB free)
  Uptime: 926.6 sec
  Load Avg:  1.61  1.49  0.93
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-12.0.1 (ORCJIT, skylake-avx512)
```

### Baseline
```
Julia Version 1.7.3
Commit 742b9abb4d (2022-05-06 12:58 UTC)
Platform Info:
  OS: Linux (x86_64-pc-linux-gnu)
      Ubuntu 22.04.2 LTS
  uname: Linux 5.15.0-1036-azure #43-Ubuntu SMP Wed Mar 29 16:11:05 UTC 2023 x86_64 x86_64
  CPU: Intel(R) Xeon(R) Platinum 8171M CPU @ 2.60GHz: 
              speed         user         nice          sys         idle          irq
       #1  2095 MHz       7348 s          0 s        324 s       4588 s          0 s
       #2  2095 MHz       8276 s          0 s        343 s       3616 s          0 s
       
  Memory: 6.781208038330078 GB (3726.10546875 MB free)
  Uptime: 1234.68 sec
  Load Avg:  1.82  1.62  1.13
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-12.0.1 (ORCJIT, skylake-avx512)
```

---
# Target result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmark: 4 May 2023 - 23:34
* Package commit: 91881e
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
| `["collect", "assoc", "basesize=1"]`                | 240.672 ms (5%) |         |   4.36 MiB (1%) |       32801 |
| `["collect", "assoc", "basesize=1024"]`             | 237.958 ms (5%) |         |   1.09 MiB (1%) |          53 |
| `["collect", "assoc", "basesize=32"]`               | 238.554 ms (5%) |         |   1.48 MiB (1%) |        1052 |
| `["collect", "seq"]`                                | 474.029 ms (5%) |         | 256.05 KiB (1%) |           2 |
| `["collect", "unordered", "basesize=1"]`            | 421.203 ms (5%) |         |  23.86 MiB (1%) |      411734 |
| `["collect", "unordered", "basesize=1024"]`         | 256.273 ms (5%) |         |   1.01 MiB (1%) |        1021 |
| `["collect", "unordered", "basesize=32"]`           | 268.298 ms (5%) |         |   1.58 MiB (1%) |       14644 |
| `["findfirst", "n=1000", "foldl"]`                  | 742.675 ms (5%) |         |                 |             |
| `["findfirst", "n=1000", "reduce", "basesize=128"]` | 711.943 ms (5%) |         | 390.77 KiB (1%) |        5490 |
| `["findfirst", "n=1000", "reduce", "basesize=256"]` | 570.232 ms (5%) |         | 170.19 KiB (1%) |        2378 |
| `["findfirst", "n=1000", "reduce", "basesize=512"]` | 668.739 ms (5%) |         | 108.55 KiB (1%) |        1509 |
| `["findfirst", "n=400", "foldl"]`                   | 554.264 ms (5%) |         |                 |             |
| `["findfirst", "n=400", "reduce", "basesize=128"]`  | 322.316 ms (5%) |         | 422.09 KiB (1%) |        5987 |
| `["findfirst", "n=400", "reduce", "basesize=256"]`  | 298.256 ms (5%) |         | 203.25 KiB (1%) |        2904 |
| `["findfirst", "n=400", "reduce", "basesize=512"]`  | 332.065 ms (5%) |         | 112.56 KiB (1%) |        1622 |
| `["findfirst", "n=500", "foldl"]`                   |  97.421 ms (5%) |         |                 |             |
| `["findfirst", "n=500", "reduce", "basesize=128"]`  | 147.966 ms (5%) |         | 189.27 KiB (1%) |        2583 |
| `["findfirst", "n=500", "reduce", "basesize=256"]`  |  98.823 ms (5%) |         |  74.72 KiB (1%) |        1022 |
| `["findfirst", "n=500", "reduce", "basesize=512"]`  | 334.284 ms (5%) |         | 111.03 KiB (1%) |        1536 |
| `["overhead", "default"]`                           |  85.705 μs (5%) |         |  32.73 KiB (1%) |         418 |
| `["overhead", "stoppable=false"]`                   |  85.904 μs (5%) |         |  32.75 KiB (1%) |         418 |
| `["overhead", "stoppable=true"]`                    |  95.805 μs (5%) |         |  44.25 KiB (1%) |         610 |
| `["parallel_histogram", "assoc", "basesize=16384"]` |   3.777 ms (5%) |         | 728.91 KiB (1%) |          57 |
| `["parallel_histogram", "assoc", "basesize=4096"]`  |   4.593 ms (5%) |         |   2.05 MiB (1%) |         221 |
| `["parallel_histogram", "assoc", "basesize=8192"]`  |   4.266 ms (5%) |         |   1.42 MiB (1%) |         117 |
| `["parallel_histogram", "comm", "basesize=16384"]`  |  20.798 ms (5%) |         |   1.59 MiB (1%) |        2723 |
| `["parallel_histogram", "comm", "basesize=4096"]`   |  24.474 ms (5%) |         |   1.18 MiB (1%) |        4979 |
| `["parallel_histogram", "comm", "basesize=8192"]`   |  25.671 ms (5%) |         |   1.71 MiB (1%) |        6633 |
| `["parallel_histogram", "seq"]`                     |   6.871 ms (5%) |         | 364.16 KiB (1%) |          24 |
| `["partition_length_maximum", "rand", "foldl"]`     |  41.200 ms (5%) |         |                 |             |
| `["partition_length_maximum", "rand", "reduce"]`    |  20.591 ms (5%) |         |  736 bytes (1%) |          11 |
| `["splitby", "count", "foldl"]`                     |   2.230 ms (5%) |         |                 |             |
| `["splitby", "count", "man"]`                       |   1.838 ms (5%) |         |                 |             |
| `["splitby", "count", "reduce"]`                    |   1.235 ms (5%) |         |   1.09 KiB (1%) |          19 |
| `["sum", "random", "foldl"]`                        |  18.817 ms (5%) |         |                 |             |
| `["sum", "random", "reduce", "basesize=128"]`       |   9.884 ms (5%) |         |  74.17 KiB (1%) |        1104 |
| `["sum", "random", "reduce", "basesize=256"]`       |   9.278 ms (5%) |         |  36.67 KiB (1%) |         544 |
| `["sum", "random", "reduce", "basesize=512"]`       |   9.690 ms (5%) |         |  18.08 KiB (1%) |         269 |
| `["sum", "uniform", "foldl"]`                       |  17.509 ms (5%) |         |                 |             |
| `["sum", "uniform", "reduce", "basesize=128"]`      |   9.204 ms (5%) |         |  74.14 KiB (1%) |        1103 |
| `["sum", "uniform", "reduce", "basesize=256"]`      |   9.044 ms (5%) |         |  36.77 KiB (1%) |         547 |
| `["sum", "uniform", "reduce", "basesize=512"]`      |   8.920 ms (5%) |         |  18.00 KiB (1%) |         267 |
| `["sum", "valley", "foldl"]`                        |  18.230 ms (5%) |         |                 |             |
| `["sum", "valley", "reduce", "basesize=128"]`       |   8.990 ms (5%) |         |  74.17 KiB (1%) |        1104 |
| `["sum", "valley", "reduce", "basesize=256"]`       |   9.527 ms (5%) |         |  36.70 KiB (1%) |         545 |
| `["sum", "valley", "reduce", "basesize=512"]`       |   9.508 ms (5%) |         |  17.97 KiB (1%) |         266 |
| `["words", "nthreads=1"]`                           |  27.947 ms (5%) |         |  31.68 MiB (1%) |     1032508 |
| `["words", "nthreads=2"]`                           |  16.756 ms (5%) |         |  32.04 MiB (1%) |     1032544 |
| `["words", "nthreads=4"]`                           |  17.175 ms (5%) |         |  32.75 MiB (1%) |     1032631 |

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
      Ubuntu 22.04.2 LTS
  uname: Linux 5.15.0-1036-azure #43-Ubuntu SMP Wed Mar 29 16:11:05 UTC 2023 x86_64 x86_64
  CPU: Intel(R) Xeon(R) Platinum 8171M CPU @ 2.60GHz: 
              speed         user         nice          sys         idle          irq
       #1  2095 MHz       4758 s          0 s        286 s       4138 s          0 s
       #2  2095 MHz       6141 s          0 s        294 s       2726 s          0 s
       
  Memory: 6.781208038330078 GB (3633.3046875 MB free)
  Uptime: 926.6 sec
  Load Avg:  1.61  1.49  0.93
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-12.0.1 (ORCJIT, skylake-avx512)
```

---
# Baseline result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmark: 4 May 2023 - 23:39
* Package commit: f8d0df
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
| `["collect", "assoc", "basesize=1"]`                | 290.247 ms (5%) |         |  25.97 MiB (1%) |      306816 |
| `["collect", "assoc", "basesize=1024"]`             | 238.901 ms (5%) |         |   2.61 MiB (1%) |         456 |
| `["collect", "assoc", "basesize=32"]`               | 241.280 ms (5%) |         |   4.82 MiB (1%) |       11716 |
| `["collect", "seq"]`                                | 473.364 ms (5%) |         | 812.73 KiB (1%) |          11 |
| `["collect", "unordered", "basesize=1"]`            | 407.320 ms (5%) |         |  23.93 MiB (1%) |      413908 |
| `["collect", "unordered", "basesize=1024"]`         | 255.374 ms (5%) |         |   1.01 MiB (1%) |        1075 |
| `["collect", "unordered", "basesize=32"]`           | 268.625 ms (5%) |         |   1.57 MiB (1%) |       14370 |
| `["findfirst", "n=1000", "foldl"]`                  | 750.346 ms (5%) |         |                 |             |
| `["findfirst", "n=1000", "reduce", "basesize=128"]` | 411.977 ms (5%) |         | 232.86 KiB (1%) |        3276 |
| `["findfirst", "n=1000", "reduce", "basesize=256"]` | 504.174 ms (5%) |         | 157.20 KiB (1%) |        2193 |
| `["findfirst", "n=1000", "reduce", "basesize=512"]` | 514.109 ms (5%) |         |  81.33 KiB (1%) |        1146 |
| `["findfirst", "n=400", "foldl"]`                   | 560.545 ms (5%) |         |                 |             |
| `["findfirst", "n=400", "reduce", "basesize=128"]`  | 307.572 ms (5%) |         | 406.47 KiB (1%) |        5765 |
| `["findfirst", "n=400", "reduce", "basesize=256"]`  | 320.346 ms (5%) |         | 221.50 KiB (1%) |        3152 |
| `["findfirst", "n=400", "reduce", "basesize=512"]`  | 429.040 ms (5%) |         | 153.28 KiB (1%) |        2199 |
| `["findfirst", "n=500", "foldl"]`                   |  97.116 ms (5%) |         |                 |             |
| `["findfirst", "n=500", "reduce", "basesize=128"]`  | 217.263 ms (5%) |         | 252.55 KiB (1%) |        3514 |
| `["findfirst", "n=500", "reduce", "basesize=256"]`  | 107.196 ms (5%) |         |  88.56 KiB (1%) |        1193 |
| `["findfirst", "n=500", "reduce", "basesize=512"]`  | 146.274 ms (5%) |         |  63.70 KiB (1%) |         867 |
| `["overhead", "default"]`                           |  85.304 μs (5%) |         |  32.73 KiB (1%) |         418 |
| `["overhead", "stoppable=false"]`                   |  84.904 μs (5%) |         |  32.75 KiB (1%) |         418 |
| `["overhead", "stoppable=true"]`                    |  98.104 μs (5%) |         |  44.25 KiB (1%) |         610 |
| `["parallel_histogram", "assoc", "basesize=16384"]` |   3.593 ms (5%) |         | 728.91 KiB (1%) |          57 |
| `["parallel_histogram", "assoc", "basesize=4096"]`  |   4.529 ms (5%) |         |   1.79 MiB (1%) |         215 |
| `["parallel_histogram", "assoc", "basesize=8192"]`  |   4.265 ms (5%) |         |   1.42 MiB (1%) |         117 |
| `["parallel_histogram", "comm", "basesize=16384"]`  |  21.237 ms (5%) |         |   1.61 MiB (1%) |        3309 |
| `["parallel_histogram", "comm", "basesize=4096"]`   |  27.636 ms (5%) |         |   1.25 MiB (1%) |        6983 |
| `["parallel_histogram", "comm", "basesize=8192"]`   |  24.869 ms (5%) |         |   1.25 MiB (1%) |        6227 |
| `["parallel_histogram", "seq"]`                     |   6.549 ms (5%) |         | 364.16 KiB (1%) |          24 |
| `["partition_length_maximum", "rand", "foldl"]`     |  41.956 ms (5%) |         |                 |             |
| `["partition_length_maximum", "rand", "reduce"]`    |  20.973 ms (5%) |         |  736 bytes (1%) |          11 |
| `["splitby", "count", "foldl"]`                     |   2.576 ms (5%) |         |                 |             |
| `["splitby", "count", "man"]`                       |   1.576 ms (5%) |         |                 |             |
| `["splitby", "count", "reduce"]`                    |   1.369 ms (5%) |         |   1.06 KiB (1%) |          18 |
| `["sum", "random", "foldl"]`                        |  19.004 ms (5%) |         |                 |             |
| `["sum", "random", "reduce", "basesize=128"]`       |   9.376 ms (5%) |         |  74.08 KiB (1%) |        1101 |
| `["sum", "random", "reduce", "basesize=256"]`       |   9.372 ms (5%) |         |  36.70 KiB (1%) |         545 |
| `["sum", "random", "reduce", "basesize=512"]`       |   9.210 ms (5%) |         |  18.11 KiB (1%) |         270 |
| `["sum", "uniform", "foldl"]`                       |  18.384 ms (5%) |         |                 |             |
| `["sum", "uniform", "reduce", "basesize=128"]`      |   9.524 ms (5%) |         |  74.11 KiB (1%) |        1102 |
| `["sum", "uniform", "reduce", "basesize=256"]`      |   9.222 ms (5%) |         |  36.73 KiB (1%) |         546 |
| `["sum", "uniform", "reduce", "basesize=512"]`      |   9.119 ms (5%) |         |  18.03 KiB (1%) |         268 |
| `["sum", "valley", "foldl"]`                        |  18.941 ms (5%) |         |                 |             |
| `["sum", "valley", "reduce", "basesize=128"]`       |   9.802 ms (5%) |         |  74.17 KiB (1%) |        1104 |
| `["sum", "valley", "reduce", "basesize=256"]`       |   9.714 ms (5%) |         |  36.70 KiB (1%) |         545 |
| `["sum", "valley", "reduce", "basesize=512"]`       |   9.739 ms (5%) |         |  18.06 KiB (1%) |         269 |
| `["words", "nthreads=1"]`                           |  28.467 ms (5%) |         |  31.74 MiB (1%) |     1034134 |
| `["words", "nthreads=2"]`                           |  16.866 ms (5%) |         |  32.09 MiB (1%) |     1034170 |
| `["words", "nthreads=4"]`                           |  17.000 ms (5%) |         |  32.99 MiB (1%) |     1034309 |

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
      Ubuntu 22.04.2 LTS
  uname: Linux 5.15.0-1036-azure #43-Ubuntu SMP Wed Mar 29 16:11:05 UTC 2023 x86_64 x86_64
  CPU: Intel(R) Xeon(R) Platinum 8171M CPU @ 2.60GHz: 
              speed         user         nice          sys         idle          irq
       #1  2095 MHz       7348 s          0 s        324 s       4588 s          0 s
       #2  2095 MHz       8276 s          0 s        343 s       3616 s          0 s
       
  Memory: 6.781208038330078 GB (3726.10546875 MB free)
  Uptime: 1234.68 sec
  Load Avg:  1.82  1.62  1.13
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-12.0.1 (ORCJIT, skylake-avx512)
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
    Address sizes:                   46 bits physical, 48 bits virtual
    Byte Order:                      Little Endian
    CPU(s):                          2
    On-line CPU(s) list:             0,1
    Vendor ID:                       GenuineIntel
    Model name:                      Intel(R) Xeon(R) Platinum 8171M CPU @ 2.60GHz
    CPU family:                      6
    Model:                           85
    Thread(s) per core:              1
    Core(s) per socket:              2
    Socket(s):                       1
    Stepping:                        4
    BogoMIPS:                        4190.34
    Flags:                           fpu vme de pse tsc msr pae mce cx8 apic sep mtrr pge mca cmov pat pse36 clflush mmx fxsr sse sse2 ss ht syscall nx pdpe1gb rdtscp lm constant_tsc rep_good nopl xtopology cpuid pni pclmulqdq ssse3 fma cx16 pcid sse4_1 sse4_2 movbe popcnt aes xsave avx f16c rdrand hypervisor lahf_lm abm 3dnowprefetch invpcid_single pti fsgsbase bmi1 hle avx2 smep bmi2 erms invpcid rtm avx512f avx512dq rdseed adx smap clflushopt avx512cd avx512bw avx512vl xsaveopt xsavec xsaves md_clear
    Hypervisor vendor:               Microsoft
    Virtualization type:             full
    L1d cache:                       64 KiB (2 instances)
    L1i cache:                       64 KiB (2 instances)
    L2 cache:                        2 MiB (2 instances)
    L3 cache:                        35.8 MiB (1 instance)
    NUMA node(s):                    1
    NUMA node0 CPU(s):               0,1
    Vulnerability Itlb multihit:     KVM: Mitigation: VMX unsupported
    Vulnerability L1tf:              Mitigation; PTE Inversion
    Vulnerability Mds:               Mitigation; Clear CPU buffers; SMT Host state unknown
    Vulnerability Meltdown:          Mitigation; PTI
    Vulnerability Mmio stale data:   Vulnerable: Clear CPU buffers attempted, no microcode; SMT Host state unknown
    Vulnerability Retbleed:          Vulnerable
    Vulnerability Spec store bypass: Vulnerable
    Vulnerability Spectre v1:        Mitigation; usercopy/swapgs barriers and __user pointer sanitization
    Vulnerability Spectre v2:        Mitigation; Retpolines, STIBP disabled, RSB filling, PBRSB-eIBRS Not affected
    Vulnerability Srbds:             Not affected
    Vulnerability Tsx async abort:   Mitigation; Clear CPU buffers; SMT Host state unknown
    

| Cpu Property       | Value                                                   |
|:------------------ |:------------------------------------------------------- |
| Brand              | Intel(R) Xeon(R) Platinum 8171M CPU @ 2.60GHz           |
| Vendor             | :Intel                                                  |
| Architecture       | :Skylake                                                |
| Model              | Family: 0x06, Model: 0x55, Stepping: 0x04, Type: 0x00   |
| Cores              | 2 physical cores, 2 logical cores (on executing CPU)    |
|                    | No Hyperthreading hardware capability detected          |
| Clock Frequencies  | Not supported by CPU                                    |
| Data Cache         | Level 1:3 : (32, 1024, 36608) kbytes                    |
|                    | 64 byte cache line size                                 |
| Address Size       | 48 bits virtual, 46 bits physical                       |
| SIMD               | 512 bit = 64 byte max. SIMD vector size                 |
| Time Stamp Counter | TSC is accessible via `rdtsc`                           |
|                    | TSC increased at every clock cycle (non-invariant TSC)  |
| Perf. Monitoring   | Performance Monitoring Counters (PMC) are not supported |
| Hypervisor         | Yes, Microsoft                                          |

