# Capítulo 1: Presentación, Análisis y Diseño

## 1.1 Descripción del caso estudio

### 1.1.1 Descripción de la empresa

MIEMPRESA es una corporación transnacional que mantiene operaciones en diversos países de la región sudamericana, incluyendo Argentina, Chile, Ecuador y Colombia. La casa matriz de la organización está establecida en el Perú, punto central desde el cual se coordinan las directrices administrativas, financieras y los lineamientos tecnológicos corporativos.

En el ámbito nacional, la compañía cuenta con una sede principal corporativa situada en la ciudad de Lima y cuatro sedes sucursales ubicadas en La Libertad, Ica, Huánuco y Puno. Esta distribución geográfica responde a la necesidad de mantener presencia física y descentralizada en las distintas regiones del país.

La estructura interna de la organización se articula mediante un modelo jerárquico estandarizado que inicia a nivel de filial por país, se desglosa en sedes por ciudad y se organiza en departamentos funcionales específicos. En cada sede operan unidades organizacionales clave como Administración, Logística, Finanzas, Marketing y Ventas, además del área de Servidores y los usuarios de las redes WiFi (Ejecutivos y Clientes).

Debido a su dispersión geográfica y a la continua interacción operativa entre sedes, la organización requiere actualizar su plataforma de comunicaciones corporativa, reemplazando una infraestructura que operó durante diez años de forma desordenada por una arquitectura de red jerárquica, escalable y de alta disponibilidad.

### 1.1.2 Descripción del problema o necesidad

Durante la última década, MIEMPRESA experimentó una expansión continua de sus operaciones que no estuvo acompañada por una planificación técnica adecuada de su infraestructura de telecomunicaciones. Cada vez que la organización inauguraba una nueva sede o filial, los equipos de comunicación se adquirían e instalaban de forma reactiva para atender la urgencia inmediata, delegando las implementaciones en consultoras externas que no dejaron documentación técnica ni lineamientos estandarizados.

Como resultado de este crecimiento desordenado, la corporación acumuló una plataforma de red fragmentada, inestable y difícil de mantener. Las fallas recurrentes de comunicación entre la sede principal en Lima y las sucursales departamentales impactan negativamente en las operaciones cotidianas del negocio, exponiendo las siguientes problemáticas específicas:

- **Crecimiento desordenado y ausencia de documentación técnica:** Tras diez años de incorporaciones improvisadas, la empresa no dispone de planos topológicos actualizados, diagramas de conexión ni inventarios formales del equipamiento. Esta falta de información impide al personal técnico diagnosticar fallas con rapidez y dificulta cualquier intento de modernización o mantenimiento preventivo.

- **Incompatibilidad entre marcas por uso de protocolos cerrados:** A lo largo de los años se adquirieron equipos de diversos fabricantes que utilizaban tecnologías propietarias y cerradas en lugar de estándares universales. Al conectar equipos de marcas distintas entre sí, surgían bloqueos e incompatibilidades de comunicación, obligando además al personal de soporte a aprender múltiples sistemas operativos diferentes, lo que retrasaba enormemente la solución de averías.

- **Conflictos por duplicidad y solapamiento de direcciones IP:** La asignación manual y no planificada del direccionamiento provocó que sedes distintas utilicen los mismos rangos de red. Como consecuencia directa, los usuarios sufren caídas intermitentes de conexión y bloqueos de acceso a los sistemas centrales debido a colisiones constantes de direcciones IP entre sedes.

- **Falta de segmentación lógica mediante VLANs:** Todos los departamentos de la empresa (como Finanzas, Administración, Ventas, Logística y Servidores) comparten el mismo dominio de red junto con los usuarios de las redes inalámbricas y clientes visitantes. Esta convivencia sin aislamiento satura el ancho de banda con tráfico de difusión innecesario y crea graves riesgos de seguridad al exponer información financiera y confidencial a accesos no autorizados.

- **Ausencia de un protocolo de enrutamiento dinámico en la red WAN:** La comunicación entre la sede central en Lima y las cuatro sedes sucursales depende de rutas manuales rígidas. Al no contar con un protocolo de enrutamiento automático y universal, la red carece de mecanismos de adaptación ante contingencias; si un enlace de telecomunicaciones se interrumpe, las oficinas remotas quedan incomunicadas hasta que un técnico intervenga manualmente.

- **Carencia de políticas de seguridad y administración remota segura:** La infraestructura no dispone de listas de control de acceso ni filtros perimetrales que restrinjan el tráfico no autorizado hacia los servidores locales y corporativos. Asimismo, la administración de routers y switches se realiza sin mecanismos de cifrado robustos, exponiendo las credenciales de gestión a posibles interceptaciones dentro de la red.

- **Vulnerabilidad ante pérdida de datos por falta de respaldo en la nube:** La información crítica de la empresa se almacena exclusivamente en servidores locales sin un plan automatizado de copias de seguridad remotas. Esta dependencia del almacenamiento físico deja a la organización expuesta a pérdidas irreversibles de información operativa y financiera frente a fallas de hardware, siniestros en los edificios o incidentes imprevistos.

### 1.1.3 Objetivos de la solución propuesta

Con la finalidad de superar las deficiencias diagnosticadas y establecer una plataforma tecnológica escalable que acompañe el crecimiento del negocio, se formulan los siguientes objetivos de implementación de la red empresarial:

#### Objetivo General

Diseñar e implementar una arquitectura de red empresarial jerárquica, escalable y segura para la sede principal y sucursales de MIEMPRESA en el Perú, optimizando el espacio de direccionamiento IP y garantizando la alta disponibilidad local, la interconexión segura y estandarizada entre sedes a través de la red WAN, y la continuidad del negocio mediante una solución de respaldo en la nube.

#### Objetivos Específicos

- Diseñar el esquema de direccionamiento IPv4 para la corporación y las sedes nacionales mediante técnicas FLSM y VLSM con una proyección de crecimiento a diez años.
- Implementar la arquitectura de red local jerárquica mediante segmentación por VLANs y redundancia de primer salto con HSRP en cada sede.
- Desplegar la infraestructura de red inalámbrica en cada sede con seguridad WPA2, aislando el tráfico de usuarios ejecutivos e invitados.
- Configurar los enlaces WAN punto a punto bajo protocolo PPP y enrutamiento dinámico RIPv2 entre la sede principal en Lima y las cuatro sucursales.
- Desplegar los servicios de red fundamentales de DHCP, DNS, páginas Web, transferencia de archivos FTP con permisos por sede y correo electrónico.
- Aplicar políticas de seguridad perimetral mediante listas de control de acceso y habilitar la administración remota segura de los equipos vía SSH.
- Dimensionar los costos del equipamiento técnico y diseñar una solución de respaldo en la nube para asegurar la continuidad del negocio.