# Multi-thread benchmark result

* Pull request commit: [`20940fdee62d9819a8aae18af85689c85a825942`](https://github.com/JuliaFolds/Transducers.jl/commit/20940fdee62d9819a8aae18af85689c85a825942)
* Pull request: <https://github.com/JuliaFolds/Transducers.jl/pull/406> (Simplify benchmark group keys)

# Judge result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmarks:
    - Target: 9 Aug 2020 - 06:16
    - Baseline: 9 Aug 2020 - 06:21
* Package commits:
    - Target: c49304
    - Baseline: 747697
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
| `["collect", "unordered", "basesize=1024"]`         |                   1.01 (5%)  | 0.99 (1%) :white_check_mark: |
| `["parallel_histogram", "assoc", "basesize=4096"]`  |                   1.00 (5%)  | 0.87 (1%) :white_check_mark: |
| `["parallel_histogram", "comm", "basesize=4096"]`   | 0.90 (5%) :white_check_mark: |                   1.01 (1%)  |
| `["parallel_histogram", "comm", "basesize=8192"]`   |                1.06 (5%) :x: |                   1.00 (1%)  |

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
  CPU: Intel(R) Xeon(R) CPU E5-2673 v4 @ 2.30GHz: 
              speed         user         nice          sys         idle          irq
       #1  2294 MHz      51777 s          0 s       2461 s      19855 s          0 s
       #2  2294 MHz      53320 s          0 s       2918 s      18944 s          0 s
       
  Memory: 6.764873504638672 GB (2917.25 MB free)
  Uptime: 764.0 sec
  Load Avg:  1.751953125  1.47607421875  0.880859375
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-8.0.1 (ORCJIT, broadwell)
```

### Baseline
```
Julia Version 1.4.2
Commit 44fa15b150* (2020-05-23 18:35 UTC)
Platform Info:
  OS: Linux (x86_64-pc-linux-gnu)
      Ubuntu 18.04.4 LTS
  uname: Linux 5.3.0-1034-azure #35~18.04.1-Ubuntu SMP Mon Jul 13 12:54:45 UTC 2020 x86_64 x86_64
  CPU: Intel(R) Xeon(R) CPU E5-2673 v4 @ 2.30GHz: 
              speed         user         nice          sys         idle          irq
       #1  2294 MHz      71050 s          0 s       3049 s      30194 s          0 s
       #2  2294 MHz      80242 s          0 s       3433 s      21709 s          0 s
       
  Memory: 6.764873504638672 GB (2918.6640625 MB free)
  Uptime: 1068.0 sec
  Load Avg:  1.57373046875  1.5537109375  1.08935546875
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-8.0.1 (ORCJIT, broadwell)
```

---
# Target result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmark: 9 Aug 2020 - 6:16
* Package commit: c49304
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
| `["collect", "assoc", "basesize=1"]`                | 360.700 ms (5%) | 12.052 ms |  87.55 MiB (1%) |     1590738 |
| `["collect", "assoc", "basesize=1024"]`             | 197.051 ms (5%) |           |   1.84 MiB (1%) |        1812 |
| `["collect", "assoc", "basesize=32"]`               | 202.379 ms (5%) |           |   5.64 MiB (1%) |       54003 |
| `["collect", "seq"]`                                | 394.689 ms (5%) |           |   1.50 MiB (1%) |       32784 |
| `["collect", "unordered", "basesize=1"]`            | 526.623 ms (5%) |           |  29.19 MiB (1%) |      405413 |
| `["collect", "unordered", "basesize=1024"]`         | 281.467 ms (5%) |           | 843.66 KiB (1%) |        7086 |
| `["collect", "unordered", "basesize=32"]`           | 233.534 ms (5%) |           |   1.50 MiB (1%) |       18559 |
| `["findfirst", "n=1000", "foldl"]`                  | 637.973 ms (5%) |           |                 |             |
| `["findfirst", "n=1000", "reduce", "basesize=128"]` | 324.380 ms (5%) |           | 564.28 KiB (1%) |       10241 |
| `["findfirst", "n=1000", "reduce", "basesize=256"]` | 333.194 ms (5%) |           | 287.38 KiB (1%) |        5230 |
| `["findfirst", "n=1000", "reduce", "basesize=512"]` | 329.166 ms (5%) |           | 149.41 KiB (1%) |        2727 |
| `["findfirst", "n=400", "foldl"]`                   | 476.807 ms (5%) |           |                 |             |
| `["findfirst", "n=400", "reduce", "basesize=128"]`  | 242.870 ms (5%) |           |   1.02 MiB (1%) |       18988 |
| `["findfirst", "n=400", "reduce", "basesize=256"]`  | 243.194 ms (5%) |           | 526.41 KiB (1%) |        9586 |
| `["findfirst", "n=400", "reduce", "basesize=512"]`  | 243.913 ms (5%) |           | 267.33 KiB (1%) |        4882 |
| `["findfirst", "n=500", "foldl"]`                   |  82.058 ms (5%) |           |                 |             |
| `["findfirst", "n=500", "reduce", "basesize=128"]`  |  41.594 ms (5%) |           | 157.47 KiB (1%) |        2855 |
| `["findfirst", "n=500", "reduce", "basesize=256"]`  |  41.761 ms (5%) |           |  84.61 KiB (1%) |        1537 |
| `["findfirst", "n=500", "reduce", "basesize=512"]`  |  43.235 ms (5%) |           |  48.33 KiB (1%) |         880 |
| `["overhead", "default"]`                           | 207.701 μs (5%) |           | 146.28 KiB (1%) |        2634 |
| `["overhead", "stoppable=false"]`                   | 216.202 μs (5%) |           | 146.27 KiB (1%) |        2632 |
| `["overhead", "stoppable=true"]`                    | 385.102 μs (5%) |           | 146.53 KiB (1%) |        2649 |
| `["parallel_histogram", "assoc", "basesize=16384"]` |   4.650 ms (5%) |           | 732.06 KiB (1%) |         103 |
| `["parallel_histogram", "assoc", "basesize=4096"]`  |   5.529 ms (5%) |           |   1.80 MiB (1%) |         497 |
| `["parallel_histogram", "assoc", "basesize=8192"]`  |   5.132 ms (5%) |           |   1.43 MiB (1%) |         242 |
| `["parallel_histogram", "comm", "basesize=16384"]`  |  13.682 ms (5%) |           |   1.22 MiB (1%) |         159 |
| `["parallel_histogram", "comm", "basesize=4096"]`   |  19.649 ms (5%) |           |   1.03 MiB (1%) |        3957 |
| `["parallel_histogram", "comm", "basesize=8192"]`   |  16.611 ms (5%) |           |   1.23 MiB (1%) |         767 |
| `["parallel_histogram", "seq"]`                     |   8.513 ms (5%) |           | 364.61 KiB (1%) |          24 |
| `["sum", "random", "foldl"]`                        |  15.648 ms (5%) |           |   64 bytes (1%) |           3 |
| `["sum", "random", "reduce", "basesize=128"]`       |   8.406 ms (5%) |           | 313.41 KiB (1%) |        6070 |
| `["sum", "random", "reduce", "basesize=256"]`       |   8.143 ms (5%) |           | 155.11 KiB (1%) |        3010 |
| `["sum", "random", "reduce", "basesize=512"]`       |   7.941 ms (5%) |           |  76.31 KiB (1%) |        1486 |
| `["sum", "uniform", "foldl"]`                       |  15.167 ms (5%) |           |   64 bytes (1%) |           3 |
| `["sum", "uniform", "reduce", "basesize=128"]`      |   8.271 ms (5%) |           | 313.36 KiB (1%) |        6067 |
| `["sum", "uniform", "reduce", "basesize=256"]`      |   8.002 ms (5%) |           | 155.13 KiB (1%) |        3011 |
| `["sum", "uniform", "reduce", "basesize=512"]`      |   7.760 ms (5%) |           |  76.31 KiB (1%) |        1486 |
| `["sum", "valley", "foldl"]`                        |  15.751 ms (5%) |           |   64 bytes (1%) |           3 |
| `["sum", "valley", "reduce", "basesize=128"]`       |   8.450 ms (5%) |           | 313.34 KiB (1%) |        6066 |
| `["sum", "valley", "reduce", "basesize=256"]`       |   8.219 ms (5%) |           | 155.14 KiB (1%) |        3012 |
| `["sum", "valley", "reduce", "basesize=512"]`       |   8.076 ms (5%) |           |  76.31 KiB (1%) |        1486 |
| `["words", "nthreads=1"]`                           |  43.120 ms (5%) |  8.925 ms |  63.01 MiB (1%) |     2058718 |
| `["words", "nthreads=2"]`                           |  20.976 ms (5%) |           |  63.62 MiB (1%) |     2066888 |
| `["words", "nthreads=4"]`                           |  22.014 ms (5%) |           |  64.89 MiB (1%) |     2079277 |

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
  CPU: Intel(R) Xeon(R) CPU E5-2673 v4 @ 2.30GHz: 
              speed         user         nice          sys         idle          irq
       #1  2294 MHz      51777 s          0 s       2461 s      19855 s          0 s
       #2  2294 MHz      53320 s          0 s       2918 s      18944 s          0 s
       
  Memory: 6.764873504638672 GB (2917.25 MB free)
  Uptime: 764.0 sec
  Load Avg:  1.751953125  1.47607421875  0.880859375
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-8.0.1 (ORCJIT, broadwell)
```

---
# Baseline result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmark: 9 Aug 2020 - 6:21
* Package commit: 747697
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
| `["collect", "assoc", "basesize=1"]`                | 357.980 ms (5%) | 14.282 ms |  87.55 MiB (1%) |     1590684 |
| `["collect", "assoc", "basesize=1024"]`             | 194.671 ms (5%) |           |   1.84 MiB (1%) |        1812 |
| `["collect", "assoc", "basesize=32"]`               | 201.648 ms (5%) |           |   5.64 MiB (1%) |       54013 |
| `["collect", "seq"]`                                | 387.799 ms (5%) |           |   1.50 MiB (1%) |       32784 |
| `["collect", "unordered", "basesize=1"]`            | 519.881 ms (5%) |           |  29.20 MiB (1%) |      406217 |
| `["collect", "unordered", "basesize=1024"]`         | 279.668 ms (5%) |           | 852.89 KiB (1%) |        7341 |
| `["collect", "unordered", "basesize=32"]`           | 240.195 ms (5%) |           |   1.49 MiB (1%) |       18009 |
| `["findfirst", "n=1000", "foldl"]`                  | 644.223 ms (5%) |           |                 |             |
| `["findfirst", "n=1000", "reduce", "basesize=128"]` | 317.295 ms (5%) |           | 564.28 KiB (1%) |       10241 |
| `["findfirst", "n=1000", "reduce", "basesize=256"]` | 322.394 ms (5%) |           | 287.39 KiB (1%) |        5231 |
| `["findfirst", "n=1000", "reduce", "basesize=512"]` | 329.917 ms (5%) |           | 149.42 KiB (1%) |        2728 |
| `["findfirst", "n=400", "foldl"]`                   | 484.057 ms (5%) |           |                 |             |
| `["findfirst", "n=400", "reduce", "basesize=128"]`  | 245.268 ms (5%) |           |   1.02 MiB (1%) |       18982 |
| `["findfirst", "n=400", "reduce", "basesize=256"]`  | 239.777 ms (5%) |           | 526.27 KiB (1%) |        9577 |
| `["findfirst", "n=400", "reduce", "basesize=512"]`  | 243.432 ms (5%) |           | 267.33 KiB (1%) |        4882 |
| `["findfirst", "n=500", "foldl"]`                   |  80.990 ms (5%) |           |                 |             |
| `["findfirst", "n=500", "reduce", "basesize=128"]`  |  41.148 ms (5%) |           | 157.45 KiB (1%) |        2854 |
| `["findfirst", "n=500", "reduce", "basesize=256"]`  |  40.612 ms (5%) |           |  84.59 KiB (1%) |        1536 |
| `["findfirst", "n=500", "reduce", "basesize=512"]`  |  42.967 ms (5%) |           |  48.30 KiB (1%) |         878 |
| `["overhead", "default"]`                           | 215.502 μs (5%) |           | 146.27 KiB (1%) |        2633 |
| `["overhead", "stoppable=false"]`                   | 209.201 μs (5%) |           | 146.28 KiB (1%) |        2633 |
| `["overhead", "stoppable=true"]`                    | 391.903 μs (5%) |           | 146.50 KiB (1%) |        2647 |
| `["parallel_histogram", "assoc", "basesize=16384"]` |   4.700 ms (5%) |           | 732.06 KiB (1%) |         103 |
| `["parallel_histogram", "assoc", "basesize=4096"]`  |   5.544 ms (5%) |           |   2.07 MiB (1%) |         503 |
| `["parallel_histogram", "assoc", "basesize=8192"]`  |   5.122 ms (5%) |           |   1.43 MiB (1%) |         242 |
| `["parallel_histogram", "comm", "basesize=16384"]`  |  14.018 ms (5%) |           |   1.22 MiB (1%) |         207 |
| `["parallel_histogram", "comm", "basesize=4096"]`   |  21.864 ms (5%) |           |   1.02 MiB (1%) |        3417 |
| `["parallel_histogram", "comm", "basesize=8192"]`   |  15.623 ms (5%) |           |   1.23 MiB (1%) |         789 |
| `["parallel_histogram", "seq"]`                     |   8.329 ms (5%) |           | 364.61 KiB (1%) |          24 |
| `["sum", "random", "foldl"]`                        |  15.651 ms (5%) |           |   64 bytes (1%) |           3 |
| `["sum", "random", "reduce", "basesize=128"]`       |   8.422 ms (5%) |           | 313.33 KiB (1%) |        6065 |
| `["sum", "random", "reduce", "basesize=256"]`       |   8.192 ms (5%) |           | 155.14 KiB (1%) |        3012 |
| `["sum", "random", "reduce", "basesize=512"]`       |   8.186 ms (5%) |           |  76.33 KiB (1%) |        1487 |
| `["sum", "uniform", "foldl"]`                       |  15.221 ms (5%) |           |   64 bytes (1%) |           3 |
| `["sum", "uniform", "reduce", "basesize=128"]`      |   8.227 ms (5%) |           | 313.41 KiB (1%) |        6070 |
| `["sum", "uniform", "reduce", "basesize=256"]`      |   7.945 ms (5%) |           | 155.14 KiB (1%) |        3012 |
| `["sum", "uniform", "reduce", "basesize=512"]`      |   7.737 ms (5%) |           |  76.31 KiB (1%) |        1486 |
| `["sum", "valley", "foldl"]`                        |  15.754 ms (5%) |           |   64 bytes (1%) |           3 |
| `["sum", "valley", "reduce", "basesize=128"]`       |   8.395 ms (5%) |           | 313.33 KiB (1%) |        6065 |
| `["sum", "valley", "reduce", "basesize=256"]`       |   8.217 ms (5%) |           | 155.14 KiB (1%) |        3012 |
| `["sum", "valley", "reduce", "basesize=512"]`       |   8.002 ms (5%) |           |  76.30 KiB (1%) |        1485 |
| `["words", "nthreads=1"]`                           |  44.723 ms (5%) |  9.157 ms |  63.33 MiB (1%) |     2069090 |
| `["words", "nthreads=2"]`                           |  21.171 ms (5%) |           |  63.94 MiB (1%) |     2077192 |
| `["words", "nthreads=4"]`                           |  22.650 ms (5%) |           |  65.21 MiB (1%) |     2089589 |

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
  CPU: Intel(R) Xeon(R) CPU E5-2673 v4 @ 2.30GHz: 
              speed         user         nice          sys         idle          irq
       #1  2294 MHz      71050 s          0 s       3049 s      30194 s          0 s
       #2  2294 MHz      80242 s          0 s       3433 s      21709 s          0 s
       
  Memory: 6.764873504638672 GB (2918.6640625 MB free)
  Uptime: 1068.0 sec
  Load Avg:  1.57373046875  1.5537109375  1.08935546875
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-8.0.1 (ORCJIT, broadwell)
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
    Model:               79
    Model name:          Intel(R) Xeon(R) CPU E5-2673 v4 @ 2.30GHz
    Stepping:            1
    CPU MHz:             2294.684
    BogoMIPS:            4589.36
    Hypervisor vendor:   Microsoft
    Virtualization type: full
    L1d cache:           32K
    L1i cache:           32K
    L2 cache:            256K
    L3 cache:            51200K
    NUMA node0 CPU(s):   0,1
    Flags:               fpu vme de pse tsc msr pae mce cx8 apic sep mtrr pge mca cmov pat pse36 clflush mmx fxsr sse sse2 ss ht syscall nx pdpe1gb rdtscp lm constant_tsc rep_good nopl xtopology cpuid pni pclmulqdq ssse3 fma cx16 pcid sse4_1 sse4_2 movbe popcnt aes xsave avx f16c rdrand hypervisor lahf_lm abm 3dnowprefetch invpcid_single pti fsgsbase bmi1 hle avx2 smep bmi2 erms invpcid rtm rdseed adx smap xsaveopt md_clear
    

| Cpu Property       | Value                                                   |
|:------------------ |:------------------------------------------------------- |
| Brand              | Intel(R) Xeon(R) CPU E5-2673 v4 @ 2.30GHz               |
| Vendor             | :Intel                                                  |
| Architecture       | :Broadwell                                              |
| Model              | Family: 0x06, Model: 0x4f, Stepping: 0x01, Type: 0x00   |
| Cores              | 2 physical cores, 2 logical cores (on executing CPU)    |
|                    | No Hyperthreading detected                              |
| Clock Frequencies  | Not supported by CPU                                    |
| Data Cache         | Level 1:3 : (32, 256, 51200) kbytes                     |
|                    | 64 byte cache line size                                 |
| Address Size       | 48 bits virtual, 44 bits physical                       |
| SIMD               | 256 bit = 32 byte max. SIMD vector size                 |
| Time Stamp Counter | TSC is accessible via `rdtsc`                           |
|                    | TSC increased at every clock cycle (non-invariant TSC)  |
| Perf. Monitoring   | Performance Monitoring Counters (PMC) are not supported |
| Hypervisor         | Yes, Microsoft                                          |

