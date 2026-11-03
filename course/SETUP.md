# Setup Guide (Windows, about 10 minutes)

You need: Python 3.12, a few libraries, and VS Code with notebook support.

**Analogy:** **uv** is a **kitchen manager**. It fetches the right version of Python (the stove). It also gives each project its own **lunchbox** of libraries (a *virtual environment*, the `.venv` folder), so projects never spill into each other.

Open a terminal in VS Code with **Ctrl + `** and run each step. Check the ✅ result before moving on.

## 1. Install uv
```powershell
winget install --id=astral-sh.uv -e
```
**Close the terminal and open a new one** so Windows can find the new command. Then check:
```powershell
uv --version
```
✅ You see something like `uv 0.x.x`.

## 2. Install Python 3.12
```powershell
uv python install 3.12
```
✅ You see `Installed Python 3.12.x`.

## 3. Make the course folder a project
Go to the course folder, then run:
```powershell
uv init --bare --python 3.12
```
✅ This creates `pyproject.toml`, the project's "shopping list" of libraries.

## 4. Add the libraries
```powershell
uv add numpy matplotlib ipykernel
```
- `numpy` handles fast math on lists of numbers.
- `matplotlib` draws plots.
- `ipykernel` lets notebooks run your Python.

✅ This creates a `.venv` folder.

## 5. Test it
```powershell
uv run python -c "import numpy, matplotlib; print('ready', numpy.__version__)"
```
✅ You see `ready 2.x.x`.

## 6. VS Code extensions
Open the Extensions panel (**Ctrl+Shift+X**) and install two extensions, both by Microsoft:
- **Python**
- **Jupyter**

## 7. Run your first notebook
1. In the Explorer sidebar, hover over the project folder's name and click **New File**. Name it `test.ipynb`, in the top folder of the project.
2. Click **Select Kernel** (top right), then **Python Environments**, then pick the one in **`.venv`**.
3. In the first cell, type `print("hello ML")` and press **Shift+Enter**.

✅ You see `hello ML` under the cell. You can delete `test.ipynb` now.

> GPU support (PyTorch with CUDA) is set up later, in Part 4. You don't need it before then.
