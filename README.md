# Matrix Determinant Tutorial

Interactive Jupyter notebook for visualizing matrix determinants, inverses, and solving linear systems.

## 🧹 Automatic Output Clearing

This workspace is configured to automatically clear Jupyter notebook outputs to keep the repository clean.

### How it works:

1. **VS Code Settings** (`.vscode/settings.json`):
   - Automatically clears outputs when saving notebooks in VS Code
   - Ignores outputs in diff views

2. **Git Hooks with nbstripout**:
   - Automatically strips outputs before every commit
   - Prevents outputs from being committed to the repository

3. **Pre-commit Hooks** (`.pre-commit-config.yaml`):
   - Additional code quality checks
   - Jupyter notebook formatting with Black
   - General file hygiene checks

### 🚀 Setup

1. **Create and activate the conda environment:**
   ```bash
   conda env create -f environment.yml
   conda activate math_env
   ```

2. **Run the setup script:**
   ```bash
   ./setup_notebook_cleaning.sh
   ```

### 🔧 Manual Commands

- **Clear outputs from a specific notebook:**
  ```bash
  nbstripout determinant_inverse_tutorial.ipynb
  ```

- **Clear outputs from all notebooks:**
  ```bash
  nbstripout *.ipynb
  ```

- **Run pre-commit checks manually:**
  ```bash
  pre-commit run --all-files
  ```

- **Check if nbstripout is working:**
  ```bash
  nbstripout --status
  ```

### 📁 Files Added for Output Clearing

- `.vscode/settings.json` - VS Code configuration
- `.pre-commit-config.yaml` - Pre-commit hooks configuration
- `setup_notebook_cleaning.sh` - Setup script
- Updated `environment.yml` - Added nbstripout and pre-commit

### 🎯 What This Prevents

- Large notebook files with embedded outputs
- Merge conflicts from output differences
- Repository bloat from binary image outputs
- Inconsistent notebook states across team members

The notebook will still run normally - outputs are only cleared for storage, not during execution!
