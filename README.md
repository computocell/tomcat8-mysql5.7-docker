# A tomcat+mysql image
[![](https://images.microbadger.com/badges/image/zer0i3/tomcat8-mysql.svg)](https://microbadger.com/images/zer0i3/tomcat8-mysql) [![](https://images.microbadger.com/badges/version/zer0i3/tomcat8-mysql.svg)](https://microbadger.com/images/zer0i3/tomcat8-mysql) [![Build Status](https://travis-ci.org/zer0i3/tomcat8-mysql-docker.svg?branch=master)](https://travis-ci.org/zer0i3/tomcat8-mysql-docker)

Uma imagem customizada para implementar o projeto da web Java com base em [tomcat8-mysql-docker]( https://github.com/m4yfly/tomcat8-mysql-docker), mais:

* Setado locales pt_BR.UTF-8
* troca do apt source para ubuntu.c3sl.ufpr.br
* JDK8
* Tomcat8.5.37
* Default mysql in ubuntu16.04

## Uso

Inicie um container:

```shell
docker run -itd --rm -p 8080:8080 computocell/tomcat8-mysql5.7
```

Configurando variaveis de ambiente do mysql:

```shell
docker run -itd --rm -p 8080:8080 --env MYSQL_USER=user --env MYSQL_USER_PWD=password computocell/tomcat8-mysql5.7
```

Variaveis de ambiente disponiveis: 

```shell
MYSQL_ROOT_PWD # Definir nova senha para o rooot 
MYSQL_USER	
MYSQL_USER_PWD # criar usuário com senha
MYSQL_USER_DB # criar um banco de dados e conceder privilégios
```

Deploy projetos Java web:

> Basta mover seu projeto para `/opt/tomcat/webapps/`
>


Dockerfile no github: [tomcat8-mysql5.7-docker](https://github.com/computocell/tomcat8-mysql5.7-docker)