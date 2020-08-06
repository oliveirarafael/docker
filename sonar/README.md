# SonarQube

## Start

Dentro da pasta onde contém o **Docker Compose** do SonarQube execute o seguinte comando, ```docker-compose up```. Após a execução será criado os containeres do SonarQube e do PostgreSQL.

## Erro

ERROR: [1] bootstrap checks failed sonar | [1]: max virtual memory areas vm.max_map_count [65530] is too low, increase to at least [262144]

## Solução

### Linux

```
sysctl -w vm.max_map_count=262144
sysctl -w fs.file-max=65536
ulimit -n 65536
ulimit -u 4096
```

### Windows

Você pode encontrar a explicação dessa solução dentro da documentação no Docker Hub do SonarQube

## Docker Hub
https://hub.docker.com/_/sonarqube/

## Documentação
https://docs.sonarqube.org/latest/

