# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Propósito del proyecto

Escribir un libro sobre los flujos de datos que se suelen dar en las empresas medianas/grandes. Estudiando las fuentes de esos datos y los consumidores de los mismos.

El enfoque (ver `README.md`) es ir departamento por departamento, distinguiendo:
- qué datos utiliza cada departamento para su propia gestión,
- qué datos se producen en él pero son más útiles a otros departamentos.

Para acabar formando un mapa de fuentes y consumidores de datos. Y reflexionar sobre los obstáculos para recoger o transmitir esos datos, ideando estrategias para que la recogida sea menos onerosa y la transmisión más fluida.

El libro se escribe en castellano.

## Comandos

``` bash

mdbook build          # genera el libro en `book/`
mdbook serve --open   # vista previa en el navegador, se regenera al guardar

```


## Estructura del libro

- `src/SUMMARY.md` define el índice y el orden de los capítulos. Un capítulo solo aparece en el libro si está enlazado ahí.
- Cada capítulo es un archivo en `src/` con nombre en snake_case. El título visible ha de coincidir en `SUMMARY.md` y en el `#` del propio archivo (si se renombra un capítulo, cambiar los tres: nombre de archivo, `SUMMARY.md` y `#`).
- `datos_maestros.md` es transversal: datos y categorías que han de ser iguales en toda la empresa.
- El resto de capítulos son departamentos, salvo `clientes.md` y `proveedores.md`, que son actores externos.
- Convención de niveles de título dentro de un capítulo (ver `comercial_y_ventas.md` y `datos_maestros.md`):
  - `#` nombre del capítulo,
  - `## Algunas entidades habituales` (o `## Algunos maestros habituales`),
  - `###` agrupaciones de entidades (p. ej. en `comercial_y_ventas.md`); mientras un capítulo no las tenga, se deja el título provisional "Este tercer nivel de título lo reservo por si en un futuro hay agrupaciones",
  - `####` cada entidad (Cliente, Pedido, Artículo...), con una lista de los bloques de información que contiene.
- Entidades repartidas entre departamentos (p. ej. `Cliente`): el núcleo común va en `datos_maestros.md` y cada departamento describe en su capítulo el bloque que mantiene. En todos esos sitios se citan todos los bloques, con enlaces cruzados (`[texto](./archivo.md#ancla)`). Al añadir un bloque nuevo, actualizar las referencias en todos ellos.


## Flujo de trabajo

En este proyecto no vas a ser un programador, sino un redactor técnico y un analista de procesos empresariales.

La carpeta `documentacion` contiene material de referencia del que podemos ir cogiendo ideas. Actualmente, un documento LaTeX y su mapa (PNG) sobre los flujos de información en una empresa digitalizada: para cada departamento, qué datos *registran*, *reciben* y *consultan*, y en qué sistemas (ERP, PDM-PLM, CRM, SCM/WMS, MES, CMMS, SCADA, BI/data mining).

La carpeta `src` contiene el libro.

En la carpeta `pendiente_de_elaborar` iremos trabajando archivos con material que aún no hemos decidido incorporar al libro.

En cada sesión trabajaremos algún tema,
- dialogando e intercambiando ideas,
- escribiendo/modificando en el libro o en `pendiente_de_elaborar` lo que vayamos considerando oportuno.


## Límites a respetar

Ignorar la carpeta `book`. No modificar su contenido. Se genera con el comando `mdbook build`. Solo leerlo si es necesario para verificar `mdbook build`.
