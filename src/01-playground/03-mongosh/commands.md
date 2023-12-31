# Connect to container
```sh
docker-compose exec mongodb bash
```

# Connect with mongosh
```sh
mongosh "mongodb://admin:<password>@localhost:27017/?tls=false"
mongosh "mongodb+srv://admin:<password>@cluster0.nllndvg.mongodb.net/"
```

# mongosh common comands
```sh
show dbs
show collections

use('Platzi')
db.products.find()
```



# Exportar archivo csv a BD en MongoDB dentro de Docker

# Copiar archivos del Host al docker

```sh
docker cp D:\Documents\Cursos\MongoDB\Introducción\features-v1.csv introduccin-mongodb-1:/media

docker cp D:\Documents\Cursos\MongoDB\Introducción\python\routes_data.csv introduccin-mongodb-1:/media
```

```sh
docker-compose exec mongodb bash
```

# Importar las características y rutas de las imágenes
```sh
mongoimport --db clothes --collection features --type csv --headerline --file "/media/features-v1.csv" --username <username> --password <password> --authenticationDatabase <username>

mongoimport --db clothes --collection data --type csv --headerline --file "/media/routes_dataset.csv" --username <username> --password <password> --authenticationDatabase <username>
```