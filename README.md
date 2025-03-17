# Intoducción

<details>
  <summary>🚀 Explicación de EGC</summary>
Nuestra empresa, EGC (Enterprise Global Chat), ofrece un servicio de chat especializado en diversos sectores como informática, negocios, economía, entre otros. Los usuarios registrados pueden consultar sus dudas directamente con expertos. Nuestro objetivo es brindar soluciones rápidas y efectivas, tanto para usuarios individuales como para pequeñas empresas.
<br>
<br>
  
Nuestra plataforma compite con otras herramientas de mensajería, como Telegram, Skype, Discord, y más, especialmente en lo que respecta a la creación de grupos y redes de usuarios. Sin embargo, en nuestra plataforma, todos los chats son privados entre los usuarios conectados, permitiendo conversaciones directas y seguras.
<br>

Al registrarse en nuestra web, los usuarios podrán acceder a grupos creados por especialistas en sectores como informática, negocios, economía y otros, disponibles en modalidades públicas o privadas. Además, los usuarios podrán crear sus propios grupos de conversación para compartir información y resolver dudas con otros usuarios.
  
</details>
<br>








<details>
<summary>🎨 Diseño de nuestra aplicación</summary>


## Mockup

### Home:

* En la página de inicio tendríamos una imagen de fondo, y en la parte superior de la pestaña se mostraría el logo junto a tres enlaces que dirigirían a páginas donde hablaríamos sobre nosotros, nuestra seguridad y soporte técnico, así como al inicio de sesión. Además, contaríamos con un footer que incluiría los logotipos de nuestras redes sociales.

![image](https://github.com/user-attachments/assets/7c5c27db-fa5a-4ce7-b655-c1a179c5a935)


### Sobre Nosotros:

* En la sección "Sobre nosotros", explicaríamos qué hace nuestra empresa, cuándo fue creada y qué ventajas ofrece en comparación con otros servicios de chat. También incluiríamos imágenes decorativas para mejorar la presentación.

![image](https://github.com/user-attachments/assets/4367be43-9c0b-4f62-b6b4-724a5508d5c5)


### Nuestra Seguridad:

* En la sección "Nuestra seguridad" explicaremos las medidas de seguridad que ofrecemos, sin entrar en detalles específicos.

![image](https://github.com/user-attachments/assets/941276f0-4848-47e5-897f-c80d1c07cc01)


### Soporte Técnico:

* En la sección de soporte técnico, los usuarios podrían ingresar su correo electrónico, describir el problema que tienen y hacer clic en un botón de "Enviar".

![image](https://github.com/user-attachments/assets/63f4c1c3-9c71-42d7-8b81-6e513d4a79f4)


### Chat:

* Este sería nuestro chat, con una lista a la izquierda que muestra nuestros contactos y amigos, y un buscador para encontrar a otros contactos.

![image](https://github.com/user-attachments/assets/6d88b906-7cba-4fa5-85a2-c13a1306e03a)


### Grupos:

* En el catálogo, el usuario podrá buscar temarios sobre ciberseguridad utilizando el buscador, y se le mostrarán diferentes temarios relacionados con el tema.

![image](https://github.com/user-attachments/assets/e68bcc31-368f-4f8c-a04e-0e3e9245ff63)


### Crear Grupo:

* En "Crear catálogo", el usuario podrá subir una imagen, añadir un título y un texto, y deberá ingresar su nombre de usuario en un apartado. Al final, tendrá un botón para crear el catálogo.

![image](https://github.com/user-attachments/assets/12724ed0-f878-4d0b-bd73-a0c204ee2e36)

### Registro:

* Así es como se vería la sección donde se registrarían nuestros usuarios. En el formulario de registro, el usuario deberá ingresar su nombre, primer apellido, un nombre de usuario, su correo electrónico, número de teléfono y una contraseña, la cual deberá confirmar nuevamente.

![image](https://github.com/user-attachments/assets/587a3bd2-9e8c-4737-8d00-9a2e71e7e9d7)


### Inicio Sesión:

* Así es como se vería nuestro inicio de sesión. El usuario solo deberá ingresar su correo electrónico y contraseña.

![image](https://github.com/user-attachments/assets/37ec7c4c-e221-415c-9b8d-cca2adff63e8)

<br>

## Gamma de colores + Logo

### Nuestra gamma de colores:

![image](https://github.com/user-attachments/assets/c999e1eb-701f-43bd-8a99-e5fd0f23e867)

### Nuestro Logo:

![ECS](https://github.com/user-attachments/assets/6ba6de8e-952c-4265-9db4-ab254b4884f4)![image](https://github.com/user-attachments/assets/03bae469-1db6-44f0-bc5f-c439e731b600)


</details>
<br>










<details>
<summary>🗺️ Nuestros esquemas</summary>
Este es nuestro esquema de nuestra web EGC:

![image](https://github.com/user-attachments/assets/d29a31b2-477b-47cb-b0c9-4ed494235236)


</details>
<br>


<details>
<summary>📊 Nuestros Diagramas</summary>

## Diagrama de RED
Como podemos ver en nuestro esquema de red, las máquinas de nuestro Proxmox se conectan al switch (vmbr0), que a su vez se conecta al router de IFP, proporcionándonos la conexión a Internet. Ahora, os mostraremos las máquinas virtuales que contiene nuestro **Proxmox**:

1. Contamos con una máquina virtual (MV) que actúa como router y se conecta a través de **pfSense**, que funciona como el firewall de nuestro proyecto.
2. Tenemos una con el **DNS**.
3. Tenemos una MV donde almacenaremos la **WEB** y el **NGINX**.
4. Una con la bas de datos de **MongoDB**.
5. Contamos con una a la que hemos llamado **cliente** que utilizamos como prueba para verificar si nuestra web funciona correctamente.
6. Otra que contiene nuestro **Docker**.
7. Nuestro **servidor de correo**.
8. Contamos con una MV donde se almacenarán nuestros **backups** de **copias de seguridad** y **recuperación**.

![Esquema-Red-Visual-Paradigm](https://github.com/user-attachments/assets/0e365779-b6c6-4654-9f4b-aa757ba3182c)


## Diagrama de BBDD
Como podemos ver en nuestro diagrama, la tabla **users** se conecta a la tabla **channels** utilizando las tablas de relación **file** y **messages**. También, la tabla usuarios tiene, en conexión aparte, la tabla **friends** y la de **private_chat**.
También tenemos dos tablas de bloqueos, unas es para **Friends** y otra la usariamos en **Channels**.

Como podemos ver en nuestro diagrama, la tabla **users** se conecta a la tabla channels mediante las tablas de relación **file** y **messages**. Además, la tabla users tiene, en una conexión aparte, la tabla **friends** y la de **private_chat**. También contamos con dos tablas de bloqueos: una es **block_friends**, que se utiliza para bloquear a amigos, y la otra es **block_channels**, que se usa para bloquear canales.


![image](https://github.com/user-attachments/assets/3c5e8c62-6a0e-470c-ba1f-e95a000f59e4)





</details>
<br>





<details>
<summary>🐋 Docker</summary>

# ¿Que es el Docker?

Docker es una plataforma que permite crear, distribuir y ejecutar aplicaciones en contenedores. Un contenedor es un entorno ligero y portátil que incluye todo lo necesario para ejecutar un software, como código, bibliotecas y dependencias, asegurando que funcione igual en cualquier sistema. Docker facilita la gestión y escalabilidad de aplicaciones, optimizando el uso de recursos y mejorando la eficiencia en desarrollo y despliegue. Se basa en imágenes preconfiguradas y permite automatizar procesos, haciéndolo ideal para entornos de desarrollo, pruebas y producción en la nube o servidores locales.

![image](https://github.com/user-attachments/assets/c191ed6f-5e29-40d3-87d6-49e7c332e7da)



# Que ventajas y descentajas da el Docker


## Ventajas✅

· **Portabilidad de contenedores**: Los contenedores funcionan igual en cualquier sistema con Docker instalado.

· **Eficiencia**: Consume menos recursos que las máquinas virtuales porque comparte el sistema operativo.

· **Escalabilidad**: Facilita la gestión y despliegue de múltiples instancias de aplicaciones.

· **Rápido despliegue**: Permite automatizar e implementar aplicaciones en segundos.

· **Aislamiento**: Evita conflictos entre dependencias de diferentes aplicaciones.



## Desventajas❌

· **Rendimiento**: Puede ser menos eficiente que una ejecución nativa.

· **Persistencia de datos**: Manejo de almacenamiento más complejo.

· **Seguridad**: Comparte el kernel del host, lo que puede generar vulnerabilidades.



  
# Introducción a la instalación de la web

Guardamos el contenido de la página web en una carpeta llamada web y la comprimimos en un archivo zip. Luego, la exportaremos a la máquina Alpine desde cmd utilizando el siguiente comando:

![image](https://github.com/user-attachments/assets/12bb95df-3edd-4466-9dd6-deb9006288c3)


Para descomprimir la carpeta que hemos exportado, utilizaremos el comando unzip. Luego, creamos una carpeta llamada **rbooks** donde almacenaremos la carpeta web que hemos descomprimido. Será necesario mover la carpeta web dentro de la carpeta **rbooks**.


Accedemos a la carpeta **rbooks** y creamos las siguientes subcarpetas que mostraremos a continuación:

![image](https://github.com/user-attachments/assets/8321eee2-4f73-4e67-9cb4-78866dbcaa43)


Dentro de la carpeta **nginx**, creamos un archivo llamado **default.conf** y le añadimos el siguiente código:

![image](https://github.com/user-attachments/assets/90ee82b1-20dc-441f-b3be-433fbe1ac5a4)


Una vez hecho esto, salimos de la carpeta **nginx** y, dentro de **rbooks**, creamos un nuevo archivo llamado **docker-compose.yml**. A continuación, en el archivo **docker-compose.yml**, aseguramos que el servicio **phpfpm** utilice el *Dockerfile* para construir la imagen personalizada. En lugar de usar la imagen **php:8-fpm-alpine** directamente, debemos indicar que se debe construir la imagen utilizando el *Dockerfile*.

```
services:
  # PHP service
  phpfpm:
    build:
      context: .
      dockerfile: Dockerfile   # Usa el Dockerfile personalizado
    container_name: phpfpm
    working_dir: /var/www/rbooks
    ports:
      - "9000:9000"
    volumes:
      - './web:/var/www/rbooks'
    environment:
      PHP_INI_DIR: /usr/local/etc/php
    restart: always
    networks:
      - netweb

  # Nginx service
  nginx:
    image: nginx:alpine
    container_name: nginx
    ports:
      - "8082:80"
    working_dir: /etc/nginx
    volumes:
      - './web:/var/www/rbooks'
      - './nginx/default.conf:/etc/nginx/conf.d/default.conf'
      - './nginx/:/var/log/nginx/'
    restart: always
    networks:
      - netweb

  # MySQL database service
  db:
    image: mysql
    container_name: miDB
    ports:
      - "3306:3306"
    environment:
      MYSQL_ROOT_PASSWORD: 1234
    volumes:
      - './mysql:/var/lib/mysql'
      - './sql:/db'
    networks:
      - netweb

  # PHPMYADMIN
  phpmyadmin:
    image: phpmyadmin
    container_name: miphpmyadmin
    environment:
      PMA_ARBITRARY: 1
      PMA_HOST: db  # Conectar phpMyAdmin al contenedor "db" (MySQL)
    ports:
      - "81:80"
    networks:
      - netweb

networks:
  netweb:
    driver: bridge

```


A continuación, crearemos el archivo **Dockerfile** y añadiremos el siguiente código para que funcione:

![image](https://github.com/user-attachments/assets/fdf3e8b4-c8e5-4f59-8688-1e79b32abbb1)


Este comando permite forzar la recreación de los contenedores en el **docker**.

![image](https://github.com/user-attachments/assets/152d72fb-a268-4556-888d-92b322e7e909)


Si accedemos a **Portainer** y vamos a la sección de **Contenedores**, podemos ver que se ha creado de forma correcta.

![image](https://github.com/user-attachments/assets/8b4ad89a-204d-4f24-87a1-d69f03bb1b1a)








Si accedemos al navegador y ponemos **http://100.77.20.22:8082**, podremos ver que hemos ingresado correctamente a la página web de RBooks.

![image](https://github.com/user-attachments/assets/574a6d8b-f4c5-4d1b-94d8-e1fc120731d3)


Ahora, debemos cargar la base de datos en **phpMyAdmin** para que las tablas se muestren correctamente y los registros funcionen en la página web. Para ello, accedemos a **http://100.77.20.22:81** en el navegador.
* Servidor --> miDB
* Usuario --> root
* Contraseña --> 1234
 
![image](https://github.com/user-attachments/assets/c53a9069-f0ab-4231-a811-68cecc4c103c)


Creamos la base de datos con el nombre **rbooks**.

![image](https://github.com/user-attachments/assets/04b92b6c-414e-4112-bf8d-d7967d416278)


Para poder importar el archivo **sql** en **phpMyAdmin**, debemos ingresar en la base de datos **rbooks**, hacer clic en *Importar*, seleccionar el archivo **bbdd-rbooks.sql** y luego hacer clic en el botón *Importar*.

![image](https://github.com/user-attachments/assets/2c2f841b-84cb-4e38-a4b2-d93207c67853)


A continuación, accedemos al archivo **conexion_be.php**, que se encuentra en la ruta ***web/php_in-sing/conexion_be.php***, y modificamos la dirección de la base de datos para establecer la conexión entre la página web y la base de datos.

![image](https://github.com/user-attachments/assets/89863329-095d-4ba2-a6ff-69adf2947224)

<br>
<br>
<br>

# Las mejoras que hemos añadido

Estos son los comandos que le hemos puesto en el archivo **docker-compose.yml**.

<br>
<br>

## context: .

•	Define el directorio base donde Docker buscará los archivos necesarios para construir la imagen.

•	En este caso, el **.** (punto) indica que el contexto de construcción es el directorio donde se encuentra el archivo docker-compose.yml.


## dockerfile: Dockerfile

•	Indica al Docker qué archivo usar para construir la imagen. En este caso, se usará el Dockerfile que está en el contexto definido arriba (.).

•	Permite personalizar la imagen en lugar de usar una predefinida.



## PHP_INI_DIR: /usr/local/etc/php

Define la variable de entorno PHP_INI_DIR, que indica la ubicación del archivo de configuración de PHP (php.ini) dentro del contenedor.

<br>
<br>

## Dockerfile Vs docker-compose
![image](https://github.com/user-attachments/assets/7dbc6d20-f0fb-4d98-9a43-3b748478d106)



## Dockerfile

### 1️⃣ FROM php:8-fpm-alpine

```
FROM php:8-fpm-alpine
```

Define la imagen base como php:8-fpm-alpine.



### 2️⃣ Instalación de dependencias y extensiones

```
RUN apk add --no-cache libpng-dev libjpeg-turbo-dev libwebp-dev \
    && docker-php-ext-install mysqli pdo pdo_mysql
```

Usa apk add --no-cache para instalar dependencias en Alpine Linux:

•	libpng-dev, libjpeg-turbo-dev, libwebp-dev: Bibliotecas necesarias para manipulación de imágenes en PHP.


Luego, instala extensiones de PHP con docker-php-ext-install:

•	mysqli: Extensión para conectarse a bases de datos MySQL.

•	pdo y pdo_mysql: Permiten usar PDO (PHP Data Objects) con MySQL.




### 3️⃣ (Opcional) Ajustar php.ini para habilitar mysqli

```
# RUN echo "extension=mysqli.so" >> /usr/local/etc/php/conf.d/docker-php-ext-mysqli.ini
```

Agrega manualmente la línea **extension=mysqli.so** al archivo de configuración de PHP. Se usará cuando PHP no detecta automáticamente la extensión mysqli.


🔹 ¿Cuándo usarlo?

Si mysqli no se activa correctamente después de instalarlo con docker-php-ext-install para asegurar de que PHP cargue la extensión en cada inicio.







</details>
<br>








<details>
<summary>⚙️ Funcionalidades</summary>
Funcionalidades que vamos a implementar:

- Funcionalidades de Registro e inicio de sesión.(Víctor)
- Que los usuarios puedan tener contactos o conversación con técnicos informáticos.(Hugo)
- Los usuarios pueden crear una tabla de técnicos informáticos. (Víctor)


Seguridad (en función de vuestro proyecto):

- MySQL (crear más de un usuario, securizar la DB, triggers)
- Protección de código fuente
- toda la parte de monitorización y seguridad que vais a implementar
</details>
<br>



<details>
<summary>🖥️ Arquitectura del Sistema</summary>
Estos seran los componentes de tecnología que utilizaremos en el sistema:
  
- NGINX:
  
  Servidor web y proxy inverso, muy eficiente en gestionar tráfico y carga.

  
- No MySQL:

  Base de datos relacional para almacenar y gestionar datos.

  
- PHP / HTML / CSS / JS:
  - PHP:

    Lenguaje de programación del lado del servidor.

    
  - HTML:

    Lenguaje para estructurar contenido web.

    
  - CSS:

    Estilos y diseño web.

    
  - JS:
  
    Lenguaje para interactividad en el navegador.

    
    
- Bind9:

  Servidor DNS que resuelve nombres de dominio a direcciones IP.

  
- Docker:

  Plataforma para crear y gestionar contenedores de aplicaciones.

  
- jabberd:

  Servidor de mensajería instantánea basado en XMPP.
  
  
- Composer:

  Herramienta para gestionar dependencias en PHP.
  
  
- WebSocket:

  Protocolo para comunicación en tiempo real entre cliente y servidor.
  
  
- IPTables:

  Firewall en Linux para controlar el tráfico de red.
  

</details>
<br>


<details>
<summary>📦☁️Maquinas Virtuales</summary>

<br>

<details>
<summary>+----------🐧 Sistemas Operativos</summary>

Estos son los Sistemas Operativos que vamos a implementar en la Maquina virtuales.


- Ubuntu Server
  
- Alpine (Docker)

- Firewall


  
</details>
<br>




<details>
<summary>+----------🔲 Hardware</summary>

Todas las VM tienen la misma capacidad de memoria RAM, CPU y disco duro, menos la VM Docker.

MV:
- RAM --> 2 GB
- CPU --> 1 (1 socket & 1 cores)
- HD --> 14 GB
<br>

MV Docker:
- RAM --> 4 GB
- CPU --> 4 (2 sockets & 2 cores)
- HD --> 60 GB

  
</details>

</details>
  
<br>

<details>
<summary>🛡️Seguridad</summary>

<br>

<details>
<summary>+----------💠 Tipos de Seguridad</summary>

# 🔥 Protección contra ataques (DDoS, Hydra, etc.)

<br>

## 1️⃣ En el Router/Ubuntu (Entrada de la red)

📌 Motivo: Es el primer punto de entrada y debe filtrar tráfico malicioso antes de que llegue a los servidores internos.

✅ Medidas:

* Firewall (iptables, UFW): Restringir accesos por IP y puertos.

* Sistema de Prevención de Intrusos (IPS) como Fail2Ban o Suricata: Detectar y bloquear intentos de fuerza bruta (Hydra).

* Protección contra DDoS (Cloudflare, iptables con rate limiting, servicios de mitigación DDoS como AWS Shield o Cloudflare).

* VPN (WireGuard, OpenVPN): Para acceso seguro de administradores.

<br>

## 2️⃣ Servidor Web

📌 Motivo: Objetivo principal de ataques como DDoS, SQL Injection y explotación de vulnerabilidades.

✅ Medidas:

* WAF (Web Application Firewall) como ModSecurity: Bloqueo de ataques a la aplicación web.

* Limitación de conexiones simultáneas con herramientas como fail2ban.

* TLS/SSL para cifrar la comunicación HTTPS.

<br>

## 3️⃣ Servidor Base de Datos

📌 Motivo: Contiene información sensible y puede sufrir SQL Injection o ataques de fuerza bruta.

✅ Medidas:

* Permitir conexiones solo desde el servidor web (bloquear accesos externos).

* Cifrar datos sensibles en la base de datos.

* Autenticación fuerte y rotación de contraseñas.

<br>

## 4️⃣ Docker

📌 Motivo: Puede contener aplicaciones con vulnerabilidades explotables.

✅ Medidas:

* Restringir acceso a contenedores con redes privadas.

* Escanear imágenes con herramientas como Trivy.

* Configurar permisos mínimos en los contenedores.

<br>

## 5️⃣ Servidor de Correo

📌 Motivo: Sujeto a ataques de phishing y fuerza bruta (SMTP, IMAP, POP3).

✅ Medidas:

* SPF, DKIM y DMARC para evitar suplantación de identidad.

* Rate limiting para prevenir ataques de fuerza bruta.

* Filtrado de spam con herramientas como SpamAssassin.

<br>

## 6️⃣ Servidor DNS

📌 Motivo: Puede ser objetivo de ataques de envenenamiento de caché o DDoS.

✅ Medidas:

* DNSSEC para validar respuestas DNS.

* Rate limiting en consultas para mit


</details>




<br>

<details>
<summary>+----------📄🛡️ Backup (Copias de Segiridad)</summary>

**https://www.incibe.es/sites/default/files/contenidos/guias/guia-copias-de-seguridad.pdf**
  
# ¿Qué es una copia de seguridad y que importancia tiene?

Una copia de seguridad es un proceso que permite duplicar y almacenar información con el fin de recuperarla en caso de pérdida o fallo del sistema. En el ámbito empresarial, resulta fundamental para garantizar la continuidad del negocio y mantener la confianza de los clientes. Forma parte de los planes de seguridad y contingencia, asegurando la protección, disponibilidad y recuperación de los datos de manera eficiente y periódica.

Imagina que tienes un cuaderno en el que anotas información crucial para tu escuela. Si lo pierdes o se daña, toda esa información desaparecería, lo que sería un gran problema. Lo mismo ocurre con los datos de un negocio: si no se cuenta con una copia de seguridad, cualquier fallo, error humano o ciberataque podría ocasionar la pérdida definitiva de información valiosa.
Por ello, realizar copias de seguridad regularmente es esencial. Es como tener una segunda versión de tu cuaderno guardada en un lugar seguro, lista para ser utilizada en caso de emergencia, evitando así pérdidas irreparables y garantizando la estabilidad de la información.


# ¿Qué copias de seguridad hariamosa?
Para definir qué información debe incluirse en las copias de seguridad, primero es necesario realizar un inventario de activos y clasificar los datos según su importancia para el negocio. Esta clasificación nos permitirá priorizar la protección de la información crítica y definir estrategias adecuadas de respaldo:

* Confidencialidad: (confidencial, interna, pública).

* Utilidad: (clientes, ventas, personal).

* Impacto: (daño de imagen, consecuencias legales, económicas, paralización de la actividad).

Esto ayuda a establecer medidas de seguridad y decidir qué información proteger, como datos de clientes, ventas o personal, y su frecuencia de respaldo.


# ¿Qué estrategias seguiríamos?
Para garantizar la seguridad y disponibilidad de nuestros datos, aplicaremos la estrategia 3-2-1 de copias de seguridad, una de las mejores prácticas en la gestión de respaldos. Su objetivo es diversificar el almacenamiento de las copias para minimizar el riesgo de pérdida de información y asegurar la posibilidad de recuperación en caso de fallo. Sus principios clave son:

* 3 copias: Mantener tres versiones de cada archivo importante: el original y al menos dos copias de respaldo.
* 2 soportes diferentes: Almacenar las copias en al menos dos tipos de medios distintos (por ejemplo, un disco duro externo y almacenamiento en la nube) para mitigar riesgos como fallos mecánicos o corrupción de datos.
* 1 copia fuera de la empresa: Guardar al menos una copia en una ubicación externa (como un servicio de almacenamiento en la nube) para proteger la información ante desastres físicos, robos o ciberataques en la infraestructura local.

Ejemplo práctico
Si trabajamos con un archivo crítico llamado "listadoproveedores.ots", podríamos aplicar la estrategia 3-2-1 de la siguiente manera:

* Archivo original: Se almacena en el equipo principal donde se trabaja con él.
* Primera copia de seguridad: Se guarda en un disco duro externo o servidor NAS local.
* Segunda copia de seguridad: Se sube a un servicio de almacenamiento en la nube (cumpliendo también con la regla de "ubicación externa").


# ¿Dónde se van a ubicar las copias?

Por el momento, almacenaremos nuestras copias de seguridad en Google Drive y en discos duros externos como medida preventiva ante cualquier incidente inesperado, garantizando que siempre tengamos acceso a nuestros datos en caso de fallos o imprevistos.

Además, hemos decidido implementar un sistema de almacenamiento en la nube para reforzar aún más la seguridad y disponibilidad de la información. Actualmente, estamos en proceso de evaluación y configuración de este servicio, asegurándonos de elegir la mejor opción en términos de fiabilidad, cifrado y accesibilidad.

También crearemos una máquina virtual en Proxmox que funcionará como servidor central para almacenar toda la información, bases de datos y código fuente de nuestro proyecto. Además, configuraremos copias de seguridad automatizadas y medidas de seguridad como firewalls y cifrado para garantizar la integridad y protección de los datos.


# Esto sera la información que copiaremos para asegurar nuestro proyecto:

* Base de Datos: La información de los usuarios y datos críticos de la empresa deben resguardarse con la mayor frecuencia posible. Un respaldo frecuente y seguro es clave para evitar pérdidas de información valiosa.

* DNS: El DNS es fundamental para el funcionamiento de los servicios en línea, asegurando que los dominios estén correctamente direccionados. Un backup del DNS garantiza que la infraestructura web siga operativa en caso de fallos.

* Código de la Web y Nginx: Resguardar el código fuente de la web junto con la configuración de Nginx es esencial para una rápida recuperación en caso de incidentes o ataques.

* Router: Mantener una copia de seguridad de la configuración del router es crucial para garantizar la conectividad de la red y facilitar su restauración en caso de fallas o modificaciones accidentales.



# Códigos del Backup
## Copias de seguridad
Hemos creado este script en Bash para automatizar la copia de seguridad cifrada de archivos desde servidores remotos a un sistema local. Su objetivo es garantizar que los respaldos sean descargados, cifrados y almacenados de forma segura, manteniendo un historial controlado mediante la gestión de copias previas y registros en un archivo de log. A continuación, os mostraremos que hace cada parte del código:

1. Configuración de usuarios de los ordenadores de destino, IPs de los ordenadores, carpeta local de respaldo, rutas en los ordenadores remotos, carpeta de logs, formato de fecha y hora; y archivo de log.
2. Crear la carpeta de logs si no existe.
3. Redirigir la salida estándar y los errores al archivo de log.
4. Escribir en el log el inicio de la ejecución.
5. Preguntar al usuario a quién desea enviar los archivos.
6. Verificar si el usuario ingresado es válido.
7. Obtener el índice del usuario seleccionado.
8. Verificar si el índice fue encontrado.
9. Obtener las configuraciones correspondientes para el usuario seleccionado.
10. Buscar los archivos de respaldo específicos para el usuario seleccionado.
11. Verificar si se han encontrado archivos de respaldo.
12. Verificar si el destino está accesible.
13. Bucle para enviar los archivos de respaldo.

```
#!/bin/bash

# Configuración
USUARIOS_ORIGEN=("hugo" "cliente")  # Lista de usuarios en diferentes ordenadores
IPS_ORIGEN=("192.168.6.10" "192.168.6.11")  # IPs de los ordenadores remotos
CARPETAS_ORIGEN=("/home/hugo/origen" "/home/cliente/origen")  # Rutas de las carpetas a copiar
CARPETA_DESTINO="/home/hugo/buckup-all/destino"  # Se guardará en el equipo local
CARPETA_TEMP="/tmp/backup_encrypt"
SCRIPT_DIR="$(dirname "$(realpath "$0")")"  # Obtiene la ruta del script
LOG_DIR="$SCRIPT_DIR/logs"
TIMESTAMP="$(date '+%H.%M_%d-%m-%Y')"  # Formato de fecha y hora
LOG_FILE="$LOG_DIR/backup_$TIMESTAMP.log"
CLAVE_CIFRADO="alumno"

# Crear carpeta de logs si no existe
mkdir -p "$LOG_DIR"

# Redirigir salida estándar y errores al archivo de log
exec >> "$LOG_FILE" 2>&1

echo "[$(date)] - Iniciando respaldo remoto con cifrado..."

# Verificar que las listas de usuarios, IPs y carpetas tengan la misma cantidad de elementos
if [ ${#USUARIOS_ORIGEN[@]} -ne ${#IPS_ORIGEN[@]} ] || [ ${#USUARIOS_ORIGEN[@]} -ne ${#CARPETAS_ORIGEN[@]} ]; then
    echo "[$(date)] - Error: Las listas de usuarios, IPs y carpetas de origen deben tener la misma cantidad de elementos."
    exit 1
fi

# Bucle para procesar cada origen
for i in "${!USUARIOS_ORIGEN[@]}"; do
    USUARIO_ORIGEN="${USUARIOS_ORIGEN[$i]}"
    IP_ORIGEN="${IPS_ORIGEN[$i]}"
    CARPETA_ORIGEN="${CARPETAS_ORIGEN[$i]}"

    echo "[$(date)] - Conectando a $USUARIO_ORIGEN@$IP_ORIGEN..."
    
    # Verificar conexión SSH con el equipo remoto
    if ! nc -z "$IP_ORIGEN" 22; then
        echo "[$(date)] - Error: No se puede conectar a $IP_ORIGEN en el puerto 22."
        continue  # Continuar con el siguiente origen si no se puede conectar
    fi

    # Crear carpeta temporal para los archivos cifrados
    mkdir -p "$CARPETA_TEMP"

    # Copiar archivos desde el equipo remoto
    echo "[$(date)] - Descargando archivos desde el servidor remoto $IP_ORIGEN..."
    if rsync -avz -e "ssh -p 22" "$USUARIO_ORIGEN@$IP_ORIGEN:$CARPETA_ORIGEN/" "$CARPETA_TEMP/"; then
        echo "[$(date)] - Archivos descargados con éxito desde $IP_ORIGEN."
    else
        echo "[$(date)] - Error: Fallo en la sincronización con rsync desde $IP_ORIGEN."
        rm -rf "$CARPETA_TEMP"
        continue  # Continuar con el siguiente origen si rsync falla
    fi

    # Crear carpeta específica para el usuario en el destino
    USUARIO_DESTINO="$CARPETA_DESTINO/$USUARIO_ORIGEN"
    mkdir -p "$USUARIO_DESTINO"

    # Gestionar el número máximo de copias (3)
    echo "[$(date)] - Verificando copias anteriores en $USUARIO_DESTINO..."
    ARCHIVOS_ANTIGUOS=($(ls -t $USUARIO_DESTINO/backup_${USUARIO_ORIGEN}_*.tar.gz.gpg))
    NUM_COPIAS=${#ARCHIVOS_ANTIGUOS[@]}
    
    if [ $NUM_COPIAS -ge 3 ]; then
        # Eliminar las copias más antiguas (mantener solo las 2 más recientes)
        ARCHIVOS_A_ELIMINAR=("${ARCHIVOS_ANTIGUOS[@]:2}")
        echo "[$(date)] - Eliminando copias antiguas: ${ARCHIVOS_A_ELIMINAR[@]}"
        rm -f "${ARCHIVOS_A_ELIMINAR[@]}"
    fi

    # Cifrar archivos manteniendo la estructura original
    echo "[$(date)] - Cifrando archivos descargados desde $IP_ORIGEN..."
    tar -czf - -C "$CARPETA_TEMP" . | \
    gpg --symmetric --cipher-algo AES256 --passphrase "$CLAVE_CIFRADO" --batch -o "$USUARIO_DESTINO/backup_${USUARIO_ORIGEN}_${TIMESTAMP}.tar.gz.gpg"

    if [ $? -eq 0 ]; then
        echo "[$(date)] - Respaldo cifrado de $USUARIO_ORIGEN almacenado en: $USUARIO_DESTINO/backup_${USUARIO_ORIGEN}_${TIMESTAMP}.tar.gz.gpg"
    else
        echo "[$(date)] - Error en el cifrado del respaldo desde $IP_ORIGEN."
    fi

    # Limpiar archivos temporales
    rm -rf "$CARPETA_TEMP"

done

# Instrucciones para descifrar
echo "[$(date)] - Para descifrar en este equipo, ejecutar:"
echo "  gpg --decrypt --passphrase \"$CLAVE_CIFRADO\" --batch $CARPETA_DESTINO/<usuario>/backup_<usuario>_<timestamp>.tar.gz.gpg | tar -xz -C $CARPETA_DESTINO/<usuario>"

echo "[$(date)] - Respaldo finalizado."
```

<br>


## Recuperación de las copias de seguridad
Hemos creado este script para transferir copias de seguridad cifradas (.tar.gz.gpg) desde una máquina local a un servidor remoto, asegurando que los respaldos sean enviados de manera segura y organizada. Su propósito es automatizar la transferencia de respaldos mientras se registran los eventos en un archivo de log para garantizar trazabilidad. A continuación, se describe brevemente cómo funciona.

1. Tenemos la configuración de los usuarios en los ordenes de destino, IPs, carpeta local donde esta respaldado, rutas en los ordenadores remotos, carpetas log, formato de la fecha y hora; y el archivo log.
2. Crear la carpeta de logs si no existe.
3. Redirigir la salida estándar y los errores al archivo de log.
4. Escribir en el log el inicio de la ejecución.
5. Preguntar al usuario a quién desea enviar los archivos.
6. Verificar si el usuario ingresado es válido.
7. Obtener el índice del usuario seleccionado.
8. Verificar si el índice fue encontrado.
9. Obtener las configuraciones correspondientes para el usuario seleccionado.
10. Buscar los archivos de respaldo específicos para el usuario seleccionado.
11. Verificar si se han encontrado archivos de respaldo.
12. Verificar si el destino está accesible.
13. Bucle para enviar los archivos de respaldo.

```
#!/bin/bash

# Configuración
USUARIOS_DESTINO=("hugo" "cliente")  # Usuarios en los ordenadores de destino
IPS_DESTINO=("192.168.6.10" "192.168.6.11")  # IPs de los ordenadores de destino
CARPETA_DESTINO_LOCAL="/home/hugo/buckup-all/destino"  # Carpeta local donde están los respaldos
CARPETA_DESTINO_REMOTO=("/home/hugo/recuperacion" "/home/cliente/recuperacion")  # Rutas en los ordenadores remotos
LOG_DIR="/home/hugo/buckup-all/logs-recup"  # Carpeta de logs
TIMESTAMP="$(date '+%H.%M_%d-%m-%Y')"  # Formato de fecha y hora
LOG_FILE="$LOG_DIR/transferencia_$TIMESTAMP.log"  # Archivo de log

# Crear la carpeta de logs si no existe
mkdir -p "$LOG_DIR"

# Redirigir la salida estándar y los errores al archivo de log
exec >> "$LOG_FILE" 2>&1

# Escribir en el log el inicio de la ejecución
echo "[$(date)] - Iniciando transferencia de respaldos."

# Preguntar al usuario a quién desea enviar los archivos
echo "[$(date)] - ¿A qué ordenador deseas enviar los archivos? (hugo/cliente)"
read -p "Escribe 'hugo' o 'cliente': " USUARIO_SELECCIONADO

# Verificar si el usuario ingresado es válido
if [[ ! " ${USUARIOS_DESTINO[@]} " =~ " ${USUARIO_SELECCIONADO} " ]]; then
    echo "[$(date)] - Error: Usuario '$USUARIO_SELECCIONADO' no válido. Selecciona entre 'hugo' o 'cliente'."
    exit 1
fi

# Obtener el índice del usuario seleccionado
INDEX=-1
for i in "${!USUARIOS_DESTINO[@]}"; do
    if [ "${USUARIOS_DESTINO[$i]}" == "$USUARIO_SELECCIONADO" ]; then
        INDEX=$i
        break
    fi
done

# Verificar si el índice fue encontrado
if [ $INDEX -eq -1 ]; then
    echo "[$(date)] - Error: No se encontró el índice del usuario seleccionado."
    exit 1
fi

# Obtener las configuraciones correspondientes para el usuario seleccionado
USUARIO_DESTINO="${USUARIOS_DESTINO[$INDEX]}"
IP_DESTINO="${IPS_DESTINO[$INDEX]}"
CARPETA_DESTINO_USUARIO="${CARPETA_DESTINO_REMOTO[$INDEX]}"

# Buscar los archivos de respaldo específicos para el usuario seleccionado
ARCHIVOS_ANTIGUOS=($(ls $CARPETA_DESTINO_LOCAL/$USUARIO_DESTINO/backup_*.tar.gz.gpg 2>/dev/null))

# Verificar si se han encontrado archivos de respaldo
if [ ${#ARCHIVOS_ANTIGUOS[@]} -eq 0 ]; then
    echo "[$(date)] - Error: No hay archivos de respaldo para enviar para el usuario $USUARIO_DESTINO en la carpeta $CARPETA_DESTINO_LOCAL/$USUARIO_DESTINO."
    exit 1
fi

# Verificar si el destino está accesible
echo "[$(date)] - Conectando a $USUARIO_DESTINO@$IP_DESTINO..."

if ! nc -z "$IP_DESTINO" 22; then
    echo "[$(date)] - Error: No se puede conectar a $IP_DESTINO en el puerto 22."
    exit 1
fi

# Bucle para enviar los archivos de respaldo
for archivo in "${ARCHIVOS_ANTIGUOS[@]}"; do
    echo "[$(date)] - Enviando archivo $archivo a $USUARIO_DESTINO@$IP_DESTINO:$CARPETA_DESTINO_USUARIO..."
    
    # Usar rsync para transferir el archivo de respaldo al destino remoto
    if rsync -avz -e "ssh -p 22" "$archivo" "$USUARIO_DESTINO@$IP_DESTINO:$CARPETA_DESTINO_USUARIO/"; then
        echo "[$(date)] - Archivo $archivo enviado exitosamente a $USUARIO_DESTINO@$IP_DESTINO."
    else
        echo "[$(date)] - Error al enviar el archivo $archivo a $USUARIO_DESTINO@$IP_DESTINO."
    fi
done

echo "[$(date)] - Transferencia de respaldos finalizada."

```
<br>


## Autenticación SSH sin Contraseña para un Script

Para evitar que el script solicite una contraseña al ejecutar los comandos SSH y rsync, debes configurar la autenticación sin contraseña mediante claves SSH.


### Generar una clave SSH en el cliente



```
ssh-keygen -t rsa -b 4096 -f ~/.ssh/id_rsa -N ""

```

Esto generará un par de claves:

* ~/.ssh/id_rsa (clave privada)
* ~/.ssh/id_rsa.pub (clave pública)



### Copiar la clave pública al servidor destino

Usa el siguiente comando para copiar automáticamente la clave pública al servidor:

```
ssh-copy-id hugo@192.168.6.10

```

Si no tienes ssh-copy-id, puedes hacerlo manualmente con:

```
cat ~/.ssh/id_rsa.pub | ssh hugo@192.168.6.10 "mkdir -p ~/.ssh && cat >> ~/.ssh/authorized_keys && chmod 600 ~/.ssh/authorized_keys"

```

### Verificar la autenticación sin contraseña

Prueba iniciar sesión en el servidor sin que te pida la contraseña:

```
ssh hugo@192.168.6.10

```
<br>
<br>


## Recibir las copias a la carpeta destino

El comando sudo chown -R hugo:hugo /home/hugo/buckup cambia el propietario y el grupo de todos los archivos y subdirectorios dentro de /home/hugo/buckup al usuario hugo

```
sudo chown -R hugo:hugo /home/hugo/buckup

```

* sudo: Ejecuta el comando con privilegios de superusuario.

* chown: Cambia el propietario de un archivo o directorio.

* -R: Aplica el cambio de propietario de forma recursiva (a todos los archivos y subdirectorios dentro de /home/hugo/buckup).

* hugo:hugo : Establece el usuario propietario como hugo y el grupo como hugo.

* /home/hugo/buckup: Especifica la carpeta a la que se aplicará el cambio.

<br>


Establece permisos de lectura, escritura y ejecución para el propietario, y solo lectura y ejecución para el grupo y otros usuarios en los archivos dentro de /home/hugo/destino.

```
sudo chmod -R 755 /home/hugo/destino

```

* sudo: Ejecuta el comando con privilegios de superusuario.

* chmod: Modifica los permisos de archivos o directorios.

* -R: Aplica el cambio de permisos recursivamente a todos los archivos y subdirectorios dentro del directorio.

* 755: Establece los permisos de lectura, escritura y ejecución para el propietario (7 = lectura, escritura y ejecución), y solo lectura y ejecución para el grupo y los otros usuarios (5 = lectura y ejecución).

* /home/hugo/destino: Especifica la ruta del directorio al cual se le aplican los permisos.


<br>
<br>


## Recibir las copias a la carpeta de recuperación

El comando sudo chown -R hugo:hugo /home/hugo/buckup cambia el propietario y el grupo de todos los archivos y subdirectorios dentro de /home/hugo/buckup al usuario hugo

```
sudo chown -R hugo:hugo /home/hugo/buckup

```

* sudo: Ejecuta el comando con privilegios de superusuario.

* chown: Cambia el propietario de un archivo o directorio.

* -R: Aplica el cambio de propietario de forma recursiva (a todos los archivos y subdirectorios dentro de /home/hugo/buckup).

* hugo:hugo : Establece el usuario propietario como hugo y el grupo como hugo.

* /home/hugo/buckup: Especifica la carpeta a la que se aplicará el cambio.

<br>
<br>


El comando sudo chmod -R u+w /home/hugo/buckup otorga permisos de escritura al usuario propietario en todos los archivos y subdirectorios dentro de /home/hugo/buckup, recursivamente.

```
sudo chmod -R u+w /home/hugo/buckup

```

* sudo: Ejecuta el comando con privilegios de superusuario.

* chmod: Modifica los permisos de archivos o directorios.

* -R: Aplica los cambios de permisos recursivamente.

* -u+w: Agrega permiso de escritura (+w) al usuario propietario (u).

* /home/hugo/buckup: Carpeta a la que se aplicará el cambio.


</details>
<br>



<details>
<summary>+----------🧱🔥 PFSense</summary>

# ¿Qué es PFSense?
Es una distribución de **FreeBSD** adaptada como **firewall** y **router**. Es de código abierto y se puede instalar en dispositivos físicos y virtuales.
Es sostenida comercialmente por **Electric Sheep Fencing LLC**, además de ser de código abierto.
pfSense proporciona funciones avanzadas de seguridad y networking, y es conocido por ser una solución de firewall de alto rendimiento. Ahora os mostraremos unas características que hemos encontrado.

* **Firewall avanzado:** Nos ofrece reglas de firewall que permite filtrar y controlar el tráfico de red de manera efectiva.
* **Enrutamiento:** Se puede utilizar como un router que nos proporciona funciones de enrutamiento avanzadas y permitiendo la conectividad entre redes.
* **VPN:** 
* **Proxy y filtrado web:** 
* **Balanceo de carga y redundancia:** 
* **Seguridad:** 
* **Interfaz gráfica:** 


Configuramos la interfaz de la dirección IP con la opción número 2, ahora te muestro los pasos que nos apareceran:
1. Nos preguntara si lo configuramos vía DHCP, hay que decir que no.
2. Añadimos la nueva dirección IP: 192.168.56.110
3. Nos preguntaran que mascara de subneteo utilizaremos: 24
4. Luego le damos al **ENTER**
5. Nos preguntara si queremos configurar una dirección IPv6 en la interfaz LAN. Le decimos que no y le volovemos a dar **ENTER**
6. Luego nos pregunta si queremos un DHCP en el servidor LAN, le decimos que si. Añadimos el inicio del rango de IP del cliente(192.168.56.150) y luego el final del rengo(192.168.56.160).





## Configuración de la interfaz WAN
La interfaz WAN se usa para conectarse a Internet. Normalmente, se configura con DHCP si el proveedor de servicios de Internet (ISP) asigna direcciones dinámicas, pero también puede ser estática.

1. Desde el menú principal, selecciona la opción
   
```
2) Set interface(s) IP address.
```

3. Selecciona la interfaz WAN, en este caso:

```
1 - WAN (em0 - dhcp)
```

3. Selecciona el tipo de configuración IP:

  * DHCP: Si el ISP asigna la IP automáticamente (opción recomendada para la mayoría).

  * Estática: Si tienes una IP fija proporcionada por tu ISP.

4. Si es IP estática, introduce:

  * Dirección IP (por ejemplo, **```192.168.1.2```**).

  * Máscara de subred (por ejemplo, **```255.255.255.0```**).

  * Puerta de enlace (IP del router del ISP, por ejemplo, ```192.168.1.1```).

5.¿Configurar IPv6?

  * Si tu ISP lo usa, puedes configurarlo o dejarlo en automático.

6. ¿Activar servidor DHCP en esta interfaz?

  * Para WAN, generalmente es No.

7. Confirmar y aplicar cambios.

<br>
<br>

## Configuración de la interfaz LAN
La interfaz LAN se usa para la red interna y suele tener una dirección IP estática.

1. Desde el menú principal, selecciona ```2) Set interface(s) IP address```.

2. Selecciona la interfaz LAN, en este caso:

```
2 - LAN (em1 - static)
```

3. Configura la IP de LAN, por ejemplo:

* Dirección IP: ```192.168.1.1``` (IP del router dentro de la red local).

* Máscara de subred: ```255.255.255.0```.

4. onfigurar IPv6:

   Puedes desactivarlo si no lo necesitas o usarlo si tu red lo soporta.

6. ¿Activar servidor DHCP en LAN?

* Sí (para que los dispositivos en la red obtengan IP automáticamente).

* Especifica un rango de IPs, por ejemplo:

  * Inicio: ```192.168.1.100```

  * Fin: ```192.168.1.200```

6. Confirmar y aplicar cambios.



![image](https://github.com/user-attachments/assets/b3f88415-07a5-4233-b5e2-9fdbbb605306)

<br>
<br>
<br>
<br>

Para poder entrar a **pfSense** en modo gráfico, tenemos que poner la dirección IP en el navegador de una máquina que esté conectada a la red LAN y que tenga el modo gráfico habilitado.

![image](https://github.com/user-attachments/assets/52450081-dc1d-4086-9f1c-1d48ce3d9e75)



Tendremos que activar el Kea DHCP que lo que hace es asignar direcciones IP dinámicamente, mejora rendimiento, permite configuraciones sin reinicio, soporta bases de datos externas y facilita administración remota mediante API. 
![image](https://github.com/user-attachments/assets/848e501c-bf3b-4d85-b0d3-725bb8bdb75e)

<br>
<br>

# Cómo activar OpenVPN

![imagen_2025-03-14_101252810-removebg-preview](https://github.com/user-attachments/assets/e9237aa2-1a9e-4c13-a7f4-1e6642275050)

## 1️⃣ Instalar OpenVPN (si no está instalado)

OpenVPN viene integrado en pfSense, pero si falta, instálalo desde:

🔹 System > Package Manager > Available Packages > Busca ```OpenVPN``` > Install

## 2️⃣ Configurar el Servidor OpenVPN en pfSense

1. Accede a la interfaz web de pfSense en ```https://192.168.1.1```

<br>

2. Ve a VPN > OpenVPN > Wizards

<br>

3. Selecciona el método de autenticación:

  * Local User Access (usuarios internos) o

  * LDAP/RADIUS (si usas autenticación externa)

<br>

4. Crear o usar una CA (Certificate Authority)

  * Si no tienes una CA, el asistente la generará.

  * Crea un certificado de servidor.

<br>

5. Configurar el servidor VPN:

  * Interfaz: ```WAN```

  * Protocolo: ```UDP``` o ```TCP``` (recomendado UDP)

  * Puerto: ```1194``` (puedes cambiarlo)

  * Tunnel Network: ```10.8.0.0/24``` (rango IP de la VPN)

  * Local Network: ```192.168.1.0/24``` (red interna)

  * Activar ```Redirect Gateway``` si quieres que todo el tráfico pase por la VPN

<br>

6. Configurar cifrado y seguridad:

  * Cipher: AES-256-CBC o AES-256-GCM

  * Auth Digest Algorithm: SHA256

  * TLS Authentication: Activar

<br>

7. Guardar y aplicar los cambios.

## 3️⃣ Crear reglas de Firewall para OpenVPN

1. Ve a Firewall > Rules > OpenVPN

<br>

2. Añade una regla:

  * Acción: ```Pass```

  * Protocolo: ```Any```

  * Fuente: ```OpenVPN```

  * Destino: ```Any```

  * Guardar y aplicar.

También, en Firewall > NAT, agrega una regla para permitir tráfico desde la VPN.



## 4️⃣ Crear Usuarios y Certificados

1.Ve a System > User Manager

<br>

2. Añade un usuario, activa "Certificate" y genera uno nuevo.

## 5️⃣ Exportar el perfil OpenVPN para clientes

1. Instala el paquete OpenVPN Client Export desde System > Package Manager.

<br>

2. Ve a VPN > OpenVPN > Client Export.

<br>

3. Descarga el archivo ```.ovpn``` para conectarte desde Windows, macOS, Linux o móviles.

## 6️⃣ Conectar un Cliente OpenVPN

* Instala OpenVPN Client en tu PC o móvil.

* Importa el archivo ```.ovpn``` y conéctate.


<br>
<br>
<br>
<br><br>
<br>
<br>
<br><br>
<br>
<br>
<br>






</details>

<br>

<details>
<summary>+----------🔐💻Cifrado de punto a punto</summary>

# Qué es el Cifrado punto a punto

El cifrado punto a punto (también conocido como cifrado end-to-end, o E2EE, por sus siglas en inglés) es un método de seguridad de comunicación que asegura que solo el emisor y el receptor de la información puedan leer los mensajes que se envían entre ellos.

![image](https://github.com/user-attachments/assets/45ede1e2-9629-4226-bec5-d94b1ac05ed3)

<br>

En este tipo de cifrado:

1️⃣ El emisor cifra el mensaje con una clave antes de enviarlo.

2️⃣ El mensaje cifrado se transmite a través de internet o cualquier otra red, pero incluso si alguien intercepta el mensaje, no podrá entenderlo, ya que no tiene la clave para descifrarlo.

3️⃣ El receptor usa su propia clave para descifrar el mensaje y leerlo.

Esto garantiza que, incluso si los servidores de la plataforma de comunicación son hackeados o las comunicaciones son interceptadas en el camino, los mensajes seguirán siendo privados y solo podrán ser leídos por las personas a quienes están destinados.

<br>

Ejemplos de aplicaciones que usan cifrado punto a punto:

* WhatsApp
* Signal
* Telegram (en chats secretos)
* iMessage

Este tipo de cifrado es muy popular porque ofrece un alto nivel de privacidad y seguridad, ya que ni siquiera los proveedores del servicio (como las plataformas de mensajería) tienen acceso a los contenidos de los mensajes.



</details>


</details>

<br>


<details>
  <summary>💾🍃 Base de Datos</summary>
  
# Mongo DB

## Qué es el Mongo DB

MongoDB es una base de datos NoSQL orientada a documentos, diseñada para manejar grandes volúmenes de datos de manera flexible y escalable. A diferencia de las bases de datos relacionales tradicionales (como MySQL o PostgreSQL), MongoDB no usa tablas ni filas, sino que almacena los datos en documentos JSON (BSON, específicamente).

![image](https://github.com/user-attachments/assets/7576c635-9443-4c87-a9fd-b5f92e74c768)



<br>

## 🔹 Principales Características de MongoDB
    
1️⃣ **Base de datos NoSQL**

  * No utiliza estructuras relacionales (tablas y filas).
  
  * En su lugar, almacena datos en documentos JSON dentro de colecciones.

<br>

2️⃣ **Flexible y escalable**

  * No necesita una estructura fija de datos (esquema flexible).
  
  * Puede escalar horizontalmente (añadiendo más servidores) con Sharding.

<br>

3️⃣ **Alto rendimiento**

* Soporta grandes volúmenes de datos con lecturas y escrituras rápidas.

<br>

4️⃣ **Soporte para consultas avanzadas**

* Puedes hacer consultas complejas con filtros, agregaciones y búsquedas avanzadas.

<br>

5️⃣ **Integración con múltiples lenguajes**

* Compatible con Python, JavaScript (Node.js), Java, PHP, etc.

<br>
<br>


## 🔹 Ejemplo de cómo funciona MongoDB

📌 Estructura de un documento en MongoDB (similar a un JSON):

```
{
  "_id": ObjectId("60d5f9f4f3a2a2b6c8e5a123"),
  "nombre": "Juan Pérez",
  "edad": 30,
  "ciudad": "Madrid",
  "hobbies": ["fútbol", "cine", "lectura"]
}
```
* Se almacena dentro de una colección (como una tabla en SQL).
* Cada documento puede tener una estructura diferente dentro de la misma colección.

<br>
<br>

## 🔹 Comparación con una Base de Datos Relacional (SQL)

![image](https://github.com/user-attachments/assets/58e22335-33ae-4e32-9479-8e75327e0e6f)

<br>
<br>

## 🔹 ¿Cuándo usar MongoDB?

✅ Cuando necesitas manejar grandes volúmenes de datos no estructurados.

✅ Para aplicaciones web y móviles con datos dinámicos y flexibles.

✅ Si buscas escalabilidad horizontal para manejar alto tráfico.

✅ Para Big Data, IoT y aplicaciones en tiempo real.


<br>
<br>

## 🔹 ¿Cuándo NO usar MongoDB?

❌ Si necesitas relaciones complejas entre datos (ej. ERP, banca).

❌ Cuando requieres transacciones ACID fuertes (ej. sistemas financieros).

❌ Si los datos son altamente estructurados y no cambian mucho.


<br>
<br>


## Nuestra BBDD

Esta es nuestra base de datos. A continuación, os mostraremos las colecciones que contiene y os explicaremos la función de cada una de ellas.

![image](https://github.com/user-attachments/assets/0be57b9c-2c76-4fc4-8aeb-04e71d1d4d93)


### Channels
En esta sección, almacenamos los canales disponibles en nuestra página web. Aquí podrás ver el nombre del canal, la fecha de creación, si es público o privado, su estado (activo o inactivo), quién lo creó y los miembros que forman parte de él.

![image](https://github.com/user-attachments/assets/2151207c-312c-47e4-8aaa-de496b998349)


### Files
Aquí almacenamos los archivos enviados entre usuarios. Podrás ver en qué canal se envió el archivo, la hora de envío y el tipo de archivo.

![image](https://github.com/user-attachments/assets/e2ef22cb-ca6b-412e-9a94-f1afa139f570)



### Messages
En esta sección se almacenan los mensajes enviados entre usuarios y en los canales. También se muestra la fecha en que se envió cada mensaje.

![image](https://github.com/user-attachments/assets/d6c36f84-5adf-4e20-9633-220c589c6e20)



### Private-Chats
En esta sección se encuentran los chats privados creados por los usuarios. Podrás ver los miembros de cada chat y los mensajes enviados en ellos.

![image](https://github.com/user-attachments/assets/4c1f7e9d-d832-43ed-bf88-e336d4bbcd4e)



### Users
Aquí almacenamos la información de los usuarios registrados en nuestra web. Puedes ver el nombre de usuario, correo electrónico, contraseña, estado, fecha de creación de la cuenta, última conexión, amigos y los usuarios que ha bloqueado.

![image](https://github.com/user-attachments/assets/1700c6c9-b171-4909-bfc9-7e5d47ac572e)

![image](https://github.com/user-attachments/assets/3ab81af1-90b3-46a8-9389-d80e080309ae)




<br>
<br>


## ¿Qué es lo que hemos hecho?





  
</details>




<br>

<details>
  <summary>🌐🔗💬 WebSocket</summary>

# WebSocket

<br>

## Qué es WebSocket

WebSocket es un protocolo de comunicación que proporciona un canal de comunicación bidireccional y persistente entre el cliente (por ejemplo, un navegador web) y un servidor. A diferencia de los métodos tradicionales de comunicación HTTP, donde cada solicitud del cliente al servidor crea una nueva conexión y debe cerrarse después de recibir la respuesta, WebSocket mantiene una conexión abierta, lo que permite que los datos se intercambien de manera continua sin necesidad de abrir nuevas conexiones.

![image](https://github.com/user-attachments/assets/02d4268b-ba83-4c6c-b205-21311c6c01ff)

<br>


## Características clave de WebSocket

1️⃣ Conexión persistente:

* ¿Qué significa? Una vez que se establece una conexión WebSocket entre el cliente y el servidor, esta se mantiene abierta durante todo el tiempo que sea necesario. No es como HTTP, que abre y cierra una conexión para cada solicitud. Esto mejora la eficiencia, ya que no es necesario realizar múltiples "handshakes" (intercambios de información para abrir y cerrar conexiones) constantemente.

* Beneficio: Permite que el servidor y el cliente se comuniquen continuamente sin la necesidad de establecer nuevas conexiones cada vez que haya algo que transmitir.


2️⃣ Comunicación bidireccional:

* ¿Qué significa? Ambos lados de la conexión (el cliente y el servidor) pueden enviar y recibir datos en cualquier momento. Mientras que en HTTP el cliente generalmente hace solicitudes y espera respuestas del servidor, en WebSocket, tanto el servidor como el cliente pueden enviar mensajes sin que uno tenga que esperar al otro.

* Beneficio: Esto es especialmente útil para aplicaciones que requieren una comunicación constante y sin interrupciones, como en chats o juegos en línea.


3️⃣ Baja latencia:

* ¿Qué significa? Dado que WebSocket mantiene una conexión abierta de manera persistente, los mensajes se pueden enviar y recibir sin la sobrecarga de establecer nuevas conexiones o esperar por respuestas del servidor. Esto reduce la latencia (el tiempo de espera entre enviar un mensaje y recibir una respuesta).

* Beneficio: Es ideal para aplicaciones en tiempo real donde los usuarios necesitan respuestas instantáneas, como en aplicaciones de mensajería o en plataformas de trading financiero.


4️⃣ Protocolo basado en TCP:

* ¿Qué significa? WebSocket se construye sobre el protocolo de transmisión TCP (Transmission Control Protocol), que es un protocolo confiable. Esto significa que los datos se transmiten de manera ordenada y garantizada. Si algún paquete de datos se pierde, TCP se encarga de reintentarlo hasta que se reciba correctamente.

* Beneficio: Da confiabilidad a las comunicaciones, asegurando que los mensajes lleguen de manera correcta y en el orden adecuado.

<br>

## Casos de uso comunes

1️⃣ Aplicaciones en tiempo real:

* Ejemplos: Chats en vivo, mensajería instantánea, aplicaciones colaborativas.

* ¿Por qué WebSocket? En estas aplicaciones, los usuarios esperan que los mensajes se reciban y se envíen de inmediato. Si se tuviera que abrir y cerrar una nueva conexión para cada mensaje, esto sería muy ineficiente. Con WebSocket, la conexión está siempre activa, permitiendo la transmisión instantánea de mensajes.


2️⃣ Juegos en línea:

* Ejemplos: Juegos multijugador, plataformas de juegos en tiempo real.

* ¿Por qué WebSocket? Los juegos multijugador en línea requieren que el servidor y los jugadores se comuniquen constantemente para actualizar el estado del juego en tiempo real. Con WebSocket, los eventos del juego (como el movimiento de los personajes, la puntuación, etc.) pueden ser enviados y recibidos de manera instantánea y continua sin la latencia de las solicitudes HTTP tradicionales.


3️⃣ Notificaciones en tiempo real:

* Ejemplos: Notificaciones de nuevos mensajes, alertas en aplicaciones, actualizaciones de noticias.

* ¿Por qué WebSocket? Las notificaciones que se actualizan constantemente, como los avisos en una red social o las alertas de sistemas, requieren un intercambio de datos en tiempo real. WebSocket permite que el servidor "emita" las notificaciones directamente a los clientes conectados, sin que el cliente tenga que hacer una solicitud constante al servidor.


4️⃣ Plataformas de trading en línea:

* Ejemplos: Mercados de acciones, criptomonedas.

* ¿Por qué WebSocket? En plataformas de trading, los precios de las acciones o las criptomonedas cambian rápidamente. Los traders necesitan información actualizada al instante para tomar decisiones informadas. WebSocket permite recibir actualizaciones de precios en tiempo real sin retrasos, lo que es crucial para una toma de decisiones ágil.


5️⃣ Aplicaciones de colaboración en tiempo real:

* Ejemplos: Google Docs, aplicaciones de edición compartida.

* ¿Por qué WebSocket? Cuando varios usuarios están colaborando en un mismo documento, los cambios deben ser reflejados en tiempo real para todos los participantes. WebSocket garantiza que los cambios de un usuario se envíen y reciban instantáneamente, manteniendo todos los participantes sincronizados.



</details>

<br>

<details>
  <summary>🖥️🌐💻 Servidor Web</summary>

# Qué es un Servidor de Web

Un servidor web es un software o sistema que se encarga de recibir, procesar y responder a las solicitudes que los navegadores web (o cualquier cliente HTTP) envían para acceder a los recursos alojados en un sitio web. Los recursos más comunes que maneja un servidor web son las páginas web, que generalmente están escritas en HTML, pero también puede servir otros tipos de contenido como imágenes, videos, archivos CSS, JavaScript y más.

Cuando un usuario ingresa una dirección web (URL) en su navegador, el navegador envía una solicitud HTTP al servidor web correspondiente. El servidor web luego procesa esa solicitud, recupera el archivo solicitado (por ejemplo, una página HTML) y lo envía de vuelta al navegador para que se muestre al usuario.

![image](https://github.com/user-attachments/assets/1e220d5f-dd4c-4ba5-969a-c6fc51c6eb69)

<br>

Los pasos básicos de funcionamiento de un servidor web son:

* Recepción de la solicitud: El navegador realiza una solicitud HTTP al servidor web, generalmente solicitando un archivo o recurso específico.

* Procesamiento de la solicitud: El servidor verifica la solicitud y, si es válida, busca el recurso solicitado (por ejemplo, una página HTML).

* Envío de la respuesta: Una vez que el recurso ha sido encontrado, el servidor web envía el archivo al navegador del usuario, que lo muestra en la pantalla.

Algunos ejemplos populares de servidores web son:

* Apache HTTP Server: Muy popular y ampliamente utilizado en entornos Linux.

* Nginx: Conocido por su alto rendimiento y eficiencia.

* Microsoft IIS: Utilizado principalmente en entornos Windows.

<br>
<br>
<br>

# Qué es un NGINX

NGINX es un servidor web de alto rendimiento, servidor proxy inverso y balanceador de carga muy utilizado en la infraestructura de Internet. Fue creado originalmente para ser un servidor web, pero con el tiempo ha evolucionado para ofrecer múltiples funcionalidades adicionales. Su principal ventaja es su capacidad para manejar un gran volumen de conexiones concurrentes de manera eficiente y con un bajo uso de recursos.

![Comandos-de-Nginx-que-usted-debe-saber-removebg-preview](https://github.com/user-attachments/assets/72dd8064-c11a-4840-92f3-c7218227b21c)

<br>

Algunas de las funciones más destacadas de NGINX incluyen:

* Servidor web: Sirve contenido estático (como archivos HTML, imágenes, videos) a los usuarios.

* Proxy inverso: Redirige las solicitudes de los usuarios a otros servidores (por ejemplo, servidores de aplicaciones), mejorando la seguridad y la carga de trabajo distribuida.

* Balanceador de carga: Distribuye el tráfico de red entre varios servidores para asegurar que ninguno de ellos se sobrecargue, mejorando la disponibilidad y la fiabilidad del sistema.

* Cacheo: Guarda en memoria las respuestas de servidores backend para reducir la carga y acelerar las respuestas a los usuarios.

  NGINX es conocido por su alta eficiencia y su capacidad para manejar miles de conexiones simultáneas con un uso mínimo de recursos, lo que lo convierte en una opción popular para aplicaciones web de alto tráfico.

  Es muy común encontrarlo en la infraestructura de empresas que gestionan aplicaciones web de gran escala.

<br>
<br>
<br>

# Los pasos para crear el Servidor Web con NGINX

## Paso 1: Actualizar los paquetes del sistema
Antes de instalar NGINX, es recomendable actualizar la lista de paquetes disponibles y los paquetes del sistema para asegurarse de que estamos trabajando con versiones recientes.
```
sudo apt update
sudo apt upgrade -y

```

## Paso 2: Instalar NGINX

Una vez actualizado el sistema, se puede instalar NGINX utilizando el gestor de paquetes apt:

```
sudo apt install nginx -y
```

## Paso 3: Verificar la instalación de NGINX
Una vez que la instalación haya finalizado, puedes verificar que NGINX se haya instalado correctamente ejecutando:

```
nginx -v
```



</details>

<br>

<details>
  <summary>🖥️🌐🔄 Servidor DNS</summary>

Un servidor DNS (Domain Name System) es un sistema que traduce los nombres de dominio (como www.ejemplo.com) en direcciones IP (como 192.168.1.1) que las computadoras usan para identificarse y comunicarse en una red, como Internet.

![image](https://github.com/user-attachments/assets/f216feb9-9c30-4a78-bf23-e86f54922e99)

<br>

Cuando escribes una dirección web en tu navegador, el servidor DNS se encarga de buscar la dirección IP correspondiente a ese nombre de dominio para que puedas acceder al sitio web. Esto es necesario porque las computadoras y otros dispositivos en una red se identifican mediante direcciones IP, pero para los usuarios es mucho más fácil recordar nombres de dominio que números de IP.

En resumen, el servidor DNS actúa como una especie de "agenda telefónica" de Internet, ayudando a resolver los nombres de dominio en las direcciones numéricas necesarias para acceder a los recursos en línea.



</details>


<br>





<br><br><br>





















# Tema sobre la WEB

<details>
  <summary>🇹🇩 Chat</summary>
  
  # Chat Interface Concept
  
  https://codepen.io/emilcarlsson/pen/ZOQZaV
  
  ![image](https://github.com/user-attachments/assets/15b8bdd0-554e-4116-b73e-086db5766ed0)


  # 5 Живой чат / Live chat
  
  https://codepen.io/retyui/pen/zxGqPJ
  
  ![image](https://github.com/user-attachments/assets/12b26776-440e-474e-89f1-c7695ad79702)


  # Sidebar AdminLTE
  
  https://codepen.io/jasp402/pen/VrYzNw
  
  ![image](https://github.com/user-attachments/assets/bec42ba2-6cfc-4304-b220-cf128d50d4c9)


  # Material Messaging App Concept
  
  https://codepen.io/ThomasDaubenton/pen/QMqaBN
  
  ![image](https://github.com/user-attachments/assets/9b322906-8ead-4d2a-ba92-3e964af13b26)


  # Discord Mockup
  
  https://codepen.io/odensc/pen/vxpMPp
  
  ![image](https://github.com/user-attachments/assets/3d085bc8-4ab1-4b66-8061-8894e0c203a2)


</details>
<br>



<details>
  <summary>📧 Enviar email a la empresa</summary>
  
  # Responsive Contact Form
  
  https://codepen.io/wgnr/pen/ExKzNJ

  ![image](https://github.com/user-attachments/assets/5a7ec21a-ad85-4233-a0f6-54e7b55af226)


  

  ##



</details>
<br>



<details>
  <summary>📝|▶️ Registrar | Inicio</summary>
  
  # Responsive Registration Form
  
  https://codepen.io/anandaprojapati/pen/GmrwYE

  ![image](https://github.com/user-attachments/assets/29bfc20d-0d2a-4ef1-bdfb-7d361b2c3ae3)


  #



</details>
<br>




<details>
  <summary>🎨 Diseños graficos</summary>
  
  # 🔲 H Y P E R H E D R O N 🔲

  https://codepen.io/shshaw/pen/eGYZOe

  ![image](https://github.com/user-attachments/assets/1455a975-41b5-4e03-9d98-42e1d57146c8)



  # canvas base typeface

  https://codepen.io/ara_node/pen/DdNQqQ

  ![image](https://github.com/user-attachments/assets/5793e444-87d7-40be-80b9-172d0b93ea7d)


  # #Anonymous Hacker Portfolio

  https://codepen.io/Breekee/pen/QWjjdOQ
  
  ![image](https://github.com/user-attachments/assets/2443b86b-ee03-4f8a-92f5-4db8135efbd1)


  # Text Glitch

  https://codepen.io/alexr4/pen/BqVbLr

  ![image](https://github.com/user-attachments/assets/567ab563-e313-4e3b-9283-8133a3e4bfb2)


  #

</details>
<br>



