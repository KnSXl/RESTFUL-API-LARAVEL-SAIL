# RESTFUL-API-LARAVEL-SAIL

## Requisitos
- PHP 8.0 ou superior
- Composer
- WLS 2
- Docker instalado e em execução

## Passos

### 1. Clonar o Repositório
```
git clone https://github.com/KnSXl/RESTFUL-API-LARAVEL-SAIL.git
```

### 2. Acessar o Diretório do Repositório
```
cd RESTFUL-API-LARAVEL-SAIL
```

### 3. Instalar as Dependências
```
docker run --rm \
    -u "$(id -u):$(id -g)" \
    -v "$(pwd):/var/www/html" \
    -w /var/www/html \
    laravelsail/php84-composer:latest \
    composer install --ignore-platform-reqs
```

### 4. Iniciar os Containers
```
vendor/bin/sail up -d
```

### 5. Gerar o Arquivo `.env`
```
cp .env.example .env
```

### 6. Gerar a Chave de Acesso
```
vendor/bin/sail artisan key:generate
```

### 7. Executar as Migrações
```
vendor/bin/sail artisan migrate
```

## Acesso ao Projeto

### Projeto Laravel Sail
- [http://localhost](http://localhost)
- [http://127.0.0.1](http://127.0.0.1)

### Banco de Dados phpMyAdmin
- [http://localhost:8888](http://localhost:8888)
- [http://127.0.0.1:8888](http://127.0.0.1:8888)