# Multi-thread benchmark result (via Travis)


# Judge result
# Benchmark Report for */home/travis/build/JuliaFolds/Transducers.jl*

## Job Properties
* Time of benchmarks:
    - Target: 17 Nov 2020 - 07:27
    - Baseline: 17 Nov 2020 - 07:32
* Package commits:
    - Target: 17ddce
    - Baseline: 8cfd2b
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
| `["collect", "assoc", "basesize=1"]`                | 0.94 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["parallel_histogram", "assoc", "basesize=4096"]`  |                   1.02 (5%)  |                1.15 (1%) :x: |
| `["parallel_histogram", "comm", "basesize=16384"]`  |                   1.01 (5%)  |                1.01 (1%) :x: |
| `["parallel_histogram", "comm", "basesize=4096"]`   |                1.06 (5%) :x: |                   1.00 (1%)  |
| `["parallel_histogram", "comm", "basesize=8192"]`   |                   1.01 (5%)  | 0.98 (1%) :white_check_mark: |

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
      Ubuntu 16.04.6 LTS
  uname: Linux 4.15.0-1028-gcp #29~16.04.1-Ubuntu SMP Tue Feb 12 16:31:10 UTC 2019 x86_64 x86_64
  CPU: Intel(R) Xeon(R) CPU: 
              speed         user         nice          sys         idle          irq
       #1  2800 MHz      48178 s          0 s       1832 s      16617 s          0 s
       #2  2800 MHz      50687 s          0 s       1647 s      14533 s          0 s
       
  Memory: 7.790031433105469 GB (5895.51171875 MB free)
  Uptime: 673.0 sec
  Load Avg:  1.77001953125  1.49072265625  0.8369140625
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-9.0.1 (ORCJIT, cascadelake)
```

### Baseline
```
Julia Version 1.5.3
Commit 788b2c77c1 (2020-11-09 13:37 UTC)
Platform Info:
  OS: Linux (x86_64-pc-linux-gnu)
      Ubuntu 16.04.6 LTS
  uname: Linux 4.15.0-1028-gcp #29~16.04.1-Ubuntu SMP Tue Feb 12 16:31:10 UTC 2019 x86_64 x86_64
  CPU: Intel(R) Xeon(R) CPU: 
              speed         user         nice          sys         idle          irq
       #1  2800 MHz      71102 s          0 s       2342 s      23636 s          0 s
       #2  2800 MHz      74245 s          0 s       2091 s      20836 s          0 s
       
  Memory: 7.790031433105469 GB (5902.8671875 MB free)
  Uptime: 978.0 sec
  Load Avg:  1.6328125  1.537109375  1.041015625
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-9.0.1 (ORCJIT, cascadelake)
```

---
# Target result
# Benchmark Report for */home/travis/build/JuliaFolds/Transducers.jl*

## Job Properties
* Time of benchmark: 17 Nov 2020 - 7:27
* Package commit: 17ddce
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
| `["collect", "assoc", "basesize=1"]`                | 311.212 ms (5%) | 16.007 ms |   82.16 MiB (1%) |     1368081 |
| `["collect", "assoc", "basesize=1024"]`             | 179.531 ms (5%) |           |    1.83 MiB (1%) |        1596 |
| `["collect", "assoc", "basesize=32"]`               | 184.061 ms (5%) |           |    5.47 MiB (1%) |       47069 |
| `["collect", "seq"]`                                | 349.602 ms (5%) |           |  512.72 KiB (1%) |          15 |
| `["collect", "unordered", "basesize=1"]`            | 350.674 ms (5%) |           |   30.01 MiB (1%) |      360708 |
| `["collect", "unordered", "basesize=1024"]`         | 199.450 ms (5%) |           |  805.61 KiB (1%) |        2501 |
| `["collect", "unordered", "basesize=32"]`           | 197.875 ms (5%) |           |    1.48 MiB (1%) |       12961 |
| `["findfirst", "n=1000", "foldl"]`                  | 555.941 ms (5%) |           |                  |             |
| `["findfirst", "n=1000", "reduce", "basesize=128"]` | 300.594 ms (5%) |           |  546.34 KiB (1%) |        9562 |
| `["findfirst", "n=1000", "reduce", "basesize=256"]` | 299.455 ms (5%) |           |  278.25 KiB (1%) |        4888 |
| `["findfirst", "n=1000", "reduce", "basesize=512"]` | 305.549 ms (5%) |           |  144.66 KiB (1%) |        2550 |
| `["findfirst", "n=400", "foldl"]`                   | 417.035 ms (5%) |           |                  |             |
| `["findfirst", "n=400", "reduce", "basesize=128"]`  | 227.678 ms (5%) |           | 1012.89 KiB (1%) |       17726 |
| `["findfirst", "n=400", "reduce", "basesize=256"]`  | 225.319 ms (5%) |           |  509.63 KiB (1%) |        8952 |
| `["findfirst", "n=400", "reduce", "basesize=512"]`  | 225.901 ms (5%) |           |  258.83 KiB (1%) |        4563 |
| `["findfirst", "n=500", "foldl"]`                   |  72.260 ms (5%) |           |                  |             |
| `["findfirst", "n=500", "reduce", "basesize=128"]`  |  39.664 ms (5%) |           |  152.59 KiB (1%) |        2677 |
| `["findfirst", "n=500", "reduce", "basesize=256"]`  |  39.402 ms (5%) |           |   82.00 KiB (1%) |        1444 |
| `["findfirst", "n=500", "reduce", "basesize=512"]`  |  41.891 ms (5%) |           |   46.84 KiB (1%) |         828 |
| `["overhead", "default"]`                           | 191.019 μs (5%) |           |  140.75 KiB (1%) |        2465 |
| `["overhead", "stoppable=false"]`                   | 189.488 μs (5%) |           |  140.78 KiB (1%) |        2465 |
| `["overhead", "stoppable=true"]`                    | 359.417 μs (5%) |           |  140.81 KiB (1%) |        2466 |
| `["parallel_histogram", "assoc", "basesize=16384"]` |   4.885 ms (5%) |           |  731.81 KiB (1%) |          94 |
| `["parallel_histogram", "assoc", "basesize=4096"]`  |   5.810 ms (5%) |           |    2.07 MiB (1%) |         454 |
| `["parallel_histogram", "assoc", "basesize=8192"]`  |   5.299 ms (5%) |           |    1.43 MiB (1%) |         220 |
| `["parallel_histogram", "comm", "basesize=16384"]`  |  12.346 ms (5%) |           |    1.26 MiB (1%) |        1313 |
| `["parallel_histogram", "comm", "basesize=4096"]`   |  15.929 ms (5%) |           |    1.18 MiB (1%) |        4939 |
| `["parallel_histogram", "comm", "basesize=8192"]`   |  13.761 ms (5%) |           |    1.28 MiB (1%) |        2101 |
| `["parallel_histogram", "seq"]`                     |   7.456 ms (5%) |           |  364.61 KiB (1%) |          24 |
| `["sum", "random", "foldl"]`                        |  14.108 ms (5%) |           |    32 bytes (1%) |           2 |
| `["sum", "random", "reduce", "basesize=128"]`       |   8.053 ms (5%) |           |  292.02 KiB (1%) |        5213 |
| `["sum", "random", "reduce", "basesize=256"]`       |   7.863 ms (5%) |           |  144.56 KiB (1%) |        2590 |
| `["sum", "random", "reduce", "basesize=512"]`       |   7.736 ms (5%) |           |   71.11 KiB (1%) |        1279 |
| `["sum", "uniform", "foldl"]`                       |  13.699 ms (5%) |           |    32 bytes (1%) |           2 |
| `["sum", "uniform", "reduce", "basesize=128"]`      |   7.780 ms (5%) |           |  292.02 KiB (1%) |        5213 |
| `["sum", "uniform", "reduce", "basesize=256"]`      |   7.561 ms (5%) |           |  144.56 KiB (1%) |        2590 |
| `["sum", "uniform", "reduce", "basesize=512"]`      |   7.454 ms (5%) |           |   71.06 KiB (1%) |        1278 |
| `["sum", "valley", "foldl"]`                        |  14.118 ms (5%) |           |    32 bytes (1%) |           2 |
| `["sum", "valley", "reduce", "basesize=128"]`       |   8.079 ms (5%) |           |  292.02 KiB (1%) |        5213 |
| `["sum", "valley", "reduce", "basesize=256"]`       |   7.877 ms (5%) |           |  144.53 KiB (1%) |        2589 |
| `["sum", "valley", "reduce", "basesize=512"]`       |   7.750 ms (5%) |           |   71.06 KiB (1%) |        1278 |
| `["words", "nthreads=1"]`                           |  23.398 ms (5%) |           |   31.58 MiB (1%) |     1028549 |
| `["words", "nthreads=2"]`                           |  26.101 ms (5%) |           |   32.29 MiB (1%) |     1028715 |
| `["words", "nthreads=4"]`                           |  26.807 ms (5%) |           |   32.75 MiB (1%) |     1028850 |

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
      Ubuntu 16.04.6 LTS
  uname: Linux 4.15.0-1028-gcp #29~16.04.1-Ubuntu SMP Tue Feb 12 16:31:10 UTC 2019 x86_64 x86_64
  CPU: Intel(R) Xeon(R) CPU: 
              speed         user         nice          sys         idle          irq
       #1  2800 MHz      48178 s          0 s       1832 s      16617 s          0 s
       #2  2800 MHz      50687 s          0 s       1647 s      14533 s          0 s
       
  Memory: 7.790031433105469 GB (5895.51171875 MB free)
  Uptime: 673.0 sec
  Load Avg:  1.77001953125  1.49072265625  0.8369140625
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-9.0.1 (ORCJIT, cascadelake)
```

---
# Baseline result
# Benchmark Report for */home/travis/build/JuliaFolds/Transducers.jl*

## Job Properties
* Time of benchmark: 17 Nov 2020 - 7:32
* Package commit: 8cfd2b
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
| `["collect", "assoc", "basesize=1"]`                | 331.136 ms (5%) | 15.934 ms |   82.16 MiB (1%) |     1368070 |
| `["collect", "assoc", "basesize=1024"]`             | 179.895 ms (5%) |           |    1.83 MiB (1%) |        1597 |
| `["collect", "assoc", "basesize=32"]`               | 185.065 ms (5%) |           |    5.47 MiB (1%) |       47069 |
| `["collect", "seq"]`                                | 349.733 ms (5%) |           |  512.72 KiB (1%) |          15 |
| `["collect", "unordered", "basesize=1"]`            | 340.352 ms (5%) |           |   30.01 MiB (1%) |      360645 |
| `["collect", "unordered", "basesize=1024"]`         | 194.655 ms (5%) |           |  798.39 KiB (1%) |        2288 |
| `["collect", "unordered", "basesize=32"]`           | 197.791 ms (5%) |           |    1.49 MiB (1%) |       12990 |
| `["findfirst", "n=1000", "foldl"]`                  | 555.898 ms (5%) |           |                  |             |
| `["findfirst", "n=1000", "reduce", "basesize=128"]` | 300.540 ms (5%) |           |  546.33 KiB (1%) |        9561 |
| `["findfirst", "n=1000", "reduce", "basesize=256"]` | 299.710 ms (5%) |           |  278.25 KiB (1%) |        4888 |
| `["findfirst", "n=1000", "reduce", "basesize=512"]` | 304.879 ms (5%) |           |  144.66 KiB (1%) |        2550 |
| `["findfirst", "n=400", "foldl"]`                   | 417.055 ms (5%) |           |                  |             |
| `["findfirst", "n=400", "reduce", "basesize=128"]`  | 228.266 ms (5%) |           | 1012.89 KiB (1%) |       17726 |
| `["findfirst", "n=400", "reduce", "basesize=256"]`  | 225.627 ms (5%) |           |  509.63 KiB (1%) |        8952 |
| `["findfirst", "n=400", "reduce", "basesize=512"]`  | 227.199 ms (5%) |           |  258.84 KiB (1%) |        4564 |
| `["findfirst", "n=500", "foldl"]`                   |  72.239 ms (5%) |           |                  |             |
| `["findfirst", "n=500", "reduce", "basesize=128"]`  |  39.658 ms (5%) |           |  152.59 KiB (1%) |        2677 |
| `["findfirst", "n=500", "reduce", "basesize=256"]`  |  39.398 ms (5%) |           |   82.00 KiB (1%) |        1444 |
| `["findfirst", "n=500", "reduce", "basesize=512"]`  |  41.917 ms (5%) |           |   46.84 KiB (1%) |         828 |
| `["overhead", "default"]`                           | 195.722 μs (5%) |           |  140.75 KiB (1%) |        2465 |
| `["overhead", "stoppable=false"]`                   | 196.933 μs (5%) |           |  140.78 KiB (1%) |        2465 |
| `["overhead", "stoppable=true"]`                    | 373.475 μs (5%) |           |  140.81 KiB (1%) |        2466 |
| `["parallel_histogram", "assoc", "basesize=16384"]` |   4.854 ms (5%) |           |  731.81 KiB (1%) |          94 |
| `["parallel_histogram", "assoc", "basesize=4096"]`  |   5.689 ms (5%) |           |    1.80 MiB (1%) |         448 |
| `["parallel_histogram", "assoc", "basesize=8192"]`  |   5.315 ms (5%) |           |    1.43 MiB (1%) |         220 |
| `["parallel_histogram", "comm", "basesize=16384"]`  |  12.211 ms (5%) |           |    1.24 MiB (1%) |         899 |
| `["parallel_histogram", "comm", "basesize=4096"]`   |  15.078 ms (5%) |           |    1.18 MiB (1%) |        5383 |
| `["parallel_histogram", "comm", "basesize=8192"]`   |  13.646 ms (5%) |           |    1.30 MiB (1%) |        2784 |
| `["parallel_histogram", "seq"]`                     |   7.438 ms (5%) |           |  364.61 KiB (1%) |          24 |
| `["sum", "random", "foldl"]`                        |  13.958 ms (5%) |           |    32 bytes (1%) |           2 |
| `["sum", "random", "reduce", "basesize=128"]`       |   7.980 ms (5%) |           |  292.02 KiB (1%) |        5213 |
| `["sum", "random", "reduce", "basesize=256"]`       |   7.742 ms (5%) |           |  144.53 KiB (1%) |        2589 |
| `["sum", "random", "reduce", "basesize=512"]`       |   7.635 ms (5%) |           |   71.11 KiB (1%) |        1279 |
| `["sum", "uniform", "foldl"]`                       |  13.706 ms (5%) |           |    32 bytes (1%) |           2 |
| `["sum", "uniform", "reduce", "basesize=128"]`      |   7.777 ms (5%) |           |  292.02 KiB (1%) |        5213 |
| `["sum", "uniform", "reduce", "basesize=256"]`      |   7.567 ms (5%) |           |  144.53 KiB (1%) |        2589 |
| `["sum", "uniform", "reduce", "basesize=512"]`      |   7.452 ms (5%) |           |   71.06 KiB (1%) |        1278 |
| `["sum", "valley", "foldl"]`                        |  14.120 ms (5%) |           |    32 bytes (1%) |           2 |
| `["sum", "valley", "reduce", "basesize=128"]`       |   8.084 ms (5%) |           |  292.02 KiB (1%) |        5213 |
| `["sum", "valley", "reduce", "basesize=256"]`       |   7.878 ms (5%) |           |  144.53 KiB (1%) |        2589 |
| `["sum", "valley", "reduce", "basesize=512"]`       |   7.744 ms (5%) |           |   71.06 KiB (1%) |        1278 |
| `["words", "nthreads=1"]`                           |  23.620 ms (5%) |           |   31.68 MiB (1%) |     1032500 |
| `["words", "nthreads=2"]`                           |  25.014 ms (5%) |           |   32.04 MiB (1%) |     1032569 |
| `["words", "nthreads=4"]`                           |  26.641 ms (5%) |           |   32.75 MiB (1%) |     1032712 |

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
      Ubuntu 16.04.6 LTS
  uname: Linux 4.15.0-1028-gcp #29~16.04.1-Ubuntu SMP Tue Feb 12 16:31:10 UTC 2019 x86_64 x86_64
  CPU: Intel(R) Xeon(R) CPU: 
              speed         user         nice          sys         idle          irq
       #1  2800 MHz      71102 s          0 s       2342 s      23636 s          0 s
       #2  2800 MHz      74245 s          0 s       2091 s      20836 s          0 s
       
  Memory: 7.790031433105469 GB (5902.8671875 MB free)
  Uptime: 978.0 sec
  Load Avg:  1.6328125  1.537109375  1.041015625
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-9.0.1 (ORCJIT, cascadelake)
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
    CPU MHz:               2800.190
    BogoMIPS:              5600.38
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

