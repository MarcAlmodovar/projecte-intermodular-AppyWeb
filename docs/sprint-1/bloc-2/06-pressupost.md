# 6. Presupuesto económico

En este documento calculamos cuánto cuesta implantar la solución TIC de AppyWeb. Las cantidades son las mismas que en `05-recursos.md`, y los precios son reales, consultados en tiendas online en noviembre de 2026.

**Todos los importes incluyen el IVA (21 %).** Cuando una fuente da el precio sin IVA, se lo hemos sumado y lo indicamos en la tabla.

## 1. Inversión inicial (pago único)

### Equipos de los trabajadores

| Elemento | Descripción | Cant. | Precio unitario | Subtotal | Fuente |
|:---|:---|:---:|---:|---:|:---|
| Portátil ligero | Lenovo ThinkPad E14 Gen 7, Intel Core Ultra 5 228V, 32 GB, SSD 512 GB, Windows 11 Pro | 4 | 1.424,11 € | 5.696,44 € | [PcComponentes](https://www.pccomponentes.com/portatil-lenovo-thinkpad-e14-gen-7-14-intel-core-ultra-5-228v-32gb-512gb-ssd-ai-boost-windows-11-pro-negro) |
| Portátil de alto rendimiento | Lenovo ThinkPad E14 Gen 7, Intel Core Ultra 7 255H, 32 GB, SSD 1 TB, Windows 11 Pro | 5 | 1.729,01 € | 8.645,05 € | [PcComponentes](https://www.pccomponentes.com/portatil-lenovo-thinkpad-e14-gen-7-14-intel-core-ultra-7-255h-32gb-1tb-ssd-w11-pro-aluminio) |
| Dock USB-C | Dell WD19S 130 W con Ethernet Gigabit | 5 | 241,00 € | 1.205,00 € | [PcComponentes](https://www.pccomponentes.com/dell-wd19s-130w-estacion-de-base-usb-3-2-gen-2-usb-c) |
| Monitor 24" | Dell P2425H Full HD IPS (2 por puesto de Desarrollo y 2 para Administración) | 12 | 200,99 € | 2.411,88 € | [PcComponentes](https://www.pccomponentes.com/monitor-dell-p2425h-238-fullhd-100hz-ips-usb-32-vesa-comfortview-altura-ajustable) |
| Ordenador de Administración | Lenovo ThinkCentre neo 50t Gen 5, Intel Core i5-14400, 16 GB, SSD 512 GB, Windows 11 Pro | 1 | 1.044,30 € | 1.044,30 € | [PcComponentes](https://www.pccomponentes.com/pc-lenovo-thinkcentre-neo-50t-gen-5-intel-core-i5-14400-16gb-512gb-ssd-dvd-rw-windows-11-pro) |
| Ordenador de Diseño | Intel Core i7-12700F, 32 GB, SSD 1 TB, gráfica RTX 4060 | 2 | 1.519,37 € | 3.038,74 € | [PcComponentes](https://www.pccomponentes.com/ordenador-sobremesa-pc-racing-delta-gaming-intel-core-i7-12700f-32gb-1tb-ssd-rtx-4060) |
| Monitor 27" 4K | Dell P2725QE 4K IPS | 2 | 440,39 € | 880,78 € | [PcComponentes](https://www.pccomponentes.com/monitor-dell-27-4k-uhd-100hz-ips-flicker-free-low-blue-light-usb-c-90w) |
| Teclado y ratón | Logitech MK295 inalámbricos | 12 | 29,99 € | 359,88 € | [PcComponentes](https://www.pccomponentes.com/logitech-mk295-silent-wireless-combo-de-raton-y-teclado-inalambricos) |
| Pantalla de la sala de reuniones | Samsung Crystal UHD 55" 4K | 1 | 349,99 € | 349,99 € | [PcComponentes](https://www.pccomponentes.com/tv-samsung-crystal-uhd-led-ue55u7022huxxh-55-4k-ultrahd-50hz-smart-tv-tizen-hdr10-plus) |
| | | | **Subtotal** | **23.632,06 €** | |

### Servidores y almacenamiento

| Elemento | Descripción | Cant. | Precio unitario | Subtotal | Fuente |
|:---|:---|:---:|---:|---:|:---|
| Servidor de comunicaciones (firewall) | Protectli Vault FW4C, mini PC de 4 puertos de red | 1 | 269,00 € | 269,00 € | [Protectli](https://eu.protectli.com/product/fw4c/) |
| Servidor web de la DMZ | Mini PC Ninkear L12 Pro, Intel Core i9-12900HK, 16 GB, SSD 1 TB, doble Ethernet | 1 | 589,99 € | 589,99 € | [PcComponentes](https://www.pccomponentes.com/mini-pc-ninkear-l12-pro-intel-core-i9-12900hk-16gb-iris-xe-1tb-ssd-windows-11-doble-ethernet) |
| Servidor interno | HPE ProLiant ML110 Gen11, Intel Xeon Bronze 3408U, 16 GB | 1 | 2.239,00 € | 2.239,00 € | [PcComponentes](https://www.pccomponentes.com/hpe-proliant-ml110-gen11-torre-4-5u-intel-xeon-bronze-3408u-16gb) |
| Discos del servidor interno | SSD Kingston DC600M 960 GB para servidor (2 discos en RAID 1) | 2 | 729,00 € | 1.458,00 € | [PcComponentes](https://pccomponentes.com/kingston-dc600m-25-ssd-960gb-uso-mixto-enterprise-sata-30) |
| NAS | Synology DiskStation DS923+, 4 bahías | 1 | 559,65 € | 559,65 € | [PcComponentes](https://www.pccomponentes.com/synology-diskstation-ds923-servidor-de-almacenamiento-nas) |
| Discos del NAS | WD Red Plus 4 TB (4 discos en RAID 5) | 4 | 131,41 € | 525,64 € | [PcComponentes](https://www.pccomponentes.com/disco-duro-wd-red-plus-35-4tb-128mb-sata-3) |
| SAI | APC Back-UPS Pro 1500 VA | 1 | 519,01 € | 519,01 € | [PcComponentes](https://www.pccomponentes.com/apc-back-ups-pro-1500-230v) |
| | | | **Subtotal** | **6.160,29 €** | |

### Red e impresión

| Elemento | Descripción | Cant. | Precio unitario | Subtotal | Fuente |
|:---|:---|:---:|---:|---:|:---|
| Switch gestionable | TP-Link TL-SG2428P, 24 puertos Gigabit PoE+ | 1 | 344,15 € | 344,15 € | [PcComponentes](https://www.pccomponentes.com/tp-link-tl-sg2428p-switch-24-puertos-gigabit-poe-plus-4-puertos-sfp) |
| Punto de acceso Wi-Fi 6 | TP-Link Omada EAP650, PoE | 2 | 116,99 € | 233,98 € | [PcComponentes](https://www.pccomponentes.com/tp-link-eap650-omada-punto-acceso-wifi-6-doble-banda-ax3000) |
| Impresora multifunción | Brother MFC-L3760CDW, láser color, red, doble cara y escáner | 1 | 389,99 € | 389,99 € | [PcComponentes](https://www.pccomponentes.com/brother-mfc-l3760cdw-multifuncion-laser-led-color-wifi-fax) |
| Armario rack | Rack de pared 19" 9U con accesorios | 1 | 184,95 € | 184,95 € | [PcComponentes](https://www.pccomponentes.com/aiten-data-armario-rack-mural-19-9u-600-x-450-x-520-mm-montado-con-accesorios) |
| Cableado | Bobina de cable UTP Cat 6 de 305 m | 1 | 162,99 € | 162,99 € | [PcComponentes](https://www.pccomponentes.com/aisens-bobina-cable-de-red-rj45-cat-6-utp-awg24-rigido-305m-gris) |
| | | | **Subtotal** | **1.316,06 €** | |

### Licencias de pago único

| Elemento | Descripción | Cant. | Precio unitario | Subtotal | Fuente |
|:---|:---|:---:|---:|---:|:---|
| Windows Server 2025 Standard | Licencia de 16 núcleos para el servidor interno | 1 | 1.978,00 € | 1.978,00 € | [Microsoft Store](https://www.microsoft.com/es-es/d/windows-server-2025-standard/dg7gmgf0wzrw) |
| Windows 11 Pro | Ya viene incluido en los portátiles y ordenadores | 12 | 0,00 € | 0,00 € | — |
| pfSense CE, Ubuntu Server, Visual Studio Code y Git | Software libre y gratuito | — | 0,00 € | 0,00 € | — |
| Synology DSM | Sistema del NAS, incluido con el equipo | 1 | 0,00 € | 0,00 € | — |
| | | | **Subtotal** | **1.978,00 €** | |

### Total de la inversión inicial

| Concepto | Importe |
|:---|---:|
| Equipos de los trabajadores | 23.632,06 € |
| Servidores y almacenamiento | 6.160,29 € |
| Red e impresión | 1.316,06 € |
| Licencias de pago único | 1.978,00 € |
| **Total inversión inicial (IVA incluido)** | **33.086,41 €** |

## 2. Costes anuales (suscripciones)

| Elemento | Descripción | Cant. | Precio | Coste anual | Fuente |
|:---|:---|:---:|---:|---:|:---|
| Microsoft 365 Empresa Estándar | Correo, Office y Teams. 12,13 €/usuario/mes sin IVA (14,68 € con IVA) | 12 usuarios | 14,68 €/mes | 2.113,92 € | [Microsoft](https://www.microsoft.com/es-es/microsoft-365/business/microsoft-365-business-basic) |
| Synology C2 Storage | Copia de seguridad en la nube de 1 TB (datos críticos: proyectos y contabilidad) | 1 | 106,75 €/año | 106,75 € | [Innet Imperia](https://shop.innetimperia.it/catalogo-prodotti/networking/accessori-networking/licenze-software-per-networking/p/1-c2onestorag1t1y-synology-c2-onestorage-1tb-1-anno) |
| API de inteligencia artificial | Uso estimado del asistente de IA de la web (pago por uso) | 1 | 20 €/mes (estimado) | 240,00 € | [Precios de la API](https://www.anthropic.com/pricing) |
| Adobe Creative Cloud para equipos | Programas de diseño gráfico y vídeo | 2 licencias | 1.250,17 €/año | 2.500,34 € | [iCreatia](https://www.icreatia.es/producto/adobe-creative-cloud-anual-licencia-teams/) |
| Figma Professional | Diseño UI/UX de webs y apps. 16 $/mes por puesto (≈ 14 €) | 2 puestos | 14 €/mes | 336,00 € | [Comparativa de precios de Figma](https://www.lilachbullock.com/figma-pricing/) |
| Antivirus ESET PROTECT Entry | 24,99 € por equipo sin IVA (30,24 € con IVA) | 13 equipos | 30,24 €/año | 393,12 € | [Bechtle](https://www.bechtle.com/at-en/shop/eset-protect-entry-11-25-1y--4611924--p) |
| **Total costes anuales (IVA incluido)** | | | | **5.690,13 €** | |

## 3. Resumen del presupuesto

| Concepto | Base imponible | IVA (21 %) | Total |
|:---|---:|---:|---:|
| Inversión inicial | 27.344,14 € | 5.742,27 € | 33.086,41 € |
| Costes del primer año | 4.702,59 € | 987,54 € | 5.690,13 € |
| **Total primer año** | **32.046,73 €** | **6.729,81 €** | **38.776,54 €** |

A partir del segundo año, la empresa solo paga las suscripciones: unos **5.690 € al año**.

## 4. Justificación de las decisiones

- **Gama profesional en los portátiles.** Elegimos ThinkPad porque es una gama pensada para empresas, resistente y con Windows 11 Pro incluido, que hace falta para unir los equipos al dominio. Los de Desarrollo llevan 32 GB y 1 TB porque usan máquinas virtuales y modelos de IA.
- **Mini PC para el firewall y la DMZ.** Un servidor de torre sería mucho más caro y no hace falta para estas funciones. El firewall necesita varios puertos de red, y el servidor web solo aloja la web, las demos y el asistente de IA.
- **Servidor de torre para el servidor interno.** Gestiona las cuentas de usuario de toda la empresa, así que necesita ser fiable. Lleva dos discos en RAID 1 para que, si falla uno, no se pare el servicio.
- **NAS con copia en la nube.** Es la solución híbrida que elegimos en `02-alternatives-viabilitat.md`. El NAS da velocidad en la oficina y la copia en la nube protege los datos si hay un incendio, un robo o un ransomware.
- **Software libre siempre que se puede.** pfSense, Ubuntu Server, Visual Studio Code y Git son gratuitos y cumplen perfectamente su función, así que ahorramos en licencias.
- **Precios.** Hemos comparado varias opciones y elegido las más económicas que cumplen los requisitos de `05-recursos.md`.

## 5. Comprobación del presupuesto

- **Coherencia con `05-recursos.md`.** Las cantidades coinciden: 12 ordenadores (4 portátiles ligeros, 5 de alto rendimiento y 3 sobremesas), 3 servidores, 1 NAS, 1 switch, 2 puntos de acceso, 1 impresora y 12 teclados y ratones.
- **Es razonable para la empresa.** AppyWeb factura unos 440.000 € al año (Bloc 1). La inversión inicial supone alrededor del 7,5 % de un año de facturación, y los equipos se amortizan en 4 o 5 años. Las suscripciones suponen unos 474 € al mes, menos de 40 € por trabajador.

## 6. Observaciones

- Los precios pueden cambiar con el tiempo. Los hemos consultado en noviembre de 2026.
- El precio de Windows Server corresponde a la licencia de 16 núcleos de la tienda de Microsoft. Antes de comprar hay que confirmar cuántas licencias de acceso de usuario (CAL) incluye para los 12 trabajadores.
- El coste de la API de inteligencia artificial es una estimación, porque se paga según el uso.
- No hemos incluido la mano de obra de la instalación, porque la haremos los miembros del grupo (ver `05-recursos.md`).
