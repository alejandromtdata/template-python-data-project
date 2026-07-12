# Plantilla para Proyectos de Análisis de Datos

Esta plantilla la utilizo como punto de partida para todos mis proyectos de **Python + Análisis de Datos**.

Incluye la estructura de carpetas, entorno virtual y dependencias básicas para empezar a trabajar rápidamente.

---

# Flujo recomendado

## 1. Crear un nuevo repositorio en GitHub

Crear el repositorio desde GitHub y clonarlo en el ordenador.

Ejemplo:

```bash
git clone git@github.com:alejandromtdata/NOMBRE_DEL_REPOSITORIO.git

cd NOMBRE_DEL_REPOSITORIO
```

Sustituir **NOMBRE_DEL_REPOSITORIO** por el nombre del proyecto.

---

## 2. Crear el entorno virtual

```bash
python3 -m venv .venv
```

Se crea un entorno virtual independiente para el proyecto.

---

## 3. Activar el entorno virtual

### macOS / Linux

```bash
source .venv/bin/activate
```

### Windows

```bash
.venv\Scripts\activate
```

Si todo ha ido bien aparecerá:

```text
(.venv)
```

al principio de la terminal.

---

## 4. Actualizar pip

```bash
python -m pip install --upgrade pip
```

---

## 5. Instalar las dependencias

```bash
pip install -r requirements.txt
```

---

## 6. Seleccionar el intérprete en VS Code

Abrir la paleta de comandos:

```
Cmd + Shift + P
```

Buscar:

```
Python: Select Interpreter
```

Seleccionar:

```
.venv
```

---

## 7. Crear el notebook

Crear un notebook dentro de:

```
notebooks/
```

Y seleccionar el kernel del entorno virtual.

---

# Estructura del proyecto

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

README.md

requirements.txt
```

---

# Librerías instaladas por defecto

- pandas
- numpy
- matplotlib
- pdfplumber
- ipykernel

Si instalo nuevas librerías:

```bash
pip install nombre_libreria
```

Actualizar requirements:

```bash
pip freeze > requirements.txt
```

---

# Lectura de archivos

## CSV

```python
import pandas as pd

df = pd.read_csv("data/raw/archivo.csv")
```

---

## TXT

```python
from pathlib import Path

texto = Path("data/raw/archivo.txt").read_text(encoding="utf-8")
```

---

## PDF

```python
import pdfplumber

with pdfplumber.open("data/raw/archivo.pdf") as pdf:
    texto = pdf.pages[0].extract_text()
```

---

# Antes del primer commit

- [ ] Entorno virtual creado
- [ ] Dependencias instaladas
- [ ] Intérprete seleccionado
- [ ] Notebook creado
- [ ] README actualizado
- [ ] requirements.txt actualizado
- [ ] Primer commit realizado

---

# Ideas para futuros proyectos

- SQL
- APIs
- Web Scraping
- Power BI
- Machine Learning
- Estadística
- Automatización
