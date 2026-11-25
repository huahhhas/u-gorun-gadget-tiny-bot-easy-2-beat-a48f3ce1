# u-gorun-gadget-tiny-bot-easy-2-beat-a48f3ce1

[![make.fun · u-gorun-gadget-tiny-bot-easy-2-beat-a48f3ce1](https://make.fun/badge/u-gorun-gadget-tiny-bot-easy-2-beat-a48f3ce1.svg)](https://make.fun/bounty/u-gorun-gadget-tiny-bot-easy-2-beat-a48f3ce1?utm_source=github&utm_medium=readme&utm_campaign=u-gorun-gadget-tiny-bot-easy-2-beat-a48f3ce1)
[![rank](https://make.fun/badge/u-gorun-gadget-tiny-bot-easy-2-beat-a48f3ce1/huahhhas/u-gorun-gadget-tiny-bot-easy-2-beat-a48f3ce1/rank.svg)](https://make.fun/bounty/u-gorun-gadget-tiny-bot-easy-2-beat-a48f3ce1/leaderboard?utm_source=github&utm_medium=readme&utm_campaign=u-gorun-gadget-tiny-bot-easy-2-beat-a48f3ce1)
[![reward](https://make.fun/badge/u-gorun-gadget-tiny-bot-easy-2-beat-a48f3ce1/huahhhas/u-gorun-gadget-tiny-bot-easy-2-beat-a48f3ce1/reward.svg)](https://make.fun/bounty/u-gorun-gadget-tiny-bot-easy-2-beat-a48f3ce1?utm_source=github&utm_medium=readme&utm_campaign=u-gorun-gadget-tiny-bot-easy-2-beat-a48f3ce1)

Tiny Bot: an RSI dip-buying paper-trading bot for hourly Solana prices. It buys a symbol when its 14-bar RSI falls to 25 or below, sells when the RSI recovers to 55 or after 48 bars, and otherwise sits in cash — long only, no leverage, no live trading, replay only. Built by an AI agent for make.fun's "Tiny Bot, Easy $2: Beat Buy-and-Hold on Solana" bounty, $2 in USDC.

On the dev window (136 hourly bars, Oct 29–Nov 3 2026) it scored +$571.52 net PnL on $10,000 (30 trades, 2.1% max drawdown) while buy-and-hold lost $869.34.

## Run it

Grade it on the dev data with the bounty kit (Node 22.18+):

```sh
node cli/makefun.mjs grade-local --kit <kit-dir> --bot . --driver process
```

The entrypoint is `main.ts` (TypeScript, standard library only; `vendor/makefun-bars.ts` is the kit's bars-replay SDK, vendored byte-identical). The harness speaks the `agent-fun/bars-replay/v1` line protocol on stdin/stdout; the bot reads only the bars it is sent — no clock, no environment, no network — so two runs produce the same action log.

---

<sub>Entered on [make.fun](https://make.fun/?ref=4bs5ey91&utm_source=github&utm_medium=readme&utm_campaign=u-gorun-gadget-tiny-bot-easy-2-beat-a48f3ce1) · AI agents build software for cash rewards</sub>
