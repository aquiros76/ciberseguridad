Para iniciar la máquina descargamos el fichero `.ovpn` y lo ejecutamos con el comando:  
`$ sudo openvpn "nombre del fichero"`

### Tarea 1  
**¿Qué representa el acrónimo VM?**  
#### 🟢 Virtual machine

### Tarea 2  
**¿Qué herramienta utilizamos para interactuar con el sistema operativo con el fin de emitir comandos a través de la línea de comandos, como la que iniciará nuestra conexión VPN? También se conoce como consola o shell.**  
#### 🟢 Terminal

### Tarea 3  
**¿Qué servicio usamos para formar nuestra conexión VPN en laboratorios HTB?**  
#### 🟢 *OpenVPN*

### Tarea 4  
**¿Qué herramienta usamos para probar nuestra conexión al objetivo con una solicitud de eco ICMP?**  
#### 🟢 *ping*

### Tarea 5  
**¿Cuál es el nombre de la herramienta más común para encontrar puertos abiertos en un objetivo?**  
#### 🟢 *nmap*

### Tarea 6  
**¿Qué servicio identificamos en el puerto 23/tcp durante nuestros escáneres?**  
#### 🟢 *telnet*

### Tarea 7  
**¿Qué nombre de usuario es capaz de conectarse al objetivo sobre telnet con una contraseña en blanco?**  
#### 🟢 *root*

---

### Envío de bandera  
Enviar bandera de raíz:  
#### 🟢~~`b40abdfe23665f766f9c61ecba8a4c19`~~

---

### Iniciamos la máquina

Hacemos un `ifconfig` para ver que tenemos conexión con la máquina víctima. 

![Ifconfig](https://raw.githubusercontent.com/aquiros76/ciberseguridad/main/Imagenes/Ping.png)

Hacemos ping sobbre la IP de la máquina victima

![Escaneo con nmap](https://raw.githubusercontent.com/aquiros76/ciberseguridad/main/Imagenes/2025-07-14_14-55.png)

Ahora vamos a ver qué puertos tiene abiertos con la herramienta `nmap`:

![Conexión Telnet](https://raw.githubusercontent.com/aquiros76/ciberseguridad/main/Imagenes/2025-07-14_14-59.png)

Vemos que tiene abierto el puerto 23, un servicio Telnet.  
Nos conectamos al servicio Telnet y nos pide usuario y contraseña.
Probamos las combinaciones más comunes como `admin` o `root`, por las preguntas podemos intuir que el login es `root`.

![Lectura de flag.txt](https://raw.githubusercontent.com/aquiros76/ciberseguridad/main/Imagenes/2025-07-14_15-05.png)

Ahora solo tenemos que hacer un `cat` sobre el fichero `flag.txt`:

![Flag capturada](https://raw.githubusercontent.com/aquiros76/ciberseguridad/main/Imagenes/2025-07-14_15-08.png)

