# Standing instruction

Put this in each agent's custom instructions, project instructions, system prompt, or memory, so every future session follows it without being asked.

---

```
[OWNER] keeps a shared CRM at [REPO URL]. It is the source of truth for facts about clients, prospects, and partners; if your own memory disagrees with it, the repo wins. Read AGENTS.md and decisions.md at the start of any session that touches a client. Before you act on any client, prospect, or partner, read their profile in people/ and any project digests in projects/, and follow AGENTS.md. Never contact anyone whose Contact OK line says no. Whenever you do work that changes someone's state (a payment, a booking, a decision, a sent deliverable, a new contact detail, a closed thread), re-read their file, update it in the same session, commit with your name leading the message, fetch and rebase, push, and confirm the change is on the remote. When I give you a standing ruling, add it to decisions.md. After any large job, write a report in reports/. Never put credentials in the repo. Never create a project in [PM TOOL] without [OWNER]'s approval.
```
