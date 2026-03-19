


# Predicción de Deserción en Empresas de IT – Proyecto Final Integrador

Este repositorio contiene el desarrollo del Proyecto Final Integrador para el Diplomado en Ciencia de Datos y Análisis Avanzado. El objetivo principal es transformar la gestión de Recursos Humanos (People Analytics) de un modelo reactivo a uno preventivo mediante analítica predictiva, identificando empleados con alta probabilidad de renuncia ($Attrition = Yes$) para reducir la rotación en un 10%.

## Contenido

- `Desercion_IT_project.ipynb`: Notebook Jupyter que contiene todo el flujo del proyecto: limpieza de datos, análisis exploratorio (EDA), balanceo de clases (SMOTE), entrenamiento de modelos y evaluación de métricas de negocio.
- `data/`: Carpeta del dataset (`WA_Fn-UseC_-HR-Employee-Attrition.csv`).
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
3. Instalar los paquetes requeridos:
   ```bash
   pip install pandas numpy scikit-learn matplotlib seaborn imbalanced-learn

(Si utilizas Google Colab, puedes omitir la creación del entorno virtual)

## Guía de Ejecución y Configuración del Entorno

El proyecto ha sido diseñado para ejecutarse de forma flexible, permitiendo su ejecucion tanto en entornos locales como en entornos basados en la nube. Siga las instrucciones según la plataforma de su preferencia:

### Opción A: Google Colab (Entorno Nube)
Esta metodología es ideal para ejecuciones rápidas sin necesidad de configuración local.

1. **Carga del Notebook:** Importe el archivo `Desercion_IT_project.ipynb` a su entorno de Google Colab.
2. **Gestión de Datos:** Localice el panel lateral de "Archivos".
   * Cree una carpeta llamada `data` y cargue el dataset `WA_Fn-UseC_-HR-Employee-Attrition.csv` dentro.
3. **Instalación de Dependencias:** El notebook cuenta con celdas preconfiguradas para instalar librerías externas como `imbalanced-learn` mediante `pip`.
4. **Procesamiento:** Seleccione la opción `Entorno de ejecución > Ejecutar todas` para iniciar el Pipeline de datos.

### Opción B: Visual Studio Code (Entorno Local)

1. **Requisitos de Software:** Es indispensable contar con las extensiones oficiales de **Python** y **Jupyter** desarrolladas por Microsoft.
2. **Selección del Kernel:**
   * Abra el archivo `Desercion_IT_project.ipynb`.
   * En el selector de la esquina superior derecha (`Select Kernel`), vincule el entorno virtual (`env`) donde instaló las dependencias previamente.
3. **Flujo Técnico Interno:** El notebook ejecutará automáticamente las siguientes fases del proyecto:
   * **Ingeniería de Variables:** Codificación de variables categóricas y escalamiento de salarios.
   * **Balanceo de Clases:** Aplicación de la técnica **SMOTE** para corregir el desequilibrio en los datos de deserción.
   * **Modelado Predictivo:** Comparativa de desempeño entre Regresión Logística y Random Forest.
4. **Visualización de Resultados:** Al finalizar, el entorno desplegará las matrices de confusión y el análisis de impacto económico del proyecto.

## Resolución de Problemas: Integridad del Dataset

Si durante la ejecución se detectan errores de ruta o archivos corruptos en el directorio `data/`, proceda con la siguiente solución:

1. **Depuración:** Elimine cualquier archivo residual o dañado dentro de la carpeta `data/`.
2. **Reposición desde Fuente Oficial:** Este proyecto utiliza el dataset de **IBM HR Analytics**. Acceda al repositorio oficial en Kaggle para obtener una copia íntegra: [Kaggle - IBM HR Analytics Dataset](https://www.kaggle.com/datasets/pavansubhasht/ibm-hr-analytics-attrition-dataset).
3. **Restauración:** Tras iniciar sesión y descargar el archivo, coloque el nuevo `.csv` en la carpeta `data/` y reinicie el Kernel del notebook para refrescar el flujo de lectura.

## Resultados Principales
### Análisis de Datos y Metodología
El proyecto se fundamenta en el dataset IBM HR Analytics Employee Attrition & Performance, el cual consta de 1,470 registros y 35 dimensiones. El flujo de trabajo técnico se desglosa en:

1. Saneamiento y Feature Engineering: Eliminación de features con varianza cero y tratamiento de variables categóricas.
2. Tratamiento de Desbalanceo: Implementación de SMOTE para mitigar el sesgo hacia la clase mayoritaria.
3. Modelado Comparativo: Evaluación de arquitecturas de Regresión Logística y Random Forest.
4. Optimización de Métricas: Foco en la maximización del Recall para asegurar la cobertura de la mayor cantidad de casos de deserción reales.

### Evaluación de Resultados e Impacto de Negocio
Tras el proceso de experimentación, se seleccionó el modelo de Regresión Logística debido a su capacidad superior de detección de casos positivos (Recall).

| Métrica | Baseline (Regresión Logística) | Modelo Final (Random Forest) |
| :--- | :---: | :---: |
| Recall | 0.66 | 0.26 |
| F1-Score | 0.46 | 0.34 |
| AUC-ROC | 0.72 | 0.81 |

### Valor Estratégico
La implementación de este modelo permite capturar el 66% de las renuncias potenciales. Considerando un costo de reposición promedio de 6 meses de salario por empleado, se estima un ahorro proyectado de $495,960 USD anuales, bajo un supuesto de efectividad de retención del 50%.

## Citaciones
* Datos: **Kaggle – IBM HR Analytics Employee Attrition & Performance**. 
