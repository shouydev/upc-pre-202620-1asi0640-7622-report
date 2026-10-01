# 1.2 Análisis de los requisitos de la red

El dimensionamiento de la infraestructura de comunicaciones de MIEMPRESA parte de un análisis cuantitativo y funcional de las demandas operativas en cada una de sus sedes. Con el propósito de garantizar una solución sostenible a largo plazo, los requerimientos contemplan un factor de crecimiento proyectado del 25% a diez años, asegurando la escalabilidad del direccionamiento IP y la capacidad de conmutación del hardware seleccionado.

![direccionamiento-multinacional](report/assets/network-requirements-analysis/direccionamiento-multinacional.png)

![direccionamiento-isp](report/assets/network-requirements-analysis/direccionamiento-isp.png)

## 1.2.1 Requisitos de la red de la Sede Principal (Lima)

La sede principal ubicada en Lima constituye el núcleo operativo, tecnológico y administrativo de la corporación. Esta dependencia alberga el centro de datos principal con los servidores corporativos centrales y concentra la mayor densidad de usuarios de la organización, distribuidos en seis áreas funcionales cableadas, dos segmentos inalámbricos y la red de gestión de equipamiento.
La cuantificación actual registra 301 dispositivos finales en operación. Al aplicar la tasa de crecimiento del 25% sobre cada área operativa, la infraestructura proyectada debe brindar soporte a un total de 380 estaciones de trabajo y servidores, además de reservar direccionamiento para los dispositivos intermediarios de red. En la Tabla 3 se presenta el desglose detallado de hosts requeridos y proyectados por segmento.

![lima-requirements](report/assets/network-requirements-analysis/lima-requirements.png)

A este dimensionamiento de hosts se añade la demanda de direccionamiento para la administración de la infraestructura de red. La gestión del equipamiento intermediario se segrega en una red virtual dedicada, la VLAN 99, que interconecta las interfaces del router, el switch de núcleo, los tres switches de distribución y los cinco switches de acceso, junto con la estación de administración autorizada PC-Admin para la sede principal y sucursales. Este segmento totaliza 11 hosts y 14 proyectados con el factor de crecimiento del 25%, requiriendo una subred con máscara de longitud de prefijo /28.
Asimismo, como medida de endurecimiento en la capa de enlace de datos, la arquitectura reserva la VLAN 999 como identificador nativo para el transporte de tramas en los enlaces troncales IEEE 802.1Q. Esta red no posee asignación de interfaces virtuales ni direccionamiento IP, permaneciendo desprovista de puertos de acceso para anular de forma definitiva vectores de ataque de salto de VLAN y doble etiquetado.
Para cada una de las sedes sucursales se estimó lo hosts por unidad operativa en base al porcentaje de hosts reflejado en la sede principal para realizar su proyección.

## 1.2.2 Requisitos de la red de la Sede Sucursal 1 (La Libertad)

La sede sucursal de La Libertad forma parte de la infraestructura descentralizada de MIEMPRESA en el norte del país. El dimensionamiento actual contempla 160 usuarios internos cableados. Al incorporar la tasa de crecimiento proyectada del 25% a diez años, la red debe soportar una capacidad definitiva de 200 estaciones de trabajo. Asimismo, se incluye la cobertura inalámbrica para ejecutivos y clientes.

## 1.2.3 Requisitos de la red de la Sede Sucursal 2 (Ica)

La sede sucursal de Ica constituye la red provincial con mayor concentración de personal dentro de la corporación. La demanda presente comprende 190 hosts. Al aplicar el factor de crecimiento del 25% a diez años, la infraestructura local se dimensiona para albergar a 238 hosts. Adicionalmente, se planifica el servicio de conectividad inalámbrica para personal ejecutivo y clientes.

## 1.2.4 Requisitos de la red de la Sede Sucursal 3 (Huánuco)

La sede sucursal de Huánuco brinda cobertura a las operaciones de la corporación en la región centro-oriental. El personal operativo en esta sede está conformado actualmente por 96 hosts. Con la proyección de crecimiento del 25% a diez años, la red se diseña para soportar a 120 hosts. Se contempla igualmente el acceso inalámbrico segregado para ejecutivos y clientes.

## 1.2.5 Requisitos de la red de la Sede Sucursal 4 (Puno)

La sede sucursal de Puno centraliza las operaciones en el sur del país. La sede registra actualmente 105 hosts, cifra que se incrementa a 132 tras aplicar el 25% de crecimiento a diez años. La solución local integra también conectividad inalámbrica con control de acceso independiente para usuarios ejecutivos y clientes.

## 1.2.6 Requisitos Adicionales de la red

Más allá del dimensionamiento cuantitativo de hosts y computadoras por sede, el caso de estudio de MIEMPRESA establece un conjunto de requisitos técnicos, funcionales y de seguridad indispensables que la arquitectura de red debe cumplir obligatoriamente para satisfacer las demandas del negocio:

### Requisitos de Tecnologías LAN y Redes Inalámbricas
- **Segmentación por VLANs y enrutamiento inter-VLAN:** Cada sede debe segmentar el tráfico de sus departamentos en redes virtuales independientes, garantizando la comunicación entre distintas VLANs de la misma sede mediante conmutación multicapa y alta disponibilidad de puerta de enlace.
- **Doble red WiFi por sede:** Cada sede debe contar con dos redes inalámbricas independientes: una red para Ejecutivos (con acceso a los recursos corporativos) y una red para Clientes e Invitados (con salida directa a Internet), ambas entregando direccionamiento automático por DHCP.
- **Contención de enlaces troncales:** Confinamiento del tráfico de control mediante una VLAN nativa dedicada (VLAN 999) en todos los enlaces troncales 802.1Q, sin direccionamiento IP ni puertos de acceso, para mitigar vulnerabilidades de capa de enlace.

### Requisitos de Conectividad WAN y Enrutamiento
- **Enlaces WAN dedicados y estandarizados:** La comunicación entre la sede central en Lima y las cuatro sucursales remotas debe realizarse a través de enlaces seriales punto a punto mediante el protocolo PPP con autenticación segura (PAP y CHAP).
- **Enrutamiento dinámico interno con RIPv2:** La red corporativa de Perú debe operar bajo el protocolo dinámico RIPv2 para mantener sincronizadas las tablas de rutas entre todas las sedes de forma automática.
- **Contingencia de salida a Internet con doble ISP:** La sede Lima debe contar con dos enlaces hacia Internet, manteniendo activo el enlace primario (ISP1) y conmutando automáticamente al enlace secundario (ISP2) ante caídas de servicio.

### Requisitos de Servicios de Red y Seguridad
- **Políticas de acceso al servidor de archivos FTP:** Cada sede debe contar con un servidor FTP propio al que solo pueden acceder los usuarios de dicha sede y el servidor central de Lima. Queda restringido el acceso directo entre servidores FTP de diferentes sucursales (por ejemplo, Ica no puede acceder al FTP de La Libertad).
- **Servidores Web locales y centralizados:** Cada sede debe disponer de un servidor Web local visible y accesible por cualquier usuario de la organización.
- **Servicio DHCP distribuido por sede:** Cada sede debe implementar su propio servidor DHCP local para aprovisionar automáticamente de parámetros IP a los equipos cableados e inalámbricos.
- **Servidor de correo centralizado:** La sede principal en Lima debe alojar el servidor corporativo de correos electrónicos para toda la empresa.
- **Administración remota segura desde PC-Admin:** Todos los routers y switches deben ser gestionados de forma remota y cifrada exclusivamente mediante sesiones SSH originadas desde una computadora de administración autorizada (PC-Admin), ubicada dentro de la red virtual de gestión (VLAN 99) en cada sede.

### Requisitos de Servicios Cloud y Continuidad del Negocio
- **Solución de respaldo corporativo en la nube:** Dimensionar y costear una solución de almacenamiento remoto comparando proveedores reales del mercado (AWS, Azure y Google Cloud), garantizando la retención y recuperación de copias de seguridad de los datos críticos.
- **Evaluación de migración a infraestructura Cloud:** Analizar la viabilidad técnica y económica de reemplazar la infraestructura física local por servicios equivalentes en la nube (VPC, routers virtuales y firewalls).