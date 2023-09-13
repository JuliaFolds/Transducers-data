# Multi-thread benchmark result

* Pull request commit: [`d9bae75c6be293d41677386624fec003eadd0213`](https://github.com/JuliaFolds/Transducers.jl/commit/d9bae75c6be293d41677386624fec003eadd0213)
* Pull request: <https://github.com/JuliaFolds/Transducers.jl/pull/243> (Update */Manifest.toml)

# Judge result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmarks:
    - Target: 13 Sep 2023 - 01:26
    - Baseline: 13 Sep 2023 - 01:32
* Package commits:
    - Target: 62f6c7
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
| `["findfirst", "n=1000", "reduce", "basesize=128"]` |                1.47 (5%) :x: |                1.39 (1%) :x: |
| `["findfirst", "n=1000", "reduce", "basesize=256"]` |                1.05 (5%) :x: |                1.06 (1%) :x: |
| `["findfirst", "n=400", "reduce", "basesize=256"]`  |                   0.96 (5%)  | 0.97 (1%) :white_check_mark: |
| `["findfirst", "n=400", "reduce", "basesize=512"]`  | 0.89 (5%) :white_check_mark: | 0.94 (1%) :white_check_mark: |
| `["findfirst", "n=500", "reduce", "basesize=128"]`  | 0.92 (5%) :white_check_mark: | 0.89 (1%) :white_check_mark: |
| `["findfirst", "n=500", "reduce", "basesize=256"]`  | 0.42 (5%) :white_check_mark: | 0.52 (1%) :white_check_mark: |
| `["overhead", "stoppable=false"]`                   | 0.95 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["parallel_histogram", "comm", "basesize=4096"]`   |                   0.99 (5%)  |                1.03 (1%) :x: |
| `["parallel_histogram", "comm", "basesize=8192"]`   | 0.84 (5%) :white_check_mark: |                   0.99 (1%)  |
| `["splitby", "count", "reduce"]`                    |                   0.98 (5%)  |                1.03 (1%) :x: |
| `["words", "nthreads=1"]`                           |                   0.95 (5%)  | 0.99 (1%) :white_check_mark: |
| `["words", "nthreads=2"]`                           | 0.91 (5%) :white_check_mark: |                   1.00 (1%)  |

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
  uname: Linux 5.15.0-1041-azure #48-Ubuntu SMP Tue Jun 20 20:34:08 UTC 2023 x86_64 x86_64
  CPU: Intel(R) Xeon(R) CPU E5-2673 v4 @ 2.30GHz: 
              speed         user         nice          sys         idle          irq
       #1  2294 MHz       6157 s          0 s        360 s       1439 s          0 s
       #2  2294 MHz       5163 s          0 s        407 s       2350 s          0 s
       
  Memory: 6.7694854736328125 GB (3451.703125 MB free)
  Uptime: 806.6 sec
  Load Avg:  1.67  1.58  1.06
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-12.0.1 (ORCJIT, broadwell)
```

### Baseline
```
Julia Version 1.7.3
Commit 742b9abb4d (2022-05-06 12:58 UTC)
Platform Info:
  OS: Linux (x86_64-pc-linux-gnu)
      Ubuntu 22.04.3 LTS
  uname: Linux 5.15.0-1041-azure #48-Ubuntu SMP Tue Jun 20 20:34:08 UTC 2023 x86_64 x86_64
  CPU: Intel(R) Xeon(R) CPU E5-2673 v4 @ 2.30GHz: 
              speed         user         nice          sys         idle          irq
       #1  2294 MHz       8724 s          0 s        476 s       2212 s          0 s
       #2  2294 MHz       7642 s          0 s        512 s       3221 s          0 s
       
  Memory: 6.7694854736328125 GB (3404.1640625 MB free)
  Uptime: 1153.23 sec
  Load Avg:  1.64  1.6  1.23
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-12.0.1 (ORCJIT, broadwell)
```

---
# Target result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmark: 13 Sep 2023 - 1:26
* Package commit: 62f6c7
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
| `["collect", "assoc", "basesize=1"]`                | 204.332 ms (5%) |         |   4.36 MiB (1%) |       32800 |
| `["collect", "assoc", "basesize=1024"]`             | 197.516 ms (5%) |         |   1.09 MiB (1%) |          53 |
| `["collect", "assoc", "basesize=32"]`               | 204.895 ms (5%) |         |   1.48 MiB (1%) |        1052 |
| `["collect", "seq"]`                                | 397.934 ms (5%) |         | 256.05 KiB (1%) |           2 |
| `["collect", "unordered", "basesize=1"]`            | 434.704 ms (5%) |         |  23.91 MiB (1%) |      413291 |
| `["collect", "unordered", "basesize=1024"]`         | 218.902 ms (5%) |         |   1.02 MiB (1%) |        1352 |
| `["collect", "unordered", "basesize=32"]`           | 242.047 ms (5%) |         |   1.61 MiB (1%) |       15511 |
| `["findfirst", "n=1000", "foldl"]`                  | 661.626 ms (5%) |         |                 |             |
| `["findfirst", "n=1000", "reduce", "basesize=128"]` | 531.114 ms (5%) |         | 319.19 KiB (1%) |        4483 |
| `["findfirst", "n=1000", "reduce", "basesize=256"]` | 541.501 ms (5%) |         | 178.81 KiB (1%) |        2511 |
| `["findfirst", "n=1000", "reduce", "basesize=512"]` | 601.515 ms (5%) |         | 108.70 KiB (1%) |        1514 |
| `["findfirst", "n=400", "foldl"]`                   | 475.134 ms (5%) |         |                 |             |
| `["findfirst", "n=400", "reduce", "basesize=128"]`  | 265.709 ms (5%) |         | 394.09 KiB (1%) |        5614 |
| `["findfirst", "n=400", "reduce", "basesize=256"]`  | 263.404 ms (5%) |         | 200.83 KiB (1%) |        2872 |
| `["findfirst", "n=400", "reduce", "basesize=512"]`  | 327.673 ms (5%) |         | 134.38 KiB (1%) |        1916 |
| `["findfirst", "n=500", "foldl"]`                   |  83.041 ms (5%) |         |                 |             |
| `["findfirst", "n=500", "reduce", "basesize=128"]`  | 139.399 ms (5%) |         | 185.66 KiB (1%) |        2543 |
| `["findfirst", "n=500", "reduce", "basesize=256"]`  |  80.646 ms (5%) |         |  72.36 KiB (1%) |         986 |
| `["findfirst", "n=500", "reduce", "basesize=512"]`  | 122.886 ms (5%) |         |  63.59 KiB (1%) |         863 |
| `["overhead", "default"]`                           |  82.200 μs (5%) |         |  32.73 KiB (1%) |         418 |
| `["overhead", "stoppable=false"]`                   |  83.300 μs (5%) |         |  32.78 KiB (1%) |         419 |
| `["overhead", "stoppable=true"]`                    | 102.804 μs (5%) |         |  44.28 KiB (1%) |         611 |
| `["parallel_histogram", "assoc", "basesize=16384"]` |   3.312 ms (5%) |         | 728.91 KiB (1%) |          57 |
| `["parallel_histogram", "assoc", "basesize=4096"]`  |   4.180 ms (5%) |         |   1.79 MiB (1%) |         215 |
| `["parallel_histogram", "assoc", "basesize=8192"]`  |   3.664 ms (5%) |         |   1.42 MiB (1%) |         117 |
| `["parallel_histogram", "comm", "basesize=16384"]`  |  16.272 ms (5%) |         |   1.51 MiB (1%) |         145 |
| `["parallel_histogram", "comm", "basesize=4096"]`   |  22.771 ms (5%) |         |   1.15 MiB (1%) |        3766 |
| `["parallel_histogram", "comm", "basesize=8192"]`   |  18.083 ms (5%) |         |   1.04 MiB (1%) |         169 |
| `["parallel_histogram", "seq"]`                     |   5.830 ms (5%) |         | 364.16 KiB (1%) |          24 |
| `["partition_length_maximum", "rand", "foldl"]`     |  43.586 ms (5%) |         |                 |             |
| `["partition_length_maximum", "rand", "reduce"]`    |  21.158 ms (5%) |         |  736 bytes (1%) |          11 |
| `["splitby", "count", "foldl"]`                     |   2.128 ms (5%) |         |                 |             |
| `["splitby", "count", "man"]`                       |   1.638 ms (5%) |         |                 |             |
| `["splitby", "count", "reduce"]`                    | 950.710 μs (5%) |         |   1.09 KiB (1%) |          19 |
| `["sum", "random", "foldl"]`                        |  16.162 ms (5%) |         |                 |             |
| `["sum", "random", "reduce", "basesize=128"]`       |   8.163 ms (5%) |         |  74.11 KiB (1%) |        1102 |
| `["sum", "random", "reduce", "basesize=256"]`       |   8.128 ms (5%) |         |  36.70 KiB (1%) |         545 |
| `["sum", "random", "reduce", "basesize=512"]`       |   7.983 ms (5%) |         |  18.05 KiB (1%) |         268 |
| `["sum", "uniform", "foldl"]`                       |  15.324 ms (5%) |         |                 |             |
| `["sum", "uniform", "reduce", "basesize=128"]`      |   8.045 ms (5%) |         |  74.14 KiB (1%) |        1103 |
| `["sum", "uniform", "reduce", "basesize=256"]`      |   7.750 ms (5%) |         |  36.70 KiB (1%) |         545 |
| `["sum", "uniform", "reduce", "basesize=512"]`      |   7.667 ms (5%) |         |  18.03 KiB (1%) |         268 |
| `["sum", "valley", "foldl"]`                        |  15.994 ms (5%) |         |                 |             |
| `["sum", "valley", "reduce", "basesize=128"]`       |   8.230 ms (5%) |         |  74.05 KiB (1%) |        1100 |
| `["sum", "valley", "reduce", "basesize=256"]`       |   8.191 ms (5%) |         |  36.73 KiB (1%) |         546 |
| `["sum", "valley", "reduce", "basesize=512"]`       |   8.105 ms (5%) |         |  18.00 KiB (1%) |         267 |
| `["words", "nthreads=1"]`                           |  32.508 ms (5%) |         |  31.51 MiB (1%) |     1026545 |
| `["words", "nthreads=2"]`                           |  18.596 ms (5%) |         |  32.22 MiB (1%) |     1026626 |
| `["words", "nthreads=4"]`                           |  19.279 ms (5%) |         |  32.85 MiB (1%) |     1026753 |

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
  uname: Linux 5.15.0-1041-azure #48-Ubuntu SMP Tue Jun 20 20:34:08 UTC 2023 x86_64 x86_64
  CPU: Intel(R) Xeon(R) CPU E5-2673 v4 @ 2.30GHz: 
              speed         user         nice          sys         idle          irq
       #1  2294 MHz       6157 s          0 s        360 s       1439 s          0 s
       #2  2294 MHz       5163 s          0 s        407 s       2350 s          0 s
       
  Memory: 6.7694854736328125 GB (3451.703125 MB free)
  Uptime: 806.6 sec
  Load Avg:  1.67  1.58  1.06
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-12.0.1 (ORCJIT, broadwell)
```

---
# Baseline result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmark: 13 Sep 2023 - 1:32
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
| `["collect", "assoc", "basesize=1"]`                | 209.602 ms (5%) |         |   4.36 MiB (1%) |       32800 |
| `["collect", "assoc", "basesize=1024"]`             | 207.646 ms (5%) |         |   1.09 MiB (1%) |          53 |
| `["collect", "assoc", "basesize=32"]`               | 205.883 ms (5%) |         |   1.48 MiB (1%) |        1052 |
| `["collect", "seq"]`                                | 410.661 ms (5%) |         | 256.05 KiB (1%) |           2 |
| `["collect", "unordered", "basesize=1"]`            | 434.143 ms (5%) |         |  23.87 MiB (1%) |      412051 |
| `["collect", "unordered", "basesize=1024"]`         | 226.655 ms (5%) |         |   1.02 MiB (1%) |        1344 |
| `["collect", "unordered", "basesize=32"]`           | 236.551 ms (5%) |         |   1.60 MiB (1%) |       15308 |
| `["findfirst", "n=1000", "foldl"]`                  | 660.012 ms (5%) |         |                 |             |
| `["findfirst", "n=1000", "reduce", "basesize=128"]` | 360.619 ms (5%) |         | 230.39 KiB (1%) |        3242 |
| `["findfirst", "n=1000", "reduce", "basesize=256"]` | 513.699 ms (5%) |         | 167.95 KiB (1%) |        2347 |
| `["findfirst", "n=1000", "reduce", "basesize=512"]` | 576.160 ms (5%) |         | 108.55 KiB (1%) |        1509 |
| `["findfirst", "n=400", "foldl"]`                   | 488.318 ms (5%) |         |                 |             |
| `["findfirst", "n=400", "reduce", "basesize=128"]`  | 273.449 ms (5%) |         | 391.73 KiB (1%) |        5565 |
| `["findfirst", "n=400", "reduce", "basesize=256"]`  | 275.061 ms (5%) |         | 207.39 KiB (1%) |        2962 |
| `["findfirst", "n=400", "reduce", "basesize=512"]`  | 366.482 ms (5%) |         | 143.34 KiB (1%) |        2045 |
| `["findfirst", "n=500", "foldl"]`                   |  80.368 ms (5%) |         |                 |             |
| `["findfirst", "n=500", "reduce", "basesize=128"]`  | 152.058 ms (5%) |         | 208.62 KiB (1%) |        2870 |
| `["findfirst", "n=500", "reduce", "basesize=256"]`  | 192.014 ms (5%) |         | 138.34 KiB (1%) |        1913 |
| `["findfirst", "n=500", "reduce", "basesize=512"]`  | 125.870 ms (5%) |         |  63.61 KiB (1%) |         864 |
| `["overhead", "default"]`                           |  84.518 μs (5%) |         |  32.77 KiB (1%) |         419 |
| `["overhead", "stoppable=false"]`                   |  88.101 μs (5%) |         |  32.78 KiB (1%) |         419 |
| `["overhead", "stoppable=true"]`                    | 101.702 μs (5%) |         |  44.25 KiB (1%) |         610 |
| `["parallel_histogram", "assoc", "basesize=16384"]` |   3.293 ms (5%) |         | 728.91 KiB (1%) |          57 |
| `["parallel_histogram", "assoc", "basesize=4096"]`  |   4.114 ms (5%) |         |   1.79 MiB (1%) |         215 |
| `["parallel_histogram", "assoc", "basesize=8192"]`  |   3.789 ms (5%) |         |   1.42 MiB (1%) |         117 |
| `["parallel_histogram", "comm", "basesize=16384"]`  |  15.761 ms (5%) |         |   1.51 MiB (1%) |         144 |
| `["parallel_histogram", "comm", "basesize=4096"]`   |  22.904 ms (5%) |         |   1.11 MiB (1%) |        2686 |
| `["parallel_histogram", "comm", "basesize=8192"]`   |  21.637 ms (5%) |         |   1.04 MiB (1%) |         356 |
| `["parallel_histogram", "seq"]`                     |   5.789 ms (5%) |         | 364.16 KiB (1%) |          24 |
| `["partition_length_maximum", "rand", "foldl"]`     |  42.691 ms (5%) |         |                 |             |
| `["partition_length_maximum", "rand", "reduce"]`    |  21.610 ms (5%) |         |  736 bytes (1%) |          11 |
| `["splitby", "count", "foldl"]`                     |   2.113 ms (5%) |         |                 |             |
| `["splitby", "count", "man"]`                       |   1.641 ms (5%) |         |                 |             |
| `["splitby", "count", "reduce"]`                    | 970.409 μs (5%) |         |   1.06 KiB (1%) |          18 |
| `["sum", "random", "foldl"]`                        |  15.939 ms (5%) |         |                 |             |
| `["sum", "random", "reduce", "basesize=128"]`       |   8.065 ms (5%) |         |  74.14 KiB (1%) |        1103 |
| `["sum", "random", "reduce", "basesize=256"]`       |   8.122 ms (5%) |         |  36.70 KiB (1%) |         545 |
| `["sum", "random", "reduce", "basesize=512"]`       |   8.006 ms (5%) |         |  18.05 KiB (1%) |         268 |
| `["sum", "uniform", "foldl"]`                       |  15.397 ms (5%) |         |                 |             |
| `["sum", "uniform", "reduce", "basesize=128"]`      |   7.958 ms (5%) |         |  74.14 KiB (1%) |        1103 |
| `["sum", "uniform", "reduce", "basesize=256"]`      |   7.918 ms (5%) |         |  36.77 KiB (1%) |         547 |
| `["sum", "uniform", "reduce", "basesize=512"]`      |   7.692 ms (5%) |         |  18.03 KiB (1%) |         268 |
| `["sum", "valley", "foldl"]`                        |  16.098 ms (5%) |         |                 |             |
| `["sum", "valley", "reduce", "basesize=128"]`       |   8.296 ms (5%) |         |  74.11 KiB (1%) |        1102 |
| `["sum", "valley", "reduce", "basesize=256"]`       |   8.111 ms (5%) |         |  36.73 KiB (1%) |         546 |
| `["sum", "valley", "reduce", "basesize=512"]`       |   8.038 ms (5%) |         |  17.97 KiB (1%) |         266 |
| `["words", "nthreads=1"]`                           |  34.112 ms (5%) |         |  31.86 MiB (1%) |     1038414 |
| `["words", "nthreads=2"]`                           |  20.350 ms (5%) |         |  32.22 MiB (1%) |     1038465 |
| `["words", "nthreads=4"]`                           |  20.276 ms (5%) |         |  33.11 MiB (1%) |     1038642 |

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
  uname: Linux 5.15.0-1041-azure #48-Ubuntu SMP Tue Jun 20 20:34:08 UTC 2023 x86_64 x86_64
  CPU: Intel(R) Xeon(R) CPU E5-2673 v4 @ 2.30GHz: 
              speed         user         nice          sys         idle          irq
       #1  2294 MHz       8724 s          0 s        476 s       2212 s          0 s
       #2  2294 MHz       7642 s          0 s        512 s       3221 s          0 s
       
  Memory: 6.7694854736328125 GB (3404.1640625 MB free)
  Uptime: 1153.23 sec
  Load Avg:  1.64  1.6  1.23
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-12.0.1 (ORCJIT, broadwell)
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
    Model name:                      Intel(R) Xeon(R) CPU E5-2673 v4 @ 2.30GHz
    CPU family:                      6
    Model:                           79
    Thread(s) per core:              1
    Core(s) per socket:              2
    Socket(s):                       1
    Stepping:                        1
    BogoMIPS:                        4589.36
    Flags:                           fpu vme de pse tsc msr pae mce cx8 apic sep mtrr pge mca cmov pat pse36 clflush mmx fxsr sse sse2 ss ht syscall nx pdpe1gb rdtscp lm constant_tsc rep_good nopl xtopology cpuid pni pclmulqdq ssse3 fma cx16 pcid sse4_1 sse4_2 movbe popcnt aes xsave avx f16c rdrand hypervisor lahf_lm abm 3dnowprefetch invpcid_single pti fsgsbase bmi1 hle avx2 smep bmi2 erms invpcid rtm rdseed adx smap xsaveopt md_clear
    Hypervisor vendor:               Microsoft
    Virtualization type:             full
    L1d cache:                       64 KiB (2 instances)
    L1i cache:                       64 KiB (2 instances)
    L2 cache:                        512 KiB (2 instances)
    L3 cache:                        50 MiB (1 instance)
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
    Vulnerability Tsx async abort:   Mitigation; Clear CPU buffers; SMT Host state unknown
    

| Cpu Property       | Value                                                   |
|:------------------ |:------------------------------------------------------- |
| Brand              | Intel(R) Xeon(R) CPU E5-2673 v4 @ 2.30GHz               |
| Vendor             | :Intel                                                  |
| Architecture       | :Broadwell                                              |
| Model              | Family: 0x06, Model: 0x4f, Stepping: 0x01, Type: 0x00   |
| Cores              | 2 physical cores, 2 logical cores (on executing CPU)    |
|                    | No Hyperthreading hardware capability detected          |
| Clock Frequencies  | Not supported by CPU                                    |
| Data Cache         | Level 1:3 : (32, 256, 51200) kbytes                     |
|                    | 64 byte cache line size                                 |
| Address Size       | 48 bits virtual, 46 bits physical                       |
| SIMD               | 256 bit = 32 byte max. SIMD vector size                 |
| Time Stamp Counter | TSC is accessible via `rdtsc`                           |
|                    | TSC increased at every clock cycle (non-invariant TSC)  |
| Perf. Monitoring   | Performance Monitoring Counters (PMC) are not supported |
| Hypervisor         | Yes, Microsoft                                          |

