# Glosario

El presente glosario recopila y define la terminología técnica, estándares internacionales, protocolos de comunicación y conceptos arquitectónicos empleados a lo largo del diseño, dimensionamiento e implementación de la infraestructura de red para la organización. Las definiciones se estructuran en orden alfabético para facilitar la consulta y unificar el marco conceptual de la solución técnica tanto en el ámbito de redes locales y conmutadas como en los enlaces de área amplia, servicios corporativos y contingencia en la nube.

- **Access Control List (ACL):** Mecanismo de seguridad perimetral implementado en enrutadores y conmutadores multicapa que evalúa y filtra el tráfico de red mediante reglas secuenciales. Permite autorizar o denegar el paso de paquetes en función de criterios como la dirección IP de origen, la dirección de destino, el protocolo de capa de transporte y los puertos de comunicación, finalizando con una regla de denegación implícita.

- **Access Point (AP):** Dispositivo de red que interconecta terminales inalámbricos con la infraestructura cableada de área local mediante señales de radiofrecuencia bajo los estándares IEEE 802.11. Opera en la capa de enlace de datos y actúa como puente entre los medios inalámbricos y las interfaces cableadas, facilitando la difusión de múltiples redes inalámbricas con aislamiento por identificador de servicio.

- **Advanced Encryption Standard (AES):** Algoritmo de cifrado simétrico por bloques adoptado a escala global para proteger la confidencialidad de los datos mediante claves de 128, 192 o 256 bits. En arquitecturas de telecomunicaciones, se utiliza como estándar de cifrado robusto en enlaces inalámbricos con WPA2 y en mecanismos de almacenamiento en reposo dentro de plataformas en la nube.

- **Alta Disponibilidad (High Availability):** Propiedad de diseño arquitectónico que garantiza la continuidad operativa y la accesibilidad ininterrumpida de los servicios de telecomunicaciones frente a fallas de hardware, software o enlaces. Se implementa mediante redundancia física de enlaces, duplicación de fuentes de energía y protocolos de conmutación por error en capas de distribución y núcleo.

- **Amazon Simple Storage Service (Amazon S3):** Servicio de almacenamiento de objetos escalable de alta disponibilidad ofrecido por Amazon Web Services. Proporciona durabilidad para salvaguardar copias de seguridad corporativas, estructurando la información en contenedores lógicos y ofreciendo múltiples categorías de almacenamiento adaptadas a la frecuencia de consulta y retención de datos.

- **Atenuación de señal:** Pérdida progresiva de potencia que sufre una señal electromagnética al propagarse a través de un medio de transmisión físico. En cables de cobre de par trenzado, impone una restricción de distancia máxima de 100 metros entre dispositivos de red para evitar la degradación de tramas y la pérdida de enlace a nivel de capa física.

- **Azure Blob Storage:** Solución de almacenamiento de objetos masivos en la nube desarrollada por Microsoft Azure, diseñada para albergar grandes volúmenes de datos no estructurados. Facilita la retención de respaldos corporativos externos con soporte para niveles caliente, frío y de archivo, integrando cifrado y replicación geográfica.

- **Broadcast Domain (Dominio de Difusión):** Segmento lógico o físico de una red informática en el que cualquier trama de difusión emitida por un host es recibida por todos los demás dispositivos pertenecientes a dicho entorno. Los enrutadores y las interfaces virtuales de conmutación multicapa delimitan estos dominios, evitando la saturación del ancho de banda y aislando el tráfico de difusión.

- **Cable de Par Trenzado (UTP):** Medio de transmisión físico compuesto por conductores de cobre entrelazados en pares helicoidales para reducir la diafonía y la interferencia electromagnética externa. Utilizado en categorías 6 y 6A con conectores RJ-45, constituye el estándar de cableado estructurado horizontal para enlaces Ethernet de alta velocidad en redes de área local.

- **Capa de Acceso:** Nivel inferior del modelo jerárquico de tres capas de Cisco, encargado de conectar de forma directa los dispositivos finales como computadoras de escritorio, servidores e impresoras a la red cableada. Su función principal consiste en controlar el acceso a la red, aplicar políticas de seguridad en puertos y segmentar los dispositivos en sus respectivas redes virtuales.

- **Capa de Distribución:** Nivel intermedio del modelo de red jerárquico que interconecta los conmutadores de acceso con el núcleo central. En este estrato se procesa el enrutamiento inter-VLAN mediante conmutadores multicapa, se ejecutan protocolos de redundancia de primer salto, se aplican listas de control de acceso y se delimitan los dominios de difusión departamentales.

- **Capa de Núcleo (Core):** Estrato superior del modelo jerárquico de conmutación, diseñado para transportar ingentes volúmenes de tráfico entre diferentes módulos de distribución y el enrutador de borde con mínima latencia. Se caracteriza por su alta velocidad de conmutación, la eliminación de filtrados complejos de paquetes y la presencia de enlaces redundantes de fibra o cobre.

- **Capital Expenditure (CapEx):** Inversión inicial de capital financiero destinada a la adquisición de activos fijos tangibles para la infraestructura corporativa de comunicaciones. Comprende el costo de compra de enrutadores, conmutadores multicapa, servidores físicos, cableado estructurado y gabinetes de telecomunicaciones amortizables a largo plazo.

- **Challenge Handshake Authentication Protocol (CHAP):** Protocolo de autenticación punto a punto seguro utilizado en enlaces seriales de área amplia. Verifica la identidad del extremo remoto mediante un intercambio de tres vías basado en un desafío generado aleatoriamente y una respuesta resumida con algoritmo hash MD5, impidiendo la exposición de contraseñas en texto claro a través del canal de comunicación.

- **Classless Inter-Domain Routing (CIDR):** Metodología de asignación de direcciones IP y enrutamiento que flexibiliza la división tradicional por clases mediante la notación de longitud de prefijo. Permite agregar múltiples rutas en bloques compactos, optimizar el tamaño de las tablas de enrutamiento y hacer un uso eficiente del espacio de direccionamiento disponible en redes corporativas e Internet.

- **Conmutación Multicapa (Multilayer Switching):** Tecnología de interconexión implementada en conmutadores que integran funciones de conmutación de tramas de capa 2 y enrutamiento de paquetes de capa 3 a velocidad de hardware. Permite el reenvío directo de paquetes entre diferentes redes virtuales mediante circuitos integrados de aplicación específica, maximizando el rendimiento del enrutamiento inter-VLAN.

- **Conmutador (Switch):** Dispositivo intermediario de capa de enlace de datos fundamental en la arquitectura de red local que reenvía tramas Ethernet de forma selectiva entre sus puertos físicos basándose en la inspección de direcciones MAC almacenadas en su tabla de conmutación. Previene colisiones, proporciona ancho de banda dedicado por puerto y segmenta dominios de colisión dentro de la infraestructura institucional.

- **Copia de Seguridad Completa (Full Backup):** Mecanismo de respaldo que realiza una copia exacta e íntegra de la totalidad de los datos y configuraciones seleccionadas del sistema corporativo en un momento determinado. Constituye la línea base fundamental para los procesos de restauración, aunque exige mayor tiempo de ejecución y capacidad de almacenamiento en los repositorios de destino.

- **Copia de Seguridad Diferencial (Differential Backup):** Estrategia de respaldo acumulativa que almacena únicamente los archivos modificados o creados desde la última copia de seguridad completa. Optimiza los tiempos de restauración al requerir únicamente la última copia completa y el último respaldo diferencial, manteniendo un equilibrio técnico entre velocidad de recuperación y espacio ocupado.

- **Copia de Seguridad Incremental (Incremental Backup):** Técnica de respaldo que registra exclusivamente la información que ha sufrido modificaciones desde la ejecución de la copia de seguridad más reciente, ya sea completa o incremental. Reduce significativamente la ventana de tiempo de respaldo y el volumen de transferencia sobre los enlaces de datos, requiriendo una cadena ordenada para su restauración.

- **Default Gateway (Puerta de Enlace Predeterminada):** Dirección IP configurada en los dispositivos finales que identifica la interfaz de red del enrutador o switch multicapa responsable de canalizar el tráfico hacia subredes externas o hacia Internet. En topologías de alta disponibilidad, corresponde a la dirección virtual compartida gestionada por protocolos de redundancia de primer salto.

- **Doble ISP (Dual ISP Failover):** Estrategia de diseño de conectividad que proporciona redundancia de acceso a la red pública Internet mediante la contratación de dos proveedores de servicios independientes. El enrutador de borde canaliza el tráfico habitualmente a través del enlace primario y conmuta de forma automática hacia el enlace secundario ante la pérdida del servicio principal mediante el empleo de rutas estáticas flotantes.

- **Domain Name System (DNS):** Sistema de base de datos distribuida y jerárquica encargado de resolver nombres de dominio textuales comprensibles para los usuarios en direcciones IP numéricas requeridas por la capa de red. En el ámbito corporativo, permite la localización transparente de servidores web, de correo y de archivos tanto a nivel local como en la red global.

- **Dynamic Host Configuration Protocol (DHCP):** Protocolo cliente-servidor de capa de aplicación que automatiza la configuración de red de los terminales en un entorno de comunicación. Asigna dinámicamente direcciones IP, máscaras de subred, puertas de enlace predeterminadas y servidores de resolución de nombres a partir de grupos de direcciones definidos para cada segmento lógico de la organización.

- **Enlace Serial:** Medio de transmisión físico de datos síncrono que transfiere información de forma secuencial bit a bit a través de una línea o canal de comunicaciones punto a punto. Es ampliamente utilizado en conexiones de área amplia para interconectar enrutadores remotos a través de líneas dedicadas mediante protocolos de línea como PPP.

- **Enlace Troncal (Trunk Link):** Conexión física punto a punto establecida entre conmutadores o entre un conmutador y un enrutador que permite transportar el tráfico de múltiples redes virtuales sobre un único medio físico. Utiliza mecanismos de multiplexación y encapsulamiento normalizados para conservar el aislamiento del tráfico departamental a través del campus.

- **Enrutamiento Dinámico:** Mecanismo mediante el cual los enrutadores intercambian información topológica de forma autónoma utilizando protocolos de enrutamiento para construir y actualizar sus tablas de reenvío. Facilita la adaptación automática ante caídas de enlaces o incorporación de nuevas subredes, determinando la ruta óptima de acuerdo con las métricas del protocolo activo.

- **Enrutamiento Estático:** Método de configuración de rutas donde el administrador de red ingresa manualmente los destinos y sus respectivos saltos o interfaces de salida en las tablas de enrutamiento. Proporciona un control determinista del tráfico, reduce la sobrecarga de procesamiento en la CPU y prescinde del consumo de ancho de banda propio de los mensajes periódicos de protocolo.

- **Enrutamiento Inter-VLAN:** Proceso de reenvío de paquetes entre redes virtuales independientes que operan en diferentes subredes lógicas. Se implementa en la capa de red mediante interfaces virtuales en conmutadores multicapa o a través de subinterfaces enrutadas, permitiendo la comunicación controlada entre departamentos conforme a las políticas de seguridad corporativas.

- **File Transfer Protocol (FTP):** Protocolo de capa de aplicación basado en el modelo cliente-servidor para la transferencia de archivos en redes TCP/IP. Utiliza conexiones separadas para control y transmisión de datos, facilitando el intercambio de documentos corporativos y respaldos de configuración bajo mecanismos de autenticación y privilegios de acceso.

- **Firewall (Cortafuegos):** Sistema de seguridad perimetral de red implementado en hardware o software que inspecciona, filtra y controla el flujo de paquetes entrantes y salientes en función de un conjunto predeterminado de reglas de seguridad. Protege la infraestructura interna aislando segmentos de servidores y bloqueando intentos de acceso no autorizados desde redes externas.

- **Fixed Length Subnet Mask (FLSM):** Metodología de subdivisión de redes donde todas las subredes derivadas de un bloque principal poseen una máscara con el mismo número de bits de prefijo, alojando idéntica cantidad de direcciones posibles. Es empleada para estructurar enlaces de área amplia o filiales homogéneas con requerimientos cuantitativos uniformes.

- **Google Cloud Storage:** Plataforma de almacenamiento de objetos gestionada por Google Cloud Platform, diseñada para ofrecer almacenamiento seguro, duradero y de alta disponibilidad para copias de seguridad institucionales. Permite configurar ciclos de vida automatizados para transferir datos hacia niveles de costo reducido a medida que transcurre el tiempo de retención.

- **Hot Standby Router Protocol (HSRP):** Protocolo de redundancia de primer salto propietario de Cisco que agrupa dos o más enrutadores o conmutadores multicapa bajo una dirección IP y MAC virtual. El equipo con mayor prioridad asume el rol activo procesando el tráfico de la subred, mientras el equipo en espera permanece listo para asumir la carga de forma transparente ante fallas.

- **Hypertext Transfer Protocol Secure (HTTPS):** Versión cifrada del protocolo de transferencia de hipertexto utilizada para la navegación web segura. Combina la transmisión de páginas en capa de aplicación con protocolos de seguridad en capa de transporte como TLS, garantizando la autenticidad del servidor, la integridad del contenido y la confidencialidad de la información transmitida frente a interceptaciones.

- **IEEE 802.1Q:** Estándar internacional de la industria para el etiquetado de tramas Ethernet en enlaces troncales de conmutación. Inserta una cabecera de cuatro bytes en la trama original para incorporar un identificador numérico de red virtual de doce bits, lo que permite diferenciar y encaminar el tráfico de hasta 4094 VLANs sobre un único medio compartido.

- **Infrastructure as a Service (IaaS):** Modelo de aprovisionamiento de computación en la nube que proporciona recursos informáticos fundamentales como procesamiento, almacenamiento y conectividad de red bajo demanda mediante virtualización. Permite prescindir de hardware físico para respaldos y servidores corporativos, delegando el mantenimiento del centro de datos en el proveedor externo.

- **Internet Message Access Protocol (IMAP):** Protocolo de capa de aplicación estándar para la gestión y lectura de correo electrónico que opera en el puerto TCP 143 o puerto seguro TCP 993. A diferencia de esquemas de descarga local, mantiene los mensajes y carpetas sincronizados directamente en el servidor de correo, permitiendo el acceso coordinado desde múltiples terminales.

- **Internet Service Provider (ISP):** Entidad u organización de telecomunicaciones que comercializa conectividad a Internet y servicios asociados a empresas y usuarios finales. En infraestructuras corporativas críticas, se contratan múltiples proveedores independientes para establecer esquemas de contingencia activa y respaldo ante interrupciones de servicio.

- **IP Helper-Address (DHCP Relay):** Función de retransmisión de paquetes configurada en las interfaces de enrutamiento o SVIs que intercepta solicitudes de difusión de terminales cliente y las reenvía como paquetes unicast hacia servidores centralizados de configuración o nombres ubicados en subredes distintas. Supera la barrera impuesta por los enrutadores al tráfico broadcast.

- **IPv4 (Internet Protocol Version 4):** Protocolo de capa de red fundamental de la arquitectura TCP/IP que implementa un esquema de direccionamiento lógico sin conexión mediante identificadores de 32 bits representados en cuatro octetos decimales. Proporciona los mecanismos de fragmentación, direccionamiento jerárquico y entrega de paquetes entre redes heterogéneas.

- **Local Area Network (LAN):** Infraestructura de comunicaciones de datos que interconecta terminales, estaciones de trabajo y dispositivos de red dentro de una extensión geográfica limitada, como un edificio o campus corporativo. Se caracteriza por sus elevadas tasas de transferencia de datos, mínima latencia y administración centralizada por la propia organización.

- **Mean Time Between Failures (MTBF):** Métrica cuantitativa de confiabilidad técnica que expresa el intervalo de tiempo promedio transcurrido entre averías consecutivas de un equipo o componente de red durante su ciclo de operación normal. Un valor elevado de MTBF indica mayor robustez y estabilidad en dispositivos críticos de núcleo y distribución.

- **Mean Time To Repair (MTTR):** Indicador temporal de mantenibilidad que mide el tiempo promedio requerido para diagnosticar, resolver y restituir el funcionamiento pleno de un equipo o enlace de comunicaciones tras producirse un incidente técnico. Su reducción es clave para cumplir con los objetivos corporativos de disponibilidad continua.

- **Operational Expenditure (OpEx):** Gastos operativos continuos derivados del mantenimiento, soporte y funcionamiento cotidiano de la infraestructura de telecomunicaciones. Engloba el consumo de energía eléctrica, costos de suscripción por almacenamiento en la nube, contratos de soporte técnico, enlaces de conectividad con proveedores de Internet y licencias de software.

- **Password Authentication Protocol (PAP):** Mecanismo de autenticación básico para enlaces seriales punto a punto que valida la identidad del extremo emisor enviando el nombre de usuario y la contraseña en texto plano no cifrado mediante un intercambio de dos vías. Debido a su vulnerabilidad frente a capturas de tráfico, su uso se restringe a entornos heredados controlados.

- **Point-to-Point Protocol (PPP):** Protocolo de capa de enlace de datos ampliamente adoptado en telecomunicaciones para establecer conexiones directas y síncronas entre dos nodos de red en enlaces de área amplia. Soporta la encapsulación de múltiples protocolos de capa de red, negociación de parámetros de conexión y mecanismos de autenticación segura.

- **Port Security:** Mecanismo de seguridad de capa de enlace configurado en las interfaces de conmutadores de acceso que restringe el ingreso de tráfico evaluando las direcciones MAC de los terminales conectados. Permite definir límites cuantitativos de dispositivos por puerto y programar acciones reactivas de bloqueo ante accesos no autorizados.

- **PortFast:** Característica de optimización para conmutadores Ethernet que acelera la transición de un puerto de acceso directamente al estado de reenvío, omitiendo las fases intermedias de escucha y aprendizaje del protocolo de árbol de expansión. Diseñado exclusivamente para puertos terminales, previene retrasos de conectividad durante la negociación DHCP.

- **Post Office Protocol Version 3 (POP3):** Protocolo cliente-servidor de capa de aplicación diseñado para recuperar mensajes de correo electrónico desde un servidor remoto hacia un cliente local a través del puerto TCP 110. Descarga los correos a la estación de trabajo y habitualmente los elimina del buzón del servidor, optimizando el espacio de almacenamiento centralizado.

- **Recovery Point Objective (RPO):** Métrica de continuidad operativa que define la cantidad máxima tolerable de pérdida de datos medida en unidades de tiempo que la organización está dispuesta a asumir ante un desastre en sus sistemas de información. Determina la frecuencia con la que deben ejecutarse las copias de seguridad de las bases de datos corporativas.

- **Recovery Time Objective (RTO):** Parámetro de gestión de continuidad que establece el plazo máximo admisible que puede permanecer inactivo un servicio, base de datos o componente de red tras ocurrir una interrupción imprevista, antes de que impacte negativamente en las operaciones del negocio. Define la celeridad exigida a los procedimientos de restauración.

- **RFC 1918:** Estándar de la Internet Engineering Task Force que reserva rangos de direcciones IPv4 para uso exclusivo en redes corporativas privadas sin posibilidad de ser enrutadas en la Internet pública. Define los bloques 10.0.0.0/8, 172.16.0.0/12 y 192.168.0.0/16, garantizando la reutilización y conservación del espacio de direccionamiento global.

- **Routing Information Protocol Version 2 (RIPv2):** Protocolo de enrutamiento dinámico interior basado en el algoritmo de vector de distancia que utiliza la cantidad de saltos como métrica para seleccionar la mejor ruta hacia un destino, con un límite máximo de 15 saltos. Admite máscaras de subred de longitud variable, difunde actualizaciones por multidifusión e incluye autenticación de mensajes.

- **Ruta Estática Flotante (Floating Static Route):** Ruta estática de respaldo configurada con una distancia administrativa numéricamente superior a la de la ruta principal o la del protocolo de enrutamiento dinámico activo. Permanece inactiva y fuera de la tabla de enrutamiento mientras el enlace primario está operativo, instalándose de forma automática ante caídas de la conexión principal.

- **Ruta por Defecto (Default Route):** Ruta estática comodín representada por una dirección y máscara de todos ceros que coincide con cualquier destino no especificado de forma explícita en la tabla de enrutamiento. Es configurada en los enrutadores de borde para dirigir todo el tráfico con destino externo hacia la puerta de enlace del proveedor de servicios de Internet.

- **Secure Shell (SSH):** Protocolo criptográfico de capa de aplicación que facilita el acceso, control y administración remota de enrutadores, conmutadores y servidores a través de una sesión cifrada y autenticada. Sustituye las conexiones de texto plano vulnerables como Telnet mediante el uso de algoritmos de clave pública y cifrado simétrico en el puerto TCP 22.

- **Service Level Agreement (SLA):** Contrato formal suscrito entre un proveedor de servicios de comunicaciones o computación en la nube y la empresa cliente, en el cual se definen con rigor matemático los parámetros mínimos de calidad, rendimiento y porcentaje de disponibilidad garantizada, estipulando compensaciones económicas en caso de incumplimiento.

- **Service Set Identifier (SSID):** Secuencia alfanumérica de hasta 32 caracteres que identifica de manera unívoca a una red inalámbrica de área local frente a los terminales cliente. Permite segmentar el entorno inalámbrico institucional en redes independientes para ejecutivos e invitados, asociando cada identificador a una red virtual cableada específica.

- **Simple Mail Transfer Protocol (SMTP):** Protocolo estándar de la familia TCP/IP empleado para la transferencia y entrega de mensajes de correo electrónico entre servidores de mensajería o desde terminales cliente hacia servidores salientes. Opera sobre la capa de transporte mediante el puerto TCP 25 utilizando comandos de texto plano o sesiones cifradas mediante extensiones TLS.

- **Spanning Tree Protocol (STP):** Protocolo de capa de enlace de datos estandarizado como IEEE 802.1D que previene la formación de bucles lógicos en topologías de conmutación Ethernet redundantes. Deshabilita dinámicamente puertos de respaldo para conformar un árbol lógico sin ciclos, activando los enlaces alternativos de manera automática si un enlace principal falla.

- **Switch Virtual Interface (SVI):** Interfaz lógica de enrutamiento de capa 3 configurada dentro de un conmutador multicapa para representar a una red virtual específica en la tabla de enrutamiento. Proporciona una dirección IP que actúa como puerta de enlace predeterminada para todos los hosts asignados a dicha VLAN, posibilitando el enrutamiento inter-VLAN por hardware.

- **Transport Layer Security (TLS):** Protocolo criptográfico moderno diseñado para proporcionar privacidad, confidencialidad e integridad en las comunicaciones establecidas a través de Internet. Empleado en servicios web seguros, correo electrónico y túneles de respaldo hacia la nube, establece canales seguros mediante el intercambio y validación de certificados digitales.

- **Variable Length Subnet Mask (VLSM):** Técnica avanzada de ingeniería de direccionamiento IP que permite subdividir un espacio de direcciones en subredes de tamaños desiguales mediante el uso de máscaras de subred de longitud diferenciada. Optimiza el aprovechamiento de los bloques IPv4 al asignar a cada segmento únicamente la cantidad de direcciones requeridas según su demanda.

- **Virtual Local Area Network (VLAN):** Segmentación lógica de una red de conmutación física que agrupa estaciones de trabajo y dispositivos de red en dominios de difusión independientes sin importar su ubicación física en el campus. Mejora la seguridad interna, reduce la propagación de tramas de difusión y optimiza la administración técnica por departamentos organizacionales.

- **Virtual Private Cloud (VPC):** Red virtual aislada y privada aprovisionada dentro del entorno de infraestructura compartida de un proveedor de servicios de computación en la nube. Permite a la empresa definir sus propios rangos de direccionamiento IP, subredes, tablas de enrutamiento y pasarelas de seguridad para albergar instancias y respaldos corporativos.

- **VLAN de Gestión (Management VLAN):** Red virtual de área local aislada y dedicada exclusivamente al transporte del tráfico administrativo de control y mantenimiento de los dispositivos de red intermediarios. Alberga las interfaces virtuales de gestión de conmutadores y enrutadores junto con la estación de administración PC-Admin bajo estrictas políticas de acceso cifrado por SSH.

- **VLAN Nativa (Native VLAN):** Red virtual específica configurada en los enlaces troncales bajo el estándar IEEE 802.1Q encargada de transportar las tramas Ethernet que transitan sin etiqueta de identificación de red. En esquemas de alta seguridad, se asigna a un identificador exclusivo como la VLAN 999 sin direccionamiento IP ni puertos de acceso para neutralizar ataques de salto de red.

- **Wide Area Network (WAN):** Infraestructura de telecomunicaciones que interconecta redes de área local distribuidas en amplias zonas geográficas, como ciudades, regiones o países. Emplea enlaces dedicados de alta velocidad arrendados a operadores de telecomunicaciones para asegurar la comunicación fluida entre la sede central y sus diferentes sucursales remotas.

- **Wireless Local Area Network (WLAN):** Red de comunicación de datos de cobertura local que prescinde de medios cableados para la interconexión de terminales, empleando ondas de radio en el espectro de 2.4 GHz y 5 GHz. Facilita la movilidad del personal corporativo y clientes, integrándose con la red cableada mediante puntos de acceso y estrictos controles de seguridad.

- **WPA2-Personal:** Estándar de seguridad inalámbrica que implementa autenticación basada en clave precompartida y cifrado de datos mediante el algoritmo AES con el protocolo CCMP. Proporciona una barrera de protección robusta contra accesos no autorizados e interceptación de tráfico en redes inalámbricas departamentales e institucionales.
