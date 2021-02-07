# Multi-thread benchmark result

* Pull request commit: [`9710189812ec8c33d5e323691251e99bc9463996`](https://github.com/JuliaFolds/Transducers.jl/commit/9710189812ec8c33d5e323691251e99bc9463996)
* Pull request: <https://github.com/JuliaFolds/Transducers.jl/pull/243> (Update */Manifest.toml)

# Judge result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmarks:
    - Target: 7 Feb 2021 - 01:02
    - Baseline: 7 Feb 2021 - 01:07
* Package commits:
    - Target: d370a2
    - Baseline: 6b0f22
* Julia commits:
    - Target: 788b2c
    - Baseline: 788b2c
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
| `["collect", "unordered", "basesize=1024"]`         | 0.87 (5%) :white_check_mark: | 0.91 (1%) :white_check_mark: |
| `["findfirst", "n=1000", "reduce", "basesize=128"]` |                1.05 (5%) :x: |                1.04 (1%) :x: |
| `["findfirst", "n=1000", "reduce", "basesize=256"]` |                1.07 (5%) :x: |                1.06 (1%) :x: |
| `["findfirst", "n=1000", "reduce", "basesize=512"]` | 0.86 (5%) :white_check_mark: | 0.92 (1%) :white_check_mark: |
| `["findfirst", "n=400", "reduce", "basesize=128"]`  |                   0.99 (5%)  | 0.97 (1%) :white_check_mark: |
| `["findfirst", "n=400", "reduce", "basesize=256"]`  |                   1.02 (5%)  | 0.98 (1%) :white_check_mark: |
| `["findfirst", "n=400", "reduce", "basesize=512"]`  |                1.08 (5%) :x: |                1.08 (1%) :x: |
| `["findfirst", "n=500", "reduce", "basesize=128"]`  | 0.42 (5%) :white_check_mark: | 0.51 (1%) :white_check_mark: |
| `["findfirst", "n=500", "reduce", "basesize=256"]`  |                1.11 (5%) :x: |                1.18 (1%) :x: |
| `["findfirst", "n=500", "reduce", "basesize=512"]`  |                1.17 (5%) :x: |                1.18 (1%) :x: |
| `["overhead", "stoppable=false"]`                   | 0.95 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["parallel_histogram", "comm", "basesize=4096"]`   |                1.34 (5%) :x: |                1.05 (1%) :x: |

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
Julia Version 1.5.3
Commit 788b2c77c1 (2020-11-09 13:37 UTC)
Platform Info:
  OS: Linux (x86_64-pc-linux-gnu)
      Ubuntu 18.04.5 LTS
  uname: Linux 5.4.0-1039-azure #41~18.04.1-Ubuntu SMP Mon Jan 18 14:00:01 UTC 2021 x86_64 x86_64
  CPU: Intel(R) Xeon(R) CPU E5-2673 v3 @ 2.40GHz: 
              speed         user         nice          sys         idle          irq
       #1  2397 MHz      51606 s          0 s       2288 s      72182 s          0 s
       #2  2397 MHz      54143 s          0 s       2696 s      69872 s          0 s
       
  Memory: 6.791393280029297 GB (3750.1484375 MB free)
  Uptime: 1280.0 sec
  Load Avg:  1.5693359375  1.48193359375  0.91015625
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-9.0.1 (ORCJIT, haswell)
```

### Baseline
```
Julia Version 1.5.3
Commit 788b2c77c1 (2020-11-09 13:37 UTC)
Platform Info:
  OS: Linux (x86_64-pc-linux-gnu)
      Ubuntu 18.04.5 LTS
  uname: Linux 5.4.0-1039-azure #41~18.04.1-Ubuntu SMP Mon Jan 18 14:00:01 UTC 2021 x86_64 x86_64
  CPU: Intel(R) Xeon(R) CPU E5-2673 v3 @ 2.40GHz: 
              speed         user         nice          sys         idle          irq
       #1  2397 MHz      78505 s          0 s       2847 s      77141 s          0 s
       #2  2397 MHz      75914 s          0 s       3226 s      79951 s          0 s
       
  Memory: 6.791393280029297 GB (3845.10546875 MB free)
  Uptime: 1605.0 sec
  Load Avg:  1.767578125  1.58056640625  1.1171875
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-9.0.1 (ORCJIT, haswell)
```

---
# Target result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmark: 7 Feb 2021 - 1:2
* Package commit: d370a2
* Julia commit: 788b2c
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
| `["collect", "assoc", "basesize=1"]`                | 302.271 ms (5%) |         |  32.66 MiB (1%) |      286762 |
| `["collect", "assoc", "basesize=1024"]`             | 252.170 ms (5%) |         |   1.79 MiB (1%) |         570 |
| `["collect", "assoc", "basesize=32"]`               | 254.231 ms (5%) |         |   3.97 MiB (1%) |       13307 |
| `["collect", "seq"]`                                | 498.757 ms (5%) |         | 512.72 KiB (1%) |          15 |
| `["collect", "unordered", "basesize=1"]`            | 519.969 ms (5%) |         |  30.01 MiB (1%) |      360633 |
| `["collect", "unordered", "basesize=1024"]`         | 315.916 ms (5%) |         | 834.14 KiB (1%) |        3432 |
| `["collect", "unordered", "basesize=32"]`           | 276.585 ms (5%) |         |   1.47 MiB (1%) |       12516 |
| `["findfirst", "n=1000", "foldl"]`                  | 727.199 ms (5%) |         |                 |             |
| `["findfirst", "n=1000", "reduce", "basesize=128"]` | 459.786 ms (5%) |         | 786.42 KiB (1%) |       13767 |
| `["findfirst", "n=1000", "reduce", "basesize=256"]` | 525.858 ms (5%) |         | 485.00 KiB (1%) |        8497 |
| `["findfirst", "n=1000", "reduce", "basesize=512"]` | 711.600 ms (5%) |         | 361.11 KiB (1%) |        6334 |
| `["findfirst", "n=400", "foldl"]`                   | 551.393 ms (5%) |         |                 |             |
| `["findfirst", "n=400", "reduce", "basesize=128"]`  | 287.683 ms (5%) |         |   1.07 MiB (1%) |       19350 |
| `["findfirst", "n=400", "reduce", "basesize=256"]`  | 304.227 ms (5%) |         | 595.48 KiB (1%) |       10504 |
| `["findfirst", "n=400", "reduce", "basesize=512"]`  | 345.877 ms (5%) |         | 384.86 KiB (1%) |        6776 |
| `["findfirst", "n=500", "foldl"]`                   |  93.367 ms (5%) |         |                 |             |
| `["findfirst", "n=500", "reduce", "basesize=128"]`  |  83.694 ms (5%) |         | 394.89 KiB (1%) |        6870 |
| `["findfirst", "n=500", "reduce", "basesize=256"]`  | 183.655 ms (5%) |         | 423.72 KiB (1%) |        7377 |
| `["findfirst", "n=500", "reduce", "basesize=512"]`  | 188.899 ms (5%) |         | 259.03 KiB (1%) |        4508 |
| `["overhead", "default"]`                           |  62.102 μs (5%) |         |  47.36 KiB (1%) |         382 |
| `["overhead", "stoppable=false"]`                   |  60.902 μs (5%) |         |  47.39 KiB (1%) |         382 |
| `["overhead", "stoppable=true"]`                    | 180.007 μs (5%) |         | 139.64 KiB (1%) |        2463 |
| `["parallel_histogram", "assoc", "basesize=16384"]` |   5.233 ms (5%) |         | 730.06 KiB (1%) |          57 |
| `["parallel_histogram", "assoc", "basesize=4096"]`  |   6.002 ms (5%) |         |   1.79 MiB (1%) |         213 |
| `["parallel_histogram", "assoc", "basesize=8192"]`  |   5.597 ms (5%) |         |   1.43 MiB (1%) |         117 |
| `["parallel_histogram", "comm", "basesize=16384"]`  |  12.287 ms (5%) |         |   1.22 MiB (1%) |         160 |
| `["parallel_histogram", "comm", "basesize=4096"]`   |  21.497 ms (5%) |         |   1.03 MiB (1%) |         732 |
| `["parallel_histogram", "comm", "basesize=8192"]`   |  14.771 ms (5%) |         |   1.23 MiB (1%) |         456 |
| `["parallel_histogram", "seq"]`                     |   9.620 ms (5%) |         | 364.61 KiB (1%) |          24 |
| `["sum", "random", "foldl"]`                        |  18.637 ms (5%) |         |   32 bytes (1%) |           2 |
| `["sum", "random", "reduce", "basesize=128"]`       |   9.520 ms (5%) |         | 103.23 KiB (1%) |        1018 |
| `["sum", "random", "reduce", "basesize=256"]`       |   9.439 ms (5%) |         |  51.23 KiB (1%) |         506 |
| `["sum", "random", "reduce", "basesize=512"]`       |   9.365 ms (5%) |         |  25.30 KiB (1%) |         252 |
| `["sum", "uniform", "foldl"]`                       |  18.106 ms (5%) |         |   32 bytes (1%) |           2 |
| `["sum", "uniform", "reduce", "basesize=128"]`      |   9.262 ms (5%) |         | 103.23 KiB (1%) |        1018 |
| `["sum", "uniform", "reduce", "basesize=256"]`      |   9.155 ms (5%) |         |  51.23 KiB (1%) |         506 |
| `["sum", "uniform", "reduce", "basesize=512"]`      |   9.089 ms (5%) |         |  25.25 KiB (1%) |         251 |
| `["sum", "valley", "foldl"]`                        |  18.627 ms (5%) |         |   32 bytes (1%) |           2 |
| `["sum", "valley", "reduce", "basesize=128"]`       |   9.517 ms (5%) |         | 103.23 KiB (1%) |        1018 |
| `["sum", "valley", "reduce", "basesize=256"]`       |   9.435 ms (5%) |         |  51.23 KiB (1%) |         506 |
| `["sum", "valley", "reduce", "basesize=512"]`       |   9.372 ms (5%) |         |  25.25 KiB (1%) |         251 |
| `["words", "nthreads=1"]`                           |  27.509 ms (5%) |         |  31.64 MiB (1%) |     1030771 |
| `["words", "nthreads=2"]`                           |  17.178 ms (5%) |         |  32.35 MiB (1%) |     1030846 |
| `["words", "nthreads=4"]`                           |  17.288 ms (5%) |         |  32.99 MiB (1%) |     1031025 |

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
- `["sum", "random"]`
- `["sum", "random", "reduce"]`
- `["sum", "uniform"]`
- `["sum", "uniform", "reduce"]`
- `["sum", "valley"]`
- `["sum", "valley", "reduce"]`
- `["words"]`

## Julia versioninfo
```
Julia Version 1.5.3
Commit 788b2c77c1 (2020-11-09 13:37 UTC)
Platform Info:
  OS: Linux (x86_64-pc-linux-gnu)
      Ubuntu 18.04.5 LTS
  uname: Linux 5.4.0-1039-azure #41~18.04.1-Ubuntu SMP Mon Jan 18 14:00:01 UTC 2021 x86_64 x86_64
  CPU: Intel(R) Xeon(R) CPU E5-2673 v3 @ 2.40GHz: 
              speed         user         nice          sys         idle          irq
       #1  2397 MHz      51606 s          0 s       2288 s      72182 s          0 s
       #2  2397 MHz      54143 s          0 s       2696 s      69872 s          0 s
       
  Memory: 6.791393280029297 GB (3750.1484375 MB free)
  Uptime: 1280.0 sec
  Load Avg:  1.5693359375  1.48193359375  0.91015625
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-9.0.1 (ORCJIT, haswell)
```

---
# Baseline result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmark: 7 Feb 2021 - 1:7
* Package commit: 6b0f22
* Julia commit: 788b2c
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
| `["collect", "assoc", "basesize=1"]`                | 306.049 ms (5%) |         |   32.66 MiB (1%) |      286762 |
| `["collect", "assoc", "basesize=1024"]`             | 250.501 ms (5%) |         |    1.79 MiB (1%) |         570 |
| `["collect", "assoc", "basesize=32"]`               | 253.233 ms (5%) |         |    3.97 MiB (1%) |       13306 |
| `["collect", "seq"]`                                | 506.227 ms (5%) |         |  512.72 KiB (1%) |          15 |
| `["collect", "unordered", "basesize=1"]`            | 528.650 ms (5%) |         |   30.01 MiB (1%) |      360610 |
| `["collect", "unordered", "basesize=1024"]`         | 361.807 ms (5%) |         |  916.14 KiB (1%) |        6056 |
| `["collect", "unordered", "basesize=32"]`           | 275.991 ms (5%) |         |    1.47 MiB (1%) |       12530 |
| `["findfirst", "n=1000", "foldl"]`                  | 733.208 ms (5%) |         |                  |             |
| `["findfirst", "n=1000", "reduce", "basesize=128"]` | 437.224 ms (5%) |         |  756.23 KiB (1%) |       13238 |
| `["findfirst", "n=1000", "reduce", "basesize=256"]` | 489.668 ms (5%) |         |  459.55 KiB (1%) |        8056 |
| `["findfirst", "n=1000", "reduce", "basesize=512"]` | 829.233 ms (5%) |         |  393.52 KiB (1%) |        6906 |
| `["findfirst", "n=400", "foldl"]`                   | 547.070 ms (5%) |         |                  |             |
| `["findfirst", "n=400", "reduce", "basesize=128"]`  | 290.546 ms (5%) |         |    1.11 MiB (1%) |       19892 |
| `["findfirst", "n=400", "reduce", "basesize=256"]`  | 298.793 ms (5%) |         |  606.58 KiB (1%) |       10684 |
| `["findfirst", "n=400", "reduce", "basesize=512"]`  | 319.538 ms (5%) |         |  357.44 KiB (1%) |        6301 |
| `["findfirst", "n=500", "foldl"]`                   |  94.132 ms (5%) |         |                  |             |
| `["findfirst", "n=500", "reduce", "basesize=128"]`  | 199.932 ms (5%) |         |  778.66 KiB (1%) |       13599 |
| `["findfirst", "n=500", "reduce", "basesize=256"]`  | 165.552 ms (5%) |         |  359.63 KiB (1%) |        6281 |
| `["findfirst", "n=500", "reduce", "basesize=512"]`  | 161.282 ms (5%) |         |  220.08 KiB (1%) |        3832 |
| `["overhead", "default"]`                           |  64.102 μs (5%) |         |   47.36 KiB (1%) |         382 |
| `["overhead", "stoppable=false"]`                   |  64.402 μs (5%) |         |   47.39 KiB (1%) |         382 |
| `["overhead", "stoppable=true"]`                    | 182.305 μs (5%) |         |  139.67 KiB (1%) |        2464 |
| `["parallel_histogram", "assoc", "basesize=16384"]` |   5.258 ms (5%) |         |  730.06 KiB (1%) |          57 |
| `["parallel_histogram", "assoc", "basesize=4096"]`  |   6.038 ms (5%) |         |    1.79 MiB (1%) |         213 |
| `["parallel_histogram", "assoc", "basesize=8192"]`  |   5.643 ms (5%) |         |    1.43 MiB (1%) |         117 |
| `["parallel_histogram", "comm", "basesize=16384"]`  |  12.317 ms (5%) |         |    1.22 MiB (1%) |         238 |
| `["parallel_histogram", "comm", "basesize=4096"]`   |  16.068 ms (5%) |         | 1002.06 KiB (1%) |         338 |
| `["parallel_histogram", "comm", "basesize=8192"]`   |  15.325 ms (5%) |         |    1.23 MiB (1%) |         459 |
| `["parallel_histogram", "seq"]`                     |   9.610 ms (5%) |         |  364.61 KiB (1%) |          24 |
| `["sum", "random", "foldl"]`                        |  18.578 ms (5%) |         |    32 bytes (1%) |           2 |
| `["sum", "random", "reduce", "basesize=128"]`       |   9.457 ms (5%) |         |  103.23 KiB (1%) |        1018 |
| `["sum", "random", "reduce", "basesize=256"]`       |   9.400 ms (5%) |         |   51.23 KiB (1%) |         506 |
| `["sum", "random", "reduce", "basesize=512"]`       |   9.340 ms (5%) |         |   25.30 KiB (1%) |         252 |
| `["sum", "uniform", "foldl"]`                       |  18.109 ms (5%) |         |    32 bytes (1%) |           2 |
| `["sum", "uniform", "reduce", "basesize=128"]`      |   9.237 ms (5%) |         |  103.23 KiB (1%) |        1018 |
| `["sum", "uniform", "reduce", "basesize=256"]`      |   9.157 ms (5%) |         |   51.23 KiB (1%) |         506 |
| `["sum", "uniform", "reduce", "basesize=512"]`      |   9.094 ms (5%) |         |   25.25 KiB (1%) |         251 |
| `["sum", "valley", "foldl"]`                        |  18.627 ms (5%) |         |    32 bytes (1%) |           2 |
| `["sum", "valley", "reduce", "basesize=128"]`       |   9.514 ms (5%) |         |  103.23 KiB (1%) |        1018 |
| `["sum", "valley", "reduce", "basesize=256"]`       |   9.433 ms (5%) |         |   51.23 KiB (1%) |         506 |
| `["sum", "valley", "reduce", "basesize=512"]`       |   9.366 ms (5%) |         |   25.25 KiB (1%) |         251 |
| `["words", "nthreads=1"]`                           |  27.638 ms (5%) |         |   31.69 MiB (1%) |     1032664 |
| `["words", "nthreads=2"]`                           |  16.930 ms (5%) |         |   32.05 MiB (1%) |     1032710 |
| `["words", "nthreads=4"]`                           |  17.408 ms (5%) |         |   32.94 MiB (1%) |     1032869 |

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
- `["sum", "random"]`
- `["sum", "random", "reduce"]`
- `["sum", "uniform"]`
- `["sum", "uniform", "reduce"]`
- `["sum", "valley"]`
- `["sum", "valley", "reduce"]`
- `["words"]`

## Julia versioninfo
```
Julia Version 1.5.3
Commit 788b2c77c1 (2020-11-09 13:37 UTC)
Platform Info:
  OS: Linux (x86_64-pc-linux-gnu)
      Ubuntu 18.04.5 LTS
  uname: Linux 5.4.0-1039-azure #41~18.04.1-Ubuntu SMP Mon Jan 18 14:00:01 UTC 2021 x86_64 x86_64
  CPU: Intel(R) Xeon(R) CPU E5-2673 v3 @ 2.40GHz: 
              speed         user         nice          sys         idle          irq
       #1  2397 MHz      78505 s          0 s       2847 s      77141 s          0 s
       #2  2397 MHz      75914 s          0 s       3226 s      79951 s          0 s
       
  Memory: 6.791393280029297 GB (3845.10546875 MB free)
  Uptime: 1605.0 sec
  Load Avg:  1.767578125  1.58056640625  1.1171875
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

    Architecture:        x86_64
    CPU op-mode(s):      32-bit, 64-bit
    Byte Order:          Little Endian
    CPU(s):              2
    On-line CPU(s) list: 0,1
    Thread(s) per core:  1
    Core(s) per socket:  2
    Socket(s):           1
    NUMA node(s):        1
    Vendor ID:           GenuineIntel
    CPU family:          6
    Model:               63
    Model name:          Intel(R) Xeon(R) CPU E5-2673 v3 @ 2.40GHz
    Stepping:            2
    CPU MHz:             2397.225
    BogoMIPS:            4794.45
    Hypervisor vendor:   Microsoft
    Virtualization type: full
    L1d cache:           32K
    L1i cache:           32K
    L2 cache:            256K
    L3 cache:            30720K
    NUMA node0 CPU(s):   0,1
    Flags:               fpu vme de pse tsc msr pae mce cx8 apic sep mtrr pge mca cmov pat pse36 clflush mmx fxsr sse sse2 ss ht syscall nx pdpe1gb rdtscp lm constant_tsc rep_good nopl xtopology cpuid pni pclmulqdq ssse3 fma cx16 pcid sse4_1 sse4_2 movbe popcnt aes xsave avx f16c rdrand hypervisor lahf_lm abm invpcid_single pti fsgsbase bmi1 avx2 smep bmi2 erms invpcid xsaveopt md_clear
    

| Cpu Property       | Value                                                   |
|:------------------ |:------------------------------------------------------- |
| Brand              | Intel(R) Xeon(R) CPU E5-2673 v3 @ 2.40GHz               |
| Vendor             | :Intel                                                  |
| Architecture       | :Haswell                                                |
| Model              | Family: 0x06, Model: 0x3f, Stepping: 0x02, Type: 0x00   |
| Cores              | 2 physical cores, 2 logical cores (on executing CPU)    |
|                    | No Hyperthreading detected                              |
| Clock Frequencies  | Not supported by CPU                                    |
| Data Cache         | Level 1:3 : (32, 256, 30720) kbytes                     |
|                    | 64 byte cache line size                                 |
| Address Size       | 48 bits virtual, 46 bits physical                       |
| SIMD               | 256 bit = 32 byte max. SIMD vector size                 |
| Time Stamp Counter | TSC is accessible via `rdtsc`                           |
|                    | TSC increased at every clock cycle (non-invariant TSC)  |
| Perf. Monitoring   | Performance Monitoring Counters (PMC) are not supported |
| Hypervisor         | Yes, Microsoft                                          |

