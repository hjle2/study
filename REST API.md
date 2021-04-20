# REST API
 > Representational State Transfer
 > Resource URI
 > Verb HTTP Method
 > Representations

## 1. GET

## 2. PUT

## 3. POST 

## 4. PATCH (?)

## 5. DELETE

* 멱등성 : 여러번 수행해도 결과가 같음 (Idempotence)
* POST 만 제외하고 모든 메소드는 멱등성을 갖는다.

자원의 일부만 변경할 때는 PATCH, 자원의 전체적인 수정이 필요할 때는 PUT?
PUT 은 전체 엔티티를 전달해줘야 하고, 전달해주지 않은 값은 전부 null이 된다.
PATCH 는 변경하고자 하는 속성만 전달하면 나머지 값은 기존 값을 유지한다.
