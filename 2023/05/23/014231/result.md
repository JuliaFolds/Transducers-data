# Multi-thread benchmark result

* Pull request commit: [`9c3461f1bb004440bc6ea9874192a2af186cb094`](https://github.com/JuliaFolds/Transducers.jl/commit/9c3461f1bb004440bc6ea9874192a2af186cb094)
* Pull request: <https://github.com/JuliaFolds/Transducers.jl/pull/243> (Update */Manifest.toml)

# Judge result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmarks:
    - Target: 23 May 2023 - 01:36
    - Baseline: 23 May 2023 - 01:42
* Package commits:
    - Target: 762d37
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
| `["collect", "unordered", "basesize=1"]`            |                   1.03 (5%)  | 0.99 (1%) :white_check_mark: |
| `["findfirst", "n=1000", "reduce", "basesize=128"]` |                1.64 (5%) :x: |                1.54 (1%) :x: |
| `["findfirst", "n=1000", "reduce", "basesize=256"]` |                1.20 (5%) :x: |                1.14 (1%) :x: |
| `["findfirst", "n=1000", "reduce", "basesize=512"]` |                1.80 (5%) :x: |                1.57 (1%) :x: |
| `["findfirst", "n=400", "reduce", "basesize=128"]`  |                   1.00 (5%)  | 0.99 (1%) :white_check_mark: |
| `["findfirst", "n=400", "reduce", "basesize=256"]`  |                   0.98 (5%)  | 0.98 (1%) :white_check_mark: |
| `["findfirst", "n=400", "reduce", "basesize=512"]`  |                1.09 (5%) :x: |                1.08 (1%) :x: |
| `["findfirst", "n=500", "reduce", "basesize=128"]`  |                2.07 (5%) :x: |                1.73 (1%) :x: |
| `["findfirst", "n=500", "reduce", "basesize=256"]`  |                2.15 (5%) :x: |                1.68 (1%) :x: |
| `["findfirst", "n=500", "reduce", "basesize=512"]`  |                1.50 (5%) :x: |                1.25 (1%) :x: |
| `["parallel_histogram", "comm", "basesize=16384"]`  |                1.07 (5%) :x: |                   1.01 (1%)  |
| `["parallel_histogram", "comm", "basesize=4096"]`   |                1.56 (5%) :x: |                1.14 (1%) :x: |
| `["parallel_histogram", "comm", "basesize=8192"]`   |                   1.00 (5%)  |                1.02 (1%) :x: |
| `["partition_length_maximum", "rand", "reduce"]`    |                   1.00 (5%)  |                1.05 (1%) :x: |
| `["splitby", "count", "man"]`                       | 0.81 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["splitby", "count", "reduce"]`                    |                1.09 (5%) :x: |                1.03 (1%) :x: |
| `["words", "nthreads=2"]`                           |                   0.97 (5%)  |                1.02 (1%) :x: |
| `["words", "nthreads=4"]`                           |                   0.95 (5%)  |                1.01 (1%) :x: |

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
  uname: Linux 5.15.0-1037-azure #44-Ubuntu SMP Thu Apr 20 13:19:31 UTC 2023 x86_64 x86_64
  CPU: Intel(R) Xeon(R) Platinum 8272CL CPU @ 2.60GHz: 
              speed         user         nice          sys         idle          irq
       #1  2593 MHz       5124 s          0 s        276 s       3330 s          0 s
       #2  2593 MHz       5408 s          0 s        332 s       2978 s          0 s
       
  Memory: 6.7812042236328125 GB (3962.87890625 MB free)
  Uptime: 878.26 sec
  Load Avg:  1.58  1.46  0.94
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
  uname: Linux 5.15.0-1037-azure #44-Ubuntu SMP Thu Apr 20 13:19:31 UTC 2023 x86_64 x86_64
  CPU: Intel(R) Xeon(R) Platinum 8272CL CPU @ 2.60GHz: 
              speed         user         nice          sys         idle          irq
       #1  2593 MHz       8117 s          0 s        342 s       3448 s          0 s
       #2  2593 MHz       7260 s          0 s        394 s       4235 s          0 s
       
  Memory: 6.7812042236328125 GB (3927.59765625 MB free)
  Uptime: 1196.17 sec
  Load Avg:  1.56  1.57  1.14
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-12.0.1 (ORCJIT, skylake-avx512)
```

---
# Target result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmark: 23 May 2023 - 1:36
* Package commit: 762d37
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
| `["collect", "assoc", "basesize=1"]`                | 199.882 ms (5%) |         |   4.36 MiB (1%) |       32800 |
| `["collect", "assoc", "basesize=1024"]`             | 197.935 ms (5%) |         |   1.09 MiB (1%) |          53 |
| `["collect", "assoc", "basesize=32"]`               | 198.365 ms (5%) |         |   1.48 MiB (1%) |        1053 |
| `["collect", "seq"]`                                | 394.616 ms (5%) |         | 256.05 KiB (1%) |           2 |
| `["collect", "unordered", "basesize=1"]`            | 364.714 ms (5%) |         |  23.58 MiB (1%) |      402540 |
| `["collect", "unordered", "basesize=1024"]`         | 213.003 ms (5%) |         |   1.00 MiB (1%) |         906 |
| `["collect", "unordered", "basesize=32"]`           | 234.727 ms (5%) |         |   1.57 MiB (1%) |       14419 |
| `["findfirst", "n=1000", "foldl"]`                  | 629.561 ms (5%) |         |                 |             |
| `["findfirst", "n=1000", "reduce", "basesize=128"]` | 561.549 ms (5%) |         | 359.28 KiB (1%) |        5045 |
| `["findfirst", "n=1000", "reduce", "basesize=256"]` | 595.931 ms (5%) |         | 200.48 KiB (1%) |        2848 |
| `["findfirst", "n=1000", "reduce", "basesize=512"]` |    1.008 s (5%) |         | 170.08 KiB (1%) |        2408 |
| `["findfirst", "n=400", "foldl"]`                   | 472.415 ms (5%) |         |                 |             |
| `["findfirst", "n=400", "reduce", "basesize=128"]`  | 246.087 ms (5%) |         | 383.16 KiB (1%) |        5455 |
| `["findfirst", "n=400", "reduce", "basesize=256"]`  | 245.866 ms (5%) |         | 196.22 KiB (1%) |        2813 |
| `["findfirst", "n=400", "reduce", "basesize=512"]`  | 355.338 ms (5%) |         | 150.00 KiB (1%) |        2140 |
| `["findfirst", "n=500", "foldl"]`                   |  81.973 ms (5%) |         |                 |             |
| `["findfirst", "n=500", "reduce", "basesize=128"]`  | 193.391 ms (5%) |         | 257.34 KiB (1%) |        3611 |
| `["findfirst", "n=500", "reduce", "basesize=256"]`  | 208.657 ms (5%) |         | 148.59 KiB (1%) |        2073 |
| `["findfirst", "n=500", "reduce", "basesize=512"]`  | 122.921 ms (5%) |         |  63.67 KiB (1%) |         866 |
| `["overhead", "default"]`                           |  73.902 μs (5%) |         |  32.73 KiB (1%) |         418 |
| `["overhead", "stoppable=false"]`                   |  75.101 μs (5%) |         |  32.72 KiB (1%) |         417 |
| `["overhead", "stoppable=true"]`                    |  87.801 μs (5%) |         |  44.25 KiB (1%) |         610 |
| `["parallel_histogram", "assoc", "basesize=16384"]` |   3.235 ms (5%) |         | 728.91 KiB (1%) |          57 |
| `["parallel_histogram", "assoc", "basesize=4096"]`  |   3.889 ms (5%) |         |   1.79 MiB (1%) |         215 |
| `["parallel_histogram", "assoc", "basesize=8192"]`  |   3.588 ms (5%) |         |   1.42 MiB (1%) |         117 |
| `["parallel_histogram", "comm", "basesize=16384"]`  |  17.837 ms (5%) |         |   1.60 MiB (1%) |        3038 |
| `["parallel_histogram", "comm", "basesize=4096"]`   |  25.861 ms (5%) |         |   1.26 MiB (1%) |        7585 |
| `["parallel_histogram", "comm", "basesize=8192"]`   |  22.283 ms (5%) |         |   1.70 MiB (1%) |        6428 |
| `["parallel_histogram", "seq"]`                     |   5.763 ms (5%) |         | 364.16 KiB (1%) |          24 |
| `["partition_length_maximum", "rand", "foldl"]`     |  35.291 ms (5%) |         |                 |             |
| `["partition_length_maximum", "rand", "reduce"]`    |  17.648 ms (5%) |         |  736 bytes (1%) |          11 |
| `["splitby", "count", "foldl"]`                     |   2.242 ms (5%) |         |                 |             |
| `["splitby", "count", "man"]`                       |   1.417 ms (5%) |         |                 |             |
| `["splitby", "count", "reduce"]`                    |   1.173 ms (5%) |         |   1.09 KiB (1%) |          19 |
| `["sum", "random", "foldl"]`                        |  16.282 ms (5%) |         |                 |             |
| `["sum", "random", "reduce", "basesize=128"]`       |   8.217 ms (5%) |         |  74.08 KiB (1%) |        1101 |
| `["sum", "random", "reduce", "basesize=256"]`       |   8.122 ms (5%) |         |  36.73 KiB (1%) |         546 |
| `["sum", "random", "reduce", "basesize=512"]`       |   8.057 ms (5%) |         |  18.08 KiB (1%) |         269 |
| `["sum", "uniform", "foldl"]`                       |  15.738 ms (5%) |         |                 |             |
| `["sum", "uniform", "reduce", "basesize=128"]`      |   8.019 ms (5%) |         |  74.14 KiB (1%) |        1103 |
| `["sum", "uniform", "reduce", "basesize=256"]`      |   7.890 ms (5%) |         |  36.70 KiB (1%) |         545 |
| `["sum", "uniform", "reduce", "basesize=512"]`      |   7.829 ms (5%) |         |  17.97 KiB (1%) |         266 |
| `["sum", "valley", "foldl"]`                        |  16.137 ms (5%) |         |                 |             |
| `["sum", "valley", "reduce", "basesize=128"]`       |   8.245 ms (5%) |         |  74.02 KiB (1%) |        1099 |
| `["sum", "valley", "reduce", "basesize=256"]`       |   8.155 ms (5%) |         |  36.70 KiB (1%) |         545 |
| `["sum", "valley", "reduce", "basesize=512"]`       |   8.136 ms (5%) |         |  18.06 KiB (1%) |         269 |
| `["words", "nthreads=1"]`                           |  24.132 ms (5%) |         |  31.73 MiB (1%) |     1033673 |
| `["words", "nthreads=2"]`                           |  15.173 ms (5%) |         |  32.44 MiB (1%) |     1033761 |
| `["words", "nthreads=4"]`                           |  15.005 ms (5%) |         |  32.89 MiB (1%) |     1033843 |

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
  uname: Linux 5.15.0-1037-azure #44-Ubuntu SMP Thu Apr 20 13:19:31 UTC 2023 x86_64 x86_64
  CPU: Intel(R) Xeon(R) Platinum 8272CL CPU @ 2.60GHz: 
              speed         user         nice          sys         idle          irq
       #1  2593 MHz       5124 s          0 s        276 s       3330 s          0 s
       #2  2593 MHz       5408 s          0 s        332 s       2978 s          0 s
       
  Memory: 6.7812042236328125 GB (3962.87890625 MB free)
  Uptime: 878.26 sec
  Load Avg:  1.58  1.46  0.94
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-12.0.1 (ORCJIT, skylake-avx512)
```

---
# Baseline result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmark: 23 May 2023 - 1:42
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
| `["collect", "assoc", "basesize=1"]`                | 200.229 ms (5%) |         |   4.36 MiB (1%) |       32800 |
| `["collect", "assoc", "basesize=1024"]`             | 198.284 ms (5%) |         |   1.09 MiB (1%) |          53 |
| `["collect", "assoc", "basesize=32"]`               | 198.283 ms (5%) |         |   1.48 MiB (1%) |        1052 |
| `["collect", "seq"]`                                | 394.980 ms (5%) |         | 256.05 KiB (1%) |           2 |
| `["collect", "unordered", "basesize=1"]`            | 352.946 ms (5%) |         |  23.90 MiB (1%) |      413098 |
| `["collect", "unordered", "basesize=1024"]`         | 213.152 ms (5%) |         |   1.01 MiB (1%) |         992 |
| `["collect", "unordered", "basesize=32"]`           | 224.168 ms (5%) |         |   1.58 MiB (1%) |       14583 |
| `["findfirst", "n=1000", "foldl"]`                  | 625.665 ms (5%) |         |                 |             |
| `["findfirst", "n=1000", "reduce", "basesize=128"]` | 343.394 ms (5%) |         | 232.86 KiB (1%) |        3276 |
| `["findfirst", "n=1000", "reduce", "basesize=256"]` | 497.711 ms (5%) |         | 175.89 KiB (1%) |        2453 |
| `["findfirst", "n=1000", "reduce", "basesize=512"]` | 561.336 ms (5%) |         | 108.55 KiB (1%) |        1509 |
| `["findfirst", "n=400", "foldl"]`                   | 469.380 ms (5%) |         |                 |             |
| `["findfirst", "n=400", "reduce", "basesize=128"]`  | 247.096 ms (5%) |         | 388.70 KiB (1%) |        5530 |
| `["findfirst", "n=400", "reduce", "basesize=256"]`  | 250.952 ms (5%) |         | 199.58 KiB (1%) |        2863 |
| `["findfirst", "n=400", "reduce", "basesize=512"]`  | 324.782 ms (5%) |         | 139.14 KiB (1%) |        1976 |
| `["findfirst", "n=500", "foldl"]`                   |  81.375 ms (5%) |         |                 |             |
| `["findfirst", "n=500", "reduce", "basesize=128"]`  |  93.535 ms (5%) |         | 149.05 KiB (1%) |        2048 |
| `["findfirst", "n=500", "reduce", "basesize=256"]`  |  97.184 ms (5%) |         |  88.38 KiB (1%) |        1204 |
| `["findfirst", "n=500", "reduce", "basesize=512"]`  |  82.067 ms (5%) |         |  50.81 KiB (1%) |         680 |
| `["overhead", "default"]`                           |  74.801 μs (5%) |         |  32.70 KiB (1%) |         417 |
| `["overhead", "stoppable=false"]`                   |  75.501 μs (5%) |         |  32.75 KiB (1%) |         418 |
| `["overhead", "stoppable=true"]`                    |  84.601 μs (5%) |         |  44.25 KiB (1%) |         610 |
| `["parallel_histogram", "assoc", "basesize=16384"]` |   3.230 ms (5%) |         | 728.91 KiB (1%) |          57 |
| `["parallel_histogram", "assoc", "basesize=4096"]`  |   3.887 ms (5%) |         |   1.79 MiB (1%) |         215 |
| `["parallel_histogram", "assoc", "basesize=8192"]`  |   3.581 ms (5%) |         |   1.42 MiB (1%) |         117 |
| `["parallel_histogram", "comm", "basesize=16384"]`  |  16.624 ms (5%) |         |   1.59 MiB (1%) |        2758 |
| `["parallel_histogram", "comm", "basesize=4096"]`   |  16.605 ms (5%) |         |   1.11 MiB (1%) |        2377 |
| `["parallel_histogram", "comm", "basesize=8192"]`   |  22.381 ms (5%) |         |   1.67 MiB (1%) |        5481 |
| `["parallel_histogram", "seq"]`                     |   5.749 ms (5%) |         | 364.16 KiB (1%) |          24 |
| `["partition_length_maximum", "rand", "foldl"]`     |  35.282 ms (5%) |         |                 |             |
| `["partition_length_maximum", "rand", "reduce"]`    |  17.571 ms (5%) |         |  704 bytes (1%) |          10 |
| `["splitby", "count", "foldl"]`                     |   2.291 ms (5%) |         |                 |             |
| `["splitby", "count", "man"]`                       |   1.754 ms (5%) |         |                 |             |
| `["splitby", "count", "reduce"]`                    |   1.078 ms (5%) |         |   1.06 KiB (1%) |          19 |
| `["sum", "random", "foldl"]`                        |  16.122 ms (5%) |         |                 |             |
| `["sum", "random", "reduce", "basesize=128"]`       |   8.160 ms (5%) |         |  74.14 KiB (1%) |        1103 |
| `["sum", "random", "reduce", "basesize=256"]`       |   8.042 ms (5%) |         |  36.77 KiB (1%) |         547 |
| `["sum", "random", "reduce", "basesize=512"]`       |   7.998 ms (5%) |         |  18.11 KiB (1%) |         270 |
| `["sum", "uniform", "foldl"]`                       |  15.739 ms (5%) |         |                 |             |
| `["sum", "uniform", "reduce", "basesize=128"]`      |   7.966 ms (5%) |         |  74.11 KiB (1%) |        1102 |
| `["sum", "uniform", "reduce", "basesize=256"]`      |   7.842 ms (5%) |         |  36.70 KiB (1%) |         545 |
| `["sum", "uniform", "reduce", "basesize=512"]`      |   7.784 ms (5%) |         |  18.00 KiB (1%) |         267 |
| `["sum", "valley", "foldl"]`                        |  16.068 ms (5%) |         |                 |             |
| `["sum", "valley", "reduce", "basesize=128"]`       |   8.220 ms (5%) |         |  74.17 KiB (1%) |        1104 |
| `["sum", "valley", "reduce", "basesize=256"]`       |   8.121 ms (5%) |         |  36.70 KiB (1%) |         545 |
| `["sum", "valley", "reduce", "basesize=512"]`       |   8.122 ms (5%) |         |  18.00 KiB (1%) |         267 |
| `["words", "nthreads=1"]`                           |  25.234 ms (5%) |         |  31.48 MiB (1%) |     1026010 |
| `["words", "nthreads=2"]`                           |  15.608 ms (5%) |         |  31.84 MiB (1%) |     1026060 |
| `["words", "nthreads=4"]`                           |  15.786 ms (5%) |         |  32.55 MiB (1%) |     1026143 |

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
  uname: Linux 5.15.0-1037-azure #44-Ubuntu SMP Thu Apr 20 13:19:31 UTC 2023 x86_64 x86_64
  CPU: Intel(R) Xeon(R) Platinum 8272CL CPU @ 2.60GHz: 
              speed         user         nice          sys         idle          irq
       #1  2593 MHz       8117 s          0 s        342 s       3448 s          0 s
       #2  2593 MHz       7260 s          0 s        394 s       4235 s          0 s
       
  Memory: 6.7812042236328125 GB (3927.59765625 MB free)
  Uptime: 1196.17 sec
  Load Avg:  1.56  1.57  1.14
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

