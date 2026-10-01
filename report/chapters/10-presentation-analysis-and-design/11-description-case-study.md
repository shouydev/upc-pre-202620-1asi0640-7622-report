# Capítulo 1: Presentación, Análisis y Diseño

## 1.1 Descripción del caso estudio

### 1.1.1 Descripción de la empresa

MIEMPRESA es una corporación transnacional con presencia consolidada en el mercado sudamericano, orientada a la gestión y comercialización de servicios a gran escala. La organización dispone de filiales operativas en Argentina, Chile, Ecuador y Colombia, mientras que su casa matriz se ubica en el Perú, punto neurálgico desde el cual se coordinan las directrices estratégicas, operativas, financieras y de infraestructura tecnológica.
En el territorio nacional, la compañía mantiene una presencia descentralizada para dar cobertura a sus operaciones comerciales y logísticas. La sede principal corporativa está establecida en la ciudad de Lima y cuatro sedes sucursales ubicadas estratégicamente en La Libertad, Ica, Huánuco y Puno.
La estructura organizativa adopta un esquema jerárquico estandarizado que inicia a nivel de filial por país, se desglosa en sedes por ciudad y se consolida internamente en unidades organizacionales específicas. En cada sede convergen departamentos esenciales como Administración, Finanzas, Ventas, Logística, Marketing y Tecnologías de la Información, además de contingentes de usuarios inalámbricos ejecutivos y clientes que demandan acceso constante a los servicios del negocio.
Dada la dispersión geográfica y el intercambio continuo de información operativa, la organización depende críticamente de una infraestructura de telecomunicaciones sólida, escalable y segura. La conectividad integral entre la casa matriz en Lima, sus cuatro sedes departamentales y los enlaces fronterizos hacia las filiales internacionales requiere una arquitectura de red jerárquica que garantice alta disponibilidad, soporte el crecimiento proyectado y erradique las fallas de integración existentes.

### 1.1.2 Descripción del problema o necesidad

La infraestructura tecnológica de MIEMPRESA operó durante la última década bajo un esquema reactivo y carente de planificación estratégica. Ante la apertura progresiva de nuevas filiales y dependencias, la adquisición e instalación de equipamiento se ejecutó sin lineamientos arquitectónicos estandarizados, ocasionando una red desarticulada cuya documentación técnica resultó inexistente o desactualizada frente a las demandas crecientes de la corporación.
La dependencia histórica de consultorías externas propició la coexistencia de equipos de red pertenecientes a múltiples fabricantes, muchos de los cuales operaban bajo protocolos y funciones propietarias incompatibles entre sí. Esta heterogeneidad tecnológica generó serias dificultades de interoperabilidad, elevó la complejidad en la administración del equipamiento y prolongó de forma crítica la curva de aprendizaje del personal técnico, limitando la capacidad de respuesta ante fallas operativas recurrentes.
El síntoma más crítico de esta desorganización se evidenció durante la integración de las nuevas sedes departamentales, donde se suscitaron bloqueos continuos en el acceso a los servicios corporativos centrales. Las auditorías técnicas constataron la presencia de conflictos por duplicidad y solapamiento de direcciones IP, interrumpiendo el flujo de datos y la operatividad entre la casa matriz y las sucursales.
A este escenario se suma la carencia de una segmentación lógica mediante redes de área local virtuales, lo cual provoca que el tráfico corporativo crítico de finanzas y administración comparta dominios de difusión con el tráfico de usuarios comerciales e invitados inalámbricos. La inexistencia de políticas formales de control de acceso, sumada a la ausencia de un esquema centralizado y seguro de copias de seguridad en la nube, expone la información estratégica a vulnerabilidades de seguridad y compromete la continuidad del negocio ante incidentes operativos.
A partir de la evaluación técnica de la infraestructura, se sintetizan las problemáticas críticas en los siguientes aspectos:
•	Crecimiento inorgánico y desactualización documental: Expansión reactiva durante una década sin planos topológicos vigentes, inventarios formales ni esquemas de red documentados.
•	Incompatibilidad multimarca y tecnologías propietarias: Coexistencia de dispositivos de múltiples proveedores con protocolos cerrados que impiden la interoperabilidad y ralentizan el soporte técnico.
•	Duplicidad y solapamiento de direcciones IP: Asignación empírica del espacio de red que genera conflictos de direcciones duplicadas entre sedes, provocando caídas de enlace e indisponibilidad de servicios corporativos.
•	Ausencia de segmentación lógica por VLAN: Tráfico sensible de finanzas, administración y servidores conviviendo en el mismo dominio de difusión que los usuarios comerciales e invitados inalámbricos.
•	Falta de políticas de control de acceso perimetral e interno: Carencia de filtros de seguridad estructurados y listas de control de acceso para mitigar vectores de ataque y accesos no autorizados a recursos críticos.
•	Carencia de enrutamiento dinámico estandarizado: Inexistencia de un protocolo de enrutamiento convergente y escalable para articular la comunicación WAN entre la sede principal y las sucursales.
•	Vulnerabilidad ante pérdida de datos por falta de respaldo offsite: Dependencia exclusiva de almacenamiento local sin un plan automatizado de copias de seguridad en la nube que garantice la continuidad del negocio.

### 1.1.3 Objetivos de la solución propuesta

Con la finalidad de superar las deficiencias diagnosticadas y establecer una plataforma tecnológica escalable que acompañe el crecimiento del negocio, se formulan los siguientes objetivos de implementación de la red empresarial:

#### Objetivo General

Diseñar e implementar una solución de red empresarial jerárquica, escalable y segura para la sede principal y sucursales de MIEMPRESA en el Perú, garantizando la interconexión eficiente con sus filiales internacionales, la optimización del espacio de direccionamiento IP y la alta disponibilidad de los servicios corporativos.

#### Objetivos Específicos

•	Diseñar el esquema de direccionamiento lógico
•	Implementar la arquitectura de conmutación LAN
•	Establecer la infraestructura de red inalámbrica
•	Configurar la conectividad WAN y el enrutamiento intercedes
•	Desplegar los servicios de red fundamentales
•	Aplicar políticas de seguridad perimetral e interna
•	Desarrollar el dimensionamiento técnico-económico y la solución de respaldo en la nube