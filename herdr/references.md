---
title: "Herdr Research References & Upstream Sources"
type: reference
tags: [herdr, references, sources, documentation, bibliography]
created: 2026-10-21
updated: 2026-10-21
confidence: high
---

# Herdr Research References & Upstream Sources

This annotated bibliography documents all primary sources, official manuals, architecture references, and community guides ingested into this research topic.

---

## 1. Official Herdr Documentation & Specifications

### [Herdr Official Website](https://herdr.dev)
- **URL**: `https://herdr.dev`
- **Scope**: Project homepage, core value proposition, quick-start guide, and binary distribution endpoints.
- **Key Ingested Data**: Product definition, platform support matrix (Linux, macOS, Windows), and default keybindings.

### [Herdr Agent Guide](https://herdr.dev/agent-guide.md)
- **URL**: `https://herdr.dev/agent-guide.md`
- **Scope**: Operational guidance for AI agents interacting with or assisting human operators on Herdr.
- **Key Ingested Data**: Concept hierarchy (Session -> Workspace -> Tab -> Pane -> Agent), first-run walkthrough, and interactive troubleshooting recipes.

### [Herdr LLM Master Index](https://herdr.dev/llms.txt)
- **URL**: `https://herdr.dev/llms.txt`
- **Scope**: Machine-readable index of official documentation for release `v0.9.5`.
- **Key Ingested Data**: Raw documentation links covering agent automation, socket APIs, configuration schemas, machine federation, and session persistence.

### [Herdr Agent Skill Specification](https://raw.githubusercontent.com/herdrdev/herdr/master/skills/herdr/SKILL.md)
- **Local Mirror**: `/Users/amgreer/Documents/personal/genSiFriends/knowledge-base/.agents/skills/herdr/SKILL.md`
- **Scope**: Strict protocol instructions for coding agents operating inside a Herdr-managed pane (`HERDR_ENV=1`).
- **Key Ingested Data**: CLI syntax, layout geometry rules, settled-state wait behaviors (`--wait`), bracketed-paste handling, and safety invariants.

### [Herdr GitHub Repository](https://github.com/herdrdev/herdr)
- **URL**: `https://github.com/herdrdev/herdr`
- **Scope**: Core codebase, socket API schema definitions, and agent detection manifests.

---

## 2. Cloud & Containerized Workspace Architecture

### [Datalumina Learn: Cloud Coding Workspace](https://learn.datalumina.com/docs/cloud-workspace)
- **URL**: `https://learn.datalumina.com/docs/cloud-workspace`
- **Author**: Dave Ebbelaar
- **Scope**: Production deployment guide for running coding agents in remote cloud servers and containerized VPS environments.
- **Key Ingested Data**:
  - Hardened multi-user security model: unprivileged `developer` user, non-root agent execution.
  - SSH key authentication (Ed25519) and IP-restricted firewall rules.
  - Headless daemon operation: decoupling laptop sleep cycles from persistent remote agent sessions.
  - Editor integration: bridging VS Code and Cursor to cloud workspaces over SSH.

---

## 3. Plugin Ecosystem & Security Analyses

### [Bitdoze: Best Herdr Plugins (2026)](https://www.bitdoze.com/best-herdr-plugins/)
- **URL**: `https://www.bitdoze.com/best-herdr-plugins/`
- **Author**: Dragos
- **Published**: October 8, 2026
- **Scope**: Exhaustive technical analysis of the Herdr plugin marketplace, vetting methodologies, and recommended extensions.
- **Key Ingested Data**:
  - The 5-minute plugin vetting checklist: reading manifest `argv` arrays, auditing credential paths, pinning git tags.
  - Breakdown of top 10 plugins: `herdr-reviewr`, `herdr-file-viewer`, `zoetrope`, `herdr-agent-usage`, `herdr-plus`, `herdr-auto-title`, `herdr-navigator`, `herdr-resurrect`, `herdr-plugin-manager`, and `collie`.
  - Plugin architecture mechanics: manifest contract, lifecycle hooks, and injected runtime environment variables (`HERDR_PLUGIN_ROOT` vs `HERDR_PLUGIN_CONFIG_DIR`).

---

## 4. Knowledge Base & Formatting Standards

### [AgentWikis LLM Knowledge Base Standard](https://agentwikis.com/llms.txt)
- **URL**: `https://agentwikis.com/llms.txt`
- **Scope**: Specification for human-readable, AI-optimized research wikis.
- **Key Ingested Data**: Dense informational frontmatter (`title`, `type`, `tags`, `updated`, `sources`), concise hierarchical headings, and top-level index formats.

---

## 5. Local Machine Configurations & Manifests

### User Configuration File
- **Path**: `/Users/amgreer/.config/herdr/config.toml`
- **Contents**: Prefix configuration (`ctrl+space`), popup commands (Lazygit), Catppuccin theme overrides, and `herdr-radar` managed sidebar/tabbar token layouts.

### User Plugin Manifest Registry
- **Path**: `/Users/amgreer/.config/herdr/plugins.json`
- **Contents**: Declarations for installed plugins:
  - `devswha.herdr-web-ui` (v0.3.52)
  - `herdr.auto-title` (v0.14.0)
  - `hhdebb.herdr-radar` (v1.4.8)
  - `nicosuave.memex` (v0.30.0)
  - `nidhi-singh02.agent-router` (v0.1.0)
  - `persiyanov.reviewr` (v0.48.0)

### User Plugin State Cache
- **Path**: `/Users/amgreer/.local/state/herdr/plugins/`
- **Contents**: Dynamic runtime state files, including `hhdebb.herdr-radar/tabbar.txt`.
