# Ubisam-Semina
유비샘 세미나 자료 정리용 리포지토리입니다.

## 자료 모음

- [[20260203] 유비샘_1차_세미나.pdf]([20260203]%20유비샘_1차_세미나.pdf)
- [[20260210] 유비샘_2차_세미나.pdf]([20260210]%20유비샘_2차_세미나.pdf)
- [[20260224] 유비샘_3차_세미나.pdf]([20260224]%20유비샘_3차_세미나.pdf)

## 세미나 정리

### 1차 세미나 (2026-02-03)

- 주제: VS Code 기반 Spring Boot/JPA 기본 흐름 정리
- 상세 PDF: [[20260203] 유비샘_1차_세미나.pdf]([20260203]%20유비샘_1차_세미나.pdf)

자세한 내용은 PDF를 참고해주세요.

#### 시작과 프로젝트 생성

VS Code 문서 소개와 확장팩 설치, `Create a Maven Project` 실행 흐름을 안내합니다.
Java 버전은 17/21을 선택하고, 기본 패키지 경로와 프로젝트 타입(Jar)을 설정합니다.
필수 의존성(Rest Repositories, Spring Data JPA, Lombok, HyperSQL)을 추가합니다.

---

#### 기본 개념과 설정

JDBC 개념과 `pom.xml`의 `dependencies` 위치를 설명합니다.
`application.properties` 설정 화면을 보여주고, JPA/SQL 로그 옵션과 `ddl-auto`, `logging.level` 의미를 정리합니다.

---

#### 프로젝트 구조

mvnw/mvnw.cmd, `pom.xml`, `src/main/java`, `src/main/resources`, `src/test/java`의 역할을 요약합니다.
`Example1Application`과 테스트 클래스 위치를 확인합니다.

---

#### 엔티티와 코드 스타일

`Hello.java` 생성과 클래스 네이밍 규칙(PascalCase)을 소개합니다.
`@Entity`, `@Data`의 의미와 getter/setter/equals/hashCode 생성 흐름을 설명합니다.
setter 작성 형식을 예시로 보여줍니다.

---

#### equals/hashCode 이해

`equals()` 비교 예시와 사용 목적을 설명합니다.
`hashCode()` 규칙과 구현 예시를 함께 정리합니다.

---

#### ORM/JPA 구조

테이블명 설정과 ORM/JPA/Hibernate 관계를 정리합니다.
`HelloRepository`를 `JpaRepository`로 구성하고 실행 후 테이블 생성 여부를 확인합니다.

---

#### 테스트와 CRUD 흐름

테스트 클래스에서 컨텍스트 로드와 `@Autowired` 주입을 설명합니다.
insert 로그 확인, `System.out.println` 팁, `Optional` 사용 이유(존재/부재)를 설명합니다.
`@GeneratedValue`로 ID 할당, `save()`와 영속성 흐름을 정리합니다.
update/delete/search 결과와 `findAll()` 빈 리스트 출력 이유를 설명합니다.

---

#### 복합키와 마무리

`@EmbeddedId` 복합키 소개와 `HelloRepository` 제네릭 변경을 설명합니다.
`findByEmail`, `findByNameAndEmail` 테스트 코드 결과를 공유합니다.
예제 소스 GitHub 링크와 세미나 마무리 메시지를 안내합니다.

### 2차 세미나 (2026-02-10)

- 주제: Data REST로 컨트롤러 없이 CRUD 실습, Talend API Tester 활용
- 상세 PDF: [[20260210] 유비샘_2차_세미나.pdf]([20260210]%20유비샘_2차_세미나.pdf)

자세한 내용은 PDF를 참고해주세요.

#### 시작과 실행 확인

VS Code 문서 소개 후, 기존 `Hello.java` 프로젝트에서 `mvnw spring-boot:run` 실행을 확인합니다.
Tomcat 시작 로그와 애플리케이션 기동 메시지를 확인합니다.

---

#### Talend 설치와 준비

Talend API Tester 설치 링크를 안내하고, Chrome 확장프로그램 추가 과정을 설명합니다.
확장 아이콘 확인과 Talend 고정(pin), 초기 화면 진입을 정리합니다.

---

#### GET/POST 기본 흐름

GET 요청으로 `/helloes` 결과 구조를 확인합니다.
POST 요청으로 생성하고 `@GeneratedValue`로 ID 자동 생성, JSON 바디 입력을 설명합니다.

---

#### 조회/수정/삭제 실습

GET으로 생성 데이터 확인, `/helloes/1` 조회 흐름을 설명합니다.
PUT 요청으로 수정 후 재조회, DELETE 요청과 삭제 결과 확인을 정리합니다.

---

#### Data REST와 COC

`/helloes` 자동 생성 이유(Data REST + `JpaRepository`)를 설명합니다.
COC 개념과 패키지 구조 적용, 리팩토링 의미를 정리합니다.

---

#### REST 개념 확장

`/worlds` 추가 확인과 REST 개념(Self Description, State Transfer)을 설명합니다.
참고 영상 링크를 안내합니다.

---

#### GitHub 실습

리포지토리 생성(README, .gitignore, License 설정) 절차를 정리합니다.
Settings에서 Wiki/Discussion 활성화, Discussion 화면 확인을 안내합니다.
Wiki 작성, 위키 주소 복사, README 편집과 Markdown 링크 문법을 설명합니다.
커밋 메시지 입력 후 README 반영 확인까지 정리합니다.

---

### 3차 세미나 (2026-02-24)

- 주제: Docker를 활용한 데이터베이스 컨테이너 실습 및 VS Code 연동
- 상세 PDF: [[20260224] 유비샘_3차_세미나.pdf]([20260224]%20유비샘_3차_세미나.pdf)

자세한 내용은 PDF를 참고해주세요.

#### Docker 이미지 다운로드 및 컨테이너 실행

MySQL, PostgreSQL, MSSQL, MariaDB 등 다양한 DB의 공식 Docker 이미지를 다운로드하고 컨테이너를 실행하는 방법을 실습합니다.
각 DB별 환경변수, 포트, 볼륨 마운트 설정 예시와 실행 명령어를 정리합니다.

#### VS Code에서 DB 연결 및 쿼리 테스트

VS Code 확장(Database Client, Container 등) 설치 후, JDBC 연결 설정 및 쿼리 테스트 방법을 안내합니다.
application.properties 예시와 각 DB별 설정값을 비교합니다.

#### pom.xml 의존성 및 Maven 설정

각 DB별 JDBC 드라이버 의존성 추가 방법과 Maven repository 설정, settings.xml 작성법을 설명합니다.

#### JPA 테스트 및 CRUD 코드 예시

MockMvc를 활용한 웹 요청 테스트 코드(Create, Read, Update, Delete) 작성 흐름을 공유합니다.
엔티티 저장 시 ID 자동 생성, 단일 값 조회/수정/삭제 예시를 설명합니다.

#### 핸들러 구현 및 이벤트 처리

@HandleBeforeCreate, @HandleAfterCreate 어노테이션을 활용한 RepositoryEventHandler 구현 및 테스트 방법을 안내합니다.

#### 기타 개념 및 참고 자료

Spring DI, TDD, AOP 등 핵심 개념을 간략히 정리하고, 관련 GitHub 소스 및 참고 링크를 안내합니다.

---