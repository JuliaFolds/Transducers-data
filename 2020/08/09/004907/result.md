# Multi-thread benchmark result (via Travis)


# Judge result
# Benchmark Report for */home/travis/build/JuliaFolds/Transducers.jl*

## Job Properties
* Time of benchmarks:
    - Target: 9 Aug 2020 - 00:43
    - Baseline: 9 Aug 2020 - 00:48
* Package commits:
    - Target: cc32d3
    - Baseline: f87cd6
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

| ID                                                  | time ratio    | memory ratio                 |
|-----------------------------------------------------|---------------|------------------------------|
| `["collect", "unordered", "basesize=1024"]`         | 1.18 (5%) :x: |                1.19 (1%) :x: |
| `["parallel_histogram", "assoc", "basesize=4096"]`  |    0.98 (5%)  | 0.77 (1%) :white_check_mark: |
| `["parallel_histogram", "comm", "basesize=16384"]`  |    1.02 (5%)  |                1.01 (1%) :x: |
| `["parallel_histogram", "comm", "basesize=4096"]`   |    1.03 (5%)  |                1.01 (1%) :x: |

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
       #1  2800 MHz      51718 s          0 s       2181 s      13831 s          0 s
       #2  2800 MHz      49001 s          0 s       1880 s      17900 s          0 s
       
  Memory: 7.790031433105469 GB (5781.03515625 MB free)
  Uptime: 695.0 sec
  Load Avg:  1.654296875  1.4677734375  0.85400390625
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
       #1  2800 MHz      70797 s          0 s       2590 s      23525 s          0 s
       #2  2800 MHz      75022 s          0 s       2533 s      20372 s          0 s
       
  Memory: 7.790031433105469 GB (5820.140625 MB free)
  Uptime: 988.0 sec
  Load Avg:  1.71337890625  1.56005859375  1.06005859375
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-8.0.1 (ORCJIT, skylake)
```

---
# Target result
# Benchmark Report for */home/travis/build/JuliaFolds/Transducers.jl*

## Job Properties
* Time of benchmark: 9 Aug 2020 - 0:43
* Package commit: cc32d3
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
| `["collect", "assoc", "basesize=1"]`                | 325.820 ms (5%) | 12.027 ms |   87.55 MiB (1%) |     1590681 |
| `["collect", "assoc", "basesize=1024"]`             | 179.745 ms (5%) |           |    1.84 MiB (1%) |        1808 |
| `["collect", "assoc", "basesize=32"]`               | 184.535 ms (5%) |           |    5.64 MiB (1%) |       54009 |
| `["collect", "seq"]`                                | 350.229 ms (5%) |           |    1.50 MiB (1%) |       32784 |
| `["collect", "unordered", "basesize=1"]`            | 372.215 ms (5%) |           |   29.16 MiB (1%) |      403163 |
| `["collect", "unordered", "basesize=1024"]`         | 259.936 ms (5%) |           | 1006.64 KiB (1%) |       17517 |
| `["collect", "unordered", "basesize=32"]`           | 207.459 ms (5%) |           |    1.51 MiB (1%) |       19069 |
| `["findfirst", "n=1000", "foldl"]`                  | 550.786 ms (5%) |           |                  |             |
| `["findfirst", "n=1000", "reduce", "basesize=128"]` | 310.751 ms (5%) |           |  563.78 KiB (1%) |       10209 |
| `["findfirst", "n=1000", "reduce", "basesize=256"]` | 303.302 ms (5%) |           |  287.20 KiB (1%) |        5219 |
| `["findfirst", "n=1000", "reduce", "basesize=512"]` | 304.807 ms (5%) |           |  149.33 KiB (1%) |        2722 |
| `["findfirst", "n=400", "foldl"]`                   | 413.290 ms (5%) |           |                  |             |
| `["findfirst", "n=400", "reduce", "basesize=128"]`  | 250.376 ms (5%) |           |    1.02 MiB (1%) |       18951 |
| `["findfirst", "n=400", "reduce", "basesize=256"]`  | 235.808 ms (5%) |           |  526.08 KiB (1%) |        9565 |
| `["findfirst", "n=400", "reduce", "basesize=512"]`  | 230.986 ms (5%) |           |  267.22 KiB (1%) |        4875 |
| `["findfirst", "n=500", "foldl"]`                   |  71.626 ms (5%) |           |                  |             |
| `["findfirst", "n=500", "reduce", "basesize=128"]`  |  42.797 ms (5%) |           |  157.39 KiB (1%) |        2850 |
| `["findfirst", "n=500", "reduce", "basesize=256"]`  |  40.825 ms (5%) |           |   84.59 KiB (1%) |        1536 |
| `["findfirst", "n=500", "reduce", "basesize=512"]`  |  42.481 ms (5%) |           |   48.30 KiB (1%) |         878 |
| `["overhead", "default"]`                           | 222.490 μs (5%) |           |  146.27 KiB (1%) |        2633 |
| `["overhead", "stoppable=false"]`                   | 226.223 μs (5%) |           |  146.27 KiB (1%) |        2632 |
| `["overhead", "stoppable=true"]`                    | 431.105 μs (5%) |           |  146.59 KiB (1%) |        2653 |
| `["parallel_histogram", "assoc", "basesize=16384"]` |   4.913 ms (5%) |           |  732.06 KiB (1%) |         103 |
| `["parallel_histogram", "assoc", "basesize=4096"]`  |   5.771 ms (5%) |           |    1.80 MiB (1%) |         497 |
| `["parallel_histogram", "assoc", "basesize=8192"]`  |   5.342 ms (5%) |           |    1.43 MiB (1%) |         243 |
| `["parallel_histogram", "comm", "basesize=16384"]`  |  13.158 ms (5%) |           |    1.24 MiB (1%) |        1791 |
| `["parallel_histogram", "comm", "basesize=4096"]`   |  18.845 ms (5%) |           |    1.12 MiB (1%) |        9542 |
| `["parallel_histogram", "comm", "basesize=8192"]`   |  14.991 ms (5%) |           |    1.27 MiB (1%) |        3121 |
| `["parallel_histogram", "seq"]`                     |   7.399 ms (5%) |           |  364.61 KiB (1%) |          24 |
| `["sum", "random", "foldl"]`                        |  13.995 ms (5%) |           |    64 bytes (1%) |           3 |
| `["sum", "random", "reduce", "basesize=128"]`       |   7.966 ms (5%) |           |  313.42 KiB (1%) |        6071 |
| `["sum", "random", "reduce", "basesize=256"]`       |   7.733 ms (5%) |           |  155.14 KiB (1%) |        3012 |
| `["sum", "random", "reduce", "basesize=512"]`       |   7.607 ms (5%) |           |   76.31 KiB (1%) |        1486 |
| `["sum", "uniform", "foldl"]`                       |  13.686 ms (5%) |           |    64 bytes (1%) |           3 |
| `["sum", "uniform", "reduce", "basesize=128"]`      |   7.814 ms (5%) |           |  313.44 KiB (1%) |        6072 |
| `["sum", "uniform", "reduce", "basesize=256"]`      |   7.559 ms (5%) |           |  155.14 KiB (1%) |        3012 |
| `["sum", "uniform", "reduce", "basesize=512"]`      |   7.448 ms (5%) |           |   76.31 KiB (1%) |        1486 |
| `["sum", "valley", "foldl"]`                        |  14.158 ms (5%) |           |    64 bytes (1%) |           3 |
| `["sum", "valley", "reduce", "basesize=128"]`       |   8.049 ms (5%) |           |  313.28 KiB (1%) |        6062 |
| `["sum", "valley", "reduce", "basesize=256"]`       |   7.836 ms (5%) |           |  155.13 KiB (1%) |        3011 |
| `["sum", "valley", "reduce", "basesize=512"]`       |   7.706 ms (5%) |           |   76.34 KiB (1%) |        1488 |
| `["words", "nthreads=1"]`                           |  33.701 ms (5%) |  7.208 ms |   63.20 MiB (1%) |     2064897 |
| `["words", "nthreads=2"]`                           |  29.754 ms (5%) |           |   64.28 MiB (1%) |     2077142 |
| `["words", "nthreads=4"]`                           |  30.304 ms (5%) |           |   64.92 MiB (1%) |     2083338 |

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
       #1  2800 MHz      51718 s          0 s       2181 s      13831 s          0 s
       #2  2800 MHz      49001 s          0 s       1880 s      17900 s          0 s
       
  Memory: 7.790031433105469 GB (5781.03515625 MB free)
  Uptime: 695.0 sec
  Load Avg:  1.654296875  1.4677734375  0.85400390625
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-8.0.1 (ORCJIT, skylake)
```

---
# Baseline result
# Benchmark Report for */home/travis/build/JuliaFolds/Transducers.jl*

## Job Properties
* Time of benchmark: 9 Aug 2020 - 0:48
* Package commit: f87cd6
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
| `["collect", "assoc", "basesize=1"]`                | 324.181 ms (5%) | 12.205 ms |  87.55 MiB (1%) |     1590722 |
| `["collect", "assoc", "basesize=1024"]`             | 179.978 ms (5%) |           |   1.84 MiB (1%) |        1809 |
| `["collect", "assoc", "basesize=32"]`               | 184.453 ms (5%) |           |   5.64 MiB (1%) |       54004 |
| `["collect", "seq"]`                                | 350.168 ms (5%) |           |   1.50 MiB (1%) |       32784 |
| `["collect", "unordered", "basesize=1"]`            | 376.816 ms (5%) |           |  29.16 MiB (1%) |      403511 |
| `["collect", "unordered", "basesize=1024"]`         | 220.341 ms (5%) |           | 845.16 KiB (1%) |        6846 |
| `["collect", "unordered", "basesize=32"]`           | 206.234 ms (5%) |           |   1.50 MiB (1%) |       18827 |
| `["findfirst", "n=1000", "foldl"]`                  | 552.052 ms (5%) |           |                 |             |
| `["findfirst", "n=1000", "reduce", "basesize=128"]` | 310.840 ms (5%) |           | 563.84 KiB (1%) |       10213 |
| `["findfirst", "n=1000", "reduce", "basesize=256"]` | 302.954 ms (5%) |           | 287.08 KiB (1%) |        5211 |
| `["findfirst", "n=1000", "reduce", "basesize=512"]` | 304.554 ms (5%) |           | 149.30 KiB (1%) |        2720 |
| `["findfirst", "n=400", "foldl"]`                   | 415.108 ms (5%) |           |                 |             |
| `["findfirst", "n=400", "reduce", "basesize=128"]`  | 250.243 ms (5%) |           |   1.02 MiB (1%) |       18942 |
| `["findfirst", "n=400", "reduce", "basesize=256"]`  | 235.679 ms (5%) |           | 526.11 KiB (1%) |        9567 |
| `["findfirst", "n=400", "reduce", "basesize=512"]`  | 230.771 ms (5%) |           | 267.09 KiB (1%) |        4867 |
| `["findfirst", "n=500", "foldl"]`                   |  71.787 ms (5%) |           |                 |             |
| `["findfirst", "n=500", "reduce", "basesize=128"]`  |  42.760 ms (5%) |           | 157.44 KiB (1%) |        2853 |
| `["findfirst", "n=500", "reduce", "basesize=256"]`  |  40.778 ms (5%) |           |  84.58 KiB (1%) |        1535 |
| `["findfirst", "n=500", "reduce", "basesize=512"]`  |  42.440 ms (5%) |           |  48.31 KiB (1%) |         879 |
| `["overhead", "default"]`                           | 223.315 μs (5%) |           | 146.28 KiB (1%) |        2634 |
| `["overhead", "stoppable=false"]`                   | 221.364 μs (5%) |           | 146.28 KiB (1%) |        2633 |
| `["overhead", "stoppable=true"]`                    | 426.607 μs (5%) |           | 146.59 KiB (1%) |        2653 |
| `["parallel_histogram", "assoc", "basesize=16384"]` |   4.814 ms (5%) |           | 732.06 KiB (1%) |         103 |
| `["parallel_histogram", "assoc", "basesize=4096"]`  |   5.881 ms (5%) |           |   2.33 MiB (1%) |         509 |
| `["parallel_histogram", "assoc", "basesize=8192"]`  |   5.259 ms (5%) |           |   1.43 MiB (1%) |         242 |
| `["parallel_histogram", "comm", "basesize=16384"]`  |  12.893 ms (5%) |           |   1.23 MiB (1%) |         589 |
| `["parallel_histogram", "comm", "basesize=4096"]`   |  18.317 ms (5%) |           |   1.10 MiB (1%) |        6726 |
| `["parallel_histogram", "comm", "basesize=8192"]`   |  15.250 ms (5%) |           |   1.27 MiB (1%) |        3169 |
| `["parallel_histogram", "seq"]`                     |   7.374 ms (5%) |           | 364.61 KiB (1%) |          24 |
| `["sum", "random", "foldl"]`                        |  14.172 ms (5%) |           |   64 bytes (1%) |           3 |
| `["sum", "random", "reduce", "basesize=128"]`       |   8.057 ms (5%) |           | 313.42 KiB (1%) |        6071 |
| `["sum", "random", "reduce", "basesize=256"]`       |   7.824 ms (5%) |           | 155.14 KiB (1%) |        3012 |
| `["sum", "random", "reduce", "basesize=512"]`       |   7.702 ms (5%) |           |  76.31 KiB (1%) |        1486 |
| `["sum", "uniform", "foldl"]`                       |  13.670 ms (5%) |           |   64 bytes (1%) |           3 |
| `["sum", "uniform", "reduce", "basesize=128"]`      |   7.797 ms (5%) |           | 313.38 KiB (1%) |        6068 |
| `["sum", "uniform", "reduce", "basesize=256"]`      |   7.560 ms (5%) |           | 155.11 KiB (1%) |        3010 |
| `["sum", "uniform", "reduce", "basesize=512"]`      |   7.447 ms (5%) |           |  76.31 KiB (1%) |        1486 |
| `["sum", "valley", "foldl"]`                        |  14.168 ms (5%) |           |   64 bytes (1%) |           3 |
| `["sum", "valley", "reduce", "basesize=128"]`       |   8.037 ms (5%) |           | 313.36 KiB (1%) |        6067 |
| `["sum", "valley", "reduce", "basesize=256"]`       |   7.834 ms (5%) |           | 155.16 KiB (1%) |        3013 |
| `["sum", "valley", "reduce", "basesize=512"]`       |   7.696 ms (5%) |           |  76.34 KiB (1%) |        1488 |
| `["words", "nthreads=1"]`                           |  34.360 ms (5%) |  6.899 ms |  63.47 MiB (1%) |     2073657 |
| `["words", "nthreads=2"]`                           |  29.590 ms (5%) |           |  64.55 MiB (1%) |     2085832 |
| `["words", "nthreads=4"]`                           |  30.473 ms (5%) |           |  65.19 MiB (1%) |     2092036 |

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
       #1  2800 MHz      70797 s          0 s       2590 s      23525 s          0 s
       #2  2800 MHz      75022 s          0 s       2533 s      20372 s          0 s
       
  Memory: 7.790031433105469 GB (5820.140625 MB free)
  Uptime: 988.0 sec
  Load Avg:  1.71337890625  1.56005859375  1.06005859375
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
    CPU MHz:               2800.246
    BogoMIPS:              5600.49
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

