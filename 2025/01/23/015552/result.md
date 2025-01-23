# Multi-thread benchmark result

* Pull request commit: [`79edb915c3daf4bd5028f7638b629e4ca73c77b9`](https://github.com/JuliaFolds/Transducers.jl/commit/79edb915c3daf4bd5028f7638b629e4ca73c77b9)
* Pull request: <https://github.com/JuliaFolds/Transducers.jl/pull/243> (Update */Manifest.toml)

# Judge result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmarks:
    - Target: 23 Jan 2025 - 01:50
    - Baseline: 23 Jan 2025 - 01:55
* Package commits:
    - Target: 08831c
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
| `["findfirst", "n=1000", "reduce", "basesize=128"]` | 0.79 (5%) :white_check_mark: | 0.81 (1%) :white_check_mark: |
| `["findfirst", "n=1000", "reduce", "basesize=256"]` |                1.11 (5%) :x: |                1.05 (1%) :x: |
| `["findfirst", "n=400", "reduce", "basesize=128"]`  |                   1.03 (5%)  |                1.02 (1%) :x: |
| `["findfirst", "n=400", "reduce", "basesize=256"]`  |                1.06 (5%) :x: |                   1.00 (1%)  |
| `["findfirst", "n=400", "reduce", "basesize=512"]`  |                1.18 (5%) :x: |                1.03 (1%) :x: |
| `["findfirst", "n=500", "reduce", "basesize=128"]`  |                1.90 (5%) :x: |                1.58 (1%) :x: |
| `["findfirst", "n=500", "reduce", "basesize=256"]`  | 0.38 (5%) :white_check_mark: | 0.47 (1%) :white_check_mark: |
| `["findfirst", "n=500", "reduce", "basesize=512"]`  |                   1.00 (5%)  |                1.02 (1%) :x: |
| `["parallel_histogram", "assoc", "basesize=4096"]`  |                   0.96 (5%)  | 0.87 (1%) :white_check_mark: |
| `["parallel_histogram", "comm", "basesize=16384"]`  |                   1.01 (5%)  |                1.01 (1%) :x: |
| `["parallel_histogram", "comm", "basesize=4096"]`   |                1.10 (5%) :x: |                1.02 (1%) :x: |
| `["parallel_histogram", "comm", "basesize=8192"]`   |                   1.03 (5%)  | 0.99 (1%) :white_check_mark: |
| `["splitby", "count", "reduce"]`                    | 0.87 (5%) :white_check_mark: | 0.97 (1%) :white_check_mark: |
| `["words", "nthreads=2"]`                           |                   0.96 (5%)  | 0.99 (1%) :white_check_mark: |

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
      Ubuntu 24.04.1 LTS
  uname: Linux 6.8.0-1020-azure #23-Ubuntu SMP Mon Dec  9 16:58:58 UTC 2024 x86_64 x86_64
  CPU: AMD EPYC 7763 64-Core Processor: 
              speed         user         nice          sys         idle          irq
       #1  3573 MHz       2407 s          0 s        173 s       4333 s          0 s
       #2  3518 MHz       2258 s          0 s        169 s       4468 s          0 s
       #3  3518 MHz       2544 s          0 s        206 s       4163 s          0 s
       #4  3521 MHz       2826 s          0 s        233 s       3858 s          0 s
       
  Memory: 15.61526870727539 GB (8476.73046875 MB free)
  Uptime: 697.87 sec
  Load Avg:  1.73  1.54  0.94
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
      Ubuntu 24.04.1 LTS
  uname: Linux 6.8.0-1020-azure #23-Ubuntu SMP Mon Dec  9 16:58:58 UTC 2024 x86_64 x86_64
  CPU: AMD EPYC 7763 64-Core Processor: 
              speed         user         nice          sys         idle          irq
       #1  3514 MHz       3674 s          0 s        230 s       6073 s          0 s
       #2  3514 MHz       3321 s          0 s        230 s       6408 s          0 s
       #3  3515 MHz       3590 s          0 s        265 s       6124 s          0 s
       #4  3527 MHz       4207 s          0 s        341 s       5434 s          0 s
       
  Memory: 15.61526870727539 GB (8379.7265625 MB free)
  Uptime: 1004.89 sec
  Load Avg:  1.75  1.61  1.14
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-12.0.1 (ORCJIT, znver3)
```

---
# Target result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmark: 23 Jan 2025 - 1:50
* Package commit: 08831c
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
| `["collect", "assoc", "basesize=1"]`                | 140.432 ms (5%) |         |   4.36 MiB (1%) |       32800 |
| `["collect", "assoc", "basesize=1024"]`             | 138.860 ms (5%) |         |   1.09 MiB (1%) |          53 |
| `["collect", "assoc", "basesize=32"]`               | 139.954 ms (5%) |         |   1.48 MiB (1%) |        1052 |
| `["collect", "seq"]`                                | 273.793 ms (5%) |         | 256.05 KiB (1%) |           2 |
| `["collect", "unordered", "basesize=1"]`            | 235.550 ms (5%) |         |  23.72 MiB (1%) |      407254 |
| `["collect", "unordered", "basesize=1024"]`         | 149.784 ms (5%) |         |   1.01 MiB (1%) |        1027 |
| `["collect", "unordered", "basesize=32"]`           | 161.079 ms (5%) |         |   1.60 MiB (1%) |       15355 |
| `["findfirst", "n=1000", "foldl"]`                  | 478.197 ms (5%) |         |                 |             |
| `["findfirst", "n=1000", "reduce", "basesize=128"]` | 266.147 ms (5%) |         | 232.61 KiB (1%) |        3268 |
| `["findfirst", "n=1000", "reduce", "basesize=256"]` | 358.008 ms (5%) |         | 164.61 KiB (1%) |        2302 |
| `["findfirst", "n=1000", "reduce", "basesize=512"]` | 336.114 ms (5%) |         |  81.42 KiB (1%) |        1149 |
| `["findfirst", "n=400", "foldl"]`                   | 358.114 ms (5%) |         |                 |             |
| `["findfirst", "n=400", "reduce", "basesize=128"]`  | 191.716 ms (5%) |         | 383.14 KiB (1%) |        5453 |
| `["findfirst", "n=400", "reduce", "basesize=256"]`  | 198.442 ms (5%) |         | 200.67 KiB (1%) |        2867 |
| `["findfirst", "n=400", "reduce", "basesize=512"]`  | 249.774 ms (5%) |         | 137.97 KiB (1%) |        1971 |
| `["findfirst", "n=500", "foldl"]`                   |  61.425 ms (5%) |         |                 |             |
| `["findfirst", "n=500", "reduce", "basesize=128"]`  |  91.523 ms (5%) |         | 177.38 KiB (1%) |        2440 |
| `["findfirst", "n=500", "reduce", "basesize=256"]`  |  57.749 ms (5%) |         |  72.30 KiB (1%) |         992 |
| `["findfirst", "n=500", "reduce", "basesize=512"]`  |  80.103 ms (5%) |         |  56.86 KiB (1%) |         779 |
| `["overhead", "default"]`                           |  49.032 μs (5%) |         |  32.73 KiB (1%) |         418 |
| `["overhead", "stoppable=false"]`                   |  48.261 μs (5%) |         |  32.72 KiB (1%) |         417 |
| `["overhead", "stoppable=true"]`                    |  57.808 μs (5%) |         |  44.22 KiB (1%) |         609 |
| `["parallel_histogram", "assoc", "basesize=16384"]` |   2.208 ms (5%) |         | 728.91 KiB (1%) |          57 |
| `["parallel_histogram", "assoc", "basesize=4096"]`  |   2.710 ms (5%) |         |   1.79 MiB (1%) |         216 |
| `["parallel_histogram", "assoc", "basesize=8192"]`  |   2.499 ms (5%) |         |   1.42 MiB (1%) |         117 |
| `["parallel_histogram", "comm", "basesize=16384"]`  |   8.070 ms (5%) |         |   1.59 MiB (1%) |        2784 |
| `["parallel_histogram", "comm", "basesize=4096"]`   |  12.829 ms (5%) |         |   1.35 MiB (1%) |       10264 |
| `["parallel_histogram", "comm", "basesize=8192"]`   |  11.138 ms (5%) |         |   1.28 MiB (1%) |        7021 |
| `["parallel_histogram", "seq"]`                     |   3.932 ms (5%) |         | 364.16 KiB (1%) |          24 |
| `["partition_length_maximum", "rand", "foldl"]`     |  29.246 ms (5%) |         |                 |             |
| `["partition_length_maximum", "rand", "reduce"]`    |  14.601 ms (5%) |         |  736 bytes (1%) |          11 |
| `["splitby", "count", "foldl"]`                     |   1.430 ms (5%) |         |                 |             |
| `["splitby", "count", "man"]`                       |   1.074 ms (5%) |         |                 |             |
| `["splitby", "count", "reduce"]`                    | 670.701 μs (5%) |         |   1.06 KiB (1%) |          19 |
| `["sum", "random", "foldl"]`                        |  10.283 ms (5%) |         |                 |             |
| `["sum", "random", "reduce", "basesize=128"]`       |   5.235 ms (5%) |         |  74.19 KiB (1%) |        1104 |
| `["sum", "random", "reduce", "basesize=256"]`       |   5.166 ms (5%) |         |  36.78 KiB (1%) |         547 |
| `["sum", "random", "reduce", "basesize=512"]`       |   5.134 ms (5%) |         |  18.08 KiB (1%) |         269 |
| `["sum", "uniform", "foldl"]`                       |  10.085 ms (5%) |         |                 |             |
| `["sum", "uniform", "reduce", "basesize=128"]`      |   5.176 ms (5%) |         |  74.25 KiB (1%) |        1106 |
| `["sum", "uniform", "reduce", "basesize=256"]`      |   5.105 ms (5%) |         |  36.75 KiB (1%) |         546 |
| `["sum", "uniform", "reduce", "basesize=512"]`      |   5.073 ms (5%) |         |  18.08 KiB (1%) |         269 |
| `["sum", "valley", "foldl"]`                        |  10.284 ms (5%) |         |                 |             |
| `["sum", "valley", "reduce", "basesize=128"]`       |   5.268 ms (5%) |         |  74.09 KiB (1%) |        1101 |
| `["sum", "valley", "reduce", "basesize=256"]`       |   5.229 ms (5%) |         |  36.81 KiB (1%) |         548 |
| `["sum", "valley", "reduce", "basesize=512"]`       |   5.207 ms (5%) |         |  18.08 KiB (1%) |         269 |
| `["words", "nthreads=1"]`                           |  13.469 ms (5%) |         |  31.51 MiB (1%) |     1026258 |
| `["words", "nthreads=2"]`                           |   8.587 ms (5%) |         |  31.86 MiB (1%) |     1026297 |
| `["words", "nthreads=4"]`                           |   9.320 ms (5%) |         |  32.76 MiB (1%) |     1026459 |

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
      Ubuntu 24.04.1 LTS
  uname: Linux 6.8.0-1020-azure #23-Ubuntu SMP Mon Dec  9 16:58:58 UTC 2024 x86_64 x86_64
  CPU: AMD EPYC 7763 64-Core Processor: 
              speed         user         nice          sys         idle          irq
       #1  3573 MHz       2407 s          0 s        173 s       4333 s          0 s
       #2  3518 MHz       2258 s          0 s        169 s       4468 s          0 s
       #3  3518 MHz       2544 s          0 s        206 s       4163 s          0 s
       #4  3521 MHz       2826 s          0 s        233 s       3858 s          0 s
       
  Memory: 15.61526870727539 GB (8476.73046875 MB free)
  Uptime: 697.87 sec
  Load Avg:  1.73  1.54  0.94
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-12.0.1 (ORCJIT, znver3)
```

---
# Baseline result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmark: 23 Jan 2025 - 1:55
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
| `["collect", "assoc", "basesize=1"]`                | 145.372 ms (5%) |         |   4.36 MiB (1%) |       32800 |
| `["collect", "assoc", "basesize=1024"]`             | 139.896 ms (5%) |         |   1.09 MiB (1%) |          54 |
| `["collect", "assoc", "basesize=32"]`               | 140.125 ms (5%) |         |   1.48 MiB (1%) |        1052 |
| `["collect", "seq"]`                                | 278.128 ms (5%) |         | 256.05 KiB (1%) |           2 |
| `["collect", "unordered", "basesize=1"]`            | 242.151 ms (5%) |         |  23.71 MiB (1%) |      406872 |
| `["collect", "unordered", "basesize=1024"]`         | 148.418 ms (5%) |         |   1.01 MiB (1%) |        1089 |
| `["collect", "unordered", "basesize=32"]`           | 160.523 ms (5%) |         |   1.60 MiB (1%) |       15380 |
| `["findfirst", "n=1000", "foldl"]`                  | 471.363 ms (5%) |         |                 |             |
| `["findfirst", "n=1000", "reduce", "basesize=128"]` | 337.564 ms (5%) |         | 287.98 KiB (1%) |        4056 |
| `["findfirst", "n=1000", "reduce", "basesize=256"]` | 323.422 ms (5%) |         | 157.20 KiB (1%) |        2193 |
| `["findfirst", "n=1000", "reduce", "basesize=512"]` | 350.086 ms (5%) |         |  81.47 KiB (1%) |        1153 |
| `["findfirst", "n=400", "foldl"]`                   | 351.544 ms (5%) |         |                 |             |
| `["findfirst", "n=400", "reduce", "basesize=128"]`  | 185.635 ms (5%) |         | 375.94 KiB (1%) |        5361 |
| `["findfirst", "n=400", "reduce", "basesize=256"]`  | 187.417 ms (5%) |         | 200.86 KiB (1%) |        2873 |
| `["findfirst", "n=400", "reduce", "basesize=512"]`  | 212.516 ms (5%) |         | 133.50 KiB (1%) |        1896 |
| `["findfirst", "n=500", "foldl"]`                   |  60.988 ms (5%) |         |                 |             |
| `["findfirst", "n=500", "reduce", "basesize=128"]`  |  48.294 ms (5%) |         | 112.12 KiB (1%) |        1528 |
| `["findfirst", "n=500", "reduce", "basesize=256"]`  | 152.895 ms (5%) |         | 152.47 KiB (1%) |        2098 |
| `["findfirst", "n=500", "reduce", "basesize=512"]`  |  80.036 ms (5%) |         |  55.91 KiB (1%) |         763 |
| `["overhead", "default"]`                           |  48.300 μs (5%) |         |  32.73 KiB (1%) |         418 |
| `["overhead", "stoppable=false"]`                   |  50.113 μs (5%) |         |  32.75 KiB (1%) |         418 |
| `["overhead", "stoppable=true"]`                    |  56.855 μs (5%) |         |  44.25 KiB (1%) |         610 |
| `["parallel_histogram", "assoc", "basesize=16384"]` |   2.216 ms (5%) |         | 728.91 KiB (1%) |          57 |
| `["parallel_histogram", "assoc", "basesize=4096"]`  |   2.814 ms (5%) |         |   2.05 MiB (1%) |         222 |
| `["parallel_histogram", "assoc", "basesize=8192"]`  |   2.480 ms (5%) |         |   1.42 MiB (1%) |         117 |
| `["parallel_histogram", "comm", "basesize=16384"]`  |   7.963 ms (5%) |         |   1.57 MiB (1%) |        2056 |
| `["parallel_histogram", "comm", "basesize=4096"]`   |  11.673 ms (5%) |         |   1.32 MiB (1%) |        9378 |
| `["parallel_histogram", "comm", "basesize=8192"]`   |  10.826 ms (5%) |         |   1.29 MiB (1%) |        7662 |
| `["parallel_histogram", "seq"]`                     |   3.923 ms (5%) |         | 364.16 KiB (1%) |          24 |
| `["partition_length_maximum", "rand", "foldl"]`     |  29.285 ms (5%) |         |                 |             |
| `["partition_length_maximum", "rand", "reduce"]`    |  14.603 ms (5%) |         |  736 bytes (1%) |          11 |
| `["splitby", "count", "foldl"]`                     |   1.426 ms (5%) |         |                 |             |
| `["splitby", "count", "man"]`                       |   1.074 ms (5%) |         |                 |             |
| `["splitby", "count", "reduce"]`                    | 767.991 μs (5%) |         |   1.09 KiB (1%) |          19 |
| `["sum", "random", "foldl"]`                        |  10.204 ms (5%) |         |                 |             |
| `["sum", "random", "reduce", "basesize=128"]`       |   5.204 ms (5%) |         |  74.19 KiB (1%) |        1104 |
| `["sum", "random", "reduce", "basesize=256"]`       |   5.159 ms (5%) |         |  36.81 KiB (1%) |         548 |
| `["sum", "random", "reduce", "basesize=512"]`       |   5.140 ms (5%) |         |  18.08 KiB (1%) |         269 |
| `["sum", "uniform", "foldl"]`                       |  10.078 ms (5%) |         |                 |             |
| `["sum", "uniform", "reduce", "basesize=128"]`      |   5.169 ms (5%) |         |  74.19 KiB (1%) |        1104 |
| `["sum", "uniform", "reduce", "basesize=256"]`      |   5.117 ms (5%) |         |  36.78 KiB (1%) |         547 |
| `["sum", "uniform", "reduce", "basesize=512"]`      |   5.081 ms (5%) |         |  18.08 KiB (1%) |         269 |
| `["sum", "valley", "foldl"]`                        |  10.290 ms (5%) |         |                 |             |
| `["sum", "valley", "reduce", "basesize=128"]`       |   5.291 ms (5%) |         |  74.09 KiB (1%) |        1101 |
| `["sum", "valley", "reduce", "basesize=256"]`       |   5.224 ms (5%) |         |  36.72 KiB (1%) |         545 |
| `["sum", "valley", "reduce", "basesize=512"]`       |   5.202 ms (5%) |         |  18.08 KiB (1%) |         269 |
| `["words", "nthreads=1"]`                           |  13.679 ms (5%) |         |  31.52 MiB (1%) |     1026619 |
| `["words", "nthreads=2"]`                           |   8.969 ms (5%) |         |  32.23 MiB (1%) |     1026698 |
| `["words", "nthreads=4"]`                           |   9.238 ms (5%) |         |  32.68 MiB (1%) |     1026766 |

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
      Ubuntu 24.04.1 LTS
  uname: Linux 6.8.0-1020-azure #23-Ubuntu SMP Mon Dec  9 16:58:58 UTC 2024 x86_64 x86_64
  CPU: AMD EPYC 7763 64-Core Processor: 
              speed         user         nice          sys         idle          irq
       #1  3514 MHz       3674 s          0 s        230 s       6073 s          0 s
       #2  3514 MHz       3321 s          0 s        230 s       6408 s          0 s
       #3  3515 MHz       3590 s          0 s        265 s       6124 s          0 s
       #4  3527 MHz       4207 s          0 s        341 s       5434 s          0 s
       
  Memory: 15.61526870727539 GB (8379.7265625 MB free)
  Uptime: 1004.89 sec
  Load Avg:  1.75  1.61  1.14
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

