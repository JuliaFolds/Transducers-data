# Multi-thread benchmark result

* Pull request commit: [`b715a813d82863fd84e17ce31a4a121c4323e8b4`](https://github.com/JuliaFolds/Transducers.jl/commit/b715a813d82863fd84e17ce31a4a121c4323e8b4)
* Pull request: <https://github.com/JuliaFolds/Transducers.jl/pull/243> (Update */Manifest.toml)

# Judge result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmarks:
    - Target: 6 Aug 2025 - 02:29
    - Baseline: 6 Aug 2025 - 02:34
* Package commits:
    - Target: aa8c6ab
    - Baseline: 2a51f8d
* Julia commits:
    - Target: 742b9ab
    - Baseline: 742b9ab
* Julia command flags:
    - Target: None
    - Baseline: None
* Environment variables:
    - Target: `JULIA_NUM_THREADS => 2`
    - Baseline: `JULIA_NUM_THREADS => 2`

## Results
A ratio greater than `1.0` denotes a possible regression (marked with :x:), while a ratio less
than `1.0` denotes a possible improvement (marked with :white_check_mark:). Brackets display [tolerances](https://juliaci.github.io/BenchmarkTools.jl/stable/manual/#Benchmark-Parameters) for the benchmark estimates. Only significant results - results
that indicate possible regressions or improvements - are shown below (thus, an empty table means that all
benchmark results remained invariant between builds).

| ID                                                  | time ratio                   | memory ratio                 |
|-----------------------------------------------------|------------------------------|------------------------------|
| `["collect", "unordered", "basesize=1"]`            | 0.79 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["findfirst", "n=1000", "reduce", "basesize=128"]` |                   0.98 (5%)  | 0.97 (1%) :white_check_mark: |
| `["findfirst", "n=1000", "reduce", "basesize=256"]` |                1.21 (5%) :x: |                1.19 (1%) :x: |
| `["findfirst", "n=1000", "reduce", "basesize=512"]` | 0.93 (5%) :white_check_mark: | 0.93 (1%) :white_check_mark: |
| `["findfirst", "n=400", "reduce", "basesize=128"]`  |                   0.96 (5%)  | 0.94 (1%) :white_check_mark: |
| `["findfirst", "n=400", "reduce", "basesize=512"]`  |                   1.03 (5%)  |                1.04 (1%) :x: |
| `["findfirst", "n=500", "reduce", "basesize=128"]`  |                1.59 (5%) :x: |                1.43 (1%) :x: |
| `["findfirst", "n=500", "reduce", "basesize=256"]`  | 0.41 (5%) :white_check_mark: | 0.49 (1%) :white_check_mark: |
| `["findfirst", "n=500", "reduce", "basesize=512"]`  | 0.71 (5%) :white_check_mark: | 0.85 (1%) :white_check_mark: |
| `["overhead", "stoppable=false"]`                   |                1.05 (5%) :x: |                   1.00 (1%)  |
| `["parallel_histogram", "comm", "basesize=16384"]`  |                   1.02 (5%)  |                1.01 (1%) :x: |
| `["parallel_histogram", "comm", "basesize=4096"]`   |                   1.01 (5%)  |                1.02 (1%) :x: |
| `["parallel_histogram", "comm", "basesize=8192"]`   |                   1.01 (5%)  |                1.03 (1%) :x: |
| `["words", "nthreads=4"]`                           | 0.92 (5%) :white_check_mark: |                   1.00 (1%)  |

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
      Ubuntu 24.04.2 LTS
  uname: Linux 6.11.0-1018-azure #18~24.04.1-Ubuntu SMP Sat Jun 28 04:46:03 UTC 2025 x86_64 x86_64
  CPU: AMD EPYC 7763 64-Core Processor: 
              speed         user         nice          sys         idle          irq
       #1  3310 MHz       2502 s          0 s        190 s       7485 s          0 s
       #2  3228 MHz       2536 s          0 s        219 s       7433 s          0 s
       #3  3243 MHz       2452 s          0 s        171 s       7565 s          0 s
       #4  3180 MHz       2504 s          0 s        145 s       7522 s          0 s
       
  Memory: 15.620681762695312 GB (12372.3359375 MB free)
  Uptime: 1021.52 sec
  Load Avg:  1.68  1.52  0.91
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-12.0.1 (ORCJIT, znver3)
```

### Baseline
```
Julia Version 1.7.3
Commit 742b9abb4d (2022-05-06 12:58 UTC)
Platform Info:
  OS: Linux (x86_64-pc-linux-gnu)
      Ubuntu 24.04.2 LTS
  uname: Linux 6.11.0-1018-azure #18~24.04.1-Ubuntu SMP Sat Jun 28 04:46:03 UTC 2025 x86_64 x86_64
  CPU: AMD EPYC 7763 64-Core Processor: 
              speed         user         nice          sys         idle          irq
       #1  3239 MHz       3368 s          0 s        245 s       9674 s          0 s
       #2  3256 MHz       3823 s          0 s        302 s       9174 s          0 s
       #3  3243 MHz       3844 s          0 s        255 s       9201 s          0 s
       #4  3237 MHz       3747 s          0 s        210 s       9327 s          0 s
       
  Memory: 15.620681762695312 GB (12349.37890625 MB free)
  Uptime: 1333.26 sec
  Load Avg:  1.64  1.63  1.14
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-12.0.1 (ORCJIT, znver3)
```

---
# Target result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmark: 6 Aug 2025 - 02:29
* Package commit: aa8c6ab
* Julia commit: 742b9ab
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
| `["collect", "assoc", "basesize=1"]`                | 149.961 ms (5%) |         |   4.36 MiB (1%) |       32800 |
| `["collect", "assoc", "basesize=1024"]`             | 148.248 ms (5%) |         |   1.09 MiB (1%) |          53 |
| `["collect", "assoc", "basesize=32"]`               | 148.408 ms (5%) |         |   1.48 MiB (1%) |        1052 |
| `["collect", "seq"]`                                | 296.122 ms (5%) |         | 256.05 KiB (1%) |           2 |
| `["collect", "unordered", "basesize=1"]`            | 254.429 ms (5%) |         |  23.68 MiB (1%) |      405710 |
| `["collect", "unordered", "basesize=1024"]`         | 158.144 ms (5%) |         |   1.01 MiB (1%) |         991 |
| `["collect", "unordered", "basesize=32"]`           | 168.810 ms (5%) |         |   1.60 MiB (1%) |       15375 |
| `["findfirst", "n=1000", "foldl"]`                  | 509.070 ms (5%) |         |                 |             |
| `["findfirst", "n=1000", "reduce", "basesize=128"]` | 270.880 ms (5%) |         | 224.89 KiB (1%) |        3172 |
| `["findfirst", "n=1000", "reduce", "basesize=256"]` | 369.315 ms (5%) |         | 164.64 KiB (1%) |        2303 |
| `["findfirst", "n=1000", "reduce", "basesize=512"]` | 398.151 ms (5%) |         |  96.75 KiB (1%) |        1346 |
| `["findfirst", "n=400", "foldl"]`                   | 381.384 ms (5%) |         |                 |             |
| `["findfirst", "n=400", "reduce", "basesize=128"]`  | 195.161 ms (5%) |         | 371.22 KiB (1%) |        5300 |
| `["findfirst", "n=400", "reduce", "basesize=256"]`  | 199.285 ms (5%) |         | 200.89 KiB (1%) |        2874 |
| `["findfirst", "n=400", "reduce", "basesize=512"]`  | 286.603 ms (5%) |         | 145.81 KiB (1%) |        2086 |
| `["findfirst", "n=500", "foldl"]`                   |  66.031 ms (5%) |         |                 |             |
| `["findfirst", "n=500", "reduce", "basesize=128"]`  | 192.809 ms (5%) |         | 308.86 KiB (1%) |        4333 |
| `["findfirst", "n=500", "reduce", "basesize=256"]`  |  75.458 ms (5%) |         |  81.23 KiB (1%) |        1114 |
| `["findfirst", "n=500", "reduce", "basesize=512"]`  |  66.362 ms (5%) |         |  50.75 KiB (1%) |         678 |
| `["overhead", "default"]`                           |  50.144 μs (5%) |         |  32.73 KiB (1%) |         418 |
| `["overhead", "stoppable=false"]`                   |  51.877 μs (5%) |         |  32.75 KiB (1%) |         418 |
| `["overhead", "stoppable=true"]`                    |  58.098 μs (5%) |         |  44.25 KiB (1%) |         610 |
| `["parallel_histogram", "assoc", "basesize=16384"]` |   2.392 ms (5%) |         | 728.91 KiB (1%) |          57 |
| `["parallel_histogram", "assoc", "basesize=4096"]`  |   2.936 ms (5%) |         |   1.79 MiB (1%) |         215 |
| `["parallel_histogram", "assoc", "basesize=8192"]`  |   2.669 ms (5%) |         |   1.42 MiB (1%) |         117 |
| `["parallel_histogram", "comm", "basesize=16384"]`  |   8.308 ms (5%) |         |   1.55 MiB (1%) |        1527 |
| `["parallel_histogram", "comm", "basesize=4096"]`   |  12.467 ms (5%) |         |   1.23 MiB (1%) |        6454 |
| `["parallel_histogram", "comm", "basesize=8192"]`   |  11.388 ms (5%) |         |   1.26 MiB (1%) |        5355 |
| `["parallel_histogram", "seq"]`                     |   4.247 ms (5%) |         | 364.16 KiB (1%) |          24 |
| `["partition_length_maximum", "rand", "foldl"]`     |  31.317 ms (5%) |         |                 |             |
| `["partition_length_maximum", "rand", "reduce"]`    |  15.681 ms (5%) |         |  736 bytes (1%) |          11 |
| `["splitby", "count", "foldl"]`                     |   1.532 ms (5%) |         |                 |             |
| `["splitby", "count", "man"]`                       |   1.166 ms (5%) |         |                 |             |
| `["splitby", "count", "reduce"]`                    | 719.014 μs (5%) |         |   1.06 KiB (1%) |          18 |
| `["sum", "random", "foldl"]`                        |  11.055 ms (5%) |         |                 |             |
| `["sum", "random", "reduce", "basesize=128"]`       |   5.666 ms (5%) |         |  74.22 KiB (1%) |        1105 |
| `["sum", "random", "reduce", "basesize=256"]`       |   5.597 ms (5%) |         |  36.72 KiB (1%) |         545 |
| `["sum", "random", "reduce", "basesize=512"]`       |   5.570 ms (5%) |         |  18.05 KiB (1%) |         268 |
| `["sum", "uniform", "foldl"]`                       |  10.933 ms (5%) |         |                 |             |
| `["sum", "uniform", "reduce", "basesize=128"]`      |   5.607 ms (5%) |         |  74.16 KiB (1%) |        1103 |
| `["sum", "uniform", "reduce", "basesize=256"]`      |   5.545 ms (5%) |         |  36.78 KiB (1%) |         547 |
| `["sum", "uniform", "reduce", "basesize=512"]`      |   5.506 ms (5%) |         |  18.08 KiB (1%) |         269 |
| `["sum", "valley", "foldl"]`                        |  11.168 ms (5%) |         |                 |             |
| `["sum", "valley", "reduce", "basesize=128"]`       |   5.729 ms (5%) |         |  74.06 KiB (1%) |        1100 |
| `["sum", "valley", "reduce", "basesize=256"]`       |   5.661 ms (5%) |         |  36.81 KiB (1%) |         548 |
| `["sum", "valley", "reduce", "basesize=512"]`       |   5.643 ms (5%) |         |  18.05 KiB (1%) |         268 |
| `["words", "nthreads=1"]`                           |  14.525 ms (5%) |         |  31.63 MiB (1%) |     1031009 |
| `["words", "nthreads=2"]`                           |   9.497 ms (5%) |         |  32.35 MiB (1%) |     1031103 |
| `["words", "nthreads=4"]`                           |   9.602 ms (5%) |         |  32.80 MiB (1%) |     1031225 |

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
      Ubuntu 24.04.2 LTS
  uname: Linux 6.11.0-1018-azure #18~24.04.1-Ubuntu SMP Sat Jun 28 04:46:03 UTC 2025 x86_64 x86_64
  CPU: AMD EPYC 7763 64-Core Processor: 
              speed         user         nice          sys         idle          irq
       #1  3310 MHz       2502 s          0 s        190 s       7485 s          0 s
       #2  3228 MHz       2536 s          0 s        219 s       7433 s          0 s
       #3  3243 MHz       2452 s          0 s        171 s       7565 s          0 s
       #4  3180 MHz       2504 s          0 s        145 s       7522 s          0 s
       
  Memory: 15.620681762695312 GB (12372.3359375 MB free)
  Uptime: 1021.52 sec
  Load Avg:  1.68  1.52  0.91
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-12.0.1 (ORCJIT, znver3)
```

---
# Baseline result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmark: 6 Aug 2025 - 02:34
* Package commit: 2a51f8d
* Julia commit: 742b9ab
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
| `["collect", "assoc", "basesize=1"]`                | 149.946 ms (5%) |         |   4.36 MiB (1%) |       32800 |
| `["collect", "assoc", "basesize=1024"]`             | 148.556 ms (5%) |         |   1.09 MiB (1%) |          53 |
| `["collect", "assoc", "basesize=32"]`               | 148.380 ms (5%) |         |   1.48 MiB (1%) |        1052 |
| `["collect", "seq"]`                                | 296.232 ms (5%) |         | 256.05 KiB (1%) |           2 |
| `["collect", "unordered", "basesize=1"]`            | 323.954 ms (5%) |         |  23.67 MiB (1%) |      405331 |
| `["collect", "unordered", "basesize=1024"]`         | 158.195 ms (5%) |         |   1.01 MiB (1%) |        1069 |
| `["collect", "unordered", "basesize=32"]`           | 169.784 ms (5%) |         |   1.60 MiB (1%) |       15396 |
| `["findfirst", "n=1000", "foldl"]`                  | 506.827 ms (5%) |         |                 |             |
| `["findfirst", "n=1000", "reduce", "basesize=128"]` | 277.015 ms (5%) |         | 232.92 KiB (1%) |        3278 |
| `["findfirst", "n=1000", "reduce", "basesize=256"]` | 305.243 ms (5%) |         | 138.48 KiB (1%) |        1949 |
| `["findfirst", "n=1000", "reduce", "basesize=512"]` | 427.451 ms (5%) |         | 103.53 KiB (1%) |        1454 |
| `["findfirst", "n=400", "foldl"]`                   | 379.911 ms (5%) |         |                 |             |
| `["findfirst", "n=400", "reduce", "basesize=128"]`  | 202.682 ms (5%) |         | 394.44 KiB (1%) |        5609 |
| `["findfirst", "n=400", "reduce", "basesize=256"]`  | 198.659 ms (5%) |         | 201.02 KiB (1%) |        2878 |
| `["findfirst", "n=400", "reduce", "basesize=512"]`  | 277.250 ms (5%) |         | 140.66 KiB (1%) |        2022 |
| `["findfirst", "n=500", "foldl"]`                   |  65.897 ms (5%) |         |                 |             |
| `["findfirst", "n=500", "reduce", "basesize=128"]`  | 121.167 ms (5%) |         | 215.58 KiB (1%) |        2988 |
| `["findfirst", "n=500", "reduce", "basesize=256"]`  | 184.227 ms (5%) |         | 166.58 KiB (1%) |        2307 |
| `["findfirst", "n=500", "reduce", "basesize=512"]`  |  93.897 ms (5%) |         |  59.84 KiB (1%) |         819 |
| `["overhead", "default"]`                           |  50.855 μs (5%) |         |  32.73 KiB (1%) |         418 |
| `["overhead", "stoppable=false"]`                   |  49.362 μs (5%) |         |  32.75 KiB (1%) |         418 |
| `["overhead", "stoppable=true"]`                    |  57.097 μs (5%) |         |  44.25 KiB (1%) |         610 |
| `["parallel_histogram", "assoc", "basesize=16384"]` |   2.386 ms (5%) |         | 728.91 KiB (1%) |          57 |
| `["parallel_histogram", "assoc", "basesize=4096"]`  |   2.939 ms (5%) |         |   1.79 MiB (1%) |         215 |
| `["parallel_histogram", "assoc", "basesize=8192"]`  |   2.667 ms (5%) |         |   1.42 MiB (1%) |         117 |
| `["parallel_histogram", "comm", "basesize=16384"]`  |   8.149 ms (5%) |         |   1.53 MiB (1%) |         882 |
| `["parallel_histogram", "comm", "basesize=4096"]`   |  12.316 ms (5%) |         |   1.21 MiB (1%) |        5677 |
| `["parallel_histogram", "comm", "basesize=8192"]`   |  11.225 ms (5%) |         |   1.23 MiB (1%) |        5195 |
| `["parallel_histogram", "seq"]`                     |   4.258 ms (5%) |         | 364.16 KiB (1%) |          24 |
| `["partition_length_maximum", "rand", "foldl"]`     |  31.307 ms (5%) |         |                 |             |
| `["partition_length_maximum", "rand", "reduce"]`    |  15.690 ms (5%) |         |  736 bytes (1%) |          11 |
| `["splitby", "count", "foldl"]`                     |   1.504 ms (5%) |         |                 |             |
| `["splitby", "count", "man"]`                       |   1.141 ms (5%) |         |                 |             |
| `["splitby", "count", "reduce"]`                    | 740.223 μs (5%) |         |   1.06 KiB (1%) |          18 |
| `["sum", "random", "foldl"]`                        |  11.134 ms (5%) |         |                 |             |
| `["sum", "random", "reduce", "basesize=128"]`       |   5.682 ms (5%) |         |  74.12 KiB (1%) |        1102 |
| `["sum", "random", "reduce", "basesize=256"]`       |   5.626 ms (5%) |         |  36.75 KiB (1%) |         546 |
| `["sum", "random", "reduce", "basesize=512"]`       |   5.607 ms (5%) |         |  18.08 KiB (1%) |         269 |
| `["sum", "uniform", "foldl"]`                       |  10.931 ms (5%) |         |                 |             |
| `["sum", "uniform", "reduce", "basesize=128"]`      |   5.587 ms (5%) |         |  74.19 KiB (1%) |        1104 |
| `["sum", "uniform", "reduce", "basesize=256"]`      |   5.543 ms (5%) |         |  36.75 KiB (1%) |         546 |
| `["sum", "uniform", "reduce", "basesize=512"]`      |   5.499 ms (5%) |         |  18.08 KiB (1%) |         269 |
| `["sum", "valley", "foldl"]`                        |  11.169 ms (5%) |         |                 |             |
| `["sum", "valley", "reduce", "basesize=128"]`       |   5.724 ms (5%) |         |  74.06 KiB (1%) |        1100 |
| `["sum", "valley", "reduce", "basesize=256"]`       |   5.663 ms (5%) |         |  36.75 KiB (1%) |         546 |
| `["sum", "valley", "reduce", "basesize=512"]`       |   5.641 ms (5%) |         |  18.08 KiB (1%) |         269 |
| `["words", "nthreads=1"]`                           |  14.432 ms (5%) |         |  31.57 MiB (1%) |     1028217 |
| `["words", "nthreads=2"]`                           |   9.900 ms (5%) |         |  32.28 MiB (1%) |     1028341 |
| `["words", "nthreads=4"]`                           |  10.443 ms (5%) |         |  32.91 MiB (1%) |     1028481 |

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
      Ubuntu 24.04.2 LTS
  uname: Linux 6.11.0-1018-azure #18~24.04.1-Ubuntu SMP Sat Jun 28 04:46:03 UTC 2025 x86_64 x86_64
  CPU: AMD EPYC 7763 64-Core Processor: 
              speed         user         nice          sys         idle          irq
       #1  3239 MHz       3368 s          0 s        245 s       9674 s          0 s
       #2  3256 MHz       3823 s          0 s        302 s       9174 s          0 s
       #3  3243 MHz       3844 s          0 s        255 s       9201 s          0 s
       #4  3237 MHz       3747 s          0 s        210 s       9327 s          0 s
       
  Memory: 15.620681762695312 GB (12349.37890625 MB free)
  Uptime: 1333.26 sec
  Load Avg:  1.64  1.63  1.14
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-12.0.1 (ORCJIT, znver3)
```

---
# Runtime information
| Runtime Info | |
|:--|:--|
| BLAS #threads | 4 |
| `BLAS.vendor()` | `openblas64` |
| `Sys.CPU_THREADS` | 4 |

`lscpu` output:

    Architecture:                         x86_64
    CPU op-mode(s):                       32-bit, 64-bit
    Address sizes:                        48 bits physical, 48 bits virtual
    Byte Order:                           Little Endian
    CPU(s):                               4
    On-line CPU(s) list:                  0-3
    Vendor ID:                            AuthenticAMD
    Model name:                           AMD EPYC 7763 64-Core Processor
    CPU family:                           25
    Model:                                1
    Thread(s) per core:                   2
    Core(s) per socket:                   2
    Socket(s):                            1
    Stepping:                             1
    BogoMIPS:                             4890.86
    Flags:                                fpu vme de pse tsc msr pae mce cx8 apic sep mtrr pge mca cmov pat pse36 clflush mmx fxsr sse sse2 ht syscall nx mmxext fxsr_opt pdpe1gb rdtscp lm constant_tsc rep_good nopl tsc_reliable nonstop_tsc cpuid extd_apicid aperfmperf tsc_known_freq pni pclmulqdq ssse3 fma cx16 pcid sse4_1 sse4_2 movbe popcnt aes xsave avx f16c rdrand hypervisor lahf_lm cmp_legacy svm cr8_legacy abm sse4a misalignsse 3dnowprefetch osvw topoext vmmcall fsgsbase bmi1 avx2 smep bmi2 erms invpcid rdseed adx smap clflushopt clwb sha_ni xsaveopt xsavec xgetbv1 xsaves user_shstk clzero xsaveerptr rdpru arat npt nrip_save tsc_scale vmcb_clean flushbyasid decodeassists pausefilter pfthreshold v_vmsave_vmload umip vaes vpclmulqdq rdpid fsrm
    Virtualization:                       AMD-V
    Hypervisor vendor:                    Microsoft
    Virtualization type:                  full
    L1d cache:                            64 KiB (2 instances)
    L1i cache:                            64 KiB (2 instances)
    L2 cache:                             1 MiB (2 instances)
    L3 cache:                             32 MiB (1 instance)
    NUMA node(s):                         1
    NUMA node0 CPU(s):                    0-3
    Vulnerability Gather data sampling:   Not affected
    Vulnerability Itlb multihit:          Not affected
    Vulnerability L1tf:                   Not affected
    Vulnerability Mds:                    Not affected
    Vulnerability Meltdown:               Not affected
    Vulnerability Mmio stale data:        Not affected
    Vulnerability Reg file data sampling: Not affected
    Vulnerability Retbleed:               Not affected
    Vulnerability Spec rstack overflow:   Vulnerable: Safe RET, no microcode
    Vulnerability Spec store bypass:      Vulnerable
    Vulnerability Spectre v1:             Mitigation; usercopy/swapgs barriers and __user pointer sanitization
    Vulnerability Spectre v2:             Mitigation; Retpolines; STIBP disabled; RSB filling; PBRSB-eIBRS Not affected; BHI Not affected
    Vulnerability Srbds:                  Not affected
    Vulnerability Tsx async abort:        Not affected
    

| Cpu Property       | Value                                                      |
|:------------------ |:---------------------------------------------------------- |
| Brand              | AMD EPYC 7763 64-Core Processor                            |
| Vendor             | :AMD                                                       |
| Architecture       | :Unknown                                                   |
| Model              | Family: 0xaf, Model: 0x01, Stepping: 0x01, Type: 0x00      |
| Cores              | 16 physical cores, 16 logical cores (on executing CPU)     |
|                    | No Hyperthreading hardware capability detected             |
| Clock Frequencies  | Not supported by CPU                                       |
| Data Cache         | Level 1:3 : (32, 512, 32768) kbytes                        |
|                    | 64 byte cache line size                                    |
| Address Size       | 48 bits virtual, 48 bits physical                          |
| SIMD               | 256 bit = 32 byte max. SIMD vector size                    |
| Time Stamp Counter | TSC is accessible via `rdtsc`                              |
|                    | TSC runs at constant rate (invariant from clock frequency) |
| Perf. Monitoring   | Performance Monitoring Counters (PMC) are not supported    |
| Hypervisor         | Yes, Microsoft                                             |

