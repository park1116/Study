# Spring Framework
Java 엔터프라이즈 개발을 편하게 해주는 오픈소스 경량급 애플리케이션 프레임워크이다.  
개발자가 복잡하고 실수하기 쉬운 Low Level에 많이 신경 쓰지 않으면서 Business Logic 개발에 전념할 수 있도록 해준다.  
단순한 웹컨테이너에서도 엔터프라이즈 개발의 고급기술을 대부분 사용할 수 있다.  
특정 계층이나 기술, 업무 분야에 국한되지 않고 애플리케이션의 전 영역을 포괄하는 범용적인 프레임워크를 말한다.  
### Spring의 전략
1. **Portable Service Abstraction(서비스 추상화)**  
트랜잭션 추상화, OXM 추상화, 데이터 액세스의 Exception 변환기능 등 기술적인 복잡함은 추상화를 통해 Low Level의 기술구현부분과 기술을 사용하는 인터페이스로 분리한다.  
2. **POJO (Plain Old Java Object)**  
스프링은 내부적으로 객체 간의 관계를 구성할 때 별도의 API 등을 사용하지 않는 POJO (Plain Old Java Object)만으로 구성이 가능하도록 되어있다. 따라서, 일반적인 Java 코드를 이용하여 객체를 구성하는 방식 그대로 스프링에서 사용 가능하다.  
이것은 특정한 라이브러리나 컨테이너에 기술이 종속적이지 않다는 것을 의미한다. 이로 인하여 개발자는 가장 일반적인 형태로 코드를 작성하고 실행할 수 있기 때문에 높은 생산성과 유연한 테스트를 할 수 있는 장점을 갖게 된다.  
3. **DI (Dependency Injection, 의존성 주입)**  
스프링은 그 자체가 구조를 설계할 수 있도록 만들어져 있어서 개발자가 부품을 만들어 조립하는 형태의 개발이 가능하다. 이렇게 조립된 코드의 최종 호출은 개발자가 결정하는 것이 아니라 프레임워크 내부에서 결정된 대로 이루어지게 되는데 이것을 **제어의 역행(IOC, Inversion of Control)** 이라고 한다.  
의존성 주입(DI, Dependency Injection)은 제어의 역행이 일어나는 것을 전제 조건으로 하여 스프링 내부의 개체(스프링에서는 bean이라는 용어로 표현)들 간의 관계를 관리할 때 사용된다. 의존성 주입은 말 그대로 특정 객체에 필요한 객체를 외부에서 결정하여 연결시키는 것을 의미한다. 쉽게 설명하면 자바에서 인터페이스를 사용하여 의존적인 관계를 처리하는 것에 비유할 수 있다.  
의존성 주입의 종류는 생성자를 통한 주입과 set 메서드를 이용한 주입으로 구분할 수 있으며, 이에 대한 처리는 간단한 어노테이션으로 대체할 수 있다.  
4. **AOP (Aspect Oriented Programming, 관점 지향 프로그래밍)**  
스프링은 AOP를 통해 반복적인 코드를 줄이고 개발자가 핵심 비즈니스 Logic에만 집중할 수 있도록 지원한다.  
대부분의 시스템에서 비즈니스 Logic은 아니지만 보안, 로그, 트랜잭션과 같이 반드시 처리가 필요한 부분을 스프링에서는 횡단 관심사 (cross-concern)라고 한다. AOP는 이러한 횡단 관심사를 별도 모듈로 분리하는 프로그래밍 패러다임이다.
### Spring Framework 특징
-	**컨테이너 역할**  
Spring 컨테이너는 Java 객체의 LifeCycle을 관리하며, Spring 컨테이너로부터 필요한 객체를 가져와 사용할 수 있다.
-	**DI(Dependency Injection) 지원**  
Spring은 설정파일이나 어노테이션을 통해서 객체 간의 의존관계를 설정할 수 있도록 하고있다.
-	**AOP(Aspect Oriented Programing) 지원**  
Spring은 트랜젝션이나 로깅, 보안과 같은 공통적으로 필요로 하는 모듈들을 실제 핵심 모듈에서 분리해서 적용할 수 있다.
-	**POJO(Plain Old Java Object) 지원**  
Spring 컨테이너에 저장되는 Java 객체는 특정한 인터페이스를 구현하거나, 특정클래스를 상속받지 않아도 된다.
-	**트랜젝션 처리를 위한 일관된 방법을 지원**  
Spring에서는 트랜잭션 처리는 어노테이션이나 XML로 설정할 수 있도록 지원해준다. JDBC, JTA등 어떤 트랜젝션을 사용하던 설정을 통해 정보를 관리하므로 트랜젝션 구현에 상관없이 동일한 코드가 사용가능하다.
-	**영속성과 관련된 다양한 API 지원**  
Spring은 Mybatis, Hibernate 등 데이터베이스 처리를 위한 ORM(Object Relational Mapping) 프레임워크들과의 연동을 지원한다.
### Spring Framework의 기능요소
 ![image](https://user-images.githubusercontent.com/55124370/117561894-ab190b80-b0d5-11eb-82cd-cdff2e974c1e.png)
-	**Core 컨테이너**  
Core 컨테이너는 Spring Framework의 기본기능을 제공한다. 이 모듈에 있는 BeanFactory는 Spring의 기본 컨테이너이면서 스프링 DI의 기반이다.
-	**Context**  
Context모듈은 BeanFactory의 개념을 확장한 것으로 국제화(I18N)메시지, 애플리케이션 생명주기 이벤트, 유효성 검증을 지원한다.
-	**DAO**  
DAO 패키지는 JDBC에 대한 추상화 계층으로 JDBC 코딩이나 예외처리하는 부분을 간편화 시켰으며, AOP 모듈을 이용해 트랜젝션 관리 서비스도 제공한다.
-	**ORM**  
Mybatis, Hibernate, JPA 등 널리 사용되는 ORM 프레임워크와의 연결고리를 제공한다. ORM 제품들을 Spring의 기능과 조합해서 사용할 수 있도록 해준다.
-	**AOP**  
AOP 모듈을 통해 Aspect 지향 프로그래밍을 지원한다. AOP 모듈은 스프링 애플리케이션에서 Aspect를 개발할 수 있는 기반을 지원한다.
-	**Web**  
일반적인 웹애플리케이션 개발에 필요한 기본기능을 제공하고, Webwork나 Struts와 같은 다른 웹 애플리케이션 프레임워크와의 통합을 지원한다.
-	**WebMVC**  
MVC(Model/View/Controller) 패러다임은 사용자 인터페이스가 애플리케이션 로직과 분리되는 웹 애플리케이션을 만드는 경우에 일반적으로 사용되는 패러다임이다. 이 패러다임을 바탕으로 웹 계층에서 결합도를 낮추는 Spring MVC 프레임워크가 있다.

### 참고자료
https://shlee0882.tistory.com/200  
https://velog.io/@msriver/Spring-2%EC%9E%A5-%EC%8A%A4%ED%94%84%EB%A7%81%EC%9D%98-%ED%8A%B9%EC%A7%95%EA%B3%BC-%EC%9D%98%EC%A1%B4%EC%84%B1-%EC%A3%BC%EC%9E%85
