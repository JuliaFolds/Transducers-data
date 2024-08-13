# Multi-thread benchmark result

* Pull request commit: [`33d6e1d3815ebe763d8e0c33156f700408917659`](https://github.com/JuliaFolds/Transducers.jl/commit/33d6e1d3815ebe763d8e0c33156f700408917659)
* Pull request: <https://github.com/JuliaFolds/Transducers.jl/pull/243> (Update */Manifest.toml)

# Judge result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmarks:
    - Target: 13 Aug 2024 - 01:36
    - Baseline: 13 Aug 2024 - 01:41
* Package commits:
    - Target: 888f19
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
| `["findfirst", "n=1000", "reduce", "basesize=128"]` |                   0.96 (5%)  | 0.94 (1%) :white_check_mark: |
| `["findfirst", "n=1000", "reduce", "basesize=256"]` | 0.94 (5%) :white_check_mark: | 0.97 (1%) :white_check_mark: |
| `["findfirst", "n=1000", "reduce", "basesize=512"]` |                   0.99 (5%)  | 0.89 (1%) :white_check_mark: |
| `["findfirst", "n=400", "reduce", "basesize=512"]`  |                1.06 (5%) :x: | 0.99 (1%) :white_check_mark: |
| `["findfirst", "n=500", "reduce", "basesize=128"]`  |                1.19 (5%) :x: |                1.18 (1%) :x: |
| `["findfirst", "n=500", "reduce", "basesize=256"]`  | 0.27 (5%) :white_check_mark: | 0.38 (1%) :white_check_mark: |
| `["findfirst", "n=500", "reduce", "basesize=512"]`  | 0.84 (5%) :white_check_mark: | 0.91 (1%) :white_check_mark: |
| `["overhead", "default"]`                           |                1.07 (5%) :x: |                   1.00 (1%)  |
| `["parallel_histogram", "comm", "basesize=16384"]`  |                   1.03 (5%)  |                1.02 (1%) :x: |
| `["parallel_histogram", "comm", "basesize=4096"]`   |                   0.99 (5%)  |                1.04 (1%) :x: |
| `["splitby", "count", "reduce"]`                    |                   1.00 (5%)  |                1.05 (1%) :x: |
| `["words", "nthreads=2"]`                           | 0.94 (5%) :white_check_mark: |                   1.00 (1%)  |

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
      Ubuntu 22.04.4 LTS
  uname: Linux 6.5.0-1025-azure #26~22.04.1-Ubuntu SMP Thu Jul 11 22:33:04 UTC 2024 x86_64 x86_64
  CPU: AMD EPYC 7763 64-Core Processor: 
              speed         user         nice          sys         idle          irq
       #1  3114 MHz       2513 s          0 s        144 s       4982 s          0 s
       #2  2445 MHz       2441 s          0 s        155 s       5050 s          0 s
       #3  3240 MHz       2294 s          0 s        172 s       5167 s          0 s
       #4  3241 MHz       2746 s          0 s        187 s       4697 s          0 s
       
  Memory: 15.606491088867188 GB (12570.58984375 MB free)
  Uptime: 767.94 sec
  Load Avg:  1.61  1.48  0.86
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
      Ubuntu 22.04.4 LTS
  uname: Linux 6.5.0-1025-azure #26~22.04.1-Ubuntu SMP Thu Jul 11 22:33:04 UTC 2024 x86_64 x86_64
  CPU: AMD EPYC 7763 64-Core Processor: 
              speed         user         nice          sys         idle          irq
       #1  3116 MHz       3443 s          0 s        193 s       6915 s          0 s
       #2  2445 MHz       4199 s          0 s        215 s       6144 s          0 s
       #3  3237 MHz       3319 s          0 s        219 s       7007 s          0 s
       #4  3244 MHz       3640 s          0 s        236 s       6668 s          0 s
       
  Memory: 15.606491088867188 GB (12458.8828125 MB free)
  Uptime: 1059.86 sec
  Load Avg:  1.76  1.67  1.12
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-12.0.1 (ORCJIT, znver3)
```

---
# Target result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmark: 13 Aug 2024 - 1:36
* Package commit: 888f19
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
| `["collect", "assoc", "basesize=1"]`                | 148.613 ms (5%) |         |   4.36 MiB (1%) |       32800 |
| `["collect", "assoc", "basesize=1024"]`             | 147.412 ms (5%) |         |   1.09 MiB (1%) |          53 |
| `["collect", "assoc", "basesize=32"]`               | 147.562 ms (5%) |         |   1.48 MiB (1%) |        1052 |
| `["collect", "seq"]`                                | 294.546 ms (5%) |         | 256.05 KiB (1%) |           2 |
| `["collect", "unordered", "basesize=1"]`            | 245.213 ms (5%) |         |  23.80 MiB (1%) |      409807 |
| `["collect", "unordered", "basesize=1024"]`         | 155.909 ms (5%) |         |   1.01 MiB (1%) |        1148 |
| `["collect", "unordered", "basesize=32"]`           | 163.394 ms (5%) |         |   1.60 MiB (1%) |       15214 |
| `["findfirst", "n=1000", "foldl"]`                  | 507.086 ms (5%) |         |                 |             |
| `["findfirst", "n=1000", "reduce", "basesize=128"]` | 276.200 ms (5%) |         | 232.83 KiB (1%) |        3275 |
| `["findfirst", "n=1000", "reduce", "basesize=256"]` | 323.796 ms (5%) |         | 152.97 KiB (1%) |        2129 |
| `["findfirst", "n=1000", "reduce", "basesize=512"]` | 391.602 ms (5%) |         |  86.41 KiB (1%) |        1224 |
| `["findfirst", "n=400", "foldl"]`                   | 378.991 ms (5%) |         |                 |             |
| `["findfirst", "n=400", "reduce", "basesize=128"]`  | 196.412 ms (5%) |         | 384.38 KiB (1%) |        5480 |
| `["findfirst", "n=400", "reduce", "basesize=256"]`  | 198.588 ms (5%) |         | 201.11 KiB (1%) |        2881 |
| `["findfirst", "n=400", "reduce", "basesize=512"]`  | 219.952 ms (5%) |         | 112.59 KiB (1%) |        1622 |
| `["findfirst", "n=500", "foldl"]`                   |  65.006 ms (5%) |         |                 |             |
| `["findfirst", "n=500", "reduce", "basesize=128"]`  | 127.653 ms (5%) |         | 232.84 KiB (1%) |        3211 |
| `["findfirst", "n=500", "reduce", "basesize=256"]`  |  50.524 ms (5%) |         |  64.25 KiB (1%) |         873 |
| `["findfirst", "n=500", "reduce", "basesize=512"]`  |  67.130 ms (5%) |         |  49.62 KiB (1%) |         672 |
| `["overhead", "default"]`                           |  53.710 μs (5%) |         |  32.70 KiB (1%) |         417 |
| `["overhead", "stoppable=false"]`                   |  52.828 μs (5%) |         |  32.75 KiB (1%) |         418 |
| `["overhead", "stoppable=true"]`                    |  60.513 μs (5%) |         |  44.25 KiB (1%) |         610 |
| `["parallel_histogram", "assoc", "basesize=16384"]` |   2.372 ms (5%) |         | 728.91 KiB (1%) |          57 |
| `["parallel_histogram", "assoc", "basesize=4096"]`  |   2.943 ms (5%) |         |   1.79 MiB (1%) |         216 |
| `["parallel_histogram", "assoc", "basesize=8192"]`  |   2.654 ms (5%) |         |   1.42 MiB (1%) |         117 |
| `["parallel_histogram", "comm", "basesize=16384"]`  |   8.542 ms (5%) |         |   1.59 MiB (1%) |        2807 |
| `["parallel_histogram", "comm", "basesize=4096"]`   |  14.103 ms (5%) |         |   1.33 MiB (1%) |        9884 |
| `["parallel_histogram", "comm", "basesize=8192"]`   |  12.089 ms (5%) |         |   1.27 MiB (1%) |        6879 |
| `["parallel_histogram", "seq"]`                     |   4.235 ms (5%) |         | 364.16 KiB (1%) |          24 |
| `["partition_length_maximum", "rand", "foldl"]`     |  31.114 ms (5%) |         |                 |             |
| `["partition_length_maximum", "rand", "reduce"]`    |  15.567 ms (5%) |         |  736 bytes (1%) |          11 |
| `["splitby", "count", "foldl"]`                     |   1.481 ms (5%) |         |                 |             |
| `["splitby", "count", "man"]`                       |   1.158 ms (5%) |         |                 |             |
| `["splitby", "count", "reduce"]`                    | 721.308 μs (5%) |         |   1.06 KiB (1%) |          18 |
| `["sum", "random", "foldl"]`                        |  11.072 ms (5%) |         |                 |             |
| `["sum", "random", "reduce", "basesize=128"]`       |   5.678 ms (5%) |         |  74.02 KiB (1%) |        1099 |
| `["sum", "random", "reduce", "basesize=256"]`       |   5.614 ms (5%) |         |  36.73 KiB (1%) |         546 |
| `["sum", "random", "reduce", "basesize=512"]`       |   5.576 ms (5%) |         |  18.08 KiB (1%) |         269 |
| `["sum", "uniform", "foldl"]`                       |  10.867 ms (5%) |         |                 |             |
| `["sum", "uniform", "reduce", "basesize=128"]`      |   5.593 ms (5%) |         |  74.11 KiB (1%) |        1102 |
| `["sum", "uniform", "reduce", "basesize=256"]`      |   5.527 ms (5%) |         |  36.77 KiB (1%) |         547 |
| `["sum", "uniform", "reduce", "basesize=512"]`      |   5.489 ms (5%) |         |  17.97 KiB (1%) |         266 |
| `["sum", "valley", "foldl"]`                        |  11.114 ms (5%) |         |                 |             |
| `["sum", "valley", "reduce", "basesize=128"]`       |   5.701 ms (5%) |         |  74.02 KiB (1%) |        1099 |
| `["sum", "valley", "reduce", "basesize=256"]`       |   5.637 ms (5%) |         |  36.70 KiB (1%) |         545 |
| `["sum", "valley", "reduce", "basesize=512"]`       |   5.601 ms (5%) |         |  18.09 KiB (1%) |         270 |
| `["words", "nthreads=1"]`                           |  14.167 ms (5%) |         |  31.72 MiB (1%) |     1033893 |
| `["words", "nthreads=2"]`                           |   9.374 ms (5%) |         |  32.43 MiB (1%) |     1033966 |
| `["words", "nthreads=4"]`                           |   9.887 ms (5%) |         |  33.06 MiB (1%) |     1034112 |

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
      Ubuntu 22.04.4 LTS
  uname: Linux 6.5.0-1025-azure #26~22.04.1-Ubuntu SMP Thu Jul 11 22:33:04 UTC 2024 x86_64 x86_64
  CPU: AMD EPYC 7763 64-Core Processor: 
              speed         user         nice          sys         idle          irq
       #1  3114 MHz       2513 s          0 s        144 s       4982 s          0 s
       #2  2445 MHz       2441 s          0 s        155 s       5050 s          0 s
       #3  3240 MHz       2294 s          0 s        172 s       5167 s          0 s
       #4  3241 MHz       2746 s          0 s        187 s       4697 s          0 s
       
  Memory: 15.606491088867188 GB (12570.58984375 MB free)
  Uptime: 767.94 sec
  Load Avg:  1.61  1.48  0.86
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-12.0.1 (ORCJIT, znver3)
```

---
# Baseline result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmark: 13 Aug 2024 - 1:41
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
| `["collect", "assoc", "basesize=1"]`                | 148.535 ms (5%) |         |   4.36 MiB (1%) |       32800 |
| `["collect", "assoc", "basesize=1024"]`             | 147.570 ms (5%) |         |   1.09 MiB (1%) |          53 |
| `["collect", "assoc", "basesize=32"]`               | 147.525 ms (5%) |         |   1.48 MiB (1%) |        1052 |
| `["collect", "seq"]`                                | 294.594 ms (5%) |         | 256.05 KiB (1%) |           2 |
| `["collect", "unordered", "basesize=1"]`            | 245.140 ms (5%) |         |  23.81 MiB (1%) |      410132 |
| `["collect", "unordered", "basesize=1024"]`         | 156.521 ms (5%) |         |   1.01 MiB (1%) |        1112 |
| `["collect", "unordered", "basesize=32"]`           | 163.611 ms (5%) |         |   1.60 MiB (1%) |       15177 |
| `["findfirst", "n=1000", "foldl"]`                  | 504.665 ms (5%) |         |                 |             |
| `["findfirst", "n=1000", "reduce", "basesize=128"]` | 287.917 ms (5%) |         | 248.78 KiB (1%) |        3484 |
| `["findfirst", "n=1000", "reduce", "basesize=256"]` | 343.225 ms (5%) |         | 157.20 KiB (1%) |        2193 |
| `["findfirst", "n=1000", "reduce", "basesize=512"]` | 394.077 ms (5%) |         |  96.75 KiB (1%) |        1346 |
| `["findfirst", "n=400", "foldl"]`                   | 377.674 ms (5%) |         |                 |             |
| `["findfirst", "n=400", "reduce", "basesize=128"]`  | 194.439 ms (5%) |         | 383.12 KiB (1%) |        5454 |
| `["findfirst", "n=400", "reduce", "basesize=256"]`  | 197.432 ms (5%) |         | 200.92 KiB (1%) |        2875 |
| `["findfirst", "n=400", "reduce", "basesize=512"]`  | 208.066 ms (5%) |         | 114.30 KiB (1%) |        1633 |
| `["findfirst", "n=500", "foldl"]`                   |  64.712 ms (5%) |         |                 |             |
| `["findfirst", "n=500", "reduce", "basesize=128"]`  | 107.406 ms (5%) |         | 197.83 KiB (1%) |        2723 |
| `["findfirst", "n=500", "reduce", "basesize=256"]`  | 183.941 ms (5%) |         | 168.56 KiB (1%) |        2371 |
| `["findfirst", "n=500", "reduce", "basesize=512"]`  |  80.043 ms (5%) |         |  54.38 KiB (1%) |         744 |
| `["overhead", "default"]`                           |  50.404 μs (5%) |         |  32.67 KiB (1%) |         416 |
| `["overhead", "stoppable=false"]`                   |  53.340 μs (5%) |         |  32.78 KiB (1%) |         419 |
| `["overhead", "stoppable=true"]`                    |  60.073 μs (5%) |         |  44.25 KiB (1%) |         610 |
| `["parallel_histogram", "assoc", "basesize=16384"]` |   2.368 ms (5%) |         | 728.91 KiB (1%) |          57 |
| `["parallel_histogram", "assoc", "basesize=4096"]`  |   2.920 ms (5%) |         |   1.79 MiB (1%) |         216 |
| `["parallel_histogram", "assoc", "basesize=8192"]`  |   2.647 ms (5%) |         |   1.42 MiB (1%) |         117 |
| `["parallel_histogram", "comm", "basesize=16384"]`  |   8.255 ms (5%) |         |   1.56 MiB (1%) |        1945 |
| `["parallel_histogram", "comm", "basesize=4096"]`   |  14.187 ms (5%) |         |   1.28 MiB (1%) |        8180 |
| `["parallel_histogram", "comm", "basesize=8192"]`   |  12.562 ms (5%) |         |   1.27 MiB (1%) |        7869 |
| `["parallel_histogram", "seq"]`                     |   4.233 ms (5%) |         | 364.16 KiB (1%) |          24 |
| `["partition_length_maximum", "rand", "foldl"]`     |  31.113 ms (5%) |         |                 |             |
| `["partition_length_maximum", "rand", "reduce"]`    |  15.567 ms (5%) |         |  736 bytes (1%) |          11 |
| `["splitby", "count", "foldl"]`                     |   1.533 ms (5%) |         |                 |             |
| `["splitby", "count", "man"]`                       |   1.157 ms (5%) |         |                 |             |
| `["splitby", "count", "reduce"]`                    | 719.593 μs (5%) |         |   1.02 KiB (1%) |          18 |
| `["sum", "random", "foldl"]`                        |  10.983 ms (5%) |         |                 |             |
| `["sum", "random", "reduce", "basesize=128"]`       |   5.595 ms (5%) |         |  74.08 KiB (1%) |        1101 |
| `["sum", "random", "reduce", "basesize=256"]`       |   5.560 ms (5%) |         |  36.70 KiB (1%) |         545 |
| `["sum", "random", "reduce", "basesize=512"]`       |   5.527 ms (5%) |         |  18.11 KiB (1%) |         270 |
| `["sum", "uniform", "foldl"]`                       |  10.878 ms (5%) |         |                 |             |
| `["sum", "uniform", "reduce", "basesize=128"]`      |   5.563 ms (5%) |         |  74.17 KiB (1%) |        1104 |
| `["sum", "uniform", "reduce", "basesize=256"]`      |   5.513 ms (5%) |         |  36.67 KiB (1%) |         544 |
| `["sum", "uniform", "reduce", "basesize=512"]`      |   5.472 ms (5%) |         |  17.97 KiB (1%) |         266 |
| `["sum", "valley", "foldl"]`                        |  11.109 ms (5%) |         |                 |             |
| `["sum", "valley", "reduce", "basesize=128"]`       |   5.696 ms (5%) |         |  74.02 KiB (1%) |        1099 |
| `["sum", "valley", "reduce", "basesize=256"]`       |   5.636 ms (5%) |         |  36.70 KiB (1%) |         545 |
| `["sum", "valley", "reduce", "basesize=512"]`       |   5.605 ms (5%) |         |  18.03 KiB (1%) |         268 |
| `["words", "nthreads=1"]`                           |  14.340 ms (5%) |         |  31.61 MiB (1%) |     1029537 |
| `["words", "nthreads=2"]`                           |   9.964 ms (5%) |         |  32.32 MiB (1%) |     1029648 |
| `["words", "nthreads=4"]`                           |  10.144 ms (5%) |         |  32.77 MiB (1%) |     1029726 |

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
      Ubuntu 22.04.4 LTS
  uname: Linux 6.5.0-1025-azure #26~22.04.1-Ubuntu SMP Thu Jul 11 22:33:04 UTC 2024 x86_64 x86_64
  CPU: AMD EPYC 7763 64-Core Processor: 
              speed         user         nice          sys         idle          irq
       #1  3116 MHz       3443 s          0 s        193 s       6915 s          0 s
       #2  2445 MHz       4199 s          0 s        215 s       6144 s          0 s
       #3  3237 MHz       3319 s          0 s        219 s       7007 s          0 s
       #4  3244 MHz       3640 s          0 s        236 s       6668 s          0 s
       
  Memory: 15.606491088867188 GB (12458.8828125 MB free)
  Uptime: 1059.86 sec
  Load Avg:  1.76  1.67  1.12
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
    Vulnerability Spec rstack overflow: Vulnerable: Safe RET, no microcode
    Vulnerability Spec store bypass:    Vulnerable
    Vulnerability Spectre v1:           Mitigation; usercopy/swapgs barriers and __user pointer sanitization
    Vulnerability Spectre v2:           Mitigation; Retpolines; STIBP disabled; RSB filling; PBRSB-eIBRS Not affected; BHI Not affected
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

