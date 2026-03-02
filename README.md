# touchtypr
<img width="1536" height="1024" alt="ChatGPT Image Mar 2, 2026, 12_26_47 AM" src="https://github.com/user-attachments/assets/7ca39244-9977-4d5f-ad19-4bb76a0ca11f" />

A single-file, offline-first touch typing trainer tailored for programming.

touchtypr focuses on the characters and patterns you actually type when you code — across **Bash**, **Python**, and **Rust** — with three training modes:

- **Symbols**: language-shaped symbol families + letters (no backspace, wrong char = 0 points)
- **Tokens**: common idioms, commands, and syntax fragments (no backspace, wrong char = 0 points)
- **Scripts**: small useful scripts with comments (backspace allowed, but costs points)

Built as a standalone `index.html` you can open locally or host on GitHub Pages.

👉 **[Launch touchtypr](https://dimfield-git.github.io/touchtypr/)**
---

## Features

- **Bash / Python / Rust** language profiles
- **Three modes**: Symbols, Tokens, Scripts
- **Adaptive difficulty** toggle (difficulty adjusts after runs)
- **Strict newlines** toggle (recommended for Scripts)
- **Theme system**: Futuristic / Cyberpunk / Hacker (Light + Dark variants)
- **Brand header animations** per theme (shimmer / neon glow / hacker scan-glitch)
- **High scores** stored locally (per language + mode)
- **Syntax highlighting** in Tokens + Scripts (while preserving per-character correctness feedback)
- Works **offline**, no dependencies, no build step

---

## Quick start

### Run locally
Just open:

- `index.html`

in your browser.

### Serve locally (recommended)
Some browsers apply stricter rules to `file://` pages. If anything feels weird, serve it:

```bash
cd /home/dim/repos/touchtypr
python3 -m http.server 8000
```

Then visit: `http://localhost:8000`

---

## Repository layout

- `index.html` — **current stable** version (what you host)
- `versions/` — archived snapshots  
  - `touchtypr_v2.3.html` — the v2.3 release snapshot

---

## Controls

- `Esc` — restart run  
- `Ctrl/Cmd + Enter` — new prompt

---

## Scoring rules

### Symbols + Tokens
- Backspace disabled
- Correct character = +1 point
- Wrong character = +0 points (no penalty beyond lost opportunity)

### Scripts
- Backspace enabled
- Each backspace costs points
- Correct characters still increase score

High scores are stored in **localStorage** (per language + mode).

---

## Versioning

I keep `index.html` as the current release and store historical snapshots in `versions/`.  
This makes it easy to host the latest while keeping a clean archive.

---

## License

MIT
