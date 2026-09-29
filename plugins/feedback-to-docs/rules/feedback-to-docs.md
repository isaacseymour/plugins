# Turn feedback into docs

When the session owner corrects your approach, record the lesson in the internal docs, so the next agent on a similar task doesn't need the same correction. The feedback can come in the session or in a PR review. Do this every time as part of the work. Don't ask first.

## What counts

Feedback counts when your first approach was wrong and the reason applies beyond this change. For example: "we don't do it that way here", "use the existing helper", "that belongs in a different package", "check X before you touch Y", or a review comment that changes the design.

Skip it when:

- it's a one-off product or scope decision about this change only,
- it's a typo, a naming nit, or plain taste, or
- a future agent wouldn't plausibly make the same mistake.

Check whether the docs already say it. If they do, the doc was hard to find or unclear. Fix that: move it, reword it, or link it from where you looked first. Don't add a second copy.

## Where it goes

Put the lesson in the place an agent doing that kind of task will read, closest to the code it's about:

1. The nearest `AGENTS.md` to the affected code. When `CLAUDE.md` only includes `AGENTS.md`, edit `AGENTS.md`.
2. An existing skill that covers the task, in the repo's `skills/` directory or a plugin. Follow the repo's rules for skills, e.g. registering a new one in `skills/README.md`.
3. The repo's `docs/`, for longer explanations that an `AGENTS.md` links to.

Prefer the repo's docs over Devin Knowledge notes. Every agent that works in the repo reads the repo's docs, not only Devin. If the right home is unclear or lives in a repo you can't reach, propose the text to the owner in your message.

## How to write it

- Write the general rule and why it holds, not the story of this session. Don't mention the PR, the ticket, or who gave the feedback.
- Edit the existing section it belongs in rather than appending a new one. Match the file's style and terseness.
- Keep it short: one or two sentences, and a pointer to the helper, file, or example when one exists.

## Which PR it goes in

- **The same PR**, as its own commit, when the feedback is on an open PR, the doc is in the same repo, and the lesson is about the code that PR changes. The reviewer sees the fix and the lesson together, and both land together.
- **A separate PR** when the doc lives in another repo, the lesson is general rather than about this change, or the original PR is merged, queued to merge, or likely to be abandoned. Link it from the original PR or session.

In your next message, say what you recorded and where in one line.
