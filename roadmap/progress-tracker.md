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

### Day 008 - Professional Commit Messages and Pull Requests

Status: Completed

Pre-class check: confirmed Day 007's deferred items were done before
starting new material — `journal/day-007.md` was written (independently,
includes a genuine mistake/reflection), and the two conceptual
`handbook/git.md` entries ("Why branches exist", fast-forward vs. merge
commit) had been rewritten in Juan's own words. Verified by reading both
files, not just taking his word for it.

Spaced-review check-in (verbal, before new material):
- Fetch vs. pull: correct, no issues.
- "Diverged" — first answer repeated the Day 007 misconception ("a
  conflict between lines"). Corrected again: diverged = both sides have
  unique commits in their history; conflict is a possible *consequence*
  only if the same lines changed. Second attempt ("if changes are on
  different lines you can diverge with no conflict") was correct — held up
  under a follow-up question, not just recited.
- Fast-forward vs. merge commit (Day 007): correct ("main hasn't moved
  since I created the branch").

Covered:
- `man git-commit` DISCUSSION section: summary line ≤50 chars, and why
  Git treats the text before the first blank line as the commit "title"
  (used standalone in `git log --oneline`, GitHub UI, `git-format-patch`).
- Commit message convention practiced live: staged a real change, wrote
  the summary line himself (`Add test line to git.md`), committed.
  Confirmed lowercase-vs-capitalized first-letter is a per-project style
  choice, not a Git rule (his stated preference: lowercase).
- Pull requests: purpose (review before merging into `main`, vs. `git
  merge` which is a local, unreviewed operation) via GitHub's "About pull
  requests" doc. Confirmed understanding: a PR compares a base branch and
  a compare branch.
- Documentation integrity catch (recurring pattern, 3rd occurrence after
  Day 006/007): first draft of the "What's a pull request?" handbook entry
  was copied near-verbatim from GitHub's docs (the draft-PR paragraph
  specifically, which also showed a conceptual mix-up — describing draft
  PRs, not PRs in general). Rejected twice; third attempt was genuinely his
  own words and conceptually correct.
- Full PR lifecycle hands-on: created `day-008-pr-practice`, committed,
  pushed with `git push -u origin <branch>`, opened a real PR on GitHub
  (`#1`), reviewed the diff via the "Files changed" tab, explained the
  three merge-strategy options (merge commit / squash / rebase — rebase
  discussed but not used), chose squash-and-merge with reasoning (one
  commit on the branch was a meaningless placeholder).
- Unplanned real mistake, used as a live teaching moment: an earlier
  commit (`add test line to git.md`) had been made directly on local
  `main` instead of on a branch — the exact anti-pattern from Day 007.
  After the PR squash-merged, local `main` and `origin/main` showed as
  diverged. Diagnosed together (not handed the answer): squash-merge
  creates a brand-new commit with no ancestry link to the original
  branch commits, so the local-only commit and the new squashed commit on
  `origin/main` had overlapping content but zero shared history. Verified
  with `git show origin/main:handbook/git.md` that nothing local was
  unique before recovering with `git reset --hard origin/main` (Juan ran
  it himself, understood why it was safe in this specific case before
  running it).
- Real gotcha caught during branch cleanup: `git branch -d
  day-008-pr-practice` did not refuse to delete despite the branch's
  commit not being an ancestor of `main` post-squash — it warned instead
  of refusing, because `-d`'s safety check compares against the branch's
  own upstream, not against `main`. Flagged explicitly as "not a reliable
  safety net after a squash-merge."
- Handbook (`handbook/git.md`) updated by Juan: commit message convention,
  and all three merge strategies (rebase marked explicitly "not practiced
  yet"), all in his own words after one rejected copy/dictation attempt.

Process change agreed for journal-writing (going forward): Juan asked to
revert to an AI-drafted-narrative pattern for journals, referencing Day 006
as "the perfect balance." Corrected using the actual tracker record — Day
006's journal and Day 007's handbook section were both flagged as
AI-drafted/transcribed and *not* considered good practice; `day-007.md`
(written independently) was the actual example that worked. Landed on a
compromise for `journal/day-008.md` and future days: mentor asks a fixed
set of short content questions (what happened / what confused you / what
mistake or uncertainty / one-sentence concept takeaway), Juan answers each
in one line from his own recall, mentor only formats those answers into
the existing template (headers/bullets) — no content or phrasing supplied
by the mentor. Use this pattern for future daily journal entries unless
Juan raises it again.

Assessment:
- Commit message convention (summary line length, imperative mood): Practiced
- PR workflow (create, review diff, choose merge strategy, merge): Practiced
- Squash-merge mechanics and its effect on local/remote divergence: Introduced,
  reinforced through a real (unplanned) hands-on recovery — needs another
  rep before "independently demonstrated"
- `git reset --hard`: Introduced (one guided, verified-safe instance only;
  revisit properly under Day 009's "recovery from mistakes" topic)
- Diverged vs. conflict distinction: Practiced, held up under a second
  spaced-review pass after one repeated wrong answer

Journal:
- journal/day-008.md

Handbook:
- handbook/git.md ("What's a pull request?", "Commit message convention",
  "Merge Strategies")

Repo state at end of session: `main` and `origin/main` synced at `8676b70`,
only `main` remains locally and on GitHub, working tree clean.

---

## Current Next Class

Day 009 - Recovery from common Git mistakes (`git reset` --soft/--mixed/
--hard, `git revert`, `git reflog`, `git commit --amend`) — the last
remaining Phase 1 Git/GitHub curriculum gap (PRs and commit messages are
now covered as of Day 008).

Before starting Day 009:
- Quick verbal spaced-review check-in: why squash-merge caused local/remote
  divergence on Day 008 (new commit, no shared ancestry), and why `git
  branch -d` didn't refuse to delete the squash-merged branch.
- Note: `git reset --hard origin/main` was already used once on Day 008 as
  a guided recovery — Day 009 should build the fuller mental model (soft
  vs. mixed vs. hard, when each is appropriate, reflog as the safety net)
  rather than starting from zero.
- Rebase-and-merge was explained conceptually but never actually run —
  flagged as unpracticed, pick up opportunistically when a suitable branch
  exists.
- Continue the new journal-writing process from Day 008 (short Q&A,
  mentor formats only) for the Day 009 entry.
