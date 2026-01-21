#  Deep Learning para Análisis de Textos: Traducción y NER

Este repositorio contiene el desarrollo de un proyecto de Procesamiento de Lenguaje Natural (NLP) dividido en dos tareas principales: Traducción Automática Neuronal y Reconocimiento de Entidades Nombradas (NER/NEL).

## 📄Descripción del Proyecto

El objetivo principal fue comparar arquitecturas clásicas de Deep Learning (RNN/LSTM) frente a enfoques modernos basados en Transformers y Transfer Learning.

###  Tecnologías utilizadas
* **Lenguaje:** Python
* **Frameworks:** TensorFlow/Keras, SpaCy.
* **Modelos:** LSTM Encoder-Decoder, Transformers (RoBERTa).
* **APIs:** Wikidata (para Entity Linking).
* **Entorno:** Google Colab (GPU T4).

---

##  Parte 1: Traducción Automática (En-Es)

Se desarrolló un sistema de traducción de Inglés a Español utilizando el corpus **TED2020**.

* **Arquitectura:** Modelo Secuencia a Secuencia (Seq2Seq) Encoder-Decoder.
* **Estrategia:** Se comparó un modelo entrenado desde cero (embeddings propios) contra un modelo utilizando **Transfer Learning** con vectores **GloVe (300d)**.
* **Resultados:** El uso de embeddings pre-entrenados aceleró la convergencia y mejoró la coherencia semántica de las traducciones, superando el **60% de precisión** en validación.

##  Parte 2: Reconocimiento de Entidades (NER & NEL)

Se entrenó un modelo para detectar entidades (Personas, Organizaciones, Lugares) sobre el dataset **CoNLL-2003**.

* **Arquitectura:** Se implementó una pipeline basada en **Transformers** (`en_core_web_trf`).
* **Rendimiento:** Se alcanzó un **F-Score del 91.24%**, superando a los modelos estadísticos tradicionales.
* **Entity Linking (NEL):** Se desarrolló un script para conectar las entidades detectadas con **Wikidata** en tiempo real, resolviendo identificadores únicos (ej: *László Krasznahorkai* -> `Q512062`).

##  Contenido del Repositorio
* `PRA2_Final.ipynb`: Notebook completo con todo el código documentado.
* `Informe_Analisis.pdf`: Documento con la justificación teórica y análisis de resultados.

---
*Proyecto realizado como parte de la asignatura de Minería de Textos del Grado en Ciencia de Datos (UOC).*
