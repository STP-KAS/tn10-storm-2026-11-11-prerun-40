> **Experimental. We are just trying this.** [Disclaimer](../DISCLAIMER.md) · This page does not start a machine. Pre-run 40. Not Wednesday. Not Tuesday. Not pre-run 1 to 39.

# Targets

Pre-run 39 held sixty chains at a ready cap of 32. Pending sat at 32. Submit-OK was 523–576 a minute. In the thirteen samples while our heavy class was present, the template's heavy count stayed 1, and 133–661 other transactions sat in the 101–149 fee band. The next single knob is the ready cap, turned off.

**Question.** On our desk node, with sixty chains and the rate held, and with no ready cap, what happens to the lane's pending count, the template, and the fee estimate, against a no-lane baseline in the same run?

**Target.** The lane runs only in the middle step and is at zero at the end. A table, written after the tail from this run's own files, shows template storage mass, template transaction count, ready mass, and the fee estimate, for the baseline minutes, the no-cap minutes, and the return minutes. **Met means the table exists and the lane is at zero, not that a particular theory won.** If the fee cap stops new submits before the six minutes are up, the table still counts.

## Why the twelve families are not in this run

At 2026-11-14T15:49:57Z the funding key's usable balance (coins over 3 tKAS, above that line) was 17,905 tKAS. Pre-runs 36 through 39 did not spend that key. A family window aborts under 18,000 tKAS. This run does not start the families, the mint line, or the guest. The two keys this series leaves unused stay unused.

## The pile, read before the arm

The lane takes a coin only when that coin is at or above 10 tKAS. At 2026-11-14T17:18:41Z the payment pile had 220 such coins, together 4,480 tKAS. Pre-run 39 moved 3,094.72 tKAS before its fee cap. This pile covers that same cap. This run does not join coins. Value stays where it is. Nothing moves onto the funding key.

## The one change, written before the arm

**Ready cap off. Sixty chains stay.** Our heavy lane (the same shape as pre-run 39: one input, two outputs, storage mass about 266,666, submitted only to the desk's private node). A ready cap of 0 means the lane does not hold a chain back for the cap. The rate is 460 sompi per gram, held. No second lane. No climb toward 1,405 or 2,000. The fee cap stays 3,000 tKAS. The moved cap stays 4,000 tKAS. The pile floor stays 200 tKAS. The lane's existing pause, at mempool size 90,000 or ready mass over 80 blocks, stays in the code. Those guards are not the knob.

**While it runs it slows other users' low-fee transactions on our node. We say so here, in public.**

| Order | Step | Lane | Length |
|---:|---|---|---:|
| 1 | BASE | off (N=0, ready cap 0) | 3 whole minutes |
| 2 | HOLD | N=60, ready cap off, rate 460 | 6 whole minutes |
| 3 | RETURN | off | 3 whole minutes |

The desk node is not restarted. One counter: the desk. The Mini is not reachable. No payment flood. No heavy submit to a public node.

Disk line: abort if the desk is under 150 GB free.
