# Python Data Project Template

This repository is my personal template for starting new Python Data Analytics projects.

It includes the recommended folder structure, a virtual environment, dependencies and basic configuration to start working quickly.

---

# Recommended Workflow

## 1. Create a new repository on GitHub

- Create a new repository.
- Clone it locally.

Example:

```bash
git clone git@github.com:YOUR_USERNAME/YOUR_REPOSITORY.git

cd YOUR_REPOSITORY
```

Replace:

- `YOUR_USERNAME` → your GitHub username.
- `YOUR_REPOSITORY` → the name of your new project.

---

## 2. Create the virtual environment

```bash
python3 -m venv .venv
```

This creates an isolated Python environment for the project.

---

## 3. Activate the virtual environment

### macOS / Linux

```bash
source .venv/bin/activate
```

### Windows

```bash
.venv\Scripts\activate
```

When activated, your terminal should display:

```text
(.venv)
```

---

## 4. Update pip

```bash
python -m pip install --upgrade pip
```

---

## 5. Install project dependencies

```bash
pip install -r requirements.txt
```

---

## 6. Select the Python interpreter in VS Code

Open Command Palette:

```
Cmd + Shift + P
```

Search:

```
Python: Select Interpreter
```

Choose:

```
.venv
```

---

## 7. Start Jupyter

Create a notebook inside:

```
notebooks/
```

Select the kernel:

```
.venv
```

---

# Project Structure

```text
data/
│
├── raw/
└── processed/

docs/

notebooks/

reports/

src/

tests/

requirements.txt

README.md
```

---

# Installed Libraries

- pandas
- numpy
- matplotlib
- pdfplumber
- ipykernel

Add new libraries when needed:

```bash
pip install library_name
```

Update requirements:

```bash
pip freeze > requirements.txt
```

---

# Reading Files

## CSV

```python
import pandas as pd

df = pd.read_csv("data/raw/file.csv")
```

---

## TXT

```python
from pathlib import Path

text = Path("data/raw/file.txt").read_text(encoding="utf-8")
```

---

## PDF

```python
import pdfplumber

with pdfplumber.open("data/raw/file.pdf") as pdf:
    text = pdf.pages[0].extract_text()
```

---

# Before the First Commit

- [ ] Virtual environment created
- [ ] Dependencies installed
- [ ] Interpreter selected
- [ ] Notebook created
- [ ] README updated
- [ ] requirements.txt updated
- [ ] First commit completed
