# DVB-T configuration files for Newcastle and the Lower Hunter regions (Archived)

## This repo is no longer updated.

This repository contains configuration files allowing anyone who lives in the Newcastle and Lower Hunter regions to watch free-to-air television via a DVB-T compatible tv tuner card on GNU/Linux without needing to use the various scanning utilities.

I've taken the liberty of generating a playlist file for VLC with all of the channels in it which can be found at [`channels.xspf`](channels.xspf). If you use mpv/mplayer you can use the [`channels.conf`](channels.conf) file instead.

### Note about Network 10

  On Sept 1st 2017, Network Ten began broadcasting their channels on the Win Network (presumably because they pissed away a lot of their money and went into receivership) and as a result Newcastle and the Lower Hunter (among a lot of other places) now receive the Win Network. The frequency is the same however the program ids and channel numbers are different. Notably the Aspire channel is either gone or been renamed to GOLD. Either way you'll still receive the same garbage you get from Network 10, just that it'll be on another network.

### Important Notes

  * These files were generated from the Mt Sugarloaf omnidirectional transmitter site and as a result may have different frequencies or program ids if you receive your signals from one of the many directional transmitters in the Hunter area (such as Munibung Hill and Charlestown).

      * Mt Sugarloaf transmitter info can be found [here](https://ozdigitaltv.com/transmitters/NSW/12-Mt-Sugarloaf).
      * The ABC website has a coverage map [here](http://www2b.abc.net.au/reception/frequencyfinder/asp/details.asp?transmissionid=18809&presdir=).
      * As does the SBS [website](http://www20.sbs.com.au/transmissions/download.php?file=9345newcastle_sbs38_dtv_pubmap.pdf).
      
### Tuning Info

The tuning info can found be in the [`au-Newcastle`](au-Newcastle) file. This file is also a usable initial scanning file that you can use with `w_scan` or another scanning utility. Using this with `w_scan` may be desirable as it would be much faster than doing a full spectrum scan. 

The following table contains the same information for your convenience.

| Network        | freq      | bw   | fec_hi | fec_lo | mod   | tm | guard | hi  |
|----------------|-----------|------|--------|--------|-------|----|-------|-----|
| Seven          | 578.5 MHz | 7MHz | 3/4    | N/A    | QAM64 | 8k | 1/16  | N/A |
| NBN Newcastle  | 585.5 MHz | 7MHz | 3/4    | N/A    | QAM64 | 8k | 1/16  | N/A |
| ABC Digital TV | 592.5 MHz | 7MHz | 3/4    | N/A    | QAM64 | 8k | 1/16  | N/A |
| SBS NSW        | 599.5 MHz | 7MHz | 3/4    | N/A    | QAM64 | 8k | 1/16  | N/A |
| Win Network    | 606.5 MHz | 7MHz | 3/4    | N/A    | QAM64 | 8k | 1/16  | N/A |

### Channel Info

The following tables shows info for each network's "program" (multiple channels are multiplexed into a single stream with each channel referred to as a program). Channels for TV radio are in a seperate table.

*Please note there are duplicate channels (possibly from other transmitters). Just watch the ones that work and delete the others.*

#### Television

| Network (see tuning table) | Channel                | PID  | TSID  | VID  | AID  |
|----------------------------|------------------------|------|-------|------|------|
| Seven                      | PRIME7 Newcastle       | 2366 | 2480  | 2660 | 2661 |
| Seven                      | PRIME7 Newcastle       | 2410 | 2480  | 2660 | 2661 |
| Seven                      | PRIME7 Newcastle       | 2411 | 2480  | 2660 | 2661 |
| Seven                      | 7TWO                   | 2412 | 2480  | 4620 | 4621 |
| Seven                      | 7mate                  | 2413 | 2480  | 4630 | 4623 |
| Seven                      | ishoptv                | 2415 | 2480  | 4650 | 4651 |
| Seven                      | 7flix                  | 2416 | 2480  | 4660 | 4661 |
| Seven                      | RACING.COM             | 2418 | 2480  | 4680 | 4681 |
| NBN Newcastle              | Nine Newcastle         | 101  | 1792  | 1000 | 1010 |
| NBN Newcastle              | 9HD Newcastle          | 111  | 1792  | 1200 | 1220 |
| NBN Newcastle              | Nine Newcastle         | 191  | 1792  | 1000 | 1010 |
| NBN Newcastle              | 9GEM Newcastle         | 121  | 1792  | 1100 | 1110 |
| NBN Newcastle              | 9GO! Newcastle         | 131  | 1792  | 1881 | 1882 |
| NBN Newcastle              | 9Life Newcastle        | 151  | 1792  | 1400 | 1410 |
| NBN Newcastle              | eXtra                  | 141  | 1792  | 1841 | 1842 |
| NBN Newcastle              | 9GO! Newcastle         | 181  | 1792  | 1881 | 1882 |
| ABC Digital TV             | ABC News 24            | 672  | 547   | 516  | 654  |
| ABC Digital TV             | ABC                    | 673  | 547   | 512  | 650  |
| ABC Digital TV             | ABC2/KIDS              | 674  | 547   | 513  | 651  |
| ABC Digital TV             | ABC                    | 675  | 547   | 512  | 650  |
| ABC Digital TV             | ABC ME (formerly ABC3) | 676  | 547   | 514  | 652  |
| SBS NSW                    | SBS ONE                | 849  | 848   | 161  | 81   |
| SBS NSW                    | SBS TWO                | 850  | 848   | 162  | 83   |
| SBS NSW                    | NITV                   | 852  | 848   | 164  | 87   |
| SBS NSW                    | SBS HD                 | 853  | 848   | 102  | 103  |
| SBS NSW                    | Food Network           | 851  | 848   | 163  | 85   |
| Win Network                | GOLD                   | 1927 | 12956 | 115  | 515  |
| Win Network                | TVSN                   | 1928 | 12956 | 116  | 516  |
| Win Network                | WIN Newcastle          | 2080 | 12956 | 1110 | 1510 |
| Win Network                | ONE Newcastle          | 2082 | 12956 | 1111 | 1511 |
| Win Network                | ELEVEN Newcastle       | 2084 | 12956 | 1112 | 1512 |
| Win Network                | WIN HD Newcastle       | 2085 | 12956 | 1113 | 1513 |
| Win Network                | WIN NETWORK            | 2086 | 12956 | 1114 | 1514 |

#### Radio

As you could probably tell, the VID for radio channels is 0 since there's no video.

| Network (see tuning table) | Channel     | PID | TSID | VID | AID |
|----------------------------|-------------|-----|------|-----|-----|
| ABC Digital TV             | Double J    | 678 | 547  | 0   | 690 |
| ABC Digital TV             | ABC Jazz    | 679 | 547  | 0   | 700 |
| SBS NSW                    | SBS Radio 1 | 862 | 848  | 0   | 201 |
| SBS NSW                    | SBS Radio 2 | 863 | 848  | 0   | 202 |
| SBS NSW                    | SBS Radio 3 | 864 | 848  | 0   | 203 |
