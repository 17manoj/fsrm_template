# 💳 Credit Risk Model Cookiecutter Template

A production-ready template for credit risk modeling projects.

---

## 🚀 Quickstart: Using This Template with Cruft

This template leverages [cookiecutter](https://cookiecutter.readthedocs.io/) for project scaffolding and is best managed with [cruft](https://cruft.github.io/cruft/) for easy template updates.

### 1️⃣ Install Cruft

&nbsp;&nbsp;First, install `cruft` (preferably in a virtual environment):

&nbsp;&nbsp;```bash
&nbsp;&nbsp;pip install cruft
&nbsp;&nbsp;```

### 2️⃣ Generate a New Project

&nbsp;&nbsp;Use `cruft` to create a new project from this template:

&nbsp;&nbsp;```bash
&nbsp;&nbsp;cruft create https://github.com/your-username/credit_risk_model.git
&nbsp;&nbsp;```

&nbsp;&nbsp;You will be prompted to enter values for:
&nbsp;&nbsp;  - `project_name`
&nbsp;&nbsp;  - `project_slug`
&nbsp;&nbsp;  - `author_name`
&nbsp;&nbsp;  - `email`
&nbsp;&nbsp;  - `description`
&nbsp;&nbsp;  - `python_version`

&nbsp;&nbsp;These are defined in [`cookiecutter.json`](cookiecutter.json).

### 3️⃣ Set Up Your Project

&nbsp;&nbsp;Navigate into your new project directory:

&nbsp;&nbsp;```bash
&nbsp;&nbsp;cd <your-project-slug>
&nbsp;&nbsp;```

&nbsp;&nbsp;Create a virtual environment and install dependencies:

&nbsp;&nbsp;```bash
&nbsp;&nbsp;make init
&nbsp;&nbsp;```

### 4️⃣ Code Formatting & Linting 🧹

&nbsp;&nbsp;This template uses [Ruff](https://docs.astral.sh/ruff/) for linting and formatting, integrated with [pre-commit](https://pre-commit.com/):

&nbsp;&nbsp;- **Install pre-commit hooks:**

&nbsp;&nbsp;  ```bash
&nbsp;&nbsp;  make precommit-install
&nbsp;&nbsp;  ```

&nbsp;&nbsp;- **Run formatting and linting on all files:**

&nbsp;&nbsp;  ```bash
&nbsp;&nbsp;  make precommit-run
&nbsp;&nbsp;  ```

&nbsp;&nbsp;- On every commit, Ruff will automatically fix formatting issues. ✨

---

## 🗂️ Project Structure Explained

Below is an overview of the generated project structure, with explanations for each key file and folder:

```text
cookiecutter.json
{{cookiecutter.project_slug}}/
├── .gitignore                  # 🚫 Specifies files and folders to be ignored by git
├── .pre-commit-config.yaml     # 🔄 Configuration for pre-commit hooks (e.g., Ruff)
├── Dockerfile                  # 🐳 Instructions to build a Docker image for the project
├── Makefile                    # 🛠️ Automation commands (setup, linting, testing, etc.)
├── pyproject.toml              # ⚙️ Project metadata and tool configuration (e.g., Ruff, pytest)
├── README.md                   # 📖 Project documentation (you're reading it!)
├── requirements.txt            # 📦 Python dependencies for the project
├── setup.py                    # 📦 Setup script for packaging and installation
├── .github/
│   ├── pull_request_template.md    # 🔀 Template for pull requests
│   └── ISSUE_TEMPLATE/            # 📝 Templates for GitHub issues
│       └── ...                    # (bug reports, feature requests, etc.)
│   └── workflows/
│       └── lint-and-test.yml      # 🤖 GitHub Actions workflow for CI (linting and testing)
├── config/                    # ⚙️ Configuration files (YAML, JSON, etc.)
├── data/
│   ├── interim/               # 🕓 Intermediate data that has been transformed
│   ├── processed/             # ✅ Final, cleaned data ready for modeling
│   └── raw/                   # 📥 Original, immutable data dump
├── models/                    # 🧠 Trained models and serialized model artifacts
├── notebooks/                 # 📓 Jupyter notebooks for exploration and analysis
├── reports/
│   └── figures/               # 📊 Generated plots and figures for reporting
├── src/
│   ├── __init__.py            # 📦 Marks the directory as a Python package
│   ├── data/                  # 📂 Data loading and preprocessing scripts
│   ├── features/              # 🏗️ Feature engineering scripts
│   ├── models/                # 🤖 Model training and evaluation code
│   └── utils/                 # 🛠️ Utility functions and helpers
└── tests/
    └── test_sample.py         # 🧪 Example unit test using pytest
```

### 📂 Folder & File Purpose

- **cookiecutter.json**:  
  &nbsp;&nbsp;Defines the template variables for project generation.
- **.gitignore**:  
  &nbsp;&nbsp;Prevents sensitive or unnecessary files from being tracked by git.
- **.pre-commit-config.yaml**:  
  &nbsp;&nbsp;Automates code formatting and linting before commits.
- **Dockerfile**:  
  &nbsp;&nbsp;Enables containerized development and deployment.
- **Makefile**:  
  &nbsp;&nbsp;Simplifies common tasks (setup, linting, testing) with `make` commands.
- **pyproject.toml**:  
  &nbsp;&nbsp;Centralizes configuration for Python tools and dependencies.
- **README.md**:  
  &nbsp;&nbsp;Provides project overview, setup, and usage instructions.
- **requirements.txt**:  
  &nbsp;&nbsp;Lists Python packages required for the project.
- **setup.py**:  
  &nbsp;&nbsp;Allows the project to be installed as a package.
- **.github/**:  
  &nbsp;&nbsp;Contains GitHub-specific templates and CI/CD workflows.
- **config/**:  
  &nbsp;&nbsp;Stores configuration files for experiments or environments.
- **data/**:  
  &nbsp;&nbsp;Organizes datasets into raw, interim, and processed stages.
- **models/**:  
  &nbsp;&nbsp;Stores trained models and related artifacts.
- **notebooks/**:  
  &nbsp;&nbsp;Houses Jupyter notebooks for prototyping and analysis.
- **reports/**:  
  &nbsp;&nbsp;Contains generated reports and visualizations.
- **src/**:  
  &nbsp;&nbsp;Main source code, organized by functionality (data, features, models, utils).
- **tests/**:  
  &nbsp;&nbsp;Unit and integration tests to ensure code quality.

---

> 💡 **Tip:**  
> Each folder is designed to separate concerns and promote best practices for reproducible, maintainable data science and machine learning projects.

---

### 5️⃣ Running Tests 🧪

&nbsp;&nbsp;Tests are located in the [`tests/`](tests/) directory and use [pytest](https://docs.pytest.org/):

&nbsp;&nbsp;```bash
&nbsp;&nbsp;pytest
&nbsp;&nbsp;```

### 6️⃣ Using Docker (Optional) 🐳

&nbsp;&nbsp;A [Dockerfile](Dockerfile) is provided for containerized development:

&nbsp;&nbsp;```bash
&nbsp;&nbsp;docker build -t my-credit-risk-model .
&nbsp;&nbsp;docker run -it my-credit-risk-model
&nbsp;&nbsp;```

---

## 🛠️ Updating Your Project with Cruft

If the template is updated, you can update your project with:

&nbsp;&nbsp;```bash
&nbsp;&nbsp;cruft update
&nbsp;&nbsp;```

---

## 📄 License

This template is provided under the MIT License.

---

## 🙋 Need Help?

- [Cookiecutter Documentation](https://cookiecutter.readthedocs.io/) 🍪
- [Cruft Documentation](https://cruft.github.io/cruft/) 🧰
- [Ruff Documentation](https://docs.astral.sh/ruff/) 🐕