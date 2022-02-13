# Multi-thread benchmark result

* Pull request commit: [`dfb62b18b9183b3266b850ffb77e28027f6de135`](https://github.com/JuliaFolds/Transducers.jl/commit/dfb62b18b9183b3266b850ffb77e28027f6de135)
* Pull request: <https://github.com/JuliaFolds/Transducers.jl/pull/243> (Update */Manifest.toml)

# Judge result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmarks:
    - Target: 13 Feb 2022 - 01:27
    - Baseline: 13 Feb 2022 - 01:32
* Package commits:
    - Target: 79eb3f
    - Baseline: 39038b
* Julia commits:
    - Target: bf5349
    - Baseline: bf5349
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
| `["findfirst", "n=1000", "foldl"]`                  |                1.05 (5%) :x: |                   1.00 (1%)  |
| `["findfirst", "n=1000", "reduce", "basesize=128"]` | 0.54 (5%) :white_check_mark: | 0.55 (1%) :white_check_mark: |
| `["findfirst", "n=1000", "reduce", "basesize=512"]` | 0.66 (5%) :white_check_mark: | 0.70 (1%) :white_check_mark: |
| `["findfirst", "n=400", "reduce", "basesize=128"]`  | 0.80 (5%) :white_check_mark: | 0.80 (1%) :white_check_mark: |
| `["findfirst", "n=400", "reduce", "basesize=512"]`  | 0.91 (5%) :white_check_mark: | 0.96 (1%) :white_check_mark: |
| `["findfirst", "n=500", "foldl"]`                   |                1.08 (5%) :x: |                   1.00 (1%)  |
| `["findfirst", "n=500", "reduce", "basesize=128"]`  |                1.06 (5%) :x: |                1.13 (1%) :x: |
| `["findfirst", "n=500", "reduce", "basesize=256"]`  | 0.34 (5%) :white_check_mark: | 0.48 (1%) :white_check_mark: |
| `["findfirst", "n=500", "reduce", "basesize=512"]`  |                1.10 (5%) :x: |                1.14 (1%) :x: |
| `["overhead", "default"]`                           | 0.92 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["overhead", "stoppable=false"]`                   | 0.91 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["overhead", "stoppable=true"]`                    | 0.90 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["parallel_histogram", "assoc", "basesize=4096"]`  |                   0.96 (5%)  | 0.87 (1%) :white_check_mark: |
| `["parallel_histogram", "comm", "basesize=16384"]`  | 0.91 (5%) :white_check_mark: |                1.01 (1%) :x: |
| `["parallel_histogram", "comm", "basesize=4096"]`   |                   0.96 (5%)  | 0.98 (1%) :white_check_mark: |
| `["parallel_histogram", "comm", "basesize=8192"]`   |                   1.02 (5%)  |                1.27 (1%) :x: |
| `["parallel_histogram", "seq"]`                     | 0.92 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["partition_length_maximum", "rand", "foldl"]`     |                1.06 (5%) :x: |                   1.00 (1%)  |
| `["splitby", "count", "foldl"]`                     | 0.85 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["splitby", "count", "reduce"]`                    |                   1.01 (5%)  |                1.03 (1%) :x: |
| `["sum", "random", "foldl"]`                        |                1.06 (5%) :x: |                   1.00 (1%)  |
| `["words", "nthreads=1"]`                           | 0.94 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["words", "nthreads=2"]`                           | 0.92 (5%) :white_check_mark: |                   1.01 (1%)  |
| `["words", "nthreads=4"]`                           | 0.93 (5%) :white_check_mark: |                   0.99 (1%)  |

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
Julia Version 1.7.2
Commit bf53498635 (2022-02-06 15:21 UTC)
Platform Info:
  OS: Linux (x86_64-pc-linux-gnu)
      Ubuntu 20.04.3 LTS
  uname: Linux 5.11.0-1028-azure #31~20.04.2-Ubuntu SMP Tue Jan 18 08:46:15 UTC 2022 x86_64 x86_64
  CPU: Intel(R) Xeon(R) Platinum 8171M CPU @ 2.60GHz: 
              speed         user         nice          sys         idle          irq
       #1  2095 MHz       5567 s          2 s        266 s       1642 s          0 s
       #2  2095 MHz       5302 s          0 s        230 s       1971 s          0 s
       
  Memory: 6.7845458984375 GB (3564.61328125 MB free)
  Uptime: 755.41 sec
  Load Avg:  1.62  1.48  0.9
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-12.0.1 (ORCJIT, skylake-avx512)
```

### Baseline
```
Julia Version 1.7.2
Commit bf53498635 (2022-02-06 15:21 UTC)
Platform Info:
  OS: Linux (x86_64-pc-linux-gnu)
      Ubuntu 20.04.3 LTS
  uname: Linux 5.11.0-1028-azure #31~20.04.2-Ubuntu SMP Tue Jan 18 08:46:15 UTC 2022 x86_64 x86_64
  CPU: Intel(R) Xeon(R) Platinum 8171M CPU @ 2.60GHz: 
              speed         user         nice          sys         idle          irq
       #1  2095 MHz       8095 s          2 s        342 s       2233 s          0 s
       #2  2095 MHz       7640 s          0 s        316 s       2738 s          0 s
       
  Memory: 6.7845458984375 GB (3466.546875 MB free)
  Uptime: 1075.48 sec
  Load Avg:  1.55  1.55  1.11
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-12.0.1 (ORCJIT, skylake-avx512)
```

---
# Target result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmark: 13 Feb 2022 - 1:27
* Package commit: 79eb3f
* Julia commit: bf5349
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
| `["collect", "assoc", "basesize=1"]`                | 279.961 ms (5%) |         |  25.97 MiB (1%) |      306785 |
| `["collect", "assoc", "basesize=1024"]`             | 223.529 ms (5%) |         |   2.61 MiB (1%) |         456 |
| `["collect", "assoc", "basesize=32"]`               | 224.762 ms (5%) |         |   4.82 MiB (1%) |       11705 |
| `["collect", "seq"]`                                | 429.413 ms (5%) |         | 812.73 KiB (1%) |          11 |
| `["collect", "unordered", "basesize=1"]`            | 398.892 ms (5%) |         |  23.91 MiB (1%) |      413470 |
| `["collect", "unordered", "basesize=1024"]`         | 241.516 ms (5%) |         |   1.01 MiB (1%) |        1082 |
| `["collect", "unordered", "basesize=32"]`           | 252.452 ms (5%) |         |   1.59 MiB (1%) |       14895 |
| `["findfirst", "n=1000", "foldl"]`                  | 730.638 ms (5%) |         |                 |             |
| `["findfirst", "n=1000", "reduce", "basesize=128"]` | 402.232 ms (5%) |         | 230.48 KiB (1%) |        3245 |
| `["findfirst", "n=1000", "reduce", "basesize=256"]` | 496.694 ms (5%) |         | 157.20 KiB (1%) |        2193 |
| `["findfirst", "n=1000", "reduce", "basesize=512"]` | 663.820 ms (5%) |         | 108.05 KiB (1%) |        1505 |
| `["findfirst", "n=400", "foldl"]`                   | 532.215 ms (5%) |         |                 |             |
| `["findfirst", "n=400", "reduce", "basesize=128"]`  | 286.876 ms (5%) |         | 386.08 KiB (1%) |        5486 |
| `["findfirst", "n=400", "reduce", "basesize=256"]`  | 291.019 ms (5%) |         | 200.86 KiB (1%) |        2873 |
| `["findfirst", "n=400", "reduce", "basesize=512"]`  | 381.395 ms (5%) |         | 139.36 KiB (1%) |        1986 |
| `["findfirst", "n=500", "foldl"]`                   |  91.229 ms (5%) |         |                 |             |
| `["findfirst", "n=500", "reduce", "basesize=128"]`  | 186.509 ms (5%) |         | 234.27 KiB (1%) |        3226 |
| `["findfirst", "n=500", "reduce", "basesize=256"]`  |  86.781 ms (5%) |         |  74.34 KiB (1%) |        1012 |
| `["findfirst", "n=500", "reduce", "basesize=512"]`  | 137.250 ms (5%) |         |  63.67 KiB (1%) |         866 |
| `["overhead", "default"]`                           |  73.504 μs (5%) |         |  32.73 KiB (1%) |         418 |
| `["overhead", "stoppable=false"]`                   |  75.205 μs (5%) |         |  32.72 KiB (1%) |         417 |
| `["overhead", "stoppable=true"]`                    |  86.705 μs (5%) |         |  44.28 KiB (1%) |         611 |
| `["parallel_histogram", "assoc", "basesize=16384"]` |   3.149 ms (5%) |         | 728.91 KiB (1%) |          57 |
| `["parallel_histogram", "assoc", "basesize=4096"]`  |   3.811 ms (5%) |         |   1.79 MiB (1%) |         216 |
| `["parallel_histogram", "assoc", "basesize=8192"]`  |   3.476 ms (5%) |         |   1.42 MiB (1%) |         118 |
| `["parallel_histogram", "comm", "basesize=16384"]`  |  18.100 ms (5%) |         |   1.55 MiB (1%) |        1507 |
| `["parallel_histogram", "comm", "basesize=4096"]`   |  27.492 ms (5%) |         |   1.23 MiB (1%) |        6329 |
| `["parallel_histogram", "comm", "basesize=8192"]`   |  25.756 ms (5%) |         |   1.67 MiB (1%) |        5440 |
| `["parallel_histogram", "seq"]`                     |   4.850 ms (5%) |         | 364.16 KiB (1%) |          24 |
| `["partition_length_maximum", "rand", "foldl"]`     |  37.907 ms (5%) |         |                 |             |
| `["partition_length_maximum", "rand", "reduce"]`    |  19.134 ms (5%) |         |  736 bytes (1%) |          11 |
| `["splitby", "count", "foldl"]`                     |   1.928 ms (5%) |         |                 |             |
| `["splitby", "count", "man"]`                       |   1.460 ms (5%) |         |                 |             |
| `["splitby", "count", "reduce"]`                    |   1.049 ms (5%) |         |   1.09 KiB (1%) |          19 |
| `["sum", "random", "foldl"]`                        |  17.018 ms (5%) |         |                 |             |
| `["sum", "random", "reduce", "basesize=128"]`       |   8.113 ms (5%) |         |  74.08 KiB (1%) |        1101 |
| `["sum", "random", "reduce", "basesize=256"]`       |   8.021 ms (5%) |         |  36.73 KiB (1%) |         546 |
| `["sum", "random", "reduce", "basesize=512"]`       |   7.997 ms (5%) |         |  18.08 KiB (1%) |         269 |
| `["sum", "uniform", "foldl"]`                       |  15.230 ms (5%) |         |                 |             |
| `["sum", "uniform", "reduce", "basesize=128"]`      |   8.328 ms (5%) |         |  74.17 KiB (1%) |        1104 |
| `["sum", "uniform", "reduce", "basesize=256"]`      |   8.078 ms (5%) |         |  36.70 KiB (1%) |         545 |
| `["sum", "uniform", "reduce", "basesize=512"]`      |   7.954 ms (5%) |         |  18.06 KiB (1%) |         269 |
| `["sum", "valley", "foldl"]`                        |  15.988 ms (5%) |         |                 |             |
| `["sum", "valley", "reduce", "basesize=128"]`       |   8.267 ms (5%) |         |  74.11 KiB (1%) |        1102 |
| `["sum", "valley", "reduce", "basesize=256"]`       |   8.155 ms (5%) |         |  36.73 KiB (1%) |         546 |
| `["sum", "valley", "reduce", "basesize=512"]`       |   8.483 ms (5%) |         |  18.03 KiB (1%) |         268 |
| `["words", "nthreads=1"]`                           |  23.803 ms (5%) |         |  31.80 MiB (1%) |     1036053 |
| `["words", "nthreads=2"]`                           |  15.373 ms (5%) |         |  32.52 MiB (1%) |     1036132 |
| `["words", "nthreads=4"]`                           |  15.427 ms (5%) |         |  32.96 MiB (1%) |     1036209 |

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
Julia Version 1.7.2
Commit bf53498635 (2022-02-06 15:21 UTC)
Platform Info:
  OS: Linux (x86_64-pc-linux-gnu)
      Ubuntu 20.04.3 LTS
  uname: Linux 5.11.0-1028-azure #31~20.04.2-Ubuntu SMP Tue Jan 18 08:46:15 UTC 2022 x86_64 x86_64
  CPU: Intel(R) Xeon(R) Platinum 8171M CPU @ 2.60GHz: 
              speed         user         nice          sys         idle          irq
       #1  2095 MHz       5567 s          2 s        266 s       1642 s          0 s
       #2  2095 MHz       5302 s          0 s        230 s       1971 s          0 s
       
  Memory: 6.7845458984375 GB (3564.61328125 MB free)
  Uptime: 755.41 sec
  Load Avg:  1.62  1.48  0.9
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-12.0.1 (ORCJIT, skylake-avx512)
```

---
# Baseline result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmark: 13 Feb 2022 - 1:32
* Package commit: 39038b
* Julia commit: bf5349
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
| `["collect", "assoc", "basesize=1"]`                | 290.510 ms (5%) |         |  25.97 MiB (1%) |      306830 |
| `["collect", "assoc", "basesize=1024"]`             | 228.260 ms (5%) |         |   2.61 MiB (1%) |         456 |
| `["collect", "assoc", "basesize=32"]`               | 228.595 ms (5%) |         |   4.82 MiB (1%) |       11701 |
| `["collect", "seq"]`                                | 447.044 ms (5%) |         | 812.73 KiB (1%) |          11 |
| `["collect", "unordered", "basesize=1"]`            | 395.456 ms (5%) |         |  23.85 MiB (1%) |      411521 |
| `["collect", "unordered", "basesize=1024"]`         | 244.491 ms (5%) |         |   1.01 MiB (1%) |        1016 |
| `["collect", "unordered", "basesize=32"]`           | 259.221 ms (5%) |         |   1.58 MiB (1%) |       14767 |
| `["findfirst", "n=1000", "foldl"]`                  | 693.827 ms (5%) |         |                 |             |
| `["findfirst", "n=1000", "reduce", "basesize=128"]` | 748.859 ms (5%) |         | 418.52 KiB (1%) |        5858 |
| `["findfirst", "n=1000", "reduce", "basesize=256"]` | 480.816 ms (5%) |         | 157.23 KiB (1%) |        2194 |
| `["findfirst", "n=1000", "reduce", "basesize=512"]` |    1.013 s (5%) |         | 155.39 KiB (1%) |        2184 |
| `["findfirst", "n=400", "foldl"]`                   | 530.184 ms (5%) |         |                 |             |
| `["findfirst", "n=400", "reduce", "basesize=128"]`  | 360.589 ms (5%) |         | 482.30 KiB (1%) |        6850 |
| `["findfirst", "n=400", "reduce", "basesize=256"]`  | 291.302 ms (5%) |         | 201.05 KiB (1%) |        2879 |
| `["findfirst", "n=400", "reduce", "basesize=512"]`  | 420.648 ms (5%) |         | 144.67 KiB (1%) |        2078 |
| `["findfirst", "n=500", "foldl"]`                   |  84.358 ms (5%) |         |                 |             |
| `["findfirst", "n=500", "reduce", "basesize=128"]`  | 175.588 ms (5%) |         | 206.45 KiB (1%) |        2888 |
| `["findfirst", "n=500", "reduce", "basesize=256"]`  | 258.211 ms (5%) |         | 156.16 KiB (1%) |        2163 |
| `["findfirst", "n=500", "reduce", "basesize=512"]`  | 124.211 ms (5%) |         |  55.95 KiB (1%) |         765 |
| `["overhead", "default"]`                           |  79.806 μs (5%) |         |  32.73 KiB (1%) |         418 |
| `["overhead", "stoppable=false"]`                   |  82.405 μs (5%) |         |  32.75 KiB (1%) |         418 |
| `["overhead", "stoppable=true"]`                    |  96.207 μs (5%) |         |  44.28 KiB (1%) |         611 |
| `["parallel_histogram", "assoc", "basesize=16384"]` |   3.139 ms (5%) |         | 728.91 KiB (1%) |          57 |
| `["parallel_histogram", "assoc", "basesize=4096"]`  |   3.965 ms (5%) |         |   2.05 MiB (1%) |         221 |
| `["parallel_histogram", "assoc", "basesize=8192"]`  |   3.613 ms (5%) |         |   1.42 MiB (1%) |         117 |
| `["parallel_histogram", "comm", "basesize=16384"]`  |  19.940 ms (5%) |         |   1.53 MiB (1%) |         911 |
| `["parallel_histogram", "comm", "basesize=4096"]`   |  28.602 ms (5%) |         |   1.25 MiB (1%) |        7004 |
| `["parallel_histogram", "comm", "basesize=8192"]`   |  25.357 ms (5%) |         |   1.31 MiB (1%) |        5813 |
| `["parallel_histogram", "seq"]`                     |   5.250 ms (5%) |         | 364.16 KiB (1%) |          24 |
| `["partition_length_maximum", "rand", "foldl"]`     |  35.604 ms (5%) |         |                 |             |
| `["partition_length_maximum", "rand", "reduce"]`    |  18.748 ms (5%) |         |  736 bytes (1%) |          11 |
| `["splitby", "count", "foldl"]`                     |   2.264 ms (5%) |         |                 |             |
| `["splitby", "count", "man"]`                       |   1.504 ms (5%) |         |                 |             |
| `["splitby", "count", "reduce"]`                    |   1.043 ms (5%) |         |   1.06 KiB (1%) |          18 |
| `["sum", "random", "foldl"]`                        |  16.121 ms (5%) |         |                 |             |
| `["sum", "random", "reduce", "basesize=128"]`       |   8.362 ms (5%) |         |  74.20 KiB (1%) |        1105 |
| `["sum", "random", "reduce", "basesize=256"]`       |   8.278 ms (5%) |         |  36.73 KiB (1%) |         546 |
| `["sum", "random", "reduce", "basesize=512"]`       |   8.257 ms (5%) |         |  18.08 KiB (1%) |         269 |
| `["sum", "uniform", "foldl"]`                       |  15.356 ms (5%) |         |                 |             |
| `["sum", "uniform", "reduce", "basesize=128"]`      |   8.301 ms (5%) |         |  74.20 KiB (1%) |        1105 |
| `["sum", "uniform", "reduce", "basesize=256"]`      |   8.020 ms (5%) |         |  36.77 KiB (1%) |         547 |
| `["sum", "uniform", "reduce", "basesize=512"]`      |   7.895 ms (5%) |         |  18.00 KiB (1%) |         267 |
| `["sum", "valley", "foldl"]`                        |  15.472 ms (5%) |         |                 |             |
| `["sum", "valley", "reduce", "basesize=128"]`       |   8.446 ms (5%) |         |  74.05 KiB (1%) |        1100 |
| `["sum", "valley", "reduce", "basesize=256"]`       |   8.210 ms (5%) |         |  36.77 KiB (1%) |         547 |
| `["sum", "valley", "reduce", "basesize=512"]`       |   8.267 ms (5%) |         |  18.00 KiB (1%) |         267 |
| `["words", "nthreads=1"]`                           |  25.343 ms (5%) |         |  31.90 MiB (1%) |     1039286 |
| `["words", "nthreads=2"]`                           |  16.786 ms (5%) |         |  32.26 MiB (1%) |     1039326 |
| `["words", "nthreads=4"]`                           |  16.581 ms (5%) |         |  33.16 MiB (1%) |     1039462 |

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
Julia Version 1.7.2
Commit bf53498635 (2022-02-06 15:21 UTC)
Platform Info:
  OS: Linux (x86_64-pc-linux-gnu)
      Ubuntu 20.04.3 LTS
  uname: Linux 5.11.0-1028-azure #31~20.04.2-Ubuntu SMP Tue Jan 18 08:46:15 UTC 2022 x86_64 x86_64
  CPU: Intel(R) Xeon(R) Platinum 8171M CPU @ 2.60GHz: 
              speed         user         nice          sys         idle          irq
       #1  2095 MHz       8095 s          2 s        342 s       2233 s          0 s
       #2  2095 MHz       7640 s          0 s        316 s       2738 s          0 s
       
  Memory: 6.7845458984375 GB (3466.546875 MB free)
  Uptime: 1075.48 sec
  Load Avg:  1.55  1.55  1.11
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
    Model:                           85
    Model name:                      Intel(R) Xeon(R) Platinum 8171M CPU @ 2.60GHz
    Stepping:                        4
    CPU MHz:                         2095.176
    BogoMIPS:                        4190.35
    Hypervisor vendor:               Microsoft
    Virtualization type:             full
    L1d cache:                       64 KiB
    L1i cache:                       64 KiB
    L2 cache:                        2 MiB
    L3 cache:                        35.8 MiB
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
    Flags:                           fpu vme de pse tsc msr pae mce cx8 apic sep mtrr pge mca cmov pat pse36 clflush mmx fxsr sse sse2 ss ht syscall nx pdpe1gb rdtscp lm constant_tsc rep_good nopl xtopology cpuid pni pclmulqdq ssse3 fma cx16 pcid sse4_1 sse4_2 movbe popcnt aes xsave avx f16c rdrand hypervisor lahf_lm abm 3dnowprefetch invpcid_single pti fsgsbase bmi1 hle avx2 smep bmi2 erms invpcid rtm mpx avx512f avx512dq rdseed adx smap clflushopt avx512cd avx512bw avx512vl xsaveopt xsavec xsaves md_clear
    

| Cpu Property       | Value                                                   |
|:------------------ |:------------------------------------------------------- |
| Brand              | Intel(R) Xeon(R) Platinum 8171M CPU @ 2.60GHz           |
| Vendor             | :Intel                                                  |
| Architecture       | :Skylake                                                |
| Model              | Family: 0x06, Model: 0x55, Stepping: 0x04, Type: 0x00   |
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

