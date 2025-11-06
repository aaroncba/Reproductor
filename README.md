# Proyecto Avance #1

## Introduccion al Proyecto

Este proyecto tiene como finalidad un mejor entendimiento de la programacion orientada a objetos. 

## ANÁLISIS DE ACTORES Y ENTIDADES DEL SISTEMA

1. DESCRIPCIÓN GENERAL DEL SISTEMA  
El sistema consiste en una página web enfocada en la gestión y reproducción de música.  
Permite la creación de usuarios, el manejo de listas de canciones favoritas, la visualización de videos musicales y la consulta de información detallada sobre canciones y álbumes.  
El sistema está diseñado bajo el paradigma de programación orientada a objetos (POO), utilizando una arquitectura cliente-servidor (frontend y backend) donde los usuarios interactúan mediante una interfaz gráfica.

2. ACTORES DEL SISTEMA

USUARIO  
El usuario es el principal actor del sistema.  
Representa a toda persona que interactúa con la página web para explorar música, crear su cuenta, y gestionar sus listas de reproducción.

Responsabilidades:  
- Registrarse e iniciar sesión en la plataforma.  
- Administrar su perfil personal.  
- Explorar canciones y álbumes disponibles.  
- Crear, modificar y eliminar canciones dentro de su lista de favoritos.  
- Reproducir música o videos.

Atributos principales:  
- idUsuario: Identificador único.  
- nombreUsuario: Nombre que usa dentro de la plataforma.  
- correo: Correo electrónico asociado a su cuenta.  
- fechaCreacion: Fecha en que se creó la cuenta.

Métodos relevantes:  
- login(): Inicia sesión del usuario.  
- logout(): Cierra sesión del usuario.  
- addFavorite(song): Agrega una canción a la lista de favoritos.  
- removeFavorite(song): Elimina una canción de la lista de favoritos.  
- getFavorites(): Devuelve la lista de canciones favoritas.

ADMINISTRADOR  
El administrador es un actor con privilegios avanzados dentro del sistema.  
Se encarga del mantenimiento y control del contenido multimedia y metadatos del sitio.

Responsabilidades:  
- Crear, editar y eliminar álbumes y canciones.  
- Administrar los metadatos y la información general del sitio.  
- Supervisar la integridad de los datos.

Atributos principales:  
- idAdmin: Identificador único.  
- username: Nombre del administrador.  
- rol: Nivel de permisos dentro del sistema.

Métodos relevantes:  
- createAlbum(): Crea un nuevo álbum.  
- updateAlbum(): Actualiza información de un álbum.  
- deleteAlbum(): Elimina un álbum (soft delete).  
- createSong(): Crea una nueva canción.

3. ENTIDADES DEL SISTEMA

ALBUM  
Representa una obra musical completa creada por un artista o banda.  
Un álbum contiene una colección de canciones y metadatos asociados.

Atributos principales:  
- idAlbum  
- titulo  
- artista  
- añoLanzamiento  
- listaCanciones (colección de objetos Cancion)

Métodos relevantes:  
- addSong(cancion)  
- removeSong(cancion)  
- getSongs()

CANCIÓN  
Entidad que representa una pista musical individual.  
Puede pertenecer a un álbum o existir de forma independiente.

Atributos principales:  
- idCancion  
- titulo  
- duracion  
- tamañoArchivo  
- creditos  
- año

REPRODUCTOR MULTIMEDIA  
Entidad que permite la reproducción de audio y video musical dentro del sistema.  
Brinda al usuario control sobre la reproducción y el volumen.

Métodos principales:  
- play(song)  
- pause()  
- stop()  
- seek(seconds)  
- setVolume(level)

4. SUGERENCIAS DE MEJORA O EXPANSIÓN

1. Agregar el actor “Artista” o “Banda”: Dado que se mencionan álbumes y canciones, podría modelarse un actor o entidad que represente al creador de la música (con atributos como nombre, país o género musical).  

2. Agregar relaciones entre entidades:  
   - Un álbum contiene varias canciones (1:N).  
   - Un usuario tiene muchas canciones favoritas (N:M entre usuario y canción).  
   - Un administrador puede gestionar múltiples álbumes y canciones.  

3. Incluir el concepto de “Lista de favoritos” como entidad: Representarla como una clase propia (ListaFavoritos) con sus métodos y relación con el usuario.  

4. Revisar nombres de métodos para seguir la notación camelCase y claridad en los tipos, por ejemplo:  
   - addFavorite(Song song)  
   - removeFavorite(Song song)  
   - createAlbum(Album album)  

5. Agregar una breve explicación sobre el uso del paradigma POO, mencionando conceptos como encapsulamiento, herencia (por ejemplo, Administrador podría heredar de Usuario) y polimorfismo (el reproductor puede comportarse distinto según el tipo de medio).




## Funciones 

* Al presionarse el boton "Limpiar el Modelo de Datos", esto hara un soft delete, el cual va a marcar ` show_model ` como ` False `. Por defecto sera definida como ` True `. 



## Modelo de Datos
* Para el modelo de datos, se utilizara la coma (,). La informacion dentro de el documento de tipo model va a tener que verse de la siguiente manera: 

``` 
id, email, author, name, album, genre, duration
01, jon@gmai.com.c, Jon, Song_1, album_1, Alternative Rock, 123 
```

## Diagramas

![imagen de diagrama UML](https://github.com/aaroncba/Reproductor/blob/main/Diagramas/Diagrama_UML_user_cancion.png)



## Complementos
![imagen de complemento](https://github.com/aaroncba/Reproductor/blob/main/imagenes%20de%20complemento/Informacion_complemento.png)


# Integrantes
| Integrante |  Numero de cuenta | Usuario de GitHub | 
| ----------- | :----------: | :--------: | 
| Aaron Isaac Colindres Barralaga | #20221002478 | [aaroncba](https://github.com/aaroncba) |
| Orlin Moises Munguia Salgado | #20231003372| [omscenz](https://github.com/omscenz) |
