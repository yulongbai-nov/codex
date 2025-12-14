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

```toml
[graphiti]
enabled = true
consent = true
endpoint = "http://localhost:8000"
# bearer_token_env_var = "GRAPHITI_TOKEN"
group_id_strategy = "hashed" # or "raw"

[graphiti.recall]
enabled = true
```

For an end-to-end setup and demo, see `docs/demos/graphiti-memory-integration/README.md`.
