# Multi-thread benchmark result

* Pull request commit: [`827303019bc01945bfa146b85006b4522fb194b7`](https://github.com/JuliaFolds/Transducers.jl/commit/827303019bc01945bfa146b85006b4522fb194b7)
* Pull request: <https://github.com/JuliaFolds/Transducers.jl/pull/243> (Update */Manifest.toml)

# Judge result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmarks:
    - Target: 30 Oct 2026 - 05:23
    - Baseline: 30 Oct 2026 - 05:28
* Package commits:
    - Target: 89eaf2e
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
| `["findfirst", "n=1000", "reduce", "basesize=128"]` | 0.70 (5%) :white_check_mark: | 0.74 (1%) :white_check_mark: |
| `["findfirst", "n=1000", "reduce", "basesize=256"]` |                1.47 (5%) :x: |                1.35 (1%) :x: |
| `["findfirst", "n=1000", "reduce", "basesize=512"]` | 0.81 (5%) :white_check_mark: | 0.78 (1%) :white_check_mark: |
| `["findfirst", "n=400", "reduce", "basesize=128"]`  |                   1.05 (5%)  |                1.07 (1%) :x: |
| `["findfirst", "n=400", "reduce", "basesize=256"]`  |                1.06 (5%) :x: |                1.04 (1%) :x: |
| `["findfirst", "n=400", "reduce", "basesize=512"]`  |                   1.02 (5%)  |                1.02 (1%) :x: |
| `["findfirst", "n=500", "reduce", "basesize=128"]`  | 0.73 (5%) :white_check_mark: | 0.82 (1%) :white_check_mark: |
| `["findfirst", "n=500", "reduce", "basesize=256"]`  | 0.92 (5%) :white_check_mark: | 0.87 (1%) :white_check_mark: |
| `["findfirst", "n=500", "reduce", "basesize=512"]`  | 0.80 (5%) :white_check_mark: | 0.91 (1%) :white_check_mark: |
| `["parallel_histogram", "comm", "basesize=16384"]`  | 0.94 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["splitby", "count", "reduce"]`                    |                   1.04 (5%)  | 0.99 (1%) :white_check_mark: |
| `["words", "nthreads=2"]`                           |                   1.01 (5%)  |                1.01 (1%) :x: |
| `["words", "nthreads=4"]`                           |                1.09 (5%) :x: |                   1.00 (1%)  |

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
      Ubuntu 24.04.5 LTS
  uname: Linux 7.0.0-1017-azure #17~24.04.1-Ubuntu SMP PREEMPT Thu Sep 24 18:46:57 UTC 2026 x86_64 x86_64
  CPU: AMD EPYC 9V74 80-Core Processor: 
              speed         user         nice          sys         idle          irq
       #1  3691 MHz       2124 s          0 s        120 s       4089 s          0 s
       #2  3697 MHz       2664 s          0 s        177 s       3503 s          0 s
       #3  3703 MHz       2620 s          0 s        129 s       3574 s          0 s
       #4  3695 MHz       2478 s          0 s        148 s       3725 s          0 s
       
  Memory: 15.60928726196289 GB (13149.890625 MB free)
  Uptime: 642.62 sec
  Load Avg:  1.83  1.64  0.98
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
      Ubuntu 24.04.5 LTS
  uname: Linux 7.0.0-1017-azure #17~24.04.1-Ubuntu SMP PREEMPT Thu Sep 24 18:46:57 UTC 2026 x86_64 x86_64
  CPU: AMD EPYC 9V74 80-Core Processor: 
              speed         user         nice          sys         idle          irq
       #1  3696 MHz       3278 s          0 s        175 s       5854 s          0 s
       #2  3700 MHz       4049 s          0 s        228 s       5041 s          0 s
       #3  3694 MHz       3668 s          0 s        166 s       5465 s          0 s
       #4  3692 MHz       3568 s          0 s        197 s       5561 s          0 s
       
  Memory: 15.60928726196289 GB (13086.88671875 MB free)
  Uptime: 940.53 sec
  Load Avg:  1.87  1.73  1.2
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-12.0.1 (ORCJIT, znver3)
```

---
# Target result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmark: 30 Oct 2026 - 05:23
* Package commit: 89eaf2e
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
| `["collect", "assoc", "basesize=1"]`                | 131.301 ms (5%) |         |   4.36 MiB (1%) |       32800 |
| `["collect", "assoc", "basesize=1024"]`             | 130.077 ms (5%) |         |   1.09 MiB (1%) |          53 |
| `["collect", "assoc", "basesize=32"]`               | 130.321 ms (5%) |         |   1.48 MiB (1%) |        1052 |
| `["collect", "seq"]`                                | 260.106 ms (5%) |         | 256.05 KiB (1%) |           2 |
| `["collect", "unordered", "basesize=1"]`            | 230.590 ms (5%) |         |  23.93 MiB (1%) |      413994 |
| `["collect", "unordered", "basesize=1024"]`         | 137.035 ms (5%) |         |   1.01 MiB (1%) |        1242 |
| `["collect", "unordered", "basesize=32"]`           | 144.230 ms (5%) |         |   1.60 MiB (1%) |       15349 |
| `["findfirst", "n=1000", "foldl"]`                  | 446.884 ms (5%) |         |                 |             |
| `["findfirst", "n=1000", "reduce", "basesize=128"]` | 243.508 ms (5%) |         | 232.86 KiB (1%) |        3276 |
| `["findfirst", "n=1000", "reduce", "basesize=256"]` | 400.002 ms (5%) |         | 184.48 KiB (1%) |        2624 |
| `["findfirst", "n=1000", "reduce", "basesize=512"]` | 292.078 ms (5%) |         |  77.36 KiB (1%) |        1091 |
| `["findfirst", "n=400", "foldl"]`                   | 334.429 ms (5%) |         |                 |             |
| `["findfirst", "n=400", "reduce", "basesize=128"]`  | 178.086 ms (5%) |         | 398.48 KiB (1%) |        5661 |
| `["findfirst", "n=400", "reduce", "basesize=256"]`  | 187.900 ms (5%) |         | 212.30 KiB (1%) |        3037 |
| `["findfirst", "n=400", "reduce", "basesize=512"]`  | 193.905 ms (5%) |         | 112.75 KiB (1%) |        1627 |
| `["findfirst", "n=500", "foldl"]`                   |  58.045 ms (5%) |         |                 |             |
| `["findfirst", "n=500", "reduce", "basesize=128"]`  |  70.447 ms (5%) |         | 172.45 KiB (1%) |        2333 |
| `["findfirst", "n=500", "reduce", "basesize=256"]`  |  52.088 ms (5%) |         |  72.12 KiB (1%) |         987 |
| `["findfirst", "n=500", "reduce", "basesize=512"]`  |  62.264 ms (5%) |         |  52.38 KiB (1%) |         701 |
| `["overhead", "default"]`                           |  48.223 μs (5%) |         |  32.73 KiB (1%) |         418 |
| `["overhead", "stoppable=false"]`                   |  46.060 μs (5%) |         |  32.78 KiB (1%) |         419 |
| `["overhead", "stoppable=true"]`                    |  53.741 μs (5%) |         |  44.25 KiB (1%) |         610 |
| `["parallel_histogram", "assoc", "basesize=16384"]` |   1.989 ms (5%) |         | 728.91 KiB (1%) |          57 |
| `["parallel_histogram", "assoc", "basesize=4096"]`  |   2.543 ms (5%) |         |   1.79 MiB (1%) |         216 |
| `["parallel_histogram", "assoc", "basesize=8192"]`  |   2.272 ms (5%) |         |   1.42 MiB (1%) |         117 |
| `["parallel_histogram", "comm", "basesize=16384"]`  |   6.284 ms (5%) |         |   1.56 MiB (1%) |        1625 |
| `["parallel_histogram", "comm", "basesize=4096"]`   |  10.891 ms (5%) |         |   1.33 MiB (1%) |        9846 |
| `["parallel_histogram", "comm", "basesize=8192"]`   |   9.474 ms (5%) |         |   1.25 MiB (1%) |        7192 |
| `["parallel_histogram", "seq"]`                     |   3.572 ms (5%) |         | 364.16 KiB (1%) |          24 |
| `["partition_length_maximum", "rand", "foldl"]`     |  27.476 ms (5%) |         |                 |             |
| `["partition_length_maximum", "rand", "reduce"]`    |  13.771 ms (5%) |         |  736 bytes (1%) |          11 |
| `["splitby", "count", "foldl"]`                     |   1.330 ms (5%) |         |                 |             |
| `["splitby", "count", "man"]`                       | 985.707 μs (5%) |         |                 |             |
| `["splitby", "count", "reduce"]`                    | 655.729 μs (5%) |         |   1.05 KiB (1%) |          19 |
| `["sum", "random", "foldl"]`                        |   9.568 ms (5%) |         |                 |             |
| `["sum", "random", "reduce", "basesize=128"]`       |   4.928 ms (5%) |         |  74.06 KiB (1%) |        1100 |
| `["sum", "random", "reduce", "basesize=256"]`       |   4.854 ms (5%) |         |  36.78 KiB (1%) |         547 |
| `["sum", "random", "reduce", "basesize=512"]`       |   4.819 ms (5%) |         |  18.08 KiB (1%) |         269 |
| `["sum", "uniform", "foldl"]`                       |   9.526 ms (5%) |         |                 |             |
| `["sum", "uniform", "reduce", "basesize=128"]`      |   4.905 ms (5%) |         |  74.19 KiB (1%) |        1104 |
| `["sum", "uniform", "reduce", "basesize=256"]`      |   4.842 ms (5%) |         |  36.78 KiB (1%) |         547 |
| `["sum", "uniform", "reduce", "basesize=512"]`      |   4.805 ms (5%) |         |  18.02 KiB (1%) |         267 |
| `["sum", "valley", "foldl"]`                        |   9.727 ms (5%) |         |                 |             |
| `["sum", "valley", "reduce", "basesize=128"]`       |   5.010 ms (5%) |         |  74.16 KiB (1%) |        1103 |
| `["sum", "valley", "reduce", "basesize=256"]`       |   4.948 ms (5%) |         |  36.75 KiB (1%) |         546 |
| `["sum", "valley", "reduce", "basesize=512"]`       |   4.921 ms (5%) |         |  18.14 KiB (1%) |         271 |
| `["words", "nthreads=1"]`                           |  12.932 ms (5%) |         |  31.74 MiB (1%) |     1034251 |
| `["words", "nthreads=2"]`                           |   8.512 ms (5%) |         |  32.46 MiB (1%) |     1034324 |
| `["words", "nthreads=4"]`                           |   9.162 ms (5%) |         |  33.09 MiB (1%) |     1034490 |

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
      Ubuntu 24.04.5 LTS
  uname: Linux 7.0.0-1017-azure #17~24.04.1-Ubuntu SMP PREEMPT Thu Sep 24 18:46:57 UTC 2026 x86_64 x86_64
  CPU: AMD EPYC 9V74 80-Core Processor: 
              speed         user         nice          sys         idle          irq
       #1  3691 MHz       2124 s          0 s        120 s       4089 s          0 s
       #2  3697 MHz       2664 s          0 s        177 s       3503 s          0 s
       #3  3703 MHz       2620 s          0 s        129 s       3574 s          0 s
       #4  3695 MHz       2478 s          0 s        148 s       3725 s          0 s
       
  Memory: 15.60928726196289 GB (13149.890625 MB free)
  Uptime: 642.62 sec
  Load Avg:  1.83  1.64  0.98
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-12.0.1 (ORCJIT, znver3)
```

---
# Baseline result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmark: 30 Oct 2026 - 05:28
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
| `["collect", "assoc", "basesize=1"]`                | 131.719 ms (5%) |         |   4.36 MiB (1%) |       32800 |
| `["collect", "assoc", "basesize=1024"]`             | 130.231 ms (5%) |         |   1.09 MiB (1%) |          53 |
| `["collect", "assoc", "basesize=32"]`               | 130.294 ms (5%) |         |   1.48 MiB (1%) |        1052 |
| `["collect", "seq"]`                                | 260.135 ms (5%) |         | 256.05 KiB (1%) |           2 |
| `["collect", "unordered", "basesize=1"]`            | 229.891 ms (5%) |         |  23.93 MiB (1%) |      413905 |
| `["collect", "unordered", "basesize=1024"]`         | 136.944 ms (5%) |         |   1.01 MiB (1%) |        1209 |
| `["collect", "unordered", "basesize=32"]`           | 143.808 ms (5%) |         |   1.60 MiB (1%) |       15328 |
| `["findfirst", "n=1000", "foldl"]`                  | 447.341 ms (5%) |         |                 |             |
| `["findfirst", "n=1000", "reduce", "basesize=128"]` | 346.831 ms (5%) |         | 314.34 KiB (1%) |        4433 |
| `["findfirst", "n=1000", "reduce", "basesize=256"]` | 272.329 ms (5%) |         | 136.86 KiB (1%) |        1926 |
| `["findfirst", "n=1000", "reduce", "basesize=512"]` | 361.083 ms (5%) |         |  99.39 KiB (1%) |        1391 |
| `["findfirst", "n=400", "foldl"]`                   | 334.776 ms (5%) |         |                 |             |
| `["findfirst", "n=400", "reduce", "basesize=128"]`  | 169.906 ms (5%) |         | 373.44 KiB (1%) |        5339 |
| `["findfirst", "n=400", "reduce", "basesize=256"]`  | 176.993 ms (5%) |         | 204.98 KiB (1%) |        2930 |
| `["findfirst", "n=400", "reduce", "basesize=512"]`  | 189.489 ms (5%) |         | 110.33 KiB (1%) |        1593 |
| `["findfirst", "n=500", "foldl"]`                   |  58.046 ms (5%) |         |                 |             |
| `["findfirst", "n=500", "reduce", "basesize=128"]`  |  97.151 ms (5%) |         | 211.30 KiB (1%) |        2890 |
| `["findfirst", "n=500", "reduce", "basesize=256"]`  |  56.485 ms (5%) |         |  82.91 KiB (1%) |        1117 |
| `["findfirst", "n=500", "reduce", "basesize=512"]`  |  78.040 ms (5%) |         |  57.59 KiB (1%) |         788 |
| `["overhead", "default"]`                           |  47.461 μs (5%) |         |  32.73 KiB (1%) |         418 |
| `["overhead", "stoppable=false"]`                   |  47.462 μs (5%) |         |  32.75 KiB (1%) |         418 |
| `["overhead", "stoppable=true"]`                    |  53.010 μs (5%) |         |  44.28 KiB (1%) |         611 |
| `["parallel_histogram", "assoc", "basesize=16384"]` |   1.986 ms (5%) |         | 728.91 KiB (1%) |          57 |
| `["parallel_histogram", "assoc", "basesize=4096"]`  |   2.535 ms (5%) |         |   1.79 MiB (1%) |         215 |
| `["parallel_histogram", "assoc", "basesize=8192"]`  |   2.268 ms (5%) |         |   1.42 MiB (1%) |         118 |
| `["parallel_histogram", "comm", "basesize=16384"]`  |   6.697 ms (5%) |         |   1.56 MiB (1%) |        1807 |
| `["parallel_histogram", "comm", "basesize=4096"]`   |  11.190 ms (5%) |         |   1.32 MiB (1%) |        9482 |
| `["parallel_histogram", "comm", "basesize=8192"]`   |   9.507 ms (5%) |         |   1.26 MiB (1%) |        7556 |
| `["parallel_histogram", "seq"]`                     |   3.546 ms (5%) |         | 364.16 KiB (1%) |          24 |
| `["partition_length_maximum", "rand", "foldl"]`     |  27.477 ms (5%) |         |                 |             |
| `["partition_length_maximum", "rand", "reduce"]`    |  13.757 ms (5%) |         |  736 bytes (1%) |          11 |
| `["splitby", "count", "foldl"]`                     |   1.343 ms (5%) |         |                 |             |
| `["splitby", "count", "man"]`                       | 986.086 μs (5%) |         |                 |             |
| `["splitby", "count", "reduce"]`                    | 627.506 μs (5%) |         |   1.06 KiB (1%) |          18 |
| `["sum", "random", "foldl"]`                        |   9.644 ms (5%) |         |                 |             |
| `["sum", "random", "reduce", "basesize=128"]`       |   4.958 ms (5%) |         |  74.19 KiB (1%) |        1104 |
| `["sum", "random", "reduce", "basesize=256"]`       |   4.898 ms (5%) |         |  36.75 KiB (1%) |         546 |
| `["sum", "random", "reduce", "basesize=512"]`       |   4.869 ms (5%) |         |  18.02 KiB (1%) |         267 |
| `["sum", "uniform", "foldl"]`                       |   9.522 ms (5%) |         |                 |             |
| `["sum", "uniform", "reduce", "basesize=128"]`      |   4.904 ms (5%) |         |  74.22 KiB (1%) |        1105 |
| `["sum", "uniform", "reduce", "basesize=256"]`      |   4.838 ms (5%) |         |  36.78 KiB (1%) |         547 |
| `["sum", "uniform", "reduce", "basesize=512"]`      |   4.806 ms (5%) |         |  18.08 KiB (1%) |         269 |
| `["sum", "valley", "foldl"]`                        |   9.727 ms (5%) |         |                 |             |
| `["sum", "valley", "reduce", "basesize=128"]`       |   5.007 ms (5%) |         |  74.12 KiB (1%) |        1102 |
| `["sum", "valley", "reduce", "basesize=256"]`       |   4.949 ms (5%) |         |  36.75 KiB (1%) |         546 |
| `["sum", "valley", "reduce", "basesize=512"]`       |   4.924 ms (5%) |         |  18.11 KiB (1%) |         270 |
| `["words", "nthreads=1"]`                           |  12.850 ms (5%) |         |  31.77 MiB (1%) |     1035224 |
| `["words", "nthreads=2"]`                           |   8.453 ms (5%) |         |  32.13 MiB (1%) |     1035267 |
| `["words", "nthreads=4"]`                           |   8.368 ms (5%) |         |  33.03 MiB (1%) |     1035537 |

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
      Ubuntu 24.04.5 LTS
  uname: Linux 7.0.0-1017-azure #17~24.04.1-Ubuntu SMP PREEMPT Thu Sep 24 18:46:57 UTC 2026 x86_64 x86_64
  CPU: AMD EPYC 9V74 80-Core Processor: 
              speed         user         nice          sys         idle          irq
       #1  3696 MHz       3278 s          0 s        175 s       5854 s          0 s
       #2  3700 MHz       4049 s          0 s        228 s       5041 s          0 s
       #3  3694 MHz       3668 s          0 s        166 s       5465 s          0 s
       #4  3692 MHz       3568 s          0 s        197 s       5561 s          0 s
       
  Memory: 15.60928726196289 GB (13086.88671875 MB free)
  Uptime: 940.53 sec
  Load Avg:  1.87  1.73  1.2
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
    Model name:                              AMD EPYC 9V74 80-Core Processor
    CPU family:                              25
    Model:                                   17
    Thread(s) per core:                      2
    Core(s) per socket:                      2
    Socket(s):                               1
    Stepping:                                1
    BogoMIPS:                                5192.29
    Flags:                                   fpu vme de pse tsc msr pae mce cx8 apic sep mtrr pge mca cmov pat pse36 clflush mmx fxsr sse sse2 ht syscall nx mmxext fxsr_opt pdpe1gb rdtscp lm constant_tsc rep_good nopl xtopology tsc_reliable nonstop_tsc cpuid extd_apicid aperfmperf tsc_known_freq pni pclmulqdq ssse3 fma cx16 pcid sse4_1 sse4_2 movbe popcnt aes xsave avx f16c rdrand hypervisor lahf_lm cmp_legacy svm cr8_legacy abm sse4a misalignsse 3dnowprefetch osvw topoext vmmcall fsgsbase bmi1 avx2 smep bmi2 erms invpcid avx512f avx512dq rdseed adx smap avx512ifma clflushopt clwb avx512cd sha_ni avx512bw avx512vl xsaveopt xsavec xgetbv1 xsaves user_shstk avx512_bf16 clzero xsaveerptr rdpru arat npt nrip_save tsc_scale vmcb_clean flushbyasid decodeassists pausefilter pfthreshold v_vmsave_vmload avx512vbmi umip avx512_vbmi2 gfni vaes vpclmulqdq avx512_vnni avx512_bitalg avx512_vpopcntdq rdpid fsrm
    Virtualization:                          AMD-V
    Hypervisor vendor:                       Microsoft
    Virtualization type:                     full
    L1d cache:                               64 KiB (2 instances)
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
    Vulnerability Tsa:                       Vulnerable: No microcode
    Vulnerability Tsx async abort:           Not affected
    Vulnerability Vmscape:                   Not affected
    

| Cpu Property       | Value                                                      |
|:------------------ |:---------------------------------------------------------- |
| Brand              | AMD EPYC 9V74 80-Core Processor                            |
| Vendor             | :AMD                                                       |
| Architecture       | :Unknown                                                   |
| Model              | Family: 0xaf, Model: 0x11, Stepping: 0x01, Type: 0x00      |
| Cores              | 8 physical cores, 16 logical cores (on executing CPU)      |
|                    | Hyperthreading hardware capability detected                |
| Clock Frequencies  | Not supported by CPU                                       |
| Data Cache         | Level 1:3 : (32, 1024, 32768) kbytes                       |
|                    | 64 byte cache line size                                    |
| Address Size       | 48 bits virtual, 48 bits physical                          |
| SIMD               | 512 bit = 64 byte max. SIMD vector size                    |
| Time Stamp Counter | TSC is accessible via `rdtsc`                              |
|                    | TSC runs at constant rate (invariant from clock frequency) |
| Perf. Monitoring   | Performance Monitoring Counters (PMC) are not supported    |
| Hypervisor         | Yes, Microsoft                                             |

