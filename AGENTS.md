# Repository notes

- This repository contains independent projects under `viikko1/`, `viikko2/` and `viikko3/`; run each project's `uv` commands from its own directory, not from the repository root.
- Python projects declare their own dependencies in their local `pyproject.toml`; current projects require Python 3.14 or newer. Use each project's lockfile when present.
- `viikko3/login` is a Flask app in `src/`, with Robot Framework Browser tests in `src/tests/`. Start it from `viikko3/login` with `uv run python src/index.py` (port 5001), then in another terminal run `uv run robot src/tests`.
- To run one login browser suite, use `uv run robot src/tests/login.robot` (or `register.robot`, `home.robot`). The browser tests require the server to be running; on a fresh Browser installation, initialize its Playwright dependencies with `uv run rfbrowser init` and `uv run rfbrowser install`.
- In `viikko3/login/src/services/user_service.py`, `UserService.validate` handles registration input validation and `check_credentials` validates login credentials.
