# Multi-thread benchmark result (via Travis)


# Judge result
# Benchmark Report for */home/travis/build/JuliaFolds/Transducers.jl*

## Job Properties
* Time of benchmarks:
    - Target: 14 Sep 2020 - 01:01
    - Baseline: 14 Sep 2020 - 01:06
* Package commits:
    - Target: 533c41
    - Baseline: b2fa04
* Julia commits:
    - Target: 697e78
    - Baseline: 697e78
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
| `["collect", "unordered", "basesize=1024"]`         |                1.12 (5%) :x: | 1.15 (1%) :x: |
| `["parallel_histogram", "comm", "basesize=16384"]`  | 0.88 (5%) :white_check_mark: |    1.00 (1%)  |
| `["parallel_histogram", "comm", "basesize=4096"]`   |                   0.97 (5%)  | 1.22 (1%) :x: |
| `["parallel_histogram", "comm", "basesize=8192"]`   |                   0.99 (5%)  | 1.02 (1%) :x: |
| `["words", "nthreads=2"]`                           |                1.06 (5%) :x: |    0.99 (1%)  |
| `["words", "nthreads=4"]`                           |                1.06 (5%) :x: |    1.00 (1%)  |

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
Julia Version 1.5.1
Commit 697e782ab8 (2020-08-25 20:08 UTC)
Platform Info:
  OS: Linux (x86_64-pc-linux-gnu)
      Ubuntu 16.04.6 LTS
  uname: Linux 4.15.0-1028-gcp #29~16.04.1-Ubuntu SMP Tue Feb 12 16:31:10 UTC 2019 x86_64 x86_64
  CPU: Intel(R) Xeon(R) CPU: 
              speed         user         nice          sys         idle          irq
       #1  2800 MHz      46110 s          0 s       1732 s      17081 s          0 s
       #2  2800 MHz      51293 s          0 s       1559 s      12267 s          0 s
       
  Memory: 7.790031433105469 GB (5865.90234375 MB free)
  Uptime: 657.0 sec
  Load Avg:  1.7470703125  1.49169921875  0.83837890625
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-9.0.1 (ORCJIT, cascadelake)
```

### Baseline
```
Julia Version 1.5.1
Commit 697e782ab8 (2020-08-25 20:08 UTC)
Platform Info:
  OS: Linux (x86_64-pc-linux-gnu)
      Ubuntu 16.04.6 LTS
  uname: Linux 4.15.0-1028-gcp #29~16.04.1-Ubuntu SMP Tue Feb 12 16:31:10 UTC 2019 x86_64 x86_64
  CPU: Intel(R) Xeon(R) CPU: 
              speed         user         nice          sys         idle          irq
       #1  2800 MHz      70224 s          0 s       2246 s      23542 s          0 s
       #2  2800 MHz      74323 s          0 s       2101 s      19825 s          0 s
       
  Memory: 7.790031433105469 GB (5865.62890625 MB free)
  Uptime: 969.0 sec
  Load Avg:  1.748046875  1.57177734375  1.05517578125
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-9.0.1 (ORCJIT, cascadelake)
```

---
# Target result
# Benchmark Report for */home/travis/build/JuliaFolds/Transducers.jl*

## Job Properties
* Time of benchmark: 14 Sep 2020 - 1:1
* Package commit: 533c41
* Julia commit: 697e78
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
| `["collect", "assoc", "basesize=1"]`                | 317.198 ms (5%) | 13.820 ms |   82.16 MiB (1%) |     1368074 |
| `["collect", "assoc", "basesize=1024"]`             | 179.990 ms (5%) |           |    1.83 MiB (1%) |        1597 |
| `["collect", "assoc", "basesize=32"]`               | 185.640 ms (5%) |           |    5.47 MiB (1%) |       47070 |
| `["collect", "seq"]`                                | 349.955 ms (5%) |           |  512.72 KiB (1%) |          15 |
| `["collect", "unordered", "basesize=1"]`            | 348.227 ms (5%) |           |   30.01 MiB (1%) |      360697 |
| `["collect", "unordered", "basesize=1024"]`         | 248.911 ms (5%) |           |  977.67 KiB (1%) |        8007 |
| `["collect", "unordered", "basesize=32"]`           | 200.419 ms (5%) |           |    1.49 MiB (1%) |       13169 |
| `["findfirst", "n=1000", "foldl"]`                  | 556.323 ms (5%) |           |                  |             |
| `["findfirst", "n=1000", "reduce", "basesize=128"]` | 301.055 ms (5%) |           |  546.33 KiB (1%) |        9561 |
| `["findfirst", "n=1000", "reduce", "basesize=256"]` | 299.747 ms (5%) |           |  278.25 KiB (1%) |        4888 |
| `["findfirst", "n=1000", "reduce", "basesize=512"]` | 305.116 ms (5%) |           |  144.66 KiB (1%) |        2550 |
| `["findfirst", "n=400", "foldl"]`                   | 417.281 ms (5%) |           |                  |             |
| `["findfirst", "n=400", "reduce", "basesize=128"]`  | 228.123 ms (5%) |           | 1012.83 KiB (1%) |       17724 |
| `["findfirst", "n=400", "reduce", "basesize=256"]`  | 226.000 ms (5%) |           |  509.63 KiB (1%) |        8952 |
| `["findfirst", "n=400", "reduce", "basesize=512"]`  | 226.819 ms (5%) |           |  258.84 KiB (1%) |        4564 |
| `["findfirst", "n=500", "foldl"]`                   |  72.319 ms (5%) |           |                  |             |
| `["findfirst", "n=500", "reduce", "basesize=128"]`  |  39.686 ms (5%) |           |  152.59 KiB (1%) |        2677 |
| `["findfirst", "n=500", "reduce", "basesize=256"]`  |  39.418 ms (5%) |           |   82.00 KiB (1%) |        1444 |
| `["findfirst", "n=500", "reduce", "basesize=512"]`  |  41.984 ms (5%) |           |   46.84 KiB (1%) |         828 |
| `["overhead", "default"]`                           | 195.821 μs (5%) |           |  140.75 KiB (1%) |        2465 |
| `["overhead", "stoppable=false"]`                   | 197.057 μs (5%) |           |  140.78 KiB (1%) |        2465 |
| `["overhead", "stoppable=true"]`                    | 385.585 μs (5%) |           |  140.84 KiB (1%) |        2467 |
| `["parallel_histogram", "assoc", "basesize=16384"]` |   4.821 ms (5%) |           |  731.81 KiB (1%) |          94 |
| `["parallel_histogram", "assoc", "basesize=4096"]`  |   5.648 ms (5%) |           |    1.80 MiB (1%) |         448 |
| `["parallel_histogram", "assoc", "basesize=8192"]`  |   5.239 ms (5%) |           |    1.43 MiB (1%) |         220 |
| `["parallel_histogram", "comm", "basesize=16384"]`  |  11.415 ms (5%) |           |    1.24 MiB (1%) |         670 |
| `["parallel_histogram", "comm", "basesize=4096"]`   |  15.226 ms (5%) |           |    1.44 MiB (1%) |        7209 |
| `["parallel_histogram", "comm", "basesize=8192"]`   |  14.335 ms (5%) |           |    1.32 MiB (1%) |        3494 |
| `["parallel_histogram", "seq"]`                     |   7.450 ms (5%) |           |  364.61 KiB (1%) |          24 |
| `["sum", "random", "foldl"]`                        |  14.071 ms (5%) |           |    32 bytes (1%) |           2 |
| `["sum", "random", "reduce", "basesize=128"]`       |   8.107 ms (5%) |           |  292.02 KiB (1%) |        5213 |
| `["sum", "random", "reduce", "basesize=256"]`       |   7.922 ms (5%) |           |  144.53 KiB (1%) |        2589 |
| `["sum", "random", "reduce", "basesize=512"]`       |   7.787 ms (5%) |           |   71.11 KiB (1%) |        1279 |
| `["sum", "uniform", "foldl"]`                       |  13.710 ms (5%) |           |    32 bytes (1%) |           2 |
| `["sum", "uniform", "reduce", "basesize=128"]`      |   7.890 ms (5%) |           |  292.02 KiB (1%) |        5213 |
| `["sum", "uniform", "reduce", "basesize=256"]`      |   7.699 ms (5%) |           |  144.53 KiB (1%) |        2589 |
| `["sum", "uniform", "reduce", "basesize=512"]`      |   7.568 ms (5%) |           |   71.06 KiB (1%) |        1278 |
| `["sum", "valley", "foldl"]`                        |  14.108 ms (5%) |           |    32 bytes (1%) |           2 |
| `["sum", "valley", "reduce", "basesize=128"]`       |   8.142 ms (5%) |           |  292.02 KiB (1%) |        5213 |
| `["sum", "valley", "reduce", "basesize=256"]`       |   7.938 ms (5%) |           |  144.53 KiB (1%) |        2589 |
| `["sum", "valley", "reduce", "basesize=512"]`       |   7.806 ms (5%) |           |   71.06 KiB (1%) |        1278 |
| `["words", "nthreads=1"]`                           |  23.286 ms (5%) |           |   31.76 MiB (1%) |     1034724 |
| `["words", "nthreads=2"]`                           |  26.695 ms (5%) |           |   32.12 MiB (1%) |     1034793 |
| `["words", "nthreads=4"]`                           |  27.263 ms (5%) |           |   32.84 MiB (1%) |     1034949 |

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
Julia Version 1.5.1
Commit 697e782ab8 (2020-08-25 20:08 UTC)
Platform Info:
  OS: Linux (x86_64-pc-linux-gnu)
      Ubuntu 16.04.6 LTS
  uname: Linux 4.15.0-1028-gcp #29~16.04.1-Ubuntu SMP Tue Feb 12 16:31:10 UTC 2019 x86_64 x86_64
  CPU: Intel(R) Xeon(R) CPU: 
              speed         user         nice          sys         idle          irq
       #1  2800 MHz      46110 s          0 s       1732 s      17081 s          0 s
       #2  2800 MHz      51293 s          0 s       1559 s      12267 s          0 s
       
  Memory: 7.790031433105469 GB (5865.90234375 MB free)
  Uptime: 657.0 sec
  Load Avg:  1.7470703125  1.49169921875  0.83837890625
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-9.0.1 (ORCJIT, cascadelake)
```

---
# Baseline result
# Benchmark Report for */home/travis/build/JuliaFolds/Transducers.jl*

## Job Properties
* Time of benchmark: 14 Sep 2020 - 1:6
* Package commit: b2fa04
* Julia commit: 697e78
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
| `["collect", "assoc", "basesize=1"]`                | 310.629 ms (5%) | 13.527 ms |   82.16 MiB (1%) |     1368080 |
| `["collect", "assoc", "basesize=1024"]`             | 180.111 ms (5%) |           |    1.83 MiB (1%) |        1597 |
| `["collect", "assoc", "basesize=32"]`               | 184.461 ms (5%) |           |    5.47 MiB (1%) |       47069 |
| `["collect", "seq"]`                                | 349.861 ms (5%) |           |  512.72 KiB (1%) |          15 |
| `["collect", "unordered", "basesize=1"]`            | 344.077 ms (5%) |           |   30.01 MiB (1%) |      360656 |
| `["collect", "unordered", "basesize=1024"]`         | 222.040 ms (5%) |           |  851.05 KiB (1%) |        3973 |
| `["collect", "unordered", "basesize=32"]`           | 200.784 ms (5%) |           |    1.49 MiB (1%) |       13066 |
| `["findfirst", "n=1000", "foldl"]`                  | 556.550 ms (5%) |           |                  |             |
| `["findfirst", "n=1000", "reduce", "basesize=128"]` | 300.337 ms (5%) |           |  546.34 KiB (1%) |        9562 |
| `["findfirst", "n=1000", "reduce", "basesize=256"]` | 299.823 ms (5%) |           |  278.25 KiB (1%) |        4888 |
| `["findfirst", "n=1000", "reduce", "basesize=512"]` | 300.454 ms (5%) |           |  144.64 KiB (1%) |        2549 |
| `["findfirst", "n=400", "foldl"]`                   | 417.702 ms (5%) |           |                  |             |
| `["findfirst", "n=400", "reduce", "basesize=128"]`  | 227.353 ms (5%) |           | 1012.88 KiB (1%) |       17726 |
| `["findfirst", "n=400", "reduce", "basesize=256"]`  | 225.212 ms (5%) |           |  509.63 KiB (1%) |        8952 |
| `["findfirst", "n=400", "reduce", "basesize=512"]`  | 226.229 ms (5%) |           |  258.84 KiB (1%) |        4564 |
| `["findfirst", "n=500", "foldl"]`                   |  72.302 ms (5%) |           |                  |             |
| `["findfirst", "n=500", "reduce", "basesize=128"]`  |  39.614 ms (5%) |           |  152.59 KiB (1%) |        2677 |
| `["findfirst", "n=500", "reduce", "basesize=256"]`  |  39.323 ms (5%) |           |   82.00 KiB (1%) |        1444 |
| `["findfirst", "n=500", "reduce", "basesize=512"]`  |  41.894 ms (5%) |           |   46.84 KiB (1%) |         828 |
| `["overhead", "default"]`                           | 197.027 μs (5%) |           |  140.75 KiB (1%) |        2465 |
| `["overhead", "stoppable=false"]`                   | 198.473 μs (5%) |           |  140.78 KiB (1%) |        2465 |
| `["overhead", "stoppable=true"]`                    | 396.029 μs (5%) |           |  140.78 KiB (1%) |        2465 |
| `["parallel_histogram", "assoc", "basesize=16384"]` |   4.878 ms (5%) |           |  731.81 KiB (1%) |          94 |
| `["parallel_histogram", "assoc", "basesize=4096"]`  |   5.708 ms (5%) |           |    1.80 MiB (1%) |         448 |
| `["parallel_histogram", "assoc", "basesize=8192"]`  |   5.303 ms (5%) |           |    1.43 MiB (1%) |         220 |
| `["parallel_histogram", "comm", "basesize=16384"]`  |  12.977 ms (5%) |           |    1.24 MiB (1%) |         837 |
| `["parallel_histogram", "comm", "basesize=4096"]`   |  15.643 ms (5%) |           |    1.18 MiB (1%) |        5304 |
| `["parallel_histogram", "comm", "basesize=8192"]`   |  14.439 ms (5%) |           |    1.30 MiB (1%) |        2607 |
| `["parallel_histogram", "seq"]`                     |   7.445 ms (5%) |           |  364.61 KiB (1%) |          24 |
| `["sum", "random", "foldl"]`                        |  13.995 ms (5%) |           |    32 bytes (1%) |           2 |
| `["sum", "random", "reduce", "basesize=128"]`       |   7.989 ms (5%) |           |  292.02 KiB (1%) |        5213 |
| `["sum", "random", "reduce", "basesize=256"]`       |   7.774 ms (5%) |           |  144.53 KiB (1%) |        2589 |
| `["sum", "random", "reduce", "basesize=512"]`       |   7.662 ms (5%) |           |   71.11 KiB (1%) |        1279 |
| `["sum", "uniform", "foldl"]`                       |  13.717 ms (5%) |           |    32 bytes (1%) |           2 |
| `["sum", "uniform", "reduce", "basesize=128"]`      |   7.783 ms (5%) |           |  292.02 KiB (1%) |        5213 |
| `["sum", "uniform", "reduce", "basesize=256"]`      |   7.552 ms (5%) |           |  144.53 KiB (1%) |        2589 |
| `["sum", "uniform", "reduce", "basesize=512"]`      |   7.461 ms (5%) |           |   71.06 KiB (1%) |        1278 |
| `["sum", "valley", "foldl"]`                        |  14.116 ms (5%) |           |    32 bytes (1%) |           2 |
| `["sum", "valley", "reduce", "basesize=128"]`       |   8.099 ms (5%) |           |  292.02 KiB (1%) |        5213 |
| `["sum", "valley", "reduce", "basesize=256"]`       |   7.854 ms (5%) |           |  144.53 KiB (1%) |        2589 |
| `["sum", "valley", "reduce", "basesize=512"]`       |   7.753 ms (5%) |           |   71.06 KiB (1%) |        1278 |
| `["words", "nthreads=1"]`                           |  23.617 ms (5%) |           |   31.66 MiB (1%) |     1031067 |
| `["words", "nthreads=2"]`                           |  25.234 ms (5%) |           |   32.38 MiB (1%) |     1031215 |
| `["words", "nthreads=4"]`                           |  25.762 ms (5%) |           |   32.83 MiB (1%) |     1031386 |

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
Julia Version 1.5.1
Commit 697e782ab8 (2020-08-25 20:08 UTC)
Platform Info:
  OS: Linux (x86_64-pc-linux-gnu)
      Ubuntu 16.04.6 LTS
  uname: Linux 4.15.0-1028-gcp #29~16.04.1-Ubuntu SMP Tue Feb 12 16:31:10 UTC 2019 x86_64 x86_64
  CPU: Intel(R) Xeon(R) CPU: 
              speed         user         nice          sys         idle          irq
       #1  2800 MHz      70224 s          0 s       2246 s      23542 s          0 s
       #2  2800 MHz      74323 s          0 s       2101 s      19825 s          0 s
       
  Memory: 7.790031433105469 GB (5865.62890625 MB free)
  Uptime: 969.0 sec
  Load Avg:  1.748046875  1.57177734375  1.05517578125
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

