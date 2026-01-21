# CLAUDE.md

## Project Overview

**aws-claude-skills** - A Claude Code plugin marketplace providing AWS-related plugins:

- **aws-expert**: AWS specialist agent using AWS Knowledge MCP server
- **serverless-dev**: Serverless development skill using AWS SAM

## Structure

```
aws-claude-skills/
├── .claude-plugin/marketplace.json   # Marketplace manifest
├── plugins/
│   ├── aws-expert/                   # Agent-based plugin
│   │   ├── .claude-plugin/plugin.json
│   │   ├── agents/aws-knowledge.md
│   │   └── commands/aws-docs.md
│   └── serverless-dev/               # Skill-based plugin
│       ├── .claude-plugin/plugin.json
│       └── skills/aws-serverless/
└── README.md
```

## Key Files

- **Plugin manifests**: `.claude-plugin/plugin.json` - name, version, description, keywords
- **MCP configs**: `.mcp.json` in each plugin - MCP server definitions
- **Agents**: `agents/*.md` - YAML frontmatter (name, description, model, color) + system prompt
- **Skills**: `skills/*/SKILL.md` - YAML frontmatter + instructions with `reference/` for detailed docs
- **Commands**: `commands/*.md` - YAML frontmatter (name, description, argument-hint, allowed-tools) + instructions

## Repository

GitHub: https://github.com/hustshawn/aws-claude-skills
