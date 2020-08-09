# Multi-thread benchmark result

* Pull request commit: [`82444ea9b6aa6e87f66da77ed9d727975cda705b`](https://github.com/JuliaFolds/Transducers.jl/commit/82444ea9b6aa6e87f66da77ed9d727975cda705b)
* Pull request: <https://github.com/JuliaFolds/Transducers.jl/pull/404> (Add bench_filter_sum.jl)

# Judge result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmarks:
    - Target: 9 Aug 2020 - 04:31
    - Baseline: 9 Aug 2020 - 04:36
* Package commits:
    - Target: 396ae9
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
| `["collect", "unordered", "basesize=1024"]`         |                1.09 (5%) :x: |                1.01 (1%) :x: |
| `["findfirst", "n=500", "foldl"]`                   |                1.05 (5%) :x: |                   1.00 (1%)  |
| `["parallel_histogram", "assoc", "basesize=4096"]`  |                   0.98 (5%)  | 0.87 (1%) :white_check_mark: |
| `["parallel_histogram", "comm", "basesize=8192"]`   | 0.89 (5%) :white_check_mark: | 0.99 (1%) :white_check_mark: |
| `["sum", "random", "foldl"]`                        | 0.92 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["sum", "uniform", "reduce", "basesize=512"]`      | 0.94 (5%) :white_check_mark: |                   1.00 (1%)  |
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
      Ubuntu 18.04.4 LTS
  uname: Linux 5.3.0-1034-azure #35~18.04.1-Ubuntu SMP Mon Jul 13 12:54:45 UTC 2020 x86_64 x86_64
  CPU: Intel(R) Xeon(R) Platinum 8171M CPU @ 2.60GHz: 
              speed         user         nice          sys         idle          irq
       #1  2095 MHz      49063 s          0 s       2208 s      18050 s          0 s
       #2  2095 MHz      50948 s          0 s       2611 s      16896 s          0 s
       
  Memory: 6.764881134033203 GB (3025.70703125 MB free)
  Uptime: 721.0 sec
  Load Avg:  1.7392578125  1.5361328125  0.9189453125
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
       #1  2095 MHz      70709 s          0 s       2655 s      24909 s          0 s
       #2  2095 MHz      74226 s          0 s       3076 s      22162 s          0 s
       
  Memory: 6.764881134033203 GB (2960.60546875 MB free)
  Uptime: 1013.0 sec
  Load Avg:  1.685546875  1.5888671875  1.1083984375
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-8.0.1 (ORCJIT, skylake)
```

---
# Target result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmark: 9 Aug 2020 - 4:31
* Package commit: 396ae9
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
| `["collect", "assoc", "basesize=1"]`                | 359.117 ms (5%) | 11.776 ms |  87.55 MiB (1%) |     1590790 |
| `["collect", "assoc", "basesize=1024"]`             | 221.435 ms (5%) |           |   1.84 MiB (1%) |        1814 |
| `["collect", "assoc", "basesize=32"]`               | 224.379 ms (5%) |           |   5.64 MiB (1%) |       54010 |
| `["collect", "seq"]`                                | 438.978 ms (5%) |           |   1.50 MiB (1%) |       32784 |
| `["collect", "unordered", "basesize=1"]`            | 432.055 ms (5%) |           |  29.15 MiB (1%) |      402314 |
| `["collect", "unordered", "basesize=1024"]`         | 315.462 ms (5%) |           | 850.02 KiB (1%) |        7493 |
| `["collect", "unordered", "basesize=32"]`           | 249.551 ms (5%) |           |   1.46 MiB (1%) |       16087 |
| `["findfirst", "n=1000", "foldl"]`                  | 674.331 ms (5%) |           |                 |             |
| `["findfirst", "n=1000", "reduce", "basesize=128"]` | 352.950 ms (5%) |           | 563.59 KiB (1%) |       10197 |
| `["findfirst", "n=1000", "reduce", "basesize=256"]` | 352.050 ms (5%) |           | 287.25 KiB (1%) |        5222 |
| `["findfirst", "n=1000", "reduce", "basesize=512"]` | 353.696 ms (5%) |           | 149.34 KiB (1%) |        2723 |
| `["findfirst", "n=400", "foldl"]`                   | 506.347 ms (5%) |           |                 |             |
| `["findfirst", "n=400", "reduce", "basesize=128"]`  | 273.566 ms (5%) |           |   1.02 MiB (1%) |       18901 |
| `["findfirst", "n=400", "reduce", "basesize=256"]`  | 264.963 ms (5%) |           | 525.86 KiB (1%) |        9551 |
| `["findfirst", "n=400", "reduce", "basesize=512"]`  | 269.116 ms (5%) |           | 267.13 KiB (1%) |        4869 |
| `["findfirst", "n=500", "foldl"]`                   |  89.803 ms (5%) |           |                 |             |
| `["findfirst", "n=500", "reduce", "basesize=128"]`  |  45.362 ms (5%) |           | 157.27 KiB (1%) |        2842 |
| `["findfirst", "n=500", "reduce", "basesize=256"]`  |  44.661 ms (5%) |           |  84.53 KiB (1%) |        1532 |
| `["findfirst", "n=500", "reduce", "basesize=512"]`  |  48.111 ms (5%) |           |  48.30 KiB (1%) |         878 |
| `["overhead", "default"]`                           | 173.611 μs (5%) |           | 146.27 KiB (1%) |        2633 |
| `["overhead", "stoppable=false"]`                   | 172.511 μs (5%) |           | 146.28 KiB (1%) |        2633 |
| `["overhead", "stoppable=true"]`                    | 332.421 μs (5%) |           | 146.53 KiB (1%) |        2649 |
| `["parallel_histogram", "assoc", "basesize=16384"]` |   4.412 ms (5%) |           | 732.06 KiB (1%) |         103 |
| `["parallel_histogram", "assoc", "basesize=4096"]`  |   5.039 ms (5%) |           |   1.80 MiB (1%) |         496 |
| `["parallel_histogram", "assoc", "basesize=8192"]`  |   4.678 ms (5%) |           |   1.43 MiB (1%) |         243 |
| `["parallel_histogram", "comm", "basesize=16384"]`  |  15.440 ms (5%) |           |   1.22 MiB (1%) |         262 |
| `["parallel_histogram", "comm", "basesize=4096"]`   |  24.279 ms (5%) |           |   1.07 MiB (1%) |        5353 |
| `["parallel_histogram", "comm", "basesize=8192"]`   |  17.953 ms (5%) |           |   1.24 MiB (1%) |        1454 |
| `["parallel_histogram", "seq"]`                     |   8.227 ms (5%) |           | 364.61 KiB (1%) |          24 |
| `["sum", "random", "foldl"]`                        |  14.925 ms (5%) |           |   64 bytes (1%) |           3 |
| `["sum", "random", "reduce", "basesize=128"]`       |   8.602 ms (5%) |           | 313.38 KiB (1%) |        6068 |
| `["sum", "random", "reduce", "basesize=256"]`       |   8.443 ms (5%) |           | 155.20 KiB (1%) |        3016 |
| `["sum", "random", "reduce", "basesize=512"]`       |   8.370 ms (5%) |           |  76.31 KiB (1%) |        1486 |
| `["sum", "uniform", "foldl"]`                       |  15.033 ms (5%) |           |   64 bytes (1%) |           3 |
| `["sum", "uniform", "reduce", "basesize=128"]`      |   7.972 ms (5%) |           | 313.44 KiB (1%) |        6072 |
| `["sum", "uniform", "reduce", "basesize=256"]`      |   7.931 ms (5%) |           | 155.14 KiB (1%) |        3012 |
| `["sum", "uniform", "reduce", "basesize=512"]`      |   8.099 ms (5%) |           |  76.31 KiB (1%) |        1486 |
| `["sum", "valley", "foldl"]`                        |  16.336 ms (5%) |           |   64 bytes (1%) |           3 |
| `["sum", "valley", "reduce", "basesize=128"]`       |   8.740 ms (5%) |           | 313.36 KiB (1%) |        6067 |
| `["sum", "valley", "reduce", "basesize=256"]`       |   8.480 ms (5%) |           | 155.16 KiB (1%) |        3013 |
| `["sum", "valley", "reduce", "basesize=512"]`       |   7.972 ms (5%) |           |  76.33 KiB (1%) |        1487 |
| `["words", "nthreads=1"]`                           |  34.839 ms (5%) |  7.107 ms |  63.16 MiB (1%) |     2063916 |
| `["words", "nthreads=2"]`                           |  18.385 ms (5%) |           |  63.77 MiB (1%) |     2072011 |
| `["words", "nthreads=4"]`                           |  18.627 ms (5%) |           |  65.04 MiB (1%) |     2084455 |

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
       #1  2095 MHz      49063 s          0 s       2208 s      18050 s          0 s
       #2  2095 MHz      50948 s          0 s       2611 s      16896 s          0 s
       
  Memory: 6.764881134033203 GB (3025.70703125 MB free)
  Uptime: 721.0 sec
  Load Avg:  1.7392578125  1.5361328125  0.9189453125
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-8.0.1 (ORCJIT, skylake)
```

---
# Baseline result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmark: 9 Aug 2020 - 4:36
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
| `["collect", "assoc", "basesize=1"]`                | 352.051 ms (5%) | 10.318 ms |  87.55 MiB (1%) |     1590777 |
| `["collect", "assoc", "basesize=1024"]`             | 218.989 ms (5%) |           |   1.84 MiB (1%) |        1812 |
| `["collect", "assoc", "basesize=32"]`               | 230.202 ms (5%) |           |   5.64 MiB (1%) |       54008 |
| `["collect", "seq"]`                                | 425.826 ms (5%) |           |   1.50 MiB (1%) |       32784 |
| `["collect", "unordered", "basesize=1"]`            | 432.573 ms (5%) |           |  29.14 MiB (1%) |      401681 |
| `["collect", "unordered", "basesize=1024"]`         | 289.913 ms (5%) |           | 838.47 KiB (1%) |        6418 |
| `["collect", "unordered", "basesize=32"]`           | 251.444 ms (5%) |           |   1.47 MiB (1%) |       16581 |
| `["findfirst", "n=1000", "foldl"]`                  | 671.970 ms (5%) |           |                 |             |
| `["findfirst", "n=1000", "reduce", "basesize=128"]` | 357.325 ms (5%) |           | 563.94 KiB (1%) |       10219 |
| `["findfirst", "n=1000", "reduce", "basesize=256"]` | 356.370 ms (5%) |           | 287.09 KiB (1%) |        5212 |
| `["findfirst", "n=1000", "reduce", "basesize=512"]` | 361.579 ms (5%) |           | 149.31 KiB (1%) |        2721 |
| `["findfirst", "n=400", "foldl"]`                   | 510.576 ms (5%) |           |                 |             |
| `["findfirst", "n=400", "reduce", "basesize=128"]`  | 266.914 ms (5%) |           |   1.02 MiB (1%) |       18909 |
| `["findfirst", "n=400", "reduce", "basesize=256"]`  | 266.801 ms (5%) |           | 525.86 KiB (1%) |        9551 |
| `["findfirst", "n=400", "reduce", "basesize=512"]`  | 266.936 ms (5%) |           | 267.25 KiB (1%) |        4877 |
| `["findfirst", "n=500", "foldl"]`                   |  85.178 ms (5%) |           |                 |             |
| `["findfirst", "n=500", "reduce", "basesize=128"]`  |  44.282 ms (5%) |           | 157.25 KiB (1%) |        2841 |
| `["findfirst", "n=500", "reduce", "basesize=256"]`  |  43.917 ms (5%) |           |  84.53 KiB (1%) |        1532 |
| `["findfirst", "n=500", "reduce", "basesize=512"]`  |  47.624 ms (5%) |           |  48.30 KiB (1%) |         878 |
| `["overhead", "default"]`                           | 172.808 μs (5%) |           | 146.27 KiB (1%) |        2633 |
| `["overhead", "stoppable=false"]`                   | 173.508 μs (5%) |           | 146.27 KiB (1%) |        2632 |
| `["overhead", "stoppable=true"]`                    | 333.514 μs (5%) |           | 146.55 KiB (1%) |        2650 |
| `["parallel_histogram", "assoc", "basesize=16384"]` |   4.426 ms (5%) |           | 732.06 KiB (1%) |         103 |
| `["parallel_histogram", "assoc", "basesize=4096"]`  |   5.131 ms (5%) |           |   2.07 MiB (1%) |         503 |
| `["parallel_histogram", "assoc", "basesize=8192"]`  |   4.662 ms (5%) |           |   1.43 MiB (1%) |         243 |
| `["parallel_histogram", "comm", "basesize=16384"]`  |  15.191 ms (5%) |           |   1.22 MiB (1%) |         158 |
| `["parallel_histogram", "comm", "basesize=4096"]`   |  24.224 ms (5%) |           |   1.07 MiB (1%) |        5855 |
| `["parallel_histogram", "comm", "basesize=8192"]`   |  20.266 ms (5%) |           |   1.25 MiB (1%) |        2334 |
| `["parallel_histogram", "seq"]`                     |   8.149 ms (5%) |           | 364.61 KiB (1%) |          24 |
| `["sum", "random", "foldl"]`                        |  16.307 ms (5%) |           |   64 bytes (1%) |           3 |
| `["sum", "random", "reduce", "basesize=128"]`       |   8.556 ms (5%) |           | 313.42 KiB (1%) |        6071 |
| `["sum", "random", "reduce", "basesize=256"]`       |   8.602 ms (5%) |           | 155.14 KiB (1%) |        3012 |
| `["sum", "random", "reduce", "basesize=512"]`       |   8.267 ms (5%) |           |  76.31 KiB (1%) |        1486 |
| `["sum", "uniform", "foldl"]`                       |  15.739 ms (5%) |           |   64 bytes (1%) |           3 |
| `["sum", "uniform", "reduce", "basesize=128"]`      |   8.160 ms (5%) |           | 313.41 KiB (1%) |        6070 |
| `["sum", "uniform", "reduce", "basesize=256"]`      |   7.760 ms (5%) |           | 155.16 KiB (1%) |        3013 |
| `["sum", "uniform", "reduce", "basesize=512"]`      |   8.574 ms (5%) |           |  76.30 KiB (1%) |        1485 |
| `["sum", "valley", "foldl"]`                        |  16.255 ms (5%) |           |   64 bytes (1%) |           3 |
| `["sum", "valley", "reduce", "basesize=128"]`       |   8.762 ms (5%) |           | 313.34 KiB (1%) |        6066 |
| `["sum", "valley", "reduce", "basesize=256"]`       |   8.467 ms (5%) |           | 155.16 KiB (1%) |        3013 |
| `["sum", "valley", "reduce", "basesize=512"]`       |   8.304 ms (5%) |           |  76.34 KiB (1%) |        1488 |
| `["words", "nthreads=1"]`                           |  33.424 ms (5%) |  6.585 ms |  63.46 MiB (1%) |     2073502 |
| `["words", "nthreads=2"]`                           |  17.379 ms (5%) |           |  64.06 MiB (1%) |     2081576 |
| `["words", "nthreads=4"]`                           |  18.152 ms (5%) |           |  65.33 MiB (1%) |     2093971 |

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
       #1  2095 MHz      70709 s          0 s       2655 s      24909 s          0 s
       #2  2095 MHz      74226 s          0 s       3076 s      22162 s          0 s
       
  Memory: 6.764881134033203 GB (2960.60546875 MB free)
  Uptime: 1013.0 sec
  Load Avg:  1.685546875  1.5888671875  1.1083984375
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
    CPU MHz:             2095.200
    BogoMIPS:            4190.40
    Hypervisor vendor:   Microsoft
    Virtualization type: full
    L1d cache:           32K
    L1i cache:           32K
    L2 cache:            1024K
    L3 cache:            36608K
    NUMA node0 CPU(s):   0,1
    Flags:               fpu vme de pse tsc msr pae mce cx8 apic sep mtrr pge mca cmov pat pse36 clflush mmx fxsr sse sse2 ss ht syscall nx pdpe1gb rdtscp lm constant_tsc rep_good nopl xtopology cpuid pni pclmulqdq ssse3 fma cx16 pcid sse4_1 sse4_2 movbe popcnt aes xsave avx f16c rdrand hypervisor lahf_lm abm 3dnowprefetch invpcid_single pti fsgsbase bmi1 hle avx2 smep bmi2 erms invpcid rtm mpx avx512f avx512dq rdseed adx smap clflushopt avx512cd avx512bw avx512vl xsaveopt xsavec xsaves
    

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

