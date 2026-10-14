# Commercial Career Pivot Workbench

AI can suggest 15 possible jobs from a CV in seconds. That doesn't mean all 15 are realistic, in demand or worth going after.

This is a workflow for sales and commercial people looking at a nearby role or a bigger career change. It checks the evidence at each step. It turns a CV into a shortlist of possible roles, shows what evidence supports each one, and separates useful ideas from claims you still need to check against the current job market.

> AI generates and organises possibilities. The person checks the evidence and decides what to pursue.

## Start Here

| If you want to... | Open this |
| --- | --- |
| Run the whole method | [Career Pivot Workflow](workflow/career-pivot-workflow.md) |
| Capture your evidence | [Career Evidence Map](templates/career-evidence-map.md) |
| Check the CV hasn't been exaggerated | [CV Claim Check](checks/cv-claim-check.md) |
| Check salary and hiring claims | [Market Claim Check](checks/market-claim-check.md) |
| See a worked example with no real data | [Fictional Commercial CV](examples/fictional-commercial-cv.md) and [Fictional Pivot Output](examples/fictional-pivot-output.md) |
| Run it with an AI assistant | [Reusable Skill](SKILL.md) |
| See how the skill was checked | [Skill Check](evaluations/skill-check.md) |
| See whether the workflow beats one prompt | [One Prompt or the Workflow](evaluations/one-prompt-comparison.md) |
| See whether it catches problems in a CV | [A CV With Six Planted Problems](evaluations/cv-with-problems-test.md) |
| See the same test with subtler problems | [A CV With Six Subtle Problems](evaluations/cv-with-subtle-problems-test.md) |

## What It Produces

- A long list of possible roles, including nearby ones
- A shortlist of up to five roles, scored on five dimensions, not on how confident the wording sounds
- A map from each role requirement to experience you've already shown
- Clear gaps, with each role requirement marked supported, partly supported, not supported or unclear
- A list of salary and demand claims that still need checking against current sources
- A small 30-day plan to test the strongest options

## The Workflow

Before you start, remove personal, customer and employer details you don't need.

1. Build the evidence map: turn the CV into an evidence map, without rewriting it yet.
2. Generate role hypotheses: suggest possible roles and explain why each might fit.
3. Create a shortlist: choose no more than five roles and score them.
4. Compare with real roles: check the best ones against current job descriptions.
5. Verify market claims: check demand, salary and location claims against current sources.
6. Design small tests: choose small actions that give you better evidence before a big decision.
7. Make the decision: the person chooses to pursue, test first, build towards, park or reject each role.

## What This Is Not

- A guarantee that someone qualifies for a role
- A source of live salary or hiring data
- A replacement for reading current job descriptions
- A reason to invent achievements, seniority or industry experience
- A place to upload or publish a real CV
- Automated job applications or unsolicited messages

## Safe Use

Use an AI tool your organisation allows. Remove contact details and any customer, employer or confidential information the task doesn't need. Keep real CVs and completed evidence maps private.

Everything under `examples/` is fictional. The repository has no real candidate, employer, customer or contact data.

## Status

This is a first working version. The method and worked example show the process, not whether it leads to a job.

I've tested it against just asking an AI, on fictional CVs. The results are on the evaluation pages, and they're plainer than I expected:

- **Pay and demand claims.** A careful one-paragraph prompt gave no unsourced pay or demand figures, and neither did the workflow. A bare one-line prompt gave pay figures when I asked for them, labelled as unchecked estimates. See [One Prompt or the Workflow](evaluations/one-prompt-comparison.md).
- **Problems planted in a CV.** Across two fictional CVs with six planted problems each, a one-line prompt flagged 61 of 72, a careful prompt 67 and the workflow 68. The careful prompt did as well as the workflow. See [the clear problems](evaluations/cv-with-problems-test.md) and [the subtle ones](evaluations/cv-with-subtle-problems-test.md). My first runs told the AI the CV was a test, so I reran them without that, and these are the rerun numbers.
- **One thing the workflow did better.** When a CV listed a skill with no example, it flagged the skill every time. The other setups sometimes wrote it up as experience.
- **The cost.** Its replies ran to about three times the length of the others.

So the workflow's gain isn't that it catches claims a plain prompt misses. It gives you a structured record: evidence IDs, scores, a plan and a decision for each role. I haven't measured whether that's worth the extra reading. The most useful feedback is whether that structure makes your choices clearer.
