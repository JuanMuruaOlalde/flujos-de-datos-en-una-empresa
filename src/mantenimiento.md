# Mantenimiento de infraestructuras

## Algunas entidades habituales

### Instalaciones

#### Activo o Equipo
- Instalación, máquina, edificio o vehículo. Dónde está y de qué forma parte (jerarquía). Criticidad.
- Fabricante. Modelo. Número de serie. Fecha de puesta en marcha. Garantía.

El mismo equipo suele aparecer en contabilidad como inmovilizado, con otro código (ver [Administración general, Contabilidad y Finanzas](./administracion.md#inmovilizado)). Conviene tener enlazados ambos.

#### Documentación de la instalación
- Planos y esquemas. Manuales de servicio. Programas de PLC y de robots (copias de seguridad). Modelo BIM.

Se guarda en el PDM y se mantiene al día, versionado, con cada modificación. Si no, la próxima avería se diagnostica a ciegas.

#### Repuesto
- Artículos de repuesto de cada equipo. Stock mínimo. Ubicación. Proveedor.

Los repuestos críticos han de estar siempre en almacén.

### Mantenimiento correctivo

#### Aviso o Solicitud de intervención
- Quién avisa. Equipo. Síntoma. Prioridad. Fecha y hora.

La mayoría de avisos vienen de [Fabricación o Servicios](./fabricacion_o_servicios.md#incidencia-de-fabricación). Algunos, de alarmas automáticas de las propias máquinas.

#### Orden de trabajo
- Tipo (correctivo, preventivo, predictivo, mejora). Equipo. Técnicos. Horas. Repuestos utilizados. Coste.
- Causa del fallo. Solución aplicada.

El historial de órdenes de cada equipo permite calcular el tiempo medio entre averías y el tiempo medio de reparación. Además de llevar un registro de la vida de cada equipo.

### Mantenimiento planificado

#### Plan de mantenimiento preventivo
- Tareas por equipo. Frecuencia, por tiempo o por uso (horas, ciclos). Próxima fecha prevista.

Hay que acordar con [Fabricación o Servicios](./fabricacion_o_servicios.md) cuándo se para cada máquina.

#### Lectura de contador o de condición
- Horas de funcionamiento. Ciclos. Vibraciones. Temperaturas.

Se recogen automáticamente (SCADA), siempre que se pueda.

Permite el mantenimiento predictivo: intervenir justo antes de que falle.

Permite el análisis post-mortem: identificar señales previas al fallo.

#### Inspección reglamentaria
- Instalaciones sujetas a inspección obligatoria (eléctricas, de presión, de protección contra incendios, ascensores...). Organismo inspector. Fechas. Resultado. Defectos a corregir.

Ver también [Prevención y Medio Ambiente](./prevencion_y_medioambiente.md) y [Cumplimiento jurídico](./juridico.md#normativa-o-requisito-legal).

### Recursos

#### Técnico de mantenimiento
- Especialidad. Habilitaciones (eléctricas, frigoristas...). Turno. Disponibilidad.

Las habilitaciones y la disponibilidad las mantiene [Departamento de personal](./departamento_personal.md#cualificación).

#### Empresa de mantenimiento externa
- Contrato. Equipos que atiende. Tiempos de respuesta.

Se contrata a través de [Compras](./compras.md#compra-de-servicios).

Para trabajar en nuestras instalaciones, cualquier subcontrata necesita la [Coordinación de actividades empresariales](./prevencion_y_medioambiente.md#coordinación-de-actividades-empresariales).

### Energía y suministros

#### Consumo de energía y suministros
- Electricidad, gas, agua, aire comprimido... Por contador, por instalación y por periodo.

Lo necesitan:
- [Administración general, Contabilidad y Finanzas](./administracion.md) (costes)
- y [Prevención y Medio Ambiente](./prevencion_y_medioambiente.md#huella-de-carbono) (huella de carbono).

### Mejoras y ampliaciones

#### Proyecto de mejora o de ampliación
- Objetivo. Presupuesto. Plazos. Instalaciones afectadas.

El diseño y la programación se pueden ensayar y simular antes en un gemelo digital de la planta, para que el cambio afecte lo menos posible a la producción. Al acabar, hay que actualizar la documentación de la instalación.

Si es una inversión, pasa por [Dirección](./direccion.md#inversión).


## Algunos potenciales puntos de fricción

### Horas y repuestos de cada orden de trabajo

Al técnico le importa arreglar la avería. Apuntar con detalle cuántas horas ha empleado y qué repuestos ha usado, en la [Orden de trabajo](./mantenimiento.md#orden-de-trabajo), es para él un trámite. Pero esos datos los necesitan:
- [Almacenes y Logística](./almacenes_y_logistica.md#stock) y [Compras](./compras.md) (reponer los repuestos consumidos),
- [Administración general, Contabilidad y Finanzas](./administracion.md) (coste de mantenimiento de cada equipo),
- [Dirección](./direccion.md#inversión) (decidir si se sigue reparando un equipo o se sustituye),
- etc.

Para facilitar el registro:
- Fichar el inicio y el fin de la orden con el móvil, leyendo la etiqueta del equipo; las horas salen solas.
- Leer la etiqueta de cada repuesto al cogerlo del almacén, ya asociado a la orden de trabajo.

Para hacer ver su valor:
- Que Mantenimiento vea el coste acumulado de cada equipo, y lo use para defender una inversión o una mejora. Es el argumento con más peso cuando se pide sustituir una máquina.

### Consumo de energía por instalación

Los contadores dependen de Mantenimiento, que vela por que los suministros funcionen. El reparto del consumo por instalación, por centro de coste o por producto le preocupa poco. Pero el [Consumo de energía y suministros](./mantenimiento.md#consumo-de-energía-y-suministros) detallado lo necesitan:
- [Prevención y Medio Ambiente](./prevencion_y_medioambiente.md#huella-de-carbono) (huella de carbono, también por producto),
- [Administración general, Contabilidad y Finanzas](./administracion.md#coste-estándar-del-artículo) (repartir el coste de la energía a cada producto),
- [Dirección](./direccion.md) (ahorros, inversiones en eficiencia),
- etc.

Para facilitar el registro:
- Contadores con lectura automática, conectados al SCADA o a un sistema de gestión energética. Leer contadores a mano, una vez al mes, da datos tardíos y poco detallados.
- Instalar contadores parciales en las instalaciones que más consumen, no en todas.

Para hacer ver su valor:
- Usar esos mismos datos para detectar fugas de aire comprimido, consumos fuera de horario o equipos que consumen más de lo normal. Son ahorros que Mantenimiento puede apuntarse.

### Altas, bajas y cambios de los equipos

Cuando se desmonta una máquina, se traslada a otro centro o se modifica a fondo, Mantenimiento lo sabe porque lo hace. Actualizar el [Activo o Equipo](./mantenimiento.md#activo-o-equipo) y la [Documentación de la instalación](./mantenimiento.md#documentación-de-la-instalación) no le urge. Pero es imprescindible para:
- [Administración general, Contabilidad y Finanzas](./administracion.md#inmovilizado) (dar de baja el inmovilizado),
- [Prevención y Medio Ambiente](./prevencion_y_medioambiente.md#evaluación-de-riesgos) (revisar la evaluación de riesgos),
- la [Póliza de seguro](./administracion.md#póliza-de-seguro) (capitales asegurados),
- [Calidad](./calidad.md) (procesos que hay que volver a validar),
- etc.

Para facilitar el registro:
- Que cualquier proyecto de mejora o de ampliación (ver [Proyecto de mejora o de ampliación](./mantenimiento.md#proyecto-de-mejora-o-de-ampliación)) no se pueda cerrar sin actualizar los equipos afectados y su documentación.
- Un único aviso de "cambio en equipo" que llegue a la vez a todos los que lo necesitan, en vez de que Mantenimiento tenga que acordarse de avisar a cada uno.

Para hacer ver su valor:
- La propia documentación actualizada es lo que necesitará el técnico que atienda la siguiente avería.
