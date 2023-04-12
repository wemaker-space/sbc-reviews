# SBC Reviews

Jin's SBC (Single-Board Computer) review and benchmarking data repo. (Inspired from Jeff Geerling Review repo)


## Motivation

I test a _lot_ of SBCs from Raspberry Pi, Radxa, Orange Pi, Pine64, ODROID, ASUS, and more.

But I decided I'd rather have a public repository with all the test data and review notes for all the SBCs I use and test.

Unless under NDA, my plan is to compile all my data here, in real-time, as a point of reference for myself and for anyone else who runs into interesting results (e.g. the RK3588 on the Rock 5 model B benchmarking _slower_ than the RK3588S on the Orange Pi 5).

## Methodology

For every board I test or review, I will open an Issue with the name of the SBC, and begin compiling data in that issue.

If you would like to see a board added that is not already listed, **please start a new [Discussion](https://github.com/geerlingguy/sbc-reviews/discussions)**—do not open an Issue until I have confirmed I am going to acquire and test a certain board.

The primary benchmarks I run are:

  - CPU: [Geekbench 5](https://www.geekbench.com/download/)
  - CPU: [Top500 HPL](https://github.com/geerlingguy/top500-benchmark)
  - CPU: TODO
  - GPU: TODO
  - Memory: TODO
  - Disk: [`disk-benchmark.sh`](https://github.com/geerlingguy/pi-cluster/blob/master/benchmarks/disk-benchmark.sh)
  - Disk: [PiBenchmarks.com](https://pibenchmarks.com)
  - Network: `iperf3` (upstream, downstream, and bidirectional)

I often test a variety of other board-specific features, too, though it depends on the amount of time I'm willing to devote to a specific board, whether I'll deep-dive or just get basic numbers.

## List of SBCs

All SBCs I have tested as part of this project are listed below. Click on the name of the SBC to view all the testing and benchmarking details.

| SBC Name | Year Introduced |
| --- | --- |
| [Radxa Rock 5 model B](https://github.com/geerlingguy/sbc-reviews/issues/3) | 2023 |
| [Orange Pi 5](https://github.com/geerlingguy/sbc-reviews/issues/5) | 2023 |
| [Banana Pi BPI-CM4](https://github.com/geerlingguy/sbc-reviews/issues/11) | 2022 |
| [StarFive VisionFive 2](https://github.com/geerlingguy/sbc-reviews/issues/10) | 2022 |
| [Radxa Rock 3 Compute Module](https://github.com/geerlingguy/sbc-reviews/issues/15) | 2021 |
| [Pine64 SOQuartz](https://github.com/geerlingguy/sbc-reviews/issues/7) | 2021 |
| [Raspberry Pi Compute Module 4](https://github.com/geerlingguy/sbc-reviews/issues/8) | 2020 |
| [Raspberry Pi 4 model B](https://github.com/geerlingguy/sbc-reviews/issues/4) | 2019 |
| [Raspberry Pi 3 model B+](https://github.com/geerlingguy/sbc-reviews/issues/16) | 2018 |

This table should be ordered by the date the board was launched, in descending order. I might add a CSV file (so it's still easy to manage by hand) which could be compiled into this README at some point in the future (that would also allow putting benchmark numbers directly into the CSV...).

## SBC Awards

I'm considering crowning certain SBCs with awards every year, like "Fastest storage" or "least functionality." That seems like it could be a fun way to blow off steam when I'm having a terrible experience, or celebrate some truly groundbreaking new features...

## Author

This repository is maintained by Jin.
