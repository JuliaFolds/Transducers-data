# Multi-thread benchmark result

* Pull request commit: [`2e861d7a0f13b5e03333d4f7c7ebad70a4f596d7`](https://github.com/JuliaFolds/Transducers.jl/commit/2e861d7a0f13b5e03333d4f7c7ebad70a4f596d7)
* Pull request: <https://github.com/JuliaFolds/Transducers.jl/pull/243> (Update */Manifest.toml)

# Judge result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmarks:
    - Target: 15 Oct 2021 - 01:24
    - Baseline: 15 Oct 2021 - 01:30
* Package commits:
    - Target: d31d3e
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
| `["collect", "unordered", "basesize=1"]`            | 0.93 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["collect", "unordered", "basesize=1024"]`         | 0.94 (5%) :white_check_mark: | 0.96 (1%) :white_check_mark: |
| `["findfirst", "n=1000", "reduce", "basesize=128"]` | 0.83 (5%) :white_check_mark: | 0.83 (1%) :white_check_mark: |
| `["findfirst", "n=1000", "reduce", "basesize=256"]` |                   1.01 (5%)  | 0.96 (1%) :white_check_mark: |
| `["findfirst", "n=1000", "reduce", "basesize=512"]` | 0.87 (5%) :white_check_mark: | 0.82 (1%) :white_check_mark: |
| `["findfirst", "n=400", "reduce", "basesize=128"]`  |                   1.04 (5%)  |                1.02 (1%) :x: |
| `["findfirst", "n=400", "reduce", "basesize=512"]`  |                   1.01 (5%)  | 0.97 (1%) :white_check_mark: |
| `["findfirst", "n=500", "reduce", "basesize=128"]`  | 0.78 (5%) :white_check_mark: | 0.79 (1%) :white_check_mark: |
| `["findfirst", "n=500", "reduce", "basesize=256"]`  |                1.08 (5%) :x: |                1.19 (1%) :x: |
| `["findfirst", "n=500", "reduce", "basesize=512"]`  |                2.03 (5%) :x: |                1.52 (1%) :x: |
| `["parallel_histogram", "comm", "basesize=16384"]`  | 0.94 (5%) :white_check_mark: |                1.26 (1%) :x: |
| `["parallel_histogram", "comm", "basesize=4096"]`   |                   0.97 (5%)  | 0.99 (1%) :white_check_mark: |
| `["parallel_histogram", "comm", "basesize=8192"]`   |                1.05 (5%) :x: |                1.02 (1%) :x: |
| `["splitby", "count", "man"]`                       | 0.93 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["splitby", "count", "reduce"]`                    |                   1.03 (5%)  |                1.02 (1%) :x: |
| `["sum", "uniform", "reduce", "basesize=256"]`      |                1.05 (5%) :x: |                   1.00 (1%)  |
| `["sum", "valley", "foldl"]`                        |                1.06 (5%) :x: |                   1.00 (1%)  |

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
  uname: Linux 5.8.0-1042-azure #45~20.04.1-Ubuntu SMP Wed Sep 15 14:24:15 UTC 2021 x86_64 x86_64
  CPU: Intel(R) Xeon(R) CPU E5-2673 v4 @ 2.30GHz: 
              speed         user         nice          sys         idle          irq
       #1  2294 MHz      54578 s         21 s       2464 s      36107 s          0 s
       #2  2294 MHz      58424 s          4 s       2608 s      32459 s          0 s
       
  Memory: 6.790920257568359 GB (3068.7890625 MB free)
  Uptime: 943.0 sec
  Load Avg:  1.58203125  1.4658203125  0.91943359375
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
      Ubuntu 20.04.3 LTS
  uname: Linux 5.8.0-1042-azure #45~20.04.1-Ubuntu SMP Wed Sep 15 14:24:15 UTC 2021 x86_64 x86_64
  CPU: Intel(R) Xeon(R) CPU E5-2673 v4 @ 2.30GHz: 
              speed         user         nice          sys         idle          irq
       #1  2294 MHz      82152 s         21 s       3158 s      44185 s          0 s
       #2  2294 MHz      84042 s          4 s       3264 s      42657 s          0 s
       
  Memory: 6.790920257568359 GB (3055.546875 MB free)
  Uptime: 1308.0 sec
  Load Avg:  1.75390625  1.5439453125  1.1240234375
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-9.0.1 (ORCJIT, broadwell)
```

---
# Target result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmark: 15 Oct 2021 - 1:24
* Package commit: d31d3e
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
| `["collect", "assoc", "basesize=1"]`                | 238.327 ms (5%) |         |  32.66 MiB (1%) |      286767 |
| `["collect", "assoc", "basesize=1024"]`             | 184.958 ms (5%) |         |   1.79 MiB (1%) |         570 |
| `["collect", "assoc", "basesize=32"]`               | 183.162 ms (5%) |         |   3.97 MiB (1%) |       13305 |
| `["collect", "seq"]`                                | 353.003 ms (5%) |         | 512.72 KiB (1%) |          15 |
| `["collect", "unordered", "basesize=1"]`            | 463.034 ms (5%) |         |  30.01 MiB (1%) |      360632 |
| `["collect", "unordered", "basesize=1024"]`         | 281.780 ms (5%) |         | 871.95 KiB (1%) |        4642 |
| `["collect", "unordered", "basesize=32"]`           | 224.783 ms (5%) |         |   1.47 MiB (1%) |       12602 |
| `["findfirst", "n=1000", "foldl"]`                  | 584.973 ms (5%) |         |                 |             |
| `["findfirst", "n=1000", "reduce", "basesize=128"]` | 523.886 ms (5%) |         | 987.70 KiB (1%) |       17354 |
| `["findfirst", "n=1000", "reduce", "basesize=256"]` | 419.384 ms (5%) |         | 466.42 KiB (1%) |        8171 |
| `["findfirst", "n=1000", "reduce", "basesize=512"]` | 553.223 ms (5%) |         | 324.33 KiB (1%) |        5689 |
| `["findfirst", "n=400", "foldl"]`                   | 432.243 ms (5%) |         |                 |             |
| `["findfirst", "n=400", "reduce", "basesize=128"]`  | 245.942 ms (5%) |         |   1.11 MiB (1%) |       19940 |
| `["findfirst", "n=400", "reduce", "basesize=256"]`  | 250.779 ms (5%) |         | 602.47 KiB (1%) |       10629 |
| `["findfirst", "n=400", "reduce", "basesize=512"]`  | 275.670 ms (5%) |         | 361.91 KiB (1%) |        6382 |
| `["findfirst", "n=500", "foldl"]`                   |  73.512 ms (5%) |         |                 |             |
| `["findfirst", "n=500", "reduce", "basesize=128"]`  | 120.546 ms (5%) |         | 541.69 KiB (1%) |        9447 |
| `["findfirst", "n=500", "reduce", "basesize=256"]`  | 117.838 ms (5%) |         | 367.92 KiB (1%) |        6394 |
| `["findfirst", "n=500", "reduce", "basesize=512"]`  | 221.630 ms (5%) |         | 282.58 KiB (1%) |        4946 |
| `["overhead", "default"]`                           |  61.500 μs (5%) |         |  47.36 KiB (1%) |         382 |
| `["overhead", "stoppable=false"]`                   |  60.000 μs (5%) |         |  47.39 KiB (1%) |         382 |
| `["overhead", "stoppable=true"]`                    | 162.498 μs (5%) |         | 139.67 KiB (1%) |        2464 |
| `["parallel_histogram", "assoc", "basesize=16384"]` |   3.652 ms (5%) |         | 730.06 KiB (1%) |          57 |
| `["parallel_histogram", "assoc", "basesize=4096"]`  |   4.558 ms (5%) |         |   1.79 MiB (1%) |         213 |
| `["parallel_histogram", "assoc", "basesize=8192"]`  |   3.965 ms (5%) |         |   1.43 MiB (1%) |         117 |
| `["parallel_histogram", "comm", "basesize=16384"]`  |  14.546 ms (5%) |         |   1.22 MiB (1%) |         261 |
| `["parallel_histogram", "comm", "basesize=4096"]`   |  20.034 ms (5%) |         |   1.02 MiB (1%) |        1215 |
| `["parallel_histogram", "comm", "basesize=8192"]`   |  19.678 ms (5%) |         |   1.25 MiB (1%) |        1128 |
| `["parallel_histogram", "seq"]`                     |   6.378 ms (5%) |         | 364.61 KiB (1%) |          24 |
| `["partition_length_maximum", "rand", "foldl"]`     |  35.657 ms (5%) |         |                 |             |
| `["partition_length_maximum", "rand", "reduce"]`    |  18.038 ms (5%) |         |   2.66 KiB (1%) |          48 |
| `["splitby", "count", "foldl"]`                     |   4.149 ms (5%) |         |   96 bytes (1%) |           4 |
| `["splitby", "count", "man"]`                       |   1.553 ms (5%) |         |                 |             |
| `["splitby", "count", "reduce"]`                    | 867.095 μs (5%) |         |   2.83 KiB (1%) |          55 |
| `["sum", "random", "foldl"]`                        |  13.669 ms (5%) |         |   32 bytes (1%) |           2 |
| `["sum", "random", "reduce", "basesize=128"]`       |   6.929 ms (5%) |         | 103.23 KiB (1%) |        1018 |
| `["sum", "random", "reduce", "basesize=256"]`       |   7.009 ms (5%) |         |  51.23 KiB (1%) |         506 |
| `["sum", "random", "reduce", "basesize=512"]`       |   7.051 ms (5%) |         |  25.30 KiB (1%) |         252 |
| `["sum", "uniform", "foldl"]`                       |  13.214 ms (5%) |         |   32 bytes (1%) |           2 |
| `["sum", "uniform", "reduce", "basesize=128"]`      |   6.955 ms (5%) |         | 103.23 KiB (1%) |        1018 |
| `["sum", "uniform", "reduce", "basesize=256"]`      |   7.152 ms (5%) |         |  51.23 KiB (1%) |         506 |
| `["sum", "uniform", "reduce", "basesize=512"]`      |   6.985 ms (5%) |         |  25.25 KiB (1%) |         251 |
| `["sum", "valley", "foldl"]`                        |  14.386 ms (5%) |         |   32 bytes (1%) |           2 |
| `["sum", "valley", "reduce", "basesize=128"]`       |   7.133 ms (5%) |         | 103.23 KiB (1%) |        1018 |
| `["sum", "valley", "reduce", "basesize=256"]`       |   7.092 ms (5%) |         |  51.23 KiB (1%) |         506 |
| `["sum", "valley", "reduce", "basesize=512"]`       |   7.012 ms (5%) |         |  25.28 KiB (1%) |         252 |
| `["words", "nthreads=1"]`                           |  27.073 ms (5%) |         |  31.65 MiB (1%) |     1031430 |
| `["words", "nthreads=2"]`                           |  16.418 ms (5%) |         |  32.01 MiB (1%) |     1031466 |
| `["words", "nthreads=4"]`                           |  16.602 ms (5%) |         |  32.91 MiB (1%) |     1031610 |

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
  uname: Linux 5.8.0-1042-azure #45~20.04.1-Ubuntu SMP Wed Sep 15 14:24:15 UTC 2021 x86_64 x86_64
  CPU: Intel(R) Xeon(R) CPU E5-2673 v4 @ 2.30GHz: 
              speed         user         nice          sys         idle          irq
       #1  2294 MHz      54578 s         21 s       2464 s      36107 s          0 s
       #2  2294 MHz      58424 s          4 s       2608 s      32459 s          0 s
       
  Memory: 6.790920257568359 GB (3068.7890625 MB free)
  Uptime: 943.0 sec
  Load Avg:  1.58203125  1.4658203125  0.91943359375
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-9.0.1 (ORCJIT, broadwell)
```

---
# Baseline result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmark: 15 Oct 2021 - 1:30
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
| `["collect", "assoc", "basesize=1"]`                | 243.517 ms (5%) |         |  32.66 MiB (1%) |      286761 |
| `["collect", "assoc", "basesize=1024"]`             | 183.023 ms (5%) |         |   1.79 MiB (1%) |         569 |
| `["collect", "assoc", "basesize=32"]`               | 185.774 ms (5%) |         |   3.97 MiB (1%) |       13306 |
| `["collect", "seq"]`                                | 365.564 ms (5%) |         | 512.72 KiB (1%) |          15 |
| `["collect", "unordered", "basesize=1"]`            | 498.674 ms (5%) |         |  30.01 MiB (1%) |      360697 |
| `["collect", "unordered", "basesize=1024"]`         | 298.795 ms (5%) |         | 908.70 KiB (1%) |        5800 |
| `["collect", "unordered", "basesize=32"]`           | 231.446 ms (5%) |         |   1.48 MiB (1%) |       12776 |
| `["findfirst", "n=1000", "foldl"]`                  | 591.391 ms (5%) |         |                 |             |
| `["findfirst", "n=1000", "reduce", "basesize=128"]` | 627.976 ms (5%) |         |   1.16 MiB (1%) |       20762 |
| `["findfirst", "n=1000", "reduce", "basesize=256"]` | 415.909 ms (5%) |         | 484.97 KiB (1%) |        8496 |
| `["findfirst", "n=1000", "reduce", "basesize=512"]` | 634.674 ms (5%) |         | 393.20 KiB (1%) |        6889 |
| `["findfirst", "n=400", "foldl"]`                   | 436.153 ms (5%) |         |                 |             |
| `["findfirst", "n=400", "reduce", "basesize=128"]`  | 237.269 ms (5%) |         |   1.09 MiB (1%) |       19620 |
| `["findfirst", "n=400", "reduce", "basesize=256"]`  | 245.204 ms (5%) |         | 600.14 KiB (1%) |       10585 |
| `["findfirst", "n=400", "reduce", "basesize=512"]`  | 272.207 ms (5%) |         | 373.44 KiB (1%) |        6584 |
| `["findfirst", "n=500", "foldl"]`                   |  73.257 ms (5%) |         |                 |             |
| `["findfirst", "n=500", "reduce", "basesize=128"]`  | 154.044 ms (5%) |         | 689.55 KiB (1%) |       12004 |
| `["findfirst", "n=500", "reduce", "basesize=256"]`  | 108.817 ms (5%) |         | 308.92 KiB (1%) |        5395 |
| `["findfirst", "n=500", "reduce", "basesize=512"]`  | 109.307 ms (5%) |         | 185.75 KiB (1%) |        3243 |
| `["overhead", "default"]`                           |  59.500 μs (5%) |         |  47.36 KiB (1%) |         382 |
| `["overhead", "stoppable=false"]`                   |  57.699 μs (5%) |         |  47.39 KiB (1%) |         382 |
| `["overhead", "stoppable=true"]`                    | 166.499 μs (5%) |         | 139.67 KiB (1%) |        2464 |
| `["parallel_histogram", "assoc", "basesize=16384"]` |   3.633 ms (5%) |         | 730.06 KiB (1%) |          57 |
| `["parallel_histogram", "assoc", "basesize=4096"]`  |   4.460 ms (5%) |         |   1.79 MiB (1%) |         213 |
| `["parallel_histogram", "assoc", "basesize=8192"]`  |   4.012 ms (5%) |         |   1.43 MiB (1%) |         117 |
| `["parallel_histogram", "comm", "basesize=16384"]`  |  15.456 ms (5%) |         | 994.45 KiB (1%) |         360 |
| `["parallel_histogram", "comm", "basesize=4096"]`   |  20.625 ms (5%) |         |   1.03 MiB (1%) |        1753 |
| `["parallel_histogram", "comm", "basesize=8192"]`   |  18.733 ms (5%) |         |   1.23 MiB (1%) |         276 |
| `["parallel_histogram", "seq"]`                     |   6.473 ms (5%) |         | 364.61 KiB (1%) |          24 |
| `["partition_length_maximum", "rand", "foldl"]`     |  35.933 ms (5%) |         |                 |             |
| `["partition_length_maximum", "rand", "reduce"]`    |  18.454 ms (5%) |         |   2.66 KiB (1%) |          48 |
| `["splitby", "count", "foldl"]`                     |   4.086 ms (5%) |         |   96 bytes (1%) |           4 |
| `["splitby", "count", "man"]`                       |   1.677 ms (5%) |         |                 |             |
| `["splitby", "count", "reduce"]`                    | 845.095 μs (5%) |         |   2.78 KiB (1%) |          52 |
| `["sum", "random", "foldl"]`                        |  13.644 ms (5%) |         |   32 bytes (1%) |           2 |
| `["sum", "random", "reduce", "basesize=128"]`       |   7.180 ms (5%) |         | 103.23 KiB (1%) |        1018 |
| `["sum", "random", "reduce", "basesize=256"]`       |   7.085 ms (5%) |         |  51.23 KiB (1%) |         506 |
| `["sum", "random", "reduce", "basesize=512"]`       |   6.936 ms (5%) |         |  25.30 KiB (1%) |         252 |
| `["sum", "uniform", "foldl"]`                       |  13.309 ms (5%) |         |   32 bytes (1%) |           2 |
| `["sum", "uniform", "reduce", "basesize=128"]`      |   6.989 ms (5%) |         | 103.23 KiB (1%) |        1018 |
| `["sum", "uniform", "reduce", "basesize=256"]`      |   6.788 ms (5%) |         |  51.23 KiB (1%) |         506 |
| `["sum", "uniform", "reduce", "basesize=512"]`      |   6.711 ms (5%) |         |  25.25 KiB (1%) |         251 |
| `["sum", "valley", "foldl"]`                        |  13.636 ms (5%) |         |   32 bytes (1%) |           2 |
| `["sum", "valley", "reduce", "basesize=128"]`       |   6.934 ms (5%) |         | 103.23 KiB (1%) |        1018 |
| `["sum", "valley", "reduce", "basesize=256"]`       |   7.065 ms (5%) |         |  51.23 KiB (1%) |         506 |
| `["sum", "valley", "reduce", "basesize=512"]`       |   6.954 ms (5%) |         |  25.25 KiB (1%) |         251 |
| `["words", "nthreads=1"]`                           |  26.202 ms (5%) |         |  31.56 MiB (1%) |     1028338 |
| `["words", "nthreads=2"]`                           |  15.794 ms (5%) |         |  31.92 MiB (1%) |     1028374 |
| `["words", "nthreads=4"]`                           |  16.640 ms (5%) |         |  32.64 MiB (1%) |     1028446 |

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
  uname: Linux 5.8.0-1042-azure #45~20.04.1-Ubuntu SMP Wed Sep 15 14:24:15 UTC 2021 x86_64 x86_64
  CPU: Intel(R) Xeon(R) CPU E5-2673 v4 @ 2.30GHz: 
              speed         user         nice          sys         idle          irq
       #1  2294 MHz      82152 s         21 s       3158 s      44185 s          0 s
       #2  2294 MHz      84042 s          4 s       3264 s      42657 s          0 s
       
  Memory: 6.790920257568359 GB (3055.546875 MB free)
  Uptime: 1308.0 sec
  Load Avg:  1.75390625  1.5439453125  1.1240234375
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

