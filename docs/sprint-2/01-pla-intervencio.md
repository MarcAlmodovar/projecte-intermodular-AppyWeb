# 1. Plan de intervención del Sprint 2

En este sprint implantamos en máquinas virtuales la infraestructura de AppyWeb que diseñamos en el Sprint 1: la red interna (LAN), la DMZ y el servidor de comunicaciones que encamina entre ellas y da DHCP a la LAN. La plantilla de la empresa la representamos con un cliente Windows y un cliente Linux.

## 1. Cambios respecto al Sprint 1

Mantenemos el direccionamiento del apartado `04-adrecament-ip.md` (LAN 192.168.10.0/24 y DMZ 192.168.20.0/24) y los nombres de los equipos. Hay dos cambios, porque así lo pide el enunciado del Sprint 2:

| Sprint 1 | Sprint 2 | Motivo |
|:---|:---|:---|
| Servidor de comunicaciones con pfSense | Servidor de comunicaciones con Ubuntu Server | El enunciado pide un servidor Linux. pfSense se basa en FreeBSD. |
| DHCP en el servidor interno (APW-SRV) | DHCP en el servidor de comunicaciones (APW-SRVCOMM) | El enunciado pide el DHCP en el servidor de comunicaciones. El servidor interno queda preparado para Active Directory y DNS en el Sprint 3. |

## 2. Secuencia de tareas

El sprint dura 5 semanas, del 16 de noviembre al 18 de diciembre, con 2 horas por semana (10 horas en total).

| Tarea | Semana | Horas | Depende de | Responsable | Colaborador |
|:---|:---:|:---:|:---|:---|:---|
| Estructura de carpetas `docs/sprint-2` | 1 | 0,5 | — | Izan | — |
| T1 · Plan de intervención | 1 | 1,5 | — | Marc | Izan |
| T2 · Máquinas virtuales | 1–2 | 2 | T1 | Izan | Marc |
| T3 · Configuración de la red y diagrama | 2–3 | 1,5 | T2 | Marc | Izan |
| T4 · Servidor de comunicaciones | 3 | 1,5 | T3 | Izan | Marc |
| T5 · Servicio DHCP | 4 | 1 | T4 | Marc | Izan |
| T6 · Pruebas de conectividad | 4–5 | 1,5 | T5 | Izan | Marc |
| T7 · Seguimiento e incidencias | 1–5 | 5 min al final de cada sesión | — | Marc e Izan | — |
| README, revisión y entrega | 5 | 0,5 | T6 | Marc e Izan | — |
| **Total** | | **10 h** | | | |

Las tareas van en cadena: no se puede configurar la red sin las máquinas, ni el DHCP sin el encaminamiento, ni hacer las pruebas sin el DHCP.

## 3. Recursos necesarios

### Máquinas virtuales

| Máquina | Función | Sistema | RAM | CPU | Disco | Red |
|:---|:---|:---|:---:|:---:|:---:|:---|
| APW-SRVCOMM | Servidor de comunicaciones: encaminamiento y DHCP | Ubuntu Server 24.04 LTS | 1 GB | 1 | 20 GB | NAT + APW-LAN + APW-DMZ |
| APW-SRV | Servidor interno | Windows Server 2025 | 4 GB | 2 | 50 GB | APW-LAN |
| APW-CLIWIN | Cliente Windows | Windows 11 Pro | 4 GB | 2 | 60 GB | APW-LAN |
| APW-CLILIN | Cliente Linux | Ubuntu Desktop 24.04 LTS | 2 GB | 2 | 25 GB | APW-LAN |
| APW-WEB | Servidor de la DMZ | Ubuntu Server 24.04 LTS | 1 GB | 1 | 20 GB | APW-DMZ |
| **Total** | | | **12 GB** | **8** | **175 GB** | |

No hace falta tenerlas todas encendidas a la vez con toda la RAM. Para las pruebas finales sí tienen que funcionar las cinco juntas.

### Imágenes y software

- **Imágenes ISO:** Ubuntu Server 24.04 LTS, Ubuntu Desktop 24.04 LTS, Windows Server 2025 (evaluación) y Windows 11 Pro (evaluación). Se descargan de las webs oficiales de Ubuntu y Microsoft.
- **Software:** VirtualBox, Git, Visual Studio Code y Canva para actualizar el diagrama.
- **Servicios:** `isc-dhcp-server` para el DHCP en APW-SRVCOMM.

## 4. Reparto de las máquinas entre los ordenadores

Las cinco máquinas se instalan en el **mismo ordenador del aula, el de Marc**. Así las redes internas `APW-LAN` y `APW-DMZ` funcionan directamente, porque en VirtualBox dos redes internas con el mismo nombre en ordenadores distintos no se conectan solas.

Izan trabaja en sus tareas desde ese mismo ordenador o prepara las máquinas en el suyo y las exporta en formato OVA para importarlas en el de Marc. Así todas acaban en el mismo equipo.

## 5. Permisos y autorizaciones

- Pedimos permiso al profesor para usar VirtualBox y unos 175 GB del disco del ordenador del aula.
- Usamos las versiones de evaluación gratuitas de Windows Server y Windows 11, que permiten usarlos legalmente durante el curso.
- No modificamos la red física del aula. Solo usamos el modo NAT y redes internas de VirtualBox, que no salen del ordenador.
- No subimos al repositorio discos de máquinas virtuales, ISO ni contraseñas.

## 6. Riesgos y medidas preventivas

| Riesgo | Medida preventiva | Norma del aula relacionada |
|:---|:---|:---|
| Muchas horas delante de la pantalla | Hacer pausas cortas cada hora, mantener una buena postura y tener la pantalla a la altura de los ojos | Respetar los descansos entre sesiones |
| Conexiones eléctricas | No desconectar cables con el equipo encendido, no sobrecargar las regletas y avisar al profesor si algo falla | No manipular el hardware ni los cables del aula sin permiso |
| Pérdida de datos | Hacer una instantánea de cada máquina antes de cada cambio importante y subir la documentación a GitHub al final de cada sesión | Guardar el trabajo y apagar los equipos correctamente |
| Cambios de red que afecten a otros equipos | Usar solo NAT y redes internas. No usar el adaptador puente y no activar DHCP fuera de la LAN virtual | No cambiar la configuración de red del ordenador del aula |

**Medios de recuperación:** instantáneas de VirtualBox, copia de la documentación en GitHub y exportación OVA de las máquinas ya terminadas.

## 7. Imprevistos y soluciones

| Imprevisto | Solución prevista |
|:---|:---|
| No hay RAM suficiente para las 5 máquinas a la vez | Bajar las máquinas Linux al mínimo y encender solo las necesarias para cada prueba. Si aun así no cabe, avisar al profesor para usar otro equipo |
| Falta espacio en disco | Usar discos de tamaño dinámico y borrar las instantáneas antiguas que ya no hagan falta |
| Una instalación no arranca | Comprobar la ISO y la configuración de la máquina (tipo de sistema, EFI, RAM). Si no se soluciona, volver a la última instantánea o reinstalar |
| Un cliente no recibe IP por DHCP | Comprobar que está en la red interna `APW-LAN`, que el servicio está activo y que no hay otro DHCP de VirtualBox en esa red. Mientras tanto, poner una IP fija temporal y documentarlo |

## 8. Seguimiento

- **Al final de cada sesión** dedicamos 5 minutos a mover las tarjetas de Trello y a apuntar en `07-seguiment-incidencies.md` lo previsto, lo hecho, el tiempo usado, los problemas y lo que queda pendiente. Comparamos el avance real con este plan.
- **Si hay un retraso que afecte a la entrega**, se lo comunicamos al profesor por mensaje en Aules o en clase. Lo anotamos en el documento 07 junto con el ajuste acordado.
- **Tablero de Trello:** https://trello.com/b/3FqRQWGf/sprint-1
