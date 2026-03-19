# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project

Single-file Tic Tac Toe game (`tictactoe.html`). No build system, no dependencies, no package manager — open the file directly in a browser to run it.

## Git Workflow

After completing any meaningful unit of work, commit and push immediately so progress is never lost:

```bash
git add <files>
git commit -m "Short imperative description of what changed"
git push
```

Use clean, descriptive commit messages in imperative tone (e.g. "Add win animation", "Fix draw detection bug").

## Architecture

Everything lives in `tictactoe.html`:
- **CSS** (inline `<style>`) — dark theme, grid layout, win highlight animation
- **HTML** — 3×3 board of `.cell` divs, score display, restart button
- **JavaScript** (inline `<script>`) — game state (`board[]`, `current`, `gameOver`, `scores`), win detection via `WINS` constant (8 winning combinations), score persistence across restarts
