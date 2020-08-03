# Multi-thread benchmark result (via Travis)


# Judge result
# Benchmark Report for */home/travis/build/JuliaFolds/Transducers.jl*

## Job Properties
* Time of benchmarks:
    - Target: 3 Aug 2020 - 22:41
    - Baseline: 3 Aug 2020 - 22:45
* Package commits:
    - Target: b99ae3
    - Baseline: a36be3
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
| `["collect", "unordered", "basesize=32"]`           |                   1.01 (5%)  |                1.01 (1%) :x: |
| `["parallel_histogram", "assoc", "basesize=4096"]`  |                   1.01 (5%)  |                1.15 (1%) :x: |
| `["parallel_histogram", "comm", "basesize=16384"]`  | 0.91 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["parallel_histogram", "comm", "basesize=4096"]`   | 0.95 (5%) :white_check_mark: | 0.97 (1%) :white_check_mark: |
| `["parallel_histogram", "comm", "basesize=8192"]`   |                1.23 (5%) :x: |                1.04 (1%) :x: |
| `["words", "nthreads=4"]`                           | 0.94 (5%) :white_check_mark: |                   1.00 (1%)  |

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
       #1  2800 MHz      44954 s          0 s       2299 s      23170 s          0 s
       #2  2800 MHz      55511 s          0 s       1702 s      13860 s          0 s
       
  Memory: 7.7900238037109375 GB (5793.27734375 MB free)
  Uptime: 718.0 sec
  Load Avg:  1.78857421875  1.505859375  0.84912109375
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
       #1  2800 MHz      69724 s          0 s       2697 s      26804 s          0 s
       #2  2800 MHz      75713 s          0 s       2299 s      21975 s          0 s
       
  Memory: 7.7900238037109375 GB (5819.19140625 MB free)
  Uptime: 1008.0 sec
  Load Avg:  1.74267578125  1.599609375  1.06591796875
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-8.0.1 (ORCJIT, skylake)
```

---
# Target result
# Benchmark Report for */home/travis/build/JuliaFolds/Transducers.jl*

## Job Properties
* Time of benchmark: 3 Aug 2020 - 22:41
* Package commit: b99ae3
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
| `["collect", "assoc", "basesize=1"]`                | 325.841 ms (5%) | 11.698 ms |  87.55 MiB (1%) |     1590732 |
| `["collect", "assoc", "basesize=1024"]`             | 179.580 ms (5%) |           |   1.84 MiB (1%) |        1812 |
| `["collect", "assoc", "basesize=32"]`               | 184.627 ms (5%) |           |   5.64 MiB (1%) |       53994 |
| `["collect", "seq"]`                                | 350.128 ms (5%) |           |   1.50 MiB (1%) |       32784 |
| `["collect", "unordered", "basesize=1"]`            | 371.800 ms (5%) |           |  29.16 MiB (1%) |      403155 |
| `["collect", "unordered", "basesize=1024"]`         | 212.351 ms (5%) |           | 858.83 KiB (1%) |        8057 |
| `["collect", "unordered", "basesize=32"]`           | 206.362 ms (5%) |           |   1.53 MiB (1%) |       20431 |
| `["findfirst", "n=1000", "foldl"]`                  | 558.222 ms (5%) |           |                 |             |
| `["findfirst", "n=1000", "reduce", "basesize=128"]` | 315.323 ms (5%) |           | 564.02 KiB (1%) |       10224 |
| `["findfirst", "n=1000", "reduce", "basesize=256"]` | 307.129 ms (5%) |           | 287.25 KiB (1%) |        5222 |
| `["findfirst", "n=1000", "reduce", "basesize=512"]` | 308.778 ms (5%) |           | 149.27 KiB (1%) |        2718 |
| `["findfirst", "n=400", "foldl"]`                   | 418.722 ms (5%) |           |                 |             |
| `["findfirst", "n=400", "reduce", "basesize=128"]`  | 253.301 ms (5%) |           |   1.02 MiB (1%) |       18947 |
| `["findfirst", "n=400", "reduce", "basesize=256"]`  | 238.857 ms (5%) |           | 526.09 KiB (1%) |        9566 |
| `["findfirst", "n=400", "reduce", "basesize=512"]`  | 234.074 ms (5%) |           | 267.19 KiB (1%) |        4873 |
| `["findfirst", "n=500", "foldl"]`                   |  72.534 ms (5%) |           |                 |             |
| `["findfirst", "n=500", "reduce", "basesize=128"]`  |  43.355 ms (5%) |           | 157.42 KiB (1%) |        2852 |
| `["findfirst", "n=500", "reduce", "basesize=256"]`  |  41.346 ms (5%) |           |  84.55 KiB (1%) |        1533 |
| `["findfirst", "n=500", "reduce", "basesize=512"]`  |  43.043 ms (5%) |           |  48.30 KiB (1%) |         878 |
| `["overhead", "default"]`                           | 225.920 μs (5%) |           | 146.27 KiB (1%) |        2633 |
| `["overhead", "stoppable=false"]`                   | 224.213 μs (5%) |           | 146.28 KiB (1%) |        2633 |
| `["overhead", "stoppable=true"]`                    | 422.150 μs (5%) |           | 146.58 KiB (1%) |        2652 |
| `["parallel_histogram", "assoc", "basesize=16384"]` |   4.817 ms (5%) |           | 732.06 KiB (1%) |         103 |
| `["parallel_histogram", "assoc", "basesize=4096"]`  |   5.724 ms (5%) |           |   2.07 MiB (1%) |         503 |
| `["parallel_histogram", "assoc", "basesize=8192"]`  |   5.234 ms (5%) |           |   1.43 MiB (1%) |         243 |
| `["parallel_histogram", "comm", "basesize=16384"]`  |  11.764 ms (5%) |           |   1.23 MiB (1%) |         963 |
| `["parallel_histogram", "comm", "basesize=4096"]`   |  18.012 ms (5%) |           |   1.07 MiB (1%) |        6435 |
| `["parallel_histogram", "comm", "basesize=8192"]`   |  18.929 ms (5%) |           |   1.33 MiB (1%) |        7197 |
| `["parallel_histogram", "seq"]`                     |   7.425 ms (5%) |           | 364.61 KiB (1%) |          24 |
| `["sum", "random", "foldl"]`                        |  14.068 ms (5%) |           |   64 bytes (1%) |           3 |
| `["sum", "random", "reduce", "basesize=128"]`       |   8.015 ms (5%) |           | 313.38 KiB (1%) |        6068 |
| `["sum", "random", "reduce", "basesize=256"]`       |   7.782 ms (5%) |           | 155.14 KiB (1%) |        3012 |
| `["sum", "random", "reduce", "basesize=512"]`       |   7.641 ms (5%) |           |  76.31 KiB (1%) |        1486 |
| `["sum", "uniform", "foldl"]`                       |  13.688 ms (5%) |           |   64 bytes (1%) |           3 |
| `["sum", "uniform", "reduce", "basesize=128"]`      |   7.808 ms (5%) |           | 313.42 KiB (1%) |        6071 |
| `["sum", "uniform", "reduce", "basesize=256"]`      |   7.556 ms (5%) |           | 155.14 KiB (1%) |        3012 |
| `["sum", "uniform", "reduce", "basesize=512"]`      |   7.451 ms (5%) |           |  76.31 KiB (1%) |        1486 |
| `["sum", "valley", "foldl"]`                        |  14.165 ms (5%) |           |   64 bytes (1%) |           3 |
| `["sum", "valley", "reduce", "basesize=128"]`       |   8.051 ms (5%) |           | 313.38 KiB (1%) |        6068 |
| `["sum", "valley", "reduce", "basesize=256"]`       |   7.817 ms (5%) |           | 155.16 KiB (1%) |        3013 |
| `["sum", "valley", "reduce", "basesize=512"]`       |   7.709 ms (5%) |           |  76.34 KiB (1%) |        1488 |
| `["words", "nthreads=1"]`                           |  42.685 ms (5%) |  7.258 ms |  62.72 MiB (1%) |     2049255 |
| `["words", "nthreads=2"]`                           |  39.785 ms (5%) |           |  63.80 MiB (1%) |     2061424 |
| `["words", "nthreads=4"]`                           |  40.159 ms (5%) |           |  64.75 MiB (1%) |     2071842 |

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
       #1  2800 MHz      44954 s          0 s       2299 s      23170 s          0 s
       #2  2800 MHz      55511 s          0 s       1702 s      13860 s          0 s
       
  Memory: 7.7900238037109375 GB (5793.27734375 MB free)
  Uptime: 718.0 sec
  Load Avg:  1.78857421875  1.505859375  0.84912109375
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-8.0.1 (ORCJIT, skylake)
```

---
# Baseline result
# Benchmark Report for */home/travis/build/JuliaFolds/Transducers.jl*

## Job Properties
* Time of benchmark: 3 Aug 2020 - 22:45
* Package commit: a36be3
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
| `["collect", "assoc", "basesize=1"]`                | 324.736 ms (5%) | 13.574 ms |  87.55 MiB (1%) |     1590783 |
| `["collect", "assoc", "basesize=1024"]`             | 179.782 ms (5%) |           |   1.84 MiB (1%) |        1808 |
| `["collect", "assoc", "basesize=32"]`               | 184.462 ms (5%) |           |   5.64 MiB (1%) |       54011 |
| `["collect", "seq"]`                                | 349.962 ms (5%) |           |   1.50 MiB (1%) |       32784 |
| `["collect", "unordered", "basesize=1"]`            | 371.451 ms (5%) |           |  29.16 MiB (1%) |      403003 |
| `["collect", "unordered", "basesize=1024"]`         | 211.141 ms (5%) |           | 857.88 KiB (1%) |        7615 |
| `["collect", "unordered", "basesize=32"]`           | 204.764 ms (5%) |           |   1.51 MiB (1%) |       19435 |
| `["findfirst", "n=1000", "foldl"]`                  | 551.701 ms (5%) |           |                 |             |
| `["findfirst", "n=1000", "reduce", "basesize=128"]` | 310.661 ms (5%) |           | 563.95 KiB (1%) |       10220 |
| `["findfirst", "n=1000", "reduce", "basesize=256"]` | 302.727 ms (5%) |           | 287.25 KiB (1%) |        5222 |
| `["findfirst", "n=1000", "reduce", "basesize=512"]` | 304.668 ms (5%) |           | 149.34 KiB (1%) |        2723 |
| `["findfirst", "n=400", "foldl"]`                   | 414.092 ms (5%) |           |                 |             |
| `["findfirst", "n=400", "reduce", "basesize=128"]`  | 249.999 ms (5%) |           |   1.02 MiB (1%) |       18948 |
| `["findfirst", "n=400", "reduce", "basesize=256"]`  | 235.690 ms (5%) |           | 525.94 KiB (1%) |        9556 |
| `["findfirst", "n=400", "reduce", "basesize=512"]`  | 230.771 ms (5%) |           | 267.14 KiB (1%) |        4870 |
| `["findfirst", "n=500", "foldl"]`                   |  71.753 ms (5%) |           |                 |             |
| `["findfirst", "n=500", "reduce", "basesize=128"]`  |  42.699 ms (5%) |           | 157.45 KiB (1%) |        2854 |
| `["findfirst", "n=500", "reduce", "basesize=256"]`  |  40.795 ms (5%) |           |  84.55 KiB (1%) |        1533 |
| `["findfirst", "n=500", "reduce", "basesize=512"]`  |  42.440 ms (5%) |           |  48.30 KiB (1%) |         878 |
| `["overhead", "default"]`                           | 223.268 μs (5%) |           | 146.27 KiB (1%) |        2633 |
| `["overhead", "stoppable=false"]`                   | 223.055 μs (5%) |           | 146.28 KiB (1%) |        2633 |
| `["overhead", "stoppable=true"]`                    | 425.702 μs (5%) |           | 146.56 KiB (1%) |        2651 |
| `["parallel_histogram", "assoc", "basesize=16384"]` |   4.824 ms (5%) |           | 732.06 KiB (1%) |         103 |
| `["parallel_histogram", "assoc", "basesize=4096"]`  |   5.653 ms (5%) |           |   1.80 MiB (1%) |         497 |
| `["parallel_histogram", "assoc", "basesize=8192"]`  |   5.254 ms (5%) |           |   1.43 MiB (1%) |         243 |
| `["parallel_histogram", "comm", "basesize=16384"]`  |  12.964 ms (5%) |           |   1.23 MiB (1%) |         998 |
| `["parallel_histogram", "comm", "basesize=4096"]`   |  18.967 ms (5%) |           |   1.11 MiB (1%) |        8907 |
| `["parallel_histogram", "comm", "basesize=8192"]`   |  15.408 ms (5%) |           |   1.28 MiB (1%) |        3743 |
| `["parallel_histogram", "seq"]`                     |   7.408 ms (5%) |           | 364.61 KiB (1%) |          24 |
| `["sum", "random", "foldl"]`                        |  14.156 ms (5%) |           |   64 bytes (1%) |           3 |
| `["sum", "random", "reduce", "basesize=128"]`       |   8.038 ms (5%) |           | 313.44 KiB (1%) |        6072 |
| `["sum", "random", "reduce", "basesize=256"]`       |   7.832 ms (5%) |           | 155.16 KiB (1%) |        3013 |
| `["sum", "random", "reduce", "basesize=512"]`       |   7.685 ms (5%) |           |  76.33 KiB (1%) |        1487 |
| `["sum", "uniform", "foldl"]`                       |  13.669 ms (5%) |           |   64 bytes (1%) |           3 |
| `["sum", "uniform", "reduce", "basesize=128"]`      |   7.784 ms (5%) |           | 313.41 KiB (1%) |        6070 |
| `["sum", "uniform", "reduce", "basesize=256"]`      |   7.542 ms (5%) |           | 155.14 KiB (1%) |        3012 |
| `["sum", "uniform", "reduce", "basesize=512"]`      |   7.430 ms (5%) |           |  76.31 KiB (1%) |        1486 |
| `["sum", "valley", "foldl"]`                        |  14.163 ms (5%) |           |   64 bytes (1%) |           3 |
| `["sum", "valley", "reduce", "basesize=128"]`       |   8.036 ms (5%) |           | 313.34 KiB (1%) |        6066 |
| `["sum", "valley", "reduce", "basesize=256"]`       |   7.831 ms (5%) |           | 155.16 KiB (1%) |        3013 |
| `["sum", "valley", "reduce", "basesize=512"]`       |   7.682 ms (5%) |           |  76.34 KiB (1%) |        1488 |
| `["words", "nthreads=1"]`                           |  43.304 ms (5%) |  7.112 ms |  63.31 MiB (1%) |     2068829 |
| `["words", "nthreads=2"]`                           |  40.182 ms (5%) |           |  64.40 MiB (1%) |     2081106 |
| `["words", "nthreads=4"]`                           |  42.902 ms (5%) |           |  65.04 MiB (1%) |     2087340 |

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
       #1  2800 MHz      69724 s          0 s       2697 s      26804 s          0 s
       #2  2800 MHz      75713 s          0 s       2299 s      21975 s          0 s
       
  Memory: 7.7900238037109375 GB (5819.19140625 MB free)
  Uptime: 1008.0 sec
  Load Avg:  1.74267578125  1.599609375  1.06591796875
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
    CPU MHz:               2800.182
    BogoMIPS:              5600.36
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

