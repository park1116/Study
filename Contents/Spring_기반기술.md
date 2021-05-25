# Spring 기반기술
스프링부트에서는 자바 소스(Java Config)로 설정을 하지만 스프링은 Servlet으로 자바 소스 설정을 한다.
### Servlet
자바를 사용하여 웹 페이지를 동적으로 생성하는 서버측 프로그램이다.  
Servlet은 Servlet Container에 의해 괸리, 실행된다.  
**HTTP Server + Servlet Container**가 웹 서버에 필요한 대부분을 구현했고, 개발자는 Servlet을 만들어 HTTP 요청을 받아 처리하는 부분을 구현하는 것이다.  
요청(Request)과 응답(Response) 즉, HTTP 웹 서버 기능 동작이 가능하다.
### Tomcat
웹 애플리케이션 서버(WAS)중 하나로 Servlet Container, Servlet Engine 이라고 표현할 수 있고 자바 웹 프로그래머가 작성한 Servlet을 관리한다. Servlet을 관리한다는 말은 클라이언트가 어떤 요청(Request)을 했을 때, 어떤 Servlet을 실행할 것인지 제어해 주는 것이다.  
Tomcat은 Servlet을 관리해주는 주체이기 때문에 아무 클래스가 아니라 Servlet(HttpServlet 클래스를 상속한 클래스)이어야 한다.
### web.xml
WAS는 Servlet을 생성하고 어떤 Servlet이 어떤 요청을 담당할 것인지, 어떤 요청이 인증과정을 거칠 것인지 등의 제어 기능을 지원한다.  
이때 WAS에 servlet에 대한 정보를 주는 파일이 web.xml(Deployment Descriptor)이다.
### DispatcherServlet
Servlet Container로부터 들어오는 요청을 관제하는 컨트롤러라고 할 수 있다.  
Spring MVC에서 요청을 받는 부분이다.  
Servlet Container에 여러 매핑 정보를 가진 여러 Servlet을 생성하고 관리할 수 도 있지만 일반적으로는 Servlet Container에는 DispatcherServlet만 등록해놓고 DispatcherServlet이 HandlerMapping을 통해 적절한 Controller로 매핑하도록 한다.
### Servlet Filter
Servlet 실행 전, 후에 어떤 작업을 하고자할 때 Servlet Filter를 사용한다.  
Interceptor를 사용할 수 있겠지만 차이점은 실행시점(handler 전, 후)에 차이가 있다.  
Filter는 Servlet Container에 등록하고 Interceptor는 스프링 컨테이너에 등록한다,
### Servlet Context
Servlet 단위로 생성되는 Context이다.  
Servlet Container에 DispatcherServlet과 같은 Servlet을 등록하면 해당 Servlet이 갖는 하나의 작은 컨테이너 역할을 하는 객체이다.  
스프링을 이용하는 경우, 스프링 컨테이너(Application Context)를 부모 Context로 사용한다.  
Application Context와 Servlet Context에 같은 id로 된 Bean이 있으면 Servlet Context에 있는 Bean을 우선 사용한다. (Bean을 찾는 순서가 Servlet에서 Servlet Context를 확인한 후에 부모인 Application Context를 확인하기 때문이다.)
### Application Context
Root Context이자 스프링에 의해 생성되는 Bean에 대한 Spring IoC Container이다.  
Beanfactory를 상속받는 Context이다.  
여러 Servlet에서 공통으로 사용할 Bean을 등록하는 Context이다.
### ContextLoaderListener
Servlet Container에 Application Context를 등록하는 방법을 제공한다.  
Servlet Container의 시작과 종료 시에 발생하는 이벤트를 처리하는 리스너를 등록하기 위해 ServletContextListener 인터페이스를 구현한 리스너를 사용하는데 그 구현체가 바로 ContextLoaderListener 이다.  
Application Context에 대한 실제 초기화 작업을 수행한다.  
ContextLoaderListener를 등록하면 자동으로 디폴트 Application Context를 생성한다.
### RequestContextListener
현재 스레드에 요청(Request)을 노출하는 Servlet Listener이다.  
RequestContextListenr를 등록하면 LocaleCOntextHolder, RequestContextHolder를 통해서 HttpServletRequest에 접근할 수 있게 한다.

### 참고 자료
https://jeong-pro.tistory.com/222
