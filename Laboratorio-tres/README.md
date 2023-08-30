# Práctica de Laboratorio 03

## 1. [Preguntas reflexivas de ambientación](#)

- ### ¿Que es y como se configura la ruta por defecto?

    La "ruta por defecto" se refiere a la dirección de red que un dispositivo o sistema operativo utiliza para enviar paquetes de datos a destinos fuera de su propia red local. Cuando un dispositivo, como una computadora, necesita enviar datos a otra ubicación en Internet o en una red externa, utiliza la ruta por defecto para encaminar esos paquetes correctamente.

    Configurar la ruta por defecto implica definir la dirección IP del router o puerta de enlace que actúa como punto de acceso a otras redes. Esto permite que los paquetes de datos enviados desde el dispositivo se dirijan al router, que luego se encargará de reenviarlos hacia sus destinos finales.

    <b>pasos para su configuración:</b>

    <ol>
        <li>
            <b>Identificar la dirección IP del router:</b>
            En primer lugar, necesitas conocer la dirección IP del router o puerta de enlace de tu red. Esta dirección IP será la que utilices como ruta por defecto.
        </li>  
        <br>
        <li>
            <b>Acceder a la configuración de red:</b>
            En tu dispositivo, accede a la configuración de red. Esto puede hacerse a través del Panel de Control en Windows, las Preferencias del Sistema en macOS o la configuración de red en distribuciones de Linux.
        </li>  
        <li>
            <b>Añadir la ruta por defecto:</b>
            Dentro de la configuración de red, busca la opción de "Configuración de red" o "Configuración de TCP/IP" según tu sistema operativo. Allí deberías encontrar un campo para introducir la "Puerta de enlace" o "Ruta por defecto". Ingresa la dirección IP del router en este campo.
        </li>
        <li>
            <b>Guardar y aplicar cambios:</b>
            Después de ingresar la dirección IP del router como ruta por defecto, guarda los cambios en la configuración de red. En algunos casos, es posible que debas reiniciar tu dispositivo para que los cambios surtan efecto.
        </li>                            
    </ol>

- ### ¿Que es y como se configura la ruta por defecto?
    La "distancia administrativa" es un concepto utilizado en enrutamiento de redes, particularmente en protocolos de enrutamiento dinámico, para determinar la confiabilidad o preferencia de una ruta en comparación con otras posibles rutas hacia una misma red de destino. En otras palabras, es un valor numérico que indica cuánto confía un router en la información proporcionada por un protocolo de enrutamiento específico al elegir una ruta para enviar paquetes de datos.

    Cada protocolo de enrutamiento tiene su propia distancia administrativa predeterminada para evaluar la confiabilidad de las rutas que presenta. En general, cuanto menor sea el valor de distancia administrativa, más confiable se considerará la ruta.

- ### ¿Que es una red directamente conectada y cual es su distancia administrativa?


    Una "red directamente conectada" se refiere a una red a la cual un dispositivo está conectado físicamente, sin la necesidad de usar ningún enlace de red adicional, como routers o switches. En otras palabras, es una red a la que un dispositivo puede acceder directamente a través de su interfaz de red sin ningún intermediario.

    Por ejemplo, si tienes una computadora conectada a un router a través de un cable Ethernet, la red local a la que pertenece esa computadora sería una red directamente conectada para ella. Del mismo modo, si un router está conectado directamente a otro router mediante un enlace dedicado, las redes de ambos routers son consideradas redes directamente conectadas entre sí.

    En resumen, una red directamente conectada es una red a la que un dispositivo tiene acceso sin usar dispositivos de enrutamiento adicionales, y su distancia administrativa es 0, lo que la convierte en la ruta más confiable y preferida para el dispositivo.

- ### ¿Que es una ruta estática?


    Una <b>ruta estática</b> a es una entrada en la tabla de enrutamiento de un dispositivo de red que ha sido configurada manualmente por un administrador de red en lugar de ser aprendida automáticamente a través de protocolos de enrutamiento dinámico. En otras palabras, en lugar de depender de que los routers intercambien información para descubrir automáticamente cómo alcanzar diferentes redes, una ruta estática se establece de manera específica y estática en cada dispositivo.

    A diferencia de las rutas dinámicas, que son aprendidas automáticamente por los dispositivos a través de protocolos de enrutamiento, las rutas estáticas deben ser ingresadas manualmente en la tabla de enrutamiento de un dispositivo. Esto se hace indicando la dirección de la red de destino y la dirección IP del siguiente salto (generalmente el siguiente router en la ruta).

    En resumen, una ruta estática es una ruta de enrutamiento configurada manualmente por un administrador de red para dirigir el tráfico hacia una red de destino específica a través de un camino determinado.


- ### ¿Que es una ruta dinámica?


    Una "ruta dinámica" es una entrada de enrutamiento en un dispositivo de red, como un router, que se aprende automáticamente a través de protocolos de enrutamiento dinámico. A diferencia de las rutas estáticas, donde los administradores de red configuran manualmente las rutas, las rutas dinámicas se establecen de manera automática y se adaptan a los cambios en la topología de la red.

    Algunos ejemplos de protocolos de enrutamiento dinámico incluyen OSPF (Open Shortest Path First), RIP (Routing Information Protocol), EIGRP (Enhanced Interior Gateway Routing Protocol) y BGP (Border Gateway Protocol). Estos protocolos utilizan algoritmos y métricas para calcular las mejores rutas y determinar cuál es la ruta más eficiente para llegar a una red de destino específica.

    En resumen, una ruta dinámica es una ruta de enrutamiento aprendida automáticamente a través de protocolos de enrutamiento dinámico, que permiten a los routers adaptarse a cambios en la red y descubrir las mejores rutas para el tráfico.


## 2. [Configuración básica MikroTik-01 ✔](#)

## Acceder al dispositivo por el puerto 8291 via Winbox:

Asegúrarse de estar conectado a la misma red que el dispositivo MikroTik. Luego, ejecutamos estos pasos:

a. Abre el programa Winbox que has instalado.

b. En el campo "Connect To", ingresa la dirección IP del dispositivo MikroTik o su dirección MAC (puedes encontrar la dirección MAC en la parte posterior del dispositivo o en su documentación).

c. Haz clic en el botón "Connect".

#### Iniciar sesión en Winbox:
Aparecerá una ventana emergente de inicio de sesión. Ingresamos el nombre de usuario y la contraseña que configuramos para el dispositivo MikroTik, en este caso no le asiganmos usuario ni contraseña.

#### Accedemos al dispositivo:
Después de iniciar sesión, tenemos acceso a la interfaz del dispositivo MikroTik a través de Winbox. Aquí realizamos configuraciones y administramos las diversas funciones del enrutador.

#### Uso del puerto 8291:
Por defecto, Winbox utiliza el puerto 8291 para la conexión segura a los dispositivos MikroTik. No es necesario especificar el número de puerto en la interfaz de inicio de sesión de Winbox, ya que está preconfigurado para utilizar el puerto 8291 de manera predeterminada.


## 2. [Configuración básica MikroTik-01 ✔](#)

una vez tengamos acceso a la interfaz del dispositivo Mikrotik

## Cambiar el nombre del dispositivo para identificarlo como R1:

En Winbox, sigue estos pasos:

a. Una vez iniciado sesión en Winbox, en la parte superior, en la "barra de título" que muestra el nombre actual del dispositivo. Hacer clic en ese nombre.

b. Se abrirá una ventana de edición. En el campo "Name", ingresar "R1" o el nombre deseado.

c. Hacer clic en el botón "Apply" para guardar los cambios.

#### Cambiar el nombre a través de la línea de comandos (CLI):

a. Acceder a la interfaz de línea de comandos del enrutador MikroTik.

b. Ejecutar el siguiente comando para cambiar el nombre del dispositivo:

` /system identity set name=R1
`

c. Si el cambio de nombre aún no se guarda, es posible que debas reiniciar el dispositivo o simplemente desconectarte y volver a conectarte.

## Etiquetar las interfaces a utilizar (2 WAN y una LAN):

#### Etiquetar las interfaces:

a. Asignar etiquetas a las interfaces:
Supongamos que tus interfaces WAN son "ether2" y "ether3", y tu interfaz LAN es "lan". Queremos etiquetar las interfaces WAN con las VLANs 10 y 20, y la interfaz LAN con la VLAN 30.

`
    /interface ethernet set ether1 vlan-id=10
    /interface ethernet set ether2 vlan-id=20
    /interface ethernet set ether3 vlan-id=30
`

b. Crear VLANs:
Ahora, debemos crear las VLANs correspondientes:

#### Configurar direcciones IP:
Asigna direcciones IP a las VLANs según tu configuración de red:

`
    /ip address add address=10.11.1.1/24 interface=vlan10
    /ip address add address=10.10.1.100/24 interface=vlan20
    /ip address add address=192.168.1.200/24 interface=vlan30
`

## Agregar un bridge y sus interfaces para la red LAN.

## Crear el Bridge:
En la interfaz de línea de comandos de MikroTik, ejecutamos el siguiente comando para crear un puente:

`
    /interface bridge add name=bridge-lan
`

<i>Aquí, "bridge-lan" es el nombre que le estamos asignando al puente.</i>

#### Agregar interfaces al Bridge:
Luego, hay que agregar las interfaces LAN al puente que creado. Supongamos que las interfaces en este caso la interfaz "lan":

`
    /interface bridge port add bridge=bridge-lan interface=lan
`

<i>Esto hará que las interfaces "lan" forme parte del puente "bridge-lan".</i>


#### Configurar direcciones IP en el puente:

Configura una dirección IP para el puente. Esto permitirá la gestión del enrutador a través del puente.

`
/ip address add address=192.168.1.1/24 interface=bridge-lan
`

<i>Asegúrate de usar una dirección IP apropiada para tu red local.</i>
    
## Agregar el direccionamiento para las dos redes externas WAN y la red interna LAN:

Configuración de direcciones IP:

- WAN1:

    `
        /ip address add address=10.11.1.0/24. interface=ether1
        /ip route add gateway=10.11.1.1
    `

- WAN2:
    
    ` 
        /ip address add address=10.11.1.0/24. interface=ether1
        /ip route add gateway=10.11.1.1
    `

    <i>Esto configura la dirección IP de WAN1 en la interfaz "ether1" y establece la puerta de enlace predeterminada como "10.11.1.1".</i>

## Agregar un Pool en el segmento de la LAN que asigne direcciones entre 192.168.1.100-192.168.1.200

#### Configuración del Pool DHCP en la red LAN:

`
    /ip pool add name=pool-lan ranges=192.168.1.100-192.168.1.200
    /ip dhcp-server add name=dhcp-lan interface=bridge-lan address-pool=pool-lan
`

<i>Esto agrega un servidor DHCP y la información de puerta de enlace y DNS que enviara a los PC conectados a la LAN.</i>

#### Configurar puerta de enlace:

`
    /ip dhcp-server network set [find] gateway=192.168.1.1
`

<i>Esto establece la dirección IP del puente interno (192.168.1.1) como la puerta de enlace para los dispositivos que obtienen direcciones IP a través del servidor DHCP.</i>

#### Configurar servidores DNS:

`
    /ip dhcp-server set [find] use-dns=yes
    /ip dns set servers=8.8.8.8,1.1.1.1
`

<i>La primera línea activa el uso de servidores DNS en el servidor DHCP. La segunda línea configura los servidores DNS a los que se dirigirán los dispositivos. En este caso, se utilizan los servidores DNS de Google (8.8.8.8 y 1.1.1.1) DNS de Google y de Cloudflare</i>

## Agregar la ruta por defecto 0.0.0.0/0.

`
/ip route add dst-address=0.0.0.0/0
`

## 3. [Configurar enrutamiento MikroTik ✔](#)

## Agregar las rutas estáticas necesarias para que los tres router conozcan la ruta a los otros dos.

Si deseas configurar rutas estáticas en tres enrutadores para que conozcan la ruta entre ellos, debes configurar las rutas apropiadas en cada uno. Supongamos que tienes tres enrutadores: R1, R2 y R3, y deseas que cada enrutador conozca cómo llegar a los otros dos. Aquí tienes los pasos para hacerlo:

#### Ruta a R2
`
/ip route add dst-address=192.168.2.0/24 gateway=IP_de_R2
`


#### Ruta a R3:
`
/ip route add dst-address=192.168.3.0/24 gateway=IP_de_R3
`

## Realizar pruebas de diagnostico PING y TRACEROUTE desde el router a los otros router.



- Utiliza el comando PING seguido de la dirección IP del enrutador de destino:

`
/ping IP_del_enrutador_destino
`


- Utiliza el comando TRACEROUTE seguido de la dirección IP del enrutador de destino:

`
/tool traceroute IP_del_enrutador_destino
`


## Realizar un backup de la configuración del equipo.

En la interfaz de administración, sigue estos pasos para realizar una copia de seguridad de la configuración:

a. Haz clic en la pestaña "Files" en el lado izquierdo.

b. En la ventana "Files", verás una lista de archivos y carpetas en el sistema de archivos del enrutador.

c. Haz clic en el botón "Backup" en la parte superior de la ventana. Esto abrirá una nueva ventana para configurar la copia de seguridad.

d. En la ventana de configuración de copia de seguridad, puedes seleccionar las opciones que desees. Por lo general, es recomendable marcar las casillas para "Include Password" y "Include User Database" para asegurarte de que las contraseñas y la base de datos de usuarios se incluyan en la copia de seguridad.

e. Ingresa un nombre para el archivo de copia de seguridad en el campo "File name." Por ejemplo, "backup_agosto_2023.backup".

f. Finalmente, haz clic en el botón "Backup" para crear la copia de seguridad. El enrutador generará un archivo de copia de seguridad que se guardará en el sistema de archivos.
