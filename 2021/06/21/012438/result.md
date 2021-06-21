# Multi-thread benchmark result

* Pull request commit: [`66cf5d576242ea76b3a0e071f40c163e544d4b4a`](https://github.com/JuliaFolds/Transducers.jl/commit/66cf5d576242ea76b3a0e071f40c163e544d4b4a)
* Pull request: <https://github.com/JuliaFolds/Transducers.jl/pull/243> (Update */Manifest.toml)

# Judge result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmarks:
    - Target: 21 Jun 2021 - 01:18
    - Baseline: 21 Jun 2021 - 01:24
* Package commits:
    - Target: 337a6a
    - Baseline: 2cfb4c
* Julia commits:
    - Target: 69fcb5
    - Baseline: 69fcb5
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
| `["collect", "assoc", "basesize=1024"]`             | 0.92 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["collect", "unordered", "basesize=1024"]`         | 0.82 (5%) :white_check_mark: | 0.91 (1%) :white_check_mark: |
| `["collect", "unordered", "basesize=32"]`           | 0.91 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["findfirst", "n=1000", "reduce", "basesize=128"]` |                1.26 (5%) :x: |                1.36 (1%) :x: |
| `["findfirst", "n=1000", "reduce", "basesize=512"]` |                   0.98 (5%)  |                1.05 (1%) :x: |
| `["findfirst", "n=400", "reduce", "basesize=128"]`  |                   0.98 (5%)  | 0.94 (1%) :white_check_mark: |
| `["findfirst", "n=400", "reduce", "basesize=256"]`  |                1.06 (5%) :x: | 0.95 (1%) :white_check_mark: |
| `["findfirst", "n=500", "reduce", "basesize=128"]`  | 0.38 (5%) :white_check_mark: | 0.44 (1%) :white_check_mark: |
| `["findfirst", "n=500", "reduce", "basesize=256"]`  | 0.85 (5%) :white_check_mark: | 0.97 (1%) :white_check_mark: |
| `["findfirst", "n=500", "reduce", "basesize=512"]`  |                1.35 (5%) :x: |                1.33 (1%) :x: |
| `["parallel_histogram", "assoc", "basesize=4096"]`  |                   0.97 (5%)  | 0.77 (1%) :white_check_mark: |
| `["parallel_histogram", "comm", "basesize=16384"]`  |                1.08 (5%) :x: |                1.01 (1%) :x: |
| `["parallel_histogram", "comm", "basesize=4096"]`   |                   0.96 (5%)  |                1.04 (1%) :x: |
| `["partition_length_maximum", "rand", "reduce"]`    | 0.89 (5%) :white_check_mark: |                1.01 (1%) :x: |
| `["splitby", "count", "foldl"]`                     | 0.92 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["splitby", "count", "reduce"]`                    | 0.79 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["sum", "random", "foldl"]`                        | 0.95 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["sum", "random", "reduce", "basesize=256"]`       | 0.87 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["sum", "random", "reduce", "basesize=512"]`       | 0.89 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["sum", "uniform", "reduce", "basesize=128"]`      | 0.86 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["sum", "uniform", "reduce", "basesize=256"]`      | 0.86 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["sum", "uniform", "reduce", "basesize=512"]`      | 0.90 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["sum", "valley", "reduce", "basesize=128"]`       | 0.87 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["sum", "valley", "reduce", "basesize=256"]`       | 0.86 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["sum", "valley", "reduce", "basesize=512"]`       | 0.87 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["words", "nthreads=2"]`                           |                1.08 (5%) :x: |                   1.00 (1%)  |

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
Julia Version 1.5.4
Commit 69fcb5745b (2021-03-11 19:13 UTC)
Platform Info:
  OS: Linux (x86_64-pc-linux-gnu)
      Ubuntu 20.04.2 LTS
  uname: Linux 5.8.0-1033-azure #35~20.04.1-Ubuntu SMP Wed May 19 06:46:04 UTC 2021 x86_64 x86_64
  CPU: Intel(R) Xeon(R) Platinum 8171M CPU @ 2.60GHz: 
              speed         user         nice          sys         idle          irq
       #1  2095 MHz      44463 s         17 s       2218 s      35724 s          0 s
       #2  2095 MHz      61489 s          4 s       2360 s      18434 s          0 s
       
  Memory: 6.790924072265625 GB (3530.86328125 MB free)
  Uptime: 830.0 sec
  Load Avg:  1.5810546875  1.4716796875  0.88818359375
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-9.0.1 (ORCJIT, skylake-avx512)
```

### Baseline
```
Julia Version 1.5.4
Commit 69fcb5745b (2021-03-11 19:13 UTC)
Platform Info:
  OS: Linux (x86_64-pc-linux-gnu)
      Ubuntu 20.04.2 LTS
  uname: Linux 5.8.0-1033-azure #35~20.04.1-Ubuntu SMP Wed May 19 06:46:04 UTC 2021 x86_64 x86_64
  CPU: Intel(R) Xeon(R) Platinum 8171M CPU @ 2.60GHz: 
              speed         user         nice          sys         idle          irq
       #1  2095 MHz      63813 s         17 s       2836 s      47813 s          0 s
       #2  2095 MHz      90409 s          4 s       3077 s      20684 s          0 s
       
  Memory: 6.790924072265625 GB (3578.04296875 MB free)
  Uptime: 1151.0 sec
  Load Avg:  1.6259765625  1.52099609375  1.0830078125
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-9.0.1 (ORCJIT, skylake-avx512)
```

---
# Target result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmark: 21 Jun 2021 - 1:18
* Package commit: 337a6a
* Julia commit: 69fcb5
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
| `["collect", "assoc", "basesize=1"]`                | 227.237 ms (5%) |         |  32.66 MiB (1%) |      286746 |
| `["collect", "assoc", "basesize=1024"]`             | 183.405 ms (5%) |         |   1.79 MiB (1%) |         570 |
| `["collect", "assoc", "basesize=32"]`               | 186.695 ms (5%) |         |   3.97 MiB (1%) |       13306 |
| `["collect", "seq"]`                                | 359.694 ms (5%) |         | 512.72 KiB (1%) |          15 |
| `["collect", "unordered", "basesize=1"]`            | 407.333 ms (5%) |         |  30.01 MiB (1%) |      360699 |
| `["collect", "unordered", "basesize=1024"]`         | 224.337 ms (5%) |         | 808.17 KiB (1%) |        2583 |
| `["collect", "unordered", "basesize=32"]`           | 208.415 ms (5%) |         |   1.48 MiB (1%) |       12804 |
| `["findfirst", "n=1000", "foldl"]`                  | 579.369 ms (5%) |         |                 |             |
| `["findfirst", "n=1000", "reduce", "basesize=128"]` | 541.933 ms (5%) |         |   1.02 MiB (1%) |       18247 |
| `["findfirst", "n=1000", "reduce", "basesize=256"]` | 460.727 ms (5%) |         | 484.97 KiB (1%) |        8496 |
| `["findfirst", "n=1000", "reduce", "basesize=512"]` | 597.882 ms (5%) |         | 352.27 KiB (1%) |        6187 |
| `["findfirst", "n=400", "foldl"]`                   | 428.627 ms (5%) |         |                 |             |
| `["findfirst", "n=400", "reduce", "basesize=128"]`  | 241.875 ms (5%) |         |   1.05 MiB (1%) |       18952 |
| `["findfirst", "n=400", "reduce", "basesize=256"]`  | 255.259 ms (5%) |         | 565.48 KiB (1%) |        9978 |
| `["findfirst", "n=400", "reduce", "basesize=512"]`  | 270.881 ms (5%) |         | 355.16 KiB (1%) |        6260 |
| `["findfirst", "n=500", "foldl"]`                   |  72.185 ms (5%) |         |                 |             |
| `["findfirst", "n=500", "reduce", "basesize=128"]`  |  68.902 ms (5%) |         | 381.09 KiB (1%) |        6630 |
| `["findfirst", "n=500", "reduce", "basesize=256"]`  | 148.109 ms (5%) |         | 403.22 KiB (1%) |        7028 |
| `["findfirst", "n=500", "reduce", "basesize=512"]`  | 153.677 ms (5%) |         | 222.56 KiB (1%) |        3884 |
| `["overhead", "default"]`                           |  54.003 μs (5%) |         |  47.33 KiB (1%) |         381 |
| `["overhead", "stoppable=false"]`                   |  55.703 μs (5%) |         |  47.36 KiB (1%) |         381 |
| `["overhead", "stoppable=true"]`                    | 133.408 μs (5%) |         | 139.64 KiB (1%) |        2463 |
| `["parallel_histogram", "assoc", "basesize=16384"]` |   3.332 ms (5%) |         | 730.06 KiB (1%) |          57 |
| `["parallel_histogram", "assoc", "basesize=4096"]`  |   3.855 ms (5%) |         |   1.79 MiB (1%) |         213 |
| `["parallel_histogram", "assoc", "basesize=8192"]`  |   3.600 ms (5%) |         |   1.43 MiB (1%) |         117 |
| `["parallel_histogram", "comm", "basesize=16384"]`  |  16.000 ms (5%) |         |   1.25 MiB (1%) |        1138 |
| `["parallel_histogram", "comm", "basesize=4096"]`   |  22.758 ms (5%) |         |   1.07 MiB (1%) |        2440 |
| `["parallel_histogram", "comm", "basesize=8192"]`   |  19.278 ms (5%) |         |   1.25 MiB (1%) |        1144 |
| `["parallel_histogram", "seq"]`                     |   6.118 ms (5%) |         | 364.61 KiB (1%) |          24 |
| `["partition_length_maximum", "rand", "foldl"]`     |  29.522 ms (5%) |         |                 |             |
| `["partition_length_maximum", "rand", "reduce"]`    |  14.648 ms (5%) |         |   2.66 KiB (1%) |          48 |
| `["splitby", "count", "foldl"]`                     |   3.684 ms (5%) |         |   96 bytes (1%) |           4 |
| `["splitby", "count", "man"]`                       |   1.609 ms (5%) |         |                 |             |
| `["splitby", "count", "reduce"]`                    | 944.554 μs (5%) |         |   2.88 KiB (1%) |          55 |
| `["sum", "random", "foldl"]`                        |  13.813 ms (5%) |         |   32 bytes (1%) |           2 |
| `["sum", "random", "reduce", "basesize=128"]`       |   8.027 ms (5%) |         | 103.23 KiB (1%) |        1018 |
| `["sum", "random", "reduce", "basesize=256"]`       |   6.845 ms (5%) |         |  51.23 KiB (1%) |         506 |
| `["sum", "random", "reduce", "basesize=512"]`       |   6.910 ms (5%) |         |  25.30 KiB (1%) |         252 |
| `["sum", "uniform", "foldl"]`                       |  13.287 ms (5%) |         |   32 bytes (1%) |           2 |
| `["sum", "uniform", "reduce", "basesize=128"]`      |   6.655 ms (5%) |         | 103.23 KiB (1%) |        1018 |
| `["sum", "uniform", "reduce", "basesize=256"]`      |   6.559 ms (5%) |         |  51.23 KiB (1%) |         506 |
| `["sum", "uniform", "reduce", "basesize=512"]`      |   6.787 ms (5%) |         |  25.25 KiB (1%) |         251 |
| `["sum", "valley", "foldl"]`                        |  13.698 ms (5%) |         |   32 bytes (1%) |           2 |
| `["sum", "valley", "reduce", "basesize=128"]`       |   6.886 ms (5%) |         | 103.23 KiB (1%) |        1018 |
| `["sum", "valley", "reduce", "basesize=256"]`       |   6.804 ms (5%) |         |  51.23 KiB (1%) |         506 |
| `["sum", "valley", "reduce", "basesize=512"]`       |   6.774 ms (5%) |         |  25.25 KiB (1%) |         251 |
| `["words", "nthreads=1"]`                           |  18.884 ms (5%) |         |  31.66 MiB (1%) |     1031225 |
| `["words", "nthreads=2"]`                           |  13.480 ms (5%) |         |  32.38 MiB (1%) |     1031317 |
| `["words", "nthreads=4"]`                           |  13.548 ms (5%) |         |  32.83 MiB (1%) |     1031428 |

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
Julia Version 1.5.4
Commit 69fcb5745b (2021-03-11 19:13 UTC)
Platform Info:
  OS: Linux (x86_64-pc-linux-gnu)
      Ubuntu 20.04.2 LTS
  uname: Linux 5.8.0-1033-azure #35~20.04.1-Ubuntu SMP Wed May 19 06:46:04 UTC 2021 x86_64 x86_64
  CPU: Intel(R) Xeon(R) Platinum 8171M CPU @ 2.60GHz: 
              speed         user         nice          sys         idle          irq
       #1  2095 MHz      44463 s         17 s       2218 s      35724 s          0 s
       #2  2095 MHz      61489 s          4 s       2360 s      18434 s          0 s
       
  Memory: 6.790924072265625 GB (3530.86328125 MB free)
  Uptime: 830.0 sec
  Load Avg:  1.5810546875  1.4716796875  0.88818359375
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-9.0.1 (ORCJIT, skylake-avx512)
```

---
# Baseline result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmark: 21 Jun 2021 - 1:24
* Package commit: 2cfb4c
* Julia commit: 69fcb5
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
| `["collect", "assoc", "basesize=1"]`                | 226.477 ms (5%) |         |  32.66 MiB (1%) |      286739 |
| `["collect", "assoc", "basesize=1024"]`             | 199.594 ms (5%) |         |   1.79 MiB (1%) |         570 |
| `["collect", "assoc", "basesize=32"]`               | 193.314 ms (5%) |         |   3.97 MiB (1%) |       13305 |
| `["collect", "seq"]`                                | 369.770 ms (5%) |         | 512.72 KiB (1%) |          15 |
| `["collect", "unordered", "basesize=1"]`            | 421.903 ms (5%) |         |  30.01 MiB (1%) |      360635 |
| `["collect", "unordered", "basesize=1024"]`         | 274.479 ms (5%) |         | 892.52 KiB (1%) |        5300 |
| `["collect", "unordered", "basesize=32"]`           | 228.724 ms (5%) |         |   1.47 MiB (1%) |       12637 |
| `["findfirst", "n=1000", "foldl"]`                  | 608.346 ms (5%) |         |                 |             |
| `["findfirst", "n=1000", "reduce", "basesize=128"]` | 428.425 ms (5%) |         | 765.80 KiB (1%) |       13415 |
| `["findfirst", "n=1000", "reduce", "basesize=256"]` | 468.099 ms (5%) |         | 485.00 KiB (1%) |        8497 |
| `["findfirst", "n=1000", "reduce", "basesize=512"]` | 612.020 ms (5%) |         | 335.83 KiB (1%) |        5889 |
| `["findfirst", "n=400", "foldl"]`                   | 423.823 ms (5%) |         |                 |             |
| `["findfirst", "n=400", "reduce", "basesize=128"]`  | 247.573 ms (5%) |         |   1.12 MiB (1%) |       20153 |
| `["findfirst", "n=400", "reduce", "basesize=256"]`  | 241.094 ms (5%) |         | 593.09 KiB (1%) |       10457 |
| `["findfirst", "n=400", "reduce", "basesize=512"]`  | 281.346 ms (5%) |         | 355.28 KiB (1%) |        6270 |
| `["findfirst", "n=500", "foldl"]`                   |  72.263 ms (5%) |         |                 |             |
| `["findfirst", "n=500", "reduce", "basesize=128"]`  | 180.989 ms (5%) |         | 870.39 KiB (1%) |       15167 |
| `["findfirst", "n=500", "reduce", "basesize=256"]`  | 174.072 ms (5%) |         | 417.48 KiB (1%) |        7288 |
| `["findfirst", "n=500", "reduce", "basesize=512"]`  | 114.097 ms (5%) |         | 167.50 KiB (1%) |        2934 |
| `["overhead", "default"]`                           |  55.703 μs (5%) |         |  47.33 KiB (1%) |         381 |
| `["overhead", "stoppable=false"]`                   |  55.503 μs (5%) |         |  47.36 KiB (1%) |         381 |
| `["overhead", "stoppable=true"]`                    | 133.108 μs (5%) |         | 139.64 KiB (1%) |        2463 |
| `["parallel_histogram", "assoc", "basesize=16384"]` |   3.316 ms (5%) |         | 730.06 KiB (1%) |          57 |
| `["parallel_histogram", "assoc", "basesize=4096"]`  |   3.984 ms (5%) |         |   2.32 MiB (1%) |         225 |
| `["parallel_histogram", "assoc", "basesize=8192"]`  |   3.575 ms (5%) |         |   1.43 MiB (1%) |         117 |
| `["parallel_histogram", "comm", "basesize=16384"]`  |  14.867 ms (5%) |         |   1.24 MiB (1%) |         736 |
| `["parallel_histogram", "comm", "basesize=4096"]`   |  23.739 ms (5%) |         |   1.03 MiB (1%) |        2133 |
| `["parallel_histogram", "comm", "basesize=8192"]`   |  20.040 ms (5%) |         |   1.25 MiB (1%) |        1274 |
| `["parallel_histogram", "seq"]`                     |   6.037 ms (5%) |         | 364.61 KiB (1%) |          24 |
| `["partition_length_maximum", "rand", "foldl"]`     |  29.294 ms (5%) |         |                 |             |
| `["partition_length_maximum", "rand", "reduce"]`    |  16.488 ms (5%) |         |   2.63 KiB (1%) |          47 |
| `["splitby", "count", "foldl"]`                     |   4.006 ms (5%) |         |   96 bytes (1%) |           4 |
| `["splitby", "count", "man"]`                       |   1.612 ms (5%) |         |                 |             |
| `["splitby", "count", "reduce"]`                    |   1.190 ms (5%) |         |   2.88 KiB (1%) |          55 |
| `["sum", "random", "foldl"]`                        |  14.573 ms (5%) |         |   32 bytes (1%) |           2 |
| `["sum", "random", "reduce", "basesize=128"]`       |   7.920 ms (5%) |         | 103.23 KiB (1%) |        1018 |
| `["sum", "random", "reduce", "basesize=256"]`       |   7.852 ms (5%) |         |  51.23 KiB (1%) |         506 |
| `["sum", "random", "reduce", "basesize=512"]`       |   7.766 ms (5%) |         |  25.30 KiB (1%) |         252 |
| `["sum", "uniform", "foldl"]`                       |  13.542 ms (5%) |         |   32 bytes (1%) |           2 |
| `["sum", "uniform", "reduce", "basesize=128"]`      |   7.715 ms (5%) |         | 103.23 KiB (1%) |        1018 |
| `["sum", "uniform", "reduce", "basesize=256"]`      |   7.616 ms (5%) |         |  51.23 KiB (1%) |         506 |
| `["sum", "uniform", "reduce", "basesize=512"]`      |   7.570 ms (5%) |         |  25.25 KiB (1%) |         251 |
| `["sum", "valley", "foldl"]`                        |  14.265 ms (5%) |         |   32 bytes (1%) |           2 |
| `["sum", "valley", "reduce", "basesize=128"]`       |   7.929 ms (5%) |         | 103.23 KiB (1%) |        1018 |
| `["sum", "valley", "reduce", "basesize=256"]`       |   7.897 ms (5%) |         |  51.23 KiB (1%) |         506 |
| `["sum", "valley", "reduce", "basesize=512"]`       |   7.800 ms (5%) |         |  25.25 KiB (1%) |         251 |
| `["words", "nthreads=1"]`                           |  19.025 ms (5%) |         |  31.58 MiB (1%) |     1028841 |
| `["words", "nthreads=2"]`                           |  12.534 ms (5%) |         |  32.29 MiB (1%) |     1028927 |
| `["words", "nthreads=4"]`                           |  13.206 ms (5%) |         |  32.74 MiB (1%) |     1028994 |

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
Julia Version 1.5.4
Commit 69fcb5745b (2021-03-11 19:13 UTC)
Platform Info:
  OS: Linux (x86_64-pc-linux-gnu)
      Ubuntu 20.04.2 LTS
  uname: Linux 5.8.0-1033-azure #35~20.04.1-Ubuntu SMP Wed May 19 06:46:04 UTC 2021 x86_64 x86_64
  CPU: Intel(R) Xeon(R) Platinum 8171M CPU @ 2.60GHz: 
              speed         user         nice          sys         idle          irq
       #1  2095 MHz      63813 s         17 s       2836 s      47813 s          0 s
       #2  2095 MHz      90409 s          4 s       3077 s      20684 s          0 s
       
  Memory: 6.790924072265625 GB (3578.04296875 MB free)
  Uptime: 1151.0 sec
  Load Avg:  1.6259765625  1.52099609375  1.0830078125
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-9.0.1 (ORCJIT, skylake-avx512)
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
    CPU MHz:                         2095.176
    BogoMIPS:                        4190.35
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

