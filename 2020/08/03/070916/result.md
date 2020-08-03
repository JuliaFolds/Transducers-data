# Multi-thread benchmark result

* Pull request commit: [`c090e2d97a872b87ce3c9c6014c8129a432bd15a`](https://github.com/JuliaFolds/Transducers.jl/commit/c090e2d97a872b87ce3c9c6014c8129a432bd15a)
* Pull request: <https://github.com/JuliaFolds/Transducers.jl/pull/390> (Use protected branch instead of manual listing in .mergify.yml)

# Judge result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmarks:
    - Target: 3 Aug 2020 - 07:04
    - Baseline: 3 Aug 2020 - 07:08
* Package commits:
    - Target: 32cfe3
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

| ID                                                  | time ratio                   | memory ratio                 |
|-----------------------------------------------------|------------------------------|------------------------------|
| `["collect", "unordered", "basesize=1024"]`         | 0.78 (5%) :white_check_mark: | 0.84 (1%) :white_check_mark: |
| `["findfirst", "n=400", "foldl"]`                   |                1.07 (5%) :x: |                   1.00 (1%)  |
| `["findfirst", "n=400", "reduce", "basesize=256"]`  |                1.06 (5%) :x: |                   1.00 (1%)  |
| `["findfirst", "n=400", "reduce", "basesize=512"]`  |                1.10 (5%) :x: |                   1.00 (1%)  |
| `["overhead", "stoppable=true"]`                    |                1.09 (5%) :x: |                   1.00 (1%)  |
| `["parallel_histogram", "comm", "basesize=16384"]`  |                   0.98 (5%)  |                1.27 (1%) :x: |
| `["parallel_histogram", "comm", "basesize=8192"]`   |                1.09 (5%) :x: |                1.03 (1%) :x: |

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
       #1  2095 MHz      51307 s          0 s       2294 s      26981 s          0 s
       #2  2095 MHz      47504 s          0 s       2355 s      30958 s          0 s
       
  Memory: 6.764884948730469 GB (2883.125 MB free)
  Uptime: 826.0 sec
  Load Avg:  1.71435546875  1.50634765625  0.9033203125
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
       #1  2095 MHz      71180 s          0 s       2764 s      34438 s          0 s
       #2  2095 MHz      71169 s          0 s       2774 s      34672 s          0 s
       
  Memory: 6.764884948730469 GB (2884.25 MB free)
  Uptime: 1106.0 sec
  Load Avg:  1.7216796875  1.58642578125  1.09521484375
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-8.0.1 (ORCJIT, skylake)
```

---
# Target result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmark: 3 Aug 2020 - 7:4
* Package commit: 32cfe3
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
| `["collect", "assoc", "basesize=1"]`                | 295.134 ms (5%) | 9.384 ms |  87.55 MiB (1%) |     1590739 |
| `["collect", "assoc", "basesize=1024"]`             | 180.807 ms (5%) |          |   1.84 MiB (1%) |        1811 |
| `["collect", "assoc", "basesize=32"]`               | 184.878 ms (5%) |          |   5.64 MiB (1%) |       54010 |
| `["collect", "seq"]`                                | 357.260 ms (5%) |          |   1.50 MiB (1%) |       32784 |
| `["collect", "unordered", "basesize=1"]`            | 381.196 ms (5%) |          |  29.17 MiB (1%) |      403699 |
| `["collect", "unordered", "basesize=1024"]`         | 232.830 ms (5%) |          | 793.28 KiB (1%) |        3817 |
| `["collect", "unordered", "basesize=32"]`           | 203.944 ms (5%) |          |   1.47 MiB (1%) |       16613 |
| `["findfirst", "n=1000", "foldl"]`                  | 560.916 ms (5%) |          |                 |             |
| `["findfirst", "n=1000", "reduce", "basesize=128"]` | 291.761 ms (5%) |          | 563.36 KiB (1%) |       10182 |
| `["findfirst", "n=1000", "reduce", "basesize=256"]` | 298.041 ms (5%) |          | 287.00 KiB (1%) |        5206 |
| `["findfirst", "n=1000", "reduce", "basesize=512"]` | 292.191 ms (5%) |          | 149.22 KiB (1%) |        2715 |
| `["findfirst", "n=400", "foldl"]`                   | 446.232 ms (5%) |          |                 |             |
| `["findfirst", "n=400", "reduce", "basesize=128"]`  | 223.226 ms (5%) |          |   1.02 MiB (1%) |       18853 |
| `["findfirst", "n=400", "reduce", "basesize=256"]`  | 234.755 ms (5%) |          | 525.41 KiB (1%) |        9522 |
| `["findfirst", "n=400", "reduce", "basesize=512"]`  | 242.169 ms (5%) |          | 267.14 KiB (1%) |        4870 |
| `["findfirst", "n=500", "foldl"]`                   |  70.641 ms (5%) |          |                 |             |
| `["findfirst", "n=500", "reduce", "basesize=128"]`  |  36.978 ms (5%) |          | 157.23 KiB (1%) |        2840 |
| `["findfirst", "n=500", "reduce", "basesize=256"]`  |  36.765 ms (5%) |          |  84.50 KiB (1%) |        1530 |
| `["findfirst", "n=500", "reduce", "basesize=512"]`  |  39.037 ms (5%) |          |  48.30 KiB (1%) |         878 |
| `["overhead", "default"]`                           | 152.207 μs (5%) |          | 146.27 KiB (1%) |        2633 |
| `["overhead", "stoppable=false"]`                   | 155.807 μs (5%) |          | 146.28 KiB (1%) |        2633 |
| `["overhead", "stoppable=true"]`                    | 275.813 μs (5%) |          | 146.55 KiB (1%) |        2650 |
| `["parallel_histogram", "assoc", "basesize=16384"]` |   3.707 ms (5%) |          | 732.06 KiB (1%) |         103 |
| `["parallel_histogram", "assoc", "basesize=4096"]`  |   4.252 ms (5%) |          |   1.80 MiB (1%) |         497 |
| `["parallel_histogram", "assoc", "basesize=8192"]`  |   3.999 ms (5%) |          |   1.43 MiB (1%) |         242 |
| `["parallel_histogram", "comm", "basesize=16384"]`  |  13.593 ms (5%) |          |   1.22 MiB (1%) |         185 |
| `["parallel_histogram", "comm", "basesize=4096"]`   |  19.925 ms (5%) |          |   1.05 MiB (1%) |        5429 |
| `["parallel_histogram", "comm", "basesize=8192"]`   |  19.234 ms (5%) |          |   1.28 MiB (1%) |        3786 |
| `["parallel_histogram", "seq"]`                     |   6.749 ms (5%) |          | 364.61 KiB (1%) |          24 |
| `["sum", "random", "foldl"]`                        |  13.356 ms (5%) |          |   64 bytes (1%) |           3 |
| `["sum", "random", "reduce", "basesize=128"]`       |   6.995 ms (5%) |          | 313.38 KiB (1%) |        6068 |
| `["sum", "random", "reduce", "basesize=256"]`       |   6.840 ms (5%) |          | 155.14 KiB (1%) |        3012 |
| `["sum", "random", "reduce", "basesize=512"]`       |   6.742 ms (5%) |          |  76.33 KiB (1%) |        1487 |
| `["sum", "uniform", "foldl"]`                       |  12.895 ms (5%) |          |   64 bytes (1%) |           3 |
| `["sum", "uniform", "reduce", "basesize=128"]`      |   6.814 ms (5%) |          | 313.41 KiB (1%) |        6070 |
| `["sum", "uniform", "reduce", "basesize=256"]`      |   6.644 ms (5%) |          | 155.14 KiB (1%) |        3012 |
| `["sum", "uniform", "reduce", "basesize=512"]`      |   6.567 ms (5%) |          |  76.31 KiB (1%) |        1486 |
| `["sum", "valley", "foldl"]`                        |  13.363 ms (5%) |          |   64 bytes (1%) |           3 |
| `["sum", "valley", "reduce", "basesize=128"]`       |   7.050 ms (5%) |          | 313.27 KiB (1%) |        6061 |
| `["sum", "valley", "reduce", "basesize=256"]`       |   6.903 ms (5%) |          | 155.14 KiB (1%) |        3012 |
| `["sum", "valley", "reduce", "basesize=512"]`       |   6.807 ms (5%) |          |  76.31 KiB (1%) |        1486 |
| `["words", "nthreads=1"]`                           |  37.390 ms (5%) | 6.286 ms |  63.34 MiB (1%) |     2069145 |
| `["words", "nthreads=2"]`                           |  20.188 ms (5%) |          |  64.42 MiB (1%) |     2081321 |
| `["words", "nthreads=4"]`                           |  21.095 ms (5%) |          |  65.37 MiB (1%) |     2091730 |

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
       #1  2095 MHz      51307 s          0 s       2294 s      26981 s          0 s
       #2  2095 MHz      47504 s          0 s       2355 s      30958 s          0 s
       
  Memory: 6.764884948730469 GB (2883.125 MB free)
  Uptime: 826.0 sec
  Load Avg:  1.71435546875  1.50634765625  0.9033203125
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-8.0.1 (ORCJIT, skylake)
```

---
# Baseline result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmark: 3 Aug 2020 - 7:8
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
| `["collect", "assoc", "basesize=1"]`                | 292.704 ms (5%) | 8.540 ms |  87.55 MiB (1%) |     1590663 |
| `["collect", "assoc", "basesize=1024"]`             | 183.047 ms (5%) |          |   1.84 MiB (1%) |        1813 |
| `["collect", "assoc", "basesize=32"]`               | 183.486 ms (5%) |          |   5.64 MiB (1%) |       54022 |
| `["collect", "seq"]`                                | 348.544 ms (5%) |          |   1.50 MiB (1%) |       32784 |
| `["collect", "unordered", "basesize=1"]`            | 382.035 ms (5%) |          |  29.17 MiB (1%) |      403973 |
| `["collect", "unordered", "basesize=1024"]`         | 299.004 ms (5%) |          | 949.78 KiB (1%) |       13779 |
| `["collect", "unordered", "basesize=32"]`           | 207.334 ms (5%) |          |   1.47 MiB (1%) |       16479 |
| `["findfirst", "n=1000", "foldl"]`                  | 560.981 ms (5%) |          |                 |             |
| `["findfirst", "n=1000", "reduce", "basesize=128"]` | 293.478 ms (5%) |          | 563.42 KiB (1%) |       10186 |
| `["findfirst", "n=1000", "reduce", "basesize=256"]` | 289.229 ms (5%) |          | 287.02 KiB (1%) |        5207 |
| `["findfirst", "n=1000", "reduce", "basesize=512"]` | 295.496 ms (5%) |          | 149.23 KiB (1%) |        2716 |
| `["findfirst", "n=400", "foldl"]`                   | 418.975 ms (5%) |          |                 |             |
| `["findfirst", "n=400", "reduce", "basesize=128"]`  | 215.240 ms (5%) |          |   1.02 MiB (1%) |       18864 |
| `["findfirst", "n=400", "reduce", "basesize=256"]`  | 220.982 ms (5%) |          | 525.45 KiB (1%) |        9525 |
| `["findfirst", "n=400", "reduce", "basesize=512"]`  | 220.117 ms (5%) |          | 266.92 KiB (1%) |        4856 |
| `["findfirst", "n=500", "foldl"]`                   |  70.383 ms (5%) |          |                 |             |
| `["findfirst", "n=500", "reduce", "basesize=128"]`  |  36.537 ms (5%) |          | 157.23 KiB (1%) |        2840 |
| `["findfirst", "n=500", "reduce", "basesize=256"]`  |  36.055 ms (5%) |          |  84.50 KiB (1%) |        1530 |
| `["findfirst", "n=500", "reduce", "basesize=512"]`  |  39.119 ms (5%) |          |  48.30 KiB (1%) |         878 |
| `["overhead", "default"]`                           | 155.513 μs (5%) |          | 146.28 KiB (1%) |        2634 |
| `["overhead", "stoppable=false"]`                   | 151.613 μs (5%) |          | 146.28 KiB (1%) |        2633 |
| `["overhead", "stoppable=true"]`                    | 254.021 μs (5%) |          | 146.55 KiB (1%) |        2650 |
| `["parallel_histogram", "assoc", "basesize=16384"]` |   3.706 ms (5%) |          | 732.06 KiB (1%) |         103 |
| `["parallel_histogram", "assoc", "basesize=4096"]`  |   4.220 ms (5%) |          |   1.80 MiB (1%) |         496 |
| `["parallel_histogram", "assoc", "basesize=8192"]`  |   3.972 ms (5%) |          |   1.43 MiB (1%) |         242 |
| `["parallel_histogram", "comm", "basesize=16384"]`  |  13.806 ms (5%) |          | 983.22 KiB (1%) |         159 |
| `["parallel_histogram", "comm", "basesize=4096"]`   |  20.700 ms (5%) |          |   1.04 MiB (1%) |        4769 |
| `["parallel_histogram", "comm", "basesize=8192"]`   |  17.717 ms (5%) |          |   1.23 MiB (1%) |         970 |
| `["parallel_histogram", "seq"]`                     |   6.743 ms (5%) |          | 364.61 KiB (1%) |          24 |
| `["sum", "random", "foldl"]`                        |  13.291 ms (5%) |          |   64 bytes (1%) |           3 |
| `["sum", "random", "reduce", "basesize=128"]`       |   7.030 ms (5%) |          | 313.42 KiB (1%) |        6071 |
| `["sum", "random", "reduce", "basesize=256"]`       |   6.825 ms (5%) |          | 155.17 KiB (1%) |        3014 |
| `["sum", "random", "reduce", "basesize=512"]`       |   6.744 ms (5%) |          |  76.34 KiB (1%) |        1488 |
| `["sum", "uniform", "foldl"]`                       |  12.881 ms (5%) |          |   64 bytes (1%) |           3 |
| `["sum", "uniform", "reduce", "basesize=128"]`      |   6.816 ms (5%) |          | 313.33 KiB (1%) |        6065 |
| `["sum", "uniform", "reduce", "basesize=256"]`      |   6.662 ms (5%) |          | 155.16 KiB (1%) |        3013 |
| `["sum", "uniform", "reduce", "basesize=512"]`      |   6.557 ms (5%) |          |  76.31 KiB (1%) |        1486 |
| `["sum", "valley", "foldl"]`                        |  13.358 ms (5%) |          |   64 bytes (1%) |           3 |
| `["sum", "valley", "reduce", "basesize=128"]`       |   7.064 ms (5%) |          | 313.34 KiB (1%) |        6066 |
| `["sum", "valley", "reduce", "basesize=256"]`       |   6.891 ms (5%) |          | 155.16 KiB (1%) |        3013 |
| `["sum", "valley", "reduce", "basesize=512"]`       |   6.800 ms (5%) |          |  76.31 KiB (1%) |        1486 |
| `["words", "nthreads=1"]`                           |  36.902 ms (5%) | 5.971 ms |  63.35 MiB (1%) |     2069457 |
| `["words", "nthreads=2"]`                           |  19.304 ms (5%) |          |  64.43 MiB (1%) |     2081713 |
| `["words", "nthreads=4"]`                           |  20.825 ms (5%) |          |  65.38 MiB (1%) |     2092139 |

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
       #1  2095 MHz      71180 s          0 s       2764 s      34438 s          0 s
       #2  2095 MHz      71169 s          0 s       2774 s      34672 s          0 s
       
  Memory: 6.764884948730469 GB (2884.25 MB free)
  Uptime: 1106.0 sec
  Load Avg:  1.7216796875  1.58642578125  1.09521484375
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

