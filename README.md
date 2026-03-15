# SVCS Ignore (VS Code Extension)

The Simple Version Control System's *Simple* Ignore file... now with *Simple* colors.

This extension teaches VS Code how to read **`.svcsignore`** files without squinting, by giving them syntax highlighting with the **same vibes as `.gitignore`**.

Because if your version control system is simple, your eyeballs should be too.

---

## What is this?

SVCS has `.svcsignore`.

VS Code has highlighting for `.gitignore`.

Reality has unfairness.

This extension restores balance.

---

## Features

- Highlights **comments** (`# like this`)
- Highlights **negation rules** (`!not-this-one`)
- Highlights **directory patterns** (`build/`)
- Understands "no really, I meant a literal `#` or `!`" via escaping:
  - `\#not-a-comment`
  - `\!not-negation`

No AI. No blockchain. No telemetry. No "sign in to continue ignoring files".

Just colors.

---

## Example

```gitignore
# ignore build artifacts
dist/
*.log

# but keep this one
!important.log

# these are literal characters, not syntax
\#hashtags-are-files-too
\!loud-files
```

---

## Install (local)

### Quick test mode (recommended)
1. Open this extension folder in VS Code
2. Press `F5`
3. A new **Extension Development Host** window opens
4. Create/open a file named `.svcsignore`

### Install for real (VSIX)
```bash
npm i -g @vscode/vsce
vsce package
code --install-extension svcsignore-1.0.0.vsix
```

Reload VS Code and enjoy your freshly highlighted ignoring.

---

## Why not just rename it to `.gitignore`?

Because SVCS is *Simple Version Control System*, not *Somehow Vanished Convention System*.

Also: if you rename everything to `.gitignore`, at some point Git will show up and start making decisions.

---

## Known limitations

This is regex-based highlighting (TextMate grammar). It's designed to be practical and readable, not a perfect reimplementation of every obscure edge-case in ignore-file lore.

If you find a line that looks wrong, open an issue (or send a PR) with:
- the exact `.svcsignore` line
- what you expected to see
- what you actually saw
- your theme name (some themes are... expressive)

---

## License

MIT, just like always, plus the ancient universal license of:

> "Please don't make me debug your theme's neon orange."