# 5. Selección de recursos materiales y humanos

Aquí explicamos qué hardware, software y personas hacen falta para montar la solución. Las cantidades son las mismas que en el diagrama de red del apartado 3 y que en el presupuesto del apartado 6.

## Hardware

### Equipos clientes

| Equipo | Cantidad | Función | Requisitos principales | Justificación |
|---|---|---|---|---|
| Portátil ligero | 4 | 1 para Dirección y 3 para Comercial y Marketing | Intel Core i5 o Ryzen 5, 16 GB de RAM, SSD de 512 GB, menos de 1,5 kg | Trabajan dentro y fuera de la oficina y hacen presentaciones a los clientes. |
| Portátil de alto rendimiento | 5 | Desarrollo de Software e IA | Intel Core i7 o Ryzen 7, 32 GB de RAM, SSD de 1 TB | Compilan código y usan máquinas virtuales y modelos de IA. |
| Dock USB-C con 2 monitores de 24" | 5 | Puesto fijo de Desarrollo en la oficina | Dock con puerto Ethernet Gigabit | Así conectan el portátil por cable y trabajan con dos pantallas. |
| Ordenador de sobremesa | 1 | Administración | Intel Core i5, 16 GB de RAM, SSD de 512 GB y 2 monitores de 24" | Trabaja siempre en la oficina con la contabilidad y la facturación. |
| Ordenador de sobremesa para diseño | 2 | Diseño UI/UX y Contenidos | Intel Core i7 o Ryzen 7, 32 GB de RAM, tarjeta gráfica dedicada y monitor de 27" 4K | Los programas de diseño y vídeo necesitan mucha potencia y colores precisos. |
| Teclado y ratón | 12 | Todos los trabajadores | Inalámbricos | Uno para cada trabajador. |
| Pantalla de la sala de reuniones | 1 | Presentaciones a clientes | 55" con HDMI | Para enseñar a los clientes las webs, las apps y los informes. |

En total son 12 ordenadores, 9 portátiles y 3 sobremesas, uno por cada trabajador.

### Servidores

| Equipo | Cantidad | Función | Requisitos principales | Justificación |
|---|---|---|---|---|
| Servidor de comunicaciones o firewall | 1 | Firewall, NAT, VPN y separación entre WAN, LAN y DMZ | Mini PC con 3 puertos de red Gigabit y 8 GB de RAM | Es lo que permite tener una DMZ y la VPN para el teletrabajo. |
| Servidor web de la DMZ | 1 | Web corporativa, asistente de IA y demos para clientes | 4 núcleos, 16 GB de RAM y SSD de 1 TB | Los servicios que se ven desde Internet tienen que estar separados de la red interna. |
| Servidor interno | 1 | Cuentas de usuario, DNS y DHCP | De 4 a 6 núcleos, 16 GB de RAM y 2 discos SSD en RAID 1 | Centraliza los usuarios y los permisos de toda la empresa. |
| NAS | 1 | Archivos compartidos y copias de seguridad | 4 bahías con 4 discos de 4 TB en RAID 5 y copia automática a la nube | Los archivos de diseño ocupan mucho y hay que tener copias de seguridad. Es la parte local de la solución híbrida que elegimos en el apartado 2. |
| SAI | 1 | Protección eléctrica de los servidores y el NAS | 1500 VA | Evita perder datos si se va la luz. |

### Dispositivos de red

| Equipo | Cantidad | Función | Requisitos principales | Justificación |
|---|---|---|---|---|
| Switch gestionable | 1 | Conectar por cable la red interna | 24 puertos Gigabit, PoE y VLAN | Hay unos 15 equipos conectados por cable y deja margen para crecer. El PoE da corriente a los puntos de acceso. |
| Punto de acceso Wi-Fi 6 | 2 | Wi-Fi de la oficina y de la sala de reuniones | Wi-Fi 6, PoE y varias redes Wi-Fi | Uno cubre la oficina y otro la sala. Emiten la red de la empresa y la de invitados, que es uno de los aspectos innovadores del apartado 2. |
| Impresora multifunción láser a color | 1 | Imprimir y escanear | Conexión de red, impresión a doble cara y escáner | Se usa sobre todo para contratos y facturas. |
| Cableado y armario rack | 1 lote | Instalación de la red | Cable Cat 6, rack de pared de 9U y latiguillos | Para dejar el cableado y los servidores ordenados. |

## Software

| Software | Dónde se usa | Justificación |
|---|---|---|
| Windows 11 Pro | Los 12 ordenadores | Permite unir los equipos al dominio y es compatible con los programas de todos los departamentos. |
| Windows Server 2025 | Servidor interno | Para las cuentas de usuario con Active Directory, el DNS y el DHCP. Es lo que trabajamos en Sistemes Operatius en Xarxa. |
| pfSense | Servidor de comunicaciones | Es un firewall gratuito y de código abierto que tiene VPN y permite crear una DMZ. |
| Ubuntu Server con Nginx | Servidor web de la DMZ | Es gratuito, ligero y muy usado para servidores web. |
| Sistema del NAS, por ejemplo Synology DSM | NAS | Viene con el NAS y permite programar las copias de seguridad. |
| Almacenamiento en la nube para las copias, por ejemplo Synology C2 Storage | NAS | Es la parte de la nube de la solución híbrida. Guarda una copia cifrada fuera de la oficina por si hay un incendio, un robo o un ataque de ransomware. |
| Suscripción a la API de un modelo de IA | Servidor web de la DMZ | Es el aspecto innovador del asistente. Responde las dudas habituales de los clientes en la web y quita trabajo a Atención al Cliente. |
| Microsoft 365 Empresa | Toda la empresa | Correo corporativo, Office y Teams para las reuniones. |
| Visual Studio Code y Git | Desarrollo | Editor de código gratuito y control de versiones. |
| Figma y Adobe Creative Cloud | Diseño | Son los programas más usados para diseño UI/UX y diseño gráfico. |
| Antivirus empresarial | Los 12 ordenadores y los servidores Windows | Protege contra malware y se gestiona todo desde un solo sitio. |

## Recursos humanos para la implantación

Estas son las personas que montarían la solución. No son trabajadores de Appy Web, sino el equipo técnico que haría el proyecto, que en nuestro caso somos los miembros del grupo.

| Perfil | Persona del grupo | Responsabilidades |
|---|---|---|
| Jefe de proyecto | Marc Almodovar | Coordinar el proyecto, controlar las fechas y el presupuesto y hablar con la empresa. |
| Técnico de redes | Izan Pons | Instalar el cableado, el switch y los puntos de acceso y configurar el firewall, la DMZ y la VPN. |
| Técnico de sistemas | Marc Almodovar | Instalar los servidores, crear las cuentas de usuario y las carpetas compartidas y configurar las copias de seguridad. |
| Técnico de soporte y documentación | Izan Pons | Preparar los ordenadores de los trabajadores, hacer las pruebas, documentarlo todo y enseñar a los trabajadores a usar el sistema. |