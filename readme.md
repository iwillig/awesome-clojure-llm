[![Awesome](https://cdn.rawgit.com/sindresorhus/awesome/d7305f38d29fed78fa85652e3a63e154dd8e8829/media/badge.svg)](https://github.com/sindresorhus/awesome)

# Awesome Clojure LLM

A curated list of tools, libraries, and resources for using LLMs with Clojure.

## Contents

- [MCP Servers](#mcp-servers)
- [Editor Integrations](#editor-integrations)
- [Libraries](#libraries)
- [CLI Tools](#cli-tools)
- [Prompts & Agents](#prompts--agents)
- [Community](#community)

## MCP Servers

- [clojure-mcp](https://github.com/bhauman/clojure-mcp) - A full-featured MCP server that connects LLM clients (Claude Code, Claude Desktop, etc.) to your Clojure project. Provides REPL integration, Clojure-aware structural editing (via parinfer, cljfmt, clj-rewrite), dispatch agents, and project summary management. Works with both CLI assistants and desktop chat apps.

## Editor Integrations

- [ECA (Editor Code Assistant)](https://github.com/editor-code-assistant/eca) - An editor-agnostic AI code assistant server written in Clojure, inspired by the LSP protocol. Supports chat, rewrite, and completion features with agents/subagents, MCP resources, and OpenTelemetry. Works with Emacs, VS Code, Vim, and IntelliJ. Supports OpenAI, Anthropic, Copilot, Ollama, and more.

## Libraries

- [Bosquet](https://github.com/zmedelis/bosquet) - LLMOps library for building LLM-based applications in Clojure. Provides prompt templating (via Selmer), prompt chaining and composition (via Pathom graph processing), agent and tool abstractions, LLM memory handling, and response caching. Supports OpenAI, Ollama, and tool calling.

## CLI Tools

- [clojure-mcp-light](https://github.com/bhauman/clojure-mcp-light) - Simple CLI tools for LLM coding assistants working with Clojure. Includes `clj-nrepl-eval` for REPL evaluation from the command line, `clj-paren-repair-claude-hook` for automatic delimiter fixing via Claude Code hooks, and `clj-paren-repair` for on-demand parenthesis repair with any LLM that has shell access.
- [ai-investigator](https://github.com/bhauman/ai-investigator) - A Babashka CLI tool that runs Claude, Gemini, and Codex in parallel to investigate problems, then synthesizes their findings with a Claude evaluator. Produces a primary path, backup path, and step-by-step implementation plan.

## Prompts & Agents

- [nucleus-clojure](https://lobehub.com/skills/michaelwhitford-nucleus-nucleus-clojure) - A Clojure-specific AI prompt for LobeHub based on the [Nucleus](https://github.com/michaelwhitford/nucleus) mathematical prompting framework. Designed for use with Clojure REPL tools, it uses symbolic equations to guide AI behavior for REPL-driven development workflows.

## Community

- [#ai-assisted-coding on Clojurians Slack](https://clojurians.slack.com/archives/C068E9L5M2Q) - Active channel for discussing AI-assisted Clojure development.
