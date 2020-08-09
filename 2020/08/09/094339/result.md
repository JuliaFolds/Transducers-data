# Multi-thread benchmark result (via Travis)


# Judge result
# Benchmark Report for */home/travis/build/JuliaFolds/Transducers.jl*

## Job Properties
* Time of benchmarks:
    - Target: 9 Aug 2020 - 09:38
    - Baseline: 9 Aug 2020 - 09:43
* Package commits:
    - Target: e0cc36
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
| `["collect", "unordered", "basesize=1024"]`         |                1.13 (5%) :x: |                1.11 (1%) :x: |
| `["parallel_histogram", "comm", "basesize=16384"]`  | 0.90 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["parallel_histogram", "comm", "basesize=4096"]`   | 0.94 (5%) :white_check_mark: | 0.98 (1%) :white_check_mark: |
| `["parallel_histogram", "comm", "basesize=8192"]`   | 0.90 (5%) :white_check_mark: | 0.99 (1%) :white_check_mark: |
| `["words", "nthreads=1"]`                           |                1.18 (5%) :x: |                   1.00 (1%)  |
| `["words", "nthreads=2"]`                           |                1.09 (5%) :x: |                   1.00 (1%)  |
| `["words", "nthreads=4"]`                           |                1.08 (5%) :x: |                   1.01 (1%)  |

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
       #1  2800 MHz      43888 s          0 s       1845 s      22060 s          0 s
       #2  2800 MHz      56167 s          0 s       2009 s       9908 s          0 s
       
  Memory: 7.790031433105469 GB (5803.02734375 MB free)
  Uptime: 687.0 sec
  Load Avg:  1.83251953125  1.53955078125  0.88134765625
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
       #1  2800 MHz      66851 s          0 s       2272 s      28213 s          0 s
       #2  2800 MHz      78640 s          0 s       2635 s      16198 s          0 s
       
  Memory: 7.790031433105469 GB (5816.08203125 MB free)
  Uptime: 983.0 sec
  Load Avg:  1.71923828125  1.59423828125  1.0849609375
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-8.0.1 (ORCJIT, skylake)
```

---
# Target result
# Benchmark Report for */home/travis/build/JuliaFolds/Transducers.jl*

## Job Properties
* Time of benchmark: 9 Aug 2020 - 9:38
* Package commit: e0cc36
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
| `["collect", "assoc", "basesize=1"]`                | 325.585 ms (5%) | 12.476 ms |  87.55 MiB (1%) |     1590680 |
| `["collect", "assoc", "basesize=1024"]`             | 179.655 ms (5%) |           |   1.84 MiB (1%) |        1807 |
| `["collect", "assoc", "basesize=32"]`               | 184.596 ms (5%) |           |   5.64 MiB (1%) |       54007 |
| `["collect", "seq"]`                                | 349.737 ms (5%) |           |   1.50 MiB (1%) |       32784 |
| `["collect", "unordered", "basesize=1"]`            | 375.716 ms (5%) |           |  29.16 MiB (1%) |      403271 |
| `["collect", "unordered", "basesize=1024"]`         | 256.725 ms (5%) |           | 996.28 KiB (1%) |       16854 |
| `["collect", "unordered", "basesize=32"]`           | 205.389 ms (5%) |           |   1.50 MiB (1%) |       18648 |
| `["findfirst", "n=1000", "foldl"]`                  | 550.373 ms (5%) |           |                 |             |
| `["findfirst", "n=1000", "reduce", "basesize=128"]` | 310.260 ms (5%) |           | 563.97 KiB (1%) |       10221 |
| `["findfirst", "n=1000", "reduce", "basesize=256"]` | 302.492 ms (5%) |           | 287.20 KiB (1%) |        5219 |
| `["findfirst", "n=1000", "reduce", "basesize=512"]` | 303.871 ms (5%) |           | 149.33 KiB (1%) |        2722 |
| `["findfirst", "n=400", "foldl"]`                   | 413.111 ms (5%) |           |                 |             |
| `["findfirst", "n=400", "reduce", "basesize=128"]`  | 250.072 ms (5%) |           |   1.02 MiB (1%) |       18953 |
| `["findfirst", "n=400", "reduce", "basesize=256"]`  | 235.454 ms (5%) |           | 526.13 KiB (1%) |        9568 |
| `["findfirst", "n=400", "reduce", "basesize=512"]`  | 229.824 ms (5%) |           | 267.23 KiB (1%) |        4876 |
| `["findfirst", "n=500", "foldl"]`                   |  71.577 ms (5%) |           |                 |             |
| `["findfirst", "n=500", "reduce", "basesize=128"]`  |  42.718 ms (5%) |           | 157.41 KiB (1%) |        2851 |
| `["findfirst", "n=500", "reduce", "basesize=256"]`  |  40.733 ms (5%) |           |  84.59 KiB (1%) |        1536 |
| `["findfirst", "n=500", "reduce", "basesize=512"]`  |  42.367 ms (5%) |           |  48.31 KiB (1%) |         879 |
| `["overhead", "default"]`                           | 222.435 μs (5%) |           | 146.25 KiB (1%) |        2632 |
| `["overhead", "stoppable=false"]`                   | 223.257 μs (5%) |           | 146.28 KiB (1%) |        2633 |
| `["overhead", "stoppable=true"]`                    | 423.630 μs (5%) |           | 146.56 KiB (1%) |        2651 |
| `["parallel_histogram", "assoc", "basesize=16384"]` |   4.945 ms (5%) |           | 732.06 KiB (1%) |         103 |
| `["parallel_histogram", "assoc", "basesize=4096"]`  |   5.813 ms (5%) |           |   1.80 MiB (1%) |         497 |
| `["parallel_histogram", "assoc", "basesize=8192"]`  |   5.412 ms (5%) |           |   1.43 MiB (1%) |         242 |
| `["parallel_histogram", "comm", "basesize=16384"]`  |  11.947 ms (5%) |           |   1.22 MiB (1%) |         424 |
| `["parallel_histogram", "comm", "basesize=4096"]`   |  15.945 ms (5%) |           |   1.03 MiB (1%) |        3850 |
| `["parallel_histogram", "comm", "basesize=8192"]`   |  14.480 ms (5%) |           |   1.26 MiB (1%) |        2998 |
| `["parallel_histogram", "seq"]`                     |   7.291 ms (5%) |           | 364.61 KiB (1%) |          24 |
| `["sum", "random", "foldl"]`                        |  14.235 ms (5%) |           |   64 bytes (1%) |           3 |
| `["sum", "random", "reduce", "basesize=128"]`       |   8.102 ms (5%) |           | 313.44 KiB (1%) |        6072 |
| `["sum", "random", "reduce", "basesize=256"]`       |   7.853 ms (5%) |           | 155.14 KiB (1%) |        3012 |
| `["sum", "random", "reduce", "basesize=512"]`       |   7.747 ms (5%) |           |  76.36 KiB (1%) |        1489 |
| `["sum", "uniform", "foldl"]`                       |  13.672 ms (5%) |           |   64 bytes (1%) |           3 |
| `["sum", "uniform", "reduce", "basesize=128"]`      |   7.803 ms (5%) |           | 313.45 KiB (1%) |        6073 |
| `["sum", "uniform", "reduce", "basesize=256"]`      |   7.559 ms (5%) |           | 155.14 KiB (1%) |        3012 |
| `["sum", "uniform", "reduce", "basesize=512"]`      |   7.445 ms (5%) |           |  76.31 KiB (1%) |        1486 |
| `["sum", "valley", "foldl"]`                        |  14.135 ms (5%) |           |   64 bytes (1%) |           3 |
| `["sum", "valley", "reduce", "basesize=128"]`       |   8.040 ms (5%) |           | 313.28 KiB (1%) |        6062 |
| `["sum", "valley", "reduce", "basesize=256"]`       |   7.817 ms (5%) |           | 155.17 KiB (1%) |        3014 |
| `["sum", "valley", "reduce", "basesize=512"]`       |   7.690 ms (5%) |           |  76.34 KiB (1%) |        1488 |
| `["words", "nthreads=1"]`                           |  36.656 ms (5%) |  7.701 ms |  63.52 MiB (1%) |     2075527 |
| `["words", "nthreads=2"]`                           |  31.378 ms (5%) |           |  64.61 MiB (1%) |     2087786 |
| `["words", "nthreads=4"]`                           |  32.456 ms (5%) |           |  65.56 MiB (1%) |     2098241 |

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
       #1  2800 MHz      43888 s          0 s       1845 s      22060 s          0 s
       #2  2800 MHz      56167 s          0 s       2009 s       9908 s          0 s
       
  Memory: 7.790031433105469 GB (5803.02734375 MB free)
  Uptime: 687.0 sec
  Load Avg:  1.83251953125  1.53955078125  0.88134765625
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-8.0.1 (ORCJIT, skylake)
```

---
# Baseline result
# Benchmark Report for */home/travis/build/JuliaFolds/Transducers.jl*

## Job Properties
* Time of benchmark: 9 Aug 2020 - 9:43
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
| `["collect", "assoc", "basesize=1"]`                | 319.534 ms (5%) | 10.735 ms |  87.55 MiB (1%) |     1590632 |
| `["collect", "assoc", "basesize=1024"]`             | 179.070 ms (5%) |           |   1.84 MiB (1%) |        1807 |
| `["collect", "assoc", "basesize=32"]`               | 184.039 ms (5%) |           |   5.64 MiB (1%) |       54017 |
| `["collect", "seq"]`                                | 349.728 ms (5%) |           |   1.50 MiB (1%) |       32784 |
| `["collect", "unordered", "basesize=1"]`            | 378.052 ms (5%) |           |  29.16 MiB (1%) |      403126 |
| `["collect", "unordered", "basesize=1024"]`         | 227.592 ms (5%) |           | 895.28 KiB (1%) |       10390 |
| `["collect", "unordered", "basesize=32"]`           | 207.537 ms (5%) |           |   1.51 MiB (1%) |       19112 |
| `["findfirst", "n=1000", "foldl"]`                  | 550.301 ms (5%) |           |                 |             |
| `["findfirst", "n=1000", "reduce", "basesize=128"]` | 311.438 ms (5%) |           | 563.88 KiB (1%) |       10215 |
| `["findfirst", "n=1000", "reduce", "basesize=256"]` | 303.385 ms (5%) |           | 287.17 KiB (1%) |        5217 |
| `["findfirst", "n=1000", "reduce", "basesize=512"]` | 305.129 ms (5%) |           | 149.31 KiB (1%) |        2721 |
| `["findfirst", "n=400", "foldl"]`                   | 413.131 ms (5%) |           |                 |             |
| `["findfirst", "n=400", "reduce", "basesize=128"]`  | 250.720 ms (5%) |           |   1.02 MiB (1%) |       18955 |
| `["findfirst", "n=400", "reduce", "basesize=256"]`  | 236.324 ms (5%) |           | 526.05 KiB (1%) |        9563 |
| `["findfirst", "n=400", "reduce", "basesize=512"]`  | 231.220 ms (5%) |           | 267.19 KiB (1%) |        4873 |
| `["findfirst", "n=500", "foldl"]`                   |  71.579 ms (5%) |           |                 |             |
| `["findfirst", "n=500", "reduce", "basesize=128"]`  |  42.865 ms (5%) |           | 157.41 KiB (1%) |        2851 |
| `["findfirst", "n=500", "reduce", "basesize=256"]`  |  40.888 ms (5%) |           |  84.58 KiB (1%) |        1535 |
| `["findfirst", "n=500", "reduce", "basesize=512"]`  |  42.521 ms (5%) |           |  48.30 KiB (1%) |         878 |
| `["overhead", "default"]`                           | 222.761 μs (5%) |           | 146.28 KiB (1%) |        2634 |
| `["overhead", "stoppable=false"]`                   | 222.012 μs (5%) |           | 146.30 KiB (1%) |        2634 |
| `["overhead", "stoppable=true"]`                    | 414.333 μs (5%) |           | 146.56 KiB (1%) |        2651 |
| `["parallel_histogram", "assoc", "basesize=16384"]` |   4.846 ms (5%) |           | 732.06 KiB (1%) |         103 |
| `["parallel_histogram", "assoc", "basesize=4096"]`  |   5.699 ms (5%) |           |   1.80 MiB (1%) |         497 |
| `["parallel_histogram", "assoc", "basesize=8192"]`  |   5.268 ms (5%) |           |   1.43 MiB (1%) |         243 |
| `["parallel_histogram", "comm", "basesize=16384"]`  |  13.347 ms (5%) |           |   1.23 MiB (1%) |         792 |
| `["parallel_histogram", "comm", "basesize=4096"]`   |  16.891 ms (5%) |           |   1.05 MiB (1%) |        5311 |
| `["parallel_histogram", "comm", "basesize=8192"]`   |  16.037 ms (5%) |           |   1.28 MiB (1%) |        4243 |
| `["parallel_histogram", "seq"]`                     |   7.286 ms (5%) |           | 364.61 KiB (1%) |          24 |
| `["sum", "random", "foldl"]`                        |  14.096 ms (5%) |           |   64 bytes (1%) |           3 |
| `["sum", "random", "reduce", "basesize=128"]`       |   8.047 ms (5%) |           | 313.45 KiB (1%) |        6073 |
| `["sum", "random", "reduce", "basesize=256"]`       |   7.804 ms (5%) |           | 155.16 KiB (1%) |        3013 |
| `["sum", "random", "reduce", "basesize=512"]`       |   7.665 ms (5%) |           |  76.34 KiB (1%) |        1488 |
| `["sum", "uniform", "foldl"]`                       |  13.651 ms (5%) |           |   64 bytes (1%) |           3 |
| `["sum", "uniform", "reduce", "basesize=128"]`      |   7.814 ms (5%) |           | 313.44 KiB (1%) |        6072 |
| `["sum", "uniform", "reduce", "basesize=256"]`      |   7.551 ms (5%) |           | 155.14 KiB (1%) |        3012 |
| `["sum", "uniform", "reduce", "basesize=512"]`      |   7.446 ms (5%) |           |  76.31 KiB (1%) |        1486 |
| `["sum", "valley", "foldl"]`                        |  14.141 ms (5%) |           |   64 bytes (1%) |           3 |
| `["sum", "valley", "reduce", "basesize=128"]`       |   8.052 ms (5%) |           | 313.39 KiB (1%) |        6069 |
| `["sum", "valley", "reduce", "basesize=256"]`       |   7.825 ms (5%) |           | 155.17 KiB (1%) |        3014 |
| `["sum", "valley", "reduce", "basesize=512"]`       |   7.692 ms (5%) |           |  76.34 KiB (1%) |        1488 |
| `["words", "nthreads=1"]`                           |  31.033 ms (5%) |  6.239 ms |  63.22 MiB (1%) |     2066149 |
| `["words", "nthreads=2"]`                           |  28.822 ms (5%) |           |  64.31 MiB (1%) |     2078337 |
| `["words", "nthreads=4"]`                           |  30.061 ms (5%) |           |  64.95 MiB (1%) |     2084622 |

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
       #1  2800 MHz      66851 s          0 s       2272 s      28213 s          0 s
       #2  2800 MHz      78640 s          0 s       2635 s      16198 s          0 s
       
  Memory: 7.790031433105469 GB (5816.08203125 MB free)
  Uptime: 983.0 sec
  Load Avg:  1.71923828125  1.59423828125  1.0849609375
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
    CPU MHz:               2800.192
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

