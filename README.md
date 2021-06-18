# parallel-bash-commands

A Github Action which executes a list of bash commands in parallel and waits for them all to successfully complete

## Example Usage

**.github/workflows/ci.yml**

<!-- start example-usage -->
```yaml
# ... more CI config ...

jobs:
  primary:
    runs-on: ubuntu-latest
    name: Primary
    steps:
      - uses: actions/checkout@v2

      - name: Run bash commands in parallel
        uses: jameshenry/parallel-bash-commands@v1
        with:
          cmd1: echo hello
          cmd2: echo world

      # ... more CI config ...
```
<!-- end example-usage -->

## Configuration Options

<!-- start configuration-options -->
```yaml
- uses: jameshenry/parallel-bash-commands@v1
  with:
    # Each command is optional and a separate named input with no default value.
    # Currently, up to 10 parallel commands are supported.

    # Optional
    cmd1: ''
    # Optional
    cmd2: ''
    # Optional
    cmd3: ''
    # Optional
    cmd4: ''
    # Optional
    cmd5: ''
    # Optional
    cmd6: ''
    # Optional
    cmd7: ''
    # Optional
    cmd8: ''
    # Optional
    cmd9: ''
    # Optional
    cmd10: ''
```
<!-- end configuration-options -->