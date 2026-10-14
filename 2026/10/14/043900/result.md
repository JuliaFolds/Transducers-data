# Multi-thread benchmark result

* Pull request commit: [`24f18b847b135884d11d15b6b6b28a79da5761c5`](https://github.com/JuliaFolds/Transducers.jl/commit/24f18b847b135884d11d15b6b6b28a79da5761c5)
* Pull request: <https://github.com/JuliaFolds/Transducers.jl/pull/243> (Update */Manifest.toml)

# Judge result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmarks:
    - Target: 14 Oct 2026 - 04:33
    - Baseline: 14 Oct 2026 - 04:38
* Package commits:
    - Target: 258d2db
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
| `["findfirst", "n=1000", "reduce", "basesize=256"]` | 0.78 (5%) :white_check_mark: | 0.89 (1%) :white_check_mark: |
| `["findfirst", "n=1000", "reduce", "basesize=512"]` |                   0.96 (5%)  | 0.98 (1%) :white_check_mark: |
| `["findfirst", "n=400", "reduce", "basesize=128"]`  |                   0.99 (5%)  | 0.99 (1%) :white_check_mark: |
| `["findfirst", "n=400", "reduce", "basesize=512"]`  |                   0.96 (5%)  | 0.93 (1%) :white_check_mark: |
| `["findfirst", "n=500", "reduce", "basesize=128"]`  |                1.05 (5%) :x: |                1.02 (1%) :x: |
| `["findfirst", "n=500", "reduce", "basesize=256"]`  |                2.94 (5%) :x: |                2.14 (1%) :x: |
| `["findfirst", "n=500", "reduce", "basesize=512"]`  |                1.06 (5%) :x: |                1.07 (1%) :x: |
| `["parallel_histogram", "assoc", "basesize=4096"]`  |                   0.96 (5%)  | 0.87 (1%) :white_check_mark: |
| `["parallel_histogram", "comm", "basesize=16384"]`  |                   0.99 (5%)  |                1.16 (1%) :x: |
| `["splitby", "count", "reduce"]`                    |                   0.98 (5%)  |                1.03 (1%) :x: |
| `["words", "nthreads=1"]`                           | 0.92 (5%) :white_check_mark: |                   1.01 (1%)  |
| `["words", "nthreads=2"]`                           | 0.92 (5%) :white_check_mark: |                   1.01 (1%)  |
| `["words", "nthreads=4"]`                           | 0.92 (5%) :white_check_mark: |                1.01 (1%) :x: |

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
      Ubuntu 24.04.5 LTS
  uname: Linux 6.17.0-1022-azure #22-Ubuntu SMP Mon Jul 27 17:24:03 UTC 2026 x86_64 x86_64
  CPU: AMD EPYC 9V74 80-Core Processor: 
              speed         user         nice          sys         idle          irq
       #1  2848 MHz       2647 s          0 s        166 s       5192 s          0 s
       #2  2869 MHz       2394 s          0 s        178 s       5390 s          0 s
       #3  2866 MHz       2522 s          0 s        178 s       5296 s          0 s
       #4  2869 MHz       2751 s          0 s        182 s       5082 s          0 s
       
  Memory: 15.614940643310547 GB (10287.4453125 MB free)
  Uptime: 805.17 sec
  Load Avg:  1.76  1.53  0.92
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
      Ubuntu 24.04.5 LTS
  uname: Linux 6.17.0-1022-azure #22-Ubuntu SMP Mon Jul 27 17:24:03 UTC 2026 x86_64 x86_64
  CPU: AMD EPYC 9V74 80-Core Processor: 
              speed         user         nice          sys         idle          irq
       #1  2867 MHz       3781 s          0 s        214 s       7120 s          0 s
       #2  2870 MHz       3479 s          0 s        239 s       7351 s          0 s
       #3  2903 MHz       3605 s          0 s        237 s       7265 s          0 s
       #4  2863 MHz       4242 s          0 s        254 s       6629 s          0 s
       
  Memory: 15.614940643310547 GB (10233.82421875 MB free)
  Uptime: 1116.86 sec
  Load Avg:  1.57  1.57  1.12
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-12.0.1 (ORCJIT, znver3)
```

---
# Target result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmark: 14 Oct 2026 - 04:33
* Package commit: 258d2db
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
| `["collect", "assoc", "basesize=1"]`                | 168.281 ms (5%) |         |   4.36 MiB (1%) |       32800 |
| `["collect", "assoc", "basesize=1024"]`             | 167.233 ms (5%) |         |   1.09 MiB (1%) |          53 |
| `["collect", "assoc", "basesize=32"]`               | 167.352 ms (5%) |         |   1.48 MiB (1%) |        1052 |
| `["collect", "seq"]`                                | 334.065 ms (5%) |         | 256.05 KiB (1%) |           2 |
| `["collect", "unordered", "basesize=1"]`            | 295.295 ms (5%) |         |  23.76 MiB (1%) |      408338 |
| `["collect", "unordered", "basesize=1024"]`         | 176.339 ms (5%) |         |   1.01 MiB (1%) |        1081 |
| `["collect", "unordered", "basesize=32"]`           | 187.666 ms (5%) |         |   1.60 MiB (1%) |       15275 |
| `["findfirst", "n=1000", "foldl"]`                  | 580.188 ms (5%) |         |                 |             |
| `["findfirst", "n=1000", "reduce", "basesize=128"]` | 316.201 ms (5%) |         | 232.86 KiB (1%) |        3276 |
| `["findfirst", "n=1000", "reduce", "basesize=256"]` | 388.008 ms (5%) |         | 157.20 KiB (1%) |        2193 |
| `["findfirst", "n=1000", "reduce", "basesize=512"]` | 396.310 ms (5%) |         |  81.33 KiB (1%) |        1146 |
| `["findfirst", "n=400", "foldl"]`                   | 434.005 ms (5%) |         |                 |             |
| `["findfirst", "n=400", "reduce", "basesize=128"]`  | 223.973 ms (5%) |         | 383.12 KiB (1%) |        5454 |
| `["findfirst", "n=400", "reduce", "basesize=256"]`  | 227.164 ms (5%) |         | 200.86 KiB (1%) |        2873 |
| `["findfirst", "n=400", "reduce", "basesize=512"]`  | 265.717 ms (5%) |         | 119.00 KiB (1%) |        1711 |
| `["findfirst", "n=500", "foldl"]`                   |  75.332 ms (5%) |         |                 |             |
| `["findfirst", "n=500", "reduce", "basesize=128"]`  | 178.655 ms (5%) |         | 270.95 KiB (1%) |        3763 |
| `["findfirst", "n=500", "reduce", "basesize=256"]`  | 210.137 ms (5%) |         | 167.88 KiB (1%) |        2362 |
| `["findfirst", "n=500", "reduce", "basesize=512"]`  |  97.248 ms (5%) |         |  58.19 KiB (1%) |         791 |
| `["overhead", "default"]`                           |  60.091 μs (5%) |         |  32.73 KiB (1%) |         418 |
| `["overhead", "stoppable=false"]`                   |  58.668 μs (5%) |         |  32.72 KiB (1%) |         417 |
| `["overhead", "stoppable=true"]`                    |  69.215 μs (5%) |         |  44.25 KiB (1%) |         610 |
| `["parallel_histogram", "assoc", "basesize=16384"]` |   2.521 ms (5%) |         | 728.91 KiB (1%) |          57 |
| `["parallel_histogram", "assoc", "basesize=4096"]`  |   3.229 ms (5%) |         |   1.79 MiB (1%) |         215 |
| `["parallel_histogram", "assoc", "basesize=8192"]`  |   2.878 ms (5%) |         |   1.42 MiB (1%) |         117 |
| `["parallel_histogram", "comm", "basesize=16384"]`  |   8.204 ms (5%) |         |   1.56 MiB (1%) |        1690 |
| `["parallel_histogram", "comm", "basesize=4096"]`   |  12.874 ms (5%) |         |   1.21 MiB (1%) |        5894 |
| `["parallel_histogram", "comm", "basesize=8192"]`   |  11.702 ms (5%) |         |   1.21 MiB (1%) |        5250 |
| `["parallel_histogram", "seq"]`                     |   4.499 ms (5%) |         | 364.16 KiB (1%) |          24 |
| `["partition_length_maximum", "rand", "foldl"]`     |  35.406 ms (5%) |         |                 |             |
| `["partition_length_maximum", "rand", "reduce"]`    |  17.765 ms (5%) |         |  736 bytes (1%) |          11 |
| `["splitby", "count", "foldl"]`                     |   1.702 ms (5%) |         |                 |             |
| `["splitby", "count", "man"]`                       |   1.276 ms (5%) |         |                 |             |
| `["splitby", "count", "reduce"]`                    | 806.918 μs (5%) |         |   1.09 KiB (1%) |          19 |
| `["sum", "random", "foldl"]`                        |  12.462 ms (5%) |         |                 |             |
| `["sum", "random", "reduce", "basesize=128"]`       |   6.365 ms (5%) |         |  74.25 KiB (1%) |        1106 |
| `["sum", "random", "reduce", "basesize=256"]`       |   6.306 ms (5%) |         |  36.75 KiB (1%) |         546 |
| `["sum", "random", "reduce", "basesize=512"]`       |   6.281 ms (5%) |         |  18.11 KiB (1%) |         270 |
| `["sum", "uniform", "foldl"]`                       |  12.287 ms (5%) |         |                 |             |
| `["sum", "uniform", "reduce", "basesize=128"]`      |   6.320 ms (5%) |         |  74.12 KiB (1%) |        1102 |
| `["sum", "uniform", "reduce", "basesize=256"]`      |   6.236 ms (5%) |         |  36.78 KiB (1%) |         547 |
| `["sum", "uniform", "reduce", "basesize=512"]`      |   6.197 ms (5%) |         |  18.05 KiB (1%) |         268 |
| `["sum", "valley", "foldl"]`                        |  12.542 ms (5%) |         |                 |             |
| `["sum", "valley", "reduce", "basesize=128"]`       |   6.442 ms (5%) |         |  74.12 KiB (1%) |        1102 |
| `["sum", "valley", "reduce", "basesize=256"]`       |   6.376 ms (5%) |         |  36.78 KiB (1%) |         547 |
| `["sum", "valley", "reduce", "basesize=512"]`       |   6.342 ms (5%) |         |  18.05 KiB (1%) |         268 |
| `["words", "nthreads=1"]`                           |  15.165 ms (5%) |         |  31.73 MiB (1%) |     1033498 |
| `["words", "nthreads=2"]`                           |   9.903 ms (5%) |         |  32.09 MiB (1%) |     1033534 |
| `["words", "nthreads=4"]`                           |  10.428 ms (5%) |         |  32.99 MiB (1%) |     1033717 |

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
      Ubuntu 24.04.5 LTS
  uname: Linux 6.17.0-1022-azure #22-Ubuntu SMP Mon Jul 27 17:24:03 UTC 2026 x86_64 x86_64
  CPU: AMD EPYC 9V74 80-Core Processor: 
              speed         user         nice          sys         idle          irq
       #1  2848 MHz       2647 s          0 s        166 s       5192 s          0 s
       #2  2869 MHz       2394 s          0 s        178 s       5390 s          0 s
       #3  2866 MHz       2522 s          0 s        178 s       5296 s          0 s
       #4  2869 MHz       2751 s          0 s        182 s       5082 s          0 s
       
  Memory: 15.614940643310547 GB (10287.4453125 MB free)
  Uptime: 805.17 sec
  Load Avg:  1.76  1.53  0.92
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-12.0.1 (ORCJIT, znver3)
```

---
# Baseline result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmark: 14 Oct 2026 - 04:38
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
| `["collect", "assoc", "basesize=1"]`                | 169.129 ms (5%) |         |   4.36 MiB (1%) |       32800 |
| `["collect", "assoc", "basesize=1024"]`             | 167.961 ms (5%) |         |   1.09 MiB (1%) |          53 |
| `["collect", "assoc", "basesize=32"]`               | 167.624 ms (5%) |         |   1.48 MiB (1%) |        1052 |
| `["collect", "seq"]`                                | 334.640 ms (5%) |         | 256.05 KiB (1%) |           2 |
| `["collect", "unordered", "basesize=1"]`            | 297.701 ms (5%) |         |  23.76 MiB (1%) |      408370 |
| `["collect", "unordered", "basesize=1024"]`         | 176.899 ms (5%) |         |   1.01 MiB (1%) |        1037 |
| `["collect", "unordered", "basesize=32"]`           | 187.291 ms (5%) |         |   1.60 MiB (1%) |       15254 |
| `["findfirst", "n=1000", "foldl"]`                  | 580.575 ms (5%) |         |                 |             |
| `["findfirst", "n=1000", "reduce", "basesize=128"]` | 316.474 ms (5%) |         | 230.61 KiB (1%) |        3249 |
| `["findfirst", "n=1000", "reduce", "basesize=256"]` | 495.508 ms (5%) |         | 176.88 KiB (1%) |        2510 |
| `["findfirst", "n=1000", "reduce", "basesize=512"]` | 410.735 ms (5%) |         |  82.89 KiB (1%) |        1169 |
| `["findfirst", "n=400", "foldl"]`                   | 434.272 ms (5%) |         |                 |             |
| `["findfirst", "n=400", "reduce", "basesize=128"]`  | 226.711 ms (5%) |         | 387.50 KiB (1%) |        5519 |
| `["findfirst", "n=400", "reduce", "basesize=256"]`  | 227.297 ms (5%) |         | 201.02 KiB (1%) |        2878 |
| `["findfirst", "n=400", "reduce", "basesize=512"]`  | 278.110 ms (5%) |         | 128.17 KiB (1%) |        1831 |
| `["findfirst", "n=500", "foldl"]`                   |  75.391 ms (5%) |         |                 |             |
| `["findfirst", "n=500", "reduce", "basesize=128"]`  | 169.925 ms (5%) |         | 266.31 KiB (1%) |        3668 |
| `["findfirst", "n=500", "reduce", "basesize=256"]`  |  71.560 ms (5%) |         |  78.45 KiB (1%) |        1068 |
| `["findfirst", "n=500", "reduce", "basesize=512"]`  |  92.128 ms (5%) |         |  54.44 KiB (1%) |         746 |
| `["overhead", "default"]`                           |  58.839 μs (5%) |         |  32.70 KiB (1%) |         417 |
| `["overhead", "stoppable=false"]`                   |  58.879 μs (5%) |         |  32.75 KiB (1%) |         418 |
| `["overhead", "stoppable=true"]`                    |  68.543 μs (5%) |         |  44.25 KiB (1%) |         610 |
| `["parallel_histogram", "assoc", "basesize=16384"]` |   2.546 ms (5%) |         | 728.91 KiB (1%) |          57 |
| `["parallel_histogram", "assoc", "basesize=4096"]`  |   3.351 ms (5%) |         |   2.05 MiB (1%) |         221 |
| `["parallel_histogram", "assoc", "basesize=8192"]`  |   2.921 ms (5%) |         |   1.42 MiB (1%) |         117 |
| `["parallel_histogram", "comm", "basesize=16384"]`  |   8.250 ms (5%) |         |   1.34 MiB (1%) |        1826 |
| `["parallel_histogram", "comm", "basesize=4096"]`   |  13.415 ms (5%) |         |   1.22 MiB (1%) |        6214 |
| `["parallel_histogram", "comm", "basesize=8192"]`   |  12.024 ms (5%) |         |   1.22 MiB (1%) |        4066 |
| `["parallel_histogram", "seq"]`                     |   4.558 ms (5%) |         | 364.16 KiB (1%) |          24 |
| `["partition_length_maximum", "rand", "foldl"]`     |  35.410 ms (5%) |         |                 |             |
| `["partition_length_maximum", "rand", "reduce"]`    |  17.727 ms (5%) |         |  736 bytes (1%) |          11 |
| `["splitby", "count", "foldl"]`                     |   1.715 ms (5%) |         |                 |             |
| `["splitby", "count", "man"]`                       |   1.278 ms (5%) |         |                 |             |
| `["splitby", "count", "reduce"]`                    | 825.377 μs (5%) |         |   1.06 KiB (1%) |          18 |
| `["sum", "random", "foldl"]`                        |  12.499 ms (5%) |         |                 |             |
| `["sum", "random", "reduce", "basesize=128"]`       |   6.386 ms (5%) |         |  74.06 KiB (1%) |        1100 |
| `["sum", "random", "reduce", "basesize=256"]`       |   6.337 ms (5%) |         |  36.75 KiB (1%) |         546 |
| `["sum", "random", "reduce", "basesize=512"]`       |   6.315 ms (5%) |         |  18.11 KiB (1%) |         270 |
| `["sum", "uniform", "foldl"]`                       |  12.285 ms (5%) |         |                 |             |
| `["sum", "uniform", "reduce", "basesize=128"]`      |   6.295 ms (5%) |         |  74.22 KiB (1%) |        1105 |
| `["sum", "uniform", "reduce", "basesize=256"]`      |   6.244 ms (5%) |         |  36.81 KiB (1%) |         548 |
| `["sum", "uniform", "reduce", "basesize=512"]`      |   6.191 ms (5%) |         |  18.02 KiB (1%) |         267 |
| `["sum", "valley", "foldl"]`                        |  12.544 ms (5%) |         |                 |             |
| `["sum", "valley", "reduce", "basesize=128"]`       |   6.446 ms (5%) |         |  74.06 KiB (1%) |        1100 |
| `["sum", "valley", "reduce", "basesize=256"]`       |   6.373 ms (5%) |         |  36.78 KiB (1%) |         547 |
| `["sum", "valley", "reduce", "basesize=512"]`       |   6.346 ms (5%) |         |  18.05 KiB (1%) |         268 |
| `["words", "nthreads=1"]`                           |  16.415 ms (5%) |         |  31.54 MiB (1%) |     1027624 |
| `["words", "nthreads=2"]`                           |  10.725 ms (5%) |         |  31.90 MiB (1%) |     1027660 |
| `["words", "nthreads=4"]`                           |  11.303 ms (5%) |         |  32.61 MiB (1%) |     1027732 |

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
      Ubuntu 24.04.5 LTS
  uname: Linux 6.17.0-1022-azure #22-Ubuntu SMP Mon Jul 27 17:24:03 UTC 2026 x86_64 x86_64
  CPU: AMD EPYC 9V74 80-Core Processor: 
              speed         user         nice          sys         idle          irq
       #1  2867 MHz       3781 s          0 s        214 s       7120 s          0 s
       #2  2870 MHz       3479 s          0 s        239 s       7351 s          0 s
       #3  2903 MHz       3605 s          0 s        237 s       7265 s          0 s
       #4  2863 MHz       4242 s          0 s        254 s       6629 s          0 s
       
  Memory: 15.614940643310547 GB (10233.82421875 MB free)
  Uptime: 1116.86 sec
  Load Avg:  1.57  1.57  1.12
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
    BogoMIPS:                                5192.26
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

