# Multi-thread benchmark result

* Pull request commit: [`79dc041cd3eb3727301774684e7dc9385270476f`](https://github.com/JuliaFolds/Transducers.jl/commit/79dc041cd3eb3727301774684e7dc9385270476f)
* Pull request: <https://github.com/JuliaFolds/Transducers.jl/pull/243> (Update */Manifest.toml)

# Judge result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmarks:
    - Target: 21 Apr 2024 - 01:29
    - Baseline: 21 Apr 2024 - 01:34
* Package commits:
    - Target: 27d975
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
| `["collect", "unordered", "basesize=1"]`            |                1.05 (5%) :x: |                   1.00 (1%)  |
| `["findfirst", "n=1000", "reduce", "basesize=256"]` |                   0.96 (5%)  | 0.96 (1%) :white_check_mark: |
| `["findfirst", "n=1000", "reduce", "basesize=512"]` | 0.85 (5%) :white_check_mark: | 0.94 (1%) :white_check_mark: |
| `["findfirst", "n=400", "reduce", "basesize=128"]`  |                   1.00 (5%)  | 0.98 (1%) :white_check_mark: |
| `["findfirst", "n=400", "reduce", "basesize=512"]`  |                1.06 (5%) :x: |                1.05 (1%) :x: |
| `["findfirst", "n=500", "reduce", "basesize=128"]`  |                1.24 (5%) :x: |                1.05 (1%) :x: |
| `["findfirst", "n=500", "reduce", "basesize=256"]`  |                   1.03 (5%)  |                1.01 (1%) :x: |
| `["findfirst", "n=500", "reduce", "basesize=512"]`  |                1.24 (5%) :x: |                1.15 (1%) :x: |
| `["parallel_histogram", "comm", "basesize=16384"]`  |                   1.03 (5%)  | 0.98 (1%) :white_check_mark: |
| `["partition_length_maximum", "rand", "reduce"]`    |                   1.00 (5%)  |                1.05 (1%) :x: |
| `["splitby", "count", "reduce"]`                    |                   1.00 (5%)  | 0.97 (1%) :white_check_mark: |
| `["sum", "random", "reduce", "basesize=128"]`       | 0.93 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["sum", "valley", "reduce", "basesize=128"]`       |                1.07 (5%) :x: |                   1.00 (1%)  |
| `["words", "nthreads=2"]`                           | 0.94 (5%) :white_check_mark: |                1.02 (1%) :x: |
| `["words", "nthreads=4"]`                           | 0.88 (5%) :white_check_mark: |                1.01 (1%) :x: |

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
  uname: Linux 6.5.0-1018-azure #19~22.04.2-Ubuntu SMP Thu Mar 21 16:45:46 UTC 2024 x86_64 x86_64
  CPU: AMD EPYC 7763 64-Core Processor: 
              speed         user         nice          sys         idle          irq
       #1  3242 MHz       2266 s          0 s        156 s       5153 s          0 s
       #2  3228 MHz       2540 s          0 s        173 s       4877 s          0 s
       #3  2579 MHz       2600 s          0 s        158 s       4825 s          0 s
       #4  2445 MHz       2569 s          0 s        174 s       4844 s          0 s
       
  Memory: 15.606494903564453 GB (12499.27734375 MB free)
  Uptime: 761.94 sec
  Load Avg:  1.63  1.5  0.89
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
  uname: Linux 6.5.0-1018-azure #19~22.04.2-Ubuntu SMP Thu Mar 21 16:45:46 UTC 2024 x86_64 x86_64
  CPU: AMD EPYC 7763 64-Core Processor: 
              speed         user         nice          sys         idle          irq
       #1  2445 MHz       3430 s          0 s        204 s       6823 s          0 s
       #2  3243 MHz       3724 s          0 s        213 s       6533 s          0 s
       #3  2583 MHz       3610 s          0 s        213 s       6641 s          0 s
       #4  3222 MHz       3773 s          0 s        228 s       6469 s          0 s
       
  Memory: 15.606494903564453 GB (12455.22265625 MB free)
  Uptime: 1050.58 sec
  Load Avg:  1.61  1.56  1.08
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-12.0.1 (ORCJIT, znver3)
```

---
# Target result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmark: 21 Apr 2024 - 1:29
* Package commit: 27d975
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
| `["collect", "assoc", "basesize=1"]`                | 147.935 ms (5%) |         |   4.36 MiB (1%) |       32800 |
| `["collect", "assoc", "basesize=1024"]`             | 147.409 ms (5%) |         |   1.09 MiB (1%) |          53 |
| `["collect", "assoc", "basesize=32"]`               | 140.823 ms (5%) |         |   1.48 MiB (1%) |        1052 |
| `["collect", "seq"]`                                | 287.572 ms (5%) |         | 256.05 KiB (1%) |           2 |
| `["collect", "unordered", "basesize=1"]`            | 243.261 ms (5%) |         |  23.82 MiB (1%) |      410337 |
| `["collect", "unordered", "basesize=1024"]`         | 152.584 ms (5%) |         |   1.01 MiB (1%) |        1087 |
| `["collect", "unordered", "basesize=32"]`           | 156.969 ms (5%) |         |   1.60 MiB (1%) |       15255 |
| `["findfirst", "n=1000", "foldl"]`                  | 490.582 ms (5%) |         |                 |             |
| `["findfirst", "n=1000", "reduce", "basesize=128"]` | 269.359 ms (5%) |         | 232.86 KiB (1%) |        3276 |
| `["findfirst", "n=1000", "reduce", "basesize=256"]` | 363.266 ms (5%) |         | 164.64 KiB (1%) |        2303 |
| `["findfirst", "n=1000", "reduce", "basesize=512"]` | 334.580 ms (5%) |         |  81.36 KiB (1%) |        1147 |
| `["findfirst", "n=400", "foldl"]`                   | 367.780 ms (5%) |         |                 |             |
| `["findfirst", "n=400", "reduce", "basesize=128"]`  | 188.694 ms (5%) |         | 376.36 KiB (1%) |        5376 |
| `["findfirst", "n=400", "reduce", "basesize=256"]`  | 193.976 ms (5%) |         | 200.86 KiB (1%) |        2873 |
| `["findfirst", "n=400", "reduce", "basesize=512"]`  | 218.952 ms (5%) |         | 112.56 KiB (1%) |        1621 |
| `["findfirst", "n=500", "foldl"]`                   |  62.254 ms (5%) |         |                 |             |
| `["findfirst", "n=500", "reduce", "basesize=128"]`  | 118.077 ms (5%) |         | 199.78 KiB (1%) |        2790 |
| `["findfirst", "n=500", "reduce", "basesize=256"]`  |  62.299 ms (5%) |         |  78.45 KiB (1%) |        1068 |
| `["findfirst", "n=500", "reduce", "basesize=512"]`  |  83.524 ms (5%) |         |  56.83 KiB (1%) |         778 |
| `["overhead", "default"]`                           |  49.893 μs (5%) |         |  32.77 KiB (1%) |         419 |
| `["overhead", "stoppable=false"]`                   |  49.703 μs (5%) |         |  32.75 KiB (1%) |         418 |
| `["overhead", "stoppable=true"]`                    |  58.690 μs (5%) |         |  44.25 KiB (1%) |         610 |
| `["parallel_histogram", "assoc", "basesize=16384"]` |   2.210 ms (5%) |         | 728.91 KiB (1%) |          57 |
| `["parallel_histogram", "assoc", "basesize=4096"]`  |   2.726 ms (5%) |         |   1.79 MiB (1%) |         216 |
| `["parallel_histogram", "assoc", "basesize=8192"]`  |   2.455 ms (5%) |         |   1.42 MiB (1%) |         117 |
| `["parallel_histogram", "comm", "basesize=16384"]`  |   8.328 ms (5%) |         |   1.56 MiB (1%) |        1698 |
| `["parallel_histogram", "comm", "basesize=4096"]`   |  13.185 ms (5%) |         |   1.32 MiB (1%) |        9329 |
| `["parallel_histogram", "comm", "basesize=8192"]`   |  11.790 ms (5%) |         |   1.28 MiB (1%) |        7717 |
| `["parallel_histogram", "seq"]`                     |   3.921 ms (5%) |         | 364.16 KiB (1%) |          24 |
| `["partition_length_maximum", "rand", "foldl"]`     |  29.382 ms (5%) |         |                 |             |
| `["partition_length_maximum", "rand", "reduce"]`    |  14.599 ms (5%) |         |  736 bytes (1%) |          11 |
| `["splitby", "count", "foldl"]`                     |   1.425 ms (5%) |         |                 |             |
| `["splitby", "count", "man"]`                       |   1.067 ms (5%) |         |                 |             |
| `["splitby", "count", "reduce"]`                    | 668.025 μs (5%) |         |   1.03 KiB (1%) |          18 |
| `["sum", "random", "foldl"]`                        |  10.150 ms (5%) |         |                 |             |
| `["sum", "random", "reduce", "basesize=128"]`       |   5.189 ms (5%) |         |  74.02 KiB (1%) |        1099 |
| `["sum", "random", "reduce", "basesize=256"]`       |   5.114 ms (5%) |         |  36.70 KiB (1%) |         545 |
| `["sum", "random", "reduce", "basesize=512"]`       |   5.079 ms (5%) |         |  18.05 KiB (1%) |         268 |
| `["sum", "uniform", "foldl"]`                       |  10.138 ms (5%) |         |                 |             |
| `["sum", "uniform", "reduce", "basesize=128"]`      |   5.157 ms (5%) |         |  74.14 KiB (1%) |        1103 |
| `["sum", "uniform", "reduce", "basesize=256"]`      |   5.110 ms (5%) |         |  36.70 KiB (1%) |         545 |
| `["sum", "uniform", "reduce", "basesize=512"]`      |   5.058 ms (5%) |         |  18.03 KiB (1%) |         268 |
| `["sum", "valley", "foldl"]`                        |  10.324 ms (5%) |         |                 |             |
| `["sum", "valley", "reduce", "basesize=128"]`       |   5.690 ms (5%) |         |  74.05 KiB (1%) |        1100 |
| `["sum", "valley", "reduce", "basesize=256"]`       |   5.317 ms (5%) |         |  36.70 KiB (1%) |         545 |
| `["sum", "valley", "reduce", "basesize=512"]`       |   5.200 ms (5%) |         |  18.06 KiB (1%) |         269 |
| `["words", "nthreads=1"]`                           |  13.772 ms (5%) |         |  31.77 MiB (1%) |     1035489 |
| `["words", "nthreads=2"]`                           |   9.650 ms (5%) |         |  32.48 MiB (1%) |     1035582 |
| `["words", "nthreads=4"]`                           |   9.663 ms (5%) |         |  32.93 MiB (1%) |     1035671 |

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
  uname: Linux 6.5.0-1018-azure #19~22.04.2-Ubuntu SMP Thu Mar 21 16:45:46 UTC 2024 x86_64 x86_64
  CPU: AMD EPYC 7763 64-Core Processor: 
              speed         user         nice          sys         idle          irq
       #1  3242 MHz       2266 s          0 s        156 s       5153 s          0 s
       #2  3228 MHz       2540 s          0 s        173 s       4877 s          0 s
       #3  2579 MHz       2600 s          0 s        158 s       4825 s          0 s
       #4  2445 MHz       2569 s          0 s        174 s       4844 s          0 s
       
  Memory: 15.606494903564453 GB (12499.27734375 MB free)
  Uptime: 761.94 sec
  Load Avg:  1.63  1.5  0.89
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-12.0.1 (ORCJIT, znver3)
```

---
# Baseline result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmark: 21 Apr 2024 - 1:34
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
| `["collect", "assoc", "basesize=1"]`                | 141.550 ms (5%) |         |   4.36 MiB (1%) |       32800 |
| `["collect", "assoc", "basesize=1024"]`             | 140.451 ms (5%) |         |   1.09 MiB (1%) |          53 |
| `["collect", "assoc", "basesize=32"]`               | 141.071 ms (5%) |         |   1.48 MiB (1%) |        1052 |
| `["collect", "seq"]`                                | 287.388 ms (5%) |         | 256.05 KiB (1%) |           2 |
| `["collect", "unordered", "basesize=1"]`            | 231.511 ms (5%) |         |  23.82 MiB (1%) |      410539 |
| `["collect", "unordered", "basesize=1024"]`         | 148.745 ms (5%) |         |   1.01 MiB (1%) |        1138 |
| `["collect", "unordered", "basesize=32"]`           | 157.890 ms (5%) |         |   1.60 MiB (1%) |       15148 |
| `["findfirst", "n=1000", "foldl"]`                  | 499.684 ms (5%) |         |                 |             |
| `["findfirst", "n=1000", "reduce", "basesize=128"]` | 270.798 ms (5%) |         | 232.73 KiB (1%) |        3272 |
| `["findfirst", "n=1000", "reduce", "basesize=256"]` | 377.226 ms (5%) |         | 172.02 KiB (1%) |        2405 |
| `["findfirst", "n=1000", "reduce", "basesize=512"]` | 391.495 ms (5%) |         |  86.38 KiB (1%) |        1223 |
| `["findfirst", "n=400", "foldl"]`                   | 368.391 ms (5%) |         |                 |             |
| `["findfirst", "n=400", "reduce", "basesize=128"]`  | 188.167 ms (5%) |         | 383.36 KiB (1%) |        5461 |
| `["findfirst", "n=400", "reduce", "basesize=256"]`  | 195.792 ms (5%) |         | 200.67 KiB (1%) |        2867 |
| `["findfirst", "n=400", "reduce", "basesize=512"]`  | 206.685 ms (5%) |         | 107.12 KiB (1%) |        1550 |
| `["findfirst", "n=500", "foldl"]`                   |  62.364 ms (5%) |         |                 |             |
| `["findfirst", "n=500", "reduce", "basesize=128"]`  |  95.400 ms (5%) |         | 190.44 KiB (1%) |        2593 |
| `["findfirst", "n=500", "reduce", "basesize=256"]`  |  60.306 ms (5%) |         |  77.62 KiB (1%) |        1056 |
| `["findfirst", "n=500", "reduce", "basesize=512"]`  |  67.154 ms (5%) |         |  49.48 KiB (1%) |         670 |
| `["overhead", "default"]`                           |  49.864 μs (5%) |         |  32.77 KiB (1%) |         419 |
| `["overhead", "stoppable=false"]`                   |  48.631 μs (5%) |         |  32.75 KiB (1%) |         418 |
| `["overhead", "stoppable=true"]`                    |  56.035 μs (5%) |         |  44.25 KiB (1%) |         610 |
| `["parallel_histogram", "assoc", "basesize=16384"]` |   2.202 ms (5%) |         | 728.91 KiB (1%) |          57 |
| `["parallel_histogram", "assoc", "basesize=4096"]`  |   2.700 ms (5%) |         |   1.79 MiB (1%) |         216 |
| `["parallel_histogram", "assoc", "basesize=8192"]`  |   2.461 ms (5%) |         |   1.42 MiB (1%) |         117 |
| `["parallel_histogram", "comm", "basesize=16384"]`  |   8.117 ms (5%) |         |   1.59 MiB (1%) |        2923 |
| `["parallel_histogram", "comm", "basesize=4096"]`   |  13.717 ms (5%) |         |   1.33 MiB (1%) |        9609 |
| `["parallel_histogram", "comm", "basesize=8192"]`   |  11.567 ms (5%) |         |   1.27 MiB (1%) |        7283 |
| `["parallel_histogram", "seq"]`                     |   3.925 ms (5%) |         | 364.16 KiB (1%) |          24 |
| `["partition_length_maximum", "rand", "foldl"]`     |  29.762 ms (5%) |         |                 |             |
| `["partition_length_maximum", "rand", "reduce"]`    |  14.577 ms (5%) |         |  704 bytes (1%) |          10 |
| `["splitby", "count", "foldl"]`                     |   1.423 ms (5%) |         |                 |             |
| `["splitby", "count", "man"]`                       |   1.068 ms (5%) |         |                 |             |
| `["splitby", "count", "reduce"]`                    | 668.706 μs (5%) |         |   1.06 KiB (1%) |          18 |
| `["sum", "random", "foldl"]`                        |  10.270 ms (5%) |         |                 |             |
| `["sum", "random", "reduce", "basesize=128"]`       |   5.603 ms (5%) |         |  74.05 KiB (1%) |        1100 |
| `["sum", "random", "reduce", "basesize=256"]`       |   5.296 ms (5%) |         |  36.58 KiB (1%) |         541 |
| `["sum", "random", "reduce", "basesize=512"]`       |   5.144 ms (5%) |         |  18.08 KiB (1%) |         269 |
| `["sum", "uniform", "foldl"]`                       |  10.344 ms (5%) |         |                 |             |
| `["sum", "uniform", "reduce", "basesize=128"]`      |   5.153 ms (5%) |         |  74.17 KiB (1%) |        1104 |
| `["sum", "uniform", "reduce", "basesize=256"]`      |   5.098 ms (5%) |         |  36.77 KiB (1%) |         547 |
| `["sum", "uniform", "reduce", "basesize=512"]`      |   5.062 ms (5%) |         |  17.97 KiB (1%) |         266 |
| `["sum", "valley", "foldl"]`                        |  10.350 ms (5%) |         |                 |             |
| `["sum", "valley", "reduce", "basesize=128"]`       |   5.312 ms (5%) |         |  74.05 KiB (1%) |        1100 |
| `["sum", "valley", "reduce", "basesize=256"]`       |   5.513 ms (5%) |         |  36.77 KiB (1%) |         547 |
| `["sum", "valley", "reduce", "basesize=512"]`       |   5.210 ms (5%) |         |  18.06 KiB (1%) |         269 |
| `["words", "nthreads=1"]`                           |  13.914 ms (5%) |         |  31.53 MiB (1%) |     1027154 |
| `["words", "nthreads=2"]`                           |  10.309 ms (5%) |         |  31.89 MiB (1%) |     1027201 |
| `["words", "nthreads=4"]`                           |  11.038 ms (5%) |         |  32.60 MiB (1%) |     1027278 |

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
  uname: Linux 6.5.0-1018-azure #19~22.04.2-Ubuntu SMP Thu Mar 21 16:45:46 UTC 2024 x86_64 x86_64
  CPU: AMD EPYC 7763 64-Core Processor: 
              speed         user         nice          sys         idle          irq
       #1  2445 MHz       3430 s          0 s        204 s       6823 s          0 s
       #2  3243 MHz       3724 s          0 s        213 s       6533 s          0 s
       #3  2583 MHz       3610 s          0 s        213 s       6641 s          0 s
       #4  3222 MHz       3773 s          0 s        228 s       6469 s          0 s
       
  Memory: 15.606494903564453 GB (12455.22265625 MB free)
  Uptime: 1050.58 sec
  Load Avg:  1.61  1.56  1.08
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
    BogoMIPS:                           4890.85
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

