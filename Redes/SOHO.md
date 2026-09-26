---
tema: "Fundamentos de Redes"
tipo: concepto
creado: 2026-09-24
---
## **¿Qué es SOHO?**

**SOHO** (del inglés *Small Office - Home Office*, "pequeña oficina - oficina en casa") es un término que describe un **entorno de trabajo de pequeña escala** — ya sea una oficina reducida o un espacio doméstico usado para trabajar — caracterizado por un **bajo volumen de usuarios y de tráfico de red**, en comparación con una empresa mediana o grande.

### ¿A qué se aplica el término?

- **Entorno / red SOHO**: el contexto físico y de red en sí — pocos usuarios, infraestructura simple.
- **[[Dispositivos de una Red|Dispositivos SOHO]]**: [[Enrutador (Router)|routers]], switches, access points, etc., pensados para uso **profesional o semiprofesional**, pero sin capacidad de asumir el volumen de trabajo de un entorno empresarial grande.

> [!important]- Diferencia clave
> Un dispositivo SOHO no es lo mismo que un dispositivo doméstico genérico ni que uno de nivel *enterprise*: maneja más carga y ofrece más funciones que un equipo casero simple, pero muchas menos que uno diseñado para cientos de usuarios simultáneos.

### Ejemplos típicos

- Un **[[Enrutador (Router)|enrutador inalámbrico integrado]]** de uso hogareño o de pequeña oficina.
- Switches de pocos puertos para conectar unos cuantos equipos.
- Access points de gama básica.

### Características de una red doméstica

- **Un solo dispositivo hace casi todo**: el [[Enrutador (Router)|router inalámbrico integrado]] suele combinar router, switch, access point y servidor [[Protocolo DHCP|DHCP]] en un solo equipo.
- **Direccionamiento privado y automático**: los dispositivos reciben una [[Dirección IP]] privada automáticamente vía DHCP — rara vez alguien configura una IP estática a mano.
- **Una sola IP pública para toda la red**: aunque haya varios dispositivos conectados, todos salen a Internet compartiendo una única [[Dirección IP]] pública, gracias a **NAT** (*Network Address Translation*), que traduce las direcciones privadas internas hacia esa IP pública compartida.
- **Mezcla de conectividad**: combina dispositivos por [[Conectividad alámbrica e inalámbrica|cable y Wi-Fi]] en la misma red, sin necesidad de [[Segmentación de Redes|segmentarla]] en subredes.
- **Seguridad básica integrada**: el router trae un [[Firewall]] simple activado por defecto, suficiente para el nivel de exposición de una red doméstica.
- **Pocos dispositivos, sin servidores dedicados**: a diferencia de una red empresarial, no suele haber un [[Servidor]] dedicado — cada dispositivo es principalmente [[Cliente|cliente]].

> [!important]- Sin NAT, esto no sería posible
> Una red doméstica típica tiene una sola IP pública asignada por el ISP, pero múltiples dispositivos necesitando salir a Internet. NAT es lo que permite que todos compartan esa única IP pública, traduciendo cada conexión saliente para que la respuesta regrese al dispositivo correcto — sin NAT, cada dispositivo necesitaría su propia IP pública, que son limitadas y más costosas.

### Características de una red de oficina pequeña

- **Más dispositivos, pero todavía manejable sin personal de TI dedicado**: entre 5 y 50 equipos aproximadamente, superando lo que un solo router doméstico gestiona con comodidad.
- **Equipos dedicados por función**: en vez de un solo router haciéndolo todo, es común separar el [[Switch|switch]] del [[Enrutador (Router)|router]] y del [[Firewall]], cada uno un dispositivo SOHO propio, aunque siguen siendo equipos de gama básica/semiprofesional.
- **Puede tener un servidor propio**: a diferencia de la red doméstica, es común un [[Servidor]] dedicado para archivos compartidos o impresión en red, aunque sigue siendo poco frecuente tener servidores especializados (DNS, correo propio, etc.).
- **Cableado más planificado**: aunque a pequeña escala, suele haber al menos un principio de [[Cableado Estructurado]] (una toma por escritorio, un switch central), en vez de cables sueltos como en una casa.
- **NAT sigue siendo la norma**: igual que en la red doméstica, comparte una sola IP pública para toda la oficina mediante NAT — la escala no suele justificar un rango de IPs públicas propio.
- **Segmentación ocasional**: algunas oficinas separan la red de invitados de la red interna mediante [[Segmentación de Redes|subredes]] o Wi-Fi independiente, algo raro de ver en el entorno puramente doméstico.

> [!important]- La línea entre "doméstico" y "oficina pequeña" es de escala, no de tecnología
> Ambos entornos usan básicamente los mismos tipos de dispositivos SOHO, NAT, y direccionamiento privado automático. La diferencia real está en la **cantidad de dispositivos** y en si vale la pena **separar funciones** en equipos dedicados (switch, router y firewall aparte) en vez de un solo equipo integrado — no en que la oficina use tecnología fundamentalmente distinta.

#### En resumen
SOHO no es una tecnología puntual, sino una categoría de escala: tanto del entorno de red como de los dispositivos pensados para operar en él, a medio camino entre el uso doméstico simple y el uso empresarial. Una red doméstica suele resolverlo todo con un solo equipo integrado; una oficina pequeña empieza a separar funciones en equipos dedicados, aunque ambas comparten NAT y direccionamiento privado automático como base.

## Ver también

- [[Dispositivos de una Red]]
- [[Enrutador (Router)]]
- [[Tipos de Redes]]
- [[Firewall]]
- [[Protocolo DHCP]]
- [[Cableado Estructurado]]