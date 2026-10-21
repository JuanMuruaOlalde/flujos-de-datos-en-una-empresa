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
- Información de líneas: Artículos. Cantidades. Descuentos. Fecha de entrega comprometida.

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


## Algunos potenciales puntos de fricción

### Motivo de pérdida de una oferta

Lo conoce el comercial cuando el cliente le dice que no. Para él la oferta ya está cerrada: apuntar por qué se perdió no le ayuda a vender más mañana. En cambio, es muy útil para:
- [Marketing](./marketing.md#competidor) (precios y argumentos de la competencia),
- [Diseño técnico de productos](./diseño_tecnico.md) (lo que el producto no cubre),
- [Dirección](./direccion.md) (dónde se está perdiendo terreno),
- etc.

Para facilitar el registro:
- Pedirlo en el mismo gesto con que se marca la [Oportunidad](./comercial_y_ventas.md#oportunidad) como perdida, con una lista corta de motivos (precio, plazo, producto, competidor...) y un campo opcional para el competidor y su precio. Con una lista larga, se acaba eligiendo siempre "otros".
- Permitir registrarlo desde el móvil, nada más salir de la visita, o dictado por voz.

Para hacer ver su valor:
- Devolver periódicamente a los comerciales el resumen de motivos de pérdida, junto con lo que se ha hecho con ellos (un argumento nuevo, una opción de producto, un ajuste de precio).
- Lo que no funciona bien: hacerlo obligatorio sin devolver nada. Se rellena, pero con el primer motivo de la lista.

### Información recogida en las visitas

Necesidades del cliente, proyectos que tiene en marcha, cambios en su organización, competidores con los que trabaja... El comercial lo lleva en la cabeza y le basta. Registrado como [Acción comercial](./comercial_y_ventas.md#acción-comercial), es útil:
- para [Marketing](./marketing.md#estudio-de-mercado) (tendencias del mercado),
- para quien atiende al cliente cuando el comercial no está (vacaciones, bajas, cambio de cartera),
- para [Postventa](./postventa.md) y [Calidad](./calidad.md) (contexto cuando hay una reclamación),
- etc.

Para facilitar el registro:
- Que el CRM esté en el móvil y que registrar una visita lleve menos de un minuto: cliente, fecha y contacto ya rellenos a partir de la agenda; el resto, texto libre o voz.
- Aceptar registros incompletos (más vale una nota breve que nada) y no exigir campos que nadie va a usar.

Para hacer ver su valor:
- Que el propio comercial lo aproveche: preparar la siguiente visita leyendo lo anotado en la anterior, ver de un vistazo el historial del cliente.
- Hay que dejar claro que no es una herramienta de control de su actividad. Si se percibe así, se registra lo justo para cubrir el expediente.

### Previsión de ventas realista

La hacen los comerciales, pero a ellos les sirve poco: lo que les importa es el pedido. Es uno de los datos de Ventas más útiles para otros departamentos (ver [Previsión de ventas](./comercial_y_ventas.md#previsión-de-ventas)). Tiene además un problema de fondo: si la previsión se confunde con los [Objetivos de ventas](./comercial_y_ventas.md#objetivos-de-ventas), cada cual la ajusta según le convenga (a la baja para superar el objetivo, o al alza para conseguir más recursos).

Para facilitar el registro:
- Partir de una previsión estadística calculada a partir del histórico; el comercial solo corrige lo que sabe que va a cambiar (un cliente nuevo, un proyecto que se cae).
- Pedirla al nivel de detalle que realmente se usa (familia de artículos y mes, por ejemplo), no artículo a artículo.

Para hacer ver su valor:
- Separar claramente previsión y objetivo. La previsión es lo que se cree que va a pasar; el objetivo, lo que se quiere que pase.
- Medir y publicar el acierto de las previsiones, sin penalizar.
- Mostrar la relación con lo que sí le importa al comercial: las roturas de stock y los retrasos en las entregas a sus clientes salen, muchas veces, de previsiones mal hechas.
