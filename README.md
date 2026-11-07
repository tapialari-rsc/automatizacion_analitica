# ⚽ Automatización Analítica y Modelo de Clasificación de Gestión Deportiva: Caso River Plate (2024-2026)

## 📌 Descripción del Proyecto
Este proyecto consiste en el diseño y desarrollo de un **prototipo automatizado de punta a punta (End-to-End Data Pipeline)** para recopilar, procesar, analizar y visualizar el rendimiento deportivo y económico del Club Atlético River Plate durante el período 2024-2026. 

A través de técnicas de **Web Scraping** e **Inteligencia Artificial**, el sistema consolida un historial de aproximadamente 150 partidos oficiales para ejecutar un **Modelo de Clasificación**. El objetivo principal es evaluar la consistencia institucional y predecir probabilísticamente si una temporada o gestión se cataloga bajo una etiqueta categórica discreta: **"Exitosa"** o **"Deficitaria"**, cruzando las variables de rendimiento técnico en cancha con el balance financiero del mercado de pases.

---

## 🎯 Preguntas de Negocio y Objetivos Estratégicos
El modelo actúa como una herramienta estratégica de toma de decisiones para la comisión directiva y la secretaría técnica, respondiendo a interrogantes clave:
*   ¿El mercado de pases de las últimas tres temporadas fue deficitario o presentó superávit?
*   ¿La gestión económica del club se condice directamente con el rendimiento deportivo en el campo?
*   **Optimización del Gasto:** Predecir perfiles de fichajes eficientes para evitar inversiones de alto riesgo (superiores a los 50M USD) guiadas por impulsos subjetivos.
*   **Mitigación de Riesgos:** Funcionar como un "sistema de alerta temprana" financiero ante eliminaciones prematuras en copas internacionales.

---

## ⚙️ Arquitectura del Flujo de Trabajo (Data Pipeline)
La solución implementa una infraestructura de automatización secuencial en la nube desarrollada sobre la plataforma **Make**, estructurada en 4 etapas críticas:

<p align="center">
<img width="1542" height="688" alt="make" src="https://github.com/user-attachments/assets/e3ab31aa-6b07-4008-ae43-490b6f6fc6c9" />
</p>

1.  **Extracción (Input):** Recuperación automatizada de datos crudos centralizados en `Google Sheets` extraídos originalmente del portal *Transfermarkt* (variables de contexto como localía, esquema táctico, y estadísticas de rendimiento como posesión, tiros al arco y faltas).
2.  **Consolidación y Preprocesamiento:** Implementación de componentes intermedios (`Tools - Text aggregator`) para unificar registros dispersos en un único bloque estructurado y optimizar la eficiencia de las solicitudes de análisis.
3.  **Motor Cognitivo (Machine Learning):** Ejecución del modelo probabilístico de clasificación a través de la API de `OpenAI (ChatGPT, Whisper)`. El algoritmo evalúa los pesos de las variables técnicas para determinar la probabilidad de éxito de la gestión (ej. `0.61 vs 0.39`).
4.  **Visualización (Output):** Traducción dinámica de las probabilidades numéricas abstractas en reportes gráficos (gráficos de dona) mediante la API de `QuickChart`, generando una URL única de consumo ejecutivo.

---

## 📊 Propuesta Conceptual de Machine Learning
*   **Tipo de Problema:** Clasificación binaria (Etiquetas discretas: *Exitosa* / *Deficitaria* o *Triunfo* / *Derrota*).
*   **Unidad de Análisis:** ~150 partidos oficiales de fútbol masculino profesional de la octava generación.
*   **Matriz de Características (Features):**
    *   *Variables de Contexto:* Localía, Competencia, Esquema táctico empleado.
    *   *Variables de Rendimiento:* Porcentaje de posesión, Tiros al arco directos, Faltas cometidas.

<p align="center">
<img width="878" height="590" alt="image" src="https://github.com/user-attachments/assets/712011a5-b405-4ff9-a218-cc37f535ff26" />
</p>

---

## 🛠️ Tecnologías y Herramientas Utilizadas
*   **Data Sourcing:** Web Scraping (Transfermarkt).
*   **Data Pipelines & Automatización:** Make (Integromat).
*   **Cloud Storage & Data Entry:** Google Sheets.
*   **Machine Learning & NLP:** OpenAI API (Modelos de Clasificación/Decisión).
*   **Data Visualization:** QuickChart API / Generación dinámica de gráficos.

---

## ⚖️ Reflexión Ética y Limitaciones
El desarrollo contempla un análisis crítico sobre el rol de la Inteligencia Artificial en entornos corporativos y deportivos. Se reconoce a la IA como una potente herramienta de optimización y reducción de costos basada en patrones matemáticos; sin embargo, el modelo se plantea como un soporte complementario que no reemplaza el pensamiento crítico humano ni la subjetividad inherente a los imponderables del deporte.
