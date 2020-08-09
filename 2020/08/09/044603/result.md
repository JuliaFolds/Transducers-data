# Multi-thread benchmark result

* Pull request commit: [`b1b48c2b922cbc37ca496b0cef8cb159b60b8a25`](https://github.com/JuliaFolds/Transducers.jl/commit/b1b48c2b922cbc37ca496b0cef8cb159b60b8a25)
* Pull request: <https://github.com/JuliaFolds/Transducers.jl/pull/404> (Add bench_filter_sum.jl)

# Judge result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmarks:
    - Target: 9 Aug 2020 - 04:40
    - Baseline: 9 Aug 2020 - 04:45
* Package commits:
    - Target: 6f7905
    - Baseline: 061a65
* Julia commits:
    - Target: 44fa15
    - Baseline: 44fa15
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
| `["collect", "unordered", "basesize=1024"]`         |                1.31 (5%) :x: |                1.17 (1%) :x: |
| `["collect", "unordered", "basesize=32"]`           |                   1.00 (5%)  | 0.97 (1%) :white_check_mark: |
| `["overhead", "stoppable=true"]`                    | 0.91 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["parallel_histogram", "comm", "basesize=4096"]`   |                1.12 (5%) :x: |                1.03 (1%) :x: |
| `["parallel_histogram", "comm", "basesize=8192"]`   | 0.92 (5%) :white_check_mark: | 0.99 (1%) :white_check_mark: |
| `["parallel_histogram", "seq"]`                     | 0.90 (5%) :white_check_mark: |                   1.00 (1%)  |

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
Julia Version 1.4.2
Commit 44fa15b150* (2020-05-23 18:35 UTC)
Platform Info:
  OS: Linux (x86_64-pc-linux-gnu)
      Ubuntu 18.04.4 LTS
  uname: Linux 5.3.0-1034-azure #35~18.04.1-Ubuntu SMP Mon Jul 13 12:54:45 UTC 2020 x86_64 x86_64
  CPU: Intel(R) Xeon(R) Platinum 8171M CPU @ 2.60GHz: 
              speed         user         nice          sys         idle          irq
       #1  2095 MHz      52007 s          0 s       2039 s      20613 s          0 s
       #2  2095 MHz      48458 s          0 s       2496 s      24261 s          0 s
       
  Memory: 6.764881134033203 GB (3034.6015625 MB free)
  Uptime: 770.0 sec
  Load Avg:  1.68603515625  1.51904296875  0.93115234375
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-8.0.1 (ORCJIT, skylake)
```

### Baseline
```
Julia Version 1.4.2
Commit 44fa15b150* (2020-05-23 18:35 UTC)
Platform Info:
  OS: Linux (x86_64-pc-linux-gnu)
      Ubuntu 18.04.4 LTS
  uname: Linux 5.3.0-1034-azure #35~18.04.1-Ubuntu SMP Mon Jul 13 12:54:45 UTC 2020 x86_64 x86_64
  CPU: Intel(R) Xeon(R) Platinum 8171M CPU @ 2.60GHz: 
              speed         user         nice          sys         idle          irq
       #1  2095 MHz      75207 s          0 s       2471 s      26089 s          0 s
       #2  2095 MHz      70329 s          0 s       2981 s      31043 s          0 s
       
  Memory: 6.764881134033203 GB (3009.85546875 MB free)
  Uptime: 1063.0 sec
  Load Avg:  1.7255859375  1.587890625  1.119140625
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-8.0.1 (ORCJIT, skylake)
```

---
# Target result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmark: 9 Aug 2020 - 4:40
* Package commit: 6f7905
* Julia commit: 44fa15
* Julia command flags: None
* Environment variables: `JULIA_NUM_THREADS => 2`

## Results
Below is a table of this job's results, obtained by running the benchmarks.
The values listed in the `ID` column have the structure `[parent_group, child_group, ..., key]`, and can be used to
index into the BaseBenchmarks suite to retrieve the corresponding benchmarks.
The percentages accompanying time and memory values in the below table are noise tolerances. The "true"
time/memory value for a given benchmark is expected to fall within this percentage of the reported value.
An empty cell means that the value was zero.

| ID                                                  | time            | GC time   | memory          | allocations |
|-----------------------------------------------------|----------------:|----------:|----------------:|------------:|
| `["collect", "assoc", "basesize=1"]`                | 356.780 ms (5%) | 10.038 ms |  87.55 MiB (1%) |     1590746 |
| `["collect", "assoc", "basesize=1024"]`             | 221.156 ms (5%) |           |   1.84 MiB (1%) |        1812 |
| `["collect", "assoc", "basesize=32"]`               | 220.833 ms (5%) |           |   5.64 MiB (1%) |       54017 |
| `["collect", "seq"]`                                | 420.512 ms (5%) |           |   1.50 MiB (1%) |       32784 |
| `["collect", "unordered", "basesize=1"]`            | 452.535 ms (5%) |           |  29.16 MiB (1%) |      403265 |
| `["collect", "unordered", "basesize=1024"]`         | 336.062 ms (5%) |           | 909.45 KiB (1%) |       11297 |
| `["collect", "unordered", "basesize=32"]`           | 249.721 ms (5%) |           |   1.43 MiB (1%) |       14206 |
| `["findfirst", "n=1000", "foldl"]`                  | 686.713 ms (5%) |           |                 |             |
| `["findfirst", "n=1000", "reduce", "basesize=128"]` | 358.111 ms (5%) |           | 564.00 KiB (1%) |       10223 |
| `["findfirst", "n=1000", "reduce", "basesize=256"]` | 360.677 ms (5%) |           | 287.23 KiB (1%) |        5221 |
| `["findfirst", "n=1000", "reduce", "basesize=512"]` | 367.410 ms (5%) |           | 149.36 KiB (1%) |        2724 |
| `["findfirst", "n=400", "foldl"]`                   | 516.054 ms (5%) |           |                 |             |
| `["findfirst", "n=400", "reduce", "basesize=128"]`  | 269.171 ms (5%) |           |   1.02 MiB (1%) |       18886 |
| `["findfirst", "n=400", "reduce", "basesize=256"]`  | 269.016 ms (5%) |           | 525.78 KiB (1%) |        9546 |
| `["findfirst", "n=400", "reduce", "basesize=512"]`  | 266.468 ms (5%) |           | 267.23 KiB (1%) |        4876 |
| `["findfirst", "n=500", "foldl"]`                   |  85.496 ms (5%) |           |                 |             |
| `["findfirst", "n=500", "reduce", "basesize=128"]`  |  45.221 ms (5%) |           | 157.28 KiB (1%) |        2843 |
| `["findfirst", "n=500", "reduce", "basesize=256"]`  |  43.903 ms (5%) |           |  84.50 KiB (1%) |        1530 |
| `["findfirst", "n=500", "reduce", "basesize=512"]`  |  46.393 ms (5%) |           |  48.30 KiB (1%) |         878 |
| `["overhead", "default"]`                           | 175.012 μs (5%) |           | 146.27 KiB (1%) |        2633 |
| `["overhead", "stoppable=false"]`                   | 180.213 μs (5%) |           | 146.28 KiB (1%) |        2633 |
| `["overhead", "stoppable=true"]`                    | 301.120 μs (5%) |           | 146.55 KiB (1%) |        2650 |
| `["parallel_histogram", "assoc", "basesize=16384"]` |   4.324 ms (5%) |           | 732.06 KiB (1%) |         103 |
| `["parallel_histogram", "assoc", "basesize=4096"]`  |   5.157 ms (5%) |           |   1.80 MiB (1%) |         497 |
| `["parallel_histogram", "assoc", "basesize=8192"]`  |   4.638 ms (5%) |           |   1.43 MiB (1%) |         243 |
| `["parallel_histogram", "comm", "basesize=16384"]`  |  14.715 ms (5%) |           |   1.22 MiB (1%) |         159 |
| `["parallel_histogram", "comm", "basesize=4096"]`   |  25.139 ms (5%) |           |   1.05 MiB (1%) |        1722 |
| `["parallel_histogram", "comm", "basesize=8192"]`   |  18.774 ms (5%) |           |   1.25 MiB (1%) |        1855 |
| `["parallel_histogram", "seq"]`                     |   7.310 ms (5%) |           | 364.61 KiB (1%) |          24 |
| `["sum", "random", "foldl"]`                        |  15.570 ms (5%) |           |   64 bytes (1%) |           3 |
| `["sum", "random", "reduce", "basesize=128"]`       |   8.571 ms (5%) |           | 313.42 KiB (1%) |        6071 |
| `["sum", "random", "reduce", "basesize=256"]`       |   8.367 ms (5%) |           | 155.17 KiB (1%) |        3014 |
| `["sum", "random", "reduce", "basesize=512"]`       |   8.234 ms (5%) |           |  76.31 KiB (1%) |        1486 |
| `["sum", "uniform", "foldl"]`                       |  15.630 ms (5%) |           |   64 bytes (1%) |           3 |
| `["sum", "uniform", "reduce", "basesize=128"]`      |   8.185 ms (5%) |           | 313.44 KiB (1%) |        6072 |
| `["sum", "uniform", "reduce", "basesize=256"]`      |   7.984 ms (5%) |           | 155.14 KiB (1%) |        3012 |
| `["sum", "uniform", "reduce", "basesize=512"]`      |   8.026 ms (5%) |           |  76.31 KiB (1%) |        1486 |
| `["sum", "valley", "foldl"]`                        |  15.517 ms (5%) |           |   64 bytes (1%) |           3 |
| `["sum", "valley", "reduce", "basesize=128"]`       |   8.520 ms (5%) |           | 313.36 KiB (1%) |        6067 |
| `["sum", "valley", "reduce", "basesize=256"]`       |   8.373 ms (5%) |           | 155.14 KiB (1%) |        3012 |
| `["sum", "valley", "reduce", "basesize=512"]`       |   8.124 ms (5%) |           |  76.33 KiB (1%) |        1487 |
| `["words", "nthreads=1"]`                           |  34.067 ms (5%) |  7.224 ms |  63.30 MiB (1%) |     2068283 |
| `["words", "nthreads=2"]`                           |  17.840 ms (5%) |           |  64.39 MiB (1%) |     2080591 |
| `["words", "nthreads=4"]`                           |  19.232 ms (5%) |           |  65.33 MiB (1%) |     2091051 |

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
Julia Version 1.4.2
Commit 44fa15b150* (2020-05-23 18:35 UTC)
Platform Info:
  OS: Linux (x86_64-pc-linux-gnu)
      Ubuntu 18.04.4 LTS
  uname: Linux 5.3.0-1034-azure #35~18.04.1-Ubuntu SMP Mon Jul 13 12:54:45 UTC 2020 x86_64 x86_64
  CPU: Intel(R) Xeon(R) Platinum 8171M CPU @ 2.60GHz: 
              speed         user         nice          sys         idle          irq
       #1  2095 MHz      52007 s          0 s       2039 s      20613 s          0 s
       #2  2095 MHz      48458 s          0 s       2496 s      24261 s          0 s
       
  Memory: 6.764881134033203 GB (3034.6015625 MB free)
  Uptime: 770.0 sec
  Load Avg:  1.68603515625  1.51904296875  0.93115234375
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-8.0.1 (ORCJIT, skylake)
```

---
# Baseline result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmark: 9 Aug 2020 - 4:45
* Package commit: 061a65
* Julia commit: 44fa15
* Julia command flags: None
* Environment variables: `JULIA_NUM_THREADS => 2`

## Results
Below is a table of this job's results, obtained by running the benchmarks.
The values listed in the `ID` column have the structure `[parent_group, child_group, ..., key]`, and can be used to
index into the BaseBenchmarks suite to retrieve the corresponding benchmarks.
The percentages accompanying time and memory values in the below table are noise tolerances. The "true"
time/memory value for a given benchmark is expected to fall within this percentage of the reported value.
An empty cell means that the value was zero.

| ID                                                  | time            | GC time   | memory          | allocations |
|-----------------------------------------------------|----------------:|----------:|----------------:|------------:|
| `["collect", "assoc", "basesize=1"]`                | 357.374 ms (5%) | 10.445 ms |  87.55 MiB (1%) |     1590790 |
| `["collect", "assoc", "basesize=1024"]`             | 222.037 ms (5%) |           |   1.84 MiB (1%) |        1813 |
| `["collect", "assoc", "basesize=32"]`               | 227.317 ms (5%) |           |   5.64 MiB (1%) |       54019 |
| `["collect", "seq"]`                                | 431.937 ms (5%) |           |   1.50 MiB (1%) |       32784 |
| `["collect", "unordered", "basesize=1"]`            | 456.605 ms (5%) |           |  29.16 MiB (1%) |      403357 |
| `["collect", "unordered", "basesize=1024"]`         | 256.136 ms (5%) |           | 779.02 KiB (1%) |        2568 |
| `["collect", "unordered", "basesize=32"]`           | 250.671 ms (5%) |           |   1.47 MiB (1%) |       16958 |
| `["findfirst", "n=1000", "foldl"]`                  | 685.610 ms (5%) |           |                 |             |
| `["findfirst", "n=1000", "reduce", "basesize=128"]` | 360.112 ms (5%) |           | 563.88 KiB (1%) |       10215 |
| `["findfirst", "n=1000", "reduce", "basesize=256"]` | 355.708 ms (5%) |           | 287.25 KiB (1%) |        5222 |
| `["findfirst", "n=1000", "reduce", "basesize=512"]` | 362.508 ms (5%) |           | 149.36 KiB (1%) |        2724 |
| `["findfirst", "n=400", "foldl"]`                   | 525.451 ms (5%) |           |                 |             |
| `["findfirst", "n=400", "reduce", "basesize=128"]`  | 271.794 ms (5%) |           |   1.02 MiB (1%) |       18913 |
| `["findfirst", "n=400", "reduce", "basesize=256"]`  | 268.428 ms (5%) |           | 525.66 KiB (1%) |        9538 |
| `["findfirst", "n=400", "reduce", "basesize=512"]`  | 270.075 ms (5%) |           | 267.13 KiB (1%) |        4869 |
| `["findfirst", "n=500", "foldl"]`                   |  85.684 ms (5%) |           |                 |             |
| `["findfirst", "n=500", "reduce", "basesize=128"]`  |  45.594 ms (5%) |           | 157.22 KiB (1%) |        2839 |
| `["findfirst", "n=500", "reduce", "basesize=256"]`  |  44.923 ms (5%) |           |  84.52 KiB (1%) |        1531 |
| `["findfirst", "n=500", "reduce", "basesize=512"]`  |  48.037 ms (5%) |           |  48.30 KiB (1%) |         878 |
| `["overhead", "default"]`                           | 173.423 μs (5%) |           | 146.27 KiB (1%) |        2633 |
| `["overhead", "stoppable=false"]`                   | 176.123 μs (5%) |           | 146.23 KiB (1%) |        2630 |
| `["overhead", "stoppable=true"]`                    | 331.744 μs (5%) |           | 146.53 KiB (1%) |        2649 |
| `["parallel_histogram", "assoc", "basesize=16384"]` |   4.430 ms (5%) |           | 732.06 KiB (1%) |         103 |
| `["parallel_histogram", "assoc", "basesize=4096"]`  |   5.046 ms (5%) |           |   1.80 MiB (1%) |         497 |
| `["parallel_histogram", "assoc", "basesize=8192"]`  |   4.745 ms (5%) |           |   1.43 MiB (1%) |         243 |
| `["parallel_histogram", "comm", "basesize=16384"]`  |  14.948 ms (5%) |           |   1.22 MiB (1%) |         159 |
| `["parallel_histogram", "comm", "basesize=4096"]`   |  22.353 ms (5%) |           |   1.02 MiB (1%) |        3410 |
| `["parallel_histogram", "comm", "basesize=8192"]`   |  20.304 ms (5%) |           |   1.26 MiB (1%) |        2867 |
| `["parallel_histogram", "seq"]`                     |   8.109 ms (5%) |           | 364.61 KiB (1%) |          24 |
| `["sum", "random", "foldl"]`                        |  15.493 ms (5%) |           |   64 bytes (1%) |           3 |
| `["sum", "random", "reduce", "basesize=128"]`       |   8.752 ms (5%) |           | 313.41 KiB (1%) |        6070 |
| `["sum", "random", "reduce", "basesize=256"]`       |   8.252 ms (5%) |           | 155.13 KiB (1%) |        3011 |
| `["sum", "random", "reduce", "basesize=512"]`       |   8.200 ms (5%) |           |  76.33 KiB (1%) |        1487 |
| `["sum", "uniform", "foldl"]`                       |  14.928 ms (5%) |           |   64 bytes (1%) |           3 |
| `["sum", "uniform", "reduce", "basesize=128"]`      |   8.132 ms (5%) |           | 313.42 KiB (1%) |        6071 |
| `["sum", "uniform", "reduce", "basesize=256"]`      |   7.845 ms (5%) |           | 155.16 KiB (1%) |        3013 |
| `["sum", "uniform", "reduce", "basesize=512"]`      |   7.761 ms (5%) |           |  76.31 KiB (1%) |        1486 |
| `["sum", "valley", "foldl"]`                        |  15.492 ms (5%) |           |   64 bytes (1%) |           3 |
| `["sum", "valley", "reduce", "basesize=128"]`       |   8.614 ms (5%) |           | 313.36 KiB (1%) |        6067 |
| `["sum", "valley", "reduce", "basesize=256"]`       |   8.557 ms (5%) |           | 155.16 KiB (1%) |        3013 |
| `["sum", "valley", "reduce", "basesize=512"]`       |   8.321 ms (5%) |           |  76.33 KiB (1%) |        1487 |
| `["words", "nthreads=1"]`                           |  33.619 ms (5%) |  6.665 ms |  63.18 MiB (1%) |     2064540 |
| `["words", "nthreads=2"]`                           |  18.182 ms (5%) |           |  63.78 MiB (1%) |     2072644 |
| `["words", "nthreads=4"]`                           |  19.055 ms (5%) |           |  64.74 MiB (1%) |     2080830 |

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
Julia Version 1.4.2
Commit 44fa15b150* (2020-05-23 18:35 UTC)
Platform Info:
  OS: Linux (x86_64-pc-linux-gnu)
      Ubuntu 18.04.4 LTS
  uname: Linux 5.3.0-1034-azure #35~18.04.1-Ubuntu SMP Mon Jul 13 12:54:45 UTC 2020 x86_64 x86_64
  CPU: Intel(R) Xeon(R) Platinum 8171M CPU @ 2.60GHz: 
              speed         user         nice          sys         idle          irq
       #1  2095 MHz      75207 s          0 s       2471 s      26089 s          0 s
       #2  2095 MHz      70329 s          0 s       2981 s      31043 s          0 s
       
  Memory: 6.764881134033203 GB (3009.85546875 MB free)
  Uptime: 1063.0 sec
  Load Avg:  1.7255859375  1.587890625  1.119140625
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-8.0.1 (ORCJIT, skylake)
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
    CPU MHz:             2095.244
    BogoMIPS:            4190.48
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
| Address Size       | 48 bits virtual, 44 bits physical                       |
| SIMD               | 512 bit = 64 byte max. SIMD vector size                 |
| Time Stamp Counter | TSC is accessible via `rdtsc`                           |
|                    | TSC increased at every clock cycle (non-invariant TSC)  |
| Perf. Monitoring   | Performance Monitoring Counters (PMC) are not supported |
| Hypervisor         | Yes, Microsoft                                          |

