# Multi-thread benchmark result

* Pull request commit: [`75954074c3c23983bd81cf36c561c7f13bf1d7fd`](https://github.com/JuliaFolds/Transducers.jl/commit/75954074c3c23983bd81cf36c561c7f13bf1d7fd)
* Pull request: <https://github.com/JuliaFolds/Transducers.jl/pull/457> (Mention executor in glossary)

# Judge result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmarks:
    - Target: 21 Feb 2021 - 08:02
    - Baseline: 21 Feb 2021 - 08:07
* Package commits:
    - Target: 33e2da
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
| `["collect", "unordered", "basesize=1024"]`         |                1.06 (5%) :x: |                1.08 (1%) :x: |
| `["findfirst", "n=1000", "reduce", "basesize=128"]` | 0.78 (5%) :white_check_mark: | 0.78 (1%) :white_check_mark: |
| `["findfirst", "n=400", "reduce", "basesize=256"]`  |                   0.98 (5%)  | 0.98 (1%) :white_check_mark: |
| `["findfirst", "n=500", "reduce", "basesize=128"]`  | 0.74 (5%) :white_check_mark: | 0.69 (1%) :white_check_mark: |
| `["findfirst", "n=500", "reduce", "basesize=256"]`  |                1.17 (5%) :x: |                1.04 (1%) :x: |
| `["findfirst", "n=500", "reduce", "basesize=512"]`  | 0.85 (5%) :white_check_mark: | 0.89 (1%) :white_check_mark: |
| `["overhead", "stoppable=true"]`                    | 0.89 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["parallel_histogram", "assoc", "basesize=4096"]`  |                   1.01 (5%)  |                1.15 (1%) :x: |
| `["parallel_histogram", "comm", "basesize=4096"]`   |                   0.99 (5%)  | 0.98 (1%) :white_check_mark: |
| `["parallel_histogram", "comm", "basesize=8192"]`   |                1.07 (5%) :x: |                   0.99 (1%)  |

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
  CPU: Intel(R) Xeon(R) Platinum 8171M CPU @ 2.60GHz: 
              speed         user         nice          sys         idle          irq
       #1  2095 MHz      51906 s          0 s       2504 s      21848 s          0 s
       #2  2095 MHz      49907 s          0 s       2509 s      23889 s          0 s
       
  Memory: 6.791393280029297 GB (3819.41015625 MB free)
  Uptime: 800.0 sec
  Load Avg:  1.71240234375  1.5341796875  0.9453125
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-9.0.1 (ORCJIT, skylake-avx512)
```

### Baseline
```
Julia Version 1.5.3
Commit 788b2c77c1 (2020-11-09 13:37 UTC)
Platform Info:
  OS: Linux (x86_64-pc-linux-gnu)
      Ubuntu 18.04.5 LTS
  uname: Linux 5.4.0-1039-azure #41~18.04.1-Ubuntu SMP Mon Jan 18 14:00:01 UTC 2021 x86_64 x86_64
  CPU: Intel(R) Xeon(R) Platinum 8171M CPU @ 2.60GHz: 
              speed         user         nice          sys         idle          irq
       #1  2095 MHz      69596 s          0 s       2957 s      31865 s          0 s
       #2  2095 MHz      76167 s          0 s       2930 s      25299 s          0 s
       
  Memory: 6.791393280029297 GB (3860.7578125 MB free)
  Uptime: 1083.0 sec
  Load Avg:  1.73681640625  1.607421875  1.13037109375
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-9.0.1 (ORCJIT, skylake-avx512)
```

---
# Target result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmark: 21 Feb 2021 - 8:2
* Package commit: 33e2da
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
| `["collect", "assoc", "basesize=1"]`                | 283.556 ms (5%) |         |  32.66 MiB (1%) |      286747 |
| `["collect", "assoc", "basesize=1024"]`             | 238.158 ms (5%) |         |   1.79 MiB (1%) |         569 |
| `["collect", "assoc", "basesize=32"]`               | 241.394 ms (5%) |         |   3.97 MiB (1%) |       13306 |
| `["collect", "seq"]`                                | 471.805 ms (5%) |         | 512.72 KiB (1%) |          15 |
| `["collect", "unordered", "basesize=1"]`            | 492.753 ms (5%) |         |  30.01 MiB (1%) |      360635 |
| `["collect", "unordered", "basesize=1024"]`         | 309.960 ms (5%) |         | 822.77 KiB (1%) |        3068 |
| `["collect", "unordered", "basesize=32"]`           | 263.274 ms (5%) |         |   1.47 MiB (1%) |       12382 |
| `["findfirst", "n=1000", "foldl"]`                  | 743.990 ms (5%) |         |                 |             |
| `["findfirst", "n=1000", "reduce", "basesize=128"]` | 567.440 ms (5%) |         | 932.64 KiB (1%) |       16316 |
| `["findfirst", "n=1000", "reduce", "basesize=256"]` | 529.549 ms (5%) |         | 485.00 KiB (1%) |        8497 |
| `["findfirst", "n=1000", "reduce", "basesize=512"]` | 691.039 ms (5%) |         | 326.66 KiB (1%) |        5732 |
| `["findfirst", "n=400", "foldl"]`                   | 560.397 ms (5%) |         |                 |             |
| `["findfirst", "n=400", "reduce", "basesize=128"]`  | 294.436 ms (5%) |         |   1.06 MiB (1%) |       19143 |
| `["findfirst", "n=400", "reduce", "basesize=256"]`  | 314.379 ms (5%) |         | 595.50 KiB (1%) |       10503 |
| `["findfirst", "n=400", "reduce", "basesize=512"]`  | 341.761 ms (5%) |         | 370.91 KiB (1%) |        6533 |
| `["findfirst", "n=500", "foldl"]`                   |  95.541 ms (5%) |         |                 |             |
| `["findfirst", "n=500", "reduce", "basesize=128"]`  | 154.590 ms (5%) |         | 546.83 KiB (1%) |        9559 |
| `["findfirst", "n=500", "reduce", "basesize=256"]`  | 188.562 ms (5%) |         | 377.89 KiB (1%) |        6591 |
| `["findfirst", "n=500", "reduce", "basesize=512"]`  | 160.141 ms (5%) |         | 220.02 KiB (1%) |        3829 |
| `["overhead", "default"]`                           |  63.800 μs (5%) |         |  47.33 KiB (1%) |         381 |
| `["overhead", "stoppable=false"]`                   |  66.300 μs (5%) |         |  47.36 KiB (1%) |         381 |
| `["overhead", "stoppable=true"]`                    | 152.201 μs (5%) |         | 139.64 KiB (1%) |        2463 |
| `["parallel_histogram", "assoc", "basesize=16384"]` |   5.167 ms (5%) |         | 730.06 KiB (1%) |          57 |
| `["parallel_histogram", "assoc", "basesize=4096"]`  |   6.105 ms (5%) |         |   2.06 MiB (1%) |         219 |
| `["parallel_histogram", "assoc", "basesize=8192"]`  |   5.550 ms (5%) |         |   1.43 MiB (1%) |         117 |
| `["parallel_histogram", "comm", "basesize=16384"]`  |  15.474 ms (5%) |         |   1.22 MiB (1%) |         160 |
| `["parallel_histogram", "comm", "basesize=4096"]`   |  24.308 ms (5%) |         |   1.03 MiB (1%) |        1613 |
| `["parallel_histogram", "comm", "basesize=8192"]`   |  20.460 ms (5%) |         |   1.24 MiB (1%) |         784 |
| `["parallel_histogram", "seq"]`                     |   9.486 ms (5%) |         | 364.61 KiB (1%) |          24 |
| `["sum", "random", "foldl"]`                        |  18.449 ms (5%) |         |   32 bytes (1%) |           2 |
| `["sum", "random", "reduce", "basesize=128"]`       |   9.355 ms (5%) |         | 103.23 KiB (1%) |        1018 |
| `["sum", "random", "reduce", "basesize=256"]`       |   9.321 ms (5%) |         |  51.23 KiB (1%) |         506 |
| `["sum", "random", "reduce", "basesize=512"]`       |   9.433 ms (5%) |         |  25.30 KiB (1%) |         252 |
| `["sum", "uniform", "foldl"]`                       |  18.079 ms (5%) |         |   32 bytes (1%) |           2 |
| `["sum", "uniform", "reduce", "basesize=128"]`      |   9.446 ms (5%) |         | 103.23 KiB (1%) |        1018 |
| `["sum", "uniform", "reduce", "basesize=256"]`      |   9.258 ms (5%) |         |  51.23 KiB (1%) |         506 |
| `["sum", "uniform", "reduce", "basesize=512"]`      |   9.096 ms (5%) |         |  25.25 KiB (1%) |         251 |
| `["sum", "valley", "foldl"]`                        |  18.870 ms (5%) |         |   32 bytes (1%) |           2 |
| `["sum", "valley", "reduce", "basesize=128"]`       |   9.704 ms (5%) |         | 103.23 KiB (1%) |        1018 |
| `["sum", "valley", "reduce", "basesize=256"]`       |   9.673 ms (5%) |         |  51.23 KiB (1%) |         506 |
| `["sum", "valley", "reduce", "basesize=512"]`       |   9.683 ms (5%) |         |  25.25 KiB (1%) |         251 |
| `["words", "nthreads=1"]`                           |  26.398 ms (5%) |         |  31.73 MiB (1%) |     1033527 |
| `["words", "nthreads=2"]`                           |  16.900 ms (5%) |         |  32.44 MiB (1%) |     1033610 |
| `["words", "nthreads=4"]`                           |  17.101 ms (5%) |         |  32.89 MiB (1%) |     1033676 |

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
  CPU: Intel(R) Xeon(R) Platinum 8171M CPU @ 2.60GHz: 
              speed         user         nice          sys         idle          irq
       #1  2095 MHz      51906 s          0 s       2504 s      21848 s          0 s
       #2  2095 MHz      49907 s          0 s       2509 s      23889 s          0 s
       
  Memory: 6.791393280029297 GB (3819.41015625 MB free)
  Uptime: 800.0 sec
  Load Avg:  1.71240234375  1.5341796875  0.9453125
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-9.0.1 (ORCJIT, skylake-avx512)
```

---
# Baseline result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmark: 21 Feb 2021 - 8:7
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

| ID                                                  | time            | GC time | memory          | allocations |
|-----------------------------------------------------|----------------:|--------:|----------------:|------------:|
| `["collect", "assoc", "basesize=1"]`                | 286.099 ms (5%) |         |  32.66 MiB (1%) |      286747 |
| `["collect", "assoc", "basesize=1024"]`             | 238.118 ms (5%) |         |   1.79 MiB (1%) |         570 |
| `["collect", "assoc", "basesize=32"]`               | 242.615 ms (5%) |         |   3.97 MiB (1%) |       13307 |
| `["collect", "seq"]`                                | 473.020 ms (5%) |         | 512.72 KiB (1%) |          15 |
| `["collect", "unordered", "basesize=1"]`            | 491.757 ms (5%) |         |  30.01 MiB (1%) |      360603 |
| `["collect", "unordered", "basesize=1024"]`         | 293.674 ms (5%) |         | 762.20 KiB (1%) |        1130 |
| `["collect", "unordered", "basesize=32"]`           | 264.167 ms (5%) |         |   1.47 MiB (1%) |       12467 |
| `["findfirst", "n=1000", "foldl"]`                  | 751.992 ms (5%) |         |                 |             |
| `["findfirst", "n=1000", "reduce", "basesize=128"]` | 726.418 ms (5%) |         |   1.16 MiB (1%) |       20776 |
| `["findfirst", "n=1000", "reduce", "basesize=256"]` | 538.067 ms (5%) |         | 484.97 KiB (1%) |        8496 |
| `["findfirst", "n=1000", "reduce", "basesize=512"]` | 701.510 ms (5%) |         | 329.06 KiB (1%) |        5777 |
| `["findfirst", "n=400", "foldl"]`                   | 563.573 ms (5%) |         |                 |             |
| `["findfirst", "n=400", "reduce", "basesize=128"]`  | 293.995 ms (5%) |         |   1.07 MiB (1%) |       19259 |
| `["findfirst", "n=400", "reduce", "basesize=256"]`  | 321.580 ms (5%) |         | 604.91 KiB (1%) |       10676 |
| `["findfirst", "n=400", "reduce", "basesize=512"]`  | 334.253 ms (5%) |         | 368.88 KiB (1%) |        6503 |
| `["findfirst", "n=500", "foldl"]`                   |  97.670 ms (5%) |         |                 |             |
| `["findfirst", "n=500", "reduce", "basesize=128"]`  | 208.027 ms (5%) |         | 789.05 KiB (1%) |       13736 |
| `["findfirst", "n=500", "reduce", "basesize=256"]`  | 161.608 ms (5%) |         | 363.75 KiB (1%) |        6336 |
| `["findfirst", "n=500", "reduce", "basesize=512"]`  | 187.537 ms (5%) |         | 247.55 KiB (1%) |        4309 |
| `["overhead", "default"]`                           |  66.901 μs (5%) |         |  47.33 KiB (1%) |         381 |
| `["overhead", "stoppable=false"]`                   |  67.500 μs (5%) |         |  47.36 KiB (1%) |         381 |
| `["overhead", "stoppable=true"]`                    | 170.501 μs (5%) |         | 139.64 KiB (1%) |        2463 |
| `["parallel_histogram", "assoc", "basesize=16384"]` |   5.292 ms (5%) |         | 730.06 KiB (1%) |          57 |
| `["parallel_histogram", "assoc", "basesize=4096"]`  |   6.047 ms (5%) |         |   1.79 MiB (1%) |         213 |
| `["parallel_histogram", "assoc", "basesize=8192"]`  |   5.594 ms (5%) |         |   1.43 MiB (1%) |         117 |
| `["parallel_histogram", "comm", "basesize=16384"]`  |  15.930 ms (5%) |         |   1.22 MiB (1%) |         269 |
| `["parallel_histogram", "comm", "basesize=4096"]`   |  24.598 ms (5%) |         |   1.05 MiB (1%) |        1640 |
| `["parallel_histogram", "comm", "basesize=8192"]`   |  19.035 ms (5%) |         |   1.25 MiB (1%) |        1071 |
| `["parallel_histogram", "seq"]`                     |   9.463 ms (5%) |         | 364.61 KiB (1%) |          24 |
| `["sum", "random", "foldl"]`                        |  18.854 ms (5%) |         |   32 bytes (1%) |           2 |
| `["sum", "random", "reduce", "basesize=128"]`       |   9.709 ms (5%) |         | 103.23 KiB (1%) |        1018 |
| `["sum", "random", "reduce", "basesize=256"]`       |   9.502 ms (5%) |         |  51.23 KiB (1%) |         506 |
| `["sum", "random", "reduce", "basesize=512"]`       |   9.057 ms (5%) |         |  25.30 KiB (1%) |         252 |
| `["sum", "uniform", "foldl"]`                       |  18.317 ms (5%) |         |   32 bytes (1%) |           2 |
| `["sum", "uniform", "reduce", "basesize=128"]`      |   9.586 ms (5%) |         | 103.23 KiB (1%) |        1018 |
| `["sum", "uniform", "reduce", "basesize=256"]`      |   9.345 ms (5%) |         |  51.23 KiB (1%) |         506 |
| `["sum", "uniform", "reduce", "basesize=512"]`      |   9.313 ms (5%) |         |  25.25 KiB (1%) |         251 |
| `["sum", "valley", "foldl"]`                        |  19.275 ms (5%) |         |   32 bytes (1%) |           2 |
| `["sum", "valley", "reduce", "basesize=128"]`       |   9.759 ms (5%) |         | 103.23 KiB (1%) |        1018 |
| `["sum", "valley", "reduce", "basesize=256"]`       |   9.793 ms (5%) |         |  51.23 KiB (1%) |         506 |
| `["sum", "valley", "reduce", "basesize=512"]`       |   9.664 ms (5%) |         |  25.25 KiB (1%) |         251 |
| `["words", "nthreads=1"]`                           |  26.247 ms (5%) |         |  31.76 MiB (1%) |     1034563 |
| `["words", "nthreads=2"]`                           |  16.678 ms (5%) |         |  32.47 MiB (1%) |     1034645 |
| `["words", "nthreads=4"]`                           |  17.534 ms (5%) |         |  33.10 MiB (1%) |     1034773 |

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
  CPU: Intel(R) Xeon(R) Platinum 8171M CPU @ 2.60GHz: 
              speed         user         nice          sys         idle          irq
       #1  2095 MHz      69596 s          0 s       2957 s      31865 s          0 s
       #2  2095 MHz      76167 s          0 s       2930 s      25299 s          0 s
       
  Memory: 6.791393280029297 GB (3860.7578125 MB free)
  Uptime: 1083.0 sec
  Load Avg:  1.73681640625  1.607421875  1.13037109375
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
    Model:               85
    Model name:          Intel(R) Xeon(R) Platinum 8171M CPU @ 2.60GHz
    Stepping:            4
    CPU MHz:             2095.076
    BogoMIPS:            4190.15
    Hypervisor vendor:   Microsoft
    Virtualization type: full
    L1d cache:           32K
    L1i cache:           32K
    L2 cache:            1024K
    L3 cache:            36608K
    NUMA node0 CPU(s):   0,1
    Flags:               fpu vme de pse tsc msr pae mce cx8 apic sep mtrr pge mca cmov pat pse36 clflush mmx fxsr sse sse2 ss ht syscall nx pdpe1gb rdtscp lm constant_tsc rep_good nopl xtopology cpuid pni pclmulqdq ssse3 fma cx16 pcid sse4_1 sse4_2 movbe popcnt aes xsave avx f16c rdrand hypervisor lahf_lm abm 3dnowprefetch invpcid_single pti fsgsbase bmi1 hle avx2 smep bmi2 erms invpcid rtm mpx avx512f avx512dq rdseed adx smap clflushopt avx512cd avx512bw avx512vl xsaveopt xsavec xsaves md_clear
    

| Cpu Property       | Value                                                   |
|:------------------ |:------------------------------------------------------- |
| Brand              | Intel(R) Xeon(R) Platinum 8171M CPU @ 2.60GHz           |
| Vendor             | :Intel                                                  |
| Architecture       | :Skylake                                                |
| Model              | Family: 0x06, Model: 0x55, Stepping: 0x04, Type: 0x00   |
| Cores              | 2 physical cores, 2 logical cores (on executing CPU)    |
|                    | No Hyperthreading detected                              |
| Clock Frequencies  | Not supported by CPU                                    |
| Data Cache         | Level 1:3 : (32, 1024, 36608) kbytes                    |
|                    | 64 byte cache line size                                 |
| Address Size       | 48 bits virtual, 46 bits physical                       |
| SIMD               | 512 bit = 64 byte max. SIMD vector size                 |
| Time Stamp Counter | TSC is accessible via `rdtsc`                           |
|                    | TSC increased at every clock cycle (non-invariant TSC)  |
| Perf. Monitoring   | Performance Monitoring Counters (PMC) are not supported |
| Hypervisor         | Yes, Microsoft                                          |

