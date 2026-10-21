# Calidad

## Algunas entidades habituales

### Sistema de gestión

#### Documento del sistema
- Procedimientos, instrucciones y formatos. Versión. Quién lo aprueba. Fecha. A quién se distribuye.

Los documentos de todos los departamentos pasan por aquí: así se sabe que cada cual trabaja con la versión vigente.

Es importante que se almacenen en un solo sitio, accesible por todas las personas que necesiten consultarlos. Así se evita tener que recurrir a copias "controladas" (que suelen tener una gran tendencia a quedar desactualizadas).

#### Certificación
- Norma (ISO 9001, normas sectoriales...). Alcance. Entidad certificadora. Vigencia.

Muchos clientes la exigen (ver [Comercial y Ventas](./comercial_y_ventas.md)).

#### Auditoría
- Tipo (interna, de cliente, de certificación, a proveedor). Fecha. Área auditada. Auditores. Hallazgos.

Los hallazgos dan lugar a acciones correctivas.

#### Requisito de cliente
- Normas o exigencias específicas de un cliente (de embalaje, de documentación, de aprobación de cambios...).

Han de conocerlos todos los departamentos que trabajan para ese cliente.

### Control del producto

#### Plan de control
- Por artículo y operación. Características a controlar. Tolerancias. Método y equipo de medida. Frecuencia. Tamaño de muestra.

Las características y tolerancias salen de los planos y especificaciones de [Diseño técnico de productos](./diseño_tecnico.md#especificación-técnica).

#### Inspección
- Dónde (en recepción, durante la fabricación, al final). Artículo. Lote. Resultado de cada característica medida. Decisión (aceptado, rechazado).

Las inspecciones de recepción enlazan con la [Recepción](./compras.md#recepción) del pedido de compra. Las inspecciones de proceso, con el [Lote](./fabricacion_o_servicios.md#lote-o-número-de-serie) fabricado. Mejor si los resultados los registra directamente el equipo de medida (así se evitan errores de transcripción).

#### Certificado de calidad
- Resultados de análisis o ensayos de un lote. Emitido por un proveedor, o por nosotros para un cliente.

#### Equipo de medida
- Identificación. Ubicación. Fechas de la última y de la próxima calibración. Resultado. Incertidumbre.

Si un equipo resulta estar descalibrado, hay que saber qué inspecciones se hicieron con él.

### No calidad

#### No conformidad
- Origen (recepción, proceso, cliente, auditoría). Artículo. Lote. Cantidad afectada. Descripción.
- Decisión (rechazar, reprocesar, aceptar con concesión). Coste.

Si viene de un proveedor, acaba en una [Devolución a proveedor](./compras.md#devolución-a-proveedor).

#### Reclamación de cliente
- Cliente. Artículo. Lote. Descripción del defecto. Plazos de respuesta exigidos. Informe de respuesta (8D o similar).

Llega a través de [Postventa](./postventa.md#incidencia-o-reclamación) o de [Comercial y Ventas](./comercial_y_ventas.md). Para investigarla hace falta la trazabilidad del lote.

#### Acción correctiva o preventiva
- Problema. Causa raíz. Acciones. Responsable. Plazo. Verificación de la eficacia.

Las acciones suelen recaer en otros departamentos.

#### Coste de la no calidad
- Rechazos. Reprocesos. Garantías. Devoluciones. Por periodo, artículo, proveedor o cliente.

Lo consultan [Dirección](./direccion.md) y [Administración general, Contabilidad y Finanzas](./administracion.md).

### Proveedores

#### Proveedor

El núcleo común (código, razón social, identificación fiscal) está en los [Datos maestros](./datos_maestros.md#proveedores).

Aquí se mantiene la parte de calidad:
- Información de calidad. Estado de homologación. Certificaciones. Evaluación periódica (calidad, puntualidad, servicio).

El resto de la información del proveedor la mantienen otros departamentos:
- Información de compras, en [Compras](./compras.md#proveedor).
- Información fiscal y financiera, en [Administración general, Contabilidad y Finanzas](./administracion.md#proveedor).

Para evaluar la puntualidad del proveedor se usan los datos de entregas de [Compras](./compras.md) y de [Almacenes y Logística](./almacenes_y_logistica.md).

### Indicadores

#### Indicadores de calidad
- Rechazos (en ppm o en %). Reclamaciones. Tiempos de respuesta. Por periodo, artículo, cliente o proveedor.

#### Satisfacción de los clientes
- Encuestas. Puntuaciones. Comentarios. Por cliente y periodo.

También le interesa a [Marketing](./marketing.md) y a [Comercial y Ventas](./comercial_y_ventas.md).


## Algunos potenciales puntos de fricción

### Lecciones aprendidas de las no conformidades

Al cerrar una [Reclamación de cliente](./calidad.md#reclamación-de-cliente) o una [Acción correctiva o preventiva](./calidad.md#acción-correctiva-o-preventiva), Calidad ya ha resuelto el problema. Redactar además la lección aprendida, de forma que se pueda aplicar a otros productos o procesos, no le resuelve nada más. Pero es muy útil para:
- [Diseño técnico de productos](./diseño_tecnico.md) (no repetir el error en los diseños nuevos),
- [Fabricación o Servicios](./fabricacion_o_servicios.md#ruta-u-hoja-de-ruta) (al industrializar productos parecidos),
- [Compras](./compras.md#proveedor) (al seleccionar proveedores para piezas similares),
- [Comercial y Ventas](./comercial_y_ventas.md#oferta-o-presupuesto) (al aceptar exigencias parecidas de otro cliente),
- etc.

Para facilitar el registro:
- Un campo específico, breve, al cerrar la acción ("¿qué haríamos distinto la próxima vez?"), con etiquetas por familia de artículo, por proceso y por tipo de fallo para poder encontrarla después.

Para hacer ver su valor:
- Que las lecciones aparezcan solas donde se necesitan: en la revisión de un diseño nuevo de esa familia de artículos, en la petición de oferta de una pieza similar, etc. Una base de lecciones que nadie consulta acaba por no alimentarse.

### Valoración económica de los defectos

Para resolver una [No conformidad](./calidad.md#no-conformidad) basta con saber qué falla y cuántas piezas están afectadas. Cuánto cuesta (piezas desechadas, horas de reproceso, transportes, desplazamientos, penalizaciones) a Calidad no le hace falta para resolverla. Sin embargo, el [Coste de la no calidad](./calidad.md#coste-de-la-no-calidad) es un dato muy útil para:
- [Dirección](./direccion.md) (decidir dónde invertir en mejoras),
- [Administración general, Contabilidad y Finanzas](./administracion.md#rentabilidad) (rentabilidad real de productos y clientes),
- [Compras](./compras.md) (repercutir al proveedor lo que le corresponde),
- etc.

Para facilitar el registro:
- Que Calidad registre solo cantidades (piezas, horas, kilómetros) y que el sistema las valore con los costes estándar que ya mantiene Administración (ver [Coste estándar del artículo](./administracion.md#coste-estándar-del-artículo)).
- Recoger automáticamente lo que ya está en otros registros: horas de reproceso en los partes de fabricación, desplazamientos en los partes de intervención de Postventa, etc.

Para hacer ver su valor:
- Presentar los problemas de calidad en euros en las reuniones de dirección: un problema valorado consigue recursos para resolverse mucho antes que uno descrito solo en porcentaje de defectos.
