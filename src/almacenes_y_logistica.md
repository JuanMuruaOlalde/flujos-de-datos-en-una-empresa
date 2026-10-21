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

Las diferencias se valoran y se contabilizan (ver [Administración general, Contabilidad y Finanzas](./administracion.md#valoración-de-existencias)). Los recuentos cíclicos, por zonas o por artículos, evitan tener que parar completamente una vez al año para contarlo todo.

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


## Algunos potenciales puntos de fricción

### Lotes y números de serie en las salidas

Para preparar un pedido basta con coger el artículo y la cantidad correctos. Leer además el lote o el número de serie de cada bulto es un paso más, que al almacén no le aporta nada. Pero sin ese dato en el [Albarán de entrega](./almacenes_y_logistica.md#albarán-de-entrega) no hay trazabilidad hacia delante, y la necesitan:
- [Calidad](./calidad.md#reclamación-de-cliente) (qué clientes recibieron un lote defectuoso),
- [Postventa](./postventa.md#equipo-instalado) (qué número de serie tiene cada equipo instalado),
- [Cumplimiento jurídico](./juridico.md) (si hay que retirar producto del mercado),
- etc.

Para facilitar el registro:
- Etiquetas con código de barras o RFID en cada bulto, y una sola lectura que registre a la vez artículo, cantidad y lote.
- Que el terminal no dé por terminada la preparación hasta haber leído el lote. Sin texto que teclear, no hay errores de transcripción.

Para hacer ver su valor:
- Explicar casos reales de retirada de producto: con trazabilidad se avisa a unos pocos clientes; sin ella, hay que avisar a todos y revisarlo todo.

### Fecha real de entrega e incidencias de entrega

Una vez cargado el camión, el pedido sale del almacén y deja de ser asunto suyo. Lo que pasa después (cuándo llega, si llega completo, si llega dañado) lo sabe el transportista. Sin embargo, es un dato muy útil para:
- [Comercial y Ventas](./comercial_y_ventas.md#pedido) (puntualidad frente a la fecha comprometida, avisar al cliente de un retraso),
- [Administración general, Contabilidad y Finanzas](./administracion.md#factura-de-cliente) (el acuse de recibo firmado zanja muchas discusiones antes de cobrar),
- [Calidad](./calidad.md) (indicadores de servicio),
- etc.

Para facilitar el registro:
- Recibir automáticamente, por EDI o por la web del transportista, el seguimiento de cada [Envío](./almacenes_y_logistica.md#envío) y el acuse de recibo digital, enlazados al número de albarán.
- Exigirlo en el contrato con el transportista (ver [Compras](./compras.md#compra-de-servicios)).

Para hacer ver su valor:
- Que Logística vea los indicadores de entrega a tiempo de sus transportistas; le sirven para elegir entre ellos y para reclamarles.

### Pesos y dimensiones de los artículos

Los [Datos logísticos del artículo](./almacenes_y_logistica.md#datos-logísticos-del-artículo) se suelen dar de alta con prisa, cuando llega el primer pedido. Para almacenar basta con saber dónde cabe. Pero un peso o unas dimensiones mal dados afectan a:
- los transportes (tarifas, carga de camiones),
- la [huella de carbono](./prevencion_y_medioambiente.md#huella-de-carbono),
- los [envases y embalajes](./prevencion_y_medioambiente.md#envases-y-embalajes),
- las declaraciones de comercio exterior (ver [Declaración de impuestos](./administracion.md#declaración-de-impuestos)),
- etc.

Para facilitar el registro:
- Medir y pesar en la primera recepción, con una báscula y un medidor de volumen (cubicadora) que pasen los datos directamente al sistema.
- Pedírselos al proveedor junto con el resto de datos del artículo (ver [Fuente de aprovisionamiento](./compras.md#fuente-de-aprovisionamiento)), o tomarlos del modelo 3D de [Diseño técnico de productos](./diseño_tecnico.md#modelo-y-plano) si es de fabricación propia.

Para hacer ver su valor:
- Mostrar las diferencias entre lo que factura el transportista (que sí pesa) y lo calculado con los datos del sistema: son errores que se pagan.

### Casi accidentes

Una carretilla que casi atropella a alguien, una carga que casi cae... Como no ha pasado nada, nadie lo apunta. Es justo el tipo de dato que necesita [Prevención y Medio Ambiente](./prevencion_y_medioambiente.md#accidente-o-incidente) para actuar antes de que haya un accidente de verdad.

Para facilitar el registro:
- Un formulario muy corto, en el móvil o en un terminal del propio almacén: dónde, qué pasó, foto. Anónimo si se quiere.
- No pedir causas ni análisis a quien lo comunica; eso lo hace después Prevención.

Para hacer ver su valor:
- Responder siempre, y publicar qué se ha cambiado gracias a cada comunicación (un espejo, una señal, un cambio de recorrido).
- Nunca usarlo para buscar culpables. Si comunicar un casi accidente trae problemas, se deja de comunicar.
