# Scope Analytics — Claude Code plugin

[Scope](https://scopeai.dev) is the **AI analyst for AI products**. This plugin connects
Claude Code to Scope so you can **install** Scope in your project and **ask questions about
your analytics** — user behavior, sessions, and LLM interactions — in natural language,
without leaving your editor.

It bundles the [`scope-analytics-mcp`](https://pypi.org/project/scope-analytics-mcp/) MCP
server, fetched and run on demand via `uvx` (nothing to install first).

## Install

```text
/plugin marketplace add wally827/scope-mcp-plugin
/plugin install scope-analytics-mcp@scopeai
```

When prompted, paste your Scope **secret** key (`sk_...`) — get it from your
[dashboard](https://scopeai.dev). Claude Code stores it in secure storage (your system
keychain on supported platforms), never in plaintext config, and never echoes it into a snippet.

> Requires [`uv`](https://docs.astral.sh/uv/) (which provides `uvx`) and a Scope project
> key — sign up at [scopeai.dev](https://scopeai.dev).

## What you can ask

- *"Use Scope to install analytics in this project."* → detect stack → install → verify
- *"What does Scope cover for my app?"* → coverage report
- *"Ask Scope why signups dropped this week."* → the analyst
- *"Show me what user `u_123` did in their last session."* → a stitched session

The setup tools only **propose** changes — Claude Code shows them and applies them on your
confirmation. Scope never edits your files or account on its own.

## Tools

- **Install / coverage:** `scope_detect_stack`, `scope_install_frontend`, `scope_install_backend`,
  `scope_verify_installation`, `scope_supported_integrations`, `scope_check_integration`,
  `scope_coverage_report`
- **Query:** `scope_ask` (the analyst), `scope_get_stats`, `scope_query_events`,
  `scope_get_session`, `scope_list_metrics`, `scope_get_metric`

## Privacy

Runs locally; talks only to the Scope backend (`api.scopeai.dev`) with your key — no data
goes to Anthropic. See [PRIVACY.md](./PRIVACY.md) and the full
[privacy policy](https://scopeai.dev/privacy-policy).

## Links

- Website — https://scopeai.dev
- Package — https://pypi.org/project/scope-analytics-mcp/
- MCP registry — `io.github.wally827/scope-analytics-mcp`

## License

[MIT](./LICENSE)
