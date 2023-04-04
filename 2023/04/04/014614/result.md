# Multi-thread benchmark result

* Pull request commit: [`6ff2b57a0c4a2956b1e91830a39e9d388027910b`](https://github.com/JuliaFolds/Transducers.jl/commit/6ff2b57a0c4a2956b1e91830a39e9d388027910b)
* Pull request: <https://github.com/JuliaFolds/Transducers.jl/pull/243> (Update */Manifest.toml)

# Judge result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmarks:
    - Target: 4 Apr 2023 - 01:40
    - Baseline: 4 Apr 2023 - 01:45
* Package commits:
    - Target: cc6a88
    - Baseline: f8d0df
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
| `["collect", "unordered", "basesize=1"]`            | 0.95 (5%) :white_check_mark: |                   1.01 (1%)  |
| `["findfirst", "n=1000", "reduce", "basesize=256"]` |                1.20 (5%) :x: |                1.17 (1%) :x: |
| `["findfirst", "n=1000", "reduce", "basesize=512"]` |                2.28 (5%) :x: |                2.11 (1%) :x: |
| `["findfirst", "n=400", "reduce", "basesize=128"]`  |                   0.99 (5%)  |                1.04 (1%) :x: |
| `["findfirst", "n=400", "reduce", "basesize=512"]`  | 0.93 (5%) :white_check_mark: | 0.86 (1%) :white_check_mark: |
| `["findfirst", "n=500", "reduce", "basesize=128"]`  |                1.21 (5%) :x: |                1.07 (1%) :x: |
| `["findfirst", "n=500", "reduce", "basesize=256"]`  |                1.05 (5%) :x: |                1.14 (1%) :x: |
| `["findfirst", "n=500", "reduce", "basesize=512"]`  |                   0.97 (5%)  | 0.88 (1%) :white_check_mark: |
| `["overhead", "stoppable=false"]`                   |                1.05 (5%) :x: |                   1.00 (1%)  |
| `["parallel_histogram", "comm", "basesize=16384"]`  |                1.09 (5%) :x: |                   1.00 (1%)  |
| `["parallel_histogram", "comm", "basesize=4096"]`   |                   0.96 (5%)  |                1.01 (1%) :x: |
| `["parallel_histogram", "comm", "basesize=8192"]`   |                1.09 (5%) :x: |                1.35 (1%) :x: |
| `["words", "nthreads=2"]`                           | 0.94 (5%) :white_check_mark: |                   0.99 (1%)  |
| `["words", "nthreads=4"]`                           |                   0.97 (5%)  | 0.99 (1%) :white_check_mark: |

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
      Ubuntu 22.04.2 LTS
  uname: Linux 5.15.0-1034-azure #41-Ubuntu SMP Fri Feb 10 19:59:45 UTC 2023 x86_64 x86_64
  CPU: Intel(R) Xeon(R) Platinum 8171M CPU @ 2.60GHz: 
              speed         user         nice          sys         idle          irq
       #1  2095 MHz       6161 s          0 s        289 s       1056 s          0 s
       #2  2095 MHz       4689 s          0 s        302 s       2468 s          0 s
       
  Memory: 6.781219482421875 GB (3641.95703125 MB free)
  Uptime: 756.49 sec
  Load Avg:  1.63  1.5  0.94
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-12.0.1 (ORCJIT, skylake-avx512)
```

### Baseline
```
Julia Version 1.7.3
Commit 742b9abb4d (2022-05-06 12:58 UTC)
Platform Info:
  OS: Linux (x86_64-pc-linux-gnu)
      Ubuntu 22.04.2 LTS
  uname: Linux 5.15.0-1034-azure #41-Ubuntu SMP Fri Feb 10 19:59:45 UTC 2023 x86_64 x86_64
  CPU: Intel(R) Xeon(R) Platinum 8171M CPU @ 2.60GHz: 
              speed         user         nice          sys         idle          irq
       #1  2095 MHz       8660 s          0 s        379 s       1722 s          0 s
       #2  2095 MHz       7068 s          0 s        397 s       3248 s          0 s
       
  Memory: 6.781219482421875 GB (3510.96484375 MB free)
  Uptime: 1082.65 sec
  Load Avg:  1.52  1.55  1.13
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-12.0.1 (ORCJIT, skylake-avx512)
```

---
# Target result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmark: 4 Apr 2023 - 1:40
* Package commit: cc6a88
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
| `["collect", "assoc", "basesize=1"]`                | 299.663 ms (5%) |         |  25.97 MiB (1%) |      306807 |
| `["collect", "assoc", "basesize=1024"]`             | 243.504 ms (5%) |         |   2.61 MiB (1%) |         456 |
| `["collect", "assoc", "basesize=32"]`               | 241.317 ms (5%) |         |   4.82 MiB (1%) |       11714 |
| `["collect", "seq"]`                                | 462.414 ms (5%) |         | 812.73 KiB (1%) |          11 |
| `["collect", "unordered", "basesize=1"]`            | 412.717 ms (5%) |         |  23.87 MiB (1%) |      412165 |
| `["collect", "unordered", "basesize=1024"]`         | 252.603 ms (5%) |         |   1.01 MiB (1%) |         941 |
| `["collect", "unordered", "basesize=32"]`           | 267.028 ms (5%) |         |   1.58 MiB (1%) |       14565 |
| `["findfirst", "n=1000", "foldl"]`                  | 753.671 ms (5%) |         |                 |             |
| `["findfirst", "n=1000", "reduce", "basesize=128"]` | 422.645 ms (5%) |         | 230.58 KiB (1%) |        3248 |
| `["findfirst", "n=1000", "reduce", "basesize=256"]` | 623.873 ms (5%) |         | 170.42 KiB (1%) |        2390 |
| `["findfirst", "n=1000", "reduce", "basesize=512"]` |    1.189 s (5%) |         | 168.31 KiB (1%) |        2376 |
| `["findfirst", "n=400", "foldl"]`                   | 555.219 ms (5%) |         |                 |             |
| `["findfirst", "n=400", "reduce", "basesize=128"]`  | 300.112 ms (5%) |         | 388.53 KiB (1%) |        5524 |
| `["findfirst", "n=400", "reduce", "basesize=256"]`  | 298.769 ms (5%) |         | 200.86 KiB (1%) |        2873 |
| `["findfirst", "n=400", "reduce", "basesize=512"]`  | 346.103 ms (5%) |         | 112.62 KiB (1%) |        1623 |
| `["findfirst", "n=500", "foldl"]`                   |  96.918 ms (5%) |         |                 |             |
| `["findfirst", "n=500", "reduce", "basesize=128"]`  | 213.603 ms (5%) |         | 238.95 KiB (1%) |        3340 |
| `["findfirst", "n=500", "reduce", "basesize=256"]`  | 208.122 ms (5%) |         | 138.64 KiB (1%) |        1900 |
| `["findfirst", "n=500", "reduce", "basesize=512"]`  | 128.028 ms (5%) |         |  55.95 KiB (1%) |         765 |
| `["overhead", "default"]`                           |  80.104 μs (5%) |         |  32.73 KiB (1%) |         418 |
| `["overhead", "stoppable=false"]`                   |  86.004 μs (5%) |         |  32.72 KiB (1%) |         417 |
| `["overhead", "stoppable=true"]`                    |  98.405 μs (5%) |         |  44.25 KiB (1%) |         610 |
| `["parallel_histogram", "assoc", "basesize=16384"]` |   3.597 ms (5%) |         | 728.91 KiB (1%) |          57 |
| `["parallel_histogram", "assoc", "basesize=4096"]`  |   4.545 ms (5%) |         |   2.05 MiB (1%) |         221 |
| `["parallel_histogram", "assoc", "basesize=8192"]`  |   4.216 ms (5%) |         |   1.42 MiB (1%) |         117 |
| `["parallel_histogram", "comm", "basesize=16384"]`  |  20.766 ms (5%) |         |   1.57 MiB (1%) |        2232 |
| `["parallel_histogram", "comm", "basesize=4096"]`   |  25.447 ms (5%) |         |   1.22 MiB (1%) |        6028 |
| `["parallel_histogram", "comm", "basesize=8192"]`   |  25.249 ms (5%) |         |   1.62 MiB (1%) |        3705 |
| `["parallel_histogram", "seq"]`                     |   6.645 ms (5%) |         | 364.16 KiB (1%) |          24 |
| `["partition_length_maximum", "rand", "foldl"]`     |  40.892 ms (5%) |         |                 |             |
| `["partition_length_maximum", "rand", "reduce"]`    |  20.507 ms (5%) |         |  736 bytes (1%) |          11 |
| `["splitby", "count", "foldl"]`                     |   2.548 ms (5%) |         |                 |             |
| `["splitby", "count", "man"]`                       |   1.608 ms (5%) |         |                 |             |
| `["splitby", "count", "reduce"]`                    |   1.215 ms (5%) |         |   1.09 KiB (1%) |          19 |
| `["sum", "random", "foldl"]`                        |  18.598 ms (5%) |         |                 |             |
| `["sum", "random", "reduce", "basesize=128"]`       |   9.505 ms (5%) |         |  74.11 KiB (1%) |        1102 |
| `["sum", "random", "reduce", "basesize=256"]`       |   9.286 ms (5%) |         |  36.70 KiB (1%) |         545 |
| `["sum", "random", "reduce", "basesize=512"]`       |   9.220 ms (5%) |         |  18.08 KiB (1%) |         269 |
| `["sum", "uniform", "foldl"]`                       |  18.231 ms (5%) |         |                 |             |
| `["sum", "uniform", "reduce", "basesize=128"]`      |   9.206 ms (5%) |         |  74.14 KiB (1%) |        1103 |
| `["sum", "uniform", "reduce", "basesize=256"]`      |   9.182 ms (5%) |         |  36.73 KiB (1%) |         546 |
| `["sum", "uniform", "reduce", "basesize=512"]`      |   9.114 ms (5%) |         |  18.06 KiB (1%) |         269 |
| `["sum", "valley", "foldl"]`                        |  18.708 ms (5%) |         |                 |             |
| `["sum", "valley", "reduce", "basesize=128"]`       |   9.511 ms (5%) |         |  73.92 KiB (1%) |        1096 |
| `["sum", "valley", "reduce", "basesize=256"]`       |   9.514 ms (5%) |         |  36.73 KiB (1%) |         546 |
| `["sum", "valley", "reduce", "basesize=512"]`       |   9.448 ms (5%) |         |  18.00 KiB (1%) |         267 |
| `["words", "nthreads=1"]`                           |  27.882 ms (5%) |         |  31.66 MiB (1%) |     1031632 |
| `["words", "nthreads=2"]`                           |  17.093 ms (5%) |         |  32.01 MiB (1%) |     1031668 |
| `["words", "nthreads=4"]`                           |  17.342 ms (5%) |         |  32.73 MiB (1%) |     1031748 |

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
      Ubuntu 22.04.2 LTS
  uname: Linux 5.15.0-1034-azure #41-Ubuntu SMP Fri Feb 10 19:59:45 UTC 2023 x86_64 x86_64
  CPU: Intel(R) Xeon(R) Platinum 8171M CPU @ 2.60GHz: 
              speed         user         nice          sys         idle          irq
       #1  2095 MHz       6161 s          0 s        289 s       1056 s          0 s
       #2  2095 MHz       4689 s          0 s        302 s       2468 s          0 s
       
  Memory: 6.781219482421875 GB (3641.95703125 MB free)
  Uptime: 756.49 sec
  Load Avg:  1.63  1.5  0.94
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-12.0.1 (ORCJIT, skylake-avx512)
```

---
# Baseline result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmark: 4 Apr 2023 - 1:45
* Package commit: f8d0df
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
| `["collect", "assoc", "basesize=1"]`                | 295.781 ms (5%) |         |  25.97 MiB (1%) |      306827 |
| `["collect", "assoc", "basesize=1024"]`             | 244.503 ms (5%) |         |   2.61 MiB (1%) |         456 |
| `["collect", "assoc", "basesize=32"]`               | 242.291 ms (5%) |         |   4.82 MiB (1%) |       11705 |
| `["collect", "seq"]`                                | 472.897 ms (5%) |         | 812.73 KiB (1%) |          11 |
| `["collect", "unordered", "basesize=1"]`            | 435.682 ms (5%) |         |  23.66 MiB (1%) |      405058 |
| `["collect", "unordered", "basesize=1024"]`         | 259.477 ms (5%) |         |   1.00 MiB (1%) |         834 |
| `["collect", "unordered", "basesize=32"]`           | 270.631 ms (5%) |         |   1.57 MiB (1%) |       14419 |
| `["findfirst", "n=1000", "foldl"]`                  | 752.104 ms (5%) |         |                 |             |
| `["findfirst", "n=1000", "reduce", "basesize=128"]` | 419.359 ms (5%) |         | 230.52 KiB (1%) |        3246 |
| `["findfirst", "n=1000", "reduce", "basesize=256"]` | 518.959 ms (5%) |         | 145.88 KiB (1%) |        2053 |
| `["findfirst", "n=1000", "reduce", "basesize=512"]` | 522.550 ms (5%) |         |  79.75 KiB (1%) |        1124 |
| `["findfirst", "n=400", "foldl"]`                   | 557.823 ms (5%) |         |                 |             |
| `["findfirst", "n=400", "reduce", "basesize=128"]`  | 302.679 ms (5%) |         | 374.80 KiB (1%) |        5354 |
| `["findfirst", "n=400", "reduce", "basesize=256"]`  | 300.479 ms (5%) |         | 200.70 KiB (1%) |        2868 |
| `["findfirst", "n=400", "reduce", "basesize=512"]`  | 371.087 ms (5%) |         | 131.41 KiB (1%) |        1873 |
| `["findfirst", "n=500", "foldl"]`                   |  97.985 ms (5%) |         |                 |             |
| `["findfirst", "n=500", "reduce", "basesize=128"]`  | 176.769 ms (5%) |         | 223.64 KiB (1%) |        3076 |
| `["findfirst", "n=500", "reduce", "basesize=256"]`  | 197.862 ms (5%) |         | 121.66 KiB (1%) |        1688 |
| `["findfirst", "n=500", "reduce", "basesize=512"]`  | 131.398 ms (5%) |         |  63.67 KiB (1%) |         866 |
| `["overhead", "default"]`                           |  82.706 μs (5%) |         |  32.73 KiB (1%) |         418 |
| `["overhead", "stoppable=false"]`                   |  81.806 μs (5%) |         |  32.75 KiB (1%) |         418 |
| `["overhead", "stoppable=true"]`                    |  94.907 μs (5%) |         |  44.28 KiB (1%) |         611 |
| `["parallel_histogram", "assoc", "basesize=16384"]` |   3.626 ms (5%) |         | 728.91 KiB (1%) |          57 |
| `["parallel_histogram", "assoc", "basesize=4096"]`  |   4.652 ms (5%) |         |   2.05 MiB (1%) |         221 |
| `["parallel_histogram", "assoc", "basesize=8192"]`  |   4.048 ms (5%) |         |   1.42 MiB (1%) |         117 |
| `["parallel_histogram", "comm", "basesize=16384"]`  |  19.062 ms (5%) |         |   1.58 MiB (1%) |        2418 |
| `["parallel_histogram", "comm", "basesize=4096"]`   |  26.537 ms (5%) |         |   1.20 MiB (1%) |        5551 |
| `["parallel_histogram", "comm", "basesize=8192"]`   |  23.215 ms (5%) |         |   1.20 MiB (1%) |        5320 |
| `["parallel_histogram", "seq"]`                     |   6.607 ms (5%) |         | 364.16 KiB (1%) |          24 |
| `["partition_length_maximum", "rand", "foldl"]`     |  41.425 ms (5%) |         |                 |             |
| `["partition_length_maximum", "rand", "reduce"]`    |  20.524 ms (5%) |         |  736 bytes (1%) |          11 |
| `["splitby", "count", "foldl"]`                     |   2.448 ms (5%) |         |                 |             |
| `["splitby", "count", "man"]`                       |   1.577 ms (5%) |         |                 |             |
| `["splitby", "count", "reduce"]`                    |   1.222 ms (5%) |         |   1.09 KiB (1%) |          19 |
| `["sum", "random", "foldl"]`                        |  18.683 ms (5%) |         |                 |             |
| `["sum", "random", "reduce", "basesize=128"]`       |   9.549 ms (5%) |         |  74.11 KiB (1%) |        1102 |
| `["sum", "random", "reduce", "basesize=256"]`       |   9.295 ms (5%) |         |  36.73 KiB (1%) |         546 |
| `["sum", "random", "reduce", "basesize=512"]`       |   9.398 ms (5%) |         |  18.08 KiB (1%) |         269 |
| `["sum", "uniform", "foldl"]`                       |  18.183 ms (5%) |         |                 |             |
| `["sum", "uniform", "reduce", "basesize=128"]`      |   9.329 ms (5%) |         |  74.14 KiB (1%) |        1103 |
| `["sum", "uniform", "reduce", "basesize=256"]`      |   9.086 ms (5%) |         |  36.70 KiB (1%) |         545 |
| `["sum", "uniform", "reduce", "basesize=512"]`      |   9.047 ms (5%) |         |  18.06 KiB (1%) |         269 |
| `["sum", "valley", "foldl"]`                        |  18.513 ms (5%) |         |                 |             |
| `["sum", "valley", "reduce", "basesize=128"]`       |   9.597 ms (5%) |         |  73.98 KiB (1%) |        1098 |
| `["sum", "valley", "reduce", "basesize=256"]`       |   9.404 ms (5%) |         |  36.70 KiB (1%) |         545 |
| `["sum", "valley", "reduce", "basesize=512"]`       |   9.396 ms (5%) |         |  18.00 KiB (1%) |         267 |
| `["words", "nthreads=1"]`                           |  27.503 ms (5%) |         |  31.85 MiB (1%) |     1037848 |
| `["words", "nthreads=2"]`                           |  18.142 ms (5%) |         |  32.20 MiB (1%) |     1037884 |
| `["words", "nthreads=4"]`                           |  17.854 ms (5%) |         |  33.10 MiB (1%) |     1038029 |

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
      Ubuntu 22.04.2 LTS
  uname: Linux 5.15.0-1034-azure #41-Ubuntu SMP Fri Feb 10 19:59:45 UTC 2023 x86_64 x86_64
  CPU: Intel(R) Xeon(R) Platinum 8171M CPU @ 2.60GHz: 
              speed         user         nice          sys         idle          irq
       #1  2095 MHz       8660 s          0 s        379 s       1722 s          0 s
       #2  2095 MHz       7068 s          0 s        397 s       3248 s          0 s
       
  Memory: 6.781219482421875 GB (3510.96484375 MB free)
  Uptime: 1082.65 sec
  Load Avg:  1.52  1.55  1.13
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
    Address sizes:                   46 bits physical, 48 bits virtual
    Byte Order:                      Little Endian
    CPU(s):                          2
    On-line CPU(s) list:             0,1
    Vendor ID:                       GenuineIntel
    Model name:                      Intel(R) Xeon(R) Platinum 8171M CPU @ 2.60GHz
    CPU family:                      6
    Model:                           85
    Thread(s) per core:              1
    Core(s) per socket:              2
    Socket(s):                       1
    Stepping:                        4
    BogoMIPS:                        4190.35
    Flags:                           fpu vme de pse tsc msr pae mce cx8 apic sep mtrr pge mca cmov pat pse36 clflush mmx fxsr sse sse2 ss ht syscall nx pdpe1gb rdtscp lm constant_tsc rep_good nopl xtopology cpuid pni pclmulqdq ssse3 fma cx16 pcid sse4_1 sse4_2 movbe popcnt aes xsave avx f16c rdrand hypervisor lahf_lm abm 3dnowprefetch invpcid_single pti fsgsbase bmi1 hle avx2 smep bmi2 erms invpcid rtm avx512f avx512dq rdseed adx smap clflushopt avx512cd avx512bw avx512vl xsaveopt xsavec xsaves md_clear
    Hypervisor vendor:               Microsoft
    Virtualization type:             full
    L1d cache:                       64 KiB (2 instances)
    L1i cache:                       64 KiB (2 instances)
    L2 cache:                        2 MiB (2 instances)
    L3 cache:                        35.8 MiB (1 instance)
    NUMA node(s):                    1
    NUMA node0 CPU(s):               0,1
    Vulnerability Itlb multihit:     KVM: Mitigation: VMX unsupported
    Vulnerability L1tf:              Mitigation; PTE Inversion
    Vulnerability Mds:               Mitigation; Clear CPU buffers; SMT Host state unknown
    Vulnerability Meltdown:          Mitigation; PTI
    Vulnerability Mmio stale data:   Vulnerable: Clear CPU buffers attempted, no microcode; SMT Host state unknown
    Vulnerability Retbleed:          Vulnerable
    Vulnerability Spec store bypass: Vulnerable
    Vulnerability Spectre v1:        Mitigation; usercopy/swapgs barriers and __user pointer sanitization
    Vulnerability Spectre v2:        Mitigation; Retpolines, STIBP disabled, RSB filling, PBRSB-eIBRS Not affected
    Vulnerability Srbds:             Not affected
    Vulnerability Tsx async abort:   Mitigation; Clear CPU buffers; SMT Host state unknown
    

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

