# Plantilla analisis de datos

## Proyecto de Análisis de Datos — practica_io_textos

Plantilla base para proyectos de análisis de datos en **Python**, utilizando entornos virtuales y notebooks de **Jupyter / VS Code**.

---

## Configuración del entorno

### Clonar el repositorio

git clone git@github.com:alejandromtdev/plantilla_datascience.git
cd plantilla_datascience

---

### Creación y activación del entorno virtual 

python3 -m venv .venv
source .venv/bin/activate
python -m pip install --upgrade pip
pip install -r requirements.txt

---

### Actualizar pip

python -m pip install --upgrade pip

---

### Instalar las dependencias

pip install -r requirements.txt

---

### Dependencias principales 
### El archivo requirements.txt incluye las librerías necesarias:

pandas
numpy
matplotlib
pdfplumber
ipykernel

---

### Ejemplo de lectura de datos en un notebook:

import pandas as pd
from pathlib import Path
import pdfplumber

---

### Leer CSV
df = pd.read_csv("data/raw/archivo.csv")

---

### Leer TXT
texto = Path("data/raw/archivo.txt").read_text(encoding="utf-8")

---

### Leer PDF
with pdfplumber.open("data/raw/archivo.pdf") as pdf:
    texto_pdf = pdf.pages[0].extract_text()

---

### Proyecto creado por Alejandromtdev como plantilla base para análisis de datos con Python y VS Code.

📬 Contacto: alejandromtdev@gmail.com

💻 GitHub: https://github.com/alejandromtdev