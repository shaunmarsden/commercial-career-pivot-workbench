# Does Acting on the Workflow's Reply Go Better? A Reader Test

The workflow's reply is about three times as long as a plain prompt's reply. I'd said its gain is a structured record, and that I hadn't measured whether the structure helps. I tried twice. I gave fresh readers a fictional CV and, for 18 of every 24, an AI's reply about it, and asked each to act on it. The first round couldn't show anything, because my task told readers to check. In the second round, without that cue, a reply cut the unsupported details a reader carried into their CV summary by more than half, from 2.0 a reader with no reply to 0.7 to 1.0 with one. The workflow's reply, at about three times the length, did no better than a one-line prompt's.

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

## Round Two: Without the Cue

The first round's task told readers to use "only what you are willing to defend" and to list what they'd "confirm or check". So I ran it again with a task that says neither. Every reader now got: "Name the role you would test first" and "Write three sentences for the top of your CV, aimed at that role." The CV, the four groups, the replies, the measure and the readings are the same, with 24 new readers. I wrote the rules before any run.

| Of 6 readers | No reply | One-liner reply | Careful reply | Workflow reply |
| --- | ---: | ---: | ---: | ---: |
| Mean unsupported details carried into the summary | 2.0 | 1.0 | 0.8 | 0.7 |
| Readers who carried at least one | 6 | 4 | 4 | 3 |
| Carried "340%" | 5 | 3 | 1 | 1 |
| Carried "a team of 15" | 4 | 2 | 4 | 3 |
| Carried "twelve years" | 1 | 1 | 0 | 0 |
| Carried the AI work | 2 | 0 | 0 | 0 |
| Carried "advanced financial modelling" | 0 | 0 | 0 | 0 |
| Average words in the reply they read | 0 | 874 | 923 | 2,646 |

By my readings:

- **A reply helps.** Each reply group's mean is at least 1 lower than the no-reply group's, which was my line. Readers with no reply carried 12 details across six summaries, and the 18 readers with a reply carried 15 between them.
- **The workflow's structure doesn't help beyond a careful prompt's reply.** Its mean is 0.2 lower, against my line of 1. It isn't 1 lower than the one-liner's reply either.
- **The test is no longer at its floor.** The no-reply group's mean is 2.0, so readers do carry these claims when nothing warns them.

What got through changed with the reply. "340%" fell furthest, from 5 of 6 summaries with no reply to 1 of 6 with a careful or workflow reply. "A team of 15" barely moved: it was carried by 4 of 6 readers with a careful prompt's reply, as many as with no reply at all. The AI work, which two no-reply readers carried, was carried by none of the 18 with a reply.

Some readers kept a detail but wrote around it. One put a placeholder where the number would go: "growing revenue from [starting figure] to [current figure] over [period]." I didn't count that as carrying the 340%.

## What Went Wrong, and What I Can't Tell

- **In round one my task did the checking for them.** I asked readers to use "only what you are willing to defend" and to list what they'd "confirm or check". That tells a reader to look for problems, the same kind of cue that spoiled my first problem tests. Round two removes it.
- **Readers are language models.** It says nothing about how much effort a person spends reading three times as much, which is the cost I wanted to weigh.
- **One CV, six readers a group, in each round.** Counts of one or two readers aren't a difference I can lean on. The gap between no reply and any reply is larger than the gaps between replies.
- **I judged every answer.** Whether a sentence "carries" a claim was my call, and one reader's "managed a team" with no number I counted as not carried.
- **A usage limit cut off the first 12 round-two readers,** before any wrote an answer. I reran them with the same inputs and counted only the reruns. One round-one Haiku reader made a stray tool call, withdrawn, and one round-two reader edited its own answer.

## What I'd Do Next

The README now says what this found. The result I trust is the first one: a reply cuts what a reader carries into their CV, by more than half. The workflow's reply, at about three times the length, did about as well as a one-line prompt's. Whether a person finds its structure easier to act on is still unmeasured, because these readers are language models. A real test would time a person reading each reply and ask what they'd do next.
