# Multi-thread benchmark result

* Pull request commit: [`9d734623018adac87e42211d88491c01ae305bc1`](https://github.com/JuliaFolds/Transducers.jl/commit/9d734623018adac87e42211d88491c01ae305bc1)
* Pull request: <https://github.com/JuliaFolds/Transducers.jl/pull/396> (Run Aqua.test_stale_deps(Transducers))

# Judge result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmarks:
    - Target: 4 Aug 2020 - 17:29
    - Baseline: 4 Aug 2020 - 17:34
* Package commits:
    - Target: 60cd8b
    - Baseline: 5c0b7f
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
| `["collect", "unordered", "basesize=1"]`            | 0.94 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["collect", "unordered", "basesize=1024"]`         | 0.94 (5%) :white_check_mark: |                   0.99 (1%)  |
| `["parallel_histogram", "comm", "basesize=4096"]`   |                   0.99 (5%)  | 0.98 (1%) :white_check_mark: |
| `["parallel_histogram", "comm", "basesize=8192"]`   | 0.80 (5%) :white_check_mark: | 0.96 (1%) :white_check_mark: |

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
  CPU: Intel(R) Xeon(R) CPU E5-2673 v3 @ 2.40GHz: 
              speed         user         nice          sys         idle          irq
       #1  2394 MHz      46619 s          0 s       2202 s      21565 s          0 s
       #2  2394 MHz      53415 s          0 s       2342 s      13982 s          0 s
       
  Memory: 6.764881134033203 GB (2911.04296875 MB free)
  Uptime: 721.0 sec
  Load Avg:  1.70068359375  1.50439453125  0.8896484375
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-8.0.1 (ORCJIT, haswell)
```

### Baseline
```
Julia Version 1.4.2
Commit 44fa15b150* (2020-05-23 18:35 UTC)
Platform Info:
  OS: Linux (x86_64-pc-linux-gnu)
      Ubuntu 18.04.4 LTS
  uname: Linux 5.3.0-1034-azure #35~18.04.1-Ubuntu SMP Mon Jul 13 12:54:45 UTC 2020 x86_64 x86_64
  CPU: Intel(R) Xeon(R) CPU E5-2673 v3 @ 2.40GHz: 
              speed         user         nice          sys         idle          irq
       #1  2394 MHz      65244 s          0 s       2694 s      30681 s          0 s
       #2  2394 MHz      79070 s          0 s       2769 s      16128 s          0 s
       
  Memory: 6.764881134033203 GB (2918.02734375 MB free)
  Uptime: 1005.0 sec
  Load Avg:  1.57568359375  1.53759765625  1.06689453125
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-8.0.1 (ORCJIT, haswell)
```

---
# Target result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmark: 4 Aug 2020 - 17:29
* Package commit: 60cd8b
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
| `["collect", "assoc", "basesize=1"]`                | 352.856 ms (5%) | 10.613 ms |  87.55 MiB (1%) |     1590772 |
| `["collect", "assoc", "basesize=1024"]`             | 217.472 ms (5%) |           |   1.84 MiB (1%) |        1812 |
| `["collect", "assoc", "basesize=32"]`               | 221.957 ms (5%) |           |   5.64 MiB (1%) |       54013 |
| `["collect", "seq"]`                                | 429.387 ms (5%) |           |   1.50 MiB (1%) |       32784 |
| `["collect", "unordered", "basesize=1"]`            | 430.348 ms (5%) |           |  29.14 MiB (1%) |      401870 |
| `["collect", "unordered", "basesize=1024"]`         | 276.232 ms (5%) |           | 839.66 KiB (1%) |        6785 |
| `["collect", "unordered", "basesize=32"]`           | 244.187 ms (5%) |           |   1.50 MiB (1%) |       18471 |
| `["findfirst", "n=1000", "foldl"]`                  | 629.529 ms (5%) |           |                 |             |
| `["findfirst", "n=1000", "reduce", "basesize=128"]` | 319.189 ms (5%) |           | 564.13 KiB (1%) |       10231 |
| `["findfirst", "n=1000", "reduce", "basesize=256"]` | 320.334 ms (5%) |           | 287.25 KiB (1%) |        5222 |
| `["findfirst", "n=1000", "reduce", "basesize=512"]` | 321.592 ms (5%) |           | 149.30 KiB (1%) |        2720 |
| `["findfirst", "n=400", "foldl"]`                   | 484.048 ms (5%) |           |                 |             |
| `["findfirst", "n=400", "reduce", "basesize=128"]`  | 239.412 ms (5%) |           |   1.02 MiB (1%) |       18971 |
| `["findfirst", "n=400", "reduce", "basesize=256"]`  | 242.004 ms (5%) |           | 526.11 KiB (1%) |        9567 |
| `["findfirst", "n=400", "reduce", "basesize=512"]`  | 251.440 ms (5%) |           | 267.28 KiB (1%) |        4879 |
| `["findfirst", "n=500", "foldl"]`                   |  80.856 ms (5%) |           |                 |             |
| `["findfirst", "n=500", "reduce", "basesize=128"]`  |  41.628 ms (5%) |           | 157.48 KiB (1%) |        2856 |
| `["findfirst", "n=500", "reduce", "basesize=256"]`  |  41.379 ms (5%) |           |  84.61 KiB (1%) |        1537 |
| `["findfirst", "n=500", "reduce", "basesize=512"]`  |  44.065 ms (5%) |           |  48.31 KiB (1%) |         879 |
| `["overhead", "default"]`                           | 182.500 μs (5%) |           | 146.27 KiB (1%) |        2633 |
| `["overhead", "stoppable=false"]`                   | 184.300 μs (5%) |           | 146.27 KiB (1%) |        2632 |
| `["overhead", "stoppable=true"]`                    | 326.801 μs (5%) |           | 146.56 KiB (1%) |        2651 |
| `["parallel_histogram", "assoc", "basesize=16384"]` |   4.589 ms (5%) |           | 732.06 KiB (1%) |         103 |
| `["parallel_histogram", "assoc", "basesize=4096"]`  |   5.282 ms (5%) |           |   1.80 MiB (1%) |         496 |
| `["parallel_histogram", "assoc", "basesize=8192"]`  |   4.928 ms (5%) |           |   1.43 MiB (1%) |         243 |
| `["parallel_histogram", "comm", "basesize=16384"]`  |  11.524 ms (5%) |           |   1.22 MiB (1%) |         187 |
| `["parallel_histogram", "comm", "basesize=4096"]`   |  16.751 ms (5%) |           |   1.02 MiB (1%) |        3346 |
| `["parallel_histogram", "comm", "basesize=8192"]`   |  12.220 ms (5%) |           |   1.22 MiB (1%) |         307 |
| `["parallel_histogram", "seq"]`                     |   8.371 ms (5%) |           | 364.61 KiB (1%) |          24 |
| `["sum", "random", "foldl"]`                        |  16.130 ms (5%) |           |   64 bytes (1%) |           3 |
| `["sum", "random", "reduce", "basesize=128"]`       |   8.459 ms (5%) |           | 313.38 KiB (1%) |        6068 |
| `["sum", "random", "reduce", "basesize=256"]`       |   8.283 ms (5%) |           | 155.16 KiB (1%) |        3013 |
| `["sum", "random", "reduce", "basesize=512"]`       |   8.161 ms (5%) |           |  76.36 KiB (1%) |        1489 |
| `["sum", "uniform", "foldl"]`                       |  15.808 ms (5%) |           |   64 bytes (1%) |           3 |
| `["sum", "uniform", "reduce", "basesize=128"]`      |   8.292 ms (5%) |           | 313.44 KiB (1%) |        6072 |
| `["sum", "uniform", "reduce", "basesize=256"]`      |   8.100 ms (5%) |           | 155.14 KiB (1%) |        3012 |
| `["sum", "uniform", "reduce", "basesize=512"]`      |   7.989 ms (5%) |           |  76.31 KiB (1%) |        1486 |
| `["sum", "valley", "foldl"]`                        |  16.230 ms (5%) |           |   64 bytes (1%) |           3 |
| `["sum", "valley", "reduce", "basesize=128"]`       |   8.499 ms (5%) |           | 313.36 KiB (1%) |        6067 |
| `["sum", "valley", "reduce", "basesize=256"]`       |   8.349 ms (5%) |           | 155.16 KiB (1%) |        3013 |
| `["sum", "valley", "reduce", "basesize=512"]`       |   8.211 ms (5%) |           |  76.34 KiB (1%) |        1488 |
| `["words", "nthreads=1"]`                           |  45.483 ms (5%) |  7.556 ms |  63.01 MiB (1%) |     2059013 |
| `["words", "nthreads=2"]`                           |  21.901 ms (5%) |           |  64.10 MiB (1%) |     2071352 |
| `["words", "nthreads=4"]`                           |  22.282 ms (5%) |           |  64.73 MiB (1%) |     2077567 |

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
  CPU: Intel(R) Xeon(R) CPU E5-2673 v3 @ 2.40GHz: 
              speed         user         nice          sys         idle          irq
       #1  2394 MHz      46619 s          0 s       2202 s      21565 s          0 s
       #2  2394 MHz      53415 s          0 s       2342 s      13982 s          0 s
       
  Memory: 6.764881134033203 GB (2911.04296875 MB free)
  Uptime: 721.0 sec
  Load Avg:  1.70068359375  1.50439453125  0.8896484375
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-8.0.1 (ORCJIT, haswell)
```

---
# Baseline result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmark: 4 Aug 2020 - 17:34
* Package commit: 5c0b7f
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
| `["collect", "assoc", "basesize=1"]`                | 352.622 ms (5%) | 13.315 ms |  87.55 MiB (1%) |     1590783 |
| `["collect", "assoc", "basesize=1024"]`             | 215.844 ms (5%) |           |   1.84 MiB (1%) |        1811 |
| `["collect", "assoc", "basesize=32"]`               | 220.402 ms (5%) |           |   5.64 MiB (1%) |       54012 |
| `["collect", "seq"]`                                | 432.487 ms (5%) |           |   1.50 MiB (1%) |       32784 |
| `["collect", "unordered", "basesize=1"]`            | 456.636 ms (5%) |           |  29.12 MiB (1%) |      400577 |
| `["collect", "unordered", "basesize=1024"]`         | 294.072 ms (5%) |           | 845.06 KiB (1%) |        6840 |
| `["collect", "unordered", "basesize=32"]`           | 242.041 ms (5%) |           |   1.50 MiB (1%) |       18413 |
| `["findfirst", "n=1000", "foldl"]`                  | 628.788 ms (5%) |           |                 |             |
| `["findfirst", "n=1000", "reduce", "basesize=128"]` | 317.742 ms (5%) |           | 564.17 KiB (1%) |       10234 |
| `["findfirst", "n=1000", "reduce", "basesize=256"]` | 319.513 ms (5%) |           | 287.30 KiB (1%) |        5225 |
| `["findfirst", "n=1000", "reduce", "basesize=512"]` | 324.857 ms (5%) |           | 149.31 KiB (1%) |        2721 |
| `["findfirst", "n=400", "foldl"]`                   | 471.520 ms (5%) |           |                 |             |
| `["findfirst", "n=400", "reduce", "basesize=128"]`  | 240.617 ms (5%) |           |   1.02 MiB (1%) |       18977 |
| `["findfirst", "n=400", "reduce", "basesize=256"]`  | 240.337 ms (5%) |           | 526.16 KiB (1%) |        9570 |
| `["findfirst", "n=400", "reduce", "basesize=512"]`  | 241.447 ms (5%) |           | 267.30 KiB (1%) |        4880 |
| `["findfirst", "n=500", "foldl"]`                   |  80.899 ms (5%) |           |                 |             |
| `["findfirst", "n=500", "reduce", "basesize=128"]`  |  41.539 ms (5%) |           | 157.48 KiB (1%) |        2856 |
| `["findfirst", "n=500", "reduce", "basesize=256"]`  |  41.400 ms (5%) |           |  84.59 KiB (1%) |        1536 |
| `["findfirst", "n=500", "reduce", "basesize=512"]`  |  44.034 ms (5%) |           |  48.33 KiB (1%) |         880 |
| `["overhead", "default"]`                           | 189.300 μs (5%) |           | 146.27 KiB (1%) |        2633 |
| `["overhead", "stoppable=false"]`                   | 187.701 μs (5%) |           | 146.30 KiB (1%) |        2634 |
| `["overhead", "stoppable=true"]`                    | 340.001 μs (5%) |           | 146.56 KiB (1%) |        2651 |
| `["parallel_histogram", "assoc", "basesize=16384"]` |   4.571 ms (5%) |           | 732.06 KiB (1%) |         103 |
| `["parallel_histogram", "assoc", "basesize=4096"]`  |   5.245 ms (5%) |           |   1.80 MiB (1%) |         497 |
| `["parallel_histogram", "assoc", "basesize=8192"]`  |   4.902 ms (5%) |           |   1.43 MiB (1%) |         243 |
| `["parallel_histogram", "comm", "basesize=16384"]`  |  11.361 ms (5%) |           |   1.22 MiB (1%) |         159 |
| `["parallel_histogram", "comm", "basesize=4096"]`   |  16.861 ms (5%) |           |   1.04 MiB (1%) |        4439 |
| `["parallel_histogram", "comm", "basesize=8192"]`   |  15.185 ms (5%) |           |   1.27 MiB (1%) |        3247 |
| `["parallel_histogram", "seq"]`                     |   8.389 ms (5%) |           | 364.61 KiB (1%) |          24 |
| `["sum", "random", "foldl"]`                        |  16.158 ms (5%) |           |   64 bytes (1%) |           3 |
| `["sum", "random", "reduce", "basesize=128"]`       |   8.492 ms (5%) |           | 313.39 KiB (1%) |        6069 |
| `["sum", "random", "reduce", "basesize=256"]`       |   8.296 ms (5%) |           | 155.19 KiB (1%) |        3015 |
| `["sum", "random", "reduce", "basesize=512"]`       |   8.168 ms (5%) |           |  76.33 KiB (1%) |        1487 |
| `["sum", "uniform", "foldl"]`                       |  15.820 ms (5%) |           |   64 bytes (1%) |           3 |
| `["sum", "uniform", "reduce", "basesize=128"]`      |   8.305 ms (5%) |           | 313.39 KiB (1%) |        6069 |
| `["sum", "uniform", "reduce", "basesize=256"]`      |   8.123 ms (5%) |           | 155.17 KiB (1%) |        3014 |
| `["sum", "uniform", "reduce", "basesize=512"]`      |   8.006 ms (5%) |           |  76.31 KiB (1%) |        1486 |
| `["sum", "valley", "foldl"]`                        |  16.251 ms (5%) |           |   64 bytes (1%) |           3 |
| `["sum", "valley", "reduce", "basesize=128"]`       |   8.506 ms (5%) |           | 313.34 KiB (1%) |        6066 |
| `["sum", "valley", "reduce", "basesize=256"]`       |   8.358 ms (5%) |           | 155.17 KiB (1%) |        3014 |
| `["sum", "valley", "reduce", "basesize=512"]`       |   8.218 ms (5%) |           |  76.31 KiB (1%) |        1486 |
| `["words", "nthreads=1"]`                           |  45.015 ms (5%) |  7.131 ms |  62.92 MiB (1%) |     2055800 |
| `["words", "nthreads=2"]`                           |  22.361 ms (5%) |           |  63.53 MiB (1%) |     2063945 |
| `["words", "nthreads=4"]`                           |  23.217 ms (5%) |           |  64.80 MiB (1%) |     2076430 |

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
  CPU: Intel(R) Xeon(R) CPU E5-2673 v3 @ 2.40GHz: 
              speed         user         nice          sys         idle          irq
       #1  2394 MHz      65244 s          0 s       2694 s      30681 s          0 s
       #2  2394 MHz      79070 s          0 s       2769 s      16128 s          0 s
       
  Memory: 6.764881134033203 GB (2918.02734375 MB free)
  Uptime: 1005.0 sec
  Load Avg:  1.57568359375  1.53759765625  1.06689453125
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-8.0.1 (ORCJIT, haswell)
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
    Model:               63
    Model name:          Intel(R) Xeon(R) CPU E5-2673 v3 @ 2.40GHz
    Stepping:            2
    CPU MHz:             2394.456
    BogoMIPS:            4788.91
    Hypervisor vendor:   Microsoft
    Virtualization type: full
    L1d cache:           32K
    L1i cache:           32K
    L2 cache:            256K
    L3 cache:            30720K
    NUMA node0 CPU(s):   0,1
    Flags:               fpu vme de pse tsc msr pae mce cx8 apic sep mtrr pge mca cmov pat pse36 clflush mmx fxsr sse sse2 ss ht syscall nx pdpe1gb rdtscp lm constant_tsc rep_good nopl xtopology cpuid pni pclmulqdq ssse3 fma cx16 pcid sse4_1 sse4_2 movbe popcnt aes xsave avx f16c rdrand hypervisor lahf_lm abm invpcid_single pti fsgsbase bmi1 avx2 smep bmi2 erms invpcid xsaveopt md_clear
    

| Cpu Property       | Value                                                   |
|:------------------ |:------------------------------------------------------- |
| Brand              | Intel(R) Xeon(R) CPU E5-2673 v3 @ 2.40GHz               |
| Vendor             | :Intel                                                  |
| Architecture       | :Haswell                                                |
| Model              | Family: 0x06, Model: 0x3f, Stepping: 0x02, Type: 0x00   |
| Cores              | 2 physical cores, 2 logical cores (on executing CPU)    |
|                    | No Hyperthreading detected                              |
| Clock Frequencies  | Not supported by CPU                                    |
| Data Cache         | Level 1:3 : (32, 256, 30720) kbytes                     |
|                    | 64 byte cache line size                                 |
| Address Size       | 48 bits virtual, 44 bits physical                       |
| SIMD               | 256 bit = 32 byte max. SIMD vector size                 |
| Time Stamp Counter | TSC is accessible via `rdtsc`                           |
|                    | TSC increased at every clock cycle (non-invariant TSC)  |
| Perf. Monitoring   | Performance Monitoring Counters (PMC) are not supported |
| Hypervisor         | Yes, Microsoft                                          |

