# Multi-thread benchmark result

* Pull request commit: [`b847eed7c054e9631be02144bc20a530d6ffbd88`](https://github.com/JuliaFolds/Transducers.jl/commit/b847eed7c054e9631be02144bc20a530d6ffbd88)
* Pull request: <https://github.com/JuliaFolds/Transducers.jl/pull/243> (Update */Manifest.toml)

# Judge result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmarks:
    - Target: 5 Jan 2021 - 01:23
    - Baseline: 5 Jan 2021 - 01:28
* Package commits:
    - Target: 93a941
    - Baseline: b299e3
* Julia commits:
    - Target: 788b2c
    - Baseline: 788b2c
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
| `["collect", "assoc", "basesize=1"]`                |                1.05 (5%) :x: |                   1.00 (1%)  |
| `["collect", "unordered", "basesize=1024"]`         |                   1.02 (5%)  | 0.99 (1%) :white_check_mark: |
| `["overhead", "stoppable=false"]`                   | 0.92 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["overhead", "stoppable=true"]`                    | 0.94 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["parallel_histogram", "comm", "basesize=8192"]`   |                1.08 (5%) :x: |                   1.00 (1%)  |
| `["words", "nthreads=1"]`                           |                1.09 (5%) :x: |                   1.01 (1%)  |
| `["words", "nthreads=2"]`                           | 0.90 (5%) :white_check_mark: |                   1.01 (1%)  |
| `["words", "nthreads=4"]`                           | 0.88 (5%) :white_check_mark: |                   1.01 (1%)  |

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
Julia Version 1.5.3
Commit 788b2c77c1 (2020-11-09 13:37 UTC)
Platform Info:
  OS: Linux (x86_64-pc-linux-gnu)
      Ubuntu 18.04.5 LTS
  uname: Linux 5.4.0-1032-azure #33~18.04.1-Ubuntu SMP Tue Nov 17 11:40:52 UTC 2020 x86_64 x86_64
  CPU: Intel(R) Xeon(R) Platinum 8171M CPU @ 2.60GHz: 
              speed         user         nice          sys         idle          irq
       #1  2095 MHz      43827 s          0 s       2343 s      21493 s          0 s
       #2  2095 MHz      53163 s          0 s       2433 s      11983 s          0 s
       
  Memory: 6.7913970947265625 GB (3744.95703125 MB free)
  Uptime: 692.0 sec
  Load Avg:  1.6689453125  1.49365234375  0.873046875
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-9.0.1 (ORCJIT, skylake-avx512)
```

### Baseline
```
Julia Version 1.5.3
Commit 788b2c77c1 (2020-11-09 13:37 UTC)
Platform Info:
  OS: Linux (x86_64-pc-linux-gnu)
      Ubuntu 18.04.5 LTS
  uname: Linux 5.4.0-1032-azure #33~18.04.1-Ubuntu SMP Tue Nov 17 11:40:52 UTC 2020 x86_64 x86_64
  CPU: Intel(R) Xeon(R) Platinum 8171M CPU @ 2.60GHz: 
              speed         user         nice          sys         idle          irq
       #1  2095 MHz      68909 s          0 s       3016 s      25701 s          0 s
       #2  2095 MHz      73548 s          0 s       3091 s      20919 s          0 s
       
  Memory: 6.7913970947265625 GB (3754.1171875 MB free)
  Uptime: 993.0 sec
  Load Avg:  1.67041015625  1.56494140625  1.07666015625
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-9.0.1 (ORCJIT, skylake-avx512)
```

---
# Target result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmark: 5 Jan 2021 - 1:23
* Package commit: 93a941
* Julia commit: 788b2c
* Julia command flags: None
* Environment variables: `JULIA_NUM_THREADS => 2`

## Results
Below is a table of this job's results, obtained by running the benchmarks.
The values listed in the `ID` column have the structure `[parent_group, child_group, ..., key]`, and can be used to
index into the BaseBenchmarks suite to retrieve the corresponding benchmarks.
The percentages accompanying time and memory values in the below table are noise tolerances. The "true"
time/memory value for a given benchmark is expected to fall within this percentage of the reported value.
An empty cell means that the value was zero.

| ID                                                  | time            | GC time   | memory           | allocations |
|-----------------------------------------------------|----------------:|----------:|-----------------:|------------:|
| `["collect", "assoc", "basesize=1"]`                | 348.465 ms (5%) | 12.573 ms |   82.16 MiB (1%) |     1368054 |
| `["collect", "assoc", "basesize=1024"]`             | 218.466 ms (5%) |           |    1.83 MiB (1%) |        1597 |
| `["collect", "assoc", "basesize=32"]`               | 222.445 ms (5%) |           |    5.47 MiB (1%) |       47069 |
| `["collect", "seq"]`                                | 423.145 ms (5%) |           |  512.72 KiB (1%) |          15 |
| `["collect", "unordered", "basesize=1"]`            | 452.739 ms (5%) |           |   30.01 MiB (1%) |      360587 |
| `["collect", "unordered", "basesize=1024"]`         | 257.683 ms (5%) |           |  763.23 KiB (1%) |        1145 |
| `["collect", "unordered", "basesize=32"]`           | 238.441 ms (5%) |           |    1.47 MiB (1%) |       12493 |
| `["findfirst", "n=1000", "foldl"]`                  | 676.872 ms (5%) |           |                  |             |
| `["findfirst", "n=1000", "reduce", "basesize=128"]` | 354.198 ms (5%) |           |  546.34 KiB (1%) |        9562 |
| `["findfirst", "n=1000", "reduce", "basesize=256"]` | 355.693 ms (5%) |           |  278.25 KiB (1%) |        4888 |
| `["findfirst", "n=1000", "reduce", "basesize=512"]` | 363.259 ms (5%) |           |  144.66 KiB (1%) |        2550 |
| `["findfirst", "n=400", "foldl"]`                   | 468.310 ms (5%) |           |                  |             |
| `["findfirst", "n=400", "reduce", "basesize=128"]`  | 256.030 ms (5%) |           | 1012.89 KiB (1%) |       17726 |
| `["findfirst", "n=400", "reduce", "basesize=256"]`  | 256.237 ms (5%) |           |  509.63 KiB (1%) |        8952 |
| `["findfirst", "n=400", "reduce", "basesize=512"]`  | 253.995 ms (5%) |           |  258.80 KiB (1%) |        4562 |
| `["findfirst", "n=500", "foldl"]`                   |  81.754 ms (5%) |           |                  |             |
| `["findfirst", "n=500", "reduce", "basesize=128"]`  |  44.440 ms (5%) |           |  152.59 KiB (1%) |        2677 |
| `["findfirst", "n=500", "reduce", "basesize=256"]`  |  43.219 ms (5%) |           |   82.00 KiB (1%) |        1444 |
| `["findfirst", "n=500", "reduce", "basesize=512"]`  |  46.173 ms (5%) |           |   46.83 KiB (1%) |         827 |
| `["overhead", "default"]`                           | 138.201 μs (5%) |           |  140.72 KiB (1%) |        2464 |
| `["overhead", "stoppable=false"]`                   | 135.601 μs (5%) |           |  140.75 KiB (1%) |        2464 |
| `["overhead", "stoppable=true"]`                    | 278.803 μs (5%) |           |  140.78 KiB (1%) |        2465 |
| `["parallel_histogram", "assoc", "basesize=16384"]` |   4.499 ms (5%) |           |  731.81 KiB (1%) |          94 |
| `["parallel_histogram", "assoc", "basesize=4096"]`  |   5.010 ms (5%) |           |    1.80 MiB (1%) |         448 |
| `["parallel_histogram", "assoc", "basesize=8192"]`  |   4.913 ms (5%) |           |    1.43 MiB (1%) |         220 |
| `["parallel_histogram", "comm", "basesize=16384"]`  |  14.856 ms (5%) |           |    1.22 MiB (1%) |         235 |
| `["parallel_histogram", "comm", "basesize=4096"]`   |  23.884 ms (5%) |           |    1.05 MiB (1%) |        1933 |
| `["parallel_histogram", "comm", "basesize=8192"]`   |  21.411 ms (5%) |           |    1.25 MiB (1%) |        1112 |
| `["parallel_histogram", "seq"]`                     |   7.848 ms (5%) |           |  364.61 KiB (1%) |          24 |
| `["sum", "random", "foldl"]`                        |  15.170 ms (5%) |           |    32 bytes (1%) |           2 |
| `["sum", "random", "reduce", "basesize=128"]`       |   8.386 ms (5%) |           |  292.02 KiB (1%) |        5213 |
| `["sum", "random", "reduce", "basesize=256"]`       |   8.190 ms (5%) |           |  144.53 KiB (1%) |        2589 |
| `["sum", "random", "reduce", "basesize=512"]`       |   8.020 ms (5%) |           |   71.11 KiB (1%) |        1279 |
| `["sum", "uniform", "foldl"]`                       |  14.405 ms (5%) |           |    32 bytes (1%) |           2 |
| `["sum", "uniform", "reduce", "basesize=128"]`      |   8.119 ms (5%) |           |  292.02 KiB (1%) |        5213 |
| `["sum", "uniform", "reduce", "basesize=256"]`      |   7.914 ms (5%) |           |  144.53 KiB (1%) |        2589 |
| `["sum", "uniform", "reduce", "basesize=512"]`      |   7.884 ms (5%) |           |   71.06 KiB (1%) |        1278 |
| `["sum", "valley", "foldl"]`                        |  15.100 ms (5%) |           |    32 bytes (1%) |           2 |
| `["sum", "valley", "reduce", "basesize=128"]`       |   8.495 ms (5%) |           |  292.02 KiB (1%) |        5213 |
| `["sum", "valley", "reduce", "basesize=256"]`       |   8.338 ms (5%) |           |  144.53 KiB (1%) |        2589 |
| `["sum", "valley", "reduce", "basesize=512"]`       |   8.294 ms (5%) |           |   71.06 KiB (1%) |        1278 |
| `["words", "nthreads=1"]`                           |  23.342 ms (5%) |           |   31.80 MiB (1%) |     1035958 |
| `["words", "nthreads=2"]`                           |  14.141 ms (5%) |           |   32.16 MiB (1%) |     1036031 |
| `["words", "nthreads=4"]`                           |  14.513 ms (5%) |           |   32.88 MiB (1%) |     1036199 |

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
Julia Version 1.5.3
Commit 788b2c77c1 (2020-11-09 13:37 UTC)
Platform Info:
  OS: Linux (x86_64-pc-linux-gnu)
      Ubuntu 18.04.5 LTS
  uname: Linux 5.4.0-1032-azure #33~18.04.1-Ubuntu SMP Tue Nov 17 11:40:52 UTC 2020 x86_64 x86_64
  CPU: Intel(R) Xeon(R) Platinum 8171M CPU @ 2.60GHz: 
              speed         user         nice          sys         idle          irq
       #1  2095 MHz      43827 s          0 s       2343 s      21493 s          0 s
       #2  2095 MHz      53163 s          0 s       2433 s      11983 s          0 s
       
  Memory: 6.7913970947265625 GB (3744.95703125 MB free)
  Uptime: 692.0 sec
  Load Avg:  1.6689453125  1.49365234375  0.873046875
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-9.0.1 (ORCJIT, skylake-avx512)
```

---
# Baseline result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmark: 5 Jan 2021 - 1:28
* Package commit: b299e3
* Julia commit: 788b2c
* Julia command flags: None
* Environment variables: `JULIA_NUM_THREADS => 2`

## Results
Below is a table of this job's results, obtained by running the benchmarks.
The values listed in the `ID` column have the structure `[parent_group, child_group, ..., key]`, and can be used to
index into the BaseBenchmarks suite to retrieve the corresponding benchmarks.
The percentages accompanying time and memory values in the below table are noise tolerances. The "true"
time/memory value for a given benchmark is expected to fall within this percentage of the reported value.
An empty cell means that the value was zero.

| ID                                                  | time            | GC time   | memory           | allocations |
|-----------------------------------------------------|----------------:|----------:|-----------------:|------------:|
| `["collect", "assoc", "basesize=1"]`                | 331.485 ms (5%) | 10.510 ms |   82.16 MiB (1%) |     1368052 |
| `["collect", "assoc", "basesize=1024"]`             | 219.610 ms (5%) |           |    1.83 MiB (1%) |        1597 |
| `["collect", "assoc", "basesize=32"]`               | 220.013 ms (5%) |           |    5.47 MiB (1%) |       47068 |
| `["collect", "seq"]`                                | 417.999 ms (5%) |           |  512.72 KiB (1%) |          15 |
| `["collect", "unordered", "basesize=1"]`            | 467.538 ms (5%) |           |   30.01 MiB (1%) |      360600 |
| `["collect", "unordered", "basesize=1024"]`         | 252.244 ms (5%) |           |  774.55 KiB (1%) |        1507 |
| `["collect", "unordered", "basesize=32"]`           | 243.434 ms (5%) |           |    1.47 MiB (1%) |       12412 |
| `["findfirst", "n=1000", "foldl"]`                  | 685.336 ms (5%) |           |                  |             |
| `["findfirst", "n=1000", "reduce", "basesize=128"]` | 354.200 ms (5%) |           |  546.34 KiB (1%) |        9562 |
| `["findfirst", "n=1000", "reduce", "basesize=256"]` | 348.894 ms (5%) |           |  278.25 KiB (1%) |        4888 |
| `["findfirst", "n=1000", "reduce", "basesize=512"]` | 356.098 ms (5%) |           |  144.64 KiB (1%) |        2549 |
| `["findfirst", "n=400", "foldl"]`                   | 490.290 ms (5%) |           |                  |             |
| `["findfirst", "n=400", "reduce", "basesize=128"]`  | 261.613 ms (5%) |           | 1012.91 KiB (1%) |       17727 |
| `["findfirst", "n=400", "reduce", "basesize=256"]`  | 264.619 ms (5%) |           |  509.63 KiB (1%) |        8952 |
| `["findfirst", "n=400", "reduce", "basesize=512"]`  | 261.891 ms (5%) |           |  258.83 KiB (1%) |        4563 |
| `["findfirst", "n=500", "foldl"]`                   |  81.966 ms (5%) |           |                  |             |
| `["findfirst", "n=500", "reduce", "basesize=128"]`  |  44.002 ms (5%) |           |  152.59 KiB (1%) |        2677 |
| `["findfirst", "n=500", "reduce", "basesize=256"]`  |  44.603 ms (5%) |           |   82.00 KiB (1%) |        1444 |
| `["findfirst", "n=500", "reduce", "basesize=512"]`  |  47.086 ms (5%) |           |   46.84 KiB (1%) |         828 |
| `["overhead", "default"]`                           | 141.803 μs (5%) |           |  140.72 KiB (1%) |        2464 |
| `["overhead", "stoppable=false"]`                   | 147.303 μs (5%) |           |  140.75 KiB (1%) |        2464 |
| `["overhead", "stoppable=true"]`                    | 296.406 μs (5%) |           |  140.78 KiB (1%) |        2465 |
| `["parallel_histogram", "assoc", "basesize=16384"]` |   4.520 ms (5%) |           |  731.81 KiB (1%) |          94 |
| `["parallel_histogram", "assoc", "basesize=4096"]`  |   5.183 ms (5%) |           |    1.80 MiB (1%) |         448 |
| `["parallel_histogram", "assoc", "basesize=8192"]`  |   4.838 ms (5%) |           |    1.43 MiB (1%) |         220 |
| `["parallel_histogram", "comm", "basesize=16384"]`  |  14.942 ms (5%) |           |    1.22 MiB (1%) |         210 |
| `["parallel_histogram", "comm", "basesize=4096"]`   |  24.672 ms (5%) |           |    1.04 MiB (1%) |        1378 |
| `["parallel_histogram", "comm", "basesize=8192"]`   |  19.856 ms (5%) |           |    1.25 MiB (1%) |        1241 |
| `["parallel_histogram", "seq"]`                     |   7.657 ms (5%) |           |  364.61 KiB (1%) |          24 |
| `["sum", "random", "foldl"]`                        |  15.126 ms (5%) |           |    32 bytes (1%) |           2 |
| `["sum", "random", "reduce", "basesize=128"]`       |   8.631 ms (5%) |           |  292.02 KiB (1%) |        5213 |
| `["sum", "random", "reduce", "basesize=256"]`       |   8.393 ms (5%) |           |  144.53 KiB (1%) |        2589 |
| `["sum", "random", "reduce", "basesize=512"]`       |   8.158 ms (5%) |           |   71.11 KiB (1%) |        1279 |
| `["sum", "uniform", "foldl"]`                       |  14.899 ms (5%) |           |    32 bytes (1%) |           2 |
| `["sum", "uniform", "reduce", "basesize=128"]`      |   8.093 ms (5%) |           |  292.02 KiB (1%) |        5213 |
| `["sum", "uniform", "reduce", "basesize=256"]`      |   7.934 ms (5%) |           |  144.53 KiB (1%) |        2589 |
| `["sum", "uniform", "reduce", "basesize=512"]`      |   8.001 ms (5%) |           |   71.06 KiB (1%) |        1278 |
| `["sum", "valley", "foldl"]`                        |  15.734 ms (5%) |           |    32 bytes (1%) |           2 |
| `["sum", "valley", "reduce", "basesize=128"]`       |   8.522 ms (5%) |           |  292.02 KiB (1%) |        5213 |
| `["sum", "valley", "reduce", "basesize=256"]`       |   8.526 ms (5%) |           |  144.53 KiB (1%) |        2589 |
| `["sum", "valley", "reduce", "basesize=512"]`       |   8.319 ms (5%) |           |   71.09 KiB (1%) |        1279 |
| `["words", "nthreads=1"]`                           |  21.463 ms (5%) |           |   31.62 MiB (1%) |     1030154 |
| `["words", "nthreads=2"]`                           |  15.758 ms (5%) |           |   31.98 MiB (1%) |     1030223 |
| `["words", "nthreads=4"]`                           |  16.456 ms (5%) |           |   32.69 MiB (1%) |     1030361 |

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
Julia Version 1.5.3
Commit 788b2c77c1 (2020-11-09 13:37 UTC)
Platform Info:
  OS: Linux (x86_64-pc-linux-gnu)
      Ubuntu 18.04.5 LTS
  uname: Linux 5.4.0-1032-azure #33~18.04.1-Ubuntu SMP Tue Nov 17 11:40:52 UTC 2020 x86_64 x86_64
  CPU: Intel(R) Xeon(R) Platinum 8171M CPU @ 2.60GHz: 
              speed         user         nice          sys         idle          irq
       #1  2095 MHz      68909 s          0 s       3016 s      25701 s          0 s
       #2  2095 MHz      73548 s          0 s       3091 s      20919 s          0 s
       
  Memory: 6.7913970947265625 GB (3754.1171875 MB free)
  Uptime: 993.0 sec
  Load Avg:  1.67041015625  1.56494140625  1.07666015625
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-9.0.1 (ORCJIT, skylake-avx512)
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
| Address Size       | 48 bits virtual, 46 bits physical                       |
| SIMD               | 512 bit = 64 byte max. SIMD vector size                 |
| Time Stamp Counter | TSC is accessible via `rdtsc`                           |
|                    | TSC increased at every clock cycle (non-invariant TSC)  |
| Perf. Monitoring   | Performance Monitoring Counters (PMC) are not supported |
| Hypervisor         | Yes, Microsoft                                          |

