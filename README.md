# API RESTful com Spring Boot e Swagger

# Passos

1. [x] Criar o Projeto;
1. [x] Habilitar o Spring Boot Actuator;
1. [ ] Criar o primeiro serviço (Controller);
1. [ ] Adicionar a documentação com o Swagger;
1. [ ] Empacotar tudo em uma imagem docker;

## Criando o Projeto

Go to https://start.spring.io

Aqui vamos utilizar o Maven e o Java 11, mas fique a vontade para selecionar o que você tiver mais afinidade, ou facilidade.

> Project: [x] Maven Project   
> Language: [x] Java   
> Spring Boot: [x] 2.3.4   
> Packaging: [x] Jar   

Preencha os metadados do projeto da forma que achar melhor. 
No meu caso foi: 

> Group: br.com.rissmann.api   
> Artifact: sandbox    
> Name: sandbox   
> Package name: br.com.rissmann.api.sandbox   

**Adicione como dependência o `Spring Web`.**


Clique em "GENERATE". Faça o download e descompacte o projeto.
Em seguida, entre na pasta do projeto e compile tudo.

```shell
$ unzip sandox.zip
$ cd sandbox
sandbox> $ mvn compile
...
[INFO] BUILD SUCCESS
...
```
Pronto. Agora você tem um projeto Spring Boot.

## Habilitar o Spring Boot Actuator

Adicione a seguinte dependência ao seu `pom.xml`

```xml
<dependency>
    <groupId>org.springframework.boot</groupId>
    <artifactId>spring-boot-starter-actuator</artifactId>
</dependency>
```

Em seguida execute os comandos para limpar e empacotar:
```shell
sandbox> $ mvn clean package
...
[INFO] BUILD SUCCESS
...
```

Pronto. 

Para testar, rode a aplicação:
```
sandbox> $ java -jar target/sandbox-0.0.1-SNAPSHOT.jar
...
```
Abra o seguinte endereço no seu browser:   
 `http://localhost:8080/actuator/health`

Você verá `{"status":"UP"}`. 

Parabéns. Agora você tem um projeto Spring Boot pronto para imaplantação em ambiente de produção.

Para saber mais sobre o Spring Boot Actuator visite https://docs.spring.io/spring-boot/docs/current/reference/htmlsingle/#production-ready
