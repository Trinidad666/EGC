# Intoducción

<details>
  <summary>🚀 Eplicación de EGC</summary>
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
De momento este es nuestro esquema de nuestra web EGC:

![image](https://github.com/user-attachments/assets/d29a31b2-477b-47cb-b0c9-4ed494235236)

De momento este es nuestro esquema de la bbdd de EGC:

![image](https://github.com/user-attachments/assets/238fc073-fcfb-4ff9-98d6-5fb9bc589641)

</details>
<br>


<details>
<summary>📊 Diagrama de red</summary>

![image](https://github.com/user-attachments/assets/575cc38e-2fde-4cbe-a35d-f735b1ca5bf2)

</details>
<br>





<details>
<summary>🐋 Docker</summary>



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

  
- MySQL:

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
<summary>🐧 Sistems Operativos</summary>

Estos son los Sistemas Operativos que vamos a implementar en la Maquina virtuales.


- Ubuntu Server
  
- Alpine (Docker)

- Firewall


  
</details>
<br>




<details>
<summary>🔲 Hardware</summary>

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
<br>




<br><br><br>








# Tema sobre la WEB

<details>
  <summary>💬 Chat</summary>
  
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
  <summary>🔲 Diseños graficos</summary>
  
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



