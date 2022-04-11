# Rust Shared Compilation Cache Action

The action sets up [sccache](https://github.com/mozilla/sccache) for Rust modules.

## Inputs

| Name | Description | Default |
| --- | --- | --- |
| version | The version of sccache to use | v0.2.15 |
| key | An additional key for the cache | *empty* |
| shared-key | An additional key that is stable over multiple jobs | *empty* |
