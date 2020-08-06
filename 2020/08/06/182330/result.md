# Multi-thread benchmark result (via Travis)


# Judge result
# Benchmark Report for */home/travis/build/JuliaFolds/Transducers.jl*

## Job Properties
* Time of benchmarks:
    - Target: 6 Aug 2020 - 18:18
    - Baseline: 6 Aug 2020 - 18:23
* Package commits:
    - Target: 650576
    - Baseline: 3599fd
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
| `["collect", "unordered", "basesize=1024"]`         |                   1.01 (5%)  | 0.97 (1%) :white_check_mark: |
| `["overhead", "stoppable=true"]`                    | 0.67 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["parallel_histogram", "comm", "basesize=4096"]`   |                   0.99 (5%)  | 0.96 (1%) :white_check_mark: |
| `["parallel_histogram", "comm", "basesize=8192"]`   |                1.10 (5%) :x: |                1.01 (1%) :x: |
| `["words", "nthreads=1"]`                           | 0.95 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["words", "nthreads=2"]`                           | 0.94 (5%) :white_check_mark: |                   1.00 (1%)  |

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
       #1  2800 MHz      50880 s          0 s       2091 s      14745 s          0 s
       #2  2800 MHz      48978 s          0 s       1976 s      16863 s          0 s
       
  Memory: 7.7900238037109375 GB (5828.92578125 MB free)
  Uptime: 689.0 sec
  Load Avg:  1.62255859375  1.50732421875  0.88232421875
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
       #1  2800 MHz      72081 s          0 s       2498 s      22435 s          0 s
       #2  2800 MHz      73028 s          0 s       2586 s      21322 s          0 s
       
  Memory: 7.7900238037109375 GB (5851.9296875 MB free)
  Uptime: 982.0 sec
  Load Avg:  1.6806640625  1.55029296875  1.0712890625
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-8.0.1 (ORCJIT, skylake)
```

---
# Target result
# Benchmark Report for */home/travis/build/JuliaFolds/Transducers.jl*

## Job Properties
* Time of benchmark: 6 Aug 2020 - 18:18
* Package commit: 650576
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
| `["collect", "assoc", "basesize=1"]`                | 328.044 ms (5%) | 12.463 ms |  87.55 MiB (1%) |     1590718 |
| `["collect", "assoc", "basesize=1024"]`             | 180.180 ms (5%) |           |   1.84 MiB (1%) |        1807 |
| `["collect", "assoc", "basesize=32"]`               | 185.283 ms (5%) |           |   5.64 MiB (1%) |       54013 |
| `["collect", "seq"]`                                | 350.432 ms (5%) |           |   1.50 MiB (1%) |       32784 |
| `["collect", "unordered", "basesize=1"]`            | 370.706 ms (5%) |           |  29.16 MiB (1%) |      403168 |
| `["collect", "unordered", "basesize=1024"]`         | 263.047 ms (5%) |           | 983.11 KiB (1%) |       16011 |
| `["collect", "unordered", "basesize=32"]`           | 206.781 ms (5%) |           |   1.52 MiB (1%) |       20138 |
| `["findfirst", "n=1000", "foldl"]`                  | 555.699 ms (5%) |           |                 |             |
| `["findfirst", "n=1000", "reduce", "basesize=128"]` | 314.062 ms (5%) |           | 564.05 KiB (1%) |       10226 |
| `["findfirst", "n=1000", "reduce", "basesize=256"]` | 306.157 ms (5%) |           | 287.19 KiB (1%) |        5218 |
| `["findfirst", "n=1000", "reduce", "basesize=512"]` | 307.721 ms (5%) |           | 149.33 KiB (1%) |        2722 |
| `["findfirst", "n=400", "foldl"]`                   | 417.342 ms (5%) |           |                 |             |
| `["findfirst", "n=400", "reduce", "basesize=128"]`  | 252.371 ms (5%) |           |   1.02 MiB (1%) |       18947 |
| `["findfirst", "n=400", "reduce", "basesize=256"]`  | 238.092 ms (5%) |           | 525.97 KiB (1%) |        9558 |
| `["findfirst", "n=400", "reduce", "basesize=512"]`  | 233.331 ms (5%) |           | 267.23 KiB (1%) |        4876 |
| `["findfirst", "n=500", "foldl"]`                   |  72.290 ms (5%) |           |                 |             |
| `["findfirst", "n=500", "reduce", "basesize=128"]`  |  43.251 ms (5%) |           | 157.41 KiB (1%) |        2851 |
| `["findfirst", "n=500", "reduce", "basesize=256"]`  |  41.222 ms (5%) |           |  84.56 KiB (1%) |        1534 |
| `["findfirst", "n=500", "reduce", "basesize=512"]`  |  42.912 ms (5%) |           |  48.31 KiB (1%) |         879 |
| `["overhead", "default"]`                           | 220.427 μs (5%) |           | 146.27 KiB (1%) |        2633 |
| `["overhead", "stoppable=false"]`                   | 222.569 μs (5%) |           | 146.30 KiB (1%) |        2634 |
| `["overhead", "stoppable=true"]`                    | 286.032 μs (5%) |           | 146.58 KiB (1%) |        2652 |
| `["parallel_histogram", "assoc", "basesize=16384"]` |   4.778 ms (5%) |           | 732.06 KiB (1%) |         103 |
| `["parallel_histogram", "assoc", "basesize=4096"]`  |   5.630 ms (5%) |           |   1.80 MiB (1%) |         497 |
| `["parallel_histogram", "assoc", "basesize=8192"]`  |   5.195 ms (5%) |           |   1.43 MiB (1%) |         243 |
| `["parallel_histogram", "comm", "basesize=16384"]`  |  13.485 ms (5%) |           |   1.23 MiB (1%) |         942 |
| `["parallel_histogram", "comm", "basesize=4096"]`   |  18.028 ms (5%) |           |   1.06 MiB (1%) |        5965 |
| `["parallel_histogram", "comm", "basesize=8192"]`   |  16.319 ms (5%) |           |   1.28 MiB (1%) |        4308 |
| `["parallel_histogram", "seq"]`                     |   7.398 ms (5%) |           | 364.61 KiB (1%) |          24 |
| `["sum", "random", "foldl"]`                        |  14.186 ms (5%) |           |   64 bytes (1%) |           3 |
| `["sum", "random", "reduce", "basesize=128"]`       |   8.046 ms (5%) |           | 313.45 KiB (1%) |        6073 |
| `["sum", "random", "reduce", "basesize=256"]`       |   7.808 ms (5%) |           | 155.16 KiB (1%) |        3013 |
| `["sum", "random", "reduce", "basesize=512"]`       |   7.710 ms (5%) |           |  76.34 KiB (1%) |        1488 |
| `["sum", "uniform", "foldl"]`                       |  13.716 ms (5%) |           |   64 bytes (1%) |           3 |
| `["sum", "uniform", "reduce", "basesize=128"]`      |   7.810 ms (5%) |           | 313.41 KiB (1%) |        6070 |
| `["sum", "uniform", "reduce", "basesize=256"]`      |   7.576 ms (5%) |           | 155.14 KiB (1%) |        3012 |
| `["sum", "uniform", "reduce", "basesize=512"]`      |   7.460 ms (5%) |           |  76.31 KiB (1%) |        1486 |
| `["sum", "valley", "foldl"]`                        |  14.196 ms (5%) |           |   64 bytes (1%) |           3 |
| `["sum", "valley", "reduce", "basesize=128"]`       |   8.061 ms (5%) |           | 313.39 KiB (1%) |        6069 |
| `["sum", "valley", "reduce", "basesize=256"]`       |   7.837 ms (5%) |           | 155.13 KiB (1%) |        3011 |
| `["sum", "valley", "reduce", "basesize=512"]`       |   7.700 ms (5%) |           |  76.34 KiB (1%) |        1488 |
| `["words", "nthreads=1"]`                           |  33.827 ms (5%) |  7.192 ms |  63.44 MiB (1%) |     2072741 |
| `["words", "nthreads=2"]`                           |  29.874 ms (5%) |           |  64.53 MiB (1%) |     2085051 |
| `["words", "nthreads=4"]`                           |  31.063 ms (5%) |           |  65.47 MiB (1%) |     2095450 |

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
       #1  2800 MHz      50880 s          0 s       2091 s      14745 s          0 s
       #2  2800 MHz      48978 s          0 s       1976 s      16863 s          0 s
       
  Memory: 7.7900238037109375 GB (5828.92578125 MB free)
  Uptime: 689.0 sec
  Load Avg:  1.62255859375  1.50732421875  0.88232421875
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-8.0.1 (ORCJIT, skylake)
```

---
# Baseline result
# Benchmark Report for */home/travis/build/JuliaFolds/Transducers.jl*

## Job Properties
* Time of benchmark: 6 Aug 2020 - 18:23
* Package commit: 3599fd
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

| ID                                                  | time            | GC time   | memory           | allocations |
|-----------------------------------------------------|----------------:|----------:|-----------------:|------------:|
| `["collect", "assoc", "basesize=1"]`                | 325.427 ms (5%) | 13.499 ms |   87.55 MiB (1%) |     1590706 |
| `["collect", "assoc", "basesize=1024"]`             | 179.863 ms (5%) |           |    1.84 MiB (1%) |        1811 |
| `["collect", "assoc", "basesize=32"]`               | 184.672 ms (5%) |           |    5.64 MiB (1%) |       54018 |
| `["collect", "seq"]`                                | 349.868 ms (5%) |           |    1.50 MiB (1%) |       32784 |
| `["collect", "unordered", "basesize=1"]`            | 367.570 ms (5%) |           |   29.15 MiB (1%) |      402904 |
| `["collect", "unordered", "basesize=1024"]`         | 260.778 ms (5%) |           | 1018.20 KiB (1%) |       17943 |
| `["collect", "unordered", "basesize=32"]`           | 205.886 ms (5%) |           |    1.51 MiB (1%) |       19319 |
| `["findfirst", "n=1000", "foldl"]`                  | 557.790 ms (5%) |           |                  |             |
| `["findfirst", "n=1000", "reduce", "basesize=128"]` | 313.397 ms (5%) |           |  564.00 KiB (1%) |       10223 |
| `["findfirst", "n=1000", "reduce", "basesize=256"]` | 305.417 ms (5%) |           |  287.25 KiB (1%) |        5222 |
| `["findfirst", "n=1000", "reduce", "basesize=512"]` | 306.977 ms (5%) |           |  149.38 KiB (1%) |        2725 |
| `["findfirst", "n=400", "foldl"]`                   | 418.822 ms (5%) |           |                  |             |
| `["findfirst", "n=400", "reduce", "basesize=128"]`  | 251.387 ms (5%) |           |    1.02 MiB (1%) |       18952 |
| `["findfirst", "n=400", "reduce", "basesize=256"]`  | 237.551 ms (5%) |           |  526.00 KiB (1%) |        9560 |
| `["findfirst", "n=400", "reduce", "basesize=512"]`  | 232.513 ms (5%) |           |  267.22 KiB (1%) |        4875 |
| `["findfirst", "n=500", "foldl"]`                   |  72.549 ms (5%) |           |                  |             |
| `["findfirst", "n=500", "reduce", "basesize=128"]`  |  43.121 ms (5%) |           |  157.41 KiB (1%) |        2851 |
| `["findfirst", "n=500", "reduce", "basesize=256"]`  |  41.084 ms (5%) |           |   84.58 KiB (1%) |        1535 |
| `["findfirst", "n=500", "reduce", "basesize=512"]`  |  42.770 ms (5%) |           |   48.30 KiB (1%) |         878 |
| `["overhead", "default"]`                           | 224.028 μs (5%) |           |  146.27 KiB (1%) |        2633 |
| `["overhead", "stoppable=false"]`                   | 222.175 μs (5%) |           |  146.27 KiB (1%) |        2632 |
| `["overhead", "stoppable=true"]`                    | 429.477 μs (5%) |           |  146.58 KiB (1%) |        2652 |
| `["parallel_histogram", "assoc", "basesize=16384"]` |   4.847 ms (5%) |           |  732.06 KiB (1%) |         103 |
| `["parallel_histogram", "assoc", "basesize=4096"]`  |   5.729 ms (5%) |           |    1.80 MiB (1%) |         497 |
| `["parallel_histogram", "assoc", "basesize=8192"]`  |   5.302 ms (5%) |           |    1.43 MiB (1%) |         243 |
| `["parallel_histogram", "comm", "basesize=16384"]`  |  13.145 ms (5%) |           |    1.23 MiB (1%) |         740 |
| `["parallel_histogram", "comm", "basesize=4096"]`   |  18.205 ms (5%) |           |    1.11 MiB (1%) |        7198 |
| `["parallel_histogram", "comm", "basesize=8192"]`   |  14.848 ms (5%) |           |    1.27 MiB (1%) |        3405 |
| `["parallel_histogram", "seq"]`                     |   7.405 ms (5%) |           |  364.61 KiB (1%) |          24 |
| `["sum", "random", "foldl"]`                        |  14.152 ms (5%) |           |    64 bytes (1%) |           3 |
| `["sum", "random", "reduce", "basesize=128"]`       |   8.047 ms (5%) |           |  313.44 KiB (1%) |        6072 |
| `["sum", "random", "reduce", "basesize=256"]`       |   7.814 ms (5%) |           |  155.14 KiB (1%) |        3012 |
| `["sum", "random", "reduce", "basesize=512"]`       |   7.701 ms (5%) |           |   76.30 KiB (1%) |        1485 |
| `["sum", "uniform", "foldl"]`                       |  13.685 ms (5%) |           |    64 bytes (1%) |           3 |
| `["sum", "uniform", "reduce", "basesize=128"]`      |   7.816 ms (5%) |           |  313.45 KiB (1%) |        6073 |
| `["sum", "uniform", "reduce", "basesize=256"]`      |   7.579 ms (5%) |           |  155.14 KiB (1%) |        3012 |
| `["sum", "uniform", "reduce", "basesize=512"]`      |   7.455 ms (5%) |           |   76.31 KiB (1%) |        1486 |
| `["sum", "valley", "foldl"]`                        |  14.176 ms (5%) |           |    64 bytes (1%) |           3 |
| `["sum", "valley", "reduce", "basesize=128"]`       |   8.061 ms (5%) |           |  313.34 KiB (1%) |        6066 |
| `["sum", "valley", "reduce", "basesize=256"]`       |   7.863 ms (5%) |           |  155.16 KiB (1%) |        3013 |
| `["sum", "valley", "reduce", "basesize=512"]`       |   7.721 ms (5%) |           |   76.33 KiB (1%) |        1487 |
| `["words", "nthreads=1"]`                           |  35.677 ms (5%) |  7.395 ms |   63.67 MiB (1%) |     2080133 |
| `["words", "nthreads=2"]`                           |  31.649 ms (5%) |           |   64.76 MiB (1%) |     2092454 |
| `["words", "nthreads=4"]`                           |  32.402 ms (5%) |           |   65.70 MiB (1%) |     2102910 |

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
       #1  2800 MHz      72081 s          0 s       2498 s      22435 s          0 s
       #2  2800 MHz      73028 s          0 s       2586 s      21322 s          0 s
       
  Memory: 7.7900238037109375 GB (5851.9296875 MB free)
  Uptime: 982.0 sec
  Load Avg:  1.6806640625  1.55029296875  1.0712890625
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
    CPU MHz:               2800.160
    BogoMIPS:              5600.32
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

