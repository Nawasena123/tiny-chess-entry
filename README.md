# tiny-chess-entry

A chess engine in 4 KB of Python for make.fun's tiny-chess-01 bounty.

- 120-square mailbox board, rotated each ply, pseudo-legal moves checked for legality in the search
- piece-square tables from simple formulas, blended by game phase at the root
- PVS alpha-beta, iterative deepening, transposition table, null move, late-move reductions, reverse futility, futility and late-move pruning, check extension
- quiescence over captures and promotions (its own capture generator), MVV-LVA, killers, history
- legality tested only for moves that can expose the king
- a fixed node budget spread over the trial: no clock, same moves every run

`main.py` is the LZMA-packed engine (made with `makefun compress`). MIT licensed.
