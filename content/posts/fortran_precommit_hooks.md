---
layout: post
title: Useful pre-commit hooks for Fortran projects
tags: fortran git
category: development
draft: true
---

The contents of the `.pre-commit-config.yaml` file:

```yaml
repos:
-   repo: https://github.com/ambv/black
    rev: stable
    hooks:
    - id: black

-   repo: https://github.com/pseewald/fprettify
    rev: v0.3.4
    hooks:
    - id: fprettify
      args: ['--indent', '2']
```