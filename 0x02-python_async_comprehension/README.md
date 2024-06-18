# Project: Python Async Comprehension

## Overview
This project focuses on understanding and implementing asynchronous generators, async comprehensions, and measuring runtime for parallel comprehensions in Python.

## Learning Objectives
By the end of this project, you should be able to:
- Explain how to write an asynchronous generator
- Demonstrate the usage of async comprehensions
- Understand how to type-annotate generators

## Requirements
### General
- Editors: `vi`, `vim`, `emacs`
- Environment: Ubuntu 18.04 LTS with Python 3.7
- Code style: `pycodestyle` (version 2.5.x)
- File endings: All files should end with a new line
- Shebang line: First line of all files should be `#!/usr/bin/env python3`
- Mandatory `README.md` file at the root of the project folder
- Documentation: All modules and functions must be documented with real sentences
- Type annotations: All functions and coroutines must be type-annotated

## Tasks
### Task 0: Async Generator
- Implement a coroutine `async_generator` that yields random numbers asynchronously.
- Utilize the `random` module for generating random numbers.
- File: `0-async_generator.py`

### Task 1: Async Comprehensions
- Import `async_generator` from Task 0 and create a coroutine `async_comprehension` to collect 10 random numbers.
- Use async comprehensions over `async_generator` to gather the random numbers.
- File: `1-async_comprehension.py`

### Task 2: Run time for four parallel comprehensions
- Import `async_comprehension` from Task 1 and create a `measure_runtime` coroutine.
- Execute `async_comprehension` four times in parallel using `asyncio.gather` and measure the total runtime.
- File: `2-measure_runtime.py`

## Repository Information
- GitHub repository: `alx-backend-python`
- Directory: `0x02-python_async_comprehension`

Copyright © 2024 ALX. All rights reserved.
