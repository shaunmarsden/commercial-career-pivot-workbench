# A CV With Six Planted Problems: Which Setup Catches Them?

I wanted to know whether the workflow catches problems in a CV that a plain prompt misses. I wrote a [fictional CV with six planted problems](../examples/fictional-commercial-cv-with-problems.md) and gave it to three setups: a one-line prompt, a careful one-paragraph prompt and the full skill. All three caught the five clear problems in every run. The sixth, a stretched job title, split them with no pattern. In two runs the workflow's own claim check labelled that title "Supported". The workflow found nothing the others missed, and its replies were about three times the length.

## What I Compared

Same setups as the [one-prompt comparison](one-prompt-comparison.md), with no mention of live research and no question about pay.

- **The one-liner:** "What careers could I move into, and what should I do next?"
- **The careful prompt:** the one-liner plus "Don't invent anything that isn't in the CV. Don't state salary, demand or remote-work claims as fact. Say where the CV doesn't show something."
- **The workflow:** the [skill](../SKILL.md), the workflow, both checks and the template, as merged.

## What I Decided in Advance

I wrote the six problems, what counts as catching one, and the reading before any run, and added no runs. For each problem in each reply I marked it flagged, passed through or silent, as the [CV's key](../examples/fictional-commercial-cv-with-problems.md) sets out.

- The workflow handles problems better than another setup if its mean problems flagged is at least 1.5 higher and its mean passed through at least 1.5 lower.
- Means within one problem of each other count as no difference.
- It costs more to read if its replies average more than twice the careful prompt's length.

## Method

Six runs a setup, 18 in all: three on a larger model and three on Haiku, in fresh conversations, in October 2026. Both models' IDs are self-reported. Each run read one file and wrote one file. I read every reply and judged all six problems in each, 108 calls in all. The replies look different across setups, so I couldn't score blind.

## Result

| Of 6 runs | One-liner | Careful prompt | Workflow |
| --- | ---: | ---: | ---: |
| Flagged all five clear problems | 6 | 6 | 6 |
| Flagged the stretched title | 4 | 2 | 3 |
| Passed the stretched title through | 2 | 4 | 3 |
| Mean problems flagged, of 6 | 5.7 | 5.3 | 5.5 |
| Mean problems passed through | 0.3 | 0.7 | 0.5 |
| Noticed the unplanned gap after 2024 | 5 | 6 | 4 |
| Average words | 869 | 920 | 2,626 |

By my readings, there's no difference between the setups on either mean, and the workflow costs more to read, at 2.9 times the careful prompt's length.

## What the Runs Did

**The five clear problems didn't separate anything.** The years that don't add up, the 340% with no baseline, the team of 15 beside two other salespeople, the unevidenced modelling skill and the vague AI line were each flagged in all 18 runs. The one-liner said it as plainly as the workflow did: "The years don't add up. The summary says twelve years of experience. The roles listed run from 2017 to 2024, which is about seven years."

**The title was the only close call, and it's arguable.** Four one-liner runs, two careful-prompt runs and three workflow runs said it needed context, such as "Head of Sales at a 20-person start-up and at a 500-person firm are different jobs". The others used the title as plain evidence of seniority. The CV does say the candidate led the commercial function and reported to the founder, which supports a head-of-function title. The stretch is my inference from "worked alongside two other salespeople". So I wouldn't call a pass-through there a clear miss.

**Two workflow runs labelled the title "Supported".** Each wrote a row in the CV claim check saying the leadership line was consistent with the title, and marked it "Supported as written". Both flagged the team size and the 340% in rows beside it. It's the workflow's label doing what it says, on a claim that was only half the problem.

**Most runs noticed a problem I didn't plant.** The dated roles stop in 2024, so there's a gap before today. Fifteen of the 18 mentioned it.

## What Went Wrong, and What I Can't Tell

- **The problems were too easy.** Five of the six are contradictions or missing numbers that anyone reading closely would see. Every setup is already good at that, so the test had no room to show a difference. A ceiling like this says nothing about harder problems.
- **One CV, six problems, six runs a setup.** The title is the only problem that varied, and it's the one I'm least sure about.
- **I wrote the problems and judged the replies.** Three title calls were borderline: two careful-prompt runs and one workflow run.
- **I counted catches, not damage.** I didn't measure whether a run invented new details on top of the CV.
- **Six of the nine Haiku runs went outside the task.** Between them they called a tool to suggest a background task ten times, and withdrew each one. So these runs weren't a blank chat.
- **It doesn't test a real CV or live research.**

## What I'd Do Next

I haven't changed the README, which says its most useful feedback is whether the workflow catches claims with nothing behind them. On this test it catches them as well as a plain prompt does, no better. A fair test needs subtler problems: a plausible figure that is consistent everywhere and has no source, a title that is stretched the same way in every place it appears, and a date that is off by a year. Those don't contradict anything on the page, so a reader has to ask where each came from. I ran that test: see [the subtle problems test](cv-with-subtle-problems-test.md).
