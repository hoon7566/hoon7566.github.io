---
layout: post
title: Just Pickup
---

## 프로젝트 기획 배경 [Github Link](https://github.com/Development-team-1/just-pickup/) 
### 기획배경
현업에서 오래된 모놀리틱 서비스를 유지보수 해보면서 프로그램은 점점 노후화되고, 새로운 기술을 적용하기에는 프로그램의 의존성에 묶여 시도하기가 힘든 환경이 되가면서 점점 MSA에 관심이 가게 되었습니다.

---


![기획이미지]({{ site.baseurl }}/images/Untitled.png) 



그래서 기술적용에 자유롭고 도메인 변경에 유연하게 대처할수 있는 MSA를 적용한 프로젝트를 만들어보자는 생각을 가졌습니다. 같은 고민을 가지고 있는 개발자 2명이 모여서 MSA을 적용한 프로젝트인 Just pickup!을 기획하였습니다. Just pickup! 이란 사용자가 카페로 간단하게 주문을 넣어서 단지 픽업을 하면 된다는 뜻으로 만들었습니다.


저희는 프로젝트 생명주기 동안 이벤트 스토밍을 적용하였으며 **[(!이벤트스토밍 링크)](https://github.com/Development-team-1/just-pickup#%EC%9D%B4%EB%B2%A4%ED%8A%B8-%EC%8A%A4%ED%86%A0%EB%B0%8D-event-storming)**

이슈에 유연하게 대처하기 위해 github issue를 적극 활용하였습니다.

### 기술

spring cloud 오픈소스 기반으로 마이크로 서비스 아키텍처를 설계하여 개발하였습니다.

---

## 아키텍처
![system architecture](https://user-images.githubusercontent.com/72686708/161487968-9d8795be-efdd-4f2d-97ea-d2c21ecaf5fb.png)
- Spring Boot
    - Spring Framwork 2.6.3
    - Java 11
    - Gradle
    - Spring Web MVC
    - Spring Security

- Spring Cloud
    - Eureka
    - Gateway
    - OpenFeign
    - Config
    - Redis Rate Limiter
- Authenticate
    - JWT (Json Web Token)
    - OAuth 2.0
- ORM
    - JPA
    - QueryDsl
- Message Queue
    - Kafka
- Database
    - PostgreSQL
    - Redis
- Test
    - Spring RestDocs
- 모니터링
    - Zipkin
    - Spring Cloud Sleuth
- Vue
    - Vue-Router
    - axios
    - Vuetify
 
1. JWT 토큰을 이용한 로그인, 회원가입 구현
2. Kafka를 사용해 이벤트 드리븐 아키텍처 구현
3. RestDocs를 이용한 테스트 작성 및 API 문서 작성
4. Open Feign을 이용한 인터페이스 형식의 HTTP 통신 구현 
5. reactive redis를 사용하여 api 호출 과부화를 막는 rate limiter 구현

## 주요 이슈 [💡Link](https://github.com/Development-team-1/just-pickup/issues) 

---

- API Rate Limiter
- JPA Fetch Join과 페이징
- Service간 데이터 join시 최적화