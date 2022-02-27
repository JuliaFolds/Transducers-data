# Multi-thread benchmark result

* Pull request commit: [`b5e46283b5090007b230fff74772c6af00022f67`](https://github.com/JuliaFolds/Transducers.jl/commit/b5e46283b5090007b230fff74772c6af00022f67)
* Pull request: <https://github.com/JuliaFolds/Transducers.jl/pull/243> (Update */Manifest.toml)

# Judge result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmarks:
    - Target: 27 Feb 2022 - 01:29
    - Baseline: 27 Feb 2022 - 01:34
* Package commits:
    - Target: 2a6258
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
| `["findfirst", "n=1000", "reduce", "basesize=512"]` | 0.76 (5%) :white_check_mark: | 0.75 (1%) :white_check_mark: |
| `["findfirst", "n=400", "reduce", "basesize=512"]`  |                1.08 (5%) :x: |                1.03 (1%) :x: |
| `["findfirst", "n=500", "reduce", "basesize=128"]`  | 0.75 (5%) :white_check_mark: | 0.82 (1%) :white_check_mark: |
| `["findfirst", "n=500", "reduce", "basesize=256"]`  | 0.56 (5%) :white_check_mark: | 0.69 (1%) :white_check_mark: |
| `["findfirst", "n=500", "reduce", "basesize=512"]`  | 0.94 (5%) :white_check_mark: | 0.95 (1%) :white_check_mark: |
| `["overhead", "stoppable=true"]`                    |                1.08 (5%) :x: |                   1.00 (1%)  |
| `["parallel_histogram", "comm", "basesize=16384"]`  |                1.07 (5%) :x: |                   0.99 (1%)  |
| `["parallel_histogram", "comm", "basesize=4096"]`   | 0.91 (5%) :white_check_mark: | 0.92 (1%) :white_check_mark: |
| `["parallel_histogram", "comm", "basesize=8192"]`   | 0.76 (5%) :white_check_mark: |                1.01 (1%) :x: |

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
  CPU: Intel(R) Xeon(R) Platinum 8272CL CPU @ 2.60GHz: 
              speed         user         nice          sys         idle          irq
       #1  2593 MHz       5412 s          1 s        259 s       4916 s          0 s
       #2  2593 MHz       5275 s          0 s        260 s       5108 s          0 s
       
  Memory: 6.784542083740234 GB (3831.65625 MB free)
  Uptime: 1067.75 sec
  Load Avg:  1.72  1.52  0.91
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
  CPU: Intel(R) Xeon(R) Platinum 8272CL CPU @ 2.60GHz: 
              speed         user         nice          sys         idle          irq
       #1  2593 MHz       7418 s          1 s        333 s       6005 s          0 s
       #2  2593 MHz       8070 s          0 s        342 s       5405 s          0 s
       
  Memory: 6.784542083740234 GB (3759.16796875 MB free)
  Uptime: 1385.53 sec
  Load Avg:  1.59  1.54  1.1
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-12.0.1 (ORCJIT, skylake-avx512)
```

---
# Target result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmark: 27 Feb 2022 - 1:29
* Package commit: 2a6258
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

| ID                                                  | time            | GC time | memory           | allocations |
|-----------------------------------------------------|----------------:|--------:|-----------------:|------------:|
| `["collect", "assoc", "basesize=1"]`                | 255.528 ms (5%) |         |   25.97 MiB (1%) |      306846 |
| `["collect", "assoc", "basesize=1024"]`             | 199.096 ms (5%) |         |    2.61 MiB (1%) |         455 |
| `["collect", "assoc", "basesize=32"]`               | 202.438 ms (5%) |         |    4.82 MiB (1%) |       11700 |
| `["collect", "seq"]`                                | 395.286 ms (5%) |         |  812.73 KiB (1%) |          11 |
| `["collect", "unordered", "basesize=1"]`            | 359.072 ms (5%) |         |   23.70 MiB (1%) |      406300 |
| `["collect", "unordered", "basesize=1024"]`         | 215.951 ms (5%) |         | 1006.27 KiB (1%) |        1086 |
| `["collect", "unordered", "basesize=32"]`           | 227.265 ms (5%) |         |    1.58 MiB (1%) |       14696 |
| `["findfirst", "n=1000", "foldl"]`                  | 625.920 ms (5%) |         |                  |             |
| `["findfirst", "n=1000", "reduce", "basesize=128"]` | 344.847 ms (5%) |         |  232.86 KiB (1%) |        3276 |
| `["findfirst", "n=1000", "reduce", "basesize=256"]` | 423.083 ms (5%) |         |  157.20 KiB (1%) |        2193 |
| `["findfirst", "n=1000", "reduce", "basesize=512"]` | 430.320 ms (5%) |         |   81.33 KiB (1%) |        1146 |
| `["findfirst", "n=400", "foldl"]`                   | 469.124 ms (5%) |         |                  |             |
| `["findfirst", "n=400", "reduce", "basesize=128"]`  | 249.862 ms (5%) |         |  386.53 KiB (1%) |        5506 |
| `["findfirst", "n=400", "reduce", "basesize=256"]`  | 248.355 ms (5%) |         |  200.94 KiB (1%) |        2876 |
| `["findfirst", "n=400", "reduce", "basesize=512"]`  | 383.175 ms (5%) |         |  153.23 KiB (1%) |        2197 |
| `["findfirst", "n=500", "foldl"]`                   |  81.421 ms (5%) |         |                  |             |
| `["findfirst", "n=500", "reduce", "basesize=128"]`  | 161.709 ms (5%) |         |  230.48 KiB (1%) |        3177 |
| `["findfirst", "n=500", "reduce", "basesize=256"]`  |  85.427 ms (5%) |         |   82.30 KiB (1%) |        1113 |
| `["findfirst", "n=500", "reduce", "basesize=512"]`  | 110.176 ms (5%) |         |   60.73 KiB (1%) |         829 |
| `["overhead", "default"]`                           |  78.001 μs (5%) |         |   32.73 KiB (1%) |         418 |
| `["overhead", "stoppable=false"]`                   |  79.701 μs (5%) |         |   32.78 KiB (1%) |         419 |
| `["overhead", "stoppable=true"]`                    |  90.601 μs (5%) |         |   44.22 KiB (1%) |         609 |
| `["parallel_histogram", "assoc", "basesize=16384"]` |   3.216 ms (5%) |         |  728.91 KiB (1%) |          57 |
| `["parallel_histogram", "assoc", "basesize=4096"]`  |   3.859 ms (5%) |         |    1.79 MiB (1%) |         216 |
| `["parallel_histogram", "assoc", "basesize=8192"]`  |   3.590 ms (5%) |         |    1.42 MiB (1%) |         118 |
| `["parallel_histogram", "comm", "basesize=16384"]`  |  18.310 ms (5%) |         |    1.57 MiB (1%) |        2035 |
| `["parallel_histogram", "comm", "basesize=4096"]`   |  21.990 ms (5%) |         |    1.14 MiB (1%) |        3587 |
| `["parallel_histogram", "comm", "basesize=8192"]`   |  17.300 ms (5%) |         |    1.32 MiB (1%) |        3565 |
| `["parallel_histogram", "seq"]`                     |   5.714 ms (5%) |         |  364.16 KiB (1%) |          24 |
| `["partition_length_maximum", "rand", "foldl"]`     |  35.350 ms (5%) |         |                  |             |
| `["partition_length_maximum", "rand", "reduce"]`    |  17.686 ms (5%) |         |   736 bytes (1%) |          11 |
| `["splitby", "count", "foldl"]`                     |   2.376 ms (5%) |         |                  |             |
| `["splitby", "count", "man"]`                       |   1.769 ms (5%) |         |                  |             |
| `["splitby", "count", "reduce"]`                    |   1.092 ms (5%) |         |    1.06 KiB (1%) |          18 |
| `["sum", "random", "foldl"]`                        |  16.100 ms (5%) |         |                  |             |
| `["sum", "random", "reduce", "basesize=128"]`       |   8.191 ms (5%) |         |   73.98 KiB (1%) |        1098 |
| `["sum", "random", "reduce", "basesize=256"]`       |   8.083 ms (5%) |         |   36.70 KiB (1%) |         545 |
| `["sum", "random", "reduce", "basesize=512"]`       |   8.013 ms (5%) |         |   18.05 KiB (1%) |         268 |
| `["sum", "uniform", "foldl"]`                       |  15.654 ms (5%) |         |                  |             |
| `["sum", "uniform", "reduce", "basesize=128"]`      |   8.095 ms (5%) |         |   74.11 KiB (1%) |        1102 |
| `["sum", "uniform", "reduce", "basesize=256"]`      |   7.940 ms (5%) |         |   36.70 KiB (1%) |         545 |
| `["sum", "uniform", "reduce", "basesize=512"]`      |   7.832 ms (5%) |         |   18.03 KiB (1%) |         268 |
| `["sum", "valley", "foldl"]`                        |  16.106 ms (5%) |         |                  |             |
| `["sum", "valley", "reduce", "basesize=128"]`       |   8.333 ms (5%) |         |   74.08 KiB (1%) |        1101 |
| `["sum", "valley", "reduce", "basesize=256"]`       |   8.163 ms (5%) |         |   36.73 KiB (1%) |         546 |
| `["sum", "valley", "reduce", "basesize=512"]`       |   8.149 ms (5%) |         |   18.03 KiB (1%) |         268 |
| `["words", "nthreads=1"]`                           |  24.394 ms (5%) |         |   31.69 MiB (1%) |     1032613 |
| `["words", "nthreads=2"]`                           |  15.538 ms (5%) |         |   32.40 MiB (1%) |     1032697 |
| `["words", "nthreads=4"]`                           |  16.198 ms (5%) |         |   33.03 MiB (1%) |     1032832 |

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
  CPU: Intel(R) Xeon(R) Platinum 8272CL CPU @ 2.60GHz: 
              speed         user         nice          sys         idle          irq
       #1  2593 MHz       5412 s          1 s        259 s       4916 s          0 s
       #2  2593 MHz       5275 s          0 s        260 s       5108 s          0 s
       
  Memory: 6.784542083740234 GB (3831.65625 MB free)
  Uptime: 1067.75 sec
  Load Avg:  1.72  1.52  0.91
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-12.0.1 (ORCJIT, skylake-avx512)
```

---
# Baseline result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmark: 27 Feb 2022 - 1:34
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

| ID                                                  | time            | GC time | memory           | allocations |
|-----------------------------------------------------|----------------:|--------:|-----------------:|------------:|
| `["collect", "assoc", "basesize=1"]`                | 255.321 ms (5%) |         |   25.97 MiB (1%) |      306845 |
| `["collect", "assoc", "basesize=1024"]`             | 198.633 ms (5%) |         |    2.61 MiB (1%) |         456 |
| `["collect", "assoc", "basesize=32"]`               | 201.336 ms (5%) |         |    4.82 MiB (1%) |       11709 |
| `["collect", "seq"]`                                | 395.255 ms (5%) |         |  812.73 KiB (1%) |          11 |
| `["collect", "unordered", "basesize=1"]`            | 352.153 ms (5%) |         |   23.87 MiB (1%) |      411904 |
| `["collect", "unordered", "basesize=1024"]`         | 213.631 ms (5%) |         | 1002.70 KiB (1%) |        1081 |
| `["collect", "unordered", "basesize=32"]`           | 225.298 ms (5%) |         |    1.58 MiB (1%) |       14691 |
| `["findfirst", "n=1000", "foldl"]`                  | 625.923 ms (5%) |         |                  |             |
| `["findfirst", "n=1000", "reduce", "basesize=128"]` | 344.233 ms (5%) |         |  232.86 KiB (1%) |        3276 |
| `["findfirst", "n=1000", "reduce", "basesize=256"]` | 422.319 ms (5%) |         |  157.20 KiB (1%) |        2193 |
| `["findfirst", "n=1000", "reduce", "basesize=512"]` | 563.108 ms (5%) |         |  108.55 KiB (1%) |        1509 |
| `["findfirst", "n=400", "foldl"]`                   | 469.617 ms (5%) |         |                  |             |
| `["findfirst", "n=400", "reduce", "basesize=128"]`  | 248.630 ms (5%) |         |  382.80 KiB (1%) |        5465 |
| `["findfirst", "n=400", "reduce", "basesize=256"]`  | 248.581 ms (5%) |         |  200.86 KiB (1%) |        2873 |
| `["findfirst", "n=400", "reduce", "basesize=512"]`  | 353.708 ms (5%) |         |  148.23 KiB (1%) |        2113 |
| `["findfirst", "n=500", "foldl"]`                   |  81.209 ms (5%) |         |                  |             |
| `["findfirst", "n=500", "reduce", "basesize=128"]`  | 216.584 ms (5%) |         |  281.44 KiB (1%) |        3937 |
| `["findfirst", "n=500", "reduce", "basesize=256"]`  | 153.651 ms (5%) |         |  118.80 KiB (1%) |        1636 |
| `["findfirst", "n=500", "reduce", "basesize=512"]`  | 116.764 ms (5%) |         |   63.69 KiB (1%) |         866 |
| `["overhead", "default"]`                           |  75.801 μs (5%) |         |   32.70 KiB (1%) |         417 |
| `["overhead", "stoppable=false"]`                   |  76.401 μs (5%) |         |   32.75 KiB (1%) |         418 |
| `["overhead", "stoppable=true"]`                    |  84.201 μs (5%) |         |   44.25 KiB (1%) |         610 |
| `["parallel_histogram", "assoc", "basesize=16384"]` |   3.221 ms (5%) |         |  728.91 KiB (1%) |          57 |
| `["parallel_histogram", "assoc", "basesize=4096"]`  |   3.863 ms (5%) |         |    1.79 MiB (1%) |         215 |
| `["parallel_histogram", "assoc", "basesize=8192"]`  |   3.576 ms (5%) |         |    1.42 MiB (1%) |         117 |
| `["parallel_histogram", "comm", "basesize=16384"]`  |  17.158 ms (5%) |         |    1.58 MiB (1%) |        2421 |
| `["parallel_histogram", "comm", "basesize=4096"]`   |  24.284 ms (5%) |         |    1.24 MiB (1%) |        6831 |
| `["parallel_histogram", "comm", "basesize=8192"]`   |  22.625 ms (5%) |         |    1.31 MiB (1%) |        5667 |
| `["parallel_histogram", "seq"]`                     |   5.721 ms (5%) |         |  364.16 KiB (1%) |          24 |
| `["partition_length_maximum", "rand", "foldl"]`     |  35.364 ms (5%) |         |                  |             |
| `["partition_length_maximum", "rand", "reduce"]`    |  17.683 ms (5%) |         |   736 bytes (1%) |          11 |
| `["splitby", "count", "foldl"]`                     |   2.299 ms (5%) |         |                  |             |
| `["splitby", "count", "man"]`                       |   1.754 ms (5%) |         |                  |             |
| `["splitby", "count", "reduce"]`                    |   1.089 ms (5%) |         |    1.06 KiB (1%) |          18 |
| `["sum", "random", "foldl"]`                        |  16.160 ms (5%) |         |                  |             |
| `["sum", "random", "reduce", "basesize=128"]`       |   8.106 ms (5%) |         |   74.14 KiB (1%) |        1103 |
| `["sum", "random", "reduce", "basesize=256"]`       |   8.080 ms (5%) |         |   36.70 KiB (1%) |         545 |
| `["sum", "random", "reduce", "basesize=512"]`       |   8.005 ms (5%) |         |   18.02 KiB (1%) |         267 |
| `["sum", "uniform", "foldl"]`                       |  15.742 ms (5%) |         |                  |             |
| `["sum", "uniform", "reduce", "basesize=128"]`      |   7.968 ms (5%) |         |   74.11 KiB (1%) |        1102 |
| `["sum", "uniform", "reduce", "basesize=256"]`      |   7.866 ms (5%) |         |   36.70 KiB (1%) |         545 |
| `["sum", "uniform", "reduce", "basesize=512"]`      |   7.820 ms (5%) |         |   18.00 KiB (1%) |         267 |
| `["sum", "valley", "foldl"]`                        |  16.066 ms (5%) |         |                  |             |
| `["sum", "valley", "reduce", "basesize=128"]`       |   8.207 ms (5%) |         |   74.14 KiB (1%) |        1103 |
| `["sum", "valley", "reduce", "basesize=256"]`       |   8.152 ms (5%) |         |   36.73 KiB (1%) |         546 |
| `["sum", "valley", "reduce", "basesize=512"]`       |   8.109 ms (5%) |         |   18.03 KiB (1%) |         268 |
| `["words", "nthreads=1"]`                           |  24.289 ms (5%) |         |   31.87 MiB (1%) |     1038546 |
| `["words", "nthreads=2"]`                           |  15.597 ms (5%) |         |   32.22 MiB (1%) |     1038589 |
| `["words", "nthreads=4"]`                           |  15.612 ms (5%) |         |   33.12 MiB (1%) |     1038727 |

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
  CPU: Intel(R) Xeon(R) Platinum 8272CL CPU @ 2.60GHz: 
              speed         user         nice          sys         idle          irq
       #1  2593 MHz       7418 s          1 s        333 s       6005 s          0 s
       #2  2593 MHz       8070 s          0 s        342 s       5405 s          0 s
       
  Memory: 6.784542083740234 GB (3759.16796875 MB free)
  Uptime: 1385.53 sec
  Load Avg:  1.59  1.54  1.1
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
    Model name:                      Intel(R) Xeon(R) Platinum 8272CL CPU @ 2.60GHz
    Stepping:                        7
    CPU MHz:                         2593.906
    BogoMIPS:                        5187.81
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

