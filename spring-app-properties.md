# Spring Boot `application.properties` Cheat Sheet

Este cheat sheet contém algumas das propriedades mais comuns que você pode configurar em seu arquivo `application.properties` do Spring Boot. 

**Observação:** Esta não é uma lista exaustiva. Para mais informações e opções de configuração, consulte a [documentação oficial do Spring Boot](https://docs.spring.io/spring-boot/docs/current/reference/html/application-properties.html).

## Geral

| Propriedade                        | Descrição                                                                                                                                            | Exemplo                               |
|---------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------|
| `spring.application.name`        | Define o nome da aplicação.                                                                                                                                 | `spring.application.name=myapp`        |
| `spring.profiles.active`         | Define o perfil ativo da aplicação.                                                                                                                             | `spring.profiles.active=dev,test`      |
| `spring.main.banner-mode`        | Controla a exibição do banner de inicialização. (Valores: "console", "log", "off")                                                                         | `spring.main.banner-mode=off`          |
| `spring.main.allow-bean-definition-overriding` | Permite que definições de beans sejam sobrescritas. (Valores: "true", "false")                                                                   | `spring.main.allow-bean-definition-overriding=true` |

## Servidor Web

| Propriedade                        | Descrição                                                                                                                                                 | Exemplo                      |
|---------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------|
| `server.port`                    | Define a porta em que o servidor web irá escutar.                                                                                                              | `server.port=8080`            |
| `server.servlet.context-path`    | Define o caminho de contexto da aplicação.                                                                                                                    | `server.servlet.context-path=/api` |
| `server.tomcat.max-threads`      | Define o número máximo de threads que o servidor Tomcat pode criar para lidar com requisições.                                                                  | `server.tomcat.max-threads=200` |
| `server.tomcat.connection-timeout` | Define o tempo limite em milissegundos para conexões com o servidor Tomcat.                                                                                       | `server.tomcat.connection-timeout=5000` |
| `server.error.whitelabel.enabled` | Define se a página de erro padrão do Spring Boot (Whitelabel Error Page) deve ser habilitada. (Valores: "true", "false")                                      | `server.error.whitelabel.enabled=false` |

## Banco de Dados

| Propriedade                                  | Descrição                                                                                           | Exemplo                                                   |
|-----------------------------------------------|----------------------------------------------------------------------------------------------------|------------------------------------------------------------|
| `spring.datasource.url`                        | Define a URL de conexão com o banco de dados.                                                        | `spring.datasource.url=jdbc:mysql://localhost:3306/mydb` |
| `spring.datasource.username`                  | Define o nome de usuário para conectar ao banco de dados.                                             | `spring.datasource.username=root`                        |
| `spring.datasource.password`                  | Define a senha para conectar ao banco de dados.                                                        | `spring.datasource.password=password`                        |
| `spring.datasource.driver-class-name`          | Define o nome da classe do driver JDBC.                                                              | `spring.datasource.driver-class-name=com.mysql.cj.jdbc.Driver` |
| `spring.jpa.hibernate.ddl-auto`               | Define a estratégia de criação de tabelas do Hibernate. (Valores: "none", "validate", "update", "create", "create-drop") | `spring.jpa.hibernate.ddl-auto=update`                    |
| `spring.jpa.show-sql`                          | Habilita o log das instruções SQL geradas pelo Hibernate. (Valores: "true", "false")                    | `spring.jpa.show-sql=true`                               |
| `spring.jpa.properties.hibernate.format_sql` | Formata as instruções SQL geradas pelo Hibernate no log. (Valores: "true", "false")                     | `spring.jpa.properties.hibernate.format_sql=true`          |


## Segurança

| Propriedade                     | Descrição                                                                                 | Exemplo                               |
|---------------------------------|---------------------------------------------------------------------------------------------|----------------------------------------|
| `spring.security.user.name`      | Define o nome de usuário padrão para autenticação básica.                                   | `spring.security.user.name=user`       |
| `spring.security.user.password`  | Define a senha padrão para autenticação básica.                                      | `spring.security.user.password=password` |
| `spring.security.oauth2.resourceserver.jwt.jwk-set-uri` | Define a URL para o JWK Set usado para validação de tokens JWT. | `spring.security.oauth2.resourceserver.jwt.jwk-set-uri=https://example.com/oauth2/jwks` |

## Logging

| Propriedade                             | Descrição                                                                                                                   | Exemplo                                           |
|------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------|
| `logging.level.root`                  | Define o nível de log raiz. (Valores: "TRACE", "DEBUG", "INFO", "WARN", "ERROR", "FATAL", "OFF")                                 | `logging.level.root=INFO`                         |
| `logging.level.org.springframework`     | Define o nível de log para o pacote `org.springframework`.                                                                 | `logging.level.org.springframework=DEBUG`            |
| `logging.file.name`                    | Define o nome do arquivo de log.                                                                                          | `logging.file.name=application.log`                |
| `logging.file.path`                    | Define o diretório onde o arquivo de log será criado.                                                                        | `logging.file.path=/var/log`                       |
| `logging.pattern.console`              | Define o padrão de formatação para o log no console.                                                                        | `logging.pattern.console=%d{yyyy-MM-dd HH:mm:ss.SSS} %-5level %logger{36} - %msg%n` |
| `logging.pattern.file`                 | Define o padrão de formatação para o log no arquivo.                                                                         | `logging.pattern.file=%d{yyyy-MM-dd HH:mm:ss.SSS} %-5level %logger{36} - %msg%n` |

**Lembre-se que esta lista não é exaustiva.** 

Existem muitas outras propriedades que podem ser configuradas no arquivo `application.properties`. Para mais informações, consulte a [documentação oficial do Spring Boot](https://docs.spring.io/spring-boot/docs/current/reference/html/application-properties.html).
