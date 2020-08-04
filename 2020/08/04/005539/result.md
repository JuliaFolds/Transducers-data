# Multi-thread benchmark result

* Pull request commit: [`274ec9ca2d88e5d67749db656914332435c56424`](https://github.com/JuliaFolds/Transducers.jl/commit/274ec9ca2d88e5d67749db656914332435c56424)
* Pull request: <https://github.com/JuliaFolds/Transducers.jl/pull/243> (Update */Manifest.toml)

# Judge result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmarks:
    - Target: 4 Aug 2020 - 00:50
    - Baseline: 4 Aug 2020 - 00:55
* Package commits:
    - Target: cd0af5
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
| `["collect", "assoc", "basesize=1"]`                | 0.90 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["collect", "unordered", "basesize=1024"]`         | 0.78 (5%) :white_check_mark: | 0.88 (1%) :white_check_mark: |
| `["findfirst", "n=1000", "foldl"]`                  | 0.84 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["findfirst", "n=500", "reduce", "basesize=512"]`  |                1.20 (5%) :x: |                   1.00 (1%)  |
| `["parallel_histogram", "comm", "basesize=16384"]`  |                1.10 (5%) :x: |                   1.00 (1%)  |
| `["parallel_histogram", "comm", "basesize=4096"]`   |                   0.99 (5%)  | 0.98 (1%) :white_check_mark: |
| `["parallel_histogram", "comm", "basesize=8192"]`   |                   0.99 (5%)  | 0.98 (1%) :white_check_mark: |
| `["parallel_histogram", "seq"]`                     |                1.14 (5%) :x: |                   1.00 (1%)  |
| `["sum", "random", "reduce", "basesize=128"]`       |                1.06 (5%) :x: |                   1.00 (1%)  |
| `["words", "nthreads=1"]`                           |                1.19 (5%) :x: |                   1.00 (1%)  |
| `["words", "nthreads=2"]`                           | 0.90 (5%) :white_check_mark: | 0.99 (1%) :white_check_mark: |

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
       #1  2095 MHz      50060 s          0 s       2137 s      14129 s          0 s
       #2  2095 MHz      46606 s          0 s       2436 s      17752 s          0 s
       
  Memory: 6.7648773193359375 GB (2931.33203125 MB free)
  Uptime: 686.0 sec
  Load Avg:  1.63720703125  1.4990234375  0.8994140625
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
       #1  2095 MHz      76475 s          0 s       2756 s      18271 s          0 s
       #2  2095 MHz      67025 s          0 s       3105 s      27856 s          0 s
       
  Memory: 6.7648773193359375 GB (2935.51171875 MB free)
  Uptime: 1000.0 sec
  Load Avg:  1.54931640625  1.515625  1.07763671875
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-8.0.1 (ORCJIT, skylake)
```

---
# Target result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmark: 4 Aug 2020 - 0:50
* Package commit: cd0af5
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
| `["collect", "assoc", "basesize=1"]`                | 295.435 ms (5%) | 10.750 ms |  87.55 MiB (1%) |     1590811 |
| `["collect", "assoc", "basesize=1024"]`             | 179.866 ms (5%) |           |   1.84 MiB (1%) |        1811 |
| `["collect", "assoc", "basesize=32"]`               | 189.910 ms (5%) |           |   5.64 MiB (1%) |       54012 |
| `["collect", "seq"]`                                | 362.307 ms (5%) |           |   1.50 MiB (1%) |       32784 |
| `["collect", "unordered", "basesize=1"]`            | 391.290 ms (5%) | 16.485 ms |  29.14 MiB (1%) |      402066 |
| `["collect", "unordered", "basesize=1024"]`         | 232.855 ms (5%) |           | 807.38 KiB (1%) |        4764 |
| `["collect", "unordered", "basesize=32"]`           | 213.027 ms (5%) |           |   1.46 MiB (1%) |       16281 |
| `["findfirst", "n=1000", "foldl"]`                  | 573.736 ms (5%) |           |                 |             |
| `["findfirst", "n=1000", "reduce", "basesize=128"]` | 348.637 ms (5%) |           | 563.69 KiB (1%) |       10203 |
| `["findfirst", "n=1000", "reduce", "basesize=256"]` | 340.536 ms (5%) |           | 287.16 KiB (1%) |        5216 |
| `["findfirst", "n=1000", "reduce", "basesize=512"]` | 345.442 ms (5%) |           | 149.34 KiB (1%) |        2723 |
| `["findfirst", "n=400", "foldl"]`                   | 421.398 ms (5%) |           |                 |             |
| `["findfirst", "n=400", "reduce", "basesize=128"]`  | 219.324 ms (5%) |           |   1.02 MiB (1%) |       18841 |
| `["findfirst", "n=400", "reduce", "basesize=256"]`  | 214.846 ms (5%) |           | 525.31 KiB (1%) |        9516 |
| `["findfirst", "n=400", "reduce", "basesize=512"]`  | 216.647 ms (5%) |           | 266.89 KiB (1%) |        4854 |
| `["findfirst", "n=500", "foldl"]`                   |  85.437 ms (5%) |           |                 |             |
| `["findfirst", "n=500", "reduce", "basesize=128"]`  |  37.688 ms (5%) |           | 157.25 KiB (1%) |        2841 |
| `["findfirst", "n=500", "reduce", "basesize=256"]`  |  37.293 ms (5%) |           |  84.50 KiB (1%) |        1530 |
| `["findfirst", "n=500", "reduce", "basesize=512"]`  |  47.928 ms (5%) |           |  48.31 KiB (1%) |         879 |
| `["overhead", "default"]`                           | 156.308 μs (5%) |           | 146.27 KiB (1%) |        2633 |
| `["overhead", "stoppable=false"]`                   | 153.008 μs (5%) |           | 146.30 KiB (1%) |        2634 |
| `["overhead", "stoppable=true"]`                    | 277.313 μs (5%) |           | 146.53 KiB (1%) |        2649 |
| `["parallel_histogram", "assoc", "basesize=16384"]` |   3.691 ms (5%) |           | 732.06 KiB (1%) |         103 |
| `["parallel_histogram", "assoc", "basesize=4096"]`  |   4.195 ms (5%) |           |   1.80 MiB (1%) |         498 |
| `["parallel_histogram", "assoc", "basesize=8192"]`  |   3.944 ms (5%) |           |   1.43 MiB (1%) |         242 |
| `["parallel_histogram", "comm", "basesize=16384"]`  |  14.185 ms (5%) |           |   1.22 MiB (1%) |         327 |
| `["parallel_histogram", "comm", "basesize=4096"]`   |  22.070 ms (5%) |           |   1.04 MiB (1%) |        4736 |
| `["parallel_histogram", "comm", "basesize=8192"]`   |  17.552 ms (5%) |           |   1.23 MiB (1%) |        1014 |
| `["parallel_histogram", "seq"]`                     |   7.663 ms (5%) |           | 364.61 KiB (1%) |          24 |
| `["sum", "random", "foldl"]`                        |  13.865 ms (5%) |           |   64 bytes (1%) |           3 |
| `["sum", "random", "reduce", "basesize=128"]`       |   7.370 ms (5%) |           | 313.38 KiB (1%) |        6068 |
| `["sum", "random", "reduce", "basesize=256"]`       |   7.151 ms (5%) |           | 155.17 KiB (1%) |        3014 |
| `["sum", "random", "reduce", "basesize=512"]`       |   7.032 ms (5%) |           |  76.33 KiB (1%) |        1487 |
| `["sum", "uniform", "foldl"]`                       |  13.327 ms (5%) |           |   64 bytes (1%) |           3 |
| `["sum", "uniform", "reduce", "basesize=128"]`      |   6.789 ms (5%) |           | 313.42 KiB (1%) |        6071 |
| `["sum", "uniform", "reduce", "basesize=256"]`      |   6.658 ms (5%) |           | 155.16 KiB (1%) |        3013 |
| `["sum", "uniform", "reduce", "basesize=512"]`      |   6.836 ms (5%) |           |  76.31 KiB (1%) |        1486 |
| `["sum", "valley", "foldl"]`                        |  13.613 ms (5%) |           |   64 bytes (1%) |           3 |
| `["sum", "valley", "reduce", "basesize=128"]`       |   6.990 ms (5%) |           | 313.34 KiB (1%) |        6066 |
| `["sum", "valley", "reduce", "basesize=256"]`       |   6.841 ms (5%) |           | 155.16 KiB (1%) |        3013 |
| `["sum", "valley", "reduce", "basesize=512"]`       |   6.762 ms (5%) |           |  76.33 KiB (1%) |        1487 |
| `["words", "nthreads=1"]`                           |  43.864 ms (5%) |  6.900 ms |  63.00 MiB (1%) |     2058572 |
| `["words", "nthreads=2"]`                           |  20.334 ms (5%) |           |  63.61 MiB (1%) |     2066751 |
| `["words", "nthreads=4"]`                           |  23.401 ms (5%) |           |  64.88 MiB (1%) |     2079275 |

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
       #1  2095 MHz      50060 s          0 s       2137 s      14129 s          0 s
       #2  2095 MHz      46606 s          0 s       2436 s      17752 s          0 s
       
  Memory: 6.7648773193359375 GB (2931.33203125 MB free)
  Uptime: 686.0 sec
  Load Avg:  1.63720703125  1.4990234375  0.8994140625
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-8.0.1 (ORCJIT, skylake)
```

---
# Baseline result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmark: 4 Aug 2020 - 0:55
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
| `["collect", "assoc", "basesize=1"]`                | 329.087 ms (5%) | 12.318 ms |  87.55 MiB (1%) |     1590772 |
| `["collect", "assoc", "basesize=1024"]`             | 186.116 ms (5%) |           |   1.84 MiB (1%) |        1812 |
| `["collect", "assoc", "basesize=32"]`               | 186.827 ms (5%) |           |   5.64 MiB (1%) |       54025 |
| `["collect", "seq"]`                                | 364.987 ms (5%) |           |   1.50 MiB (1%) |       32784 |
| `["collect", "unordered", "basesize=1"]`            | 377.096 ms (5%) |           |  29.12 MiB (1%) |      400726 |
| `["collect", "unordered", "basesize=1024"]`         | 297.819 ms (5%) |           | 921.14 KiB (1%) |       12045 |
| `["collect", "unordered", "basesize=32"]`           | 208.157 ms (5%) |           |   1.46 MiB (1%) |       15931 |
| `["findfirst", "n=1000", "foldl"]`                  | 684.001 ms (5%) |           |                 |             |
| `["findfirst", "n=1000", "reduce", "basesize=128"]` | 353.446 ms (5%) |           | 563.80 KiB (1%) |       10210 |
| `["findfirst", "n=1000", "reduce", "basesize=256"]` | 352.400 ms (5%) |           | 287.16 KiB (1%) |        5216 |
| `["findfirst", "n=1000", "reduce", "basesize=512"]` | 356.529 ms (5%) |           | 149.22 KiB (1%) |        2715 |
| `["findfirst", "n=400", "foldl"]`                   | 424.698 ms (5%) |           |                 |             |
| `["findfirst", "n=400", "reduce", "basesize=128"]`  | 228.569 ms (5%) |           |   1.02 MiB (1%) |       18855 |
| `["findfirst", "n=400", "reduce", "basesize=256"]`  | 217.124 ms (5%) |           | 525.31 KiB (1%) |        9516 |
| `["findfirst", "n=400", "reduce", "basesize=512"]`  | 216.016 ms (5%) |           | 266.92 KiB (1%) |        4856 |
| `["findfirst", "n=500", "foldl"]`                   |  86.553 ms (5%) |           |                 |             |
| `["findfirst", "n=500", "reduce", "basesize=128"]`  |  37.860 ms (5%) |           | 157.23 KiB (1%) |        2840 |
| `["findfirst", "n=500", "reduce", "basesize=256"]`  |  37.256 ms (5%) |           |  84.50 KiB (1%) |        1530 |
| `["findfirst", "n=500", "reduce", "basesize=512"]`  |  39.794 ms (5%) |           |  48.30 KiB (1%) |         878 |
| `["overhead", "default"]`                           | 154.417 μs (5%) |           | 146.27 KiB (1%) |        2633 |
| `["overhead", "stoppable=false"]`                   | 157.917 μs (5%) |           | 146.30 KiB (1%) |        2634 |
| `["overhead", "stoppable=true"]`                    | 269.530 μs (5%) |           | 146.53 KiB (1%) |        2649 |
| `["parallel_histogram", "assoc", "basesize=16384"]` |   3.683 ms (5%) |           | 732.06 KiB (1%) |         103 |
| `["parallel_histogram", "assoc", "basesize=4096"]`  |   4.180 ms (5%) |           |   1.80 MiB (1%) |         497 |
| `["parallel_histogram", "assoc", "basesize=8192"]`  |   3.939 ms (5%) |           |   1.43 MiB (1%) |         242 |
| `["parallel_histogram", "comm", "basesize=16384"]`  |  12.925 ms (5%) |           |   1.22 MiB (1%) |         159 |
| `["parallel_histogram", "comm", "basesize=4096"]`   |  22.323 ms (5%) |           |   1.06 MiB (1%) |        6083 |
| `["parallel_histogram", "comm", "basesize=8192"]`   |  17.782 ms (5%) |           |   1.26 MiB (1%) |        2956 |
| `["parallel_histogram", "seq"]`                     |   6.727 ms (5%) |           | 364.61 KiB (1%) |          24 |
| `["sum", "random", "foldl"]`                        |  13.586 ms (5%) |           |   64 bytes (1%) |           3 |
| `["sum", "random", "reduce", "basesize=128"]`       |   6.963 ms (5%) |           | 313.41 KiB (1%) |        6070 |
| `["sum", "random", "reduce", "basesize=256"]`       |   6.826 ms (5%) |           | 155.17 KiB (1%) |        3014 |
| `["sum", "random", "reduce", "basesize=512"]`       |   6.722 ms (5%) |           |  76.31 KiB (1%) |        1486 |
| `["sum", "uniform", "foldl"]`                       |  13.162 ms (5%) |           |   64 bytes (1%) |           3 |
| `["sum", "uniform", "reduce", "basesize=128"]`      |   6.771 ms (5%) |           | 313.45 KiB (1%) |        6073 |
| `["sum", "uniform", "reduce", "basesize=256"]`      |   6.627 ms (5%) |           | 155.14 KiB (1%) |        3012 |
| `["sum", "uniform", "reduce", "basesize=512"]`      |   6.545 ms (5%) |           |  76.31 KiB (1%) |        1486 |
| `["sum", "valley", "foldl"]`                        |  14.005 ms (5%) |           |   64 bytes (1%) |           3 |
| `["sum", "valley", "reduce", "basesize=128"]`       |   7.055 ms (5%) |           | 313.34 KiB (1%) |        6066 |
| `["sum", "valley", "reduce", "basesize=256"]`       |   6.877 ms (5%) |           | 155.16 KiB (1%) |        3013 |
| `["sum", "valley", "reduce", "basesize=512"]`       |   6.762 ms (5%) |           |  76.34 KiB (1%) |        1488 |
| `["words", "nthreads=1"]`                           |  36.936 ms (5%) |  6.021 ms |  63.20 MiB (1%) |     2064885 |
| `["words", "nthreads=2"]`                           |  22.679 ms (5%) |           |  64.29 MiB (1%) |     2077169 |
| `["words", "nthreads=4"]`                           |  22.675 ms (5%) |           |  64.93 MiB (1%) |     2083451 |

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
       #1  2095 MHz      76475 s          0 s       2756 s      18271 s          0 s
       #2  2095 MHz      67025 s          0 s       3105 s      27856 s          0 s
       
  Memory: 6.7648773193359375 GB (2935.51171875 MB free)
  Uptime: 1000.0 sec
  Load Avg:  1.54931640625  1.515625  1.07763671875
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
    CPU MHz:             2095.207
    BogoMIPS:            4190.41
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

