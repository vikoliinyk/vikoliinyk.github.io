---
title: "Keep your code tidy with simple pre-commit hooks"
layout: post
date: 2020-06-02 10:10
<!-- image: /assets/images/markdown.jpg -->
headerImage: false
tag:
- code
star: false
category: blog
author: viktoriiaoliinyk
description: Guidance on basic code quality checks for Data Scientists
---
### Objective
Simple code quality checks allow Data Scientists to mantain good coding practice across the projects.
Below are some pre-commit hooks which enable these checks.

<ul>
    <li><b>Black:</b> a PEP 8 compliant formatter. Refortmats entire files in place</li>
    <li><b>Flake8:</b> verifies PEP8, pyflakes, and circular complexity of the code</li>
    <li><b>End-of-file-fixer:</b> self-explanatory</li>
    <li><b>check-yaml:</b> self-explanatory</li>
    <li><b>trailing-whitespace:</b> self-explanatory</li>
    <li><b>mypy:</b> static type checker. Esures that you're using variables and functions in your code correctly</li>
    <li><b>Order Imports:</b> automatically sorts the Python module imports</li>
</ul>

### Pre-requisities
Make sure you have `pre-commit` installed in your environment. Note `pre-commit` requires `python-3.6+`.

```python
$ pip install pre-commit
```

### Setup
Create `.pre-commit-config.yml` file in the root of your project and add the following configuration to it:

```yml
repos:
-   repo: https://github.com/ambv/black
    rev: stable
    hooks:
    - id: black
      language_version: python3.10 # use your python version here
-   repo: https://github.com/pre-commit/pre-commit-hooks
    rev: v2.3.0
    hooks:
    - id: flake8
    - id: check-yaml
    - id: end-of-file-fixer
    - id: trailing-whitespace
    - id: requirements-txt-fixer
-   repo: https://github.com/asottile/reorder_python_imports
    rev: v2.1.0
    hooks:
    - id: reorder-python-imports
-   repo: https://github.com/pre-commit/mirrors-mypy
    rev: v0.761
    hooks:
    - id: mypy
```

### How to run it
Once you have the pre-commit framework installed and your `.pre-commit-config.yml` file is ready, run `pre-commit install` at the source directory to set up the hooks specified in your configuration file.

Post installation, pre-commit will run automatically on `git commit`. 
Please rectify all code quality issues reported by `flake8`. Others will auto-correct your code.


