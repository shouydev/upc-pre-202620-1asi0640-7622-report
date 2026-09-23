# 2.3 Esquema de direccionamiento IP para cada sede (VLSM)

<!--
HITO 1 (Semana 7) - OBLIGATORIO
Aplicación de Máscara de Subred de Longitud Variable (VLSM) dentro de cada sede, considerando la proyección de crecimiento del 25% a 10 años:
-->

## 2.3.1 Sede Principal (Lima)

<!--
Cálculo VLSM ordenado de mayor a menor número de hosts requeridos:
- Ventas: 98 req -> 123 proyectados
- Administración: 80 req -> 100 proyectados
- Marketing: 29 req -> 37 proyectados
- Logística: 25 req -> 32 proyectados
- Finanzas: 21 req -> 27 proyectados
- WiFi Ejecutivos: 21 req -> 27 proyectados
- WiFi Clientes: 15 req -> 19 proyectados
- Servidores: 12 req -> 15 proyectados
- Nativa / Gestión: Equipos de red
Tabla VLSM detallada: VLAN, Departamento, Hosts Requeridos, Hosts Asignados, Dirección de Red, Máscara (prefijo y decimal), Primer IP Útil, Último IP Útil, Broadcast, Default Gateway.
-->

[Contenido y tabla VLSM Sede Lima]

## 2.3.2 Sede Sucursal 1 (La Libertad)

<!--
Cálculo VLSM para La Libertad:
160 usuarios requeridos -> 200 usuarios proyectados (+25%), más WiFi y gestión.
-->

[Contenido y tabla VLSM Sede La Libertad]

## 2.3.3 Sede Sucursal 2 (Ica)

<!--
Cálculo VLSM para Ica:
190 usuarios requeridos -> 238 usuarios proyectados (+25%), más WiFi y gestión.
-->

[Contenido y tabla VLSM Sede Ica]

## 2.3.4 Sede Sucursal 3 (Huánuco)

<!--
Cálculo VLSM para Huánuco:
96 usuarios requeridos -> 120 usuarios proyectados (+25%), más WiFi y gestión.
-->

[Contenido y tabla VLSM Sede Huánuco]

## 2.3.5 Sede Sucursal 4 (Puno)

<!--
Cálculo VLSM para Puno:
105 usuarios requeridos -> 132 usuarios proyectados (+25%), más WiFi y gestión.
-->

[Contenido y tabla VLSM Sede Puno]
