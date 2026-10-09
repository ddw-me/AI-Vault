# Recovery Guide

This guide covers ordinary recovery for a Git-backed Obsidian vault. Make a copy of the vault before attempting unfamiliar recovery. Do not use destructive Git commands just because a command looks faster.

## Recovering an archived vault

An extracted archive does not contain Git history. Preserve the original extracted folder before experimenting, and open a saved copy in a separate folder when comparing or recovering notes.

### Without Git

1. Keep the original vault folder unchanged.
2. Make a copy of the vault or restore the backup into a separate folder.
3. Compare the affected notes and attachments side by side.
4. Copy only the selected content back into the working vault.
5. Open the changed notes in Obsidian and check their links before continuing.

### Optional Git setup

Git is optional for an archive recipient. If you want local checkpoints and history, initialize a repository after reviewing the extracted vault:

```text
cd /path/to/vault
git init
git status
git add -- path/to/selected/files
git diff --cached --check
git commit -m "Initial vault checkpoint"
```

Review staged files before the first commit and do not add credentials, private keys, or other sensitive material. Configure a remote only if you understand where the vault will be stored and who can access it.

## Using a remote repository

After creating local commits, you can connect the vault to a remote Git repository so its history and notes have an off-device copy. GitHub supports private repositories that are accessible only to you and people you explicitly share them with; see GitHub's [about repositories](https://docs.github.com/en/repositories/creating-and-managing-repositories/about-repositories) and [repository access guidance](https://docs.github.com/en/repositories/managing-your-repositorys-settings-and-features/repository-access-and-collaboration). GitLab is another option: its projects can be private, with access limited to project members; see [GitLab project and group visibility](https://docs.gitlab.com/user/public_access/).

Before pushing a vault, review the files and history for credentials, private keys, personal information, and notes you do not want stored with that provider. A private repository is access-controlled, not automatically encrypted or risk-free. Enable strong account protection, share access deliberately, and confirm the provider's storage and retention terms.

The remote repository provides an off-device copy, while local commits provide convenient checkpoints and history. They solve related but different recovery problems. After creating a private remote, add it as `origin` and push committed changes; see the provider's Git instructions if you need help creating the remote or configuring authentication.

Once `origin` is configured, a simple working cycle is:

```text
git pull --ff-only
git add -- path/to/changed/files
git diff --cached --check
git commit -m "Checkpoint notes"
git push
```

Pull before starting work so you have the latest remote changes. Commit related local changes as a checkpoint, then push the commit so the remote has the same recovery point. If `git pull --ff-only` or `git push` reports a conflict or other error, stop and inspect the state before trying a different command.

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
