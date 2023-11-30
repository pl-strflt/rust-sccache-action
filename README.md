> [!WARNING]  
> This project is now deprecated.
>
> Please use [Mozilla-Actions/sccache-action](https://github.com/Mozilla-Actions/sccache-action) instead.

# Rust Shared Compilation Cache Action

The action sets up [sccache](https://github.com/mozilla/sccache) for Rust modules.

## Inputs

| Name | Description | Default |
| --- | --- | --- |
| version | The version of sccache to use | v0.3.1 |
| key | An additional key for the cache | *empty* |
| shared-key | An additional key that is stable over multiple jobs | *empty* |
| skip-save | If set to true, it will use the cache in read-only mode | false |
| autoclean | If set to true, it will use cargo-cache to clean the cache before saving | false |

## Env

| Name | Description | Example |
| --- | --- | --- |
| CACHE_SKIP_SAVE | If set to true, it will use the cache in read-only mode | true |
| SCCACHE_DIR | The path where the sccache should be set up on the runner | ${{ github.workspace }}/.cache/sccache |
| SCCACHE_CACHE_SIZE | The sccache max size limit | 2G |

## Outputs

| Name | Description |
| --- | --- |
| cache-hit | A boolean value to indicate an exact match was found for the key. |
| cache-primary-key | Cache primary key passed in the input to use in subsequent steps of the workflow. |
| cache-matched-key | Key of the cache that was restored, it could either be the primary key on cache-hit or a partial/complete match of one of the restore keys. |

See [actions/cache](https://github.com/actions/cache/blob/64daede5552c68991cba51f3bc0ac2bc26945a11/README.md#environment-variables) and [mozilla/sccache](https://github.com/mozilla/sccache) for a full list of configuration options through environmental variables.
