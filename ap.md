# Access Point  

Para esta práctica voy a usar un Punto de Acceso de la marca TP-LINK, el modelo TL-WA801N.  
Comienzamos conectando el Punto de Acceso a la corriente y mediante el cable Ethernet lo conecto a mi portatil para poder acceder a su configuración. 
Una vez dentro lo primero que hago es elegir el modo de operación, en mi caso elijo el modo Punto de Acceso que es el que me interesa para llevar a cabo esta práctica.  

![a]()  

A continuación, le configuro una IP estática dentro de mi red que es la 192.168.1.0 y le asigno la IP 192.168.1.254, la máscara /24 y la gateway que es la IP de mi router, es decir, la 192.168.1.1  

![a]()  

Habilito la conexión inalámbrica y le asigno un nombre a mi punto de acceso. El nombre será TP-Proyecto-Ana  

![a]()  

En la sección DHCP settings habilito el servicio DHCP y configuro el rango de IPs que va a asignar, en este caso en rango es 192.168.1.100 - .192.168.1.199.  
Añado la gateway y el servidor DNS que será el de mi proveedor de internet.  

![a]()  

En el apartado Time Settings configuro mi zona horaria.  

![a]()  

Por último en la sección Status podemos ver la configuración que he hecho.  

![a]()
