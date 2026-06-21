# Multi-thread benchmark result

* Pull request commit: [`f2bce8704dcbb164546ae49e3c8010bd1054e447`](https://github.com/JuliaFolds/Transducers.jl/commit/f2bce8704dcbb164546ae49e3c8010bd1054e447)
* Pull request: <https://github.com/JuliaFolds/Transducers.jl/pull/243> (Update */Manifest.toml)

# Judge result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmarks:
    - Target: 21 Jun 2026 - 05:06
    - Baseline: 21 Jun 2026 - 05:11
* Package commits:
    - Target: 22d51cf
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
| `["findfirst", "n=1000", "reduce", "basesize=128"]` |                1.42 (5%) :x: |                1.35 (1%) :x: |
| `["findfirst", "n=400", "reduce", "basesize=128"]`  |                   0.97 (5%)  | 0.96 (1%) :white_check_mark: |
| `["findfirst", "n=400", "reduce", "basesize=256"]`  |                   1.02 (5%)  |                1.03 (1%) :x: |
| `["findfirst", "n=400", "reduce", "basesize=512"]`  |                   1.05 (5%)  |                1.08 (1%) :x: |
| `["findfirst", "n=500", "reduce", "basesize=128"]`  |                1.25 (5%) :x: |                1.20 (1%) :x: |
| `["findfirst", "n=500", "reduce", "basesize=256"]`  | 0.34 (5%) :white_check_mark: | 0.47 (1%) :white_check_mark: |
| `["findfirst", "n=500", "reduce", "basesize=512"]`  | 0.85 (5%) :white_check_mark: | 0.91 (1%) :white_check_mark: |
| `["parallel_histogram", "assoc", "basesize=4096"]`  |                1.06 (5%) :x: |                1.15 (1%) :x: |
| `["parallel_histogram", "comm", "basesize=4096"]`   |                   0.97 (5%)  | 0.99 (1%) :white_check_mark: |
| `["splitby", "count", "foldl"]`                     | 0.89 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["splitby", "count", "reduce"]`                    |                   0.99 (5%)  |                1.03 (1%) :x: |

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
      Ubuntu 24.04.4 LTS
  uname: Linux 6.17.0-1018-azure #18~24.04.1-Ubuntu SMP Thu May 28 16:39:11 UTC 2026 x86_64 x86_64
  CPU: AMD EPYC 7763 64-Core Processor: 
              speed         user         nice          sys         idle          irq
       #1  3248 MHz       2647 s          0 s        181 s       3690 s          0 s
       #2  3245 MHz       2079 s          0 s        186 s       4234 s          0 s
       #3  3244 MHz       2358 s          0 s        139 s       4013 s          0 s
       #4  3243 MHz       2860 s          0 s        165 s       3503 s          0 s
       
  Memory: 15.614940643310547 GB (12269.70703125 MB free)
  Uptime: 656.5 sec
  Load Avg:  1.6  1.46  0.85
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
      Ubuntu 24.04.4 LTS
  uname: Linux 6.17.0-1018-azure #18~24.04.1-Ubuntu SMP Thu May 28 16:39:11 UTC 2026 x86_64 x86_64
  CPU: AMD EPYC 7763 64-Core Processor: 
              speed         user         nice          sys         idle          irq
       #1  3244 MHz       3698 s          0 s        226 s       5652 s          0 s
       #2  3250 MHz       3291 s          0 s        262 s       6004 s          0 s
       #3  3245 MHz       3741 s          0 s        189 s       5643 s          0 s
       #4  3245 MHz       3991 s          0 s        232 s       5367 s          0 s
       
  Memory: 15.614940643310547 GB (12154.203125 MB free)
  Uptime: 963.36 sec
  Load Avg:  1.63  1.57  1.08
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-12.0.1 (ORCJIT, znver3)
```

---
# Target result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmark: 21 Jun 2026 - 05:06
* Package commit: 22d51cf
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
| `["collect", "assoc", "basesize=1"]`                | 150.177 ms (5%) |         |   4.36 MiB (1%) |       32800 |
| `["collect", "assoc", "basesize=1024"]`             | 148.578 ms (5%) |         |   1.09 MiB (1%) |          53 |
| `["collect", "assoc", "basesize=32"]`               | 148.706 ms (5%) |         |   1.48 MiB (1%) |        1052 |
| `["collect", "seq"]`                                | 296.404 ms (5%) |         | 256.05 KiB (1%) |           2 |
| `["collect", "unordered", "basesize=1"]`            | 253.299 ms (5%) |         |  23.71 MiB (1%) |      406760 |
| `["collect", "unordered", "basesize=1024"]`         | 158.756 ms (5%) |         |   1.01 MiB (1%) |        1198 |
| `["collect", "unordered", "basesize=32"]`           | 169.516 ms (5%) |         |   1.60 MiB (1%) |       15302 |
| `["findfirst", "n=1000", "foldl"]`                  | 509.746 ms (5%) |         |                 |             |
| `["findfirst", "n=1000", "reduce", "basesize=128"]` | 394.833 ms (5%) |         | 313.17 KiB (1%) |        4408 |
| `["findfirst", "n=1000", "reduce", "basesize=256"]` | 341.664 ms (5%) |         | 157.20 KiB (1%) |        2193 |
| `["findfirst", "n=1000", "reduce", "basesize=512"]` | 469.275 ms (5%) |         | 103.62 KiB (1%) |        1457 |
| `["findfirst", "n=400", "foldl"]`                   | 381.484 ms (5%) |         |                 |             |
| `["findfirst", "n=400", "reduce", "basesize=128"]`  | 195.743 ms (5%) |         | 380.02 KiB (1%) |        5415 |
| `["findfirst", "n=400", "reduce", "basesize=256"]`  | 199.814 ms (5%) |         | 200.80 KiB (1%) |        2871 |
| `["findfirst", "n=400", "reduce", "basesize=512"]`  | 231.941 ms (5%) |         | 121.17 KiB (1%) |        1735 |
| `["findfirst", "n=500", "foldl"]`                   |  66.220 ms (5%) |         |                 |             |
| `["findfirst", "n=500", "reduce", "basesize=128"]`  | 163.997 ms (5%) |         | 279.09 KiB (1%) |        3878 |
| `["findfirst", "n=500", "reduce", "basesize=256"]`  |  57.667 ms (5%) |         |  74.34 KiB (1%) |        1012 |
| `["findfirst", "n=500", "reduce", "basesize=512"]`  |  81.100 ms (5%) |         |  54.44 KiB (1%) |         746 |
| `["overhead", "default"]`                           |  51.808 μs (5%) |         |  32.73 KiB (1%) |         418 |
| `["overhead", "stoppable=false"]`                   |  52.920 μs (5%) |         |  32.75 KiB (1%) |         418 |
| `["overhead", "stoppable=true"]`                    |  57.498 μs (5%) |         |  44.25 KiB (1%) |         610 |
| `["parallel_histogram", "assoc", "basesize=16384"]` |   2.403 ms (5%) |         | 728.91 KiB (1%) |          57 |
| `["parallel_histogram", "assoc", "basesize=4096"]`  |   3.137 ms (5%) |         |   2.05 MiB (1%) |         222 |
| `["parallel_histogram", "assoc", "basesize=8192"]`  |   2.705 ms (5%) |         |   1.42 MiB (1%) |         118 |
| `["parallel_histogram", "comm", "basesize=16384"]`  |   8.770 ms (5%) |         |   1.60 MiB (1%) |        2960 |
| `["parallel_histogram", "comm", "basesize=4096"]`   |  12.905 ms (5%) |         |   1.34 MiB (1%) |        9984 |
| `["parallel_histogram", "comm", "basesize=8192"]`   |  11.739 ms (5%) |         |   1.30 MiB (1%) |        8179 |
| `["parallel_histogram", "seq"]`                     |   4.271 ms (5%) |         | 364.16 KiB (1%) |          24 |
| `["partition_length_maximum", "rand", "foldl"]`     |  31.389 ms (5%) |         |                 |             |
| `["partition_length_maximum", "rand", "reduce"]`    |  15.722 ms (5%) |         |  704 bytes (1%) |          10 |
| `["splitby", "count", "foldl"]`                     |   1.552 ms (5%) |         |                 |             |
| `["splitby", "count", "man"]`                       |   1.167 ms (5%) |         |                 |             |
| `["splitby", "count", "reduce"]`                    | 719.554 μs (5%) |         |   1.06 KiB (1%) |          18 |
| `["sum", "random", "foldl"]`                        |  11.128 ms (5%) |         |                 |             |
| `["sum", "random", "reduce", "basesize=128"]`       |   5.714 ms (5%) |         |  74.12 KiB (1%) |        1102 |
| `["sum", "random", "reduce", "basesize=256"]`       |   5.655 ms (5%) |         |  36.81 KiB (1%) |         548 |
| `["sum", "random", "reduce", "basesize=512"]`       |   5.611 ms (5%) |         |  18.08 KiB (1%) |         269 |
| `["sum", "uniform", "foldl"]`                       |  10.945 ms (5%) |         |                 |             |
| `["sum", "uniform", "reduce", "basesize=128"]`      |   5.624 ms (5%) |         |  74.12 KiB (1%) |        1102 |
| `["sum", "uniform", "reduce", "basesize=256"]`      |   5.560 ms (5%) |         |  36.81 KiB (1%) |         548 |
| `["sum", "uniform", "reduce", "basesize=512"]`      |   5.523 ms (5%) |         |  18.08 KiB (1%) |         269 |
| `["sum", "valley", "foldl"]`                        |  11.180 ms (5%) |         |                 |             |
| `["sum", "valley", "reduce", "basesize=128"]`       |   5.736 ms (5%) |         |  74.06 KiB (1%) |        1100 |
| `["sum", "valley", "reduce", "basesize=256"]`       |   5.685 ms (5%) |         |  36.78 KiB (1%) |         547 |
| `["sum", "valley", "reduce", "basesize=512"]`       |   5.659 ms (5%) |         |  18.08 KiB (1%) |         269 |
| `["words", "nthreads=1"]`                           |  14.813 ms (5%) |         |  31.61 MiB (1%) |     1029454 |
| `["words", "nthreads=2"]`                           |   9.518 ms (5%) |         |  31.97 MiB (1%) |     1029490 |
| `["words", "nthreads=4"]`                           |  10.227 ms (5%) |         |  32.68 MiB (1%) |     1029562 |

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
      Ubuntu 24.04.4 LTS
  uname: Linux 6.17.0-1018-azure #18~24.04.1-Ubuntu SMP Thu May 28 16:39:11 UTC 2026 x86_64 x86_64
  CPU: AMD EPYC 7763 64-Core Processor: 
              speed         user         nice          sys         idle          irq
       #1  3248 MHz       2647 s          0 s        181 s       3690 s          0 s
       #2  3245 MHz       2079 s          0 s        186 s       4234 s          0 s
       #3  3244 MHz       2358 s          0 s        139 s       4013 s          0 s
       #4  3243 MHz       2860 s          0 s        165 s       3503 s          0 s
       
  Memory: 15.614940643310547 GB (12269.70703125 MB free)
  Uptime: 656.5 sec
  Load Avg:  1.6  1.46  0.85
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-12.0.1 (ORCJIT, znver3)
```

---
# Baseline result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmark: 21 Jun 2026 - 05:11
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
| `["collect", "assoc", "basesize=1"]`                | 150.160 ms (5%) |         |   4.36 MiB (1%) |       32801 |
| `["collect", "assoc", "basesize=1024"]`             | 148.850 ms (5%) |         |   1.09 MiB (1%) |          53 |
| `["collect", "assoc", "basesize=32"]`               | 148.675 ms (5%) |         |   1.48 MiB (1%) |        1053 |
| `["collect", "seq"]`                                | 296.444 ms (5%) |         | 256.05 KiB (1%) |           2 |
| `["collect", "unordered", "basesize=1"]`            | 252.079 ms (5%) |         |  23.72 MiB (1%) |      407088 |
| `["collect", "unordered", "basesize=1024"]`         | 158.314 ms (5%) |         |   1.01 MiB (1%) |        1083 |
| `["collect", "unordered", "basesize=32"]`           | 168.391 ms (5%) |         |   1.60 MiB (1%) |       15392 |
| `["findfirst", "n=1000", "foldl"]`                  | 509.736 ms (5%) |         |                 |             |
| `["findfirst", "n=1000", "reduce", "basesize=128"]` | 277.719 ms (5%) |         | 232.73 KiB (1%) |        3272 |
| `["findfirst", "n=1000", "reduce", "basesize=256"]` | 341.796 ms (5%) |         | 157.20 KiB (1%) |        2193 |
| `["findfirst", "n=1000", "reduce", "basesize=512"]` | 469.565 ms (5%) |         | 103.62 KiB (1%) |        1457 |
| `["findfirst", "n=400", "foldl"]`                   | 381.478 ms (5%) |         |                 |             |
| `["findfirst", "n=400", "reduce", "basesize=128"]`  | 202.064 ms (5%) |         | 396.78 KiB (1%) |        5628 |
| `["findfirst", "n=400", "reduce", "basesize=256"]`  | 196.005 ms (5%) |         | 195.25 KiB (1%) |        2797 |
| `["findfirst", "n=400", "reduce", "basesize=512"]`  | 221.337 ms (5%) |         | 112.56 KiB (1%) |        1621 |
| `["findfirst", "n=500", "foldl"]`                   |  66.207 ms (5%) |         |                 |             |
| `["findfirst", "n=500", "reduce", "basesize=128"]`  | 130.861 ms (5%) |         | 231.92 KiB (1%) |        3194 |
| `["findfirst", "n=500", "reduce", "basesize=256"]`  | 169.150 ms (5%) |         | 156.86 KiB (1%) |        2181 |
| `["findfirst", "n=500", "reduce", "basesize=512"]`  |  95.692 ms (5%) |         |  59.84 KiB (1%) |         819 |
| `["overhead", "default"]`                           |  52.318 μs (5%) |         |  32.73 KiB (1%) |         418 |
| `["overhead", "stoppable=false"]`                   |  51.727 μs (5%) |         |  32.75 KiB (1%) |         418 |
| `["overhead", "stoppable=true"]`                    |  57.678 μs (5%) |         |  44.25 KiB (1%) |         610 |
| `["parallel_histogram", "assoc", "basesize=16384"]` |   2.401 ms (5%) |         | 728.91 KiB (1%) |          57 |
| `["parallel_histogram", "assoc", "basesize=4096"]`  |   2.970 ms (5%) |         |   1.79 MiB (1%) |         216 |
| `["parallel_histogram", "assoc", "basesize=8192"]`  |   2.695 ms (5%) |         |   1.42 MiB (1%) |         117 |
| `["parallel_histogram", "comm", "basesize=16384"]`  |   8.710 ms (5%) |         |   1.59 MiB (1%) |        2644 |
| `["parallel_histogram", "comm", "basesize=4096"]`   |  13.366 ms (5%) |         |   1.36 MiB (1%) |       10632 |
| `["parallel_histogram", "comm", "basesize=8192"]`   |  11.806 ms (5%) |         |   1.30 MiB (1%) |        8179 |
| `["parallel_histogram", "seq"]`                     |   4.269 ms (5%) |         | 364.16 KiB (1%) |          24 |
| `["partition_length_maximum", "rand", "foldl"]`     |  31.367 ms (5%) |         |                 |             |
| `["partition_length_maximum", "rand", "reduce"]`    |  15.709 ms (5%) |         |  704 bytes (1%) |          10 |
| `["splitby", "count", "foldl"]`                     |   1.746 ms (5%) |         |                 |             |
| `["splitby", "count", "man"]`                       |   1.168 ms (5%) |         |                 |             |
| `["splitby", "count", "reduce"]`                    | 726.077 μs (5%) |         |   1.03 KiB (1%) |          18 |
| `["sum", "random", "foldl"]`                        |  11.091 ms (5%) |         |                 |             |
| `["sum", "random", "reduce", "basesize=128"]`       |   5.666 ms (5%) |         |  74.16 KiB (1%) |        1103 |
| `["sum", "random", "reduce", "basesize=256"]`       |   5.616 ms (5%) |         |  36.81 KiB (1%) |         548 |
| `["sum", "random", "reduce", "basesize=512"]`       |   5.592 ms (5%) |         |  18.11 KiB (1%) |         270 |
| `["sum", "uniform", "foldl"]`                       |  10.972 ms (5%) |         |                 |             |
| `["sum", "uniform", "reduce", "basesize=128"]`      |   5.601 ms (5%) |         |  74.19 KiB (1%) |        1104 |
| `["sum", "uniform", "reduce", "basesize=256"]`      |   5.557 ms (5%) |         |  36.78 KiB (1%) |         547 |
| `["sum", "uniform", "reduce", "basesize=512"]`      |   5.516 ms (5%) |         |  18.08 KiB (1%) |         269 |
| `["sum", "valley", "foldl"]`                        |  11.181 ms (5%) |         |                 |             |
| `["sum", "valley", "reduce", "basesize=128"]`       |   5.738 ms (5%) |         |  74.09 KiB (1%) |        1101 |
| `["sum", "valley", "reduce", "basesize=256"]`       |   5.679 ms (5%) |         |  36.78 KiB (1%) |         547 |
| `["sum", "valley", "reduce", "basesize=512"]`       |   5.656 ms (5%) |         |  18.08 KiB (1%) |         269 |
| `["words", "nthreads=1"]`                           |  14.829 ms (5%) |         |  31.53 MiB (1%) |     1027365 |
| `["words", "nthreads=2"]`                           |   9.661 ms (5%) |         |  32.24 MiB (1%) |     1027455 |
| `["words", "nthreads=4"]`                           |   9.895 ms (5%) |         |  32.69 MiB (1%) |     1027537 |

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
      Ubuntu 24.04.4 LTS
  uname: Linux 6.17.0-1018-azure #18~24.04.1-Ubuntu SMP Thu May 28 16:39:11 UTC 2026 x86_64 x86_64
  CPU: AMD EPYC 7763 64-Core Processor: 
              speed         user         nice          sys         idle          irq
       #1  3244 MHz       3698 s          0 s        226 s       5652 s          0 s
       #2  3250 MHz       3291 s          0 s        262 s       6004 s          0 s
       #3  3245 MHz       3741 s          0 s        189 s       5643 s          0 s
       #4  3245 MHz       3991 s          0 s        232 s       5367 s          0 s
       
  Memory: 15.614940643310547 GB (12154.203125 MB free)
  Uptime: 963.36 sec
  Load Avg:  1.63  1.57  1.08
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
    Model name:                              AMD EPYC 7763 64-Core Processor
    CPU family:                              25
    Model:                                   1
    Thread(s) per core:                      2
    Core(s) per socket:                      2
    Socket(s):                               1
    Stepping:                                1
    BogoMIPS:                                4890.86
    Flags:                                   fpu vme de pse tsc msr pae mce cx8 apic sep mtrr pge mca cmov pat pse36 clflush mmx fxsr sse sse2 ht syscall nx mmxext fxsr_opt pdpe1gb rdtscp lm constant_tsc rep_good nopl tsc_reliable nonstop_tsc cpuid extd_apicid aperfmperf tsc_known_freq pni pclmulqdq ssse3 fma cx16 pcid sse4_1 sse4_2 movbe popcnt aes xsave avx f16c rdrand hypervisor lahf_lm cmp_legacy svm cr8_legacy abm sse4a misalignsse 3dnowprefetch osvw topoext vmmcall fsgsbase bmi1 avx2 smep bmi2 erms invpcid rdseed adx smap clflushopt clwb sha_ni xsaveopt xsavec xgetbv1 xsaves user_shstk clzero xsaveerptr rdpru arat npt nrip_save tsc_scale vmcb_clean flushbyasid decodeassists pausefilter pfthreshold v_vmsave_vmload umip vaes vpclmulqdq rdpid fsrm
    Virtualization:                          AMD-V
    Hypervisor vendor:                       Microsoft
    Virtualization type:                     full
    L1d cache:                               64 KiB (2 instances)
    L1i cache:                               64 KiB (2 instances)
    L2 cache:                                1 MiB (2 instances)
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
    Vulnerability Old microcode:             Not affected
    Vulnerability Reg file data sampling:    Not affected
    Vulnerability Retbleed:                  Not affected
    Vulnerability Spec rstack overflow:      Vulnerable: Safe RET, no microcode
    Vulnerability Spec store bypass:         Vulnerable
    Vulnerability Spectre v1:                Mitigation; usercopy/swapgs barriers and __user pointer sanitization
    Vulnerability Spectre v2:                Mitigation; Retpolines; STIBP disabled; RSB filling; PBRSB-eIBRS Not affected; BHI Not affected
    Vulnerability Srbds:                     Not affected
    Vulnerability Tsa:                       Vulnerable: No microcode
    Vulnerability Tsx async abort:           Not affected
    Vulnerability Vmscape:                   Not affected
    

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

