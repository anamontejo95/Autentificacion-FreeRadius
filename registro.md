# Activación de Registro  

En este apartado voy a hacer la configuración necesaria para poder monitorear a los clientes. Voy a registrar tanto las conexiones exitosas como las fallidas. Para ello edito el fichero:  

>>/etc/freeradius/3.0/radiusd.conf  

Voy a la sección de logs, como podemos ver viene deshabilitado por defecto.  

![a](https://github.com/anamontejo95/Autentificacion-FreeRadius/blob/main/imagenes/freeradius/7.png)  

Como queremos que si se recojan el fichero de logs las conexiones editamos el fichero indicando los siguientes parámetros:  

>>auth = yes
>>auth_badpass = yes (para los intentos fallidos)
>>auth_goodpass = yes (para los intentos existosos)  

![a](https://github.com/anamontejo95/Autentificacion-FreeRadius/blob/main/imagenes/freeradius/8.png)  

Una vez editado y guardada la configuración del fichero reinicio el servicio para que se apliquen los cambios.

>>systemctl restart freeradius  

Y por último, pruebo a hacer conexiones al punto de acceso tanto con la contraseña incorrecta como correcta para ver como aparece en el fichero de log.  
Podemos verlo con el comando  

>>tail -f /var/log/freeradius/radius.log  

![a](https://github.com/anamontejo95/Autentificacion-FreeRadius/blob/main/imagenes/freeradius/9.png)
