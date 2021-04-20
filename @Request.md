# @RequestParam
 - http 요청 파라미터를 변수로 받는다.
 - 예를 들어, http://localhost:8080/user/login?id=hjle2 를 받기 위해서
 - @GetMapping(path="/user/login")
 - public RETURNTYPE getId(@RequestParam(value="id", required=false) String id)
 - 로 받을 수 있따.
 - required는 default 값 true일 경우 파라미터가 반드시 있어야 한다.
 - defaultValue = "value" <= value 대신 원하는 초기값을 설정할 수 있다.

# @PathVariable
- 중괄호에 명시된 값을 변수로 받는다. 
- @RequestMapping("/user/{id}")
- public String getUserId(@PathVariable("id") String id)

# @RequestBody
 - HTTP 요청의 body 부분을 그대로 변수로 받는다.
 - 주로 XML, JSON 을 받을 때 사용한다.

# @CookieValue 
 - HTTP 요청의 쿠키정보를 받는다.

# @RequestHeader
 - HTTP 요청의 헤더정보를 가져온다.
 - @RequestHeader("Header") String Header

