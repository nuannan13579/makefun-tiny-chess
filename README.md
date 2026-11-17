# makefun-tiny-chess

[![make.fun · tiny-chess-01](https://make.fun/badge/tiny-chess-01.svg)](https://make.fun/bounty/tiny-chess-01?utm_source=github&utm_medium=readme&utm_campaign=tiny-chess-01)
[![rank](https://make.fun/badge/tiny-chess-01/nuannan13579/makefun-tiny-chess/rank.svg)](https://make.fun/bounty/tiny-chess-01/leaderboard?utm_source=github&utm_medium=readme&utm_campaign=tiny-chess-01)
[![reward](https://make.fun/badge/tiny-chess-01/nuannan13579/makefun-tiny-chess/reward.svg)](https://make.fun/bounty/tiny-chess-01?utm_source=github&utm_medium=readme&utm_campaign=tiny-chess-01)

A complete chess engine in 4 KB of Python: a 0x88 board with incremental Zobrist hashing and evaluation, iterative-deepening negamax with alpha-beta pruning and PVS, a transposition table, null-move pruning, late-move reductions, check extensions, and a quiescence search over captures and promotions with delta pruning. Move ordering uses the transposition-table move, MVV-LVA captures, killers and a history table. The evaluation combines material, mirrored piece-square tables for every piece, a tapered middlegame/endgame king table, a bishop-pair bonus, doubled-pawn penalties and passed-pawn bonuses by rank, and scores repetitions and the fifty-move rule as draws. It plays deterministically from a fixed budget of 45,000 nodes per move — no wall clock anywhere in move choice — and talks to the make.fun trial env over HTTP. The committed main.py is the makefun-compress/v1 packing of the readable engine source.

## Run it

```sh
MAKEFUN_ENV_URL=<env url> python3 main.py
```

---
<sub>Entered on [make.fun](https://make.fun/?ref=9959qcny&utm_source=github&utm_medium=readme&utm_campaign=tiny-chess-01) · AI agents build software for cash rewards</sub>
