# Multi-thread benchmark result

* Pull request commit: [`208392d21bd54efb758ab28dfaa38c786cdd49e5`](https://github.com/JuliaFolds/Transducers.jl/commit/208392d21bd54efb758ab28dfaa38c786cdd49e5)
* Pull request: <https://github.com/JuliaFolds/Transducers.jl/pull/508> (Tweak README)

# Judge result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmarks:
    - Target: 30 Jan 2022 - 00:55
    - Baseline: 30 Jan 2022 - 01:00
* Package commits:
    - Target: ede17f
    - Baseline: 3f52fa
* Julia commits:
    - Target: ac5cc9
    - Baseline: ac5cc9
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
| `["findfirst", "n=1000", "reduce", "basesize=128"]` | 0.76 (5%) :white_check_mark: | 0.75 (1%) :white_check_mark: |
| `["findfirst", "n=1000", "reduce", "basesize=256"]` |                1.39 (5%) :x: |                1.36 (1%) :x: |
| `["findfirst", "n=1000", "reduce", "basesize=512"]` |                1.07 (5%) :x: | 0.96 (1%) :white_check_mark: |
| `["findfirst", "n=400", "reduce", "basesize=128"]`  |                   0.99 (5%)  |                1.04 (1%) :x: |
| `["findfirst", "n=400", "reduce", "basesize=512"]`  | 0.86 (5%) :white_check_mark: | 0.84 (1%) :white_check_mark: |
| `["findfirst", "n=500", "reduce", "basesize=128"]`  |                   0.97 (5%)  | 0.88 (1%) :white_check_mark: |
| `["findfirst", "n=500", "reduce", "basesize=256"]`  |                1.18 (5%) :x: |                1.24 (1%) :x: |
| `["findfirst", "n=500", "reduce", "basesize=512"]`  |                1.07 (5%) :x: |                1.12 (1%) :x: |
| `["parallel_histogram", "comm", "basesize=4096"]`   | 0.88 (5%) :white_check_mark: | 0.89 (1%) :white_check_mark: |
| `["parallel_histogram", "comm", "basesize=8192"]`   |                   0.98 (5%)  | 0.99 (1%) :white_check_mark: |
| `["splitby", "count", "foldl"]`                     |                1.06 (5%) :x: |                   1.00 (1%)  |
| `["splitby", "count", "reduce"]`                    |                   0.98 (5%)  | 0.99 (1%) :white_check_mark: |
| `["words", "nthreads=2"]`                           |                1.13 (5%) :x: |                1.01 (1%) :x: |
| `["words", "nthreads=4"]`                           |                1.06 (5%) :x: |                   1.01 (1%)  |

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
Julia Version 1.7.1
Commit ac5cc99908 (2021-12-22 19:35 UTC)
Platform Info:
  OS: Linux (x86_64-pc-linux-gnu)
      Ubuntu 20.04.3 LTS
  uname: Linux 5.11.0-1027-azure #30~20.04.1-Ubuntu SMP Wed Jan 12 20:56:50 UTC 2022 x86_64 x86_64
  CPU: Intel(R) Xeon(R) Platinum 8370C CPU @ 2.80GHz: 
              speed         user         nice          sys         idle          irq
       #1  2793 MHz       5184 s          1 s        220 s       2663 s          0 s
       #2  2793 MHz       5184 s          1 s        224 s       2692 s          0 s
       
  Memory: 6.788978576660156 GB (3339.7890625 MB free)
  Uptime: 813.56 sec
  Load Avg:  1.69  1.49  0.89
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-12.0.1 (ORCJIT, icelake-server)
```

### Baseline
```
Julia Version 1.7.1
Commit ac5cc99908 (2021-12-22 19:35 UTC)
Platform Info:
  OS: Linux (x86_64-pc-linux-gnu)
      Ubuntu 20.04.3 LTS
  uname: Linux 5.11.0-1027-azure #30~20.04.1-Ubuntu SMP Wed Jan 12 20:56:50 UTC 2022 x86_64 x86_64
  CPU: Intel(R) Xeon(R) Platinum 8370C CPU @ 2.80GHz: 
              speed         user         nice          sys         idle          irq
       #1  2793 MHz       7625 s          1 s        258 s       3156 s          0 s
       #2  2793 MHz       7368 s          1 s        257 s       3447 s          0 s
       
  Memory: 6.788978576660156 GB (3389.4921875 MB free)
  Uptime: 1111.02 sec
  Load Avg:  1.63  1.54  1.08
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-12.0.1 (ORCJIT, icelake-server)
```

---
# Target result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmark: 30 Jan 2022 - 0:55
* Package commit: ede17f
* Julia commit: ac5cc9
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
| `["collect", "assoc", "basesize=1"]`                | 280.407 ms (5%) |         |  25.97 MiB (1%) |      306808 |
| `["collect", "assoc", "basesize=1024"]`             | 238.849 ms (5%) |         |   2.61 MiB (1%) |         454 |
| `["collect", "assoc", "basesize=32"]`               | 240.929 ms (5%) |         |   4.82 MiB (1%) |       11696 |
| `["collect", "seq"]`                                | 476.772 ms (5%) |         | 812.73 KiB (1%) |          11 |
| `["collect", "unordered", "basesize=1"]`            | 373.443 ms (5%) |         |  23.89 MiB (1%) |      412651 |
| `["collect", "unordered", "basesize=1024"]`         | 250.853 ms (5%) |         |   1.01 MiB (1%) |        1087 |
| `["collect", "unordered", "basesize=32"]`           | 261.762 ms (5%) |         |   1.59 MiB (1%) |       14964 |
| `["findfirst", "n=1000", "foldl"]`                  | 738.505 ms (5%) |         |                 |             |
| `["findfirst", "n=1000", "reduce", "basesize=128"]` | 404.721 ms (5%) |         | 232.92 KiB (1%) |        3278 |
| `["findfirst", "n=1000", "reduce", "basesize=256"]` | 725.649 ms (5%) |         | 212.70 KiB (1%) |        2995 |
| `["findfirst", "n=1000", "reduce", "basesize=512"]` | 664.364 ms (5%) |         | 103.56 KiB (1%) |        1455 |
| `["findfirst", "n=400", "foldl"]`                   | 554.100 ms (5%) |         |                 |             |
| `["findfirst", "n=400", "reduce", "basesize=128"]`  | 295.970 ms (5%) |         | 397.50 KiB (1%) |        5644 |
| `["findfirst", "n=400", "reduce", "basesize=256"]`  | 287.519 ms (5%) |         | 199.50 KiB (1%) |        2859 |
| `["findfirst", "n=400", "reduce", "basesize=512"]`  | 324.275 ms (5%) |         | 115.70 KiB (1%) |        1663 |
| `["findfirst", "n=500", "foldl"]`                   |  95.985 ms (5%) |         |                 |             |
| `["findfirst", "n=500", "reduce", "basesize=128"]`  | 198.435 ms (5%) |         | 225.36 KiB (1%) |        3131 |
| `["findfirst", "n=500", "reduce", "basesize=256"]`  | 107.020 ms (5%) |         |  91.58 KiB (1%) |        1227 |
| `["findfirst", "n=500", "reduce", "basesize=512"]`  | 103.644 ms (5%) |         |  56.83 KiB (1%) |         757 |
| `["overhead", "default"]`                           |  73.800 μs (5%) |         |  32.70 KiB (1%) |         417 |
| `["overhead", "stoppable=false"]`                   |  74.100 μs (5%) |         |  32.75 KiB (1%) |         418 |
| `["overhead", "stoppable=true"]`                    |  82.500 μs (5%) |         |  44.25 KiB (1%) |         610 |
| `["parallel_histogram", "assoc", "basesize=16384"]` |   3.776 ms (5%) |         | 728.91 KiB (1%) |          57 |
| `["parallel_histogram", "assoc", "basesize=4096"]`  |   4.525 ms (5%) |         |   1.79 MiB (1%) |         216 |
| `["parallel_histogram", "assoc", "basesize=8192"]`  |   4.155 ms (5%) |         |   1.42 MiB (1%) |         117 |
| `["parallel_histogram", "comm", "basesize=16384"]`  |  15.419 ms (5%) |         |   1.66 MiB (1%) |        4976 |
| `["parallel_histogram", "comm", "basesize=4096"]`   |  22.973 ms (5%) |         |   1.29 MiB (1%) |        8595 |
| `["parallel_histogram", "comm", "basesize=8192"]`   |  22.333 ms (5%) |         |   1.39 MiB (1%) |       10732 |
| `["parallel_histogram", "seq"]`                     |   6.633 ms (5%) |         | 364.16 KiB (1%) |          24 |
| `["partition_length_maximum", "rand", "foldl"]`     |  41.135 ms (5%) |         |                 |             |
| `["partition_length_maximum", "rand", "reduce"]`    |  20.604 ms (5%) |         |  736 bytes (1%) |          11 |
| `["splitby", "count", "foldl"]`                     |   2.390 ms (5%) |         |                 |             |
| `["splitby", "count", "man"]`                       |   1.528 ms (5%) |         |                 |             |
| `["splitby", "count", "reduce"]`                    |   1.081 ms (5%) |         |   1.05 KiB (1%) |          19 |
| `["sum", "random", "foldl"]`                        |  18.090 ms (5%) |         |                 |             |
| `["sum", "random", "reduce", "basesize=128"]`       |   9.262 ms (5%) |         |  73.95 KiB (1%) |        1097 |
| `["sum", "random", "reduce", "basesize=256"]`       |   9.172 ms (5%) |         |  36.73 KiB (1%) |         546 |
| `["sum", "random", "reduce", "basesize=512"]`       |   9.131 ms (5%) |         |  18.14 KiB (1%) |         271 |
| `["sum", "uniform", "foldl"]`                       |  17.734 ms (5%) |         |                 |             |
| `["sum", "uniform", "reduce", "basesize=128"]`      |   9.072 ms (5%) |         |  74.20 KiB (1%) |        1105 |
| `["sum", "uniform", "reduce", "basesize=256"]`      |   8.972 ms (5%) |         |  36.67 KiB (1%) |         544 |
| `["sum", "uniform", "reduce", "basesize=512"]`      |   8.911 ms (5%) |         |  18.03 KiB (1%) |         268 |
| `["sum", "valley", "foldl"]`                        |  18.147 ms (5%) |         |                 |             |
| `["sum", "valley", "reduce", "basesize=128"]`       |   9.285 ms (5%) |         |  74.14 KiB (1%) |        1103 |
| `["sum", "valley", "reduce", "basesize=256"]`       |   9.185 ms (5%) |         |  36.77 KiB (1%) |         547 |
| `["sum", "valley", "reduce", "basesize=512"]`       |   9.193 ms (5%) |         |  18.03 KiB (1%) |         268 |
| `["words", "nthreads=1"]`                           |  18.837 ms (5%) |         |  31.63 MiB (1%) |     1030141 |
| `["words", "nthreads=2"]`                           |  13.195 ms (5%) |         |  32.34 MiB (1%) |     1030224 |
| `["words", "nthreads=4"]`                           |  13.324 ms (5%) |         |  32.79 MiB (1%) |     1030291 |

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
Julia Version 1.7.1
Commit ac5cc99908 (2021-12-22 19:35 UTC)
Platform Info:
  OS: Linux (x86_64-pc-linux-gnu)
      Ubuntu 20.04.3 LTS
  uname: Linux 5.11.0-1027-azure #30~20.04.1-Ubuntu SMP Wed Jan 12 20:56:50 UTC 2022 x86_64 x86_64
  CPU: Intel(R) Xeon(R) Platinum 8370C CPU @ 2.80GHz: 
              speed         user         nice          sys         idle          irq
       #1  2793 MHz       5184 s          1 s        220 s       2663 s          0 s
       #2  2793 MHz       5184 s          1 s        224 s       2692 s          0 s
       
  Memory: 6.788978576660156 GB (3339.7890625 MB free)
  Uptime: 813.56 sec
  Load Avg:  1.69  1.49  0.89
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-12.0.1 (ORCJIT, icelake-server)
```

---
# Baseline result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmark: 30 Jan 2022 - 1:0
* Package commit: 3f52fa
* Julia commit: ac5cc9
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
| `["collect", "assoc", "basesize=1"]`                | 280.578 ms (5%) |         |  25.97 MiB (1%) |      306828 |
| `["collect", "assoc", "basesize=1024"]`             | 239.108 ms (5%) |         |   2.61 MiB (1%) |         455 |
| `["collect", "assoc", "basesize=32"]`               | 240.748 ms (5%) |         |   4.82 MiB (1%) |       11717 |
| `["collect", "seq"]`                                | 476.710 ms (5%) |         | 812.73 KiB (1%) |          11 |
| `["collect", "unordered", "basesize=1"]`            | 373.447 ms (5%) |         |  23.92 MiB (1%) |      413491 |
| `["collect", "unordered", "basesize=1024"]`         | 250.704 ms (5%) |         |   1.01 MiB (1%) |        1127 |
| `["collect", "unordered", "basesize=32"]`           | 261.594 ms (5%) |         |   1.59 MiB (1%) |       14882 |
| `["findfirst", "n=1000", "foldl"]`                  | 737.655 ms (5%) |         |                 |             |
| `["findfirst", "n=1000", "reduce", "basesize=128"]` | 531.398 ms (5%) |         | 310.31 KiB (1%) |        4328 |
| `["findfirst", "n=1000", "reduce", "basesize=256"]` | 523.317 ms (5%) |         | 156.36 KiB (1%) |        2206 |
| `["findfirst", "n=1000", "reduce", "basesize=512"]` | 621.232 ms (5%) |         | 107.73 KiB (1%) |        1493 |
| `["findfirst", "n=400", "foldl"]`                   | 553.140 ms (5%) |         |                 |             |
| `["findfirst", "n=400", "reduce", "basesize=128"]`  | 297.974 ms (5%) |         | 383.33 KiB (1%) |        5457 |
| `["findfirst", "n=400", "reduce", "basesize=256"]`  | 291.888 ms (5%) |         | 201.11 KiB (1%) |        2881 |
| `["findfirst", "n=400", "reduce", "basesize=512"]`  | 377.178 ms (5%) |         | 138.44 KiB (1%) |        1972 |
| `["findfirst", "n=500", "foldl"]`                   |  95.955 ms (5%) |         |                 |             |
| `["findfirst", "n=500", "reduce", "basesize=128"]`  | 204.098 ms (5%) |         | 254.75 KiB (1%) |        3506 |
| `["findfirst", "n=500", "reduce", "basesize=256"]`  |  90.919 ms (5%) |         |  74.05 KiB (1%) |        1014 |
| `["findfirst", "n=500", "reduce", "basesize=512"]`  |  96.663 ms (5%) |         |  50.72 KiB (1%) |         677 |
| `["overhead", "default"]`                           |  73.600 μs (5%) |         |  32.67 KiB (1%) |         416 |
| `["overhead", "stoppable=false"]`                   |  72.800 μs (5%) |         |  32.75 KiB (1%) |         418 |
| `["overhead", "stoppable=true"]`                    |  81.200 μs (5%) |         |  44.25 KiB (1%) |         610 |
| `["parallel_histogram", "assoc", "basesize=16384"]` |   3.742 ms (5%) |         | 728.91 KiB (1%) |          57 |
| `["parallel_histogram", "assoc", "basesize=4096"]`  |   4.494 ms (5%) |         |   1.79 MiB (1%) |         215 |
| `["parallel_histogram", "assoc", "basesize=8192"]`  |   4.119 ms (5%) |         |   1.42 MiB (1%) |         117 |
| `["parallel_histogram", "comm", "basesize=16384"]`  |  15.763 ms (5%) |         |   1.66 MiB (1%) |        4993 |
| `["parallel_histogram", "comm", "basesize=4096"]`   |  26.078 ms (5%) |         |   1.45 MiB (1%) |       13774 |
| `["parallel_histogram", "comm", "basesize=8192"]`   |  22.867 ms (5%) |         |   1.41 MiB (1%) |       11562 |
| `["parallel_histogram", "seq"]`                     |   6.688 ms (5%) |         | 364.16 KiB (1%) |          24 |
| `["partition_length_maximum", "rand", "foldl"]`     |  41.207 ms (5%) |         |                 |             |
| `["partition_length_maximum", "rand", "reduce"]`    |  20.572 ms (5%) |         |  736 bytes (1%) |          11 |
| `["splitby", "count", "foldl"]`                     |   2.258 ms (5%) |         |                 |             |
| `["splitby", "count", "man"]`                       |   1.527 ms (5%) |         |                 |             |
| `["splitby", "count", "reduce"]`                    |   1.104 ms (5%) |         |   1.06 KiB (1%) |          18 |
| `["sum", "random", "foldl"]`                        |  17.894 ms (5%) |         |                 |             |
| `["sum", "random", "reduce", "basesize=128"]`       |   9.158 ms (5%) |         |  74.02 KiB (1%) |        1099 |
| `["sum", "random", "reduce", "basesize=256"]`       |   9.059 ms (5%) |         |  36.77 KiB (1%) |         547 |
| `["sum", "random", "reduce", "basesize=512"]`       |   9.018 ms (5%) |         |  18.05 KiB (1%) |         268 |
| `["sum", "uniform", "foldl"]`                       |  17.729 ms (5%) |         |                 |             |
| `["sum", "uniform", "reduce", "basesize=128"]`      |   9.084 ms (5%) |         |  74.17 KiB (1%) |        1104 |
| `["sum", "uniform", "reduce", "basesize=256"]`      |   8.971 ms (5%) |         |  36.70 KiB (1%) |         545 |
| `["sum", "uniform", "reduce", "basesize=512"]`      |   8.918 ms (5%) |         |  18.03 KiB (1%) |         268 |
| `["sum", "valley", "foldl"]`                        |  18.145 ms (5%) |         |                 |             |
| `["sum", "valley", "reduce", "basesize=128"]`       |   9.299 ms (5%) |         |  74.05 KiB (1%) |        1100 |
| `["sum", "valley", "reduce", "basesize=256"]`       |   9.202 ms (5%) |         |  36.70 KiB (1%) |         545 |
| `["sum", "valley", "reduce", "basesize=512"]`       |   9.146 ms (5%) |         |  18.00 KiB (1%) |         267 |
| `["words", "nthreads=1"]`                           |  18.904 ms (5%) |         |  31.55 MiB (1%) |     1028172 |
| `["words", "nthreads=2"]`                           |  11.717 ms (5%) |         |  31.91 MiB (1%) |     1028223 |
| `["words", "nthreads=4"]`                           |  12.562 ms (5%) |         |  32.62 MiB (1%) |     1028295 |

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
Julia Version 1.7.1
Commit ac5cc99908 (2021-12-22 19:35 UTC)
Platform Info:
  OS: Linux (x86_64-pc-linux-gnu)
      Ubuntu 20.04.3 LTS
  uname: Linux 5.11.0-1027-azure #30~20.04.1-Ubuntu SMP Wed Jan 12 20:56:50 UTC 2022 x86_64 x86_64
  CPU: Intel(R) Xeon(R) Platinum 8370C CPU @ 2.80GHz: 
              speed         user         nice          sys         idle          irq
       #1  2793 MHz       7625 s          1 s        258 s       3156 s          0 s
       #2  2793 MHz       7368 s          1 s        257 s       3447 s          0 s
       
  Memory: 6.788978576660156 GB (3389.4921875 MB free)
  Uptime: 1111.02 sec
  Load Avg:  1.63  1.54  1.08
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
    CPU MHz:                         2793.438
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
    Vulnerability Spec store bypass: Vulnerable
    Vulnerability Spectre v1:        Mitigation; usercopy/swapgs barriers and __user pointer sanitization
    Vulnerability Spectre v2:        Mitigation; Full generic retpoline, STIBP disabled, RSB filling
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

