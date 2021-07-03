## MongoDB comandos basicos

###### Crear una base de datos

```
use db_name
```

###### Listar las bases de datos

```
show dbs
```

###### Insertar un documento a la db

```
db.nombre_de_coleccion.insert({})
```

###### Listar colecciones

```
show collections
```

###### Eliminar una db

```
db.dropDatabase()
```

###### Crear una coleccion

```
db.createCollection("nombre")
```

###### Eliminar una coleccion

```
db.nombre_de_coleccion.drop()
```

###### Buscart todos los datos

```
  db.nombre_de_coleccion.find().pretty()
```

###### Buscart todos los datos con un limite

```
  db.nombre_de_coleccion.find().limit(valor)
```

###### Buscar un dato en particular

```
 db.nombre_de_coleccion.find({atributo : valor})
```

###### Buscar un dato en particular (devuelve el primer resultado)

```
db.nombre_de_coleccion.findOne({atributo : valor})
```

###### Ordenar una busqueda

```
db.nombre_de_coleccion.find({atributo : valor}).short({atributo:1})
```

###### Mostrar el numero de documentos

```
db.nombre_de_coleccion.count()
```

###### Actualizar un documento

```
db.nombre_de_coleccion.update({atributo_a_buscar : valor}, {objeto completo modificado})
```

###### Actualizar un documento sin escribir todo el objeto

```
db.nombre_de_coleccion.update({atributo_a_buscar : valor}, {$set:{atributo: valor}})
```

###### Insertar un objeto con el metodo set

```
db.nombre_de_coleccion.update({atributo_a_buscar : valor}, {$set:{atributo: valor}}, {upsert:true})
```

###### Incrementar un valor numerico

```
db.nombre_de_coleccion.update({atributo_a_buscar : valor}, {$inc:{atributo: incremento}})
```

###### Renombrar una propiedad en un documento

```
 db.nombre_de_coleccion.update({atributo_a_buscar : valor}, {$rename:{nombre_del_atributo: nuevo_nombre_del_atributo}})
```

###### Eliminar todos los documentos

```
 db.nombre_de_coleccion.remove()
```

###### Eliminar un documento

```
 db.nombre_de_coleccion.remove({atributo_a_buscar : valor})
```
