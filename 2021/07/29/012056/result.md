# Multi-thread benchmark result

* Pull request commit: [`cfddcc60572b4a97efb21951a871c5956e384008`](https://github.com/JuliaFolds/Transducers.jl/commit/cfddcc60572b4a97efb21951a871c5956e384008)
* Pull request: <https://github.com/JuliaFolds/Transducers.jl/pull/243> (Update */Manifest.toml)

# Judge result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmarks:
    - Target: 29 Jul 2021 - 01:14
    - Baseline: 29 Jul 2021 - 01:20
* Package commits:
    - Target: c69c5b
    - Baseline: 9ac175
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
| `["findfirst", "n=1000", "reduce", "basesize=256"]` |                1.09 (5%) :x: |                1.02 (1%) :x: |
| `["findfirst", "n=1000", "reduce", "basesize=512"]` | 0.91 (5%) :white_check_mark: | 0.91 (1%) :white_check_mark: |
| `["findfirst", "n=400", "foldl"]`                   |                1.05 (5%) :x: |                   1.00 (1%)  |
| `["findfirst", "n=400", "reduce", "basesize=128"]`  |                   1.02 (5%)  | 0.98 (1%) :white_check_mark: |
| `["findfirst", "n=400", "reduce", "basesize=256"]`  |                   1.02 (5%)  |                1.02 (1%) :x: |
| `["findfirst", "n=400", "reduce", "basesize=512"]`  |                   1.02 (5%)  | 0.98 (1%) :white_check_mark: |
| `["findfirst", "n=500", "reduce", "basesize=128"]`  |                1.07 (5%) :x: |                1.04 (1%) :x: |
| `["findfirst", "n=500", "reduce", "basesize=256"]`  |                1.26 (5%) :x: |                1.09 (1%) :x: |
| `["findfirst", "n=500", "reduce", "basesize=512"]`  |                2.28 (5%) :x: |                1.80 (1%) :x: |
| `["overhead", "stoppable=true"]`                    | 0.94 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["splitby", "count", "man"]`                       |                1.12 (5%) :x: |                   1.00 (1%)  |
| `["splitby", "count", "reduce"]`                    |                   1.00 (5%)  | 0.98 (1%) :white_check_mark: |
| `["words", "nthreads=1"]`                           | 0.94 (5%) :white_check_mark: |                   0.99 (1%)  |

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
  uname: Linux 5.8.0-1036-azure #38~20.04.1-Ubuntu SMP Thu Jun 17 14:14:18 UTC 2021 x86_64 x86_64
  CPU: Intel(R) Xeon(R) CPU E5-2673 v3 @ 2.40GHz: 
              speed         user         nice          sys         idle          irq
       #1  2394 MHz      64256 s         16 s       2125 s      37965 s          0 s
       #2  2394 MHz      46268 s         10 s       2327 s      56298 s          0 s
       
  Memory: 6.790924072265625 GB (3330.71484375 MB free)
  Uptime: 1055.0 sec
  Load Avg:  1.69873046875  1.50146484375  0.91845703125
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
  uname: Linux 5.8.0-1036-azure #38~20.04.1-Ubuntu SMP Thu Jun 17 14:14:18 UTC 2021 x86_64 x86_64
  CPU: Intel(R) Xeon(R) CPU E5-2673 v3 @ 2.40GHz: 
              speed         user         nice          sys         idle          irq
       #1  2394 MHz      84225 s         16 s       2638 s      51539 s          0 s
       #2  2394 MHz      77293 s         10 s       2881 s      58664 s          0 s
       
  Memory: 6.790924072265625 GB (3369.359375 MB free)
  Uptime: 1396.0 sec
  Load Avg:  1.646484375  1.54736328125  1.11767578125
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-9.0.1 (ORCJIT, haswell)
```

---
# Target result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmark: 29 Jul 2021 - 1:14
* Package commit: c69c5b
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

| ID                                                  | time            | GC time  | memory           | allocations |
|-----------------------------------------------------|----------------:|---------:|-----------------:|------------:|
| `["collect", "assoc", "basesize=1"]`                | 288.550 ms (5%) |          |   32.66 MiB (1%) |      286757 |
| `["collect", "assoc", "basesize=1024"]`             | 238.503 ms (5%) |          |    1.79 MiB (1%) |         570 |
| `["collect", "assoc", "basesize=32"]`               | 244.184 ms (5%) |          |    3.97 MiB (1%) |       13305 |
| `["collect", "seq"]`                                | 472.526 ms (5%) |          |  512.72 KiB (1%) |          15 |
| `["collect", "unordered", "basesize=1"]`            | 483.364 ms (5%) | 8.297 ms |   30.02 MiB (1%) |      360772 |
| `["collect", "unordered", "basesize=1024"]`         | 341.288 ms (5%) |          |  927.27 KiB (1%) |        6412 |
| `["collect", "unordered", "basesize=32"]`           | 265.871 ms (5%) |          |    1.47 MiB (1%) |       12378 |
| `["findfirst", "n=1000", "foldl"]`                  | 713.694 ms (5%) |          |                  |             |
| `["findfirst", "n=1000", "reduce", "basesize=128"]` | 800.039 ms (5%) |          |    1.25 MiB (1%) |       22437 |
| `["findfirst", "n=1000", "reduce", "basesize=256"]` | 527.899 ms (5%) |          |  494.53 KiB (1%) |        8674 |
| `["findfirst", "n=1000", "reduce", "basesize=512"]` | 658.993 ms (5%) |          |  319.84 KiB (1%) |        5614 |
| `["findfirst", "n=400", "foldl"]`                   | 529.593 ms (5%) |          |                  |             |
| `["findfirst", "n=400", "reduce", "basesize=128"]`  | 290.443 ms (5%) |          |    1.10 MiB (1%) |       19750 |
| `["findfirst", "n=400", "reduce", "basesize=256"]`  | 301.591 ms (5%) |          |  600.13 KiB (1%) |       10586 |
| `["findfirst", "n=400", "reduce", "basesize=512"]`  | 319.482 ms (5%) |          |  352.81 KiB (1%) |        6221 |
| `["findfirst", "n=500", "foldl"]`                   |  89.832 ms (5%) |          |                  |             |
| `["findfirst", "n=500", "reduce", "basesize=128"]`  | 207.938 ms (5%) |          |  785.02 KiB (1%) |       13690 |
| `["findfirst", "n=500", "reduce", "basesize=256"]`  | 197.919 ms (5%) |          |  419.61 KiB (1%) |        7331 |
| `["findfirst", "n=500", "reduce", "basesize=512"]`  | 323.719 ms (5%) |          |  355.94 KiB (1%) |        6217 |
| `["overhead", "default"]`                           |  56.901 μs (5%) |          |   47.36 KiB (1%) |         382 |
| `["overhead", "stoppable=false"]`                   |  55.501 μs (5%) |          |   47.36 KiB (1%) |         381 |
| `["overhead", "stoppable=true"]`                    | 153.502 μs (5%) |          |  139.67 KiB (1%) |        2464 |
| `["parallel_histogram", "assoc", "basesize=16384"]` |   4.455 ms (5%) |          |  730.06 KiB (1%) |          57 |
| `["parallel_histogram", "assoc", "basesize=4096"]`  |   5.314 ms (5%) |          |    1.79 MiB (1%) |         213 |
| `["parallel_histogram", "assoc", "basesize=8192"]`  |   4.804 ms (5%) |          |    1.43 MiB (1%) |         117 |
| `["parallel_histogram", "comm", "basesize=16384"]`  |  12.219 ms (5%) |          |    1.22 MiB (1%) |         160 |
| `["parallel_histogram", "comm", "basesize=4096"]`   |  18.144 ms (5%) |          | 1019.78 KiB (1%) |         302 |
| `["parallel_histogram", "comm", "basesize=8192"]`   |  14.206 ms (5%) |          |    1.22 MiB (1%) |         261 |
| `["parallel_histogram", "seq"]`                     |   7.893 ms (5%) |          |  364.61 KiB (1%) |          24 |
| `["partition_length_maximum", "rand", "foldl"]`     |  59.155 ms (5%) |          |                  |             |
| `["partition_length_maximum", "rand", "reduce"]`    |  30.921 ms (5%) |          |    2.66 KiB (1%) |          48 |
| `["splitby", "count", "foldl"]`                     |   4.236 ms (5%) |          |    96 bytes (1%) |           4 |
| `["splitby", "count", "man"]`                       |   1.773 ms (5%) |          |                  |             |
| `["splitby", "count", "reduce"]`                    | 878.510 μs (5%) |          |    2.83 KiB (1%) |          55 |
| `["sum", "random", "foldl"]`                        |  17.438 ms (5%) |          |    32 bytes (1%) |           2 |
| `["sum", "random", "reduce", "basesize=128"]`       |   9.032 ms (5%) |          |  103.23 KiB (1%) |        1018 |
| `["sum", "random", "reduce", "basesize=256"]`       |   9.301 ms (5%) |          |   51.23 KiB (1%) |         506 |
| `["sum", "random", "reduce", "basesize=512"]`       |   9.123 ms (5%) |          |   25.30 KiB (1%) |         252 |
| `["sum", "uniform", "foldl"]`                       |  16.550 ms (5%) |          |    32 bytes (1%) |           2 |
| `["sum", "uniform", "reduce", "basesize=128"]`      |   8.829 ms (5%) |          |  103.23 KiB (1%) |        1018 |
| `["sum", "uniform", "reduce", "basesize=256"]`      |   8.625 ms (5%) |          |   51.23 KiB (1%) |         506 |
| `["sum", "uniform", "reduce", "basesize=512"]`      |   8.479 ms (5%) |          |   25.25 KiB (1%) |         251 |
| `["sum", "valley", "foldl"]`                        |  17.248 ms (5%) |          |    32 bytes (1%) |           2 |
| `["sum", "valley", "reduce", "basesize=128"]`       |   9.068 ms (5%) |          |  103.23 KiB (1%) |        1018 |
| `["sum", "valley", "reduce", "basesize=256"]`       |   9.045 ms (5%) |          |   51.23 KiB (1%) |         506 |
| `["sum", "valley", "reduce", "basesize=512"]`       |   8.832 ms (5%) |          |   25.25 KiB (1%) |         251 |
| `["words", "nthreads=1"]`                           |  24.050 ms (5%) |          |   31.55 MiB (1%) |     1028458 |
| `["words", "nthreads=2"]`                           |  14.431 ms (5%) |          |   31.91 MiB (1%) |     1028494 |
| `["words", "nthreads=4"]`                           |  15.439 ms (5%) |          |   32.81 MiB (1%) |     1028673 |

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
  uname: Linux 5.8.0-1036-azure #38~20.04.1-Ubuntu SMP Thu Jun 17 14:14:18 UTC 2021 x86_64 x86_64
  CPU: Intel(R) Xeon(R) CPU E5-2673 v3 @ 2.40GHz: 
              speed         user         nice          sys         idle          irq
       #1  2394 MHz      64256 s         16 s       2125 s      37965 s          0 s
       #2  2394 MHz      46268 s         10 s       2327 s      56298 s          0 s
       
  Memory: 6.790924072265625 GB (3330.71484375 MB free)
  Uptime: 1055.0 sec
  Load Avg:  1.69873046875  1.50146484375  0.91845703125
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-9.0.1 (ORCJIT, haswell)
```

---
# Baseline result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmark: 29 Jul 2021 - 1:20
* Package commit: 9ac175
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
| `["collect", "assoc", "basesize=1"]`                | 288.803 ms (5%) |         |  32.66 MiB (1%) |      286759 |
| `["collect", "assoc", "basesize=1024"]`             | 238.973 ms (5%) |         |   1.79 MiB (1%) |         570 |
| `["collect", "assoc", "basesize=32"]`               | 248.401 ms (5%) |         |   3.97 MiB (1%) |       13306 |
| `["collect", "seq"]`                                | 463.569 ms (5%) |         | 512.72 KiB (1%) |          15 |
| `["collect", "unordered", "basesize=1"]`            | 508.789 ms (5%) |         |  30.01 MiB (1%) |      360677 |
| `["collect", "unordered", "basesize=1024"]`         | 346.198 ms (5%) |         | 926.64 KiB (1%) |        6392 |
| `["collect", "unordered", "basesize=32"]`           | 264.131 ms (5%) |         |   1.48 MiB (1%) |       12742 |
| `["findfirst", "n=1000", "foldl"]`                  | 680.669 ms (5%) |         |                 |             |
| `["findfirst", "n=1000", "reduce", "basesize=128"]` | 779.660 ms (5%) |         |   1.25 MiB (1%) |       22429 |
| `["findfirst", "n=1000", "reduce", "basesize=256"]` | 485.655 ms (5%) |         | 484.92 KiB (1%) |        8491 |
| `["findfirst", "n=1000", "reduce", "basesize=512"]` | 722.463 ms (5%) |         | 349.95 KiB (1%) |        6148 |
| `["findfirst", "n=400", "foldl"]`                   | 504.200 ms (5%) |         |                 |             |
| `["findfirst", "n=400", "reduce", "basesize=128"]`  | 283.623 ms (5%) |         |   1.12 MiB (1%) |       20134 |
| `["findfirst", "n=400", "reduce", "basesize=256"]`  | 294.788 ms (5%) |         | 590.77 KiB (1%) |       10418 |
| `["findfirst", "n=400", "reduce", "basesize=512"]`  | 314.711 ms (5%) |         | 359.78 KiB (1%) |        6344 |
| `["findfirst", "n=500", "foldl"]`                   |  86.887 ms (5%) |         |                 |             |
| `["findfirst", "n=500", "reduce", "basesize=128"]`  | 194.695 ms (5%) |         | 757.14 KiB (1%) |       13187 |
| `["findfirst", "n=500", "reduce", "basesize=256"]`  | 157.164 ms (5%) |         | 386.47 KiB (1%) |        6716 |
| `["findfirst", "n=500", "reduce", "basesize=512"]`  | 142.204 ms (5%) |         | 197.34 KiB (1%) |        3455 |
| `["overhead", "default"]`                           |  57.900 μs (5%) |         |  47.36 KiB (1%) |         382 |
| `["overhead", "stoppable=false"]`                   |  56.900 μs (5%) |         |  47.39 KiB (1%) |         382 |
| `["overhead", "stoppable=true"]`                    | 163.802 μs (5%) |         | 139.67 KiB (1%) |        2464 |
| `["parallel_histogram", "assoc", "basesize=16384"]` |   4.484 ms (5%) |         | 730.06 KiB (1%) |          57 |
| `["parallel_histogram", "assoc", "basesize=4096"]`  |   5.217 ms (5%) |         |   1.79 MiB (1%) |         213 |
| `["parallel_histogram", "assoc", "basesize=8192"]`  |   4.834 ms (5%) |         |   1.43 MiB (1%) |         117 |
| `["parallel_histogram", "comm", "basesize=16384"]`  |  12.520 ms (5%) |         |   1.22 MiB (1%) |         192 |
| `["parallel_histogram", "comm", "basesize=4096"]`   |  18.979 ms (5%) |         |   1.00 MiB (1%) |        1133 |
| `["parallel_histogram", "comm", "basesize=8192"]`   |  14.524 ms (5%) |         |   1.23 MiB (1%) |         432 |
| `["parallel_histogram", "seq"]`                     |   7.849 ms (5%) |         | 364.61 KiB (1%) |          24 |
| `["partition_length_maximum", "rand", "foldl"]`     |  59.049 ms (5%) |         |                 |             |
| `["partition_length_maximum", "rand", "reduce"]`    |  30.433 ms (5%) |         |   2.66 KiB (1%) |          48 |
| `["splitby", "count", "foldl"]`                     |   4.249 ms (5%) |         |   96 bytes (1%) |           4 |
| `["splitby", "count", "man"]`                       |   1.585 ms (5%) |         |                 |             |
| `["splitby", "count", "reduce"]`                    | 878.309 μs (5%) |         |   2.88 KiB (1%) |          55 |
| `["sum", "random", "foldl"]`                        |  17.109 ms (5%) |         |   32 bytes (1%) |           2 |
| `["sum", "random", "reduce", "basesize=128"]`       |   9.050 ms (5%) |         | 103.23 KiB (1%) |        1018 |
| `["sum", "random", "reduce", "basesize=256"]`       |   8.907 ms (5%) |         |  51.23 KiB (1%) |         506 |
| `["sum", "random", "reduce", "basesize=512"]`       |   8.892 ms (5%) |         |  25.30 KiB (1%) |         252 |
| `["sum", "uniform", "foldl"]`                       |  16.758 ms (5%) |         |   32 bytes (1%) |           2 |
| `["sum", "uniform", "reduce", "basesize=128"]`      |   8.818 ms (5%) |         | 103.23 KiB (1%) |        1018 |
| `["sum", "uniform", "reduce", "basesize=256"]`      |   8.643 ms (5%) |         |  51.23 KiB (1%) |         506 |
| `["sum", "uniform", "reduce", "basesize=512"]`      |   8.566 ms (5%) |         |  25.25 KiB (1%) |         251 |
| `["sum", "valley", "foldl"]`                        |  17.288 ms (5%) |         |   32 bytes (1%) |           2 |
| `["sum", "valley", "reduce", "basesize=128"]`       |   9.056 ms (5%) |         | 103.23 KiB (1%) |        1018 |
| `["sum", "valley", "reduce", "basesize=256"]`       |   8.990 ms (5%) |         |  51.23 KiB (1%) |         506 |
| `["sum", "valley", "reduce", "basesize=512"]`       |   8.983 ms (5%) |         |  25.25 KiB (1%) |         251 |
| `["words", "nthreads=1"]`                           |  25.557 ms (5%) |         |  31.86 MiB (1%) |     1038068 |
| `["words", "nthreads=2"]`                           |  15.094 ms (5%) |         |  32.22 MiB (1%) |     1038106 |
| `["words", "nthreads=4"]`                           |  15.421 ms (5%) |         |  32.93 MiB (1%) |     1038227 |

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
  uname: Linux 5.8.0-1036-azure #38~20.04.1-Ubuntu SMP Thu Jun 17 14:14:18 UTC 2021 x86_64 x86_64
  CPU: Intel(R) Xeon(R) CPU E5-2673 v3 @ 2.40GHz: 
              speed         user         nice          sys         idle          irq
       #1  2394 MHz      84225 s         16 s       2638 s      51539 s          0 s
       #2  2394 MHz      77293 s         10 s       2881 s      58664 s          0 s
       
  Memory: 6.790924072265625 GB (3369.359375 MB free)
  Uptime: 1396.0 sec
  Load Avg:  1.646484375  1.54736328125  1.11767578125
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
    CPU MHz:                         2394.454
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

