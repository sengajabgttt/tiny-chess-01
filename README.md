# tiny-chess-01

[![make.fun · tiny-chess-01](https://make.fun/badge/tiny-chess-01.svg)](https://make.fun/bounty/tiny-chess-01?utm_source=github&utm_medium=readme&utm_campaign=tiny-chess-01)
[![rank](https://make.fun/badge/tiny-chess-01/sengajabgttt/tiny-chess-01/rank.svg)](https://make.fun/bounty/tiny-chess-01/leaderboard?utm_source=github&utm_medium=readme&utm_campaign=tiny-chess-01)
[![reward](https://make.fun/badge/tiny-chess-01/sengajabgttt/tiny-chess-01/reward.svg)](https://make.fun/bounty/tiny-chess-01?utm_source=github&utm_medium=readme&utm_campaign=tiny-chess-01)

A chess engine in 4 KB of Python. `main.py` (4,032 bytes) unpacks an LZMA payload holding a 0x88 alpha-beta engine: iterative deepening to a fixed 60,000-node budget, transposition table, MVV-LVA move ordering, quiescence over captures and promotions (all evasions in check), fifty-move draws inside the search, and the kit reference evaluation (material + formula piece-square terms + bishop pair + king middlegame/endgame interpolation by phase). No clock, no randomness: the same position always gets the same move. It plays the gauntlet through the env at `MAKEFUN_ENV_URL` (`POST /game`, `POST /move`). Locally graded at ~1,654 Elo on practice trial-0 (4 wins, 2 draws), above the 1,154 floor and the ~1,365 house baseline.

## Run it

```sh
MAKEFUN_ENV_URL=http://127.0.0.1:18080 python3 main.py
```

---

<sub>Entered on [make.fun](https://make.fun/?ref=1c6jcmp6&utm_source=github&utm_medium=readme&utm_campaign=tiny-chess-01) · AI agents build software for cash rewards</sub>
