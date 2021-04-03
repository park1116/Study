# SOAP (Simple Object Access Protocol)
SOAP은 일반적으로 널리 알려진 HTTP, HTTPS, SMTP 등을 통해 XML 기반의 메시지를 컴퓨터 네트워크 상에서 교환하는 프로토콜이다.<br>
SOAP은 웹 서비스에서 기본적인 메시지를 전달하는 기반이 된다.<br>
SOAP에는 몇가지 형태의 메시지 패턴이 있지만, 보통의 경우 원격 프로시져 호출(RPC) 패턴으로, 네트워크 노드(Client)에서 다른 쪽 노드(Server)로 메시지를 요청하고, 서버는 메시지를 즉시 응답하게 된다.<br>
Envelope / header / body 로 이루어진 구조와 전송(transport)과 상호 중립성(interaction neutrality)의 개념을 가지고 있다.
### SOAP의 특징
- HTTP는 기존 원격 기술들에 비해서 프록시와 방화벽에 구애 받지 않고 쉽게 통신 가능하다.<br>
- 융통성 있게도 각각 다른 트랜스포트 프로토콜들의 사용을 허용하고 있다.<br>
- 플랫폼 독립적이고, 프로그래밍 언어에 독립적이다.<br>
- XML 포맷은 태그 형태로 보내기 때문에 CORBA같은 미들웨어 기술과 비교해서 상대적으로 느리다. 이것은 전송할 메시지가 적을 때 에는 문제 되지 않을 수 있다.
### 참고자료
https://ko.wikipedia.org/wiki/SOAP
