# Rubric: is this a good first issue?

<!--
THIS IS THE PART YOU WRITE. The skill in SKILL.md executes whatever checks
you define here. It ships empty on purpose: the judgment is your work.

A filled rubric must contain:

1. At least one row in the checks table. Each row needs all four columns:
   - Check: a short name (used in the output JSON).
   - Evidence: exactly what to look at, and where. Name the source
     (repo-facts block, issue body, comment thread, or the locations in
     references/evidence-guide.md). "The repo" is not a source; "the last
     5 default-branch commit dates" is.
   - Pass condition: a condition someone else could apply and get your
     answer. Prefer thresholds with numbers ("a maintainer commented
     within 30 days") over adjectives ("maintainer is responsive").
   - Weight: `required` (a fail here rejects the issue) or `preferred`
     (never changes the verdict; a nice-to-have that helps rank the
     issues you accept).

2. A verdict rule below the table: how the check grades combine into
   accept or reject, including how `unclear` is treated. The verdict
   space is binary. If you write no rule for `unclear`, the skill treats
   it as fail.

Cover what actually kills first contributions. The lecture named four
families: the maintainer is alive, the repo is in use, the scope fits a
newcomer, and nobody else is already on it. A rubric that ignores a family
will fail eval issues designed around that family.
-->

## Checks

| Check | Evidence | Pass condition | Weight |
|---|---|---|---|
| unclaimed |  Issue body, assignees list, and comment thread.| Issue has 0 assignees, no open linked PR attempting a fix, and no unabandoned claim comment within the last 14 days. | Required |
| repo_in_use |  Repo facts: repository status, archiving flag, and PR activity.| Repository is not archived or marked read-only, has at least 50 stars, and has merged at least 1 pull request within the last 90 days. | required |
| maintainer_active |Repo facts: commit history and comment timestamps.  | At least 1 commit to default branch or maintainer comment response within the last 60 days. | Required |
| beginner_friendly |  Issue is explicitly labeled `good first issue`, `beginner-friendly`, `easy`, or a maintainer comment explicitly confirms newcomers are welcome.| Issue is explicitly labeled `good first issue`, `beginner-friendly`, `easy`, or a maintainer comment explicitly confirms newcomers are welcome. | Preferred|
## Verdict rule

<!-- State how the grades above combine into accept or reject, and how
unclear is treated. Example shape (write your own): "accept if every
required check passes; preferred checks never change the verdict, they
rank accepted issues; unclear counts as fail." -->

Accept if and only if every `required` check passes. If any `required` check fails or is unclear, the verdict is reject (unclear counts as fail). The `preferred` check (`beginner_friendly`) never alters the binary verdict; it is strictly used to rank accepted issues.