## **¿Qué es una conexión?**

En el contexto de [[Redes|redes]], una **[[Conexión|conexión]]** es el **[[enlace]] establecido** entre dos o más **[[Dispositivos de una Red|dispositivos]]** que permite el **intercambio de [[Datos]]** entre ellos.

Una [[Conexión|conexión]] implica que ambos extremos (por ejemplo, un [[Cliente|Cliente]] y un [[Servidor]]) han **acordado comunicarse**, siguiendo un **[[Estándares y Protocolos|protocolo]]** específico que define cómo se envían, reciben y confirman los [[Datos]].
#### Existen dos enfoques principales:

- **Orientada a [[Conexión|conexión]]**: Antes de enviar [[Datos]], se establece un **canal formal** entre los [[Dispositivos de una Red|dispositivos]] (como un "saludo" inicial), se garantiza el orden y la entrega de los [[Datos]], y al final se cierra la [[Conexión|conexión]]. El ejemplo más común es **[[TCP]]**, que usa un proceso de **negociación** (conocido como **[[_three-way handshake_]]**) para establecer la [[Conexión|conexión]] antes de transmitir [[Información]].
- **Sin [[Conexión|conexión]]**: Los [[Datos]] se envían directamente, sin establecer un [[enlace]] previo ni garantizar que lleguen o en qué orden. El ejemplo típico es **[[UDP]]**, más rápido pero menos confiable.