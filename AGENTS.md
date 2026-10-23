# Rules for agents working in this repo

Read this whole file before you read or write anything else here. These rules apply to every agent equally.

## If you're new here

You may be any AI, arriving with no memory of this repo. Start here.

**Read in this order:**

1. This file, all of it.
2. `decisions.md`: the owner's standing rulings. They override your defaults and anything you remember.
3. The newest few files in `reports/`, so you know what other agents did recently.
4. `people/INDEX.md` and `projects/INDEX.md`, to see who's already here.
5. The specific profile or digest you're about to work on.

**First, check the Owner block below.** If it still says `YOUR NAME`, this copy hasn't been set up. Don't fill it in yourself. Ask the owner, and work only on what they ask until it's done.

**Finding someone:** look them up in `people/INDEX.md`, then search the whole repo for their name, company, domain, email, and aliases. Never trust one search alone.

**Where everything goes:**

| You have… | It goes in… | Start from… |
|---|---|---|
| A person or company you work with, or might | `people/firstname-lastname.md` | `templates/person.md` |
| A project that already exists in the PM tool | `projects/client-project.md` | `templates/project-digest.md` |
| A standing ruling the owner just gave you ("always X," "never Y") | `decisions.md`, one dated line | The format at the top of that file |
| What you did in a session: a first pass, a review, a bulk change | `reports/YYYY-MM-DD-agent-task.md` | `templates/report.md` |
| A file you made but can't push | The handoff location in the Owner block | Same folder structure as here |
| A password, code, key, or account number | Nowhere in this repo | The owner's password manager |

**Examples:** `docs/example-person.md` and `docs/example-project-digest.md` show filled-in records for a made-up client. Copy their shape, never their content.

## Owner

<!-- Fill this in once, when you set up your copy. -->

- **Owner:** YOUR NAME, YOUR BUSINESS
- **Agents that write here:** e.g. Claude, Claude Code, ChatGPT, Codex, a custom agent
- **Project-management tool:** e.g. Basecamp, or "none" (if none, delete `projects/`)
- **PM project limit:** e.g. "12 projects, owner approves every one," or "none"
- **Handoff location:** where an agent that can't push leaves its files, e.g. a shared Drive folder or a folder on a server every agent can reach
- **Default timezone for dates:** e.g. America/New_York

## What this repo is

A CRM written as Markdown. One person or company per file. Every agent reads the relevant file before acting on that person, and updates it in the same session when something changes. It is a CRM, not a codebase: no code, no HTML, no scripts in `people/` or `projects/`.

This repo is the source of truth for facts about clients, prospects, and partners. If an agent's own memory disagrees with a file here, the file wins, and the agent fixes whichever one is wrong.

## The rules

1. **One profile per person.** Every person or company has exactly one profile in `people/`. Before creating one, search the repo for the person's name, company, domain, email, and any alias. If a profile exists, update it in place. Two profiles for one person is the most common failure (see `docs/lessons.md`). If you find two, merge them into one and delete the other in the same commit.
2. **One digest per real PM project.** `projects/` holds one digest for each project that already exists in the PM tool, and nothing else. A client with two PM projects has two digests and still one profile. These are different kinds of record, not duplicates.
   - Every digest links to the client's `people/` profile on its first line. Contact details and the overall relationship live in the profile; don't repeat them in each digest.
   - The profile lists the client's digests under **Projects**.
3. **Never create a project yourself.** You may write a digest for a project that exists. Creating a project in the PM tool, or proposing to move a client into one, needs the owner's explicit approval.
4. **Respect Contact OK.** Every person file carries one line in exactly this form: `- **Contact OK (YYYY-MM-DD):** yes`, `no`, or `ask owner`, with the date it was last decided.
   - `no` (they unsubscribed, asked not to be contacted, died, or the address is dead) is permanent. Never override it, never delete it, never draft outreach to that person. Add the reason on the same line.
   - If the line is missing, treat it as `ask owner`.
5. **Keep files current.** When you learn something that changes a person's state (a payment, a booking, a decision, a sent deliverable, a closed thread, a new contact detail), update their file in the same session. A stale file is worse than no file, because agents trust it.
6. **Facts, not feelings.** Record who they are, deal terms, dates, deliverables, contact details, open threads, decisions, and working rules: how this person needs to be worked with ("money discussed only in writing," "never rewrite their wording"). Leave out the owner's venting, gossip, and private opinions of people.
7. **Never invent.** If you don't know something, write `unknown`. Don't estimate, round, or fill gaps with plausible guesses. A wrong fact in a CRM gets repeated by every agent that reads it.
   - Primary records (the email, the contract, the invoice, the platform's own page) beat summaries. A fact you only have from a summary (your own memory, a chat recap, another agent's notes) is secondhand; mark it so (see rule 11).
8. **No credentials, ever.** No passwords, PINs, backup or recovery codes, API keys, tokens, or session links. Email threads and chat logs often contain these; strip them when you copy context in. "Login is in the password manager under X" is fine.
9. **No highly sensitive personal data.** No government ID numbers, tax IDs, bank or card numbers, health details, or private home addresses of individuals. Business addresses, work emails, and work phones are fine and wanted.
10. **Dates on everything.** Use absolute dates (`Oct 21, 2026`), never relative ones ("last Tuesday," "next week"). Every status line and every "latest" line gets a date.
11. **Say where facts came from when it matters.** If a fact is secondhand, inferred from a platform listing, or contradicts another source, say so in a few words ("per the Upwork contract record," "per the owner, Oct 3, 2026," "secondhand: from a chat summary").
12. **Never contradict the PM tool.** A `projects/` digest is deliberately shorter than the PM tool's record, but nothing in it may disagree with the PM tool. If you change one, make sure the other still agrees.

## File format

All filenames are lowercase, hyphens only. Short lines, one fact per line where you can.

**Profiles (`people/`):** name the file `firstname-lastname.md` or `firstname-lastname-company.md`, or `company-name.md` when there's no named person. Copy `templates/person.md`; `docs/example-person.md` shows a filled-in one.

- Title line: `# Name—Company (domain)`
- Then short bulleted fields: **Status**, **Contact OK**, **Who**, **Contact**, **Deal**, **Projects**, **History**, **Last contact**, **Open threads**, **Next step**
- Status is one of: client, former client, prospect, partner, vendor. Add a qualifier after it (on hold, paused, cold, winding down).

**Digests (`projects/`):** name the file after the client and the project, e.g. `example-co-site-migration.md`. Copy `templates/project-digest.md`. The first line under the title links to the client's profile.

## Working alongside other agents

Other agents may be writing to this repo at the same time as you.

- **Re-read before you write.** However you write (git, a connector, an API), read the current version of the file immediately before changing it. Files change under you.
- **Pull before you write, and fetch and rebase right before you push.** If your push is rejected, rebase and push again. Never force-push.
- **Read back after you push.** Re-read at least one file you changed, from the remote, and confirm your change is there. A push can report success and still not contain what you meant.
- **Check again for duplicates after rebasing.** Another agent may have created the same person's file while you worked. If so, merge your facts into their file and delete yours in the same commit.
- **Edit in place.** Change the lines that changed. Don't rewrite a file wholesale unless you're fixing its structure.
- **Lead the commit message with your name** ("Claude: …", "Codex: …") so the history shows which agent wrote what.

## Large changes

- **Mass edits go on a branch.** Any change that touches more than a handful of files (a new field everywhere, a format fix, an import) goes on its own branch first. It isn't done until you've counted the files changed on the remote and the count matches what you intended. Then merge.
- **Keep the indexes current.** `people/INDEX.md` and `projects/INDEX.md` list one line per file, in the format shown at the top of each. Whoever adds, renames, or deletes a file updates the index in the same commit. The indexes are how a cold agent finds anyone without reading a thousand files.

## When you can't reach a source, or can't push

- If some of the owner's material is out of your reach (another agent's workspace, an app you're not connected to, a machine you can't access), don't guess at it. List it by name in your report so the owner can pull it.
- If you can't push to this repo, put your files in the **handoff location** named above, in the same folder structure, and say so in your report. Only hand files to the owner directly if no handoff location exists. Files left with the owner tend never to reach the other agents.

## Recording the owner's decisions

When the owner gives you a standing ruling ("this repo beats your memory," "never email anyone at Example Co," "statuses are now sourced/screened/placed"), add it to `decisions.md` as one dated line in the same session. A ruling that lives only in your chat dies with your chat.

## Reporting back

After any substantial session (a first pass, a review, a bulk change, an import), do both:

- Write a report to `reports/YYYY-MM-DD-agent-task.md` from `templates/report.md`, and push it with your other changes. Other agents read these to see what's already been done.
- Tell the owner in a short list: who you added, who you updated, what you couldn't reach, and anything that needs their decision. Don't recap file contents the owner can open.
