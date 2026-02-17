# Multi-thread benchmark result

* Pull request commit: [`b2eb2a564b3a8a97538178a037eecef6f64d5bc4`](https://github.com/JuliaFolds/Transducers.jl/commit/b2eb2a564b3a8a97538178a037eecef6f64d5bc4)
* Pull request: <https://github.com/JuliaFolds/Transducers.jl/pull/243> (Update */Manifest.toml)

# Judge result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmarks:
    - Target: 17 Feb 2026 - 02:50
    - Baseline: 17 Feb 2026 - 02:56
* Package commits:
    - Target: 221cf78
    - Baseline: 2a51f8d
* Julia commits:
    - Target: 742b9ab
    - Baseline: 742b9ab
* Julia command flags:
    - Target: None
    - Baseline: None
* Environment variables:
    - Target: `JULIA_NUM_THREADS => 2`
    - Baseline: `JULIA_NUM_THREADS => 2`

## Results
A ratio greater than `1.0` denotes a possible regression (marked with :x:), while a ratio less
than `1.0` denotes a possible improvement (marked with :white_check_mark:). Brackets display [tolerances](https://juliaci.github.io/BenchmarkTools.jl/stable/manual/#Benchmark-Parameters) for the benchmark estimates. Only significant results - results
that indicate possible regressions or improvements - are shown below (thus, an empty table means that all
benchmark results remained invariant between builds).

| ID                                                  | time ratio                   | memory ratio                 |
|-----------------------------------------------------|------------------------------|------------------------------|
| `["findfirst", "n=1000", "reduce", "basesize=128"]` | 0.86 (5%) :white_check_mark: | 0.88 (1%) :white_check_mark: |
| `["findfirst", "n=1000", "reduce", "basesize=256"]` | 0.93 (5%) :white_check_mark: | 0.91 (1%) :white_check_mark: |
| `["findfirst", "n=400", "reduce", "basesize=128"]`  |                   0.98 (5%)  | 0.95 (1%) :white_check_mark: |
| `["findfirst", "n=400", "reduce", "basesize=512"]`  |                1.31 (5%) :x: |                1.34 (1%) :x: |
| `["findfirst", "n=500", "reduce", "basesize=128"]`  |                1.09 (5%) :x: |                1.08 (1%) :x: |
| `["findfirst", "n=500", "reduce", "basesize=256"]`  |                2.55 (5%) :x: |                2.12 (1%) :x: |
| `["findfirst", "n=500", "reduce", "basesize=512"]`  |                3.45 (5%) :x: |                2.44 (1%) :x: |
| `["parallel_histogram", "assoc", "basesize=4096"]`  |                   1.02 (5%)  |                1.30 (1%) :x: |
| `["parallel_histogram", "comm", "basesize=4096"]`   |                   1.05 (5%)  | 0.96 (1%) :white_check_mark: |
| `["parallel_histogram", "comm", "basesize=8192"]`   |                   0.99 (5%)  |                1.01 (1%) :x: |
| `["splitby", "count", "reduce"]`                    | 0.92 (5%) :white_check_mark: | 0.97 (1%) :white_check_mark: |
| `["words", "nthreads=2"]`                           | 0.87 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["words", "nthreads=4"]`                           | 0.89 (5%) :white_check_mark: |                   1.00 (1%)  |

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
      Ubuntu 24.04.3 LTS
  uname: Linux 6.14.0-1017-azure #17~24.04.1-Ubuntu SMP Mon Dec  1 20:10:50 UTC 2025 x86_64 x86_64
  CPU: AMD EPYC 9V74 80-Core Processor: 
              speed         user         nice          sys         idle          irq
       #1  2867 MHz       3006 s          0 s        160 s       4201 s          0 s
       #2  2866 MHz       2112 s          0 s        180 s       5071 s          0 s
       #3  2868 MHz       2487 s          0 s        160 s       4714 s          0 s
       #4  2877 MHz       2697 s          0 s        177 s       4497 s          0 s
       
  Memory: 15.615703582763672 GB (12016.33984375 MB free)
  Uptime: 740.45 sec
  Load Avg:  1.77  1.52  0.89
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-12.0.1 (ORCJIT, znver3)
```

### Baseline
```
Julia Version 1.7.3
Commit 742b9abb4d (2022-05-06 12:58 UTC)
Platform Info:
  OS: Linux (x86_64-pc-linux-gnu)
      Ubuntu 24.04.3 LTS
  uname: Linux 6.14.0-1017-azure #17~24.04.1-Ubuntu SMP Mon Dec  1 20:10:50 UTC 2025 x86_64 x86_64
  CPU: AMD EPYC 9V74 80-Core Processor: 
              speed         user         nice          sys         idle          irq
       #1  2872 MHz       4340 s          0 s        222 s       5941 s          0 s
       #2  2870 MHz       3473 s          0 s        240 s       6787 s          0 s
       #3  2872 MHz       3329 s          0 s        214 s       6955 s          0 s
       #4  2870 MHz       4032 s          0 s        241 s       6238 s          0 s
       
  Memory: 15.615703582763672 GB (11944.49609375 MB free)
  Uptime: 1054.82 sec
  Load Avg:  1.59  1.61  1.12
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-12.0.1 (ORCJIT, znver3)
```

---
# Target result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmark: 17 Feb 2026 - 02:50
* Package commit: 221cf78
* Julia commit: 742b9ab
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
| `["collect", "assoc", "basesize=1"]`                | 168.924 ms (5%) |         |   4.36 MiB (1%) |       32800 |
| `["collect", "assoc", "basesize=1024"]`             | 167.500 ms (5%) |         |   1.09 MiB (1%) |          54 |
| `["collect", "assoc", "basesize=32"]`               | 167.652 ms (5%) |         |   1.48 MiB (1%) |        1053 |
| `["collect", "seq"]`                                | 334.344 ms (5%) |         | 256.05 KiB (1%) |           2 |
| `["collect", "unordered", "basesize=1"]`            | 315.495 ms (5%) |         |  23.90 MiB (1%) |      413156 |
| `["collect", "unordered", "basesize=1024"]`         | 176.423 ms (5%) |         |   1.01 MiB (1%) |        1085 |
| `["collect", "unordered", "basesize=32"]`           | 188.397 ms (5%) |         |   1.60 MiB (1%) |       15422 |
| `["findfirst", "n=1000", "foldl"]`                  | 581.001 ms (5%) |         |                 |             |
| `["findfirst", "n=1000", "reduce", "basesize=128"]` | 444.125 ms (5%) |         | 313.97 KiB (1%) |        4421 |
| `["findfirst", "n=1000", "reduce", "basesize=256"]` | 354.500 ms (5%) |         | 137.06 KiB (1%) |        1937 |
| `["findfirst", "n=1000", "reduce", "basesize=512"]` | 486.867 ms (5%) |         | 107.73 KiB (1%) |        1493 |
| `["findfirst", "n=400", "foldl"]`                   | 434.658 ms (5%) |         |                 |             |
| `["findfirst", "n=400", "reduce", "basesize=128"]`  | 224.250 ms (5%) |         | 377.30 KiB (1%) |        5393 |
| `["findfirst", "n=400", "reduce", "basesize=256"]`  | 227.436 ms (5%) |         | 200.67 KiB (1%) |        2867 |
| `["findfirst", "n=400", "reduce", "basesize=512"]`  | 297.432 ms (5%) |         | 139.36 KiB (1%) |        1987 |
| `["findfirst", "n=500", "foldl"]`                   |  75.447 ms (5%) |         |                 |             |
| `["findfirst", "n=500", "reduce", "basesize=128"]`  | 186.789 ms (5%) |         | 279.09 KiB (1%) |        3878 |
| `["findfirst", "n=500", "reduce", "basesize=256"]`  | 164.232 ms (5%) |         | 149.34 KiB (1%) |        2028 |
| `["findfirst", "n=500", "reduce", "basesize=512"]`  | 494.425 ms (5%) |         | 189.48 KiB (1%) |        2661 |
| `["overhead", "default"]`                           |  62.131 μs (5%) |         |  32.73 KiB (1%) |         418 |
| `["overhead", "stoppable=false"]`                   |  63.193 μs (5%) |         |  32.72 KiB (1%) |         417 |
| `["overhead", "stoppable=true"]`                    |  70.965 μs (5%) |         |  44.28 KiB (1%) |         611 |
| `["parallel_histogram", "assoc", "basesize=16384"]` |   2.538 ms (5%) |         | 728.91 KiB (1%) |          57 |
| `["parallel_histogram", "assoc", "basesize=4096"]`  |   3.325 ms (5%) |         |   2.32 MiB (1%) |         228 |
| `["parallel_histogram", "assoc", "basesize=8192"]`  |   2.897 ms (5%) |         |   1.42 MiB (1%) |         118 |
| `["parallel_histogram", "comm", "basesize=16384"]`  |   8.522 ms (5%) |         |   1.56 MiB (1%) |        1907 |
| `["parallel_histogram", "comm", "basesize=4096"]`   |  14.729 ms (5%) |         |   1.29 MiB (1%) |        8354 |
| `["parallel_histogram", "comm", "basesize=8192"]`   |  12.664 ms (5%) |         |   1.26 MiB (1%) |        7388 |
| `["parallel_histogram", "seq"]`                     |   4.507 ms (5%) |         | 364.16 KiB (1%) |          24 |
| `["partition_length_maximum", "rand", "foldl"]`     |  35.414 ms (5%) |         |                 |             |
| `["partition_length_maximum", "rand", "reduce"]`    |  17.741 ms (5%) |         |  736 bytes (1%) |          11 |
| `["splitby", "count", "foldl"]`                     |   1.710 ms (5%) |         |                 |             |
| `["splitby", "count", "man"]`                       |   1.281 ms (5%) |         |                 |             |
| `["splitby", "count", "reduce"]`                    | 784.597 μs (5%) |         |   1.06 KiB (1%) |          19 |
| `["sum", "random", "foldl"]`                        |  12.404 ms (5%) |         |                 |             |
| `["sum", "random", "reduce", "basesize=128"]`       |   6.385 ms (5%) |         |  74.19 KiB (1%) |        1104 |
| `["sum", "random", "reduce", "basesize=256"]`       |   6.306 ms (5%) |         |  36.81 KiB (1%) |         548 |
| `["sum", "random", "reduce", "basesize=512"]`       |   6.257 ms (5%) |         |  18.08 KiB (1%) |         269 |
| `["sum", "uniform", "foldl"]`                       |  12.294 ms (5%) |         |                 |             |
| `["sum", "uniform", "reduce", "basesize=128"]`      |   6.336 ms (5%) |         |  74.22 KiB (1%) |        1105 |
| `["sum", "uniform", "reduce", "basesize=256"]`      |   6.252 ms (5%) |         |  36.75 KiB (1%) |         546 |
| `["sum", "uniform", "reduce", "basesize=512"]`      |   6.205 ms (5%) |         |  18.02 KiB (1%) |         267 |
| `["sum", "valley", "foldl"]`                        |  12.547 ms (5%) |         |                 |             |
| `["sum", "valley", "reduce", "basesize=128"]`       |   6.460 ms (5%) |         |  74.19 KiB (1%) |        1104 |
| `["sum", "valley", "reduce", "basesize=256"]`       |   6.373 ms (5%) |         |  36.78 KiB (1%) |         547 |
| `["sum", "valley", "reduce", "basesize=512"]`       |   6.352 ms (5%) |         |  18.05 KiB (1%) |         268 |
| `["words", "nthreads=1"]`                           |  15.652 ms (5%) |         |  31.62 MiB (1%) |     1029452 |
| `["words", "nthreads=2"]`                           |   9.920 ms (5%) |         |  31.97 MiB (1%) |     1029488 |
| `["words", "nthreads=4"]`                           |  10.498 ms (5%) |         |  32.87 MiB (1%) |     1029681 |

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
      Ubuntu 24.04.3 LTS
  uname: Linux 6.14.0-1017-azure #17~24.04.1-Ubuntu SMP Mon Dec  1 20:10:50 UTC 2025 x86_64 x86_64
  CPU: AMD EPYC 9V74 80-Core Processor: 
              speed         user         nice          sys         idle          irq
       #1  2867 MHz       3006 s          0 s        160 s       4201 s          0 s
       #2  2866 MHz       2112 s          0 s        180 s       5071 s          0 s
       #3  2868 MHz       2487 s          0 s        160 s       4714 s          0 s
       #4  2877 MHz       2697 s          0 s        177 s       4497 s          0 s
       
  Memory: 15.615703582763672 GB (12016.33984375 MB free)
  Uptime: 740.45 sec
  Load Avg:  1.77  1.52  0.89
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-12.0.1 (ORCJIT, znver3)
```

---
# Baseline result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmark: 17 Feb 2026 - 02:56
* Package commit: 2a51f8d
* Julia commit: 742b9ab
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
| `["collect", "assoc", "basesize=1"]`                | 169.051 ms (5%) |         |   4.36 MiB (1%) |       32801 |
| `["collect", "assoc", "basesize=1024"]`             | 167.826 ms (5%) |         |   1.09 MiB (1%) |          54 |
| `["collect", "assoc", "basesize=32"]`               | 167.736 ms (5%) |         |   1.48 MiB (1%) |        1052 |
| `["collect", "seq"]`                                | 334.258 ms (5%) |         | 256.05 KiB (1%) |           2 |
| `["collect", "unordered", "basesize=1"]`            | 316.639 ms (5%) |         |  23.88 MiB (1%) |      412463 |
| `["collect", "unordered", "basesize=1024"]`         | 176.626 ms (5%) |         |   1.01 MiB (1%) |        1063 |
| `["collect", "unordered", "basesize=32"]`           | 188.610 ms (5%) |         |   1.60 MiB (1%) |       15371 |
| `["findfirst", "n=1000", "foldl"]`                  | 580.957 ms (5%) |         |                 |             |
| `["findfirst", "n=1000", "reduce", "basesize=128"]` | 517.567 ms (5%) |         | 357.53 KiB (1%) |        5033 |
| `["findfirst", "n=1000", "reduce", "basesize=256"]` | 380.284 ms (5%) |         | 151.00 KiB (1%) |        2116 |
| `["findfirst", "n=1000", "reduce", "basesize=512"]` | 486.011 ms (5%) |         | 107.73 KiB (1%) |        1493 |
| `["findfirst", "n=400", "foldl"]`                   | 434.592 ms (5%) |         |                 |             |
| `["findfirst", "n=400", "reduce", "basesize=128"]`  | 229.234 ms (5%) |         | 397.80 KiB (1%) |        5650 |
| `["findfirst", "n=400", "reduce", "basesize=256"]`  | 227.310 ms (5%) |         | 200.89 KiB (1%) |        2874 |
| `["findfirst", "n=400", "reduce", "basesize=512"]`  | 227.747 ms (5%) |         | 103.78 KiB (1%) |        1500 |
| `["findfirst", "n=500", "foldl"]`                   |  75.433 ms (5%) |         |                 |             |
| `["findfirst", "n=500", "reduce", "basesize=128"]`  | 170.628 ms (5%) |         | 257.75 KiB (1%) |        3610 |
| `["findfirst", "n=500", "reduce", "basesize=256"]`  |  64.491 ms (5%) |         |  70.47 KiB (1%) |         955 |
| `["findfirst", "n=500", "reduce", "basesize=512"]`  | 143.160 ms (5%) |         |  77.70 KiB (1%) |        1054 |
| `["overhead", "default"]`                           |  61.731 μs (5%) |         |  32.73 KiB (1%) |         418 |
| `["overhead", "stoppable=false"]`                   |  61.852 μs (5%) |         |  32.69 KiB (1%) |         416 |
| `["overhead", "stoppable=true"]`                    |  69.242 μs (5%) |         |  44.25 KiB (1%) |         610 |
| `["parallel_histogram", "assoc", "basesize=16384"]` |   2.557 ms (5%) |         | 728.91 KiB (1%) |          57 |
| `["parallel_histogram", "assoc", "basesize=4096"]`  |   3.255 ms (5%) |         |   1.79 MiB (1%) |         216 |
| `["parallel_histogram", "assoc", "basesize=8192"]`  |   2.900 ms (5%) |         |   1.42 MiB (1%) |         117 |
| `["parallel_histogram", "comm", "basesize=16384"]`  |   8.744 ms (5%) |         |   1.57 MiB (1%) |        2200 |
| `["parallel_histogram", "comm", "basesize=4096"]`   |  14.041 ms (5%) |         |   1.35 MiB (1%) |       10282 |
| `["parallel_histogram", "comm", "basesize=8192"]`   |  12.830 ms (5%) |         |   1.24 MiB (1%) |        6050 |
| `["parallel_histogram", "seq"]`                     |   4.582 ms (5%) |         | 364.16 KiB (1%) |          24 |
| `["partition_length_maximum", "rand", "foldl"]`     |  35.409 ms (5%) |         |                 |             |
| `["partition_length_maximum", "rand", "reduce"]`    |  17.742 ms (5%) |         |  736 bytes (1%) |          11 |
| `["splitby", "count", "foldl"]`                     |   1.731 ms (5%) |         |                 |             |
| `["splitby", "count", "man"]`                       |   1.276 ms (5%) |         |                 |             |
| `["splitby", "count", "reduce"]`                    | 850.354 μs (5%) |         |   1.09 KiB (1%) |          19 |
| `["sum", "random", "foldl"]`                        |  12.398 ms (5%) |         |                 |             |
| `["sum", "random", "reduce", "basesize=128"]`       |   6.353 ms (5%) |         |  74.22 KiB (1%) |        1105 |
| `["sum", "random", "reduce", "basesize=256"]`       |   6.303 ms (5%) |         |  36.75 KiB (1%) |         546 |
| `["sum", "random", "reduce", "basesize=512"]`       |   6.265 ms (5%) |         |  18.08 KiB (1%) |         269 |
| `["sum", "uniform", "foldl"]`                       |  12.289 ms (5%) |         |                 |             |
| `["sum", "uniform", "reduce", "basesize=128"]`      |   6.323 ms (5%) |         |  74.19 KiB (1%) |        1104 |
| `["sum", "uniform", "reduce", "basesize=256"]`      |   6.254 ms (5%) |         |  36.78 KiB (1%) |         547 |
| `["sum", "uniform", "reduce", "basesize=512"]`      |   6.210 ms (5%) |         |  18.05 KiB (1%) |         268 |
| `["sum", "valley", "foldl"]`                        |  12.549 ms (5%) |         |                 |             |
| `["sum", "valley", "reduce", "basesize=128"]`       |   6.460 ms (5%) |         |  74.16 KiB (1%) |        1103 |
| `["sum", "valley", "reduce", "basesize=256"]`       |   6.385 ms (5%) |         |  36.78 KiB (1%) |         547 |
| `["sum", "valley", "reduce", "basesize=512"]`       |   6.345 ms (5%) |         |  18.05 KiB (1%) |         268 |
| `["words", "nthreads=1"]`                           |  15.742 ms (5%) |         |  31.61 MiB (1%) |     1029960 |
| `["words", "nthreads=2"]`                           |  11.445 ms (5%) |         |  31.97 MiB (1%) |     1030033 |
| `["words", "nthreads=4"]`                           |  11.806 ms (5%) |         |  32.86 MiB (1%) |     1030176 |

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
      Ubuntu 24.04.3 LTS
  uname: Linux 6.14.0-1017-azure #17~24.04.1-Ubuntu SMP Mon Dec  1 20:10:50 UTC 2025 x86_64 x86_64
  CPU: AMD EPYC 9V74 80-Core Processor: 
              speed         user         nice          sys         idle          irq
       #1  2872 MHz       4340 s          0 s        222 s       5941 s          0 s
       #2  2870 MHz       3473 s          0 s        240 s       6787 s          0 s
       #3  2872 MHz       3329 s          0 s        214 s       6955 s          0 s
       #4  2870 MHz       4032 s          0 s        241 s       6238 s          0 s
       
  Memory: 15.615703582763672 GB (11944.49609375 MB free)
  Uptime: 1054.82 sec
  Load Avg:  1.59  1.61  1.12
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-12.0.1 (ORCJIT, znver3)
```

---
# Runtime information
| Runtime Info | |
|:--|:--|
| BLAS #threads | 4 |
| `BLAS.vendor()` | `openblas64` |
| `Sys.CPU_THREADS` | 4 |

`lscpu` output:

    Architecture:                            x86_64
    CPU op-mode(s):                          32-bit, 64-bit
    Address sizes:                           48 bits physical, 48 bits virtual
    Byte Order:                              Little Endian
    CPU(s):                                  4
    On-line CPU(s) list:                     0-3
    Vendor ID:                               AuthenticAMD
    Model name:                              AMD EPYC 9V74 80-Core Processor
    CPU family:                              25
    Model:                                   17
    Thread(s) per core:                      2
    Core(s) per socket:                      2
    Socket(s):                               1
    Stepping:                                1
    BogoMIPS:                                5192.30
    Flags:                                   fpu vme de pse tsc msr pae mce cx8 apic sep mtrr pge mca cmov pat pse36 clflush mmx fxsr sse sse2 ht syscall nx mmxext fxsr_opt pdpe1gb rdtscp lm constant_tsc rep_good nopl tsc_reliable nonstop_tsc cpuid extd_apicid aperfmperf tsc_known_freq pni pclmulqdq ssse3 fma cx16 pcid sse4_1 sse4_2 movbe popcnt aes xsave avx f16c rdrand hypervisor lahf_lm cmp_legacy svm cr8_legacy abm sse4a misalignsse 3dnowprefetch osvw topoext vmmcall fsgsbase bmi1 avx2 smep bmi2 erms invpcid rdseed adx smap clflushopt clwb sha_ni xsaveopt xsavec xgetbv1 xsaves user_shstk clzero xsaveerptr rdpru arat npt nrip_save tsc_scale vmcb_clean flushbyasid decodeassists pausefilter pfthreshold v_vmsave_vmload umip vaes vpclmulqdq rdpid fsrm
    Virtualization:                          AMD-V
    Hypervisor vendor:                       Microsoft
    Virtualization type:                     full
    L1d cache:                               64 KiB (2 instances)
    L1i cache:                               64 KiB (2 instances)
    L2 cache:                                2 MiB (2 instances)
    L3 cache:                                32 MiB (1 instance)
    NUMA node(s):                            1
    NUMA node0 CPU(s):                       0-3
    Vulnerability Gather data sampling:      Not affected
    Vulnerability Ghostwrite:                Not affected
    Vulnerability Indirect target selection: Not affected
    Vulnerability Itlb multihit:             Not affected
    Vulnerability L1tf:                      Not affected
    Vulnerability Mds:                       Not affected
    Vulnerability Meltdown:                  Not affected
    Vulnerability Mmio stale data:           Not affected
    Vulnerability Reg file data sampling:    Not affected
    Vulnerability Retbleed:                  Not affected
    Vulnerability Spec rstack overflow:      Vulnerable: Safe RET, no microcode
    Vulnerability Spec store bypass:         Vulnerable
    Vulnerability Spectre v1:                Mitigation; usercopy/swapgs barriers and __user pointer sanitization
    Vulnerability Spectre v2:                Mitigation; Retpolines; STIBP disabled; RSB filling; PBRSB-eIBRS Not affected; BHI Not affected
    Vulnerability Srbds:                     Not affected
    Vulnerability Tsa:                       Vulnerable: Clear CPU buffers attempted, no microcode
    Vulnerability Tsx async abort:           Not affected
    Vulnerability Vmscape:                   Not affected
    

| Cpu Property       | Value                                                      |
|:------------------ |:---------------------------------------------------------- |
| Brand              | AMD EPYC 9V74 80-Core Processor                            |
| Vendor             | :AMD                                                       |
| Architecture       | :Unknown                                                   |
| Model              | Family: 0xaf, Model: 0x11, Stepping: 0x01, Type: 0x00      |
| Cores              | 16 physical cores, 16 logical cores (on executing CPU)     |
|                    | No Hyperthreading hardware capability detected             |
| Clock Frequencies  | Not supported by CPU                                       |
| Data Cache         | Level 1:3 : (32, 1024, 32768) kbytes                       |
|                    | 64 byte cache line size                                    |
| Address Size       | 48 bits virtual, 48 bits physical                          |
| SIMD               | 256 bit = 32 byte max. SIMD vector size                    |
| Time Stamp Counter | TSC is accessible via `rdtsc`                              |
|                    | TSC runs at constant rate (invariant from clock frequency) |
| Perf. Monitoring   | Performance Monitoring Counters (PMC) are not supported    |
| Hypervisor         | Yes, Microsoft                                             |

