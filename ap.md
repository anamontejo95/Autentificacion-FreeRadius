# Access Point  

Para esta práctica voy a usar un Punto de Acceso de la marca TP-LINK, el modelo TL-WA801N.  

![a](https://github.com/anamontejo95/Autentificacion-FreeRadius/blob/main/imagenes/ap.jpg)

Comienzamos conectando el Punto de Acceso a la corriente y mediante el cable Ethernet lo conecto a mi portatil para poder acceder a su configuración. 
Una vez dentro lo primero que hago es elegir el modo de operación, en mi caso elijo el modo Punto de Acceso que es el que me interesa para llevar a cabo esta práctica.  

![a](https://github.com/anamontejo95/Autentificacion-FreeRadius/blob/main/imagenes/accesspoint/1.png)  

A continuación, le configuro una IP estática dentro de mi red que es la 192.168.1.0 y le asigno la IP 192.168.1.254, la máscara /24 y la gateway que es la IP de mi router, es decir, la 192.168.1.1  

![a](https://github.com/anamontejo95/Autentificacion-FreeRadius/blob/main/imagenes/accesspoint/2.png)  

Habilito la conexión inalámbrica y le asigno un nombre a mi punto de acceso. El nombre será TP-Proyecto-Ana  

![a](https://github.com/anamontejo95/Autentificacion-FreeRadius/blob/main/imagenes/accesspoint/3.png)  

En la sección DHCP settings habilito el servicio DHCP y configuro el rango de IPs que va a asignar, en este caso en rango es 192.168.1.100 - .192.168.1.199.  
Añado la gateway y el servidor DNS que será el de mi proveedor de internet.  

![a](https://github.com/anamontejo95/Autentificacion-FreeRadius/blob/main/imagenes/accesspoint/5.png)  

En el apartado Time Settings configuro mi zona horaria.  

![a](https://github.com/anamontejo95/Autentificacion-FreeRadius/blob/main/imagenes/accesspoint/6.png)  

Por último en la sección Status podemos ver la configuración que he hecho.  

![a](https://github.com/anamontejo95/Autentificacion-FreeRadius/blob/main/imagenes/accesspoint/7.png)
