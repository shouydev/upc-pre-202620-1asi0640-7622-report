# Conclusiones y recomendaciones

## Conclusiones

Tras el diseño, dimensionamiento e implementación integral de la infraestructura de telecomunicaciones para MIEMPRESA, se formulan las siguientes conclusiones técnicas basadas en los resultados operativos obtenidos en la solución:

- **Eficacia y escalabilidad del esquema de direccionamiento lógico:** La aplicación combinada de técnicas FLSM para los enlaces y filiales multinacionales, junto con VLSM para la distribución interna de las sedes peruanas proyectadas al 25% a diez años, erradicó definitivamente los conflictos históricos de duplicidad y solapamiento de direcciones IP. El diseño asignó de forma óptima los bloques del espacio privado RFC 1918, garantizando capacidad de crecimiento para los próximos diez años sin fragmentación de subredes.

- **Robustez de la conmutación jerárquica y alta disponibilidad local:** La implementación del modelo de tres capas mediante conmutadores Catalyst 3650 y 2960 permitió aislar los dominios de difusión departamentales mediante VLANs independientes bajo el estándar IEEE 802.1Q. Asimismo, la configuración de redundancia de primer salto con HSRP versión 2 entre los conmutadores de distribución aseguró la continuidad del tráfico local ante fallas físicas de hardware, con tiempos de conmutación transparentes para las estaciones de trabajo.

- **Segregación y control en la conectividad inalámbrica:** El despliegue de puntos de acceso con doble identificador de red inalámbrica y seguridad WPA2-Personal logró aislar de forma estricta el tráfico sensible de los usuarios ejecutivos respecto a los clientes e invitados. La integración con servidores DHCP locales simplificó el aprovisionamiento dinámico de parámetros de red, garantizando que los dispositivos visitantes únicamente dispongan de salida directa hacia Internet sin visibilidad hacia la infraestructura interna.

- **Estandarización y convergencia en la red de área amplia:** La interconexión entre la sede central en Lima y las cuatro sedes sucursales mediante enlaces punto a punto bajo protocolo PPP con autenticación PAP y CHAP resolvió la incompatibilidad multimarca preexistente. Además, la adopción de enrutamiento dinámico RIPv2 proporcionó una sincronización automática de tablas de rutas, mientras que la configuración de rutas estáticas conmutables hacia ISP1 e ISP2 garantizó la disponibilidad del servicio de salida a Internet ante eventuales caídas del proveedor principal.

- **Efectividad en los servicios corporativos y control de acceso:** La distribución descentralizada de servidores Web, DHCP y FTP locales en cada sede, combinada con la centralización del correo electrónico y DNS en Lima, satisfizo las demandas operativas de la organización. Las listas de control de acceso aplicadas en la capa de distribución garantizaron el estricto cumplimiento de las políticas de acceso al servidor de archivos, restringiendo la visibilidad entre sucursales y canalizando la gestión administrativa exclusivamente vía SSH desde la estación autorizada PC-Admin en la VLAN 99.

- **Sostenibilidad económica y resiliencia mediante la solución Cloud:** El análisis comparativo entre proveedores de nube pública demostró la viabilidad técnica y financiera de externalizar las copias de seguridad hacia plataformas como Amazon S3 o Azure Blob Storage frente a la adquisición de infraestructura física redundante en cada sede. Esta estrategia permite alcanzar objetivos exigentes de tiempo de recuperación y punto de recuperación con costos operativos mensuales predecibles bajo un modelo de pago por consumo.

## Recomendaciones

Con el propósito de garantizar la estabilidad operativa, optimizar el rendimiento y orientar la evolución tecnológica continua de la plataforma de red implementada, se plantean las siguientes recomendaciones de ingeniería:

- **Monitoreo proactivo y telemetría de red:** Implementar una plataforma centralizada de gestión basada en el protocolo simple de administración de red SNMP y análisis de flujos NetFlow. Esta herramienta permitirá vigilar en tiempo real el consumo de ancho de banda en los enlaces WAN seriales, la temperatura de los conmutadores y la tasa de descarte de paquetes, facilitando el diagnóstico preventivo antes de que se presenten degradaciones de servicio.

- **Automatización y pruebas periódicas del plan de respaldo en la nube:** Establecer políticas de ciclo de vida automatizadas en el repositorio de almacenamiento Cloud para migrar copias de seguridad antiguas hacia niveles de archivo de menor costo tras sesenta días de retención. Asimismo, se aconseja ejecutar simulacros semestrales de restauración total de bases de datos para comprobar que los tiempos de respuesta cumplan con el objetivo de tiempo de recuperación estipulado para la organización.

- **Mantenimiento preventivo y actualización de software:** Programar ventanas periódicas de mantenimiento fuera del horario laboral para la actualización de imágenes del sistema operativo Cisco IOS XE en conmutadores y enrutadores. Estas labores deben incluir la aplicación de parches de seguridad, la verificación física de ventiladores y fuentes de alimentación redundantes, y la comprobación de los tiempos de respuesta del protocolo HSRP en cada sede.

- **Fortalecimiento de la seguridad en la capa de acceso:** Incorporar progresivamente mecanismos de endurecimiento en los conmutadores de acceso, tales como inspección dinámica de paquetes ARP mediante DAI, supervisión de indagación DHCP Snooping y protección de puertos con Port Security, con la finalidad de mitigar ataques internos de denegación de servicio o suplantación de direcciones.

- **Planificación de la transición hacia IPv6:** Diseñar un plan de direccionamiento bajo el esquema IPv6 Dual-Stack que prepare a la corporación para la adopción gradual del nuevo protocolo de capa de red. Esta iniciativa permitirá convivir con el direccionamiento IPv4 actual sin interrumpir la operación, asegurando la compatibilidad tecnológica futura ante la transición global de los proveedores de servicios de Internet.
