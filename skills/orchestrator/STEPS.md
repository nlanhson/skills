# The sprint, step by step

## PLAN

1. With the product lead, settle the sprint goal in one sentence, the time box and the tasks.
   Tasks come from what they ask for and from the Confirmed list in `LATER.md`. A line that
   becomes a task is deleted from `LATER.md`.
2. Write the goal lines: numbered, each one true or false.
3. Give each task a letter, a size (below) and the goal line it serves.
4. Ready check for the sprint. Does the team have what these tasks need: a design system when
   there is a screen, code rules, the product docs, a way to run the app and its tests? A gap
   does not stop the sprint. It goes into the STOP 1 message as one line: what is missing, and
   what the roles will assume instead.
5. Start `ba` once, for all normal tasks. It writes one spec per task. Its Brief has:

       TASK: A <title>, B <title> (normal): write the specs
       SPEC: none yet. The ask, in the product lead's words: "<their words>"
       OWNS: <the specs folder>

6. One challenge round per sprint. Start `designer`, `developer` and `qa` side by side. Each
   reads all the specs once and changes no file. Their Reports carry `CHALLENGE:` lines, and
   QA's also carries `TEST CASE:` lines. Their Brief has:

       TASK: challenge round on A, B
       SPEC: <the spec paths>
       OWNS: nothing

7. A challenge counts only if it says how the issue hurts the sprint goal and comes with a fix.
   Anything else is a line for `LATER.md`.
8. Settle each challenge: yourself when it is routine, with one question when it is taste or
   costly to undo. Then start `ba` again. Only the BA writes specs. Its Brief has:

       TASK: update the specs
       SPEC: <the accepted changes and QA's test cases, spec by spec>
       OWNS: <the specs folder>

9. Write `SPRINT.md`.
10. STOP 1. Send the STOP 1 message. On yes, start the Status with `STOP 1 passed` and commit
    the notes and the specs.

The STOP 1 message is 20 lines at most, with no table: the goal lines; the tasks, one line each
with size and time; at most three open points, the ones that most change what gets built, your
pick first; what is missing and what the team will assume, one line; then one question:
approve? Everything else stays in `SPRINT.md` and the specs.

## Two sizes of task

- Normal: the full path.
- Small: about 30 minutes or less at role pace, with nothing new to define. No BA and no
  challenge round. You write it as three lines in the Brief's SPEC (what, where, done means).
  One role builds it and one role checks it: QC for a change of look or wording, QA for a change
  of behaviour. Talk small tasks through at PLAN, one short yes or no each. They then run in
  the sprint like any other task.

## BUILD

Per task, in the order `SPRINT.md` gives:

1. Designer first when the task has a screen, then Developer. Developer first when the screen
   cannot run without the new logic. Side by side when they share no files and no single
   resource. Where the screen and the logic meet at a name (a function, an action), put that
   name in both Briefs.
2. A builder that lacks something reports it under MISSING with what it assumed, and keeps
   working. Get the piece while the work goes on.
3. After each Report, update the task's Status in `SPRINT.md`. At the end of every session,
   replace the Status line: what finished, what is running, what waits on whom, and what the
   next session starts with.

## CHECK

Per built task:

1. Start `qa` and `qc` side by side. Fill in CHANGED. Give QC the builders' Reports.
2. Both say READY: the task is done. When all the tasks of a goal line are done, mark it true.
3. One says NOT READY: send its FINDINGS to the builder who owns those files, then check again.
   Two rounds at most. Still failing: cut the task or park it in `LATER.md`, and say so.

## SHIP

1. Check each goal line.
2. STOP 2. Send the STOP 2 message. They review. Then read back `## Ideas to confirm` one by
   one: keep (move it to Confirmed) or drop (delete it). Commit the notes.

The STOP 2 message is 20 lines at most, with no table: the verdict; each goal line true or
false; what was cut, parked or changed beyond the ask; how to see the result; then one question:
does it pass? Everything else stays in the notes.

## Closing a sprint

- Delete the specs of done tasks. Git keeps them.
- A choice that outlives the sprint goes in the project's decisions log as one line.
- `SPRINT.md` is replaced by the next sprint's, never added to.

## Note shapes

`SPRINT.md`:

    # Sprint <n>: <the goal in one sentence>

    Time box: <start> to <end>

    Goal lines:
    1. <a line that is true or false>

    | Task | Size | Serves line | Roles | Time | Status |
    |---|---|---|---|---|---|
    | A <title> | normal | 1 | Designer, Developer, QA, QC | 60 min | not started |

    Status: <100 words at most, replaced each session. It starts with `STOP 1 passed` once the
    plan is approved, and ends with what the next session starts with>

`LATER.md`:

    # Later

    ## Ideas to confirm
    - <date> <the idea in one line>

    ## Confirmed
    - <date> <the finding or idea in one line> (<who spotted it>)
