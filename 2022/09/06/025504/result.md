# Multi-thread benchmark result

* Pull request commit: [`9119118103d89df226028e6caaef2c74e48183b2`](https://github.com/JuliaFolds/Transducers.jl/commit/9119118103d89df226028e6caaef2c74e48183b2)
* Pull request: <https://github.com/JuliaFolds/Transducers.jl/pull/243> (Update */Manifest.toml)

# Judge result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmarks:
    - Target: 6 Sep 2022 - 02:48
    - Baseline: 6 Sep 2022 - 02:54
* Package commits:
    - Target: f4283f
    - Baseline: 6125fe
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
| `["collect", "unordered", "basesize=1"]`            |                   0.98 (5%)  | 0.99 (1%) :white_check_mark: |
| `["findfirst", "n=1000", "reduce", "basesize=128"]` | 0.68 (5%) :white_check_mark: | 0.67 (1%) :white_check_mark: |
| `["findfirst", "n=1000", "reduce", "basesize=512"]` |                1.58 (5%) :x: |                1.45 (1%) :x: |
| `["findfirst", "n=400", "reduce", "basesize=128"]`  |                   0.98 (5%)  |                1.03 (1%) :x: |
| `["findfirst", "n=400", "reduce", "basesize=512"]`  |                1.05 (5%) :x: |                1.03 (1%) :x: |
| `["findfirst", "n=500", "reduce", "basesize=128"]`  |                   0.96 (5%)  |                1.03 (1%) :x: |
| `["findfirst", "n=500", "reduce", "basesize=256"]`  | 0.30 (5%) :white_check_mark: | 0.39 (1%) :white_check_mark: |
| `["findfirst", "n=500", "reduce", "basesize=512"]`  |                1.47 (5%) :x: |                1.26 (1%) :x: |
| `["parallel_histogram", "assoc", "basesize=4096"]`  |                   0.99 (5%)  | 0.87 (1%) :white_check_mark: |
| `["parallel_histogram", "assoc", "basesize=8192"]`  | 0.92 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["parallel_histogram", "comm", "basesize=8192"]`   |                1.12 (5%) :x: |                1.05 (1%) :x: |
| `["splitby", "count", "reduce"]`                    |                1.06 (5%) :x: |                   1.00 (1%)  |
| `["words", "nthreads=4"]`                           |                   0.96 (5%)  | 0.99 (1%) :white_check_mark: |

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
      Ubuntu 20.04.4 LTS
  uname: Linux 5.15.0-1017-azure #20~20.04.1-Ubuntu SMP Fri Aug 5 12:16:53 UTC 2022 x86_64 x86_64
  CPU: Intel(R) Xeon(R) CPU E5-2673 v3 @ 2.40GHz: 
              speed         user         nice          sys         idle          irq
       #1  2397 MHz       4903 s          2 s        286 s       2290 s          0 s
       #2  2397 MHz       5645 s          0 s        294 s       1551 s          0 s
       
  Memory: 6.781242370605469 GB (3714.37109375 MB free)
  Uptime: 757.12 sec
  Load Avg:  1.68  1.52  0.94
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-12.0.1 (ORCJIT, haswell)
```

### Baseline
```
Julia Version 1.7.3
Commit 742b9abb4d (2022-05-06 12:58 UTC)
Platform Info:
  OS: Linux (x86_64-pc-linux-gnu)
      Ubuntu 20.04.4 LTS
  uname: Linux 5.15.0-1017-azure #20~20.04.1-Ubuntu SMP Fri Aug 5 12:16:53 UTC 2022 x86_64 x86_64
  CPU: Intel(R) Xeon(R) CPU E5-2673 v3 @ 2.40GHz: 
              speed         user         nice          sys         idle          irq
       #1  2397 MHz       7698 s          2 s        351 s       2722 s          0 s
       #2  2397 MHz       7803 s          0 s        370 s       2608 s          0 s
       
  Memory: 6.781242370605469 GB (3662.81640625 MB free)
  Uptime: 1086.93 sec
  Load Avg:  1.6  1.56  1.13
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-12.0.1 (ORCJIT, haswell)
```

---
# Target result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmark: 6 Sep 2022 - 2:48
* Package commit: f4283f
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
| `["collect", "assoc", "basesize=1"]`                | 304.981 ms (5%) |         |  25.97 MiB (1%) |      306788 |
| `["collect", "assoc", "basesize=1024"]`             | 252.396 ms (5%) |         |   2.61 MiB (1%) |         456 |
| `["collect", "assoc", "basesize=32"]`               | 252.107 ms (5%) |         |   4.82 MiB (1%) |       11708 |
| `["collect", "seq"]`                                | 502.661 ms (5%) |         | 812.73 KiB (1%) |          11 |
| `["collect", "unordered", "basesize=1"]`            | 423.319 ms (5%) |         |  23.60 MiB (1%) |      403113 |
| `["collect", "unordered", "basesize=1024"]`         | 273.400 ms (5%) |         |   1.02 MiB (1%) |        1257 |
| `["collect", "unordered", "basesize=32"]`           | 288.305 ms (5%) |         |   1.59 MiB (1%) |       15095 |
| `["findfirst", "n=1000", "foldl"]`                  | 721.438 ms (5%) |         |                 |             |
| `["findfirst", "n=1000", "reduce", "basesize=128"]` | 405.441 ms (5%) |         | 232.67 KiB (1%) |        3270 |
| `["findfirst", "n=1000", "reduce", "basesize=256"]` | 490.604 ms (5%) |         | 157.20 KiB (1%) |        2193 |
| `["findfirst", "n=1000", "reduce", "basesize=512"]` |    1.060 s (5%) |         | 157.81 KiB (1%) |        2219 |
| `["findfirst", "n=400", "foldl"]`                   | 528.234 ms (5%) |         |                 |             |
| `["findfirst", "n=400", "reduce", "basesize=128"]`  | 312.037 ms (5%) |         | 428.83 KiB (1%) |        6082 |
| `["findfirst", "n=400", "reduce", "basesize=256"]`  | 285.238 ms (5%) |         | 200.16 KiB (1%) |        2865 |
| `["findfirst", "n=400", "reduce", "basesize=512"]`  | 395.290 ms (5%) |         | 141.03 KiB (1%) |        2014 |
| `["findfirst", "n=500", "foldl"]`                   |  92.038 ms (5%) |         |                 |             |
| `["findfirst", "n=500", "reduce", "basesize=128"]`  | 170.411 ms (5%) |         | 213.28 KiB (1%) |        2932 |
| `["findfirst", "n=500", "reduce", "basesize=256"]`  |  78.453 ms (5%) |         |  62.81 KiB (1%) |         860 |
| `["findfirst", "n=500", "reduce", "basesize=512"]`  | 141.402 ms (5%) |         |  63.70 KiB (1%) |         867 |
| `["overhead", "default"]`                           |  76.404 μs (5%) |         |  32.70 KiB (1%) |         417 |
| `["overhead", "stoppable=false"]`                   |  71.304 μs (5%) |         |  32.78 KiB (1%) |         419 |
| `["overhead", "stoppable=true"]`                    |  86.205 μs (5%) |         |  44.16 KiB (1%) |         607 |
| `["parallel_histogram", "assoc", "basesize=16384"]` |   3.544 ms (5%) |         | 728.91 KiB (1%) |          57 |
| `["parallel_histogram", "assoc", "basesize=4096"]`  |   4.529 ms (5%) |         |   1.79 MiB (1%) |         215 |
| `["parallel_histogram", "assoc", "basesize=8192"]`  |   3.837 ms (5%) |         |   1.42 MiB (1%) |         117 |
| `["parallel_histogram", "comm", "basesize=16384"]`  |  13.165 ms (5%) |         |   1.51 MiB (1%) |         226 |
| `["parallel_histogram", "comm", "basesize=4096"]`   |  16.600 ms (5%) |         |   1.03 MiB (1%) |        2306 |
| `["parallel_histogram", "comm", "basesize=8192"]`   |  18.830 ms (5%) |         |   1.15 MiB (1%) |        3665 |
| `["parallel_histogram", "seq"]`                     |   6.387 ms (5%) |         | 364.16 KiB (1%) |          24 |
| `["partition_length_maximum", "rand", "foldl"]`     |  62.412 ms (5%) |         |                 |             |
| `["partition_length_maximum", "rand", "reduce"]`    |  31.720 ms (5%) |         |  736 bytes (1%) |          11 |
| `["splitby", "count", "foldl"]`                     |   1.925 ms (5%) |         |                 |             |
| `["splitby", "count", "man"]`                       |   1.513 ms (5%) |         |                 |             |
| `["splitby", "count", "reduce"]`                    | 930.746 μs (5%) |         |   1.06 KiB (1%) |          18 |
| `["sum", "random", "foldl"]`                        |  17.895 ms (5%) |         |                 |             |
| `["sum", "random", "reduce", "basesize=128"]`       |   9.405 ms (5%) |         |  74.23 KiB (1%) |        1106 |
| `["sum", "random", "reduce", "basesize=256"]`       |   9.317 ms (5%) |         |  36.64 KiB (1%) |         543 |
| `["sum", "random", "reduce", "basesize=512"]`       |   9.004 ms (5%) |         |  18.05 KiB (1%) |         268 |
| `["sum", "uniform", "foldl"]`                       |  17.490 ms (5%) |         |                 |             |
| `["sum", "uniform", "reduce", "basesize=128"]`      |   9.000 ms (5%) |         |  74.14 KiB (1%) |        1103 |
| `["sum", "uniform", "reduce", "basesize=256"]`      |   8.868 ms (5%) |         |  36.67 KiB (1%) |         544 |
| `["sum", "uniform", "reduce", "basesize=512"]`      |   9.057 ms (5%) |         |  18.03 KiB (1%) |         268 |
| `["sum", "valley", "foldl"]`                        |  17.842 ms (5%) |         |                 |             |
| `["sum", "valley", "reduce", "basesize=128"]`       |   9.430 ms (5%) |         |  74.11 KiB (1%) |        1102 |
| `["sum", "valley", "reduce", "basesize=256"]`       |   9.260 ms (5%) |         |  36.70 KiB (1%) |         545 |
| `["sum", "valley", "reduce", "basesize=512"]`       |   9.141 ms (5%) |         |  18.03 KiB (1%) |         268 |
| `["words", "nthreads=1"]`                           |  27.528 ms (5%) |         |  31.45 MiB (1%) |     1024477 |
| `["words", "nthreads=2"]`                           |  17.002 ms (5%) |         |  32.16 MiB (1%) |     1024574 |
| `["words", "nthreads=4"]`                           |  17.430 ms (5%) |         |  32.61 MiB (1%) |     1024640 |

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
      Ubuntu 20.04.4 LTS
  uname: Linux 5.15.0-1017-azure #20~20.04.1-Ubuntu SMP Fri Aug 5 12:16:53 UTC 2022 x86_64 x86_64
  CPU: Intel(R) Xeon(R) CPU E5-2673 v3 @ 2.40GHz: 
              speed         user         nice          sys         idle          irq
       #1  2397 MHz       4903 s          2 s        286 s       2290 s          0 s
       #2  2397 MHz       5645 s          0 s        294 s       1551 s          0 s
       
  Memory: 6.781242370605469 GB (3714.37109375 MB free)
  Uptime: 757.12 sec
  Load Avg:  1.68  1.52  0.94
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-12.0.1 (ORCJIT, haswell)
```

---
# Baseline result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmark: 6 Sep 2022 - 2:54
* Package commit: 6125fe
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
| `["collect", "assoc", "basesize=1"]`                | 311.957 ms (5%) |         |  25.97 MiB (1%) |      306858 |
| `["collect", "assoc", "basesize=1024"]`             | 255.534 ms (5%) |         |   2.61 MiB (1%) |         456 |
| `["collect", "assoc", "basesize=32"]`               | 253.311 ms (5%) |         |   4.82 MiB (1%) |       11700 |
| `["collect", "seq"]`                                | 484.840 ms (5%) |         | 812.73 KiB (1%) |          11 |
| `["collect", "unordered", "basesize=1"]`            | 432.344 ms (5%) |         |  23.90 MiB (1%) |      412896 |
| `["collect", "unordered", "basesize=1024"]`         | 268.416 ms (5%) |         |   1.01 MiB (1%) |        1237 |
| `["collect", "unordered", "basesize=32"]`           | 283.683 ms (5%) |         |   1.60 MiB (1%) |       15376 |
| `["findfirst", "n=1000", "foldl"]`                  | 721.553 ms (5%) |         |                 |             |
| `["findfirst", "n=1000", "reduce", "basesize=128"]` | 595.035 ms (5%) |         | 348.28 KiB (1%) |        4880 |
| `["findfirst", "n=1000", "reduce", "basesize=256"]` | 488.744 ms (5%) |         | 157.36 KiB (1%) |        2197 |
| `["findfirst", "n=1000", "reduce", "basesize=512"]` | 670.239 ms (5%) |         | 108.61 KiB (1%) |        1511 |
| `["findfirst", "n=400", "foldl"]`                   | 541.511 ms (5%) |         |                 |             |
| `["findfirst", "n=400", "reduce", "basesize=128"]`  | 318.588 ms (5%) |         | 417.05 KiB (1%) |        5936 |
| `["findfirst", "n=400", "reduce", "basesize=256"]`  | 295.127 ms (5%) |         | 198.56 KiB (1%) |        2845 |
| `["findfirst", "n=400", "reduce", "basesize=512"]`  | 374.977 ms (5%) |         | 137.45 KiB (1%) |        1953 |
| `["findfirst", "n=500", "foldl"]`                   |  92.867 ms (5%) |         |                 |             |
| `["findfirst", "n=500", "reduce", "basesize=128"]`  | 177.644 ms (5%) |         | 207.20 KiB (1%) |        2896 |
| `["findfirst", "n=500", "reduce", "basesize=256"]`  | 260.412 ms (5%) |         | 160.45 KiB (1%) |        2236 |
| `["findfirst", "n=500", "reduce", "basesize=512"]`  |  96.181 ms (5%) |         |  50.72 KiB (1%) |         677 |
| `["overhead", "default"]`                           |  77.704 μs (5%) |         |  32.67 KiB (1%) |         416 |
| `["overhead", "stoppable=false"]`                   |  72.004 μs (5%) |         |  32.78 KiB (1%) |         419 |
| `["overhead", "stoppable=true"]`                    |  85.205 μs (5%) |         |  44.28 KiB (1%) |         611 |
| `["parallel_histogram", "assoc", "basesize=16384"]` |   3.613 ms (5%) |         | 728.91 KiB (1%) |          57 |
| `["parallel_histogram", "assoc", "basesize=4096"]`  |   4.562 ms (5%) |         |   2.05 MiB (1%) |         222 |
| `["parallel_histogram", "assoc", "basesize=8192"]`  |   4.166 ms (5%) |         |   1.42 MiB (1%) |         117 |
| `["parallel_histogram", "comm", "basesize=16384"]`  |  12.859 ms (5%) |         |   1.51 MiB (1%) |         208 |
| `["parallel_histogram", "comm", "basesize=4096"]`   |  17.291 ms (5%) |         |   1.03 MiB (1%) |        2958 |
| `["parallel_histogram", "comm", "basesize=8192"]`   |  16.864 ms (5%) |         |   1.09 MiB (1%) |         612 |
| `["parallel_histogram", "seq"]`                     |   6.489 ms (5%) |         | 364.16 KiB (1%) |          24 |
| `["partition_length_maximum", "rand", "foldl"]`     |  62.843 ms (5%) |         |                 |             |
| `["partition_length_maximum", "rand", "reduce"]`    |  32.169 ms (5%) |         |  736 bytes (1%) |          11 |
| `["splitby", "count", "foldl"]`                     |   1.849 ms (5%) |         |                 |             |
| `["splitby", "count", "man"]`                       |   1.513 ms (5%) |         |                 |             |
| `["splitby", "count", "reduce"]`                    | 874.546 μs (5%) |         |   1.06 KiB (1%) |          18 |
| `["sum", "random", "foldl"]`                        |  17.905 ms (5%) |         |                 |             |
| `["sum", "random", "reduce", "basesize=128"]`       |   9.301 ms (5%) |         |  74.17 KiB (1%) |        1104 |
| `["sum", "random", "reduce", "basesize=256"]`       |   9.179 ms (5%) |         |  36.67 KiB (1%) |         544 |
| `["sum", "random", "reduce", "basesize=512"]`       |   9.055 ms (5%) |         |  18.08 KiB (1%) |         269 |
| `["sum", "uniform", "foldl"]`                       |  17.122 ms (5%) |         |                 |             |
| `["sum", "uniform", "reduce", "basesize=128"]`      |   9.339 ms (5%) |         |  74.17 KiB (1%) |        1104 |
| `["sum", "uniform", "reduce", "basesize=256"]`      |   9.131 ms (5%) |         |  36.73 KiB (1%) |         546 |
| `["sum", "uniform", "reduce", "basesize=512"]`      |   8.888 ms (5%) |         |  18.00 KiB (1%) |         267 |
| `["sum", "valley", "foldl"]`                        |  18.243 ms (5%) |         |                 |             |
| `["sum", "valley", "reduce", "basesize=128"]`       |   9.426 ms (5%) |         |  74.14 KiB (1%) |        1103 |
| `["sum", "valley", "reduce", "basesize=256"]`       |   9.254 ms (5%) |         |  36.73 KiB (1%) |         546 |
| `["sum", "valley", "reduce", "basesize=512"]`       |   9.476 ms (5%) |         |  18.00 KiB (1%) |         267 |
| `["words", "nthreads=1"]`                           |  28.542 ms (5%) |         |  31.62 MiB (1%) |     1030191 |
| `["words", "nthreads=2"]`                           |  17.473 ms (5%) |         |  32.33 MiB (1%) |     1030289 |
| `["words", "nthreads=4"]`                           |  18.093 ms (5%) |         |  32.96 MiB (1%) |     1030457 |

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
      Ubuntu 20.04.4 LTS
  uname: Linux 5.15.0-1017-azure #20~20.04.1-Ubuntu SMP Fri Aug 5 12:16:53 UTC 2022 x86_64 x86_64
  CPU: Intel(R) Xeon(R) CPU E5-2673 v3 @ 2.40GHz: 
              speed         user         nice          sys         idle          irq
       #1  2397 MHz       7698 s          2 s        351 s       2722 s          0 s
       #2  2397 MHz       7803 s          0 s        370 s       2608 s          0 s
       
  Memory: 6.781242370605469 GB (3662.81640625 MB free)
  Uptime: 1086.93 sec
  Load Avg:  1.6  1.56  1.13
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-12.0.1 (ORCJIT, haswell)
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
    Model:                           63
    Model name:                      Intel(R) Xeon(R) CPU E5-2673 v3 @ 2.40GHz
    Stepping:                        2
    CPU MHz:                         2397.222
    BogoMIPS:                        4794.44
    Hypervisor vendor:               Microsoft
    Virtualization type:             full
    L1d cache:                       64 KiB
    L1i cache:                       64 KiB
    L2 cache:                        512 KiB
    L3 cache:                        30 MiB
    NUMA node0 CPU(s):               0,1
    Vulnerability Itlb multihit:     KVM: Mitigation: VMX unsupported
    Vulnerability L1tf:              Mitigation; PTE Inversion
    Vulnerability Mds:               Mitigation; Clear CPU buffers; SMT Host state unknown
    Vulnerability Meltdown:          Mitigation; PTI
    Vulnerability Mmio stale data:   Vulnerable: Clear CPU buffers attempted, no microcode; SMT Host state unknown
    Vulnerability Retbleed:          Not affected
    Vulnerability Spec store bypass: Vulnerable
    Vulnerability Spectre v1:        Mitigation; usercopy/swapgs barriers and __user pointer sanitization
    Vulnerability Spectre v2:        Mitigation; Retpolines, STIBP disabled, RSB filling
    Vulnerability Srbds:             Not affected
    Vulnerability Tsx async abort:   Not affected
    Flags:                           fpu vme de pse tsc msr pae mce cx8 apic sep mtrr pge mca cmov pat pse36 clflush mmx fxsr sse sse2 ss ht syscall nx pdpe1gb rdtscp lm constant_tsc rep_good nopl xtopology cpuid pni pclmulqdq ssse3 fma cx16 pcid sse4_1 sse4_2 movbe popcnt aes xsave avx f16c rdrand hypervisor lahf_lm abm invpcid_single pti fsgsbase bmi1 avx2 smep bmi2 erms invpcid xsaveopt md_clear
    

| Cpu Property       | Value                                                   |
|:------------------ |:------------------------------------------------------- |
| Brand              | Intel(R) Xeon(R) CPU E5-2673 v3 @ 2.40GHz               |
| Vendor             | :Intel                                                  |
| Architecture       | :Haswell                                                |
| Model              | Family: 0x06, Model: 0x3f, Stepping: 0x02, Type: 0x00   |
| Cores              | 2 physical cores, 2 logical cores (on executing CPU)    |
|                    | No Hyperthreading hardware capability detected          |
| Clock Frequencies  | Not supported by CPU                                    |
| Data Cache         | Level 1:3 : (32, 256, 30720) kbytes                     |
|                    | 64 byte cache line size                                 |
| Address Size       | 48 bits virtual, 46 bits physical                       |
| SIMD               | 256 bit = 32 byte max. SIMD vector size                 |
| Time Stamp Counter | TSC is accessible via `rdtsc`                           |
|                    | TSC increased at every clock cycle (non-invariant TSC)  |
| Perf. Monitoring   | Performance Monitoring Counters (PMC) are not supported |
| Hypervisor         | Yes, Microsoft                                          |

