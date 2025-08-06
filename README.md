
# Setup Docker Laravel 11 com PHP 8.3
[Conheça a Codespace!](https://codespace.it.ao)

### Passo a passo
Clone Repositório
```sh
git clone -b laravel-12-with-php8.4 https://github.com/codespace-ao/laravel-base.git app-laravel
```
```sh
cd app-laravel
```

Suba os containers do projeto
```sh
docker-compose up -d
```


Crie o Arquivo .env
```sh
cp .env.example .env
```

Acesse o container app
```sh
docker-compose exec app bash
```


Instale as dependências do projeto
```sh
composer install
```

Gere a key do projeto Laravel
```sh
php artisan key:generate
```

OPCIONAL: Gere o banco SQLite (caso não use o banco PostgreSql)
```sh
touch database/database.sqlite
```

Rodar as migrations
```sh
php artisan migrate
```

Acesse o projeto
[http://localhost:8000](http://localhost:8000)
