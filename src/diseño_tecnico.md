# Diseño técnico de productos

## Algunas entidades habituales

### Desarrollo del producto

#### Modelo y plano
- Modelo 3D. Planos 2D. Especificaciones de fabricación y de montaje.
- Versionado. Estado (en diseño, aprobado, obsoleto). Quién lo aprueba y cuándo.

Se guardan en el PDM. Se guarda histórico de todas las versiones. Con especial indicación de las dós últimas versiones: la actualmente vigente y la anterior.

Suelen ser consultados por variadas partes. Sobre todo por:
- [Fabricación o Servicios](./fabricacion_o_servicios.md),
- [Compras](./compras.md),
- [Proveedores](./compras.md#petición-de-oferta),
- [Subcontrataciones](./compras.md#subcontratación)
- [Postventa](./postventa.md),
- etc.

[Marketing](./marketing.md) también suele acceder a modelos y planos. Para la elaboración de catálogos, videos,...

Al aprobarse un artículo nuevo, se da de alta en los [Datos maestros](./datos_maestros.md#artículos) para que el resto de la empresa pueda trabajar con él.

#### Lista de materiales (BOM)
- Componentes de cada producto. Cantidades. Versión. Fechas de validez.

También llamada BOM (*bill of materials*).

De un mismo producto suele haber varias variantes:
- la lista de diseño,
- la lista de fabricación (organizada según el proceso, ver [Fabricación o Servicios](./fabricacion_o_servicios.md#ruta-u-hoja-de-ruta))
- la lista de servicio (con los repuestos, ver [Postventa](./postventa.md#repuesto)),
- etc.

Pasan del PDM al ERP; mantener ambos sistemas sincronizados es una de las integraciones más delicadas.

#### Especificación técnica
- Requisitos que ha de cumplir. Materiales. Tolerancias. Normas aplicables. Características críticas.

[Compras](./compras.md#petición-de-oferta) la envía a los proveedores.

[Calidad](./calidad.md#plan-de-control) la utiliza para preparar los planes de control.

#### Cálculo, Simulación o Ensayo
- Qué se comprueba. Modelo o prototipo utilizado. Condiciones. Resultados. Conclusiones.

Primero sobre modelos digitales (CAE) y después sobre prototipos físicos.

#### Prototipo
- Versión del diseño. Cómo se hizo (impresión 3D, taller propio, proveedor). Ensayos realizados. Coste.

#### Invención
- Descripción. Inventores. Fecha. Decisión (patentar, mantener en secreto, publicar).

Si se patenta, pasa a [Cumplimiento jurídico](./juridico.md#patente-marca-o-diseño-registrado).

### Gestión de cambios

#### Solicitud de cambio o Petición de estudio
- Quién lo pide. Qué artículo. Motivo. Urgencia. Decisión.

ECR (Engineering Change Request), ECO (Engineering Change Order)

Pueden llegar desde variadas partes:
- [Postventa](./postventa.md#solución-conocida)
- [Calidad](./calidad.md#acción-correctiva-o-preventiva) (fallos),
- [Fabricación o Servicios](./fabricacion_o_servicios.md) (dificultades de fabricación),
- [Compras](./compras.md) (componentes que dejan de fabricarse),
- [Comercial y Ventas](./comercial_y_ventas.md) (peticiones de clientes),
- etc.

#### Orden de cambio
- Artículos y documentos afectados. Nueva versión. Fecha a partir de la cual se aplica.
- Qué hacer con el stock y los pedidos existentes (agotar, reprocesar, desechar).

La notificación de lo que se ha cambiado tiene que llegar a tiempo a:
- [Compras](./compras.md),
- [Fabricación o Servicios](./fabricacion_o_servicios.md),
- [Almacenes y Logística](./almacenes_y_logistica.md),
- [Calidad](./calidad.md)
- y [Postventa](./postventa.md).

Si alguno se entera tarde, se compra o se fabrica la versión antigua.

### Ofertas y configuración

#### Reglas de configuración
- Opciones de cada producto. Compatibilidades e incompatibilidades. Coste de cada opción.

Permiten a [Comercial y Ventas](./comercial_y_ventas.md#oferta-o-presupuesto) configurar un producto sin consultar cada vez a la oficina técnica.

#### Ingeniería de oferta
- Estudio técnico de una petición especial. Solución propuesta. Estimación de horas y de costes.

Para las [Ofertas](./comercial_y_ventas.md#oferta-o-presupuesto) que no se resuelven con las reglas de configuración.

### Documentación de producto

#### Documento técnico
- Manual de uso, de mantenimiento, instrucciones de montaje, catálogo técnico... Versión. Idiomas. Artículos y revisiones a los que aplica.

Mejor redactarlo como documento estructurado y modular, reaprovechando textos y gráficos del resto del PDM. Existen diversos productos sofware para redacción de documentos técnicos.

Los documentos técnicos suelen ser consultados por múltiples partes:
- [Postventa](./postventa.md),
- [Almacenes y Logística](./almacenes_y_logistica.md) (manuales de mantenimiento)
- [Marketing](./marketing.md),
- los propios clientes,
- etc.

#### Glosario y Memoria de traducción
- Términos técnicos y su traducción aprobada en cada idioma. Frases ya traducidas.

Ahorra traducciones y mantiene la coherencia. Por ejemplo: en los documentos técnicos, en las descripciones en varios idiomas de los [Datos maestros](./datos_maestros.md#artículos),...

#### Expediente técnico y Declaración de conformidad
- Normas y directivas aplicables. Ensayos. Análisis de riesgos. Declaración firmada.

Necesarios para poner el producto en el mercado (por ejemplo, con el marcado CE). Ver también [Cumplimiento jurídico](./juridico.md#requisito-legal).
