# Almacenes y Logística

## Algunas entidades habituales

### Clientes y transportistas

#### Cliente

El núcleo común (código, razón social, identificación fiscal) está en los [Datos maestros](./datos_maestros.md#clientes).

Aquí se mantiene la parte logística:
- Información logística. Puntos de entrega. Horarios de recepción. Exigencias de embalaje y de etiquetado. Transportista habitual.

El resto de la información del cliente la mantienen otros departamentos:
- Información comercial, en [Comercial y Ventas](./comercial_y_ventas.md#cliente).
- Información fiscal y financiera, en [Administración general, Contabilidad y Finanzas](./administracion.md#cliente).

#### Transportista
- Zonas y servicios que cubre. Tarifas por zona, peso y volumen. Plazos. Cómo se intercambian los datos de los envíos (web, EDI).

Un transportista es un proveedor más (ver [Datos maestros](./datos_maestros.md#proveedores)): lo contrata [Compras](./compras.md#compra-de-servicios), pero quien trabaja con él a diario es Logística.

### Almacenes y artículos

#### Almacén
- Centro. Dirección. Tipo (materias primas, producto terminado, repuestos...). Responsable.

En el sistema, un almacén no siempre es un edificio propio. También se definen almacenes para controlar aspectos tales como, por ejemplo:
- el material en casa de un subcontratista (ver [Pedido de subcontratación](./compras.md#pedido-de-subcontratación)),
- el que llevan en sus vehículos los técnicos de [Postventa](./postventa.md#repuesto),
- el que está en consigna en casa de un cliente,
- el que va de camino entre dos centros (en tránsito),
- el que acabamos de descargar y está pendiente de contar/almacenar,
- el que acabamos de contar/preparar y está pendiente de cargar,
- etc.

#### Ubicación
- Zona, pasillo, estantería, hueco. Capacidad. Tipo (de preparación, de reserva, refrigerada, para productos peligrosos...).

Los productos químicos solo pueden ir en zonas preparadas para ellos (ver [Prevención y Medio Ambiente](./prevencion_y_medioambiente.md#producto-químico)).

#### Datos logísticos del artículo
- Unidades de medida (de almacén, de compra, de venta) y sus conversiones. Dimensiones y peso. Unidades por caja y por palé.
- Condiciones de conservación (temperatura, caducidad). Si se controla por lotes o por números de serie.
- Código arancelario y país de origen, para las aduanas.

Los necesitan también otros departamentos como, por ejemplo:
- [Compras](./compras.md#fuente-de-aprovisionamiento) (unidades de compra), 
- [Comercial y Ventas](./comercial_y_ventas.md) (unidades de venta), 
- los transportistas (peso y volumen de los envíos),
- [Administración general, Contabilidad y Finanzas](./administracion.md#declaración-de-impuestos) (estadísticas de comercio exterior),
- etc.

#### Embalaje
- Tipos de embalaje (cajas, palés, contenedores retornables). Instrucciones de embalaje por artículo o por cliente. Material y peso.
- Embalajes retornables que están en poder de clientes y proveedores.

De aquí salen las exigencias de embalaje y de etiquetado a los proveedores (ver [Compras](./compras.md#condiciones-de-entrega)) y los datos de envases que necesita [Prevención y Medio Ambiente](./prevencion_y_medioambiente.md#envases-y-embalajes).

### Existencias

#### Stock
- Artículo. Almacén. Ubicación. Lote o número de serie. Cantidad. Estado (disponible, reservado para un pedido o una orden, bloqueado por calidad, en tránsito).

El stock es uno de los datos de Almacenes más útiles para otros departamentos como, por ejemplo:
- [Comercial y Ventas](./comercial_y_ventas.md#pedido) (qué se puede prometer),
- [Fabricación o Servicios](./fabricacion_o_servicios.md#necesidades-de-materiales-mrp)
- [Compras](./compras.md) (qué falta),
- [Administración general, Contabilidad y Finanzas](./administracion.md#valoración-de-existencias) (cuánto vale),
- etc.

#### Movimiento de stock
- Entrada, salida o traspaso. Artículo. Cantidad. Lote. Ubicaciones de origen y de destino. Fecha y hora. Persona. Documento que lo origina (recepción, orden de fabricación, pedido, ajuste).

Mejor registrarlo en el momento, leyendo las etiquetas (códigos de barras, RFID) con terminales fijos o móviles, que apuntarlo y teclearlo después.

#### Traspaso entre almacenes
- Artículos. Cantidades. Almacenes de origen y de destino. Fechas de envío y de llegada.

Mientras viaja, el material está en tránsito: ha salido de un almacén pero aún no ha llegado al otro.

#### Inventario físico
- Recuento por ubicación. Diferencias con el stock del sistema. Ajustes y su motivo.

Las diferencias se valoran y se contabilizan (ver [Administración general, Contabilidad y Finanzas](./administracion.md#valoración-de-existencias)). Los recuentos cíclicos, por zonas o por artículos, evitan tener que parar comnpletamente una vez al año para contarlo todo.

#### Stock obsoleto o sin movimiento
- Artículos sin salidas desde hace tiempo, caducados o de revisiones antiguas. Cantidad. Valor.

Muchas veces viene de [Órdenes de cambio](./diseño_tecnico.md#orden-de-cambio) o de previsiones de venta que no se cumplieron. Hay que decidir qué hacer con él, y puede requerir una [Provisión](./administracion.md#provisión).

### Entradas

#### Previsión de llegadas
- Pedidos de compra pendientes de recibir. Avisos de envío de los proveedores (qué viene, cuándo, en cuántos bultos).

Sale de los [Pedidos de compra](./compras.md#pedido-de-compra). Con ella se organizan los muelles y las personas de descarga.

#### Recepción

Los datos del albarán y del pedido están en [Compras](./compras.md#recepción). Aquí se añade:
- Comprobación física. Bultos. Cantidades. Daños visibles.
- Etiquetado. Ubicación donde queda.

Si el material se ha de inspeccionar antes de utilizarlo, queda bloqueado hasta que [Calidad](./calidad.md#inspección) lo libera.

#### Devolución de cliente
- Artículos devueltos. Estado en que llegan. Destino (al stock, a reparar, a desechar).

Ver [Devolución o Abono](./comercial_y_ventas.md#devolución-o-abono) y [Devolución o RMA](./postventa.md#devolución-o-rma).

### Salidas

#### Orden de preparación (orden de *picking*)
- Pedidos a servir. Artículos. Cantidades. Ubicaciones de donde cogerlos. Persona. Fecha.

Se elaboran a partir de:
- los [Pedidos](./comercial_y_ventas.md#pedido) de clientes,
- las [Órdenes de fabricación](./fabricacion_o_servicios.md#orden-de-fabricación) (materiales a llevar a planta),
- los traspasos entre almacenes,
- etc.

#### Albarán de entrega
- Cliente. Punto de entrega. Artículos. Cantidades. Lotes o números de serie. Fecha.

Los albaranes entregados son la base de las [Facturas de cliente](./administracion.md#factura-de-cliente). Los lotes y números de serie entregados completan la [trazabilidad](./fabricacion_o_servicios.md#lote-o-número-de-serie) de producto y, si procede, el [parque instalado](./postventa.md#equipo-instalado) de Postventa.

#### Envío
- Transportista. Bultos. Peso y volumen. Coste. Número de seguimiento. Fecha real de entrega. Acuse de recibo.
- Documentación especial si son mercancías peligrosas.

La fecha real de entrega permite medir la puntualidad frente a la fecha comprometida por [Comercial y Ventas](./comercial_y_ventas.md#pedido).

Los pesos y las distancias sirven para calcular la [huella de carbono](./prevencion_y_medioambiente.md#huella-de-carbono).

#### Incidencia de entrega
- Envío. Tipo (retraso, daño, pérdida, entrega incompleta o equivocada). Responsable. Reclamación al transportista.

Comercial y Ventas ha de saberlo para avisar al cliente. Si hay daños, puede dar lugar a un [Siniestro](./administracion.md#siniestro).

#### Documentación aduanera
- Exportaciones e importaciones. Código arancelario. Origen. Valor. Incoterm. Declaración de aduanas.

Necesita datos:
- de [Comercial y Ventas](./comercial_y_ventas.md#condiciones-de-entrega) (precios, Incoterms),
- del artículo (código arancelario, origen)
- del [Control de exportaciones](./juridico.md#control-de-exportaciones),
- etc.

### Planificación e indicadores

#### Previsión de carga de trabajo
- Recepciones y expediciones previstas por día. Personas y muelles necesarios.

Sale de los pedidos de compra, de los pedidos de clientes y de la [Previsión de ventas](./comercial_y_ventas.md#previsión-de-ventas).

#### Clasificación ABC de artículos
- Por número de movimientos o por valor.

Decide qué ubicaciones se asignan (los que más se mueven conviene tenerlos más cerca de los muelles) y cada cuánto se cuentan (los de mayor valor ha de estar más controlados).

#### Indicadores logísticos
- Entregas a tiempo y completas. Errores de preparación. Exactitud del inventario. Rotación del stock. Coste logístico por pedido o por kilo.
- Puntualidad de los proveedores.

La puntualidad de los proveedores la usa [Calidad](./calidad.md#proveedor) para evaluarlos.
