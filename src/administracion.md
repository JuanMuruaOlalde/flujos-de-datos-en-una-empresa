# Administración general, Contabilidad y Finanzas

## Algunas entidades habituales

### Clientes y proveedores

#### Cliente

El núcleo común (código, razón social, identificación fiscal) está en los [Datos maestros](./datos_maestros.md#clientes).

Aquí se mantienen la parte fiscal y la financiera:
- Información fiscal. Dirección fiscal. Régimen de impuestos.
- Información financiera. Formas de pago. Límite de crédito (riesgo).

El resto de la información del cliente la mantienen otros departamentos:
- Información comercial, en [Comercial y Ventas](./comercial_y_ventas.md#cliente).
- Información logística, en [Almacenes y Logística](./almacenes_y_logistica.md#cliente).

#### Proveedor

El núcleo común (código, razón social, identificación fiscal) está en los [Datos maestros](./datos_maestros.md#proveedores).

Aquí se mantienen la parte fiscal y la financiera:
- Información fiscal. Dirección fiscal. Régimen de impuestos.
- Información financiera. Formas de pago. Cuenta bancaria.

El resto de la información del proveedor la mantienen otros departamentos:
- Información de compras, en [Compras](./compras.md#proveedor).
- Información de calidad, en [Calidad](./calidad.md#proveedor).

Las peticiones de cambio de cuenta bancaria son un intento de fraude muy habitual: hay que confirmarlas siempre por otro canal.

### Facturación

#### Factura de cliente
- Información de cabecera: Sociedad que factura. Cliente. Fecha. Forma de pago. Vencimientos.
- Información de líneas: Artículos o servicios. Cantidades. Precios. Descuentos. Impuestos.

Las facturas se generan a partir de lo entregado o realizado:
- [Albaranes de entrega](./almacenes_y_logistica.md#albarán-de-entrega), 
- [Partes de horas](./fabricacion_o_servicios.md#parte-de-horas-o-de-actividad) o hitos de proyecto, 
- [Partes de intervención](./postventa.md#parte-de-intervención) fuera de garantía, 
- cuotas de [Contratos de servicio](./comercial_y_ventas.md#contrato-de-servicio-o-suscripción),
- etc. 

En cada vez más países ha de ser electrónica y comunicarse a la administración tributaria en el momento de emitirla.

#### Factura rectificativa o Abono
- Factura que corrige. Motivo. Importes.

Suele venir de una [Devolución o Abono](./comercial_y_ventas.md#devolución-o-abono) de Comercial y Ventas, o de la liquidación de los rappels.

#### Factura de proveedor

Su contenido, y el cruce con el pedido y la recepción, están en [Compras](./compras.md#factura-de-proveedor).

Aquí se añade:
- Contabilización. Cuenta de gasto o de existencias. Centro de coste. Impuestos deducibles.
- Vencimientos de pago.

Las diferencias de precio o de cantidad las ha de aclarar Compras antes de pagarla.

### Cobros y pagos

#### Vencimiento de cobro
- Factura. Cliente. Importe. Fecha de vencimiento. Forma de cobro (transferencia, recibo domiciliado, pagaré...). Estado.

#### Riesgo de cliente
- Límite de crédito concedido (ver [Cliente](./administracion.md#cliente)). Riesgo vivo: pedidos pendientes de servir y facturas pendientes de cobro. Cobertura del seguro de crédito.

[Comercial y Ventas](./comercial_y_ventas.md#pedido) lo ha de consultar antes de aceptar un pedido. Si se supera el límite, el pedido queda bloqueado hasta que alguien lo autorice.

#### Impagado
- Cliente. Facturas. Importe. Gestiones de cobro realizadas. Acuerdos de pago.

Comercial y Ventas ha de saberlo enseguida, antes de aceptar nuevos pedidos de ese cliente. Si acaba en los tribunales, pasa a [Cumplimiento jurídico](./juridico.md#litigio-o-reclamación-judicial).

#### Vencimiento de pago
- Factura. Proveedor (o empleado, o administración pública). Importe. Fecha de vencimiento. Forma de pago. Estado.

Se suelen pagar por remesas.

#### Movimiento bancario
- Cuenta. Fecha. Importe. Concepto. Cobro o pago al que corresponde.

Los extractos llegan solos del banco. Lo laborioso es casar cada movimiento con su factura; mucho más fácil si el cliente indica en la transferencia qué factura paga.

#### Previsión de tesorería
- Cobros y pagos previstos por semana o por mes. Saldo previsto en cada cuenta.

Se nutre de múltiples fuentes: 
- vencimientos de cobro y de pago de facturas, 
- estimaciones cuándo tocará cobrar o pagar los pedidos pendientes, 
- pago de nóminas, 
- previsiones de pago de impuestos,
- estimaciones de rendimiento de inversiones,
- etc.

#### Financiación
- Préstamos, pólizas de crédito, líneas de descuento, *leasing*, avales. Entidad. Importe. Tipo de interés. Vencimientos. Garantías.

Para firmarlos hace falta un [Poder](./juridico.md#poder-o-apoderamiento). Muchos avales los piden los clientes en contratos y licitaciones (ver [Comercial y Ventas](./comercial_y_ventas.md#contrato-o-acuerdo-marco)).

### Contabilidad

#### Plan de cuentas
- Cuentas contables y su estructura.

En un grupo multinacional suele haber un plan de cuentas común y uno local en cada país, con su tabla de equivalencias. Es un caso claro de maestro global con variantes locales (ver [Datos maestros](./datos_maestros.md#plan-de-cuentas)).

#### Asiento contable
- Sociedad. Fecha. Cuentas. Importes al debe y al haber. Centro de coste. Documento de origen.

La mayoría se generan solos a partir de facturas, cobros, pagos, nóminas, movimientos de almacén... registrados en otros departamentos. Cuanto mejores sean los datos de origen, menos asientos manuales hay que hacer.

#### Centro de coste
- Departamento, sección o proyecto al que se imputan gastos e ingresos. Responsable.

Lo han de indicar todos los que piden compras o registran gastos (ver [Solicitud de compra](./compras.md#solicitud-de-compra) y [Gasto de viaje](./departamento_personal.md#gasto-de-viaje)).

#### Inmovilizado
- Bien. Fecha y valor de adquisición. Vida útil. Amortización. Ubicación. Fecha de baja.

Las altas vienen de las [Inversiones](./direccion.md#inversión). La misma instalación es en Mantenimiento un [Activo o Equipo](./mantenimiento.md#activo-o-equipo), normalmente con otro código: conviene tenerlos enlazados.

#### Provisión
- Motivo (rappels, litigios, garantías, clientes dudosos, stock obsoleto...). Importe. Periodo.

Los datos para calcular provisiones pueden venir de varias fuentes:
- rappels de [Comercial y Ventas](./comercial_y_ventas.md#descuentos-promociones-y-rappels),
- litigios de [Cumplimiento jurídico](./juridico.md#litigio-o-reclamación-judicial),
- garantías de [Postventa](./postventa.md#garantía),
- stock obsoleto de [Almacenes y Logística](./almacenes_y_logistica.md#stock-obsoleto-o-sin-movimiento),
- etc.

#### Cierre y Cuentas anuales
- Balance. Cuenta de resultados. Memoria. Informe de auditoría. Depósito en el registro.

Antes de cada cierre hace falta que todos los departamentos hayan registrado lo suyo: recepciones, consumos, partes, facturas... Después de cada cierre ya no se puede inputar nada con fecha anterior al cierre; las correcciones van como correcciones en el siguiente periodo.

Las cuentas anuales han de depositarse en el registro. El cierre anual es una obligación legal.

#### Consolidación
- Cuentas de cada [Sociedad](./juridico.md#sociedad) del grupo. Operaciones entre sociedades del grupo, que hay que eliminar. Conversión de monedas.

Las ventas y compras entre sociedades del grupo han de coincidir en ambos lados; si no, cuadrarlas lleva mucho tiempo.

### Costes y control de gestión

#### Coste estándar del artículo
- Materiales, mano de obra y gastos generales previstos para cada artículo. Fecha de cálculo.

Se calcula con:
- la [Lista de materiales](./diseño_tecnico.md#lista-de-materiales),
- la [Ruta](./fabricacion_o_servicios.md#ruta-u-hoja-de-ruta),
- las tarifas de [Compras](./compras.md#tarifa-del-proveedor),
- el coste por hora de cada [Puesto](./fabricacion_o_servicios.md#puesto-o-centro-de-trabajo),
- etc.

Comercial y Ventas lo necesita para fijar precios.

Comparándo el coste estándar con el [Coste real](./fabricacion_o_servicios.md#coste-real-de-fabricación) salen las desviaciones.

#### Valoración de existencias
- Valor del stock por artículo y almacén. Método de valoración (coste estándar, precio medio...).

Las cantidades las da [Almacenes y Logística](./almacenes_y_logistica.md#stock); el valor, Contabilidad.

#### Rentabilidad
- Margen por cliente, artículo, familia, canal, proyecto o comercial.

Se calcula cruzando las ventas con los costes.

Lo consultan [Dirección](./direccion.md#cuadro-de-mando) y [Comercial y Ventas](./comercial_y_ventas.md).

#### Seguimiento del presupuesto
- Real frente a presupuesto, por centro de coste y cuenta. Desviaciones. Explicaciones.

El presupuesto lo aprueba [Dirección](./direccion.md#presupuesto-anual).

Cada responsable de centro de coste ha de explicar sus desviaciones.

### Impuestos

#### Declaración de impuestos
- Impuesto (sobre el valor añadido, sobre sociedades, retenciones, impuestos especiales...). Periodo. Importe. Fecha de presentación.

Salen sobre todo de las facturas y de las nóminas. Aunque algunos impuestos necesitan datos muy específicos de otros departamentos: los de envases (ver [Prevención y Medio Ambiente](./prevencion_y_medioambiente.md#envases-y-embalajes)), los códigos arancelarios y pesos para las estadísticas de comercio exterior (ver [Almacenes y Logística](./almacenes_y_logistica.md#datos-logísticos-del-artículo)), etc.

### Seguros

#### Póliza de seguro
- Riesgo cubierto (daños, responsabilidad civil, transporte, crédito...). Aseguradora. Capitales. Franquicias. Vencimiento.

Para fijar los capitales hace falta el valor de las instalaciones y del stock. Ver también [Cumplimiento jurídico](./juridico.md#contrato).

#### Siniestro
- Fecha. Qué ha pasado. Póliza. Daños. Reclamación a la aseguradora. Indemnización.

Los datos los aportan quienes sufren el daño: [Almacenes y Logística](./almacenes_y_logistica.md#incidencia-de-entrega) (mercancía dañada en el transporte), [Mantenimiento de infraestructuras](./mantenimiento.md#orden-de-trabajo) (averías, incendios), [Prevención y Medio Ambiente](./prevencion_y_medioambiente.md#accidente-o-incidente) (accidentes), etc.
