# Obsidian Setup

This vault includes a small set of optional community plugins. They are installed in the repository so the vault can be shared as a complete edition, but community plugins are disabled by default in this baseline. Enable only the ones you understand and want to use.

## Core Obsidian features

The vault uses Obsidian's built-in Daily Notes and Templates features. The repository includes portable settings for:

- daily notes in `Daily Notes/`;
- the standard template in `Templates/Daily Notes Template.md`;
- templates in `Templates/`.

You can change these settings for your own workflow without changing the note structure.

## Included optional plugins

| Plugin | Useful for | Considerations |
| --- | --- | --- |
| Calendar | Viewing and opening daily notes from a calendar | Optional convenience for daily-note navigation |
| Editing Toolbar | A formatting toolbar and optional editing assistance | Its AI features are disabled and unconfigured in this vault; review its consent and provider settings before enabling them |
| Linter | Consistent Markdown formatting and metadata style | Start with conservative rules and review changes before applying them broadly |
| Style Settings | Theme and CSS-variable controls | Useful only when a theme or plugin exposes settings through it |
| Tasks | Searching and managing tasks across notes | Adds query syntax and complexity; ordinary Markdown checkboxes work without it |
| Advanced Tables | Easier table editing and formatting | Useful when the vault contains tables, otherwise unnecessary |
| Tag Wrangler | Renaming, merging, and navigating tags | Useful for a tag-heavy vault, but not required by the starter workflow |

The versions in the repository are a snapshot and may become out of date. Read each plugin's current documentation before relying on it for important data.

## Enabling or removing plugins

1. Open **Settings → Community plugins**.
2. Turn off Restricted mode only if Obsidian requires it for the plugin you want to use.
3. Enable one plugin at a time and check that it behaves as expected.
4. Disable or uninstall plugins that do not help your workflow.

Removing a plugin from Obsidian does not necessarily remove its tracked files from a Git checkout. If you want the edition itself to stop carrying a plugin, remove it deliberately from the repository and update this note.

## AI plugin boundary

The Editing Toolbar configuration is shipped with its AI features disabled, without accepted consent, and without a configured provider or model. This is intentional. The daily workflow in this vault is tool-agnostic and does not require an AI plugin inside Obsidian. You may use an external AI tool instead, provided you understand what notes it can access and where its data goes.
