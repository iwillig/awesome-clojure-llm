[![Awesome](https://cdn.rawgit.com/sindresorhus/awesome/d7305f38d29fed78fa85652e3a63e154dd8e8829/media/badge.svg)](https://github.com/sindresorhus/awesome)

# Awesome Clojure LLM

A curated list of tools, libraries, and resources for using LLMs with Clojure.

## Contents

- [MCP Servers](#mcp-servers)
- [CLI Tools](#cli-tools)
- [Community](#community)

## MCP Servers

- [clojure-mcp](https://github.com/bhauman/clojure-mcp) - A full-featured MCP server that connects LLM clients (Claude Code, Claude Desktop, etc.) to your Clojure project. Provides REPL integration, Clojure-aware structural editing (via parinfer, cljfmt, clj-rewrite), dispatch agents, and project summary management. Works with both CLI assistants and desktop chat apps.

## CLI Tools

- [clojure-mcp-light](https://github.com/bhauman/clojure-mcp-light) - Simple CLI tools for LLM coding assistants working with Clojure. Includes `clj-nrepl-eval` for REPL evaluation from the command line, `clj-paren-repair-claude-hook` for automatic delimiter fixing via Claude Code hooks, and `clj-paren-repair` for on-demand parenthesis repair with any LLM that has shell access.
- [ai-investigator](https://github.com/bhauman/ai-investigator) - A Babashka CLI tool that runs Claude, Gemini, and Codex in parallel to investigate problems, then synthesizes their findings with a Claude evaluator. Produces a primary path, backup path, and step-by-step implementation plan.

## Community

- [#ai-assisted-coding on Clojurians Slack](https://clojurians.slack.com/archives/C068E9L5M2Q) - Active channel for discussing AI-assisted Clojure development.
