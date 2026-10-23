# Lessons learned

Every rule in `AGENTS.md` exists because something went wrong without it. These are the cases, from running this system with several agents on a real consulting practice.

## Two agents, one person, two files

Two agents worked the repo at the same time. Both found the same vendor, and both created a file for it under slightly different names. Neither checked again before pushing.

**Rule:** Search by name, company, domain, and email before creating a file. Check again after rebasing. If you created a duplicate, merge your facts into the existing file and delete yours in the same commit.

## "Unsubscribe," and a contact who had died

During an outreach campaign, one person replied "Unsubscribe" and another contact turned out to have died. The files had nowhere to record either fact. Nothing would stop the next agent from drafting a friendly follow-up to both. The fix meant adding one field to over a thousand existing files.

**Rule:** Every person file carries a Contact OK line from day one. "No" is permanent and never deleted.

## The handoff that never arrived

An agent that couldn't push built the files and handed them to the owner. They sat in a chat window until the owner noticed and carried them to another agent by hand.

**Rule:** Agents that can't push leave files in a named handoff location every agent can reach. Handing files to the owner is the last resort.

## The push that changed nothing

An agent pushed, got a success message, and moved on. Another agent had moved the file in the meantime, so the push changed nothing that mattered. Fetching and rebasing didn't catch it.

**Rule:** Re-read the current file right before writing it. After pushing, read back at least one changed file from the remote and confirm the change is there.

## The summary that looked like a fact

Agents building files from their own conversation summaries believed they were following "never invent." But a summary is already a paraphrase, and details drift every time one is copied.

**Rule:** Primary records beat summaries. A fact you only have from a summary is marked secondhand.

## A thousand files, counted

A field was added to every person file across several agent sessions. Partway through, nobody could say which files had it.

**Rule:** Mass edits go on a branch and aren't done until the count of changed files on the remote matches the intended count.

## The email thread had a password in it

The most useful context about a client was a long email thread. Halfway down, someone had pasted a login so a contractor could fix the site. An agent summarizing the thread could easily have copied it straight into the CRM.

**Rule:** No credentials, ever, including ones you find in source material. Write "login is in the password manager" if the fact that access exists matters.

## Plausible is not true

When a client file is thin, an agent wants to fill it in. A guessed rate, an assumed start date, or a likely job title reads exactly like a real fact, and every agent after it repeats it.

**Rule:** Write `unknown`. A file full of honest unknowns tells the owner what to fill in; a file full of guesses tells nobody anything.

## The platform says active; the client went quiet months ago

Freelance platforms and PM tools keep contracts open long after the work stops. An agent that copies "Active" from the platform makes a dead client look live.

**Rule:** Record the platform status and the real last-contact date separately. Let the owner decide what "active" means.

## "Last week" is useless a week later

Agents wrote relative dates ("yesterday," "next Monday"). They were correct when written and wrong forever after.

**Rule:** Absolute dates only, on every status line.

## The agent couldn't see it, so it said nothing

One agent had no access to another agent's workspace. It didn't mention the gap, and the owner assumed the sweep was complete.

**Rule:** List every source you couldn't reach, by name. A gap you report gets filled; a gap you hide doesn't.

## The CRM turned into a diary

Owners talk to their agents candidly about clients: frustrations, guesses about motives, private opinions. Copied into a shared file, that becomes both useless to the next agent and a liability if the file is ever seen.

**Rule:** Facts, not feelings. Deal terms, dates, deliverables, contacts, decisions, open threads, and working rules ("money discussed only in writing"). The working rules stay; the venting goes.

## A project for everyone

Once a nice project exists in the PM tool, agents start making more. Slots fill with one-off clients, and the PM tool stops meaning "the people who matter most."

**Rule:** Agents document projects that exist. They never create one. The owner approves each one.
