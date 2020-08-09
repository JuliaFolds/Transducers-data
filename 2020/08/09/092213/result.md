# Multi-thread benchmark result (via Travis)


# Judge result
# Benchmark Report for */home/travis/build/JuliaFolds/Transducers.jl*

## Job Properties
* Time of benchmarks:
    - Target: 9 Aug 2020 - 09:17
    - Baseline: 9 Aug 2020 - 09:21
* Package commits:
    - Target: 25eaf0
    - Baseline: b8efee
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
| `["collect", "unordered", "basesize=1024"]`         | 0.75 (5%) :white_check_mark: | 0.80 (1%) :white_check_mark: |
| `["collect", "unordered", "basesize=32"]`           |                   1.00 (5%)  | 0.99 (1%) :white_check_mark: |
| `["parallel_histogram", "comm", "basesize=16384"]`  | 0.86 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["parallel_histogram", "comm", "basesize=8192"]`   |                   0.99 (5%)  | 0.99 (1%) :white_check_mark: |
| `["words", "nthreads=2"]`                           |                   0.97 (5%)  | 0.99 (1%) :white_check_mark: |
| `["words", "nthreads=4"]`                           |                   0.96 (5%)  | 0.99 (1%) :white_check_mark: |

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
       #1  2800 MHz      51114 s          0 s       1805 s      14510 s          0 s
       #2  2800 MHz      49605 s          0 s       2310 s      16376 s          0 s
       
  Memory: 7.790031433105469 GB (5854.89453125 MB free)
  Uptime: 691.0 sec
  Load Avg:  1.75146484375  1.5693359375  0.90673828125
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
       #1  2800 MHz      72167 s          0 s       2387 s      22106 s          0 s
       #2  2800 MHz      73876 s          0 s       2704 s      20922 s          0 s
       
  Memory: 7.790031433105469 GB (5874.0625 MB free)
  Uptime: 984.0 sec
  Load Avg:  1.7255859375  1.60205078125  1.0966796875
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-8.0.1 (ORCJIT, skylake)
```

---
# Target result
# Benchmark Report for */home/travis/build/JuliaFolds/Transducers.jl*

## Job Properties
* Time of benchmark: 9 Aug 2020 - 9:17
* Package commit: 25eaf0
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
| `["collect", "assoc", "basesize=1"]`                | 322.065 ms (5%) | 11.729 ms |  87.55 MiB (1%) |     1590665 |
| `["collect", "assoc", "basesize=1024"]`             | 179.595 ms (5%) |           |   1.84 MiB (1%) |        1812 |
| `["collect", "assoc", "basesize=32"]`               | 184.240 ms (5%) |           |   5.64 MiB (1%) |       54016 |
| `["collect", "seq"]`                                | 349.719 ms (5%) |           |   1.50 MiB (1%) |       32784 |
| `["collect", "unordered", "basesize=1"]`            | 380.263 ms (5%) |           |  29.17 MiB (1%) |      404033 |
| `["collect", "unordered", "basesize=1024"]`         | 210.499 ms (5%) |           | 823.72 KiB (1%) |        5810 |
| `["collect", "unordered", "basesize=32"]`           | 206.004 ms (5%) |           |   1.51 MiB (1%) |       19345 |
| `["findfirst", "n=1000", "foldl"]`                  | 551.137 ms (5%) |           |                 |             |
| `["findfirst", "n=1000", "reduce", "basesize=128"]` | 310.776 ms (5%) |           | 563.97 KiB (1%) |       10221 |
| `["findfirst", "n=1000", "reduce", "basesize=256"]` | 303.094 ms (5%) |           | 287.20 KiB (1%) |        5219 |
| `["findfirst", "n=1000", "reduce", "basesize=512"]` | 304.617 ms (5%) |           | 149.30 KiB (1%) |        2720 |
| `["findfirst", "n=400", "foldl"]`                   | 413.708 ms (5%) |           |                 |             |
| `["findfirst", "n=400", "reduce", "basesize=128"]`  | 250.317 ms (5%) |           |   1.02 MiB (1%) |       18953 |
| `["findfirst", "n=400", "reduce", "basesize=256"]`  | 235.651 ms (5%) |           | 526.05 KiB (1%) |        9563 |
| `["findfirst", "n=400", "reduce", "basesize=512"]`  | 230.851 ms (5%) |           | 267.20 KiB (1%) |        4874 |
| `["findfirst", "n=500", "foldl"]`                   |  71.668 ms (5%) |           |                 |             |
| `["findfirst", "n=500", "reduce", "basesize=128"]`  |  42.780 ms (5%) |           | 157.42 KiB (1%) |        2852 |
| `["findfirst", "n=500", "reduce", "basesize=256"]`  |  40.734 ms (5%) |           |  84.58 KiB (1%) |        1535 |
| `["findfirst", "n=500", "reduce", "basesize=512"]`  |  42.456 ms (5%) |           |  48.30 KiB (1%) |         878 |
| `["overhead", "default"]`                           | 221.438 μs (5%) |           | 146.28 KiB (1%) |        2634 |
| `["overhead", "stoppable=false"]`                   | 221.040 μs (5%) |           | 146.25 KiB (1%) |        2631 |
| `["overhead", "stoppable=true"]`                    | 415.398 μs (5%) |           | 146.58 KiB (1%) |        2652 |
| `["parallel_histogram", "assoc", "basesize=16384"]` |   4.921 ms (5%) |           | 732.06 KiB (1%) |         103 |
| `["parallel_histogram", "assoc", "basesize=4096"]`  |   5.767 ms (5%) |           |   1.80 MiB (1%) |         497 |
| `["parallel_histogram", "assoc", "basesize=8192"]`  |   5.347 ms (5%) |           |   1.43 MiB (1%) |         243 |
| `["parallel_histogram", "comm", "basesize=16384"]`  |  11.455 ms (5%) |           |   1.23 MiB (1%) |         574 |
| `["parallel_histogram", "comm", "basesize=4096"]`   |  19.134 ms (5%) |           |   1.12 MiB (1%) |        7833 |
| `["parallel_histogram", "comm", "basesize=8192"]`   |  14.995 ms (5%) |           |   1.27 MiB (1%) |        3106 |
| `["parallel_histogram", "seq"]`                     |   7.299 ms (5%) |           | 364.61 KiB (1%) |          24 |
| `["sum", "random", "foldl"]`                        |  13.981 ms (5%) |           |   64 bytes (1%) |           3 |
| `["sum", "random", "reduce", "basesize=128"]`       |   7.928 ms (5%) |           | 313.39 KiB (1%) |        6069 |
| `["sum", "random", "reduce", "basesize=256"]`       |   7.684 ms (5%) |           | 155.16 KiB (1%) |        3013 |
| `["sum", "random", "reduce", "basesize=512"]`       |   7.588 ms (5%) |           |  76.31 KiB (1%) |        1486 |
| `["sum", "uniform", "foldl"]`                       |  13.688 ms (5%) |           |   64 bytes (1%) |           3 |
| `["sum", "uniform", "reduce", "basesize=128"]`      |   7.788 ms (5%) |           | 313.41 KiB (1%) |        6070 |
| `["sum", "uniform", "reduce", "basesize=256"]`      |   7.548 ms (5%) |           | 155.14 KiB (1%) |        3012 |
| `["sum", "uniform", "reduce", "basesize=512"]`      |   7.442 ms (5%) |           |  76.31 KiB (1%) |        1486 |
| `["sum", "valley", "foldl"]`                        |  14.149 ms (5%) |           |   64 bytes (1%) |           3 |
| `["sum", "valley", "reduce", "basesize=128"]`       |   8.013 ms (5%) |           | 313.36 KiB (1%) |        6067 |
| `["sum", "valley", "reduce", "basesize=256"]`       |   7.792 ms (5%) |           | 155.16 KiB (1%) |        3013 |
| `["sum", "valley", "reduce", "basesize=512"]`       |   7.672 ms (5%) |           |  76.34 KiB (1%) |        1488 |
| `["words", "nthreads=1"]`                           |  33.339 ms (5%) |  6.861 ms |  63.14 MiB (1%) |     2063016 |
| `["words", "nthreads=2"]`                           |  28.311 ms (5%) |           |  63.75 MiB (1%) |     2071151 |
| `["words", "nthreads=4"]`                           |  29.916 ms (5%) |           |  64.71 MiB (1%) |     2079336 |

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
       #1  2800 MHz      51114 s          0 s       1805 s      14510 s          0 s
       #2  2800 MHz      49605 s          0 s       2310 s      16376 s          0 s
       
  Memory: 7.790031433105469 GB (5854.89453125 MB free)
  Uptime: 691.0 sec
  Load Avg:  1.75146484375  1.5693359375  0.90673828125
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-8.0.1 (ORCJIT, skylake)
```

---
# Baseline result
# Benchmark Report for */home/travis/build/JuliaFolds/Transducers.jl*

## Job Properties
* Time of benchmark: 9 Aug 2020 - 9:21
* Package commit: b8efee
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
| `["collect", "assoc", "basesize=1"]`                | 322.525 ms (5%) | 12.522 ms |  87.55 MiB (1%) |     1590638 |
| `["collect", "assoc", "basesize=1024"]`             | 179.534 ms (5%) |           |   1.84 MiB (1%) |        1811 |
| `["collect", "assoc", "basesize=32"]`               | 184.023 ms (5%) |           |   5.64 MiB (1%) |       54013 |
| `["collect", "seq"]`                                | 349.776 ms (5%) |           |   1.50 MiB (1%) |       32784 |
| `["collect", "unordered", "basesize=1"]`            | 372.857 ms (5%) | 10.094 ms |  29.16 MiB (1%) |      403532 |
| `["collect", "unordered", "basesize=1024"]`         | 279.499 ms (5%) |           |   1.01 MiB (1%) |       19354 |
| `["collect", "unordered", "basesize=32"]`           | 205.026 ms (5%) |           |   1.53 MiB (1%) |       20692 |
| `["findfirst", "n=1000", "foldl"]`                  | 552.626 ms (5%) |           |                 |             |
| `["findfirst", "n=1000", "reduce", "basesize=128"]` | 311.499 ms (5%) |           | 564.03 KiB (1%) |       10225 |
| `["findfirst", "n=1000", "reduce", "basesize=256"]` | 303.516 ms (5%) |           | 287.14 KiB (1%) |        5215 |
| `["findfirst", "n=1000", "reduce", "basesize=512"]` | 305.111 ms (5%) |           | 149.30 KiB (1%) |        2720 |
| `["findfirst", "n=400", "foldl"]`                   | 414.746 ms (5%) |           |                 |             |
| `["findfirst", "n=400", "reduce", "basesize=128"]`  | 250.672 ms (5%) |           |   1.02 MiB (1%) |       18950 |
| `["findfirst", "n=400", "reduce", "basesize=256"]`  | 236.164 ms (5%) |           | 526.09 KiB (1%) |        9566 |
| `["findfirst", "n=400", "reduce", "basesize=512"]`  | 231.270 ms (5%) |           | 267.09 KiB (1%) |        4867 |
| `["findfirst", "n=500", "foldl"]`                   |  71.875 ms (5%) |           |                 |             |
| `["findfirst", "n=500", "reduce", "basesize=128"]`  |  42.824 ms (5%) |           | 157.41 KiB (1%) |        2851 |
| `["findfirst", "n=500", "reduce", "basesize=256"]`  |  40.849 ms (5%) |           |  84.58 KiB (1%) |        1535 |
| `["findfirst", "n=500", "reduce", "basesize=512"]`  |  42.522 ms (5%) |           |  48.31 KiB (1%) |         879 |
| `["overhead", "default"]`                           | 222.130 μs (5%) |           | 146.22 KiB (1%) |        2630 |
| `["overhead", "stoppable=false"]`                   | 222.969 μs (5%) |           | 146.27 KiB (1%) |        2632 |
| `["overhead", "stoppable=true"]`                    | 427.047 μs (5%) |           | 146.55 KiB (1%) |        2650 |
| `["parallel_histogram", "assoc", "basesize=16384"]` |   4.864 ms (5%) |           | 732.06 KiB (1%) |         103 |
| `["parallel_histogram", "assoc", "basesize=4096"]`  |   5.723 ms (5%) |           |   1.80 MiB (1%) |         497 |
| `["parallel_histogram", "assoc", "basesize=8192"]`  |   5.313 ms (5%) |           |   1.43 MiB (1%) |         243 |
| `["parallel_histogram", "comm", "basesize=16384"]`  |  13.378 ms (5%) |           |   1.23 MiB (1%) |         789 |
| `["parallel_histogram", "comm", "basesize=4096"]`   |  18.847 ms (5%) |           |   1.12 MiB (1%) |        9403 |
| `["parallel_histogram", "comm", "basesize=8192"]`   |  15.197 ms (5%) |           |   1.28 MiB (1%) |        4101 |
| `["parallel_histogram", "seq"]`                     |   7.299 ms (5%) |           | 364.61 KiB (1%) |          24 |
| `["sum", "random", "foldl"]`                        |  14.044 ms (5%) |           |   64 bytes (1%) |           3 |
| `["sum", "random", "reduce", "basesize=128"]`       |   8.032 ms (5%) |           | 313.41 KiB (1%) |        6070 |
| `["sum", "random", "reduce", "basesize=256"]`       |   7.784 ms (5%) |           | 155.13 KiB (1%) |        3011 |
| `["sum", "random", "reduce", "basesize=512"]`       |   7.629 ms (5%) |           |  76.31 KiB (1%) |        1486 |
| `["sum", "uniform", "foldl"]`                       |  13.654 ms (5%) |           |   64 bytes (1%) |           3 |
| `["sum", "uniform", "reduce", "basesize=128"]`      |   7.958 ms (5%) |           | 313.44 KiB (1%) |        6072 |
| `["sum", "uniform", "reduce", "basesize=256"]`      |   7.732 ms (5%) |           | 155.14 KiB (1%) |        3012 |
| `["sum", "uniform", "reduce", "basesize=512"]`      |   7.513 ms (5%) |           |  76.31 KiB (1%) |        1486 |
| `["sum", "valley", "foldl"]`                        |  14.277 ms (5%) |           |   64 bytes (1%) |           3 |
| `["sum", "valley", "reduce", "basesize=128"]`       |   8.123 ms (5%) |           | 313.34 KiB (1%) |        6066 |
| `["sum", "valley", "reduce", "basesize=256"]`       |   7.818 ms (5%) |           | 155.14 KiB (1%) |        3012 |
| `["sum", "valley", "reduce", "basesize=512"]`       |   7.688 ms (5%) |           |  76.34 KiB (1%) |        1488 |
| `["words", "nthreads=1"]`                           |  34.558 ms (5%) |  7.015 ms |  63.46 MiB (1%) |     2072853 |
| `["words", "nthreads=2"]`                           |  29.304 ms (5%) |           |  64.55 MiB (1%) |     2085023 |
| `["words", "nthreads=4"]`                           |  31.241 ms (5%) |           |  65.49 MiB (1%) |     2095401 |

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
       #1  2800 MHz      72167 s          0 s       2387 s      22106 s          0 s
       #2  2800 MHz      73876 s          0 s       2704 s      20922 s          0 s
       
  Memory: 7.790031433105469 GB (5874.0625 MB free)
  Uptime: 984.0 sec
  Load Avg:  1.7255859375  1.60205078125  1.0966796875
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
    CPU MHz:               2800.162
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

