# Laravel - Docker

> ⚠ USE ONLY THIS REPOSITORY FOR DEVELOPMENT PURPOSE

## Laravel Compatibility
✔ Laravel 5.8 ✔ Laravel 5.7 ✔ Laravel 5.6

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
DB_USERNAME=laravel
DB_PASSWORD=secret
...
REDIS_HOST=redis
REDIS_PASSWORD=null
REDIS_PORT=6379
...
```

### Configure nginx server
Copy `nginx/app.conf.example` to `nginx/app.conf`

## Launch
Up container services
```cmd
cd laravel-docker
docker-compose up -d
```
Open browser in 🌐 http://localhost


## Laravel artisan CLI

### Move to laravel-docker directory
```cmd
cd laravel-docker
```

### Install dependencies
```cmd
docker-compose run --rm app composer install
```

### Run key generation
```cmd
docker-compose run --rm app php artisan key:generate
```

### Run storage link creation
```cmd
docker-compose run --rm app php artisan storage:link
```

### Run migrations and seeders
```cmd
docker-compose run --rm app php artisan migrate --seed
```

### Run tinker
```cmd
docker-compose run --rm app php artisan tinker
```
