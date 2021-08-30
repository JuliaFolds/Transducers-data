# Multi-thread benchmark result

* Pull request commit: [`703c77f68ce1fdea1927d7794f6cee0daba8de48`](https://github.com/JuliaFolds/Transducers.jl/commit/703c77f68ce1fdea1927d7794f6cee0daba8de48)
* Pull request: <https://github.com/JuliaFolds/Transducers.jl/pull/243> (Update */Manifest.toml)

# Judge result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmarks:
    - Target: 30 Aug 2021 - 01:15
    - Baseline: 30 Aug 2021 - 01:21
* Package commits:
    - Target: f9e741
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
| `["collect", "unordered", "basesize=1024"]`         | 0.82 (5%) :white_check_mark: | 0.85 (1%) :white_check_mark: |
| `["findfirst", "n=1000", "reduce", "basesize=128"]` |                   0.99 (5%)  |                1.02 (1%) :x: |
| `["findfirst", "n=1000", "reduce", "basesize=512"]` | 0.91 (5%) :white_check_mark: | 0.90 (1%) :white_check_mark: |
| `["findfirst", "n=400", "reduce", "basesize=128"]`  |                   1.02 (5%)  |                1.04 (1%) :x: |
| `["findfirst", "n=500", "reduce", "basesize=128"]`  |                1.17 (5%) :x: |                1.07 (1%) :x: |
| `["findfirst", "n=500", "reduce", "basesize=256"]`  | 0.92 (5%) :white_check_mark: |                1.12 (1%) :x: |
| `["findfirst", "n=500", "reduce", "basesize=512"]`  |                1.25 (5%) :x: |                1.08 (1%) :x: |
| `["overhead", "stoppable=true"]`                    | 0.93 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["parallel_histogram", "assoc", "basesize=4096"]`  |                   0.99 (5%)  | 0.87 (1%) :white_check_mark: |
| `["parallel_histogram", "comm", "basesize=4096"]`   |                1.23 (5%) :x: |                   1.00 (1%)  |
| `["parallel_histogram", "comm", "basesize=8192"]`   | 0.93 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["partition_length_maximum", "rand", "reduce"]`    |                   1.00 (5%)  |                1.01 (1%) :x: |
| `["splitby", "count", "foldl"]`                     |                2.16 (5%) :x: |                6.00 (1%) :x: |
| `["splitby", "count", "man"]`                       | 0.93 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["splitby", "count", "reduce"]`                    | 0.95 (5%) :white_check_mark: |                1.05 (1%) :x: |

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
  uname: Linux 5.8.0-1039-azure #42~20.04.1-Ubuntu SMP Thu Jul 15 14:11:07 UTC 2021 x86_64 x86_64
  CPU: Intel(R) Xeon(R) CPU E5-2673 v3 @ 2.40GHz: 
              speed         user         nice          sys         idle          irq
       #1  2397 MHz      60483 s         12 s       2350 s      17687 s          0 s
       #2  2397 MHz      51570 s          8 s       2220 s      27000 s          0 s
       
  Memory: 6.790924072265625 GB (3285.3046875 MB free)
  Uptime: 815.0 sec
  Load Avg:  1.5693359375  1.533203125  0.9912109375
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
  uname: Linux 5.8.0-1039-azure #42~20.04.1-Ubuntu SMP Thu Jul 15 14:11:07 UTC 2021 x86_64 x86_64
  CPU: Intel(R) Xeon(R) CPU E5-2673 v3 @ 2.40GHz: 
              speed         user         nice          sys         idle          irq
       #1  2397 MHz      89754 s         12 s       2894 s      23454 s          0 s
       #2  2397 MHz      74816 s          8 s       2797 s      38723 s          0 s
       
  Memory: 6.790924072265625 GB (3263.1484375 MB free)
  Uptime: 1172.0 sec
  Load Avg:  1.474609375  1.51513671875  1.15283203125
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-9.0.1 (ORCJIT, haswell)
```

---
# Target result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmark: 30 Aug 2021 - 1:15
* Package commit: f9e741
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
| `["collect", "assoc", "basesize=1"]`                | 299.021 ms (5%) |         |  32.66 MiB (1%) |      286756 |
| `["collect", "assoc", "basesize=1024"]`             | 251.347 ms (5%) |         |   1.79 MiB (1%) |         569 |
| `["collect", "assoc", "basesize=32"]`               | 254.218 ms (5%) |         |   3.97 MiB (1%) |       13306 |
| `["collect", "seq"]`                                | 504.214 ms (5%) |         | 512.72 KiB (1%) |          15 |
| `["collect", "unordered", "basesize=1"]`            | 518.828 ms (5%) |         |  30.01 MiB (1%) |      360586 |
| `["collect", "unordered", "basesize=1024"]`         | 347.380 ms (5%) |         | 913.42 KiB (1%) |        5969 |
| `["collect", "unordered", "basesize=32"]`           | 281.286 ms (5%) |         |   1.47 MiB (1%) |       12524 |
| `["findfirst", "n=1000", "foldl"]`                  | 728.131 ms (5%) |         |                 |             |
| `["findfirst", "n=1000", "reduce", "basesize=128"]` | 805.114 ms (5%) |         |   1.26 MiB (1%) |       22673 |
| `["findfirst", "n=1000", "reduce", "basesize=256"]` | 516.689 ms (5%) |         | 484.92 KiB (1%) |        8494 |
| `["findfirst", "n=1000", "reduce", "basesize=512"]` | 656.541 ms (5%) |         | 317.53 KiB (1%) |        5574 |
| `["findfirst", "n=400", "foldl"]`                   | 547.671 ms (5%) |         |                 |             |
| `["findfirst", "n=400", "reduce", "basesize=128"]`  | 292.440 ms (5%) |         |   1.11 MiB (1%) |       19929 |
| `["findfirst", "n=400", "reduce", "basesize=256"]`  | 290.897 ms (5%) |         | 597.70 KiB (1%) |       10535 |
| `["findfirst", "n=400", "reduce", "basesize=512"]`  | 329.476 ms (5%) |         | 368.77 KiB (1%) |        6498 |
| `["findfirst", "n=500", "foldl"]`                   |  93.838 ms (5%) |         |                 |             |
| `["findfirst", "n=500", "reduce", "basesize=128"]`  | 222.847 ms (5%) |         | 849.67 KiB (1%) |       14800 |
| `["findfirst", "n=500", "reduce", "basesize=256"]`  | 169.270 ms (5%) |         | 423.27 KiB (1%) |        7350 |
| `["findfirst", "n=500", "reduce", "basesize=512"]`  | 154.821 ms (5%) |         | 215.44 KiB (1%) |        3753 |
| `["overhead", "default"]`                           |  59.602 μs (5%) |         |  47.36 KiB (1%) |         382 |
| `["overhead", "stoppable=false"]`                   |  61.702 μs (5%) |         |  47.39 KiB (1%) |         382 |
| `["overhead", "stoppable=true"]`                    | 159.606 μs (5%) |         | 139.67 KiB (1%) |        2464 |
| `["parallel_histogram", "assoc", "basesize=16384"]` |   4.774 ms (5%) |         | 730.06 KiB (1%) |          57 |
| `["parallel_histogram", "assoc", "basesize=4096"]`  |   5.523 ms (5%) |         |   1.79 MiB (1%) |         213 |
| `["parallel_histogram", "assoc", "basesize=8192"]`  |   5.144 ms (5%) |         |   1.43 MiB (1%) |         117 |
| `["parallel_histogram", "comm", "basesize=16384"]`  |  12.648 ms (5%) |         |   1.22 MiB (1%) |         199 |
| `["parallel_histogram", "comm", "basesize=4096"]`   |  19.206 ms (5%) |         |   1.01 MiB (1%) |         884 |
| `["parallel_histogram", "comm", "basesize=8192"]`   |  14.709 ms (5%) |         |   1.23 MiB (1%) |         403 |
| `["parallel_histogram", "seq"]`                     |   8.638 ms (5%) |         | 364.61 KiB (1%) |          24 |
| `["partition_length_maximum", "rand", "foldl"]`     |  64.053 ms (5%) |         |                 |             |
| `["partition_length_maximum", "rand", "reduce"]`    |  31.881 ms (5%) |         |   2.66 KiB (1%) |          48 |
| `["splitby", "count", "foldl"]`                     |   4.689 ms (5%) |         |   96 bytes (1%) |           4 |
| `["splitby", "count", "man"]`                       |   1.833 ms (5%) |         |                 |             |
| `["splitby", "count", "reduce"]`                    | 951.937 μs (5%) |         |   2.88 KiB (1%) |          55 |
| `["sum", "random", "foldl"]`                        |  18.709 ms (5%) |         |   32 bytes (1%) |           2 |
| `["sum", "random", "reduce", "basesize=128"]`       |   9.605 ms (5%) |         | 103.23 KiB (1%) |        1018 |
| `["sum", "random", "reduce", "basesize=256"]`       |   9.485 ms (5%) |         |  51.23 KiB (1%) |         506 |
| `["sum", "random", "reduce", "basesize=512"]`       |   9.420 ms (5%) |         |  25.30 KiB (1%) |         252 |
| `["sum", "uniform", "foldl"]`                       |  18.155 ms (5%) |         |   32 bytes (1%) |           2 |
| `["sum", "uniform", "reduce", "basesize=128"]`      |   9.287 ms (5%) |         | 103.23 KiB (1%) |        1018 |
| `["sum", "uniform", "reduce", "basesize=256"]`      |   9.174 ms (5%) |         |  51.23 KiB (1%) |         506 |
| `["sum", "uniform", "reduce", "basesize=512"]`      |   9.100 ms (5%) |         |  25.25 KiB (1%) |         251 |
| `["sum", "valley", "foldl"]`                        |  18.669 ms (5%) |         |   32 bytes (1%) |           2 |
| `["sum", "valley", "reduce", "basesize=128"]`       |   9.581 ms (5%) |         | 103.23 KiB (1%) |        1018 |
| `["sum", "valley", "reduce", "basesize=256"]`       |   9.458 ms (5%) |         |  51.23 KiB (1%) |         506 |
| `["sum", "valley", "reduce", "basesize=512"]`       |   9.369 ms (5%) |         |  25.25 KiB (1%) |         251 |
| `["words", "nthreads=1"]`                           |  26.366 ms (5%) |         |  31.40 MiB (1%) |     1023077 |
| `["words", "nthreads=2"]`                           |  15.521 ms (5%) |         |  32.12 MiB (1%) |     1023211 |
| `["words", "nthreads=4"]`                           |  15.961 ms (5%) |         |  32.57 MiB (1%) |     1023295 |

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
  uname: Linux 5.8.0-1039-azure #42~20.04.1-Ubuntu SMP Thu Jul 15 14:11:07 UTC 2021 x86_64 x86_64
  CPU: Intel(R) Xeon(R) CPU E5-2673 v3 @ 2.40GHz: 
              speed         user         nice          sys         idle          irq
       #1  2397 MHz      60483 s         12 s       2350 s      17687 s          0 s
       #2  2397 MHz      51570 s          8 s       2220 s      27000 s          0 s
       
  Memory: 6.790924072265625 GB (3285.3046875 MB free)
  Uptime: 815.0 sec
  Load Avg:  1.5693359375  1.533203125  0.9912109375
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-9.0.1 (ORCJIT, haswell)
```

---
# Baseline result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmark: 30 Aug 2021 - 1:21
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
| `["collect", "assoc", "basesize=1"]`                | 299.073 ms (5%) |         |  32.66 MiB (1%) |      286765 |
| `["collect", "assoc", "basesize=1024"]`             | 250.633 ms (5%) |         |   1.79 MiB (1%) |         570 |
| `["collect", "assoc", "basesize=32"]`               | 252.922 ms (5%) |         |   3.97 MiB (1%) |       13307 |
| `["collect", "seq"]`                                | 506.392 ms (5%) |         | 512.72 KiB (1%) |          15 |
| `["collect", "unordered", "basesize=1"]`            | 522.718 ms (5%) |         |  30.01 MiB (1%) |      360612 |
| `["collect", "unordered", "basesize=1024"]`         | 423.338 ms (5%) |         |   1.05 MiB (1%) |       11122 |
| `["collect", "unordered", "basesize=32"]`           | 276.094 ms (5%) |         |   1.47 MiB (1%) |       12455 |
| `["findfirst", "n=1000", "foldl"]`                  | 737.475 ms (5%) |         |                 |             |
| `["findfirst", "n=1000", "reduce", "basesize=128"]` | 810.452 ms (5%) |         |   1.24 MiB (1%) |       22317 |
| `["findfirst", "n=1000", "reduce", "basesize=256"]` | 519.842 ms (5%) |         | 482.64 KiB (1%) |        8455 |
| `["findfirst", "n=1000", "reduce", "basesize=512"]` | 720.183 ms (5%) |         | 351.98 KiB (1%) |        6175 |
| `["findfirst", "n=400", "foldl"]`                   | 550.325 ms (5%) |         |                 |             |
| `["findfirst", "n=400", "reduce", "basesize=128"]`  | 286.809 ms (5%) |         |   1.07 MiB (1%) |       19261 |
| `["findfirst", "n=400", "reduce", "basesize=256"]`  | 299.951 ms (5%) |         | 593.03 KiB (1%) |       10455 |
| `["findfirst", "n=400", "reduce", "basesize=512"]`  | 327.210 ms (5%) |         | 368.78 KiB (1%) |        6499 |
| `["findfirst", "n=500", "foldl"]`                   |  94.062 ms (5%) |         |                 |             |
| `["findfirst", "n=500", "reduce", "basesize=128"]`  | 190.076 ms (5%) |         | 791.19 KiB (1%) |       13765 |
| `["findfirst", "n=500", "reduce", "basesize=256"]`  | 183.090 ms (5%) |         | 377.92 KiB (1%) |        6592 |
| `["findfirst", "n=500", "reduce", "basesize=512"]`  | 124.236 ms (5%) |         | 199.44 KiB (1%) |        3476 |
| `["overhead", "default"]`                           |  61.002 μs (5%) |         |  47.36 KiB (1%) |         382 |
| `["overhead", "stoppable=false"]`                   |  60.002 μs (5%) |         |  47.39 KiB (1%) |         382 |
| `["overhead", "stoppable=true"]`                    | 171.207 μs (5%) |         | 139.67 KiB (1%) |        2464 |
| `["parallel_histogram", "assoc", "basesize=16384"]` |   4.742 ms (5%) |         | 730.06 KiB (1%) |          57 |
| `["parallel_histogram", "assoc", "basesize=4096"]`  |   5.563 ms (5%) |         |   2.06 MiB (1%) |         219 |
| `["parallel_histogram", "assoc", "basesize=8192"]`  |   5.089 ms (5%) |         |   1.43 MiB (1%) |         117 |
| `["parallel_histogram", "comm", "basesize=16384"]`  |  12.757 ms (5%) |         |   1.22 MiB (1%) |         188 |
| `["parallel_histogram", "comm", "basesize=4096"]`   |  15.662 ms (5%) |         |   1.01 MiB (1%) |        1219 |
| `["parallel_histogram", "comm", "basesize=8192"]`   |  15.831 ms (5%) |         |   1.23 MiB (1%) |         397 |
| `["parallel_histogram", "seq"]`                     |   8.671 ms (5%) |         | 364.61 KiB (1%) |          24 |
| `["partition_length_maximum", "rand", "foldl"]`     |  64.331 ms (5%) |         |                 |             |
| `["partition_length_maximum", "rand", "reduce"]`    |  31.905 ms (5%) |         |   2.63 KiB (1%) |          47 |
| `["splitby", "count", "foldl"]`                     |   2.167 ms (5%) |         |   16 bytes (1%) |           1 |
| `["splitby", "count", "man"]`                       |   1.966 ms (5%) |         |                 |             |
| `["splitby", "count", "reduce"]`                    |   1.005 ms (5%) |         |   2.75 KiB (1%) |          51 |
| `["sum", "random", "foldl"]`                        |  18.766 ms (5%) |         |   32 bytes (1%) |           2 |
| `["sum", "random", "reduce", "basesize=128"]`       |   9.608 ms (5%) |         | 103.23 KiB (1%) |        1018 |
| `["sum", "random", "reduce", "basesize=256"]`       |   9.458 ms (5%) |         |  51.23 KiB (1%) |         506 |
| `["sum", "random", "reduce", "basesize=512"]`       |   9.380 ms (5%) |         |  25.30 KiB (1%) |         252 |
| `["sum", "uniform", "foldl"]`                       |  18.302 ms (5%) |         |   32 bytes (1%) |           2 |
| `["sum", "uniform", "reduce", "basesize=128"]`      |   9.283 ms (5%) |         | 103.23 KiB (1%) |        1018 |
| `["sum", "uniform", "reduce", "basesize=256"]`      |   9.168 ms (5%) |         |  51.23 KiB (1%) |         506 |
| `["sum", "uniform", "reduce", "basesize=512"]`      |   9.128 ms (5%) |         |  25.25 KiB (1%) |         251 |
| `["sum", "valley", "foldl"]`                        |  18.730 ms (5%) |         |   32 bytes (1%) |           2 |
| `["sum", "valley", "reduce", "basesize=128"]`       |   9.599 ms (5%) |         | 103.23 KiB (1%) |        1018 |
| `["sum", "valley", "reduce", "basesize=256"]`       |   9.480 ms (5%) |         |  51.23 KiB (1%) |         506 |
| `["sum", "valley", "reduce", "basesize=512"]`       |   9.388 ms (5%) |         |  25.25 KiB (1%) |         251 |
| `["words", "nthreads=1"]`                           |  25.958 ms (5%) |         |  31.51 MiB (1%) |     1026312 |
| `["words", "nthreads=2"]`                           |  15.884 ms (5%) |         |  31.87 MiB (1%) |     1026348 |
| `["words", "nthreads=4"]`                           |  16.599 ms (5%) |         |  32.76 MiB (1%) |     1026481 |

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
  uname: Linux 5.8.0-1039-azure #42~20.04.1-Ubuntu SMP Thu Jul 15 14:11:07 UTC 2021 x86_64 x86_64
  CPU: Intel(R) Xeon(R) CPU E5-2673 v3 @ 2.40GHz: 
              speed         user         nice          sys         idle          irq
       #1  2397 MHz      89754 s         12 s       2894 s      23454 s          0 s
       #2  2397 MHz      74816 s          8 s       2797 s      38723 s          0 s
       
  Memory: 6.790924072265625 GB (3263.1484375 MB free)
  Uptime: 1172.0 sec
  Load Avg:  1.474609375  1.51513671875  1.15283203125
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

