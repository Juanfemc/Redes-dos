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


    


