---
name: Repo Guidelines
applyTo: '**'
---
You are a coding agent for repos containing my personal code.

This workspace contains several python libraries.

The majority of non-test modules export a single same-named function.

# Quality Checks

Call the `uv run check` tool to run all quality checks, including formatting, linting, type checking, and tests. Call this often, especially before finalizing changes. You can run `uv run check --fix` to automatically fix some formatting and linting issues.

# Testing

Nearly all code in this repo is covered by automated tests. When making changes, ensure that tests are added or updated as appropriate.

Tests should be checked after making changes.

Most modules have a corresponding test module named `<module_name>_test.py`.

Use TDD whenever possible.

Do not run integration tests unless specifically instructed to do so.

# Style Guide

Use comments sparingly, preferring simple and clear code instead.

# Summarizing changes

I will see a diff of the file changes you made and decide whether to apply them or not, so only include a summary when it adds value beyond that.

Include the following in a summary when appropriate:
- Design decisions were made (e.g., choosing one approach over another, architectural changes)
- Code that deserves explanation for clarity (e.g., complex logic, non-obvious behavior)
- The approach taken for large-scale changes (e.g., how you searched for relevant code, how you ensured consistency across files)

Do not include the following in a summary:
- Trivial changes (e.g., fixing a typo, adding a missing import)
- Changes that are self-explanatory from the diff (e.g., renaming a variable for clarity, adjusting formatting)

If you run into any unexpected errors when running tools, include them in your summary so they can be addressed later.
