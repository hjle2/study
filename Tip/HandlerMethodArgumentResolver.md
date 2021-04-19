# HandlerMethodArgumentResolver
### - 컨트롤러 메서드에 "특정 조건"에 맞는 파라미터가 있을 때 원하는 값을 바인딩 해주는 인터페이스
- Controller에서 @RequestBody 어노테이션을 이용해 Body 값을 받아올 때,
@PathVariable 어노테이션으로 Path Parameter 값을 받아올 때 사용하여 값을 받아온다.

## 사용 방법
### 1. 어노테이션 작성해주기
 - @Target(ElementType.PARAMETER)
 - @Rentention(RetentionPolicy.RUNTIME) 어노테이션을 클래스 정의 위에 선언

### 2. Controller 어노테이션 추가
 - Parameter 에(@CustonResolver Object objec) 작성

### 3. Resolver 작성하기
 - HandlerMethodArgumentResolver 를 상속핟아 작성
 - override 해야하는 메서드 두가지 작성
 - supportsParameter 메서드에 현재 파라미터를 resolver 이 지원하는 지 여부에 대한 boolean 리턴
 - resolveArgument 메서드는 실제로 바인딩할 객체 리턴

### 4. resolver 를 스프링에 등록
 - 
    @Override
    public void addArgumentResolvers(List<HandlerMethodArgumentResolver> argumentResolvers) {
        argumentResolvers.add(customHandlerMethodArgumentResolver);
    }
  
  [참고!](https://velog.io/@kingcjy/Spring-HandlerMethodArgumentResolver%EC%9D%98-%EC%82%AC%EC%9A%A9%EB%B2%95%EA%B3%BC-%EB%8F%99%EC%9E%91%EC%9B%90%EB%A6%AC)
