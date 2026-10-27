# PDSSP Tutorials

Tutorials for Python projects for PDSSP.

## Use VS Code

Simply sync the environment with `uv` with 

```console
uv sync --all-groups --all-extras
```

Then start editing.

## Launch on JupyterLab

To use `uv` and `jupyterlab` together, sync the environment with `uv`:

```console
uv sync --all-groups --all-extras
```

Then create the kernel for `tutorials` with the following command:

```console
uv run ipython kernel install --user --env VIRTUAL_ENV $(pwd)/.venv --name=tutorials
```

Then start the server:

```console
uv run --with jupyter jupyter lab
```

When creating a notebook, select the `tutorials` kernel from the dropdown. If you need to install a dependency without affecting the `pyproject.toml` file, launch the following in a notebook cell:

```python
!uv pip install <dependency>
```

For more use cases, read the [guide of Jupyter integration in `uv`](https://docs.astral.sh/uv/guides/integration/jupyter/).
