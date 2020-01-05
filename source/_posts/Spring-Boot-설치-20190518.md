---
title: Spring Boot 설치
categories:
  - Linux
  - Swin project
  - Spring boot
tags:
  - Linux
  - Ubuntu 18.04
  - Spring boot
  - Maven
date: 2019-05-18 08:12:10
updated:
thumbnail:
comments:
---

Spring boot를 처음 다뤄보기에 잘못된 부분이 일부 있을수도 있습니다. 아래 작업은 [링크](https://docs.spring.io/spring-boot/docs/current/reference/html/getting-started-installing-spring-boot.html)를 참고하여 진행하였습니다.
 
 
 
## Spring boot 란?

{% blockquote Spring boot https://spring.io/projects/spring-boot#overview/ %}
Spring Boot makes it easy to create stand-alone, production-grade Spring based Applications that you can "just run".

We take an opinionated view of the Spring platform and third-party libraries so you can get started with minimum fuss. Most Spring Boot applications need very little Spring configuration.
{% endblockquote %}
 
 
 
## 사전작업

### Java 설치

- 설치 확인
```
java -version
```

- 설치
```
apt install default-jdk
```

### sdkman 설치

- 설치 확인
```
sdk version
```

- 설치
```
curl -s http://get.sdkman.io | bash
source "/root/.sdkman/bin/sdkman-init.sh"
```

## Spring boot 설치

- 설치 확인
```
spring --version
```

- 설치
```
sdk install springboot
```

- 생성
생성할 디렉토리에서 다음 명령어 입력
(--build는 생략 시 default: Maven)
```
spring init --build <maven/gradle> <이름>
```

- 실행
생성된 디렉토리로 이동한 후 다음 명령어 입력
```
mvn spring-boot:run
```

- 확인
http://localhost:8080 접속

주의! 접속하기 전 8080 포트가 열려있는 상태인지 확인하셔야 합니다.
