# CLAUDE.md

## Proyecto
MVP SaaS para pequeñas gestorías españolas. La primera función genera borradores de alegaciones frente a multas de tráfico a partir de un formulario.

Antes de implementar cambios, leer:
- `docs/idea.md`
- `docs/MVP_SPEC.md`
- `docs/TECH_SPEC.md`

## Objetivo inmediato
Construir únicamente el primer flujo funcional descrito en `docs/MVP_SPEC.md`.

## Reglas de desarrollo
- TypeScript estricto.
- Mantener la arquitectura simple.
- No añadir funcionalidades fuera del MVP sin necesidad.
- Evitar dependencias innecesarias.
- Nunca exponer claves API al cliente.
- Validar entradas también en servidor.
- No persistir datos personales del formulario en la primera versión.
- No registrar datos sensibles en logs.
- Separar la integración del proveedor de IA en `lib/ai`.
- Tratar la salida de IA como un borrador que requiere revisión humana.
- La IA no debe inventar hechos ni datos del expediente.

## Stack
- Next.js
- TypeScript
- Tailwind CSS
- Zod

## Flujo a implementar
1. Landing mínima.
2. Formulario en `/generar`.
3. Validación cliente/servidor.
4. `POST /api/generate`.
5. Integración del modelo en servidor.
6. Mostrar borrador editable.
7. Botón copiar.
8. Estados de carga y errores.

## Fuera de alcance
No implementar todavía:
- login;
- base de datos;
- pagos;
- panel administrativo;
- OCR;
- firma electrónica;
- presentación automática;
- integraciones con administraciones;
- app móvil;
- más tipos de documentos.

## Forma de trabajar
- Implementar en incrementos pequeños.
- Antes de cada bloque relevante, inspeccionar el código existente.
- Después de cambios, ejecutar lint/typecheck/build disponibles y corregir errores provocados por el cambio.
- No reescribir archivos no relacionados.
- Si una decisión no está definida y afecta de forma importante al producto, detenerse y explicarla antes de asumirla.

## Primer encargo para Claude Code
Inspecciona el repositorio y los tres documentos de `docs/`. Prepara el proyecto Next.js con TypeScript, Tailwind y Zod siguiendo `docs/TECH_SPEC.md`. Implementa después el flujo MVP de `docs/MVP_SPEC.md` en incrementos pequeños. No añadas autenticación, base de datos ni pagos. Antes de conectar un proveedor de IA, deja la capa `lib/ai` aislada y documenta exactamente qué variable de entorno necesita el usuario configurar.
