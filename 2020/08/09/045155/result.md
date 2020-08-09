# Multi-thread benchmark result (via Travis)


# Judge result
# Benchmark Report for */home/travis/build/JuliaFolds/Transducers.jl*

## Job Properties
* Time of benchmarks:
    - Target: 9 Aug 2020 - 04:46
    - Baseline: 9 Aug 2020 - 04:51
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
| `["collect", "unordered", "basesize=1024"]`         | 0.88 (5%) :white_check_mark: | 0.93 (1%) :white_check_mark: |
| `["collect", "unordered", "basesize=32"]`           |                   1.01 (5%)  | 0.99 (1%) :white_check_mark: |
| `["parallel_histogram", "comm", "basesize=16384"]`  | 0.95 (5%) :white_check_mark: |                   1.00 (1%)  |

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
       #1  2800 MHz      54037 s          0 s       2025 s      12161 s          0 s
       #2  2800 MHz      46655 s          0 s       1916 s      20089 s          0 s
       
  Memory: 7.7900238037109375 GB (5841.0078125 MB free)
  Uptime: 697.0 sec
  Load Avg:  1.78466796875  1.53466796875  0.89404296875
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
       #1  2800 MHz      74359 s          0 s       2619 s      20050 s          0 s
       #2  2800 MHz      71284 s          0 s       2310 s      24018 s          0 s
       
  Memory: 7.7900238037109375 GB (5910.3828125 MB free)
  Uptime: 987.0 sec
  Load Avg:  1.673828125  1.60888671875  1.103515625
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-8.0.1 (ORCJIT, skylake)
```

---
# Target result
# Benchmark Report for */home/travis/build/JuliaFolds/Transducers.jl*

## Job Properties
* Time of benchmark: 9 Aug 2020 - 4:46
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
| `["collect", "assoc", "basesize=1"]`                | 327.902 ms (5%) | 13.481 ms |  87.55 MiB (1%) |     1590688 |
| `["collect", "assoc", "basesize=1024"]`             | 179.586 ms (5%) |           |   1.84 MiB (1%) |        1807 |
| `["collect", "assoc", "basesize=32"]`               | 184.376 ms (5%) |           |   5.64 MiB (1%) |       54006 |
| `["collect", "seq"]`                                | 350.227 ms (5%) |           |   1.50 MiB (1%) |       32784 |
| `["collect", "unordered", "basesize=1"]`            | 371.845 ms (5%) |           |  29.16 MiB (1%) |      402971 |
| `["collect", "unordered", "basesize=1024"]`         | 238.152 ms (5%) |           | 938.97 KiB (1%) |       13141 |
| `["collect", "unordered", "basesize=32"]`           | 208.129 ms (5%) |           |   1.50 MiB (1%) |       18864 |
| `["findfirst", "n=1000", "foldl"]`                  | 551.918 ms (5%) |           |                 |             |
| `["findfirst", "n=1000", "reduce", "basesize=128"]` | 310.451 ms (5%) |           | 563.92 KiB (1%) |       10218 |
| `["findfirst", "n=1000", "reduce", "basesize=256"]` | 302.521 ms (5%) |           | 287.33 KiB (1%) |        5227 |
| `["findfirst", "n=1000", "reduce", "basesize=512"]` | 304.038 ms (5%) |           | 149.38 KiB (1%) |        2725 |
| `["findfirst", "n=400", "foldl"]`                   | 413.272 ms (5%) |           |                 |             |
| `["findfirst", "n=400", "reduce", "basesize=128"]`  | 249.756 ms (5%) |           |   1.02 MiB (1%) |       18950 |
| `["findfirst", "n=400", "reduce", "basesize=256"]`  | 235.636 ms (5%) |           | 526.03 KiB (1%) |        9562 |
| `["findfirst", "n=400", "reduce", "basesize=512"]`  | 230.610 ms (5%) |           | 267.25 KiB (1%) |        4877 |
| `["findfirst", "n=500", "foldl"]`                   |  71.605 ms (5%) |           |                 |             |
| `["findfirst", "n=500", "reduce", "basesize=128"]`  |  42.750 ms (5%) |           | 157.36 KiB (1%) |        2848 |
| `["findfirst", "n=500", "reduce", "basesize=256"]`  |  40.746 ms (5%) |           |  84.59 KiB (1%) |        1536 |
| `["findfirst", "n=500", "reduce", "basesize=512"]`  |  42.423 ms (5%) |           |  48.31 KiB (1%) |         879 |
| `["overhead", "default"]`                           | 222.999 μs (5%) |           | 146.27 KiB (1%) |        2633 |
| `["overhead", "stoppable=false"]`                   | 221.677 μs (5%) |           | 146.28 KiB (1%) |        2633 |
| `["overhead", "stoppable=true"]`                    | 418.582 μs (5%) |           | 146.58 KiB (1%) |        2652 |
| `["parallel_histogram", "assoc", "basesize=16384"]` |   4.921 ms (5%) |           | 732.06 KiB (1%) |         103 |
| `["parallel_histogram", "assoc", "basesize=4096"]`  |   5.772 ms (5%) |           |   1.80 MiB (1%) |         497 |
| `["parallel_histogram", "assoc", "basesize=8192"]`  |   5.359 ms (5%) |           |   1.43 MiB (1%) |         243 |
| `["parallel_histogram", "comm", "basesize=16384"]`  |  12.483 ms (5%) |           |   1.23 MiB (1%) |         765 |
| `["parallel_histogram", "comm", "basesize=4096"]`   |  18.912 ms (5%) |           |   1.13 MiB (1%) |        3532 |
| `["parallel_histogram", "comm", "basesize=8192"]`   |  15.591 ms (5%) |           |   1.27 MiB (1%) |        3635 |
| `["parallel_histogram", "seq"]`                     |   7.432 ms (5%) |           | 364.61 KiB (1%) |          24 |
| `["sum", "random", "foldl"]`                        |  14.095 ms (5%) |           |   64 bytes (1%) |           3 |
| `["sum", "random", "reduce", "basesize=128"]`       |   8.043 ms (5%) |           | 313.38 KiB (1%) |        6068 |
| `["sum", "random", "reduce", "basesize=256"]`       |   7.788 ms (5%) |           | 155.20 KiB (1%) |        3016 |
| `["sum", "random", "reduce", "basesize=512"]`       |   7.671 ms (5%) |           |  76.31 KiB (1%) |        1486 |
| `["sum", "uniform", "foldl"]`                       |  13.682 ms (5%) |           |   64 bytes (1%) |           3 |
| `["sum", "uniform", "reduce", "basesize=128"]`      |   7.794 ms (5%) |           | 313.44 KiB (1%) |        6072 |
| `["sum", "uniform", "reduce", "basesize=256"]`      |   7.564 ms (5%) |           | 155.14 KiB (1%) |        3012 |
| `["sum", "uniform", "reduce", "basesize=512"]`      |   7.451 ms (5%) |           |  76.31 KiB (1%) |        1486 |
| `["sum", "valley", "foldl"]`                        |  14.166 ms (5%) |           |   64 bytes (1%) |           3 |
| `["sum", "valley", "reduce", "basesize=128"]`       |   8.044 ms (5%) |           | 313.31 KiB (1%) |        6064 |
| `["sum", "valley", "reduce", "basesize=256"]`       |   7.843 ms (5%) |           | 155.17 KiB (1%) |        3014 |
| `["sum", "valley", "reduce", "basesize=512"]`       |   7.687 ms (5%) |           |  76.31 KiB (1%) |        1486 |
| `["words", "nthreads=1"]`                           |  35.618 ms (5%) |  7.483 ms |  63.44 MiB (1%) |     2072899 |
| `["words", "nthreads=2"]`                           |  30.322 ms (5%) |           |  64.52 MiB (1%) |     2085126 |
| `["words", "nthreads=4"]`                           |  31.003 ms (5%) |           |  65.16 MiB (1%) |     2091399 |

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
       #1  2800 MHz      54037 s          0 s       2025 s      12161 s          0 s
       #2  2800 MHz      46655 s          0 s       1916 s      20089 s          0 s
       
  Memory: 7.7900238037109375 GB (5841.0078125 MB free)
  Uptime: 697.0 sec
  Load Avg:  1.78466796875  1.53466796875  0.89404296875
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-8.0.1 (ORCJIT, skylake)
```

---
# Baseline result
# Benchmark Report for */home/travis/build/JuliaFolds/Transducers.jl*

## Job Properties
* Time of benchmark: 9 Aug 2020 - 4:51
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

| ID                                                  | time            | GC time   | memory           | allocations |
|-----------------------------------------------------|----------------:|----------:|-----------------:|------------:|
| `["collect", "assoc", "basesize=1"]`                | 323.216 ms (5%) | 12.170 ms |   87.55 MiB (1%) |     1590638 |
| `["collect", "assoc", "basesize=1024"]`             | 179.774 ms (5%) |           |    1.84 MiB (1%) |        1809 |
| `["collect", "assoc", "basesize=32"]`               | 184.350 ms (5%) |           |    5.64 MiB (1%) |       54008 |
| `["collect", "seq"]`                                | 349.789 ms (5%) |           |    1.50 MiB (1%) |       32784 |
| `["collect", "unordered", "basesize=1"]`            | 372.205 ms (5%) |           |   29.16 MiB (1%) |      403083 |
| `["collect", "unordered", "basesize=1024"]`         | 269.815 ms (5%) |           | 1010.00 KiB (1%) |       17396 |
| `["collect", "unordered", "basesize=32"]`           | 206.669 ms (5%) |           |    1.52 MiB (1%) |       20062 |
| `["findfirst", "n=1000", "foldl"]`                  | 555.367 ms (5%) |           |                  |             |
| `["findfirst", "n=1000", "reduce", "basesize=128"]` | 313.599 ms (5%) |           |  563.94 KiB (1%) |       10219 |
| `["findfirst", "n=1000", "reduce", "basesize=256"]` | 304.823 ms (5%) |           |  287.22 KiB (1%) |        5220 |
| `["findfirst", "n=1000", "reduce", "basesize=512"]` | 306.902 ms (5%) |           |  149.42 KiB (1%) |        2728 |
| `["findfirst", "n=400", "foldl"]`                   | 416.953 ms (5%) |           |                  |             |
| `["findfirst", "n=400", "reduce", "basesize=128"]`  | 251.065 ms (5%) |           |    1.02 MiB (1%) |       18950 |
| `["findfirst", "n=400", "reduce", "basesize=256"]`  | 237.069 ms (5%) |           |  526.00 KiB (1%) |        9560 |
| `["findfirst", "n=400", "reduce", "basesize=512"]`  | 232.034 ms (5%) |           |  267.23 KiB (1%) |        4876 |
| `["findfirst", "n=500", "foldl"]`                   |  72.361 ms (5%) |           |                  |             |
| `["findfirst", "n=500", "reduce", "basesize=128"]`  |  42.983 ms (5%) |           |  157.42 KiB (1%) |        2852 |
| `["findfirst", "n=500", "reduce", "basesize=256"]`  |  40.938 ms (5%) |           |   84.58 KiB (1%) |        1535 |
| `["findfirst", "n=500", "reduce", "basesize=512"]`  |  42.695 ms (5%) |           |   48.30 KiB (1%) |         878 |
| `["overhead", "default"]`                           | 222.314 μs (5%) |           |  146.28 KiB (1%) |        2634 |
| `["overhead", "stoppable=false"]`                   | 222.149 μs (5%) |           |  146.28 KiB (1%) |        2633 |
| `["overhead", "stoppable=true"]`                    | 421.250 μs (5%) |           |  146.58 KiB (1%) |        2652 |
| `["parallel_histogram", "assoc", "basesize=16384"]` |   4.873 ms (5%) |           |  732.06 KiB (1%) |         103 |
| `["parallel_histogram", "assoc", "basesize=4096"]`  |   5.727 ms (5%) |           |    1.80 MiB (1%) |         497 |
| `["parallel_histogram", "assoc", "basesize=8192"]`  |   5.309 ms (5%) |           |    1.43 MiB (1%) |         242 |
| `["parallel_histogram", "comm", "basesize=16384"]`  |  13.207 ms (5%) |           |    1.23 MiB (1%) |         751 |
| `["parallel_histogram", "comm", "basesize=4096"]`   |  18.992 ms (5%) |           |    1.12 MiB (1%) |        9363 |
| `["parallel_histogram", "comm", "basesize=8192"]`   |  15.034 ms (5%) |           |    1.27 MiB (1%) |        3108 |
| `["parallel_histogram", "seq"]`                     |   7.414 ms (5%) |           |  364.61 KiB (1%) |          24 |
| `["sum", "random", "foldl"]`                        |  14.084 ms (5%) |           |    64 bytes (1%) |           3 |
| `["sum", "random", "reduce", "basesize=128"]`       |   8.020 ms (5%) |           |  313.44 KiB (1%) |        6072 |
| `["sum", "random", "reduce", "basesize=256"]`       |   7.785 ms (5%) |           |  155.14 KiB (1%) |        3012 |
| `["sum", "random", "reduce", "basesize=512"]`       |   7.668 ms (5%) |           |   76.31 KiB (1%) |        1486 |
| `["sum", "uniform", "foldl"]`                       |  13.687 ms (5%) |           |    64 bytes (1%) |           3 |
| `["sum", "uniform", "reduce", "basesize=128"]`      |   7.794 ms (5%) |           |  313.41 KiB (1%) |        6070 |
| `["sum", "uniform", "reduce", "basesize=256"]`      |   7.575 ms (5%) |           |  155.14 KiB (1%) |        3012 |
| `["sum", "uniform", "reduce", "basesize=512"]`      |   7.446 ms (5%) |           |   76.31 KiB (1%) |        1486 |
| `["sum", "valley", "foldl"]`                        |  14.180 ms (5%) |           |    64 bytes (1%) |           3 |
| `["sum", "valley", "reduce", "basesize=128"]`       |   8.067 ms (5%) |           |  313.28 KiB (1%) |        6062 |
| `["sum", "valley", "reduce", "basesize=256"]`       |   7.850 ms (5%) |           |  155.13 KiB (1%) |        3011 |
| `["sum", "valley", "reduce", "basesize=512"]`       |   7.708 ms (5%) |           |   76.31 KiB (1%) |        1486 |
| `["words", "nthreads=1"]`                           |  35.390 ms (5%) |  7.382 ms |   63.07 MiB (1%) |     2060875 |
| `["words", "nthreads=2"]`                           |  31.455 ms (5%) |           |   64.15 MiB (1%) |     2073138 |
| `["words", "nthreads=4"]`                           |  32.334 ms (5%) |           |   64.79 MiB (1%) |     2079327 |

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
       #1  2800 MHz      74359 s          0 s       2619 s      20050 s          0 s
       #2  2800 MHz      71284 s          0 s       2310 s      24018 s          0 s
       
  Memory: 7.7900238037109375 GB (5910.3828125 MB free)
  Uptime: 987.0 sec
  Load Avg:  1.673828125  1.60888671875  1.103515625
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
    CPU MHz:               2800.266
    BogoMIPS:              5600.53
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

