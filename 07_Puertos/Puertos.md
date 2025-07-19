## 🔌 Puertos Comunes e Importantes para Hacking

> ⚠️ **Nota**: Conocer los puertos es esencial para el escaneo de red, enumeración de servicios y explotación.

### 📍 Puertos Bien Conocidos (0–1023)

| Puerto | Protocolo | Servicio       | Descripción breve                                                |
|--------|-----------|----------------|------------------------------------------------------------------|
| 20     | TCP       | FTP (Data)     | Transferencia de archivos (canal de datos).                      |
| 21     | TCP       | FTP (Control)  | Inicio de sesión FTP y comandos.                                |
| 22     | TCP       | SSH            | Acceso remoto cifrado. Muy usado para bruteforce o tunneling.   |
| 23     | TCP       | Telnet         | Acceso remoto sin cifrar. Objetivo común por su inseguridad.    |
| 25     | TCP       | SMTP           | Envío de correos. Usado en ataques de spam o spoofing.          |
| 53     | UDP/TCP   | DNS            | Resolución de nombres. Usado en ataques de DNS spoofing.        |
| 67/68  | UDP       | DHCP           | Asignación de IP. Puede usarse para rogue DHCP.                 |
| 69     | UDP       | TFTP           | FTP simple sin autenticación. Blanco fácil.                     |
| 80     | TCP       | HTTP           | Web sin cifrar. Punto de entrada común (XSS, LFI, etc.).        |
| 110    | TCP       | POP3           | Correo entrante. Puede ser objetivo para credenciales.          |
| 111    | TCP/UDP   | RPCbind        | Identificación de servicios RPC (NFS, etc.).                    |
| 123    | UDP       | NTP            | Sincronización horaria. Puede ser explotado en ataques DDoS.    |
| 135    | TCP       | MS RPC         | Servicios Windows (DCE/RPC). Usado en enumeración o exploits.  |
| 137-139| UDP/TCP   | NetBIOS        | Compartición de archivos en Windows. Enumeración de red.        |
| 143    | TCP       | IMAP           | Correo entrante. A veces sin cifrar.                            |
| 161/162| UDP       | SNMP           | Administración de red. Muchas veces mal configurado.            |
| 179    | TCP       | BGP            | Routing entre sistemas. Pocos ataques, pero críticos.           |
| 389    | TCP/UDP   | LDAP           | Directorio de usuarios. Utilizado en ataques a Active Directory.|
| 443    | TCP       | HTTPS          | Web cifrada. Objetivo de SSL stripping o fallos en TLS.         |
| 445    | TCP       | SMB            | Compartición de archivos (Windows). Muy explotado (EternalBlue).|
| 465    | TCP       | SMTPS          | SMTP cifrado.                                                    |
| 514    | UDP       | Syslog         | Registro de eventos. Puede ser interceptado.                    |
| 587    | TCP       | SMTP (TLS)     | Envío de correos autenticados.                                  |
| 636    | TCP       | LDAPS          | LDAP seguro.                                                     |
| 873    | TCP       | rsync          | Sincronización remota de archivos. Puede ser público.           |
| 902    | TCP       | VMware         | Acceso a hosts VMware.                                           |
| 993    | TCP       | IMAPS          | IMAP seguro.                                                     |
| 995    | TCP       | POP3S          | POP3 seguro.                                                     |

📍 Puertos Registrados / Misceláneos (1024–49151)

| Puerto  | Protocolo | Servicio       | Uso en hacking                                                   |
|---------|-----------|----------------|------------------------------------------------------------------|
| 1080    | TCP       | SOCKS Proxy    | Usado como proxy para tunneling.                                |
| 1433    | TCP       | MS SQL Server  | Base de datos Microsoft. Objetivo de ataques de inyección.      |
| 1521    | TCP       | Oracle DB      | Base de datos Oracle.                                            |
| 1723    | TCP       | PPTP VPN       | VPN antigua. Vulnerable.                                         |
| 2049    | TCP/UDP   | NFS            | Sistema de archivos en red. Se puede montar remotamente.         |
| 3306    | TCP       | MySQL          | BD MySQL. Común en webapps.                                     |
| 3389    | TCP       | RDP            | Escritorio remoto de Windows. Ataques de fuerza bruta o exploits.|
| 5060/61 | UDP/TCP   | SIP            | Telefonía IP. VoIP, blanco de sniffing o spoofing.               |
| 5432    | TCP       | PostgreSQL     | Base de datos PostgreSQL.                                       |
| 5900    | TCP       | VNC            | Escritorio remoto. A menudo sin cifrar.                         |
| 6379    | TCP       | Redis          | BD en memoria. A menudo sin autenticación.                      |
| 8080    | TCP       | HTTP alt       | Servidores web secundarios.                                     |

### 🛠️ Consejos

- 📡 Usa herramientas como `nmap`, `masscan` o `rustscan` para detectar servicios abiertos.
    
- 🔍 Observa versiones con `nmap -sV` y vulnerabilidades con `--script vuln`.