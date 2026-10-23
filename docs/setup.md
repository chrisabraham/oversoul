# Setup

## 1. Make your private copy

On GitHub, open this template and click **Use this template → Create a new repository**. Set visibility to **Private**. Your copy will hold names, emails, phone numbers, and deal terms. Never make it public.

## 2. Fill in the Owner section

Open `AGENTS.md` and fill in the **Owner** block: your name, your business, which agents write here, which PM tool you use (or "none"), a handoff location, and your default timezone. If you don't use a PM tool, delete `projects/` and the line about it in the README.

The handoff location is where an agent that can't push leaves its files: a shared Drive folder, a folder on a server, anywhere every agent can reach. Without one, agents hand files to you, and files handed to you tend to sit in a chat window and never reach the repo.

## 3. Give your agents access

Every agent needs to read the repo and push to it. How depends on the agent:

- **Agents that run in a terminal or a cloud workspace** (Claude Code, Codex, and similar): give them a GitHub token or app access scoped to this one repo. They clone it, edit files, commit, and push like any developer.
- **Chat assistants with a GitHub connector**: connect GitHub and grant access to this repo only.
- **Chat assistants with no repo access**: they can still follow the rules. Ask them to produce the updated file, then commit it yourself or hand it to an agent that can push.
- **Custom agents on your own server**: clone the repo there and let the agent push with a deploy key that can write to this repo only.

Give each agent the narrowest access that works: this repo, nothing else.

- Use the narrowest credential your platform offers: a fine-grained token or app installation limited to this one repo, with write access to contents and nothing more. Give each agent its own, so you can revoke one without breaking the others.
- Store it in the agent's own secure credential store (its connector settings, secrets manager, or environment). Never paste a token into a prompt or a chat, and never commit it to the repo.
- If a token leaks, revoke it first, then figure out how it happened.

## 4. Run the first pass

Paste `prompts/first-pass.md` into each agent, one at a time or all at once. Each agent sweeps its own conversations, files, and connected apps. Expect duplicates and gaps on the first run. The second agent will find files the first one created and should update them in place.

## 5. Make it stick

Put `prompts/standing-instruction.md` wherever each agent keeps permanent instructions (custom instructions, project instructions, a system prompt, or memory). Without it, agents follow the rules when asked and forget the rest of the time.

## 6. Decide which memory wins

Many agents now keep their own memory of you and your clients. That gives you two sources of truth, and they will drift apart. Decide once, and tell every agent: this repo is canonical for facts about clients, prospects, and partners. When an agent's memory disagrees with a file, the file wins and the agent fixes the difference. The standing instruction already says this; make sure it's in every agent.

## 7. Review it on a schedule

Run `prompts/review.md` every week or two. Chat agents won't remember to on their own, so give it a mechanism: a scheduled task if your agent supports one, or a recurring calendar reminder to paste the prompt yourself. Fix duplicates and stale files as they show up.

## Optional: a secret scan

Rule 6 depends on every agent getting it right every time. A free secret scanner (for example, GitHub's own secret scanning, or gitleaks as a GitHub Action) gives you a backstop that flags credentials pushed by mistake. Turn one on if you can.
