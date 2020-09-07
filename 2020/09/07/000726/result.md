# Multi-thread benchmark result (via Travis)


# Judge result
# Benchmark Report for */home/travis/build/JuliaFolds/Transducers.jl*

## Job Properties
* Time of benchmarks:
    - Target: 7 Sep 2020 - 00:02
    - Baseline: 7 Sep 2020 - 00:07
* Package commits:
    - Target: 511d1e
    - Baseline: 733595
* Julia commits:
    - Target: 697e78
    - Baseline: 697e78
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
| `["collect", "unordered", "basesize=1024"]`         |                   0.97 (5%)  | 0.98 (1%) :white_check_mark: |
| `["parallel_histogram", "assoc", "basesize=4096"]`  |                   1.03 (5%)  |                1.15 (1%) :x: |
| `["parallel_histogram", "comm", "basesize=16384"]`  |                   0.97 (5%)  | 0.99 (1%) :white_check_mark: |
| `["parallel_histogram", "comm", "basesize=4096"]`   |                1.08 (5%) :x: | 0.97 (1%) :white_check_mark: |
| `["parallel_histogram", "comm", "basesize=8192"]`   |                   0.98 (5%)  |                1.05 (1%) :x: |
| `["words", "nthreads=1"]`                           | 0.95 (5%) :white_check_mark: |                   1.00 (1%)  |

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
Julia Version 1.5.1
Commit 697e782ab8 (2020-08-25 20:08 UTC)
Platform Info:
  OS: Linux (x86_64-pc-linux-gnu)
      Ubuntu 16.04.6 LTS
  uname: Linux 4.15.0-1028-gcp #29~16.04.1-Ubuntu SMP Tue Feb 12 16:31:10 UTC 2019 x86_64 x86_64
  CPU: Intel(R) Xeon(R) CPU: 
              speed         user         nice          sys         idle          irq
       #1  2800 MHz      47059 s          0 s       1840 s      17048 s          0 s
       #2  2800 MHz      51526 s          0 s       1616 s      13020 s          0 s
       
  Memory: 7.7900238037109375 GB (5896.87109375 MB free)
  Uptime: 666.0 sec
  Load Avg:  1.775390625  1.53173828125  0.8662109375
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-9.0.1 (ORCJIT, cascadelake)
```

### Baseline
```
Julia Version 1.5.1
Commit 697e782ab8 (2020-08-25 20:08 UTC)
Platform Info:
  OS: Linux (x86_64-pc-linux-gnu)
      Ubuntu 16.04.6 LTS
  uname: Linux 4.15.0-1028-gcp #29~16.04.1-Ubuntu SMP Tue Feb 12 16:31:10 UTC 2019 x86_64 x86_64
  CPU: Intel(R) Xeon(R) CPU: 
              speed         user         nice          sys         idle          irq
       #1  2800 MHz      69027 s          0 s       2226 s      22387 s          0 s
       #2  2800 MHz      73236 s          0 s       1976 s      18550 s          0 s
       
  Memory: 7.7900238037109375 GB (5968.6015625 MB free)
  Uptime: 943.0 sec
  Load Avg:  1.67236328125  1.6162109375  1.07861328125
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-9.0.1 (ORCJIT, cascadelake)
```

---
# Target result
# Benchmark Report for */home/travis/build/JuliaFolds/Transducers.jl*

## Job Properties
* Time of benchmark: 7 Sep 2020 - 0:2
* Package commit: 511d1e
* Julia commit: 697e78
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
| `["collect", "assoc", "basesize=1"]`                | 309.802 ms (5%) | 15.131 ms |   82.16 MiB (1%) |     1368083 |
| `["collect", "assoc", "basesize=1024"]`             | 179.457 ms (5%) |           |    1.83 MiB (1%) |        1597 |
| `["collect", "assoc", "basesize=32"]`               | 184.963 ms (5%) |           |    5.47 MiB (1%) |       47069 |
| `["collect", "seq"]`                                | 349.889 ms (5%) |           |  512.72 KiB (1%) |          15 |
| `["collect", "unordered", "basesize=1"]`            | 353.972 ms (5%) |           |   30.01 MiB (1%) |      360624 |
| `["collect", "unordered", "basesize=1024"]`         | 202.924 ms (5%) |           |  824.20 KiB (1%) |        3096 |
| `["collect", "unordered", "basesize=32"]`           | 200.860 ms (5%) |           |    1.49 MiB (1%) |       13277 |
| `["findfirst", "n=1000", "foldl"]`                  | 557.097 ms (5%) |           |                  |             |
| `["findfirst", "n=1000", "reduce", "basesize=128"]` | 300.826 ms (5%) |           |  546.38 KiB (1%) |        9563 |
| `["findfirst", "n=1000", "reduce", "basesize=256"]` | 299.528 ms (5%) |           |  278.25 KiB (1%) |        4888 |
| `["findfirst", "n=1000", "reduce", "basesize=512"]` | 304.792 ms (5%) |           |  144.66 KiB (1%) |        2550 |
| `["findfirst", "n=400", "foldl"]`                   | 418.080 ms (5%) |           |                  |             |
| `["findfirst", "n=400", "reduce", "basesize=128"]`  | 227.933 ms (5%) |           | 1012.91 KiB (1%) |       17727 |
| `["findfirst", "n=400", "reduce", "basesize=256"]`  | 225.634 ms (5%) |           |  509.63 KiB (1%) |        8952 |
| `["findfirst", "n=400", "reduce", "basesize=512"]`  | 226.849 ms (5%) |           |  258.84 KiB (1%) |        4564 |
| `["findfirst", "n=500", "foldl"]`                   |  72.424 ms (5%) |           |                  |             |
| `["findfirst", "n=500", "reduce", "basesize=128"]`  |  39.714 ms (5%) |           |  152.59 KiB (1%) |        2677 |
| `["findfirst", "n=500", "reduce", "basesize=256"]`  |  39.451 ms (5%) |           |   82.00 KiB (1%) |        1444 |
| `["findfirst", "n=500", "reduce", "basesize=512"]`  |  41.927 ms (5%) |           |   46.84 KiB (1%) |         828 |
| `["overhead", "default"]`                           | 196.370 μs (5%) |           |  140.75 KiB (1%) |        2465 |
| `["overhead", "stoppable=false"]`                   | 193.764 μs (5%) |           |  140.78 KiB (1%) |        2465 |
| `["overhead", "stoppable=true"]`                    | 374.659 μs (5%) |           |  140.78 KiB (1%) |        2465 |
| `["parallel_histogram", "assoc", "basesize=16384"]` |   4.862 ms (5%) |           |  731.81 KiB (1%) |          94 |
| `["parallel_histogram", "assoc", "basesize=4096"]`  |   5.737 ms (5%) |           |    2.07 MiB (1%) |         454 |
| `["parallel_histogram", "assoc", "basesize=8192"]`  |   5.289 ms (5%) |           |    1.43 MiB (1%) |         220 |
| `["parallel_histogram", "comm", "basesize=16384"]`  |  11.721 ms (5%) |           |    1.24 MiB (1%) |         771 |
| `["parallel_histogram", "comm", "basesize=4096"]`   |  16.716 ms (5%) |           |    1.40 MiB (1%) |        6087 |
| `["parallel_histogram", "comm", "basesize=8192"]`   |  13.702 ms (5%) |           |    1.34 MiB (1%) |        4158 |
| `["parallel_histogram", "seq"]`                     |   7.451 ms (5%) |           |  364.61 KiB (1%) |          24 |
| `["sum", "random", "foldl"]`                        |  14.095 ms (5%) |           |    32 bytes (1%) |           2 |
| `["sum", "random", "reduce", "basesize=128"]`       |   8.025 ms (5%) |           |  292.02 KiB (1%) |        5213 |
| `["sum", "random", "reduce", "basesize=256"]`       |   7.848 ms (5%) |           |  144.53 KiB (1%) |        2589 |
| `["sum", "random", "reduce", "basesize=512"]`       |   7.719 ms (5%) |           |   71.11 KiB (1%) |        1279 |
| `["sum", "uniform", "foldl"]`                       |  13.690 ms (5%) |           |    32 bytes (1%) |           2 |
| `["sum", "uniform", "reduce", "basesize=128"]`      |   7.764 ms (5%) |           |  292.02 KiB (1%) |        5213 |
| `["sum", "uniform", "reduce", "basesize=256"]`      |   7.547 ms (5%) |           |  144.53 KiB (1%) |        2589 |
| `["sum", "uniform", "reduce", "basesize=512"]`      |   7.444 ms (5%) |           |   71.06 KiB (1%) |        1278 |
| `["sum", "valley", "foldl"]`                        |  14.117 ms (5%) |           |    32 bytes (1%) |           2 |
| `["sum", "valley", "reduce", "basesize=128"]`       |   8.046 ms (5%) |           |  292.02 KiB (1%) |        5213 |
| `["sum", "valley", "reduce", "basesize=256"]`       |   7.865 ms (5%) |           |  144.53 KiB (1%) |        2589 |
| `["sum", "valley", "reduce", "basesize=512"]`       |   7.737 ms (5%) |           |   71.06 KiB (1%) |        1278 |
| `["words", "nthreads=1"]`                           |  21.916 ms (5%) |           |   31.52 MiB (1%) |     1026491 |
| `["words", "nthreads=2"]`                           |  24.878 ms (5%) |           |   32.24 MiB (1%) |     1026701 |
| `["words", "nthreads=4"]`                           |  25.973 ms (5%) |           |   32.87 MiB (1%) |     1027001 |

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
Julia Version 1.5.1
Commit 697e782ab8 (2020-08-25 20:08 UTC)
Platform Info:
  OS: Linux (x86_64-pc-linux-gnu)
      Ubuntu 16.04.6 LTS
  uname: Linux 4.15.0-1028-gcp #29~16.04.1-Ubuntu SMP Tue Feb 12 16:31:10 UTC 2019 x86_64 x86_64
  CPU: Intel(R) Xeon(R) CPU: 
              speed         user         nice          sys         idle          irq
       #1  2800 MHz      47059 s          0 s       1840 s      17048 s          0 s
       #2  2800 MHz      51526 s          0 s       1616 s      13020 s          0 s
       
  Memory: 7.7900238037109375 GB (5896.87109375 MB free)
  Uptime: 666.0 sec
  Load Avg:  1.775390625  1.53173828125  0.8662109375
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-9.0.1 (ORCJIT, cascadelake)
```

---
# Baseline result
# Benchmark Report for */home/travis/build/JuliaFolds/Transducers.jl*

## Job Properties
* Time of benchmark: 7 Sep 2020 - 0:7
* Package commit: 733595
* Julia commit: 697e78
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
| `["collect", "assoc", "basesize=1"]`                | 312.388 ms (5%) | 13.844 ms |   82.16 MiB (1%) |     1368082 |
| `["collect", "assoc", "basesize=1024"]`             | 179.979 ms (5%) |           |    1.83 MiB (1%) |        1596 |
| `["collect", "assoc", "basesize=32"]`               | 185.067 ms (5%) |           |    5.47 MiB (1%) |       47070 |
| `["collect", "seq"]`                                | 349.733 ms (5%) |           |  512.72 KiB (1%) |          15 |
| `["collect", "unordered", "basesize=1"]`            | 369.933 ms (5%) |  9.260 ms |   30.28 MiB (1%) |      369616 |
| `["collect", "unordered", "basesize=1024"]`         | 208.449 ms (5%) |           |  842.70 KiB (1%) |        3688 |
| `["collect", "unordered", "basesize=32"]`           | 198.674 ms (5%) |           |    1.49 MiB (1%) |       13146 |
| `["findfirst", "n=1000", "foldl"]`                  | 556.012 ms (5%) |           |                  |             |
| `["findfirst", "n=1000", "reduce", "basesize=128"]` | 300.689 ms (5%) |           |  546.34 KiB (1%) |        9562 |
| `["findfirst", "n=1000", "reduce", "basesize=256"]` | 299.650 ms (5%) |           |  278.25 KiB (1%) |        4888 |
| `["findfirst", "n=1000", "reduce", "basesize=512"]` | 304.459 ms (5%) |           |  144.66 KiB (1%) |        2550 |
| `["findfirst", "n=400", "foldl"]`                   | 417.247 ms (5%) |           |                  |             |
| `["findfirst", "n=400", "reduce", "basesize=128"]`  | 227.793 ms (5%) |           | 1012.91 KiB (1%) |       17727 |
| `["findfirst", "n=400", "reduce", "basesize=256"]`  | 225.557 ms (5%) |           |  509.63 KiB (1%) |        8952 |
| `["findfirst", "n=400", "reduce", "basesize=512"]`  | 226.602 ms (5%) |           |  258.84 KiB (1%) |        4564 |
| `["findfirst", "n=500", "foldl"]`                   |  72.317 ms (5%) |           |                  |             |
| `["findfirst", "n=500", "reduce", "basesize=128"]`  |  39.609 ms (5%) |           |  152.59 KiB (1%) |        2677 |
| `["findfirst", "n=500", "reduce", "basesize=256"]`  |  39.433 ms (5%) |           |   82.00 KiB (1%) |        1444 |
| `["findfirst", "n=500", "reduce", "basesize=512"]`  |  41.924 ms (5%) |           |   46.84 KiB (1%) |         828 |
| `["overhead", "default"]`                           | 197.168 μs (5%) |           |  140.75 KiB (1%) |        2465 |
| `["overhead", "stoppable=false"]`                   | 193.473 μs (5%) |           |  140.78 KiB (1%) |        2465 |
| `["overhead", "stoppable=true"]`                    | 374.846 μs (5%) |           |  140.81 KiB (1%) |        2466 |
| `["parallel_histogram", "assoc", "basesize=16384"]` |   4.769 ms (5%) |           |  731.81 KiB (1%) |          94 |
| `["parallel_histogram", "assoc", "basesize=4096"]`  |   5.596 ms (5%) |           |    1.80 MiB (1%) |         448 |
| `["parallel_histogram", "assoc", "basesize=8192"]`  |   5.194 ms (5%) |           |    1.43 MiB (1%) |         220 |
| `["parallel_histogram", "comm", "basesize=16384"]`  |  12.140 ms (5%) |           |    1.26 MiB (1%) |        1364 |
| `["parallel_histogram", "comm", "basesize=4096"]`   |  15.432 ms (5%) |           |    1.45 MiB (1%) |        7631 |
| `["parallel_histogram", "comm", "basesize=8192"]`   |  14.049 ms (5%) |           |    1.27 MiB (1%) |        1895 |
| `["parallel_histogram", "seq"]`                     |   7.478 ms (5%) |           |  364.61 KiB (1%) |          24 |
| `["sum", "random", "foldl"]`                        |  13.972 ms (5%) |           |    32 bytes (1%) |           2 |
| `["sum", "random", "reduce", "basesize=128"]`       |   8.006 ms (5%) |           |  292.02 KiB (1%) |        5213 |
| `["sum", "random", "reduce", "basesize=256"]`       |   7.797 ms (5%) |           |  144.53 KiB (1%) |        2589 |
| `["sum", "random", "reduce", "basesize=512"]`       |   7.655 ms (5%) |           |   71.11 KiB (1%) |        1279 |
| `["sum", "uniform", "foldl"]`                       |  13.724 ms (5%) |           |    32 bytes (1%) |           2 |
| `["sum", "uniform", "reduce", "basesize=128"]`      |   7.797 ms (5%) |           |  292.02 KiB (1%) |        5213 |
| `["sum", "uniform", "reduce", "basesize=256"]`      |   7.611 ms (5%) |           |  144.53 KiB (1%) |        2589 |
| `["sum", "uniform", "reduce", "basesize=512"]`      |   7.470 ms (5%) |           |   71.06 KiB (1%) |        1278 |
| `["sum", "valley", "foldl"]`                        |  14.120 ms (5%) |           |    32 bytes (1%) |           2 |
| `["sum", "valley", "reduce", "basesize=128"]`       |   8.092 ms (5%) |           |  292.02 KiB (1%) |        5213 |
| `["sum", "valley", "reduce", "basesize=256"]`       |   7.888 ms (5%) |           |  144.53 KiB (1%) |        2589 |
| `["sum", "valley", "reduce", "basesize=512"]`       |   7.756 ms (5%) |           |   71.06 KiB (1%) |        1278 |
| `["words", "nthreads=1"]`                           |  23.082 ms (5%) |           |   31.44 MiB (1%) |     1024179 |
| `["words", "nthreads=2"]`                           |  25.316 ms (5%) |           |   32.16 MiB (1%) |     1024317 |
| `["words", "nthreads=4"]`                           |  26.413 ms (5%) |           |   32.61 MiB (1%) |     1024454 |

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
Julia Version 1.5.1
Commit 697e782ab8 (2020-08-25 20:08 UTC)
Platform Info:
  OS: Linux (x86_64-pc-linux-gnu)
      Ubuntu 16.04.6 LTS
  uname: Linux 4.15.0-1028-gcp #29~16.04.1-Ubuntu SMP Tue Feb 12 16:31:10 UTC 2019 x86_64 x86_64
  CPU: Intel(R) Xeon(R) CPU: 
              speed         user         nice          sys         idle          irq
       #1  2800 MHz      69027 s          0 s       2226 s      22387 s          0 s
       #2  2800 MHz      73236 s          0 s       1976 s      18550 s          0 s
       
  Memory: 7.7900238037109375 GB (5968.6015625 MB free)
  Uptime: 943.0 sec
  Load Avg:  1.67236328125  1.6162109375  1.07861328125
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-9.0.1 (ORCJIT, cascadelake)
```

---
# Runtime information
| Runtime Info | |
|:--|:--|
| BLAS #threads | 2 |
| `BLAS.vendor()` | `openblas64` |
| `Sys.CPU_THREADS` | 2 |

`lscpu` output:

    Architecture:          x86_64
    CPU op-mode(s):        32-bit, 64-bit
    Byte Order:            Little Endian
    CPU(s):                2
    On-line CPU(s) list:   0,1
    Thread(s) per core:    2
    Core(s) per socket:    1
    Socket(s):             1
    NUMA node(s):          1
    Vendor ID:             GenuineIntel
    CPU family:            6
    Model:                 85
    Model name:            Intel(R) Xeon(R) CPU
    Stepping:              7
    CPU MHz:               2800.196
    BogoMIPS:              5600.39
    Hypervisor vendor:     KVM
    Virtualization type:   full
    L1d cache:             32K
    L1i cache:             32K
    L2 cache:              1024K
    L3 cache:              33792K
    NUMA node0 CPU(s):     0,1
    Flags:                 fpu vme de pse tsc msr pae mce cx8 apic sep mtrr pge mca cmov pat pse36 clflush mmx fxsr sse sse2 ss ht syscall nx pdpe1gb rdtscp lm constant_tsc rep_good nopl xtopology nonstop_tsc cpuid pni pclmulqdq ssse3 fma cx16 pcid sse4_1 sse4_2 x2apic movbe popcnt aes xsave avx f16c rdrand hypervisor lahf_lm abm 3dnowprefetch invpcid_single ssbd ibrs ibpb stibp ibrs_enhanced fsgsbase tsc_adjust bmi1 hle avx2 smep bmi2 erms invpcid rtm mpx avx512f avx512dq rdseed adx smap clflushopt clwb avx512cd avx512bw avx512vl xsaveopt xsavec xgetbv1 xsaves arat avx512_vnni arch_capabilities
    

| Cpu Property       | Value                                                      |
|:------------------ |:---------------------------------------------------------- |
| Brand              | Intel(R) Xeon(R) CPU                                       |
| Vendor             | :Intel                                                     |
| Architecture       | :Skylake                                                   |
| Model              | Family: 0x06, Model: 0x55, Stepping: 0x07, Type: 0x00      |
| Cores              | 1 physical cores, 2 logical cores (on executing CPU)       |
|                    | Hyperthreading detected                                    |
| Clock Frequencies  | Not supported by CPU                                       |
| Data Cache         | Level 1:3 : (32, 1024, 33792) kbytes                       |
|                    | 64 byte cache line size                                    |
| Address Size       | 48 bits virtual, 46 bits physical                          |
| SIMD               | 512 bit = 64 byte max. SIMD vector size                    |
| Time Stamp Counter | TSC is accessible via `rdtsc`                              |
|                    | TSC runs at constant rate (invariant from clock frequency) |
| Perf. Monitoring   | Performance Monitoring Counters (PMC) are not supported    |
| Hypervisor         | Yes, KVM                                                   |

