# Multi-thread benchmark result

* Pull request commit: [`d8d240018f170046a9e768cbd3209a15b3ecdee0`](https://github.com/JuliaFolds/Transducers.jl/commit/d8d240018f170046a9e768cbd3209a15b3ecdee0)
* Pull request: <https://github.com/JuliaFolds/Transducers.jl/pull/409> (Switch to Julia 1.5 as the main version in CIs)

# Judge result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmarks:
    - Target: 9 Aug 2020 - 20:42
    - Baseline: 9 Aug 2020 - 20:47
* Package commits:
    - Target: 34d0fb
    - Baseline: b8efee
* Julia commits:
    - Target: 96786e
    - Baseline: 96786e
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
| `["overhead", "stoppable=true"]`                    | 0.95 (5%) :white_check_mark: |    1.00 (1%)  |
| `["parallel_histogram", "comm", "basesize=4096"]`   |                   1.04 (5%)  | 1.01 (1%) :x: |
| `["parallel_histogram", "comm", "basesize=8192"]`   | 0.86 (5%) :white_check_mark: |    1.00 (1%)  |
| `["words", "nthreads=2"]`                           | 0.94 (5%) :white_check_mark: |    1.00 (1%)  |
| `["words", "nthreads=4"]`                           | 0.94 (5%) :white_check_mark: |    1.00 (1%)  |

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
Julia Version 1.5.0
Commit 96786e22cc (2020-08-01 23:44 UTC)
Platform Info:
  OS: Linux (x86_64-pc-linux-gnu)
      Ubuntu 18.04.4 LTS
  uname: Linux 5.3.0-1034-azure #35~18.04.1-Ubuntu SMP Mon Jul 13 12:54:45 UTC 2020 x86_64 x86_64
  CPU: Intel(R) Xeon(R) Platinum 8272CL CPU @ 2.60GHz: 
              speed         user         nice          sys         idle          irq
       #1  2593 MHz      47024 s          0 s       2302 s      39095 s          0 s
       #2  2593 MHz      48210 s          0 s       2432 s      38720 s          0 s
       
  Memory: 6.7913818359375 GB (3169.65625 MB free)
  Uptime: 908.0 sec
  Load Avg:  2.02880859375  1.55517578125  0.91162109375
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-9.0.1 (ORCJIT, skylake)
```

### Baseline
```
Julia Version 1.5.0
Commit 96786e22cc (2020-08-01 23:44 UTC)
Platform Info:
  OS: Linux (x86_64-pc-linux-gnu)
      Ubuntu 18.04.4 LTS
  uname: Linux 5.3.0-1034-azure #35~18.04.1-Ubuntu SMP Mon Jul 13 12:54:45 UTC 2020 x86_64 x86_64
  CPU: Intel(R) Xeon(R) Platinum 8272CL CPU @ 2.60GHz: 
              speed         user         nice          sys         idle          irq
       #1  2593 MHz      67387 s          0 s       2863 s      45358 s          0 s
       #2  2593 MHz      70420 s          0 s       2992 s      43046 s          0 s
       
  Memory: 6.7913818359375 GB (3245.234375 MB free)
  Uptime: 1180.0 sec
  Load Avg:  1.74365234375  1.59521484375  1.08837890625
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-9.0.1 (ORCJIT, skylake)
```

---
# Target result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmark: 9 Aug 2020 - 20:42
* Package commit: 34d0fb
* Julia commit: 96786e
* Julia command flags: None
* Environment variables: `JULIA_NUM_THREADS => 2`

## Results
Below is a table of this job's results, obtained by running the benchmarks.
The values listed in the `ID` column have the structure `[parent_group, child_group, ..., key]`, and can be used to
index into the BaseBenchmarks suite to retrieve the corresponding benchmarks.
The percentages accompanying time and memory values in the below table are noise tolerances. The "true"
time/memory value for a given benchmark is expected to fall within this percentage of the reported value.
An empty cell means that the value was zero.

| ID                                                  | time            | GC time  | memory           | allocations |
|-----------------------------------------------------|----------------:|---------:|-----------------:|------------:|
| `["collect", "assoc", "basesize=1"]`                | 302.082 ms (5%) | 9.289 ms |   82.16 MiB (1%) |     1368051 |
| `["collect", "assoc", "basesize=1024"]`             | 198.380 ms (5%) |          |    1.83 MiB (1%) |        1596 |
| `["collect", "assoc", "basesize=32"]`               | 202.190 ms (5%) |          |    5.47 MiB (1%) |       47069 |
| `["collect", "seq"]`                                | 394.960 ms (5%) |          |  512.72 KiB (1%) |          15 |
| `["collect", "unordered", "basesize=1"]`            | 405.596 ms (5%) |          |   30.01 MiB (1%) |      360568 |
| `["collect", "unordered", "basesize=1024"]`         | 231.957 ms (5%) |          |  780.86 KiB (1%) |        1709 |
| `["collect", "unordered", "basesize=32"]`           | 220.186 ms (5%) |          |    1.46 MiB (1%) |       12317 |
| `["findfirst", "n=1000", "foldl"]`                  | 625.577 ms (5%) |          |                  |             |
| `["findfirst", "n=1000", "reduce", "basesize=128"]` | 317.238 ms (5%) |          |  546.34 KiB (1%) |        9562 |
| `["findfirst", "n=1000", "reduce", "basesize=256"]` | 316.208 ms (5%) |          |  278.25 KiB (1%) |        4888 |
| `["findfirst", "n=1000", "reduce", "basesize=512"]` | 321.257 ms (5%) |          |  144.64 KiB (1%) |        2549 |
| `["findfirst", "n=400", "foldl"]`                   | 469.152 ms (5%) |          |                  |             |
| `["findfirst", "n=400", "reduce", "basesize=128"]`  | 239.199 ms (5%) |          | 1012.88 KiB (1%) |       17726 |
| `["findfirst", "n=400", "reduce", "basesize=256"]`  | 237.918 ms (5%) |          |  509.63 KiB (1%) |        8952 |
| `["findfirst", "n=400", "reduce", "basesize=512"]`  | 239.344 ms (5%) |          |  258.84 KiB (1%) |        4564 |
| `["findfirst", "n=500", "foldl"]`                   |  81.440 ms (5%) |          |                  |             |
| `["findfirst", "n=500", "reduce", "basesize=128"]`  |  41.804 ms (5%) |          |  152.59 KiB (1%) |        2677 |
| `["findfirst", "n=500", "reduce", "basesize=256"]`  |  41.534 ms (5%) |          |   82.00 KiB (1%) |        1444 |
| `["findfirst", "n=500", "reduce", "basesize=512"]`  |  44.275 ms (5%) |          |   46.84 KiB (1%) |         828 |
| `["overhead", "default"]`                           | 145.801 μs (5%) |          |  140.75 KiB (1%) |        2465 |
| `["overhead", "stoppable=false"]`                   | 148.100 μs (5%) |          |  140.78 KiB (1%) |        2465 |
| `["overhead", "stoppable=true"]`                    | 273.401 μs (5%) |          |  140.84 KiB (1%) |        2467 |
| `["parallel_histogram", "assoc", "basesize=16384"]` |   4.440 ms (5%) |          |  731.81 KiB (1%) |          94 |
| `["parallel_histogram", "assoc", "basesize=4096"]`  |   5.064 ms (5%) |          |    1.80 MiB (1%) |         448 |
| `["parallel_histogram", "assoc", "basesize=8192"]`  |   4.760 ms (5%) |          |    1.43 MiB (1%) |         220 |
| `["parallel_histogram", "comm", "basesize=16384"]`  |  12.898 ms (5%) |          |    1.22 MiB (1%) |         208 |
| `["parallel_histogram", "comm", "basesize=4096"]`   |  22.282 ms (5%) |          |    1.04 MiB (1%) |        1458 |
| `["parallel_histogram", "comm", "basesize=8192"]`   |  16.067 ms (5%) |          |    1.24 MiB (1%) |         929 |
| `["parallel_histogram", "seq"]`                     |   8.146 ms (5%) |          |  364.61 KiB (1%) |          24 |
| `["sum", "random", "foldl"]`                        |  15.794 ms (5%) |          |    32 bytes (1%) |           2 |
| `["sum", "random", "reduce", "basesize=128"]`       |   8.266 ms (5%) |          |  292.02 KiB (1%) |        5213 |
| `["sum", "random", "reduce", "basesize=256"]`       |   8.094 ms (5%) |          |  144.53 KiB (1%) |        2589 |
| `["sum", "random", "reduce", "basesize=512"]`       |   8.027 ms (5%) |          |   71.11 KiB (1%) |        1279 |
| `["sum", "uniform", "foldl"]`                       |  15.407 ms (5%) |          |    32 bytes (1%) |           2 |
| `["sum", "uniform", "reduce", "basesize=128"]`      |   8.102 ms (5%) |          |  292.02 KiB (1%) |        5213 |
| `["sum", "uniform", "reduce", "basesize=256"]`      |   7.957 ms (5%) |          |  144.53 KiB (1%) |        2589 |
| `["sum", "uniform", "reduce", "basesize=512"]`      |   7.847 ms (5%) |          |   71.06 KiB (1%) |        1278 |
| `["sum", "valley", "foldl"]`                        |  16.008 ms (5%) |          |    32 bytes (1%) |           2 |
| `["sum", "valley", "reduce", "basesize=128"]`       |   8.326 ms (5%) |          |  292.02 KiB (1%) |        5213 |
| `["sum", "valley", "reduce", "basesize=256"]`       |   8.212 ms (5%) |          |  144.53 KiB (1%) |        2589 |
| `["sum", "valley", "reduce", "basesize=512"]`       |   8.088 ms (5%) |          |   71.06 KiB (1%) |        1278 |
| `["words", "nthreads=1"]`                           |  22.578 ms (5%) |          |   31.72 MiB (1%) |     1033315 |
| `["words", "nthreads=2"]`                           |  13.696 ms (5%) |          |   32.44 MiB (1%) |     1033453 |
| `["words", "nthreads=4"]`                           |  13.740 ms (5%) |          |   32.89 MiB (1%) |     1033604 |

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
Julia Version 1.5.0
Commit 96786e22cc (2020-08-01 23:44 UTC)
Platform Info:
  OS: Linux (x86_64-pc-linux-gnu)
      Ubuntu 18.04.4 LTS
  uname: Linux 5.3.0-1034-azure #35~18.04.1-Ubuntu SMP Mon Jul 13 12:54:45 UTC 2020 x86_64 x86_64
  CPU: Intel(R) Xeon(R) Platinum 8272CL CPU @ 2.60GHz: 
              speed         user         nice          sys         idle          irq
       #1  2593 MHz      47024 s          0 s       2302 s      39095 s          0 s
       #2  2593 MHz      48210 s          0 s       2432 s      38720 s          0 s
       
  Memory: 6.7913818359375 GB (3169.65625 MB free)
  Uptime: 908.0 sec
  Load Avg:  2.02880859375  1.55517578125  0.91162109375
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-9.0.1 (ORCJIT, skylake)
```

---
# Baseline result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmark: 9 Aug 2020 - 20:47
* Package commit: b8efee
* Julia commit: 96786e
* Julia command flags: None
* Environment variables: `JULIA_NUM_THREADS => 2`

## Results
Below is a table of this job's results, obtained by running the benchmarks.
The values listed in the `ID` column have the structure `[parent_group, child_group, ..., key]`, and can be used to
index into the BaseBenchmarks suite to retrieve the corresponding benchmarks.
The percentages accompanying time and memory values in the below table are noise tolerances. The "true"
time/memory value for a given benchmark is expected to fall within this percentage of the reported value.
An empty cell means that the value was zero.

| ID                                                  | time            | GC time  | memory           | allocations |
|-----------------------------------------------------|----------------:|---------:|-----------------:|------------:|
| `["collect", "assoc", "basesize=1"]`                | 301.650 ms (5%) | 8.482 ms |   82.15 MiB (1%) |     1368048 |
| `["collect", "assoc", "basesize=1024"]`             | 198.736 ms (5%) |          |    1.83 MiB (1%) |        1597 |
| `["collect", "assoc", "basesize=32"]`               | 202.571 ms (5%) |          |    5.47 MiB (1%) |       47069 |
| `["collect", "seq"]`                                | 394.958 ms (5%) |          |  512.72 KiB (1%) |          15 |
| `["collect", "unordered", "basesize=1"]`            | 406.225 ms (5%) |          |   30.01 MiB (1%) |      360557 |
| `["collect", "unordered", "basesize=1024"]`         | 214.961 ms (5%) |          |  753.11 KiB (1%) |         821 |
| `["collect", "unordered", "basesize=32"]`           | 219.817 ms (5%) |          |    1.46 MiB (1%) |       12323 |
| `["findfirst", "n=1000", "foldl"]`                  | 624.560 ms (5%) |          |                  |             |
| `["findfirst", "n=1000", "reduce", "basesize=128"]` | 317.254 ms (5%) |          |  546.33 KiB (1%) |        9561 |
| `["findfirst", "n=1000", "reduce", "basesize=256"]` | 316.007 ms (5%) |          |  278.25 KiB (1%) |        4888 |
| `["findfirst", "n=1000", "reduce", "basesize=512"]` | 321.191 ms (5%) |          |  144.66 KiB (1%) |        2550 |
| `["findfirst", "n=400", "foldl"]`                   | 468.877 ms (5%) |          |                  |             |
| `["findfirst", "n=400", "reduce", "basesize=128"]`  | 239.490 ms (5%) |          | 1012.91 KiB (1%) |       17727 |
| `["findfirst", "n=400", "reduce", "basesize=256"]`  | 237.822 ms (5%) |          |  509.66 KiB (1%) |        8953 |
| `["findfirst", "n=400", "reduce", "basesize=512"]`  | 239.083 ms (5%) |          |  258.83 KiB (1%) |        4563 |
| `["findfirst", "n=500", "foldl"]`                   |  81.291 ms (5%) |          |                  |             |
| `["findfirst", "n=500", "reduce", "basesize=128"]`  |  41.791 ms (5%) |          |  152.59 KiB (1%) |        2677 |
| `["findfirst", "n=500", "reduce", "basesize=256"]`  |  41.620 ms (5%) |          |   82.00 KiB (1%) |        1444 |
| `["findfirst", "n=500", "reduce", "basesize=512"]`  |  44.228 ms (5%) |          |   46.80 KiB (1%) |         826 |
| `["overhead", "default"]`                           | 145.200 μs (5%) |          |  140.75 KiB (1%) |        2465 |
| `["overhead", "stoppable=false"]`                   | 147.100 μs (5%) |          |  140.78 KiB (1%) |        2465 |
| `["overhead", "stoppable=true"]`                    | 288.500 μs (5%) |          |  140.84 KiB (1%) |        2467 |
| `["parallel_histogram", "assoc", "basesize=16384"]` |   4.450 ms (5%) |          |  731.81 KiB (1%) |          94 |
| `["parallel_histogram", "assoc", "basesize=4096"]`  |   5.065 ms (5%) |          |    1.80 MiB (1%) |         448 |
| `["parallel_histogram", "assoc", "basesize=8192"]`  |   4.759 ms (5%) |          |    1.43 MiB (1%) |         220 |
| `["parallel_histogram", "comm", "basesize=16384"]`  |  13.330 ms (5%) |          |    1.22 MiB (1%) |         201 |
| `["parallel_histogram", "comm", "basesize=4096"]`   |  21.458 ms (5%) |          |    1.03 MiB (1%) |        1575 |
| `["parallel_histogram", "comm", "basesize=8192"]`   |  18.598 ms (5%) |          |    1.24 MiB (1%) |         736 |
| `["parallel_histogram", "seq"]`                     |   8.171 ms (5%) |          |  364.61 KiB (1%) |          24 |
| `["sum", "random", "foldl"]`                        |  15.937 ms (5%) |          |    32 bytes (1%) |           2 |
| `["sum", "random", "reduce", "basesize=128"]`       |   8.327 ms (5%) |          |  292.02 KiB (1%) |        5213 |
| `["sum", "random", "reduce", "basesize=256"]`       |   8.213 ms (5%) |          |  144.53 KiB (1%) |        2589 |
| `["sum", "random", "reduce", "basesize=512"]`       |   8.079 ms (5%) |          |   71.11 KiB (1%) |        1279 |
| `["sum", "uniform", "foldl"]`                       |  15.414 ms (5%) |          |    32 bytes (1%) |           2 |
| `["sum", "uniform", "reduce", "basesize=128"]`      |   8.081 ms (5%) |          |  292.02 KiB (1%) |        5213 |
| `["sum", "uniform", "reduce", "basesize=256"]`      |   7.937 ms (5%) |          |  144.53 KiB (1%) |        2589 |
| `["sum", "uniform", "reduce", "basesize=512"]`      |   7.853 ms (5%) |          |   71.06 KiB (1%) |        1278 |
| `["sum", "valley", "foldl"]`                        |  16.061 ms (5%) |          |    32 bytes (1%) |           2 |
| `["sum", "valley", "reduce", "basesize=128"]`       |   8.329 ms (5%) |          |  292.02 KiB (1%) |        5213 |
| `["sum", "valley", "reduce", "basesize=256"]`       |   8.216 ms (5%) |          |  144.53 KiB (1%) |        2589 |
| `["sum", "valley", "reduce", "basesize=512"]`       |   8.102 ms (5%) |          |   71.09 KiB (1%) |        1279 |
| `["words", "nthreads=1"]`                           |  21.585 ms (5%) |          |   31.70 MiB (1%) |     1032861 |
| `["words", "nthreads=2"]`                           |  14.568 ms (5%) |          |   32.41 MiB (1%) |     1033008 |
| `["words", "nthreads=4"]`                           |  14.580 ms (5%) |          |   32.87 MiB (1%) |     1033163 |

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
Julia Version 1.5.0
Commit 96786e22cc (2020-08-01 23:44 UTC)
Platform Info:
  OS: Linux (x86_64-pc-linux-gnu)
      Ubuntu 18.04.4 LTS
  uname: Linux 5.3.0-1034-azure #35~18.04.1-Ubuntu SMP Mon Jul 13 12:54:45 UTC 2020 x86_64 x86_64
  CPU: Intel(R) Xeon(R) Platinum 8272CL CPU @ 2.60GHz: 
              speed         user         nice          sys         idle          irq
       #1  2593 MHz      67387 s          0 s       2863 s      45358 s          0 s
       #2  2593 MHz      70420 s          0 s       2992 s      43046 s          0 s
       
  Memory: 6.7913818359375 GB (3245.234375 MB free)
  Uptime: 1180.0 sec
  Load Avg:  1.74365234375  1.59521484375  1.08837890625
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-9.0.1 (ORCJIT, skylake)
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
    Model name:          Intel(R) Xeon(R) Platinum 8272CL CPU @ 2.60GHz
    Stepping:            7
    CPU MHz:             2593.905
    BogoMIPS:            5187.81
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
| Brand              | Intel(R) Xeon(R) Platinum 8272CL CPU @ 2.60GHz          |
| Vendor             | :Intel                                                  |
| Architecture       | :Skylake                                                |
| Model              | Family: 0x06, Model: 0x55, Stepping: 0x07, Type: 0x00   |
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

