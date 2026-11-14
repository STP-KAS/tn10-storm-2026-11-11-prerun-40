> **Experimental. We are just trying this.** [Disclaimer](../DISCLAIMER.md) · Kaspa Testnet-10 only. tKAS has no value.

# Lock (pre-run 40)

Locked before the first submit.

- Network: Testnet-10. The desk node is not restarted and it is not stopped.
- One knob: the ready cap, turned off. Sixty chains stay. The rate stays 460 sompi per gram. No second lane. No fee climb. No payment ladder. The chain count is not changed.
- The lane submits only to the desk node. While it is on, it slows other users' low-fee transactions on our node.
- No coin join in this run. At 2026-11-14T17:18:41Z the payment pile had 220 coins at or above 10 tKAS, together 4,480 tKAS. That covers the same fee cap pre-run 39 hit. Value is not moved onto the funding key.
- No covenant families, no mint line, no guest. The funding key was at 17,905 usable tKAS at 2026-11-14T15:49:57Z, under the 18,000 line. Pre-runs 36 through 39 did not spend it.
- The two keys this series leaves unused stay unused. The lane spends the payment pile.
- One counter: the desk node. The Mini is not reachable. No Mini-armed file.
- Fee cap 3,000 tKAS, moved cap 4,000 tKAS, pile floor 200 tKAS. The lane's existing pause, at mempool size 90,000 or ready mass over 80 blocks, stays. Same guards as pre-run 39.
- Disk line: abort if the desk is under 150 GB free. It was 328.09 GB at the end of pre-run 39.
- A miss is a retry with the fix written first. This page is not rewritten to match the result.
