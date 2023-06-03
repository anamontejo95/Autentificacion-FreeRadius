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
