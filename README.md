# Miniproyecto de Clasificación de MRI

## Objetivo del Proyecto
Desarrollar una **Red Neuronal Convolucional (CNN)** para clasificar imágenes de resonancia magnética (MRI) cerebral en 4 categorías:
1.  **Glioma**
2.  **Meningioma**
3.  **Pituitaria (Pituitary)**
4.  **Tejido Sano (Healthy Tissue)**

**Dataset:** 7,023 imágenes de MRI desde varios ángulos.

---

## Entregables
1.  **Jupyter Notebook (`.ipynb`):** Implementación completa (Limpia, documentada y reproducible).
2.  **Informe Científico (`.pdf`):** Un reporte de **máximo 2 páginas** (sin incluir referencias) en **formato IEEE** (estilo CVPR). Usa las plantillas de LaTeX o Word proporcionadas.

---

## Fases del Proyecto (Flujo de Trabajo)
Me tomé la libertad de armar una propuesta de fases de desarrollo. La idea es que cada fase del código genere directamente el material que nos pide la rúbrica para el informe final (como los mapas de colores, la matriz de confusión y las métricas F1)
Esta estructura ya esta en el archivo `main.ipynb`. Es solo una base para empezar, así que sientanse libres de sugerir cambios o ajustes si lo ven necesario

*   **Fase 1:** Configuración del entorno y carga de datos (Se recomienda PyTorch).
*   **Fase 2:** EDA (Visualización de muestras de todas las clases + verificación del balance de clases).
*   **Fase 3:** Preprocesamiento (Redimensionar, Normalizar, Aumentación de Datos).
*   **Fase 4:** Arquitectura CNN (Bloques de Conv-ReLU-Pool + Dropout).
*   **Fase 5:** Entrenamiento (Loss: CrossEntropy, Optimizador: Adam, monitoreo de Validación).
*   **Fase 6:** Evaluación (Matriz de Confusión, F1-Score, visualización de errores).
*   **Fase 7:** Discusión (Preparar insights para el informe IEEE).

---

## Lista de Verificación de la Rúbrica (Cómo obtener 100%)

### 1. El Informe (90% de la nota)
- [ ] **Introducción (15%):** Contexto claro, relevancia justificada y breve "estado del arte".
- [ ] **Metodología (10%):** Detallar cada paso (datos usados, capas de la arquitectura, activaciones, hiperparámetros como LR, tamaño de batch, épocas).
- [ ] **Figuras y Subplots (10%):** Alta resolución, mapas de colores adecuados, correctamente enumerados y referenciados en el texto.
- [ ] **Resultados Cualitativos (10%):** Subplots organizados comparando resultados (ej. predicción vs. realidad).
- [ ] **Resultados Cuantitativos (10%):** Tablas con métricas (Accuracy, F1, promedio/desviación). Descripciones claras.
- [ ] **Discusión (10%):** Comparar resultados con la teoría, citar fuentes y analizar fuentes de error.
- [ ] **Redacción y Ortografía (10%):** Lenguaje técnico, sin errores, párrafos bien estructurados.
- [ ] **Formato (15%):** Cumplimiento al 100% del formato IEEE. Nombres de autores incluidos. Citas correctas.
- [ ] **EVITAR PENALIZACIÓN:** Asegurar que el reporte tenga **exactamente 2 páginas** o menos (excluyendo bibliografía).

### 2. El Código (10% de la nota)
- [ ] **Limpieza:** Sin "código muerto" (bloques comentados que no se usan).
- [ ] **Documentación:** Cada función o bloque lógico principal debe tener un comentario o celda markdown explicándolo.
- [ ] **Orden:** Las celdas deben ejecutarse en secuencia sin errores.

---

## Consejos Pro para el Equipo
*   **Framework:** Se recomiendan **PyTorch** por ser el estándar de la industria.
*   **Overfitting:** Usar **Aumentación de Datos** (flips horizontales, rotaciones) y capas de **Dropout**. Esto se menciona explícitamente en el material de AlexNet.
*   **Preprocesamiento:** Las imágenes de MRI varían en intensidad; estandarizarlas/normalizarlas es obligatorio.
*   **Reproducibilidad:** Mantener siempre la función `set_seed()` al principio para asegurar que todos obtengamos los mismos resultados.
*   **Estado del Arte:** Mencionar arquitecturas como **AlexNet**, **VGG** o **ResNet** en la intro/metodología añade calidad de "Nivel Maestría" al reporte.

---

## Recursos
*   **Link del Dataset:** [Brain Tumor MRI Scans (Kaggle)](https://www.kaggle.com/datasets/rm1000/brain-tumor-mri-scans)  
*   **Plantilla LaTeX:** `Docs/Template-Curso-Tecnicas-de-Deep-Learning-latex/`
*   **Código Base:** `main.ipynb`
