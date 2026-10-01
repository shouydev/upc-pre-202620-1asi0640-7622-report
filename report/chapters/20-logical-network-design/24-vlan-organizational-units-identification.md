## 2.4 Identificación de las unidades organizacionales (VLAN)

La arquitectura lógica de conmutación de MIEMPRESA implementa una segmentación integral basada en el estándar IEEE 802.1Q. Esta estrategia divide la infraestructura conmutada en múltiples redes de área local virtuales (VLAN), delimitando dominios de difusión independientes por área funcional para minimizar la propagación de tráfico no deseado y optimizar el rendimiento del medio de transmisión.

Para garantizar la coherencia operativa y simplificar el mantenimiento, se establece una topología de asignación de VLAN homogénea que se replica en la sede principal Lima y en las cuatro sedes sucursales (La Libertad, Ica, Huánuco y Puno). Cada departamento funcional cuenta con un identificador numérico unificado y políticas de seguridad alineadas con sus responsabilidades corporativas.

### 2.4.1 Segregación del plano de gestión (VLAN 99)

El aislamiento del plano de administración respecto del plano de datos de los usuarios constituye un principio de diseño fundamental en redes empresariales. El estándar corporativo prohíbe taxativamente el uso de la VLAN 1 predeterminada para fines de administración. En su lugar, se implementa la VLAN 99, denominada formalmente GESTION, como un segmento protegido y exclusivo para la supervisión y mantenimiento del equipamiento activo.

En esta red se configuran las interfaces virtuales de conmutador de los switches multicapa de distribución y switches de acceso, así como la interfaz o subinterfaz de gestión del enrutador central y enrutadores de sucursal. El acceso administrativo a estos nodos queda confinado estrictamente al protocolo SSH versión 2 con cifrado asimétrico robusto en el puerto TCP 22, bloqueando de manera permanente protocolos en texto plano como Telnet o HTTP.

Asimismo, la superficie de ataque se restringe mediante listas de control de acceso aplicadas en la capa de distribución, permitiendo el inicio de sesiones SSH exclusivamente desde la dirección IP estática de la estación PC-Admin. En la sede Lima, este segmento soporta inicialmente 11 nodos (1 enrutador Cisco 2811, 1 switch de núcleo Catalyst 3560, 3 switches multicapa Catalyst 3560, 5 switches de acceso Catalyst 2960-24TT y la estación PC-Admin), dimensionándose para albergar a 14 nodos tras aplicar la tasa de crecimiento proyectada del 25%, lo que demanda una subred de prefijo /28.

### 2.4.2 Endurecimiento de enlaces troncales y VLAN Nativa (VLAN 999)

Los enlaces troncales IEEE 802.1Q transportan el tráfico etiquetado de múltiples redes virtuales entre dispositivos de conmutación. Por especificación de protocolo, las tramas que carecen de etiqueta de encapsulación son asignadas a la VLAN nativa. La configuración predeterminada de los conmutadores comerciales designa la VLAN 1 como nativa, lo cual representa una vulnerabilidad crítica ante vectores de ataque de capa 2.

Entre las principales amenazas mitigadas destaca el ataque de salto de VLAN por doble etiquetado. En este escenario, un host malicioso inyecta tramas con dos encabezados 802.1Q: el switch de conmutación elimina la etiqueta externa por coincidir con la red nativa y reenvía la trama al enlace troncal, donde el conmutador de destino lee la segunda etiqueta y entrega el paquete a un segmento sensible sin someterlo a inspección de capa de red ni filtros de enrutamiento.

Para neutralizar esta vulnerabilidad de forma definitiva, se establece la VLAN 999, denominada formalmente NATIVA, como una red de contención exclusiva para todos los puertos troncales de la corporación. Esta red opera bajo directrices de estricto aislamiento: no posee interfaces virtuales de conmutador ni direcciones IP asignadas, carece de puertos de acceso asignados a usuarios o servidores, y no interviene en los esquemas de enrutamiento inter-VLAN. Cualquier trama no etiquetada que transite por los troncales queda confinada y descartada en este segmento de cuarentena.

### 2.4.3 Matriz consolidada de identificación de VLANs

En la @tbl:vlan-organizational-units se presenta la matriz integral de segmentación lógica de MIEMPRESA. El esquema define diez redes virtuales con su identificador numérico, nombre estandarizado, alcance territorial, tipología de tráfico, estado de interfaz virtual y la descripción de su propósito funcional junto con las políticas de seguridad asociadas.

| ID VLAN | Nombre de VLAN | Alcance | Tipo de Tráfico | Estado SVI | Propósito Funcional y Políticas de Seguridad |
| :---: | :---: | :---: | :---: | :---: | :--- |
| 10 | VENTAS | Todas las sedes | Datos cableados | Enrutable | Segmento operativo para estaciones de ventas y facturación comercial con acceso a servidores y salida a Internet. |
| 20 | ADMINISTRACION | Todas las sedes | Datos cableados | Enrutable | Tráfico corporativo de gerencia y operaciones administrativas con permisos restringidos hacia segmentos financieros. |
| 30 | MARKETING | Todas las sedes | Datos cableados | Enrutable | Estaciones de diseño comercial y publicidad con conectividad hacia servidores internos y navegación externa. |
| 40 | LOGISTICA | Todas las sedes | Datos cableados | Enrutable | Gestión de inventarios y despacho de mercadería con acceso directo al sistema de almacenamiento y servidores. |
| 50 | FINANZAS | Todas las sedes | Datos cableados | Enrutable | Operaciones contables y tesorería aisladas mediante listas de control de acceso para proteger información confidencial. |
| 60 | SERVIDORES | Todas las sedes | Servidores y servicios | Enrutable | Granja de servidores locales y centralizados para servicios de red con políticas de acceso y monitoreo reforzadas. |
| 70 | WIFI_EJECUTIVOS | Todas las sedes | Inalámbrico corporativo | Enrutable | Conectividad inalámbrica cifrada bajo WPA2 para personal ejecutivo con acceso autenticado a la red corporativa. |
| 80 | WIFI_CLIENTES | Todas las sedes | Inalámbrico invitados | Enrutable | Acceso inalámbrico exclusivo para visitas y clientes con salida directa a Internet y aislamiento total de la red interna. |
| 99 | GESTION | Todas las sedes | Gestión equipamiento | Enrutable | Segmento administrativo para acceso SSH versión 2 a conmutadores y enrutadores permitido únicamente desde PC-Admin. |
| 999 | NATIVA | Todas las sedes | Tráfico troncal 802.1Q | No enrutable | Red dummy de contención en enlaces troncales sin direccionamiento IP ni puertos de acceso para anular saltos de VLAN. |
: Matriz consolidada de asignación de VLANs corporativas {#tbl:vlan-organizational-units}

*Nota.* Esquema uniforme de segmentación lógica aplicado en la sede principal y sedes sucursales de la corporación.
