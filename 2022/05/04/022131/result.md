# Multi-thread benchmark result

* Pull request commit: [`7073e6a1cd654354ef43000668f062ed13d7465c`](https://github.com/JuliaFolds/Transducers.jl/commit/7073e6a1cd654354ef43000668f062ed13d7465c)
* Pull request: <https://github.com/JuliaFolds/Transducers.jl/pull/243> (Update */Manifest.toml)

# Judge result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmarks:
    - Target: 4 May 2022 - 02:16
    - Baseline: 4 May 2022 - 02:21
* Package commits:
    - Target: 7ee1df
    - Baseline: 6125fe
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
| `["collect", "assoc", "basesize=1"]`                | 0.94 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["collect", "assoc", "basesize=1024"]`             | 0.94 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["collect", "assoc", "basesize=32"]`               | 0.94 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["collect", "seq"]`                                | 0.88 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["collect", "unordered", "basesize=1"]`            | 0.94 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["collect", "unordered", "basesize=1024"]`         | 0.94 (5%) :white_check_mark: |                1.03 (1%) :x: |
| `["collect", "unordered", "basesize=32"]`           | 0.93 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["findfirst", "n=1000", "reduce", "basesize=128"]` |                1.08 (5%) :x: |                   1.00 (1%)  |
| `["findfirst", "n=1000", "reduce", "basesize=256"]` |                1.23 (5%) :x: |                1.18 (1%) :x: |
| `["findfirst", "n=1000", "reduce", "basesize=512"]` | 0.94 (5%) :white_check_mark: | 0.84 (1%) :white_check_mark: |
| `["findfirst", "n=400", "reduce", "basesize=128"]`  |                1.06 (5%) :x: |                1.02 (1%) :x: |
| `["findfirst", "n=400", "reduce", "basesize=256"]`  |                1.09 (5%) :x: |                1.02 (1%) :x: |
| `["findfirst", "n=400", "reduce", "basesize=512"]`  |                   1.04 (5%)  |                1.05 (1%) :x: |
| `["findfirst", "n=500", "reduce", "basesize=128"]`  |                1.64 (5%) :x: |                1.41 (1%) :x: |
| `["findfirst", "n=500", "reduce", "basesize=256"]`  | 0.91 (5%) :white_check_mark: | 0.88 (1%) :white_check_mark: |
| `["findfirst", "n=500", "reduce", "basesize=512"]`  |                   0.96 (5%)  |                1.09 (1%) :x: |
| `["overhead", "stoppable=true"]`                    | 0.93 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["parallel_histogram", "comm", "basesize=8192"]`   |                   1.02 (5%)  | 0.98 (1%) :white_check_mark: |
| `["partition_length_maximum", "rand", "foldl"]`     |                1.14 (5%) :x: |                   1.00 (1%)  |
| `["splitby", "count", "foldl"]`                     | 0.94 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["splitby", "count", "man"]`                       | 0.70 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["splitby", "count", "reduce"]`                    |                   1.00 (5%)  |                1.03 (1%) :x: |
| `["sum", "random", "reduce", "basesize=128"]`       |                1.08 (5%) :x: |                   1.00 (1%)  |
| `["sum", "random", "reduce", "basesize=256"]`       |                1.07 (5%) :x: |                   1.00 (1%)  |
| `["sum", "random", "reduce", "basesize=512"]`       |                1.07 (5%) :x: |                   1.00 (1%)  |
| `["sum", "uniform", "reduce", "basesize=128"]`      |                1.07 (5%) :x: |                   1.00 (1%)  |
| `["sum", "uniform", "reduce", "basesize=256"]`      |                1.07 (5%) :x: |                   1.00 (1%)  |
| `["sum", "uniform", "reduce", "basesize=512"]`      |                1.08 (5%) :x: |                   1.00 (1%)  |
| `["words", "nthreads=2"]`                           |                1.07 (5%) :x: |                1.02 (1%) :x: |
| `["words", "nthreads=4"]`                           |                1.12 (5%) :x: |                   1.01 (1%)  |

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
      Ubuntu 20.04.4 LTS
  uname: Linux 5.13.0-1022-azure #26~20.04.1-Ubuntu SMP Thu Apr 7 19:42:45 UTC 2022 x86_64 x86_64
  CPU: Intel(R) Xeon(R) Platinum 8272CL CPU @ 2.60GHz: 
              speed         user         nice          sys         idle          irq
       #1  2593 MHz       5416 s          1 s        204 s       2747 s          0 s
       #2  2593 MHz       4771 s          1 s        206 s       3418 s          0 s
       
  Memory: 6.783607482910156 GB (3829.55859375 MB free)
  Uptime: 844.36 sec
  Load Avg:  1.71  1.49  0.88
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
      Ubuntu 20.04.4 LTS
  uname: Linux 5.13.0-1022-azure #26~20.04.1-Ubuntu SMP Thu Apr 7 19:42:45 UTC 2022 x86_64 x86_64
  CPU: Intel(R) Xeon(R) Platinum 8272CL CPU @ 2.60GHz: 
              speed         user         nice          sys         idle          irq
       #1  2593 MHz       7910 s          1 s        281 s       3269 s          0 s
       #2  2593 MHz       7002 s          1 s        277 s       4206 s          0 s
       
  Memory: 6.783607482910156 GB (3786.20703125 MB free)
  Uptime: 1153.96 sec
  Load Avg:  1.68  1.58  1.1
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-12.0.1 (ORCJIT, skylake-avx512)
```

---
# Target result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmark: 4 May 2022 - 2:16
* Package commit: 7ee1df
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
| `["collect", "assoc", "basesize=1"]`                | 229.626 ms (5%) |         |  25.97 MiB (1%) |      306808 |
| `["collect", "assoc", "basesize=1024"]`             | 185.805 ms (5%) |         |   2.61 MiB (1%) |         456 |
| `["collect", "assoc", "basesize=32"]`               | 187.656 ms (5%) |         |   4.82 MiB (1%) |       11711 |
| `["collect", "seq"]`                                | 348.446 ms (5%) |         | 812.73 KiB (1%) |          11 |
| `["collect", "unordered", "basesize=1"]`            | 324.250 ms (5%) |         |  23.80 MiB (1%) |      409798 |
| `["collect", "unordered", "basesize=1024"]`         | 199.824 ms (5%) |         |   1.01 MiB (1%) |         964 |
| `["collect", "unordered", "basesize=32"]`           | 208.779 ms (5%) |         |   1.58 MiB (1%) |       14545 |
| `["findfirst", "n=1000", "foldl"]`                  | 629.331 ms (5%) |         |                 |             |
| `["findfirst", "n=1000", "reduce", "basesize=128"]` | 346.754 ms (5%) |         | 232.83 KiB (1%) |        3275 |
| `["findfirst", "n=1000", "reduce", "basesize=256"]` | 490.876 ms (5%) |         | 179.25 KiB (1%) |        2504 |
| `["findfirst", "n=1000", "reduce", "basesize=512"]` | 430.935 ms (5%) |         |  81.42 KiB (1%) |        1149 |
| `["findfirst", "n=400", "foldl"]`                   | 472.973 ms (5%) |         |                 |             |
| `["findfirst", "n=400", "reduce", "basesize=128"]`  | 244.673 ms (5%) |         | 383.19 KiB (1%) |        5456 |
| `["findfirst", "n=400", "reduce", "basesize=256"]`  | 254.884 ms (5%) |         | 204.61 KiB (1%) |        2939 |
| `["findfirst", "n=400", "reduce", "basesize=512"]`  | 363.801 ms (5%) |         | 149.34 KiB (1%) |        2146 |
| `["findfirst", "n=500", "foldl"]`                   |  82.010 ms (5%) |         |                 |             |
| `["findfirst", "n=500", "reduce", "basesize=128"]`  | 192.638 ms (5%) |         | 258.31 KiB (1%) |        3609 |
| `["findfirst", "n=500", "reduce", "basesize=256"]`  | 148.816 ms (5%) |         | 119.52 KiB (1%) |        1652 |
| `["findfirst", "n=500", "reduce", "basesize=512"]`  | 100.710 ms (5%) |         |  60.38 KiB (1%) |         819 |
| `["overhead", "default"]`                           |  73.300 μs (5%) |         |  32.73 KiB (1%) |         418 |
| `["overhead", "stoppable=false"]`                   |  74.800 μs (5%) |         |  32.75 KiB (1%) |         418 |
| `["overhead", "stoppable=true"]`                    |  78.801 μs (5%) |         |  44.25 KiB (1%) |         610 |
| `["parallel_histogram", "assoc", "basesize=16384"]` |   3.229 ms (5%) |         | 728.91 KiB (1%) |          57 |
| `["parallel_histogram", "assoc", "basesize=4096"]`  |   3.738 ms (5%) |         |   1.79 MiB (1%) |         215 |
| `["parallel_histogram", "assoc", "basesize=8192"]`  |   3.544 ms (5%) |         |   1.42 MiB (1%) |         117 |
| `["parallel_histogram", "comm", "basesize=16384"]`  |  17.959 ms (5%) |         |   1.58 MiB (1%) |        2339 |
| `["parallel_histogram", "comm", "basesize=4096"]`   |  24.538 ms (5%) |         |   1.26 MiB (1%) |        7398 |
| `["parallel_histogram", "comm", "basesize=8192"]`   |  22.797 ms (5%) |         |   1.30 MiB (1%) |        5880 |
| `["parallel_histogram", "seq"]`                     |   5.760 ms (5%) |         | 364.16 KiB (1%) |          24 |
| `["partition_length_maximum", "rand", "foldl"]`     |  35.174 ms (5%) |         |                 |             |
| `["partition_length_maximum", "rand", "reduce"]`    |  17.612 ms (5%) |         |  736 bytes (1%) |          11 |
| `["splitby", "count", "foldl"]`                     |   2.178 ms (5%) |         |                 |             |
| `["splitby", "count", "man"]`                       |   1.228 ms (5%) |         |                 |             |
| `["splitby", "count", "reduce"]`                    |   1.082 ms (5%) |         |   1.09 KiB (1%) |          19 |
| `["sum", "random", "foldl"]`                        |  16.271 ms (5%) |         |                 |             |
| `["sum", "random", "reduce", "basesize=128"]`       |   8.205 ms (5%) |         |  74.20 KiB (1%) |        1105 |
| `["sum", "random", "reduce", "basesize=256"]`       |   8.094 ms (5%) |         |  36.80 KiB (1%) |         548 |
| `["sum", "random", "reduce", "basesize=512"]`       |   8.044 ms (5%) |         |  18.11 KiB (1%) |         270 |
| `["sum", "uniform", "foldl"]`                       |  15.770 ms (5%) |         |                 |             |
| `["sum", "uniform", "reduce", "basesize=128"]`      |   7.989 ms (5%) |         |  74.17 KiB (1%) |        1104 |
| `["sum", "uniform", "reduce", "basesize=256"]`      |   7.902 ms (5%) |         |  36.70 KiB (1%) |         545 |
| `["sum", "uniform", "reduce", "basesize=512"]`      |   7.851 ms (5%) |         |  18.03 KiB (1%) |         268 |
| `["sum", "valley", "foldl"]`                        |  16.149 ms (5%) |         |                 |             |
| `["sum", "valley", "reduce", "basesize=128"]`       |   8.218 ms (5%) |         |  74.02 KiB (1%) |        1099 |
| `["sum", "valley", "reduce", "basesize=256"]`       |   8.147 ms (5%) |         |  36.77 KiB (1%) |         547 |
| `["sum", "valley", "reduce", "basesize=512"]`       |   8.099 ms (5%) |         |  18.03 KiB (1%) |         268 |
| `["words", "nthreads=1"]`                           |  22.853 ms (5%) |         |  31.74 MiB (1%) |     1034285 |
| `["words", "nthreads=2"]`                           |  15.856 ms (5%) |         |  32.46 MiB (1%) |     1034367 |
| `["words", "nthreads=4"]`                           |  16.258 ms (5%) |         |  32.90 MiB (1%) |     1034433 |

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
      Ubuntu 20.04.4 LTS
  uname: Linux 5.13.0-1022-azure #26~20.04.1-Ubuntu SMP Thu Apr 7 19:42:45 UTC 2022 x86_64 x86_64
  CPU: Intel(R) Xeon(R) Platinum 8272CL CPU @ 2.60GHz: 
              speed         user         nice          sys         idle          irq
       #1  2593 MHz       5416 s          1 s        204 s       2747 s          0 s
       #2  2593 MHz       4771 s          1 s        206 s       3418 s          0 s
       
  Memory: 6.783607482910156 GB (3829.55859375 MB free)
  Uptime: 844.36 sec
  Load Avg:  1.71  1.49  0.88
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-12.0.1 (ORCJIT, skylake-avx512)
```

---
# Baseline result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmark: 4 May 2022 - 2:21
* Package commit: 6125fe
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
| `["collect", "assoc", "basesize=1"]`                | 245.100 ms (5%) |         |   25.97 MiB (1%) |      306861 |
| `["collect", "assoc", "basesize=1024"]`             | 198.155 ms (5%) |         |    2.61 MiB (1%) |         456 |
| `["collect", "assoc", "basesize=32"]`               | 200.352 ms (5%) |         |    4.82 MiB (1%) |       11709 |
| `["collect", "seq"]`                                | 395.200 ms (5%) |         |  812.73 KiB (1%) |          11 |
| `["collect", "unordered", "basesize=1"]`            | 343.730 ms (5%) |         |   23.79 MiB (1%) |      409444 |
| `["collect", "unordered", "basesize=1024"]`         | 212.987 ms (5%) |         | 1001.55 KiB (1%) |         967 |
| `["collect", "unordered", "basesize=32"]`           | 223.575 ms (5%) |         |    1.58 MiB (1%) |       14742 |
| `["findfirst", "n=1000", "foldl"]`                  | 629.877 ms (5%) |         |                  |             |
| `["findfirst", "n=1000", "reduce", "basesize=128"]` | 322.401 ms (5%) |         |  231.75 KiB (1%) |        3256 |
| `["findfirst", "n=1000", "reduce", "basesize=256"]` | 397.947 ms (5%) |         |  151.28 KiB (1%) |        2128 |
| `["findfirst", "n=1000", "reduce", "basesize=512"]` | 456.740 ms (5%) |         |   96.75 KiB (1%) |        1346 |
| `["findfirst", "n=400", "foldl"]`                   | 472.873 ms (5%) |         |                  |             |
| `["findfirst", "n=400", "reduce", "basesize=128"]`  | 230.250 ms (5%) |         |  374.69 KiB (1%) |        5352 |
| `["findfirst", "n=400", "reduce", "basesize=256"]`  | 233.688 ms (5%) |         |  200.89 KiB (1%) |        2874 |
| `["findfirst", "n=400", "reduce", "basesize=512"]`  | 348.561 ms (5%) |         |  141.58 KiB (1%) |        2014 |
| `["findfirst", "n=500", "foldl"]`                   |  81.852 ms (5%) |         |                  |             |
| `["findfirst", "n=500", "reduce", "basesize=128"]`  | 117.255 ms (5%) |         |  182.80 KiB (1%) |        2526 |
| `["findfirst", "n=500", "reduce", "basesize=256"]`  | 164.029 ms (5%) |         |  136.50 KiB (1%) |        1875 |
| `["findfirst", "n=500", "reduce", "basesize=512"]`  | 105.106 ms (5%) |         |   55.17 KiB (1%) |         752 |
| `["overhead", "default"]`                           |  74.600 μs (5%) |         |   32.73 KiB (1%) |         418 |
| `["overhead", "stoppable=false"]`                   |  76.501 μs (5%) |         |   32.72 KiB (1%) |         417 |
| `["overhead", "stoppable=true"]`                    |  84.801 μs (5%) |         |   44.25 KiB (1%) |         610 |
| `["parallel_histogram", "assoc", "basesize=16384"]` |   3.245 ms (5%) |         |  728.91 KiB (1%) |          57 |
| `["parallel_histogram", "assoc", "basesize=4096"]`  |   3.893 ms (5%) |         |    1.79 MiB (1%) |         216 |
| `["parallel_histogram", "assoc", "basesize=8192"]`  |   3.614 ms (5%) |         |    1.42 MiB (1%) |         117 |
| `["parallel_histogram", "comm", "basesize=16384"]`  |  17.930 ms (5%) |         |    1.58 MiB (1%) |        2411 |
| `["parallel_histogram", "comm", "basesize=4096"]`   |  24.398 ms (5%) |         |    1.25 MiB (1%) |        7067 |
| `["parallel_histogram", "comm", "basesize=8192"]`   |  22.251 ms (5%) |         |    1.32 MiB (1%) |        6080 |
| `["parallel_histogram", "seq"]`                     |   5.776 ms (5%) |         |  364.16 KiB (1%) |          24 |
| `["partition_length_maximum", "rand", "foldl"]`     |  30.831 ms (5%) |         |                  |             |
| `["partition_length_maximum", "rand", "reduce"]`    |  17.588 ms (5%) |         |   736 bytes (1%) |          11 |
| `["splitby", "count", "foldl"]`                     |   2.316 ms (5%) |         |                  |             |
| `["splitby", "count", "man"]`                       |   1.752 ms (5%) |         |                  |             |
| `["splitby", "count", "reduce"]`                    |   1.084 ms (5%) |         |    1.06 KiB (1%) |          18 |
| `["sum", "random", "foldl"]`                        |  16.217 ms (5%) |         |                  |             |
| `["sum", "random", "reduce", "basesize=128"]`       |   7.627 ms (5%) |         |   74.02 KiB (1%) |        1099 |
| `["sum", "random", "reduce", "basesize=256"]`       |   7.573 ms (5%) |         |   36.73 KiB (1%) |         546 |
| `["sum", "random", "reduce", "basesize=512"]`       |   7.496 ms (5%) |         |   18.11 KiB (1%) |         270 |
| `["sum", "uniform", "foldl"]`                       |  15.636 ms (5%) |         |                  |             |
| `["sum", "uniform", "reduce", "basesize=128"]`      |   7.439 ms (5%) |         |   74.11 KiB (1%) |        1102 |
| `["sum", "uniform", "reduce", "basesize=256"]`      |   7.364 ms (5%) |         |   36.73 KiB (1%) |         546 |
| `["sum", "uniform", "reduce", "basesize=512"]`      |   7.293 ms (5%) |         |   18.06 KiB (1%) |         269 |
| `["sum", "valley", "foldl"]`                        |  16.141 ms (5%) |         |                  |             |
| `["sum", "valley", "reduce", "basesize=128"]`       |   8.268 ms (5%) |         |   74.11 KiB (1%) |        1102 |
| `["sum", "valley", "reduce", "basesize=256"]`       |   8.152 ms (5%) |         |   36.73 KiB (1%) |         546 |
| `["sum", "valley", "reduce", "basesize=512"]`       |   8.115 ms (5%) |         |   17.97 KiB (1%) |         266 |
| `["words", "nthreads=1"]`                           |  22.665 ms (5%) |         |   31.57 MiB (1%) |     1028150 |
| `["words", "nthreads=2"]`                           |  14.834 ms (5%) |         |   31.92 MiB (1%) |     1028186 |
| `["words", "nthreads=4"]`                           |  14.517 ms (5%) |         |   32.63 MiB (1%) |     1028268 |

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
      Ubuntu 20.04.4 LTS
  uname: Linux 5.13.0-1022-azure #26~20.04.1-Ubuntu SMP Thu Apr 7 19:42:45 UTC 2022 x86_64 x86_64
  CPU: Intel(R) Xeon(R) Platinum 8272CL CPU @ 2.60GHz: 
              speed         user         nice          sys         idle          irq
       #1  2593 MHz       7910 s          1 s        281 s       3269 s          0 s
       #2  2593 MHz       7002 s          1 s        277 s       4206 s          0 s
       
  Memory: 6.783607482910156 GB (3786.20703125 MB free)
  Uptime: 1153.96 sec
  Load Avg:  1.68  1.58  1.1
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
    CPU MHz:                         2593.907
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

