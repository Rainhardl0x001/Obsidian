---
tema: "Fundamentos de Redes"
tipo: concepto
creado: 2026-09-24
---
## **¿Qué es un cable de consola?**
Un **cable de consola** es el [[Medios de Red|cable físico]] que [[Conexión|conecta]] una [[computadora]] directamente al **[[puerto de consola]]** de un [[Enrutador (Router)|router]] o [[Switch|switch]], permitiendo acceder a su **[[CLI|CLI]]** para configurarlo por primera vez — antes de que el equipo tenga cualquier [[Dirección IP|Dirección IP]] o [[Conexión|conexión]] de [[Redes|red]] funcional.

### Por qué es necesario
Un equipo de [[Redes|red]] **nuevo, sin configurar**, no tiene [[Dirección IP|Dirección IP]] ni acceso remoto habilitado ([[SSH (Secure Shell)]]), por lo que no se le puede acceder a través de la [[Redes|red]]. El cable de consola resuelve exactamente ese problema: Es una **[[Conexión Serial (DCE y DTE)|conexión serial]]** directa, que no depende de ninguna configuración previa del equipo.

### Tipos de cable de consola
- **[[Rollover cable]]**: El tipo clásico, con **[[conectores RJ-45]]** en ambos extremos, pero con los [[pines]] "invertidos" (el pin 1 de un extremo corresponde al pin 8 del otro) — de ahí su nombre. Se conecta al [[puerto RJ-45]] de [[consola]] del equipo y, del otro lado, a un [[adaptador RJ-45-a-USB]] o [[RJ-45-a-DB9]] para [[Conexión|conectarse]] a la [[computadora]].
- **[[USB directo]]**: Equipos más modernos incluyen un **[[puerto de consola USB-a-USB]]**, eliminando la necesidad del [[adaptador]].

> [!important]- El cable de consola no transmite datos de red
> A diferencia de un cable [[Ethernet|Ethernet]], el cable de consola no lleva tráfico de [[Redes|red]] — es exclusivamente para **administración local** del equipo a través de su [[CLI|CLI]]. Por eso su distancia máxima es corta (unos pocos metros) y no tiene relación con la [[Dirección IP|Dirección IP]] ni el [[Direccionamiento|direccionamiento]] del equipo.
### Cómo se usa
Del lado de la [[computadora]], se necesita un **[[programa emulador de terminal]]** (como [[PuTTY]] o [[Tera Term]]) configurado con los parámetros correctos de [[Conexión Serial (DCE y DTE)|comunicación serial]] ([[velocidad en baudios]], [[bits de datos]], [[paridad]]) para poder ver e interactuar con la [[CLI|CLI]] del equipo.

> [!example] Ejemplo
> Al sacar un [[Switch|switch]] nuevo de la caja, un [[técnico]] lo [[Conexión|conecta]] a su [[laptop]] con un cable de consola ([[rollover]] + [[adaptador USB]]), abre [[PuTTY]] configurado a [[9600 baudios]], y desde ahí le asigna su primera [[Dirección IP|Dirección IP]] de administración — algo imposible de hacer todavía por [[Redes|red]], porque el [[Switch|switch]] aún no tiene ninguna configurada.

#### En resumen
El cable de consola es el método de acceso local a la [[CLI|CLI]] de un equipo de [[Redes|red]] antes de que tenga cualquier configuración — típicamente un [[rollover cable con adaptador USB]], usado junto a un [[emulador de terminal]], y sin relación con el [[Redes|tráfico de red]] normal del equipo.

## Ver también
- [[CLI]]
- [[Conexión Serial (DCE y DTE)]]
- [[Enrutador (Router)]]
- [[Switch]]
- [[Ethernet]]