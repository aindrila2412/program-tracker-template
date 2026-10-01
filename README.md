# Program Tracker Template

A personal, reusable starter kit for running a small program or project on GitHub or GitLab issues: issue templates, a RAID log, a weekly status report, a program charter, and a Markdown lint check.

> **Personal template project. Sample data only.**
> Every name, date, and status in this repository is **fictional sample content**. Nothing here describes real client, employer, or team work, and no real metrics are included.

## Purpose

I built this to practise (and share) a simple, async-first way to track a program using only core platform features. It is a starting point to adapt, not a prescribed methodology.

## What is inside

```text
program-tracker-template/
├── README.md
├── LICENSE
├── .gitignore
├── .markdownlint.json
├── .gitlab-ci.yml                     # GitLab CI: markdown lint
├── .github/
│   ├── ISSUE_TEMPLATE/                # GitHub issue templates
│   │   ├── config.yml
│   │   ├── risk-blocker.md
│   │   ├── status-update.md
│   │   └── retrospective.md
│   └── workflows/markdownlint.yml     # GitHub Actions: markdown lint
├── .gitlab/issue_templates/           # GitLab issue templates
│   ├── risk-blocker.md
│   ├── status-update.md
│   └── retrospective.md
├── templates/
│   ├── program-charter-template.md
│   ├── weekly-status-template.md
│   ├── raid-log-template.md
│   ├── raid-log-template.csv
│   └── dependency-register-template.csv
└── examples/                          # fictional, filled-in samples
    ├── sample-charter-fictional.md
    ├── sample-weekly-status-fictional.md
    ├── raid-log-sample.csv
    └── dependency-register-sample.csv
```

## How to use it

1. Create a new repository or project and copy in the files you need.
2. **Issue templates:** keep `.github/ISSUE_TEMPLATE/` for GitHub or `.gitlab/issue_templates/` for GitLab (delete the other).
3. **Labels:** create the labels in [Labels](#labels). On GitLab, scoped labels use `::`. On GitHub, use the `type: ...` names the templates reference.
4. **Charter:** fill in `templates/program-charter-template.md` at kick-off.
5. **Dependencies:** list cross-team dependencies in `dependency-register-template.csv` and link them from the RAID log.
6. **RAID log:** keep `raid-log-template.csv` in a spreadsheet, or use the Markdown version. Review it weekly.
7. **Status:** post a weekly status issue (or copy `weekly-status-template.md`).
8. **Retrospective:** open a retrospective issue at each milestone or at close.
9. **CI:** the Markdown lint runs on pull/merge requests and on the default branch.

## Labels

| Label (GitLab scoped) | Purpose |
|---|---|
| `status::backlog` | Not yet started |
| `status::in-progress` | Being worked on |
| `status::at-risk` | Needs attention or has a risk raised |
| `status::blocked` | Cannot proceed until a blocker is resolved |
| `status::done` | Finished |
| `type::workstream` | A major piece of the program |
| `type::risk` | A risk or blocker issue |
| `type::status-update` | Periodic status report |
| `type::retro` | Retrospective |

## Board layout

One board with a list per status: Backlog, In progress, At risk, Blocked, Done. Optionally filter by milestone.

## Sample program board (fictional)

*Program: "Example Onboarding Revamp". Illustrative only.*

| Workstream | Status | Owner | Next step | Target date |
|---|---|---|---|---|
| Requirements and scope | `status::done` | Sample Owner A | Sign-off recorded | 2026-01-15 |
| Training content | `status::in-progress` | Sample Owner B | Draft module 2 | 2026-02-10 |
| Tooling setup | `status::blocked` | Sample Owner C | Waiting on access approval | 2026-02-20 |
| Pilot rollout | `status::backlog` | Sample Owner A | Confirm pilot group | 2026-03-05 |

## Linting locally

```bash
npx --yes markdownlint-cli2 "**/*.md" "#node_modules"
```

## Limitations

- It is a lightweight template. It does not replace a scheduling tool or a formal methodology.
- The GitHub and GitLab templates are kept in sync by hand.
- Scoring guides and cadences are suggestions only.

## Licence

MIT. See [LICENSE](LICENSE).
