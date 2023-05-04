# Multi-thread benchmark result

* Pull request commit: [`ee673408636b0187a086a95119da60d6cb8cae8d`](https://github.com/JuliaFolds/Transducers.jl/commit/ee673408636b0187a086a95119da60d6cb8cae8d)
* Pull request: <https://github.com/JuliaFolds/Transducers.jl/pull/553> (Add fast pathway for `copy`, `collect`, `tcollect`, and `tcopy` for size-stable operations)

# Judge result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmarks:
    - Target: 4 May 2023 - 23:12
    - Baseline: 4 May 2023 - 23:17
* Package commits:
    - Target: 491c05
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
| `["collect", "assoc", "basesize=1"]`                | 0.73 (5%) :white_check_mark: | 0.17 (1%) :white_check_mark: |
| `["collect", "assoc", "basesize=1024"]`             |                1.11 (5%) :x: | 0.42 (1%) :white_check_mark: |
| `["collect", "assoc", "basesize=32"]`               |                   0.99 (5%)  | 0.31 (1%) :white_check_mark: |
| `["collect", "seq"]`                                |                   1.02 (5%)  | 0.32 (1%) :white_check_mark: |
| `["collect", "unordered", "basesize=1024"]`         | 0.90 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["findfirst", "n=1000", "foldl"]`                  |                1.11 (5%) :x: |                   1.00 (1%)  |
| `["findfirst", "n=1000", "reduce", "basesize=256"]` | 0.81 (5%) :white_check_mark: | 0.86 (1%) :white_check_mark: |
| `["findfirst", "n=1000", "reduce", "basesize=512"]` |                1.06 (5%) :x: | 0.95 (1%) :white_check_mark: |
| `["findfirst", "n=400", "reduce", "basesize=128"]`  |                1.10 (5%) :x: |                1.03 (1%) :x: |
| `["findfirst", "n=400", "reduce", "basesize=256"]`  |                1.09 (5%) :x: |                   1.00 (1%)  |
| `["findfirst", "n=400", "reduce", "basesize=512"]`  |                   0.99 (5%)  | 0.85 (1%) :white_check_mark: |
| `["findfirst", "n=500", "reduce", "basesize=128"]`  |                1.40 (5%) :x: |                1.28 (1%) :x: |
| `["findfirst", "n=500", "reduce", "basesize=256"]`  |                2.01 (5%) :x: |                1.58 (1%) :x: |
| `["findfirst", "n=500", "reduce", "basesize=512"]`  | 0.84 (5%) :white_check_mark: |                1.05 (1%) :x: |
| `["parallel_histogram", "assoc", "basesize=4096"]`  |                1.09 (5%) :x: |                1.15 (1%) :x: |
| `["parallel_histogram", "assoc", "basesize=8192"]`  |                1.11 (5%) :x: |                   1.00 (1%)  |
| `["parallel_histogram", "comm", "basesize=16384"]`  |                1.05 (5%) :x: |                1.02 (1%) :x: |
| `["parallel_histogram", "comm", "basesize=4096"]`   |                   1.00 (5%)  | 0.95 (1%) :white_check_mark: |
| `["parallel_histogram", "comm", "basesize=8192"]`   |                1.18 (5%) :x: |                1.02 (1%) :x: |
| `["partition_length_maximum", "rand", "foldl"]`     | 0.94 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["splitby", "count", "reduce"]`                    | 0.93 (5%) :white_check_mark: |                1.03 (1%) :x: |
| `["sum", "random", "reduce", "basesize=128"]`       |                1.12 (5%) :x: |                   1.00 (1%)  |
| `["sum", "uniform", "reduce", "basesize=128"]`      |                1.07 (5%) :x: |                   1.00 (1%)  |
| `["sum", "uniform", "reduce", "basesize=256"]`      |                1.12 (5%) :x: |                   1.00 (1%)  |
| `["sum", "uniform", "reduce", "basesize=512"]`      |                1.09 (5%) :x: |                   1.00 (1%)  |
| `["sum", "valley", "reduce", "basesize=512"]`       |                1.06 (5%) :x: |                   1.00 (1%)  |
| `["words", "nthreads=1"]`                           | 0.89 (5%) :white_check_mark: |                   1.01 (1%)  |
| `["words", "nthreads=2"]`                           | 0.88 (5%) :white_check_mark: |                   1.01 (1%)  |
| `["words", "nthreads=4"]`                           | 0.85 (5%) :white_check_mark: |                1.01 (1%) :x: |

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
  CPU: Intel(R) Xeon(R) CPU E5-2673 v4 @ 2.30GHz: 
              speed         user         nice          sys         idle          irq
       #1  2294 MHz       5256 s          0 s        270 s       1834 s          0 s
       #2  2294 MHz       5496 s          0 s        296 s       1550 s          0 s
       
  Memory: 6.781208038330078 GB (3631.453125 MB free)
  Uptime: 744.18 sec
  Load Avg:  1.71  1.55  0.99
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
      Ubuntu 22.04.2 LTS
  uname: Linux 5.15.0-1036-azure #43-Ubuntu SMP Wed Mar 29 16:11:05 UTC 2023 x86_64 x86_64
  CPU: Intel(R) Xeon(R) CPU E5-2673 v4 @ 2.30GHz: 
              speed         user         nice          sys         idle          irq
       #1  2294 MHz       7302 s          0 s        319 s       2805 s          0 s
       #2  2294 MHz       8121 s          0 s        345 s       1951 s          0 s
       
  Memory: 6.781208038330078 GB (3745.01953125 MB free)
  Uptime: 1052.23 sec
  Load Avg:  1.62  1.59  1.16
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-12.0.1 (ORCJIT, broadwell)
```

---
# Target result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmark: 4 May 2023 - 23:12
* Package commit: 491c05
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
| `["collect", "assoc", "basesize=1"]`                | 158.325 ms (5%) |         |   4.36 MiB (1%) |       32800 |
| `["collect", "assoc", "basesize=1024"]`             | 176.535 ms (5%) |         |   1.09 MiB (1%) |          53 |
| `["collect", "assoc", "basesize=32"]`               | 160.511 ms (5%) |         |   1.48 MiB (1%) |        1052 |
| `["collect", "seq"]`                                | 338.813 ms (5%) |         | 256.05 KiB (1%) |           2 |
| `["collect", "unordered", "basesize=1"]`            | 359.197 ms (5%) |         |  23.91 MiB (1%) |      413284 |
| `["collect", "unordered", "basesize=1024"]`         | 174.278 ms (5%) |         |   1.02 MiB (1%) |        1427 |
| `["collect", "unordered", "basesize=32"]`           | 194.169 ms (5%) |         |   1.60 MiB (1%) |       15361 |
| `["findfirst", "n=1000", "foldl"]`                  | 541.090 ms (5%) |         |                 |             |
| `["findfirst", "n=1000", "reduce", "basesize=128"]` | 404.613 ms (5%) |         | 312.02 KiB (1%) |        4380 |
| `["findfirst", "n=1000", "reduce", "basesize=256"]` | 313.890 ms (5%) |         | 139.20 KiB (1%) |        1954 |
| `["findfirst", "n=1000", "reduce", "basesize=512"]` | 520.729 ms (5%) |         | 103.56 KiB (1%) |        1455 |
| `["findfirst", "n=400", "foldl"]`                   | 377.315 ms (5%) |         |                 |             |
| `["findfirst", "n=400", "reduce", "basesize=128"]`  | 225.100 ms (5%) |         | 394.34 KiB (1%) |        5608 |
| `["findfirst", "n=400", "reduce", "basesize=256"]`  | 228.861 ms (5%) |         | 201.02 KiB (1%) |        2878 |
| `["findfirst", "n=400", "reduce", "basesize=512"]`  | 259.095 ms (5%) |         | 112.66 KiB (1%) |        1624 |
| `["findfirst", "n=500", "foldl"]`                   |  61.022 ms (5%) |         |                 |             |
| `["findfirst", "n=500", "reduce", "basesize=128"]`  | 137.381 ms (5%) |         | 227.86 KiB (1%) |        3163 |
| `["findfirst", "n=500", "reduce", "basesize=256"]`  | 126.762 ms (5%) |         | 119.03 KiB (1%) |        1643 |
| `["findfirst", "n=500", "reduce", "basesize=512"]`  |  85.973 ms (5%) |         |  64.92 KiB (1%) |         871 |
| `["overhead", "default"]`                           |  71.600 μs (5%) |         |  32.77 KiB (1%) |         419 |
| `["overhead", "stoppable=false"]`                   |  73.300 μs (5%) |         |  32.75 KiB (1%) |         418 |
| `["overhead", "stoppable=true"]`                    |  84.500 μs (5%) |         |  44.22 KiB (1%) |         609 |
| `["parallel_histogram", "assoc", "basesize=16384"]` |   2.451 ms (5%) |         | 728.91 KiB (1%) |          57 |
| `["parallel_histogram", "assoc", "basesize=4096"]`  |   3.318 ms (5%) |         |   2.05 MiB (1%) |         221 |
| `["parallel_histogram", "assoc", "basesize=8192"]`  |   2.979 ms (5%) |         |   1.42 MiB (1%) |         117 |
| `["parallel_histogram", "comm", "basesize=16384"]`  |  17.872 ms (5%) |         |   1.61 MiB (1%) |        3452 |
| `["parallel_histogram", "comm", "basesize=4096"]`   |  23.353 ms (5%) |         |   1.24 MiB (1%) |        6833 |
| `["parallel_histogram", "comm", "basesize=8192"]`   |  23.007 ms (5%) |         |   1.25 MiB (1%) |        5556 |
| `["parallel_histogram", "seq"]`                     |   4.221 ms (5%) |         | 364.16 KiB (1%) |          24 |
| `["partition_length_maximum", "rand", "foldl"]`     |  31.110 ms (5%) |         |                 |             |
| `["partition_length_maximum", "rand", "reduce"]`    |  16.045 ms (5%) |         |  736 bytes (1%) |          11 |
| `["splitby", "count", "foldl"]`                     |   1.550 ms (5%) |         |                 |             |
| `["splitby", "count", "man"]`                       |   1.223 ms (5%) |         |                 |             |
| `["splitby", "count", "reduce"]`                    | 739.703 μs (5%) |         |   1.09 KiB (1%) |          19 |
| `["sum", "random", "foldl"]`                        |  11.790 ms (5%) |         |                 |             |
| `["sum", "random", "reduce", "basesize=128"]`       |   6.816 ms (5%) |         |  74.11 KiB (1%) |        1102 |
| `["sum", "random", "reduce", "basesize=256"]`       |   6.244 ms (5%) |         |  36.70 KiB (1%) |         545 |
| `["sum", "random", "reduce", "basesize=512"]`       |   5.943 ms (5%) |         |  18.08 KiB (1%) |         269 |
| `["sum", "uniform", "foldl"]`                       |  11.459 ms (5%) |         |                 |             |
| `["sum", "uniform", "reduce", "basesize=128"]`      |   6.114 ms (5%) |         |  74.17 KiB (1%) |        1104 |
| `["sum", "uniform", "reduce", "basesize=256"]`      |   6.387 ms (5%) |         |  36.70 KiB (1%) |         545 |
| `["sum", "uniform", "reduce", "basesize=512"]`      |   6.183 ms (5%) |         |  17.97 KiB (1%) |         266 |
| `["sum", "valley", "foldl"]`                        |  11.673 ms (5%) |         |                 |             |
| `["sum", "valley", "reduce", "basesize=128"]`       |   6.000 ms (5%) |         |  74.05 KiB (1%) |        1100 |
| `["sum", "valley", "reduce", "basesize=256"]`       |   5.996 ms (5%) |         |  36.73 KiB (1%) |         546 |
| `["sum", "valley", "reduce", "basesize=512"]`       |   6.127 ms (5%) |         |  18.03 KiB (1%) |         268 |
| `["words", "nthreads=1"]`                           |  22.731 ms (5%) |         |  31.66 MiB (1%) |     1031963 |
| `["words", "nthreads=2"]`                           |  15.499 ms (5%) |         |  32.38 MiB (1%) |     1032068 |
| `["words", "nthreads=4"]`                           |  14.704 ms (5%) |         |  33.01 MiB (1%) |     1032196 |

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
  CPU: Intel(R) Xeon(R) CPU E5-2673 v4 @ 2.30GHz: 
              speed         user         nice          sys         idle          irq
       #1  2294 MHz       5256 s          0 s        270 s       1834 s          0 s
       #2  2294 MHz       5496 s          0 s        296 s       1550 s          0 s
       
  Memory: 6.781208038330078 GB (3631.453125 MB free)
  Uptime: 744.18 sec
  Load Avg:  1.71  1.55  0.99
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-12.0.1 (ORCJIT, broadwell)
```

---
# Baseline result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmark: 4 May 2023 - 23:17
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
| `["collect", "assoc", "basesize=1"]`                | 215.916 ms (5%) |         |  25.97 MiB (1%) |      306823 |
| `["collect", "assoc", "basesize=1024"]`             | 158.375 ms (5%) |         |   2.61 MiB (1%) |         456 |
| `["collect", "assoc", "basesize=32"]`               | 162.770 ms (5%) |         |   4.82 MiB (1%) |       11703 |
| `["collect", "seq"]`                                | 332.777 ms (5%) |         | 812.73 KiB (1%) |          11 |
| `["collect", "unordered", "basesize=1"]`            | 344.198 ms (5%) |         |  23.93 MiB (1%) |      414028 |
| `["collect", "unordered", "basesize=1024"]`         | 192.886 ms (5%) |         |   1.02 MiB (1%) |        1510 |
| `["collect", "unordered", "basesize=32"]`           | 186.671 ms (5%) |         |   1.61 MiB (1%) |       15532 |
| `["findfirst", "n=1000", "foldl"]`                  | 487.768 ms (5%) |         |                 |             |
| `["findfirst", "n=1000", "reduce", "basesize=128"]` | 390.654 ms (5%) |         | 309.89 KiB (1%) |        4336 |
| `["findfirst", "n=1000", "reduce", "basesize=256"]` | 388.965 ms (5%) |         | 161.86 KiB (1%) |        2278 |
| `["findfirst", "n=1000", "reduce", "basesize=512"]` | 489.152 ms (5%) |         | 109.08 KiB (1%) |        1532 |
| `["findfirst", "n=400", "foldl"]`                   | 367.248 ms (5%) |         |                 |             |
| `["findfirst", "n=400", "reduce", "basesize=128"]`  | 203.778 ms (5%) |         | 383.95 KiB (1%) |        5463 |
| `["findfirst", "n=400", "reduce", "basesize=256"]`  | 209.639 ms (5%) |         | 200.86 KiB (1%) |        2873 |
| `["findfirst", "n=400", "reduce", "basesize=512"]`  | 261.113 ms (5%) |         | 132.92 KiB (1%) |        1894 |
| `["findfirst", "n=500", "foldl"]`                   |  60.866 ms (5%) |         |                 |             |
| `["findfirst", "n=500", "reduce", "basesize=128"]`  |  98.064 ms (5%) |         | 177.36 KiB (1%) |        2439 |
| `["findfirst", "n=500", "reduce", "basesize=256"]`  |  63.018 ms (5%) |         |  75.39 KiB (1%) |        1024 |
| `["findfirst", "n=500", "reduce", "basesize=512"]`  | 102.024 ms (5%) |         |  61.56 KiB (1%) |         844 |
| `["overhead", "default"]`                           |  70.501 μs (5%) |         |  32.70 KiB (1%) |         417 |
| `["overhead", "stoppable=false"]`                   |  72.200 μs (5%) |         |  32.78 KiB (1%) |         419 |
| `["overhead", "stoppable=true"]`                    |  86.100 μs (5%) |         |  44.28 KiB (1%) |         611 |
| `["parallel_histogram", "assoc", "basesize=16384"]` |   2.409 ms (5%) |         | 728.91 KiB (1%) |          57 |
| `["parallel_histogram", "assoc", "basesize=4096"]`  |   3.032 ms (5%) |         |   1.79 MiB (1%) |         215 |
| `["parallel_histogram", "assoc", "basesize=8192"]`  |   2.678 ms (5%) |         |   1.42 MiB (1%) |         117 |
| `["parallel_histogram", "comm", "basesize=16384"]`  |  16.971 ms (5%) |         |   1.58 MiB (1%) |        2543 |
| `["parallel_histogram", "comm", "basesize=4096"]`   |  23.306 ms (5%) |         |   1.30 MiB (1%) |        8805 |
| `["parallel_histogram", "comm", "basesize=8192"]`   |  19.516 ms (5%) |         |   1.22 MiB (1%) |        6241 |
| `["parallel_histogram", "seq"]`                     |   4.190 ms (5%) |         | 364.16 KiB (1%) |          24 |
| `["partition_length_maximum", "rand", "foldl"]`     |  33.243 ms (5%) |         |                 |             |
| `["partition_length_maximum", "rand", "reduce"]`    |  16.684 ms (5%) |         |  736 bytes (1%) |          11 |
| `["splitby", "count", "foldl"]`                     |   1.562 ms (5%) |         |                 |             |
| `["splitby", "count", "man"]`                       |   1.223 ms (5%) |         |                 |             |
| `["splitby", "count", "reduce"]`                    | 792.203 μs (5%) |         |   1.06 KiB (1%) |          18 |
| `["sum", "random", "foldl"]`                        |  11.837 ms (5%) |         |                 |             |
| `["sum", "random", "reduce", "basesize=128"]`       |   6.103 ms (5%) |         |  74.14 KiB (1%) |        1103 |
| `["sum", "random", "reduce", "basesize=256"]`       |   5.961 ms (5%) |         |  36.70 KiB (1%) |         545 |
| `["sum", "random", "reduce", "basesize=512"]`       |   5.824 ms (5%) |         |  18.08 KiB (1%) |         269 |
| `["sum", "uniform", "foldl"]`                       |  11.300 ms (5%) |         |                 |             |
| `["sum", "uniform", "reduce", "basesize=128"]`      |   5.714 ms (5%) |         |  74.14 KiB (1%) |        1103 |
| `["sum", "uniform", "reduce", "basesize=256"]`      |   5.713 ms (5%) |         |  36.73 KiB (1%) |         546 |
| `["sum", "uniform", "reduce", "basesize=512"]`      |   5.661 ms (5%) |         |  18.03 KiB (1%) |         268 |
| `["sum", "valley", "foldl"]`                        |  11.738 ms (5%) |         |                 |             |
| `["sum", "valley", "reduce", "basesize=128"]`       |   6.157 ms (5%) |         |  74.11 KiB (1%) |        1102 |
| `["sum", "valley", "reduce", "basesize=256"]`       |   6.077 ms (5%) |         |  36.67 KiB (1%) |         544 |
| `["sum", "valley", "reduce", "basesize=512"]`       |   5.795 ms (5%) |         |  18.00 KiB (1%) |         267 |
| `["words", "nthreads=1"]`                           |  25.572 ms (5%) |         |  31.40 MiB (1%) |     1023343 |
| `["words", "nthreads=2"]`                           |  17.544 ms (5%) |         |  32.12 MiB (1%) |     1023471 |
| `["words", "nthreads=4"]`                           |  17.330 ms (5%) |         |  32.56 MiB (1%) |     1023537 |

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
  CPU: Intel(R) Xeon(R) CPU E5-2673 v4 @ 2.30GHz: 
              speed         user         nice          sys         idle          irq
       #1  2294 MHz       7302 s          0 s        319 s       2805 s          0 s
       #2  2294 MHz       8121 s          0 s        345 s       1951 s          0 s
       
  Memory: 6.781208038330078 GB (3745.01953125 MB free)
  Uptime: 1052.23 sec
  Load Avg:  1.62  1.59  1.16
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
    Address sizes:                   46 bits physical, 48 bits virtual
    Byte Order:                      Little Endian
    CPU(s):                          2
    On-line CPU(s) list:             0,1
    Vendor ID:                       GenuineIntel
    Model name:                      Intel(R) Xeon(R) CPU E5-2673 v4 @ 2.30GHz
    CPU family:                      6
    Model:                           79
    Thread(s) per core:              1
    Core(s) per socket:              2
    Socket(s):                       1
    Stepping:                        1
    BogoMIPS:                        4589.37
    Flags:                           fpu vme de pse tsc msr pae mce cx8 apic sep mtrr pge mca cmov pat pse36 clflush mmx fxsr sse sse2 ss ht syscall nx pdpe1gb rdtscp lm constant_tsc rep_good nopl xtopology cpuid pni pclmulqdq ssse3 fma cx16 pcid sse4_1 sse4_2 movbe popcnt aes xsave avx f16c rdrand hypervisor lahf_lm abm 3dnowprefetch invpcid_single pti fsgsbase bmi1 hle avx2 smep bmi2 erms invpcid rtm rdseed adx smap xsaveopt md_clear
    Hypervisor vendor:               Microsoft
    Virtualization type:             full
    L1d cache:                       64 KiB (2 instances)
    L1i cache:                       64 KiB (2 instances)
    L2 cache:                        512 KiB (2 instances)
    L3 cache:                        50 MiB (1 instance)
    NUMA node(s):                    1
    NUMA node0 CPU(s):               0,1
    Vulnerability Itlb multihit:     KVM: Mitigation: VMX unsupported
    Vulnerability L1tf:              Mitigation; PTE Inversion
    Vulnerability Mds:               Mitigation; Clear CPU buffers; SMT Host state unknown
    Vulnerability Meltdown:          Mitigation; PTI
    Vulnerability Mmio stale data:   Vulnerable: Clear CPU buffers attempted, no microcode; SMT Host state unknown
    Vulnerability Retbleed:          Not affected
    Vulnerability Spec store bypass: Vulnerable
    Vulnerability Spectre v1:        Mitigation; usercopy/swapgs barriers and __user pointer sanitization
    Vulnerability Spectre v2:        Mitigation; Retpolines, STIBP disabled, RSB filling, PBRSB-eIBRS Not affected
    Vulnerability Srbds:             Not affected
    Vulnerability Tsx async abort:   Mitigation; Clear CPU buffers; SMT Host state unknown
    

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

