# Multi-thread benchmark result

* Pull request commit: [`7c6209cb0e801fab5b2da0b15ef8366260610084`](https://github.com/JuliaFolds/Transducers.jl/commit/7c6209cb0e801fab5b2da0b15ef8366260610084)
* Pull request: <https://github.com/JuliaFolds/Transducers.jl/pull/243> (Update */Manifest.toml)

# Judge result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmarks:
    - Target: 19 Nov 2020 - 00:55
    - Baseline: 19 Nov 2020 - 01:00
* Package commits:
    - Target: 9a454c
    - Baseline: b299e3
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

| ID                                                  | time ratio    | memory ratio                 |
|-----------------------------------------------------|---------------|------------------------------|
| `["collect", "unordered", "basesize=1024"]`         | 1.10 (5%) :x: |                1.09 (1%) :x: |
| `["overhead", "stoppable=true"]`                    | 1.06 (5%) :x: |                   1.00 (1%)  |
| `["parallel_histogram", "assoc", "basesize=4096"]`  |    0.99 (5%)  | 0.87 (1%) :white_check_mark: |
| `["parallel_histogram", "comm", "basesize=4096"]`   |    0.97 (5%)  |                1.01 (1%) :x: |
| `["parallel_histogram", "comm", "basesize=8192"]`   | 1.23 (5%) :x: |                1.02 (1%) :x: |
| `["words", "nthreads=2"]`                           | 1.09 (5%) :x: | 0.99 (1%) :white_check_mark: |
| `["words", "nthreads=4"]`                           | 1.08 (5%) :x: |                   1.00 (1%)  |

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
  uname: Linux 5.4.0-1031-azure #32~18.04.1-Ubuntu SMP Tue Oct 6 10:03:22 UTC 2020 x86_64 x86_64
  CPU: Intel(R) Xeon(R) Platinum 8171M CPU @ 2.60GHz: 
              speed         user         nice          sys         idle          irq
       #1  2095 MHz      48644 s          0 s       2396 s      16984 s          0 s
       #2  2095 MHz      49316 s          0 s       2404 s      16886 s          0 s
       
  Memory: 6.791393280029297 GB (3701.73046875 MB free)
  Uptime: 702.0 sec
  Load Avg:  1.5751953125  1.47998046875  0.88720703125
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
  uname: Linux 5.4.0-1031-azure #32~18.04.1-Ubuntu SMP Tue Oct 6 10:03:22 UTC 2020 x86_64 x86_64
  CPU: Intel(R) Xeon(R) Platinum 8171M CPU @ 2.60GHz: 
              speed         user         nice          sys         idle          irq
       #1  2095 MHz      71780 s          0 s       2997 s      23478 s          0 s
       #2  2095 MHz      72089 s          0 s       3038 s      23655 s          0 s
       
  Memory: 6.791393280029297 GB (3720.99609375 MB free)
  Uptime: 1004.0 sec
  Load Avg:  1.7138671875  1.57373046875  1.09375
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-9.0.1 (ORCJIT, skylake-avx512)
```

---
# Target result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmark: 19 Nov 2020 - 0:55
* Package commit: 9a454c
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

| ID                                                  | time            | GC time   | memory           | allocations |
|-----------------------------------------------------|----------------:|----------:|-----------------:|------------:|
| `["collect", "assoc", "basesize=1"]`                | 357.003 ms (5%) | 11.452 ms |   82.16 MiB (1%) |     1368053 |
| `["collect", "assoc", "basesize=1024"]`             | 238.234 ms (5%) |           |    1.83 MiB (1%) |        1597 |
| `["collect", "assoc", "basesize=32"]`               | 242.285 ms (5%) |           |    5.47 MiB (1%) |       47069 |
| `["collect", "seq"]`                                | 474.163 ms (5%) |           |  512.72 KiB (1%) |          15 |
| `["collect", "unordered", "basesize=1"]`            | 481.097 ms (5%) |           |   30.01 MiB (1%) |      360591 |
| `["collect", "unordered", "basesize=1024"]`         | 329.796 ms (5%) |           |  858.86 KiB (1%) |        4223 |
| `["collect", "unordered", "basesize=32"]`           | 261.760 ms (5%) |           |    1.46 MiB (1%) |       12250 |
| `["findfirst", "n=1000", "foldl"]`                  | 753.794 ms (5%) |           |                  |             |
| `["findfirst", "n=1000", "reduce", "basesize=128"]` | 382.172 ms (5%) |           |  546.33 KiB (1%) |        9561 |
| `["findfirst", "n=1000", "reduce", "basesize=256"]` | 380.830 ms (5%) |           |  278.25 KiB (1%) |        4888 |
| `["findfirst", "n=1000", "reduce", "basesize=512"]` | 387.532 ms (5%) |           |  144.66 KiB (1%) |        2550 |
| `["findfirst", "n=400", "foldl"]`                   | 565.487 ms (5%) |           |                  |             |
| `["findfirst", "n=400", "reduce", "basesize=128"]`  | 288.869 ms (5%) |           | 1012.91 KiB (1%) |       17727 |
| `["findfirst", "n=400", "reduce", "basesize=256"]`  | 286.842 ms (5%) |           |  509.63 KiB (1%) |        8952 |
| `["findfirst", "n=400", "reduce", "basesize=512"]`  | 288.290 ms (5%) |           |  258.84 KiB (1%) |        4564 |
| `["findfirst", "n=500", "foldl"]`                   |  98.036 ms (5%) |           |                  |             |
| `["findfirst", "n=500", "reduce", "basesize=128"]`  |  50.292 ms (5%) |           |  152.59 KiB (1%) |        2677 |
| `["findfirst", "n=500", "reduce", "basesize=256"]`  |  50.161 ms (5%) |           |   82.00 KiB (1%) |        1444 |
| `["findfirst", "n=500", "reduce", "basesize=512"]`  |  53.364 ms (5%) |           |   46.84 KiB (1%) |         828 |
| `["overhead", "default"]`                           | 173.501 μs (5%) |           |  140.75 KiB (1%) |        2465 |
| `["overhead", "stoppable=false"]`                   | 176.001 μs (5%) |           |  140.78 KiB (1%) |        2465 |
| `["overhead", "stoppable=true"]`                    | 324.603 μs (5%) |           |  140.81 KiB (1%) |        2466 |
| `["parallel_histogram", "assoc", "basesize=16384"]` |   5.320 ms (5%) |           |  731.81 KiB (1%) |          94 |
| `["parallel_histogram", "assoc", "basesize=4096"]`  |   6.041 ms (5%) |           |    1.80 MiB (1%) |         448 |
| `["parallel_histogram", "assoc", "basesize=8192"]`  |   5.695 ms (5%) |           |    1.43 MiB (1%) |         220 |
| `["parallel_histogram", "comm", "basesize=16384"]`  |  15.717 ms (5%) |           |    1.22 MiB (1%) |         182 |
| `["parallel_histogram", "comm", "basesize=4096"]`   |  23.131 ms (5%) |           |    1.05 MiB (1%) |        1976 |
| `["parallel_histogram", "comm", "basesize=8192"]`   |  21.772 ms (5%) |           |    1.26 MiB (1%) |        1499 |
| `["parallel_histogram", "seq"]`                     |   9.903 ms (5%) |           |  364.61 KiB (1%) |          24 |
| `["sum", "random", "foldl"]`                        |  19.066 ms (5%) |           |    32 bytes (1%) |           2 |
| `["sum", "random", "reduce", "basesize=128"]`       |   9.974 ms (5%) |           |  292.02 KiB (1%) |        5213 |
| `["sum", "random", "reduce", "basesize=256"]`       |   9.791 ms (5%) |           |  144.53 KiB (1%) |        2589 |
| `["sum", "random", "reduce", "basesize=512"]`       |   9.660 ms (5%) |           |   71.11 KiB (1%) |        1279 |
| `["sum", "uniform", "foldl"]`                       |  18.595 ms (5%) |           |    32 bytes (1%) |           2 |
| `["sum", "uniform", "reduce", "basesize=128"]`      |   9.707 ms (5%) |           |  292.02 KiB (1%) |        5213 |
| `["sum", "uniform", "reduce", "basesize=256"]`      |   9.560 ms (5%) |           |  144.53 KiB (1%) |        2589 |
| `["sum", "uniform", "reduce", "basesize=512"]`      |   9.437 ms (5%) |           |   71.06 KiB (1%) |        1278 |
| `["sum", "valley", "foldl"]`                        |  19.161 ms (5%) |           |    32 bytes (1%) |           2 |
| `["sum", "valley", "reduce", "basesize=128"]`       |  10.022 ms (5%) |           |  292.02 KiB (1%) |        5213 |
| `["sum", "valley", "reduce", "basesize=256"]`       |   9.860 ms (5%) |           |  144.53 KiB (1%) |        2589 |
| `["sum", "valley", "reduce", "basesize=512"]`       |   9.733 ms (5%) |           |   71.06 KiB (1%) |        1278 |
| `["words", "nthreads=1"]`                           |  25.166 ms (5%) |           |   31.79 MiB (1%) |     1035954 |
| `["words", "nthreads=2"]`                           |  17.225 ms (5%) |           |   32.14 MiB (1%) |     1036023 |
| `["words", "nthreads=4"]`                           |  17.535 ms (5%) |           |   32.86 MiB (1%) |     1036161 |

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
  uname: Linux 5.4.0-1031-azure #32~18.04.1-Ubuntu SMP Tue Oct 6 10:03:22 UTC 2020 x86_64 x86_64
  CPU: Intel(R) Xeon(R) Platinum 8171M CPU @ 2.60GHz: 
              speed         user         nice          sys         idle          irq
       #1  2095 MHz      48644 s          0 s       2396 s      16984 s          0 s
       #2  2095 MHz      49316 s          0 s       2404 s      16886 s          0 s
       
  Memory: 6.791393280029297 GB (3701.73046875 MB free)
  Uptime: 702.0 sec
  Load Avg:  1.5751953125  1.47998046875  0.88720703125
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-9.0.1 (ORCJIT, skylake-avx512)
```

---
# Baseline result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmark: 19 Nov 2020 - 1:0
* Package commit: b299e3
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

| ID                                                  | time            | GC time  | memory           | allocations |
|-----------------------------------------------------|----------------:|---------:|-----------------:|------------:|
| `["collect", "assoc", "basesize=1"]`                | 354.672 ms (5%) | 9.795 ms |   82.16 MiB (1%) |     1368050 |
| `["collect", "assoc", "basesize=1024"]`             | 238.343 ms (5%) |          |    1.83 MiB (1%) |        1597 |
| `["collect", "assoc", "basesize=32"]`               | 242.275 ms (5%) |          |    5.47 MiB (1%) |       47069 |
| `["collect", "seq"]`                                | 474.135 ms (5%) |          |  512.72 KiB (1%) |          15 |
| `["collect", "unordered", "basesize=1"]`            | 474.459 ms (5%) |          |   30.01 MiB (1%) |      360564 |
| `["collect", "unordered", "basesize=1024"]`         | 299.029 ms (5%) |          |  786.77 KiB (1%) |        1916 |
| `["collect", "unordered", "basesize=32"]`           | 261.952 ms (5%) |          |    1.46 MiB (1%) |       12088 |
| `["findfirst", "n=1000", "foldl"]`                  | 749.350 ms (5%) |          |                  |             |
| `["findfirst", "n=1000", "reduce", "basesize=128"]` | 379.625 ms (5%) |          |  546.34 KiB (1%) |        9562 |
| `["findfirst", "n=1000", "reduce", "basesize=256"]` | 378.346 ms (5%) |          |  278.25 KiB (1%) |        4888 |
| `["findfirst", "n=1000", "reduce", "basesize=512"]` | 385.108 ms (5%) |          |  144.66 KiB (1%) |        2550 |
| `["findfirst", "n=400", "foldl"]`                   | 562.408 ms (5%) |          |                  |             |
| `["findfirst", "n=400", "reduce", "basesize=128"]`  | 286.833 ms (5%) |          | 1012.91 KiB (1%) |       17727 |
| `["findfirst", "n=400", "reduce", "basesize=256"]`  | 284.944 ms (5%) |          |  509.63 KiB (1%) |        8952 |
| `["findfirst", "n=400", "reduce", "basesize=512"]`  | 286.000 ms (5%) |          |  258.83 KiB (1%) |        4563 |
| `["findfirst", "n=500", "foldl"]`                   |  97.591 ms (5%) |          |                  |             |
| `["findfirst", "n=500", "reduce", "basesize=128"]`  |  50.107 ms (5%) |          |  152.59 KiB (1%) |        2677 |
| `["findfirst", "n=500", "reduce", "basesize=256"]`  |  49.767 ms (5%) |          |   82.00 KiB (1%) |        1444 |
| `["findfirst", "n=500", "reduce", "basesize=512"]`  |  53.079 ms (5%) |          |   46.84 KiB (1%) |         828 |
| `["overhead", "default"]`                           | 175.701 μs (5%) |          |  140.72 KiB (1%) |        2464 |
| `["overhead", "stoppable=false"]`                   | 173.601 μs (5%) |          |  140.75 KiB (1%) |        2464 |
| `["overhead", "stoppable=true"]`                    | 306.301 μs (5%) |          |  140.78 KiB (1%) |        2465 |
| `["parallel_histogram", "assoc", "basesize=16384"]` |   5.341 ms (5%) |          |  731.81 KiB (1%) |          94 |
| `["parallel_histogram", "assoc", "basesize=4096"]`  |   6.118 ms (5%) |          |    2.07 MiB (1%) |         454 |
| `["parallel_histogram", "assoc", "basesize=8192"]`  |   5.707 ms (5%) |          |    1.43 MiB (1%) |         220 |
| `["parallel_histogram", "comm", "basesize=16384"]`  |  15.770 ms (5%) |          |    1.22 MiB (1%) |         205 |
| `["parallel_histogram", "comm", "basesize=4096"]`   |  23.900 ms (5%) |          |    1.03 MiB (1%) |        1910 |
| `["parallel_histogram", "comm", "basesize=8192"]`   |  17.766 ms (5%) |          |    1.24 MiB (1%) |         811 |
| `["parallel_histogram", "seq"]`                     |   9.840 ms (5%) |          |  364.61 KiB (1%) |          24 |
| `["sum", "random", "foldl"]`                        |  19.203 ms (5%) |          |    32 bytes (1%) |           2 |
| `["sum", "random", "reduce", "basesize=128"]`       |   9.992 ms (5%) |          |  292.02 KiB (1%) |        5213 |
| `["sum", "random", "reduce", "basesize=256"]`       |   9.810 ms (5%) |          |  144.53 KiB (1%) |        2589 |
| `["sum", "random", "reduce", "basesize=512"]`       |   9.741 ms (5%) |          |   71.11 KiB (1%) |        1279 |
| `["sum", "uniform", "foldl"]`                       |  18.451 ms (5%) |          |    32 bytes (1%) |           2 |
| `["sum", "uniform", "reduce", "basesize=128"]`      |   9.649 ms (5%) |          |  292.02 KiB (1%) |        5213 |
| `["sum", "uniform", "reduce", "basesize=256"]`      |   9.501 ms (5%) |          |  144.53 KiB (1%) |        2589 |
| `["sum", "uniform", "reduce", "basesize=512"]`      |   9.367 ms (5%) |          |   71.06 KiB (1%) |        1278 |
| `["sum", "valley", "foldl"]`                        |  19.264 ms (5%) |          |    32 bytes (1%) |           2 |
| `["sum", "valley", "reduce", "basesize=128"]`       |  10.019 ms (5%) |          |  292.02 KiB (1%) |        5213 |
| `["sum", "valley", "reduce", "basesize=256"]`       |   9.855 ms (5%) |          |  144.53 KiB (1%) |        2589 |
| `["sum", "valley", "reduce", "basesize=512"]`       |   9.732 ms (5%) |          |   71.06 KiB (1%) |        1278 |
| `["words", "nthreads=1"]`                           |  25.278 ms (5%) |          |   31.77 MiB (1%) |     1034881 |
| `["words", "nthreads=2"]`                           |  15.757 ms (5%) |          |   32.48 MiB (1%) |     1035019 |
| `["words", "nthreads=4"]`                           |  16.204 ms (5%) |          |   32.94 MiB (1%) |     1035166 |

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
  uname: Linux 5.4.0-1031-azure #32~18.04.1-Ubuntu SMP Tue Oct 6 10:03:22 UTC 2020 x86_64 x86_64
  CPU: Intel(R) Xeon(R) Platinum 8171M CPU @ 2.60GHz: 
              speed         user         nice          sys         idle          irq
       #1  2095 MHz      71780 s          0 s       2997 s      23478 s          0 s
       #2  2095 MHz      72089 s          0 s       3038 s      23655 s          0 s
       
  Memory: 6.791393280029297 GB (3720.99609375 MB free)
  Uptime: 1004.0 sec
  Load Avg:  1.7138671875  1.57373046875  1.09375
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
    CPU MHz:             2095.077
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

