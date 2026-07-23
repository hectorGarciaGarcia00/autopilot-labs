
InboxAI — Master Plan

1. Objetivo

Crear un SaaS para gestorías y asesorías que analice correos entrantes, los clasifique y genere respuestas sugeridas.

El usuario siempre revisará la respuesta antes de enviarla.

2. Cliente objetivo

Gestorías y asesorías pequeñas o medianas en España.

Perfil inicial:

- Entre 2 y 20 empleados.
- Uso intensivo del correo electrónico.
- Gran volumen de consultas repetitivas.
- Gestión frecuente de facturas, nóminas, impuestos y documentación.

3. Problema

Las gestorías pierden muchas horas en:

- Leer correos.
- Identificar al cliente.
- Clasificar solicitudes.
- Revisar documentos adjuntos.
- Responder preguntas repetitivas.
- Detectar asuntos urgentes.

4. Propuesta de valor

InboxAI prepara cada correo antes de que el gestor lo lea.

Para cada mensaje:

1. Identifica el cliente.
2. Clasifica el asunto.
3. Detecta la prioridad.
4. Resume el contenido.
5. Propone una respuesta.
6. Permite revisar y enviar.

5. MVP

El MVP incluirá únicamente:

- Registro e inicio de sesión.
- Conexión con Gmail.
- Lectura de correos.
- Clasificación automática.
- Resumen automático.
- Prioridad del correo.
- Respuesta sugerida.
- Edición y envío manual.

6. Categorías iniciales

- Facturas.
- Nóminas.
- Impuestos.
- Documentación.
- Consulta de cliente.
- Nuevo cliente.
- Urgente.
- Otros.

7. Fuera del MVP

No se desarrollará inicialmente:

- Outlook.
- Respuestas totalmente automáticas.
- Contabilidad.
- OCR avanzado.
- Gestión documental completa.
- Aplicación móvil.
- Integraciones con programas de gestoría.
- Pagos y suscripciones.

8. Stack técnico provisional

- Frontend: Next.js.
- Lenguaje: TypeScript.
- Base de datos: PostgreSQL con Supabase.
- Autenticación: Supabase Auth.
- IA: API de OpenAI o Anthropic.
- Correo: Gmail API.
- Hosting: Vercel.
- Repositorio: GitHub.

9. Principios del proyecto

- Construir solo lo necesario para validar.
- No automatizar envíos sin revisión humana.
- Priorizar seguridad y privacidad.
- Mantener la arquitectura simple.
- Evitar funcionalidades que no ayuden a conseguir clientes.
- No dedicar más de cinco horas semanales.

10. Métricas iniciales

- Correos procesados.
- Tiempo estimado ahorrado.
- Porcentaje de respuestas aceptadas.
- Porcentaje de respuestas editadas.
- Errores de clasificación.
- Usuarios activos.

11. Plan inicial

Fase 1 — Validación

- Diseñar un prototipo.
- Hablar con gestorías.
- Confirmar problemas reales.
- Validar el precio.

Fase 2 — MVP

- Crear autenticación.
- Integrar Gmail.
- Procesar correos.
- Generar clasificación, resumen y respuesta.
- Crear panel de revisión.

Fase 3 — Piloto

- Incorporar entre 3 y 5 gestorías.
- Analizar errores.
- Mejorar los prompts.
- Medir tiempo ahorrado.

Fase 4 — Comercialización

- Añadir suscripciones.
- Crear landing page definitiva.
- Captar clientes.
- Automatizar soporte y onboarding.

12. Criterio para continuar

Solo se desarrollará el MVP completo si al menos tres gestorías confirman que el problema existe y aceptan probar una primera versión.