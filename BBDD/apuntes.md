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
============================================================================
Almacena la información básica de cada usuario, como nombre, correo electrónico y número de teléfono.
============================================================================
id_usuario

nombre_usuario

email

telefono

fecha_registro

estado

foto_perfil

fecha_ultimo_acceso


<br>


# Chats

============================================================================
Registra los diferentes chats, ya sean individuales o grupales, incluyendo detalles como el nombre del chat y su tipo.
============================================================================

id_chat

nombre_chat

tipo_chat

fecha_creacion


<br>


# Participantes

============================================================================
Mantiene un registro de qué usuarios participan en cada chat, indicando su fecha de ingreso y salida.
============================================================================

id_participante

id_usuario

id_chat

fecha_ingreso

fecha_salida


<br>


# Mensajes

============================================================================
Contiene los mensajes enviados en los chats, incluyendo el contenido, tipo de mensaje y fecha de envío.
============================================================================

id_mensaje

id_chat

id_usuario

contenido

tipo_mensaje

fecha_envio


<br>


# Archivos

============================================================================
Almacena información sobre los archivos adjuntos en los mensajes, como imágenes, videos o documentos.
============================================================================

id_archivo

id_mensaje

tipo_archivo

ruta_archivo

tamano_archivo


<br>


# Grupos

============================================================================
Guarda detalles específicos de los chats grupales, como el administrador del grupo y su descripción.
============================================================================

id_grupo

id_chat

id_administrador

descripcion

foto_grupo


<br>


# Notificaciones

============================================================================
Registra las notificaciones enviadas a los usuarios, indicando el tipo de notificación y su contenido.
============================================================================

id_notificacion

id_usuario

id_chat

tipo_notificacion

contenido

leido

fecha


<br>


# Configuración del Usuario

============================================================================
Almacena las preferencias y configuraciones personales de cada usuario, como ajustes de privacidad y notificaciones.
============================================================================

id_usuario

notificaciones

sonido_notificaciones

privacidad


<br>


# Bloqueos

============================================================================
Lleva un registro de los usuarios que han sido bloqueados por otros usuarios, incluyendo la fecha del bloqueo.
============================================================================

id_bloqueo

id_usuario

id_usuario_bloqueado

fecha_bloqueo


<br>


# Llamadas

============================================================================
Registra información sobre las llamadas de voz o video realizadas entre usuarios, incluyendo la duración y fecha de la llamada.
============================================================================

id_llamada

id_usuario_origen

id_usuario_destino

tipo_llamada

duracion

fecha_llamada
