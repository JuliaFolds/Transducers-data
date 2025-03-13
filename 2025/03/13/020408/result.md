# Multi-thread benchmark result

* Pull request commit: [`80290c9fedb3de149b8b19a834850d857f5241e1`](https://github.com/JuliaFolds/Transducers.jl/commit/80290c9fedb3de149b8b19a834850d857f5241e1)
* Pull request: <https://github.com/JuliaFolds/Transducers.jl/pull/243> (Update */Manifest.toml)

# Judge result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmarks:
    - Target: 13 Mar 2025 - 01:58
    - Baseline: 13 Mar 2025 - 02:03
* Package commits:
    - Target: 7667bc
    - Baseline: 2a51f8
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
| `["findfirst", "n=1000", "reduce", "basesize=128"]` |                1.06 (5%) :x: |                1.06 (1%) :x: |
| `["findfirst", "n=1000", "reduce", "basesize=256"]` |                1.08 (5%) :x: |                1.04 (1%) :x: |
| `["findfirst", "n=1000", "reduce", "basesize=512"]` |                   1.00 (5%)  |                1.05 (1%) :x: |
| `["findfirst", "n=400", "reduce", "basesize=128"]`  |                   1.03 (5%)  |                1.02 (1%) :x: |
| `["findfirst", "n=400", "reduce", "basesize=512"]`  |                1.37 (5%) :x: |                1.36 (1%) :x: |
| `["findfirst", "n=500", "reduce", "basesize=128"]`  | 0.61 (5%) :white_check_mark: | 0.71 (1%) :white_check_mark: |
| `["findfirst", "n=500", "reduce", "basesize=256"]`  | 0.71 (5%) :white_check_mark: | 0.74 (1%) :white_check_mark: |
| `["findfirst", "n=500", "reduce", "basesize=512"]`  |                   1.00 (5%)  |                1.03 (1%) :x: |
| `["parallel_histogram", "comm", "basesize=16384"]`  |                1.07 (5%) :x: |                   1.00 (1%)  |
| `["parallel_histogram", "comm", "basesize=4096"]`   |                1.06 (5%) :x: | 0.98 (1%) :white_check_mark: |
| `["splitby", "count", "reduce"]`                    |                   1.00 (5%)  |                1.03 (1%) :x: |
| `["words", "nthreads=4"]`                           | 0.92 (5%) :white_check_mark: | 0.99 (1%) :white_check_mark: |

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
      Ubuntu 24.04.2 LTS
  uname: Linux 6.8.0-1021-azure #25-Ubuntu SMP Wed Jan 15 20:45:09 UTC 2025 x86_64 x86_64
  CPU: AMD EPYC 7763 64-Core Processor: 
              speed         user         nice          sys         idle          irq
       #1  3242 MHz       2389 s          0 s        195 s       4639 s          0 s
       #2  3241 MHz       3141 s          0 s        221 s       3844 s          0 s
       #3  3242 MHz       2549 s          0 s        193 s       4453 s          0 s
       #4  3241 MHz       2027 s          0 s        216 s       4913 s          0 s
       
  Memory: 15.61526870727539 GB (8532.0078125 MB free)
  Uptime: 729.04 sec
  Load Avg:  1.68  1.51  0.9
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
      Ubuntu 24.04.2 LTS
  uname: Linux 6.8.0-1021-azure #25-Ubuntu SMP Wed Jan 15 20:45:09 UTC 2025 x86_64 x86_64
  CPU: AMD EPYC 7763 64-Core Processor: 
              speed         user         nice          sys         idle          irq
       #1  3246 MHz       3418 s          0 s        254 s       6644 s          0 s
       #2  3242 MHz       4161 s          0 s        304 s       5835 s          0 s
       #3  3244 MHz       4104 s          0 s        254 s       5933 s          0 s
       #4  3245 MHz       3234 s          0 s        309 s       6709 s          0 s
       
  Memory: 15.61526870727539 GB (8578.4140625 MB free)
  Uptime: 1039.09 sec
  Load Avg:  1.76  1.68  1.16
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-12.0.1 (ORCJIT, znver3)
```

---
# Target result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmark: 13 Mar 2025 - 1:58
* Package commit: 7667bc
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
| `["collect", "assoc", "basesize=1"]`                | 149.895 ms (5%) |         |   4.36 MiB (1%) |       32800 |
| `["collect", "assoc", "basesize=1024"]`             | 148.219 ms (5%) |         |   1.09 MiB (1%) |          53 |
| `["collect", "assoc", "basesize=32"]`               | 148.376 ms (5%) |         |   1.48 MiB (1%) |        1052 |
| `["collect", "seq"]`                                | 296.059 ms (5%) |         | 256.05 KiB (1%) |           2 |
| `["collect", "unordered", "basesize=1"]`            | 244.564 ms (5%) |         |  23.69 MiB (1%) |      406007 |
| `["collect", "unordered", "basesize=1024"]`         | 158.444 ms (5%) |         |   1.01 MiB (1%) |        1053 |
| `["collect", "unordered", "basesize=32"]`           | 171.068 ms (5%) |         |   1.60 MiB (1%) |       15320 |
| `["findfirst", "n=1000", "foldl"]`                  | 509.275 ms (5%) |         |                 |             |
| `["findfirst", "n=1000", "reduce", "basesize=128"]` | 292.466 ms (5%) |         | 246.58 KiB (1%) |        3458 |
| `["findfirst", "n=1000", "reduce", "basesize=256"]` | 359.234 ms (5%) |         | 157.23 KiB (1%) |        2194 |
| `["findfirst", "n=1000", "reduce", "basesize=512"]` | 457.377 ms (5%) |         | 108.55 KiB (1%) |        1509 |
| `["findfirst", "n=400", "foldl"]`                   | 381.324 ms (5%) |         |                 |             |
| `["findfirst", "n=400", "reduce", "basesize=128"]`  | 201.977 ms (5%) |         | 393.44 KiB (1%) |        5587 |
| `["findfirst", "n=400", "reduce", "basesize=256"]`  | 199.140 ms (5%) |         | 200.89 KiB (1%) |        2874 |
| `["findfirst", "n=400", "reduce", "basesize=512"]`  | 302.219 ms (5%) |         | 152.75 KiB (1%) |        2195 |
| `["findfirst", "n=500", "foldl"]`                   |  65.658 ms (5%) |         |                 |             |
| `["findfirst", "n=500", "reduce", "basesize=128"]`  |  93.568 ms (5%) |         | 184.58 KiB (1%) |        2561 |
| `["findfirst", "n=500", "reduce", "basesize=256"]`  | 132.685 ms (5%) |         | 124.95 KiB (1%) |        1735 |
| `["findfirst", "n=500", "reduce", "basesize=512"]`  |  88.722 ms (5%) |         |  56.84 KiB (1%) |         779 |
| `["overhead", "default"]`                           |  49.914 μs (5%) |         |  32.73 KiB (1%) |         418 |
| `["overhead", "stoppable=false"]`                   |  52.558 μs (5%) |         |  32.75 KiB (1%) |         418 |
| `["overhead", "stoppable=true"]`                    |  57.338 μs (5%) |         |  44.25 KiB (1%) |         610 |
| `["parallel_histogram", "assoc", "basesize=16384"]` |   2.402 ms (5%) |         | 728.91 KiB (1%) |          57 |
| `["parallel_histogram", "assoc", "basesize=4096"]`  |   2.939 ms (5%) |         |   1.79 MiB (1%) |         215 |
| `["parallel_histogram", "assoc", "basesize=8192"]`  |   2.689 ms (5%) |         |   1.42 MiB (1%) |         117 |
| `["parallel_histogram", "comm", "basesize=16384"]`  |   8.351 ms (5%) |         |   1.56 MiB (1%) |        1842 |
| `["parallel_histogram", "comm", "basesize=4096"]`   |  13.043 ms (5%) |         |   1.31 MiB (1%) |        9053 |
| `["parallel_histogram", "comm", "basesize=8192"]`   |  11.244 ms (5%) |         |   1.27 MiB (1%) |        7923 |
| `["parallel_histogram", "seq"]`                     |   4.272 ms (5%) |         | 364.16 KiB (1%) |          24 |
| `["partition_length_maximum", "rand", "foldl"]`     |  31.316 ms (5%) |         |                 |             |
| `["partition_length_maximum", "rand", "reduce"]`    |  15.675 ms (5%) |         |  736 bytes (1%) |          11 |
| `["splitby", "count", "foldl"]`                     |   1.572 ms (5%) |         |                 |             |
| `["splitby", "count", "man"]`                       |   1.140 ms (5%) |         |                 |             |
| `["splitby", "count", "reduce"]`                    | 727.530 μs (5%) |         |   1.09 KiB (1%) |          19 |
| `["sum", "random", "foldl"]`                        |  11.129 ms (5%) |         |                 |             |
| `["sum", "random", "reduce", "basesize=128"]`       |   5.704 ms (5%) |         |  74.25 KiB (1%) |        1106 |
| `["sum", "random", "reduce", "basesize=256"]`       |   5.622 ms (5%) |         |  36.81 KiB (1%) |         548 |
| `["sum", "random", "reduce", "basesize=512"]`       |   5.601 ms (5%) |         |  18.02 KiB (1%) |         267 |
| `["sum", "uniform", "foldl"]`                       |  10.919 ms (5%) |         |                 |             |
| `["sum", "uniform", "reduce", "basesize=128"]`      |   5.597 ms (5%) |         |  74.16 KiB (1%) |        1103 |
| `["sum", "uniform", "reduce", "basesize=256"]`      |   5.547 ms (5%) |         |  36.78 KiB (1%) |         547 |
| `["sum", "uniform", "reduce", "basesize=512"]`      |   5.517 ms (5%) |         |  18.05 KiB (1%) |         268 |
| `["sum", "valley", "foldl"]`                        |  11.173 ms (5%) |         |                 |             |
| `["sum", "valley", "reduce", "basesize=128"]`       |   5.733 ms (5%) |         |  74.06 KiB (1%) |        1100 |
| `["sum", "valley", "reduce", "basesize=256"]`       |   5.664 ms (5%) |         |  36.78 KiB (1%) |         547 |
| `["sum", "valley", "reduce", "basesize=512"]`       |   5.638 ms (5%) |         |  18.08 KiB (1%) |         269 |
| `["words", "nthreads=1"]`                           |  14.037 ms (5%) |         |  31.66 MiB (1%) |     1030939 |
| `["words", "nthreads=2"]`                           |   9.210 ms (5%) |         |  32.37 MiB (1%) |     1031061 |
| `["words", "nthreads=4"]`                           |   9.343 ms (5%) |         |  32.82 MiB (1%) |     1031139 |

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
      Ubuntu 24.04.2 LTS
  uname: Linux 6.8.0-1021-azure #25-Ubuntu SMP Wed Jan 15 20:45:09 UTC 2025 x86_64 x86_64
  CPU: AMD EPYC 7763 64-Core Processor: 
              speed         user         nice          sys         idle          irq
       #1  3242 MHz       2389 s          0 s        195 s       4639 s          0 s
       #2  3241 MHz       3141 s          0 s        221 s       3844 s          0 s
       #3  3242 MHz       2549 s          0 s        193 s       4453 s          0 s
       #4  3241 MHz       2027 s          0 s        216 s       4913 s          0 s
       
  Memory: 15.61526870727539 GB (8532.0078125 MB free)
  Uptime: 729.04 sec
  Load Avg:  1.68  1.51  0.9
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-12.0.1 (ORCJIT, znver3)
```

---
# Baseline result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmark: 13 Mar 2025 - 2:3
* Package commit: 2a51f8
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
| `["collect", "assoc", "basesize=1"]`                | 149.777 ms (5%) |         |   4.36 MiB (1%) |       32800 |
| `["collect", "assoc", "basesize=1024"]`             | 148.408 ms (5%) |         |   1.09 MiB (1%) |          53 |
| `["collect", "assoc", "basesize=32"]`               | 148.362 ms (5%) |         |   1.48 MiB (1%) |        1052 |
| `["collect", "seq"]`                                | 296.026 ms (5%) |         | 256.05 KiB (1%) |           2 |
| `["collect", "unordered", "basesize=1"]`            | 248.872 ms (5%) |         |  23.68 MiB (1%) |      405924 |
| `["collect", "unordered", "basesize=1024"]`         | 158.106 ms (5%) |         |   1.01 MiB (1%) |        1093 |
| `["collect", "unordered", "basesize=32"]`           | 170.043 ms (5%) |         |   1.60 MiB (1%) |       15225 |
| `["findfirst", "n=1000", "foldl"]`                  | 508.311 ms (5%) |         |                 |             |
| `["findfirst", "n=1000", "reduce", "basesize=128"]` | 276.781 ms (5%) |         | 232.73 KiB (1%) |        3272 |
| `["findfirst", "n=1000", "reduce", "basesize=256"]` | 334.064 ms (5%) |         | 151.11 KiB (1%) |        2120 |
| `["findfirst", "n=1000", "reduce", "basesize=512"]` | 455.972 ms (5%) |         | 103.53 KiB (1%) |        1454 |
| `["findfirst", "n=400", "foldl"]`                   | 380.481 ms (5%) |         |                 |             |
| `["findfirst", "n=400", "reduce", "basesize=128"]`  | 196.179 ms (5%) |         | 384.55 KiB (1%) |        5467 |
| `["findfirst", "n=400", "reduce", "basesize=256"]`  | 199.323 ms (5%) |         | 200.86 KiB (1%) |        2873 |
| `["findfirst", "n=400", "reduce", "basesize=512"]`  | 221.051 ms (5%) |         | 112.59 KiB (1%) |        1622 |
| `["findfirst", "n=500", "foldl"]`                   |  65.501 ms (5%) |         |                 |             |
| `["findfirst", "n=500", "reduce", "basesize=128"]`  | 153.895 ms (5%) |         | 261.38 KiB (1%) |        3638 |
| `["findfirst", "n=500", "reduce", "basesize=256"]`  | 185.679 ms (5%) |         | 168.56 KiB (1%) |        2371 |
| `["findfirst", "n=500", "reduce", "basesize=512"]`  |  88.785 ms (5%) |         |  55.20 KiB (1%) |         753 |
| `["overhead", "default"]`                           |  50.104 μs (5%) |         |  32.73 KiB (1%) |         418 |
| `["overhead", "stoppable=false"]`                   |  52.398 μs (5%) |         |  32.72 KiB (1%) |         417 |
| `["overhead", "stoppable=true"]`                    |  58.139 μs (5%) |         |  44.25 KiB (1%) |         610 |
| `["parallel_histogram", "assoc", "basesize=16384"]` |   2.507 ms (5%) |         | 728.91 KiB (1%) |          57 |
| `["parallel_histogram", "assoc", "basesize=4096"]`  |   3.001 ms (5%) |         |   1.79 MiB (1%) |         216 |
| `["parallel_histogram", "assoc", "basesize=8192"]`  |   2.713 ms (5%) |         |   1.42 MiB (1%) |         117 |
| `["parallel_histogram", "comm", "basesize=16384"]`  |   7.799 ms (5%) |         |   1.56 MiB (1%) |        1694 |
| `["parallel_histogram", "comm", "basesize=4096"]`   |  12.320 ms (5%) |         |   1.34 MiB (1%) |       10125 |
| `["parallel_histogram", "comm", "basesize=8192"]`   |  11.577 ms (5%) |         |   1.28 MiB (1%) |        8228 |
| `["parallel_histogram", "seq"]`                     |   4.261 ms (5%) |         | 364.16 KiB (1%) |          24 |
| `["partition_length_maximum", "rand", "foldl"]`     |  31.303 ms (5%) |         |                 |             |
| `["partition_length_maximum", "rand", "reduce"]`    |  15.707 ms (5%) |         |  736 bytes (1%) |          11 |
| `["splitby", "count", "foldl"]`                     |   1.561 ms (5%) |         |                 |             |
| `["splitby", "count", "man"]`                       |   1.140 ms (5%) |         |                 |             |
| `["splitby", "count", "reduce"]`                    | 725.391 μs (5%) |         |   1.06 KiB (1%) |          18 |
| `["sum", "random", "foldl"]`                        |  11.042 ms (5%) |         |                 |             |
| `["sum", "random", "reduce", "basesize=128"]`       |   5.634 ms (5%) |         |  74.16 KiB (1%) |        1103 |
| `["sum", "random", "reduce", "basesize=256"]`       |   5.599 ms (5%) |         |  36.78 KiB (1%) |         547 |
| `["sum", "random", "reduce", "basesize=512"]`       |   5.563 ms (5%) |         |  18.05 KiB (1%) |         268 |
| `["sum", "uniform", "foldl"]`                       |  10.932 ms (5%) |         |                 |             |
| `["sum", "uniform", "reduce", "basesize=128"]`      |   5.588 ms (5%) |         |  74.16 KiB (1%) |        1103 |
| `["sum", "uniform", "reduce", "basesize=256"]`      |   5.541 ms (5%) |         |  36.81 KiB (1%) |         548 |
| `["sum", "uniform", "reduce", "basesize=512"]`      |   5.508 ms (5%) |         |  18.08 KiB (1%) |         269 |
| `["sum", "valley", "foldl"]`                        |  11.165 ms (5%) |         |                 |             |
| `["sum", "valley", "reduce", "basesize=128"]`       |   5.714 ms (5%) |         |  74.09 KiB (1%) |        1101 |
| `["sum", "valley", "reduce", "basesize=256"]`       |   5.657 ms (5%) |         |  36.78 KiB (1%) |         547 |
| `["sum", "valley", "reduce", "basesize=512"]`       |   5.626 ms (5%) |         |  18.08 KiB (1%) |         269 |
| `["words", "nthreads=1"]`                           |  14.475 ms (5%) |         |  31.81 MiB (1%) |     1036581 |
| `["words", "nthreads=2"]`                           |   9.649 ms (5%) |         |  32.52 MiB (1%) |     1036678 |
| `["words", "nthreads=4"]`                           |  10.203 ms (5%) |         |  33.15 MiB (1%) |     1036871 |

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
      Ubuntu 24.04.2 LTS
  uname: Linux 6.8.0-1021-azure #25-Ubuntu SMP Wed Jan 15 20:45:09 UTC 2025 x86_64 x86_64
  CPU: AMD EPYC 7763 64-Core Processor: 
              speed         user         nice          sys         idle          irq
       #1  3246 MHz       3418 s          0 s        254 s       6644 s          0 s
       #2  3242 MHz       4161 s          0 s        304 s       5835 s          0 s
       #3  3244 MHz       4104 s          0 s        254 s       5933 s          0 s
       #4  3245 MHz       3234 s          0 s        309 s       6709 s          0 s
       
  Memory: 15.61526870727539 GB (8578.4140625 MB free)
  Uptime: 1039.09 sec
  Load Avg:  1.76  1.68  1.16
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

    Architecture:                         x86_64
    CPU op-mode(s):                       32-bit, 64-bit
    Address sizes:                        48 bits physical, 48 bits virtual
    Byte Order:                           Little Endian
    CPU(s):                               4
    On-line CPU(s) list:                  0-3
    Vendor ID:                            AuthenticAMD
    Model name:                           AMD EPYC 7763 64-Core Processor
    CPU family:                           25
    Model:                                1
    Thread(s) per core:                   2
    Core(s) per socket:                   2
    Socket(s):                            1
    Stepping:                             1
    BogoMIPS:                             4890.84
    Flags:                                fpu vme de pse tsc msr pae mce cx8 apic sep mtrr pge mca cmov pat pse36 clflush mmx fxsr sse sse2 ht syscall nx mmxext fxsr_opt pdpe1gb rdtscp lm constant_tsc rep_good nopl tsc_reliable nonstop_tsc cpuid extd_apicid aperfmperf pni pclmulqdq ssse3 fma cx16 pcid sse4_1 sse4_2 movbe popcnt aes xsave avx f16c rdrand hypervisor lahf_lm cmp_legacy svm cr8_legacy abm sse4a misalignsse 3dnowprefetch osvw topoext vmmcall fsgsbase bmi1 avx2 smep bmi2 erms invpcid rdseed adx smap clflushopt clwb sha_ni xsaveopt xsavec xgetbv1 xsaves user_shstk clzero xsaveerptr rdpru arat npt nrip_save tsc_scale vmcb_clean flushbyasid decodeassists pausefilter pfthreshold v_vmsave_vmload umip vaes vpclmulqdq rdpid fsrm
    Virtualization:                       AMD-V
    Hypervisor vendor:                    Microsoft
    Virtualization type:                  full
    L1d cache:                            64 KiB (2 instances)
    L1i cache:                            64 KiB (2 instances)
    L2 cache:                             1 MiB (2 instances)
    L3 cache:                             32 MiB (1 instance)
    NUMA node(s):                         1
    NUMA node0 CPU(s):                    0-3
    Vulnerability Gather data sampling:   Not affected
    Vulnerability Itlb multihit:          Not affected
    Vulnerability L1tf:                   Not affected
    Vulnerability Mds:                    Not affected
    Vulnerability Meltdown:               Not affected
    Vulnerability Mmio stale data:        Not affected
    Vulnerability Reg file data sampling: Not affected
    Vulnerability Retbleed:               Not affected
    Vulnerability Spec rstack overflow:   Vulnerable: Safe RET, no microcode
    Vulnerability Spec store bypass:      Vulnerable
    Vulnerability Spectre v1:             Mitigation; usercopy/swapgs barriers and __user pointer sanitization
    Vulnerability Spectre v2:             Mitigation; Retpolines; STIBP disabled; RSB filling; PBRSB-eIBRS Not affected; BHI Not affected
    Vulnerability Srbds:                  Not affected
    Vulnerability Tsx async abort:        Not affected
    

| Cpu Property       | Value                                                      |
|:------------------ |:---------------------------------------------------------- |
| Brand              | AMD EPYC 7763 64-Core Processor                            |
| Vendor             | :AMD                                                       |
| Architecture       | :Unknown                                                   |
| Model              | Family: 0xaf, Model: 0x01, Stepping: 0x01, Type: 0x00      |
| Cores              | 16 physical cores, 16 logical cores (on executing CPU)     |
|                    | No Hyperthreading hardware capability detected             |
| Clock Frequencies  | Not supported by CPU                                       |
| Data Cache         | Level 1:3 : (32, 512, 32768) kbytes                        |
|                    | 64 byte cache line size                                    |
| Address Size       | 48 bits virtual, 48 bits physical                          |
| SIMD               | 256 bit = 32 byte max. SIMD vector size                    |
| Time Stamp Counter | TSC is accessible via `rdtsc`                              |
|                    | TSC runs at constant rate (invariant from clock frequency) |
| Perf. Monitoring   | Performance Monitoring Counters (PMC) are not supported    |
| Hypervisor         | Yes, Microsoft                                             |

