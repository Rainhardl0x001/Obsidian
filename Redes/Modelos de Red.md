## **¿Qué son los modelos de red?**

Un **[[Modelos de Red|modelo de red]]** es una **representación conceptual, organizada por capas**, que describe cómo debe ocurrir la **comunicación de [[Datos|datos]]** entre [[Dispositivos de una Red|dispositivos]] dentro de una [[Redes|red]], dividiendo ese proceso complejo en **partes más pequeñas y manejables**, donde cada capa cumple una función específica y se apoya en la capa anterior/siguiente. Su propósito principal es servir como una **guía o referencia estandarizada** para que:

- Los **fabricantes** sepan cómo diseñar [[Dispositivos de una Red|dispositivos]] y [[Estándares y Protocolos|protocolos]] que funcionen correctamente con los de otros fabricantes.
- Los **[[desarrolladores]]** puedan crear [[software]] de [[Redes|red]] sin necesidad de entender cómo funciona cada capa por debajo de la suya.
- Se facilite el **diagnóstico de problemas**, ya que se puede aislar en qué capa específica está ocurriendo una falla.
- Se pueda **enseñar y entender** la [[Comunicación de Red|comunicación de red]] de forma progresiva, capa por capa.

Los dos [[Modelos de Red|modelos]] más importantes en [[Redes|redes]] son:

- **[[Modelo de Red (OSI)|Modelo OSI]] (7 capas)**: un modelo **teórico y de referencia**, creado por la [[ISO|ISO]], que describe de forma muy detallada cada función de la comunicación (física, enlace de datos, red, transporte, sesión, presentación, aplicación).
- **[[Modelo de Red (TCP ∕ IP)|Modelo TCP/IP]] (4 capas)**: el modelo **práctico**, que realmente se usa en [[Internet|Internet]], más compacto que [[Modelo de Red (OSI)|OSI]], pero basado en los mismos principios.


<div style="display: flex; flex-direction: column; align-items: center; margin: 25px 0; font-family: sans-serif; font-size: 14px;">
  <div style="display: grid; grid-template-columns: 1fr 1fr; gap: 4px; align-items: stretch; width: 100%; max-width: 580px;">
    
    <!-- TCP/IP: Aplicación (Abarca capas 7, 6 y 5) -->
    <div style="grid-column: 1; grid-row: 1 / span 3; justify-self: end; width: 200px; background-color: #b894e6; color: #11111b; font-weight: bold; border-radius: 8px; display: flex; align-items: center; justify-content: center; box-shadow: 0 2px 5px rgba(0,0,0,0.2);">
      Aplicación
    </div>

    <!-- OSI: Aplicación -->
    <div style="grid-column: 2; grid-row: 1; justify-self: start; width: 130px; height: 38px; background-color: #cba6f7; color: #11111b; font-weight: bold; border-radius: 8px; display: flex; align-items: center; justify-content: center; box-shadow: 0 2px 5px rgba(0,0,0,0.2);">
      Aplicación
    </div>

    <!-- OSI: Presentación -->
    <div style="grid-column: 2; grid-row: 2; justify-self: start; width: 155px; height: 38px; background-color: #b894e6; color: #11111b; font-weight: bold; border-radius: 8px; display: flex; align-items: center; justify-content: center; box-shadow: 0 2px 5px rgba(0,0,0,0.2);">
      Presentación
    </div>

    <!-- OSI: Sesión -->
    <div style="grid-column: 2; grid-row: 3; justify-self: start; width: 180px; height: 38px; background-color: #a582d5; color: #11111b; font-weight: bold; border-radius: 8px; display: flex; align-items: center; justify-content: center; box-shadow: 0 2px 5px rgba(0,0,0,0.2);">
      Sesión
    </div>

    <!-- TCP/IP: Transporte -->
    <div style="grid-column: 1; grid-row: 4; justify-self: end; width: 225px; height: 38px; background-color: #9270c4; color: #ffffff; font-weight: bold; border-radius: 8px; display: flex; align-items: center; justify-content: center; box-shadow: 0 2px 5px rgba(0,0,0,0.2);">
      Transporte
    </div>

    <!-- OSI: Transporte -->
    <div style="grid-column: 2; grid-row: 4; justify-self: start; width: 205px; height: 38px; background-color: #9270c4; color: #ffffff; font-weight: bold; border-radius: 8px; display: flex; align-items: center; justify-content: center; box-shadow: 0 2px 5px rgba(0,0,0,0.2);">
      Transporte
    </div>

    <!-- TCP/IP: Red -->
    <div style="grid-column: 1; grid-row: 5; justify-self: end; width: 250px; height: 38px; background-color: #7f5fb3; color: #ffffff; font-weight: bold; border-radius: 8px; display: flex; align-items: center; justify-content: center; box-shadow: 0 2px 5px rgba(0,0,0,0.2);">
      Red
    </div>

    <!-- OSI: Red -->
    <div style="grid-column: 2; grid-row: 5; justify-self: start; width: 230px; height: 38px; background-color: #7f5fb3; color: #ffffff; font-weight: bold; border-radius: 8px; display: flex; align-items: center; justify-content: center; box-shadow: 0 2px 5px rgba(0,0,0,0.2);">
      Red
    </div>

    <!-- TCP/IP: Acceso a la red (Abarca capas 2 y 1) -->
    <div style="grid-column: 1; grid-row: 6 / span 2; justify-self: end; width: 280px; background-color: #6c4da2; color: #ffffff; font-weight: bold; border-radius: 8px; display: flex; align-items: center; justify-content: center; box-shadow: 0 2px 5px rgba(0,0,0,0.2);">
      Acceso a la red
    </div>

    <!-- OSI: Enlace de datos -->
    <div style="grid-column: 2; grid-row: 6; justify-self: start; width: 255px; height: 38px; background-color: #6c4da2; color: #ffffff; font-weight: bold; border-radius: 8px; display: flex; align-items: center; justify-content: center; box-shadow: 0 2px 5px rgba(0,0,0,0.2);">
      Enlace de datos
    </div>

    <!-- OSI: Física -->
    <div style="grid-column: 2; grid-row: 7; justify-self: start; width: 280px; height: 38px; background-color: #593b91; color: #ffffff; font-weight: bold; border-radius: 8px; display: flex; align-items: center; justify-content: center; box-shadow: 0 2px 5px rgba(0,0,0,0.2);">
      Física
    </div>

    <!-- Etiqueta TCP/IP -->
    <div style="grid-column: 1; grid-row: 8; text-align: center; font-weight: bold; color: #cba6f7; margin-top: 12px; font-size: 15px;">
      modelo TCP/IP
    </div>

    <!-- Etiqueta OSI -->
    <div style="grid-column: 2; grid-row: 8; text-align: center; font-weight: bold; color: #cba6f7; margin-top: 12px; font-size: 15px;">
      modelo OSI
    </div>

  </div>
</div>
![[Pasted image 20260923222559.png]]

**En resumen**: Un [[Modelos de Red|modelo]] no es un [[Estándares y Protocolos|protocolo]] ni un [[Dispositivos de una Red|dispositivo]] — es un **mapa conceptual** que organiza y explica cómo debe estructurarse la [[Comunicación de Red|comunicación en una red]], dividiéndola en capas con responsabilidades claras, y sirviendo como base para que los [[Estándares y Protocolos|protocolos]] y [[Dispositivos de una Red|dispositivos]] reales (como [[Modelo de Red (TCP ∕ IP)|TCP/IP]], [[Ethernet]], [[Enrutador (Router)|routers]]) se diseñen de forma compatible entre sí.

### ¿Qué es un encabezado (Header)?

Un **[[Modelos de Red|encabezado]]** (o _header_) es un bloque de [[Información|información]] de control que una capa añade al principio de los [[Datos|datos]] durante el proceso de **[[encapsulamiento]]**.

A medida que la [[Información|información]] desciende por las capas del [[Modelos de Red|modelo de red]], cada capa le coloca su propio "**sobre**" o **etiqueta** con las **instrucciones necesarias** para que la misma capa en el [[Dispositivos de una Red|dispositivo]] de destino sepa cómo [[interpretar]], [[procesar]] y [[reenviar]] esos datos.