# Memo

Spring Boot와 JPA를 활용하여 메모를 생성, 조회, 수정, 삭제(CRUD)할 수 있는 REST API 프로젝트입니다.

---

# 프로젝트 소개

메모를 효율적으로 관리하기 위한 백엔드 애플리케이션입니다.
Spring Boot의 계층형 아키텍처(Controller-Service-Repository)를 적용하여 CRUD 기능을 구현하였으며, JPA를 이용한 데이터베이스 연동과 REST API 설계를 학습하는 것을 목표로 개발했습니다.

---

# 기술 스택

* Java 21
* Spring Boot
* Spring Data JPA
* MySQL
* Gradle
* Lombok

---

# 프로젝트 구조

```
src
 ├── controller
 ├── service
 ├── repository
 ├── entity
 └── dto
```

---

# 주요 기능

## 메모 등록

```http
POST /memo
```

새로운 메모를 생성합니다.

---

## 메모 전체 조회

```http
GET /memo
```

저장된 모든 메모를 조회합니다.

---

## 메모 단건 조회

```http
GET /memo/{id}
```

ID를 이용하여 메모를 조회합니다.

---

## 메모 수정

```http
PUT /memo/{id}
```

기존 메모의 내용을 수정합니다.

---

## 메모 삭제

```http
DELETE /memo/{id}
```

선택한 메모를 삭제합니다.

---

# 데이터베이스

MySQL을 사용하며 JPA를 통해 테이블을 자동 생성합니다.

```properties
spring.datasource.url=jdbc:mysql://localhost:3306/memo
spring.datasource.username=사용자명
spring.datasource.password=비밀번호

spring.jpa.hibernate.ddl-auto=update
spring.jpa.show-sql=true
```

---

# 실행 방법

### 저장소 클론

```bash
git clone <Repository_URL>
```

### 프로젝트 실행

```bash
./gradlew bootRun
```

또는 IntelliJ IDEA에서 실행 버튼을 눌러 실행할 수 있습니다.

---

# 학습 내용

* Spring Boot 프로젝트 구성
* REST API 설계
* Controller-Service-Repository 계층 분리
* Spring Data JPA 활용
* CRUD 기능 구현
* MySQL 연동
* Git & GitHub를 활용한 버전 관리

---

# 향후 개선 사항

* 예외 처리(Global Exception Handler)
* 입력값 검증(Validation)
* 페이징 기능
* 검색 기능
* Swagger(OpenAPI) 적용
* 테스트 코드 작성

---

# 프로젝트 목적

Spring Boot 기반의 CRUD 애플리케이션을 직접 구현하며 REST API 개발 방식과 JPA를 활용한 데이터 관리 방법을 익히기 위한 프로젝트입니다. 계층형 아키텍처를 적용하여 유지보수성과 확장성을 고려한 백엔드 개발 경험을 쌓는 것을 목표로 했습니다.
