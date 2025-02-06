# Introduccion a la instalación de la web

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










