# Configuration

For basic configuration instructions, see [this documentation](https://developers.openai.com/codex/config-basic).

For advanced configuration instructions, see [this documentation](https://developers.openai.com/codex/config-advanced).

For a full configuration reference, see [this documentation](https://developers.openai.com/codex/config-reference).

## Connecting to MCP servers

Codex can connect to MCP servers configured in `~/.codex/config.toml`. See the configuration reference for the latest MCP server options:

- https://developers.openai.com/codex/config-reference

## Notify

Codex can run a notification hook when the agent finishes a turn. See the configuration reference for the latest notification settings:

- https://developers.openai.com/codex/config-reference

## Graphiti memory integration

Codex can optionally ingest and recall conversation turns via Graphiti. Configure it under `[graphiti]` in `~/.codex/config.toml`.

Graphiti requires marking the project trusted and granting explicit consent:

```toml
[projects."/absolute/path/to/your/repo"]
trust_level = "trusted"

[graphiti]
enabled = true
consent = true
endpoint = "http://localhost:8000"
# bearer_token_env_var = "GRAPHITI_BEARER_TOKEN"
group_id_strategy = "hashed" # or "raw"
include_git_metadata = false
include_system_messages = false
# user_scope_key = "me@example.com"

[graphiti.recall]
enabled = true
scopes_mode = "static" # or "auto"
scopes = ["session", "workspace"]

[graphiti.auto_promote]
enabled = false
```

For an end-to-end setup and demo, see `docs/demos/graphiti-memory-integration/README.md`.
