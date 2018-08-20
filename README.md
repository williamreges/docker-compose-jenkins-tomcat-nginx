## Docker Compose com Jenkins e Tomcat
Através da execução do arquivo docker-compose em ambiente docker pode-se subir um ambiente pré
configurado de servidores conteinizados com Jenkins e Tomcat.


## Proposta
A proposta inicial do projeto é criar um ambiente onde possa ser utilizado Jenkins como CI/CD. E o 
servidor de aplicação é o tomcat. Para que o funcionamento de builder e deploy no tomcat tenha efeito 
é necessário configurar um job no jenkins.
O job é configurado para clonar projetos do git, buildar, testar e fazer deploy em qualquer servidor de aplicação,
como o tomcat por exemplo.

## Entendendo o Jenkins

* Site oficial do [Jenkins](https://jenkins.io/).


