# Skills

A marketplace of skills for AI coding agents. One repo, many agents — start where you are.

## Skills

| Skill | What it does | Claude Code | opencode |
| --- | --- | --- | --- |
| [agent-topics](plugins/agent-topics/skills/agent-topics/SKILL.md) | Split a discussion into topics, one background subagent per topic. Chat with each agent directly; they sleep between messages and report back only when told to wrap. | ✅ | 🚧 planned |

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
cp -r skills/plugins/agent-topics/skills/agent-topics ~/.claude/skills/
```

## Install — opencode

Coming soon. The opencode flavor of `agent-topics` is in progress and will land under [`skills/`](skills/).

## For maintainers

After editing a plugin, validate before pushing:

```sh
claude plugin validate .
```

## License

MIT
