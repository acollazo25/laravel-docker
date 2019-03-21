# Laravel - Docker

> ⚠ USE ONLY THIS REPOSITORY FOR DEVELOPMENT PURPOSE

## Install
Clone in root project directory.
```cmd
git clone https://github.com/acollazo25/laravel-docker.git
```

## Configure

### Configure laravel environment
Laravel project `.env` example
```dotenv
...
DB_CONNECTION=mysql
DB_HOST=db
DB_PORT=3306
DB_DATABASE=laravel
DB_USERNAME=root
DB_PASSWORD=secret
...
REDIS_HOST=redis
REDIS_PASSWORD=null
REDIS_PORT=6379
...
```

## Launch
Up container services
```cmd
docker-compose up -d
```
Open browser in http://localhost

### Configure nginx server
Copy `nginx/app.conf.example` to `nginx/app.conf`


## Laravel artisan CLI

### Move to laravel-docker directory
```cmd
cd laravel-docker
```

### Run migrations and seeders
```cmd
docker-compose run app php artisan migrate --seed
```

### Run tinker
```cmd
docker-compose run app php artisan tinker
```
