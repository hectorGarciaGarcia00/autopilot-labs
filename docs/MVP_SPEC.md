# MVP — Generador IA para gestorías

## Objetivo de la v1
Validar que una gestoría puede ahorrar tiempo generando un primer borrador de alegaciones frente a una multa de tráfico mediante un formulario guiado y una IA.

## Usuario objetivo
Gestor o administrativo de una pequeña gestoría española (1–10 empleados).

## Caso de uso inicial
Alegaciones/recurso de una multa de tráfico.

## Flujo principal
1. El usuario entra en la aplicación.
2. Selecciona «Multa de tráfico».
3. Completa el formulario.
4. Revisa los datos introducidos.
5. Pulsa «Generar borrador».
6. El backend construye una petición estructurada al modelo de IA.
7. La IA devuelve un borrador del escrito.
8. El usuario revisa y edita el contenido.
9. El usuario copia o descarga el resultado.

## Formulario mínimo
- Nombre y apellidos / razón social del interesado.
- NIF/CIF.
- Organismo sancionador.
- Número de expediente.
- Fecha de la infracción.
- Descripción de la infracción/notificación.
- Importe de la sanción.
- Motivo por el que se desea recurrir.
- Información o pruebas adicionales.
- Texto relevante de la notificación recibida.

## Salida esperada
Un borrador profesional y estructurado que incluya, cuando proceda:
- Identificación del interesado.
- Identificación del expediente.
- Exposición de hechos basada únicamente en los datos aportados.
- Alegaciones propuestas.
- Petición final.
- Marcadores claros cuando falte información.

## Reglas de seguridad y calidad
- La aplicación genera borradores; no presenta escritos automáticamente.
- El usuario debe revisar el documento antes de utilizarlo.
- La IA no debe inventar hechos, fechas, expedientes, pruebas ni normativa.
- Si falta información esencial, debe indicarlo expresamente.
- La interfaz mostrará que el resultado requiere revisión profesional.

## Fuera del MVP
- Presentación automática ante administraciones.
- Firma electrónica.
- Integraciones con DGT, AEAT o Seguridad Social.
- OCR avanzado de documentos.
- Gestión completa de expedientes.
- Facturación.
- Aplicación móvil nativa.
- Múltiples tipos de escritos.

## Criterio de éxito inicial
Una gestoría puede completar el flujo completo y obtener en pocos minutos un borrador suficientemente útil como para ahorrar tiempo respecto a redactarlo desde cero.
