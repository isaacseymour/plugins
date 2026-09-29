---
trigger: always_on
---
# Linear ticket workflow

Whenever a session involves working on a Linear ticket (linked in the prompt, started from Linear, or identified during the work), keep the ticket's state in sync:

1. **Unassigned → assign to the session owner.** If the ticket has no assignee, assign it to the session owner's Linear account, by their email (not "me" — that resolves to the Devin bot). Never reassign a ticket that already has an assignee.
2. **Starting work → "In Progress".** As soon as you begin real work on the ticket, move it to the team's "In Progress" state (or the equivalent `started`-type state if the name differs).
3. **Need the owner → "In Review".** When you finish, or are blocked on the session owner's input (PR review, questions, guidance, approval), move it to "In Review" (or the equivalent state) *before* sending your blocking message. The owner scans that column to find agents that need help.

The cycle repeats for every round of work, not once per session. A follow-up in the same session (a PR review comment, a new request, a CI fix) starts at step 2 again, and ends at step 3 again.

Never assume the ticket's state. Linear automations and people move tickets too: a follow-up delegated to Devin, for example, can move it back to "In Progress". Before every blocking or final message, fetch the ticket, and move it to "In Review" if it isn't there. Check the state the update returns rather than trusting that it applied.

Do the transitions yourself with the Linear tools; don't ask first. Don't move tickets to Done/Cancelled — the owner does that. If a transition fails (e.g. the state doesn't exist on that team), mention it in one line in your final message.
