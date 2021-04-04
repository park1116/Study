# WAS (Web Application Server)
웹 브라우저와 같은 클라이언트로부터 웹 서버가 요청을 받으면 애플리케이션에 대한 로직을 실행하여 웹 서버로 다시 반환해주는 소프트웨어이다.<br>
웹 서버는 웹 브라우저 클라이언트로부터 HTTP 요청을 받아 정적인 컨텐츠(HTML, CSS, IMAGE 등)를 제공하는 컴퓨터 프로그램이다.<br>
WAS는 DB조회나 다양한 로직 처리를 요구하는 동적인 컨텐츠(JSP, ASP, PHP 등)를 제공하기 위해 만들어진 Application Server이다.<br>
WAS는 웹 컨테이너(Web Container) 혹은 서블릿 컨테이너(Servlet Container) 라고 불린다. Container란 JSP, Servlet을 실행시킬 수 있는 소프트웨어를 말한다. 즉, WAS는 JSP, Servlet 구동 환경을 제공한다.
### Web Server와 WAS를 나눠야 하는 이유
WAS는 웹 서버 + 웹 컨테이너 개념이라 웹 서버가 없더라도 웹 서버의 역할을 동시에 수행할 수 있다. 그렇지만 웹 서버와 WAS를 나눠서 사용한다.
#### 1. 기능을 분리하여 서버 부하 방지<br>
웹 서버는 정적인 컨텐츠를 처리하고 WAS는 동적인 컨텐츠를 처리한다. <br>
만약 부하가 적다면 문제없지만, 부하가 많다면 굳이 빠른 시간에 처리할 수 있는 정적 컨텐츠를 WAS에서 처리하여 부하를 줄 필요가 없다.
#### 2. 물리적으로 분리하여 보안 강화<br>
SSL에 대한 암복호화 처리에 WebServer를 사용한다.
#### 3. 여러 대의 WAS를 연결 가능<br>
Load Balancing을 위해서 Web Server를 사용한다.<br>
대용량 웹 어플리케이션의 경우(여러 개의 서버 사용) Web Server와 WAS를 분리하여 무중단 운영을 위한 장애 극복에 쉽게 대응할 수 있다.<br>
예를 들어, 앞 단의 Web Server에서 오류가 발생한 WAS를 이용하지 못하도록 한 후 WAS를 재시작함으로써 사용자는 오류를 느끼지 못하고 이용할 수 있다.
#### 4. 여러 웹 어플리케이션 서비스 가능<br>
하나의 서버에서 PHP Application 과 Java Application을 함께 사용하는 경우가 있다.<br>
즉, 자원 이용의 효율성 및 장애 극복, 배포 및 유지보수의 편의성을 위해 Web Server와 WAS를 분리한다.
### 참고자료
https://gmlwjd9405.github.io/2018/10/27/webserver-vs-was.html
https://goldsony.tistory.com/37

