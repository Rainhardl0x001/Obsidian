---
tema: "Fundamentos de Redes"
tipo: concepto
creado: 2026-09-24
---
## **¿Qué dispositivos componen una red?**

Una [[Redes|red]] se arma combinando cuatro elementos básicos: **[[Cliente|clientes]]** que piden servicios, **servidores** que los proveen, **dispositivos intermedios** que dirigen el tráfico entre ambos, y **medios** por donde viaja la información.

- Clientes o terminales: Una **aplicación**, **software** o **interfaz** que envía **peticiones** a un **servidor**, para poner a disposición del **usuario** los **servicios** y **datos** que ese servidor proporciona, normalmente a través de una [[Redes|red]].

- Servidores: [[Dispositivos de una Red|Dispositivos]] conectados a la red dedicados a **procesar el flujo de datos**, atendiendo las peticiones de los [[Cliente|clientes]] o terminales.

- Dispositivos intermedios: Se encargan de **interconectar** los distintos segmentos de una red, dirigiendo el **flujo de datos** entre clientes y servidores. Los más comunes:
	- **[[Switch]]**: interconecta dispositivos dentro de una misma red.
	- **[[Enrutador (Router)|Router]]**: interconecta redes distintas entre sí.
	- **[[Dispositivos Inalámbricos (Wireless Devices)|Access Point]]**: da acceso inalámbrico a la red.
	- **[[Módem]]**: adapta la señal para transmitirla por el medio externo (línea telefónica, cable, fibra).

- Medios: **Canal físico o inalámbrico** por el cual viajan los datos dentro de la red:
	- **Cableados**: par trenzado (UTP), fibra óptica.
	- **Inalámbricos**: ondas de radio, Wi-Fi.

Ver [[Medios de Red]] para ventajas y desventajas de cada tipo.

> [!important]- Diferencia clave entre Switch y Router
> Un switch conecta dispositivos **dentro** de una misma red; un router conecta **redes distintas** entre sí. Es un error común confundirlos porque muchos equipos domésticos combinan ambas funciones (ver [[SOHO]]).

> [!important]- Caso especial: P2P
> Normalmente un dispositivo es solo cliente o solo servidor. En una red [[P2P|P2P (Peer to Peer)]], un mismo dispositivo puede ser ambas cosas a la vez: el servidor corre en segundo plano mientras el cliente se usa en primer plano.
#### En resumen
Toda red, sin importar su tamaño, combina estos cuatro elementos: quién pide (cliente), quién responde (servidor), quién dirige el tráfico entre ambos (dispositivos intermedios) y por dónde viaja la información (medios).
## Ver también

- [[Redes]]
- [[Cliente]]
- [[Enrutador (Router)]]
- [[Medios de Red]]
- [[SOHO]]