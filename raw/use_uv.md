# Project Environment Rule

Must use `uv` for managing the Python project.

* Use `uv` to manage dependencies
* Must Use `uv run` to execute Python code
* Use `uv add/remove` to add/remove dependencies 

## Common `uv` commands
The followings are some examples for using uv:
```bash
# initialize project
uv init

# add / remove dependencies
uv add <package>
uv add --dev <package>
uv remove <package>

# lock & sync environment
uv lock
uv sync

# run code
uv run python script.py
uv run pytest
```

## Working Directory (CRITICAL)
ALL commands MUST be executed from the project root directory
(the directory containing `pyproject.toml` and `uv.lock`).

Running `uv run ...` outside the project root is NOT allowed,
as it may resolve to a different environment.



