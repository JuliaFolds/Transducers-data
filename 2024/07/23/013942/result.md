# Multi-thread benchmark result

* Pull request commit: [`4d531ef8f05742afc992c6eef778d2795e4ec338`](https://github.com/JuliaFolds/Transducers.jl/commit/4d531ef8f05742afc992c6eef778d2795e4ec338)
* Pull request: <https://github.com/JuliaFolds/Transducers.jl/pull/243> (Update */Manifest.toml)

# Judge result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmarks:
    - Target: 23 Jul 2024 - 01:34
    - Baseline: 23 Jul 2024 - 01:39
* Package commits:
    - Target: e33259
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
| `["findfirst", "n=1000", "reduce", "basesize=128"]` |                1.90 (5%) :x: |                1.79 (1%) :x: |
| `["findfirst", "n=1000", "reduce", "basesize=256"]` | 0.85 (5%) :white_check_mark: | 0.91 (1%) :white_check_mark: |
| `["findfirst", "n=1000", "reduce", "basesize=512"]` | 0.87 (5%) :white_check_mark: | 0.89 (1%) :white_check_mark: |
| `["findfirst", "n=400", "reduce", "basesize=128"]`  | 0.88 (5%) :white_check_mark: | 0.87 (1%) :white_check_mark: |
| `["findfirst", "n=400", "reduce", "basesize=512"]`  |                   1.05 (5%)  | 0.96 (1%) :white_check_mark: |
| `["findfirst", "n=500", "reduce", "basesize=128"]`  | 0.50 (5%) :white_check_mark: | 0.60 (1%) :white_check_mark: |
| `["findfirst", "n=500", "reduce", "basesize=256"]`  |                1.08 (5%) :x: |                1.24 (1%) :x: |
| `["findfirst", "n=500", "reduce", "basesize=512"]`  |                1.10 (5%) :x: |                1.05 (1%) :x: |
| `["parallel_histogram", "assoc", "basesize=4096"]`  |                   0.97 (5%)  | 0.87 (1%) :white_check_mark: |
| `["parallel_histogram", "comm", "basesize=4096"]`   |                   0.96 (5%)  | 0.88 (1%) :white_check_mark: |
| `["splitby", "count", "foldl"]`                     |                1.12 (5%) :x: |                   1.00 (1%)  |
| `["words", "nthreads=2"]`                           | 0.90 (5%) :white_check_mark: | 0.99 (1%) :white_check_mark: |
| `["words", "nthreads=4"]`                           | 0.94 (5%) :white_check_mark: |                   1.00 (1%)  |

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
  uname: Linux 6.5.0-1023-azure #24~22.04.1-Ubuntu SMP Wed Jun 12 19:55:26 UTC 2024 x86_64 x86_64
  CPU: AMD EPYC 7763 64-Core Processor: 
              speed         user         nice          sys         idle          irq
       #1  2445 MHz       2439 s          0 s        155 s       4442 s          0 s
       #2  3243 MHz       2948 s          0 s        162 s       3941 s          0 s
       #3  2643 MHz       2419 s          0 s        166 s       4460 s          0 s
       #4  2884 MHz       2213 s          0 s        180 s       4639 s          0 s
       
  Memory: 15.606491088867188 GB (12448.8125 MB free)
  Uptime: 708.18 sec
  Load Avg:  1.7  1.52  0.9
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
  uname: Linux 6.5.0-1023-azure #24~22.04.1-Ubuntu SMP Wed Jun 12 19:55:26 UTC 2024 x86_64 x86_64
  CPU: AMD EPYC 7763 64-Core Processor: 
              speed         user         nice          sys         idle          irq
       #1  3243 MHz       3471 s          0 s        208 s       6294 s          0 s
       #2  2445 MHz       3830 s          0 s        219 s       5938 s          0 s
       #3  2445 MHz       3648 s          0 s        214 s       6123 s          0 s
       #4  2592 MHz       3695 s          0 s        230 s       6050 s          0 s
       
  Memory: 15.606491088867188 GB (12487.734375 MB free)
  Uptime: 1002.81 sec
  Load Avg:  1.79  1.68  1.14
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-12.0.1 (ORCJIT, znver3)
```

---
# Target result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmark: 23 Jul 2024 - 1:34
* Package commit: e33259
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
| `["collect", "assoc", "basesize=1"]`                | 148.661 ms (5%) |         |   4.36 MiB (1%) |       32800 |
| `["collect", "assoc", "basesize=1024"]`             | 147.417 ms (5%) |         |   1.09 MiB (1%) |          53 |
| `["collect", "assoc", "basesize=32"]`               | 147.567 ms (5%) |         |   1.48 MiB (1%) |        1052 |
| `["collect", "seq"]`                                | 294.559 ms (5%) |         | 256.05 KiB (1%) |           2 |
| `["collect", "unordered", "basesize=1"]`            | 247.193 ms (5%) |         |  23.82 MiB (1%) |      410217 |
| `["collect", "unordered", "basesize=1024"]`         | 156.317 ms (5%) |         |   1.01 MiB (1%) |        1036 |
| `["collect", "unordered", "basesize=32"]`           | 163.652 ms (5%) |         |   1.60 MiB (1%) |       15227 |
| `["findfirst", "n=1000", "foldl"]`                  | 505.289 ms (5%) |         |                 |             |
| `["findfirst", "n=1000", "reduce", "basesize=128"]` | 526.253 ms (5%) |         | 416.02 KiB (1%) |        5893 |
| `["findfirst", "n=1000", "reduce", "basesize=256"]` | 339.045 ms (5%) |         | 157.20 KiB (1%) |        2193 |
| `["findfirst", "n=1000", "reduce", "basesize=512"]` | 395.035 ms (5%) |         |  96.75 KiB (1%) |        1346 |
| `["findfirst", "n=400", "foldl"]`                   | 379.720 ms (5%) |         |                 |             |
| `["findfirst", "n=400", "reduce", "basesize=128"]`  | 200.798 ms (5%) |         | 394.50 KiB (1%) |        5612 |
| `["findfirst", "n=400", "reduce", "basesize=256"]`  | 198.641 ms (5%) |         | 200.83 KiB (1%) |        2872 |
| `["findfirst", "n=400", "reduce", "basesize=512"]`  | 241.674 ms (5%) |         | 129.00 KiB (1%) |        1844 |
| `["findfirst", "n=500", "foldl"]`                   |  65.016 ms (5%) |         |                 |             |
| `["findfirst", "n=500", "reduce", "basesize=128"]`  |  56.874 ms (5%) |         | 137.20 KiB (1%) |        1852 |
| `["findfirst", "n=500", "reduce", "basesize=256"]`  | 140.210 ms (5%) |         | 154.94 KiB (1%) |        2098 |
| `["findfirst", "n=500", "reduce", "basesize=512"]`  |  94.042 ms (5%) |         |  59.84 KiB (1%) |         819 |
| `["overhead", "default"]`                           |  51.997 μs (5%) |         |  32.77 KiB (1%) |         419 |
| `["overhead", "stoppable=false"]`                   |  51.576 μs (5%) |         |  32.81 KiB (1%) |         420 |
| `["overhead", "stoppable=true"]`                    |  57.687 μs (5%) |         |  44.25 KiB (1%) |         610 |
| `["parallel_histogram", "assoc", "basesize=16384"]` |   2.377 ms (5%) |         | 728.91 KiB (1%) |          57 |
| `["parallel_histogram", "assoc", "basesize=4096"]`  |   2.934 ms (5%) |         |   1.79 MiB (1%) |         216 |
| `["parallel_histogram", "assoc", "basesize=8192"]`  |   2.658 ms (5%) |         |   1.42 MiB (1%) |         117 |
| `["parallel_histogram", "comm", "basesize=16384"]`  |   8.539 ms (5%) |         |   1.58 MiB (1%) |        2591 |
| `["parallel_histogram", "comm", "basesize=4096"]`   |  13.556 ms (5%) |         |   1.17 MiB (1%) |        4591 |
| `["parallel_histogram", "comm", "basesize=8192"]`   |  12.079 ms (5%) |         |   1.27 MiB (1%) |        7030 |
| `["parallel_histogram", "seq"]`                     |   4.234 ms (5%) |         | 364.16 KiB (1%) |          24 |
| `["partition_length_maximum", "rand", "foldl"]`     |  31.125 ms (5%) |         |                 |             |
| `["partition_length_maximum", "rand", "reduce"]`    |  15.607 ms (5%) |         |  736 bytes (1%) |          11 |
| `["splitby", "count", "foldl"]`                     |   1.735 ms (5%) |         |                 |             |
| `["splitby", "count", "man"]`                       |   1.133 ms (5%) |         |                 |             |
| `["splitby", "count", "reduce"]`                    | 726.285 μs (5%) |         |   1.09 KiB (1%) |          19 |
| `["sum", "random", "foldl"]`                        |  11.081 ms (5%) |         |                 |             |
| `["sum", "random", "reduce", "basesize=128"]`       |   5.684 ms (5%) |         |  74.14 KiB (1%) |        1103 |
| `["sum", "random", "reduce", "basesize=256"]`       |   5.618 ms (5%) |         |  36.77 KiB (1%) |         547 |
| `["sum", "random", "reduce", "basesize=512"]`       |   5.578 ms (5%) |         |  18.08 KiB (1%) |         269 |
| `["sum", "uniform", "foldl"]`                       |  10.867 ms (5%) |         |                 |             |
| `["sum", "uniform", "reduce", "basesize=128"]`      |   5.579 ms (5%) |         |  74.17 KiB (1%) |        1104 |
| `["sum", "uniform", "reduce", "basesize=256"]`      |   5.521 ms (5%) |         |  36.70 KiB (1%) |         545 |
| `["sum", "uniform", "reduce", "basesize=512"]`      |   5.473 ms (5%) |         |  18.03 KiB (1%) |         268 |
| `["sum", "valley", "foldl"]`                        |  11.113 ms (5%) |         |                 |             |
| `["sum", "valley", "reduce", "basesize=128"]`       |   5.697 ms (5%) |         |  73.98 KiB (1%) |        1098 |
| `["sum", "valley", "reduce", "basesize=256"]`       |   5.632 ms (5%) |         |  36.70 KiB (1%) |         545 |
| `["sum", "valley", "reduce", "basesize=512"]`       |   5.597 ms (5%) |         |  18.06 KiB (1%) |         269 |
| `["words", "nthreads=1"]`                           |  14.516 ms (5%) |         |  31.65 MiB (1%) |     1031132 |
| `["words", "nthreads=2"]`                           |   9.124 ms (5%) |         |  32.01 MiB (1%) |     1031172 |
| `["words", "nthreads=4"]`                           |   9.728 ms (5%) |         |  32.90 MiB (1%) |     1031318 |

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
  uname: Linux 6.5.0-1023-azure #24~22.04.1-Ubuntu SMP Wed Jun 12 19:55:26 UTC 2024 x86_64 x86_64
  CPU: AMD EPYC 7763 64-Core Processor: 
              speed         user         nice          sys         idle          irq
       #1  2445 MHz       2439 s          0 s        155 s       4442 s          0 s
       #2  3243 MHz       2948 s          0 s        162 s       3941 s          0 s
       #3  2643 MHz       2419 s          0 s        166 s       4460 s          0 s
       #4  2884 MHz       2213 s          0 s        180 s       4639 s          0 s
       
  Memory: 15.606491088867188 GB (12448.8125 MB free)
  Uptime: 708.18 sec
  Load Avg:  1.7  1.52  0.9
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-12.0.1 (ORCJIT, znver3)
```

---
# Baseline result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmark: 23 Jul 2024 - 1:39
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
| `["collect", "assoc", "basesize=1"]`                | 149.001 ms (5%) |         |   4.36 MiB (1%) |       32800 |
| `["collect", "assoc", "basesize=1024"]`             | 147.605 ms (5%) |         |   1.09 MiB (1%) |          53 |
| `["collect", "assoc", "basesize=32"]`               | 147.564 ms (5%) |         |   1.48 MiB (1%) |        1052 |
| `["collect", "seq"]`                                | 294.649 ms (5%) |         | 256.05 KiB (1%) |           2 |
| `["collect", "unordered", "basesize=1"]`            | 245.890 ms (5%) |         |  23.85 MiB (1%) |      411470 |
| `["collect", "unordered", "basesize=1024"]`         | 156.332 ms (5%) |         |   1.01 MiB (1%) |        1055 |
| `["collect", "unordered", "basesize=32"]`           | 163.207 ms (5%) |         |   1.60 MiB (1%) |       15265 |
| `["findfirst", "n=1000", "foldl"]`                  | 506.880 ms (5%) |         |                 |             |
| `["findfirst", "n=1000", "reduce", "basesize=128"]` | 276.304 ms (5%) |         | 232.73 KiB (1%) |        3272 |
| `["findfirst", "n=1000", "reduce", "basesize=256"]` | 397.066 ms (5%) |         | 173.20 KiB (1%) |        2435 |
| `["findfirst", "n=1000", "reduce", "basesize=512"]` | 453.427 ms (5%) |         | 108.55 KiB (1%) |        1509 |
| `["findfirst", "n=400", "foldl"]`                   | 379.204 ms (5%) |         |                 |             |
| `["findfirst", "n=400", "reduce", "basesize=128"]`  | 228.796 ms (5%) |         | 454.31 KiB (1%) |        6428 |
| `["findfirst", "n=400", "reduce", "basesize=256"]`  | 198.680 ms (5%) |         | 200.98 KiB (1%) |        2877 |
| `["findfirst", "n=400", "reduce", "basesize=512"]`  | 230.931 ms (5%) |         | 135.05 KiB (1%) |        1919 |
| `["findfirst", "n=500", "foldl"]`                   |  65.222 ms (5%) |         |                 |             |
| `["findfirst", "n=500", "reduce", "basesize=128"]`  | 114.365 ms (5%) |         | 228.78 KiB (1%) |        3120 |
| `["findfirst", "n=500", "reduce", "basesize=256"]`  | 129.842 ms (5%) |         | 125.02 KiB (1%) |        1736 |
| `["findfirst", "n=500", "reduce", "basesize=512"]`  |  85.271 ms (5%) |         |  56.91 KiB (1%) |         779 |
| `["overhead", "default"]`                           |  53.029 μs (5%) |         |  32.73 KiB (1%) |         418 |
| `["overhead", "stoppable=false"]`                   |  52.157 μs (5%) |         |  32.75 KiB (1%) |         418 |
| `["overhead", "stoppable=true"]`                    |  58.940 μs (5%) |         |  44.25 KiB (1%) |         610 |
| `["parallel_histogram", "assoc", "basesize=16384"]` |   2.385 ms (5%) |         | 728.91 KiB (1%) |          57 |
| `["parallel_histogram", "assoc", "basesize=4096"]`  |   3.019 ms (5%) |         |   2.05 MiB (1%) |         222 |
| `["parallel_histogram", "assoc", "basesize=8192"]`  |   2.663 ms (5%) |         |   1.42 MiB (1%) |         117 |
| `["parallel_histogram", "comm", "basesize=16384"]`  |   8.708 ms (5%) |         |   1.59 MiB (1%) |        2779 |
| `["parallel_histogram", "comm", "basesize=4096"]`   |  14.105 ms (5%) |         |   1.33 MiB (1%) |        9690 |
| `["parallel_histogram", "comm", "basesize=8192"]`   |  12.280 ms (5%) |         |   1.28 MiB (1%) |        6682 |
| `["parallel_histogram", "seq"]`                     |   4.240 ms (5%) |         | 364.16 KiB (1%) |          24 |
| `["partition_length_maximum", "rand", "foldl"]`     |  31.117 ms (5%) |         |                 |             |
| `["partition_length_maximum", "rand", "reduce"]`    |  15.587 ms (5%) |         |  736 bytes (1%) |          11 |
| `["splitby", "count", "foldl"]`                     |   1.544 ms (5%) |         |                 |             |
| `["splitby", "count", "man"]`                       |   1.157 ms (5%) |         |                 |             |
| `["splitby", "count", "reduce"]`                    | 723.701 μs (5%) |         |   1.09 KiB (1%) |          19 |
| `["sum", "random", "foldl"]`                        |  11.024 ms (5%) |         |                 |             |
| `["sum", "random", "reduce", "basesize=128"]`       |   5.624 ms (5%) |         |  74.20 KiB (1%) |        1105 |
| `["sum", "random", "reduce", "basesize=256"]`       |   5.585 ms (5%) |         |  36.67 KiB (1%) |         544 |
| `["sum", "random", "reduce", "basesize=512"]`       |   5.550 ms (5%) |         |  18.11 KiB (1%) |         270 |
| `["sum", "uniform", "foldl"]`                       |  10.867 ms (5%) |         |                 |             |
| `["sum", "uniform", "reduce", "basesize=128"]`      |   5.572 ms (5%) |         |  74.08 KiB (1%) |        1101 |
| `["sum", "uniform", "reduce", "basesize=256"]`      |   5.524 ms (5%) |         |  36.73 KiB (1%) |         546 |
| `["sum", "uniform", "reduce", "basesize=512"]`      |   5.490 ms (5%) |         |  18.00 KiB (1%) |         267 |
| `["sum", "valley", "foldl"]`                        |  11.114 ms (5%) |         |                 |             |
| `["sum", "valley", "reduce", "basesize=128"]`       |   5.702 ms (5%) |         |  74.08 KiB (1%) |        1101 |
| `["sum", "valley", "reduce", "basesize=256"]`       |   5.636 ms (5%) |         |  36.70 KiB (1%) |         545 |
| `["sum", "valley", "reduce", "basesize=512"]`       |   5.608 ms (5%) |         |  18.06 KiB (1%) |         269 |
| `["words", "nthreads=1"]`                           |  14.506 ms (5%) |         |  31.70 MiB (1%) |     1033015 |
| `["words", "nthreads=2"]`                           |  10.116 ms (5%) |         |  32.41 MiB (1%) |     1033125 |
| `["words", "nthreads=4"]`                           |  10.346 ms (5%) |         |  32.86 MiB (1%) |     1033193 |

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
  uname: Linux 6.5.0-1023-azure #24~22.04.1-Ubuntu SMP Wed Jun 12 19:55:26 UTC 2024 x86_64 x86_64
  CPU: AMD EPYC 7763 64-Core Processor: 
              speed         user         nice          sys         idle          irq
       #1  3243 MHz       3471 s          0 s        208 s       6294 s          0 s
       #2  2445 MHz       3830 s          0 s        219 s       5938 s          0 s
       #3  2445 MHz       3648 s          0 s        214 s       6123 s          0 s
       #4  2592 MHz       3695 s          0 s        230 s       6050 s          0 s
       
  Memory: 15.606491088867188 GB (12487.734375 MB free)
  Uptime: 1002.81 sec
  Load Avg:  1.79  1.68  1.14
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
    Vulnerability Spec rstack overflow: Vulnerable: Safe RET, no microcode
    Vulnerability Spec store bypass:    Vulnerable
    Vulnerability Spectre v1:           Mitigation; usercopy/swapgs barriers and __user pointer sanitization
    Vulnerability Spectre v2:           Mitigation; Retpolines; STIBP disabled; RSB filling; PBRSB-eIBRS Not affected; BHI Not affected
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

