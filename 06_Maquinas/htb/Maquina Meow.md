Para iniciar la maquina descargamos el fichero .ovpn y lo ejecutamos con el comando:
`$ sudo openvpn "nombre del fichero"`

Tarea 1
Qué representa el acrónimo VM?
<span style="color: lime;">Virtual machine</span>

Tarea 2
Qué herramienta utilizamos para interactuar con el sistema operativo con el fin de emitir comandos a través de la línea de comandos, como la que iniciará nuestra conexión VPN? También se conoce como consola o shell.
<span style="color: lime;">Terminal</span>

Tareas 3
Qué servicio usamos para formar nuestra conexión VPN en laboratorios HTB?
<span style="color: lime;">openvpn</span>

Tareas 4
Qué herramienta usamos para probar nuestra conexión al objetivo con una solicitud de eco ICMP?
<span style="color: lime;">ping</span>

Tareas 5
Cuál es el nombre de la herramienta más común para encontrar puertos abiertos en un objetivo?
<span style="color: lime;">nmap</span>

Tareas 6
Qué servicio identificamos en el puerto 23/tcp durante nuestros escáneres?
<span style="color: lime;">telnet</span>

Tareas 7
Qué nombre de usuario es capaz de conectarse al objetivo sobre telnet con una contraseña en blanco?
<span style="color: lime;">root</span>

Envío de bandera
Enviar bandera de raíz
<span style="color: lime;">b40abdfe23665f766f9c61ecba8a4c19</span>

### Iniciamos la máquina
Hacemos un ifconfing para ver que tenemos conexión con la máquina victima.
![Ping a la IP de la máquina víctima](Imagenes/ping.png)

![[2025-07-14_14-41.png]] 
Hacemos ping a la IP de la maquina victima 

![[Imagenes/2025-07-14_14-55.png]]
Ahora vamos a ver que puertos tiene abiertos con la herramienta nmap

![[2025-07-14_14-59.png]]
Vemos que tiene abierto el puerto 23, un servicio telnet.
Nos conectamos al servicio telnet y nos pide usuario y contraseña.
Probamos las combinaciones mas comunes como admin o root, por las preguntas podemos intuir que el login es root.

![[2025-07-14_15-05.png]]
Ahora solo tenemos que hacer un cat sobre el fichero flag.txt
![[2025-07-14_15-08.png]]
