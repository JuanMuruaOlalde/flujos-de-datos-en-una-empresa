# Compras

## Algunas entidades habituales

### Proveedores y contactos

#### Proveedor

El núcleo común (código, razón social, identificación fiscal) está en los [Datos maestros](./datos_maestros.md#proveedores).

Aquí se mantiene la parte de compras:
- Información de compras. Comprador asignado. Categorías de proveedor. Condiciones de compra. Idioma.

El resto de la información del proveedor la mantienen otros departamentos:
- Información fiscal y financiera, en [Administración general, Contabilidad y Finanzas](./administracion.md#proveedor).
- Información de calidad, en [Calidad](./calidad.md#proveedor).

#### Potencial proveedor
- Información básica. Nombre o razón social. Qué puede suministrar. Origen (feria, búsqueda, recomendación...).
- Estado. Cuándo pasa a ser Proveedor y quién lo decide.

Normalmente no se le puede comprar a un cierto proveedor hasta que [Calidad](./calidad.md#proveedor) lo homologa.

#### Persona de contacto
- Información de contacto. Nombre. Cargo. Teléfono. Email. Idioma.
- Proveedor o potencial proveedor al que pertenece.

Son datos personales, sujetos a la normativa de protección de datos (ver [Cumplimiento jurídico](./juridico.md)).

#### Fuente de aprovisionamiento
- Qué proveedores pueden suministrar cada artículo. Proveedor preferente. Reparto entre varios proveedores.
- Por cada proveedor y artículo: código y descripción con que lo denomina el proveedor. Unidad de compra. Lote mínimo. Plazo de entrega.

Imprescindible si se intercambian pedidos por EDI.

### Condiciones de compra

#### Tarifa del proveedor
- Precios por artículo. Escalas por cantidad. Periodo de validez. Moneda.

#### Contrato o acuerdo marco
- Precios y condiciones pactados con un proveedor para un periodo. Volúmenes comprometidos.

Ver también [Cumplimiento jurídico](./juridico.md).

#### Condiciones de entrega
- Incoterms. Portes. Plazos de entrega. Embalaje y etiquetado exigidos.

El embalaje y el etiquetado los suele definir [Almacenes y Logística](./almacenes_y_logistica.md#embalaje).

### Ciclo de compra

#### Solicitud de compra
- Quién la pide. Para qué. Artículos o servicios. Cantidades. Fecha en que se necesita. Centro de coste. Aprobación.

Puede venir de cualquier departamento, o generarse automáticamente desde la planificación de necesidades (ver [Fabricación o Servicios](./fabricacion_o_servicios.md#necesidades-de-materiales-mrp)).

#### Petición de oferta
- Proveedores consultados. Artículos o servicios. Cantidades. Fecha límite de respuesta.

Para artículos nuevos o artículos especiales hay que adjuntar planos y especificaciones de [Diseño técnico de productos](./diseño_tecnico.md).

#### Oferta del proveedor
- Precios. Plazos. Condiciones. Validez.

Comparando las de varios proveedores se elige a quién comprar.

#### Pedido de compra
- Información de cabecera: Fechas. Condiciones.
- Información de líneas: Artículos. Cantidades. Precios. Fecha de entrega solicitada y fecha confirmada por el proveedor.

El proveedor puede recibirlo por EDI o consultarlo (y confirmarlo) en un portal de proveedores. [Almacenes y Logística](./almacenes_y_logistica.md#previsión-de-llegadas) necesita conocerlo para preparar las recepciones.

#### Seguimiento de entregas
- Pedidos con retraso. Reclamaciones al proveedor. Nuevas fechas.

Los retrasos afectan a la planificación de [Fabricación o Servicios](./fabricacion_o_servicios.md) y/o a las fechas comprometidas por [Comercial y Ventas](./comercial_y_ventas.md#pedido).

#### Recepción
- Albarán del proveedor. Artículos y cantidades recibidos. Fecha. Pedido al que corresponde.

La registra [Almacenes y Logística](./almacenes_y_logistica.md#recepción). Si hay inspección, suele ser [Calidad](./calidad.md#inspección) decide si se acepta o no la recepción.

#### Factura de proveedor
- Información de cabecera: Fecha. Vencimientos.
- Información de líneas: Artículos. Cantidades. Precios. Impuestos.

La registra [Administración general, Contabilidad y Finanzas](./administracion.md#factura-de-proveedor). Antes de pagarla se cruza con el pedido y con la recepción: que lo facturado se haya pedido, que se haya recibido y que haya sido Ok; además de que los precios en factura coincidan con los acordados en el pedido.

#### Devolución a proveedor
- Artículos y cantidades devueltos. Motivo. Abono o reposición esperados.

Suele partir de una no conformidad de [Calidad](./calidad.md#no-conformidad).

### Organización y objetivos

#### Comprador y su cartera
- Categorías de compra, familias de artículos o proveedores asignados a cada comprador.

#### Categorías de proveedor
- Tipo de suministro (materias primas, componentes, subcontratación, servicios, transporte...). Criticidad. Zona.

#### Presupuesto de compras
- Por categoría, familia de artículos o centro de coste. Por periodo.

Se elabora a partir de:
- la [Previsión de ventas](./comercial_y_ventas.md#previsión-de-ventas)
- y los planes de [Fabricación o Servicios](./fabricacion_o_servicios.md).

#### Análisis del gasto
- Importes comprados por proveedor, categoría, artículo y periodo. Ahorros conseguidos.

Lo consulta [Dirección](./direccion.md).

Es también la base de las emisiones indirectas en la huella de carbono (ver [Prevención y Medio Ambiente](./prevencion_y_medioambiente.md#huella-de-carbono)).

### Subcontratación

#### Pedido de subcontratación
- Operación o trabajo encargado. Material que enviamos al subcontratista. Material que nos devuelve.

El subcontratista necesita consultar en el PDM los planos y especificaciones de lo que ha de fabricar (ver [Diseño técnico de productos](./diseño_tecnico.md)).

Nosotros hemos de controlar cuánto material nuestro tiene en su casa (ver [Almacenes y Logística](./almacenes_y_logistica.md#almacén)).

#### Compra de servicios
- Servicio contratado. Periodo. Certificación de lo realizado (horas, hitos).

Si el proveedor trabaja en nuestras instalaciones, hay que coordinar con él la prevención de riesgos (ver [Prevención y Medio Ambiente](./prevencion_y_medioambiente.md#coordinación-de-actividades-empresariales)).


## Algunos potenciales puntos de fricción

### Fecha confirmada por el proveedor y sus cambios

El proveedor confirma una fecha de entrega, o la cambia, normalmente por correo o por teléfono. El comprador ya sabe la fecha y no siente la necesidad de actualizar el [Pedido de compra](./compras.md#pedido-de-compra). Pero esa fecha la necesitan:
- [Fabricación o Servicios](./fabricacion_o_servicios.md#necesidades-de-materiales-mrp) (la planificación cuenta con el material en la fecha que dice el sistema),
- [Comercial y Ventas](./comercial_y_ventas.md#pedido) (fechas comprometidas a los clientes),
- [Almacenes y Logística](./almacenes_y_logistica.md#previsión-de-llegadas) (organizar las descargas),
- [Calidad](./calidad.md#proveedor) (puntualidad del proveedor),
- etc.

Para facilitar el registro:
- Que sea el propio proveedor quien confirme y modifique las fechas, por EDI o en un portal de proveedores. El comprador solo revisa las que no le cuadran.
- Avisos automáticos de pedidos sin confirmar o con la fecha vencida, para pedir la confirmación antes de que sea tarde.

Para hacer ver su valor:
- Mostrar al comprador qué órdenes de fabricación o qué pedidos de clientes dependen de cada pedido de compra. Un retraso deja de ser una fecha en un correo y pasa a ser un cliente concreto que no recibirá a tiempo.

### Datos de sostenibilidad y de cumplimiento de los proveedores

País de origen, certificados, emisiones, fichas de datos de seguridad de los productos químicos, información sobre sustancias restringidas, comprobaciones en listas de sanciones... Al comprador le basta con el precio, el plazo y la calidad. Pero estos datos los necesitan:
- [Prevención y Medio Ambiente](./prevencion_y_medioambiente.md#huella-de-carbono) (huella de carbono, [productos químicos](./prevencion_y_medioambiente.md#producto-químico), [Informe de sostenibilidad](./prevencion_y_medioambiente.md#informe-de-sostenibilidad)),
- [Cumplimiento jurídico](./juridico.md#control-de-exportaciones) (sanciones, debida diligencia en la cadena de suministro),
- [Almacenes y Logística](./almacenes_y_logistica.md#documentación-aduanera) (origen, para las aduanas),
- etc.

Para facilitar el registro:
- Pedirlos una sola vez, al dar de alta al proveedor, con un cuestionario único que recoja lo que piden todos los departamentos; y actualizarlos con campañas periódicas, no cada cual por su cuenta.
- Que el proveedor los cargue y los mantenga en el portal de proveedores, con fechas de caducidad y avisos automáticos.
- Aprovechar las plataformas compartidas en las que el proveedor ya ha cargado esa información para otros clientes.

Para hacer ver su valor:
- Incluir estos datos en la evaluación del proveedor y en la decisión de compra. Si nunca influyen en nada, el comprador los verá como burocracia.

### Motivo de la elección de un proveedor

Después de comparar varias [Ofertas de proveedor](./compras.md#oferta-del-proveedor), el comprador sabe por qué ha elegido una. Para él la decisión ya está tomada. Pero dejarlo registrado es útil:
- para auditorías y para [Cumplimiento jurídico](./juridico.md#mapa-de-riesgos-de-cumplimiento) (demostrar que no hubo favoritismos),
- para [Dirección](./direccion.md) (por qué no se eligió la oferta más barata),
- para el siguiente comprador que tenga que repetir la compra,
- etc.

Para facilitar el registro:
- Un comparativo de ofertas generado por el sistema a partir de las ofertas recibidas, en el que solo hay que marcar la elegida y escoger el motivo.
- Exigirlo solo por encima de un cierto importe.

Para hacer ver su valor:
- Que el propio comprador pueda consultar, en la siguiente compra, qué se pagó, a quién, y por qué se descartó a los demás.
