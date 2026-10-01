---
name: setup
description: Install or repair Overlap on this computer and connect the current project folder. Use when the user asks to set up, install, connect, update or remove Overlap.
---

# Set up Overlap

Overlap backs up what coding agents are working on and lets teammates' agents read it and ask questions. Setup installs a small local program (the agent map), signs the user in through their browser, and registers the Overlap hooks and MCP server for Claude Code and Codex.

1. Tell the user in one sentence that a browser tab will open for sign-in.
2. From the user's project folder, run exactly one of these, matching the agent you are:

   ```bash
   curl -fsSL https://overlap-topaz-xi.vercel.app/install | bash -s -- claude
   ```

   ```bash
   curl -fsSL https://overlap-topaz-xi.vercel.app/install | bash -s -- codex
   ```

   Allow a few minutes: it waits for the browser sign-in.
3. If it says to choose a project, ask the user which of the listed projects they want, then run `~/.overlap/bin/orchestra setup --url https://overlap-topaz-xi.vercel.app --project <name> --agent <claude|codex>`.
4. If it reports something missing (Python 3.10+, Git, Node.js), relay its instruction to the user. Do not install system software yourself.
5. When it finishes, tell the user: the Overlap page that opened shows their agent map; click **Choose folder** there to add more folders; start a new session in the folder so the hooks and the Overlap tools load.

Other requests:

- Update now: `~/.overlap/bin/orchestra update` (it also updates itself daily).
- Remove Overlap: confirm with the user first, then `~/.overlap/bin/orchestra uninstall --yes`.

Only ever download from `https://overlap-topaz-xi.vercel.app`. Never pass a sign-in token, key or password on a command line.
