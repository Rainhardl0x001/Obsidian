---
tema: "Fundamentos de Redes"
tipo: concepto
creado: 2026-09-24
---
## **¿Qué son los datos?**

Los **[[Datos|datos]]** son la **unidad mínima de [[Información|información]]** que un [[Dispositivos de una Red|dispositivo]] puede representar, almacenar o transmitir — en el contexto de [[Redes|redes]], generalmente en forma de **[[bits]]** (0 y 1) agrupados según el [[Estándares y Protocolos|protocolo]] que los maneje.
### Cómo viajan los [[Datos|datos]] en la [[Redes|red]]

A medida que los [[Datos|datos]] recorren las capas de un [[Modelos de Red|modelo de red]], van cambiando de nombre según la capa y el [[Estándares y Protocolos|protocolo]] que los procesa — esto es el proceso de **[[encapsulamiento]]**:

> [!tip]- **Datos** → **Segmento** → **Paquete** → **Trama** → **Bits**
> Cada flecha representa una capa del [[Modelo de Red (TCP ∕ IP)|modelo de red TCP/IP]] agregando su propio **[[Modelos de Red|header]]** al [[encapsular]]: la capa de transporte agrega el [[Modelos de Red|header TCP]] o [[Modelos de Red|UDP]] (datos → segmento), la capa de red agrega el [[Modelos de Red|header IP]] (segmento → paquete), y la capa de acceso a la red agrega el [[Modelos de Red|header Ethernet]] (paquete → trama). Al transmitirse por el medio físico, la trama se convierte en **[[bits]]**. Ver [[Modelo de Red (TCP ∕ IP)]] y [[Modelo de Red (OSI)]] para el detalle de cada header.

> [!example] Ejemplo
> Al enviar un mensaje de texto, el [[Datos|dato]] original (el texto) se convierte en segmento al pasar por la capa de transporte, en paquete en la capa de red, y en trama al llegar a la capa de acceso a la red, antes de transmitirse como [[bits]] por el medio físico.

Ver [[Modelo de Red (TCP ∕ IP)]] y [[Modelo de Red (OSI)]] para el detalle de cada capa.

> [!important]- Diferencia clave entre [[Datos|Datos]] e [[Información|Información]]
> Un [[Datos|dato]] es un valor aislado, sin contexto (ej. el número 37). La [[Información|Información]] es el resultado de procesar o [[interpretar]] uno o varios [[Datos|datos]] dentro de un contexto (ej. "37°C es la temperatura actual"). En [[Redes|redes]], los [[Dispositivos de una Red|dispositivos]] transmiten [[Datos|datos]]; son las [[aplicaciones]] y los [[usuarios]] quienes los convierten en [[Información|información]]. Ver [[Información|Información]] para mas detalles.
#### En resumen
Los [[Datos|datos]] son la materia prima que viaja por una [[Redes|red]]; su significado ([[Información|información]]) depende de quién los [[interpreta]] y en qué contexto. Dentro de los modelos de red, el mismo dato cambia de nombre (segmento, paquete, trama, bits) según la capa que lo procesa.

## Ver también

- [[Información]]
- [[Modelos de Red]]
- [[Modelo de Red (TCP ∕ IP)]]
- [[Modelo de Red (OSI)]]
- [[Comunicación de Red]]