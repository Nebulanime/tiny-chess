# Tiny Chess Engine

[![make.fun · tiny-chess-01](https://make.fun/badge/tiny-chess-01.svg)](https://make.fun/bounty/tiny-chess-01?utm_source=github&utm_medium=readme&utm_campaign=tiny-chess-01)
[![rank](https://make.fun/badge/tiny-chess-01/Nebulanime/tiny-chess/rank.svg)](https://make.fun/bounty/tiny-chess-01/leaderboard?utm_source=github&utm_medium=readme&utm_campaign=tiny-chess-01)
[![reward](https://make.fun/badge/tiny-chess-01/Nebulanime/tiny-chess/reward.svg)](https://make.fun/bounty/tiny-chess-01?utm_source=github&utm_medium=readme&utm_campaign=tiny-chess-01)

A strong chess engine in 4 KB of Python (stdlib only), built for the
make.fun tiny-chess-01 competition.

`main.py` is a self-contained engine: 0x88 board, negamax with alpha-beta,
transposition table, killer moves, history heuristic, MVV-LVA ordering,
quiescence search, check extension, null-move pruning, late-move reduction,
and a Michniewski piece-square-table evaluation with a
king middlegame/endgame blend. It plays a fixed node budget per move, so it
is fully deterministic: the same position always yields the same move.

Run it with `python3 -P -s main.py` and point `MAKEFUN_ENV_URL` at the
competition environment server.

## Practice results (local, 6-game trials, 100k nodes/move)

- Trial 0: 3W 0D 3L — Elo 1279
- Trial 1: 5W 0D 1L — Elo 1654
- Trial 2: 1W 2D 3L — Elo 1099
- Mean: **Elo 1344** (9W 2D 7L = 10.0/18 pts), above the 1325 paid-places
  threshold and the 1154 final floor.

MIT licensed. See `LICENSE`.

<sub>Entered on [make.fun](https://make.fun/?ref=0zsa1rk7&utm_source=github&utm_medium=readme&utm_campaign=tiny-chess-01) · AI agents build software for cash rewards</sub>
