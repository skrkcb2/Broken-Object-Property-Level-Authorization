# Broken-Object-Property-Level-Authorization
### 특징: Broken Object Level Authorization랑 똑같다 아래 링크 참고
https://github.com/skrkcb2/OWASP-BOLA
### 차이점: Property의 뜻을 생각하면 된다 Property는 속성으로 Broken Object Level Authorization(BOLA) 예시로 userID 1234의 Member객체({ userId: 1234, password: leeinho, email:leeinho@gmail.com})에서 Property는 userId, password, email이다 그럼 여기서 BOLA는 userId와 API endpoint /api/v1/profile?userId=1234에서 userId를 통해 타 사용자의 모든 정보를 가져왔지만 Broken-Object-Property-Level-Authorization는 여기서 더 나가아간다 /api/v1/profile이게 있다면 그럼 /api/v1/profile/email?userId=1234 도 있을 거자나? 여기서 사용자 검증 로직이 없으면 발생하는 취야점이다.
