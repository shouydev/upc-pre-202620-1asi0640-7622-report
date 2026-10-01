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

Más allá del dimensionamiento de hosts por departamento, la solución técnica debe satisfacer un conjunto de requisitos funcionales y de arquitectura indispensables:
- Arquitectura de red jerárquica y escalable: Adopción del modelo de tres capas para organizar el tráfico, facilitar el diagnóstico de incidencias y permitir la incorporación de nuevos módulos sin alterar la topología existente.
- Segmentación lógica estricta mediante VLANs: Creación de redes virtuales independientes por unidad organizativa bajo el estándar IEEE 802.1Q para aislar dominios de difusión y optimizar el rendimiento de la conmutación.
- Mitigación de vulnerabilidades de capa de enlace mediante VLAN nativa dedicada: Configuración de la VLAN 999 como red nativa en todos los enlaces troncales 802.1Q, manteniéndola desprovista de direccionamiento IP, interfaces virtuales de conmutador y puertos de acceso, neutralizando ataques de salto de VLAN y doble etiquetado.
- Topología WAN Hub-and-Spoke con enrutamiento dinámico: Concentración del tráfico intersedes en Lima como nodo central mediante enlaces seriales punto a punto dedicados, empleando el protocolo dinámico RIPv2 para la convergencia interna y una ruta predeterminada estática hacia los proveedores de Internet.
- Segregación inalámbrica segura bajo estándar WPA2: Habilitación de dos identificadores de conjunto de servicios por sede, uno para personal ejecutivo con acceso a recursos locales y otro exclusivo para clientes con salida directa a Internet sin visibilidad de la red empresarial.
- Servicios de red distribuidos y centralizados: Despliegue de servidores FTP, HTTPS y DHCP locales en cada sede, manteniendo el servidor de correos y DNS centralizado en la sede Lima.
- Gestión administrativa segura mediante segmento exclusivo y SSH versión 2: Confinamiento del plano de gestión hacia conmutadores y enrutadores dentro de la VLAN 99, restringiendo el acceso administrativo exclusivamente a sesiones cifradas bajo SSH versión 2 originadas desde la estación autorizada PC-Admin.
- Continuidad operativa y copias de seguridad en la nube: Implementación de un mecanismo automatizado de respaldo offsite hacia un proveedor de nube pública, garantizando la recuperación de configuraciones y datos críticos ante desastres físicos.