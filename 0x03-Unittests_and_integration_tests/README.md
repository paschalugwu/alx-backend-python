# 0x03. Unittests and Integration Tests

Welcome to the **0x03-Unittests_and_integration_tests** project! This project focuses on mastering unit and integration testing in Python, leveraging the `unittest` framework and various testing techniques. Here's a breakdown of the tasks and key concepts covered in this project.

## Table of Contents

- [Introduction](#introduction)
- [Resources](#resources)
- [Learning Objectives](#learning-objectives)
- [Requirements](#requirements)
- [Tasks](#tasks)
  - [Task 0: Parameterize a Unit Test](#task-0-parameterize-a-unit-test)
  - [Task 1: Parameterize a Unit Test for Exceptions](#task-1-parameterize-a-unit-test-for-exceptions)
  - [Task 2: Mock HTTP Calls](#task-2-mock-http-calls)
  - [Task 3: Parameterize and Patch](#task-3-parameterize-and-patch)
  - [Task 4: Parameterize and Patch as Decorators](#task-4-parameterize-and-patch-as-decorators)
  - [Task 5: Mocking a Property](#task-5-mocking-a-property)
  - [Task 6: More Patching](#task-6-more-patching)
  - [Task 7: Parameterize Tests](#task-7-parameterize-tests)
  - [Task 8: Integration Test Fixtures](#task-8-integration-test-fixtures)
  - [Task 9: Integration Tests](#task-9-integration-tests)
- [Repository Structure](#repository-structure)
- [Authors](#authors)

## Introduction

Unit testing is essential for verifying the correctness of individual functions and methods in isolation, while integration testing ensures that various parts of a codebase work together as expected. This project emphasizes the following:

- Writing efficient and comprehensive unit tests.
- Mocking external dependencies to isolate the functionality under test.
- Parameterizing tests for broader coverage.
- Implementing integration tests to validate end-to-end functionality.

## Resources

- [unittest — Unit testing framework](https://docs.python.org/3/library/unittest.html)
- [unittest.mock — mock object library](https://docs.python.org/3/library/unittest.mock.html)
- [parameterized](https://github.com/wolever/parameterized)
- [Memoization](https://en.wikipedia.org/wiki/Memoization)

## Learning Objectives

By the end of this project, you should be able to:

- Differentiate between unit and integration tests.
- Implement common testing patterns such as mocking, parameterizations, and fixtures.

## Requirements

- Code must be compatible with Python 3.7 on Ubuntu 18.04 LTS.
- Follow the `pycodestyle` style guide (version 2.5).
- All scripts must be executable.
- Include proper documentation for modules, classes, and functions.
- All functions and coroutines should be type-annotated.

## Tasks

### Task 0: Parameterize a Unit Test

**Objective:** Write unit tests for `utils.access_nested_map` using `parameterized.expand`.

**File:** `test_utils.py`

- Create `TestAccessNestedMap` class inheriting from `unittest.TestCase`.
- Implement `test_access_nested_map` method.
- Test the function with different inputs and validate results using `assertEqual`.

### Task 1: Parameterize a Unit Test for Exceptions

**Objective:** Test `utils.access_nested_map` for `KeyError` exceptions.

**File:** `test_utils.py`

- Extend `TestAccessNestedMap` with `test_access_nested_map_exception`.
- Use `assertRaises` to check for `KeyError` on invalid paths.

### Task 2: Mock HTTP Calls

**Objective:** Test `utils.get_json` function without making real HTTP calls.

**File:** `test_utils.py`

- Create `TestGetJson` class.
- Implement `test_get_json` using `unittest.mock.patch` to mock `requests.get`.

### Task 3: Parameterize and Patch

**Objective:** Test memoization functionality in `utils.memoize`.

**File:** `test_utils.py`

- Create `TestMemoize` class.
- Define `TestClass` with memoized property.
- Test that `a_method` is called once even if `a_property` is accessed multiple times.

### Task 4: Parameterize and Patch as Decorators

**Objective:** Test `client.GithubOrgClient.org` method.

**File:** `test_client.py`

- Create `TestGithubOrgClient` class.
- Implement `test_org` method using `@patch` to mock `get_json`.
- Parameterize tests for different organization names.

### Task 5: Mocking a Property

**Objective:** Unit test `GithubOrgClient._public_repos_url`.

**File:** `test_client.py`

- Implement `test_public_repos_url`.
- Mock `GithubOrgClient.org` to return a known payload and validate the URL.

### Task 6: More Patching

**Objective:** Unit test `GithubOrgClient.public_repos`.

**File:** `test_client.py`

- Implement `test_public_repos` using `@patch` for `get_json` and `_public_repos_url`.
- Validate the list of repos returned.

### Task 7: Parameterize Tests

**Objective:** Test `GithubOrgClient.has_license`.

**File:** `test_client.py`

- Implement `test_has_license`.
- Parameterize tests with different license keys and repositories.

### Task 8: Integration Test Fixtures

**Objective:** Integration test `GithubOrgClient.public_repos`.

**File:** `test_client.py`

- Create `TestIntegrationGithubOrgClient` class.
- Use `@parameterized_class` to set up fixtures.
- Mock `requests.get` to return fixture payloads.

### Task 9: Integration Tests

**Objective:** Integration test for public repositories with and without licenses.

**File:** `test_client.py`

- Implement `test_public_repos` and `test_public_repos_with_license`.
- Validate results against fixture data.

## Repository Structure

```bash
0x03-Unittests_and_integration_tests/
├── client.py
├── fixtures.py
├── README.md
├── test_client.py
└── test_utils.py
```

## Authors

*Paschal Ugwu* - [GitHub](https://github.com/Paschalugwu)

---

This project provides a structured approach to mastering unit and integration testing in Python. Ensure all tests pass and adhere to the project requirements. Good luck!
