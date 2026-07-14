# Cloud Engineer Academy - Progress Tracker

This file is the source of truth for my Cloud Engineer Academy progress.
See `curriculum-phases.md` for the full phase-by-phase curriculum and
`../CLAUDE.md` for mentor/teaching instructions.

Note: on 2026-07-14 the learning system was restructured — mentor instructions
moved into `../CLAUDE.md`, the future curriculum moved into
`curriculum-phases.md`, and the handbook was split by topic. See
`../journal/day-006.md` for details. That journal entry, plus the "Fetch vs
Pull, and Handling Diverged Branches" section added to `handbook/git.md` on
the same day, were both drafted by the AI and transcribed rather than
independently written — flagged for a quick spaced-review check-in (verbal,
not written) at a later session, to confirm the fetch/pull/diverged/conflict
concepts actually stuck.

## Completed Classes

### Day 001 - Linux Setup and Navigation

Status: Completed

Main topics:
- Installed Python
- Verified pip
- Installed Git
- Set up GitHub
- Installed WSL with Ubuntu
- Entered Linux for the first time
- Learned basic Linux navigation
- Created the Cloud Engineer Academy folder structure
- Created the Handbook and Journal
- Made the first Git commit

Journal:
- journal/day-001.md

Handbook:
- handbook/linux.md

---

### Day 002 - Working With Files in Linux

Status: Completed

Main topics:
- touch
- cat
- echo
- cp
- mv
- rm
- nano
- Created Linux file practice project
- Completed Linux file challenge
- Made Git commits for file practice and challenge

Journal:
- Added as "Day 2 Update" inside journal/day-001.md

Handbook:
- handbook/linux.md

Project:
- projects/linux-file-practice

---

### Day 003 - Git Fundamentals

Status: Completed

Main topics:
- README.md
- git status
- git diff
- git diff --staged
- git add
- git commit
- git log --oneline --graph
- git restore
- .gitignore
- Clean commit habits

Journal:
- Pending

Handbook:
- handbook/git.md

---

### Day 004 - GitHub Connection

Status: Completed

Main topics:
- Local repository vs remote repository
- GitHub repository setup
- SSH key generation
- SSH authentication with GitHub
- git remote -v
- git remote set-url origin
- git push -u origin main
- origin/main

Journal:
- journal/day-004.md

Handbook:
- handbook/git.md

Remote repository:
- github.com/JuanCamilo012599/cloud-engineer-academy

---

### Day 005 - GitHub Workflow and Sync

Status: Completed

Main topics:
- git pull
- git push
- origin/main
- local branch vs remote branch
- syncing local and remote repositories
- clean GitHub workflow

Journal:
- journal/day-005.md

Handbook:
- handbook/git.md

---

### Day 006 - Pulling Remote Changes and Merge Conflicts

Status: Completed

Main topics:
- Editing files directly on GitHub.com
- git fetch vs git pull
- Reading ahead / behind / diverged in git status
- Fast-forward pull
- Forcing a diverged history on purpose
- git pull --no-rebase (merge vs rebase vs ff-only)
- Reading and resolving conflict markers
- Completing a merge commit
- Mistake: edited locally instead of on GitHub, fixed with git restore

Assessment:
- Fetch/pull, ahead/behind/diverged, live conflict resolution: Practiced
- Handbook and journal writeups for this day: AI-drafted, needs review

Journal:
- journal/day-006.md

Handbook:
- handbook/git.md ("Fetch vs Pull, and Handling Diverged Branches")

---

## Current Next Class

Day 007 - Branching in Git

Topics:
- git branch (create, list, delete)
- git switch / git checkout for moving between branches
- why branches exist (isolating work before merging into main)
- merging a branch into main, including a case with no conflicts
- deleting a merged branch locally and on GitHub
