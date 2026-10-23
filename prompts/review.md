# Review prompt

Run this every week or two in any one agent. It keeps the repo trustworthy as it grows. Chat agents won't remember to run it on their own: set it up as a scheduled task if your agent supports one, or put a recurring reminder on your calendar.

---

```
Audit [REPO URL] against its AGENTS.md. Report only; don't change anything until I approve each fix.

1. Duplicates: two or more profiles in people/ that describe the same person or company (match on name, company, domain, email, and aliases).
2. Digest errors: any digest in projects/ with no link to a people/ profile or a broken link, any profile whose Projects line doesn't match its digests, any digest that repeats the profile's contact details, and any digest for a project that doesn't exist in the PM tool.
3. Contact OK: files missing the Contact OK line, and any sign of outreach drafted or sent to someone marked no.
4. Stale files: anything marked active, on hold, or with an open thread whose most recent date is more than 30 days old.
5. Secrets: any line that holds a password, code, token, key, or financial account number. Report the path and the type only. Never quote the value.
6. Invented-looking facts: precise figures or dates with no source and no "per …" note, which could be guesses.
7. Format drift: files missing Status, Last contact, or Next step, or using relative dates.
8. Index drift: entries in people/INDEX.md or projects/INDEX.md that don't match the files in their folder, and files missing from the index.
9. Decisions: any file that contradicts a ruling in decisions.md.

When you're done, write reports/YYYY-MM-DD-[your name]-review.md from templates/report.md.

Report as a short list, worst first, with the file path for each finding and the fix you recommend.
```
