# Proyecto Simbiosis Plan de iteración E3

| Versión | Fecha | Estado |
| --- | --- | --- |
| 1.0 | 06/10/2026 | Vigente |

Este plan define el trabajo previsto para E3, la tercera iteración de Elaboración. Selecciona las funciones del foro y la resolución de reportes sobre su contenido. Establece también las actividades, los recursos, los productos y los criterios de evaluación.

El plan pertenece a un proyecto simulado. La duración, el equipo, el esfuerzo y el coste son supuestos de la simulación. El alcance funcional corresponde a lo acordado para E3. Los requisitos proceden de los documentos del proyecto. El plan no presenta como realizados los trabajos previstos en E1 o E2.

## 1 Punto de partida

| Dato | Valor |
| --- | --- |
| Proyecto | Proyecto Simbiosis |
| Iteración | E3 |
| Fase | Elaboración |
| Duración simulada | Dos semanas de trabajo, con diez días laborables |
| Calendario | Días 1 a 10 de E3. No son fechas del curso. |
| Ámbitos principales | Consulta y participación en el foro, seguimiento, notificaciones y reportes con resolución |
| Equipo simulado | Tres personas, con seis horas disponibles por persona y día |
| Capacidad | 180 horas de trabajo del equipo |
| Esfuerzo asignado | 162 horas para actividades y 18 horas de reserva |

Las referencias de requisitos son la [Visión y Alcance](../vision/vision_y_alcance.md), versión 2.4, la [SRS](../requisitos/srs.md), versión 0.14, y el [catálogo de requisitos](../requisitos/catalogo-requisitos.md), versión 1.13. Se consultan también las actas enlazadas en esos documentos.

UR significa requisito de usuario. FR significa requisito funcional. NFR significa requisito no funcional. Los identificadores de este plan remiten al catálogo. Las descripciones resumen el alcance seleccionado y no sustituyen la redacción canónica de los requisitos.

El [plan de E1](plan-iteracion-e1.md) aborda acceso, cuentas y ayuda. El [plan de E2](plan-iteracion-e2.md) amplía el trabajo con salud y recetas. Al iniciar E3, el equipo revisará las evaluaciones y las versiones de los productos disponibles. Identificará los permisos, escenarios y decisiones que puede reutilizar.

Si falta un producto necesario, el equipo registrará la carencia y ajustará el alcance o el esfuerzo antes de iniciar el trabajo que dependa de él. No dará por resuelto un riesgo solo porque aparezca en un plan anterior.

La Visión limita el proyecto a seis meses y 90.000 €. El equipo revisará el esfuerzo y gasto reales de las iteraciones anteriores antes de confirmar los recursos disponibles para E3.

## 2 Objetivos de E3

E3 tiene tres objetivos:

- Ampliar el modelo acumulado con una vista del foro y de la resolución de reportes sobre su contenido.
- Precisar la consulta pública, la participación con sesión iniciada, la gestión de comentarios propios y la actuación del coordinador sobre contenido reportado.
- Comprobar mediante un prototipo limitado los permisos, la persistencia de las interacciones y el recorrido desde la presentación del reporte hasta la consulta de su resolución.

El modelo conservará las vistas de E1 y E2 y revisará los elementos compartidos. E3 mantiene un alcance limitado. No completa todos los requisitos del foro ni toda la moderación de la plataforma.

El prototipo permitirá estudiar los riesgos seleccionados. E3 no representa por sí sola el cierre de Elaboración ni una versión preparada para producción.

## 3 Riesgos que se abordarán

La prioridad de la tabla es un supuesto del plan. El equipo la revisará al iniciar E3.

| Riesgo | Prioridad | Trabajo previsto | Evidencia esperada |
| --- | --- | --- | --- |
| Permitir participación sin sesión iniciada o impedir la consulta pública | Alta | Separar consulta y participación; comprobar permisos en el servidor. | Pruebas de consulta anónima y de participación permitida y denegada. |
| Permitir editar o eliminar comentarios ajenos o editar fuera del plazo | Alta | Precisar autoría y cómputo de los quince minutos. | Pruebas con dos autores y operaciones dentro y fuera del plazo. |
| Perder la relación entre una respuesta y su comentario original | Media | Precisar cómo se conservan y muestran las respuestas, incluida la eliminación del comentario original. | Escenarios y pruebas con comentarios y respuestas relacionados. |
| Permitir que un usuario resuelva reportes sin ser coordinador | Alta | Comprobar el permiso en el servidor y conservar la actuación realizada. | Pruebas de resolución permitida y denegada. |
| Mantener visible contenido retirado o perder coherencia con la resolución | Alta | Comprobar la visibilidad posterior y el registro de la decisión. | Pruebas de consulta directa y búsqueda después de retirar contenido. |
| Notificar a un destinatario incorrecto o mostrar información privada | Alta | Precisar destinatarios y datos de los avisos. | Pruebas de respuestas, seguimiento y resolución con cuentas distintas. |
| Superar los tiempos previstos de consulta o publicación | Media | Medir las operaciones implementadas del foro con la carga de referencia. | Informe de tiempos, errores, carga y límites de la medición. |

La moderación dependerá de las políticas que se hayan confirmado. El prototipo utilizará contenido ficticio y reglas de prueba identificadas. Sus resultados no demostrarán que las políticas del producto estén completas ni que exista un servicio de moderación continuo.

## 4 Alcance del trabajo de requisitos

E3 estudiará las siguientes funciones. El equipo consultará el catálogo completo para comprobar las reglas y dependencias. Incorporará los objetivos seleccionados a una tercera vista del mismo modelo de casos de uso.

### 4.1 Consulta pública y búsqueda del foro

**UR-04.** Cualquier persona podrá consultar el foro sin registrarse. La consulta incluye hilos, comentarios y respuestas. Incluye también las publicaciones destacadas por número de «me gusta» o de respuestas durante las últimas 24 horas.

FR seleccionados: FR-195, FR-039 y FR-040.

E3 incluye la búsqueda por autor con coincidencia exacta, rango de fechas, etiquetas y palabras clave en el título o cuerpo. El usuario podrá combinar esos criterios.

FR seleccionados: FR-034, FR-035, FR-036, FR-037 y FR-038.

Los hilos sin nuevas publicaciones ni comentarios durante 90 días se archivarán automáticamente. Seguirán siendo visibles y no admitirán nuevos comentarios.

FR seleccionado: FR-033.

La consulta pública y la participación tienen condiciones diferentes. El archivo automático es una regla del sistema; no supone identificar un participante externo adicional.

### 4.2 Publicación y comentarios propios

**UR-04.** E3 incluye la creación de hilos con título y cuerpo de contenido. Incluye publicar comentarios y responder a otros comentarios, conservando la relación entre el comentario original y la respuesta.

FR seleccionados: FR-022, FR-023 y FR-024.

El comentario admite hasta 1.000 caracteres. Su autor podrá editarlo durante los quince minutos posteriores a su publicación y eliminarlo permanentemente. El contenido eliminado dejará de ser visible en el foro.

FR seleccionados: FR-027 y FR-028.

Las publicaciones y los comentarios muestran su fecha y hora en el formato definido por el catálogo.

FR seleccionado: FR-032.

Crear hilos, comentar, responder, seguir hilos y dar «me gusta» requiere una sesión iniciada.

FR seleccionado: FR-021.

E3 no incorpora la edición o eliminación de hilos propios como funciones nuevas: los requisitos seleccionados regulan esas acciones sobre comentarios. El equipo no ampliará el alcance por analogía.

### 4.3 Seguimiento y reacciones positivas

**UR-04.** E3 incluye seguir hilos y consultarlos en una sección de hilos seguidos del perfil. Incluye dar «me gusta» a publicaciones y mostrar su contador.

FR seleccionados: FR-029 y FR-031.

No se habilitan reacciones negativas. Seguir usuarios es una función distinta de seguir hilos y queda para otra iteración.

### 4.4 Presentación y resolución de reportes del foro

**UR-09.** E3 incluye reportar publicaciones y comentarios del foro mediante una opción visible junto al contenido. El usuario seleccionará una categoría y podrá añadir un comentario. El sistema registrará el reporte y confirmará su recepción.

FR seleccionados: la parte de FR-120 y FR-121 correspondiente al foro; FR-122, FR-123, FR-124 y FR-125.

**UR-10.** E3 incluye que el coordinador consulte los reportes pendientes, seleccione uno, revise el contenido y decida mantenerlo, editarlo o retirarlo. El sistema conservará la resolución y el registro de la actuación. El contenido retirado dejará de ser accesible para los usuarios.

FR seleccionados: la parte de FR-136 necesaria para consultar los reportes; FR-137, FR-146 y FR-147, aplicados al foro.

El usuario que reportó recibirá el resultado sin datos personales del autor afectado. Cuando se actúe sobre el contenido, se contemplará la comunicación al autor con los motivos de la decisión.

FR seleccionados: FR-126 y FR-138.

El [acta general](../captura/acta-captura-requisitos-generales.md) establece que el coordinador es el único rol responsable de administrar y moderar el foro. Se conserva esa responsabilidad. Las reglas concretas de moderación siguen pendientes de aclaración.

E3 completa el recorrido de presentación y resolución del reporte dentro del alcance seleccionado. La revisión previa de publicaciones, las apelaciones, la restauración de contenido y las sanciones sobre cuentas quedan para otras iteraciones.

### 4.5 Notificaciones internas

**UR-04 y UR-09.** E3 incluye los avisos de respuestas, menciones mediante `@alias`, novedades de hilos seguidos, recepción de reportes y resolución de reportes. El usuario podrá consultarlos y acceder al hilo o contenido relacionado cuando corresponda.

FR seleccionados: FR-025, FR-026, FR-030, FR-125 y FR-126. Se tendrá en cuenta FR-138 para las comunicaciones al autor afectado.

Estos avisos son internos. E3 no añade envío de correo por estas interacciones. El equipo reutilizará el modelo acumulado cuando amplíe las notificaciones con otros temas en futuras iteraciones.

### 4.6 Identidad pública y ayuda

**UR-01.** El foro mostrará el alias como identidad pública. Mantendrá separada esa identidad de los datos privados de las cuentas.

FR seleccionado: la parte de FR-192 correspondiente al foro.

**UR-07.** Las intervenciones y publicaciones de nutricionistas acreditados mostrarán el distintivo profesional. Es una regla de presentación del foro; no incorpora los consejos de vida saludable a E3.

FR seleccionado: la parte de FR-206 correspondiente al foro. Se conserva la condición de aprobación profesional de FR-191.

**UR-12.** E3 amplía la ayuda existente con los temas de búsqueda, consulta y participación en el foro, seguimiento, reacciones, reportes y notificaciones. Conserva las funciones de ayuda contextual, navegación y control estudiadas en E1.

FR seleccionados: la parte de FR-173 correspondiente al foro y las condiciones de FR-172 y FR-174 a FR-177. Los temas de ayuda previstos por este plan se limitarán a las funciones seleccionadas.

El equipo revisará el alcance de la ayuda existente. No creará un objetivo diferente por cada tema nuevo.

### 4.7 Reglas y preguntas pendientes

Antes de programar los escenarios afectados, el equipo aclarará estas cuestiones:

- Cómo se interpreta la búsqueda por autor sin exponer su nombre completo en el foro.
- Cómo se computa el límite de edición y qué ocurre si una solicitud coincide con su vencimiento.
- Qué ocurre con las respuestas cuando se elimina el comentario original.
- Cómo se computan los 90 días de inactividad y qué operaciones se permiten sobre un hilo archivado.
- Qué regla evita reacciones repetidas y si se permite retirar un «me gusta».
- Qué categorías y criterios permiten resolver cada reporte, y qué ocurre si el contenido ya ha sido eliminado.
- Cómo se tratan varios reportes sobre el mismo contenido y resoluciones concurrentes.
- Qué información reciben el usuario que reportó y el autor afectado, y qué ocurre con enlaces a contenido retirado.

Las respuestas se registrarán como acuerdos de la simulación, con su procedencia. Las decisiones aún no confirmadas permanecerán como preguntas. Los datos y reglas de prueba se identificarán como tales. El plan no modifica por sí mismo el catálogo ni la SRS.

## 5 Profundidad y funcionalidad pendiente

El alcance del trabajo de requisitos es mayor que el alcance del prototipo.

| Trabajo | Profundidad prevista |
| --- | --- |
| Funciones del apartado 4 | Identificar participantes, objetivos y relaciones. Añadir la vista del foro y reportes al modelo acumulado. |
| Elementos compartidos con E1 y E2 | Revisar nombres, permisos y relaciones. Conservar los identificadores de los objetivos existentes. |
| Consulta pública, comentarios propios y resolución de reportes | Precisar los escenarios y condiciones necesarios para estudiar los riesgos. |
| Resto de funciones seleccionadas | Registrar el objetivo, las reglas, el respaldo en requisitos y las preguntas necesarias para revisar el modelo. |
| Prototipo | Implementar solo los recorridos limitados del apartado 7. |
| Pruebas | Comprobar los recorridos implementados y registrar sus límites. |

El producto principal del modelado será el diagrama de la tercera vista. El equipo actualizará el [mismo documento del modelo](../modelos/modelo-casos-de-uso.md), sus tablas y su alcance acumulado. Revisará las vistas anteriores cuando cambien elementos compartidos. Mantendrá la misma frontera del sistema y los mismos nombres de actores.

La imagen de esta vista se llamará `casos-de-uso-foro-reportes.png` y se guardará en `docs/modelos/imagenes/`, conforme a la [guía de modelos](../modelos/README.md). Se conservará también el archivo editable de la herramienta cuando esté disponible.

Las siguientes funciones se mantienen para iteraciones posteriores:

| Funcionalidad pendiente | Requisitos | Motivo |
| --- | --- | --- |
| Mensajes directos y seguimiento de usuarios | FR-196 y FR-197 | Limitar E3 a la interacción en hilos. |
| Reportes sobre recetas, consejos, perfiles y otros contenidos | Parte pendiente de FR-120 y FR-121 | Ampliar después el recorrido probado en el foro. |
| Verificación automática de contenido y gestión de reglas de moderación | FR-127 a FR-131, FR-150 y la parte correspondiente de FR-151 | Precisar las políticas antes de incorporar bloqueo automático. |
| Revisión previa y moderación específica de recetas y consejos | FR-132 a FR-135 | Aclarar la relación entre revisión del coordinador y validación nutricional. |
| Apelaciones y restauración de contenido | FR-139 y FR-142 | Concretar su tramitación y la relación entre decisión, apelación y restauración. |
| Priorización avanzada, alertas por múltiples reportes y estadísticas | Parte pendiente de FR-136; FR-145 y FR-148 | Mantener una resolución limitada de reportes. |
| Bloqueo temporal y expulsión de cuentas | FR-186 y FR-187 | Estudiar después las sanciones y sus políticas. |
| Fin de la relación de cuidado y ciclo de vida completo de sus cuentas | FR-208 a FR-210 y acuerdos del acta general | Conservar los efectos de acceso estudiados en E2 y aclarar quién termina la relación y cómo se reactiva la cuenta. |
| Consejos de vida saludable y valoraciones y comentarios de recetas | Resto de UR-07 y UR-11 | Incorporar otras vistas en iteraciones posteriores. |
| Recordatorios, alertas, umbrales, calculadora y funciones pendientes de recetas | Pendientes de UR-05, UR-06 y UR-08 indicados en el plan E2 | Conservar el alcance limitado de E3. |
| Integración con Google | FR-006, FR-018, FR-190 y NFR-015 | Revisar su riesgo al iniciar E3 y conservarla como integración pendiente. |
| Progreso entre sesiones, multimedia y búsqueda en la ayuda | FR-178, FR-179 y FR-180 | Ampliar la ayuda después de sus temas seleccionados. |

Los pendientes técnicos de E1 y E2 se revisarán al inicio. El modelo puede representar una función cuya implementación siga pendiente. FR-017 y FR-149 están retirados; no se incorporarán como tareas de E3.

Las reglas de moderación multilingüe de FR-151 y la interfaz de escritorio y móvil de FR-152 se aplicarán dentro del alcance implementado. No demostrarán la moderación completa de todas las clases de contenido.

Los aplazamientos no eliminan requisitos del proyecto. Las exclusiones siguen siendo las de la Visión y la SRS.

## 6 Requisitos no funcionales

Los NFR condicionan la arquitectura, la interfaz y las pruebas. No se convierten automáticamente en casos de uso.

| NFR | Trabajo previsto en E3 | Límite de la comprobación |
| --- | --- | --- |
| NFR-004 y NFR-005 | Medir búsqueda y consulta del foro con la carga de referencia. | Se comprobarán las consultas implementadas, no todas las consultas del sistema. |
| NFR-006 | Medir la publicación de comentarios del foro. | No se comprobarán todas las publicaciones de recetas o mensajes. |
| NFR-010 | Revisar formularios, contenido, respuestas, avisos y resolución de reportes con una herramienta automática y una revisión manual. | La revisión no demostrará la conformidad de toda la plataforma con WCAG 2.2 AA. |
| NFR-003 y NFR-014 | Comprobar los recorridos del prototipo en castellano y gallego, incluido el cambio de idioma. | No se implementará traducción automática del contenido. |
| NFR-011, NFR-012 y NFR-013 | Reutilizar el entorno web en la nube y comprobar acceso responsivo y estándares abiertos. | El entorno no será el despliegue de producción. |
| NFR-001 y NFR-007 | Revisar la disponibilidad y el ajuste automático de recursos con la nueva carga del foro. | E3 no demostrará disponibilidad mensual ni escalado automático completo. |
| NFR-002, NFR-008 y NFR-009 | Conservar las decisiones de copias y recuperación de las iteraciones anteriores y revisar las necesidades del foro. | Las pruebas de E3 no demostrarán la recuperación de todo el sistema; NFR-002 mantiene su alcance canónico de salud y recetas. |
| NFR-015 | Mantener las condiciones de autenticación externa. | Se comprobarán cuando se aborde Google. |

La prueba de carga utilizará 100 usuarios concurrentes y 10 operaciones por segundo durante 30 minutos. El equipo definirá y registrará la mezcla de operaciones antes de ejecutarla. Incluirá búsqueda y consulta del foro y publicación de comentarios implementados.

El informe separará los resultados por operación. El 95 % de las búsquedas y consultas deberá completarse en un máximo de 2 segundos. El 95 % de las publicaciones de comentarios deberá completarse en un máximo de 3 segundos. Se aplicarán los límites de medición del apartado 2.1.3 del [acta técnica](../captura/acta-acuerdos-tecnicos-operativos.md).

Las operaciones de resolución de reportes se medirán y describirán, pero no se les asignará por analogía un límite que no esté confirmado. La relación de NFR-005 y NFR-006 con FR concretos sigue pendiente en el catálogo.

Las pruebas de permisos comprobarán las reglas seleccionadas. No demostrarán por sí solas la seguridad completa del producto ni el cumplimiento de todas las obligaciones legales.

## 7 Trabajo de arquitectura y prototipo

### 7.1 Revisión de arquitectura

El equipo revisará la propuesta y las evidencias disponibles de E1 y E2. Mantendrá como hipótesis una aplicación web modular con interfaz, lógica de aplicación y persistencia separadas. Revisará esa hipótesis cuando las pruebas aporten evidencia nueva.

La propuesta debe permitir relacionar hilos, comentarios, respuestas, seguidores, avisos y reportes. Conservará la autoría necesaria para comprobar permisos sin publicar datos personales. Los permisos se comprobarán en el servidor en cada operación protegida.

El equipo estudiará la coherencia entre una actuación del coordinador, la visibilidad del contenido, el registro de la resolución y sus notificaciones. Estudiará también la conservación de las respuestas cuando cambia la visibilidad del comentario original.

Las decisiones técnicas pertenecen a la simulación. No obligan a utilizar una tecnología concreta ni a crear un servicio independiente por cada función.

### 7.2 Escenarios del prototipo

El prototipo reutilizará la base técnica disponible. Utilizará persistencia, cuentas ficticias y una interfaz mínima. Implementará estos recorridos:

1. **Consulta pública.** Una persona sin sesión iniciada buscará un hilo por palabras clave y consultará su contenido. Se comprobará que no puede crear hilos ni comentarios. Se consultará también un hilo archivado preparado como dato de prueba.
2. **Publicación y autoría.** Un usuario con sesión iniciada creará un hilo y un comentario. Otro usuario responderá. Se comprobará la relación entre ambos comentarios, la edición dentro y fuera del plazo y la denegación de edición o eliminación de un comentario ajeno.
3. **Seguimiento y aviso.** Un usuario seguirá un hilo. Otro publicará un comentario y el primero consultará la notificación correspondiente. Se comprobará que un usuario que no sigue el hilo no recibe ese aviso por seguimiento.
4. **Reporte y resolución.** Un usuario reportará un comentario. El coordinador lo resolverá con una decisión de mantener, editar o retirar. Se registrará la actuación y el usuario consultará el resultado. Se comprobará el aviso al autor cuando corresponda y la denegación de resolución a un usuario sin ese permiso.
5. **Visibilidad posterior.** Tras retirar contenido, se comprobará que no aparece en la consulta pública ni en los resultados y que no puede recuperarse mediante su dirección directa. El registro de moderación conservará la información necesaria para revisar la actuación, conforme a las reglas confirmadas.

Los recorridos de resolución utilizarán reportes distintos para probar las decisiones previstas. Las políticas de esos ejemplos se identificarán como reglas de prueba. Si falta una regla necesaria, se registrará la pregunta y se ajustará el recorrido afectado antes de implementarlo.

El prototipo no implementará todos los filtros, los destacados, los «me gusta», las menciones, el archivo automático completo, la ayuda ni todos los tipos de contenido reportable. El hilo archivado de prueba permitirá comprobar sus permisos, pero no demostrará el proceso automático de 90 días. Estas funciones siguen formando parte del trabajo de requisitos seleccionado cuando así lo indica el apartado 4.

### 7.3 Entorno y recursos

El equipo necesitará un repositorio Git, una herramienta de modelado, un entorno web de prueba, una base de datos y herramientas de pruebas automáticas, carga y accesibilidad. Reutilizará los recursos anteriores cuando estén disponibles.

Los datos de prueba incluirán dos usuarios autores, un coordinador, hilos activos y archivados, comentarios con respuestas, seguimiento, avisos y reportes. Se prepararán tiempos de publicación controlados para comprobar el límite de edición. No se utilizarán datos personales ni contenido real reportado.

Las comprobaciones de permisos utilizarán solicitudes directas al servidor, además del recorrido de la interfaz. El informe identificará las versiones del código, la configuración, los datos y las herramientas, con los pasos para repetir las pruebas.

## 8 Equipo esfuerzo y coste

Las personas siguientes forman el equipo de desarrollo simulado. No son los actores del sistema.

| Persona | Responsabilidades | Horas asignadas | Reserva |
| --- | --- | --- | --- |
| P1 | Coordinación, requisitos y modelo de casos de uso | 54 | 6 |
| P2 | Arquitectura y desarrollo | 54 | 6 |
| P3 | Integración, datos y pruebas | 54 | 6 |
| Total | Equipo de tres personas | 162 | 18 |

Cada persona dispone de 60 horas durante E3. Las 18 horas de reserva cubren incidencias y ajustes. Si la reserva no basta, la coordinación reducirá recorridos secundarios del prototipo o el tamaño del conjunto de prueba. Registrará el cambio y conservará las comprobaciones prioritarias de permisos, autoría, resolución y visibilidad posterior.

Se mantiene como supuesto una tarifa interna de 35 € por hora. Las 180 horas cuestan 6.300 €, incluida la reserva. Se asignan otros 300 € al entorno y a los servicios de prueba. El coste máximo previsto de E3 es **6.600 €**.

La suma de los presupuestos previstos de E1, E2 y E3 es 19.800 €. Esta cifra no representa el gasto real ni el coste total del proyecto. El equipo revisará el presupuesto restante con los datos de cierre disponibles.

## 9 Actividades calendario y revisiones

Las horas de la tabla son horas de trabajo de cada persona. No son la duración de la actividad. Varias actividades pueden coincidir en el calendario.

| ID | Actividad | Días | Responsable | P1 | P2 | P3 | Total |
| --- | --- | --- | --- | --- | --- | --- | --- |
| T1 | Revisar resultados anteriores, plan y riesgos | 1 | P1 | 6 | 3 | 3 | 12 |
| T2 | Ampliar el modelo y precisar los escenarios prioritarios | 1–6 | P1 | 30 | 6 | 6 | 42 |
| T3 | Revisar arquitectura, permisos y coherencia de moderación | 2–7 | P2 | 6 | 15 | 3 | 24 |
| T4 | Preparar entorno y datos de foro, avisos y reportes | 1–5 | P3 | 0 | 6 | 6 | 12 |
| T5 | Construir e integrar los recorridos del prototipo | 4–8 | P2 | 0 | 18 | 18 | 36 |
| T6 | Ejecutar pruebas y analizar resultados | 7–10 | P3 | 3 | 3 | 12 | 18 |
| T7 | Consolidar productos y registrar pendientes | 9 | P1 | 6 | 3 | 3 | 12 |
| T8 | Revisar y evaluar E3 | 10 | P1 | 3 | 0 | 3 | 6 |
| Total | Trabajo asignado | 1–10 | P1 | 54 | 54 | 54 | 162 |

T2, T3 y T4 comenzarán tras la revisión inicial de T1. T5 necesita los primeros escenarios revisados de T2, las decisiones iniciales de T3 y el entorno mínimo de T4. Esas primeras versiones deberán estar disponibles en el día 3. Las tres actividades podrán continuar después.

T6 comenzará con los recorridos integrados disponibles. La prueba de carga y la revisión final requerirán una versión integrada de T5. Los resultados podrán exigir ajustes. T7 conservará los pendientes conocidos; T8 incorporará los resultados finales al cierre.

| Revisión | Día | Resultado previsto |
| --- | --- | --- |
| Inicio | 1 | Resultados y carencias anteriores identificados; alcance y riesgos revisados. |
| Escenarios y arquitectura | 3 | Reglas necesarias, primeros escenarios y entorno mínimo disponibles. |
| Demostración interna | 8 | Recorridos integrados y primeras pruebas de permisos y reportes registrados. |
| Cierre de E3 | 10 | Productos contrastados con el plan; riesgos, esfuerzo y trabajo siguiente revisados. |

La coordinación comprobará cada día el avance, el esfuerzo consumido y los obstáculos. Cada cambio de alcance indicará su motivo, su efecto y el trabajo aplazado. El equipo mantendrá identificadas las versiones revisadas de los productos.

## 10 Productos y criterios de evaluación

| Producto previsto | Responsable | Criterio para su revisión |
| --- | --- | --- |
| Modelo de casos de uso acumulado | P1 | Incorpora los objetivos del apartado 4, conserva la coherencia con E1 y E2 y declara la cobertura parcial. |
| Escenarios y preguntas de requisitos | P1 | Distinguen consulta pública, autoría y permisos de resolución; separan acuerdos de preguntas abiertas. |
| Descripción revisada de arquitectura | P2 | Explica decisiones de persistencia, permisos, visibilidad y avisos, con sus requisitos y riesgos. |
| Prototipo integrado | P2 | Permite repetir los recorridos limitados del apartado 7 con datos ficticios. |
| Informe de pruebas | P3 | Identifica versión, entorno, datos, carga y resultados; registra fallos y límites. |
| Evaluación de E3 | P1 | Compara objetivos, alcance, esfuerzo y coste previstos con los resultados y propone el trabajo siguiente. |

La revisión del modelo comprobará que sus elementos representan objetivos y participantes externos respaldados por requisitos. No se exigirá un caso independiente por FR o NFR ni una cantidad mínima de relaciones `include` o `extend`.

Las vistas mantendrán nombres compatibles y la misma frontera del sistema. Los casos que conserven su objetivo mantendrán su identificador. La presentación del reporte y su resolución representarán objetivos distintos, aunque se refieran al mismo reporte. El modelo indicará qué incorpora E3 y qué revisa de iteraciones anteriores.

Las pruebas mostrarán operaciones permitidas y denegadas. Comprobarán la consulta sin registro, la participación con sesión, la autoría de comentarios, el límite de edición, el permiso de resolución y la invisibilidad del contenido retirado.

Las pruebas de avisos comprobarán destinatarios y contenido comunicado. Las mediciones técnicas indicarán qué demuestran y qué queda pendiente. Si un objetivo no se alcanza, el equipo registrará el resultado y propondrá una acción.

## 11 Evaluación y continuidad previstas

La evaluación se realizará en el día 10. Este plan establece cómo se evaluará E3; no registra resultados ya obtenidos.

El equipo comparará el trabajo realizado con el plan. Registrará objetivos alcanzados, desviaciones de esfuerzo y coste, incidencias y lecciones aprendidas. Revisará qué riesgos se han reducido y cuáles permanecen abiertos.

La evaluación se conservará como documento separado. Identificará el commit que contiene el estado revisado del modelo, sus imágenes y archivos editables disponibles. Cerrar E3 no declarará automáticamente una línea base formal.

El equipo seleccionará el trabajo siguiente a partir de riesgos y pendientes acumulados. Conservará los elementos válidos del modelo y revisará la arquitectura cuando las nuevas evidencias lo exijan.

E3 no permite declarar completos el foro, la moderación ni el modelo del sistema. La revisión previa de publicaciones, el fin de las relaciones de cuidado y la tramitación de apelaciones conservan sus cuestiones pendientes. La evaluación indicará qué trabajo adicional se necesita antes de la siguiente iteración.

## 12 Documentos de referencia

- [Plan de iteración E1](plan-iteracion-e1.md) y [plan de iteración E2](plan-iteracion-e2.md).
- [Documento de Visión y Alcance](../vision/vision_y_alcance.md).
- [SRS](../requisitos/srs.md) y [catálogo canónico de requisitos](../requisitos/catalogo-requisitos.md).
- [Acta de captura de requisitos generales](../captura/acta-captura-requisitos-generales.md).
- [Acta de acuerdos técnicos y operativos](../captura/acta-acuerdos-tecnicos-operativos.md).
- [Modelo de casos de uso](../modelos/modelo-casos-de-uso.md) y [guía de modelos](../modelos/README.md).
