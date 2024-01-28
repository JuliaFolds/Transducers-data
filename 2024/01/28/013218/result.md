# Multi-thread benchmark result

* Pull request commit: [`0925517fe2555513e3a9b01ed994d4a1a204f566`](https://github.com/JuliaFolds/Transducers.jl/commit/0925517fe2555513e3a9b01ed994d4a1a204f566)
* Pull request: <https://github.com/JuliaFolds/Transducers.jl/pull/243> (Update */Manifest.toml)

# Judge result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmarks:
    - Target: 28 Jan 2024 - 01:27
    - Baseline: 28 Jan 2024 - 01:31
* Package commits:
    - Target: d987e3
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
| `["findfirst", "n=1000", "reduce", "basesize=128"]` |                1.31 (5%) :x: |                1.33 (1%) :x: |
| `["findfirst", "n=1000", "reduce", "basesize=256"]` |                1.11 (5%) :x: |                1.06 (1%) :x: |
| `["findfirst", "n=1000", "reduce", "basesize=512"]` | 0.50 (5%) :white_check_mark: | 0.57 (1%) :white_check_mark: |
| `["findfirst", "n=400", "reduce", "basesize=128"]`  |                   0.96 (5%)  | 0.95 (1%) :white_check_mark: |
| `["findfirst", "n=400", "reduce", "basesize=512"]`  |                1.20 (5%) :x: |                1.32 (1%) :x: |
| `["findfirst", "n=500", "reduce", "basesize=128"]`  |                1.64 (5%) :x: |                1.36 (1%) :x: |
| `["findfirst", "n=500", "reduce", "basesize=256"]`  | 0.76 (5%) :white_check_mark: | 0.70 (1%) :white_check_mark: |
| `["findfirst", "n=500", "reduce", "basesize=512"]`  |                1.06 (5%) :x: |                1.03 (1%) :x: |
| `["overhead", "stoppable=false"]`                   |                1.06 (5%) :x: |                   1.00 (1%)  |
| `["parallel_histogram", "assoc", "basesize=4096"]`  |                   1.03 (5%)  |                1.15 (1%) :x: |
| `["splitby", "count", "reduce"]`                    |                   0.99 (5%)  |                1.03 (1%) :x: |
| `["words", "nthreads=2"]`                           |                1.06 (5%) :x: |                   1.01 (1%)  |
| `["words", "nthreads=4"]`                           |                   1.05 (5%)  |                1.01 (1%) :x: |

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
      Ubuntu 22.04.3 LTS
  uname: Linux 6.2.0-1018-azure #18~22.04.1-Ubuntu SMP Tue Nov 21 19:25:02 UTC 2023 x86_64 x86_64
  CPU: AMD EPYC 7763 64-Core Processor: 
              speed         user         nice          sys         idle          irq
       #1  2445 MHz       2568 s          0 s        152 s       4202 s          0 s
       #2  3243 MHz       2433 s          0 s        176 s       4314 s          0 s
       #3  2617 MHz       2392 s          0 s        170 s       4359 s          0 s
       #4  2445 MHz       2704 s          0 s        178 s       4044 s          0 s
       
  Memory: 15.60690689086914 GB (12363.1953125 MB free)
  Uptime: 696.07 sec
  Load Avg:  1.7  1.5  0.87
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
      Ubuntu 22.04.3 LTS
  uname: Linux 6.2.0-1018-azure #18~22.04.1-Ubuntu SMP Tue Nov 21 19:25:02 UTC 2023 x86_64 x86_64
  CPU: AMD EPYC 7763 64-Core Processor: 
              speed         user         nice          sys         idle          irq
       #1  2609 MHz       3505 s          0 s        210 s       6096 s          0 s
       #2  2445 MHz       4049 s          0 s        226 s       5536 s          0 s
       #3  2445 MHz       3318 s          0 s        213 s       6278 s          0 s
       #4  3243 MHz       3808 s          0 s        227 s       5782 s          0 s
       
  Memory: 15.60690689086914 GB (12350.5859375 MB free)
  Uptime: 985.59 sec
  Load Avg:  1.74  1.62  1.1
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-12.0.1 (ORCJIT, znver3)
```

---
# Target result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmark: 28 Jan 2024 - 1:27
* Package commit: d987e3
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
| `["collect", "assoc", "basesize=1"]`                | 149.019 ms (5%) |         |   4.36 MiB (1%) |       32800 |
| `["collect", "assoc", "basesize=1024"]`             | 147.406 ms (5%) |         |   1.09 MiB (1%) |          53 |
| `["collect", "assoc", "basesize=32"]`               | 147.522 ms (5%) |         |   1.48 MiB (1%) |        1052 |
| `["collect", "seq"]`                                | 294.547 ms (5%) |         | 256.05 KiB (1%) |           2 |
| `["collect", "unordered", "basesize=1"]`            | 247.714 ms (5%) |         |  23.79 MiB (1%) |      409434 |
| `["collect", "unordered", "basesize=1024"]`         | 156.403 ms (5%) |         |   1.01 MiB (1%) |        1064 |
| `["collect", "unordered", "basesize=32"]`           | 163.475 ms (5%) |         |   1.60 MiB (1%) |       15167 |
| `["findfirst", "n=1000", "foldl"]`                  | 507.497 ms (5%) |         |                 |             |
| `["findfirst", "n=1000", "reduce", "basesize=128"]` | 396.290 ms (5%) |         | 338.47 KiB (1%) |        4697 |
| `["findfirst", "n=1000", "reduce", "basesize=256"]` | 376.527 ms (5%) |         | 166.56 KiB (1%) |        2333 |
| `["findfirst", "n=1000", "reduce", "basesize=512"]` | 395.823 ms (5%) |         |  96.75 KiB (1%) |        1346 |
| `["findfirst", "n=400", "foldl"]`                   | 378.839 ms (5%) |         |                 |             |
| `["findfirst", "n=400", "reduce", "basesize=128"]`  | 194.145 ms (5%) |         | 374.62 KiB (1%) |        5350 |
| `["findfirst", "n=400", "reduce", "basesize=256"]`  | 198.039 ms (5%) |         | 200.67 KiB (1%) |        2867 |
| `["findfirst", "n=400", "reduce", "basesize=512"]`  | 263.126 ms (5%) |         | 148.55 KiB (1%) |        2113 |
| `["findfirst", "n=500", "foldl"]`                   |  65.609 ms (5%) |         |                 |             |
| `["findfirst", "n=500", "reduce", "basesize=128"]`  | 159.862 ms (5%) |         | 270.11 KiB (1%) |        3747 |
| `["findfirst", "n=500", "reduce", "basesize=256"]`  |  87.505 ms (5%) |         |  93.88 KiB (1%) |        1282 |
| `["findfirst", "n=500", "reduce", "basesize=512"]`  |  88.639 ms (5%) |         |  56.81 KiB (1%) |         778 |
| `["overhead", "default"]`                           |  50.755 μs (5%) |         |  32.73 KiB (1%) |         418 |
| `["overhead", "stoppable=false"]`                   |  52.108 μs (5%) |         |  32.78 KiB (1%) |         419 |
| `["overhead", "stoppable=true"]`                    |  58.169 μs (5%) |         |  44.28 KiB (1%) |         611 |
| `["parallel_histogram", "assoc", "basesize=16384"]` |   2.381 ms (5%) |         | 728.91 KiB (1%) |          57 |
| `["parallel_histogram", "assoc", "basesize=4096"]`  |   3.015 ms (5%) |         |   2.05 MiB (1%) |         222 |
| `["parallel_histogram", "assoc", "basesize=8192"]`  |   2.653 ms (5%) |         |   1.42 MiB (1%) |         117 |
| `["parallel_histogram", "comm", "basesize=16384"]`  |   7.958 ms (5%) |         |   1.57 MiB (1%) |        1959 |
| `["parallel_histogram", "comm", "basesize=4096"]`   |  12.815 ms (5%) |         |   1.32 MiB (1%) |        9385 |
| `["parallel_histogram", "comm", "basesize=8192"]`   |  12.074 ms (5%) |         |   1.27 MiB (1%) |        7725 |
| `["parallel_histogram", "seq"]`                     |   4.252 ms (5%) |         | 364.16 KiB (1%) |          24 |
| `["partition_length_maximum", "rand", "foldl"]`     |  31.113 ms (5%) |         |                 |             |
| `["partition_length_maximum", "rand", "reduce"]`    |  15.575 ms (5%) |         |  736 bytes (1%) |          11 |
| `["splitby", "count", "foldl"]`                     |   1.481 ms (5%) |         |                 |             |
| `["splitby", "count", "man"]`                       |   1.158 ms (5%) |         |                 |             |
| `["splitby", "count", "reduce"]`                    | 720.537 μs (5%) |         |   1.09 KiB (1%) |          19 |
| `["sum", "random", "foldl"]`                        |  10.996 ms (5%) |         |                 |             |
| `["sum", "random", "reduce", "basesize=128"]`       |   5.634 ms (5%) |         |  74.17 KiB (1%) |        1104 |
| `["sum", "random", "reduce", "basesize=256"]`       |   5.566 ms (5%) |         |  36.70 KiB (1%) |         545 |
| `["sum", "random", "reduce", "basesize=512"]`       |   5.535 ms (5%) |         |  18.05 KiB (1%) |         268 |
| `["sum", "uniform", "foldl"]`                       |  10.861 ms (5%) |         |                 |             |
| `["sum", "uniform", "reduce", "basesize=128"]`      |   5.567 ms (5%) |         |  74.17 KiB (1%) |        1104 |
| `["sum", "uniform", "reduce", "basesize=256"]`      |   5.505 ms (5%) |         |  36.73 KiB (1%) |         546 |
| `["sum", "uniform", "reduce", "basesize=512"]`      |   5.466 ms (5%) |         |  17.97 KiB (1%) |         266 |
| `["sum", "valley", "foldl"]`                        |  11.105 ms (5%) |         |                 |             |
| `["sum", "valley", "reduce", "basesize=128"]`       |   5.684 ms (5%) |         |  74.08 KiB (1%) |        1101 |
| `["sum", "valley", "reduce", "basesize=256"]`       |   5.627 ms (5%) |         |  36.73 KiB (1%) |         546 |
| `["sum", "valley", "reduce", "basesize=512"]`       |   5.607 ms (5%) |         |  18.06 KiB (1%) |         269 |
| `["words", "nthreads=1"]`                           |  14.171 ms (5%) |         |  31.65 MiB (1%) |     1031543 |
| `["words", "nthreads=2"]`                           |   9.922 ms (5%) |         |  32.36 MiB (1%) |     1031639 |
| `["words", "nthreads=4"]`                           |  10.024 ms (5%) |         |  32.99 MiB (1%) |     1031788 |

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
      Ubuntu 22.04.3 LTS
  uname: Linux 6.2.0-1018-azure #18~22.04.1-Ubuntu SMP Tue Nov 21 19:25:02 UTC 2023 x86_64 x86_64
  CPU: AMD EPYC 7763 64-Core Processor: 
              speed         user         nice          sys         idle          irq
       #1  2445 MHz       2568 s          0 s        152 s       4202 s          0 s
       #2  3243 MHz       2433 s          0 s        176 s       4314 s          0 s
       #3  2617 MHz       2392 s          0 s        170 s       4359 s          0 s
       #4  2445 MHz       2704 s          0 s        178 s       4044 s          0 s
       
  Memory: 15.60690689086914 GB (12363.1953125 MB free)
  Uptime: 696.07 sec
  Load Avg:  1.7  1.5  0.87
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-12.0.1 (ORCJIT, znver3)
```

---
# Baseline result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmark: 28 Jan 2024 - 1:31
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
| `["collect", "assoc", "basesize=1"]`                | 148.589 ms (5%) |         |   4.36 MiB (1%) |       32800 |
| `["collect", "assoc", "basesize=1024"]`             | 147.467 ms (5%) |         |   1.09 MiB (1%) |          53 |
| `["collect", "assoc", "basesize=32"]`               | 147.575 ms (5%) |         |   1.48 MiB (1%) |        1052 |
| `["collect", "seq"]`                                | 294.615 ms (5%) |         | 256.05 KiB (1%) |           2 |
| `["collect", "unordered", "basesize=1"]`            | 245.744 ms (5%) |         |  23.88 MiB (1%) |      412497 |
| `["collect", "unordered", "basesize=1024"]`         | 156.284 ms (5%) |         |   1.01 MiB (1%) |        1123 |
| `["collect", "unordered", "basesize=32"]`           | 163.404 ms (5%) |         |   1.60 MiB (1%) |       15274 |
| `["findfirst", "n=1000", "foldl"]`                  | 507.500 ms (5%) |         |                 |             |
| `["findfirst", "n=1000", "reduce", "basesize=128"]` | 302.365 ms (5%) |         | 255.33 KiB (1%) |        3577 |
| `["findfirst", "n=1000", "reduce", "basesize=256"]` | 338.838 ms (5%) |         | 157.20 KiB (1%) |        2193 |
| `["findfirst", "n=1000", "reduce", "basesize=512"]` | 792.120 ms (5%) |         | 168.34 KiB (1%) |        2377 |
| `["findfirst", "n=400", "foldl"]`                   | 379.763 ms (5%) |         |                 |             |
| `["findfirst", "n=400", "reduce", "basesize=128"]`  | 202.685 ms (5%) |         | 395.78 KiB (1%) |        5622 |
| `["findfirst", "n=400", "reduce", "basesize=256"]`  | 196.986 ms (5%) |         | 199.97 KiB (1%) |        2859 |
| `["findfirst", "n=400", "reduce", "basesize=512"]`  | 219.925 ms (5%) |         | 112.59 KiB (1%) |        1622 |
| `["findfirst", "n=500", "foldl"]`                   |  65.241 ms (5%) |         |                 |             |
| `["findfirst", "n=500", "reduce", "basesize=128"]`  |  97.649 ms (5%) |         | 198.12 KiB (1%) |        2680 |
| `["findfirst", "n=500", "reduce", "basesize=256"]`  | 114.817 ms (5%) |         | 133.27 KiB (1%) |        1798 |
| `["findfirst", "n=500", "reduce", "basesize=512"]`  |  83.559 ms (5%) |         |  55.23 KiB (1%) |         754 |
| `["overhead", "default"]`                           |  52.028 μs (5%) |         |  32.70 KiB (1%) |         417 |
| `["overhead", "stoppable=false"]`                   |  49.162 μs (5%) |         |  32.78 KiB (1%) |         419 |
| `["overhead", "stoppable=true"]`                    |  57.848 μs (5%) |         |  44.28 KiB (1%) |         611 |
| `["parallel_histogram", "assoc", "basesize=16384"]` |   2.381 ms (5%) |         | 728.91 KiB (1%) |          57 |
| `["parallel_histogram", "assoc", "basesize=4096"]`  |   2.932 ms (5%) |         |   1.79 MiB (1%) |         216 |
| `["parallel_histogram", "assoc", "basesize=8192"]`  |   2.658 ms (5%) |         |   1.42 MiB (1%) |         117 |
| `["parallel_histogram", "comm", "basesize=16384"]`  |   7.890 ms (5%) |         |   1.56 MiB (1%) |        1909 |
| `["parallel_histogram", "comm", "basesize=4096"]`   |  12.558 ms (5%) |         |   1.32 MiB (1%) |        9522 |
| `["parallel_histogram", "comm", "basesize=8192"]`   |  12.145 ms (5%) |         |   1.28 MiB (1%) |        8124 |
| `["parallel_histogram", "seq"]`                     |   4.245 ms (5%) |         | 364.16 KiB (1%) |          24 |
| `["partition_length_maximum", "rand", "foldl"]`     |  31.104 ms (5%) |         |                 |             |
| `["partition_length_maximum", "rand", "reduce"]`    |  15.567 ms (5%) |         |  736 bytes (1%) |          11 |
| `["splitby", "count", "foldl"]`                     |   1.505 ms (5%) |         |                 |             |
| `["splitby", "count", "man"]`                       |   1.158 ms (5%) |         |                 |             |
| `["splitby", "count", "reduce"]`                    | 727.781 μs (5%) |         |   1.06 KiB (1%) |          18 |
| `["sum", "random", "foldl"]`                        |  11.034 ms (5%) |         |                 |             |
| `["sum", "random", "reduce", "basesize=128"]`       |   5.642 ms (5%) |         |  74.08 KiB (1%) |        1101 |
| `["sum", "random", "reduce", "basesize=256"]`       |   5.587 ms (5%) |         |  36.70 KiB (1%) |         545 |
| `["sum", "random", "reduce", "basesize=512"]`       |   5.548 ms (5%) |         |  18.11 KiB (1%) |         270 |
| `["sum", "uniform", "foldl"]`                       |  10.867 ms (5%) |         |                 |             |
| `["sum", "uniform", "reduce", "basesize=128"]`      |   5.580 ms (5%) |         |  74.14 KiB (1%) |        1103 |
| `["sum", "uniform", "reduce", "basesize=256"]`      |   5.525 ms (5%) |         |  36.77 KiB (1%) |         547 |
| `["sum", "uniform", "reduce", "basesize=512"]`      |   5.483 ms (5%) |         |  18.03 KiB (1%) |         268 |
| `["sum", "valley", "foldl"]`                        |  11.114 ms (5%) |         |                 |             |
| `["sum", "valley", "reduce", "basesize=128"]`       |   5.699 ms (5%) |         |  74.11 KiB (1%) |        1102 |
| `["sum", "valley", "reduce", "basesize=256"]`       |   5.641 ms (5%) |         |  36.70 KiB (1%) |         545 |
| `["sum", "valley", "reduce", "basesize=512"]`       |   5.608 ms (5%) |         |  18.06 KiB (1%) |         269 |
| `["words", "nthreads=1"]`                           |  14.034 ms (5%) |         |  31.36 MiB (1%) |     1021635 |
| `["words", "nthreads=2"]`                           |   9.391 ms (5%) |         |  32.08 MiB (1%) |     1021715 |
| `["words", "nthreads=4"]`                           |   9.592 ms (5%) |         |  32.52 MiB (1%) |     1021781 |

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
      Ubuntu 22.04.3 LTS
  uname: Linux 6.2.0-1018-azure #18~22.04.1-Ubuntu SMP Tue Nov 21 19:25:02 UTC 2023 x86_64 x86_64
  CPU: AMD EPYC 7763 64-Core Processor: 
              speed         user         nice          sys         idle          irq
       #1  2609 MHz       3505 s          0 s        210 s       6096 s          0 s
       #2  2445 MHz       4049 s          0 s        226 s       5536 s          0 s
       #3  2445 MHz       3318 s          0 s        213 s       6278 s          0 s
       #4  3243 MHz       3808 s          0 s        227 s       5782 s          0 s
       
  Memory: 15.60690689086914 GB (12350.5859375 MB free)
  Uptime: 985.59 sec
  Load Avg:  1.74  1.62  1.1
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

    Architecture:                       x86_64
    CPU op-mode(s):                     32-bit, 64-bit
    Address sizes:                      48 bits physical, 48 bits virtual
    Byte Order:                         Little Endian
    CPU(s):                             4
    On-line CPU(s) list:                0-3
    Vendor ID:                          AuthenticAMD
    Model name:                         AMD EPYC 7763 64-Core Processor
    CPU family:                         25
    Model:                              1
    Thread(s) per core:                 2
    Core(s) per socket:                 2
    Socket(s):                          1
    Stepping:                           1
    BogoMIPS:                           4890.85
    Flags:                              fpu vme de pse tsc msr pae mce cx8 apic sep mtrr pge mca cmov pat pse36 clflush mmx fxsr sse sse2 ht syscall nx mmxext fxsr_opt pdpe1gb rdtscp lm constant_tsc rep_good nopl tsc_reliable nonstop_tsc cpuid extd_apicid aperfmperf pni pclmulqdq ssse3 fma cx16 pcid sse4_1 sse4_2 movbe popcnt aes xsave avx f16c rdrand hypervisor lahf_lm cmp_legacy svm cr8_legacy abm sse4a misalignsse 3dnowprefetch osvw topoext invpcid_single vmmcall fsgsbase bmi1 avx2 smep bmi2 erms invpcid rdseed adx smap clflushopt clwb sha_ni xsaveopt xsavec xgetbv1 xsaves clzero xsaveerptr rdpru arat npt nrip_save tsc_scale vmcb_clean flushbyasid decodeassists pausefilter pfthreshold v_vmsave_vmload umip vaes vpclmulqdq rdpid fsrm
    Virtualization:                     AMD-V
    Hypervisor vendor:                  Microsoft
    Virtualization type:                full
    L1d cache:                          64 KiB (2 instances)
    L1i cache:                          64 KiB (2 instances)
    L2 cache:                           1 MiB (2 instances)
    L3 cache:                           32 MiB (1 instance)
    NUMA node(s):                       1
    NUMA node0 CPU(s):                  0-3
    Vulnerability Gather data sampling: Not affected
    Vulnerability Itlb multihit:        Not affected
    Vulnerability L1tf:                 Not affected
    Vulnerability Mds:                  Not affected
    Vulnerability Meltdown:             Not affected
    Vulnerability Mmio stale data:      Not affected
    Vulnerability Retbleed:             Not affected
    Vulnerability Spec rstack overflow: Mitigation; safe RET, no microcode
    Vulnerability Spec store bypass:    Vulnerable
    Vulnerability Spectre v1:           Mitigation; usercopy/swapgs barriers and __user pointer sanitization
    Vulnerability Spectre v2:           Mitigation; Retpolines, STIBP disabled, RSB filling, PBRSB-eIBRS Not affected
    Vulnerability Srbds:                Not affected
    Vulnerability Tsx async abort:      Not affected
    

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

