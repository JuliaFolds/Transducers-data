# Multi-thread benchmark result

* Pull request commit: [`df971939fbcc9db76d22af5d0a0460b5d0db10a8`](https://github.com/JuliaFolds/Transducers.jl/commit/df971939fbcc9db76d22af5d0a0460b5d0db10a8)
* Pull request: <https://github.com/JuliaFolds/Transducers.jl/pull/243> (Update */Manifest.toml)

# Judge result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmarks:
    - Target: 19 May 2026 - 04:16
    - Baseline: 19 May 2026 - 04:21
* Package commits:
    - Target: e436d0e
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
| `["findfirst", "n=1000", "reduce", "basesize=128"]` |                   0.99 (5%)  | 0.99 (1%) :white_check_mark: |
| `["findfirst", "n=1000", "reduce", "basesize=256"]` |                1.45 (5%) :x: |                1.40 (1%) :x: |
| `["findfirst", "n=1000", "reduce", "basesize=512"]` | 0.76 (5%) :white_check_mark: | 0.78 (1%) :white_check_mark: |
| `["findfirst", "n=400", "reduce", "basesize=128"]`  |                   0.97 (5%)  | 0.96 (1%) :white_check_mark: |
| `["findfirst", "n=400", "reduce", "basesize=512"]`  |                   1.01 (5%)  |                1.02 (1%) :x: |
| `["findfirst", "n=500", "reduce", "basesize=128"]`  |                1.11 (5%) :x: |                1.19 (1%) :x: |
| `["findfirst", "n=500", "reduce", "basesize=256"]`  |                1.05 (5%) :x: |                1.02 (1%) :x: |
| `["findfirst", "n=500", "reduce", "basesize=512"]`  |                4.93 (5%) :x: |                3.34 (1%) :x: |
| `["parallel_histogram", "comm", "basesize=16384"]`  |                1.07 (5%) :x: |                   1.01 (1%)  |
| `["parallel_histogram", "comm", "basesize=8192"]`   |                   1.02 (5%)  |                1.01 (1%) :x: |
| `["words", "nthreads=4"]`                           |                1.07 (5%) :x: |                   0.99 (1%)  |

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
  uname: Linux 6.17.0-1013-azure #13~24.04.1-Ubuntu SMP Wed Apr 15 16:52:17 UTC 2026 x86_64 x86_64
  CPU: AMD EPYC 9V74 80-Core Processor: 
              speed         user         nice          sys         idle          irq
       #1  2874 MHz       2135 s          0 s        172 s       4325 s          0 s
       #2  2872 MHz       2252 s          0 s        150 s       4220 s          0 s
       #3  2870 MHz       2863 s          0 s        164 s       3591 s          0 s
       #4  2871 MHz       2947 s          0 s        181 s       3502 s          0 s
       
  Memory: 15.614952087402344 GB (12218.55859375 MB free)
  Uptime: 667.0 sec
  Load Avg:  1.61  1.49  0.92
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
  uname: Linux 6.17.0-1013-azure #13~24.04.1-Ubuntu SMP Wed Apr 15 16:52:17 UTC 2026 x86_64 x86_64
  CPU: AMD EPYC 9V74 80-Core Processor: 
              speed         user         nice          sys         idle          irq
       #1  2871 MHz       3207 s          0 s        234 s       6297 s          0 s
       #2  2867 MHz       3666 s          0 s        213 s       5849 s          0 s
       #3  2871 MHz       3891 s          0 s        208 s       5627 s          0 s
       #4  2897 MHz       4264 s          0 s        235 s       5237 s          0 s
       
  Memory: 15.614952087402344 GB (12239.98046875 MB free)
  Uptime: 978.16 sec
  Load Avg:  1.75  1.6  1.13
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-12.0.1 (ORCJIT, znver3)
```

---
# Target result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmark: 19 May 2026 - 04:16
* Package commit: e436d0e
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
| `["collect", "assoc", "basesize=1"]`                | 168.895 ms (5%) |         |   4.36 MiB (1%) |       32800 |
| `["collect", "assoc", "basesize=1024"]`             | 167.231 ms (5%) |         |   1.09 MiB (1%) |          53 |
| `["collect", "assoc", "basesize=32"]`               | 167.487 ms (5%) |         |   1.48 MiB (1%) |        1052 |
| `["collect", "seq"]`                                | 334.103 ms (5%) |         | 256.05 KiB (1%) |           2 |
| `["collect", "unordered", "basesize=1"]`            | 278.669 ms (5%) |         |  23.80 MiB (1%) |      409590 |
| `["collect", "unordered", "basesize=1024"]`         | 176.412 ms (5%) |         |   1.01 MiB (1%) |        1103 |
| `["collect", "unordered", "basesize=32"]`           | 186.409 ms (5%) |         |   1.60 MiB (1%) |       15235 |
| `["findfirst", "n=1000", "foldl"]`                  | 576.985 ms (5%) |         |                 |             |
| `["findfirst", "n=1000", "reduce", "basesize=128"]` | 311.737 ms (5%) |         | 229.67 KiB (1%) |        3234 |
| `["findfirst", "n=1000", "reduce", "basesize=256"]` | 626.634 ms (5%) |         | 225.62 KiB (1%) |        3177 |
| `["findfirst", "n=1000", "reduce", "basesize=512"]` | 394.197 ms (5%) |         |  81.23 KiB (1%) |        1143 |
| `["findfirst", "n=400", "foldl"]`                   | 431.689 ms (5%) |         |                 |             |
| `["findfirst", "n=400", "reduce", "basesize=128"]`  | 227.383 ms (5%) |         | 389.73 KiB (1%) |        5545 |
| `["findfirst", "n=400", "reduce", "basesize=256"]`  | 225.773 ms (5%) |         | 200.86 KiB (1%) |        2873 |
| `["findfirst", "n=400", "reduce", "basesize=512"]`  | 279.129 ms (5%) |         | 130.50 KiB (1%) |        1860 |
| `["findfirst", "n=500", "foldl"]`                   |  74.933 ms (5%) |         |                 |             |
| `["findfirst", "n=500", "reduce", "basesize=128"]`  |  83.125 ms (5%) |         | 167.86 KiB (1%) |        2261 |
| `["findfirst", "n=500", "reduce", "basesize=256"]`  | 200.310 ms (5%) |         | 167.88 KiB (1%) |        2371 |
| `["findfirst", "n=500", "reduce", "basesize=512"]`  | 454.041 ms (5%) |         | 181.31 KiB (1%) |        2527 |
| `["overhead", "default"]`                           |  58.548 μs (5%) |         |  32.73 KiB (1%) |         418 |
| `["overhead", "stoppable=false"]`                   |  59.860 μs (5%) |         |  32.72 KiB (1%) |         417 |
| `["overhead", "stoppable=true"]`                    |  66.579 μs (5%) |         |  44.25 KiB (1%) |         610 |
| `["parallel_histogram", "assoc", "basesize=16384"]` |   2.526 ms (5%) |         | 728.91 KiB (1%) |          57 |
| `["parallel_histogram", "assoc", "basesize=4096"]`  |   3.227 ms (5%) |         |   1.79 MiB (1%) |         216 |
| `["parallel_histogram", "assoc", "basesize=8192"]`  |   2.889 ms (5%) |         |   1.42 MiB (1%) |         117 |
| `["parallel_histogram", "comm", "basesize=16384"]`  |   9.060 ms (5%) |         |   1.57 MiB (1%) |        2136 |
| `["parallel_histogram", "comm", "basesize=4096"]`   |  14.548 ms (5%) |         |   1.34 MiB (1%) |        9974 |
| `["parallel_histogram", "comm", "basesize=8192"]`   |  12.994 ms (5%) |         |   1.27 MiB (1%) |        7682 |
| `["parallel_histogram", "seq"]`                     |   4.499 ms (5%) |         | 364.16 KiB (1%) |          24 |
| `["partition_length_maximum", "rand", "foldl"]`     |  35.418 ms (5%) |         |                 |             |
| `["partition_length_maximum", "rand", "reduce"]`    |  17.734 ms (5%) |         |  736 bytes (1%) |          11 |
| `["splitby", "count", "foldl"]`                     |   1.669 ms (5%) |         |                 |             |
| `["splitby", "count", "man"]`                       |   1.279 ms (5%) |         |                 |             |
| `["splitby", "count", "reduce"]`                    | 827.281 μs (5%) |         |   1.06 KiB (1%) |          18 |
| `["sum", "random", "foldl"]`                        |  12.519 ms (5%) |         |                 |             |
| `["sum", "random", "reduce", "basesize=128"]`       |   6.437 ms (5%) |         |  74.19 KiB (1%) |        1104 |
| `["sum", "random", "reduce", "basesize=256"]`       |   6.360 ms (5%) |         |  36.81 KiB (1%) |         548 |
| `["sum", "random", "reduce", "basesize=512"]`       |   6.317 ms (5%) |         |  18.02 KiB (1%) |         267 |
| `["sum", "uniform", "foldl"]`                       |  12.288 ms (5%) |         |                 |             |
| `["sum", "uniform", "reduce", "basesize=128"]`      |   6.321 ms (5%) |         |  74.19 KiB (1%) |        1104 |
| `["sum", "uniform", "reduce", "basesize=256"]`      |   6.240 ms (5%) |         |  36.75 KiB (1%) |         546 |
| `["sum", "uniform", "reduce", "basesize=512"]`      |   6.195 ms (5%) |         |  18.05 KiB (1%) |         268 |
| `["sum", "valley", "foldl"]`                        |  12.545 ms (5%) |         |                 |             |
| `["sum", "valley", "reduce", "basesize=128"]`       |   6.449 ms (5%) |         |  74.09 KiB (1%) |        1101 |
| `["sum", "valley", "reduce", "basesize=256"]`       |   6.372 ms (5%) |         |  36.78 KiB (1%) |         547 |
| `["sum", "valley", "reduce", "basesize=512"]`       |   6.346 ms (5%) |         |  18.08 KiB (1%) |         269 |
| `["words", "nthreads=1"]`                           |  16.052 ms (5%) |         |  31.82 MiB (1%) |     1036792 |
| `["words", "nthreads=2"]`                           |  10.523 ms (5%) |         |  32.18 MiB (1%) |     1036855 |
| `["words", "nthreads=4"]`                           |  11.507 ms (5%) |         |  32.89 MiB (1%) |     1036932 |

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
  uname: Linux 6.17.0-1013-azure #13~24.04.1-Ubuntu SMP Wed Apr 15 16:52:17 UTC 2026 x86_64 x86_64
  CPU: AMD EPYC 9V74 80-Core Processor: 
              speed         user         nice          sys         idle          irq
       #1  2874 MHz       2135 s          0 s        172 s       4325 s          0 s
       #2  2872 MHz       2252 s          0 s        150 s       4220 s          0 s
       #3  2870 MHz       2863 s          0 s        164 s       3591 s          0 s
       #4  2871 MHz       2947 s          0 s        181 s       3502 s          0 s
       
  Memory: 15.614952087402344 GB (12218.55859375 MB free)
  Uptime: 667.0 sec
  Load Avg:  1.61  1.49  0.92
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-12.0.1 (ORCJIT, znver3)
```

---
# Baseline result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmark: 19 May 2026 - 04:21
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
| `["collect", "assoc", "basesize=1"]`                | 168.814 ms (5%) |         |   4.36 MiB (1%) |       32800 |
| `["collect", "assoc", "basesize=1024"]`             | 167.661 ms (5%) |         |   1.09 MiB (1%) |          54 |
| `["collect", "assoc", "basesize=32"]`               | 167.541 ms (5%) |         |   1.48 MiB (1%) |        1053 |
| `["collect", "seq"]`                                | 334.084 ms (5%) |         | 256.05 KiB (1%) |           2 |
| `["collect", "unordered", "basesize=1"]`            | 279.544 ms (5%) |         |  23.77 MiB (1%) |      408822 |
| `["collect", "unordered", "basesize=1024"]`         | 176.338 ms (5%) |         |   1.01 MiB (1%) |        1052 |
| `["collect", "unordered", "basesize=32"]`           | 185.908 ms (5%) |         |   1.60 MiB (1%) |       15191 |
| `["findfirst", "n=1000", "foldl"]`                  | 580.691 ms (5%) |         |                 |             |
| `["findfirst", "n=1000", "reduce", "basesize=128"]` | 316.446 ms (5%) |         | 232.86 KiB (1%) |        3276 |
| `["findfirst", "n=1000", "reduce", "basesize=256"]` | 430.761 ms (5%) |         | 161.05 KiB (1%) |        2265 |
| `["findfirst", "n=1000", "reduce", "basesize=512"]` | 517.446 ms (5%) |         | 103.59 KiB (1%) |        1456 |
| `["findfirst", "n=400", "foldl"]`                   | 434.350 ms (5%) |         |                 |             |
| `["findfirst", "n=400", "reduce", "basesize=128"]`  | 234.532 ms (5%) |         | 405.08 KiB (1%) |        5738 |
| `["findfirst", "n=400", "reduce", "basesize=256"]`  | 227.462 ms (5%) |         | 200.89 KiB (1%) |        2874 |
| `["findfirst", "n=400", "reduce", "basesize=512"]`  | 275.145 ms (5%) |         | 127.36 KiB (1%) |        1821 |
| `["findfirst", "n=500", "foldl"]`                   |  75.396 ms (5%) |         |                 |             |
| `["findfirst", "n=500", "reduce", "basesize=128"]`  |  74.691 ms (5%) |         | 140.47 KiB (1%) |        1912 |
| `["findfirst", "n=500", "reduce", "basesize=256"]`  | 189.934 ms (5%) |         | 164.77 KiB (1%) |        2275 |
| `["findfirst", "n=500", "reduce", "basesize=512"]`  |  92.189 ms (5%) |         |  54.34 KiB (1%) |         743 |
| `["overhead", "default"]`                           |  57.397 μs (5%) |         |  32.73 KiB (1%) |         418 |
| `["overhead", "stoppable=false"]`                   |  57.758 μs (5%) |         |  32.75 KiB (1%) |         418 |
| `["overhead", "stoppable=true"]`                    |  64.277 μs (5%) |         |  44.25 KiB (1%) |         610 |
| `["parallel_histogram", "assoc", "basesize=16384"]` |   2.561 ms (5%) |         | 728.91 KiB (1%) |          57 |
| `["parallel_histogram", "assoc", "basesize=4096"]`  |   3.246 ms (5%) |         |   1.79 MiB (1%) |         216 |
| `["parallel_histogram", "assoc", "basesize=8192"]`  |   2.885 ms (5%) |         |   1.42 MiB (1%) |         117 |
| `["parallel_histogram", "comm", "basesize=16384"]`  |   8.448 ms (5%) |         |   1.56 MiB (1%) |        1792 |
| `["parallel_histogram", "comm", "basesize=4096"]`   |  13.927 ms (5%) |         |   1.33 MiB (1%) |        9612 |
| `["parallel_histogram", "comm", "basesize=8192"]`   |  12.693 ms (5%) |         |   1.25 MiB (1%) |        7183 |
| `["parallel_histogram", "seq"]`                     |   4.605 ms (5%) |         | 364.16 KiB (1%) |          24 |
| `["partition_length_maximum", "rand", "foldl"]`     |  35.416 ms (5%) |         |                 |             |
| `["partition_length_maximum", "rand", "reduce"]`    |  17.753 ms (5%) |         |  736 bytes (1%) |          11 |
| `["splitby", "count", "foldl"]`                     |   1.709 ms (5%) |         |                 |             |
| `["splitby", "count", "man"]`                       |   1.279 ms (5%) |         |                 |             |
| `["splitby", "count", "reduce"]`                    | 853.619 μs (5%) |         |   1.06 KiB (1%) |          18 |
| `["sum", "random", "foldl"]`                        |  12.363 ms (5%) |         |                 |             |
| `["sum", "random", "reduce", "basesize=128"]`       |   6.318 ms (5%) |         |  74.16 KiB (1%) |        1103 |
| `["sum", "random", "reduce", "basesize=256"]`       |   6.278 ms (5%) |         |  36.75 KiB (1%) |         546 |
| `["sum", "random", "reduce", "basesize=512"]`       |   6.238 ms (5%) |         |  18.08 KiB (1%) |         269 |
| `["sum", "uniform", "foldl"]`                       |  12.287 ms (5%) |         |                 |             |
| `["sum", "uniform", "reduce", "basesize=128"]`      |   6.326 ms (5%) |         |  74.19 KiB (1%) |        1104 |
| `["sum", "uniform", "reduce", "basesize=256"]`      |   6.243 ms (5%) |         |  36.75 KiB (1%) |         546 |
| `["sum", "uniform", "reduce", "basesize=512"]`      |   6.202 ms (5%) |         |  18.05 KiB (1%) |         268 |
| `["sum", "valley", "foldl"]`                        |  12.542 ms (5%) |         |                 |             |
| `["sum", "valley", "reduce", "basesize=128"]`       |   6.447 ms (5%) |         |  74.12 KiB (1%) |        1102 |
| `["sum", "valley", "reduce", "basesize=256"]`       |   6.369 ms (5%) |         |  36.75 KiB (1%) |         546 |
| `["sum", "valley", "reduce", "basesize=512"]`       |   6.343 ms (5%) |         |  18.08 KiB (1%) |         269 |
| `["words", "nthreads=1"]`                           |  15.976 ms (5%) |         |  31.78 MiB (1%) |     1035351 |
| `["words", "nthreads=2"]`                           |  10.127 ms (5%) |         |  32.49 MiB (1%) |     1035432 |
| `["words", "nthreads=4"]`                           |  10.758 ms (5%) |         |  33.13 MiB (1%) |     1035626 |

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
  uname: Linux 6.17.0-1013-azure #13~24.04.1-Ubuntu SMP Wed Apr 15 16:52:17 UTC 2026 x86_64 x86_64
  CPU: AMD EPYC 9V74 80-Core Processor: 
              speed         user         nice          sys         idle          irq
       #1  2871 MHz       3207 s          0 s        234 s       6297 s          0 s
       #2  2867 MHz       3666 s          0 s        213 s       5849 s          0 s
       #3  2871 MHz       3891 s          0 s        208 s       5627 s          0 s
       #4  2897 MHz       4264 s          0 s        235 s       5237 s          0 s
       
  Memory: 15.614952087402344 GB (12239.98046875 MB free)
  Uptime: 978.16 sec
  Load Avg:  1.75  1.6  1.13
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
    BogoMIPS:                                5192.26
    Flags:                                   fpu vme de pse tsc msr pae mce cx8 apic sep mtrr pge mca cmov pat pse36 clflush mmx fxsr sse sse2 ht syscall nx mmxext fxsr_opt pdpe1gb rdtscp lm constant_tsc rep_good nopl tsc_reliable nonstop_tsc cpuid extd_apicid aperfmperf tsc_known_freq pni pclmulqdq ssse3 fma cx16 pcid sse4_1 sse4_2 movbe popcnt aes xsave avx f16c rdrand hypervisor lahf_lm cmp_legacy svm cr8_legacy abm sse4a misalignsse 3dnowprefetch osvw topoext vmmcall fsgsbase bmi1 avx2 smep bmi2 erms invpcid rdseed adx smap clflushopt clwb sha_ni xsaveopt xsavec xgetbv1 xsaves user_shstk clzero xsaveerptr rdpru arat npt nrip_save tsc_scale vmcb_clean flushbyasid decodeassists pausefilter pfthreshold v_vmsave_vmload umip vaes vpclmulqdq rdpid fsrm
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
| Cores              | 16 physical cores, 16 logical cores (on executing CPU)     |
|                    | No Hyperthreading hardware capability detected             |
| Clock Frequencies  | Not supported by CPU                                       |
| Data Cache         | Level 1:3 : (32, 1024, 32768) kbytes                       |
|                    | 64 byte cache line size                                    |
| Address Size       | 48 bits virtual, 48 bits physical                          |
| SIMD               | 256 bit = 32 byte max. SIMD vector size                    |
| Time Stamp Counter | TSC is accessible via `rdtsc`                              |
|                    | TSC runs at constant rate (invariant from clock frequency) |
| Perf. Monitoring   | Performance Monitoring Counters (PMC) are not supported    |
| Hypervisor         | Yes, Microsoft                                             |

