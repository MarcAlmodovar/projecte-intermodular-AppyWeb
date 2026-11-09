# Plan de direccionamiento y nombre de equipos
Aqui voy a definir las redes de AppyWeb y las direcciones IP de sus equipos. El plan se basa en las necesidades mencionadas en 04-adrecament-ip.md y en los equipos de el bloc 01

## Redes de la empresa

| Red | Direccion de red | Mascara de red | Puerta de enlace | Uso|
|:---|:---|:---|:---|:---|
|Lan interna| 192.168.10.0 | 255.255.255.0 (/24) | 192.168.10.1 | Ordenadores de los trabajadores, NAS e impresoras |
|DMZ| 192.168.20.0 | 255.255.255.0 (/24) | 192.168.20.1 | Servidor de la web corporativa |
| Invitados | 192.168.30.0 | 255.255.255.0 (/24) | 192.168.30.1 | Wifi para los clientes |
| VPN | 10.8.0.0 | 255.255.255.0 (/24) | 10.8.0.1 | Teletrabajo y acceso desde fuera de la empresa |

Hemos elegido el prefijo /24, porque es el mas estandar y permite 254 equipos, con nuestros 12 trabajadores nos sobra.

## Separacion entre red interna y DMZ

El servidor web de la DMZ es accesible desde internet, por lo que es el equipo con mas riesgo de sufrir un ataque. si lo ponemos en una red separada el firewall impide que los ataques pasen a las demas redes, asi aunque alguien ataque a el servidor de la DMZ no podran tener acceso a los NAS ni a los equipos de los trabajadores.

La red de invitados tambien esta separada, para que los clientes esten en redes distintas y que si intentan atacar a la red, tampoco llege a los equipos de dentro de la empresa.

## Organizacion de Red

Para que la red este organizada la organizaremos asi:

| Rango | Uso |
|:---|:---|
|.1 | Routers/ firewall (Puerta de enlaze) |
|.2 - .9 | Dispositivos de Red (switches, y puntos de acceso) |
|.10 - .49 | Servidores e Impresoras (IPs fijas) |
|.100 - .199| Ordenadores de los trabajadores(IPs fijas, por departamento)|
|.200 - .250| Rango de DHCP |

## Tabla de direccionamiento

| Nombre del equipo | Red | Direccion IP | Mascara | Puerta de enlace |
|:---|:---|:---|:---|:---|
| APW Web (LAN) | LAN | 192.168.10.1 | /24 | / |
| APW Web (DMZ) | DMZ | 192.168.20.1 | /24 | / |
| APW Web (Invitados) | Invitados | 192.168.30.1 | /24 | / |
| APW-ROUTER (VPN) | VPN | 10.8.0.1 | /24 | — |
| APW-SWITCH | LAN interna | 192.168.10.2 | /24 | 192.168.10.1 |
| APW-AP-01 | LAN interna | 192.168.10.3 | /24 | 192.168.10.1 |
| APW-AP-02 | LAN interna | 192.168.10.4 | /24 | 192.168.10.1 |
| APW-NAS | LAN interna | 192.168.10.10 | /24 | 192.168.10.1 |
| APW-IMPRESORA | LAN interna | 192.168.10.20 | /24 | 192.168.10.1 |
| APW-DIR-01 (Dirección) | LAN interna | 192.168.10.101 | /24 | 192.168.10.1 |
| APW-ADM-01 (Administración) | LAN interna | 192.168.10.111 | /24 | 192.168.10.1 |
| APW-COM-01 a APW-COM-03 (Comercial) | LAN interna | 192.168.10.121 – 192.168.10.123 | /24 | 192.168.10.1 |
| APW-DEV-01 a APW-DEV-05 (Desarrollo) | LAN interna | 192.168.10.131 – 192.168.10.135 | /24 | 192.168.10.1 |
| APW-DIS-01 a APW-DIS-02 (Diseño) | LAN interna | 192.168.10.141 – 192.168.10.142 | /24 | 192.168.10.1 |
| APW-WEB (servidor web y demos) | DMZ | 192.168.20.10 | /24 | 192.168.20.1 |
| Dispositivos de invitados | Invitados | 192.168.30.200 – 192.168.30.250 (DHCP) | /24 | 192.168.30.1 |
| Trabajadores conectados por VPN | VPN | 10.8.0.100 – 10.8.0.150 (automática) | /24 | 10.8.0.1 |

## Nombres de los equipos 

Todos los Nombres empiezan por APW, el departamento a el que pertenecen y su numero de equipo, asi se sabe rapidamente de quien es.

## Comprobacion de el plan

- Cada red usa rangos diferentes(192.168.10.0, 192.168.20.0, 192.168.30.0, 10.8.0.0) para que este mas organizado
- Ninguna direccion IP se repite dentro de la red.
- hay 12 ordenadores en la red, uno por persona, como en el bloc 1
- Cada departamento tiene su propio bloque de IP, y queda espacio libre para añadir mas personal.

