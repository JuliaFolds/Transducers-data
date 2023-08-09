# Multi-thread benchmark result

* Pull request commit: [`739005de060b782ec16b65424a6ce47f1d38d33e`](https://github.com/JuliaFolds/Transducers.jl/commit/739005de060b782ec16b65424a6ce47f1d38d33e)
* Pull request: <https://github.com/JuliaFolds/Transducers.jl/pull/243> (Update */Manifest.toml)

# Judge result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmarks:
    - Target: 9 Aug 2023 - 01:35
    - Baseline: 9 Aug 2023 - 01:40
* Package commits:
    - Target: 681985
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
| `["findfirst", "n=400", "reduce", "basesize=128"]`  |                   1.04 (5%)  |                1.07 (1%) :x: |
| `["findfirst", "n=400", "reduce", "basesize=512"]`  | 0.72 (5%) :white_check_mark: | 0.76 (1%) :white_check_mark: |
| `["findfirst", "n=500", "reduce", "basesize=128"]`  | 0.92 (5%) :white_check_mark: | 0.90 (1%) :white_check_mark: |
| `["findfirst", "n=500", "reduce", "basesize=256"]`  |                2.19 (5%) :x: |                1.79 (1%) :x: |
| `["findfirst", "n=500", "reduce", "basesize=512"]`  | 0.91 (5%) :white_check_mark: | 0.89 (1%) :white_check_mark: |
| `["parallel_histogram", "assoc", "basesize=4096"]`  |                   0.99 (5%)  | 0.87 (1%) :white_check_mark: |
| `["parallel_histogram", "comm", "basesize=16384"]`  |                1.13 (5%) :x: |                1.01 (1%) :x: |
| `["parallel_histogram", "comm", "basesize=4096"]`   |                1.12 (5%) :x: |                   1.00 (1%)  |
| `["parallel_histogram", "comm", "basesize=8192"]`   |                1.16 (5%) :x: | 0.95 (1%) :white_check_mark: |
| `["partition_length_maximum", "rand", "reduce"]`    |                   1.00 (5%)  |                1.05 (1%) :x: |
| `["splitby", "count", "reduce"]`                    |                   1.01 (5%)  |                1.03 (1%) :x: |

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
      Ubuntu 22.04.2 LTS
  uname: Linux 5.15.0-1042-azure #49-Ubuntu SMP Tue Jul 11 17:28:46 UTC 2023 x86_64 x86_64
  CPU: Intel(R) Xeon(R) Platinum 8272CL CPU @ 2.60GHz: 
              speed         user         nice          sys         idle          irq
       #1  2593 MHz       5084 s          0 s        265 s       2567 s          0 s
       #2  2593 MHz       5433 s          0 s        256 s       2212 s          0 s
       
  Memory: 6.7694854736328125 GB (3575.5390625 MB free)
  Uptime: 796.53 sec
  Load Avg:  1.68  1.55  0.95
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-12.0.1 (ORCJIT, skylake-avx512)
```

### Baseline
```
Julia Version 1.7.3
Commit 742b9abb4d (2022-05-06 12:58 UTC)
Platform Info:
  OS: Linux (x86_64-pc-linux-gnu)
      Ubuntu 22.04.2 LTS
  uname: Linux 5.15.0-1042-azure #49-Ubuntu SMP Tue Jul 11 17:28:46 UTC 2023 x86_64 x86_64
  CPU: Intel(R) Xeon(R) Platinum 8272CL CPU @ 2.60GHz: 
              speed         user         nice          sys         idle          irq
       #1  2593 MHz       7176 s          0 s        339 s       3487 s          0 s
       #2  2593 MHz       8081 s          0 s        326 s       2583 s          0 s
       
  Memory: 6.7694854736328125 GB (3544.328125 MB free)
  Uptime: 1105.86 sec
  Load Avg:  1.54  1.58  1.14
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-12.0.1 (ORCJIT, skylake-avx512)
```

---
# Target result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmark: 9 Aug 2023 - 1:35
* Package commit: 681985
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
| `["collect", "assoc", "basesize=1"]`                | 199.752 ms (5%) |         |   4.36 MiB (1%) |       32800 |
| `["collect", "assoc", "basesize=1024"]`             | 198.384 ms (5%) |         |   1.09 MiB (1%) |          53 |
| `["collect", "assoc", "basesize=32"]`               | 198.533 ms (5%) |         |   1.48 MiB (1%) |        1052 |
| `["collect", "seq"]`                                | 394.538 ms (5%) |         | 256.05 KiB (1%) |           2 |
| `["collect", "unordered", "basesize=1"]`            | 341.828 ms (5%) |         |  23.90 MiB (1%) |      413116 |
| `["collect", "unordered", "basesize=1024"]`         | 211.962 ms (5%) |         |   1.00 MiB (1%) |         851 |
| `["collect", "unordered", "basesize=32"]`           | 223.486 ms (5%) |         |   1.58 MiB (1%) |       14652 |
| `["findfirst", "n=1000", "foldl"]`                  | 627.778 ms (5%) |         |                 |             |
| `["findfirst", "n=1000", "reduce", "basesize=128"]` | 343.510 ms (5%) |         | 232.83 KiB (1%) |        3275 |
| `["findfirst", "n=1000", "reduce", "basesize=256"]` | 421.310 ms (5%) |         | 157.20 KiB (1%) |        2193 |
| `["findfirst", "n=1000", "reduce", "basesize=512"]` | 564.877 ms (5%) |         | 108.64 KiB (1%) |        1512 |
| `["findfirst", "n=400", "foldl"]`                   | 471.332 ms (5%) |         |                 |             |
| `["findfirst", "n=400", "reduce", "basesize=128"]`  | 263.291 ms (5%) |         | 413.84 KiB (1%) |        5871 |
| `["findfirst", "n=400", "reduce", "basesize=256"]`  | 247.543 ms (5%) |         | 200.98 KiB (1%) |        2877 |
| `["findfirst", "n=400", "reduce", "basesize=512"]`  | 272.613 ms (5%) |         | 112.69 KiB (1%) |        1625 |
| `["findfirst", "n=500", "foldl"]`                   |  81.663 ms (5%) |         |                 |             |
| `["findfirst", "n=500", "reduce", "basesize=128"]`  | 163.697 ms (5%) |         | 224.05 KiB (1%) |        3086 |
| `["findfirst", "n=500", "reduce", "basesize=256"]`  | 155.360 ms (5%) |         | 129.16 KiB (1%) |        1769 |
| `["findfirst", "n=500", "reduce", "basesize=512"]`  | 105.770 ms (5%) |         |  56.78 KiB (1%) |         776 |
| `["overhead", "default"]`                           |  74.301 μs (5%) |         |  32.70 KiB (1%) |         417 |
| `["overhead", "stoppable=false"]`                   |  73.501 μs (5%) |         |  32.75 KiB (1%) |         418 |
| `["overhead", "stoppable=true"]`                    |  84.701 μs (5%) |         |  44.22 KiB (1%) |         609 |
| `["parallel_histogram", "assoc", "basesize=16384"]` |   3.280 ms (5%) |         | 728.91 KiB (1%) |          57 |
| `["parallel_histogram", "assoc", "basesize=4096"]`  |   3.938 ms (5%) |         |   1.79 MiB (1%) |         216 |
| `["parallel_histogram", "assoc", "basesize=8192"]`  |   3.638 ms (5%) |         |   1.42 MiB (1%) |         117 |
| `["parallel_histogram", "comm", "basesize=16384"]`  |  15.313 ms (5%) |         |   1.53 MiB (1%) |         799 |
| `["parallel_histogram", "comm", "basesize=4096"]`   |  17.757 ms (5%) |         |   1.12 MiB (1%) |        2976 |
| `["parallel_histogram", "comm", "basesize=8192"]`   |  15.175 ms (5%) |         |   1.06 MiB (1%) |        1083 |
| `["parallel_histogram", "seq"]`                     |   5.811 ms (5%) |         | 364.16 KiB (1%) |          24 |
| `["partition_length_maximum", "rand", "foldl"]`     |  35.161 ms (5%) |         |                 |             |
| `["partition_length_maximum", "rand", "reduce"]`    |  17.570 ms (5%) |         |  736 bytes (1%) |          11 |
| `["splitby", "count", "foldl"]`                     |   2.569 ms (5%) |         |                 |             |
| `["splitby", "count", "man"]`                       |   1.752 ms (5%) |         |                 |             |
| `["splitby", "count", "reduce"]`                    |   1.140 ms (5%) |         |   1.06 KiB (1%) |          18 |
| `["sum", "random", "foldl"]`                        |  16.333 ms (5%) |         |                 |             |
| `["sum", "random", "reduce", "basesize=128"]`       |   8.247 ms (5%) |         |  74.17 KiB (1%) |        1104 |
| `["sum", "random", "reduce", "basesize=256"]`       |   8.150 ms (5%) |         |  36.67 KiB (1%) |         544 |
| `["sum", "random", "reduce", "basesize=512"]`       |   8.087 ms (5%) |         |  18.11 KiB (1%) |         270 |
| `["sum", "uniform", "foldl"]`                       |  15.696 ms (5%) |         |                 |             |
| `["sum", "uniform", "reduce", "basesize=128"]`      |   7.952 ms (5%) |         |  74.20 KiB (1%) |        1105 |
| `["sum", "uniform", "reduce", "basesize=256"]`      |   7.857 ms (5%) |         |  36.77 KiB (1%) |         547 |
| `["sum", "uniform", "reduce", "basesize=512"]`      |   7.790 ms (5%) |         |  18.03 KiB (1%) |         268 |
| `["sum", "valley", "foldl"]`                        |  16.137 ms (5%) |         |                 |             |
| `["sum", "valley", "reduce", "basesize=128"]`       |   8.272 ms (5%) |         |  74.11 KiB (1%) |        1102 |
| `["sum", "valley", "reduce", "basesize=256"]`       |   8.179 ms (5%) |         |  36.77 KiB (1%) |         547 |
| `["sum", "valley", "reduce", "basesize=512"]`       |   8.146 ms (5%) |         |  18.00 KiB (1%) |         267 |
| `["words", "nthreads=1"]`                           |  22.594 ms (5%) |         |  31.81 MiB (1%) |     1036416 |
| `["words", "nthreads=2"]`                           |  14.108 ms (5%) |         |  32.17 MiB (1%) |     1036452 |
| `["words", "nthreads=4"]`                           |  14.185 ms (5%) |         |  33.06 MiB (1%) |     1036620 |

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
      Ubuntu 22.04.2 LTS
  uname: Linux 5.15.0-1042-azure #49-Ubuntu SMP Tue Jul 11 17:28:46 UTC 2023 x86_64 x86_64
  CPU: Intel(R) Xeon(R) Platinum 8272CL CPU @ 2.60GHz: 
              speed         user         nice          sys         idle          irq
       #1  2593 MHz       5084 s          0 s        265 s       2567 s          0 s
       #2  2593 MHz       5433 s          0 s        256 s       2212 s          0 s
       
  Memory: 6.7694854736328125 GB (3575.5390625 MB free)
  Uptime: 796.53 sec
  Load Avg:  1.68  1.55  0.95
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-12.0.1 (ORCJIT, skylake-avx512)
```

---
# Baseline result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmark: 9 Aug 2023 - 1:40
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
| `["collect", "assoc", "basesize=1"]`                | 199.903 ms (5%) |         |   4.36 MiB (1%) |       32800 |
| `["collect", "assoc", "basesize=1024"]`             | 197.786 ms (5%) |         |   1.09 MiB (1%) |          53 |
| `["collect", "assoc", "basesize=32"]`               | 198.030 ms (5%) |         |   1.48 MiB (1%) |        1052 |
| `["collect", "seq"]`                                | 394.698 ms (5%) |         | 256.05 KiB (1%) |           2 |
| `["collect", "unordered", "basesize=1"]`            | 342.187 ms (5%) |         |  23.89 MiB (1%) |      412757 |
| `["collect", "unordered", "basesize=1024"]`         | 212.321 ms (5%) |         |   1.00 MiB (1%) |         852 |
| `["collect", "unordered", "basesize=32"]`           | 223.920 ms (5%) |         |   1.58 MiB (1%) |       14562 |
| `["findfirst", "n=1000", "foldl"]`                  | 625.395 ms (5%) |         |                 |             |
| `["findfirst", "n=1000", "reduce", "basesize=128"]` | 341.706 ms (5%) |         | 232.67 KiB (1%) |        3270 |
| `["findfirst", "n=1000", "reduce", "basesize=256"]` | 420.160 ms (5%) |         | 157.20 KiB (1%) |        2193 |
| `["findfirst", "n=1000", "reduce", "basesize=512"]` | 560.218 ms (5%) |         | 108.55 KiB (1%) |        1509 |
| `["findfirst", "n=400", "foldl"]`                   | 469.413 ms (5%) |         |                 |             |
| `["findfirst", "n=400", "reduce", "basesize=128"]`  | 253.310 ms (5%) |         | 387.73 KiB (1%) |        5514 |
| `["findfirst", "n=400", "reduce", "basesize=256"]`  | 246.567 ms (5%) |         | 200.77 KiB (1%) |        2870 |
| `["findfirst", "n=400", "reduce", "basesize=512"]`  | 376.822 ms (5%) |         | 148.83 KiB (1%) |        2149 |
| `["findfirst", "n=500", "foldl"]`                   |  81.370 ms (5%) |         |                 |             |
| `["findfirst", "n=500", "reduce", "basesize=128"]`  | 177.918 ms (5%) |         | 248.22 KiB (1%) |        3447 |
| `["findfirst", "n=500", "reduce", "basesize=256"]`  |  70.830 ms (5%) |         |  72.16 KiB (1%) |         979 |
| `["findfirst", "n=500", "reduce", "basesize=512"]`  | 116.111 ms (5%) |         |  63.62 KiB (1%) |         864 |
| `["overhead", "default"]`                           |  75.701 μs (5%) |         |  32.73 KiB (1%) |         418 |
| `["overhead", "stoppable=false"]`                   |  74.301 μs (5%) |         |  32.72 KiB (1%) |         417 |
| `["overhead", "stoppable=true"]`                    |  86.502 μs (5%) |         |  44.28 KiB (1%) |         611 |
| `["parallel_histogram", "assoc", "basesize=16384"]` |   3.241 ms (5%) |         | 728.91 KiB (1%) |          57 |
| `["parallel_histogram", "assoc", "basesize=4096"]`  |   3.970 ms (5%) |         |   2.05 MiB (1%) |         222 |
| `["parallel_histogram", "assoc", "basesize=8192"]`  |   3.584 ms (5%) |         |   1.42 MiB (1%) |         117 |
| `["parallel_histogram", "comm", "basesize=16384"]`  |  13.609 ms (5%) |         |   1.51 MiB (1%) |         144 |
| `["parallel_histogram", "comm", "basesize=4096"]`   |  15.819 ms (5%) |         |   1.12 MiB (1%) |        2811 |
| `["parallel_histogram", "comm", "basesize=8192"]`   |  13.031 ms (5%) |         |   1.12 MiB (1%) |         169 |
| `["parallel_histogram", "seq"]`                     |   5.740 ms (5%) |         | 364.16 KiB (1%) |          24 |
| `["partition_length_maximum", "rand", "foldl"]`     |  35.195 ms (5%) |         |                 |             |
| `["partition_length_maximum", "rand", "reduce"]`    |  17.587 ms (5%) |         |  704 bytes (1%) |          10 |
| `["splitby", "count", "foldl"]`                     |   2.620 ms (5%) |         |                 |             |
| `["splitby", "count", "man"]`                       |   1.755 ms (5%) |         |                 |             |
| `["splitby", "count", "reduce"]`                    |   1.126 ms (5%) |         |   1.03 KiB (1%) |          18 |
| `["sum", "random", "foldl"]`                        |  16.278 ms (5%) |         |                 |             |
| `["sum", "random", "reduce", "basesize=128"]`       |   8.216 ms (5%) |         |  74.08 KiB (1%) |        1101 |
| `["sum", "random", "reduce", "basesize=256"]`       |   8.121 ms (5%) |         |  36.77 KiB (1%) |         547 |
| `["sum", "random", "reduce", "basesize=512"]`       |   8.057 ms (5%) |         |  18.08 KiB (1%) |         269 |
| `["sum", "uniform", "foldl"]`                       |  15.722 ms (5%) |         |                 |             |
| `["sum", "uniform", "reduce", "basesize=128"]`      |   7.950 ms (5%) |         |  74.02 KiB (1%) |        1099 |
| `["sum", "uniform", "reduce", "basesize=256"]`      |   7.839 ms (5%) |         |  36.77 KiB (1%) |         547 |
| `["sum", "uniform", "reduce", "basesize=512"]`      |   7.800 ms (5%) |         |  18.00 KiB (1%) |         267 |
| `["sum", "valley", "foldl"]`                        |  16.062 ms (5%) |         |                 |             |
| `["sum", "valley", "reduce", "basesize=128"]`       |   8.189 ms (5%) |         |  74.08 KiB (1%) |        1101 |
| `["sum", "valley", "reduce", "basesize=256"]`       |   8.122 ms (5%) |         |  36.77 KiB (1%) |         547 |
| `["sum", "valley", "reduce", "basesize=512"]`       |   8.088 ms (5%) |         |  18.03 KiB (1%) |         268 |
| `["words", "nthreads=1"]`                           |  22.367 ms (5%) |         |  31.70 MiB (1%) |     1033344 |
| `["words", "nthreads=2"]`                           |  13.899 ms (5%) |         |  32.06 MiB (1%) |     1033382 |
| `["words", "nthreads=4"]`                           |  13.871 ms (5%) |         |  32.95 MiB (1%) |     1033546 |

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
      Ubuntu 22.04.2 LTS
  uname: Linux 5.15.0-1042-azure #49-Ubuntu SMP Tue Jul 11 17:28:46 UTC 2023 x86_64 x86_64
  CPU: Intel(R) Xeon(R) Platinum 8272CL CPU @ 2.60GHz: 
              speed         user         nice          sys         idle          irq
       #1  2593 MHz       7176 s          0 s        339 s       3487 s          0 s
       #2  2593 MHz       8081 s          0 s        326 s       2583 s          0 s
       
  Memory: 6.7694854736328125 GB (3544.328125 MB free)
  Uptime: 1105.86 sec
  Load Avg:  1.54  1.58  1.14
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-12.0.1 (ORCJIT, skylake-avx512)
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
    Model name:                      Intel(R) Xeon(R) Platinum 8272CL CPU @ 2.60GHz
    CPU family:                      6
    Model:                           85
    Thread(s) per core:              1
    Core(s) per socket:              2
    Socket(s):                       1
    Stepping:                        7
    BogoMIPS:                        5187.81
    Flags:                           fpu vme de pse tsc msr pae mce cx8 apic sep mtrr pge mca cmov pat pse36 clflush mmx fxsr sse sse2 ss ht syscall nx pdpe1gb rdtscp lm constant_tsc rep_good nopl xtopology cpuid pni pclmulqdq ssse3 fma cx16 pcid sse4_1 sse4_2 movbe popcnt aes xsave avx f16c rdrand hypervisor lahf_lm abm 3dnowprefetch invpcid_single pti fsgsbase bmi1 hle avx2 smep bmi2 erms invpcid rtm avx512f avx512dq rdseed adx smap clflushopt avx512cd avx512bw avx512vl xsaveopt xsavec xsaves md_clear
    Hypervisor vendor:               Microsoft
    Virtualization type:             full
    L1d cache:                       64 KiB (2 instances)
    L1i cache:                       64 KiB (2 instances)
    L2 cache:                        2 MiB (2 instances)
    L3 cache:                        35.8 MiB (1 instance)
    NUMA node(s):                    1
    NUMA node0 CPU(s):               0,1
    Vulnerability Itlb multihit:     KVM: Mitigation: VMX unsupported
    Vulnerability L1tf:              Mitigation; PTE Inversion
    Vulnerability Mds:               Mitigation; Clear CPU buffers; SMT Host state unknown
    Vulnerability Meltdown:          Mitigation; PTI
    Vulnerability Mmio stale data:   Vulnerable: Clear CPU buffers attempted, no microcode; SMT Host state unknown
    Vulnerability Retbleed:          Vulnerable
    Vulnerability Spec store bypass: Vulnerable
    Vulnerability Spectre v1:        Mitigation; usercopy/swapgs barriers and __user pointer sanitization
    Vulnerability Spectre v2:        Mitigation; Retpolines, STIBP disabled, RSB filling, PBRSB-eIBRS Not affected
    Vulnerability Srbds:             Not affected
    Vulnerability Tsx async abort:   Mitigation; Clear CPU buffers; SMT Host state unknown
    

| Cpu Property       | Value                                                   |
|:------------------ |:------------------------------------------------------- |
| Brand              | Intel(R) Xeon(R) Platinum 8272CL CPU @ 2.60GHz          |
| Vendor             | :Intel                                                  |
| Architecture       | :Skylake                                                |
| Model              | Family: 0x06, Model: 0x55, Stepping: 0x07, Type: 0x00   |
| Cores              | 2 physical cores, 2 logical cores (on executing CPU)    |
|                    | No Hyperthreading hardware capability detected          |
| Clock Frequencies  | Not supported by CPU                                    |
| Data Cache         | Level 1:3 : (32, 1024, 36608) kbytes                    |
|                    | 64 byte cache line size                                 |
| Address Size       | 48 bits virtual, 46 bits physical                       |
| SIMD               | 512 bit = 64 byte max. SIMD vector size                 |
| Time Stamp Counter | TSC is accessible via `rdtsc`                           |
|                    | TSC increased at every clock cycle (non-invariant TSC)  |
| Perf. Monitoring   | Performance Monitoring Counters (PMC) are not supported |
| Hypervisor         | Yes, Microsoft                                          |

