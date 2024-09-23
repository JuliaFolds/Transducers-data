# Multi-thread benchmark result

* Pull request commit: [`345e1f4f977bf303230fcbb23322ad73adb92c95`](https://github.com/JuliaFolds/Transducers.jl/commit/345e1f4f977bf303230fcbb23322ad73adb92c95)
* Pull request: <https://github.com/JuliaFolds/Transducers.jl/pull/243> (Update */Manifest.toml)

# Judge result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmarks:
    - Target: 23 Sep 2024 - 01:51
    - Baseline: 23 Sep 2024 - 01:56
* Package commits:
    - Target: 4f9a5d
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
| `["findfirst", "n=1000", "reduce", "basesize=128"]` |                1.47 (5%) :x: |                1.42 (1%) :x: |
| `["findfirst", "n=1000", "reduce", "basesize=256"]` | 0.85 (5%) :white_check_mark: | 0.93 (1%) :white_check_mark: |
| `["findfirst", "n=1000", "reduce", "basesize=512"]` | 0.59 (5%) :white_check_mark: | 0.62 (1%) :white_check_mark: |
| `["findfirst", "n=400", "reduce", "basesize=128"]`  |                   1.02 (5%)  |                1.04 (1%) :x: |
| `["findfirst", "n=400", "reduce", "basesize=256"]`  |                   1.01 (5%)  |                1.03 (1%) :x: |
| `["findfirst", "n=400", "reduce", "basesize=512"]`  | 0.92 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["findfirst", "n=500", "reduce", "basesize=128"]`  | 0.30 (5%) :white_check_mark: | 0.39 (1%) :white_check_mark: |
| `["findfirst", "n=500", "reduce", "basesize=256"]`  | 0.41 (5%) :white_check_mark: | 0.58 (1%) :white_check_mark: |
| `["findfirst", "n=500", "reduce", "basesize=512"]`  |                2.27 (5%) :x: |                1.83 (1%) :x: |
| `["parallel_histogram", "assoc", "basesize=4096"]`  |                   1.04 (5%)  |                1.15 (1%) :x: |
| `["splitby", "count", "reduce"]`                    | 0.87 (5%) :white_check_mark: | 0.97 (1%) :white_check_mark: |
| `["words", "nthreads=1"]`                           |                   0.99 (5%)  |                1.02 (1%) :x: |
| `["words", "nthreads=2"]`                           |                1.08 (5%) :x: |                1.01 (1%) :x: |
| `["words", "nthreads=4"]`                           |                1.06 (5%) :x: |                   1.01 (1%)  |

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
      Ubuntu 22.04.5 LTS
  uname: Linux 6.8.0-1014-azure #16~22.04.1-Ubuntu SMP Thu Aug 15 21:31:41 UTC 2024 x86_64 x86_64
  CPU: AMD EPYC 7763 64-Core Processor: 
              speed         user         nice          sys         idle          irq
       #1  3232 MHz       2317 s          0 s        191 s       4713 s          0 s
       #2  3202 MHz       2815 s          0 s        218 s       4174 s          0 s
       #3  3249 MHz       2391 s          0 s        207 s       4628 s          0 s
       #4  3246 MHz       2356 s          0 s        196 s       4670 s          0 s
       
  Memory: 15.615272521972656 GB (12448.73828125 MB free)
  Uptime: 725.27 sec
  Load Avg:  1.68  1.48  0.87
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
      Ubuntu 22.04.5 LTS
  uname: Linux 6.8.0-1014-azure #16~22.04.1-Ubuntu SMP Thu Aug 15 21:31:41 UTC 2024 x86_64 x86_64
  CPU: AMD EPYC 7763 64-Core Processor: 
              speed         user         nice          sys         idle          irq
       #1  3242 MHz       3333 s          0 s        246 s       6623 s          0 s
       #2  3173 MHz       4352 s          0 s        289 s       5547 s          0 s
       #3  3183 MHz       3538 s          0 s        309 s       6362 s          0 s
       #4  2445 MHz       3264 s          0 s        271 s       6670 s          0 s
       
  Memory: 15.615272521972656 GB (12457.4453125 MB free)
  Uptime: 1024.02 sec
  Load Avg:  1.57  1.57  1.09
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-12.0.1 (ORCJIT, znver3)
```

---
# Target result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmark: 23 Sep 2024 - 1:51
* Package commit: 4f9a5d
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
| `["collect", "assoc", "basesize=1"]`                | 149.457 ms (5%) |         |   4.36 MiB (1%) |       32800 |
| `["collect", "assoc", "basesize=1024"]`             | 148.189 ms (5%) |         |   1.09 MiB (1%) |          53 |
| `["collect", "assoc", "basesize=32"]`               | 148.367 ms (5%) |         |   1.48 MiB (1%) |        1052 |
| `["collect", "seq"]`                                | 296.084 ms (5%) |         | 256.05 KiB (1%) |           2 |
| `["collect", "unordered", "basesize=1"]`            | 256.782 ms (5%) |         |  23.69 MiB (1%) |      405980 |
| `["collect", "unordered", "basesize=1024"]`         | 157.787 ms (5%) |         |   1.01 MiB (1%) |        1054 |
| `["collect", "unordered", "basesize=32"]`           | 170.316 ms (5%) |         |   1.60 MiB (1%) |       15347 |
| `["findfirst", "n=1000", "foldl"]`                  | 510.824 ms (5%) |         |                 |             |
| `["findfirst", "n=1000", "reduce", "basesize=128"]` | 409.785 ms (5%) |         | 329.88 KiB (1%) |        4628 |
| `["findfirst", "n=1000", "reduce", "basesize=256"]` | 368.540 ms (5%) |         | 164.61 KiB (1%) |        2302 |
| `["findfirst", "n=1000", "reduce", "basesize=512"]` | 467.987 ms (5%) |         | 105.08 KiB (1%) |        1475 |
| `["findfirst", "n=400", "foldl"]`                   | 381.419 ms (5%) |         |                 |             |
| `["findfirst", "n=400", "reduce", "basesize=128"]`  | 199.128 ms (5%) |         | 387.17 KiB (1%) |        5508 |
| `["findfirst", "n=400", "reduce", "basesize=256"]`  | 199.605 ms (5%) |         | 200.86 KiB (1%) |        2873 |
| `["findfirst", "n=400", "reduce", "basesize=512"]`  | 254.153 ms (5%) |         | 138.98 KiB (1%) |        1971 |
| `["findfirst", "n=500", "foldl"]`                   |  65.605 ms (5%) |         |                 |             |
| `["findfirst", "n=500", "reduce", "basesize=128"]`  |  54.191 ms (5%) |         | 115.73 KiB (1%) |        1591 |
| `["findfirst", "n=500", "reduce", "basesize=256"]`  |  81.852 ms (5%) |         |  98.48 KiB (1%) |        1341 |
| `["findfirst", "n=500", "reduce", "basesize=512"]`  | 184.519 ms (5%) |         |  96.58 KiB (1%) |        1337 |
| `["overhead", "default"]`                           |  51.878 μs (5%) |         |  32.73 KiB (1%) |         418 |
| `["overhead", "stoppable=false"]`                   |  52.579 μs (5%) |         |  32.75 KiB (1%) |         418 |
| `["overhead", "stoppable=true"]`                    |  57.689 μs (5%) |         |  44.25 KiB (1%) |         610 |
| `["parallel_histogram", "assoc", "basesize=16384"]` |   2.402 ms (5%) |         | 728.91 KiB (1%) |          57 |
| `["parallel_histogram", "assoc", "basesize=4096"]`  |   3.067 ms (5%) |         |   2.05 MiB (1%) |         222 |
| `["parallel_histogram", "assoc", "basesize=8192"]`  |   2.676 ms (5%) |         |   1.42 MiB (1%) |         117 |
| `["parallel_histogram", "comm", "basesize=16384"]`  |   7.805 ms (5%) |         |   1.55 MiB (1%) |        1484 |
| `["parallel_histogram", "comm", "basesize=4096"]`   |  12.810 ms (5%) |         |   1.31 MiB (1%) |        9236 |
| `["parallel_histogram", "comm", "basesize=8192"]`   |  12.245 ms (5%) |         |   1.28 MiB (1%) |        7332 |
| `["parallel_histogram", "seq"]`                     |   4.271 ms (5%) |         | 364.16 KiB (1%) |          24 |
| `["partition_length_maximum", "rand", "foldl"]`     |  31.317 ms (5%) |         |                 |             |
| `["partition_length_maximum", "rand", "reduce"]`    |  15.704 ms (5%) |         |  736 bytes (1%) |          11 |
| `["splitby", "count", "foldl"]`                     |   1.514 ms (5%) |         |                 |             |
| `["splitby", "count", "man"]`                       |   1.165 ms (5%) |         |                 |             |
| `["splitby", "count", "reduce"]`                    | 720.995 μs (5%) |         |   1.06 KiB (1%) |          18 |
| `["sum", "random", "foldl"]`                        |  11.014 ms (5%) |         |                 |             |
| `["sum", "random", "reduce", "basesize=128"]`       |   5.651 ms (5%) |         |  74.14 KiB (1%) |        1103 |
| `["sum", "random", "reduce", "basesize=256"]`       |   5.580 ms (5%) |         |  36.73 KiB (1%) |         546 |
| `["sum", "random", "reduce", "basesize=512"]`       |   5.546 ms (5%) |         |  18.11 KiB (1%) |         270 |
| `["sum", "uniform", "foldl"]`                       |  10.919 ms (5%) |         |                 |             |
| `["sum", "uniform", "reduce", "basesize=128"]`      |   5.603 ms (5%) |         |  74.11 KiB (1%) |        1102 |
| `["sum", "uniform", "reduce", "basesize=256"]`      |   5.531 ms (5%) |         |  36.70 KiB (1%) |         545 |
| `["sum", "uniform", "reduce", "basesize=512"]`      |   5.492 ms (5%) |         |  18.03 KiB (1%) |         268 |
| `["sum", "valley", "foldl"]`                        |  11.168 ms (5%) |         |                 |             |
| `["sum", "valley", "reduce", "basesize=128"]`       |   5.726 ms (5%) |         |  74.05 KiB (1%) |        1100 |
| `["sum", "valley", "reduce", "basesize=256"]`       |   5.670 ms (5%) |         |  36.77 KiB (1%) |         547 |
| `["sum", "valley", "reduce", "basesize=512"]`       |   5.628 ms (5%) |         |  18.03 KiB (1%) |         268 |
| `["words", "nthreads=1"]`                           |  14.265 ms (5%) |         |  31.89 MiB (1%) |     1039056 |
| `["words", "nthreads=2"]`                           |  10.289 ms (5%) |         |  32.25 MiB (1%) |     1039092 |
| `["words", "nthreads=4"]`                           |  10.710 ms (5%) |         |  32.96 MiB (1%) |     1039175 |

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
      Ubuntu 22.04.5 LTS
  uname: Linux 6.8.0-1014-azure #16~22.04.1-Ubuntu SMP Thu Aug 15 21:31:41 UTC 2024 x86_64 x86_64
  CPU: AMD EPYC 7763 64-Core Processor: 
              speed         user         nice          sys         idle          irq
       #1  3232 MHz       2317 s          0 s        191 s       4713 s          0 s
       #2  3202 MHz       2815 s          0 s        218 s       4174 s          0 s
       #3  3249 MHz       2391 s          0 s        207 s       4628 s          0 s
       #4  3246 MHz       2356 s          0 s        196 s       4670 s          0 s
       
  Memory: 15.615272521972656 GB (12448.73828125 MB free)
  Uptime: 725.27 sec
  Load Avg:  1.68  1.48  0.87
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-12.0.1 (ORCJIT, znver3)
```

---
# Baseline result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmark: 23 Sep 2024 - 1:56
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
| `["collect", "assoc", "basesize=1"]`                | 149.819 ms (5%) |         |   4.36 MiB (1%) |       32800 |
| `["collect", "assoc", "basesize=1024"]`             | 148.503 ms (5%) |         |   1.09 MiB (1%) |          53 |
| `["collect", "assoc", "basesize=32"]`               | 148.431 ms (5%) |         |   1.48 MiB (1%) |        1052 |
| `["collect", "seq"]`                                | 296.250 ms (5%) |         | 256.05 KiB (1%) |           2 |
| `["collect", "unordered", "basesize=1"]`            | 262.318 ms (5%) |         |  23.68 MiB (1%) |      405814 |
| `["collect", "unordered", "basesize=1024"]`         | 157.974 ms (5%) |         |   1.01 MiB (1%) |        1011 |
| `["collect", "unordered", "basesize=32"]`           | 170.464 ms (5%) |         |   1.60 MiB (1%) |       15298 |
| `["findfirst", "n=1000", "foldl"]`                  | 509.567 ms (5%) |         |                 |             |
| `["findfirst", "n=1000", "reduce", "basesize=128"]` | 278.118 ms (5%) |         | 232.86 KiB (1%) |        3276 |
| `["findfirst", "n=1000", "reduce", "basesize=256"]` | 433.583 ms (5%) |         | 176.88 KiB (1%) |        2510 |
| `["findfirst", "n=1000", "reduce", "basesize=512"]` | 797.892 ms (5%) |         | 168.34 KiB (1%) |        2377 |
| `["findfirst", "n=400", "foldl"]`                   | 381.243 ms (5%) |         |                 |             |
| `["findfirst", "n=400", "reduce", "basesize=128"]`  | 195.789 ms (5%) |         | 373.95 KiB (1%) |        5344 |
| `["findfirst", "n=400", "reduce", "basesize=256"]`  | 198.185 ms (5%) |         | 194.83 KiB (1%) |        2803 |
| `["findfirst", "n=400", "reduce", "basesize=512"]`  | 275.088 ms (5%) |         | 139.62 KiB (1%) |        2001 |
| `["findfirst", "n=500", "foldl"]`                   |  65.869 ms (5%) |         |                 |             |
| `["findfirst", "n=500", "reduce", "basesize=128"]`  | 181.234 ms (5%) |         | 294.25 KiB (1%) |        4142 |
| `["findfirst", "n=500", "reduce", "basesize=256"]`  | 198.284 ms (5%) |         | 170.73 KiB (1%) |        2397 |
| `["findfirst", "n=500", "reduce", "basesize=512"]`  |  81.289 ms (5%) |         |  52.73 KiB (1%) |         718 |
| `["overhead", "default"]`                           |  52.038 μs (5%) |         |  32.73 KiB (1%) |         418 |
| `["overhead", "stoppable=false"]`                   |  50.656 μs (5%) |         |  32.75 KiB (1%) |         418 |
| `["overhead", "stoppable=true"]`                    |  57.899 μs (5%) |         |  44.25 KiB (1%) |         610 |
| `["parallel_histogram", "assoc", "basesize=16384"]` |   2.408 ms (5%) |         | 728.91 KiB (1%) |          57 |
| `["parallel_histogram", "assoc", "basesize=4096"]`  |   2.954 ms (5%) |         |   1.79 MiB (1%) |         216 |
| `["parallel_histogram", "assoc", "basesize=8192"]`  |   2.689 ms (5%) |         |   1.42 MiB (1%) |         117 |
| `["parallel_histogram", "comm", "basesize=16384"]`  |   8.069 ms (5%) |         |   1.56 MiB (1%) |        1829 |
| `["parallel_histogram", "comm", "basesize=4096"]`   |  13.161 ms (5%) |         |   1.33 MiB (1%) |        9650 |
| `["parallel_histogram", "comm", "basesize=8192"]`   |  12.138 ms (5%) |         |   1.28 MiB (1%) |        7278 |
| `["parallel_histogram", "seq"]`                     |   4.277 ms (5%) |         | 364.16 KiB (1%) |          24 |
| `["partition_length_maximum", "rand", "foldl"]`     |  31.328 ms (5%) |         |                 |             |
| `["partition_length_maximum", "rand", "reduce"]`    |  15.675 ms (5%) |         |  736 bytes (1%) |          11 |
| `["splitby", "count", "foldl"]`                     |   1.558 ms (5%) |         |                 |             |
| `["splitby", "count", "man"]`                       |   1.166 ms (5%) |         |                 |             |
| `["splitby", "count", "reduce"]`                    | 826.435 μs (5%) |         |   1.09 KiB (1%) |          19 |
| `["sum", "random", "foldl"]`                        |  11.037 ms (5%) |         |                 |             |
| `["sum", "random", "reduce", "basesize=128"]`       |   5.619 ms (5%) |         |  74.17 KiB (1%) |        1104 |
| `["sum", "random", "reduce", "basesize=256"]`       |   5.590 ms (5%) |         |  36.73 KiB (1%) |         546 |
| `["sum", "random", "reduce", "basesize=512"]`       |   5.552 ms (5%) |         |  18.11 KiB (1%) |         270 |
| `["sum", "uniform", "foldl"]`                       |  10.918 ms (5%) |         |                 |             |
| `["sum", "uniform", "reduce", "basesize=128"]`      |   5.590 ms (5%) |         |  74.17 KiB (1%) |        1104 |
| `["sum", "uniform", "reduce", "basesize=256"]`      |   5.531 ms (5%) |         |  36.77 KiB (1%) |         547 |
| `["sum", "uniform", "reduce", "basesize=512"]`      |   5.498 ms (5%) |         |  18.03 KiB (1%) |         268 |
| `["sum", "valley", "foldl"]`                        |  11.168 ms (5%) |         |                 |             |
| `["sum", "valley", "reduce", "basesize=128"]`       |   5.719 ms (5%) |         |  74.11 KiB (1%) |        1102 |
| `["sum", "valley", "reduce", "basesize=256"]`       |   5.658 ms (5%) |         |  36.73 KiB (1%) |         546 |
| `["sum", "valley", "reduce", "basesize=512"]`       |   5.638 ms (5%) |         |  18.06 KiB (1%) |         269 |
| `["words", "nthreads=1"]`                           |  14.421 ms (5%) |         |  31.42 MiB (1%) |     1023580 |
| `["words", "nthreads=2"]`                           |   9.531 ms (5%) |         |  31.77 MiB (1%) |     1023616 |
| `["words", "nthreads=4"]`                           |  10.057 ms (5%) |         |  32.67 MiB (1%) |     1023769 |

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
      Ubuntu 22.04.5 LTS
  uname: Linux 6.8.0-1014-azure #16~22.04.1-Ubuntu SMP Thu Aug 15 21:31:41 UTC 2024 x86_64 x86_64
  CPU: AMD EPYC 7763 64-Core Processor: 
              speed         user         nice          sys         idle          irq
       #1  3242 MHz       3333 s          0 s        246 s       6623 s          0 s
       #2  3173 MHz       4352 s          0 s        289 s       5547 s          0 s
       #3  3183 MHz       3538 s          0 s        309 s       6362 s          0 s
       #4  2445 MHz       3264 s          0 s        271 s       6670 s          0 s
       
  Memory: 15.615272521972656 GB (12457.4453125 MB free)
  Uptime: 1024.02 sec
  Load Avg:  1.57  1.57  1.09
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
    BogoMIPS:                             4890.85
    Flags:                                fpu vme de pse tsc msr pae mce cx8 apic sep mtrr pge mca cmov pat pse36 clflush mmx fxsr sse sse2 ht syscall nx mmxext fxsr_opt pdpe1gb rdtscp lm constant_tsc rep_good nopl tsc_reliable nonstop_tsc cpuid extd_apicid aperfmperf pni pclmulqdq ssse3 fma cx16 pcid sse4_1 sse4_2 movbe popcnt aes xsave avx f16c rdrand hypervisor lahf_lm cmp_legacy svm cr8_legacy abm sse4a misalignsse 3dnowprefetch osvw topoext vmmcall fsgsbase bmi1 avx2 smep bmi2 erms invpcid rdseed adx smap clflushopt clwb sha_ni xsaveopt xsavec xgetbv1 xsaves user_shstk clzero xsaveerptr rdpru arat npt nrip_save tsc_scale vmcb_clean flushbyasid decodeassists pausefilter pfthreshold v_vmsave_vmload umip vaes vpclmulqdq rdpid fsrm
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

