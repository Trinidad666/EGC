taba columna

<br>
<br>
<br>
<br>
<br>


· identificacion que van ha ser identidades

· todos los datos que vamos a necesitar guardar.

· servicios que vamos a querer que necesiten backend

· guardar archivos de que tipo y cules
 
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>

# Usuarios
id_usuario
nombre_usuario
email
telefono
fecha_registro
estado
foto_perfil
fecha_ultimo_acceso


# Chats
id_chat
nombre_chat
tipo_chat
fecha_creacion

# Participantes
id_participante
id_usuario
id_chat
fecha_ingreso
fecha_salida

# Mensajes
id_mensaje
id_chat
id_usuario
contenido
tipo_mensaje
fecha_envio

# Archivos
id_archivo
id_mensaje
tipo_archivo
ruta_archivo
tamano_archivo

# Grupos
id_grupo
id_chat
id_administrador
descripcion
foto_grupo

# Notificaciones
id_notificacion
id_usuario
id_chat
tipo_notificacion
contenido
leido
fecha

# Configuración del Usuario
id_usuario
notificaciones
sonido_notificaciones
privacidad

# Bloqueos
id_bloqueo
id_usuario
id_usuario_bloqueado
fecha_bloqueo

# Llamadas
id_llamada
id_usuario_origen
id_usuario_destino
tipo_llamada
duracion
fecha_llamada
