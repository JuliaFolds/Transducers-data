# Multi-thread benchmark result (via Travis)


# Judge result
# Benchmark Report for */home/travis/build/JuliaFolds/Transducers.jl*

## Job Properties
* Time of benchmarks:
    - Target: 9 Aug 2020 - 05:04
    - Baseline: 9 Aug 2020 - 05:08
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
| `["collect", "unordered", "basesize=1024"]`         |                1.17 (5%) :x: |                1.11 (1%) :x: |
| `["parallel_histogram", "comm", "basesize=16384"]`  | 0.93 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["parallel_histogram", "comm", "basesize=4096"]`   | 0.87 (5%) :white_check_mark: | 0.91 (1%) :white_check_mark: |
| `["parallel_histogram", "comm", "basesize=8192"]`   |                   1.00 (5%)  |                1.03 (1%) :x: |
| `["words", "nthreads=1"]`                           |                1.08 (5%) :x: |                   1.00 (1%)  |
| `["words", "nthreads=2"]`                           |                1.06 (5%) :x: |                   1.00 (1%)  |

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
       #1  2800 MHz      49870 s          0 s       2046 s      16337 s          0 s
       #2  2800 MHz      51153 s          0 s       2025 s      15841 s          0 s
       
  Memory: 7.790031433105469 GB (5790.01171875 MB free)
  Uptime: 699.0 sec
  Load Avg:  1.75634765625  1.56494140625  0.921875
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
       #1  2800 MHz      69110 s          0 s       2514 s      25523 s          0 s
       #2  2800 MHz      76810 s          0 s       2535 s      18471 s          0 s
       
  Memory: 7.790031433105469 GB (5814.921875 MB free)
  Uptime: 988.0 sec
  Load Avg:  1.740234375  1.6103515625  1.11181640625
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-8.0.1 (ORCJIT, skylake)
```

---
# Target result
# Benchmark Report for */home/travis/build/JuliaFolds/Transducers.jl*

## Job Properties
* Time of benchmark: 9 Aug 2020 - 5:4
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
| `["collect", "assoc", "basesize=1"]`                | 332.866 ms (5%) | 12.882 ms |  87.55 MiB (1%) |     1590750 |
| `["collect", "assoc", "basesize=1024"]`             | 180.139 ms (5%) |           |   1.84 MiB (1%) |        1807 |
| `["collect", "assoc", "basesize=32"]`               | 185.110 ms (5%) |           |   5.64 MiB (1%) |       54004 |
| `["collect", "seq"]`                                | 349.868 ms (5%) |           |   1.50 MiB (1%) |       32784 |
| `["collect", "unordered", "basesize=1"]`            | 378.981 ms (5%) |           |  29.17 MiB (1%) |      403866 |
| `["collect", "unordered", "basesize=1024"]`         | 241.718 ms (5%) |           | 941.80 KiB (1%) |       13367 |
| `["collect", "unordered", "basesize=32"]`           | 206.574 ms (5%) |           |   1.52 MiB (1%) |       19714 |
| `["findfirst", "n=1000", "foldl"]`                  | 550.852 ms (5%) |           |                 |             |
| `["findfirst", "n=1000", "reduce", "basesize=128"]` | 310.688 ms (5%) |           | 563.92 KiB (1%) |       10218 |
| `["findfirst", "n=1000", "reduce", "basesize=256"]` | 302.532 ms (5%) |           | 287.28 KiB (1%) |        5224 |
| `["findfirst", "n=1000", "reduce", "basesize=512"]` | 304.319 ms (5%) |           | 149.33 KiB (1%) |        2722 |
| `["findfirst", "n=400", "foldl"]`                   | 413.400 ms (5%) |           |                 |             |
| `["findfirst", "n=400", "reduce", "basesize=128"]`  | 250.273 ms (5%) |           |   1.02 MiB (1%) |       18951 |
| `["findfirst", "n=400", "reduce", "basesize=256"]`  | 235.680 ms (5%) |           | 526.34 KiB (1%) |        9582 |
| `["findfirst", "n=400", "reduce", "basesize=512"]`  | 230.959 ms (5%) |           | 267.20 KiB (1%) |        4874 |
| `["findfirst", "n=500", "foldl"]`                   |  71.636 ms (5%) |           |                 |             |
| `["findfirst", "n=500", "reduce", "basesize=128"]`  |  42.764 ms (5%) |           | 157.42 KiB (1%) |        2852 |
| `["findfirst", "n=500", "reduce", "basesize=256"]`  |  40.741 ms (5%) |           |  84.59 KiB (1%) |        1536 |
| `["findfirst", "n=500", "reduce", "basesize=512"]`  |  42.424 ms (5%) |           |  48.31 KiB (1%) |         879 |
| `["overhead", "default"]`                           | 223.591 μs (5%) |           | 146.27 KiB (1%) |        2633 |
| `["overhead", "stoppable=false"]`                   | 223.509 μs (5%) |           | 146.27 KiB (1%) |        2632 |
| `["overhead", "stoppable=true"]`                    | 421.464 μs (5%) |           | 146.58 KiB (1%) |        2652 |
| `["parallel_histogram", "assoc", "basesize=16384"]` |   4.899 ms (5%) |           | 732.06 KiB (1%) |         103 |
| `["parallel_histogram", "assoc", "basesize=4096"]`  |   5.831 ms (5%) |           |   1.80 MiB (1%) |         498 |
| `["parallel_histogram", "assoc", "basesize=8192"]`  |   5.339 ms (5%) |           |   1.43 MiB (1%) |         243 |
| `["parallel_histogram", "comm", "basesize=16384"]`  |  11.605 ms (5%) |           |   1.23 MiB (1%) |         582 |
| `["parallel_histogram", "comm", "basesize=4096"]`   |  16.470 ms (5%) |           |   1.05 MiB (1%) |        4964 |
| `["parallel_histogram", "comm", "basesize=8192"]`   |  15.400 ms (5%) |           |   1.27 MiB (1%) |        3416 |
| `["parallel_histogram", "seq"]`                     |   7.382 ms (5%) |           | 364.61 KiB (1%) |          24 |
| `["sum", "random", "foldl"]`                        |  14.142 ms (5%) |           |   64 bytes (1%) |           3 |
| `["sum", "random", "reduce", "basesize=128"]`       |   8.039 ms (5%) |           | 313.41 KiB (1%) |        6070 |
| `["sum", "random", "reduce", "basesize=256"]`       |   7.833 ms (5%) |           | 155.17 KiB (1%) |        3014 |
| `["sum", "random", "reduce", "basesize=512"]`       |   7.680 ms (5%) |           |  76.31 KiB (1%) |        1486 |
| `["sum", "uniform", "foldl"]`                       |  13.689 ms (5%) |           |   64 bytes (1%) |           3 |
| `["sum", "uniform", "reduce", "basesize=128"]`      |   7.814 ms (5%) |           | 313.44 KiB (1%) |        6072 |
| `["sum", "uniform", "reduce", "basesize=256"]`      |   7.569 ms (5%) |           | 155.14 KiB (1%) |        3012 |
| `["sum", "uniform", "reduce", "basesize=512"]`      |   7.448 ms (5%) |           |  76.31 KiB (1%) |        1486 |
| `["sum", "valley", "foldl"]`                        |  14.173 ms (5%) |           |   64 bytes (1%) |           3 |
| `["sum", "valley", "reduce", "basesize=128"]`       |   8.038 ms (5%) |           | 313.39 KiB (1%) |        6069 |
| `["sum", "valley", "reduce", "basesize=256"]`       |   7.814 ms (5%) |           | 155.16 KiB (1%) |        3013 |
| `["sum", "valley", "reduce", "basesize=512"]`       |   7.703 ms (5%) |           |  76.34 KiB (1%) |        1488 |
| `["words", "nthreads=1"]`                           |  37.745 ms (5%) |  7.924 ms |  63.22 MiB (1%) |     2065888 |
| `["words", "nthreads=2"]`                           |  31.527 ms (5%) |           |  63.83 MiB (1%) |     2074068 |
| `["words", "nthreads=4"]`                           |  31.438 ms (5%) |           |  64.79 MiB (1%) |     2082278 |

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
       #1  2800 MHz      49870 s          0 s       2046 s      16337 s          0 s
       #2  2800 MHz      51153 s          0 s       2025 s      15841 s          0 s
       
  Memory: 7.790031433105469 GB (5790.01171875 MB free)
  Uptime: 699.0 sec
  Load Avg:  1.75634765625  1.56494140625  0.921875
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-8.0.1 (ORCJIT, skylake)
```

---
# Baseline result
# Benchmark Report for */home/travis/build/JuliaFolds/Transducers.jl*

## Job Properties
* Time of benchmark: 9 Aug 2020 - 5:8
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

| ID                                                  | time            | GC time   | memory          | allocations |
|-----------------------------------------------------|----------------:|----------:|----------------:|------------:|
| `["collect", "assoc", "basesize=1"]`                | 326.334 ms (5%) | 12.430 ms |  87.55 MiB (1%) |     1590642 |
| `["collect", "assoc", "basesize=1024"]`             | 179.319 ms (5%) |           |   1.84 MiB (1%) |        1807 |
| `["collect", "assoc", "basesize=32"]`               | 184.055 ms (5%) |           |   5.64 MiB (1%) |       53999 |
| `["collect", "seq"]`                                | 349.814 ms (5%) |           |   1.50 MiB (1%) |       32784 |
| `["collect", "unordered", "basesize=1"]`            | 371.533 ms (5%) |           |  29.16 MiB (1%) |      403134 |
| `["collect", "unordered", "basesize=1024"]`         | 206.662 ms (5%) |           | 846.89 KiB (1%) |        6957 |
| `["collect", "unordered", "basesize=32"]`           | 205.874 ms (5%) |           |   1.53 MiB (1%) |       20452 |
| `["findfirst", "n=1000", "foldl"]`                  | 556.244 ms (5%) |           |                 |             |
| `["findfirst", "n=1000", "reduce", "basesize=128"]` | 314.742 ms (5%) |           | 563.94 KiB (1%) |       10219 |
| `["findfirst", "n=1000", "reduce", "basesize=256"]` | 306.811 ms (5%) |           | 287.28 KiB (1%) |        5224 |
| `["findfirst", "n=1000", "reduce", "basesize=512"]` | 308.523 ms (5%) |           | 149.23 KiB (1%) |        2716 |
| `["findfirst", "n=400", "foldl"]`                   | 417.576 ms (5%) |           |                 |             |
| `["findfirst", "n=400", "reduce", "basesize=128"]`  | 252.662 ms (5%) |           |   1.02 MiB (1%) |       18952 |
| `["findfirst", "n=400", "reduce", "basesize=256"]`  | 238.698 ms (5%) |           | 526.06 KiB (1%) |        9564 |
| `["findfirst", "n=400", "reduce", "basesize=512"]`  | 233.805 ms (5%) |           | 267.17 KiB (1%) |        4872 |
| `["findfirst", "n=500", "foldl"]`                   |  72.366 ms (5%) |           |                 |             |
| `["findfirst", "n=500", "reduce", "basesize=128"]`  |  43.298 ms (5%) |           | 157.39 KiB (1%) |        2850 |
| `["findfirst", "n=500", "reduce", "basesize=256"]`  |  41.293 ms (5%) |           |  84.58 KiB (1%) |        1535 |
| `["findfirst", "n=500", "reduce", "basesize=512"]`  |  42.995 ms (5%) |           |  48.31 KiB (1%) |         879 |
| `["overhead", "default"]`                           | 226.030 μs (5%) |           | 146.27 KiB (1%) |        2633 |
| `["overhead", "stoppable=false"]`                   | 225.442 μs (5%) |           | 146.30 KiB (1%) |        2634 |
| `["overhead", "stoppable=true"]`                    | 430.676 μs (5%) |           | 146.58 KiB (1%) |        2652 |
| `["parallel_histogram", "assoc", "basesize=16384"]` |   4.881 ms (5%) |           | 732.06 KiB (1%) |         103 |
| `["parallel_histogram", "assoc", "basesize=4096"]`  |   5.747 ms (5%) |           |   1.80 MiB (1%) |         498 |
| `["parallel_histogram", "assoc", "basesize=8192"]`  |   5.322 ms (5%) |           |   1.43 MiB (1%) |         243 |
| `["parallel_histogram", "comm", "basesize=16384"]`  |  12.533 ms (5%) |           |   1.23 MiB (1%) |         687 |
| `["parallel_histogram", "comm", "basesize=4096"]`   |  19.035 ms (5%) |           |   1.16 MiB (1%) |        9508 |
| `["parallel_histogram", "comm", "basesize=8192"]`   |  15.391 ms (5%) |           |   1.23 MiB (1%) |         796 |
| `["parallel_histogram", "seq"]`                     |   7.449 ms (5%) |           | 364.61 KiB (1%) |          24 |
| `["sum", "random", "foldl"]`                        |  14.075 ms (5%) |           |   64 bytes (1%) |           3 |
| `["sum", "random", "reduce", "basesize=128"]`       |   7.997 ms (5%) |           | 313.44 KiB (1%) |        6072 |
| `["sum", "random", "reduce", "basesize=256"]`       |   7.785 ms (5%) |           | 155.19 KiB (1%) |        3015 |
| `["sum", "random", "reduce", "basesize=512"]`       |   7.621 ms (5%) |           |  76.38 KiB (1%) |        1490 |
| `["sum", "uniform", "foldl"]`                       |  13.688 ms (5%) |           |   64 bytes (1%) |           3 |
| `["sum", "uniform", "reduce", "basesize=128"]`      |   7.812 ms (5%) |           | 313.42 KiB (1%) |        6071 |
| `["sum", "uniform", "reduce", "basesize=256"]`      |   7.568 ms (5%) |           | 155.14 KiB (1%) |        3012 |
| `["sum", "uniform", "reduce", "basesize=512"]`      |   7.447 ms (5%) |           |  76.31 KiB (1%) |        1486 |
| `["sum", "valley", "foldl"]`                        |  14.184 ms (5%) |           |   64 bytes (1%) |           3 |
| `["sum", "valley", "reduce", "basesize=128"]`       |   8.071 ms (5%) |           | 313.38 KiB (1%) |        6068 |
| `["sum", "valley", "reduce", "basesize=256"]`       |   7.832 ms (5%) |           | 155.16 KiB (1%) |        3013 |
| `["sum", "valley", "reduce", "basesize=512"]`       |   7.704 ms (5%) |           |  76.34 KiB (1%) |        1488 |
| `["words", "nthreads=1"]`                           |  34.873 ms (5%) |  6.933 ms |  63.16 MiB (1%) |     2063546 |
| `["words", "nthreads=2"]`                           |  29.865 ms (5%) |           |  63.77 MiB (1%) |     2071663 |
| `["words", "nthreads=4"]`                           |  30.653 ms (5%) |           |  64.73 MiB (1%) |     2079885 |

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
       #1  2800 MHz      69110 s          0 s       2514 s      25523 s          0 s
       #2  2800 MHz      76810 s          0 s       2535 s      18471 s          0 s
       
  Memory: 7.790031433105469 GB (5814.921875 MB free)
  Uptime: 988.0 sec
  Load Avg:  1.740234375  1.6103515625  1.11181640625
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
    CPU MHz:               2800.256
    BogoMIPS:              5600.51
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

