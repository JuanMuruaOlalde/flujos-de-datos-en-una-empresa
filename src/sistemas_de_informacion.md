# Sistemas de información, IT

## Algunas entidades habituales

### Sistemas e infraestructura

#### Aplicación o Sistema
- Responsable funcional (el departamento usuario). Proveedor. Versión. Contrato de soporte.

Ver [lista de las aplicaciones y sistemas habituales](#apéndice-algunos-softwares-habituales)

#### Integración
- Qué datos pasan de qué sistema a cuál. Cuándo (en tiempo real, cada noche...). Cómo (EDI, servicios web, ficheros). Responsable.

Es la versión técnica del mapa de flujos que se describe en este libro. Si no está documentada, nadie sabe qué se rompe al cambiar un sistema.

#### Equipo informático
- Ordenadores, móviles, terminales, servidores, impresoras,... Persona o puesto al que está asignado. Fecha de compra. Garantía.

Son equipos que se renevan con frecuencia (cada cuatro o cinco años). Es conveniente llevar un buen inventario.

#### Licencia de software
- Programa. Número de licencias. A quién están asignadas. Vencimiento. Coste.

Ver también [Cumplimiento jurídico](./juridico.md#licencia).

### Usuarios y seguridad

#### Usuario y Permisos
- Persona. Sistemas a los que accede. Perfil o rol en cada uno. Fechas de alta y de baja.

Las altas, bajas y cambios de puesto los comunica [Departamento de personal](./departamento_personal.md#empleado). Si no llegan a tiempo, quedan accesos abiertos de personas que ya no están.

#### Copia de seguridad
- Qué se copia. Frecuencia. Dónde se guarda. Última prueba de recuperación.

#### Incidente de seguridad
- Qué ha pasado. Sistemas y datos afectados. Medidas tomadas.

Si afecta a datos personales, es una [Brecha de seguridad](./juridico.md#brecha-de-seguridad) que puede ser necesario comunicar a otras instancias.

### Soporte

#### Incidencia o Petición de usuario
- Usuario. Sistema. Descripción. Prioridad. Técnico asignado. Tiempos de respuesta y de resolución.

#### Proyecto o Petición de desarrollo
- Quién lo pide. Qué se necesita. Prioridad. Estimación. Estado.

### Datos

#### Catálogo de productos de datos
- Qué significa cada dato. En qué sistema está. Qué departamento es responsable de mantenerlo.

IT no suele ser el dueño de los datos, sino de los sistemas que los contienen.

Entre otros muchos, los [Datos maestros](./datos_maestros.md) y sus responsables deberían aparecer aquí.

#### Almacén de datos
- Datos extraídos de todos los sistemas. Filtrados, adecuados y almacenados. Histórico.

IT se encarga de capturar, filtrar, adecuar y almacenar los datos en bruto y preelaborados. Para que los usuarios puedan consultarlos y analizarlos por sí mismos. Lo utilizan sobre todo [Dirección](./direccion.md#cuadro-de-mando) y [Marketing](./marketing.md#estudio-de-comportamiento).

#### Calidad de los datos
- Duplicados. Datos incompletos. Datos que no coinciden entre sistemas. Responsable de corregirlos.

Lo ideal es que quien descubre un error lo corrija, o avise a quien mantiene ese dato.



## apéndice: algunos softwares habituales

| Sistema | Dominio | Muestra de algunos datos que maneja |
|---|---|---|
| ERP | Económico-administrativo | Pedidos, órdenes, movimientos de stock, costes, facturación |
| CRM | Comercial | Oportunidades, ofertas, motivos de pérdida |
| MES / MOM | Ejecución de producción | Declaraciones de producción, paradas, scrap, tiempos |
| PLM / PDM | Ingeniería | BOM, rutas, revisiones, ECO |
| WMS | Almacén | Ubicaciones, movimientos, inventarios |
| GMAO / CMMS | Mantenimiento | Órdenes, averías, preventivos, repuestos |
| SCADA / Historian | Procesos productivos | Señales de sensor, estados de máquina |
| LIMS | Calidad | Ensayos, resultados, certificados |
| EDI / portales cliente | Cadena de suministro | Previsiones, llamadas, ASN |

Acrónimos:
- ERP (Enterprise Resource Planning)
- CRM (Customer Relationship Management)
- MES (Manufacturing Execution System)
- MOM (Manufacturing Operations Management)
- PLM (Product Lifecycle Management)
- PDM (Product Data Management)
- CMS (Content Management System)
- WMS (Warehouse Management System)
- WES (Warehouse Execution System)
- WCS (Warehouse Control System)
- GMAO (Gestión de Mantenimiento Asistido por Ordenador)
- CMMS (Computerized Maintenance Management System)
- SCADA (Supervisory Control and Data Acquisition)
- LIMS (Laboratory Information Management System)
- EDI (Electronic Data Interchange)

