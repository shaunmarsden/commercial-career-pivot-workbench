# Does Acting on the Workflow's Reply Go Better? A Reader Test

The workflow's reply is about three times as long as a plain prompt's reply. I'd said its gain is a structured record, and that I hadn't measured whether the structure helps. I tried. I gave 24 fresh readers a fictional CV and, for 18 of them, an AI's reply about it, and asked each to act on it. The test couldn't show a benefit. All 24 readers, including the six who had no reply at all, left the unsupported claims out of their CV summary and named the problems to check. The one claim that got through was "a team of 15". It reached 2 of 6 summaries with no reply, 0 of 6 with a one-line prompt's reply, 4 of 6 with a careful prompt's reply and 1 of 6 with the workflow's.

## What I Did

The readers got the [fictional CV with six planted problems](../examples/fictional-commercial-cv-with-problems.md) and one of four things:

- **No reply:** the CV only.
- **A one-line prompt's reply**, from the [problem test](cv-with-problems-test.md)'s rerun without the cue.
- **A careful prompt's reply**, from the same rerun.
- **The workflow's reply**, from the same rerun.

Every reader got the same task. "You are the candidate. You have no information beyond the CV and, if there is one, the reply, and you can't check anything." They name the role they'd test first, write three sentences for the top of their CV "using only what you are willing to defend", and list what they'd confirm or check before sending it.

## What I Decided in Advance

I wrote the measures and readings before any run, and added no runs.

- **Carried:** how many of five unsupported details appear in the three-sentence summary as plain claims: "twelve years", "340%", "team of 15", "advanced financial modelling", "AI initiatives". Restating safely, such as seven years or "grew revenue" with no figure, doesn't count.
- **Listed:** how many of the planted problems the reader names in the check list.
- **Words:** the length of the reply the reader was given.
- A reply helps if its group's mean carried is at least 1 lower than the no-reply group's. The workflow's structure helps beyond a careful prompt's reply if its mean carried is at least 1 lower, or its mean listed at least 1 higher. Means within 1 of each other count as no difference.

## Method

24 readers in four groups of six, three on a larger model and three on Haiku in each, in fresh conversations, in October 2026. Both models' IDs are self-reported. Each read one file and wrote one file. I read every answer. The replies look different across groups, so I couldn't score blind.

## Result

| Of 6 readers | No reply | One-liner reply | Careful reply | Workflow reply |
| --- | ---: | ---: | ---: | ---: |
| Carried "a team of 15" into the summary | 2 | 0 | 4 | 1 |
| Carried any of the other four details | 0 | 0 | 0 | 0 |
| Named the five checkable problems | 6 | 6 | 6 | 6 |
| Average words in the reply they read | 0 | 874 | 923 | 2,646 |

By my readings, there's no difference between any two groups, because no group's mean carried differs from another's by 1, and every reader listed everything. As a test I hadn't set in advance, the one-liner's 0 of 6 against the careful prompt's 4 of 6 gives p = 0.03, and the workflow's 1 of 6 against the careful prompt's 4 of 6 gives p = 0.12, one-tailed, by an exact test. I wouldn't lean on either, with six readers a group.

## What the Readers Did

**Every reader did the checking themselves.** One reader with no reply wrote: "The 'twelve years' summary line. The dates run from 2017 to 2024, which is about seven years. I will correct the line, or add earlier experience with dates." The same reader, on the 340%: "The 340% revenue growth. I need the starting revenue, the end revenue, the period, and whether it was company revenue or something I can own. Until then it stays off the CV."

**The team of 15 was the exception.** Eight of the 24 summaries mentioned a team. Seven gave the number 15 and one wrote "managed a team". Five of the seven had read a reply and two had not, and I can't say why a reader who had been told to defend only what they could would still use the number.

**One reader argued with the reply.** They wrote: "One point in the adviser's reply is wrong for my constraints. It says Senior Account Executive 'does not involve stepping down'. It does."

## What Went Wrong, and What I Can't Tell

- **My task did the checking for them.** I asked readers to use "only what you are willing to defend" and to list what they'd "confirm or check". That tells a reader to look for problems, which is the same kind of cue that spoiled my first problem tests. It's why readers with no reply did as well. The test can't show what a reply adds, because the instructions already add it.
- **Readers are language models.** It says nothing about how much effort a person spends reading three times as much, which is the cost I wanted to weigh.
- **One CV, six readers a group.** Four of six against none isn't a difference I can lean on.
- **I judged every answer.** Whether a sentence "carries" a claim was my call, and one reader's "managed a team" with no number I counted as not carried.
- **One Haiku reader went outside the task.** It called a tool to suggest a background task and withdrew it.

## What I'd Do Next

I haven't changed the README beyond one sentence saying I tried. A fair version of this test would give readers the task without the cue, for example "Write the three sentences for the top of your CV for the role you'd test first", and nothing about checking or defending, so that what carries into the summary depends on what the reply told them. I haven't run it.
