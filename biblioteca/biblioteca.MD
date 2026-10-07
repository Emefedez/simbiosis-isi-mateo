# Caso de la biblioteca · ejercicio guiado de casos de uso

| Versión | Fecha | Estado |
| --- | --- | --- |
| 1.1 | 02/10/2026 | Vigente |

Este caso se utiliza en el ejercicio guiado inicial de L4. Contiene los requisitos de usuario (UR) y los requisitos funcionales (FR) necesarios para elaborar el diagrama de casos de uso durante la demostración.

## UR-01

El Socio podrá buscar libros en el catálogo para localizar los ejemplares que le interesan.

- **FR-01:** El sistema debe permitir al Socio buscar libros por título, autor o palabra clave.

**COMO** Socio,
**PARA** localizar los ejemplares que me interesan.

## UR-02

El Usuario invitado podrá buscar libros en el catálogo para localizar los ejemplares que le interesan.

- **FR-12:** El sistema debe permitir al Usuario invitado buscar libros por título, autor o palabra clave.

## UR-03

El Socio podrá reservar un libro para recogerlo en la biblioteca.

- **FR-03:** El sistema debe permitir al Socio reservar un libro.
- **FR-10:** véase «Requisitos funcionales compartidos».

## UR-04

El Socio podrá reservar una revista para recogerla en la biblioteca.

- **FR-04:** El sistema debe permitir al Socio reservar una revista.
- **FR-10:** véase «Requisitos funcionales compartidos».

## Requisitos funcionales compartidos

- **FR-10:** El sistema debe verificar la disponibilidad del ejemplar antes de confirmar la reserva y mostrar un mensaje si no está disponible. Asociado a UR-03 y UR-04.