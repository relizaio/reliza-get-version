# `reliza-get-version`

## About
This action uses the Reliza CLI, [`reliza-cli`](https://github.com/relizaio/reliza-cli), to get the version.

## Usage

Get the version info:

```yaml
steps:
- uses: relizaio/reliza-get-version@1.4
  with:
    reliza_api_id: <api-id-obtained-from-relizahub>
    reliza_api_key: <api-key-obtained-from-relizahub>
```

## Inputs
The actions supports the following inputs:

- `reliza_api_id`: The project API ID obtained from RelizaHub.
- `reliza_api_key`: The project API Key obtained from RelizaHub.
- `ci_metadata`: Metadata for CI run (Optional)
- `path`: Path to the relative to root of the repo (default is '.')
- `reliza_project_id`: Project ID in Reliza Hub to obtain version for in case org-wide api key is used (Optional)

## Outputs
The actions produces the following outputs:

- `reliza_full_version`: Full Version for the new release.
- `reliza_short_version`: Short Version for the new release (this is guaranteed to be compatible with container image tag).
- `reliza_build_start`: Recorded build start time.
- `reliza_do_build`: Flag to control if build should continue.
- `reliza_last_commit`: Last recorded commit prior to the new release.
