# Especificación técnica inicial

Este documento fija decisiones suficientes para que Claude Code pueda comenzar la implementación sin rediseñar el producto.

## Principios
- MVP pequeño y desplegable.
- Una sola aplicación web.
- Evitar microservicios y complejidad prematura.
- Mantener el proveedor de IA desacoplado del resto de la aplicación.
- No almacenar datos sensibles innecesariamente en la primera versión.

## Stack propuesto
- Frontend + backend: Next.js con TypeScript.
- UI: Tailwind CSS.
- Validación: Zod.
- IA: capa `lib/ai` con proveedor configurable mediante variables de entorno.
- Persistencia inicial: ninguna para el primer flujo funcional.
- Despliegue objetivo: Vercel o equivalente compatible con Next.js.

## Pantallas del MVP

### `/`
Landing mínima con:
- Nombre/propuesta de valor.
- Botón «Crear borrador».
- Aviso de revisión profesional.

### `/generar`
Formulario de multa de tráfico.

### Resultado
Puede mostrarse en `/generar` tras recibir la respuesta. Debe permitir:
- Leer el borrador.
- Editarlo.
- Copiarlo.
- Volver a modificar los datos y regenerar.

## Backend
Endpoint recomendado:

`POST /api/generate`

Entrada JSON:
- `fullName`
- `taxId`
- `authority`
- `caseNumber`
- `infractionDate`
- `notificationDescription`
- `amount`
- `appealReason`
- `additionalEvidence`
- `notificationText`

Salida JSON:
- `draft`: string
- `warnings`: string[]

## Validación
- Campos esenciales obligatorios.
- Longitudes máximas razonables.
- El backend vuelve a validar todos los datos.
- No confiar únicamente en validación del navegador.

## Capa IA
Crear una interfaz simple para evitar acoplar la aplicación a un proveedor concreto.

Responsabilidades:
1. Recibir datos ya validados.
2. Construir instrucciones y contexto.
3. Solicitar el borrador al modelo.
4. Devolver texto + advertencias.

La clave API nunca debe enviarse al navegador.

## Prompting
El prompt debe exigir:
- español profesional y claro;
- no inventar información;
- no asumir normativa que no haya sido verificada;
- señalar datos ausentes;
- separar hechos aportados de propuestas de alegación;
- producir un borrador editable, no afirmar que el escrito está listo para presentar sin revisión.

## Privacidad
Para el prototipo:
- No crear historial de expedientes.
- No guardar formularios en base de datos.
- No registrar el contenido completo de los escritos en logs.
- Variables secretas únicamente en entorno servidor.

## Evolución posterior, solo tras validar
- Autenticación.
- Base de datos.
- Historial.
- Plantillas por tipo de trámite.
- Subida y extracción de documentos.
- Exportación DOCX/PDF.
- Suscripciones y límites de uso.

## Definición de terminado del primer incremento
- Proyecto ejecutable localmente.
- Landing funcional.
- Formulario validado.
- Endpoint servidor funcional.
- Integración real con un modelo de IA.
- Resultado editable y copiable.
- Manejo básico de errores y estados de carga.
- README con instalación y variables de entorno.
