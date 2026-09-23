# 3.4 Implementación de Enrutamiento dinámico y estático

<!--
HITO 2 (Semana 15) - ALCANCE WAN Y SALIDA A INTERNET
Detallar:
1. Enrutamiento estático y ruta predeterminada (Default Route) hacia los ISPs en el Router de Borde/Frontera.
2. Configuración de enrutamiento dinámico RIPv2 en los routers de la red interna (Sede Principal y Sucursales).
3. Desactivación de auto-summary (no auto-summary) e interfaces pasivas (passive-interface) en interfaces LAN.
4. Verificación de tablas de enrutamiento ('show ip route', 'show ip protocols') y pruebas de conectividad inter-sedes.
-->

## 3.4.1 Implementación de enrutamiento estático

### Scripts de configuración (Ruta por defecto e ISP)
```cisco
! Configuración de ruta por defecto y rutas estáticas
```

### Verificación de enrutamiento estático
[Capturas de consola y tablas de rutas]

## 3.4.2 Implementación de enrutamiento dinámico (RIPv2)

### Scripts de configuración RIPv2
```cisco
! Configuración de router rip, version 2, no auto-summary, network ...
```

### Verificación de tablas de enrutamiento dinámico y conectividad inter-sedes
[Capturas de tablas de enrutamiento y pruebas de ping extremo a extremo]
