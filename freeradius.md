# Servidor FreeRadius  

Para crear el servidor de FreeRadius voy a crear una máquina virtual en VirtualBox con el sistema operativo Ubuntu.  

Como esta máquina va a actuar como servidor lo primero es configurarle una IP estática dentro de nuestra red. Para ello vamos al fichero 

>>/etc/netplan/01-network-manager-all.yaml  

Como podemos ver le he asignado una IP estática, una gateway y un servicio DNS.  

![a](https://github.com/anamontejo95/Autentificacion-FreeRadius/blob/main/imagenes/freeradius/1.png)  

Ahora instalamos el servicio FreeRadius con el comando  

>>apt install freeradius  

Y comprobamos que el servicio esté funcionando.  

![a](https://github.com/anamontejo95/Autentificacion-FreeRadius/blob/main/imagenes/freeradius/2.png)  

Vamos a la carpeta donde se encuentran los ficheros de configuración de este servicio que está en la ruta  

>>/etc/freeradius/3.0  

![a](https://github.com/anamontejo95/Autentificacion-FreeRadius/blob/main/imagenes/freeradius/3.png)  

## Fichero Users  

En el fichero users vamos a definir los usuarios que podrán tener acceso así como sus contraseñas para cada uno de ellos.  

![a](https://github.com/anamontejo95/Autentificacion-FreeRadius/blob/main/imagenes/freeradius/4.png)

Podemos comprobar que el puerto de escucha por defecto (1812) esté abierto y escuchando con el comando:  

>>ss -ln  

![a](https://github.com/anamontejo95/Autentificacion-FreeRadius/blob/main/imagenes/freeradius/5%20ss%20-ln.png)  

## Fichero Clients  

En el fichero clients.conf vamos a configurar al cliente que es el punto de acceso. Para ello introducimos su IP y la contraseña que compartirán el servidor FreeRadius y el Access Point.  

![a](https://github.com/anamontejo95/Autentificacion-FreeRadius/blob/main/imagenes/freeradius/5.png)  

## Access Point  

Tenemos que volver al punto de acceso para terminar su configuración vinculándolo con el servidor que ya tenemos preparado. Para ello podemos acceder con nuestra navegador a la página del punto de acceso sin necesidad de cable ya que ahora si conocemos su ip.  
En el apartado Wireless Security eligo la opción WPA/WPA2 - Enterprise. Le indico el tipo de encriptación (AES), la IP del servidor y la clave que comparten.  
![a](https://github.com/anamontejo95/Autentificacion-FreeRadius/blob/main/imagenes/accesspoint/4.png)

## Radtest  

Podemos hacer una prueba desde el propio servidor para comprobar que está funcionando correctamente con el comando:  

>>radtest ana montejo 192.168.1.254 1812 Rodrigo2023!
>>radtest usuario contraseña ip-access-point puerto contraseña-radius-ap  

![a](https://github.com/anamontejo95/Autentificacion-FreeRadius/blob/main/imagenes/freeradius/6.png)
