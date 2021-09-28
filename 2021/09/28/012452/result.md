# Multi-thread benchmark result

* Pull request commit: [`dc6540c2d87c22dd370afb94682298041c98f988`](https://github.com/JuliaFolds/Transducers.jl/commit/dc6540c2d87c22dd370afb94682298041c98f988)
* Pull request: <https://github.com/JuliaFolds/Transducers.jl/pull/243> (Update */Manifest.toml)

# Judge result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmarks:
    - Target: 28 Sep 2021 - 01:18
    - Baseline: 28 Sep 2021 - 01:24
* Package commits:
    - Target: dfeddb
    - Baseline: 1e5e53
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
| `["collect", "unordered", "basesize=1"]`            | 0.94 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["collect", "unordered", "basesize=1024"]`         |                1.08 (5%) :x: |                   1.00 (1%)  |
| `["findfirst", "n=1000", "reduce", "basesize=128"]` |                   1.05 (5%)  |                1.09 (1%) :x: |
| `["findfirst", "n=1000", "reduce", "basesize=512"]` | 0.94 (5%) :white_check_mark: | 0.90 (1%) :white_check_mark: |
| `["findfirst", "n=400", "reduce", "basesize=128"]`  |                   0.98 (5%)  |                1.03 (1%) :x: |
| `["findfirst", "n=400", "reduce", "basesize=256"]`  |                   1.03 (5%)  |                1.04 (1%) :x: |
| `["findfirst", "n=500", "reduce", "basesize=128"]`  |                1.36 (5%) :x: |                1.33 (1%) :x: |
| `["findfirst", "n=500", "reduce", "basesize=256"]`  | 0.70 (5%) :white_check_mark: | 0.85 (1%) :white_check_mark: |
| `["overhead", "stoppable=false"]`                   | 0.95 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["parallel_histogram", "assoc", "basesize=4096"]`  |                   0.99 (5%)  | 0.87 (1%) :white_check_mark: |
| `["parallel_histogram", "comm", "basesize=16384"]`  |                1.07 (5%) :x: |                1.01 (1%) :x: |
| `["parallel_histogram", "comm", "basesize=4096"]`   | 0.76 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["splitby", "count", "foldl"]`                     | 0.55 (5%) :white_check_mark: | 0.17 (1%) :white_check_mark: |
| `["splitby", "count", "man"]`                       |                1.12 (5%) :x: |                   1.00 (1%)  |
| `["splitby", "count", "reduce"]`                    |                   1.04 (5%)  | 0.98 (1%) :white_check_mark: |

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
      Ubuntu 20.04.3 LTS
  uname: Linux 5.8.0-1041-azure #44~20.04.1-Ubuntu SMP Fri Aug 20 20:41:09 UTC 2021 x86_64 x86_64
  CPU: Intel(R) Xeon(R) Platinum 8171M CPU @ 2.60GHz: 
              speed         user         nice          sys         idle          irq
       #1  2095 MHz      49522 s         13 s       2336 s      26265 s          0 s
       #2  2095 MHz      60438 s         15 s       2564 s      15162 s          0 s
       
  Memory: 6.790924072265625 GB (3574.2265625 MB free)
  Uptime: 789.0 sec
  Load Avg:  1.6279296875  1.46142578125  0.8994140625
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
      Ubuntu 20.04.3 LTS
  uname: Linux 5.8.0-1041-azure #44~20.04.1-Ubuntu SMP Fri Aug 20 20:41:09 UTC 2021 x86_64 x86_64
  CPU: Intel(R) Xeon(R) Platinum 8171M CPU @ 2.60GHz: 
              speed         user         nice          sys         idle          irq
       #1  2095 MHz      72482 s         13 s       3008 s      36828 s          0 s
       #2  2095 MHz      88620 s         15 s       3146 s      20794 s          0 s
       
  Memory: 6.790924072265625 GB (3521.67578125 MB free)
  Uptime: 1133.0 sec
  Load Avg:  1.69970703125  1.54833984375  1.10986328125
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-9.0.1 (ORCJIT, skylake-avx512)
```

---
# Target result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmark: 28 Sep 2021 - 1:18
* Package commit: dfeddb
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
| `["collect", "assoc", "basesize=1"]`                | 287.395 ms (5%) |         |  32.66 MiB (1%) |      286746 |
| `["collect", "assoc", "basesize=1024"]`             | 242.238 ms (5%) |         |   1.79 MiB (1%) |         569 |
| `["collect", "assoc", "basesize=32"]`               | 242.726 ms (5%) |         |   3.97 MiB (1%) |       13306 |
| `["collect", "seq"]`                                | 474.126 ms (5%) |         | 512.72 KiB (1%) |          15 |
| `["collect", "unordered", "basesize=1"]`            | 515.110 ms (5%) |         |  30.01 MiB (1%) |      360601 |
| `["collect", "unordered", "basesize=1024"]`         | 367.920 ms (5%) |         | 949.48 KiB (1%) |        7123 |
| `["collect", "unordered", "basesize=32"]`           | 271.048 ms (5%) |         |   1.48 MiB (1%) |       12800 |
| `["findfirst", "n=1000", "foldl"]`                  | 749.073 ms (5%) |         |                 |             |
| `["findfirst", "n=1000", "reduce", "basesize=128"]` | 813.379 ms (5%) |         |   1.24 MiB (1%) |       22262 |
| `["findfirst", "n=1000", "reduce", "basesize=256"]` | 503.473 ms (5%) |         | 466.42 KiB (1%) |        8171 |
| `["findfirst", "n=1000", "reduce", "basesize=512"]` | 701.583 ms (5%) |         | 329.00 KiB (1%) |        5775 |
| `["findfirst", "n=400", "foldl"]`                   | 561.930 ms (5%) |         |                 |             |
| `["findfirst", "n=400", "reduce", "basesize=128"]`  | 304.130 ms (5%) |         |   1.12 MiB (1%) |       20136 |
| `["findfirst", "n=400", "reduce", "basesize=256"]`  | 310.291 ms (5%) |         | 597.75 KiB (1%) |       10540 |
| `["findfirst", "n=400", "reduce", "basesize=512"]`  | 340.119 ms (5%) |         | 373.55 KiB (1%) |        6585 |
| `["findfirst", "n=500", "foldl"]`                   |  97.454 ms (5%) |         |                 |             |
| `["findfirst", "n=500", "reduce", "basesize=128"]`  | 253.039 ms (5%) |         | 892.00 KiB (1%) |       15560 |
| `["findfirst", "n=500", "reduce", "basesize=256"]`  | 148.177 ms (5%) |         | 354.23 KiB (1%) |        6159 |
| `["findfirst", "n=500", "reduce", "basesize=512"]`  | 388.589 ms (5%) |         | 388.45 KiB (1%) |        6801 |
| `["overhead", "default"]`                           |  65.802 μs (5%) |         |  47.33 KiB (1%) |         381 |
| `["overhead", "stoppable=false"]`                   |  65.602 μs (5%) |         |  47.36 KiB (1%) |         381 |
| `["overhead", "stoppable=true"]`                    | 181.706 μs (5%) |         | 139.64 KiB (1%) |        2463 |
| `["parallel_histogram", "assoc", "basesize=16384"]` |   4.797 ms (5%) |         | 730.06 KiB (1%) |          57 |
| `["parallel_histogram", "assoc", "basesize=4096"]`  |   5.523 ms (5%) |         |   1.79 MiB (1%) |         213 |
| `["parallel_histogram", "assoc", "basesize=8192"]`  |   5.165 ms (5%) |         |   1.43 MiB (1%) |         117 |
| `["parallel_histogram", "comm", "basesize=16384"]`  |  15.939 ms (5%) |         |   1.23 MiB (1%) |         634 |
| `["parallel_histogram", "comm", "basesize=4096"]`   |  18.860 ms (5%) |         |   1.04 MiB (1%) |        1713 |
| `["parallel_histogram", "comm", "basesize=8192"]`   |  20.755 ms (5%) |         |   1.25 MiB (1%) |        1201 |
| `["parallel_histogram", "seq"]`                     |   8.753 ms (5%) |         | 364.61 KiB (1%) |          24 |
| `["partition_length_maximum", "rand", "foldl"]`     |  40.220 ms (5%) |         |                 |             |
| `["partition_length_maximum", "rand", "reduce"]`    |  20.389 ms (5%) |         |   2.66 KiB (1%) |          48 |
| `["splitby", "count", "foldl"]`                     |   2.902 ms (5%) |         |   16 bytes (1%) |           1 |
| `["splitby", "count", "man"]`                       |   2.282 ms (5%) |         |                 |             |
| `["splitby", "count", "reduce"]`                    |   1.404 ms (5%) |         |   2.78 KiB (1%) |          52 |
| `["sum", "random", "foldl"]`                        |  19.384 ms (5%) |         |   32 bytes (1%) |           2 |
| `["sum", "random", "reduce", "basesize=128"]`       |   9.989 ms (5%) |         | 103.23 KiB (1%) |        1018 |
| `["sum", "random", "reduce", "basesize=256"]`       |   9.889 ms (5%) |         |  51.23 KiB (1%) |         506 |
| `["sum", "random", "reduce", "basesize=512"]`       |   9.797 ms (5%) |         |  25.30 KiB (1%) |         252 |
| `["sum", "uniform", "foldl"]`                       |  18.314 ms (5%) |         |   32 bytes (1%) |           2 |
| `["sum", "uniform", "reduce", "basesize=128"]`      |   9.527 ms (5%) |         | 103.23 KiB (1%) |        1018 |
| `["sum", "uniform", "reduce", "basesize=256"]`      |   9.434 ms (5%) |         |  51.23 KiB (1%) |         506 |
| `["sum", "uniform", "reduce", "basesize=512"]`      |   9.351 ms (5%) |         |  25.25 KiB (1%) |         251 |
| `["sum", "valley", "foldl"]`                        |  19.188 ms (5%) |         |   32 bytes (1%) |           2 |
| `["sum", "valley", "reduce", "basesize=128"]`       |   9.884 ms (5%) |         | 103.23 KiB (1%) |        1018 |
| `["sum", "valley", "reduce", "basesize=256"]`       |   9.772 ms (5%) |         |  51.23 KiB (1%) |         506 |
| `["sum", "valley", "reduce", "basesize=512"]`       |   9.712 ms (5%) |         |  25.25 KiB (1%) |         251 |
| `["words", "nthreads=1"]`                           |  25.226 ms (5%) |         |  31.74 MiB (1%) |     1034612 |
| `["words", "nthreads=2"]`                           |  15.769 ms (5%) |         |  32.10 MiB (1%) |     1034666 |
| `["words", "nthreads=4"]`                           |  16.875 ms (5%) |         |  33.00 MiB (1%) |     1034844 |

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
      Ubuntu 20.04.3 LTS
  uname: Linux 5.8.0-1041-azure #44~20.04.1-Ubuntu SMP Fri Aug 20 20:41:09 UTC 2021 x86_64 x86_64
  CPU: Intel(R) Xeon(R) Platinum 8171M CPU @ 2.60GHz: 
              speed         user         nice          sys         idle          irq
       #1  2095 MHz      49522 s         13 s       2336 s      26265 s          0 s
       #2  2095 MHz      60438 s         15 s       2564 s      15162 s          0 s
       
  Memory: 6.790924072265625 GB (3574.2265625 MB free)
  Uptime: 789.0 sec
  Load Avg:  1.6279296875  1.46142578125  0.8994140625
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-9.0.1 (ORCJIT, skylake-avx512)
```

---
# Baseline result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmark: 28 Sep 2021 - 1:24
* Package commit: 1e5e53
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

| ID                                                  | time            | GC time   | memory          | allocations |
|-----------------------------------------------------|----------------:|----------:|----------------:|------------:|
| `["collect", "assoc", "basesize=1"]`                | 286.604 ms (5%) |           |  32.66 MiB (1%) |      286738 |
| `["collect", "assoc", "basesize=1024"]`             | 241.774 ms (5%) |           |   1.79 MiB (1%) |         569 |
| `["collect", "assoc", "basesize=32"]`               | 243.218 ms (5%) |           |   3.97 MiB (1%) |       13307 |
| `["collect", "seq"]`                                | 474.136 ms (5%) |           | 512.72 KiB (1%) |          15 |
| `["collect", "unordered", "basesize=1"]`            | 546.653 ms (5%) | 13.742 ms |  30.01 MiB (1%) |      360645 |
| `["collect", "unordered", "basesize=1024"]`         | 341.104 ms (5%) |           | 953.05 KiB (1%) |        7237 |
| `["collect", "unordered", "basesize=32"]`           | 270.799 ms (5%) |           |   1.48 MiB (1%) |       12669 |
| `["findfirst", "n=1000", "foldl"]`                  | 754.005 ms (5%) |           |                 |             |
| `["findfirst", "n=1000", "reduce", "basesize=128"]` | 775.546 ms (5%) |           |   1.14 MiB (1%) |       20506 |
| `["findfirst", "n=1000", "reduce", "basesize=256"]` | 508.445 ms (5%) |           | 466.42 KiB (1%) |        8171 |
| `["findfirst", "n=1000", "reduce", "basesize=512"]` | 748.878 ms (5%) |           | 363.73 KiB (1%) |        6386 |
| `["findfirst", "n=400", "foldl"]`                   | 565.280 ms (5%) |           |                 |             |
| `["findfirst", "n=400", "reduce", "basesize=128"]`  | 309.659 ms (5%) |           |   1.09 MiB (1%) |       19574 |
| `["findfirst", "n=400", "reduce", "basesize=256"]`  | 300.124 ms (5%) |           | 576.83 KiB (1%) |       10173 |
| `["findfirst", "n=400", "reduce", "basesize=512"]`  | 341.944 ms (5%) |           | 371.00 KiB (1%) |        6538 |
| `["findfirst", "n=500", "foldl"]`                   |  97.901 ms (5%) |           |                 |             |
| `["findfirst", "n=500", "reduce", "basesize=128"]`  | 185.997 ms (5%) |           | 669.31 KiB (1%) |       11671 |
| `["findfirst", "n=500", "reduce", "basesize=256"]`  | 210.631 ms (5%) |           | 414.84 KiB (1%) |        7231 |
| `["findfirst", "n=500", "reduce", "basesize=512"]`  | 390.169 ms (5%) |           | 388.50 KiB (1%) |        6801 |
| `["overhead", "default"]`                           |  67.202 μs (5%) |           |  47.33 KiB (1%) |         381 |
| `["overhead", "stoppable=false"]`                   |  69.402 μs (5%) |           |  47.39 KiB (1%) |         382 |
| `["overhead", "stoppable=true"]`                    | 182.206 μs (5%) |           | 139.67 KiB (1%) |        2464 |
| `["parallel_histogram", "assoc", "basesize=16384"]` |   4.769 ms (5%) |           | 730.06 KiB (1%) |          57 |
| `["parallel_histogram", "assoc", "basesize=4096"]`  |   5.569 ms (5%) |           |   2.06 MiB (1%) |         219 |
| `["parallel_histogram", "assoc", "basesize=8192"]`  |   5.140 ms (5%) |           |   1.43 MiB (1%) |         117 |
| `["parallel_histogram", "comm", "basesize=16384"]`  |  14.877 ms (5%) |           |   1.22 MiB (1%) |         160 |
| `["parallel_histogram", "comm", "basesize=4096"]`   |  24.736 ms (5%) |           |   1.05 MiB (1%) |        2373 |
| `["parallel_histogram", "comm", "basesize=8192"]`   |  20.691 ms (5%) |           |   1.25 MiB (1%) |        1119 |
| `["parallel_histogram", "seq"]`                     |   8.675 ms (5%) |           | 364.61 KiB (1%) |          24 |
| `["partition_length_maximum", "rand", "foldl"]`     |  40.414 ms (5%) |           |                 |             |
| `["partition_length_maximum", "rand", "reduce"]`    |  20.385 ms (5%) |           |   2.66 KiB (1%) |          48 |
| `["splitby", "count", "foldl"]`                     |   5.318 ms (5%) |           |   96 bytes (1%) |           4 |
| `["splitby", "count", "man"]`                       |   2.030 ms (5%) |           |                 |             |
| `["splitby", "count", "reduce"]`                    |   1.352 ms (5%) |           |   2.84 KiB (1%) |          54 |
| `["sum", "random", "foldl"]`                        |  19.047 ms (5%) |           |   32 bytes (1%) |           2 |
| `["sum", "random", "reduce", "basesize=128"]`       |   9.791 ms (5%) |           | 103.23 KiB (1%) |        1018 |
| `["sum", "random", "reduce", "basesize=256"]`       |   9.670 ms (5%) |           |  51.23 KiB (1%) |         506 |
| `["sum", "random", "reduce", "basesize=512"]`       |   9.609 ms (5%) |           |  25.30 KiB (1%) |         252 |
| `["sum", "uniform", "foldl"]`                       |  18.597 ms (5%) |           |   32 bytes (1%) |           2 |
| `["sum", "uniform", "reduce", "basesize=128"]`      |   9.517 ms (5%) |           | 103.23 KiB (1%) |        1018 |
| `["sum", "uniform", "reduce", "basesize=256"]`      |   9.420 ms (5%) |           |  51.23 KiB (1%) |         506 |
| `["sum", "uniform", "reduce", "basesize=512"]`      |   9.364 ms (5%) |           |  25.25 KiB (1%) |         251 |
| `["sum", "valley", "foldl"]`                        |  19.190 ms (5%) |           |   32 bytes (1%) |           2 |
| `["sum", "valley", "reduce", "basesize=128"]`       |   9.850 ms (5%) |           | 103.23 KiB (1%) |        1018 |
| `["sum", "valley", "reduce", "basesize=256"]`       |   9.744 ms (5%) |           |  51.23 KiB (1%) |         506 |
| `["sum", "valley", "reduce", "basesize=512"]`       |   9.675 ms (5%) |           |  25.25 KiB (1%) |         251 |
| `["words", "nthreads=1"]`                           |  25.307 ms (5%) |           |  31.66 MiB (1%) |     1031865 |
| `["words", "nthreads=2"]`                           |  16.451 ms (5%) |           |  32.38 MiB (1%) |     1031946 |
| `["words", "nthreads=4"]`                           |  16.801 ms (5%) |           |  32.83 MiB (1%) |     1032013 |

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
      Ubuntu 20.04.3 LTS
  uname: Linux 5.8.0-1041-azure #44~20.04.1-Ubuntu SMP Fri Aug 20 20:41:09 UTC 2021 x86_64 x86_64
  CPU: Intel(R) Xeon(R) Platinum 8171M CPU @ 2.60GHz: 
              speed         user         nice          sys         idle          irq
       #1  2095 MHz      72482 s         13 s       3008 s      36828 s          0 s
       #2  2095 MHz      88620 s         15 s       3146 s      20794 s          0 s
       
  Memory: 6.790924072265625 GB (3521.67578125 MB free)
  Uptime: 1133.0 sec
  Load Avg:  1.69970703125  1.54833984375  1.10986328125
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
    CPU MHz:                         2095.108
    BogoMIPS:                        4190.21
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

