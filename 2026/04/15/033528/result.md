# Multi-thread benchmark result

* Pull request commit: [`c23d0798bcfeb8a7233fa5bb10cb862190e85260`](https://github.com/JuliaFolds/Transducers.jl/commit/c23d0798bcfeb8a7233fa5bb10cb862190e85260)
* Pull request: <https://github.com/JuliaFolds/Transducers.jl/pull/243> (Update */Manifest.toml)

# Judge result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmarks:
    - Target: 15 Apr 2026 - 03:29
    - Baseline: 15 Apr 2026 - 03:35
* Package commits:
    - Target: ed33bb8
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
| `["findfirst", "n=1000", "reduce", "basesize=256"]` | 0.91 (5%) :white_check_mark: | 0.94 (1%) :white_check_mark: |
| `["findfirst", "n=1000", "reduce", "basesize=512"]` | 0.76 (5%) :white_check_mark: | 0.77 (1%) :white_check_mark: |
| `["findfirst", "n=400", "reduce", "basesize=128"]`  |                   1.02 (5%)  |                1.03 (1%) :x: |
| `["findfirst", "n=400", "reduce", "basesize=512"]`  |                1.18 (5%) :x: |                1.25 (1%) :x: |
| `["findfirst", "n=500", "reduce", "basesize=128"]`  |                2.87 (5%) :x: |                2.22 (1%) :x: |
| `["findfirst", "n=500", "reduce", "basesize=256"]`  |                1.71 (5%) :x: |                1.33 (1%) :x: |
| `["findfirst", "n=500", "reduce", "basesize=512"]`  |                   1.00 (5%)  | 0.93 (1%) :white_check_mark: |
| `["parallel_histogram", "comm", "basesize=16384"]`  |                1.08 (5%) :x: |                   1.01 (1%)  |
| `["parallel_histogram", "comm", "basesize=4096"]`   |                   0.96 (5%)  |                1.01 (1%) :x: |
| `["splitby", "count", "foldl"]`                     | 0.90 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["splitby", "count", "reduce"]`                    |                1.19 (5%) :x: | 0.97 (1%) :white_check_mark: |
| `["words", "nthreads=2"]`                           |                1.05 (5%) :x: |                   1.01 (1%)  |

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
      Ubuntu 24.04.4 LTS
  uname: Linux 6.17.0-1010-azure #10~24.04.1-Ubuntu SMP Fri Mar  6 22:00:57 UTC 2026 x86_64 x86_64
  CPU: AMD EPYC 7763 64-Core Processor: 
              speed         user         nice          sys         idle          irq
       #1  3242 MHz       2320 s          0 s        166 s       4100 s          0 s
       #2  3232 MHz       2329 s          0 s        178 s       4077 s          0 s
       #3  3250 MHz       2649 s          0 s        143 s       3788 s          0 s
       #4  3238 MHz       2632 s          0 s        140 s       3805 s          0 s
       
  Memory: 15.61495590209961 GB (11282.2109375 MB free)
  Uptime: 663.61 sec
  Load Avg:  1.57  1.45  0.86
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
      Ubuntu 24.04.4 LTS
  uname: Linux 6.17.0-1010-azure #10~24.04.1-Ubuntu SMP Fri Mar  6 22:00:57 UTC 2026 x86_64 x86_64
  CPU: AMD EPYC 7763 64-Core Processor: 
              speed         user         nice          sys         idle          irq
       #1  3241 MHz       3809 s          0 s        213 s       5614 s          0 s
       #2  3176 MHz       3568 s          0 s        236 s       5825 s          0 s
       #3  3243 MHz       3801 s          0 s        212 s       5618 s          0 s
       #4  3243 MHz       3524 s          0 s        196 s       5909 s          0 s
       
  Memory: 15.61495590209961 GB (11087.08984375 MB free)
  Uptime: 969.39 sec
  Load Avg:  1.64  1.56  1.09
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-12.0.1 (ORCJIT, znver3)
```

---
# Target result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmark: 15 Apr 2026 - 03:29
* Package commit: ed33bb8
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
| `["collect", "assoc", "basesize=1"]`                | 150.002 ms (5%) |         |   4.36 MiB (1%) |       32800 |
| `["collect", "assoc", "basesize=1024"]`             | 148.435 ms (5%) |         |   1.09 MiB (1%) |          53 |
| `["collect", "assoc", "basesize=32"]`               | 148.573 ms (5%) |         |   1.48 MiB (1%) |        1052 |
| `["collect", "seq"]`                                | 296.454 ms (5%) |         | 256.05 KiB (1%) |           2 |
| `["collect", "unordered", "basesize=1"]`            | 245.529 ms (5%) |         |  23.71 MiB (1%) |      406883 |
| `["collect", "unordered", "basesize=1024"]`         | 157.816 ms (5%) |         |   1.01 MiB (1%) |        1084 |
| `["collect", "unordered", "basesize=32"]`           | 168.856 ms (5%) |         |   1.60 MiB (1%) |       15210 |
| `["findfirst", "n=1000", "foldl"]`                  | 510.578 ms (5%) |         |                 |             |
| `["findfirst", "n=1000", "reduce", "basesize=128"]` | 370.375 ms (5%) |         | 303.05 KiB (1%) |        4260 |
| `["findfirst", "n=1000", "reduce", "basesize=256"]` | 342.050 ms (5%) |         | 157.23 KiB (1%) |        2194 |
| `["findfirst", "n=1000", "reduce", "basesize=512"]` | 469.164 ms (5%) |         | 103.53 KiB (1%) |        1454 |
| `["findfirst", "n=400", "foldl"]`                   | 382.221 ms (5%) |         |                 |             |
| `["findfirst", "n=400", "reduce", "basesize=128"]`  | 201.164 ms (5%) |         | 391.64 KiB (1%) |        5578 |
| `["findfirst", "n=400", "reduce", "basesize=256"]`  | 199.620 ms (5%) |         | 198.83 KiB (1%) |        2855 |
| `["findfirst", "n=400", "reduce", "basesize=512"]`  | 255.613 ms (5%) |         | 138.05 KiB (1%) |        1971 |
| `["findfirst", "n=500", "foldl"]`                   |  66.349 ms (5%) |         |                 |             |
| `["findfirst", "n=500", "reduce", "basesize=128"]`  | 149.277 ms (5%) |         | 256.25 KiB (1%) |        3544 |
| `["findfirst", "n=500", "reduce", "basesize=256"]`  | 171.053 ms (5%) |         | 160.67 KiB (1%) |        2223 |
| `["findfirst", "n=500", "reduce", "basesize=512"]`  |  81.252 ms (5%) |         |  52.77 KiB (1%) |         719 |
| `["overhead", "default"]`                           |  50.995 μs (5%) |         |  32.70 KiB (1%) |         417 |
| `["overhead", "stoppable=false"]`                   |  52.137 μs (5%) |         |  32.75 KiB (1%) |         418 |
| `["overhead", "stoppable=true"]`                    |  57.247 μs (5%) |         |  44.25 KiB (1%) |         610 |
| `["parallel_histogram", "assoc", "basesize=16384"]` |   2.396 ms (5%) |         | 728.91 KiB (1%) |          57 |
| `["parallel_histogram", "assoc", "basesize=4096"]`  |   2.960 ms (5%) |         |   1.79 MiB (1%) |         216 |
| `["parallel_histogram", "assoc", "basesize=8192"]`  |   2.678 ms (5%) |         |   1.42 MiB (1%) |         117 |
| `["parallel_histogram", "comm", "basesize=16384"]`  |   8.972 ms (5%) |         |   1.58 MiB (1%) |        2302 |
| `["parallel_histogram", "comm", "basesize=4096"]`   |  12.644 ms (5%) |         |   1.32 MiB (1%) |        9281 |
| `["parallel_histogram", "comm", "basesize=8192"]`   |  11.840 ms (5%) |         |   1.28 MiB (1%) |        7909 |
| `["parallel_histogram", "seq"]`                     |   4.269 ms (5%) |         | 364.16 KiB (1%) |          24 |
| `["partition_length_maximum", "rand", "foldl"]`     |  31.370 ms (5%) |         |                 |             |
| `["partition_length_maximum", "rand", "reduce"]`    |  15.713 ms (5%) |         |  736 bytes (1%) |          11 |
| `["splitby", "count", "foldl"]`                     |   1.490 ms (5%) |         |                 |             |
| `["splitby", "count", "man"]`                       |   1.167 ms (5%) |         |                 |             |
| `["splitby", "count", "reduce"]`                    | 859.969 μs (5%) |         |   1.03 KiB (1%) |          18 |
| `["sum", "random", "foldl"]`                        |  11.008 ms (5%) |         |                 |             |
| `["sum", "random", "reduce", "basesize=128"]`       |   5.658 ms (5%) |         |  74.19 KiB (1%) |        1104 |
| `["sum", "random", "reduce", "basesize=256"]`       |   5.577 ms (5%) |         |  36.81 KiB (1%) |         548 |
| `["sum", "random", "reduce", "basesize=512"]`       |   5.543 ms (5%) |         |  18.11 KiB (1%) |         270 |
| `["sum", "uniform", "foldl"]`                       |  10.924 ms (5%) |         |                 |             |
| `["sum", "uniform", "reduce", "basesize=128"]`      |   5.608 ms (5%) |         |  74.19 KiB (1%) |        1104 |
| `["sum", "uniform", "reduce", "basesize=256"]`      |   5.536 ms (5%) |         |  36.78 KiB (1%) |         547 |
| `["sum", "uniform", "reduce", "basesize=512"]`      |   5.504 ms (5%) |         |  18.05 KiB (1%) |         268 |
| `["sum", "valley", "foldl"]`                        |  11.173 ms (5%) |         |                 |             |
| `["sum", "valley", "reduce", "basesize=128"]`       |   5.741 ms (5%) |         |  74.09 KiB (1%) |        1101 |
| `["sum", "valley", "reduce", "basesize=256"]`       |   5.676 ms (5%) |         |  36.75 KiB (1%) |         546 |
| `["sum", "valley", "reduce", "basesize=512"]`       |   5.655 ms (5%) |         |  18.05 KiB (1%) |         268 |
| `["words", "nthreads=1"]`                           |  14.631 ms (5%) |         |  31.72 MiB (1%) |     1033763 |
| `["words", "nthreads=2"]`                           |  10.420 ms (5%) |         |  32.44 MiB (1%) |     1033837 |
| `["words", "nthreads=4"]`                           |  10.903 ms (5%) |         |  33.06 MiB (1%) |     1034008 |

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
      Ubuntu 24.04.4 LTS
  uname: Linux 6.17.0-1010-azure #10~24.04.1-Ubuntu SMP Fri Mar  6 22:00:57 UTC 2026 x86_64 x86_64
  CPU: AMD EPYC 7763 64-Core Processor: 
              speed         user         nice          sys         idle          irq
       #1  3242 MHz       2320 s          0 s        166 s       4100 s          0 s
       #2  3232 MHz       2329 s          0 s        178 s       4077 s          0 s
       #3  3250 MHz       2649 s          0 s        143 s       3788 s          0 s
       #4  3238 MHz       2632 s          0 s        140 s       3805 s          0 s
       
  Memory: 15.61495590209961 GB (11282.2109375 MB free)
  Uptime: 663.61 sec
  Load Avg:  1.57  1.45  0.86
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-12.0.1 (ORCJIT, znver3)
```

---
# Baseline result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmark: 15 Apr 2026 - 03:35
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
| `["collect", "assoc", "basesize=1"]`                | 149.955 ms (5%) |         |   4.36 MiB (1%) |       32800 |
| `["collect", "assoc", "basesize=1024"]`             | 148.701 ms (5%) |         |   1.09 MiB (1%) |          53 |
| `["collect", "assoc", "basesize=32"]`               | 148.518 ms (5%) |         |   1.48 MiB (1%) |        1052 |
| `["collect", "seq"]`                                | 296.495 ms (5%) |         | 256.05 KiB (1%) |           2 |
| `["collect", "unordered", "basesize=1"]`            | 245.948 ms (5%) |         |  23.73 MiB (1%) |      407386 |
| `["collect", "unordered", "basesize=1024"]`         | 158.179 ms (5%) |         |   1.01 MiB (1%) |        1121 |
| `["collect", "unordered", "basesize=32"]`           | 168.551 ms (5%) |         |   1.60 MiB (1%) |       15249 |
| `["findfirst", "n=1000", "foldl"]`                  | 510.813 ms (5%) |         |                 |             |
| `["findfirst", "n=1000", "reduce", "basesize=128"]` | 369.306 ms (5%) |         | 305.06 KiB (1%) |        4270 |
| `["findfirst", "n=1000", "reduce", "basesize=256"]` | 375.287 ms (5%) |         | 167.05 KiB (1%) |        2336 |
| `["findfirst", "n=1000", "reduce", "basesize=512"]` | 614.369 ms (5%) |         | 135.08 KiB (1%) |        1883 |
| `["findfirst", "n=400", "foldl"]`                   | 382.283 ms (5%) |         |                 |             |
| `["findfirst", "n=400", "reduce", "basesize=128"]`  | 197.625 ms (5%) |         | 380.19 KiB (1%) |        5406 |
| `["findfirst", "n=400", "reduce", "basesize=256"]`  | 200.409 ms (5%) |         | 197.09 KiB (1%) |        2831 |
| `["findfirst", "n=400", "reduce", "basesize=512"]`  | 216.045 ms (5%) |         | 110.31 KiB (1%) |        1592 |
| `["findfirst", "n=500", "foldl"]`                   |  66.348 ms (5%) |         |                 |             |
| `["findfirst", "n=500", "reduce", "basesize=128"]`  |  52.102 ms (5%) |         | 115.41 KiB (1%) |        1575 |
| `["findfirst", "n=500", "reduce", "basesize=256"]`  | 100.079 ms (5%) |         | 120.53 KiB (1%) |        1629 |
| `["findfirst", "n=500", "reduce", "basesize=512"]`  |  81.318 ms (5%) |         |  56.81 KiB (1%) |         778 |
| `["overhead", "default"]`                           |  50.003 μs (5%) |         |  32.73 KiB (1%) |         418 |
| `["overhead", "stoppable=false"]`                   |  51.216 μs (5%) |         |  32.75 KiB (1%) |         418 |
| `["overhead", "stoppable=true"]`                    |  55.914 μs (5%) |         |  44.22 KiB (1%) |         609 |
| `["parallel_histogram", "assoc", "basesize=16384"]` |   2.400 ms (5%) |         | 728.91 KiB (1%) |          57 |
| `["parallel_histogram", "assoc", "basesize=4096"]`  |   2.967 ms (5%) |         |   1.79 MiB (1%) |         216 |
| `["parallel_histogram", "assoc", "basesize=8192"]`  |   2.681 ms (5%) |         |   1.42 MiB (1%) |         117 |
| `["parallel_histogram", "comm", "basesize=16384"]`  |   8.283 ms (5%) |         |   1.57 MiB (1%) |        1976 |
| `["parallel_histogram", "comm", "basesize=4096"]`   |  13.139 ms (5%) |         |   1.30 MiB (1%) |        8801 |
| `["parallel_histogram", "comm", "basesize=8192"]`   |  12.077 ms (5%) |         |   1.28 MiB (1%) |        8253 |
| `["parallel_histogram", "seq"]`                     |   4.265 ms (5%) |         | 364.16 KiB (1%) |          24 |
| `["partition_length_maximum", "rand", "foldl"]`     |  31.352 ms (5%) |         |                 |             |
| `["partition_length_maximum", "rand", "reduce"]`    |  15.699 ms (5%) |         |  736 bytes (1%) |          11 |
| `["splitby", "count", "foldl"]`                     |   1.652 ms (5%) |         |                 |             |
| `["splitby", "count", "man"]`                       |   1.167 ms (5%) |         |                 |             |
| `["splitby", "count", "reduce"]`                    | 724.496 μs (5%) |         |   1.06 KiB (1%) |          18 |
| `["sum", "random", "foldl"]`                        |  11.117 ms (5%) |         |                 |             |
| `["sum", "random", "reduce", "basesize=128"]`       |   5.704 ms (5%) |         |  74.12 KiB (1%) |        1102 |
| `["sum", "random", "reduce", "basesize=256"]`       |   5.639 ms (5%) |         |  36.75 KiB (1%) |         546 |
| `["sum", "random", "reduce", "basesize=512"]`       |   5.604 ms (5%) |         |  18.08 KiB (1%) |         269 |
| `["sum", "uniform", "foldl"]`                       |  10.939 ms (5%) |         |                 |             |
| `["sum", "uniform", "reduce", "basesize=128"]`      |   5.608 ms (5%) |         |  74.22 KiB (1%) |        1105 |
| `["sum", "uniform", "reduce", "basesize=256"]`      |   5.548 ms (5%) |         |  36.78 KiB (1%) |         547 |
| `["sum", "uniform", "reduce", "basesize=512"]`      |   5.511 ms (5%) |         |  18.05 KiB (1%) |         268 |
| `["sum", "valley", "foldl"]`                        |  11.185 ms (5%) |         |                 |             |
| `["sum", "valley", "reduce", "basesize=128"]`       |   5.740 ms (5%) |         |  74.12 KiB (1%) |        1102 |
| `["sum", "valley", "reduce", "basesize=256"]`       |   5.676 ms (5%) |         |  36.75 KiB (1%) |         546 |
| `["sum", "valley", "reduce", "basesize=512"]`       |   5.659 ms (5%) |         |  18.08 KiB (1%) |         269 |
| `["words", "nthreads=1"]`                           |  14.669 ms (5%) |         |  31.89 MiB (1%) |     1038946 |
| `["words", "nthreads=2"]`                           |   9.888 ms (5%) |         |  32.25 MiB (1%) |     1039014 |
| `["words", "nthreads=4"]`                           |  10.385 ms (5%) |         |  33.14 MiB (1%) |     1039156 |

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
      Ubuntu 24.04.4 LTS
  uname: Linux 6.17.0-1010-azure #10~24.04.1-Ubuntu SMP Fri Mar  6 22:00:57 UTC 2026 x86_64 x86_64
  CPU: AMD EPYC 7763 64-Core Processor: 
              speed         user         nice          sys         idle          irq
       #1  3241 MHz       3809 s          0 s        213 s       5614 s          0 s
       #2  3176 MHz       3568 s          0 s        236 s       5825 s          0 s
       #3  3243 MHz       3801 s          0 s        212 s       5618 s          0 s
       #4  3243 MHz       3524 s          0 s        196 s       5909 s          0 s
       
  Memory: 15.61495590209961 GB (11087.08984375 MB free)
  Uptime: 969.39 sec
  Load Avg:  1.64  1.56  1.09
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

    Architecture:                            x86_64
    CPU op-mode(s):                          32-bit, 64-bit
    Address sizes:                           48 bits physical, 48 bits virtual
    Byte Order:                              Little Endian
    CPU(s):                                  4
    On-line CPU(s) list:                     0-3
    Vendor ID:                               AuthenticAMD
    Model name:                              AMD EPYC 7763 64-Core Processor
    CPU family:                              25
    Model:                                   1
    Thread(s) per core:                      2
    Core(s) per socket:                      2
    Socket(s):                               1
    Stepping:                                1
    BogoMIPS:                                4890.85
    Flags:                                   fpu vme de pse tsc msr pae mce cx8 apic sep mtrr pge mca cmov pat pse36 clflush mmx fxsr sse sse2 ht syscall nx mmxext fxsr_opt pdpe1gb rdtscp lm constant_tsc rep_good nopl tsc_reliable nonstop_tsc cpuid extd_apicid aperfmperf tsc_known_freq pni pclmulqdq ssse3 fma cx16 pcid sse4_1 sse4_2 movbe popcnt aes xsave avx f16c rdrand hypervisor lahf_lm cmp_legacy svm cr8_legacy abm sse4a misalignsse 3dnowprefetch osvw topoext vmmcall fsgsbase bmi1 avx2 smep bmi2 erms invpcid rdseed adx smap clflushopt clwb sha_ni xsaveopt xsavec xgetbv1 xsaves user_shstk clzero xsaveerptr rdpru arat npt nrip_save tsc_scale vmcb_clean flushbyasid decodeassists pausefilter pfthreshold v_vmsave_vmload umip vaes vpclmulqdq rdpid fsrm
    Virtualization:                          AMD-V
    Hypervisor vendor:                       Microsoft
    Virtualization type:                     full
    L1d cache:                               64 KiB (2 instances)
    L1i cache:                               64 KiB (2 instances)
    L2 cache:                                1 MiB (2 instances)
    L3 cache:                                32 MiB (1 instance)
    NUMA node(s):                            1
    NUMA node0 CPU(s):                       0-3
    Vulnerability Gather data sampling:      Not affected
    Vulnerability Ghostwrite:                Not affected
    Vulnerability Indirect target selection: Not affected
    Vulnerability Itlb multihit:             Not affected
    Vulnerability L1tf:                      Not affected
    Vulnerability Mds:                       Not affected
    Vulnerability Meltdown:                  Not affected
    Vulnerability Mmio stale data:           Not affected
    Vulnerability Old microcode:             Not affected
    Vulnerability Reg file data sampling:    Not affected
    Vulnerability Retbleed:                  Not affected
    Vulnerability Spec rstack overflow:      Vulnerable: Safe RET, no microcode
    Vulnerability Spec store bypass:         Vulnerable
    Vulnerability Spectre v1:                Mitigation; usercopy/swapgs barriers and __user pointer sanitization
    Vulnerability Spectre v2:                Mitigation; Retpolines; STIBP disabled; RSB filling; PBRSB-eIBRS Not affected; BHI Not affected
    Vulnerability Srbds:                     Not affected
    Vulnerability Tsa:                       Vulnerable: No microcode
    Vulnerability Tsx async abort:           Not affected
    Vulnerability Vmscape:                   Not affected
    

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

