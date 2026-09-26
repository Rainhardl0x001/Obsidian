El **[[Modelo de Red (OSI)|modelo OSI]]** (_Open Systems Interconnection_) es un [[Modelos de Red|modelo]] **teórico y de referencia**, creado por la **[[ISO|ISO]]**, que describe de forma detallada cómo debería ocurrir la comunicación de [[Datos|datos]] entre [[Dispositivos de una Red|dispositivos]] dentro de una [[Redes|red]], dividiéndola en **siete capas**, cada una con una función específica y bien delimitada. A diferencia de [[Modelo de Red (TCP ∕ IP)|TCP/IP]], ningún [[Estándares y Protocolos|protocolo]] real sigue el [[Modelo de Red (OSI)|Modelo OSI]] al pie de la letra, su valor está en servir de **referencia conceptual** para enseñar y entender la [[Comunicación de Red|comunicación de red]] con mayor granularidad.

<table style="margin: 0 auto; border-collapse: collapse;">
  <thead>
    <tr>
      <th style="text-align: center; padding: 8px 16px;">Nivel</th>
      <th style="text-align: left; padding: 8px 16px;">Capa</th>
      <th style="text-align: left; padding: 8px 16px;">Encapsulamiento (PDU)</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td style="text-align: center; padding: 8px 16px;"><b>7</b></td>
      <td style="padding: 8px 16px;"><span style="color: #cba6f7; font-weight: bold;">Aplicación</span></td>
      <td style="padding: 8px 16px;"><span style="background-color: #cba6f7; color: #11111b; padding: 2px 8px; border-radius: 4px; font-weight: bold;">Datos</span></td>
    </tr>
    <tr>
      <td style="text-align: center; padding: 8px 16px;"><b>6</b></td>
      <td style="padding: 8px 16px;"><span style="color: #cba6f7; font-weight: bold;">Presentación</span></td>
      <td style="padding: 8px 16px;"><span style="background-color: #cba6f7; color: #11111b; padding: 2px 8px; border-radius: 4px; font-weight: bold;">Datos</span></td>
    </tr>
    <tr>
      <td style="text-align: center; padding: 8px 16px;"><b>5</b></td>
      <td style="padding: 8px 16px;"><span style="color: #cba6f7; font-weight: bold;">Sesión</span></td>
      <td style="padding: 8px 16px;"><span style="background-color: #cba6f7; color: #11111b; padding: 2px 8px; border-radius: 4px; font-weight: bold;">Datos</span></td>
    </tr>
    <tr>
      <td style="text-align: center; padding: 8px 16px;"><b>4</b></td>
      <td style="padding: 8px 16px;"><span style="color: #cba6f7; font-weight: bold;">Transporte</span></td>
      <td style="padding: 8px 16px;"><span style="background-color: #9270c4; color: #ffffff; padding: 2px 8px; border-radius: 4px;">Segmento</span> <span style="background-color: #cba6f7; color: #11111b; padding: 2px 8px; border-radius: 4px; font-weight: bold;">Datos</span></td>
    </tr>
    <tr>
      <td style="text-align: center; padding: 8px 16px;"><b>3</b></td>
      <td style="padding: 8px 16px;"><span style="color: #cba6f7; font-weight: bold;">Red</span></td>
      <td style="padding: 8px 16px;"><span style="background-color: #7f5fb3; color: #ffffff; padding: 2px 8px; border-radius: 4px;">Paquete</span> <span style="background-color: #9270c4; color: #ffffff; padding: 2px 8px; border-radius: 4px;">Segmento</span> <span style="background-color: #cba6f7; color: #11111b; padding: 2px 8px; border-radius: 4px; font-weight: bold;">Datos</span></td>
    </tr>
    <tr>
      <td style="text-align: center; padding: 8px 16px;"><b>2</b></td>
      <td style="padding: 8px 16px;"><span style="color: #cba6f7; font-weight: bold;">Enlace de datos</span></td>
      <td style="padding: 8px 16px;"><span style="background-color: #6c4da2; color: #ffffff; padding: 2px 8px; border-radius: 4px;">Trama</span> <span style="background-color: #7f5fb3; color: #ffffff; padding: 2px 8px; border-radius: 4px;">Paquete</span> <span style="background-color: #9270c4; color: #ffffff; padding: 2px 8px; border-radius: 4px;">Segmento</span> <span style="background-color: #cba6f7; color: #11111b; padding: 2px 8px; border-radius: 4px; font-weight: bold;">Datos</span> <span style="background-color: #6c4da2; color: #ffffff; padding: 2px 8px; border-radius: 4px;">Trama</span></td>
    </tr>
    <tr>
      <td style="text-align: center; padding: 8px 16px;"><b>1</b></td>
      <td style="padding: 8px 16px;"><span style="color: #cba6f7; font-weight: bold;">Física</span></td>
      <td style="padding: 8px 16px;"><span style="background-color: #593b91; color: #ffffff; padding: 2px 8px; border-radius: 4px; letter-spacing: 1px;">010101 Bits 101010</span></td>
    </tr>
  </tbody>
</table>

**Las siete capas, de arriba hacia abajo:**

**7. Aplicación**: es la capa donde interactúan directamente los **[[Programa|programas]] y el [[Usuario|usuario]]**. Aquí operan protocolos como **[[Protocolo HTTP ∕ HTTPS|HTTP]]**, **[[Protocolo FTP|FTP]]**, **[[Protocolo SMTP|SMTP]]** y **[[Protocolo DNS|DNS]]**.
- No tiene un [[Modelos de Red|encabezado]] "de [[Redes|red]]" estandarizado; el formato del mensaje lo define el propio [[Estándares y Protocolos|protocolo]] de aplicación (por ejemplo, la estructura de una petición [[Protocolo HTTP ∕ HTTPS|HTTP]]).

**6. Presentación**: se encarga de **traducir, [[cifrar]] y [[comprimir]]** los [[Datos|datos]], para que la [[Información|información]] sea entendible entre distintos [[Sistemas|sistemas]] (por ejemplo, convirtiendo formatos de texto, imágenes o cifrando la información con **[[Protocolo TLS|TLS]]**).
- Tampoco tiene un [[Modelos de Red|encabezado]] fijo; depende del mecanismo de cifrado/compresión usado.

**5. Sesión**: se encarga de **establecer, mantener y finalizar** la sesión de comunicación entre dos [[Dispositivos de una Red|dispositivos]], coordinando cuándo empieza y termina el intercambio de [[Datos|datos]].
- Igual que las dos anteriores, no tiene un [[Modelos de Red|encabezado]] estandarizado propio.

**4. Transporte**: se encarga de **cómo viajan los [[Datos|datos]]** entre origen y destino, garantizando (o no) la entrega. La unidad de [[Datos|datos]] aquí se llama **segmento** ([[Protocolo TCP|TCP]]) o **datagrama** ([[Protocolo UDP|UDP]]).
- **[[Protocolo TCP|TCP]]**: su [[Modelos de Red|encabezado]] incluye **puerto origen y destino**, **[[número de secuencia]]**, **[[número de confirmación (ACK)]]** y **[[flags de control]]** ([[SYN]], [[ACK]], [[FIN]], usados en el _[[handshake]]_).
- **[[Protocolo UDP|UDP]]**: su [[Modelos de Red|encabezado]] es más simple — **[[puerto origen]], [[puerto destino]], [[longitud]]** y **[[checksum]]**.

**3. Red**: se encarga del **[[Direccionamiento]] y [[enrutamiento]]** de los [[Datos|datos]] entre [[Redes|redes]] distintas. La unidad de datos se llama **paquete**.
- [[Modelos de Red|Encabezado]] **[[Protocolo IP|IP]]**: incluye la **[[Dirección IP]] de origen**, la **[[Dirección IP]] de destino**, el **[[TTL]]** (_Time To Live_) y el **[[Estándares y Protocolos|protocolo]]** que se transporta ([[Protocolo TCP|TCP]] o [[Protocolo UDP|UDP]]).

**2. Enlace de [[Datos|datos]]**: se encarga de organizar los [[Datos|datos]] en **tramas**, usando **[[direcciones físicas (MAC)]]** para identificar [[Dispositivos de una Red|dispositivos]] dentro de una misma [[Redes|red]] local. Aquí operan estándares como **[[Ethernet]]** y **[[Wi-Fi]] (802.11)**. La unidad de datos se llama **trama (frame)**.
- [[Modelos de Red|Encabezado]]: incluye la **[[Dirección MAC]] de origen**, la **[[Dirección MAC]] de destino** y el **tipo de [[Estándares y Protocolos|protocolo]]** [[encapsulado]].

**1. Física**: se encarga de la **transmisión real** de los **[[bits]]** a través del medio físico (cables, ondas de radio), ocupándose de voltajes, señales, frecuencias y conectores.
- No maneja [[Modelos de Red|encabezados]] ni direcciones — solo se ocupa de la señal eléctrica/óptica/de radio en sí.

**En resumen**: El [[Modelo de Red (OSI)|Modelo OSI]] separa en siete pasos claros lo que [[Modelo de Red (TCP ∕ IP)|TCP/IP]] resume en cuatro (o cinco). Las capas inferiores (Física, Enlace, Red, Transporte) tienen [[Modelos de Red|encabezados]] bien definidos que se van agregando en el **[[encapsulamiento]]**, mientras que las capas superiores (Sesión, Presentación, Aplicación) dependen más del [[Estándares y Protocolos|protocolo]] específico que se use en cada caso. Es especialmente útil para **diagnosticar problemas de [[Redes|red]]** (se puede aislar en qué capa específica ocurre una falla) y para **entender conceptualmente** cada función por separado, aunque en la práctica los [[Estándares y Protocolos|protocolos]] reales de [[Internet|Internet]] se basen en el modelo [[Modelo de Red (TCP ∕ IP)|TCP/IP]].
