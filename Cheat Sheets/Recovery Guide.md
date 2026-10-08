# Recovery Guide

This guide covers ordinary recovery for a Git-backed Obsidian vault. Make a copy of the vault before attempting unfamiliar recovery. Do not use destructive Git commands just because a command looks faster.

## Check what changed

From the vault root:

```text
git status
git diff
git diff --cached
```

These commands show which files changed, what is not staged, and what is already staged. Review the filenames before using any command that restores or removes content.

## Make a safe checkpoint

When the current state is useful, save it before experimenting:

```text
git add -- path/to/file.md another/file.md
git diff --cached --check
git commit -m "Checkpoint notes"
```

Stage named files when possible. A checkpoint gives you a known point to return to, but it does not replace a remote backup or a tested copy of the vault.

## Recover an uncommitted edit

If a file contains accidental changes and the last committed version is the one you want, inspect the diff first:

```text
git diff -- path/to/file.md
```

Only after checking the path and diff, restore that specific file:

```text
git restore -- path/to/file.md
```

This discards uncommitted changes to that file. Do not use it on the whole vault unless you have deliberately confirmed that every uncommitted change can be lost.

If the change is staged, inspect it with `git diff --cached` and unstage it before deciding whether to edit or restore it:

```text
git restore --staged -- path/to/file.md
```

## Recover a committed change

Do not rewrite shared history just to undo an ordinary commit. For a commit that has already been shared, use a new reverting commit after reviewing the change:

```text
git log --oneline -5
git show <commit>
git revert <commit>
```

If you are unsure which commit or file should be recovered, stop after inspection and make a copy before asking for help.

## Obsidian File Recovery

Obsidian may retain recoverable versions of recently edited notes when File recovery is enabled. Open **Settings → Core plugins → File recovery** and inspect the available snapshots. Restore or copy the needed text into a new note first when possible, then compare it with the current file before replacing anything.

File recovery is not a complete backup system. It may not cover deleted files, older history, attachments, or another device. Git commits, synchronized copies, and periodic archives serve different recovery needs.

## If synchronization caused a conflict

Stop editing the conflicting file until you understand which copy contains the desired content. Keep both versions, compare them, and preserve the useful material in one deliberate edit. Commit or archive the resolved result after checking the note and its links.
