# Multi-thread benchmark result

* Pull request commit: [`d6a738272f10b332fd9fa855198ec18485a920c5`](https://github.com/JuliaFolds/Transducers.jl/commit/d6a738272f10b332fd9fa855198ec18485a920c5)
* Pull request: <https://github.com/JuliaFolds/Transducers.jl/pull/397> (Define collect(::Foldable) rather than collect(::Eduction))

# Judge result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmarks:
    - Target: 6 Aug 2020 - 17:13
    - Baseline: 6 Aug 2020 - 17:18
* Package commits:
    - Target: cd2770
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

| ID                                                  | time ratio                   | memory ratio                 |
|-----------------------------------------------------|------------------------------|------------------------------|
| `["collect", "unordered", "basesize=1024"]`         | 0.92 (5%) :white_check_mark: | 0.91 (1%) :white_check_mark: |
| `["words", "nthreads=2"]`                           |                   1.03 (5%)  |                1.01 (1%) :x: |

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
       #1  2095 MHz      54602 s          0 s       2369 s      40740 s          0 s
       #2  2095 MHz      48165 s          0 s       2445 s      47079 s          0 s
       
  Memory: 6.764881134033203 GB (2912.3828125 MB free)
  Uptime: 1000.0 sec
  Load Avg:  1.79248046875  1.5615234375  0.943359375
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
       #1  2095 MHz      77642 s          0 s       2964 s      47367 s          0 s
       #2  2095 MHz      71165 s          0 s       2897 s      53931 s          0 s
       
  Memory: 6.764881134033203 GB (2955.1328125 MB free)
  Uptime: 1305.0 sec
  Load Avg:  1.6396484375  1.5986328125  1.13330078125
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-8.0.1 (ORCJIT, skylake)
```

---
# Target result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmark: 6 Aug 2020 - 17:13
* Package commit: cd2770
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
| `["collect", "assoc", "basesize=1"]`                | 383.413 ms (5%) | 11.281 ms |  87.55 MiB (1%) |     1590790 |
| `["collect", "assoc", "basesize=1024"]`             | 241.652 ms (5%) |           |   1.84 MiB (1%) |        1812 |
| `["collect", "assoc", "basesize=32"]`               | 247.704 ms (5%) |           |   5.64 MiB (1%) |       54013 |
| `["collect", "seq"]`                                | 478.802 ms (5%) |           |   1.50 MiB (1%) |       32784 |
| `["collect", "unordered", "basesize=1"]`            | 503.830 ms (5%) |           |  29.16 MiB (1%) |      403329 |
| `["collect", "unordered", "basesize=1024"]`         | 321.227 ms (5%) |           | 835.05 KiB (1%) |        6535 |
| `["collect", "unordered", "basesize=32"]`           | 272.261 ms (5%) |           |   1.47 MiB (1%) |       16535 |
| `["findfirst", "n=1000", "foldl"]`                  | 762.343 ms (5%) |           |                 |             |
| `["findfirst", "n=1000", "reduce", "basesize=128"]` | 385.668 ms (5%) |           | 564.30 KiB (1%) |       10242 |
| `["findfirst", "n=1000", "reduce", "basesize=256"]` | 385.724 ms (5%) |           | 287.23 KiB (1%) |        5221 |
| `["findfirst", "n=1000", "reduce", "basesize=512"]` | 392.868 ms (5%) |           | 149.38 KiB (1%) |        2725 |
| `["findfirst", "n=400", "foldl"]`                   | 575.523 ms (5%) |           |                 |             |
| `["findfirst", "n=400", "reduce", "basesize=128"]`  | 290.966 ms (5%) |           |   1.02 MiB (1%) |       18972 |
| `["findfirst", "n=400", "reduce", "basesize=256"]`  | 287.388 ms (5%) |           | 526.22 KiB (1%) |        9574 |
| `["findfirst", "n=400", "reduce", "basesize=512"]`  | 292.149 ms (5%) |           | 267.23 KiB (1%) |        4876 |
| `["findfirst", "n=500", "foldl"]`                   |  96.996 ms (5%) |           |                 |             |
| `["findfirst", "n=500", "reduce", "basesize=128"]`  |  50.065 ms (5%) |           | 157.38 KiB (1%) |        2849 |
| `["findfirst", "n=500", "reduce", "basesize=256"]`  |  50.191 ms (5%) |           |  84.59 KiB (1%) |        1536 |
| `["findfirst", "n=500", "reduce", "basesize=512"]`  |  53.578 ms (5%) |           |  48.31 KiB (1%) |         879 |
| `["overhead", "default"]`                           | 204.710 μs (5%) |           | 146.27 KiB (1%) |        2633 |
| `["overhead", "stoppable=false"]`                   | 203.010 μs (5%) |           | 146.28 KiB (1%) |        2633 |
| `["overhead", "stoppable=true"]`                    | 368.818 μs (5%) |           | 146.53 KiB (1%) |        2649 |
| `["parallel_histogram", "assoc", "basesize=16384"]` |   5.256 ms (5%) |           | 732.06 KiB (1%) |         103 |
| `["parallel_histogram", "assoc", "basesize=4096"]`  |   6.053 ms (5%) |           |   1.80 MiB (1%) |         497 |
| `["parallel_histogram", "assoc", "basesize=8192"]`  |   5.540 ms (5%) |           |   1.43 MiB (1%) |         242 |
| `["parallel_histogram", "comm", "basesize=16384"]`  |  15.314 ms (5%) |           |   1.22 MiB (1%) |         159 |
| `["parallel_histogram", "comm", "basesize=4096"]`   |  23.462 ms (5%) |           |   1.06 MiB (1%) |        5360 |
| `["parallel_histogram", "comm", "basesize=8192"]`   |  20.274 ms (5%) |           |   1.23 MiB (1%) |        1066 |
| `["parallel_histogram", "seq"]`                     |   9.565 ms (5%) |           | 364.61 KiB (1%) |          24 |
| `["sum", "random", "foldl"]`                        |  18.778 ms (5%) |           |   64 bytes (1%) |           3 |
| `["sum", "random", "reduce", "basesize=128"]`       |  10.015 ms (5%) |           | 313.38 KiB (1%) |        6068 |
| `["sum", "random", "reduce", "basesize=256"]`       |   9.904 ms (5%) |           | 155.16 KiB (1%) |        3013 |
| `["sum", "random", "reduce", "basesize=512"]`       |   9.763 ms (5%) |           |  76.30 KiB (1%) |        1485 |
| `["sum", "uniform", "foldl"]`                       |  18.023 ms (5%) |           |   64 bytes (1%) |           3 |
| `["sum", "uniform", "reduce", "basesize=128"]`      |   9.640 ms (5%) |           | 313.42 KiB (1%) |        6071 |
| `["sum", "uniform", "reduce", "basesize=256"]`      |   9.499 ms (5%) |           | 155.16 KiB (1%) |        3013 |
| `["sum", "uniform", "reduce", "basesize=512"]`      |   9.300 ms (5%) |           |  76.31 KiB (1%) |        1486 |
| `["sum", "valley", "foldl"]`                        |  19.052 ms (5%) |           |   64 bytes (1%) |           3 |
| `["sum", "valley", "reduce", "basesize=128"]`       |  10.140 ms (5%) |           | 313.34 KiB (1%) |        6066 |
| `["sum", "valley", "reduce", "basesize=256"]`       |   9.955 ms (5%) |           | 155.14 KiB (1%) |        3012 |
| `["sum", "valley", "reduce", "basesize=512"]`       |   9.805 ms (5%) |           |  76.31 KiB (1%) |        1486 |
| `["words", "nthreads=1"]`                           |  38.370 ms (5%) |  7.549 ms |  63.21 MiB (1%) |     2065577 |
| `["words", "nthreads=2"]`                           |  20.032 ms (5%) |           |  64.29 MiB (1%) |     2077869 |
| `["words", "nthreads=4"]`                           |  20.410 ms (5%) |           |  64.93 MiB (1%) |     2084063 |

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
       #1  2095 MHz      54602 s          0 s       2369 s      40740 s          0 s
       #2  2095 MHz      48165 s          0 s       2445 s      47079 s          0 s
       
  Memory: 6.764881134033203 GB (2912.3828125 MB free)
  Uptime: 1000.0 sec
  Load Avg:  1.79248046875  1.5615234375  0.943359375
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-8.0.1 (ORCJIT, skylake)
```

---
# Baseline result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmark: 6 Aug 2020 - 17:18
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
| `["collect", "assoc", "basesize=1"]`                | 383.453 ms (5%) | 13.032 ms |  87.55 MiB (1%) |     1590730 |
| `["collect", "assoc", "basesize=1024"]`             | 242.860 ms (5%) |           |   1.84 MiB (1%) |        1811 |
| `["collect", "assoc", "basesize=32"]`               | 246.763 ms (5%) |           |   5.64 MiB (1%) |       54019 |
| `["collect", "seq"]`                                | 478.169 ms (5%) |           |   1.50 MiB (1%) |       32784 |
| `["collect", "unordered", "basesize=1"]`            | 511.763 ms (5%) |           |  29.16 MiB (1%) |      403403 |
| `["collect", "unordered", "basesize=1024"]`         | 349.212 ms (5%) |           | 914.13 KiB (1%) |       11260 |
| `["collect", "unordered", "basesize=32"]`           | 273.357 ms (5%) |           |   1.47 MiB (1%) |       16983 |
| `["findfirst", "n=1000", "foldl"]`                  | 763.569 ms (5%) |           |                 |             |
| `["findfirst", "n=1000", "reduce", "basesize=128"]` | 383.776 ms (5%) |           | 564.25 KiB (1%) |       10239 |
| `["findfirst", "n=1000", "reduce", "basesize=256"]` | 384.188 ms (5%) |           | 287.33 KiB (1%) |        5227 |
| `["findfirst", "n=1000", "reduce", "basesize=512"]` | 392.414 ms (5%) |           | 149.36 KiB (1%) |        2724 |
| `["findfirst", "n=400", "foldl"]`                   | 570.520 ms (5%) |           |                 |             |
| `["findfirst", "n=400", "reduce", "basesize=128"]`  | 288.581 ms (5%) |           |   1.02 MiB (1%) |       18961 |
| `["findfirst", "n=400", "reduce", "basesize=256"]`  | 286.783 ms (5%) |           | 526.30 KiB (1%) |        9579 |
| `["findfirst", "n=400", "reduce", "basesize=512"]`  | 289.657 ms (5%) |           | 267.30 KiB (1%) |        4880 |
| `["findfirst", "n=500", "foldl"]`                   |  98.454 ms (5%) |           |                 |             |
| `["findfirst", "n=500", "reduce", "basesize=128"]`  |  50.429 ms (5%) |           | 157.41 KiB (1%) |        2851 |
| `["findfirst", "n=500", "reduce", "basesize=256"]`  |  50.054 ms (5%) |           |  84.55 KiB (1%) |        1533 |
| `["findfirst", "n=500", "reduce", "basesize=512"]`  |  52.962 ms (5%) |           |  48.33 KiB (1%) |         880 |
| `["overhead", "default"]`                           | 201.616 μs (5%) |           | 146.27 KiB (1%) |        2633 |
| `["overhead", "stoppable=false"]`                   | 208.817 μs (5%) |           | 146.28 KiB (1%) |        2633 |
| `["overhead", "stoppable=true"]`                    | 356.228 μs (5%) |           | 146.55 KiB (1%) |        2650 |
| `["parallel_histogram", "assoc", "basesize=16384"]` |   5.271 ms (5%) |           | 732.06 KiB (1%) |         103 |
| `["parallel_histogram", "assoc", "basesize=4096"]`  |   6.112 ms (5%) |           |   1.80 MiB (1%) |         497 |
| `["parallel_histogram", "assoc", "basesize=8192"]`  |   5.712 ms (5%) |           |   1.43 MiB (1%) |         242 |
| `["parallel_histogram", "comm", "basesize=16384"]`  |  15.794 ms (5%) |           |   1.22 MiB (1%) |         159 |
| `["parallel_histogram", "comm", "basesize=4096"]`   |  23.124 ms (5%) |           |   1.07 MiB (1%) |        3207 |
| `["parallel_histogram", "comm", "basesize=8192"]`   |  19.338 ms (5%) |           |   1.24 MiB (1%) |        1549 |
| `["parallel_histogram", "seq"]`                     |   9.649 ms (5%) |           | 364.61 KiB (1%) |          24 |
| `["sum", "random", "foldl"]`                        |  18.537 ms (5%) |           |   64 bytes (1%) |           3 |
| `["sum", "random", "reduce", "basesize=128"]`       |  10.116 ms (5%) |           | 313.31 KiB (1%) |        6064 |
| `["sum", "random", "reduce", "basesize=256"]`       |   9.910 ms (5%) |           | 155.16 KiB (1%) |        3013 |
| `["sum", "random", "reduce", "basesize=512"]`       |   9.538 ms (5%) |           |  76.30 KiB (1%) |        1485 |
| `["sum", "uniform", "foldl"]`                       |  18.447 ms (5%) |           |   64 bytes (1%) |           3 |
| `["sum", "uniform", "reduce", "basesize=128"]`      |   9.834 ms (5%) |           | 313.41 KiB (1%) |        6070 |
| `["sum", "uniform", "reduce", "basesize=256"]`      |   9.611 ms (5%) |           | 155.17 KiB (1%) |        3014 |
| `["sum", "uniform", "reduce", "basesize=512"]`      |   9.420 ms (5%) |           |  76.31 KiB (1%) |        1486 |
| `["sum", "valley", "foldl"]`                        |  19.069 ms (5%) |           |   64 bytes (1%) |           3 |
| `["sum", "valley", "reduce", "basesize=128"]`       |  10.074 ms (5%) |           | 313.31 KiB (1%) |        6064 |
| `["sum", "valley", "reduce", "basesize=256"]`       |   9.987 ms (5%) |           | 155.16 KiB (1%) |        3013 |
| `["sum", "valley", "reduce", "basesize=512"]`       |   9.808 ms (5%) |           |  76.31 KiB (1%) |        1486 |
| `["words", "nthreads=1"]`                           |  38.557 ms (5%) |  7.612 ms |  62.92 MiB (1%) |     2056124 |
| `["words", "nthreads=2"]`                           |  19.521 ms (5%) |           |  63.53 MiB (1%) |     2064294 |
| `["words", "nthreads=4"]`                           |  20.111 ms (5%) |           |  64.49 MiB (1%) |     2072530 |

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
       #1  2095 MHz      77642 s          0 s       2964 s      47367 s          0 s
       #2  2095 MHz      71165 s          0 s       2897 s      53931 s          0 s
       
  Memory: 6.764881134033203 GB (2955.1328125 MB free)
  Uptime: 1305.0 sec
  Load Avg:  1.6396484375  1.5986328125  1.13330078125
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
    CPU MHz:             2095.228
    BogoMIPS:            4190.45
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

