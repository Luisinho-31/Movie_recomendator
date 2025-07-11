# Movie_recomendator
## Modelo de aprendizaje no supervisado: Recomendador de peliculas
En este colab veremos como se muestran las recomendaciones de una pelicula basado en el modelo de Content-bases recommendatios System este es un modelo de ML no Supervisado

Este proyecto tiene la finalidad de dar aquellas peliculas similares o mas cercanas
en recomendaciones y generos de pelicula

## Herramientas
Para este proyecto se utilizaron las siguientes herramientas y librerias
Python
-Pandas
-Numpy
-Matplotlib
-Google 
-Sklearn
-Kaggle

## fuente de datos:
https://www.kaggle.com/datasets/tmdb/tmdb-movie-metadata

## Objetivo:

El objetivo de este pryecto es realizar un modelo para recomendar peliculas similares 
a quella que buscas tomando caracteristicas similares, entre recomendacion y generos 

## Proceso
El proyecto se realizó en un colab de google, los primero pasos fue hacer una unión
entre dos datasets que se tenian, donde la llave de relación es el id de la pelicula, 
se realizó una exploración de datos revisando si existen valores nulos o ceros en aquellas
columnas que son de nuestro interes, continuando solamente nos quedamos con las columnas
a trabajar, en este caso solo nos quedamos con genero, id, descripción, titulo, entre otras 
se eliminan las stop words de nuestra columna de reseña para que nos de palabras mas especificas
o quite palabras que nos hacen ruido y no aportan nada, se usa el coseno para medir la disancia de 
similitud entre un registro y otro, usando cosine_similarity, ya obteniendo los valores 
se realizó una funcion donde te regresa los valores mas cercanos a la pelicula que le pones 
y la cantidad de registros que deseas

### Posible Salida
recomendar_peliculas('Kung Fu Panda 2', 10)

| title                        | generos_str                                            |
|------------------------------|--------------------------------------------------------|
| Kung Fu Panda                | Adventure, Animation, Family, Comedy                   |
| Legend of a Rabbit           | Animation, Family, Action, Adventure, Comedy           |
| Kung Fu Hustle               | Action, Comedy, Crime, Fantasy                         |
| Bulletproof Monk             | Action, Comedy, Fantasy                                |
| Kickboxer: Vengeance         | Action, Drama                                          |
| Kung Fu Panda 3              | Action, Adventure, Animation, Comedy, Family           |
| Kung Pow: Enter the Fist     | Action, Comedy                                         |
| The Forbidden Kingdom        | Action, Adventure, Fantasy                             |
| 2046                         | Fantasy, Drama, Science Fiction, Romance               |
| The Hadza: Last of the First | Documentary                                            |


## Autor
Luis Fernando Castillo https://github.com/Luisinho-31
