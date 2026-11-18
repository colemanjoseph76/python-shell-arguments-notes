# Parse shell-like arguments: implementation

## What the example does

shlex.split handles shell-like quoting but does not execute anything. Shell substitutions and redirections remain text; do not pass the result to a shell.

The public function is `solve(value)`. The JSON input contract can be seen in this concrete example:

```json
"tool --name \"Ada Lovelace\""
```

Expected result:

```json
[
  "tool",
  "--name",
  "Ada Lovelace"
]
```

Run `python3 example.py` for the Python representation of the result. `solution.py` contains the full implementation and can also be imported by another script.

## Scope

The function implements exactly the behavior described above. It does not perform network or filesystem access. Python exceptions indicate unsupported input; the next lesson turns them into a command-line error response. Review the limitations before reusing it in an application.
