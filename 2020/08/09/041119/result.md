# Multi-thread benchmark result (via Travis)


# Judge result
# Benchmark Report for */home/travis/build/JuliaFolds/Transducers.jl*

## Job Properties
* Time of benchmarks:
    - Target: 9 Aug 2020 - 04:06
    - Baseline: 9 Aug 2020 - 04:10
* Package commits:
    - Target: a8816d
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
| `["collect", "unordered", "basesize=1024"]`         |                   1.02 (5%)  | 0.98 (1%) :white_check_mark: |
| `["overhead", "stoppable=true"]`                    |                1.47 (5%) :x: |                   1.00 (1%)  |
| `["parallel_histogram", "comm", "basesize=4096"]`   | 0.85 (5%) :white_check_mark: | 0.94 (1%) :white_check_mark: |
| `["words", "nthreads=2"]`                           |                   1.01 (5%)  | 0.98 (1%) :white_check_mark: |

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
       #1  2800 MHz      51402 s          0 s       2194 s      13573 s          0 s
       #2  2800 MHz      49340 s          0 s       1725 s      17556 s          0 s
       
  Memory: 7.7900238037109375 GB (5834.6484375 MB free)
  Uptime: 692.0 sec
  Load Avg:  1.7158203125  1.5322265625  0.88134765625
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
       #1  2800 MHz      70682 s          0 s       2602 s      22448 s          0 s
       #2  2800 MHz      74766 s          0 s       2316 s      20246 s          0 s
       
  Memory: 7.7900238037109375 GB (5858.37109375 MB free)
  Uptime: 979.0 sec
  Load Avg:  1.73974609375  1.6298828125  1.09912109375
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-8.0.1 (ORCJIT, skylake)
```

---
# Target result
# Benchmark Report for */home/travis/build/JuliaFolds/Transducers.jl*

## Job Properties
* Time of benchmark: 9 Aug 2020 - 4:6
* Package commit: a8816d
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
| `["collect", "assoc", "basesize=1"]`                | 325.183 ms (5%) | 12.977 ms |   87.55 MiB (1%) |     1590726 |
| `["collect", "assoc", "basesize=1024"]`             | 179.754 ms (5%) |           |    1.84 MiB (1%) |        1812 |
| `["collect", "assoc", "basesize=32"]`               | 184.944 ms (5%) |           |    5.64 MiB (1%) |       54021 |
| `["collect", "seq"]`                                | 350.398 ms (5%) |           |    1.50 MiB (1%) |       32784 |
| `["collect", "unordered", "basesize=1"]`            | 377.454 ms (5%) |           |   29.16 MiB (1%) |      403258 |
| `["collect", "unordered", "basesize=1024"]`         | 267.541 ms (5%) |           | 1002.80 KiB (1%) |       17271 |
| `["collect", "unordered", "basesize=32"]`           | 206.022 ms (5%) |           |    1.52 MiB (1%) |       19729 |
| `["findfirst", "n=1000", "foldl"]`                  | 551.453 ms (5%) |           |                  |             |
| `["findfirst", "n=1000", "reduce", "basesize=128"]` | 309.873 ms (5%) |           |  563.86 KiB (1%) |       10214 |
| `["findfirst", "n=1000", "reduce", "basesize=256"]` | 302.697 ms (5%) |           |  287.22 KiB (1%) |        5220 |
| `["findfirst", "n=1000", "reduce", "basesize=512"]` | 304.477 ms (5%) |           |  149.33 KiB (1%) |        2722 |
| `["findfirst", "n=400", "foldl"]`                   | 413.934 ms (5%) |           |                  |             |
| `["findfirst", "n=400", "reduce", "basesize=128"]`  | 249.982 ms (5%) |           |    1.02 MiB (1%) |       18942 |
| `["findfirst", "n=400", "reduce", "basesize=256"]`  | 235.603 ms (5%) |           |  526.06 KiB (1%) |        9564 |
| `["findfirst", "n=400", "reduce", "basesize=512"]`  | 229.488 ms (5%) |           |  267.17 KiB (1%) |        4872 |
| `["findfirst", "n=500", "foldl"]`                   |  71.752 ms (5%) |           |                  |             |
| `["findfirst", "n=500", "reduce", "basesize=128"]`  |  42.731 ms (5%) |           |  157.39 KiB (1%) |        2850 |
| `["findfirst", "n=500", "reduce", "basesize=256"]`  |  40.745 ms (5%) |           |   84.59 KiB (1%) |        1536 |
| `["findfirst", "n=500", "reduce", "basesize=512"]`  |  42.439 ms (5%) |           |   48.30 KiB (1%) |         878 |
| `["overhead", "default"]`                           | 223.551 μs (5%) |           |  146.25 KiB (1%) |        2632 |
| `["overhead", "stoppable=false"]`                   | 223.584 μs (5%) |           |  146.28 KiB (1%) |        2633 |
| `["overhead", "stoppable=true"]`                    | 419.323 μs (5%) |           |  146.58 KiB (1%) |        2652 |
| `["parallel_histogram", "assoc", "basesize=16384"]` |   4.905 ms (5%) |           |  732.06 KiB (1%) |         103 |
| `["parallel_histogram", "assoc", "basesize=4096"]`  |   5.749 ms (5%) |           |    1.80 MiB (1%) |         497 |
| `["parallel_histogram", "assoc", "basesize=8192"]`  |   5.331 ms (5%) |           |    1.43 MiB (1%) |         243 |
| `["parallel_histogram", "comm", "basesize=16384"]`  |  12.551 ms (5%) |           |    1.23 MiB (1%) |         684 |
| `["parallel_histogram", "comm", "basesize=4096"]`   |  15.763 ms (5%) |           |    1.03 MiB (1%) |        3900 |
| `["parallel_histogram", "comm", "basesize=8192"]`   |  15.027 ms (5%) |           |    1.27 MiB (1%) |        3199 |
| `["parallel_histogram", "seq"]`                     |   7.390 ms (5%) |           |  364.61 KiB (1%) |          24 |
| `["sum", "random", "foldl"]`                        |  14.072 ms (5%) |           |    64 bytes (1%) |           3 |
| `["sum", "random", "reduce", "basesize=128"]`       |   8.009 ms (5%) |           |  313.39 KiB (1%) |        6069 |
| `["sum", "random", "reduce", "basesize=256"]`       |   7.750 ms (5%) |           |  155.16 KiB (1%) |        3013 |
| `["sum", "random", "reduce", "basesize=512"]`       |   7.639 ms (5%) |           |   76.30 KiB (1%) |        1485 |
| `["sum", "uniform", "foldl"]`                       |  13.693 ms (5%) |           |    64 bytes (1%) |           3 |
| `["sum", "uniform", "reduce", "basesize=128"]`      |   7.810 ms (5%) |           |  313.44 KiB (1%) |        6072 |
| `["sum", "uniform", "reduce", "basesize=256"]`      |   7.568 ms (5%) |           |  155.14 KiB (1%) |        3012 |
| `["sum", "uniform", "reduce", "basesize=512"]`      |   7.460 ms (5%) |           |   76.31 KiB (1%) |        1486 |
| `["sum", "valley", "foldl"]`                        |  14.155 ms (5%) |           |    64 bytes (1%) |           3 |
| `["sum", "valley", "reduce", "basesize=128"]`       |   8.045 ms (5%) |           |  313.36 KiB (1%) |        6067 |
| `["sum", "valley", "reduce", "basesize=256"]`       |   7.835 ms (5%) |           |  155.14 KiB (1%) |        3012 |
| `["sum", "valley", "reduce", "basesize=512"]`       |   7.689 ms (5%) |           |   76.34 KiB (1%) |        1488 |
| `["words", "nthreads=1"]`                           |  34.498 ms (5%) |  7.319 ms |   62.69 MiB (1%) |     2048150 |
| `["words", "nthreads=2"]`                           |  29.426 ms (5%) |           |   63.29 MiB (1%) |     2056245 |
| `["words", "nthreads=4"]`                           |  30.628 ms (5%) |           |   64.56 MiB (1%) |     2068734 |

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
       #1  2800 MHz      51402 s          0 s       2194 s      13573 s          0 s
       #2  2800 MHz      49340 s          0 s       1725 s      17556 s          0 s
       
  Memory: 7.7900238037109375 GB (5834.6484375 MB free)
  Uptime: 692.0 sec
  Load Avg:  1.7158203125  1.5322265625  0.88134765625
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-8.0.1 (ORCJIT, skylake)
```

---
# Baseline result
# Benchmark Report for */home/travis/build/JuliaFolds/Transducers.jl*

## Job Properties
* Time of benchmark: 9 Aug 2020 - 4:10
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
| `["collect", "assoc", "basesize=1"]`                | 322.038 ms (5%) | 12.851 ms |  87.55 MiB (1%) |     1590683 |
| `["collect", "assoc", "basesize=1024"]`             | 179.665 ms (5%) |           |   1.84 MiB (1%) |        1812 |
| `["collect", "assoc", "basesize=32"]`               | 184.284 ms (5%) |           |   5.64 MiB (1%) |       54010 |
| `["collect", "seq"]`                                | 350.099 ms (5%) |           |   1.50 MiB (1%) |       32784 |
| `["collect", "unordered", "basesize=1"]`            | 375.689 ms (5%) |           |  29.16 MiB (1%) |      403008 |
| `["collect", "unordered", "basesize=1024"]`         | 261.999 ms (5%) |           |   1.00 MiB (1%) |       18318 |
| `["collect", "unordered", "basesize=32"]`           | 205.586 ms (5%) |           |   1.51 MiB (1%) |       19267 |
| `["findfirst", "n=1000", "foldl"]`                  | 556.794 ms (5%) |           |                 |             |
| `["findfirst", "n=1000", "reduce", "basesize=128"]` | 315.007 ms (5%) |           | 563.97 KiB (1%) |       10221 |
| `["findfirst", "n=1000", "reduce", "basesize=256"]` | 307.035 ms (5%) |           | 287.16 KiB (1%) |        5216 |
| `["findfirst", "n=1000", "reduce", "basesize=512"]` | 308.811 ms (5%) |           | 149.30 KiB (1%) |        2720 |
| `["findfirst", "n=400", "foldl"]`                   | 417.936 ms (5%) |           |                 |             |
| `["findfirst", "n=400", "reduce", "basesize=128"]`  | 253.193 ms (5%) |           |   1.02 MiB (1%) |       18942 |
| `["findfirst", "n=400", "reduce", "basesize=256"]`  | 238.900 ms (5%) |           | 526.00 KiB (1%) |        9560 |
| `["findfirst", "n=400", "reduce", "basesize=512"]`  | 233.528 ms (5%) |           | 267.16 KiB (1%) |        4871 |
| `["findfirst", "n=500", "foldl"]`                   |  72.422 ms (5%) |           |                 |             |
| `["findfirst", "n=500", "reduce", "basesize=128"]`  |  43.282 ms (5%) |           | 157.39 KiB (1%) |        2850 |
| `["findfirst", "n=500", "reduce", "basesize=256"]`  |  41.313 ms (5%) |           |  84.56 KiB (1%) |        1534 |
| `["findfirst", "n=500", "reduce", "basesize=512"]`  |  43.014 ms (5%) |           |  48.31 KiB (1%) |         879 |
| `["overhead", "default"]`                           | 225.457 μs (5%) |           | 146.27 KiB (1%) |        2633 |
| `["overhead", "stoppable=false"]`                   | 223.739 μs (5%) |           | 146.27 KiB (1%) |        2632 |
| `["overhead", "stoppable=true"]`                    | 284.625 μs (5%) |           | 146.58 KiB (1%) |        2652 |
| `["parallel_histogram", "assoc", "basesize=16384"]` |   4.854 ms (5%) |           | 732.06 KiB (1%) |         103 |
| `["parallel_histogram", "assoc", "basesize=4096"]`  |   5.680 ms (5%) |           |   1.80 MiB (1%) |         498 |
| `["parallel_histogram", "assoc", "basesize=8192"]`  |   5.278 ms (5%) |           |   1.43 MiB (1%) |         243 |
| `["parallel_histogram", "comm", "basesize=16384"]`  |  12.776 ms (5%) |           |   1.22 MiB (1%) |         160 |
| `["parallel_histogram", "comm", "basesize=4096"]`   |  18.508 ms (5%) |           |   1.10 MiB (1%) |        6544 |
| `["parallel_histogram", "comm", "basesize=8192"]`   |  15.413 ms (5%) |           |   1.27 MiB (1%) |        3374 |
| `["parallel_histogram", "seq"]`                     |   7.391 ms (5%) |           | 364.61 KiB (1%) |          24 |
| `["sum", "random", "foldl"]`                        |  14.112 ms (5%) |           |   64 bytes (1%) |           3 |
| `["sum", "random", "reduce", "basesize=128"]`       |   8.021 ms (5%) |           | 313.42 KiB (1%) |        6071 |
| `["sum", "random", "reduce", "basesize=256"]`       |   7.785 ms (5%) |           | 155.13 KiB (1%) |        3011 |
| `["sum", "random", "reduce", "basesize=512"]`       |   7.675 ms (5%) |           |  76.31 KiB (1%) |        1486 |
| `["sum", "uniform", "foldl"]`                       |  13.700 ms (5%) |           |   64 bytes (1%) |           3 |
| `["sum", "uniform", "reduce", "basesize=128"]`      |   7.803 ms (5%) |           | 313.44 KiB (1%) |        6072 |
| `["sum", "uniform", "reduce", "basesize=256"]`      |   7.573 ms (5%) |           | 155.14 KiB (1%) |        3012 |
| `["sum", "uniform", "reduce", "basesize=512"]`      |   7.456 ms (5%) |           |  76.31 KiB (1%) |        1486 |
| `["sum", "valley", "foldl"]`                        |  14.187 ms (5%) |           |   64 bytes (1%) |           3 |
| `["sum", "valley", "reduce", "basesize=128"]`       |   8.056 ms (5%) |           | 313.28 KiB (1%) |        6062 |
| `["sum", "valley", "reduce", "basesize=256"]`       |   7.853 ms (5%) |           | 155.16 KiB (1%) |        3013 |
| `["sum", "valley", "reduce", "basesize=512"]`       |   7.710 ms (5%) |           |  76.33 KiB (1%) |        1487 |
| `["words", "nthreads=1"]`                           |  33.238 ms (5%) |  7.082 ms |  63.22 MiB (1%) |     2066117 |
| `["words", "nthreads=2"]`                           |  29.001 ms (5%) |           |  64.31 MiB (1%) |     2078318 |
| `["words", "nthreads=4"]`                           |  30.052 ms (5%) |           |  64.94 MiB (1%) |     2084526 |

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
       #1  2800 MHz      70682 s          0 s       2602 s      22448 s          0 s
       #2  2800 MHz      74766 s          0 s       2316 s      20246 s          0 s
       
  Memory: 7.7900238037109375 GB (5858.37109375 MB free)
  Uptime: 979.0 sec
  Load Avg:  1.73974609375  1.6298828125  1.09912109375
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
    CPU MHz:               2800.176
    BogoMIPS:              5600.35
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

