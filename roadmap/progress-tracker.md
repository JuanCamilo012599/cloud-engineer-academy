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

## Completed Classes (continued)

### Day 007 - Branching in Git

Status: Completed

Covered:
- Spaced-review check-in on Day 006 concepts (fetch vs pull, diverged branches,
  conflict markers) before starting new material. Mostly solid; corrected one
  nuance — divergence is about commit history branching (both sides committed
  separately), not necessarily about the same lines changing. Conflict is a
  possible *consequence* of divergence, not the same thing.
- Why branches exist: walked through the concrete cost of committing straight
  to main (teammates pulling broken/unfinished work, blocked until it's fixed;
  worse if main auto-deploys to prod).
- git branch (no args) - lists branches, `*` marks current (HEAD).
- git branch <name> - creates a branch without switching to it.
- git switch <name> - moves HEAD to a branch (noted git checkout is the older,
  more overloaded equivalent).
- Demonstrated branch isolation directly: created `day-007-branching`, added
  and committed `branch-test.md` there, confirmed the file does NOT exist back
  on `main` until merged.
- git merge <name> - performed a fast-forward merge (day-007-branching into
  main, no divergence so no merge commit needed). Explained why Git could
  fast-forward here vs. the real merge commit from Day 006.
- git branch -d <name> - safe delete (refuses if unmerged); contrasted with
  -D (force delete, can lose unreachable commits) - discussed but not run.
- Full remote branch lifecycle on a second practice branch
  (`day-007-remote-practice`): created, switched, committed a file, pushed
  with `git push -u origin <branch>` (observed upstream tracking get set
  up), verified it appeared on GitHub via `git branch -a`, merged into main
  (another fast-forward), pushed `main`, then deleted the branch both
  locally (`git branch -d`) and on GitHub (`git push origin --delete`), and
  confirmed with `git branch -a` that only `main`/`origin/main` remained.
  Correctly predicted the final `git branch -a` output before running it.
- Teach-back: explained the full create → switch → merge → delete lifecycle
  unprompted. Correct on branch isolation and roughly right on fast-forward
  ("no divergence") and on deleting merged branches; both refined slightly
  (fast-forward specifically because `main` hadn't moved at all since the
  branch was created; deleting a merged branch is safe because its commits
  already live permanently in main's history — the branch name was just a
  temporary pointer).
- Local repo state at end of session: `main` up to date with `origin/main`,
  both practice branches deleted locally and remotely, working tree has
  only handbook/tracker doc edits pending commit.

Documentation note (flagged, same as Day 006): first draft of the
`## Branching in Git` section in `handbook/git.md` was written by
transcribing the mentor's dictated explanation almost verbatim rather than
independently — caught and named directly this session rather than let
slide. Agreed compromise: factual command definitions (branch/switch/merge/
-d/-D/push -u/push --delete) may stay as accurate reference notes; the two
conceptual entries (**why branches exist**, **fast-forward vs. merge
commit**) still need to be rewritten by Juan from his own teach-back
sentences (which were already correct in substance, just incomplete) rather
than from the mentor's fuller paragraph. Not done yet — deferred to next
session at Juan's request. Flagged for a quick spaced-review check-in
(verbal, not written) alongside the existing Day 006 flag.

Journal: Pending (not yet written for this day)
Handbook: `handbook/git.md` has a `## Branching in Git` section, but the two
conceptual entries need the from-scratch rewrite described above before
they should be considered done.

---

## Current Next Class

Day 008 - next Git/GitHub topic per curriculum-phases.md (to be selected
based on remaining Phase 1 Git/GitHub gaps — PRs, professional commit
messages, and recovery from common mistakes are not yet covered).

Before starting Day 008:
- Quick verbal spaced-review check-in covering both flagged items: Day 006
  (fetch/pull, diverged, conflict markers) and Day 007 (why branches exist,
  fast-forward vs. merge commit) — confirm concepts hold up without notes
  in front of him.
- Have Juan finish rewriting the two conceptual `handbook/git.md` entries
  from his own teach-back sentences (see Day 007 documentation note above),
  and write the Day 007 journal entry, before or at the start of that
  session.
