https://www.pyopensci.org/python-package-guide/package-structure-code/python-package-structure.html

## Activate environemnt
python --version
python3 --version
python3 -m pip install --upgrade pip setuptools #global upgrade
python3 -m venv .venv #make venv

source .venv/bin/activate       # for bash shell
source .venv/bin/activate.csh   # for c shell
source .venv/bin/activate.fish  # for fish shell
.\.venv\Scripts\activate        # for powershell

# install editable based on pyproject.toml
pip install -e .[dev]  # install in dev mode, with editable



## Test coverage
pytest --cov=src --cov-report=xml:coverage_reports/coverage.xml --cov-report=html:coverage_reports/htmlcov --cov-report=term tests/

## mdBook
# server view:
mdbook serve ./docs/userguide/ --open
# build the book
mdbook build ./docs/userguide/