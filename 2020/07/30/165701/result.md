# Multi-thread benchmark result (via Travis)


# Judge result
# Benchmark Report for */home/travis/build/JuliaFolds/Transducers.jl*

## Job Properties
* Time of benchmarks:
    - Target: 30 Jul 2020 - 16:51
    - Baseline: 30 Jul 2020 - 16:56
* Package commits:
    - Target: 20e12e
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

| ID                                                  | time ratio                   | memory ratio  |
|-----------------------------------------------------|------------------------------|---------------|
| `["collect", "unordered", "basesize=1024"]`         |                1.05 (5%) :x: | 1.02 (1%) :x: |
| `["parallel_histogram", "comm", "basesize=16384"]`  | 0.94 (5%) :white_check_mark: |    0.99 (1%)  |
| `["parallel_histogram", "comm", "basesize=4096"]`   |                1.05 (5%) :x: | 1.03 (1%) :x: |

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
       #1  2800 MHz      50549 s          0 s       1958 s      13269 s          0 s
       #2  2800 MHz      48259 s          0 s       2028 s      16704 s          0 s
       
  Memory: 7.790031433105469 GB (5854.8671875 MB free)
  Uptime: 676.0 sec
  Load Avg:  1.673828125  1.42431640625  0.81005859375
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
       #1  2800 MHz      74210 s          0 s       2574 s      22264 s          0 s
       #2  2800 MHz      73864 s          0 s       2800 s      23507 s          0 s
       
  Memory: 7.790031433105469 GB (5829.9921875 MB free)
  Uptime: 1010.0 sec
  Load Avg:  1.77294921875  1.56103515625  1.04736328125
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-8.0.1 (ORCJIT, skylake)
```

---
# Target result
# Benchmark Report for */home/travis/build/JuliaFolds/Transducers.jl*

## Job Properties
* Time of benchmark: 30 Jul 2020 - 16:51
* Package commit: 20e12e
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
| `["collect", "assoc", "basesize=1"]`                | 328.102 ms (5%) | 12.315 ms |  87.55 MiB (1%) |     1590737 |
| `["collect", "assoc", "basesize=1024"]`             | 179.846 ms (5%) |           |   1.84 MiB (1%) |        1807 |
| `["collect", "assoc", "basesize=32"]`               | 184.469 ms (5%) |           |   5.64 MiB (1%) |       54018 |
| `["collect", "seq"]`                                | 350.298 ms (5%) |           |   1.50 MiB (1%) |       32784 |
| `["collect", "unordered", "basesize=1"]`            | 370.665 ms (5%) |           |  29.16 MiB (1%) |      403439 |
| `["collect", "unordered", "basesize=1024"]`         | 259.850 ms (5%) |           | 976.03 KiB (1%) |       15558 |
| `["collect", "unordered", "basesize=32"]`           | 207.680 ms (5%) |           |   1.50 MiB (1%) |       19005 |
| `["findfirst", "n=1000", "foldl"]`                  | 551.997 ms (5%) |           |                 |             |
| `["findfirst", "n=1000", "reduce", "basesize=128"]` | 310.652 ms (5%) |           | 563.72 KiB (1%) |       10209 |
| `["findfirst", "n=1000", "reduce", "basesize=256"]` | 302.893 ms (5%) |           | 287.08 KiB (1%) |        5215 |
| `["findfirst", "n=1000", "reduce", "basesize=512"]` | 304.498 ms (5%) |           | 149.13 KiB (1%) |        2713 |
| `["findfirst", "n=400", "foldl"]`                   | 414.404 ms (5%) |           |                 |             |
| `["findfirst", "n=400", "reduce", "basesize=128"]`  | 250.284 ms (5%) |           |   1.02 MiB (1%) |       18955 |
| `["findfirst", "n=400", "reduce", "basesize=256"]`  | 235.934 ms (5%) |           | 525.95 KiB (1%) |        9561 |
| `["findfirst", "n=400", "reduce", "basesize=512"]`  | 230.775 ms (5%) |           | 267.03 KiB (1%) |        4867 |
| `["findfirst", "n=500", "foldl"]`                   |  71.796 ms (5%) |           |                 |             |
| `["findfirst", "n=500", "reduce", "basesize=128"]`  |  42.807 ms (5%) |           | 157.25 KiB (1%) |        2845 |
| `["findfirst", "n=500", "reduce", "basesize=256"]`  |  40.786 ms (5%) |           |  84.42 KiB (1%) |        1529 |
| `["findfirst", "n=500", "reduce", "basesize=512"]`  |  42.427 ms (5%) |           |  48.17 KiB (1%) |         874 |
| `["overhead", "default"]`                           | 225.683 μs (5%) |           | 146.16 KiB (1%) |        2629 |
| `["overhead", "stoppable=false"]`                   | 223.168 μs (5%) |           | 146.16 KiB (1%) |        2629 |
| `["overhead", "stoppable=true"]`                    | 429.739 μs (5%) |           | 146.45 KiB (1%) |        2648 |
| `["parallel_histogram", "assoc", "basesize=16384"]` |   4.955 ms (5%) |           | 732.02 KiB (1%) |         101 |
| `["parallel_histogram", "assoc", "basesize=4096"]`  |   5.845 ms (5%) |           |   1.80 MiB (1%) |         495 |
| `["parallel_histogram", "assoc", "basesize=8192"]`  |   5.438 ms (5%) |           |   1.43 MiB (1%) |         241 |
| `["parallel_histogram", "comm", "basesize=16384"]`  |  12.530 ms (5%) |           |   1.22 MiB (1%) |         159 |
| `["parallel_histogram", "comm", "basesize=4096"]`   |  19.007 ms (5%) |           |   1.10 MiB (1%) |        8565 |
| `["parallel_histogram", "comm", "basesize=8192"]`   |  15.804 ms (5%) |           |   1.27 MiB (1%) |        3240 |
| `["parallel_histogram", "seq"]`                     |   7.378 ms (5%) |           | 364.61 KiB (1%) |          24 |
| `["sum", "random", "foldl"]`                        |  14.171 ms (5%) |           |   64 bytes (1%) |           3 |
| `["sum", "random", "reduce", "basesize=128"]`       |   8.081 ms (5%) |           | 313.34 KiB (1%) |        6068 |
| `["sum", "random", "reduce", "basesize=256"]`       |   7.835 ms (5%) |           | 155.08 KiB (1%) |        3010 |
| `["sum", "random", "reduce", "basesize=512"]`       |   7.710 ms (5%) |           |  76.25 KiB (1%) |        1484 |
| `["sum", "uniform", "foldl"]`                       |  13.668 ms (5%) |           |   64 bytes (1%) |           3 |
| `["sum", "uniform", "reduce", "basesize=128"]`      |   7.810 ms (5%) |           | 313.30 KiB (1%) |        6065 |
| `["sum", "uniform", "reduce", "basesize=256"]`      |   7.574 ms (5%) |           | 155.13 KiB (1%) |        3013 |
| `["sum", "uniform", "reduce", "basesize=512"]`      |   7.443 ms (5%) |           |  76.25 KiB (1%) |        1484 |
| `["sum", "valley", "foldl"]`                        |  14.162 ms (5%) |           |   64 bytes (1%) |           3 |
| `["sum", "valley", "reduce", "basesize=128"]`       |   8.065 ms (5%) |           | 313.23 KiB (1%) |        6061 |
| `["sum", "valley", "reduce", "basesize=256"]`       |   7.834 ms (5%) |           | 155.09 KiB (1%) |        3011 |
| `["sum", "valley", "reduce", "basesize=512"]`       |   7.706 ms (5%) |           |  76.28 KiB (1%) |        1486 |
| `["words", "nthreads=1"]`                           |  45.782 ms (5%) |  7.375 ms |  63.15 MiB (1%) |     2062645 |
| `["words", "nthreads=2"]`                           |  40.764 ms (5%) |           |  64.23 MiB (1%) |     2074853 |
| `["words", "nthreads=4"]`                           |  41.713 ms (5%) |           |  64.87 MiB (1%) |     2081048 |

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
       #1  2800 MHz      50549 s          0 s       1958 s      13269 s          0 s
       #2  2800 MHz      48259 s          0 s       2028 s      16704 s          0 s
       
  Memory: 7.790031433105469 GB (5854.8671875 MB free)
  Uptime: 676.0 sec
  Load Avg:  1.673828125  1.42431640625  0.81005859375
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-8.0.1 (ORCJIT, skylake)
```

---
# Baseline result
# Benchmark Report for */home/travis/build/JuliaFolds/Transducers.jl*

## Job Properties
* Time of benchmark: 30 Jul 2020 - 16:56
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
| `["collect", "assoc", "basesize=1"]`                | 328.390 ms (5%) | 13.504 ms |  87.55 MiB (1%) |     1590680 |
| `["collect", "assoc", "basesize=1024"]`             | 179.917 ms (5%) |           |   1.84 MiB (1%) |        1808 |
| `["collect", "assoc", "basesize=32"]`               | 184.677 ms (5%) |           |   5.64 MiB (1%) |       54004 |
| `["collect", "seq"]`                                | 350.021 ms (5%) |           |   1.50 MiB (1%) |       32784 |
| `["collect", "unordered", "basesize=1"]`            | 373.197 ms (5%) |           |  29.16 MiB (1%) |      403304 |
| `["collect", "unordered", "basesize=1024"]`         | 246.506 ms (5%) |           | 960.81 KiB (1%) |       14584 |
| `["collect", "unordered", "basesize=32"]`           | 206.616 ms (5%) |           |   1.51 MiB (1%) |       19423 |
| `["findfirst", "n=1000", "foldl"]`                  | 551.237 ms (5%) |           |                 |             |
| `["findfirst", "n=1000", "reduce", "basesize=128"]` | 311.396 ms (5%) |           | 563.80 KiB (1%) |       10214 |
| `["findfirst", "n=1000", "reduce", "basesize=256"]` | 303.375 ms (5%) |           | 287.03 KiB (1%) |        5212 |
| `["findfirst", "n=1000", "reduce", "basesize=512"]` | 304.832 ms (5%) |           | 149.23 KiB (1%) |        2720 |
| `["findfirst", "n=400", "foldl"]`                   | 413.838 ms (5%) |           |                 |             |
| `["findfirst", "n=400", "reduce", "basesize=128"]`  | 250.308 ms (5%) |           |   1.02 MiB (1%) |       18943 |
| `["findfirst", "n=400", "reduce", "basesize=256"]`  | 235.988 ms (5%) |           | 525.94 KiB (1%) |        9560 |
| `["findfirst", "n=400", "reduce", "basesize=512"]`  | 231.070 ms (5%) |           | 267.03 KiB (1%) |        4867 |
| `["findfirst", "n=500", "foldl"]`                   |  71.880 ms (5%) |           |                 |             |
| `["findfirst", "n=500", "reduce", "basesize=128"]`  |  42.836 ms (5%) |           | 157.27 KiB (1%) |        2846 |
| `["findfirst", "n=500", "reduce", "basesize=256"]`  |  40.818 ms (5%) |           |  84.44 KiB (1%) |        1530 |
| `["findfirst", "n=500", "reduce", "basesize=512"]`  |  42.514 ms (5%) |           |  48.17 KiB (1%) |         874 |
| `["overhead", "default"]`                           | 223.610 μs (5%) |           | 146.16 KiB (1%) |        2629 |
| `["overhead", "stoppable=false"]`                   | 223.905 μs (5%) |           | 146.16 KiB (1%) |        2629 |
| `["overhead", "stoppable=true"]`                    | 421.634 μs (5%) |           | 146.44 KiB (1%) |        2647 |
| `["parallel_histogram", "assoc", "basesize=16384"]` |   4.942 ms (5%) |           | 732.02 KiB (1%) |         101 |
| `["parallel_histogram", "assoc", "basesize=4096"]`  |   5.793 ms (5%) |           |   1.80 MiB (1%) |         495 |
| `["parallel_histogram", "assoc", "basesize=8192"]`  |   5.414 ms (5%) |           |   1.43 MiB (1%) |         241 |
| `["parallel_histogram", "comm", "basesize=16384"]`  |  13.266 ms (5%) |           |   1.23 MiB (1%) |         715 |
| `["parallel_histogram", "comm", "basesize=4096"]`   |  18.028 ms (5%) |           |   1.07 MiB (1%) |        6089 |
| `["parallel_histogram", "comm", "basesize=8192"]`   |  15.443 ms (5%) |           |   1.27 MiB (1%) |        3264 |
| `["parallel_histogram", "seq"]`                     |   7.396 ms (5%) |           | 364.61 KiB (1%) |          24 |
| `["sum", "random", "foldl"]`                        |  14.134 ms (5%) |           |   64 bytes (1%) |           3 |
| `["sum", "random", "reduce", "basesize=128"]`       |   8.060 ms (5%) |           | 313.34 KiB (1%) |        6068 |
| `["sum", "random", "reduce", "basesize=256"]`       |   7.798 ms (5%) |           | 155.08 KiB (1%) |        3010 |
| `["sum", "random", "reduce", "basesize=512"]`       |   7.688 ms (5%) |           |  76.25 KiB (1%) |        1484 |
| `["sum", "uniform", "foldl"]`                       |  13.669 ms (5%) |           |   64 bytes (1%) |           3 |
| `["sum", "uniform", "reduce", "basesize=128"]`      |   7.811 ms (5%) |           | 313.31 KiB (1%) |        6066 |
| `["sum", "uniform", "reduce", "basesize=256"]`      |   7.555 ms (5%) |           | 155.08 KiB (1%) |        3010 |
| `["sum", "uniform", "reduce", "basesize=512"]`      |   7.451 ms (5%) |           |  76.25 KiB (1%) |        1484 |
| `["sum", "valley", "foldl"]`                        |  14.156 ms (5%) |           |   64 bytes (1%) |           3 |
| `["sum", "valley", "reduce", "basesize=128"]`       |   8.069 ms (5%) |           | 313.28 KiB (1%) |        6064 |
| `["sum", "valley", "reduce", "basesize=256"]`       |   7.841 ms (5%) |           | 155.11 KiB (1%) |        3012 |
| `["sum", "valley", "reduce", "basesize=512"]`       |   7.693 ms (5%) |           |  76.27 KiB (1%) |        1485 |
| `["words", "nthreads=1"]`                           |  45.731 ms (5%) |  7.510 ms |  63.06 MiB (1%) |     2060622 |
| `["words", "nthreads=2"]`                           |  40.414 ms (5%) |           |  63.66 MiB (1%) |     2068744 |
| `["words", "nthreads=4"]`                           |  42.465 ms (5%) |           |  64.94 MiB (1%) |     2081196 |

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
       #1  2800 MHz      74210 s          0 s       2574 s      22264 s          0 s
       #2  2800 MHz      73864 s          0 s       2800 s      23507 s          0 s
       
  Memory: 7.790031433105469 GB (5829.9921875 MB free)
  Uptime: 1010.0 sec
  Load Avg:  1.77294921875  1.56103515625  1.04736328125
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

