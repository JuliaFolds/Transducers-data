# Multi-thread benchmark result (via Travis)


# Judge result
# Benchmark Report for */home/travis/build/JuliaFolds/Transducers.jl*

## Job Properties
* Time of benchmarks:
    - Target: 5 Sep 2020 - 01:43
    - Baseline: 5 Sep 2020 - 01:50
* Package commits:
    - Target: 960f74
    - Baseline: ff5762
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
| `["collect", "unordered", "basesize=1024"]`         | 0.95 (5%) :white_check_mark: | 0.99 (1%) :white_check_mark: |
| `["parallel_histogram", "comm", "basesize=16384"]`  | 0.93 (5%) :white_check_mark: |                1.02 (1%) :x: |
| `["parallel_histogram", "comm", "basesize=4096"]`   |                   1.02 (5%)  | 0.83 (1%) :white_check_mark: |
| `["words", "nthreads=2"]`                           |                   0.99 (5%)  | 0.99 (1%) :white_check_mark: |

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
       #1  2800 MHz      49482 s          0 s       1728 s      46464 s          0 s
       #2  2800 MHz      48329 s          0 s       1671 s      48917 s          0 s
       
  Memory: 7.790031433105469 GB (5804.01171875 MB free)
  Uptime: 996.0 sec
  Load Avg:  1.6728515625  1.44287109375  0.8291015625
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
       #1  2800 MHz      70645 s          0 s       2220 s      66493 s          0 s
       #2  2800 MHz      74228 s          0 s       2238 s      64280 s          0 s
       
  Memory: 7.790031433105469 GB (5823.203125 MB free)
  Uptime: 1414.0 sec
  Load Avg:  1.7275390625  1.388671875  0.97802734375
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-9.0.1 (ORCJIT, cascadelake)
```

---
# Target result
# Benchmark Report for */home/travis/build/JuliaFolds/Transducers.jl*

## Job Properties
* Time of benchmark: 5 Sep 2020 - 1:43
* Package commit: 960f74
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
| `["collect", "assoc", "basesize=1"]`                | 312.205 ms (5%) | 12.871 ms |   82.16 MiB (1%) |     1368077 |
| `["collect", "assoc", "basesize=1024"]`             | 180.007 ms (5%) |           |    1.83 MiB (1%) |        1597 |
| `["collect", "assoc", "basesize=32"]`               | 184.450 ms (5%) |           |    5.47 MiB (1%) |       47070 |
| `["collect", "seq"]`                                | 350.178 ms (5%) |           |  512.72 KiB (1%) |          15 |
| `["collect", "unordered", "basesize=1"]`            | 353.396 ms (5%) |           |   30.01 MiB (1%) |      360629 |
| `["collect", "unordered", "basesize=1024"]`         | 199.315 ms (5%) |           |  806.27 KiB (1%) |        2522 |
| `["collect", "unordered", "basesize=32"]`           | 202.832 ms (5%) |           |    1.49 MiB (1%) |       13300 |
| `["findfirst", "n=1000", "foldl"]`                  | 552.837 ms (5%) |           |                  |             |
| `["findfirst", "n=1000", "reduce", "basesize=128"]` | 299.656 ms (5%) |           |  546.33 KiB (1%) |        9561 |
| `["findfirst", "n=1000", "reduce", "basesize=256"]` | 298.399 ms (5%) |           |  278.25 KiB (1%) |        4888 |
| `["findfirst", "n=1000", "reduce", "basesize=512"]` | 302.501 ms (5%) |           |  144.66 KiB (1%) |        2550 |
| `["findfirst", "n=400", "foldl"]`                   | 414.706 ms (5%) |           |                  |             |
| `["findfirst", "n=400", "reduce", "basesize=128"]`  | 226.375 ms (5%) |           | 1012.91 KiB (1%) |       17727 |
| `["findfirst", "n=400", "reduce", "basesize=256"]`  | 224.282 ms (5%) |           |  509.63 KiB (1%) |        8952 |
| `["findfirst", "n=400", "reduce", "basesize=512"]`  | 225.533 ms (5%) |           |  258.84 KiB (1%) |        4564 |
| `["findfirst", "n=500", "foldl"]`                   |  71.879 ms (5%) |           |                  |             |
| `["findfirst", "n=500", "reduce", "basesize=128"]`  |  39.451 ms (5%) |           |  152.59 KiB (1%) |        2677 |
| `["findfirst", "n=500", "reduce", "basesize=256"]`  |  39.172 ms (5%) |           |   82.00 KiB (1%) |        1444 |
| `["findfirst", "n=500", "reduce", "basesize=512"]`  |  41.709 ms (5%) |           |   46.84 KiB (1%) |         828 |
| `["overhead", "default"]`                           | 195.711 μs (5%) |           |  140.75 KiB (1%) |        2465 |
| `["overhead", "stoppable=false"]`                   | 193.305 μs (5%) |           |  140.78 KiB (1%) |        2465 |
| `["overhead", "stoppable=true"]`                    | 372.484 μs (5%) |           |  140.78 KiB (1%) |        2465 |
| `["parallel_histogram", "assoc", "basesize=16384"]` |   4.895 ms (5%) |           |  731.81 KiB (1%) |          94 |
| `["parallel_histogram", "assoc", "basesize=4096"]`  |   5.784 ms (5%) |           |    1.80 MiB (1%) |         448 |
| `["parallel_histogram", "assoc", "basesize=8192"]`  |   5.284 ms (5%) |           |    1.43 MiB (1%) |         220 |
| `["parallel_histogram", "comm", "basesize=16384"]`  |  11.906 ms (5%) |           |    1.28 MiB (1%) |        2138 |
| `["parallel_histogram", "comm", "basesize=4096"]`   |  16.205 ms (5%) |           |    1.19 MiB (1%) |        7136 |
| `["parallel_histogram", "comm", "basesize=8192"]`   |  13.977 ms (5%) |           |    1.32 MiB (1%) |        3425 |
| `["parallel_histogram", "seq"]`                     |   7.501 ms (5%) |           |  364.61 KiB (1%) |          24 |
| `["sum", "random", "foldl"]`                        |  14.081 ms (5%) |           |    32 bytes (1%) |           2 |
| `["sum", "random", "reduce", "basesize=128"]`       |   7.965 ms (5%) |           |  292.02 KiB (1%) |        5213 |
| `["sum", "random", "reduce", "basesize=256"]`       |   7.743 ms (5%) |           |  144.53 KiB (1%) |        2589 |
| `["sum", "random", "reduce", "basesize=512"]`       |   7.650 ms (5%) |           |   71.11 KiB (1%) |        1279 |
| `["sum", "uniform", "foldl"]`                       |  13.625 ms (5%) |           |    32 bytes (1%) |           2 |
| `["sum", "uniform", "reduce", "basesize=128"]`      |   7.746 ms (5%) |           |  292.02 KiB (1%) |        5213 |
| `["sum", "uniform", "reduce", "basesize=256"]`      |   7.548 ms (5%) |           |  144.53 KiB (1%) |        2589 |
| `["sum", "uniform", "reduce", "basesize=512"]`      |   7.441 ms (5%) |           |   71.06 KiB (1%) |        1278 |
| `["sum", "valley", "foldl"]`                        |  14.185 ms (5%) |           |    32 bytes (1%) |           2 |
| `["sum", "valley", "reduce", "basesize=128"]`       |   8.050 ms (5%) |           |  292.02 KiB (1%) |        5213 |
| `["sum", "valley", "reduce", "basesize=256"]`       |   7.847 ms (5%) |           |  144.53 KiB (1%) |        2589 |
| `["sum", "valley", "reduce", "basesize=512"]`       |   7.724 ms (5%) |           |   71.06 KiB (1%) |        1278 |
| `["words", "nthreads=1"]`                           |  23.500 ms (5%) |           |   31.57 MiB (1%) |     1028318 |
| `["words", "nthreads=2"]`                           |  25.594 ms (5%) |           |   31.93 MiB (1%) |     1028387 |
| `["words", "nthreads=4"]`                           |  26.912 ms (5%) |           |   32.83 MiB (1%) |     1028678 |

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
       #1  2800 MHz      49482 s          0 s       1728 s      46464 s          0 s
       #2  2800 MHz      48329 s          0 s       1671 s      48917 s          0 s
       
  Memory: 7.790031433105469 GB (5804.01171875 MB free)
  Uptime: 996.0 sec
  Load Avg:  1.6728515625  1.44287109375  0.8291015625
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-9.0.1 (ORCJIT, cascadelake)
```

---
# Baseline result
# Benchmark Report for */home/travis/build/JuliaFolds/Transducers.jl*

## Job Properties
* Time of benchmark: 5 Sep 2020 - 1:50
* Package commit: ff5762
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
| `["collect", "assoc", "basesize=1"]`                | 308.908 ms (5%) | 14.089 ms |   82.16 MiB (1%) |     1368085 |
| `["collect", "assoc", "basesize=1024"]`             | 179.842 ms (5%) |           |    1.83 MiB (1%) |        1597 |
| `["collect", "assoc", "basesize=32"]`               | 183.907 ms (5%) |           |    5.47 MiB (1%) |       47069 |
| `["collect", "seq"]`                                | 349.915 ms (5%) |           |  512.72 KiB (1%) |          15 |
| `["collect", "unordered", "basesize=1"]`            | 351.148 ms (5%) |           |   30.01 MiB (1%) |      360622 |
| `["collect", "unordered", "basesize=1024"]`         | 210.411 ms (5%) |           |  816.70 KiB (1%) |        2856 |
| `["collect", "unordered", "basesize=32"]`           | 200.109 ms (5%) |           |    1.51 MiB (1%) |       13666 |
| `["findfirst", "n=1000", "foldl"]`                  | 554.744 ms (5%) |           |                  |             |
| `["findfirst", "n=1000", "reduce", "basesize=128"]` | 299.990 ms (5%) |           |  546.34 KiB (1%) |        9562 |
| `["findfirst", "n=1000", "reduce", "basesize=256"]` | 298.748 ms (5%) |           |  278.25 KiB (1%) |        4888 |
| `["findfirst", "n=1000", "reduce", "basesize=512"]` | 304.000 ms (5%) |           |  144.66 KiB (1%) |        2550 |
| `["findfirst", "n=400", "foldl"]`                   | 416.161 ms (5%) |           |                  |             |
| `["findfirst", "n=400", "reduce", "basesize=128"]`  | 227.046 ms (5%) |           | 1012.86 KiB (1%) |       17725 |
| `["findfirst", "n=400", "reduce", "basesize=256"]`  | 224.960 ms (5%) |           |  509.66 KiB (1%) |        8953 |
| `["findfirst", "n=400", "reduce", "basesize=512"]`  | 226.336 ms (5%) |           |  258.84 KiB (1%) |        4564 |
| `["findfirst", "n=500", "foldl"]`                   |  72.096 ms (5%) |           |                  |             |
| `["findfirst", "n=500", "reduce", "basesize=128"]`  |  39.585 ms (5%) |           |  152.59 KiB (1%) |        2677 |
| `["findfirst", "n=500", "reduce", "basesize=256"]`  |  39.357 ms (5%) |           |   82.00 KiB (1%) |        1444 |
| `["findfirst", "n=500", "reduce", "basesize=512"]`  |  41.901 ms (5%) |           |   46.84 KiB (1%) |         828 |
| `["overhead", "default"]`                           | 193.472 μs (5%) |           |  140.75 KiB (1%) |        2465 |
| `["overhead", "stoppable=false"]`                   | 195.355 μs (5%) |           |  140.78 KiB (1%) |        2465 |
| `["overhead", "stoppable=true"]`                    | 370.586 μs (5%) |           |  140.78 KiB (1%) |        2465 |
| `["parallel_histogram", "assoc", "basesize=16384"]` |   4.859 ms (5%) |           |  731.81 KiB (1%) |          94 |
| `["parallel_histogram", "assoc", "basesize=4096"]`  |   5.700 ms (5%) |           |    1.80 MiB (1%) |         448 |
| `["parallel_histogram", "assoc", "basesize=8192"]`  |   5.296 ms (5%) |           |    1.43 MiB (1%) |         220 |
| `["parallel_histogram", "comm", "basesize=16384"]`  |  12.800 ms (5%) |           |    1.26 MiB (1%) |        1469 |
| `["parallel_histogram", "comm", "basesize=4096"]`   |  15.868 ms (5%) |           |    1.44 MiB (1%) |        7194 |
| `["parallel_histogram", "comm", "basesize=8192"]`   |  14.466 ms (5%) |           |    1.33 MiB (1%) |        3656 |
| `["parallel_histogram", "seq"]`                     |   7.477 ms (5%) |           |  364.61 KiB (1%) |          24 |
| `["sum", "random", "foldl"]`                        |  14.003 ms (5%) |           |    32 bytes (1%) |           2 |
| `["sum", "random", "reduce", "basesize=128"]`       |   7.985 ms (5%) |           |  292.02 KiB (1%) |        5213 |
| `["sum", "random", "reduce", "basesize=256"]`       |   7.752 ms (5%) |           |  144.53 KiB (1%) |        2589 |
| `["sum", "random", "reduce", "basesize=512"]`       |   7.652 ms (5%) |           |   71.11 KiB (1%) |        1279 |
| `["sum", "uniform", "foldl"]`                       |  13.729 ms (5%) |           |    32 bytes (1%) |           2 |
| `["sum", "uniform", "reduce", "basesize=128"]`      |   7.744 ms (5%) |           |  292.02 KiB (1%) |        5213 |
| `["sum", "uniform", "reduce", "basesize=256"]`      |   7.555 ms (5%) |           |  144.53 KiB (1%) |        2589 |
| `["sum", "uniform", "reduce", "basesize=512"]`      |   7.439 ms (5%) |           |   71.06 KiB (1%) |        1278 |
| `["sum", "valley", "foldl"]`                        |  14.116 ms (5%) |           |    32 bytes (1%) |           2 |
| `["sum", "valley", "reduce", "basesize=128"]`       |   8.067 ms (5%) |           |  292.02 KiB (1%) |        5213 |
| `["sum", "valley", "reduce", "basesize=256"]`       |   7.845 ms (5%) |           |  144.53 KiB (1%) |        2589 |
| `["sum", "valley", "reduce", "basesize=512"]`       |   7.744 ms (5%) |           |   71.06 KiB (1%) |        1278 |
| `["words", "nthreads=1"]`                           |  23.747 ms (5%) |           |   31.67 MiB (1%) |     1032017 |
| `["words", "nthreads=2"]`                           |  25.855 ms (5%) |           |   32.39 MiB (1%) |     1032178 |
| `["words", "nthreads=4"]`                           |  26.647 ms (5%) |           |   32.84 MiB (1%) |     1032363 |

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
       #1  2800 MHz      70645 s          0 s       2220 s      66493 s          0 s
       #2  2800 MHz      74228 s          0 s       2238 s      64280 s          0 s
       
  Memory: 7.790031433105469 GB (5823.203125 MB free)
  Uptime: 1414.0 sec
  Load Avg:  1.7275390625  1.388671875  0.97802734375
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
    CPU MHz:               2800.220
    BogoMIPS:              5600.44
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

