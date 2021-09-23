# Multi-thread benchmark result

* Pull request commit: [`8794cca6ad6b0c3455c2f5baa72532cdd0e06c9a`](https://github.com/JuliaFolds/Transducers.jl/commit/8794cca6ad6b0c3455c2f5baa72532cdd0e06c9a)
* Pull request: <https://github.com/JuliaFolds/Transducers.jl/pull/243> (Update */Manifest.toml)

# Judge result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmarks:
    - Target: 23 Sep 2021 - 01:22
    - Baseline: 23 Sep 2021 - 01:27
* Package commits:
    - Target: 99fec2
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
| `["collect", "unordered", "basesize=1"]`            | 0.92 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["collect", "unordered", "basesize=1024"]`         |                1.18 (5%) :x: |                1.14 (1%) :x: |
| `["findfirst", "n=1000", "reduce", "basesize=128"]` |                1.93 (5%) :x: |                1.77 (1%) :x: |
| `["findfirst", "n=1000", "reduce", "basesize=256"]` |                   0.99 (5%)  | 0.96 (1%) :white_check_mark: |
| `["findfirst", "n=1000", "reduce", "basesize=512"]` | 0.94 (5%) :white_check_mark: | 0.97 (1%) :white_check_mark: |
| `["findfirst", "n=400", "reduce", "basesize=128"]`  |                   0.97 (5%)  | 0.93 (1%) :white_check_mark: |
| `["findfirst", "n=400", "reduce", "basesize=256"]`  |                   1.00 (5%)  |                1.01 (1%) :x: |
| `["findfirst", "n=400", "reduce", "basesize=512"]`  |                   1.03 (5%)  |                1.10 (1%) :x: |
| `["findfirst", "n=500", "reduce", "basesize=128"]`  |                1.69 (5%) :x: |                1.71 (1%) :x: |
| `["findfirst", "n=500", "reduce", "basesize=256"]`  |                1.32 (5%) :x: |                1.19 (1%) :x: |
| `["findfirst", "n=500", "reduce", "basesize=512"]`  |                1.32 (5%) :x: |                1.18 (1%) :x: |
| `["overhead", "default"]`                           |                1.14 (5%) :x: |                   1.00 (1%)  |
| `["overhead", "stoppable=false"]`                   |                1.06 (5%) :x: |                   1.00 (1%)  |
| `["parallel_histogram", "comm", "basesize=4096"]`   |                1.07 (5%) :x: | 0.99 (1%) :white_check_mark: |

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
  CPU: Intel(R) Xeon(R) CPU E5-2673 v3 @ 2.40GHz: 
              speed         user         nice          sys         idle          irq
       #1  2394 MHz      58587 s         13 s       2556 s      18158 s          0 s
       #2  2394 MHz      52919 s         12 s       2315 s      24641 s          0 s
       
  Memory: 6.790924072265625 GB (3439.6171875 MB free)
  Uptime: 805.0 sec
  Load Avg:  1.7158203125  1.552734375  0.97216796875
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
      Ubuntu 20.04.3 LTS
  uname: Linux 5.8.0-1041-azure #44~20.04.1-Ubuntu SMP Fri Aug 20 20:41:09 UTC 2021 x86_64 x86_64
  CPU: Intel(R) Xeon(R) CPU E5-2673 v3 @ 2.40GHz: 
              speed         user         nice          sys         idle          irq
       #1  2394 MHz      79020 s         13 s       3125 s      32064 s          0 s
       #2  2394 MHz      84236 s         12 s       2941 s      27493 s          0 s
       
  Memory: 6.790924072265625 GB (3378.66015625 MB free)
  Uptime: 1155.0 sec
  Load Avg:  1.61279296875  1.56982421875  1.16064453125
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-9.0.1 (ORCJIT, haswell)
```

---
# Target result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmark: 23 Sep 2021 - 1:22
* Package commit: 99fec2
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
| `["collect", "assoc", "basesize=1"]`                | 287.242 ms (5%) |         |   32.66 MiB (1%) |      286758 |
| `["collect", "assoc", "basesize=1024"]`             | 232.456 ms (5%) |         |    1.79 MiB (1%) |         570 |
| `["collect", "assoc", "basesize=32"]`               | 235.945 ms (5%) |         |    3.97 MiB (1%) |       13307 |
| `["collect", "seq"]`                                | 457.605 ms (5%) |         |  512.72 KiB (1%) |          15 |
| `["collect", "unordered", "basesize=1"]`            | 481.939 ms (5%) |         |   30.01 MiB (1%) |      360583 |
| `["collect", "unordered", "basesize=1024"]`         | 352.644 ms (5%) |         |  949.39 KiB (1%) |        7120 |
| `["collect", "unordered", "basesize=32"]`           | 263.798 ms (5%) |         |    1.47 MiB (1%) |       12560 |
| `["findfirst", "n=1000", "foldl"]`                  | 663.463 ms (5%) |         |                  |             |
| `["findfirst", "n=1000", "reduce", "basesize=128"]` | 814.515 ms (5%) |         |    1.31 MiB (1%) |       23464 |
| `["findfirst", "n=1000", "reduce", "basesize=256"]` | 485.462 ms (5%) |         |  466.45 KiB (1%) |        8172 |
| `["findfirst", "n=1000", "reduce", "basesize=512"]` | 651.254 ms (5%) |         |  358.50 KiB (1%) |        6279 |
| `["findfirst", "n=400", "foldl"]`                   | 486.923 ms (5%) |         |                  |             |
| `["findfirst", "n=400", "reduce", "basesize=128"]`  | 286.771 ms (5%) |         |    1.10 MiB (1%) |       19818 |
| `["findfirst", "n=400", "reduce", "basesize=256"]`  | 283.406 ms (5%) |         |  604.52 KiB (1%) |       10652 |
| `["findfirst", "n=400", "reduce", "basesize=512"]`  | 315.499 ms (5%) |         |  375.59 KiB (1%) |        6616 |
| `["findfirst", "n=500", "foldl"]`                   |  82.755 ms (5%) |         |                  |             |
| `["findfirst", "n=500", "reduce", "basesize=128"]`  | 253.384 ms (5%) |         | 1022.63 KiB (1%) |       17784 |
| `["findfirst", "n=500", "reduce", "basesize=256"]`  | 195.110 ms (5%) |         |  431.02 KiB (1%) |        7510 |
| `["findfirst", "n=500", "reduce", "basesize=512"]`  | 312.418 ms (5%) |         |  351.67 KiB (1%) |        6159 |
| `["overhead", "default"]`                           |  63.000 μs (5%) |         |   47.36 KiB (1%) |         382 |
| `["overhead", "stoppable=false"]`                   |  61.501 μs (5%) |         |   47.39 KiB (1%) |         382 |
| `["overhead", "stoppable=true"]`                    | 166.701 μs (5%) |         |  139.67 KiB (1%) |        2464 |
| `["parallel_histogram", "assoc", "basesize=16384"]` |   4.373 ms (5%) |         |  730.06 KiB (1%) |          57 |
| `["parallel_histogram", "assoc", "basesize=4096"]`  |   5.106 ms (5%) |         |    1.79 MiB (1%) |         213 |
| `["parallel_histogram", "assoc", "basesize=8192"]`  |   4.734 ms (5%) |         |    1.43 MiB (1%) |         117 |
| `["parallel_histogram", "comm", "basesize=16384"]`  |  12.287 ms (5%) |         |    1.22 MiB (1%) |         206 |
| `["parallel_histogram", "comm", "basesize=4096"]`   |  19.772 ms (5%) |         |    1.00 MiB (1%) |        1119 |
| `["parallel_histogram", "comm", "basesize=8192"]`   |  14.599 ms (5%) |         |    1.23 MiB (1%) |         311 |
| `["parallel_histogram", "seq"]`                     |   7.581 ms (5%) |         |  364.61 KiB (1%) |          24 |
| `["partition_length_maximum", "rand", "foldl"]`     |  56.641 ms (5%) |         |                  |             |
| `["partition_length_maximum", "rand", "reduce"]`    |  29.828 ms (5%) |         |    2.66 KiB (1%) |          48 |
| `["splitby", "count", "foldl"]`                     |   4.102 ms (5%) |         |    96 bytes (1%) |           4 |
| `["splitby", "count", "man"]`                       |   1.757 ms (5%) |         |                  |             |
| `["splitby", "count", "reduce"]`                    | 919.406 μs (5%) |         |    2.84 KiB (1%) |          54 |
| `["sum", "random", "foldl"]`                        |  16.422 ms (5%) |         |    32 bytes (1%) |           2 |
| `["sum", "random", "reduce", "basesize=128"]`       |   8.776 ms (5%) |         |  103.23 KiB (1%) |        1018 |
| `["sum", "random", "reduce", "basesize=256"]`       |   8.619 ms (5%) |         |   51.23 KiB (1%) |         506 |
| `["sum", "random", "reduce", "basesize=512"]`       |   8.639 ms (5%) |         |   25.30 KiB (1%) |         252 |
| `["sum", "uniform", "foldl"]`                       |  16.004 ms (5%) |         |    32 bytes (1%) |           2 |
| `["sum", "uniform", "reduce", "basesize=128"]`      |   8.610 ms (5%) |         |  103.23 KiB (1%) |        1018 |
| `["sum", "uniform", "reduce", "basesize=256"]`      |   8.426 ms (5%) |         |   51.23 KiB (1%) |         506 |
| `["sum", "uniform", "reduce", "basesize=512"]`      |   8.326 ms (5%) |         |   25.25 KiB (1%) |         251 |
| `["sum", "valley", "foldl"]`                        |  16.526 ms (5%) |         |    32 bytes (1%) |           2 |
| `["sum", "valley", "reduce", "basesize=128"]`       |   8.919 ms (5%) |         |  103.23 KiB (1%) |        1018 |
| `["sum", "valley", "reduce", "basesize=256"]`       |   8.752 ms (5%) |         |   51.23 KiB (1%) |         506 |
| `["sum", "valley", "reduce", "basesize=512"]`       |   8.684 ms (5%) |         |   25.25 KiB (1%) |         251 |
| `["words", "nthreads=1"]`                           |  25.155 ms (5%) |         |   31.91 MiB (1%) |     1039490 |
| `["words", "nthreads=2"]`                           |  16.267 ms (5%) |         |   32.27 MiB (1%) |     1039526 |
| `["words", "nthreads=4"]`                           |  17.076 ms (5%) |         |   33.17 MiB (1%) |     1039703 |

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
  CPU: Intel(R) Xeon(R) CPU E5-2673 v3 @ 2.40GHz: 
              speed         user         nice          sys         idle          irq
       #1  2394 MHz      58587 s         13 s       2556 s      18158 s          0 s
       #2  2394 MHz      52919 s         12 s       2315 s      24641 s          0 s
       
  Memory: 6.790924072265625 GB (3439.6171875 MB free)
  Uptime: 805.0 sec
  Load Avg:  1.7158203125  1.552734375  0.97216796875
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-9.0.1 (ORCJIT, haswell)
```

---
# Baseline result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmark: 23 Sep 2021 - 1:27
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

| ID                                                  | time            | GC time | memory          | allocations |
|-----------------------------------------------------|----------------:|--------:|----------------:|------------:|
| `["collect", "assoc", "basesize=1"]`                | 281.082 ms (5%) |         |  32.66 MiB (1%) |      286756 |
| `["collect", "assoc", "basesize=1024"]`             | 236.500 ms (5%) |         |   1.79 MiB (1%) |         570 |
| `["collect", "assoc", "basesize=32"]`               | 238.433 ms (5%) |         |   3.97 MiB (1%) |       13306 |
| `["collect", "seq"]`                                | 447.808 ms (5%) |         | 512.72 KiB (1%) |          15 |
| `["collect", "unordered", "basesize=1"]`            | 521.170 ms (5%) |         |  30.01 MiB (1%) |      360665 |
| `["collect", "unordered", "basesize=1024"]`         | 297.836 ms (5%) |         | 835.58 KiB (1%) |        3478 |
| `["collect", "unordered", "basesize=32"]`           | 267.508 ms (5%) |         |   1.47 MiB (1%) |       12504 |
| `["findfirst", "n=1000", "foldl"]`                  | 673.551 ms (5%) |         |                 |             |
| `["findfirst", "n=1000", "reduce", "basesize=128"]` | 422.726 ms (5%) |         | 758.64 KiB (1%) |       13283 |
| `["findfirst", "n=1000", "reduce", "basesize=256"]` | 490.554 ms (5%) |         | 484.97 KiB (1%) |        8496 |
| `["findfirst", "n=1000", "reduce", "basesize=512"]` | 691.777 ms (5%) |         | 367.92 KiB (1%) |        6449 |
| `["findfirst", "n=400", "foldl"]`                   | 492.581 ms (5%) |         |                 |             |
| `["findfirst", "n=400", "reduce", "basesize=128"]`  | 295.127 ms (5%) |         |   1.18 MiB (1%) |       21272 |
| `["findfirst", "n=400", "reduce", "basesize=256"]`  | 284.766 ms (5%) |         | 597.67 KiB (1%) |       10537 |
| `["findfirst", "n=400", "reduce", "basesize=512"]`  | 305.243 ms (5%) |         | 341.39 KiB (1%) |        6026 |
| `["findfirst", "n=500", "foldl"]`                   |  83.855 ms (5%) |         |                 |             |
| `["findfirst", "n=500", "reduce", "basesize=128"]`  | 149.684 ms (5%) |         | 597.33 KiB (1%) |       10412 |
| `["findfirst", "n=500", "reduce", "basesize=256"]`  | 148.268 ms (5%) |         | 361.30 KiB (1%) |        6285 |
| `["findfirst", "n=500", "reduce", "basesize=512"]`  | 237.212 ms (5%) |         | 298.48 KiB (1%) |        5218 |
| `["overhead", "default"]`                           |  55.400 μs (5%) |         |  47.36 KiB (1%) |         382 |
| `["overhead", "stoppable=false"]`                   |  57.900 μs (5%) |         |  47.39 KiB (1%) |         382 |
| `["overhead", "stoppable=true"]`                    | 163.901 μs (5%) |         | 139.67 KiB (1%) |        2464 |
| `["parallel_histogram", "assoc", "basesize=16384"]` |   4.358 ms (5%) |         | 730.06 KiB (1%) |          57 |
| `["parallel_histogram", "assoc", "basesize=4096"]`  |   5.155 ms (5%) |         |   1.79 MiB (1%) |         213 |
| `["parallel_histogram", "assoc", "basesize=8192"]`  |   4.713 ms (5%) |         |   1.43 MiB (1%) |         117 |
| `["parallel_histogram", "comm", "basesize=16384"]`  |  12.510 ms (5%) |         |   1.22 MiB (1%) |         160 |
| `["parallel_histogram", "comm", "basesize=4096"]`   |  18.560 ms (5%) |         |   1.02 MiB (1%) |        1195 |
| `["parallel_histogram", "comm", "basesize=8192"]`   |  15.339 ms (5%) |         |   1.23 MiB (1%) |         534 |
| `["parallel_histogram", "seq"]`                     |   7.597 ms (5%) |         | 364.61 KiB (1%) |          24 |
| `["partition_length_maximum", "rand", "foldl"]`     |  57.067 ms (5%) |         |                 |             |
| `["partition_length_maximum", "rand", "reduce"]`    |  29.791 ms (5%) |         |   2.66 KiB (1%) |          48 |
| `["splitby", "count", "foldl"]`                     |   4.159 ms (5%) |         |   96 bytes (1%) |           4 |
| `["splitby", "count", "man"]`                       |   1.788 ms (5%) |         |                 |             |
| `["splitby", "count", "reduce"]`                    | 935.805 μs (5%) |         |   2.84 KiB (1%) |          54 |
| `["sum", "random", "foldl"]`                        |  16.379 ms (5%) |         |   32 bytes (1%) |           2 |
| `["sum", "random", "reduce", "basesize=128"]`       |   8.798 ms (5%) |         | 103.23 KiB (1%) |        1018 |
| `["sum", "random", "reduce", "basesize=256"]`       |   8.616 ms (5%) |         |  51.23 KiB (1%) |         506 |
| `["sum", "random", "reduce", "basesize=512"]`       |   8.629 ms (5%) |         |  25.30 KiB (1%) |         252 |
| `["sum", "uniform", "foldl"]`                       |  15.970 ms (5%) |         |   32 bytes (1%) |           2 |
| `["sum", "uniform", "reduce", "basesize=128"]`      |   8.600 ms (5%) |         | 103.23 KiB (1%) |        1018 |
| `["sum", "uniform", "reduce", "basesize=256"]`      |   8.391 ms (5%) |         |  51.23 KiB (1%) |         506 |
| `["sum", "uniform", "reduce", "basesize=512"]`      |   8.409 ms (5%) |         |  25.25 KiB (1%) |         251 |
| `["sum", "valley", "foldl"]`                        |  16.517 ms (5%) |         |   32 bytes (1%) |           2 |
| `["sum", "valley", "reduce", "basesize=128"]`       |   8.877 ms (5%) |         | 103.23 KiB (1%) |        1018 |
| `["sum", "valley", "reduce", "basesize=256"]`       |   8.662 ms (5%) |         |  51.23 KiB (1%) |         506 |
| `["sum", "valley", "reduce", "basesize=512"]`       |   8.628 ms (5%) |         |  25.25 KiB (1%) |         251 |
| `["words", "nthreads=1"]`                           |  24.249 ms (5%) |         |  31.84 MiB (1%) |     1037310 |
| `["words", "nthreads=2"]`                           |  16.109 ms (5%) |         |  32.20 MiB (1%) |     1037346 |
| `["words", "nthreads=4"]`                           |  16.833 ms (5%) |         |  33.09 MiB (1%) |     1037479 |

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
  CPU: Intel(R) Xeon(R) CPU E5-2673 v3 @ 2.40GHz: 
              speed         user         nice          sys         idle          irq
       #1  2394 MHz      79020 s         13 s       3125 s      32064 s          0 s
       #2  2394 MHz      84236 s         12 s       2941 s      27493 s          0 s
       
  Memory: 6.790924072265625 GB (3378.66015625 MB free)
  Uptime: 1155.0 sec
  Load Avg:  1.61279296875  1.56982421875  1.16064453125
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
    CPU MHz:                         2394.453
    BogoMIPS:                        4788.90
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

