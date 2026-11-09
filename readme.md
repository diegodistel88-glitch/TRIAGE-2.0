# 🏥 Sistema de Triage 2.0 — Complejo Sanitario Favaloro Molas

Sistema de **Triage Informatizado de Nueva Generación** basado en algoritmos clínicos y Machine Learning, desarrollado para el **Complejo Sanitario Favaloro Molas**.

Clasifica pacientes según su nivel de urgencia en la guardia mediante la evaluación **ABCDE**, el **Triángulo de Evaluación Pediátrica**, escalas validadas (Glasgow, dolor, PAM) y genera automáticamente **diagnósticos de enfermería NANDA 2025** y recomendaciones de actuación.

---

## 📋 Características principales

- ⏱️ **Cronómetro de triage** automático (indicador de calidad asistencial)
- 🎨 **5 niveles de prioridad** con colores estándar internacionales (Rojo, Naranja, Amarillo, Verde, Azul)
- 🩺 **Evaluación ABCDE** completa (Vía Aérea, Respiración, Circulación, Déficit Neurológico, Exposición)
- 👶 **Triángulo de Evaluación Pediátrica** (0–14 años) con 7 estados clínicos
- 📊 **Cálculo automático de PAM** y validación de signos vitales según edad
- 🧠 **Diagnósticos NANDA 2025** generados en tiempo real
- 💡 **Recomendaciones de enfermería** según el nivel de triage
- 📋 **Resumen copiable** al portapapeles para pegar en la historia clínica
- 🔒 **100% local** — no envía datos a ningún servidor
- 📱 **Responsive** — funciona en PC, tablet y móvil

---

## 🚀 Cómo usar el sistema

### 1. Inicio del triage
Al abrir la página, el **cronómetro** comienza automáticamente. Registra el tiempo que demanda la valoración inicial.

### 2. Datos del paciente
Complete nombre, edad, género y antecedentes médicos (HTA, DBT, EPOC, ACV, arritmias, coronarios, asma, epilepsia, obesidad, etc.).

> ⚠️ **La edad condiciona el sistema**:
> - **≤ 10 años** → se oculta el campo de presión arterial
> - **≤ 14 años** → aparece automáticamente el **Triángulo Pediátrico**

### 3. Signos vitales
Registre FC, PA (calcula PAM automáticamente), FR, temperatura, SpO₂ y glucemia.

> Los campos se colorean en **verde** (normal), **rojo** (anormal) o **azul** (normal pediátrico) en tiempo real.

### 4. Evaluación ABCDE
Cada sección (A, B, C, D, E) tiene un checkbox **"Sin problemas"** que autocompleta valores normales y bloquea los campos.

En **E (Exposición)** se registra el tipo de lesión:
- **Agudo**: cerrado, abierto (laceración, cortante, punzante, transfixiante), quemadura (tipo, superficie, grado) o politraumatismo
- **Crónico**: úlceras por presión, lesiones vasculares, etc.

### 5. Dolor, salud mental, alergias y violencia
- Escala de dolor 0–10 con localización (si es tórax → clasificación típico vs. atípico)
- Condición de salud mental (conducta suicida, psicosis, abuso de sustancias, etc.)
- Reacción alérgica (anafilaxia, respiratoria, cutánea, alimentaria)
- Situación de violencia (doméstica, de género, infantil)

### 6. Resolución
Indique si el paciente: sigue por consultorio externo, consultorio de guardia o ingresa a guardia.

### 7. Calcular triage
Presione **"Calcular triage"**. El sistema mostrará:

| Elemento | Descripción |
|----------|-------------|
| 🎨 Color y prioridad | Rojo (inmediato), Naranja (10 min), Amarillo (60 min), Verde (120 min), Azul (240 min) |
| 🩺 Diagnósticos NANDA 2025 | Generados automáticamente según hallazgos |
| 💡 Recomendaciones de enfermería | Intervenciones sugeridas según el nivel |
| 📋 Resumen completo | Documento copiable a la historia clínica |

### 8. Copiar resumen
El botón **"Copiar Resumen Completo"** genera un informe estructurado con todos los datos, alteraciones marcadas con ⚠️ y el resultado del triage.

---

## ⚙️ Instalación y despliegue

Este archivo es un **HTML autocontenido** (CSS y JavaScript embebidos). No requiere servidor, base de datos ni instalación.

### Opción A — GitHub Pages (recomendada)

1. Cree un repositorio en GitHub (ej. `triage-favaloro-molas`).
2. Suba el archivo `index.html` a la rama `main`.
3. Vaya a **Settings → Pages**.
4. En *Source*, seleccione **"Deploy from a branch"** → rama `main` → carpeta `/ (root)`.
5. Guarde. En 1–2 minutos estará disponible en:
