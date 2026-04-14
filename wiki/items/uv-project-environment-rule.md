---
title: UV Project Environment Rule
type: item
category: Project Setup
raw_source: raw/use_uv.md
tags:
  - uv
  - python
  - environment
  - workflow
  - dependencies
created: 2026-04-13
updated: 2026-04-13
---

## What It Is

A project setup rule that standardizes Python dependency management and command execution around `uv`.

## When To Use

Use this when bootstrapping or working in a Python repository that should keep one consistent dependency manager and runtime entry point for installs, locking, syncing, and test execution.

## Key Details

- Requires `uv` for managing project dependencies.
- Requires `uv run` for executing Python code and test commands.
- Recommends `uv add` and `uv remove` for dependency changes instead of mixing package managers.
- Includes common commands for initialization, locking, syncing, and running scripts or tests.
- Adds a critical rule that all commands must be run from the project root containing `pyproject.toml` and `uv.lock`.

## Related Items

- [[raw/uv_pytomal.toml]]
- [[wiki/items/uv-project-config-example]]
- [[wiki/items/vscode-python-debugger]]
