# Fabricación o Servicios

## Algunas entidades habituales

### Definición del proceso

#### Ruta u Hoja de ruta
- Operaciones y su secuencia. Puesto de trabajo de cada operación. Tiempos de preparación y de ejecución. Utillajes y herramientas.

Se elabora al industrializar un producto nuevo, partiendo de los planos y de la lista de materiales de [Diseño técnico de productos](./diseño_tecnico.md#lista-de-materiales-bom). 

Es la base para calcular costes (ver [Administración general, Contabilidad y Finanzas](./administracion.md#coste-estándar-del-artículo)).

Y para calcular cargas de trabajo.

#### Puesto o Centro de trabajo
- Máquinas o grupos de personas. Capacidad. Calendario y turnos. Coste por hora.

La disponibilidad real de las máquinas depende de [Mantenimiento de infraestructuras](./mantenimiento.md).

#### Instrucción de trabajo
- Pasos a seguir en cada operación. Diagramas, fotos o vídeos. Parámetros de proceso. Puntos de control. Versión.

Se guarda en el PDM y se consulta a pie de máquina.

#### Programa de máquina
- Programas de CNC, de robots o de PLC. Versión. Máquina en que se usa.

Se generan con CAM o con simulación *offline*, a partir de los modelos 3D de [Diseño técnico de productos](./diseño_tecnico.md#modelo-y-plano).

### Planificación

#### Plan maestro de producción
- Cantidades a fabricar por artículo (o familia) y periodo.

Parte de la [Previsión de ventas](./comercial_y_ventas.md#previsión-de-ventas) y de los pedidos en cartera.

#### Necesidades de materiales (MRP)
- Parámetros de planificación de cada artículo. Stock de seguridad. Tamaño de lote. Plazo.
- Propuestas de fabricación y de compra. Cantidades. Fechas.

Cruza el plan maestro con:
- las listas de materiales (BOM),
- el stock de [Almacenes y Logística](./almacenes_y_logistica.md)
- y los pedidos pendientes de [Compras](./compras.md).

Las necesidades de materiales se convierten en propuestas de compra.

#### Programa de producción
- Secuencia de órdenes en cada puesto de trabajo. Fechas previstas de inicio y de fin.

Se rehace cada vez que surge una incidencia.

Las simulaciones sobre un gemelo digital de la planta ayudan a ver su impacto antes de decidir.

### Ejecución

#### Orden de fabricación
- Artículo. Cantidad. Fechas. Ruta y lista de materiales aplicadas. Estado.

[Almacenes y Logística](./almacenes_y_logistica.md#orden-de-preparación-orden-de-picking) prepara y entrega los materiales que necesitan las órdenes de fabricación en curso.

#### Parte de fabricación
- Por operación. Cantidades buenas y defectuosas. Tiempos reales. Persona. Paros.

Es uno de los datos de Fabricación más útiles para otros departamentos tales como:
- [Administración general, Contabilidad y Finanzas](./administracion.md) (coste real),
- [Departamento de personal](./departamento_personal.md) (horas, incentivos),
- [Calidad](./calidad.md) (rechazos),
- [Mantenimiento de infraestructuras](./mantenimiento.md) (paros por avería),
- [Comercial y Ventas](./comercial_y_ventas.md#pedido) (avance de los pedidos),
- etc.

#### Consumo de material
- Artículos. Cantidades. Lotes. Orden de fabricación.

Descuenta stock en [Almacenes y Logística](./almacenes_y_logistica.md#stock).

#### Lote o Número de serie
- Qué se fabricó, cuándo y con qué orden de fabricación.
- Lotes de componentes y materias primas utilizados. Máquinas y personas que intervinieron. Parámetros de proceso.

Permite la trazabilidad: hacia atrás (de qué proveedor vino un componente defectuoso) y hacia delante (qué clientes recibieron un lote afectado).

La necesitan [Calidad](./calidad.md), [Postventa](./postventa.md#equipo-instalado) y, si hay que retirar producto del mercado, [Cumplimiento jurídico](./juridico.md).

#### Incidencia de fabricación
- Puesto. Orden. Causa (avería, falta de material, defecto de calidad, falta de personal...). Duración. Solución.

Según la causa, la ha de resolver otro departamento: [Mantenimiento de infraestructuras](./mantenimiento.md#aviso-o-solicitud-de-intervención), [Compras](./compras.md), [Almacenes y Logística](./almacenes_y_logistica.md), [Calidad](./calidad.md#no-conformidad),...

#### Datos de proceso
- Contadores, estados de las máquinas, alarmas, parámetros (temperaturas, presiones...).

Suelen recogerse automáticamente (SCADA). Así no hay que apuntarlos a mano.

Alimentan los partes, la trazabilidad y el mantenimiento predictivo.

### Indicadores

#### Rendimiento de las instalaciones (OEE)
- Disponibilidad. Rendimiento. Calidad. Por puesto, turno y periodo.

#### Coste real de fabricación
- Materiales, horas y gastos generales imputados a cada orden. Desviaciones respecto al coste previsto.

Lo calcula [Administración general, Contabilidad y Finanzas](./administracion.md) con los datos de los partes y de los consumos.

### Prestación de servicios

#### Orden de servicio
- Cliente. Servicio a prestar. Personas o equipos asignados. Fechas. Estado.

Viene de un [Contrato de servicio o Suscripción](./comercial_y_ventas.md#contrato-de-servicio-o-suscripción) o de un [Proyecto](./comercial_y_ventas.md#proyecto) que ha sido vendido por Comercial y Ventas.

#### Recurso
- Persona, equipo o vehículo. Cualificaciones. Disponibilidad. Coste por hora.

Las cualificaciones y las disponibilidades de las personas las mantiene [Departamento de personal](./departamento_personal.md).

#### Parte de horas o de actividad
- Persona. Fecha. Proyecto u orden de servicio. Horas. Tareas realizadas. Gastos.

Sirve a la vez para:
- facturar al cliente (ver [Administración general, Contabilidad y Finanzas](./administracion.md#factura-de-cliente)),
- controlar el avance de los proyectos,
- la nómina (ver [Departamento de personal](./departamento_personal.md)),
- el cálculo de costes,
- etc.


## Algunos potenciales puntos de fricción

### Causa de cada paro

Cuando una máquina se para, quien la atiende quiere volver a ponerla en marcha cuanto antes. Apuntar por qué se paró (avería, falta de material, cambio de formato, falta de personal, defecto de calidad...) no le ayuda en ese momento. Pero la causa, registrada en la [Incidencia de fabricación](./fabricacion_o_servicios.md#incidencia-de-fabricación), es muy útil para:
- [Mantenimiento de infraestructuras](./mantenimiento.md#aviso-o-solicitud-de-intervención) (averías que se repiten),
- [Compras](./compras.md) y [Almacenes y Logística](./almacenes_y_logistica.md) (faltas de material),
- [Calidad](./calidad.md#no-conformidad) (defectos),
- el [Rendimiento de las instalaciones (OEE)](./fabricacion_o_servicios.md#rendimiento-de-las-instalaciones-oee) que consulta [Dirección](./direccion.md),
- etc.

Para facilitar el registro:
- Que el paro, su hora de inicio y su duración los detecte la propia máquina (ver [Datos de proceso](./fabricacion_o_servicios.md#datos-de-proceso)). A la persona solo se le pide la causa.
- Una pantalla táctil junto a la máquina, con pocos botones grandes: las causas más habituales en ese puesto. Se puede detallar después, en un momento más tranquilo.
- Que elegir la causa sirva a la vez para avisar a quien la tiene que resolver: si es una avería, el aviso le llega a Mantenimiento.

Para hacer ver su valor:
- Un panel en la propia línea con los paros del turno y sus causas, y su evolución.
- Comentar en las reuniones de inicio de turno qué causas se han atacado gracias a esos datos.

### Lotes de los componentes consumidos

Al montar o al alimentar una máquina, a quien lo hace le basta con usar el componente correcto. De qué lote es le da igual. Sin embargo, registrar el lote en el [Consumo de material](./fabricacion_o_servicios.md#consumo-de-material) es lo que permite la trazabilidad hacia atrás del [Lote o Número de serie](./fabricacion_o_servicios.md#lote-o-número-de-serie) fabricado. Y esa trazabilidad la necesitan:
- [Calidad](./calidad.md#reclamación-de-cliente) (de qué lote de proveedor viene un defecto),
- [Compras](./compras.md#devolución-a-proveedor) (reclamar al proveedor),
- [Postventa](./postventa.md#equipo-instalado) y [Cumplimiento jurídico](./juridico.md) (qué equipos o qué clientes están afectados),
- etc.

Para facilitar el registro:
- Que [Almacenes y Logística](./almacenes_y_logistica.md#orden-de-preparación-orden-de-picking) entregue el material en kits ya asociados a la orden de fabricación, con el lote registrado en la preparación.
- Si no, leer la etiqueta del contenedor al empezar a usarlo; y que la orden no se pueda iniciar o cerrar sin esa lectura.

Para hacer ver su valor:
- Explicar casos reales en que la trazabilidad permitió acotar un problema a unas pocas unidades, en vez de revisar o retirar toda la producción de varias semanas.

### Tiempos reales y piezas defectuosas en el parte

El [Parte de fabricación](./fabricacion_o_servicios.md#parte-de-fabricación) pide cantidades buenas y defectuosas y tiempos reales. Para quien lo rellena, el trabajo ya está hecho; y a veces tiene la sensación de que esos datos sirven para controlarle. Pero son la base de:
- el [Coste real de fabricación](./fabricacion_o_servicios.md#coste-real-de-fabricación) y, a partir de él, de los precios (ver [Coste estándar del artículo](./administracion.md#coste-estándar-del-artículo)),
- la corrección de los tiempos de la [Ruta](./fabricacion_o_servicios.md#ruta-u-hoja-de-ruta), y por tanto de una planificación realista,
- [Calidad](./calidad.md) (rechazos),
- etc.

Para facilitar el registro:
- Tomar contadores y tiempos directamente de las máquinas siempre que se pueda; la persona solo confirma o corrige.
- Registrar inicio y fin de cada operación con una lectura de la hoja de la orden o del puesto, no tecleando horas al final del turno, de memoria.

Para hacer ver su valor:
- Separar claramente el uso de estos datos para mejorar el proceso del uso para evaluar a las personas. Si se mezclan, los datos se "maquillan" (las piezas defectuosas desaparecen, los tiempos se ajustan a lo esperado).
- Mostrar los cambios que se han hecho a partir de ellos: tiempos estándar corregidos, programas de producción que por fin se cumplen.

### Parte de horas en los proyectos y servicios

En una empresa de servicios, el [Parte de horas o de actividad](./fabricacion_o_servicios.md#parte-de-horas-o-de-actividad) suele ser la tarea más odiada de la semana. A quien lo rellena no le sirve para hacer su trabajo. Pero de él dependen:
- la [Factura de cliente](./administracion.md#factura-de-cliente) (en los servicios facturados por horas),
- el control del avance y del margen de cada [Proyecto](./comercial_y_ventas.md#proyecto),
- la [Nómina](./departamento_personal.md#nómina) (horas extra, desplazamientos),
- las estimaciones de las próximas ofertas,
- etc.

Para facilitar el registro:
- Proponerlo ya rellenado a partir de la agenda, de las órdenes de servicio asignadas o de la semana anterior; solo hay que corregir.
- Registrarlo cada día, desde el móvil, en menos de un minuto. A final de mes nadie se acuerda de en qué estuvo cada día.

Para hacer ver su valor:
- Que cada persona, y cada jefe de proyecto, vea el estado de sus proyectos: horas previstas frente a horas reales.
- Usar esos datos en las ofertas siguientes, y decirlo: "este presupuesto sale de las horas reales que registrasteis en proyectos parecidos".
