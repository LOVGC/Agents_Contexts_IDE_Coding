---
title: UV Project Configuration Example
type: item
category: Project Setup
raw_source: raw/uv_pytomal.toml
tags:
  - uv
  - pyproject
  - dependencies
  - pytorch
  - cuda
created: 2026-04-13
updated: 2026-04-13
---

## What It Is

An example project configuration showing how to declare a Python project, core dependencies, a CUDA PyTorch index source, and a dev dependency group under `uv`.

## When To Use

Use this when you need a reference for structuring a `uv`-managed Python project with a pinned Python version, scientific Python dependencies, and a custom PyTorch wheel index.

## Key Details

- Defines basic project metadata including name, version, description, readme, and required Python version.
- Includes a scientific Python dependency set with `numpy`, `pandas`, `scikit-learn`, `scipy`, `matplotlib`, `einops`, `tqdm`, and `torch`.
- Configures `torch` to resolve from an explicit `pytorch-cu128` index on Linux and Windows.
- Declares the custom PyTorch package index URL under `tool.uv.index`.
- Adds a `dev` dependency group with `ipykernel` for notebook-oriented development.

## Related Items

- [[raw/use_uv.md]]
- [[wiki/items/uv-project-environment-rule]]
- [[wiki/items/vscode-python-debugger]]
