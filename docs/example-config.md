# Sample configuration

For a sample configuration file, see [this documentation](https://developers.openai.com/codex/config-sample).

## Graphiti example

```toml
[graphiti]
enabled = true
consent = true
endpoint = "http://localhost:8000"

[graphiti.recall]
enabled = true
```

For an end-to-end setup and demo, see `docs/demos/graphiti-memory-integration/README.md`.
