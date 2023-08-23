# Multi-thread benchmark result

* Pull request commit: [`db2183c6d683b69a68d3dee2034624a1cb7b8e6d`](https://github.com/JuliaFolds/Transducers.jl/commit/db2183c6d683b69a68d3dee2034624a1cb7b8e6d)
* Pull request: <https://github.com/JuliaFolds/Transducers.jl/pull/243> (Update */Manifest.toml)

# Judge result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmarks:
    - Target: 23 Aug 2023 - 01:20
    - Baseline: 23 Aug 2023 - 01:25
* Package commits:
    - Target: e3d518
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
| `["findfirst", "n=1000", "reduce", "basesize=256"]` | 0.73 (5%) :white_check_mark: | 0.84 (1%) :white_check_mark: |
| `["findfirst", "n=1000", "reduce", "basesize=512"]` | 0.83 (5%) :white_check_mark: | 0.86 (1%) :white_check_mark: |
| `["findfirst", "n=400", "reduce", "basesize=128"]`  |                   0.97 (5%)  | 0.98 (1%) :white_check_mark: |
| `["findfirst", "n=400", "reduce", "basesize=512"]`  | 0.86 (5%) :white_check_mark: | 0.83 (1%) :white_check_mark: |
| `["findfirst", "n=500", "reduce", "basesize=128"]`  |                1.15 (5%) :x: |                1.15 (1%) :x: |
| `["findfirst", "n=500", "reduce", "basesize=256"]`  | 0.49 (5%) :white_check_mark: | 0.59 (1%) :white_check_mark: |
| `["parallel_histogram", "comm", "basesize=16384"]`  |                1.09 (5%) :x: |                1.06 (1%) :x: |
| `["parallel_histogram", "comm", "basesize=4096"]`   | 0.85 (5%) :white_check_mark: | 0.90 (1%) :white_check_mark: |
| `["parallel_histogram", "comm", "basesize=8192"]`   |                1.31 (5%) :x: |                1.21 (1%) :x: |
| `["partition_length_maximum", "rand", "reduce"]`    |                   1.00 (5%)  |                1.05 (1%) :x: |

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
      Ubuntu 22.04.3 LTS
  uname: Linux 5.15.0-1041-azure #48-Ubuntu SMP Tue Jun 20 20:34:08 UTC 2023 x86_64 x86_64
  CPU: Intel(R) Xeon(R) Platinum 8370C CPU @ 2.80GHz: 
              speed         user         nice          sys         idle          irq
       #1  2793 MHz       4791 s          0 s        268 s       1936 s          0 s
       #2  2793 MHz       5648 s          0 s        260 s       1067 s          0 s
       
  Memory: 6.7694854736328125 GB (3516.703125 MB free)
  Uptime: 704.56 sec
  Load Avg:  1.59  1.53  0.95
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
      Ubuntu 22.04.3 LTS
  uname: Linux 5.15.0-1041-azure #48-Ubuntu SMP Tue Jun 20 20:34:08 UTC 2023 x86_64 x86_64
  CPU: Intel(R) Xeon(R) Platinum 8370C CPU @ 2.80GHz: 
              speed         user         nice          sys         idle          irq
       #1  2793 MHz       7006 s          0 s        341 s       2714 s          0 s
       #2  2793 MHz       8138 s          0 s        332 s       1569 s          0 s
       
  Memory: 6.7694854736328125 GB (3410.77734375 MB free)
  Uptime: 1011.43 sec
  Load Avg:  1.59  1.58  1.14
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-12.0.1 (ORCJIT, icelake-server)
```

---
# Target result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmark: 23 Aug 2023 - 1:20
* Package commit: e3d518
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
| `["collect", "assoc", "basesize=1"]`                | 241.325 ms (5%) |         |   4.36 MiB (1%) |       32800 |
| `["collect", "assoc", "basesize=1024"]`             | 238.786 ms (5%) |         |   1.09 MiB (1%) |          53 |
| `["collect", "assoc", "basesize=32"]`               | 238.776 ms (5%) |         |   1.48 MiB (1%) |        1052 |
| `["collect", "seq"]`                                | 476.672 ms (5%) |         | 256.05 KiB (1%) |           2 |
| `["collect", "unordered", "basesize=1"]`            | 372.266 ms (5%) |         |  23.92 MiB (1%) |      413560 |
| `["collect", "unordered", "basesize=1024"]`         | 250.881 ms (5%) |         |   1.01 MiB (1%) |        1038 |
| `["collect", "unordered", "basesize=32"]`           | 261.993 ms (5%) |         |   1.59 MiB (1%) |       15018 |
| `["findfirst", "n=1000", "foldl"]`                  | 740.040 ms (5%) |         |                 |             |
| `["findfirst", "n=1000", "reduce", "basesize=128"]` | 405.879 ms (5%) |         | 232.86 KiB (1%) |        3276 |
| `["findfirst", "n=1000", "reduce", "basesize=256"]` | 472.723 ms (5%) |         | 151.53 KiB (1%) |        2114 |
| `["findfirst", "n=1000", "reduce", "basesize=512"]` | 579.999 ms (5%) |         |  96.75 KiB (1%) |        1346 |
| `["findfirst", "n=400", "foldl"]`                   | 555.219 ms (5%) |         |                 |             |
| `["findfirst", "n=400", "reduce", "basesize=128"]`  | 294.904 ms (5%) |         | 388.64 KiB (1%) |        5526 |
| `["findfirst", "n=400", "reduce", "basesize=256"]`  | 294.396 ms (5%) |         | 200.64 KiB (1%) |        2866 |
| `["findfirst", "n=400", "reduce", "basesize=512"]`  | 327.776 ms (5%) |         | 112.53 KiB (1%) |        1620 |
| `["findfirst", "n=500", "foldl"]`                   |  96.095 ms (5%) |         |                 |             |
| `["findfirst", "n=500", "reduce", "basesize=128"]`  | 194.703 ms (5%) |         | 228.53 KiB (1%) |        3165 |
| `["findfirst", "n=500", "reduce", "basesize=256"]`  | 135.619 ms (5%) |         | 100.34 KiB (1%) |        1377 |
| `["findfirst", "n=500", "reduce", "basesize=512"]`  | 125.197 ms (5%) |         |  56.83 KiB (1%) |         778 |
| `["overhead", "default"]`                           |  71.799 μs (5%) |         |  32.70 KiB (1%) |         417 |
| `["overhead", "stoppable=false"]`                   |  71.899 μs (5%) |         |  32.69 KiB (1%) |         416 |
| `["overhead", "stoppable=true"]`                    |  82.300 μs (5%) |         |  44.25 KiB (1%) |         610 |
| `["parallel_histogram", "assoc", "basesize=16384"]` |   3.717 ms (5%) |         | 728.91 KiB (1%) |          57 |
| `["parallel_histogram", "assoc", "basesize=4096"]`  |   4.511 ms (5%) |         |   1.79 MiB (1%) |         216 |
| `["parallel_histogram", "assoc", "basesize=8192"]`  |   4.109 ms (5%) |         |   1.42 MiB (1%) |         117 |
| `["parallel_histogram", "comm", "basesize=16384"]`  |  15.855 ms (5%) |         |   1.60 MiB (1%) |        2941 |
| `["parallel_histogram", "comm", "basesize=4096"]`   |  21.546 ms (5%) |         |   1.22 MiB (1%) |        6091 |
| `["parallel_histogram", "comm", "basesize=8192"]`   |  20.096 ms (5%) |         |   1.36 MiB (1%) |        4354 |
| `["parallel_histogram", "seq"]`                     |   6.672 ms (5%) |         | 364.16 KiB (1%) |          24 |
| `["partition_length_maximum", "rand", "foldl"]`     |  41.165 ms (5%) |         |                 |             |
| `["partition_length_maximum", "rand", "reduce"]`    |  20.593 ms (5%) |         |  736 bytes (1%) |          11 |
| `["splitby", "count", "foldl"]`                     |   2.371 ms (5%) |         |                 |             |
| `["splitby", "count", "man"]`                       |   1.528 ms (5%) |         |                 |             |
| `["splitby", "count", "reduce"]`                    |   1.108 ms (5%) |         |   1.09 KiB (1%) |          19 |
| `["sum", "random", "foldl"]`                        |  17.945 ms (5%) |         |                 |             |
| `["sum", "random", "reduce", "basesize=128"]`       |   9.173 ms (5%) |         |  74.08 KiB (1%) |        1101 |
| `["sum", "random", "reduce", "basesize=256"]`       |   9.070 ms (5%) |         |  36.67 KiB (1%) |         544 |
| `["sum", "random", "reduce", "basesize=512"]`       |   9.023 ms (5%) |         |  18.08 KiB (1%) |         269 |
| `["sum", "uniform", "foldl"]`                       |  17.722 ms (5%) |         |                 |             |
| `["sum", "uniform", "reduce", "basesize=128"]`      |   9.053 ms (5%) |         |  74.11 KiB (1%) |        1102 |
| `["sum", "uniform", "reduce", "basesize=256"]`      |   8.962 ms (5%) |         |  36.73 KiB (1%) |         546 |
| `["sum", "uniform", "reduce", "basesize=512"]`      |   8.911 ms (5%) |         |  18.03 KiB (1%) |         268 |
| `["sum", "valley", "foldl"]`                        |  18.134 ms (5%) |         |                 |             |
| `["sum", "valley", "reduce", "basesize=128"]`       |   9.261 ms (5%) |         |  74.11 KiB (1%) |        1102 |
| `["sum", "valley", "reduce", "basesize=256"]`       |   9.175 ms (5%) |         |  36.73 KiB (1%) |         546 |
| `["sum", "valley", "reduce", "basesize=512"]`       |   9.180 ms (5%) |         |  18.00 KiB (1%) |         267 |
| `["words", "nthreads=1"]`                           |  19.081 ms (5%) |         |  31.80 MiB (1%) |     1035421 |
| `["words", "nthreads=2"]`                           |  12.327 ms (5%) |         |  32.51 MiB (1%) |     1035494 |
| `["words", "nthreads=4"]`                           |  12.990 ms (5%) |         |  33.14 MiB (1%) |     1035627 |

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
      Ubuntu 22.04.3 LTS
  uname: Linux 5.15.0-1041-azure #48-Ubuntu SMP Tue Jun 20 20:34:08 UTC 2023 x86_64 x86_64
  CPU: Intel(R) Xeon(R) Platinum 8370C CPU @ 2.80GHz: 
              speed         user         nice          sys         idle          irq
       #1  2793 MHz       4791 s          0 s        268 s       1936 s          0 s
       #2  2793 MHz       5648 s          0 s        260 s       1067 s          0 s
       
  Memory: 6.7694854736328125 GB (3516.703125 MB free)
  Uptime: 704.56 sec
  Load Avg:  1.59  1.53  0.95
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-12.0.1 (ORCJIT, icelake-server)
```

---
# Baseline result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmark: 23 Aug 2023 - 1:25
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
| `["collect", "assoc", "basesize=1"]`                | 240.900 ms (5%) |         |   4.36 MiB (1%) |       32800 |
| `["collect", "assoc", "basesize=1024"]`             | 239.168 ms (5%) |         |   1.09 MiB (1%) |          54 |
| `["collect", "assoc", "basesize=32"]`               | 239.059 ms (5%) |         |   1.48 MiB (1%) |        1053 |
| `["collect", "seq"]`                                | 477.160 ms (5%) |         | 256.05 KiB (1%) |           2 |
| `["collect", "unordered", "basesize=1"]`            | 375.592 ms (5%) |         |  23.79 MiB (1%) |      409325 |
| `["collect", "unordered", "basesize=1024"]`         | 251.621 ms (5%) |         |   1.01 MiB (1%) |         956 |
| `["collect", "unordered", "basesize=32"]`           | 261.654 ms (5%) |         |   1.59 MiB (1%) |       15048 |
| `["findfirst", "n=1000", "foldl"]`                  | 737.887 ms (5%) |         |                 |             |
| `["findfirst", "n=1000", "reduce", "basesize=128"]` | 403.140 ms (5%) |         | 232.67 KiB (1%) |        3270 |
| `["findfirst", "n=1000", "reduce", "basesize=256"]` | 647.709 ms (5%) |         | 180.20 KiB (1%) |        2563 |
| `["findfirst", "n=1000", "reduce", "basesize=512"]` | 699.408 ms (5%) |         | 112.67 KiB (1%) |        1571 |
| `["findfirst", "n=400", "foldl"]`                   | 553.799 ms (5%) |         |                 |             |
| `["findfirst", "n=400", "reduce", "basesize=128"]`  | 302.558 ms (5%) |         | 398.19 KiB (1%) |        5650 |
| `["findfirst", "n=400", "reduce", "basesize=256"]`  | 291.296 ms (5%) |         | 200.89 KiB (1%) |        2874 |
| `["findfirst", "n=400", "reduce", "basesize=512"]`  | 380.496 ms (5%) |         | 136.05 KiB (1%) |        1941 |
| `["findfirst", "n=500", "foldl"]`                   |  95.753 ms (5%) |         |                 |             |
| `["findfirst", "n=500", "reduce", "basesize=128"]`  | 169.075 ms (5%) |         | 199.19 KiB (1%) |        2757 |
| `["findfirst", "n=500", "reduce", "basesize=256"]`  | 275.122 ms (5%) |         | 170.78 KiB (1%) |        2384 |
| `["findfirst", "n=500", "reduce", "basesize=512"]`  | 124.325 ms (5%) |         |  56.83 KiB (1%) |         778 |
| `["overhead", "default"]`                           |  74.999 μs (5%) |         |  32.67 KiB (1%) |         416 |
| `["overhead", "stoppable=false"]`                   |  75.399 μs (5%) |         |  32.75 KiB (1%) |         418 |
| `["overhead", "stoppable=true"]`                    |  85.700 μs (5%) |         |  44.25 KiB (1%) |         610 |
| `["parallel_histogram", "assoc", "basesize=16384"]` |   3.732 ms (5%) |         | 728.91 KiB (1%) |          57 |
| `["parallel_histogram", "assoc", "basesize=4096"]`  |   4.515 ms (5%) |         |   1.79 MiB (1%) |         215 |
| `["parallel_histogram", "assoc", "basesize=8192"]`  |   4.126 ms (5%) |         |   1.42 MiB (1%) |         117 |
| `["parallel_histogram", "comm", "basesize=16384"]`  |  14.582 ms (5%) |         |   1.51 MiB (1%) |         144 |
| `["parallel_histogram", "comm", "basesize=4096"]`   |  25.435 ms (5%) |         |   1.35 MiB (1%) |       10455 |
| `["parallel_histogram", "comm", "basesize=8192"]`   |  15.367 ms (5%) |         |   1.12 MiB (1%) |        2825 |
| `["parallel_histogram", "seq"]`                     |   6.635 ms (5%) |         | 364.16 KiB (1%) |          24 |
| `["partition_length_maximum", "rand", "foldl"]`     |  41.194 ms (5%) |         |                 |             |
| `["partition_length_maximum", "rand", "reduce"]`    |  20.633 ms (5%) |         |  704 bytes (1%) |          10 |
| `["splitby", "count", "foldl"]`                     |   2.283 ms (5%) |         |                 |             |
| `["splitby", "count", "man"]`                       |   1.529 ms (5%) |         |                 |             |
| `["splitby", "count", "reduce"]`                    |   1.079 ms (5%) |         |   1.09 KiB (1%) |          19 |
| `["sum", "random", "foldl"]`                        |  18.084 ms (5%) |         |                 |             |
| `["sum", "random", "reduce", "basesize=128"]`       |   9.211 ms (5%) |         |  74.17 KiB (1%) |        1104 |
| `["sum", "random", "reduce", "basesize=256"]`       |   9.148 ms (5%) |         |  36.70 KiB (1%) |         545 |
| `["sum", "random", "reduce", "basesize=512"]`       |   9.087 ms (5%) |         |  18.11 KiB (1%) |         270 |
| `["sum", "uniform", "foldl"]`                       |  17.733 ms (5%) |         |                 |             |
| `["sum", "uniform", "reduce", "basesize=128"]`      |   9.048 ms (5%) |         |  74.11 KiB (1%) |        1102 |
| `["sum", "uniform", "reduce", "basesize=256"]`      |   8.962 ms (5%) |         |  36.73 KiB (1%) |         546 |
| `["sum", "uniform", "reduce", "basesize=512"]`      |   8.913 ms (5%) |         |  18.03 KiB (1%) |         268 |
| `["sum", "valley", "foldl"]`                        |  18.150 ms (5%) |         |                 |             |
| `["sum", "valley", "reduce", "basesize=128"]`       |   9.283 ms (5%) |         |  74.14 KiB (1%) |        1103 |
| `["sum", "valley", "reduce", "basesize=256"]`       |   9.196 ms (5%) |         |  36.70 KiB (1%) |         545 |
| `["sum", "valley", "reduce", "basesize=512"]`       |   9.173 ms (5%) |         |  18.00 KiB (1%) |         267 |
| `["words", "nthreads=1"]`                           |  18.787 ms (5%) |         |  31.71 MiB (1%) |     1033207 |
| `["words", "nthreads=2"]`                           |  12.490 ms (5%) |         |  32.43 MiB (1%) |     1033298 |
| `["words", "nthreads=4"]`                           |  12.749 ms (5%) |         |  32.88 MiB (1%) |     1033371 |

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
      Ubuntu 22.04.3 LTS
  uname: Linux 5.15.0-1041-azure #48-Ubuntu SMP Tue Jun 20 20:34:08 UTC 2023 x86_64 x86_64
  CPU: Intel(R) Xeon(R) Platinum 8370C CPU @ 2.80GHz: 
              speed         user         nice          sys         idle          irq
       #1  2793 MHz       7006 s          0 s        341 s       2714 s          0 s
       #2  2793 MHz       8138 s          0 s        332 s       1569 s          0 s
       
  Memory: 6.7694854736328125 GB (3410.77734375 MB free)
  Uptime: 1011.43 sec
  Load Avg:  1.59  1.58  1.14
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

