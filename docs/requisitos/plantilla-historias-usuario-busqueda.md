# Historias de usuario de búsqueda


## Fuentes comunes

- [Acta de UC-21 Buscar recetas](../captura/acta-acuerdos-uc-21-buscar-recetas.md), v1.1, Vigente.
- [Catálogo de requisitos](catalogo-requisitos.md), UR-08 y FR pertinentes.
- [Modelo de casos de uso](../modelos/modelo-casos-de-uso.md), UC-21.

## Épica de búsqueda

Una épica expresa una necesidad amplia que se descompone en historias con valor propio.

Como cliente, quiero realizar una compra, para obtener mis productos.

**Estado:** descompuesta en US-01, US-02 y US-03. Conserva la necesidad conjunta. No cuenta como una cuarta historia de la entrega.

## Justificación de la división

[Escribir dos frases que expliquen los resultados útiles que separa la división.]

## US-01

**Título:** Añadir un producto al carrito

Como cliente de una tienda online, quiero agregar productos a mi carro de la compra, para reunir mi compra con los artículos deseados antes de confirmar el pedido.

**Fuentes:** UR-08; UC-21; [FR principal]; acta, [apartado pertinente].

### Criterios de aceptación

> Están mal, son **para US-02**
- **CA-01.** Dado un carrito, cuando contiene dos unidades de un producto y hay 6 disponibles en el momento en el que el usuario quiere escoger 4, entonces el sistema permite al usuario agregar la nueva cantidad al carrito.
- **CA-02.** Dado un carrito, cuando contiene dos unidades de un producto y hay 6 disponibles en el momento en el que el usuario quiere escoger 8, entonces el sistema no permite al usuario agregar la nueva cantidad al carrito, y marcará un error.
- **CA-03.** Dado un carrito, cuando tenga una cantidad inválida de productos en el carrito, entonces este número no se agregará y se volverá a un "known-good" value.

## US-02

**Título:** Cambiar la cantidad de un producto que ya está en el carrito

Como cliente de una tienda online, quiero modificar la cantidad de un producto del carrito, para adaptar la compra a lo que necesito.

**Fuentes:** UR-08; UC-21; [FR principal]; acta, [apartado pertinente].

### Criterios de aceptación

- **CA-01.** Dado un carrito, cuando contiene dos unidades de un producto y hay 6 disponibles en el momento en el que el usuario quiere escoger 4, entonces el sistema permite al usuario agregar la nueva cantidad al carrito.
- **CA-02.** Dado un carrito, cuando contiene dos unidades de un producto y hay 6 disponibles en el momento en el que el usuario quiere escoger 8, entonces el sistema no permite al usuario agregar la nueva cantidad al carrito, y marcará un error.
- **CA-03.** Dado un carrito, cuando tenga una cantidad inválida de productos en el carrito, entonces este número no se agregará y se volverá a un "known-good" value.


# Ejercicio, redacta y divide:

# Épica de búsqueda

Como usuario registrado, quiero buscar recetas según mis criterios, para localizar una receta que se ajuste a lo que necesito y consultar su detalle.

**Estado:** descompuesta en US-01, US-02 y US-03. Conserva la necesidad conjunta.

### Criterios de aceptación

- **CA-01.** Dado que existe una receta con "crema" en el título que emplea "calabacín" y no emplea "nata", y otra receta con "crema" en el título que emplea "calabacín" y "nata", cuando el usuario registrado busca el texto "crema" incluyendo "calabacín" y excluyendo "nata", entonces solo se entrega la primera receta.

- **CA-02.** Dado que el usuario registrado no ha indicado ningún criterio de búsqueda, cuando lanza la búsqueda, entonces el sistema solicita un criterio y no ejecuta la búsqueda.

- **CA-03.** Dado que una búsqueda ha entregado resultados y el usuario registrado consulta el detalle de una de esas recetas, cuando vuelve a los resultados, entonces se conservan los criterios y el orden de la última búsqueda.

## Justificación de la división

Se modula cada parte para mejorar la aplicación.

## US-01

**Título:** Buscar recetas mediante palabras clave.

Como usuario registrado, quiero buscar recetas mediante una palabra o frase, para localizar las recetas relacionadas con un plato o tema concreto sin recorrer todas las recetas publicadas.

**Fuentes:** 
    -UR-08; 
    -UC-21; 
    -FR-085; 
    -acta, [apartado_1].

### Criterios de aceptación

- **CA-01.** Dado que existen recetas asociadas a la palabra clave "fitness", cuando el cliente busca con ese término, entonces se entregan solamente las recetas que tienen "fitness" asociado.

- **CA-02.** Dado que no existe ninguna receta asociada a la palabra clave "sin lactosa", cuando el cliente busca con ese término, entonces no se entrega ningún resultado.

- **CA-03.** Dado que no existe ninguna receta con la frase exacta "desayuno tropical", pero sí una receta con "desayuno" y otra con "tropical", cuando el cliente busca con la frase "desayuno tropical", entonces no se entrega ningún resultado.


## US-02

**Título:** Buscar recetas por ingredientes seleccionados.

Como usuario registrado, quiero buscar recetas seleccionando los ingredientes que deseo encontrar, para obtener solo recetas que incluyan todos los ingredientes que quiero utilizar.

**Fuentes:**
    - UR-08
    - UC-21
    - FR-087
    - acta [2_criterios_de_búsqueda].

### Criterios de aceptación

- **CA-01.** Dado que existen recetas que emplean el ingrediente "calabacín", cuando el cliente busca por ese ingrediente, entonces se entregan las recetas que lo emplean.

- **CA-02.** Dado que no existe ninguna receta que emplee el ingrediente "calabaza", cuando el cliente busca por ese ingrediente, entonces no se entrega ninguna receta.

- **CA-03.** Dado que no existe ninguna receta que emplee todos los ingredientes elegidos, cuando el cliente realiza la búsqueda con esos ingredientes, entonces no se entrega ninguna receta.


## US-03

**Título:** Buscar recetas por exclusión de ingredientes seleccionados.

Como usuario registrado, quiero excluir de la búsqueda los ingredientes que no deseo, para descartar las recetas que contienen ingredientes que no quiero o no puedo consumir.

**Fuentes:** 
    -UR-08;
    -UC-21;
    -FR-086;
    -acta, [2_criterios_de_búsqueda].

### Criterios de aceptación

- **CA-01.** Dado que existen recetas que contienen el ingrediente "pan" y recetas que no lo contienen, cuando el usuario registrado busca excluyendo "pan", entonces no se entrega ninguna receta que contenga ese ingrediente.

- **CA-02.** Dado que ninguna receta contiene el ingrediente a excluir "chorizo", cuando el usuario registrado busca excluyendo ese ingrediente, entonces se entrega el mismo resultado que sin la exclusión.

- **CA-03.** Dado que el usuario registrado ha escrito el mismo término "lechuga" como inclusión y como exclusión, cuando lanza la búsqueda, entonces el sistema señala el conflicto y no realiza la búsqueda.


## Mejora tras la revisión INVEST

### Épica de búsqueda

**Criterios INVEST:**

- *Independiente:* No, engloba la localización y la consulta detallada.
- *Negociable:* Baja negociabilidad al agrupar múltiples bloques funcionales.
- *Valiosa:* Sí, expresa una necesidad global del usuario.
- *Estimable:* No es estimable con precisión por su gran tamaño.
- *Pequeña:* No, requiere descomposición al ser una épica.
- *Testable:* No es directamente testable sin desagregar sus criterios.

**Defectos frecuentes:** Mezcla de capacidades y falta de atomicidad.

**Trazabilidad:** Aunque la búsqueda de recetas se menciona de forma general en el *acta de captura de requisitos generales* y en el *acta de acuerdos técnicos y operativos*, la agrupación de búsqueda y consulta en una única entidad carece de soporte explícito en las actas.

### US-01

**Criterios INVEST:**

- *Independiente:* Sí, centrada en la búsqueda por términos de texto.
- *Negociable:* Sí, permite acordar las reglas de coincidencia textual.
- *Valiosa:* Sí, aporta valor directo para la localización de recetas.
- *Estimable:* Sí, acotada técnicamente.
- *Pequeña:* Sí, representa una capacidad única.
- *Testable:* Sí, verificable mediante la devolución o no de resultados según las palabras clave.

**Defectos frecuentes:** No introduce componentes técnicos ni pasos de implantación.

**Trazabilidad:** La funcionalidad general de búsqueda de recetas está confirmada en el *acta de captura de requisitos generales* y en el *acta de acuerdos técnicos y operativos* (párrafos 2.1.2 y 2.4.3). Sin embargo, el mecanismo específico de búsqueda por palabra clave no aparece detallado explícitamente en el texto de las actas.

### US-03

**Criterios INVEST:**

- *Independiente:* No totalmente, se solapa con los mecanismos de filtrado e inclusión de ingredientes.
- *Negociable:* Sí, respecto a la sintaxis de exclusión.
- *Valiosa:* Sí, pero la redacción defectuosa resta claridad a la necesidad real.
- *Estimable:* Difícil de estimar por la ambigüedad del objeto a excluir («términos»).
- *Pequeña:* Sí en propósito, pero imprecisa en su alcance real.
- *Testable:* Dificultad de prueba por falta de precisión en el objeto de la exclusión.

**Defectos frecuentes:** Actor genérico, verbo redundante, cambio de perspectiva gramatical en la finalidad y ambigüedad en el objeto a excluir.

**Trazabilidad:** La exclusión explícita de términos no está contemplada ni acordada en el *acta de captura de requisitos generales* ni en el *acta de acuerdos técnicos y operativos*.

## Dudas pendientes

"Ninguna"

## Declaración de uso de IA

He utilizado IA para corregir el error de la estructura Dado-Cuando-Entonces, sin cambiar el contenido explicado; también para arreglar el formato de los criterios INVEST.