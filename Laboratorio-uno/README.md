# Práctica de Laboratorio 01

## [Preguntas reflexivas de ambientación](#)

### a. ¿Cual es la dirección de red y de broadcast de un host que tiene una ip 192.168.10.10/30?

| Dirección IP | Máscara de Red |
|--------------|----------------|
|192.168.10.10 |255.255.255.252 |
|              |                |


| Dirección Red | Primera Dirección | última Dirección | Broadcast      |
|---------------|-------------------|------------------|----------------|
| 192.168.10.8  | 192.168.10.9      | 192.168.10.10    | 192.168.10.11  |
|               |                   |                  |                |     

_Dos direcciones ip disponibles_     

### b. ¿Que información se puede inferir de un host con la dirección 169.254.255.200/26?

La dirección IP 169.254.255.200/26 pertenece a un rango de direcciones especiales conocido como "link-local" o "autoconfiguración de enlace local". Estas direcciones se utilizan en situaciones en las que un dispositivo no puede obtener una dirección IP válida de un servidor DHCP y necesita asignarse automáticamente una dirección para la comunicación en una red local.

En este caso, la notación "/26" indica una máscara de subred de longitud 26, lo que significa que los primeros 26 bits de la dirección IP se utilizan para identificar la red y los últimos 6 bits son para identificar hosts dentro de esa red.

La dirección IP 169.254.255.200 en binario es:

```
10101001.11111110.11111111.11001000
```

La máscara de subred de longitud 26 en binario es:

```
11111111.11111111.11111111.11000000
```

Esto significa que el host con la dirección IP 169.254.255.200/26 pertenece a la red 169.254.255.192/26.

En este rango de direcciones link-local, no se puede inferir mucho sobre la ubicación geográfica o la función del host. Estas direcciones generalmente se utilizan en redes locales para permitir la comunicación entre dispositivos cuando no hay un servidor DHCP disponible. Puede ser que el dispositivo esté configurado para usar una dirección link-local porque no pudo obtener una dirección IP de manera convencional.


### c. ¿Cuantas sub-redes puede lograr con la mascara 172.16.0.0/22?

En el caso de la máscara /22 y una dirección IP base de 172.16.0.0, esto significa que los primeros 22 bits se utilizan para identificar la red y los 10 bits restantes se destinan para los hosts dentro de cada subred.

Cantidad de bits para la porción de red = 22
Cantidad de subredes = 2^22 = 4,194,304

Por lo tanto, con la máscara de subred 172.16.0.0/22, puedes lograr un total de 4,194,304 subredes. Cada una de estas subredes tendría una cantidad de direcciones IP disponibles para hosts, determinada por los 10 bits restantes para la porción de host en cada subred.

### d. ¿Cuantos clientes puede tener la sub red 172.16.0.0/22?

En una subred con la máscara /22, hay 10 bits disponibles para la porción de host, lo que significa que hay 2^10 (1024) direcciones IP únicas disponibles para hosts en esa subred.

Debemos tener en cuenta que algunas direcciones IP dentro de la subred generalmente se reservan para propósitos especiales, como la dirección de red y la dirección de broadcast. Usualmente, la primera dirección IP (la de menor valor) se reserva para la dirección de red, y la última dirección IP (la de mayor valor) se reserva para la dirección de broadcast. Esto significa que la cantidad real de direcciones IP utilizables para clientes será ligeramente menor que 1024.

Por lo tanto, en la subred 172.16.0.0/22, con 10 bits para la porción de host, puedes tener alrededor de 1022 clientes. Recuerda que algunos enrutadores y dispositivos de red también pueden utilizar direcciones IP dentro de la subred, por lo que es importante considerar esto al planificar la cantidad de dispositivos cliente.

### e. ¿Que clase y tipo de dirección es 10.10.10.0/24?

En la actualidad, el concepto de "clases" de direcciones IP se ha vuelto menos relevante debido a la adopción de la notación de máscara de subred variable (VLSM) y al agotamiento de direcciones IPv4. Sin embargo, para responder a tu pregunta:

La dirección IP 10.10.10.0/24 pertenece al rango privado de direcciones IP clase A. 

## [Caracterización de los adaptadores ✔](#)

|Parámetro||Valor|
|--|:--:|--:|
|Número de adaptadores Físicos|-->|2|
|Número de adaptadores Virtuales|-->|5|
|Tipo de Adaptador principal|-->|Wi-fi|
|Fabricante del Adaptador principal|-->|Realtek Semiconductor Corp.|
|Código MAC del fabricante|-->|20-2B-20|
|MAC|-->|20-2B-20-A7-D0-A1|

## [Caracterización de la red ✔](#) 
|Parámetro|Valor|
|--|--:|
|__Subnet__|192.168.1.0/24|
|IPv4|192.168.1.12|
|Subnet Mask decimal|24|
|Subnet Mask octetos|255.255.255.0|
|Número de direcciones de Host|254|
|Rango de direcciones de Host|192.168.1.1-254|
|IP Broadcast|192.168.1.255|
|Server DHCP|192.168.1.254|
|Server DNS|8.8.8.8|

## [Caracterización de la puerta de enlace ✔](#) 
|Parámetro|Valor|
|--|--:|
|Número de Entradas en la tabla ARP |11|
|IPv4 Gateway|192.168.1.1|
|MAC Gateway|80-78-71-04-50-b5|
|ISP|COLOMBIA TELECOMUNICACIONES S.A. ESP|
|[IP Publica][5]|186.99.203.121|

## [Retardo de la red ✔](#) 
|Servidor|IP|Tiempo promedio/ms|
|--|--|--|
|DNS Google|8.8.8.8|49|
|DNS Cloudflare|1.1.1.1|118|
|OpenDNS|208.67.222.222|113|
|Alternate DNS|76.76.19.19|43|
|DNS Quad9|9.9.9.9|60|
|AdGuard DNS|94.140.14.14|178|


## [Capacidad del canal ✔](#) 
|Servidor|Ping/ms|Down/MB|Up/MB|
|--|:--:|--:|--:|
|[speed test][1]|73|2.60|0.81|
|[Netflix][2]||2.9|3.1|
|[Claro][3]|44|2.3|0.9|
|[nperf][4]|48.7|2.79|0.8|
