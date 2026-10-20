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

Ver también [Prevención y Medio Ambiente](./prevencion_y_medioambiente.md) y [Cumplimiento jurídico](./juridico.md#requisito-legal).

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
