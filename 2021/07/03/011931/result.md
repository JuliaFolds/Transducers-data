# Multi-thread benchmark result

* Pull request commit: [`2079048f70b20b9658ef0cc025e801a2a4d590a9`](https://github.com/JuliaFolds/Transducers.jl/commit/2079048f70b20b9658ef0cc025e801a2a4d590a9)
* Pull request: <https://github.com/JuliaFolds/Transducers.jl/pull/243> (Update */Manifest.toml)

# Judge result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmarks:
    - Target: 3 Jul 2021 - 01:13
    - Baseline: 3 Jul 2021 - 01:18
* Package commits:
    - Target: 7fb4aa
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
| `["collect", "assoc", "basesize=1024"]`             | 0.94 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["collect", "unordered", "basesize=1"]`            | 0.92 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["collect", "unordered", "basesize=1024"]`         |                1.07 (5%) :x: |                1.06 (1%) :x: |
| `["collect", "unordered", "basesize=32"]`           | 0.94 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["findfirst", "n=1000", "reduce", "basesize=128"]` | 0.91 (5%) :white_check_mark: |                1.04 (1%) :x: |
| `["findfirst", "n=1000", "reduce", "basesize=256"]` |                   1.05 (5%)  |                1.07 (1%) :x: |
| `["findfirst", "n=1000", "reduce", "basesize=512"]` | 0.90 (5%) :white_check_mark: | 0.97 (1%) :white_check_mark: |
| `["findfirst", "n=400", "reduce", "basesize=128"]`  |                   0.97 (5%)  | 0.97 (1%) :white_check_mark: |
| `["findfirst", "n=400", "reduce", "basesize=256"]`  |                1.07 (5%) :x: | 0.97 (1%) :white_check_mark: |
| `["findfirst", "n=400", "reduce", "basesize=512"]`  |                   1.03 (5%)  | 0.98 (1%) :white_check_mark: |
| `["findfirst", "n=500", "reduce", "basesize=128"]`  |                1.95 (5%) :x: |                1.86 (1%) :x: |
| `["findfirst", "n=500", "reduce", "basesize=256"]`  |                1.45 (5%) :x: |                1.15 (1%) :x: |
| `["findfirst", "n=500", "reduce", "basesize=512"]`  | 0.57 (5%) :white_check_mark: | 0.71 (1%) :white_check_mark: |
| `["overhead", "stoppable=false"]`                   |                1.05 (5%) :x: |                   1.00 (1%)  |
| `["parallel_histogram", "assoc", "basesize=8192"]`  |                1.06 (5%) :x: |                   1.00 (1%)  |
| `["parallel_histogram", "comm", "basesize=4096"]`   |                1.10 (5%) :x: |                1.02 (1%) :x: |
| `["parallel_histogram", "comm", "basesize=8192"]`   | 0.81 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["partition_length_maximum", "rand", "reduce"]`    | 0.94 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["splitby", "count", "man"]`                       |                1.09 (5%) :x: |                   1.00 (1%)  |
| `["sum", "random", "reduce", "basesize=128"]`       |                1.05 (5%) :x: |                   1.00 (1%)  |
| `["sum", "random", "reduce", "basesize=256"]`       | 0.94 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["words", "nthreads=2"]`                           |                1.11 (5%) :x: |                   1.00 (1%)  |

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
  CPU: Intel(R) Xeon(R) CPU E5-2673 v4 @ 2.30GHz: 
              speed         user         nice          sys         idle          irq
       #1  2294 MHz      53722 s          8 s       2382 s      31524 s          0 s
       #2  2294 MHz      55928 s         16 s       2384 s      29485 s          0 s
       
  Memory: 6.790924072265625 GB (3700.6640625 MB free)
  Uptime: 886.0 sec
  Load Avg:  1.56787109375  1.4609375  0.9140625
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-9.0.1 (ORCJIT, broadwell)
```

### Baseline
```
Julia Version 1.5.4
Commit 69fcb5745b (2021-03-11 19:13 UTC)
Platform Info:
  OS: Linux (x86_64-pc-linux-gnu)
      Ubuntu 20.04.2 LTS
  uname: Linux 5.8.0-1036-azure #38~20.04.1-Ubuntu SMP Thu Jun 17 14:14:18 UTC 2021 x86_64 x86_64
  CPU: Intel(R) Xeon(R) CPU E5-2673 v4 @ 2.30GHz: 
              speed         user         nice          sys         idle          irq
       #1  2294 MHz      78642 s          8 s       3039 s      40550 s          0 s
       #2  2294 MHz      82130 s         16 s       3022 s      37126 s          0 s
       
  Memory: 6.790924072265625 GB (3726.80078125 MB free)
  Uptime: 1233.0 sec
  Load Avg:  1.54248046875  1.533203125  1.11865234375
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-9.0.1 (ORCJIT, broadwell)
```

---
# Target result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmark: 3 Jul 2021 - 1:13
* Package commit: 7fb4aa
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
| `["collect", "assoc", "basesize=1"]`                | 229.485 ms (5%) |         |  32.66 MiB (1%) |      286770 |
| `["collect", "assoc", "basesize=1024"]`             | 160.640 ms (5%) |         |   1.79 MiB (1%) |         570 |
| `["collect", "assoc", "basesize=32"]`               | 163.185 ms (5%) |         |   3.97 MiB (1%) |       13305 |
| `["collect", "seq"]`                                | 316.781 ms (5%) |         | 512.72 KiB (1%) |          15 |
| `["collect", "unordered", "basesize=1"]`            | 412.297 ms (5%) |         |  30.01 MiB (1%) |      360632 |
| `["collect", "unordered", "basesize=1024"]`         | 236.106 ms (5%) |         | 831.14 KiB (1%) |        3336 |
| `["collect", "unordered", "basesize=32"]`           | 197.283 ms (5%) |         |   1.47 MiB (1%) |       12627 |
| `["findfirst", "n=1000", "foldl"]`                  | 536.175 ms (5%) |         |                 |             |
| `["findfirst", "n=1000", "reduce", "basesize=128"]` | 340.751 ms (5%) |         | 781.61 KiB (1%) |       13674 |
| `["findfirst", "n=1000", "reduce", "basesize=256"]` | 414.595 ms (5%) |         | 484.97 KiB (1%) |        8496 |
| `["findfirst", "n=1000", "reduce", "basesize=512"]` | 493.340 ms (5%) |         | 319.80 KiB (1%) |        5612 |
| `["findfirst", "n=400", "foldl"]`                   | 394.637 ms (5%) |         |                 |             |
| `["findfirst", "n=400", "reduce", "basesize=128"]`  | 235.269 ms (5%) |         |   1.13 MiB (1%) |       20277 |
| `["findfirst", "n=400", "reduce", "basesize=256"]`  | 234.347 ms (5%) |         | 574.55 KiB (1%) |       10132 |
| `["findfirst", "n=400", "reduce", "basesize=512"]`  | 248.097 ms (5%) |         | 343.69 KiB (1%) |        6065 |
| `["findfirst", "n=500", "foldl"]`                   |  63.174 ms (5%) |         |                 |             |
| `["findfirst", "n=500", "reduce", "basesize=128"]`  | 143.865 ms (5%) |         | 742.59 KiB (1%) |       12933 |
| `["findfirst", "n=500", "reduce", "basesize=256"]`  | 151.616 ms (5%) |         | 407.89 KiB (1%) |        7115 |
| `["findfirst", "n=500", "reduce", "basesize=512"]`  | 119.770 ms (5%) |         | 210.89 KiB (1%) |        3671 |
| `["overhead", "default"]`                           |  59.601 μs (5%) |         |  47.36 KiB (1%) |         382 |
| `["overhead", "stoppable=false"]`                   |  57.701 μs (5%) |         |  47.36 KiB (1%) |         381 |
| `["overhead", "stoppable=true"]`                    | 145.901 μs (5%) |         | 139.67 KiB (1%) |        2464 |
| `["parallel_histogram", "assoc", "basesize=16384"]` |   3.154 ms (5%) |         | 730.06 KiB (1%) |          57 |
| `["parallel_histogram", "assoc", "basesize=4096"]`  |   3.845 ms (5%) |         |   1.79 MiB (1%) |         213 |
| `["parallel_histogram", "assoc", "basesize=8192"]`  |   3.589 ms (5%) |         |   1.43 MiB (1%) |         117 |
| `["parallel_histogram", "comm", "basesize=16384"]`  |  14.222 ms (5%) |         |   1.01 MiB (1%) |         571 |
| `["parallel_histogram", "comm", "basesize=4096"]`   |  21.354 ms (5%) |         |   1.02 MiB (1%) |        1679 |
| `["parallel_histogram", "comm", "basesize=8192"]`   |  14.212 ms (5%) |         |   1.24 MiB (1%) |         668 |
| `["parallel_histogram", "seq"]`                     |   5.526 ms (5%) |         | 364.61 KiB (1%) |          24 |
| `["partition_length_maximum", "rand", "foldl"]`     |  31.016 ms (5%) |         |                 |             |
| `["partition_length_maximum", "rand", "reduce"]`    |  14.966 ms (5%) |         |   2.66 KiB (1%) |          48 |
| `["splitby", "count", "foldl"]`                     |   3.477 ms (5%) |         |   96 bytes (1%) |           4 |
| `["splitby", "count", "man"]`                       |   1.498 ms (5%) |         |                 |             |
| `["splitby", "count", "reduce"]`                    | 745.306 μs (5%) |         |   2.84 KiB (1%) |          54 |
| `["sum", "random", "foldl"]`                        |  11.797 ms (5%) |         |   32 bytes (1%) |           2 |
| `["sum", "random", "reduce", "basesize=128"]`       |   6.255 ms (5%) |         | 103.23 KiB (1%) |        1018 |
| `["sum", "random", "reduce", "basesize=256"]`       |   5.767 ms (5%) |         |  51.23 KiB (1%) |         506 |
| `["sum", "random", "reduce", "basesize=512"]`       |   6.017 ms (5%) |         |  25.30 KiB (1%) |         252 |
| `["sum", "uniform", "foldl"]`                       |  11.283 ms (5%) |         |   32 bytes (1%) |           2 |
| `["sum", "uniform", "reduce", "basesize=128"]`      |   5.949 ms (5%) |         | 103.23 KiB (1%) |        1018 |
| `["sum", "uniform", "reduce", "basesize=256"]`      |   5.610 ms (5%) |         |  51.23 KiB (1%) |         506 |
| `["sum", "uniform", "reduce", "basesize=512"]`      |   5.651 ms (5%) |         |  25.25 KiB (1%) |         251 |
| `["sum", "valley", "foldl"]`                        |  11.608 ms (5%) |         |   32 bytes (1%) |           2 |
| `["sum", "valley", "reduce", "basesize=128"]`       |   6.081 ms (5%) |         | 103.23 KiB (1%) |        1018 |
| `["sum", "valley", "reduce", "basesize=256"]`       |   5.812 ms (5%) |         |  51.23 KiB (1%) |         506 |
| `["sum", "valley", "reduce", "basesize=512"]`       |   5.826 ms (5%) |         |  25.25 KiB (1%) |         251 |
| `["words", "nthreads=1"]`                           |  21.752 ms (5%) |         |  31.49 MiB (1%) |     1025867 |
| `["words", "nthreads=2"]`                           |  15.619 ms (5%) |         |  32.20 MiB (1%) |     1025949 |
| `["words", "nthreads=4"]`                           |  14.648 ms (5%) |         |  32.65 MiB (1%) |     1026027 |

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
  CPU: Intel(R) Xeon(R) CPU E5-2673 v4 @ 2.30GHz: 
              speed         user         nice          sys         idle          irq
       #1  2294 MHz      53722 s          8 s       2382 s      31524 s          0 s
       #2  2294 MHz      55928 s         16 s       2384 s      29485 s          0 s
       
  Memory: 6.790924072265625 GB (3700.6640625 MB free)
  Uptime: 886.0 sec
  Load Avg:  1.56787109375  1.4609375  0.9140625
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-9.0.1 (ORCJIT, broadwell)
```

---
# Baseline result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmark: 3 Jul 2021 - 1:18
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
| `["collect", "assoc", "basesize=1"]`                | 227.445 ms (5%) |         |  32.66 MiB (1%) |      286769 |
| `["collect", "assoc", "basesize=1024"]`             | 171.318 ms (5%) |         |   1.79 MiB (1%) |         570 |
| `["collect", "assoc", "basesize=32"]`               | 163.494 ms (5%) |         |   3.97 MiB (1%) |       13305 |
| `["collect", "seq"]`                                | 302.990 ms (5%) |         | 512.72 KiB (1%) |          15 |
| `["collect", "unordered", "basesize=1"]`            | 449.748 ms (5%) |         |  30.01 MiB (1%) |      360654 |
| `["collect", "unordered", "basesize=1024"]`         | 221.442 ms (5%) |         | 783.80 KiB (1%) |        1821 |
| `["collect", "unordered", "basesize=32"]`           | 209.928 ms (5%) |         |   1.48 MiB (1%) |       12761 |
| `["findfirst", "n=1000", "foldl"]`                  | 528.361 ms (5%) |         |                 |             |
| `["findfirst", "n=1000", "reduce", "basesize=128"]` | 375.489 ms (5%) |         | 749.77 KiB (1%) |       13144 |
| `["findfirst", "n=1000", "reduce", "basesize=256"]` | 395.597 ms (5%) |         | 454.98 KiB (1%) |        7975 |
| `["findfirst", "n=1000", "reduce", "basesize=512"]` | 545.736 ms (5%) |         | 328.97 KiB (1%) |        5773 |
| `["findfirst", "n=400", "foldl"]`                   | 400.647 ms (5%) |         |                 |             |
| `["findfirst", "n=400", "reduce", "basesize=128"]`  | 241.446 ms (5%) |         |   1.16 MiB (1%) |       20821 |
| `["findfirst", "n=400", "reduce", "basesize=256"]`  | 218.116 ms (5%) |         | 593.33 KiB (1%) |       10473 |
| `["findfirst", "n=400", "reduce", "basesize=512"]`  | 241.392 ms (5%) |         | 350.56 KiB (1%) |        6183 |
| `["findfirst", "n=500", "foldl"]`                   |  62.235 ms (5%) |         |                 |             |
| `["findfirst", "n=500", "reduce", "basesize=128"]`  |  73.685 ms (5%) |         | 399.77 KiB (1%) |        6962 |
| `["findfirst", "n=500", "reduce", "basesize=256"]`  | 104.272 ms (5%) |         | 354.61 KiB (1%) |        6176 |
| `["findfirst", "n=500", "reduce", "basesize=512"]`  | 210.055 ms (5%) |         | 295.98 KiB (1%) |        5163 |
| `["overhead", "default"]`                           |  58.501 μs (5%) |         |  47.36 KiB (1%) |         382 |
| `["overhead", "stoppable=false"]`                   |  54.900 μs (5%) |         |  47.36 KiB (1%) |         381 |
| `["overhead", "stoppable=true"]`                    | 145.501 μs (5%) |         | 139.67 KiB (1%) |        2464 |
| `["parallel_histogram", "assoc", "basesize=16384"]` |   3.071 ms (5%) |         | 730.06 KiB (1%) |          57 |
| `["parallel_histogram", "assoc", "basesize=4096"]`  |   3.890 ms (5%) |         |   1.79 MiB (1%) |         213 |
| `["parallel_histogram", "assoc", "basesize=8192"]`  |   3.400 ms (5%) |         |   1.43 MiB (1%) |         117 |
| `["parallel_histogram", "comm", "basesize=16384"]`  |  14.593 ms (5%) |         |   1.02 MiB (1%) |         310 |
| `["parallel_histogram", "comm", "basesize=4096"]`   |  19.328 ms (5%) |         |   1.00 MiB (1%) |        1127 |
| `["parallel_histogram", "comm", "basesize=8192"]`   |  17.452 ms (5%) |         |   1.23 MiB (1%) |         525 |
| `["parallel_histogram", "seq"]`                     |   5.540 ms (5%) |         | 364.61 KiB (1%) |          24 |
| `["partition_length_maximum", "rand", "foldl"]`     |  32.177 ms (5%) |         |                 |             |
| `["partition_length_maximum", "rand", "reduce"]`    |  16.003 ms (5%) |         |   2.66 KiB (1%) |          48 |
| `["splitby", "count", "foldl"]`                     |   3.483 ms (5%) |         |   96 bytes (1%) |           4 |
| `["splitby", "count", "man"]`                       |   1.378 ms (5%) |         |                 |             |
| `["splitby", "count", "reduce"]`                    | 744.806 μs (5%) |         |   2.84 KiB (1%) |          54 |
| `["sum", "random", "foldl"]`                        |  12.188 ms (5%) |         |   32 bytes (1%) |           2 |
| `["sum", "random", "reduce", "basesize=128"]`       |   5.938 ms (5%) |         | 103.23 KiB (1%) |        1018 |
| `["sum", "random", "reduce", "basesize=256"]`       |   6.142 ms (5%) |         |  51.23 KiB (1%) |         506 |
| `["sum", "random", "reduce", "basesize=512"]`       |   5.856 ms (5%) |         |  25.30 KiB (1%) |         252 |
| `["sum", "uniform", "foldl"]`                       |  11.446 ms (5%) |         |   32 bytes (1%) |           2 |
| `["sum", "uniform", "reduce", "basesize=128"]`      |   6.049 ms (5%) |         | 103.23 KiB (1%) |        1018 |
| `["sum", "uniform", "reduce", "basesize=256"]`      |   5.712 ms (5%) |         |  51.23 KiB (1%) |         506 |
| `["sum", "uniform", "reduce", "basesize=512"]`      |   5.803 ms (5%) |         |  25.25 KiB (1%) |         251 |
| `["sum", "valley", "foldl"]`                        |  11.613 ms (5%) |         |   32 bytes (1%) |           2 |
| `["sum", "valley", "reduce", "basesize=128"]`       |   5.969 ms (5%) |         | 103.23 KiB (1%) |        1018 |
| `["sum", "valley", "reduce", "basesize=256"]`       |   5.975 ms (5%) |         |  51.23 KiB (1%) |         506 |
| `["sum", "valley", "reduce", "basesize=512"]`       |   5.953 ms (5%) |         |  25.25 KiB (1%) |         251 |
| `["words", "nthreads=1"]`                           |  21.941 ms (5%) |         |  31.56 MiB (1%) |     1027775 |
| `["words", "nthreads=2"]`                           |  14.055 ms (5%) |         |  32.27 MiB (1%) |     1027872 |
| `["words", "nthreads=4"]`                           |  15.331 ms (5%) |         |  32.91 MiB (1%) |     1028043 |

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
  CPU: Intel(R) Xeon(R) CPU E5-2673 v4 @ 2.30GHz: 
              speed         user         nice          sys         idle          irq
       #1  2294 MHz      78642 s          8 s       3039 s      40550 s          0 s
       #2  2294 MHz      82130 s         16 s       3022 s      37126 s          0 s
       
  Memory: 6.790924072265625 GB (3726.80078125 MB free)
  Uptime: 1233.0 sec
  Load Avg:  1.54248046875  1.533203125  1.11865234375
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-9.0.1 (ORCJIT, broadwell)
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
    Model:                           79
    Model name:                      Intel(R) Xeon(R) CPU E5-2673 v4 @ 2.30GHz
    Stepping:                        1
    CPU MHz:                         2294.685
    BogoMIPS:                        4589.37
    Hypervisor vendor:               Microsoft
    Virtualization type:             full
    L1d cache:                       64 KiB
    L1i cache:                       64 KiB
    L2 cache:                        512 KiB
    L3 cache:                        50 MiB
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
    Flags:                           fpu vme de pse tsc msr pae mce cx8 apic sep mtrr pge mca cmov pat pse36 clflush mmx fxsr sse sse2 ss ht syscall nx pdpe1gb rdtscp lm constant_tsc rep_good nopl xtopology cpuid pni pclmulqdq ssse3 fma cx16 pcid sse4_1 sse4_2 movbe popcnt aes xsave avx f16c rdrand hypervisor lahf_lm abm 3dnowprefetch invpcid_single pti fsgsbase bmi1 hle avx2 smep bmi2 erms invpcid rtm rdseed adx smap xsaveopt md_clear
    

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

