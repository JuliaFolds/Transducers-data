# Multi-thread benchmark result (via Travis)


# Judge result
# Benchmark Report for */home/travis/build/JuliaFolds/Transducers.jl*

## Job Properties
* Time of benchmarks:
    - Target: 3 Aug 2020 - 07:29
    - Baseline: 3 Aug 2020 - 07:33
* Package commits:
    - Target: 80b639
    - Baseline: 64beaa
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
| `["collect", "unordered", "basesize=1024"]`         |                1.07 (5%) :x: |                1.03 (1%) :x: |
| `["parallel_histogram", "assoc", "basesize=4096"]`  |                   0.99 (5%)  | 0.87 (1%) :white_check_mark: |
| `["parallel_histogram", "comm", "basesize=16384"]`  | 0.94 (5%) :white_check_mark: |                1.02 (1%) :x: |
| `["parallel_histogram", "comm", "basesize=4096"]`   |                   0.99 (5%)  |                1.04 (1%) :x: |
| `["parallel_histogram", "comm", "basesize=8192"]`   |                   0.95 (5%)  | 0.99 (1%) :white_check_mark: |
| `["words", "nthreads=1"]`                           |                   0.99 (5%)  | 0.99 (1%) :white_check_mark: |
| `["words", "nthreads=2"]`                           |                   0.97 (5%)  | 0.99 (1%) :white_check_mark: |
| `["words", "nthreads=4"]`                           |                   0.96 (5%)  | 0.98 (1%) :white_check_mark: |

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
      Ubuntu 16.04.6 LTS
  uname: Linux 4.15.0-1028-gcp #29~16.04.1-Ubuntu SMP Tue Feb 12 16:31:10 UTC 2019 x86_64 x86_64
  CPU: Intel(R) Xeon(R) CPU: 
              speed         user         nice          sys         idle          irq
       #1  2800 MHz      50046 s          0 s       2236 s      14440 s          0 s
       #2  2800 MHz      48836 s          0 s       1745 s      16328 s          0 s
       
  Memory: 7.7900238037109375 GB (5808.66796875 MB free)
  Uptime: 675.0 sec
  Load Avg:  1.7607421875  1.50048828125  0.8583984375
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
      Ubuntu 16.04.6 LTS
  uname: Linux 4.15.0-1028-gcp #29~16.04.1-Ubuntu SMP Tue Feb 12 16:31:10 UTC 2019 x86_64 x86_64
  CPU: Intel(R) Xeon(R) CPU: 
              speed         user         nice          sys         idle          irq
       #1  2800 MHz      72237 s          0 s       2620 s      20299 s          0 s
       #2  2800 MHz      71106 s          0 s       2332 s      21803 s          0 s
       
  Memory: 7.7900238037109375 GB (5817.5390625 MB free)
  Uptime: 960.0 sec
  Load Avg:  1.71826171875  1.57373046875  1.0615234375
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-8.0.1 (ORCJIT, skylake)
```

---
# Target result
# Benchmark Report for */home/travis/build/JuliaFolds/Transducers.jl*

## Job Properties
* Time of benchmark: 3 Aug 2020 - 7:29
* Package commit: 80b639
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
| `["collect", "assoc", "basesize=1"]`                | 318.796 ms (5%) | 12.329 ms |  87.55 MiB (1%) |     1590732 |
| `["collect", "assoc", "basesize=1024"]`             | 179.205 ms (5%) |           |   1.84 MiB (1%) |        1807 |
| `["collect", "assoc", "basesize=32"]`               | 183.935 ms (5%) |           |   5.64 MiB (1%) |       54008 |
| `["collect", "seq"]`                                | 349.605 ms (5%) |           |   1.50 MiB (1%) |       32784 |
| `["collect", "unordered", "basesize=1"]`            | 368.204 ms (5%) |           |  29.15 MiB (1%) |      402782 |
| `["collect", "unordered", "basesize=1024"]`         | 217.463 ms (5%) |           | 871.38 KiB (1%) |        8860 |
| `["collect", "unordered", "basesize=32"]`           | 205.129 ms (5%) |           |   1.52 MiB (1%) |       19853 |
| `["findfirst", "n=1000", "foldl"]`                  | 556.311 ms (5%) |           |                 |             |
| `["findfirst", "n=1000", "reduce", "basesize=128"]` | 314.540 ms (5%) |           | 563.86 KiB (1%) |       10214 |
| `["findfirst", "n=1000", "reduce", "basesize=256"]` | 306.836 ms (5%) |           | 287.17 KiB (1%) |        5217 |
| `["findfirst", "n=1000", "reduce", "basesize=512"]` | 308.267 ms (5%) |           | 149.31 KiB (1%) |        2721 |
| `["findfirst", "n=400", "foldl"]`                   | 417.619 ms (5%) |           |                 |             |
| `["findfirst", "n=400", "reduce", "basesize=128"]`  | 252.721 ms (5%) |           |   1.02 MiB (1%) |       18941 |
| `["findfirst", "n=400", "reduce", "basesize=256"]`  | 238.570 ms (5%) |           | 525.95 KiB (1%) |        9557 |
| `["findfirst", "n=400", "reduce", "basesize=512"]`  | 233.612 ms (5%) |           | 267.19 KiB (1%) |        4873 |
| `["findfirst", "n=500", "foldl"]`                   |  72.365 ms (5%) |           |                 |             |
| `["findfirst", "n=500", "reduce", "basesize=128"]`  |  43.228 ms (5%) |           | 157.34 KiB (1%) |        2847 |
| `["findfirst", "n=500", "reduce", "basesize=256"]`  |  41.263 ms (5%) |           |  84.58 KiB (1%) |        1535 |
| `["findfirst", "n=500", "reduce", "basesize=512"]`  |  42.972 ms (5%) |           |  48.33 KiB (1%) |         880 |
| `["overhead", "default"]`                           | 221.791 μs (5%) |           | 146.28 KiB (1%) |        2634 |
| `["overhead", "stoppable=false"]`                   | 220.257 μs (5%) |           | 146.28 KiB (1%) |        2633 |
| `["overhead", "stoppable=true"]`                    | 419.674 μs (5%) |           | 146.58 KiB (1%) |        2652 |
| `["parallel_histogram", "assoc", "basesize=16384"]` |   4.784 ms (5%) |           | 732.06 KiB (1%) |         103 |
| `["parallel_histogram", "assoc", "basesize=4096"]`  |   5.611 ms (5%) |           |   1.80 MiB (1%) |         497 |
| `["parallel_histogram", "assoc", "basesize=8192"]`  |   5.201 ms (5%) |           |   1.43 MiB (1%) |         242 |
| `["parallel_histogram", "comm", "basesize=16384"]`  |  11.787 ms (5%) |           |   1.24 MiB (1%) |        1450 |
| `["parallel_histogram", "comm", "basesize=4096"]`   |  18.548 ms (5%) |           |   1.15 MiB (1%) |        7447 |
| `["parallel_histogram", "comm", "basesize=8192"]`   |  14.675 ms (5%) |           |   1.26 MiB (1%) |        2628 |
| `["parallel_histogram", "seq"]`                     |   7.449 ms (5%) |           | 364.61 KiB (1%) |          24 |
| `["sum", "random", "foldl"]`                        |  14.067 ms (5%) |           |   64 bytes (1%) |           3 |
| `["sum", "random", "reduce", "basesize=128"]`       |   8.002 ms (5%) |           | 313.45 KiB (1%) |        6073 |
| `["sum", "random", "reduce", "basesize=256"]`       |   7.774 ms (5%) |           | 155.11 KiB (1%) |        3010 |
| `["sum", "random", "reduce", "basesize=512"]`       |   7.657 ms (5%) |           |  76.34 KiB (1%) |        1488 |
| `["sum", "uniform", "foldl"]`                       |  13.671 ms (5%) |           |   64 bytes (1%) |           3 |
| `["sum", "uniform", "reduce", "basesize=128"]`      |   7.781 ms (5%) |           | 313.41 KiB (1%) |        6070 |
| `["sum", "uniform", "reduce", "basesize=256"]`      |   7.549 ms (5%) |           | 155.14 KiB (1%) |        3012 |
| `["sum", "uniform", "reduce", "basesize=512"]`      |   7.436 ms (5%) |           |  76.31 KiB (1%) |        1486 |
| `["sum", "valley", "foldl"]`                        |  14.132 ms (5%) |           |   64 bytes (1%) |           3 |
| `["sum", "valley", "reduce", "basesize=128"]`       |   8.052 ms (5%) |           | 313.34 KiB (1%) |        6066 |
| `["sum", "valley", "reduce", "basesize=256"]`       |   7.834 ms (5%) |           | 155.16 KiB (1%) |        3013 |
| `["sum", "valley", "reduce", "basesize=512"]`       |   7.688 ms (5%) |           |  76.36 KiB (1%) |        1489 |
| `["words", "nthreads=1"]`                           |  40.074 ms (5%) |  6.595 ms |  62.66 MiB (1%) |     2047148 |
| `["words", "nthreads=2"]`                           |  37.178 ms (5%) |           |  63.26 MiB (1%) |     2055276 |
| `["words", "nthreads=4"]`                           |  38.309 ms (5%) |           |  64.23 MiB (1%) |     2063555 |

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
      Ubuntu 16.04.6 LTS
  uname: Linux 4.15.0-1028-gcp #29~16.04.1-Ubuntu SMP Tue Feb 12 16:31:10 UTC 2019 x86_64 x86_64
  CPU: Intel(R) Xeon(R) CPU: 
              speed         user         nice          sys         idle          irq
       #1  2800 MHz      50046 s          0 s       2236 s      14440 s          0 s
       #2  2800 MHz      48836 s          0 s       1745 s      16328 s          0 s
       
  Memory: 7.7900238037109375 GB (5808.66796875 MB free)
  Uptime: 675.0 sec
  Load Avg:  1.7607421875  1.50048828125  0.8583984375
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-8.0.1 (ORCJIT, skylake)
```

---
# Baseline result
# Benchmark Report for */home/travis/build/JuliaFolds/Transducers.jl*

## Job Properties
* Time of benchmark: 3 Aug 2020 - 7:33
* Package commit: 64beaa
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
| `["collect", "assoc", "basesize=1"]`                | 319.256 ms (5%) | 10.459 ms |  87.55 MiB (1%) |     1590670 |
| `["collect", "assoc", "basesize=1024"]`             | 179.270 ms (5%) |           |   1.84 MiB (1%) |        1811 |
| `["collect", "assoc", "basesize=32"]`               | 183.666 ms (5%) |           |   5.64 MiB (1%) |       54011 |
| `["collect", "seq"]`                                | 349.620 ms (5%) |           |   1.50 MiB (1%) |       32784 |
| `["collect", "unordered", "basesize=1"]`            | 367.474 ms (5%) |           |  29.15 MiB (1%) |      402933 |
| `["collect", "unordered", "basesize=1024"]`         | 204.099 ms (5%) |           | 841.95 KiB (1%) |        6641 |
| `["collect", "unordered", "basesize=32"]`           | 205.201 ms (5%) |           |   1.50 MiB (1%) |       18920 |
| `["findfirst", "n=1000", "foldl"]`                  | 550.777 ms (5%) |           |                 |             |
| `["findfirst", "n=1000", "reduce", "basesize=128"]` | 309.820 ms (5%) |           | 563.84 KiB (1%) |       10213 |
| `["findfirst", "n=1000", "reduce", "basesize=256"]` | 302.139 ms (5%) |           | 287.34 KiB (1%) |        5228 |
| `["findfirst", "n=1000", "reduce", "basesize=512"]` | 303.646 ms (5%) |           | 149.39 KiB (1%) |        2726 |
| `["findfirst", "n=400", "foldl"]`                   | 413.458 ms (5%) |           |                 |             |
| `["findfirst", "n=400", "reduce", "basesize=128"]`  | 249.502 ms (5%) |           |   1.02 MiB (1%) |       18953 |
| `["findfirst", "n=400", "reduce", "basesize=256"]`  | 235.150 ms (5%) |           | 526.05 KiB (1%) |        9563 |
| `["findfirst", "n=400", "reduce", "basesize=512"]`  | 230.219 ms (5%) |           | 267.19 KiB (1%) |        4873 |
| `["findfirst", "n=500", "foldl"]`                   |  71.647 ms (5%) |           |                 |             |
| `["findfirst", "n=500", "reduce", "basesize=128"]`  |  42.624 ms (5%) |           | 157.41 KiB (1%) |        2851 |
| `["findfirst", "n=500", "reduce", "basesize=256"]`  |  40.693 ms (5%) |           |  84.59 KiB (1%) |        1536 |
| `["findfirst", "n=500", "reduce", "basesize=512"]`  |  42.344 ms (5%) |           |  48.30 KiB (1%) |         878 |
| `["overhead", "default"]`                           | 221.585 μs (5%) |           | 146.27 KiB (1%) |        2633 |
| `["overhead", "stoppable=false"]`                   | 220.990 μs (5%) |           | 146.28 KiB (1%) |        2633 |
| `["overhead", "stoppable=true"]`                    | 422.045 μs (5%) |           | 146.58 KiB (1%) |        2652 |
| `["parallel_histogram", "assoc", "basesize=16384"]` |   4.776 ms (5%) |           | 732.06 KiB (1%) |         103 |
| `["parallel_histogram", "assoc", "basesize=4096"]`  |   5.671 ms (5%) |           |   2.07 MiB (1%) |         503 |
| `["parallel_histogram", "assoc", "basesize=8192"]`  |   5.186 ms (5%) |           |   1.43 MiB (1%) |         243 |
| `["parallel_histogram", "comm", "basesize=16384"]`  |  12.599 ms (5%) |           |   1.22 MiB (1%) |         159 |
| `["parallel_histogram", "comm", "basesize=4096"]`   |  18.723 ms (5%) |           |   1.11 MiB (1%) |        9389 |
| `["parallel_histogram", "comm", "basesize=8192"]`   |  15.395 ms (5%) |           |   1.27 MiB (1%) |        3465 |
| `["parallel_histogram", "seq"]`                     |   7.386 ms (5%) |           | 364.61 KiB (1%) |          24 |
| `["sum", "random", "foldl"]`                        |  14.053 ms (5%) |           |   64 bytes (1%) |           3 |
| `["sum", "random", "reduce", "basesize=128"]`       |   7.995 ms (5%) |           | 313.42 KiB (1%) |        6071 |
| `["sum", "random", "reduce", "basesize=256"]`       |   7.762 ms (5%) |           | 155.17 KiB (1%) |        3014 |
| `["sum", "random", "reduce", "basesize=512"]`       |   7.643 ms (5%) |           |  76.31 KiB (1%) |        1486 |
| `["sum", "uniform", "foldl"]`                       |  13.657 ms (5%) |           |   64 bytes (1%) |           3 |
| `["sum", "uniform", "reduce", "basesize=128"]`      |   7.782 ms (5%) |           | 313.42 KiB (1%) |        6071 |
| `["sum", "uniform", "reduce", "basesize=256"]`      |   7.542 ms (5%) |           | 155.14 KiB (1%) |        3012 |
| `["sum", "uniform", "reduce", "basesize=512"]`      |   7.434 ms (5%) |           |  76.31 KiB (1%) |        1486 |
| `["sum", "valley", "foldl"]`                        |  14.130 ms (5%) |           |   64 bytes (1%) |           3 |
| `["sum", "valley", "reduce", "basesize=128"]`       |   8.022 ms (5%) |           | 313.36 KiB (1%) |        6067 |
| `["sum", "valley", "reduce", "basesize=256"]`       |   7.805 ms (5%) |           | 155.16 KiB (1%) |        3013 |
| `["sum", "valley", "reduce", "basesize=512"]`       |   7.685 ms (5%) |           |  76.34 KiB (1%) |        1488 |
| `["words", "nthreads=1"]`                           |  40.463 ms (5%) |  6.574 ms |  63.49 MiB (1%) |     2074386 |
| `["words", "nthreads=2"]`                           |  38.300 ms (5%) |           |  64.10 MiB (1%) |     2082519 |
| `["words", "nthreads=4"]`                           |  39.710 ms (5%) |           |  65.37 MiB (1%) |     2094976 |

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
      Ubuntu 16.04.6 LTS
  uname: Linux 4.15.0-1028-gcp #29~16.04.1-Ubuntu SMP Tue Feb 12 16:31:10 UTC 2019 x86_64 x86_64
  CPU: Intel(R) Xeon(R) CPU: 
              speed         user         nice          sys         idle          irq
       #1  2800 MHz      72237 s          0 s       2620 s      20299 s          0 s
       #2  2800 MHz      71106 s          0 s       2332 s      21803 s          0 s
       
  Memory: 7.7900238037109375 GB (5817.5390625 MB free)
  Uptime: 960.0 sec
  Load Avg:  1.71826171875  1.57373046875  1.0615234375
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

    Architecture:          x86_64
    CPU op-mode(s):        32-bit, 64-bit
    Byte Order:            Little Endian
    CPU(s):                2
    On-line CPU(s) list:   0,1
    Thread(s) per core:    2
    Core(s) per socket:    1
    Socket(s):             1
    NUMA node(s):          1
    Vendor ID:             GenuineIntel
    CPU family:            6
    Model:                 85
    Model name:            Intel(R) Xeon(R) CPU
    Stepping:              7
    CPU MHz:               2800.212
    BogoMIPS:              5600.42
    Hypervisor vendor:     KVM
    Virtualization type:   full
    L1d cache:             32K
    L1i cache:             32K
    L2 cache:              1024K
    L3 cache:              33792K
    NUMA node0 CPU(s):     0,1
    Flags:                 fpu vme de pse tsc msr pae mce cx8 apic sep mtrr pge mca cmov pat pse36 clflush mmx fxsr sse sse2 ss ht syscall nx pdpe1gb rdtscp lm constant_tsc rep_good nopl xtopology nonstop_tsc cpuid pni pclmulqdq ssse3 fma cx16 pcid sse4_1 sse4_2 x2apic movbe popcnt aes xsave avx f16c rdrand hypervisor lahf_lm abm 3dnowprefetch invpcid_single ssbd ibrs ibpb stibp ibrs_enhanced fsgsbase tsc_adjust bmi1 hle avx2 smep bmi2 erms invpcid rtm mpx avx512f avx512dq rdseed adx smap clflushopt clwb avx512cd avx512bw avx512vl xsaveopt xsavec xgetbv1 xsaves arat avx512_vnni arch_capabilities
    

| Cpu Property       | Value                                                      |
|:------------------ |:---------------------------------------------------------- |
| Brand              | Intel(R) Xeon(R) CPU                                       |
| Vendor             | :Intel                                                     |
| Architecture       | :Skylake                                                   |
| Model              | Family: 0x06, Model: 0x55, Stepping: 0x07, Type: 0x00      |
| Cores              | 1 physical cores, 2 logical cores (on executing CPU)       |
|                    | Hyperthreading detected                                    |
| Clock Frequencies  | Not supported by CPU                                       |
| Data Cache         | Level 1:3 : (32, 1024, 33792) kbytes                       |
|                    | 64 byte cache line size                                    |
| Address Size       | 48 bits virtual, 46 bits physical                          |
| SIMD               | 512 bit = 64 byte max. SIMD vector size                    |
| Time Stamp Counter | TSC is accessible via `rdtsc`                              |
|                    | TSC runs at constant rate (invariant from clock frequency) |
| Perf. Monitoring   | Performance Monitoring Counters (PMC) are not supported    |
| Hypervisor         | Yes, KVM                                                   |

