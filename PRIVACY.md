# Privacy

The Scope Analytics plugin runs entirely on your machine. It launches the
`scope-analytics-mcp` server locally (via `uvx`) and communicates only with the Scope
backend (`https://api.scopeai.dev`) using the API key you provide.

- **Your API key** is stored by Claude Code in secure storage (your system keychain on supported platforms) — not in plaintext config.
- **No data is sent to Anthropic** or any third party by this plugin.
- Requests carry your key only to authenticate to your own Scope project.

Full policy: https://scopeai.dev/privacy-policy · Questions: info@scopeai.dev
