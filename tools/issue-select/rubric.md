# Rubric: is this a good first issue?

Dates are measured from the capture date (eval) or today (live). Ignore issue titles, go by repo facts and the comment thread. "Maintainer" = OWNER, MEMBER, or COLLABORATOR.

## Checks

| Check | Evidence | Pass condition | Weight |
|---|---|---|---|
| maintainer-alive | last 5 default-branch commits (author + date) | At least 1 commit in the last 90 days that is human work: authored by a non-bot, or a bot merging a PR from a human's branch. Bots merging bot PRs (dependabot etc.) don't count. | required |
| repo-in-use | repo line (archived flag), latest release, last push | archived: no AND (release within 365 days OR last push within 90 days). Stars don't matter. | required |
| ai-policy | contribution policy line | Fail only on an outright ban on AI-generated code. Conditions (disclose, review, understand, no *fully* AI-generated PRs) or no policy = pass. | required |
| scope | issue body + comment thread + linked PRs | Fail if: umbrella/tracking issue, OR a feature/behavior change that no maintainer opened or agreed to in the thread (bugs and docs tasks are fine), OR design still being argued, OR it's a usage question, OR 2+ PRs for it closed unmerged. | required |
| unclaimed | assignees, linked PRs, comment thread | Fail if: an assignee is set, OR any open PR (linked or mentioned in the thread; mentioned with unknown state counts as open), OR a claim comment in the last 120 days. Older claims with no PR are stale. | required |
| responsive | maintainer first-response sample | 2+ sampled issues got a maintainer reply within 14 days. | preferred |
| newcomer-friendly | labels, opener, issue body | good first issue / help wanted label, OR opened by a maintainer, OR names files / acceptance criteria. | preferred |

## Verdict rule

Accept only if all 5 required checks pass. Unclear on a required check counts as fail. Preferred checks never change the verdict, they just rank accepted issues.
