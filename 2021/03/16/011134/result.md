# Multi-thread benchmark result

* Pull request commit: [`6c70e1ede631cea9e0bdb8b85eaa16446354e066`](https://github.com/JuliaFolds/Transducers.jl/commit/6c70e1ede631cea9e0bdb8b85eaa16446354e066)
* Pull request: <https://github.com/JuliaFolds/Transducers.jl/pull/243> (Update */Manifest.toml)

# Judge result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmarks:
    - Target: 16 Mar 2021 - 01:05
    - Baseline: 16 Mar 2021 - 01:11
* Package commits:
    - Target: aea6bd
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
| `["collect", "assoc", "basesize=32"]`               |                1.06 (5%) :x: |                   1.00 (1%)  |
| `["collect", "unordered", "basesize=1"]`            |                1.07 (5%) :x: |                   1.00 (1%)  |
| `["collect", "unordered", "basesize=1024"]`         | 0.92 (5%) :white_check_mark: | 0.94 (1%) :white_check_mark: |
| `["findfirst", "n=1000", "reduce", "basesize=128"]` |                1.06 (5%) :x: |                1.07 (1%) :x: |
| `["findfirst", "n=1000", "reduce", "basesize=256"]` | 0.80 (5%) :white_check_mark: | 0.84 (1%) :white_check_mark: |
| `["findfirst", "n=1000", "reduce", "basesize=512"]` |                   1.05 (5%)  |                1.05 (1%) :x: |
| `["findfirst", "n=400", "reduce", "basesize=128"]`  |                1.09 (5%) :x: |                   1.01 (1%)  |
| `["findfirst", "n=400", "reduce", "basesize=256"]`  |                   1.01 (5%)  | 0.97 (1%) :white_check_mark: |
| `["findfirst", "n=400", "reduce", "basesize=512"]`  |                1.05 (5%) :x: |                1.06 (1%) :x: |
| `["findfirst", "n=500", "reduce", "basesize=128"]`  |                1.58 (5%) :x: |                1.47 (1%) :x: |
| `["findfirst", "n=500", "reduce", "basesize=256"]`  | 0.92 (5%) :white_check_mark: | 0.85 (1%) :white_check_mark: |
| `["findfirst", "n=500", "reduce", "basesize=512"]`  | 0.67 (5%) :white_check_mark: | 0.80 (1%) :white_check_mark: |
| `["parallel_histogram", "assoc", "basesize=4096"]`  |                1.07 (5%) :x: |                1.15 (1%) :x: |
| `["parallel_histogram", "comm", "basesize=4096"]`   |                   0.98 (5%)  | 0.97 (1%) :white_check_mark: |
| `["parallel_histogram", "comm", "basesize=8192"]`   |                1.15 (5%) :x: |                   1.01 (1%)  |
| `["parallel_histogram", "seq"]`                     |                1.09 (5%) :x: |                   1.00 (1%)  |
| `["splitby", "count", "man"]`                       |                1.20 (5%) :x: |                   1.00 (1%)  |
| `["splitby", "count", "reduce"]`                    |                   1.00 (5%)  | 0.99 (1%) :white_check_mark: |
| `["sum", "uniform", "reduce", "basesize=128"]`      | 0.95 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["sum", "valley", "reduce", "basesize=512"]`       | 0.95 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["words", "nthreads=2"]`                           |                1.05 (5%) :x: |                   0.99 (1%)  |

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
  CPU: Intel(R) Xeon(R) CPU E5-2673 v4 @ 2.30GHz: 
              speed         user         nice          sys         idle          irq
       #1  2294 MHz      54476 s         12 s       2434 s      20937 s          0 s
       #2  2294 MHz      55701 s         12 s       2537 s      19578 s          0 s
       
  Memory: 6.7913818359375 GB (3358.1015625 MB free)
  Uptime: 795.0 sec
  Load Avg:  1.66357421875  1.54248046875  0.98681640625
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
  uname: Linux 5.4.0-1040-azure #42-Ubuntu SMP Fri Feb 5 15:39:06 UTC 2021 x86_64 x86_64
  CPU: Intel(R) Xeon(R) CPU E5-2673 v4 @ 2.30GHz: 
              speed         user         nice          sys         idle          irq
       #1  2294 MHz      82494 s         12 s       3096 s      26245 s          0 s
       #2  2294 MHz      78284 s         12 s       3214 s      30345 s          0 s
       
  Memory: 6.7913818359375 GB (3361.609375 MB free)
  Uptime: 1137.0 sec
  Load Avg:  1.63037109375  1.55615234375  1.1591796875
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-9.0.1 (ORCJIT, broadwell)
```

---
# Target result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmark: 16 Mar 2021 - 1:5
* Package commit: aea6bd
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
| `["collect", "assoc", "basesize=1"]`                | 229.941 ms (5%) |         |   32.66 MiB (1%) |      286772 |
| `["collect", "assoc", "basesize=1024"]`             | 170.497 ms (5%) |         |    1.79 MiB (1%) |         570 |
| `["collect", "assoc", "basesize=32"]`               | 181.681 ms (5%) |         |    3.97 MiB (1%) |       13305 |
| `["collect", "seq"]`                                | 331.081 ms (5%) |         |  512.72 KiB (1%) |          15 |
| `["collect", "unordered", "basesize=1"]`            | 433.632 ms (5%) |         |   30.01 MiB (1%) |      360676 |
| `["collect", "unordered", "basesize=1024"]`         | 271.725 ms (5%) |         |  908.55 KiB (1%) |        5795 |
| `["collect", "unordered", "basesize=32"]`           | 205.112 ms (5%) |         |    1.47 MiB (1%) |       12592 |
| `["findfirst", "n=1000", "foldl"]`                  | 561.390 ms (5%) |         |                  |             |
| `["findfirst", "n=1000", "reduce", "basesize=128"]` | 391.276 ms (5%) |         |  832.61 KiB (1%) |       14568 |
| `["findfirst", "n=1000", "reduce", "basesize=256"]` | 370.189 ms (5%) |         |  461.78 KiB (1%) |        8090 |
| `["findfirst", "n=1000", "reduce", "basesize=512"]` | 566.729 ms (5%) |         |  352.30 KiB (1%) |        6188 |
| `["findfirst", "n=400", "foldl"]`                   | 420.093 ms (5%) |         |                  |             |
| `["findfirst", "n=400", "reduce", "basesize=128"]`  | 244.817 ms (5%) |         |    1.09 MiB (1%) |       19691 |
| `["findfirst", "n=400", "reduce", "basesize=256"]`  | 238.324 ms (5%) |         |  591.03 KiB (1%) |       10434 |
| `["findfirst", "n=400", "reduce", "basesize=512"]`  | 271.345 ms (5%) |         |  375.66 KiB (1%) |        6617 |
| `["findfirst", "n=500", "foldl"]`                   |  64.879 ms (5%) |         |                  |             |
| `["findfirst", "n=500", "reduce", "basesize=128"]`  | 197.609 ms (5%) |         |  941.84 KiB (1%) |       16479 |
| `["findfirst", "n=500", "reduce", "basesize=256"]`  | 102.816 ms (5%) |         |  297.19 KiB (1%) |        5189 |
| `["findfirst", "n=500", "reduce", "basesize=512"]`  | 114.794 ms (5%) |         |  220.00 KiB (1%) |        3828 |
| `["overhead", "default"]`                           |  61.901 μs (5%) |         |   47.36 KiB (1%) |         382 |
| `["overhead", "stoppable=false"]`                   |  59.100 μs (5%) |         |   47.39 KiB (1%) |         382 |
| `["overhead", "stoppable=true"]`                    | 164.001 μs (5%) |         |  139.67 KiB (1%) |        2464 |
| `["parallel_histogram", "assoc", "basesize=16384"]` |   3.405 ms (5%) |         |  730.06 KiB (1%) |          57 |
| `["parallel_histogram", "assoc", "basesize=4096"]`  |   4.327 ms (5%) |         |    2.06 MiB (1%) |         219 |
| `["parallel_histogram", "assoc", "basesize=8192"]`  |   3.736 ms (5%) |         |    1.43 MiB (1%) |         117 |
| `["parallel_histogram", "comm", "basesize=16384"]`  |  13.063 ms (5%) |         |    1.02 MiB (1%) |         329 |
| `["parallel_histogram", "comm", "basesize=4096"]`   |  22.260 ms (5%) |         | 1020.88 KiB (1%) |         940 |
| `["parallel_histogram", "comm", "basesize=8192"]`   |  20.079 ms (5%) |         |    1.26 MiB (1%) |        1479 |
| `["parallel_histogram", "seq"]`                     |   6.470 ms (5%) |         |  364.61 KiB (1%) |          24 |
| `["partition_length_maximum", "rand", "foldl"]`     |  32.986 ms (5%) |         |                  |             |
| `["partition_length_maximum", "rand", "reduce"]`    |  16.710 ms (5%) |         |    2.66 KiB (1%) |          48 |
| `["splitby", "count", "foldl"]`                     |   3.716 ms (5%) |         |    96 bytes (1%) |           4 |
| `["splitby", "count", "man"]`                       |   1.745 ms (5%) |         |                  |             |
| `["splitby", "count", "reduce"]`                    | 812.104 μs (5%) |         |    2.84 KiB (1%) |          54 |
| `["sum", "random", "foldl"]`                        |  12.214 ms (5%) |         |    32 bytes (1%) |           2 |
| `["sum", "random", "reduce", "basesize=128"]`       |   6.444 ms (5%) |         |  103.23 KiB (1%) |        1018 |
| `["sum", "random", "reduce", "basesize=256"]`       |   6.392 ms (5%) |         |   51.23 KiB (1%) |         506 |
| `["sum", "random", "reduce", "basesize=512"]`       |   6.319 ms (5%) |         |   25.30 KiB (1%) |         252 |
| `["sum", "uniform", "foldl"]`                       |  11.952 ms (5%) |         |    32 bytes (1%) |           2 |
| `["sum", "uniform", "reduce", "basesize=128"]`      |   6.286 ms (5%) |         |  103.23 KiB (1%) |        1018 |
| `["sum", "uniform", "reduce", "basesize=256"]`      |   6.199 ms (5%) |         |   51.23 KiB (1%) |         506 |
| `["sum", "uniform", "reduce", "basesize=512"]`      |   6.108 ms (5%) |         |   25.25 KiB (1%) |         251 |
| `["sum", "valley", "foldl"]`                        |  12.488 ms (5%) |         |    32 bytes (1%) |           2 |
| `["sum", "valley", "reduce", "basesize=128"]`       |   6.516 ms (5%) |         |  103.23 KiB (1%) |        1018 |
| `["sum", "valley", "reduce", "basesize=256"]`       |   6.483 ms (5%) |         |   51.23 KiB (1%) |         506 |
| `["sum", "valley", "reduce", "basesize=512"]`       |   6.403 ms (5%) |         |   25.25 KiB (1%) |         251 |
| `["words", "nthreads=1"]`                           |  25.270 ms (5%) |         |   31.58 MiB (1%) |     1028310 |
| `["words", "nthreads=2"]`                           |  15.262 ms (5%) |         |   31.94 MiB (1%) |     1028346 |
| `["words", "nthreads=4"]`                           |  15.953 ms (5%) |         |   32.84 MiB (1%) |     1028499 |

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
  CPU: Intel(R) Xeon(R) CPU E5-2673 v4 @ 2.30GHz: 
              speed         user         nice          sys         idle          irq
       #1  2294 MHz      54476 s         12 s       2434 s      20937 s          0 s
       #2  2294 MHz      55701 s         12 s       2537 s      19578 s          0 s
       
  Memory: 6.7913818359375 GB (3358.1015625 MB free)
  Uptime: 795.0 sec
  Load Avg:  1.66357421875  1.54248046875  0.98681640625
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-9.0.1 (ORCJIT, broadwell)
```

---
# Baseline result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmark: 16 Mar 2021 - 1:11
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
| `["collect", "assoc", "basesize=1"]`                | 219.395 ms (5%) |         |  32.66 MiB (1%) |      286764 |
| `["collect", "assoc", "basesize=1024"]`             | 170.726 ms (5%) |         |   1.79 MiB (1%) |         570 |
| `["collect", "assoc", "basesize=32"]`               | 172.137 ms (5%) |         |   3.97 MiB (1%) |       13306 |
| `["collect", "seq"]`                                | 338.360 ms (5%) |         | 512.72 KiB (1%) |          15 |
| `["collect", "unordered", "basesize=1"]`            | 406.054 ms (5%) |         |  30.01 MiB (1%) |      360593 |
| `["collect", "unordered", "basesize=1024"]`         | 295.799 ms (5%) |         | 967.05 KiB (1%) |        7685 |
| `["collect", "unordered", "basesize=32"]`           | 205.487 ms (5%) |         |   1.48 MiB (1%) |       12738 |
| `["findfirst", "n=1000", "foldl"]`                  | 551.123 ms (5%) |         |                 |             |
| `["findfirst", "n=1000", "reduce", "basesize=128"]` | 367.775 ms (5%) |         | 774.81 KiB (1%) |       13562 |
| `["findfirst", "n=1000", "reduce", "basesize=256"]` | 461.875 ms (5%) |         | 550.14 KiB (1%) |        9652 |
| `["findfirst", "n=1000", "reduce", "basesize=512"]` | 541.997 ms (5%) |         | 335.84 KiB (1%) |        5890 |
| `["findfirst", "n=400", "foldl"]`                   | 410.355 ms (5%) |         |                 |             |
| `["findfirst", "n=400", "reduce", "basesize=128"]`  | 224.046 ms (5%) |         |   1.09 MiB (1%) |       19582 |
| `["findfirst", "n=400", "reduce", "basesize=256"]`  | 235.039 ms (5%) |         | 609.28 KiB (1%) |       10740 |
| `["findfirst", "n=400", "reduce", "basesize=512"]`  | 257.351 ms (5%) |         | 355.27 KiB (1%) |        6269 |
| `["findfirst", "n=500", "foldl"]`                   |  66.588 ms (5%) |         |                 |             |
| `["findfirst", "n=500", "reduce", "basesize=128"]`  | 125.212 ms (5%) |         | 641.30 KiB (1%) |       11182 |
| `["findfirst", "n=500", "reduce", "basesize=256"]`  | 112.192 ms (5%) |         | 349.72 KiB (1%) |        6081 |
| `["findfirst", "n=500", "reduce", "basesize=512"]`  | 171.299 ms (5%) |         | 275.30 KiB (1%) |        4802 |
| `["overhead", "default"]`                           |  60.900 μs (5%) |         |  47.36 KiB (1%) |         382 |
| `["overhead", "stoppable=false"]`                   |  57.501 μs (5%) |         |  47.39 KiB (1%) |         382 |
| `["overhead", "stoppable=true"]`                    | 157.801 μs (5%) |         | 139.67 KiB (1%) |        2464 |
| `["parallel_histogram", "assoc", "basesize=16384"]` |   3.314 ms (5%) |         | 730.06 KiB (1%) |          57 |
| `["parallel_histogram", "assoc", "basesize=4096"]`  |   4.047 ms (5%) |         |   1.79 MiB (1%) |         213 |
| `["parallel_histogram", "assoc", "basesize=8192"]`  |   3.667 ms (5%) |         |   1.43 MiB (1%) |         117 |
| `["parallel_histogram", "comm", "basesize=16384"]`  |  13.473 ms (5%) |         |   1.02 MiB (1%) |         351 |
| `["parallel_histogram", "comm", "basesize=4096"]`   |  22.690 ms (5%) |         |   1.03 MiB (1%) |        1845 |
| `["parallel_histogram", "comm", "basesize=8192"]`   |  17.401 ms (5%) |         |   1.25 MiB (1%) |        1225 |
| `["parallel_histogram", "seq"]`                     |   5.934 ms (5%) |         | 364.61 KiB (1%) |          24 |
| `["partition_length_maximum", "rand", "foldl"]`     |  34.225 ms (5%) |         |                 |             |
| `["partition_length_maximum", "rand", "reduce"]`    |  17.523 ms (5%) |         |   2.66 KiB (1%) |          48 |
| `["splitby", "count", "foldl"]`                     |   3.785 ms (5%) |         |   96 bytes (1%) |           4 |
| `["splitby", "count", "man"]`                       |   1.458 ms (5%) |         |                 |             |
| `["splitby", "count", "reduce"]`                    | 815.604 μs (5%) |         |   2.88 KiB (1%) |          55 |
| `["sum", "random", "foldl"]`                        |  12.400 ms (5%) |         |   32 bytes (1%) |           2 |
| `["sum", "random", "reduce", "basesize=128"]`       |   6.559 ms (5%) |         | 103.23 KiB (1%) |        1018 |
| `["sum", "random", "reduce", "basesize=256"]`       |   6.343 ms (5%) |         |  51.23 KiB (1%) |         506 |
| `["sum", "random", "reduce", "basesize=512"]`       |   6.422 ms (5%) |         |  25.30 KiB (1%) |         252 |
| `["sum", "uniform", "foldl"]`                       |  12.210 ms (5%) |         |   32 bytes (1%) |           2 |
| `["sum", "uniform", "reduce", "basesize=128"]`      |   6.617 ms (5%) |         | 103.23 KiB (1%) |        1018 |
| `["sum", "uniform", "reduce", "basesize=256"]`      |   6.330 ms (5%) |         |  51.23 KiB (1%) |         506 |
| `["sum", "uniform", "reduce", "basesize=512"]`      |   6.243 ms (5%) |         |  25.25 KiB (1%) |         251 |
| `["sum", "valley", "foldl"]`                        |  13.075 ms (5%) |         |   32 bytes (1%) |           2 |
| `["sum", "valley", "reduce", "basesize=128"]`       |   6.703 ms (5%) |         | 103.23 KiB (1%) |        1018 |
| `["sum", "valley", "reduce", "basesize=256"]`       |   6.523 ms (5%) |         |  51.23 KiB (1%) |         506 |
| `["sum", "valley", "reduce", "basesize=512"]`       |   6.742 ms (5%) |         |  25.28 KiB (1%) |         252 |
| `["words", "nthreads=1"]`                           |  25.182 ms (5%) |         |  31.84 MiB (1%) |     1036734 |
| `["words", "nthreads=2"]`                           |  14.490 ms (5%) |         |  32.19 MiB (1%) |     1036770 |
| `["words", "nthreads=4"]`                           |  15.649 ms (5%) |         |  32.91 MiB (1%) |     1036851 |

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
  CPU: Intel(R) Xeon(R) CPU E5-2673 v4 @ 2.30GHz: 
              speed         user         nice          sys         idle          irq
       #1  2294 MHz      82494 s         12 s       3096 s      26245 s          0 s
       #2  2294 MHz      78284 s         12 s       3214 s      30345 s          0 s
       
  Memory: 6.7913818359375 GB (3361.609375 MB free)
  Uptime: 1137.0 sec
  Load Avg:  1.63037109375  1.55615234375  1.1591796875
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
    Vulnerability Itlb multihit:     KVM: Vulnerable
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

