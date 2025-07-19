
🔐 Puertos Importantes para Hacking (por Categoría)

🌐 Web y HTTP/HTTPS

| Puerto | Protocolo | Servicio | Descripción                                                    |
| ------ | --------- | -------- | -------------------------------------------------------------- |
| 80     | TCP       | HTTP     | Web sin cifrar. Objetivo común de pruebas (XSS, LFI, etc.).    |
| 443    | TCP       | HTTPS    | Web cifrada. Puede ser objetivo de ataques TLS, SSRF, etc.     |
| 8080   | TCP       | HTTP-alt | Usado como servidor web alternativo o panel de administración. |
📁 Compartición de Archivos y Redes Windows

| Puerto   | Protocolo | Servicio   | Descripción |
|----------|-----------|------------|-------------|
| 137-139  | TCP/UDP   | NetBIOS    | Compartición de archivos, enumeración de red Windows. |
| 445      | TCP       | SMB        | Compartición en Windows. Usado en exploits como EternalBlue. |
| 2049     | TCP/UDP   | NFS        | Compartición Unix/Linux. Puede ser montado remotamente. |
🔐 Acceso Remoto

| Puerto | Protocolo | Servicio | Descripción |
|--------|-----------|----------|-------------|
| 22     | TCP       | SSH      | Acceso remoto seguro. Bruteforce, tunneling, pivoting. |
| 23     | TCP       | Telnet   | Acceso sin cifrar. Muy vulnerable, usado para pruebas iniciales. |
| 3389   | TCP       | RDP      | Escritorio remoto Windows. Objetivo común de bruteforce. |
| 5900   | TCP       | VNC      | Control remoto de escritorio. Muchas veces sin autenticación. |
🛜 DNS, DHCP y Servicios de Red

| Puerto | Protocolo | Servicio | Descripción |
|--------|-----------|----------|-------------|
| 53     | UDP/TCP   | DNS      | Resolución de nombres. Usado en ataques como spoofing o tunneling. |
| 67/68  | UDP       | DHCP     | Asignación IP. Puede usarse en ataques rogue DHCP. |
| 123    | UDP       | NTP      | Sincronización horaria. Puede amplificar ataques DDoS. |
✉️ Correo Electrónico

| Puerto | Protocolo | Servicio | Descripción |
|--------|-----------|----------|-------------|
| 25     | TCP       | SMTP     | Envío de correo. Spoofing o envío de spam. |
| 110    | TCP       | POP3     | Correo entrante. Puede ser interceptado sin cifrado. |
| 143    | TCP       | IMAP     | Acceso a correo. A veces mal protegido. |
| 465    | TCP       | SMTPS    | SMTP cifrado con SSL. |
| 587    | TCP       | SMTP-TLS | Envío de correo autenticado. |
| 993    | TCP       | IMAPS    | IMAP cifrado. |
| 995    | TCP       | POP3S    | POP3 cifrado. |
🗃️ Bases de Datos

| Puerto | Protocolo | Servicio     | Descripción |
|--------|-----------|--------------|-------------|
| 1433   | TCP       | MS SQL       | Microsoft SQL Server. Bruteforce o inyección SQL. |
| 1521   | TCP       | Oracle DB    | Oracle Database. Puede revelar datos críticos. |
| 3306   | TCP       | MySQL        | Común en servidores web. Inyecciones o acceso directo. |
| 5432   | TCP       | PostgreSQL   | Base de datos PostgreSQL. |
| 6379   | TCP       | Redis        | Base de datos en memoria. A menudo sin autenticación. |
☁️ Servicios Misceláneos

| Puerto | Protocolo | Servicio     | Descripción |
|--------|-----------|--------------|-------------|
| 111    | TCP/UDP   | RPCbind      | Usado para localizar servicios RPC como NFS. |
| 135    | TCP       | MS RPC       | Windows DCOM, enumeración en entornos Windows. |
| 161/162| UDP       | SNMP         | Monitorización de red. A menudo sin contraseña. |
| 873    | TCP       | rsync        | Sincronización de archivos. Puede estar expuesto. |
| 1080   | TCP       | SOCKS Proxy  | Usado como proxy para túneles o rebotes. |
| 5060   | UDP       | SIP          | Voz IP. Puede permitir escucha o suplantación. |
| 902    | TCP       | VMware ESXi  | Acceso a máquinas virtuales o administración remota. |
📌 Consejos útiles

- Usa `nmap -sS -p- IP` para escaneo completo de puertos TCP.
- Usa `nmap -sU -p- IP` para escaneo UDP (más lento).
- Usa `nmap -sV -sC` para detección de servicios y scripts de enumeración.
- Herramientas recomendadas: `nmap`, `rustscan`, `masscan`, `netcat`, `tcpdump`, `wireshark`.
