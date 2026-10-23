# First-pass prompt

Paste this into each agent once, after your private copy of the repo exists. Replace the bracketed parts. Each agent sweeps what it alone can reach, so run it in every agent you use.

---

```
You are one of [OWNER]'s AI agents (the others are [LIST OTHER AGENTS]). [OWNER] keeps a private GitHub repo that works as a shared CRM for every client, prospect, and partner: [REPO URL]

Do this:

1. Read the repo first, in the order AGENTS.md gives under "If you're new here": AGENTS.md, decisions.md, the newest reports/, then people/INDEX.md and projects/INDEX.md so you know who is already there. Follow the rules exactly. If the Owner block in AGENTS.md still says YOUR NAME, stop and ask [OWNER] to fill it in.

2. Go through the sources [OWNER] has given you access to for this work: your projects, past conversations and chats, files, notes, memory, and any apps [OWNER] has connected (email, calendar, freelance platforms, PM tools). Go back as far as those sources reach. Find every client, prospect, partner, vendor, and client-related company or person. Take only what's about the work: skip personal, family, health, and unrelated material even when it sits in the same mailbox or chat. Prefer primary records (the actual email, contract, invoice, or platform page) over summaries of them. Any fact you only have from a summary, including your own memory, gets marked secondhand.

3. For each one, create their profile in people/ from templates/person.md, or update the profile that's already there. Search for existing profiles by name, company, domain, email, and aliases before creating anything. Update in place; never make a second profile for the same person. Include who they are, company, status, Contact OK, the deal or history, key dates, contact details where you have them, and what's still open.

   Then, only for projects that actually exist in [PM TOOL], write one digest per project in projects/ from templates/project-digest.md. Link each digest to the client's profile, and list the digests in the profile's Projects line. Don't repeat the profile's contact details in the digest. Update people/INDEX.md and projects/INDEX.md in the same commit as each new file.

4. If you learn that someone unsubscribed, asked not to be contacted, died, or has a dead address, set their Contact OK line to no with the reason. That line is permanent.

5. If some of your material is unreachable from where you're running (another workspace, an app you're not connected to, a device you can't access), don't guess at its contents. List it by name in your report.

6. Don't invent anything. If a detail is uncertain or missing, write that it's unknown.

7. Never copy passwords, codes, tokens, or financial account numbers into any file, even if they appear in the material you're reading.

8. Commit with your name leading the message, fetch and rebase, and push. Then re-read at least one changed file from the remote and confirm your change is there. If you can't push, put the files in the handoff location named in AGENTS.md, in the same folder structure, and say so in your report.

9. From now on, keep the repo current: whenever you do client work with [OWNER], update that person's file as part of the work and push.

10. Never create a project in [PM TOOL] for anyone. [OWNER] approves those personally; this repo is where everyone else lives.

When your first pass is done, write reports/YYYY-MM-DD-[your name]-first-pass.md from templates/report.md and push it. Then report back to me as a short list: who you added, who you updated, and what you couldn't reach.
```
