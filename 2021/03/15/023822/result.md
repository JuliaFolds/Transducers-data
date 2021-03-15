# Multi-thread benchmark result

* Pull request commit: [`ddeedb60f7c225aefd72943b2944bf5368b508d9`](https://github.com/JuliaFolds/Transducers.jl/commit/ddeedb60f7c225aefd72943b2944bf5368b508d9)
* Pull request: <https://github.com/JuliaFolds/Transducers.jl/pull/464> (Add PreChunk and PreVacant)

# Judge result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmarks:
    - Target: 15 Mar 2021 - 02:32
    - Baseline: 15 Mar 2021 - 02:37
* Package commits:
    - Target: 0f752f
    - Baseline: eb6f73
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
| `["collect", "unordered", "basesize=1024"]`         | 0.89 (5%) :white_check_mark: | 0.95 (1%) :white_check_mark: |
| `["findfirst", "n=1000", "reduce", "basesize=256"]` |                1.13 (5%) :x: |                1.17 (1%) :x: |
| `["findfirst", "n=1000", "reduce", "basesize=512"]` | 0.89 (5%) :white_check_mark: | 0.93 (1%) :white_check_mark: |
| `["findfirst", "n=400", "reduce", "basesize=128"]`  |                   1.02 (5%)  | 0.98 (1%) :white_check_mark: |
| `["findfirst", "n=500", "reduce", "basesize=128"]`  |                1.22 (5%) :x: |                1.12 (1%) :x: |
| `["findfirst", "n=500", "reduce", "basesize=256"]`  | 0.83 (5%) :white_check_mark: | 0.97 (1%) :white_check_mark: |
| `["findfirst", "n=500", "reduce", "basesize=512"]`  | 0.84 (5%) :white_check_mark: | 0.87 (1%) :white_check_mark: |
| `["overhead", "stoppable=false"]`                   |                1.09 (5%) :x: |                   1.00 (1%)  |
| `["parallel_histogram", "assoc", "basesize=4096"]`  |                   0.98 (5%)  | 0.87 (1%) :white_check_mark: |
| `["parallel_histogram", "comm", "basesize=4096"]`   |                   1.04 (5%)  | 0.95 (1%) :white_check_mark: |
| `["splitby", "count", "foldl"]`                     |                1.64 (5%) :x: |                6.00 (1%) :x: |
| `["splitby", "count", "man"]`                       | 0.87 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["splitby", "count", "reduce"]`                    |                1.06 (5%) :x: |                1.02 (1%) :x: |
| `["sum", "random", "foldl"]`                        | 0.89 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["sum", "random", "reduce", "basesize=128"]`       | 0.89 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["sum", "random", "reduce", "basesize=256"]`       | 0.90 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["sum", "random", "reduce", "basesize=512"]`       | 0.91 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["sum", "uniform", "foldl"]`                       | 0.91 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["sum", "uniform", "reduce", "basesize=128"]`      | 0.89 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["sum", "uniform", "reduce", "basesize=256"]`      | 0.90 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["sum", "uniform", "reduce", "basesize=512"]`      | 0.89 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["sum", "valley", "foldl"]`                        | 0.92 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["sum", "valley", "reduce", "basesize=128"]`       | 0.90 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["sum", "valley", "reduce", "basesize=256"]`       | 0.90 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["sum", "valley", "reduce", "basesize=512"]`       | 0.91 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["words", "nthreads=2"]`                           | 0.93 (5%) :white_check_mark: | 0.98 (1%) :white_check_mark: |

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
  uname: Linux 5.4.0-1040-azure #42-Ubuntu SMP Fri Feb 5 15:39:06 UTC 2021 x86_64 x86_64
  CPU: Intel(R) Xeon(R) Platinum 8171M CPU @ 2.60GHz: 
              speed         user         nice          sys         idle          irq
       #1  2095 MHz      54929 s         16 s       2534 s      17054 s          0 s
       #2  2095 MHz      55032 s          6 s       2504 s      17077 s          0 s
       
  Memory: 6.791378021240234 GB (3426.0703125 MB free)
  Uptime: 763.0 sec
  Load Avg:  1.671875  1.537109375  0.94775390625
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
  uname: Linux 5.4.0-1040-azure #42-Ubuntu SMP Fri Feb 5 15:39:06 UTC 2021 x86_64 x86_64
  CPU: Intel(R) Xeon(R) Platinum 8171M CPU @ 2.60GHz: 
              speed         user         nice          sys         idle          irq
       #1  2095 MHz      77334 s         16 s       3061 s      25181 s          0 s
       #2  2095 MHz      80377 s          6 s       3052 s      22322 s          0 s
       
  Memory: 6.791378021240234 GB (3486.328125 MB free)
  Uptime: 1075.0 sec
  Load Avg:  1.72802734375  1.60986328125  1.14599609375
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-9.0.1 (ORCJIT, skylake-avx512)
```

---
# Target result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmark: 15 Mar 2021 - 2:32
* Package commit: 0f752f
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
| `["collect", "assoc", "basesize=1"]`                | 257.276 ms (5%) |         |   32.66 MiB (1%) |      286737 |
| `["collect", "assoc", "basesize=1024"]`             | 219.932 ms (5%) |         |    1.79 MiB (1%) |         569 |
| `["collect", "assoc", "basesize=32"]`               | 222.302 ms (5%) |         |    3.97 MiB (1%) |       13305 |
| `["collect", "seq"]`                                | 433.733 ms (5%) |         |  512.72 KiB (1%) |          15 |
| `["collect", "unordered", "basesize=1"]`            | 465.376 ms (5%) |         |   30.01 MiB (1%) |      360559 |
| `["collect", "unordered", "basesize=1024"]`         | 276.078 ms (5%) |         |  839.08 KiB (1%) |        3590 |
| `["collect", "unordered", "basesize=32"]`           | 252.220 ms (5%) |         |    1.47 MiB (1%) |       12636 |
| `["findfirst", "n=1000", "foldl"]`                  | 696.433 ms (5%) |         |                  |             |
| `["findfirst", "n=1000", "reduce", "basesize=128"]` | 776.772 ms (5%) |         |    1.25 MiB (1%) |       22503 |
| `["findfirst", "n=1000", "reduce", "basesize=256"]` | 516.611 ms (5%) |         |  498.73 KiB (1%) |        8735 |
| `["findfirst", "n=1000", "reduce", "basesize=512"]` | 654.658 ms (5%) |         |  326.77 KiB (1%) |        5735 |
| `["findfirst", "n=400", "foldl"]`                   | 527.938 ms (5%) |         |                  |             |
| `["findfirst", "n=400", "reduce", "basesize=128"]`  | 286.366 ms (5%) |         |    1.09 MiB (1%) |       19657 |
| `["findfirst", "n=400", "reduce", "basesize=256"]`  | 301.974 ms (5%) |         |  609.25 KiB (1%) |       10739 |
| `["findfirst", "n=400", "reduce", "basesize=512"]`  | 324.196 ms (5%) |         |  368.80 KiB (1%) |        6501 |
| `["findfirst", "n=500", "foldl"]`                   |  85.625 ms (5%) |         |                  |             |
| `["findfirst", "n=500", "reduce", "basesize=128"]`  | 235.139 ms (5%) |         |  862.05 KiB (1%) |       15048 |
| `["findfirst", "n=500", "reduce", "basesize=256"]`  | 132.912 ms (5%) |         |  351.86 KiB (1%) |        6114 |
| `["findfirst", "n=500", "reduce", "basesize=512"]`  | 228.340 ms (5%) |         |  257.38 KiB (1%) |        4506 |
| `["overhead", "default"]`                           |  62.701 μs (5%) |         |   47.33 KiB (1%) |         381 |
| `["overhead", "stoppable=false"]`                   |  64.201 μs (5%) |         |   47.36 KiB (1%) |         381 |
| `["overhead", "stoppable=true"]`                    | 154.702 μs (5%) |         |  139.64 KiB (1%) |        2463 |
| `["parallel_histogram", "assoc", "basesize=16384"]` |   3.877 ms (5%) |         |  730.06 KiB (1%) |          57 |
| `["parallel_histogram", "assoc", "basesize=4096"]`  |   4.845 ms (5%) |         |    1.79 MiB (1%) |         213 |
| `["parallel_histogram", "assoc", "basesize=8192"]`  |   4.317 ms (5%) |         |    1.43 MiB (1%) |         117 |
| `["parallel_histogram", "comm", "basesize=16384"]`  |  15.673 ms (5%) |         |    1.23 MiB (1%) |         569 |
| `["parallel_histogram", "comm", "basesize=4096"]`   |  24.814 ms (5%) |         | 1020.47 KiB (1%) |         909 |
| `["parallel_histogram", "comm", "basesize=8192"]`   |  22.903 ms (5%) |         |    1.26 MiB (1%) |        1388 |
| `["parallel_histogram", "seq"]`                     |   7.115 ms (5%) |         |  364.61 KiB (1%) |          24 |
| `["partition_length_maximum", "rand", "foldl"]`     |  34.714 ms (5%) |         |                  |             |
| `["partition_length_maximum", "rand", "reduce"]`    |  17.995 ms (5%) |         |    2.66 KiB (1%) |          48 |
| `["splitby", "count", "foldl"]`                     |   3.838 ms (5%) |         |    96 bytes (1%) |           4 |
| `["splitby", "count", "man"]`                       |   1.630 ms (5%) |         |                  |             |
| `["splitby", "count", "reduce"]`                    |   1.181 ms (5%) |         |    2.84 KiB (1%) |          54 |
| `["sum", "random", "foldl"]`                        |  16.062 ms (5%) |         |    32 bytes (1%) |           2 |
| `["sum", "random", "reduce", "basesize=128"]`       |   8.096 ms (5%) |         |  103.23 KiB (1%) |        1018 |
| `["sum", "random", "reduce", "basesize=256"]`       |   8.246 ms (5%) |         |   51.23 KiB (1%) |         506 |
| `["sum", "random", "reduce", "basesize=512"]`       |   8.167 ms (5%) |         |   25.30 KiB (1%) |         252 |
| `["sum", "uniform", "foldl"]`                       |  15.649 ms (5%) |         |    32 bytes (1%) |           2 |
| `["sum", "uniform", "reduce", "basesize=128"]`      |   7.883 ms (5%) |         |  103.23 KiB (1%) |        1018 |
| `["sum", "uniform", "reduce", "basesize=256"]`      |   7.960 ms (5%) |         |   51.23 KiB (1%) |         506 |
| `["sum", "uniform", "reduce", "basesize=512"]`      |   7.828 ms (5%) |         |   25.25 KiB (1%) |         251 |
| `["sum", "valley", "foldl"]`                        |  16.614 ms (5%) |         |    32 bytes (1%) |           2 |
| `["sum", "valley", "reduce", "basesize=128"]`       |   8.349 ms (5%) |         |  103.23 KiB (1%) |        1018 |
| `["sum", "valley", "reduce", "basesize=256"]`       |   8.185 ms (5%) |         |   51.23 KiB (1%) |         506 |
| `["sum", "valley", "reduce", "basesize=512"]`       |   8.259 ms (5%) |         |   25.25 KiB (1%) |         251 |
| `["words", "nthreads=1"]`                           |  22.268 ms (5%) |         |   31.44 MiB (1%) |     1024782 |
| `["words", "nthreads=2"]`                           |  14.252 ms (5%) |         |   31.80 MiB (1%) |     1024823 |
| `["words", "nthreads=4"]`                           |  14.920 ms (5%) |         |   32.52 MiB (1%) |     1024930 |

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
  uname: Linux 5.4.0-1040-azure #42-Ubuntu SMP Fri Feb 5 15:39:06 UTC 2021 x86_64 x86_64
  CPU: Intel(R) Xeon(R) Platinum 8171M CPU @ 2.60GHz: 
              speed         user         nice          sys         idle          irq
       #1  2095 MHz      54929 s         16 s       2534 s      17054 s          0 s
       #2  2095 MHz      55032 s          6 s       2504 s      17077 s          0 s
       
  Memory: 6.791378021240234 GB (3426.0703125 MB free)
  Uptime: 763.0 sec
  Load Avg:  1.671875  1.537109375  0.94775390625
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-9.0.1 (ORCJIT, skylake-avx512)
```

---
# Baseline result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmark: 15 Mar 2021 - 2:37
* Package commit: eb6f73
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
| `["collect", "assoc", "basesize=1"]`                | 265.330 ms (5%) |         |  32.66 MiB (1%) |      286739 |
| `["collect", "assoc", "basesize=1024"]`             | 214.672 ms (5%) |         |   1.79 MiB (1%) |         570 |
| `["collect", "assoc", "basesize=32"]`               | 222.073 ms (5%) |         |   3.97 MiB (1%) |       13306 |
| `["collect", "seq"]`                                | 436.865 ms (5%) |         | 512.72 KiB (1%) |          15 |
| `["collect", "unordered", "basesize=1"]`            | 473.322 ms (5%) |         |  30.01 MiB (1%) |      360569 |
| `["collect", "unordered", "basesize=1024"]`         | 308.564 ms (5%) |         | 879.36 KiB (1%) |        4861 |
| `["collect", "unordered", "basesize=32"]`           | 250.590 ms (5%) |         |   1.47 MiB (1%) |       12527 |
| `["findfirst", "n=1000", "foldl"]`                  | 682.478 ms (5%) |         |                 |             |
| `["findfirst", "n=1000", "reduce", "basesize=128"]` | 779.025 ms (5%) |         |   1.24 MiB (1%) |       22297 |
| `["findfirst", "n=1000", "reduce", "basesize=256"]` | 456.158 ms (5%) |         | 425.20 KiB (1%) |        7466 |
| `["findfirst", "n=1000", "reduce", "basesize=512"]` | 739.338 ms (5%) |         | 352.27 KiB (1%) |        6187 |
| `["findfirst", "n=400", "foldl"]`                   | 512.480 ms (5%) |         |                 |             |
| `["findfirst", "n=400", "reduce", "basesize=128"]`  | 282.028 ms (5%) |         |   1.11 MiB (1%) |       20056 |
| `["findfirst", "n=400", "reduce", "basesize=256"]`  | 299.591 ms (5%) |         | 607.14 KiB (1%) |       10711 |
| `["findfirst", "n=400", "reduce", "basesize=512"]`  | 311.257 ms (5%) |         | 371.05 KiB (1%) |        6539 |
| `["findfirst", "n=500", "foldl"]`                   |  88.942 ms (5%) |         |                 |             |
| `["findfirst", "n=500", "reduce", "basesize=128"]`  | 192.337 ms (5%) |         | 772.59 KiB (1%) |       13441 |
| `["findfirst", "n=500", "reduce", "basesize=256"]`  | 159.228 ms (5%) |         | 363.75 KiB (1%) |        6336 |
| `["findfirst", "n=500", "reduce", "basesize=512"]`  | 273.253 ms (5%) |         | 296.34 KiB (1%) |        5187 |
| `["overhead", "default"]`                           |  64.901 μs (5%) |         |  47.33 KiB (1%) |         381 |
| `["overhead", "stoppable=false"]`                   |  59.100 μs (5%) |         |  47.36 KiB (1%) |         381 |
| `["overhead", "stoppable=true"]`                    | 152.802 μs (5%) |         | 139.67 KiB (1%) |        2464 |
| `["parallel_histogram", "assoc", "basesize=16384"]` |   3.942 ms (5%) |         | 730.06 KiB (1%) |          57 |
| `["parallel_histogram", "assoc", "basesize=4096"]`  |   4.940 ms (5%) |         |   2.06 MiB (1%) |         219 |
| `["parallel_histogram", "assoc", "basesize=8192"]`  |   4.329 ms (5%) |         |   1.43 MiB (1%) |         117 |
| `["parallel_histogram", "comm", "basesize=16384"]`  |  15.105 ms (5%) |         |   1.22 MiB (1%) |         160 |
| `["parallel_histogram", "comm", "basesize=4096"]`   |  23.896 ms (5%) |         |   1.05 MiB (1%) |        2219 |
| `["parallel_histogram", "comm", "basesize=8192"]`   |  23.088 ms (5%) |         |   1.26 MiB (1%) |        1508 |
| `["parallel_histogram", "seq"]`                     |   7.037 ms (5%) |         | 364.61 KiB (1%) |          24 |
| `["partition_length_maximum", "rand", "foldl"]`     |  33.956 ms (5%) |         |                 |             |
| `["partition_length_maximum", "rand", "reduce"]`    |  17.854 ms (5%) |         |   2.66 KiB (1%) |          48 |
| `["splitby", "count", "foldl"]`                     |   2.344 ms (5%) |         |   16 bytes (1%) |           1 |
| `["splitby", "count", "man"]`                       |   1.870 ms (5%) |         |                 |             |
| `["splitby", "count", "reduce"]`                    |   1.113 ms (5%) |         |   2.78 KiB (1%) |          52 |
| `["sum", "random", "foldl"]`                        |  17.964 ms (5%) |         |   32 bytes (1%) |           2 |
| `["sum", "random", "reduce", "basesize=128"]`       |   9.046 ms (5%) |         | 103.23 KiB (1%) |        1018 |
| `["sum", "random", "reduce", "basesize=256"]`       |   9.133 ms (5%) |         |  51.23 KiB (1%) |         506 |
| `["sum", "random", "reduce", "basesize=512"]`       |   9.009 ms (5%) |         |  25.30 KiB (1%) |         252 |
| `["sum", "uniform", "foldl"]`                       |  17.257 ms (5%) |         |   32 bytes (1%) |           2 |
| `["sum", "uniform", "reduce", "basesize=128"]`      |   8.846 ms (5%) |         | 103.23 KiB (1%) |        1018 |
| `["sum", "uniform", "reduce", "basesize=256"]`      |   8.819 ms (5%) |         |  51.23 KiB (1%) |         506 |
| `["sum", "uniform", "reduce", "basesize=512"]`      |   8.754 ms (5%) |         |  25.25 KiB (1%) |         251 |
| `["sum", "valley", "foldl"]`                        |  18.138 ms (5%) |         |   32 bytes (1%) |           2 |
| `["sum", "valley", "reduce", "basesize=128"]`       |   9.251 ms (5%) |         | 103.23 KiB (1%) |        1018 |
| `["sum", "valley", "reduce", "basesize=256"]`       |   9.131 ms (5%) |         |  51.23 KiB (1%) |         506 |
| `["sum", "valley", "reduce", "basesize=512"]`       |   9.097 ms (5%) |         |  25.28 KiB (1%) |         252 |
| `["words", "nthreads=1"]`                           |  21.647 ms (5%) |         |  31.68 MiB (1%) |     1032011 |
| `["words", "nthreads=2"]`                           |  15.294 ms (5%) |         |  32.40 MiB (1%) |     1032094 |
| `["words", "nthreads=4"]`                           |  15.130 ms (5%) |         |  32.85 MiB (1%) |     1032160 |

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
  uname: Linux 5.4.0-1040-azure #42-Ubuntu SMP Fri Feb 5 15:39:06 UTC 2021 x86_64 x86_64
  CPU: Intel(R) Xeon(R) Platinum 8171M CPU @ 2.60GHz: 
              speed         user         nice          sys         idle          irq
       #1  2095 MHz      77334 s         16 s       3061 s      25181 s          0 s
       #2  2095 MHz      80377 s          6 s       3052 s      22322 s          0 s
       
  Memory: 6.791378021240234 GB (3486.328125 MB free)
  Uptime: 1075.0 sec
  Load Avg:  1.72802734375  1.60986328125  1.14599609375
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
    CPU MHz:                         2095.076
    BogoMIPS:                        4190.15
    Hypervisor vendor:               Microsoft
    Virtualization type:             full
    L1d cache:                       64 KiB
    L1i cache:                       64 KiB
    L2 cache:                        2 MiB
    L3 cache:                        35.8 MiB
    NUMA node0 CPU(s):               0,1
    Vulnerability Itlb multihit:     KVM: Vulnerable
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

