# Fabricación o Servicios

## Algunas entidades habituales

### Definición del proceso

#### Ruta u Hoja de ruta
- Operaciones y su secuencia. Puesto de trabajo de cada operación. Tiempos de preparación y de ejecución. Utillajes y herramientas.

Se elabora al industrializar un producto nuevo, partiendo de los planos y de la lista de materiales de [Diseño técnico de productos](./diseño_tecnico.md#lista-de-materiales). Es la base para calcular costes (ver [Administración general, Contabilidad y Finanzas](./administracion.md#coste-estándar-del-artículo)) y cargas de trabajo.

#### Puesto o Centro de trabajo
- Máquinas o grupos de personas. Capacidad. Calendario y turnos. Coste por hora.

La disponibilidad real de las máquinas depende de [Mantenimiento de infraestructuras](./mantenimiento.md).

#### Instrucción de trabajo
- Pasos a seguir en cada operación. Fotos o vídeos. Parámetros de proceso. Puntos de control. Versión.

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

Cruza el plan maestro con las listas de materiales, el stock de [Almacenes y Logística](./almacenes_y_logistica.md) y los pedidos pendientes de [Compras](./compras.md). Las propuestas de compra se convierten en solicitudes o pedidos de compra.

#### Programa de producción
- Secuencia de órdenes en cada puesto de trabajo. Fechas previstas de inicio y de fin.

Se rehace cada vez que surge una incidencia. Las simulaciones sobre un gemelo digital de la planta ayudan a ver su impacto antes de decidir.

### Ejecución

#### Orden de fabricación
- Artículo. Cantidad. Fechas. Ruta y lista de materiales aplicadas. Estado.

[Almacenes y Logística](./almacenes_y_logistica.md#orden-de-preparación) prepara y entrega los materiales que necesita.

#### Parte de fabricación
- Por operación. Cantidades buenas y defectuosas. Tiempos reales. Persona. Paros.

Es uno de los datos de Fabricación más útiles para otros departamentos: [Administración general, Contabilidad y Finanzas](./administracion.md) (coste real), [Departamento de personal](./departamento_personal.md) (horas, incentivos), [Calidad](./calidad.md) (rechazos), [Mantenimiento de infraestructuras](./mantenimiento.md) (paros por avería), [Comercial y Ventas](./comercial_y_ventas.md#pedido) (avance de los pedidos).

#### Consumo de material
- Artículos. Cantidades. Lotes. Orden de fabricación.

Descuenta stock en [Almacenes y Logística](./almacenes_y_logistica.md#stock).

#### Lote o Número de serie
- Qué se fabricó, cuándo y con qué orden.
- Lotes de componentes y materias primas utilizados. Máquinas y personas que intervinieron. Parámetros de proceso.

Permite la trazabilidad: hacia atrás (de qué proveedor vino un componente defectuoso) y hacia delante (qué clientes recibieron un lote afectado). La necesitan [Calidad](./calidad.md), [Postventa](./postventa.md#equipo-instalado) y, si hay que retirar producto del mercado, [Cumplimiento jurídico](./juridico.md).

#### Incidencia de fabricación
- Puesto. Orden. Causa (avería, falta de material, defecto de calidad, falta de personal...). Duración. Solución.

Según la causa, la ha de resolver otro departamento: [Mantenimiento de infraestructuras](./mantenimiento.md#aviso-o-solicitud-de-intervención), [Compras](./compras.md), [Almacenes y Logística](./almacenes_y_logistica.md), [Calidad](./calidad.md#no-conformidad)...

#### Datos de proceso
- Contadores, estados de las máquinas, alarmas, parámetros (temperaturas, presiones...). Recogidos automáticamente (SCADA).

Así no hay que apuntarlos a mano. Alimentan los partes, la trazabilidad y el mantenimiento predictivo.

### Indicadores

#### Rendimiento de las instalaciones (OEE)
- Disponibilidad. Rendimiento. Calidad. Por puesto, turno y periodo.

#### Coste real de fabricación
- Materiales, horas y gastos generales imputados a cada orden. Desviaciones respecto al coste previsto.

Lo calcula [Administración general, Contabilidad y Finanzas](./administracion.md) con los datos de los partes y de los consumos.

### Prestación de servicios

#### Orden de servicio
- Cliente. Servicio a prestar. Personas o equipos asignados. Fechas. Estado.

Viene de un [Contrato de servicio o Suscripción](./comercial_y_ventas.md#contrato-de-servicio-o-suscripción) o de un [Proyecto](./comercial_y_ventas.md#proyecto) vendidos por Comercial y Ventas.

#### Recurso
- Persona, equipo o vehículo. Cualificaciones. Disponibilidad. Coste por hora.

Las cualificaciones y las ausencias de las personas las mantiene [Departamento de personal](./departamento_personal.md).

#### Parte de horas o de actividad
- Persona. Fecha. Proyecto u orden de servicio. Horas. Tareas realizadas. Gastos.

Sirve a la vez para facturar al cliente (ver [Administración general, Contabilidad y Finanzas](./administracion.md#factura-de-cliente)), para controlar el avance de los proyectos y para la nómina (ver [Departamento de personal](./departamento_personal.md)).
