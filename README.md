# oversoul

A shared memory for a team of AI agents, kept as plain Markdown in one private Git repo.

![The oversoul house: a house built of paper files, five agents arriving as orbs of light, one shared memory glowing in the attic, and the starter jar in the window](oversoul-doodle.jpg)

You probably work with more than one AI: Claude in one window, Claude Code in a terminal, ChatGPT or Codex somewhere else, maybe a custom agent on a server. Each one forgets everything between sessions, and none of them knows what the others did. oversoul fixes that the boring way. Every person or company you work with gets one Markdown profile in `people/`. Every project that already exists in your project-management tool gets a short digest in `projects/`, linked to that profile. Every agent reads the profile and its digests before acting on that person, and updates them after. That's the whole system.

This is a framework, not a product: a way for several AIs to collaborate on one body of knowledge. It ships about 80% finished. The rules, templates, prompts, and lessons are here. The folders are empty, and the last 20% is yours: your name, your agents, your fields, your use. Think of it as an empty house, or a sourdough starter. `docs/adapting.md` has ideas for finishing it.

I built this for myself first—one shared memory for the crew of AI agents I work with every day—then stripped out everything personal to me. What is left is yours to clone and use, or to study as a source for your own fork.

## Why "oversoul"

In his 1841 essay "The Over-Soul," Ralph Waldo Emerson described "that Unity, that Over-soul, within which every man's particular being is contained and made one with all other." Each of your agents is a fragment: it sees one conversation, forgets it, and never meets the others. The repo is the one memory they all draw from and all add to. No single agent holds the whole picture, and every agent can read it.

## Why Git and Markdown

- **Every agent can read it.** Anything that can read a file or clone a repo can use it. No API keys, no vendor, no schema migrations.
- **History for free.** Every change has an author, a date, and a commit message. When an agent gets something wrong you can see which one, and roll it back.
- **Diffable and greppable.** You can read the whole CRM in a text editor. So can every agent.
- **Yours.** It's a folder. Move it anywhere.

## Two kinds of record

Most people keep their biggest projects in a real project-management tool (Basecamp, Linear, Asana, Notion, whatever) and everyone else in their head. oversoul gives both a place:

- **`people/`** holds one profile per person or company: clients, prospects, partners, vendors, and former clients worth remembering. Who they are, how to reach them, the deal, the history. Everyone you work with has exactly one.
- **`projects/`** holds a short digest of each project that already lives in your PM tool, linked to the client's profile. A client with two projects has one profile and two digests. The full record stays in the PM tool; the digest is the part every agent needs. Optional: delete the folder if you don't use a PM tool.

Agents can document a project that exists. Only you can create one.

## Get started

1. Click **Use this template** on GitHub. **Make your copy PRIVATE.** It will hold names, emails, phone numbers, and deal terms.
2. Edit the **Owner** section at the top of `AGENTS.md`: your name, your business, your agents, your PM tool.
3. Give each agent access to your private repo.
4. Paste `prompts/first-pass.md` into each agent. Each one sweeps everything it can reach, fills `people/`, and writes a `projects/` digest for each real PM project.
5. Add `prompts/standing-instruction.md` to each agent's custom instructions, project instructions, or memory, so it keeps the repo current from then on.

`docs/setup.md` covers each step in more detail, including how to connect the most common agents.

## What's in the box

| Path | What it is |
|---|---|
| `AGENTS.md` | The rules, plus a map for any AI arriving cold: what to read, where everything goes. Codex and similar tools load it automatically |
| `decisions.md` | The owner's standing rulings, one dated line each. Overrides every agent's defaults |
| `CLAUDE.md`, `GEMINI.md` | One-line pointers to `AGENTS.md` for tools that look for their own filename |
| `templates/person.md` | The shape of a `people/` profile |
| `templates/project-digest.md` | The shape of a `projects/` digest |
| `templates/report.md` | The shape of an agent's session report |
| `people/`, `projects/` | Empty, each with a README and an `INDEX.md` showing the line format |
| `reports/` | Empty. One file per substantial agent session, so agents can see what the others did |
| `docs/example-person.md`, `docs/example-project-digest.md` | A filled-in profile and project digest for a made-up client, so you can see what good looks like |
| `prompts/first-pass.md` | The kickoff prompt: sweep your sources and populate the repo |
| `prompts/standing-instruction.md` | The short instruction that keeps every agent writing back |
| `prompts/review.md` | A periodic audit prompt: stale files, duplicates, leaked secrets |
| `docs/setup.md` | Setup, step by step |
| `docs/adapting.md` | The last 20%: what to fill in, and other ways to use the same pattern |
| `docs/lessons.md` | What went wrong with real agents on a real CRM, and the rule each mistake produced |

## What this is not

- **Not a password manager.** Credentials never go in this repo. Use 1Password, Bitwarden, or similar.
- **Not code.** There's nothing to install or run. It's a set of conventions that agents follow.
- **Not public data.** The template is public. Your copy must not be.

## License

[CC BY 4.0](LICENSE). Use it, fork it, sell services on top of it, and credit the source.

Started by [Chris Abraham](https://chrisabraham.net).
