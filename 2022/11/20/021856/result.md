# Multi-thread benchmark result

* Pull request commit: [`adb836a62c98ac48449cec932a9878b6426c58fb`](https://github.com/JuliaFolds/Transducers.jl/commit/adb836a62c98ac48449cec932a9878b6426c58fb)
* Pull request: <https://github.com/JuliaFolds/Transducers.jl/pull/243> (Update */Manifest.toml)

# Judge result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmarks:
    - Target: 20 Nov 2022 - 02:12
    - Baseline: 20 Nov 2022 - 02:18
* Package commits:
    - Target: ce70d0
    - Baseline: 958213
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
| `["findfirst", "n=1000", "reduce", "basesize=128"]` |                1.05 (5%) :x: |                1.06 (1%) :x: |
| `["findfirst", "n=1000", "reduce", "basesize=256"]` |                1.07 (5%) :x: |                   1.00 (1%)  |
| `["findfirst", "n=1000", "reduce", "basesize=512"]` |                2.06 (5%) :x: |                1.72 (1%) :x: |
| `["findfirst", "n=400", "reduce", "basesize=128"]`  |                1.05 (5%) :x: |                   1.00 (1%)  |
| `["findfirst", "n=400", "reduce", "basesize=512"]`  |                   1.02 (5%)  | 0.97 (1%) :white_check_mark: |
| `["findfirst", "n=500", "reduce", "basesize=128"]`  | 0.81 (5%) :white_check_mark: | 0.81 (1%) :white_check_mark: |
| `["findfirst", "n=500", "reduce", "basesize=256"]`  | 0.51 (5%) :white_check_mark: | 0.58 (1%) :white_check_mark: |
| `["findfirst", "n=500", "reduce", "basesize=512"]`  |                1.74 (5%) :x: |                1.40 (1%) :x: |
| `["parallel_histogram", "comm", "basesize=16384"]`  |                1.05 (5%) :x: |                   1.00 (1%)  |
| `["parallel_histogram", "comm", "basesize=4096"]`   | 0.90 (5%) :white_check_mark: | 0.94 (1%) :white_check_mark: |
| `["parallel_histogram", "comm", "basesize=8192"]`   |                   1.05 (5%)  | 0.99 (1%) :white_check_mark: |
| `["splitby", "count", "reduce"]`                    |                   1.00 (5%)  | 0.97 (1%) :white_check_mark: |
| `["sum", "uniform", "reduce", "basesize=256"]`      | 0.94 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["words", "nthreads=2"]`                           |                1.08 (5%) :x: |                   1.01 (1%)  |
| `["words", "nthreads=4"]`                           |                1.05 (5%) :x: |                   1.01 (1%)  |

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
      Ubuntu 22.04.1 LTS
  uname: Linux 5.15.0-1022-azure #27-Ubuntu SMP Thu Oct 13 17:09:33 UTC 2022 x86_64 x86_64
  CPU: Intel(R) Xeon(R) CPU E5-2673 v3 @ 2.40GHz: 
              speed         user         nice          sys         idle          irq
       #1  2397 MHz       5643 s          0 s        244 s       1417 s          0 s
       #2  2397 MHz       5136 s          0 s        264 s       1909 s          0 s
       
  Memory: 6.781223297119141 GB (3779.8828125 MB free)
  Uptime: 738.73 sec
  Load Avg:  1.75  1.57  1.0
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-12.0.1 (ORCJIT, haswell)
```

### Baseline
```
Julia Version 1.7.3
Commit 742b9abb4d (2022-05-06 12:58 UTC)
Platform Info:
  OS: Linux (x86_64-pc-linux-gnu)
      Ubuntu 22.04.1 LTS
  uname: Linux 5.15.0-1022-azure #27-Ubuntu SMP Thu Oct 13 17:09:33 UTC 2022 x86_64 x86_64
  CPU: Intel(R) Xeon(R) CPU E5-2673 v3 @ 2.40GHz: 
              speed         user         nice          sys         idle          irq
       #1  2397 MHz       8406 s          0 s        314 s       1802 s          0 s
       #2  2397 MHz       7226 s          0 s        366 s       2932 s          0 s
       
  Memory: 6.781223297119141 GB (3751.9375 MB free)
  Uptime: 1061.05 sec
  Load Avg:  1.72  1.63  1.18
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-12.0.1 (ORCJIT, haswell)
```

---
# Target result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmark: 20 Nov 2022 - 2:12
* Package commit: ce70d0
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
| `["collect", "assoc", "basesize=1"]`                | 276.206 ms (5%) |         |  25.97 MiB (1%) |      306822 |
| `["collect", "assoc", "basesize=1024"]`             | 223.132 ms (5%) |         |   2.61 MiB (1%) |         456 |
| `["collect", "assoc", "basesize=32"]`               | 228.826 ms (5%) |         |   4.82 MiB (1%) |       11706 |
| `["collect", "seq"]`                                | 441.386 ms (5%) |         | 812.73 KiB (1%) |          11 |
| `["collect", "unordered", "basesize=1"]`            | 373.527 ms (5%) |         |  23.86 MiB (1%) |      411562 |
| `["collect", "unordered", "basesize=1024"]`         | 237.776 ms (5%) |         |   1.01 MiB (1%) |        1140 |
| `["collect", "unordered", "basesize=32"]`           | 250.193 ms (5%) |         |   1.60 MiB (1%) |       15297 |
| `["findfirst", "n=1000", "foldl"]`                  | 645.068 ms (5%) |         |                 |             |
| `["findfirst", "n=1000", "reduce", "basesize=128"]` | 590.102 ms (5%) |         | 358.95 KiB (1%) |        5063 |
| `["findfirst", "n=1000", "reduce", "basesize=256"]` | 481.122 ms (5%) |         | 156.88 KiB (1%) |        2202 |
| `["findfirst", "n=1000", "reduce", "basesize=512"]` |    1.135 s (5%) |         | 171.06 KiB (1%) |        2399 |
| `["findfirst", "n=400", "foldl"]`                   | 482.792 ms (5%) |         |                 |             |
| `["findfirst", "n=400", "reduce", "basesize=128"]`  | 271.702 ms (5%) |         | 376.55 KiB (1%) |        5365 |
| `["findfirst", "n=400", "reduce", "basesize=256"]`  | 268.543 ms (5%) |         | 200.95 KiB (1%) |        2876 |
| `["findfirst", "n=400", "reduce", "basesize=512"]`  | 349.094 ms (5%) |         | 134.31 KiB (1%) |        1914 |
| `["findfirst", "n=500", "foldl"]`                   |  82.736 ms (5%) |         |                 |             |
| `["findfirst", "n=500", "reduce", "basesize=128"]`  | 171.974 ms (5%) |         | 219.78 KiB (1%) |        3060 |
| `["findfirst", "n=500", "reduce", "basesize=256"]`  |  78.904 ms (5%) |         |  71.38 KiB (1%) |         971 |
| `["findfirst", "n=500", "reduce", "basesize=512"]`  | 230.510 ms (5%) |         |  92.92 KiB (1%) |        1260 |
| `["overhead", "default"]`                           |  71.003 μs (5%) |         |  32.77 KiB (1%) |         419 |
| `["overhead", "stoppable=false"]`                   |  71.203 μs (5%) |         |  32.75 KiB (1%) |         418 |
| `["overhead", "stoppable=true"]`                    |  84.603 μs (5%) |         |  44.28 KiB (1%) |         611 |
| `["parallel_histogram", "assoc", "basesize=16384"]` |   3.344 ms (5%) |         | 728.91 KiB (1%) |          57 |
| `["parallel_histogram", "assoc", "basesize=4096"]`  |   4.012 ms (5%) |         |   1.79 MiB (1%) |         215 |
| `["parallel_histogram", "assoc", "basesize=8192"]`  |   3.681 ms (5%) |         |   1.42 MiB (1%) |         117 |
| `["parallel_histogram", "comm", "basesize=16384"]`  |  11.397 ms (5%) |         |   1.51 MiB (1%) |         245 |
| `["parallel_histogram", "comm", "basesize=4096"]`   |  14.057 ms (5%) |         |   1.03 MiB (1%) |        1871 |
| `["parallel_histogram", "comm", "basesize=8192"]`   |  14.525 ms (5%) |         |   1.06 MiB (1%) |         184 |
| `["parallel_histogram", "seq"]`                     |   6.086 ms (5%) |         | 364.16 KiB (1%) |          24 |
| `["partition_length_maximum", "rand", "foldl"]`     |  56.565 ms (5%) |         |                 |             |
| `["partition_length_maximum", "rand", "reduce"]`    |  28.264 ms (5%) |         |  736 bytes (1%) |          11 |
| `["splitby", "count", "foldl"]`                     |   1.889 ms (5%) |         |                 |             |
| `["splitby", "count", "man"]`                       |   1.461 ms (5%) |         |                 |             |
| `["splitby", "count", "reduce"]`                    | 890.132 μs (5%) |         |   1.06 KiB (1%) |          19 |
| `["sum", "random", "foldl"]`                        |  16.494 ms (5%) |         |                 |             |
| `["sum", "random", "reduce", "basesize=128"]`       |   8.361 ms (5%) |         |  74.17 KiB (1%) |        1104 |
| `["sum", "random", "reduce", "basesize=256"]`       |   8.237 ms (5%) |         |  36.80 KiB (1%) |         548 |
| `["sum", "random", "reduce", "basesize=512"]`       |   8.193 ms (5%) |         |  18.05 KiB (1%) |         268 |
| `["sum", "uniform", "foldl"]`                       |  15.994 ms (5%) |         |                 |             |
| `["sum", "uniform", "reduce", "basesize=128"]`      |   8.130 ms (5%) |         |  74.08 KiB (1%) |        1101 |
| `["sum", "uniform", "reduce", "basesize=256"]`      |   7.996 ms (5%) |         |  36.70 KiB (1%) |         545 |
| `["sum", "uniform", "reduce", "basesize=512"]`      |   7.953 ms (5%) |         |  18.00 KiB (1%) |         267 |
| `["sum", "valley", "foldl"]`                        |  16.447 ms (5%) |         |                 |             |
| `["sum", "valley", "reduce", "basesize=128"]`       |   8.401 ms (5%) |         |  74.14 KiB (1%) |        1103 |
| `["sum", "valley", "reduce", "basesize=256"]`       |   8.281 ms (5%) |         |  36.70 KiB (1%) |         545 |
| `["sum", "valley", "reduce", "basesize=512"]`       |   8.309 ms (5%) |         |  18.03 KiB (1%) |         268 |
| `["words", "nthreads=1"]`                           |  24.388 ms (5%) |         |  31.69 MiB (1%) |     1032324 |
| `["words", "nthreads=2"]`                           |  16.077 ms (5%) |         |  32.05 MiB (1%) |     1032391 |
| `["words", "nthreads=4"]`                           |  15.972 ms (5%) |         |  32.94 MiB (1%) |     1032577 |

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
      Ubuntu 22.04.1 LTS
  uname: Linux 5.15.0-1022-azure #27-Ubuntu SMP Thu Oct 13 17:09:33 UTC 2022 x86_64 x86_64
  CPU: Intel(R) Xeon(R) CPU E5-2673 v3 @ 2.40GHz: 
              speed         user         nice          sys         idle          irq
       #1  2397 MHz       5643 s          0 s        244 s       1417 s          0 s
       #2  2397 MHz       5136 s          0 s        264 s       1909 s          0 s
       
  Memory: 6.781223297119141 GB (3779.8828125 MB free)
  Uptime: 738.73 sec
  Load Avg:  1.75  1.57  1.0
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-12.0.1 (ORCJIT, haswell)
```

---
# Baseline result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmark: 20 Nov 2022 - 2:18
* Package commit: 958213
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
| `["collect", "assoc", "basesize=1"]`                | 283.963 ms (5%) |         |  25.97 MiB (1%) |      306855 |
| `["collect", "assoc", "basesize=1024"]`             | 222.096 ms (5%) |         |   2.61 MiB (1%) |         455 |
| `["collect", "assoc", "basesize=32"]`               | 227.337 ms (5%) |         |   4.82 MiB (1%) |       11709 |
| `["collect", "seq"]`                                | 445.020 ms (5%) |         | 812.73 KiB (1%) |          11 |
| `["collect", "unordered", "basesize=1"]`            | 380.325 ms (5%) |         |  23.68 MiB (1%) |      405701 |
| `["collect", "unordered", "basesize=1024"]`         | 243.964 ms (5%) |         |   1.01 MiB (1%) |        1072 |
| `["collect", "unordered", "basesize=32"]`           | 250.983 ms (5%) |         |   1.60 MiB (1%) |       15352 |
| `["findfirst", "n=1000", "foldl"]`                  | 645.398 ms (5%) |         |                 |             |
| `["findfirst", "n=1000", "reduce", "basesize=128"]` | 560.703 ms (5%) |         | 338.78 KiB (1%) |        4781 |
| `["findfirst", "n=1000", "reduce", "basesize=256"]` | 450.987 ms (5%) |         | 157.20 KiB (1%) |        2193 |
| `["findfirst", "n=1000", "reduce", "basesize=512"]` | 550.752 ms (5%) |         |  99.30 KiB (1%) |        1386 |
| `["findfirst", "n=400", "foldl"]`                   | 483.417 ms (5%) |         |                 |             |
| `["findfirst", "n=400", "reduce", "basesize=128"]`  | 258.648 ms (5%) |         | 375.44 KiB (1%) |        5360 |
| `["findfirst", "n=400", "reduce", "basesize=256"]`  | 259.448 ms (5%) |         | 201.11 KiB (1%) |        2881 |
| `["findfirst", "n=400", "reduce", "basesize=512"]`  | 341.959 ms (5%) |         | 139.06 KiB (1%) |        1978 |
| `["findfirst", "n=500", "foldl"]`                   |  82.913 ms (5%) |         |                 |             |
| `["findfirst", "n=500", "reduce", "basesize=128"]`  | 211.995 ms (5%) |         | 272.00 KiB (1%) |        3794 |
| `["findfirst", "n=500", "reduce", "basesize=256"]`  | 155.153 ms (5%) |         | 122.98 KiB (1%) |        1690 |
| `["findfirst", "n=500", "reduce", "basesize=512"]`  | 132.674 ms (5%) |         |  66.17 KiB (1%) |         901 |
| `["overhead", "default"]`                           |  72.503 μs (5%) |         |  32.73 KiB (1%) |         418 |
| `["overhead", "stoppable=false"]`                   |  70.903 μs (5%) |         |  32.75 KiB (1%) |         418 |
| `["overhead", "stoppable=true"]`                    |  85.604 μs (5%) |         |  44.28 KiB (1%) |         611 |
| `["parallel_histogram", "assoc", "basesize=16384"]` |   3.335 ms (5%) |         | 728.91 KiB (1%) |          57 |
| `["parallel_histogram", "assoc", "basesize=4096"]`  |   3.968 ms (5%) |         |   1.79 MiB (1%) |         215 |
| `["parallel_histogram", "assoc", "basesize=8192"]`  |   3.666 ms (5%) |         |   1.42 MiB (1%) |         117 |
| `["parallel_histogram", "comm", "basesize=16384"]`  |  10.848 ms (5%) |         |   1.51 MiB (1%) |         237 |
| `["parallel_histogram", "comm", "basesize=4096"]`   |  15.680 ms (5%) |         |   1.09 MiB (1%) |        2918 |
| `["parallel_histogram", "comm", "basesize=8192"]`   |  13.842 ms (5%) |         |   1.07 MiB (1%) |        1389 |
| `["parallel_histogram", "seq"]`                     |   6.048 ms (5%) |         | 364.16 KiB (1%) |          24 |
| `["partition_length_maximum", "rand", "foldl"]`     |  56.299 ms (5%) |         |                 |             |
| `["partition_length_maximum", "rand", "reduce"]`    |  28.102 ms (5%) |         |  736 bytes (1%) |          11 |
| `["splitby", "count", "foldl"]`                     |   1.900 ms (5%) |         |                 |             |
| `["splitby", "count", "man"]`                       |   1.487 ms (5%) |         |                 |             |
| `["splitby", "count", "reduce"]`                    | 888.226 μs (5%) |         |   1.09 KiB (1%) |          19 |
| `["sum", "random", "foldl"]`                        |  16.441 ms (5%) |         |                 |             |
| `["sum", "random", "reduce", "basesize=128"]`       |   8.227 ms (5%) |         |  74.08 KiB (1%) |        1101 |
| `["sum", "random", "reduce", "basesize=256"]`       |   8.204 ms (5%) |         |  36.70 KiB (1%) |         545 |
| `["sum", "random", "reduce", "basesize=512"]`       |   8.118 ms (5%) |         |  18.08 KiB (1%) |         269 |
| `["sum", "uniform", "foldl"]`                       |  16.011 ms (5%) |         |                 |             |
| `["sum", "uniform", "reduce", "basesize=128"]`      |   8.156 ms (5%) |         |  74.11 KiB (1%) |        1102 |
| `["sum", "uniform", "reduce", "basesize=256"]`      |   8.541 ms (5%) |         |  36.77 KiB (1%) |         547 |
| `["sum", "uniform", "reduce", "basesize=512"]`      |   7.973 ms (5%) |         |  18.03 KiB (1%) |         268 |
| `["sum", "valley", "foldl"]`                        |  16.507 ms (5%) |         |                 |             |
| `["sum", "valley", "reduce", "basesize=128"]`       |   8.391 ms (5%) |         |  74.05 KiB (1%) |        1100 |
| `["sum", "valley", "reduce", "basesize=256"]`       |   8.300 ms (5%) |         |  36.67 KiB (1%) |         544 |
| `["sum", "valley", "reduce", "basesize=512"]`       |   8.244 ms (5%) |         |  18.00 KiB (1%) |         267 |
| `["words", "nthreads=1"]`                           |  24.363 ms (5%) |         |  31.42 MiB (1%) |     1023460 |
| `["words", "nthreads=2"]`                           |  14.832 ms (5%) |         |  31.77 MiB (1%) |     1023501 |
| `["words", "nthreads=4"]`                           |  15.166 ms (5%) |         |  32.67 MiB (1%) |     1023695 |

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
      Ubuntu 22.04.1 LTS
  uname: Linux 5.15.0-1022-azure #27-Ubuntu SMP Thu Oct 13 17:09:33 UTC 2022 x86_64 x86_64
  CPU: Intel(R) Xeon(R) CPU E5-2673 v3 @ 2.40GHz: 
              speed         user         nice          sys         idle          irq
       #1  2397 MHz       8406 s          0 s        314 s       1802 s          0 s
       #2  2397 MHz       7226 s          0 s        366 s       2932 s          0 s
       
  Memory: 6.781223297119141 GB (3751.9375 MB free)
  Uptime: 1061.05 sec
  Load Avg:  1.72  1.63  1.18
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-12.0.1 (ORCJIT, haswell)
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
    Model name:                      Intel(R) Xeon(R) CPU E5-2673 v3 @ 2.40GHz
    CPU family:                      6
    Model:                           63
    Thread(s) per core:              1
    Core(s) per socket:              2
    Socket(s):                       1
    Stepping:                        2
    BogoMIPS:                        4794.44
    Flags:                           fpu vme de pse tsc msr pae mce cx8 apic sep mtrr pge mca cmov pat pse36 clflush mmx fxsr sse sse2 ss ht syscall nx pdpe1gb rdtscp lm constant_tsc rep_good nopl xtopology cpuid pni pclmulqdq ssse3 fma cx16 pcid sse4_1 sse4_2 movbe popcnt aes xsave avx f16c rdrand hypervisor lahf_lm abm invpcid_single pti fsgsbase bmi1 avx2 smep bmi2 erms invpcid xsaveopt md_clear
    Hypervisor vendor:               Microsoft
    Virtualization type:             full
    L1d cache:                       64 KiB (2 instances)
    L1i cache:                       64 KiB (2 instances)
    L2 cache:                        512 KiB (2 instances)
    L3 cache:                        30 MiB (1 instance)
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
    Vulnerability Tsx async abort:   Not affected
    

| Cpu Property       | Value                                                   |
|:------------------ |:------------------------------------------------------- |
| Brand              | Intel(R) Xeon(R) CPU E5-2673 v3 @ 2.40GHz               |
| Vendor             | :Intel                                                  |
| Architecture       | :Haswell                                                |
| Model              | Family: 0x06, Model: 0x3f, Stepping: 0x02, Type: 0x00   |
| Cores              | 2 physical cores, 2 logical cores (on executing CPU)    |
|                    | No Hyperthreading hardware capability detected          |
| Clock Frequencies  | Not supported by CPU                                    |
| Data Cache         | Level 1:3 : (32, 256, 30720) kbytes                     |
|                    | 64 byte cache line size                                 |
| Address Size       | 48 bits virtual, 46 bits physical                       |
| SIMD               | 256 bit = 32 byte max. SIMD vector size                 |
| Time Stamp Counter | TSC is accessible via `rdtsc`                           |
|                    | TSC increased at every clock cycle (non-invariant TSC)  |
| Perf. Monitoring   | Performance Monitoring Counters (PMC) are not supported |
| Hypervisor         | Yes, Microsoft                                          |

