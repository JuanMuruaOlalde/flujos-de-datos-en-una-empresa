# Comercial y Ventas

## Algunas entidades habituales

### Clientes y contactos

#### Cliente

El núcleo común (código, razón social, identificación fiscal) está en los [Datos maestros](./datos_maestros.md#clientes). 

Aquí se mantiene la parte comercial:
- Información comercial. Comercial asignado. Categorías de cliente. Lista de precios y descuentos aplicables. Idioma.

El resto de la información del cliente la mantienen otros departamentos:
- Información fiscal y financiera, en [Administración general, Contabilidad y Finanzas](./administracion.md#cliente).
- Información logística, en [Almacenes y Logística](./almacenes_y_logistica.md#cliente).

#### Cliente potencial
También llamado *lead*, es alguien que aún no compra.
- Información básica. Nombre o razón social. Origen (feria, web, recomendación...).
- Estado. Cuándo pasa a ser Cliente y quién lo decide.

#### Persona de contacto
- Información de contacto. Nombre. Cargo. Teléfono. Email. Idioma.
- Cliente o potencial cliente al que pertenece.

Son datos personales, sujetos a la normativa de protección de datos (ver [Cumplimiento jurídico](./juridico.md)).


### Maestros para ventas

#### Referencia cruzada de artículos
- Código y descripción con que cada cliente denomina a nuestros artículos.

Imprescindible si se intercambian pedidos por EDI.

#### Listas de precios
Por tipo de cliente. Por zonas. Por épocas del año.

#### Descuentos, promociones y rappels
- Descuentos. Por cliente. Por familia de artículos. Por cantidad.
- Promociones. Periodo de validez.
- Rappels. Descuentos por volumen anual. Escalas.

Los rappels se han de ir provisionando en contabilidad (ver [Administración general, Contabilidad y Finanzas](./administracion.md#provisión)).

#### Contrato o acuerdo marco
- Precios y condiciones pactados con un cliente para un periodo. Volúmenes comprometidos.

Ver también [Cumplimiento jurídico](./juridico.md).

#### Condiciones de entrega
- Incoterms. Portes. Plazos de entrega.


### Gestión del ciclo de ventas

#### Acción comercial
Una entrada en el CRM

#### Oportunidad
- Fase. Probabilidad. Importe estimado. Fecha prevista de cierre.

Alimenta el embudo de ventas (*pipeline*).

#### Oferta o presupuesto
- Información de cabecera: Fechas. Validez. Versión.
- Información de líneas: Artículos. Cantidades. Precios.

En empresas industriales suele necesitar la colaboración de [Diseño técnico de productos](./diseño_tecnico.md) (configuración, ingeniería de oferta).

#### Pedido
- Información de cabecera: Fechas. Condiciones.
- Información de líneas: Articulos. Cantidades. Descuentos. Fecha de entrega comprometida.

Para comprometer una fecha de entrega hay que consultar la disponibilidad en [Almacenes y Logística](./almacenes_y_logistica.md#stock) o la capacidad de [Fabricación o Servicios](./fabricacion_o_servicios.md).

#### Contrato de servicio o suscripción
- Periodicidad. Cuotas recurrentes. Renovaciones.

#### Proyecto
- Hitos. Horas. Facturación por avance.

#### Devolución o abono
- Artículos y cantidades devueltos. Motivo. Importe a abonar.

Se gestionan a caballo con [Postventa](./postventa.md).



### Organización y objetivos

#### Comercial y su cartera
- Clientes, zonas o canales asignados a cada comercial.

#### Categorías de cliente
- Zona. Canal (venta directa, distribuidor, online...). Segmento. Sector.

#### Objetivos de ventas
- Por comercial, zona, cliente o familia de artículos. Por periodo.

#### Previsión de ventas
- Cantidades previstas por artículo (o familia) y periodo.

Es uno de los datos de Ventas más útiles para otros departamentos, tales como:
- [Compras](./compras.md),
- [Fabricación o Servicios](./fabricacion_o_servicios.md),
- [Almacenes y Logística](./almacenes_y_logistica.md),
- [Dirección](./direccion.md),
- etc.

#### Comisiones
- Reglas de cálculo. Importes devengados por cada comercial.

Acaban en la nómina (ver [Departamento de personal](./departamento_personal.md)).


