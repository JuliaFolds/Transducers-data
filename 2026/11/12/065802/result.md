# Multi-thread benchmark result

* Pull request commit: [`0ee5ee6919ab64426ec6949834131e6cc062eb6d`](https://github.com/JuliaFolds/Transducers.jl/commit/0ee5ee6919ab64426ec6949834131e6cc062eb6d)
* Pull request: <https://github.com/JuliaFolds/Transducers.jl/pull/243> (Update */Manifest.toml)

# Judge result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmarks:
    - Target: 12 Nov 2026 - 06:52
    - Baseline: 12 Nov 2026 - 06:57
* Package commits:
    - Target: 3d21f39
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
| `["findfirst", "n=1000", "reduce", "basesize=128"]` |                1.47 (5%) :x: |                1.42 (1%) :x: |
| `["findfirst", "n=1000", "reduce", "basesize=256"]` | 0.94 (5%) :white_check_mark: | 0.92 (1%) :white_check_mark: |
| `["findfirst", "n=1000", "reduce", "basesize=512"]` | 0.94 (5%) :white_check_mark: | 0.92 (1%) :white_check_mark: |
| `["findfirst", "n=400", "reduce", "basesize=128"]`  |                   0.99 (5%)  | 0.98 (1%) :white_check_mark: |
| `["findfirst", "n=400", "reduce", "basesize=512"]`  |                1.06 (5%) :x: |                   1.00 (1%)  |
| `["findfirst", "n=500", "reduce", "basesize=128"]`  | 0.55 (5%) :white_check_mark: | 0.62 (1%) :white_check_mark: |
| `["findfirst", "n=500", "reduce", "basesize=256"]`  | 0.44 (5%) :white_check_mark: | 0.50 (1%) :white_check_mark: |
| `["findfirst", "n=500", "reduce", "basesize=512"]`  |                1.16 (5%) :x: |                1.06 (1%) :x: |
| `["parallel_histogram", "comm", "basesize=16384"]`  | 0.94 (5%) :white_check_mark: | 0.76 (1%) :white_check_mark: |
| `["parallel_histogram", "comm", "basesize=4096"]`   |                   0.99 (5%)  |                1.02 (1%) :x: |
| `["parallel_histogram", "comm", "basesize=8192"]`   |                   0.99 (5%)  | 0.91 (1%) :white_check_mark: |
| `["splitby", "count", "foldl"]`                     |                1.07 (5%) :x: |                   1.00 (1%)  |
| `["splitby", "count", "reduce"]`                    | 0.89 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["words", "nthreads=2"]`                           | 0.95 (5%) :white_check_mark: |                1.01 (1%) :x: |

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
      Ubuntu 26.04.1 LTS
  uname: Linux 7.0.0-1019-azure #20-Ubuntu SMP PREEMPT Mon Oct 19 22:41:16 UTC 2026 x86_64 unknown
  CPU: AMD EPYC 9V45 96-Core Processor: 
              speed         user         nice          sys         idle          irq
       #1  4529 MHz       1909 s          0 s        157 s       4091 s          0 s
       #2  4520 MHz       2929 s          0 s        161 s       3062 s          0 s
       #3  4532 MHz       2266 s          0 s        158 s       3729 s          0 s
       #4  4549 MHz       2361 s          0 s        159 s       3608 s          0 s
       
  Memory: 15.608440399169922 GB (13201.671875 MB free)
  Uptime: 620.02 sec
  Load Avg:  1.87  1.66  0.94
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-12.0.1 (ORCJIT, generic)
```

### Baseline
```
Julia Version 1.7.3
Commit 742b9abb4d (2022-05-06 12:58 UTC)
Platform Info:
  OS: Linux (x86_64-pc-linux-gnu)
      Ubuntu 26.04.1 LTS
  uname: Linux 7.0.0-1019-azure #20-Ubuntu SMP PREEMPT Mon Oct 19 22:41:16 UTC 2026 x86_64 unknown
  CPU: AMD EPYC 9V45 96-Core Processor: 
              speed         user         nice          sys         idle          irq
       #1  4536 MHz       3024 s          0 s        212 s       5748 s          0 s
       #2  4537 MHz       4052 s          0 s        224 s       4703 s          0 s
       #3  4532 MHz       3199 s          0 s        211 s       5571 s          0 s
       #4  4535 MHz       3696 s          0 s        219 s       5043 s          0 s
       
  Memory: 15.608440399169922 GB (13156.2734375 MB free)
  Uptime: 903.22 sec
  Load Avg:  1.91  1.76  1.17
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-12.0.1 (ORCJIT, generic)
```

---
# Target result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmark: 12 Nov 2026 - 06:52
* Package commit: 3d21f39
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
| `["collect", "assoc", "basesize=1"]`                | 101.583 ms (5%) |         |   4.36 MiB (1%) |       32800 |
| `["collect", "assoc", "basesize=1024"]`             | 100.874 ms (5%) |         |   1.09 MiB (1%) |          53 |
| `["collect", "assoc", "basesize=32"]`               | 100.892 ms (5%) |         |   1.48 MiB (1%) |        1052 |
| `["collect", "seq"]`                                | 201.579 ms (5%) |         | 256.05 KiB (1%) |           2 |
| `["collect", "unordered", "basesize=1"]`            | 164.901 ms (5%) |         |  23.68 MiB (1%) |      405745 |
| `["collect", "unordered", "basesize=1024"]`         | 104.547 ms (5%) |         |   1.01 MiB (1%) |        1140 |
| `["collect", "unordered", "basesize=32"]`           | 108.681 ms (5%) |         |   1.59 MiB (1%) |       14857 |
| `["findfirst", "n=1000", "foldl"]`                  | 340.979 ms (5%) |         |                 |             |
| `["findfirst", "n=1000", "reduce", "basesize=128"]` | 274.671 ms (5%) |         | 329.69 KiB (1%) |        4622 |
| `["findfirst", "n=1000", "reduce", "basesize=256"]` | 251.278 ms (5%) |         | 161.80 KiB (1%) |        2279 |
| `["findfirst", "n=1000", "reduce", "basesize=512"]` | 221.593 ms (5%) |         |  76.53 KiB (1%) |        1081 |
| `["findfirst", "n=400", "foldl"]`                   | 256.442 ms (5%) |         |                 |             |
| `["findfirst", "n=400", "reduce", "basesize=128"]`  | 131.472 ms (5%) |         | 382.25 KiB (1%) |        5439 |
| `["findfirst", "n=400", "reduce", "basesize=256"]`  | 132.669 ms (5%) |         | 200.92 KiB (1%) |        2874 |
| `["findfirst", "n=400", "reduce", "basesize=512"]`  | 148.796 ms (5%) |         | 112.59 KiB (1%) |        1622 |
| `["findfirst", "n=500", "foldl"]`                   |  44.284 ms (5%) |         |                 |             |
| `["findfirst", "n=500", "reduce", "basesize=128"]`  |  28.849 ms (5%) |         |  96.89 KiB (1%) |        1321 |
| `["findfirst", "n=500", "reduce", "basesize=256"]`  |  44.710 ms (5%) |         |  76.92 KiB (1%) |        1051 |
| `["findfirst", "n=500", "reduce", "basesize=512"]`  |  53.784 ms (5%) |         |  52.56 KiB (1%) |         712 |
| `["overhead", "default"]`                           |  35.293 μs (5%) |         |  32.77 KiB (1%) |         419 |
| `["overhead", "stoppable=false"]`                   |  35.854 μs (5%) |         |  32.75 KiB (1%) |         418 |
| `["overhead", "stoppable=true"]`                    |  40.841 μs (5%) |         |  44.28 KiB (1%) |         611 |
| `["parallel_histogram", "assoc", "basesize=16384"]` |   1.522 ms (5%) |         | 728.91 KiB (1%) |          57 |
| `["parallel_histogram", "assoc", "basesize=4096"]`  |   1.988 ms (5%) |         |   1.79 MiB (1%) |         216 |
| `["parallel_histogram", "assoc", "basesize=8192"]`  |   1.756 ms (5%) |         |   1.42 MiB (1%) |         118 |
| `["parallel_histogram", "comm", "basesize=16384"]`  |   4.862 ms (5%) |         |   1.16 MiB (1%) |         136 |
| `["parallel_histogram", "comm", "basesize=4096"]`   |   9.196 ms (5%) |         |   1.35 MiB (1%) |       10290 |
| `["parallel_histogram", "comm", "basesize=8192"]`   |   8.653 ms (5%) |         |   1.37 MiB (1%) |        6084 |
| `["parallel_histogram", "seq"]`                     |   2.680 ms (5%) |         | 364.16 KiB (1%) |          24 |
| `["partition_length_maximum", "rand", "foldl"]`     |  29.754 ms (5%) |         |                 |             |
| `["partition_length_maximum", "rand", "reduce"]`    |  14.890 ms (5%) |         |  736 bytes (1%) |          11 |
| `["splitby", "count", "foldl"]`                     |   1.272 ms (5%) |         |                 |             |
| `["splitby", "count", "man"]`                       | 693.227 μs (5%) |         |                 |             |
| `["splitby", "count", "reduce"]`                    | 545.173 μs (5%) |         |   1.06 KiB (1%) |          18 |
| `["sum", "random", "foldl"]`                        |   7.742 ms (5%) |         |                 |             |
| `["sum", "random", "reduce", "basesize=128"]`       |   3.963 ms (5%) |         |  74.19 KiB (1%) |        1104 |
| `["sum", "random", "reduce", "basesize=256"]`       |   3.918 ms (5%) |         |  36.78 KiB (1%) |         547 |
| `["sum", "random", "reduce", "basesize=512"]`       |   3.899 ms (5%) |         |  18.08 KiB (1%) |         269 |
| `["sum", "uniform", "foldl"]`                       |   7.501 ms (5%) |         |                 |             |
| `["sum", "uniform", "reduce", "basesize=128"]`      |   3.846 ms (5%) |         |  74.12 KiB (1%) |        1102 |
| `["sum", "uniform", "reduce", "basesize=256"]`      |   3.803 ms (5%) |         |  36.78 KiB (1%) |         547 |
| `["sum", "uniform", "reduce", "basesize=512"]`      |   3.780 ms (5%) |         |  18.02 KiB (1%) |         267 |
| `["sum", "valley", "foldl"]`                        |   7.791 ms (5%) |         |                 |             |
| `["sum", "valley", "reduce", "basesize=128"]`       |   3.986 ms (5%) |         |  74.09 KiB (1%) |        1101 |
| `["sum", "valley", "reduce", "basesize=256"]`       |   3.944 ms (5%) |         |  36.78 KiB (1%) |         547 |
| `["sum", "valley", "reduce", "basesize=512"]`       |   3.931 ms (5%) |         |  18.11 KiB (1%) |         270 |
| `["words", "nthreads=1"]`                           |   8.336 ms (5%) |         |  31.98 MiB (1%) |     1042227 |
| `["words", "nthreads=2"]`                           |   5.624 ms (5%) |         |  32.70 MiB (1%) |     1042325 |
| `["words", "nthreads=4"]`                           |   6.146 ms (5%) |         |  33.33 MiB (1%) |     1042468 |

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
      Ubuntu 26.04.1 LTS
  uname: Linux 7.0.0-1019-azure #20-Ubuntu SMP PREEMPT Mon Oct 19 22:41:16 UTC 2026 x86_64 unknown
  CPU: AMD EPYC 9V45 96-Core Processor: 
              speed         user         nice          sys         idle          irq
       #1  4529 MHz       1909 s          0 s        157 s       4091 s          0 s
       #2  4520 MHz       2929 s          0 s        161 s       3062 s          0 s
       #3  4532 MHz       2266 s          0 s        158 s       3729 s          0 s
       #4  4549 MHz       2361 s          0 s        159 s       3608 s          0 s
       
  Memory: 15.608440399169922 GB (13201.671875 MB free)
  Uptime: 620.02 sec
  Load Avg:  1.87  1.66  0.94
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-12.0.1 (ORCJIT, generic)
```

---
# Baseline result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmark: 12 Nov 2026 - 06:57
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
| `["collect", "assoc", "basesize=1"]`                | 101.444 ms (5%) |         |   4.36 MiB (1%) |       32800 |
| `["collect", "assoc", "basesize=1024"]`             | 100.980 ms (5%) |         |   1.09 MiB (1%) |          53 |
| `["collect", "assoc", "basesize=32"]`               | 100.904 ms (5%) |         |   1.48 MiB (1%) |        1052 |
| `["collect", "seq"]`                                | 201.558 ms (5%) |         | 256.05 KiB (1%) |           2 |
| `["collect", "unordered", "basesize=1"]`            | 164.942 ms (5%) |         |  23.72 MiB (1%) |      407137 |
| `["collect", "unordered", "basesize=1024"]`         | 104.632 ms (5%) |         |   1.01 MiB (1%) |        1088 |
| `["collect", "unordered", "basesize=32"]`           | 108.878 ms (5%) |         |   1.59 MiB (1%) |       15047 |
| `["findfirst", "n=1000", "foldl"]`                  | 341.837 ms (5%) |         |                 |             |
| `["findfirst", "n=1000", "reduce", "basesize=128"]` | 186.397 ms (5%) |         | 232.86 KiB (1%) |        3276 |
| `["findfirst", "n=1000", "reduce", "basesize=256"]` | 266.715 ms (5%) |         | 175.67 KiB (1%) |        2449 |
| `["findfirst", "n=1000", "reduce", "basesize=512"]` | 234.582 ms (5%) |         |  83.53 KiB (1%) |        1176 |
| `["findfirst", "n=400", "foldl"]`                   | 255.925 ms (5%) |         |                 |             |
| `["findfirst", "n=400", "reduce", "basesize=128"]`  | 132.947 ms (5%) |         | 390.28 KiB (1%) |        5548 |
| `["findfirst", "n=400", "reduce", "basesize=256"]`  | 134.032 ms (5%) |         | 200.98 KiB (1%) |        2877 |
| `["findfirst", "n=400", "reduce", "basesize=512"]`  | 139.752 ms (5%) |         | 112.89 KiB (1%) |        1617 |
| `["findfirst", "n=500", "foldl"]`                   |  44.399 ms (5%) |         |                 |             |
| `["findfirst", "n=500", "reduce", "basesize=128"]`  |  52.828 ms (5%) |         | 156.84 KiB (1%) |        2142 |
| `["findfirst", "n=500", "reduce", "basesize=256"]`  | 101.056 ms (5%) |         | 155.06 KiB (1%) |        2126 |
| `["findfirst", "n=500", "reduce", "basesize=512"]`  |  46.171 ms (5%) |         |  49.42 KiB (1%) |         668 |
| `["overhead", "default"]`                           |  36.395 μs (5%) |         |  32.70 KiB (1%) |         417 |
| `["overhead", "stoppable=false"]`                   |  35.273 μs (5%) |         |  32.78 KiB (1%) |         419 |
| `["overhead", "stoppable=true"]`                    |  40.782 μs (5%) |         |  44.28 KiB (1%) |         611 |
| `["parallel_histogram", "assoc", "basesize=16384"]` |   1.530 ms (5%) |         | 728.91 KiB (1%) |          57 |
| `["parallel_histogram", "assoc", "basesize=4096"]`  |   1.999 ms (5%) |         |   1.79 MiB (1%) |         216 |
| `["parallel_histogram", "assoc", "basesize=8192"]`  |   1.754 ms (5%) |         |   1.42 MiB (1%) |         117 |
| `["parallel_histogram", "comm", "basesize=16384"]`  |   5.163 ms (5%) |         |   1.51 MiB (1%) |         156 |
| `["parallel_histogram", "comm", "basesize=4096"]`   |   9.278 ms (5%) |         |   1.32 MiB (1%) |        9451 |
| `["parallel_histogram", "comm", "basesize=8192"]`   |   8.741 ms (5%) |         |   1.50 MiB (1%) |        6246 |
| `["parallel_histogram", "seq"]`                     |   2.690 ms (5%) |         | 364.16 KiB (1%) |          24 |
| `["partition_length_maximum", "rand", "foldl"]`     |  29.765 ms (5%) |         |                 |             |
| `["partition_length_maximum", "rand", "reduce"]`    |  14.895 ms (5%) |         |  736 bytes (1%) |          11 |
| `["splitby", "count", "foldl"]`                     |   1.187 ms (5%) |         |                 |             |
| `["splitby", "count", "man"]`                       | 696.212 μs (5%) |         |                 |             |
| `["splitby", "count", "reduce"]`                    | 610.502 μs (5%) |         |   1.06 KiB (1%) |          18 |
| `["sum", "random", "foldl"]`                        |   7.756 ms (5%) |         |                 |             |
| `["sum", "random", "reduce", "basesize=128"]`       |   3.971 ms (5%) |         |  74.09 KiB (1%) |        1101 |
| `["sum", "random", "reduce", "basesize=256"]`       |   3.927 ms (5%) |         |  36.78 KiB (1%) |         547 |
| `["sum", "random", "reduce", "basesize=512"]`       |   3.909 ms (5%) |         |  18.11 KiB (1%) |         270 |
| `["sum", "uniform", "foldl"]`                       |   7.524 ms (5%) |         |                 |             |
| `["sum", "uniform", "reduce", "basesize=128"]`      |   3.855 ms (5%) |         |  74.16 KiB (1%) |        1103 |
| `["sum", "uniform", "reduce", "basesize=256"]`      |   3.810 ms (5%) |         |  36.72 KiB (1%) |         545 |
| `["sum", "uniform", "reduce", "basesize=512"]`      |   3.788 ms (5%) |         |  18.08 KiB (1%) |         269 |
| `["sum", "valley", "foldl"]`                        |   7.806 ms (5%) |         |                 |             |
| `["sum", "valley", "reduce", "basesize=128"]`       |   3.981 ms (5%) |         |  74.12 KiB (1%) |        1102 |
| `["sum", "valley", "reduce", "basesize=256"]`       |   3.954 ms (5%) |         |  36.78 KiB (1%) |         547 |
| `["sum", "valley", "reduce", "basesize=512"]`       |   3.935 ms (5%) |         |  18.11 KiB (1%) |         270 |
| `["words", "nthreads=1"]`                           |   8.585 ms (5%) |         |  31.91 MiB (1%) |     1040176 |
| `["words", "nthreads=2"]`                           |   5.938 ms (5%) |         |  32.27 MiB (1%) |     1040212 |
| `["words", "nthreads=4"]`                           |   6.131 ms (5%) |         |  33.16 MiB (1%) |     1040398 |

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
      Ubuntu 26.04.1 LTS
  uname: Linux 7.0.0-1019-azure #20-Ubuntu SMP PREEMPT Mon Oct 19 22:41:16 UTC 2026 x86_64 unknown
  CPU: AMD EPYC 9V45 96-Core Processor: 
              speed         user         nice          sys         idle          irq
       #1  4536 MHz       3024 s          0 s        212 s       5748 s          0 s
       #2  4537 MHz       4052 s          0 s        224 s       4703 s          0 s
       #3  4532 MHz       3199 s          0 s        211 s       5571 s          0 s
       #4  4535 MHz       3696 s          0 s        219 s       5043 s          0 s
       
  Memory: 15.608440399169922 GB (13156.2734375 MB free)
  Uptime: 903.22 sec
  Load Avg:  1.91  1.76  1.17
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-12.0.1 (ORCJIT, generic)
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
    Model name:                              AMD EPYC 9V45 96-Core Processor
    CPU family:                              26
    Model:                                   2
    Thread(s) per core:                      2
    Core(s) per socket:                      2
    Socket(s):                               1
    Stepping:                                1
    BogoMIPS:                                5192.24
    Flags:                                   fpu vme de pse tsc msr pae mce cx8 apic sep mtrr pge mca cmov pat pse36 clflush mmx fxsr sse sse2 ht syscall nx mmxext fxsr_opt pdpe1gb rdtscp lm constant_tsc rep_good nopl xtopology tsc_reliable nonstop_tsc cpuid extd_apicid aperfmperf tsc_known_freq pni pclmulqdq ssse3 fma cx16 pcid sse4_1 sse4_2 x2apic movbe popcnt aes xsave avx f16c rdrand hypervisor lahf_lm cmp_legacy svm cr8_legacy abm sse4a misalignsse 3dnowprefetch osvw topoext vmmcall fsgsbase bmi1 avx2 smep bmi2 erms invpcid avx512f avx512dq rdseed adx smap avx512ifma clflushopt clwb avx512cd sha_ni avx512bw avx512vl xsaveopt xsavec xgetbv1 xsaves user_shstk avx_vnni avx512_bf16 clzero xsaveerptr rdpru arat npt nrip_save tsc_scale vmcb_clean flushbyasid decodeassists pausefilter pfthreshold v_vmsave_vmload avx512vbmi umip avx512_vbmi2 gfni vaes vpclmulqdq avx512_vnni avx512_bitalg avx512_vpopcntdq rdpid fsrm avx512_vp2intersect
    Virtualization:                          AMD-V
    Hypervisor vendor:                       Microsoft
    Virtualization type:                     full
    L1d cache:                               96 KiB (2 instances)
    L1i cache:                               64 KiB (2 instances)
    L2 cache:                                2 MiB (2 instances)
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
    Vulnerability Tsa:                       Not affected
    Vulnerability Tsx async abort:           Not affected
    Vulnerability Vmscape:                   Not affected
    

| Cpu Property       | Value                                                      |
|:------------------ |:---------------------------------------------------------- |
| Brand              | AMD EPYC 9V45 96-Core Processor                            |
| Vendor             | :AMD                                                       |
| Architecture       | :Unknown                                                   |
| Model              | Family: 0xbf, Model: 0x02, Stepping: 0x01, Type: 0x00      |
| Cores              | 8 physical cores, 16 logical cores (on executing CPU)      |
|                    | Hyperthreading hardware capability detected                |
| Clock Frequencies  | Not supported by CPU                                       |
| Data Cache         | Level 1:3 : (48, 1024, 32768) kbytes                       |
|                    | 64 byte cache line size                                    |
| Address Size       | 48 bits virtual, 48 bits physical                          |
| SIMD               | 512 bit = 64 byte max. SIMD vector size                    |
| Time Stamp Counter | TSC is accessible via `rdtsc`                              |
|                    | TSC runs at constant rate (invariant from clock frequency) |
| Perf. Monitoring   | Performance Monitoring Counters (PMC) are not supported    |
| Hypervisor         | Yes, Microsoft                                             |

