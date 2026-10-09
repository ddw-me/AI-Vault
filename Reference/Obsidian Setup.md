# Obsidian Setup

This note explains how to install Obsidian, open this vault, verify its shipped settings, and decide whether to enable optional features. If you are new to Obsidian, start here before following the [Quick Start](../Cheat%20Sheets/Quick%20Start.md).

## Install Obsidian and open the vault

1. Download Obsidian from the official [Obsidian download page](https://obsidian.md/download) and install it for your computer or device.
2. Obtain this vault by cloning the repository or downloading an archive. If you received an archive, extract it before opening it.
3. In Obsidian, choose **Open folder as vault** and select the folder containing `README.md`. Do not open one of its subdirectories as the vault.
4. If you are viewing the repository on GitHub, the Markdown files and their relative links can also be read directly there. Opening the folder in Obsidian is required for editing and using the vault as a working system.

Obsidian stores the vault's notes as ordinary Markdown files alongside its local configuration. This makes the notes portable and lets you use Git or another backup method, but it also means that synchronized copies should be set up and tested carefully.

## First-run checks

This vault uses Obsidian's built-in Daily Notes and Templates features. After opening it, verify that these settings are present and adjust them only if you want a different layout:

- daily notes in `Daily Notes/`;
- the standard template in `Templates/Daily Notes Template.md`;
- templates in `Templates/`;
- relative Markdown links with Wikilinks disabled.

See the official [Obsidian Help](https://help.obsidian.md/) for current instructions when menu names or settings differ between versions.

## Theme and optional plugins

The vault includes the Border theme as its default appearance. If you prefer Obsidian's standard appearance, open **Settings → Appearance → Themes** and select **Default**.

The repository includes optional community plugins, but they are disabled by default in this baseline. When Obsidian warns that the vault contains community plugins or asks whether to trust them, declining is safe: the core workflow does not require any community plugin. Enable only the plugins you understand and want to use.

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
