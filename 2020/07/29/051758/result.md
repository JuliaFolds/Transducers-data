# Multi-thread benchmark result

* Pull request commit: [`161879165f8484d866dc83bf0345fa6e2e034ef9`](https://github.com/JuliaFolds/Transducers.jl/commit/161879165f8484d866dc83bf0345fa6e2e034ef9)
* Pull request: <https://github.com/JuliaFolds/Transducers.jl/pull/384> (Call BenchmarkCI.pushresult on Travis)

# Judge result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmarks:
    - Target: 29 Jul 2020 - 05:12
    - Baseline: 29 Jul 2020 - 05:17
* Package commits:
    - Target: 8f761d
    - Baseline: e71b71
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
| `["collect", "unordered", "basesize=1024"]`         |                1.09 (5%) :x: |                1.07 (1%) :x: |
| `["parallel_histogram", "comm", "basesize=4096"]`   |                1.14 (5%) :x: |                   1.00 (1%)  |
| `["parallel_histogram", "comm", "basesize=8192"]`   | 0.94 (5%) :white_check_mark: | 0.98 (1%) :white_check_mark: |

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
  uname: Linux 5.3.0-1032-azure #33~18.04.1-Ubuntu SMP Fri Jun 26 15:01:15 UTC 2020 x86_64 x86_64
  CPU: Intel(R) Xeon(R) Platinum 8171M CPU @ 2.60GHz: 
              speed         user         nice          sys         idle          irq
       #1  2095 MHz      54380 s          0 s       2368 s      25279 s          0 s
       #2  2095 MHz      47957 s          0 s       2394 s      31369 s          0 s
       
  Memory: 6.764884948730469 GB (2985.30078125 MB free)
  Uptime: 840.0 sec
  Load Avg:  1.60107421875  1.45166015625  0.86669921875
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
  uname: Linux 5.3.0-1032-azure #33~18.04.1-Ubuntu SMP Fri Jun 26 15:01:15 UTC 2020 x86_64 x86_64
  CPU: Intel(R) Xeon(R) Platinum 8171M CPU @ 2.60GHz: 
              speed         user         nice          sys         idle          irq
       #1  2095 MHz      74807 s          0 s       2819 s      34917 s          0 s
       #2  2095 MHz      74101 s          0 s       2839 s      35173 s          0 s
       
  Memory: 6.764884948730469 GB (3005.26953125 MB free)
  Uptime: 1147.0 sec
  Load Avg:  1.65625  1.53369140625  1.07177734375
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-8.0.1 (ORCJIT, skylake)
```

---
# Target result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmark: 29 Jul 2020 - 5:12
* Package commit: 8f761d
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
| `["collect", "assoc", "basesize=1"]`                | 384.647 ms (5%) | 11.883 ms |  87.55 MiB (1%) |     1590719 |
| `["collect", "assoc", "basesize=1024"]`             | 240.658 ms (5%) |           |   1.84 MiB (1%) |        1811 |
| `["collect", "assoc", "basesize=32"]`               | 245.936 ms (5%) |           |   5.64 MiB (1%) |       54023 |
| `["collect", "seq"]`                                | 476.917 ms (5%) |           |   1.50 MiB (1%) |       32784 |
| `["collect", "unordered", "basesize=1"]`            | 506.432 ms (5%) |           |  29.15 MiB (1%) |      402504 |
| `["collect", "unordered", "basesize=1024"]`         | 375.710 ms (5%) |           | 928.53 KiB (1%) |       12518 |
| `["collect", "unordered", "basesize=32"]`           | 275.006 ms (5%) |           |   1.47 MiB (1%) |       16794 |
| `["findfirst", "n=1000", "foldl"]`                  | 757.481 ms (5%) |           |                 |             |
| `["findfirst", "n=1000", "reduce", "basesize=128"]` | 384.805 ms (5%) |           | 563.69 KiB (1%) |       10207 |
| `["findfirst", "n=1000", "reduce", "basesize=256"]` | 384.096 ms (5%) |           | 287.11 KiB (1%) |        5217 |
| `["findfirst", "n=1000", "reduce", "basesize=512"]` | 392.582 ms (5%) |           | 149.25 KiB (1%) |        2721 |
| `["findfirst", "n=400", "foldl"]`                   | 574.487 ms (5%) |           |                 |             |
| `["findfirst", "n=400", "reduce", "basesize=128"]`  | 290.884 ms (5%) |           |   1.02 MiB (1%) |       18942 |
| `["findfirst", "n=400", "reduce", "basesize=256"]`  | 288.037 ms (5%) |           | 526.22 KiB (1%) |        9578 |
| `["findfirst", "n=400", "reduce", "basesize=512"]`  | 289.489 ms (5%) |           | 267.17 KiB (1%) |        4876 |
| `["findfirst", "n=500", "foldl"]`                   |  97.228 ms (5%) |           |                 |             |
| `["findfirst", "n=500", "reduce", "basesize=128"]`  |  50.489 ms (5%) |           | 157.22 KiB (1%) |        2843 |
| `["findfirst", "n=500", "reduce", "basesize=256"]`  |  49.910 ms (5%) |           |  84.44 KiB (1%) |        1530 |
| `["findfirst", "n=500", "reduce", "basesize=512"]`  |  53.189 ms (5%) |           |  48.17 KiB (1%) |         874 |
| `["overhead", "default"]`                           | 210.710 μs (5%) |           | 146.14 KiB (1%) |        2628 |
| `["overhead", "stoppable=false"]`                   | 208.810 μs (5%) |           | 146.11 KiB (1%) |        2626 |
| `["overhead", "stoppable=true"]`                    | 370.219 μs (5%) |           | 146.42 KiB (1%) |        2646 |
| `["parallel_histogram", "assoc", "basesize=16384"]` |   5.261 ms (5%) |           | 732.02 KiB (1%) |         101 |
| `["parallel_histogram", "assoc", "basesize=4096"]`  |   6.000 ms (5%) |           |   1.80 MiB (1%) |         495 |
| `["parallel_histogram", "assoc", "basesize=8192"]`  |   5.700 ms (5%) |           |   1.43 MiB (1%) |         240 |
| `["parallel_histogram", "comm", "basesize=16384"]`  |  15.995 ms (5%) |           |   1.22 MiB (1%) |         159 |
| `["parallel_histogram", "comm", "basesize=4096"]`   |  26.079 ms (5%) |           |   1.07 MiB (1%) |        4926 |
| `["parallel_histogram", "comm", "basesize=8192"]`   |  19.246 ms (5%) |           |   1.22 MiB (1%) |         171 |
| `["parallel_histogram", "seq"]`                     |   9.288 ms (5%) |           | 364.61 KiB (1%) |          24 |
| `["sum", "random", "foldl"]`                        |  18.537 ms (5%) |           |   64 bytes (1%) |           3 |
| `["sum", "random", "reduce", "basesize=128"]`       |   9.909 ms (5%) |           | 313.33 KiB (1%) |        6067 |
| `["sum", "random", "reduce", "basesize=256"]`       |   9.689 ms (5%) |           | 155.08 KiB (1%) |        3010 |
| `["sum", "random", "reduce", "basesize=512"]`       |   9.438 ms (5%) |           |  76.23 KiB (1%) |        1483 |
| `["sum", "uniform", "foldl"]`                       |  18.063 ms (5%) |           |   64 bytes (1%) |           3 |
| `["sum", "uniform", "reduce", "basesize=128"]`      |   9.810 ms (5%) |           | 313.30 KiB (1%) |        6065 |
| `["sum", "uniform", "reduce", "basesize=256"]`      |   9.563 ms (5%) |           | 155.09 KiB (1%) |        3011 |
| `["sum", "uniform", "reduce", "basesize=512"]`      |   9.493 ms (5%) |           |  76.25 KiB (1%) |        1484 |
| `["sum", "valley", "foldl"]`                        |  18.758 ms (5%) |           |   64 bytes (1%) |           3 |
| `["sum", "valley", "reduce", "basesize=128"]`       |  10.103 ms (5%) |           | 313.27 KiB (1%) |        6063 |
| `["sum", "valley", "reduce", "basesize=256"]`       |   9.653 ms (5%) |           | 155.06 KiB (1%) |        3009 |
| `["sum", "valley", "reduce", "basesize=512"]`       |   9.711 ms (5%) |           |  76.25 KiB (1%) |        1484 |
| `["words", "nthreads=1"]`                           |  50.656 ms (5%) |  7.938 ms |  63.08 MiB (1%) |     2061091 |
| `["words", "nthreads=2"]`                           |  25.699 ms (5%) |           |  64.17 MiB (1%) |     2073351 |
| `["words", "nthreads=4"]`                           |  26.797 ms (5%) |           |  65.11 MiB (1%) |     2083712 |

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
  uname: Linux 5.3.0-1032-azure #33~18.04.1-Ubuntu SMP Fri Jun 26 15:01:15 UTC 2020 x86_64 x86_64
  CPU: Intel(R) Xeon(R) Platinum 8171M CPU @ 2.60GHz: 
              speed         user         nice          sys         idle          irq
       #1  2095 MHz      54380 s          0 s       2368 s      25279 s          0 s
       #2  2095 MHz      47957 s          0 s       2394 s      31369 s          0 s
       
  Memory: 6.764884948730469 GB (2985.30078125 MB free)
  Uptime: 840.0 sec
  Load Avg:  1.60107421875  1.45166015625  0.86669921875
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-8.0.1 (ORCJIT, skylake)
```

---
# Baseline result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmark: 29 Jul 2020 - 5:17
* Package commit: e71b71
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
| `["collect", "assoc", "basesize=1"]`                | 382.489 ms (5%) | 11.468 ms |  87.55 MiB (1%) |     1590707 |
| `["collect", "assoc", "basesize=1024"]`             | 240.804 ms (5%) |           |   1.84 MiB (1%) |        1808 |
| `["collect", "assoc", "basesize=32"]`               | 246.457 ms (5%) |           |   5.64 MiB (1%) |       54009 |
| `["collect", "seq"]`                                | 477.439 ms (5%) |           |   1.50 MiB (1%) |       32784 |
| `["collect", "unordered", "basesize=1"]`            | 501.318 ms (5%) |           |  29.17 MiB (1%) |      403781 |
| `["collect", "unordered", "basesize=1024"]`         | 343.783 ms (5%) |           | 869.67 KiB (1%) |        8415 |
| `["collect", "unordered", "basesize=32"]`           | 271.439 ms (5%) |           |   1.47 MiB (1%) |       16761 |
| `["findfirst", "n=1000", "foldl"]`                  | 756.915 ms (5%) |           |                 |             |
| `["findfirst", "n=1000", "reduce", "basesize=128"]` | 383.039 ms (5%) |           | 563.78 KiB (1%) |       10213 |
| `["findfirst", "n=1000", "reduce", "basesize=256"]` | 380.948 ms (5%) |           | 287.25 KiB (1%) |        5226 |
| `["findfirst", "n=1000", "reduce", "basesize=512"]` | 386.235 ms (5%) |           | 149.28 KiB (1%) |        2723 |
| `["findfirst", "n=400", "foldl"]`                   | 565.247 ms (5%) |           |                 |             |
| `["findfirst", "n=400", "reduce", "basesize=128"]`  | 288.253 ms (5%) |           |   1.02 MiB (1%) |       18929 |
| `["findfirst", "n=400", "reduce", "basesize=256"]`  | 287.205 ms (5%) |           | 526.14 KiB (1%) |        9573 |
| `["findfirst", "n=400", "reduce", "basesize=512"]`  | 288.626 ms (5%) |           | 267.11 KiB (1%) |        4872 |
| `["findfirst", "n=500", "foldl"]`                   |  97.518 ms (5%) |           |                 |             |
| `["findfirst", "n=500", "reduce", "basesize=128"]`  |  50.250 ms (5%) |           | 157.31 KiB (1%) |        2849 |
| `["findfirst", "n=500", "reduce", "basesize=256"]`  |  49.961 ms (5%) |           |  84.44 KiB (1%) |        1530 |
| `["findfirst", "n=500", "reduce", "basesize=512"]`  |  52.814 ms (5%) |           |  48.20 KiB (1%) |         876 |
| `["overhead", "default"]`                           | 208.619 μs (5%) |           | 146.14 KiB (1%) |        2628 |
| `["overhead", "stoppable=false"]`                   | 208.519 μs (5%) |           | 146.16 KiB (1%) |        2629 |
| `["overhead", "stoppable=true"]`                    | 388.934 μs (5%) |           | 146.42 KiB (1%) |        2646 |
| `["parallel_histogram", "assoc", "basesize=16384"]` |   5.155 ms (5%) |           | 732.02 KiB (1%) |         101 |
| `["parallel_histogram", "assoc", "basesize=4096"]`  |   5.966 ms (5%) |           |   1.80 MiB (1%) |         495 |
| `["parallel_histogram", "assoc", "basesize=8192"]`  |   5.613 ms (5%) |           |   1.43 MiB (1%) |         241 |
| `["parallel_histogram", "comm", "basesize=16384"]`  |  15.688 ms (5%) |           |   1.22 MiB (1%) |         159 |
| `["parallel_histogram", "comm", "basesize=4096"]`   |  22.974 ms (5%) |           |   1.07 MiB (1%) |        3496 |
| `["parallel_histogram", "comm", "basesize=8192"]`   |  20.380 ms (5%) |           |   1.25 MiB (1%) |        2020 |
| `["parallel_histogram", "seq"]`                     |   9.557 ms (5%) |           | 364.61 KiB (1%) |          24 |
| `["sum", "random", "foldl"]`                        |  19.072 ms (5%) |           |   64 bytes (1%) |           3 |
| `["sum", "random", "reduce", "basesize=128"]`       |   9.881 ms (5%) |           | 313.34 KiB (1%) |        6068 |
| `["sum", "random", "reduce", "basesize=256"]`       |   9.699 ms (5%) |           | 155.08 KiB (1%) |        3010 |
| `["sum", "random", "reduce", "basesize=512"]`       |   9.713 ms (5%) |           |  76.25 KiB (1%) |        1484 |
| `["sum", "uniform", "foldl"]`                       |  17.977 ms (5%) |           |   64 bytes (1%) |           3 |
| `["sum", "uniform", "reduce", "basesize=128"]`      |   9.666 ms (5%) |           | 313.34 KiB (1%) |        6068 |
| `["sum", "uniform", "reduce", "basesize=256"]`      |   9.617 ms (5%) |           | 155.08 KiB (1%) |        3010 |
| `["sum", "uniform", "reduce", "basesize=512"]`      |   9.344 ms (5%) |           |  76.25 KiB (1%) |        1484 |
| `["sum", "valley", "foldl"]`                        |  19.183 ms (5%) |           |   64 bytes (1%) |           3 |
| `["sum", "valley", "reduce", "basesize=128"]`       |   9.882 ms (5%) |           | 313.27 KiB (1%) |        6063 |
| `["sum", "valley", "reduce", "basesize=256"]`       |   9.862 ms (5%) |           | 155.08 KiB (1%) |        3010 |
| `["sum", "valley", "reduce", "basesize=512"]`       |   9.711 ms (5%) |           |  76.25 KiB (1%) |        1484 |
| `["words", "nthreads=1"]`                           |  51.645 ms (5%) |  7.882 ms |  63.17 MiB (1%) |     2063880 |
| `["words", "nthreads=2"]`                           |  24.643 ms (5%) |           |  63.77 MiB (1%) |     2071983 |
| `["words", "nthreads=4"]`                           |  25.811 ms (5%) |           |  64.74 MiB (1%) |     2080218 |

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
  uname: Linux 5.3.0-1032-azure #33~18.04.1-Ubuntu SMP Fri Jun 26 15:01:15 UTC 2020 x86_64 x86_64
  CPU: Intel(R) Xeon(R) Platinum 8171M CPU @ 2.60GHz: 
              speed         user         nice          sys         idle          irq
       #1  2095 MHz      74807 s          0 s       2819 s      34917 s          0 s
       #2  2095 MHz      74101 s          0 s       2839 s      35173 s          0 s
       
  Memory: 6.764884948730469 GB (3005.26953125 MB free)
  Uptime: 1147.0 sec
  Load Avg:  1.65625  1.53369140625  1.07177734375
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
    CPU MHz:             2095.198
    BogoMIPS:            4190.39
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

