# 🔍 EDA: Análisis Exploratorio de Datos - FinTech Churn

![Jupyter Notebook](https://img.shields.io/badge/Jupyter-Notebook-F37626?style=for-the-badge&logo=jupyter&logoColor=white)
![Pandas](https://img.shields.io/badge/Pandas-150458?style=for-the-badge&logo=pandas&logoColor=white)
![Seaborn](https://img.shields.io/badge/Seaborn-Analysis-blue?style=for-the-badge)

> **Fase 1 del Proyecto FinTech Churn Prediction:** Diagnóstico profundo del comportamiento del cliente y detección de patrones de fuga.

## 📄 Descripción del Análisis

Este notebook documenta el proceso completo de **Investigación de Datos (EDA)** realizado previo al modelado predictivo. El objetivo principal fue transformar datos crudos transaccionales y demográficos en *insights* de negocio accionables, identificando las causas raíz por las cuales los clientes abandonan la plataforma financiera.

A través de análisis univariado, bivariado y multivariado, se establecieron las hipótesis que posteriormente alimentaron el modelo de Machine Learning en producción.

## 🗝️ Hallazgos Clave (Key Insights)

El análisis reveló patrones comportamentales críticos que diferencian a los clientes leales de los que abandonan (Churners):

* 🚨 **El Factor "Silencioso":** La inactividad es el predictor más fuerte. Los clientes con **baja frecuencia de logins** y **muchos días desde su última transacción** tienen una probabilidad de fuga exponencialmente mayor.
* 📞 **La Paradoja del Soporte:** Se encontró una correlación directa entre el número de interacciones con soporte y el abandono, sugiriendo que las incidencias no resueltas son un detonante principal.
* 📉 **Outliers de Riesgo:** Se detectaron anomalías significativas en usuarios con `CreditScore` bajo y `Days_Since_Last_Transaction` alto, perfilándolos como el segmento de mayor riesgo inmediato.
* 🧩 **Segmentación:** Se identificaron clusters de usuarios de alto riesgo basados en la combinación de edad, geografía y número de productos contratados.

## ⚙️ Ingeniería de Características (Feature Engineering)

Para mejorar la capacidad predictiva de los modelos posteriores, se diseñaron nuevas variables sintéticas a partir de los datos existentes:

* `Balance_per_Salary`: Capacidad económica real del cliente.
* `Tenure_per_Age`: Fidelidad relativa a la edad del usuario.
* `Logins_per_Transaction`: Ratio de engagement (uso de la app vs. uso transaccional).

## 🛠️ Estructura del Notebook

1.  **Carga y Limpieza:** Tratamiento de valores nulos, duplicados y tipología de datos.
2.  **Análisis Univariado:** Distribución de variables numéricas y categóricas (Histogramas, Boxplots).
3.  **Análisis Bivariado:** Relación de cada variable con la variable objetivo (`Exited`).
4.  **Detección de Outliers:** Análisis de dispersión para identificar anomalías.
5.  **Matriz de Correlación:** Mapa de calor para detectar multicolinealidad.
6.  **Conclusiones y Siguientes Pasos:** Definición de estrategia para la Fase 2 (Modelado).

## 🚀 Cómo ejecutar este análisis

Necesitarás un entorno con soporte para Jupyter Notebooks.

1.  **Instalar librerías necesarias:**
    ```bash
    pip install pandas numpy matplotlib seaborn
    ```
2.  **Abrir el notebook:**
    ```bash
    jupyter notebook EDAchurnFintech.ipynb
    ```
    *(O cárgalo directamente en Google Colab para una visualización rápida).*

---
**Autor:** [Tu Nombre]
*Este análisis forma parte de la suite de proyectos de Data Science para el sector FinTech.*
