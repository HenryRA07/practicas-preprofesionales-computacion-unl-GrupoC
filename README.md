# Sistema de Gestión de Prácticas Preprofesionales - Carrera de Computación (UNL)

Este repositorio contiene la **Especificación de Requisitos de Software (ERS)** y el análisis de diseño del sistema para automatizar, optimizar y controlar el ciclo de vida de las prácticas preprofesionales (laborales y de servicio comunitario) de la Carrera de Computación en la Universidad Nacional de Loja (UNL). 

> **Nota de Ingeniería:** Como este proyecto se encuentra estrictamente en su fase de **Elicitación, Análisis y Validación de Requisitos (Unidad 1)**, este repositorio está dedicado a la documentación técnica, diagramas de arquitectura conceptual y prototipado ágil bajo control de versiones, sentando las bases sólidas antes del inicio del desarrollo de código fuente.

---

## 👥 Integrantes del Equipo (Dev's) (Grupo4)
* **Jeam Henry Romero Aguilar** *(Líder de Proyecto / Analista de Requisitos)*
* **Franz Ludeña** *(Lógica / Componentes de Negocio)*
* **Alexander Gallo** *(Frontend / Diseño de Experiencia de Usuario)*
* **Francisco Chamba** *(Testing / Control de Calidad de Requisitos)*

* **Asignatura:** Requisitos de Software (3º Ciclo "A")
* **Docente:** Ing. Edwin René Guamán Quinche
* **Institución:** Universidad Nacional de Loja

---

## 🎯 Objetivos del Informe Técnico

### Objetivo General
Documentar de forma estructurada las actividades desarrolladas durante el proceso de elicitación y análisis de requisitos de software para el Sistema de Gestión de Prácticas Preprofesionales de la Carrera de Computación de la Universidad Nacional de Loja, aplicando múltiples técnicas de levantamiento de información (entrevistas, estudio de documentos, análisis de sistemas existentes, lluvia de ideas y prototipado de interfaces) con la finalidad de identificar y estructurar los requisitos funcionales y no funcionales que permitan automatizar el registro, seguimiento y certificación de las 360 horas reglamentarias.

### Objetivos Específicos
1. **Aplicar técnicas de elicitación de requisitos** (entrevista al Director de Carrera, análisis normativo, estudio comparativo de sistemas y dinámicas de grupo) para identificar de manera exhaustiva las necesidades insatisfechas, problemas críticos y actores involucrados en el ecosistema actual de prácticas de la UNL.
2. **Analizar y especificar los requisitos del sistema** a través de fichas funcionales detalladas, diagramación de casos de uso y validación interactiva de prototipos, garantizando que el diseño conceptual cubra los criterios de calidad, transparencia y honestidad académica exigidos por la institución.

---

## 🔍 Descripción del Problema e Impacto

### Situación Actual
Actualmente, la gestión de las prácticas preprofesionales en la carrera se ejecuta de forma fragmentada y parcialmente manual. Al involucrar la participación coordinada de 6 actores distintos (*Estudiante, Tutor Académico, Tutor Institucional, Responsable de Prácticas, Director de Carrera y Secretaría*), el flujo de información a través de formularios físicos y archivos aislados genera cuellos de botella administrativos.

### Problemas Críticos Detectados
* **Desconocimiento de la Carga Horaria Extensa:** Estudiantes confunden las 360 horas reglamentarias obligatorias (240 horas laborales y 120 horas de servicio comunitario) creyendo erróneamente que corresponden a asignaturas regulares cortas de 40 horas, provocando retrasos en sus egresos.
* **Tareas No Profesionalizantes:** Empresas e instituciones receptoras asignan en ocasiones actividades ajenas al perfil de egreso (ej. simple digitalización de textos), perdiendo el valor académico de la práctica.
* **Falta de Alertas Tempranas en la Evaluación:** El marco normativo institucional reprueba automáticamente al estudiante si no obtiene una nota mínima de 7/10 o si incumple el 100% de asistencia. El proceso actual carece de alertas preventivas.
* **Rechazo Recurrente de Informes Finales:** Los portafolios físicos e informes finales sufren devoluciones constantes debido a errores estructurales mínimos o falta de alguno de los 6 apartados obligatorios normados.
* **Gestión de Convenios y Plazas Opaca:** Los estudiantes inician tarde sus procesos al no contar con un catálogo centralizado y público de empresas con convenios o cartas de compromiso vigentes.

---

## 🛠️ Metodología de Elicitación Aplicada

Para mitigar los problemas identificados, el equipo aplicó y documentó 5 técnicas clave, cuyos formatos y resultados están estructurados bajo control de versiones:

### 1. Entrevista Estructurada
* **Entrevistado:** Ing. Edison Coronel *(Director de la Carrera de Computación)*
* **Enlace a Evidencias (Drive):** [Repositorio de Grabaciones y Actas](https://drive.google.com/drive/folders/1c4jUZbGQRzdMpZwWbZnakDFfJSPHs8I1?usp=drive_link)
* **Resultados:** Descubrimiento de las necesidades de validación de matrícula, control estricto quincenal e insatisfacciones normativas del portafolio del egresado.

### 2. Estudio de Documentos Normativos
* **Fuentes Analizadas:** Reglamento de Régimen Académico de la UNL y Normas de Prácticas Preprofesionales.
* **Resultados:** Definición estricta de las reglas de negocio (nota mínima 7/10, asistencia 100%, desglose exacto de horas 240/120 y estructura obligatoria del reporte final).

### 3. Estudio de Sistemas Existentes (Benchmarking)
* **Plataformas Analizadas:** *Stazhlink*, *ISYPLUS Pasajes* y portales afines de gestión de vacantes y control de flujos de procesos.
* **Resultados:** Extracción de patrones de diseño de interfaces para entradas de búsqueda indexadas, filtrado por estados de solicitudes y diseño modular de reportes quincenales.

### 4. Lluvia de Ideas (Brainstorming)
* **Moderación:** Dinámicas de grupo orientadas a la priorización y descarte de características redundantes mediante matrices de votación estudiantil.
* **Resultados:** Traducción directa de ideas crudas en requerimientos funcionales técnicos organizados por prioridad de negocio.

### 5. Prototipado UX/UI (Figma)
* **Enfoque:** Creación de maquetas de interfaz de alta fidelidad orientadas al *Tutor Institucional* (para el marcado diario rápido de asistencia) y al *Estudiante* (para la consulta en tiempo real del progreso horario).
* **Resultados de Validación:** Integración de componentes interactivos (calendarios dinámicos y alertas visuales de campos requeridos) tras la retroalimentación obtenida.

---

## 📑 Estructura del Repositorio

El contenido técnico de este trabajo está distribuido de forma modular bajo la siguiente jerarquía de archivos:

```text
├── README.md                     # Este archivo (Presentación oficial y resumen ejecutivo)
├── .gitignore                    # Configuración de exclusión de archivos temporales de Office o IDEs
├── docs/                         # Documentación detallada de la Metodología de Elicitación
│   ├── 01_entrevista/            # Formato de preparación, notas de campo y enlaces a grabaciones
│   ├── 02_estudio_documentos/    # Análisis reglamentario de la UNL y glosario de términos inicial
│   ├── 03_sistemas_existentes/   # Tablas analíticas de Entradas, Procesos y Salidas (EPS) de benchmarking
│   └── 04_lluvia_ideas/          # Registro del debate del equipo y matriz de votación para priorización
├── design/                       # Modelado, Arquitectura y Experiencia de Usuario
│   ├── diagramas/                # Diagrama de Casos de Uso del Negocio y Actores del Sistema
│   └── prototipos/               # Capturas de interfaces de Figma y enlaces a maquetas navegables
└── specification/                # Especificación Final de Requisitos de Software (ERS)
    ├── requisitos_funcionales.md # Fichas técnicas individuales estructuradas (RF-01 a RF-08)
    └── requisitos_no_funcionales.md # Especificación de atributos de calidad (Seguridad, Usabilidad, Rendimiento)