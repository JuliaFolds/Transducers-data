# Multi-thread benchmark result

* Pull request commit: [`dda66629ce694bbf766995393cc64b69577eee4f`](https://github.com/JuliaFolds/Transducers.jl/commit/dda66629ce694bbf766995393cc64b69577eee4f)
* Pull request: <https://github.com/JuliaFolds/Transducers.jl/pull/243> (Update */Manifest.toml)

# Judge result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmarks:
    - Target: 5 Aug 2022 - 02:16
    - Baseline: 5 Aug 2022 - 02:22
* Package commits:
    - Target: 9ab5b2
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
| `["findfirst", "n=1000", "reduce", "basesize=128"]` |                1.25 (5%) :x: |                1.34 (1%) :x: |
| `["findfirst", "n=1000", "reduce", "basesize=256"]` | 0.83 (5%) :white_check_mark: | 0.80 (1%) :white_check_mark: |
| `["findfirst", "n=400", "reduce", "basesize=128"]`  |                   1.03 (5%)  |                1.04 (1%) :x: |
| `["findfirst", "n=400", "reduce", "basesize=256"]`  |                   0.97 (5%)  | 0.97 (1%) :white_check_mark: |
| `["findfirst", "n=400", "reduce", "basesize=512"]`  | 0.90 (5%) :white_check_mark: | 0.95 (1%) :white_check_mark: |
| `["findfirst", "n=500", "reduce", "basesize=256"]`  | 0.78 (5%) :white_check_mark: | 0.75 (1%) :white_check_mark: |
| `["findfirst", "n=500", "reduce", "basesize=512"]`  | 0.78 (5%) :white_check_mark: | 0.92 (1%) :white_check_mark: |
| `["parallel_histogram", "comm", "basesize=4096"]`   |                   1.00 (5%)  |                1.17 (1%) :x: |
| `["parallel_histogram", "comm", "basesize=8192"]`   | 0.95 (5%) :white_check_mark: | 0.90 (1%) :white_check_mark: |
| `["splitby", "count", "reduce"]`                    |                1.06 (5%) :x: |                   1.00 (1%)  |

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
       #1  2793 MHz       4449 s          1 s        192 s       3178 s          0 s
       #2  2793 MHz       5755 s          1 s        207 s       1870 s          0 s
       
  Memory: 6.780967712402344 GB (3436.94921875 MB free)
  Uptime: 787.9 sec
  Load Avg:  1.73  1.51  0.9
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
       #1  2793 MHz       6993 s          1 s        242 s       3640 s          0 s
       #2  2793 MHz       7952 s          1 s        268 s       2668 s          0 s
       
  Memory: 6.780967712402344 GB (3357.90234375 MB free)
  Uptime: 1093.82 sec
  Load Avg:  1.61  1.59  1.11
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-12.0.1 (ORCJIT, icelake-server)
```

---
# Target result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmark: 5 Aug 2022 - 2:16
* Package commit: 9ab5b2
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
| `["collect", "assoc", "basesize=1"]`                | 279.559 ms (5%) |         |  25.97 MiB (1%) |      306803 |
| `["collect", "assoc", "basesize=1024"]`             | 238.558 ms (5%) |         |   2.61 MiB (1%) |         456 |
| `["collect", "assoc", "basesize=32"]`               | 240.358 ms (5%) |         |   4.82 MiB (1%) |       11712 |
| `["collect", "seq"]`                                | 477.915 ms (5%) |         | 812.73 KiB (1%) |          11 |
| `["collect", "unordered", "basesize=1"]`            | 373.957 ms (5%) |         |  23.91 MiB (1%) |      413435 |
| `["collect", "unordered", "basesize=1024"]`         | 250.905 ms (5%) |         |   1.01 MiB (1%) |        1054 |
| `["collect", "unordered", "basesize=32"]`           | 261.768 ms (5%) |         |   1.59 MiB (1%) |       15054 |
| `["findfirst", "n=1000", "foldl"]`                  | 736.347 ms (5%) |         |                 |             |
| `["findfirst", "n=1000", "reduce", "basesize=128"]` | 501.531 ms (5%) |         | 299.38 KiB (1%) |        4167 |
| `["findfirst", "n=1000", "reduce", "basesize=256"]` | 447.974 ms (5%) |         | 136.02 KiB (1%) |        1916 |
| `["findfirst", "n=1000", "reduce", "basesize=512"]` | 660.513 ms (5%) |         | 108.55 KiB (1%) |        1509 |
| `["findfirst", "n=400", "foldl"]`                   | 551.686 ms (5%) |         |                 |             |
| `["findfirst", "n=400", "reduce", "basesize=128"]`  | 295.292 ms (5%) |         | 397.41 KiB (1%) |        5636 |
| `["findfirst", "n=400", "reduce", "basesize=256"]`  | 289.600 ms (5%) |         | 200.88 KiB (1%) |        2874 |
| `["findfirst", "n=400", "reduce", "basesize=512"]`  | 356.616 ms (5%) |         | 130.28 KiB (1%) |        1852 |
| `["findfirst", "n=500", "foldl"]`                   |  95.668 ms (5%) |         |                 |             |
| `["findfirst", "n=500", "reduce", "basesize=128"]`  | 131.374 ms (5%) |         | 175.53 KiB (1%) |        2410 |
| `["findfirst", "n=500", "reduce", "basesize=256"]`  | 163.406 ms (5%) |         | 116.41 KiB (1%) |        1598 |
| `["findfirst", "n=500", "reduce", "basesize=512"]`  |  96.954 ms (5%) |         |  50.78 KiB (1%) |         679 |
| `["overhead", "default"]`                           |  71.900 μs (5%) |         |  32.70 KiB (1%) |         417 |
| `["overhead", "stoppable=false"]`                   |  71.900 μs (5%) |         |  32.75 KiB (1%) |         418 |
| `["overhead", "stoppable=true"]`                    |  80.200 μs (5%) |         |  44.25 KiB (1%) |         610 |
| `["parallel_histogram", "assoc", "basesize=16384"]` |   3.728 ms (5%) |         | 728.91 KiB (1%) |          57 |
| `["parallel_histogram", "assoc", "basesize=4096"]`  |   4.524 ms (5%) |         |   1.79 MiB (1%) |         216 |
| `["parallel_histogram", "assoc", "basesize=8192"]`  |   4.130 ms (5%) |         |   1.42 MiB (1%) |         117 |
| `["parallel_histogram", "comm", "basesize=16384"]`  |  16.131 ms (5%) |         |   1.70 MiB (1%) |        6276 |
| `["parallel_histogram", "comm", "basesize=4096"]`   |  24.718 ms (5%) |         |   1.41 MiB (1%) |       12525 |
| `["parallel_histogram", "comm", "basesize=8192"]`   |  20.881 ms (5%) |         |   1.24 MiB (1%) |        2521 |
| `["parallel_histogram", "seq"]`                     |   6.659 ms (5%) |         | 364.16 KiB (1%) |          24 |
| `["partition_length_maximum", "rand", "foldl"]`     |  41.209 ms (5%) |         |                 |             |
| `["partition_length_maximum", "rand", "reduce"]`    |  20.582 ms (5%) |         |  736 bytes (1%) |          11 |
| `["splitby", "count", "foldl"]`                     |   2.310 ms (5%) |         |                 |             |
| `["splitby", "count", "man"]`                       |   1.528 ms (5%) |         |                 |             |
| `["splitby", "count", "reduce"]`                    |   1.152 ms (5%) |         |   1.09 KiB (1%) |          19 |
| `["sum", "random", "foldl"]`                        |  17.932 ms (5%) |         |                 |             |
| `["sum", "random", "reduce", "basesize=128"]`       |   9.172 ms (5%) |         |  74.11 KiB (1%) |        1102 |
| `["sum", "random", "reduce", "basesize=256"]`       |   9.078 ms (5%) |         |  36.73 KiB (1%) |         546 |
| `["sum", "random", "reduce", "basesize=512"]`       |   9.028 ms (5%) |         |  18.08 KiB (1%) |         269 |
| `["sum", "uniform", "foldl"]`                       |  17.723 ms (5%) |         |                 |             |
| `["sum", "uniform", "reduce", "basesize=128"]`      |   9.062 ms (5%) |         |  74.23 KiB (1%) |        1106 |
| `["sum", "uniform", "reduce", "basesize=256"]`      |   8.955 ms (5%) |         |  36.80 KiB (1%) |         548 |
| `["sum", "uniform", "reduce", "basesize=512"]`      |   8.911 ms (5%) |         |  17.97 KiB (1%) |         266 |
| `["sum", "valley", "foldl"]`                        |  18.134 ms (5%) |         |                 |             |
| `["sum", "valley", "reduce", "basesize=128"]`       |   9.270 ms (5%) |         |  74.08 KiB (1%) |        1101 |
| `["sum", "valley", "reduce", "basesize=256"]`       |   9.194 ms (5%) |         |  36.70 KiB (1%) |         545 |
| `["sum", "valley", "reduce", "basesize=512"]`       |   9.190 ms (5%) |         |  18.03 KiB (1%) |         268 |
| `["words", "nthreads=1"]`                           |  19.055 ms (5%) |         |  31.98 MiB (1%) |     1042534 |
| `["words", "nthreads=2"]`                           |  11.869 ms (5%) |         |  32.34 MiB (1%) |     1042570 |
| `["words", "nthreads=4"]`                           |  12.560 ms (5%) |         |  33.05 MiB (1%) |     1042643 |

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
       #1  2793 MHz       4449 s          1 s        192 s       3178 s          0 s
       #2  2793 MHz       5755 s          1 s        207 s       1870 s          0 s
       
  Memory: 6.780967712402344 GB (3436.94921875 MB free)
  Uptime: 787.9 sec
  Load Avg:  1.73  1.51  0.9
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-12.0.1 (ORCJIT, icelake-server)
```

---
# Baseline result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmark: 5 Aug 2022 - 2:22
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
| `["collect", "assoc", "basesize=1"]`                | 280.707 ms (5%) |         |  25.97 MiB (1%) |      306777 |
| `["collect", "assoc", "basesize=1024"]`             | 239.152 ms (5%) |         |   2.61 MiB (1%) |         456 |
| `["collect", "assoc", "basesize=32"]`               | 241.146 ms (5%) |         |   4.82 MiB (1%) |       11712 |
| `["collect", "seq"]`                                | 477.188 ms (5%) |         | 812.73 KiB (1%) |          11 |
| `["collect", "unordered", "basesize=1"]`            | 379.611 ms (5%) |         |  23.90 MiB (1%) |      412935 |
| `["collect", "unordered", "basesize=1024"]`         | 251.113 ms (5%) |         |   1.01 MiB (1%) |        1046 |
| `["collect", "unordered", "basesize=32"]`           | 262.043 ms (5%) |         |   1.59 MiB (1%) |       15119 |
| `["findfirst", "n=1000", "foldl"]`                  | 739.159 ms (5%) |         |                 |             |
| `["findfirst", "n=1000", "reduce", "basesize=128"]` | 401.127 ms (5%) |         | 223.98 KiB (1%) |        3162 |
| `["findfirst", "n=1000", "reduce", "basesize=256"]` | 540.227 ms (5%) |         | 168.97 KiB (1%) |        2377 |
| `["findfirst", "n=1000", "reduce", "basesize=512"]` | 663.189 ms (5%) |         | 108.55 KiB (1%) |        1509 |
| `["findfirst", "n=400", "foldl"]`                   | 554.330 ms (5%) |         |                 |             |
| `["findfirst", "n=400", "reduce", "basesize=128"]`  | 287.279 ms (5%) |         | 380.73 KiB (1%) |        5424 |
| `["findfirst", "n=400", "reduce", "basesize=256"]`  | 299.550 ms (5%) |         | 207.72 KiB (1%) |        2960 |
| `["findfirst", "n=400", "reduce", "basesize=512"]`  | 397.439 ms (5%) |         | 137.86 KiB (1%) |        1973 |
| `["findfirst", "n=500", "foldl"]`                   |  96.049 ms (5%) |         |                 |             |
| `["findfirst", "n=500", "reduce", "basesize=128"]`  | 134.490 ms (5%) |         | 175.73 KiB (1%) |        2416 |
| `["findfirst", "n=500", "reduce", "basesize=256"]`  | 209.939 ms (5%) |         | 155.33 KiB (1%) |        2120 |
| `["findfirst", "n=500", "reduce", "basesize=512"]`  | 124.409 ms (5%) |         |  55.11 KiB (1%) |         749 |
| `["overhead", "default"]`                           |  71.400 μs (5%) |         |  32.73 KiB (1%) |         418 |
| `["overhead", "stoppable=false"]`                   |  72.300 μs (5%) |         |  32.75 KiB (1%) |         418 |
| `["overhead", "stoppable=true"]`                    |  80.401 μs (5%) |         |  44.25 KiB (1%) |         610 |
| `["parallel_histogram", "assoc", "basesize=16384"]` |   3.732 ms (5%) |         | 728.91 KiB (1%) |          57 |
| `["parallel_histogram", "assoc", "basesize=4096"]`  |   4.482 ms (5%) |         |   1.79 MiB (1%) |         216 |
| `["parallel_histogram", "assoc", "basesize=8192"]`  |   4.118 ms (5%) |         |   1.42 MiB (1%) |         117 |
| `["parallel_histogram", "comm", "basesize=16384"]`  |  16.795 ms (5%) |         |   1.68 MiB (1%) |        5782 |
| `["parallel_histogram", "comm", "basesize=4096"]`   |  24.755 ms (5%) |         |   1.21 MiB (1%) |        5701 |
| `["parallel_histogram", "comm", "basesize=8192"]`   |  22.027 ms (5%) |         |   1.37 MiB (1%) |        9687 |
| `["parallel_histogram", "seq"]`                     |   6.683 ms (5%) |         | 364.16 KiB (1%) |          24 |
| `["partition_length_maximum", "rand", "foldl"]`     |  41.187 ms (5%) |         |                 |             |
| `["partition_length_maximum", "rand", "reduce"]`    |  20.605 ms (5%) |         |  736 bytes (1%) |          11 |
| `["splitby", "count", "foldl"]`                     |   2.266 ms (5%) |         |                 |             |
| `["splitby", "count", "man"]`                       |   1.528 ms (5%) |         |                 |             |
| `["splitby", "count", "reduce"]`                    |   1.089 ms (5%) |         |   1.09 KiB (1%) |          19 |
| `["sum", "random", "foldl"]`                        |  17.980 ms (5%) |         |                 |             |
| `["sum", "random", "reduce", "basesize=128"]`       |   9.137 ms (5%) |         |  74.11 KiB (1%) |        1102 |
| `["sum", "random", "reduce", "basesize=256"]`       |   9.098 ms (5%) |         |  36.73 KiB (1%) |         546 |
| `["sum", "random", "reduce", "basesize=512"]`       |   9.038 ms (5%) |         |  18.11 KiB (1%) |         270 |
| `["sum", "uniform", "foldl"]`                       |  17.730 ms (5%) |         |                 |             |
| `["sum", "uniform", "reduce", "basesize=128"]`      |   9.038 ms (5%) |         |  74.17 KiB (1%) |        1104 |
| `["sum", "uniform", "reduce", "basesize=256"]`      |   8.968 ms (5%) |         |  36.67 KiB (1%) |         544 |
| `["sum", "uniform", "reduce", "basesize=512"]`      |   8.914 ms (5%) |         |  18.03 KiB (1%) |         268 |
| `["sum", "valley", "foldl"]`                        |  18.145 ms (5%) |         |                 |             |
| `["sum", "valley", "reduce", "basesize=128"]`       |   9.275 ms (5%) |         |  74.14 KiB (1%) |        1103 |
| `["sum", "valley", "reduce", "basesize=256"]`       |   9.197 ms (5%) |         |  36.70 KiB (1%) |         545 |
| `["sum", "valley", "reduce", "basesize=512"]`       |   9.173 ms (5%) |         |  18.03 KiB (1%) |         268 |
| `["words", "nthreads=1"]`                           |  18.448 ms (5%) |         |  31.72 MiB (1%) |     1033452 |
| `["words", "nthreads=2"]`                           |  12.108 ms (5%) |         |  32.08 MiB (1%) |     1033488 |
| `["words", "nthreads=4"]`                           |  13.003 ms (5%) |         |  32.97 MiB (1%) |     1033675 |

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
       #1  2793 MHz       6993 s          1 s        242 s       3640 s          0 s
       #2  2793 MHz       7952 s          1 s        268 s       2668 s          0 s
       
  Memory: 6.780967712402344 GB (3357.90234375 MB free)
  Uptime: 1093.82 sec
  Load Avg:  1.61  1.59  1.11
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
    CPU MHz:                         2793.436
    BogoMIPS:                        5586.87
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

