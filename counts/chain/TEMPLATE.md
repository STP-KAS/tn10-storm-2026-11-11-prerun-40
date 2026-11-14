> **Experimental. We are just trying this.** [Disclaimer](../../DISCLAIMER.md) · Kaspa Testnet-10 only. tKAS has no value. Counts only.

# Template, pre-run 40

The desk probe, every 20 s, on our own desk node. A cell is the median of that minute's samples. An odd count takes the middle sample. An even count takes the average of the two middle samples. Template storage mass is the mass the template's transactions carry. "Under 400k" is how many of those samples had template storage mass under 400,000. The lane log is a different clock: its pending count is the lane's own in-flight count at the minute line. "Our heavy" is the probe's class for ids this lane had already written, at fee rate 460.

The lane was off in BASE (17:24–17:26Z) and RETURN (17:33–17:35Z). HOLD on the clock was 17:27–17:32Z, sixty chains, no ready cap, rate 460. The fee cap stopped new submits at 17:31:15Z. The 17:32 minute is still inside that clock, and the lane submitted 0 in it.

| Minute (UTC) | Step | Samples | Mempool | Ready count | Ready mass, blocks of 500k | Template txs | Template storage mass | Samples under 400k | Fee estimate priority / normal / low | Our heavy in mempool | Lane pending | Lane submit-OK |
|---|---|---:|---:|---:|---:|---:|---:|---:|---|---:|---:|---:|
| 2026-11-14T17:24 | BASE | 3 | 0 | 0 | 0 | 0 | 0 | 3 of 3 | 100 / 100 / 100 | 0 | 0 | 0 |
| 2026-11-14T17:25 | BASE | 3 | 0 | 0 | 0 | 0 | 0 | 3 of 3 | 100 / 100 / 100 | 0 | 0 | 0 |
| 2026-11-14T17:26 | BASE | 3 | 0 | 0 | 0 | 0 | 0 | 3 of 3 | 100 / 100 / 100 | 0 | 0 | 0 |
| 2026-11-14T17:27 | HOLD | 3 | 1,109 | 1,108 | 36.94 | 4 | 266,714 | 3 of 3 | 635.02 / 191.22 / 115 | 56 | 60 | 631 |
| 2026-11-14T17:28 | HOLD | 3 | 1,739 | 1,764 | 40.05 | 4 | 266,838 | 3 of 3 | 662.27 / 191.75 / 115.03 | 53 | 60 | 595 |
| 2026-11-14T17:29 | HOLD | 3 | 1,953 | 1,952 | 46.60 | 9 | 266,821 | 3 of 3 | 694.39 / 192.29 / 115.07 | 60 | 60 | 519 |
| 2026-11-14T17:30 | HOLD | 3 | 1,821 | 1,835 | 48.67 | 5 | 266,941 | 3 of 3 | 706.02 / 192.47 / 115.09 | 55 | 60 | 566 |
| 2026-11-14T17:31 | HOLD | 3 | 1 | 1 | 0.04 | 1 | 0 | 3 of 3 | 100 / 100 / 100 | 0 | 0 | 134 |
| 2026-11-14T17:32 | HOLD | 3 | 0 | 0 | 0 | 0 | 0 | 3 of 3 | 100 / 100 / 100 | 0 | 0 | 0 |
| 2026-11-14T17:33 | RETURN | 2 | 0 | 0 | 0 | 0 | 0 | 2 of 2 | 100 / 100 / 100 | 0 | 0 | 0 |
| 2026-11-14T17:34 | RETURN | 3 | 0 | 0 | 0 | 0 | 0 | 3 of 3 | 100 / 100 / 100 | 0 | 0 | 0 |
| 2026-11-14T17:35 | RETURN | 3 | 0 | 0 | 0 | 0 | 0 | 3 of 3 | 100 / 100 / 100 | 0 | — | — |

The 17:31 median is pulled by the two samples after our class had left. The sample at 17:31:16Z, one second after the fee cap, has mempool size 1,694, our heavy class 30, template storage mass 267,556, template heavy count 1, 1,624 other transactions in the 101–149 fee band, and a priority fee estimate of 615.32. The samples at 17:31:36Z and 17:31:57Z have our heavy class 0 and a fee estimate of 100. The 134 submits belong to the minute.

Across the thirteen samples from 17:27:12Z through 17:31:16Z, while our heavy class was present, template storage mass runs from 266,707 to 267,556. All thirteen are under 400,000. The template's heavy count is 1 in each of those thirteen, and that one template transaction is classed as ours. Our heavy class in those samples is 30 to 60 transactions, all ready, fee rate 460 on the class. In the twelve samples through 17:30:56Z the class is 50 to 60, and two of them, at 17:29:14Z and 17:29:55Z, are 60. The same thirteen samples also hold other transactions: 532 to 1,941 of them sit in the 101–149 fee band, and in these samples that band's ready count equals its count. Mempool size in those samples is 593 to 2,027. Ready mass in those samples runs from 30.66 to 49.71 blocks. In some of those samples the ready count is above the mempool size field. We report both as the probe wrote them.

No sample in this run has a template heavy count above 1. No sample has template storage mass at or above 400,000.

The sample at 17:32:58Z, after our class had left, has mempool size 50, template storage mass 1,596, template heavy count 0, 50 other transactions in the 101–149 band, and a fee estimate of 100. The minute's median is still an empty read. The sample at 17:31:57Z is mempool size 1, template storage mass 0, one other transaction, fee estimate 100.

The lane's own minute lines say pending 60 and submit-OK 631, 595, 519 and 566. Sixty chains were available, the ready cap was off, and pending on those four lines is 60. The 17:31 row stamps pending 0 on the first tick of 17:32, after the cap at 17:31:15Z, and that minute has 134 submits. The submit count is the minute. The 17:35 lane minute was not flushed. The probe covers it, and the end line says pending 0.

The lane's end line at 17:36:00Z: 2,445 submit-OK, 0 rejects, 0 lost, fees 3,002.11 tKAS, parked 91.69 tKAS, 139 coins taken, pending 0. Node rate on the lane's own entries was 459.99–460. Storage mass did not drift. The second lane submitted 0. The lane's pause lines stay 0. The highest ready mass in the samples above is 49.71 blocks.

One BASE sample, at 17:24:28Z, read mempool size 8, template storage mass 127,924, template heavy count 1, classed other, not our heavy. Seven of those eight sit in the 101–149 band. The lane submitted 0, and the fee estimate is 100 / 100 / 100. One BASE sample, at 17:26:11Z, read mempool size 7, template storage mass 0, template heavy count 0, seven other transactions in the 101–149 band, fee estimate 100. The other BASE samples are empty.
