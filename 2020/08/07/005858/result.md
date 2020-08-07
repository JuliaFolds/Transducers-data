# Multi-thread benchmark result

* Pull request commit: [`e330305d6ac297a350d2a94171b173d80e5ba9f6`](https://github.com/JuliaFolds/Transducers.jl/commit/e330305d6ac297a350d2a94171b173d80e5ba9f6)
* Pull request: <https://github.com/JuliaFolds/Transducers.jl/pull/243> (Update */Manifest.toml)

# Judge result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmarks:
    - Target: 7 Aug 2020 - 00:52
    - Baseline: 7 Aug 2020 - 00:58
* Package commits:
    - Target: c23088
    - Baseline: f87cd6
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
| `["collect", "unordered", "basesize=1024"]`         | 0.71 (5%) :white_check_mark: | 0.82 (1%) :white_check_mark: |

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
      Ubuntu 18.04.4 LTS
  uname: Linux 5.3.0-1034-azure #35~18.04.1-Ubuntu SMP Mon Jul 13 12:54:45 UTC 2020 x86_64 x86_64
  CPU: Intel(R) Xeon(R) Platinum 8171M CPU @ 2.60GHz: 
              speed         user         nice          sys         idle          irq
       #1  2095 MHz      50684 s          0 s       2276 s      18658 s          0 s
       #2  2095 MHz      51356 s          0 s       2340 s      18072 s          0 s
       
  Memory: 6.764881134033203 GB (3017.91015625 MB free)
  Uptime: 737.0 sec
  Load Avg:  1.67919921875  1.6328125  1.02392578125
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
      Ubuntu 18.04.4 LTS
  uname: Linux 5.3.0-1034-azure #35~18.04.1-Ubuntu SMP Mon Jul 13 12:54:45 UTC 2020 x86_64 x86_64
  CPU: Intel(R) Xeon(R) Platinum 8171M CPU @ 2.60GHz: 
              speed         user         nice          sys         idle          irq
       #1  2095 MHz      76876 s          0 s       2947 s      25709 s          0 s
       #2  2095 MHz      74952 s          0 s       2995 s      27767 s          0 s
       
  Memory: 6.764881134033203 GB (2991.3671875 MB free)
  Uptime: 1078.0 sec
  Load Avg:  1.669921875  1.5927734375  1.181640625
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-8.0.1 (ORCJIT, skylake)
```

---
# Target result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmark: 7 Aug 2020 - 0:52
* Package commit: c23088
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
| `["collect", "assoc", "basesize=1"]`                | 393.473 ms (5%) | 12.091 ms |  87.55 MiB (1%) |     1590727 |
| `["collect", "assoc", "basesize=1024"]`             | 249.352 ms (5%) |           |   1.84 MiB (1%) |        1813 |
| `["collect", "assoc", "basesize=32"]`               | 253.889 ms (5%) |           |   5.64 MiB (1%) |       54014 |
| `["collect", "seq"]`                                | 496.831 ms (5%) |           |   1.50 MiB (1%) |       32784 |
| `["collect", "unordered", "basesize=1"]`            | 515.906 ms (5%) |           |  29.16 MiB (1%) |      403549 |
| `["collect", "unordered", "basesize=1024"]`         | 276.487 ms (5%) |           | 766.91 KiB (1%) |        2129 |
| `["collect", "unordered", "basesize=32"]`           | 281.554 ms (5%) |           |   1.47 MiB (1%) |       16784 |
| `["findfirst", "n=1000", "foldl"]`                  | 784.210 ms (5%) |           |                 |             |
| `["findfirst", "n=1000", "reduce", "basesize=128"]` | 396.860 ms (5%) |           | 564.14 KiB (1%) |       10232 |
| `["findfirst", "n=1000", "reduce", "basesize=256"]` | 394.601 ms (5%) |           | 287.41 KiB (1%) |        5232 |
| `["findfirst", "n=1000", "reduce", "basesize=512"]` | 401.833 ms (5%) |           | 149.34 KiB (1%) |        2723 |
| `["findfirst", "n=400", "foldl"]`                   | 587.874 ms (5%) |           |                 |             |
| `["findfirst", "n=400", "reduce", "basesize=128"]`  | 299.112 ms (5%) |           |   1.02 MiB (1%) |       18979 |
| `["findfirst", "n=400", "reduce", "basesize=256"]`  | 296.633 ms (5%) |           | 526.27 KiB (1%) |        9577 |
| `["findfirst", "n=400", "reduce", "basesize=512"]`  | 297.589 ms (5%) |           | 267.20 KiB (1%) |        4874 |
| `["findfirst", "n=500", "foldl"]`                   | 101.546 ms (5%) |           |                 |             |
| `["findfirst", "n=500", "reduce", "basesize=128"]`  |  52.205 ms (5%) |           | 157.50 KiB (1%) |        2857 |
| `["findfirst", "n=500", "reduce", "basesize=256"]`  |  51.873 ms (5%) |           |  84.61 KiB (1%) |        1537 |
| `["findfirst", "n=500", "reduce", "basesize=512"]`  |  55.265 ms (5%) |           |  48.31 KiB (1%) |         879 |
| `["overhead", "default"]`                           | 216.912 μs (5%) |           | 146.27 KiB (1%) |        2633 |
| `["overhead", "stoppable=false"]`                   | 216.912 μs (5%) |           | 146.27 KiB (1%) |        2632 |
| `["overhead", "stoppable=true"]`                    | 379.020 μs (5%) |           | 146.55 KiB (1%) |        2650 |
| `["parallel_histogram", "assoc", "basesize=16384"]` |   5.576 ms (5%) |           | 732.06 KiB (1%) |         103 |
| `["parallel_histogram", "assoc", "basesize=4096"]`  |   6.362 ms (5%) |           |   1.80 MiB (1%) |         497 |
| `["parallel_histogram", "assoc", "basesize=8192"]`  |   5.968 ms (5%) |           |   1.43 MiB (1%) |         243 |
| `["parallel_histogram", "comm", "basesize=16384"]`  |  16.232 ms (5%) |           |   1.22 MiB (1%) |         159 |
| `["parallel_histogram", "comm", "basesize=4096"]`   |  24.158 ms (5%) |           |   1.05 MiB (1%) |        5080 |
| `["parallel_histogram", "comm", "basesize=8192"]`   |  20.908 ms (5%) |           |   1.25 MiB (1%) |        2051 |
| `["parallel_histogram", "seq"]`                     |  10.141 ms (5%) |           | 364.61 KiB (1%) |          24 |
| `["sum", "random", "foldl"]`                        |  19.809 ms (5%) |           |   64 bytes (1%) |           3 |
| `["sum", "random", "reduce", "basesize=128"]`       |  10.426 ms (5%) |           | 313.39 KiB (1%) |        6069 |
| `["sum", "random", "reduce", "basesize=256"]`       |  10.215 ms (5%) |           | 155.14 KiB (1%) |        3012 |
| `["sum", "random", "reduce", "basesize=512"]`       |  10.054 ms (5%) |           |  76.31 KiB (1%) |        1486 |
| `["sum", "uniform", "foldl"]`                       |  19.343 ms (5%) |           |   64 bytes (1%) |           3 |
| `["sum", "uniform", "reduce", "basesize=128"]`      |  10.201 ms (5%) |           | 313.42 KiB (1%) |        6071 |
| `["sum", "uniform", "reduce", "basesize=256"]`      |   9.980 ms (5%) |           | 155.14 KiB (1%) |        3012 |
| `["sum", "uniform", "reduce", "basesize=512"]`      |   9.845 ms (5%) |           |  76.33 KiB (1%) |        1487 |
| `["sum", "valley", "foldl"]`                        |  20.032 ms (5%) |           |   64 bytes (1%) |           3 |
| `["sum", "valley", "reduce", "basesize=128"]`       |  10.526 ms (5%) |           | 313.28 KiB (1%) |        6062 |
| `["sum", "valley", "reduce", "basesize=256"]`       |  10.348 ms (5%) |           | 155.17 KiB (1%) |        3014 |
| `["sum", "valley", "reduce", "basesize=512"]`       |  10.185 ms (5%) |           |  76.34 KiB (1%) |        1488 |
| `["words", "nthreads=1"]`                           |  39.280 ms (5%) |  7.396 ms |  63.02 MiB (1%) |     2059355 |
| `["words", "nthreads=2"]`                           |  20.393 ms (5%) |           |  64.10 MiB (1%) |     2071626 |
| `["words", "nthreads=4"]`                           |  21.105 ms (5%) |           |  65.05 MiB (1%) |     2082080 |

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
      Ubuntu 18.04.4 LTS
  uname: Linux 5.3.0-1034-azure #35~18.04.1-Ubuntu SMP Mon Jul 13 12:54:45 UTC 2020 x86_64 x86_64
  CPU: Intel(R) Xeon(R) Platinum 8171M CPU @ 2.60GHz: 
              speed         user         nice          sys         idle          irq
       #1  2095 MHz      50684 s          0 s       2276 s      18658 s          0 s
       #2  2095 MHz      51356 s          0 s       2340 s      18072 s          0 s
       
  Memory: 6.764881134033203 GB (3017.91015625 MB free)
  Uptime: 737.0 sec
  Load Avg:  1.67919921875  1.6328125  1.02392578125
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-8.0.1 (ORCJIT, skylake)
```

---
# Baseline result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmark: 7 Aug 2020 - 0:58
* Package commit: f87cd6
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
| `["collect", "assoc", "basesize=1"]`                | 396.886 ms (5%) | 11.360 ms |  87.55 MiB (1%) |     1590784 |
| `["collect", "assoc", "basesize=1024"]`             | 250.758 ms (5%) |           |   1.84 MiB (1%) |        1813 |
| `["collect", "assoc", "basesize=32"]`               | 255.245 ms (5%) |           |   5.64 MiB (1%) |       54021 |
| `["collect", "seq"]`                                | 497.703 ms (5%) |           |   1.50 MiB (1%) |       32784 |
| `["collect", "unordered", "basesize=1"]`            | 516.324 ms (5%) |           |  29.16 MiB (1%) |      403568 |
| `["collect", "unordered", "basesize=1024"]`         | 391.624 ms (5%) |           | 931.00 KiB (1%) |       12676 |
| `["collect", "unordered", "basesize=32"]`           | 282.097 ms (5%) |           |   1.47 MiB (1%) |       16717 |
| `["findfirst", "n=1000", "foldl"]`                  | 789.276 ms (5%) |           |                 |             |
| `["findfirst", "n=1000", "reduce", "basesize=128"]` | 399.900 ms (5%) |           | 564.14 KiB (1%) |       10232 |
| `["findfirst", "n=1000", "reduce", "basesize=256"]` | 397.830 ms (5%) |           | 287.33 KiB (1%) |        5227 |
| `["findfirst", "n=1000", "reduce", "basesize=512"]` | 405.205 ms (5%) |           | 149.42 KiB (1%) |        2728 |
| `["findfirst", "n=400", "foldl"]`                   | 592.624 ms (5%) |           |                 |             |
| `["findfirst", "n=400", "reduce", "basesize=128"]`  | 300.983 ms (5%) |           |   1.02 MiB (1%) |       18977 |
| `["findfirst", "n=400", "reduce", "basesize=256"]`  | 298.950 ms (5%) |           | 526.16 KiB (1%) |        9570 |
| `["findfirst", "n=400", "reduce", "basesize=512"]`  | 300.973 ms (5%) |           | 267.27 KiB (1%) |        4878 |
| `["findfirst", "n=500", "foldl"]`                   | 102.371 ms (5%) |           |                 |             |
| `["findfirst", "n=500", "reduce", "basesize=128"]`  |  52.523 ms (5%) |           | 157.50 KiB (1%) |        2857 |
| `["findfirst", "n=500", "reduce", "basesize=256"]`  |  52.295 ms (5%) |           |  84.59 KiB (1%) |        1536 |
| `["findfirst", "n=500", "reduce", "basesize=512"]`  |  55.568 ms (5%) |           |  48.33 KiB (1%) |         880 |
| `["overhead", "default"]`                           | 215.321 μs (5%) |           | 146.27 KiB (1%) |        2633 |
| `["overhead", "stoppable=false"]`                   | 215.421 μs (5%) |           | 146.27 KiB (1%) |        2632 |
| `["overhead", "stoppable=true"]`                    | 378.036 μs (5%) |           | 146.53 KiB (1%) |        2649 |
| `["parallel_histogram", "assoc", "basesize=16384"]` |   5.575 ms (5%) |           | 732.06 KiB (1%) |         103 |
| `["parallel_histogram", "assoc", "basesize=4096"]`  |   6.338 ms (5%) |           |   1.80 MiB (1%) |         497 |
| `["parallel_histogram", "assoc", "basesize=8192"]`  |   5.964 ms (5%) |           |   1.43 MiB (1%) |         243 |
| `["parallel_histogram", "comm", "basesize=16384"]`  |  15.896 ms (5%) |           |   1.22 MiB (1%) |         159 |
| `["parallel_histogram", "comm", "basesize=4096"]`   |  25.123 ms (5%) |           |   1.05 MiB (1%) |        5210 |
| `["parallel_histogram", "comm", "basesize=8192"]`   |  21.905 ms (5%) |           |   1.25 MiB (1%) |        2289 |
| `["parallel_histogram", "seq"]`                     |  10.110 ms (5%) |           | 364.61 KiB (1%) |          24 |
| `["sum", "random", "foldl"]`                        |  19.950 ms (5%) |           |   64 bytes (1%) |           3 |
| `["sum", "random", "reduce", "basesize=128"]`       |  10.579 ms (5%) |           | 313.38 KiB (1%) |        6068 |
| `["sum", "random", "reduce", "basesize=256"]`       |  10.350 ms (5%) |           | 155.13 KiB (1%) |        3011 |
| `["sum", "random", "reduce", "basesize=512"]`       |  10.234 ms (5%) |           |  76.36 KiB (1%) |        1489 |
| `["sum", "uniform", "foldl"]`                       |  19.405 ms (5%) |           |   64 bytes (1%) |           3 |
| `["sum", "uniform", "reduce", "basesize=128"]`      |  10.200 ms (5%) |           | 313.42 KiB (1%) |        6071 |
| `["sum", "uniform", "reduce", "basesize=256"]`      |  10.008 ms (5%) |           | 155.14 KiB (1%) |        3012 |
| `["sum", "uniform", "reduce", "basesize=512"]`      |   9.845 ms (5%) |           |  76.31 KiB (1%) |        1486 |
| `["sum", "valley", "foldl"]`                        |  20.087 ms (5%) |           |   64 bytes (1%) |           3 |
| `["sum", "valley", "reduce", "basesize=128"]`       |  10.654 ms (5%) |           | 313.31 KiB (1%) |        6064 |
| `["sum", "valley", "reduce", "basesize=256"]`       |  10.485 ms (5%) |           | 155.16 KiB (1%) |        3013 |
| `["sum", "valley", "reduce", "basesize=512"]`       |  10.350 ms (5%) |           |  76.31 KiB (1%) |        1486 |
| `["words", "nthreads=1"]`                           |  38.726 ms (5%) |  7.267 ms |  62.89 MiB (1%) |     2054477 |
| `["words", "nthreads=2"]`                           |  20.363 ms (5%) |           |  63.98 MiB (1%) |     2066740 |
| `["words", "nthreads=4"]`                           |  21.524 ms (5%) |           |  64.93 MiB (1%) |     2077211 |

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
      Ubuntu 18.04.4 LTS
  uname: Linux 5.3.0-1034-azure #35~18.04.1-Ubuntu SMP Mon Jul 13 12:54:45 UTC 2020 x86_64 x86_64
  CPU: Intel(R) Xeon(R) Platinum 8171M CPU @ 2.60GHz: 
              speed         user         nice          sys         idle          irq
       #1  2095 MHz      76876 s          0 s       2947 s      25709 s          0 s
       #2  2095 MHz      74952 s          0 s       2995 s      27767 s          0 s
       
  Memory: 6.764881134033203 GB (2991.3671875 MB free)
  Uptime: 1078.0 sec
  Load Avg:  1.669921875  1.5927734375  1.181640625
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

    Architecture:        x86_64
    CPU op-mode(s):      32-bit, 64-bit
    Byte Order:          Little Endian
    CPU(s):              2
    On-line CPU(s) list: 0,1
    Thread(s) per core:  1
    Core(s) per socket:  2
    Socket(s):           1
    NUMA node(s):        1
    Vendor ID:           GenuineIntel
    CPU family:          6
    Model:               85
    Model name:          Intel(R) Xeon(R) Platinum 8171M CPU @ 2.60GHz
    Stepping:            4
    CPU MHz:             2095.193
    BogoMIPS:            4190.38
    Hypervisor vendor:   Microsoft
    Virtualization type: full
    L1d cache:           32K
    L1i cache:           32K
    L2 cache:            1024K
    L3 cache:            36608K
    NUMA node0 CPU(s):   0,1
    Flags:               fpu vme de pse tsc msr pae mce cx8 apic sep mtrr pge mca cmov pat pse36 clflush mmx fxsr sse sse2 ss ht syscall nx pdpe1gb rdtscp lm constant_tsc rep_good nopl xtopology cpuid pni pclmulqdq ssse3 fma cx16 pcid sse4_1 sse4_2 movbe popcnt aes xsave avx f16c rdrand hypervisor lahf_lm abm 3dnowprefetch invpcid_single pti fsgsbase bmi1 hle avx2 smep bmi2 erms invpcid rtm mpx avx512f avx512dq rdseed adx smap clflushopt avx512cd avx512bw avx512vl xsaveopt xsavec xsaves md_clear
    

| Cpu Property       | Value                                                   |
|:------------------ |:------------------------------------------------------- |
| Brand              | Intel(R) Xeon(R) Platinum 8171M CPU @ 2.60GHz           |
| Vendor             | :Intel                                                  |
| Architecture       | :Skylake                                                |
| Model              | Family: 0x06, Model: 0x55, Stepping: 0x04, Type: 0x00   |
| Cores              | 2 physical cores, 2 logical cores (on executing CPU)    |
|                    | No Hyperthreading detected                              |
| Clock Frequencies  | Not supported by CPU                                    |
| Data Cache         | Level 1:3 : (32, 1024, 36608) kbytes                    |
|                    | 64 byte cache line size                                 |
| Address Size       | 48 bits virtual, 44 bits physical                       |
| SIMD               | 512 bit = 64 byte max. SIMD vector size                 |
| Time Stamp Counter | TSC is accessible via `rdtsc`                           |
|                    | TSC increased at every clock cycle (non-invariant TSC)  |
| Perf. Monitoring   | Performance Monitoring Counters (PMC) are not supported |
| Hypervisor         | Yes, Microsoft                                          |

