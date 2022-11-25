# Multi-thread benchmark result

* Pull request commit: [`2d55cffdb622911e54afbbeb31b4973850d29346`](https://github.com/JuliaFolds/Transducers.jl/commit/2d55cffdb622911e54afbbeb31b4973850d29346)
* Pull request: <https://github.com/JuliaFolds/Transducers.jl/pull/536> (Update for v1.9 compatability)

# Judge result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmarks:
    - Target: 25 Nov 2022 - 17:52
    - Baseline: 25 Nov 2022 - 17:57
* Package commits:
    - Target: bc9f5b
    - Baseline: 958213
* Julia commits:
    - Target: 742b9a
    - Baseline: 742b9a
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
| `["findfirst", "n=1000", "reduce", "basesize=128"]` | 0.61 (5%) :white_check_mark: | 0.64 (1%) :white_check_mark: |
| `["findfirst", "n=1000", "reduce", "basesize=256"]` | 0.75 (5%) :white_check_mark: | 0.87 (1%) :white_check_mark: |
| `["findfirst", "n=400", "reduce", "basesize=128"]`  |                   1.01 (5%)  |                1.04 (1%) :x: |
| `["findfirst", "n=400", "reduce", "basesize=512"]`  | 0.81 (5%) :white_check_mark: | 0.82 (1%) :white_check_mark: |
| `["findfirst", "n=500", "reduce", "basesize=128"]`  | 0.77 (5%) :white_check_mark: | 0.89 (1%) :white_check_mark: |
| `["findfirst", "n=500", "reduce", "basesize=256"]`  |                1.16 (5%) :x: |                1.13 (1%) :x: |
| `["findfirst", "n=500", "reduce", "basesize=512"]`  | 0.47 (5%) :white_check_mark: | 0.63 (1%) :white_check_mark: |
| `["overhead", "default"]`                           | 0.95 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["overhead", "stoppable=false"]`                   |                1.07 (5%) :x: |                   1.00 (1%)  |
| `["partition_length_maximum", "rand", "reduce"]`    |                   1.00 (5%)  | 0.96 (1%) :white_check_mark: |
| `["words", "nthreads=2"]`                           |                1.16 (5%) :x: |                1.01 (1%) :x: |
| `["words", "nthreads=4"]`                           |                1.10 (5%) :x: |                   1.00 (1%)  |

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
- `["partition_length_maximum", "rand"]`
- `["splitby", "count"]`
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
Julia Version 1.7.3
Commit 742b9abb4d (2022-05-06 12:58 UTC)
Platform Info:
  OS: Linux (x86_64-pc-linux-gnu)
      Ubuntu 22.04.1 LTS
  uname: Linux 5.15.0-1023-azure #29-Ubuntu SMP Wed Oct 19 22:37:08 UTC 2022 x86_64 x86_64
  CPU: Intel(R) Xeon(R) Platinum 8370C CPU @ 2.80GHz: 
              speed         user         nice          sys         idle          irq
       #1  2793 MHz       5317 s          0 s        201 s       1318 s          0 s
       #2  2793 MHz       5025 s          0 s        206 s       1596 s          0 s
       
  Memory: 6.781219482421875 GB (3674.0625 MB free)
  Uptime: 688.23 sec
  Load Avg:  1.55  1.47  0.91
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-12.0.1 (ORCJIT, icelake-server)
```

### Baseline
```
Julia Version 1.7.3
Commit 742b9abb4d (2022-05-06 12:58 UTC)
Platform Info:
  OS: Linux (x86_64-pc-linux-gnu)
      Ubuntu 22.04.1 LTS
  uname: Linux 5.15.0-1023-azure #29-Ubuntu SMP Wed Oct 19 22:37:08 UTC 2022 x86_64 x86_64
  CPU: Intel(R) Xeon(R) Platinum 8370C CPU @ 2.80GHz: 
              speed         user         nice          sys         idle          irq
       #1  2793 MHz       7915 s          0 s        234 s       1598 s          0 s
       #2  2793 MHz       6989 s          0 s        241 s       2505 s          0 s
       
  Memory: 6.781219482421875 GB (3818.58203125 MB free)
  Uptime: 979.57 sec
  Load Avg:  1.67  1.58  1.11
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-12.0.1 (ORCJIT, icelake-server)
```

---
# Target result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmark: 25 Nov 2022 - 17:52
* Package commit: bc9f5b
* Julia commit: 742b9a
* Julia command flags: None
* Environment variables: `JULIA_NUM_THREADS => 2`

## Results
Below is a table of this job's results, obtained by running the benchmarks.
The values listed in the `ID` column have the structure `[parent_group, child_group, ..., key]`, and can be used to
index into the BaseBenchmarks suite to retrieve the corresponding benchmarks.
The percentages accompanying time and memory values in the below table are noise tolerances. The "true"
time/memory value for a given benchmark is expected to fall within this percentage of the reported value.
An empty cell means that the value was zero.

| ID                                                  | time            | GC time | memory          | allocations |
|-----------------------------------------------------|----------------:|--------:|----------------:|------------:|
| `["collect", "assoc", "basesize=1"]`                | 278.636 ms (5%) |         |  25.97 MiB (1%) |      306845 |
| `["collect", "assoc", "basesize=1024"]`             | 238.784 ms (5%) |         |   2.61 MiB (1%) |         455 |
| `["collect", "assoc", "basesize=32"]`               | 240.685 ms (5%) |         |   4.82 MiB (1%) |       11710 |
| `["collect", "seq"]`                                | 477.676 ms (5%) |         | 812.73 KiB (1%) |          11 |
| `["collect", "unordered", "basesize=1"]`            | 368.398 ms (5%) |         |  23.91 MiB (1%) |      413334 |
| `["collect", "unordered", "basesize=1024"]`         | 249.533 ms (5%) |         |   1.01 MiB (1%) |         963 |
| `["collect", "unordered", "basesize=32"]`           | 260.224 ms (5%) |         |   1.59 MiB (1%) |       15036 |
| `["findfirst", "n=1000", "foldl"]`                  | 735.868 ms (5%) |         |                 |             |
| `["findfirst", "n=1000", "reduce", "basesize=128"]` | 403.515 ms (5%) |         | 232.86 KiB (1%) |        3276 |
| `["findfirst", "n=1000", "reduce", "basesize=256"]` | 496.662 ms (5%) |         | 157.20 KiB (1%) |        2193 |
| `["findfirst", "n=1000", "reduce", "basesize=512"]` | 503.217 ms (5%) |         |  81.33 KiB (1%) |        1146 |
| `["findfirst", "n=400", "foldl"]`                   | 551.765 ms (5%) |         |                 |             |
| `["findfirst", "n=400", "reduce", "basesize=128"]`  | 292.299 ms (5%) |         | 394.34 KiB (1%) |        5599 |
| `["findfirst", "n=400", "reduce", "basesize=256"]`  | 288.759 ms (5%) |         | 200.39 KiB (1%) |        2873 |
| `["findfirst", "n=400", "reduce", "basesize=512"]`  | 324.821 ms (5%) |         | 112.62 KiB (1%) |        1623 |
| `["findfirst", "n=500", "foldl"]`                   |  95.634 ms (5%) |         |                 |             |
| `["findfirst", "n=500", "reduce", "basesize=128"]`  | 175.968 ms (5%) |         | 231.34 KiB (1%) |        3165 |
| `["findfirst", "n=500", "reduce", "basesize=256"]`  | 273.605 ms (5%) |         | 167.88 KiB (1%) |        2371 |
| `["findfirst", "n=500", "reduce", "basesize=512"]`  | 143.126 ms (5%) |         |  63.67 KiB (1%) |         866 |
| `["overhead", "default"]`                           |  67.600 μs (5%) |         |  32.73 KiB (1%) |         418 |
| `["overhead", "stoppable=false"]`                   |  70.100 μs (5%) |         |  32.75 KiB (1%) |         418 |
| `["overhead", "stoppable=true"]`                    |  78.799 μs (5%) |         |  44.22 KiB (1%) |         609 |
| `["parallel_histogram", "assoc", "basesize=16384"]` |   3.721 ms (5%) |         | 728.91 KiB (1%) |          57 |
| `["parallel_histogram", "assoc", "basesize=4096"]`  |   4.483 ms (5%) |         |   1.79 MiB (1%) |         216 |
| `["parallel_histogram", "assoc", "basesize=8192"]`  |   4.107 ms (5%) |         |   1.42 MiB (1%) |         117 |
| `["parallel_histogram", "comm", "basesize=16384"]`  |  13.750 ms (5%) |         |   1.64 MiB (1%) |        4327 |
| `["parallel_histogram", "comm", "basesize=4096"]`   |  23.789 ms (5%) |         |   1.39 MiB (1%) |       11609 |
| `["parallel_histogram", "comm", "basesize=8192"]`   |  20.345 ms (5%) |         |   1.36 MiB (1%) |        8362 |
| `["parallel_histogram", "seq"]`                     |   6.657 ms (5%) |         | 364.16 KiB (1%) |          24 |
| `["partition_length_maximum", "rand", "foldl"]`     |  41.182 ms (5%) |         |                 |             |
| `["partition_length_maximum", "rand", "reduce"]`    |  20.578 ms (5%) |         |  704 bytes (1%) |          10 |
| `["splitby", "count", "foldl"]`                     |   2.288 ms (5%) |         |                 |             |
| `["splitby", "count", "man"]`                       |   1.527 ms (5%) |         |                 |             |
| `["splitby", "count", "reduce"]`                    |   1.151 ms (5%) |         |   1.06 KiB (1%) |          18 |
| `["sum", "random", "foldl"]`                        |  17.915 ms (5%) |         |                 |             |
| `["sum", "random", "reduce", "basesize=128"]`       |   9.140 ms (5%) |         |  74.14 KiB (1%) |        1103 |
| `["sum", "random", "reduce", "basesize=256"]`       |   9.059 ms (5%) |         |  36.67 KiB (1%) |         544 |
| `["sum", "random", "reduce", "basesize=512"]`       |   9.008 ms (5%) |         |  18.08 KiB (1%) |         269 |
| `["sum", "uniform", "foldl"]`                       |  17.724 ms (5%) |         |                 |             |
| `["sum", "uniform", "reduce", "basesize=128"]`      |   9.024 ms (5%) |         |  74.20 KiB (1%) |        1105 |
| `["sum", "uniform", "reduce", "basesize=256"]`      |   8.949 ms (5%) |         |  36.77 KiB (1%) |         547 |
| `["sum", "uniform", "reduce", "basesize=512"]`      |   8.901 ms (5%) |         |  18.03 KiB (1%) |         268 |
| `["sum", "valley", "foldl"]`                        |  18.137 ms (5%) |         |                 |             |
| `["sum", "valley", "reduce", "basesize=128"]`       |   9.260 ms (5%) |         |  74.08 KiB (1%) |        1101 |
| `["sum", "valley", "reduce", "basesize=256"]`       |   9.187 ms (5%) |         |  36.70 KiB (1%) |         545 |
| `["sum", "valley", "reduce", "basesize=512"]`       |   9.205 ms (5%) |         |  18.00 KiB (1%) |         267 |
| `["words", "nthreads=1"]`                           |  18.277 ms (5%) |         |  31.78 MiB (1%) |     1035525 |
| `["words", "nthreads=2"]`                           |  13.633 ms (5%) |         |  32.50 MiB (1%) |     1035598 |
| `["words", "nthreads=4"]`                           |  13.789 ms (5%) |         |  32.94 MiB (1%) |     1035669 |

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
- `["partition_length_maximum", "rand"]`
- `["splitby", "count"]`
- `["sum", "random"]`
- `["sum", "random", "reduce"]`
- `["sum", "uniform"]`
- `["sum", "uniform", "reduce"]`
- `["sum", "valley"]`
- `["sum", "valley", "reduce"]`
- `["words"]`

## Julia versioninfo
```
Julia Version 1.7.3
Commit 742b9abb4d (2022-05-06 12:58 UTC)
Platform Info:
  OS: Linux (x86_64-pc-linux-gnu)
      Ubuntu 22.04.1 LTS
  uname: Linux 5.15.0-1023-azure #29-Ubuntu SMP Wed Oct 19 22:37:08 UTC 2022 x86_64 x86_64
  CPU: Intel(R) Xeon(R) Platinum 8370C CPU @ 2.80GHz: 
              speed         user         nice          sys         idle          irq
       #1  2793 MHz       5317 s          0 s        201 s       1318 s          0 s
       #2  2793 MHz       5025 s          0 s        206 s       1596 s          0 s
       
  Memory: 6.781219482421875 GB (3674.0625 MB free)
  Uptime: 688.23 sec
  Load Avg:  1.55  1.47  0.91
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-12.0.1 (ORCJIT, icelake-server)
```

---
# Baseline result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmark: 25 Nov 2022 - 17:57
* Package commit: 958213
* Julia commit: 742b9a
* Julia command flags: None
* Environment variables: `JULIA_NUM_THREADS => 2`

## Results
Below is a table of this job's results, obtained by running the benchmarks.
The values listed in the `ID` column have the structure `[parent_group, child_group, ..., key]`, and can be used to
index into the BaseBenchmarks suite to retrieve the corresponding benchmarks.
The percentages accompanying time and memory values in the below table are noise tolerances. The "true"
time/memory value for a given benchmark is expected to fall within this percentage of the reported value.
An empty cell means that the value was zero.

| ID                                                  | time            | GC time | memory          | allocations |
|-----------------------------------------------------|----------------:|--------:|----------------:|------------:|
| `["collect", "assoc", "basesize=1"]`                | 277.889 ms (5%) |         |  25.97 MiB (1%) |      306852 |
| `["collect", "assoc", "basesize=1024"]`             | 238.773 ms (5%) |         |   2.61 MiB (1%) |         456 |
| `["collect", "assoc", "basesize=32"]`               | 240.442 ms (5%) |         |   4.82 MiB (1%) |       11713 |
| `["collect", "seq"]`                                | 477.645 ms (5%) |         | 812.73 KiB (1%) |          11 |
| `["collect", "unordered", "basesize=1"]`            | 365.997 ms (5%) |         |  23.93 MiB (1%) |      413856 |
| `["collect", "unordered", "basesize=1024"]`         | 250.053 ms (5%) |         |   1.01 MiB (1%) |        1023 |
| `["collect", "unordered", "basesize=32"]`           | 260.861 ms (5%) |         |   1.59 MiB (1%) |       14983 |
| `["findfirst", "n=1000", "foldl"]`                  | 736.474 ms (5%) |         |                 |             |
| `["findfirst", "n=1000", "reduce", "basesize=128"]` | 662.115 ms (5%) |         | 364.67 KiB (1%) |        5129 |
| `["findfirst", "n=1000", "reduce", "basesize=256"]` | 658.147 ms (5%) |         | 180.23 KiB (1%) |        2564 |
| `["findfirst", "n=1000", "reduce", "basesize=512"]` | 503.234 ms (5%) |         |  81.36 KiB (1%) |        1147 |
| `["findfirst", "n=400", "foldl"]`                   | 552.568 ms (5%) |         |                 |             |
| `["findfirst", "n=400", "reduce", "basesize=128"]`  | 288.284 ms (5%) |         | 378.22 KiB (1%) |        5392 |
| `["findfirst", "n=400", "reduce", "basesize=256"]`  | 290.376 ms (5%) |         | 200.86 KiB (1%) |        2873 |
| `["findfirst", "n=400", "reduce", "basesize=512"]`  | 398.772 ms (5%) |         | 138.08 KiB (1%) |        1988 |
| `["findfirst", "n=500", "foldl"]`                   |  95.773 ms (5%) |         |                 |             |
| `["findfirst", "n=500", "reduce", "basesize=128"]`  | 229.593 ms (5%) |         | 259.59 KiB (1%) |        3628 |
| `["findfirst", "n=500", "reduce", "basesize=256"]`  | 235.768 ms (5%) |         | 149.22 KiB (1%) |        2074 |
| `["findfirst", "n=500", "reduce", "basesize=512"]`  | 303.970 ms (5%) |         | 101.06 KiB (1%) |        1384 |
| `["overhead", "default"]`                           |  71.399 μs (5%) |         |  32.73 KiB (1%) |         418 |
| `["overhead", "stoppable=false"]`                   |  65.799 μs (5%) |         |  32.72 KiB (1%) |         417 |
| `["overhead", "stoppable=true"]`                    |  79.000 μs (5%) |         |  44.25 KiB (1%) |         610 |
| `["parallel_histogram", "assoc", "basesize=16384"]` |   3.743 ms (5%) |         | 728.91 KiB (1%) |          57 |
| `["parallel_histogram", "assoc", "basesize=4096"]`  |   4.524 ms (5%) |         |   1.79 MiB (1%) |         216 |
| `["parallel_histogram", "assoc", "basesize=8192"]`  |   4.131 ms (5%) |         |   1.42 MiB (1%) |         117 |
| `["parallel_histogram", "comm", "basesize=16384"]`  |  14.379 ms (5%) |         |   1.64 MiB (1%) |        4508 |
| `["parallel_histogram", "comm", "basesize=4096"]`   |  23.282 ms (5%) |         |   1.39 MiB (1%) |       11594 |
| `["parallel_histogram", "comm", "basesize=8192"]`   |  20.224 ms (5%) |         |   1.37 MiB (1%) |        9498 |
| `["parallel_histogram", "seq"]`                     |   6.681 ms (5%) |         | 364.16 KiB (1%) |          24 |
| `["partition_length_maximum", "rand", "foldl"]`     |  41.110 ms (5%) |         |                 |             |
| `["partition_length_maximum", "rand", "reduce"]`    |  20.573 ms (5%) |         |  736 bytes (1%) |          11 |
| `["splitby", "count", "foldl"]`                     |   2.305 ms (5%) |         |                 |             |
| `["splitby", "count", "man"]`                       |   1.527 ms (5%) |         |                 |             |
| `["splitby", "count", "reduce"]`                    |   1.097 ms (5%) |         |   1.06 KiB (1%) |          18 |
| `["sum", "random", "foldl"]`                        |  17.998 ms (5%) |         |                 |             |
| `["sum", "random", "reduce", "basesize=128"]`       |   9.196 ms (5%) |         |  74.14 KiB (1%) |        1103 |
| `["sum", "random", "reduce", "basesize=256"]`       |   9.105 ms (5%) |         |  36.73 KiB (1%) |         546 |
| `["sum", "random", "reduce", "basesize=512"]`       |   9.060 ms (5%) |         |  18.14 KiB (1%) |         271 |
| `["sum", "uniform", "foldl"]`                       |  17.720 ms (5%) |         |                 |             |
| `["sum", "uniform", "reduce", "basesize=128"]`      |   9.050 ms (5%) |         |  74.14 KiB (1%) |        1103 |
| `["sum", "uniform", "reduce", "basesize=256"]`      |   8.961 ms (5%) |         |  36.73 KiB (1%) |         546 |
| `["sum", "uniform", "reduce", "basesize=512"]`      |   8.908 ms (5%) |         |  18.03 KiB (1%) |         268 |
| `["sum", "valley", "foldl"]`                        |  18.133 ms (5%) |         |                 |             |
| `["sum", "valley", "reduce", "basesize=128"]`       |   9.264 ms (5%) |         |  74.17 KiB (1%) |        1104 |
| `["sum", "valley", "reduce", "basesize=256"]`       |   9.168 ms (5%) |         |  36.70 KiB (1%) |         545 |
| `["sum", "valley", "reduce", "basesize=512"]`       |   9.148 ms (5%) |         |  18.00 KiB (1%) |         267 |
| `["words", "nthreads=1"]`                           |  18.103 ms (5%) |         |  31.75 MiB (1%) |     1034310 |
| `["words", "nthreads=2"]`                           |  11.729 ms (5%) |         |  32.10 MiB (1%) |     1034354 |
| `["words", "nthreads=4"]`                           |  12.493 ms (5%) |         |  33.00 MiB (1%) |     1034530 |

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
- `["partition_length_maximum", "rand"]`
- `["splitby", "count"]`
- `["sum", "random"]`
- `["sum", "random", "reduce"]`
- `["sum", "uniform"]`
- `["sum", "uniform", "reduce"]`
- `["sum", "valley"]`
- `["sum", "valley", "reduce"]`
- `["words"]`

## Julia versioninfo
```
Julia Version 1.7.3
Commit 742b9abb4d (2022-05-06 12:58 UTC)
Platform Info:
  OS: Linux (x86_64-pc-linux-gnu)
      Ubuntu 22.04.1 LTS
  uname: Linux 5.15.0-1023-azure #29-Ubuntu SMP Wed Oct 19 22:37:08 UTC 2022 x86_64 x86_64
  CPU: Intel(R) Xeon(R) Platinum 8370C CPU @ 2.80GHz: 
              speed         user         nice          sys         idle          irq
       #1  2793 MHz       7915 s          0 s        234 s       1598 s          0 s
       #2  2793 MHz       6989 s          0 s        241 s       2505 s          0 s
       
  Memory: 6.781219482421875 GB (3818.58203125 MB free)
  Uptime: 979.57 sec
  Load Avg:  1.67  1.58  1.11
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-12.0.1 (ORCJIT, icelake-server)
```

---
# Runtime information
| Runtime Info | |
|:--|:--|
| BLAS #threads | 2 |
| `BLAS.vendor()` | `openblas64` |
| `Sys.CPU_THREADS` | 2 |

`lscpu` output:

    Architecture:                    x86_64
    CPU op-mode(s):                  32-bit, 64-bit
    Address sizes:                   46 bits physical, 48 bits virtual
    Byte Order:                      Little Endian
    CPU(s):                          2
    On-line CPU(s) list:             0,1
    Vendor ID:                       GenuineIntel
    Model name:                      Intel(R) Xeon(R) Platinum 8370C CPU @ 2.80GHz
    CPU family:                      6
    Model:                           106
    Thread(s) per core:              1
    Core(s) per socket:              2
    Socket(s):                       1
    Stepping:                        6
    BogoMIPS:                        5586.87
    Flags:                           fpu vme de pse tsc msr pae mce cx8 apic sep mtrr pge mca cmov pat pse36 clflush mmx fxsr sse sse2 ss ht syscall nx pdpe1gb rdtscp lm constant_tsc rep_good nopl xtopology cpuid pni pclmulqdq ssse3 fma cx16 pcid sse4_1 sse4_2 movbe popcnt aes xsave avx f16c rdrand hypervisor lahf_lm abm 3dnowprefetch invpcid_single pti fsgsbase bmi1 hle avx2 smep bmi2 erms invpcid rtm avx512f avx512dq rdseed adx smap clflushopt avx512cd avx512bw avx512vl xsaveopt xsavec xsaves md_clear
    Hypervisor vendor:               Microsoft
    Virtualization type:             full
    L1d cache:                       96 KiB (2 instances)
    L1i cache:                       64 KiB (2 instances)
    L2 cache:                        2.5 MiB (2 instances)
    L3 cache:                        48 MiB (1 instance)
    NUMA node(s):                    1
    NUMA node0 CPU(s):               0,1
    Vulnerability Itlb multihit:     KVM: Mitigation: VMX unsupported
    Vulnerability L1tf:              Mitigation; PTE Inversion
    Vulnerability Mds:               Mitigation; Clear CPU buffers; SMT Host state unknown
    Vulnerability Meltdown:          Mitigation; PTI
    Vulnerability Mmio stale data:   Vulnerable: Clear CPU buffers attempted, no microcode; SMT Host state unknown
    Vulnerability Retbleed:          Not affected
    Vulnerability Spec store bypass: Vulnerable
    Vulnerability Spectre v1:        Mitigation; usercopy/swapgs barriers and __user pointer sanitization
    Vulnerability Spectre v2:        Mitigation; Retpolines, STIBP disabled, RSB filling, PBRSB-eIBRS Not affected
    Vulnerability Srbds:             Not affected
    Vulnerability Tsx async abort:   Mitigation; Clear CPU buffers; SMT Host state unknown
    

| Cpu Property       | Value                                                   |
|:------------------ |:------------------------------------------------------- |
| Brand              | Intel(R) Xeon(R) Platinum 8370C CPU @ 2.80GHz           |
| Vendor             | :Intel                                                  |
| Architecture       | :UnknownIntel                                           |
| Model              | Family: 0x06, Model: 0x6a, Stepping: 0x06, Type: 0x00   |
| Cores              | 2 physical cores, 2 logical cores (on executing CPU)    |
|                    | No Hyperthreading hardware capability detected          |
| Clock Frequencies  | Not supported by CPU                                    |
| Data Cache         | Level 1:3 : (48, 1280, 49152) kbytes                    |
|                    | 64 byte cache line size                                 |
| Address Size       | 48 bits virtual, 46 bits physical                       |
| SIMD               | 512 bit = 64 byte max. SIMD vector size                 |
| Time Stamp Counter | TSC is accessible via `rdtsc`                           |
|                    | TSC increased at every clock cycle (non-invariant TSC)  |
| Perf. Monitoring   | Performance Monitoring Counters (PMC) are not supported |
| Hypervisor         | Yes, Microsoft                                          |

