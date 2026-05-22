# Especificación de Requisitos No Funcionales (ERNF)

Este documento describe las restricciones de diseño, atributos de calidad, estándares técnicos y propiedades emergentes que el **Sistema de Gestión de Prácticas Preprofesionales** debe cumplir para asegurar estabilidad, rendimiento y seguridad bajo el contexto institucional.

---

## 1. Seguridad y Privacidad de Datos
* **RNF-01 (Autenticación Segura):** Toda interacción con el sistema debe exigir un inicio de sesión cifrado. Se priorizará el uso de credenciales institucionales mediante protocolos de Single Sign-On (SSO).
* **RNF-02 (Control de Acceso Basado en Roles - RBAC):** El sistema debe segmentar de forma estricta los privilegios de los 6 actores (*Estudiante, Tutor Académico, Tutor Institucional, Responsable de Prácticas, Director de Carrera y Secretaría*). Ningún actor podrá visualizar o modificar datos que no correspondan a su competencia.
* **RNF-03 (Protección de Datos Personales):** Dado que se manejan datos sensibles de estudiantes y contratos de empresas, los archivos cargados en el repositorio de almacenamiento deben encriptarse en reposo usando el estándar AES-256.

## 2. Rendimiento y Concurrencia
* **RNF-04 (Tiempo de Respuesta Eficiente):** Las consultas de carga del dashboard del conteo acumulado de horas (RF-04) o la renderización de las tablas de solicitudes no deben superar los 2 segundos bajo condiciones normales de red.
* **RNF-05 (Soporte de Carga Concurrente):** El sistema debe ser capaz de soportar accesos concurrentes de estudiantes en épocas de entrega de informes finales sin degradación del servicio o caídas del servidor.

## 3. Disponibilidad y Resiliencia
* **RNF-06 (Disponibilidad Continua):** El sistema debe garantizar una disponibilidad operativa del 99.5% durante el período académico ordinario, estando accesible las 24 horas del día para permitir el registro flexible de bitácoras por parte de los tutores institucionales.
* **RNF-07 (Respaldos Automatizados):** Se realizarán copias de seguridad automáticas diarias de la base de datos relacional y de los archivos PDF del portafolio estudiantil cargados para prevenir pérdidas fortuitas de información.

## 4. Usabilidad y Experiencia de Usuario (UX/UI)
* **RNF-08 (Diseño Responsivo e Intuitivo):** La interfaz del sistema debe adaptarse de forma fluida a dispositivos móviles, tablets y computadoras de escritorio. Esto es crítico para facilitar que el Tutor Institucional registre la asistencia desde cualquier dispositivo móvil en el lugar de trabajo.
* **RNF-09 (Validación Preventiva e Feedback):** Las pantallas de ingreso de datos deben incluir componentes amigables (como calendarios interactivos) y desplegar alertas visuales inmediatas de éxito o mensajes de error claros al guardar transacciones.

## 5. Compatibilidad y Portabilidad
* **RNF-10 (Compatibilidad Multiplataforma):** La aplicación web debe ser totalmente compatible y funcional en las versiones más recientes de los principales navegadores del mercado (Google Chrome, Mozilla Firefox, Microsoft Edge y Safari).
* **RNF-11 (Arquitectura Contenidizada):** El sistema debe estar diseñado para ser empaquetado mediante contenedores virtuales (ej. Docker), asegurando su portabilidad y facilidad de despliegue en infraestructuras tanto locales como en la nube.