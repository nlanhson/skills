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

The team keeps two notes in your project, `SPRINT.md` and `LATER.md`. They go in the folder your
project's instructions name, or in `docs/`.

Each role runs on Opus. A sprint of three small tasks takes about fifteen helper runs.

## Remove

Delete the link `~/.claude/skills/orchestrator`, and the links `ba.md`, `designer.md`,
`developer.md`, `qa.md` and `qc.md` in `~/.claude/agents`.

## Status

First version. It has run full sprints on small practice projects. A wider review step between
sprints is planned.

## Licence

MIT. See `LICENSE`.
