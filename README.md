# Operon Agent Skills

Canonical SKILL.md files for AI agent monetization, published by [Operon](https://operon.so) - the ad network for AI agents.

These skills run inside any Skill-aware agent (Claude Code, Cursor, Codex CLI, ElizaOS, and others). Three of them help developers reason about and integrate Operon as a publisher; four are marketplace-specific variants of the integration skill that change only the source-attribution string.

## About

Three skills, distributed as plain Markdown files with YAML frontmatter:

1. **`estimate-agent-revenue`** - projects monthly revenue for an agent based on query volume, vertical, and fill rate.
2. **`score-agent-response-quality`** - rates an existing agent response across six dimensions and explains why each score was assigned.
3. **`monetize-agent-responses`** - guided integration of Operon's publisher SDK (generic `@operon/sdk` or ElizaOS `@operon/plugin-publisher-sdk`) into an existing agent. ~10 minute walkthrough on Node 18+.

The four entries under `monetize-agent-responses-variants/` are the same Skill 3 with marketplace-specific source attribution (used so each marketplace gets credit for the install). The canonical version lives at `monetize-agent-responses/SKILL.md`.

Aggregator marketplaces (LobeHub, SkillsMP, FindSkills, MCP Market) auto-index this repo via GitHub crawl. No submission needed; their listings will pick up the canonical skills with `source: skill3-github` attribution.

## Install

### skills.sh

Submit `monetize-agent-responses-variants/skills-sh/SKILL.md` (and the other two canonical skills) via the skills.sh submission flow. The variant uses `source: skill3-skills-sh` for attribution.

### ClawHub

Submit via ClawHub's contributor flow. Use `monetize-agent-responses-variants/clawhub/SKILL.md` for the integration skill.

### agentskill.sh

Submit `monetize-agent-responses-variants/agentskill-sh/SKILL.md` plus the canonical evaluator skills.

### Bankr Skills

Submit `monetize-agent-responses-variants/bankr/SKILL.md` plus the canonical evaluator skills.

### Source-only install

Clone this repo and point your agent at the SKILL.md files directly:

```bash
git clone https://github.com/operonhq/agent-skills.git
```

Then load any `*/SKILL.md` into your agent's skills directory or your tool's skill loader. The frontmatter is stable across loaders that follow the Anthropic Skill convention.

## Source attribution

Each SKILL.md sets a `source` field (in the integration skill's SDK init block) that flows through to placement logs and the publisher dashboard. Canonical: `skill3-github`. Marketplace variants override this so installs from each marketplace carry their own attribution.

If you fork or republish, leave the `source` value alone unless you have a reason to retag (and tell us, so we can wire your attribution string).

## Contributing

Issues and PRs are welcome.

- Bug or copy fix in an existing skill: open a PR against the relevant `SKILL.md`.
- New marketplace variant: copy `monetize-agent-responses/SKILL.md` into a new directory under `monetize-agent-responses-variants/`, change the `source` value in the SDK init snippet (Step 4 + Step 8) and the UTM strings in Step 10, and open a PR.
- Voice rules: hyphens not em dashes, no "this isn't X, this is Y" framing, no marketing-speak. Match the existing tone.

## Links

- Skills landing page: [operon.so/skills](https://operon.so/skills)
- Operon homepage: [operon.so](https://operon.so)
- Publisher SDK on npm: [@operon/sdk](https://www.npmjs.com/package/@operon/sdk)
- ElizaOS plugin: [@operon/plugin-publisher-sdk](https://www.npmjs.com/package/@operon/plugin-publisher-sdk)
- Contact: hi@operon.so

## License

MIT. See [LICENSE](LICENSE).
