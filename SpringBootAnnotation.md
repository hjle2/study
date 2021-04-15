# springboot_Annotations
### @SpringBootApplcation
 + 스프링 부트의 자동 설정, 스프링 Bean 읽기와 생성을 몯 자동 설정
 + 이 위치부터 설정을 읽어나가기 때문에 프로젝트의 최상단에 위치해야 함

### @RestController
 + __JSON__을 반환하는 컨트롤러로 설정

### @GetMapping
 - ex) @GetMapping("/hello")
 + HTTP Method 중 Get의 요청으 받는 API로 설정

### @RunWith(SpringRunner.class)
 + 테스트 진행시 JUnit에 내장되 실행자 외에 다른 실행자(SpringRunner) 실행 시키는 설정
 + 스프링 부트 테스트와 JUnit사이 연결자 역할

### @WebMvcTest
 + Web(Spring MVC)에 집중할 수 있는 어노테이션
 + 선언할 경우 @Controller, @rAdvice 등은 사용 가능
 + @Service, @Component, @Repository 등은 사용 불가
 + JPA 기능이 작동하지 않음

### @Autowired
 + 스프링이 관리하는 빈을 주입 받음

### @Getter
 + 선언된 모든 필드의 get 메소드 생성

### @RequiredArgsConstructor
 + 선언된 모든 final필득 포함된 생성자 생성
 + final이 없는 필드는 생성자에 미포함

### @NoArgsConstructor
 + 기본 생성자 생성
 
### @Builder
 + 해당 클래스으 빌더 패턴 클랫 생성
 + 생성자 상단에 선언 시에는 생성자에 포함된 필드만 빌더에 포함

### @RequestParam
 - ex) @RequestParam("name") String name 
 + name 이라는 이름으로 넘긴 파라미터를 name에 저장
 + 외부에서 API로 넘긴 파라미터르 가져오는 어노테이션

### @Entity
 + 테이블과 링크될 클래스
 + 기본값으로 클래스의 카멜케이스 이름을 언더스코어 네이밍으로 테이블 이름을 매칭
 + 필드의 값 변경 위치 혼란스럽기 때문에 Entity 클래스에서는 절대 Setter 메소드를 생성하지 않아야 함

### @Id
 + 해당 테이블의 PK필드
 + 웬만하면 Auto_increament를 추천(bigint type)

### @GeneratedValue
 + PK의 생성 규칙

### @Column
 + 테이블의 칼럼을 의미하며 선언하지 않아도 @Entity선언 된 클래스의 필드는 모두 칼럼임
 + 기본값 외에 추가로 변경이 필요한 옵션을 위 사용

### @MappedSuperclass
 + JPA Entity 클래스가 해당 어노테이션이 선언된 클래스를 상속할 경우, 해당 클래스의 필드들도 칼럼으로 인식

### @EntityListeners(AuditingEntityListener.class)
 + 해당 클래스에 Auditing기능 포함시킴

### @CreatedDate
 + Entity가 생성되어 저장될 때 시간이 자동 저장

### @LastModifiedDate
 + 조회하 Entity의 값을 변경할 때의 시간이 자동 저장됨

### @After
 + Junit에서 단위테스트가 끝날 때마다 수행되는 메소드를 지정
 + 배포 전 전체 테스트 시 테스트간 데이터 침범을 막기 위해 사용

### @SpringBootTest
 + 별도의 설정 없이 H2 데이터 베이스를 자동으로 실행

### @Target(ElementType.PARAMETER)
 + 이 어노테이션이 생성될 수 있는 위치 지정
 + ANNOTATION TYPE, PARAMETER, TYPE, FIELD, CONSTRUCTOR 등의 ElemetType 사용 가능
 + 선언된 ElementType 과 같은 타입을 선언된 객체에서만 사용 가능

### @interface
- ex) public @interface LoginUser
+ LoginUser라는 이름을 가진 어노테이션 클래스로 지정하여 해당 이름으 어노테이션 사용 가능

### @WithMockUser(roles="USER")
 - 인증된 모의 사용자를 만들어 사용
 - MockMvc에서만 동작

