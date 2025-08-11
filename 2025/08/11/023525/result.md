# Multi-thread benchmark result

* Pull request commit: [`5270508911c0aee825323df32b95857b5615b225`](https://github.com/JuliaFolds/Transducers.jl/commit/5270508911c0aee825323df32b95857b5615b225)
* Pull request: <https://github.com/JuliaFolds/Transducers.jl/pull/243> (Update */Manifest.toml)

# Judge result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmarks:
    - Target: 11 Aug 2025 - 02:29
    - Baseline: 11 Aug 2025 - 02:34
* Package commits:
    - Target: 05c6557
    - Baseline: 2a51f8d
* Julia commits:
    - Target: 742b9ab
    - Baseline: 742b9ab
* Julia command flags:
    - Target: None
    - Baseline: None
* Environment variables:
    - Target: `JULIA_NUM_THREADS => 2`
    - Baseline: `JULIA_NUM_THREADS => 2`

## Results
A ratio greater than `1.0` denotes a possible regression (marked with :x:), while a ratio less
than `1.0` denotes a possible improvement (marked with :white_check_mark:). Brackets display [tolerances](https://juliaci.github.io/BenchmarkTools.jl/stable/manual/#Benchmark-Parameters) for the benchmark estimates. Only significant results - results
that indicate possible regressions or improvements - are shown below (thus, an empty table means that all
benchmark results remained invariant between builds).

| ID                                                  | time ratio                   | memory ratio                 |
|-----------------------------------------------------|------------------------------|------------------------------|
| `["findfirst", "n=1000", "reduce", "basesize=512"]` | 0.77 (5%) :white_check_mark: | 0.75 (1%) :white_check_mark: |
| `["findfirst", "n=400", "reduce", "basesize=128"]`  |                   1.01 (5%)  |                1.04 (1%) :x: |
| `["findfirst", "n=400", "reduce", "basesize=512"]`  | 0.93 (5%) :white_check_mark: |                1.06 (1%) :x: |
| `["findfirst", "n=500", "reduce", "basesize=128"]`  | 0.62 (5%) :white_check_mark: | 0.70 (1%) :white_check_mark: |
| `["findfirst", "n=500", "reduce", "basesize=256"]`  |                1.79 (5%) :x: |                1.20 (1%) :x: |
| `["findfirst", "n=500", "reduce", "basesize=512"]`  |                1.09 (5%) :x: |                1.05 (1%) :x: |
| `["overhead", "stoppable=true"]`                    |                1.07 (5%) :x: |                   1.00 (1%)  |
| `["parallel_histogram", "assoc", "basesize=4096"]`  |                   1.03 (5%)  |                1.15 (1%) :x: |
| `["parallel_histogram", "comm", "basesize=4096"]`   |                1.07 (5%) :x: |                1.03 (1%) :x: |
| `["parallel_histogram", "comm", "basesize=8192"]`   |                   0.97 (5%)  |                1.02 (1%) :x: |
| `["splitby", "count", "reduce"]`                    |                1.19 (5%) :x: | 0.97 (1%) :white_check_mark: |

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
      Ubuntu 24.04.2 LTS
  uname: Linux 6.11.0-1018-azure #18~24.04.1-Ubuntu SMP Sat Jun 28 04:46:03 UTC 2025 x86_64 x86_64
  CPU: AMD EPYC 7763 64-Core Processor: 
              speed         user         nice          sys         idle          irq
       #1  3246 MHz       2378 s          0 s        174 s       4699 s          0 s
       #2  3244 MHz       2612 s          0 s        191 s       4453 s          0 s
       #3  3175 MHz       2377 s          0 s        182 s       4702 s          0 s
       #4  3242 MHz       2736 s          0 s        181 s       4336 s          0 s
       
  Memory: 15.620681762695312 GB (12449.03125 MB free)
  Uptime: 728.23 sec
  Load Avg:  1.59  1.49  0.9
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
      Ubuntu 24.04.2 LTS
  uname: Linux 6.11.0-1018-azure #18~24.04.1-Ubuntu SMP Sat Jun 28 04:46:03 UTC 2025 x86_64 x86_64
  CPU: AMD EPYC 7763 64-Core Processor: 
              speed         user         nice          sys         idle          irq
       #1  3250 MHz       3686 s          0 s        260 s       6432 s          0 s
       #2  3245 MHz       3709 s          0 s        280 s       6394 s          0 s
       #3  3242 MHz       3621 s          0 s        240 s       6527 s          0 s
       #4  3251 MHz       3918 s          0 s        231 s       6232 s          0 s
       
  Memory: 15.620681762695312 GB (12402.76171875 MB free)
  Uptime: 1041.38 sec
  Load Avg:  1.6  1.58  1.12
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-12.0.1 (ORCJIT, znver3)
```

---
# Target result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmark: 11 Aug 2025 - 02:29
* Package commit: 05c6557
* Julia commit: 742b9ab
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
| `["collect", "assoc", "basesize=1"]`                | 149.340 ms (5%) |         |   4.36 MiB (1%) |       32800 |
| `["collect", "assoc", "basesize=1024"]`             | 148.174 ms (5%) |         |   1.09 MiB (1%) |          53 |
| `["collect", "assoc", "basesize=32"]`               | 148.320 ms (5%) |         |   1.48 MiB (1%) |        1053 |
| `["collect", "seq"]`                                | 296.049 ms (5%) |         | 256.05 KiB (1%) |           2 |
| `["collect", "unordered", "basesize=1"]`            | 257.973 ms (5%) |         |  23.67 MiB (1%) |      405394 |
| `["collect", "unordered", "basesize=1024"]`         | 158.155 ms (5%) |         |   1.01 MiB (1%) |        1003 |
| `["collect", "unordered", "basesize=32"]`           | 168.773 ms (5%) |         |   1.60 MiB (1%) |       15332 |
| `["findfirst", "n=1000", "foldl"]`                  | 507.305 ms (5%) |         |                 |             |
| `["findfirst", "n=1000", "reduce", "basesize=128"]` | 276.358 ms (5%) |         | 232.67 KiB (1%) |        3270 |
| `["findfirst", "n=1000", "reduce", "basesize=256"]` | 384.356 ms (5%) |         | 170.27 KiB (1%) |        2375 |
| `["findfirst", "n=1000", "reduce", "basesize=512"]` | 347.459 ms (5%) |         |  81.33 KiB (1%) |        1146 |
| `["findfirst", "n=400", "foldl"]`                   | 379.683 ms (5%) |         |                 |             |
| `["findfirst", "n=400", "reduce", "basesize=128"]`  | 197.443 ms (5%) |         | 397.33 KiB (1%) |        5634 |
| `["findfirst", "n=400", "reduce", "basesize=256"]`  | 198.654 ms (5%) |         | 201.17 KiB (1%) |        2883 |
| `["findfirst", "n=400", "reduce", "basesize=512"]`  | 257.944 ms (5%) |         | 148.95 KiB (1%) |        2092 |
| `["findfirst", "n=500", "foldl"]`                   |  65.910 ms (5%) |         |                 |             |
| `["findfirst", "n=500", "reduce", "basesize=128"]`  |  90.902 ms (5%) |         | 175.77 KiB (1%) |        2420 |
| `["findfirst", "n=500", "reduce", "basesize=256"]`  | 149.952 ms (5%) |         | 139.00 KiB (1%) |        1949 |
| `["findfirst", "n=500", "reduce", "basesize=512"]`  |  92.939 ms (5%) |         |  59.77 KiB (1%) |         816 |
| `["overhead", "default"]`                           |  51.175 μs (5%) |         |  32.73 KiB (1%) |         418 |
| `["overhead", "stoppable=false"]`                   |  52.468 μs (5%) |         |  32.75 KiB (1%) |         418 |
| `["overhead", "stoppable=true"]`                    |  60.673 μs (5%) |         |  44.25 KiB (1%) |         610 |
| `["parallel_histogram", "assoc", "basesize=16384"]` |   2.394 ms (5%) |         | 728.91 KiB (1%) |          57 |
| `["parallel_histogram", "assoc", "basesize=4096"]`  |   3.033 ms (5%) |         |   2.05 MiB (1%) |         222 |
| `["parallel_histogram", "assoc", "basesize=8192"]`  |   2.674 ms (5%) |         |   1.42 MiB (1%) |         117 |
| `["parallel_histogram", "comm", "basesize=16384"]`  |   8.094 ms (5%) |         |   1.56 MiB (1%) |        1808 |
| `["parallel_histogram", "comm", "basesize=4096"]`   |  13.653 ms (5%) |         |   1.33 MiB (1%) |        9890 |
| `["parallel_histogram", "comm", "basesize=8192"]`   |  11.820 ms (5%) |         |   1.30 MiB (1%) |        8189 |
| `["parallel_histogram", "seq"]`                     |   4.262 ms (5%) |         | 364.16 KiB (1%) |          24 |
| `["partition_length_maximum", "rand", "foldl"]`     |  31.324 ms (5%) |         |                 |             |
| `["partition_length_maximum", "rand", "reduce"]`    |  15.723 ms (5%) |         |  736 bytes (1%) |          11 |
| `["splitby", "count", "foldl"]`                     |   1.487 ms (5%) |         |                 |             |
| `["splitby", "count", "man"]`                       |   1.166 ms (5%) |         |                 |             |
| `["splitby", "count", "reduce"]`                    | 858.764 μs (5%) |         |   1.06 KiB (1%) |          18 |
| `["sum", "random", "foldl"]`                        |  11.062 ms (5%) |         |                 |             |
| `["sum", "random", "reduce", "basesize=128"]`       |   5.676 ms (5%) |         |  74.25 KiB (1%) |        1106 |
| `["sum", "random", "reduce", "basesize=256"]`       |   5.609 ms (5%) |         |  36.81 KiB (1%) |         548 |
| `["sum", "random", "reduce", "basesize=512"]`       |   5.572 ms (5%) |         |  18.08 KiB (1%) |         269 |
| `["sum", "uniform", "foldl"]`                       |  10.938 ms (5%) |         |                 |             |
| `["sum", "uniform", "reduce", "basesize=128"]`      |   5.611 ms (5%) |         |  74.12 KiB (1%) |        1102 |
| `["sum", "uniform", "reduce", "basesize=256"]`      |   5.542 ms (5%) |         |  36.78 KiB (1%) |         547 |
| `["sum", "uniform", "reduce", "basesize=512"]`      |   5.504 ms (5%) |         |  18.05 KiB (1%) |         268 |
| `["sum", "valley", "foldl"]`                        |  11.162 ms (5%) |         |                 |             |
| `["sum", "valley", "reduce", "basesize=128"]`       |   5.728 ms (5%) |         |  74.09 KiB (1%) |        1101 |
| `["sum", "valley", "reduce", "basesize=256"]`       |   5.672 ms (5%) |         |  36.72 KiB (1%) |         545 |
| `["sum", "valley", "reduce", "basesize=512"]`       |   5.639 ms (5%) |         |  18.08 KiB (1%) |         269 |
| `["words", "nthreads=1"]`                           |  14.776 ms (5%) |         |  31.81 MiB (1%) |     1036398 |
| `["words", "nthreads=2"]`                           |   9.362 ms (5%) |         |  32.16 MiB (1%) |     1036440 |
| `["words", "nthreads=4"]`                           |   9.844 ms (5%) |         |  32.88 MiB (1%) |     1036555 |

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
      Ubuntu 24.04.2 LTS
  uname: Linux 6.11.0-1018-azure #18~24.04.1-Ubuntu SMP Sat Jun 28 04:46:03 UTC 2025 x86_64 x86_64
  CPU: AMD EPYC 7763 64-Core Processor: 
              speed         user         nice          sys         idle          irq
       #1  3246 MHz       2378 s          0 s        174 s       4699 s          0 s
       #2  3244 MHz       2612 s          0 s        191 s       4453 s          0 s
       #3  3175 MHz       2377 s          0 s        182 s       4702 s          0 s
       #4  3242 MHz       2736 s          0 s        181 s       4336 s          0 s
       
  Memory: 15.620681762695312 GB (12449.03125 MB free)
  Uptime: 728.23 sec
  Load Avg:  1.59  1.49  0.9
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-12.0.1 (ORCJIT, znver3)
```

---
# Baseline result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmark: 11 Aug 2025 - 02:34
* Package commit: 2a51f8d
* Julia commit: 742b9ab
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
| `["collect", "assoc", "basesize=1"]`                | 149.693 ms (5%) |         |   4.36 MiB (1%) |       32800 |
| `["collect", "assoc", "basesize=1024"]`             | 148.369 ms (5%) |         |   1.09 MiB (1%) |          53 |
| `["collect", "assoc", "basesize=32"]`               | 148.356 ms (5%) |         |   1.48 MiB (1%) |        1052 |
| `["collect", "seq"]`                                | 296.105 ms (5%) |         | 256.05 KiB (1%) |           2 |
| `["collect", "unordered", "basesize=1"]`            | 259.199 ms (5%) |         |  23.67 MiB (1%) |      405323 |
| `["collect", "unordered", "basesize=1024"]`         | 158.573 ms (5%) |         |   1.01 MiB (1%) |        1085 |
| `["collect", "unordered", "basesize=32"]`           | 170.933 ms (5%) |         |   1.60 MiB (1%) |       15350 |
| `["findfirst", "n=1000", "foldl"]`                  | 507.305 ms (5%) |         |                 |             |
| `["findfirst", "n=1000", "reduce", "basesize=128"]` | 276.258 ms (5%) |         | 232.73 KiB (1%) |        3272 |
| `["findfirst", "n=1000", "reduce", "basesize=256"]` | 388.806 ms (5%) |         | 170.44 KiB (1%) |        2383 |
| `["findfirst", "n=1000", "reduce", "basesize=512"]` | 453.990 ms (5%) |         | 108.55 KiB (1%) |        1509 |
| `["findfirst", "n=400", "foldl"]`                   | 379.595 ms (5%) |         |                 |             |
| `["findfirst", "n=400", "reduce", "basesize=128"]`  | 196.185 ms (5%) |         | 383.16 KiB (1%) |        5455 |
| `["findfirst", "n=400", "reduce", "basesize=256"]`  | 198.471 ms (5%) |         | 200.67 KiB (1%) |        2867 |
| `["findfirst", "n=400", "reduce", "basesize=512"]`  | 277.366 ms (5%) |         | 140.69 KiB (1%) |        2023 |
| `["findfirst", "n=500", "foldl"]`                   |  65.924 ms (5%) |         |                 |             |
| `["findfirst", "n=500", "reduce", "basesize=128"]`  | 146.117 ms (5%) |         | 252.73 KiB (1%) |        3492 |
| `["findfirst", "n=500", "reduce", "basesize=256"]`  |  83.609 ms (5%) |         | 115.45 KiB (1%) |        1546 |
| `["findfirst", "n=500", "reduce", "basesize=512"]`  |  85.106 ms (5%) |         |  56.86 KiB (1%) |         779 |
| `["overhead", "default"]`                           |  51.847 μs (5%) |         |  32.73 KiB (1%) |         418 |
| `["overhead", "stoppable=false"]`                   |  51.718 μs (5%) |         |  32.75 KiB (1%) |         418 |
| `["overhead", "stoppable=true"]`                    |  56.476 μs (5%) |         |  44.25 KiB (1%) |         610 |
| `["parallel_histogram", "assoc", "basesize=16384"]` |   2.386 ms (5%) |         | 728.91 KiB (1%) |          57 |
| `["parallel_histogram", "assoc", "basesize=4096"]`  |   2.940 ms (5%) |         |   1.79 MiB (1%) |         216 |
| `["parallel_histogram", "assoc", "basesize=8192"]`  |   2.698 ms (5%) |         |   1.42 MiB (1%) |         118 |
| `["parallel_histogram", "comm", "basesize=16384"]`  |   8.261 ms (5%) |         |   1.56 MiB (1%) |        1821 |
| `["parallel_histogram", "comm", "basesize=4096"]`   |  12.785 ms (5%) |         |   1.30 MiB (1%) |        8679 |
| `["parallel_histogram", "comm", "basesize=8192"]`   |  12.225 ms (5%) |         |   1.27 MiB (1%) |        7896 |
| `["parallel_histogram", "seq"]`                     |   4.241 ms (5%) |         | 364.16 KiB (1%) |          24 |
| `["partition_length_maximum", "rand", "foldl"]`     |  31.309 ms (5%) |         |                 |             |
| `["partition_length_maximum", "rand", "reduce"]`    |  15.711 ms (5%) |         |  736 bytes (1%) |          11 |
| `["splitby", "count", "foldl"]`                     |   1.513 ms (5%) |         |                 |             |
| `["splitby", "count", "man"]`                       |   1.166 ms (5%) |         |                 |             |
| `["splitby", "count", "reduce"]`                    | 721.331 μs (5%) |         |   1.09 KiB (1%) |          19 |
| `["sum", "random", "foldl"]`                        |  11.045 ms (5%) |         |                 |             |
| `["sum", "random", "reduce", "basesize=128"]`       |   5.627 ms (5%) |         |  74.16 KiB (1%) |        1103 |
| `["sum", "random", "reduce", "basesize=256"]`       |   5.591 ms (5%) |         |  36.69 KiB (1%) |         544 |
| `["sum", "random", "reduce", "basesize=512"]`       |   5.563 ms (5%) |         |  18.11 KiB (1%) |         270 |
| `["sum", "uniform", "foldl"]`                       |  10.930 ms (5%) |         |                 |             |
| `["sum", "uniform", "reduce", "basesize=128"]`      |   5.589 ms (5%) |         |  74.22 KiB (1%) |        1105 |
| `["sum", "uniform", "reduce", "basesize=256"]`      |   5.534 ms (5%) |         |  36.75 KiB (1%) |         546 |
| `["sum", "uniform", "reduce", "basesize=512"]`      |   5.500 ms (5%) |         |  18.08 KiB (1%) |         269 |
| `["sum", "valley", "foldl"]`                        |  11.168 ms (5%) |         |                 |             |
| `["sum", "valley", "reduce", "basesize=128"]`       |   5.725 ms (5%) |         |  74.19 KiB (1%) |        1104 |
| `["sum", "valley", "reduce", "basesize=256"]`       |   5.662 ms (5%) |         |  36.78 KiB (1%) |         547 |
| `["sum", "valley", "reduce", "basesize=512"]`       |   5.626 ms (5%) |         |  18.08 KiB (1%) |         269 |
| `["words", "nthreads=1"]`                           |  14.859 ms (5%) |         |  31.58 MiB (1%) |     1028640 |
| `["words", "nthreads=2"]`                           |   9.195 ms (5%) |         |  31.93 MiB (1%) |     1028678 |
| `["words", "nthreads=4"]`                           |   9.736 ms (5%) |         |  32.65 MiB (1%) |     1028769 |

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
      Ubuntu 24.04.2 LTS
  uname: Linux 6.11.0-1018-azure #18~24.04.1-Ubuntu SMP Sat Jun 28 04:46:03 UTC 2025 x86_64 x86_64
  CPU: AMD EPYC 7763 64-Core Processor: 
              speed         user         nice          sys         idle          irq
       #1  3250 MHz       3686 s          0 s        260 s       6432 s          0 s
       #2  3245 MHz       3709 s          0 s        280 s       6394 s          0 s
       #3  3242 MHz       3621 s          0 s        240 s       6527 s          0 s
       #4  3251 MHz       3918 s          0 s        231 s       6232 s          0 s
       
  Memory: 15.620681762695312 GB (12402.76171875 MB free)
  Uptime: 1041.38 sec
  Load Avg:  1.6  1.58  1.12
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

    Architecture:                         x86_64
    CPU op-mode(s):                       32-bit, 64-bit
    Address sizes:                        48 bits physical, 48 bits virtual
    Byte Order:                           Little Endian
    CPU(s):                               4
    On-line CPU(s) list:                  0-3
    Vendor ID:                            AuthenticAMD
    Model name:                           AMD EPYC 7763 64-Core Processor
    CPU family:                           25
    Model:                                1
    Thread(s) per core:                   2
    Core(s) per socket:                   2
    Socket(s):                            1
    Stepping:                             1
    BogoMIPS:                             4890.86
    Flags:                                fpu vme de pse tsc msr pae mce cx8 apic sep mtrr pge mca cmov pat pse36 clflush mmx fxsr sse sse2 ht syscall nx mmxext fxsr_opt pdpe1gb rdtscp lm constant_tsc rep_good nopl tsc_reliable nonstop_tsc cpuid extd_apicid aperfmperf tsc_known_freq pni pclmulqdq ssse3 fma cx16 pcid sse4_1 sse4_2 movbe popcnt aes xsave avx f16c rdrand hypervisor lahf_lm cmp_legacy svm cr8_legacy abm sse4a misalignsse 3dnowprefetch osvw topoext vmmcall fsgsbase bmi1 avx2 smep bmi2 erms invpcid rdseed adx smap clflushopt clwb sha_ni xsaveopt xsavec xgetbv1 xsaves user_shstk clzero xsaveerptr rdpru arat npt nrip_save tsc_scale vmcb_clean flushbyasid decodeassists pausefilter pfthreshold v_vmsave_vmload umip vaes vpclmulqdq rdpid fsrm
    Virtualization:                       AMD-V
    Hypervisor vendor:                    Microsoft
    Virtualization type:                  full
    L1d cache:                            64 KiB (2 instances)
    L1i cache:                            64 KiB (2 instances)
    L2 cache:                             1 MiB (2 instances)
    L3 cache:                             32 MiB (1 instance)
    NUMA node(s):                         1
    NUMA node0 CPU(s):                    0-3
    Vulnerability Gather data sampling:   Not affected
    Vulnerability Itlb multihit:          Not affected
    Vulnerability L1tf:                   Not affected
    Vulnerability Mds:                    Not affected
    Vulnerability Meltdown:               Not affected
    Vulnerability Mmio stale data:        Not affected
    Vulnerability Reg file data sampling: Not affected
    Vulnerability Retbleed:               Not affected
    Vulnerability Spec rstack overflow:   Vulnerable: Safe RET, no microcode
    Vulnerability Spec store bypass:      Vulnerable
    Vulnerability Spectre v1:             Mitigation; usercopy/swapgs barriers and __user pointer sanitization
    Vulnerability Spectre v2:             Mitigation; Retpolines; STIBP disabled; RSB filling; PBRSB-eIBRS Not affected; BHI Not affected
    Vulnerability Srbds:                  Not affected
    Vulnerability Tsx async abort:        Not affected
    

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

