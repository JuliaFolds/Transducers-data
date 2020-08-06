# Multi-thread benchmark result

* Pull request commit: [`bf825b3a109fc793d9b33e1768c3b6b6b2916397`](https://github.com/JuliaFolds/Transducers.jl/commit/bf825b3a109fc793d9b33e1768c3b6b6b2916397)
* Pull request: <https://github.com/JuliaFolds/Transducers.jl/pull/397> (Define collect(::Foldable) rather than collect(::Eduction))

# Judge result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmarks:
    - Target: 6 Aug 2020 - 17:28
    - Baseline: 6 Aug 2020 - 17:33
* Package commits:
    - Target: 650576
    - Baseline: 3599fd
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
| `["collect", "unordered", "basesize=1024"]`         |                1.29 (5%) :x: |                1.17 (1%) :x: |
| `["overhead", "default"]`                           | 0.88 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["overhead", "stoppable=false"]`                   | 0.88 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["overhead", "stoppable=true"]`                    | 0.95 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["parallel_histogram", "assoc", "basesize=16384"]` |                1.12 (5%) :x: |                   1.00 (1%)  |
| `["parallel_histogram", "assoc", "basesize=4096"]`  |                   1.03 (5%)  |                1.15 (1%) :x: |
| `["parallel_histogram", "assoc", "basesize=8192"]`  |                1.07 (5%) :x: |                   1.00 (1%)  |
| `["parallel_histogram", "comm", "basesize=4096"]`   | 0.93 (5%) :white_check_mark: | 0.98 (1%) :white_check_mark: |
| `["parallel_histogram", "comm", "basesize=8192"]`   |                   0.96 (5%)  | 0.99 (1%) :white_check_mark: |
| `["sum", "valley", "reduce", "basesize=256"]`       | 0.91 (5%) :white_check_mark: |                   1.00 (1%)  |

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
       #1  2095 MHz      50854 s          0 s       2203 s      22207 s          0 s
       #2  2095 MHz      50744 s          0 s       2497 s      22828 s          0 s
       
  Memory: 6.764881134033203 GB (2990.015625 MB free)
  Uptime: 778.0 sec
  Load Avg:  1.7421875  1.5302734375  0.91162109375
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
       #1  2095 MHz      70833 s          0 s       2730 s      31673 s          0 s
       #2  2095 MHz      76748 s          0 s       2956 s      26414 s          0 s
       
  Memory: 6.764881134033203 GB (3024.6328125 MB free)
  Uptime: 1080.0 sec
  Load Avg:  1.6337890625  1.56591796875  1.09619140625
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-8.0.1 (ORCJIT, skylake)
```

---
# Target result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmark: 6 Aug 2020 - 17:28
* Package commit: 650576
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
| `["collect", "assoc", "basesize=1"]`                | 366.520 ms (5%) | 10.696 ms |  87.55 MiB (1%) |     1590819 |
| `["collect", "assoc", "basesize=1024"]`             | 228.971 ms (5%) |           |   1.84 MiB (1%) |        1812 |
| `["collect", "assoc", "basesize=32"]`               | 234.456 ms (5%) |           |   5.64 MiB (1%) |       54011 |
| `["collect", "seq"]`                                | 452.709 ms (5%) |           |   1.50 MiB (1%) |       32784 |
| `["collect", "unordered", "basesize=1"]`            | 467.754 ms (5%) |           |  29.16 MiB (1%) |      403483 |
| `["collect", "unordered", "basesize=1024"]`         | 359.978 ms (5%) |           | 931.17 KiB (1%) |       12687 |
| `["collect", "unordered", "basesize=32"]`           | 264.577 ms (5%) |           |   1.47 MiB (1%) |       16631 |
| `["findfirst", "n=1000", "foldl"]`                  | 734.967 ms (5%) |           |                 |             |
| `["findfirst", "n=1000", "reduce", "basesize=128"]` | 375.174 ms (5%) |           | 564.22 KiB (1%) |       10237 |
| `["findfirst", "n=1000", "reduce", "basesize=256"]` | 370.135 ms (5%) |           | 287.36 KiB (1%) |        5229 |
| `["findfirst", "n=1000", "reduce", "basesize=512"]` | 378.527 ms (5%) |           | 149.33 KiB (1%) |        2722 |
| `["findfirst", "n=400", "foldl"]`                   | 538.090 ms (5%) |           |                 |             |
| `["findfirst", "n=400", "reduce", "basesize=128"]`  | 279.451 ms (5%) |           |   1.02 MiB (1%) |       18974 |
| `["findfirst", "n=400", "reduce", "basesize=256"]`  | 281.459 ms (5%) |           | 526.27 KiB (1%) |        9577 |
| `["findfirst", "n=400", "reduce", "basesize=512"]`  | 283.135 ms (5%) |           | 267.25 KiB (1%) |        4877 |
| `["findfirst", "n=500", "foldl"]`                   |  90.304 ms (5%) |           |                 |             |
| `["findfirst", "n=500", "reduce", "basesize=128"]`  |  47.531 ms (5%) |           | 157.47 KiB (1%) |        2855 |
| `["findfirst", "n=500", "reduce", "basesize=256"]`  |  47.961 ms (5%) |           |  84.61 KiB (1%) |        1537 |
| `["findfirst", "n=500", "reduce", "basesize=512"]`  |  50.533 ms (5%) |           |  48.30 KiB (1%) |         878 |
| `["overhead", "default"]`                           | 162.408 μs (5%) |           | 146.22 KiB (1%) |        2630 |
| `["overhead", "stoppable=false"]`                   | 164.408 μs (5%) |           | 146.27 KiB (1%) |        2632 |
| `["overhead", "stoppable=true"]`                    | 307.215 μs (5%) |           | 146.55 KiB (1%) |        2650 |
| `["parallel_histogram", "assoc", "basesize=16384"]` |   4.883 ms (5%) |           | 732.06 KiB (1%) |         103 |
| `["parallel_histogram", "assoc", "basesize=4096"]`  |   5.573 ms (5%) |           |   2.07 MiB (1%) |         502 |
| `["parallel_histogram", "assoc", "basesize=8192"]`  |   5.214 ms (5%) |           |   1.43 MiB (1%) |         242 |
| `["parallel_histogram", "comm", "basesize=16384"]`  |  15.992 ms (5%) |           |   1.22 MiB (1%) |         286 |
| `["parallel_histogram", "comm", "basesize=4096"]`   |  23.804 ms (5%) |           |   1.05 MiB (1%) |        4848 |
| `["parallel_histogram", "comm", "basesize=8192"]`   |  19.177 ms (5%) |           |   1.24 MiB (1%) |        1245 |
| `["parallel_histogram", "seq"]`                     |   8.565 ms (5%) |           | 364.61 KiB (1%) |          24 |
| `["sum", "random", "foldl"]`                        |  17.036 ms (5%) |           |   64 bytes (1%) |           3 |
| `["sum", "random", "reduce", "basesize=128"]`       |   9.048 ms (5%) |           | 313.38 KiB (1%) |        6068 |
| `["sum", "random", "reduce", "basesize=256"]`       |   8.810 ms (5%) |           | 155.14 KiB (1%) |        3012 |
| `["sum", "random", "reduce", "basesize=512"]`       |   8.787 ms (5%) |           |  76.34 KiB (1%) |        1488 |
| `["sum", "uniform", "foldl"]`                       |  16.865 ms (5%) |           |   64 bytes (1%) |           3 |
| `["sum", "uniform", "reduce", "basesize=128"]`      |   8.857 ms (5%) |           | 313.39 KiB (1%) |        6069 |
| `["sum", "uniform", "reduce", "basesize=256"]`      |   8.382 ms (5%) |           | 155.16 KiB (1%) |        3013 |
| `["sum", "uniform", "reduce", "basesize=512"]`      |   8.471 ms (5%) |           |  76.31 KiB (1%) |        1486 |
| `["sum", "valley", "foldl"]`                        |  16.910 ms (5%) |           |   64 bytes (1%) |           3 |
| `["sum", "valley", "reduce", "basesize=128"]`       |   9.122 ms (5%) |           | 313.31 KiB (1%) |        6064 |
| `["sum", "valley", "reduce", "basesize=256"]`       |   8.580 ms (5%) |           | 155.13 KiB (1%) |        3011 |
| `["sum", "valley", "reduce", "basesize=512"]`       |   8.712 ms (5%) |           |  76.33 KiB (1%) |        1487 |
| `["words", "nthreads=1"]`                           |  35.093 ms (5%) |  6.767 ms |  63.33 MiB (1%) |     2069088 |
| `["words", "nthreads=2"]`                           |  18.910 ms (5%) |           |  63.93 MiB (1%) |     2077207 |
| `["words", "nthreads=4"]`                           |  19.528 ms (5%) |           |  64.90 MiB (1%) |     2085444 |

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
       #1  2095 MHz      50854 s          0 s       2203 s      22207 s          0 s
       #2  2095 MHz      50744 s          0 s       2497 s      22828 s          0 s
       
  Memory: 6.764881134033203 GB (2990.015625 MB free)
  Uptime: 778.0 sec
  Load Avg:  1.7421875  1.5302734375  0.91162109375
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-8.0.1 (ORCJIT, skylake)
```

---
# Baseline result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmark: 6 Aug 2020 - 17:33
* Package commit: 3599fd
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
| `["collect", "assoc", "basesize=1"]`                | 377.044 ms (5%) | 11.886 ms |  87.55 MiB (1%) |     1590788 |
| `["collect", "assoc", "basesize=1024"]`             | 235.937 ms (5%) |           |   1.84 MiB (1%) |        1812 |
| `["collect", "assoc", "basesize=32"]`               | 240.603 ms (5%) |           |   5.64 MiB (1%) |       54014 |
| `["collect", "seq"]`                                | 468.595 ms (5%) |           |   1.50 MiB (1%) |       32784 |
| `["collect", "unordered", "basesize=1"]`            | 486.097 ms (5%) |           |  29.15 MiB (1%) |      402901 |
| `["collect", "unordered", "basesize=1024"]`         | 278.620 ms (5%) |           | 796.39 KiB (1%) |        3725 |
| `["collect", "unordered", "basesize=32"]`           | 262.498 ms (5%) |           |   1.47 MiB (1%) |       16400 |
| `["findfirst", "n=1000", "foldl"]`                  | 722.371 ms (5%) |           |                 |             |
| `["findfirst", "n=1000", "reduce", "basesize=128"]` | 369.738 ms (5%) |           | 564.11 KiB (1%) |       10230 |
| `["findfirst", "n=1000", "reduce", "basesize=256"]` | 366.266 ms (5%) |           | 287.27 KiB (1%) |        5223 |
| `["findfirst", "n=1000", "reduce", "basesize=512"]` | 379.241 ms (5%) |           | 149.38 KiB (1%) |        2725 |
| `["findfirst", "n=400", "foldl"]`                   | 548.391 ms (5%) |           |                 |             |
| `["findfirst", "n=400", "reduce", "basesize=128"]`  | 280.084 ms (5%) |           |   1.02 MiB (1%) |       18969 |
| `["findfirst", "n=400", "reduce", "basesize=256"]`  | 273.607 ms (5%) |           | 526.16 KiB (1%) |        9570 |
| `["findfirst", "n=400", "reduce", "basesize=512"]`  | 278.940 ms (5%) |           | 267.33 KiB (1%) |        4882 |
| `["findfirst", "n=500", "foldl"]`                   |  91.009 ms (5%) |           |                 |             |
| `["findfirst", "n=500", "reduce", "basesize=128"]`  |  47.634 ms (5%) |           | 157.42 KiB (1%) |        2852 |
| `["findfirst", "n=500", "reduce", "basesize=256"]`  |  47.602 ms (5%) |           |  84.58 KiB (1%) |        1535 |
| `["findfirst", "n=500", "reduce", "basesize=512"]`  |  49.688 ms (5%) |           |  48.33 KiB (1%) |         880 |
| `["overhead", "default"]`                           | 185.117 μs (5%) |           | 146.27 KiB (1%) |        2633 |
| `["overhead", "stoppable=false"]`                   | 186.717 μs (5%) |           | 146.27 KiB (1%) |        2632 |
| `["overhead", "stoppable=true"]`                    | 324.230 μs (5%) |           | 146.52 KiB (1%) |        2648 |
| `["parallel_histogram", "assoc", "basesize=16384"]` |   4.352 ms (5%) |           | 732.06 KiB (1%) |         103 |
| `["parallel_histogram", "assoc", "basesize=4096"]`  |   5.415 ms (5%) |           |   1.80 MiB (1%) |         497 |
| `["parallel_histogram", "assoc", "basesize=8192"]`  |   4.888 ms (5%) |           |   1.43 MiB (1%) |         242 |
| `["parallel_histogram", "comm", "basesize=16384"]`  |  15.816 ms (5%) |           |   1.22 MiB (1%) |         158 |
| `["parallel_histogram", "comm", "basesize=4096"]`   |  25.486 ms (5%) |           |   1.06 MiB (1%) |        5841 |
| `["parallel_histogram", "comm", "basesize=8192"]`   |  19.934 ms (5%) |           |   1.25 MiB (1%) |        2344 |
| `["parallel_histogram", "seq"]`                     |   8.775 ms (5%) |           | 364.61 KiB (1%) |          24 |
| `["sum", "random", "foldl"]`                        |  17.216 ms (5%) |           |   64 bytes (1%) |           3 |
| `["sum", "random", "reduce", "basesize=128"]`       |   9.366 ms (5%) |           | 313.38 KiB (1%) |        6068 |
| `["sum", "random", "reduce", "basesize=256"]`       |   9.120 ms (5%) |           | 155.14 KiB (1%) |        3012 |
| `["sum", "random", "reduce", "basesize=512"]`       |   8.925 ms (5%) |           |  76.33 KiB (1%) |        1487 |
| `["sum", "uniform", "foldl"]`                       |  16.623 ms (5%) |           |   64 bytes (1%) |           3 |
| `["sum", "uniform", "reduce", "basesize=128"]`      |   8.930 ms (5%) |           | 313.39 KiB (1%) |        6069 |
| `["sum", "uniform", "reduce", "basesize=256"]`      |   8.709 ms (5%) |           | 155.13 KiB (1%) |        3011 |
| `["sum", "uniform", "reduce", "basesize=512"]`      |   8.440 ms (5%) |           |  76.31 KiB (1%) |        1486 |
| `["sum", "valley", "foldl"]`                        |  17.626 ms (5%) |           |   64 bytes (1%) |           3 |
| `["sum", "valley", "reduce", "basesize=128"]`       |   9.401 ms (5%) |           | 313.34 KiB (1%) |        6066 |
| `["sum", "valley", "reduce", "basesize=256"]`       |   9.465 ms (5%) |           | 155.16 KiB (1%) |        3013 |
| `["sum", "valley", "reduce", "basesize=512"]`       |   8.740 ms (5%) |           |  76.33 KiB (1%) |        1487 |
| `["words", "nthreads=1"]`                           |  36.658 ms (5%) |  6.661 ms |  63.23 MiB (1%) |     2065864 |
| `["words", "nthreads=2"]`                           |  18.658 ms (5%) |           |  63.83 MiB (1%) |     2073975 |
| `["words", "nthreads=4"]`                           |  19.850 ms (5%) |           |  64.80 MiB (1%) |     2082249 |

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
       #1  2095 MHz      70833 s          0 s       2730 s      31673 s          0 s
       #2  2095 MHz      76748 s          0 s       2956 s      26414 s          0 s
       
  Memory: 6.764881134033203 GB (3024.6328125 MB free)
  Uptime: 1080.0 sec
  Load Avg:  1.6337890625  1.56591796875  1.09619140625
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
    CPU MHz:             2095.191
    BogoMIPS:            4190.38
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

