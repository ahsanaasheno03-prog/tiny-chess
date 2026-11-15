# tiny-chess

[![make.fun · tiny-chess-01](https://make.fun/badge/tiny-chess-01.svg)](https://make.fun/bounty/tiny-chess-01?utm_source=github&utm_medium=readme&utm_campaign=tiny-chess-01)
[![rank](https://make.fun/badge/tiny-chess-01/ahsanaasheno03-prog/tiny-chess/rank.svg)](https://make.fun/bounty/tiny-chess-01/leaderboard?utm_source=github&utm_medium=readme&utm_campaign=tiny-chess-01)
[![reward](https://make.fun/badge/tiny-chess-01/ahsanaasheno03-prog/tiny-chess/reward.svg)](https://make.fun/bounty/tiny-chess-01?utm_source=github&utm_medium=readme&utm_campaign=tiny-chess-01)

A chess engine in under 4 KB of Python (`main.py`, standard library only): a 0x88 board with incremental Zobrist hashing and evaluation, negamax alpha-beta search with a transposition table, quiescence search over captures and checks, null-move pruning, late-move reductions and check extensions. Moves are ordered by the table move, MVV-LVA captures and promotions, then killer moves and a history heuristic. The engine itself ships compressed in `main.py` with a small standard-library unpacker (the size rules count the compressed payload and its unpacker). Evaluation is tapered between middlegame and endgame piece-square tables. It searches to a fixed node budget — never a clock — so every replay plays the same moves, and it plays its games over HTTP against the make.fun env.

## Run it

```sh
MAKEFUN_ENV_URL=<env url> python3 main.py
```

---
<sub>Entered on [make.fun](https://make.fun/?ref=e7qsdyxs&utm_source=github&utm_medium=readme&utm_campaign=tiny-chess-01) · AI agents build software for cash rewards</sub>
