---
tema: "Fundamentos de Redes"
tipo: concepto
creado: 2026-09-25
---

## **¿Qué es Internet?**

**Internet** (también conocida como **red de redes**) es una **[[Internetwork|internetwork]]** pública y global: la interconexión de millones de [[Redes|redes]] distintas —administradas de forma independiente por miles de **[[ISP|ISPs]]** y organizaciones— que permite la **comunicación** y el **intercambio de [[Datos]]** entre dispositivos alrededor del mundo, sin importar su ubicación física.

> [!important]- Internet es solo el ejemplo más grande de dos conceptos que ya viste
> Como estudiaste en [[Internetwork]] y en [[WAN]], Internet no introduce ningún mecanismo nuevo — es simplemente la **WAN** más grande que existe, y una **internetwork** pública en vez de privada. Una empresa que conecta las [[LAN|LANs]] de dos oficinas mediante un [[Enrutador (Router)|router]] también crea una internetwork y técnicamente una WAN — solo que privada y a mucha menor escala que Internet.

### Cómo funciona

Internet opera bajo un conjunto de **[[Estándares y Protocolos|protocolos estándar]]**, principalmente **[[Modelo de Red (TCP ∕ IP)|TCP/IP]]**, que garantizan que la [[Información]] se transmita correctamente entre las distintas redes que la componen, sin importar el tipo de [[Dispositivos de una Red|dispositivo]], sistema operativo o proveedor involucrado. Cada red individual conserva su propio [[Direccionamiento|direccionamiento]] y administración, pero todas acuerdan hablar el mismo protocolo para poder comunicarse entre sí — el mismo principio que ya viste al crear una [[WAN]].

### A qué se accede a través de Internet

A través de Internet es posible acceder a servicios como la **[[World Wide Web|World Wide Web]]**, **correo electrónico**, **mensajería**, **streaming**, **[[Llamada Telefónica (PSTN vs VoIP)|VoIP]]** y muchos otros, todos basados en el modelo **[[Cliente-servidor]]** — aunque, como viste en [[P2P (Peer to Peer)]], algunos servicios (compartición de archivos, criptomonedas) usan un modelo distinto sobre la misma infraestructura.

> [!important]- Web no es sinónimo de Internet
> Es un error común: **Internet** es la infraestructura de redes interconectadas (el "cómo" se transmite todo); la **[[World Wide Web]]** es solo uno de los servicios que corre sobre esa infraestructura (páginas web vía [[Protocolo HTTP ∕ HTTPS|HTTP]]), igual que el correo electrónico o el streaming son otros servicios distintos que también usan Internet, pero no son "la web".

### Origen del Internet

Internet nació como **ARPANET** (*Advanced Research Projects Agency Network*), una red experimental creada en 1969 por el Departamento de Defensa de EE.UU., a través de su agencia de investigación **ARPA** (hoy DARPA). Su objetivo inicial no era la comunicación masiva de hoy, sino conectar computadoras de universidades y centros de investigación para **compartir recursos computacionales** costosos y escasos en esa época.

- **1969**: ARPANET conecta sus primeros 4 nodos (UCLA, Stanford, UC Santa Bárbara y la Universidad de Utah).
- **1973-1974**: se desarrolla **[[Modelo de Red (TCP ∕ IP)|TCP/IP]]**, diseñado específicamente para que **redes distintas** pudieran interconectarse entre sí de forma confiable — resolviendo el mismo problema que hoy describe [[Internetwork]]. El estándar fue formalizado por **[[Estándares y Protocolos|IETF]]** mediante documentos RFC.
- **1983**: ARPANET adopta oficialmente TCP/IP como su protocolo estándar, reemplazando el protocolo original — este momento se considera el nacimiento técnico de "Internet" tal como se entiende hoy.
- **1989-1991**: Tim Berners-Lee crea la **[[World Wide Web]]** ([[Protocolo HTTP ∕ HTTPS|HTTP]], HTML, URLs) — la web es una *aplicación* que corre sobre Internet, no Internet en sí misma, aunque hoy ambos términos se usen indistintamente en el lenguaje cotidiano.
- **Década de 1990 en adelante**: Internet se abre al uso comercial y público, dejando de ser exclusivamente académico/militar, aparecen los primeros **[[ISP|ISPs]]** comerciales, y comienza el crecimiento explosivo que la convirtió en la [[WAN|WAN]] global que conoces hoy.

> [!important]- Internet no fue diseñado para lo que es hoy
> ARPANET se diseñó para conectar un puñado de computadoras de investigación de forma resiliente (que sobreviviera si algún nodo fallaba) — nunca se planeó para soportar miles de millones de dispositivos, streaming de video o comercio electrónico. Que TCP/IP haya podido escalar hasta ese punto, sin rediseñarse desde cero, es parte de por qué se considera un estándar tan bien logrado.

### Cómo te conectas tú a esa red de redes

Un usuario final nunca se conecta "directo" a Internet — se conecta a través de un **[[ISP]]**, que a su vez está interconectado con otros ISPs mediante acuerdos de *peering* y protocolos como BGP (ver [[ISP]] para el detalle de los niveles Tier 1/2/3). Ese camino completo, desde tu dispositivo hasta el servidor que quieres alcanzar, es justo lo que ya viste encadenado paso a paso en [[Funcionamiento de las Redes]]: obtener una IP vía [[Protocolo DHCP|DHCP]], resolver el dominio vía [[Protocolo DNS|DNS]], resolver la MAC del siguiente salto vía [[Resolución de Direcciones (ARP y ND)|ARP/ND]], y enrutar el tráfico salto a salto a través de tu [[LAN]], posiblemente una [[MAN]], y finalmente la WAN pública.

> [!important]- Tu dirección IP pública no es realmente "tuya"
> Como viste en [[NAT]], si tienes una red doméstica u [[SOHO]], todos tus dispositivos comparten una única IP pública asignada por tu ISP — Internet, como red global, solo "ve" esa IP compartida, nunca las direcciones privadas internas de tu red.

### Acceso privado sobre Internet pública

No todo lo que viaja por Internet es público: una **[[VPN]]** permite crear un túnel cifrado sobre esta infraestructura compartida, y una **[[Intranet]]** reutiliza exactamente las mismas tecnologías de Internet (TCP/IP, HTTP) pero restringida al uso interno de una organización — ambos son buenos ejemplos de que "Internet" es la infraestructura subyacente, no un único uso fijo de ella.

#### En resumen
Internet es la internetwork pública más grande que existe — millones de redes independientes interconectadas mediante TCP/IP y los ISPs que las conectan entre sí. Nació en 1969 como ARPANET, un proyecto militar/académico sin relación con su uso actual, y adoptó TCP/IP en 1983 como el estándar que le permitió escalar hasta lo que es hoy. La Web, el correo y el streaming son servicios que corren sobre ella, no sinónimos de ella; y tecnologías como VPN e Intranet muestran que esa misma infraestructura puede usarse de forma privada.

## Ver también

- [[Internetwork]]
- [[WAN]]
- [[ISP]]
- [[World Wide Web]]
- [[Modelo de Red (TCP ∕ IP)]]
- [[VPN]]
- [[Intranet]]
- [[Funcionamiento de las Redes]]