# docker-sonarqubesample
Projeto de exemplo SonarQube 
## Imagem SonarQube:
imagem utilizada
 ```
  image: sonarqube:10.6.0-community
 ```
Imagens recomendadas:
```
sonarqube:lts-community
sonarqube:community
```
para outras imagens ver mais em https://hub.docker.com/_/sonarqube

## Serviços criados

    SonarQube: Ferramenta para análise contínua de código.
    PostgreSQL: Banco de dados utilizado pelo SonarQube para armazenar dados.

## Variáveis de Ambiente

    SonarQube:
        SONAR_JDBC_URL: Especifica a URL de conexão JDBC para o banco de dados PostgreSQL.
        SONAR_JDBC_USERNAME: Define o nome de usuário para acessar o banco de dados.
        SONAR_JDBC_PASSWORD: Define a senha para acessar o banco de dados.

    PostgreSQL:
        POSTGRES_USER: Define o nome de usuário do banco de dados PostgreSQL.
        POSTGRES_PASSWORD: Define a senha do banco de dados PostgreSQL.

## Volumes

    sonar_data: Armazena dados do SonarQube de forma persistente.
    sonar_logs: Armazena logs do SonarQube de forma persistente.
    sonar_db: Armazena dados do banco de dados PostgreSQL de forma persistente.

Este arquivo configura a rede e volumes necessários para que o SonarQube e o PostgreSQL funcionem corretamente e persistam os dados.

# Executando a Criação do Projeto

Para criar e iniciar os serviços definidos no arquivo docker-compose.yaml, utilize o seguinte comando:
```
docker compose up -d
```

# Referências
Docker images Sonarqube: https://hub.docker.com/_/sonarqube

Docker images Sonarscanner cli: https://hub.docker.com/r/sonarsource/sonar-scanner-cli

Documentação Sonarqube : https://docs.sonarsource.com/sonarqube/latest/

Instalação SonarQube como Docker: https://docs.sonarsource.com/sonarqube/latest/setup-and-upgrade/install-the-server/installing-sonarqube-from-docker/

SonarScanner CLI: https://docs.sonarsource.com/sonarqube/latest/analyzing-source-code/scanners/sonarscanner/

