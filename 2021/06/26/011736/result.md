# Multi-thread benchmark result

* Pull request commit: [`8a25a6b7b17b094a97a2fcf0a1ae500c5bf1a865`](https://github.com/JuliaFolds/Transducers.jl/commit/8a25a6b7b17b094a97a2fcf0a1ae500c5bf1a865)
* Pull request: <https://github.com/JuliaFolds/Transducers.jl/pull/243> (Update */Manifest.toml)

# Judge result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmarks:
    - Target: 26 Jun 2021 - 01:11
    - Baseline: 26 Jun 2021 - 01:17
* Package commits:
    - Target: 08089d
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
| `["collect", "unordered", "basesize=1"]`            | 0.77 (5%) :white_check_mark: | 0.98 (1%) :white_check_mark: |
| `["collect", "unordered", "basesize=1024"]`         |                1.13 (5%) :x: |                1.07 (1%) :x: |
| `["findfirst", "n=1000", "reduce", "basesize=256"]` |                   0.96 (5%)  | 0.96 (1%) :white_check_mark: |
| `["findfirst", "n=1000", "reduce", "basesize=512"]` | 0.93 (5%) :white_check_mark: | 0.99 (1%) :white_check_mark: |
| `["findfirst", "n=400", "reduce", "basesize=128"]`  | 0.88 (5%) :white_check_mark: | 0.91 (1%) :white_check_mark: |
| `["findfirst", "n=500", "reduce", "basesize=128"]`  | 0.81 (5%) :white_check_mark: | 0.80 (1%) :white_check_mark: |
| `["findfirst", "n=500", "reduce", "basesize=256"]`  | 0.68 (5%) :white_check_mark: | 0.73 (1%) :white_check_mark: |
| `["findfirst", "n=500", "reduce", "basesize=512"]`  |                1.08 (5%) :x: |                1.12 (1%) :x: |
| `["parallel_histogram", "comm", "basesize=8192"]`   | 0.95 (5%) :white_check_mark: | 0.98 (1%) :white_check_mark: |
| `["splitby", "count", "foldl"]`                     |                1.86 (5%) :x: |                6.00 (1%) :x: |
| `["splitby", "count", "reduce"]`                    |                   1.02 (5%)  |                1.08 (1%) :x: |

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
  CPU: Intel(R) Xeon(R) Platinum 8272CL CPU @ 2.60GHz: 
              speed         user         nice          sys         idle          irq
       #1  2593 MHz      54231 s         10 s       2099 s      16039 s          0 s
       #2  2593 MHz      51690 s          8 s       2292 s      18439 s          0 s
       
  Memory: 6.790924072265625 GB (3610.42578125 MB free)
  Uptime: 730.0 sec
  Load Avg:  1.6240234375  1.46044921875  0.8740234375
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
  CPU: Intel(R) Xeon(R) Platinum 8272CL CPU @ 2.60GHz: 
              speed         user         nice          sys         idle          irq
       #1  2593 MHz      77395 s         10 s       2815 s      24879 s          0 s
       #2  2593 MHz      77932 s          8 s       2878 s      24475 s          0 s
       
  Memory: 6.790924072265625 GB (3390.81640625 MB free)
  Uptime: 1059.0 sec
  Load Avg:  1.712890625  1.5673828125  1.09765625
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-9.0.1 (ORCJIT, skylake-avx512)
```

---
# Target result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmark: 26 Jun 2021 - 1:11
* Package commit: 08089d
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
| `["collect", "assoc", "basesize=1"]`                | 238.004 ms (5%) |         |  32.66 MiB (1%) |      286745 |
| `["collect", "assoc", "basesize=1024"]`             | 198.075 ms (5%) |         |   1.79 MiB (1%) |         569 |
| `["collect", "assoc", "basesize=32"]`               | 200.266 ms (5%) |         |   3.97 MiB (1%) |       13307 |
| `["collect", "seq"]`                                | 394.849 ms (5%) |         | 512.72 KiB (1%) |          15 |
| `["collect", "unordered", "basesize=1"]`            | 421.265 ms (5%) |         |  30.01 MiB (1%) |      360566 |
| `["collect", "unordered", "basesize=1024"]`         | 279.403 ms (5%) |         | 911.39 KiB (1%) |        5904 |
| `["collect", "unordered", "basesize=32"]`           | 222.849 ms (5%) |         |   1.47 MiB (1%) |       12522 |
| `["findfirst", "n=1000", "foldl"]`                  | 627.129 ms (5%) |         |                 |             |
| `["findfirst", "n=1000", "reduce", "basesize=128"]` | 686.644 ms (5%) |         |   1.25 MiB (1%) |       22503 |
| `["findfirst", "n=1000", "reduce", "basesize=256"]` | 423.473 ms (5%) |         | 466.42 KiB (1%) |        8171 |
| `["findfirst", "n=1000", "reduce", "basesize=512"]` | 567.411 ms (5%) |         | 347.42 KiB (1%) |        6109 |
| `["findfirst", "n=400", "foldl"]`                   | 470.715 ms (5%) |         |                 |             |
| `["findfirst", "n=400", "reduce", "basesize=128"]`  | 248.208 ms (5%) |         |   1.10 MiB (1%) |       19734 |
| `["findfirst", "n=400", "reduce", "basesize=256"]`  | 264.777 ms (5%) |         | 602.66 KiB (1%) |       10638 |
| `["findfirst", "n=400", "reduce", "basesize=512"]`  | 269.209 ms (5%) |         | 357.55 KiB (1%) |        6310 |
| `["findfirst", "n=500", "foldl"]`                   |  81.626 ms (5%) |         |                 |             |
| `["findfirst", "n=500", "reduce", "basesize=128"]`  | 150.294 ms (5%) |         | 707.91 KiB (1%) |       12329 |
| `["findfirst", "n=500", "reduce", "basesize=256"]`  |  91.527 ms (5%) |         | 264.81 KiB (1%) |        4620 |
| `["findfirst", "n=500", "reduce", "basesize=512"]`  | 248.951 ms (5%) |         | 330.63 KiB (1%) |        5772 |
| `["overhead", "default"]`                           |  60.301 μs (5%) |         |  47.36 KiB (1%) |         382 |
| `["overhead", "stoppable=false"]`                   |  60.001 μs (5%) |         |  47.39 KiB (1%) |         382 |
| `["overhead", "stoppable=true"]`                    | 155.102 μs (5%) |         | 139.67 KiB (1%) |        2464 |
| `["parallel_histogram", "assoc", "basesize=16384"]` |   3.973 ms (5%) |         | 730.06 KiB (1%) |          57 |
| `["parallel_histogram", "assoc", "basesize=4096"]`  |   4.585 ms (5%) |         |   1.79 MiB (1%) |         213 |
| `["parallel_histogram", "assoc", "basesize=8192"]`  |   4.288 ms (5%) |         |   1.43 MiB (1%) |         117 |
| `["parallel_histogram", "comm", "basesize=16384"]`  |  13.301 ms (5%) |         |   1.23 MiB (1%) |         428 |
| `["parallel_histogram", "comm", "basesize=4096"]`   |  21.502 ms (5%) |         |   1.05 MiB (1%) |        2753 |
| `["parallel_histogram", "comm", "basesize=8192"]`   |  19.244 ms (5%) |         |   1.25 MiB (1%) |        1139 |
| `["parallel_histogram", "seq"]`                     |   7.244 ms (5%) |         | 364.61 KiB (1%) |          24 |
| `["partition_length_maximum", "rand", "foldl"]`     |  33.737 ms (5%) |         |                 |             |
| `["partition_length_maximum", "rand", "reduce"]`    |  16.877 ms (5%) |         |   2.66 KiB (1%) |          48 |
| `["splitby", "count", "foldl"]`                     |   4.429 ms (5%) |         |   96 bytes (1%) |           4 |
| `["splitby", "count", "man"]`                       |   1.938 ms (5%) |         |                 |             |
| `["splitby", "count", "reduce"]`                    |   1.127 ms (5%) |         |   2.84 KiB (1%) |          54 |
| `["sum", "random", "foldl"]`                        |  15.868 ms (5%) |         |   32 bytes (1%) |           2 |
| `["sum", "random", "reduce", "basesize=128"]`       |   8.112 ms (5%) |         | 103.23 KiB (1%) |        1018 |
| `["sum", "random", "reduce", "basesize=256"]`       |   8.011 ms (5%) |         |  51.23 KiB (1%) |         506 |
| `["sum", "random", "reduce", "basesize=512"]`       |   7.957 ms (5%) |         |  25.30 KiB (1%) |         252 |
| `["sum", "uniform", "foldl"]`                       |  15.510 ms (5%) |         |   32 bytes (1%) |           2 |
| `["sum", "uniform", "reduce", "basesize=128"]`      |   7.953 ms (5%) |         | 103.23 KiB (1%) |        1018 |
| `["sum", "uniform", "reduce", "basesize=256"]`      |   7.866 ms (5%) |         |  51.23 KiB (1%) |         506 |
| `["sum", "uniform", "reduce", "basesize=512"]`      |   7.819 ms (5%) |         |  25.25 KiB (1%) |         251 |
| `["sum", "valley", "foldl"]`                        |  16.048 ms (5%) |         |   32 bytes (1%) |           2 |
| `["sum", "valley", "reduce", "basesize=128"]`       |   8.168 ms (5%) |         | 103.23 KiB (1%) |        1018 |
| `["sum", "valley", "reduce", "basesize=256"]`       |   8.096 ms (5%) |         |  51.23 KiB (1%) |         506 |
| `["sum", "valley", "reduce", "basesize=512"]`       |   8.044 ms (5%) |         |  25.25 KiB (1%) |         251 |
| `["words", "nthreads=1"]`                           |  22.456 ms (5%) |         |  31.68 MiB (1%) |     1032598 |
| `["words", "nthreads=2"]`                           |  14.140 ms (5%) |         |  32.03 MiB (1%) |     1032634 |
| `["words", "nthreads=4"]`                           |  14.667 ms (5%) |         |  32.93 MiB (1%) |     1032778 |

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
  CPU: Intel(R) Xeon(R) Platinum 8272CL CPU @ 2.60GHz: 
              speed         user         nice          sys         idle          irq
       #1  2593 MHz      54231 s         10 s       2099 s      16039 s          0 s
       #2  2593 MHz      51690 s          8 s       2292 s      18439 s          0 s
       
  Memory: 6.790924072265625 GB (3610.42578125 MB free)
  Uptime: 730.0 sec
  Load Avg:  1.6240234375  1.46044921875  0.8740234375
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-9.0.1 (ORCJIT, skylake-avx512)
```

---
# Baseline result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmark: 26 Jun 2021 - 1:17
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
| `["collect", "assoc", "basesize=1"]`                | 238.497 ms (5%) |         |  32.66 MiB (1%) |      286742 |
| `["collect", "assoc", "basesize=1024"]`             | 198.638 ms (5%) |         |   1.79 MiB (1%) |         570 |
| `["collect", "assoc", "basesize=32"]`               | 200.168 ms (5%) |         |   3.97 MiB (1%) |       13306 |
| `["collect", "seq"]`                                | 395.094 ms (5%) |         | 512.72 KiB (1%) |          15 |
| `["collect", "unordered", "basesize=1"]`            | 549.736 ms (5%) |         |  30.62 MiB (1%) |      380456 |
| `["collect", "unordered", "basesize=1024"]`         | 246.543 ms (5%) |         | 849.77 KiB (1%) |        3914 |
| `["collect", "unordered", "basesize=32"]`           | 223.795 ms (5%) |         |   1.48 MiB (1%) |       12860 |
| `["findfirst", "n=1000", "foldl"]`                  | 628.211 ms (5%) |         |                 |             |
| `["findfirst", "n=1000", "reduce", "basesize=128"]` | 685.422 ms (5%) |         |   1.25 MiB (1%) |       22503 |
| `["findfirst", "n=1000", "reduce", "basesize=256"]` | 442.297 ms (5%) |         | 484.97 KiB (1%) |        8496 |
| `["findfirst", "n=1000", "reduce", "basesize=512"]` | 612.053 ms (5%) |         | 352.30 KiB (1%) |        6188 |
| `["findfirst", "n=400", "foldl"]`                   | 470.807 ms (5%) |         |                 |             |
| `["findfirst", "n=400", "reduce", "basesize=128"]`  | 280.924 ms (5%) |         |   1.21 MiB (1%) |       21769 |
| `["findfirst", "n=400", "reduce", "basesize=256"]`  | 264.691 ms (5%) |         | 607.36 KiB (1%) |       10724 |
| `["findfirst", "n=400", "reduce", "basesize=512"]`  | 279.173 ms (5%) |         | 357.47 KiB (1%) |        6303 |
| `["findfirst", "n=500", "foldl"]`                   |  81.696 ms (5%) |         |                 |             |
| `["findfirst", "n=500", "reduce", "basesize=128"]`  | 186.150 ms (5%) |         | 888.05 KiB (1%) |       15434 |
| `["findfirst", "n=500", "reduce", "basesize=256"]`  | 134.140 ms (5%) |         | 363.75 KiB (1%) |        6336 |
| `["findfirst", "n=500", "reduce", "basesize=512"]`  | 231.177 ms (5%) |         | 296.34 KiB (1%) |        5187 |
| `["overhead", "default"]`                           |  58.701 μs (5%) |         |  47.33 KiB (1%) |         381 |
| `["overhead", "stoppable=false"]`                   |  61.601 μs (5%) |         |  47.39 KiB (1%) |         382 |
| `["overhead", "stoppable=true"]`                    | 160.903 μs (5%) |         | 139.64 KiB (1%) |        2463 |
| `["parallel_histogram", "assoc", "basesize=16384"]` |   3.982 ms (5%) |         | 730.06 KiB (1%) |          57 |
| `["parallel_histogram", "assoc", "basesize=4096"]`  |   4.596 ms (5%) |         |   1.79 MiB (1%) |         213 |
| `["parallel_histogram", "assoc", "basesize=8192"]`  |   4.295 ms (5%) |         |   1.43 MiB (1%) |         117 |
| `["parallel_histogram", "comm", "basesize=16384"]`  |  12.970 ms (5%) |         |   1.23 MiB (1%) |         351 |
| `["parallel_histogram", "comm", "basesize=4096"]`   |  22.203 ms (5%) |         |   1.06 MiB (1%) |         770 |
| `["parallel_histogram", "comm", "basesize=8192"]`   |  20.280 ms (5%) |         |   1.27 MiB (1%) |        1870 |
| `["parallel_histogram", "seq"]`                     |   7.251 ms (5%) |         | 364.61 KiB (1%) |          24 |
| `["partition_length_maximum", "rand", "foldl"]`     |  33.730 ms (5%) |         |                 |             |
| `["partition_length_maximum", "rand", "reduce"]`    |  16.875 ms (5%) |         |   2.66 KiB (1%) |          48 |
| `["splitby", "count", "foldl"]`                     |   2.378 ms (5%) |         |   16 bytes (1%) |           1 |
| `["splitby", "count", "man"]`                       |   1.947 ms (5%) |         |                 |             |
| `["splitby", "count", "reduce"]`                    |   1.107 ms (5%) |         |   2.64 KiB (1%) |          49 |
| `["sum", "random", "foldl"]`                        |  16.004 ms (5%) |         |   32 bytes (1%) |           2 |
| `["sum", "random", "reduce", "basesize=128"]`       |   8.182 ms (5%) |         | 103.23 KiB (1%) |        1018 |
| `["sum", "random", "reduce", "basesize=256"]`       |   8.090 ms (5%) |         |  51.23 KiB (1%) |         506 |
| `["sum", "random", "reduce", "basesize=512"]`       |   8.054 ms (5%) |         |  25.30 KiB (1%) |         252 |
| `["sum", "uniform", "foldl"]`                       |  15.552 ms (5%) |         |   32 bytes (1%) |           2 |
| `["sum", "uniform", "reduce", "basesize=128"]`      |   7.942 ms (5%) |         | 103.23 KiB (1%) |        1018 |
| `["sum", "uniform", "reduce", "basesize=256"]`      |   7.871 ms (5%) |         |  51.23 KiB (1%) |         506 |
| `["sum", "uniform", "reduce", "basesize=512"]`      |   7.822 ms (5%) |         |  25.25 KiB (1%) |         251 |
| `["sum", "valley", "foldl"]`                        |  16.139 ms (5%) |         |   32 bytes (1%) |           2 |
| `["sum", "valley", "reduce", "basesize=128"]`       |   8.191 ms (5%) |         | 103.23 KiB (1%) |        1018 |
| `["sum", "valley", "reduce", "basesize=256"]`       |   8.103 ms (5%) |         |  51.23 KiB (1%) |         506 |
| `["sum", "valley", "reduce", "basesize=512"]`       |   8.099 ms (5%) |         |  25.25 KiB (1%) |         251 |
| `["words", "nthreads=1"]`                           |  21.982 ms (5%) |         |  31.60 MiB (1%) |     1029764 |
| `["words", "nthreads=2"]`                           |  13.684 ms (5%) |         |  31.96 MiB (1%) |     1029800 |
| `["words", "nthreads=4"]`                           |  14.466 ms (5%) |         |  32.86 MiB (1%) |     1029941 |

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
  CPU: Intel(R) Xeon(R) Platinum 8272CL CPU @ 2.60GHz: 
              speed         user         nice          sys         idle          irq
       #1  2593 MHz      77395 s         10 s       2815 s      24879 s          0 s
       #2  2593 MHz      77932 s          8 s       2878 s      24475 s          0 s
       
  Memory: 6.790924072265625 GB (3390.81640625 MB free)
  Uptime: 1059.0 sec
  Load Avg:  1.712890625  1.5673828125  1.09765625
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
    Model name:                      Intel(R) Xeon(R) Platinum 8272CL CPU @ 2.60GHz
    Stepping:                        7
    CPU MHz:                         2593.906
    BogoMIPS:                        5187.81
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
| Brand              | Intel(R) Xeon(R) Platinum 8272CL CPU @ 2.60GHz          |
| Vendor             | :Intel                                                  |
| Architecture       | :Skylake                                                |
| Model              | Family: 0x06, Model: 0x55, Stepping: 0x07, Type: 0x00   |
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

