This folder holds the project's own Python package, for classes and functions that are reused across notebooks and workflow scripts.

The package lives in `project_package_name/`. Rename the folder and the `name` in `libs/pyproject.toml` when you set up the project, and update the matching entries in the root `pyproject.toml`.

The root `pyproject.toml` installs this package in editable mode through `[tool.uv.sources]`, so `uv sync` from the repository root is all you need. Changes to the code take effect without reinstalling. Import it anywhere in the project:

```python
from project_package_name import some_function
```

Add dependencies that the package itself needs to `libs/pyproject.toml`. Add dependencies that only notebooks or workflow scripts need to the root `pyproject.toml` with `uv add <package>`.
