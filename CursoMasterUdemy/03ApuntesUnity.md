# 3 Gestión y Creación de Assets UNITY

## Funcionamiento de escenas

- Las escenas sirven para poder fragmentar el juego en partes
    - A lo largo de pasar por las escenas podamos cargar una y destruir la otra
- Cuando se le da al play carga una escena y la ejecuta (la pone en funcionamiento)
- SOLO HAY UNA ESCENA EN FUNCIONAMIENTO
- Cuando una escena es muy larga/pesada yo puedo indicarle a Unity que cuando cargue la escena anterior vaya cargando esta otra escena
    - En paralelo en el background la carga y la almacena, no va a necesitar cargarla
- Otra estrategia es tener una escena que diga "cargando..." y cada vez que cambio de nivel la llamo
---

## Gestión de escenas

- Con la ruedita del ratón sobre los iconos de las escenas los agranda
- Doble clic y abre la escena
- Hay un editor multi escenas que permite tener varias escenas abiertas y facilita las cosas para no tener que estar abriendo y cerrando las escenas para pasar información de unas a otras
- Cada vez que yo creo una escena Unity crea un archivio con ese nombre .unity
- Tanto los gameObjects que son perennes en la escena como los que se crean (y destruyen) en tiempo de ejecución están dentro de la escena
- Cuando borro una escena NO HAY VUELTA ATRÁS
- Ctrl + D las duplica, puedo seleccionar varias y borrarlas, etc
- Puedo crear una escena sin camara ni luz ( totalmente vacía ) con Ctrl + N y elegir empty
    - Esta escena no está todavía en el disco duro, usar Save as...
- Esto es todo lo que contienen las escenas, no hay más

----

## Plantillas de escenas

- Puedo crear mi propia plantilla
- Puedo crear una plantilla desde cero o a partir de una escena
- Con la escena cargada en el menú File/Save as Template...
    - Cuando la abro en el inspector me indica que escena tiene como referencia la plantilla
    - Se le puede poner un titulo y descripción
    - Para que salga una imagen del previo antes de cargar la plantilla, se hace en el inspector Thumbnail/ Snapshot/View/Main Camera
        - Seleccionar la vista del juego y Take a SnapShot
        - En Texture cambio la imagen
- Puedo usar Create Scene Template para crear una plantilla desde cero, desde clic derecho Scene
- Cada vez que diga File/New aparecerá en el menú
----

## Edición de múltiples escenas

- Puedo arrastrar la segunda escena a la jerarquía para abrirla simultáneamente
- Tengo que definir la escena activa. Puedo hacerlo desde el menú de los tres puntitos Set Active Scene
- Tengo tambien load/unload scene, remove scene
- Al tener dos escenas abiertas, visualizo lo que hay en las dos escenas. Puedo usar el unload para dejar de visualizar una de ellas
---

## Selección de escenas en Build Settings

- File/Build Settings
    - Me permite seleccionar las escenas que quiero construir. Arrastrando. 
    - Add Open Scene añade la sesión abierta
    - El checkbox, si lo desmarco no la cargará en la construcción
    - Para mover las escenas de la lista, seleccionar y arrastrar
----

## GameObjects

- Permiten conectar  con los assets que estoy trabajando
    - Imagen, textura, script, y quiero que esté dentro de la escena si o si va a tener que estar asociado a un GameObject
    - Definen sus propiedades a través de componentes a través de los cuales se pueden conectar con los assets
    - Por lo tanto, para conectar los GameObjects con los Assets se usarán componentes
- Todos los GameObjects tienen un componente GameObject (El nombre, la etiqueta y el Layout en el inspector)
    - Y todos tienen el componente Transform (Position, Rotation, Scale en X,Y,Z)
- Si renderizo un cubo, veo que en el inspector también tiene el componente Mesh
    - También tiene el Mesh Renderer con materiales, luces
    - También tiene el box collider
- Por ejemplo, si creo un GameObject de Audio, el componente Audio Source es lo que me va a permitir conectarlo con un Asset de sonido
- Puedo crear un GameObject cubo desde cero
    - Creo un GameObject vacío
    - Le añado MeshFilter, que sirve para conectar con las mallas 3D y selecciono el cubo como malla ( Unity viene con las geometrias básicas pre-cargadas)
    - Con el Mesh renderer lo traigo a la escena
    - Le falta el material, por eso se ve lila. En la ocpión Materials selecciono DefaultMaterial
    - Para que sea como el cube que viene preconfigurado en Unity le falta el componente Box Collider
- GameObjects también provee de elementos para la UI como bótones
- También provée de cámaras
- GameObjects es todo lo que va a estar dentro de una escena
-----

## Flujo de trabajo entre componentes

- Seleccionar el GameObject en la jerarquía y luego añadir el componente desde el menú, o desde el Add Component en el inspector
- Todos los componentes tienen un botón de ayuda que te lleva directo a la documentación de Unity, se puede traducir al español
- Puedo guardar las propiedades de transform en un preset con el botón de al lado del Help, Save Preset, botón Save Current To
- Después tengo los tres puntitos que me despliega un menú
    - Reset, Copy Component / Paste Component, Paste Component Values (para pegar los valores de las propiedades de un componente a otro)
    - Puedo desplegar las propiedades en una ventana nueva con Properties
    - Move Up, Move Down para moverlos (excepto los dos primeros, el resto los puedo mover con excepciones)
    - Remove Component
    - etc.
----

## Tipos de datos de componentes

- Los checkbocks son booleans al fin y al cabo
- Hay propiedades que no están el editor a las que se accede por codigo
- Cajas numéricas, a veces con enteros, a veces con decimales
- A veces se puede elegir colores
- Color Pikers para elegir un color o el canal Alpha (transparencia)
- Sliders
- Selección de archivos/presets/mallas (icono redonda). En escena no se carga ninguna malla por defecto, están en Assets 
- En los de audio hay edición de curvas, en los de animación también
----

## Componentes más usados

- 

