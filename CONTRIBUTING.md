# Contributing to DigiPassPortPaper

This repository uses **Git** for version control and **GitHub** as the central copy. You do not need to be a Git expert to contribute, but please follow the workflow below so that we do not overwrite each other's work.

## 1. First-time setup

1. Create a GitHub account if you do not have one.
2. Ask the repository owner to add you as a **collaborator** with **Write** permission.
3. Install Git on your computer, or use **GitHub Desktop** if you prefer a graphical interface.
4. Clone the repository once:
   ```bash
   git clone git@github.com:heinz-preisig/DigiPassPortPaper.git
   cd DigiPassPortPaper
   ```

## 2. Normal editing workflow

Before you start editing, always make sure you have the latest version:

```bash
git pull origin master
```

Then edit the files you need. When you are done, commit and push your changes:

```bash
git status                   # see what you changed
git add <files-you-changed>  # or use `git add -A` to stage all
git commit -m "Brief description of the change"
git push origin master
```

Use a clear commit message, for example:

- `Update portal architecture section to clarify federation`
- `Add references to ECHA substance registry`
- `Fix typo in abstract`

## 3. How to avoid merge problems

The most common problem is that two people edit the same file at the same time. Git will then produce a **merge conflict** that must be resolved manually. To avoid this:

- **Pull before every editing session.**
- **Push small changes often.** Do not wait until you have edited ten files.
- **Tell others which file you are working on** (for example, in a short message).
- **Do not edit the same file at the same time** as someone else.

If you followed these rules and still see a conflict, follow the steps in the next section.

## 4. What to do if a merge conflict happens

If `git pull` or `git push` prints a message about a **conflict**, stop and do not close the terminal.

1. See which files are in conflict:
   ```bash
   git status
   ```
2. Open each conflicted file in your editor.
3. Look for markers like this:
   ```
   <<<<<<< HEAD
   text from the version on GitHub
   =======
   text from your local version
   >>>>>>> your-branch
   ```
4. Decide which text to keep (or combine both), then delete the `<<<<<<<`, `=======`, and `>>>>>>>` markers.
5. Save the file.
6. Stage and commit the resolved file:
   ```bash
   git add <file>
   git commit -m "Resolve merge conflict in <file>"
   git push origin master
   ```

If you are unsure which version is correct, **stop and ask**. Never force a push (`git push --force`) unless the repository owner tells you to.

## 5. Project layout

- `DPP____The_Graph_of_Passport_Model/main.tex` — the main LaTeX file. Open this file to compile the paper.
- `DPP____The_Graph_of_Passport_Model/*.tex` — individual sections.
- `DPP____The_Graph_of_Passport_Model/figures/` — PDF figures.
- `DPP____The_Graph_of_Passport_Model/references.bib` — bibliography entries.
- `pyproject.toml` — Python project metadata (used only for tooling).

You do **not** need to commit generated files such as `.aux`, `.log`, `.out`, `.synctex.gz`, or compiled PDFs; they are ignored automatically through `.gitignore`.

## 6. If you do not want to use the command line

You can use **GitHub Desktop** (free from https://desktop.github.com/) or another Git GUI. The steps are the same: **pull**, edit, commit, **push**.

## 7. Need help?

If you are stuck, do not guess. Ask the repository owner or another co-author for help before running commands you do not understand.
