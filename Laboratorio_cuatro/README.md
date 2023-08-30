
## 1. [Preguntas reflexivas de ambientación](#)

- ### ¿Como funcionan los servidores DHCP y DNS?

Servidores DHCP:

El DHCP es un protocolo que permite a los dispositivos en una red obtener automáticamente una dirección IP y otra información de configuración de red, como la máscara de subred, la puerta de enlace predeterminada y los servidores DNS. Aquí está cómo funciona:

Solicitud y Oferta:
Cuando un dispositivo se conecta a una red y está configurado para obtener una dirección IP automáticamente, envía una solicitud DHCP a la red. Los servidores DHCP en la red responden con ofertas de direcciones IP disponibles y otros detalles de configuración.

Selección:
El dispositivo selecciona una oferta y envía un mensaje al servidor DHCP para aceptarla. Los otros servidores DHCP en la red son notificados de que esa oferta ya no está disponible.

Asignación:
El servidor DHCP asigna la dirección IP elegida junto con la información de configuración adicional al dispositivo. El dispositivo ahora tiene una dirección IP válida y puede comunicarse en la red.

Renovación:
Las direcciones IP asignadas tienen un tiempo de arrendamiento. Antes de que expire, el dispositivo solicitará una renovación de la dirección IP al mismo servidor DHCP para extender el tiempo de uso. Si el servidor DHCP está disponible, renueva la dirección IP.

Servidores DNS:

El DNS es el sistema que convierte los nombres de dominio, como "www.ejemplo.com", en direcciones IP, que son necesarias para que las computadoras se comuniquen entre sí. Aquí está cómo funciona:

Resolución de nombres:
Cuando escribes un nombre de dominio en el navegador (por ejemplo, www.ejemplo.com), tu dispositivo envía una consulta DNS para resolver el nombre a una dirección IP.

Búsqueda en caché local:
Primero, tu dispositivo verifica su propia caché local de DNS para ver si ya ha resuelto esa dirección IP recientemente. Si es así, utiliza la dirección IP almacenada.

Consulta a servidores DNS:
Si la dirección IP no se encuentra en la caché, tu dispositivo envía la consulta a un servidor DNS local o proporcionado por tu proveedor de servicios de Internet.

Recorrido DNS:
Si el servidor DNS local no tiene la respuesta, realiza una serie de consultas en cascada hacia servidores DNS superiores, como los servidores raíz y los servidores de nombres de dominio de nivel superior.

Respuesta DNS:
Uno de los servidores DNS en el recorrido proporciona la dirección IP correspondiente al nombre de dominio. El servidor local almacena esta respuesta en su caché para futuras consultas y devuelve la dirección IP al dispositivo que realizó la consulta original.

- ### ¿Como funcionan los servidores DHCP y DNS?

Las rutas estáticas y dinámicas son dos enfoques diferentes para el enrutamiento de tráfico en una red. Cada enfoque tiene sus ventajas y desventajas. Aquí están las desventajas comunes de las rutas estáticas en comparación con las rutas dinámicas:


### Desventajas de las Rutas Estáticas:

No se Adaptan: Las rutas estáticas no se ajustan automáticamente a cambios en la red, lo que puede causar problemas si la red cambia.

Complejidad: Gestionar rutas estáticas en redes grandes es complicado y puede llevar a errores.

Escalabilidad Limitada: Las rutas estáticas no funcionan bien en redes grandes con muchos destinos.

Fallas de Redundancia: No manejan automáticamente rutas de respaldo en caso de fallas.

No Optimizan: No eligen automáticamente las rutas más eficientes según el rendimiento de la red.

Configuración Lenta: Configurar rutas estáticas en cada enrutador lleva tiempo.

En resumen, las rutas dinámicas tienen ventajas como adaptabilidad, escalabilidad y optimización automática, lo que las hace preferibles en muchas redes.

### ¿Cual es el algoritmo y la métrica que implementa RIP?.

RIP (Routing Information Protocol) implementa el algoritmo de enrutamiento de vector de distancia. El algoritmo de vector de distancia es un enfoque de enrutamiento que se basa en el intercambio de información entre enrutadores vecinos para determinar las rutas a las diferentes redes en la red.

La métrica que utiliza RIP para determinar la mejor ruta hacia una red se basa en el conteo de saltos (hops). Cada salto representa un enrutador intermedio que debe atravesarse para llegar a la red de destino. RIP tiene una métrica máxima de 15 saltos. Si una ruta supera esta métrica, se considera inalcanzable. Esto significa que RIP favorece rutas con menos saltos, pero no considera otras métricas de rendimiento, como la velocidad de enlace o la congestión.

### ¿Que diferencias hay entre las versiones 1 y 2 de RIP?. (Ventajas y Desventajas)

Las versiones 1 y 2 de RIP (Routing Information Protocol) son protocolos de enrutamiento ampliamente utilizados, pero con diferencias clave en términos de funcionalidad y características. Aquí hay un resumen de las diferencias, ventajas y desventajas entre RIP versión 1 y versión 2:

#### RIP Versión 1:

Ventajas:

Simplicidad: RIP v1 es muy simple y fácil de configurar. Es adecuado para redes pequeñas y menos complejas.
Amplia Compatibilidad: Muchos dispositivos y sistemas operativos todavía admiten RIP v1, lo que lo hace utilizable en una variedad de entornos.
Baja Carga de Tráfico: RIP v1 genera menos tráfico de red en comparación con algunas otras soluciones de enrutamiento debido a sus actualizaciones de enrutamiento menos frecuentes.

Desventajas:

Métrica Limitada: Solo utiliza la métrica basada en saltos (hops) para determinar rutas, lo que puede resultar en rutas subóptimas en redes más grandes y complejas.
Falta de Autenticación: RIP v1 carece de autenticación, lo que lo hace vulnerable a ataques de envenenamiento de ruta.

#### RIP Versión 2:

Ventajas:

Soporte para Subredes: RIP v2 puede anunciar rutas a subredes, lo que lo hace más adecuado para redes modernas con direcciones IP más eficientes.
Autenticación: RIP v2 admite autenticación, lo que mejora la seguridad y reduce el riesgo de envenenamiento de ruta.
Métricas Más Flexibles: Aunque sigue utilizando saltos como métrica principal, RIP v2 puede incluir información adicional en las actualizaciones de enrutamiento.
Desventajas:

Mayor Carga de Tráfico: RIP v2 genera más tráfico de red debido a actualizaciones más frecuentes y a la necesidad de anunciar información adicional de subredes.
Configuración Más Compleja: Aunque todavía es más simple que otros protocolos, RIP v2 puede requerir configuraciones adicionales para aprovechar sus características.


### ¿Que diferencias hay entre una IP estática, una IP dinámica y una IP reservada?.

Las diferencias entre una IP estática, una IP dinámica y una IP reservada se relacionan con cómo se asignan y administran las direcciones IP en una red. Aquí está un resumen de estas diferencias:

#### IP Estática:

Asignación: Una dirección IP estática se asigna manualmente a un dispositivo de forma permanente. No cambia a menos que se modifique manualmente.

Uso: Las direcciones IP estáticas son comunes en servidores, impresoras de red, enrutadores y otros dispositivos que necesitan tener una dirección IP fija para ser fácilmente accesibles.

Ventajas: Garantiza que el dispositivo siempre tenga la misma dirección IP, lo que facilita su identificación y acceso. Útil para servicios que requieren conectividad constante.

Desventajas: Puede ser laborioso administrar y configurar manualmente las direcciones IP en una red grande. Menos flexible para cambios en la topología de la red.


#### IP Dinámica:

Asignación: Una dirección IP dinámica se asigna automáticamente a un dispositivo desde un grupo de direcciones disponibles en un rango definido por un servidor DHCP.

Uso: Es común en dispositivos cliente como computadoras, teléfonos y tabletas en redes locales y en Internet.

Ventajas: Simplifica la administración, ya que las direcciones IP se asignan automáticamente. Ayuda a conservar direcciones IP al liberarlas cuando no están en uso.

Desventajas: Las direcciones IP pueden cambiar con el tiempo, lo que dificulta el acceso predecible a dispositivos. No es ideal para servicios que necesitan una dirección IP constante.


#### IP Reservada:

Asignación: Las direcciones IP reservadas son direcciones IP en un rango específico que están reservadas para un propósito particular, como servidores DHCP, enrutadores o dispositivos críticos.

Uso: Se utilizan para asegurar que ciertos dispositivos siempre tengan direcciones IP disponibles y fijas.

Ventajas: Proporciona direcciones IP consistentes para dispositivos específicos, incluso cuando se utiliza DHCP. Evita conflictos y asegura la disponibilidad de direcciones IP.

Desventajas: Si se reserva un número excesivo de direcciones IP, puede agotar el rango disponible para otros dispositivos.

