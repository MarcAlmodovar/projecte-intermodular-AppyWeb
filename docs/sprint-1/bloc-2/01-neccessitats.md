# 1. Identificación de las necesidades TIC

Antes de proponer una solución, hemos revisado qué necesita cada departamento de Appy Web para trabajar. Partimos de lo que definimos en el Bloc 1: 12 trabajadores repartidos en 5 departamentos, una oficina en Alcoy y una parte del trabajo en teletrabajo.

## Necesidades comunes a toda la empresa

Hay necesidades que tienen todos los trabajadores, sea cual sea su departamento:

- **Conexión a Internet rápida y estable**, porque casi todo el trabajo es online (servidores en la nube, Google Ads, reuniones con clientes…).
- **Una cuenta de usuario para cada trabajador**, con su contraseña, para saber quién accede a cada cosa.
- **Carpetas compartidas** para no tener los archivos repartidos por los ordenadores de cada uno.
- **Copias de seguridad automáticas**, porque perder el código o los diseños de un cliente sería un problema muy grave.
- **Seguridad**: firewall, antivirus y separar la red interna de los servicios que se ven desde Internet.
- **Acceso remoto seguro (VPN)** para los que teletrabajan o están visitando a un cliente.

## Tabla de necesidades por departamento

| Departamento | Necesidad | Usuarios afectados | Justificación |
|---|---|---|---|
| Dirección / Gerencia | Acceso remoto por VPN a los archivos de la empresa | 1 (Gerente) | Trabaja muchas veces fuera de la oficina, reunido con clientes, bancos o proveedores. |
| Dirección / Gerencia | Acceso a todas las carpetas de la empresa (permisos de administrador de datos) | 1 | Tiene que poder revisar los proyectos, los presupuestos y la contabilidad. |
| Administración y Atención al Cliente | Impresora multifunción en red (imprimir y escanear) | 1 (y el resto de forma puntual) | Imprime contratos y facturas y escanea documentos firmados. |
| Administración y Atención al Cliente | Carpeta privada con permisos solo para Administración y Dirección | 2 | Las nóminas, facturas y datos de clientes son confidenciales (protección de datos). |
| Administración y Atención al Cliente | Conexión por cable estable | 1 | Trabaja siempre en la oficina con programas de contabilidad y facturación online. |
| Comercial y Marketing Digital | Wi-Fi en toda la oficina y en la sala de reuniones | 3 | Trabajan con portátil y hacen presentaciones a los clientes que vienen a la oficina. |
| Comercial y Marketing Digital | Acceso remoto por VPN | 3 | Visitan a clientes y necesitan los presupuestos y los informes desde fuera. |
| Desarrollo de Software e IA | Conexión rápida por cable (dock) y acceso al NAS | 5 | Descargan y suben mucho código, imágenes de máquinas virtuales y modelos de IA. |
| Desarrollo de Software e IA | Un servidor en la DMZ para la web corporativa y las demos para clientes | 5 (y los clientes desde fuera) | Tienen que enseñar a los clientes cómo va su web o app antes de publicarla, sin abrir la red interna. |
| Desarrollo de Software e IA | Acceso por VPN a la red de la oficina | 5 | Hacen teletrabajo algunos días. |
| Diseño UI/UX y Contenidos | Mucho espacio compartido en el NAS | 2 | Los archivos de diseño y vídeo ocupan mucho y los tienen que ver los programadores. |
| Diseño UI/UX y Contenidos | Conexión por cable (Gigabit) | 2 | Mueven archivos muy grandes entre su ordenador y el NAS. |
| Toda la empresa | Wi-Fi de invitados separada | Clientes que vienen a la oficina | Los clientes pueden tener Internet sin entrar en la red de la empresa. |
| Toda la empresa | Web corporativa | Clientes y posibles clientes | Es el escaparate de la empresa. Al ser una agencia web, es lo primero que miran los clientes. |
| Toda la empresa | SAI (sistema de alimentación ininterrumpida) | 12 | Si se va la luz, los servidores y el NAS se apagan bien y no se pierden datos. |

## Fuentes consultadas

Para decidir estas necesidades nos hemos basado en:

- Los documentos del Bloc 1 de nuestro proyecto: `01-empresa.md`, `02-organitzacio.md`, `03-recursos-tic.md` y `04-maquinari-programari.md`.
- Lo que hemos visto en los módulos de Serveis en Xarxa, Sistemes Operatius en Xarxa y Seguretat Informàtica.
- La web de INCIBE para empresas, con recomendaciones de ciberseguridad para pymes: https://www.incibe.es/empresas
- Las webs de agencias reales parecidas a la nuestra que usamos en el Bloc 1 como referencia.