# Sample configuration

For a sample configuration file, see [this documentation](https://developers.openai.com/codex/config-sample).

## Graphiti example

```toml
[projects."/absolute/path/to/your/repo"]
trust_level = "trusted"

[graphiti]
enabled = true
consent = true
endpoint = "http://localhost:8000"
group_id_strategy = "hashed"
ingest_scopes = ["session", "workspace"]

[graphiti.recall]
enabled = true
scopes_mode = "static"
scopes = ["session", "workspace"]
```

For an end-to-end setup and demo, see `docs/demos/graphiti-memory-integration/README.md`.
