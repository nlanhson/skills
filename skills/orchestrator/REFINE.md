# Refine mode

Between sprints the team looks wide, on purpose. Build mode can stay narrow because this exists.
Refine runs when the product lead says yes to your offer after a sprint closes, or asks for it.
It changes no code. It ends with the refine message, then the lessons.

## 1. Explore

Start `qa` and `qc` side by side on the whole product, not on the last sprint's tasks:

    SPRINT GOAL: none, this is refine mode
    TASK: explore
    SPEC: the whole product as it runs today. <what it is for, in one line>
    OWNS: nothing
    TIME: 15
    DONE MEANS: up to eight FINDINGS, worst first, none of them already in LATER.md. QA finds
    them by using the product, QC by comparing it with the standard. No file changed.

## 2. The council

For one question too big for a single role. Only a question the product lead asks, or one you
propose and they say yes to. One per refine. No such question: skip this step.

1. Answers. Start all five roles side by side, each on its own:

       SPRINT GOAL: none, this is refine mode
       TASK: council
       SPEC: <the question, and the two or three facts needed to answer it>
       OWNS: nothing
       TIME: 5
       DONE MEANS: one line group in your Report, above LATER. `ANSWER: <your answer, from your
       own role's goal, in six lines at most, with its strongest reason and its biggest risk>`.
       No file changed.

2. Reviews. Take the names off the five answers, shuffle them and number them 1 to 5. Send all
   five back to each role:

       SPRINT GOAL: none, this is refine mode
       TASK: council review
       SPEC: <the question, then answers 1 to 5>
       OWNS: nothing
       TIME: 5
       DONE MEANS: three lines in your Report, above LATER. `BEST: <number> because <one line>`.
       `WEAKEST: <number> because <one line>`. `MISSED: <what all five overlooked>`. No file
       changed.

3. Sum up yourself: where they agree, where they split and why, what all of them missed, and
   your own recommendation. The product lead decides. A council never decides.

## 3. Sort LATER.md

- Add the explore findings. Merge lines that say the same thing. A line stays one sentence.
- Delete lines that are fixed, no longer true, or three sprints old and never picked.
- A line the product lead added or kept is never deleted without asking.
- Twenty lines at most. If more remain, the weakest go. Git keeps them.
- Put the five that would help the product's users most at the top, the most valuable first.

## 4. Look back

From this sprint's own record (fix rounds, MISSING lines, cut tasks, the product lead's
corrections, estimates against real time), draw three lessons at most. A lesson is one rule with
its reason, and it traces back to something that happened. Never add one because it sounds like
good practice.

- A lesson about this product goes into the project's instructions file, the one every role
  already reads, under `## Team lessons`. Write it only after the product lead says yes.
- A lesson about how a role works on any project: tell the product lead which role it belongs
  to. You do not edit role files.

## 5. The refine message

One message in the stop shape from SKILL.md, in this order and nothing more:

1. One sentence: refine is done, and nothing in the product changed.
2. If the council sat, three sentences: what most chose, who disagreed and why, your pick.
3. The top five lines of `LATER.md` as a numbered list, each in a few plain words. The new
   findings are in it, so they need no paragraph of their own.
4. The question: which of these go into the next sprint?

When they have answered, propose the lessons in a message of their own, with one question: add
them? Then PLAN starts from their sprint answer.
