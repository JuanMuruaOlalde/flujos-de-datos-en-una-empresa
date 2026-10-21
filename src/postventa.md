# Postventa

## Algunas entidades habituales

### Parque instalado

#### Equipo instalado
- Artículo. Número de serie. Cliente. Ubicación. Fecha de instalación o de puesta en marcha.
- Configuración real tal como se entregó (opciones, versiones de software, componentes sustituidos después).
- Historial de intervenciones.

El número de serie enlaza con la trazabilidad de [Fabricación o Servicios](./fabricacion_o_servicios.md#lote-o-número-de-serie).

#### Garantía
- Equipo o artículo. Fechas de inicio y de fin. Qué cubre (piezas, mano de obra, desplazamientos).

Decide si una intervención se factura o no.

#### Documentación de la instalación
- Planos y esquemas tal como se construyó. Manuales. Programas y parámetros cargados.

En instalaciones grandes o personalizadas a medida para un cliente. Se guarda en el PDM, junto a la documentación de producto de [Diseño técnico de productos](./diseño_tecnico.md).

#### Datos de uso del equipo
- Horas de funcionamiento. Alarmas. Lecturas de sensores.

Recibidos a distancia, si el equipo está conectado.

Permiten pasar del mantenimiento preventivo al predictivo. Y son una fuente muy valiosa para [Diseño técnico de productos](./diseño_tecnico.md) y [Marketing](./marketing.md): ya que permiten ver cómo se usa realmente el producto.

### Atención al cliente

#### Incidencia o Reclamación
- Cliente. Persona de contacto. Equipo afectado. Canal (teléfono, email, web, técnico en visita). Fecha.
- Descripción. Gravedad. Estado. Plazos de respuesta y de resolución comprometidos.

Las reclamaciones por defectos van también a [Calidad](./calidad.md#reclamación-de-cliente).

#### Solución conocida
- Síntoma. Causa. Solución. Equipos o versiones a los que aplica.

Una base de conocimiento que crece con cada intervención. Ahorra tiempo a los técnicos y da pistas de mejora a [Diseño técnico de productos](./diseño_tecnico.md).

### Intervenciones

#### Aviso u Orden de servicio
- Incidencia o mantenimiento que la origina. Equipo. Técnico asignado. Fecha prevista. Prioridad.

Para asignar un técnico hay que conocer su disponibilidad y su cualificación (ver [Departamento de personal](./departamento_personal.md#cualificación)).

#### Parte de intervención
- Trabajos realizados. Horas. Desplazamientos. Repuestos utilizados. Causa del fallo.
- Fotos. Firma del cliente.

Es uno de los datos de Postventa más útiles para otros departamentos:
- [Administración general, Contabilidad y Finanzas](./administracion.md#factura-de-cliente) (facturar lo que no cubre la garantía),
- [Departamento de personal](./departamento_personal.md) (horas, dietas),
- [Almacenes y Logística](./almacenes_y_logistica.md) (repuestos consumidos),
- [Calidad](./calidad.md)
- [Diseño técnico de productos](./diseño_tecnico.md) (fallos en campo),
- etc.

#### Repuesto
- Artículos de repuesto de cada equipo. Stock en almacén y en los vehículos de los técnicos. Plazo de suministro.

Hay que garantizarlos durante años, aunque el producto ya no se fabrique.

#### Devolución o RMA
- Equipo o artículo devuelto. Motivo. Diagnóstico. Decisión (reparar, sustituir, abonar).

Se gestionan a caballo con [Comercial y Ventas](./comercial_y_ventas.md#devolución-o-abono).

### Contratos de servicio

#### Contrato de mantenimiento
- Equipos cubiertos. Nivel de servicio (tiempo de respuesta, horario). Visitas preventivas incluidas.

Lo vende [Comercial y Ventas](./comercial_y_ventas.md#contrato-de-servicio-o-suscripción). Postventa se encarga de cumplirlo.

#### Plan de mantenimiento de equipos de clientes
- Tareas preventivas. Frecuencia. Próxima visita.

Parecido al que mantiene [Mantenimiento de infraestructuras](./mantenimiento.md#plan-de-mantenimiento-preventivo) para las instalaciones propias.


## Algunos potenciales puntos de fricción

### Causa del fallo en el parte de intervención

La conoce el técnico, pero lo que a él le importa es dejar el equipo funcionando y pasar al siguiente aviso. Registrada en el [Parte de intervención](./postventa.md#parte-de-intervención), la causa del fallo es muy útil para:
- [Diseño técnico de productos](./diseño_tecnico.md#solicitud-de-cambio-o-petición-de-estudio) (fallos que se repiten),
- [Calidad](./calidad.md#acción-correctiva-o-preventiva) (acciones correctivas),
- [Compras](./compras.md#proveedor) (componentes de un proveedor que fallan más),
- etc.

Para facilitar el registro:
- Una lista corta de causas por familia de equipo, en el móvil, y texto libre solo para los casos raros.
- Proponer la causa más probable a partir de los síntomas y de las [Soluciones conocidas](./postventa.md#solución-conocida); el técnico solo la confirma o la corrige.
- Admitir una foto de la pieza dañada como registro mínimo; la codificación la puede hacer después otra persona.

Para hacer ver su valor:
- Devolverle al técnico la base de soluciones conocidas que se construye con esas causas: ve que lo que registra hoy le ahorra tiempo mañana, a él y a sus compañeros.
- Contar qué cambios de diseño o de proveedor se han hecho gracias a esos datos.
- No convertirlo en un indicador individual. Si una causa "le compromete", acabará registrándose otra más inocua.

### Configuración real del equipo después de la intervención

Cuando se sustituye un componente por otro de distinta versión, o se actualiza el software, el [Equipo instalado](./postventa.md#equipo-instalado) deja de ser como se entregó. Al técnico que está allí no le hace falta apuntarlo: lo está viendo. Pero lo necesitan:
- el siguiente técnico que vaya (y que preparará los repuestos según lo que dice el sistema),
- la [trazabilidad](./fabricacion_o_servicios.md#lote-o-número-de-serie), si hay que localizar los equipos con un componente defectuoso,
- [Comercial y Ventas](./comercial_y_ventas.md) (equipos antiguos, candidatos a renovación o a mejora),
- etc.

Para facilitar el registro:
- Que registrar el repuesto montado (leyendo su etiqueta o su número de serie) actualice automáticamente la configuración del equipo.
- Para el software, que el propio equipo informe de su versión si está conectado (ver [Datos de uso del equipo](./postventa.md#datos-de-uso-del-equipo)).

Para hacer ver su valor:
- Recordar los casos en que un técnico se desplazó con el repuesto equivocado porque la configuración no estaba al día.

### Repuestos consumidos del vehículo

El técnico coge del vehículo lo que necesita y sigue trabajando. Si no registra el consumo:
- el stock de [Almacenes y Logística](./almacenes_y_logistica.md#stock) no es real,
- no se puede facturar al cliente lo que no cubre la garantía (ver [Factura de cliente](./administracion.md#factura-de-cliente)),
- [Compras](./compras.md) no repone a tiempo,
- etc.

Para facilitar el registro:
- Leer la etiqueta del repuesto con el móvil al usarlo, dentro del propio parte de intervención.
- Proponer los repuestos habituales de esa avería, para que solo haya que confirmarlos.

Para hacer ver su valor:
- Reponer el vehículo automáticamente según lo consumido. Así el primer beneficiado es el propio técnico: lo que registra hoy es lo que encontrará repuesto mañana; lo que no registra, le faltará.
