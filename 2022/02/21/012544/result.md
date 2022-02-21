# Multi-thread benchmark result

* Pull request commit: [`1176c155147bfdaaed3c4792fb0518f763e2e6f7`](https://github.com/JuliaFolds/Transducers.jl/commit/1176c155147bfdaaed3c4792fb0518f763e2e6f7)
* Pull request: <https://github.com/JuliaFolds/Transducers.jl/pull/243> (Update */Manifest.toml)

# Judge result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmarks:
    - Target: 21 Feb 2022 - 01:20
    - Baseline: 21 Feb 2022 - 01:25
* Package commits:
    - Target: 00c224
    - Baseline: 39038b
* Julia commits:
    - Target: bf5349
    - Baseline: bf5349
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
| `["collect", "unordered", "basesize=1024"]`         |                   1.00 (5%)  |                1.03 (1%) :x: |
| `["findfirst", "n=1000", "reduce", "basesize=256"]` | 0.87 (5%) :white_check_mark: | 0.93 (1%) :white_check_mark: |
| `["findfirst", "n=1000", "reduce", "basesize=512"]` |                1.31 (5%) :x: |                1.33 (1%) :x: |
| `["findfirst", "n=400", "reduce", "basesize=512"]`  |                   1.03 (5%)  | 0.94 (1%) :white_check_mark: |
| `["findfirst", "n=500", "reduce", "basesize=128"]`  | 0.90 (5%) :white_check_mark: | 0.95 (1%) :white_check_mark: |
| `["findfirst", "n=500", "reduce", "basesize=256"]`  | 0.39 (5%) :white_check_mark: | 0.49 (1%) :white_check_mark: |
| `["findfirst", "n=500", "reduce", "basesize=512"]`  | 0.82 (5%) :white_check_mark: | 0.91 (1%) :white_check_mark: |
| `["overhead", "default"]`                           |                1.10 (5%) :x: |                   1.00 (1%)  |
| `["parallel_histogram", "assoc", "basesize=16384"]` |                1.05 (5%) :x: |                   1.00 (1%)  |
| `["parallel_histogram", "assoc", "basesize=4096"]`  | 0.94 (5%) :white_check_mark: | 0.87 (1%) :white_check_mark: |
| `["parallel_histogram", "assoc", "basesize=8192"]`  | 0.81 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["parallel_histogram", "comm", "basesize=4096"]`   |                   0.96 (5%)  | 0.94 (1%) :white_check_mark: |
| `["parallel_histogram", "comm", "basesize=8192"]`   |                   0.99 (5%)  |                1.33 (1%) :x: |
| `["partition_length_maximum", "rand", "reduce"]`    | 0.88 (5%) :white_check_mark: |                1.05 (1%) :x: |
| `["sum", "random", "reduce", "basesize=128"]`       | 0.94 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["sum", "uniform", "foldl"]`                       | 0.90 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["sum", "valley", "reduce", "basesize=128"]`       | 0.94 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["sum", "valley", "reduce", "basesize=256"]`       | 0.95 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["sum", "valley", "reduce", "basesize=512"]`       |                1.06 (5%) :x: |                   1.00 (1%)  |
| `["words", "nthreads=2"]`                           | 0.88 (5%) :white_check_mark: |                   1.00 (1%)  |

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
Julia Version 1.7.2
Commit bf53498635 (2022-02-06 15:21 UTC)
Platform Info:
  OS: Linux (x86_64-pc-linux-gnu)
      Ubuntu 20.04.3 LTS
  uname: Linux 5.11.0-1028-azure #31~20.04.2-Ubuntu SMP Tue Jan 18 08:46:15 UTC 2022 x86_64 x86_64
  CPU: Intel(R) Xeon(R) Platinum 8171M CPU @ 2.60GHz: 
              speed         user         nice          sys         idle          irq
       #1  2095 MHz       5140 s          1 s        224 s       4030 s          0 s
       #2  2095 MHz       5592 s          1 s        245 s       3600 s          0 s
       
  Memory: 6.7845458984375 GB (3539.95703125 MB free)
  Uptime: 948.13 sec
  Load Avg:  1.75  1.54  0.94
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-12.0.1 (ORCJIT, skylake-avx512)
```

### Baseline
```
Julia Version 1.7.2
Commit bf53498635 (2022-02-06 15:21 UTC)
Platform Info:
  OS: Linux (x86_64-pc-linux-gnu)
      Ubuntu 20.04.3 LTS
  uname: Linux 5.11.0-1028-azure #31~20.04.2-Ubuntu SMP Tue Jan 18 08:46:15 UTC 2022 x86_64 x86_64
  CPU: Intel(R) Xeon(R) Platinum 8171M CPU @ 2.60GHz: 
              speed         user         nice          sys         idle          irq
       #1  2095 MHz       7830 s          1 s        296 s       4422 s          0 s
       #2  2095 MHz       7727 s          1 s        315 s       4548 s          0 s
       
  Memory: 6.7845458984375 GB (3508.015625 MB free)
  Uptime: 1264.13 sec
  Load Avg:  1.63  1.57  1.13
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-12.0.1 (ORCJIT, skylake-avx512)
```

---
# Target result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmark: 21 Feb 2022 - 1:20
* Package commit: 00c224
* Julia commit: bf5349
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
| `["collect", "assoc", "basesize=1"]`                | 284.155 ms (5%) |         |  25.97 MiB (1%) |      306789 |
| `["collect", "assoc", "basesize=1024"]`             | 230.356 ms (5%) |         |   2.61 MiB (1%) |         456 |
| `["collect", "assoc", "basesize=32"]`               | 227.629 ms (5%) |         |   4.82 MiB (1%) |       11717 |
| `["collect", "seq"]`                                | 451.335 ms (5%) |         | 812.73 KiB (1%) |          11 |
| `["collect", "unordered", "basesize=1"]`            | 393.840 ms (5%) |         |  23.88 MiB (1%) |      412383 |
| `["collect", "unordered", "basesize=1024"]`         | 248.510 ms (5%) |         |   1.01 MiB (1%) |        1093 |
| `["collect", "unordered", "basesize=32"]`           | 259.654 ms (5%) |         |   1.59 MiB (1%) |       15062 |
| `["findfirst", "n=1000", "foldl"]`                  | 707.719 ms (5%) |         |                 |             |
| `["findfirst", "n=1000", "reduce", "basesize=128"]` | 399.532 ms (5%) |         | 232.89 KiB (1%) |        3277 |
| `["findfirst", "n=1000", "reduce", "basesize=256"]` | 489.968 ms (5%) |         | 157.20 KiB (1%) |        2193 |
| `["findfirst", "n=1000", "reduce", "basesize=512"]` | 665.564 ms (5%) |         | 108.55 KiB (1%) |        1509 |
| `["findfirst", "n=400", "foldl"]`                   | 550.667 ms (5%) |         |                 |             |
| `["findfirst", "n=400", "reduce", "basesize=128"]`  | 286.995 ms (5%) |         | 377.56 KiB (1%) |        5381 |
| `["findfirst", "n=400", "reduce", "basesize=256"]`  | 293.484 ms (5%) |         | 200.86 KiB (1%) |        2873 |
| `["findfirst", "n=400", "reduce", "basesize=512"]`  | 426.186 ms (5%) |         | 147.17 KiB (1%) |        2117 |
| `["findfirst", "n=500", "foldl"]`                   |  90.368 ms (5%) |         |                 |             |
| `["findfirst", "n=500", "reduce", "basesize=128"]`  | 158.687 ms (5%) |         | 199.20 KiB (1%) |        2732 |
| `["findfirst", "n=500", "reduce", "basesize=256"]`  |  86.901 ms (5%) |         |  71.38 KiB (1%) |         970 |
| `["findfirst", "n=500", "reduce", "basesize=512"]`  |  98.040 ms (5%) |         |  49.62 KiB (1%) |         672 |
| `["overhead", "default"]`                           |  79.205 μs (5%) |         |  32.73 KiB (1%) |         418 |
| `["overhead", "stoppable=false"]`                   |  86.106 μs (5%) |         |  32.72 KiB (1%) |         417 |
| `["overhead", "stoppable=true"]`                    |  91.906 μs (5%) |         |  44.25 KiB (1%) |         610 |
| `["parallel_histogram", "assoc", "basesize=16384"]` |   3.242 ms (5%) |         | 728.91 KiB (1%) |          57 |
| `["parallel_histogram", "assoc", "basesize=4096"]`  |   3.868 ms (5%) |         |   1.79 MiB (1%) |         216 |
| `["parallel_histogram", "assoc", "basesize=8192"]`  |   3.164 ms (5%) |         |   1.42 MiB (1%) |         117 |
| `["parallel_histogram", "comm", "basesize=16384"]`  |  19.531 ms (5%) |         |   1.59 MiB (1%) |        2769 |
| `["parallel_histogram", "comm", "basesize=4096"]`   |  26.673 ms (5%) |         |   1.18 MiB (1%) |        4949 |
| `["parallel_histogram", "comm", "basesize=8192"]`   |  24.582 ms (5%) |         |   1.67 MiB (1%) |        5512 |
| `["parallel_histogram", "seq"]`                     |   5.144 ms (5%) |         | 364.16 KiB (1%) |          24 |
| `["partition_length_maximum", "rand", "foldl"]`     |  38.372 ms (5%) |         |                 |             |
| `["partition_length_maximum", "rand", "reduce"]`    |  17.151 ms (5%) |         |  736 bytes (1%) |          11 |
| `["splitby", "count", "foldl"]`                     |   1.968 ms (5%) |         |                 |             |
| `["splitby", "count", "man"]`                       |   1.461 ms (5%) |         |                 |             |
| `["splitby", "count", "reduce"]`                    | 957.260 μs (5%) |         |   1.06 KiB (1%) |          18 |
| `["sum", "random", "foldl"]`                        |  15.631 ms (5%) |         |                 |             |
| `["sum", "random", "reduce", "basesize=128"]`       |   8.294 ms (5%) |         |  74.17 KiB (1%) |        1104 |
| `["sum", "random", "reduce", "basesize=256"]`       |   8.099 ms (5%) |         |  36.80 KiB (1%) |         548 |
| `["sum", "random", "reduce", "basesize=512"]`       |   8.189 ms (5%) |         |  18.08 KiB (1%) |         269 |
| `["sum", "uniform", "foldl"]`                       |  15.154 ms (5%) |         |                 |             |
| `["sum", "uniform", "reduce", "basesize=128"]`      |   8.523 ms (5%) |         |  74.08 KiB (1%) |        1101 |
| `["sum", "uniform", "reduce", "basesize=256"]`      |   7.756 ms (5%) |         |  36.70 KiB (1%) |         545 |
| `["sum", "uniform", "reduce", "basesize=512"]`      |   8.273 ms (5%) |         |  18.00 KiB (1%) |         267 |
| `["sum", "valley", "foldl"]`                        |  16.753 ms (5%) |         |                 |             |
| `["sum", "valley", "reduce", "basesize=128"]`       |   8.249 ms (5%) |         |  74.05 KiB (1%) |        1100 |
| `["sum", "valley", "reduce", "basesize=256"]`       |   8.347 ms (5%) |         |  36.73 KiB (1%) |         546 |
| `["sum", "valley", "reduce", "basesize=512"]`       |   8.380 ms (5%) |         |  18.06 KiB (1%) |         269 |
| `["words", "nthreads=1"]`                           |  23.582 ms (5%) |         |  31.75 MiB (1%) |     1034183 |
| `["words", "nthreads=2"]`                           |  14.887 ms (5%) |         |  32.46 MiB (1%) |     1034263 |
| `["words", "nthreads=4"]`                           |  17.240 ms (5%) |         |  33.09 MiB (1%) |     1034434 |

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
Julia Version 1.7.2
Commit bf53498635 (2022-02-06 15:21 UTC)
Platform Info:
  OS: Linux (x86_64-pc-linux-gnu)
      Ubuntu 20.04.3 LTS
  uname: Linux 5.11.0-1028-azure #31~20.04.2-Ubuntu SMP Tue Jan 18 08:46:15 UTC 2022 x86_64 x86_64
  CPU: Intel(R) Xeon(R) Platinum 8171M CPU @ 2.60GHz: 
              speed         user         nice          sys         idle          irq
       #1  2095 MHz       5140 s          1 s        224 s       4030 s          0 s
       #2  2095 MHz       5592 s          1 s        245 s       3600 s          0 s
       
  Memory: 6.7845458984375 GB (3539.95703125 MB free)
  Uptime: 948.13 sec
  Load Avg:  1.75  1.54  0.94
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-12.0.1 (ORCJIT, skylake-avx512)
```

---
# Baseline result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmark: 21 Feb 2022 - 1:25
* Package commit: 39038b
* Julia commit: bf5349
* Julia command flags: None
* Environment variables: `JULIA_NUM_THREADS => 2`

## Results
Below is a table of this job's results, obtained by running the benchmarks.
The values listed in the `ID` column have the structure `[parent_group, child_group, ..., key]`, and can be used to
index into the BaseBenchmarks suite to retrieve the corresponding benchmarks.
The percentages accompanying time and memory values in the below table are noise tolerances. The "true"
time/memory value for a given benchmark is expected to fall within this percentage of the reported value.
An empty cell means that the value was zero.

| ID                                                  | time            | GC time | memory           | allocations |
|-----------------------------------------------------|----------------:|--------:|-----------------:|------------:|
| `["collect", "assoc", "basesize=1"]`                | 278.098 ms (5%) |         |   25.97 MiB (1%) |      306842 |
| `["collect", "assoc", "basesize=1024"]`             | 231.315 ms (5%) |         |    2.61 MiB (1%) |         456 |
| `["collect", "assoc", "basesize=32"]`               | 233.170 ms (5%) |         |    4.82 MiB (1%) |       11705 |
| `["collect", "seq"]`                                | 454.476 ms (5%) |         |  812.73 KiB (1%) |          11 |
| `["collect", "unordered", "basesize=1"]`            | 397.162 ms (5%) |         |   23.89 MiB (1%) |      412689 |
| `["collect", "unordered", "basesize=1024"]`         | 247.920 ms (5%) |         | 1002.77 KiB (1%) |        1012 |
| `["collect", "unordered", "basesize=32"]`           | 257.490 ms (5%) |         |    1.58 MiB (1%) |       14672 |
| `["findfirst", "n=1000", "foldl"]`                  | 730.271 ms (5%) |         |                  |             |
| `["findfirst", "n=1000", "reduce", "basesize=128"]` | 399.150 ms (5%) |         |  232.86 KiB (1%) |        3276 |
| `["findfirst", "n=1000", "reduce", "basesize=256"]` | 560.231 ms (5%) |         |  168.66 KiB (1%) |        2354 |
| `["findfirst", "n=1000", "reduce", "basesize=512"]` | 507.088 ms (5%) |         |   81.33 KiB (1%) |        1146 |
| `["findfirst", "n=400", "foldl"]`                   | 551.411 ms (5%) |         |                  |             |
| `["findfirst", "n=400", "reduce", "basesize=128"]`  | 285.084 ms (5%) |         |  380.28 KiB (1%) |        5426 |
| `["findfirst", "n=400", "reduce", "basesize=256"]`  | 295.733 ms (5%) |         |  201.23 KiB (1%) |        2889 |
| `["findfirst", "n=400", "reduce", "basesize=512"]`  | 413.017 ms (5%) |         |  156.36 KiB (1%) |        2240 |
| `["findfirst", "n=500", "foldl"]`                   |  93.871 ms (5%) |         |                  |             |
| `["findfirst", "n=500", "reduce", "basesize=128"]`  | 176.749 ms (5%) |         |  209.91 KiB (1%) |        2883 |
| `["findfirst", "n=500", "reduce", "basesize=256"]`  | 220.637 ms (5%) |         |  145.08 KiB (1%) |        2022 |
| `["findfirst", "n=500", "reduce", "basesize=512"]`  | 118.886 ms (5%) |         |   54.45 KiB (1%) |         747 |
| `["overhead", "default"]`                           |  72.205 μs (5%) |         |   32.77 KiB (1%) |         419 |
| `["overhead", "stoppable=false"]`                   |  84.505 μs (5%) |         |   32.72 KiB (1%) |         417 |
| `["overhead", "stoppable=true"]`                    |  93.706 μs (5%) |         |   44.25 KiB (1%) |         610 |
| `["parallel_histogram", "assoc", "basesize=16384"]` |   3.086 ms (5%) |         |  728.91 KiB (1%) |          57 |
| `["parallel_histogram", "assoc", "basesize=4096"]`  |   4.131 ms (5%) |         |    2.05 MiB (1%) |         221 |
| `["parallel_histogram", "assoc", "basesize=8192"]`  |   3.888 ms (5%) |         |    1.42 MiB (1%) |         117 |
| `["parallel_histogram", "comm", "basesize=16384"]`  |  19.097 ms (5%) |         |    1.58 MiB (1%) |        2591 |
| `["parallel_histogram", "comm", "basesize=4096"]`   |  27.691 ms (5%) |         |    1.26 MiB (1%) |        7428 |
| `["parallel_histogram", "comm", "basesize=8192"]`   |  24.737 ms (5%) |         |    1.26 MiB (1%) |        5520 |
| `["parallel_histogram", "seq"]`                     |   5.176 ms (5%) |         |  364.16 KiB (1%) |          24 |
| `["partition_length_maximum", "rand", "foldl"]`     |  38.304 ms (5%) |         |                  |             |
| `["partition_length_maximum", "rand", "reduce"]`    |  19.397 ms (5%) |         |   704 bytes (1%) |          10 |
| `["splitby", "count", "foldl"]`                     |   1.921 ms (5%) |         |                  |             |
| `["splitby", "count", "man"]`                       |   1.463 ms (5%) |         |                  |             |
| `["splitby", "count", "reduce"]`                    | 915.158 μs (5%) |         |    1.06 KiB (1%) |          18 |
| `["sum", "random", "foldl"]`                        |  16.426 ms (5%) |         |                  |             |
| `["sum", "random", "reduce", "basesize=128"]`       |   8.817 ms (5%) |         |   74.17 KiB (1%) |        1104 |
| `["sum", "random", "reduce", "basesize=256"]`       |   8.061 ms (5%) |         |   36.73 KiB (1%) |         546 |
| `["sum", "random", "reduce", "basesize=512"]`       |   8.355 ms (5%) |         |   18.11 KiB (1%) |         270 |
| `["sum", "uniform", "foldl"]`                       |  16.814 ms (5%) |         |                  |             |
| `["sum", "uniform", "reduce", "basesize=128"]`      |   8.198 ms (5%) |         |   74.17 KiB (1%) |        1104 |
| `["sum", "uniform", "reduce", "basesize=256"]`      |   8.033 ms (5%) |         |   36.80 KiB (1%) |         548 |
| `["sum", "uniform", "reduce", "basesize=512"]`      |   7.955 ms (5%) |         |   18.03 KiB (1%) |         268 |
| `["sum", "valley", "foldl"]`                        |  16.570 ms (5%) |         |                  |             |
| `["sum", "valley", "reduce", "basesize=128"]`       |   8.763 ms (5%) |         |   74.11 KiB (1%) |        1102 |
| `["sum", "valley", "reduce", "basesize=256"]`       |   8.810 ms (5%) |         |   36.73 KiB (1%) |         546 |
| `["sum", "valley", "reduce", "basesize=512"]`       |   7.933 ms (5%) |         |   18.09 KiB (1%) |         270 |
| `["words", "nthreads=1"]`                           |  23.735 ms (5%) |         |   31.60 MiB (1%) |     1029637 |
| `["words", "nthreads=2"]`                           |  16.903 ms (5%) |         |   32.31 MiB (1%) |     1029711 |
| `["words", "nthreads=4"]`                           |  16.666 ms (5%) |         |   32.94 MiB (1%) |     1029845 |

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
Julia Version 1.7.2
Commit bf53498635 (2022-02-06 15:21 UTC)
Platform Info:
  OS: Linux (x86_64-pc-linux-gnu)
      Ubuntu 20.04.3 LTS
  uname: Linux 5.11.0-1028-azure #31~20.04.2-Ubuntu SMP Tue Jan 18 08:46:15 UTC 2022 x86_64 x86_64
  CPU: Intel(R) Xeon(R) Platinum 8171M CPU @ 2.60GHz: 
              speed         user         nice          sys         idle          irq
       #1  2095 MHz       7830 s          1 s        296 s       4422 s          0 s
       #2  2095 MHz       7727 s          1 s        315 s       4548 s          0 s
       
  Memory: 6.7845458984375 GB (3508.015625 MB free)
  Uptime: 1264.13 sec
  Load Avg:  1.63  1.57  1.13
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-12.0.1 (ORCJIT, skylake-avx512)
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
    Byte Order:                      Little Endian
    Address sizes:                   46 bits physical, 48 bits virtual
    CPU(s):                          2
    On-line CPU(s) list:             0,1
    Thread(s) per core:              1
    Core(s) per socket:              2
    Socket(s):                       1
    NUMA node(s):                    1
    Vendor ID:                       GenuineIntel
    CPU family:                      6
    Model:                           85
    Model name:                      Intel(R) Xeon(R) Platinum 8171M CPU @ 2.60GHz
    Stepping:                        4
    CPU MHz:                         2095.195
    BogoMIPS:                        4190.39
    Hypervisor vendor:               Microsoft
    Virtualization type:             full
    L1d cache:                       64 KiB
    L1i cache:                       64 KiB
    L2 cache:                        2 MiB
    L3 cache:                        35.8 MiB
    NUMA node0 CPU(s):               0,1
    Vulnerability Itlb multihit:     KVM: Mitigation: VMX unsupported
    Vulnerability L1tf:              Mitigation; PTE Inversion
    Vulnerability Mds:               Mitigation; Clear CPU buffers; SMT Host state unknown
    Vulnerability Meltdown:          Mitigation; PTI
    Vulnerability Spec store bypass: Vulnerable
    Vulnerability Spectre v1:        Mitigation; usercopy/swapgs barriers and __user pointer sanitization
    Vulnerability Spectre v2:        Mitigation; Full generic retpoline, STIBP disabled, RSB filling
    Vulnerability Srbds:             Not affected
    Vulnerability Tsx async abort:   Mitigation; Clear CPU buffers; SMT Host state unknown
    Flags:                           fpu vme de pse tsc msr pae mce cx8 apic sep mtrr pge mca cmov pat pse36 clflush mmx fxsr sse sse2 ss ht syscall nx pdpe1gb rdtscp lm constant_tsc rep_good nopl xtopology cpuid pni pclmulqdq ssse3 fma cx16 pcid sse4_1 sse4_2 movbe popcnt aes xsave avx f16c rdrand hypervisor lahf_lm abm 3dnowprefetch invpcid_single pti fsgsbase bmi1 hle avx2 smep bmi2 erms invpcid rtm mpx avx512f avx512dq rdseed adx smap clflushopt avx512cd avx512bw avx512vl xsaveopt xsavec xsaves md_clear
    

| Cpu Property       | Value                                                   |
|:------------------ |:------------------------------------------------------- |
| Brand              | Intel(R) Xeon(R) Platinum 8171M CPU @ 2.60GHz           |
| Vendor             | :Intel                                                  |
| Architecture       | :Skylake                                                |
| Model              | Family: 0x06, Model: 0x55, Stepping: 0x04, Type: 0x00   |
| Cores              | 2 physical cores, 2 logical cores (on executing CPU)    |
|                    | No Hyperthreading hardware capability detected          |
| Clock Frequencies  | Not supported by CPU                                    |
| Data Cache         | Level 1:3 : (32, 1024, 36608) kbytes                    |
|                    | 64 byte cache line size                                 |
| Address Size       | 48 bits virtual, 46 bits physical                       |
| SIMD               | 512 bit = 64 byte max. SIMD vector size                 |
| Time Stamp Counter | TSC is accessible via `rdtsc`                           |
|                    | TSC increased at every clock cycle (non-invariant TSC)  |
| Perf. Monitoring   | Performance Monitoring Counters (PMC) are not supported |
| Hypervisor         | Yes, Microsoft                                          |

