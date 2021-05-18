# JPA
자바 ORM 기술에 대한 표준 명세로, JAVA에서 제공하는 API이다. Spring에서 제공하는 것이 아니다.  
자바 어플리케이션에서 관계형 데이터베이스를 사용하는 방식을 정의한 인터페이스이다.  
JPA는 말 그대로 인터페이스이지 특정 기능을 하는 라이브러리가 아니다.  
기존 EJB에서 제공되던 Entity bean을 대체하는 기술이다.  
ORM이기 때문에 자바 클래스와 DB테이블을 매핑한다. SQL을 매핑하지 않는다.  
### ORM과 SQL Mapper 비교
ORM은 DB 테이블을 자바 객체로 매핑함으로써 객체간의 관계를 바탕으로 SQL을 자동으로 생성하는 것이다.  
Mapper는 SQL을 명시해주어야 한다.  
ORM은 RDB의 관계를 Object에 반영하는 것이 목적이다.  
Mapper는 단순히 필드를 매핑시키는 것이 목적이다.  
### JPA 동작 과정
 ![image](https://user-images.githubusercontent.com/55124370/118620757-c3d59f80-b800-11eb-9a52-ebeddf3e88a7.png)  
JPA는 애플리케이션과 JDBC 사이에서 동작한다.  
개발자가 JPA를 사용하면, JPA 내부에서 JDBC API를 사용하여 SQL을 호출하여 DB와 통신한다.  
즉, 개발자가 직접 JDBC API를 쓰는 것이 아니다.
### JPA의 특징
- 데이터를 객체지향적으로 관리할 수 있기 때문에 개발자는 비즈니스 로직에 집중할 수 있고 객체지향 개발이 가능하다.
- 자바 객체와 DB 테이블 사이의 매핑 설정을 통해 SQL을 생성한다.
- 객체를 통해 쿼리를 작성할 수 있는 JPQL(Java Persistence Query Language)를 지원한다.
- JPA는 성능향상을 위해 지연 로딩이나 즉시 로딩과 같은 몇 가지 기법을 제공하는데 잘 활용하면 SQL을 직접 사용하는 것과 유사한 성능을 낼 수 있다.
### JPA를 사용해야 하는 이유
1. Sql 중심적인 개발에서 객체 중심적인 개발 가능  
Sql 코드의 반복을 제거할 수 있다.
2.	생산성 증가  
간단한 메소드로 CRUD가 가능하다.
3.	유지보수 용이  
필드 변경 시 SQL을 수정할 필요 없이 필드만 수정하면 JPA가 처리한다.
4.	Object와 RDB 간의 패러다임 불일치 해결
### 참고자료
https://velog.io/@adam2/JPA%EB%8A%94-%EB%8F%84%EB%8D%B0%EC%B2%B4-%EB%AD%98%EA%B9%8C-orm-%EC%98%81%EC%86%8D%EC%84%B1-hibernate-spring-data-jpa

