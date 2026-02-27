# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

This is a single-file Tic Tac Toe web application (`tictactoe.html`) with no build system or dependencies. Open it directly in any browser.

## Running the App

```bash
open tictactoe.html
```

## Architecture

Everything lives in `tictactoe.html` — HTML structure, CSS (dark theme), and JavaScript are all embedded in one file.

**Game state variables:**
- `board`: 9-element array for the grid
- `current`: active player (`'X'` or `'O'`)
- `over`: boolean for game-end state
- `scores`: win/draw tallies
- `mode`: `'human'` (2-player) or `'cpu'` (vs AI)
- `diff`: `'easy'` or `'hard'`

**AI implementation:**
- Hard mode: full minimax algorithm via `bestMove()` / `minimax()`
- Easy mode: 50% optimal (minimax), 50% random move via `easyMove()`

**Win detection:** `WINS` array defines all 8 winning combinations; `checkEnd()` evaluates after each move.
