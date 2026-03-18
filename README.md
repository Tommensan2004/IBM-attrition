


# Predicción de Deserción en Empresas de IT – Proyecto Final Integrador

Este repositorio contiene el desarrollo del Proyecto Final Integrador para el Diplomado en Ciencia de Datos y Análisis Avanzado. El objetivo principal es transformar la gestión de Recursos Humanos (People Analytics) de un modelo reactivo a uno preventivo mediante analítica predictiva, identificando empleados con alta probabilidad de renuncia ($Attrition = Yes$) para reducir la rotación en un 10%.

## Contenido

- `TPfinal_Test.ipynb`: Notebook Jupyter que contiene todo el ciclo de vida del proyecto: limpieza de datos, análisis exploratorio (EDA), balanceo de clases (SMOTE), entrenamiento de modelos y evaluación de métricas de negocio.
- `data/`: Carpeta destinada a los archivos de datos (ej. `WA_Fn-UseC_-HR-Employee-Attrition.csv`).
- `README.md`: Este archivo, que describe el proyecto, requisitos y resultados principales.

## Requisitos

- **Python 3.11** o superior.
- **Librerías principales:** `pandas`, `numpy`, `scikit-learn`, `matplotlib`, `seaborn`.
- **Librerías de preprocesamiento:** `imbalanced-learn` (para balanceo SMOTE).

## Instalación

1. Clona este repositorio en tu máquina local.
2. Se recomienda crear un entorno virtual:
   ```bash
   python -m venv env
   source env/bin/activate  # En Windows: env\Scripts\activate
