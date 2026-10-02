# Program Tracker Template

A small starter kit I put together for tracking a program or project with plain GitHub or GitLab issues. It has issue
templates, a RAID log, a dependency register, a weekly status template, a program charter template, a decision log
template and a Markdown lint check.

Everything in it is made-up sample content. The names, dates and statuses are fictional, and none of it comes from real
client, employer or team work.

I made this to practise keeping a program visible in writing, without needing any special tooling. It's a starting
point, not a method you have to follow.

## How I'd use it

Copy the files you want into a new repo or project. If you're on GitHub, keep `.github/ISSUE_TEMPLATE/` and delete
`.gitlab/`. If you're on GitLab, do the opposite. Then create the labels below, fill in the charter at kick-off, and
post a status issue each week. The RAID log and dependency register are CSV files so they open in any spreadsheet, and
there's a Markdown version of the RAID log too. Open a retrospective issue at each milestone.

The templates are in `templates/` and the filled-in fictional examples are in `examples/`. The decision log is just a
table for noting what was decided, by whom and why.

## Labels

On GitLab I use scoped labels with `::`, like `status::in-progress`. On GitHub the templates expect `type: ...` style
names, so rename them if you prefer. The set I use is:

- status: `backlog`, `in-progress`, `at-risk`, `blocked`, `done`
- type: `workstream`, `risk`, `status-update`, `retro`

A simple board with one column per status is enough: Backlog, In progress, At risk, Blocked, Done.

## Linting

The CI only checks Markdown. To run it yourself:

```bash
npx --yes markdownlint-cli2 "**/*.md" "#node_modules"
```

## Honest notes

It's lightweight on purpose and won't replace a scheduling tool. I keep the GitHub and GitLab templates in sync by
hand, so they can drift. The cadences and scoring ideas are just suggestions. If I came back to it I'd add a short
worked example that follows one risk from the RAID log all the way to a retrospective.

## Licence

MIT, see [LICENSE](LICENSE).
