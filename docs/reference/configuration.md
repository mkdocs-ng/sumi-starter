---
description: Every option in my-project.toml, with types and defaults.
---

# Configuration

My Project reads `my-project.toml` from the current folder. Environment variables override the file.

```toml title="my-project.toml"
[project]
name = "hello"
output = "build/"
verbose = false
```

| Option | Type | Default | Description |
| --- | --- | --- | --- |
| `name` | string | folder name | Shown in output and logs. |
| `output` | path | `build/` | Where results are written. Created if missing. |
| `verbose` | boolean | `false` | Print every step. Same as `--verbose`. |
| `timeout` | integer | `30` | Seconds before a run is stopped. `0` waits forever. |
{.fields}

## Environment variables

| Variable | Overrides |
| --- | --- |
| `MY_PROJECT_TOKEN` | The API token. Never put it in the file. |
| `MY_PROJECT_OUTPUT` | `output` |
{.fields}
