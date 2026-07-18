# Generative AI / LLM Policy

## TL;DR

- We know that you might use AI tools to help you.
- We don't accept abdication of responsibility to AI.
- Every contribution must come from a human who understands it and takes full responsibility, however it was produced.
- Any AI involvement in authoring means the contribution should include an `Assisted-by:` trailer - it's binary, it either had AI involvement or it didn't, with no threshold to judge.
- AI tools never go in Co-authored-by:.
- Unsupervised agentic tools are not permitted.
- If you can't explain and defend every line, don't submit it.
- During review: engage with feedback, don't just regenerate and resubmit. "The AI wrote it" isn't a valid answer.
- When reviewing, don't post AI-generated review comments or summaries without fact-checking them yourself.
- Consequences: rejection, permanent ban for bot-like behaviour, or being blocked until you talk to the Governance Working Group.


## Policy

Every contribution must come from a human, however it was created. Unsupervised agentic tools are not permitted. Accounts exhibiting bot-like behaviour - automated mass pull request creation or reviews - will be permanently banned, whether they belong to a human or not.

A contribution is anything you bring to the OCA - code, review, documentation, discussion. Contribution is a social process.

Contributions must be relevant and thought through. They must address real problems or real improvements. They should be describable in a short message, and should either have a tight scope or make very few changes.

Contributors are encouraged to be transparent with their use of AI by including an `Assisted-by:` trailer in the commit when any AI is used to develop the commit. This should be stated for any level of AI use, from advice through to fully autonomous coding, and this trailer carries no implication about the quality of the work. If multiple agents or models were involved, add a separate `Assisted-by:` line for each, following the same convention as `Co-authored-by:` with no blank lines between them:

```text
Assisted-by: Claude Opus 4.6
Assisted-by: GitHub Copilot:gpt-5
```

It is not necessary to add this to the PR title, but you should show it in the description.

Authorship fields such as `Co-authored-by:` must not be used for AI tools, as this remains legally undefined. Disclosure is welcomed and expected; it does not diminish the contributor's responsibility.

The three benefits of this declaration are as follows:

1. Attestation - It requires the contributor to decide, consciously, what is their own work and what was sourced from AI tools
2. Audit - It lets OCA see the scale and trend of AI-assisted contribution over time.
3. Ending the guesswork - Without declaration, poor contributions can be assumed to be AI and good ones assumed human - both often wrongly which is an inefficient distraction.

Self-quality check: if the contributor is not able to read and understand their contribution in full, they should not expect anyone else to. The human contributor takes ultimate and absolute responsibility for their contribution.

Review is a conversation - when a reviewer raises a point with the contributor, then respond to the point raised. Regenerating the contribution and resubmitting without engaging is not a response, and repeated iterations of this kind count against the rework dimension in the metrics framework.

The contributor must be able to explain and defend every line of their contribution. 'The AI wrote it' is not an answer to a question or a critique - it is a statement that the responsibility this policy requires has not been met.

Do not post AI-generated review comments. Maintainers can prompt an LLM themselves if they want its view; what a review contributes is human judgement, and that cannot be delegated. Do not post AI-generated summaries unless you have verified them and take responsibility for their content in full. All LLM output reads plausibly - establishing that it is also correct is the contributor's work, not the reader's.

If your contribution quantity, quality and rate fall outside acceptable metrics as defined in the Default Metrics Framework or PSC issued Metrics Framework, contributions will be rejected without further review. If the behaviour is not addressed, you will be blocked from contributing until you have discussed the matter with the Governance Working Group.

## Default Metrics framework

The contribution volume problem arises when quantity, rate and quality issues combine and the burden on reviewers multiplies rather than adds, and quickly exceeds what any volunteer can absorb.

Unless modified by PSC, contribution metrics are measured as follows.

The three dimensions:

Quantity
: The size of each contribution - lines changed, files touched, scope covered. Reference point: a patch is under 30 lines in a single file.

Rate
: How frequently contributions arrive from one source. Reference point: a reviewer needs time to absorb each change; contributions arriving faster than they can reasonably be reviewed are arriving too fast. Wait for acknowledgement before sending another.

Quality
: How much reviewer effort each contribution consumes - clarity of description, CI status, review iterations needed, relevance to a real problem.

A simple way to reason about the combined burden:

    reviewer burden = quantity x rate

Each dimension multiplies the others. Ten small clean patches over a month is a low burden. Ten large unclear PRs in a day is an unmanageable one, even though the count is the same.

Default red lines, any one of which triggers scrutiny and any two of which trigger rejection:

- more than 5 pull requests or 10 reviews from one source in 24 hours (it might depend on the specific PSC criteria)
- individual contributions exceeding 500 lines without prior agreement with a maintainer
- repeated review iterations that regenerate code rather than engage with feedback
- ultimately, the reviewer decides to accept or reject

These figures are starting points and will be tuned as tooling develops. The principle is fixed: contribute at a pace and size a human volunteer can meet.

## Credits

This policy was based on the policy of the attrs project, with thanks to them for developing it.

Development of this document was led by Stuart J Mackintosh, with significant contribution from Enric Tobella Alomar, and reviewed by the OCA Governance Working Group.
