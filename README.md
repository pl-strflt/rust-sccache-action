# Rust Shared Compilation Cache Action

The action sets up [sccache](https://github.com/mozilla/sccache) for Rust modules.

The action requires `GITHUB_TOKEN` to be set in env.

## Inputs

| Name | Description | Default |
| --- | --- | --- |
| version | The version of sccache to use | v0.2.15 |
| key | An additional key for the cache | *empty* |
| shared-key | An additional key that is stable over multiple jobs | *empty* |
