# Tickets

Read this when the product lead names tickets, or the project's instructions name its tracker.

## The ask

- The tracker (such as Jira) says what is wanted. The spec says what was agreed for this sprint.
- The ask is what the named tickets ask for (the description and its acceptance lines, labelled
  or not), plus what the product lead said. A ticket's comments and wishes are not the ask.
- A comment that decides something the ticket's lines do not say is neither followed nor dropped:
  say it in one line at STOP 1 and let the product lead settle it.
- Their words may add something no ticket covers, or take only a part of a ticket for this
  sprint. Neither is a clash: plan what they said. The part they left out is not the ask.
- Where their words and a ticket differ on the same point, the ticket wins. Say the clash in one
  line at STOP 1.
- Work comes only from tickets the product lead names or approves. With none named, the ask is
  their words. If they say to take the next tickets, propose a set that fits the time box and let
  them approve it at STOP 1. A ticket that holds other tickets: ask which they mean.

## Reading them

- Read the named tickets yourself, for scope and size. Put only their numbers in TICKETS,
  never the text: each role reads them itself, and still works from the spec.
- A ticket you cannot open: say you could not read it, never that it does not exist. Plan the
  ones you can read, and ask for the others at STOP 1. If you can read none, ask at once and plan
  nothing. Never plan from a guess.
- A role that says under MISSING that it could not read a ticket: start it again with what that
  ticket asks for in its Brief, and give every later role the same lines.
- Write the ticket numbers on the `Tickets:` line of `SPRINT.md`, so a new session knows.
- A ticket whose ask changed after you showed the plan, before their yes: say what changed in
  one line and ask before you follow it. Until they answer, the plan they approved stands.
- After the yes, a change is not followed: build the approved plan, say the change at STOP 2,
  and do not call that ticket passed.

## The whole board

When the project names its tracker, the team knows the whole board, not only the named tickets.
The board is the project or board the instructions name. If they name none, ask once which one.

- As PLAN begins, never at a bare opening: list the board yourself (number, title, status, the
  full changed stamp). Start `ba` with the TASK `read the board`, the notes folder under OWNS
  and, in SPEC, the numbers to read. It reads those in full and keeps `BOARD.md` there.
- The first time, SPEC holds every number. Later, the new tickets and those whose changed stamp
  moved. A board too big for one run is read in parts, one BA after another, until none is left.
  Then count: `BOARD.md` has one line for every ticket on your list.
- List the board again before STOP 1, at the yes, before STOP 2 and when a session resumes a
  sprint. Never skip one to save time or cost. Never run the board BA beside QA and QC.
- Read `BOARD.md` once a session. After that, take the BA's Report: what moved, and new clashes.
- Reading the board never starts work. A sprint ticket whose ask changed is handled as above.
  A status move or a comment that changes no ask is not said.
- Anything else new goes into the next stop message under `New on the board`, three lines at
  most, the ones that touch this sprint first. One already said is not said again: keep the
  stamp of the last board you told them about in the Status.
- A clash between tickets that touches this sprint is one line at STOP 1.

## Nobody writes to the tracker

You included. What should change there (a status, a wording, a new bug) is a list in each stop
message, three lines at most: the ones that matter most. The product lead makes the change.

## When a ticket and the spec differ

A role that sees a requirement or acceptance line say what the spec does not sends a `DIFFERS:`
line and keeps working from the spec.

- In the challenge round: where the spec misses or contradicts a line of the ask, accept it,
  since the ticket wins. Sort any other like a challenge.
- After STOP 1, build nothing from one. Note it in the Status of `SPRINT.md`, so a new session
  still has it, and say it in one line at the next stop. One already said is not said again.
- A ticket with an open `DIFFERS:` line, one the product lead has not settled yet,
  is not said to have passed.
