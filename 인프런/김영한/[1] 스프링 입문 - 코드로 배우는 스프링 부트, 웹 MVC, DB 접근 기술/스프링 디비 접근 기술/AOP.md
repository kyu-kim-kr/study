### AOP가 필요한 상황

- 모든 메서드의 호출시간을 측정하고 싶다면?
- 공통 관심사항 (cross-cutting concern) vs 핵심 관심 사항 (core concern)

#### 문제

- 회원가입, 회원 조회에 시간을 측정하는 기능은 핵심 관심 사항이 아니다
- 시간을 측정하는 로직은 공통 관심 사항이다.
- 시간을 측정하는 로직은 핵심 비즈니스의 로직이 섞여서 유지보수가 어렵다
- 시간을 측정하는 로직을 별도의 공통 로직으로 만들기 매우어렵다
- 시간을 측정하는 로직을 변경할 때 모든 로직을 찾아가면서 변경해야한다

### 동작방식

- AOP 적용전 의존관계는 helloController -> memberService   
- AOP 적용후 의존관계 helloController -> 프록서 memberService -> joinPoint.preoceed() -> 실제 memberService
