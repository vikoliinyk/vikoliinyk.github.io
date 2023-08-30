---
title: "Basic code quality checks"
layout: post
date: 2020-06-02 10:10
<!-- image: /assets/images/markdown.jpg -->
headerImage: false
tag:
- code
star: false
category: blog
author: viktoriiaoliinyk
description: Introduction to fair and ethical AI
---
### Objective
Code quality checks before code check-in will enable us manage standard coding practice across the repository.
We would be leveraging pre-commit hooks for the following code quality checks:

<ul>
    <li>Black: Automated code formatting</li>
    <li>Flake8: Code quality check</li>
    <li>End-of-file-fixer: (self explanatory)</li>
    <li>check-yaml: (self explanatory)</li>
    <li>trailing-whitespace: (self explanatory)</li>
    <li>mypy</li>
    <li>Order Imports</li>
    <li>Pre-requisities</li>
    <li>Pre-commit requires python3.6+, hence we are migrating to python3.7 to have compatibility with Databricks Runtime 6.1</li>
</ul>

### Setup
Pre-commit config

```yml
repos:
-   repo: https://github.com/ambv/black
    rev: stable
    hooks:
    - id: black
      language_version: python3.7
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



