# Adapting it: the last 20%

oversoul ships as a CRM for a solo consultant because that's where it was built. The pattern underneath is more general: several AIs, one folder of Markdown, one file per thing, shared rules, and Git as the memory and the audit trail. Finish it however your work needs.

## What you have to fill in

- **The Owner block** at the top of `AGENTS.md`: your name, your agents, your PM tool (or none), your handoff location, your timezone.
- **Your agents' access:** each one reads and pushes to your private copy, and nothing else.
- **The standing instruction**, pasted into each agent's permanent instructions. Without it, nothing sticks.

That's enough to run. Everything below is optional.

## What you can change

- **The fields.** `templates/person.md` is a starting point. Add the fields your work needs (industry, deal stage, renewal date, referral source) and delete the ones it doesn't. Change the template, then tell your agents to backfill on a branch (see "Large changes" in `AGENTS.md`).
- **The status words.** Client, prospect, partner, vendor, and former client fit a consultancy. A recruiter might use sourced, screened, placed. A nonprofit might use donor, volunteer, grantee.
- **The folders.** `people/` and `projects/` are two record types. Add your own: `vendors/`, `deals/`, `sources/`. Give each one a README that says what goes in it, a template, and a line in `AGENTS.md`.
- **The rules.** Keep the ones that protect you (no credentials, never invent, Contact OK, one file per thing). Loosen or add the rest.

## Other uses for the same pattern

- **A sales pipeline:** one file per deal, with a status line agents keep current.
- **A research notebook:** one file per source or per question; agents add findings and mark what's secondhand.
- **A household:** one file per vendor, contractor, appliance, or policy, with renewal dates and who to call.
- **A writing project:** one file per character, place, or thread, so every AI drafting a chapter knows the canon.
- **A job search:** one file per company and per contact, with what was sent and when.
- **A small team's shared brain:** the same CRM, written to by several people's agents instead of one person's.

## What to keep, whatever you build

- One file per thing, searched for before it's created.
- `unknown` instead of a guess.
- No credentials, ever.
- Absolute dates.
- Agents name themselves in commits and confirm their pushes landed.
- A review on a schedule.

Those are the parts that made it work with several agents at once. The rest is furniture.
