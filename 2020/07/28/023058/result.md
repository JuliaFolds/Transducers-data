# Multi-thread benchmark result

* Pull request commit: [`b4407500122f4faaf4b76c323d1176091cdc5e2b`](https://github.com/JuliaFolds/Transducers.jl/commit/b4407500122f4faaf4b76c323d1176091cdc5e2b)
* Pull request: <https://github.com/JuliaFolds/Transducers.jl/pull/381> (Run tests with --depwarn=error)

# Judge result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmarks:
    - Target: 28 Jul 2020 - 02:25
    - Baseline: 28 Jul 2020 - 02:30
* Package commits:
    - Target: 6e0ef3
    - Baseline: 9462f4
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
| `["collect", "unordered", "basesize=1024"]`         | 0.87 (5%) :white_check_mark: | 0.93 (1%) :white_check_mark: |
| `["parallel_histogram", "comm", "basesize=4096"]`   | 0.94 (5%) :white_check_mark: | 0.98 (1%) :white_check_mark: |
| `["parallel_histogram", "comm", "basesize=8192"]`   | 0.87 (5%) :white_check_mark: | 0.98 (1%) :white_check_mark: |
| `["words", "nthreads=2"]`                           | 0.91 (5%) :white_check_mark: |                   0.99 (1%)  |
| `["words", "nthreads=4"]`                           | 0.88 (5%) :white_check_mark: | 0.99 (1%) :white_check_mark: |

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
       #1  2095 MHz      55456 s          0 s       2136 s      10016 s          0 s
       #2  2095 MHz      42522 s          0 s       2454 s      22375 s          0 s
       
  Memory: 6.764884948730469 GB (3011.05859375 MB free)
  Uptime: 695.0 sec
  Load Avg:  1.7421875  1.51416015625  0.8935546875
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
       #1  2095 MHz      80957 s          0 s       2632 s      12604 s          0 s
       #2  2095 MHz      61571 s          0 s       2831 s      31622 s          0 s
       
  Memory: 6.764884948730469 GB (2974.18359375 MB free)
  Uptime: 983.0 sec
  Load Avg:  1.66796875  1.5625  1.08349609375
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-8.0.1 (ORCJIT, skylake)
```

---
# Target result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmark: 28 Jul 2020 - 2:25
* Package commit: 6e0ef3
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
| `["collect", "assoc", "basesize=1"]`                | 317.003 ms (5%) | 11.947 ms |  87.55 MiB (1%) |     1590779 |
| `["collect", "assoc", "basesize=1024"]`             | 197.324 ms (5%) |           |   1.84 MiB (1%) |        1812 |
| `["collect", "assoc", "basesize=32"]`               | 203.078 ms (5%) |           |   5.64 MiB (1%) |       54015 |
| `["collect", "seq"]`                                | 376.456 ms (5%) |           |   1.50 MiB (1%) |       32784 |
| `["collect", "unordered", "basesize=1"]`            | 402.007 ms (5%) |           |  29.13 MiB (1%) |      401304 |
| `["collect", "unordered", "basesize=1024"]`         | 256.284 ms (5%) |           | 834.39 KiB (1%) |        6493 |
| `["collect", "unordered", "basesize=32"]`           | 218.577 ms (5%) |           |   1.46 MiB (1%) |       16303 |
| `["findfirst", "n=1000", "foldl"]`                  | 597.625 ms (5%) |           |                 |             |
| `["findfirst", "n=1000", "reduce", "basesize=128"]` | 316.150 ms (5%) |           | 563.42 KiB (1%) |       10190 |
| `["findfirst", "n=1000", "reduce", "basesize=256"]` | 309.524 ms (5%) |           | 286.88 KiB (1%) |        5202 |
| `["findfirst", "n=1000", "reduce", "basesize=512"]` | 321.442 ms (5%) |           | 149.16 KiB (1%) |        2715 |
| `["findfirst", "n=400", "foldl"]`                   | 440.904 ms (5%) |           |                 |             |
| `["findfirst", "n=400", "reduce", "basesize=128"]`  | 237.755 ms (5%) |           |   1.02 MiB (1%) |       18864 |
| `["findfirst", "n=400", "reduce", "basesize=256"]`  | 237.192 ms (5%) |           | 525.39 KiB (1%) |        9525 |
| `["findfirst", "n=400", "reduce", "basesize=512"]`  | 236.204 ms (5%) |           | 266.92 KiB (1%) |        4860 |
| `["findfirst", "n=500", "foldl"]`                   |  73.972 ms (5%) |           |                 |             |
| `["findfirst", "n=500", "reduce", "basesize=128"]`  |  39.724 ms (5%) |           | 157.16 KiB (1%) |        2839 |
| `["findfirst", "n=500", "reduce", "basesize=256"]`  |  38.813 ms (5%) |           |  84.39 KiB (1%) |        1527 |
| `["findfirst", "n=500", "reduce", "basesize=512"]`  |  41.922 ms (5%) |           |  48.17 KiB (1%) |         874 |
| `["overhead", "default"]`                           | 154.402 μs (5%) |           | 146.16 KiB (1%) |        2629 |
| `["overhead", "stoppable=false"]`                   | 155.702 μs (5%) |           | 146.16 KiB (1%) |        2629 |
| `["overhead", "stoppable=true"]`                    | 275.803 μs (5%) |           | 146.42 KiB (1%) |        2646 |
| `["parallel_histogram", "assoc", "basesize=16384"]` |   3.714 ms (5%) |           | 732.02 KiB (1%) |         101 |
| `["parallel_histogram", "assoc", "basesize=4096"]`  |   4.304 ms (5%) |           |   1.80 MiB (1%) |         495 |
| `["parallel_histogram", "assoc", "basesize=8192"]`  |   4.017 ms (5%) |           |   1.43 MiB (1%) |         241 |
| `["parallel_histogram", "comm", "basesize=16384"]`  |  13.401 ms (5%) |           |   1.22 MiB (1%) |         159 |
| `["parallel_histogram", "comm", "basesize=4096"]`   |  22.866 ms (5%) |           |   1.06 MiB (1%) |        5483 |
| `["parallel_histogram", "comm", "basesize=8192"]`   |  16.789 ms (5%) |           |   1.24 MiB (1%) |        1687 |
| `["parallel_histogram", "seq"]`                     |   6.755 ms (5%) |           | 364.61 KiB (1%) |          24 |
| `["sum", "random", "foldl"]`                        |  14.045 ms (5%) |           |   64 bytes (1%) |           3 |
| `["sum", "random", "reduce", "basesize=128"]`       |   7.333 ms (5%) |           | 313.34 KiB (1%) |        6068 |
| `["sum", "random", "reduce", "basesize=256"]`       |   6.990 ms (5%) |           | 155.13 KiB (1%) |        3013 |
| `["sum", "random", "reduce", "basesize=512"]`       |   7.103 ms (5%) |           |  76.27 KiB (1%) |        1485 |
| `["sum", "uniform", "foldl"]`                       |  13.424 ms (5%) |           |   64 bytes (1%) |           3 |
| `["sum", "uniform", "reduce", "basesize=128"]`      |   6.834 ms (5%) |           | 313.34 KiB (1%) |        6068 |
| `["sum", "uniform", "reduce", "basesize=256"]`      |   6.654 ms (5%) |           | 155.08 KiB (1%) |        3010 |
| `["sum", "uniform", "reduce", "basesize=512"]`      |   6.611 ms (5%) |           |  76.25 KiB (1%) |        1484 |
| `["sum", "valley", "foldl"]`                        |  13.761 ms (5%) |           |   64 bytes (1%) |           3 |
| `["sum", "valley", "reduce", "basesize=128"]`       |   7.259 ms (5%) |           | 313.27 KiB (1%) |        6063 |
| `["sum", "valley", "reduce", "basesize=256"]`       |   7.199 ms (5%) |           | 155.09 KiB (1%) |        3011 |
| `["sum", "valley", "reduce", "basesize=512"]`       |   7.255 ms (5%) |           |  76.28 KiB (1%) |        1486 |
| `["words", "nthreads=1"]`                           |  39.694 ms (5%) |  6.845 ms |  63.08 MiB (1%) |     2061033 |
| `["words", "nthreads=2"]`                           |  20.296 ms (5%) |           |  64.17 MiB (1%) |     2073288 |
| `["words", "nthreads=4"]`                           |  20.240 ms (5%) |           |  64.81 MiB (1%) |     2079538 |

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
       #1  2095 MHz      55456 s          0 s       2136 s      10016 s          0 s
       #2  2095 MHz      42522 s          0 s       2454 s      22375 s          0 s
       
  Memory: 6.764884948730469 GB (3011.05859375 MB free)
  Uptime: 695.0 sec
  Load Avg:  1.7421875  1.51416015625  0.8935546875
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-8.0.1 (ORCJIT, skylake)
```

---
# Baseline result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmark: 28 Jul 2020 - 2:30
* Package commit: 9462f4
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
| `["collect", "assoc", "basesize=1"]`                | 307.153 ms (5%) | 8.810 ms |  87.55 MiB (1%) |     1590803 |
| `["collect", "assoc", "basesize=1024"]`             | 194.478 ms (5%) |          |   1.84 MiB (1%) |        1812 |
| `["collect", "assoc", "basesize=32"]`               | 196.415 ms (5%) |          |   5.64 MiB (1%) |       54019 |
| `["collect", "seq"]`                                | 375.379 ms (5%) |          |   1.50 MiB (1%) |       32784 |
| `["collect", "unordered", "basesize=1"]`            | 386.729 ms (5%) |          |  29.13 MiB (1%) |      401430 |
| `["collect", "unordered", "basesize=1024"]`         | 294.814 ms (5%) |          | 900.56 KiB (1%) |       10683 |
| `["collect", "unordered", "basesize=32"]`           | 222.239 ms (5%) |          |   1.45 MiB (1%) |       15621 |
| `["findfirst", "n=1000", "foldl"]`                  | 600.257 ms (5%) |          |                 |             |
| `["findfirst", "n=1000", "reduce", "basesize=128"]` | 314.304 ms (5%) |          | 563.34 KiB (1%) |       10185 |
| `["findfirst", "n=1000", "reduce", "basesize=256"]` | 312.747 ms (5%) |          | 287.00 KiB (1%) |        5210 |
| `["findfirst", "n=1000", "reduce", "basesize=512"]` | 320.546 ms (5%) |          | 149.19 KiB (1%) |        2717 |
| `["findfirst", "n=400", "foldl"]`                   | 448.949 ms (5%) |          |                 |             |
| `["findfirst", "n=400", "reduce", "basesize=128"]`  | 239.431 ms (5%) |          |   1.02 MiB (1%) |       18878 |
| `["findfirst", "n=400", "reduce", "basesize=256"]`  | 232.992 ms (5%) |          | 525.31 KiB (1%) |        9520 |
| `["findfirst", "n=400", "reduce", "basesize=512"]`  | 236.968 ms (5%) |          | 266.83 KiB (1%) |        4854 |
| `["findfirst", "n=500", "foldl"]`                   |  74.038 ms (5%) |          |                 |             |
| `["findfirst", "n=500", "reduce", "basesize=128"]`  |  39.487 ms (5%) |          | 157.14 KiB (1%) |        2838 |
| `["findfirst", "n=500", "reduce", "basesize=256"]`  |  38.685 ms (5%) |          |  84.39 KiB (1%) |        1527 |
| `["findfirst", "n=500", "reduce", "basesize=512"]`  |  41.807 ms (5%) |          |  48.17 KiB (1%) |         874 |
| `["overhead", "default"]`                           | 150.701 μs (5%) |          | 146.16 KiB (1%) |        2629 |
| `["overhead", "stoppable=false"]`                   | 152.501 μs (5%) |          | 146.16 KiB (1%) |        2629 |
| `["overhead", "stoppable=true"]`                    | 280.502 μs (5%) |          | 146.41 KiB (1%) |        2645 |
| `["parallel_histogram", "assoc", "basesize=16384"]` |   3.747 ms (5%) |          | 732.02 KiB (1%) |         101 |
| `["parallel_histogram", "assoc", "basesize=4096"]`  |   4.239 ms (5%) |          |   1.80 MiB (1%) |         495 |
| `["parallel_histogram", "assoc", "basesize=8192"]`  |   3.952 ms (5%) |          |   1.43 MiB (1%) |         241 |
| `["parallel_histogram", "comm", "basesize=16384"]`  |  14.083 ms (5%) |          |   1.22 MiB (1%) |         263 |
| `["parallel_histogram", "comm", "basesize=4096"]`   |  24.405 ms (5%) |          |   1.08 MiB (1%) |        6571 |
| `["parallel_histogram", "comm", "basesize=8192"]`   |  19.397 ms (5%) |          |   1.26 MiB (1%) |        3017 |
| `["parallel_histogram", "seq"]`                     |   6.720 ms (5%) |          | 364.61 KiB (1%) |          24 |
| `["sum", "random", "foldl"]`                        |  14.086 ms (5%) |          |   64 bytes (1%) |           3 |
| `["sum", "random", "reduce", "basesize=128"]`       |   7.226 ms (5%) |          | 313.38 KiB (1%) |        6070 |
| `["sum", "random", "reduce", "basesize=256"]`       |   7.106 ms (5%) |          | 155.09 KiB (1%) |        3011 |
| `["sum", "random", "reduce", "basesize=512"]`       |   6.942 ms (5%) |          |  76.25 KiB (1%) |        1484 |
| `["sum", "uniform", "foldl"]`                       |  13.326 ms (5%) |          |   64 bytes (1%) |           3 |
| `["sum", "uniform", "reduce", "basesize=128"]`      |   7.121 ms (5%) |          | 313.38 KiB (1%) |        6070 |
| `["sum", "uniform", "reduce", "basesize=256"]`      |   6.856 ms (5%) |          | 155.08 KiB (1%) |        3010 |
| `["sum", "uniform", "reduce", "basesize=512"]`      |   6.752 ms (5%) |          |  76.25 KiB (1%) |        1484 |
| `["sum", "valley", "foldl"]`                        |  14.153 ms (5%) |          |   64 bytes (1%) |           3 |
| `["sum", "valley", "reduce", "basesize=128"]`       |   7.522 ms (5%) |          | 313.25 KiB (1%) |        6062 |
| `["sum", "valley", "reduce", "basesize=256"]`       |   7.208 ms (5%) |          | 155.09 KiB (1%) |        3011 |
| `["sum", "valley", "reduce", "basesize=512"]`       |   7.064 ms (5%) |          |  76.27 KiB (1%) |        1485 |
| `["words", "nthreads=1"]`                           |  38.315 ms (5%) | 6.643 ms |  63.65 MiB (1%) |     2080421 |
| `["words", "nthreads=2"]`                           |  22.269 ms (5%) |          |  64.74 MiB (1%) |     2092640 |
| `["words", "nthreads=4"]`                           |  22.890 ms (5%) |          |  65.69 MiB (1%) |     2103125 |

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
       #1  2095 MHz      80957 s          0 s       2632 s      12604 s          0 s
       #2  2095 MHz      61571 s          0 s       2831 s      31622 s          0 s
       
  Memory: 6.764884948730469 GB (2974.18359375 MB free)
  Uptime: 983.0 sec
  Load Avg:  1.66796875  1.5625  1.08349609375
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
    CPU MHz:             2095.079
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

