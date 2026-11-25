# Briefs, Reports and sizing

## The Brief

Start a role with a Brief of exactly these lines:

    SPRINT GOAL: <one sentence>
    TASK: <letter> <title> (normal | small)
    SPEC: <path, or the three lines of a small task>
    TICKETS: <ticket numbers, when the work comes from a tracker>
    OWNS: <folders this role may change>
    TIME: <minutes>
    DONE MEANS: <the checks, and the project's commit rule>
    CHANGED: <files or commits this task touched>

- CHANGED is for QA and QC only. Give QC the builders' Reports too.
- TICKETS is for work the product lead gave as tickets: read [TICKETS.md](TICKETS.md) first.
  With no tickets, leave TICKETS out.
- Add the project's hard rules a role cannot find by itself: push, commit and secret rules.
- The BA's Brief, the challenge round and the BA's update pass have their own TASK and SPEC
  lines: see PLAN in STEPS.md. Refine Briefs are in REFINE.md.
- OWNS: the project's own list wins. With none, you set it per task, so that no two roles
  running at once share a file.
- Commits: the project's rule wins. With none, each builder commits its own task's files when
  its work is done, in one commit whose message starts with the task letter. You commit the
  notes, the specs and any line you added to the instructions file at each stop. Nobody pushes.
  Put the rule in DONE MEANS.
- Side by side only when tasks share no files and no single resource: one local database, one
  simulator, one dev port, one git index. Say which task waits for which.
- A role past one and a half times its TIME: read where it is, then take it back, split it or
  start it again. Never wait without a limit.

## Reading a Report

A Report has these lines: VERDICT, MISSING, REUSED, NEW, FINDINGS (QA and QC), LATER, PROOF.

- A line is missing, PROOF above all: not accepted. Send it back once and name the line.
- Check the work, not the summary: the files it names really changed (`git status`,
  `git diff --stat`), the tests it names exist, and nothing outside OWNS changed. A claim the
  files contradict: not accepted. Send it back once and name the claim.
- Before you start QA and QC, note `git status --porcelain` and `git rev-parse HEAD`. After both
  return, both must read the same. A difference makes both runs void: have the builder who owns
  the changed file put it right, then start QA and QC again.
- MISSING: get the piece (another role, the docs, or one question to the product lead) while
  the work goes on. When it arrives, have the assumption checked.
- NOT READY with FINDINGS `nothing`: a case could not be run. No builder gets it back, and it
  uses up no check round. Get what is MISSING and check again once. If you cannot, the task is
  built, not checked: its goal line stays unmarked, and the STOP 2 message lists what
  nobody could check, for the product lead's eyes. Their answer there settles that goal line.
- LATER: copy each line into `LATER.md` under Confirmed, unless it is already there. No work
  starts from it.
- NEW: something made new where an existing thing would do goes back to its builder.
- A Report is yours to act on. The product lead hears the outcome, in one line, when the task
  changes state.

## Sizing

- Size from this project's own record: the Status in `SPRINT.md` says what the last sprint
  really took.
- With no record, your first numbers are guesses, and you say so. On a small change a role
  pass takes 2 to 10 minutes. A screen with device checks or a back-end piece takes 20 to 60.
  Start from the small end, and after PLAN rescale the build by how long planning really took
  against your guess.
- The time box is the team's working time, counted from the product lead's yes. Waiting for
  them never uses it up, and you never give them a deadline.
- The real limits are single resources and the product lead's decision time.
- When an estimate was wrong, say so in one line and size the next sprint from what this one
  really took.
