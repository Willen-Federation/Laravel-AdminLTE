# docker-laravel 🐳

## How to Start 

### Getting Started

#### Use on Make 
```bash
make for-linux-env # Linux environment only
make install
```

#### Manually 
```bash
docker compose build
docker compose up -d
docker compose exec app composer install
docker compose exec app cp .env.example .env
docker compose exec app php artisan key:generate
docker compose exec app php artisan storage:link
docker compose exec app chmod -R 777 storage bootstrap/cache
```

### Boot

```bash
docker-compose up -d
```
http://localhost[http://localhost]


## Container structures

```bash
├── app
├── web
└── db
```

### app container

- Base image
  - [php](https://hub.docker.com/_/php):8.3-fpm-bullseye
  - [composer](https://hub.docker.com/_/composer):2.7

### web container

- Base image
  - [nginx](https://hub.docker.com/_/nginx):1.26

### db container

- Base image
  - [mysql](https://hub.docker.com/_/mysql):8.4

### mailpit container

- Base image
  - [axllent/mailpit](https://hub.docker.com/r/axllent/mailpit)
