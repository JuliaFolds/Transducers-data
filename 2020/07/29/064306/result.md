# Multi-thread benchmark result (via Travis)


# Judge result
# Benchmark Report for */home/travis/build/JuliaFolds/Transducers.jl*

## Job Properties
* Time of benchmarks:
    - Target: 29 Jul 2020 - 06:37
    - Baseline: 29 Jul 2020 - 06:42
* Package commits:
    - Target: 0a4715
    - Baseline: f3056a
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
| `["collect", "unordered", "basesize=1024"]`         | 1.14 (5%) :x: |                1.12 (1%) :x: |
| `["parallel_histogram", "comm", "basesize=16384"]`  |    0.99 (5%)  | 0.99 (1%) :white_check_mark: |
| `["parallel_histogram", "comm", "basesize=4096"]`   |    1.02 (5%)  | 0.98 (1%) :white_check_mark: |
| `["parallel_histogram", "comm", "basesize=8192"]`   |    0.99 (5%)  | 0.99 (1%) :white_check_mark: |
| `["words", "nthreads=4"]`                           |    1.02 (5%)  |                1.01 (1%) :x: |

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
       #1  2800 MHz      47230 s          0 s       2108 s      16925 s          0 s
       #2  2800 MHz      52055 s          0 s       1944 s      13662 s          0 s
       
  Memory: 7.7900238037109375 GB (5824.5078125 MB free)
  Uptime: 682.0 sec
  Load Avg:  1.7236328125  1.55224609375  0.9267578125
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
       #1  2800 MHz      68593 s          0 s       2662 s      24443 s          0 s
       #2  2800 MHz      76168 s          0 s       2326 s      18420 s          0 s
       
  Memory: 7.7900238037109375 GB (5846.84375 MB free)
  Uptime: 977.0 sec
  Load Avg:  1.728515625  1.609375  1.11962890625
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-8.0.1 (ORCJIT, skylake)
```

---
# Target result
# Benchmark Report for */home/travis/build/JuliaFolds/Transducers.jl*

## Job Properties
* Time of benchmark: 29 Jul 2020 - 6:37
* Package commit: 0a4715
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
| `["collect", "assoc", "basesize=1"]`                | 325.709 ms (5%) | 12.669 ms |  87.55 MiB (1%) |     1590678 |
| `["collect", "assoc", "basesize=1024"]`             | 179.653 ms (5%) |           |   1.84 MiB (1%) |        1808 |
| `["collect", "assoc", "basesize=32"]`               | 184.427 ms (5%) |           |   5.64 MiB (1%) |       54004 |
| `["collect", "seq"]`                                | 350.527 ms (5%) |           |   1.50 MiB (1%) |       32784 |
| `["collect", "unordered", "basesize=1"]`            | 368.263 ms (5%) |           |  29.16 MiB (1%) |      403012 |
| `["collect", "unordered", "basesize=1024"]`         | 222.203 ms (5%) |           | 885.55 KiB (1%) |        9767 |
| `["collect", "unordered", "basesize=32"]`           | 206.332 ms (5%) |           |   1.50 MiB (1%) |       18871 |
| `["findfirst", "n=1000", "foldl"]`                  | 555.751 ms (5%) |           |                 |             |
| `["findfirst", "n=1000", "reduce", "basesize=128"]` | 314.211 ms (5%) |           | 563.81 KiB (1%) |       10215 |
| `["findfirst", "n=1000", "reduce", "basesize=256"]` | 306.304 ms (5%) |           | 287.08 KiB (1%) |        5215 |
| `["findfirst", "n=1000", "reduce", "basesize=512"]` | 307.744 ms (5%) |           | 149.19 KiB (1%) |        2717 |
| `["findfirst", "n=400", "foldl"]`                   | 417.402 ms (5%) |           |                 |             |
| `["findfirst", "n=400", "reduce", "basesize=128"]`  | 251.789 ms (5%) |           |   1.02 MiB (1%) |       18947 |
| `["findfirst", "n=400", "reduce", "basesize=256"]`  | 238.109 ms (5%) |           | 525.83 KiB (1%) |        9553 |
| `["findfirst", "n=400", "reduce", "basesize=512"]`  | 233.249 ms (5%) |           | 267.06 KiB (1%) |        4869 |
| `["findfirst", "n=500", "foldl"]`                   |  72.307 ms (5%) |           |                 |             |
| `["findfirst", "n=500", "reduce", "basesize=128"]`  |  43.197 ms (5%) |           | 157.25 KiB (1%) |        2845 |
| `["findfirst", "n=500", "reduce", "basesize=256"]`  |  41.211 ms (5%) |           |  84.45 KiB (1%) |        1531 |
| `["findfirst", "n=500", "reduce", "basesize=512"]`  |  42.878 ms (5%) |           |  48.17 KiB (1%) |         874 |
| `["overhead", "default"]`                           | 222.326 μs (5%) |           | 146.16 KiB (1%) |        2629 |
| `["overhead", "stoppable=false"]`                   | 219.654 μs (5%) |           | 146.16 KiB (1%) |        2629 |
| `["overhead", "stoppable=true"]`                    | 422.524 μs (5%) |           | 146.44 KiB (1%) |        2647 |
| `["parallel_histogram", "assoc", "basesize=16384"]` |   5.063 ms (5%) |           | 732.02 KiB (1%) |         101 |
| `["parallel_histogram", "assoc", "basesize=4096"]`  |   5.901 ms (5%) |           |   1.80 MiB (1%) |         495 |
| `["parallel_histogram", "assoc", "basesize=8192"]`  |   5.497 ms (5%) |           |   1.43 MiB (1%) |         241 |
| `["parallel_histogram", "comm", "basesize=16384"]`  |  13.064 ms (5%) |           |   1.23 MiB (1%) |         945 |
| `["parallel_histogram", "comm", "basesize=4096"]`   |  19.767 ms (5%) |           |   1.09 MiB (1%) |        7959 |
| `["parallel_histogram", "comm", "basesize=8192"]`   |  15.695 ms (5%) |           |   1.28 MiB (1%) |        3818 |
| `["parallel_histogram", "seq"]`                     |   7.429 ms (5%) |           | 364.61 KiB (1%) |          24 |
| `["sum", "random", "foldl"]`                        |  14.162 ms (5%) |           |   64 bytes (1%) |           3 |
| `["sum", "random", "reduce", "basesize=128"]`       |   8.049 ms (5%) |           | 313.34 KiB (1%) |        6068 |
| `["sum", "random", "reduce", "basesize=256"]`       |   7.798 ms (5%) |           | 155.06 KiB (1%) |        3009 |
| `["sum", "random", "reduce", "basesize=512"]`       |   7.694 ms (5%) |           |  76.30 KiB (1%) |        1487 |
| `["sum", "uniform", "foldl"]`                       |  13.712 ms (5%) |           |   64 bytes (1%) |           3 |
| `["sum", "uniform", "reduce", "basesize=128"]`      |   7.807 ms (5%) |           | 313.36 KiB (1%) |        6069 |
| `["sum", "uniform", "reduce", "basesize=256"]`      |   7.579 ms (5%) |           | 155.08 KiB (1%) |        3010 |
| `["sum", "uniform", "reduce", "basesize=512"]`      |   7.456 ms (5%) |           |  76.25 KiB (1%) |        1484 |
| `["sum", "valley", "foldl"]`                        |  14.207 ms (5%) |           |   64 bytes (1%) |           3 |
| `["sum", "valley", "reduce", "basesize=128"]`       |   8.063 ms (5%) |           | 313.27 KiB (1%) |        6063 |
| `["sum", "valley", "reduce", "basesize=256"]`       |   7.855 ms (5%) |           | 155.08 KiB (1%) |        3010 |
| `["sum", "valley", "reduce", "basesize=512"]`       |   7.707 ms (5%) |           |  76.28 KiB (1%) |        1486 |
| `["words", "nthreads=1"]`                           |  44.029 ms (5%) |  7.581 ms |  63.23 MiB (1%) |     2065885 |
| `["words", "nthreads=2"]`                           |  40.825 ms (5%) |           |  64.31 MiB (1%) |     2078062 |
| `["words", "nthreads=4"]`                           |  42.540 ms (5%) |           |  65.26 MiB (1%) |     2088481 |

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
       #1  2800 MHz      47230 s          0 s       2108 s      16925 s          0 s
       #2  2800 MHz      52055 s          0 s       1944 s      13662 s          0 s
       
  Memory: 7.7900238037109375 GB (5824.5078125 MB free)
  Uptime: 682.0 sec
  Load Avg:  1.7236328125  1.55224609375  0.9267578125
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-8.0.1 (ORCJIT, skylake)
```

---
# Baseline result
# Benchmark Report for */home/travis/build/JuliaFolds/Transducers.jl*

## Job Properties
* Time of benchmark: 29 Jul 2020 - 6:42
* Package commit: f3056a
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
| `["collect", "assoc", "basesize=1"]`                | 326.236 ms (5%) | 12.720 ms |  87.55 MiB (1%) |     1590667 |
| `["collect", "assoc", "basesize=1024"]`             | 179.918 ms (5%) |           |   1.84 MiB (1%) |        1811 |
| `["collect", "assoc", "basesize=32"]`               | 184.817 ms (5%) |           |   5.64 MiB (1%) |       54021 |
| `["collect", "seq"]`                                | 350.074 ms (5%) |           |   1.50 MiB (1%) |       32784 |
| `["collect", "unordered", "basesize=1"]`            | 380.062 ms (5%) |           |  29.17 MiB (1%) |      403680 |
| `["collect", "unordered", "basesize=1024"]`         | 195.772 ms (5%) |           | 789.83 KiB (1%) |        3260 |
| `["collect", "unordered", "basesize=32"]`           | 206.260 ms (5%) |           |   1.49 MiB (1%) |       18150 |
| `["findfirst", "n=1000", "foldl"]`                  | 552.028 ms (5%) |           |                 |             |
| `["findfirst", "n=1000", "reduce", "basesize=128"]` | 310.481 ms (5%) |           | 563.86 KiB (1%) |       10218 |
| `["findfirst", "n=1000", "reduce", "basesize=256"]` | 302.569 ms (5%) |           | 287.13 KiB (1%) |        5218 |
| `["findfirst", "n=1000", "reduce", "basesize=512"]` | 304.351 ms (5%) |           | 149.17 KiB (1%) |        2716 |
| `["findfirst", "n=400", "foldl"]`                   | 414.453 ms (5%) |           |                 |             |
| `["findfirst", "n=400", "reduce", "basesize=128"]`  | 250.165 ms (5%) |           |   1.02 MiB (1%) |       18950 |
| `["findfirst", "n=400", "reduce", "basesize=256"]`  | 235.633 ms (5%) |           | 525.95 KiB (1%) |        9561 |
| `["findfirst", "n=400", "reduce", "basesize=512"]`  | 230.239 ms (5%) |           | 267.03 KiB (1%) |        4867 |
| `["findfirst", "n=500", "foldl"]`                   |  71.778 ms (5%) |           |                 |             |
| `["findfirst", "n=500", "reduce", "basesize=128"]`  |  42.695 ms (5%) |           | 157.28 KiB (1%) |        2847 |
| `["findfirst", "n=500", "reduce", "basesize=256"]`  |  40.724 ms (5%) |           |  84.45 KiB (1%) |        1531 |
| `["findfirst", "n=500", "reduce", "basesize=512"]`  |  42.450 ms (5%) |           |  48.17 KiB (1%) |         874 |
| `["overhead", "default"]`                           | 225.107 μs (5%) |           | 146.13 KiB (1%) |        2627 |
| `["overhead", "stoppable=false"]`                   | 227.100 μs (5%) |           | 146.17 KiB (1%) |        2630 |
| `["overhead", "stoppable=true"]`                    | 419.845 μs (5%) |           | 146.44 KiB (1%) |        2647 |
| `["parallel_histogram", "assoc", "basesize=16384"]` |   4.887 ms (5%) |           | 732.02 KiB (1%) |         101 |
| `["parallel_histogram", "assoc", "basesize=4096"]`  |   5.752 ms (5%) |           |   1.80 MiB (1%) |         495 |
| `["parallel_histogram", "assoc", "basesize=8192"]`  |   5.320 ms (5%) |           |   1.43 MiB (1%) |         240 |
| `["parallel_histogram", "comm", "basesize=16384"]`  |  13.216 ms (5%) |           |   1.25 MiB (1%) |        2142 |
| `["parallel_histogram", "comm", "basesize=4096"]`   |  19.469 ms (5%) |           |   1.12 MiB (1%) |        9572 |
| `["parallel_histogram", "comm", "basesize=8192"]`   |  15.907 ms (5%) |           |   1.30 MiB (1%) |        5058 |
| `["parallel_histogram", "seq"]`                     |   7.415 ms (5%) |           | 364.61 KiB (1%) |          24 |
| `["sum", "random", "foldl"]`                        |  14.162 ms (5%) |           |   64 bytes (1%) |           3 |
| `["sum", "random", "reduce", "basesize=128"]`       |   8.041 ms (5%) |           | 313.38 KiB (1%) |        6070 |
| `["sum", "random", "reduce", "basesize=256"]`       |   7.812 ms (5%) |           | 155.11 KiB (1%) |        3012 |
| `["sum", "random", "reduce", "basesize=512"]`       |   7.704 ms (5%) |           |  76.30 KiB (1%) |        1487 |
| `["sum", "uniform", "foldl"]`                       |  13.663 ms (5%) |           |   64 bytes (1%) |           3 |
| `["sum", "uniform", "reduce", "basesize=128"]`      |   7.784 ms (5%) |           | 313.36 KiB (1%) |        6069 |
| `["sum", "uniform", "reduce", "basesize=256"]`      |   7.559 ms (5%) |           | 155.08 KiB (1%) |        3010 |
| `["sum", "uniform", "reduce", "basesize=512"]`      |   7.448 ms (5%) |           |  76.25 KiB (1%) |        1484 |
| `["sum", "valley", "foldl"]`                        |  14.164 ms (5%) |           |   64 bytes (1%) |           3 |
| `["sum", "valley", "reduce", "basesize=128"]`       |   8.041 ms (5%) |           | 313.30 KiB (1%) |        6065 |
| `["sum", "valley", "reduce", "basesize=256"]`       |   7.835 ms (5%) |           | 155.08 KiB (1%) |        3010 |
| `["sum", "valley", "reduce", "basesize=512"]`       |   7.694 ms (5%) |           |  76.28 KiB (1%) |        1486 |
| `["words", "nthreads=1"]`                           |  44.341 ms (5%) |  7.434 ms |  62.70 MiB (1%) |     2048793 |
| `["words", "nthreads=2"]`                           |  40.872 ms (5%) |           |  63.78 MiB (1%) |     2061062 |
| `["words", "nthreads=4"]`                           |  41.709 ms (5%) |           |  64.42 MiB (1%) |     2067313 |

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
       #1  2800 MHz      68593 s          0 s       2662 s      24443 s          0 s
       #2  2800 MHz      76168 s          0 s       2326 s      18420 s          0 s
       
  Memory: 7.7900238037109375 GB (5846.84375 MB free)
  Uptime: 977.0 sec
  Load Avg:  1.728515625  1.609375  1.11962890625
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
    CPU MHz:               2800.244
    BogoMIPS:              5600.48
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

