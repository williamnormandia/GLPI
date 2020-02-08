# GLPI com Docker compose e dados persistentes

Este repositório com o docker compose necessário para executar o GLPI através de **Docker** em sua ultima versão.

## Procedimento

### Instlando o docker:

```bash
curl -fsSL https://get.docker.com | sh
```

### Instalando do docker-compose

```bash
curl -L https://github.com/docker/compose/releases/download/1.25.1/docker-compose-`uname -s`-`uname -m` -o /usr/local/bin/docker-compose
chmod +x /usr/local/bin/docker-compose
```

### Criando diretório para presistencia de dados e baixando o repositório

```bash
cd /opt 

git clone https://github.com/williamnormandia/GLPI.git

cd GLPI 

mkdir -p ./var/www/html/glpi \
         ./var/lib/mysql

chown 472:472 ./var/lib/mysql \
              ./var/lib/mysql 
```

### Executando os containers

```bash
docker-compose up -d
```
Para acesar o **GLPI** acesse http://<seu_ip> 