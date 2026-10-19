# Career Agent

A personal Career Agent built independently in Python. This repository currently
contains **project structure only**. No discovery, matching, storage, configuration
loading, or automation is implemented.

## Planned scope

V1 will discover jobs through permitted public Greenhouse, Lever, and Ashby ATS
APIs, filter and rank opportunities using candidate preferences, deduplicate
results, and save them to Google Sheets. Provider permissions and usage limits
will be checked when integrations are implemented.

Freelance discovery, outreach, and application preparation are future work.
No code is copied from existing Career Agent projects or Witness MCP.

## Local setup

Use Python 3.11 or newer. From the repository root on macOS or Linux:

```sh
python3 -m venv .venv
source .venv/bin/activate
python -m pip install -r requirements.txt
cp .env.example .env
```

On Windows PowerShell, activate with `.venv\Scripts\Activate.ps1` and copy the
template with `Copy-Item .env.example .env`.

There are no third-party dependencies yet. The package can be imported directly
from the repository root; no packaging or installation framework is required.
There is no application command to run yet, and `.env` is not loaded by any code.
You do not need credentials to review this scaffold.

## File guide

Every Python file below contains only a descriptive module docstring.

| File | Purpose |
| --- | --- |
| `career_agent/__init__.py` | Marks the main Python package. |
| `career_agent/discovery/__init__.py` | Groups future job discovery integrations. |
| `career_agent/discovery/greenhouse.py` | Placeholder for permitted public Greenhouse API discovery. |
| `career_agent/discovery/lever.py` | Placeholder for permitted public Lever API discovery. |
| `career_agent/discovery/ashby.py` | Placeholder for permitted public Ashby API discovery. |
| `career_agent/matching/__init__.py` | Groups future candidate-to-job matching logic. |
| `career_agent/matching/filters.py` | Placeholder for candidate preference filters. |
| `career_agent/matching/ranking.py` | Placeholder for scoring and ordering opportunities. |
| `career_agent/matching/deduplication.py` | Placeholder for recognizing duplicate opportunities. |
| `career_agent/storage/__init__.py` | Groups future persistence integrations. |
| `career_agent/storage/google_sheets.py` | Placeholder for saving results to Google Sheets. |
| `career_agent/config/__init__.py` | Groups future configuration handling. |
| `career_agent/config/settings.py` | Placeholder for loading and validating preferences and environment settings. |
| `tests/README.md` | Explains where future tests belong and how to run them. |
| `requirements.txt` | Reserves one place for dependencies; intentionally contains comments only. |
| `.env.example` | Documents proposed environment variable names using empty values. |
| `.gitignore` | Keeps local environments, secrets, credentials, resumes, and personal data out of Git. |
| `README.md` | Explains scope, setup, structure, and local data handling. |

## Tests

No tests or features are implemented yet. Future tests can use Python's built-in
`unittest` without an additional dependency:

```sh
python -m unittest discover -s tests -p 'test_*.py'
```

At this stage that command discovers zero tests; it does not validate any job
discovery or matching behavior. See `tests/README.md` for the intended layout.

## Local secrets and personal data

Keep actual values in `.env`, credentials in `credentials/`, resumes in
`resumes/`, and candidate preferences or job exports in `data/` or `personal_data/`.
Those local paths are ignored by Git and are not created by this scaffold.
`.env.example` is safe to commit because it contains no real values.

Common credential filenames, key files, and resume filenames are also ignored.
Other personal documents and exports belong in the private directories above. Ignore rules cannot identify every sensitive filename
or remove files already tracked by Git. Review `git status` and your staged diff
before committing, and never use `git add -f` for private files.

All changes are intended for local review before any GitHub push.
