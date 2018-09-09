## Stack docker com Tomcat, Jenklins e Nginx 
Instanciação de ambiente rodando tomcat como servidor de aplicação, jenkins como serviço de CD/CD e Nginx para load balancer.

## Proposta
A proposta inicial é instalar o tomcat como serviço de aplicação e configurar o nginx como seu balanceador de carga, tudo em containeres. O Jenkins pode ser confiugado para fazer builds e deploy de projetos para dentro dos conteineres tomcat.

## Rodando projeto em clurster Swarm
### 1. Crei um cluster utlizando Docker Swarm e faça clone no repositorio:
 $ docker swarm init --advertise-addr ip-servidor-manager

### 2. Faça clone do projeto no repositório:
 $ git clone https://github.com/WilliamRegesDeveloper/docker-compose-jenkins-tomcat-nginx.git

### 3. Entre no projeto docker-compose-jenkins-tomcat clonado e rode o comando para subir os stacks de servidores configurados no arquivo docker-service3.yml:
 $ docker stack deploy --compose-file docker-service3.yml servico-docker

### 4. Veja os serviços rodando:
$ docker service ls

### 5. Entre nos serviços pelas portas externas já configuradas no arquivo docker-service3.yml:
* porta 8080 - login: sysdba; senha: masterkey;
* porta 50001 - Acesso ao serviço Jenkins;
* porta 80 - Porta do Nginx que redireciona para o servidor balanceado.


## Entendendo o Jenkins

* Site oficial do [Jenkins](https://jenkins.io/).

