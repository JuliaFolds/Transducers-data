# Multi-thread benchmark result

* Pull request commit: [`acc2016a1aceb24533519e0c8918db913e2dd457`](https://github.com/JuliaFolds/Transducers.jl/commit/acc2016a1aceb24533519e0c8918db913e2dd457)
* Pull request: <https://github.com/JuliaFolds/Transducers.jl/pull/243> (Update */Manifest.toml)

# Judge result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmarks:
    - Target: 25 Jan 2023 - 01:45
    - Baseline: 25 Jan 2023 - 01:50
* Package commits:
    - Target: 003716
    - Baseline: f8d0df
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
| `["findfirst", "n=1000", "reduce", "basesize=128"]` | 0.84 (5%) :white_check_mark: | 0.85 (1%) :white_check_mark: |
| `["findfirst", "n=1000", "reduce", "basesize=256"]` |                1.20 (5%) :x: |                1.26 (1%) :x: |
| `["findfirst", "n=1000", "reduce", "basesize=512"]` |                1.75 (5%) :x: |                1.68 (1%) :x: |
| `["findfirst", "n=400", "reduce", "basesize=512"]`  | 0.75 (5%) :white_check_mark: | 0.75 (1%) :white_check_mark: |
| `["findfirst", "n=500", "reduce", "basesize=128"]`  |                1.40 (5%) :x: |                1.37 (1%) :x: |
| `["findfirst", "n=500", "reduce", "basesize=256"]`  |                2.47 (5%) :x: |                1.87 (1%) :x: |
| `["findfirst", "n=500", "reduce", "basesize=512"]`  |                   1.01 (5%)  |                1.03 (1%) :x: |
| `["overhead", "stoppable=true"]`                    |                1.05 (5%) :x: |                   1.00 (1%)  |
| `["parallel_histogram", "comm", "basesize=16384"]`  |                1.08 (5%) :x: |                1.01 (1%) :x: |
| `["parallel_histogram", "comm", "basesize=4096"]`   |                   1.01 (5%)  |                1.06 (1%) :x: |
| `["parallel_histogram", "comm", "basesize=8192"]`   | 0.80 (5%) :white_check_mark: | 0.85 (1%) :white_check_mark: |
| `["splitby", "count", "reduce"]`                    |                1.06 (5%) :x: |                   1.00 (1%)  |
| `["words", "nthreads=2"]`                           |                1.05 (5%) :x: |                   1.01 (1%)  |
| `["words", "nthreads=4"]`                           |                1.06 (5%) :x: |                   1.01 (1%)  |

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
      Ubuntu 22.04.1 LTS
  uname: Linux 5.15.0-1031-azure #38-Ubuntu SMP Mon Jan 9 12:49:59 UTC 2023 x86_64 x86_64
  CPU: Intel(R) Xeon(R) Platinum 8370C CPU @ 2.80GHz: 
              speed         user         nice          sys         idle          irq
       #1  2793 MHz       4948 s          0 s        219 s       2746 s          0 s
       #2  2793 MHz       5436 s          0 s        245 s       2228 s          0 s
       
  Memory: 6.781219482421875 GB (3707.41796875 MB free)
  Uptime: 795.62 sec
  Load Avg:  1.64  1.49  0.9
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-12.0.1 (ORCJIT, icelake-server)
```

### Baseline
```
Julia Version 1.7.3
Commit 742b9abb4d (2022-05-06 12:58 UTC)
Platform Info:
  OS: Linux (x86_64-pc-linux-gnu)
      Ubuntu 22.04.1 LTS
  uname: Linux 5.15.0-1031-azure #38-Ubuntu SMP Mon Jan 9 12:49:59 UTC 2023 x86_64 x86_64
  CPU: Intel(R) Xeon(R) Platinum 8370C CPU @ 2.80GHz: 
              speed         user         nice          sys         idle          irq
       #1  2793 MHz       7306 s          0 s        284 s       3381 s          0 s
       #2  2793 MHz       7840 s          0 s        294 s       2839 s          0 s
       
  Memory: 6.781219482421875 GB (3431.79296875 MB free)
  Uptime: 1102.16 sec
  Load Avg:  1.79  1.63  1.13
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-12.0.1 (ORCJIT, icelake-server)
```

---
# Target result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmark: 25 Jan 2023 - 1:45
* Package commit: 003716
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

| ID                                                  | time            | GC time | memory          | allocations |
|-----------------------------------------------------|----------------:|--------:|----------------:|------------:|
| `["collect", "assoc", "basesize=1"]`                | 279.451 ms (5%) |         |  25.97 MiB (1%) |      306789 |
| `["collect", "assoc", "basesize=1024"]`             | 239.143 ms (5%) |         |   2.61 MiB (1%) |         454 |
| `["collect", "assoc", "basesize=32"]`               | 241.417 ms (5%) |         |   4.82 MiB (1%) |       11717 |
| `["collect", "seq"]`                                | 477.578 ms (5%) |         | 812.73 KiB (1%) |          11 |
| `["collect", "unordered", "basesize=1"]`            | 374.854 ms (5%) |         |  23.89 MiB (1%) |      412716 |
| `["collect", "unordered", "basesize=1024"]`         | 250.998 ms (5%) |         |   1.01 MiB (1%) |         974 |
| `["collect", "unordered", "basesize=32"]`           | 260.988 ms (5%) |         |   1.59 MiB (1%) |       14975 |
| `["findfirst", "n=1000", "foldl"]`                  | 736.776 ms (5%) |         |                 |             |
| `["findfirst", "n=1000", "reduce", "basesize=128"]` | 406.308 ms (5%) |         | 232.86 KiB (1%) |        3276 |
| `["findfirst", "n=1000", "reduce", "basesize=256"]` | 670.033 ms (5%) |         | 209.59 KiB (1%) |        2931 |
| `["findfirst", "n=1000", "reduce", "basesize=512"]` | 880.842 ms (5%) |         | 136.66 KiB (1%) |        1903 |
| `["findfirst", "n=400", "foldl"]`                   | 552.690 ms (5%) |         |                 |             |
| `["findfirst", "n=400", "reduce", "basesize=128"]`  | 297.629 ms (5%) |         | 382.30 KiB (1%) |        5444 |
| `["findfirst", "n=400", "reduce", "basesize=256"]`  | 293.382 ms (5%) |         | 200.86 KiB (1%) |        2873 |
| `["findfirst", "n=400", "reduce", "basesize=512"]`  | 322.529 ms (5%) |         | 112.59 KiB (1%) |        1622 |
| `["findfirst", "n=500", "foldl"]`                   |  95.768 ms (5%) |         |                 |             |
| `["findfirst", "n=500", "reduce", "basesize=128"]`  | 268.771 ms (5%) |         | 307.61 KiB (1%) |        4288 |
| `["findfirst", "n=500", "reduce", "basesize=256"]`  | 232.431 ms (5%) |         | 148.09 KiB (1%) |        2081 |
| `["findfirst", "n=500", "reduce", "basesize=512"]`  | 137.151 ms (5%) |         |  61.61 KiB (1%) |         844 |
| `["overhead", "default"]`                           |  72.200 μs (5%) |         |  32.73 KiB (1%) |         418 |
| `["overhead", "stoppable=false"]`                   |  71.300 μs (5%) |         |  32.75 KiB (1%) |         418 |
| `["overhead", "stoppable=true"]`                    |  81.600 μs (5%) |         |  44.28 KiB (1%) |         611 |
| `["parallel_histogram", "assoc", "basesize=16384"]` |   3.718 ms (5%) |         | 728.91 KiB (1%) |          57 |
| `["parallel_histogram", "assoc", "basesize=4096"]`  |   4.490 ms (5%) |         |   1.79 MiB (1%) |         216 |
| `["parallel_histogram", "assoc", "basesize=8192"]`  |   4.099 ms (5%) |         |   1.42 MiB (1%) |         117 |
| `["parallel_histogram", "comm", "basesize=16384"]`  |  15.395 ms (5%) |         |   1.67 MiB (1%) |        5519 |
| `["parallel_histogram", "comm", "basesize=4096"]`   |  23.966 ms (5%) |         |   1.39 MiB (1%) |       11756 |
| `["parallel_histogram", "comm", "basesize=8192"]`   |  16.801 ms (5%) |         |   1.16 MiB (1%) |        4087 |
| `["parallel_histogram", "seq"]`                     |   6.693 ms (5%) |         | 364.16 KiB (1%) |          24 |
| `["partition_length_maximum", "rand", "foldl"]`     |  41.192 ms (5%) |         |                 |             |
| `["partition_length_maximum", "rand", "reduce"]`    |  20.606 ms (5%) |         |  736 bytes (1%) |          11 |
| `["splitby", "count", "foldl"]`                     |   2.378 ms (5%) |         |                 |             |
| `["splitby", "count", "man"]`                       |   1.528 ms (5%) |         |                 |             |
| `["splitby", "count", "reduce"]`                    |   1.163 ms (5%) |         |   1.06 KiB (1%) |          19 |
| `["sum", "random", "foldl"]`                        |  17.997 ms (5%) |         |                 |             |
| `["sum", "random", "reduce", "basesize=128"]`       |   9.191 ms (5%) |         |  74.20 KiB (1%) |        1105 |
| `["sum", "random", "reduce", "basesize=256"]`       |   9.098 ms (5%) |         |  36.80 KiB (1%) |         548 |
| `["sum", "random", "reduce", "basesize=512"]`       |   9.042 ms (5%) |         |  18.08 KiB (1%) |         269 |
| `["sum", "uniform", "foldl"]`                       |  17.727 ms (5%) |         |                 |             |
| `["sum", "uniform", "reduce", "basesize=128"]`      |   9.056 ms (5%) |         |  74.20 KiB (1%) |        1105 |
| `["sum", "uniform", "reduce", "basesize=256"]`      |   8.959 ms (5%) |         |  36.70 KiB (1%) |         545 |
| `["sum", "uniform", "reduce", "basesize=512"]`      |   8.910 ms (5%) |         |  18.03 KiB (1%) |         268 |
| `["sum", "valley", "foldl"]`                        |  18.139 ms (5%) |         |                 |             |
| `["sum", "valley", "reduce", "basesize=128"]`       |   9.266 ms (5%) |         |  74.14 KiB (1%) |        1103 |
| `["sum", "valley", "reduce", "basesize=256"]`       |   9.177 ms (5%) |         |  36.70 KiB (1%) |         545 |
| `["sum", "valley", "reduce", "basesize=512"]`       |   9.184 ms (5%) |         |  18.00 KiB (1%) |         267 |
| `["words", "nthreads=1"]`                           |  18.489 ms (5%) |         |  31.75 MiB (1%) |     1033777 |
| `["words", "nthreads=2"]`                           |  12.716 ms (5%) |         |  32.46 MiB (1%) |     1033873 |
| `["words", "nthreads=4"]`                           |  13.429 ms (5%) |         |  33.09 MiB (1%) |     1034017 |

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
      Ubuntu 22.04.1 LTS
  uname: Linux 5.15.0-1031-azure #38-Ubuntu SMP Mon Jan 9 12:49:59 UTC 2023 x86_64 x86_64
  CPU: Intel(R) Xeon(R) Platinum 8370C CPU @ 2.80GHz: 
              speed         user         nice          sys         idle          irq
       #1  2793 MHz       4948 s          0 s        219 s       2746 s          0 s
       #2  2793 MHz       5436 s          0 s        245 s       2228 s          0 s
       
  Memory: 6.781219482421875 GB (3707.41796875 MB free)
  Uptime: 795.62 sec
  Load Avg:  1.64  1.49  0.9
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-12.0.1 (ORCJIT, icelake-server)
```

---
# Baseline result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmark: 25 Jan 2023 - 1:50
* Package commit: f8d0df
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

| ID                                                  | time            | GC time | memory          | allocations |
|-----------------------------------------------------|----------------:|--------:|----------------:|------------:|
| `["collect", "assoc", "basesize=1"]`                | 279.191 ms (5%) |         |  25.97 MiB (1%) |      306874 |
| `["collect", "assoc", "basesize=1024"]`             | 239.826 ms (5%) |         |   2.61 MiB (1%) |         457 |
| `["collect", "assoc", "basesize=32"]`               | 241.306 ms (5%) |         |   4.82 MiB (1%) |       11714 |
| `["collect", "seq"]`                                | 478.039 ms (5%) |         | 812.73 KiB (1%) |          11 |
| `["collect", "unordered", "basesize=1"]`            | 369.572 ms (5%) |         |  23.93 MiB (1%) |      413871 |
| `["collect", "unordered", "basesize=1024"]`         | 250.446 ms (5%) |         |   1.01 MiB (1%) |        1028 |
| `["collect", "unordered", "basesize=32"]`           | 260.766 ms (5%) |         |   1.59 MiB (1%) |       14933 |
| `["findfirst", "n=1000", "foldl"]`                  | 736.541 ms (5%) |         |                 |             |
| `["findfirst", "n=1000", "reduce", "basesize=128"]` | 481.441 ms (5%) |         | 274.92 KiB (1%) |        3845 |
| `["findfirst", "n=1000", "reduce", "basesize=256"]` | 556.125 ms (5%) |         | 166.38 KiB (1%) |        2330 |
| `["findfirst", "n=1000", "reduce", "basesize=512"]` | 504.700 ms (5%) |         |  81.42 KiB (1%) |        1149 |
| `["findfirst", "n=400", "foldl"]`                   | 553.001 ms (5%) |         |                 |             |
| `["findfirst", "n=400", "reduce", "basesize=128"]`  | 294.316 ms (5%) |         | 386.08 KiB (1%) |        5486 |
| `["findfirst", "n=400", "reduce", "basesize=256"]`  | 292.807 ms (5%) |         | 201.05 KiB (1%) |        2879 |
| `["findfirst", "n=400", "reduce", "basesize=512"]`  | 430.186 ms (5%) |         | 149.92 KiB (1%) |        2147 |
| `["findfirst", "n=500", "foldl"]`                   |  95.832 ms (5%) |         |                 |             |
| `["findfirst", "n=500", "reduce", "basesize=128"]`  | 191.517 ms (5%) |         | 224.81 KiB (1%) |        3134 |
| `["findfirst", "n=500", "reduce", "basesize=256"]`  |  94.167 ms (5%) |         |  79.16 KiB (1%) |        1070 |
| `["findfirst", "n=500", "reduce", "basesize=512"]`  | 135.665 ms (5%) |         |  59.80 KiB (1%) |         817 |
| `["overhead", "default"]`                           |  69.900 μs (5%) |         |  32.73 KiB (1%) |         418 |
| `["overhead", "stoppable=false"]`                   |  70.900 μs (5%) |         |  32.78 KiB (1%) |         419 |
| `["overhead", "stoppable=true"]`                    |  77.600 μs (5%) |         |  44.25 KiB (1%) |         610 |
| `["parallel_histogram", "assoc", "basesize=16384"]` |   3.724 ms (5%) |         | 728.91 KiB (1%) |          57 |
| `["parallel_histogram", "assoc", "basesize=4096"]`  |   4.485 ms (5%) |         |   1.79 MiB (1%) |         215 |
| `["parallel_histogram", "assoc", "basesize=8192"]`  |   4.107 ms (5%) |         |   1.42 MiB (1%) |         117 |
| `["parallel_histogram", "comm", "basesize=16384"]`  |  14.282 ms (5%) |         |   1.65 MiB (1%) |        4751 |
| `["parallel_histogram", "comm", "basesize=4096"]`   |  23.809 ms (5%) |         |   1.31 MiB (1%) |        9037 |
| `["parallel_histogram", "comm", "basesize=8192"]`   |  20.925 ms (5%) |         |   1.35 MiB (1%) |        9518 |
| `["parallel_histogram", "seq"]`                     |   6.703 ms (5%) |         | 364.16 KiB (1%) |          24 |
| `["partition_length_maximum", "rand", "foldl"]`     |  41.189 ms (5%) |         |                 |             |
| `["partition_length_maximum", "rand", "reduce"]`    |  20.612 ms (5%) |         |  736 bytes (1%) |          11 |
| `["splitby", "count", "foldl"]`                     |   2.351 ms (5%) |         |                 |             |
| `["splitby", "count", "man"]`                       |   1.528 ms (5%) |         |                 |             |
| `["splitby", "count", "reduce"]`                    |   1.099 ms (5%) |         |   1.06 KiB (1%) |          18 |
| `["sum", "random", "foldl"]`                        |  18.031 ms (5%) |         |                 |             |
| `["sum", "random", "reduce", "basesize=128"]`       |   9.156 ms (5%) |         |  74.17 KiB (1%) |        1104 |
| `["sum", "random", "reduce", "basesize=256"]`       |   9.121 ms (5%) |         |  36.73 KiB (1%) |         546 |
| `["sum", "random", "reduce", "basesize=512"]`       |   9.066 ms (5%) |         |  18.11 KiB (1%) |         270 |
| `["sum", "uniform", "foldl"]`                       |  17.728 ms (5%) |         |                 |             |
| `["sum", "uniform", "reduce", "basesize=128"]`      |   9.035 ms (5%) |         |  74.17 KiB (1%) |        1104 |
| `["sum", "uniform", "reduce", "basesize=256"]`      |   8.964 ms (5%) |         |  36.77 KiB (1%) |         547 |
| `["sum", "uniform", "reduce", "basesize=512"]`      |   8.902 ms (5%) |         |  18.00 KiB (1%) |         267 |
| `["sum", "valley", "foldl"]`                        |  18.142 ms (5%) |         |                 |             |
| `["sum", "valley", "reduce", "basesize=128"]`       |   9.258 ms (5%) |         |  74.14 KiB (1%) |        1103 |
| `["sum", "valley", "reduce", "basesize=256"]`       |   9.194 ms (5%) |         |  36.70 KiB (1%) |         545 |
| `["sum", "valley", "reduce", "basesize=512"]`       |   9.208 ms (5%) |         |  18.00 KiB (1%) |         267 |
| `["words", "nthreads=1"]`                           |  18.406 ms (5%) |         |  31.47 MiB (1%) |     1025445 |
| `["words", "nthreads=2"]`                           |  12.079 ms (5%) |         |  32.18 MiB (1%) |     1025565 |
| `["words", "nthreads=4"]`                           |  12.722 ms (5%) |         |  32.81 MiB (1%) |     1025700 |

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
      Ubuntu 22.04.1 LTS
  uname: Linux 5.15.0-1031-azure #38-Ubuntu SMP Mon Jan 9 12:49:59 UTC 2023 x86_64 x86_64
  CPU: Intel(R) Xeon(R) Platinum 8370C CPU @ 2.80GHz: 
              speed         user         nice          sys         idle          irq
       #1  2793 MHz       7306 s          0 s        284 s       3381 s          0 s
       #2  2793 MHz       7840 s          0 s        294 s       2839 s          0 s
       
  Memory: 6.781219482421875 GB (3431.79296875 MB free)
  Uptime: 1102.16 sec
  Load Avg:  1.79  1.63  1.13
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-12.0.1 (ORCJIT, icelake-server)
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
    Address sizes:                   46 bits physical, 48 bits virtual
    Byte Order:                      Little Endian
    CPU(s):                          2
    On-line CPU(s) list:             0,1
    Vendor ID:                       GenuineIntel
    Model name:                      Intel(R) Xeon(R) Platinum 8370C CPU @ 2.80GHz
    CPU family:                      6
    Model:                           106
    Thread(s) per core:              1
    Core(s) per socket:              2
    Socket(s):                       1
    Stepping:                        6
    BogoMIPS:                        5586.87
    Flags:                           fpu vme de pse tsc msr pae mce cx8 apic sep mtrr pge mca cmov pat pse36 clflush mmx fxsr sse sse2 ss ht syscall nx pdpe1gb rdtscp lm constant_tsc rep_good nopl xtopology cpuid pni pclmulqdq ssse3 fma cx16 pcid sse4_1 sse4_2 movbe popcnt aes xsave avx f16c rdrand hypervisor lahf_lm abm 3dnowprefetch invpcid_single pti fsgsbase bmi1 hle avx2 smep bmi2 erms invpcid rtm avx512f avx512dq rdseed adx smap clflushopt avx512cd avx512bw avx512vl xsaveopt xsavec xsaves md_clear
    Hypervisor vendor:               Microsoft
    Virtualization type:             full
    L1d cache:                       96 KiB (2 instances)
    L1i cache:                       64 KiB (2 instances)
    L2 cache:                        2.5 MiB (2 instances)
    L3 cache:                        48 MiB (1 instance)
    NUMA node(s):                    1
    NUMA node0 CPU(s):               0,1
    Vulnerability Itlb multihit:     KVM: Mitigation: VMX unsupported
    Vulnerability L1tf:              Mitigation; PTE Inversion
    Vulnerability Mds:               Mitigation; Clear CPU buffers; SMT Host state unknown
    Vulnerability Meltdown:          Mitigation; PTI
    Vulnerability Mmio stale data:   Vulnerable: Clear CPU buffers attempted, no microcode; SMT Host state unknown
    Vulnerability Retbleed:          Not affected
    Vulnerability Spec store bypass: Vulnerable
    Vulnerability Spectre v1:        Mitigation; usercopy/swapgs barriers and __user pointer sanitization
    Vulnerability Spectre v2:        Mitigation; Retpolines, STIBP disabled, RSB filling, PBRSB-eIBRS Not affected
    Vulnerability Srbds:             Not affected
    Vulnerability Tsx async abort:   Mitigation; Clear CPU buffers; SMT Host state unknown
    

| Cpu Property       | Value                                                   |
|:------------------ |:------------------------------------------------------- |
| Brand              | Intel(R) Xeon(R) Platinum 8370C CPU @ 2.80GHz           |
| Vendor             | :Intel                                                  |
| Architecture       | :UnknownIntel                                           |
| Model              | Family: 0x06, Model: 0x6a, Stepping: 0x06, Type: 0x00   |
| Cores              | 2 physical cores, 2 logical cores (on executing CPU)    |
|                    | No Hyperthreading hardware capability detected          |
| Clock Frequencies  | Not supported by CPU                                    |
| Data Cache         | Level 1:3 : (48, 1280, 49152) kbytes                    |
|                    | 64 byte cache line size                                 |
| Address Size       | 48 bits virtual, 46 bits physical                       |
| SIMD               | 512 bit = 64 byte max. SIMD vector size                 |
| Time Stamp Counter | TSC is accessible via `rdtsc`                           |
|                    | TSC increased at every clock cycle (non-invariant TSC)  |
| Perf. Monitoring   | Performance Monitoring Counters (PMC) are not supported |
| Hypervisor         | Yes, Microsoft                                          |

