# Agenda

## Call Helper

### [Useful Link in IT](./useful-link.md)

### [Userful Contact Window](./useful-contact.md)

## Dev VM Environment Setup

### [Apply for a DevVM](./dev-vm.md)

### [Windows Software setup/check](./guide/dev-vm-windows.md)

#### Setup Development Tools

- Chocolatey
- Scoop

#### [for Backend]

- [Java]
  - JDK
    - Version:17+
    - Environment variable
  - Maven
    - Version:3.9+
    - settings.xml
    - .m2 folder destination
    [Check Maven](./verify/maven.md)
  - VS Code
    - Java Extension Pack
    - Java Debugger
    - Java Test Runner
    - Java Debug Terminal
    - Maven for Java
      - settings.json for maven path
      - settings.json
  - Intellij
    - ...
- [Python]
  - Python
    - pip
  - venv
  - PyCharm

- [Others....ex:DBeaver]

- [....]

#### [for Frontend]

- Node.js
  - npm server config
- Angular
  - ...
- React
  - ...

#### [for CI/CD]

- Docker
  - Docker Desktop
  - Harbor setting
- Git
  - Gitlab Configuration
  - Azure DevOps Configuration
  - VS Code
    - Cline

#### [for Others Optional]

- K8s Kind
- Teams PWA
- SourceTree
- WSL2
- Dev Container
  - if you use wsl2, you can use dev container

### [Linux vm setup and check](./dev-vm-linux.md)

- apt
- yum

#### [for Backend]

#### [for Frontend]

#### [for CI/CD]

#### [for Others Optional]

---

## Workshop

### [Backend Java Development](./workshop/backend-java-development.md)

#### Chapter 1: Basic Spring Boot Project

AR:
//how about Acceptance Criteria for this chapter

1. A executable springboot jar file
2. Include some api end point can communicate with browser
  2.1 show me "hello world"
  2.2 can calculate_divide
  2.3 can throw exception
  2.4 can log in different level
  2.5 can store/read data in csv file
  2.6 can store/read data in database
  2.7 can pass unit test

DoD:

  //how about Done Definition for this chapter

Backlog:

  //How about your plan backlog in this chapter

Tutorial

- [ Beggining ]
  0. Introduction
  1. IOC & DI
  2. AOP
  3. Logback & SLF4J
   3.1 loglevel: debug, info, warn, error
   3.2 logback.xml
   3.3 logback-spring.xml
  4. POM.xml Structure
  5. Basic Maven command line SHOULD KNOWN
   5.0 Maven Lifecycle
   5.1 mvn clean compile
   5.2 mvn clean test
   5.3 mvn clean package
   5.4 mvn clean verify
   5.5 mvn clean install
   5.6 mvn clean deploy
   5.7 mvn clean site
   5.8 mvn spring-boot:run
   5.9 mvn spring-boot:run -Dspring-boot.run.profiles=dev
   5.10 mvn spring-boot:run -DskipTests

- [ REST API ]
  - MVC Architecture
  - GET
  - POST

- [ Simple Unit Test ]
  - JUnit 5
  - Spring Boot Test
  - VSCode Test Runner
  - VSCode Debug Terminal

#### Chapter 2: TodoList Backend Project

AR:
  
  //how about Acceptance Criteria for this chapter

DoD:

  //how about Done Definition for this chapter

Backlog:

  //How about your plan backlog in this chapter

Tutorial:

- [ Data Access ]
  - JDBCTemplate
  - ORM & JPA
  - MyBatis/MyBatis Plus

- [ External Service Calling ]
  - RestTemplate call
  - Async RestTemplate call
  - gRPC call

- [ Test by Mock ]
  - Mockito
  - MockBean
  - MockRestTemplate
  - MockMvc

#### Chapter 3: Secure your TodoList Backend Project

AR:

DoD:

Backlog:

Tutorial:

- [ Security ]
  - Security Architecture
    - Filter Chain
    - Security Filter
    - Security Configuration
  - JWT
    - JWT with Spring Security
    - JWT with JJWT
    - JWT with Keycloak
  - OIDC
    - OIDC with Spring Security
    - OIDC with Keycloak
  - OAuth2
    - OAuth2 with Spring Security
    - OAuth2 with Keycloak
  - SAML
    - SAML with Spring Security
    - SAML with Keycloak
  - tSSO

  - A4

#### Chapter 4: Batch/Scheduler Backend Project

AR:

DoD:

Backlog:

Tutorial:

- [ Batch Scheduling ]
- [ Batch Processing ]
- [ Job Scheduling ]
- [ Job Orchestrating ]

### [Backend Python Development](./workshop/python.md)

#### Chapter $M: XXXXXXXX Project

AR:
  
  //how about Acceptance Criteria for this chapter

DoD:

  //how about Done Definition for this chapter

Backlog:

  //How about your plan backlog in this chapter

Tutorial:

- [ Xxxxxxxxx ]
- [ Xxxxxxxxx ]

### [Frontend Angular Development](./workshop/angular.md)

#### Chapter $N: XXXXXXXX Project

AR:
  
  //how about Acceptance Criteria for this chapter

DoD:

  //how about Done Definition for this chapter

Backlog:

  //How about your plan backlog in this chapter

Tutorial:

- [ Xxxxxxxxx ]
- [ Xxxxxxxxx ]

### [Frontend React Development](./workshop/react.md)

#### Chapter $O: XXXXXXXX Project

AR:
  
  //how about Acceptance Criteria for this chapter

DoD:

  //how about Done Definition for this chapter

Backlog:

  //How about your plan backlog in this chapter

Tutorial:

- [ Xxxxxxxxx ]
- [ Xxxxxxxxx ]

### [CI/CD]

#### Chapter $P: XXXXXXXX Project

AR:
  
  //how about Acceptance Criteria for this chapter

DoD:

  //how about Done Definition for this chapter

Backlog:

  //How about your plan backlog in this chapter

Tutorial:

- [ Xxxxxxxxx ]
- [ Xxxxxxxxx ]

### [Observability]

#### Chapter $Q: XXXXXXXX Project

AR:

DoD:

Backlog:

Tutorial:

- [ Xxxxxxxxx ]
- [ Xxxxxxxxx ]

### [SRE/Monitoring]

#### Chapter $R: XXXXXXXX Project

AR:
  
  //how about Acceptance Criteria for this chapter

DoD:

  //how about Done Definition for this chapter

Backlog:

  //How about your plan backlog in this chapter

Tutorial:

- [ Xxxxxxxxx ]
- [ Xxxxxxxxx ]

### [AICopilot]

#### Chapter $S: XXXXXXXX Project

AR:
  
  //how about Acceptance Criteria for this chapter

DoD:

  //how about Done Definition for this chapter

Backlog:

  //How about your plan backlog in this chapter

Tutorial:

- [ Xxxxxxxxx ]
- [ Xxxxxxxxx ]

### [$Others....]

#### Chapter $T: XXXXXXXX Project

AR:
  
  //how about Acceptance Criteria for this chapter

DoD:

  //how about Done Definition for this chapter

Backlog:

  //How about your plan backlog in this chapter

Tutorial:

- [ Xxxxxxxxx ]
- [ Xxxxxxxxx ]
