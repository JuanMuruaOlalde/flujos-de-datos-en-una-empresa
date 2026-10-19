# Cuestiones abiertas

## Categorías de cliente en una multinacional

Por ahora están en `src/comercial_y_ventas.md`. Falta pensar hasta qué punto puede ir una parte básica en los datos maestros globales y hasta qué punto dependen demasiado de cada país o filial.

## Repartir el Artículo entre departamentos, como el Cliente

Al completar los capítulos han ido apareciendo datos del artículo que mantiene cada departamento: planos, revisiones y lista de materiales en `src/diseño_tecnico.md`; fuentes de aprovisionamiento en `src/compras.md`; ruta y parámetros de planificación en `src/fabricacion_o_servicios.md`; plan de control en `src/calidad.md`; información comercial en `src/marketing.md`; envases en `src/prevencion_y_medioambiente.md`. Y también en `src/almacenes_y_logistica.md` (datos logísticos) y en `src/administracion.md` (coste estándar).

Por ahora cada uno es una entidad aparte. Falta decidir si se le aplica al Artículo el mismo esquema que al Cliente y al Proveedor (núcleo en los datos maestros y un bloque por departamento, con referencias cruzadas). Es lo que hacen muchos ERP con las "vistas" del maestro de artículos. Inconveniente: con siete u ocho bloques, las listas de referencias cruzadas se alargan mucho.

## Empleado como dato maestro

Casi todos los departamentos necesitan saber quién es quién: usuarios en IT, comerciales, compradores, técnicos, operarios... Por ahora el Empleado está entero en `src/departamento_personal.md`. Falta pensar si su parte organizativa (código, nombre, sociedad, departamento, puesto, responsable) debería ir a los datos maestros. Con cuidado, porque son datos personales.
