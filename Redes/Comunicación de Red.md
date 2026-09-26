---
tema: "Fundamentos de Redes"
tipo: concepto
creado: 2026-09-24
---
## **¿Qué es una comunicación de red?**

Es el **proceso** mediante el cual dos o más **[[Dispositivos de una Red|dispositivos]]** intercambian **[[Datos]]** a través de una [[Redes|red]], siguiendo reglas y [[Estándares y Protocolos|protocolos]] que garantizan que la [[Información]] se transmita de forma correcta y ordenada. Este proceso se puede clasificar según varios criterios.

### Modos de comunicación (dirección del flujo de [[Datos]])

- **[[Simplex]]**: La comunicación es en **un solo sentido**, el [[emisor]] siempre envía y el [[receptor]] siempre recibe, sin poder invertir los roles (ejemplo: una [[radio]] o un [[teclado]]).
- **[[Half-duplex]]**: Ambos [[Dispositivos de una Red|dispositivos]] pueden **enviar y recibir**, pero no al mismo tiempo, deben turnarse (ejemplo: un walkie-talkie).
- **[[Full-duplex]]**: Ambos [[Dispositivos de una Red|dispositivos]] pueden **enviar y recibir simultáneamente** (ejemplo: una llamada telefónica).

### Tipos de transmisión (a cuántos destinos se envían los [[Datos]])

- **[[Unicast]]**: Los [[Datos]] se envían de **un [[emisor]] a un solo [[receptor]]** específico.
- **[[Broadcast]]**: Los [[Datos]] se envían de **un [[emisor]] a todos los [[Dispositivos de una Red|dispositivos]]** de la [[Redes|red]].
- **[[Multicast]]**: Los [[Datos]] se envían de **un [[emisor]] a un grupo específico** de [[receptores]], no a todos.

### Serial vs Paralela (cuántos bits viajan a la vez)

- **Transmisión serial**: los [[Bit|bits]] viajan **uno detrás de otro**, en secuencia, a través de un solo canal — ver [[Conexión Serial (DCE y DTE)]] para el detalle de este método aplicado a la configuración de equipos.
- **Transmisión paralela**: **varios bits viajan simultáneamente**, cada uno por su propio canal o hilo dentro del mismo cable.

> [!important]- Por qué lo serial ganó, contra la intuición
> Parecería que enviar varios bits a la vez (paralela) siempre sería más rápido que enviarlos uno por uno (serial). Pero a altas velocidades, mantener todos los canales paralelos perfectamente sincronizados entre sí (evitar el *clock skew*, donde un bit llega microsegundos antes que otro) se vuelve muy difícil y limita qué tan rápido se puede transmitir. Por eso casi todas las interfaces modernas de alta velocidad —Ethernet, USB, SATA— son seriales: un solo canal bien optimizado terminó superando a varios canales paralelos mal sincronizados.

### Síncrona vs Asíncrona (cómo se coordina el ritmo del envío)

- **Transmisión síncrona**: emisor y receptor comparten una **señal de reloj común**, que marca exactamente cuándo empieza y termina cada bit. Los datos viajan en un flujo continuo, sin pausas entre caracteres.
- **Transmisión asíncrona**: no hay reloj compartido — cada bloque de datos (típicamente un carácter) viaja acompañado de sus propios **bits de inicio y parada**, que le indican al receptor dónde empieza y termina cada unidad, de forma independiente.

> [!important]- El trade-off entre ambas
> La transmisión síncrona es más eficiente (sin bits extra de inicio/parada en cada carácter), pero requiere que ambos extremos mantengan la sincronización de reloj constantemente. La asíncrona es más simple y tolerante a pequeñas variaciones de tiempo entre dispositivos, a costa de un poco de sobrecarga (*overhead*) en cada unidad enviada — es el método que usaban los puertos seriales clásicos (UART) para conectar módems y periféricos.

### Banda base vs Banda ancha (cómo se usa el ancho de banda del medio)

- **Banda base (*baseband*)**: el medio transmite **una sola señal digital a la vez**, usando **todo** el ancho de banda disponible para ese único canal. Es el método que usa [[Ethernet]] sobre [[Par Trenzado (UTP)]].
- **Banda ancha (*broadband*)**: el ancho de banda del medio se **divide en múltiples canales o frecuencias** mediante modulación, permitiendo transmitir **varias señales distintas simultáneamente** sobre el mismo cable.

> [!important]- Por qué tu Internet por cable se llama "banda ancha"
> Un [[Cable Coaxial|cable coaxial]] de TV por cable transporta al mismo tiempo decenas de canales de televisión **y** tu conexión a Internet — todo sobre el mismo cable físico, porque cada servicio ocupa una franja de frecuencia distinta (banda ancha). Ethernet, en cambio, no comparte su cable con nada más: toda la capacidad del cable UTP se dedica a una sola señal digital de datos (banda base).

> [!example] Ejemplo
> Cuando tu router recibe Internet por [[Tipos de Conexión a Internet|cable]], esa conexión llega en banda ancha (compartiendo el cable con señales de TV). Pero una vez que tu router distribuye esos datos a tus dispositivos por Ethernet dentro de tu casa, esa parte del trayecto ya es banda base — un solo canal digital dedicado exclusivamente a datos.

#### En resumen
La comunicación de red se puede clasificar según varios criterios independientes entre sí: la dirección del flujo (simplex, half-duplex, full-duplex), a cuántos destinos llega (unicast, broadcast, multicast), cuántos bits viajan a la vez (serial vs paralela), cómo se coordina el tiempo de envío (síncrona vs asíncrona), y cómo se aprovecha el ancho de banda del medio (banda base vs banda ancha). Un mismo enlace real suele combinar una opción de cada categoría.

## Ver también

- [[Simplex]]
- [[Half-duplex]]
- [[Full-duplex]]
- [[Unicast]]
- [[Broadcast]]
- [[Multicast]]
- [[Conexión Serial (DCE y DTE)]]
- [[Ethernet]]
- [[Tipos de Conexión a Internet]]