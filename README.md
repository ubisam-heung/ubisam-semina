# Ubisam-Semina
유비샘 세미나 자료 정리용 리포지토리입니다.

## 자료 모음

- [[20260203] 유비샘_1차_세미나.pdf]([20260203]%20유비샘_1차_세미나.pdf)
- [[20260210] 유비샘_2차_세미나.pdf]([20260210]%20유비샘_2차_세미나.pdf)
- [[20260224] 유비샘_3차_세미나.pdf]([20260224]%20유비샘_3차_세미나.pdf)
- [[20260303] 유비샘_4차_세미나.pdf]([20260303]%20유비샘_4차_세미나.pdf)
- [[20260310] 유비샘_5차_세미나.pdf]([20260310]%20유비샘_5차_세미나.pdf)
- [[20260311] 유비샘_세미나_추가내용.pdf]([20260311]%20유비샘_세미나_추가내용.pdf)

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

---

#### Docker 이미지 다운로드 및 컨테이너 실행

MySQL, PostgreSQL, MSSQL, MariaDB 등 다양한 DB의 공식 Docker 이미지를 다운로드하고 컨테이너를 실행하는 방법을 실습합니다.
각 DB별 환경변수, 포트, 볼륨 마운트 설정 예시와 실행 명령어를 정리합니다.

---

#### VS Code에서 DB 연결 및 쿼리 테스트

VS Code 확장(Database Client, Container 등) 설치 후, JDBC 연결 설정 및 쿼리 테스트 방법을 안내합니다.
application.properties 예시와 각 DB별 설정값을 비교합니다.

---

#### pom.xml 의존성 및 Maven 설정

각 DB별 JDBC 드라이버 의존성 추가 방법과 Maven repository 설정, settings.xml 작성법을 설명합니다.

---

#### JPA 테스트 및 CRUD 코드 예시

MockMvc를 활용한 웹 요청 테스트 코드(Create, Read, Update, Delete) 작성 흐름을 공유합니다.
엔티티 저장 시 ID 자동 생성, 단일 값 조회/수정/삭제 예시를 설명합니다.

---

#### 핸들러 구현 및 이벤트 처리

@HandleBeforeCreate, @HandleAfterCreate 어노테이션을 활용한 RepositoryEventHandler 구현 및 테스트 방법을 안내합니다.

---

#### 기타 개념 및 참고 자료

Spring DI, TDD, AOP 등 핵심 개념을 간략히 정리하고, 관련 GitHub 소스 및 참고 링크를 안내합니다.

---

### 4차 세미나 (2026-03-03)

- 주제: 자바코드 기반 검색 쿼리 구현, COC 구조 적용, Vue 프론트엔드 연동 실습
- 상세 PDF: [[20260303] 유비샘_4차_세미나.pdf]([20260303]%20유비샘_4차_세미나.pdf)

자세한 내용은 PDF를 참고해주세요.

---

#### CRUD - 자바코드로 Search 쿼리 구현

- ORM 기반으로 SQL 없이 자바코드(JpaSpecificationBuilder)로 동적 검색 쿼리 작성
- HelloRepository를 RestfulJpaRepository로 변경, findAll(Specification<Hello> spec) 활용
- @HandleBeforeRead 이벤트 핸들러로 검색 전처리 및 로그 출력
- pom.xml에 querydsl-jpa 의존성 추가, @EnableRestfulJpaRepositories 설정
- Talend API Tester로 POST/GET 테스트, DB 결과 확인

---

#### 사용자의 입력 파라미터 처리

- Hello.java에 @Transient keyword 필드 추가 (DB 미저장 검색어)
- Handler에서 keyword 기반 동적 쿼리 생성 및 테스트 코드 작성
- mockMvc로 /helloes/search POST 테스트, 정상 동작 확인

---

#### COC(Convention over Configuration) 구조 적용

- example1/domain, example1/api/helloes 구조로 폴더 리팩토링
- ApplicationApiConfig에서 @EnableRestfulJpaRepositories, @EnableJpaRepositories, RepositoryRestConfigurer 구현
- config.setBasePath("/api"), config.exposeIdsFor(Hello.class, World.class) 등 REST 설정
- CORS 허용, id 노출 등 실무 설정 적용

---

#### Vue 프론트엔드 연동

- Node.js, Vue, Vuetify 설치 및 VSCode 확장 활용
- frontend1 폴더 생성, package.json 관리, npm run dev/hello 명령어 추가
- axios로 백엔드 /api/helloes/search POST 연동, 콘솔에서 결과 확인
- Vuetify 컴포넌트로 UI 구성, ESLint 설정 팁 제공

---

#### 게시판 예제 및 참고자료

- 게시판 예제 코드, RESTful API 설계, 프론트-백엔드 연동 실습
- 참고: [myownstudy-backend](https://github.com/ubisam-heung/myownstudy-backend), [myownstudy-frontend](https://github.com/ubisam-heung/myownstudy-frontend)
- 기타 참고: [Vuetify Components](https://vuetifyjs.com/en/components/all/), [Convention over Configuration(CoC)란](https://velog.io/@rkddntjd7/Convention-over-ConfigurationCoC%EB%9E%80)

---

### 5차 세미나 (2026-03-10)

- 주제: Restful Query, STOMP(WebSocket) 실습 및 이론, 자바 인터페이스 개념
- 상세 PDF: [[20260310] 유비샘_5차_세미나.pdf]([20260310]%20유비샘_5차_세미나.pdf)

자세한 내용은 PDF를 참고해주세요.

#### Restful Query 실습

---

- Repository에서 페이징(pagination)과 정렬(sort) 기능을 지원
- Talend API Tester로 POST 요청 시 `/api/helloes/search?size=1` 등으로 size 지정 가능 (기본값 20)
- `sort` 파라미터로 정렬 기준 지정 가능

---

#### STOMP(WebSocket) 실습 및 이론

- Docker로 STOMP 서버 컨테이너 실행: 
  ```bash
  docker run -d -p 9030:8080 --name ubisam-stomp-server ghcr.io/u2waremanager/io.u2ware.product.stomp-server:3.5.11
  ```
- 브라우저에서 ws://localhost:9030/stomp/websocket 접속, 채널 구독 및 메시지 송수신 실습
- Pub/Sub 구조, destination(주소) 기반 라우팅 이해
- WebSocket의 한계와 STOMP의 역할(메시지 목적지 지정, 라우팅)
- STOMP 주소 예시: `/topic/{이름}`(브로드캐스트), `/app/{이름}`(엔드포인트)

---

#### Stomp Backend Client (Spring Boot)

- pom.xml에 WebSocket, u2ware-common-stomp 의존성 추가
- application.properties에 STOMP 서버 주소 및 구독 채널 설정
- `WebsocketStompClientHandler` 인터페이스 구현, 메시지 수신/전송 예제
- 예시 코드:
  ```java
  @Component
  public class UbisamSubscriber implements WebsocketStompClientHandler {
      @Autowired public WebsocketStompProperties properties;
      @Autowired public ObjectMapper mapper;
      @Autowired public HelloRepository helloRepository;
      @Override
      public void handleFrame(WebsocketStompClient client, JsonNode message) {
          // 메시지 처리 및 DB 저장, 응답 전송
      }
      @Override
      public String getDestination() {
          return properties.getSubscriptions().get("ubisam");
      }
  }
  ```
- 서버 실행 후 브라우저에서 메시지 송수신 테스트

---

#### Stomp Frontend Client (Vue)

- npm으로 stompjs 설치: `npm install stompjs`
- stomp 폴더 및 hello.vue 생성, ws://localhost:9030/stomp/websocket로 연결
- 예시 코드:
  ```js
  import stompjs from 'stompjs';
  let url = 'ws://localhost:9030/stomp/websocket';
  let ws = stompjs.client(url);
  ws.connect({}, frame => {
      ws.subscribe('/topic/robot', message => {
          console.log('message: '+ message.body);
      });
  });
  ```
- npm run dev로 서버 실행, 브라우저에서 메시지 수신 확인

---

#### 자바 인터페이스 개념

- 인터페이스는 기능의 규약(계약, contract) 역할
- 구현 클래스는 인터페이스의 모든 메서드 구현 필수
- 다형성, 확장성, 팀 개발에서의 명확한 역할 분담에 기여
- 예시:
  ```java
  interface Payment { void pay(); }
  class CardPayment implements Payment {
      @Override public void pay() { System.out.println("카드 결제"); }
  }
  ```

---
### 세미나 추가 내용 (2026-03-11)

- 주제: COC와 Test Code 구조 개선
- 상세 PDF: [[20260311] 유비샘_세미나_추가내용.pdf]([20260311]%20유비샘_세미나_추가내용.pdf)

자세한 내용은 PDF를 참고해주세요.

## 세미나 추가 내용 (COC, Test Code 등)

### COC (Convention over Configuration)

- GitHub에서 리포지토리 생성 시 네이밍 규칙을 준수합니다.
  - 예시: `com.ubisam.projects.semina.backend` (ubisam-research 조직 규칙)
- 실제 리포지토리 생성 및 클론 과정을 실습합니다.
- 백엔드 코드 리포지토리 구조와 네이밍 규칙을 정립합니다.

---

### Test Code 구조 개선

- 기존에는 모든 테스트 코드를 `ApplicationTests.java`에 작성했으나, 이는 COC에 위배됩니다.
- 테스트 코드를 도메인별로 분리하여 작성해야 합니다.
  - 예: Hello, World 각각에 대한 테스트 클래스를 별도 생성
- 폴더 구조 예시:
  - `src/test/java/backend/api/HelloTests.java`
  - `src/test/java/backend/api/WorldTests.java`
- 실제로 test 폴더 하위에 api 폴더를 만들고, 각 도메인별 테스트 클래스를 생성합니다.

---
### 6차 세미나 (2026-03-18)

#### 주제 및 참고 자료

- STOMP 세션 구조, Publisher/Subscriber 패턴, 보안(OAuth2, Google 연동), Docker 활용, Boilerplate 코드 클론 및 실습
- 상세 PDF: [[20260318] 유비샘_6차_세미나.pdf]([20260318]%20유비샘_6차_세미나.pdf)

---

#### STOMP 추가 내용

- Session은 클라이언트이자 통신 모듈로, 생성자에서 URL을 전달하고 connect/disconnect/publish 등 메서드를 제공
- Reconnector: 5초마다 연결 상태 확인, 끊기면 재연결
- Publisher: 5초마다 JSON 메시지 발행, 장비 연동 코드 포함
- Subscriber: 주소와 콜백 함수로 메시지 수신, action 값에 따라 응답 발행
- 언어별 템플릿 제공 목표, 다양한 프로토콜 환경에서 동일 패턴 적용 가능

예시 코드:
```java
Session session = new Session();
Reconnector reconnector = new Reconnector(session);
reconnector.start();
Publisher publisher = new Publisher(session);
publisher.start();
```

---

#### 보안: Google OAuth 설정 및 Docker 실습

- Google Cloud Platform에서 프로젝트 생성, OAuth 클라이언트 ID 발급, 리디렉션 URI 설정
- Docker로 OAuth 서버 컨테이너 실행, 초기 계정 설정 및 로그인 테스트
- PostgreSQL DB 연동, application.properties 옵션 추가, DB 연결 및 테이블 생성 확인
- Google 계정 연동 옵션 추가, OAuth 서버와 연동 테스트

실습 명령어 예시:
```bash
docker run -d -p 9090:9090 -e server.port=9090 --name ubisam-oauth-server ghcr.io/u2waremanager/io.u2ware.product.oauth2-server:3.5.11
```

---

#### Stomp 서버 보안 설정 및 연동

- Stomp-server 컨테이너 실행 시 OAuth2 인증 옵션 추가
- access_token 파라미터로 STOMP Client 연결, 토큰 발급 및 연결 테스트
- 인가(Authorization) 및 Token Theft 개념 설명

실습 명령어 예시:
```bash
docker run -d -p 9030:8080 --name ubisam-oauth2-stomp-server -e spring.security.oauth2.resourceserver.jwt.issuer-uri=http://192.168.0.11:9090 -e spring.security.oauth2.resourceserver.jwt.jwk-set-uri=http://192.168.0.11:9090/oauth2/jwks ghcr.io/u2waremanager/io.u2ware.product.stomp-server:3.5.11
```

---

#### Docker Compose 활용 및 Boilerplate 코드 클론

- Dockerfile-dev.yml로 여러 컨테이너 그룹 실행, 이미지 경로 변경 및 docker compose 명령어 사용
- Google 연동 옵션 추가, 리디렉션 URL 변경, 정상 로그인 및 STOMP Client 연결 테스트
- Boilerplate backend/frontend 리포지토리 클론, .m2/settings.xml 설정, backend/frontend 서버 실행 및 테스트

실습 명령어 예시:
```bash
docker compose -f Dockerfile-dev.yml up -d
```

---


