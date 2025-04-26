# Multi-thread benchmark result

* Pull request commit: [`de7a7aba73a4f183338b80ec419c3ea76315f911`](https://github.com/JuliaFolds/Transducers.jl/commit/de7a7aba73a4f183338b80ec419c3ea76315f911)
* Pull request: <https://github.com/JuliaFolds/Transducers.jl/pull/243> (Update */Manifest.toml)

# Judge result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmarks:
    - Target: 26 Apr 2025 - 02:00
    - Baseline: 26 Apr 2025 - 02:05
* Package commits:
    - Target: 4aa28c7
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
| `["findfirst", "n=1000", "reduce", "basesize=128"]` |                1.22 (5%) :x: |                1.26 (1%) :x: |
| `["findfirst", "n=1000", "reduce", "basesize=256"]` |                1.10 (5%) :x: |                1.02 (1%) :x: |
| `["findfirst", "n=1000", "reduce", "basesize=512"]` | 0.57 (5%) :white_check_mark: | 0.64 (1%) :white_check_mark: |
| `["findfirst", "n=400", "reduce", "basesize=128"]`  |                   1.04 (5%)  |                1.04 (1%) :x: |
| `["findfirst", "n=400", "reduce", "basesize=512"]`  |                1.18 (5%) :x: |                1.11 (1%) :x: |
| `["findfirst", "n=500", "reduce", "basesize=128"]`  |                1.22 (5%) :x: |                1.27 (1%) :x: |
| `["findfirst", "n=500", "reduce", "basesize=256"]`  |                2.29 (5%) :x: |                1.95 (1%) :x: |
| `["findfirst", "n=500", "reduce", "basesize=512"]`  |                2.19 (5%) :x: |                1.80 (1%) :x: |
| `["parallel_histogram", "comm", "basesize=16384"]`  | 0.95 (5%) :white_check_mark: |                1.24 (1%) :x: |
| `["parallel_histogram", "comm", "basesize=4096"]`   |                   0.95 (5%)  | 0.98 (1%) :white_check_mark: |
| `["parallel_histogram", "comm", "basesize=8192"]`   |                   0.99 (5%)  | 0.99 (1%) :white_check_mark: |
| `["splitby", "count", "reduce"]`                    | 0.84 (5%) :white_check_mark: |                1.08 (1%) :x: |
| `["words", "nthreads=4"]`                           | 0.92 (5%) :white_check_mark: |                   0.99 (1%)  |

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
  uname: Linux 6.11.0-1012-azure #12~24.04.1-Ubuntu SMP Mon Mar 10 19:00:39 UTC 2025 x86_64 x86_64
  CPU: AMD EPYC 7763 64-Core Processor: 
              speed         user         nice          sys         idle          irq
       #1  3241 MHz       2446 s          0 s        192 s       5403 s          0 s
       #2  3248 MHz       2554 s          0 s        196 s       5319 s          0 s
       #3  3243 MHz       2203 s          0 s        199 s       5666 s          0 s
       #4  3243 MHz       2818 s          0 s        228 s       4984 s          0 s
       
  Memory: 15.614944458007812 GB (8674.13671875 MB free)
  Uptime: 814.58 sec
  Load Avg:  1.78  1.52  0.89
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
  uname: Linux 6.11.0-1012-azure #12~24.04.1-Ubuntu SMP Mon Mar 10 19:00:39 UTC 2025 x86_64 x86_64
  CPU: AMD EPYC 7763 64-Core Processor: 
              speed         user         nice          sys         idle          irq
       #1  3240 MHz       3649 s          0 s        255 s       7225 s          0 s
       #2  3227 MHz       3744 s          0 s        267 s       7145 s          0 s
       #3  3231 MHz       3234 s          0 s        262 s       7662 s          0 s
       #4  3246 MHz       4189 s          0 s        329 s       6603 s          0 s
       
  Memory: 15.614944458007812 GB (8678.671875 MB free)
  Uptime: 1123.92 sec
  Load Avg:  1.64  1.61  1.11
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-12.0.1 (ORCJIT, znver3)
```

---
# Target result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmark: 26 Apr 2025 - 02:00
* Package commit: 4aa28c7
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
| `["collect", "assoc", "basesize=1"]`                | 149.821 ms (5%) |         |   4.36 MiB (1%) |       32800 |
| `["collect", "assoc", "basesize=1024"]`             | 148.164 ms (5%) |         |   1.09 MiB (1%) |          53 |
| `["collect", "assoc", "basesize=32"]`               | 148.361 ms (5%) |         |   1.48 MiB (1%) |        1052 |
| `["collect", "seq"]`                                | 296.122 ms (5%) |         | 256.05 KiB (1%) |           2 |
| `["collect", "unordered", "basesize=1"]`            | 242.391 ms (5%) |         |  23.69 MiB (1%) |      406119 |
| `["collect", "unordered", "basesize=1024"]`         | 158.380 ms (5%) |         |   1.01 MiB (1%) |        1147 |
| `["collect", "unordered", "basesize=32"]`           | 169.663 ms (5%) |         |   1.60 MiB (1%) |       15413 |
| `["findfirst", "n=1000", "foldl"]`                  | 509.847 ms (5%) |         |                 |             |
| `["findfirst", "n=1000", "reduce", "basesize=128"]` | 339.613 ms (5%) |         | 293.22 KiB (1%) |        4086 |
| `["findfirst", "n=1000", "reduce", "basesize=256"]` | 372.699 ms (5%) |         | 160.47 KiB (1%) |        2267 |
| `["findfirst", "n=1000", "reduce", "basesize=512"]` | 456.797 ms (5%) |         | 108.55 KiB (1%) |        1509 |
| `["findfirst", "n=400", "foldl"]`                   | 381.136 ms (5%) |         |                 |             |
| `["findfirst", "n=400", "reduce", "basesize=128"]`  | 205.321 ms (5%) |         | 398.62 KiB (1%) |        5672 |
| `["findfirst", "n=400", "reduce", "basesize=256"]`  | 199.419 ms (5%) |         | 200.86 KiB (1%) |        2873 |
| `["findfirst", "n=400", "reduce", "basesize=512"]`  | 308.509 ms (5%) |         | 153.14 KiB (1%) |        2194 |
| `["findfirst", "n=500", "foldl"]`                   |  65.637 ms (5%) |         |                 |             |
| `["findfirst", "n=500", "reduce", "basesize=128"]`  | 138.859 ms (5%) |         | 258.20 KiB (1%) |        3575 |
| `["findfirst", "n=500", "reduce", "basesize=256"]`  | 131.830 ms (5%) |         | 140.72 KiB (1%) |        1911 |
| `["findfirst", "n=500", "reduce", "basesize=512"]`  | 188.661 ms (5%) |         | 102.03 KiB (1%) |        1405 |
| `["overhead", "default"]`                           |  53.079 μs (5%) |         |  32.73 KiB (1%) |         418 |
| `["overhead", "stoppable=false"]`                   |  53.240 μs (5%) |         |  32.75 KiB (1%) |         418 |
| `["overhead", "stoppable=true"]`                    |  59.782 μs (5%) |         |  44.25 KiB (1%) |         610 |
| `["parallel_histogram", "assoc", "basesize=16384"]` |   2.414 ms (5%) |         | 728.91 KiB (1%) |          57 |
| `["parallel_histogram", "assoc", "basesize=4096"]`  |   2.987 ms (5%) |         |   1.79 MiB (1%) |         216 |
| `["parallel_histogram", "assoc", "basesize=8192"]`  |   2.690 ms (5%) |         |   1.42 MiB (1%) |         117 |
| `["parallel_histogram", "comm", "basesize=16384"]`  |   8.438 ms (5%) |         |   1.58 MiB (1%) |        2392 |
| `["parallel_histogram", "comm", "basesize=4096"]`   |  12.268 ms (5%) |         |   1.30 MiB (1%) |        8604 |
| `["parallel_histogram", "comm", "basesize=8192"]`   |  11.913 ms (5%) |         |   1.28 MiB (1%) |        6603 |
| `["parallel_histogram", "seq"]`                     |   4.274 ms (5%) |         | 364.16 KiB (1%) |          24 |
| `["partition_length_maximum", "rand", "foldl"]`     |  31.305 ms (5%) |         |                 |             |
| `["partition_length_maximum", "rand", "reduce"]`    |  15.696 ms (5%) |         |  736 bytes (1%) |          11 |
| `["splitby", "count", "foldl"]`                     |   1.537 ms (5%) |         |                 |             |
| `["splitby", "count", "man"]`                       |   1.165 ms (5%) |         |                 |             |
| `["splitby", "count", "reduce"]`                    | 724.080 μs (5%) |         |   1.09 KiB (1%) |          19 |
| `["sum", "random", "foldl"]`                        |  11.127 ms (5%) |         |                 |             |
| `["sum", "random", "reduce", "basesize=128"]`       |   5.712 ms (5%) |         |  74.25 KiB (1%) |        1106 |
| `["sum", "random", "reduce", "basesize=256"]`       |   5.640 ms (5%) |         |  36.78 KiB (1%) |         547 |
| `["sum", "random", "reduce", "basesize=512"]`       |   5.606 ms (5%) |         |  18.08 KiB (1%) |         269 |
| `["sum", "uniform", "foldl"]`                       |  10.926 ms (5%) |         |                 |             |
| `["sum", "uniform", "reduce", "basesize=128"]`      |   5.617 ms (5%) |         |  74.19 KiB (1%) |        1104 |
| `["sum", "uniform", "reduce", "basesize=256"]`      |   5.562 ms (5%) |         |  36.78 KiB (1%) |         547 |
| `["sum", "uniform", "reduce", "basesize=512"]`      |   5.517 ms (5%) |         |  18.08 KiB (1%) |         269 |
| `["sum", "valley", "foldl"]`                        |  11.173 ms (5%) |         |                 |             |
| `["sum", "valley", "reduce", "basesize=128"]`       |   5.725 ms (5%) |         |  74.12 KiB (1%) |        1102 |
| `["sum", "valley", "reduce", "basesize=256"]`       |   5.672 ms (5%) |         |  36.78 KiB (1%) |         547 |
| `["sum", "valley", "reduce", "basesize=512"]`       |   5.645 ms (5%) |         |  18.05 KiB (1%) |         268 |
| `["words", "nthreads=1"]`                           |  14.735 ms (5%) |         |  31.72 MiB (1%) |     1033461 |
| `["words", "nthreads=2"]`                           |   9.521 ms (5%) |         |  32.44 MiB (1%) |     1033534 |
| `["words", "nthreads=4"]`                           |   9.677 ms (5%) |         |  32.88 MiB (1%) |     1033603 |

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
  uname: Linux 6.11.0-1012-azure #12~24.04.1-Ubuntu SMP Mon Mar 10 19:00:39 UTC 2025 x86_64 x86_64
  CPU: AMD EPYC 7763 64-Core Processor: 
              speed         user         nice          sys         idle          irq
       #1  3241 MHz       2446 s          0 s        192 s       5403 s          0 s
       #2  3248 MHz       2554 s          0 s        196 s       5319 s          0 s
       #3  3243 MHz       2203 s          0 s        199 s       5666 s          0 s
       #4  3243 MHz       2818 s          0 s        228 s       4984 s          0 s
       
  Memory: 15.614944458007812 GB (8674.13671875 MB free)
  Uptime: 814.58 sec
  Load Avg:  1.78  1.52  0.89
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-12.0.1 (ORCJIT, znver3)
```

---
# Baseline result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmark: 26 Apr 2025 - 02:05
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
| `["collect", "assoc", "basesize=1"]`                | 149.861 ms (5%) |         |   4.36 MiB (1%) |       32800 |
| `["collect", "assoc", "basesize=1024"]`             | 148.447 ms (5%) |         |   1.09 MiB (1%) |          53 |
| `["collect", "assoc", "basesize=32"]`               | 148.335 ms (5%) |         |   1.48 MiB (1%) |        1052 |
| `["collect", "seq"]`                                | 296.011 ms (5%) |         | 256.05 KiB (1%) |           2 |
| `["collect", "unordered", "basesize=1"]`            | 244.897 ms (5%) |         |  23.69 MiB (1%) |      406255 |
| `["collect", "unordered", "basesize=1024"]`         | 158.200 ms (5%) |         |   1.01 MiB (1%) |        1176 |
| `["collect", "unordered", "basesize=32"]`           | 171.475 ms (5%) |         |   1.61 MiB (1%) |       15480 |
| `["findfirst", "n=1000", "foldl"]`                  | 510.233 ms (5%) |         |                 |             |
| `["findfirst", "n=1000", "reduce", "basesize=128"]` | 277.569 ms (5%) |         | 232.86 KiB (1%) |        3276 |
| `["findfirst", "n=1000", "reduce", "basesize=256"]` | 340.010 ms (5%) |         | 157.20 KiB (1%) |        2193 |
| `["findfirst", "n=1000", "reduce", "basesize=512"]` | 796.340 ms (5%) |         | 168.31 KiB (1%) |        2376 |
| `["findfirst", "n=400", "foldl"]`                   | 381.316 ms (5%) |         |                 |             |
| `["findfirst", "n=400", "reduce", "basesize=128"]`  | 196.523 ms (5%) |         | 383.12 KiB (1%) |        5454 |
| `["findfirst", "n=400", "reduce", "basesize=256"]`  | 199.624 ms (5%) |         | 200.89 KiB (1%) |        2874 |
| `["findfirst", "n=400", "reduce", "basesize=512"]`  | 262.369 ms (5%) |         | 137.97 KiB (1%) |        1980 |
| `["findfirst", "n=500", "foldl"]`                   |  66.266 ms (5%) |         |                 |             |
| `["findfirst", "n=500", "reduce", "basesize=128"]`  | 113.957 ms (5%) |         | 202.89 KiB (1%) |        2825 |
| `["findfirst", "n=500", "reduce", "basesize=256"]`  |  57.631 ms (5%) |         |  72.12 KiB (1%) |         978 |
| `["findfirst", "n=500", "reduce", "basesize=512"]`  |  86.203 ms (5%) |         |  56.80 KiB (1%) |         777 |
| `["overhead", "default"]`                           |  52.208 μs (5%) |         |  32.73 KiB (1%) |         418 |
| `["overhead", "stoppable=false"]`                   |  51.827 μs (5%) |         |  32.75 KiB (1%) |         418 |
| `["overhead", "stoppable=true"]`                    |  57.919 μs (5%) |         |  44.25 KiB (1%) |         610 |
| `["parallel_histogram", "assoc", "basesize=16384"]` |   2.399 ms (5%) |         | 728.91 KiB (1%) |          57 |
| `["parallel_histogram", "assoc", "basesize=4096"]`  |   2.961 ms (5%) |         |   1.79 MiB (1%) |         216 |
| `["parallel_histogram", "assoc", "basesize=8192"]`  |   2.674 ms (5%) |         |   1.42 MiB (1%) |         117 |
| `["parallel_histogram", "comm", "basesize=16384"]`  |   8.919 ms (5%) |         |   1.27 MiB (1%) |        1000 |
| `["parallel_histogram", "comm", "basesize=4096"]`   |  12.885 ms (5%) |         |   1.33 MiB (1%) |        9589 |
| `["parallel_histogram", "comm", "basesize=8192"]`   |  11.980 ms (5%) |         |   1.30 MiB (1%) |        8160 |
| `["parallel_histogram", "seq"]`                     |   4.258 ms (5%) |         | 364.16 KiB (1%) |          24 |
| `["partition_length_maximum", "rand", "foldl"]`     |  31.305 ms (5%) |         |                 |             |
| `["partition_length_maximum", "rand", "reduce"]`    |  15.694 ms (5%) |         |  736 bytes (1%) |          11 |
| `["splitby", "count", "foldl"]`                     |   1.476 ms (5%) |         |                 |             |
| `["splitby", "count", "man"]`                       |   1.140 ms (5%) |         |                 |             |
| `["splitby", "count", "reduce"]`                    | 859.193 μs (5%) |         |   1.02 KiB (1%) |          19 |
| `["sum", "random", "foldl"]`                        |  11.096 ms (5%) |         |                 |             |
| `["sum", "random", "reduce", "basesize=128"]`       |   5.691 ms (5%) |         |  74.19 KiB (1%) |        1104 |
| `["sum", "random", "reduce", "basesize=256"]`       |   5.622 ms (5%) |         |  36.75 KiB (1%) |         546 |
| `["sum", "random", "reduce", "basesize=512"]`       |   5.586 ms (5%) |         |  18.08 KiB (1%) |         269 |
| `["sum", "uniform", "foldl"]`                       |  10.926 ms (5%) |         |                 |             |
| `["sum", "uniform", "reduce", "basesize=128"]`      |   5.587 ms (5%) |         |  74.16 KiB (1%) |        1103 |
| `["sum", "uniform", "reduce", "basesize=256"]`      |   5.536 ms (5%) |         |  36.78 KiB (1%) |         547 |
| `["sum", "uniform", "reduce", "basesize=512"]`      |   5.494 ms (5%) |         |  18.08 KiB (1%) |         269 |
| `["sum", "valley", "foldl"]`                        |  11.173 ms (5%) |         |                 |             |
| `["sum", "valley", "reduce", "basesize=128"]`       |   5.693 ms (5%) |         |  74.09 KiB (1%) |        1101 |
| `["sum", "valley", "reduce", "basesize=256"]`       |   5.642 ms (5%) |         |  36.72 KiB (1%) |         545 |
| `["sum", "valley", "reduce", "basesize=512"]`       |   5.629 ms (5%) |         |  18.08 KiB (1%) |         269 |
| `["words", "nthreads=1"]`                           |  14.712 ms (5%) |         |  31.75 MiB (1%) |     1034495 |
| `["words", "nthreads=2"]`                           |   9.985 ms (5%) |         |  32.46 MiB (1%) |     1034574 |
| `["words", "nthreads=4"]`                           |  10.562 ms (5%) |         |  33.09 MiB (1%) |     1034739 |

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
  uname: Linux 6.11.0-1012-azure #12~24.04.1-Ubuntu SMP Mon Mar 10 19:00:39 UTC 2025 x86_64 x86_64
  CPU: AMD EPYC 7763 64-Core Processor: 
              speed         user         nice          sys         idle          irq
       #1  3240 MHz       3649 s          0 s        255 s       7225 s          0 s
       #2  3227 MHz       3744 s          0 s        267 s       7145 s          0 s
       #3  3231 MHz       3234 s          0 s        262 s       7662 s          0 s
       #4  3246 MHz       4189 s          0 s        329 s       6603 s          0 s
       
  Memory: 15.614944458007812 GB (8678.671875 MB free)
  Uptime: 1123.92 sec
  Load Avg:  1.64  1.61  1.11
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

