# Multi-thread benchmark result

* Pull request commit: [`eae57fd773285c7dc4594baa154c8c1a58ab3bf0`](https://github.com/JuliaFolds/Transducers.jl/commit/eae57fd773285c7dc4594baa154c8c1a58ab3bf0)
* Pull request: <https://github.com/JuliaFolds/Transducers.jl/pull/243> (Update */Manifest.toml)

# Judge result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmarks:
    - Target: 24 Oct 2020 - 01:17
    - Baseline: 24 Oct 2020 - 01:22
* Package commits:
    - Target: e314ef
    - Baseline: da98f2
* Julia commits:
    - Target: 539f3c
    - Baseline: 539f3c
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

| ID                                                  | time ratio    | memory ratio  |
|-----------------------------------------------------|---------------|---------------|
| `["collect", "unordered", "basesize=1024"]`         |    0.98 (5%)  | 1.04 (1%) :x: |
| `["words", "nthreads=4"]`                           | 1.05 (5%) :x: |    1.01 (1%)  |

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
Julia Version 1.5.2
Commit 539f3ce943 (2020-09-23 23:17 UTC)
Platform Info:
  OS: Linux (x86_64-pc-linux-gnu)
      Ubuntu 18.04.5 LTS
  uname: Linux 5.4.0-1031-azure #32~18.04.1-Ubuntu SMP Tue Oct 6 10:03:22 UTC 2020 x86_64 x86_64
  CPU: Intel(R) Xeon(R) Platinum 8171M CPU @ 2.60GHz: 
              speed         user         nice          sys         idle          irq
       #1  2095 MHz      47388 s          0 s       2188 s      42191 s          0 s
       #2  2095 MHz      52031 s          0 s       2343 s      37773 s          0 s
       
  Memory: 6.764892578125 GB (3422.58984375 MB free)
  Uptime: 940.0 sec
  Load Avg:  1.70947265625  1.4970703125  0.87939453125
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-9.0.1 (ORCJIT, skylake-avx512)
```

### Baseline
```
Julia Version 1.5.2
Commit 539f3ce943 (2020-09-23 23:17 UTC)
Platform Info:
  OS: Linux (x86_64-pc-linux-gnu)
      Ubuntu 18.04.5 LTS
  uname: Linux 5.4.0-1031-azure #32~18.04.1-Ubuntu SMP Tue Oct 6 10:03:22 UTC 2020 x86_64 x86_64
  CPU: Intel(R) Xeon(R) Platinum 8171M CPU @ 2.60GHz: 
              speed         user         nice          sys         idle          irq
       #1  2095 MHz      68342 s          0 s       2747 s      52554 s          0 s
       #2  2095 MHz      78860 s          0 s       2966 s      42416 s          0 s
       
  Memory: 6.764892578125 GB (3431.90625 MB free)
  Uptime: 1263.0 sec
  Load Avg:  1.5703125  1.50830078125  1.0654296875
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-9.0.1 (ORCJIT, skylake-avx512)
```

---
# Target result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmark: 24 Oct 2020 - 1:17
* Package commit: e314ef
* Julia commit: 539f3c
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
| `["collect", "assoc", "basesize=1"]`                | 374.774 ms (5%) | 12.106 ms |   82.16 MiB (1%) |     1368051 |
| `["collect", "assoc", "basesize=1024"]`             | 250.295 ms (5%) |           |    1.83 MiB (1%) |        1597 |
| `["collect", "assoc", "basesize=32"]`               | 254.795 ms (5%) |           |    5.47 MiB (1%) |       47069 |
| `["collect", "seq"]`                                | 497.016 ms (5%) |           |  512.72 KiB (1%) |          15 |
| `["collect", "unordered", "basesize=1"]`            | 505.653 ms (5%) |           |   30.01 MiB (1%) |      360642 |
| `["collect", "unordered", "basesize=1024"]`         | 313.183 ms (5%) |           |  820.61 KiB (1%) |        2999 |
| `["collect", "unordered", "basesize=32"]`           | 274.050 ms (5%) |           |    1.46 MiB (1%) |       12329 |
| `["findfirst", "n=1000", "foldl"]`                  | 790.576 ms (5%) |           |                  |             |
| `["findfirst", "n=1000", "reduce", "basesize=128"]` | 400.158 ms (5%) |           |  546.33 KiB (1%) |        9561 |
| `["findfirst", "n=1000", "reduce", "basesize=256"]` | 401.319 ms (5%) |           |  278.25 KiB (1%) |        4888 |
| `["findfirst", "n=1000", "reduce", "basesize=512"]` | 406.414 ms (5%) |           |  144.66 KiB (1%) |        2550 |
| `["findfirst", "n=400", "foldl"]`                   | 590.951 ms (5%) |           |                  |             |
| `["findfirst", "n=400", "reduce", "basesize=128"]`  | 301.341 ms (5%) |           | 1012.83 KiB (1%) |       17724 |
| `["findfirst", "n=400", "reduce", "basesize=256"]`  | 299.882 ms (5%) |           |  509.63 KiB (1%) |        8952 |
| `["findfirst", "n=400", "reduce", "basesize=512"]`  | 300.410 ms (5%) |           |  258.83 KiB (1%) |        4563 |
| `["findfirst", "n=500", "foldl"]`                   | 102.303 ms (5%) |           |                  |             |
| `["findfirst", "n=500", "reduce", "basesize=128"]`  |  52.547 ms (5%) |           |  152.59 KiB (1%) |        2677 |
| `["findfirst", "n=500", "reduce", "basesize=256"]`  |  52.308 ms (5%) |           |   82.00 KiB (1%) |        1444 |
| `["findfirst", "n=500", "reduce", "basesize=512"]`  |  55.710 ms (5%) |           |   46.83 KiB (1%) |         827 |
| `["overhead", "default"]`                           | 180.201 μs (5%) |           |  140.72 KiB (1%) |        2464 |
| `["overhead", "stoppable=false"]`                   | 176.201 μs (5%) |           |  140.78 KiB (1%) |        2465 |
| `["overhead", "stoppable=true"]`                    | 342.304 μs (5%) |           |  140.78 KiB (1%) |        2465 |
| `["parallel_histogram", "assoc", "basesize=16384"]` |   5.539 ms (5%) |           |  731.81 KiB (1%) |          94 |
| `["parallel_histogram", "assoc", "basesize=4096"]`  |   6.293 ms (5%) |           |    1.80 MiB (1%) |         448 |
| `["parallel_histogram", "assoc", "basesize=8192"]`  |   5.920 ms (5%) |           |    1.43 MiB (1%) |         220 |
| `["parallel_histogram", "comm", "basesize=16384"]`  |  15.858 ms (5%) |           |    1.22 MiB (1%) |         160 |
| `["parallel_histogram", "comm", "basesize=4096"]`   |  23.439 ms (5%) |           |    1.03 MiB (1%) |        1678 |
| `["parallel_histogram", "comm", "basesize=8192"]`   |  19.691 ms (5%) |           |    1.25 MiB (1%) |        1232 |
| `["parallel_histogram", "seq"]`                     |  10.185 ms (5%) |           |  364.61 KiB (1%) |          24 |
| `["sum", "random", "foldl"]`                        |  19.819 ms (5%) |           |    32 bytes (1%) |           2 |
| `["sum", "random", "reduce", "basesize=128"]`       |  10.328 ms (5%) |           |  292.02 KiB (1%) |        5213 |
| `["sum", "random", "reduce", "basesize=256"]`       |  10.169 ms (5%) |           |  144.53 KiB (1%) |        2589 |
| `["sum", "random", "reduce", "basesize=512"]`       |  10.072 ms (5%) |           |   71.11 KiB (1%) |        1279 |
| `["sum", "uniform", "foldl"]`                       |  19.422 ms (5%) |           |    32 bytes (1%) |           2 |
| `["sum", "uniform", "reduce", "basesize=128"]`      |  10.163 ms (5%) |           |  292.02 KiB (1%) |        5213 |
| `["sum", "uniform", "reduce", "basesize=256"]`      |  10.001 ms (5%) |           |  144.53 KiB (1%) |        2589 |
| `["sum", "uniform", "reduce", "basesize=512"]`      |   9.855 ms (5%) |           |   71.06 KiB (1%) |        1278 |
| `["sum", "valley", "foldl"]`                        |  20.005 ms (5%) |           |    32 bytes (1%) |           2 |
| `["sum", "valley", "reduce", "basesize=128"]`       |  10.436 ms (5%) |           |  292.02 KiB (1%) |        5213 |
| `["sum", "valley", "reduce", "basesize=256"]`       |  10.297 ms (5%) |           |  144.53 KiB (1%) |        2589 |
| `["sum", "valley", "reduce", "basesize=512"]`       |  10.164 ms (5%) |           |   71.06 KiB (1%) |        1278 |
| `["words", "nthreads=1"]`                           |  28.969 ms (5%) |           |   31.52 MiB (1%) |     1027131 |
| `["words", "nthreads=2"]`                           |  17.688 ms (5%) |           |   32.24 MiB (1%) |     1027285 |
| `["words", "nthreads=4"]`                           |  18.604 ms (5%) |           |   32.88 MiB (1%) |     1027544 |

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
Julia Version 1.5.2
Commit 539f3ce943 (2020-09-23 23:17 UTC)
Platform Info:
  OS: Linux (x86_64-pc-linux-gnu)
      Ubuntu 18.04.5 LTS
  uname: Linux 5.4.0-1031-azure #32~18.04.1-Ubuntu SMP Tue Oct 6 10:03:22 UTC 2020 x86_64 x86_64
  CPU: Intel(R) Xeon(R) Platinum 8171M CPU @ 2.60GHz: 
              speed         user         nice          sys         idle          irq
       #1  2095 MHz      47388 s          0 s       2188 s      42191 s          0 s
       #2  2095 MHz      52031 s          0 s       2343 s      37773 s          0 s
       
  Memory: 6.764892578125 GB (3422.58984375 MB free)
  Uptime: 940.0 sec
  Load Avg:  1.70947265625  1.4970703125  0.87939453125
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-9.0.1 (ORCJIT, skylake-avx512)
```

---
# Baseline result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmark: 24 Oct 2020 - 1:22
* Package commit: da98f2
* Julia commit: 539f3c
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
| `["collect", "assoc", "basesize=1"]`                | 378.256 ms (5%) | 12.226 ms |   82.15 MiB (1%) |     1368047 |
| `["collect", "assoc", "basesize=1024"]`             | 250.006 ms (5%) |           |    1.83 MiB (1%) |        1597 |
| `["collect", "assoc", "basesize=32"]`               | 255.307 ms (5%) |           |    5.47 MiB (1%) |       47069 |
| `["collect", "seq"]`                                | 497.157 ms (5%) |           |  512.72 KiB (1%) |          15 |
| `["collect", "unordered", "basesize=1"]`            | 506.081 ms (5%) |           |   30.01 MiB (1%) |      360582 |
| `["collect", "unordered", "basesize=1024"]`         | 319.630 ms (5%) |           |  792.36 KiB (1%) |        2095 |
| `["collect", "unordered", "basesize=32"]`           | 276.989 ms (5%) |           |    1.46 MiB (1%) |       12251 |
| `["findfirst", "n=1000", "foldl"]`                  | 790.182 ms (5%) |           |                  |             |
| `["findfirst", "n=1000", "reduce", "basesize=128"]` | 397.894 ms (5%) |           |  546.33 KiB (1%) |        9561 |
| `["findfirst", "n=1000", "reduce", "basesize=256"]` | 398.315 ms (5%) |           |  278.25 KiB (1%) |        4888 |
| `["findfirst", "n=1000", "reduce", "basesize=512"]` | 405.269 ms (5%) |           |  144.66 KiB (1%) |        2550 |
| `["findfirst", "n=400", "foldl"]`                   | 590.765 ms (5%) |           |                  |             |
| `["findfirst", "n=400", "reduce", "basesize=128"]`  | 299.780 ms (5%) |           | 1012.86 KiB (1%) |       17725 |
| `["findfirst", "n=400", "reduce", "basesize=256"]`  | 299.136 ms (5%) |           |  509.63 KiB (1%) |        8952 |
| `["findfirst", "n=400", "reduce", "basesize=512"]`  | 301.708 ms (5%) |           |  258.83 KiB (1%) |        4563 |
| `["findfirst", "n=500", "foldl"]`                   | 102.043 ms (5%) |           |                  |             |
| `["findfirst", "n=500", "reduce", "basesize=128"]`  |  52.503 ms (5%) |           |  152.59 KiB (1%) |        2677 |
| `["findfirst", "n=500", "reduce", "basesize=256"]`  |  52.209 ms (5%) |           |   82.00 KiB (1%) |        1444 |
| `["findfirst", "n=500", "reduce", "basesize=512"]`  |  55.533 ms (5%) |           |   46.84 KiB (1%) |         828 |
| `["overhead", "default"]`                           | 180.203 μs (5%) |           |  140.75 KiB (1%) |        2465 |
| `["overhead", "stoppable=false"]`                   | 181.203 μs (5%) |           |  140.78 KiB (1%) |        2465 |
| `["overhead", "stoppable=true"]`                    | 339.206 μs (5%) |           |  140.78 KiB (1%) |        2465 |
| `["parallel_histogram", "assoc", "basesize=16384"]` |   5.605 ms (5%) |           |  731.81 KiB (1%) |          94 |
| `["parallel_histogram", "assoc", "basesize=4096"]`  |   6.375 ms (5%) |           |    1.80 MiB (1%) |         448 |
| `["parallel_histogram", "assoc", "basesize=8192"]`  |   5.997 ms (5%) |           |    1.43 MiB (1%) |         220 |
| `["parallel_histogram", "comm", "basesize=16384"]`  |  15.652 ms (5%) |           |    1.22 MiB (1%) |         194 |
| `["parallel_histogram", "comm", "basesize=4096"]`   |  23.182 ms (5%) |           |    1.02 MiB (1%) |        1683 |
| `["parallel_histogram", "comm", "basesize=8192"]`   |  19.590 ms (5%) |           |    1.24 MiB (1%) |         912 |
| `["parallel_histogram", "seq"]`                     |  10.202 ms (5%) |           |  364.61 KiB (1%) |          24 |
| `["sum", "random", "foldl"]`                        |  19.974 ms (5%) |           |    32 bytes (1%) |           2 |
| `["sum", "random", "reduce", "basesize=128"]`       |  10.420 ms (5%) |           |  292.02 KiB (1%) |        5213 |
| `["sum", "random", "reduce", "basesize=256"]`       |  10.232 ms (5%) |           |  144.53 KiB (1%) |        2589 |
| `["sum", "random", "reduce", "basesize=512"]`       |  10.110 ms (5%) |           |   71.11 KiB (1%) |        1279 |
| `["sum", "uniform", "foldl"]`                       |  19.448 ms (5%) |           |    32 bytes (1%) |           2 |
| `["sum", "uniform", "reduce", "basesize=128"]`      |  10.162 ms (5%) |           |  292.02 KiB (1%) |        5213 |
| `["sum", "uniform", "reduce", "basesize=256"]`      |   9.991 ms (5%) |           |  144.53 KiB (1%) |        2589 |
| `["sum", "uniform", "reduce", "basesize=512"]`      |   9.863 ms (5%) |           |   71.06 KiB (1%) |        1278 |
| `["sum", "valley", "foldl"]`                        |  20.024 ms (5%) |           |    32 bytes (1%) |           2 |
| `["sum", "valley", "reduce", "basesize=128"]`       |  10.425 ms (5%) |           |  292.02 KiB (1%) |        5213 |
| `["sum", "valley", "reduce", "basesize=256"]`       |  10.295 ms (5%) |           |  144.53 KiB (1%) |        2589 |
| `["sum", "valley", "reduce", "basesize=512"]`       |  10.129 ms (5%) |           |   71.09 KiB (1%) |        1279 |
| `["words", "nthreads=1"]`                           |  29.128 ms (5%) |           |   31.62 MiB (1%) |     1030416 |
| `["words", "nthreads=2"]`                           |  17.439 ms (5%) |           |   31.98 MiB (1%) |     1030494 |
| `["words", "nthreads=4"]`                           |  17.687 ms (5%) |           |   32.70 MiB (1%) |     1030641 |

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
Julia Version 1.5.2
Commit 539f3ce943 (2020-09-23 23:17 UTC)
Platform Info:
  OS: Linux (x86_64-pc-linux-gnu)
      Ubuntu 18.04.5 LTS
  uname: Linux 5.4.0-1031-azure #32~18.04.1-Ubuntu SMP Tue Oct 6 10:03:22 UTC 2020 x86_64 x86_64
  CPU: Intel(R) Xeon(R) Platinum 8171M CPU @ 2.60GHz: 
              speed         user         nice          sys         idle          irq
       #1  2095 MHz      68342 s          0 s       2747 s      52554 s          0 s
       #2  2095 MHz      78860 s          0 s       2966 s      42416 s          0 s
       
  Memory: 6.764892578125 GB (3431.90625 MB free)
  Uptime: 1263.0 sec
  Load Avg:  1.5703125  1.50830078125  1.0654296875
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
    CPU MHz:             2095.079
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
| Address Size       | 48 bits virtual, 44 bits physical                       |
| SIMD               | 512 bit = 64 byte max. SIMD vector size                 |
| Time Stamp Counter | TSC is accessible via `rdtsc`                           |
|                    | TSC increased at every clock cycle (non-invariant TSC)  |
| Perf. Monitoring   | Performance Monitoring Counters (PMC) are not supported |
| Hypervisor         | Yes, Microsoft                                          |

