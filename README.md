# Microproyecto2
Microproyecto 2. Sistemas de información. 
MICRO-PROYECTO 2
	En una situación hipotética, usted es amigo de Eustaquio; Eustaquio es el presidente del club de Videojuegos y le gustaría hacer una página web para atraer más personas a su club.
	Eustaquio tiene un conjunto de requerimientos:
Cada club tiene un nombre, una descripción, y un listado de videojuegos.
Cada videojuego tiene un título, un género, una descripción.
Debe permitir a los usuarios tener acceso a listados de los juegos que ofrece dicho club.
Debe permitir a los usuarios hacer una búsqueda de todos los juegos del sistema.
Por temas de escalabilidad, un usuario puede ser creado sin un club inicialmente
Para ingresar a un club, deberá registrar una membresía (una afiliación o suscripción) en la base de datos para dicho club.
Dicho usuario debe tener, nombre y apellido, Username, email, contraseña y videojuego preferido
Un usuario deberá poder acceder a vista de su perfil para modificar su información sea nombre, apellido, videojuego preferido o retirarse de un club
El listado de la información de videojuegos y clubes será proporcionado desde el inicio y se deben precargar en la base de datos. Véase la última sección de este documento para los datos en formato JSON que se deben cargar.

REQUERIMIENTOS FUNCIONALES

Vista de registro:
Esta vista es importante ya que le permite al usuario entrar a la plataforma. Si el usuario no está registrado y no inicia sesión no puede acceder al listado de juegos disponibles, entonces esta página debe mostrar un formulario en donde el usuario ingrese sus datos personales tales como nombre, correo electrónico y contraseña para poder registrarse en la plataforma. Además, deben agregarse otros métodos de registro tales como Google, Twitter, etc.  (al menos uno). 
 
Vista de inicio de sesión: 
En esta vista se debe mostrar un formulario para que el usuario pueda entrar a la plataforma haciendo uso de correo electrónico y contraseña. Además deben agregarse otros métodos de autenticación tales como Google, Twitter, etc.

Vista de inicio (página principal): 
Esta página únicamente puede ser visitada cuando un usuario ha iniciado sesión correctamente, en caso de que alguien intente entrar a esta sección sin estar autenticado, se debe redirigir inmediatamente a la vista de inicio de sesión. 
Aquí el usuario debe encontrar el listado de los clubes.  Se debe mostrar al usuario los clubes de una forma agradable donde se pueda ver toda la información referente al mismo, incluyendo si el usuario ya está suscrito al club o no. Además, al dar click sobre un club, se debe redirigir al usuario hacia la página de detalles del mismo.

Vista detalles de un club: 
Esta página, al igual que la anterior, es privada. Únicamente puede mostrar el detalle de un club si hay un usuario autenticado.
Aquí se debe mostrar toda la información del club y se debe permitir, a través de un botón, que el usuario se suscriba (solicite una membresía) a dicho club. En caso de que el usuario ya esté registrado en el club, el botón pasa a ser un botón para retirarse del club.
Se deben mostrar los detalles de todos los juegos que incluye el club.

Vista de buscador: 
En esta sección el usuario debe encontrar una barra de búsqueda que le permita ingresar el nombre del juego que quiere buscar y al ejecutar la búsqueda, deben aparecer los juegos que coincidan con dicho criterio.

Registro de usuarios:
Los usuarios deben poder registrarse en la página web proporcionando su nombre, apellido, nombre de usuario, email, contraseña y videojuego preferido. El videojuego preferido debe ser uno de los registrados en base de datos.
La información del usuario debe almacenarse en la base de datos de Firebase Firestore.

Acceso a los juegos del club:
Los usuarios registrados deben poder acceder a los juegos que ofrece el club de videojuegos.
Se deben mostrar los juegos disponibles junto con su información, como nombre, género y descripción.

Gestión de clubes:
Los usuarios deben poder unirse a un club existente.
Para unirse a un club, un usuario debe solicitar una afiliación (membresía) entrando a la página del club y presionando el botón de suscripción.
La información de la membresía, relacionando el ID del club con el usuario, debe almacenarse en la base de datos.

Perfil de usuario:
Los usuarios deben poder acceder a su perfil para ver y modificar su información personal.
Deben poder editar su nombre, apellido y videojuego preferido.
Los usuarios deben poder retirarse de un club al que están afiliados.

Interfaz de usuario:
La aplicación debe tener una interfaz de usuario clara y fácil de usar.
La interfaz debe ser responsive, adaptándose a diferentes dispositivos como teléfonos móviles, tabletas y computadoras de escritorio.
Se debe utilizar React para estructurar el contenido de la aplicación, incluyendo formularios, tablas y elementos visuales.
Se deben aplicar estilos con CSS para hacer que la aplicación sea visualmente atractiva y coherente.
Se debe utilizar Firebase como plataforma de desarrollo y Firestore como base de datos para almacenar la información de los usuarios, clubes y membresías.
La aplicación debe ser capaz de leer y escribir datos en la base de datos de Firestore.


Datos Precargados
	Para ahorrar tiempo de desarrollo, se deben cargar estos datos iniciales sobre videojuegos y clubes manualmente en la base de datos, de modo que el sistema cuente con información para poder crear membresías.


Videojuegos

[
   {
     "ID": "1",
     "titulo": "The Witcher 3: Wild Hunt",
     "genero": "RPG",
     "descripcion": "Un épico juego de rol de mundo abierto con una trama envolvente y gráficos impresionantes."
   },
   {
     "ID": "2",
     "titulo": "Red Dead Redemption 2",
     "genero": "Acción/Aventura",
     "descripcion": "Un juego de vaqueros ambientado en el Salvaje Oeste con una narrativa profunda y un vasto mundo abierto."
   },
   {
     "ID": "3",
     "titulo": "The Legend of Zelda: Breath of the Wild",
     "genero": "Aventura",
     "descripcion": "Una aventura épica con un vasto mundo, rompecabezas desafiantes y una historia cautivadora."
   },
   {
     "ID": "4",
     "titulo": "Dark Souls III",
     "genero": "Acción/RPG",
     "descripcion": "Un juego desafiante con combates intensos y un mundo oscuro y misterioso."
   },
   {
     "ID": "5",
     "titulo": "Super Mario Odyssey",
     "genero": "Plataformas",
     "descripcion": "Una colorida aventura de plataformas con un fontanero saltarín y mundos imaginativos."
   },
   {
     "ID": "6",
     "titulo": "Overwatch",
     "genero": "FPS",
     "descripcion": "Un juego de disparos en equipo con héroes únicos y emocionantes partidas."
   },
   {
     "ID": "7",
     "titulo": "Minecraft",
     "genero": "Sandbox",
     "descripcion": "Un mundo abierto de construcción y exploración donde puedes crear tus propias aventuras."
   },
   {
     "ID": "8",
     "titulo": "Fortnite",
     "genero": "Battle Royale",
     "descripcion": "Un juego de supervivencia en línea con construcción y combates intensos."
   },
   {
     "ID": "9",
     "titulo": "FIFA 22",
     "genero": "Deportes",
     "descripcion": "El simulador de fútbol más popular con equipos reales y modos de juego variados."
   },
   {
     "ID": "10",
     "titulo": "Call of Duty: Warzone",
     "genero": "Battle Royale",
     "descripcion": "Un juego de disparos en línea con acción frenética y mapas enormes."
   },
   {
     "ID": "11",
     "titulo": "Assassin's Creed Valhalla",
     "genero": "Acción/Aventura",
     "descripcion": "Una aventura vikinga con combates, exploración y una historia intrigante."
   },
   {
     "ID": "12",
     "titulo": "Cyberpunk 2077",
     "genero": "RPG",
     "descripcion": "Un futuro distópico lleno de tecnología, crimen y decisiones morales."
   },
   {
     "ID": "13",
     "titulo": "Among Us",
     "genero": "Multijugador",
     "descripcion": "Un juego de engaño y deducción en el espacio con amigos o desconocidos."
   },
   {
     "ID": "14",
     "titulo": "Animal Crossing: New Horizons",
     "genero": "Simulación",
     "descripcion": "Una vida tranquila en una isla paradisíaca con actividades relajantes."
   },
   {
     "ID": "15",
     "titulo": "League of Legends",
     "genero": "MOBA",
     "descripcion": "Batallas estratégicas en línea con campeones y habilidades únicas."
   },
   {
     "ID": "16",
     "titulo": "Genshin Impact",
     "genero": "Acción/RPG",
     "descripcion": "Un mundo de fantasía con personajes elementales y una jugabilidad cautivadora."
   },
   {
     "ID": "17",
     "titulo": "Apex Legends",
     "genero": "Battle Royale",
     "descripcion": "Combates en equipo en un mundo futurista con héroes y habilidades únicas."
   },
   {
     "ID": "18",
     "titulo": "World of Warcraft",
     "genero": "MMORPG",
     "descripcion": "Un vasto mundo de fantasía con razas, clases y misiones épicas."
   },
   {
     "ID": "19",
     "titulo": "Control",
     "genero": "Acción/Aventura",
     "descripcion": "Explora una agencia secreta y descubre poderes sobrenaturales en este juego intrigante."
   },
   {
     "ID": "20",
     "titulo": "Hades",
     "genero": "Roguelike",
     "descripcion": "Embárcate en un viaje al inframundo y desafía a los dioses en este juego de acción y mitología."
   }
 ]



Clubes


[
   {
     "ID": "1",
     "nombre": "Club de Aventureros",
     "descripcion": "Explora lugares misteriosos y descubre tesoros ocultos con otros entusiastas de la aventura.",
     "videojuegos": ["1", "3", "11"]
   },
   {
     "ID": "2",
     "nombre": "Club de Estrategia",
     "descripcion": "Reúnete con estrategas brillantes para debatir tácticas, resolver enigmas y conquistar mundos virtuales.",
     "videojuegos": ["4", "15", "16"]
   },
   {
     "ID": "3",
     "nombre": "Club de Constructores",
     "descripcion": "Comparte tus creaciones en Minecraft, diseña estructuras asombrosas y colabora en proyectos épicos.",
     "videojuegos": ["7", "8", "14"]
   },
   {
     "ID": "4",
     "nombre": "Club de Fútbol Virtual",
     "descripcion": "Forma parte de un equipo virtual, compite en torneos y demuestra tus habilidades en FIFA 22.",
     "videojuegos": ["9", "10", "18"]
   },
   {
     "ID": "5",
     "nombre": "Club de Cazadores de Zombis",
     "descripcion": "Únete a otros supervivientes en la lucha contra hordas de no muertos en juegos como Left 4 Dead o Resident Evil.",
     "videojuegos": ["2", "13", "17"]
   }
 ]



