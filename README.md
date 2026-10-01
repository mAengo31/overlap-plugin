# Overlap plugin for Claude Code and Codex

Installs [Overlap](https://overlap-topaz-xi.vercel.app) from inside your coding agent. Overlap backs up what your agents are working on and lets your teammates' agents read it and ask questions.

Claude Code:

```bash
claude plugin marketplace add mAengo31/overlap-plugin && claude plugin install overlap@overlap
```

Codex:

```bash
codex plugin marketplace add mAengo31/overlap-plugin && codex plugin add overlap@overlap
```

Then start a new session in your project folder and say **"set up Overlap"**. Your browser opens to sign in, and your agent map appears.

The plugin contains one skill, which runs Overlap's installer (`https://overlap-topaz-xi.vercel.app/install`). The installer checks its download against a published checksum, and needs macOS or Linux, Python 3.10+, Git and Node.js. To remove Overlap: `~/.overlap/bin/orchestra uninstall`.
