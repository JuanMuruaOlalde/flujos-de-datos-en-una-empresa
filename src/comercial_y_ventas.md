# Comercial y Ventas

## Algunas entidades habituales

### Clientes y contactos

#### cliente

El núcleo común (código, razón social, identificación fiscal) está en los [Datos maestros](./datos_maestros.md#clientes). 

Aquí se mantiene la parte comercial:
- Información comercial. Comercial asignado. Categorías de cliente. Lista de precios y descuentos aplicables. Idioma.

El resto de la información del cliente la mantienen otros departamentos:
- Información fiscal y financiera, en [Administración general, Contabilidad y Finanzas](./administracion.md#cliente).
- Información logística, en [Almacenes y Logística](./almacenes_y_logistica.md#cliente).

#### cliente potencial
También llamado *lead*. Alguien que aún no compra.
- Información básica. Nombre o razón social. Origen (feria, web, recomendación...).
- Estado. Cuándo pasa a ser Cliente y quién lo decide.

#### persona de contacto
- Información de contacto. Nombre. Cargo. Teléfono. Email. Idioma.
- Cliente o potencial cliente al que pertenece.

Son datos personales, sujetos a la normativa de protección de datos (ver [Cumplimiento jurídico](./juridico.md)).


### Maestros para ventas

#### referencia cruzada de artículos
- Código y descripción con que cada cliente denomina a nuestros artículos.

Imprescindible si se intercambian pedidos por EDI.

#### listas de precios
Por tipo de cliente. Por zonas. Por épocas del año.

#### descuentos, promociones y rappels
- Descuentos. Por cliente. Por familia de artículos. Por cantidad.
- Promociones. Periodo de validez.
- Rappels. Descuentos por volumen anual. Escalas.

Los rappels se han de ir provisionando en contabilidad (ver [Administración general, Contabilidad y Finanzas](./administracion.md#provisión)).

#### contrato o acuerdo marco
- Precios y condiciones pactados con un cliente para un periodo. Volúmenes comprometidos.

Ver también [Cumplimiento jurídico](./juridico.md).

#### condiciones de entrega
- Incoterms. Portes. Plazos de entrega.


### Gestión del ciclo de ventas

#### acción comercial
Una entrada en el CRM

#### oportunidad
- Fase. Probabilidad. Importe estimado. Fecha prevista de cierre.

Alimenta el embudo de ventas (*pipeline*).

#### oferta o presupuesto
- Información de cabecera. Fechas. Validez. Versión.
- Información de líneas. Artículos. Cantidades. Precios.

En empresas industriales suele necesitar la colaboración de [Diseño técnico de productos](./diseño_tecnico.md) (configuración, ingeniería de oferta).

#### pedido
- Información de cabecera. Fechas. Condiciones.
- Información de líneas. Articulos. Cantidades. Descuentos. Fecha de entrega comprometida.

Para comprometer una fecha de entrega hay que consultar la disponibilidad en [Almacenes y Logística](./almacenes_y_logistica.md#stock) o la capacidad de [Fabricación o Servicios](./fabricacion_o_servicios.md).

#### contrato de servicio o suscripción
- Periodicidad. Cuotas recurrentes. Renovaciones.

#### proyecto
- Hitos. Horas. Facturación por avance.

#### devolución o abono
- Artículos y cantidades devueltos. Motivo. Importe a abonar.

A caballo con [Postventa](./postventa.md).



### Organización y objetivos

#### comercial y su cartera
- Clientes, zonas o canales asignados a cada comercial.

#### categorías de cliente
- Zona. Canal (venta directa, distribuidor, online...). Segmento. Sector.

#### objetivos de ventas
- Por comercial, zona, cliente o familia de artículos. Por periodo.

#### previsión de ventas
- Cantidades previstas por artículo (o familia) y periodo.

Es uno de los datos de Ventas más útiles para otros departamentos: [Compras](./compras.md), [Fabricación o Servicios](./fabricacion_o_servicios.md), [Almacenes y Logística](./almacenes_y_logistica.md), [Dirección](./direccion.md).

#### comisiones
- Reglas de cálculo. Importes devengados por cada comercial.

Acaban en la nómina (ver [Departamento de personal](./departamento_personal.md)).


