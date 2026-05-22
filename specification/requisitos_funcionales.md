# Especificación de Requisitos Funcionales (ERF)

Este documento detalla los requisitos funcionales del **Sistema de Gestión de Prácticas Preprofesionales**. Cada requisito describe una función específica que el sistema debe ejecutar para satisfacer las necesidades de los usuarios y cumplir con la normativa institucional de la UNL.

---

## Resumen de Actores del Sistema
* **Estudiante:** Usuario que ejecuta las prácticas, registra su asistencia diaria, carga evidencias y genera su informe final.
* **Tutor Institucional:** Supervisor en la entidad receptora que controla la asistencia diaria y certifica las actividades quincenales del practicante.
* **Responsable de Prácticas:** Encargado de validar la pertinencia de las actividades y gestionar las solicitudes de plazas.
* **Secretaría de la Carrera:** Actor encargado de verificar el expediente y emitir el certificado oficial de cumplimiento.

---

## Fichas Técnicas de Requisitos Funcionales

### RF-01: Verificación de Matrícula Legal
| Campo | Detalle |
| :--- | :--- |
| **Código** | RF-01 |
| **Nombre** | Verificación de Matrícula Legal |
| **Descripción** | El sistema debe permitir verificar de forma automática que el estudiante posea una matrícula legalizada en la asignatura correspondiente antes de iniciar cualquier proceso técnico. |
| **Entradas** | Cédula del estudiante, código de carrera, período académico. |
| **Proceso** | El sistema consulta el estado de matriculación en la base de datos central de la universidad y valida que el estado sea "Activo". |
| **Salidas** | Confirmación de habilitación / Mensaje de error bloqueante ("Estudiante no matriculado"). |
| **Actor Principal**| Estudiante |
| **Prioridad** | Alta |

---

### RF-02: Validación de Prerrequisitos Académicos
| Campo | Detalle |
| :--- | :--- |
| **Código** | RF-02 |
| **Nombre** | Validación de Prerrequisitos Académicos |
| **Descripción** | El sistema permitirá validar si el estudiante ha aprobado la totalidad de los niveles y asignaturas previas requeridas para quedar legalmente habilitado para las prácticas de ciclos superiores. |
| **Entradas** | Historial académico (Récord de calificaciones). |
| **Proceso** | El sistema cruza la malla curricular vigente con las materias aprobadas por el postulante. |
| **Salidas** | Estado de aptitud ("Habilitado" / "No Habilitado" con lista de materias pendientes). |
| **Actor Principal**| Estudiante |
| **Prioridad** | Alta |

---

### RF-03: Registro Diario de Asistencia y Bitácora
| Campo | Detalle |
| :--- | :--- |
| **Código** | RF-03 |
| **Nombre** | Registro Diario de Asistencia y Bitácora |
| **Descripción** | El sistema debe permitir registrar al tutor institucional el control diario de asistencia (hora de entrada y salida), junto con la descripción detallada de las actividades ejecutadas por el practicante. |
| **Entradas** | Fecha, hora de ingreso, hora de salida, descripción de la actividad, observaciones. |
| **Proceso** | El sistema calcula automáticamente las horas netas realizadas del día, valida el formato de fecha e indexa el registro al portafolio del alumno. |
| **Salidas** | Registro de jornada guardado con éxito / Alerta de campos obligatorios faltantes. |
| **Actor Principal**| Tutor Institucional |
| **Prioridad** | Alta |

---

### RF-04: Contador Dinámico de Progreso Horario
| Campo | Detalle |
| :--- | :--- |
| **Código** | RF-04 |
| **Nombre** | Contador Dinámico de Progreso Horario |
| **Descripción** | El sistema presentará al estudiante un panel visual con el conteo y desglose acumulado en tiempo real de las 240 horas de prácticas laborales y las 120 horas de servicio comunitario de forma independiente. |
| **Entradas** | Horas aprobadas de las bitácoras diarias. |
| **Proceso** | Sumatoria segregada de horas validadas por tipo de práctica (Laboral / Comunitaria) y cálculo del porcentaje restante para llegar a las 360 totales. |
| **Salidas** | Dashboard con barras de progreso numéricas y porcentuales. |
| **Actor Principal**| Estudiante |
| **Prioridad** | Alta |

---

### RF-05: Validación de Pertinencia Profesional
| Campo | Detalle |
| :--- | :--- |
| **Código** | RF-05 |
| **Nombre** | Validación de Pertinencia Profesional |
| **Descripción** | El sistema permitirá analizar al responsable de prácticas la viabilidad y pertinencia de las actividades técnicas propuestas por las empresas aliadas, asegurando que se alineen estrictamente al perfil de egreso de Computación. |
| **Entradas** | Plan de actividades de la empresa / institución receptora. |
| **Proceso** | El responsable evalúa digitalmente si las tareas no son "no profesionalizantes" (ej. evitar simple digitalización) y emite un dictamen. |
| **Salidas** | Estado del plan de prácticas ("Aprobado" / "Rechazado con observaciones"). |
| **Actor Principal**| Responsable de Prácticas de la Carrera |
| **Prioridad** | Alta |

---

### RF-06: Generación y Carga del Informe Estructurado Final
| Campo | Detalle |
| :--- | :--- |
| **Código** | RF-06 |
| **Nombre** | Generación y Carga del Informe Estructurado Final |
| **Descripción** | El sistema permitirá generar y cargar al estudiante el informe final detallado, compilando de forma automatizada las fechas, porcentajes de asistencia y la estructura reglamentaria obligatoria de la UNL. |
| **Entradas** | Datos consolidados de bitácoras, archivos adjuntos de evidencias. |
| **Proceso** | El sistema maqueta un documento PDF inalterable que incluye obligatoriamente los 6 apartados normados: Presentación, Objetivos, Metodología, Resultados, Conclusiones y Recomendaciones. |
| **Salidas** | Archivo PDF del informe final listo para revisión del Tutor Académico. |
| **Actor Principal**| Estudiante |
| **Prioridad** | Alta |

---

### RF-07: Gestión de Evidencias de Convalidación Laboral
| Campo | Detalle |
| :--- | :--- |
| **Código** | RF-07 |
| **Nombre** | Gestión de Evidencias de Convalidación Laboral |
| **Descripción** | El sistema permitirá cargar al estudiante las evidencias legales y laborales (como contratos previos o afiliaciones) para tramitar la confirmación de la experiencia laboral previa bajo la modalidad de convalidación. |
| **Entradas** | Contrato de trabajo, mecanizado del IESS, certificado de funciones en formato PDF. |
| **Proceso** | Almacenamiento seguro del expediente y notificación automática al Responsable de Prácticas para su respectiva auditoría jurídica y técnica. |
| **Salidas** | Confirmación de carga exitosa / Alerta de archivo corrupto o formato no soportado. |
| **Actor Principal**| Estudiante |
| **Prioridad** | Media |

---

### RF-08: Emisión Automatizada de Certificado de Cumplimiento
| Campo | Detalle |
| :--- | :--- |
| **Código** | RF-08 |
| **Nombre** | Emisión Automatizada de Certificado de Cumplimiento |
| **Descripción** | El sistema permitirá emitir a la secretaría de la carrera el certificado general oficial de cumplimiento de las prácticas preprofesionales una vez verificado el cierre correcto del portafolio. |
| **Entradas** | Expediente aprobado por el Responsable y Tutor Académico. |
| **Proceso** | Verificación sistémica de que el estudiante sume las 360 horas y cuente con evaluaciones válidas superiores a 7/10. Generación de código QR de validación institucional. |
| **Salidas** | Certificado Oficial de Prácticas Preprofesionales firmado electrónicamente en formato PDF. |
| **Actor Principal**| Secretaría de la Carrera |
| **Prioridad** | Alta |