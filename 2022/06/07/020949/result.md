# Multi-thread benchmark result

* Pull request commit: [`0ac3bd029e14326d143d38c0d0e98405ea9e1b6e`](https://github.com/JuliaFolds/Transducers.jl/commit/0ac3bd029e14326d143d38c0d0e98405ea9e1b6e)
* Pull request: <https://github.com/JuliaFolds/Transducers.jl/pull/243> (Update */Manifest.toml)

# Judge result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmarks:
    - Target: 7 Jun 2022 - 02:04
    - Baseline: 7 Jun 2022 - 02:09
* Package commits:
    - Target: c57618
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
| `["collect", "unordered", "basesize=1024"]`         |                   1.00 (5%)  |                1.03 (1%) :x: |
| `["findfirst", "n=1000", "reduce", "basesize=256"]` |                1.13 (5%) :x: |                1.04 (1%) :x: |
| `["findfirst", "n=1000", "reduce", "basesize=512"]` | 0.51 (5%) :white_check_mark: | 0.61 (1%) :white_check_mark: |
| `["findfirst", "n=400", "reduce", "basesize=128"]`  | 0.94 (5%) :white_check_mark: | 0.97 (1%) :white_check_mark: |
| `["findfirst", "n=400", "reduce", "basesize=256"]`  |                   0.99 (5%)  |                1.02 (1%) :x: |
| `["findfirst", "n=400", "reduce", "basesize=512"]`  |                1.36 (5%) :x: |                1.32 (1%) :x: |
| `["findfirst", "n=500", "reduce", "basesize=128"]`  |                1.24 (5%) :x: |                1.18 (1%) :x: |
| `["findfirst", "n=500", "reduce", "basesize=256"]`  | 0.86 (5%) :white_check_mark: | 0.88 (1%) :white_check_mark: |
| `["findfirst", "n=500", "reduce", "basesize=512"]`  |                1.22 (5%) :x: |                1.13 (1%) :x: |
| `["parallel_histogram", "comm", "basesize=16384"]`  |                   0.97 (5%)  | 0.98 (1%) :white_check_mark: |
| `["parallel_histogram", "comm", "basesize=4096"]`   | 0.80 (5%) :white_check_mark: | 0.89 (1%) :white_check_mark: |
| `["parallel_histogram", "comm", "basesize=8192"]`   |                1.05 (5%) :x: | 0.76 (1%) :white_check_mark: |
| `["partition_length_maximum", "rand", "reduce"]`    |                   1.00 (5%)  | 0.96 (1%) :white_check_mark: |
| `["splitby", "count", "man"]`                       | 0.81 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["splitby", "count", "reduce"]`                    |                   1.01 (5%)  |                1.05 (1%) :x: |
| `["sum", "random", "foldl"]`                        | 0.86 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["sum", "random", "reduce", "basesize=128"]`       | 0.94 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["sum", "random", "reduce", "basesize=256"]`       | 0.94 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["sum", "random", "reduce", "basesize=512"]`       | 0.94 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["sum", "valley", "reduce", "basesize=128"]`       | 0.93 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["sum", "valley", "reduce", "basesize=256"]`       | 0.93 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["words", "nthreads=2"]`                           |                1.07 (5%) :x: | 0.99 (1%) :white_check_mark: |
| `["words", "nthreads=4"]`                           |                1.12 (5%) :x: | 0.99 (1%) :white_check_mark: |

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
  uname: Linux 5.13.0-1025-azure #29~20.04.1-Ubuntu SMP Thu May 19 14:50:45 UTC 2022 x86_64 x86_64
  CPU: Intel(R) Xeon(R) Platinum 8272CL CPU @ 2.60GHz: 
              speed         user         nice          sys         idle          irq
       #1  2593 MHz       5742 s          1 s        203 s       3578 s          0 s
       #2  2593 MHz       4644 s          1 s        210 s       4693 s          0 s
       
  Memory: 6.783603668212891 GB (3719.0234375 MB free)
  Uptime: 958.14 sec
  Load Avg:  1.73  1.5  0.91
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
  uname: Linux 5.13.0-1025-azure #29~20.04.1-Ubuntu SMP Thu May 19 14:50:45 UTC 2022 x86_64 x86_64
  CPU: Intel(R) Xeon(R) Platinum 8272CL CPU @ 2.60GHz: 
              speed         user         nice          sys         idle          irq
       #1  2593 MHz       7879 s          1 s        264 s       4496 s          0 s
       #2  2593 MHz       7298 s          1 s        264 s       5107 s          0 s
       
  Memory: 6.783603668212891 GB (3798.41015625 MB free)
  Uptime: 1270.38 sec
  Load Avg:  1.58  1.57  1.11
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-12.0.1 (ORCJIT, skylake-avx512)
```

---
# Target result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmark: 7 Jun 2022 - 2:4
* Package commit: c57618
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
| `["collect", "assoc", "basesize=1"]`                | 244.311 ms (5%) |         |  25.97 MiB (1%) |      306854 |
| `["collect", "assoc", "basesize=1024"]`             | 198.081 ms (5%) |         |   2.61 MiB (1%) |         456 |
| `["collect", "assoc", "basesize=32"]`               | 200.472 ms (5%) |         |   4.82 MiB (1%) |       11713 |
| `["collect", "seq"]`                                | 394.948 ms (5%) |         | 812.73 KiB (1%) |          11 |
| `["collect", "unordered", "basesize=1"]`            | 340.902 ms (5%) |         |  23.92 MiB (1%) |      413544 |
| `["collect", "unordered", "basesize=1024"]`         | 213.679 ms (5%) |         |   1.01 MiB (1%) |        1018 |
| `["collect", "unordered", "basesize=32"]`           | 222.221 ms (5%) |         |   1.58 MiB (1%) |       14693 |
| `["findfirst", "n=1000", "foldl"]`                  | 625.500 ms (5%) |         |                 |             |
| `["findfirst", "n=1000", "reduce", "basesize=128"]` | 343.018 ms (5%) |         | 232.67 KiB (1%) |        3270 |
| `["findfirst", "n=1000", "reduce", "basesize=256"]` | 560.014 ms (5%) |         | 184.42 KiB (1%) |        2622 |
| `["findfirst", "n=1000", "reduce", "basesize=512"]` | 458.286 ms (5%) |         |  96.84 KiB (1%) |        1349 |
| `["findfirst", "n=400", "foldl"]`                   | 469.277 ms (5%) |         |                 |             |
| `["findfirst", "n=400", "reduce", "basesize=128"]`  | 253.526 ms (5%) |         | 398.52 KiB (1%) |        5665 |
| `["findfirst", "n=400", "reduce", "basesize=256"]`  | 246.808 ms (5%) |         | 200.77 KiB (1%) |        2870 |
| `["findfirst", "n=400", "reduce", "basesize=512"]`  | 382.230 ms (5%) |         | 153.28 KiB (1%) |        2199 |
| `["findfirst", "n=500", "foldl"]`                   |  81.395 ms (5%) |         |                 |             |
| `["findfirst", "n=500", "reduce", "basesize=128"]`  | 173.188 ms (5%) |         | 258.16 KiB (1%) |        3586 |
| `["findfirst", "n=500", "reduce", "basesize=256"]`  |  62.094 ms (5%) |         |  62.81 KiB (1%) |         860 |
| `["findfirst", "n=500", "reduce", "basesize=512"]`  | 107.288 ms (5%) |         |  59.92 KiB (1%) |         821 |
| `["overhead", "default"]`                           |  74.302 μs (5%) |         |  32.73 KiB (1%) |         418 |
| `["overhead", "stoppable=false"]`                   |  74.302 μs (5%) |         |  32.75 KiB (1%) |         418 |
| `["overhead", "stoppable=true"]`                    |  85.302 μs (5%) |         |  44.25 KiB (1%) |         610 |
| `["parallel_histogram", "assoc", "basesize=16384"]` |   3.228 ms (5%) |         | 728.91 KiB (1%) |          57 |
| `["parallel_histogram", "assoc", "basesize=4096"]`  |   3.886 ms (5%) |         |   1.79 MiB (1%) |         216 |
| `["parallel_histogram", "assoc", "basesize=8192"]`  |   3.584 ms (5%) |         |   1.42 MiB (1%) |         117 |
| `["parallel_histogram", "comm", "basesize=16384"]`  |  17.729 ms (5%) |         |   1.56 MiB (1%) |        1897 |
| `["parallel_histogram", "comm", "basesize=4096"]`   |  19.711 ms (5%) |         |   1.10 MiB (1%) |        2220 |
| `["parallel_histogram", "comm", "basesize=8192"]`   |  21.894 ms (5%) |         |   1.26 MiB (1%) |        6067 |
| `["parallel_histogram", "seq"]`                     |   5.738 ms (5%) |         | 364.16 KiB (1%) |          24 |
| `["partition_length_maximum", "rand", "foldl"]`     |  35.245 ms (5%) |         |                 |             |
| `["partition_length_maximum", "rand", "reduce"]`    |  17.602 ms (5%) |         |  704 bytes (1%) |          10 |
| `["splitby", "count", "foldl"]`                     |   2.245 ms (5%) |         |                 |             |
| `["splitby", "count", "man"]`                       |   1.417 ms (5%) |         |                 |             |
| `["splitby", "count", "reduce"]`                    |   1.085 ms (5%) |         |   1.06 KiB (1%) |          18 |
| `["sum", "random", "foldl"]`                        |  14.013 ms (5%) |         |                 |             |
| `["sum", "random", "reduce", "basesize=128"]`       |   7.686 ms (5%) |         |  74.20 KiB (1%) |        1105 |
| `["sum", "random", "reduce", "basesize=256"]`       |   7.623 ms (5%) |         |  36.77 KiB (1%) |         547 |
| `["sum", "random", "reduce", "basesize=512"]`       |   7.582 ms (5%) |         |  18.11 KiB (1%) |         270 |
| `["sum", "uniform", "foldl"]`                       |  15.758 ms (5%) |         |                 |             |
| `["sum", "uniform", "reduce", "basesize=128"]`      |   7.954 ms (5%) |         |  74.14 KiB (1%) |        1103 |
| `["sum", "uniform", "reduce", "basesize=256"]`      |   7.862 ms (5%) |         |  36.73 KiB (1%) |         546 |
| `["sum", "uniform", "reduce", "basesize=512"]`      |   7.817 ms (5%) |         |  18.03 KiB (1%) |         268 |
| `["sum", "valley", "foldl"]`                        |  16.087 ms (5%) |         |                 |             |
| `["sum", "valley", "reduce", "basesize=128"]`       |   7.622 ms (5%) |         |  74.05 KiB (1%) |        1100 |
| `["sum", "valley", "reduce", "basesize=256"]`       |   7.564 ms (5%) |         |  36.70 KiB (1%) |         545 |
| `["sum", "valley", "reduce", "basesize=512"]`       |   8.074 ms (5%) |         |  18.06 KiB (1%) |         269 |
| `["words", "nthreads=1"]`                           |  23.023 ms (5%) |         |  31.66 MiB (1%) |     1031178 |
| `["words", "nthreads=2"]`                           |  15.690 ms (5%) |         |  32.02 MiB (1%) |     1031214 |
| `["words", "nthreads=4"]`                           |  15.398 ms (5%) |         |  32.74 MiB (1%) |     1031299 |

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
  uname: Linux 5.13.0-1025-azure #29~20.04.1-Ubuntu SMP Thu May 19 14:50:45 UTC 2022 x86_64 x86_64
  CPU: Intel(R) Xeon(R) Platinum 8272CL CPU @ 2.60GHz: 
              speed         user         nice          sys         idle          irq
       #1  2593 MHz       5742 s          1 s        203 s       3578 s          0 s
       #2  2593 MHz       4644 s          1 s        210 s       4693 s          0 s
       
  Memory: 6.783603668212891 GB (3719.0234375 MB free)
  Uptime: 958.14 sec
  Load Avg:  1.73  1.5  0.91
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-12.0.1 (ORCJIT, skylake-avx512)
```

---
# Baseline result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmark: 7 Jun 2022 - 2:9
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
| `["collect", "assoc", "basesize=1"]`                | 245.691 ms (5%) |         |   25.97 MiB (1%) |      306758 |
| `["collect", "assoc", "basesize=1024"]`             | 198.476 ms (5%) |         |    2.61 MiB (1%) |         455 |
| `["collect", "assoc", "basesize=32"]`               | 200.096 ms (5%) |         |    4.82 MiB (1%) |       11713 |
| `["collect", "seq"]`                                | 395.197 ms (5%) |         |  812.73 KiB (1%) |          11 |
| `["collect", "unordered", "basesize=1"]`            | 342.917 ms (5%) |         |   23.90 MiB (1%) |      412878 |
| `["collect", "unordered", "basesize=1024"]`         | 212.798 ms (5%) |         | 1004.77 KiB (1%) |         894 |
| `["collect", "unordered", "basesize=32"]`           | 223.882 ms (5%) |         |    1.58 MiB (1%) |       14732 |
| `["findfirst", "n=1000", "foldl"]`                  | 630.272 ms (5%) |         |                  |             |
| `["findfirst", "n=1000", "reduce", "basesize=128"]` | 348.160 ms (5%) |         |  232.86 KiB (1%) |        3276 |
| `["findfirst", "n=1000", "reduce", "basesize=256"]` | 497.241 ms (5%) |         |  177.58 KiB (1%) |        2491 |
| `["findfirst", "n=1000", "reduce", "basesize=512"]` | 903.728 ms (5%) |         |  158.78 KiB (1%) |        2237 |
| `["findfirst", "n=400", "foldl"]`                   | 472.878 ms (5%) |         |                  |             |
| `["findfirst", "n=400", "reduce", "basesize=128"]`  | 268.368 ms (5%) |         |  411.88 KiB (1%) |        5862 |
| `["findfirst", "n=400", "reduce", "basesize=256"]`  | 248.618 ms (5%) |         |  196.98 KiB (1%) |        2825 |
| `["findfirst", "n=400", "reduce", "basesize=512"]`  | 281.216 ms (5%) |         |  115.73 KiB (1%) |        1666 |
| `["findfirst", "n=500", "foldl"]`                   |  81.991 ms (5%) |         |                  |             |
| `["findfirst", "n=500", "reduce", "basesize=128"]`  | 139.664 ms (5%) |         |  218.41 KiB (1%) |        2983 |
| `["findfirst", "n=500", "reduce", "basesize=256"]`  |  72.181 ms (5%) |         |   71.47 KiB (1%) |         979 |
| `["findfirst", "n=500", "reduce", "basesize=512"]`  |  87.961 ms (5%) |         |   53.05 KiB (1%) |         709 |
| `["overhead", "default"]`                           |  71.202 μs (5%) |         |   32.73 KiB (1%) |         418 |
| `["overhead", "stoppable=false"]`                   |  75.902 μs (5%) |         |   32.72 KiB (1%) |         417 |
| `["overhead", "stoppable=true"]`                    |  85.201 μs (5%) |         |   44.22 KiB (1%) |         609 |
| `["parallel_histogram", "assoc", "basesize=16384"]` |   3.230 ms (5%) |         |  728.91 KiB (1%) |          57 |
| `["parallel_histogram", "assoc", "basesize=4096"]`  |   3.871 ms (5%) |         |    1.79 MiB (1%) |         216 |
| `["parallel_histogram", "assoc", "basesize=8192"]`  |   3.565 ms (5%) |         |    1.42 MiB (1%) |         117 |
| `["parallel_histogram", "comm", "basesize=16384"]`  |  18.306 ms (5%) |         |    1.60 MiB (1%) |        3056 |
| `["parallel_histogram", "comm", "basesize=4096"]`   |  24.588 ms (5%) |         |    1.24 MiB (1%) |        6772 |
| `["parallel_histogram", "comm", "basesize=8192"]`   |  20.788 ms (5%) |         |    1.67 MiB (1%) |        5295 |
| `["parallel_histogram", "seq"]`                     |   5.769 ms (5%) |         |  364.16 KiB (1%) |          24 |
| `["partition_length_maximum", "rand", "foldl"]`     |  35.255 ms (5%) |         |                  |             |
| `["partition_length_maximum", "rand", "reduce"]`    |  17.654 ms (5%) |         |   736 bytes (1%) |          11 |
| `["splitby", "count", "foldl"]`                     |   2.275 ms (5%) |         |                  |             |
| `["splitby", "count", "man"]`                       |   1.754 ms (5%) |         |                  |             |
| `["splitby", "count", "reduce"]`                    |   1.078 ms (5%) |         |    1.02 KiB (1%) |          18 |
| `["sum", "random", "foldl"]`                        |  16.278 ms (5%) |         |                  |             |
| `["sum", "random", "reduce", "basesize=128"]`       |   8.156 ms (5%) |         |   74.14 KiB (1%) |        1103 |
| `["sum", "random", "reduce", "basesize=256"]`       |   8.108 ms (5%) |         |   36.70 KiB (1%) |         545 |
| `["sum", "random", "reduce", "basesize=512"]`       |   8.025 ms (5%) |         |   18.11 KiB (1%) |         270 |
| `["sum", "uniform", "foldl"]`                       |  15.689 ms (5%) |         |                  |             |
| `["sum", "uniform", "reduce", "basesize=128"]`      |   7.971 ms (5%) |         |   74.11 KiB (1%) |        1102 |
| `["sum", "uniform", "reduce", "basesize=256"]`      |   7.930 ms (5%) |         |   36.70 KiB (1%) |         545 |
| `["sum", "uniform", "reduce", "basesize=512"]`      |   7.869 ms (5%) |         |   18.03 KiB (1%) |         268 |
| `["sum", "valley", "foldl"]`                        |  16.115 ms (5%) |         |                  |             |
| `["sum", "valley", "reduce", "basesize=128"]`       |   8.232 ms (5%) |         |   74.11 KiB (1%) |        1102 |
| `["sum", "valley", "reduce", "basesize=256"]`       |   8.120 ms (5%) |         |   36.70 KiB (1%) |         545 |
| `["sum", "valley", "reduce", "basesize=512"]`       |   8.110 ms (5%) |         |   18.06 KiB (1%) |         269 |
| `["words", "nthreads=1"]`                           |  24.165 ms (5%) |         |   31.76 MiB (1%) |     1034931 |
| `["words", "nthreads=2"]`                           |  14.690 ms (5%) |         |   32.47 MiB (1%) |     1035016 |
| `["words", "nthreads=4"]`                           |  13.800 ms (5%) |         |   33.10 MiB (1%) |     1035186 |

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
  uname: Linux 5.13.0-1025-azure #29~20.04.1-Ubuntu SMP Thu May 19 14:50:45 UTC 2022 x86_64 x86_64
  CPU: Intel(R) Xeon(R) Platinum 8272CL CPU @ 2.60GHz: 
              speed         user         nice          sys         idle          irq
       #1  2593 MHz       7879 s          1 s        264 s       4496 s          0 s
       #2  2593 MHz       7298 s          1 s        264 s       5107 s          0 s
       
  Memory: 6.783603668212891 GB (3798.41015625 MB free)
  Uptime: 1270.38 sec
  Load Avg:  1.58  1.57  1.11
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

