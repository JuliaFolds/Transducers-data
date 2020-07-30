# Multi-thread benchmark result

* Pull request commit: [`246886f6307aebe4936e62119b5aa0e598de7428`](https://github.com/JuliaFolds/Transducers.jl/commit/246886f6307aebe4936e62119b5aa0e598de7428)
* Pull request: <https://github.com/JuliaFolds/Transducers.jl/pull/387> (Add KeepSomething; deprecate Keep)

# Judge result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmarks:
    - Target: 30 Jul 2020 - 17:45
    - Baseline: 30 Jul 2020 - 17:50
* Package commits:
    - Target: d361e7
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

| ID                                                  | time ratio                   | memory ratio                 |
|-----------------------------------------------------|------------------------------|------------------------------|
| `["collect", "unordered", "basesize=1024"]`         | 0.81 (5%) :white_check_mark: | 0.88 (1%) :white_check_mark: |
| `["overhead", "default"]`                           | 0.93 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["overhead", "stoppable=true"]`                    |                1.08 (5%) :x: |                   1.00 (1%)  |
| `["parallel_histogram", "comm", "basesize=4096"]`   |                   1.00 (5%)  | 0.99 (1%) :white_check_mark: |
| `["parallel_histogram", "comm", "basesize=8192"]`   | 0.94 (5%) :white_check_mark: |                   1.01 (1%)  |

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
  CPU: Intel(R) Xeon(R) CPU E5-2673 v4 @ 2.30GHz: 
              speed         user         nice          sys         idle          irq
       #1  2294 MHz      50428 s          0 s       2516 s      19043 s          0 s
       #2  2294 MHz      52624 s          0 s       2640 s      16551 s          0 s
       
  Memory: 6.764884948730469 GB (2983.25 MB free)
  Uptime: 739.0 sec
  Load Avg:  1.76123046875  1.57080078125  0.9560546875
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
  uname: Linux 5.3.0-1032-azure #33~18.04.1-Ubuntu SMP Fri Jun 26 15:01:15 UTC 2020 x86_64 x86_64
  CPU: Intel(R) Xeon(R) CPU E5-2673 v4 @ 2.30GHz: 
              speed         user         nice          sys         idle          irq
       #1  2294 MHz      76163 s          0 s       3073 s      22760 s          0 s
       #2  2294 MHz      72882 s          0 s       3254 s      25690 s          0 s
       
  Memory: 6.764884948730469 GB (2988.046875 MB free)
  Uptime: 1042.0 sec
  Load Avg:  1.60888671875  1.58935546875  1.1376953125
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-8.0.1 (ORCJIT, broadwell)
```

---
# Target result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmark: 30 Jul 2020 - 17:45
* Package commit: d361e7
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
| `["collect", "assoc", "basesize=1"]`                | 336.094 ms (5%) | 11.856 ms |  87.55 MiB (1%) |     1590700 |
| `["collect", "assoc", "basesize=1024"]`             | 181.492 ms (5%) |           |   1.84 MiB (1%) |        1813 |
| `["collect", "assoc", "basesize=32"]`               | 186.726 ms (5%) |           |   5.64 MiB (1%) |       54010 |
| `["collect", "seq"]`                                | 359.371 ms (5%) |           |   1.50 MiB (1%) |       32784 |
| `["collect", "unordered", "basesize=1"]`            | 447.805 ms (5%) |           |  29.19 MiB (1%) |      405459 |
| `["collect", "unordered", "basesize=1024"]`         | 237.923 ms (5%) |           | 812.16 KiB (1%) |        5025 |
| `["collect", "unordered", "basesize=32"]`           | 217.564 ms (5%) |           |   1.50 MiB (1%) |       18752 |
| `["findfirst", "n=1000", "foldl"]`                  | 590.870 ms (5%) |           |                 |             |
| `["findfirst", "n=1000", "reduce", "basesize=128"]` | 303.439 ms (5%) |           | 564.13 KiB (1%) |       10235 |
| `["findfirst", "n=1000", "reduce", "basesize=256"]` | 300.395 ms (5%) |           | 287.23 KiB (1%) |        5225 |
| `["findfirst", "n=1000", "reduce", "basesize=512"]` | 305.976 ms (5%) |           | 149.23 KiB (1%) |        2720 |
| `["findfirst", "n=400", "foldl"]`                   | 434.115 ms (5%) |           |                 |             |
| `["findfirst", "n=400", "reduce", "basesize=128"]`  | 228.220 ms (5%) |           |   1.02 MiB (1%) |       18970 |
| `["findfirst", "n=400", "reduce", "basesize=256"]`  | 224.885 ms (5%) |           | 526.13 KiB (1%) |        9572 |
| `["findfirst", "n=400", "reduce", "basesize=512"]`  | 225.481 ms (5%) |           | 267.20 KiB (1%) |        4878 |
| `["findfirst", "n=500", "foldl"]`                   |  73.566 ms (5%) |           |                 |             |
| `["findfirst", "n=500", "reduce", "basesize=128"]`  |  38.751 ms (5%) |           | 157.34 KiB (1%) |        2851 |
| `["findfirst", "n=500", "reduce", "basesize=256"]`  |  38.268 ms (5%) |           |  84.47 KiB (1%) |        1532 |
| `["findfirst", "n=500", "reduce", "basesize=512"]`  |  39.648 ms (5%) |           |  48.16 KiB (1%) |         873 |
| `["overhead", "default"]`                           | 173.300 μs (5%) |           | 146.16 KiB (1%) |        2629 |
| `["overhead", "stoppable=false"]`                   | 188.500 μs (5%) |           | 146.14 KiB (1%) |        2628 |
| `["overhead", "stoppable=true"]`                    | 349.601 μs (5%) |           | 146.38 KiB (1%) |        2643 |
| `["parallel_histogram", "assoc", "basesize=16384"]` |   3.932 ms (5%) |           | 732.02 KiB (1%) |         101 |
| `["parallel_histogram", "assoc", "basesize=4096"]`  |   4.825 ms (5%) |           |   1.80 MiB (1%) |         495 |
| `["parallel_histogram", "assoc", "basesize=8192"]`  |   4.322 ms (5%) |           |   1.43 MiB (1%) |         241 |
| `["parallel_histogram", "comm", "basesize=16384"]`  |  13.379 ms (5%) |           |   1.22 MiB (1%) |         316 |
| `["parallel_histogram", "comm", "basesize=4096"]`   |  20.891 ms (5%) |           |   1.04 MiB (1%) |        4209 |
| `["parallel_histogram", "comm", "basesize=8192"]`   |  16.297 ms (5%) |           |   1.23 MiB (1%) |         973 |
| `["parallel_histogram", "seq"]`                     |   7.068 ms (5%) |           | 364.61 KiB (1%) |          24 |
| `["sum", "random", "foldl"]`                        |  13.680 ms (5%) |           |   64 bytes (1%) |           3 |
| `["sum", "random", "reduce", "basesize=128"]`       |   7.359 ms (5%) |           | 313.34 KiB (1%) |        6068 |
| `["sum", "random", "reduce", "basesize=256"]`       |   7.020 ms (5%) |           | 155.06 KiB (1%) |        3009 |
| `["sum", "random", "reduce", "basesize=512"]`       |   6.928 ms (5%) |           |  76.27 KiB (1%) |        1485 |
| `["sum", "uniform", "foldl"]`                       |  13.352 ms (5%) |           |   64 bytes (1%) |           3 |
| `["sum", "uniform", "reduce", "basesize=128"]`      |   7.276 ms (5%) |           | 313.38 KiB (1%) |        6070 |
| `["sum", "uniform", "reduce", "basesize=256"]`      |   6.731 ms (5%) |           | 155.08 KiB (1%) |        3010 |
| `["sum", "uniform", "reduce", "basesize=512"]`      |   6.734 ms (5%) |           |  76.25 KiB (1%) |        1484 |
| `["sum", "valley", "foldl"]`                        |  13.827 ms (5%) |           |   64 bytes (1%) |           3 |
| `["sum", "valley", "reduce", "basesize=128"]`       |   7.354 ms (5%) |           | 313.27 KiB (1%) |        6063 |
| `["sum", "valley", "reduce", "basesize=256"]`       |   7.047 ms (5%) |           | 155.08 KiB (1%) |        3010 |
| `["sum", "valley", "reduce", "basesize=512"]`       |   6.953 ms (5%) |           |  76.27 KiB (1%) |        1485 |
| `["words", "nthreads=1"]`                           |  50.628 ms (5%) |  7.830 ms |  63.39 MiB (1%) |     2071338 |
| `["words", "nthreads=2"]`                           |  25.758 ms (5%) |           |  64.00 MiB (1%) |     2079495 |
| `["words", "nthreads=4"]`                           |  27.703 ms (5%) |           |  64.96 MiB (1%) |     2087747 |

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
  CPU: Intel(R) Xeon(R) CPU E5-2673 v4 @ 2.30GHz: 
              speed         user         nice          sys         idle          irq
       #1  2294 MHz      50428 s          0 s       2516 s      19043 s          0 s
       #2  2294 MHz      52624 s          0 s       2640 s      16551 s          0 s
       
  Memory: 6.764884948730469 GB (2983.25 MB free)
  Uptime: 739.0 sec
  Load Avg:  1.76123046875  1.57080078125  0.9560546875
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-8.0.1 (ORCJIT, broadwell)
```

---
# Baseline result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmark: 30 Jul 2020 - 17:50
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
| `["collect", "assoc", "basesize=1"]`                | 332.612 ms (5%) | 12.690 ms |  87.55 MiB (1%) |     1590737 |
| `["collect", "assoc", "basesize=1024"]`             | 180.920 ms (5%) |           |   1.84 MiB (1%) |        1812 |
| `["collect", "assoc", "basesize=32"]`               | 183.679 ms (5%) |           |   5.64 MiB (1%) |       54015 |
| `["collect", "seq"]`                                | 358.771 ms (5%) |           |   1.50 MiB (1%) |       32784 |
| `["collect", "unordered", "basesize=1"]`            | 455.638 ms (5%) |           |  29.19 MiB (1%) |      405183 |
| `["collect", "unordered", "basesize=1024"]`         | 295.112 ms (5%) |           | 917.98 KiB (1%) |       11843 |
| `["collect", "unordered", "basesize=32"]`           | 216.371 ms (5%) |           |   1.50 MiB (1%) |       18797 |
| `["findfirst", "n=1000", "foldl"]`                  | 584.838 ms (5%) |           |                 |             |
| `["findfirst", "n=1000", "reduce", "basesize=128"]` | 300.058 ms (5%) |           | 564.06 KiB (1%) |       10231 |
| `["findfirst", "n=1000", "reduce", "basesize=256"]` | 294.498 ms (5%) |           | 287.20 KiB (1%) |        5223 |
| `["findfirst", "n=1000", "reduce", "basesize=512"]` | 305.596 ms (5%) |           | 149.23 KiB (1%) |        2720 |
| `["findfirst", "n=400", "foldl"]`                   | 435.712 ms (5%) |           |                 |             |
| `["findfirst", "n=400", "reduce", "basesize=128"]`  | 225.747 ms (5%) |           |   1.02 MiB (1%) |       18983 |
| `["findfirst", "n=400", "reduce", "basesize=256"]`  | 225.409 ms (5%) |           | 526.31 KiB (1%) |        9584 |
| `["findfirst", "n=400", "reduce", "basesize=512"]`  | 225.856 ms (5%) |           | 267.06 KiB (1%) |        4869 |
| `["findfirst", "n=500", "foldl"]`                   |  73.209 ms (5%) |           |                 |             |
| `["findfirst", "n=500", "reduce", "basesize=128"]`  |  37.917 ms (5%) |           | 157.39 KiB (1%) |        2854 |
| `["findfirst", "n=500", "reduce", "basesize=256"]`  |  38.185 ms (5%) |           |  84.48 KiB (1%) |        1533 |
| `["findfirst", "n=500", "reduce", "basesize=512"]`  |  40.526 ms (5%) |           |  48.20 KiB (1%) |         876 |
| `["overhead", "default"]`                           | 186.400 μs (5%) |           | 146.16 KiB (1%) |        2629 |
| `["overhead", "stoppable=false"]`                   | 189.600 μs (5%) |           | 146.16 KiB (1%) |        2629 |
| `["overhead", "stoppable=true"]`                    | 324.201 μs (5%) |           | 146.42 KiB (1%) |        2646 |
| `["parallel_histogram", "assoc", "basesize=16384"]` |   3.916 ms (5%) |           | 732.02 KiB (1%) |         101 |
| `["parallel_histogram", "assoc", "basesize=4096"]`  |   4.691 ms (5%) |           |   1.80 MiB (1%) |         495 |
| `["parallel_histogram", "assoc", "basesize=8192"]`  |   4.257 ms (5%) |           |   1.43 MiB (1%) |         240 |
| `["parallel_histogram", "comm", "basesize=16384"]`  |  13.270 ms (5%) |           |   1.22 MiB (1%) |         158 |
| `["parallel_histogram", "comm", "basesize=4096"]`   |  20.811 ms (5%) |           |   1.05 MiB (1%) |        4090 |
| `["parallel_histogram", "comm", "basesize=8192"]`   |  17.247 ms (5%) |  2.036 ms |   1.23 MiB (1%) |         452 |
| `["parallel_histogram", "seq"]`                     |   6.968 ms (5%) |           | 364.61 KiB (1%) |          24 |
| `["sum", "random", "foldl"]`                        |  13.731 ms (5%) |           |   64 bytes (1%) |           3 |
| `["sum", "random", "reduce", "basesize=128"]`       |   7.437 ms (5%) |           | 313.33 KiB (1%) |        6067 |
| `["sum", "random", "reduce", "basesize=256"]`       |   7.121 ms (5%) |           | 155.06 KiB (1%) |        3009 |
| `["sum", "random", "reduce", "basesize=512"]`       |   7.106 ms (5%) |           |  76.27 KiB (1%) |        1485 |
| `["sum", "uniform", "foldl"]`                       |  13.251 ms (5%) |           |   64 bytes (1%) |           3 |
| `["sum", "uniform", "reduce", "basesize=128"]`      |   7.161 ms (5%) |           | 313.33 KiB (1%) |        6067 |
| `["sum", "uniform", "reduce", "basesize=256"]`      |   6.833 ms (5%) |           | 155.02 KiB (1%) |        3006 |
| `["sum", "uniform", "reduce", "basesize=512"]`      |   6.525 ms (5%) |           |  76.25 KiB (1%) |        1484 |
| `["sum", "valley", "foldl"]`                        |  13.869 ms (5%) |           |   64 bytes (1%) |           3 |
| `["sum", "valley", "reduce", "basesize=128"]`       |   7.328 ms (5%) |           | 313.27 KiB (1%) |        6063 |
| `["sum", "valley", "reduce", "basesize=256"]`       |   7.063 ms (5%) |           | 155.08 KiB (1%) |        3010 |
| `["sum", "valley", "reduce", "basesize=512"]`       |   6.913 ms (5%) |           |  76.25 KiB (1%) |        1484 |
| `["words", "nthreads=1"]`                           |  49.260 ms (5%) |  7.611 ms |  63.34 MiB (1%) |     2069511 |
| `["words", "nthreads=2"]`                           |  25.304 ms (5%) |           |  64.43 MiB (1%) |     2081705 |
| `["words", "nthreads=4"]`                           |  26.657 ms (5%) |           |  65.37 MiB (1%) |     2092168 |

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
  CPU: Intel(R) Xeon(R) CPU E5-2673 v4 @ 2.30GHz: 
              speed         user         nice          sys         idle          irq
       #1  2294 MHz      76163 s          0 s       3073 s      22760 s          0 s
       #2  2294 MHz      72882 s          0 s       3254 s      25690 s          0 s
       
  Memory: 6.764884948730469 GB (2988.046875 MB free)
  Uptime: 1042.0 sec
  Load Avg:  1.60888671875  1.58935546875  1.1376953125
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
    CPU MHz:             2294.688
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

