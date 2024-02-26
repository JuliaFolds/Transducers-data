# Multi-thread benchmark result

* Pull request commit: [`e85ab1e6914fbadee7f30527bfc79f3a0fe013a9`](https://github.com/JuliaFolds/Transducers.jl/commit/e85ab1e6914fbadee7f30527bfc79f3a0fe013a9)
* Pull request: <https://github.com/JuliaFolds/Transducers.jl/pull/243> (Update */Manifest.toml)

# Judge result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmarks:
    - Target: 26 Feb 2024 - 01:23
    - Baseline: 26 Feb 2024 - 01:28
* Package commits:
    - Target: ded6e0
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
| `["findfirst", "n=1000", "reduce", "basesize=512"]` | 0.44 (5%) :white_check_mark: | 0.48 (1%) :white_check_mark: |
| `["findfirst", "n=400", "reduce", "basesize=128"]`  |                   0.97 (5%)  | 0.97 (1%) :white_check_mark: |
| `["findfirst", "n=400", "reduce", "basesize=512"]`  | 0.91 (5%) :white_check_mark: | 0.94 (1%) :white_check_mark: |
| `["findfirst", "n=500", "reduce", "basesize=128"]`  |                1.28 (5%) :x: |                1.33 (1%) :x: |
| `["findfirst", "n=500", "reduce", "basesize=256"]`  | 0.91 (5%) :white_check_mark: |                1.10 (1%) :x: |
| `["findfirst", "n=500", "reduce", "basesize=512"]`  |                1.05 (5%) :x: |                1.09 (1%) :x: |
| `["overhead", "stoppable=false"]`                   | 0.94 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["parallel_histogram", "assoc", "basesize=4096"]`  |                   1.05 (5%)  |                1.15 (1%) :x: |
| `["parallel_histogram", "comm", "basesize=16384"]`  |                1.08 (5%) :x: |                1.03 (1%) :x: |
| `["parallel_histogram", "comm", "basesize=4096"]`   |                   1.03 (5%)  |                1.03 (1%) :x: |
| `["splitby", "count", "foldl"]`                     |                1.06 (5%) :x: |                   1.00 (1%)  |
| `["splitby", "count", "reduce"]`                    |                   1.00 (5%)  | 0.94 (1%) :white_check_mark: |

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
      Ubuntu 22.04.4 LTS
  uname: Linux 6.2.0-1019-azure #19~22.04.1-Ubuntu SMP Wed Jan 10 22:57:03 UTC 2024 x86_64 x86_64
  CPU: AMD EPYC 7763 64-Core Processor: 
              speed         user         nice          sys         idle          irq
       #1  3244 MHz       2853 s          0 s        167 s       4056 s          0 s
       #2  2445 MHz       2776 s          0 s        172 s       4123 s          0 s
       #3  3180 MHz       2361 s          0 s        160 s       4546 s          0 s
       #4  2605 MHz       1993 s          0 s        165 s       4917 s          0 s
       
  Memory: 15.606903076171875 GB (12475.98828125 MB free)
  Uptime: 711.12 sec
  Load Avg:  1.75  1.53  0.89
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
      Ubuntu 22.04.4 LTS
  uname: Linux 6.2.0-1019-azure #19~22.04.1-Ubuntu SMP Wed Jan 10 22:57:03 UTC 2024 x86_64 x86_64
  CPU: AMD EPYC 7763 64-Core Processor: 
              speed         user         nice          sys         idle          irq
       #1  2445 MHz       4020 s          0 s        222 s       5728 s          0 s
       #2  2445 MHz       3812 s          0 s        225 s       5930 s          0 s
       #3  3242 MHz       3680 s          0 s        204 s       6078 s          0 s
       #4  3254 MHz       3050 s          0 s        220 s       6702 s          0 s
       
  Memory: 15.606903076171875 GB (12428.84375 MB free)
  Uptime: 1001.39 sec
  Load Avg:  1.71  1.69  1.15
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-12.0.1 (ORCJIT, znver3)
```

---
# Target result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmark: 26 Feb 2024 - 1:23
* Package commit: ded6e0
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
| `["collect", "assoc", "basesize=1"]`                | 148.597 ms (5%) |         |   4.36 MiB (1%) |       32800 |
| `["collect", "assoc", "basesize=1024"]`             | 147.426 ms (5%) |         |   1.09 MiB (1%) |          53 |
| `["collect", "assoc", "basesize=32"]`               | 147.584 ms (5%) |         |   1.48 MiB (1%) |        1052 |
| `["collect", "seq"]`                                | 294.497 ms (5%) |         | 256.05 KiB (1%) |           2 |
| `["collect", "unordered", "basesize=1"]`            | 245.807 ms (5%) |         |  23.78 MiB (1%) |      409067 |
| `["collect", "unordered", "basesize=1024"]`         | 156.538 ms (5%) |         |   1.02 MiB (1%) |        1267 |
| `["collect", "unordered", "basesize=32"]`           | 163.807 ms (5%) |         |   1.60 MiB (1%) |       15278 |
| `["findfirst", "n=1000", "foldl"]`                  | 506.695 ms (5%) |         |                 |             |
| `["findfirst", "n=1000", "reduce", "basesize=128"]` | 277.484 ms (5%) |         | 232.92 KiB (1%) |        3278 |
| `["findfirst", "n=1000", "reduce", "basesize=256"]` | 339.490 ms (5%) |         | 157.20 KiB (1%) |        2193 |
| `["findfirst", "n=1000", "reduce", "basesize=512"]` | 347.284 ms (5%) |         |  81.33 KiB (1%) |        1146 |
| `["findfirst", "n=400", "foldl"]`                   | 378.892 ms (5%) |         |                 |             |
| `["findfirst", "n=400", "reduce", "basesize=128"]`  | 193.031 ms (5%) |         | 373.78 KiB (1%) |        5336 |
| `["findfirst", "n=400", "reduce", "basesize=256"]`  | 198.844 ms (5%) |         | 200.83 KiB (1%) |        2872 |
| `["findfirst", "n=400", "reduce", "basesize=512"]`  | 283.934 ms (5%) |         | 150.92 KiB (1%) |        2139 |
| `["findfirst", "n=500", "foldl"]`                   |  64.595 ms (5%) |         |                 |             |
| `["findfirst", "n=500", "reduce", "basesize=128"]`  | 121.319 ms (5%) |         | 224.20 KiB (1%) |        3071 |
| `["findfirst", "n=500", "reduce", "basesize=256"]`  | 131.833 ms (5%) |         | 151.12 KiB (1%) |        2038 |
| `["findfirst", "n=500", "reduce", "basesize=512"]`  |  85.117 ms (5%) |         |  60.31 KiB (1%) |         816 |
| `["overhead", "default"]`                           |  52.248 μs (5%) |         |  32.73 KiB (1%) |         418 |
| `["overhead", "stoppable=false"]`                   |  50.203 μs (5%) |         |  32.75 KiB (1%) |         418 |
| `["overhead", "stoppable=true"]`                    |  57.959 μs (5%) |         |  44.25 KiB (1%) |         610 |
| `["parallel_histogram", "assoc", "basesize=16384"]` |   2.377 ms (5%) |         | 728.91 KiB (1%) |          57 |
| `["parallel_histogram", "assoc", "basesize=4096"]`  |   3.061 ms (5%) |         |   2.05 MiB (1%) |         222 |
| `["parallel_histogram", "assoc", "basesize=8192"]`  |   2.660 ms (5%) |         |   1.42 MiB (1%) |         117 |
| `["parallel_histogram", "comm", "basesize=16384"]`  |   8.614 ms (5%) |         |   1.59 MiB (1%) |        2698 |
| `["parallel_histogram", "comm", "basesize=4096"]`   |  13.471 ms (5%) |         |   1.41 MiB (1%) |       12272 |
| `["parallel_histogram", "comm", "basesize=8192"]`   |  11.447 ms (5%) |         |   1.29 MiB (1%) |        8629 |
| `["parallel_histogram", "seq"]`                     |   4.235 ms (5%) |         | 364.16 KiB (1%) |          24 |
| `["partition_length_maximum", "rand", "foldl"]`     |  31.117 ms (5%) |         |                 |             |
| `["partition_length_maximum", "rand", "reduce"]`    |  15.571 ms (5%) |         |  736 bytes (1%) |          11 |
| `["splitby", "count", "foldl"]`                     |   1.553 ms (5%) |         |                 |             |
| `["splitby", "count", "man"]`                       |   1.132 ms (5%) |         |                 |             |
| `["splitby", "count", "reduce"]`                    | 722.068 μs (5%) |         |   1.03 KiB (1%) |          18 |
| `["sum", "random", "foldl"]`                        |  10.992 ms (5%) |         |                 |             |
| `["sum", "random", "reduce", "basesize=128"]`       |   5.628 ms (5%) |         |  74.14 KiB (1%) |        1103 |
| `["sum", "random", "reduce", "basesize=256"]`       |   5.573 ms (5%) |         |  36.70 KiB (1%) |         545 |
| `["sum", "random", "reduce", "basesize=512"]`       |   5.538 ms (5%) |         |  18.08 KiB (1%) |         269 |
| `["sum", "uniform", "foldl"]`                       |  10.872 ms (5%) |         |                 |             |
| `["sum", "uniform", "reduce", "basesize=128"]`      |   5.581 ms (5%) |         |  74.08 KiB (1%) |        1101 |
| `["sum", "uniform", "reduce", "basesize=256"]`      |   5.514 ms (5%) |         |  36.77 KiB (1%) |         547 |
| `["sum", "uniform", "reduce", "basesize=512"]`      |   5.477 ms (5%) |         |  18.03 KiB (1%) |         268 |
| `["sum", "valley", "foldl"]`                        |  11.112 ms (5%) |         |                 |             |
| `["sum", "valley", "reduce", "basesize=128"]`       |   5.687 ms (5%) |         |  74.05 KiB (1%) |        1100 |
| `["sum", "valley", "reduce", "basesize=256"]`       |   5.631 ms (5%) |         |  36.70 KiB (1%) |         545 |
| `["sum", "valley", "reduce", "basesize=512"]`       |   5.599 ms (5%) |         |  18.06 KiB (1%) |         269 |
| `["words", "nthreads=1"]`                           |  14.413 ms (5%) |         |  31.79 MiB (1%) |     1035556 |
| `["words", "nthreads=2"]`                           |   9.130 ms (5%) |         |  32.15 MiB (1%) |     1035592 |
| `["words", "nthreads=4"]`                           |   9.399 ms (5%) |         |  32.86 MiB (1%) |     1035665 |

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
      Ubuntu 22.04.4 LTS
  uname: Linux 6.2.0-1019-azure #19~22.04.1-Ubuntu SMP Wed Jan 10 22:57:03 UTC 2024 x86_64 x86_64
  CPU: AMD EPYC 7763 64-Core Processor: 
              speed         user         nice          sys         idle          irq
       #1  3244 MHz       2853 s          0 s        167 s       4056 s          0 s
       #2  2445 MHz       2776 s          0 s        172 s       4123 s          0 s
       #3  3180 MHz       2361 s          0 s        160 s       4546 s          0 s
       #4  2605 MHz       1993 s          0 s        165 s       4917 s          0 s
       
  Memory: 15.606903076171875 GB (12475.98828125 MB free)
  Uptime: 711.12 sec
  Load Avg:  1.75  1.53  0.89
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-12.0.1 (ORCJIT, znver3)
```

---
# Baseline result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmark: 26 Feb 2024 - 1:28
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
| `["collect", "assoc", "basesize=1"]`                | 149.024 ms (5%) |         |   4.36 MiB (1%) |       32800 |
| `["collect", "assoc", "basesize=1024"]`             | 147.480 ms (5%) |         |   1.09 MiB (1%) |          54 |
| `["collect", "assoc", "basesize=32"]`               | 147.544 ms (5%) |         |   1.48 MiB (1%) |        1052 |
| `["collect", "seq"]`                                | 294.563 ms (5%) |         | 256.05 KiB (1%) |           2 |
| `["collect", "unordered", "basesize=1"]`            | 246.737 ms (5%) |         |  23.77 MiB (1%) |      408896 |
| `["collect", "unordered", "basesize=1024"]`         | 156.386 ms (5%) |         |   1.01 MiB (1%) |        1100 |
| `["collect", "unordered", "basesize=32"]`           | 163.167 ms (5%) |         |   1.60 MiB (1%) |       15272 |
| `["findfirst", "n=1000", "foldl"]`                  | 506.891 ms (5%) |         |                 |             |
| `["findfirst", "n=1000", "reduce", "basesize=128"]` | 276.208 ms (5%) |         | 232.83 KiB (1%) |        3275 |
| `["findfirst", "n=1000", "reduce", "basesize=256"]` | 339.206 ms (5%) |         | 157.20 KiB (1%) |        2193 |
| `["findfirst", "n=1000", "reduce", "basesize=512"]` | 792.759 ms (5%) |         | 168.34 KiB (1%) |        2377 |
| `["findfirst", "n=400", "foldl"]`                   | 379.186 ms (5%) |         |                 |             |
| `["findfirst", "n=400", "reduce", "basesize=128"]`  | 198.186 ms (5%) |         | 384.50 KiB (1%) |        5486 |
| `["findfirst", "n=400", "reduce", "basesize=256"]`  | 197.933 ms (5%) |         | 200.86 KiB (1%) |        2873 |
| `["findfirst", "n=400", "reduce", "basesize=512"]`  | 311.122 ms (5%) |         | 161.03 KiB (1%) |        2330 |
| `["findfirst", "n=500", "foldl"]`                   |  65.272 ms (5%) |         |                 |             |
| `["findfirst", "n=500", "reduce", "basesize=128"]`  |  94.902 ms (5%) |         | 168.41 KiB (1%) |        2327 |
| `["findfirst", "n=500", "reduce", "basesize=256"]`  | 145.430 ms (5%) |         | 137.20 KiB (1%) |        1921 |
| `["findfirst", "n=500", "reduce", "basesize=512"]`  |  80.870 ms (5%) |         |  55.28 KiB (1%) |         758 |
| `["overhead", "default"]`                           |  50.624 μs (5%) |         |  32.77 KiB (1%) |         419 |
| `["overhead", "stoppable=false"]`                   |  53.500 μs (5%) |         |  32.81 KiB (1%) |         420 |
| `["overhead", "stoppable=true"]`                    |  57.828 μs (5%) |         |  44.25 KiB (1%) |         610 |
| `["parallel_histogram", "assoc", "basesize=16384"]` |   2.374 ms (5%) |         | 728.91 KiB (1%) |          57 |
| `["parallel_histogram", "assoc", "basesize=4096"]`  |   2.923 ms (5%) |         |   1.79 MiB (1%) |         216 |
| `["parallel_histogram", "assoc", "basesize=8192"]`  |   2.650 ms (5%) |         |   1.42 MiB (1%) |         117 |
| `["parallel_histogram", "comm", "basesize=16384"]`  |   8.006 ms (5%) |         |   1.54 MiB (1%) |        1252 |
| `["parallel_histogram", "comm", "basesize=4096"]`   |  13.141 ms (5%) |         |   1.36 MiB (1%) |       10760 |
| `["parallel_histogram", "comm", "basesize=8192"]`   |  11.505 ms (5%) |         |   1.28 MiB (1%) |        8211 |
| `["parallel_histogram", "seq"]`                     |   4.230 ms (5%) |         | 364.16 KiB (1%) |          24 |
| `["partition_length_maximum", "rand", "foldl"]`     |  31.108 ms (5%) |         |                 |             |
| `["partition_length_maximum", "rand", "reduce"]`    |  15.588 ms (5%) |         |  736 bytes (1%) |          11 |
| `["splitby", "count", "foldl"]`                     |   1.464 ms (5%) |         |                 |             |
| `["splitby", "count", "man"]`                       |   1.157 ms (5%) |         |                 |             |
| `["splitby", "count", "reduce"]`                    | 722.610 μs (5%) |         |   1.09 KiB (1%) |          19 |
| `["sum", "random", "foldl"]`                        |  10.978 ms (5%) |         |                 |             |
| `["sum", "random", "reduce", "basesize=128"]`       |   5.600 ms (5%) |         |  74.17 KiB (1%) |        1104 |
| `["sum", "random", "reduce", "basesize=256"]`       |   5.559 ms (5%) |         |  36.70 KiB (1%) |         545 |
| `["sum", "random", "reduce", "basesize=512"]`       |   5.531 ms (5%) |         |  18.08 KiB (1%) |         269 |
| `["sum", "uniform", "foldl"]`                       |  10.905 ms (5%) |         |                 |             |
| `["sum", "uniform", "reduce", "basesize=128"]`      |   5.575 ms (5%) |         |  74.14 KiB (1%) |        1103 |
| `["sum", "uniform", "reduce", "basesize=256"]`      |   5.527 ms (5%) |         |  36.67 KiB (1%) |         544 |
| `["sum", "uniform", "reduce", "basesize=512"]`      |   5.485 ms (5%) |         |  18.00 KiB (1%) |         267 |
| `["sum", "valley", "foldl"]`                        |  11.113 ms (5%) |         |                 |             |
| `["sum", "valley", "reduce", "basesize=128"]`       |   5.698 ms (5%) |         |  74.05 KiB (1%) |        1100 |
| `["sum", "valley", "reduce", "basesize=256"]`       |   5.638 ms (5%) |         |  36.73 KiB (1%) |         546 |
| `["sum", "valley", "reduce", "basesize=512"]`       |   5.604 ms (5%) |         |  18.03 KiB (1%) |         268 |
| `["words", "nthreads=1"]`                           |  14.392 ms (5%) |         |  31.59 MiB (1%) |     1029065 |
| `["words", "nthreads=2"]`                           |   9.545 ms (5%) |         |  32.31 MiB (1%) |     1029144 |
| `["words", "nthreads=4"]`                           |   9.730 ms (5%) |         |  32.75 MiB (1%) |     1029210 |

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
      Ubuntu 22.04.4 LTS
  uname: Linux 6.2.0-1019-azure #19~22.04.1-Ubuntu SMP Wed Jan 10 22:57:03 UTC 2024 x86_64 x86_64
  CPU: AMD EPYC 7763 64-Core Processor: 
              speed         user         nice          sys         idle          irq
       #1  2445 MHz       4020 s          0 s        222 s       5728 s          0 s
       #2  2445 MHz       3812 s          0 s        225 s       5930 s          0 s
       #3  3242 MHz       3680 s          0 s        204 s       6078 s          0 s
       #4  3254 MHz       3050 s          0 s        220 s       6702 s          0 s
       
  Memory: 15.606903076171875 GB (12428.84375 MB free)
  Uptime: 1001.39 sec
  Load Avg:  1.71  1.69  1.15
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

    Architecture:                       x86_64
    CPU op-mode(s):                     32-bit, 64-bit
    Address sizes:                      48 bits physical, 48 bits virtual
    Byte Order:                         Little Endian
    CPU(s):                             4
    On-line CPU(s) list:                0-3
    Vendor ID:                          AuthenticAMD
    Model name:                         AMD EPYC 7763 64-Core Processor
    CPU family:                         25
    Model:                              1
    Thread(s) per core:                 2
    Core(s) per socket:                 2
    Socket(s):                          1
    Stepping:                           1
    BogoMIPS:                           4890.86
    Flags:                              fpu vme de pse tsc msr pae mce cx8 apic sep mtrr pge mca cmov pat pse36 clflush mmx fxsr sse sse2 ht syscall nx mmxext fxsr_opt pdpe1gb rdtscp lm constant_tsc rep_good nopl tsc_reliable nonstop_tsc cpuid extd_apicid aperfmperf pni pclmulqdq ssse3 fma cx16 pcid sse4_1 sse4_2 movbe popcnt aes xsave avx f16c rdrand hypervisor lahf_lm cmp_legacy svm cr8_legacy abm sse4a misalignsse 3dnowprefetch osvw topoext invpcid_single vmmcall fsgsbase bmi1 avx2 smep bmi2 erms invpcid rdseed adx smap clflushopt clwb sha_ni xsaveopt xsavec xgetbv1 xsaves clzero xsaveerptr rdpru arat npt nrip_save tsc_scale vmcb_clean flushbyasid decodeassists pausefilter pfthreshold v_vmsave_vmload umip vaes vpclmulqdq rdpid fsrm
    Virtualization:                     AMD-V
    Hypervisor vendor:                  Microsoft
    Virtualization type:                full
    L1d cache:                          64 KiB (2 instances)
    L1i cache:                          64 KiB (2 instances)
    L2 cache:                           1 MiB (2 instances)
    L3 cache:                           32 MiB (1 instance)
    NUMA node(s):                       1
    NUMA node0 CPU(s):                  0-3
    Vulnerability Gather data sampling: Not affected
    Vulnerability Itlb multihit:        Not affected
    Vulnerability L1tf:                 Not affected
    Vulnerability Mds:                  Not affected
    Vulnerability Meltdown:             Not affected
    Vulnerability Mmio stale data:      Not affected
    Vulnerability Retbleed:             Not affected
    Vulnerability Spec rstack overflow: Mitigation; safe RET, no microcode
    Vulnerability Spec store bypass:    Vulnerable
    Vulnerability Spectre v1:           Mitigation; usercopy/swapgs barriers and __user pointer sanitization
    Vulnerability Spectre v2:           Mitigation; Retpolines, STIBP disabled, RSB filling, PBRSB-eIBRS Not affected
    Vulnerability Srbds:                Not affected
    Vulnerability Tsx async abort:      Not affected
    

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

