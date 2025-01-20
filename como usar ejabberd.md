# ¿Como usar Ejabberd?

**ejabberd** es un servidor de mensajería instantánea basado en el protocolo XMPP (Extensible Messaging and Presence Protocol). Para usar ejabberd sin necesidad de XAMPP, es necesario instalar ejabberd directamente en el sistema operativo de tu elección. XAMPP es un paquete que incluye Apache, MySQL, PHP, y otros componentes, pero no es necesario para ejecutar ejabberd, ya que ejabberd funciona por sí solo sin depender de estos componentes.

Aquí te explico cómo instalar y ejecutar ejabberd sin XAMPP:

### 1. **Instalar ejabberd**

La instalación de ejabberd varía según el sistema operativo que estés utilizando. Aquí te muestro cómo hacerlo en los sistemas más comunes.

#### En **Linux** (Debian/Ubuntu):
1. **Actualizar el sistema**:
   ```bash
   sudo apt update
   sudo apt upgrade
   ```

2. **Instalar ejabberd**:
   ```bash
   sudo apt install ejabberd
   ```

   Esto instalará ejabberd y sus dependencias necesarias.

#### En **Windows**:
1. Dirígete a la página oficial de [ejabberd](https://www.ejabberd.im/downloads) y descarga el instalador para Windows.
2. Ejecuta el instalador y sigue las instrucciones en pantalla.

#### En **macOS** (usando Homebrew):
1. **Instalar Homebrew** (si no lo tienes ya instalado):
   ```bash
   /bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
   ```

2. **Instalar ejabberd**:
   ```bash
   brew install ejabberd
   ```

### 2. **Configurar ejabberd**

Una vez instalado, debes configurar ejabberd. La configuración predeterminada es bastante básica, pero puedes personalizarla según tus necesidades.

1. **Archivo de configuración**:
   La configuración de ejabberd se encuentra en el archivo `ejabberd.yml`. En Linux, suele estar en el directorio `/etc/ejabberd/`, y en Windows se encuentra en el directorio de instalación.

2. **Modificar dominios y usuarios**:
   Puedes modificar el archivo `ejabberd.yml` para configurar tu dominio y otros parámetros como la autenticación, servicios, y módulos que quieras usar.

3. **Crear usuarios**:
   Ejabberd permite crear usuarios desde la línea de comandos con el siguiente comando:
   ```bash
   ejabberdctl register usuario tu_dominio contrasena
   ```

   Por ejemplo, para crear el usuario `juan` en el dominio `mi_servidor.com`, ejecutarías:
   ```bash
   ejabberdctl register juan mi_servidor.com contrasena
   ```

### 3. **Iniciar y detener ejabberd**

Para iniciar el servidor ejabberd:

- En **Linux** o **macOS**, puedes iniciar el servicio con:
  ```bash
  sudo service ejabberd start
  ```

  O si prefieres usar la línea de comandos directamente:
  ```bash
  ejabberdctl start
  ```

- En **Windows**, puedes iniciar ejabberd desde el menú de inicio o utilizando la línea de comandos en el directorio de instalación.

### 4. **Acceder a la interfaz de administración web**

ejabberd incluye una interfaz de administración basada en la web para gestionar el servidor y usuarios. El acceso por defecto es a través de:

```
http://localhost:5280/admin
```

Las credenciales predeterminadas son:
- Usuario: `admin`
- Contraseña: la que hayas definido durante la instalación.

### 5. **Usar el servidor ejabberd**

Una vez que ejabberd está en funcionamiento, puedes conectarte a tu servidor usando cualquier cliente XMPP (como Pidgin, Gajim, o Xabber) y autenticarte con el nombre de usuario y la contraseña que hayas creado.

### Conclusión

Ejabberd puede funcionar sin XAMPP porque no requiere de Apache, MySQL, ni PHP. Simplemente necesitas instalar ejabberd directamente, configurarlo adecuadamente, y luego usar clientes XMPP para conectarte al servidor. La instalación y configuración es sencilla y bien documentada, por lo que no deberías tener problemas para ponerlo en marcha sin necesidad de otros servidores o herramientas como XAMPP.<br>

## Enlaces de como usar Ejabberd con Websocket

#### Getting started with WebSocket API in ejabberd

https://www.process-one.net/blog/getting-started-with-websocket-api-in-ejabberd/

