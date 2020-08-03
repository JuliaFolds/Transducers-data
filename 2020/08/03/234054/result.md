# Multi-thread benchmark result

* Pull request commit: [`87c2409b804f19647f5c830e0b2f85b1cb24be39`](https://github.com/JuliaFolds/Transducers.jl/commit/87c2409b804f19647f5c830e0b2f85b1cb24be39)
* Pull request: <https://github.com/JuliaFolds/Transducers.jl/pull/385> (Add more specialization hints to the compiler)

# Judge result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmarks:
    - Target: 3 Aug 2020 - 23:35
    - Baseline: 3 Aug 2020 - 23:40
* Package commits:
    - Target: 21d6eb
    - Baseline: 84af4e
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
| `["collect", "unordered", "basesize=1"]`            | 0.93 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["collect", "unordered", "basesize=1024"]`         | 0.80 (5%) :white_check_mark: | 0.90 (1%) :white_check_mark: |
| `["parallel_histogram", "assoc", "basesize=4096"]`  |                   0.99 (5%)  | 0.87 (1%) :white_check_mark: |
| `["parallel_histogram", "comm", "basesize=4096"]`   |                   1.03 (5%)  |                1.01 (1%) :x: |
| `["parallel_histogram", "comm", "basesize=8192"]`   |                   1.00 (5%)  | 0.98 (1%) :white_check_mark: |
| `["words", "nthreads=1"]`                           | 0.77 (5%) :white_check_mark: |                   0.99 (1%)  |
| `["words", "nthreads=2"]`                           | 0.80 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["words", "nthreads=4"]`                           | 0.76 (5%) :white_check_mark: |                   0.99 (1%)  |

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
       #1  2095 MHz      48991 s          0 s       2370 s      23937 s          0 s
       #2  2095 MHz      52631 s          0 s       2321 s      20403 s          0 s
       
  Memory: 6.764884948730469 GB (2878.59375 MB free)
  Uptime: 774.0 sec
  Load Avg:  1.54931640625  1.4404296875  0.859375
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
       #1  2095 MHz      75089 s          0 s       2825 s      27406 s          0 s
       #2  2095 MHz      72463 s          0 s       2797 s      29966 s          0 s
       
  Memory: 6.764884948730469 GB (2928.5 MB free)
  Uptime: 1076.0 sec
  Load Avg:  1.6591796875  1.54296875  1.068359375
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-8.0.1 (ORCJIT, skylake)
```

---
# Target result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmark: 3 Aug 2020 - 23:35
* Package commit: 21d6eb
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
| `["collect", "assoc", "basesize=1"]`                | 369.101 ms (5%) | 11.160 ms |  87.55 MiB (1%) |     1590741 |
| `["collect", "assoc", "basesize=1024"]`             | 227.836 ms (5%) |           |   1.84 MiB (1%) |        1811 |
| `["collect", "assoc", "basesize=32"]`               | 235.386 ms (5%) |           |   5.64 MiB (1%) |       54009 |
| `["collect", "seq"]`                                | 452.531 ms (5%) |           |   1.50 MiB (1%) |       32784 |
| `["collect", "unordered", "basesize=1"]`            | 453.156 ms (5%) |           |  29.16 MiB (1%) |      403418 |
| `["collect", "unordered", "basesize=1024"]`         | 252.354 ms (5%) |           | 758.56 KiB (1%) |        1595 |
| `["collect", "unordered", "basesize=32"]`           | 261.538 ms (5%) |           |   1.47 MiB (1%) |       16644 |
| `["findfirst", "n=1000", "foldl"]`                  | 725.289 ms (5%) |           |                 |             |
| `["findfirst", "n=1000", "reduce", "basesize=128"]` | 367.880 ms (5%) |           | 563.45 KiB (1%) |       10188 |
| `["findfirst", "n=1000", "reduce", "basesize=256"]` | 366.002 ms (5%) |           | 287.22 KiB (1%) |        5220 |
| `["findfirst", "n=1000", "reduce", "basesize=512"]` | 375.982 ms (5%) |           | 149.31 KiB (1%) |        2721 |
| `["findfirst", "n=400", "foldl"]`                   | 541.147 ms (5%) |           |                 |             |
| `["findfirst", "n=400", "reduce", "basesize=128"]`  | 277.593 ms (5%) |           |   1.02 MiB (1%) |       18923 |
| `["findfirst", "n=400", "reduce", "basesize=256"]`  | 274.762 ms (5%) |           | 526.03 KiB (1%) |        9562 |
| `["findfirst", "n=400", "reduce", "basesize=512"]`  | 276.291 ms (5%) |           | 267.19 KiB (1%) |        4873 |
| `["findfirst", "n=500", "foldl"]`                   |  92.472 ms (5%) |           |                 |             |
| `["findfirst", "n=500", "reduce", "basesize=128"]`  |  47.848 ms (5%) |           | 157.25 KiB (1%) |        2841 |
| `["findfirst", "n=500", "reduce", "basesize=256"]`  |  47.289 ms (5%) |           |  84.50 KiB (1%) |        1530 |
| `["findfirst", "n=500", "reduce", "basesize=512"]`  |  50.460 ms (5%) |           |  48.30 KiB (1%) |         878 |
| `["overhead", "default"]`                           | 197.708 μs (5%) |           | 146.27 KiB (1%) |        2633 |
| `["overhead", "stoppable=false"]`                   | 197.208 μs (5%) |           | 146.25 KiB (1%) |        2631 |
| `["overhead", "stoppable=true"]`                    | 341.613 μs (5%) |           | 146.52 KiB (1%) |        2648 |
| `["parallel_histogram", "assoc", "basesize=16384"]` |   4.974 ms (5%) |           | 732.06 KiB (1%) |         103 |
| `["parallel_histogram", "assoc", "basesize=4096"]`  |   5.637 ms (5%) |           |   1.80 MiB (1%) |         497 |
| `["parallel_histogram", "assoc", "basesize=8192"]`  |   5.318 ms (5%) |           |   1.43 MiB (1%) |         243 |
| `["parallel_histogram", "comm", "basesize=16384"]`  |  15.562 ms (5%) |           |   1.22 MiB (1%) |         159 |
| `["parallel_histogram", "comm", "basesize=4096"]`   |  23.852 ms (5%) |           |   1.07 MiB (1%) |        3298 |
| `["parallel_histogram", "comm", "basesize=8192"]`   |  20.511 ms (5%) |  2.095 ms |   1.23 MiB (1%) |        1080 |
| `["parallel_histogram", "seq"]`                     |   8.837 ms (5%) |           | 364.61 KiB (1%) |          24 |
| `["sum", "random", "foldl"]`                        |  17.738 ms (5%) |           |   64 bytes (1%) |           3 |
| `["sum", "random", "reduce", "basesize=128"]`       |   9.276 ms (5%) |           | 313.42 KiB (1%) |        6071 |
| `["sum", "random", "reduce", "basesize=256"]`       |   9.088 ms (5%) |           | 155.14 KiB (1%) |        3012 |
| `["sum", "random", "reduce", "basesize=512"]`       |   8.979 ms (5%) |           |  76.31 KiB (1%) |        1486 |
| `["sum", "uniform", "foldl"]`                       |  17.421 ms (5%) |           |   64 bytes (1%) |           3 |
| `["sum", "uniform", "reduce", "basesize=128"]`      |   9.115 ms (5%) |           | 313.45 KiB (1%) |        6073 |
| `["sum", "uniform", "reduce", "basesize=256"]`      |   9.019 ms (5%) |           | 155.17 KiB (1%) |        3014 |
| `["sum", "uniform", "reduce", "basesize=512"]`      |   8.921 ms (5%) |           |  76.31 KiB (1%) |        1486 |
| `["sum", "valley", "foldl"]`                        |  17.768 ms (5%) |           |   64 bytes (1%) |           3 |
| `["sum", "valley", "reduce", "basesize=128"]`       |   9.479 ms (5%) |           | 313.34 KiB (1%) |        6066 |
| `["sum", "valley", "reduce", "basesize=256"]`       |   9.158 ms (5%) |           | 155.16 KiB (1%) |        3013 |
| `["sum", "valley", "reduce", "basesize=512"]`       |   9.088 ms (5%) |           |  76.31 KiB (1%) |        1486 |
| `["words", "nthreads=1"]`                           |  35.802 ms (5%) |  7.004 ms |  63.02 MiB (1%) |     2059235 |
| `["words", "nthreads=2"]`                           |  19.694 ms (5%) |           |  64.11 MiB (1%) |     2071543 |
| `["words", "nthreads=4"]`                           |  19.711 ms (5%) |           |  64.74 MiB (1%) |     2077743 |

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
       #1  2095 MHz      48991 s          0 s       2370 s      23937 s          0 s
       #2  2095 MHz      52631 s          0 s       2321 s      20403 s          0 s
       
  Memory: 6.764884948730469 GB (2878.59375 MB free)
  Uptime: 774.0 sec
  Load Avg:  1.54931640625  1.4404296875  0.859375
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-8.0.1 (ORCJIT, skylake)
```

---
# Baseline result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmark: 3 Aug 2020 - 23:40
* Package commit: 84af4e
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
| `["collect", "assoc", "basesize=1"]`                | 369.629 ms (5%) | 11.928 ms |  87.55 MiB (1%) |     1590749 |
| `["collect", "assoc", "basesize=1024"]`             | 233.067 ms (5%) |           |   1.84 MiB (1%) |        1812 |
| `["collect", "assoc", "basesize=32"]`               | 240.209 ms (5%) |           |   5.64 MiB (1%) |       54002 |
| `["collect", "seq"]`                                | 455.955 ms (5%) |           |   1.50 MiB (1%) |       32784 |
| `["collect", "unordered", "basesize=1"]`            | 488.295 ms (5%) |           |  29.16 MiB (1%) |      403510 |
| `["collect", "unordered", "basesize=1024"]`         | 316.935 ms (5%) |           | 839.02 KiB (1%) |        6453 |
| `["collect", "unordered", "basesize=32"]`           | 265.737 ms (5%) |           |   1.46 MiB (1%) |       16327 |
| `["findfirst", "n=1000", "foldl"]`                  | 718.767 ms (5%) |           |                 |             |
| `["findfirst", "n=1000", "reduce", "basesize=128"]` | 367.161 ms (5%) |           | 563.56 KiB (1%) |       10195 |
| `["findfirst", "n=1000", "reduce", "basesize=256"]` | 366.087 ms (5%) |           | 287.06 KiB (1%) |        5210 |
| `["findfirst", "n=1000", "reduce", "basesize=512"]` | 370.424 ms (5%) |           | 149.38 KiB (1%) |        2725 |
| `["findfirst", "n=400", "foldl"]`                   | 539.629 ms (5%) |           |                 |             |
| `["findfirst", "n=400", "reduce", "basesize=128"]`  | 278.232 ms (5%) |           |   1.02 MiB (1%) |       18898 |
| `["findfirst", "n=400", "reduce", "basesize=256"]`  | 274.735 ms (5%) |           | 525.92 KiB (1%) |        9555 |
| `["findfirst", "n=400", "reduce", "basesize=512"]`  | 283.140 ms (5%) |           | 267.16 KiB (1%) |        4871 |
| `["findfirst", "n=500", "foldl"]`                   |  91.829 ms (5%) |           |                 |             |
| `["findfirst", "n=500", "reduce", "basesize=128"]`  |  47.677 ms (5%) |           | 157.25 KiB (1%) |        2841 |
| `["findfirst", "n=500", "reduce", "basesize=256"]`  |  47.503 ms (5%) |           |  84.55 KiB (1%) |        1533 |
| `["findfirst", "n=500", "reduce", "basesize=512"]`  |  50.647 ms (5%) |           |  48.30 KiB (1%) |         878 |
| `["overhead", "default"]`                           | 196.315 μs (5%) |           | 146.27 KiB (1%) |        2633 |
| `["overhead", "stoppable=false"]`                   | 197.416 μs (5%) |           | 146.28 KiB (1%) |        2633 |
| `["overhead", "stoppable=true"]`                    | 340.727 μs (5%) |           | 146.53 KiB (1%) |        2649 |
| `["parallel_histogram", "assoc", "basesize=16384"]` |   4.973 ms (5%) |           | 732.06 KiB (1%) |         103 |
| `["parallel_histogram", "assoc", "basesize=4096"]`  |   5.708 ms (5%) |           |   2.07 MiB (1%) |         503 |
| `["parallel_histogram", "assoc", "basesize=8192"]`  |   5.312 ms (5%) |           |   1.43 MiB (1%) |         242 |
| `["parallel_histogram", "comm", "basesize=16384"]`  |  15.690 ms (5%) |           |   1.22 MiB (1%) |         158 |
| `["parallel_histogram", "comm", "basesize=4096"]`   |  23.126 ms (5%) |           |   1.06 MiB (1%) |        5868 |
| `["parallel_histogram", "comm", "basesize=8192"]`   |  20.437 ms (5%) |           |   1.26 MiB (1%) |        2476 |
| `["parallel_histogram", "seq"]`                     |   8.816 ms (5%) |           | 364.61 KiB (1%) |          24 |
| `["sum", "random", "foldl"]`                        |  17.987 ms (5%) |           |   64 bytes (1%) |           3 |
| `["sum", "random", "reduce", "basesize=128"]`       |   9.396 ms (5%) |           | 313.41 KiB (1%) |        6070 |
| `["sum", "random", "reduce", "basesize=256"]`       |   9.225 ms (5%) |           | 155.17 KiB (1%) |        3014 |
| `["sum", "random", "reduce", "basesize=512"]`       |   9.117 ms (5%) |           |  76.34 KiB (1%) |        1488 |
| `["sum", "uniform", "foldl"]`                       |  17.282 ms (5%) |           |   64 bytes (1%) |           3 |
| `["sum", "uniform", "reduce", "basesize=128"]`      |   9.167 ms (5%) |           | 313.38 KiB (1%) |        6068 |
| `["sum", "uniform", "reduce", "basesize=256"]`      |   8.912 ms (5%) |           | 155.16 KiB (1%) |        3013 |
| `["sum", "uniform", "reduce", "basesize=512"]`      |   8.760 ms (5%) |           |  76.31 KiB (1%) |        1486 |
| `["sum", "valley", "foldl"]`                        |  17.479 ms (5%) |           |   64 bytes (1%) |           3 |
| `["sum", "valley", "reduce", "basesize=128"]`       |   9.392 ms (5%) |           | 313.33 KiB (1%) |        6065 |
| `["sum", "valley", "reduce", "basesize=256"]`       |   9.226 ms (5%) |           | 155.16 KiB (1%) |        3013 |
| `["sum", "valley", "reduce", "basesize=512"]`       |   9.089 ms (5%) |           |  76.34 KiB (1%) |        1488 |
| `["words", "nthreads=1"]`                           |  46.449 ms (5%) |  6.766 ms |  63.36 MiB (1%) |     2070066 |
| `["words", "nthreads=2"]`                           |  24.659 ms (5%) |           |  63.96 MiB (1%) |     2078256 |
| `["words", "nthreads=4"]`                           |  26.030 ms (5%) |           |  65.24 MiB (1%) |     2090764 |

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
       #1  2095 MHz      75089 s          0 s       2825 s      27406 s          0 s
       #2  2095 MHz      72463 s          0 s       2797 s      29966 s          0 s
       
  Memory: 6.764884948730469 GB (2928.5 MB free)
  Uptime: 1076.0 sec
  Load Avg:  1.6591796875  1.54296875  1.068359375
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
    CPU MHz:             2095.162
    BogoMIPS:            4190.32
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

