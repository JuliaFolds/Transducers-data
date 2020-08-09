# Multi-thread benchmark result

* Pull request commit: [`1b4e7f74ed4b4f816c86c64b1c12e2a8d28ea753`](https://github.com/JuliaFolds/Transducers.jl/commit/1b4e7f74ed4b4f816c86c64b1c12e2a8d28ea753)
* Pull request: <https://github.com/JuliaFolds/Transducers.jl/pull/243> (Update */Manifest.toml)

# Judge result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmarks:
    - Target: 9 Aug 2020 - 00:53
    - Baseline: 9 Aug 2020 - 00:59
* Package commits:
    - Target: b3702c
    - Baseline: f87cd6
* Julia commits:
    - Target: 44fa15
    - Baseline: 44fa15
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
| `["collect", "assoc", "basesize=1024"]`             |                1.10 (5%) :x: |                   1.00 (1%)  |
| `["collect", "assoc", "basesize=32"]`               |                1.06 (5%) :x: |                   1.00 (1%)  |
| `["collect", "unordered", "basesize=1"]`            |                1.05 (5%) :x: |                   1.00 (1%)  |
| `["collect", "unordered", "basesize=1024"]`         |                1.10 (5%) :x: |                1.01 (1%) :x: |
| `["collect", "unordered", "basesize=32"]`           |                1.08 (5%) :x: |                   1.00 (1%)  |
| `["findfirst", "n=1000", "reduce", "basesize=128"]` |                1.06 (5%) :x: |                   1.00 (1%)  |
| `["findfirst", "n=1000", "reduce", "basesize=256"]` |                1.14 (5%) :x: |                   1.00 (1%)  |
| `["findfirst", "n=1000", "reduce", "basesize=512"]` |                1.07 (5%) :x: |                   1.00 (1%)  |
| `["findfirst", "n=400", "reduce", "basesize=128"]`  | 0.95 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["findfirst", "n=400", "reduce", "basesize=256"]`  |                1.06 (5%) :x: |                   1.00 (1%)  |
| `["findfirst", "n=500", "foldl"]`                   |                1.17 (5%) :x: |                   1.00 (1%)  |
| `["findfirst", "n=500", "reduce", "basesize=128"]`  | 0.93 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["findfirst", "n=500", "reduce", "basesize=512"]`  |                1.15 (5%) :x: |                   1.00 (1%)  |
| `["overhead", "default"]`                           |                1.08 (5%) :x: |                   1.00 (1%)  |
| `["overhead", "stoppable=false"]`                   |                1.13 (5%) :x: |                   1.00 (1%)  |
| `["overhead", "stoppable=true"]`                    |                1.06 (5%) :x: |                   1.00 (1%)  |
| `["parallel_histogram", "assoc", "basesize=16384"]` |                1.17 (5%) :x: |                   1.00 (1%)  |
| `["parallel_histogram", "assoc", "basesize=4096"]`  |                1.06 (5%) :x: | 0.87 (1%) :white_check_mark: |
| `["parallel_histogram", "assoc", "basesize=8192"]`  |                1.07 (5%) :x: |                   1.00 (1%)  |
| `["parallel_histogram", "comm", "basesize=16384"]`  | 0.93 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["parallel_histogram", "comm", "basesize=4096"]`   | 0.88 (5%) :white_check_mark: |                1.02 (1%) :x: |
| `["parallel_histogram", "comm", "basesize=8192"]`   | 0.89 (5%) :white_check_mark: | 0.98 (1%) :white_check_mark: |
| `["sum", "random", "reduce", "basesize=128"]`       | 0.92 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["sum", "uniform", "reduce", "basesize=256"]`      |                1.05 (5%) :x: |                   1.00 (1%)  |
| `["sum", "uniform", "reduce", "basesize=512"]`      |                1.07 (5%) :x: |                   1.00 (1%)  |
| `["sum", "valley", "reduce", "basesize=128"]`       | 0.91 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["sum", "valley", "reduce", "basesize=512"]`       |                1.14 (5%) :x: |                   1.00 (1%)  |
| `["words", "nthreads=1"]`                           | 0.83 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["words", "nthreads=2"]`                           | 0.93 (5%) :white_check_mark: |                   1.00 (1%)  |

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
Julia Version 1.4.2
Commit 44fa15b150* (2020-05-23 18:35 UTC)
Platform Info:
  OS: Linux (x86_64-pc-linux-gnu)
      Ubuntu 18.04.4 LTS
  uname: Linux 5.3.0-1034-azure #35~18.04.1-Ubuntu SMP Mon Jul 13 12:54:45 UTC 2020 x86_64 x86_64
  CPU: Intel(R) Xeon(R) CPU E5-2673 v4 @ 2.30GHz: 
              speed         user         nice          sys         idle          irq
       #1  2294 MHz      51991 s          0 s       2154 s      15377 s          0 s
       #2  2294 MHz      48848 s          0 s       2784 s      17717 s          0 s
       
  Memory: 6.764881134033203 GB (2978.6171875 MB free)
  Uptime: 717.0 sec
  Load Avg:  1.74609375  1.58984375  0.97412109375
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-8.0.1 (ORCJIT, broadwell)
```

### Baseline
```
Julia Version 1.4.2
Commit 44fa15b150* (2020-05-23 18:35 UTC)
Platform Info:
  OS: Linux (x86_64-pc-linux-gnu)
      Ubuntu 18.04.4 LTS
  uname: Linux 5.3.0-1034-azure #35~18.04.1-Ubuntu SMP Mon Jul 13 12:54:45 UTC 2020 x86_64 x86_64
  CPU: Intel(R) Xeon(R) CPU E5-2673 v4 @ 2.30GHz: 
              speed         user         nice          sys         idle          irq
       #1  2294 MHz      72453 s          0 s       2956 s      27081 s          0 s
       #2  2294 MHz      77052 s          0 s       3416 s      21837 s          0 s
       
  Memory: 6.764881134033203 GB (2960.5234375 MB free)
  Uptime: 1048.0 sec
  Load Avg:  1.68798828125  1.5810546875  1.14892578125
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-8.0.1 (ORCJIT, broadwell)
```

---
# Target result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmark: 9 Aug 2020 - 0:53
* Package commit: b3702c
* Julia commit: 44fa15
* Julia command flags: None
* Environment variables: `JULIA_NUM_THREADS => 2`

## Results
Below is a table of this job's results, obtained by running the benchmarks.
The values listed in the `ID` column have the structure `[parent_group, child_group, ..., key]`, and can be used to
index into the BaseBenchmarks suite to retrieve the corresponding benchmarks.
The percentages accompanying time and memory values in the below table are noise tolerances. The "true"
time/memory value for a given benchmark is expected to fall within this percentage of the reported value.
An empty cell means that the value was zero.

| ID                                                  | time            | GC time   | memory          | allocations |
|-----------------------------------------------------|----------------:|----------:|----------------:|------------:|
| `["collect", "assoc", "basesize=1"]`                | 326.802 ms (5%) | 12.976 ms |  87.55 MiB (1%) |     1590761 |
| `["collect", "assoc", "basesize=1024"]`             | 188.237 ms (5%) |           |   1.84 MiB (1%) |        1812 |
| `["collect", "assoc", "basesize=32"]`               | 190.443 ms (5%) |           |   5.64 MiB (1%) |       54020 |
| `["collect", "seq"]`                                | 345.216 ms (5%) |           |   1.50 MiB (1%) |       32784 |
| `["collect", "unordered", "basesize=1"]`            | 461.418 ms (5%) |           |  29.17 MiB (1%) |      404048 |
| `["collect", "unordered", "basesize=1024"]`         | 213.919 ms (5%) |           | 786.03 KiB (1%) |        3398 |
| `["collect", "unordered", "basesize=32"]`           | 217.123 ms (5%) |           |   1.49 MiB (1%) |       18352 |
| `["findfirst", "n=1000", "foldl"]`                  | 560.687 ms (5%) |           |                 |             |
| `["findfirst", "n=1000", "reduce", "basesize=128"]` | 301.972 ms (5%) |           | 564.20 KiB (1%) |       10236 |
| `["findfirst", "n=1000", "reduce", "basesize=256"]` | 298.323 ms (5%) |           | 287.23 KiB (1%) |        5221 |
| `["findfirst", "n=1000", "reduce", "basesize=512"]` | 300.014 ms (5%) |           | 149.36 KiB (1%) |        2724 |
| `["findfirst", "n=400", "foldl"]`                   | 399.774 ms (5%) |           |                 |             |
| `["findfirst", "n=400", "reduce", "basesize=128"]`  | 218.698 ms (5%) |           |   1.02 MiB (1%) |       18971 |
| `["findfirst", "n=400", "reduce", "basesize=256"]`  | 210.418 ms (5%) |           | 526.22 KiB (1%) |        9574 |
| `["findfirst", "n=400", "reduce", "basesize=512"]`  | 201.672 ms (5%) |           | 267.19 KiB (1%) |        4873 |
| `["findfirst", "n=500", "foldl"]`                   |  76.097 ms (5%) |           |                 |             |
| `["findfirst", "n=500", "reduce", "basesize=128"]`  |  35.109 ms (5%) |           | 157.48 KiB (1%) |        2856 |
| `["findfirst", "n=500", "reduce", "basesize=256"]`  |  34.501 ms (5%) |           |  84.58 KiB (1%) |        1535 |
| `["findfirst", "n=500", "reduce", "basesize=512"]`  |  40.690 ms (5%) |           |  48.31 KiB (1%) |         879 |
| `["overhead", "default"]`                           | 176.701 μs (5%) |           | 146.25 KiB (1%) |        2632 |
| `["overhead", "stoppable=false"]`                   | 186.200 μs (5%) |           | 146.28 KiB (1%) |        2633 |
| `["overhead", "stoppable=true"]`                    | 348.501 μs (5%) |           | 146.56 KiB (1%) |        2651 |
| `["parallel_histogram", "assoc", "basesize=16384"]` |   4.028 ms (5%) |           | 732.06 KiB (1%) |         103 |
| `["parallel_histogram", "assoc", "basesize=4096"]`  |   4.894 ms (5%) |           |   1.80 MiB (1%) |         497 |
| `["parallel_histogram", "assoc", "basesize=8192"]`  |   4.415 ms (5%) |           |   1.43 MiB (1%) |         243 |
| `["parallel_histogram", "comm", "basesize=16384"]`  |  12.523 ms (5%) |           |   1.22 MiB (1%) |         159 |
| `["parallel_histogram", "comm", "basesize=4096"]`   |  18.779 ms (5%) |           |   1.05 MiB (1%) |        4669 |
| `["parallel_histogram", "comm", "basesize=8192"]`   |  17.141 ms (5%) |           |   1.23 MiB (1%) |        1029 |
| `["parallel_histogram", "seq"]`                     |   7.111 ms (5%) |           | 364.61 KiB (1%) |          24 |
| `["sum", "random", "foldl"]`                        |  13.039 ms (5%) |           |   64 bytes (1%) |           3 |
| `["sum", "random", "reduce", "basesize=128"]`       |   6.633 ms (5%) |           | 313.41 KiB (1%) |        6070 |
| `["sum", "random", "reduce", "basesize=256"]`       |   6.456 ms (5%) |           | 155.14 KiB (1%) |        3012 |
| `["sum", "random", "reduce", "basesize=512"]`       |   6.957 ms (5%) |           |  76.33 KiB (1%) |        1487 |
| `["sum", "uniform", "foldl"]`                       |  13.258 ms (5%) |           |   64 bytes (1%) |           3 |
| `["sum", "uniform", "reduce", "basesize=128"]`      |   6.944 ms (5%) |           | 313.45 KiB (1%) |        6073 |
| `["sum", "uniform", "reduce", "basesize=256"]`      |   6.835 ms (5%) |           | 155.14 KiB (1%) |        3012 |
| `["sum", "uniform", "reduce", "basesize=512"]`      |   7.024 ms (5%) |           |  76.31 KiB (1%) |        1486 |
| `["sum", "valley", "foldl"]`                        |  13.536 ms (5%) |           |   64 bytes (1%) |           3 |
| `["sum", "valley", "reduce", "basesize=128"]`       |   6.955 ms (5%) |           | 313.33 KiB (1%) |        6065 |
| `["sum", "valley", "reduce", "basesize=256"]`       |   6.687 ms (5%) |           | 155.14 KiB (1%) |        3012 |
| `["sum", "valley", "reduce", "basesize=512"]`       |   7.042 ms (5%) |           |  76.34 KiB (1%) |        1488 |
| `["words", "nthreads=1"]`                           |  33.911 ms (5%) |  7.422 ms |  63.18 MiB (1%) |     2064147 |
| `["words", "nthreads=2"]`                           |  19.006 ms (5%) |           |  64.27 MiB (1%) |     2076416 |
| `["words", "nthreads=4"]`                           |  19.790 ms (5%) |           |  65.21 MiB (1%) |     2086800 |

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
- `["sum", "random"]`
- `["sum", "random", "reduce"]`
- `["sum", "uniform"]`
- `["sum", "uniform", "reduce"]`
- `["sum", "valley"]`
- `["sum", "valley", "reduce"]`
- `["words"]`

## Julia versioninfo
```
Julia Version 1.4.2
Commit 44fa15b150* (2020-05-23 18:35 UTC)
Platform Info:
  OS: Linux (x86_64-pc-linux-gnu)
      Ubuntu 18.04.4 LTS
  uname: Linux 5.3.0-1034-azure #35~18.04.1-Ubuntu SMP Mon Jul 13 12:54:45 UTC 2020 x86_64 x86_64
  CPU: Intel(R) Xeon(R) CPU E5-2673 v4 @ 2.30GHz: 
              speed         user         nice          sys         idle          irq
       #1  2294 MHz      51991 s          0 s       2154 s      15377 s          0 s
       #2  2294 MHz      48848 s          0 s       2784 s      17717 s          0 s
       
  Memory: 6.764881134033203 GB (2978.6171875 MB free)
  Uptime: 717.0 sec
  Load Avg:  1.74609375  1.58984375  0.97412109375
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-8.0.1 (ORCJIT, broadwell)
```

---
# Baseline result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmark: 9 Aug 2020 - 0:59
* Package commit: f87cd6
* Julia commit: 44fa15
* Julia command flags: None
* Environment variables: `JULIA_NUM_THREADS => 2`

## Results
Below is a table of this job's results, obtained by running the benchmarks.
The values listed in the `ID` column have the structure `[parent_group, child_group, ..., key]`, and can be used to
index into the BaseBenchmarks suite to retrieve the corresponding benchmarks.
The percentages accompanying time and memory values in the below table are noise tolerances. The "true"
time/memory value for a given benchmark is expected to fall within this percentage of the reported value.
An empty cell means that the value was zero.

| ID                                                  | time            | GC time   | memory          | allocations |
|-----------------------------------------------------|----------------:|----------:|----------------:|------------:|
| `["collect", "assoc", "basesize=1"]`                | 334.912 ms (5%) | 13.354 ms |  87.55 MiB (1%) |     1590642 |
| `["collect", "assoc", "basesize=1024"]`             | 171.355 ms (5%) |           |   1.84 MiB (1%) |        1810 |
| `["collect", "assoc", "basesize=32"]`               | 179.030 ms (5%) |           |   5.64 MiB (1%) |       54018 |
| `["collect", "seq"]`                                | 341.819 ms (5%) |           |   1.50 MiB (1%) |       32784 |
| `["collect", "unordered", "basesize=1"]`            | 439.234 ms (5%) |           |  29.21 MiB (1%) |      406326 |
| `["collect", "unordered", "basesize=1024"]`         | 194.770 ms (5%) |           | 776.08 KiB (1%) |        2425 |
| `["collect", "unordered", "basesize=32"]`           | 201.062 ms (5%) |           |   1.50 MiB (1%) |       18353 |
| `["findfirst", "n=1000", "foldl"]`                  | 581.315 ms (5%) |           |                 |             |
| `["findfirst", "n=1000", "reduce", "basesize=128"]` | 285.057 ms (5%) |           | 564.20 KiB (1%) |       10236 |
| `["findfirst", "n=1000", "reduce", "basesize=256"]` | 261.131 ms (5%) |           | 287.30 KiB (1%) |        5225 |
| `["findfirst", "n=1000", "reduce", "basesize=512"]` | 279.874 ms (5%) |           | 149.34 KiB (1%) |        2723 |
| `["findfirst", "n=400", "foldl"]`                   | 413.412 ms (5%) |           |                 |             |
| `["findfirst", "n=400", "reduce", "basesize=128"]`  | 231.317 ms (5%) |           |   1.02 MiB (1%) |       18975 |
| `["findfirst", "n=400", "reduce", "basesize=256"]`  | 199.072 ms (5%) |           | 526.17 KiB (1%) |        9571 |
| `["findfirst", "n=400", "reduce", "basesize=512"]`  | 196.634 ms (5%) |           | 267.27 KiB (1%) |        4878 |
| `["findfirst", "n=500", "foldl"]`                   |  65.133 ms (5%) |           |                 |             |
| `["findfirst", "n=500", "reduce", "basesize=128"]`  |  37.670 ms (5%) |           | 157.45 KiB (1%) |        2854 |
| `["findfirst", "n=500", "reduce", "basesize=256"]`  |  36.035 ms (5%) |           |  84.61 KiB (1%) |        1537 |
| `["findfirst", "n=500", "reduce", "basesize=512"]`  |  35.331 ms (5%) |           |  48.31 KiB (1%) |         879 |
| `["overhead", "default"]`                           | 164.201 μs (5%) |           | 146.23 KiB (1%) |        2631 |
| `["overhead", "stoppable=false"]`                   | 164.700 μs (5%) |           | 146.28 KiB (1%) |        2633 |
| `["overhead", "stoppable=true"]`                    | 327.501 μs (5%) |           | 146.53 KiB (1%) |        2649 |
| `["parallel_histogram", "assoc", "basesize=16384"]` |   3.453 ms (5%) |           | 732.06 KiB (1%) |         103 |
| `["parallel_histogram", "assoc", "basesize=4096"]`  |   4.611 ms (5%) |           |   2.07 MiB (1%) |         503 |
| `["parallel_histogram", "assoc", "basesize=8192"]`  |   4.146 ms (5%) |           |   1.43 MiB (1%) |         243 |
| `["parallel_histogram", "comm", "basesize=16384"]`  |  13.459 ms (5%) |           |   1.22 MiB (1%) |         159 |
| `["parallel_histogram", "comm", "basesize=4096"]`   |  21.313 ms (5%) |           |   1.03 MiB (1%) |        3927 |
| `["parallel_histogram", "comm", "basesize=8192"]`   |  19.291 ms (5%) |           |   1.26 MiB (1%) |        2494 |
| `["parallel_histogram", "seq"]`                     |   6.884 ms (5%) |           | 364.61 KiB (1%) |          24 |
| `["sum", "random", "foldl"]`                        |  12.854 ms (5%) |           |   64 bytes (1%) |           3 |
| `["sum", "random", "reduce", "basesize=128"]`       |   7.193 ms (5%) |           | 313.38 KiB (1%) |        6068 |
| `["sum", "random", "reduce", "basesize=256"]`       |   6.614 ms (5%) |           | 155.17 KiB (1%) |        3014 |
| `["sum", "random", "reduce", "basesize=512"]`       |   7.029 ms (5%) |           |  76.33 KiB (1%) |        1487 |
| `["sum", "uniform", "foldl"]`                       |  12.940 ms (5%) |           |   64 bytes (1%) |           3 |
| `["sum", "uniform", "reduce", "basesize=128"]`      |   6.932 ms (5%) |           | 313.42 KiB (1%) |        6071 |
| `["sum", "uniform", "reduce", "basesize=256"]`      |   6.500 ms (5%) |           | 155.16 KiB (1%) |        3013 |
| `["sum", "uniform", "reduce", "basesize=512"]`      |   6.542 ms (5%) |           |  76.31 KiB (1%) |        1486 |
| `["sum", "valley", "foldl"]`                        |  13.425 ms (5%) |           |   64 bytes (1%) |           3 |
| `["sum", "valley", "reduce", "basesize=128"]`       |   7.678 ms (5%) |           | 313.34 KiB (1%) |        6066 |
| `["sum", "valley", "reduce", "basesize=256"]`       |   6.440 ms (5%) |           | 155.14 KiB (1%) |        3012 |
| `["sum", "valley", "reduce", "basesize=512"]`       |   6.156 ms (5%) |           |  76.33 KiB (1%) |        1487 |
| `["words", "nthreads=1"]`                           |  40.615 ms (5%) |  8.694 ms |  63.14 MiB (1%) |     2062861 |
| `["words", "nthreads=2"]`                           |  20.437 ms (5%) |           |  64.23 MiB (1%) |     2075131 |
| `["words", "nthreads=4"]`                           |  20.224 ms (5%) |           |  65.17 MiB (1%) |     2085533 |

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
- `["sum", "random"]`
- `["sum", "random", "reduce"]`
- `["sum", "uniform"]`
- `["sum", "uniform", "reduce"]`
- `["sum", "valley"]`
- `["sum", "valley", "reduce"]`
- `["words"]`

## Julia versioninfo
```
Julia Version 1.4.2
Commit 44fa15b150* (2020-05-23 18:35 UTC)
Platform Info:
  OS: Linux (x86_64-pc-linux-gnu)
      Ubuntu 18.04.4 LTS
  uname: Linux 5.3.0-1034-azure #35~18.04.1-Ubuntu SMP Mon Jul 13 12:54:45 UTC 2020 x86_64 x86_64
  CPU: Intel(R) Xeon(R) CPU E5-2673 v4 @ 2.30GHz: 
              speed         user         nice          sys         idle          irq
       #1  2294 MHz      72453 s          0 s       2956 s      27081 s          0 s
       #2  2294 MHz      77052 s          0 s       3416 s      21837 s          0 s
       
  Memory: 6.764881134033203 GB (2960.5234375 MB free)
  Uptime: 1048.0 sec
  Load Avg:  1.68798828125  1.5810546875  1.14892578125
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-8.0.1 (ORCJIT, broadwell)
```

---
# Runtime information
| Runtime Info | |
|:--|:--|
| BLAS #threads | 2 |
| `BLAS.vendor()` | `openblas64` |
| `Sys.CPU_THREADS` | 2 |

`lscpu` output:

    Architecture:        x86_64
    CPU op-mode(s):      32-bit, 64-bit
    Byte Order:          Little Endian
    CPU(s):              2
    On-line CPU(s) list: 0,1
    Thread(s) per core:  1
    Core(s) per socket:  2
    Socket(s):           1
    NUMA node(s):        1
    Vendor ID:           GenuineIntel
    CPU family:          6
    Model:               79
    Model name:          Intel(R) Xeon(R) CPU E5-2673 v4 @ 2.30GHz
    Stepping:            1
    CPU MHz:             2294.685
    BogoMIPS:            4589.37
    Hypervisor vendor:   Microsoft
    Virtualization type: full
    L1d cache:           32K
    L1i cache:           32K
    L2 cache:            256K
    L3 cache:            51200K
    NUMA node0 CPU(s):   0,1
    Flags:               fpu vme de pse tsc msr pae mce cx8 apic sep mtrr pge mca cmov pat pse36 clflush mmx fxsr sse sse2 ss ht syscall nx pdpe1gb rdtscp lm constant_tsc rep_good nopl xtopology cpuid pni pclmulqdq ssse3 fma cx16 pcid sse4_1 sse4_2 movbe popcnt aes xsave avx f16c rdrand hypervisor lahf_lm abm 3dnowprefetch invpcid_single pti fsgsbase bmi1 hle avx2 smep bmi2 erms invpcid rtm rdseed adx smap xsaveopt md_clear
    

| Cpu Property       | Value                                                   |
|:------------------ |:------------------------------------------------------- |
| Brand              | Intel(R) Xeon(R) CPU E5-2673 v4 @ 2.30GHz               |
| Vendor             | :Intel                                                  |
| Architecture       | :Broadwell                                              |
| Model              | Family: 0x06, Model: 0x4f, Stepping: 0x01, Type: 0x00   |
| Cores              | 2 physical cores, 2 logical cores (on executing CPU)    |
|                    | No Hyperthreading detected                              |
| Clock Frequencies  | Not supported by CPU                                    |
| Data Cache         | Level 1:3 : (32, 256, 51200) kbytes                     |
|                    | 64 byte cache line size                                 |
| Address Size       | 48 bits virtual, 44 bits physical                       |
| SIMD               | 256 bit = 32 byte max. SIMD vector size                 |
| Time Stamp Counter | TSC is accessible via `rdtsc`                           |
|                    | TSC increased at every clock cycle (non-invariant TSC)  |
| Perf. Monitoring   | Performance Monitoring Counters (PMC) are not supported |
| Hypervisor         | Yes, Microsoft                                          |

