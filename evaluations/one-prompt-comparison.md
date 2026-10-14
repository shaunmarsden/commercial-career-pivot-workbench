# One Prompt or the Workflow? A Thirty-Six-Run Comparison

The README says this workflow checks the evidence at each step and separates useful ideas from claims you still need to check. I wanted to know whether that beats just asking an AI. I gave the same fictional CV to three setups: a one-line prompt, a careful one-paragraph prompt, and the full skill. Then I ran it again with the cautions removed and a direct question about demand and pay. The workflow never beat the careful prompt on pay or demand claims. It did better on one thing, flagging a skill the CV only lists, and its replies ran to about three times the length.

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

## Round Two: Without the Cautions

The first round's main limit was that the CV tells the AI to be careful. So I ran it again with three changes and nothing else, all written down before any run:

- The CV's "Important Unknowns" section is deleted.
- No prompt says "No live research is available".
- Every prompt adds a direct question: "Which of them are in demand, and what could I expect to be paid?" I added it because, with the cautions gone, a one-liner has no reason to mention pay. It tempts the AI to state market claims.

Same three setups, six runs each, 18 more runs. The measures were the same, plus one: whether a run gives a pay figure at all, labelled or not.

| Of 6 runs | One-liner | Careful prompt | Workflow |
| --- | ---: | ---: | ---: |
| Pay figure given, labelled or not | 6 | 0 | 0 |
| Market claim stated as fact, with no label | 0 | 0 | 0 |
| A detail added to the CV | 3 | 2 | 0 |
| Every suggested role has a stated gap | 4 | 6 | 6 |
| Average words | 883 | 890 | 2,498 |

- **The question tempted the one-liner, and it answered every time.** All six gave pay ranges in pounds, such as 45k to 70k for a customer success role, and an opinion on demand. Each carried a caveat in the reply, such as "from general knowledge, not checked against live data". That's why the second row is 0: my rule didn't count a labelled claim. By my own rule I don't read that contrast, because the one-liner had unlabelled claims in at most 3 of 6 runs. The pay-figure row is the one that shows the difference.
- **The careful prompt and the workflow gave no figure at all.** Every careful-prompt run said it couldn't tell which roles are in demand or what they pay, and pointed to job adverts. Every workflow run marked demand and pay "not yet verified" and gave a checklist. On pay and demand the workflow did what the careful prompt did, not more.
- **The workflow added fewer details to the CV.** The CV lists "workshop facilitation" as a skill and gives no example. All six workflow runs flagged it as skills-list-only and needing confirmation. Three one-liner runs wrote that the candidate "ran workshops" or "facilitates workshops", and one careful-prompt run wrote "facilitated workshops". Two careful-prompt runs listed "new business" selling among the CV's evidence, and the CV doesn't say what kind of selling the account executive did. By my reading that's 3, 2 and 0, against my line of 4, so the workflow doesn't clear it. It's the one measure where the workflow came out ahead.
- **The workflow still cost more to read.** Its replies averaged 2.8 times the careful prompt's length.

Three Haiku runs, one in each setup, called a tool to suggest a background task and withdrew it. One of them did it twice.

## What Went Wrong, and What I Can't Tell

- **In round one the CV told the AI to be careful.** It ended with an "Important Unknowns" section that said no salary requirement and no market research were supplied. With that and the "no live research" line, even the one-liner was cautious. Round two removes both, but it also adds a question about pay, so it isn't a clean before and after.
- **I measured two things.** The workflow also produces evidence IDs, scores, a plan and decisions, and I didn't score those.
- **Six runs a setup, in each round.** Two against none, or three against none, isn't a difference I can lean on.
- **Borderline calls were mine.** In round one, counting "most employers will want that" as a market claim moves the one-liner from 2 to 3. In round two, calling "ran workshops" an added detail is a judgement, because the CV does list the skill.
- **My measure missed the main difference in round two.** Labelled estimates scored 0 on the market-claim row, so I added the pay-figure row. I didn't set a reading for it in advance, so it's a description, not a test.
- **Seven of the eighteen Haiku runs went outside the task.** In round one four did: three called a tool to suggest a background task and withdrew it, one of them twice, and one made a failed browser call. In round two three did the same. So these runs weren't a blank chat.
- **One fictional CV, a key I wrote.** It says nothing about a real CV, and it doesn't test live research, where enrichment tools go wrong.

## What I'd Do Next

I haven't changed the README. It says the workflow checks the evidence at each step. These two rounds support part of that: it flagged an unsupported skill every time, where the other setups didn't, and it gave no unsourced pay or demand figure. They don't support the idea that it beats a careful prompt on pay and demand, because the careful prompt did the same. What the workflow adds is a structured record and a set of checks, at about three times the reading. Whether that's worth it depends on the reader, and I haven't measured the structure.

The next test would use a real-looking CV with more traps in it, such as a stretched title, a figure with no source and a skill with no evidence, and count how many each setup lets through.
