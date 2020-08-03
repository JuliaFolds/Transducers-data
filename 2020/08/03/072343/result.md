# Multi-thread benchmark result

* Pull request commit: [`e2012140b5a074b31876264ce83234aa67b53a8e`](https://github.com/JuliaFolds/Transducers.jl/commit/e2012140b5a074b31876264ce83234aa67b53a8e)
* Pull request: <https://github.com/JuliaFolds/Transducers.jl/pull/390> (Use protected branch instead of manual listing in .mergify.yml)

# Judge result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmarks:
    - Target: 3 Aug 2020 - 07:18
    - Baseline: 3 Aug 2020 - 07:23
* Package commits:
    - Target: 5105e4
    - Baseline: 64beaa
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
| `["collect", "unordered", "basesize=1"]`            |                1.07 (5%) :x: |    1.00 (1%)  |
| `["collect", "unordered", "basesize=1024"]`         | 0.91 (5%) :white_check_mark: | 1.01 (1%) :x: |
| `["findfirst", "n=500", "reduce", "basesize=128"]`  |                1.13 (5%) :x: |    1.00 (1%)  |
| `["findfirst", "n=500", "reduce", "basesize=256"]`  |                1.11 (5%) :x: |    1.00 (1%)  |
| `["findfirst", "n=500", "reduce", "basesize=512"]`  |                1.10 (5%) :x: |    1.00 (1%)  |
| `["parallel_histogram", "comm", "basesize=16384"]`  | 0.93 (5%) :white_check_mark: |    1.00 (1%)  |
| `["parallel_histogram", "comm", "basesize=4096"]`   |                   0.96 (5%)  | 1.01 (1%) :x: |
| `["sum", "valley", "reduce", "basesize=128"]`       | 0.86 (5%) :white_check_mark: |    1.00 (1%)  |
| `["sum", "valley", "reduce", "basesize=256"]`       | 0.86 (5%) :white_check_mark: |    1.00 (1%)  |
| `["sum", "valley", "reduce", "basesize=512"]`       | 0.86 (5%) :white_check_mark: |    1.00 (1%)  |

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
       #1  2095 MHz      49159 s          0 s       2450 s      17581 s          0 s
       #2  2095 MHz      49979 s          0 s       2496 s      16960 s          0 s
       
  Memory: 6.7648773193359375 GB (2884.63671875 MB free)
  Uptime: 713.0 sec
  Load Avg:  1.62548828125  1.458984375  0.875
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
       #1  2095 MHz      73375 s          0 s       2881 s      21013 s          0 s
       #2  2095 MHz      69550 s          0 s       2991 s      24912 s          0 s
       
  Memory: 6.7648773193359375 GB (2880.203125 MB free)
  Uptime: 995.0 sec
  Load Avg:  1.71435546875  1.57373046875  1.07861328125
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-8.0.1 (ORCJIT, skylake)
```

---
# Target result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmark: 3 Aug 2020 - 7:18
* Package commit: 5105e4
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
| `["collect", "assoc", "basesize=1"]`                | 307.901 ms (5%) | 12.463 ms |  87.55 MiB (1%) |     1590799 |
| `["collect", "assoc", "basesize=1024"]`             | 193.457 ms (5%) |           |   1.84 MiB (1%) |        1811 |
| `["collect", "assoc", "basesize=32"]`               | 192.321 ms (5%) |           |   5.64 MiB (1%) |       54003 |
| `["collect", "seq"]`                                | 360.550 ms (5%) |           |   1.50 MiB (1%) |       32784 |
| `["collect", "unordered", "basesize=1"]`            | 403.594 ms (5%) |           |  29.14 MiB (1%) |      401645 |
| `["collect", "unordered", "basesize=1024"]`         | 315.545 ms (5%) |           | 968.61 KiB (1%) |       15083 |
| `["collect", "unordered", "basesize=32"]`           | 215.325 ms (5%) |           |   1.46 MiB (1%) |       15928 |
| `["findfirst", "n=1000", "foldl"]`                  | 585.028 ms (5%) |           |                 |             |
| `["findfirst", "n=1000", "reduce", "basesize=128"]` | 305.214 ms (5%) |           | 563.53 KiB (1%) |       10193 |
| `["findfirst", "n=1000", "reduce", "basesize=256"]` | 310.127 ms (5%) |           | 287.00 KiB (1%) |        5206 |
| `["findfirst", "n=1000", "reduce", "basesize=512"]` | 306.324 ms (5%) |           | 149.25 KiB (1%) |        2717 |
| `["findfirst", "n=400", "foldl"]`                   | 434.951 ms (5%) |           |                 |             |
| `["findfirst", "n=400", "reduce", "basesize=128"]`  | 225.968 ms (5%) |           |   1.02 MiB (1%) |       18869 |
| `["findfirst", "n=400", "reduce", "basesize=256"]`  | 223.947 ms (5%) |           | 525.34 KiB (1%) |        9518 |
| `["findfirst", "n=400", "reduce", "basesize=512"]`  | 222.597 ms (5%) |           | 266.94 KiB (1%) |        4857 |
| `["findfirst", "n=500", "foldl"]`                   |  71.865 ms (5%) |           |                 |             |
| `["findfirst", "n=500", "reduce", "basesize=128"]`  |  41.884 ms (5%) |           | 157.23 KiB (1%) |        2840 |
| `["findfirst", "n=500", "reduce", "basesize=256"]`  |  41.408 ms (5%) |           |  84.50 KiB (1%) |        1530 |
| `["findfirst", "n=500", "reduce", "basesize=512"]`  |  44.062 ms (5%) |           |  48.30 KiB (1%) |         878 |
| `["overhead", "default"]`                           | 153.101 μs (5%) |           | 146.25 KiB (1%) |        2632 |
| `["overhead", "stoppable=false"]`                   | 150.201 μs (5%) |           | 146.28 KiB (1%) |        2633 |
| `["overhead", "stoppable=true"]`                    | 269.102 μs (5%) |           | 146.55 KiB (1%) |        2650 |
| `["parallel_histogram", "assoc", "basesize=16384"]` |   3.687 ms (5%) |           | 732.06 KiB (1%) |         103 |
| `["parallel_histogram", "assoc", "basesize=4096"]`  |   4.189 ms (5%) |           |   1.80 MiB (1%) |         497 |
| `["parallel_histogram", "assoc", "basesize=8192"]`  |   3.949 ms (5%) |           |   1.43 MiB (1%) |         242 |
| `["parallel_histogram", "comm", "basesize=16384"]`  |  13.462 ms (5%) |           |   1.22 MiB (1%) |         159 |
| `["parallel_histogram", "comm", "basesize=4096"]`   |  22.808 ms (5%) |           |   1.08 MiB (1%) |        5225 |
| `["parallel_histogram", "comm", "basesize=8192"]`   |  19.099 ms (5%) |           |   1.27 MiB (1%) |        3152 |
| `["parallel_histogram", "seq"]`                     |   6.712 ms (5%) |           | 364.61 KiB (1%) |          24 |
| `["sum", "random", "foldl"]`                        |  13.661 ms (5%) |           |   64 bytes (1%) |           3 |
| `["sum", "random", "reduce", "basesize=128"]`       |   8.102 ms (5%) |           | 313.41 KiB (1%) |        6070 |
| `["sum", "random", "reduce", "basesize=256"]`       |   7.929 ms (5%) |           | 155.19 KiB (1%) |        3015 |
| `["sum", "random", "reduce", "basesize=512"]`       |   7.847 ms (5%) |           |  76.33 KiB (1%) |        1487 |
| `["sum", "uniform", "foldl"]`                       |  13.278 ms (5%) |           |   64 bytes (1%) |           3 |
| `["sum", "uniform", "reduce", "basesize=128"]`      |   7.868 ms (5%) |           | 313.45 KiB (1%) |        6073 |
| `["sum", "uniform", "reduce", "basesize=256"]`      |   7.726 ms (5%) |           | 155.14 KiB (1%) |        3012 |
| `["sum", "uniform", "reduce", "basesize=512"]`      |   7.659 ms (5%) |           |  76.31 KiB (1%) |        1486 |
| `["sum", "valley", "foldl"]`                        |  13.402 ms (5%) |           |   64 bytes (1%) |           3 |
| `["sum", "valley", "reduce", "basesize=128"]`       |   7.030 ms (5%) |           | 313.31 KiB (1%) |        6064 |
| `["sum", "valley", "reduce", "basesize=256"]`       |   6.887 ms (5%) |           | 155.16 KiB (1%) |        3013 |
| `["sum", "valley", "reduce", "basesize=512"]`       |   6.781 ms (5%) |           |  76.34 KiB (1%) |        1488 |
| `["words", "nthreads=1"]`                           |  36.800 ms (5%) |  6.054 ms |  63.04 MiB (1%) |     2059743 |
| `["words", "nthreads=2"]`                           |  19.471 ms (5%) |           |  64.13 MiB (1%) |     2071913 |
| `["words", "nthreads=4"]`                           |  19.681 ms (5%) |           |  64.76 MiB (1%) |     2078137 |

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
       #1  2095 MHz      49159 s          0 s       2450 s      17581 s          0 s
       #2  2095 MHz      49979 s          0 s       2496 s      16960 s          0 s
       
  Memory: 6.7648773193359375 GB (2884.63671875 MB free)
  Uptime: 713.0 sec
  Load Avg:  1.62548828125  1.458984375  0.875
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-8.0.1 (ORCJIT, skylake)
```

---
# Baseline result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmark: 3 Aug 2020 - 7:23
* Package commit: 64beaa
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

| ID                                                  | time            | GC time  | memory          | allocations |
|-----------------------------------------------------|----------------:|---------:|----------------:|------------:|
| `["collect", "assoc", "basesize=1"]`                | 303.008 ms (5%) | 9.742 ms |  87.55 MiB (1%) |     1590774 |
| `["collect", "assoc", "basesize=1024"]`             | 186.091 ms (5%) |          |   1.84 MiB (1%) |        1811 |
| `["collect", "assoc", "basesize=32"]`               | 194.508 ms (5%) |          |   5.64 MiB (1%) |       54010 |
| `["collect", "seq"]`                                | 363.418 ms (5%) |          |   1.50 MiB (1%) |       32784 |
| `["collect", "unordered", "basesize=1"]`            | 375.659 ms (5%) |          |  29.15 MiB (1%) |      402389 |
| `["collect", "unordered", "basesize=1024"]`         | 347.221 ms (5%) |          | 956.63 KiB (1%) |       14271 |
| `["collect", "unordered", "basesize=32"]`           | 211.694 ms (5%) |          |   1.46 MiB (1%) |       16023 |
| `["findfirst", "n=1000", "foldl"]`                  | 582.663 ms (5%) |          |                 |             |
| `["findfirst", "n=1000", "reduce", "basesize=128"]` | 298.848 ms (5%) |          | 563.48 KiB (1%) |       10190 |
| `["findfirst", "n=1000", "reduce", "basesize=256"]` | 299.500 ms (5%) |          | 287.00 KiB (1%) |        5206 |
| `["findfirst", "n=1000", "reduce", "basesize=512"]` | 304.304 ms (5%) |          | 149.28 KiB (1%) |        2719 |
| `["findfirst", "n=400", "foldl"]`                   | 428.591 ms (5%) |          |                 |             |
| `["findfirst", "n=400", "reduce", "basesize=128"]`  | 224.366 ms (5%) |          |   1.02 MiB (1%) |       18881 |
| `["findfirst", "n=400", "reduce", "basesize=256"]`  | 226.824 ms (5%) |          | 525.41 KiB (1%) |        9522 |
| `["findfirst", "n=400", "reduce", "basesize=512"]`  | 220.316 ms (5%) |          | 266.94 KiB (1%) |        4857 |
| `["findfirst", "n=500", "foldl"]`                   |  70.928 ms (5%) |          |                 |             |
| `["findfirst", "n=500", "reduce", "basesize=128"]`  |  37.136 ms (5%) |          | 157.28 KiB (1%) |        2843 |
| `["findfirst", "n=500", "reduce", "basesize=256"]`  |  37.256 ms (5%) |          |  84.50 KiB (1%) |        1530 |
| `["findfirst", "n=500", "reduce", "basesize=512"]`  |  40.006 ms (5%) |          |  48.30 KiB (1%) |         878 |
| `["overhead", "default"]`                           | 153.701 μs (5%) |          | 146.25 KiB (1%) |        2632 |
| `["overhead", "stoppable=false"]`                   | 155.301 μs (5%) |          | 146.27 KiB (1%) |        2632 |
| `["overhead", "stoppable=true"]`                    | 280.001 μs (5%) |          | 146.55 KiB (1%) |        2650 |
| `["parallel_histogram", "assoc", "basesize=16384"]` |   3.677 ms (5%) |          | 732.06 KiB (1%) |         103 |
| `["parallel_histogram", "assoc", "basesize=4096"]`  |   4.179 ms (5%) |          |   1.80 MiB (1%) |         496 |
| `["parallel_histogram", "assoc", "basesize=8192"]`  |   3.927 ms (5%) |          |   1.43 MiB (1%) |         242 |
| `["parallel_histogram", "comm", "basesize=16384"]`  |  14.406 ms (5%) |          |   1.22 MiB (1%) |         159 |
| `["parallel_histogram", "comm", "basesize=4096"]`   |  23.760 ms (5%) |          |   1.06 MiB (1%) |        5986 |
| `["parallel_histogram", "comm", "basesize=8192"]`   |  19.234 ms (5%) |          |   1.26 MiB (1%) |        2445 |
| `["parallel_histogram", "seq"]`                     |   6.703 ms (5%) |          | 364.61 KiB (1%) |          24 |
| `["sum", "random", "foldl"]`                        |  13.110 ms (5%) |          |   64 bytes (1%) |           3 |
| `["sum", "random", "reduce", "basesize=128"]`       |   8.012 ms (5%) |          | 313.41 KiB (1%) |        6070 |
| `["sum", "random", "reduce", "basesize=256"]`       |   7.839 ms (5%) |          | 155.14 KiB (1%) |        3012 |
| `["sum", "random", "reduce", "basesize=512"]`       |   7.770 ms (5%) |          |  76.31 KiB (1%) |        1486 |
| `["sum", "uniform", "foldl"]`                       |  12.934 ms (5%) |          |   64 bytes (1%) |           3 |
| `["sum", "uniform", "reduce", "basesize=128"]`      |   7.866 ms (5%) |          | 313.44 KiB (1%) |        6072 |
| `["sum", "uniform", "reduce", "basesize=256"]`      |   7.688 ms (5%) |          | 155.14 KiB (1%) |        3012 |
| `["sum", "uniform", "reduce", "basesize=512"]`      |   7.607 ms (5%) |          |  76.31 KiB (1%) |        1486 |
| `["sum", "valley", "foldl"]`                        |  13.840 ms (5%) |          |   64 bytes (1%) |           3 |
| `["sum", "valley", "reduce", "basesize=128"]`       |   8.189 ms (5%) |          | 313.34 KiB (1%) |        6066 |
| `["sum", "valley", "reduce", "basesize=256"]`       |   7.991 ms (5%) |          | 155.16 KiB (1%) |        3013 |
| `["sum", "valley", "reduce", "basesize=512"]`       |   7.855 ms (5%) |          |  76.33 KiB (1%) |        1487 |
| `["words", "nthreads=1"]`                           |  36.982 ms (5%) | 5.976 ms |  63.29 MiB (1%) |     2068004 |
| `["words", "nthreads=2"]`                           |  18.997 ms (5%) |          |  63.90 MiB (1%) |     2076144 |
| `["words", "nthreads=4"]`                           |  19.812 ms (5%) |          |  65.17 MiB (1%) |     2088537 |

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
       #1  2095 MHz      73375 s          0 s       2881 s      21013 s          0 s
       #2  2095 MHz      69550 s          0 s       2991 s      24912 s          0 s
       
  Memory: 6.7648773193359375 GB (2880.203125 MB free)
  Uptime: 995.0 sec
  Load Avg:  1.71435546875  1.57373046875  1.07861328125
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
    CPU MHz:             2095.077
    BogoMIPS:            4190.15
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

