- JPA는 기존의 반복 코드는 물론, 기본적인 SQL도 JPA가 직접 만들어 실행함.
- JPA를 사용하면, SQL과 데이터 중심의 설계에서 객체 중심의 설계로 패러다임을 전환할 수 있다.
- JPA를 사용하면 개발 생산성을 크게 높일 수 있다.

- `spring.jpa.show-sql=true` jpa가 날리는 쿼리를 볼 수 있다
- `spring.jpa.hibernate.ddl-auto=none` 회원객체를 보고 전부 테이블을 만든다. 하지만 만ㅁ들어진걸 쓸거기때문에 none으로 한다. create하면 create테이블 까지 자동으로 만들어준다

- jpa를 쓰려면 entity를 먼저 매핑해야한다
- jpa는 인터페이스만 있다. 구현은 여러업체가 한다.
- jpa는 객체랑 ORM이라는 기술이다.
- JPA는 entitymanager로 모든게 동작한다. build.gradled에서 jpa 라이브러리를 받을때 자동으로 스프링부트가 entitymanager를 생성해주기때문에 injection받으면된

- persistence는 영구화, 영구히 저장한다
- `em.createQuery("select m from Member m", Member.class)
                .getResultList();` 보통 테이블대상으로 sql을 날리는데 entity를 대상으로 sql을 날린다. 객체 자체를 select한
- findById나 CRUD같은건 쿼리를 안날려도 되는데 findByName이나 findAll 같은거는 쿼리를 쳐서 해야한- - 서비스에서 데이터 저장 변경조회할때 항상 @Transactional 이 있어야한다


cmd + option + n 인라인 -> 리턴으로 통합한다
