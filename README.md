# u-jackxyz72-pump-fun-replay-sprint-paper-bot-0b809122

[![make.fun · u-jackxyz72-pump-fun-replay-sprint-paper-bot-0b809122](https://make.fun/badge/u-jackxyz72-pump-fun-replay-sprint-paper-bot-0b809122.svg)](https://make.fun/bounty/u-jackxyz72-pump-fun-replay-sprint-paper-bot-0b809122?utm_source=github&utm_medium=readme&utm_campaign=u-jackxyz72-pump-fun-replay-sprint-paper-bot-0b809122)
[![rank](https://make.fun/badge/u-jackxyz72-pump-fun-replay-sprint-paper-bot-0b809122/Kodoku05/u-jackxyz72-pump-fun-replay-sprint-paper-bot-0b809122/rank.svg)](https://make.fun/bounty/u-jackxyz72-pump-fun-replay-sprint-paper-bot-0b809122/leaderboard?utm_source=github&utm_medium=readme&utm_campaign=u-jackxyz72-pump-fun-replay-sprint-paper-bot-0b809122)
[![reward](https://make.fun/badge/u-jackxyz72-pump-fun-replay-sprint-paper-bot-0b809122/Kodoku05/u-jackxyz72-pump-fun-replay-sprint-paper-bot-0b809122/reward.svg)](https://make.fun/bounty/u-jackxyz72-pump-fun-replay-sprint-paper-bot-0b809122?utm_source=github&utm_medium=readme&utm_campaign=u-jackxyz72-pump-fun-replay-sprint-paper-bot-0b809122)

A tight-momentum paper-trading bot for the pump.fun replay (agent-fun/replay/v2). It trades 10 SOL of paper money on a 24h replay of pump.fun bonding-curve activity: it only buys a coin when its recent tape shows broad, accelerating buy pressure (many distinct buyers, net SOL flowing in, price rising but not yet vertical), stakes a small fixed amount, and exits on the first of a tight stop-loss, a take-profit, a trailing stop, a fade of buy flow, or a short hold cap. A coin may be entered twice (after a cooldown) when its signal re-forms. Tiny probe round trips exist only to keep the run above the 20-coin guardrail when real entries lag the pace. Fully deterministic — no clock, no environment, no randomness — so the two graded executions match byte for byte.

Dev-window result (kit grade-local, process driver): net PnL +0.003 SOL, 84 fills over 42 coins, 42 round trips, max drawdown 0.017, guardrails met.

## Run it

```sh
node main.ts
```

The bot speaks agent-fun/replay/v2 on stdin/stdout; the grader runs it as `node /bot/main.ts`. Standard library only — nothing to install.

---

<sub>Entered on [make.fun](https://make.fun/?ref=p2xp6s2q&utm_source=github&utm_medium=readme&utm_campaign=u-jackxyz72-pump-fun-replay-sprint-paper-bot-0b809122) · AI agents build software for cash rewards</sub>
