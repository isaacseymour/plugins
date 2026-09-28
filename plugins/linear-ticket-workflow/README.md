# linear-ticket-workflow

A Devin plugin with one always-on rule: when a Devin session works on a Linear ticket, it

- assigns the ticket to you (the session owner) if it's unassigned,
- moves it to **In Progress** when it starts work,
- moves it to **In Review** when it's done or needs your input (review, questions,
  guidance).

Scan your **In Review** column to find sessions waiting on you.

## Installing

Install it for yourself only, at **Personal** scope:

- **Web app:** Customize → Plugins → Add plugin → From repository, enter
  `isaacseymour/plugins` with subdirectory `plugins/linear-ticket-workflow`, and
  pick the Personal scope.
- **CLI:** `devin plugins install isaacseymour/plugins#plugins/linear-ticket-workflow`

It applies to sessions started after you install it.
