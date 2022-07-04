# Laravel Dev Environment With Docker

## Initial Setup

### Create a yml file

```
touch docker-compose.yml
```

### Create a mysql directory

```
mkdir mysql
```

### create a dockerfile

```
touch Dockerfile
```

### create a nginx directory

```
mkdir nginx
```

### create a default.conf file under nginx directory

```
touch nginx/default.conf
```

### create a src directory

```
mkdir src
```

### create a public directory under src directory

```
cd src
```

```
mkdir public
```
### create a index.html file under src/public directory

```
cd ../../
```

```
touch src/public/index.html
```

#write your required dockerfile, service, volume etc

### Run docker compose

```
docker-compose bulid && docker-compose up -d
```
### remove public/index.htm file under src directory

```
cd src
```

```
rm -r public
```

### install laravel project root directory

```
composer create-project laravel/laravel .
```

### Migrate database by docker-compose
 
 ```
 cd ../
 ```

 ```
 docker-compose exec php php /var/www/html/artisan migrate
 ```

 ### down docker file

 ```
 docker-compose down
 ```
