# Multi-thread benchmark result

* Pull request commit: [`dc735af6e016360b281e6a2d608df65be1e1e903`](https://github.com/JuliaFolds/Transducers.jl/commit/dc735af6e016360b281e6a2d608df65be1e1e903)
* Pull request: <https://github.com/JuliaFolds/Transducers.jl/pull/402> (Add more specialization hints to the compiler)

# Judge result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmarks:
    - Target: 9 Aug 2020 - 02:43
    - Baseline: 9 Aug 2020 - 02:48
* Package commits:
    - Target: f25a5a
    - Baseline: 71524a
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
| `["collect", "unordered", "basesize=1024"]`         |                1.08 (5%) :x: | 1.04 (1%) :x: |
| `["overhead", "stoppable=false"]`                   | 0.94 (5%) :white_check_mark: |    1.00 (1%)  |
| `["sum", "random", "foldl"]`                        |                1.05 (5%) :x: |    1.00 (1%)  |
| `["sum", "random", "reduce", "basesize=128"]`       |                1.05 (5%) :x: |    1.00 (1%)  |
| `["sum", "random", "reduce", "basesize=512"]`       |                1.05 (5%) :x: |    1.00 (1%)  |

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
       #1  2095 MHz      47279 s          0 s       2113 s      21352 s          0 s
       #2  2095 MHz      54316 s          0 s       2426 s      14877 s          0 s
       
  Memory: 6.764881134033203 GB (2976.82421875 MB free)
  Uptime: 734.0 sec
  Load Avg:  1.69921875  1.515625  0.91064453125
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
       #1  2095 MHz      69447 s          0 s       2612 s      28545 s          0 s
       #2  2095 MHz      77927 s          0 s       2842 s      20628 s          0 s
       
  Memory: 6.764881134033203 GB (3001.3203125 MB free)
  Uptime: 1034.0 sec
  Load Avg:  1.7822265625  1.61572265625  1.1181640625
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-8.0.1 (ORCJIT, skylake)
```

---
# Target result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmark: 9 Aug 2020 - 2:43
* Package commit: f25a5a
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
| `["collect", "assoc", "basesize=1"]`                | 360.676 ms (5%) | 11.572 ms |  87.55 MiB (1%) |     1590766 |
| `["collect", "assoc", "basesize=1024"]`             | 223.929 ms (5%) |           |   1.84 MiB (1%) |        1813 |
| `["collect", "assoc", "basesize=32"]`               | 229.451 ms (5%) |           |   5.64 MiB (1%) |       54016 |
| `["collect", "seq"]`                                | 441.130 ms (5%) |           |   1.50 MiB (1%) |       32784 |
| `["collect", "unordered", "basesize=1"]`            | 462.748 ms (5%) |           |  29.16 MiB (1%) |      403567 |
| `["collect", "unordered", "basesize=1024"]`         | 280.730 ms (5%) |           | 803.22 KiB (1%) |        4498 |
| `["collect", "unordered", "basesize=32"]`           | 258.437 ms (5%) |           |   1.47 MiB (1%) |       16945 |
| `["findfirst", "n=1000", "foldl"]`                  | 679.165 ms (5%) |           |                 |             |
| `["findfirst", "n=1000", "reduce", "basesize=128"]` | 357.963 ms (5%) |           | 563.70 KiB (1%) |       10204 |
| `["findfirst", "n=1000", "reduce", "basesize=256"]` | 360.530 ms (5%) |           | 287.11 KiB (1%) |        5213 |
| `["findfirst", "n=1000", "reduce", "basesize=512"]` | 369.300 ms (5%) |           | 149.22 KiB (1%) |        2715 |
| `["findfirst", "n=400", "foldl"]`                   | 522.980 ms (5%) |           |                 |             |
| `["findfirst", "n=400", "reduce", "basesize=128"]`  | 269.490 ms (5%) |           |   1.02 MiB (1%) |       18932 |
| `["findfirst", "n=400", "reduce", "basesize=256"]`  | 265.389 ms (5%) |           | 525.66 KiB (1%) |        9538 |
| `["findfirst", "n=400", "reduce", "basesize=512"]`  | 273.595 ms (5%) |           | 267.09 KiB (1%) |        4867 |
| `["findfirst", "n=500", "foldl"]`                   |  82.882 ms (5%) |           |                 |             |
| `["findfirst", "n=500", "reduce", "basesize=128"]`  |  45.859 ms (5%) |           | 157.36 KiB (1%) |        2848 |
| `["findfirst", "n=500", "reduce", "basesize=256"]`  |  46.155 ms (5%) |           |  84.56 KiB (1%) |        1534 |
| `["findfirst", "n=500", "reduce", "basesize=512"]`  |  49.101 ms (5%) |           |  48.30 KiB (1%) |         878 |
| `["overhead", "default"]`                           | 170.204 μs (5%) |           | 146.27 KiB (1%) |        2633 |
| `["overhead", "stoppable=false"]`                   | 164.803 μs (5%) |           | 146.28 KiB (1%) |        2633 |
| `["overhead", "stoppable=true"]`                    | 317.206 μs (5%) |           | 146.53 KiB (1%) |        2649 |
| `["parallel_histogram", "assoc", "basesize=16384"]` |   4.398 ms (5%) |           | 732.06 KiB (1%) |         103 |
| `["parallel_histogram", "assoc", "basesize=4096"]`  |   5.217 ms (5%) |           |   1.80 MiB (1%) |         497 |
| `["parallel_histogram", "assoc", "basesize=8192"]`  |   4.872 ms (5%) |           |   1.43 MiB (1%) |         242 |
| `["parallel_histogram", "comm", "basesize=16384"]`  |  15.419 ms (5%) |           |   1.22 MiB (1%) |         159 |
| `["parallel_histogram", "comm", "basesize=4096"]`   |  22.774 ms (5%) |           |   1.05 MiB (1%) |        4991 |
| `["parallel_histogram", "comm", "basesize=8192"]`   |  19.522 ms (5%) |           |   1.25 MiB (1%) |        2363 |
| `["parallel_histogram", "seq"]`                     |   7.816 ms (5%) |           | 364.61 KiB (1%) |          24 |
| `["sum", "random", "foldl"]`                        |  16.020 ms (5%) |           |   64 bytes (1%) |           3 |
| `["sum", "random", "reduce", "basesize=128"]`       |   9.107 ms (5%) |           | 313.42 KiB (1%) |        6071 |
| `["sum", "random", "reduce", "basesize=256"]`       |   8.627 ms (5%) |           | 155.19 KiB (1%) |        3015 |
| `["sum", "random", "reduce", "basesize=512"]`       |   8.436 ms (5%) |           |  76.36 KiB (1%) |        1489 |
| `["sum", "uniform", "foldl"]`                       |  15.316 ms (5%) |           |   64 bytes (1%) |           3 |
| `["sum", "uniform", "reduce", "basesize=128"]`      |   8.480 ms (5%) |           | 313.42 KiB (1%) |        6071 |
| `["sum", "uniform", "reduce", "basesize=256"]`      |   8.195 ms (5%) |           | 155.16 KiB (1%) |        3013 |
| `["sum", "uniform", "reduce", "basesize=512"]`      |   8.048 ms (5%) |           |  76.31 KiB (1%) |        1486 |
| `["sum", "valley", "foldl"]`                        |  15.766 ms (5%) |           |   64 bytes (1%) |           3 |
| `["sum", "valley", "reduce", "basesize=128"]`       |   8.810 ms (5%) |           | 313.33 KiB (1%) |        6065 |
| `["sum", "valley", "reduce", "basesize=256"]`       |   8.710 ms (5%) |           | 155.17 KiB (1%) |        3014 |
| `["sum", "valley", "reduce", "basesize=512"]`       |   8.577 ms (5%) |           |  76.33 KiB (1%) |        1487 |
| `["words", "nthreads=1"]`                           |  35.156 ms (5%) |  7.040 ms |  62.95 MiB (1%) |     2056507 |
| `["words", "nthreads=2"]`                           |  19.148 ms (5%) |           |  64.03 MiB (1%) |     2068785 |
| `["words", "nthreads=4"]`                           |  19.138 ms (5%) |           |  64.98 MiB (1%) |     2079137 |

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
       #1  2095 MHz      47279 s          0 s       2113 s      21352 s          0 s
       #2  2095 MHz      54316 s          0 s       2426 s      14877 s          0 s
       
  Memory: 6.764881134033203 GB (2976.82421875 MB free)
  Uptime: 734.0 sec
  Load Avg:  1.69921875  1.515625  0.91064453125
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-8.0.1 (ORCJIT, skylake)
```

---
# Baseline result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmark: 9 Aug 2020 - 2:48
* Package commit: 71524a
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
| `["collect", "assoc", "basesize=1"]`                | 356.143 ms (5%) | 10.628 ms |  87.55 MiB (1%) |     1590747 |
| `["collect", "assoc", "basesize=1024"]`             | 227.429 ms (5%) |           |   1.84 MiB (1%) |        1813 |
| `["collect", "assoc", "basesize=32"]`               | 227.820 ms (5%) |           |   5.64 MiB (1%) |       54020 |
| `["collect", "seq"]`                                | 443.084 ms (5%) |           |   1.50 MiB (1%) |       32784 |
| `["collect", "unordered", "basesize=1"]`            | 457.989 ms (5%) |           |  29.16 MiB (1%) |      403312 |
| `["collect", "unordered", "basesize=1024"]`         | 259.125 ms (5%) |           | 775.56 KiB (1%) |        2347 |
| `["collect", "unordered", "basesize=32"]`           | 258.727 ms (5%) |           |   1.47 MiB (1%) |       16842 |
| `["findfirst", "n=1000", "foldl"]`                  | 689.666 ms (5%) |           |                 |             |
| `["findfirst", "n=1000", "reduce", "basesize=128"]` | 356.623 ms (5%) |           | 563.95 KiB (1%) |       10220 |
| `["findfirst", "n=1000", "reduce", "basesize=256"]` | 355.402 ms (5%) |           | 287.30 KiB (1%) |        5225 |
| `["findfirst", "n=1000", "reduce", "basesize=512"]` | 363.551 ms (5%) |           | 149.34 KiB (1%) |        2723 |
| `["findfirst", "n=400", "foldl"]`                   | 520.886 ms (5%) |           |                 |             |
| `["findfirst", "n=400", "reduce", "basesize=128"]`  | 270.920 ms (5%) |           |   1.02 MiB (1%) |       18885 |
| `["findfirst", "n=400", "reduce", "basesize=256"]`  | 271.050 ms (5%) |           | 525.73 KiB (1%) |        9543 |
| `["findfirst", "n=400", "reduce", "basesize=512"]`  | 272.723 ms (5%) |           | 267.03 KiB (1%) |        4863 |
| `["findfirst", "n=500", "foldl"]`                   |  86.996 ms (5%) |           |                 |             |
| `["findfirst", "n=500", "reduce", "basesize=128"]`  |  45.678 ms (5%) |           | 157.30 KiB (1%) |        2844 |
| `["findfirst", "n=500", "reduce", "basesize=256"]`  |  45.740 ms (5%) |           |  84.53 KiB (1%) |        1532 |
| `["findfirst", "n=500", "reduce", "basesize=512"]`  |  48.361 ms (5%) |           |  48.30 KiB (1%) |         878 |
| `["overhead", "default"]`                           | 174.004 μs (5%) |           | 146.27 KiB (1%) |        2633 |
| `["overhead", "stoppable=false"]`                   | 175.603 μs (5%) |           | 146.28 KiB (1%) |        2633 |
| `["overhead", "stoppable=true"]`                    | 329.707 μs (5%) |           | 146.55 KiB (1%) |        2650 |
| `["parallel_histogram", "assoc", "basesize=16384"]` |   4.541 ms (5%) |           | 732.06 KiB (1%) |         103 |
| `["parallel_histogram", "assoc", "basesize=4096"]`  |   5.286 ms (5%) |           |   1.80 MiB (1%) |         497 |
| `["parallel_histogram", "assoc", "basesize=8192"]`  |   4.782 ms (5%) |           |   1.43 MiB (1%) |         242 |
| `["parallel_histogram", "comm", "basesize=16384"]`  |  15.147 ms (5%) |           |   1.22 MiB (1%) |         158 |
| `["parallel_histogram", "comm", "basesize=4096"]`   |  23.967 ms (5%) |           |   1.04 MiB (1%) |        4734 |
| `["parallel_histogram", "comm", "basesize=8192"]`   |  20.515 ms (5%) |           |   1.25 MiB (1%) |        2384 |
| `["parallel_histogram", "seq"]`                     |   7.864 ms (5%) |           | 364.61 KiB (1%) |          24 |
| `["sum", "random", "foldl"]`                        |  15.217 ms (5%) |           |   64 bytes (1%) |           3 |
| `["sum", "random", "reduce", "basesize=128"]`       |   8.644 ms (5%) |           | 313.42 KiB (1%) |        6071 |
| `["sum", "random", "reduce", "basesize=256"]`       |   8.498 ms (5%) |           | 155.13 KiB (1%) |        3011 |
| `["sum", "random", "reduce", "basesize=512"]`       |   8.019 ms (5%) |           |  76.30 KiB (1%) |        1485 |
| `["sum", "uniform", "foldl"]`                       |  15.281 ms (5%) |           |   64 bytes (1%) |           3 |
| `["sum", "uniform", "reduce", "basesize=128"]`      |   8.320 ms (5%) |           | 313.41 KiB (1%) |        6070 |
| `["sum", "uniform", "reduce", "basesize=256"]`      |   8.419 ms (5%) |           | 155.16 KiB (1%) |        3013 |
| `["sum", "uniform", "reduce", "basesize=512"]`      |   8.143 ms (5%) |           |  76.31 KiB (1%) |        1486 |
| `["sum", "valley", "foldl"]`                        |  16.203 ms (5%) |           |   64 bytes (1%) |           3 |
| `["sum", "valley", "reduce", "basesize=128"]`       |   8.811 ms (5%) |           | 313.33 KiB (1%) |        6065 |
| `["sum", "valley", "reduce", "basesize=256"]`       |   8.835 ms (5%) |           | 155.16 KiB (1%) |        3013 |
| `["sum", "valley", "reduce", "basesize=512"]`       |   8.440 ms (5%) |           |  76.31 KiB (1%) |        1486 |
| `["words", "nthreads=1"]`                           |  34.068 ms (5%) |  6.478 ms |  63.30 MiB (1%) |     2068155 |
| `["words", "nthreads=2"]`                           |  18.506 ms (5%) |           |  64.38 MiB (1%) |     2080361 |
| `["words", "nthreads=4"]`                           |  19.530 ms (5%) |           |  65.02 MiB (1%) |     2086610 |

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
       #1  2095 MHz      69447 s          0 s       2612 s      28545 s          0 s
       #2  2095 MHz      77927 s          0 s       2842 s      20628 s          0 s
       
  Memory: 6.764881134033203 GB (3001.3203125 MB free)
  Uptime: 1034.0 sec
  Load Avg:  1.7822265625  1.61572265625  1.1181640625
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
    CPU MHz:             2095.196
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

