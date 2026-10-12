# One Prompt or the Workflow? An Eighteen-Run Comparison

The README says this workflow checks the evidence at each step and separates useful ideas from claims you still need to check. I wanted to know whether that beats just asking an AI. I gave the same fictional CV to three setups: a one-line prompt, a careful one-paragraph prompt, and the full skill. I counted pay and demand claims stated as fact, and details added to the CV. On this CV the workflow gained nothing on either count, and its replies were three times as long.

## What I Compared

Every run got the [fictional CV](../examples/fictional-commercial-cv.md) and was told no live research was available.

- **The one-liner:** "What careers could I move into, and what should I do next?"
- **The careful prompt:** the one-liner plus "Don't invent anything that isn't in the CV. Don't state salary, demand or remote-work claims as fact. Say where the CV doesn't show something."
- **The workflow:** the [skill](../SKILL.md), the workflow, both checks and the template, as merged. The worked example's output was left out.

## What I Decided in Advance

I wrote four measures and the readings before any run, and added no runs after.

- **Market claim run:** states, as fact and with no "check it" label, a pay figure, a hiring-demand statement, whether roles are hybrid or remote, or how hard a role is to get into. Hedged and labelled claims don't count, and neither does a claim about what a role does.
- **CV claim run:** states or suggests an achievement, figure, responsibility, seniority or skill that isn't in the CV.
- **Gaps shown:** every suggested role has a stated gap.
- **Words:** the length of the reply.

The readings:

- The workflow cuts unsupported market claims if the one-liner has them in at least 4 of 6 runs and the workflow in at most 1 of 6. The same line applies to CV claims.
- It adds something beyond a careful prompt only if the careful prompt is at least 4 of 6 and the workflow at most 1 of 6.
- It costs more to read if its average length is more than twice the careful prompt's.

## Method

Six runs a setup, 18 in all: three on a larger model and three on Haiku, in fresh conversations, in October 2026. Both models' IDs are self-reported. Each run read one file and wrote one file. I judged every reply by reading it, and a script only found candidate lines. The replies look different across setups, so I couldn't score blind.

## Result

| Of 6 runs | One-liner | Careful prompt | Workflow |
| --- | ---: | ---: | ---: |
| Market claim stated as fact | 2 (3 if borderline counts) | 0 | 0 |
| A detail added to the CV | 1 | 0 | 2 |
| Every suggested role has a stated gap | 4 | 6 | 6 |
| Average words | 818 | 853 | 2,541 |

By my readings:

- **The workflow didn't cut market claims.** The one-liner had them in 2 of 6 runs, short of my 4. Two against none is p = 0.23, one-tailed, by an exact test.
- **It didn't cut CV claims.** The one-liner had one and the workflow had two, the wrong way round.
- **It added nothing beyond a careful prompt.** The careful prompt had neither problem.
- **It cost more to read.** The workflow's replies ran to three times the careful prompt's length.

## What the Runs Did

**The market claims were small.** Two one-liner runs wrote "often hybrid" and "usually hybrid" about a role. A third wrote that "most employers will want" people-management experience, which I count as borderline. Every other run, in every setup, said it had no market data and pointed to job adverts.

**The CV details were small too.** A one-liner run wrote "senior stakeholder work", where the CV says operational and commercial stakeholders. A workflow run put the same phrase in a skill column. Another workflow run described the account executive's work as "new-business selling", where the CV doesn't say what kind of selling it was. A different run noted that gap.

**The one-liner missed gaps.** Two of its six runs left at least one role with no stated gap. The careful prompt and the workflow stated one for every role, in all twelve runs.

**Four one-liner runs called the coaching "informal".** The CV says "coached". No careful-prompt or workflow run did. In the two earlier rounds of the [skill check](skill-check.md), six workflow runs did, so this isn't a clean difference.

## What Went Wrong, and What I Can't Tell

- **The CV tells the AI to be careful.** It ends with an "Important Unknowns" section that says no salary requirement and no market research were supplied. With that and the "no live research" line, even the one-liner was cautious. This is the main limit. It's a test of whether the workflow adds care when the AI is already prompted to be careful.
- **I measured two things.** The workflow also produces evidence IDs, scores, a plan and decisions, and I didn't score those.
- **Six runs a setup.** Two against none isn't a difference I can lean on.
- **Borderline calls were mine.** Counting "most employers will want that" as a market claim moves the one-liner from 2 to 3.
- **Four of the nine Haiku runs went outside the task.** Three called a tool to suggest a background task and withdrew it, one of them twice, and one made a failed browser call. So these runs weren't a blank chat.
- **One fictional CV, a key I wrote.** It says nothing about a real CV, and it doesn't test live research, where enrichment tools go wrong.

## What I'd Do Next

I haven't changed the README. It still says the workflow checks the evidence at each step, and this test didn't show that it does more than a careful prompt on a CV that already carries the cautions. The fair next test removes them: a CV with no "Important Unknowns" section, and no "no live research" line in the prompt. That's where an AI is tempted to fill the gaps, and where the guardrails would show.
