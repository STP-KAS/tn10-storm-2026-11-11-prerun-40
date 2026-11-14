> **Experimental. We are just trying this.** [Disclaimer](DISCLAIMER.md) · Kaspa Testnet-10 only; tKAS has no value.
>
> **This is a pre-run. Pre-run 40.** It is not the Wednesday run. It is not the Tuesday run. It is not pre-run 1 to 39, and it does not edit their repos. A read does not start a runner.

# tn10-storm-2026-11-11-prerun-40

**Pre-run 40: one heavy lane of ours, sixty chains, no ready cap, on the desk node, with the lane off at both ends.** The neuron stays [tn10-storm-2026-11-11](https://github.com/STP-KAS/tn10-storm-2026-11-11). This repo does not edit that repo.

> **Our own testing.** This is our own Kaspa Testnet-10 testing, run on our own machines and nodes. What these pages report is what we observed in this run; it is not a claim of how TN10 or Kaspa behave in general.

| Field | Value |
|---|---|
| Target | A table of the desk template and the desk fee estimate with our lane off, then at sixty chains with no ready cap, then off again. The lane returns to zero |
| The change | One knob: the ready cap, turned off. Sixty chains stay. The rate stays 460 sompi per gram. No payment ladder. No second lane. No fee climb |
| Met or not met | **met** on the table and on the lane returning to zero. BASE 17:24–17:26Z: fee estimate 100 / 100 / 100, lane submit 0. HOLD: the lane log shows pending 60 and submit-OK 631, 595, 519 and 566. In the thirteen samples from 17:27:12Z through 17:31:16Z the template's heavy count is 1, template storage mass 266,707–267,556, our heavy class 30–60 at fee rate 460, and 532–1,941 other transactions sit in the 101–149 fee band. Ready mass in those samples is 30.66–49.71 blocks. The fee cap stopped new submits at 17:31:15Z (134 submit-OK in that minute, fees 3,002.11 tKAS). No sample has a template heavy count above 1, and every sample is under 400,000. RETURN fee estimate 100 / 100 / 100, pending 0 from 17:33. 2,445 submit-OK, 0 rejects |
| Retry count | 0. The next attempt is a new repo. This one is not resumed |
| Core tags | — |
| Status | done. Closed from the lane log and the probe |

Plan, lock, and the prediction are in [plan/PLAN.md](plan/PLAN.md), [locks/LOCKED.md](locks/LOCKED.md), and [plan/PREDICTIONS.md](plan/PREDICTIONS.md). Written before any submit.

While the lane is on, it slows other users' low-fee transactions on our node. We say so here.
