## 1.6 logs + utilidade rndc + nsupdate


1. Fai que no equipo darthvader se faga un log de todas as consultas (/var/log/bind/queries.log) e de todas as actualizacions (/var/log/bind/update.log) a dous ficheiros de log diferentes. Captura a configuración. Amosa as capturas dos dous ficheiros de log, despois de facer consultas e actualizacións e transferencias de zona.

Creamos todo o necesario para que poda facer log executando os seguintes comandos:

![imaxe1](capturas/captura1.png)

Realizamos varias consultas:

![imaxe2](capturas/captura2.png)

Capturas dos dous ficheiros despois das consultas:

![imaxe3](capturas/captura3.png)

2. Investiga como co comando "dig" podes pedir unha copia dunha zona.

![imaxe4](capturas/captura4.png)

3. Permite que o equipo darthvader poida ser controlado coa utilidade rndc desde un cliente ubuntu ou debian. Fai unha captura do servidor reiniciandose.

Añadimos esto en el apartado de named.conf.options del darthvader.
    
![imaxe5](capturas/captura5.png)

Creamos el rndc.conf dentro de leia

![imaxe6](capturas/captura6.png)

Añadimos este archivo al compose

![imaxe7](capturas/capturas7.png)

4. Instala unha zona dinámica no servidor darthvader chamada galaxia.lan e introduce os rexistros aaylasecura (192.168.20.239) e yarua (192.168.20.238). Esta zona debe ser cargada mediante rndc, e o servidor reiniciado con rndc. Proba tamén a eliminala con rndc. Inclue capturas do resultado dos comandos, comprobando tamén que se poden facer consultas.

![imaxe10](capturas/captura10.png)

![imaxe11](capturas/capturas11.png)

![imaxe12](capturas/captura12.png)

Comprobaciones:
![imaxe8](capturas/captura8.png)

![imaxe9](capturas/captura9.png)

5. Mediante a utilidade nsupdate, engade un rexistro chamado darthmaul (192.168.20.144) á zona starwars.lan empregando chaves

Creamos el archivo actualiza.txt y lo rellenamos con esto:

![imaxe14](capturas/captura14.png)

Una vez creado se actualiza con el nsupdate y hacemos la comprobación:

![imaxe13](capturas/captura13.png)
