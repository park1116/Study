# Servlet (서블릿)
클라이언트의 요청을 처리하고, 그 결과를 반환하는 Servlet 클래스의 구현 규칙을 지킨 자바 웹 프로그래밍 기술이다.<br>
클라이언트가 어떠한 요청을 하면 그에 대한 결과를 다시 전송해주는 역할을 하는 자바 프로그램이다.<br>
일반적으로 웹 서버는 정적인 페이지만을 제공한다. 그렇기 때문에 동적인 페이지를 제공하기 위해서 웹 서버는 다른 곳에 도움을 요청하여 동적인 페이지를 작성해야 한다. 이때 웹 서버가 동적인 페이지를 제공할 수 있도록 도와주는 어플리케이션이 서블릿이다.

### Servlet 특징
- 클라이언트의 요청에 대해 동적으로 작동하는 웹 어플리케이션 컴포넌트
- Html을 사용하여 요청에 응답한다.
- Java thread를 이용하여 동작한다
- MVC패턴에서 Controller로 이용된다.
- HTTP프로토콜 서비스를 지원하는 javax.servlet.http.HttpServlet 클래스를 상속받는다.
- UDP보다 처리 속도가 느리다.
- HTML 변경 시 Servlet을 재컴파일해야 하는 단점이 있다.
### Servlet 동작 방식
1. 클라이언특 URL을 입력하면 HTTP Request가 Servlet Container로 전송한다.
2. 요청을 전송받은 Servlet Container는 HtppServletRequest, HttpServletResponse 객체를 생성한다.
3. Web.xml을 기반으로 사용자가 요청한 URL이 어느 서블릿에 대한 요청인지 찾는다.
4. 해당 서블릿에서 service메소드를 호출한 후 클라이언트의 GET, POST여부에 따라서 doGet() 또는 doPost()를 호출한다.
5. doGet() 또는 doPost() 메소드는 동적 페이지를 생성한 후 HttpServletResponse객체에 응답을 보낸다.
6. 응답이 끝나면 HttpServletRequest, HttpServletResponse 두 객체를 소멸시킨다.
### 참고자료
https://mangkyu.tistory.com/14

