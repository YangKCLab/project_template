# Contributing guidelines

How the team coordinates work in this repository. The [lab manual](https://github.com/YangKCLab/lab-manual/blob/main/docs/research-practices.md) (lab members only) describes the lab-wide setup: a GitHub Project board, a Slack channel, a Google Drive folder, and a running notes document for each project.

## GitHub Issues vs. Slack

### Use GitHub Issues for

- **Task tracking:** anything that needs to get done, such as analysis steps, coding tasks, writing sections, or data preparation.
- **Discussion tied to a task:** questions, updates, blockers, or decisions about a specific task. Comment on the relevant issue.
- **Bug reports or data problems,** for example "classification output has unexpected NaN rows".
- **Requests for review,** for example "please review this codebook change". Link the pull request or file.

Rule of thumb: **if someone might need to find this information next week, it goes on GitHub.**

### Use Slack for

- **Quick questions** that don't need a permanent record, such as "are you free at 3?"
- **Heads-ups,** such as "I'll be offline tomorrow" or "I just pushed a new notebook".
- **Early brainstorming,** before an idea is concrete enough for an issue.
- **Sharing links or articles** for quick reactions.

Rule of thumb: **if it's okay for this message to disappear in a week, Slack is fine.**

### General principles

1. When in doubt, use GitHub. It's easier to find things later.
2. If a Slack conversation produces an action item or a decision, create or update a GitHub issue with the outcome.
3. Tag people on GitHub issues when you need their input. Don't rely on Slack pings for task-related requests.

## Writing issues

After each project meeting, the team turns every TODO item into an issue on the project board. Each issue should be:

- **Specific and actionable,** with clear criteria for when it is done.
- **Assigned** to one or more team members who are responsible for finishing it.
- **Small:** no more than one week of work. Split larger tasks into sub-issues.

## Issue triage

Every open issue gets a **milestone** and a **priority label**.

### Milestones (which phase of work)

TODO: list this project's phases, for example:

- **Data preparation:** data collection, extraction, and enrichment
- **Analysis:** the main analyses
- **Manuscript:** drafts, figures, tables, and references

### Priority labels (when to work on it)

- `now`: actively being worked on, or blocking progress
- `next`: needed soon; queue it up after current work
- `later`: important, but not until a future phase

Re-triage priority labels at the weekly meeting. When a milestone is complete, promote `next` issues to `now` and `later` issues to `next` as appropriate.

## Branches and pull requests

- Do not push to `main`. Create a branch for each piece of work and open a pull request.
- Link the pull request to its issue, for example with "Closes #12" in the description.
- At least one reviewer approves before the pull request is merged.
- Never commit `.env`, API keys, or large or sensitive data files.
