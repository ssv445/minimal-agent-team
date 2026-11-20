# Pre-review self-check

The builder runs this before every review request and fix round. Add a line whenever a review FAIL teaches one. Write new lines as "When the diff <trigger>: <check>". Mark a line n/a if its trigger doesn't match.

- [ ] Lint and the touched tests are green (a lint nit must never use a review round)
- [ ] Every claim in the spec or PR body is true in the code
- [ ] Each error path has a test
- [ ] Acceptance criteria wording matches what the tests assert
- [ ] New site-wide text (banner, footer): grepped existing tests for that text
- [ ] When the diff removes, skips or loosens a test or assertion: say so, with the reason, in the PR's For humans part
- [ ] Merged the base in before the final review
- [ ] All fixes from the last round are in one commit, one push
