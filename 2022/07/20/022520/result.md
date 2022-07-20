# Multi-thread benchmark result

* Pull request commit: [`d2a2a9ad3616bc07e95a3a045519737ab9434f43`](https://github.com/JuliaFolds/Transducers.jl/commit/d2a2a9ad3616bc07e95a3a045519737ab9434f43)
* Pull request: <https://github.com/JuliaFolds/Transducers.jl/pull/243> (Update */Manifest.toml)

# Judge result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmarks:
    - Target: 20 Jul 2022 - 02:19
    - Baseline: 20 Jul 2022 - 02:24
* Package commits:
    - Target: 7387b2
    - Baseline: 6125fe
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
| `["findfirst", "n=1000", "reduce", "basesize=128"]` | 0.84 (5%) :white_check_mark: | 0.88 (1%) :white_check_mark: |
| `["findfirst", "n=1000", "reduce", "basesize=256"]` |                1.12 (5%) :x: |                1.18 (1%) :x: |
| `["findfirst", "n=400", "reduce", "basesize=128"]`  |                   1.02 (5%)  |                1.03 (1%) :x: |
| `["findfirst", "n=400", "reduce", "basesize=512"]`  |                1.23 (5%) :x: |                1.15 (1%) :x: |
| `["findfirst", "n=500", "reduce", "basesize=128"]`  |                   1.00 (5%)  | 0.98 (1%) :white_check_mark: |
| `["findfirst", "n=500", "reduce", "basesize=256"]`  | 0.40 (5%) :white_check_mark: | 0.50 (1%) :white_check_mark: |
| `["findfirst", "n=500", "reduce", "basesize=512"]`  |                1.53 (5%) :x: |                1.42 (1%) :x: |
| `["parallel_histogram", "comm", "basesize=16384"]`  |                   1.00 (5%)  | 0.99 (1%) :white_check_mark: |
| `["parallel_histogram", "comm", "basesize=4096"]`   |                   1.05 (5%)  |                1.04 (1%) :x: |
| `["parallel_histogram", "comm", "basesize=8192"]`   |                   0.98 (5%)  | 0.98 (1%) :white_check_mark: |

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
      Ubuntu 20.04.4 LTS
  uname: Linux 5.15.0-1014-azure #17~20.04.1-Ubuntu SMP Thu Jun 23 20:01:51 UTC 2022 x86_64 x86_64
  CPU: Intel(R) Xeon(R) Platinum 8370C CPU @ 2.80GHz: 
              speed         user         nice          sys         idle          irq
       #1  2793 MHz       5520 s          1 s        269 s       4436 s          0 s
       #2  2793 MHz       4804 s          1 s        268 s       5167 s          0 s
       
  Memory: 6.780967712402344 GB (3398.8671875 MB free)
  Uptime: 1029.27 sec
  Load Avg:  1.8  1.55  0.93
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
      Ubuntu 20.04.4 LTS
  uname: Linux 5.15.0-1014-azure #17~20.04.1-Ubuntu SMP Thu Jun 23 20:01:51 UTC 2022 x86_64 x86_64
  CPU: Intel(R) Xeon(R) Platinum 8370C CPU @ 2.80GHz: 
              speed         user         nice          sys         idle          irq
       #1  2793 MHz       8028 s          1 s        341 s       4946 s          0 s
       #2  2793 MHz       7038 s          1 s        353 s       5937 s          0 s
       
  Memory: 6.780967712402344 GB (3432.28125 MB free)
  Uptime: 1338.79 sec
  Load Avg:  1.74  1.74  1.2
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-12.0.1 (ORCJIT, icelake-server)
```

---
# Target result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmark: 20 Jul 2022 - 2:19
* Package commit: 7387b2
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
| `["collect", "assoc", "basesize=1"]`                | 286.880 ms (5%) |         |  25.97 MiB (1%) |      306773 |
| `["collect", "assoc", "basesize=1024"]`             | 239.070 ms (5%) |         |   2.61 MiB (1%) |         456 |
| `["collect", "assoc", "basesize=32"]`               | 241.442 ms (5%) |         |   4.82 MiB (1%) |       11695 |
| `["collect", "seq"]`                                | 476.883 ms (5%) |         | 812.73 KiB (1%) |          11 |
| `["collect", "unordered", "basesize=1"]`            | 425.948 ms (5%) |         |  23.98 MiB (1%) |      415557 |
| `["collect", "unordered", "basesize=1024"]`         | 253.016 ms (5%) |         |   1.01 MiB (1%) |        1000 |
| `["collect", "unordered", "basesize=32"]`           | 266.089 ms (5%) |         |   1.59 MiB (1%) |       15137 |
| `["findfirst", "n=1000", "foldl"]`                  | 736.888 ms (5%) |         |                 |             |
| `["findfirst", "n=1000", "reduce", "basesize=128"]` | 475.895 ms (5%) |         | 274.80 KiB (1%) |        3852 |
| `["findfirst", "n=1000", "reduce", "basesize=256"]` | 499.238 ms (5%) |         | 157.23 KiB (1%) |        2194 |
| `["findfirst", "n=1000", "reduce", "basesize=512"]` | 661.402 ms (5%) |         | 108.55 KiB (1%) |        1509 |
| `["findfirst", "n=400", "foldl"]`                   | 553.399 ms (5%) |         |                 |             |
| `["findfirst", "n=400", "reduce", "basesize=128"]`  | 296.974 ms (5%) |         | 400.27 KiB (1%) |        5690 |
| `["findfirst", "n=400", "reduce", "basesize=256"]`  | 292.165 ms (5%) |         | 200.89 KiB (1%) |        2874 |
| `["findfirst", "n=400", "reduce", "basesize=512"]`  | 449.225 ms (5%) |         | 153.14 KiB (1%) |        2194 |
| `["findfirst", "n=500", "foldl"]`                   |  95.839 ms (5%) |         |                 |             |
| `["findfirst", "n=500", "reduce", "basesize=128"]`  | 165.465 ms (5%) |         | 203.72 KiB (1%) |        2813 |
| `["findfirst", "n=500", "reduce", "basesize=256"]`  |  90.360 ms (5%) |         |  72.12 KiB (1%) |         980 |
| `["findfirst", "n=500", "reduce", "basesize=512"]`  | 137.172 ms (5%) |         |  63.69 KiB (1%) |         866 |
| `["overhead", "default"]`                           |  73.503 μs (5%) |         |  32.73 KiB (1%) |         418 |
| `["overhead", "stoppable=false"]`                   |  74.304 μs (5%) |         |  32.72 KiB (1%) |         417 |
| `["overhead", "stoppable=true"]`                    |  84.304 μs (5%) |         |  44.25 KiB (1%) |         610 |
| `["parallel_histogram", "assoc", "basesize=16384"]` |   3.718 ms (5%) |         | 728.91 KiB (1%) |          57 |
| `["parallel_histogram", "assoc", "basesize=4096"]`  |   4.561 ms (5%) |         |   1.79 MiB (1%) |         216 |
| `["parallel_histogram", "assoc", "basesize=8192"]`  |   4.104 ms (5%) |         |   1.42 MiB (1%) |         117 |
| `["parallel_histogram", "comm", "basesize=16384"]`  |  16.824 ms (5%) |         |   1.67 MiB (1%) |        5519 |
| `["parallel_histogram", "comm", "basesize=4096"]`   |  26.425 ms (5%) |         |   1.41 MiB (1%) |       12442 |
| `["parallel_histogram", "comm", "basesize=8192"]`   |  21.872 ms (5%) |         |   1.33 MiB (1%) |        9671 |
| `["parallel_histogram", "seq"]`                     |   6.655 ms (5%) |         | 364.16 KiB (1%) |          24 |
| `["partition_length_maximum", "rand", "foldl"]`     |  41.219 ms (5%) |         |                 |             |
| `["partition_length_maximum", "rand", "reduce"]`    |  20.615 ms (5%) |         |  736 bytes (1%) |          11 |
| `["splitby", "count", "foldl"]`                     |   2.325 ms (5%) |         |                 |             |
| `["splitby", "count", "man"]`                       |   1.528 ms (5%) |         |                 |             |
| `["splitby", "count", "reduce"]`                    |   1.084 ms (5%) |         |   1.09 KiB (1%) |          19 |
| `["sum", "random", "foldl"]`                        |  18.070 ms (5%) |         |                 |             |
| `["sum", "random", "reduce", "basesize=128"]`       |   9.262 ms (5%) |         |  74.23 KiB (1%) |        1106 |
| `["sum", "random", "reduce", "basesize=256"]`       |   9.189 ms (5%) |         |  36.77 KiB (1%) |         547 |
| `["sum", "random", "reduce", "basesize=512"]`       |   9.127 ms (5%) |         |  18.08 KiB (1%) |         269 |
| `["sum", "uniform", "foldl"]`                       |  17.736 ms (5%) |         |                 |             |
| `["sum", "uniform", "reduce", "basesize=128"]`      |   9.101 ms (5%) |         |  74.17 KiB (1%) |        1104 |
| `["sum", "uniform", "reduce", "basesize=256"]`      |   8.995 ms (5%) |         |  36.77 KiB (1%) |         547 |
| `["sum", "uniform", "reduce", "basesize=512"]`      |   8.934 ms (5%) |         |  18.03 KiB (1%) |         268 |
| `["sum", "valley", "foldl"]`                        |  18.146 ms (5%) |         |                 |             |
| `["sum", "valley", "reduce", "basesize=128"]`       |   9.298 ms (5%) |         |  74.14 KiB (1%) |        1103 |
| `["sum", "valley", "reduce", "basesize=256"]`       |   9.216 ms (5%) |         |  36.70 KiB (1%) |         545 |
| `["sum", "valley", "reduce", "basesize=512"]`       |   9.222 ms (5%) |         |  18.00 KiB (1%) |         267 |
| `["words", "nthreads=1"]`                           |  19.161 ms (5%) |         |  31.64 MiB (1%) |     1031145 |
| `["words", "nthreads=2"]`                           |  12.626 ms (5%) |         |  32.36 MiB (1%) |     1031223 |
| `["words", "nthreads=4"]`                           |  13.100 ms (5%) |         |  32.98 MiB (1%) |     1031373 |

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
      Ubuntu 20.04.4 LTS
  uname: Linux 5.15.0-1014-azure #17~20.04.1-Ubuntu SMP Thu Jun 23 20:01:51 UTC 2022 x86_64 x86_64
  CPU: Intel(R) Xeon(R) Platinum 8370C CPU @ 2.80GHz: 
              speed         user         nice          sys         idle          irq
       #1  2793 MHz       5520 s          1 s        269 s       4436 s          0 s
       #2  2793 MHz       4804 s          1 s        268 s       5167 s          0 s
       
  Memory: 6.780967712402344 GB (3398.8671875 MB free)
  Uptime: 1029.27 sec
  Load Avg:  1.8  1.55  0.93
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-12.0.1 (ORCJIT, icelake-server)
```

---
# Baseline result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmark: 20 Jul 2022 - 2:24
* Package commit: 6125fe
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
| `["collect", "assoc", "basesize=1"]`                | 284.731 ms (5%) |         |  25.97 MiB (1%) |      306817 |
| `["collect", "assoc", "basesize=1024"]`             | 239.738 ms (5%) |         |   2.61 MiB (1%) |         456 |
| `["collect", "assoc", "basesize=32"]`               | 241.943 ms (5%) |         |   4.82 MiB (1%) |       11707 |
| `["collect", "seq"]`                                | 478.123 ms (5%) |         | 812.73 KiB (1%) |          11 |
| `["collect", "unordered", "basesize=1"]`            | 420.286 ms (5%) |         |  23.98 MiB (1%) |      415713 |
| `["collect", "unordered", "basesize=1024"]`         | 252.189 ms (5%) |         |   1.01 MiB (1%) |        1146 |
| `["collect", "unordered", "basesize=32"]`           | 265.347 ms (5%) |         |   1.60 MiB (1%) |       15187 |
| `["findfirst", "n=1000", "foldl"]`                  | 736.409 ms (5%) |         |                 |             |
| `["findfirst", "n=1000", "reduce", "basesize=128"]` | 567.837 ms (5%) |         | 311.16 KiB (1%) |        4372 |
| `["findfirst", "n=1000", "reduce", "basesize=256"]` | 446.142 ms (5%) |         | 133.81 KiB (1%) |        1891 |
| `["findfirst", "n=1000", "reduce", "basesize=512"]` | 661.104 ms (5%) |         | 108.55 KiB (1%) |        1509 |
| `["findfirst", "n=400", "foldl"]`                   | 552.496 ms (5%) |         |                 |             |
| `["findfirst", "n=400", "reduce", "basesize=128"]`  | 290.976 ms (5%) |         | 389.11 KiB (1%) |        5538 |
| `["findfirst", "n=400", "reduce", "basesize=256"]`  | 290.614 ms (5%) |         | 200.89 KiB (1%) |        2874 |
| `["findfirst", "n=400", "reduce", "basesize=512"]`  | 365.246 ms (5%) |         | 132.88 KiB (1%) |        1893 |
| `["findfirst", "n=500", "foldl"]`                   |  95.776 ms (5%) |         |                 |             |
| `["findfirst", "n=500", "reduce", "basesize=128"]`  | 165.758 ms (5%) |         | 207.88 KiB (1%) |        2846 |
| `["findfirst", "n=500", "reduce", "basesize=256"]`  | 227.969 ms (5%) |         | 145.67 KiB (1%) |        2020 |
| `["findfirst", "n=500", "reduce", "basesize=512"]`  |  89.851 ms (5%) |         |  44.73 KiB (1%) |         604 |
| `["overhead", "default"]`                           |  73.504 μs (5%) |         |  32.73 KiB (1%) |         418 |
| `["overhead", "stoppable=false"]`                   |  72.903 μs (5%) |         |  32.75 KiB (1%) |         418 |
| `["overhead", "stoppable=true"]`                    |  86.704 μs (5%) |         |  44.22 KiB (1%) |         609 |
| `["parallel_histogram", "assoc", "basesize=16384"]` |   3.738 ms (5%) |         | 728.91 KiB (1%) |          57 |
| `["parallel_histogram", "assoc", "basesize=4096"]`  |   4.508 ms (5%) |         |   1.79 MiB (1%) |         216 |
| `["parallel_histogram", "assoc", "basesize=8192"]`  |   4.145 ms (5%) |         |   1.42 MiB (1%) |         117 |
| `["parallel_histogram", "comm", "basesize=16384"]`  |  16.904 ms (5%) |         |   1.70 MiB (1%) |        6235 |
| `["parallel_histogram", "comm", "basesize=4096"]`   |  25.184 ms (5%) |         |   1.35 MiB (1%) |       10554 |
| `["parallel_histogram", "comm", "basesize=8192"]`   |  22.356 ms (5%) |         |   1.36 MiB (1%) |        9826 |
| `["parallel_histogram", "seq"]`                     |   6.653 ms (5%) |         | 364.16 KiB (1%) |          24 |
| `["partition_length_maximum", "rand", "foldl"]`     |  41.164 ms (5%) |         |                 |             |
| `["partition_length_maximum", "rand", "reduce"]`    |  20.611 ms (5%) |         |  736 bytes (1%) |          11 |
| `["splitby", "count", "foldl"]`                     |   2.276 ms (5%) |         |                 |             |
| `["splitby", "count", "man"]`                       |   1.528 ms (5%) |         |                 |             |
| `["splitby", "count", "reduce"]`                    |   1.106 ms (5%) |         |   1.09 KiB (1%) |          19 |
| `["sum", "random", "foldl"]`                        |  18.132 ms (5%) |         |                 |             |
| `["sum", "random", "reduce", "basesize=128"]`       |   9.328 ms (5%) |         |  74.17 KiB (1%) |        1104 |
| `["sum", "random", "reduce", "basesize=256"]`       |   9.200 ms (5%) |         |  36.67 KiB (1%) |         544 |
| `["sum", "random", "reduce", "basesize=512"]`       |   9.150 ms (5%) |         |  18.08 KiB (1%) |         269 |
| `["sum", "uniform", "foldl"]`                       |  17.725 ms (5%) |         |                 |             |
| `["sum", "uniform", "reduce", "basesize=128"]`      |   9.078 ms (5%) |         |  74.14 KiB (1%) |        1103 |
| `["sum", "uniform", "reduce", "basesize=256"]`      |   9.002 ms (5%) |         |  36.73 KiB (1%) |         546 |
| `["sum", "uniform", "reduce", "basesize=512"]`      |   8.950 ms (5%) |         |  18.03 KiB (1%) |         268 |
| `["sum", "valley", "foldl"]`                        |  18.137 ms (5%) |         |                 |             |
| `["sum", "valley", "reduce", "basesize=128"]`       |   9.315 ms (5%) |         |  74.20 KiB (1%) |        1105 |
| `["sum", "valley", "reduce", "basesize=256"]`       |   9.217 ms (5%) |         |  36.77 KiB (1%) |         547 |
| `["sum", "valley", "reduce", "basesize=512"]`       |   9.214 ms (5%) |         |  18.03 KiB (1%) |         268 |
| `["words", "nthreads=1"]`                           |  19.279 ms (5%) |         |  31.81 MiB (1%) |     1036494 |
| `["words", "nthreads=2"]`                           |  12.359 ms (5%) |         |  32.17 MiB (1%) |     1036530 |
| `["words", "nthreads=4"]`                           |  13.109 ms (5%) |         |  33.07 MiB (1%) |     1036709 |

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
      Ubuntu 20.04.4 LTS
  uname: Linux 5.15.0-1014-azure #17~20.04.1-Ubuntu SMP Thu Jun 23 20:01:51 UTC 2022 x86_64 x86_64
  CPU: Intel(R) Xeon(R) Platinum 8370C CPU @ 2.80GHz: 
              speed         user         nice          sys         idle          irq
       #1  2793 MHz       8028 s          1 s        341 s       4946 s          0 s
       #2  2793 MHz       7038 s          1 s        353 s       5937 s          0 s
       
  Memory: 6.780967712402344 GB (3432.28125 MB free)
  Uptime: 1338.79 sec
  Load Avg:  1.74  1.74  1.2
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
    Byte Order:                      Little Endian
    Address sizes:                   46 bits physical, 48 bits virtual
    CPU(s):                          2
    On-line CPU(s) list:             0,1
    Thread(s) per core:              1
    Core(s) per socket:              2
    Socket(s):                       1
    NUMA node(s):                    1
    Vendor ID:                       GenuineIntel
    CPU family:                      6
    Model:                           106
    Model name:                      Intel(R) Xeon(R) Platinum 8370C CPU @ 2.80GHz
    Stepping:                        6
    CPU MHz:                         2793.602
    BogoMIPS:                        5587.20
    Hypervisor vendor:               Microsoft
    Virtualization type:             full
    L1d cache:                       96 KiB
    L1i cache:                       64 KiB
    L2 cache:                        2.5 MiB
    L3 cache:                        48 MiB
    NUMA node0 CPU(s):               0,1
    Vulnerability Itlb multihit:     KVM: Mitigation: VMX unsupported
    Vulnerability L1tf:              Mitigation; PTE Inversion
    Vulnerability Mds:               Mitigation; Clear CPU buffers; SMT Host state unknown
    Vulnerability Meltdown:          Mitigation; PTI
    Vulnerability Mmio stale data:   Vulnerable: Clear CPU buffers attempted, no microcode; SMT Host state unknown
    Vulnerability Spec store bypass: Vulnerable
    Vulnerability Spectre v1:        Mitigation; usercopy/swapgs barriers and __user pointer sanitization
    Vulnerability Spectre v2:        Mitigation; Retpolines, STIBP disabled, RSB filling
    Vulnerability Srbds:             Not affected
    Vulnerability Tsx async abort:   Mitigation; Clear CPU buffers; SMT Host state unknown
    Flags:                           fpu vme de pse tsc msr pae mce cx8 apic sep mtrr pge mca cmov pat pse36 clflush mmx fxsr sse sse2 ss ht syscall nx pdpe1gb rdtscp lm constant_tsc rep_good nopl xtopology cpuid pni pclmulqdq ssse3 fma cx16 pcid sse4_1 sse4_2 movbe popcnt aes xsave avx f16c rdrand hypervisor lahf_lm abm 3dnowprefetch invpcid_single pti fsgsbase bmi1 hle avx2 smep bmi2 erms invpcid rtm avx512f avx512dq rdseed adx smap clflushopt avx512cd avx512bw avx512vl xsaveopt xsavec xsaves md_clear
    

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

