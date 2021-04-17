# Multi-thread benchmark result

* Pull request commit: [`8b33be968f7f43380f37d93371f21e10a5b1959f`](https://github.com/JuliaFolds/Transducers.jl/commit/8b33be968f7f43380f37d93371f21e10a5b1959f)
* Pull request: <https://github.com/JuliaFolds/Transducers.jl/pull/470> (Use Julia 1.6 for building docs)

# Judge result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmarks:
    - Target: 17 Apr 2021 - 22:48
    - Baseline: 17 Apr 2021 - 22:53
* Package commits:
    - Target: 6128c6
    - Baseline: 3d3cc9
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
| `["collect", "unordered", "basesize=1024"]`         | 0.91 (5%) :white_check_mark: | 0.97 (1%) :white_check_mark: |
| `["findfirst", "n=1000", "reduce", "basesize=128"]` | 0.59 (5%) :white_check_mark: | 0.63 (1%) :white_check_mark: |
| `["findfirst", "n=1000", "reduce", "basesize=256"]` |                1.08 (5%) :x: |                1.05 (1%) :x: |
| `["findfirst", "n=1000", "reduce", "basesize=512"]` | 0.93 (5%) :white_check_mark: | 0.88 (1%) :white_check_mark: |
| `["findfirst", "n=400", "reduce", "basesize=128"]`  |                   0.99 (5%)  | 0.99 (1%) :white_check_mark: |
| `["findfirst", "n=400", "reduce", "basesize=256"]`  |                   1.03 (5%)  |                1.01 (1%) :x: |
| `["findfirst", "n=400", "reduce", "basesize=512"]`  |                   0.99 (5%)  |                1.04 (1%) :x: |
| `["findfirst", "n=500", "reduce", "basesize=128"]`  | 0.59 (5%) :white_check_mark: | 0.62 (1%) :white_check_mark: |
| `["findfirst", "n=500", "reduce", "basesize=256"]`  |                   1.04 (5%)  |                1.03 (1%) :x: |
| `["findfirst", "n=500", "reduce", "basesize=512"]`  |                2.19 (5%) :x: |                1.74 (1%) :x: |
| `["parallel_histogram", "comm", "basesize=4096"]`   | 0.84 (5%) :white_check_mark: |                   1.01 (1%)  |
| `["parallel_histogram", "comm", "basesize=8192"]`   |                1.05 (5%) :x: |                   1.00 (1%)  |
| `["splitby", "count", "foldl"]`                     | 0.47 (5%) :white_check_mark: | 0.17 (1%) :white_check_mark: |
| `["splitby", "count", "man"]`                       | 0.91 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["words", "nthreads=4"]`                           | 0.95 (5%) :white_check_mark: |                   0.99 (1%)  |

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
  uname: Linux 5.4.0-1043-azure #45-Ubuntu SMP Fri Mar 19 17:33:38 UTC 2021 x86_64 x86_64
  CPU: Intel(R) Xeon(R) CPU E5-2673 v3 @ 2.40GHz: 
              speed         user         nice          sys         idle          irq
       #1  2397 MHz      55037 s         17 s       2251 s      29395 s          0 s
       #2  2397 MHz      56392 s          5 s       2230 s      27930 s          0 s
       
  Memory: 6.791343688964844 GB (3710.8359375 MB free)
  Uptime: 872.0 sec
  Load Avg:  1.689453125  1.52392578125  0.93310546875
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-9.0.1 (ORCJIT, haswell)
```

### Baseline
```
Julia Version 1.5.4
Commit 69fcb5745b (2021-03-11 19:13 UTC)
Platform Info:
  OS: Linux (x86_64-pc-linux-gnu)
      Ubuntu 20.04.2 LTS
  uname: Linux 5.4.0-1043-azure #45-Ubuntu SMP Fri Mar 19 17:33:38 UTC 2021 x86_64 x86_64
  CPU: Intel(R) Xeon(R) CPU E5-2673 v3 @ 2.40GHz: 
              speed         user         nice          sys         idle          irq
       #1  2397 MHz      79838 s         17 s       2708 s      36438 s          0 s
       #2  2397 MHz      80918 s          5 s       2680 s      35261 s          0 s
       
  Memory: 6.791343688964844 GB (3740.59375 MB free)
  Uptime: 1196.0 sec
  Load Avg:  1.7236328125  1.599609375  1.13720703125
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-9.0.1 (ORCJIT, haswell)
```

---
# Target result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmark: 17 Apr 2021 - 22:48
* Package commit: 6128c6
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
| `["collect", "assoc", "basesize=1"]`                | 290.860 ms (5%) |         |  32.66 MiB (1%) |      286756 |
| `["collect", "assoc", "basesize=1024"]`             | 246.449 ms (5%) |         |   1.79 MiB (1%) |         569 |
| `["collect", "assoc", "basesize=32"]`               | 247.006 ms (5%) |         |   3.97 MiB (1%) |       13307 |
| `["collect", "seq"]`                                | 485.310 ms (5%) |         | 512.72 KiB (1%) |          15 |
| `["collect", "unordered", "basesize=1"]`            | 491.164 ms (5%) |         |  30.01 MiB (1%) |      360569 |
| `["collect", "unordered", "basesize=1024"]`         | 317.212 ms (5%) |         | 878.02 KiB (1%) |        4836 |
| `["collect", "unordered", "basesize=32"]`           | 272.610 ms (5%) |         |   1.47 MiB (1%) |       12609 |
| `["findfirst", "n=1000", "foldl"]`                  | 699.223 ms (5%) |         |                 |             |
| `["findfirst", "n=1000", "reduce", "basesize=128"]` | 513.152 ms (5%) |         | 875.11 KiB (1%) |       15342 |
| `["findfirst", "n=1000", "reduce", "basesize=256"]` | 506.415 ms (5%) |         | 484.97 KiB (1%) |        8496 |
| `["findfirst", "n=1000", "reduce", "basesize=512"]` | 647.868 ms (5%) |         | 317.50 KiB (1%) |        5573 |
| `["findfirst", "n=400", "foldl"]`                   | 526.393 ms (5%) |         |                 |             |
| `["findfirst", "n=400", "reduce", "basesize=128"]`  | 281.010 ms (5%) |         |   1.07 MiB (1%) |       19315 |
| `["findfirst", "n=400", "reduce", "basesize=256"]`  | 300.045 ms (5%) |         | 604.66 KiB (1%) |       10661 |
| `["findfirst", "n=400", "reduce", "basesize=512"]`  | 311.751 ms (5%) |         | 366.44 KiB (1%) |        6459 |
| `["findfirst", "n=500", "foldl"]`                   |  88.664 ms (5%) |         |                 |             |
| `["findfirst", "n=500", "reduce", "basesize=128"]`  | 145.459 ms (5%) |         | 541.72 KiB (1%) |        9448 |
| `["findfirst", "n=500", "reduce", "basesize=256"]`  | 178.438 ms (5%) |         | 382.63 KiB (1%) |        6676 |
| `["findfirst", "n=500", "reduce", "basesize=512"]`  | 335.100 ms (5%) |         | 351.64 KiB (1%) |        6150 |
| `["overhead", "default"]`                           |  61.402 μs (5%) |         |  47.36 KiB (1%) |         382 |
| `["overhead", "stoppable=false"]`                   |  61.403 μs (5%) |         |  47.39 KiB (1%) |         382 |
| `["overhead", "stoppable=true"]`                    | 165.507 μs (5%) |         | 139.67 KiB (1%) |        2464 |
| `["parallel_histogram", "assoc", "basesize=16384"]` |   4.580 ms (5%) |         | 730.06 KiB (1%) |          57 |
| `["parallel_histogram", "assoc", "basesize=4096"]`  |   5.289 ms (5%) |         |   1.79 MiB (1%) |         213 |
| `["parallel_histogram", "assoc", "basesize=8192"]`  |   4.924 ms (5%) |         |   1.43 MiB (1%) |         117 |
| `["parallel_histogram", "comm", "basesize=16384"]`  |  12.233 ms (5%) |         |   1.22 MiB (1%) |         160 |
| `["parallel_histogram", "comm", "basesize=4096"]`   |  17.460 ms (5%) |         |   1.01 MiB (1%) |        1260 |
| `["parallel_histogram", "comm", "basesize=8192"]`   |  14.740 ms (5%) |         |   1.23 MiB (1%) |         348 |
| `["parallel_histogram", "seq"]`                     |   8.083 ms (5%) |         | 364.61 KiB (1%) |          24 |
| `["partition_length_maximum", "rand", "foldl"]`     |  61.167 ms (5%) |         |                 |             |
| `["partition_length_maximum", "rand", "reduce"]`    |  31.027 ms (5%) |         |   2.66 KiB (1%) |          48 |
| `["splitby", "count", "foldl"]`                     |   2.098 ms (5%) |         |   16 bytes (1%) |           1 |
| `["splitby", "count", "man"]`                       |   1.691 ms (5%) |         |                 |             |
| `["splitby", "count", "reduce"]`                    | 984.943 μs (5%) |         |   2.75 KiB (1%) |          51 |
| `["sum", "random", "foldl"]`                        |  17.541 ms (5%) |         |   32 bytes (1%) |           2 |
| `["sum", "random", "reduce", "basesize=128"]`       |   9.160 ms (5%) |         | 103.23 KiB (1%) |        1018 |
| `["sum", "random", "reduce", "basesize=256"]`       |   9.083 ms (5%) |         |  51.23 KiB (1%) |         506 |
| `["sum", "random", "reduce", "basesize=512"]`       |   9.053 ms (5%) |         |  25.30 KiB (1%) |         252 |
| `["sum", "uniform", "foldl"]`                       |  17.070 ms (5%) |         |   32 bytes (1%) |           2 |
| `["sum", "uniform", "reduce", "basesize=128"]`      |   8.974 ms (5%) |         | 103.23 KiB (1%) |        1018 |
| `["sum", "uniform", "reduce", "basesize=256"]`      |   8.831 ms (5%) |         |  51.23 KiB (1%) |         506 |
| `["sum", "uniform", "reduce", "basesize=512"]`      |   8.849 ms (5%) |         |  25.25 KiB (1%) |         251 |
| `["sum", "valley", "foldl"]`                        |  17.582 ms (5%) |         |   32 bytes (1%) |           2 |
| `["sum", "valley", "reduce", "basesize=128"]`       |   9.227 ms (5%) |         | 103.23 KiB (1%) |        1018 |
| `["sum", "valley", "reduce", "basesize=256"]`       |   9.131 ms (5%) |         |  51.23 KiB (1%) |         506 |
| `["sum", "valley", "reduce", "basesize=512"]`       |   9.091 ms (5%) |         |  25.25 KiB (1%) |         251 |
| `["words", "nthreads=1"]`                           |  25.516 ms (5%) |         |  31.57 MiB (1%) |     1028261 |
| `["words", "nthreads=2"]`                           |  16.215 ms (5%) |         |  32.28 MiB (1%) |     1028340 |
| `["words", "nthreads=4"]`                           |  16.400 ms (5%) |         |  32.73 MiB (1%) |     1028457 |

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
  uname: Linux 5.4.0-1043-azure #45-Ubuntu SMP Fri Mar 19 17:33:38 UTC 2021 x86_64 x86_64
  CPU: Intel(R) Xeon(R) CPU E5-2673 v3 @ 2.40GHz: 
              speed         user         nice          sys         idle          irq
       #1  2397 MHz      55037 s         17 s       2251 s      29395 s          0 s
       #2  2397 MHz      56392 s          5 s       2230 s      27930 s          0 s
       
  Memory: 6.791343688964844 GB (3710.8359375 MB free)
  Uptime: 872.0 sec
  Load Avg:  1.689453125  1.52392578125  0.93310546875
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-9.0.1 (ORCJIT, haswell)
```

---
# Baseline result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmark: 17 Apr 2021 - 22:53
* Package commit: 3d3cc9
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

| ID                                                  | time            | GC time | memory           | allocations |
|-----------------------------------------------------|----------------:|--------:|-----------------:|------------:|
| `["collect", "assoc", "basesize=1"]`                | 294.299 ms (5%) |         |   32.66 MiB (1%) |      286755 |
| `["collect", "assoc", "basesize=1024"]`             | 244.984 ms (5%) |         |    1.79 MiB (1%) |         570 |
| `["collect", "assoc", "basesize=32"]`               | 246.909 ms (5%) |         |    3.97 MiB (1%) |       13306 |
| `["collect", "seq"]`                                | 485.472 ms (5%) |         |  512.72 KiB (1%) |          15 |
| `["collect", "unordered", "basesize=1"]`            | 506.325 ms (5%) |         |   30.01 MiB (1%) |      360595 |
| `["collect", "unordered", "basesize=1024"]`         | 347.555 ms (5%) |         |  905.73 KiB (1%) |        5705 |
| `["collect", "unordered", "basesize=32"]`           | 271.034 ms (5%) |         |    1.47 MiB (1%) |       12628 |
| `["findfirst", "n=1000", "foldl"]`                  | 703.359 ms (5%) |         |                  |             |
| `["findfirst", "n=1000", "reduce", "basesize=128"]` | 866.322 ms (5%) |         |    1.35 MiB (1%) |       24174 |
| `["findfirst", "n=1000", "reduce", "basesize=256"]` | 470.719 ms (5%) |         |  461.78 KiB (1%) |        8090 |
| `["findfirst", "n=1000", "reduce", "basesize=512"]` | 697.965 ms (5%) |         |  361.08 KiB (1%) |        6333 |
| `["findfirst", "n=400", "foldl"]`                   | 525.280 ms (5%) |         |                  |             |
| `["findfirst", "n=400", "reduce", "basesize=128"]`  | 283.957 ms (5%) |         |    1.09 MiB (1%) |       19545 |
| `["findfirst", "n=400", "reduce", "basesize=256"]`  | 292.193 ms (5%) |         |  597.73 KiB (1%) |       10539 |
| `["findfirst", "n=400", "reduce", "basesize=512"]`  | 316.173 ms (5%) |         |  352.83 KiB (1%) |        6230 |
| `["findfirst", "n=500", "foldl"]`                   |  89.265 ms (5%) |         |                  |             |
| `["findfirst", "n=500", "reduce", "basesize=128"]`  | 244.891 ms (5%) |         |  878.33 KiB (1%) |       15333 |
| `["findfirst", "n=500", "reduce", "basesize=256"]`  | 170.774 ms (5%) |         |  373.25 KiB (1%) |        6507 |
| `["findfirst", "n=500", "reduce", "basesize=512"]`  | 152.721 ms (5%) |         |  202.05 KiB (1%) |        3538 |
| `["overhead", "default"]`                           |  59.903 μs (5%) |         |   47.36 KiB (1%) |         382 |
| `["overhead", "stoppable=false"]`                   |  61.703 μs (5%) |         |   47.39 KiB (1%) |         382 |
| `["overhead", "stoppable=true"]`                    | 171.208 μs (5%) |         |  139.67 KiB (1%) |        2464 |
| `["parallel_histogram", "assoc", "basesize=16384"]` |   4.602 ms (5%) |         |  730.06 KiB (1%) |          57 |
| `["parallel_histogram", "assoc", "basesize=4096"]`  |   5.306 ms (5%) |         |    1.79 MiB (1%) |         213 |
| `["parallel_histogram", "assoc", "basesize=8192"]`  |   4.962 ms (5%) |         |    1.43 MiB (1%) |         117 |
| `["parallel_histogram", "comm", "basesize=16384"]`  |  12.281 ms (5%) |         |    1.22 MiB (1%) |         200 |
| `["parallel_histogram", "comm", "basesize=4096"]`   |  20.760 ms (5%) |         | 1023.03 KiB (1%) |         626 |
| `["parallel_histogram", "comm", "basesize=8192"]`   |  13.985 ms (5%) |         |    1.23 MiB (1%) |         379 |
| `["parallel_histogram", "seq"]`                     |   8.137 ms (5%) |         |  364.61 KiB (1%) |          24 |
| `["partition_length_maximum", "rand", "foldl"]`     |  61.266 ms (5%) |         |                  |             |
| `["partition_length_maximum", "rand", "reduce"]`    |  30.973 ms (5%) |         |    2.66 KiB (1%) |          48 |
| `["splitby", "count", "foldl"]`                     |   4.448 ms (5%) |         |    96 bytes (1%) |           4 |
| `["splitby", "count", "man"]`                       |   1.858 ms (5%) |         |                  |             |
| `["splitby", "count", "reduce"]`                    | 986.938 μs (5%) |         |    2.75 KiB (1%) |          51 |
| `["sum", "random", "foldl"]`                        |  17.248 ms (5%) |         |    32 bytes (1%) |           2 |
| `["sum", "random", "reduce", "basesize=128"]`       |   9.075 ms (5%) |         |  103.23 KiB (1%) |        1018 |
| `["sum", "random", "reduce", "basesize=256"]`       |   8.988 ms (5%) |         |   51.23 KiB (1%) |         506 |
| `["sum", "random", "reduce", "basesize=512"]`       |   8.933 ms (5%) |         |   25.30 KiB (1%) |         252 |
| `["sum", "uniform", "foldl"]`                       |  17.105 ms (5%) |         |    32 bytes (1%) |           2 |
| `["sum", "uniform", "reduce", "basesize=128"]`      |   8.953 ms (5%) |         |  103.23 KiB (1%) |        1018 |
| `["sum", "uniform", "reduce", "basesize=256"]`      |   8.843 ms (5%) |         |   51.23 KiB (1%) |         506 |
| `["sum", "uniform", "reduce", "basesize=512"]`      |   8.797 ms (5%) |         |   25.25 KiB (1%) |         251 |
| `["sum", "valley", "foldl"]`                        |  17.615 ms (5%) |         |    32 bytes (1%) |           2 |
| `["sum", "valley", "reduce", "basesize=128"]`       |   9.270 ms (5%) |         |  103.23 KiB (1%) |        1018 |
| `["sum", "valley", "reduce", "basesize=256"]`       |   9.126 ms (5%) |         |   51.23 KiB (1%) |         506 |
| `["sum", "valley", "reduce", "basesize=512"]`       |   9.079 ms (5%) |         |   25.25 KiB (1%) |         251 |
| `["words", "nthreads=1"]`                           |  25.574 ms (5%) |         |   31.65 MiB (1%) |     1030823 |
| `["words", "nthreads=2"]`                           |  16.542 ms (5%) |         |   32.37 MiB (1%) |     1030942 |
| `["words", "nthreads=4"]`                           |  17.280 ms (5%) |         |   33.00 MiB (1%) |     1031097 |

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
  uname: Linux 5.4.0-1043-azure #45-Ubuntu SMP Fri Mar 19 17:33:38 UTC 2021 x86_64 x86_64
  CPU: Intel(R) Xeon(R) CPU E5-2673 v3 @ 2.40GHz: 
              speed         user         nice          sys         idle          irq
       #1  2397 MHz      79838 s         17 s       2708 s      36438 s          0 s
       #2  2397 MHz      80918 s          5 s       2680 s      35261 s          0 s
       
  Memory: 6.791343688964844 GB (3740.59375 MB free)
  Uptime: 1196.0 sec
  Load Avg:  1.7236328125  1.599609375  1.13720703125
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-9.0.1 (ORCJIT, haswell)
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
    CPU MHz:                         2397.224
    BogoMIPS:                        4794.44
    Hypervisor vendor:               Microsoft
    Virtualization type:             full
    L1d cache:                       64 KiB
    L1i cache:                       64 KiB
    L2 cache:                        512 KiB
    L3 cache:                        30 MiB
    NUMA node0 CPU(s):               0,1
    Vulnerability Itlb multihit:     KVM: Vulnerable
    Vulnerability L1tf:              Mitigation; PTE Inversion
    Vulnerability Mds:               Mitigation; Clear CPU buffers; SMT Host state unknown
    Vulnerability Meltdown:          Mitigation; PTI
    Vulnerability Spec store bypass: Vulnerable
    Vulnerability Spectre v1:        Mitigation; usercopy/swapgs barriers and __user pointer sanitization
    Vulnerability Spectre v2:        Mitigation; Full generic retpoline, STIBP disabled, RSB filling
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

