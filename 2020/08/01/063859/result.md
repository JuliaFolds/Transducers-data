# Multi-thread benchmark result (via Travis)


# Judge result
# Benchmark Report for */home/travis/build/JuliaFolds/Transducers.jl*

## Job Properties
* Time of benchmarks:
    - Target: 1 Aug 2020 - 06:33
    - Baseline: 1 Aug 2020 - 06:38
* Package commits:
    - Target: f03c59
    - Baseline: d1995c
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
| `["collect", "unordered", "basesize=1024"]`         | 0.82 (5%) :white_check_mark: | 0.84 (1%) :white_check_mark: |
| `["overhead", "stoppable=true"]`                    |                1.64 (5%) :x: |                   1.00 (1%)  |
| `["parallel_histogram", "comm", "basesize=4096"]`   | 0.91 (5%) :white_check_mark: | 0.95 (1%) :white_check_mark: |

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
       #1  2800 MHz      51320 s          0 s       2272 s      12982 s          0 s
       #2  2800 MHz      48252 s          0 s       1930 s      18059 s          0 s
       
  Memory: 7.790031433105469 GB (5585.0390625 MB free)
  Uptime: 687.0 sec
  Load Avg:  1.75927734375  1.50634765625  0.87109375
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
       #1  2800 MHz      73149 s          0 s       2696 s      19704 s          0 s
       #2  2800 MHz      71479 s          0 s       2539 s      23247 s          0 s
       
  Memory: 7.790031433105469 GB (5611.91015625 MB free)
  Uptime: 978.0 sec
  Load Avg:  1.73583984375  1.58642578125  1.07861328125
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-8.0.1 (ORCJIT, skylake)
```

---
# Target result
# Benchmark Report for */home/travis/build/JuliaFolds/Transducers.jl*

## Job Properties
* Time of benchmark: 1 Aug 2020 - 6:33
* Package commit: f03c59
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
| `["collect", "assoc", "basesize=1"]`                | 323.578 ms (5%) | 12.299 ms |  87.55 MiB (1%) |     1590666 |
| `["collect", "assoc", "basesize=1024"]`             | 179.481 ms (5%) |           |   1.84 MiB (1%) |        1807 |
| `["collect", "assoc", "basesize=32"]`               | 184.412 ms (5%) |           |   5.64 MiB (1%) |       54013 |
| `["collect", "seq"]`                                | 350.183 ms (5%) |           |   1.50 MiB (1%) |       32784 |
| `["collect", "unordered", "basesize=1"]`            | 369.808 ms (5%) |           |  29.15 MiB (1%) |      402885 |
| `["collect", "unordered", "basesize=1024"]`         | 233.498 ms (5%) |           | 921.20 KiB (1%) |       12004 |
| `["collect", "unordered", "basesize=32"]`           | 206.936 ms (5%) |           |   1.53 MiB (1%) |       20859 |
| `["findfirst", "n=1000", "foldl"]`                  | 555.745 ms (5%) |           |                 |             |
| `["findfirst", "n=1000", "reduce", "basesize=128"]` | 315.088 ms (5%) |           | 564.03 KiB (1%) |       10225 |
| `["findfirst", "n=1000", "reduce", "basesize=256"]` | 307.447 ms (5%) |           | 287.19 KiB (1%) |        5218 |
| `["findfirst", "n=1000", "reduce", "basesize=512"]` | 309.093 ms (5%) |           | 149.27 KiB (1%) |        2718 |
| `["findfirst", "n=400", "foldl"]`                   | 417.206 ms (5%) |           |                 |             |
| `["findfirst", "n=400", "reduce", "basesize=128"]`  | 253.331 ms (5%) |           |   1.02 MiB (1%) |       18946 |
| `["findfirst", "n=400", "reduce", "basesize=256"]`  | 238.969 ms (5%) |           | 525.98 KiB (1%) |        9559 |
| `["findfirst", "n=400", "reduce", "basesize=512"]`  | 233.282 ms (5%) |           | 267.20 KiB (1%) |        4874 |
| `["findfirst", "n=500", "foldl"]`                   |  72.271 ms (5%) |           |                 |             |
| `["findfirst", "n=500", "reduce", "basesize=128"]`  |  43.363 ms (5%) |           | 157.38 KiB (1%) |        2849 |
| `["findfirst", "n=500", "reduce", "basesize=256"]`  |  41.343 ms (5%) |           |  84.58 KiB (1%) |        1535 |
| `["findfirst", "n=500", "reduce", "basesize=512"]`  |  43.049 ms (5%) |           |  48.30 KiB (1%) |         878 |
| `["overhead", "default"]`                           | 221.436 μs (5%) |           | 146.28 KiB (1%) |        2634 |
| `["overhead", "stoppable=false"]`                   | 222.270 μs (5%) |           | 146.30 KiB (1%) |        2634 |
| `["overhead", "stoppable=true"]`                    | 411.328 μs (5%) |           | 146.56 KiB (1%) |        2651 |
| `["parallel_histogram", "assoc", "basesize=16384"]` |   4.798 ms (5%) |           | 732.06 KiB (1%) |         103 |
| `["parallel_histogram", "assoc", "basesize=4096"]`  |   5.712 ms (5%) |           |   1.80 MiB (1%) |         498 |
| `["parallel_histogram", "assoc", "basesize=8192"]`  |   5.209 ms (5%) |           |   1.43 MiB (1%) |         243 |
| `["parallel_histogram", "comm", "basesize=16384"]`  |  12.027 ms (5%) |           |   1.23 MiB (1%) |         646 |
| `["parallel_histogram", "comm", "basesize=4096"]`   |  16.622 ms (5%) |           |   1.04 MiB (1%) |        4614 |
| `["parallel_histogram", "comm", "basesize=8192"]`   |  14.872 ms (5%) |           |   1.26 MiB (1%) |        2802 |
| `["parallel_histogram", "seq"]`                     |   7.442 ms (5%) |           | 364.61 KiB (1%) |          24 |
| `["sum", "random", "foldl"]`                        |  14.023 ms (5%) |           |   64 bytes (1%) |           3 |
| `["sum", "random", "reduce", "basesize=128"]`       |   7.981 ms (5%) |           | 313.41 KiB (1%) |        6070 |
| `["sum", "random", "reduce", "basesize=256"]`       |   7.764 ms (5%) |           | 155.19 KiB (1%) |        3015 |
| `["sum", "random", "reduce", "basesize=512"]`       |   7.628 ms (5%) |           |  76.36 KiB (1%) |        1489 |
| `["sum", "uniform", "foldl"]`                       |  13.686 ms (5%) |           |   64 bytes (1%) |           3 |
| `["sum", "uniform", "reduce", "basesize=128"]`      |   7.808 ms (5%) |           | 313.36 KiB (1%) |        6067 |
| `["sum", "uniform", "reduce", "basesize=256"]`      |   7.564 ms (5%) |           | 155.14 KiB (1%) |        3012 |
| `["sum", "uniform", "reduce", "basesize=512"]`      |   7.455 ms (5%) |           |  76.31 KiB (1%) |        1486 |
| `["sum", "valley", "foldl"]`                        |  14.175 ms (5%) |           |   64 bytes (1%) |           3 |
| `["sum", "valley", "reduce", "basesize=128"]`       |   8.058 ms (5%) |           | 313.36 KiB (1%) |        6067 |
| `["sum", "valley", "reduce", "basesize=256"]`       |   7.841 ms (5%) |           | 155.16 KiB (1%) |        3013 |
| `["sum", "valley", "reduce", "basesize=512"]`       |   7.706 ms (5%) |           |  76.34 KiB (1%) |        1488 |
| `["words", "nthreads=1"]`                           |  42.385 ms (5%) |  7.370 ms |  62.90 MiB (1%) |     2055333 |
| `["words", "nthreads=2"]`                           |  38.711 ms (5%) |           |  63.99 MiB (1%) |     2067588 |
| `["words", "nthreads=4"]`                           |  39.513 ms (5%) |           |  64.62 MiB (1%) |     2073763 |

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
       #1  2800 MHz      51320 s          0 s       2272 s      12982 s          0 s
       #2  2800 MHz      48252 s          0 s       1930 s      18059 s          0 s
       
  Memory: 7.790031433105469 GB (5585.0390625 MB free)
  Uptime: 687.0 sec
  Load Avg:  1.75927734375  1.50634765625  0.87109375
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-8.0.1 (ORCJIT, skylake)
```

---
# Baseline result
# Benchmark Report for */home/travis/build/JuliaFolds/Transducers.jl*

## Job Properties
* Time of benchmark: 1 Aug 2020 - 6:38
* Package commit: d1995c
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
| `["collect", "assoc", "basesize=1"]`                | 323.631 ms (5%) | 11.646 ms |  87.55 MiB (1%) |     1590703 |
| `["collect", "assoc", "basesize=1024"]`             | 179.817 ms (5%) |           |   1.84 MiB (1%) |        1807 |
| `["collect", "assoc", "basesize=32"]`               | 184.419 ms (5%) |           |   5.64 MiB (1%) |       54014 |
| `["collect", "seq"]`                                | 350.122 ms (5%) |           |   1.50 MiB (1%) |       32784 |
| `["collect", "unordered", "basesize=1"]`            | 370.276 ms (5%) |           |  29.16 MiB (1%) |      403138 |
| `["collect", "unordered", "basesize=1024"]`         | 286.136 ms (5%) |           |   1.07 MiB (1%) |       22950 |
| `["collect", "unordered", "basesize=32"]`           | 206.655 ms (5%) |           |   1.52 MiB (1%) |       19943 |
| `["findfirst", "n=1000", "foldl"]`                  | 554.176 ms (5%) |           |                 |             |
| `["findfirst", "n=1000", "reduce", "basesize=128"]` | 312.791 ms (5%) |           | 563.88 KiB (1%) |       10219 |
| `["findfirst", "n=1000", "reduce", "basesize=256"]` | 305.063 ms (5%) |           | 287.13 KiB (1%) |        5218 |
| `["findfirst", "n=1000", "reduce", "basesize=512"]` | 306.570 ms (5%) |           | 149.19 KiB (1%) |        2717 |
| `["findfirst", "n=400", "foldl"]`                   | 416.042 ms (5%) |           |                 |             |
| `["findfirst", "n=400", "reduce", "basesize=128"]`  | 251.668 ms (5%) |           |   1.02 MiB (1%) |       18951 |
| `["findfirst", "n=400", "reduce", "basesize=256"]`  | 237.209 ms (5%) |           | 525.88 KiB (1%) |        9556 |
| `["findfirst", "n=400", "reduce", "basesize=512"]`  | 232.397 ms (5%) |           | 267.06 KiB (1%) |        4869 |
| `["findfirst", "n=500", "foldl"]`                   |  72.073 ms (5%) |           |                 |             |
| `["findfirst", "n=500", "reduce", "basesize=128"]`  |  43.043 ms (5%) |           | 157.27 KiB (1%) |        2846 |
| `["findfirst", "n=500", "reduce", "basesize=256"]`  |  41.064 ms (5%) |           |  84.48 KiB (1%) |        1533 |
| `["findfirst", "n=500", "reduce", "basesize=512"]`  |  42.749 ms (5%) |           |  48.19 KiB (1%) |         875 |
| `["overhead", "default"]`                           | 222.089 μs (5%) |           | 146.16 KiB (1%) |        2629 |
| `["overhead", "stoppable=false"]`                   | 220.850 μs (5%) |           | 146.16 KiB (1%) |        2629 |
| `["overhead", "stoppable=true"]`                    | 250.996 μs (5%) |           | 146.45 KiB (1%) |        2648 |
| `["parallel_histogram", "assoc", "basesize=16384"]` |   4.852 ms (5%) |           | 732.02 KiB (1%) |         101 |
| `["parallel_histogram", "assoc", "basesize=4096"]`  |   5.694 ms (5%) |           |   1.80 MiB (1%) |         495 |
| `["parallel_histogram", "assoc", "basesize=8192"]`  |   5.291 ms (5%) |           |   1.43 MiB (1%) |         241 |
| `["parallel_histogram", "comm", "basesize=16384"]`  |  12.567 ms (5%) |           |   1.24 MiB (1%) |        1295 |
| `["parallel_histogram", "comm", "basesize=4096"]`   |  18.227 ms (5%) |           |   1.10 MiB (1%) |        8126 |
| `["parallel_histogram", "comm", "basesize=8192"]`   |  14.440 ms (5%) |           |   1.27 MiB (1%) |        3387 |
| `["parallel_histogram", "seq"]`                     |   7.384 ms (5%) |           | 364.61 KiB (1%) |          24 |
| `["sum", "random", "foldl"]`                        |  14.105 ms (5%) |           |   64 bytes (1%) |           3 |
| `["sum", "random", "reduce", "basesize=128"]`       |   8.037 ms (5%) |           | 313.34 KiB (1%) |        6068 |
| `["sum", "random", "reduce", "basesize=256"]`       |   7.806 ms (5%) |           | 155.09 KiB (1%) |        3011 |
| `["sum", "random", "reduce", "basesize=512"]`       |   7.668 ms (5%) |           |  76.31 KiB (1%) |        1488 |
| `["sum", "uniform", "foldl"]`                       |  13.690 ms (5%) |           |   64 bytes (1%) |           3 |
| `["sum", "uniform", "reduce", "basesize=128"]`      |   7.814 ms (5%) |           | 313.34 KiB (1%) |        6068 |
| `["sum", "uniform", "reduce", "basesize=256"]`      |   7.573 ms (5%) |           | 155.08 KiB (1%) |        3010 |
| `["sum", "uniform", "reduce", "basesize=512"]`      |   7.455 ms (5%) |           |  76.25 KiB (1%) |        1484 |
| `["sum", "valley", "foldl"]`                        |  14.183 ms (5%) |           |   64 bytes (1%) |           3 |
| `["sum", "valley", "reduce", "basesize=128"]`       |   8.068 ms (5%) |           | 313.31 KiB (1%) |        6066 |
| `["sum", "valley", "reduce", "basesize=256"]`       |   7.854 ms (5%) |           | 155.09 KiB (1%) |        3011 |
| `["sum", "valley", "reduce", "basesize=512"]`       |   7.705 ms (5%) |           |  76.28 KiB (1%) |        1486 |
| `["words", "nthreads=1"]`                           |  44.068 ms (5%) |  7.060 ms |  63.21 MiB (1%) |     2065561 |
| `["words", "nthreads=2"]`                           |  38.966 ms (5%) |           |  64.30 MiB (1%) |     2077778 |
| `["words", "nthreads=4"]`                           |  40.026 ms (5%) |           |  65.25 MiB (1%) |     2088268 |

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
       #1  2800 MHz      73149 s          0 s       2696 s      19704 s          0 s
       #2  2800 MHz      71479 s          0 s       2539 s      23247 s          0 s
       
  Memory: 7.790031433105469 GB (5611.91015625 MB free)
  Uptime: 978.0 sec
  Load Avg:  1.73583984375  1.58642578125  1.07861328125
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
    CPU MHz:               2800.186
    BogoMIPS:              5600.37
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

