sbc-bench v0.9.40 BQ-H616 (Wed, 12 Apr 2023 14:57:58 +0800)

Distributor ID:	Debian
Description:	Debian GNU/Linux 11 (bullseye)
Release:	11
Codename:	bullseye

/usr/bin/gcc (Debian 10.2.1-6) 10.2.1 20210110

Uptime: 14:57:59 up  1:42,  2 users,  load average: 0.96, 0.88, 0.48,  51.4°C,  493341835

Linux 5.16.17-sun50iw9 (BTT-CB1) 	04/12/23 	_aarch64_	(4 CPU)

avg-cpu:  %user   %nice %system %iowait  %steal   %idle
           2.43    0.00    1.06    0.07    0.00   96.43

Device             tps    kB_read/s    kB_wrtn/s    kB_dscd/s    kB_read    kB_wrtn    kB_dscd
mmcblk2           9.80        72.29       143.14         0.00     443926     879012          0
zram0             0.05         0.22         0.00         0.00       1332          4          0
zram1             0.01         0.01         0.01         0.00         68         72          0

               total        used        free      shared  buff/cache   available
Mem:           986Mi       148Mi       744Mi       0.0Ki        93Mi       772Mi
Swap:          493Mi          0B       493Mi

Filename				Type		Size	Used	Priority
/dev/zram0                             	partition	505316	0	5

##########################################################################

Checking cpufreq OPP (Cortex-A53):

No cpufreq support available. Measured on cpu1: 1006 MHz (1006.566/1006.494/1006.398)

##########################################################################

Hardware sensors:

cpu_thermal-virtual-0
temp1:        +54.7 C  (crit = +105.0 C)

gpu_thermal-virtual-0
temp1:        +54.6 C  

ddr_thermal-virtual-0
temp1:        +54.3 C  

ve_thermal-virtual-0
temp1:        +54.2 C  

##########################################################################

Executing benchmark on cpu0 (Cortex-A53):

tinymembench v0.4.9-nuumio (simple benchmark for memory throughput and latency)

CFLAGS: 
bandwidth test min repeats (-b): 2
bandwidth test max repeats (-B): 3
bandwidth test mem realloc (-M): no      (-m for realloc)
      latency test repeats (-l): 3
        latency test count (-c): 1000000

==========================================================================
== Memory bandwidth tests                                               ==
==                                                                      ==
== Note 1: 1MB = 1000000 bytes                                          ==
== Note 2: Test result is the best of repeated runs. Number of repeats  ==
==         is shown in brackets                                         ==
== Note 3: Results for 'copy' tests show how many bytes can be          ==
==         copied per second (adding together read and writen           ==
==         bytes would have provided twice higher numbers)              ==
== Note 4: 2-pass copy means that we are using a small temporary buffer ==
==         to first fetch data into it, and only then write it to the   ==
==         destination (source -> L1 cache, L1 cache -> destination)    ==
== Note 5: If sample standard deviation exceeds 0.1%, it is shown in    ==
==         brackets                                                     ==
==========================================================================

 C copy backwards                                 :   1480.0 MB/s (3, 14.4%)
 C copy backwards (32 byte blocks)                :   1480.4 MB/s (3, 1.9%)
 C copy backwards (64 byte blocks)                :   1508.8 MB/s (3, 1.7%)
 C copy                                           :   1474.4 MB/s (3, 1.3%)
 C copy prefetched (32 bytes step)                :   1068.5 MB/s (3, 3.1%)
 C copy prefetched (64 bytes step)                :   1127.2 MB/s (3, 1.1%)
 C 2-pass copy                                    :   1169.5 MB/s (3, 0.5%)
 C 2-pass copy prefetched (32 bytes step)         :    853.2 MB/s (3, 0.4%)
 C 2-pass copy prefetched (64 bytes step)         :    824.0 MB/s (3, 1.7%)
 C scan 8                                         :    196.7 MB/s (3, 0.2%)
 C scan 16                                        :    389.8 MB/s (3, 0.3%)
 C scan 32                                        :    760.8 MB/s (3, 0.4%)
 C scan 64                                        :   1361.5 MB/s (3, 2.6%)
 C fill                                           :   5232.3 MB/s (3, 1.4%)
 C fill (shuffle within 16 byte blocks)           :   5218.3 MB/s (3, 1.5%)
 C fill (shuffle within 32 byte blocks)           :   5229.9 MB/s (3, 0.5%)
 C fill (shuffle within 64 byte blocks)           :   5207.6 MB/s (3, 1.2%)
 ---
 libc memcpy copy                                 :   1564.4 MB/s (3, 2.7%)
 libc memchr scan                                 :   1515.6 MB/s (3, 1.3%)
 libc memset fill                                 :   5127.9 MB/s (2)
 ---
 NEON LDP/STP copy                                :   1530.9 MB/s (3, 1.9%)
 NEON LDP/STP copy pldl2strm (32 bytes step)      :    955.2 MB/s (2)
 NEON LDP/STP copy pldl2strm (64 bytes step)      :   1223.4 MB/s (3, 0.9%)
 NEON LDP/STP copy pldl1keep (32 bytes step)      :   1621.6 MB/s (3, 1.4%)
 NEON LDP/STP copy pldl1keep (64 bytes step)      :   1642.7 MB/s (3, 3.4%)
 NEON LD1/ST1 copy                                :   1492.8 MB/s (3, 0.4%)
 NEON LDP load                                    :   1855.5 MB/s (3, 1.6%)
 NEON LDNP load                                   :   1693.6 MB/s (3, 2.0%)
 NEON STP fill                                    :   5239.5 MB/s (3, 1.4%)
 NEON STNP fill                                   :   4219.8 MB/s (3, 2.2%)
 ARM LDP/STP copy                                 :   1530.0 MB/s (3, 1.9%)
 ARM LDP load                                     :   1861.9 MB/s (3, 1.9%)
 ARM LDNP load                                    :   1689.7 MB/s (3, 2.0%)
 ARM STP fill                                     :   5084.1 MB/s (2)
 ARM STNP fill                                    :   4189.4 MB/s (3, 2.2%)

==========================================================================
== Memory latency test                                                  ==
==                                                                      ==
== Average time is measured for random memory accesses in the buffers   ==
== of different sizes. The larger is the buffer, the more significant   ==
== are relative contributions of TLB, L1/L2 cache misses and SDRAM      ==
== accesses. For extremely large buffer sizes we are expecting to see   ==
== page table walk with several requests to SDRAM for almost every      ==
== memory access (though 64MiB is not nearly large enough to experience ==
== this effect to its fullest).                                         ==
==                                                                      ==
== Note 1: All the numbers are representing extra time, which needs to  ==
==         be added to L1 cache latency. The cycle timings for L1 cache ==
==         latency can be usually found in the processor documentation. ==
== Note 2: Dual random read means that we are simultaneously performing ==
==         two independent memory accesses at a time. In the case if    ==
==         the memory subsystem can't handle multiple outstanding       ==
==         requests, dual random read has the same timings as two       ==
==         single reads performed one after another.                    ==
==========================================================================

block size : single random read / dual random read, [MADV_NOHUGEPAGE]
      1024 :    0.0 ns          /     0.0 ns 
      2048 :    0.0 ns          /     0.0 ns 
      4096 :    0.0 ns          /     0.0 ns 
      8192 :    0.0 ns          /     0.0 ns 
     16384 :    0.0 ns          /     0.0 ns 
     32768 :    0.1 ns          /     0.0 ns 
     65536 :    6.6 ns          /    11.1 ns 
    131072 :   10.2 ns          /    15.8 ns 
    262144 :   15.0 ns          /    21.9 ns 
    524288 :   87.8 ns          /   133.3 ns 
   1048576 :  130.4 ns          /   172.7 ns 
   2097152 :  152.8 ns          /   186.4 ns 
   4194304 :  172.4 ns          /   202.3 ns 
   8388608 :  182.0 ns          /   211.8 ns 
  16777216 :  189.7 ns          /   218.8 ns 
  33554432 :  193.7 ns          /   225.3 ns 
  67108864 :  208.8 ns          /   252.5 ns 

block size : single random read / dual random read, [MADV_HUGEPAGE]
      1024 :    0.0 ns          /     0.0 ns 
      2048 :    0.0 ns          /     0.0 ns 
      4096 :    0.0 ns          /     0.0 ns 
      8192 :    0.0 ns          /     0.0 ns 
     16384 :    0.0 ns          /     0.0 ns 
     32768 :    0.1 ns          /     0.0 ns 
     65536 :    6.6 ns          /    11.1 ns 
    131072 :   10.2 ns          /    15.7 ns 
    262144 :   13.8 ns          /    19.1 ns 
    524288 :   87.6 ns          /   133.8 ns 
   1048576 :  131.2 ns          /   173.0 ns 
   2097152 :  152.2 ns          /   185.3 ns 
   4194304 :  163.1 ns          /   190.1 ns 
   8388608 :  167.5 ns          /   191.4 ns 
  16777216 :  170.6 ns          /   192.2 ns 
  33554432 :  172.5 ns          /   192.8 ns 
  67108864 :  173.1 ns          /   192.7 ns 

##########################################################################

Executing ramlat on cpu0 (Cortex-A53), results in ns:

       size:  1x32  2x32  1x64  2x64 1xPTR 2xPTR 4xPTR 8xPTR
         4k: 4.011 4.063 3.012 3.000 2.987 2.986 4.105 8.334 
         8k: 3.980 3.992 2.986 2.990 2.987 2.987 4.131 8.336 
        16k: 3.983 3.983 2.999 2.997 2.995 2.999 4.104 8.339 
        32k: 8.496 10.92 7.797 10.34 7.802 10.61 15.87 29.22 
        64k: 24.06 26.26 22.91 24.89 22.94 25.08 35.90 67.71 
       128k: 26.11 27.23 24.81 26.20 24.84 26.33 38.53 77.85 
       256k: 41.81 55.53 41.56 56.36 40.32 49.85 80.95 159.4 
       512k: 169.0 173.3 170.3 175.3 165.9 166.0 240.2 477.8 
      1024k: 180.6 182.6 178.2 181.2 178.3 178.4 245.8 493.3 
      2048k: 183.6 182.3 179.0 182.1 178.6 181.9 245.5 498.5 
      4096k: 190.7 192.0 190.3 194.7 189.3 190.6 259.1 518.4 
      8192k: 193.6 196.3 191.2 194.3 193.9 193.5 264.5 530.8 
     16384k: 202.2 201.7 195.7 200.5 195.9 200.4 269.0 559.0 
     32768k: 206.8 204.2 197.7 203.3 197.9 203.7 270.4 559.6 
     65536k: 226.9 200.6 198.2 200.6 205.8 201.0 268.2 581.4 
    131072k: 224.7 249.3 222.1 225.1 240.6 233.3 300.0 605.7 

##########################################################################

Executing benchmark twice on cluster 0 (Cortex-A53)

OpenSSL 1.1.1n, built on 15 Mar 2022
type             16 bytes     64 bytes    256 bytes   1024 bytes   8192 bytes  16384 bytes
aes-128-cbc      65308.23k   208068.59k   445028.52k   649117.01k   749199.36k   755870.38k
aes-128-cbc      65389.67k   207643.58k   444223.66k   648155.14k   747446.27k   754854.57k
aes-192-cbc      62452.06k   188008.23k   371105.79k   504670.21k   564172.12k   568076.97k
aes-192-cbc      62626.42k   188420.74k   371661.82k   505677.82k   564985.86k   569633.45k
aes-256-cbc      61192.85k   176025.79k   326405.63k   425506.82k   466731.01k   464841.39k
aes-256-cbc      61163.81k   176234.99k   326281.56k   425387.69k   466709.16k   465534.98k

##########################################################################

Executing benchmark single-threaded on cpu0 (Cortex-A53)

7-Zip (a) [64] 16.02 : Copyright (c) 1999-2016 Igor Pavlov : 2016-05-21
p7zip Version 16.02 (locale=C,Utf16=off,HugeFiles=on,64 bits,4 CPUs LE)

LE
CPU Freq: 64000000 - - - - - - - -

RAM size:     986 MB,  # CPU hardware threads:   4
RAM usage:    435 MB,  # Benchmark threads:      1

                       Compressing  |                  Decompressing
Dict     Speed Usage    R/U Rating  |      Speed Usage    R/U Rating
         KiB/s     %   MIPS   MIPS  |      KiB/s     %   MIPS   MIPS

22:        616   100    600    600  |      11033   100    942    942
23:        582   100    593    593  |      10844   100    939    939
24:        554   100    596    596  |      10650   100    935    935
25:        530   100    606    606  |      10419   100    928    927
----------------------------------  | ------------------------------
Avr:             100    599    599  |              100    936    936
Tot:             100    768    767

##########################################################################

Executing benchmark 3 times multi-threaded on CPUs 0-3

7-Zip (a) [64] 16.02 : Copyright (c) 1999-2016 Igor Pavlov : 2016-05-21
p7zip Version 16.02 (locale=C,Utf16=off,HugeFiles=on,64 bits,4 CPUs LE)

LE
CPU Freq: 64000000 - - - - - 512000000 1024000000 2048000000

RAM size:     986 MB,  # CPU hardware threads:   4
RAM usage:    882 MB,  # Benchmark threads:      4

                       Compressing  |                  Decompressing
Dict     Speed Usage    R/U Rating  |      Speed Usage    R/U Rating
         KiB/s     %   MIPS   MIPS  |      KiB/s     %   MIPS   MIPS

22:       1730   315    534   1683  |      41368   384    919   3529
23:       1690   325    530   1722  |      41204   390    914   3565
24:       1666   335    535   1792  |      40495   391    909   3555
25:       1271   301    483   1452  |      39298   390    897   3497
----------------------------------  | ------------------------------
Avr:             319    520   1662  |              389    910   3537
Tot:             354    715   2599

7-Zip (a) [64] 16.02 : Copyright (c) 1999-2016 Igor Pavlov : 2016-05-21
p7zip Version 16.02 (locale=C,Utf16=off,HugeFiles=on,64 bits,4 CPUs LE)

LE
CPU Freq: 64000000 - - - - - - - -

RAM size:     986 MB,  # CPU hardware threads:   4
RAM usage:    882 MB,  # Benchmark threads:      4

                       Compressing  |                  Decompressing
Dict     Speed Usage    R/U Rating  |      Speed Usage    R/U Rating
         KiB/s     %   MIPS   MIPS  |      KiB/s     %   MIPS   MIPS

22:       1734   316    534   1688  |      41621   387    919   3551
23:       1694   325    532   1726  |      40732   386    913   3524
24:       1682   336    538   1809  |      40502   391    909   3556
25:       1327   306    496   1515  |      39170   389    897   3486
----------------------------------  | ------------------------------
Avr:             321    525   1685  |              388    909   3529
Tot:             354    717   2607

7-Zip (a) [64] 16.02 : Copyright (c) 1999-2016 Igor Pavlov : 2016-05-21
p7zip Version 16.02 (locale=C,Utf16=off,HugeFiles=on,64 bits,4 CPUs LE)

LE
CPU Freq: - - - - - - - 1024000000 2048000000

RAM size:     986 MB,  # CPU hardware threads:   4
RAM usage:    882 MB,  # Benchmark threads:      4

                       Compressing  |                  Decompressing
Dict     Speed Usage    R/U Rating  |      Speed Usage    R/U Rating
         KiB/s     %   MIPS   MIPS  |      KiB/s     %   MIPS   MIPS

22:       1735   316    535   1689  |      41840   389    919   3570
23:       1691   324    532   1723  |      41174   390    914   3563
24:       1681   336    537   1808  |      40407   390    909   3547
25:       1331   307    496   1521  |      39068   388    897   3477
----------------------------------  | ------------------------------
Avr:             321    525   1685  |              389    910   3539
Tot:             355    717   2612

Compression: 1662,1685,1685
Decompression: 3537,3529,3539
Total: 2599,2607,2612

##########################################################################

** cpuminer-multi 1.3.7 by tpruvot@github **
BTC donation address: 1FhDPLPpw18X4srecguG3MxJYe4a1JsZnd (tpruvot)

[2023-04-12 15:14:01] 4 miner threads started, using 'scrypt' algorithm.
[2023-04-12 15:14:02] CPU #0: 0.83 kH/s
[2023-04-12 15:14:02] CPU #1: 0.78 kH/s
[2023-04-12 15:14:02] CPU #2: 0.77 kH/s
[2023-04-12 15:14:02] CPU #3: 0.72 kH/s
[2023-04-12 15:14:02] Total: 3.11 kH/s
[2023-04-12 15:14:05] Total: 3.23 kH/s
[2023-04-12 15:14:06] Total: 3.47 kH/s
[2023-04-12 15:14:10] CPU #2: 0.90 kH/s
[2023-04-12 15:14:10] CPU #1: 0.91 kH/s
[2023-04-12 15:14:11] CPU #0: 0.90 kH/s
[2023-04-12 15:14:11] CPU #3: 0.89 kH/s
[2023-04-12 15:14:11] Total: 3.63 kH/s
[2023-04-12 15:14:16] CPU #1: 0.92 kH/s
[2023-04-12 15:14:16] CPU #2: 0.91 kH/s
[2023-04-12 15:14:16] Total: 3.62 kH/s
[2023-04-12 15:14:21] CPU #0: 0.90 kH/s
[2023-04-12 15:14:21] CPU #3: 0.90 kH/s
[2023-04-12 15:14:21] Total: 3.62 kH/s
[2023-04-12 15:14:26] CPU #2: 0.91 kH/s
[2023-04-12 15:14:26] CPU #1: 0.91 kH/s
[2023-04-12 15:14:26] Total: 3.62 kH/s
[2023-04-12 15:14:31] CPU #0: 0.90 kH/s
[2023-04-12 15:14:31] CPU #3: 0.90 kH/s
[2023-04-12 15:14:31] Total: 3.61 kH/s
[2023-04-12 15:14:36] CPU #1: 0.91 kH/s
[2023-04-12 15:14:36] Total: 3.62 kH/s
[2023-04-12 15:14:36] CPU #2: 0.90 kH/s
[2023-04-12 15:14:40] CPU #0: 0.91 kH/s
[2023-04-12 15:14:41] CPU #3: 0.90 kH/s
[2023-04-12 15:14:41] Total: 3.62 kH/s
[2023-04-12 15:14:46] Total: 3.62 kH/s
[2023-04-12 15:14:46] CPU #1: 0.92 kH/s
[2023-04-12 15:14:46] CPU #2: 0.90 kH/s
[2023-04-12 15:14:46] CPU #0: 0.90 kH/s
[2023-04-12 15:14:51] CPU #3: 0.91 kH/s
[2023-04-12 15:14:51] Total: 3.62 kH/s
[2023-04-12 15:14:56] Total: 3.59 kH/s
[2023-04-12 15:14:56] CPU #1: 0.92 kH/s
[2023-04-12 15:14:56] CPU #0: 0.90 kH/s
[2023-04-12 15:14:56] CPU #2: 0.88 kH/s
[2023-04-12 15:15:01] CPU #3: 0.90 kH/s
[2023-04-12 15:15:01] Total: 3.61 kH/s
[2023-04-12 15:15:02] CPU #2: 0.87 kH/s
[2023-04-12 15:15:06] CPU #1: 0.92 kH/s
[2023-04-12 15:15:06] Total: 3.62 kH/s
[2023-04-12 15:15:06] CPU #0: 0.90 kH/s
[2023-04-12 15:15:11] CPU #3: 0.91 kH/s
[2023-04-12 15:15:11] Total: 3.62 kH/s
[2023-04-12 15:15:11] CPU #2: 0.89 kH/s
[2023-04-12 15:15:16] Total: 3.62 kH/s
[2023-04-12 15:15:16] CPU #1: 0.91 kH/s
[2023-04-12 15:15:16] CPU #0: 0.89 kH/s
[2023-04-12 15:15:21] CPU #2: 0.91 kH/s
[2023-04-12 15:15:21] CPU #3: 0.91 kH/s
[2023-04-12 15:15:21] Total: 3.62 kH/s
[2023-04-12 15:15:26] Total: 3.62 kH/s
[2023-04-12 15:15:26] CPU #1: 0.90 kH/s
[2023-04-12 15:15:26] CPU #0: 0.89 kH/s
[2023-04-12 15:15:31] CPU #2: 0.90 kH/s
[2023-04-12 15:15:31] CPU #3: 0.90 kH/s
[2023-04-12 15:15:31] Total: 3.60 kH/s
[2023-04-12 15:15:36] CPU #1: 0.90 kH/s
[2023-04-12 15:15:36] Total: 3.59 kH/s
[2023-04-12 15:15:36] CPU #0: 0.90 kH/s
[2023-04-12 15:15:41] CPU #2: 0.91 kH/s
[2023-04-12 15:15:41] CPU #3: 0.90 kH/s
[2023-04-12 15:15:41] Total: 3.62 kH/s
[2023-04-12 15:15:46] Total: 3.62 kH/s
[2023-04-12 15:15:46] CPU #1: 0.91 kH/s
[2023-04-12 15:15:46] CPU #0: 0.91 kH/s
[2023-04-12 15:15:51] CPU #2: 0.91 kH/s
[2023-04-12 15:15:51] CPU #3: 0.89 kH/s
[2023-04-12 15:15:51] Total: 3.62 kH/s
[2023-04-12 15:15:56] Total: 3.61 kH/s
[2023-04-12 15:15:56] CPU #1: 0.91 kH/s
[2023-04-12 15:15:56] CPU #0: 0.91 kH/s
[2023-04-12 15:16:01] CPU #3: 0.90 kH/s
[2023-04-12 15:16:01] Total: 3.62 kH/s
[2023-04-12 15:16:01] CPU #2: 0.89 kH/s
[2023-04-12 15:16:06] CPU #1: 0.91 kH/s
[2023-04-12 15:16:06] Total: 3.62 kH/s
[2023-04-12 15:16:06] CPU #0: 0.91 kH/s
[2023-04-12 15:16:11] CPU #2: 0.90 kH/s
[2023-04-12 15:16:11] CPU #3: 0.89 kH/s
[2023-04-12 15:16:11] Total: 3.60 kH/s
[2023-04-12 15:16:16] CPU #1: 0.91 kH/s
[2023-04-12 15:16:16] Total: 3.62 kH/s
[2023-04-12 15:16:16] CPU #0: 0.91 kH/s
[2023-04-12 15:16:21] CPU #2: 0.90 kH/s
[2023-04-12 15:16:21] CPU #3: 0.89 kH/s
[2023-04-12 15:16:21] Total: 3.60 kH/s
[2023-04-12 15:16:26] CPU #1: 0.91 kH/s
[2023-04-12 15:16:26] Total: 3.61 kH/s
[2023-04-12 15:16:26] CPU #0: 0.91 kH/s
[2023-04-12 15:16:31] CPU #2: 0.91 kH/s
[2023-04-12 15:16:31] CPU #3: 0.90 kH/s
[2023-04-12 15:16:31] Total: 3.63 kH/s
[2023-04-12 15:16:36] Total: 3.61 kH/s
[2023-04-12 15:16:36] CPU #1: 0.90 kH/s
[2023-04-12 15:16:36] CPU #0: 0.91 kH/s
[2023-04-12 15:16:41] CPU #3: 0.90 kH/s
[2023-04-12 15:16:41] Total: 3.61 kH/s
[2023-04-12 15:16:41] CPU #2: 0.89 kH/s
[2023-04-12 15:16:46] Total: 3.62 kH/s
[2023-04-12 15:16:46] CPU #1: 0.90 kH/s
[2023-04-12 15:16:46] CPU #0: 0.91 kH/s
[2023-04-12 15:16:51] CPU #3: 0.90 kH/s
[2023-04-12 15:16:51] Total: 3.62 kH/s
[2023-04-12 15:16:51] CPU #2: 0.90 kH/s
[2023-04-12 15:16:56] CPU #1: 0.90 kH/s
[2023-04-12 15:16:56] Total: 3.60 kH/s
[2023-04-12 15:16:56] CPU #0: 0.91 kH/s
[2023-04-12 15:17:01] CPU #2: 0.90 kH/s
[2023-04-12 15:17:01] CPU #3: 0.90 kH/s
[2023-04-12 15:17:01] Total: 3.62 kH/s
[2023-04-12 15:17:06] CPU #1: 0.91 kH/s
[2023-04-12 15:17:06] Total: 3.62 kH/s
[2023-04-12 15:17:06] CPU #0: 0.91 kH/s
[2023-04-12 15:17:11] CPU #3: 0.91 kH/s
[2023-04-12 15:17:11] Total: 3.61 kH/s
[2023-04-12 15:17:11] CPU #2: 0.90 kH/s
[2023-04-12 15:17:16] Total: 3.64 kH/s
[2023-04-12 15:17:16] CPU #1: 0.91 kH/s
[2023-04-12 15:17:16] CPU #0: 0.90 kH/s
[2023-04-12 15:17:21] CPU #3: 0.91 kH/s
[2023-04-12 15:17:21] Total: 3.62 kH/s
[2023-04-12 15:17:21] CPU #2: 0.90 kH/s
[2023-04-12 15:17:26] Total: 3.61 kH/s
[2023-04-12 15:17:26] CPU #1: 0.90 kH/s
[2023-04-12 15:17:26] CPU #0: 0.90 kH/s
[2023-04-12 15:17:31] CPU #3: 0.91 kH/s
[2023-04-12 15:17:31] Total: 3.62 kH/s
[2023-04-12 15:17:31] CPU #2: 0.90 kH/s
[2023-04-12 15:17:36] Total: 3.63 kH/s
[2023-04-12 15:17:36] CPU #1: 0.91 kH/s
[2023-04-12 15:17:36] CPU #0: 0.91 kH/s
[2023-04-12 15:17:41] CPU #3: 0.91 kH/s
[2023-04-12 15:17:41] Total: 3.62 kH/s
[2023-04-12 15:17:41] CPU #2: 0.90 kH/s
[2023-04-12 15:17:46] Total: 3.61 kH/s
[2023-04-12 15:17:46] CPU #1: 0.91 kH/s
[2023-04-12 15:17:46] CPU #0: 0.90 kH/s
[2023-04-12 15:17:51] CPU #3: 0.90 kH/s
[2023-04-12 15:17:51] Total: 3.60 kH/s
[2023-04-12 15:17:51] CPU #2: 0.89 kH/s
[2023-04-12 15:17:56] Total: 3.60 kH/s
[2023-04-12 15:17:56] CPU #1: 0.92 kH/s
[2023-04-12 15:17:56] CPU #0: 0.89 kH/s
[2023-04-12 15:18:01] CPU #3: 0.91 kH/s
[2023-04-12 15:18:01] Total: 3.62 kH/s
[2023-04-12 15:18:01] CPU #2: 0.90 kH/s
[2023-04-12 15:18:06] Total: 3.62 kH/s
[2023-04-12 15:18:06] CPU #1: 0.91 kH/s
[2023-04-12 15:18:06] CPU #0: 0.90 kH/s
[2023-04-12 15:18:11] CPU #3: 0.91 kH/s
[2023-04-12 15:18:11] Total: 3.61 kH/s
[2023-04-12 15:18:11] CPU #2: 0.90 kH/s
[2023-04-12 15:18:16] Total: 3.62 kH/s
[2023-04-12 15:18:16] CPU #1: 0.91 kH/s
[2023-04-12 15:18:16] CPU #0: 0.90 kH/s
[2023-04-12 15:18:21] CPU #3: 0.91 kH/s
[2023-04-12 15:18:21] Total: 3.62 kH/s
[2023-04-12 15:18:21] CPU #2: 0.90 kH/s
[2023-04-12 15:18:26] Total: 3.63 kH/s
[2023-04-12 15:18:26] CPU #1: 0.91 kH/s
[2023-04-12 15:18:26] CPU #0: 0.90 kH/s
[2023-04-12 15:18:31] CPU #3: 0.91 kH/s
[2023-04-12 15:18:31] Total: 3.60 kH/s
[2023-04-12 15:18:31] CPU #2: 0.90 kH/s
[2023-04-12 15:18:36] Total: 3.62 kH/s
[2023-04-12 15:18:36] CPU #1: 0.90 kH/s
[2023-04-12 15:18:36] CPU #0: 0.90 kH/s
[2023-04-12 15:18:41] CPU #3: 0.91 kH/s
[2023-04-12 15:18:41] Total: 3.60 kH/s
[2023-04-12 15:18:41] CPU #2: 0.90 kH/s
[2023-04-12 15:18:46] CPU #1: 0.91 kH/s
[2023-04-12 15:18:46] Total: 3.62 kH/s
[2023-04-12 15:18:46] CPU #0: 0.90 kH/s
[2023-04-12 15:18:51] CPU #2: 0.91 kH/s
[2023-04-12 15:18:51] CPU #3: 0.90 kH/s
[2023-04-12 15:18:51] Total: 3.62 kH/s
[2023-04-12 15:18:56] Total: 3.62 kH/s
[2023-04-12 15:18:56] CPU #1: 0.91 kH/s
[2023-04-12 15:18:56] CPU #0: 0.90 kH/s

Total Scores: 3.64,3.63,3.62,3.61,3.60,3.59,3.47

##########################################################################

Testing maximum cpufreq again, still under full load. System health now:

Time      CPU n/a    load %cpu %sys %usr %nice %io %irq   Temp
15:18:34: n/a MHz    4.21 100%   0%  98%   0%   0%   0%  72.4°C

Checking cpufreq OPP (Cortex-A53):

No cpufreq support available. Measured on cpu1: 1006 MHz (1006.997/1006.709/1006.614)

##########################################################################

Hardware sensors:

cpu_thermal-virtual-0
temp1:        +64.1 C  (crit = +105.0 C)

gpu_thermal-virtual-0
temp1:        +64.1 C  

ddr_thermal-virtual-0
temp1:        +63.4 C  

ve_thermal-virtual-0
temp1:        +64.1 C  

##########################################################################

Thermal source: /sys/devices/virtual/thermal/thermal_zone0/ (cpu-thermal)

System health while running tinymembench:

Time      CPU n/a    load %cpu %sys %usr %nice %io %irq   Temp
14:58:03: n/a MHz    1.04   3%   1%   2%   0%   0%   0%  56.8°C
14:58:13: n/a MHz    1.03  27%   1%  25%   0%   0%   0%  61.3°C
14:58:23: n/a MHz    1.03  27%   1%  26%   0%   0%   0%  61.6°C
14:58:34: n/a MHz    1.02  27%   1%  26%   0%   0%   0%  61.4°C
14:58:44: n/a MHz    1.02  29%   2%  26%   0%   0%   0%  62.4°C
14:58:54: n/a MHz    1.02  28%   1%  25%   0%   0%   0%  64.0°C
14:59:04: n/a MHz    1.01  28%   1%  26%   0%   0%   0%  63.2°C
14:59:14: n/a MHz    1.01  28%   2%  26%   0%   0%   0%  64.5°C
14:59:24: n/a MHz    1.01  29%   2%  26%   0%   0%   0%  54.6°C
14:59:34: n/a MHz    1.09  26%   1%  25%   0%   0%   0%  57.2°C

System health while running ramlat:

Time      CPU n/a    load %cpu %sys %usr %nice %io %irq   Temp
14:59:40: n/a MHz    1.24   3%   1%   2%   0%   0%   0%  57.3°C
14:59:44: n/a MHz    1.22  27%   1%  25%   0%   0%   0%  57.0°C
14:59:47: n/a MHz    1.22  27%   1%  25%   0%   0%   0%  57.3°C
14:59:50: n/a MHz    1.20  27%   1%  25%   0%   0%   0%  58.2°C
14:59:53: n/a MHz    1.20  27%   1%  25%   0%   0%   0%  56.8°C
14:59:56: n/a MHz    1.19  28%   2%  25%   0%   0%   0%  57.9°C
14:59:59: n/a MHz    1.17  27%   1%  25%   0%   0%   0%  58.1°C
15:00:02: n/a MHz    1.17  28%   1%  26%   0%   0%   0%  57.9°C
15:00:05: n/a MHz    1.16  27%   1%  25%   0%   0%   0%  58.2°C
15:00:08: n/a MHz    1.14  27%   1%  25%   0%   0%   0%  57.7°C
15:00:11: n/a MHz    1.14  27%   2%  25%   0%   0%   0%  58.7°C
15:00:14: n/a MHz    1.13  27%   1%  25%   0%   0%   0%  58.9°C

System health while running OpenSSL benchmark:

Time      CPU n/a    load %cpu %sys %usr %nice %io %irq   Temp
15:00:18: n/a MHz    1.20   4%   1%   2%   0%   0%   0%  59.0°C
15:00:34: n/a MHz    1.16  26%   1%  25%   0%   0%   0%  57.7°C
15:00:50: n/a MHz    1.12  26%   0%  25%   0%   0%   0%  57.1°C
15:01:06: n/a MHz    1.17  26%   0%  25%   0%   0%   0%  57.0°C
15:01:22: n/a MHz    1.14  26%   0%  25%   0%   0%   0%  57.4°C
15:01:38: n/a MHz    1.10  26%   1%  25%   0%   0%   0%  57.2°C
15:01:54: n/a MHz    1.07  26%   1%  25%   0%   0%   0%  56.1°C

System health while running 7-zip single core benchmark:

Time      CPU n/a    load %cpu %sys %usr %nice %io %irq   Temp
15:02:06: n/a MHz    1.06   4%   1%   3%   0%   0%   0%  56.8°C
15:02:20: n/a MHz    1.05  27%   1%  25%   0%   0%   0%  56.8°C
15:02:34: n/a MHz    1.04  26%   1%  25%   0%   0%   0%  55.7°C
15:02:48: n/a MHz    1.03  26%   1%  25%   0%   0%   0%  56.0°C
15:03:02: n/a MHz    1.02  27%   1%  25%   0%   0%   0%  55.3°C
15:03:17: n/a MHz    1.02  26%   1%  25%   0%   0%   0%  55.6°C
15:03:31: n/a MHz    1.01  27%   1%  25%   0%   0%   0%  55.6°C
15:03:45: n/a MHz    1.01  26%   1%  25%   0%   0%   0%  55.7°C
15:03:59: n/a MHz    1.01  27%   1%  25%   0%   0%   0%  56.0°C
15:04:13: n/a MHz    1.00  26%   1%  25%   0%   0%   0%  55.9°C
15:04:27: n/a MHz    1.08  26%   1%  25%   0%   0%   0%  56.2°C
15:04:41: n/a MHz    1.06  26%   1%  25%   0%   0%   0%  55.8°C
15:04:55: n/a MHz    1.05  26%   1%  25%   0%   0%   0%  56.4°C
15:05:09: n/a MHz    1.04  27%   1%  25%   0%   0%   0%  56.0°C

System health while running 7-zip multi core benchmark:

Time      CPU n/a    load %cpu %sys %usr %nice %io %irq   Temp
15:05:23: n/a MHz    1.03   5%   1%   3%   0%   0%   0%  56.0°C
15:05:56: n/a MHz    2.03  83%   1%  82%   0%   0%   0%  64.2°C
15:06:29: n/a MHz    3.07  93%   1%  91%   0%   0%   0%  65.5°C
15:07:02: n/a MHz    3.71  89%   2%  86%   0%   0%   0%  66.9°C
15:07:31: n/a MHz    3.80  85%   2%  82%   0%   0%   0%  66.2°C
15:08:00: n/a MHz    4.91  96%  39%  56%   0%   0%   0%  66.0°C
15:08:30: n/a MHz    4.28  90%   2%  87%   0%   0%   0%  66.5°C
15:08:59: n/a MHz    3.94  92%   1%  90%   0%   0%   0%  67.5°C
15:09:28: n/a MHz    4.04  91%   1%  89%   0%   0%   0%  66.4°C
15:10:00: n/a MHz    4.22  94%   2%  92%   0%   0%   0%  68.3°C
15:10:29: n/a MHz    4.27  83%   2%  80%   0%   0%   0%  67.7°C
15:11:03: n/a MHz    4.87  95%  29%  66%   0%   0%   0%  68.8°C
15:11:36: n/a MHz    4.21  83%   1%  81%   0%   0%   0%  68.3°C
15:12:08: n/a MHz    4.16  93%   1%  91%   0%   0%   0%  66.5°C
15:12:39: n/a MHz    4.16  89%   2%  86%   0%   0%   0%  67.9°C
15:13:08: n/a MHz    3.79  87%   2%  85%   0%   0%   0%  67.6°C
15:13:42: n/a MHz    4.89  95%  27%  68%   0%   0%   0%  69.8°C

System health while running cpuminer:

Time      CPU n/a    load %cpu %sys %usr %nice %io %irq   Temp
15:14:07: n/a MHz    4.55  11%   1%   9%   0%   0%   0%  70.3°C
15:14:52: n/a MHz    4.69 100%   1%  98%   0%   0%   0%  71.3°C
15:15:36: n/a MHz    4.45 100%   1%  98%   0%   0%   0%  71.8°C
15:16:20: n/a MHz    4.25 100%   1%  98%   0%   0%   0%  72.1°C
15:17:05: n/a MHz    4.16 100%   1%  98%   0%   0%   0%  71.6°C
15:17:50: n/a MHz    4.36 100%   1%  98%   0%   0%   0%  72.7°C
15:18:34: n/a MHz    4.21 100%   0%  98%   0%   0%   0%  72.4°C

##########################################################################

Linux 5.16.17-sun50iw9 (BTT-CB1) 	04/12/23 	_aarch64_	(4 CPU)

avg-cpu:  %user   %nice %system %iowait  %steal   %idle
          13.36    0.00    1.57    0.07    0.00   84.99

Device             tps    kB_read/s    kB_wrtn/s    kB_dscd/s    kB_read    kB_wrtn    kB_dscd
mmcblk2          10.59       104.62       130.93         0.00     774954     969860          0
zram0           132.84       230.55       300.80         0.00    1707708    2228104          0
zram1             0.00         0.01         0.01         0.00         68         72          0

               total        used        free      shared  buff/cache   available
Mem:           986Mi       112Mi       815Mi       0.0Ki        59Mi       811Mi
Swap:          493Mi        67Mi       425Mi

Filename				Type		Size	Used	Priority
/dev/zram0                             	partition	505316	69096	5

CPU sysfs topology (clusters, cpufreq members, clockspeeds)
                 cpufreq   min    max
 CPU    cluster  policy   speed  speed   core type
  0        0        0       -      -     Cortex-A53 / r0p4
  1        0        0       -      -     Cortex-A53 / r0p4
  2        0        0       -      -     Cortex-A53 / r0p4
  3        0        0       -      -     Cortex-A53 / r0p4

Architecture:                    aarch64
CPU op-mode(s):                  32-bit, 64-bit
Byte Order:                      Little Endian
CPU(s):                          4
On-line CPU(s) list:             0-3
Thread(s) per core:              1
Core(s) per socket:              4
Socket(s):                       1
NUMA node(s):                    1
Vendor ID:                       ARM
Model:                           4
Model name:                      Cortex-A53
Stepping:                        r0p4
BogoMIPS:                        48.00
NUMA node0 CPU(s):               0-3
Vulnerability Itlb multihit:     Not affected
Vulnerability L1tf:              Not affected
Vulnerability Mds:               Not affected
Vulnerability Meltdown:          Not affected
Vulnerability Spec store bypass: Not affected
Vulnerability Spectre v1:        Mitigation; __user pointer sanitization
Vulnerability Spectre v2:        Not affected
Vulnerability Srbds:             Not affected
Vulnerability Tsx async abort:   Not affected
Flags:                           fp asimd evtstrm aes pmull sha1 sha2 crc32 cpuid

SoC guess: Allwinner H616/H313
DT compat: allwinner,sun50i-h616
 Compiler: /usr/bin/gcc (Debian 10.2.1-6) 10.2.1 20210110 / aarch64-linux-gnu
 Userland: arm64
   Kernel: 5.16.17-sun50iw9/aarch64
           CONFIG_HZ=250
           CONFIG_HZ_250=y
           CONFIG_PREEMPT_NONE=y
           CONFIG_PREEMPT_NONE_BUILD=y

##########################################################################

5.16 has reached end-of-life on 2022-04-13 with version 5.16.20.
This 5.16.17 and all other 5.16 revisions are unsupported since then.

##########################################################################

   opp-table-cpu:
       480 MHz    820.0 mV
       600 MHz    820.0 mV
       792 MHz    860.0 mV
      1008 MHz    900.0 mV
      1200 MHz    960.0 mV
      1512 MHz   1100.0 mV

##########################################################################

Results validation:

  * Swapping (ZRAM) occured
  * Too much background activity (%system): 2% avg, 39% max
  * No throttling

| BQ-H616 | ~1010 MHz | 5.16 | BTT-CB1 2.3.2 Bullseye arm64 | 2610 | 767 | 465190 | 1560 | 5130 | 3.63 |
