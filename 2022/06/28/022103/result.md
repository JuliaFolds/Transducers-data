# Multi-thread benchmark result

* Pull request commit: [`10546ef7f53d4d6a2e455da8e7e36c45791ea424`](https://github.com/JuliaFolds/Transducers.jl/commit/10546ef7f53d4d6a2e455da8e7e36c45791ea424)
* Pull request: <https://github.com/JuliaFolds/Transducers.jl/pull/243> (Update */Manifest.toml)

# Judge result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmarks:
    - Target: 28 Jun 2022 - 02:15
    - Baseline: 28 Jun 2022 - 02:20
* Package commits:
    - Target: 30d1c8
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
| `["collect", "unordered", "basesize=1"]`            |                   1.01 (5%)  | 0.99 (1%) :white_check_mark: |
| `["collect", "unordered", "basesize=32"]`           |                1.06 (5%) :x: |                   1.00 (1%)  |
| `["findfirst", "n=1000", "reduce", "basesize=128"]` |                   1.02 (5%)  |                1.05 (1%) :x: |
| `["findfirst", "n=1000", "reduce", "basesize=256"]` | 0.73 (5%) :white_check_mark: | 0.81 (1%) :white_check_mark: |
| `["findfirst", "n=1000", "reduce", "basesize=512"]` | 0.71 (5%) :white_check_mark: | 0.75 (1%) :white_check_mark: |
| `["findfirst", "n=400", "reduce", "basesize=128"]`  | 0.93 (5%) :white_check_mark: | 0.93 (1%) :white_check_mark: |
| `["findfirst", "n=400", "reduce", "basesize=512"]`  |                   0.96 (5%)  |                1.02 (1%) :x: |
| `["findfirst", "n=500", "reduce", "basesize=128"]`  |                1.12 (5%) :x: |                1.11 (1%) :x: |
| `["findfirst", "n=500", "reduce", "basesize=256"]`  |                3.69 (5%) :x: |                2.39 (1%) :x: |
| `["findfirst", "n=500", "reduce", "basesize=512"]`  | 0.91 (5%) :white_check_mark: | 0.89 (1%) :white_check_mark: |
| `["parallel_histogram", "assoc", "basesize=4096"]`  |                   1.01 (5%)  |                1.15 (1%) :x: |
| `["parallel_histogram", "comm", "basesize=16384"]`  |                   0.95 (5%)  | 0.97 (1%) :white_check_mark: |
| `["parallel_histogram", "comm", "basesize=4096"]`   |                   1.02 (5%)  |                1.01 (1%) :x: |
| `["parallel_histogram", "comm", "basesize=8192"]`   |                   0.96 (5%)  |                1.07 (1%) :x: |
| `["splitby", "count", "man"]`                       |                1.23 (5%) :x: |                   1.00 (1%)  |

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
  uname: Linux 5.13.0-1031-azure #37~20.04.1-Ubuntu SMP Mon Jun 13 22:51:01 UTC 2022 x86_64 x86_64
  CPU: Intel(R) Xeon(R) Platinum 8272CL CPU @ 2.60GHz: 
              speed         user         nice          sys         idle          irq
       #1  2593 MHz       4818 s          1 s        256 s       2061 s          0 s
       #2  2593 MHz       5382 s          1 s        295 s       1474 s          0 s
       
  Memory: 6.783607482910156 GB (3750.49609375 MB free)
  Uptime: 719.38 sec
  Load Avg:  1.67  1.49  0.89
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
      Ubuntu 20.04.4 LTS
  uname: Linux 5.13.0-1031-azure #37~20.04.1-Ubuntu SMP Mon Jun 13 22:51:01 UTC 2022 x86_64 x86_64
  CPU: Intel(R) Xeon(R) Platinum 8272CL CPU @ 2.60GHz: 
              speed         user         nice          sys         idle          irq
       #1  2593 MHz       6689 s          1 s        328 s       3196 s          0 s
       #2  2593 MHz       8245 s          1 s        354 s       1631 s          0 s
       
  Memory: 6.783607482910156 GB (3742.828125 MB free)
  Uptime: 1027.7 sec
  Load Avg:  1.73  1.65  1.13
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-12.0.1 (ORCJIT, skylake-avx512)
```

---
# Target result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmark: 28 Jun 2022 - 2:15
* Package commit: 30d1c8
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

| ID                                                  | time            | GC time | memory           | allocations |
|-----------------------------------------------------|----------------:|--------:|-----------------:|------------:|
| `["collect", "assoc", "basesize=1"]`                | 243.125 ms (5%) |         |   25.97 MiB (1%) |      306772 |
| `["collect", "assoc", "basesize=1024"]`             | 198.282 ms (5%) |         |    2.61 MiB (1%) |         456 |
| `["collect", "assoc", "basesize=32"]`               | 200.821 ms (5%) |         |    4.82 MiB (1%) |       11707 |
| `["collect", "seq"]`                                | 394.990 ms (5%) |         |  812.73 KiB (1%) |          11 |
| `["collect", "unordered", "basesize=1"]`            | 355.974 ms (5%) |         |   23.57 MiB (1%) |      402071 |
| `["collect", "unordered", "basesize=1024"]`         | 213.938 ms (5%) |         | 1000.27 KiB (1%) |        1023 |
| `["collect", "unordered", "basesize=32"]`           | 238.439 ms (5%) |         |    1.58 MiB (1%) |       14600 |
| `["findfirst", "n=1000", "foldl"]`                  | 625.893 ms (5%) |         |                  |             |
| `["findfirst", "n=1000", "reduce", "basesize=128"]` | 352.249 ms (5%) |         |  244.89 KiB (1%) |        3431 |
| `["findfirst", "n=1000", "reduce", "basesize=256"]` | 428.309 ms (5%) |         |  156.56 KiB (1%) |        2189 |
| `["findfirst", "n=1000", "reduce", "basesize=512"]` | 531.603 ms (5%) |         |   95.77 KiB (1%) |        1353 |
| `["findfirst", "n=400", "foldl"]`                   | 469.735 ms (5%) |         |                  |             |
| `["findfirst", "n=400", "reduce", "basesize=128"]`  | 245.147 ms (5%) |         |  378.55 KiB (1%) |        5402 |
| `["findfirst", "n=400", "reduce", "basesize=256"]`  | 247.756 ms (5%) |         |  200.95 KiB (1%) |        2876 |
| `["findfirst", "n=400", "reduce", "basesize=512"]`  | 322.499 ms (5%) |         |  139.20 KiB (1%) |        1977 |
| `["findfirst", "n=500", "foldl"]`                   |  81.453 ms (5%) |         |                  |             |
| `["findfirst", "n=500", "reduce", "basesize=128"]`  | 148.825 ms (5%) |         |  217.59 KiB (1%) |        3011 |
| `["findfirst", "n=500", "reduce", "basesize=256"]`  | 242.737 ms (5%) |         |  167.88 KiB (1%) |        2371 |
| `["findfirst", "n=500", "reduce", "basesize=512"]`  | 106.897 ms (5%) |         |   56.89 KiB (1%) |         780 |
| `["overhead", "default"]`                           |  74.001 μs (5%) |         |   32.73 KiB (1%) |         418 |
| `["overhead", "stoppable=false"]`                   |  74.101 μs (5%) |         |   32.75 KiB (1%) |         418 |
| `["overhead", "stoppable=true"]`                    |  84.301 μs (5%) |         |   44.25 KiB (1%) |         610 |
| `["parallel_histogram", "assoc", "basesize=16384"]` |   3.206 ms (5%) |         |  728.91 KiB (1%) |          57 |
| `["parallel_histogram", "assoc", "basesize=4096"]`  |   3.918 ms (5%) |         |    2.05 MiB (1%) |         222 |
| `["parallel_histogram", "assoc", "basesize=8192"]`  |   3.537 ms (5%) |         |    1.42 MiB (1%) |         117 |
| `["parallel_histogram", "comm", "basesize=16384"]`  |  16.803 ms (5%) |         |    1.55 MiB (1%) |        1310 |
| `["parallel_histogram", "comm", "basesize=4096"]`   |  25.595 ms (5%) |         |    1.27 MiB (1%) |        7889 |
| `["parallel_histogram", "comm", "basesize=8192"]`   |  22.053 ms (5%) |         |    1.33 MiB (1%) |        5738 |
| `["parallel_histogram", "seq"]`                     |   5.722 ms (5%) |         |  364.16 KiB (1%) |          24 |
| `["partition_length_maximum", "rand", "foldl"]`     |  35.232 ms (5%) |         |                  |             |
| `["partition_length_maximum", "rand", "reduce"]`    |  17.628 ms (5%) |         |   736 bytes (1%) |          11 |
| `["splitby", "count", "foldl"]`                     |   2.291 ms (5%) |         |                  |             |
| `["splitby", "count", "man"]`                       |   1.752 ms (5%) |         |                  |             |
| `["splitby", "count", "reduce"]`                    |   1.146 ms (5%) |         |    1.06 KiB (1%) |          18 |
| `["sum", "random", "foldl"]`                        |  16.144 ms (5%) |         |                  |             |
| `["sum", "random", "reduce", "basesize=128"]`       |   8.176 ms (5%) |         |   74.20 KiB (1%) |        1105 |
| `["sum", "random", "reduce", "basesize=256"]`       |   8.064 ms (5%) |         |   36.80 KiB (1%) |         548 |
| `["sum", "random", "reduce", "basesize=512"]`       |   7.987 ms (5%) |         |   18.11 KiB (1%) |         270 |
| `["sum", "uniform", "foldl"]`                       |  15.753 ms (5%) |         |                  |             |
| `["sum", "uniform", "reduce", "basesize=128"]`      |   7.983 ms (5%) |         |   74.17 KiB (1%) |        1104 |
| `["sum", "uniform", "reduce", "basesize=256"]`      |   7.878 ms (5%) |         |   36.70 KiB (1%) |         545 |
| `["sum", "uniform", "reduce", "basesize=512"]`      |   7.823 ms (5%) |         |   18.03 KiB (1%) |         268 |
| `["sum", "valley", "foldl"]`                        |  16.068 ms (5%) |         |                  |             |
| `["sum", "valley", "reduce", "basesize=128"]`       |   8.233 ms (5%) |         |   74.02 KiB (1%) |        1099 |
| `["sum", "valley", "reduce", "basesize=256"]`       |   8.132 ms (5%) |         |   36.73 KiB (1%) |         546 |
| `["sum", "valley", "reduce", "basesize=512"]`       |   8.086 ms (5%) |         |   18.03 KiB (1%) |         268 |
| `["words", "nthreads=1"]`                           |  23.102 ms (5%) |         |   31.65 MiB (1%) |     1031307 |
| `["words", "nthreads=2"]`                           |  14.362 ms (5%) |         |   32.37 MiB (1%) |     1031394 |
| `["words", "nthreads=4"]`                           |  14.878 ms (5%) |         |   33.00 MiB (1%) |     1031529 |

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
  uname: Linux 5.13.0-1031-azure #37~20.04.1-Ubuntu SMP Mon Jun 13 22:51:01 UTC 2022 x86_64 x86_64
  CPU: Intel(R) Xeon(R) Platinum 8272CL CPU @ 2.60GHz: 
              speed         user         nice          sys         idle          irq
       #1  2593 MHz       4818 s          1 s        256 s       2061 s          0 s
       #2  2593 MHz       5382 s          1 s        295 s       1474 s          0 s
       
  Memory: 6.783607482910156 GB (3750.49609375 MB free)
  Uptime: 719.38 sec
  Load Avg:  1.67  1.49  0.89
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-12.0.1 (ORCJIT, skylake-avx512)
```

---
# Baseline result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmark: 28 Jun 2022 - 2:20
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

| ID                                                  | time            | GC time | memory           | allocations |
|-----------------------------------------------------|----------------:|--------:|-----------------:|------------:|
| `["collect", "assoc", "basesize=1"]`                | 246.195 ms (5%) |         |   25.97 MiB (1%) |      306733 |
| `["collect", "assoc", "basesize=1024"]`             | 198.899 ms (5%) |         |    2.61 MiB (1%) |         456 |
| `["collect", "assoc", "basesize=32"]`               | 200.858 ms (5%) |         |    4.82 MiB (1%) |       11703 |
| `["collect", "seq"]`                                | 395.308 ms (5%) |         |  812.73 KiB (1%) |          11 |
| `["collect", "unordered", "basesize=1"]`            | 351.775 ms (5%) |         |   23.85 MiB (1%) |      411444 |
| `["collect", "unordered", "basesize=1024"]`         | 212.401 ms (5%) |         | 1005.64 KiB (1%) |         930 |
| `["collect", "unordered", "basesize=32"]`           | 224.312 ms (5%) |         |    1.58 MiB (1%) |       14709 |
| `["findfirst", "n=1000", "foldl"]`                  | 629.061 ms (5%) |         |                  |             |
| `["findfirst", "n=1000", "reduce", "basesize=128"]` | 344.934 ms (5%) |         |  232.86 KiB (1%) |        3276 |
| `["findfirst", "n=1000", "reduce", "basesize=256"]` | 585.583 ms (5%) |         |  193.91 KiB (1%) |        2748 |
| `["findfirst", "n=1000", "reduce", "basesize=512"]` | 749.537 ms (5%) |         |  127.72 KiB (1%) |        1810 |
| `["findfirst", "n=400", "foldl"]`                   | 471.994 ms (5%) |         |                  |             |
| `["findfirst", "n=400", "reduce", "basesize=128"]`  | 264.516 ms (5%) |         |  409.06 KiB (1%) |        5827 |
| `["findfirst", "n=400", "reduce", "basesize=256"]`  | 248.149 ms (5%) |         |  200.98 KiB (1%) |        2877 |
| `["findfirst", "n=400", "reduce", "basesize=512"]`  | 334.491 ms (5%) |         |  136.30 KiB (1%) |        1952 |
| `["findfirst", "n=500", "foldl"]`                   |  81.846 ms (5%) |         |                  |             |
| `["findfirst", "n=500", "reduce", "basesize=128"]`  | 133.350 ms (5%) |         |  196.48 KiB (1%) |        2699 |
| `["findfirst", "n=500", "reduce", "basesize=256"]`  |  65.860 ms (5%) |         |   70.33 KiB (1%) |         948 |
| `["findfirst", "n=500", "reduce", "basesize=512"]`  | 117.097 ms (5%) |         |   63.66 KiB (1%) |         865 |
| `["overhead", "default"]`                           |  75.200 μs (5%) |         |   32.70 KiB (1%) |         417 |
| `["overhead", "stoppable=false"]`                   |  74.700 μs (5%) |         |   32.75 KiB (1%) |         418 |
| `["overhead", "stoppable=true"]`                    |  83.900 μs (5%) |         |   44.25 KiB (1%) |         610 |
| `["parallel_histogram", "assoc", "basesize=16384"]` |   3.223 ms (5%) |         |  728.91 KiB (1%) |          57 |
| `["parallel_histogram", "assoc", "basesize=4096"]`  |   3.866 ms (5%) |         |    1.79 MiB (1%) |         216 |
| `["parallel_histogram", "assoc", "basesize=8192"]`  |   3.553 ms (5%) |         |    1.42 MiB (1%) |         117 |
| `["parallel_histogram", "comm", "basesize=16384"]`  |  17.617 ms (5%) |         |    1.59 MiB (1%) |        2901 |
| `["parallel_histogram", "comm", "basesize=4096"]`   |  25.124 ms (5%) |         |    1.26 MiB (1%) |        7373 |
| `["parallel_histogram", "comm", "basesize=8192"]`   |  22.937 ms (5%) |         |    1.24 MiB (1%) |        6187 |
| `["parallel_histogram", "seq"]`                     |   5.761 ms (5%) |         |  364.16 KiB (1%) |          24 |
| `["partition_length_maximum", "rand", "foldl"]`     |  35.156 ms (5%) |         |                  |             |
| `["partition_length_maximum", "rand", "reduce"]`    |  17.604 ms (5%) |         |   736 bytes (1%) |          11 |
| `["splitby", "count", "foldl"]`                     |   2.223 ms (5%) |         |                  |             |
| `["splitby", "count", "man"]`                       |   1.422 ms (5%) |         |                  |             |
| `["splitby", "count", "reduce"]`                    |   1.149 ms (5%) |         |    1.06 KiB (1%) |          19 |
| `["sum", "random", "foldl"]`                        |  16.221 ms (5%) |         |                  |             |
| `["sum", "random", "reduce", "basesize=128"]`       |   8.128 ms (5%) |         |   74.11 KiB (1%) |        1102 |
| `["sum", "random", "reduce", "basesize=256"]`       |   8.085 ms (5%) |         |   36.80 KiB (1%) |         548 |
| `["sum", "random", "reduce", "basesize=512"]`       |   8.024 ms (5%) |         |   18.11 KiB (1%) |         270 |
| `["sum", "uniform", "foldl"]`                       |  15.729 ms (5%) |         |                  |             |
| `["sum", "uniform", "reduce", "basesize=128"]`      |   7.937 ms (5%) |         |   74.23 KiB (1%) |        1106 |
| `["sum", "uniform", "reduce", "basesize=256"]`      |   7.869 ms (5%) |         |   36.77 KiB (1%) |         547 |
| `["sum", "uniform", "reduce", "basesize=512"]`      |   7.849 ms (5%) |         |   18.06 KiB (1%) |         269 |
| `["sum", "valley", "foldl"]`                        |  16.134 ms (5%) |         |                  |             |
| `["sum", "valley", "reduce", "basesize=128"]`       |   8.233 ms (5%) |         |   74.14 KiB (1%) |        1103 |
| `["sum", "valley", "reduce", "basesize=256"]`       |   8.170 ms (5%) |         |   36.77 KiB (1%) |         547 |
| `["sum", "valley", "reduce", "basesize=512"]`       |   8.143 ms (5%) |         |   18.06 KiB (1%) |         269 |
| `["words", "nthreads=1"]`                           |  24.107 ms (5%) |         |   31.80 MiB (1%) |     1036337 |
| `["words", "nthreads=2"]`                           |  14.607 ms (5%) |         |   32.51 MiB (1%) |     1036410 |
| `["words", "nthreads=4"]`                           |  14.996 ms (5%) |         |   33.14 MiB (1%) |     1036555 |

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
  uname: Linux 5.13.0-1031-azure #37~20.04.1-Ubuntu SMP Mon Jun 13 22:51:01 UTC 2022 x86_64 x86_64
  CPU: Intel(R) Xeon(R) Platinum 8272CL CPU @ 2.60GHz: 
              speed         user         nice          sys         idle          irq
       #1  2593 MHz       6689 s          1 s        328 s       3196 s          0 s
       #2  2593 MHz       8245 s          1 s        354 s       1631 s          0 s
       
  Memory: 6.783607482910156 GB (3742.828125 MB free)
  Uptime: 1027.7 sec
  Load Avg:  1.73  1.65  1.13
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
    Vulnerability Mmio stale data:   Vulnerable: Clear CPU buffers attempted, no microcode; SMT Host state unknown
    Vulnerability Spec store bypass: Vulnerable
    Vulnerability Spectre v1:        Mitigation; usercopy/swapgs barriers and __user pointer sanitization
    Vulnerability Spectre v2:        Mitigation; Retpolines, STIBP disabled, RSB filling
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

