# Does the Skill Do What Its Steps Say? A Twelve-Run Check

I changed [the skill](../SKILL.md) and wanted to know whether an AI that loads it does what the steps say. I ran it six times on the fictional CV, found two loose ends, fixed them, and ran it six more times. The small-tests step appeared in every run. No run made a pay or demand claim, and the market-evidence score stayed blank every time. After the two edits, Interest was scored the same way in all six runs and the plan was four weekly steps in all six.

## What I Checked

Each run was told to follow the skill on the [fictional CV](../examples/fictional-commercial-cv.md), with "no live research is available". The inputs were the skill, the workflow, both checks and the evidence-map template. I left out the worked example's output, so a run couldn't copy it.

I wrote five checks before any run:

- **Small tests:** a plan of small tests over 30 days.
- **Market blank:** no number in the market-evidence column.
- **No market claims:** no salary, hiring-demand or remote-work claim stated as fact.
- **No invented CV facts:** no achievement, figure or responsibility that isn't in the CV.
- **Shape:** no more than five roles shortlisted, five scores visible, and a decision for each.

The first round's rule: a step works if its check holds in at least 5 of 6 runs. I added no runs.

## Method

Each round was six runs: three on a larger model and three on Haiku, in fresh conversations, in October 2026. Both models' IDs are self-reported. Each run read one file and wrote one file. I read the evidence maps, shortlists, test plans, decisions and CV claim checks in all twelve, and not every line of the role hypotheses. Nothing here is scripted.

## Round One: The Skill as It Was

| Check | Runs, of 6 |
| --- | ---: |
| A small-tests plan over 30 days | 6 |
| That plan has two or three tests | 4 |
| Market-evidence score left blank | 6 |
| No salary, demand or remote-work claim | 6 |
| Interest scored 1, not left to the user | 3 |

- **The step appeared every time, but the count slipped.** The skill said "two or three small tests". Two runs, one on each model, laid out four weekly actions, as the worked example does. By my line that's 4 of 6, so it fell short.
- **Interest split.** Three runs scored it 1 as a placeholder. Three left it for the user. The workflow was silent, and I'd set that unclear shape in three or more runs would mean the steps were ambiguous.

## What I Changed

Two small edits, made after seeing round one:

- Workflow step 3 now says: if the CV doesn't say what you'd enjoy, score Interest 1, which means uncertain, say it's a placeholder, and don't leave it blank or guess higher.
- Skill step 8 now says to design a four-week plan of small tests, one step a week, covering two or three of the shortlisted roles.

## Round Two: After the Edits

| Check | Round one | Round two |
| --- | ---: | ---: |
| Interest scored 1 and called a placeholder | 3 of 6 | 6 of 6 |
| Four weekly steps covering two or three roles | 4 of 6 | 6 of 6 |
| Market-evidence score left blank | 6 | 6 |
| No salary, demand or remote-work claim | 6 | 6 |

Both edits work by the rule I set, and neither broke the checks that held before. The market-evidence column was left blank, or marked "not yet scored", in all twelve runs. Every run marked salary, demand and hybrid availability "not yet verified" and gave a checklist for collecting listings.

## What Went Wrong, and What I Can't Tell

- **Round two was a response to round one.** I wrote the edits after seeing the problem, so it shows the edits fix what I saw. It doesn't show they'd survive a different CV.
- **"Informal" crept in.** The CV says "coached two new account managers". Six of the twelve runs called the coaching informal, once as "informal leadership". It's a safe direction, since it makes the claim smaller, but the CV doesn't say it. I found no invented achievement, figure or responsibility.
- **Some role descriptions were stated as likely.** Runs said things like "may be advertised at a junior level" or "not entry level". My rule covered salary, demand and remote work, so I didn't count them. They're market claims in spirit, and they were hedged.
- **One Haiku run went outside the task.** In round one it called a tool to suggest a background task, then withdrew it, so these runs aren't a blank chat.
- **One fictional CV, six runs a round, a key I wrote and read myself.** The scores a run chose for Gap size and Practical fit varied, and I didn't judge them.
- **It doesn't test live research.** Every run had none.

## What the Repository Does Now

The workflow and the skill carry both edits. The worked example scores Interest 1 for the same reason.
