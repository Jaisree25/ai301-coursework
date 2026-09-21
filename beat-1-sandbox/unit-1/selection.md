# Unit 1 — Issue Selection

Path: `beat-1-sandbox/unit-1/selection.md`

Record of the issue carried into Unit 2, and of the evaluation runs that produced
`eval-run.txt`. This file is graded at the path above; a copy kept anywhere else in
the repository is not read.

Complete every labelled field below. Each is graded on its own; content placed under the
wrong label is not graded.

---

## Selected issue

**Issue link**

https://github.com/codepath/pathreview-ai301-fa26-s3/issues/69

**Verdict output**

````
Graded all three against the rubric, with the Path Review house rule from scope.md applied (classmates' claim comments don't block).

Shared repo evidence (all three candidates, captured 2026-09-21):
- maintainer-alive — pass: human commit by Aburke225 on 2026-09-16 (5 days ago); Aburke225 is COLLABORATOR on the issues.
- repo-in-use — pass: archived: false; no releases, but last push 2026-09-16 (within 90 days).
- ai-policy — pass: docs/CONTRIBUTING.md and the PR template say nothing about AI (silence passes).
- responsive (preferred) — fail: the 5 most recently updated issues were all opened by the maintainer and none has a maintainer reply yet (only student claims).

Ranked read-out — all three accepted, in fit order:

1. #69 Output parser crashes on a top-level JSON array — best fit. It's about how the RAG generator handles raw LLM output, the most LLM-facing of the three. Bounded bug in 2 named files, with the fix verified by removing an xfail marker from an existing test (est. 2–4 h). Two classmate claims (Yina-Mu, tonybuii2003), which the house rule ignores.
2. #60 Faithfulness checker crashes on text: None — RAG evaluation side, a good match for RAG/LLM work. Smallest fix, with exact repro steps and a named failing test. One classmate claim.
3. #57 Tech detector counts vendored/build files — agent side, but the fix is path filtering rather than model logic, so it matches AI interests least. Clear repro and 2 named failing tests. One classmate claim.

None rejected. Every candidate passed scope (maintainer-filed bug with named files/tests), unclaimed (no assignee, no linked or mentioned PR; classmate claims don't count here), and newcomer-friendly (good first issue label, maintainer-filed).

Note: responsive failed on all three because the tracker was seeded 11 days ago and the maintainer hasn't replied to anything yet. That isn't a sign of an unresponsive repo, just nothing to measure. The check is preferred, so no verdict changes.

```json
[
  {
    "item": "https://github.com/codepath/pathreview-ai301-fa26-s3/issues/69",
    "checks": [
      {"name": "maintainer-alive", "grade": "pass", "evidence": "2026-09-16 commit by Aburke225 (human, COLLABORATOR): 'chore: track five more manifest entries against the tracker'"},
      {"name": "repo-in-use", "grade": "pass", "evidence": "archived: false; no releases, but last push 2026-09-16 (5 days)"},
      {"name": "ai-policy", "grade": "pass", "evidence": "docs/CONTRIBUTING.md and PULL_REQUEST_TEMPLATE.md contain no statement on AI"},
      {"name": "scope", "grade": "pass", "evidence": "Maintainer-filed bug: .items() on list raises AttributeError; files named rag/generator/output_parser.py + tests/unit/test_output_parser.py; est. 2-4 hours"},
      {"name": "unclaimed", "grade": "pass", "evidence": "assignees: none; no linked or cross-referenced PRs; claims by Yina-Mu and tonybuii2003 are classmate claims, ignored per Path Review house rule"},
      {"name": "responsive", "grade": "fail", "evidence": "5 most recently updated issues (#69,#67,#60,#57,#62) all maintainer-opened with no maintainer reply"},
      {"name": "newcomer-friendly", "grade": "pass", "evidence": "labels: good first issue, tier-1; opened by maintainer; names files and the xfail test to un-mark"}
    ],
    "verdict": "accept"
  },
  {
    "item": "https://github.com/codepath/pathreview-ai301-fa26-s3/issues/60",
    "checks": [
      {"name": "maintainer-alive", "grade": "pass", "evidence": "2026-09-16 commit by Aburke225 (human, COLLABORATOR)"},
      {"name": "repo-in-use", "grade": "pass", "evidence": "archived: false; no releases, but last push 2026-09-16 (5 days)"},
      {"name": "ai-policy", "grade": "pass", "evidence": "docs/CONTRIBUTING.md and PULL_REQUEST_TEMPLATE.md contain no statement on AI"},
      {"name": "scope", "grade": "pass", "evidence": "Maintainer-filed bug with repro: check('Knows Python.', [{'text': None}]) raises TypeError; failing test test_none_context_chunk_text named"},
      {"name": "unclaimed", "grade": "pass", "evidence": "assignees: none; no linked or cross-referenced PRs; pkmaster21 claim is a classmate claim, ignored per house rule"},
      {"name": "responsive", "grade": "fail", "evidence": "5 most recently updated issues all maintainer-opened with no maintainer reply"},
      {"name": "newcomer-friendly", "grade": "pass", "evidence": "labels: good first issue, tier-1; opened by maintainer; repro + named test"}
    ],
    "verdict": "accept"
  },
  {
    "item": "https://github.com/codepath/pathreview-ai301-fa26-s3/issues/57",
    "checks": [
      {"name": "maintainer-alive", "grade": "pass", "evidence": "2026-09-16 commit by Aburke225 (human, COLLABORATOR)"},
      {"name": "repo-in-use", "grade": "pass", "evidence": "archived: false; no releases, but last push 2026-09-16 (5 days)"},
      {"name": "ai-policy", "grade": "pass", "evidence": "docs/CONTRIBUTING.md and PULL_REQUEST_TEMPLATE.md contain no statement on AI"},
      {"name": "scope", "grade": "pass", "evidence": "Maintainer-filed bug with repro: node_modules/ and build/ files counted, primary_language 'JavaScript' vs expected 'Python'; failing tests named"},
      {"name": "unclaimed", "grade": "pass", "evidence": "assignees: none; no linked or cross-referenced PRs; ApoorvThite claim is a classmate claim, ignored per house rule"},
      {"name": "responsive", "grade": "fail", "evidence": "5 most recently updated issues all maintainer-opened with no maintainer reply"},
      {"name": "newcomer-friendly", "grade": "pass", "evidence": "labels: good first issue, tier-1; opened by maintainer; repro + two named failing tests"}
    ],
    "verdict": "accept"
  }
]
```
````

---

## Eval iterations

Quote source text directly in each field below. Paraphrase does not satisfy them.

**Run history**

1. Partial run, `--only issue-01,issue-06,issue-09,issue-12,issue-20`: `agreement: 5/5 scored items`
2. Full run, saved with `--save-run eval-run.txt`: `agreement: 20/20 scored items  (bar: 18/20: PASS)`

**Issue analysis**

**issue-12** (bookwyrm-social/bookwyrm#1133). My rubric decided **reject**; the gold label is **reject**.

At first this one looks like an easy accept. maintainer-alive passed on "2026-08-12 Mouse Reeve merged PR #4080 from Patrick Childers' branch", repo-in-use passed on "release v0.9.1 on 2026-07-20", and unclaimed passed because the only claim comment was from 2024, which is way outside my 120-day window. It even has a `good first issue` label. The thing that killed it was the contribution policy line: "We do not accept AI-generated code or documentation." My ai-policy check only fails on an outright ban, and this is a ban, not a condition like disclosing or reviewing AI output. I use AI in my workflow for this course, so taking this issue would mean going against the maintainers' rule.

It also failed scope, which came back `unclear`. It's an enhancement opened by a user with association NONE, and the maintainer only said a stacked bar "could be built with html/css" and never actually agreed to the feature. My verdict rule treats unclear on a required check as a fail, so it would have been rejected even without the AI ban. Since two separate checks both said reject, I'm pretty confident this one is right.

**Check rationale**

> | scope | issue body + comment thread + linked PRs | Fail if: umbrella/tracking issue, OR a feature/behavior change that no maintainer opened or agreed to in the thread (bugs and docs tasks are fine), OR design still being argued, OR it's a usage question, OR 2+ PRs for it closed unmerged. | required |

The evidence guide says "short is not the same as unscoped", so I didn't want a scope check that just rewards long, well-written issues. Some of the bundle titles are also misleading on purpose. So I based scope on who asked for the work and whether the thread settled it. The middle clause is what separates issue-20 from issue-09. Both are feature requests, but issue-20 was opened by `cursor[bot]` with "Logo asset TBD" and 0 comments, and issue-09 was opened by a MEMBER who wrote "just give it a try". I left bugs and docs tasks out of that clause because the expected behavior is already known (issue-01 and issue-14 are docs tasks filed by contributors and should pass). I set the closed PR limit at 2 instead of 1 because issue-09 has one closed PR (#11627) and is still a good issue, but issue-15 has two abandoned PRs and years of design arguing.

**Trade-offs**

The "no maintainer opened or agreed to" clause can't tell the difference between a regression and a new feature. I ran the four calibration bundles to check with `--include-calibration --only calib-01,calib-02,calib-03,calib-04`, and the harness printed: "calib-01  accept  reject   NO     failed: scope, newcomer-friendly (preferred)". calib-01 is the p5.js `min()` issue. The body says "This is not an exact bug report, but a request", and `min(1, 2, 3, 4)` worked in v1 but errors in 2.x. It has 0 comments, so no maintainer had agreed to it yet, and my check treated it like an unapproved feature request. So my rubric will miss issues like this, where a real regression is written as a request and no maintainer has looked at it yet. If I loosened the clause, wishlist issues like issue-20 would start passing. Calibration items aren't scored, so I decided to keep the check as it is. The scored set didn't change: the full run is still 20/20, and the rubric.md fingerprint in eval-run.txt (`sha256:4eda842c74c6a7fa`) matches the file I uploaded.

---

## Selection rationale

Graded on whether all three are answered, in your own words. Not on how good the
reasoning is, and not on length — a short honest answer to each earns the full marks.
This is also the basis for the claim comment you write in Unit 2.

**Selection rationale**

1. **Fit and time.** I'm most interested in AI, LLMs and agents, and #69 is in `rag/generator/output_parser.py`, which is the code that turns raw LLM output into structured data. An LLM returning a JSON array instead of an object is a problem I've actually hit in my own RAG projects. It also seems like a good size for a first contribution: two files named in the issue, an estimate of 2-4 hours, and an existing `xfail` test (H-02) that will tell me when the fix works.
2. **What the verdict got right, and what it couldn't weigh.** The skill correctly found that the repo is active (commit 5 days ago), the issue is a bug filed by the maintainer with a clear scope, there's no assignee or open PR, and there's no AI restriction. What it can't really judge is how crowded the issue is. Two classmates (Yina-Mu and tonybuii2003) already commented to claim it. The house rule says that doesn't block me, but I still compared it to #60, which only has one claim. I went with #69 anyway because it fits my interests better. The responsive check failed too, but that's only because the tracker is 11 days old and the maintainer hasn't replied to anything yet, so I didn't hold that against it.
3. **Difficulty claiming it.** Since other people are already on it, my PR will probably be one of a few for the same bug. I want mine to stand out with a clean fix and a test that actually covers the array case, not just removing the `xfail`. I also need to write a real claim comment in Unit 2, not just a one-liner.

---

Related paths: `eval-run.txt` in this directory; your skill's files in
`tools/issue-select/`.
