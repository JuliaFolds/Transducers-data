# Multi-thread benchmark result

* Pull request commit: [`6795e603680b6210075c0ad4ba9f8e7dd4b8b1a4`](https://github.com/JuliaFolds/Transducers.jl/commit/6795e603680b6210075c0ad4ba9f8e7dd4b8b1a4)
* Pull request: <https://github.com/JuliaFolds/Transducers.jl/pull/393> (Avoid using "automatic approve" hack in mergify)

# Judge result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmarks:
    - Target: 3 Aug 2020 - 22:41
    - Baseline: 3 Aug 2020 - 22:46
* Package commits:
    - Target: 69a891
    - Baseline: a36be3
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
| `["collect", "unordered", "basesize=1024"]`         | 0.93 (5%) :white_check_mark: | 0.95 (1%) :white_check_mark: |
| `["parallel_histogram", "assoc", "basesize=4096"]`  |                   1.00 (5%)  | 0.87 (1%) :white_check_mark: |
| `["parallel_histogram", "comm", "basesize=4096"]`   |                   1.00 (5%)  |                1.03 (1%) :x: |
| `["sum", "uniform", "reduce", "basesize=256"]`      |                1.06 (5%) :x: |                   1.00 (1%)  |
| `["words", "nthreads=1"]`                           |                   0.97 (5%)  | 0.99 (1%) :white_check_mark: |
| `["words", "nthreads=2"]`                           |                   0.97 (5%)  | 0.99 (1%) :white_check_mark: |

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
       #1  2095 MHz      46860 s          0 s       2422 s      50777 s          0 s
       #2  2095 MHz      56810 s          0 s       2482 s      40917 s          0 s
       
  Memory: 6.764884948730469 GB (2888.6328125 MB free)
  Uptime: 1022.0 sec
  Load Avg:  1.70361328125  1.498046875  0.90673828125
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
       #1  2095 MHz      69034 s          0 s       2897 s      58003 s          0 s
       #2  2095 MHz      80687 s          0 s       2906 s      46604 s          0 s
       
  Memory: 6.764884948730469 GB (2891.62890625 MB free)
  Uptime: 1324.0 sec
  Load Avg:  1.701171875  1.568359375  1.1005859375
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-8.0.1 (ORCJIT, skylake)
```

---
# Target result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmark: 3 Aug 2020 - 22:41
* Package commit: 69a891
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
| `["collect", "assoc", "basesize=1"]`                | 383.643 ms (5%) | 11.569 ms |  87.55 MiB (1%) |     1590747 |
| `["collect", "assoc", "basesize=1024"]`             | 239.567 ms (5%) |           |   1.84 MiB (1%) |        1812 |
| `["collect", "assoc", "basesize=32"]`               | 245.619 ms (5%) |           |   5.64 MiB (1%) |       54006 |
| `["collect", "seq"]`                                | 476.191 ms (5%) |           |   1.50 MiB (1%) |       32784 |
| `["collect", "unordered", "basesize=1"]`            | 488.857 ms (5%) |           |  29.16 MiB (1%) |      403520 |
| `["collect", "unordered", "basesize=1024"]`         | 353.255 ms (5%) |           | 887.61 KiB (1%) |        9854 |
| `["collect", "unordered", "basesize=32"]`           | 272.733 ms (5%) |           |   1.47 MiB (1%) |       16504 |
| `["findfirst", "n=1000", "foldl"]`                  | 759.883 ms (5%) |           |                 |             |
| `["findfirst", "n=1000", "reduce", "basesize=128"]` | 385.392 ms (5%) |           | 564.06 KiB (1%) |       10227 |
| `["findfirst", "n=1000", "reduce", "basesize=256"]` | 384.319 ms (5%) |           | 287.28 KiB (1%) |        5224 |
| `["findfirst", "n=1000", "reduce", "basesize=512"]` | 390.828 ms (5%) |           | 149.39 KiB (1%) |        2726 |
| `["findfirst", "n=400", "foldl"]`                   | 570.664 ms (5%) |           |                 |             |
| `["findfirst", "n=400", "reduce", "basesize=128"]`  | 291.912 ms (5%) |           |   1.02 MiB (1%) |       18939 |
| `["findfirst", "n=400", "reduce", "basesize=256"]`  | 289.059 ms (5%) |           | 525.69 KiB (1%) |        9540 |
| `["findfirst", "n=400", "reduce", "basesize=512"]`  | 291.424 ms (5%) |           | 267.11 KiB (1%) |        4868 |
| `["findfirst", "n=500", "foldl"]`                   |  98.187 ms (5%) |           |                 |             |
| `["findfirst", "n=500", "reduce", "basesize=128"]`  |  50.719 ms (5%) |           | 157.34 KiB (1%) |        2847 |
| `["findfirst", "n=500", "reduce", "basesize=256"]`  |  50.382 ms (5%) |           |  84.55 KiB (1%) |        1533 |
| `["findfirst", "n=500", "reduce", "basesize=512"]`  |  53.695 ms (5%) |           |  48.31 KiB (1%) |         879 |
| `["overhead", "default"]`                           | 197.907 μs (5%) |           | 146.27 KiB (1%) |        2633 |
| `["overhead", "stoppable=false"]`                   | 199.508 μs (5%) |           | 146.28 KiB (1%) |        2633 |
| `["overhead", "stoppable=true"]`                    | 346.913 μs (5%) |           | 146.53 KiB (1%) |        2649 |
| `["parallel_histogram", "assoc", "basesize=16384"]` |   5.068 ms (5%) |           | 732.06 KiB (1%) |         103 |
| `["parallel_histogram", "assoc", "basesize=4096"]`  |   5.941 ms (5%) |           |   1.80 MiB (1%) |         497 |
| `["parallel_histogram", "assoc", "basesize=8192"]`  |   5.497 ms (5%) |           |   1.43 MiB (1%) |         243 |
| `["parallel_histogram", "comm", "basesize=16384"]`  |  16.138 ms (5%) |           |   1.22 MiB (1%) |         159 |
| `["parallel_histogram", "comm", "basesize=4096"]`   |  25.011 ms (5%) |           |   1.06 MiB (1%) |        5158 |
| `["parallel_histogram", "comm", "basesize=8192"]`   |  20.085 ms (5%) |           |   1.25 MiB (1%) |        2307 |
| `["parallel_histogram", "seq"]`                     |   9.418 ms (5%) |           | 364.61 KiB (1%) |          24 |
| `["sum", "random", "foldl"]`                        |  18.660 ms (5%) |           |   64 bytes (1%) |           3 |
| `["sum", "random", "reduce", "basesize=128"]`       |   9.930 ms (5%) |           | 313.39 KiB (1%) |        6069 |
| `["sum", "random", "reduce", "basesize=256"]`       |   9.861 ms (5%) |           | 155.14 KiB (1%) |        3012 |
| `["sum", "random", "reduce", "basesize=512"]`       |   9.608 ms (5%) |           |  76.31 KiB (1%) |        1486 |
| `["sum", "uniform", "foldl"]`                       |  18.330 ms (5%) |           |   64 bytes (1%) |           3 |
| `["sum", "uniform", "reduce", "basesize=128"]`      |   9.807 ms (5%) |           | 313.45 KiB (1%) |        6073 |
| `["sum", "uniform", "reduce", "basesize=256"]`      |   9.517 ms (5%) |           | 155.14 KiB (1%) |        3012 |
| `["sum", "uniform", "reduce", "basesize=512"]`      |   9.348 ms (5%) |           |  76.31 KiB (1%) |        1486 |
| `["sum", "valley", "foldl"]`                        |  18.937 ms (5%) |           |   64 bytes (1%) |           3 |
| `["sum", "valley", "reduce", "basesize=128"]`       |   9.938 ms (5%) |           | 313.31 KiB (1%) |        6064 |
| `["sum", "valley", "reduce", "basesize=256"]`       |   9.783 ms (5%) |           | 155.13 KiB (1%) |        3011 |
| `["sum", "valley", "reduce", "basesize=512"]`       |   9.670 ms (5%) |           |  76.31 KiB (1%) |        1486 |
| `["words", "nthreads=1"]`                           |  50.054 ms (5%) |  7.934 ms |  62.61 MiB (1%) |     2045631 |
| `["words", "nthreads=2"]`                           |  25.648 ms (5%) |           |  63.70 MiB (1%) |     2057885 |
| `["words", "nthreads=4"]`                           |  26.603 ms (5%) |           |  64.64 MiB (1%) |     2068276 |

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
       #1  2095 MHz      46860 s          0 s       2422 s      50777 s          0 s
       #2  2095 MHz      56810 s          0 s       2482 s      40917 s          0 s
       
  Memory: 6.764884948730469 GB (2888.6328125 MB free)
  Uptime: 1022.0 sec
  Load Avg:  1.70361328125  1.498046875  0.90673828125
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-8.0.1 (ORCJIT, skylake)
```

---
# Baseline result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmark: 3 Aug 2020 - 22:46
* Package commit: a36be3
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
| `["collect", "assoc", "basesize=1"]`                | 384.109 ms (5%) | 13.056 ms |  87.55 MiB (1%) |     1590792 |
| `["collect", "assoc", "basesize=1024"]`             | 239.800 ms (5%) |           |   1.84 MiB (1%) |        1812 |
| `["collect", "assoc", "basesize=32"]`               | 245.157 ms (5%) |           |   5.64 MiB (1%) |       54016 |
| `["collect", "seq"]`                                | 473.440 ms (5%) |           |   1.50 MiB (1%) |       32784 |
| `["collect", "unordered", "basesize=1"]`            | 485.819 ms (5%) |  8.298 ms |  29.16 MiB (1%) |      403376 |
| `["collect", "unordered", "basesize=1024"]`         | 378.385 ms (5%) |           | 932.06 KiB (1%) |       12666 |
| `["collect", "unordered", "basesize=32"]`           | 269.545 ms (5%) |           |   1.47 MiB (1%) |       16763 |
| `["findfirst", "n=1000", "foldl"]`                  | 751.371 ms (5%) |           |                 |             |
| `["findfirst", "n=1000", "reduce", "basesize=128"]` | 379.572 ms (5%) |           | 564.16 KiB (1%) |       10233 |
| `["findfirst", "n=1000", "reduce", "basesize=256"]` | 379.240 ms (5%) |           | 287.30 KiB (1%) |        5225 |
| `["findfirst", "n=1000", "reduce", "basesize=512"]` | 387.084 ms (5%) |           | 149.33 KiB (1%) |        2722 |
| `["findfirst", "n=400", "foldl"]`                   | 561.744 ms (5%) |           |                 |             |
| `["findfirst", "n=400", "reduce", "basesize=128"]`  | 288.141 ms (5%) |           |   1.02 MiB (1%) |       18866 |
| `["findfirst", "n=400", "reduce", "basesize=256"]`  | 285.797 ms (5%) |           | 526.16 KiB (1%) |        9570 |
| `["findfirst", "n=400", "reduce", "basesize=512"]`  | 288.138 ms (5%) |           | 267.20 KiB (1%) |        4874 |
| `["findfirst", "n=500", "foldl"]`                   |  97.117 ms (5%) |           |                 |             |
| `["findfirst", "n=500", "reduce", "basesize=128"]`  |  49.685 ms (5%) |           | 157.34 KiB (1%) |        2847 |
| `["findfirst", "n=500", "reduce", "basesize=256"]`  |  49.648 ms (5%) |           |  84.58 KiB (1%) |        1535 |
| `["findfirst", "n=500", "reduce", "basesize=512"]`  |  52.430 ms (5%) |           |  48.31 KiB (1%) |         879 |
| `["overhead", "default"]`                           | 196.512 μs (5%) |           | 146.27 KiB (1%) |        2633 |
| `["overhead", "stoppable=false"]`                   | 199.912 μs (5%) |           | 146.28 KiB (1%) |        2633 |
| `["overhead", "stoppable=true"]`                    | 352.121 μs (5%) |           | 146.55 KiB (1%) |        2650 |
| `["parallel_histogram", "assoc", "basesize=16384"]` |   5.084 ms (5%) |           | 732.06 KiB (1%) |         103 |
| `["parallel_histogram", "assoc", "basesize=4096"]`  |   5.955 ms (5%) |           |   2.07 MiB (1%) |         503 |
| `["parallel_histogram", "assoc", "basesize=8192"]`  |   5.397 ms (5%) |           |   1.43 MiB (1%) |         243 |
| `["parallel_histogram", "comm", "basesize=16384"]`  |  15.915 ms (5%) |           |   1.22 MiB (1%) |         158 |
| `["parallel_histogram", "comm", "basesize=4096"]`   |  25.061 ms (5%) |           |   1.03 MiB (1%) |        3590 |
| `["parallel_histogram", "comm", "basesize=8192"]`   |  20.809 ms (5%) |           |   1.26 MiB (1%) |        2589 |
| `["parallel_histogram", "seq"]`                     |   9.178 ms (5%) |           | 364.61 KiB (1%) |          24 |
| `["sum", "random", "foldl"]`                        |  18.598 ms (5%) |           |   64 bytes (1%) |           3 |
| `["sum", "random", "reduce", "basesize=128"]`       |  10.058 ms (5%) |           | 313.36 KiB (1%) |        6067 |
| `["sum", "random", "reduce", "basesize=256"]`       |   9.745 ms (5%) |           | 155.14 KiB (1%) |        3012 |
| `["sum", "random", "reduce", "basesize=512"]`       |   9.464 ms (5%) |           |  76.33 KiB (1%) |        1487 |
| `["sum", "uniform", "foldl"]`                       |  18.417 ms (5%) |           |   64 bytes (1%) |           3 |
| `["sum", "uniform", "reduce", "basesize=128"]`      |   9.761 ms (5%) |           | 313.44 KiB (1%) |        6072 |
| `["sum", "uniform", "reduce", "basesize=256"]`      |   8.961 ms (5%) |           | 155.19 KiB (1%) |        3015 |
| `["sum", "uniform", "reduce", "basesize=512"]`      |   9.322 ms (5%) |           |  76.31 KiB (1%) |        1486 |
| `["sum", "valley", "foldl"]`                        |  18.855 ms (5%) |           |   64 bytes (1%) |           3 |
| `["sum", "valley", "reduce", "basesize=128"]`       |   9.898 ms (5%) |           | 313.34 KiB (1%) |        6066 |
| `["sum", "valley", "reduce", "basesize=256"]`       |   9.799 ms (5%) |           | 155.16 KiB (1%) |        3013 |
| `["sum", "valley", "reduce", "basesize=512"]`       |   9.790 ms (5%) |           |  76.33 KiB (1%) |        1487 |
| `["words", "nthreads=1"]`                           |  51.598 ms (5%) |  7.935 ms |  63.28 MiB (1%) |     2067769 |
| `["words", "nthreads=2"]`                           |  26.495 ms (5%) |           |  64.37 MiB (1%) |     2079997 |
| `["words", "nthreads=4"]`                           |  26.311 ms (5%) |           |  65.00 MiB (1%) |     2086203 |

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
       #1  2095 MHz      69034 s          0 s       2897 s      58003 s          0 s
       #2  2095 MHz      80687 s          0 s       2906 s      46604 s          0 s
       
  Memory: 6.764884948730469 GB (2891.62890625 MB free)
  Uptime: 1324.0 sec
  Load Avg:  1.701171875  1.568359375  1.1005859375
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

