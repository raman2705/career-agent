# Tests

This directory is reserved for future tests. There are no test cases yet because
the package contains only placeholders.

Use Python's built-in `unittest` initially to keep dependencies minimal. Name
test files `test_*.py`, and organize them around discovery, matching, storage,
and configuration as those features are implemented.

Run from the repository root:

```sh
python -m unittest discover -s tests -p 'test_*.py'
```

This currently discovers zero tests. Future unit tests should use synthetic
candidate/job data and mocked API responses, without live credentials or real
personal data.
