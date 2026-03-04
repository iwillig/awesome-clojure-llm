[![Awesome](https://cdn.rawgit.com/sindresorhus/awesome/d7305f38d29fed78fa85652e3a63e154dd8e8829/media/badge.svg)](https://github.com/sindresorhus/awesome)

# Awesome Clojure LLM

A curated list of tools, libraries, and resources for using LLMs with Clojure.

## Contents

- [MCP Servers](#mcp-servers)
- [Editor Integrations](#editor-integrations)
- [Libraries](#libraries)
- [CLI Tools](#cli-tools)
- [Open LLM Harnesses](#open-llm-harnesses)
- [Prompts & Agents](#prompts--agents)
- [Open Weight Models](#open-weight-models)
- [Community](#community)

## MCP Servers

- [Gaiwan MCP SDK](https://github.com/GaiwanTeam/mcp-sdk) - A pure Clojure SDK for building MCP servers with full protocol support (2025-06-18). Supports tools, prompts, resources, and resource templates over both STDIO and HTTP transports. Includes capability negotiation and client notification.
- [MCP Toolkit](https://github.com/metosin/mcp-toolkit) - A Clojure/ClojureScript MCP SDK from Metosin with APIs for both clients and servers. I/O agnostic with Promesa-based async support. Implements tools, prompts, resources, sampling, completion, logging, and more. Includes examples for STDIO and HTTP/SSE transports.
- [PluMCP](https://github.com/plumce/plumcp) - A low-dependency Clojure/ClojureScript library for building MCP clients and servers. Supports nearly all non-deprecated MCP features and transports including OAuth 2.1 with Streamable HTTP. Works across JVM and Node.js runtimes.
- [mcp-clojure-sdk](https://github.com/unravel-team/mcp-clojure-sdk) - A Clojure SDK for creating Model Context Protocol servers. Provides tools, resources, and prompts registration with STDIO transport via core.async. Includes example servers for calculators, Vega-lite charts, and code analysis.
- [clojure-mcp](https://github.com/bhauman/clojure-mcp) - A full-featured MCP server that connects LLM clients (Claude Code, Claude Desktop, etc.) to your Clojure project. Provides REPL integration, Clojure-aware structural editing (via parinfer, cljfmt, clj-rewrite), dispatch agents, and project summary management. Works with both CLI assistants and desktop chat apps.

## Editor Integrations

- [Calva Backseat Driver](https://github.com/BetterThanTomorrow/calva-backseat-driver) - A VS Code extension that gives AI assistants (CoPilot, Cursor, Windsurf, Claude Desktop) access to the Clojure REPL via Calva. Provides tools for code evaluation, structural editing with bracket balancing (via Parinfer), symbol lookup, and clojuredocs.org integration. Also works as an MCP server.
- [ECA (Editor Code Assistant)](https://github.com/editor-code-assistant/eca) - An editor-agnostic AI code assistant server written in Clojure, inspired by the LSP protocol. Supports chat, rewrite, and completion features with agents/subagents, MCP resources, and OpenTelemetry. Works with Emacs, VS Code, Vim, and IntelliJ. Supports OpenAI, Anthropic, Copilot, Ollama, and more.

## Libraries

- [Agent-o-rama](https://github.com/redplanetlabs/agent-o-rama) - An end-to-end LLM agent platform for building, tracing, testing, and monitoring agents with integrated storage and one-click deployment. Provides first-class Java and Clojure APIs, a web UI for traces and experiments, datasets and evaluators, streaming, human-in-the-loop input, time-series telemetry, and online evaluation. Built on Rama.
- [Matryoshka](https://github.com/yogthos/Matryoshka) - Process documents 100x larger than your LLM's context window without vector databases or chunking. Uses a constrained symbolic DSL (Nucleus) where the LLM outputs S-expression commands executed by a logic engine, achieving 97%+ token savings via handle-based storage. Includes an MCP server, REPL, and tree-sitter symbol extraction.
- [Mycelium](https://github.com/yogthos/mycelium) - Schema-enforced, composable workflow components for Clojure designed for LLM agent orchestration. Structures applications as directed graphs of pure data transformations with Malli-validated inputs/outputs. Each cell has a fixed scope so agents never need to see the rest of the application. Includes compile-time validation, hierarchical composition, tracing, and agent brief generation.
- [instructor-clj](https://github.com/unravel-team/instructor-clj) - A Clojure library inspired by [instructor](https://github.com/jxnl/instructor) for getting structured output from LLMs. Define response schemas with Malli, get validated and parsed data back. Supports OpenAI, Anthropic, Gemini, Mistral, Ollama, and OpenRouter via litellm-clj, with automatic retries.
- [DSCloj](https://github.com/unravel-team/DSCloj) - A Clojure library inspired by DSPy for declarative LLM pipeline programming. Define modules with Malli-validated typed inputs/outputs, switch between providers (OpenAI, Anthropic, Gemini, Ollama, etc.) via litellm-clj, and stream structured output with progressive parsing over core.async channels.
- [Bosquet](https://github.com/zmedelis/bosquet) - LLMOps library for building LLM-based applications in Clojure. Provides prompt templating (via Selmer), prompt chaining and composition (via Pathom graph processing), agent and tool abstractions, LLM memory handling, and response caching. Supports OpenAI, Ollama, and tool calling.

## CLI Tools

- [clojure-mcp-light](https://github.com/bhauman/clojure-mcp-light) - Simple CLI tools for LLM coding assistants working with Clojure. Includes `clj-nrepl-eval` for REPL evaluation from the command line, `clj-paren-repair-claude-hook` for automatic delimiter fixing via Claude Code hooks, and `clj-paren-repair` for on-demand parenthesis repair with any LLM that has shell access.
- [ai-investigator](https://github.com/bhauman/ai-investigator) - A Babashka CLI tool that runs Claude, Gemini, and Codex in parallel to investigate problems, then synthesizes their findings with a Claude evaluator. Produces a primary path, backup path, and step-by-step implementation plan.
- [brepl](https://github.com/licht1stein/brepl) - Enables AI-assisted Clojure development by solving the notorious parenthesis problem. It fully supports Claude Code and ECA (Editor Code Assistant) through their hook systems, providing three essential capabilities: Automatic bracket fixing; Simple REPL evaluation; Live file synchronization.

## Open LLM Harnesses

- [opencode](https://opencode.ai/) - An open source coding agent TUI. Supports custom agents, instructions files, and MCP integrations. Works well with Clojure projects via system prompts and clojure-mcp. ([GitHub](https://github.com/anomalyco/opencode))
- [pi](https://github.com/badlogic/pi-mono) - A monorepo of tools for building AI agents and managing LLM deployments. Includes a unified multi-provider LLM API, agent runtime with tool calling, an interactive coding agent CLI, a terminal UI library, and a CLI for managing vLLM deployments on GPU pods.

## Prompts & Agents

- [clojure-system-prompt](https://github.com/iwillig/clojure-system-prompt) - A system prompt for LLM coding assistants optimized for REPL-driven Clojure development. Enforces idiomatic functional patterns, anti-hallucination rules, and REPL-first workflows. Works with pi, opencode, Claude Code skills, and more. Includes prompt compression via LLMLingua.
- [Nucleus](https://github.com/michaelwhitford/nucleus) - A mathematical framework for prompting AI models through symbolic equations. Replaces verbose natural language instructions with compressed mathematical symbols and S-expressions. Includes a Clojure REPL mode (`Human ⊗ AI ⊗ REPL`) and context-switching profiles for different workflows.

## Open Weight Models

Open weight models that work well for Clojure code generation and assistance.

- [Kimi K2.5](https://huggingface.co/moonshotai/Kimi-K2.5) - A large Mixture-of-Experts model from Moonshot AI with strong coding capabilities. Performs well on Clojure tasks including REPL-driven development and functional programming patterns.
- [MiniMax-M2.1](https://huggingface.co/MiniMaxAI/MiniMax-M2.1) - A large Mixture-of-Experts model from MiniMax with strong coding and reasoning capabilities. Performs well on Clojure code generation and functional programming tasks.
- [Qwen3-Coder-Next](https://huggingface.co/Qwen/Qwen3-Coder-Next) - A code-specialized model from Alibaba's Qwen team optimized for code generation, understanding, and agentic coding tasks. Performs well on Clojure development with good support for functional programming idioms.

## Community

- [#ai-assisted-coding on Clojurians Slack](https://clojurians.slack.com/archives/C068E9L5M2Q) - Active channel for discussing AI-assisted Clojure development.
