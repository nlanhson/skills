# The sprint, step by step

## PLAN

1. The product lead gives the goal, in words or as named tickets (then read TICKETS.md). Put
   it in one sentence. You set the tasks and the time box. Tasks come from what they asked for.
   A Confirmed line in `LATER.md` becomes a task only when they picked it, and is then deleted.
2. Write the goal lines: numbered, each one true or false.
3. Give each task a letter, a size (below) and the goal line it serves.
4. Ready check. Does the team have what these tasks need: a design system when there is a
   screen, code rules, the product docs, a way to run the app and its tests? A gap does not stop
   the sprint: it goes into the STOP 1 message as one line, with what the roles will assume.
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

7. Sort every challenge. However many roles raise it, and however well they argue:
   - It fixes a fault in a spec (wrong, unclear, impossible, cannot be tested, clashes with
     another line) and adds no work beyond the ask: accept it.
   - Its fix adds work, or changes how something behaves today (a new step, a changed rule,
     another role in the task): do not accept it. It becomes an open choice for STOP 1 with the
     small option as your pick, or a line in `LATER.md`.
   - It does no harm to the sprint goal, or has no fix: a line in `LATER.md`.
8. Start `ba` again with the accepted changes and QA's test cases. Specs are written to the
   small option of every open choice. Only the BA writes specs. Its Brief has:

       TASK: update the specs
       SPEC: <the accepted changes and QA's test cases, spec by spec>
       OWNS: <the specs folder>

9. Write `SPRINT.md`.
10. STOP 1. Send the STOP 1 message in the stop shape from SKILL.md: the plan is ready and
    nothing is built; the time, as team time from their yes; at most three open choices, each
    said as what will happen unless they object; what is missing; with tickets, any clash with
    their words and what to change in the tracker; the question. The goal lines and the task
    table stay in `SPRINT.md`.
11. On yes, start the Status with `STOP 1 passed` and the time, and commit the notes and the
    specs. If they pick a bigger option, the BA updates that spec first and the task is resized.

## Two sizes of task

- Normal: the full path.
- Small: about 30 minutes or less at role pace, with nothing new to define. No BA and no
  challenge round. You write it as three lines in the Brief's SPEC (what, where, done means).
  One role builds it and one checks it: QC for a change of look or wording, QA for behaviour.

## BUILD

Per task, in the order `SPRINT.md` gives:

1. Designer first when the task has a screen, then Developer. Developer first when the screen
   cannot run without the new logic. Side by side when they share no files and no single
   resource. Where the screen and the logic meet at a name (a function, an action), put that
   name in both Briefs.
2. A builder that lacks something reports it under MISSING with what it assumed, and keeps
   working. Get the piece while the work goes on.
3. After each Report, update the task's Status in `SPRINT.md`. At the end of a session, replace
   the Status line: what finished, what runs, what waits on whom, what the next one starts with.

## CHECK

1. Per built task, start `qa` and `qc` side by side. Fill in CHANGED. QC gets the builders' Reports.
2. Both say READY: the task is done. When all the tasks of a goal line are done, mark it true.
3. One says NOT READY: send its FINDINGS to the builder who owns those files, then check again.
   Two rounds at most. Still failing: cut the task or park it in `LATER.md`, and say so.

## SHIP

1. Check each goal line.
2. STOP 2. Send the STOP 2 message in the stop shape: the verdict and each goal in plain words;
   with tickets, which tickets passed and what to change in the tracker; what was cut, parked or
   changed beyond the ask; how to see the result; then the question: does it pass?
3. When they have answered, read back `## Ideas to confirm` one by one: keep (move it to
   Confirmed) or drop (delete it). Commit the notes.

## Closing a sprint

- Delete the specs of done tasks. Git keeps them.
- A choice the product lead made that outlives the sprint: one dated line in the project's
  decisions log. With no log, ask once whether to keep such lines under `## Decisions` in the
  project's instructions file, and write there only after that yes.
- Start the Status with `Closed`, and write how long planning and the build really took.
- `SPRINT.md` is replaced by the next sprint's, never added to.
- Then offer refine mode in one line. On yes, follow [REFINE.md](REFINE.md).

## Note shapes

`SPRINT.md`:

    # Sprint <n>: <the goal in one sentence>
    Time box: <minutes of team time, counted from the product lead's yes>
    Tickets: <numbers, only when the work came as tickets: then read TICKETS.md every session>
    Goal lines:
    1. <a line that is true or false>

    | Task | Size | Serves line | Roles | Time | Status |
    |---|---|---|---|---|---|
    | A <title> | normal | 1 | Designer, Developer, QA, QC | 15 min | not started |

    Status: <100 words at most, replaced each session. It starts with `STOP 1 passed` once the
    plan is approved and with `Closed` once the sprint is closed. It ends with what comes next>

`LATER.md`:

    # Later
    ## Ideas to confirm
    - <date> <the idea in one line>

    ## Confirmed
    - <date> <the finding or idea in one line> (<who spotted it>)
