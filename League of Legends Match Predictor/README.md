# League of Legends Match Predictor 

Este proyecto utiliza **Deep Learning (PyTorch)** para predecir el resultado de partidas de League of Legends basándose en estadísticas en tiempo real (oro, muertes, torres, etc.).

##  Descripción
El objetivo es construir y entrenar un modelo de **Regresión Logística** utilizando redes neuronales para clasificar si un equipo ganará o perderá una partida.

##  Tecnologías utilizadas
* **Python**
* **PyTorch** (nn.Module, Optimizers, Loss Functions)
* **Pandas & NumPy** (Procesamiento de datos)
* **Scikit-learn** (Escalado y métricas)
* **Matplotlib & Seaborn** (Visualización de resultados)

##  Pasos del Proyecto
1. **Preprocesamiento:** Limpieza de datos y normalización con `StandardScaler`.
2. **Arquitectura:** Implementación de una red neuronal lineal con activación Sigmoide.
3. **Entrenamiento:** Optimización mediante SGD (Stochastic Gradient Descent).
4. **Evaluación:** Análisis de precisión y generación de **Matriz de Confusión**.
5. **Análisis:** Identificación de las variables más influyentes (Feature Importance).

##  Resultados
El modelo logra identificar patrones clave, siendo la **Diferencia de Oro** y el **Control de Objetivos** los factores más determinantes para predecir la victoria.

##  Cómo ejecutarlo
1. Clona el repositorio.
2. Asegúrate de tener instalado PyTorch y Pandas:
   ```bash
   pip install torch pandas scikit-learn matplotlib seaborn
