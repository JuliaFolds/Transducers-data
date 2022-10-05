# Multi-thread benchmark result

* Pull request commit: [`b5eda89358e6aa2f5bf36f67a65cb1ee7e4ee273`](https://github.com/JuliaFolds/Transducers.jl/commit/b5eda89358e6aa2f5bf36f67a65cb1ee7e4ee273)
* Pull request: <https://github.com/JuliaFolds/Transducers.jl/pull/536> (add delimitedfiles as dependency for 1.9 compat)

# Judge result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmarks:
    - Target: 5 Oct 2022 - 21:06
    - Baseline: 5 Oct 2022 - 21:11
* Package commits:
    - Target: be335f
    - Baseline: 958213
* Julia commits:
    - Target: 742b9a
    - Baseline: 742b9a
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
| `["collect", "assoc", "basesize=1024"]`             |                1.13 (5%) :x: |                   1.00 (1%)  |
| `["collect", "assoc", "basesize=32"]`               |                1.06 (5%) :x: |                   1.00 (1%)  |
| `["collect", "seq"]`                                |                1.13 (5%) :x: |                   1.00 (1%)  |
| `["collect", "unordered", "basesize=1"]`            |                1.09 (5%) :x: |                   0.99 (1%)  |
| `["collect", "unordered", "basesize=1024"]`         |                1.13 (5%) :x: |                   1.00 (1%)  |
| `["collect", "unordered", "basesize=32"]`           |                1.13 (5%) :x: |                   1.00 (1%)  |
| `["findfirst", "n=1000", "foldl"]`                  | 0.88 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["findfirst", "n=1000", "reduce", "basesize=128"]` |                   1.02 (5%)  |                1.04 (1%) :x: |
| `["findfirst", "n=1000", "reduce", "basesize=256"]` |                1.11 (5%) :x: |                1.09 (1%) :x: |
| `["findfirst", "n=1000", "reduce", "basesize=512"]` |                1.15 (5%) :x: |                1.12 (1%) :x: |
| `["findfirst", "n=400", "reduce", "basesize=512"]`  |                1.35 (5%) :x: |                1.29 (1%) :x: |
| `["findfirst", "n=500", "reduce", "basesize=128"]`  |                1.52 (5%) :x: |                1.41 (1%) :x: |
| `["findfirst", "n=500", "reduce", "basesize=256"]`  |                2.29 (5%) :x: |                1.71 (1%) :x: |
| `["findfirst", "n=500", "reduce", "basesize=512"]`  |                1.12 (5%) :x: |                   1.00 (1%)  |
| `["overhead", "stoppable=false"]`                   | 0.93 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["parallel_histogram", "assoc", "basesize=16384"]` |                1.13 (5%) :x: |                   1.00 (1%)  |
| `["parallel_histogram", "assoc", "basesize=4096"]`  |                1.12 (5%) :x: |                   1.00 (1%)  |
| `["parallel_histogram", "assoc", "basesize=8192"]`  |                1.13 (5%) :x: |                   1.00 (1%)  |
| `["parallel_histogram", "comm", "basesize=16384"]`  |                1.06 (5%) :x: | 0.99 (1%) :white_check_mark: |
| `["parallel_histogram", "comm", "basesize=4096"]`   |                1.10 (5%) :x: |                1.07 (1%) :x: |
| `["parallel_histogram", "comm", "basesize=8192"]`   | 0.94 (5%) :white_check_mark: |                   1.01 (1%)  |
| `["parallel_histogram", "seq"]`                     |                1.14 (5%) :x: |                   1.00 (1%)  |
| `["partition_length_maximum", "rand", "reduce"]`    |                   1.00 (5%)  | 0.96 (1%) :white_check_mark: |
| `["splitby", "count", "foldl"]`                     |                1.21 (5%) :x: |                   1.00 (1%)  |
| `["splitby", "count", "man"]`                       |                1.40 (5%) :x: |                   1.00 (1%)  |
| `["splitby", "count", "reduce"]`                    |                   1.00 (5%)  | 0.97 (1%) :white_check_mark: |
| `["sum", "random", "reduce", "basesize=128"]`       |                1.07 (5%) :x: |                   1.00 (1%)  |
| `["sum", "random", "reduce", "basesize=256"]`       |                1.07 (5%) :x: |                   1.00 (1%)  |
| `["sum", "random", "reduce", "basesize=512"]`       |                1.07 (5%) :x: |                   1.00 (1%)  |
| `["sum", "uniform", "foldl"]`                       |                1.14 (5%) :x: |                   1.00 (1%)  |
| `["sum", "uniform", "reduce", "basesize=128"]`      |                1.07 (5%) :x: |                   1.00 (1%)  |
| `["sum", "uniform", "reduce", "basesize=256"]`      |                1.07 (5%) :x: |                   1.00 (1%)  |
| `["sum", "uniform", "reduce", "basesize=512"]`      |                1.06 (5%) :x: |                   1.00 (1%)  |
| `["sum", "valley", "foldl"]`                        |                1.13 (5%) :x: |                   1.00 (1%)  |
| `["sum", "valley", "reduce", "basesize=128"]`       |                1.07 (5%) :x: |                   1.00 (1%)  |
| `["sum", "valley", "reduce", "basesize=256"]`       |                1.13 (5%) :x: |                   1.00 (1%)  |
| `["sum", "valley", "reduce", "basesize=512"]`       |                1.13 (5%) :x: |                   1.00 (1%)  |
| `["words", "nthreads=1"]`                           |                1.15 (5%) :x: |                   1.01 (1%)  |
| `["words", "nthreads=2"]`                           |                1.09 (5%) :x: |                1.02 (1%) :x: |
| `["words", "nthreads=4"]`                           |                1.12 (5%) :x: |                1.02 (1%) :x: |

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
Julia Version 1.7.3
Commit 742b9abb4d (2022-05-06 12:58 UTC)
Platform Info:
  OS: Linux (x86_64-pc-linux-gnu)
      Ubuntu 20.04.5 LTS
  uname: Linux 5.15.0-1020-azure #25~20.04.1-Ubuntu SMP Thu Sep 1 19:20:56 UTC 2022 x86_64 x86_64
  CPU: Intel(R) Xeon(R) Platinum 8272CL CPU @ 2.60GHz: 
              speed         user         nice          sys         idle          irq
       #1  2593 MHz       5076 s          0 s        250 s       3526 s          0 s
       #2  2593 MHz       5030 s          0 s        285 s       3539 s          0 s
       
  Memory: 6.781253814697266 GB (3738.08984375 MB free)
  Uptime: 890.03 sec
  Load Avg:  1.66  1.48  0.87
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-12.0.1 (ORCJIT, skylake-avx512)
```

### Baseline
```
Julia Version 1.7.3
Commit 742b9abb4d (2022-05-06 12:58 UTC)
Platform Info:
  OS: Linux (x86_64-pc-linux-gnu)
      Ubuntu 20.04.5 LTS
  uname: Linux 5.15.0-1020-azure #25~20.04.1-Ubuntu SMP Thu Sep 1 19:20:56 UTC 2022 x86_64 x86_64
  CPU: Intel(R) Xeon(R) Platinum 8272CL CPU @ 2.60GHz: 
              speed         user         nice          sys         idle          irq
       #1  2593 MHz       7420 s          0 s        290 s       4060 s          0 s
       #2  2593 MHz       7239 s          0 s        317 s       4215 s          0 s
       
  Memory: 6.781253814697266 GB (3751.6328125 MB free)
  Uptime: 1182.24 sec
  Load Avg:  1.66  1.58  1.09
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-12.0.1 (ORCJIT, skylake-avx512)
```

---
# Target result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmark: 5 Oct 2022 - 21:6
* Package commit: be335f
* Julia commit: 742b9a
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
| `["collect", "assoc", "basesize=1"]`                | 243.220 ms (5%) |         |   25.97 MiB (1%) |      306836 |
| `["collect", "assoc", "basesize=1024"]`             | 198.270 ms (5%) |         |    2.61 MiB (1%) |         455 |
| `["collect", "assoc", "basesize=32"]`               | 200.037 ms (5%) |         |    4.82 MiB (1%) |       11699 |
| `["collect", "seq"]`                                | 394.990 ms (5%) |         |  812.73 KiB (1%) |          11 |
| `["collect", "unordered", "basesize=1"]`            | 347.368 ms (5%) |         |   23.75 MiB (1%) |      408124 |
| `["collect", "unordered", "basesize=1024"]`         | 212.702 ms (5%) |         | 1002.55 KiB (1%) |         976 |
| `["collect", "unordered", "basesize=32"]`           | 223.389 ms (5%) |         |    1.58 MiB (1%) |       14596 |
| `["findfirst", "n=1000", "foldl"]`                  | 555.739 ms (5%) |         |                  |             |
| `["findfirst", "n=1000", "reduce", "basesize=128"]` | 321.366 ms (5%) |         |  232.91 KiB (1%) |        3278 |
| `["findfirst", "n=1000", "reduce", "basesize=256"]` | 439.031 ms (5%) |         |  164.70 KiB (1%) |        2303 |
| `["findfirst", "n=1000", "reduce", "basesize=512"]` | 532.160 ms (5%) |         |  108.64 KiB (1%) |        1513 |
| `["findfirst", "n=400", "foldl"]`                   | 417.645 ms (5%) |         |                  |             |
| `["findfirst", "n=400", "reduce", "basesize=128"]`  | 227.333 ms (5%) |         |  373.44 KiB (1%) |        5324 |
| `["findfirst", "n=400", "reduce", "basesize=256"]`  | 232.572 ms (5%) |         |  200.84 KiB (1%) |        2872 |
| `["findfirst", "n=400", "reduce", "basesize=512"]`  | 384.364 ms (5%) |         |  170.78 KiB (1%) |        2441 |
| `["findfirst", "n=500", "foldl"]`                   |  72.301 ms (5%) |         |                  |             |
| `["findfirst", "n=500", "reduce", "basesize=128"]`  | 193.556 ms (5%) |         |  296.27 KiB (1%) |        4056 |
| `["findfirst", "n=500", "reduce", "basesize=256"]`  | 144.468 ms (5%) |         |  122.45 KiB (1%) |        1692 |
| `["findfirst", "n=500", "reduce", "basesize=512"]`  |  82.905 ms (5%) |         |   49.70 KiB (1%) |         675 |
| `["overhead", "default"]`                           |  73.701 μs (5%) |         |   32.70 KiB (1%) |         417 |
| `["overhead", "stoppable=false"]`                   |  70.401 μs (5%) |         |   32.75 KiB (1%) |         418 |
| `["overhead", "stoppable=true"]`                    |  85.501 μs (5%) |         |   44.22 KiB (1%) |         609 |
| `["parallel_histogram", "assoc", "basesize=16384"]` |   3.226 ms (5%) |         |  728.91 KiB (1%) |          57 |
| `["parallel_histogram", "assoc", "basesize=4096"]`  |   3.938 ms (5%) |         |    2.05 MiB (1%) |         222 |
| `["parallel_histogram", "assoc", "basesize=8192"]`  |   3.595 ms (5%) |         |    1.42 MiB (1%) |         117 |
| `["parallel_histogram", "comm", "basesize=16384"]`  |  17.219 ms (5%) |         |    1.58 MiB (1%) |        2367 |
| `["parallel_histogram", "comm", "basesize=4096"]`   |  23.604 ms (5%) |         |    1.23 MiB (1%) |        6462 |
| `["parallel_histogram", "comm", "basesize=8192"]`   |  20.960 ms (5%) |         |    1.31 MiB (1%) |        2724 |
| `["parallel_histogram", "seq"]`                     |   5.772 ms (5%) |         |  364.16 KiB (1%) |          24 |
| `["partition_length_maximum", "rand", "foldl"]`     |  31.042 ms (5%) |         |                  |             |
| `["partition_length_maximum", "rand", "reduce"]`    |  17.541 ms (5%) |         |   736 bytes (1%) |          11 |
| `["splitby", "count", "foldl"]`                     |   2.336 ms (5%) |         |                  |             |
| `["splitby", "count", "man"]`                       |   1.752 ms (5%) |         |                  |             |
| `["splitby", "count", "reduce"]`                    |   1.095 ms (5%) |         |    1.06 KiB (1%) |          19 |
| `["sum", "random", "foldl"]`                        |  14.442 ms (5%) |         |                  |             |
| `["sum", "random", "reduce", "basesize=128"]`       |   7.727 ms (5%) |         |   74.08 KiB (1%) |        1101 |
| `["sum", "random", "reduce", "basesize=256"]`       |   7.637 ms (5%) |         |   36.67 KiB (1%) |         544 |
| `["sum", "random", "reduce", "basesize=512"]`       |   7.570 ms (5%) |         |   18.08 KiB (1%) |         269 |
| `["sum", "uniform", "foldl"]`                       |  15.735 ms (5%) |         |                  |             |
| `["sum", "uniform", "reduce", "basesize=128"]`      |   7.527 ms (5%) |         |   74.14 KiB (1%) |        1103 |
| `["sum", "uniform", "reduce", "basesize=256"]`      |   7.422 ms (5%) |         |   36.77 KiB (1%) |         547 |
| `["sum", "uniform", "reduce", "basesize=512"]`      |   7.359 ms (5%) |         |   18.06 KiB (1%) |         269 |
| `["sum", "valley", "foldl"]`                        |  16.142 ms (5%) |         |                  |             |
| `["sum", "valley", "reduce", "basesize=128"]`       |   8.234 ms (5%) |         |   74.08 KiB (1%) |        1101 |
| `["sum", "valley", "reduce", "basesize=256"]`       |   8.121 ms (5%) |         |   36.67 KiB (1%) |         544 |
| `["sum", "valley", "reduce", "basesize=512"]`       |   8.107 ms (5%) |         |   18.00 KiB (1%) |         267 |
| `["words", "nthreads=1"]`                           |  23.849 ms (5%) |         |   31.85 MiB (1%) |     1038145 |
| `["words", "nthreads=2"]`                           |  14.125 ms (5%) |         |   32.57 MiB (1%) |     1038259 |
| `["words", "nthreads=4"]`                           |  14.621 ms (5%) |         |   33.19 MiB (1%) |     1038398 |

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
Julia Version 1.7.3
Commit 742b9abb4d (2022-05-06 12:58 UTC)
Platform Info:
  OS: Linux (x86_64-pc-linux-gnu)
      Ubuntu 20.04.5 LTS
  uname: Linux 5.15.0-1020-azure #25~20.04.1-Ubuntu SMP Thu Sep 1 19:20:56 UTC 2022 x86_64 x86_64
  CPU: Intel(R) Xeon(R) Platinum 8272CL CPU @ 2.60GHz: 
              speed         user         nice          sys         idle          irq
       #1  2593 MHz       5076 s          0 s        250 s       3526 s          0 s
       #2  2593 MHz       5030 s          0 s        285 s       3539 s          0 s
       
  Memory: 6.781253814697266 GB (3738.08984375 MB free)
  Uptime: 890.03 sec
  Load Avg:  1.66  1.48  0.87
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-12.0.1 (ORCJIT, skylake-avx512)
```

---
# Baseline result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmark: 5 Oct 2022 - 21:11
* Package commit: 958213
* Julia commit: 742b9a
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
| `["collect", "assoc", "basesize=1"]`                | 233.233 ms (5%) |         |   25.97 MiB (1%) |      306861 |
| `["collect", "assoc", "basesize=1024"]`             | 175.288 ms (5%) |         |    2.61 MiB (1%) |         455 |
| `["collect", "assoc", "basesize=32"]`               | 188.309 ms (5%) |         |    4.82 MiB (1%) |       11712 |
| `["collect", "seq"]`                                | 348.659 ms (5%) |         |  812.73 KiB (1%) |          11 |
| `["collect", "unordered", "basesize=1"]`            | 319.542 ms (5%) |         |   23.92 MiB (1%) |      413743 |
| `["collect", "unordered", "basesize=1024"]`         | 187.654 ms (5%) |         | 1002.98 KiB (1%) |         996 |
| `["collect", "unordered", "basesize=32"]`           | 198.417 ms (5%) |         |    1.59 MiB (1%) |       14839 |
| `["findfirst", "n=1000", "foldl"]`                  | 630.394 ms (5%) |         |                  |             |
| `["findfirst", "n=1000", "reduce", "basesize=128"]` | 315.366 ms (5%) |         |  224.61 KiB (1%) |        3163 |
| `["findfirst", "n=1000", "reduce", "basesize=256"]` | 396.050 ms (5%) |         |  151.16 KiB (1%) |        2124 |
| `["findfirst", "n=1000", "reduce", "basesize=512"]` | 460.807 ms (5%) |         |   96.94 KiB (1%) |        1352 |
| `["findfirst", "n=400", "foldl"]`                   | 416.599 ms (5%) |         |                  |             |
| `["findfirst", "n=400", "reduce", "basesize=128"]`  | 226.622 ms (5%) |         |  374.61 KiB (1%) |        5346 |
| `["findfirst", "n=400", "reduce", "basesize=256"]`  | 232.731 ms (5%) |         |  200.09 KiB (1%) |        2864 |
| `["findfirst", "n=400", "reduce", "basesize=512"]`  | 285.111 ms (5%) |         |  132.11 KiB (1%) |        1882 |
| `["findfirst", "n=500", "foldl"]`                   |  72.350 ms (5%) |         |                  |             |
| `["findfirst", "n=500", "reduce", "basesize=128"]`  | 127.471 ms (5%) |         |  209.84 KiB (1%) |        2878 |
| `["findfirst", "n=500", "reduce", "basesize=256"]`  |  62.987 ms (5%) |         |   71.53 KiB (1%) |         978 |
| `["findfirst", "n=500", "reduce", "basesize=512"]`  |  73.858 ms (5%) |         |   49.59 KiB (1%) |         671 |
| `["overhead", "default"]`                           |  76.601 μs (5%) |         |   32.73 KiB (1%) |         418 |
| `["overhead", "stoppable=false"]`                   |  75.401 μs (5%) |         |   32.78 KiB (1%) |         419 |
| `["overhead", "stoppable=true"]`                    |  83.701 μs (5%) |         |   44.28 KiB (1%) |         611 |
| `["parallel_histogram", "assoc", "basesize=16384"]` |   2.851 ms (5%) |         |  728.91 KiB (1%) |          57 |
| `["parallel_histogram", "assoc", "basesize=4096"]`  |   3.503 ms (5%) |         |    2.05 MiB (1%) |         221 |
| `["parallel_histogram", "assoc", "basesize=8192"]`  |   3.169 ms (5%) |         |    1.42 MiB (1%) |         117 |
| `["parallel_histogram", "comm", "basesize=16384"]`  |  16.209 ms (5%) |         |    1.60 MiB (1%) |        3150 |
| `["parallel_histogram", "comm", "basesize=4096"]`   |  21.465 ms (5%) |         |    1.15 MiB (1%) |        3721 |
| `["parallel_histogram", "comm", "basesize=8192"]`   |  22.219 ms (5%) |         |    1.30 MiB (1%) |        5329 |
| `["parallel_histogram", "seq"]`                     |   5.081 ms (5%) |         |  364.16 KiB (1%) |          24 |
| `["partition_length_maximum", "rand", "foldl"]`     |  31.049 ms (5%) |         |                  |             |
| `["partition_length_maximum", "rand", "reduce"]`    |  17.622 ms (5%) |         |   768 bytes (1%) |          12 |
| `["splitby", "count", "foldl"]`                     |   1.930 ms (5%) |         |                  |             |
| `["splitby", "count", "man"]`                       |   1.253 ms (5%) |         |                  |             |
| `["splitby", "count", "reduce"]`                    |   1.098 ms (5%) |         |    1.09 KiB (1%) |          19 |
| `["sum", "random", "foldl"]`                        |  14.103 ms (5%) |         |                  |             |
| `["sum", "random", "reduce", "basesize=128"]`       |   7.204 ms (5%) |         |   74.08 KiB (1%) |        1101 |
| `["sum", "random", "reduce", "basesize=256"]`       |   7.114 ms (5%) |         |   36.73 KiB (1%) |         546 |
| `["sum", "random", "reduce", "basesize=512"]`       |   7.066 ms (5%) |         |   18.11 KiB (1%) |         270 |
| `["sum", "uniform", "foldl"]`                       |  13.816 ms (5%) |         |                  |             |
| `["sum", "uniform", "reduce", "basesize=128"]`      |   7.067 ms (5%) |         |   74.08 KiB (1%) |        1101 |
| `["sum", "uniform", "reduce", "basesize=256"]`      |   6.960 ms (5%) |         |   36.70 KiB (1%) |         545 |
| `["sum", "uniform", "reduce", "basesize=512"]`      |   6.910 ms (5%) |         |   18.03 KiB (1%) |         268 |
| `["sum", "valley", "foldl"]`                        |  14.274 ms (5%) |         |                  |             |
| `["sum", "valley", "reduce", "basesize=128"]`       |   7.719 ms (5%) |         |   74.05 KiB (1%) |        1100 |
| `["sum", "valley", "reduce", "basesize=256"]`       |   7.208 ms (5%) |         |   36.73 KiB (1%) |         546 |
| `["sum", "valley", "reduce", "basesize=512"]`       |   7.168 ms (5%) |         |   18.06 KiB (1%) |         269 |
| `["words", "nthreads=1"]`                           |  20.731 ms (5%) |         |   31.59 MiB (1%) |     1028966 |
| `["words", "nthreads=2"]`                           |  12.971 ms (5%) |         |   31.94 MiB (1%) |     1029026 |
| `["words", "nthreads=4"]`                           |  13.092 ms (5%) |         |   32.66 MiB (1%) |     1029132 |

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
Julia Version 1.7.3
Commit 742b9abb4d (2022-05-06 12:58 UTC)
Platform Info:
  OS: Linux (x86_64-pc-linux-gnu)
      Ubuntu 20.04.5 LTS
  uname: Linux 5.15.0-1020-azure #25~20.04.1-Ubuntu SMP Thu Sep 1 19:20:56 UTC 2022 x86_64 x86_64
  CPU: Intel(R) Xeon(R) Platinum 8272CL CPU @ 2.60GHz: 
              speed         user         nice          sys         idle          irq
       #1  2593 MHz       7420 s          0 s        290 s       4060 s          0 s
       #2  2593 MHz       7239 s          0 s        317 s       4215 s          0 s
       
  Memory: 6.781253814697266 GB (3751.6328125 MB free)
  Uptime: 1182.24 sec
  Load Avg:  1.66  1.58  1.09
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-12.0.1 (ORCJIT, skylake-avx512)
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
    CPU MHz:                         2593.907
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
    Vulnerability Mmio stale data:   Vulnerable: Clear CPU buffers attempted, no microcode; SMT Host state unknown
    Vulnerability Retbleed:          Vulnerable
    Vulnerability Spec store bypass: Vulnerable
    Vulnerability Spectre v1:        Mitigation; usercopy/swapgs barriers and __user pointer sanitization
    Vulnerability Spectre v2:        Mitigation; Retpolines, STIBP disabled, RSB filling
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

