# Skills

An AI product team for Claude Code.

You talk to one lead, the orchestrator. It runs a team of five roles that takes work from idea to
shipped, in sprints with a fixed scope. You step in twice per sprint: to approve the plan, and to
review what shipped.

## The team

- **Orchestrator:** the lead. It plans, hands out work and checks results. It builds nothing itself.
- **BA:** writes what to build and what done means.
- **Designer:** owns the look.
- **Developer:** owns how it works.
- **QA:** the tester. It uses the result and tries to break it.
- **QC:** the inspector. It compares the result with your project's standard.

## How a sprint runs

1. **Plan.** You say what you want. The BA writes short specs, the others push back once, and you
   approve.
2. **Build.** The Designer and the Developer work only on the sprint's tasks. Anything else they
   spot goes on a list for later.
3. **Check.** QA and QC check each task. A task that fails goes back to its builder.
4. **Ship.** The orchestrator reports, and you review.

An idea you mention in the middle of a sprint is noted, not built. At the end you decide whether
to keep it.

When your project keeps its requirements in a tracker such as Jira, name the tickets and the team
reads them. The tracker says what is wanted. The spec says what was agreed for this sprint, and
the team builds and tests from the spec. Where a ticket and the spec disagree, you are told. The
team never writes to the tracker: what should change there comes to you as a short list.

When your project's instructions name the tracker, the team also reads the whole board. The BA
reads every ticket in full and keeps a note of it, `BOARD.md`, with your project's other notes:
a line per ticket, then the clashes it found. The board is read again at each stop, and you are
told what is new. Reading never starts work: the team builds only what you name or approve.

To lock the tracker, deny its write tools in your project's own `.claude/settings.json`. The rule
holds for the roles too. Use the tool names your session shows under `/mcp`:

    { "permissions": { "deny": ["mcp__<server>__<write tool>"] } }

Between sprints you can run a refine pass. It is the one time the team looks wide: QA and QC go
over the whole product, the list for later is sorted and cut to twenty lines, and the team
proposes what it learned as rules for your project. For one big question, the five roles sit as
a council: each answers alone, they review each other's answers without names, and the
orchestrator sums up. You decide.

The orchestrator writes to you like a colleague in a chat: short, plain, and only when something
has changed or it needs your answer.

## Install

    git clone https://github.com/nlanhson/skills.git
    cd skills
    ./install

This links the skill and the five roles into `~/.claude`. Anything already there under the same
name is moved to `~/.claude/backups` first. To update, run `git pull`.

To try it in one project only, without touching your own setup:

    CLAUDE_CONFIG_DIR=/path/to/your/project/.claude ./install --trial

The command is then `/orchestrator-next`, and it exists in that project only.

## Use

Open Claude Code in your project, type `/orchestrator`, and say what you want from the sprint.

The team keeps two notes in your project, `SPRINT.md` and `LATER.md`, plus short specs while a
sprint runs. They go in the folder your project's instructions name, or in `docs/`. It commits
its work locally and never pushes. With your yes, it adds what it learned and what you decided
to your project's instructions file.

Each role runs on Opus. A sprint of three small tasks takes about fifteen helper runs, and a
refine pass with a council about twelve more.

## Remove

Delete the link `~/.claude/skills/orchestrator`, and the links `ba.md`, `designer.md`,
`developer.md`, `qa.md` and `qc.md` in `~/.claude/agents`.

## Status

Second version. It has run full sprints and refine passes on small practice projects.

## Licence

MIT. See `LICENSE`.
