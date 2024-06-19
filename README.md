# ProjetoFinalDocker

## 1- Docker

1. Tenha docker e docker compose instalado em sua máquina.

## 2- Ambiente

1. ```bash
   mkdir ProjetoDocker
   cd ProjetoDocker
   ```
2. ```bash
   git clone https://github.com/heloshartmann/ProjetoFinalDocker.git
   ```
3. ```bash
   cd ProjetoFinalDocker
   ```
4. ```bash
    sudo docker-compose up -d
    ```

## 3- Projeto: WordPress

1. Acesse o WordPress na porta 8000 e termine sua configuração.
2. Após, instale e ative o plugin do Redis "Redis Object Cache".


### Editar arquivo wp-config.php

1. ```bash
    docker-compose exec wordpress bash
    ```

2.  ```bash
    apt-get update
    apt-get install nano
    ```

3. ```bash
    nano wp-config.php
    ```

4. ```php
    // Enable Redis Object Cache
    define('WP_CACHE', true);
    define('WP_REDIS_HOST', 'redis');
    define('WP_REDIS_PORT', 6379);
    ```

### Verificar Redis    

1. Nas configs do Redis, ative o cache de objetos.

## 4- Projeto: Prometheus

1. Acesse o Prometheus na porta 9090, vá em Status e Targets.