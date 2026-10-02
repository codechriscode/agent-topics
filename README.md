# Skills

A repo you can add as marketplace of skills. One repo, many agents — start where you are.

Layout is harness-first: each harness gets a folder (`claude/`, `opencode/`, ...) holding the same-named skill, flavored for that harness's mechanics.

## Skills

| Skill | What it does | Claude Code | opencode |
| --- | --- | --- | --- |
| [agent-topics](claude/agent-topics/skills/agent-topics/SKILL.md) | Split a discussion into topics, one subagent per topic. Chat with each agent directly; they idle between messages and report back only when told to wrap. | ✅ | 🚧 in progress |

## Install — Claude Code

Add this repo as a plugin marketplace and install the skill:

```sh
claude plugin marketplace add codechriscode/skills
claude plugin install agent-topics@skills
```

Or from inside a session:

```
/plugin marketplace add codechriscode/skills
/plugin install agent-topics@skills
```

The skill loads as `agent-topics` (prefixed `agent-topics:` in plugin context). Restart your session or run `/reload-plugins` if it doesn't show up right away.

### Manual install (no marketplace)

Copy the skill folder into your personal skills directory:

```sh
git clone https://github.com/codechriscode/skills
mkdir -p ~/.claude/skills
cp -r skills/claude/agent-topics/skills/agent-topics ~/.claude/skills/
```

## Install — opencode

In progress — the opencode flavor of `agent-topics` is being tested and is not published yet. It ships a `SKILL.md` plus a `/agent-topics` command (a `.opencode/command/agent-topics.md` file) so the skill can also be invoked as a literal slash command.

> Both flavors share the skill name. Install only the flavor for your harness: opencode also reads `~/.claude/skills/`, so having both flavors in directories it scans causes a name collision.

## For maintainers

After editing a plugin, validate before pushing:

```sh
claude plugin validate .
```

## License

MIT
