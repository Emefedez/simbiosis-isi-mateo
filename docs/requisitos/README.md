# Requisitos

Esta carpeta contiene la especificación de requisitos de Proyecto Simbiosis.

La línea base de requisitos está formada por los dos documentos siguientes, que deben versionarse y publicarse conjuntamente:

- **[Especificación de requisitos de software (SRS)](srs.md):** describe el propósito, alcance, contexto, interfaces, atributos de calidad, decisiones abiertas, glosario, modelos y trazabilidad del producto.
- **[Catálogo de requisitos](catalogo-requisitos.md):** contiene el texto canónico de los requisitos de usuario (UR), funcionales (FR) y no funcionales (NFR), junto con sus identificadores, fuentes, estado y relaciones de trazabilidad.

El catálogo no es una especificación independiente: es parte de la SRS. Para consultar o aprobar una versión de la especificación se deben utilizar siempre ambos documentos en la misma versión o etiqueta de publicación.

## Uso en las prácticas

La SRS se consolida como línea base común y sirve de referencia compartida en las prácticas:

- L04 construye el diagrama de E1. L05 incorpora E2 al modelo acumulado.
- L06 redacta las descripciones detalladas de UC-05 y UC-21 con actas aprobadas.
- L07 divide una épica de búsqueda de UC-21 en tres historias, con criterios de aceptación y revisión INVEST. La épica conserva la necesidad conjunta. Cada historia conserva sus fuentes.
- L08 ordena cinco historias dadas y justifica dos decisiones. Prepara las comprobaciones de NFR-005 y NFR-010 sobre US-03 y una DoD común de cuatro condiciones. La gestión del cambio se intentará recuperar en A10; su diseño sigue pendiente.
- L09, L10 y L11 emplean los requisitos como fuente para los modelos de análisis.

Las entregas de cada equipo no modifican directamente esta línea base común. El repositorio publica la versión de referencia que deben consultar; los artefactos producidos en cada práctica conservan sus propios enlaces de trazabilidad hacia los requisitos pertinentes.

## Convenciones

- Los identificadores de requisitos son estables y no se reutilizan.
- El catálogo es la única fuente de verdad para la redacción atómica de UR, FR y NFR.
- El glosario forma parte de la SRS.
- Las decisiones de captura posteriores que precisen información del Documento de Visión y Alcance se registran en las actas correspondientes y se reflejan en esta línea base con su trazabilidad.
- Las solicitudes de cambio aprobadas actualizan los documentos afectados y quedan registradas en [`../cambios/`](../cambios/registro-solicitudes-cambio.md).

## Documentación relacionada

- [Plantilla de backlog](plantilla-backlog.md), v1.2. Estructura vacía para preparar `backlog-propuesto.md`: orden, decisiones de prioridad, comprobaciones de calidad y Definición de Hecho. La posición y el identificador de cada historia son independientes. La conclusión vincula una condición de DoD con la evidencia necesaria.
- [Visión y alcance](../vision/vision_y_alcance.md)
- [Actas de captura y aclaraciones](../captura/README.md)
- [Registro de decisiones](../decisiones/registro-decisiones.md)
- [Criterios de revisión de requisitos](../calidad/criterios-revision-requisitos.md)
- [Modelos de análisis](../modelos/README.md)
- [Plantilla de historias de usuario de búsqueda](plantilla-historias-usuario-busqueda.md), v1.1, preparada para L07. Copiarla como `historias-usuario-busqueda.md` en el repositorio individual. La plantilla está vacía; incluye la épica de búsqueda y tres historias con identificadores locales US-01 a US-03. La plantilla está disponible en este repositorio.
