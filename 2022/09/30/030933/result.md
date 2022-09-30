# Multi-thread benchmark result

* Pull request commit: [`80e9417c1b4784a0fa416bae9601f8f4bcd36e77`](https://github.com/JuliaFolds/Transducers.jl/commit/80e9417c1b4784a0fa416bae9601f8f4bcd36e77)
* Pull request: <https://github.com/JuliaFolds/Transducers.jl/pull/243> (Update */Manifest.toml)

# Judge result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmarks:
    - Target: 30 Sep 2022 - 03:03
    - Baseline: 30 Sep 2022 - 03:09
* Package commits:
    - Target: f8364b
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
| `["findfirst", "n=1000", "reduce", "basesize=128"]` | 0.66 (5%) :white_check_mark: | 0.70 (1%) :white_check_mark: |
| `["findfirst", "n=1000", "reduce", "basesize=256"]` |                1.19 (5%) :x: |                1.12 (1%) :x: |
| `["findfirst", "n=1000", "reduce", "basesize=512"]` | 0.89 (5%) :white_check_mark: | 0.91 (1%) :white_check_mark: |
| `["findfirst", "n=400", "reduce", "basesize=256"]`  |                   0.99 (5%)  | 0.97 (1%) :white_check_mark: |
| `["findfirst", "n=400", "reduce", "basesize=512"]`  |                1.30 (5%) :x: |                1.30 (1%) :x: |
| `["findfirst", "n=500", "reduce", "basesize=128"]`  |                1.74 (5%) :x: |                1.49 (1%) :x: |
| `["findfirst", "n=500", "reduce", "basesize=256"]`  | 0.53 (5%) :white_check_mark: | 0.61 (1%) :white_check_mark: |
| `["parallel_histogram", "comm", "basesize=4096"]`   | 0.93 (5%) :white_check_mark: | 0.89 (1%) :white_check_mark: |
| `["parallel_histogram", "comm", "basesize=8192"]`   |                   1.02 (5%)  |                1.20 (1%) :x: |
| `["partition_length_maximum", "rand", "reduce"]`    |                   1.00 (5%)  |                1.05 (1%) :x: |
| `["splitby", "count", "man"]`                       |                1.24 (5%) :x: |                   1.00 (1%)  |
| `["splitby", "count", "reduce"]`                    |                1.06 (5%) :x: |                1.01 (1%) :x: |
| `["words", "nthreads=1"]`                           |                   0.96 (5%)  |                1.01 (1%) :x: |
| `["words", "nthreads=2"]`                           |                   0.97 (5%)  |                1.01 (1%) :x: |
| `["words", "nthreads=4"]`                           | 0.95 (5%) :white_check_mark: |                   1.00 (1%)  |

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
      Ubuntu 20.04.5 LTS
  uname: Linux 5.15.0-1020-azure #25~20.04.1-Ubuntu SMP Thu Sep 1 19:20:56 UTC 2022 x86_64 x86_64
  CPU: Intel(R) Xeon(R) Platinum 8272CL CPU @ 2.60GHz: 
              speed         user         nice          sys         idle          irq
       #1  2593 MHz       4697 s          2 s        256 s       1950 s          0 s
       #2  2593 MHz       5566 s          1 s        302 s       1071 s          0 s
       
  Memory: 6.781253814697266 GB (3675.05078125 MB free)
  Uptime: 698.81 sec
  Load Avg:  1.62  1.5  0.91
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
      Ubuntu 20.04.5 LTS
  uname: Linux 5.15.0-1020-azure #25~20.04.1-Ubuntu SMP Thu Sep 1 19:20:56 UTC 2022 x86_64 x86_64
  CPU: Intel(R) Xeon(R) Platinum 8272CL CPU @ 2.60GHz: 
              speed         user         nice          sys         idle          irq
       #1  2593 MHz       7033 s          2 s        318 s       2670 s          0 s
       #2  2593 MHz       8025 s          1 s        363 s       1668 s          0 s
       
  Memory: 6.781253814697266 GB (3627.26171875 MB free)
  Uptime: 1011.01 sec
  Load Avg:  1.65  1.6  1.13
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-12.0.1 (ORCJIT, skylake-avx512)
```

---
# Target result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmark: 30 Sep 2022 - 3:3
* Package commit: f8364b
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
| `["collect", "assoc", "basesize=1"]`                | 244.698 ms (5%) |         |   25.97 MiB (1%) |      306843 |
| `["collect", "assoc", "basesize=1024"]`             | 198.410 ms (5%) |         |    2.61 MiB (1%) |         456 |
| `["collect", "assoc", "basesize=32"]`               | 200.511 ms (5%) |         |    4.82 MiB (1%) |       11714 |
| `["collect", "seq"]`                                | 394.946 ms (5%) |         |  812.73 KiB (1%) |          11 |
| `["collect", "unordered", "basesize=1"]`            | 349.299 ms (5%) |         |   23.56 MiB (1%) |      401910 |
| `["collect", "unordered", "basesize=1024"]`         | 213.300 ms (5%) |         | 1001.61 KiB (1%) |         895 |
| `["collect", "unordered", "basesize=32"]`           | 224.230 ms (5%) |         |    1.58 MiB (1%) |       14681 |
| `["findfirst", "n=1000", "foldl"]`                  | 626.476 ms (5%) |         |                  |             |
| `["findfirst", "n=1000", "reduce", "basesize=128"]` | 353.242 ms (5%) |         |  240.97 KiB (1%) |        3383 |
| `["findfirst", "n=1000", "reduce", "basesize=256"]` | 505.147 ms (5%) |         |  176.34 KiB (1%) |        2479 |
| `["findfirst", "n=1000", "reduce", "basesize=512"]` | 503.727 ms (5%) |         |   98.45 KiB (1%) |        1373 |
| `["findfirst", "n=400", "foldl"]`                   | 470.084 ms (5%) |         |                  |             |
| `["findfirst", "n=400", "reduce", "basesize=128"]`  | 244.897 ms (5%) |         |  388.52 KiB (1%) |        5520 |
| `["findfirst", "n=400", "reduce", "basesize=256"]`  | 249.158 ms (5%) |         |  201.00 KiB (1%) |        2876 |
| `["findfirst", "n=400", "reduce", "basesize=512"]`  | 353.246 ms (5%) |         |  153.12 KiB (1%) |        2194 |
| `["findfirst", "n=500", "foldl"]`                   |  81.546 ms (5%) |         |                  |             |
| `["findfirst", "n=500", "reduce", "basesize=128"]`  | 199.741 ms (5%) |         |  267.16 KiB (1%) |        3753 |
| `["findfirst", "n=500", "reduce", "basesize=256"]`  |  76.822 ms (5%) |         |   74.52 KiB (1%) |        1011 |
| `["findfirst", "n=500", "reduce", "basesize=512"]`  | 116.506 ms (5%) |         |   63.66 KiB (1%) |         865 |
| `["overhead", "default"]`                           |  75.101 μs (5%) |         |   32.67 KiB (1%) |         416 |
| `["overhead", "stoppable=false"]`                   |  76.201 μs (5%) |         |   32.72 KiB (1%) |         417 |
| `["overhead", "stoppable=true"]`                    |  86.102 μs (5%) |         |   44.22 KiB (1%) |         609 |
| `["parallel_histogram", "assoc", "basesize=16384"]` |   3.227 ms (5%) |         |  728.91 KiB (1%) |          57 |
| `["parallel_histogram", "assoc", "basesize=4096"]`  |   3.890 ms (5%) |         |    1.79 MiB (1%) |         215 |
| `["parallel_histogram", "assoc", "basesize=8192"]`  |   3.573 ms (5%) |         |    1.42 MiB (1%) |         117 |
| `["parallel_histogram", "comm", "basesize=16384"]`  |  18.547 ms (5%) |         |    1.60 MiB (1%) |        2977 |
| `["parallel_histogram", "comm", "basesize=4096"]`   |  24.143 ms (5%) |         |    1.13 MiB (1%) |        3265 |
| `["parallel_histogram", "comm", "basesize=8192"]`   |  22.342 ms (5%) |         |    1.30 MiB (1%) |        5788 |
| `["parallel_histogram", "seq"]`                     |   5.748 ms (5%) |         |  364.16 KiB (1%) |          24 |
| `["partition_length_maximum", "rand", "foldl"]`     |  35.198 ms (5%) |         |                  |             |
| `["partition_length_maximum", "rand", "reduce"]`    |  17.616 ms (5%) |         |   736 bytes (1%) |          11 |
| `["splitby", "count", "foldl"]`                     |   2.319 ms (5%) |         |                  |             |
| `["splitby", "count", "man"]`                       |   1.752 ms (5%) |         |                  |             |
| `["splitby", "count", "reduce"]`                    |   1.146 ms (5%) |         |    1.06 KiB (1%) |          18 |
| `["sum", "random", "foldl"]`                        |  16.087 ms (5%) |         |                  |             |
| `["sum", "random", "reduce", "basesize=128"]`       |   8.113 ms (5%) |         |   74.14 KiB (1%) |        1103 |
| `["sum", "random", "reduce", "basesize=256"]`       |   8.019 ms (5%) |         |   36.70 KiB (1%) |         545 |
| `["sum", "random", "reduce", "basesize=512"]`       |   7.935 ms (5%) |         |   18.08 KiB (1%) |         269 |
| `["sum", "uniform", "foldl"]`                       |  15.700 ms (5%) |         |                  |             |
| `["sum", "uniform", "reduce", "basesize=128"]`      |   7.981 ms (5%) |         |   74.14 KiB (1%) |        1103 |
| `["sum", "uniform", "reduce", "basesize=256"]`      |   7.871 ms (5%) |         |   36.77 KiB (1%) |         547 |
| `["sum", "uniform", "reduce", "basesize=512"]`      |   7.823 ms (5%) |         |   18.03 KiB (1%) |         268 |
| `["sum", "valley", "foldl"]`                        |  16.077 ms (5%) |         |                  |             |
| `["sum", "valley", "reduce", "basesize=128"]`       |   8.184 ms (5%) |         |   74.11 KiB (1%) |        1102 |
| `["sum", "valley", "reduce", "basesize=256"]`       |   8.086 ms (5%) |         |   36.73 KiB (1%) |         546 |
| `["sum", "valley", "reduce", "basesize=512"]`       |   8.072 ms (5%) |         |   18.03 KiB (1%) |         268 |
| `["words", "nthreads=1"]`                           |  23.091 ms (5%) |         |   31.68 MiB (1%) |     1032609 |
| `["words", "nthreads=2"]`                           |  14.435 ms (5%) |         |   32.40 MiB (1%) |     1032686 |
| `["words", "nthreads=4"]`                           |  14.315 ms (5%) |         |   32.84 MiB (1%) |     1032784 |

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
      Ubuntu 20.04.5 LTS
  uname: Linux 5.15.0-1020-azure #25~20.04.1-Ubuntu SMP Thu Sep 1 19:20:56 UTC 2022 x86_64 x86_64
  CPU: Intel(R) Xeon(R) Platinum 8272CL CPU @ 2.60GHz: 
              speed         user         nice          sys         idle          irq
       #1  2593 MHz       4697 s          2 s        256 s       1950 s          0 s
       #2  2593 MHz       5566 s          1 s        302 s       1071 s          0 s
       
  Memory: 6.781253814697266 GB (3675.05078125 MB free)
  Uptime: 698.81 sec
  Load Avg:  1.62  1.5  0.91
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-12.0.1 (ORCJIT, skylake-avx512)
```

---
# Baseline result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmark: 30 Sep 2022 - 3:9
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
| `["collect", "assoc", "basesize=1"]`                | 244.888 ms (5%) |         |   25.97 MiB (1%) |      306856 |
| `["collect", "assoc", "basesize=1024"]`             | 198.881 ms (5%) |         |    2.61 MiB (1%) |         456 |
| `["collect", "assoc", "basesize=32"]`               | 200.793 ms (5%) |         |    4.82 MiB (1%) |       11710 |
| `["collect", "seq"]`                                | 395.123 ms (5%) |         |  812.73 KiB (1%) |          11 |
| `["collect", "unordered", "basesize=1"]`            | 344.850 ms (5%) |         |   23.89 MiB (1%) |      412640 |
| `["collect", "unordered", "basesize=1024"]`         | 213.384 ms (5%) |         | 1001.42 KiB (1%) |        1033 |
| `["collect", "unordered", "basesize=32"]`           | 223.432 ms (5%) |         |    1.58 MiB (1%) |       14604 |
| `["findfirst", "n=1000", "foldl"]`                  | 629.850 ms (5%) |         |                  |             |
| `["findfirst", "n=1000", "reduce", "basesize=128"]` | 538.820 ms (5%) |         |  345.00 KiB (1%) |        4892 |
| `["findfirst", "n=1000", "reduce", "basesize=256"]` | 422.905 ms (5%) |         |  157.20 KiB (1%) |        2193 |
| `["findfirst", "n=1000", "reduce", "basesize=512"]` | 565.291 ms (5%) |         |  108.58 KiB (1%) |        1510 |
| `["findfirst", "n=400", "foldl"]`                   | 472.389 ms (5%) |         |                  |             |
| `["findfirst", "n=400", "reduce", "basesize=128"]`  | 251.167 ms (5%) |         |  392.23 KiB (1%) |        5582 |
| `["findfirst", "n=400", "reduce", "basesize=256"]`  | 251.114 ms (5%) |         |  207.69 KiB (1%) |        2957 |
| `["findfirst", "n=400", "reduce", "basesize=512"]`  | 272.457 ms (5%) |         |  117.80 KiB (1%) |        1684 |
| `["findfirst", "n=500", "foldl"]`                   |  81.921 ms (5%) |         |                  |             |
| `["findfirst", "n=500", "reduce", "basesize=128"]`  | 115.077 ms (5%) |         |  179.47 KiB (1%) |        2440 |
| `["findfirst", "n=500", "reduce", "basesize=256"]`  | 145.399 ms (5%) |         |  122.62 KiB (1%) |        1684 |
| `["findfirst", "n=500", "reduce", "basesize=512"]`  | 117.202 ms (5%) |         |   63.69 KiB (1%) |         866 |
| `["overhead", "default"]`                           |  73.001 μs (5%) |         |   32.67 KiB (1%) |         416 |
| `["overhead", "stoppable=false"]`                   |  76.401 μs (5%) |         |   32.75 KiB (1%) |         418 |
| `["overhead", "stoppable=true"]`                    |  85.302 μs (5%) |         |   44.25 KiB (1%) |         610 |
| `["parallel_histogram", "assoc", "basesize=16384"]` |   3.234 ms (5%) |         |  728.91 KiB (1%) |          57 |
| `["parallel_histogram", "assoc", "basesize=4096"]`  |   3.870 ms (5%) |         |    1.79 MiB (1%) |         216 |
| `["parallel_histogram", "assoc", "basesize=8192"]`  |   3.579 ms (5%) |         |    1.42 MiB (1%) |         117 |
| `["parallel_histogram", "comm", "basesize=16384"]`  |  18.417 ms (5%) |         |    1.60 MiB (1%) |        3049 |
| `["parallel_histogram", "comm", "basesize=4096"]`   |  26.007 ms (5%) |         |    1.27 MiB (1%) |        7730 |
| `["parallel_histogram", "comm", "basesize=8192"]`   |  21.966 ms (5%) |         |    1.08 MiB (1%) |        1722 |
| `["parallel_histogram", "seq"]`                     |   5.767 ms (5%) |         |  364.16 KiB (1%) |          24 |
| `["partition_length_maximum", "rand", "foldl"]`     |  35.252 ms (5%) |         |                  |             |
| `["partition_length_maximum", "rand", "reduce"]`    |  17.594 ms (5%) |         |   704 bytes (1%) |          10 |
| `["splitby", "count", "foldl"]`                     |   2.235 ms (5%) |         |                  |             |
| `["splitby", "count", "man"]`                       |   1.418 ms (5%) |         |                  |             |
| `["splitby", "count", "reduce"]`                    |   1.085 ms (5%) |         |    1.05 KiB (1%) |          19 |
| `["sum", "random", "foldl"]`                        |  16.245 ms (5%) |         |                  |             |
| `["sum", "random", "reduce", "basesize=128"]`       |   8.186 ms (5%) |         |   74.17 KiB (1%) |        1104 |
| `["sum", "random", "reduce", "basesize=256"]`       |   8.089 ms (5%) |         |   36.73 KiB (1%) |         546 |
| `["sum", "random", "reduce", "basesize=512"]`       |   8.014 ms (5%) |         |   18.08 KiB (1%) |         269 |
| `["sum", "uniform", "foldl"]`                       |  15.737 ms (5%) |         |                  |             |
| `["sum", "uniform", "reduce", "basesize=128"]`      |   7.970 ms (5%) |         |   74.14 KiB (1%) |        1103 |
| `["sum", "uniform", "reduce", "basesize=256"]`      |   7.885 ms (5%) |         |   36.70 KiB (1%) |         545 |
| `["sum", "uniform", "reduce", "basesize=512"]`      |   7.818 ms (5%) |         |   18.00 KiB (1%) |         267 |
| `["sum", "valley", "foldl"]`                        |  16.143 ms (5%) |         |                  |             |
| `["sum", "valley", "reduce", "basesize=128"]`       |   8.235 ms (5%) |         |   74.08 KiB (1%) |        1101 |
| `["sum", "valley", "reduce", "basesize=256"]`       |   8.128 ms (5%) |         |   36.73 KiB (1%) |         546 |
| `["sum", "valley", "reduce", "basesize=512"]`       |   8.112 ms (5%) |         |   18.09 KiB (1%) |         270 |
| `["words", "nthreads=1"]`                           |  23.943 ms (5%) |         |   31.35 MiB (1%) |     1020729 |
| `["words", "nthreads=2"]`                           |  14.901 ms (5%) |         |   32.06 MiB (1%) |     1020824 |
| `["words", "nthreads=4"]`                           |  15.084 ms (5%) |         |   32.69 MiB (1%) |     1020969 |

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
      Ubuntu 20.04.5 LTS
  uname: Linux 5.15.0-1020-azure #25~20.04.1-Ubuntu SMP Thu Sep 1 19:20:56 UTC 2022 x86_64 x86_64
  CPU: Intel(R) Xeon(R) Platinum 8272CL CPU @ 2.60GHz: 
              speed         user         nice          sys         idle          irq
       #1  2593 MHz       7033 s          2 s        318 s       2670 s          0 s
       #2  2593 MHz       8025 s          1 s        363 s       1668 s          0 s
       
  Memory: 6.781253814697266 GB (3627.26171875 MB free)
  Uptime: 1011.01 sec
  Load Avg:  1.65  1.6  1.13
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
    Vulnerability Mmio stale data:   Vulnerable: Clear CPU buffers attempted, no microcode; SMT Host state unknown
    Vulnerability Retbleed:          Vulnerable
    Vulnerability Spec store bypass: Vulnerable
    Vulnerability Spectre v1:        Mitigation; usercopy/swapgs barriers and __user pointer sanitization
    Vulnerability Spectre v2:        Mitigation; Retpolines, STIBP disabled, RSB filling
    Vulnerability Srbds:             Not affected
    Vulnerability Tsx async abort:   Mitigation; Clear CPU buffers; SMT Host state unknown
    Flags:                           fpu vme de pse tsc msr pae mce cx8 apic sep mtrr pge mca cmov pat pse36 clflush mmx fxsr sse sse2 ss ht syscall nx pdpe1gb rdtscp lm constant_tsc rep_good nopl xtopology cpuid pni pclmulqdq ssse3 fma cx16 pcid sse4_1 sse4_2 movbe popcnt aes xsave avx f16c rdrand hypervisor lahf_lm abm 3dnowprefetch invpcid_single pti fsgsbase bmi1 hle avx2 smep bmi2 erms invpcid rtm avx512f avx512dq rdseed adx smap clflushopt avx512cd avx512bw avx512vl xsaveopt xsavec xsaves md_clear
    

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

