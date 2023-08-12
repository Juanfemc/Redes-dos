# Práctica de Laboratorio 01

## [Preguntas reflexivas de ambientación](#)

### ¿Cual es la dirección de red y de broadcast de un host que tiene una ip 192.168.10.10/30?

| Dirección IP | Máscara de Red |
|--------------|----------------|
|192.168.10.10 |255.255.255.252 |
|              |                |


| Dirección Red | Primera Dirección | última Dirección | Broadcast      |
|---------------|-------------------|------------------|----------------|
| 192.168.10.8  | 192.168.10.9      | 192.168.10.10    | 192.168.10.11  |
|               |                   |                  |                |     

_Dos direcciones ip disponibles_     

### ¿Que información se puede inferir de un host con la dirección 169.254.255.200/26?.

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



