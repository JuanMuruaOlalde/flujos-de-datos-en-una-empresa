# Diseño técnico de productos

## Algunas entidades habituales

### Desarrollo del producto

#### Modelo y plano
- Modelo 3D. Planos 2D. Especificaciones de fabricación y de montaje.
- Revisión. Estado (en diseño, aprobado, obsoleto). Quién lo aprueba y cuándo.

Se guardan en el PDM. Al aprobarse un artículo nuevo, se da de alta en los [Datos maestros](./datos_maestros.md#artículos) para que el resto de la empresa pueda trabajar con él.

#### Lista de materiales
- Componentes de cada artículo. Cantidades. Revisión. Fechas de validez.

También llamada BOM (*bill of materials*). De un mismo producto suele haber varias: la de diseño, la de fabricación (organizada según el proceso, ver [Fabricación o Servicios](./fabricacion_o_servicios.md#ruta-u-hoja-de-ruta)) y la de servicio (con los repuestos, ver [Postventa](./postventa.md#repuesto)). Pasa del PDM al ERP; mantener ambos sincronizados es una de las integraciones más delicadas.

#### Especificación técnica
- Requisitos que ha de cumplir. Materiales. Tolerancias. Normas aplicables. Características críticas.

[Calidad](./calidad.md#plan-de-control) la utiliza para preparar los planes de control. Y [Compras](./compras.md#petición-de-oferta) la envía a los proveedores.

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

Llegan de todas partes: [Postventa](./postventa.md#solución-conocida) y [Calidad](./calidad.md#acción-correctiva-o-preventiva) (fallos), [Fabricación o Servicios](./fabricacion_o_servicios.md) (dificultades de fabricación), [Compras](./compras.md) (componentes que dejan de fabricarse), [Comercial y Ventas](./comercial_y_ventas.md) (peticiones de clientes).

#### Orden de cambio
- Artículos y documentos afectados. Nueva revisión. Fecha a partir de la cual se aplica.
- Qué hacer con el stock y los pedidos existentes (agotar, reprocesar, desechar).

Tiene que llegar a tiempo a [Compras](./compras.md), [Fabricación o Servicios](./fabricacion_o_servicios.md), [Almacenes y Logística](./almacenes_y_logistica.md), [Calidad](./calidad.md) y [Postventa](./postventa.md). Si alguno se entera tarde, se compra o se fabrica la revisión antigua.

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

Mejor como documento estructurado y modular, reaprovechando textos y gráficos del resto del PDM. Lo consultan [Postventa](./postventa.md), [Marketing](./marketing.md) y los propios clientes.

#### Glosario y Memoria de traducción
- Términos técnicos y su traducción aprobada en cada idioma. Frases ya traducidas.

Ahorra traducciones y mantiene la coherencia con las descripciones en varios idiomas de los [Datos maestros](./datos_maestros.md#artículos).

#### Expediente técnico y Declaración de conformidad
- Normas y directivas aplicables. Ensayos. Análisis de riesgos. Declaración firmada.

Necesarios para poner el producto en el mercado (por ejemplo, con el marcado CE). Ver también [Cumplimiento jurídico](./juridico.md#requisito-legal).
