 ## Instala no equipo tyrion (Windows) o rol de servidor DHCP coa seguinte configuración: (deberás ter apagados os servidores DHCP do punto anterior) ##

1. Un ámbito para os equipos da rede privada lanister, con un intervalo de exclusión.

![imaxe1](capturas/captura1.png)

2. Deberás crear unha reserva estática que estará no rango de enderezos do seu ámbito correspondente.

![imaxe2](capturas/captura2.png)

3. Establece os nomes de dominio e servidores DNS primario de cada zona.

![imaxe2](capturas/captura3.png)

4. Deberás actualizar a zona primaria no servidor DNS tywin.


5. Engade outro ámbito para a rede primaria stark (necesitas outra interface de rede) que actualice a zona prinaria DNS definida no equipo arya.

6. Instala no equipo jaime un servizo DHCP failover para a subrede lanister.

- Instalas el servicio DHCP
- Configuramos el DHCP
![imaxe2](capturas/captura4.png)

![imaxe2](capturas/captura5.png)

-Del enrutador, el router

![imaxe2](capturas/captura6.png)

- Añadimos el DNS

![imaxe2](capturas/captura7.png)

- Activar las actualizaciones de DNS en el DHCP y luego en el DNS de la zona:

![imaxe2](capturas/captura21.png)

- Comprobar que el DHCP primario funciona:

![imaxe2](capturas/captura10.png)

- Cpmprobamos que apagando el DHCP primario sigue asignando IP desde Jamie:

![imaxe2](capturas/captura11.png)

- Comprobamos que el dns se añadio correctamente

![imaxe2](capturas/captura12.png)

- En STARK, Jon recibe la IP por el DHCP:

![imaxe2](capturas/captura13.png)

-Comprobamos que recibe esa ip:
![imaxe2](capturas/captura14.png)

- Comprobamos que el dns se añadio bien 
![imaxe2](capturas/captura15.png)

7. Necesitarás polo menos tres clientes (Cercei,Joffrey, Myrcella) para a rede lannister e un para a  rede stark (jon).
    Inclúe capturas de:
    Configuración dos ambitos e rangos de enderezos
    Configuración de opcións
    Configuración da actualización
    Vídeo no que o cliente renova a concesión, e se ve  a zona DNS unha vez que o DHCP actualiza o DNS. Tamén o cliente debe ser capaz de resolver o seu propio nome (non FQDN).
    Clientes das dúas subredes, amosando DNS, router e enderezo IP.
    Configuración dos servidores failover.

![imaxe2](capturas/captura3.png)

9. Capturas dos clientes obtendo enderezos cos dous servidores failover encendidos, e con un acendido e outro apagado (de forma alterna)9.Elimina a interface de rede 192.168.11.8 de tyrion, e configura o servizo DHCP Relay no router. Comproba que os equipos da rede stark.lan reciben a configuración de rede de xeito correcto. Inclúe as capturas necesarias.

- En Tyrion desactivamos la interfaz 11.
![imaxe2](capturas/captura16.png)
- Configuramos en router el DHCP relay
![imaxe2](capturas/captura17.png)
- Y en el router decimos que envíe por Ethernet, para que llegue a la subred a la que el DHCP no
tiene vinculada
![imaxe2](capturas/captura20.png)
- comprobamos que el equipo recibe la IP
![imaxe2](capturas/captura18.png)
- En el router también podemos comprobar que está funcionando correctamente
![imaxe2](capturas/captura18.png)