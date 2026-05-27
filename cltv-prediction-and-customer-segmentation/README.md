#  Predicción de Customer Lifetime Value (CLTV) y Recompra

Bienvenido/a a este proyecto de analítica avanzada de clientes. En este repositorio se aborda la resolución de un problema de negocio real utilizando técnicas de análisis exploratorio, segmentación y Machine Learning para predecir el comportamiento futuro de los consumidores.

Este trabajo fue desarrollado como parte de la evaluación continua de la asignatura Analítica de Clientes.

---

##  Descripción del Proyecto

El objetivo principal es estimar el valor que los clientes aportarán a la empresa durante su relación comercial (CLTV) y predecir su probabilidad de volver a comprar. Esto permite a los equipos de marketing adelantarse a las necesidades de los usuarios, optimizar el CPA (Coste Por Adquisición) y diseñar estrategias personalizadas priorizando a los grupos de mayor valor.

###  Fases del Proyecto:
1. **Análisis Exploratorio de Datos (EDA):** Limpieza, tratamiento de outliers y análisis temporal/demográfico del comportamiento de compra físico y online.
2. **Ingeniería de Características y Clustering:** Cálculo de variables RFM (Recency, Frequency, Monetary) y segmentación de clientes mediante el algoritmo K-Means ($k=3$) para identificar perfiles VIP y en riesgo.
3. **Modelado Predictivo:** Entrenamiento y evaluación de algoritmos basados en árboles (Random Forest, XGBoost y LightGBM) para predecir la recompra.
4. **Explicabilidad (XAI):** Interpretación del modelo "caja negra" mediante Feature Importance, valores SHAP, Partial Dependence Plots (PDP) y un modelo sustituto (Surrogate Tree).
5. **Gobernanza y Ética (AI Act):** Análisis de las implicaciones legales y éticas del sistema, sesgos, minimización de datos y discriminación indirecta según el marco normativo europeo.

---

##  Tecnologías y Librerías Utilizadas

* **Lenguaje:** Python
* **Manipulación de Datos:** `pandas`, `numpy`
* **Visualización:** `plotly.express`, `matplotlib`, `shap`
* **Machine Learning:** `scikit-learn`, `xgboost`, `lightgbm`

---

##  Resultados Clave

* **Segmentación:** Se identificó a un grupo selecto de **524 clientes "High" (VIP)** con una frecuencia de compra excepcional (12.5 veces) y un gasto medio que dobla al resto de segmentos.
* **Modelo Ganador:** **LightGBM** obtuvo el mejor rendimiento global con un **Recall del 93%** para la clase positiva (identificando a los clientes que vuelven a comprar) y un **AUC de 0.640**.
* **El factor decisivo:** Gracias al análisis con SHAP, se demostró que la variable **Recency** (días desde la última compra) es, con gran diferencia, el predictor más importante del comportamiento futuro del cliente.

---

##  Estructura del Repositorio

* `clientes4_davidmestres_v2.ipynb`: Notebook completo con el código fuente ejecutado paso a paso.
* `clientes4_davidmestres_v2.html`: Versión exportada del notebook para una visualización rápida de las gráficas interactivas.
* `*.csv`: Datasets crudos utilizados para el análisis (recibos de ventas, información de clientes y objetivos comerciales).

---

*Proyecto desarrollado por David Mestres*
