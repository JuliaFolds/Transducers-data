# Multi-thread benchmark result

* Pull request commit: [`c704e2d45ba3ee4e3ead60fc11c5da147d7cb75e`](https://github.com/JuliaFolds/Transducers.jl/commit/c704e2d45ba3ee4e3ead60fc11c5da147d7cb75e)
* Pull request: <https://github.com/JuliaFolds/Transducers.jl/pull/397> (Define collect(::Foldable) rather than collect(::Eduction))

# Judge result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmarks:
    - Target: 6 Aug 2020 - 15:29
    - Baseline: 6 Aug 2020 - 15:34
* Package commits:
    - Target: 9b885b
    - Baseline: 76f082
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
| `["collect", "unordered", "basesize=1024"]`         |    0.99 (5%)  | 0.99 (1%) :white_check_mark: |
| `["overhead", "stoppable=true"]`                    | 1.08 (5%) :x: |                   1.00 (1%)  |
| `["parallel_histogram", "assoc", "basesize=4096"]`  |    1.00 (5%)  | 0.87 (1%) :white_check_mark: |
| `["parallel_histogram", "comm", "basesize=4096"]`   | 1.12 (5%) :x: |                1.02 (1%) :x: |
| `["parallel_histogram", "comm", "basesize=8192"]`   |    1.04 (5%)  |                1.03 (1%) :x: |
| `["words", "nthreads=2"]`                           |    1.03 (5%)  |                1.01 (1%) :x: |

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
  CPU: Intel(R) Xeon(R) CPU E5-2673 v4 @ 2.30GHz: 
              speed         user         nice          sys         idle          irq
       #1  2294 MHz      46616 s          0 s       2358 s      25245 s          0 s
       #2  2294 MHz      54954 s          0 s       2715 s      16870 s          0 s
       
  Memory: 6.764881134033203 GB (2952.10546875 MB free)
  Uptime: 761.0 sec
  Load Avg:  1.6767578125  1.54931640625  0.974609375
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-8.0.1 (ORCJIT, broadwell)
```

### Baseline
```
Julia Version 1.4.2
Commit 44fa15b150* (2020-05-23 18:35 UTC)
Platform Info:
  OS: Linux (x86_64-pc-linux-gnu)
      Ubuntu 18.04.4 LTS
  uname: Linux 5.3.0-1034-azure #35~18.04.1-Ubuntu SMP Mon Jul 13 12:54:45 UTC 2020 x86_64 x86_64
  CPU: Intel(R) Xeon(R) CPU E5-2673 v4 @ 2.30GHz: 
              speed         user         nice          sys         idle          irq
       #1  2294 MHz      68159 s          0 s       2948 s      32252 s          0 s
       #2  2294 MHz      78404 s          0 s       3271 s      22098 s          0 s
       
  Memory: 6.764881134033203 GB (3001.0625 MB free)
  Uptime: 1054.0 sec
  Load Avg:  1.7822265625  1.63671875  1.1650390625
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-8.0.1 (ORCJIT, broadwell)
```

---
# Target result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmark: 6 Aug 2020 - 15:29
* Package commit: 9b885b
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
| `["collect", "assoc", "basesize=1"]`                | 308.420 ms (5%) | 11.623 ms |  87.55 MiB (1%) |     1590778 |
| `["collect", "assoc", "basesize=1024"]`             | 164.584 ms (5%) |           |   1.84 MiB (1%) |        1808 |
| `["collect", "assoc", "basesize=32"]`               | 169.434 ms (5%) |           |   5.64 MiB (1%) |       54014 |
| `["collect", "seq"]`                                | 322.598 ms (5%) |           |   1.50 MiB (1%) |       32784 |
| `["collect", "unordered", "basesize=1"]`            | 420.410 ms (5%) |           |  29.17 MiB (1%) |      404197 |
| `["collect", "unordered", "basesize=1024"]`         | 191.591 ms (5%) |           | 785.03 KiB (1%) |        3289 |
| `["collect", "unordered", "basesize=32"]`           | 198.756 ms (5%) |           |   1.49 MiB (1%) |       18019 |
| `["findfirst", "n=1000", "foldl"]`                  | 529.913 ms (5%) |           |                 |             |
| `["findfirst", "n=1000", "reduce", "basesize=128"]` | 273.369 ms (5%) |           | 564.17 KiB (1%) |       10234 |
| `["findfirst", "n=1000", "reduce", "basesize=256"]` | 279.582 ms (5%) |           | 287.33 KiB (1%) |        5227 |
| `["findfirst", "n=1000", "reduce", "basesize=512"]` | 283.174 ms (5%) |           | 149.27 KiB (1%) |        2718 |
| `["findfirst", "n=400", "foldl"]`                   | 395.819 ms (5%) |           |                 |             |
| `["findfirst", "n=400", "reduce", "basesize=128"]`  | 206.269 ms (5%) |           |   1.02 MiB (1%) |       18967 |
| `["findfirst", "n=400", "reduce", "basesize=256"]`  | 206.009 ms (5%) |           | 526.20 KiB (1%) |        9573 |
| `["findfirst", "n=400", "reduce", "basesize=512"]`  | 205.599 ms (5%) |           | 267.30 KiB (1%) |        4880 |
| `["findfirst", "n=500", "foldl"]`                   |  66.902 ms (5%) |           |                 |             |
| `["findfirst", "n=500", "reduce", "basesize=128"]`  |  35.352 ms (5%) |           | 157.50 KiB (1%) |        2857 |
| `["findfirst", "n=500", "reduce", "basesize=256"]`  |  34.959 ms (5%) |           |  84.61 KiB (1%) |        1537 |
| `["findfirst", "n=500", "reduce", "basesize=512"]`  |  37.543 ms (5%) |           |  48.33 KiB (1%) |         880 |
| `["overhead", "default"]`                           | 193.301 μs (5%) |           | 146.27 KiB (1%) |        2633 |
| `["overhead", "stoppable=false"]`                   | 195.102 μs (5%) |           | 146.27 KiB (1%) |        2632 |
| `["overhead", "stoppable=true"]`                    | 334.702 μs (5%) |           | 146.53 KiB (1%) |        2649 |
| `["parallel_histogram", "assoc", "basesize=16384"]` |   3.916 ms (5%) |           | 732.06 KiB (1%) |         103 |
| `["parallel_histogram", "assoc", "basesize=4096"]`  |   4.598 ms (5%) |           |   1.80 MiB (1%) |         497 |
| `["parallel_histogram", "assoc", "basesize=8192"]`  |   4.249 ms (5%) |           |   1.43 MiB (1%) |         242 |
| `["parallel_histogram", "comm", "basesize=16384"]`  |  12.051 ms (5%) |           |   1.22 MiB (1%) |         160 |
| `["parallel_histogram", "comm", "basesize=4096"]`   |  21.560 ms (5%) |           |   1.06 MiB (1%) |        5659 |
| `["parallel_histogram", "comm", "basesize=8192"]`   |  17.412 ms (5%) |           |   1.26 MiB (1%) |        2579 |
| `["parallel_histogram", "seq"]`                     |   6.793 ms (5%) |           | 364.61 KiB (1%) |          24 |
| `["sum", "random", "foldl"]`                        |  12.820 ms (5%) |           |   64 bytes (1%) |           3 |
| `["sum", "random", "reduce", "basesize=128"]`       |   6.962 ms (5%) |           | 313.42 KiB (1%) |        6071 |
| `["sum", "random", "reduce", "basesize=256"]`       |   6.778 ms (5%) |           | 155.14 KiB (1%) |        3012 |
| `["sum", "random", "reduce", "basesize=512"]`       |   6.616 ms (5%) |           |  76.31 KiB (1%) |        1486 |
| `["sum", "uniform", "foldl"]`                       |  12.458 ms (5%) |           |   64 bytes (1%) |           3 |
| `["sum", "uniform", "reduce", "basesize=128"]`      |   6.881 ms (5%) |           | 313.41 KiB (1%) |        6070 |
| `["sum", "uniform", "reduce", "basesize=256"]`      |   6.596 ms (5%) |           | 155.16 KiB (1%) |        3013 |
| `["sum", "uniform", "reduce", "basesize=512"]`      |   6.486 ms (5%) |           |  76.31 KiB (1%) |        1486 |
| `["sum", "valley", "foldl"]`                        |  12.822 ms (5%) |           |   64 bytes (1%) |           3 |
| `["sum", "valley", "reduce", "basesize=128"]`       |   6.979 ms (5%) |           | 313.33 KiB (1%) |        6065 |
| `["sum", "valley", "reduce", "basesize=256"]`       |   6.847 ms (5%) |           | 155.13 KiB (1%) |        3011 |
| `["sum", "valley", "reduce", "basesize=512"]`       |   6.676 ms (5%) |           |  76.31 KiB (1%) |        1486 |
| `["words", "nthreads=1"]`                           |  38.341 ms (5%) |  8.249 ms |  63.26 MiB (1%) |     2066589 |
| `["words", "nthreads=2"]`                           |  18.417 ms (5%) |           |  64.35 MiB (1%) |     2078856 |
| `["words", "nthreads=4"]`                           |  19.015 ms (5%) |           |  65.30 MiB (1%) |     2089296 |

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
  CPU: Intel(R) Xeon(R) CPU E5-2673 v4 @ 2.30GHz: 
              speed         user         nice          sys         idle          irq
       #1  2294 MHz      46616 s          0 s       2358 s      25245 s          0 s
       #2  2294 MHz      54954 s          0 s       2715 s      16870 s          0 s
       
  Memory: 6.764881134033203 GB (2952.10546875 MB free)
  Uptime: 761.0 sec
  Load Avg:  1.6767578125  1.54931640625  0.974609375
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-8.0.1 (ORCJIT, broadwell)
```

---
# Baseline result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmark: 6 Aug 2020 - 15:34
* Package commit: 76f082
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
| `["collect", "assoc", "basesize=1"]`                | 303.695 ms (5%) | 12.358 ms |  87.55 MiB (1%) |     1590789 |
| `["collect", "assoc", "basesize=1024"]`             | 166.744 ms (5%) |           |   1.84 MiB (1%) |        1812 |
| `["collect", "assoc", "basesize=32"]`               | 171.332 ms (5%) |           |   5.64 MiB (1%) |       54011 |
| `["collect", "seq"]`                                | 324.415 ms (5%) |           |   1.50 MiB (1%) |       32784 |
| `["collect", "unordered", "basesize=1"]`            | 410.656 ms (5%) |           |  29.19 MiB (1%) |      404971 |
| `["collect", "unordered", "basesize=1024"]`         | 192.654 ms (5%) |           | 795.39 KiB (1%) |        3616 |
| `["collect", "unordered", "basesize=32"]`           | 191.948 ms (5%) |           |   1.50 MiB (1%) |       18825 |
| `["findfirst", "n=1000", "foldl"]`                  | 530.805 ms (5%) |           |                 |             |
| `["findfirst", "n=1000", "reduce", "basesize=128"]` | 274.464 ms (5%) |           | 564.16 KiB (1%) |       10233 |
| `["findfirst", "n=1000", "reduce", "basesize=256"]` | 273.201 ms (5%) |           | 287.20 KiB (1%) |        5219 |
| `["findfirst", "n=1000", "reduce", "basesize=512"]` | 275.011 ms (5%) |           | 149.36 KiB (1%) |        2724 |
| `["findfirst", "n=400", "foldl"]`                   | 402.911 ms (5%) |           |                 |             |
| `["findfirst", "n=400", "reduce", "basesize=128"]`  | 207.602 ms (5%) |           |   1.02 MiB (1%) |       18983 |
| `["findfirst", "n=400", "reduce", "basesize=256"]`  | 202.195 ms (5%) |           | 526.34 KiB (1%) |        9582 |
| `["findfirst", "n=400", "reduce", "basesize=512"]`  | 207.057 ms (5%) |           | 267.36 KiB (1%) |        4884 |
| `["findfirst", "n=500", "foldl"]`                   |  66.873 ms (5%) |           |                 |             |
| `["findfirst", "n=500", "reduce", "basesize=128"]`  |  35.407 ms (5%) |           | 157.50 KiB (1%) |        2857 |
| `["findfirst", "n=500", "reduce", "basesize=256"]`  |  34.840 ms (5%) |           |  84.63 KiB (1%) |        1538 |
| `["findfirst", "n=500", "reduce", "basesize=512"]`  |  37.205 ms (5%) |           |  48.33 KiB (1%) |         880 |
| `["overhead", "default"]`                           | 188.100 μs (5%) |           | 146.27 KiB (1%) |        2633 |
| `["overhead", "stoppable=false"]`                   | 187.300 μs (5%) |           | 146.27 KiB (1%) |        2632 |
| `["overhead", "stoppable=true"]`                    | 309.301 μs (5%) |           | 146.55 KiB (1%) |        2650 |
| `["parallel_histogram", "assoc", "basesize=16384"]` |   3.896 ms (5%) |           | 732.06 KiB (1%) |         103 |
| `["parallel_histogram", "assoc", "basesize=4096"]`  |   4.615 ms (5%) |           |   2.07 MiB (1%) |         503 |
| `["parallel_histogram", "assoc", "basesize=8192"]`  |   4.239 ms (5%) |           |   1.43 MiB (1%) |         242 |
| `["parallel_histogram", "comm", "basesize=16384"]`  |  12.335 ms (5%) |           |   1.22 MiB (1%) |         159 |
| `["parallel_histogram", "comm", "basesize=4096"]`   |  19.334 ms (5%) |           |   1.04 MiB (1%) |        4313 |
| `["parallel_histogram", "comm", "basesize=8192"]`   |  16.727 ms (5%) |           |   1.23 MiB (1%) |         465 |
| `["parallel_histogram", "seq"]`                     |   6.854 ms (5%) |           | 364.61 KiB (1%) |          24 |
| `["sum", "random", "foldl"]`                        |  12.622 ms (5%) |           |   64 bytes (1%) |           3 |
| `["sum", "random", "reduce", "basesize=128"]`       |   7.020 ms (5%) |           | 313.41 KiB (1%) |        6070 |
| `["sum", "random", "reduce", "basesize=256"]`       |   6.840 ms (5%) |           | 155.13 KiB (1%) |        3011 |
| `["sum", "random", "reduce", "basesize=512"]`       |   6.667 ms (5%) |           |  76.31 KiB (1%) |        1486 |
| `["sum", "uniform", "foldl"]`                       |  12.315 ms (5%) |           |   64 bytes (1%) |           3 |
| `["sum", "uniform", "reduce", "basesize=128"]`      |   6.881 ms (5%) |           | 313.42 KiB (1%) |        6071 |
| `["sum", "uniform", "reduce", "basesize=256"]`      |   6.689 ms (5%) |           | 155.09 KiB (1%) |        3009 |
| `["sum", "uniform", "reduce", "basesize=512"]`      |   6.542 ms (5%) |           |  76.30 KiB (1%) |        1485 |
| `["sum", "valley", "foldl"]`                        |  12.916 ms (5%) |           |   64 bytes (1%) |           3 |
| `["sum", "valley", "reduce", "basesize=128"]`       |   7.147 ms (5%) |           | 313.34 KiB (1%) |        6066 |
| `["sum", "valley", "reduce", "basesize=256"]`       |   6.934 ms (5%) |           | 155.16 KiB (1%) |        3013 |
| `["sum", "valley", "reduce", "basesize=512"]`       |   6.842 ms (5%) |           |  76.33 KiB (1%) |        1487 |
| `["words", "nthreads=1"]`                           |  37.390 ms (5%) |  8.078 ms |  63.09 MiB (1%) |     2061200 |
| `["words", "nthreads=2"]`                           |  17.859 ms (5%) |           |  63.70 MiB (1%) |     2069351 |
| `["words", "nthreads=4"]`                           |  18.896 ms (5%) |           |  64.97 MiB (1%) |     2081859 |

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
  CPU: Intel(R) Xeon(R) CPU E5-2673 v4 @ 2.30GHz: 
              speed         user         nice          sys         idle          irq
       #1  2294 MHz      68159 s          0 s       2948 s      32252 s          0 s
       #2  2294 MHz      78404 s          0 s       3271 s      22098 s          0 s
       
  Memory: 6.764881134033203 GB (3001.0625 MB free)
  Uptime: 1054.0 sec
  Load Avg:  1.7822265625  1.63671875  1.1650390625
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-8.0.1 (ORCJIT, broadwell)
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
    Model:               79
    Model name:          Intel(R) Xeon(R) CPU E5-2673 v4 @ 2.30GHz
    Stepping:            1
    CPU MHz:             2294.686
    BogoMIPS:            4589.37
    Hypervisor vendor:   Microsoft
    Virtualization type: full
    L1d cache:           32K
    L1i cache:           32K
    L2 cache:            256K
    L3 cache:            51200K
    NUMA node0 CPU(s):   0,1
    Flags:               fpu vme de pse tsc msr pae mce cx8 apic sep mtrr pge mca cmov pat pse36 clflush mmx fxsr sse sse2 ss ht syscall nx pdpe1gb rdtscp lm constant_tsc rep_good nopl xtopology cpuid pni pclmulqdq ssse3 fma cx16 pcid sse4_1 sse4_2 movbe popcnt aes xsave avx f16c rdrand hypervisor lahf_lm abm 3dnowprefetch invpcid_single pti fsgsbase bmi1 hle avx2 smep bmi2 erms invpcid rtm rdseed adx smap xsaveopt md_clear
    

| Cpu Property       | Value                                                   |
|:------------------ |:------------------------------------------------------- |
| Brand              | Intel(R) Xeon(R) CPU E5-2673 v4 @ 2.30GHz               |
| Vendor             | :Intel                                                  |
| Architecture       | :Broadwell                                              |
| Model              | Family: 0x06, Model: 0x4f, Stepping: 0x01, Type: 0x00   |
| Cores              | 2 physical cores, 2 logical cores (on executing CPU)    |
|                    | No Hyperthreading detected                              |
| Clock Frequencies  | Not supported by CPU                                    |
| Data Cache         | Level 1:3 : (32, 256, 51200) kbytes                     |
|                    | 64 byte cache line size                                 |
| Address Size       | 48 bits virtual, 44 bits physical                       |
| SIMD               | 256 bit = 32 byte max. SIMD vector size                 |
| Time Stamp Counter | TSC is accessible via `rdtsc`                           |
|                    | TSC increased at every clock cycle (non-invariant TSC)  |
| Perf. Monitoring   | Performance Monitoring Counters (PMC) are not supported |
| Hypervisor         | Yes, Microsoft                                          |

