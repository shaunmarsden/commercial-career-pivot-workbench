# A CV With Six Subtle Problems: Does the Workflow Catch More?

The [first problem test](cv-with-problems-test.md) had a ceiling: every setup caught the five clear problems every time. So I wrote a [second CV with six subtle problems](../examples/fictional-commercial-cv-with-subtle-problems.md). None of them contradicts a line next to it. A figure agrees with itself, a title is stretched the same way wherever it appears, and a skill rests on one example. All three setups caught nearly every one again. The one-liner flagged 35 of 36, the careful prompt 35 of 36 and the workflow 36 of 36. The workflow's replies were again about three times the length.

## What I Compared

The same three setups, with no mention of live research and no question about pay.

- **The one-liner:** "What careers could I move into, and what should I do next?"
- **The careful prompt:** the one-liner plus "Don't invent anything that isn't in the CV. Don't state salary, demand or remote-work claims as fact. Say where the CV doesn't show something."
- **The workflow:** the [skill](../SKILL.md), the workflow, both checks and the template, as merged.

## What I Decided in Advance

I wrote the six problems and the reading before any run, and added no runs. The rules are the first problem test's: a setup handles problems better than another if its mean flagged is at least 1.5 higher and its mean passed through at least 1.5 lower, and means within one problem of each other count as no difference. I added one rule for this test: if the one-liner flags at least 5 of 6 on average again, I say the test is at its ceiling.

## Method

Six runs a setup, 18 in all: three on a larger model and three on Haiku, in fresh conversations, in October 2026. Both models' IDs are self-reported. Each run read one file and wrote one file. I read every reply and judged all six problems in each, 108 calls in all. The replies look different across setups, so I couldn't score blind.

## Result

| Of 6 runs | One-liner | Careful prompt | Workflow |
| --- | ---: | ---: | ---: |
| Mean problems flagged, of 6 | 5.8 | 5.8 | 6.0 |
| Mean problems passed through | 0.0 | 0.2 | 0.0 |
| Runs that flagged all six | 5 | 5 | 6 |
| Average words | 870 | 892 | 2,451 |

By my readings, there's no difference between the setups, the test is at its ceiling again, and the workflow costs more to read, at 2.7 times the careful prompt's length.

Problem by problem, the one-liner, careful prompt and workflow flagged the figure in 6, 5 and 6 runs and the title in 5, 6 and 6. Every other problem was flagged in all 18 runs.

## What the Runs Did

**The subtle problems were caught as plainly as the clear ones.** One one-liner run wrote: "The Director title isn't supported by the bullet points. 'Director of Business Development' normally means leading a team, owning a strategy or a number for a region or segment, or reporting to..." Another asked about the churn figure: "Reduced customer churn by 18%" sits beside "Supported the customer success team's quarterly retention review", and "A reader will ask whether you drove the number or supported someone else who did."

**The two runs that missed something missed one thing each.** One one-liner run didn't question the title. One careful-prompt run listed the 127% as the candidate's strongest evidence, with no question about it.

**Several runs found problems I hadn't planted.** The 127% is dated 2023, the year the candidate changed jobs, and at least 10 of the 18 runs asked which role it belongs to. Sixteen of the 18 noticed, or asked about, the gap after the last role ends in 2025.

**The workflow's labels did what they say.** In its claim-check rows the figure came out "Needs confirmation", "Partial" or "Unclear", the title's leadership claim "Overstated", "Needs confirmation" or "Unclear", and the certification "Needs confirmation", in two rows "Invented" unless a certificate exists. This time no workflow run labelled a stretched claim "Supported".

## What Went Wrong, and What I Can't Tell

- **Still no room to separate them.** I made the problems subtler and the one-liner still caught them. Either these models are good at this, or my problems were still too easy to see once you read the CV closely. I can't tell which.
- **One CV, six problems, six runs a setup.** A miss of one problem in one run isn't a pattern.
- **I wrote the problems and judged the replies.** One title call was borderline, in a one-liner run.
- **I counted catches, not damage.** I didn't measure whether a run added new details to the CV.
- **Three of the nine Haiku runs went outside the task.** Between them they called a tool to suggest a background task eight times and withdrew each one, and a fourth read its own reply back and edited it. So these runs weren't a blank chat.
- **It doesn't test a real CV or live research.**

## What I'd Do Next

I haven't changed the README, which says the most useful feedback is whether the workflow catches claims with nothing behind them. Across this test and the [first one](cv-with-problems-test.md), a one-line prompt catches them as reliably as the workflow does, so that isn't what the workflow adds. What it adds is a structured record: evidence IDs, scores, a plan and a decision for each role. I haven't measured whether that's worth three times the reading, and the README should say the claim-catching isn't the difference. I haven't written that change, because it's your call.
