# Project README

### 0x01. Python - Async

### Learning Objectives

By the end of this project, you should be able to explain:
- `async` and `await` syntax
- How to execute an async program with `asyncio`
- How to run concurrent coroutines
- How to create `asyncio` tasks
- How to use the `random` module

### Requirements

#### General

- A `README.md` file at the root of the project folder
- Allowed editors: `vi`, `vim`, `emacs`
- Interpreted/compiled on Ubuntu 18.04 LTS using `python3` (version 3.7)
- Files end with a new line
- Files must be executable
- First line of files should be `#!/usr/bin/env python3`
- Code should use `pycodestyle` style (version 2.5.x)
- Functions and coroutines must be type-annotated
- Modules should have documentation
- Functions should have documentation

## Tasks

### 0. The basics of async

Write an asynchronous coroutine `wait_random` that waits for a random delay between 0 and `max_delay` seconds and returns it.

### 1. Let's execute multiple coroutines at the same time with async

Write an async routine `wait_n` that spawns `wait_random` `n` times with the specified `max_delay` and returns a list of delays in ascending order.

### 2. Measure the runtime

Create a `measure_time` function that measures the total execution time for `wait_n(n, max_delay)` and returns `total_time / n`.

### 3. Tasks

Write a function `task_wait_random` that returns an `asyncio.Task`.

### 4. Tasks

Alter the code from `wait_n` into a new function `task_wait_n` that calls `task_wait_random`.

For detailed instructions and code implementation, refer to the respective files in the GitHub repository `alx-backend-python` under the directory `0x01-python_async_function`.

Copyright © 2024 ALX, All rights reserved.
