# NovaMarket-analysis-
Este proyecto es un análisis correlacional (exploratorio)

# 📊 Análisis de Factores de Comportamiento del Cliente — NovaRetail+

[![Python](https://img.shields.io/badge/Python-3.9+-3776AB?style=for-the-badge&logo=python&logoColor=white)](https://www.python.org/)
[![Pandas](https://img.shields.io/badge/Pandas-1.5+-150458?style=for-the-badge&logo=pandas&logoColor=white)](https://pandas.pydata.org/)
[![Seaborn](https://img.shields.io/badge/Seaborn-0.12+-3776AB?style=for-the-badge&logo=python&logoColor=white)](https://seaborn.pydata.org/)
[![Jupyter](https://img.shields.io/badge/Jupyter_Notebook-F37626?style=for-the-badge&logo=jupyter&logoColor=white)](https://jupyter.org/)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg?style=for-the-badge)](https://opensource.org/licenses/MIT)

---

## 📌 Descripción del Proyecto

Este repositorio alberga el análisis exploratorio y estadístico de comportamiento del cliente para la plataforma e-commerce **NovaRetail+**. El estudio evalúa un dataset de 15,000 registros de usuarios para identificar las variables que presentan una correlación directa con el **ingreso anual generado** (`ingreso_anual`).

El objetivo es proveer al equipo de **Crecimiento y Retención** de evidencia cuantitativa para optimizar la toma de decisiones, la inversión en retargeting y la segmentación estratégica.

---

## 🎯 Problema de Negocio

El equipo comercial carecía de visibilidad clara sobre las palancas que realmente impulsan el rendimiento financiero de cada cliente, enfrentando las siguientes preguntas clave:

* ¿El ingreso anual depende principalmente de atributos demográficos (`edad`, `nivel_ingreso`)?
* ¿Existe una relación directa entre la `satisfaccion` percibida y la facturación generada?
* ¿Qué métricas de comportamiento recurrente representan la mayor correlación con los ingresos?

---

## 🛠️ Tecnologías y Herramientas

* **Lenguaje de Programación:** Python 3.9+
* **Entorno de Desarrollo:** Jupyter Notebook
* **Análisis y Manipulación de Datos:** `pandas`, `numpy`
* **Estadística y Modelado:** `scipy.stats` (Matriz de correlación de Pearson)
* **Visualización de Datos:** `matplotlib`, `seaborn`

---

## 📁 Estructura del Repositorio

```text
├── data/
│   └── novaretail_dataset.csv       # Dataset principal (15,000 registros)
├── notebooks/
│   └── novaretail_behavior_eda.ipynb # Notebook con la limpieza, EDA y correlaciones
├── README.md                         # Documentación general del proyecto
└── LICENSE                           # Licencia del repositorio
```

---

## 🔬 Metodología

1. **Auditoría y Limpieza de Datos:**
   * Evaluación de integridad y detección de duplicados/nulos en 15,000 observaciones.
   * Corrección de tipos de datos (conversión del atributo `edad` a número entero).
2. **Análisis Exploratorio de Datos (EDA):**
   * Inspección de distribuciones numéricas, categóricas y binarias.
   * Cálculo de medidas de tendencia central y dispersión.
3. **Análisis de Correlación de Pearson:**
   * Cálculo de la matriz de correlación de Pearson (`df.corr()`).
   * Representación mediante mapas de calor (*heatmaps*) para la identificación de dependencias lineales.

---

## 📈 Resumen de Correlaciones Clave

| Variable Analizada | Correlación con `ingreso_anual` | Impacto / Interpretación |
| :--- | :---: | :--- |
| **`compras_mes`** | **+0.967** | Asociación fuerte y directa (motor principal del ingreso) |
| **`visitas_mes`** | **+0.337** | Asociación moderada positiva con la facturación |
| **`gasto_publicidad_dirigida`** | **+0.579** *(vs. visitas)* | Alta efectividad para incentivar el tráfico a la plataforma |
| **`edad` / `nivel_ingreso`** | **~0.000** | Sin correlación lineal directa con el ingreso anual |
| **`satisfaccion`** | **~0.000** | Sin impacto directo inmediato sobre el volumen de facturación |

---

## 💡 Principales Hallazgos e Insights

* 🛒 **Frecuencia Transaccional como Motor Financiero:** Las `compras_mes` presentan una correlación de **0.967** con el ingreso anual, demostrando que incentivar la recurrencia es la palanca de mayor retorno.
* 🌐 **Efectividad del Retargeting:** La inversión en publicidad dirigida muestra una correlación de **0.579** con la frecuencia de visitas, validando su efectividad para impulsar la actividad en el e-commerce.
* 🎯 **Desmitificación Demográfica:** Factores como la edad, percepción socioeconómica o la satisfacción no garantizan un mayor volumen transaccional por sí solos, sugiriendo que las campañas deben enfocarse en el hábito de compra.

---

## 🚀 Recomendaciones de Negocio

1. **Diseño de Loops de Retención:** Implementar incentivos de compra recurrente (suscripciones, programas de puntos) en lugar de campañas enfocadas únicamente en captación.
2. **Optimización Publicitaria:** Mantener y afinar el presupuesto en `gasto_publicidad_dirigida`, enfocándolo en usuarios con alta intención de visita.
3. **Segmentación por Comportamiento (RFM):** Transicionar de una segmentación demográfica tradicional a una basada en Recencia, Frecuencia y Valor Monetario.

---

## ✒️ Autor

* **Eric Vázquez González** — *Data Analyst*
