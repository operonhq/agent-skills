# Operon Agent Skills

[![skills.sh](https://skills.sh/b/operonhq/agent-skills)](https://skills.sh/operonhq/agent-skills)

Canonical SKILL.md files for AI agent monetization, published by [Operon](https://operon.so) - the ad network for AI agents.

These skills run inside any Skill-aware agent (Claude Code, Cursor, Codex CLI, Windsurf, ElizaOS, and others). They help developers reason about and integrate Operon as a publisher.

## About

Three skills, distributed as plain Markdown files with YAML frontmatter:

1. **`estimate-agent-revenue`** - projects monthly revenue for an agent based on query volume, vertical, and fill rate.
2. **`score-agent-response-quality`** - rates an existing agent response across six dimensions and explains why each score was assigned.
3. **`monetize-agent-responses`** - guided integration of Operon's publisher SDK (generic `@operon/sdk` or ElizaOS `@operon/plugin-publisher-sdk`) into an existing agent. ~10 minute walkthrough on Node 18+.

Aggregator marketplaces (LobeHub, SkillsMP, FindSkills, MCP Market) auto-index this repo via GitHub crawl. No submission needed; their listings will pick up the canonical skills with `source: skill3-github` attribution.

## Install

### skills CLI (recommended)

```bash
npx skills add operonhq/agent-skills
```

Pulls all three skills. Counts toward the skills.sh leaderboard. Works with Claude Code, Cursor, Windsurf, and other skills-CLI-compatible agents.

### Per-skill curl

For surgical pulls of a single skill:

```bash
curl -o SKILL.md https://operon.so/skills/estimate-agent-revenue/SKILL.md
curl -o SKILL.md https://operon.so/skills/score-agent-response-quality/SKILL.md
curl -o SKILL.md https://operon.so/skills/monetize-agent-responses/SKILL.md
```

### Source-only install

Clone this repo and point your agent at the SKILL.md files directly:

```bash
git clone https://github.com/operonhq/agent-skills.git
```

Then load any `*/SKILL.md` into your agent's skills directory or your tool's skill loader. The frontmatter is stable across loaders that follow the Anthropic Skill convention.

## Source attribution

Each SKILL.md sets a `source` field (in the integration skill's SDK init block) that flows through to placement logs and the publisher dashboard. Canonical: `skill3-github`. Marketplaces that ingest this repo may rewrite the value to credit their channel.

If you fork or republish, leave the `source` value alone unless you have a reason to retag (and tell us, so we can wire your attribution string).

## Contributing

Issues and PRs are welcome.

- Bug or copy fix in an existing skill: open a PR against the relevant `SKILL.md`.
- Voice rules: hyphens not em dashes, no "this isn't X, this is Y" framing, no marketing-speak. Match the existing tone.

## Links

- Skills landing page: [operon.so/skills](https://operon.so/skills)
- Operon homepage: [operon.so](https://operon.so)
- Publisher SDK on npm: [@operon/sdk](https://www.npmjs.com/package/@operon/sdk)
- ElizaOS plugin: [@operon/plugin-publisher-sdk](https://www.npmjs.com/package/@operon/plugin-publisher-sdk)
- Contact: hi@operon.so

## License

MIT. See [LICENSE](LICENSE).
