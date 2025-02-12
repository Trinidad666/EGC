# Que es Scylla

ScyllaDB es una base de datos NoSQL increíblemente rápida y escalable para aplicaciones que hacen un uso intensivo de los datos y requieren un alto rendimiento y una baja latencia . Empresas como Comcast, Starbucks, Discord y Zillow confían en ella y es capaz de realizar millones de operaciones por segundo y escalar petabytes.


<br>
<br>
<br>
<br>
<br>
<br>

# Como instalarla

https://opensource.docs.scylladb.com/stable/getting-started/install-scylla/install-on-linux.html

Este conjunto de comandos sirve para agregar el repositorio de ScyllaDB a tu sistema Debian o Ubuntu, de modo que puedas instalar y actualizar ScyllaDB a través de apt (el gestor de paquetes).

<br>
<br>


## Crear un directorio para almacenar claves GPG:

Este comando crea el directorio /etc/apt/keyrings si no existe. Este directorio se usará para almacenar las claves GPG que permiten verificar la autenticidad del repositorio.

```
sudo mkdir -p /etc/apt/keyrings
```


## Importar la clave pública de ScyllaDB:

Aquí, se está utilizando GPG para descargar e importar la clave pública de ScyllaDB desde un servidor de claves (en este caso, keyserver.ubuntu.com). La clave a43e06657bac99e3 es necesaria para autenticar los paquetes provenientes del repositorio de ScyllaDB. Esta clave se guarda en el archivo /etc/apt/keyrings/scylladb.gpg.

```
sudo gpg --homedir /tmp --no-default-keyring --keyring /etc/apt/keyrings/scylladb.gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys a43e06657bac99e3

```

## Descargar el archivo de lista de repositorios de ScyllaDB:

Este comando usa wget para descargar el archivo de repositorio de ScyllaDB y lo guarda en el directorio /etc/apt/sources.list.d/. El archivo scylla.list contiene la URL del repositorio para instalar ScyllaDB versión 6.2.

```
sudo wget -O /etc/apt/sources.list.d/scylla.list http://downloads.scylladb.com/deb/debian/scylla-6.2.list
```


<br>
<br>


Este conjunto de comandos se utiliza para instalar ScyllaDB en tu sistema y gestionar su versión. Aquí te explico paso a paso lo que hace cada comando:

<br>


## Actualizar la lista de paquetes disponibles:

Este comando actualiza la lista de paquetes en tu sistema, obteniendo información actualizada de todos los repositorios configurados, incluido el de ScyllaDB que configuraste previamente. Es un paso necesario para asegurar que apt esté al tanto de las versiones más recientes disponibles para instalar.

```
sudo apt-get update
```


## Instalar ScyllaDB

Este comando instala la última versión oficial de ScyllaDB disponible en el repositorio que configuraste. El parámetro **-y** hace que la instalación proceda automáticamente sin pedir confirmación, lo que facilita la automatización del proceso.

```
sudo apt-get install -y scylla
```

## Ver todas las versiones disponibles de ScyllaDB:

Este comando lista todas las versiones de ScyllaDB que están disponibles en los repositorios. Te muestra la versión y la fecha de la actualización para que puedas decidir cuál deseas instalar.

```
apt-cache madison scylla
```

Ejemplo de salida del comando:

```
scylla | 5.2.3-0.20230608.ea08d409f155-1 | https://downloads.scylladb.com/downloads/scylla/deb/debian-ubuntu/scylladb-5.2 stable/main amd64 Packages
scylla | 5.2.2-0.20230521.9dd70a58c3f9-1 | https://downloads.scylladb.com/downloads/scylla/deb/debian-ubuntu/scylladb-5.2 stable/main amd64 Packages
scylla | 5.2.1-0.20230508.f1c45553bc29-1 | https://downloads.scylladb.com/downloads/scylla/deb/debian-ubuntu/scylladb-5.2 stable/main amd64 Packages
scylla | 5.2.0-0.20230427.429b696bbc1b-1 | https://downloads.scylladb.com/downloads/scylla/deb/debian-ubuntu/scylladb-5.2 stable/main amd64 Packages
```















