---
title: VS Code Python Debugger Patterns
type: item
category: VS Code / Debugger
raw_source: raw/launch.json
tags:
  - vscode
  - debugger
  - python
created: 2026-04-08
updated: 2026-04-08
---

# VS Code Python Debugger Patterns

## What It Is

A collected `launch.json` snippet that demonstrates three useful Python debugging setups for VS Code.

## When To Use

Use this as a starting point when you need to debug the current file, launch a module or test directly, or run a Python script with command-line arguments and environment variables.

## Key Details

- `Python Debugger: Current File` runs the file that is currently open in VS Code.
- `Debug tests modules` shows how to debug a module entrypoint such as `tests.test_rx_baseband`.
- `Python: train TimesNet Long-Term Forecast (Learning)` shows how to pass CLI arguments and set `CUDA_VISIBLE_DEVICES` inside the debug configuration.

## Related Items

- [[raw/launch.json]]
- [[wiki/index]]
