![Magento 2](https://cdn.rawgit.com/rafaelstz/magento2-snippets-visualstudio/master/images/icon.png)

#  Magento 2 Docker para desenvolvimento

### Apache 2.4 + PHP 7.1 + OPCache + MariaDB + N98 Magerun 2 + XDebug + Redis


### Requirementos

Instalar [Docker](https://docs.docker.com/engine/installation/linux/docker-ce/ubuntu/) e [Docker-compose](https://docs.docker.com/compose/install/#install-compose).

### Como usar

Clone os arquivos desse repositório:

```
git clone https://github.com/AGPDev/docker-magento23.git
```

Acesse a pasta após clonar:

```
cd docker-magento23
```

Inicialize os container:

```
./start
```

Clone o projeto do Magento 2.3:

```
git clone https://github.com/magento/magento2.git src
```

Faça a instalação das dependencias via composer:

```
./composer install
```

Após a configuração acesse a loja através do endereço: http://localhost/ e faça a instalação, no passo 2 adicione as configurações de conexão com o banco:

```
Host: db
Username: magento
Password: magento
Database Name: magento
```

Após a instalação coloque o Magento em modo desenvolvimento para poder as opções disponíveis:

```
./magento deploy:mode:set developer
```

O link do GraphQl é http://localhost/graphql

Para testar o GraphQl exitem algumas ferramentas uma delas é uma extensão para o Chrome:

[ChromeiQL](https://chrome.google.com/webstore/detail/chromeiql/fkkiamalmpiidkljmicmjfbieiclmeij)

### Paineis

**Web server:** http://localhost/

**PHPMyAdmin:** http://localhost:8080

**Local emails:** http://localhost:8025

### Comandos

| Comandos  | Descrição  | Opções & Exemplos   |
|---|---|---|
| `./start`  | Inicializar os containers | |
| `./stop`  | Parar os containers | |
| `./kill`  | Parar e remover os containers, networks, volumes, e imagens criadas do respectivo projeto | |
| `./shell`  | Acessar o container | `./shell root` |
| `./magento`  | Executar comandos do Magento CLI | |
| `./n98`  | Executar comandos do Magerun | |
| `./grunt-init`  | Preparar o Grunt para uso | |
| `./grunt`  | Usa Grunt especificando um tema ou em todos os temas. | `./grunt luma` |
| `./xdebug`  | Habilitar / Desabilitar o XDebug | |
| `./composer`  | Executar comandos do Composer | `./composer update` |
