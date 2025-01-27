# Broken-Object-Property-Level-Authorization
### 특징: Broken Object Level Authorization와 공격 메커니즘이 비슷하니 아래 링크 참고하세요.
https://github.com/skrkcb2/OWASP-BOLA  

**Property**는 객체의 **속성**을 의미합니다. 예를 들어, `userID`가 1234인 `Member` 객체가 있다고 가정해 봅시다:

```json
{
  "userId": 1234,              #userId 속성(property)
  "password": "leeinho",       #password 속성(property)
  "email": "leeinho@gmail.com" #email 속성(property)
}
```

- ###  설명:
  우리는 **Broken Object Level Authorization**를 시연할 떄 **api/v1/profile(사용자 전체 객체)/1234** 로 테스트를 합니다. 그럼 이러한 생각을 할 수 있을 겁니다 **api/v1/email(전체 객체 중 이메일 속성)/1234** 도 존재 할거 같은데 근데 이 API가 검증이 제대로 이루어지지 않는다면? 이 의문점이 **Broken-Object-Property-Level-Authorization** 입니다.

- ### 결론:  
  **Broken Object Level Authorization:** 는 Member(사용자 전체) 객체를 다루는 api에서의 검증이 이루어지지 않을떄 이지만  
  **Broken-Object-Property-Level-Authorization:** 는 Member 객체의 email property(사용자 중 email속성)을 다루는 api에서 검증이 이루어지지 않았을 떄 입니다.
