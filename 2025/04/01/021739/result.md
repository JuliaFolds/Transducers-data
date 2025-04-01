# Multi-thread benchmark result

* Pull request commit: [`5b4b673a6defe8295970dfd49ffe10f440ac8444`](https://github.com/JuliaFolds/Transducers.jl/commit/5b4b673a6defe8295970dfd49ffe10f440ac8444)
* Pull request: <https://github.com/JuliaFolds/Transducers.jl/pull/243> (Update */Manifest.toml)

# Judge result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmarks:
    - Target: 1 Apr 2025 - 02:12
    - Baseline: 1 Apr 2025 - 02:17
* Package commits:
    - Target: b0c7a31
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
| `["findfirst", "n=1000", "reduce", "basesize=128"]` |                1.43 (5%) :x: |                1.43 (1%) :x: |
| `["findfirst", "n=1000", "reduce", "basesize=256"]` |                1.07 (5%) :x: |                1.02 (1%) :x: |
| `["findfirst", "n=1000", "reduce", "basesize=512"]` | 0.94 (5%) :white_check_mark: | 0.95 (1%) :white_check_mark: |
| `["findfirst", "n=400", "reduce", "basesize=512"]`  |                1.25 (5%) :x: |                1.25 (1%) :x: |
| `["findfirst", "n=500", "reduce", "basesize=128"]`  | 0.44 (5%) :white_check_mark: | 0.61 (1%) :white_check_mark: |
| `["findfirst", "n=500", "reduce", "basesize=256"]`  | 0.85 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["parallel_histogram", "comm", "basesize=4096"]`   |                1.06 (5%) :x: |                1.07 (1%) :x: |
| `["splitby", "count", "reduce"]`                    |                   0.98 (5%)  |                1.03 (1%) :x: |
| `["words", "nthreads=1"]`                           | 0.95 (5%) :white_check_mark: | 0.99 (1%) :white_check_mark: |
| `["words", "nthreads=2"]`                           |                   0.97 (5%)  | 0.99 (1%) :white_check_mark: |

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
       #1  3245 MHz       2308 s          0 s        174 s       5008 s          0 s
       #2  3249 MHz       2442 s          0 s        208 s       4862 s          0 s
       #3  3234 MHz       2726 s          0 s        198 s       4527 s          0 s
       #4  3243 MHz       2556 s          0 s        241 s       4670 s          0 s
       
  Memory: 15.61526870727539 GB (8597.75390625 MB free)
  Uptime: 757.08 sec
  Load Avg:  1.68  1.53  0.93
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
       #1  3250 MHz       3550 s          0 s        251 s       6745 s          0 s
       #2  3244 MHz       3735 s          0 s        302 s       6532 s          0 s
       #3  3253 MHz       3910 s          0 s        261 s       6337 s          0 s
       #4  3242 MHz       3589 s          0 s        299 s       6636 s          0 s
       
  Memory: 15.61526870727539 GB (8574.4921875 MB free)
  Uptime: 1063.47 sec
  Load Avg:  1.71  1.63  1.15
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-12.0.1 (ORCJIT, znver3)
```

---
# Target result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmark: 1 Apr 2025 - 02:12
* Package commit: b0c7a31
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
| `["collect", "assoc", "basesize=1"]`                | 150.249 ms (5%) |         |   4.36 MiB (1%) |       32800 |
| `["collect", "assoc", "basesize=1024"]`             | 148.105 ms (5%) |         |   1.09 MiB (1%) |          53 |
| `["collect", "assoc", "basesize=32"]`               | 148.311 ms (5%) |         |   1.48 MiB (1%) |        1052 |
| `["collect", "seq"]`                                | 295.988 ms (5%) |         | 256.05 KiB (1%) |           2 |
| `["collect", "unordered", "basesize=1"]`            | 244.066 ms (5%) |         |  23.67 MiB (1%) |      405448 |
| `["collect", "unordered", "basesize=1024"]`         | 157.967 ms (5%) |         |   1.01 MiB (1%) |        1113 |
| `["collect", "unordered", "basesize=32"]`           | 170.319 ms (5%) |         |   1.60 MiB (1%) |       15298 |
| `["findfirst", "n=1000", "foldl"]`                  | 508.121 ms (5%) |         |                 |             |
| `["findfirst", "n=1000", "reduce", "basesize=128"]` | 398.714 ms (5%) |         | 329.91 KiB (1%) |        4629 |
| `["findfirst", "n=1000", "reduce", "basesize=256"]` | 362.666 ms (5%) |         | 160.55 KiB (1%) |        2243 |
| `["findfirst", "n=1000", "reduce", "basesize=512"]` | 425.341 ms (5%) |         | 102.33 KiB (1%) |        1424 |
| `["findfirst", "n=400", "foldl"]`                   | 380.239 ms (5%) |         |                 |             |
| `["findfirst", "n=400", "reduce", "basesize=128"]`  | 198.095 ms (5%) |         | 371.09 KiB (1%) |        5295 |
| `["findfirst", "n=400", "reduce", "basesize=256"]`  | 199.289 ms (5%) |         | 201.02 KiB (1%) |        2878 |
| `["findfirst", "n=400", "reduce", "basesize=512"]`  | 276.931 ms (5%) |         | 141.00 KiB (1%) |        2013 |
| `["findfirst", "n=500", "foldl"]`                   |  65.334 ms (5%) |         |                 |             |
| `["findfirst", "n=500", "reduce", "basesize=128"]`  |  56.137 ms (5%) |         | 138.12 KiB (1%) |        1858 |
| `["findfirst", "n=500", "reduce", "basesize=256"]`  | 121.644 ms (5%) |         | 135.12 KiB (1%) |        1834 |
| `["findfirst", "n=500", "reduce", "basesize=512"]`  |  87.654 ms (5%) |         |  55.95 KiB (1%) |         765 |
| `["overhead", "default"]`                           |  52.538 μs (5%) |         |  32.73 KiB (1%) |         418 |
| `["overhead", "stoppable=false"]`                   |  51.596 μs (5%) |         |  32.75 KiB (1%) |         418 |
| `["overhead", "stoppable=true"]`                    |  57.788 μs (5%) |         |  44.25 KiB (1%) |         610 |
| `["parallel_histogram", "assoc", "basesize=16384"]` |   2.399 ms (5%) |         | 728.91 KiB (1%) |          57 |
| `["parallel_histogram", "assoc", "basesize=4096"]`  |   3.026 ms (5%) |         |   1.79 MiB (1%) |         216 |
| `["parallel_histogram", "assoc", "basesize=8192"]`  |   2.724 ms (5%) |         |   1.42 MiB (1%) |         117 |
| `["parallel_histogram", "comm", "basesize=16384"]`  |   8.208 ms (5%) |         |   1.55 MiB (1%) |        1340 |
| `["parallel_histogram", "comm", "basesize=4096"]`   |  12.357 ms (5%) |         |   1.31 MiB (1%) |        9055 |
| `["parallel_histogram", "comm", "basesize=8192"]`   |  11.198 ms (5%) |         |   1.27 MiB (1%) |        6320 |
| `["parallel_histogram", "seq"]`                     |   4.255 ms (5%) |         | 364.16 KiB (1%) |          24 |
| `["partition_length_maximum", "rand", "foldl"]`     |  31.293 ms (5%) |         |                 |             |
| `["partition_length_maximum", "rand", "reduce"]`    |  16.331 ms (5%) |         |  736 bytes (1%) |          11 |
| `["splitby", "count", "foldl"]`                     |   1.552 ms (5%) |         |                 |             |
| `["splitby", "count", "man"]`                       |   1.165 ms (5%) |         |                 |             |
| `["splitby", "count", "reduce"]`                    | 719.974 μs (5%) |         |   1.09 KiB (1%) |          19 |
| `["sum", "random", "foldl"]`                        |  11.073 ms (5%) |         |                 |             |
| `["sum", "random", "reduce", "basesize=128"]`       |   5.681 ms (5%) |         |  74.19 KiB (1%) |        1104 |
| `["sum", "random", "reduce", "basesize=256"]`       |   5.617 ms (5%) |         |  36.75 KiB (1%) |         546 |
| `["sum", "random", "reduce", "basesize=512"]`       |   5.598 ms (5%) |         |  18.08 KiB (1%) |         269 |
| `["sum", "uniform", "foldl"]`                       |  10.930 ms (5%) |         |                 |             |
| `["sum", "uniform", "reduce", "basesize=128"]`      |   5.617 ms (5%) |         |  74.12 KiB (1%) |        1102 |
| `["sum", "uniform", "reduce", "basesize=256"]`      |   5.540 ms (5%) |         |  36.75 KiB (1%) |         546 |
| `["sum", "uniform", "reduce", "basesize=512"]`      |   5.551 ms (5%) |         |  18.08 KiB (1%) |         269 |
| `["sum", "valley", "foldl"]`                        |  11.165 ms (5%) |         |                 |             |
| `["sum", "valley", "reduce", "basesize=128"]`       |   5.723 ms (5%) |         |  74.16 KiB (1%) |        1103 |
| `["sum", "valley", "reduce", "basesize=256"]`       |   5.686 ms (5%) |         |  36.75 KiB (1%) |         546 |
| `["sum", "valley", "reduce", "basesize=512"]`       |   5.664 ms (5%) |         |  18.05 KiB (1%) |         268 |
| `["words", "nthreads=1"]`                           |  14.087 ms (5%) |         |  31.50 MiB (1%) |     1025730 |
| `["words", "nthreads=2"]`                           |   9.048 ms (5%) |         |  31.86 MiB (1%) |     1025766 |
| `["words", "nthreads=4"]`                           |   9.970 ms (5%) |         |  32.76 MiB (1%) |     1025933 |

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
       #1  3245 MHz       2308 s          0 s        174 s       5008 s          0 s
       #2  3249 MHz       2442 s          0 s        208 s       4862 s          0 s
       #3  3234 MHz       2726 s          0 s        198 s       4527 s          0 s
       #4  3243 MHz       2556 s          0 s        241 s       4670 s          0 s
       
  Memory: 15.61526870727539 GB (8597.75390625 MB free)
  Uptime: 757.08 sec
  Load Avg:  1.68  1.53  0.93
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-12.0.1 (ORCJIT, znver3)
```

---
# Baseline result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmark: 1 Apr 2025 - 02:17
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
| `["collect", "assoc", "basesize=1"]`                | 149.815 ms (5%) |         |   4.36 MiB (1%) |       32800 |
| `["collect", "assoc", "basesize=1024"]`             | 148.498 ms (5%) |         |   1.09 MiB (1%) |          53 |
| `["collect", "assoc", "basesize=32"]`               | 148.246 ms (5%) |         |   1.48 MiB (1%) |        1052 |
| `["collect", "seq"]`                                | 295.988 ms (5%) |         | 256.05 KiB (1%) |           2 |
| `["collect", "unordered", "basesize=1"]`            | 250.698 ms (5%) |         |  23.70 MiB (1%) |      406557 |
| `["collect", "unordered", "basesize=1024"]`         | 158.753 ms (5%) |         |   1.01 MiB (1%) |        1133 |
| `["collect", "unordered", "basesize=32"]`           | 171.289 ms (5%) |         |   1.60 MiB (1%) |       15262 |
| `["findfirst", "n=1000", "foldl"]`                  | 509.305 ms (5%) |         |                 |             |
| `["findfirst", "n=1000", "reduce", "basesize=128"]` | 278.006 ms (5%) |         | 230.61 KiB (1%) |        3249 |
| `["findfirst", "n=1000", "reduce", "basesize=256"]` | 340.441 ms (5%) |         | 157.00 KiB (1%) |        2194 |
| `["findfirst", "n=1000", "reduce", "basesize=512"]` | 451.660 ms (5%) |         | 107.83 KiB (1%) |        1498 |
| `["findfirst", "n=400", "foldl"]`                   | 380.959 ms (5%) |         |                 |             |
| `["findfirst", "n=400", "reduce", "basesize=128"]`  | 202.389 ms (5%) |         | 374.42 KiB (1%) |        5341 |
| `["findfirst", "n=400", "reduce", "basesize=256"]`  | 199.848 ms (5%) |         | 200.80 KiB (1%) |        2871 |
| `["findfirst", "n=400", "reduce", "basesize=512"]`  | 221.704 ms (5%) |         | 112.56 KiB (1%) |        1621 |
| `["findfirst", "n=500", "foldl"]`                   |  66.251 ms (5%) |         |                 |             |
| `["findfirst", "n=500", "reduce", "basesize=128"]`  | 128.719 ms (5%) |         | 225.22 KiB (1%) |        3096 |
| `["findfirst", "n=500", "reduce", "basesize=256"]`  | 143.932 ms (5%) |         | 135.42 KiB (1%) |        1886 |
| `["findfirst", "n=500", "reduce", "basesize=512"]`  |  86.346 ms (5%) |         |  55.88 KiB (1%) |         762 |
| `["overhead", "default"]`                           |  52.047 μs (5%) |         |  32.73 KiB (1%) |         418 |
| `["overhead", "stoppable=false"]`                   |  52.518 μs (5%) |         |  32.75 KiB (1%) |         418 |
| `["overhead", "stoppable=true"]`                    |  58.840 μs (5%) |         |  44.25 KiB (1%) |         610 |
| `["parallel_histogram", "assoc", "basesize=16384"]` |   2.413 ms (5%) |         | 728.91 KiB (1%) |          57 |
| `["parallel_histogram", "assoc", "basesize=4096"]`  |   2.964 ms (5%) |         |   1.79 MiB (1%) |         216 |
| `["parallel_histogram", "assoc", "basesize=8192"]`  |   2.755 ms (5%) |         |   1.42 MiB (1%) |         117 |
| `["parallel_histogram", "comm", "basesize=16384"]`  |   8.111 ms (5%) |         |   1.54 MiB (1%) |        1082 |
| `["parallel_histogram", "comm", "basesize=4096"]`   |  11.656 ms (5%) |         |   1.23 MiB (1%) |        6376 |
| `["parallel_histogram", "comm", "basesize=8192"]`   |  11.301 ms (5%) |         |   1.26 MiB (1%) |        6782 |
| `["parallel_histogram", "seq"]`                     |   4.270 ms (5%) |         | 364.16 KiB (1%) |          24 |
| `["partition_length_maximum", "rand", "foldl"]`     |  31.298 ms (5%) |         |                 |             |
| `["partition_length_maximum", "rand", "reduce"]`    |  15.676 ms (5%) |         |  736 bytes (1%) |          11 |
| `["splitby", "count", "foldl"]`                     |   1.607 ms (5%) |         |                 |             |
| `["splitby", "count", "man"]`                       |   1.140 ms (5%) |         |                 |             |
| `["splitby", "count", "reduce"]`                    | 735.513 μs (5%) |         |   1.06 KiB (1%) |          18 |
| `["sum", "random", "foldl"]`                        |  11.051 ms (5%) |         |                 |             |
| `["sum", "random", "reduce", "basesize=128"]`       |   5.621 ms (5%) |         |  74.19 KiB (1%) |        1104 |
| `["sum", "random", "reduce", "basesize=256"]`       |   5.603 ms (5%) |         |  36.78 KiB (1%) |         547 |
| `["sum", "random", "reduce", "basesize=512"]`       |   5.568 ms (5%) |         |  18.08 KiB (1%) |         269 |
| `["sum", "uniform", "foldl"]`                       |  10.911 ms (5%) |         |                 |             |
| `["sum", "uniform", "reduce", "basesize=128"]`      |   5.599 ms (5%) |         |  74.16 KiB (1%) |        1103 |
| `["sum", "uniform", "reduce", "basesize=256"]`      |   5.536 ms (5%) |         |  36.78 KiB (1%) |         547 |
| `["sum", "uniform", "reduce", "basesize=512"]`      |   5.498 ms (5%) |         |  18.08 KiB (1%) |         269 |
| `["sum", "valley", "foldl"]`                        |  11.165 ms (5%) |         |                 |             |
| `["sum", "valley", "reduce", "basesize=128"]`       |   5.721 ms (5%) |         |  74.06 KiB (1%) |        1100 |
| `["sum", "valley", "reduce", "basesize=256"]`       |   5.671 ms (5%) |         |  36.66 KiB (1%) |         543 |
| `["sum", "valley", "reduce", "basesize=512"]`       |   5.694 ms (5%) |         |  18.05 KiB (1%) |         268 |
| `["words", "nthreads=1"]`                           |  14.846 ms (5%) |         |  31.86 MiB (1%) |     1038140 |
| `["words", "nthreads=2"]`                           |   9.295 ms (5%) |         |  32.22 MiB (1%) |     1038176 |
| `["words", "nthreads=4"]`                           |   9.636 ms (5%) |         |  32.93 MiB (1%) |     1038258 |

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
       #1  3250 MHz       3550 s          0 s        251 s       6745 s          0 s
       #2  3244 MHz       3735 s          0 s        302 s       6532 s          0 s
       #3  3253 MHz       3910 s          0 s        261 s       6337 s          0 s
       #4  3242 MHz       3589 s          0 s        299 s       6636 s          0 s
       
  Memory: 15.61526870727539 GB (8574.4921875 MB free)
  Uptime: 1063.47 sec
  Load Avg:  1.71  1.63  1.15
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
    BogoMIPS:                             4890.85
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

