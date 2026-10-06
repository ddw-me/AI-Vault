# Home-Level Agent Template

This is a starting point for a computer's home-level AI instructions. It is intentionally separate from the vault's root `AGENTS.md`.

The vault instructions should remain portable. A home-level file may describe the computer's role, available tools, local paths, and host-specific safety boundaries. Create a separate version for each computer when those details differ.

On a Unix-like system, an AI tool that reads `~/AGENTS.md` can use a symlink such as:

```text
ln -s /path/to/this/file ~/AGENTS.md
```

Do not put credentials, tokens, or confidential work instructions in a file intended for sharing.
