# Multi-thread benchmark result

* Pull request commit: [`32edf7a74b0ac1396af2d862d8b6d3cf9e61939d`](https://github.com/JuliaFolds/Transducers.jl/commit/32edf7a74b0ac1396af2d862d8b6d3cf9e61939d)
* Pull request: <https://github.com/JuliaFolds/Transducers.jl/pull/243> (Update */Manifest.toml)

# Judge result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmarks:
    - Target: 11 Jun 2026 - 04:38
    - Baseline: 11 Jun 2026 - 04:43
* Package commits:
    - Target: 9efe8c4
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

| ID                                                  | time ratio    | memory ratio                 |
|-----------------------------------------------------|---------------|------------------------------|
| `["findfirst", "n=1000", "reduce", "basesize=128"]` |    0.99 (5%)  | 0.98 (1%) :white_check_mark: |
| `["findfirst", "n=1000", "reduce", "basesize=256"]` | 1.33 (5%) :x: |                1.17 (1%) :x: |
| `["findfirst", "n=400", "reduce", "basesize=128"]`  |    1.04 (5%)  |                1.05 (1%) :x: |
| `["findfirst", "n=400", "reduce", "basesize=256"]`  |    1.01 (5%)  |                1.05 (1%) :x: |
| `["findfirst", "n=400", "reduce", "basesize=512"]`  | 1.23 (5%) :x: |                1.25 (1%) :x: |
| `["findfirst", "n=500", "reduce", "basesize=128"]`  | 1.21 (5%) :x: |                1.13 (1%) :x: |
| `["findfirst", "n=500", "reduce", "basesize=256"]`  | 1.19 (5%) :x: |                1.08 (1%) :x: |
| `["findfirst", "n=500", "reduce", "basesize=512"]`  | 3.63 (5%) :x: |                2.34 (1%) :x: |
| `["parallel_histogram", "comm", "basesize=16384"]`  | 1.14 (5%) :x: |                1.01 (1%) :x: |
| `["parallel_histogram", "comm", "basesize=4096"]`   | 1.10 (5%) :x: |                1.02 (1%) :x: |
| `["parallel_histogram", "comm", "basesize=8192"]`   |    0.97 (5%)  |                1.02 (1%) :x: |

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
  uname: Linux 6.17.0-1015-azure #15~24.04.1-Ubuntu SMP Wed May  6 22:37:49 UTC 2026 x86_64 x86_64
  CPU: AMD EPYC 9V74 80-Core Processor: 
              speed         user         nice          sys         idle          irq
       #1  2862 MHz       2295 s          0 s        145 s       7258 s          0 s
       #2  2868 MHz       2811 s          0 s        179 s       6705 s          0 s
       #3  2893 MHz       2427 s          0 s        146 s       7128 s          0 s
       #4  2870 MHz       2673 s          0 s        179 s       6848 s          0 s
       
  Memory: 15.614948272705078 GB (12304.046875 MB free)
  Uptime: 974.5 sec
  Load Avg:  1.85  1.55  0.91
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
  uname: Linux 6.17.0-1015-azure #15~24.04.1-Ubuntu SMP Wed May  6 22:37:49 UTC 2026 x86_64 x86_64
  CPU: AMD EPYC 9V74 80-Core Processor: 
              speed         user         nice          sys         idle          irq
       #1  2870 MHz       3328 s          0 s        193 s       9263 s          0 s
       #2  2855 MHz       4152 s          0 s        240 s       8390 s          0 s
       #3  2874 MHz       4128 s          0 s        196 s       8466 s          0 s
       #4  2874 MHz       3434 s          0 s        240 s       9113 s          0 s
       
  Memory: 15.614948272705078 GB (12286.69921875 MB free)
  Uptime: 1283.66 sec
  Load Avg:  1.73  1.66  1.14
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-12.0.1 (ORCJIT, znver3)
```

---
# Target result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmark: 11 Jun 2026 - 04:38
* Package commit: 9efe8c4
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
| `["collect", "assoc", "basesize=1"]`                | 168.838 ms (5%) |         |   4.36 MiB (1%) |       32800 |
| `["collect", "assoc", "basesize=1024"]`             | 167.266 ms (5%) |         |   1.09 MiB (1%) |          53 |
| `["collect", "assoc", "basesize=32"]`               | 167.518 ms (5%) |         |   1.48 MiB (1%) |        1052 |
| `["collect", "seq"]`                                | 334.127 ms (5%) |         | 256.05 KiB (1%) |           2 |
| `["collect", "unordered", "basesize=1"]`            | 283.707 ms (5%) |         |  23.80 MiB (1%) |      409596 |
| `["collect", "unordered", "basesize=1024"]`         | 176.667 ms (5%) |         |   1.01 MiB (1%) |        1069 |
| `["collect", "unordered", "basesize=32"]`           | 186.746 ms (5%) |         |   1.60 MiB (1%) |       15220 |
| `["findfirst", "n=1000", "foldl"]`                  | 580.218 ms (5%) |         |                 |             |
| `["findfirst", "n=1000", "reduce", "basesize=128"]` | 316.280 ms (5%) |         | 232.83 KiB (1%) |        3275 |
| `["findfirst", "n=1000", "reduce", "basesize=256"]` | 518.227 ms (5%) |         | 184.41 KiB (1%) |        2623 |
| `["findfirst", "n=1000", "reduce", "basesize=512"]` | 396.172 ms (5%) |         |  81.42 KiB (1%) |        1149 |
| `["findfirst", "n=400", "foldl"]`                   | 433.936 ms (5%) |         |                 |             |
| `["findfirst", "n=400", "reduce", "basesize=128"]`  | 234.912 ms (5%) |         | 403.77 KiB (1%) |        5748 |
| `["findfirst", "n=400", "reduce", "basesize=256"]`  | 229.537 ms (5%) |         | 207.19 KiB (1%) |        2956 |
| `["findfirst", "n=400", "reduce", "basesize=512"]`  | 310.205 ms (5%) |         | 140.67 KiB (1%) |        2012 |
| `["findfirst", "n=500", "foldl"]`                   |  75.319 ms (5%) |         |                 |             |
| `["findfirst", "n=500", "reduce", "basesize=128"]`  | 158.183 ms (5%) |         | 233.98 KiB (1%) |        3267 |
| `["findfirst", "n=500", "reduce", "basesize=256"]`  | 223.498 ms (5%) |         | 168.44 KiB (1%) |        2372 |
| `["findfirst", "n=500", "reduce", "basesize=512"]`  | 275.026 ms (5%) |         | 118.86 KiB (1%) |        1637 |
| `["overhead", "default"]`                           |  57.767 μs (5%) |         |  32.73 KiB (1%) |         418 |
| `["overhead", "stoppable=false"]`                   |  58.108 μs (5%) |         |  32.75 KiB (1%) |         418 |
| `["overhead", "stoppable=true"]`                    |  63.355 μs (5%) |         |  44.28 KiB (1%) |         611 |
| `["parallel_histogram", "assoc", "basesize=16384"]` |   2.540 ms (5%) |         | 728.91 KiB (1%) |          57 |
| `["parallel_histogram", "assoc", "basesize=4096"]`  |   3.247 ms (5%) |         |   1.79 MiB (1%) |         216 |
| `["parallel_histogram", "assoc", "basesize=8192"]`  |   2.901 ms (5%) |         |   1.42 MiB (1%) |         117 |
| `["parallel_histogram", "comm", "basesize=16384"]`  |   9.292 ms (5%) |         |   1.58 MiB (1%) |        2449 |
| `["parallel_histogram", "comm", "basesize=4096"]`   |  15.482 ms (5%) |         |   1.36 MiB (1%) |       10857 |
| `["parallel_histogram", "comm", "basesize=8192"]`   |  12.023 ms (5%) |         |   1.28 MiB (1%) |        8153 |
| `["parallel_histogram", "seq"]`                     |   4.503 ms (5%) |         | 364.16 KiB (1%) |          24 |
| `["partition_length_maximum", "rand", "foldl"]`     |  35.398 ms (5%) |         |                 |             |
| `["partition_length_maximum", "rand", "reduce"]`    |  17.759 ms (5%) |         |  736 bytes (1%) |          11 |
| `["splitby", "count", "foldl"]`                     |   1.723 ms (5%) |         |                 |             |
| `["splitby", "count", "man"]`                       |   1.277 ms (5%) |         |                 |             |
| `["splitby", "count", "reduce"]`                    | 838.002 μs (5%) |         |   1.06 KiB (1%) |          18 |
| `["sum", "random", "foldl"]`                        |  12.467 ms (5%) |         |                 |             |
| `["sum", "random", "reduce", "basesize=128"]`       |   6.398 ms (5%) |         |  74.19 KiB (1%) |        1104 |
| `["sum", "random", "reduce", "basesize=256"]`       |   6.331 ms (5%) |         |  36.72 KiB (1%) |         545 |
| `["sum", "random", "reduce", "basesize=512"]`       |   6.292 ms (5%) |         |  18.11 KiB (1%) |         270 |
| `["sum", "uniform", "foldl"]`                       |  12.286 ms (5%) |         |                 |             |
| `["sum", "uniform", "reduce", "basesize=128"]`      |   6.314 ms (5%) |         |  74.19 KiB (1%) |        1104 |
| `["sum", "uniform", "reduce", "basesize=256"]`      |   6.245 ms (5%) |         |  36.66 KiB (1%) |         543 |
| `["sum", "uniform", "reduce", "basesize=512"]`      |   6.199 ms (5%) |         |  18.05 KiB (1%) |         268 |
| `["sum", "valley", "foldl"]`                        |  12.544 ms (5%) |         |                 |             |
| `["sum", "valley", "reduce", "basesize=128"]`       |   6.446 ms (5%) |         |  74.06 KiB (1%) |        1100 |
| `["sum", "valley", "reduce", "basesize=256"]`       |   6.382 ms (5%) |         |  36.78 KiB (1%) |         547 |
| `["sum", "valley", "reduce", "basesize=512"]`       |   6.354 ms (5%) |         |  18.08 KiB (1%) |         269 |
| `["words", "nthreads=1"]`                           |  15.745 ms (5%) |         |  31.89 MiB (1%) |     1038844 |
| `["words", "nthreads=2"]`                           |  10.289 ms (5%) |         |  32.24 MiB (1%) |     1038880 |
| `["words", "nthreads=4"]`                           |  10.584 ms (5%) |         |  32.96 MiB (1%) |     1038953 |

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
  uname: Linux 6.17.0-1015-azure #15~24.04.1-Ubuntu SMP Wed May  6 22:37:49 UTC 2026 x86_64 x86_64
  CPU: AMD EPYC 9V74 80-Core Processor: 
              speed         user         nice          sys         idle          irq
       #1  2862 MHz       2295 s          0 s        145 s       7258 s          0 s
       #2  2868 MHz       2811 s          0 s        179 s       6705 s          0 s
       #3  2893 MHz       2427 s          0 s        146 s       7128 s          0 s
       #4  2870 MHz       2673 s          0 s        179 s       6848 s          0 s
       
  Memory: 15.614948272705078 GB (12304.046875 MB free)
  Uptime: 974.5 sec
  Load Avg:  1.85  1.55  0.91
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-12.0.1 (ORCJIT, znver3)
```

---
# Baseline result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmark: 11 Jun 2026 - 04:43
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
| `["collect", "assoc", "basesize=1"]`                | 168.912 ms (5%) |         |   4.36 MiB (1%) |       32801 |
| `["collect", "assoc", "basesize=1024"]`             | 167.637 ms (5%) |         |   1.09 MiB (1%) |          54 |
| `["collect", "assoc", "basesize=32"]`               | 167.623 ms (5%) |         |   1.48 MiB (1%) |        1053 |
| `["collect", "seq"]`                                | 334.129 ms (5%) |         | 256.05 KiB (1%) |           2 |
| `["collect", "unordered", "basesize=1"]`            | 275.410 ms (5%) |         |  23.78 MiB (1%) |      408970 |
| `["collect", "unordered", "basesize=1024"]`         | 176.111 ms (5%) |         |   1.01 MiB (1%) |        1015 |
| `["collect", "unordered", "basesize=32"]`           | 186.015 ms (5%) |         |   1.60 MiB (1%) |       15189 |
| `["findfirst", "n=1000", "foldl"]`                  | 580.384 ms (5%) |         |                 |             |
| `["findfirst", "n=1000", "reduce", "basesize=128"]` | 319.012 ms (5%) |         | 236.92 KiB (1%) |        3329 |
| `["findfirst", "n=1000", "reduce", "basesize=256"]` | 388.408 ms (5%) |         | 157.20 KiB (1%) |        2193 |
| `["findfirst", "n=1000", "reduce", "basesize=512"]` | 396.781 ms (5%) |         |  81.33 KiB (1%) |        1146 |
| `["findfirst", "n=400", "foldl"]`                   | 434.273 ms (5%) |         |                 |             |
| `["findfirst", "n=400", "reduce", "basesize=128"]`  | 226.128 ms (5%) |         | 384.12 KiB (1%) |        5478 |
| `["findfirst", "n=400", "reduce", "basesize=256"]`  | 227.064 ms (5%) |         | 197.05 KiB (1%) |        2826 |
| `["findfirst", "n=400", "reduce", "basesize=512"]`  | 251.878 ms (5%) |         | 112.56 KiB (1%) |        1621 |
| `["findfirst", "n=500", "foldl"]`                   |  75.400 ms (5%) |         |                 |             |
| `["findfirst", "n=500", "reduce", "basesize=128"]`  | 130.747 ms (5%) |         | 207.00 KiB (1%) |        2854 |
| `["findfirst", "n=500", "reduce", "basesize=256"]`  | 187.253 ms (5%) |         | 156.08 KiB (1%) |        2157 |
| `["findfirst", "n=500", "reduce", "basesize=512"]`  |  75.702 ms (5%) |         |  50.84 KiB (1%) |         681 |
| `["overhead", "default"]`                           |  57.977 μs (5%) |         |  32.67 KiB (1%) |         416 |
| `["overhead", "stoppable=false"]`                   |  58.839 μs (5%) |         |  32.75 KiB (1%) |         418 |
| `["overhead", "stoppable=true"]`                    |  64.026 μs (5%) |         |  44.25 KiB (1%) |         610 |
| `["parallel_histogram", "assoc", "basesize=16384"]` |   2.539 ms (5%) |         | 728.91 KiB (1%) |          57 |
| `["parallel_histogram", "assoc", "basesize=4096"]`  |   3.228 ms (5%) |         |   1.79 MiB (1%) |         216 |
| `["parallel_histogram", "assoc", "basesize=8192"]`  |   2.884 ms (5%) |         |   1.42 MiB (1%) |         117 |
| `["parallel_histogram", "comm", "basesize=16384"]`  |   8.175 ms (5%) |         |   1.56 MiB (1%) |        1829 |
| `["parallel_histogram", "comm", "basesize=4096"]`   |  14.061 ms (5%) |         |   1.34 MiB (1%) |        9946 |
| `["parallel_histogram", "comm", "basesize=8192"]`   |  12.391 ms (5%) |         |   1.26 MiB (1%) |        7048 |
| `["parallel_histogram", "seq"]`                     |   4.507 ms (5%) |         | 364.16 KiB (1%) |          24 |
| `["partition_length_maximum", "rand", "foldl"]`     |  35.402 ms (5%) |         |                 |             |
| `["partition_length_maximum", "rand", "reduce"]`    |  17.756 ms (5%) |         |  736 bytes (1%) |          11 |
| `["splitby", "count", "foldl"]`                     |   1.726 ms (5%) |         |                 |             |
| `["splitby", "count", "man"]`                       |   1.279 ms (5%) |         |                 |             |
| `["splitby", "count", "reduce"]`                    | 801.757 μs (5%) |         |   1.06 KiB (1%) |          18 |
| `["sum", "random", "foldl"]`                        |  12.525 ms (5%) |         |                 |             |
| `["sum", "random", "reduce", "basesize=128"]`       |   6.395 ms (5%) |         |  74.22 KiB (1%) |        1105 |
| `["sum", "random", "reduce", "basesize=256"]`       |   6.355 ms (5%) |         |  36.78 KiB (1%) |         547 |
| `["sum", "random", "reduce", "basesize=512"]`       |   6.329 ms (5%) |         |  18.11 KiB (1%) |         270 |
| `["sum", "uniform", "foldl"]`                       |  12.288 ms (5%) |         |                 |             |
| `["sum", "uniform", "reduce", "basesize=128"]`      |   6.300 ms (5%) |         |  74.16 KiB (1%) |        1103 |
| `["sum", "uniform", "reduce", "basesize=256"]`      |   6.231 ms (5%) |         |  36.75 KiB (1%) |         546 |
| `["sum", "uniform", "reduce", "basesize=512"]`      |   6.197 ms (5%) |         |  18.08 KiB (1%) |         269 |
| `["sum", "valley", "foldl"]`                        |  12.540 ms (5%) |         |                 |             |
| `["sum", "valley", "reduce", "basesize=128"]`       |   6.444 ms (5%) |         |  74.12 KiB (1%) |        1102 |
| `["sum", "valley", "reduce", "basesize=256"]`       |   6.369 ms (5%) |         |  36.78 KiB (1%) |         547 |
| `["sum", "valley", "reduce", "basesize=512"]`       |   6.344 ms (5%) |         |  18.05 KiB (1%) |         268 |
| `["words", "nthreads=1"]`                           |  15.804 ms (5%) |         |  31.62 MiB (1%) |     1030442 |
| `["words", "nthreads=2"]`                           |   9.890 ms (5%) |         |  31.98 MiB (1%) |     1030478 |
| `["words", "nthreads=4"]`                           |  10.732 ms (5%) |         |  32.88 MiB (1%) |     1030676 |

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
  uname: Linux 6.17.0-1015-azure #15~24.04.1-Ubuntu SMP Wed May  6 22:37:49 UTC 2026 x86_64 x86_64
  CPU: AMD EPYC 9V74 80-Core Processor: 
              speed         user         nice          sys         idle          irq
       #1  2870 MHz       3328 s          0 s        193 s       9263 s          0 s
       #2  2855 MHz       4152 s          0 s        240 s       8390 s          0 s
       #3  2874 MHz       4128 s          0 s        196 s       8466 s          0 s
       #4  2874 MHz       3434 s          0 s        240 s       9113 s          0 s
       
  Memory: 15.614948272705078 GB (12286.69921875 MB free)
  Uptime: 1283.66 sec
  Load Avg:  1.73  1.66  1.14
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
    BogoMIPS:                                5192.27
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

