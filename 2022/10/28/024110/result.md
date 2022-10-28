# Multi-thread benchmark result

* Pull request commit: [`8bf49fa9f5c0af9bebc670de3f51dc8a1812495f`](https://github.com/JuliaFolds/Transducers.jl/commit/8bf49fa9f5c0af9bebc670de3f51dc8a1812495f)
* Pull request: <https://github.com/JuliaFolds/Transducers.jl/pull/243> (Update */Manifest.toml)

# Judge result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmarks:
    - Target: 28 Oct 2022 - 02:35
    - Baseline: 28 Oct 2022 - 02:40
* Package commits:
    - Target: 2d29a2
    - Baseline: 958213
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
| `["findfirst", "n=1000", "reduce", "basesize=512"]` | 0.64 (5%) :white_check_mark: | 0.71 (1%) :white_check_mark: |
| `["findfirst", "n=400", "reduce", "basesize=128"]`  |                1.08 (5%) :x: |                1.11 (1%) :x: |
| `["findfirst", "n=400", "reduce", "basesize=512"]`  |                1.14 (5%) :x: |                1.12 (1%) :x: |
| `["findfirst", "n=500", "reduce", "basesize=128"]`  |                1.15 (5%) :x: |                1.16 (1%) :x: |
| `["findfirst", "n=500", "reduce", "basesize=256"]`  |                1.24 (5%) :x: |                1.10 (1%) :x: |
| `["findfirst", "n=500", "reduce", "basesize=512"]`  | 0.52 (5%) :white_check_mark: | 0.59 (1%) :white_check_mark: |
| `["parallel_histogram", "comm", "basesize=16384"]`  |                1.08 (5%) :x: |                   0.99 (1%)  |
| `["parallel_histogram", "comm", "basesize=4096"]`   | 0.88 (5%) :white_check_mark: | 0.98 (1%) :white_check_mark: |
| `["parallel_histogram", "comm", "basesize=8192"]`   | 0.94 (5%) :white_check_mark: | 0.95 (1%) :white_check_mark: |
| `["partition_length_maximum", "rand", "reduce"]`    |                   1.01 (5%)  |                1.05 (1%) :x: |
| `["splitby", "count", "reduce"]`                    | 0.93 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["words", "nthreads=4"]`                           |                1.05 (5%) :x: | 0.99 (1%) :white_check_mark: |

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
  uname: Linux 5.15.0-1022-azure #27~20.04.1-Ubuntu SMP Mon Oct 17 02:03:50 UTC 2022 x86_64 x86_64
  CPU: Intel(R) Xeon(R) Platinum 8171M CPU @ 2.60GHz: 
              speed         user         nice          sys         idle          irq
       #1  2095 MHz       5280 s          1 s        281 s       1732 s          0 s
       #2  2095 MHz       5456 s          2 s        293 s       1549 s          0 s
       
  Memory: 6.78125 GB (3745.59375 MB free)
  Uptime: 736.62 sec
  Load Avg:  1.57  1.5  0.98
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
  uname: Linux 5.15.0-1022-azure #27~20.04.1-Ubuntu SMP Mon Oct 17 02:03:50 UTC 2022 x86_64 x86_64
  CPU: Intel(R) Xeon(R) Platinum 8171M CPU @ 2.60GHz: 
              speed         user         nice          sys         idle          irq
       #1  2095 MHz       7702 s          1 s        347 s       2488 s          0 s
       #2  2095 MHz       7986 s          2 s        359 s       2200 s          0 s
       
  Memory: 6.78125 GB (3723.15625 MB free)
  Uptime: 1061.92 sec
  Load Avg:  1.67  1.59  1.17
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-12.0.1 (ORCJIT, skylake-avx512)
```

---
# Target result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmark: 28 Oct 2022 - 2:35
* Package commit: 2d29a2
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
| `["collect", "assoc", "basesize=1"]`                | 310.889 ms (5%) |         |   25.97 MiB (1%) |      306786 |
| `["collect", "assoc", "basesize=1024"]`             | 252.260 ms (5%) |         |    2.61 MiB (1%) |         456 |
| `["collect", "assoc", "basesize=32"]`               | 251.355 ms (5%) |         |    4.82 MiB (1%) |       11716 |
| `["collect", "seq"]`                                | 493.898 ms (5%) |         |  812.73 KiB (1%) |          11 |
| `["collect", "unordered", "basesize=1"]`            | 434.949 ms (5%) |         |   23.78 MiB (1%) |      409220 |
| `["collect", "unordered", "basesize=1024"]`         | 270.308 ms (5%) |         | 1004.17 KiB (1%) |        1034 |
| `["collect", "unordered", "basesize=32"]`           | 283.520 ms (5%) |         |    1.58 MiB (1%) |       14604 |
| `["findfirst", "n=1000", "foldl"]`                  | 781.593 ms (5%) |         |                  |             |
| `["findfirst", "n=1000", "reduce", "basesize=128"]` | 428.170 ms (5%) |         |  232.83 KiB (1%) |        3275 |
| `["findfirst", "n=1000", "reduce", "basesize=256"]` | 525.244 ms (5%) |         |  155.69 KiB (1%) |        2174 |
| `["findfirst", "n=1000", "reduce", "basesize=512"]` | 717.103 ms (5%) |         |  111.81 KiB (1%) |        1554 |
| `["findfirst", "n=400", "foldl"]`                   | 595.601 ms (5%) |         |                  |             |
| `["findfirst", "n=400", "reduce", "basesize=128"]`  | 338.023 ms (5%) |         |  415.03 KiB (1%) |        5905 |
| `["findfirst", "n=400", "reduce", "basesize=256"]`  | 313.981 ms (5%) |         |  201.17 KiB (1%) |        2883 |
| `["findfirst", "n=400", "reduce", "basesize=512"]`  | 433.260 ms (5%) |         |  140.66 KiB (1%) |        2025 |
| `["findfirst", "n=500", "foldl"]`                   | 101.724 ms (5%) |         |                  |             |
| `["findfirst", "n=500", "reduce", "basesize=128"]`  | 252.576 ms (5%) |         |  279.17 KiB (1%) |        3879 |
| `["findfirst", "n=500", "reduce", "basesize=256"]`  | 238.714 ms (5%) |         |  131.06 KiB (1%) |        1837 |
| `["findfirst", "n=500", "reduce", "basesize=512"]`  | 132.832 ms (5%) |         |   55.91 KiB (1%) |         763 |
| `["overhead", "default"]`                           |  88.910 μs (5%) |         |   32.73 KiB (1%) |         418 |
| `["overhead", "stoppable=false"]`                   |  90.910 μs (5%) |         |   32.75 KiB (1%) |         418 |
| `["overhead", "stoppable=true"]`                    | 101.908 μs (5%) |         |   44.22 KiB (1%) |         609 |
| `["parallel_histogram", "assoc", "basesize=16384"]` |   4.019 ms (5%) |         |  728.91 KiB (1%) |          57 |
| `["parallel_histogram", "assoc", "basesize=4096"]`  |   4.834 ms (5%) |         |    1.79 MiB (1%) |         216 |
| `["parallel_histogram", "assoc", "basesize=8192"]`  |   4.442 ms (5%) |         |    1.42 MiB (1%) |         117 |
| `["parallel_histogram", "comm", "basesize=16384"]`  |  21.517 ms (5%) |         |    1.59 MiB (1%) |        2650 |
| `["parallel_histogram", "comm", "basesize=4096"]`   |  23.786 ms (5%) |         |    1.18 MiB (1%) |        4721 |
| `["parallel_histogram", "comm", "basesize=8192"]`   |  23.678 ms (5%) |         |    1.17 MiB (1%) |        3716 |
| `["parallel_histogram", "seq"]`                     |   7.162 ms (5%) |         |  364.16 KiB (1%) |          24 |
| `["partition_length_maximum", "rand", "foldl"]`     |  44.457 ms (5%) |         |                  |             |
| `["partition_length_maximum", "rand", "reduce"]`    |  22.195 ms (5%) |         |   736 bytes (1%) |          11 |
| `["splitby", "count", "foldl"]`                     |   2.777 ms (5%) |         |                  |             |
| `["splitby", "count", "man"]`                       |   1.771 ms (5%) |         |                  |             |
| `["splitby", "count", "reduce"]`                    |   1.353 ms (5%) |         |    1.09 KiB (1%) |          19 |
| `["sum", "random", "foldl"]`                        |  20.159 ms (5%) |         |                  |             |
| `["sum", "random", "reduce", "basesize=128"]`       |  10.161 ms (5%) |         |   74.17 KiB (1%) |        1104 |
| `["sum", "random", "reduce", "basesize=256"]`       |  10.061 ms (5%) |         |   36.73 KiB (1%) |         546 |
| `["sum", "random", "reduce", "basesize=512"]`       |   9.993 ms (5%) |         |   18.08 KiB (1%) |         269 |
| `["sum", "uniform", "foldl"]`                       |  19.639 ms (5%) |         |                  |             |
| `["sum", "uniform", "reduce", "basesize=128"]`      |   9.925 ms (5%) |         |   74.14 KiB (1%) |        1103 |
| `["sum", "uniform", "reduce", "basesize=256"]`      |   9.825 ms (5%) |         |   36.77 KiB (1%) |         547 |
| `["sum", "uniform", "reduce", "basesize=512"]`      |   9.742 ms (5%) |         |   18.00 KiB (1%) |         267 |
| `["sum", "valley", "foldl"]`                        |  20.114 ms (5%) |         |                  |             |
| `["sum", "valley", "reduce", "basesize=128"]`       |  10.260 ms (5%) |         |   74.11 KiB (1%) |        1102 |
| `["sum", "valley", "reduce", "basesize=256"]`       |  10.212 ms (5%) |         |   36.61 KiB (1%) |         542 |
| `["sum", "valley", "reduce", "basesize=512"]`       |  10.189 ms (5%) |         |   18.00 KiB (1%) |         267 |
| `["words", "nthreads=1"]`                           |  29.232 ms (5%) |         |   31.73 MiB (1%) |     1034243 |
| `["words", "nthreads=2"]`                           |  18.444 ms (5%) |         |   32.45 MiB (1%) |     1034324 |
| `["words", "nthreads=4"]`                           |  18.489 ms (5%) |         |   32.89 MiB (1%) |     1034391 |

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
  uname: Linux 5.15.0-1022-azure #27~20.04.1-Ubuntu SMP Mon Oct 17 02:03:50 UTC 2022 x86_64 x86_64
  CPU: Intel(R) Xeon(R) Platinum 8171M CPU @ 2.60GHz: 
              speed         user         nice          sys         idle          irq
       #1  2095 MHz       5280 s          1 s        281 s       1732 s          0 s
       #2  2095 MHz       5456 s          2 s        293 s       1549 s          0 s
       
  Memory: 6.78125 GB (3745.59375 MB free)
  Uptime: 736.62 sec
  Load Avg:  1.57  1.5  0.98
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-12.0.1 (ORCJIT, skylake-avx512)
```

---
# Baseline result
# Benchmark Report for */home/runner/work/Transducers.jl/Transducers.jl*

## Job Properties
* Time of benchmark: 28 Oct 2022 - 2:40
* Package commit: 958213
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
| `["collect", "assoc", "basesize=1"]`                | 310.620 ms (5%) |         |   25.97 MiB (1%) |      306851 |
| `["collect", "assoc", "basesize=1024"]`             | 248.348 ms (5%) |         |    2.61 MiB (1%) |         455 |
| `["collect", "assoc", "basesize=32"]`               | 250.860 ms (5%) |         |    4.82 MiB (1%) |       11721 |
| `["collect", "seq"]`                                | 494.162 ms (5%) |         |  812.73 KiB (1%) |          11 |
| `["collect", "unordered", "basesize=1"]`            | 430.291 ms (5%) |         |   23.90 MiB (1%) |      413006 |
| `["collect", "unordered", "basesize=1024"]`         | 269.668 ms (5%) |         | 1004.89 KiB (1%) |         782 |
| `["collect", "unordered", "basesize=32"]`           | 278.393 ms (5%) |         |    1.58 MiB (1%) |       14757 |
| `["findfirst", "n=1000", "foldl"]`                  | 787.816 ms (5%) |         |                  |             |
| `["findfirst", "n=1000", "reduce", "basesize=128"]` | 442.543 ms (5%) |         |  232.86 KiB (1%) |        3274 |
| `["findfirst", "n=1000", "reduce", "basesize=256"]` | 530.401 ms (5%) |         |  154.91 KiB (1%) |        2164 |
| `["findfirst", "n=1000", "reduce", "basesize=512"]` |    1.115 s (5%) |         |  156.47 KiB (1%) |        2182 |
| `["findfirst", "n=400", "foldl"]`                   | 591.040 ms (5%) |         |                  |             |
| `["findfirst", "n=400", "reduce", "basesize=128"]`  | 312.494 ms (5%) |         |  374.59 KiB (1%) |        5351 |
| `["findfirst", "n=400", "reduce", "basesize=256"]`  | 312.949 ms (5%) |         |  200.80 KiB (1%) |        2871 |
| `["findfirst", "n=400", "reduce", "basesize=512"]`  | 380.625 ms (5%) |         |  125.62 KiB (1%) |        1795 |
| `["findfirst", "n=500", "foldl"]`                   | 102.489 ms (5%) |         |                  |             |
| `["findfirst", "n=500", "reduce", "basesize=128"]`  | 219.367 ms (5%) |         |  241.55 KiB (1%) |        3353 |
| `["findfirst", "n=500", "reduce", "basesize=256"]`  | 192.604 ms (5%) |         |  119.03 KiB (1%) |        1643 |
| `["findfirst", "n=500", "reduce", "basesize=512"]`  | 257.573 ms (5%) |         |   94.42 KiB (1%) |        1287 |
| `["overhead", "default"]`                           |  88.207 μs (5%) |         |   32.70 KiB (1%) |         417 |
| `["overhead", "stoppable=false"]`                   |  87.207 μs (5%) |         |   32.75 KiB (1%) |         418 |
| `["overhead", "stoppable=true"]`                    | 103.008 μs (5%) |         |   44.22 KiB (1%) |         609 |
| `["parallel_histogram", "assoc", "basesize=16384"]` |   4.053 ms (5%) |         |  728.91 KiB (1%) |          57 |
| `["parallel_histogram", "assoc", "basesize=4096"]`  |   4.842 ms (5%) |         |    1.79 MiB (1%) |         215 |
| `["parallel_histogram", "assoc", "basesize=8192"]`  |   4.473 ms (5%) |         |    1.42 MiB (1%) |         117 |
| `["parallel_histogram", "comm", "basesize=16384"]`  |  19.993 ms (5%) |         |    1.60 MiB (1%) |        3002 |
| `["parallel_histogram", "comm", "basesize=4096"]`   |  26.995 ms (5%) |         |    1.20 MiB (1%) |        5512 |
| `["parallel_histogram", "comm", "basesize=8192"]`   |  25.101 ms (5%) |         |    1.24 MiB (1%) |        4842 |
| `["parallel_histogram", "seq"]`                     |   7.210 ms (5%) |         |  364.16 KiB (1%) |          24 |
| `["partition_length_maximum", "rand", "foldl"]`     |  44.050 ms (5%) |         |                  |             |
| `["partition_length_maximum", "rand", "reduce"]`    |  22.026 ms (5%) |         |   704 bytes (1%) |          10 |
| `["splitby", "count", "foldl"]`                     |   2.775 ms (5%) |         |                  |             |
| `["splitby", "count", "man"]`                       |   1.776 ms (5%) |         |                  |             |
| `["splitby", "count", "reduce"]`                    |   1.452 ms (5%) |         |    1.09 KiB (1%) |          19 |
| `["sum", "random", "foldl"]`                        |  20.466 ms (5%) |         |                  |             |
| `["sum", "random", "reduce", "basesize=128"]`       |  10.236 ms (5%) |         |   74.11 KiB (1%) |        1102 |
| `["sum", "random", "reduce", "basesize=256"]`       |  10.182 ms (5%) |         |   36.73 KiB (1%) |         546 |
| `["sum", "random", "reduce", "basesize=512"]`       |  10.104 ms (5%) |         |   18.05 KiB (1%) |         268 |
| `["sum", "uniform", "foldl"]`                       |  19.680 ms (5%) |         |                  |             |
| `["sum", "uniform", "reduce", "basesize=128"]`      |   9.979 ms (5%) |         |   74.20 KiB (1%) |        1105 |
| `["sum", "uniform", "reduce", "basesize=256"]`      |   9.853 ms (5%) |         |   36.77 KiB (1%) |         547 |
| `["sum", "uniform", "reduce", "basesize=512"]`      |   9.793 ms (5%) |         |   18.06 KiB (1%) |         269 |
| `["sum", "valley", "foldl"]`                        |  20.183 ms (5%) |         |                  |             |
| `["sum", "valley", "reduce", "basesize=128"]`       |  10.326 ms (5%) |         |   74.05 KiB (1%) |        1100 |
| `["sum", "valley", "reduce", "basesize=256"]`       |  10.194 ms (5%) |         |   36.73 KiB (1%) |         546 |
| `["sum", "valley", "reduce", "basesize=512"]`       |  10.164 ms (5%) |         |   18.03 KiB (1%) |         268 |
| `["words", "nthreads=1"]`                           |  28.329 ms (5%) |         |   32.00 MiB (1%) |     1042868 |
| `["words", "nthreads=2"]`                           |  17.582 ms (5%) |         |   32.36 MiB (1%) |     1042939 |
| `["words", "nthreads=4"]`                           |  17.584 ms (5%) |         |   33.25 MiB (1%) |     1043081 |

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
  uname: Linux 5.15.0-1022-azure #27~20.04.1-Ubuntu SMP Mon Oct 17 02:03:50 UTC 2022 x86_64 x86_64
  CPU: Intel(R) Xeon(R) Platinum 8171M CPU @ 2.60GHz: 
              speed         user         nice          sys         idle          irq
       #1  2095 MHz       7702 s          1 s        347 s       2488 s          0 s
       #2  2095 MHz       7986 s          2 s        359 s       2200 s          0 s
       
  Memory: 6.78125 GB (3723.15625 MB free)
  Uptime: 1061.92 sec
  Load Avg:  1.67  1.59  1.17
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
    Model name:                      Intel(R) Xeon(R) Platinum 8171M CPU @ 2.60GHz
    Stepping:                        4
    CPU MHz:                         2095.194
    BogoMIPS:                        4190.38
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
    Vulnerability Spectre v2:        Mitigation; Retpolines, STIBP disabled, RSB filling, PBRSB-eIBRS Not affected
    Vulnerability Srbds:             Not affected
    Vulnerability Tsx async abort:   Mitigation; Clear CPU buffers; SMT Host state unknown
    Flags:                           fpu vme de pse tsc msr pae mce cx8 apic sep mtrr pge mca cmov pat pse36 clflush mmx fxsr sse sse2 ss ht syscall nx pdpe1gb rdtscp lm constant_tsc rep_good nopl xtopology cpuid pni pclmulqdq ssse3 fma cx16 pcid sse4_1 sse4_2 movbe popcnt aes xsave avx f16c rdrand hypervisor lahf_lm abm 3dnowprefetch invpcid_single pti fsgsbase bmi1 hle avx2 smep bmi2 erms invpcid rtm mpx avx512f avx512dq rdseed adx smap clflushopt avx512cd avx512bw avx512vl xsaveopt xsavec xsaves md_clear
    

| Cpu Property       | Value                                                   |
|:------------------ |:------------------------------------------------------- |
| Brand              | Intel(R) Xeon(R) Platinum 8171M CPU @ 2.60GHz           |
| Vendor             | :Intel                                                  |
| Architecture       | :Skylake                                                |
| Model              | Family: 0x06, Model: 0x55, Stepping: 0x04, Type: 0x00   |
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

