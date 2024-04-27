# Multi-thread benchmark result

* Pull request commit: [`af6a4bf4f47da13b0f11513b6562a2880d5d345a`](https://github.com/JuliaFolds/Transducers.jl/commit/af6a4bf4f47da13b0f11513b6562a2880d5d345a)
* Pull request: <https://github.com/JuliaFolds/Transducers.jl/pull/243> (Update */Manifest.toml)

# Judge result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmarks:
    - Target: 27 Apr 2024 - 01:23
    - Baseline: 27 Apr 2024 - 01:28
* Package commits:
    - Target: b5e166
    - Baseline: 2a51f8
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
| `["findfirst", "n=1000", "reduce", "basesize=128"]` |                   0.98 (5%)  | 0.96 (1%) :white_check_mark: |
| `["findfirst", "n=1000", "reduce", "basesize=256"]` |                1.10 (5%) :x: |                1.06 (1%) :x: |
| `["findfirst", "n=1000", "reduce", "basesize=512"]` |                1.70 (5%) :x: |                1.56 (1%) :x: |
| `["findfirst", "n=400", "reduce", "basesize=128"]`  |                   1.03 (5%)  |                1.03 (1%) :x: |
| `["findfirst", "n=400", "reduce", "basesize=512"]`  |                   0.96 (5%)  | 0.95 (1%) :white_check_mark: |
| `["findfirst", "n=500", "reduce", "basesize=128"]`  |                   1.03 (5%)  |                1.04 (1%) :x: |
| `["findfirst", "n=500", "reduce", "basesize=256"]`  |                1.94 (5%) :x: |                1.71 (1%) :x: |
| `["findfirst", "n=500", "reduce", "basesize=512"]`  | 0.89 (5%) :white_check_mark: | 0.86 (1%) :white_check_mark: |
| `["parallel_histogram", "assoc", "basesize=4096"]`  |                   0.98 (5%)  | 0.87 (1%) :white_check_mark: |
| `["parallel_histogram", "comm", "basesize=16384"]`  |                1.09 (5%) :x: |                   1.01 (1%)  |
| `["parallel_histogram", "comm", "basesize=4096"]`   | 0.85 (5%) :white_check_mark: | 0.96 (1%) :white_check_mark: |
| `["parallel_histogram", "comm", "basesize=8192"]`   |                   1.00 (5%)  |                1.01 (1%) :x: |
| `["splitby", "count", "reduce"]`                    |                   0.99 (5%)  |                1.03 (1%) :x: |
| `["words", "nthreads=2"]`                           |                   0.95 (5%)  | 0.99 (1%) :white_check_mark: |

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
      Ubuntu 22.04.4 LTS
  uname: Linux 6.5.0-1018-azure #19~22.04.2-Ubuntu SMP Thu Mar 21 16:45:46 UTC 2024 x86_64 x86_64
  CPU: AMD EPYC 7763 64-Core Processor: 
              speed         user         nice          sys         idle          irq
       #1  2445 MHz       2426 s          0 s        157 s       4787 s          0 s
       #2  3244 MHz       2212 s          0 s        159 s       5007 s          0 s
       #3  2559 MHz       2579 s          0 s        170 s       4625 s          0 s
       #4  2445 MHz       2854 s          0 s        178 s       4336 s          0 s
       
  Memory: 15.606494903564453 GB (12481.97265625 MB free)
  Uptime: 740.75 sec
  Load Avg:  1.72  1.5  0.88
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
      Ubuntu 22.04.4 LTS
  uname: Linux 6.5.0-1018-azure #19~22.04.2-Ubuntu SMP Thu Mar 21 16:45:46 UTC 2024 x86_64 x86_64
  CPU: AMD EPYC 7763 64-Core Processor: 
              speed         user         nice          sys         idle          irq
       #1  3243 MHz       3395 s          0 s        204 s       6667 s          0 s
       #2  3243 MHz       3768 s          0 s        214 s       6294 s          0 s
       #3  2589 MHz       3509 s          0 s        219 s       6544 s          0 s
       #4  2913 MHz       3990 s          0 s        228 s       6048 s          0 s
       
  Memory: 15.606494903564453 GB (12469.73046875 MB free)
  Uptime: 1030.97 sec
  Load Avg:  1.56  1.57  1.08
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-12.0.1 (ORCJIT, znver3)
```

---
# Target result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmark: 27 Apr 2024 - 1:23
* Package commit: b5e166
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
| `["collect", "assoc", "basesize=1"]`                | 148.755 ms (5%) |         |   4.36 MiB (1%) |       32800 |
| `["collect", "assoc", "basesize=1024"]`             | 147.415 ms (5%) |         |   1.09 MiB (1%) |          53 |
| `["collect", "assoc", "basesize=32"]`               | 147.545 ms (5%) |         |   1.48 MiB (1%) |        1052 |
| `["collect", "seq"]`                                | 294.552 ms (5%) |         | 256.05 KiB (1%) |           2 |
| `["collect", "unordered", "basesize=1"]`            | 244.339 ms (5%) |         |  23.80 MiB (1%) |      409716 |
| `["collect", "unordered", "basesize=1024"]`         | 155.894 ms (5%) |         |   1.01 MiB (1%) |        1046 |
| `["collect", "unordered", "basesize=32"]`           | 163.100 ms (5%) |         |   1.59 MiB (1%) |       15022 |
| `["findfirst", "n=1000", "foldl"]`                  | 507.498 ms (5%) |         |                 |             |
| `["findfirst", "n=1000", "reduce", "basesize=128"]` | 276.223 ms (5%) |         | 232.86 KiB (1%) |        3276 |
| `["findfirst", "n=1000", "reduce", "basesize=256"]` | 371.828 ms (5%) |         | 167.05 KiB (1%) |        2336 |
| `["findfirst", "n=1000", "reduce", "basesize=512"]` | 589.140 ms (5%) |         | 126.88 KiB (1%) |        1793 |
| `["findfirst", "n=400", "foldl"]`                   | 378.749 ms (5%) |         |                 |             |
| `["findfirst", "n=400", "reduce", "basesize=128"]`  | 199.062 ms (5%) |         | 389.80 KiB (1%) |        5547 |
| `["findfirst", "n=400", "reduce", "basesize=256"]`  | 198.479 ms (5%) |         | 200.86 KiB (1%) |        2873 |
| `["findfirst", "n=400", "reduce", "basesize=512"]`  | 210.850 ms (5%) |         | 107.16 KiB (1%) |        1551 |
| `["findfirst", "n=500", "foldl"]`                   |  64.946 ms (5%) |         |                 |             |
| `["findfirst", "n=500", "reduce", "basesize=128"]`  | 122.514 ms (5%) |         | 230.92 KiB (1%) |        3171 |
| `["findfirst", "n=500", "reduce", "basesize=256"]`  | 160.865 ms (5%) |         | 154.08 KiB (1%) |        2121 |
| `["findfirst", "n=500", "reduce", "basesize=512"]`  |  67.086 ms (5%) |         |  49.59 KiB (1%) |         671 |
| `["overhead", "default"]`                           |  50.795 μs (5%) |         |  32.70 KiB (1%) |         417 |
| `["overhead", "stoppable=false"]`                   |  51.606 μs (5%) |         |  32.72 KiB (1%) |         417 |
| `["overhead", "stoppable=true"]`                    |  58.539 μs (5%) |         |  44.28 KiB (1%) |         611 |
| `["parallel_histogram", "assoc", "basesize=16384"]` |   2.392 ms (5%) |         | 728.91 KiB (1%) |          57 |
| `["parallel_histogram", "assoc", "basesize=4096"]`  |   2.917 ms (5%) |         |   1.79 MiB (1%) |         216 |
| `["parallel_histogram", "assoc", "basesize=8192"]`  |   2.650 ms (5%) |         |   1.42 MiB (1%) |         117 |
| `["parallel_histogram", "comm", "basesize=16384"]`  |   8.544 ms (5%) |         |   1.57 MiB (1%) |        2005 |
| `["parallel_histogram", "comm", "basesize=4096"]`   |  12.328 ms (5%) |         |   1.30 MiB (1%) |        8615 |
| `["parallel_histogram", "comm", "basesize=8192"]`   |  11.963 ms (5%) |         |   1.28 MiB (1%) |        7520 |
| `["parallel_histogram", "seq"]`                     |   4.244 ms (5%) |         | 364.16 KiB (1%) |          24 |
| `["partition_length_maximum", "rand", "foldl"]`     |  31.113 ms (5%) |         |                 |             |
| `["partition_length_maximum", "rand", "reduce"]`    |  15.588 ms (5%) |         |  736 bytes (1%) |          11 |
| `["splitby", "count", "foldl"]`                     |   1.501 ms (5%) |         |                 |             |
| `["splitby", "count", "man"]`                       |   1.157 ms (5%) |         |                 |             |
| `["splitby", "count", "reduce"]`                    | 718.112 μs (5%) |         |   1.09 KiB (1%) |          18 |
| `["sum", "random", "foldl"]`                        |  11.036 ms (5%) |         |                 |             |
| `["sum", "random", "reduce", "basesize=128"]`       |   5.657 ms (5%) |         |  74.14 KiB (1%) |        1103 |
| `["sum", "random", "reduce", "basesize=256"]`       |   5.592 ms (5%) |         |  36.73 KiB (1%) |         546 |
| `["sum", "random", "reduce", "basesize=512"]`       |   5.563 ms (5%) |         |  18.08 KiB (1%) |         269 |
| `["sum", "uniform", "foldl"]`                       |  10.862 ms (5%) |         |                 |             |
| `["sum", "uniform", "reduce", "basesize=128"]`      |   5.561 ms (5%) |         |  74.11 KiB (1%) |        1102 |
| `["sum", "uniform", "reduce", "basesize=256"]`      |   5.501 ms (5%) |         |  36.73 KiB (1%) |         546 |
| `["sum", "uniform", "reduce", "basesize=512"]`      |   5.468 ms (5%) |         |  18.03 KiB (1%) |         268 |
| `["sum", "valley", "foldl"]`                        |  11.104 ms (5%) |         |                 |             |
| `["sum", "valley", "reduce", "basesize=128"]`       |   5.683 ms (5%) |         |  74.08 KiB (1%) |        1101 |
| `["sum", "valley", "reduce", "basesize=256"]`       |   5.634 ms (5%) |         |  36.70 KiB (1%) |         545 |
| `["sum", "valley", "reduce", "basesize=512"]`       |   5.614 ms (5%) |         |  18.06 KiB (1%) |         269 |
| `["words", "nthreads=1"]`                           |  14.151 ms (5%) |         |  31.80 MiB (1%) |     1035658 |
| `["words", "nthreads=2"]`                           |   9.419 ms (5%) |         |  32.15 MiB (1%) |     1035710 |
| `["words", "nthreads=4"]`                           |  10.065 ms (5%) |         |  33.05 MiB (1%) |     1035893 |

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
      Ubuntu 22.04.4 LTS
  uname: Linux 6.5.0-1018-azure #19~22.04.2-Ubuntu SMP Thu Mar 21 16:45:46 UTC 2024 x86_64 x86_64
  CPU: AMD EPYC 7763 64-Core Processor: 
              speed         user         nice          sys         idle          irq
       #1  2445 MHz       2426 s          0 s        157 s       4787 s          0 s
       #2  3244 MHz       2212 s          0 s        159 s       5007 s          0 s
       #3  2559 MHz       2579 s          0 s        170 s       4625 s          0 s
       #4  2445 MHz       2854 s          0 s        178 s       4336 s          0 s
       
  Memory: 15.606494903564453 GB (12481.97265625 MB free)
  Uptime: 740.75 sec
  Load Avg:  1.72  1.5  0.88
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-12.0.1 (ORCJIT, znver3)
```

---
# Baseline result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmark: 27 Apr 2024 - 1:28
* Package commit: 2a51f8
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
| `["collect", "assoc", "basesize=1"]`                | 149.045 ms (5%) |         |   4.36 MiB (1%) |       32800 |
| `["collect", "assoc", "basesize=1024"]`             | 147.605 ms (5%) |         |   1.09 MiB (1%) |          54 |
| `["collect", "assoc", "basesize=32"]`               | 147.538 ms (5%) |         |   1.48 MiB (1%) |        1052 |
| `["collect", "seq"]`                                | 294.645 ms (5%) |         | 256.05 KiB (1%) |           2 |
| `["collect", "unordered", "basesize=1"]`            | 243.138 ms (5%) |         |  23.82 MiB (1%) |      410262 |
| `["collect", "unordered", "basesize=1024"]`         | 156.067 ms (5%) |         |   1.01 MiB (1%) |        1114 |
| `["collect", "unordered", "basesize=32"]`           | 162.873 ms (5%) |         |   1.59 MiB (1%) |       14988 |
| `["findfirst", "n=1000", "foldl"]`                  | 506.930 ms (5%) |         |                 |             |
| `["findfirst", "n=1000", "reduce", "basesize=128"]` | 282.760 ms (5%) |         | 241.44 KiB (1%) |        3382 |
| `["findfirst", "n=1000", "reduce", "basesize=256"]` | 339.323 ms (5%) |         | 157.20 KiB (1%) |        2193 |
| `["findfirst", "n=1000", "reduce", "basesize=512"]` | 346.813 ms (5%) |         |  81.33 KiB (1%) |        1146 |
| `["findfirst", "n=400", "foldl"]`                   | 378.936 ms (5%) |         |                 |             |
| `["findfirst", "n=400", "reduce", "basesize=128"]`  | 192.993 ms (5%) |         | 377.61 KiB (1%) |        5383 |
| `["findfirst", "n=400", "reduce", "basesize=256"]`  | 197.617 ms (5%) |         | 198.88 KiB (1%) |        2854 |
| `["findfirst", "n=400", "reduce", "basesize=512"]`  | 220.464 ms (5%) |         | 112.56 KiB (1%) |        1621 |
| `["findfirst", "n=500", "foldl"]`                   |  65.904 ms (5%) |         |                 |             |
| `["findfirst", "n=500", "reduce", "basesize=128"]`  | 119.409 ms (5%) |         | 222.98 KiB (1%) |        3036 |
| `["findfirst", "n=500", "reduce", "basesize=256"]`  |  82.949 ms (5%) |         |  90.16 KiB (1%) |        1242 |
| `["findfirst", "n=500", "reduce", "basesize=512"]`  |  75.179 ms (5%) |         |  57.77 KiB (1%) |         770 |
| `["overhead", "default"]`                           |  49.462 μs (5%) |         |  32.73 KiB (1%) |         418 |
| `["overhead", "stoppable=false"]`                   |  49.182 μs (5%) |         |  32.75 KiB (1%) |         418 |
| `["overhead", "stoppable=true"]`                    |  58.980 μs (5%) |         |  44.25 KiB (1%) |         610 |
| `["parallel_histogram", "assoc", "basesize=16384"]` |   2.377 ms (5%) |         | 728.91 KiB (1%) |          57 |
| `["parallel_histogram", "assoc", "basesize=4096"]`  |   2.990 ms (5%) |         |   2.05 MiB (1%) |         222 |
| `["parallel_histogram", "assoc", "basesize=8192"]`  |   2.654 ms (5%) |         |   1.42 MiB (1%) |         117 |
| `["parallel_histogram", "comm", "basesize=16384"]`  |   7.809 ms (5%) |         |   1.56 MiB (1%) |        1742 |
| `["parallel_histogram", "comm", "basesize=4096"]`   |  14.482 ms (5%) |         |   1.36 MiB (1%) |       10598 |
| `["parallel_histogram", "comm", "basesize=8192"]`   |  11.977 ms (5%) |         |   1.27 MiB (1%) |        7676 |
| `["parallel_histogram", "seq"]`                     |   4.244 ms (5%) |         | 364.16 KiB (1%) |          24 |
| `["partition_length_maximum", "rand", "foldl"]`     |  31.115 ms (5%) |         |                 |             |
| `["partition_length_maximum", "rand", "reduce"]`    |  15.566 ms (5%) |         |  736 bytes (1%) |          11 |
| `["splitby", "count", "foldl"]`                     |   1.539 ms (5%) |         |                 |             |
| `["splitby", "count", "man"]`                       |   1.157 ms (5%) |         |                 |             |
| `["splitby", "count", "reduce"]`                    | 721.769 μs (5%) |         |   1.06 KiB (1%) |          19 |
| `["sum", "random", "foldl"]`                        |  10.982 ms (5%) |         |                 |             |
| `["sum", "random", "reduce", "basesize=128"]`       |   5.590 ms (5%) |         |  74.20 KiB (1%) |        1105 |
| `["sum", "random", "reduce", "basesize=256"]`       |   5.562 ms (5%) |         |  36.67 KiB (1%) |         544 |
| `["sum", "random", "reduce", "basesize=512"]`       |   5.533 ms (5%) |         |  18.08 KiB (1%) |         269 |
| `["sum", "uniform", "foldl"]`                       |  10.861 ms (5%) |         |                 |             |
| `["sum", "uniform", "reduce", "basesize=128"]`      |   5.559 ms (5%) |         |  74.14 KiB (1%) |        1103 |
| `["sum", "uniform", "reduce", "basesize=256"]`      |   5.504 ms (5%) |         |  36.73 KiB (1%) |         546 |
| `["sum", "uniform", "reduce", "basesize=512"]`      |   5.468 ms (5%) |         |  18.03 KiB (1%) |         268 |
| `["sum", "valley", "foldl"]`                        |  11.106 ms (5%) |         |                 |             |
| `["sum", "valley", "reduce", "basesize=128"]`       |   5.692 ms (5%) |         |  74.08 KiB (1%) |        1101 |
| `["sum", "valley", "reduce", "basesize=256"]`       |   5.631 ms (5%) |         |  36.70 KiB (1%) |         545 |
| `["sum", "valley", "reduce", "basesize=512"]`       |   5.607 ms (5%) |         |  18.06 KiB (1%) |         269 |
| `["words", "nthreads=1"]`                           |  14.610 ms (5%) |         |  31.80 MiB (1%) |     1035963 |
| `["words", "nthreads=2"]`                           |   9.876 ms (5%) |         |  32.51 MiB (1%) |     1036036 |
| `["words", "nthreads=4"]`                           |  10.244 ms (5%) |         |  33.14 MiB (1%) |     1036252 |

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
      Ubuntu 22.04.4 LTS
  uname: Linux 6.5.0-1018-azure #19~22.04.2-Ubuntu SMP Thu Mar 21 16:45:46 UTC 2024 x86_64 x86_64
  CPU: AMD EPYC 7763 64-Core Processor: 
              speed         user         nice          sys         idle          irq
       #1  3243 MHz       3395 s          0 s        204 s       6667 s          0 s
       #2  3243 MHz       3768 s          0 s        214 s       6294 s          0 s
       #3  2589 MHz       3509 s          0 s        219 s       6544 s          0 s
       #4  2913 MHz       3990 s          0 s        228 s       6048 s          0 s
       
  Memory: 15.606494903564453 GB (12469.73046875 MB free)
  Uptime: 1030.97 sec
  Load Avg:  1.56  1.57  1.08
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

    Architecture:                       x86_64
    CPU op-mode(s):                     32-bit, 64-bit
    Address sizes:                      48 bits physical, 48 bits virtual
    Byte Order:                         Little Endian
    CPU(s):                             4
    On-line CPU(s) list:                0-3
    Vendor ID:                          AuthenticAMD
    Model name:                         AMD EPYC 7763 64-Core Processor
    CPU family:                         25
    Model:                              1
    Thread(s) per core:                 2
    Core(s) per socket:                 2
    Socket(s):                          1
    Stepping:                           1
    BogoMIPS:                           4890.87
    Flags:                              fpu vme de pse tsc msr pae mce cx8 apic sep mtrr pge mca cmov pat pse36 clflush mmx fxsr sse sse2 ht syscall nx mmxext fxsr_opt pdpe1gb rdtscp lm constant_tsc rep_good nopl tsc_reliable nonstop_tsc cpuid extd_apicid aperfmperf pni pclmulqdq ssse3 fma cx16 pcid sse4_1 sse4_2 movbe popcnt aes xsave avx f16c rdrand hypervisor lahf_lm cmp_legacy svm cr8_legacy abm sse4a misalignsse 3dnowprefetch osvw topoext invpcid_single vmmcall fsgsbase bmi1 avx2 smep bmi2 erms invpcid rdseed adx smap clflushopt clwb sha_ni xsaveopt xsavec xgetbv1 xsaves clzero xsaveerptr rdpru arat npt nrip_save tsc_scale vmcb_clean flushbyasid decodeassists pausefilter pfthreshold v_vmsave_vmload umip vaes vpclmulqdq rdpid fsrm
    Virtualization:                     AMD-V
    Hypervisor vendor:                  Microsoft
    Virtualization type:                full
    L1d cache:                          64 KiB (2 instances)
    L1i cache:                          64 KiB (2 instances)
    L2 cache:                           1 MiB (2 instances)
    L3 cache:                           32 MiB (1 instance)
    NUMA node(s):                       1
    NUMA node0 CPU(s):                  0-3
    Vulnerability Gather data sampling: Not affected
    Vulnerability Itlb multihit:        Not affected
    Vulnerability L1tf:                 Not affected
    Vulnerability Mds:                  Not affected
    Vulnerability Meltdown:             Not affected
    Vulnerability Mmio stale data:      Not affected
    Vulnerability Retbleed:             Not affected
    Vulnerability Spec rstack overflow: Vulnerable: Safe RET, no microcode
    Vulnerability Spec store bypass:    Vulnerable
    Vulnerability Spectre v1:           Mitigation; usercopy/swapgs barriers and __user pointer sanitization
    Vulnerability Spectre v2:           Mitigation; Retpolines, STIBP disabled, RSB filling, PBRSB-eIBRS Not affected
    Vulnerability Srbds:                Not affected
    Vulnerability Tsx async abort:      Not affected
    

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

