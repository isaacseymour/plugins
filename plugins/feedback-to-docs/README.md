# feedback-to-docs

A Devin plugin with one always-on rule: when you correct Devin's approach, in the session
or in PR review, Devin writes the lesson into the repo's agent docs (`AGENTS.md`, skills,
`docs/`) so the next agent on a similar task already knows it.

It adds the doc change to the PR under review when the lesson is about that PR's code, and
opens a separate PR when the doc lives elsewhere or the lesson is general.

## Installing

Install it for yourself only, at **Personal** scope:

- **Web app:** Customize → Plugins → Add plugin → From repository, enter
  `isaacseymour/plugins` with subdirectory `plugins/feedback-to-docs`, and pick the
  Personal scope.
- **CLI:** `devin plugins install isaacseymour/plugins#plugins/feedback-to-docs`

It applies to sessions started after you install it.
