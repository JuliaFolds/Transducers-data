# Multi-thread benchmark result

* Pull request commit: [`124ecb12e7c18be51172be774afd4d798858d2ce`](https://github.com/JuliaFolds/Transducers.jl/commit/124ecb12e7c18be51172be774afd4d798858d2ce)
* Pull request: <https://github.com/JuliaFolds/Transducers.jl/pull/506> (Use Julia 1.7 for multi-thread benchmark)

# Judge result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmarks:
    - Target: 29 Jan 2022 - 04:15
    - Baseline: 29 Jan 2022 - 04:20
* Package commits:
    - Target: 7be515
    - Baseline: a0aefc
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
| `["findfirst", "n=1000", "reduce", "basesize=128"]` | 0.89 (5%) :white_check_mark: | 0.91 (1%) :white_check_mark: |
| `["findfirst", "n=1000", "reduce", "basesize=256"]` |                1.27 (5%) :x: |                1.13 (1%) :x: |
| `["findfirst", "n=1000", "reduce", "basesize=512"]` | 0.85 (5%) :white_check_mark: | 0.90 (1%) :white_check_mark: |
| `["findfirst", "n=400", "reduce", "basesize=128"]`  |                   1.00 (5%)  | 0.98 (1%) :white_check_mark: |
| `["findfirst", "n=400", "reduce", "basesize=512"]`  | 0.91 (5%) :white_check_mark: | 0.95 (1%) :white_check_mark: |
| `["findfirst", "n=500", "reduce", "basesize=128"]`  |                1.24 (5%) :x: |                1.19 (1%) :x: |
| `["findfirst", "n=500", "reduce", "basesize=256"]`  | 0.76 (5%) :white_check_mark: | 0.83 (1%) :white_check_mark: |
| `["findfirst", "n=500", "reduce", "basesize=512"]`  | 0.90 (5%) :white_check_mark: |                1.04 (1%) :x: |
| `["parallel_histogram", "comm", "basesize=16384"]`  | 0.93 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["parallel_histogram", "comm", "basesize=4096"]`   |                   1.03 (5%)  |                1.02 (1%) :x: |
| `["parallel_histogram", "comm", "basesize=8192"]`   |                   1.01 (5%)  | 0.99 (1%) :white_check_mark: |
| `["splitby", "count", "reduce"]`                    |                   1.03 (5%)  |                1.03 (1%) :x: |
| `["words", "nthreads=1"]`                           | 0.90 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["words", "nthreads=2"]`                           | 0.91 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["words", "nthreads=4"]`                           | 0.92 (5%) :white_check_mark: |                   1.00 (1%)  |

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
  CPU: Intel(R) Xeon(R) Platinum 8272CL CPU @ 2.60GHz: 
              speed         user         nice          sys         idle          irq
       #1  2593 MHz       5371 s          1 s        241 s       1541 s          0 s
       #2  2593 MHz       5260 s          1 s        212 s       1717 s          0 s
       
  Memory: 6.788978576660156 GB (3427.171875 MB free)
  Uptime: 723.61 sec
  Load Avg:  1.69  1.49  0.9
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-12.0.1 (ORCJIT, skylake-avx512)
```

### Baseline
```
Julia Version 1.7.1
Commit ac5cc99908 (2021-12-22 19:35 UTC)
Platform Info:
  OS: Linux (x86_64-pc-linux-gnu)
      Ubuntu 20.04.3 LTS
  uname: Linux 5.11.0-1027-azure #30~20.04.1-Ubuntu SMP Wed Jan 12 20:56:50 UTC 2022 x86_64 x86_64
  CPU: Intel(R) Xeon(R) Platinum 8272CL CPU @ 2.60GHz: 
              speed         user         nice          sys         idle          irq
       #1  2593 MHz       7830 s          1 s        280 s       2084 s          0 s
       #2  2593 MHz       7476 s          1 s        251 s       2507 s          0 s
       
  Memory: 6.788978576660156 GB (3417.91796875 MB free)
  Uptime: 1028.59 sec
  Load Avg:  1.66  1.55  1.09
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-12.0.1 (ORCJIT, skylake-avx512)
```

---
# Target result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmark: 29 Jan 2022 - 4:15
* Package commit: 7be515
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

| ID                                                  | time            | GC time | memory           | allocations |
|-----------------------------------------------------|----------------:|--------:|-----------------:|------------:|
| `["collect", "assoc", "basesize=1"]`                | 244.096 ms (5%) |         |   25.97 MiB (1%) |      306805 |
| `["collect", "assoc", "basesize=1024"]`             | 198.654 ms (5%) |         |    2.61 MiB (1%) |         456 |
| `["collect", "assoc", "basesize=32"]`               | 199.918 ms (5%) |         |    4.82 MiB (1%) |       11710 |
| `["collect", "seq"]`                                | 395.097 ms (5%) |         |  812.73 KiB (1%) |          11 |
| `["collect", "unordered", "basesize=1"]`            | 352.841 ms (5%) |         |   23.89 MiB (1%) |      412773 |
| `["collect", "unordered", "basesize=1024"]`         | 211.813 ms (5%) |         | 1001.92 KiB (1%) |        1063 |
| `["collect", "unordered", "basesize=32"]`           | 223.906 ms (5%) |         |    1.59 MiB (1%) |       14814 |
| `["findfirst", "n=1000", "foldl"]`                  | 630.167 ms (5%) |         |                  |             |
| `["findfirst", "n=1000", "reduce", "basesize=128"]` | 345.361 ms (5%) |         |  232.80 KiB (1%) |        3274 |
| `["findfirst", "n=1000", "reduce", "basesize=256"]` | 537.895 ms (5%) |         |  176.91 KiB (1%) |        2511 |
| `["findfirst", "n=1000", "reduce", "basesize=512"]` | 688.297 ms (5%) |         |  124.88 KiB (1%) |        1749 |
| `["findfirst", "n=400", "foldl"]`                   | 472.870 ms (5%) |         |                  |             |
| `["findfirst", "n=400", "reduce", "basesize=128"]`  | 245.247 ms (5%) |         |  376.06 KiB (1%) |        5366 |
| `["findfirst", "n=400", "reduce", "basesize=256"]`  | 248.918 ms (5%) |         |  201.23 KiB (1%) |        2885 |
| `["findfirst", "n=400", "reduce", "basesize=512"]`  | 346.871 ms (5%) |         |  145.38 KiB (1%) |        2064 |
| `["findfirst", "n=500", "foldl"]`                   |  82.000 ms (5%) |         |                  |             |
| `["findfirst", "n=500", "reduce", "basesize=128"]`  | 182.578 ms (5%) |         |  246.11 KiB (1%) |        3429 |
| `["findfirst", "n=500", "reduce", "basesize=256"]`  |  88.656 ms (5%) |         |   80.33 KiB (1%) |        1096 |
| `["findfirst", "n=500", "reduce", "basesize=512"]`  |  95.840 ms (5%) |         |   56.86 KiB (1%) |         756 |
| `["overhead", "default"]`                           |  75.501 μs (5%) |         |   32.70 KiB (1%) |         417 |
| `["overhead", "stoppable=false"]`                   |  76.000 μs (5%) |         |   32.72 KiB (1%) |         417 |
| `["overhead", "stoppable=true"]`                    |  85.189 μs (5%) |         |   44.25 KiB (1%) |         610 |
| `["parallel_histogram", "assoc", "basesize=16384"]` |   3.237 ms (5%) |         |  728.91 KiB (1%) |          57 |
| `["parallel_histogram", "assoc", "basesize=4096"]`  |   3.881 ms (5%) |         |    1.79 MiB (1%) |         216 |
| `["parallel_histogram", "assoc", "basesize=8192"]`  |   3.567 ms (5%) |         |    1.42 MiB (1%) |         118 |
| `["parallel_histogram", "comm", "basesize=16384"]`  |  17.063 ms (5%) |         |    1.57 MiB (1%) |        1952 |
| `["parallel_histogram", "comm", "basesize=4096"]`   |  24.856 ms (5%) |         |    1.23 MiB (1%) |        6331 |
| `["parallel_histogram", "comm", "basesize=8192"]`   |  22.896 ms (5%) |         |    1.26 MiB (1%) |        5292 |
| `["parallel_histogram", "seq"]`                     |   5.777 ms (5%) |         |  364.16 KiB (1%) |          24 |
| `["partition_length_maximum", "rand", "foldl"]`     |  35.317 ms (5%) |         |                  |             |
| `["partition_length_maximum", "rand", "reduce"]`    |  17.622 ms (5%) |         |   736 bytes (1%) |          11 |
| `["splitby", "count", "foldl"]`                     |   2.275 ms (5%) |         |                  |             |
| `["splitby", "count", "man"]`                       |   1.418 ms (5%) |         |                  |             |
| `["splitby", "count", "reduce"]`                    |   1.120 ms (5%) |         |    1.09 KiB (1%) |          19 |
| `["sum", "random", "foldl"]`                        |  16.151 ms (5%) |         |                  |             |
| `["sum", "random", "reduce", "basesize=128"]`       |   8.135 ms (5%) |         |   74.20 KiB (1%) |        1105 |
| `["sum", "random", "reduce", "basesize=256"]`       |   8.031 ms (5%) |         |   36.73 KiB (1%) |         546 |
| `["sum", "random", "reduce", "basesize=512"]`       |   7.960 ms (5%) |         |   18.08 KiB (1%) |         269 |
| `["sum", "uniform", "foldl"]`                       |  15.701 ms (5%) |         |                  |             |
| `["sum", "uniform", "reduce", "basesize=128"]`      |   8.013 ms (5%) |         |   74.20 KiB (1%) |        1105 |
| `["sum", "uniform", "reduce", "basesize=256"]`      |   7.896 ms (5%) |         |   36.73 KiB (1%) |         546 |
| `["sum", "uniform", "reduce", "basesize=512"]`      |   7.834 ms (5%) |         |   18.03 KiB (1%) |         268 |
| `["sum", "valley", "foldl"]`                        |  16.145 ms (5%) |         |                  |             |
| `["sum", "valley", "reduce", "basesize=128"]`       |   8.238 ms (5%) |         |   74.11 KiB (1%) |        1102 |
| `["sum", "valley", "reduce", "basesize=256"]`       |   8.141 ms (5%) |         |   36.77 KiB (1%) |         547 |
| `["sum", "valley", "reduce", "basesize=512"]`       |   8.113 ms (5%) |         |   18.06 KiB (1%) |         269 |
| `["words", "nthreads=1"]`                           |  23.276 ms (5%) |         |   31.57 MiB (1%) |     1028651 |
| `["words", "nthreads=2"]`                           |  14.967 ms (5%) |         |   32.28 MiB (1%) |     1028730 |
| `["words", "nthreads=4"]`                           |  14.783 ms (5%) |         |   32.73 MiB (1%) |     1028817 |

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
  CPU: Intel(R) Xeon(R) Platinum 8272CL CPU @ 2.60GHz: 
              speed         user         nice          sys         idle          irq
       #1  2593 MHz       5371 s          1 s        241 s       1541 s          0 s
       #2  2593 MHz       5260 s          1 s        212 s       1717 s          0 s
       
  Memory: 6.788978576660156 GB (3427.171875 MB free)
  Uptime: 723.61 sec
  Load Avg:  1.69  1.49  0.9
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-12.0.1 (ORCJIT, skylake-avx512)
```

---
# Baseline result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmark: 29 Jan 2022 - 4:20
* Package commit: a0aefc
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

| ID                                                  | time            | GC time | memory           | allocations |
|-----------------------------------------------------|----------------:|--------:|-----------------:|------------:|
| `["collect", "assoc", "basesize=1"]`                | 249.426 ms (5%) |         |   25.97 MiB (1%) |      306854 |
| `["collect", "assoc", "basesize=1024"]`             | 198.891 ms (5%) |         |    2.61 MiB (1%) |         456 |
| `["collect", "assoc", "basesize=32"]`               | 201.014 ms (5%) |         |    4.82 MiB (1%) |       11707 |
| `["collect", "seq"]`                                | 395.338 ms (5%) |         |  812.73 KiB (1%) |          11 |
| `["collect", "unordered", "basesize=1"]`            | 359.289 ms (5%) |         |   23.91 MiB (1%) |      413264 |
| `["collect", "unordered", "basesize=1024"]`         | 212.752 ms (5%) |         | 1002.70 KiB (1%) |         951 |
| `["collect", "unordered", "basesize=32"]`           | 226.971 ms (5%) |         |    1.59 MiB (1%) |       14842 |
| `["findfirst", "n=1000", "foldl"]`                  | 629.577 ms (5%) |         |                  |             |
| `["findfirst", "n=1000", "reduce", "basesize=128"]` | 386.144 ms (5%) |         |  255.88 KiB (1%) |        3601 |
| `["findfirst", "n=1000", "reduce", "basesize=256"]` | 424.624 ms (5%) |         |  157.20 KiB (1%) |        2193 |
| `["findfirst", "n=1000", "reduce", "basesize=512"]` | 807.380 ms (5%) |         |  138.94 KiB (1%) |        1966 |
| `["findfirst", "n=400", "foldl"]`                   | 472.370 ms (5%) |         |                  |             |
| `["findfirst", "n=400", "reduce", "basesize=128"]`  | 245.010 ms (5%) |         |  383.12 KiB (1%) |        5454 |
| `["findfirst", "n=400", "reduce", "basesize=256"]`  | 247.971 ms (5%) |         |  200.86 KiB (1%) |        2873 |
| `["findfirst", "n=400", "reduce", "basesize=512"]`  | 381.426 ms (5%) |         |  153.08 KiB (1%) |        2192 |
| `["findfirst", "n=500", "foldl"]`                   |  81.906 ms (5%) |         |                  |             |
| `["findfirst", "n=500", "reduce", "basesize=128"]`  | 147.257 ms (5%) |         |  207.48 KiB (1%) |        2870 |
| `["findfirst", "n=500", "reduce", "basesize=256"]`  | 116.025 ms (5%) |         |   96.73 KiB (1%) |        1334 |
| `["findfirst", "n=500", "reduce", "basesize=512"]`  | 105.958 ms (5%) |         |   54.48 KiB (1%) |         748 |
| `["overhead", "default"]`                           |  76.800 μs (5%) |         |   32.70 KiB (1%) |         417 |
| `["overhead", "stoppable=false"]`                   |  76.400 μs (5%) |         |   32.75 KiB (1%) |         418 |
| `["overhead", "stoppable=true"]`                    |  86.201 μs (5%) |         |   44.25 KiB (1%) |         610 |
| `["parallel_histogram", "assoc", "basesize=16384"]` |   3.235 ms (5%) |         |  728.91 KiB (1%) |          57 |
| `["parallel_histogram", "assoc", "basesize=4096"]`  |   3.903 ms (5%) |         |    1.79 MiB (1%) |         216 |
| `["parallel_histogram", "assoc", "basesize=8192"]`  |   3.571 ms (5%) |         |    1.42 MiB (1%) |         117 |
| `["parallel_histogram", "comm", "basesize=16384"]`  |  18.326 ms (5%) |         |    1.57 MiB (1%) |        2111 |
| `["parallel_histogram", "comm", "basesize=4096"]`   |  24.134 ms (5%) |         |    1.21 MiB (1%) |        5699 |
| `["parallel_histogram", "comm", "basesize=8192"]`   |  22.698 ms (5%) |         |    1.28 MiB (1%) |        5542 |
| `["parallel_histogram", "seq"]`                     |   5.792 ms (5%) |         |  364.16 KiB (1%) |          24 |
| `["partition_length_maximum", "rand", "foldl"]`     |  35.241 ms (5%) |         |                  |             |
| `["partition_length_maximum", "rand", "reduce"]`    |  17.602 ms (5%) |         |   736 bytes (1%) |          11 |
| `["splitby", "count", "foldl"]`                     |   2.254 ms (5%) |         |                  |             |
| `["splitby", "count", "man"]`                       |   1.420 ms (5%) |         |                  |             |
| `["splitby", "count", "reduce"]`                    |   1.091 ms (5%) |         |    1.06 KiB (1%) |          18 |
| `["sum", "random", "foldl"]`                        |  16.159 ms (5%) |         |                  |             |
| `["sum", "random", "reduce", "basesize=128"]`       |   8.126 ms (5%) |         |   74.11 KiB (1%) |        1102 |
| `["sum", "random", "reduce", "basesize=256"]`       |   8.048 ms (5%) |         |   36.73 KiB (1%) |         546 |
| `["sum", "random", "reduce", "basesize=512"]`       |   7.984 ms (5%) |         |   18.08 KiB (1%) |         269 |
| `["sum", "uniform", "foldl"]`                       |  15.730 ms (5%) |         |                  |             |
| `["sum", "uniform", "reduce", "basesize=128"]`      |   7.941 ms (5%) |         |   74.08 KiB (1%) |        1101 |
| `["sum", "uniform", "reduce", "basesize=256"]`      |   7.866 ms (5%) |         |   36.67 KiB (1%) |         544 |
| `["sum", "uniform", "reduce", "basesize=512"]`      |   7.805 ms (5%) |         |   18.03 KiB (1%) |         268 |
| `["sum", "valley", "foldl"]`                        |  16.125 ms (5%) |         |                  |             |
| `["sum", "valley", "reduce", "basesize=128"]`       |   8.279 ms (5%) |         |   74.08 KiB (1%) |        1101 |
| `["sum", "valley", "reduce", "basesize=256"]`       |   8.174 ms (5%) |         |   36.70 KiB (1%) |         545 |
| `["sum", "valley", "reduce", "basesize=512"]`       |   8.142 ms (5%) |         |   18.03 KiB (1%) |         268 |
| `["words", "nthreads=1"]`                           |  25.971 ms (5%) |         |   31.45 MiB (1%) |     1024321 |
| `["words", "nthreads=2"]`                           |  16.437 ms (5%) |         |   32.16 MiB (1%) |     1024410 |
| `["words", "nthreads=4"]`                           |  16.117 ms (5%) |         |   32.61 MiB (1%) |     1024517 |

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
  CPU: Intel(R) Xeon(R) Platinum 8272CL CPU @ 2.60GHz: 
              speed         user         nice          sys         idle          irq
       #1  2593 MHz       7830 s          1 s        280 s       2084 s          0 s
       #2  2593 MHz       7476 s          1 s        251 s       2507 s          0 s
       
  Memory: 6.788978576660156 GB (3417.91796875 MB free)
  Uptime: 1028.59 sec
  Load Avg:  1.66  1.55  1.09
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
    CPU MHz:                         2593.905
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

