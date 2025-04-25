Práctica con el dataset sample_mflix de MongoDB 

Ejercicios propuestos y resultados: 

1. Número de películas lanzadas cada año 
Haz una consulta que muestre cuántas películas se lanzaron en cada año. 

```json
db.getCollection('movies').aggregate(
  [
    {
      $group: {
        _id: '$year',
        cantidadPeliculas: { $sum: 1 }
      }
    },
    { $sort: { _id: 1 } },
    {
      $project: {
        _id: 0,
        año: '$_id',
        cantidadPeliculas: 1
      }
    }
  ]
);
```

2. Calificación promedio de IMDb por género 
Encuentra la calificación promedio de IMDb para películas en cada género. 

```json
db.getCollection('movies').aggregate(
  [
    { $unwind: '$genres' },
    { $match: { 'imdb.rating': { $ne: null } } },
    {
      $group: {
        _id: '$genres',
        promedioRating: { $avg: '$imdb.rating' }
      }
    },
    { $sort: { promedioRating: -1 } },
    {
      $project: {
        _id: 0,
        genero: '$_id',
        promedioRating: {
          $round: ['$promedioRating', 2]
        }
      }
    }
  ],
  { maxTimeMS: 60000, allowDiskUse: true }
);

#################
RESULT:
#################

[
  { "genero": "Film-Noir", "promedioRating": 7.4 },
  { "genero": "Short", "promedioRating": 7.38 },
  { "genero": "Documentary", "promedioRating": 7.37 },
  { "genero": "News", "promedioRating": 7.25 },
  { "genero": "History", "promedioRating": 7.17 },
  { "genero": "War", "promedioRating": 7.13 },
  { "genero": "Biography", "promedioRating": 7.09 },
  { "genero": "Talk-Show", "promedioRating": 7.0 },
  { "genero": "Animation", "promedioRating": 6.9 },
  { "genero": "Music", "promedioRating": 6.88 },
  { "genero": "Western", "promedioRating": 6.82 },
  { "genero": "Drama", "promedioRating": 6.8 },
  { "genero": "Sport", "promedioRating": 6.75 },
  { "genero": "Crime", "promedioRating": 6.69 },
  { "genero": "Musical", "promedioRating": 6.67 },
  { "genero": "Romance", "promedioRating": 6.66 },
  { "genero": "Mystery", "promedioRating": 6.53 },
  { "genero": "Adventure", "promedioRating": 6.49 },
  { "genero": "Comedy", "promedioRating": 6.45 },
  { "genero": "Fantasy", "promedioRating": 6.38 },
  { "genero": "Action", "promedioRating": 6.35 },
  { "genero": "Family", "promedioRating": 6.33 },
  { "genero": "Thriller", "promedioRating": 6.3 },
  { "genero": "Sci-Fi", "promedioRating": 6.12 },
  { "genero": "Horror", "promedioRating": 5.78 }
]
```

3. Top 5 películas con más alta calificación en IMDb 
Lista las 5 películas con la calificación IMDb más alta. 

```json
db.getCollection('movies').aggregate(
  [
    { $match: { 'imdb.rating': { $ne: null } } },
    { $sort: { 'imdb.rating': -1 } },
    { $limit: 5 },
    {
      $project: {
        _id: 0,
        titulo: '$title',
        calificacionIMDb: '$imdb.rating',
        votos: '$imdb.votes'
      }
    }
  ]
);

#################
RESULT:
################# [
{
  "titulo": "The Danish Girl",
  "calificacionIMDb": "",
  "votos": ""
},
{
  "titulo": "Landet som icke èr",
  "calificacionIMDb": "",
  "votos": ""
},
{
  "titulo": "Scouts Guide to the Zombie Apocalypse",
  "calificacionIMDb": "",
  "votos": ""
},
{
  "titulo": "Catching the Sun",
  "calificacionIMDb": "",
  "votos": ""
},
{
  "titulo": "La nao capitana",
  "calificacionIMDb": "",
  "votos": ""
}
]
```

4. Número total de películas y duración promedio por director 
Determina el número total de películas y la duración promedio para cada director. 

```json
db.getCollection('movies').aggregate(
  [
    { $unwind: '$directors' },
    { $match: { runtime: { $ne: null } } },
    {
      $group: {
        _id: '$directors',
        cantidadPeliculas: { $sum: 1 },
        duracionPromedio: { $avg: '$runtime' }
      }
    },
    {
      $project: {
        _id: 0,
        director: '$_id',
        cantidadPeliculas: 1,
        duracionPromedio: {
          $round: ['$duracionPromedio', 2]
        }
      }
    },
    { $sort: { cantidadPeliculas: -1 } }
  ]
);

#################
RESULT:
#################

[{Multiples resultados}]


```

5. Distribución de películas por clasificación MPAA 
Encuentra la distribución de películas basadas en su clasificación MPAA. 

```json
db.getCollection('movies').aggregate(
  [
    {
      $match: {
        rated: { $exists: true, $ne: null }
      }
    },
    {
      $group: {
        _id: '$rated',
        cantidad: { $sum: 1 }
      }
    },
    {
      $project: {
        _id: 0,
        clasificacion: '$_id',
        cantidad: 1
      }
    },
    { $sort: { cantidad: -1 } }
  ],
  { maxTimeMS: 60000, allowDiskUse: true }
);

#################
RESULT:
#################
[
  {
    "clasificacion": "R",
    "cantidad": 5537
  },
  {
    "clasificacion": "PG-13",
    "cantidad": 2321
  },
  {
    "clasificacion": "PG",
    "cantidad": 1852
  },
  {
    "clasificacion": "APPROVED",
    "cantidad": 709
  },
  {
    "clasificacion": "G",
    "cantidad": 477
  },
  {
    "clasificacion": "PASSED",
    "cantidad": 181
  },
  {
    "clasificacion": "TV-14",
    "cantidad": 89
  },
  {
    "clasificacion": "TV-PG",
    "cantidad": 76
  },
  {
    "clasificacion": "TV-MA",
    "cantidad": 60
  },
  {
    "clasificacion": "TV-G",
    "cantidad": 59
  },
  {
    "clasificacion": "GP",
    "cantidad": 44
  },
  {
    "clasificacion": "M",
    "cantidad": 37
  },
  {
    "clasificacion": "Approved",
    "cantidad": 5
  },
  {
    "clasificacion": "TV-Y7",
    "cantidad": 3
  },
  {
    "clasificacion": "AO",
    "cantidad": 3
  },
  {
    "clasificacion": "Not Rated",
    "cantidad": 1
  },
  {
    "clasificacion": "OPEN",
    "cantidad": 1
  }
]
```
6. Top 3 países productores de películas 
Encuentra los 3 países que producen el mayor número de películas. 

```json
db.getCollection('movies').aggregate(
  [
    { $unwind: '$countries' },
    {
      $group: {
        _id: '$countries',
        cantidadPeliculas: { $sum: 1 }
      }
    },
    { $sort: { cantidadPeliculas: -1 } },
    { $limit: 3 },
    {
      $project: {
        _id: 0,
        pais: '$_id',
        cantidadPeliculas: 1
      }
    }
  ]
);

#################
RESULT:
#################
[
    {
    "cantidadPeliculas": 10921,
    "pais": "USA"
    },
    {
    "cantidadPeliculas": 2652,
    "pais": "UK"
    },
    {
    "cantidadPeliculas": 2647,
    "pais": "France"
    }
]
```
7. Número promedio de miembros del reparto para películas después del 2000 
Para películas lanzadas después del 2000, calcula el número promedio de miembros del reparto. 

```json
db.getCollection('movies').aggregate(
  [
    { $match: { year: { $gt: 2000 } } },
    {
      $project: {
        numCast: {
          $size: { $ifNull: ['$cast', []] }
        }
      }
    },
    {
      $group: {
        _id: null,
        promedioMiembrosReparto: {
          $avg: '$numCast'
        }
      }
    },
    {
      $project: {
        _id: 0,
        promedioMiembrosReparto: 1
      }
    }
  ]
);

#################
RESULT:
#################
[
    {
  "promedioMiembrosReparto": 3.8223223223223224
    }
]
```
8. Calificación promedio de IMDb y número de comentarios 
Determina la calificación promedio de IMDb para las películas y su respectivo número de 
comentarios. 

```json
db.getCollection('movies').aggregate(
  [
    {
      $lookup: {
        from: 'comments',
        localField: '_id',
        foreignField: 'movie_id',
        as: 'movie_comments'
      }
    },
    {
      $project: {
        title: 1,
        imdbRating: '$imdb.rating',
        numComments: { $size: '$movie_comments' }
      }
    }
  ]
);

#################
RESULT:
#################

[{Multiples resultados}]

```

9. Número total de películas comentadas por usuario 
Encuentra el número total de películas en las que cada usuario ha comentado. 

```json
db.getCollection('comments').aggregate(
  [
    {
      $group: {
        _id: '$email',
        totalMoviesCommented: { $count: {} }
      }
    },
    {
      $project: {
        _id: 0,
        email: '$_id',
        totalMoviesCommented: 1
      }
    }
  ]
);

#################
RESULT:
#################

[{Multiples resultados}]

```

10.  Películas del género "Western" con comentarios previos a 2020 
Encuentra películas del género "Western" y sus respectivos comentarios antes del "2020-
01-01". 

```json
db.getCollection('movies').aggregate(
  [
    { $match: { genres: 'Western' } },
    {
      $lookup: {
        from: 'comments',
        localField: '_id',
        foreignField: 'movie_id',
        as: 'comments'
      }
    },
    { $unwind: '$comments' },
    {
      $match: {
        'comments.date': {
          $lt: ISODate('2020-01-01T00:00:00.000Z')
        }
      }
    },
    { $project: { title: 1, comments: 1 } }
  ]
);

#################
RESULT:
#################

[{Multiples resultados}]

```